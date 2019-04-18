---
id: CF1CC9C3-1F47-4A0D-8ECE-B7343DBE3559
---

## Namespace Android

### Type Changed: Android.Manifest

### Type Changed: Android.Manifest.Permission

Added fields:

<pre style='color: green'>
	public static const string BindCarrierConfigService = "android.permission.BIND_CARRIER_CONFIG_SERVICE";
	public static const string BindChooserTargetService = "android.permission.BIND_CHOOSER_TARGET_SERVICE";
	public static const string BindIncallService = "android.permission.BIND_INCALL_SERVICE";
	public static const string BindTelecomConnectionService = "android.permission.BIND_TELECOM_CONNECTION_SERVICE";
	public static const string PackageUsageStats = "android.permission.PACKAGE_USAGE_STATS";
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
[Obsolete (]
	public static const int AmPmBackgroundColor;
	[Obsolete (]
	public static const int AmPmTextColor;
	[Obsolete (]
	public static const int DayOfWeekBackground;
	[Obsolete (]
	public static const int DayOfWeekTextAppearance;
	[Obsolete (]
	public static const int DirectionDescriptions;
	[Obsolete (]
	public static const int FocusedMonthDateColor;
	[Obsolete (]
	public static const int HeaderAmPmTextAppearance;
	[Obsolete (]
	public static const int HeaderDayOfMonthTextAppearance;
	[Obsolete (]
	public static const int HeaderMonthTextAppearance;
	[Obsolete (]
	public static const int HeaderTimeTextAppearance;
	[Obsolete (]
	public static const int HeaderYearTextAppearance;
	[Obsolete (]
	public static const int SelectedDateVerticalBar;
	[Obsolete (]
	public static const int SelectedWeekBackgroundColor;
	[Obsolete (]
	public static const int ShownWeekCount;
	[Obsolete (]
	public static const int ShowOnLockScreen;
	[Obsolete (]
	public static const int ShowWeekNumber;
	[Obsolete (]
	public static const int TargetDescriptions;
	[Obsolete (]
	public static const int UnfocusedMonthDateColor;
	[Obsolete (]
	public static const int WeekNumberColor;
	[Obsolete (]
	public static const int WeekSeparatorLineColor;
	[Obsolete (]
	public static const int YearListItemTextAppearance;
	[Obsolete (]
	public static const int YearListSelectorColor;
```

Added fields:

<pre style='color: green'>
	public static const int AllowUndo;
	public static const int AutoVerify;
	public static const int BreakStrategy;
	public static const int ColorBackgroundFloating;
	public static const int DrawableTint;
	public static const int DrawableTintMode;
	public static const int DynamicResources;
	public static const int End;
	public static const int ExtractNativeLibs;
	public static const int Fraction;
	public static const int FullBackupContent;
	public static const int HyphenationFrequency;
	public static const int IconTint;
	public static const int IconTintMode;
	public static const int LeftIndents;
	public static const int LockTaskMode;
	public static const int NavigationTint;
	public static const int NavigationTintMode;
	public static const int NumbersInnerTextColor;
	public static const int OverflowTint;
	public static const int OverflowTintMode;
	public static const int RemoveBeforeMRelease;
	public static const int Reserved0;
	public static const int RightIndents;
	public static const int ScrollIndicators;
	public static const int ShowForAllUsers;
	public static const int Start;
	public static const int StylusButtonPressable;
	public static const int SupportsAssist;
	public static const int SupportsLaunchVoiceAssistFromKeyguard;
	public static const int ThumbPosition;
	public static const int TrackTint;
	public static const int TrackTintMode;
	public static const int UsesCleartextTraffic;
	public static const int WindowLightStatusBar;
</pre>

### Type Changed: Android.Resource.Id

Added fields:

<pre style='color: green'>
	public static const int AccessibilityActionScrollDown;
	public static const int AccessibilityActionScrollLeft;
	public static const int AccessibilityActionScrollRight;
	public static const int AccessibilityActionScrollToPosition;
	public static const int AccessibilityActionScrollUp;
	public static const int AccessibilityActionShowOnScreen;
	public static const int AccessibilityActionStylusButtonPress;
	public static const int PasteAsPlainText;
	public static const int Redo;
	public static const int ReplaceText;
	public static const int ShareText;
	public static const int Undo;
</pre>

### Type Changed: Android.Resource.Style

Added fields:

<pre style='color: green'>
	public static const int TextAppearanceMaterialWidgetButtonInverse;
	public static const int ThemeMaterialDayNight;
	public static const int ThemeMaterialDayNightDarkActionBar;
	public static const int ThemeMaterialDayNightDialog;
	public static const int ThemeMaterialDayNightDialogAlert;
	public static const int ThemeMaterialDayNightDialogMinWidth;
	public static const int ThemeMaterialDayNightDialogNoActionBar;
	public static const int ThemeMaterialDayNightDialogNoActionBarMinWidth;
	public static const int ThemeMaterialDayNightDialogPresentation;
	public static const int ThemeMaterialDayNightDialogWhenLarge;
	public static const int ThemeMaterialDayNightDialogWhenLargeDarkActionBar;
	public static const int ThemeMaterialDayNightDialogWhenLargeNoActionBar;
	public static const int ThemeMaterialDayNightNoActionBar;
	public static const int ThemeMaterialDayNightNoActionBarFullscreen;
	public static const int ThemeMaterialDayNightNoActionBarOverscan;
	public static const int ThemeMaterialDayNightNoActionBarTranslucentDecor;
	public static const int ThemeMaterialDayNightPanel;
	public static const int ThemeMaterialLightDialogWhenLargeDarkActionBar;
	public static const int ThemeMaterialLightLightStatusBar;
	public static const int ThemeOverlayMaterialDialog;
	public static const int ThemeOverlayMaterialDialogAlert;
	public static const int WidgetMaterialButtonColored;
</pre>

## Namespace Android.Accounts

### Type Changed: Android.Accounts.AccountManager

Added field:

<pre style='color: green'>
	public static const string KeyLastAuthenticatedTime = "lastAuthenticatedTime";
</pre>

Added method:

<pre style='color: green'>
	public virtual bool NotifyAccountAuthenticated (Account account);
</pre>

## Namespace Android.App

### Type Changed: Android.App.Activity

Added properties:

<pre style='color: green'>
	public virtual bool IsVoiceInteraction { get; }
	public Android.Views.SearchEvent SearchEvent { get; }
	public virtual VoiceInteractor VoiceInteractor { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void OnProvideAssistContent (AssistContent outContent);
	public virtual void OnRequestPermissionsResult (int requestCode, string[] permissions, int[] grantResults);
	public virtual bool OnSearchRequested (Android.Views.SearchEvent searchEvent);
	public virtual Android.Views.ActionMode OnWindowStartingActionMode (Android.Views.ActionMode.ICallback callback, int type);
	public void RequestPermissions (string[] permissions, int requestCode);
	public virtual void ShowLockTaskEscapeMessage ();
	public virtual Android.Views.ActionMode StartActionMode (Android.Views.ActionMode.ICallback callback, int type);
</pre>

### Type Changed: Android.App.ActivityManager

Added fields:

<pre style='color: green'>
	public static const string ActionReportHeapLimit = "android.app.action.REPORT_HEAP_LIMIT";
	public static const int LockTaskModeLocked;
	public static const int LockTaskModeNone;
	public static const int LockTaskModePinned;
</pre>

Obsoleted properties:

```
[Obsolete (]
	public virtual bool IsInLockTaskMode { get; }
```

Added property:

<pre style='color: green'>
	public virtual int LockTaskModeState { get; }
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
	public static const int ImportanceForegroundService;
	public static const int ImportanceTopSleeping;
</pre>

### Type Changed: Android.App.ActivityOptions

Added method:

<pre style='color: green'>
	public static ActivityOptions MakeClipRevealAnimation (Android.Views.View source, int startX, int startY, int width, int height);
</pre>

### Type Changed: Android.App.AlarmManager

Added methods:

<pre style='color: green'>
	public virtual void SetAndAllowWhileIdle (int type, long triggerAtMillis, PendingIntent operation);
	public virtual void SetExactAndAllowWhileIdle (int type, long triggerAtMillis, PendingIntent operation);
</pre>

### Type Changed: Android.App.AlertDialog

Modified constructors:

```
protected AlertDialog (Android.Content.Context context, int theme themeResId)
```

Obsoleted fields:

```
[Obsolete (]
	public static const int ThemeDeviceDefaultDark;
	[Obsolete (]
	public static const int ThemeDeviceDefaultLight;
	[Obsolete (]
	public static const int ThemeHoloDark;
	[Obsolete (]
	public static const int ThemeHoloLight;
	[Obsolete (]
	public static const int ThemeTraditional;
```

### Type Changed: Android.App.AlertDialog.Builder

Modified constructors:

```
public AlertDialog (Android.Content.Context context, int theme themeResId)
```

Obsoleted methods:

```
[Obsolete (]
	public virtual AlertDialog.Builder SetInverseBackgroundForced (bool useInverseBackground);
```

### Type Changed: Android.App.AppOpsManager

Added field:

<pre style='color: green'>
	public static const string OpstrMockLocation = "android:mock_location";
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
	public virtual Android.Views.ActionMode OnWindowStartingActionMode (Android.Views.ActionMode.ICallback callback, int type);
</pre>

### Type Changed: Android.App.Fragment

Added properties:

<pre style='color: green'>
	public virtual Android.Content.Context Context { get; }
	public Java.Lang.Object Host { get; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void OnAttach (Activity activity);
	[Obsolete (]
	public virtual void OnInflate (Activity activity, Android.Util.IAttributeSet attrs, Android.OS.Bundle savedInstanceState);
```

Added methods:

<pre style='color: green'>
	public virtual void OnAttach (Android.Content.Context context);
	public virtual void OnInflate (Android.Content.Context context, Android.Util.IAttributeSet attrs, Android.OS.Bundle savedInstanceState);
	public virtual void OnRequestPermissionsResult (int requestCode, string[] permissions, int[] grantResults);
	public void RequestPermissions (string[] permissions, int requestCode);
</pre>

### Type Changed: Android.App.Instrumentation

Obsoleted methods:

```
[Obsolete (]
	public virtual void StartAllocCounting ();
	[Obsolete (]
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

### Type Changed: Android.App.Notification.BigPictureStyle

Added method:

<pre style='color: green'>
	public virtual Notification.BigPictureStyle BigLargeIcon (Android.Graphics.Drawables.Icon icon);
</pre>

### Type Changed: Android.App.Notification.Builder

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
	public static const string ActionNotificationPolicyChanged = "android.app.action.NOTIFICATION_POLICY_CHANGED";
	public static const int InterruptionFilterAlarms;
	public static const int InterruptionFilterAll;
	public static const int InterruptionFilterNone;
	public static const int InterruptionFilterPriority;
	public static const int InterruptionFilterUnknown;
</pre>

Added properties:

<pre style='color: green'>
	public int CurrentInterruptionFilter { get; }
	public virtual bool IsNotificationPolicyAccessGranted { get; }
	public virtual NotificationManager.Policy NotificationPolicy { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual Android.Service.Notification.StatusBarNotification[] GetActiveNotifications ();
	public virtual void RequestPolicyAccess (NotificationManager.NotificationPolicyAccessRequestCallback callback, Android.OS.Handler handler);
	public void SetInterruptionFilter (int interruptionFilter);
</pre>

### Type Changed: Android.App.PendingIntent

Added field:

<pre style='color: green'>
	public static const int FlagImmutable;
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

### New Type Android.App.AssistContent

<pre style='color: green'>
public class AssistContent : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AssistContent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AssistContent ();
	// fields
	public static const string AssistKey = "android:assist_content";
	// properties
	public virtual Android.Content.ClipData ClipData { get; set; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual Android.Content.Intent Intent { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public static AssistContent GetAssistContent (Android.OS.Bundle assistBundle);
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

### New Type Android.App.AssistStructure

<pre style='color: green'>
public sealed class AssistStructure : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields
	public static const string AssistKey = "android:assist_structure";
	// properties
	public Android.Content.ComponentName ActivityComponent { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int WindowNodeCount { get; }
	// methods
	public virtual int DescribeContents ();
	public static AssistStructure GetAssistStructure (Android.OS.Bundle assistBundle);
	public AssistStructure.WindowNode GetWindowNodeAt (int index);
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
		public static const int TextStyleBold;
		public static const int TextStyleItalic;
		public static const int TextStyleStrikeThru;
		public static const int TextStyleUnderline;
		// properties
		public virtual int ChildCount { get; }
		public virtual string ClassName { get; }
		public string ContentDescription { get; }
		public virtual Java.Lang.ICharSequence ContentDescriptionFormatted { get; }
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
		public virtual bool IsEnabled { get; }
		public virtual bool IsFocusable { get; }
		public virtual bool IsFocused { get; }
		public virtual bool IsLongClickable { get; }
		public virtual bool IsSelected { get; }
		public virtual bool IsStylusButtonPressable { get; }
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
		public virtual int TextStyle { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public virtual int Top { get; }
		public virtual int Visibility { get; }
		public virtual int Width { get; }
		// methods
		public virtual AssistStructure.ViewNode GetChildAt (int index);
	}
	public class WindowNode : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected AssistStructure (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
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
	public virtual bool OnShouldSaveFragmentState (Fragment fragment);
	public virtual void OnStartActivityFromFragment (Fragment fragment, Android.Content.Intent intent, int requestCode, Android.OS.Bundle options);
	public virtual bool OnUseFragmentManagerInflaterFactory ();
}
</pre>

### New Type Android.App.VoiceInteractor

<pre style='color: green'>
public class VoiceInteractor : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool SubmitRequest (VoiceInteractor.Request request);
	public virtual bool[] SupportsCommands (string[] commands);

	// inner types
	public class AbortVoiceRequest : Android.App.VoiceInteractor+Request, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (Java.Lang.ICharSequence message, Android.OS.Bundle extras);
		public VoiceInteractor (string message, Android.OS.Bundle extras);
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
		public VoiceInteractor (Java.Lang.ICharSequence message, Android.OS.Bundle extras);
		public VoiceInteractor (string message, Android.OS.Bundle extras);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnCompleteResult (Android.OS.Bundle result);
	}
	public class ConfirmationRequest : Android.App.VoiceInteractor+Request, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (Java.Lang.ICharSequence prompt, Android.OS.Bundle extras);
		public VoiceInteractor (string prompt, Android.OS.Bundle extras);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnConfirmationResult (bool confirmed, Android.OS.Bundle result);
	}
	public class PickOptionRequest : Android.App.VoiceInteractor+Request, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public VoiceInteractor (Java.Lang.ICharSequence prompt, VoiceInteractor.PickOptionRequest.Option[] options, Android.OS.Bundle extras);
		public VoiceInteractor (string prompt, VoiceInteractor.PickOptionRequest.Option[] options, Android.OS.Bundle extras);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnPickOptionResult (bool finished, VoiceInteractor.PickOptionRequest.Option[] selections, Android.OS.Bundle result);

		// inner types
		public sealed class Option : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
			// constructors
			public VoiceInteractor (Java.Lang.ICharSequence label);
			public VoiceInteractor (string label);
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
	public abstract class Request : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VoiceInteractor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		public virtual Activity Activity { get; }
		public virtual Android.Content.Context Context { get; }
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

Added field:

<pre style='color: green'>
	public static const string ActionReadyForUserInitialization = "android.app.action.READY_FOR_USER_INITIALIZATION";
</pre>

Added methods:

<pre style='color: green'>
	public virtual string OnChoosePrivateKeyAlias (Android.Content.Context context, Android.Content.Intent intent, int uid, string host, int port, string url, string alias);
	public virtual void OnReadyForUserInitialization (Android.Content.Context context, Android.Content.Intent intent);
	public virtual void OnSystemUpdatePending (Android.Content.Context context, Android.Content.Intent intent, long receivedTime);
</pre>

### Type Changed: Android.App.Admin.DevicePolicyManager

Obsoleted fields:

```
[Obsolete (]
	public static const string ExtraProvisioningDeviceAdminPackageName = "android.app.extra.PROVISIONING_DEVICE_ADMIN_PACKAGE_NAME";
```

Added fields:

<pre style='color: green'>
	public static const string ActionManagedProfileProvisioned = "android.app.action.MANAGED_PROFILE_PROVISIONED";
	public static const string ActionSystemUpdatePolicyChanged = "android.app.action.SYSTEM_UPDATE_POLICY_CHANGED";
	public static const int EncryptionStatusActiveDefaultKey;
	public static const string ExtraProvisioningBtDeviceId = "android.app.extra.PROVISIONING_BT_DEVICE_ID";
	public static const string ExtraProvisioningBtMacAddress = "android.app.extra.PROVISIONING_BT_MAC_ADDRESS";
	public static const string ExtraProvisioningBtUseProxy = "android.app.extra.PROVISIONING_BT_USE_PROXY";
	public static const string ExtraProvisioningBtUuid = "android.app.extra.PROVISIONING_BT_UUID";
	public static const string ExtraProvisioningDeviceAdminCertificateChecksum = "android.app.extra.PROVISIONING_DEVICE_ADMIN_CERTIFICATE_CHECKSUM";
	public static const string ExtraProvisioningDeviceAdminComponentName = "android.app.extra.PROVISIONING_DEVICE_ADMIN_COMPONENT_NAME";
	public static const string ExtraProvisioningDeviceAdminMinimumVersionCode = "android.app.extra.PROVISIONING_DEVICE_ADMIN_MINIMUM_VERSION_CODE";
	public static const string ExtraProvisioningDeviceInitializerCertificateChecksum = "android.app.extra.PROVISIONING_DEVICE_INITIALIZER_CERTIFICATE_CHECKSUM";
	public static const string ExtraProvisioningDeviceInitializerComponentName = "android.app.extra.PROVISIONING_DEVICE_INITIALIZER_COMPONENT_NAME";
	public static const string ExtraProvisioningDeviceInitializerMinimumVersionCode = "android.app.extra.PROVISIONING_DEVICE_INITIALIZER_MINIMUM_VERSION_CODE";
	public static const string ExtraProvisioningDeviceInitializerPackageChecksum = "android.app.extra.PROVISIONING_DEVICE_INITIALIZER_PACKAGE_CHECKSUM";
	public static const string ExtraProvisioningDeviceInitializerPackageDownloadCookieHeader = "android.app.extra.PROVISIONING_DEVICE_INITIALIZER_PACKAGE_DOWNLOAD_COOKIE_HEADER";
	public static const string ExtraProvisioningDeviceInitializerPackageDownloadLocation = "android.app.extra.PROVISIONING_DEVICE_INITIALIZER_PACKAGE_DOWNLOAD_LOCATION";
	public static const string ExtraProvisioningResetProtectionParameters = "android.app.extra.PROVISIONING_RESET_PROTECTION_PARAMETERS";
	public static const string ExtraProvisioningSkipEncryption = "android.app.extra.PROVISIONING_SKIP_ENCRYPTION";
	public static const string MimeTypeProvisioningNfcV2 = "application/com.android.managedprovisioning.v2";
	public static const int PermissionPolicyAutoDeny;
	public static const int PermissionPolicyAutoGrant;
	public static const int PermissionPolicyPrompt;
	public static const int ResetPasswordDoNotAskCredentialsOnBoot;
</pre>

Added property:

<pre style='color: green'>
	public virtual SystemUpdatePolicy SystemUpdatePolicy { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void ClearDeviceInitializerApp (Android.Content.ComponentName who);
	public virtual bool GetBluetoothContactSharingDisabled (Android.Content.ComponentName who);
	public virtual string GetCertInstallerPackage (Android.Content.ComponentName who);
	public virtual int GetPermissionPolicy (Android.Content.ComponentName admin);
	public virtual System.Collections.Generic.IList&lt;Android.OS.PersistableBundle&gt; GetTrustAgentConfiguration (Android.Content.ComponentName admin, Android.Content.ComponentName agent);
	public virtual bool IsDeviceInitializerApp (string packageName);
	public virtual void SendDeviceInitializerStatus (int statusCode, string description);
	public virtual void SetBluetoothContactSharingDisabled (Android.Content.ComponentName who, bool disabled);
	public virtual void SetCertInstallerPackage (Android.Content.ComponentName who, string installerPackage);
	public virtual bool SetDeviceInitializer (Android.Content.ComponentName who, Android.Content.ComponentName initializer);
	public virtual bool SetKeyguardDisabled (Android.Content.ComponentName admin, bool disabled);
	public virtual bool SetPermissionGranted (Android.Content.ComponentName admin, string packageName, string permission, bool granted);
	public virtual void SetPermissionPolicy (Android.Content.ComponentName admin, int policy);
	public virtual void SetPreferredSetupActivity (Android.Content.ComponentName admin, Android.Content.ComponentName activity);
	public virtual bool SetStatusBarDisabled (Android.Content.ComponentName admin, bool disabled);
	public virtual void SetSystemUpdatePolicy (Android.Content.ComponentName who, SystemUpdatePolicy policy);
	public virtual void SetTrustAgentConfiguration (Android.Content.ComponentName admin, Android.Content.ComponentName target, Android.OS.PersistableBundle configuration);
	public virtual bool SetUserEnabled (Android.Content.ComponentName admin);
	public virtual void SetUserIcon (Android.Content.ComponentName admin, Android.Graphics.Bitmap icon);
</pre>

### New Type Android.App.Admin.DeviceInitializerStatus

<pre style='color: green'>
public class DeviceInitializerStatus : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected DeviceInitializerStatus (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const int FlagStatusCustom;
	public static const int FlagStatusError;
	public static const int FlagStatusHighPriority;
	public static const int FlagStatusReserved;
	public static const int StatusErrorConnectWifi;
	public static const int StatusErrorDeleteApps;
	public static const int StatusErrorDoubleBump;
	public static const int StatusErrorDownloadPackage;
	public static const int StatusErrorInstallPackage;
	public static const int StatusErrorResetProtectionBlockingProvisioning;
	public static const int StatusErrorSetDevicePolicy;
	public static const int StatusStateConnectingBluetoothProxy;
	public static const int StatusStateDeviceProvisioned;
	public static const int StatusStateDisconnectingBluetoothProxy;
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.App.Admin.SystemUpdatePolicy

<pre style='color: green'>
public class SystemUpdatePolicy : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected SystemUpdatePolicy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const int TypeInstallAutomatic;
	public static const int TypeInstallWindowed;
	public static const int TypePostpone;
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual int InstallWindowEnd { get; }
	public virtual int InstallWindowStart { get; }
	public virtual int PolicyType { get; }
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

## Namespace Android.App.Usage

### Type Changed: Android.App.Usage.UsageEvents

### Type Changed: Android.App.Usage.UsageEvents.Event

Added field:

<pre style='color: green'>
	public static const int Interaction;
</pre>

### Type Changed: Android.App.Usage.UsageStatsManager

Added method:

<pre style='color: green'>
	public bool IsAppInactive (string packageName);
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
	public virtual NetworkUsageStats QueryDetails (int networkType, string subscriberId, long startTime, long endTime);
	public virtual NetworkUsageStats QueryDetailsForUid (int networkType, string subscriberId, long startTime, long endTime, int uid);
	public virtual NetworkUsageStats QuerySummary (int networkType, string subscriberId, long startTime, long endTime);
	public virtual NetworkUsageStats.Bucket QuerySummaryForDevice (int networkType, string subscriberId, long startTime, long endTime);
	public virtual NetworkUsageStats.Bucket QuerySummaryForUser (int networkType, string subscriberId, long startTime, long endTime);
}
</pre>

### New Type Android.App.Usage.NetworkUsageStats

<pre style='color: green'>
public sealed class NetworkUsageStats : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public bool HasNextBucket { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void Close ();
	public bool GetNextBucket (NetworkUsageStats.Bucket bucketOut);

	// inner types
	public class Bucket : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected NetworkUsageStats (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public NetworkUsageStats ();
		// fields
		public static const int StateAll;
		public static const int StateDefault;
		public static const int StateForeground;
		public static const int UidRemoved;
		public static const int UidTethering;
		// properties
		public virtual long EndTimeStamp { get; }
		public virtual long RxBytes { get; }
		public virtual long RxPackets { get; }
		public virtual long StartTimeStamp { get; }
		public virtual int State { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public virtual long TxBytes { get; }
		public virtual long TxPackets { get; }
		public virtual int Uid { get; }
	}
}
</pre>

## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothA2dp

### Type Changed: Android.Bluetooth.BluetoothA2dp.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const int Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothGatt

### Type Changed: Android.Bluetooth.BluetoothGatt.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const int Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothGattServer

### Type Changed: Android.Bluetooth.BluetoothGattServer.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const int Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothHeadset

### Type Changed: Android.Bluetooth.BluetoothHeadset.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const int Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothHealth

### Type Changed: Android.Bluetooth.BluetoothHealth.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const int Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothProfile

Added field:

<pre style='color: green'>
	public static const int Sap;
</pre>

### Type Changed: Android.Bluetooth.BluetoothSocket

Added fields:

<pre style='color: green'>
	public static const int TypeL2cap;
	public static const int TypeRfcomm;
	public static const int TypeSco;
</pre>

Added properties:

<pre style='color: green'>
	public int ConnectionType { get; }
	public int MaxReceivePacketSize { get; }
	public int MaxTransmitPacketSize { get; }
</pre>

## Namespace Android.Bluetooth.LE

### Type Changed: Android.Bluetooth.LE.ScanSettings

Added fields:

<pre style='color: green'>
	public static const int CallbackTypeFirstMatch;
	public static const int CallbackTypeMatchLost;
	public static const int MatchModeAggressive;
	public static const int MatchModeSticky;
	public static const int MatchNumFewAdvertisement;
	public static const int MatchNumMaxAdvertisement;
	public static const int MatchNumOneAdvertisement;
	public static const int ScanModeOpportunistic;
</pre>

### Type Changed: Android.Bluetooth.LE.ScanSettings.Builder

Added methods:

<pre style='color: green'>
	public ScanSettings.Builder SetCallbackType (ScanCallbackType callbackType);
	public ScanSettings.Builder SetMatchMode (int matchMode);
	public ScanSettings.Builder SetNumOfMatches (int numOfMatches);
</pre>

## Namespace Android.Content

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
	public virtual int CheckSelfPermission (string permission);
	public int GetColor (int id);
	public Res.ColorStateList GetColorStateList (int id);
	public Java.Lang.Object GetSystemService (Java.Lang.Class serviceClass);
</pre>

### Type Changed: Android.Content.ContextWrapper

Added methods:

<pre style='color: green'>
	public override int CheckSelfPermission (string permission);
	public virtual string GetSystemServiceName (Java.Lang.Class serviceClass);
</pre>

### Type Changed: Android.Content.Intent

Added fields:

<pre style='color: green'>
	public static const string ActionProcessText = "android.intent.action.PROCESS_TEXT";
	public static const string CategoryVoice = "android.intent.category.VOICE";
	public static const string ExtraAlternateIntents = "android.intent.extra.ALTERNATE_INTENTS";
	public static const string ExtraAssistUid = "android.intent.extra.ASSIST_UID";
	public static const string ExtraChooserRefinementIntentSender = "android.intent.extra.CHOOSER_REFINEMENT_INTENT_SENDER";
	public static const string ExtraProcessText = "android.intent.extra.PROCESS_TEXT";
	public static const string ExtraProcessTextReadonly = "android.intent.extra.PROCESS_TEXT_READONLY";
	public static const string ExtraResultReceiver = "android.intent.extra.RESULT_RECEIVER";
</pre>

### Type Changed: Android.Content.IntentFilter

Added fields:

<pre style='color: green'>
	public static const string SchemeHttp = "http";
	public static const string SchemeHttps = "https";
</pre>

### Type Changed: Android.Content.RestrictionEntry

Added constructor:

<pre style='color: green'>
	public RestrictionEntry (string key, RestrictionEntry[] restrictionEntries, bool isBundleArray);
</pre>

Added fields:

<pre style='color: green'>
	public static const int TypeBundle;
	public static const int TypeBundleArray;
</pre>

Added methods:

<pre style='color: green'>
	public virtual RestrictionEntry[] GetRestrictions ();
	public virtual void SetRestrictions (RestrictionEntry[] restrictions);
</pre>

### Type Changed: Android.Content.RestrictionsManager

Added method:

<pre style='color: green'>
	public static Android.OS.Bundle ConvertRestrictionsToBundle (System.Collections.Generic.IList&lt;RestrictionEntry&gt; entries);
</pre>

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ApplicationInfo

Added fields:

<pre style='color: green'>
	public static const int FlagExtractNativeLibs;
	public static const int FlagUsesCleartextTraffic;
</pre>

Added properties:

<pre style='color: green'>
	public int FullBackupContent { get; set; }
	public bool HardwareAccelerated { get; set; }
</pre>

### Type Changed: Android.Content.PM.PackageManager

Added fields:

<pre style='color: green'>
	public static const string FeatureAudioPro = "android.hardware.audio.pro";
	public static const string FeatureAutomotive = "android.hardware.type.automotive";
	public static const string FeatureHifiSensors = "android.hardware.sensor.hifi_sensors";
	public static const string FeatureMidi = "android.software.midi";
	public static const int MatchAll;
</pre>

## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.ColorStateList

Added property:

<pre style='color: green'>
	public virtual int ChangingConfigurations { get; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public static ColorStateList CreateFromXml (Resources r, System.Xml.XmlReader parser);
```

Added method:

<pre style='color: green'>
	public static ColorStateList CreateFromXml (Resources r, System.Xml.XmlReader parser, Resources.Theme theme);
</pre>

### Type Changed: Android.Content.Res.Resources

Obsoleted methods:

```
[Obsolete (]
	public virtual Android.Graphics.Color GetColor (int id);
	[Obsolete (]
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
	public int ChangingConfigurations { get; }
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
[Obsolete (]
	public virtual void Deactivate ();
	[Obsolete (]
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
	public static const int Depth16;
	public static const int DepthPointCloud;
	public static const int FlexRgb888;
	public static const int FlexRgba8888;
	public static const int Private;
	public static const int Raw12;
	public static const int Yuv422888;
	public static const int Yuv444888;
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

Added property:

<pre style='color: green'>
	public virtual System.Collections.Generic.IList&lt;Android.Animation.Animator.IAnimatorListener&gt; Listeners { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddListener (Android.Animation.Animator.IAnimatorListener listener);
	public virtual void RemoveListener (Android.Animation.Animator.IAnimatorListener listener);
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
	public virtual bool Dither { get; }
	public virtual bool FilterBitmap { get; }
	public virtual int LayoutDirection { get; }
</pre>

Modified methods:

```
public abstract void SetColorFilter (Android.Graphics.ColorFilter cf colorFilter)
	public virtual void SetTint (int tint tintColor)
```

Added methods:

<pre style='color: green'>
	public virtual void GetHotspotBounds (Android.Graphics.Rect outRect);
	public virtual bool OnLayoutDirectionChange (int layoutDirection);
	public bool SetLayoutDirection (int layoutDirection);
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
	public virtual int GetLayerGravity (int index);
	public virtual int GetLayerHeight (int index);
	public virtual int GetLayerInsetBottom (int index);
	public virtual int GetLayerInsetEnd (int index);
	public virtual int GetLayerInsetLeft (int index);
	public virtual int GetLayerInsetRight (int index);
	public virtual int GetLayerInsetStart (int index);
	public virtual int GetLayerInsetTop (int index);
	public virtual int GetLayerWidth (int index);
	public virtual void SetDrawable (int index, Drawable drawable);
	public virtual void SetLayerGravity (int index, int gravity);
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
	public static Icon CreateWithResource (string resPackage, int resId);
	public static Icon CreateWithResource (Android.Content.Context context, int resId);
	public virtual int DescribeContents ();
	public Drawable LoadDrawable (Android.Content.Context context);
	public void LoadDrawableAsync (Android.Content.Context context, Icon.IOnDrawableLoadedListener listener, Android.OS.Handler handler);
	public void LoadDrawableAsync (Android.Content.Context context, Android.OS.Message andThen);
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

### Type Changed: Android.Hardware.Camera

Added field:

<pre style='color: green'>
	public static const int CameraErrorEvicted;
</pre>

## Namespace Android.Hardware.Camera2

### Type Changed: Android.Hardware.Camera2.CameraAccessException

Added fields:

<pre style='color: green'>
	public static const int CameraInUse;
	public static const int MaxCamerasInUse;
</pre>

### Type Changed: Android.Hardware.Camera2.CameraCaptureSession

Added properties:

<pre style='color: green'>
	public virtual Android.Views.Surface InputSurface { get; }
	public virtual bool IsReprocessible { get; }
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
	public static CameraCharacteristics.Key ShadingAvailableModes { get; }
	public static CameraCharacteristics.Key StatisticsInfoAvailableLensShadingMapModes { get; }
</pre>

### Type Changed: Android.Hardware.Camera2.CameraDevice

Added methods:

<pre style='color: green'>
	public virtual CaptureRequest.Builder CreateReprocessCaptureRequest (TotalCaptureResult inputResult);
	public virtual void CreateReprocessibleCaptureSession (Params.InputConfiguration inputConfig, System.Collections.Generic.IList&lt;Android.Views.Surface&gt; outputs, CameraCaptureSession.StateCallback callback, Android.OS.Handler handler);
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

### Type Changed: Android.Hardware.Camera2.CameraMetadata

Added fields:

<pre style='color: green'>
	public static const int ControlAePrecaptureTriggerCancel;
	public static const int InfoSupportedHardwareLevelHighResolution;
	public static const int LensFacingExternal;
	public static const int NoiseReductionModeMinimal;
	public static const int RequestAvailableCapabilitiesDepthOutput;
	public static const int RequestAvailableCapabilitiesOpaqueReprocessing;
	public static const int RequestAvailableCapabilitiesYuvReprocessing;
	public static const int TonemapModeGammaValue;
	public static const int TonemapModePresetCurve;
	public static const int TonemapPresetCurveRec709;
	public static const int TonemapPresetCurveSrgb;
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

## Namespace Android.Hardware.Camera2.Params

### Type Changed: Android.Hardware.Camera2.Params.StreamConfigurationMap

Added methods:

<pre style='color: green'>
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

## Namespace Android.Hardware.Usb

### Type Changed: Android.Hardware.Usb.UsbDevice

Added property:

<pre style='color: green'>
	public virtual string Version { get; }
</pre>

## Namespace Android.Media

### Type Changed: Android.Media.AsyncPlayer

Obsoleted methods:

```
[Obsolete (]
	public virtual void Play (Android.Content.Context context, Android.Net.Uri uri, bool looping, Stream stream);
```

Added method:

<pre style='color: green'>
	public virtual void Play (Android.Content.Context context, Android.Net.Uri uri, bool looping, AudioAttributes attributes);
</pre>

### Type Changed: Android.Media.AudioFormat

Added fields:

<pre style='color: green'>
	public static const int ChannelOut7point1Surround;
	public static const int EncodingDts;
	public static const int EncodingDtsHd;
</pre>

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
	public static const int AdjustMute;
	public static const int AdjustToggleMute;
	public static const int AdjustUnmute;
	public static const int GetDevicesAll;
	public static const int GetDevicesInputs;
	public static const int GetDevicesOutputs;
	public static const string PropertySupportMicNearUltrasound = "android.media.property.SUPPORT_MIC_NEAR_ULTRASOUND";
	public static const string PropertySupportSpeakerNearUltrasound = "android.media.property.SUPPORT_SPEAKER_NEAR_ULTRASOUND";
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void SetStreamMute (Stream streamType, bool state);
	[Obsolete (]
	public virtual void SetStreamSolo (Stream streamType, bool state);
```

Added methods:

<pre style='color: green'>
	public virtual AudioDeviceInfo[] GetDevices (int flags);
	public virtual bool IsStreamMute (int streamType);
	public virtual void RegisterAudioDeviceCallback (AudioDeviceCallback callback, Android.OS.Handler handler);
	public virtual void UnregisterAudioDeviceCallback (AudioDeviceCallback callback);
</pre>

### Type Changed: Android.Media.AudioRecord

Added fields:

<pre style='color: green'>
	public static const int ReadBlocking;
	public static const int ReadNonBlocking;
</pre>

Added properties:

<pre style='color: green'>
	public virtual AudioFormat Format { get; }
	public virtual int NativeFrameCount { get; }
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
	public virtual AudioRecord.Builder SetAudioSource (int source);
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

Modified properties:

```
protected public virtual int NativeFrameCount { get; }
```

Added properties:

<pre style='color: green'>
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
	public virtual AudioTrack.Builder SetTransferMode (int mode);
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

### Type Changed: Android.Media.Image

Added property:

<pre style='color: green'>
	public virtual bool IsOpaque { get; }
</pre>

### Type Changed: Android.Media.ImageReader

Added property:

<pre style='color: green'>
	public virtual bool IsOpaque { get; }
</pre>

Added method:

<pre style='color: green'>
	public static ImageReader NewOpaqueInstance (int width, int height, int maxImages);
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

Added fields:

<pre style='color: green'>
	public static const int ErrorInsufficientResource;
	public static const int ErrorReclaimed;
</pre>

Added property:

<pre style='color: green'>
	public int ErrorCode { get; }
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

### Type Changed: Android.Media.MediaCodecInfo

### Type Changed: Android.Media.MediaCodecInfo.CodecCapabilities

Added fields:

<pre style='color: green'>
	public static const int COLORFormat32bitABGR8888;
	public static const int COLORFormatRGBAFlexible;
	public static const int COLORFormatRGBFlexible;
	public static const int COLORFormatYUV422Flexible;
	public static const int COLORFormatYUV444Flexible;
</pre>

Added property:

<pre style='color: green'>
	public int MaxSupportedInstances { get; }
</pre>

### Type Changed: Android.Media.MediaCodecInfo.CodecProfileLevel

Added fields:

<pre style='color: green'>
	public static const int MPEG2LevelH14;
	public static const int MPEG2LevelHL;
	public static const int MPEG2LevelLL;
	public static const int MPEG2LevelML;
	public static const int MPEG2Profile422;
	public static const int MPEG2ProfileHigh;
	public static const int MPEG2ProfileMain;
	public static const int MPEG2ProfileSimple;
	public static const int MPEG2ProfileSNR;
	public static const int MPEG2ProfileSpatial;
</pre>

### Type Changed: Android.Media.MediaCodecInfo.VideoCapabilities

Added method:

<pre style='color: green'>
	public Android.Util.Range GetAchievableFrameRatesFor (int width, int height);
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

Added fields:

<pre style='color: green'>
	public static const int EventSessionReclaimed;
	public static const int KeyStatusExpired;
	public static const int KeyStatusInternalError;
	public static const int KeyStatusOutputNotAllowed;
	public static const int KeyStatusPending;
	public static const int KeyStatusUsable;
	public static const int RequestTypeInitial;
	public static const int RequestTypeRelease;
	public static const int RequestTypeRenewal;
</pre>

Added methods:

<pre style='color: green'>
	public void SetOnExpirationUpdateListener (MediaDrm.IOnExpirationUpdateListener listener, Android.OS.Handler handler);
	public void SetOnKeysChangeListener (MediaDrm.IOnKeysChangeListener listener, Android.OS.Handler handler);
</pre>

### Type Changed: Android.Media.MediaDrm.KeyRequest

Added property:

<pre style='color: green'>
	public int RequestType { get; }
</pre>

### New Type Android.Media.KeyStatus

<pre style='color: green'>
public sealed class KeyStatus : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public int StatusCode { get; }
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

### New Type Android.Media.IOnKeysChangeListener

<pre style='color: green'>
public interface IOnKeysChangeListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnKeysChange (MediaDrm md, byte[] sessionId, System.Collections.Generic.IList&lt;MediaDrm.KeyStatus&gt; keyInformation, bool hasNewUsableKey);
}
</pre>

### New Type Android.Media.KeysChangeEventArgs

<pre style='color: green'>
public class KeysChangeEventArgs : System.EventArgs {
	// constructors
	public MediaDrm (MediaDrm md, byte[] sessionId, System.Collections.Generic.IList&lt;MediaDrm.KeyStatus&gt; keyInformation, bool hasNewUsableKey);
	// properties
	public bool HasNewUsableKey { get; }
	public System.Collections.Generic.IList&lt;MediaDrm.KeyStatus&gt; KeyInformation { get; }
	public MediaDrm Md { get; }
	public byte[] SessionId { get; }
}
</pre>

### Type Changed: Android.Media.MediaExtractor

Added methods:

<pre style='color: green'>
	public void SetDataSource (IMediaDataSource dataSource);
	public System.Threading.Tasks.Task SetDataSourceAsync (IMediaDataSource dataSource);
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
</pre>

### Type Changed: Android.Media.MediaMetadataRetriever

Added field:

<pre style='color: green'>
	public static const int MetadataKeyCaptureFramerate;
</pre>

Added methods:

<pre style='color: green'>
	public virtual void SetDataSource (IMediaDataSource dataSource);
	public System.Threading.Tasks.Task SetDataSourceAsync (IMediaDataSource dataSource);
</pre>

### Type Changed: Android.Media.MediaPlayer

Added fields:

<pre style='color: green'>
	public static const int PlaybackRateAudioModeDefault;
	public static const int PlaybackRateAudioModeResample;
	public static const int PlaybackRateAudioModeStretch;
</pre>

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
	public virtual void SetDataSource (IMediaDataSource dataSource);
	public System.Threading.Tasks.Task SetDataSourceAsync (IMediaDataSource dataSource);
	public virtual void SetOnTimedMetaDataAvailableListener (MediaPlayer.IOnTimedMetaDataAvailableListener listener);
	public virtual void SetPlaybackRate (float rate, int audioMode);
</pre>

### Type Changed: Android.Media.MediaPlayer.TrackInfo

Added field:

<pre style='color: green'>
	public static const int MediaTrackTypeMetadata;
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
	// fields
	public static const int TypeAuxLine;
	public static const int TypeBluetoothA2dp;
	public static const int TypeBluetoothSco;
	public static const int TypeBuiltinEarpiece;
	public static const int TypeBuiltinMic;
	public static const int TypeBuiltinSpeaker;
	public static const int TypeDock;
	public static const int TypeFm;
	public static const int TypeFmTuner;
	public static const int TypeHdmi;
	public static const int TypeHdmiArc;
	public static const int TypeLineAnalog;
	public static const int TypeLineDigital;
	public static const int TypeTelephony;
	public static const int TypeTvTuner;
	public static const int TypeUnknown;
	public static const int TypeUsbAccessory;
	public static const int TypeUsbDevice;
	public static const int TypeWiredHeadphones;
	public static const int TypeWiredHeadset;
	// properties
	public int Id { get; }
	public bool IsSink { get; }
	public bool IsSource { get; }
	public string ProductName { get; }
	public Java.Lang.ICharSequence ProductNameFormatted { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int Type { get; }
	// methods
	public int[] GetChannelCounts ();
	public int[] GetChannelIndexMasks ();
	public int[] GetChannelMasks ();
	public int[] GetFormats ();
	public int[] GetSampleRates ();
}
</pre>

### New Type Android.Media.ImageWriter

<pre style='color: green'>
public class ImageWriter : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ImageWriter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual int Format { get; }
	public virtual int MaxImages { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Close ();
	public virtual Image DequeueInputImage ();
	public static ImageWriter NewInstance (Android.Views.Surface surface, int maxImages);
	public virtual void QueueInputImage (Image image);
	public virtual void SetImageListener (ImageWriter.IImageListener listener, Android.OS.Handler handler);

	// inner types
	public interface IImageListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual void OnInputImageReleased (ImageWriter writer);
	}
	public class ImageEventArgs : System.EventArgs {
		// constructors
		public ImageWriter (ImageWriter writer);
		// properties
		public ImageWriter Writer { get; }
	}
}
</pre>

### New Type Android.Media.IMediaDataSource

<pre style='color: green'>
public interface IMediaDataSource : Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual long Size { get; }
	// methods
	public virtual int ReadAt (long position, byte[] buffer, int size);
}
</pre>

### New Type Android.Media.MediaSync

<pre style='color: green'>
public sealed class MediaSync : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MediaSync ();
	// fields
	public static const int MediasyncErrorAudiotrackFail;
	public static const int MediasyncErrorSurfaceFail;
	public static const int PlaybackRateAudioModeDefault;
	public static const int PlaybackRateAudioModeResample;
	public static const int PlaybackRateAudioModeStretch;
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
	public void SetPlaybackRate (float rate, int audioMode);
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
		public virtual void OnError (MediaSync sync, int what, int extra);
	}
	public class ErrorEventArgs : System.EventArgs {
		// constructors
		public MediaSync (MediaSync sync, int what, int extra);
		// properties
		public int Extra { get; }
		public MediaSync Sync { get; }
		public int What { get; }
	}
}
</pre>

### New Type Android.Media.MediaTimestamp

<pre style='color: green'>
public sealed class MediaTimestamp : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public float ClockRate { get; set; }
	public long MediaTimeUs { get; set; }
	public long NanoTime { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Media.PlaybackParams

<pre style='color: green'>
public sealed class PlaybackParams : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public PlaybackParams ();
	// fields
	public static const int AudioFallbackModeDefault;
	public static const int AudioFallbackModeFail;
	public static const int AudioFallbackModeMute;
	// properties
	public int AudioFallbackMode { get; }
	public float Pitch { get; }
	public float Speed { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public PlaybackParams AllowDefaults ();
	public PlaybackParams SetAudioFallbackMode (int audioFallbackMode);
	public PlaybackParams SetPitch (float pitch);
	public PlaybackParams SetSpeed (float speed);
}
</pre>

### New Type Android.Media.SyncParams

<pre style='color: green'>
public sealed class SyncParams : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public SyncParams ();
	// fields
	public static const int AudioAdjustModeDefault;
	public static const int AudioAdjustModeResample;
	public static const int AudioAdjustModeStretch;
	public static const int SyncSourceAudio;
	public static const int SyncSourceDefault;
	public static const int SyncSourceSystemClock;
	public static const int SyncSourceVsync;
	// properties
	public int AudioAdjustMode { get; }
	public float FrameRate { get; }
	public int SyncSource { get; }
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
	public void GetMediaItem (string mediaId, MediaBrowser.MediaItemCallback cb);
</pre>

### New Type Android.Media.Browse.MediaItemCallback

<pre style='color: green'>
public abstract class MediaItemCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected MediaBrowser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MediaBrowser ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnError ();
	public virtual void OnMediaItemLoaded (MediaBrowser.MediaItem item);
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
</pre>

### Type Changed: Android.Media.TV.TvInputManager

Added fields:

<pre style='color: green'>
	public static const long TimeShiftInvalidTime;
	public static const int TimeShiftStatusAvailable;
	public static const int TimeShiftStatusUnavailable;
	public static const int TimeShiftStatusUnknown;
	public static const int TimeShiftStatusUnsupported;
	public static const int VideoUnavailableReasonAudioOnly;
</pre>

### Type Changed: Android.Media.TV.TvInputService

### Type Changed: Android.Media.TV.TvInputService.Session

Added methods:

<pre style='color: green'>
	public virtual void LayoutSurface (int left, int top, int right, int bottom);
	public virtual void NotifyTimeShiftStatusChanged (int status);
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
	public virtual void OnTimeShiftStatusChanged (string inputId, int status);
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

## Namespace Android.Net

### Type Changed: Android.Net.ConnectivityManager

Added fields:

<pre style='color: green'>
	public static const string ActionCaptivePortalSignIn = "android.net.conn.CAPTIVE_PORTAL";
	public static const string ExtraCaptivePortalToken = "captivePortalToken";
</pre>

Obsoleted properties:

```
[Obsolete (]
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
[Obsolete (]
	public virtual NetworkInfo[] GetAllNetworkInfo ();
	[Obsolete (]
	public virtual NetworkInfo GetNetworkInfo (ConnectivityType networkType);
	[Obsolete (]
	public static bool IsNetworkTypeValid (ConnectivityType networkType);
	[Obsolete (]
	public virtual void ReportBadNetwork (Network network);
	[Obsolete (]
	public static bool SetProcessDefaultNetwork (Network network);
```

Added methods:

<pre style='color: green'>
	public virtual bool BindProcessToNetwork (Network network);
	public virtual void IgnoreNetworkWithCaptivePortal (Network network, string actionToken);
	public virtual void ReportCaptivePortalDismissed (Network network, string actionToken);
	public virtual void ReportNetworkConnectivity (Network network, bool hasConnectivity);
	public virtual bool RequestBandwidthUpdate (Network network);
</pre>

### Type Changed: Android.Net.ConnectivityManager.NetworkCallback

Added method:

<pre style='color: green'>
	public virtual void OnPreCheck (Network network);
</pre>

### Type Changed: Android.Net.IpPrefix

Added method:

<pre style='color: green'>
	public bool Contains (Java.Net.InetAddress address);
</pre>

### Type Changed: Android.Net.Network

Added property:

<pre style='color: green'>
	public virtual long NetworkHandle { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual Java.Net.URLConnection OpenConnection (Java.Net.URL url, Java.Net.Proxy proxy);
</pre>

### Type Changed: Android.Net.Proxy

Obsoleted fields:

```
[Obsolete (]
	public static const string ExtraProxyInfo = "android.intent.extra.PROXY_INFO";
```

## Namespace Android.Net.Wifi

### Type Changed: Android.Net.Wifi.ScanResult

Added fields:

<pre style='color: green'>
	public static const int ChannelWidth160mhz;
	public static const int ChannelWidth20mhz;
	public static const int ChannelWidth40mhz;
	public static const int ChannelWidth80mhz;
	public static const int ChannelWidth80mhzPlusMhz;
</pre>

Added properties:

<pre style='color: green'>
	public int CenterFreq0 { get; set; }
	public int CenterFreq1 { get; set; }
	public int ChannelWidth { get; set; }
	public bool Is80211McRTTResponder { get; set; }
	public string OperatorFriendlyName { get; set; }
	public bool PasspointNetwork { get; set; }
	public string VenueName { get; set; }
</pre>

### Type Changed: Android.Net.Wifi.WifiConfiguration

Added properties:

<pre style='color: green'>
	public virtual bool IsPasspoint { get; }
	public string ProviderFriendlyName { get; set; }
	public Java.Util.HashSet RoamingConsortiumIds { get; set; }
</pre>

### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig

Obsoleted properties:

```
[Obsolete (]
	public virtual string SubjectMatch { get; set; }
```

Added properties:

<pre style='color: green'>
	public virtual string AltSubjectMatch { get; set; }
	public virtual string DomainSubjectMatch { get; }
	public virtual string Plmn { get; set; }
	public virtual string Realm { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void SetDomainSuffixMatch (string domain);
</pre>

### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig.Eap

Added field:

<pre style='color: green'>
	public static const int AkaPrime;
</pre>

## Namespace Android.Nfc

### Type Changed: Android.Nfc.NfcEvent

Added property:

<pre style='color: green'>
	public sbyte PeerLlcpVersion { get; set; }
</pre>

## Namespace Android.Nfc.CardEmulators

### Type Changed: Android.Nfc.CardEmulators.CardEmulation

Added fields:

<pre style='color: green'>
	public static const string ActionRequestServiceResources = "android.nfc.cardemulation.action.REQUEST_SERVICE_RESOURCES";
	public static const string ExtraBannerResId = "android.nfc.cardemulation.extra.BANNER_RES_ID";
	public static const string ExtraDescription = "android.nfc.cardemulation.extra.DESCRIPTION";
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

Added property:

<pre style='color: green'>
	public static int PreviewSdkInt { get; }
</pre>

### Type Changed: Android.OS.Build.VERSION_CODES

Added field:

<pre style='color: green'>
	public static const int Mnc;
</pre>

### Type Changed: Android.OS.Debug

Obsoleted properties:

```
[Obsolete (]
	public static int GlobalAllocCount { get; }
	[Obsolete (]
	public static int GlobalAllocSize { get; }
	[Obsolete (]
	public static int GlobalClassInitCount { get; }
	[Obsolete (]
	public static int GlobalClassInitTime { get; }
	[Obsolete (]
	public static int GlobalFreedCount { get; }
	[Obsolete (]
	public static int GlobalFreedSize { get; }
	[Obsolete (]
	public static int GlobalGcInvocationCount { get; }
	[Obsolete (]
	public static int ThreadAllocCount { get; }
	[Obsolete (]
	public static int ThreadAllocSize { get; }
	[Obsolete (]
	public static int ThreadGcInvocationCount { get; }
```

Added property:

<pre style='color: green'>
	public static System.Collections.Generic.IDictionary&lt;System.String,System.String&gt; RuntimeStats { get; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public static void ResetAllCounts ();
	[Obsolete (]
	public static void ResetGlobalAllocCount ();
	[Obsolete (]
	public static void ResetGlobalAllocSize ();
	[Obsolete (]
	public static void ResetGlobalClassInitCount ();
	[Obsolete (]
	public static void ResetGlobalClassInitTime ();
	[Obsolete (]
	public static void ResetGlobalFreedCount ();
	[Obsolete (]
	public static void ResetGlobalFreedSize ();
	[Obsolete (]
	public static void ResetGlobalGcInvocationCount ();
	[Obsolete (]
	public static void ResetThreadAllocCount ();
	[Obsolete (]
	public static void ResetThreadAllocSize ();
	[Obsolete (]
	public static void ResetThreadGcInvocationCount ();
```

Added method:

<pre style='color: green'>
	public static string GetRuntimeStat (string statName);
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
	public virtual void RegisterFileDescriptorCallback (Java.IO.FileDescriptor fd, int events, MessageQueue.FileDescriptorCallback callback);
	public virtual void UnregisterFileDescriptorCallback (Java.IO.FileDescriptor fd);
</pre>

### New Type Android.OS.FileDescriptorCallback

<pre style='color: green'>
public abstract class FileDescriptorCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected MessageQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MessageQueue ();
	// fields
	public static const int EventError;
	public static const int EventInput;
	public static const int EventOutput;
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int OnFileDescriptorEvents (Java.IO.FileDescriptor fd, int events);
}
</pre>

### Type Changed: Android.OS.Parcel

Added methods:

<pre style='color: green'>
	public Java.Lang.Object ReadTypedObject (IParcelableCreator c);
	public void WriteTypedObject (Java.Lang.Object val, int parcelableFlags);
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

### Type Changed: Android.OS.UserManager

Added field:

<pre style='color: green'>
	public static const string DisallowSafeBoot = "no_safe_boot";
</pre>

Added property:

<pre style='color: green'>
	public virtual bool IsSystemUser { get; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual bool SetRestrictionsChallenge (string newPin);
```

Added method:

<pre style='color: green'>
	public virtual long GetUserCreationTime (UserHandle userHandle);
</pre>

## Namespace Android.Print

### Type Changed: Android.Print.PrintAttributes

Added fields:

<pre style='color: green'>
	public static const int DuplexModeLongEdge;
	public static const int DuplexModeNone;
	public static const int DuplexModeShortEdge;
</pre>

Added property:

<pre style='color: green'>
	public int DuplexMode { get; }
</pre>

### Type Changed: Android.Print.PrintAttributes.Builder

Added method:

<pre style='color: green'>
	public PrintAttributes.Builder SetDuplexMode (int duplexMode);
</pre>

### Type Changed: Android.Print.PrinterCapabilitiesInfo

Added property:

<pre style='color: green'>
	public int DuplexModes { get; }
</pre>

### Type Changed: Android.Print.PrinterCapabilitiesInfo.Builder

Added method:

<pre style='color: green'>
	public PrinterCapabilitiesInfo.Builder SetDuplexModes (int duplexModes, int defaultDuplexMode);
</pre>

## Namespace Android.Provider

### Type Changed: Android.Provider.AlarmClock

Added fields:

<pre style='color: green'>
	public static const string ActionVoiceCancelAlarm = "android.intent.action.VOICE_CANCEL_ALARM";
	public static const string ActionVoiceDeleteAlarm = "android.intent.action.VOICE_DELETE_ALARM";
	public static const string AlarmSearchModeAll = "all";
	public static const string AlarmSearchModeNext = "next";
	public static const string AlarmSearchModeNone = "none";
	public static const string AlarmSearchModeTime = "time";
	public static const string ExtraAlarmSearchMode = "android.intent.extra.alarm.ALARM_SEARCH_MODE";
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

### Type Changed: Android.Provider.ContactsContract.Email

Added property:

<pre style='color: green'>
	public static Android.Net.Uri EnterpriseContentLookupUri { get; }
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

### Type Changed: Android.Provider.ContactsContract.DisplayNameSources

Added field:

<pre style='color: green'>
	public static const int StructuredPhoneticName;
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

### New Type Android.Provider.Authorization

<pre style='color: green'>
public sealed class Authorization : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public ContactsContract ();
	// fields
	public static const string AuthorizationMethod = "authorize";
	public static const string KeyAuthorizedUri = "authorized_uri";
	public static const string KeyUriToAuthorize = "uri_to_authorize";
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Provider.ProviderStatus

<pre style='color: green'>
public sealed class ProviderStatus : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const string ContentType = "vnd.android.cursor.dir/provider_status";
	public static const string Status = "status";
	public static const int StatusChangingLocale;
	public static const int StatusNoAccountsNoContacts;
	public static const int StatusNormal;
	public static const int StatusUpgrading;
	// properties
	public static Android.Net.Uri ContentUri { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### Type Changed: Android.Provider.MediaStore

Added fields:

<pre style='color: green'>
	public static const string ActionStillImageCameraCooldown = "android.media.action.STILL_IMAGE_CAMERA_COOLDOWN";
	public static const string ActionStillImageCameraPrewarm = "android.media.action.STILL_IMAGE_CAMERA_PREWARM";
</pre>

### Type Changed: Android.Provider.Settings

Added fields:

<pre style='color: green'>
	public static const string ActionVoiceControlAirplaneMode = "android.settings.VOICE_CONTROL_AIRPLANE_MODE";
	public static const string ActionVoiceControlBatterySaverMode = "android.settings.VOICE_CONTROL_BATTERY_SAVER_MODE";
	public static const string ActionVoiceControlDoNotDisturbMode = "android.settings.VOICE_CONTROL_DO_NOT_DISTURB_MODE";
	public static const string ActionZenAccessSettings = "android.settings.ZEN_ACCESS_SETTINGS";
	public static const string ExtraAirplaneModeEnabled = "airplane_mode_enabled";
	public static const string ExtraBatterySaverModeEnabled = "android.settings.extra.battery_saver_mode_enabled";
	public static const string ExtraDoNotDisturbModeEnabled = "android.settings.extra.do_not_disturb_mode_enabled";
	public static const string ExtraDoNotDisturbModeMinutes = "android.settings.extra.do_not_disturb_mode_minutes";
	public static const string IntentCategoryUsageAccessConfig = "android.intent.category.USAGE_ACCESS_CONFIG";
	public static const string MetadataUsageAccessReason = "android.settings.metadata.USAGE_ACCESS_REASON";
</pre>

### Type Changed: Android.Provider.Settings.Global

Added field:

<pre style='color: green'>
	public static const string HideCarrierNetworkSettings = "hide_carrier_network_settings";
</pre>

### Type Changed: Android.Provider.Settings.Secure

Obsoleted fields:

```
[Obsolete (]
	public static const string AllowMockLocation = "mock_location";
	[Obsolete (]
	public static const string LockPatternEnabled = "lock_pattern_autolock";
```

### Type Changed: Android.Provider.Settings.System

Added fields:

<pre style='color: green'>
	public static const string DtmfToneTypeWhenDialing = "dtmf_tone_type";
	public static const string VibrateWhenRinging = "vibrate_when_ringing";
</pre>

### Type Changed: Android.Provider.Telephony

### Type Changed: Android.Provider.Telephony.Carriers

Obsoleted fields:

```
[Obsolete (]
	public static const string Bearer = "bearer";
```

Added field:

<pre style='color: green'>
	public static const string BearerBitmask = "bearer_bitmask";
</pre>

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
[Obsolete (]
	public void Execute ();
	[Obsolete (]
	public void SetInput (Script.KernelID s, Allocation a);
	[Obsolete (]
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
	public Script.FieldID Field { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public Java.Lang.Object Value { get; }
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

	// inner types
	public interface IDiag : Java.Lang.Annotation.IAnnotation, Android.Runtime.IJavaObject, System.IDisposable {
	}
	public interface ISide : Java.Lang.Annotation.IAnnotation, Android.Runtime.IJavaObject, System.IDisposable {
	}
	public interface ITranspose : Java.Lang.Annotation.IAnnotation, Android.Runtime.IJavaObject, System.IDisposable {
	}
	public interface IUplo : Java.Lang.Annotation.IAnnotation, Android.Runtime.IJavaObject, System.IDisposable {
	}
}
</pre>

## Namespace Android.Security

### Type Changed: Android.Security.KeyChain

Added method:

<pre style='color: green'>
	public static void ChoosePrivateKeyAlias (Android.App.Activity activity, IKeyChainAliasCallback response, string[] keyTypes, Java.Security.IPrincipal[] issuers, string host, int port, string url, string alias);
</pre>

### Type Changed: Android.Security.KeyStoreParameter

Added property:

<pre style='color: green'>
	public Android.Content.Context Context { get; }
</pre>

### New Type Android.Security.EcIesParameterSpec

<pre style='color: green'>
public class EcIesParameterSpec : Java.Lang.Object, Java.Security.Spec.IAlgorithmParameterSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected EcIesParameterSpec (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const int PointFormatCompressed;
	public static const int PointFormatUncompressed;
	public static const int PointFormatUnspecified;
	// properties
	public static EcIesParameterSpec Default { get; }
	public virtual int DemCipherKeySize { get; }
	public virtual string DemCipherTransformation { get; }
	public virtual string DemMacAlgorithm { get; }
	public virtual int DemMacKeySize { get; }
	public virtual string KemKdfAlgorithm { get; }
	public virtual int KemPointFormat { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }

	// inner types
	public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected EcIesParameterSpec (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public EcIesParameterSpec ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual EcIesParameterSpec Build ();
		public virtual EcIesParameterSpec.Builder SetDemCipherKeySize (int sizeBits);
		public virtual EcIesParameterSpec.Builder SetDemCipherTransformation (string transformation);
		public virtual EcIesParameterSpec.Builder SetDemMacAlgorithm (string algorithm);
		public virtual EcIesParameterSpec.Builder SetDemMacKeySize (int sizeBits);
		public virtual EcIesParameterSpec.Builder SetKemKdfAlgorithm (string algorithm);
		public virtual EcIesParameterSpec.Builder SetKemPointFormat (int pointFormat);
	}
}
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
[Obsolete (]
	public virtual void OnSendDataSms (byte[] data, int subId, string destAddress, int destPort, CarrierMessagingService.IResultCallback callback);
	[Obsolete (]
	public virtual void OnSendMultipartTextSms (System.Collections.Generic.IList<string> parts, int subId, string destAddress, CarrierMessagingService.IResultCallback callback);
	[Obsolete (]
	public virtual void OnSendTextSms (string text, int subId, string destAddress, CarrierMessagingService.IResultCallback callback);
```

Added methods:

<pre style='color: green'>
	public virtual void OnSendDataSms (byte[] data, int subId, string destAddress, int destPort, int sendSmsFlag, CarrierMessagingService.IResultCallback callback);
	public virtual void OnSendMultipartTextSms (System.Collections.Generic.IList&lt;string&gt; parts, int subId, string destAddress, int sendSmsFlag, CarrierMessagingService.IResultCallback callback);
	public virtual void OnSendTextSms (string text, int subId, string destAddress, int sendSmsFlag, CarrierMessagingService.IResultCallback callback);
</pre>

### New Type Android.Service.Carrier.CarrierConfigService

<pre style='color: green'>
public abstract class CarrierConfigService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected CarrierConfigService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CarrierConfigService ();
	// fields
	public static const string ServiceInterface = "android.service.carrier.CarrierConfigService";
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Android.OS.IBinder OnBind (Android.Content.Intent p0);
	public virtual Android.OS.PersistableBundle OnLoadConfig (CarrierIdentifier id);
}
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

## Namespace Android.Service.Dreams

### Type Changed: Android.Service.Dreams.DreamService

Added methods:

<pre style='color: green'>
	public virtual bool OnSearchRequested (Android.Views.SearchEvent e);
	public virtual Android.Views.ActionMode OnWindowStartingActionMode (Android.Views.ActionMode.ICallback callback, int type);
</pre>

## Namespace Android.Service.Media

### Type Changed: Android.Service.Media.MediaBrowserService

Added method:

<pre style='color: green'>
	public virtual void GetMediaItem (string mediaId, MediaBrowserService.Result result);
</pre>

## Namespace Android.Service.Notification

### Type Changed: Android.Service.Notification.NotificationListenerService

Added fields:

<pre style='color: green'>
	public static const int InterruptionFilterAlarms;
	public static const int InterruptionFilterUnknown;
</pre>

Added method:

<pre style='color: green'>
	public void SetNotificationsShown (string[] keys);
</pre>

## Namespace Android.Service.Voice

### Type Changed: Android.Service.Voice.VoiceInteractionService

Added fields:

<pre style='color: green'>
	public static const int StartSourceAssistGesture;
	public static const int StartWithAssist;
</pre>

Added methods:

<pre style='color: green'>
	public virtual void OnLaunchVoiceAssistFromKeyguard ();
	public virtual void ShowSession (Android.OS.Bundle args, int flags);
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
	public virtual Android.Views.LayoutInflater LayoutInflater { get; }
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
	public virtual void Hide ();
	public virtual void HideWindow ();
	public void OnAbortVoice (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, string message, Android.OS.Bundle extras);
	public virtual void OnAbortVoice (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, Java.Lang.ICharSequence message, Android.OS.Bundle extras);
	public virtual void OnBackPressed ();
	public virtual void OnCancel (VoiceInteractionSession.Request request);
	public virtual void OnCommand (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, string command, Android.OS.Bundle extras);
	public void OnCompleteVoice (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, string message, Android.OS.Bundle extras);
	public virtual void OnCompleteVoice (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, Java.Lang.ICharSequence message, Android.OS.Bundle extras);
	public virtual void OnComputeInsets (VoiceInteractionSession.Insets outInsets);
	public virtual void OnConfigurationChanged (Android.Content.Res.Configuration newConfig);
	public void OnConfirm (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, string prompt, Android.OS.Bundle extras);
	public virtual void OnConfirm (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, Java.Lang.ICharSequence prompt, Android.OS.Bundle extras);
	public virtual void OnCreate (Android.OS.Bundle args, int showFlags);
	public virtual Android.Views.View OnCreateContentView ();
	public virtual bool[] OnGetSupportedCommands (VoiceInteractionSession.Caller caller, string[] commands);
	public virtual void OnHandleAssist (Android.OS.Bundle assistBundle);
	public virtual void OnHide ();
	public virtual void OnLowMemory ();
	public void OnPickOption (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, string prompt, Android.App.VoiceInteractor.PickOptionRequest.Option[] options, Android.OS.Bundle extras);
	public virtual void OnPickOption (VoiceInteractionSession.Caller caller, VoiceInteractionSession.Request request, Java.Lang.ICharSequence prompt, Android.App.VoiceInteractor.PickOptionRequest.Option[] options, Android.OS.Bundle extras);
	public virtual void OnShow (Android.OS.Bundle args, int showFlags);
	public virtual void OnTaskFinished (Android.Content.Intent intent, int taskId);
	public virtual void OnTaskStarted (Android.Content.Intent intent, int taskId);
	public virtual void OnTrimMemory (Android.Content.TrimMemory level);
	public virtual void SetKeepAwake (bool keepAwake);
	public virtual void SetTheme (int theme);
	public virtual void Show ();
	public virtual void ShowWindow ();
	public virtual void StartVoiceActivity (Android.Content.Intent intent);
</pre>

## Namespace Android.Speech

### Type Changed: Android.Speech.RecognizerIntent

Added field:

<pre style='color: green'>
	public static const string ExtraPreferOffline = "android.speech.extra.PREFER_OFFLINE";
</pre>

## Namespace Android.Speech.Tts

### Type Changed: Android.Speech.Tts.UtteranceProgressListener

Added method:

<pre style='color: green'>
	public virtual void OnStop (string utteranceId, bool isStarted);
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
	public static const string ActionIncomingCall = "android.telecom.action.INCOMING_CALL";
	public static const string ActionShowCallAccessibilitySettings = "android.telecom.action.SHOW_CALL_ACCESSIBILITY_SETTINGS";
	public static const string ActionShowRespondViaSmsSettings = "android.telecom.action.SHOW_RESPOND_VIA_SMS_SETTINGS";
	public static const string ExtraCallBackNumber = "android.telecom.extra.CALL_BACK_NUMBER";
	public static const string ExtraChangeDefaultDialerPackageName = "android.telecom.extra.CHANGE_DEFAULT_DIALER_PACKAGE_NAME";
	public static const string ExtraIncomingCallExtras = "android.telecom.extra.INCOMING_CALL_EXTRAS";
	public static const string ExtraOutgoingCallExtras = "android.telecom.extra.OUTGOING_CALL_EXTRAS";
	public static const string ExtraPhoneAccountHandle = "android.telecom.extra.PHONE_ACCOUNT_HANDLE";
	public static const string ExtraStartCallWithVideoState = "android.telecom.extra.START_CALL_WITH_VIDEO_STATE";
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
	public static const int StateActive;
	public static const int StateConnecting;
	public static const int StateDialing;
	public static const int StateDisconnected;
	public static const int StateDisconnecting;
	public static const int StateHolding;
	public static const int StateNew;
	public static const int StateRinging;
	public static const int StateSelectPhoneAccount;
	// properties
	public System.Collections.Generic.IList&lt;string&gt; CannedTextResponses { get; }
	public System.Collections.Generic.IList&lt;Call&gt; Children { get; }
	public System.Collections.Generic.IList&lt;Call&gt; ConferenceableCalls { get; }
	public Call Parent { get; }
	public string RemainingPostDialSequence { get; }
	public int State { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public InCallService.VideoCall VideoCall { get; }
	// methods
	public void Answer (int videoState);
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
		public virtual void OnStateChanged (Call call, int state);
		public virtual void OnVideoCallChanged (Call call, InCallService.VideoCall videoCall);
	}
	public class Details : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected Call (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// fields
		public static const int CapabilityCanPauseVideo;
		public static const int CapabilityDisconnectFromConference;
		public static const int CapabilityHold;
		public static const int CapabilityManageConference;
		public static const int CapabilityMergeConference;
		public static const int CapabilityMute;
		public static const int CapabilityRespondViaText;
		public static const int CapabilitySeparateFromConference;
		public static const int CapabilitySupportHold;
		public static const int CapabilitySupportsVtLocalBidirectional;
		public static const int CapabilitySupportsVtLocalRx;
		public static const int CapabilitySupportsVtLocalTx;
		public static const int CapabilitySupportsVtRemoteBidirectional;
		public static const int CapabilitySupportsVtRemoteRx;
		public static const int CapabilitySupportsVtRemoteTx;
		public static const int CapabilitySwapConference;
		public static const int PropertyConference;
		public static const int PropertyEmergencyCallbackMode;
		public static const int PropertyGenericConference;
		public static const int PropertyHighDefAudio;
		public static const int PropertyWifi;
		// properties
		public virtual PhoneAccountHandle AccountHandle { get; }
		public virtual int CallCapabilities { get; }
		public virtual string CallerDisplayName { get; }
		public virtual int CallerDisplayNamePresentation { get; }
		public virtual int CallProperties { get; }
		public long ConnectTimeMillis { get; }
		public virtual DisconnectCause DisconnectCause { get; }
		public virtual Android.OS.Bundle Extras { get; }
		public virtual GatewayInfo GatewayInfo { get; }
		public virtual int HandlePresentation { get; }
		public virtual StatusHints StatusHints { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public virtual int VideoState { get; }
		// methods
		public virtual bool Can (int capability);
		public static bool Can (int capabilities, int capability);
		public static string CapabilitiesToString (int capabilities);
		public virtual Android.Net.Uri GetHandle ();
		public virtual bool HasProperty (int property);
		public static bool HasProperty (int properties, int property);
		public static string PropertiesToString (int properties);
	}
}
</pre>

### New Type Android.Telecom.CallAudioState

<pre style='color: green'>
public sealed class CallAudioState : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public CallAudioState (bool muted, int route, int supportedRouteMask);
	// fields
	public static const int RouteBluetooth;
	public static const int RouteEarpiece;
	public static const int RouteSpeaker;
	public static const int RouteWiredHeadset;
	public static const int RouteWiredOrEarpiece;
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public bool IsMuted { get; }
	public int Route { get; }
	public int SupportedRouteMask { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static string AudioRouteToString (int route);
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

### New Type Android.Telecom.Conference

<pre style='color: green'>
public abstract class Conference : Java.Lang.Object, IConferenceable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected Conference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Conference (PhoneAccountHandle phoneAccount);
	// fields
	public static const long ConnectTimeNotSpecified;
	// properties
	public CallAudioState CallAudioState { get; }
	public System.Collections.Generic.IList&lt;Connection&gt; ConferenceableConnections { get; set; }
	public int ConnectionCapabilities { get; set; }
	public System.Collections.Generic.IList&lt;Connection&gt; Connections { get; }
	public long ConnectionTime { get; set; }
	public DisconnectCause DisconnectCause { get; }
	public PhoneAccountHandle PhoneAccountHandle { get; }
	public int State { get; }
	public StatusHints StatusHints { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual Connection.VideoProvider VideoProvider { get; }
	public virtual int VideoState { get; }
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
	public void SetDisconnected (DisconnectCause disconnectCause);
	public void SetOnHold ();
	public void SetVideoProvider (Connection c, Connection.VideoProvider videoProvider);
	public void SetVideoState (Connection c, int videoState);
}
</pre>

### New Type Android.Telecom.Connection

<pre style='color: green'>
public abstract class Connection : Java.Lang.Object, IConferenceable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected Connection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Connection ();
	// fields
	public static const int CapabilityCanPauseVideo;
	public static const int CapabilityCanUpgradeToVideo;
	public static const int CapabilityDisconnectFromConference;
	public static const int CapabilityHold;
	public static const int CapabilityManageConference;
	public static const int CapabilityMergeConference;
	public static const int CapabilityMute;
	public static const int CapabilityRespondViaText;
	public static const int CapabilitySeparateFromConference;
	public static const int CapabilitySupportHold;
	public static const int CapabilitySupportsVtLocalBidirectional;
	public static const int CapabilitySupportsVtLocalRx;
	public static const int CapabilitySupportsVtLocalTx;
	public static const int CapabilitySupportsVtRemoteBidirectional;
	public static const int CapabilitySupportsVtRemoteRx;
	public static const int CapabilitySupportsVtRemoteTx;
	public static const int CapabilitySwapConference;
	public static const int StateActive;
	public static const int StateDialing;
	public static const int StateDisconnected;
	public static const int StateHolding;
	public static const int StateInitializing;
	public static const int StateNew;
	public static const int StateRinging;
	// properties
	public Android.Net.Uri Address { get; }
	public int AddressPresentation { get; }
	public bool AudioModeIsVoip { get; set; }
	public CallAudioState CallAudioState { get; }
	public string CallerDisplayName { get; }
	public int CallerDisplayNamePresentation { get; }
	public Conference Conference { get; }
	public System.Collections.Generic.IList&lt;IConferenceable&gt; Conferenceables { get; set; }
	public int ConnectionCapabilities { get; set; }
	public DisconnectCause DisconnectCause { get; }
	public bool RingbackRequested { get; set; }
	public int State { get; }
	public StatusHints StatusHints { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static string CapabilitiesToString (int capabilities);
	public static Connection CreateCanceledConnection ();
	public static Connection CreateFailedConnection (DisconnectCause disconnectCause);
	public void Destroy ();
	public Connection.VideoProvider GetVideoProvider ();
	public virtual void OnAbort ();
	public virtual void OnAnswer ();
	public virtual void OnAnswer (int videoState);
	public virtual void OnCallAudioStateChanged (CallAudioState state);
	public virtual void OnDisconnect ();
	public virtual void OnHold ();
	public virtual void OnPlayDtmfTone (char c);
	public virtual void OnPostDialContinue (bool proceed);
	public virtual void OnReject ();
	public virtual void OnSeparate ();
	public virtual void OnStateChanged (int state);
	public virtual void OnStopDtmfTone ();
	public virtual void OnUnhold ();
	public void SetActive ();
	public void SetAddress (Android.Net.Uri address, int presentation);
	public void SetCallerDisplayName (string callerDisplayName, int presentation);
	public void SetConferenceableConnections (System.Collections.Generic.IList&lt;Connection&gt; conferenceableConnections);
	public void SetConnectionService (ConnectionService connectionService);
	public void SetDialing ();
	public void SetDisconnected (DisconnectCause disconnectCause);
	public void SetInitialized ();
	public void SetInitializing ();
	public void SetNextPostDialChar (char nextChar);
	public void SetOnHold ();
	public void SetPostDialWait (string remaining);
	public void SetRinging ();
	public void SetVideoProvider (Connection.VideoProvider videoProvider);
	public void SetVideoState (int videoState);
	public static string StateToString (int state);

	// inner types
	public abstract class VideoProvider : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected Connection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public Connection ();
		// fields
		public static const int SessionEventCameraFailure;
		public static const int SessionEventCameraReady;
		public static const int SessionEventRxPause;
		public static const int SessionEventRxResume;
		public static const int SessionEventTxStart;
		public static const int SessionEventTxStop;
		public static const int SessionModifyRequestFail;
		public static const int SessionModifyRequestInvalid;
		public static const int SessionModifyRequestRejectedByRemote;
		public static const int SessionModifyRequestSuccess;
		public static const int SessionModifyRequestTimedOut;
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void ChangeCameraCapabilities (VideoProfile.CameraCapabilities cameraCapabilities);
		public virtual void ChangePeerDimensions (int width, int height);
		public virtual void ChangeVideoQuality (int videoQuality);
		public virtual void HandleCallSessionEvent (int e);
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
		public virtual void ReceiveSessionModifyResponse (int status, VideoProfile requestedProfile, VideoProfile responseProfile);
		public virtual void SetCallDataUsage (long dataUsage);
	}
}
</pre>

### New Type Android.Telecom.ConnectionRequest

<pre style='color: green'>
public sealed class ConnectionRequest : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public ConnectionRequest (PhoneAccountHandle accountHandle, Android.Net.Uri handle, Android.OS.Bundle extras);
	public ConnectionRequest (PhoneAccountHandle accountHandle, Android.Net.Uri handle, Android.OS.Bundle extras, int videoState);
	// properties
	public PhoneAccountHandle AccountHandle { get; }
	public Android.Net.Uri Address { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public Android.OS.Bundle Extras { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int VideoState { get; }
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

### New Type Android.Telecom.DisconnectCause

<pre style='color: green'>
public sealed class DisconnectCause : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public DisconnectCause (int code, Java.Lang.ICharSequence label, Java.Lang.ICharSequence description, string reason, int toneToPlay);
	public DisconnectCause (int code, string label, string description, string reason, int toneToPlay);
	public DisconnectCause (int code, Java.Lang.ICharSequence label, Java.Lang.ICharSequence description, string reason);
	public DisconnectCause (int code, string label, string description, string reason);
	public DisconnectCause (int code, string reason);
	public DisconnectCause (int code);
	// fields
	public static const int Busy;
	public static const int Canceled;
	public static const int ConnectionManagerNotSupported;
	public static const int Error;
	public static const int Local;
	public static const int Missed;
	public static const int Other;
	public static const int Rejected;
	public static const int Remote;
	public static const int Restricted;
	public static const int Unknown;
	// properties
	public int Code { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public string Description { get; }
	public Java.Lang.ICharSequence DescriptionFormatted { get; }
	public string Label { get; }
	public Java.Lang.ICharSequence LabelFormatted { get; }
	public string Reason { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int Tone { get; }
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

### New Type Android.Telecom.IConferenceable

<pre style='color: green'>
public interface IConferenceable : Android.Runtime.IJavaObject, System.IDisposable {
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
	public void SetAudioRoute (int route);
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
			public virtual void OnCallSessionEvent (int e);
			public virtual void OnCameraCapabilitiesChanged (VideoProfile.CameraCapabilities cameraCapabilities);
			public virtual void OnPeerDimensionsChanged (int width, int height);
			public virtual void OnSessionModifyRequestReceived (VideoProfile videoProfile);
			public virtual void OnSessionModifyResponseReceived (int status, VideoProfile requestedProfile, VideoProfile responseProfile);
			public virtual void OnVideoQualityChanged (int videoQuality);
		}
	}
}
</pre>

### New Type Android.Telecom.PhoneAccount

<pre style='color: green'>
public sealed class PhoneAccount : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields
	public static const int CapabilityCallProvider;
	public static const int CapabilityConnectionManager;
	public static const int CapabilityPlaceEmergencyCalls;
	public static const int CapabilitySimSubscription;
	public static const int CapabilityVideoCalling;
	public static const int NoHighlightColor;
	public static const int NoResourceId;
	public static const string SchemeSip = "sip";
	public static const string SchemeTel = "tel";
	public static const string SchemeVoicemail = "voicemail";
	// properties
	public PhoneAccountHandle AccountHandle { get; }
	public Android.Net.Uri Address { get; }
	public int Capabilities { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public int HighlightColor { get; }
	public Android.Graphics.Drawables.Icon Icon { get; }
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
	public bool HasCapabilities (int capability);
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
	public int ConnectionCapabilities { get; }
	public System.Collections.Generic.IList&lt;RemoteConnection&gt; Connections { get; }
	public DisconnectCause DisconnectCause { get; }
	public int State { get; }
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
		public virtual void OnConnectionCapabilitiesChanged (RemoteConference conference, int connectionCapabilities);
		public virtual void OnConnectionRemoved (RemoteConference conference, RemoteConnection connection);
		public virtual void OnDestroyed (RemoteConference conference);
		public virtual void OnDisconnected (RemoteConference conference, DisconnectCause disconnectCause);
		public virtual void OnStateChanged (RemoteConference conference, int oldState, int newState);
	}
}
</pre>

### New Type Android.Telecom.RemoteConnection

<pre style='color: green'>
public sealed class RemoteConnection : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public Android.Net.Uri Address { get; }
	public int AddressPresentation { get; }
	public string CallerDisplayName { get; }
	public Java.Lang.ICharSequence CallerDisplayNameFormatted { get; }
	public int CallerDisplayNamePresentation { get; }
	public RemoteConference Conference { get; }
	public System.Collections.Generic.IList&lt;RemoteConnection&gt; ConferenceableConnections { get; }
	public int ConnectionCapabilities { get; }
	public DisconnectCause DisconnectCause { get; }
	public bool IsRingbackRequested { get; }
	public bool IsVoipAudioMode { get; }
	public int State { get; }
	public StatusHints StatusHints { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void Abort ();
	public void Answer ();
	public void Disconnect ();
	public void Hold ();
	public void PlayDtmfTone (char digit);
	public void PostDialContinue (bool proceed);
	public void RegisterCallback (RemoteConnection.Callback callback, Android.OS.Handler handler);
	public void RegisterCallback (RemoteConnection.Callback callback);
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
		public virtual void OnAddressChanged (RemoteConnection connection, Android.Net.Uri address, int presentation);
		public virtual void OnCallerDisplayNameChanged (RemoteConnection connection, string callerDisplayName, int presentation);
		public virtual void OnConferenceableConnectionsChanged (RemoteConnection connection, System.Collections.Generic.IList&lt;RemoteConnection&gt; conferenceableConnections);
		public virtual void OnConferenceChanged (RemoteConnection connection, RemoteConference conference);
		public virtual void OnConnectionCapabilitiesChanged (RemoteConnection connection, int connectionCapabilities);
		public virtual void OnDestroyed (RemoteConnection connection);
		public virtual void OnDisconnected (RemoteConnection connection, DisconnectCause disconnectCause);
		public virtual void OnPostDialChar (RemoteConnection connection, char nextChar);
		public virtual void OnPostDialWait (RemoteConnection connection, string remainingPostDialSequence);
		public virtual void OnRingbackRequested (RemoteConnection connection, bool ringback);
		public virtual void OnStateChanged (RemoteConnection connection, int state);
		public virtual void OnStatusHintsChanged (RemoteConnection connection, StatusHints statusHints);
		public virtual void OnVoipAudioChanged (RemoteConnection connection, bool isVoip);
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
	public VideoProfile (int videoState);
	public VideoProfile (int videoState, int quality);
	// fields
	public static const int QualityDefault;
	public static const int QualityHigh;
	public static const int QualityLow;
	public static const int QualityMedium;
	public static const int StateAudioOnly;
	public static const int StateBidirectional;
	public static const int StatePaused;
	public static const int StateRxEnabled;
	public static const int StateTxEnabled;
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual int Quality { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual int GetVideoState ();
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
	public class VideoState : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected VideoProfile (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public static bool IsAudioOnly (int videoState);
		public static bool IsBidirectional (int videoState);
		public static bool IsPaused (int videoState);
		public static bool IsReceptionEnabled (int videoState);
		public static bool IsTransmissionEnabled (int videoState);
		public static string VideoStateToString (int videoState);
	}
}
</pre>

## Namespace Android.Telephony

### Type Changed: Android.Telephony.PhoneNumberUtils

Added methods:

<pre style='color: green'>
	public static void AddPhoneTtsSpan (Android.Text.ISpannable s, int start, int end);
	public static string FormatNumberToRFC3966 (string phoneNumber, string defaultCountryIso);
	public static Android.Text.Style.TtsSpan GetPhoneTtsSpan (string phoneNumberString);
	public static string GetPhoneTtsSpannable (string phoneNumber);
	public static Java.Lang.ICharSequence GetPhoneTtsSpannableFormatted (Java.Lang.ICharSequence phoneNumber);
</pre>

### Type Changed: Android.Telephony.SignalStrength

Added property:

<pre style='color: green'>
	public virtual int Level { get; }
</pre>

### Type Changed: Android.Telephony.SmsMessage

Obsoleted methods:

```
[Obsolete (]
	public static SmsMessage CreateFromPdu (byte[] pdu);
```

Added method:

<pre style='color: green'>
	public static SmsMessage CreateFromPdu (byte[] pdu, string format);
</pre>

### Type Changed: Android.Telephony.TelephonyManager

Added field:

<pre style='color: green'>
	public static const string ActionEmergencyAssistance = "android.telephony.action.EMERGENCY_ASSISTANCE";
</pre>

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
	public virtual void NotifyCarrierNetworkChange (bool active);
</pre>

### New Type Android.Telephony.CarrierConfigManager

<pre style='color: green'>
public class CarrierConfigManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CarrierConfigManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const string ActionCarrierConfigChanged = "android.telephony.action.CARRIER_CONFIG_CHANGED";
	public static const string BoolAdditionalCallSetting = "bool_additional_call_setting";
	public static const string BoolAllowEmergencyNumbersInCallLog = "bool_allow_emergency_numbers_in_call_log";
	public static const string BoolAllowLocalDtmfTones = "bool_allow_local_dtmf_tones";
	public static const string BoolApnExpand = "bool_apn_expand";
	public static const string BoolAutoRetryEnabled = "bool_auto_retry_enabled";
	public static const string BoolCarrierSettingsEnable = "bool_carrier_settings_enable";
	public static const string BoolCarrierVolteAvailable = "bool_carrier_volte_available";
	public static const string BoolCarrierVolteProvisioned = "bool_carrier_volte_provisioned";
	public static const string BoolCarrierVolteTtySupported = "bool_carrier_volte_tty_supported";
	public static const string BoolDisableCdmaActivationCode = "bool_disable_cdma_activation_code";
	public static const string BoolDtmfTypeEnabled = "bool_dtmf_type_enabled";
	public static const string BoolEnableDialerKeyVibration = "bool_enable_dialer_key_vibration";
	public static const string BoolHasInCallNoiseSuppression = "bool_has_in_call_noise_suppression";
	public static const string BoolHideCarrierNetworkSettings = "bool_hide_carrier_network_settings";
	public static const string BoolIgnoreSimNetworkLockedEvents = "bool_ignore_sim_network_locked_events";
	public static const string BoolOperatorSelectionExpand = "bool_operator_selection_expand";
	public static const string BoolPrefer2g = "bool_prefer_2g";
	public static const string BoolShowApnSettingCdma = "bool_show_apn_setting_cdma";
	public static const string BoolShowCdmaChoices = "bool_show_cdma_choices";
	public static const string BoolShowOnscreenDialButton = "bool_show_onscreen_dial_button";
	public static const string BoolSimNetworkUnlockAllowDismiss = "bool_sim_network_unlock_allow_dismiss";
	public static const string BoolSupportPauseImsVideoCalls = "bool_support_pause_ims_video_calls";
	public static const string BoolSupportSwapAfterMerge = "bool_support_swap_after_merge";
	public static const string BoolUseHfaForProvisioning = "bool_use_hfa_for_provisioning";
	public static const string BoolUseOtaspForProvisioning = "bool_use_otasp_for_provisioning";
	public static const string BoolVoicemailNotificationPersistent = "bool_voicemail_notification_persistent";
	public static const string BoolVoicePrivacyDisable = "bool_voice_privacy_disable";
	public static const string BoolWorldPhone = "bool_world_phone";
	public static const string IntVolteReplacementRat = "int_volte_replacement_rat";
	// properties
	public virtual Android.OS.PersistableBundle Config { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.OS.PersistableBundle GetConfigForSubId (int subId);
	public virtual void ReloadCarrierConfigForSubId (int subId);
}
</pre>

## Namespace Android.Test.Mock

### Type Changed: Android.Test.Mock.MockContext

Added methods:

<pre style='color: green'>
	public override int CheckSelfPermission (string permission);
	public virtual string GetSystemServiceName (Java.Lang.Class serviceClass);
</pre>

### Type Changed: Android.Test.Mock.MockCursor

Modified properties:

```
public virtual Android.OS.Bundle Extras { get; set; }
```

Obsoleted methods:

```
[Obsolete (]
	public virtual void Deactivate ();
	[Obsolete (]
	public virtual bool Requery ();
```

### Type Changed: Android.Test.Mock.MockPackageManager

Added methods:

<pre style='color: green'>
	public virtual System.Collections.Generic.IList&lt;Android.Content.IntentFilter&gt; GetAllIntentFilters (string packageName);
	public virtual string GetDefaultBrowserPackageName (int userId);
	public virtual bool SetDefaultBrowserPackageName (string packageName, int userId);
</pre>

## Namespace Android.Text

### Type Changed: Android.Text.Layout

Added fields:

<pre style='color: green'>
	public static const int BreakStrategyBalanced;
	public static const int BreakStrategyHighQuality;
	public static const int BreakStrategySimple;
	public static const int HyphenationFrequencyFull;
	public static const int HyphenationFrequencyNone;
	public static const int HyphenationFrequencyNormal;
</pre>

### Type Changed: Android.Text.SpannableStringBuilder

Added property:

<pre style='color: green'>
	public virtual int TextWatcherDepth { get; }
</pre>

## Namespace Android.Transitions

### Type Changed: Android.Transitions.Transition

Added method:

<pre style='color: green'>
	protected virtual bool AreValuesChanged (TransitionValues oldValues, TransitionValues newValues);
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

### Type Changed: Android.Util.EventLog

Added methods:

<pre style='color: green'>
	public static int WriteEvent (int tag, float value);
	public static System.Threading.Tasks.Task&lt;int&gt; WriteEventAsync (int tag, float value);
</pre>

## Namespace Android.Views

### Type Changed: Android.Views.ActionMode

Added fields:

<pre style='color: green'>
	public static const int TypeFloating;
	public static const int TypePrimary;
</pre>

Added property:

<pre style='color: green'>
	public virtual int Type { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void InvalidateContentRect ();
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

Obsoleted methods:

```
[Obsolete (]
	public virtual float[] GetSupportedRefreshRates ();
```

Added methods:

<pre style='color: green'>
	public virtual Display.Mode GetMode ();
	public virtual Display.Mode[] GetSupportedModes ();
</pre>

### Type Changed: Android.Views.GestureDetector

Added event:

<pre style='color: green'>
	public event System.EventHandler&lt;GestureDetector.StylusButtonPressEventArgs&gt; StylusButtonPress;
</pre>

Added method:

<pre style='color: green'>
	public virtual void SetOnStylusButtonPressListener (GestureDetector.IOnStylusButtonPressListener onStylusButtonPressListener);
</pre>

### Type Changed: Android.Views.GestureDetector.SimpleOnGestureListener

Added method:

<pre style='color: green'>
	public virtual bool OnStylusButtonPress (MotionEvent e);
</pre>

### New Type Android.Views.IOnStylusButtonPressListener

<pre style='color: green'>
public interface IOnStylusButtonPressListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual bool OnStylusButtonPress (MotionEvent e);
}
</pre>

### New Type Android.Views.StylusButtonPressEventArgs

<pre style='color: green'>
public class StylusButtonPressEventArgs : System.EventArgs {
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
	public static const int StylusButtonPress;
</pre>

### Type Changed: Android.Views.IMenuItem

Added methods:

<pre style='color: green'>
	public virtual IMenuItem SetIconTintList (Android.Content.Res.ColorStateList tint);
	public virtual IMenuItem SetIconTintMode (Android.Graphics.PorterDuff.Mode tintMode);
</pre>

### Type Changed: Android.Views.InputDevice

Added property:

<pre style='color: green'>
	public bool HasMic { get; }
</pre>

### Type Changed: Android.Views.IViewParent

Added method:

<pre style='color: green'>
	public virtual ActionMode StartActionModeForChild (View originalView, ActionMode.ICallback callback, int type);
</pre>

### Type Changed: Android.Views.KeyEvent

Added fields:

<pre style='color: green'>
	public static const int KeycodeNavigateIn;
	public static const int KeycodeNavigateNext;
	public static const int KeycodeNavigateOut;
	public static const int KeycodeNavigatePrevious;
</pre>

### Type Changed: Android.Views.MotionEvent

Added property:

<pre style='color: green'>
	public bool IsStylusButtonPressed { get; }
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

### Type Changed: Android.Views.View

Added fields:

<pre style='color: green'>
	public static const int ScrollIndicatorBottom;
	public static const int ScrollIndicatorEnd;
	public static const int ScrollIndicatorLeft;
	public static const int ScrollIndicatorRight;
	public static const int ScrollIndicatorStart;
	public static const int ScrollIndicatorTop;
	public static const int SystemUiFlagLightStatusBar;
	public static const int TextDirectionFirstStrongLtr;
	public static const int TextDirectionFirstStrongRtl;
</pre>

Added properties:

<pre style='color: green'>
	public string AccessibilityClassName { get; }
	public virtual Java.Lang.ICharSequence AccessibilityClassNameFormatted { get; }
	public virtual int BackgroundColor { get; }
	public virtual Android.Graphics.Drawables.Drawable Foreground { get; set; }
	public virtual GravityFlags ForegroundGravity { get; }
	public virtual Android.Content.Res.ColorStateList ForegroundTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ForegroundTintMode { get; set; }
	public virtual WindowInsets RootWindowInsets { get; }
	public virtual int ScrollIndicators { get; set; }
	public virtual bool StylusButtonPressable { get; set; }
</pre>

Added events:

<pre style='color: green'>
	public event System.EventHandler&lt;View.ScrollChangeEventArgs&gt; ScrollChange;
	public event System.EventHandler&lt;View.StylusButtonPressEventArgs&gt; StylusButtonPress;
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DispatchProvideStructure (ViewStructure structure);
	public virtual bool GetClipBounds (Android.Graphics.Rect outRect);
	public virtual void OnDrawForeground (Android.Graphics.Canvas canvas);
	public virtual void OnProvideStructure (ViewStructure structure);
	public virtual void OnProvideVirtualStructure (ViewStructure structure);
	public virtual bool PerformStylusButtonPress ();
	public virtual void SetForegroundGravity (GravityFlags gravity);
	public virtual void SetOnScrollChangeListener (View.IOnScrollChangeListener l);
	public virtual void SetOnStylusButtonPressListener (View.IOnStylusButtonPressListener l);
	public virtual void SetScrollIndicators (int indicators, int mask);
	public virtual ActionMode StartActionMode (ActionMode.ICallback callback, int type);
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

### New Type Android.Views.IOnStylusButtonPressListener

<pre style='color: green'>
public interface IOnStylusButtonPressListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual bool OnStylusButtonPress (View v);
}
</pre>

### New Type Android.Views.StylusButtonPressEventArgs

<pre style='color: green'>
public class StylusButtonPressEventArgs : System.EventArgs {
	// constructors
	public View (bool handled, View v);
	// properties
	public bool Handled { get; set; }
	public View V { get; }
}
</pre>

### Type Changed: Android.Views.ViewGroup

Obsoleted properties:

```
[Obsolete (]
	public virtual bool AlwaysDrawnWithCacheEnabled { get; set; }
	[Obsolete (]
	public virtual bool AnimationCacheEnabled { get; set; }
	[Obsolete (]
	protected virtual bool ChildrenDrawnWithCacheEnabled { get; set; }
```

Added method:

<pre style='color: green'>
	public virtual ActionMode StartActionModeForChild (View originalView, ActionMode.ICallback callback, int type);
</pre>

### Type Changed: Android.Views.Window

### Type Changed: Android.Views.Window.ICallback

Added methods:

<pre style='color: green'>
	public virtual bool OnSearchRequested (SearchEvent searchEvent);
	public virtual ActionMode OnWindowStartingActionMode (ActionMode.ICallback callback, int type);
</pre>

### Type Changed: Android.Views.WindowManagerLayoutParams

Added field:

<pre style='color: green'>
	public static const int TypeApplicationAboveSubPanel;
</pre>

Added property:

<pre style='color: green'>
	public int PreferredDisplayModeId { get; set; }
</pre>

### New Type Android.Views.SearchEvent

<pre style='color: green'>
public class SearchEvent : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected SearchEvent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual InputDevice InputDevice { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Views.ViewAssistStructure

<pre style='color: green'>
public abstract class ViewAssistStructure : Android.Views.ViewStructure, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ViewAssistStructure (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ViewAssistStructure ();
	// properties
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
	public virtual void AsyncCommit ();
	public virtual ViewAssistStructure AsyncNewChild (int index);
	public virtual ViewAssistStructure NewChild (int index);
	public virtual void SetAccessibilityFocused (bool state);
	public virtual void SetActivated (bool state);
	public virtual void SetCheckable (bool state);
	public virtual void SetChecked (bool state);
	public virtual void SetClassName (string className);
	public virtual void SetClickable (bool state);
	public virtual void SetContentDescription (Java.Lang.ICharSequence contentDescription);
	public void SetContentDescription (string contentDescription);
	public virtual void SetDimens (int left, int top, int scrollX, int scrollY, int width, int height);
	public virtual void SetEnabled (bool state);
	public virtual void SetFocusable (bool state);
	public virtual void SetFocused (bool state);
	public virtual void SetId (int id, string packageName, string typeName, string entryName);
	public virtual void SetLongClickable (bool state);
	public virtual void SetSelected (bool state);
	public virtual void SetStylusButtonPressable (bool state);
	public virtual void SetText (Java.Lang.ICharSequence text, int selectionStart, int selectionEnd);
	public void SetText (string text, int selectionStart, int selectionEnd);
	public virtual void SetTextPaint (Android.Text.TextPaint paint);
	public virtual void SetVisibility (int visibility);
}
</pre>

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityEvent

Added field:

<pre style='color: green'>
	public static const int TypeViewStylusButtonPressed;
</pre>

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo

Added fields:

<pre style='color: green'>
	public static const string ActionArgumentColumnInt = "android.view.accessibility.action.ARGUMENT_COLUMN_INT";
	public static const string ActionArgumentRowInt = "android.view.accessibility.action.ARGUMENT_ROW_INT";
</pre>

Added property:

<pre style='color: green'>
	public virtual bool StylusButtonPressable { get; set; }
</pre>

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo.AccessibilityAction

Added properties:

<pre style='color: green'>
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollDown { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollLeft { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollRight { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollToPosition { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollUp { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionShowOnScreen { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionStylusButtonPress { get; }
</pre>

## Namespace Android.Webkit

### Type Changed: Android.Webkit.WebResourceResponse


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Webkit.WebResourceResponseBase</span>

### Type Changed: Android.Webkit.WebSettings

Added property:

<pre style='color: green'>
	public virtual bool OffscreenPreRaster { get; set; }
</pre>

### Type Changed: Android.Webkit.WebView

Added methods:

<pre style='color: green'>
	public virtual WebMessagePort[] CreateWebMessageChannel ();
	public virtual void PostMessageToMainFrame (WebMessage message, Android.Net.Uri targetOrigin);
	public virtual void PostVisualStateCallback (long requestId, WebView.VisualStateCallback callback);
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
[Obsolete (]
	public virtual void OnReceivedError (WebView view, ClientError errorCode, string description, string failingUrl);
```

Added methods:

<pre style='color: green'>
	public virtual void OnPageCommitVisible (WebView view, string url);
	public virtual void OnReceivedError (WebView view, IWebResourceRequest request, WebResourceError error);
	public virtual void OnReceivedHttpError (WebView view, IWebResourceRequest request, WebResourceResponseBase errorResponse);
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
	public virtual int ErrorCode { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

### New Type Android.Webkit.WebResourceResponseBase

<pre style='color: green'>
public abstract class WebResourceResponseBase : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WebResourceResponseBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WebResourceResponseBase ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
</pre>

## Namespace Android.Widget

### Type Changed: Android.Widget.ActionMenuView

Added methods:

<pre style='color: green'>
	public virtual void SetOverflowTintList (Android.Content.Res.ColorStateList tint);
	public virtual void SetOverflowTintMode (Android.Graphics.PorterDuff.Mode tintMode);
</pre>

### Type Changed: Android.Widget.ArrayAdapter

Added property:

<pre style='color: green'>
	public virtual Android.Content.Res.Resources.Theme DropDownViewTheme { get; set; }
</pre>

### Type Changed: Android.Widget.CalendarView

Obsoleted properties:

```
[Obsolete (]
	public virtual Android.Graphics.Color FocusedMonthDateColor { get; set; }
	[Obsolete (]
	public virtual Android.Graphics.Drawables.Drawable SelectedDateVerticalBar { get; set; }
	[Obsolete (]
	public virtual Android.Graphics.Color SelectedWeekBackgroundColor { get; set; }
	[Obsolete (]
	public virtual int ShownWeekCount { get; set; }
	[Obsolete (]
	public virtual Android.Graphics.Color UnfocusedMonthDateColor { get; set; }
	[Obsolete (]
	public virtual Android.Graphics.Color WeekNumberColor { get; set; }
	[Obsolete (]
	public virtual Android.Graphics.Color WeekSeparatorLineColor { get; set; }
```

Obsoleted methods:

```
[Obsolete (]
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
	public virtual void SetWindowLayoutType (int layoutType);
</pre>

### Type Changed: Android.Widget.PopupMenu

Added property:

<pre style='color: green'>
	public virtual int Gravity { get; set; }
</pre>

### Type Changed: Android.Widget.PopupWindow

Added properties:

<pre style='color: green'>
	public virtual bool OverlapAnchor { get; set; }
	public virtual int WindowLayoutType { get; set; }
</pre>

Obsoleted methods:

```
[Obsolete (]
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
	public virtual int GetRule (int verb);
</pre>

### Type Changed: Android.Widget.RemoteViews

Added methods:

<pre style='color: green'>
	public virtual void SetIcon (int viewId, string methodName, Android.Graphics.Drawables.Icon value);
	public virtual void SetImageViewIcon (int viewId, Android.Graphics.Drawables.Icon icon);
</pre>

### Type Changed: Android.Widget.SimpleAdapter

Added property:

<pre style='color: green'>
	public virtual Android.Content.Res.Resources.Theme DropDownViewTheme { get; set; }
</pre>

### Type Changed: Android.Widget.Spinner

Added constructor:

<pre style='color: green'>
	public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes, SpinnerMode mode, Android.Content.Context popupContext);
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
	public virtual int BreakStrategy { get; set; }
	public virtual Android.Content.Res.ColorStateList CompoundDrawableTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode CompoundDrawableTintMode { get; set; }
	public virtual int HyphenationFrequency { get; set; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void SetTextAppearance (Android.Content.Context context, int resId);
```

Modified methods:

```
public virtual void SetTextAppearance (Android.Content.Context context, int resid resId)
```

Added methods:

<pre style='color: green'>
	public virtual int[] GetLeftIndents ();
	public virtual int[] GetRightIndents ();
	public virtual void SetIndents (int[] leftIndents, int[] rightIndents);
	public virtual void SetTextAppearance (int resId);
</pre>

### Type Changed: Android.Widget.TimePicker

Obsoleted properties:

```
[Obsolete (]
	public virtual Java.Lang.Integer CurrentHour { get; set; }
	[Obsolete (]
	public virtual Java.Lang.Integer CurrentMinute { get; set; }
```

Added properties:

<pre style='color: green'>
	public virtual int Hour { get; set; }
	public virtual int Minute { get; set; }
</pre>

### Type Changed: Android.Widget.Toolbar

Added methods:

<pre style='color: green'>
	public virtual void SetNavigationTintList (Android.Content.Res.ColorStateList tint);
	public virtual void SetNavigationTintMode (Android.Graphics.PorterDuff.Mode tintMode);
	public virtual void SetOverflowTintList (Android.Content.Res.ColorStateList tint);
	public virtual void SetOverflowTintMode (Android.Graphics.PorterDuff.Mode tintMode);
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

## New Namespace Android.Hardware.Fingerprint

### New Type Android.Hardware.Fingerprint.Fingerprint

<pre style='color: green'>
public sealed class Fingerprint : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public Fingerprint (Java.Lang.ICharSequence p0, int p1, int p2, long p3);
	public Fingerprint (string p0, int p1, int p2, long p3);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public string Name { get; }
	public Java.Lang.ICharSequence NameFormatted { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel p0, Android.OS.ParcelableWriteFlags p1);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Hardware.Fingerprint.FingerprintManager

<pre style='color: green'>
public class FingerprintManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected FingerprintManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const int FingerprintAcquiredGood;
	public static const int FingerprintAcquiredImagerDirty;
	public static const int FingerprintAcquiredInsufficient;
	public static const int FingerprintAcquiredPartial;
	public static const int FingerprintAcquiredTooFast;
	public static const int FingerprintAcquiredTooSlow;
	public static const int FingerprintAcquiredVendorBase;
	public static const int FingerprintErrorCanceled;
	public static const int FingerprintErrorHwUnavailable;
	public static const int FingerprintErrorLockout;
	public static const int FingerprintErrorNoSpace;
	public static const int FingerprintErrorTimeout;
	public static const int FingerprintErrorUnableToProcess;
	public static const int FingerprintErrorVendorBase;
	// properties
	public virtual bool HasEnrolledFingerprints { get; }
	public virtual bool IsHardwareDetected { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Authenticate (FingerprintManager.CryptoObject crypto, Android.OS.CancellationSignal cancel, FingerprintManager.AuthenticationCallback callback, int flags);

	// inner types
	public abstract class AuthenticationCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected FingerprintManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public FingerprintManager ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnAuthenticationError (int errMsgId, Java.Lang.ICharSequence errString);
		public void OnAuthenticationError (int errMsgId, string errString);
		public virtual void OnAuthenticationFailed ();
		public virtual void OnAuthenticationHelp (int helpMsgId, Java.Lang.ICharSequence helpString);
		public void OnAuthenticationHelp (int helpMsgId, string helpString);
		public virtual void OnAuthenticationSucceeded (FingerprintManager.AuthenticationResult result);
	}
	public sealed class AuthenticationResult : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public FingerprintManager (FingerprintManager.CryptoObject crypto, Fingerprint fingerprint);
		// properties
		public FingerprintManager.CryptoObject CryptoObject { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
	public class CryptoObject : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected FingerprintManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public FingerprintManager (Javax.Crypto.Mac mac);
		public FingerprintManager (Javax.Crypto.Cipher cipher);
		public FingerprintManager (Java.Security.Signature signature);
		// properties
		public virtual Javax.Crypto.Cipher Cipher { get; }
		public virtual Javax.Crypto.Mac Mac { get; }
		public virtual Java.Security.Signature Signature { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
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
	public static const int TypeBluetooth;
	public static const int TypeUsb;
	public static const int TypeVirtual;
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public int Id { get; }
	public int InputPortCount { get; }
	public bool IsPrivate { get; }
	public int OutputPortCount { get; }
	public Android.OS.Bundle Properties { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int Type { get; }
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
		// fields
		public static const int TypeInput;
		public static const int TypeOutput;
		// properties
		public string Name { get; }
		public int PortNumber { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public int Type { get; }
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
	public bool IsEncryptionAtRestRequired { get; }
	public bool IsRandomizedEncryptionRequired { get; }
	public bool IsUserAuthenticationRequired { get; }
	public int KeySize { get; }
	public string KeystoreAlias { get; }
	public Java.Util.Date KeyValidityForConsumptionEnd { get; }
	public Java.Util.Date KeyValidityForOriginationEnd { get; }
	public Java.Util.Date KeyValidityStart { get; }
	public int Purposes { get; }
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
		public KeyGenParameterSpec (string keystoreAlias, int purposes);
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
		public KeyGenParameterSpec.Builder SetEncryptionAtRestRequired (bool required);
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
	public virtual int Origin { get; }
	public virtual int Purposes { get; }
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
	public static const int OriginGenerated;
	public static const int OriginImported;
	public static const int OriginUnknown;
	public static const int PurposeDecrypt;
	public static const int PurposeEncrypt;
	public static const int PurposeSign;
	public static const int PurposeVerify;
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
	public bool IsEncryptionAtRestRequired { get; }
	public bool IsRandomizedEncryptionRequired { get; }
	public bool IsUserAuthenticationRequired { get; }
	public Java.Util.Date KeyValidityForConsumptionEnd { get; }
	public Java.Util.Date KeyValidityForOriginationEnd { get; }
	public Java.Util.Date KeyValidityStart { get; }
	public int Purposes { get; }
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
		public KeyProtection (int purposes);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public KeyProtection Build ();
		public KeyProtection.Builder SetBlockModes (string[] blockModes);
		public KeyProtection.Builder SetDigests (string[] digests);
		public KeyProtection.Builder SetEncryptionAtRestRequired (bool required);
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
	public ChooserTarget (Java.Lang.ICharSequence title, Android.Graphics.Drawables.Icon icon, float score, Android.App.PendingIntent pendingIntent);
	public ChooserTarget (string title, Android.Graphics.Drawables.Icon icon, float score, Android.App.PendingIntent pendingIntent);
	public ChooserTarget (Java.Lang.ICharSequence title, Android.Graphics.Drawables.Icon icon, float score, Android.Content.IntentSender intentSender);
	public ChooserTarget (string title, Android.Graphics.Drawables.Icon icon, float score, Android.Content.IntentSender intentSender);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public Android.Graphics.Drawables.Icon Icon { get; }
	public Android.Content.IntentSender IntentSender { get; }
	public float Score { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public string Title { get; }
	public Java.Lang.ICharSequence TitleFormatted { get; }
	// methods
	public virtual int DescribeContents ();
	public bool SendIntent (Android.Content.Context context, Android.Content.Intent fillInIntent);
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
