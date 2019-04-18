---
id: B3B3F30E-6399-493A-9338-A4606CD362FD
---

## Namespace Android

### Type Changed: Android.Manifest

### Type Changed: Android.Manifest.Permission

Obsoleted fields:

```
[Obsolete ()]
	public static const string BindCarrierMessagingService = "android.permission.BIND_CARRIER_MESSAGING_SERVICE";
```

Added fields:

<pre style='color: green'>
	public static const string AccessNotificationPolicy = "android.permission.ACCESS_NOTIFICATION_POLICY";
	public static const string BindCarrierServices = "android.permission.BIND_CARRIER_SERVICES";
	public static const string BindChooserTargetService = "android.permission.BIND_CHOOSER_TARGET_SERVICE";
	public static const string BindIncallService = "android.permission.BIND_INCALL_SERVICE";
	public static const string BindMidiDeviceService = "android.permission.BIND_MIDI_DEVICE_SERVICE";
	public static const string BindTelecomConnectionService = "android.permission.BIND_TELECOM_CONNECTION_SERVICE";
	public static const string GetAccountsPrivileged = "android.permission.GET_ACCOUNTS_PRIVILEGED";
	public static const string PackageUsageStats = "android.permission.PACKAGE_USAGE_STATS";
	public static const string RequestIgnoreBatteryOptimizations = "android.permission.REQUEST_IGNORE_BATTERY_OPTIMIZATIONS";
	public static const string RequestInstallPackages = "android.permission.REQUEST_INSTALL_PACKAGES";
	public static const string UseFingerprint = "android.permission.USE_FINGERPRINT";
</pre>

### Type Changed: Android.Manifest.Permission_group

Added fields:

<pre style='color: green'>
	public static const string Contacts = "android.permission-group.CONTACTS";
	public static const string Phone = "android.permission-group.PHONE";
	public static const string Sensors = "android.permission-group.SENSORS";
	public static const string Sms = "android.permission-group.SMS";
</pre>

### Type Changed: Android.Resource

### Type Changed: Android.Resource.Attribute

Obsoleted fields:

```
[Obsolete ()]
	public static const int AmPmBackgroundColor;
	[Obsolete ()]
	public static const int AmPmTextColor;
	[Obsolete ()]
	public static const int DayOfWeekBackground;
	[Obsolete ()]
	public static const int DayOfWeekTextAppearance;
	[Obsolete ()]
	public static const int DirectionDescriptions;
	[Obsolete ()]
	public static const int FocusedMonthDateColor;
	[Obsolete ()]
	public static const int HeaderAmPmTextAppearance;
	[Obsolete ()]
	public static const int HeaderDayOfMonthTextAppearance;
	[Obsolete ()]
	public static const int HeaderMonthTextAppearance;
	[Obsolete ()]
	public static const int HeaderTimeTextAppearance;
	[Obsolete ()]
	public static const int HeaderYearTextAppearance;
	[Obsolete ()]
	public static const int SelectedDateVerticalBar;
	[Obsolete ()]
	public static const int SelectedWeekBackgroundColor;
	[Obsolete ()]
	public static const int ShownWeekCount;
	[Obsolete ()]
	public static const int ShowOnLockScreen;
	[Obsolete ()]
	public static const int ShowWeekNumber;
	[Obsolete ()]
	public static const int TargetDescriptions;
	[Obsolete ()]
	public static const int UnfocusedMonthDateColor;
	[Obsolete ()]
	public static const int WeekNumberColor;
	[Obsolete ()]
	public static const int WeekSeparatorLineColor;
	[Obsolete ()]
	public static const int YearListItemTextAppearance;
	[Obsolete ()]
	public static const int YearListSelectorColor;
```

Added fields:

<pre style='color: green'>
	public static const int AllowUndo;
	public static const int AutoVerify;
	public static const int BreakStrategy;
	public static const int ColorBackgroundFloating;
	public static const int ContextClickable;
	public static const int DrawableTint;
	public static const int DrawableTintMode;
	public static const int End;
	public static const int ExtractNativeLibs;
	public static const int FingerprintAuthDrawable;
	public static const int Fraction;
	public static const int FullBackupContent;
	public static const int HyphenationFrequency;
	public static const int LockTaskMode;
	public static const int LogoDescription;
	public static const int NumbersInnerTextColor;
	public static const int ScrollIndicators;
	public static const int ShowForAllUsers;
	public static const int Start;
	public static const int SubtitleTextColor;
	public static const int SupportsAssist;
	public static const int SupportsLaunchVoiceAssistFromKeyguard;
	public static const int ThumbPosition;
	public static const int TitleTextColor;
	public static const int TrackTint;
	public static const int TrackTintMode;
	public static const int UsesCleartextTraffic;
	public static const int WindowLightStatusBar;
</pre>

### Type Changed: Android.Resource.Id

Added fields:

<pre style='color: green'>
	public static const int AccessibilityActionContextClick;
	public static const int AccessibilityActionScrollDown;
	public static const int AccessibilityActionScrollLeft;
	public static const int AccessibilityActionScrollRight;
	public static const int AccessibilityActionScrollToPosition;
	public static const int AccessibilityActionScrollUp;
	public static const int AccessibilityActionShowOnScreen;
	public static const int PasteAsPlainText;
	public static const int Redo;
	public static const int ReplaceText;
	public static const int ShareText;
	public static const int Undo;
</pre>

### Type Changed: Android.Resource.String

Added field:

<pre style='color: green'>
	public static const int FingerprintIconContentDescription;
</pre>

### Type Changed: Android.Resource.Style

Added fields:

<pre style='color: green'>
	public static const int TextAppearanceMaterialWidgetButtonInverse;
	public static const int ThemeMaterialLightLightStatusBar;
	public static const int ThemeOverlayMaterialDialog;
	public static const int ThemeOverlayMaterialDialogAlert;
	public static const int WidgetMaterialButtonColored;
</pre>

## Namespace Android.Accounts

### Type Changed: Android.Accounts.AbstractAccountAuthenticator

Added field:

<pre style='color: green'>
	public static const string KeyCustomTokenExpiry = "android.accounts.expiry";
</pre>

### Type Changed: Android.Accounts.AccountManager

Added field:

<pre style='color: green'>
	public static const string KeyLastAuthenticatedTime = "lastAuthenticatedTime";
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public static Android.Content.Intent NewChooseAccountIntent (Account selectedAccount, System.Collections.Generic.IList<Account> allowableAccounts, string[] allowableAccountTypes, bool alwaysPromptForAccount, string descriptionOverrideText, string addAccountAuthTokenType, string[] addAccountRequiredFeatures, Android.OS.Bundle addAccountOptions);
```

Added methods:

<pre style='color: green'>
	public static Android.Content.Intent NewChooseAccountIntent (Account selectedAccount, System.Collections.Generic.IList&lt;Account&gt; allowableAccounts, string[] allowableAccountTypes, string descriptionOverrideText, string addAccountAuthTokenType, string[] addAccountRequiredFeatures, Android.OS.Bundle addAccountOptions);
	public virtual bool NotifyAccountAuthenticated (Account account);
</pre>

## Namespace Android.App

### Type Changed: Android.App.Activity

Added properties:

<pre style='color: green'>
	public virtual bool IsVoiceInteraction { get; }
	public virtual bool IsVoiceInteractionRoot { get; }
	public Android.Views.SearchEvent SearchEvent { get; }
	public virtual VoiceInteractor VoiceInteractor { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void OnProvideAssistContent (Assist.AssistContent outContent);
	public virtual Android.Net.Uri OnProvideReferrer ();
	public virtual void OnRequestPermissionsResult (int requestCode, string[] permissions, Android.Content.PM.Permission[] grantResults);
	public virtual bool OnSearchRequested (Android.Views.SearchEvent searchEvent);
	public virtual void OnStateNotSaved ();
	public virtual Android.Views.ActionMode OnWindowStartingActionMode (Android.Views.ActionMode.ICallback callback, Android.Views.ActionModeType type);
	public void RequestPermissions (string[] permissions, int requestCode);
	public virtual bool ShouldShowRequestPermissionRationale (string permission);
	public virtual bool ShowAssist (Android.OS.Bundle args);
	public virtual void ShowLockTaskEscapeMessage ();
	public virtual Android.Views.ActionMode StartActionMode (Android.Views.ActionMode.ICallback callback, Android.Views.ActionModeType type);
</pre>

### Type Changed: Android.App.ActivityManager

Added field:

<pre style='color: green'>
	public static const string ActionReportHeapLimit = "android.app.action.REPORT_HEAP_LIMIT";
</pre>

Obsoleted properties:

```
[Obsolete ()]
	public virtual bool IsInLockTaskMode { get; }
```

Added property:

<pre style='color: green'>
	public virtual LockTaskMode LockTaskModeState { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void ClearWatchHeapLimit ();
	public virtual void SetWatchHeapLimit (long pssSize);
</pre>

### Type Changed: Android.App.ActivityManager.RecentTaskInfo

Added properties:

<pre style='color: green'>
	public Android.Content.ComponentName BaseActivity { get; set; }
	public int NumActivities { get; set; }
	public Android.Content.ComponentName TopActivity { get; set; }
</pre>

### Type Changed: Android.App.ActivityManager.RunningAppProcessInfo

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const Importance ImportanceForegroundService;

	[Obsolete]
	public static const Importance ImportanceTopSleeping;
</pre>

### Type Changed: Android.App.ActivityOptions

Added fields:

<pre style='color: green'>
	public static const string ExtraUsageTimeReport = "android.activity.usage_time";
	public static const string ExtraUsageTimeReportPackages = "android.usage_time_packages";
</pre>

Added methods:

<pre style='color: green'>
	public static ActivityOptions MakeBasic ();
	public static ActivityOptions MakeClipRevealAnimation (Android.Views.View source, int startX, int startY, int width, int height);
	public virtual void RequestUsageTimeReport (PendingIntent receiver);
</pre>

### Type Changed: Android.App.AlarmManager

Added methods:

<pre style='color: green'>
	public virtual void SetAndAllowWhileIdle (AlarmType type, long triggerAtMillis, PendingIntent operation);
	public virtual void SetExactAndAllowWhileIdle (AlarmType type, long triggerAtMillis, PendingIntent operation);
</pre>

### Type Changed: Android.App.AlertDialog

Modified constructors:

```
protected AlertDialog (Android.Content.Context context, int theme themeResId)
```

Obsoleted fields:

```
[Obsolete ()]
	public static const int ThemeDeviceDefaultDark;
	[Obsolete ()]
	public static const int ThemeDeviceDefaultLight;
	[Obsolete ()]
	public static const int ThemeHoloDark;
	[Obsolete ()]
	public static const int ThemeHoloLight;
	[Obsolete ()]
	public static const int ThemeTraditional;
```

### Type Changed: Android.App.AlertDialog.Builder

Modified constructors:

```
public AlertDialog (Android.Content.Context context, int theme themeResId)
```

Obsoleted methods:

```
[Obsolete ()]
	public virtual AlertDialog.Builder SetInverseBackgroundForced (bool useInverseBackground);
```

### Type Changed: Android.App.AppOpsManager

Added fields:

<pre style='color: green'>
	public static const string OpstrAddVoicemail = "android:add_voicemail";
	public static const string OpstrBodySensors = "android:body_sensors";
	public static const string OpstrCallPhone = "android:call_phone";
	public static const string OpstrCamera = "android:camera";
	public static const string OpstrMockLocation = "android:mock_location";
	public static const string OpstrReadCalendar = "android:read_calendar";
	public static const string OpstrReadCallLog = "android:read_call_log";
	public static const string OpstrReadCellBroadcasts = "android:read_cell_broadcasts";
	public static const string OpstrReadContacts = "android:read_contacts";
	public static const string OpstrReadExternalStorage = "android:read_external_storage";
	public static const string OpstrReadPhoneState = "android:read_phone_state";
	public static const string OpstrReadSms = "android:read_sms";
	public static const string OpstrReceiveMms = "android:receive_mms";
	public static const string OpstrReceiveSms = "android:receive_sms";
	public static const string OpstrReceiveWapPush = "android:receive_wap_push";
	public static const string OpstrRecordAudio = "android:record_audio";
	public static const string OpstrSendSms = "android:send_sms";
	public static const string OpstrSystemAlertWindow = "android:system_alert_window";
	public static const string OpstrUseFingerprint = "android:use_fingerprint";
	public static const string OpstrUseSip = "android:use_sip";
	public static const string OpstrWriteCalendar = "android:write_calendar";
	public static const string OpstrWriteCallLog = "android:write_call_log";
	public static const string OpstrWriteContacts = "android:write_contacts";
	public static const string OpstrWriteExternalStorage = "android:write_external_storage";
	public static const string OpstrWriteSettings = "android:write_settings";
</pre>

Added methods:

<pre style='color: green'>
	public virtual AppOpsManagerMode NoteProxyOp (string op, string proxiedPackageName);
	public virtual AppOpsManagerMode NoteProxyOpNoThrow (string op, string proxiedPackageName);
	public static string PermissionToOp (string permission);
</pre>

### Type Changed: Android.App.Dialog

Modified constructors:

```
public Dialog (Android.Content.Context context, int theme themeResId)
```

Added property:

<pre style='color: green'>
	public Android.Views.SearchEvent SearchEvent { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool OnSearchRequested (Android.Views.SearchEvent searchEvent);
	public virtual Android.Views.ActionMode OnWindowStartingActionMode (Android.Views.ActionMode.ICallback callback, Android.Views.ActionModeType type);
</pre>

### Type Changed: Android.App.Fragment

Added properties:

<pre style='color: green'>
	public virtual Android.Content.Context Context { get; }
	public Java.Lang.Object Host { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void OnAttach (Activity activity);
	[Obsolete ()]
	public virtual void OnInflate (Activity activity, Android.Util.IAttributeSet attrs, Android.OS.Bundle savedInstanceState);
```

Added methods:

<pre style='color: green'>
	public virtual void OnAttach (Android.Content.Context context);
	public virtual void OnInflate (Android.Content.Context context, Android.Util.IAttributeSet attrs, Android.OS.Bundle savedInstanceState);
	public virtual void OnRequestPermissionsResult (int requestCode, string[] permissions, Android.Content.PM.Permission[] grantResults);
	public void RequestPermissions (string[] permissions, int requestCode);
	public virtual bool ShouldShowRequestPermissionRationale (string permission);
</pre>

### Type Changed: Android.App.Importance

Added values:

<pre style='color: green'>
	ForegroundService = 125,
	TopSleeping = 150,
</pre>

### Type Changed: Android.App.Instrumentation

Obsoleted methods:

```
[Obsolete ()]
	public virtual void StartAllocCounting ();
	[Obsolete ()]
	public virtual void StopAllocCounting ();
```

### Type Changed: Android.App.KeyguardManager

Added property:

<pre style='color: green'>
	public virtual bool IsDeviceSecure { get; }
</pre>

### Type Changed: Android.App.Notification

Added field:

<pre style='color: green'>
	public static const string CategoryReminder = "reminder";
</pre>

Added property:

<pre style='color: green'>
	public virtual Android.Graphics.Drawables.Icon SmallIcon { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual Android.Graphics.Drawables.Icon GetLargeIcon ();
</pre>

### Type Changed: Android.App.Notification.Action

Modified properties:

```
public virtual int Android.Graphics.Drawables.Icon Icon { get; set; }
```

### Type Changed: Android.App.Notification.Builder

Added constructors:

<pre style='color: green'>
	public Notification (Android.Graphics.Drawables.Icon icon, Java.Lang.ICharSequence title, PendingIntent intent);
	public Notification (Android.Graphics.Drawables.Icon icon, string title, PendingIntent intent);
</pre>

### Type Changed: Android.App.Notification.BigPictureStyle

Added method:

<pre style='color: green'>
	public virtual Notification.BigPictureStyle BigLargeIcon (Android.Graphics.Drawables.Icon icon);
</pre>

### Type Changed: Android.App.Notification.Builder

Obsoleted methods:

```
[Obsolete ()]
	public virtual Notification.Builder AddAction (int icon, Java.Lang.ICharSequence title, PendingIntent intent);
	[Obsolete ()]
	public Notification.Builder AddAction (int icon, string title, PendingIntent intent);
```

Modified methods:

```
public virtual Notification.Builder SetLargeIcon (Android.Graphics.Bitmap icon b)
```

Added methods:

<pre style='color: green'>
	public virtual Notification.Builder SetLargeIcon (Android.Graphics.Drawables.Icon icon);
	public virtual Notification.Builder SetSmallIcon (Android.Graphics.Drawables.Icon icon);
</pre>

### New Type Android.App.CarExtender

<pre style='color: green'>
public sealed class CarExtender : Java.Lang.Object, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public Notification ();
	public Notification (Notification notif);
	// properties
	public int Color { get; }
	public Android.Graphics.Bitmap LargeIcon { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Notification.Builder Extend (Notification.Builder builder);
	public Notification.CarExtender.UnreadConversation GetUnreadConversation ();
	public Notification.CarExtender SetColor (Android.Graphics.Color color);
	public Notification.CarExtender SetLargeIcon (Android.Graphics.Bitmap largeIcon);
	public Notification.CarExtender SetUnreadConversation (Notification.CarExtender.UnreadConversation unreadConversation);

	// inner types
	public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected Notification (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public Notification (string name);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual Notification.CarExtender.Builder AddMessage (string message);
		public virtual Notification.CarExtender.UnreadConversation Build ();
		public virtual Notification.CarExtender.Builder SetLatestTimestamp (long timestamp);
		public virtual Notification.CarExtender.Builder SetReadPendingIntent (PendingIntent pendingIntent);
		public virtual Notification.CarExtender.Builder SetReplyAction (PendingIntent pendingIntent, RemoteInput remoteInput);
	}
	public class UnreadConversation : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected Notification (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		public virtual long LatestTimestamp { get; }
		public virtual string Participant { get; }
		public virtual PendingIntent ReadPendingIntent { get; }
		public virtual RemoteInput RemoteInput { get; }
		public virtual PendingIntent ReplyPendingIntent { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual string[] GetMessages ();
		public virtual string[] GetParticipants ();
	}
}
</pre>

### Type Changed: Android.App.NotificationManager

Added fields:

<pre style='color: green'>
	public static const string ActionInterruptionFilterChanged = "android.app.action.INTERRUPTION_FILTER_CHANGED";
	public static const string ActionNotificationPolicyAccessGrantedChanged = "android.app.action.NOTIFICATION_POLICY_ACCESS_GRANTED_CHANGED";
	public static const string ActionNotificationPolicyChanged = "android.app.action.NOTIFICATION_POLICY_CHANGED";
</pre>

Added properties:

<pre style='color: green'>
	public InterruptionFilter CurrentInterruptionFilter { get; }
	public virtual bool IsNotificationPolicyAccessGranted { get; }
	public virtual NotificationManager.Policy NotificationPolicy { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual Android.Service.Notification.StatusBarNotification[] GetActiveNotifications ();
	public void SetInterruptionFilter (InterruptionFilter interruptionFilter);
</pre>

### Type Changed: Android.App.PendingIntent

Added method:

<pre style='color: green'>
	public void Send (Android.Content.Context context, Result code, Android.Content.Intent intent, PendingIntent.IOnFinished onFinished, Android.OS.Handler handler, string requiredPermission, Android.OS.Bundle options);
</pre>

### Type Changed: Android.App.PendingIntentFlags

Added value:

<pre style='color: green'>
	Immutable = 67108864,
</pre>

### Type Changed: Android.App.SharedElementCallback

Added method:

<pre style='color: green'>
	public virtual void OnSharedElementsArrived (System.Collections.Generic.IList&lt;string&gt; sharedElementNames, System.Collections.Generic.IList&lt;Android.Views.View&gt; sharedElements, SharedElementCallback.IOnSharedElementsReadyListener listener);
</pre>

### Type Changed: Android.App.TimePickerDialog

Modified constructors:

```
public TimePickerDialog (Android.Content.Context context, TimePickerDialog.IOnTimeSetListener callBack listener, int hourOfDay, int minute, bool is24HourView)
	public TimePickerDialog (Android.Content.Context context, int theme themeResId, TimePickerDialog.IOnTimeSetListener callBack listener, int hourOfDay, int minute, bool is24HourView)
```

### Type Changed: Android.App.WallpaperManager

Added property:

<pre style='color: green'>
	public virtual bool IsWallpaperSupported { get; }
</pre>

### New Type Android.App.FragmentContainer

<pre style='color: green'>
public abstract class FragmentContainer : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected FragmentContainer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FragmentContainer ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.Views.View OnFindViewById (int id);
	public virtual bool OnHasView ();
}
</pre>

### New Type Android.App.FragmentController

<pre style='color: green'>
public class FragmentController : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected FragmentController (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual FragmentManager FragmentManager { get; }
	public virtual LoaderManager LoaderManager { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void AttachHost (Fragment parent);
	public static FragmentController CreateController (FragmentHostCallback callbacks);
	public virtual void DispatchActivityCreated ();
	public virtual void DispatchConfigurationChanged (Android.Content.Res.Configuration newConfig);
	public virtual bool DispatchContextItemSelected (Android.Views.IMenuItem item);
	public virtual void DispatchCreate ();
	public virtual bool DispatchCreateOptionsMenu (Android.Views.IMenu menu, Android.Views.MenuInflater inflater);
	public virtual void DispatchDestroy ();
	public virtual void DispatchDestroyView ();
	public virtual void DispatchLowMemory ();
	public virtual bool DispatchOptionsItemSelected (Android.Views.IMenuItem item);
	public virtual void DispatchOptionsMenuClosed (Android.Views.IMenu menu);
	public virtual void DispatchPause ();
	public virtual bool DispatchPrepareOptionsMenu (Android.Views.IMenu menu);
	public virtual void DispatchResume ();
	public virtual void DispatchStart ();
	public virtual void DispatchStop ();
	public virtual void DispatchTrimMemory (int level);
	public virtual void DoLoaderDestroy ();
	public virtual void DoLoaderStart ();
	public virtual void DoLoaderStop (bool retain);
	public virtual void DumpLoaders (string prefix, Java.IO.FileDescriptor fd, Java.IO.PrintWriter writer, string[] args);
	public virtual bool ExecPendingActions ();
	public virtual Fragment FindFragmentByWho (string who);
	public virtual void NoteStateNotSaved ();
	public virtual Android.Views.View OnCreateView (Android.Views.View parent, string name, Android.Content.Context context, Android.Util.IAttributeSet attrs);
	public virtual void ReportLoaderStart ();
	public virtual void RestoreAllState (Android.OS.IParcelable state, System.Collections.Generic.IList&lt;Fragment&gt; nonConfigList);
	public virtual void RestoreLoaderNonConfig (Android.Util.ArrayMap loaderManagers);
	public virtual Android.Util.ArrayMap RetainLoaderNonConfig ();
	public virtual System.Collections.Generic.IList&lt;Fragment&gt; RetainNonConfig ();
	public virtual Android.OS.IParcelable SaveAllState ();
}
</pre>

### New Type Android.App.FragmentHostCallback

<pre style='color: green'>
public abstract class FragmentHostCallback : Android.App.FragmentContainer, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected FragmentHostCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FragmentHostCallback (Android.Content.Context context, Android.OS.Handler handler, int windowAnimations);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnAttachFragment (Fragment fragment);
	public virtual void OnDump (string prefix, Java.IO.FileDescriptor fd, Java.IO.PrintWriter writer, string[] args);
	public override Android.Views.View OnFindViewById (int id);
	public virtual Java.Lang.Object OnGetHost ();
	public virtual Android.Views.LayoutInflater OnGetLayoutInflater ();
	public virtual int OnGetWindowAnimations ();
	public override bool OnHasView ();
	public virtual bool OnHasWindowAnimations ();
	public virtual void OnInvalidateOptionsMenu ();
	public virtual void OnRequestPermissionsFromFragment (Fragment fragment, string[] permissions, int requestCode);
	public virtual bool OnShouldSaveFragmentState (Fragment fragment);
	public virtual void OnStartActivityFromFragment (Fragment fragment, Android.Content.Intent intent, int requestCode, Android.OS.Bundle options);
	public virtual bool OnUseFragmentManagerInflaterFactory ();
}
</pre>

### New Type Android.App.InterruptionFilter

<pre style='color: green'>
[Serializable]
public enum InterruptionFilter {
	Alarms = 4,
	All = 1,
	None = 3,
	Priority = 2,
	Unknown = 0,
}
</pre>

### New Type Android.App.LockTaskMode

<pre style='color: green'>
[Serializable]
public enum LockTaskMode {
	Locked = 1,
	None = 0,
	Pinned = 2,
}
</pre>

### New Type Android.App.NotificationPriorityCategory

<pre style='color: green'>
[Serializable]
public enum NotificationPriorityCategory {
	Calls = 8,
	Events = 2,
	Messages = 4,
	Reminders = 1,
	RepeatCallers = 16,
}
</pre>

### New Type Android.App.NotificationPrioritySenders

<pre style='color: green'>
[Serializable]
public enum NotificationPrioritySenders {
	Any = 0,
	Contacts = 1,
	Starred = 2,
}
</pre>

### New Type Android.App.VoiceInteractor

<pre style='color: green'>
public sealed class VoiceInteractor : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public VoiceInteractor.Request GetActiveRequest (string name);
	public VoiceInteractor.Request[] GetActiveRequests ();
	public bool SubmitRequest (VoiceInteractor.Request request);
	public bool SubmitRequest (VoiceInteractor.Request request, string name);
	public bool[] SupportsCommands (string[] commands);

	// inner types
	public class AbortVoiceRequest : Android.App.VoiceInteractor+Request, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (VoiceInteractor.Prompt prompt, Android.OS.Bundle extras);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnAbortResult (Android.OS.Bundle result);
	}
	public class CommandRequest : Android.App.VoiceInteractor+Request, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (string command, Android.OS.Bundle args);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnCommandResult (bool isCompleted, Android.OS.Bundle result);
	}
	public class CompleteVoiceRequest : Android.App.VoiceInteractor+Request, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (VoiceInteractor.Prompt prompt, Android.OS.Bundle extras);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnCompleteResult (Android.OS.Bundle result);
	}
	public class ConfirmationRequest : Android.App.VoiceInteractor+Request, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (VoiceInteractor.Prompt prompt, Android.OS.Bundle extras);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnConfirmationResult (bool confirmed, Android.OS.Bundle result);
	}
	public class PickOptionRequest : Android.App.VoiceInteractor+Request, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (VoiceInteractor.Prompt prompt, VoiceInteractor.PickOptionRequest.Option[] options, Android.OS.Bundle extras);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnPickOptionResult (bool finished, VoiceInteractor.PickOptionRequest.Option[] selections, Android.OS.Bundle result);

		// inner types
		public sealed class Option : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
			// constructors
			public VoiceInteractor (Java.Lang.ICharSequence label, int index);
			public VoiceInteractor (string label, int index);
			// properties
			public static Android.OS.IParcelableCreator Creator { get; }
			public Android.OS.Bundle Extras { get; set; }
			public int Index { get; }
			public string Label { get; }
			public Java.Lang.ICharSequence LabelFormatted { get; }
			protected override IntPtr ThresholdClass { get; }
			protected override System.Type ThresholdType { get; }
			// methods
			public VoiceInteractor.PickOptionRequest.Option AddSynonym (Java.Lang.ICharSequence synonym);
			public VoiceInteractor.PickOptionRequest.Option AddSynonym (string synonym);
			public int CountSynonyms ();
			public virtual int DescribeContents ();
			public string GetSynonymAt (int index);
			public Java.Lang.ICharSequence GetSynonymAtFormatted (int index);
			public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

			// inner types
			public static class InterfaceConsts {
				// fields
				public static const int ContentsFileDescriptor;

				[Obsolete]
				public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
			}
		}
	}
	public class Prompt : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (Java.Lang.ICharSequence[] voicePrompts, Java.Lang.ICharSequence visualPrompt);
		public VoiceInteractor (string[] voicePrompts, string visualPrompt);
		public VoiceInteractor (Java.Lang.ICharSequence prompt);
		public VoiceInteractor (string prompt);
		// properties
		public static Android.OS.IParcelableCreator Creator { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public string VisualPrompt { get; }
		public virtual Java.Lang.ICharSequence VisualPromptFormatted { get; }
		// methods
		public virtual int CountVoicePrompts ();
		public virtual int DescribeContents ();
		public string GetVoicePromptAt (int index);
		public virtual Java.Lang.ICharSequence GetVoicePromptAtFormatted (int index);
		public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const int ContentsFileDescriptor;

			[Obsolete]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
		}
	}
	public abstract class Request : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		public virtual Activity Activity { get; }
		public virtual Android.Content.Context Context { get; }
		public virtual string Name { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void Cancel ();
		public virtual void OnAttached (Activity activity);
		public virtual void OnCancel ();
		public virtual void OnDetached ();
	}
}
</pre>

## Namespace Android.App.Admin

### Type Changed: Android.App.Admin.DeviceAdminReceiver

Added methods:

<pre style='color: green'>
	public virtual string OnChoosePrivateKeyAlias (Android.Content.Context context, Android.Content.Intent intent, int uid, Android.Net.Uri uri, string alias);
	public virtual void OnReadyForUserInitialization (Android.Content.Context context, Android.Content.Intent intent);
	public virtual void OnSystemUpdatePending (Android.Content.Context context, Android.Content.Intent intent, long receivedTime);
</pre>

### Type Changed: Android.App.Admin.DevicePolicyManager

Obsoleted fields:

```
[Obsolete ()]
	public static const string ExtraProvisioningDeviceAdminPackageName = "android.app.extra.PROVISIONING_DEVICE_ADMIN_PACKAGE_NAME";
```

Added fields:

<pre style='color: green'>
	public static const string ActionDeviceOwnerChanged = "android.app.action.DEVICE_OWNER_CHANGED";
	public static const string ActionManagedProfileProvisioned = "android.app.action.MANAGED_PROFILE_PROVISIONED";
	public static const string ActionProvisionManagedDevice = "android.app.action.PROVISION_MANAGED_DEVICE";
	public static const string ActionSystemUpdatePolicyChanged = "android.app.action.SYSTEM_UPDATE_POLICY_CHANGED";
	public static const string ExtraProvisioningDeviceAdminComponentName = "android.app.extra.PROVISIONING_DEVICE_ADMIN_COMPONENT_NAME";
	public static const string ExtraProvisioningDeviceAdminMinimumVersionCode = "android.app.extra.PROVISIONING_DEVICE_ADMIN_MINIMUM_VERSION_CODE";
	public static const string ExtraProvisioningDeviceAdminSignatureChecksum = "android.app.extra.PROVISIONING_DEVICE_ADMIN_SIGNATURE_CHECKSUM";
	public static const string ExtraProvisioningSkipEncryption = "android.app.extra.PROVISIONING_SKIP_ENCRYPTION";

	[Obsolete]
	public static const ResetPasswordFlags ResetPasswordDoNotAskCredentialsOnBoot;
</pre>

Added property:

<pre style='color: green'>
	public virtual SystemUpdatePolicy SystemUpdatePolicy { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual Android.OS.UserHandle CreateAndInitializeUser (Android.Content.ComponentName admin, string name, string ownerName, Android.Content.ComponentName profileOwnerComponent, Android.OS.Bundle adminExtras);
	[Obsolete ()]
	public virtual Android.OS.UserHandle CreateUser (Android.Content.ComponentName admin, string name);
```

Modified methods:

```
public virtual bool GetCrossProfileCallerIdDisabled (Android.Content.ComponentName who admin)
	public virtual bool InstallKeyPair (Android.Content.ComponentName who admin, Java.Security.IPrivateKey privKey, Java.Security.Cert.Certificate cert, string alias)
	public virtual bool IsAdminActive (Android.Content.ComponentName who admin)
	public virtual void RemoveActiveAdmin (Android.Content.ComponentName who admin)
	public virtual void SetCrossProfileCallerIdDisabled (Android.Content.ComponentName who admin, bool disabled)
	public virtual void SetProfileName (Android.Content.ComponentName who admin, string profileName)
```

Added methods:

<pre style='color: green'>
	public virtual bool GetBluetoothContactSharingDisabled (Android.Content.ComponentName admin);
	public virtual string GetCertInstallerPackage (Android.Content.ComponentName admin);
	public virtual PermissionGrantState GetPermissionGrantState (Android.Content.ComponentName admin, string packageName, string permission);
	public virtual PermissionPolicy GetPermissionPolicy (Android.Content.ComponentName admin);
	public virtual System.Collections.Generic.IList&lt;Android.OS.PersistableBundle&gt; GetTrustAgentConfiguration (Android.Content.ComponentName admin, Android.Content.ComponentName agent);
	public virtual void SetBluetoothContactSharingDisabled (Android.Content.ComponentName admin, bool disabled);
	public virtual void SetCertInstallerPackage (Android.Content.ComponentName admin, string installerPackage);
	public virtual bool SetKeyguardDisabled (Android.Content.ComponentName admin, bool disabled);
	public virtual bool SetPermissionGrantState (Android.Content.ComponentName admin, string packageName, string permission, PermissionGrantState grantState);
	public virtual void SetPermissionPolicy (Android.Content.ComponentName admin, PermissionPolicy policy);
	public virtual bool SetStatusBarDisabled (Android.Content.ComponentName admin, bool disabled);
	public virtual void SetSystemUpdatePolicy (Android.Content.ComponentName admin, SystemUpdatePolicy policy);
	public virtual void SetTrustAgentConfiguration (Android.Content.ComponentName admin, Android.Content.ComponentName target, Android.OS.PersistableBundle configuration);
	public virtual void SetUserIcon (Android.Content.ComponentName admin, Android.Graphics.Bitmap icon);
</pre>

### Type Changed: Android.App.Admin.EncryptionStatus

Added value:

<pre style='color: green'>
	ActiveDefaultKey = 4,
</pre>

### Type Changed: Android.App.Admin.ResetPasswordFlags

Added value:

<pre style='color: green'>
	DoNotAskCredentialsOnBoot = 2,
</pre>

### New Type Android.App.Admin.PermissionGrantState

<pre style='color: green'>
[Serializable]
public enum PermissionGrantState {
	Default = 0,
	Denied = 2,
	Granted = 1,
}
</pre>

### New Type Android.App.Admin.PermissionPolicy

<pre style='color: green'>
[Serializable]
public enum PermissionPolicy {
	AutoDeny = 2,
	AutoGrant = 1,
	Prompt = 0,
}
</pre>

### New Type Android.App.Admin.SystemUpdatePolicy

<pre style='color: green'>
public class SystemUpdatePolicy : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected SystemUpdatePolicy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual int InstallWindowEnd { get; }
	public virtual int InstallWindowStart { get; }
	public virtual SystemUpdatePolicyType PolicyType { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static SystemUpdatePolicy CreateAutomaticInstallPolicy ();
	public static SystemUpdatePolicy CreatePostponeInstallPolicy ();
	public static SystemUpdatePolicy CreateWindowedInstallPolicy (int startTime, int endTime);
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

### New Type Android.App.Admin.SystemUpdatePolicyType

<pre style='color: green'>
[Serializable]
public enum SystemUpdatePolicyType {
	InstallAutomatic = 1,
	InstallWindowed = 2,
	Postpone = 3,
}
</pre>

## Namespace Android.App.Usage

### Type Changed: Android.App.Usage.UsageEventType

Added value:

<pre style='color: green'>
	UserInteraction = 7,
</pre>

### Type Changed: Android.App.Usage.UsageStatsManager

Added method:

<pre style='color: green'>
	public bool IsAppInactive (string packageName);
</pre>

### New Type Android.App.Usage.NetworkStats

<pre style='color: green'>
public sealed class NetworkStats : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public bool HasNextBucket { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void Close ();
	public bool GetNextBucket (NetworkStats.Bucket bucketOut);

	// inner types
	public class Bucket : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected NetworkStats (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public NetworkStats ();
		// fields
		public static const int UidAll;
		public static const int UidRemoved;
		public static const int UidTethering;
		// properties
		public virtual long EndTimeStamp { get; }
		public virtual long RxBytes { get; }
		public virtual long RxPackets { get; }
		public virtual long StartTimeStamp { get; }
		public virtual NetworkUsageState State { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public virtual long TxBytes { get; }
		public virtual long TxPackets { get; }
		public virtual int Uid { get; }
	}
}
</pre>

### New Type Android.App.Usage.NetworkStatsManager

<pre style='color: green'>
public class NetworkStatsManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected NetworkStatsManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual NetworkStats QueryDetails (Android.Net.ConnectivityType networkType, string subscriberId, long startTime, long endTime);
	public virtual NetworkStats QueryDetailsForUid (Android.Net.ConnectivityType networkType, string subscriberId, long startTime, long endTime, int uid);
	public virtual NetworkStats QuerySummary (Android.Net.ConnectivityType networkType, string subscriberId, long startTime, long endTime);
	public virtual NetworkStats.Bucket QuerySummaryForDevice (Android.Net.ConnectivityType networkType, string subscriberId, long startTime, long endTime);
	public virtual NetworkStats.Bucket QuerySummaryForUser (Android.Net.ConnectivityType networkType, string subscriberId, long startTime, long endTime);
}
</pre>

### New Type Android.App.Usage.NetworkUsageState

<pre style='color: green'>
[Serializable]
public enum NetworkUsageState {
	All = -1,
	Default = 1,
	Foreground = 2,
}
</pre>

## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothA2dp

### Type Changed: Android.Bluetooth.BluetoothA2dp.InterfaceConsts

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const ProfileType Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothDevice

Added method:

<pre style='color: green'>
	public BluetoothGatt ConnectGatt (Android.Content.Context context, bool autoConnect, BluetoothGattCallback callback, BluetoothTransports transport);
</pre>

### Type Changed: Android.Bluetooth.BluetoothGatt

### Type Changed: Android.Bluetooth.BluetoothGatt.InterfaceConsts

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const ProfileType Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothGattServer

### Type Changed: Android.Bluetooth.BluetoothGattServer.InterfaceConsts

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const ProfileType Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothHeadset

### Type Changed: Android.Bluetooth.BluetoothHeadset.InterfaceConsts

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const ProfileType Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothHealth

### Type Changed: Android.Bluetooth.BluetoothHealth.InterfaceConsts

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const ProfileType Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothProfile

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const ProfileType Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothSocket

Added properties:

<pre style='color: green'>
	public BluetoothConnectionType ConnectionType { get; }
	public int MaxReceivePacketSize { get; }
	public int MaxTransmitPacketSize { get; }
</pre>

### Type Changed: Android.Bluetooth.ProfileType

Added value:

<pre style='color: green'>
	Sap = 10,
</pre>

### New Type Android.Bluetooth.BluetoothConnectionType

<pre style='color: green'>
[Serializable]
public enum BluetoothConnectionType {
	L2cap = 3,
	Rfcomm = 1,
	Sco = 2,
}
</pre>

### New Type Android.Bluetooth.BluetoothTransports

<pre style='color: green'>
[Serializable]
public enum BluetoothTransports {
	Auto = 0,
	Bredr = 1,
	Le = 2,
}
</pre>

## Namespace Android.Bluetooth.LE

### Type Changed: Android.Bluetooth.LE.ScanCallbackType

Added values:

<pre style='color: green'>
	FirstMatch = 2,
	MatchLost = 4,
</pre>

### Type Changed: Android.Bluetooth.LE.ScanMode

Added value:

<pre style='color: green'>
	Opportunistic = -1,
</pre>

### Type Changed: Android.Bluetooth.LE.ScanSettings

### Type Changed: Android.Bluetooth.LE.ScanSettings.Builder

Added methods:

<pre style='color: green'>
	public ScanSettings.Builder SetCallbackType (ScanCallbackType callbackType);
	public ScanSettings.Builder SetMatchMode (BluetoothScanMatchMode matchMode);
	public ScanSettings.Builder SetNumOfMatches (int numOfMatches);
</pre>

### New Type Android.Bluetooth.LE.BluetoothScanMatchMode

<pre style='color: green'>
[Serializable]
public enum BluetoothScanMatchMode {
	Aggressive = 1,
	Sticky = 2,
}
</pre>

### New Type Android.Bluetooth.LE.BluetoothScanMatchNumber

<pre style='color: green'>
[Serializable]
public enum BluetoothScanMatchNumber {
	FewAdvertisement = 2,
	MaxAdvertisement = 3,
	OneAdvertisement = 1,
}
</pre>

## Namespace Android.Content

### Type Changed: Android.Content.AbstractThreadedSyncAdapter

Added method:

<pre style='color: green'>
	public virtual void OnSecurityException (Android.Accounts.Account account, Android.OS.Bundle extras, string authority, SyncResult syncResult);
</pre>

### Type Changed: Android.Content.ComponentName

Added methods:

<pre style='color: green'>
	public static ComponentName CreateRelative (Context pkg, string cls);
	public static ComponentName CreateRelative (string pkg, string cls);
</pre>

### Type Changed: Android.Content.ContentProviderOperation

Added properties:

<pre style='color: green'>
	public virtual bool IsAssertQuery { get; }
	public virtual bool IsDelete { get; }
	public virtual bool IsInsert { get; }
	public virtual bool IsUpdate { get; }
</pre>

### Type Changed: Android.Content.Context

Added fields:

<pre style='color: green'>
	public static const string CarrierConfigService = "carrier_config";
	public static const string FingerprintService = "fingerprint";
	public static const string MidiService = "midi";
	public static const string NetworkStatsService = "netstats";
</pre>

Added methods:

<pre style='color: green'>
	public virtual PM.Permission CheckSelfPermission (string permission);
	public int GetColor (int id);
	public Res.ColorStateList GetColorStateList (int id);
	public Java.Lang.Object GetSystemService (Java.Lang.Class serviceClass);
	public virtual string GetSystemServiceName (Java.Lang.Class serviceClass);
</pre>

### Type Changed: Android.Content.ContextWrapper

Added methods:

<pre style='color: green'>
	public override PM.Permission CheckSelfPermission (string permission);
	public override string GetSystemServiceName (Java.Lang.Class serviceClass);
</pre>

### Type Changed: Android.Content.Intent

Added fields:

<pre style='color: green'>
	public static const string ActionProcessText = "android.intent.action.PROCESS_TEXT";
	public static const string CategoryVoice = "android.intent.category.VOICE";
	public static const string ExtraAlternateIntents = "android.intent.extra.ALTERNATE_INTENTS";
	public static const string ExtraAssistInputDeviceId = "android.intent.extra.ASSIST_INPUT_DEVICE_ID";
	public static const string ExtraAssistUid = "android.intent.extra.ASSIST_UID";
	public static const string ExtraChooserRefinementIntentSender = "android.intent.extra.CHOOSER_REFINEMENT_INTENT_SENDER";
	public static const string ExtraProcessText = "android.intent.extra.PROCESS_TEXT";
	public static const string ExtraProcessTextReadonly = "android.intent.extra.PROCESS_TEXT_READONLY";
	public static const string ExtraResultReceiver = "android.intent.extra.RESULT_RECEIVER";
</pre>

### Type Changed: Android.Content.RestrictionEntry

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const RestrictionEntryType TypeBundle;

	[Obsolete]
	public static const RestrictionEntryType TypeBundleArray;
</pre>

Added methods:

<pre style='color: green'>
	public static RestrictionEntry CreateBundleArrayEntry (string key, RestrictionEntry[] restrictionEntries);
	public static RestrictionEntry CreateBundleEntry (string key, RestrictionEntry[] restrictionEntries);
	public virtual RestrictionEntry[] GetRestrictions ();
	public virtual void SetRestrictions (RestrictionEntry[] restrictions);
</pre>

### Type Changed: Android.Content.RestrictionEntryType

Added values:

<pre style='color: green'>
	Bundle = 7,
	BundleArray = 8,
</pre>

### Type Changed: Android.Content.RestrictionsManager

Added method:

<pre style='color: green'>
	public static Android.OS.Bundle ConvertRestrictionsToBundle (System.Collections.Generic.IList&lt;RestrictionEntry&gt; entries);
</pre>

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ApplicationInfoFlags

Added values:

<pre style='color: green'>
	ExtractNativeLibs = 268435456,
	HardwareAccelerated = 536870912,
	UsesCleartextTraffic = 134217728,
</pre>

### Type Changed: Android.Content.PM.PackageInfoFlags

Added value:

<pre style='color: green'>
	MatchAll = 131072,
</pre>

### Type Changed: Android.Content.PM.PackageManager

Added fields:

<pre style='color: green'>
	public static const string FeatureAudioPro = "android.hardware.audio.pro";
	public static const string FeatureAutomotive = "android.hardware.type.automotive";
	public static const string FeatureFingerprint = "android.hardware.fingerprint";
	public static const string FeatureHifiSensors = "android.hardware.sensor.hifi_sensors";
	public static const string FeatureMidi = "android.software.midi";
</pre>

Added method:

<pre style='color: green'>
	public virtual bool IsPermissionRevokedByPolicy (string permName, string pkgName);
</pre>

### Type Changed: Android.Content.PM.PermissionInfo

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const PermissionInfoFlags FlagInstalled;
</pre>

### Type Changed: Android.Content.PM.PermissionInfoFlags

Added value:

<pre style='color: green'>
	Installed = 1073741824,
</pre>

### Type Changed: Android.Content.PM.Protection

Added values:

<pre style='color: green'>
	FlagInstaller = 256,
	FlagPre23 = 128,
	FlagPreinstalled = 1024,
	FlagPrivileged = 16,
	FlagVerifier = 512,
</pre>

## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.ColorStateList

Added property:

<pre style='color: green'>
	public virtual Android.Content.PM.ConfigChanges ChangingConfigurations { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public static ColorStateList CreateFromXml (Resources r, System.Xml.XmlReader parser);
```

Added method:

<pre style='color: green'>
	public static ColorStateList CreateFromXml (Resources r, System.Xml.XmlReader parser, Resources.Theme theme);
</pre>

### Type Changed: Android.Content.Res.Configuration

Added property:

<pre style='color: green'>
	public bool IsScreenRound { get; }
</pre>

### Type Changed: Android.Content.Res.Resources

Obsoleted methods:

```
[Obsolete ()]
	public virtual Android.Graphics.Color GetColor (int id);
	[Obsolete ()]
	public virtual ColorStateList GetColorStateList (int id);
```

Added methods:

<pre style='color: green'>
	public virtual Android.Graphics.Color GetColor (int id, Resources.Theme theme);
	public virtual ColorStateList GetColorStateList (int id, Resources.Theme theme);
</pre>

### Type Changed: Android.Content.Res.Resources.Theme

Added property:

<pre style='color: green'>
	public Android.Content.PM.ConfigChanges ChangingConfigurations { get; }
</pre>

### Type Changed: Android.Content.Res.ScreenLayout

Added values:

<pre style='color: green'>
	RoundMask = 768,
	RoundNo = 256,
	RoundUndefined = 0,
	RoundYes = 512,
</pre>

## Namespace Android.Database

### Type Changed: Android.Database.AbstractCursor

Modified properties:

```
public virtual Android.OS.Bundle Extras { get; set; }
```

### Type Changed: Android.Database.CursorWrapper

Modified properties:

```
public virtual Android.OS.Bundle Extras { get; set; }
```

Obsoleted methods:

```
[Obsolete ()]
	public virtual void Deactivate ();
	[Obsolete ()]
	public virtual bool Requery ();
```

### Type Changed: Android.Database.ICursor

Modified properties:

```
public abstract Android.OS.Bundle Extras { get; set; }
```

## Namespace Android.Graphics

### Type Changed: Android.Graphics.Canvas

Added methods:

<pre style='color: green'>
	public virtual void DrawTextRun (char[] text, int index, int count, int contextIndex, int contextCount, float x, float y, bool isRtl, Paint paint);
	public virtual void DrawTextRun (Java.Lang.ICharSequence text, int start, int end, int contextStart, int contextEnd, float x, float y, bool isRtl, Paint paint);
	public void DrawTextRun (string text, int start, int end, int contextStart, int contextEnd, float x, float y, bool isRtl, Paint paint);
</pre>

### Type Changed: Android.Graphics.ImageFormat

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const ImageFormatType Depth16;

	[Obsolete]
	public static const ImageFormatType DepthPointCloud;

	[Obsolete]
	public static const ImageFormatType FlexRgb888;

	[Obsolete]
	public static const ImageFormatType FlexRgba8888;

	[Obsolete]
	public static const ImageFormatType Private;

	[Obsolete]
	public static const ImageFormatType Raw12;

	[Obsolete]
	public static const ImageFormatType Yuv422888;

	[Obsolete]
	public static const ImageFormatType Yuv444888;
</pre>

### Type Changed: Android.Graphics.ImageFormatType

Added values:

<pre style='color: green'>
	Depth16 = 1144402265,
	DepthPointCloud = 257,
	FlexRgb888 = 41,
	FlexRgba8888 = 42,
	Private = 34,
	Raw12 = 38,
	Yuv422888 = 39,
	Yuv444888 = 40,
</pre>

### Type Changed: Android.Graphics.Paint

Added methods:

<pre style='color: green'>
	public virtual int GetOffsetForAdvance (char[] text, int start, int end, int contextStart, int contextEnd, bool isRtl, float advance);
	public virtual int GetOffsetForAdvance (Java.Lang.ICharSequence text, int start, int end, int contextStart, int contextEnd, bool isRtl, float advance);
	public int GetOffsetForAdvance (string text, int start, int end, int contextStart, int contextEnd, bool isRtl, float advance);
	public float GetRunAdvance (string text, int start, int end, int contextStart, int contextEnd, bool isRtl, int offset);
	public virtual float GetRunAdvance (Java.Lang.ICharSequence text, int start, int end, int contextStart, int contextEnd, bool isRtl, int offset);
	public virtual float GetRunAdvance (char[] text, int start, int end, int contextStart, int contextEnd, bool isRtl, int offset);
	public virtual bool HasGlyph (string string);
</pre>

## Namespace Android.Graphics.Drawables

### Type Changed: Android.Graphics.Drawables.AnimatedVectorDrawable

Added interface:

<pre style='color: green'>
	IAnimatable2
</pre>

Added methods:

<pre style='color: green'>
	public virtual void ClearAnimationCallbacks ();
	public virtual void RegisterAnimationCallback (Animatable2AnimationCallback callback);
	public virtual void Reset ();
	public virtual bool UnregisterAnimationCallback (Animatable2AnimationCallback callback);
</pre>

### Type Changed: Android.Graphics.Drawables.BitmapDrawable

Modified methods:

```
public override void SetColorFilter (Android.Graphics.ColorFilter cf colorFilter)
```

### Type Changed: Android.Graphics.Drawables.ClipDrawable


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Android.Graphics.Drawables.Drawable</span></span>

 <span style='color:green'>Android.Graphics.Drawables.DrawableWrapper</span>

Modified methods:

```
public virtual override void InvalidateDrawable (Drawable who)
	public virtual override void ScheduleDrawable (Drawable who, Java.Lang.IRunnable what, long when)
	public virtual override void UnscheduleDrawable (Drawable who, Java.Lang.IRunnable what)
```

### Type Changed: Android.Graphics.Drawables.Drawable

Added properties:

<pre style='color: green'>
	public virtual bool IsFilterBitmap { get; }
	public virtual Android.Views.LayoutDirection LayoutDirection { get; }
</pre>

Modified methods:

```
public abstract void SetColorFilter (Android.Graphics.ColorFilter cf colorFilter)
	public virtual void SetTint (int tint tintColor)
```

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetDither (bool dither);
```

Added methods:

<pre style='color: green'>
	public virtual void GetHotspotBounds (Android.Graphics.Rect outRect);
	public virtual bool OnLayoutDirectionChanged (int layoutDirection);
	public bool SetLayoutDirection (Android.Views.LayoutDirection layoutDirection);
</pre>

### Type Changed: Android.Graphics.Drawables.DrawableContainer

Modified methods:

```
public override void SetColorFilter (Android.Graphics.ColorFilter cf colorFilter)
```

### Type Changed: Android.Graphics.Drawables.GradientDrawable

Modified methods:

```
public override void SetColorFilter (Android.Graphics.ColorFilter cf colorFilter)
```

### Type Changed: Android.Graphics.Drawables.InsetDrawable


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Android.Graphics.Drawables.Drawable</span></span>

 <span style='color:green'>Android.Graphics.Drawables.DrawableWrapper</span>

Modified properties:

```
public virtual override Drawable Drawable { get; }
```

Modified methods:

```
public virtual override void InvalidateDrawable (Drawable who)
	public virtual override void ScheduleDrawable (Drawable who, Java.Lang.IRunnable what, long when)
	public virtual override void UnscheduleDrawable (Drawable who, Java.Lang.IRunnable what)
```

### Type Changed: Android.Graphics.Drawables.LayerDrawable

Added properties:

<pre style='color: green'>
	public virtual int BottomPadding { get; }
	public virtual int EndPadding { get; }
	public virtual int LeftPadding { get; }
	public virtual int RightPadding { get; }
	public virtual int StartPadding { get; }
	public virtual int TopPadding { get; }
</pre>

Modified methods:

```
public override void SetColorFilter (Android.Graphics.ColorFilter cf colorFilter)
```

Added methods:

<pre style='color: green'>
	public virtual int AddLayer (Drawable dr);
	public virtual int FindIndexByLayerId (int id);
	public virtual Android.Views.GravityFlags GetLayerGravity (int index);
	public virtual int GetLayerHeight (int index);
	public virtual int GetLayerInsetBottom (int index);
	public virtual int GetLayerInsetEnd (int index);
	public virtual int GetLayerInsetLeft (int index);
	public virtual int GetLayerInsetRight (int index);
	public virtual int GetLayerInsetStart (int index);
	public virtual int GetLayerInsetTop (int index);
	public virtual int GetLayerWidth (int index);
	public virtual void SetDrawable (int index, Drawable drawable);
	public virtual void SetLayerGravity (int index, Android.Views.GravityFlags gravity);
	public virtual void SetLayerHeight (int index, int h);
	public virtual void SetLayerInsetBottom (int index, int b);
	public virtual void SetLayerInsetEnd (int index, int e);
	public virtual void SetLayerInsetLeft (int index, int l);
	public virtual void SetLayerInsetRelative (int index, int s, int t, int e, int b);
	public virtual void SetLayerInsetRight (int index, int r);
	public virtual void SetLayerInsetStart (int index, int s);
	public virtual void SetLayerInsetTop (int index, int t);
	public virtual void SetLayerSize (int index, int w, int h);
	public virtual void SetLayerWidth (int index, int w);
	public virtual void SetPadding (int left, int top, int right, int bottom);
	public virtual void SetPaddingRelative (int start, int top, int end, int bottom);
</pre>

### Type Changed: Android.Graphics.Drawables.NinePatchDrawable

Modified methods:

```
public override void SetColorFilter (Android.Graphics.ColorFilter cf colorFilter)
```

### Type Changed: Android.Graphics.Drawables.RippleDrawable

Added field:

<pre style='color: green'>
	public static const int RadiusAuto;
</pre>

Added property:

<pre style='color: green'>
	public virtual int Radius { get; set; }
</pre>

### Type Changed: Android.Graphics.Drawables.RotateDrawable


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Android.Graphics.Drawables.Drawable</span></span>

 <span style='color:green'>Android.Graphics.Drawables.DrawableWrapper</span>

Modified properties:

```
public virtual override Drawable Drawable { get; set; }
```

Modified methods:

```
public virtual override void InvalidateDrawable (Drawable who)
	public virtual override void ScheduleDrawable (Drawable who, Java.Lang.IRunnable what, long when)
	public virtual override void UnscheduleDrawable (Drawable who, Java.Lang.IRunnable what)
```

### Type Changed: Android.Graphics.Drawables.ScaleDrawable


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Android.Graphics.Drawables.Drawable</span></span>

 <span style='color:green'>Android.Graphics.Drawables.DrawableWrapper</span>

Modified properties:

```
public virtual override Drawable Drawable { get; }
```

Modified methods:

```
public virtual override void InvalidateDrawable (Drawable who)
	public virtual override void ScheduleDrawable (Drawable who, Java.Lang.IRunnable what, long when)
	public virtual override void UnscheduleDrawable (Drawable who, Java.Lang.IRunnable what)
```

### Type Changed: Android.Graphics.Drawables.ShapeDrawable

Modified methods:

```
public override void SetColorFilter (Android.Graphics.ColorFilter cf colorFilter)
```

### New Type Android.Graphics.Drawables.Animatable2AnimationCallback

<pre style='color: green'>
public abstract class Animatable2AnimationCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected Animatable2AnimationCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Animatable2AnimationCallback ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnAnimationEnd (Drawable drawable);
	public virtual void OnAnimationStart (Drawable drawable);
}
</pre>

### New Type Android.Graphics.Drawables.DrawableWrapper

<pre style='color: green'>
public abstract class DrawableWrapper : Android.Graphics.Drawables.Drawable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DrawableWrapper (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DrawableWrapper (Drawable dr);
	// properties
	public virtual Drawable Drawable { get; set; }
	public override int Opacity { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Draw (Android.Graphics.Canvas canvas);
	public virtual void InvalidateDrawable (Drawable who);
	public virtual void ScheduleDrawable (Drawable who, Java.Lang.IRunnable what, long when);
	public override void SetAlpha (int alpha);
	public override void SetColorFilter (Android.Graphics.ColorFilter colorFilter);
	public virtual void UnscheduleDrawable (Drawable who, Java.Lang.IRunnable what);
}
</pre>

### New Type Android.Graphics.Drawables.IAnimatable2

<pre style='color: green'>
public interface IAnimatable2 : IAnimatable, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void ClearAnimationCallbacks ();
	public virtual void RegisterAnimationCallback (Animatable2AnimationCallback callback);
	public virtual bool UnregisterAnimationCallback (Animatable2AnimationCallback callback);
}
</pre>

### New Type Android.Graphics.Drawables.Icon

<pre style='color: green'>
public sealed class Icon : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static Icon CreateWithBitmap (Android.Graphics.Bitmap bits);
	public static Icon CreateWithContentUri (Android.Net.Uri uri);
	public static Icon CreateWithContentUri (string uri);
	public static Icon CreateWithData (byte[] data, int offset, int length);
	public static Icon CreateWithFilePath (string path);
	public static Icon CreateWithResource (Android.Content.Context context, int resId);
	public static Icon CreateWithResource (string resPackage, int resId);
	public virtual int DescribeContents ();
	public Drawable LoadDrawable (Android.Content.Context context);
	public void LoadDrawableAsync (Android.Content.Context context, Android.OS.Message andThen);
	public void LoadDrawableAsync (Android.Content.Context context, Icon.IOnDrawableLoadedListener listener, Android.OS.Handler handler);
	public Icon SetTint (int tint);
	public Icon SetTintList (Android.Content.Res.ColorStateList tintList);
	public Icon SetTintMode (Android.Graphics.PorterDuff.Mode mode);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public interface IOnDrawableLoadedListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual void OnDrawableLoaded (Drawable d);
	}
	public class DrawableLoadedEventArgs : System.EventArgs {
		// constructors
		public Icon (Drawable d);
		// properties
		public Drawable D { get; }
	}
}
</pre>

## Namespace Android.Hardware

### Type Changed: Android.Hardware.CameraError

Added value:

<pre style='color: green'>
	Evicted = 2,
</pre>

## Namespace Android.Hardware.Camera2

### Type Changed: Android.Hardware.Camera2.CameraAccessErrorType

Added value:

<pre style='color: green'>
	InUse = 4,
</pre>

### Type Changed: Android.Hardware.Camera2.CameraAccessException

Added field:

<pre style='color: green'>
	public static const int MaxCamerasInUse;
</pre>

### Type Changed: Android.Hardware.Camera2.CameraCaptureSession

Added properties:

<pre style='color: green'>
	public virtual Android.Views.Surface InputSurface { get; }
	public virtual bool IsReprocessable { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void Prepare (Android.Views.Surface surface);
</pre>

### Type Changed: Android.Hardware.Camera2.CameraCaptureSession.StateCallback

Added method:

<pre style='color: green'>
	public virtual void OnSurfacePrepared (CameraCaptureSession session, Android.Views.Surface surface);
</pre>

### Type Changed: Android.Hardware.Camera2.CameraCharacteristics

Added properties:

<pre style='color: green'>
	public static CameraCharacteristics.Key ControlAeLockAvailable { get; }
	public static CameraCharacteristics.Key ControlAvailableModes { get; }
	public static CameraCharacteristics.Key ControlAwbLockAvailable { get; }
	public static CameraCharacteristics.Key DepthDepthIsExclusive { get; }
	public static CameraCharacteristics.Key LensIntrinsicCalibration { get; }
	public static CameraCharacteristics.Key LensPoseRotation { get; }
	public static CameraCharacteristics.Key LensPoseTranslation { get; }
	public static CameraCharacteristics.Key LensRadialDistortion { get; }
	public static CameraCharacteristics.Key ReprocessMaxCaptureStall { get; }
	public static CameraCharacteristics.Key RequestMaxNumInputStreams { get; }
	public static CameraCharacteristics.Key SensorInfoLensShadingApplied { get; }
	public static CameraCharacteristics.Key SensorInfoPreCorrectionActiveArraySize { get; }
	public static CameraCharacteristics.Key ShadingAvailableModes { get; }
	public static CameraCharacteristics.Key StatisticsInfoAvailableLensShadingMapModes { get; }
</pre>

### Type Changed: Android.Hardware.Camera2.CameraDevice

Added methods:

<pre style='color: green'>
	public virtual void CreateConstrainedHighSpeedCaptureSession (System.Collections.Generic.IList&lt;Android.Views.Surface&gt; outputs, CameraCaptureSession.StateCallback callback, Android.OS.Handler handler);
	public virtual void CreateReprocessableCaptureSession (Params.InputConfiguration inputConfig, System.Collections.Generic.IList&lt;Android.Views.Surface&gt; outputs, CameraCaptureSession.StateCallback callback, Android.OS.Handler handler);
	public virtual CaptureRequest.Builder CreateReprocessCaptureRequest (TotalCaptureResult inputResult);
</pre>

### Type Changed: Android.Hardware.Camera2.CameraManager

Added methods:

<pre style='color: green'>
	public void RegisterTorchCallback (CameraManager.TorchCallback callback, Android.OS.Handler handler);
	public void SetTorchMode (string cameraId, bool enabled);
	public void UnregisterTorchCallback (CameraManager.TorchCallback callback);
</pre>

### New Type Android.Hardware.Camera2.TorchCallback

<pre style='color: green'>
public abstract class TorchCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CameraManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CameraManager ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnTorchModeChanged (string cameraId, bool enabled);
	public virtual void OnTorchModeUnavailable (string cameraId);
}
</pre>

### Type Changed: Android.Hardware.Camera2.CaptureRequest

Added properties:

<pre style='color: green'>
	public bool IsReprocess { get; }
	public static CaptureRequest.Key ReprocessEffectiveExposureFactor { get; }
	public static CaptureRequest.Key TonemapGamma { get; }
	public static CaptureRequest.Key TonemapPresetCurve { get; }
</pre>

### Type Changed: Android.Hardware.Camera2.CaptureResult

Added properties:

<pre style='color: green'>
	public static CaptureResult.Key LensIntrinsicCalibration { get; }
	public static CaptureResult.Key LensPoseRotation { get; }
	public static CaptureResult.Key LensPoseTranslation { get; }
	public static CaptureResult.Key LensRadialDistortion { get; }
	public static CaptureResult.Key ReprocessEffectiveExposureFactor { get; }
	public static CaptureResult.Key TonemapGamma { get; }
	public static CaptureResult.Key TonemapPresetCurve { get; }
</pre>

### Type Changed: Android.Hardware.Camera2.ControlAEPrecaptureTrigger

Added value:

<pre style='color: green'>
	Cancel = 2,
</pre>

### Type Changed: Android.Hardware.Camera2.EdgeMode

Added value:

<pre style='color: green'>
	ZeroShutterLag = 3,
</pre>

### Type Changed: Android.Hardware.Camera2.LensFacing

Added value:

<pre style='color: green'>
	External = 2,
</pre>

### Type Changed: Android.Hardware.Camera2.NoiseReductionMode

Added values:

<pre style='color: green'>
	Minimal = 3,
	ZeroShutterLag = 4,
</pre>

### Type Changed: Android.Hardware.Camera2.RequestAvailableCapabilities

Added values:

<pre style='color: green'>
	ConstrainedHighSpeedVideo = 9,
	DepthOutput = 8,
	PrivateReprocessing = 4,
	YuvReprocessing = 7,
</pre>

### Type Changed: Android.Hardware.Camera2.TonemapMode

Added values:

<pre style='color: green'>
	GammaValue = 3,
	PresetCurve = 4,
</pre>

### New Type Android.Hardware.Camera2.CameraConstrainedHighSpeedCaptureSession

<pre style='color: green'>
public abstract class CameraConstrainedHighSpeedCaptureSession : Android.Hardware.Camera2.CameraCaptureSession, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CameraConstrainedHighSpeedCaptureSession (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CameraConstrainedHighSpeedCaptureSession ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual System.Collections.Generic.IList&lt;CaptureRequest&gt; CreateHighSpeedRequestList (CaptureRequest request);
}
</pre>

### New Type Android.Hardware.Camera2.TonemapPresetCurveType

<pre style='color: green'>
[Serializable]
public enum TonemapPresetCurveType {
	Rec709 = 1,
	Srgb = 0,
}
</pre>

## Namespace Android.Hardware.Camera2.Params

### Type Changed: Android.Hardware.Camera2.Params.StreamConfigurationMap

Added methods:

<pre style='color: green'>
	public Android.Util.Size[] GetHighResolutionOutputSizes (int format);
	public int[] GetInputFormats ();
	public Android.Util.Size[] GetInputSizes (int format);
	public int[] GetValidOutputFormatsForInput (int inputFormat);
</pre>

### New Type Android.Hardware.Camera2.Params.InputConfiguration

<pre style='color: green'>
public sealed class InputConfiguration : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public InputConfiguration (int width, int height, int format);
	// properties
	public int Format { get; }
	public int Height { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int Width { get; }
}
</pre>

## Namespace Android.Hardware.Fingerprints

### New Type Android.Hardware.Fingerprints.FingerprintManager

<pre style='color: green'>
public class FingerprintManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected FingerprintManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual bool HasEnrolledFingerprints { get; }
	public virtual bool IsHardwareDetected { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Authenticate (FingerprintManager.CryptoObject crypto, Android.OS.CancellationSignal cancel, FingerprintAuthenticationFlags flags, FingerprintManager.AuthenticationCallback callback, Android.OS.Handler handler);

	// inner types
	public abstract class AuthenticationCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected FingerprintManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public FingerprintManager ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnAuthenticationError (FingerprintState errorCode, Java.Lang.ICharSequence errString);
		public void OnAuthenticationError (FingerprintState errorCode, string errString);
		public virtual void OnAuthenticationFailed ();
		public virtual void OnAuthenticationHelp (FingerprintState helpCode, Java.Lang.ICharSequence helpString);
		public void OnAuthenticationHelp (FingerprintState helpCode, string helpString);
		public virtual void OnAuthenticationSucceeded (FingerprintManager.AuthenticationResult result);
	}
	public class AuthenticationResult : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected FingerprintManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		public virtual FingerprintManager.CryptoObject CryptoObject { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
	public sealed class CryptoObject : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public FingerprintManager (Javax.Crypto.Mac mac);
		public FingerprintManager (Javax.Crypto.Cipher cipher);
		public FingerprintManager (Java.Security.Signature signature);
		// properties
		public Javax.Crypto.Cipher Cipher { get; }
		public Javax.Crypto.Mac Mac { get; }
		public Java.Security.Signature Signature { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
}
</pre>

### New Type Android.Hardware.Fingerprints.FingerprintState

<pre style='color: green'>
[Serializable]
public enum FingerprintState {
	AcquiredGood = 0,
	AcquiredImagerDirty = 3,
	AcquiredInsufficient = 2,
	AcquiredPartial = 1,
	AcquiredTooFast = 5,
	AcquiredTooSlow = 4,
	ErrorCanceled = 5,
	ErrorHwUnavailable = 1,
	ErrorLockout = 7,
	ErrorNoSpace = 4,
	ErrorTimeout = 3,
	ErrorUnableToProcess = 2,
}
</pre>

## Namespace Android.Hardware.Usb

### Type Changed: Android.Hardware.Usb.UsbDevice

Added property:

<pre style='color: green'>
	public virtual string Version { get; }
</pre>

## Namespace Android.Media

### Type Changed: Android.Media.Adjust

Added values:

<pre style='color: green'>
	Mute = -100,
	ToggleMute = 101,
	Unmute = 100,
</pre>

### Type Changed: Android.Media.AsyncPlayer

Obsoleted methods:

```
[Obsolete ()]
	public virtual void Play (Android.Content.Context context, Android.Net.Uri uri, bool looping, Stream stream);
```

Added method:

<pre style='color: green'>
	public virtual void Play (Android.Content.Context context, Android.Net.Uri uri, bool looping, AudioAttributes attributes);
</pre>

### Type Changed: Android.Media.AudioFormat

Added properties:

<pre style='color: green'>
	public virtual int ChannelCount { get; }
	public virtual int ChannelIndexMask { get; }
</pre>

### Type Changed: Android.Media.AudioFormat.Builder

Added method:

<pre style='color: green'>
	public virtual AudioFormat.Builder SetChannelIndexMask (int channelIndexMask);
</pre>

### Type Changed: Android.Media.AudioManager

Added fields:

<pre style='color: green'>
	public static const string PropertySupportMicNearUltrasound = "android.media.property.SUPPORT_MIC_NEAR_ULTRASOUND";
	public static const string PropertySupportSpeakerNearUltrasound = "android.media.property.SUPPORT_SPEAKER_NEAR_ULTRASOUND";
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetStreamMute (Stream streamType, bool state);
	[Obsolete ()]
	public virtual void SetStreamSolo (Stream streamType, bool state);
```

Added methods:

<pre style='color: green'>
	public virtual AudioDeviceInfo[] GetDevices (GetDevicesTargets flags);
	public virtual bool IsStreamMute (Stream streamType);
	public virtual void RegisterAudioDeviceCallback (AudioDeviceCallback callback, Android.OS.Handler handler);
	public virtual void UnregisterAudioDeviceCallback (AudioDeviceCallback callback);
</pre>

### Type Changed: Android.Media.AudioRecord

Added properties:

<pre style='color: green'>
	public virtual int BufferSizeInFrames { get; }
	public virtual AudioFormat Format { get; }
	public virtual AudioDeviceInfo PreferredDevice { get; }
	public virtual AudioDeviceInfo RoutedDevice { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddOnRoutingChangedListener (AudioRecord.IOnRoutingChangedListener listener, Android.OS.Handler handler);
	public virtual int Read (short[] audioData, int offsetInShorts, int sizeInShorts, int readMode);
	public virtual int Read (Java.Nio.ByteBuffer audioBuffer, int sizeInBytes, int readMode);
	public virtual int Read (float[] audioData, int offsetInFloats, int sizeInFloats, int readMode);
	public virtual int Read (byte[] audioData, int offsetInBytes, int sizeInBytes, int readMode);
	public System.Threading.Tasks.Task&lt;int&gt; ReadAsync (short[] audioData, int offsetInShorts, int sizeInShorts, int readMode);
	public System.Threading.Tasks.Task&lt;int&gt; ReadAsync (float[] audioData, int offsetInFloats, int sizeInFloats, int readMode);
	public System.Threading.Tasks.Task&lt;int&gt; ReadAsync (byte[] audioData, int offsetInBytes, int sizeInBytes, int readMode);
	public System.Threading.Tasks.Task&lt;int&gt; ReadAsync (Java.Nio.ByteBuffer audioBuffer, int sizeInBytes, int readMode);
	public virtual void RemoveOnRoutingChangedListener (AudioRecord.IOnRoutingChangedListener listener);
	public virtual bool SetPreferredDevice (AudioDeviceInfo deviceInfo);
</pre>

### New Type Android.Media.Builder

<pre style='color: green'>
public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected AudioRecord (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AudioRecord ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual AudioRecord Build ();
	public virtual AudioRecord.Builder SetAudioFormat (AudioFormat format);
	public virtual AudioRecord.Builder SetAudioSource (AudioSource source);
	public virtual AudioRecord.Builder SetBufferSizeInBytes (int bufferSizeInBytes);
}
</pre>

### New Type Android.Media.IOnRoutingChangedListener

<pre style='color: green'>
public interface IOnRoutingChangedListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnRoutingChanged (AudioRecord audioRecord);
}
</pre>

### New Type Android.Media.RoutingChangedEventArgs

<pre style='color: green'>
public class RoutingChangedEventArgs : System.EventArgs {
	// constructors
	public AudioRecord (AudioRecord audioRecord);
	// properties
	public AudioRecord AudioRecord { get; }
}
</pre>

### Type Changed: Android.Media.AudioTrack

Added properties:

<pre style='color: green'>
	public virtual int BufferSizeInFrames { get; }
	public virtual AudioFormat Format { get; }
	public virtual PlaybackParams PlaybackParams { get; set; }
	public virtual AudioDeviceInfo PreferredDevice { get; }
	public virtual AudioDeviceInfo RoutedDevice { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddOnRoutingChangedListener (AudioTrack.IOnRoutingChangedListener listener, Android.OS.Handler handler);
	public virtual void RemoveOnRoutingChangedListener (AudioTrack.IOnRoutingChangedListener listener);
	public virtual bool SetPreferredDevice (AudioDeviceInfo deviceInfo);
	public virtual int Write (byte[] audioData, int offsetInBytes, int sizeInBytes, WriteMode writeMode);
	public virtual int Write (short[] audioData, int offsetInShorts, int sizeInShorts, WriteMode writeMode);
	public virtual int Write (Java.Nio.ByteBuffer audioData, int sizeInBytes, WriteMode writeMode, long timestamp);
	public System.Threading.Tasks.Task&lt;int&gt; WriteAsync (Java.Nio.ByteBuffer audioData, int sizeInBytes, WriteMode writeMode, long timestamp);
	public System.Threading.Tasks.Task&lt;int&gt; WriteAsync (byte[] audioData, int offsetInBytes, int sizeInBytes, WriteMode writeMode);
	public System.Threading.Tasks.Task&lt;int&gt; WriteAsync (short[] audioData, int offsetInShorts, int sizeInShorts, WriteMode writeMode);
</pre>

### New Type Android.Media.Builder

<pre style='color: green'>
public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected AudioTrack (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AudioTrack ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual AudioTrack Build ();
	public virtual AudioTrack.Builder SetAudioAttributes (AudioAttributes attributes);
	public virtual AudioTrack.Builder SetAudioFormat (AudioFormat format);
	public virtual AudioTrack.Builder SetBufferSizeInBytes (int bufferSizeInBytes);
	public virtual AudioTrack.Builder SetSessionId (int sessionId);
	public virtual AudioTrack.Builder SetTransferMode (AudioTrackMode mode);
}
</pre>

### New Type Android.Media.IOnRoutingChangedListener

<pre style='color: green'>
public interface IOnRoutingChangedListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnRoutingChanged (AudioTrack audioTrack);
}
</pre>

### New Type Android.Media.RoutingChangedEventArgs

<pre style='color: green'>
public class RoutingChangedEventArgs : System.EventArgs {
	// constructors
	public AudioTrack (AudioTrack audioTrack);
	// properties
	public AudioTrack AudioTrack { get; }
}
</pre>

### Type Changed: Android.Media.ChannelOut

Added value:

<pre style='color: green'>
	C7point1Surround = 6396,
</pre>

### Type Changed: Android.Media.Encoding

Added values:

<pre style='color: green'>
	Dts = 7,
	DtsHd = 8,
</pre>

### Type Changed: Android.Media.ExifInterface

Added fields:

<pre style='color: green'>
	public static const string TagDatetimeDigitized = "DateTimeDigitized";
	public static const string TagSubsecTime = "SubSecTime";
	public static const string TagSubsecTimeDig = "SubSecTimeDigitized";
	public static const string TagSubsecTimeOrig = "SubSecTimeOriginal";
</pre>

### Type Changed: Android.Media.MediaCodec

Added methods:

<pre style='color: green'>
	public static Android.Views.Surface CreatePersistentInputSurface ();
	public void SetCallback (MediaCodec.Callback cb, Android.OS.Handler handler);
	public void SetInputSurface (Android.Views.Surface surface);
	public void SetOnFrameRenderedListener (MediaCodec.IOnFrameRenderedListener listener, Android.OS.Handler handler);
	public void SetOutputSurface (Android.Views.Surface surface);
</pre>

### Type Changed: Android.Media.MediaCodec.CodecException

Added property:

<pre style='color: green'>
	public MediaCodecErrorCode ErrorCode { get; }
</pre>

### Type Changed: Android.Media.MediaCodec.CryptoException

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const MediaCodecCryptoErrorType ErrorSessionNotOpened;
</pre>

### New Type Android.Media.IOnFrameRenderedListener

<pre style='color: green'>
public interface IOnFrameRenderedListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnFrameRendered (MediaCodec codec, long presentationTimeUs, long nanoTime);
}
</pre>

### New Type Android.Media.FrameRenderedEventArgs

<pre style='color: green'>
public class FrameRenderedEventArgs : System.EventArgs {
	// constructors
	public MediaCodec (MediaCodec codec, long presentationTimeUs, long nanoTime);
	// properties
	public MediaCodec Codec { get; }
	public long NanoTime { get; }
	public long PresentationTimeUs { get; }
}
</pre>

### Type Changed: Android.Media.MediaCodecCapabilities

Added values:

<pre style='color: green'>
	Format32bitabgr8888 = 2130747392,
	Formatrgbaflexible = 2134288520,
	Formatrgbflexible = 2134292616,
	Formatyuv422flexible = 2135042184,
	Formatyuv444flexible = 2135181448,
</pre>

### Type Changed: Android.Media.MediaCodecCryptoErrorType

Added value:

<pre style='color: green'>
	SessionNotOpened = 5,
</pre>

### Type Changed: Android.Media.MediaCodecInfo

### Type Changed: Android.Media.MediaCodecInfo.CodecCapabilities

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const MediaCodecCapabilities COLORFormat32bitABGR8888;

	[Obsolete]
	public static const MediaCodecCapabilities COLORFormatRGBAFlexible;

	[Obsolete]
	public static const MediaCodecCapabilities COLORFormatRGBFlexible;

	[Obsolete]
	public static const MediaCodecCapabilities COLORFormatYUV422Flexible;

	[Obsolete]
	public static const MediaCodecCapabilities COLORFormatYUV444Flexible;
</pre>

Added property:

<pre style='color: green'>
	public int MaxSupportedInstances { get; }
</pre>

### Type Changed: Android.Media.MediaCodecInfo.CodecProfileLevel

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const MediaCodecProfileLevel MPEG2LevelH14;

	[Obsolete]
	public static const MediaCodecProfileLevel MPEG2LevelHL;

	[Obsolete]
	public static const MediaCodecProfileLevel MPEG2LevelLL;

	[Obsolete]
	public static const MediaCodecProfileLevel MPEG2LevelML;

	[Obsolete]
	public static const MediaCodecProfileType MPEG2Profile422;

	[Obsolete]
	public static const MediaCodecProfileType MPEG2ProfileHigh;

	[Obsolete]
	public static const MediaCodecProfileType MPEG2ProfileMain;

	[Obsolete]
	public static const MediaCodecProfileType MPEG2ProfileSimple;

	[Obsolete]
	public static const MediaCodecProfileType MPEG2ProfileSNR;

	[Obsolete]
	public static const MediaCodecProfileType MPEG2ProfileSpatial;
</pre>

### Type Changed: Android.Media.MediaCodecInfo.VideoCapabilities

Added method:

<pre style='color: green'>
	public Android.Util.Range GetAchievableFrameRatesFor (int width, int height);
</pre>

### Type Changed: Android.Media.MediaCodecProfileLevel

Added values:

<pre style='color: green'>
	Mpeg2levelh14 = 2,
	Mpeg2levelhl = 3,
	Mpeg2levelll = 0,
	Mpeg2levelml = 1,
</pre>

### Type Changed: Android.Media.MediaCodecProfileType

Added values:

<pre style='color: green'>
	Mpeg2profile422 = 2,
	Mpeg2profilehigh = 5,
	Mpeg2profilemain = 1,
	Mpeg2profilesimple = 0,
	Mpeg2profilesnr = 3,
	Mpeg2profilespatial = 4,
</pre>

### Type Changed: Android.Media.MediaCrypto

Added method:

<pre style='color: green'>
	public void SetMediaDrmSession (byte[] sessionId);
</pre>

### Type Changed: Android.Media.MediaDescription

Added property:

<pre style='color: green'>
	public virtual Android.Net.Uri MediaUri { get; }
</pre>

### Type Changed: Android.Media.MediaDescription.Builder

Added method:

<pre style='color: green'>
	public virtual MediaDescription.Builder SetMediaUri (Android.Net.Uri mediaUri);
</pre>

### Type Changed: Android.Media.MediaDrm

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const MediaDrmEventType EventSessionReclaimed;
</pre>

Added methods:

<pre style='color: green'>
	public void SetOnExpirationUpdateListener (MediaDrm.IOnExpirationUpdateListener listener, Android.OS.Handler handler);
	public void SetOnKeyStatusChangeListener (MediaDrm.IOnKeyStatusChangeListener listener, Android.OS.Handler handler);
</pre>

### Type Changed: Android.Media.MediaDrm.KeyRequest

Added fields:

<pre style='color: green'>
	public static const int RequestTypeInitial;
	public static const int RequestTypeRelease;
	public static const int RequestTypeRenewal;
</pre>

Added property:

<pre style='color: green'>
	public int RequestType { get; }
</pre>

### New Type Android.Media.KeyStatus

<pre style='color: green'>
public sealed class KeyStatus : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public MediaDrmStatusCode StatusCode { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public byte[] GetKeyId ();
}
</pre>

### New Type Android.Media.IOnExpirationUpdateListener

<pre style='color: green'>
public interface IOnExpirationUpdateListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnExpirationUpdate (MediaDrm md, byte[] sessionId, long expirationTime);
}
</pre>

### New Type Android.Media.ExpirationUpdateEventArgs

<pre style='color: green'>
public class ExpirationUpdateEventArgs : System.EventArgs {
	// constructors
	public MediaDrm (MediaDrm md, byte[] sessionId, long expirationTime);
	// properties
	public long ExpirationTime { get; }
	public MediaDrm Md { get; }
	public byte[] SessionId { get; }
}
</pre>

### New Type Android.Media.IOnKeyStatusChangeListener

<pre style='color: green'>
public interface IOnKeyStatusChangeListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnKeyStatusChange (MediaDrm md, byte[] sessionId, System.Collections.Generic.IList&lt;MediaDrm.KeyStatus&gt; keyInformation, bool hasNewUsableKey);
}
</pre>

### New Type Android.Media.KeyStatusChangeEventArgs

<pre style='color: green'>
public class KeyStatusChangeEventArgs : System.EventArgs {
	// constructors
	public MediaDrm (MediaDrm md, byte[] sessionId, System.Collections.Generic.IList&lt;MediaDrm.KeyStatus&gt; keyInformation, bool hasNewUsableKey);
	// properties
	public bool HasNewUsableKey { get; }
	public System.Collections.Generic.IList&lt;MediaDrm.KeyStatus&gt; KeyInformation { get; }
	public MediaDrm Md { get; }
	public byte[] SessionId { get; }
}
</pre>

### Type Changed: Android.Media.MediaDrmEventType

Added value:

<pre style='color: green'>
	SessionReclaimed = 5,
</pre>

### Type Changed: Android.Media.MediaExtractor

Added methods:

<pre style='color: green'>
	public void SetDataSource (MediaDataSource dataSource);
	public System.Threading.Tasks.Task SetDataSourceAsync (MediaDataSource dataSource);
</pre>

### Type Changed: Android.Media.MediaFormat

Added fields:

<pre style='color: green'>
	public static const string KeyLevel = "level";
	public static const string KeyOperatingRate = "operating-rate";
	public static const string KeyPriority = "priority";
	public static const string KeyRotation = "rotation-degrees";
	public static const string KeySliceHeight = "slice-height";
	public static const string KeyStride = "stride";
	public static const string MimetypeAudioEac3 = "audio/eac3";
</pre>

### Type Changed: Android.Media.MediaMetadataRetriever

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const MetadataKey MetadataKeyCaptureFramerate;
</pre>

Added methods:

<pre style='color: green'>
	public virtual void SetDataSource (MediaDataSource dataSource);
	public System.Threading.Tasks.Task SetDataSourceAsync (MediaDataSource dataSource);
</pre>

### Type Changed: Android.Media.MediaPlayer

Added properties:

<pre style='color: green'>
	public virtual PlaybackParams PlaybackParams { get; set; }
	public virtual SyncParams SyncParams { get; set; }
	public virtual MediaTimestamp Timestamp { get; }
</pre>

Added event:

<pre style='color: green'>
	public event System.EventHandler&lt;MediaPlayer.TimedMetaDataAvailableEventArgs&gt; TimedMetaDataAvailable;
</pre>

Added methods:

<pre style='color: green'>
	public virtual void SetDataSource (MediaDataSource dataSource);
	public System.Threading.Tasks.Task SetDataSourceAsync (MediaDataSource dataSource);
	public virtual void SetOnTimedMetaDataAvailableListener (MediaPlayer.IOnTimedMetaDataAvailableListener listener);
</pre>

### Type Changed: Android.Media.MediaPlayer.TrackInfo

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const MediaTrackType MediaTrackTypeMetadata;
</pre>

### New Type Android.Media.IOnTimedMetaDataAvailableListener

<pre style='color: green'>
public interface IOnTimedMetaDataAvailableListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnTimedMetaDataAvailable (MediaPlayer mp, TimedMetaData data);
}
</pre>

### New Type Android.Media.TimedMetaDataAvailableEventArgs

<pre style='color: green'>
public class TimedMetaDataAvailableEventArgs : System.EventArgs {
	// constructors
	public MediaPlayer (MediaPlayer mp, TimedMetaData data);
	// properties
	public TimedMetaData Data { get; }
	public MediaPlayer Mp { get; }
}
</pre>

### Type Changed: Android.Media.MediaRecorder

Added method:

<pre style='color: green'>
	public virtual void SetInputSurface (Android.Views.Surface surface);
</pre>

### Type Changed: Android.Media.MediaTrackType

Added value:

<pre style='color: green'>
	Metadata = 5,
</pre>

### Type Changed: Android.Media.MetadataKey

Added value:

<pre style='color: green'>
	CaptureFramerate = 25,
</pre>

### New Type Android.Media.AudioAdjustMode

<pre style='color: green'>
[Serializable]
public enum AudioAdjustMode {
	Default = 0,
	Resample = 2,
	Stretch = 1,
}
</pre>

### New Type Android.Media.AudioDeviceCallback

<pre style='color: green'>
public abstract class AudioDeviceCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected AudioDeviceCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AudioDeviceCallback ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnAudioDevicesAdded (AudioDeviceInfo[] addedDevices);
	public virtual void OnAudioDevicesRemoved (AudioDeviceInfo[] removedDevices);
}
</pre>

### New Type Android.Media.AudioDeviceInfo

<pre style='color: green'>
public sealed class AudioDeviceInfo : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public int Id { get; }
	public bool IsSink { get; }
	public bool IsSource { get; }
	public string ProductName { get; }
	public Java.Lang.ICharSequence ProductNameFormatted { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public AudioDeviceType Type { get; }
	// methods
	public int[] GetChannelCounts ();
	public int[] GetChannelIndexMasks ();
	public int[] GetChannelMasks ();
	public Encoding[] GetEncodings ();
	public int[] GetSampleRates ();
}
</pre>

### New Type Android.Media.AudioDeviceType

<pre style='color: green'>
[Serializable]
public enum AudioDeviceType {
	AuxLine = 19,
	BluetoothA2dp = 8,
	BluetoothSco = 7,
	BuiltinEarpiece = 1,
	BuiltinMic = 15,
	BuiltinSpeaker = 2,
	Dock = 13,
	Fm = 14,
	FmTuner = 16,
	Hdmi = 9,
	HdmiArc = 10,
	Ip = 20,
	LineAnalog = 5,
	LineDigital = 6,
	Telephony = 18,
	TvTuner = 17,
	Unknown = 0,
	UsbAccessory = 12,
	UsbDevice = 11,
	WiredHeadphones = 4,
	WiredHeadset = 3,
}
</pre>

### New Type Android.Media.AudioFallbackMode

<pre style='color: green'>
[Serializable]
public enum AudioFallbackMode {
	Default = 0,
	Fail = 2,
	Mute = 1,
}
</pre>

### New Type Android.Media.AudioRecordReadOptions

<pre style='color: green'>
[Serializable]
public enum AudioRecordReadOptions {
	Blocking = 0,
	NonBlocking = 1,
}
</pre>

### New Type Android.Media.AudioSyncSource

<pre style='color: green'>
[Serializable]
public enum AudioSyncSource {
	Audio = 2,
	Default = 0,
	SystemClock = 1,
	Vsync = 3,
}
</pre>

### New Type Android.Media.GetDevicesTargets

<pre style='color: green'>
[Serializable]
public enum GetDevicesTargets {
	All = 3,
	Inputs = 1,
	Outputs = 2,
}
</pre>

### New Type Android.Media.ImageWriter

<pre style='color: green'>
public class ImageWriter : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ImageWriter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual Android.Graphics.ImageFormatType Format { get; }
	public virtual int MaxImages { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Close ();
	public virtual Image DequeueInputImage ();
	public static ImageWriter NewInstance (Android.Views.Surface surface, int maxImages);
	public virtual void QueueInputImage (Image image);
	public virtual void SetOnImageReleasedListener (ImageWriter.IOnImageReleasedListener listener, Android.OS.Handler handler);

	// inner types
	public interface IOnImageReleasedListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual void OnImageReleased (ImageWriter writer);
	}
	public class ImageReleasedEventArgs : System.EventArgs {
		// constructors
		public ImageWriter (ImageWriter writer);
		// properties
		public ImageWriter Writer { get; }
	}
}
</pre>

### New Type Android.Media.MediaCodecErrorCode

<pre style='color: green'>
[Serializable]
public enum MediaCodecErrorCode {
	InsufficientResource = 1100,
	Reclaimed = 1101,
}
</pre>

### New Type Android.Media.MediaDataSource

<pre style='color: green'>
public abstract class MediaDataSource : Java.Lang.Object, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected MediaDataSource (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MediaDataSource ();
	// properties
	public virtual long Size { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Close ();
	public virtual int ReadAt (long position, byte[] buffer, int offset, int size);
}
</pre>

### New Type Android.Media.MediaDrmResetException

<pre style='color: green'>
public class MediaDrmResetException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected MediaDrmResetException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MediaDrmResetException (string detailMessage);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Media.MediaDrmStatusCode

<pre style='color: green'>
[Serializable]
public enum MediaDrmStatusCode {
	Expired = 1,
	InternalError = 4,
	OutputNotAllowed = 2,
	Pending = 3,
	Usable = 0,
}
</pre>

### New Type Android.Media.MediaSync

<pre style='color: green'>
public sealed class MediaSync : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MediaSync ();
	// properties
	public PlaybackParams PlaybackParams { get; set; }
	public SyncParams SyncParams { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public MediaTimestamp Timestamp { get; }
	// methods
	public Android.Views.Surface CreateInputSurface ();
	public void Flush ();
	public void QueueAudio (Java.Nio.ByteBuffer audioData, int bufferId, long presentationTimeUs);
	public void Release ();
	public void SetAudioTrack (AudioTrack audioTrack);
	public void SetCallback (MediaSync.Callback cb, Android.OS.Handler handler);
	public void SetOnErrorListener (MediaSync.IOnErrorListener listener, Android.OS.Handler handler);
	public void SetSurface (Android.Views.Surface surface);

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MediaSync (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MediaSync ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnAudioBufferConsumed (MediaSync sync, Java.Nio.ByteBuffer audioBuffer, int bufferId);
	}
	public interface IOnErrorListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual void OnError (MediaSync sync, MediaSyncErrorCode what, int extra);
	}
	public class ErrorEventArgs : System.EventArgs {
		// constructors
		public MediaSync (MediaSync sync, MediaSyncErrorCode what, int extra);
		// properties
		public int Extra { get; }
		public MediaSync Sync { get; }
		public MediaSyncErrorCode What { get; }
	}
}
</pre>

### New Type Android.Media.MediaSyncErrorCode

<pre style='color: green'>
[Serializable]
public enum MediaSyncErrorCode {
	AudiotrackFail = 1,
	SurfaceFail = 2,
}
</pre>

### New Type Android.Media.MediaTimestamp

<pre style='color: green'>
public sealed class MediaTimestamp : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public long AnchorMediaTimeUs { get; }
	public long AnchorSytemNanoTime { get; }
	public float MediaClockRate { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Media.PlaybackParams

<pre style='color: green'>
public sealed class PlaybackParams : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public PlaybackParams ();
	// properties
	public AudioFallbackMode AudioFallbackMode { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public float Pitch { get; }
	public float Speed { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public PlaybackParams AllowDefaults ();
	public virtual int DescribeContents ();
	public PlaybackParams SetAudioFallbackMode (int audioFallbackMode);
	public PlaybackParams SetPitch (float pitch);
	public PlaybackParams SetSpeed (float speed);
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

### New Type Android.Media.SyncParams

<pre style='color: green'>
public sealed class SyncParams : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public SyncParams ();
	// properties
	public AudioAdjustMode AudioAdjustMode { get; }
	public float FrameRate { get; }
	public AudioSyncSource SyncSource { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public float Tolerance { get; }
	// methods
	public SyncParams AllowDefaults ();
	public SyncParams SetAudioAdjustMode (int audioAdjustMode);
	public SyncParams SetFrameRate (float frameRate);
	public SyncParams SetSyncSource (int syncSource);
	public SyncParams SetTolerance (float tolerance);
}
</pre>

### New Type Android.Media.TimedMetaData

<pre style='color: green'>
public sealed class TimedMetaData : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public long Timestamp { get; }
	// methods
	public byte[] GetMetaData ();
}
</pre>

## Namespace Android.Media.Browse

### Type Changed: Android.Media.Browse.MediaBrowser

Added method:

<pre style='color: green'>
	public void GetItem (string mediaId, MediaBrowser.ItemCallback cb);
</pre>

### Type Changed: Android.Media.Browse.MediaBrowser.SubscriptionCallback

Modified methods:

```
public virtual void OnError (string id parentId)
```

### New Type Android.Media.Browse.ItemCallback

<pre style='color: green'>
public abstract class ItemCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected MediaBrowser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MediaBrowser ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnError (string itemId);
	public virtual void OnItemLoaded (MediaBrowser.MediaItem item);
}
</pre>

## Namespace Android.Media.Session

### Type Changed: Android.Media.Session.MediaController

### Type Changed: Android.Media.Session.MediaController.TransportControls

Added method:

<pre style='color: green'>
	public void PlayFromUri (Android.Net.Uri uri, Android.OS.Bundle extras);
</pre>

### Type Changed: Android.Media.Session.MediaSession

### Type Changed: Android.Media.Session.MediaSession.Callback

Added method:

<pre style='color: green'>
	public virtual void OnPlayFromUri (Android.Net.Uri uri, Android.OS.Bundle extras);
</pre>

### Type Changed: Android.Media.Session.PlaybackState

Added field:

<pre style='color: green'>
	public static const long ActionPlayFromUri;
</pre>

## Namespace Android.Media.TV

### Type Changed: Android.Media.TV.TvContentRating

Added property:

<pre style='color: green'>
	public static TvContentRating Unrated { get; }
</pre>

### Type Changed: Android.Media.TV.TvContract

### Type Changed: Android.Media.TV.TvContract.Channels

Added fields:

<pre style='color: green'>
	public static const string ColumnAppLinkColor = "app_link_color";
	public static const string ColumnAppLinkIconUri = "app_link_icon_uri";
	public static const string ColumnAppLinkIntentUri = "app_link_intent_uri";
	public static const string ColumnAppLinkPosterArtUri = "app_link_poster_art_uri";
	public static const string ColumnAppLinkText = "app_link_text";
	public static const string ColumnInternalProviderFlag1 = "internal_provider_flag1";
	public static const string ColumnInternalProviderFlag2 = "internal_provider_flag2";
	public static const string ColumnInternalProviderFlag3 = "internal_provider_flag3";
	public static const string ColumnInternalProviderFlag4 = "internal_provider_flag4";
</pre>

### Type Changed: Android.Media.TV.TvContract.Programs

Added fields:

<pre style='color: green'>
	public static const string ColumnInternalProviderFlag1 = "internal_provider_flag1";
	public static const string ColumnInternalProviderFlag2 = "internal_provider_flag2";
	public static const string ColumnInternalProviderFlag3 = "internal_provider_flag3";
	public static const string ColumnInternalProviderFlag4 = "internal_provider_flag4";
	public static const string ColumnSearchable = "searchable";
</pre>

### Type Changed: Android.Media.TV.TvInputManager

Added field:

<pre style='color: green'>
	public static const long TimeShiftInvalidTime;
</pre>

### Type Changed: Android.Media.TV.TvInputService

### Type Changed: Android.Media.TV.TvInputService.Session

Added methods:

<pre style='color: green'>
	public virtual void LayoutSurface (int left, int top, int right, int bottom);
	public virtual void NotifyTimeShiftStatusChanged (TimeShiftStatus status);
	public virtual void OnOverlayViewSizeChanged (int width, int height);
	public virtual long OnTimeShiftGetCurrentPosition ();
	public virtual long OnTimeShiftGetStartPosition ();
	public virtual void OnTimeShiftPause ();
	public virtual void OnTimeShiftResume ();
	public virtual void OnTimeShiftSeekTo (long timeMs);
	public virtual void OnTimeShiftSetPlaybackParams (Android.Media.PlaybackParams params);
</pre>

### Type Changed: Android.Media.TV.TvTrackInfo

Added properties:

<pre style='color: green'>
	public string Description { get; }
	public Java.Lang.ICharSequence DescriptionFormatted { get; }
	public float VideoPixelAspectRatio { get; }
</pre>

### Type Changed: Android.Media.TV.TvTrackInfo.Builder

Added methods:

<pre style='color: green'>
	public TvTrackInfo.Builder SetDescription (Java.Lang.ICharSequence description);
	public TvTrackInfo.Builder SetDescription (string description);
	public TvTrackInfo.Builder SetVideoPixelAspectRatio (float videoPixelAspectRatio);
</pre>

### Type Changed: Android.Media.TV.TvView

Added methods:

<pre style='color: green'>
	public virtual void SetTimeShiftPositionCallback (TvView.TimeShiftPositionCallback callback);
	public virtual void TimeShiftPause ();
	public virtual void TimeShiftResume ();
	public virtual void TimeShiftSeekTo (long timeMs);
	public virtual void TimeShiftSetPlaybackParams (Android.Media.PlaybackParams params);
</pre>

### Type Changed: Android.Media.TV.TvView.TvInputCallback

Added method:

<pre style='color: green'>
	public virtual void OnTimeShiftStatusChanged (string inputId, TimeShiftStatus status);
</pre>

### New Type Android.Media.TV.TimeShiftPositionCallback

<pre style='color: green'>
public abstract class TimeShiftPositionCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected TvView (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TvView ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnTimeShiftCurrentPositionChanged (string inputId, long timeMs);
	public virtual void OnTimeShiftStartPositionChanged (string inputId, long timeMs);
}
</pre>

### Type Changed: Android.Media.TV.VideoUnavailableReason

Added value:

<pre style='color: green'>
	AudioOnly = 4,
</pre>

### New Type Android.Media.TV.TimeShiftStatus

<pre style='color: green'>
[Serializable]
public enum TimeShiftStatus {
	Available = 3,
	Unavailable = 2,
	Unknown = 0,
	Unsupported = 1,
}
</pre>

## Namespace Android.Net

### Type Changed: Android.Net.ConnectivityManager

Added fields:

<pre style='color: green'>
	public static const string ActionCaptivePortalSignIn = "android.net.conn.CAPTIVE_PORTAL";
	public static const string ExtraCaptivePortal = "android.net.extra.CAPTIVE_PORTAL";
</pre>

Obsoleted properties:

```
[Obsolete ()]
	public static Network ProcessDefaultNetwork { get; }
```

Added properties:

<pre style='color: green'>
	public virtual Network ActiveNetwork { get; }
	public virtual Network BoundNetworkForProcess { get; }
	public virtual ProxyInfo DefaultProxy { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual NetworkInfo[] GetAllNetworkInfo ();
	[Obsolete ()]
	public virtual NetworkInfo GetNetworkInfo (ConnectivityType networkType);
	[Obsolete ()]
	public static bool IsNetworkTypeValid (ConnectivityType networkType);
	[Obsolete ()]
	public virtual void ReportBadNetwork (Network network);
	[Obsolete ()]
	public static bool SetProcessDefaultNetwork (Network network);
```

Added methods:

<pre style='color: green'>
	public virtual bool BindProcessToNetwork (Network network);
	public virtual void RegisterNetworkCallback (NetworkRequest request, Android.App.PendingIntent operation);
	public virtual void ReportNetworkConnectivity (Network network, bool hasConnectivity);
	public virtual bool RequestBandwidthUpdate (Network network);
	public virtual void UnregisterNetworkCallback (Android.App.PendingIntent operation);
</pre>

### Type Changed: Android.Net.IpPrefix

Added method:

<pre style='color: green'>
	public bool Contains (Java.Net.InetAddress address);
</pre>

### Type Changed: Android.Net.NetCapability

Added values:

<pre style='color: green'>
	CaptivePortal = 17,
	Validated = 16,
</pre>

### Type Changed: Android.Net.Network

Added property:

<pre style='color: green'>
	public virtual long NetworkHandle { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void BindSocket (Java.IO.FileDescriptor fd);
	public virtual Java.Net.URLConnection OpenConnection (Java.Net.URL url, Java.Net.Proxy proxy);
</pre>

### Type Changed: Android.Net.NetworkCapabilities

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const NetCapability NetCapabilityCaptivePortal;

	[Obsolete]
	public static const NetCapability NetCapabilityValidated;
</pre>

### Type Changed: Android.Net.Proxy

Obsoleted fields:

```
[Obsolete ()]
	public static const string ExtraProxyInfo = "android.intent.extra.PROXY_INFO";
```

### New Type Android.Net.CaptivePortal

<pre style='color: green'>
public class CaptivePortal : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected CaptivePortal (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void IgnoreNetwork ();
	public virtual void ReportCaptivePortalDismissed ();
	public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

## Namespace Android.Net.Wifi

### Type Changed: Android.Net.Wifi.ScanResult

Added properties:

<pre style='color: green'>
	public int CenterFreq0 { get; set; }
	public int CenterFreq1 { get; set; }
	public int ChannelWidth { get; set; }
	public virtual bool IsPasspointNetwork { get; }
	public Java.Lang.ICharSequence OperatorFriendlyName { get; set; }
	public Java.Lang.ICharSequence VenueName { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual bool Is80211mcResponder ();
</pre>

### Type Changed: Android.Net.Wifi.WifiConfiguration

Added properties:

<pre style='color: green'>
	public virtual bool IsPasspoint { get; }
	public string ProviderFriendlyName { get; set; }
	public System.Collections.Generic.IList&lt;long&gt; RoamingConsortiumIds { get; set; }
</pre>

### Type Changed: Android.Net.Wifi.WifiEapMethod

Added value:

<pre style='color: green'>
	AkaPrime = 6,
</pre>

### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig

Obsoleted properties:

```
[Obsolete ()]
	public virtual string SubjectMatch { get; set; }
```

Added properties:

<pre style='color: green'>
	public virtual string AltSubjectMatch { get; set; }
	public virtual string DomainSuffixMatch { get; set; }
	public virtual string Plmn { get; set; }
	public virtual string Realm { get; set; }
</pre>

### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig.Eap

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const WifiEapMethod AkaPrime;
</pre>

### Type Changed: Android.Net.Wifi.WifiManager

Added field:

<pre style='color: green'>
	public static const string ExtraResultsUpdated = "resultsUpdated";
</pre>

### New Type Android.Net.Wifi.WifiChannelWidth

<pre style='color: green'>
[Serializable]
public enum WifiChannelWidth {
	Width160mhz = 3,
	Width20mhz = 0,
	Width40mhz = 1,
	Width80mhz = 2,
	Width80mhzPlusMhz = 4,
}
</pre>

## Namespace Android.Nfc

### Type Changed: Android.Nfc.NfcEvent

Added properties:

<pre style='color: green'>
	public int PeerLlcpMajorVersion { get; set; }
	public int PeerLlcpMinorVersion { get; set; }
</pre>

## Namespace Android.OS

### Type Changed: Android.OS.BatteryManager

Added fields:

<pre style='color: green'>
	public static const string ActionCharging = "android.os.action.CHARGING";
	public static const string ActionDischarging = "android.os.action.DISCHARGING";
</pre>

Added property:

<pre style='color: green'>
	public virtual bool IsCharging { get; }
</pre>

### Type Changed: Android.OS.Build

### Type Changed: Android.OS.Build.VERSION

Added properties:

<pre style='color: green'>
	public static string BaseOs { get; }
	public static int PreviewSdkInt { get; }
	public static string SecurityPatch { get; }
</pre>

### Type Changed: Android.OS.Build.VERSION_CODES

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const BuildVersionCodes M;
</pre>

### Type Changed: Android.OS.BuildVersionCodes

Added value:

<pre style='color: green'>
	M = 23,
</pre>

### Type Changed: Android.OS.DeadObjectException

Added constructor:

<pre style='color: green'>
	public DeadObjectException (string message);
</pre>

### Type Changed: Android.OS.Debug

Obsoleted properties:

```
[Obsolete ()]
	public static int GlobalAllocCount { get; }
	[Obsolete ()]
	public static int GlobalAllocSize { get; }
	[Obsolete ()]
	public static int GlobalClassInitCount { get; }
	[Obsolete ()]
	public static int GlobalClassInitTime { get; }
	[Obsolete ()]
	public static int GlobalFreedCount { get; }
	[Obsolete ()]
	public static int GlobalFreedSize { get; }
	[Obsolete ()]
	public static int GlobalGcInvocationCount { get; }
	[Obsolete ()]
	public static int ThreadAllocCount { get; }
	[Obsolete ()]
	public static int ThreadAllocSize { get; }
	[Obsolete ()]
	public static int ThreadGcInvocationCount { get; }
```

Added property:

<pre style='color: green'>
	public static System.Collections.Generic.IDictionary&lt;System.String,System.String&gt; RuntimeStats { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public static void ResetAllCounts ();
	[Obsolete ()]
	public static void ResetGlobalAllocCount ();
	[Obsolete ()]
	public static void ResetGlobalAllocSize ();
	[Obsolete ()]
	public static void ResetGlobalClassInitCount ();
	[Obsolete ()]
	public static void ResetGlobalClassInitTime ();
	[Obsolete ()]
	public static void ResetGlobalFreedCount ();
	[Obsolete ()]
	public static void ResetGlobalFreedSize ();
	[Obsolete ()]
	public static void ResetGlobalGcInvocationCount ();
	[Obsolete ()]
	public static void ResetThreadAllocCount ();
	[Obsolete ()]
	public static void ResetThreadAllocSize ();
	[Obsolete ()]
	public static void ResetThreadGcInvocationCount ();
```

Added method:

<pre style='color: green'>
	public static string GetRuntimeStat (string statName);
</pre>

### Type Changed: Android.OS.Debug.MemoryInfo

Added property:

<pre style='color: green'>
	public virtual System.Collections.Generic.IDictionary&lt;System.String,System.String&gt; MemoryStats { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual string GetMemoryStat (string statName);
</pre>

### Type Changed: Android.OS.Environment

Added field:

<pre style='color: green'>
	public static const string MediaEjecting = "ejecting";
</pre>

### Type Changed: Android.OS.Looper

Added properties:

<pre style='color: green'>
	public virtual bool IsCurrentThread { get; }
	public virtual MessageQueue Queue { get; }
</pre>

### Type Changed: Android.OS.MessageQueue

Added property:

<pre style='color: green'>
	public virtual bool IsIdle { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddOnFileDescriptorEventListener (Java.IO.FileDescriptor fd, int events, MessageQueue.IOnFileDescriptorEventListener listener);
	public virtual void RemoveOnFileDescriptorEventListener (Java.IO.FileDescriptor fd);
</pre>

### New Type Android.OS.IOnFileDescriptorEventListener

<pre style='color: green'>
public interface IOnFileDescriptorEventListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual int OnFileDescriptorEvents (Java.IO.FileDescriptor fd, MessageQueueEventType events);
}
</pre>

### New Type Android.OS.FileDescriptorEventHandler

<pre style='color: green'>
public sealed delegate FileDescriptorEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public MessageQueue (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Java.IO.FileDescriptor fd, MessageQueueEventType events, System.AsyncCallback callback, object object);
	public virtual int EndInvoke (System.IAsyncResult result);
	public virtual int Invoke (Java.IO.FileDescriptor fd, MessageQueueEventType events);
}
</pre>

### Type Changed: Android.OS.Parcel

Added methods:

<pre style='color: green'>
	public Java.Lang.Object ReadTypedObject (IParcelableCreator c);
	public void WriteTypedObject (Java.Lang.Object val, ParcelableWriteFlags parcelableFlags);
</pre>

### Type Changed: Android.OS.PowerManager

Added field:

<pre style='color: green'>
	public static const string ActionDeviceIdleModeChanged = "android.os.action.DEVICE_IDLE_MODE_CHANGED";
</pre>

Added property:

<pre style='color: green'>
	public virtual bool IsDeviceIdleMode { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual bool IsIgnoringBatteryOptimizations (string packageName);
</pre>

### Type Changed: Android.OS.Process

Added method:

<pre style='color: green'>
	public static bool Is64Bit ();
</pre>

### Type Changed: Android.OS.StrictMode

### Type Changed: Android.OS.StrictMode.ThreadPolicy

### Type Changed: Android.OS.StrictMode.Builder

Added methods:

<pre style='color: green'>
	public StrictMode.ThreadPolicy.Builder DetectResourceMismatches ();
	public StrictMode.ThreadPolicy.Builder PermitResourceMismatches ();
</pre>

### Type Changed: Android.OS.StrictMode.VmPolicy

### Type Changed: Android.OS.StrictMode.Builder

Added methods:

<pre style='color: green'>
	public StrictMode.VmPolicy.Builder DetectCleartextNetwork ();
	public StrictMode.VmPolicy.Builder PenaltyDeathOnCleartextNetwork ();
</pre>

### Type Changed: Android.OS.TransactionTooLargeException

Added constructor:

<pre style='color: green'>
	public TransactionTooLargeException (string msg);
</pre>

### Type Changed: Android.OS.UserManager

Added fields:

<pre style='color: green'>
	public static const string AllowParentProfileAppLinking = "allow_parent_profile_app_linking";
	public static const string DisallowFun = "no_fun";
	public static const string DisallowNetworkReset = "no_network_reset";
	public static const string DisallowSafeBoot = "no_safe_boot";
</pre>

Added property:

<pre style='color: green'>
	public virtual bool IsSystemUser { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual bool SetRestrictionsChallenge (string newPin);
```

Added method:

<pre style='color: green'>
	public virtual long GetUserCreationTime (UserHandle userHandle);
</pre>

### New Type Android.OS.MessageQueueEventType

<pre style='color: green'>
[Serializable]
public enum MessageQueueEventType {
	Error = 4,
	Input = 1,
	Output = 2,
}
</pre>

## Namespace Android.Print

### Type Changed: Android.Print.PrintAttributes

Added property:

<pre style='color: green'>
	public DuplexMode DuplexMode { get; }
</pre>

### Type Changed: Android.Print.PrintAttributes.Builder

Added method:

<pre style='color: green'>
	public PrintAttributes.Builder SetDuplexMode (DuplexMode duplexMode);
</pre>

### Type Changed: Android.Print.PrinterCapabilitiesInfo

Added property:

<pre style='color: green'>
	public DuplexMode DuplexModes { get; }
</pre>

### Type Changed: Android.Print.PrinterCapabilitiesInfo.Builder

Added method:

<pre style='color: green'>
	public PrinterCapabilitiesInfo.Builder SetDuplexModes (DuplexMode duplexModes, DuplexMode defaultDuplexMode);
</pre>

### New Type Android.Print.DuplexMode

<pre style='color: green'>
[Serializable]
public enum DuplexMode {
	LongEdge = 2,
	None = 1,
	ShortEdge = 4,
}
</pre>

## Namespace Android.PrintServices

### Type Changed: Android.PrintServices.PrintService

Added field:

<pre style='color: green'>
	public static const string ExtraPrintDocumentInfo = "android.printservice.extra.PRINT_DOCUMENT_INFO";
</pre>

## Namespace Android.Provider

### Type Changed: Android.Provider.AlarmClock

Added fields:

<pre style='color: green'>
	public static const string ActionDismissAlarm = "android.intent.action.DISMISS_ALARM";
	public static const string ActionSnoozeAlarm = "android.intent.action.SNOOZE_ALARM";
	public static const string AlarmSearchModeAll = "android.all";
	public static const string AlarmSearchModeLabel = "android.label";
	public static const string AlarmSearchModeNext = "android.next";
	public static const string AlarmSearchModeTime = "android.time";
	public static const string ExtraAlarmSearchMode = "android.intent.extra.alarm.SEARCH_MODE";
	public static const string ExtraAlarmSnoozeDuration = "android.intent.extra.alarm.SNOOZE_DURATION";
	public static const string ExtraIsPm = "android.intent.extra.alarm.IS_PM";
</pre>

### Type Changed: Android.Provider.CallLog

### Type Changed: Android.Provider.CallLog.Calls

Added field:

<pre style='color: green'>
	public static const string CachedPhotoUri = "photo_uri";
</pre>

### Type Changed: Android.Provider.ContactsContract

### Type Changed: Android.Provider.ContactsContract.CommonDataKinds

### Type Changed: Android.Provider.ContactsContract.Callable

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Contactables

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Email

Added property:

<pre style='color: green'>
	public static Android.Net.Uri EnterpriseContentLookupUri { get; }
</pre>

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Event

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.GroupMembership

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Identity

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Im

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Nickname

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Note

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Organization

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Phone

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Photo

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Relation

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.SipAddress

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.StructuredName

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.StructuredPostal

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Website

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Contacts

Added field:

<pre style='color: green'>
	public static const string QueryParameterVcardNoPhoto = "no_photo";
</pre>

### Type Changed: Android.Provider.ContactsContract.AggregationSuggestions

### New Type Android.Provider.Builder

<pre style='color: green'>
public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public ContactsContract ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public ContactsContract.Contacts.AggregationSuggestions.Builder AddNameParameter (string name);
	public Android.Net.Uri Build ();
	public ContactsContract.Contacts.AggregationSuggestions.Builder SetContactId (long contactId);
	public ContactsContract.Contacts.AggregationSuggestions.Builder SetLimit (int limit);
}
</pre>

### Type Changed: Android.Provider.ContactsContract.Data

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Entity

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Photo

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Data

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.DataColumns

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.DisplayNameSources

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const DisplayNameSources StructuredPhoneticName;
</pre>

### Type Changed: Android.Provider.ContactsContract.Intents

### Type Changed: Android.Provider.ContactsContract.Insert

Added fields:

<pre style='color: green'>
	public static const string ExtraAccount = "android.provider.extra.ACCOUNT";
	public static const string ExtraDataSet = "android.provider.extra.DATA_SET";
</pre>

### Type Changed: Android.Provider.ContactsContract.QuickContact

Added fields:

<pre style='color: green'>
	public static const string ExtraMode = "android.provider.extra.MODE";
	public static const string ExtraPrioritizedMimetype = "android.provider.extra.PRIORITIZED_MIMETYPE";
</pre>

Added methods:

<pre style='color: green'>
	public static void ShowQuickContact (Android.Content.Context context, Android.Graphics.Rect target, Android.Net.Uri lookupUri, string[] excludeMimes, string prioritizedMimeType);
	public static void ShowQuickContact (Android.Content.Context context, Android.Views.View target, Android.Net.Uri lookupUri, string[] excludeMimes, string prioritizedMimeType);
</pre>

### Type Changed: Android.Provider.ContactsContract.RawContacts

### Type Changed: Android.Provider.ContactsContract.Data

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.Entity

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### Type Changed: Android.Provider.ContactsContract.RawContactsEntity

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

<pre style='color: green'>
	public static const string CarrierPresence = "carrier_presence";
	public static const int CarrierPresenceVtCapable;
</pre>

### New Type Android.Provider.ProviderStatus

<pre style='color: green'>
public sealed class ProviderStatus : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const string ContentType = "vnd.android.cursor.dir/provider_status";
	public static const string Status = "status";
	// properties
	public static Android.Net.Uri ContentUri { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### Type Changed: Android.Provider.DisplayNameSources

Added value:

<pre style='color: green'>
	StructuredPhoneticName = 37,
</pre>

### Type Changed: Android.Provider.DocumentsContract

Added fields:

<pre style='color: green'>
	public static const string ExtraExcludeSelf = "android.provider.extra.EXCLUDE_SELF";
	public static const string ExtraPrompt = "android.provider.extra.PROMPT";
</pre>

### Type Changed: Android.Provider.MediaStore

Added field:

<pre style='color: green'>
	public static const string MetaDataStillImageCameraPrewarmService = "android.media.still_image_camera_preview_service";
</pre>

### Type Changed: Android.Provider.Settings

Added fields:

<pre style='color: green'>
	public static const string ActionIgnoreBatteryOptimizationSettings = "android.settings.IGNORE_BATTERY_OPTIMIZATION_SETTINGS";
	public static const string ActionManageOverlayPermission = "android.settings.action.MANAGE_OVERLAY_PERMISSION";
	public static const string ActionManageWriteSettings = "android.settings.action.MANAGE_WRITE_SETTINGS";
	public static const string ActionNotificationPolicyAccessSettings = "android.settings.NOTIFICATION_POLICY_ACCESS_SETTINGS";
	public static const string ActionRequestIgnoreBatteryOptimizations = "android.settings.REQUEST_IGNORE_BATTERY_OPTIMIZATIONS";
	public static const string ActionVoiceControlAirplaneMode = "android.settings.VOICE_CONTROL_AIRPLANE_MODE";
	public static const string ActionVoiceControlBatterySaverMode = "android.settings.VOICE_CONTROL_BATTERY_SAVER_MODE";
	public static const string ActionVoiceControlDoNotDisturbMode = "android.settings.VOICE_CONTROL_DO_NOT_DISTURB_MODE";
	public static const string ExtraAirplaneModeEnabled = "airplane_mode_enabled";
	public static const string ExtraBatterySaverModeEnabled = "android.settings.extra.battery_saver_mode_enabled";
	public static const string ExtraDoNotDisturbModeEnabled = "android.settings.extra.do_not_disturb_mode_enabled";
	public static const string ExtraDoNotDisturbModeMinutes = "android.settings.extra.do_not_disturb_mode_minutes";
	public static const string IntentCategoryUsageAccessConfig = "android.intent.category.USAGE_ACCESS_CONFIG";
	public static const string MetadataUsageAccessReason = "android.settings.metadata.USAGE_ACCESS_REASON";
</pre>

Added method:

<pre style='color: green'>
	public static bool CanDrawOverlays (Android.Content.Context context);
</pre>

### Type Changed: Android.Provider.Settings.Global

Added field:

<pre style='color: green'>
	public static const string WifiDeviceOwnerConfigsLockdown = "wifi_device_owner_configs_lockdown";
</pre>

### Type Changed: Android.Provider.Settings.Secure

Obsoleted fields:

```
[Obsolete ()]
	public static const string AllowMockLocation = "mock_location";
	[Obsolete ()]
	public static const string LockPatternEnabled = "lock_pattern_autolock";
	[Obsolete ()]
	public static const string LockPatternVisible = "lock_pattern_visible_pattern";
```

### Type Changed: Android.Provider.Settings.System

Added fields:

<pre style='color: green'>
	public static const string DtmfToneTypeWhenDialing = "dtmf_tone_type";
	public static const string VibrateWhenRinging = "vibrate_when_ringing";
</pre>

Added method:

<pre style='color: green'>
	public static bool CanWrite (Android.Content.Context context);
</pre>

### Type Changed: Android.Provider.Telephony

### Type Changed: Android.Provider.Telephony.Threads

Added methods:

<pre style='color: green'>
	public static long GetOrCreateThreadId (Android.Content.Context context, string recipient);
	public static long GetOrCreateThreadId (Android.Content.Context context, System.Collections.Generic.ICollection&lt;string&gt; recipients);
</pre>

### Type Changed: Android.Provider.VoicemailContract

### Type Changed: Android.Provider.VoicemailContract.Status

Added fields:

<pre style='color: green'>
	public static const string PhoneAccountComponentName = "phone_account_component_name";
	public static const string PhoneAccountId = "phone_account_id";
</pre>

### Type Changed: Android.Provider.VoicemailContract.Voicemails

Added fields:

<pre style='color: green'>
	public static const string Deleted = "deleted";
	public static const string Dirty = "dirty";
	public static const string PhoneAccountComponentName = "subscription_component_name";
	public static const string PhoneAccountId = "subscription_id";
</pre>

### New Type Android.Provider.ContactsProviderStatus

<pre style='color: green'>
[Serializable]
public enum ContactsProviderStatus {
	Busy = 1,
	Empty = 2,
	Normal = 0,
}
</pre>

## Namespace Android.Renderscripts

### Type Changed: Android.Renderscripts.Allocation

Added methods:

<pre style='color: green'>
	public virtual void Copy1DRangeTo (int off, int count, short[] d);
	public virtual void Copy1DRangeTo (int off, int count, Java.Lang.Object array);
	public virtual void Copy1DRangeTo (int off, int count, int[] d);
	public virtual void Copy1DRangeTo (int off, int count, float[] d);
	public virtual void Copy1DRangeTo (int off, int count, byte[] d);
	public virtual void Copy1DRangeToUnchecked (int off, int count, short[] d);
	public virtual void Copy1DRangeToUnchecked (int off, int count, Java.Lang.Object array);
	public virtual void Copy1DRangeToUnchecked (int off, int count, int[] d);
	public virtual void Copy1DRangeToUnchecked (int off, int count, float[] d);
	public virtual void Copy1DRangeToUnchecked (int off, int count, byte[] d);
	public virtual void Copy2DRangeTo (int xoff, int yoff, int w, int h, short[] data);
	public virtual void Copy2DRangeTo (int xoff, int yoff, int w, int h, Java.Lang.Object array);
	public virtual void Copy2DRangeTo (int xoff, int yoff, int w, int h, int[] data);
	public virtual void Copy2DRangeTo (int xoff, int yoff, int w, int h, float[] data);
	public virtual void Copy2DRangeTo (int xoff, int yoff, int w, int h, byte[] data);
	public virtual void Copy3DRangeFrom (int xoff, int yoff, int zoff, int w, int h, int d, Java.Lang.Object array);
	public virtual void Copy3DRangeFrom (int xoff, int yoff, int zoff, int w, int h, int d, Allocation data, int dataXoff, int dataYoff, int dataZoff);
	public virtual void Copy3DRangeTo (int xoff, int yoff, int zoff, int w, int h, int d, Java.Lang.Object array);
	public virtual void SetAutoPadding (bool useAutoPadding);
	public virtual void SetFromFieldPacker (int xoff, int yoff, int zoff, int component_number, FieldPacker fp);
</pre>

### Type Changed: Android.Renderscripts.AllocationAdapter

Added methods:

<pre style='color: green'>
	public static AllocationAdapter CreateTyped (RenderScript rs, Allocation a, Type t);
	public virtual void SetX (int x);
</pre>

### Type Changed: Android.Renderscripts.Element

Added methods:

<pre style='color: green'>
	public static Element F16 (RenderScript rs);
	public static Element F16_2 (RenderScript rs);
	public static Element F16_3 (RenderScript rs);
	public static Element F16_4 (RenderScript rs);
</pre>

### Type Changed: Android.Renderscripts.Element.DataType

Added property:

<pre style='color: green'>
	public static Element.DataType Float16 { get; }
</pre>

### Type Changed: Android.Renderscripts.RenderScript

Added property:

<pre style='color: green'>
	public static long MinorVersion { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static RenderScript CreateMultiContext (Android.Content.Context ctx, RenderScript.ContextType ct, int flags, int API_number);
	public static void ReleaseAllContexts ();
</pre>

### Type Changed: Android.Renderscripts.Script

Added methods:

<pre style='color: green'>
	protected virtual Script.InvokeID CreateInvokeID (int slot);
	protected virtual void ForEach (int slot, Allocation[] ains, Allocation aout, FieldPacker v, Script.LaunchOptions sc);
	protected virtual void ForEach (int slot, Allocation[] ains, Allocation aout, FieldPacker v);
</pre>

### New Type Android.Renderscripts.InvokeID

<pre style='color: green'>
public sealed class InvokeID : Android.Renderscripts.BaseObj, System.IDisposable, Android.Runtime.IJavaObject {
}
</pre>

### Type Changed: Android.Renderscripts.ScriptGroup

Obsoleted methods:

```
[Obsolete ()]
	public void Execute ();
	[Obsolete ()]
	public void SetInput (Script.KernelID s, Allocation a);
	[Obsolete ()]
	public void SetOutput (Script.KernelID s, Allocation a);
```

Added method:

<pre style='color: green'>
	public Java.Lang.Object[] Execute (Java.Lang.Object[] inputs);
</pre>

### New Type Android.Renderscripts.Binding

<pre style='color: green'>
public sealed class Binding : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public ScriptGroup (Script.FieldID field, Java.Lang.Object value);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Renderscripts.Builder2

<pre style='color: green'>
public sealed class Builder2 : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public ScriptGroup (RenderScript rs);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public ScriptGroup.Input AddInput ();
	public ScriptGroup.Closure AddInvoke (Script.InvokeID invoke, Java.Lang.Object[] argsAndBindings);
	public ScriptGroup.Closure AddKernel (Script.KernelID k, Type returnType, Java.Lang.Object[] argsAndBindings);
	public ScriptGroup Create (string name, ScriptGroup.Future[] outputs);
}
</pre>

### New Type Android.Renderscripts.Closure

<pre style='color: green'>
public sealed class Closure : Android.Renderscripts.BaseObj, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public ScriptGroup.Future Return { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public ScriptGroup.Future GetGlobal (Script.FieldID field);
}
</pre>

### New Type Android.Renderscripts.Future

<pre style='color: green'>
public sealed class Future : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
}
</pre>

### New Type Android.Renderscripts.Input

<pre style='color: green'>
public sealed class Input : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
}
</pre>

### New Type Android.Renderscripts.ScriptIntrinsicBLAS

<pre style='color: green'>
public sealed class ScriptIntrinsicBLAS : Android.Renderscripts.ScriptIntrinsic, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const int ConjTranspose;
	public static const int Left;
	public static const int Lower;
	public static const int NonUnit;
	public static const int NoTranspose;
	public static const int Right;
	public static const int Transpose;
	public static const int Unit;
	public static const int Upper;
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void BNNM (Allocation A, int a_offset, Allocation B, int b_offset, Allocation C, int c_offset, int c_mult);
	public void CGBMV (int TransA, int KL, int KU, Float2 alpha, Allocation A, Allocation X, int incX, Float2 beta, Allocation Y, int incY);
	public void CGEMM (int TransA, int TransB, Float2 alpha, Allocation A, Allocation B, Float2 beta, Allocation C);
	public void CGEMV (int TransA, Float2 alpha, Allocation A, Allocation X, int incX, Float2 beta, Allocation Y, int incY);
	public void CGERC (Float2 alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void CGERU (Float2 alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void CHBMV (int Uplo, int K, Float2 alpha, Allocation A, Allocation X, int incX, Float2 beta, Allocation Y, int incY);
	public void CHEMM (int Side, int Uplo, Float2 alpha, Allocation A, Allocation B, Float2 beta, Allocation C);
	public void CHEMV (int Uplo, Float2 alpha, Allocation A, Allocation X, int incX, Float2 beta, Allocation Y, int incY);
	public void CHER (int Uplo, float alpha, Allocation X, int incX, Allocation A);
	public void CHER2 (int Uplo, Float2 alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void CHER2K (int Uplo, int Trans, Float2 alpha, Allocation A, Allocation B, float beta, Allocation C);
	public void CHERK (int Uplo, int Trans, float alpha, Allocation A, float beta, Allocation C);
	public void CHPMV (int Uplo, Float2 alpha, Allocation Ap, Allocation X, int incX, Float2 beta, Allocation Y, int incY);
	public void CHPR (int Uplo, float alpha, Allocation X, int incX, Allocation Ap);
	public void CHPR2 (int Uplo, Float2 alpha, Allocation X, int incX, Allocation Y, int incY, Allocation Ap);
	public static ScriptIntrinsicBLAS Create (RenderScript rs);
	public void CSYMM (int Side, int Uplo, Float2 alpha, Allocation A, Allocation B, Float2 beta, Allocation C);
	public void CSYR2K (int Uplo, int Trans, Float2 alpha, Allocation A, Allocation B, Float2 beta, Allocation C);
	public void CSYRK (int Uplo, int Trans, Float2 alpha, Allocation A, Float2 beta, Allocation C);
	public void CTBMV (int Uplo, int TransA, int Diag, int K, Allocation A, Allocation X, int incX);
	public void CTBSV (int Uplo, int TransA, int Diag, int K, Allocation A, Allocation X, int incX);
	public void CTPMV (int Uplo, int TransA, int Diag, Allocation Ap, Allocation X, int incX);
	public void CTPSV (int Uplo, int TransA, int Diag, Allocation Ap, Allocation X, int incX);
	public void CTRMM (int Side, int Uplo, int TransA, int Diag, Float2 alpha, Allocation A, Allocation B);
	public void CTRMV (int Uplo, int TransA, int Diag, Allocation A, Allocation X, int incX);
	public void CTRSM (int Side, int Uplo, int TransA, int Diag, Float2 alpha, Allocation A, Allocation B);
	public void CTRSV (int Uplo, int TransA, int Diag, Allocation A, Allocation X, int incX);
	public void DGBMV (int TransA, int KL, int KU, double alpha, Allocation A, Allocation X, int incX, double beta, Allocation Y, int incY);
	public void DGEMM (int TransA, int TransB, double alpha, Allocation A, Allocation B, double beta, Allocation C);
	public void DGEMV (int TransA, double alpha, Allocation A, Allocation X, int incX, double beta, Allocation Y, int incY);
	public void DGER (double alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void DSBMV (int Uplo, int K, double alpha, Allocation A, Allocation X, int incX, double beta, Allocation Y, int incY);
	public void DSPMV (int Uplo, double alpha, Allocation Ap, Allocation X, int incX, double beta, Allocation Y, int incY);
	public void DSPR (int Uplo, double alpha, Allocation X, int incX, Allocation Ap);
	public void DSPR2 (int Uplo, double alpha, Allocation X, int incX, Allocation Y, int incY, Allocation Ap);
	public void DSYMM (int Side, int Uplo, double alpha, Allocation A, Allocation B, double beta, Allocation C);
	public void DSYMV (int Uplo, double alpha, Allocation A, Allocation X, int incX, double beta, Allocation Y, int incY);
	public void DSYR (int Uplo, double alpha, Allocation X, int incX, Allocation A);
	public void DSYR2 (int Uplo, double alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void DSYR2K (int Uplo, int Trans, double alpha, Allocation A, Allocation B, double beta, Allocation C);
	public void DSYRK (int Uplo, int Trans, double alpha, Allocation A, double beta, Allocation C);
	public void DTBMV (int Uplo, int TransA, int Diag, int K, Allocation A, Allocation X, int incX);
	public void DTBSV (int Uplo, int TransA, int Diag, int K, Allocation A, Allocation X, int incX);
	public void DTPMV (int Uplo, int TransA, int Diag, Allocation Ap, Allocation X, int incX);
	public void DTPSV (int Uplo, int TransA, int Diag, Allocation Ap, Allocation X, int incX);
	public void DTRMM (int Side, int Uplo, int TransA, int Diag, double alpha, Allocation A, Allocation B);
	public void DTRMV (int Uplo, int TransA, int Diag, Allocation A, Allocation X, int incX);
	public void DTRSM (int Side, int Uplo, int TransA, int Diag, double alpha, Allocation A, Allocation B);
	public void DTRSV (int Uplo, int TransA, int Diag, Allocation A, Allocation X, int incX);
	public void SGBMV (int TransA, int KL, int KU, float alpha, Allocation A, Allocation X, int incX, float beta, Allocation Y, int incY);
	public void SGEMM (int TransA, int TransB, float alpha, Allocation A, Allocation B, float beta, Allocation C);
	public void SGEMV (int TransA, float alpha, Allocation A, Allocation X, int incX, float beta, Allocation Y, int incY);
	public void SGER (float alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void SSBMV (int Uplo, int K, float alpha, Allocation A, Allocation X, int incX, float beta, Allocation Y, int incY);
	public void SSPMV (int Uplo, float alpha, Allocation Ap, Allocation X, int incX, float beta, Allocation Y, int incY);
	public void SSPR (int Uplo, float alpha, Allocation X, int incX, Allocation Ap);
	public void SSPR2 (int Uplo, float alpha, Allocation X, int incX, Allocation Y, int incY, Allocation Ap);
	public void SSYMM (int Side, int Uplo, float alpha, Allocation A, Allocation B, float beta, Allocation C);
	public void SSYMV (int Uplo, float alpha, Allocation A, Allocation X, int incX, float beta, Allocation Y, int incY);
	public void SSYR (int Uplo, float alpha, Allocation X, int incX, Allocation A);
	public void SSYR2 (int Uplo, float alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void SSYR2K (int Uplo, int Trans, float alpha, Allocation A, Allocation B, float beta, Allocation C);
	public void SSYRK (int Uplo, int Trans, float alpha, Allocation A, float beta, Allocation C);
	public void STBMV (int Uplo, int TransA, int Diag, int K, Allocation A, Allocation X, int incX);
	public void STBSV (int Uplo, int TransA, int Diag, int K, Allocation A, Allocation X, int incX);
	public void STPMV (int Uplo, int TransA, int Diag, Allocation Ap, Allocation X, int incX);
	public void STPSV (int Uplo, int TransA, int Diag, Allocation Ap, Allocation X, int incX);
	public void STRMM (int Side, int Uplo, int TransA, int Diag, float alpha, Allocation A, Allocation B);
	public void STRMV (int Uplo, int TransA, int Diag, Allocation A, Allocation X, int incX);
	public void STRSM (int Side, int Uplo, int TransA, int Diag, float alpha, Allocation A, Allocation B);
	public void STRSV (int Uplo, int TransA, int Diag, Allocation A, Allocation X, int incX);
	public void ZGBMV (int TransA, int KL, int KU, Double2 alpha, Allocation A, Allocation X, int incX, Double2 beta, Allocation Y, int incY);
	public void ZGEMM (int TransA, int TransB, Double2 alpha, Allocation A, Allocation B, Double2 beta, Allocation C);
	public void ZGEMV (int TransA, Double2 alpha, Allocation A, Allocation X, int incX, Double2 beta, Allocation Y, int incY);
	public void ZGERC (Double2 alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void ZGERU (Double2 alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void ZHBMV (int Uplo, int K, Double2 alpha, Allocation A, Allocation X, int incX, Double2 beta, Allocation Y, int incY);
	public void ZHEMM (int Side, int Uplo, Double2 alpha, Allocation A, Allocation B, Double2 beta, Allocation C);
	public void ZHEMV (int Uplo, Double2 alpha, Allocation A, Allocation X, int incX, Double2 beta, Allocation Y, int incY);
	public void ZHER (int Uplo, double alpha, Allocation X, int incX, Allocation A);
	public void ZHER2 (int Uplo, Double2 alpha, Allocation X, int incX, Allocation Y, int incY, Allocation A);
	public void ZHER2K (int Uplo, int Trans, Double2 alpha, Allocation A, Allocation B, double beta, Allocation C);
	public void ZHERK (int Uplo, int Trans, double alpha, Allocation A, double beta, Allocation C);
	public void ZHPMV (int Uplo, Double2 alpha, Allocation Ap, Allocation X, int incX, Double2 beta, Allocation Y, int incY);
	public void ZHPR (int Uplo, double alpha, Allocation X, int incX, Allocation Ap);
	public void ZHPR2 (int Uplo, Double2 alpha, Allocation X, int incX, Allocation Y, int incY, Allocation Ap);
	public void ZSYMM (int Side, int Uplo, Double2 alpha, Allocation A, Allocation B, Double2 beta, Allocation C);
	public void ZSYR2K (int Uplo, int Trans, Double2 alpha, Allocation A, Allocation B, Double2 beta, Allocation C);
	public void ZSYRK (int Uplo, int Trans, Double2 alpha, Allocation A, Double2 beta, Allocation C);
	public void ZTBMV (int Uplo, int TransA, int Diag, int K, Allocation A, Allocation X, int incX);
	public void ZTBSV (int Uplo, int TransA, int Diag, int K, Allocation A, Allocation X, int incX);
	public void ZTPMV (int Uplo, int TransA, int Diag, Allocation Ap, Allocation X, int incX);
	public void ZTPSV (int Uplo, int TransA, int Diag, Allocation Ap, Allocation X, int incX);
	public void ZTRMM (int Side, int Uplo, int TransA, int Diag, Double2 alpha, Allocation A, Allocation B);
	public void ZTRMV (int Uplo, int TransA, int Diag, Allocation A, Allocation X, int incX);
	public void ZTRSM (int Side, int Uplo, int TransA, int Diag, Double2 alpha, Allocation A, Allocation B);
	public void ZTRSV (int Uplo, int TransA, int Diag, Allocation A, Allocation X, int incX);
}
</pre>

## Namespace Android.Security

### Type Changed: Android.Security.KeyChain

Obsoleted methods:

```
[Obsolete ()]
	public static bool IsBoundKeyAlgorithm (string algorithm);
```

Added method:

<pre style='color: green'>
	public static void ChoosePrivateKeyAlias (Android.App.Activity activity, IKeyChainAliasCallback response, string[] keyTypes, Java.Security.IPrincipal[] issuers, Android.Net.Uri uri, string alias);
</pre>

### New Type Android.Security.NetworkSecurityPolicy

<pre style='color: green'>
public class NetworkSecurityPolicy : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected NetworkSecurityPolicy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static NetworkSecurityPolicy Instance { get; }
	public virtual bool IsCleartextTrafficPermitted { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

## Namespace Android.Service.Carrier

### Type Changed: Android.Service.Carrier.CarrierMessagingService

Added field:

<pre style='color: green'>
	public static const int SendFlagRequestDeliveryStatus;
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void OnSendDataSms (byte[] data, int subId, string destAddress, int destPort, CarrierMessagingService.IResultCallback callback);
	[Obsolete ()]
	public virtual void OnSendMultipartTextSms (System.Collections.Generic.IList<string> parts, int subId, string destAddress, CarrierMessagingService.IResultCallback callback);
	[Obsolete ()]
	public virtual void OnSendTextSms (string text, int subId, string destAddress, CarrierMessagingService.IResultCallback callback);
```

Added methods:

<pre style='color: green'>
	public virtual void OnSendDataSms (byte[] data, int subId, string destAddress, int destPort, int sendSmsFlag, CarrierMessagingService.IResultCallback callback);
	public virtual void OnSendMultipartTextSms (System.Collections.Generic.IList&lt;string&gt; parts, int subId, string destAddress, int sendSmsFlag, CarrierMessagingService.IResultCallback callback);
	public virtual void OnSendTextSms (string text, int subId, string destAddress, int sendSmsFlag, CarrierMessagingService.IResultCallback callback);
</pre>

### New Type Android.Service.Carrier.CarrierIdentifier

<pre style='color: green'>
public class CarrierIdentifier : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected CarrierIdentifier (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CarrierIdentifier (string mcc, string mnc, string spn, string imsi, string gid1, string gid2);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual string Gid1 { get; }
	public virtual string Gid2 { get; }
	public virtual string Imsi { get; }
	public virtual string Mcc { get; }
	public virtual string Mnc { get; }
	public virtual string Spn { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Service.Carrier.CarrierService

<pre style='color: green'>
public abstract class CarrierService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected CarrierService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CarrierService ();
	// fields
	public static const string CarrierServiceInterface = "android.service.carrier.CarrierService";
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void NotifyCarrierNetworkChange (bool active);
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual Android.OS.PersistableBundle OnLoadConfig (CarrierIdentifier id);
}
</pre>

## Namespace Android.Service.Dreams

### Type Changed: Android.Service.Dreams.DreamService

Added methods:

<pre style='color: green'>
	public virtual bool OnSearchRequested (Android.Views.SearchEvent e);
	public virtual Android.Views.ActionMode OnWindowStartingActionMode (Android.Views.ActionMode.ICallback callback, Android.Views.ActionModeType type);
</pre>

## Namespace Android.Service.Media

### Type Changed: Android.Service.Media.MediaBrowserService

Added method:

<pre style='color: green'>
	public virtual void OnLoadItem (string itemId, MediaBrowserService.Result result);
</pre>

### New Type Android.Service.Media.CameraPrewarmService

<pre style='color: green'>
public abstract class CameraPrewarmService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected CameraPrewarmService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CameraPrewarmService ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual void OnCooldown (bool cameraIntentFired);
	public virtual void OnPrewarm ();
}
</pre>

## Namespace Android.Service.Notification

### Type Changed: Android.Service.Notification.InterruptionFilterType

Added values:

<pre style='color: green'>
	Alarms = 4,
	Unknown = 0,
</pre>

### Type Changed: Android.Service.Notification.NotificationListenerService

Added method:

<pre style='color: green'>
	public void SetNotificationsShown (string[] keys);
</pre>

## Namespace Android.Service.Voice

### Type Changed: Android.Service.Voice.VoiceInteractionService

Added property:

<pre style='color: green'>
	public virtual ShowFlags DisabledShowContext { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void OnLaunchVoiceAssistFromKeyguard ();
	public virtual void ShowSession (Android.OS.Bundle args, ShowFlags flags);
</pre>

### Type Changed: Android.Service.Voice.VoiceInteractionSession

Added interfaces:

<pre style='color: green'>
	Android.Content.IComponentCallbacks2
	Android.Content.IComponentCallbacks
</pre>

Added properties:

<pre style='color: green'>
	public virtual Android.Content.Context Context { get; }
	public virtual ShowFlags DisabledShowContext { get; set; }
	public virtual Android.Views.LayoutInflater LayoutInflater { get; }
	public virtual ShowFlags UserDisabledShowContext { get; }
	public virtual Android.App.Dialog Window { get; }
</pre>

Modified methods:

```
public virtual bool OnKeyDown (Android.Views.Keycode p0 keyCode, Android.Views.KeyEvent p1 e)
	public virtual bool OnKeyLongPress (Android.Views.Keycode p0 keyCode, Android.Views.KeyEvent p1 e)
	public virtual bool OnKeyMultiple (Android.Views.Keycode p0 keyCode, int p1 count, Android.Views.KeyEvent p2 e)
	public virtual bool OnKeyUp (Android.Views.Keycode p0 keyCode, Android.Views.KeyEvent p1 e)
```

Added methods:

<pre style='color: green'>
	public virtual void CloseSystemDialogs ();
	public virtual void Dump (string prefix, Java.IO.FileDescriptor fd, Java.IO.PrintWriter writer, string[] args);
	public virtual void Hide ();
	public virtual void OnAssistStructureFailure (Java.Lang.Throwable failure);
	public virtual void OnBackPressed ();
	public virtual void OnCancelRequest (VoiceInteractionSession.Request request);
	public virtual void OnComputeInsets (VoiceInteractionSession.Insets outInsets);
	public virtual void OnConfigurationChanged (Android.Content.Res.Configuration newConfig);
	public virtual void OnCreate ();
	public virtual Android.Views.View OnCreateContentView ();
	public virtual bool[] OnGetSupportedCommands (string[] commands);
	public virtual void OnHandleAssist (Android.OS.Bundle data, Android.App.Assist.AssistStructure structure, Android.App.Assist.AssistContent content);
	public virtual void OnHandleScreenshot (Android.Graphics.Bitmap screenshot);
	public virtual void OnHide ();
	public virtual void OnLockscreenShown ();
	public virtual void OnLowMemory ();
	public virtual void OnRequestAbortVoice (VoiceInteractionSession.AbortVoiceRequest request);
	public virtual void OnRequestCommand (VoiceInteractionSession.CommandRequest request);
	public virtual void OnRequestCompleteVoice (VoiceInteractionSession.CompleteVoiceRequest request);
	public virtual void OnRequestConfirmation (VoiceInteractionSession.ConfirmationRequest request);
	public virtual void OnRequestPickOption (VoiceInteractionSession.PickOptionRequest request);
	public virtual void OnShow (Android.OS.Bundle args, ShowFlags showFlags);
	public virtual void OnTaskFinished (Android.Content.Intent intent, int taskId);
	public virtual void OnTaskStarted (Android.Content.Intent intent, int taskId);
	public virtual void OnTrimMemory (Android.Content.TrimMemory level);
	public virtual void SetKeepAwake (bool keepAwake);
	public virtual void SetTheme (int theme);
	public virtual void Show (Android.OS.Bundle args, ShowFlags flags);
	public virtual void StartVoiceActivity (Android.Content.Intent intent);
</pre>

### New Type Android.Service.Voice.ShowFlags

<pre style='color: green'>
[Serializable]
public enum ShowFlags {
	SourceApplication = 8,
	SourceAssistGesture = 4,
	WithAssist = 1,
	WithScreenshot = 2,
}
</pre>

### New Type Android.Service.Voice.ToucheableInsetsType

<pre style='color: green'>
[Serializable]
public enum ToucheableInsetsType {
	Content = 1,
	Frame = 0,
	Region = 3,
}
</pre>

## Namespace Android.Speech

### Type Changed: Android.Speech.RecognitionService

### Type Changed: Android.Speech.RecognitionService.Callback

Added property:

<pre style='color: green'>
	public virtual int CallingUid { get; }
</pre>

### Type Changed: Android.Speech.RecognizerIntent

Added field:

<pre style='color: green'>
	public static const string ExtraPreferOffline = "android.speech.extra.PREFER_OFFLINE";
</pre>

## Namespace Android.Speech.Tts

### Type Changed: Android.Speech.Tts.UtteranceProgressListener

Added method:

<pre style='color: green'>
	public virtual void OnStop (string utteranceId, bool interrupted);
</pre>

## Namespace Android.Systems

### Type Changed: Android.Systems.OsConstants

Added properties:

<pre style='color: green'>
	public static int StMandlock { get; }
	public static int StNoatime { get; }
	public static int StNodev { get; }
	public static int StNodiratime { get; }
	public static int StNoexec { get; }
	public static int StNosuid { get; }
	public static int StRdonly { get; }
	public static int StRelatime { get; }
	public static int StSynchronous { get; }
</pre>

## Namespace Android.Telecom

### Type Changed: Android.Telecom.TelecomManager

Added fields:

<pre style='color: green'>
	public static const string ActionChangeDefaultDialer = "android.telecom.action.CHANGE_DEFAULT_DIALER";
	public static const string ActionChangePhoneAccounts = "android.telecom.action.CHANGE_PHONE_ACCOUNTS";
	public static const string ActionConfigurePhoneAccount = "android.telecom.action.CONFIGURE_PHONE_ACCOUNT";
	public static const string ActionDefaultDialerChanged = "android.telecom.action.DEFAULT_DIALER_CHANGED";
	public static const string ActionIncomingCall = "android.telecom.action.INCOMING_CALL";
	public static const string ActionShowCallAccessibilitySettings = "android.telecom.action.SHOW_CALL_ACCESSIBILITY_SETTINGS";
	public static const string ActionShowRespondViaSmsSettings = "android.telecom.action.SHOW_RESPOND_VIA_SMS_SETTINGS";
	public static const string ExtraCallBackNumber = "android.telecom.extra.CALL_BACK_NUMBER";
	public static const string ExtraCallSubject = "android.telecom.extra.CALL_SUBJECT";
	public static const string ExtraChangeDefaultDialerPackageName = "android.telecom.extra.CHANGE_DEFAULT_DIALER_PACKAGE_NAME";
	public static const string ExtraIncomingCallAddress = "android.telecom.extra.INCOMING_CALL_ADDRESS";
	public static const string ExtraIncomingCallExtras = "android.telecom.extra.INCOMING_CALL_EXTRAS";
	public static const string ExtraOutgoingCallExtras = "android.telecom.extra.OUTGOING_CALL_EXTRAS";
	public static const string ExtraPhoneAccountHandle = "android.telecom.extra.PHONE_ACCOUNT_HANDLE";
	public static const string ExtraStartCallWithVideoState = "android.telecom.extra.START_CALL_WITH_VIDEO_STATE";
	public static const string MetadataInCallServiceUi = "android.telecom.IN_CALL_SERVICE_UI";
</pre>

Added properties:

<pre style='color: green'>
	public virtual System.Collections.Generic.IList&lt;PhoneAccountHandle&gt; CallCapablePhoneAccounts { get; }
	public virtual string DefaultDialerPackage { get; }
	public virtual PhoneAccountHandle SimCallManager { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddNewIncomingCall (PhoneAccountHandle phoneAccount, Android.OS.Bundle extras);
	public virtual Android.Net.Uri GetAdnUriForPhoneAccount (PhoneAccountHandle accountHandle);
	public virtual PhoneAccountHandle GetDefaultOutgoingPhoneAccount (string uriScheme);
	public virtual string GetLine1Number (PhoneAccountHandle accountHandle);
	public virtual PhoneAccount GetPhoneAccount (PhoneAccountHandle account);
	public virtual string GetVoiceMailNumber (PhoneAccountHandle accountHandle);
	public virtual bool HandleMmi (string dialString, PhoneAccountHandle accountHandle);
	public virtual bool IsVoiceMailNumber (PhoneAccountHandle accountHandle, string number);
	public virtual void PlaceCall (Android.Net.Uri address, Android.OS.Bundle extras);
	public virtual void RegisterPhoneAccount (PhoneAccount account);
	public virtual void SilenceRinger ();
	public virtual void UnregisterPhoneAccount (PhoneAccountHandle accountHandle);
</pre>

### New Type Android.Telecom.Call

<pre style='color: green'>
public sealed class Call : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const string AvailablePhoneAccounts = "selectPhoneAccountAccounts";
	// properties
	public System.Collections.Generic.IList&lt;string&gt; CannedTextResponses { get; }
	public System.Collections.Generic.IList&lt;Call&gt; Children { get; }
	public System.Collections.Generic.IList&lt;Call&gt; ConferenceableCalls { get; }
	public Call Parent { get; }
	public string RemainingPostDialSequence { get; }
	public CallState State { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public InCallService.VideoCall VideoCall { get; }
	// methods
	public void Answer (VideoProfileState videoState);
	public void Conference (Call callToConferenceWith);
	public void Disconnect ();
	public Call.Details GetDetails ();
	public void Hold ();
	public void MergeConference ();
	public void PhoneAccountSelected (PhoneAccountHandle accountHandle, bool setDefault);
	public void PlayDtmfTone (char digit);
	public void PostDialContinue (bool proceed);
	public void RegisterCallback (Call.Callback callback);
	public void RegisterCallback (Call.Callback callback, Android.OS.Handler handler);
	public void Reject (bool rejectWithMessage, string textMessage);
	public void SplitFromConference ();
	public void StopDtmfTone ();
	public void SwapConference ();
	public void Unhold ();
	public void UnregisterCallback (Call.Callback callback);

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected Call (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public Call ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnCallDestroyed (Call call);
		public virtual void OnCannedTextResponsesLoaded (Call call, System.Collections.Generic.IList&lt;string&gt; cannedTextResponses);
		public virtual void OnChildrenChanged (Call call, System.Collections.Generic.IList&lt;Call&gt; children);
		public virtual void OnConferenceableCallsChanged (Call call, System.Collections.Generic.IList&lt;Call&gt; conferenceableCalls);
		public virtual void OnDetailsChanged (Call call, Call.Details details);
		public virtual void OnParentChanged (Call call, Call parent);
		public virtual void OnPostDialWait (Call call, string remainingPostDialSequence);
		public virtual void OnStateChanged (Call call, CallState state);
		public virtual void OnVideoCallChanged (Call call, InCallService.VideoCall videoCall);
	}
	public class Details : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected Call (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		public virtual PhoneAccountHandle AccountHandle { get; }
		public virtual ConnectionCapability CallCapabilities { get; }
		public virtual string CallerDisplayName { get; }
		public virtual Presentation CallerDisplayNamePresentation { get; }
		public virtual CallProperty CallProperties { get; }
		public long ConnectTimeMillis { get; }
		public virtual DisconnectCause DisconnectCause { get; }
		public virtual Android.OS.Bundle Extras { get; }
		public virtual GatewayInfo GatewayInfo { get; }
		public virtual Presentation HandlePresentation { get; }
		public virtual Android.OS.Bundle IntentExtras { get; }
		public virtual StatusHints StatusHints { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public virtual VideoProfileState VideoState { get; }
		// methods
		public virtual bool Can (ConnectionCapability capability);
		public static bool Can (ConnectionCapability capabilities, ConnectionCapability capability);
		public static string CapabilitiesToString (ConnectionCapability capabilities);
		public virtual Android.Net.Uri GetHandle ();
		public virtual bool HasProperty (CallProperty property);
		public static bool HasProperty (CallProperty properties, CallProperty property);
		public static string PropertiesToString (CallProperty properties);
	}
}
</pre>

### New Type Android.Telecom.CallAudioRoute

<pre style='color: green'>
[Serializable]
public enum CallAudioRoute {
	Bluetooth = 2,
	Earpiece = 1,
	Speaker = 8,
	WiredHeadset = 4,
	WiredOrEarpiece = 5,
}
</pre>

### New Type Android.Telecom.CallAudioState

<pre style='color: green'>
public sealed class CallAudioState : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public CallAudioState (bool muted, CallAudioRoute route, CallAudioRoute supportedRouteMask);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public bool IsMuted { get; }
	public CallAudioRoute Route { get; }
	public CallAudioRoute SupportedRouteMask { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static string AudioRouteToString (CallAudioRoute route);
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel destination, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Telecom.CallCapability

<pre style='color: green'>
[Serializable]
public enum CallCapability {
	CanPauseVideo = 1048576,
	DisconnectFromConference = 8192,
	Hold = 1,
	ManageConference = 128,
	MergeConference = 4,
	Mute = 64,
	RespondViaText = 32,
	SeparateFromConference = 4096,
	SupportHold = 2,
	SupportsVtLocalBidirectional = 768,
	SupportsVtLocalRx = 256,
	SupportsVtLocalTx = 512,
	SupportsVtRemoteBidirectional = 3072,
	SupportsVtRemoteRx = 1024,
	SupportsVtRemoteTx = 2048,
	SwapConference = 8,
}
</pre>

### New Type Android.Telecom.CallProperty

<pre style='color: green'>
[Serializable]
public enum CallProperty {
	Conference = 1,
	EmergencyCallbackMode = 4,
	GenericConference = 2,
	HighDefAudio = 16,
	Wifi = 8,
}
</pre>

### New Type Android.Telecom.CallState

<pre style='color: green'>
[Serializable]
public enum CallState {
	Active = 4,
	Connecting = 9,
	Dialing = 1,
	Disconnected = 7,
	Disconnecting = 10,
	Holding = 3,
	New = 0,
	Ringing = 2,
	SelectPhoneAccount = 8,
}
</pre>

### New Type Android.Telecom.Causes

<pre style='color: green'>
[Serializable]
public enum Causes {
	Busy = 7,
	Canceled = 4,
	ConnectionManagerNotSupported = 10,
	Error = 1,
	Local = 2,
	Missed = 5,
	Other = 9,
	Rejected = 6,
	Remote = 3,
	Restricted = 8,
	Unknown = 0,
}
</pre>

### New Type Android.Telecom.Conference

<pre style='color: green'>
public abstract class Conference : Android.Telecom.Conferenceable, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected Conference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Conference (PhoneAccountHandle phoneAccount);
	// fields
	public static const long ConnectTimeNotSpecified;
	// properties
	public CallAudioState CallAudioState { get; }
	public System.Collections.Generic.IList&lt;Connection&gt; ConferenceableConnections { get; set; }
	public ConnectionState ConnectionCapabilities { get; }
	public System.Collections.Generic.IList&lt;Connection&gt; Connections { get; }
	public long ConnectionTime { get; set; }
	public DisconnectCause DisconnectCause { get; }
	public Android.OS.Bundle Extras { get; set; }
	public PhoneAccountHandle PhoneAccountHandle { get; }
	public CallState State { get; }
	public StatusHints StatusHints { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual Connection.VideoProvider VideoProvider { get; }
	public virtual VideoProfileState VideoState { get; }
	// methods
	public bool AddConnection (Connection connection);
	public void Destroy ();
	public virtual void OnCallAudioStateChanged (CallAudioState state);
	public virtual void OnConnectionAdded (Connection connection);
	public virtual void OnDisconnect ();
	public virtual void OnHold ();
	public virtual void OnMerge ();
	public virtual void OnMerge (Connection connection);
	public virtual void OnPlayDtmfTone (char c);
	public virtual void OnSeparate (Connection connection);
	public virtual void OnStopDtmfTone ();
	public virtual void OnSwap ();
	public virtual void OnUnhold ();
	public void RemoveConnection (Connection connection);
	public void SetActive ();
	public void SetConnectionCapabilities (ConnectionCapability connectionCapabilities);
	public void SetDialing ();
	public void SetDisconnected (DisconnectCause disconnectCause);
	public void SetOnHold ();
	public void SetVideoProvider (Connection c, Connection.VideoProvider videoProvider);
	public void SetVideoState (Connection c, VideoProfileState videoState);
}
</pre>

### New Type Android.Telecom.Conferenceable

<pre style='color: green'>
public abstract class Conferenceable : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected Conferenceable (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
}
</pre>

### New Type Android.Telecom.Connection

<pre style='color: green'>
public abstract class Connection : Android.Telecom.Conferenceable, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected Connection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Connection ();
	// fields
	public static const string ExtraCallSubject = "android.telecom.extra.CALL_SUBJECT";
	public static const string ExtraChildAddress = "android.telecom.extra.CHILD_ADDRESS";
	public static const string ExtraLastForwardedNumber = "android.telecom.extra.LAST_FORWARDED_NUMBER";
	// properties
	public Android.Net.Uri Address { get; }
	public Presentation AddressPresentation { get; }
	public bool AudioModeIsVoip { get; set; }
	public CallAudioState CallAudioState { get; }
	public string CallerDisplayName { get; }
	public Presentation CallerDisplayNamePresentation { get; }
	public Conference Conference { get; }
	public System.Collections.Generic.IList&lt;Conferenceable&gt; Conferenceables { get; set; }
	public ConnectionCapability ConnectionCapabilities { get; set; }
	public DisconnectCause DisconnectCause { get; }
	public Android.OS.Bundle Extras { get; set; }
	public bool RingbackRequested { get; set; }
	public CallState State { get; }
	public StatusHints StatusHints { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static string CapabilitiesToString (ConnectionCapability capabilities);
	public static Connection CreateCanceledConnection ();
	public static Connection CreateFailedConnection (DisconnectCause disconnectCause);
	public void Destroy ();
	public Connection.VideoProvider GetVideoProvider ();
	public virtual void OnAbort ();
	public virtual void OnAnswer ();
	public virtual void OnAnswer (VideoProfileState videoState);
	public virtual void OnCallAudioStateChanged (CallAudioState state);
	public virtual void OnDisconnect ();
	public virtual void OnHold ();
	public virtual void OnPlayDtmfTone (char c);
	public virtual void OnPostDialContinue (bool proceed);
	public virtual void OnReject ();
	public virtual void OnSeparate ();
	public virtual void OnStateChanged (CallState state);
	public virtual void OnStopDtmfTone ();
	public virtual void OnUnhold ();
	public void SetActive ();
	public void SetAddress (Android.Net.Uri address, Presentation presentation);
	public void SetCallerDisplayName (string callerDisplayName, Presentation presentation);
	public void SetConferenceableConnections (System.Collections.Generic.IList&lt;Connection&gt; conferenceableConnections);
	public void SetDialing ();
	public void SetDisconnected (DisconnectCause disconnectCause);
	public void SetInitialized ();
	public void SetInitializing ();
	public void SetNextPostDialChar (char nextChar);
	public void SetOnHold ();
	public void SetPostDialWait (string remaining);
	public void SetRinging ();
	public void SetVideoProvider (Connection.VideoProvider videoProvider);
	public void SetVideoState (VideoProfileState videoState);
	public static string StateToString (ConnectionState state);

	// inner types
	public abstract class VideoProvider : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected Connection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public Connection ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void ChangeCameraCapabilities (VideoProfile.CameraCapabilities cameraCapabilities);
		public virtual void ChangePeerDimensions (int width, int height);
		public virtual void ChangeVideoQuality (VideoQuality videoQuality);
		public virtual void HandleCallSessionEvent (VideoSessionEvent e);
		public virtual void OnRequestCameraCapabilities ();
		public virtual void OnRequestConnectionDataUsage ();
		public virtual void OnSendSessionModifyRequest (VideoProfile fromProfile, VideoProfile toProfile);
		public virtual void OnSendSessionModifyResponse (VideoProfile responseProfile);
		public virtual void OnSetCamera (string cameraId);
		public virtual void OnSetDeviceOrientation (int rotation);
		public virtual void OnSetDisplaySurface (Android.Views.Surface surface);
		public virtual void OnSetPauseImage (Android.Net.Uri uri);
		public virtual void OnSetPreviewSurface (Android.Views.Surface surface);
		public virtual void OnSetZoom (float value);
		public virtual void ReceiveSessionModifyRequest (VideoProfile videoProfile);
		public virtual void ReceiveSessionModifyResponse (ModifyRequestResult status, VideoProfile requestedProfile, VideoProfile responseProfile);
		public virtual void SetCallDataUsage (long dataUsage);
	}
}
</pre>

### New Type Android.Telecom.ConnectionCapability

<pre style='color: green'>
[Serializable]
public enum ConnectionCapability {
	CanPauseVideo = 1048576,
	CanUpgradeToVideo = 524288,
	DisconnectFromConference = 8192,
	Hold = 1,
	ManageConference = 128,
	MergeConference = 4,
	Mute = 64,
	RespondViaText = 32,
	SeparateFromConference = 4096,
	SupportHold = 2,
	SupportsVtLocalBidirectional = 768,
	SupportsVtLocalRx = 256,
	SupportsVtLocalTx = 512,
	SupportsVtRemoteBidirectional = 3072,
	SupportsVtRemoteRx = 1024,
	SupportsVtRemoteTx = 2048,
	SwapConference = 8,
}
</pre>

### New Type Android.Telecom.ConnectionRequest

<pre style='color: green'>
public sealed class ConnectionRequest : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public ConnectionRequest (PhoneAccountHandle accountHandle, Android.Net.Uri handle, Android.OS.Bundle extras);
	public ConnectionRequest (PhoneAccountHandle accountHandle, Android.Net.Uri handle, Android.OS.Bundle extras, VideoProfileState videoState);
	// properties
	public PhoneAccountHandle AccountHandle { get; }
	public Android.Net.Uri Address { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public Android.OS.Bundle Extras { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public VideoProfileState VideoState { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel destination, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Telecom.ConnectionService

<pre style='color: green'>
public abstract class ConnectionService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ConnectionService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnectionService ();
	// fields
	public static const string ServiceInterface = "android.telecom.ConnectionService";
	// properties
	public System.Collections.Generic.ICollection&lt;Connection&gt; AllConnections { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void AddConference (Conference conference);
	public void AddExistingConnection (PhoneAccountHandle phoneAccountHandle, Connection connection);
	public void ConferenceRemoteConnections (RemoteConnection remoteConnection1, RemoteConnection remoteConnection2);
	public RemoteConnection CreateRemoteIncomingConnection (PhoneAccountHandle connectionManagerPhoneAccount, ConnectionRequest request);
	public RemoteConnection CreateRemoteOutgoingConnection (PhoneAccountHandle connectionManagerPhoneAccount, ConnectionRequest request);
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual void OnConference (Connection connection1, Connection connection2);
	public virtual Connection OnCreateIncomingConnection (PhoneAccountHandle connectionManagerPhoneAccount, ConnectionRequest request);
	public virtual Connection OnCreateOutgoingConnection (PhoneAccountHandle connectionManagerPhoneAccount, ConnectionRequest request);
	public virtual void OnRemoteConferenceAdded (RemoteConference conference);
	public virtual void OnRemoteExistingConnectionAdded (RemoteConnection connection);
}
</pre>

### New Type Android.Telecom.ConnectionState

<pre style='color: green'>
[Serializable]
public enum ConnectionState {
	Active = 4,
	Dialing = 3,
	Disconnected = 6,
	Holding = 5,
	Initializing = 0,
	New = 1,
	Ringing = 2,
}
</pre>

### New Type Android.Telecom.DisconnectCause

<pre style='color: green'>
public sealed class DisconnectCause : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public DisconnectCause (Causes code, Java.Lang.ICharSequence label, Java.Lang.ICharSequence description, string reason, Android.Media.Tone toneToPlay);
	public DisconnectCause (Causes code, string label, string description, string reason, Android.Media.Tone toneToPlay);
	public DisconnectCause (Causes code, Java.Lang.ICharSequence label, Java.Lang.ICharSequence description, string reason);
	public DisconnectCause (Causes code, string label, string description, string reason);
	public DisconnectCause (Causes code, string reason);
	public DisconnectCause (Causes code);
	// properties
	public Causes Code { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public string Description { get; }
	public Java.Lang.ICharSequence DescriptionFormatted { get; }
	public string Label { get; }
	public Java.Lang.ICharSequence LabelFormatted { get; }
	public string Reason { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public Android.Media.Tone Tone { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel destination, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Telecom.GatewayInfo

<pre style='color: green'>
public class GatewayInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected GatewayInfo (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public GatewayInfo (string packageName, Android.Net.Uri gatewayUri, Android.Net.Uri originalAddress);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual Android.Net.Uri GatewayAddress { get; }
	public virtual string GatewayProviderPackageName { get; }
	public virtual bool IsEmpty { get; }
	public virtual Android.Net.Uri OriginalAddress { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel destination, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Telecom.InCallService

<pre style='color: green'>
public abstract class InCallService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected InCallService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public InCallService ();
	// fields
	public static const string ServiceInterface = "android.telecom.InCallService";
	// properties
	public CallAudioState CallAudioState { get; }
	public System.Collections.Generic.IList&lt;Call&gt; Calls { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public bool CanAddCall ();
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual void OnBringToForeground (bool showDialpad);
	public virtual void OnCallAdded (Call call);
	public virtual void OnCallAudioStateChanged (CallAudioState audioState);
	public virtual void OnCallRemoved (Call call);
	public virtual void OnCanAddCallChanged (bool canAddCall);
	public void SetAudioRoute (VideoQuality route);
	public void SetMuted (bool state);

	// inner types
	public abstract class VideoCall : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected InCallService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public InCallService ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void RegisterCallback (InCallService.VideoCall.Callback callback);
		public virtual void RegisterCallback (InCallService.VideoCall.Callback callback, Android.OS.Handler handler);
		public virtual void RequestCallDataUsage ();
		public virtual void RequestCameraCapabilities ();
		public virtual void SendSessionModifyRequest (VideoProfile requestProfile);
		public virtual void SendSessionModifyResponse (VideoProfile responseProfile);
		public virtual void SetCamera (string cameraId);
		public virtual void SetDeviceOrientation (int rotation);
		public virtual void SetDisplaySurface (Android.Views.Surface surface);
		public virtual void SetPauseImage (Android.Net.Uri uri);
		public virtual void SetPreviewSurface (Android.Views.Surface surface);
		public virtual void SetZoom (float value);
		public virtual void UnregisterCallback (InCallService.VideoCall.Callback callback);

		// inner types
		public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
			// constructors
			protected InCallService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
			public InCallService ();
			// properties
			protected override IntPtr ThresholdClass { get; }
			protected override System.Type ThresholdType { get; }
			// methods
			public virtual void OnCallDataUsageChanged (long dataUsage);
			public virtual void OnCallSessionEvent (VideoSessionEvent e);
			public virtual void OnCameraCapabilitiesChanged (VideoProfile.CameraCapabilities cameraCapabilities);
			public virtual void OnPeerDimensionsChanged (int width, int height);
			public virtual void OnSessionModifyRequestReceived (VideoProfile videoProfile);
			public virtual void OnSessionModifyResponseReceived (ModifyRequestResult status, VideoProfile requestedProfile, VideoProfile responseProfile);
			public virtual void OnVideoQualityChanged (VideoQuality videoQuality);
		}
	}
}
</pre>

### New Type Android.Telecom.ModifyRequestResult

<pre style='color: green'>
[Serializable]
public enum ModifyRequestResult {
	Fail = 2,
	Invalid = 3,
	RejectedByRemote = 5,
	Success = 1,
	TimedOut = 4,
}
</pre>

### New Type Android.Telecom.PhoneAccount

<pre style='color: green'>
public sealed class PhoneAccount : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields
	public static const int NoHighlightColor;
	public static const int NoResourceId;
	public static const string SchemeSip = "sip";
	public static const string SchemeTel = "tel";
	public static const string SchemeVoicemail = "voicemail";
	// properties
	public PhoneAccountHandle AccountHandle { get; }
	public Android.Net.Uri Address { get; }
	public ConnectionCapability Capabilities { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public int HighlightColor { get; }
	public Android.Graphics.Drawables.Icon Icon { get; }
	public bool IsEnabled { get; }
	public string Label { get; }
	public Java.Lang.ICharSequence LabelFormatted { get; }
	public string ShortDescription { get; }
	public Java.Lang.ICharSequence ShortDescriptionFormatted { get; }
	public Android.Net.Uri SubscriptionAddress { get; }
	public System.Collections.Generic.IList&lt;string&gt; SupportedUriSchemes { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public bool HasCapabilities (ConnectionCapability capability);
	public static PhoneAccount.Builder InvokeBuilder (PhoneAccountHandle accountHandle, Java.Lang.ICharSequence label);
	public static PhoneAccount.Builder InvokeBuilder (PhoneAccountHandle accountHandle, string label);
	public bool SupportsUriScheme (string uriScheme);
	public PhoneAccount.Builder ToBuilder ();
	public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected PhoneAccount (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public PhoneAccount (PhoneAccountHandle accountHandle, Java.Lang.ICharSequence label);
		public PhoneAccount (PhoneAccountHandle accountHandle, string label);
		public PhoneAccount (PhoneAccount phoneAccount);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual PhoneAccount.Builder AddSupportedUriScheme (string uriScheme);
		public virtual PhoneAccount Build ();
		public virtual PhoneAccount.Builder SetAddress (Android.Net.Uri value);
		public virtual PhoneAccount.Builder SetCapabilities (int value);
		public virtual PhoneAccount.Builder SetHighlightColor (int value);
		public virtual PhoneAccount.Builder SetIcon (Android.Graphics.Drawables.Icon icon);
		public virtual PhoneAccount.Builder SetShortDescription (Java.Lang.ICharSequence value);
		public PhoneAccount.Builder SetShortDescription (string value);
		public virtual PhoneAccount.Builder SetSubscriptionAddress (Android.Net.Uri value);
		public virtual PhoneAccount.Builder SetSupportedUriSchemes (System.Collections.Generic.IList&lt;string&gt; uriSchemes);
	}
}
</pre>

### New Type Android.Telecom.PhoneAccountCapability

<pre style='color: green'>
[Serializable]
public enum PhoneAccountCapability {
	CallProvider = 2,
	CallSubject = 64,
	ConnectionManager = 1,
	PlaceEmergencyCalls = 16,
	SimSubscription = 4,
	VideoCalling = 8,
}
</pre>

### New Type Android.Telecom.PhoneAccountHandle

<pre style='color: green'>
public sealed class PhoneAccountHandle : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public PhoneAccountHandle (Android.Content.ComponentName componentName, string id);
	public PhoneAccountHandle (Android.Content.ComponentName componentName, string id, Android.OS.UserHandle userHandle);
	// properties
	public Android.Content.ComponentName ComponentName { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public string Id { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public Android.OS.UserHandle UserHandle { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Telecom.RemoteConference

<pre style='color: green'>
public sealed class RemoteConference : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public System.Collections.Generic.IList&lt;RemoteConnection&gt; ConferenceableConnections { get; }
	public ConnectionCapability ConnectionCapabilities { get; }
	public System.Collections.Generic.IList&lt;RemoteConnection&gt; Connections { get; }
	public DisconnectCause DisconnectCause { get; }
	public Android.OS.Bundle Extras { get; }
	public CallState State { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void Disconnect ();
	public void Hold ();
	public void Merge ();
	public void PlayDtmfTone (char digit);
	public void RegisterCallback (RemoteConference.Callback callback, Android.OS.Handler handler);
	public void RegisterCallback (RemoteConference.Callback callback);
	public void Separate (RemoteConnection connection);
	public void SetCallAudioState (CallAudioState state);
	public void StopDtmfTone ();
	public void Swap ();
	public void Unhold ();
	public void UnregisterCallback (RemoteConference.Callback callback);

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected RemoteConference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public RemoteConference ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnConferenceableConnectionsChanged (RemoteConference conference, System.Collections.Generic.IList&lt;RemoteConnection&gt; conferenceableConnections);
		public virtual void OnConnectionAdded (RemoteConference conference, RemoteConnection connection);
		public virtual void OnConnectionCapabilitiesChanged (RemoteConference conference, ConnectionCapability connectionCapabilities);
		public virtual void OnConnectionRemoved (RemoteConference conference, RemoteConnection connection);
		public virtual void OnDestroyed (RemoteConference conference);
		public virtual void OnDisconnected (RemoteConference conference, DisconnectCause disconnectCause);
		public virtual void OnExtrasChanged (RemoteConference conference, Android.OS.Bundle extras);
		public virtual void OnStateChanged (RemoteConference conference, CallState oldState, CallState newState);
	}
}
</pre>

### New Type Android.Telecom.RemoteConnection

<pre style='color: green'>
public sealed class RemoteConnection : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public Android.Net.Uri Address { get; }
	public Presentation AddressPresentation { get; }
	public string CallerDisplayName { get; }
	public Java.Lang.ICharSequence CallerDisplayNameFormatted { get; }
	public Presentation CallerDisplayNamePresentation { get; }
	public RemoteConference Conference { get; }
	public System.Collections.Generic.IList&lt;RemoteConnection&gt; ConferenceableConnections { get; }
	public ConnectionCapability ConnectionCapabilities { get; }
	public DisconnectCause DisconnectCause { get; }
	public Android.OS.Bundle Extras { get; }
	public bool IsRingbackRequested { get; }
	public bool IsVoipAudioMode { get; }
	public CallState State { get; }
	public StatusHints StatusHints { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public VideoQuality VideoState { get; }
	// methods
	public void Abort ();
	public void Answer ();
	public void Disconnect ();
	public RemoteConnection.VideoProvider GetVideoProvider ();
	public void Hold ();
	public void PlayDtmfTone (char digit);
	public void PostDialContinue (bool proceed);
	public void RegisterCallback (RemoteConnection.Callback callback);
	public void RegisterCallback (RemoteConnection.Callback callback, Android.OS.Handler handler);
	public void Reject ();
	public void SetCallAudioState (CallAudioState state);
	public void StopDtmfTone ();
	public void Unhold ();
	public void UnregisterCallback (RemoteConnection.Callback callback);

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected RemoteConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public RemoteConnection ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnAddressChanged (RemoteConnection connection, Android.Net.Uri address, Presentation presentation);
		public virtual void OnCallerDisplayNameChanged (RemoteConnection connection, string callerDisplayName, Presentation presentation);
		public virtual void OnConferenceableConnectionsChanged (RemoteConnection connection, System.Collections.Generic.IList&lt;RemoteConnection&gt; conferenceableConnections);
		public virtual void OnConferenceChanged (RemoteConnection connection, RemoteConference conference);
		public virtual void OnConnectionCapabilitiesChanged (RemoteConnection connection, ConnectionCapability connectionCapabilities);
		public virtual void OnDestroyed (RemoteConnection connection);
		public virtual void OnDisconnected (RemoteConnection connection, DisconnectCause disconnectCause);
		public virtual void OnExtrasChanged (RemoteConnection connection, Android.OS.Bundle extras);
		public virtual void OnPostDialChar (RemoteConnection connection, char nextChar);
		public virtual void OnPostDialWait (RemoteConnection connection, string remainingPostDialSequence);
		public virtual void OnRingbackRequested (RemoteConnection connection, bool ringback);
		public virtual void OnStateChanged (RemoteConnection connection, CallState state);
		public virtual void OnStatusHintsChanged (RemoteConnection connection, StatusHints statusHints);
		public virtual void OnVideoProviderChanged (RemoteConnection connection, RemoteConnection.VideoProvider videoProvider);
		public virtual void OnVideoStateChanged (RemoteConnection connection, VideoProfileState videoState);
		public virtual void OnVoipAudioChanged (RemoteConnection connection, bool isVoip);
	}
	public class VideoProvider : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected RemoteConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void RegisterCallback (RemoteConnection.VideoProvider.Callback l);
		public virtual void RequestCallDataUsage ();
		public virtual void RequestCameraCapabilities ();
		public virtual void SendSessionModifyRequest (VideoProfile fromProfile, VideoProfile toProfile);
		public virtual void SendSessionModifyResponse (VideoProfile responseProfile);
		public virtual void SetCamera (string cameraId);
		public virtual void SetDeviceOrientation (int rotation);
		public virtual void SetDisplaySurface (Android.Views.Surface surface);
		public virtual void SetPauseImage (Android.Net.Uri uri);
		public virtual void SetPreviewSurface (Android.Views.Surface surface);
		public virtual void SetZoom (float value);
		public virtual void UnregisterCallback (RemoteConnection.VideoProvider.Callback l);

		// inner types
		public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
			// constructors
			protected RemoteConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
			public RemoteConnection ();
			// properties
			protected override IntPtr ThresholdClass { get; }
			protected override System.Type ThresholdType { get; }
			// methods
			public virtual void OnCallDataUsageChanged (RemoteConnection.VideoProvider videoProvider, long dataUsage);
			public virtual void OnCallSessionEvent (RemoteConnection.VideoProvider videoProvider, VideoSessionEvent e);
			public virtual void OnCameraCapabilitiesChanged (RemoteConnection.VideoProvider videoProvider, VideoProfile.CameraCapabilities cameraCapabilities);
			public virtual void OnPeerDimensionsChanged (RemoteConnection.VideoProvider videoProvider, int width, int height);
			public virtual void OnSessionModifyRequestReceived (RemoteConnection.VideoProvider videoProvider, VideoProfile videoProfile);
			public virtual void OnSessionModifyResponseReceived (RemoteConnection.VideoProvider videoProvider, VideoProfileState status, VideoProfile requestedProfile, VideoProfile responseProfile);
			public virtual void OnVideoQualityChanged (RemoteConnection.VideoProvider videoProvider, VideoQuality videoQuality);
		}
	}
}
</pre>

### New Type Android.Telecom.StatusHints

<pre style='color: green'>
public sealed class StatusHints : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public StatusHints (Java.Lang.ICharSequence label, Android.Graphics.Drawables.Icon icon, Android.OS.Bundle extras);
	public StatusHints (string label, Android.Graphics.Drawables.Icon icon, Android.OS.Bundle extras);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public Android.OS.Bundle Extras { get; }
	public Android.Graphics.Drawables.Icon Icon { get; }
	public string Label { get; }
	public Java.Lang.ICharSequence LabelFormatted { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Telecom.VideoProfile

<pre style='color: green'>
public class VideoProfile : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected VideoProfile (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public VideoProfile (VideoProfileState videoState);
	public VideoProfile (VideoProfileState videoState, int quality);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual VideoQuality Quality { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual VideoProfileState VideoState { get; }
	// methods
	public virtual int DescribeContents ();
	public static bool IsAudioOnly (VideoProfileState videoState);
	public static bool IsBidirectional (VideoProfileState videoState);
	public static bool IsPaused (VideoProfileState videoState);
	public static bool IsReceptionEnabled (VideoProfileState videoState);
	public static bool IsTransmissionEnabled (VideoProfileState videoState);
	public static bool IsVideo (VideoProfileState videoState);
	public static string VideoStateToString (VideoProfileState videoState);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class CameraCapabilities : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		public VideoProfile (int width, int height);
		// properties
		public static Android.OS.IParcelableCreator Creator { get; }
		public int Height { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public int Width { get; }
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
}
</pre>

### New Type Android.Telecom.VideoProfileState

<pre style='color: green'>
[Serializable]
public enum VideoProfileState {
	AudioOnly = 0,
	Bidirectional = 3,
	Paused = 4,
	RxEnabled = 2,
	TxEnabled = 1,
}
</pre>

### New Type Android.Telecom.VideoQuality

<pre style='color: green'>
[Serializable]
public enum VideoQuality {
	Default = 4,
	High = 1,
	Low = 3,
	Medium = 2,
}
</pre>

### New Type Android.Telecom.VideoSessionEvent

<pre style='color: green'>
[Serializable]
public enum VideoSessionEvent {
	CameraFailure = 5,
	CameraReady = 6,
	RxPause = 1,
	RxResume = 2,
	TxStart = 3,
	TxStop = 4,
}
</pre>

## Namespace Android.Telephony

### Type Changed: Android.Telephony.CellSignalStrength

Added fields:

<pre style='color: green'>
	public static const int SignalStrengthGood;
	public static const int SignalStrengthGreat;
	public static const int SignalStrengthModerate;
	public static const int SignalStrengthNoneOrUnknown;
	public static const int SignalStrengthPoor;
</pre>

### Type Changed: Android.Telephony.PhoneNumberUtils

Added methods:

<pre style='color: green'>
	public static void AddTtsSpan (Android.Text.ISpannable s, int start, int endExclusive);
	public static Android.Text.Style.TtsSpan CreateTtsSpan (string phoneNumberString);
	public static string CreateTtsSpannable (string phoneNumber);
	public static Java.Lang.ICharSequence CreateTtsSpannableFormatted (Java.Lang.ICharSequence phoneNumber);
	public static string FormatNumberToRFC3966 (string phoneNumber, string defaultCountryIso);
</pre>

### Type Changed: Android.Telephony.SignalStrength

Added property:

<pre style='color: green'>
	public virtual int Level { get; }
</pre>

### Type Changed: Android.Telephony.SmsManager

Added field:

<pre style='color: green'>
	public static const string MmsConfigSupportHttpCharsetHeader = "supportHttpCharsetHeader";
</pre>

### Type Changed: Android.Telephony.SmsMessage

Obsoleted methods:

```
[Obsolete ()]
	public static SmsMessage CreateFromPdu (byte[] pdu);
```

Added method:

<pre style='color: green'>
	public static SmsMessage CreateFromPdu (byte[] pdu, string format);
</pre>

### Type Changed: Android.Telephony.TelephonyManager

Added fields:

<pre style='color: green'>
	public static const string ActionConfigureVoicemail = "android.telephony.action.CONFIGURE_VOICEMAIL";
	public static const string VvmTypeCvvm = "vvm_type_cvvm";
	public static const string VvmTypeOmtp = "vvm_type_omtp";
</pre>

Obsoleted properties:

```
[Obsolete ()]
	public virtual System.Collections.Generic.IList<NeighboringCellInfo> NeighboringCellInfo { get; }
```

Added properties:

<pre style='color: green'>
	public virtual bool IsHearingAidCompatibilitySupported { get; }
	public virtual bool IsTtyModeSupported { get; }
	public virtual bool IsWorldPhone { get; }
	public virtual int PhoneCount { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool CanChangeDtmfToneLength ();
	public virtual string GetDeviceId (int slotId);
</pre>

### New Type Android.Telephony.CarrierConfigManager

<pre style='color: green'>
public class CarrierConfigManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CarrierConfigManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const string ActionCarrierConfigChanged = "android.telephony.action.CARRIER_CONFIG_CHANGED";
	public static const string KeyAdditionalCallSettingBool = "additional_call_setting_bool";
	public static const string KeyAllowEmergencyNumbersInCallLogBool = "allow_emergency_numbers_in_call_log_bool";
	public static const string KeyAllowLocalDtmfTonesBool = "allow_local_dtmf_tones_bool";
	public static const string KeyApnExpandBool = "apn_expand_bool";
	public static const string KeyAutoRetryEnabledBool = "auto_retry_enabled_bool";
	public static const string KeyCarrierAllowTurnoffImsBool = "carrier_allow_turnoff_ims_bool";
	public static const string KeyCarrierSettingsEnableBool = "carrier_settings_enable_bool";
	public static const string KeyCarrierVolteAvailableBool = "carrier_volte_available_bool";
	public static const string KeyCarrierVolteProvisioningRequiredBool = "carrier_volte_provisioning_required_bool";
	public static const string KeyCarrierVolteTtySupportedBool = "carrier_volte_tty_supported_bool";
	public static const string KeyCarrierVtAvailableBool = "carrier_vt_available_bool";
	public static const string KeyCarrierVvmPackageNameString = "carrier_vvm_package_name_string";
	public static const string KeyCarrierWfcImsAvailableBool = "carrier_wfc_ims_available_bool";
	public static const string KeyCdmaNonroamingNetworksStringArray = "cdma_nonroaming_networks_string_array";
	public static const string KeyCdmaRoamingNetworksStringArray = "cdma_roaming_networks_string_array";
	public static const string KeyCspEnabledBool = "csp_enabled_bool";
	public static const string KeyDefaultSimCallManagerString = "default_sim_call_manager_string";
	public static const string KeyDisableCdmaActivationCodeBool = "disable_cdma_activation_code_bool";
	public static const string KeyDtmfTypeEnabledBool = "dtmf_type_enabled_bool";
	public static const string KeyEnableDialerKeyVibrationBool = "enable_dialer_key_vibration_bool";
	public static const string KeyForceHomeNetworkBool = "force_home_network_bool";
	public static const string KeyGsmNonroamingNetworksStringArray = "gsm_nonroaming_networks_string_array";
	public static const string KeyGsmRoamingNetworksStringArray = "gsm_roaming_networks_string_array";
	public static const string KeyHasInCallNoiseSuppressionBool = "has_in_call_noise_suppression_bool";
	public static const string KeyHideCarrierNetworkSettingsBool = "hide_carrier_network_settings_bool";
	public static const string KeyHideSimLockSettingsBool = "hide_sim_lock_settings_bool";
	public static const string KeyIgnoreSimNetworkLockedEventsBool = "ignore_sim_network_locked_events_bool";
	public static const string KeyMmsAliasEnabledBool = "aliasEnabled";
	public static const string KeyMmsAliasMaxCharsInt = "aliasMaxChars";
	public static const string KeyMmsAliasMinCharsInt = "aliasMinChars";
	public static const string KeyMmsAllowAttachAudioBool = "allowAttachAudio";
	public static const string KeyMmsAppendTransactionIdBool = "enabledTransID";
	public static const string KeyMmsEmailGatewayNumberString = "emailGatewayNumber";
	public static const string KeyMmsGroupMmsEnabledBool = "enableGroupMms";
	public static const string KeyMmsHttpParamsString = "httpParams";
	public static const string KeyMmsHttpSocketTimeoutInt = "httpSocketTimeout";
	public static const string KeyMmsMaxImageHeightInt = "maxImageHeight";
	public static const string KeyMmsMaxImageWidthInt = "maxImageWidth";
	public static const string KeyMmsMaxMessageSizeInt = "maxMessageSize";
	public static const string KeyMmsMessageTextMaxSizeInt = "maxMessageTextSize";
	public static const string KeyMmsMmsDeliveryReportEnabledBool = "enableMMSDeliveryReports";
	public static const string KeyMmsMmsEnabledBool = "enabledMMS";
	public static const string KeyMmsMmsReadReportEnabledBool = "enableMMSReadReports";
	public static const string KeyMmsMultipartSmsEnabledBool = "enableMultipartSMS";
	public static const string KeyMmsNaiSuffixString = "naiSuffix";
	public static const string KeyMmsNotifyWapMmscEnabledBool = "enabledNotifyWapMMSC";
	public static const string KeyMmsRecipientLimitInt = "recipientLimit";
	public static const string KeyMmsSendMultipartSmsAsSeparateMessagesBool = "sendMultipartSmsAsSeparateMessages";
	public static const string KeyMmsShowCellBroadcastAppLinksBool = "config_cellBroadcastAppLinks";
	public static const string KeyMmsSmsDeliveryReportEnabledBool = "enableSMSDeliveryReports";
	public static const string KeyMmsSmsToMmsTextLengthThresholdInt = "smsToMmsTextLengthThreshold";
	public static const string KeyMmsSmsToMmsTextThresholdInt = "smsToMmsTextThreshold";
	public static const string KeyMmsSubjectMaxLengthInt = "maxSubjectLength";
	public static const string KeyMmsSupportHttpCharsetHeaderBool = "supportHttpCharsetHeader";
	public static const string KeyMmsSupportMmsContentDispositionBool = "supportMmsContentDisposition";
	public static const string KeyMmsUaProfTagNameString = "uaProfTagName";
	public static const string KeyMmsUaProfUrlString = "uaProfUrl";
	public static const string KeyMmsUserAgentString = "userAgent";
	public static const string KeyOperatorSelectionExpandBool = "operator_selection_expand_bool";
	public static const string KeyPrefer2gBool = "prefer_2g_bool";
	public static const string KeyShowApnSettingCdmaBool = "show_apn_setting_cdma_bool";
	public static const string KeyShowCdmaChoicesBool = "show_cdma_choices_bool";
	public static const string KeyShowOnscreenDialButtonBool = "show_onscreen_dial_button_bool";
	public static const string KeySimNetworkUnlockAllowDismissBool = "sim_network_unlock_allow_dismiss_bool";
	public static const string KeySupportPauseImsVideoCallsBool = "support_pause_ims_video_calls_bool";
	public static const string KeySupportSwapAfterMergeBool = "support_swap_after_merge_bool";
	public static const string KeyUseHfaForProvisioningBool = "use_hfa_for_provisioning_bool";
	public static const string KeyUseOtaspForProvisioningBool = "use_otasp_for_provisioning_bool";
	public static const string KeyVoicemailNotificationPersistentBool = "voicemail_notification_persistent_bool";
	public static const string KeyVoicePrivacyDisableUiBool = "voice_privacy_disable_ui_bool";
	public static const string KeyVolteReplacementRatInt = "volte_replacement_rat_int";
	public static const string KeyVvmDestinationNumberString = "vvm_destination_number_string";
	public static const string KeyVvmPortNumberInt = "vvm_port_number_int";
	public static const string KeyVvmTypeString = "vvm_type_string";
	public static const string KeyWorldPhoneBool = "world_phone_bool";
	// properties
	public virtual Android.OS.PersistableBundle Config { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.OS.PersistableBundle GetConfigForSubId (int subId);
	public virtual void NotifyConfigChangedForSubId (int subId);
}
</pre>

## Namespace Android.Test.Mock

### Type Changed: Android.Test.Mock.MockContext

Added methods:

<pre style='color: green'>
	public override Android.Content.PM.Permission CheckSelfPermission (string permission);
	public override string GetSystemServiceName (Java.Lang.Class serviceClass);
</pre>

### Type Changed: Android.Test.Mock.MockCursor

Modified properties:

```
public virtual Android.OS.Bundle Extras { get; set; }
```

Obsoleted methods:

```
[Obsolete ()]
	public virtual void Deactivate ();
	[Obsolete ()]
	public virtual bool Requery ();
```

### Type Changed: Android.Test.Mock.MockPackageManager

Added methods:

<pre style='color: green'>
	public virtual System.Collections.Generic.IList&lt;Android.Content.IntentFilter&gt; GetAllIntentFilters (string packageName);
	public virtual string GetDefaultBrowserPackageName (int userId);
	public override bool IsPermissionRevokedByPolicy (string permName, string pkgName);
	public virtual bool SetDefaultBrowserPackageName (string packageName, int userId);
</pre>

## Namespace Android.Text

### Type Changed: Android.Text.SpannableStringBuilder

Added property:

<pre style='color: green'>
	public virtual int TextWatcherDepth { get; }
</pre>

### New Type Android.Text.BreakStrategy

<pre style='color: green'>
[Serializable]
public enum BreakStrategy {
	Balanced = 2,
	HighQuality = 1,
	Simple = 0,
}
</pre>

### New Type Android.Text.HyphenationFrequency

<pre style='color: green'>
[Serializable]
public enum HyphenationFrequency {
	Full = 2,
	None = 0,
	Normal = 1,
}
</pre>

## Namespace Android.Text.Format

### Type Changed: Android.Text.Format.Formatter

Modified methods:

```
public string FormatFileSize (Android.Content.Context context, long number sizeBytes)
	public string FormatShortFileSize (Android.Content.Context context, long number sizeBytes)
```

## Namespace Android.Transitions

### Type Changed: Android.Transitions.Transition

Added method:

<pre style='color: green'>
	public virtual bool IsTransitionRequired (TransitionValues startValues, TransitionValues endValues);
</pre>

### Type Changed: Android.Transitions.TransitionManager

Added method:

<pre style='color: green'>
	public static void EndTransitions (Android.Views.ViewGroup sceneRoot);
</pre>

### New Type Android.Transitions.ChangeScroll

<pre style='color: green'>
public class ChangeScroll : Android.Transitions.Transition, Java.Lang.ICloneable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ChangeScroll (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ChangeScroll ();
	public ChangeScroll (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void CaptureEndValues (TransitionValues transitionValues);
	public override void CaptureStartValues (TransitionValues transitionValues);
}
</pre>

## Namespace Android.Util

### Type Changed: Android.Util.DisplayMetrics

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const DisplayMetricsDensity Density360;

	[Obsolete]
	public static const DisplayMetricsDensity Density420;
</pre>

### Type Changed: Android.Util.DisplayMetricsDensity

Added values:

<pre style='color: green'>
	D360 = 360,
	D420 = 420,
</pre>

### Type Changed: Android.Util.EventLog

Added methods:

<pre style='color: green'>
	public static int WriteEvent (int tag, float value);
	public static System.Threading.Tasks.Task&lt;int&gt; WriteEventAsync (int tag, float value);
</pre>

### New Type Android.Util.ArraySet

<pre style='color: green'>
public sealed class ArraySet : Java.Lang.Object, Java.Util.ICollection, Java.Util.ISet, Java.Lang.IIterable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public ArraySet (ArraySet set);
	public ArraySet (int capacity);
	public ArraySet ();
	// properties
	public virtual bool IsEmpty { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Add (Java.Lang.Object value);
	public void AddAll (ArraySet array);
	public virtual bool AddAll (System.Collections.ICollection collection);
	public virtual void Clear ();
	public virtual bool Contains (Java.Lang.Object key);
	public virtual bool ContainsAll (System.Collections.ICollection collection);
	public void EnsureCapacity (int minimumCapacity);
	public int IndexOf (Java.Lang.Object key);
	public virtual Java.Util.IIterator Iterator ();
	public virtual bool Remove (Java.Lang.Object object);
	public bool RemoveAll (ArraySet array);
	public virtual bool RemoveAll (System.Collections.ICollection collection);
	public Java.Lang.Object RemoveAt (int index);
	public virtual bool RetainAll (System.Collections.ICollection collection);
	public virtual int Size ();
	public virtual Java.Lang.Object[] ToArray ();
	public virtual Java.Lang.Object[] ToArray (Java.Lang.Object[] array);
	public Java.Lang.Object ValueAt (int index);
}
</pre>

## Namespace Android.Views

### Type Changed: Android.Views.ActionMode

Added field:

<pre style='color: green'>
	public static const int DefaultHideDuration;
</pre>

Added property:

<pre style='color: green'>
	public virtual ActionModeType Type { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void Hide (long duration);
	public virtual void InvalidateContentRect ();
	public virtual void OnWindowFocusChanged (bool hasWindowFocus);
</pre>

### New Type Android.Views.Callback2

<pre style='color: green'>
public abstract class Callback2 : Java.Lang.Object, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ActionMode (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ActionMode ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool OnActionItemClicked (ActionMode mode, IMenuItem item);
	public virtual bool OnCreateActionMode (ActionMode mode, IMenu menu);
	public virtual void OnDestroyActionMode (ActionMode mode);
	public virtual void OnGetContentRect (ActionMode mode, View view, Android.Graphics.Rect outRect);
	public virtual bool OnPrepareActionMode (ActionMode mode, IMenu menu);
}
</pre>

### Type Changed: Android.Views.ContextThemeWrapper

Modified constructors:

```
public ContextThemeWrapper (Android.Content.Context base, int themeres themeResId)
```

Added constructor:

<pre style='color: green'>
	public ContextThemeWrapper (Android.Content.Context base, Android.Content.Res.Resources.Theme theme);
</pre>

### Type Changed: Android.Views.Display

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const DisplayFlags FlagRound;
	public static const int InvalidDisplay;
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual float[] GetSupportedRefreshRates ();
```

Added methods:

<pre style='color: green'>
	public virtual Display.Mode GetMode ();
	public virtual Display.Mode[] GetSupportedModes ();
</pre>

### Type Changed: Android.Views.DisplayFlags

Added value:

<pre style='color: green'>
	Round = 16,
</pre>

### Type Changed: Android.Views.FeedbackConstants

Added value:

<pre style='color: green'>
	ContextClick = 6,
</pre>

### Type Changed: Android.Views.GestureDetector

Added event:

<pre style='color: green'>
	public event System.EventHandler&lt;GestureDetector.ContextClickEventArgs&gt; ContextClick;
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool OnGenericMotionEvent (MotionEvent ev);
	public virtual void SetContextClickListener (GestureDetector.IOnContextClickListener onContextClickListener);
</pre>

### Type Changed: Android.Views.GestureDetector.SimpleOnGestureListener

Added method:

<pre style='color: green'>
	public virtual bool OnContextClick (MotionEvent e);
</pre>

### New Type Android.Views.IOnContextClickListener

<pre style='color: green'>
public interface IOnContextClickListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual bool OnContextClick (MotionEvent e);
}
</pre>

### New Type Android.Views.ContextClickEventArgs

<pre style='color: green'>
public class ContextClickEventArgs : System.EventArgs {
	// constructors
	public GestureDetector (bool handled, MotionEvent e);
	// properties
	public MotionEvent Event { get; }
	public bool Handled { get; set; }
}
</pre>

### Type Changed: Android.Views.HapticFeedbackConstants

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const FeedbackConstants ContextClick;
</pre>

### Type Changed: Android.Views.InputDevice

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const InputSourceType SourceBluetoothStylus;
</pre>

Added property:

<pre style='color: green'>
	public bool HasMicrophone { get; }
</pre>

### Type Changed: Android.Views.InputSourceType

Added value:

<pre style='color: green'>
	BluetoothStylus = 49154,
</pre>

### Type Changed: Android.Views.IViewParent

Added method:

<pre style='color: red'>
	public virtual ActionMode StartActionModeForChild (View originalView, ActionMode.ICallback callback, ActionModeType type);
</pre>

### Type Changed: Android.Views.Keycode

Added values:

<pre style='color: green'>
	MediaSkipBackward = 273,
	MediaSkipForward = 272,
	MediaStepBackward = 275,
	MediaStepForward = 274,
	NavigateIn = 262,
	NavigateNext = 261,
	NavigateOut = 263,
	NavigatePrevious = 260,
</pre>

### Type Changed: Android.Views.MotionEvent

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const MotionEventButtonState ButtonStylusPrimary;

	[Obsolete]
	public static const MotionEventButtonState ButtonStylusSecondary;
</pre>

Added property:

<pre style='color: green'>
	public MotionEventButtonState ActionButton { get; }
</pre>

### Type Changed: Android.Views.MotionEventActions

Added values:

<pre style='color: green'>
	ButtonPress = 11,
	ButtonRelease = 12,
</pre>

### Type Changed: Android.Views.MotionEventButtonState

Added values:

<pre style='color: green'>
	StylusPrimary = 32,
	StylusSecondary = 64,
</pre>

### Type Changed: Android.Views.ScaleGestureDetector

Added property:

<pre style='color: green'>
	public virtual bool StylusScaleEnabled { get; set; }
</pre>

### Type Changed: Android.Views.Surface

Added method:

<pre style='color: green'>
	public virtual Android.Graphics.Canvas LockHardwareCanvas ();
</pre>

### Type Changed: Android.Views.SystemUiFlags

Added value:

<pre style='color: green'>
	LightStatusBar = 8192,
</pre>

### Type Changed: Android.Views.TextDirection

Added values:

<pre style='color: green'>
	FirstStrongLtr = 6,
	FirstStrongRtl = 7,
</pre>

### Type Changed: Android.Views.View

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const SystemUiFlags SystemUiFlagLightStatusBar;

	[Obsolete]
	public static const TextDirection TextDirectionFirstStrongLtr;

	[Obsolete]
	public static const TextDirection TextDirectionFirstStrongRtl;
</pre>

Added properties:

<pre style='color: green'>
	public string AccessibilityClassName { get; }
	public virtual Java.Lang.ICharSequence AccessibilityClassNameFormatted { get; }
	public virtual bool ContextClickable { get; set; }
	public virtual Android.Graphics.Drawables.Drawable Foreground { get; set; }
	public virtual GravityFlags ForegroundGravity { get; }
	public virtual Android.Content.Res.ColorStateList ForegroundTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ForegroundTintMode { get; set; }
	public virtual WindowInsets RootWindowInsets { get; }
	public virtual ScrollIndicatorPosition ScrollIndicators { get; }
</pre>

Added events:

<pre style='color: green'>
	public event System.EventHandler&lt;View.ContextClickEventArgs&gt; ContextClick;
	public event System.EventHandler&lt;View.ScrollChangeEventArgs&gt; ScrollChange;
</pre>

Modified methods:

```
public virtual void AddChildrenForAccessibility (System.Collections.Generic.IList<View> children outChildren)
```

Added methods:

<pre style='color: green'>
	public virtual void DispatchProvideStructure (ViewStructure structure);
	public virtual bool GetClipBounds (Android.Graphics.Rect outRect);
	public virtual void OnDrawForeground (Android.Graphics.Canvas canvas);
	public virtual void OnProvideStructure (ViewStructure structure);
	public virtual void OnProvideVirtualStructure (ViewStructure structure);
	public virtual bool PerformContextClick ();
	public virtual void SetForegroundGravity (GravityFlags gravity);
	public virtual void SetOnContextClickListener (View.IOnContextClickListener l);
	public virtual void SetOnScrollChangeListener (View.IOnScrollChangeListener l);
	public virtual void SetScrollIndicators (int indicators, int mask);
	public virtual void SetScrollIndicators (int indicators);
	public virtual ActionMode StartActionMode (ActionMode.ICallback callback, ActionModeType type);
</pre>

### New Type Android.Views.IOnContextClickListener

<pre style='color: green'>
public interface IOnContextClickListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual bool OnContextClick (View v);
}
</pre>

### New Type Android.Views.ContextClickEventArgs

<pre style='color: green'>
public class ContextClickEventArgs : System.EventArgs {
	// constructors
	public View (bool handled, View v);
	// properties
	public bool Handled { get; set; }
	public View V { get; }
}
</pre>

### New Type Android.Views.IOnScrollChangeListener

<pre style='color: green'>
public interface IOnScrollChangeListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnScrollChange (View v, int scrollX, int scrollY, int oldScrollX, int oldScrollY);
}
</pre>

### New Type Android.Views.ScrollChangeEventArgs

<pre style='color: green'>
public class ScrollChangeEventArgs : System.EventArgs {
	// constructors
	public View (View v, int scrollX, int scrollY, int oldScrollX, int oldScrollY);
	// properties
	public int OldScrollX { get; }
	public int OldScrollY { get; }
	public int ScrollX { get; }
	public int ScrollY { get; }
	public View V { get; }
}
</pre>

### Type Changed: Android.Views.ViewConfiguration

Added property:

<pre style='color: green'>
	public static long DefaultActionModeHideDuration { get; }
</pre>

### Type Changed: Android.Views.ViewGroup

Obsoleted properties:

```
[Obsolete ()]
	public virtual bool AlwaysDrawnWithCacheEnabled { get; set; }
	[Obsolete ()]
	public virtual bool AnimationCacheEnabled { get; set; }
	[Obsolete ()]
	protected virtual bool ChildrenDrawnWithCacheEnabled { get; set; }
```

Added methods:

<pre style='color: green'>
	public virtual void OnViewAdded (View child);
	public virtual void OnViewRemoved (View child);
	public virtual ActionMode StartActionModeForChild (View originalView, ActionMode.ICallback callback, ActionModeType type);
</pre>

### Type Changed: Android.Views.Window

### Type Changed: Android.Views.Window.ICallback

Added methods:

<pre style='color: red'>
	public virtual bool OnSearchRequested (SearchEvent searchEvent);
	public virtual ActionMode OnWindowStartingActionMode (ActionMode.ICallback callback, ActionModeType type);
</pre>

### Type Changed: Android.Views.WindowManagerLayoutParams

Added property:

<pre style='color: green'>
	public int PreferredDisplayModeId { get; set; }
</pre>

### New Type Android.Views.ActionModeType

<pre style='color: green'>
[Serializable]
public enum ActionModeType {
	Floating = 1,
	Primary = 0,
}
</pre>

### New Type Android.Views.ScrollIndicatorPosition

<pre style='color: green'>
[Serializable]
public enum ScrollIndicatorPosition {
	Bottom = 2,
	End = 32,
	Left = 4,
	Right = 8,
	Start = 16,
	Top = 1,
}
</pre>

### New Type Android.Views.SearchEvent

<pre style='color: green'>
public class SearchEvent : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected SearchEvent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SearchEvent (InputDevice inputDevice);
	// properties
	public virtual InputDevice InputDevice { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Views.ViewStructure

<pre style='color: green'>
public abstract class ViewStructure : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ViewStructure (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ViewStructure ();
	// properties
	public virtual int ChildCount { get; set; }
	public virtual Android.OS.Bundle Extras { get; }
	public virtual bool HasExtras { get; }
	public string Hint { get; set; }
	public virtual Java.Lang.ICharSequence HintFormatted { get; set; }
	public string Text { get; set; }
	public virtual Java.Lang.ICharSequence TextFormatted { get; set; }
	public virtual int TextSelectionEnd { get; }
	public virtual int TextSelectionStart { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int AddChildCount (int num);
	public virtual void AsyncCommit ();
	public virtual ViewStructure AsyncNewChild (int index);
	public virtual ViewStructure NewChild (int index);
	public virtual void SetAccessibilityFocused (bool state);
	public virtual void SetActivated (bool state);
	public virtual void SetAlpha (float alpha);
	public virtual void SetCheckable (bool state);
	public virtual void SetChecked (bool state);
	public virtual void SetClassName (string className);
	public virtual void SetClickable (bool state);
	public virtual void SetContentDescription (Java.Lang.ICharSequence contentDescription);
	public void SetContentDescription (string contentDescription);
	public virtual void SetContextClickable (bool state);
	public virtual void SetDimens (int left, int top, int scrollX, int scrollY, int width, int height);
	public virtual void SetElevation (float elevation);
	public virtual void SetEnabled (bool state);
	public virtual void SetFocusable (bool state);
	public virtual void SetFocused (bool state);
	public virtual void SetId (int id, string packageName, string typeName, string entryName);
	public virtual void SetLongClickable (bool state);
	public virtual void SetSelected (bool state);
	public void SetText (string text, int selectionStart, int selectionEnd);
	public virtual void SetText (Java.Lang.ICharSequence text, int selectionStart, int selectionEnd);
	public virtual void SetTextLines (int[] charOffsets, int[] baselines);
	public virtual void SetTextStyle (float size, int fgColor, int bgColor, Android.App.Assist.AssistTextStyle style);
	public virtual void SetTransformation (Android.Graphics.Matrix matrix);
	public virtual void SetVisibility (ViewStates visibility);
}
</pre>

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo

Added fields:

<pre style='color: green'>
	public static const string ActionArgumentColumnInt = "android.view.accessibility.action.ARGUMENT_COLUMN_INT";
	public static const string ActionArgumentRowInt = "android.view.accessibility.action.ARGUMENT_ROW_INT";
</pre>

Added property:

<pre style='color: green'>
	public virtual bool ContextClickable { get; set; }
</pre>

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo.AccessibilityAction

Added properties:

<pre style='color: green'>
	public static AccessibilityNodeInfo.AccessibilityAction ActionContextClick { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollDown { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollLeft { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollRight { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollToPosition { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollUp { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionShowOnScreen { get; }
</pre>

### Type Changed: Android.Views.Accessibility.EventTypes

Added values:

<pre style='color: green'>
	AssistReadingContext = 16777216,
	ViewContextClicked = 8388608,
</pre>

## Namespace Android.Webkit

### Type Changed: Android.Webkit.PermissionRequest

Added field:

<pre style='color: green'>
	public static const string ResourceMidiSysex = "android.webkit.resource.MIDI_SYSEX";
</pre>

### Type Changed: Android.Webkit.WebSettings

Added property:

<pre style='color: green'>
	public virtual bool OffscreenPreRaster { get; set; }
</pre>

### Type Changed: Android.Webkit.WebView

Obsoleted methods:

```
[Obsolete ()]
	public virtual bool OverlayHorizontalScrollbar ();
	[Obsolete ()]
	public virtual bool OverlayVerticalScrollbar ();
	[Obsolete ()]
	public virtual void SetHorizontalScrollbarOverlay (bool overlay);
	[Obsolete ()]
	public virtual void SetVerticalScrollbarOverlay (bool overlay);
```

Added methods:

<pre style='color: green'>
	public virtual WebMessagePort[] CreateWebMessageChannel ();
	public virtual void PostVisualStateCallback (long requestId, WebView.VisualStateCallback callback);
	public virtual void PostWebMessage (WebMessage message, Android.Net.Uri targetOrigin);
</pre>

### New Type Android.Webkit.VisualStateCallback

<pre style='color: green'>
public abstract class VisualStateCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WebView (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WebView ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnComplete (long requestId);
}
</pre>

### Type Changed: Android.Webkit.WebViewClient

Obsoleted methods:

```
[Obsolete ()]
	public virtual void OnReceivedError (WebView view, ClientError errorCode, string description, string failingUrl);
```

Added methods:

<pre style='color: green'>
	public virtual void OnPageCommitVisible (WebView view, string url);
	public virtual void OnReceivedError (WebView view, IWebResourceRequest request, WebResourceError error);
	public virtual void OnReceivedHttpError (WebView view, IWebResourceRequest request, WebResourceResponse errorResponse);
</pre>

### New Type Android.Webkit.WebMessage

<pre style='color: green'>
public class WebMessage : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WebMessage (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WebMessage (string data);
	public WebMessage (string data, WebMessagePort[] ports);
	// properties
	public virtual string Data { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual WebMessagePort[] GetPorts ();
}
</pre>

### New Type Android.Webkit.WebMessagePort

<pre style='color: green'>
public abstract class WebMessagePort : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WebMessagePort (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Close ();
	public virtual void PostMessage (WebMessage message);
	public virtual void SetWebMessageCallback (WebMessagePort.WebMessageCallback callback);
	public virtual void SetWebMessageCallback (WebMessagePort.WebMessageCallback callback, Android.OS.Handler handler);

	// inner types
	public abstract class WebMessageCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected WebMessagePort (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public WebMessagePort ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnMessage (WebMessagePort port, WebMessage message);
	}
}
</pre>

### New Type Android.Webkit.WebResourceError

<pre style='color: green'>
public abstract class WebResourceError : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WebResourceError (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public string Description { get; }
	public virtual Java.Lang.ICharSequence DescriptionFormatted { get; }
	public virtual ClientError ErrorCode { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

## Namespace Android.Widget

### Type Changed: Android.Widget.ActionMenuView

Added property:

<pre style='color: green'>
	public virtual Android.Graphics.Drawables.Drawable OverflowIcon { get; set; }
</pre>

### Type Changed: Android.Widget.ArrayAdapter

Added interface:

<pre style='color: green'>
	IThemedSpinnerAdapter
</pre>

Added property:

<pre style='color: green'>
	public virtual Android.Content.Res.Resources.Theme DropDownViewTheme { get; set; }
</pre>

### Type Changed: Android.Widget.ArrayAdapter`1

Added interface:

<pre style='color: green'>
	IThemedSpinnerAdapter
</pre>

### Type Changed: Android.Widget.CalendarView

Obsoleted properties:

```
[Obsolete ()]
	public virtual Android.Graphics.Color FocusedMonthDateColor { get; set; }
	[Obsolete ()]
	public virtual Android.Graphics.Drawables.Drawable SelectedDateVerticalBar { get; set; }
	[Obsolete ()]
	public virtual Android.Graphics.Color SelectedWeekBackgroundColor { get; set; }
	[Obsolete ()]
	public virtual int ShownWeekCount { get; set; }
	[Obsolete ()]
	public virtual Android.Graphics.Color UnfocusedMonthDateColor { get; set; }
	[Obsolete ()]
	public virtual Android.Graphics.Color WeekNumberColor { get; set; }
	[Obsolete ()]
	public virtual Android.Graphics.Color WeekSeparatorLineColor { get; set; }
```

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetSelectedDateVerticalBar (int resourceId);
```

### Type Changed: Android.Widget.CheckedTextView

Modified methods:

```
public virtual void SetCheckMarkDrawable (int resid resId)
```

### Type Changed: Android.Widget.CompoundButton

Added property:

<pre style='color: green'>
	public virtual Android.Graphics.Drawables.Drawable ButtonDrawable { get; }
</pre>

Modified methods:

```
public virtual void SetButtonDrawable (Android.Graphics.Drawables.Drawable d drawable)
	public virtual void SetButtonDrawable (int resid resId)
```

### Type Changed: Android.Widget.CursorAdapter

Added interface:

<pre style='color: green'>
	IThemedSpinnerAdapter
</pre>

Added property:

<pre style='color: green'>
	public virtual Android.Content.Res.Resources.Theme DropDownViewTheme { get; set; }
</pre>

### Type Changed: Android.Widget.FrameLayout

Modified properties:

```
public virtual override Android.Graphics.Drawables.Drawable Foreground { get; set; }
	public virtual override Android.Views.GravityFlags ForegroundGravity { get; }
	public virtual override Android.Content.Res.ColorStateList ForegroundTintList { get; set; }
	public virtual override Android.Graphics.PorterDuff.Mode ForegroundTintMode { get; set; }
```

Modified methods:

```
public virtual override void SetForegroundGravity (Android.Views.GravityFlags foregroundGravity)
```

### Type Changed: Android.Widget.ImageView

Added method:

<pre style='color: green'>
	public virtual void SetImageIcon (Android.Graphics.Drawables.Icon icon);
</pre>

### Type Changed: Android.Widget.ListPopupWindow

Added method:

<pre style='color: green'>
	public virtual void SetWindowLayoutType (Android.Views.WindowManagerTypes layoutType);
</pre>

### Type Changed: Android.Widget.PopupMenu

Added property:

<pre style='color: green'>
	public virtual Android.Views.GravityFlags Gravity { get; set; }
</pre>

### Type Changed: Android.Widget.PopupWindow

Added properties:

<pre style='color: green'>
	public virtual bool OverlapAnchor { get; set; }
	public virtual Android.Views.WindowManagerTypes WindowLayoutType { get; set; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetWindowLayoutMode (int widthSpec, int heightSpec);
```

Added methods:

<pre style='color: green'>
	public virtual void SetEnterTransition (Android.Transitions.Transition enterTransition);
	public virtual void SetExitTransition (Android.Transitions.Transition exitTransition);
</pre>

### Type Changed: Android.Widget.QuickContactBadge

Added method:

<pre style='color: green'>
	public virtual void SetPrioritizedMimeType (string prioritizedMimeType);
</pre>

### Type Changed: Android.Widget.RelativeLayout

### Type Changed: Android.Widget.RelativeLayout.LayoutParams

Added method:

<pre style='color: green'>
	public virtual int GetRule (LayoutRules verb);
</pre>

### Type Changed: Android.Widget.RemoteViews

Added methods:

<pre style='color: green'>
	public virtual void SetIcon (int viewId, string methodName, Android.Graphics.Drawables.Icon value);
	public virtual void SetImageViewIcon (int viewId, Android.Graphics.Drawables.Icon icon);
</pre>

### Type Changed: Android.Widget.ResourceCursorAdapter

Added interface:

<pre style='color: green'>
	IThemedSpinnerAdapter
</pre>

### Type Changed: Android.Widget.SimpleAdapter

Added interface:

<pre style='color: green'>
	IThemedSpinnerAdapter
</pre>

Added property:

<pre style='color: green'>
	public virtual Android.Content.Res.Resources.Theme DropDownViewTheme { get; set; }
</pre>

### Type Changed: Android.Widget.SimpleCursorAdapter

Added interface:

<pre style='color: green'>
	IThemedSpinnerAdapter
</pre>

### Type Changed: Android.Widget.Spinner

Added constructor:

<pre style='color: green'>
	public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes, SpinnerMode mode, Android.Content.Res.Resources.Theme popupTheme);
</pre>

Added property:

<pre style='color: green'>
	public virtual Android.Content.Context PopupContext { get; }
</pre>

### Type Changed: Android.Widget.Switch

Added properties:

<pre style='color: green'>
	public virtual Android.Content.Res.ColorStateList ThumbTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ThumbTintMode { get; set; }
	public virtual Android.Content.Res.ColorStateList TrackTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode TrackTintMode { get; set; }
</pre>

### Type Changed: Android.Widget.TextView

Added properties:

<pre style='color: green'>
	public virtual Android.Text.BreakStrategy BreakStrategy { get; set; }
	public virtual Android.Content.Res.ColorStateList CompoundDrawableTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode CompoundDrawableTintMode { get; set; }
	public virtual Android.Views.ActionMode.ICallback CustomInsertionActionModeCallback { get; set; }
	public virtual Android.Text.HyphenationFrequency HyphenationFrequency { get; set; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetTextAppearance (Android.Content.Context context, int resId);
```

Modified methods:

```
public virtual void SetTextAppearance (Android.Content.Context context, int resid resId)
```

Added method:

<pre style='color: green'>
	public virtual void SetTextAppearance (int resId);
</pre>

### Type Changed: Android.Widget.TimePicker

Obsoleted properties:

```
[Obsolete ()]
	public virtual Java.Lang.Integer CurrentHour { get; set; }
	[Obsolete ()]
	public virtual Java.Lang.Integer CurrentMinute { get; set; }
```

Added properties:

<pre style='color: green'>
	public virtual int Hour { get; set; }
	public virtual int Minute { get; set; }
</pre>

### Type Changed: Android.Widget.Toolbar

Added property:

<pre style='color: green'>
	public virtual Android.Graphics.Drawables.Drawable OverflowIcon { get; set; }
</pre>

### New Type Android.Widget.IThemedSpinnerAdapter

<pre style='color: green'>
public interface IThemedSpinnerAdapter : ISpinnerAdapter, IAdapter, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual Android.Content.Res.Resources.Theme DropDownViewTheme { get; set; }
}
</pre>

## Namespace Java.Lang

### Type Changed: Java.Lang.StrictMath

Modified methods:

```
public double Acos (double d x)
	public double Asin (double d x)
	public double Atan (double d x)
	public double Cbrt (double d x)
	public double Cosh (double d x)
	public double Exp (double d x)
	public double Expm1 (double d x)
	public double Log (double d x)
	public double Log10 (double d x)
	public double Log1p (double d x)
	public double Sinh (double d x)
	public double Tanh (double d x)
```

## New Namespace Android.App.Assist

### New Type Android.App.Assist.AssistContent

<pre style='color: green'>
public class AssistContent : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AssistContent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AssistContent ();
	// properties
	public virtual Android.Content.ClipData ClipData { get; set; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual Android.OS.Bundle Extras { get; }
	public virtual Android.Content.Intent Intent { get; set; }
	public virtual bool IsAppProvidedIntent { get; }
	public virtual string StructuredData { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual Android.Net.Uri WebUri { get; set; }
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

### New Type Android.App.Assist.AssistStructure

<pre style='color: green'>
public class AssistStructure : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AssistStructure (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AssistStructure ();
	// properties
	public virtual Android.Content.ComponentName ActivityComponent { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual int WindowNodeCount { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual AssistStructure.WindowNode GetWindowNodeAt (int index);
	public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public class ViewNode : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected AssistStructure (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// fields
		public static const int TextColorUndefined;
		// properties
		public virtual float Alpha { get; }
		public virtual int ChildCount { get; }
		public virtual string ClassName { get; }
		public string ContentDescription { get; }
		public virtual Java.Lang.ICharSequence ContentDescriptionFormatted { get; }
		public virtual float Elevation { get; }
		public virtual Android.OS.Bundle Extras { get; }
		public virtual int Height { get; }
		public virtual string Hint { get; }
		public virtual int Id { get; }
		public virtual string IdEntry { get; }
		public virtual string IdPackage { get; }
		public virtual string IdType { get; }
		public virtual bool IsAccessibilityFocused { get; }
		public virtual bool IsActivated { get; }
		public virtual bool IsAssistBlocked { get; }
		public virtual bool IsCheckable { get; }
		public virtual bool IsChecked { get; }
		public virtual bool IsClickable { get; }
		public virtual bool IsContextClickable { get; }
		public virtual bool IsEnabled { get; }
		public virtual bool IsFocusable { get; }
		public virtual bool IsFocused { get; }
		public virtual bool IsLongClickable { get; }
		public virtual bool IsSelected { get; }
		public virtual int Left { get; }
		public virtual int ScrollX { get; }
		public virtual int ScrollY { get; }
		public string Text { get; }
		public virtual int TextBackgroundColor { get; }
		public virtual int TextColor { get; }
		public virtual Java.Lang.ICharSequence TextFormatted { get; }
		public virtual int TextSelectionEnd { get; }
		public virtual int TextSelectionStart { get; }
		public virtual float TextSize { get; }
		public virtual AssistTextStyle TextStyle { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public virtual int Top { get; }
		public virtual Android.Graphics.Matrix Transformation { get; }
		public virtual Android.Views.ViewStates Visibility { get; }
		public virtual int Width { get; }
		// methods
		public virtual AssistStructure.ViewNode GetChildAt (int index);
		public virtual int[] GetTextLineBaselines ();
		public virtual int[] GetTextLineCharOffsets ();
	}
	public class WindowNode : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected AssistStructure (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		public virtual int DisplayId { get; }
		public virtual int Height { get; }
		public virtual int Left { get; }
		public virtual AssistStructure.ViewNode RootViewNode { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public string Title { get; }
		public virtual Java.Lang.ICharSequence TitleFormatted { get; }
		public virtual int Top { get; }
		public virtual int Width { get; }
	}
}
</pre>

### New Type Android.App.Assist.AssistTextStyle

<pre style='color: green'>
[Serializable]
public enum AssistTextStyle {
	Bold = 1,
	Italic = 2,
	StrikeThru = 8,
	Underline = 4,
}
</pre>

## New Namespace Android.Media.Midi

### New Type Android.Media.Midi.MidiDevice

<pre style='color: green'>
public sealed class MidiDevice : Java.Lang.Object, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public MidiDeviceInfo Info { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Close ();
	public MidiDevice.MidiConnection ConnectPorts (MidiInputPort inputPort, int outputPortNumber);
	public MidiInputPort OpenInputPort (int portNumber);
	public MidiOutputPort OpenOutputPort (int portNumber);

	// inner types
	public class MidiConnection : Java.Lang.Object, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		protected MidiDevice (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void Close ();
	}
}
</pre>

### New Type Android.Media.Midi.MidiDeviceInfo

<pre style='color: green'>
public sealed class MidiDeviceInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields
	public static const string PropertyBluetoothDevice = "bluetooth_device";
	public static const string PropertyManufacturer = "manufacturer";
	public static const string PropertyName = "name";
	public static const string PropertyProduct = "product";
	public static const string PropertySerialNumber = "serial_number";
	public static const string PropertyUsbDevice = "usb_device";
	public static const string PropertyVersion = "version";
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public int Id { get; }
	public int InputPortCount { get; }
	public bool IsPrivate { get; }
	public int OutputPortCount { get; }
	public Android.OS.Bundle Properties { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public MidiDeviceType Type { get; }
	// methods
	public virtual int DescribeContents ();
	public MidiDeviceInfo.PortInfo[] GetPorts ();
	public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class PortInfo : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// properties
		public string Name { get; }
		public int PortNumber { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public MidiPortType Type { get; }
	}
}
</pre>

### New Type Android.Media.Midi.MidiDeviceService

<pre style='color: green'>
public abstract class MidiDeviceService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected MidiDeviceService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MidiDeviceService ();
	// fields
	public static const string ServiceInterface = "android.media.midi.MidiDeviceService";
	// properties
	public MidiDeviceInfo DeviceInfo { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public MidiReceiver[] GetOutputPortReceivers ();
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual void OnClose ();
	public virtual void OnDeviceStatusChanged (MidiDeviceStatus status);
	public virtual MidiReceiver[] OnGetInputPortReceivers ();
}
</pre>

### New Type Android.Media.Midi.MidiDeviceStatus

<pre style='color: green'>
public sealed class MidiDeviceStatus : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public MidiDeviceInfo DeviceInfo { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public int GetOutputPortOpenCount (int portNumber);
	public bool IsInputPortOpen (int portNumber);
	public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Media.Midi.MidiDeviceType

<pre style='color: green'>
[Serializable]
public enum MidiDeviceType {
	Bluetooth = 3,
	Usb = 1,
	Virtual = 2,
}
</pre>

### New Type Android.Media.Midi.MidiInputPort

<pre style='color: green'>
public sealed class MidiInputPort : Android.Media.Midi.MidiReceiver, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public int PortNumber { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Close ();
	public override void OnSend (byte[] msg, int offset, int count, long timestamp);
}
</pre>

### New Type Android.Media.Midi.MidiManager

<pre style='color: green'>
public sealed class MidiManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public MidiDeviceInfo[] GetDevices ();
	public void OpenBluetoothDevice (Android.Bluetooth.BluetoothDevice bluetoothDevice, MidiManager.IOnDeviceOpenedListener listener, Android.OS.Handler handler);
	public void OpenDevice (MidiDeviceInfo deviceInfo, MidiManager.IOnDeviceOpenedListener listener, Android.OS.Handler handler);
	public void RegisterDeviceCallback (MidiManager.DeviceCallback callback, Android.OS.Handler handler);
	public void UnregisterDeviceCallback (MidiManager.DeviceCallback callback);

	// inner types
	public class DeviceCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MidiManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MidiManager ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnDeviceAdded (MidiDeviceInfo device);
		public virtual void OnDeviceRemoved (MidiDeviceInfo device);
		public virtual void OnDeviceStatusChanged (MidiDeviceStatus status);
	}
	public interface IOnDeviceOpenedListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual void OnDeviceOpened (MidiDevice device);
	}
	public class DeviceOpenedEventArgs : System.EventArgs {
		// constructors
		public MidiManager (MidiDevice device);
		// properties
		public MidiDevice Device { get; }
	}
}
</pre>

### New Type Android.Media.Midi.MidiOutputPort

<pre style='color: green'>
public sealed class MidiOutputPort : Android.Media.Midi.MidiSender, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public int PortNumber { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Close ();
	public override void OnConnect (MidiReceiver receiver);
	public override void OnDisconnect (MidiReceiver receiver);
}
</pre>

### New Type Android.Media.Midi.MidiPortType

<pre style='color: green'>
[Serializable]
public enum MidiPortType {
	Input = 1,
	Output = 2,
}
</pre>

### New Type Android.Media.Midi.MidiReceiver

<pre style='color: green'>
public abstract class MidiReceiver : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected MidiReceiver (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MidiReceiver ();
	public MidiReceiver (int maxMessageSize);
	// properties
	public int MaxMessageSize { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Flush ();
	public virtual void OnFlush ();
	public virtual void OnSend (byte[] msg, int offset, int count, long timestamp);
	public virtual void Send (byte[] msg, int offset, int count);
	public virtual void Send (byte[] msg, int offset, int count, long timestamp);
}
</pre>

### New Type Android.Media.Midi.MidiSender

<pre style='color: green'>
public abstract class MidiSender : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected MidiSender (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MidiSender ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Connect (MidiReceiver receiver);
	public virtual void Disconnect (MidiReceiver receiver);
	public virtual void OnConnect (MidiReceiver receiver);
	public virtual void OnDisconnect (MidiReceiver receiver);
}
</pre>

## New Namespace Android.Security.Keystore

### New Type Android.Security.Keystore.KeyExpiredException

<pre style='color: green'>
public class KeyExpiredException : Java.Security.InvalidKeyException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected KeyExpiredException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public KeyExpiredException ();
	public KeyExpiredException (string message);
	public KeyExpiredException (string message, Java.Lang.Throwable cause);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Security.Keystore.KeyGenParameterSpec

<pre style='color: green'>
public sealed class KeyGenParameterSpec : Java.Lang.Object, Java.Security.Spec.IAlgorithmParameterSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public Java.Security.Spec.IAlgorithmParameterSpec AlgorithmParameterSpec { get; }
	public Java.Util.Date CertificateNotAfter { get; }
	public Java.Util.Date CertificateNotBefore { get; }
	public Java.Math.BigInteger CertificateSerialNumber { get; }
	public Javax.Security.Auth.X500.X500Principal CertificateSubject { get; }
	public bool IsDigestsSpecified { get; }
	public bool IsRandomizedEncryptionRequired { get; }
	public bool IsUserAuthenticationRequired { get; }
	public int KeySize { get; }
	public string KeystoreAlias { get; }
	public Java.Util.Date KeyValidityForConsumptionEnd { get; }
	public Java.Util.Date KeyValidityForOriginationEnd { get; }
	public Java.Util.Date KeyValidityStart { get; }
	public KeyStorePurpose Purposes { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int UserAuthenticationValidityDurationSeconds { get; }
	// methods
	public string[] GetBlockModes ();
	public string[] GetDigests ();
	public string[] GetEncryptionPaddings ();
	public string[] GetSignaturePaddings ();

	// inner types
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public KeyGenParameterSpec (string keystoreAlias, KeyStorePurpose purposes);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public KeyGenParameterSpec Build ();
		public KeyGenParameterSpec.Builder SetAlgorithmParameterSpec (Java.Security.Spec.IAlgorithmParameterSpec spec);
		public KeyGenParameterSpec.Builder SetBlockModes (string[] blockModes);
		public KeyGenParameterSpec.Builder SetCertificateNotAfter (Java.Util.Date date);
		public KeyGenParameterSpec.Builder SetCertificateNotBefore (Java.Util.Date date);
		public KeyGenParameterSpec.Builder SetCertificateSerialNumber (Java.Math.BigInteger serialNumber);
		public KeyGenParameterSpec.Builder SetCertificateSubject (Javax.Security.Auth.X500.X500Principal subject);
		public KeyGenParameterSpec.Builder SetDigests (string[] digests);
		public KeyGenParameterSpec.Builder SetEncryptionPaddings (string[] paddings);
		public KeyGenParameterSpec.Builder SetKeySize (int keySize);
		public KeyGenParameterSpec.Builder SetKeyValidityEnd (Java.Util.Date endDate);
		public KeyGenParameterSpec.Builder SetKeyValidityForConsumptionEnd (Java.Util.Date endDate);
		public KeyGenParameterSpec.Builder SetKeyValidityForOriginationEnd (Java.Util.Date endDate);
		public KeyGenParameterSpec.Builder SetKeyValidityStart (Java.Util.Date startDate);
		public KeyGenParameterSpec.Builder SetRandomizedEncryptionRequired (bool required);
		public KeyGenParameterSpec.Builder SetSignaturePaddings (string[] paddings);
		public KeyGenParameterSpec.Builder SetUserAuthenticationRequired (bool required);
		public KeyGenParameterSpec.Builder SetUserAuthenticationValidityDurationSeconds (int seconds);
	}
}
</pre>

### New Type Android.Security.Keystore.KeyInfo

<pre style='color: green'>
public class KeyInfo : Java.Lang.Object, Java.Security.Spec.IKeySpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected KeyInfo (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual bool IsInsideSecureHardware { get; }
	public virtual bool IsUserAuthenticationRequired { get; }
	public virtual bool IsUserAuthenticationRequirementEnforcedBySecureHardware { get; }
	public virtual int KeySize { get; }
	public virtual string KeystoreAlias { get; }
	public virtual Java.Util.Date KeyValidityForConsumptionEnd { get; }
	public virtual Java.Util.Date KeyValidityForOriginationEnd { get; }
	public virtual Java.Util.Date KeyValidityStart { get; }
	public virtual KeyStorePurpose Purposes { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual int UserAuthenticationValidityDurationSeconds { get; }
	// methods
	public virtual string[] GetBlockModes ();
	public virtual string[] GetDigests ();
	public virtual string[] GetEncryptionPaddings ();
	public virtual string[] GetSignaturePaddings ();
}
</pre>

### New Type Android.Security.Keystore.KeyNotYetValidException

<pre style='color: green'>
public class KeyNotYetValidException : Java.Security.InvalidKeyException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected KeyNotYetValidException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public KeyNotYetValidException ();
	public KeyNotYetValidException (string message);
	public KeyNotYetValidException (string message, Java.Lang.Throwable cause);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Security.Keystore.KeyPermanentlyInvalidatedException

<pre style='color: green'>
public class KeyPermanentlyInvalidatedException : Java.Security.InvalidKeyException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected KeyPermanentlyInvalidatedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public KeyPermanentlyInvalidatedException ();
	public KeyPermanentlyInvalidatedException (string message);
	public KeyPermanentlyInvalidatedException (string message, Java.Lang.Throwable cause);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Security.Keystore.KeyProperties

<pre style='color: green'>
public abstract class KeyProperties : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected KeyProperties (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const string BlockModeCbc = "CBC";
	public static const string BlockModeCtr = "CTR";
	public static const string BlockModeEcb = "ECB";
	public static const string BlockModeGcm = "GCM";
	public static const string DigestMd5 = "MD5";
	public static const string DigestNone = "NONE";
	public static const string DigestSha1 = "SHA-1";
	public static const string DigestSha224 = "SHA-224";
	public static const string DigestSha256 = "SHA-256";
	public static const string DigestSha384 = "SHA-384";
	public static const string DigestSha512 = "SHA-512";
	public static const string EncryptionPaddingNone = "NoPadding";
	public static const string EncryptionPaddingPkcs7 = "PKCS7Padding";
	public static const string EncryptionPaddingRsaOaep = "OAEPPadding";
	public static const string EncryptionPaddingRsaPkcs1 = "PKCS1Padding";
	public static const string KeyAlgorithmAes = "AES";
	public static const string KeyAlgorithmEc = "EC";
	public static const string KeyAlgorithmHmacSha1 = "HmacSHA1";
	public static const string KeyAlgorithmHmacSha224 = "HmacSHA224";
	public static const string KeyAlgorithmHmacSha256 = "HmacSHA256";
	public static const string KeyAlgorithmHmacSha384 = "HmacSHA384";
	public static const string KeyAlgorithmHmacSha512 = "HmacSHA512";
	public static const string KeyAlgorithmRsa = "RSA";
	public static const string SignaturePaddingRsaPkcs1 = "PKCS1";
	public static const string SignaturePaddingRsaPss = "PSS";
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Security.Keystore.KeyProtection

<pre style='color: green'>
public sealed class KeyProtection : Java.Lang.Object, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public bool IsDigestsSpecified { get; }
	public bool IsRandomizedEncryptionRequired { get; }
	public bool IsUserAuthenticationRequired { get; }
	public Java.Util.Date KeyValidityForConsumptionEnd { get; }
	public Java.Util.Date KeyValidityForOriginationEnd { get; }
	public Java.Util.Date KeyValidityStart { get; }
	public KeyStorePurpose Purposes { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int UserAuthenticationValidityDurationSeconds { get; }
	// methods
	public string[] GetBlockModes ();
	public string[] GetDigests ();
	public string[] GetEncryptionPaddings ();
	public string[] GetSignaturePaddings ();

	// inner types
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public KeyProtection (KeyStorePurpose purposes);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public KeyProtection Build ();
		public KeyProtection.Builder SetBlockModes (string[] blockModes);
		public KeyProtection.Builder SetDigests (string[] digests);
		public KeyProtection.Builder SetEncryptionPaddings (string[] paddings);
		public KeyProtection.Builder SetKeyValidityEnd (Java.Util.Date endDate);
		public KeyProtection.Builder SetKeyValidityForConsumptionEnd (Java.Util.Date endDate);
		public KeyProtection.Builder SetKeyValidityForOriginationEnd (Java.Util.Date endDate);
		public KeyProtection.Builder SetKeyValidityStart (Java.Util.Date startDate);
		public KeyProtection.Builder SetRandomizedEncryptionRequired (bool required);
		public KeyProtection.Builder SetSignaturePaddings (string[] paddings);
		public KeyProtection.Builder SetUserAuthenticationRequired (bool required);
		public KeyProtection.Builder SetUserAuthenticationValidityDurationSeconds (int seconds);
	}
}
</pre>

### New Type Android.Security.Keystore.KeyStoreOrigin

<pre style='color: green'>
[Serializable]
public enum KeyStoreOrigin {
	Generated = 1,
	Imported = 2,
	Unknown = 4,
}
</pre>

### New Type Android.Security.Keystore.KeyStorePurpose

<pre style='color: green'>
[Serializable]
public enum KeyStorePurpose {
	Decrypt = 2,
	Encrypt = 1,
	Sign = 4,
	Verify = 8,
}
</pre>

### New Type Android.Security.Keystore.UserNotAuthenticatedException

<pre style='color: green'>
public class UserNotAuthenticatedException : Java.Security.InvalidKeyException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected UserNotAuthenticatedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public UserNotAuthenticatedException ();
	public UserNotAuthenticatedException (string message);
	public UserNotAuthenticatedException (string message, Java.Lang.Throwable cause);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

## New Namespace Android.Service.Chooser

### New Type Android.Service.Chooser.ChooserTarget

<pre style='color: green'>
public sealed class ChooserTarget : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public ChooserTarget (Java.Lang.ICharSequence title, Android.Graphics.Drawables.Icon icon, float score, Android.Content.ComponentName componentName, Android.OS.Bundle intentExtras);
	public ChooserTarget (string title, Android.Graphics.Drawables.Icon icon, float score, Android.Content.ComponentName componentName, Android.OS.Bundle intentExtras);
	// properties
	public Android.Content.ComponentName ComponentName { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public Android.Graphics.Drawables.Icon Icon { get; }
	public Android.OS.Bundle IntentExtras { get; }
	public float Score { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public string Title { get; }
	public Java.Lang.ICharSequence TitleFormatted { get; }
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

### New Type Android.Service.Chooser.ChooserTargetService

<pre style='color: green'>
public abstract class ChooserTargetService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ChooserTargetService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ChooserTargetService ();
	// fields
	public static const string BindPermission = "android.permission.BIND_CHOOSER_TARGET_SERVICE";
	public static const string MetaDataName = "android.service.chooser.chooser_target_service";
	public static const string ServiceInterface = "android.service.chooser.ChooserTargetService";
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual System.Collections.Generic.IList&lt;ChooserTarget&gt; OnGetChooserTargets (Android.Content.ComponentName targetActivityName, Android.Content.IntentFilter matchedFilter);
}
</pre>
