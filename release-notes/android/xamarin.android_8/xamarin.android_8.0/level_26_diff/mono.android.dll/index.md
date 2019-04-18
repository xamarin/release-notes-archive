---
id: F1BEF46B-6ECE-4BBB-AD97-A32D21BDEBAB
---

## Namespace Android

### Type Changed: Android.Manifest

### Type Changed: Android.Manifest.Permission

Added fields:

```
public static const string AnswerPhoneCalls = "android.permission.ANSWER_PHONE_CALLS";
	public static const string BindAutofillService = "android.permission.BIND_AUTOFILL_SERVICE";
	public static const string BindVisualVoicemailService = "android.permission.BIND_VISUAL_VOICEMAIL_SERVICE";
	public static const string InstantAppForegroundService = "android.permission.INSTANT_APP_FOREGROUND_SERVICE";
	public static const string ManageOwnCalls = "android.permission.MANAGE_OWN_CALLS";
	public static const string ReadPhoneNumbers = "android.permission.READ_PHONE_NUMBERS";
	public static const string RequestCompanionRunInBackground = "android.permission.REQUEST_COMPANION_RUN_IN_BACKGROUND";
	public static const string RequestCompanionUseDataInBackground = "android.permission.REQUEST_COMPANION_USE_DATA_IN_BACKGROUND";
	public static const string RequestDeletePackages = "android.permission.REQUEST_DELETE_PACKAGES";
```







### Type Changed: Android.Resource

### Type Changed: Android.Resource.Attribute

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const int CanRequestEnhancedWebAccessibility;
```

Added fields:

```
public static const int AlphabeticModifiers;
	public static const int AppCategory;
	public static const int AutoSizeMaxTextSize;
	public static const int AutoSizeMinTextSize;
	public static const int AutoSizePresetSizes;
	public static const int AutoSizeStepGranularity;
	public static const int AutoSizeTextType;
	public static const int AutofillHints;
	public static const int AutofilledHighlight;
	public static const int CanRequestFingerprintGestures;
	public static const int CertDigest;
	public static const int ColorError;
	public static const int ColorMode;
	public static const int DefaultFocusHighlightEnabled;
	public static const int FocusedByDefault;
	public static const int Font;
	public static const int FontProviderAuthority;
	public static const int FontProviderCerts;
	public static const int FontProviderPackage;
	public static const int FontProviderQuery;
	public static const int FontStyle;
	public static const int FontWeight;
	public static const int IconSpaceReserved;
	public static const int IconTint;
	public static const int IconTintMode;
	public static const int ImportantForAutofill;
	public static const int IsFeatureSplit;
	public static const int IsStatic;
	public static const int IsolatedSplits;
	public static const int JustificationMode;
	public static const int KeyboardNavigationCluster;
	public static const int LayoutMarginHorizontal;
	public static const int LayoutMarginVertical;
	public static const int MaxAspectRatio;
	public static const int Min;
	public static const int NextClusterForward;
	public static const int NumericModifiers;
	public static const int PaddingHorizontal;
	public static const int PaddingVertical;
	public static const int PersistentWhenFeatureAvailable;
	public static const int PrimaryContentAlpha;
	public static const int RecreateOnConfigChanges;
	public static const int RecycleEnabled;
	public static const int RequiredFeature;
	public static const int RequiredNotFeature;
	public static const int RotationAnimation;
	public static const int SecondaryContentAlpha;
	public static const int SingleLineTitle;
	public static const int SplitName;
	public static const int TargetProcesses;
	public static const int TargetSandboxVersion;
	public static const int TooltipText;
	public static const int VisibleToInstantApps;
	public static const int WindowSplashscreenContent;
```





### Type Changed: Android.Resource.Id

Added fields:

```
public static const int AccessibilityActionMoveWindow;
	public static const int Autofill;
	public static const int TextAssist;
```





### Type Changed: Android.Resource.String

Added field:

```
public static const int PasteAsPlainText;
```









## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityService

Added properties:

```
public AccessibilityButtonController AccessibilityButtonController { get; }
	public FingerprintGestureController FingerprintGestureController { get; }
```





### Type Changed: Android.AccessibilityServices.AccessibilityServiceCapabilities

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CanRequestFingerprintGestures = 64,</span>
</pre>





### Type Changed: Android.AccessibilityServices.AccessibilityServiceFlags

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EnableAccessibilityVolume = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestAccessibilityButton = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestFingerprintGestures = 512,</span>
</pre>





### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.AccessibilityServices.AccessibilityServiceCapabilities enum directly instead of this field.")]
	public static const AccessibilityServiceCapabilities CapabilityCanRequestFingerprintGestures;

	[Obsolete ("This constant will be removed in the future version. Use Android.AccessibilityServices.AccessibilityServiceFlags enum directly instead of this field.")]
	public static const AccessibilityServiceFlags FlagEnableAccessibilityVolume;

	[Obsolete ("This constant will be removed in the future version. Use Android.AccessibilityServices.AccessibilityServiceFlags enum directly instead of this field.")]
	public static const AccessibilityServiceFlags FlagRequestAccessibilityButton;

	[Obsolete ("This constant will be removed in the future version. Use Android.AccessibilityServices.AccessibilityServiceFlags enum directly instead of this field.")]
	public static const AccessibilityServiceFlags FlagRequestFingerprintGestures;
```



Added methods:

```
public string LoadSummary (Android.Content.PM.PackageManager packageManager);
	public virtual Java.Lang.ICharSequence LoadSummaryFormatted (Android.Content.PM.PackageManager packageManager);
```





### Type Changed: Android.AccessibilityServices.GestureDescription

### Type Changed: Android.AccessibilityServices.GestureDescription.StrokeDescription

Added constructor:

```
public GestureDescription (Android.Graphics.Path path, long startTime, long duration, bool willContinue);
```



Added methods:

```
public virtual GestureDescription.StrokeDescription ContinueStroke (Android.Graphics.Path path, long startTime, long duration, bool willContinue);
	public virtual bool WillContinue ();
```







### New Type Android.AccessibilityServices.AccessibilityButtonController

<pre class='added' data-is-non-breaking="">
public sealed class AccessibilityButtonController : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsAccessibilityButtonAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void RegisterAccessibilityButtonCallback (AccessibilityButtonController.AccessibilityButtonCallback callback);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RegisterAccessibilityButtonCallback (AccessibilityButtonController.AccessibilityButtonCallback callback, Android.OS.Handler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void UnregisterAccessibilityButtonCallback (AccessibilityButtonController.AccessibilityButtonCallback callback);</span>

	// inner types
	public abstract class AccessibilityButtonCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public AccessibilityButtonController ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">protected AccessibilityButtonController (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnAvailabilityChanged (AccessibilityButtonController controller, bool available);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnClicked (AccessibilityButtonController controller);</span>
	}
}
</pre>



### New Type Android.AccessibilityServices.FingerprintGestureController

<pre class='added' data-is-non-breaking="">
public sealed class FingerprintGestureController : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsGestureDetectionAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void RegisterFingerprintGestureCallback (FingerprintGestureController.FingerprintGestureCallback callback, Android.OS.Handler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void UnregisterFingerprintGestureCallback (FingerprintGestureController.FingerprintGestureCallback callback);</span>

	// inner types
	public abstract class FingerprintGestureCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public FingerprintGestureController ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">protected FingerprintGestureController (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnGestureDetected (FingerptintGestureTypes gesture);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnGestureDetectionAvailabilityChanged (bool available);</span>
	}
}
</pre>



### New Type Android.AccessibilityServices.FingerptintGestureTypes

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum FingerptintGestureTypes {
	<span class='added added-field ' data-is-non-breaking="">SwipeDown = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">SwipeLeft = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SwipeRight = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">SwipeUp = 4,</span>
}
</pre>





## Namespace Android.Accounts

### Type Changed: Android.Accounts.AbstractAccountAuthenticator

Added methods:

```
public virtual Android.OS.Bundle FinishSession (AccountAuthenticatorResponse response, string accountType, Android.OS.Bundle sessionBundle);
	public virtual Android.OS.Bundle IsCredentialsUpdateSuggested (AccountAuthenticatorResponse response, Account account, string statusToken);
	public virtual Android.OS.Bundle StartAddAccountSession (AccountAuthenticatorResponse response, string accountType, string authTokenType, string[] requiredFeatures, Android.OS.Bundle options);
	public virtual Android.OS.Bundle StartUpdateCredentialsSession (AccountAuthenticatorResponse response, Account account, string authTokenType, Android.OS.Bundle options);
```





### Type Changed: Android.Accounts.AccountManager

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string LoginAccountsChangedAction = "android.accounts.LOGIN_ACCOUNTS_CHANGED";
```

Added fields:

```
public static const string ActionAccountRemoved = "android.accounts.action.ACCOUNT_REMOVED";
	public static const string KeyAccountSessionBundle = "accountSessionBundle";
	public static const string KeyAccountStatusToken = "accountStatusToken";
	public static const string PackageNameKeyLegacyNotVisible = "android:accounts:key_legacy_not_visible";
	public static const string PackageNameKeyLegacyVisible = "android:accounts:key_legacy_visible";
```



Added methods:

```
public virtual bool AddAccountExplicitly (Account account, string password, Android.OS.Bundle extras, System.Collections.Generic.IDictionary<System.String,Java.Lang.Integer> visibility);
	public virtual void AddOnAccountsUpdatedListener (IOnAccountsUpdateListener listener, Android.OS.Handler handler, bool updateImmediately, string[] accountTypes);
	public virtual IAccountManagerFuture FinishSession (Android.OS.Bundle sessionBundle, Android.App.Activity activity, IAccountManagerCallback callback, Android.OS.Handler handler);
	public virtual AccountVisibility GetAccountVisibility (Account account, string packageName);
	public virtual System.Collections.Generic.IDictionary<Account,Java.Lang.Integer> GetAccountsAndVisibilityForPackage (string packageName, string accountType);
	public virtual System.Collections.Generic.IDictionary<System.String,Java.Lang.Integer> GetPackagesAndVisibilityForAccount (Account account);
	public virtual IAccountManagerFuture IsCredentialsUpdateSuggested (Account account, string statusToken, IAccountManagerCallback callback, Android.OS.Handler handler);
	public virtual bool SetAccountVisibility (Account account, string packageName, AccountVisibility visibility);
	public virtual IAccountManagerFuture StartAddAccountSession (string accountType, string authTokenType, string[] requiredFeatures, Android.OS.Bundle options, Android.App.Activity activity, IAccountManagerCallback callback, Android.OS.Handler handler);
	public virtual IAccountManagerFuture StartUpdateCredentialsSession (Account account, string authTokenType, Android.OS.Bundle options, Android.App.Activity activity, IAccountManagerCallback callback, Android.OS.Handler handler);
```





### New Type Android.Accounts.AccountVisibility

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AccountVisibility {
	<span class='added added-field ' data-is-non-breaking="">NotVisible = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserManagedNotVisible = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">UserManagedVisible = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Visible = 1,</span>
}
</pre>





## Namespace Android.Animation

### Type Changed: Android.Animation.AnimatorSet

Added property:

```
public long CurrentPlayTime { get; set; }
```



Added method:

```
public void Reverse ();
```





### Type Changed: Android.Animation.ValueAnimator

Added method:

```
public static bool AreAnimatorsEnabled ();
```







## Namespace Android.App

### Type Changed: Android.App.Activity

Added properties:

```
public virtual bool IsActivityTransitionRunning { get; }
	public virtual int MaxNumPictureInPictureActions { get; }
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void EnterPictureInPictureMode ();
	[Obsolete ("deprecated")]
	public virtual void OnMultiWindowModeChanged (bool isInMultiWindowMode);
	[Obsolete ("deprecated")]
	public virtual void OnPictureInPictureModeChanged (bool isInPictureInPictureMode);
	[Obsolete ("deprecated")]
	public virtual void OnVisibleBehindCanceled ();
	[Obsolete ("deprecated")]
	public virtual bool RequestVisibleBehind (bool visible);
```

Added methods:

```
public virtual bool EnterPictureInPictureMode (PictureInPictureParams params);
	public virtual void OnMultiWindowModeChanged (bool isInMultiWindowMode, Android.Content.Res.Configuration newConfig);
	public virtual void OnPictureInPictureModeChanged (bool isInPictureInPictureMode, Android.Content.Res.Configuration newConfig);
	public virtual void SetPictureInPictureParams (PictureInPictureParams params);
```





### Type Changed: Android.App.ActivityManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual System.Collections.Generic.IList<ActivityManager.RunningServiceInfo> GetRunningServices (int maxNum);
```

### Type Changed: Android.App.ActivityManager.RunningAppProcessInfo

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.App.Importance enum directly instead of this field.")]
	public static const Importance ImportanceCached;

	[Obsolete ("This constant will be removed in the future version. Use Android.App.Importance enum directly instead of this field.")]
	public static const Importance ImportancePerceptiblePre26;
```







### Type Changed: Android.App.ActivityOptions

Added property:

```
public virtual int LaunchDisplayId { get; }
```



Added methods:

```
public virtual ActivityOptions SetAppVerificationBundle (Android.OS.Bundle bundle);
	public virtual ActivityOptions SetLaunchDisplayId (int launchDisplayId);
```





### Type Changed: Android.App.AppOpsManager

Added fields:

```
public static const string OpstrAnswerPhoneCalls = "android:answer_phone_calls";
	public static const string OpstrPictureInPicture = "android:picture_in_picture";
	public static const string OpstrProcessOutgoingCalls = "android:process_outgoing_calls";
	public static const string OpstrReadPhoneNumbers = "android:read_phone_numbers";
```





### Type Changed: Android.App.Fragment

Added properties:

```
public bool IsStateSaved { get; }
	public Android.Views.LayoutInflater LayoutInflater { get; }
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void OnMultiWindowModeChanged (bool isInMultiWindowMode);
	[Obsolete ("deprecated")]
	public virtual void OnPictureInPictureModeChanged (bool isInPictureInPictureMode);
```

Added methods:

```
public virtual Android.Views.LayoutInflater OnGetLayoutInflater (Android.OS.Bundle savedInstanceState);
	public virtual void OnMultiWindowModeChanged (bool isInMultiWindowMode, Android.Content.Res.Configuration newConfig);
	public virtual void OnPictureInPictureModeChanged (bool isInPictureInPictureMode, Android.Content.Res.Configuration newConfig);
	public virtual void PostponeEnterTransition ();
	public virtual void StartPostponedEnterTransition ();
```





### Type Changed: Android.App.FragmentController

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void DispatchMultiWindowModeChanged (bool isInMultiWindowMode);
	[Obsolete ("deprecated")]
	public virtual void DispatchPictureInPictureModeChanged (bool isInPictureInPictureMode);
```

Added methods:

```
public virtual void DispatchMultiWindowModeChanged (bool isInMultiWindowMode, Android.Content.Res.Configuration newConfig);
	public virtual void DispatchPictureInPictureModeChanged (bool isInPictureInPictureMode, Android.Content.Res.Configuration newConfig);
```





### Type Changed: Android.App.FragmentManager

Added properties:

```
public virtual System.Collections.Generic.IList<Fragment> Fragments { get; }
	public virtual bool IsStateSaved { get; }
	public virtual Fragment PrimaryNavigationFragment { get; }
```



Added methods:

```
public virtual void RegisterFragmentLifecycleCallbacks (FragmentManager.FragmentLifecycleCallbacks cb, bool recursive);
	public virtual void UnregisterFragmentLifecycleCallbacks (FragmentManager.FragmentLifecycleCallbacks cb);
```



### New Type Android.App.FragmentLifecycleCallbacks

<pre class='added' data-is-non-breaking="">
public abstract class FragmentLifecycleCallbacks : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FragmentManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FragmentManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentActivityCreated (FragmentManager fm, Fragment f, Android.OS.Bundle savedInstanceState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentAttached (FragmentManager fm, Fragment f, Android.Content.Context context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentCreated (FragmentManager fm, Fragment f, Android.OS.Bundle savedInstanceState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentDestroyed (FragmentManager fm, Fragment f);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentDetached (FragmentManager fm, Fragment f);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentPaused (FragmentManager fm, Fragment f);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentPreAttached (FragmentManager fm, Fragment f, Android.Content.Context context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentPreCreated (FragmentManager fm, Fragment f, Android.OS.Bundle savedInstanceState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentResumed (FragmentManager fm, Fragment f);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentSaveInstanceState (FragmentManager fm, Fragment f, Android.OS.Bundle outState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentStarted (FragmentManager fm, Fragment f);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentStopped (FragmentManager fm, Fragment f);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentViewCreated (FragmentManager fm, Fragment f, Android.Views.View v, Android.OS.Bundle savedInstanceState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFragmentViewDestroyed (FragmentManager fm, Fragment f);</span>
}
</pre>





### Type Changed: Android.App.FragmentTransaction

Added methods:

```
public virtual FragmentTransaction RunOnCommit (Java.Lang.IRunnable runnable);
	public virtual FragmentTransaction SetPrimaryNavigationFragment (Fragment fragment);
	public virtual FragmentTransaction SetReorderingAllowed (bool reorderingAllowed);
```





### Type Changed: Android.App.Importance

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Cached = 400,</span>
	<span class='added added-field ' data-is-non-breaking="">PerceptiblePre26 = 130,</span>
</pre>





### Type Changed: Android.App.Instrumentation

Added property:

```
public virtual string ProcessName { get; }
```



Added methods:

```
public virtual Android.OS.TestLooperManager AcquireLooperManager (Android.OS.Looper looper);
	public virtual void AddResults (Android.OS.Bundle results);
```



### Type Changed: Android.App.Instrumentation.ActivityMonitor

Added constructor:

```
public Instrumentation ();
```



Added method:

```
public virtual Instrumentation.ActivityResult OnStartActivity (Android.Content.Intent intent);
```







### Type Changed: Android.App.KeyguardManager

Added method:

```
public virtual void RequestDismissKeyguard (Activity activity, KeyguardManager.KeyguardDismissCallback callback);
```



### New Type Android.App.KeyguardDismissCallback

<pre class='added' data-is-non-breaking="">
public abstract class KeyguardDismissCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public KeyguardManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected KeyguardManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnDismissCancelled ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnDismissError ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnDismissSucceeded ();</span>
}
</pre>





### Type Changed: Android.App.Notification

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string ExtraLargeIcon = "android.largeIcon";
	[Obsolete ("deprecated")]
	public static const string ExtraSmallIcon = "android.icon";
```

Added fields:

```
public static const string ExtraAudioContentsUri = "android.audioContents";
	public static const string ExtraChannelId = "android.intent.extra.CHANNEL_ID";
	public static const string ExtraColorized = "android.colorized";
	public static const string ExtraHistoricMessages = "android.messages.historic";
	public static const string ExtraNotificationId = "android.intent.extra.NOTIFICATION_ID";
	public static const string ExtraNotificationTag = "android.intent.extra.NOTIFICATION_TAG";
```



Added properties:

```
public virtual NotificationBadgeIconType BadgeIconType { get; }
	public virtual string ChannelId { get; }
	public virtual NotificationGroupAlertBehavior GroupAlertBehavior { get; }
	public string SettingsText { get; }
	public virtual Java.Lang.ICharSequence SettingsTextFormatted { get; }
	public virtual string ShortcutId { get; }
	public virtual long TimeoutAfter { get; }
```



### Type Changed: Android.App.Notification.Action

Added method:

```
public virtual RemoteInput[] GetDataOnlyRemoteInputs ();
```





### Type Changed: Android.App.Notification.Builder

Added constructor:

```
public Notification (Android.Content.Context context, string channelId);
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Notification.Builder SetDefaults (NotificationDefaults defaults);
	[Obsolete ("deprecated")]
	public virtual Notification.Builder SetLights (int argb, int onMs, int offMs);
	[Obsolete ("deprecated")]
	public virtual Notification.Builder SetPriority (int pri);
	[Obsolete ("deprecated")]
	public virtual Notification.Builder SetSound (Android.Net.Uri sound);
	[Obsolete ("deprecated")]
	public virtual Notification.Builder SetSound (Android.Net.Uri sound, Android.Media.AudioAttributes audioAttributes);
	[Obsolete ("deprecated")]
	public virtual Notification.Builder SetVibrate (long[] pattern);
```

Added methods:

```
public virtual Notification.Builder SetBadgeIconType (NotificationBadgeIconType icon);
	public virtual Notification.Builder SetChannelId (string channelId);
	public virtual Notification.Builder SetColorized (bool colorize);
	public virtual Notification.Builder SetGroupAlertBehavior (NotificationGroupAlertBehavior groupAlertBehavior);
	public virtual Notification.Builder SetSettingsText (Java.Lang.ICharSequence text);
	public Notification.Builder SetSettingsText (string text);
	public virtual Notification.Builder SetShortcutId (string shortcutId);
	public virtual Notification.Builder SetTimeoutAfter (long durationMs);
```





### Type Changed: Android.App.Notification.MessagingStyle

Added property:

```
public virtual System.Collections.Generic.IList<Notification.MessagingStyle.Message> HistoricMessages { get; }
```



Added method:

```
public virtual Notification.MessagingStyle AddHistoricMessage (Notification.MessagingStyle.Message message);
```



### Type Changed: Android.App.Notification.Message

Added property:

```
public Android.OS.Bundle Extras { get; }
```







### Type Changed: Android.App.Notification.WearableExtender

Added property:

```
public string BridgeTag { get; }
```



Added method:

```
public Notification.WearableExtender SetBridgeTag (string bridgeTag);
```







### Type Changed: Android.App.NotificationManager

Added properties:

```
public virtual System.Collections.Generic.IList<NotificationChannelGroup> NotificationChannelGroups { get; }
	public virtual System.Collections.Generic.IList<NotificationChannel> NotificationChannels { get; }
```



Added methods:

```
public virtual void CreateNotificationChannel (NotificationChannel channel);
	public virtual void CreateNotificationChannelGroup (NotificationChannelGroup group);
	public virtual void CreateNotificationChannelGroups (System.Collections.Generic.IList<NotificationChannelGroup> groups);
	public virtual void CreateNotificationChannels (System.Collections.Generic.IList<NotificationChannel> channels);
	public virtual void DeleteNotificationChannel (string channelId);
	public virtual void DeleteNotificationChannelGroup (string groupId);
	public virtual NotificationChannel GetNotificationChannel (string channelId);
```





### Type Changed: Android.App.PendingIntent

Added method:

```
public static PendingIntent GetForegroundService (Android.Content.Context context, int requestCode, Android.Content.Intent intent, PendingIntentFlags flags);
```





### Type Changed: Android.App.RemoteInput

Added properties:

```
public System.Collections.Generic.ICollection<string> AllowedDataTypes { get; }
	public bool IsDataOnly { get; }
```



Added methods:

```
public static void AddDataResultToIntent (RemoteInput remoteInput, Android.Content.Intent intent, System.Collections.Generic.IDictionary<System.String,Android.Net.Uri> results);
	public static System.Collections.Generic.IDictionary<System.String,Android.Net.Uri> GetDataResultsFromIntent (Android.Content.Intent intent, string remoteInputResultKey);
```



### Type Changed: Android.App.RemoteInput.Builder

Modified methods:

```
public RemoteInput.Builder SetAllowFreeFormInput (bool allowFreeFormInput allowFreeFormTextInput)
```

Added method:

```
public RemoteInput.Builder SetAllowDataType (string mimeType, bool doAllow);
```







### New Type Android.App.AuthenticationRequiredException

<pre class='added' data-is-non-breaking="">
public sealed class AuthenticationRequiredException : Java.Lang.SecurityException, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AuthenticationRequiredException (Java.Lang.Throwable cause, PendingIntent userAction);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PendingIntent UserAction { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.App.NotificationBadgeIconType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NotificationBadgeIconType {
	<span class='added added-field ' data-is-non-breaking="">Large = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Small = 1,</span>
}
</pre>



### New Type Android.App.NotificationChannel

<pre class='added' data-is-non-breaking="">
public sealed class NotificationChannel : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NotificationChannel (string id, Java.Lang.ICharSequence name, NotificationImportance importance);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NotificationChannel (string id, string name, NotificationImportance importance);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string DefaultChannelId = "miscellaneous";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Android.Media.AudioAttributes AudioAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Description { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Group { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Id { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NotificationImportance Importance { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int LightColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NotificationVisibility LockscreenVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Lang.ICharSequence NameFormatted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Net.Uri Sound { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public bool CanBypassDnd ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool CanShowBadge ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void EnableLights (bool lights);</span>
	<span class='added added-method ' data-is-non-breaking="">public void EnableVibration (bool vibration);</span>
	<span class='added added-method ' data-is-non-breaking="">public long[] GetVibrationPattern ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetBypassDnd (bool bypassDnd);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetShowBadge (bool showBadge);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetSound (Android.Net.Uri sound, Android.Media.AudioAttributes audioAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetVibrationPattern (long[] vibrationPattern);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool ShouldShowLights ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool ShouldVibrate ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.App.NotificationChannelGroup

<pre class='added' data-is-non-breaking="">
public sealed class NotificationChannelGroup : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NotificationChannelGroup (string id, Java.Lang.ICharSequence name);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NotificationChannelGroup (string id, string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;NotificationChannel&gt; Channels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Id { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Lang.ICharSequence NameFormatted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public NotificationChannelGroup Clone ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.App.NotificationGroupAlertBehavior

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NotificationGroupAlertBehavior {
	<span class='added added-field ' data-is-non-breaking="">All = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Children = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Summary = 1,</span>
}
</pre>



### New Type Android.App.PictureInPictureParams

<pre class='added' data-is-non-breaking="">
public sealed class PictureInPictureParams : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public PictureInPictureParams ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">protected PictureInPictureParams (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual PictureInPictureParams Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual PictureInPictureParams.Builder SetActions (System.Collections.Generic.IList&lt;RemoteAction&gt; actions);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual PictureInPictureParams.Builder SetAspectRatio (Android.Util.Rational aspectRatio);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual PictureInPictureParams.Builder SetSourceRectHint (Android.Graphics.Rect launchBounds);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.App.RemoteAction

<pre class='added' data-is-non-breaking="">
public sealed class RemoteAction : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RemoteAction (Android.Graphics.Drawables.Icon icon, Java.Lang.ICharSequence title, Java.Lang.ICharSequence contentDescription, PendingIntent intent);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RemoteAction (Android.Graphics.Drawables.Icon icon, string title, string contentDescription, PendingIntent intent);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public PendingIntent ActionIntent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ContentDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Lang.ICharSequence ContentDescriptionFormatted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool Enabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Graphics.Drawables.Icon Icon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Title { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Lang.ICharSequence TitleFormatted { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public RemoteAction Clone ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Dump (string prefix, Java.IO.PrintWriter pw);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## Namespace Android.App.Admin

### Type Changed: Android.App.Admin.DeviceAdminReceiver

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void OnPasswordChanged (Android.Content.Context context, Android.Content.Intent intent);
	[Obsolete ("deprecated")]
	public virtual void OnPasswordExpiring (Android.Content.Context context, Android.Content.Intent intent);
	[Obsolete ("deprecated")]
	public virtual void OnPasswordFailed (Android.Content.Context context, Android.Content.Intent intent);
	[Obsolete ("deprecated")]
	public virtual void OnPasswordSucceeded (Android.Content.Context context, Android.Content.Intent intent);
```

Added methods:

```
public virtual void OnNetworkLogsAvailable (Android.Content.Context context, Android.Content.Intent intent, long batchToken, int networkLogsCount);
	public virtual void OnPasswordChanged (Android.Content.Context context, Android.Content.Intent intent, Android.OS.UserHandle user);
	public virtual void OnPasswordExpiring (Android.Content.Context context, Android.Content.Intent intent, Android.OS.UserHandle user);
	public virtual void OnPasswordFailed (Android.Content.Context context, Android.Content.Intent intent, Android.OS.UserHandle user);
	public virtual void OnPasswordSucceeded (Android.Content.Context context, Android.Content.Intent intent, Android.OS.UserHandle user);
	public virtual void OnUserAdded (Android.Content.Context context, Android.Content.Intent intent, Android.OS.UserHandle newUser);
	public virtual void OnUserRemoved (Android.Content.Context context, Android.Content.Intent intent, Android.OS.UserHandle removedUser);
```





### Type Changed: Android.App.Admin.DevicePolicyManager

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string ExtraProvisioningEmailAddress = "android.app.extra.PROVISIONING_EMAIL_ADDRESS";
```

Added fields:

```
public static const string ActionApplicationDelegationScopesChanged = "android.app.action.APPLICATION_DELEGATION_SCOPES_CHANGED";
	public static const string ActionDeviceAdminService = "android.app.action.DEVICE_ADMIN_SERVICE";
	public static const string ActionProvisioningSuccessful = "android.app.action.PROVISIONING_SUCCESSFUL";
	public static const string DelegationAppRestrictions = "delegation-app-restrictions";
	public static const string DelegationBlockUninstall = "delegation-block-uninstall";
	public static const string DelegationCertInstall = "delegation-cert-install";
	public static const string DelegationEnableSystemApp = "delegation-enable-system-app";
	public static const string DelegationPackageAccess = "delegation-package-access";
	public static const string DelegationPermissionGrant = "delegation-permission-grant";
	public static const string ExtraDelegationScopes = "android.app.extra.DELEGATION_SCOPES";
	public static const string ExtraProvisioningDisclaimerContent = "android.app.extra.PROVISIONING_DISCLAIMER_CONTENT";
	public static const string ExtraProvisioningDisclaimerHeader = "android.app.extra.PROVISIONING_DISCLAIMER_HEADER";
	public static const string ExtraProvisioningDisclaimers = "android.app.extra.PROVISIONING_DISCLAIMERS";
	public static const string ExtraProvisioningKeepAccountOnMigration = "android.app.extra.PROVISIONING_KEEP_ACCOUNT_ON_MIGRATION";
	public static const string ExtraProvisioningSkipUserConsent = "android.app.extra.PROVISIONING_SKIP_USER_CONSENT";

	[Obsolete ("This constant will be removed in the future version. Use Android.App.Admin.DevicePolicyManagerFlags enum directly instead of this field.")]
	public static const DevicePolicyManagerFlags FlagEvictCredentialEncryptionKey;
	public static const string PolicyDisableCamera = "policy_disable_camera";
	public static const string PolicyDisableScreenCapture = "policy_disable_screen_capture";
```



Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual bool IsCallerApplicationRestrictionsManagingPackage { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void ClearDeviceOwnerApp (string packageName);
	[Obsolete ("deprecated")]
	public virtual void ClearProfileOwner (Android.Content.ComponentName admin);
	[Obsolete ("deprecated")]
	public virtual string GetApplicationRestrictionsManagingPackage (Android.Content.ComponentName admin);
	[Obsolete ("deprecated")]
	public virtual string GetCertInstallerPackage (Android.Content.ComponentName admin);
	[Obsolete ("deprecated")]
	public virtual void SetApplicationRestrictionsManagingPackage (Android.Content.ComponentName admin, string packageName);
	[Obsolete ("deprecated")]
	public virtual void SetCertInstallerPackage (Android.Content.ComponentName admin, string installerPackage);
```

Added methods:

```
public virtual bool BindDeviceAdminServiceAsUser (Android.Content.ComponentName admin, Android.Content.Intent serviceIntent, Android.Content.IServiceConnection conn, Android.Content.Bind flags, Android.OS.UserHandle targetUser);
	public virtual bool ClearResetPasswordToken (Android.Content.ComponentName admin);
	public virtual Android.Content.Intent CreateAdminSupportIntent (string restriction);
	public virtual System.Collections.Generic.ICollection<string> GetAffiliationIds (Android.Content.ComponentName admin);
	public virtual System.Collections.Generic.IList<Android.OS.UserHandle> GetBindDeviceAdminTargetUsers (Android.Content.ComponentName admin);
	public virtual System.Collections.Generic.IList<string> GetDelegatePackages (Android.Content.ComponentName admin, string delegationScope);
	public virtual System.Collections.Generic.IList<string> GetDelegatedScopes (Android.Content.ComponentName admin, string delegatedPackage);
	public virtual string[] GetLockTaskPackages (Android.Content.ComponentName admin);
	public virtual SystemUpdateInfo GetPendingSystemUpdate (Android.Content.ComponentName admin);
	public virtual System.Collections.Generic.IList<string> GetPermittedCrossProfileNotificationListeners (Android.Content.ComponentName admin);
	public virtual long GetRequiredStrongAuthTimeout (Android.Content.ComponentName admin);
	public virtual bool IsBackupServiceEnabled (Android.Content.ComponentName admin);
	public virtual bool IsNetworkLoggingEnabled (Android.Content.ComponentName admin);
	public virtual bool IsResetPasswordTokenActive (Android.Content.ComponentName admin);
	public virtual void LockNow (DevicePolicyManagerFlags flags);
	public virtual bool ResetPasswordWithToken (Android.Content.ComponentName admin, string password, byte[] token, ResetPasswordFlags flags);
	public virtual System.Collections.Generic.IList<NetworkEvent> RetrieveNetworkLogs (Android.Content.ComponentName admin, long batchToken);
	public virtual void SetAffiliationIds (Android.Content.ComponentName admin, System.Collections.Generic.ICollection<string> ids);
	public virtual void SetBackupServiceEnabled (Android.Content.ComponentName admin, bool enabled);
	public virtual void SetDelegatedScopes (Android.Content.ComponentName admin, string delegatePackage, System.Collections.Generic.IList<string> scopes);
	public virtual void SetNetworkLoggingEnabled (Android.Content.ComponentName admin, bool enabled);
	public virtual bool SetPermittedCrossProfileNotificationListeners (Android.Content.ComponentName admin, System.Collections.Generic.IList<string> packageList);
	public virtual void SetRequiredStrongAuthTimeout (Android.Content.ComponentName admin, long timeoutMs);
	public virtual bool SetResetPasswordToken (Android.Content.ComponentName admin, byte[] token);
```





### Type Changed: Android.App.Admin.DevicePolicyManagerFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EvictCredentialEncryptionKey = 1,</span>
</pre>





### New Type Android.App.Admin.ConnectEvent

<pre class='added' data-is-non-breaking="">
public sealed class ConnectEvent : Android.App.Admin.NetworkEvent, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Net.InetAddress InetAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Port { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);</span>
}
</pre>



### New Type Android.App.Admin.DeviceAdminService

<pre class='added' data-is-non-breaking="">
public class DeviceAdminService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DeviceAdminService ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DeviceAdminService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override Android.OS.IBinder OnBind (Android.Content.Intent intent);</span>
}
</pre>



### New Type Android.App.Admin.DnsEvent

<pre class='added' data-is-non-breaking="">
public sealed class DnsEvent : Android.App.Admin.NetworkEvent, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Hostname { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;Java.Net.InetAddress&gt; InetAddresses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int TotalResolvedAddressCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);</span>
}
</pre>



### New Type Android.App.Admin.NetworkEvent

<pre class='added' data-is-non-breaking="">
public abstract class NetworkEvent : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NetworkEvent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PackageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long Timestamp { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.App.Admin.SecurityPatchStates

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SecurityPatchStates {
	<span class='added added-field ' data-is-non-breaking="">StateFalse = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StateTrue = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">StateUnknown = 0,</span>
}
</pre>



### New Type Android.App.Admin.SystemUpdateInfo

<pre class='added' data-is-non-breaking="">
public sealed class SystemUpdateInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long ReceivedTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SecurityPatchStates SecurityPatchState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## Namespace Android.App.Assist

### Type Changed: Android.App.Assist.AssistStructure

Added properties:

```
public virtual long AcquisitionEndTime { get; }
	public virtual long AcquisitionStartTime { get; }
	public virtual bool IsHomeActivity { get; }
```



### Type Changed: Android.App.Assist.AssistStructure.ViewNode

Added properties:

```
public virtual Android.Views.Autofill.AutofillId AutofillId { get; }
	public virtual Android.Views.AutofillType AutofillType { get; }
	public virtual Android.Views.Autofill.AutofillValue AutofillValue { get; }
	public virtual Android.Views.ViewStructure.HtmlInfo HtmlInfo { get; }
	public virtual Android.Text.InputTypes InputType { get; }
	public virtual bool IsOpaque { get; }
	public virtual Android.OS.LocaleList LocaleList { get; }
	public virtual string WebDomain { get; }
```



Added methods:

```
public virtual string[] GetAutofillHints ();
	public string[] GetAutofillOptions ();
	public virtual Java.Lang.ICharSequence[] GetAutofillOptionsFormatted ();
```









## Namespace Android.App.Backup

### Type Changed: Android.App.Backup.BackupDataOutput

Added property:

```
public virtual long Quota { get; }
```





### Type Changed: Android.App.Backup.FullBackupDataOutput

Added property:

```
public virtual long Quota { get; }
```







## Namespace Android.App.Job

### Type Changed: Android.App.Job.JobInfo

Added properties:

```
public virtual Android.Content.ClipData ClipData { get; }
	public virtual int ClipGrantFlags { get; }
	public virtual bool IsRequireBatteryNotLow { get; }
	public virtual bool IsRequireStorageNotLow { get; }
	public virtual Android.OS.Bundle TransientExtras { get; }
```



### Type Changed: Android.App.Job.JobInfo.Builder

Added methods:

```
public JobInfo.Builder SetClipData (Android.Content.ClipData clip, Android.Content.ActivityFlags grantFlags);
	public JobInfo.Builder SetRequiresBatteryNotLow (bool batteryNotLow);
	public JobInfo.Builder SetRequiresStorageNotLow (bool storageNotLow);
	public JobInfo.Builder SetTransientExtras (Android.OS.Bundle extras);
```







### Type Changed: Android.App.Job.JobParameters

Added properties:

```
public virtual Android.Content.ClipData ClipData { get; }
	public virtual int ClipGrantFlags { get; }
	public virtual Android.OS.Bundle TransientExtras { get; }
```



Added methods:

```
public virtual void CompleteWork (JobWorkItem work);
	public virtual JobWorkItem DequeueWork ();
```





### Type Changed: Android.App.Job.JobScheduler

Added method:

```
public virtual int Enqueue (JobInfo job, JobWorkItem work);
```





### Type Changed: Android.App.Job.NetworkType

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Metered = 4,</span>
</pre>





### New Type Android.App.Job.JobServiceEngine

<pre class='added' data-is-non-breaking="">
public abstract class JobServiceEngine : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public JobServiceEngine (Android.App.Service service);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected JobServiceEngine (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Android.OS.IBinder Binder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void JobFinished (JobParameters params, bool needsReschedule);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool OnStartJob (JobParameters params);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool OnStopJob (JobParameters params);</span>
}
</pre>



### New Type Android.App.Job.JobWorkItem

<pre class='added' data-is-non-breaking="">
public sealed class JobWorkItem : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public JobWorkItem (Android.Content.Intent intent);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int DeliveryCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Content.Intent Intent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## Namespace Android.App.Usage

### Type Changed: Android.App.Usage.NetworkStats

### Type Changed: Android.App.Usage.NetworkStats.Bucket

Added property:

```
public virtual MeteredStates Metered { get; }
```







### New Type Android.App.Usage.ExternalStorageStats

<pre class='added' data-is-non-breaking="">
public sealed class ExternalStorageStats : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public long AppBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long AudioBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long ImageBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long TotalBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long VideoBytes { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.App.Usage.MeteredStates

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MeteredStates {
	<span class='added added-field ' data-is-non-breaking="">All = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>



### New Type Android.App.Usage.StorageStats

<pre class='added' data-is-non-breaking="">
public sealed class StorageStats : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public long AppBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long CacheBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long DataBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.App.Usage.StorageStatsManager

<pre class='added' data-is-non-breaking="">
public class StorageStatsManager : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected StorageStatsManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual long GetFreeBytes (Java.Util.UUID storageUuid);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual long GetTotalBytes (Java.Util.UUID storageUuid);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ExternalStorageStats QueryExternalStatsForUser (Java.Util.UUID storageUuid, Android.OS.UserHandle user);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual StorageStats QueryStatsForPackage (Java.Util.UUID storageUuid, string packageName, Android.OS.UserHandle user);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual StorageStats QueryStatsForUid (Java.Util.UUID storageUuid, int uid);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual StorageStats QueryStatsForUser (Java.Util.UUID storageUuid, Android.OS.UserHandle user);</span>
}
</pre>





## Namespace Android.Appwidget

### Type Changed: Android.Appwidget.AppWidgetHost

Added method:

```
public virtual int[] GetAppWidgetIds ();
```





### Type Changed: Android.Appwidget.AppWidgetHostView

Added method:

```
public virtual void SetExecutor (Java.Util.Concurrent.IExecutor executor);
```





### Type Changed: Android.Appwidget.AppWidgetManager

Added field:

```
public static const string ExtraAppwidgetPreview = "appWidgetPreview";
```



Added property:

```
public virtual bool IsRequestPinAppWidgetSupported { get; }
```



Added methods:

```
public virtual System.Collections.Generic.IList<AppWidgetProviderInfo> GetInstalledProvidersForPackage (string packageName, Android.OS.UserHandle profile);
	public virtual bool RequestPinAppWidget (Android.Content.ComponentName provider, Android.OS.Bundle extras, Android.App.PendingIntent successCallback);
```







## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothAdapter

Added properties:

```
public bool IsLe2MPhySupported { get; }
	public bool IsLeCodedPhySupported { get; }
	public bool IsLeExtendedAdvertisingSupported { get; }
	public bool IsLePeriodicAdvertisingSupported { get; }
	public int LeMaximumAdvertisingDataLength { get; }
```





### Type Changed: Android.Bluetooth.BluetoothDevice

Added methods:

```
public BluetoothGatt ConnectGatt (Android.Content.Context context, bool autoConnect, BluetoothGattCallback callback, BluetoothTransports transport, LE.ScanSettingsPhy phy);
	public BluetoothGatt ConnectGatt (Android.Content.Context context, bool autoConnect, BluetoothGattCallback callback, BluetoothTransports transport, LE.ScanSettingsPhy phy, Android.OS.Handler handler);
```





### Type Changed: Android.Bluetooth.BluetoothGatt

Added methods:

```
public void ReadPhy ();
	public void SetPreferredPhy (BluetoothPhy txPhy, BluetoothPhy rxPhy, BluetoothPhyOption phyOptions);
```





### Type Changed: Android.Bluetooth.BluetoothGattCallback

Added methods:

```
public virtual void OnPhyRead (BluetoothGatt gatt, LE.ScanSettingsPhy txPhy, LE.ScanSettingsPhy rxPhy, GattStatus status);
	public virtual void OnPhyUpdate (BluetoothGatt gatt, LE.ScanSettingsPhy txPhy, LE.ScanSettingsPhy rxPhy, GattStatus status);
```





### Type Changed: Android.Bluetooth.BluetoothGattServer

Added methods:

```
public void ReadPhy (BluetoothDevice device);
	public void SetPreferredPhy (BluetoothDevice device, BluetoothPhy txPhy, BluetoothPhy rxPhy, BluetoothPhyOption phyOptions);
```





### Type Changed: Android.Bluetooth.BluetoothGattServerCallback

Added methods:

```
public virtual void OnPhyRead (BluetoothDevice device, LE.ScanSettingsPhy txPhy, LE.ScanSettingsPhy rxPhy, GattStatus status);
	public virtual void OnPhyUpdate (BluetoothDevice device, LE.ScanSettingsPhy txPhy, LE.ScanSettingsPhy rxPhy, GattStatus status);
```





### New Type Android.Bluetooth.BluetoothPhy

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum BluetoothPhy {
	<span class='added added-field ' data-is-non-breaking="">Le1m = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Le1mMask = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Le2m = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Le2mMask = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LeCoded = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">LeCodedMask = 4,</span>
}
</pre>



### New Type Android.Bluetooth.BluetoothPhyOption

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum BluetoothPhyOption {
	<span class='added added-field ' data-is-non-breaking="">NoPreferred = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">S2 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">S8 = 2,</span>
}
</pre>





## Namespace Android.Bluetooth.LE

### Type Changed: Android.Bluetooth.LE.BluetoothLeAdvertiser

Added methods:

```
public void StartAdvertisingSet (AdvertisingSetParameters parameters, AdvertiseData advertiseData, AdvertiseData scanResponse, PeriodicAdvertisingParameters periodicParameters, AdvertiseData periodicData, AdvertisingSetCallback callback);
	public void StartAdvertisingSet (AdvertisingSetParameters parameters, AdvertiseData advertiseData, AdvertiseData scanResponse, PeriodicAdvertisingParameters periodicParameters, AdvertiseData periodicData, AdvertisingSetCallback callback, Android.OS.Handler handler);
	public void StartAdvertisingSet (AdvertisingSetParameters parameters, AdvertiseData advertiseData, AdvertiseData scanResponse, PeriodicAdvertisingParameters periodicParameters, AdvertiseData periodicData, int duration, int maxExtendedAdvertisingEvents, AdvertisingSetCallback callback);
	public void StartAdvertisingSet (AdvertisingSetParameters parameters, AdvertiseData advertiseData, AdvertiseData scanResponse, PeriodicAdvertisingParameters periodicParameters, AdvertiseData periodicData, int duration, int maxExtendedAdvertisingEvents, AdvertisingSetCallback callback, Android.OS.Handler handler);
	public void StopAdvertisingSet (AdvertisingSetCallback callback);
```





### Type Changed: Android.Bluetooth.LE.BluetoothLeScanner

Added fields:

```
public static const string ExtraCallbackType = "android.bluetooth.le.extra.CALLBACK_TYPE";
	public static const string ExtraErrorCode = "android.bluetooth.le.extra.ERROR_CODE";
	public static const string ExtraListScanResult = "android.bluetooth.le.extra.LIST_SCAN_RESULT";
```



Added methods:

```
public int StartScan (System.Collections.Generic.IList<ScanFilter> filters, ScanSettings settings, Android.App.PendingIntent callbackIntent);
	public void StopScan (Android.App.PendingIntent callbackIntent);
```





### Type Changed: Android.Bluetooth.LE.ScanResult

Added constructor:

```
public ScanResult (Android.Bluetooth.BluetoothDevice device, int eventType, ScanSettingsPhy primaryPhy, ScanSettingsPhy secondaryPhy, int advertisingSid, AdvertiseTxPower txPower, int rssi, int periodicAdvertisingInterval, ScanRecord scanRecord, long timestampNanos);
```



Added fields:

```
public static const int PeriodicIntervalNotPresent;
	public static const int SidNotPresent;
	public static const int TxPowerNotPresent;
```



Added properties:

```
public int AdvertisingSid { get; }
	public DataStatus DataStatus { get; }
	public bool IsConnectable { get; }
	public bool IsLegacy { get; }
	public int PeriodicAdvertisingInterval { get; }
	public ScanSettingsPhy PrimaryPhy { get; }
	public ScanSettingsPhy SecondaryPhy { get; }
	public AdvertiseTxPower TxPower { get; }
```





### Type Changed: Android.Bluetooth.LE.ScanSettings

Added properties:

```
public bool Legacy { get; }
	public ScanSettingsPhy Phy { get; }
```



### Type Changed: Android.Bluetooth.LE.ScanSettings.Builder

Added methods:

```
public ScanSettings.Builder SetLegacy (bool legacy);
	public ScanSettings.Builder SetPhy (Android.Bluetooth.BluetoothPhy phy);
```







### New Type Android.Bluetooth.LE.AdvertiseResult

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AdvertiseResult {
	<span class='added added-field ' data-is-non-breaking="">FailedAlreadyStarted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedDataTooLarge = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedFeatureUnsupported = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedInternalError = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedTooManyAdvertisers = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>



### New Type Android.Bluetooth.LE.AdvertiseTxPower

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AdvertiseTxPower {
	<span class='added added-field ' data-is-non-breaking="">High = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Low = -15,</span>
	<span class='added added-field ' data-is-non-breaking="">Max = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Medium = -7,</span>
	<span class='added added-field ' data-is-non-breaking="">Min = -127,</span>
	<span class='added added-field ' data-is-non-breaking="">UltraLow = -21,</span>
}
</pre>



### New Type Android.Bluetooth.LE.AdvertisingSet

<pre class='added' data-is-non-breaking="">
public sealed class AdvertisingSet : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void EnableAdvertising (bool enable, int duration, int maxExtendedAdvertisingEvents);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAdvertisingData (AdvertiseData advertiseData);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAdvertisingParameters (AdvertisingSetParameters parameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetPeriodicAdvertisingData (AdvertiseData periodicData);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetPeriodicAdvertisingEnabled (bool enable);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetPeriodicAdvertisingParameters (PeriodicAdvertisingParameters parameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetScanResponseData (AdvertiseData scanResponse);</span>
}
</pre>



### New Type Android.Bluetooth.LE.AdvertisingSetCallback

<pre class='added' data-is-non-breaking="">
public abstract class AdvertisingSetCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisingSetCallback ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AdvertisingSetCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnAdvertisingDataSet (AdvertisingSet advertisingSet, AdvertiseResult status);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnAdvertisingEnabled (AdvertisingSet advertisingSet, bool enable, AdvertiseResult status);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnAdvertisingParametersUpdated (AdvertisingSet advertisingSet, int txPower, AdvertiseResult status);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnAdvertisingSetStarted (AdvertisingSet advertisingSet, int txPower, AdvertiseResult status);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnAdvertisingSetStopped (AdvertisingSet advertisingSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnPeriodicAdvertisingDataSet (AdvertisingSet advertisingSet, AdvertiseResult status);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnPeriodicAdvertisingEnabled (AdvertisingSet advertisingSet, bool enable, AdvertiseResult status);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnPeriodicAdvertisingParametersUpdated (AdvertisingSet advertisingSet, AdvertiseResult status);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnScanResponseDataSet (AdvertisingSet advertisingSet, AdvertiseResult status);</span>
}
</pre>



### New Type Android.Bluetooth.LE.AdvertisingSetParameters

<pre class='added' data-is-non-breaking="">
public sealed class AdvertisingSetParameters : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int IntervalHigh;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int IntervalLow;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int IntervalMax;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int IntervalMedium;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int IntervalMin;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Interval { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsAnonymous { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsConnectable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsLegacy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsScannable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Bluetooth.BluetoothPhy PrimaryPhy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Bluetooth.BluetoothPhy SecondaryPhy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AdvertiseTxPower TxPowerLevel { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool IncludeTxPower ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public AdvertisingSetParameters ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetAnonymous (bool isAnonymous);</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetConnectable (bool connectable);</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetIncludeTxPower (bool includeTxPower);</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetInterval (int interval);</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetLegacyMode (bool isLegacy);</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetPrimaryPhy (ScanSettingsPhy primaryPhy);</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetScannable (bool scannable);</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetSecondaryPhy (ScanSettingsPhy secondaryPhy);</span>
		<span class='added added-method ' data-is-non-breaking="">public AdvertisingSetParameters.Builder SetTxPowerLevel (AdvertiseTxPower txPowerLevel);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Bluetooth.LE.BluetoothPhy

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum BluetoothPhy {
	<span class='added added-field ' data-is-non-breaking="">Unused = 0,</span>
}
</pre>



### New Type Android.Bluetooth.LE.DataStatus

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum DataStatus {
	<span class='added added-field ' data-is-non-breaking="">Complete = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Truncated = 2,</span>
}
</pre>



### New Type Android.Bluetooth.LE.PeriodicAdvertisingParameters

<pre class='added' data-is-non-breaking="">
public sealed class PeriodicAdvertisingParameters : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IncludeTxPower { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Interval { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public PeriodicAdvertisingParameters ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public PeriodicAdvertisingParameters Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public PeriodicAdvertisingParameters.Builder SetIncludeTxPower (bool includeTxPower);</span>
		<span class='added added-method ' data-is-non-breaking="">public PeriodicAdvertisingParameters.Builder SetInterval (int interval);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Bluetooth.LE.ScanSettingsPhy

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ScanSettingsPhy {
	<span class='added added-field ' data-is-non-breaking="">AllSupported = 255,</span>
}
</pre>





## Namespace Android.Content

### Type Changed: Android.Content.ActivityFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ReceiverVisibleToInstantApps = 2097152,</span>
</pre>





### Type Changed: Android.Content.ClipData

Added method:

```
public virtual void AddItem (ContentResolver resolver, ClipData.Item item);
```





### Type Changed: Android.Content.ClipDescription

Added property:

```
public virtual long Timestamp { get; }
```





### Type Changed: Android.Content.ContentProvider

Added methods:

```
public virtual Android.Database.ICursor Query (Android.Net.Uri uri, string[] projection, Android.OS.Bundle queryArgs, Android.OS.CancellationSignal cancellationSignal);
	public virtual bool Refresh (Android.Net.Uri uri, Android.OS.Bundle args, Android.OS.CancellationSignal cancellationSignal);
```





### Type Changed: Android.Content.ContentProviderClient

Modified methods:

```
public virtual Android.Database.ICursor Query (Android.Net.Uri url uri, string[] projection, string selection, string[] selectionArgs, string sortOrder, Android.OS.CancellationSignal cancellationSignal)
```

Added methods:

```
public virtual Android.Database.ICursor Query (Android.Net.Uri uri, string[] projection, Android.OS.Bundle queryArgs, Android.OS.CancellationSignal cancellationSignal);
	public virtual bool Refresh (Android.Net.Uri url, Android.OS.Bundle args, Android.OS.CancellationSignal cancellationSignal);
```





### Type Changed: Android.Content.ContentResolver

Added fields:

```
public static const string ExtraHonoredArgs = "android.content.extra.HONORED_ARGS";
	public static const string ExtraRefreshSupported = "android.content.extra.REFRESH_SUPPORTED";
	public static const string ExtraTotalCount = "android.content.extra.TOTAL_COUNT";
	public static const string QueryArgLimit = "android:query-arg-limit";
	public static const string QueryArgOffset = "android:query-arg-offset";
	public static const string QueryArgSortCollation = "android:query-arg-sort-collation";
	public static const string QueryArgSortColumns = "android:query-arg-sort-columns";
	public static const string QueryArgSortDirection = "android:query-arg-sort-direction";
	public static const string QueryArgSqlSelection = "android:query-arg-sql-selection";
	public static const string QueryArgSqlSelectionArgs = "android:query-arg-sql-selection-args";
	public static const string QueryArgSqlSortOrder = "android:query-arg-sql-sort-order";

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.QuerySortDirection enum directly instead of this field.")]
	public static const QuerySortDirection QuerySortDirectionAscending;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.QuerySortDirection enum directly instead of this field.")]
	public static const QuerySortDirection QuerySortDirectionDescending;
```



Added methods:

```
public Android.Database.ICursor Query (Android.Net.Uri uri, string[] projection, Android.OS.Bundle queryArgs, Android.OS.CancellationSignal cancellationSignal);
	public bool Refresh (Android.Net.Uri url, Android.OS.Bundle args, Android.OS.CancellationSignal cancellationSignal);
```





### Type Changed: Android.Content.Context

Added fields:

```
public static const string CompanionDeviceService = "companiondevice";
	public static const int ReceiverVisibleToInstantApps;
	public static const string StorageStatsService = "storagestats";
	public static const string TextClassificationService = "textclassification";
	public static const string WifiAwareService = "wifiaware";
```



Added methods:

```
public virtual Context CreateContextForSplit (string splitName);
	public virtual Intent RegisterReceiver (BroadcastReceiver receiver, IntentFilter filter, ActivityFlags flags);
	public virtual Intent RegisterReceiver (BroadcastReceiver receiver, IntentFilter filter, string broadcastPermission, Android.OS.Handler scheduler, ActivityFlags flags);
	public virtual void RevokeUriPermission (string toPackage, Android.Net.Uri uri, ActivityFlags modeFlags);
	public virtual ComponentName StartForegroundService (Intent service);
```





### Type Changed: Android.Content.ContextWrapper

Added methods:

```
public override Context CreateContextForSplit (string splitName);
	public override Intent RegisterReceiver (BroadcastReceiver receiver, IntentFilter filter, ActivityFlags flags);
	public override Intent RegisterReceiver (BroadcastReceiver receiver, IntentFilter filter, string broadcastPermission, Android.OS.Handler scheduler, ActivityFlags flags);
	public override void RevokeUriPermission (string targetPackage, Android.Net.Uri uri, ActivityFlags modeFlags);
	public override ComponentName StartForegroundService (Intent service);
```





### Type Changed: Android.Content.Intent

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string ActionDeviceStorageLow = "android.intent.action.DEVICE_STORAGE_LOW";
	[Obsolete ("deprecated")]
	public static const string ActionDeviceStorageOk = "android.intent.action.DEVICE_STORAGE_OK";
	[Obsolete ("deprecated")]
	public static const string ExtraShortcutIcon = "android.intent.extra.shortcut.ICON";
	[Obsolete ("deprecated")]
	public static const string ExtraShortcutIconResource = "android.intent.extra.shortcut.ICON_RESOURCE";
	[Obsolete ("deprecated")]
	public static const string ExtraShortcutIntent = "android.intent.extra.shortcut.INTENT";
	[Obsolete ("deprecated")]
	public static const string ExtraShortcutName = "android.intent.extra.shortcut.NAME";
```

Added fields:

```
public static const string ActionCarrierSetup = "android.intent.action.CARRIER_SETUP";
	public static const string CategoryTypedOpenable = "android.intent.category.TYPED_OPENABLE";
	public static const string CategoryVrHome = "android.intent.category.VR_HOME";
	public static const string ExtraComponentName = "android.intent.extra.COMPONENT_NAME";
	public static const string ExtraContentAnnotations = "android.intent.extra.CONTENT_ANNOTATIONS";
	public static const string ExtraFromStorage = "android.intent.extra.FROM_STORAGE";
	public static const string ExtraQuickViewFeatures = "android.intent.extra.QUICK_VIEW_FEATURES";
```



Added method:

```
public virtual void RemoveFlags (ActivityFlags flags);
```





### New Type Android.Content.QuerySortDirection

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum QuerySortDirection {
	<span class='added added-field ' data-is-non-breaking="">Ascending = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Descending = 1,</span>
}
</pre>



### New Type Android.Content.QuickViewConstants

<pre class='added' data-is-non-breaking="">
public class QuickViewConstants : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected QuickViewConstants (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string FeatureDownload = "android:download";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string FeatureEdit = "android:edit";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string FeaturePrint = "android:print";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string FeatureSend = "android:send";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string FeatureView = "android:view";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ActivityInfo

Added property:

```
public ActivityColorMode ColorMode { get; set; }
```





### Type Changed: Android.Content.PM.ApplicationInfo

Added properties:

```
public ApplicationCategories Category { get; set; }
	public System.Collections.Generic.IList<string> SplitNames { get; set; }
	public Java.Util.UUID StorageUuid { get; set; }
```



Added methods:

```
public static string GetCategoryTitle (Android.Content.Context context, ApplicationCategories category);
	public static Java.Lang.ICharSequence GetCategoryTitleFormatted (Android.Content.Context context, ApplicationCategories category);
```





### Type Changed: Android.Content.PM.ComponentInfo

Added property:

```
public string SplitName { get; set; }
```





### Type Changed: Android.Content.PM.ConfigChanges

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ColorMode = 16384,</span>
</pre>





### Type Changed: Android.Content.PM.InstrumentationInfo

Added properties:

```
public System.Collections.Generic.IList<string> SplitNames { get; set; }
	public string TargetProcesses { get; set; }
```





### Type Changed: Android.Content.PM.LauncherApps

Added fields:

```
public static const string ActionConfirmPinAppwidget = "android.content.pm.action.CONFIRM_PIN_APPWIDGET";
	public static const string ActionConfirmPinShortcut = "android.content.pm.action.CONFIRM_PIN_SHORTCUT";
	public static const string ExtraPinItemRequest = "android.content.pm.extra.PIN_ITEM_REQUEST";
```



Added property:

```
public virtual System.Collections.Generic.IList<Android.OS.UserHandle> Profiles { get; }
```



Added methods:

```
public virtual ApplicationInfo GetApplicationInfo (string packageName, PackageInfoFlags flags, Android.OS.UserHandle user);
	public virtual LauncherApps.PinItemRequest GetPinItemRequest (Android.Content.Intent intent);
	public virtual Android.Content.IntentSender GetShortcutConfigActivityIntent (LauncherActivityInfo info);
	public virtual System.Collections.Generic.IList<LauncherActivityInfo> GetShortcutConfigActivityList (string packageName, Android.OS.UserHandle user);
```



### New Type Android.Content.PM.PinItemRequest

<pre class='added' data-is-non-breaking="">
public sealed class PinItemRequest : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Content.PM.PinItemRequestType enum directly instead of this field.")]
	public static const PinItemRequestType RequestTypeAppwidget;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Content.PM.PinItemRequestType enum directly instead of this field.")]
	public static const PinItemRequestType RequestTypeShortcut;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.OS.Bundle Extras { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsValid { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PinItemRequestType RequestType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ShortcutInfo ShortcutInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public bool Accept ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Accept (Android.OS.Bundle options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Android.Appwidget.AppWidgetProviderInfo GetAppWidgetProviderInfo (Android.Content.Context context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





### Type Changed: Android.Content.PM.PackageInstaller

Added fields:

```
public static const string ActionSessionCommitted = "android.content.pm.action.SESSION_COMMITTED";
	public static const string ExtraSession = "android.content.pm.extra.SESSION";
```



Added method:

```
public virtual void Uninstall (VersionedPackage versionedPackage, Android.Content.IntentSender statusReceiver);
```



### Type Changed: Android.Content.PM.PackageInstaller.SessionInfo

Added properties:

```
public virtual PackageInstallReason InstallReason { get; }
	public virtual bool IsSealed { get; }
```





### Type Changed: Android.Content.PM.PackageInstaller.SessionParams

Added method:

```
public virtual void SetInstallReason (PackageInstallReason installReason);
```







### Type Changed: Android.Content.PM.PackageManager

Added fields:

```
public static const string FeatureActivitiesOnSecondaryDisplays = "android.software.activities_on_secondary_displays";
	public static const string FeatureAutofill = "android.software.autofill";
	public static const string FeatureCompanionDeviceSetup = "android.software.companion_device_setup";
	public static const string FeatureEmbedded = "android.hardware.type.embedded";
	public static const string FeatureLeanbackOnly = "android.software.leanback_only";
	public static const string FeatureVrHeadtracking = "android.hardware.vr.headtracking";
	public static const string FeatureVulkanHardwareCompute = "android.hardware.vulkan.compute";
	public static const string FeatureWifiAware = "android.hardware.wifi.aware";
	public static const int VersionCodeHighest;
```



Added properties:

```
public virtual int InstantAppCookieMaxBytes { get; }
	public virtual bool IsInstantApp { get; }
```



Added methods:

```
public virtual bool CanRequestPackageInstalls ();
	public virtual void ClearInstantAppCookie ();
	public virtual ChangedPackages GetChangedPackages (int sequenceNumber);
	public virtual byte[] GetInstantAppCookie ();
	public virtual PackageInfo GetPackageInfo (VersionedPackage versionedPackage, PackageInfoFlags flags);
	public virtual System.Collections.Generic.IList<SharedLibraryInfo> GetSharedLibraries (PackageInstallReason flags);
	public virtual bool InvokeIsInstantApp (string packageName);
	public virtual void SetApplicationCategoryHint (string packageName, int categoryHint);
	public virtual void UpdateInstantAppCookie (byte[] cookie);
```





### Type Changed: Android.Content.PM.Protection

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FlagRuntimeOnly = 8192,</span>
</pre>





### Type Changed: Android.Content.PM.ResolveInfo

Added property:

```
public bool IsInstantAppAvailable { get; set; }
```





### Type Changed: Android.Content.PM.ShortcutManager

Added property:

```
public virtual bool IsRequestPinShortcutSupported { get; }
```



Added methods:

```
public virtual Android.Content.Intent CreateShortcutResultIntent (ShortcutInfo shortcut);
	public virtual bool RequestPinShortcut (ShortcutInfo shortcut, Android.Content.IntentSender resultIntent);
```





### New Type Android.Content.PM.ActivityColorMode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ActivityColorMode {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hdr = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WideColorGamut = 1,</span>
}
</pre>



### New Type Android.Content.PM.ApplicationCategories

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ApplicationCategories {
	<span class='added added-field ' data-is-non-breaking="">Audio = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Game = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Maps = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">News = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Productivity = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Social = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>



### New Type Android.Content.PM.ChangedPackages

<pre class='added' data-is-non-breaking="">
public sealed class ChangedPackages : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ChangedPackages (int sequenceNumber, System.Collections.Generic.IList&lt;string&gt; packageNames);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;string&gt; PackageNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int SequenceNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Content.PM.PackageInstallReason

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PackageInstallReason {
	<span class='added added-field ' data-is-non-breaking="">DeviceRestore = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">DeviceSetup = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Policy = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">User = 4,</span>
}
</pre>



### New Type Android.Content.PM.PinItemRequestType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PinItemRequestType {
	<span class='added added-field ' data-is-non-breaking="">Appwidget = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Shortcut = 1,</span>
}
</pre>



### New Type Android.Content.PM.SharedLibraryInfo

<pre class='added' data-is-non-breaking="">
public sealed class SharedLibraryInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Content.PM.SharedLibraryType enum directly instead of this field.")]
	public static const SharedLibraryType TypeBuiltin;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Content.PM.SharedLibraryType enum directly instead of this field.")]
	public static const SharedLibraryType TypeDynamic;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Content.PM.SharedLibraryType enum directly instead of this field.")]
	public static const SharedLibraryType TypeStatic;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int VersionUndefined;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VersionedPackage DeclaringPackage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;VersionedPackage&gt; DependentPackages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SharedLibraryType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Version { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Content.PM.SharedLibraryType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SharedLibraryType {
	<span class='added added-field ' data-is-non-breaking="">Builtin = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Dynamic = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Static = 2,</span>
}
</pre>



### New Type Android.Content.PM.VersionedPackage

<pre class='added' data-is-non-breaking="">
public sealed class VersionedPackage : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VersionedPackage (string packageName, int versionCode);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string PackageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int VersionCode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.Configuration

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeHdrMask;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeHdrNo;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeHdrShift;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeHdrUndefined;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeHdrYes;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeUndefined;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeWideColorGamutMask;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeWideColorGamutNo;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeWideColorGamutUndefined;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.ColorMode enum directly instead of this field.")]
	public static const ColorMode ColorModeWideColorGamutYes;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.UiMode enum directly instead of this field.")]
	public static const UiMode UiModeTypeVrHeadset;
```



Added properties:

```
public ColorMode ColorMode { get; set; }
	public bool IsScreenHdr { get; }
	public bool IsScreenWideColorGamut { get; }
```





### Type Changed: Android.Content.Res.Resources

Added method:

```
public virtual Android.Graphics.Typeface GetFont (int id);
```





### Type Changed: Android.Content.Res.TypedArray

Added method:

```
public virtual Android.Graphics.Typeface GetFont (int index);
```





### Type Changed: Android.Content.Res.UiMode

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TypeVrHeadset = 7,</span>
</pre>





### New Type Android.Content.Res.ColorMode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ColorMode {
	<span class='added added-field ' data-is-non-breaking="">HdrMask = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">HdrNo = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HdrShift = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HdrUndefined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">HdrYes = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WideColorGamutMask = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">WideColorGamutNo = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">WideColorGamutUndefined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WideColorGamutYes = 2,</span>
}
</pre>





## Namespace Android.Graphics

### Type Changed: Android.Graphics.Bitmap

Added property:

```
public ColorSpace ColorSpace { get; }
```



Added methods:

```
public static Bitmap CreateBitmap (int width, int height, Bitmap.Config config, bool hasAlpha);
	public static Bitmap CreateBitmap (Android.Util.DisplayMetrics display, int width, int height, Bitmap.Config config, bool hasAlpha);
	public static Bitmap CreateBitmap (int width, int height, Bitmap.Config config, bool hasAlpha, ColorSpace colorSpace);
	public static Bitmap CreateBitmap (Android.Util.DisplayMetrics display, int width, int height, Bitmap.Config config, bool hasAlpha, ColorSpace colorSpace);
```



### Type Changed: Android.Graphics.Bitmap.Config

Added properties:

```
public static Bitmap.Config Hardware { get; }
	public static Bitmap.Config RgbaF16 { get; }
```







### Type Changed: Android.Graphics.BitmapFactory

### Type Changed: Android.Graphics.BitmapFactory.Options

Added properties:

```
public ColorSpace InPreferredColorSpace { get; set; }
	public ColorSpace OutColorSpace { get; set; }
	public Bitmap.Config OutConfig { get; set; }
```







### Type Changed: Android.Graphics.Canvas

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool ClipPath (Path path, Region.Op op);
	[Obsolete ("deprecated")]
	public virtual bool ClipRect (Rect rect, Region.Op op);
	[Obsolete ("deprecated")]
	public virtual bool ClipRect (RectF rect, Region.Op op);
	[Obsolete ("deprecated")]
	public virtual bool ClipRect (float left, float top, float right, float bottom, Region.Op op);
	[Obsolete ("deprecated")]
	public virtual int Save (SaveFlags saveFlags);
	[Obsolete ("deprecated")]
	public virtual int SaveLayer (RectF bounds, Paint paint, SaveFlags saveFlags);
	[Obsolete ("deprecated")]
	public virtual int SaveLayer (float left, float top, float right, float bottom, Paint paint, SaveFlags saveFlags);
	[Obsolete ("deprecated")]
	public virtual int SaveLayerAlpha (RectF bounds, int alpha, SaveFlags saveFlags);
	[Obsolete ("deprecated")]
	public virtual int SaveLayerAlpha (float left, float top, float right, float bottom, int alpha, SaveFlags saveFlags);
```

Added methods:

```
public virtual bool ClipOutPath (Path path);
	public virtual bool ClipOutRect (Rect rect);
	public virtual bool ClipOutRect (RectF rect);
	public virtual bool ClipOutRect (int left, int top, int right, int bottom);
	public virtual bool ClipOutRect (float left, float top, float right, float bottom);
```





### Type Changed: Android.Graphics.ColorMatrixColorFilter

Added method:

```
public virtual void GetColorMatrix (ColorMatrix colorMatrix);
```





### Type Changed: Android.Graphics.Format

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Rgba1010102 = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">RgbaF16 = 22,</span>
</pre>





### Type Changed: Android.Graphics.LightingColorFilter

Added properties:

```
public virtual int ColorAdd { get; }
	public virtual int ColorMultiply { get; }
```





### Type Changed: Android.Graphics.Paint

Added property:

```
public virtual string FontVariationSettings { get; }
```



Added method:

```
public virtual bool SetFontVariationSettings (string fontVariationSettings);
```





### Type Changed: Android.Graphics.Path

Added method:

```
public virtual float[] Approximate (float acceptableError);
```





### Type Changed: Android.Graphics.SurfaceTexture

Added constructor:

```
public SurfaceTexture (bool singleBufferMode);
```



Added property:

```
public virtual bool IsReleased { get; }
```





### New Type Android.Graphics.ColorSpace

<pre class='added' data-is-non-breaking="">
public abstract class ColorSpace : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ColorSpace (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int MaxId;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int MinId;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual int ComponentCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int Id { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantD50 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantD55 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantD60 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantD65 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantD75 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;float&gt; IlluminantE { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsSrgb { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsWideGamut { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static ColorSpace Adapt (ColorSpace colorSpace, float[] whitePoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ColorSpace Adapt (ColorSpace colorSpace, float[] whitePoint, ColorSpace.Adaptation adaptation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Connector Connect (ColorSpace source);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Connector Connect (ColorSpace source, ColorSpace destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Connector Connect (ColorSpace source, ColorSpace.RenderIntent intent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Connector Connect (ColorSpace source, ColorSpace destination, ColorSpace.RenderIntent intent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float[] FromXyz (float[] v);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float[] FromXyz (float x, float y, float z);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ColorSpace Get (ColorSpace.Named name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float GetMaxValue (int component);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float GetMinValue (int component);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ColorSpace.Model GetModel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static ColorSpace Match (float[] toXYZD50, ColorSpace.Rgb.TransferParameters function);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float[] ToXyz (float[] v);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float[] ToXyz (float r, float g, float b);</span>

	// inner types
	public sealed class Adaptation : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Adaptation Bradford { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Adaptation Ciecat02 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Adaptation VonKries { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Adaptation ValueOf (string name);</span>
		<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Adaptation[] Values ();</span>
	}
	public class Connector : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected ColorSpace (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public virtual ColorSpace Destination { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual ColorSpace.RenderIntent RenderIntent { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual ColorSpace Source { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] Transform (float[] v);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] Transform (float r, float g, float b);</span>
	}
	public sealed class Model : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Model Cmyk { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public int ComponentCount { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Model Lab { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Model Rgb { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Model Xyz { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Model ValueOf (string name);</span>
		<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Model[] Values ();</span>
	}
	public sealed class Named : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named Aces { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named Acescg { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named AdobeRgb { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named Bt2020 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named Bt709 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named CieLab { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named CieXyz { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named DciP3 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named DisplayP3 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named ExtendedSrgb { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named LinearExtendedSrgb { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named LinearSrgb { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named Ntsc1953 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named ProPhotoRgb { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named SmpteC { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.Named Srgb { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Named ValueOf (string name);</span>
		<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.Named[] Values ();</span>
	}
	public sealed class RenderIntent : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.RenderIntent Absolute { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.RenderIntent Perceptual { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.RenderIntent Relative { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ColorSpace.RenderIntent Saturation { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.RenderIntent ValueOf (string name);</span>
		<span class='added added-method ' data-is-non-breaking="">public static ColorSpace.RenderIntent[] Values ();</span>
	}
	public class Rgb : Android.Graphics.ColorSpace, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected ColorSpace (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		<span class='added added-constructor ' data-is-non-breaking="">public ColorSpace (string name, float[] toXYZ, ColorSpace.Rgb.TransferParameters function);</span>
		<span class='added added-constructor ' data-is-non-breaking="">public ColorSpace (string name, float[] toXYZ, double gamma);</span>
		<span class='added added-constructor ' data-is-non-breaking="">public ColorSpace (string name, float[] toXYZ, Java.Util.Functions.IDoubleUnaryOperator oetf, Java.Util.Functions.IDoubleUnaryOperator eotf);</span>
		<span class='added added-constructor ' data-is-non-breaking="">public ColorSpace (string name, float[] primaries, float[] whitePoint, ColorSpace.Rgb.TransferParameters function);</span>
		<span class='added added-constructor ' data-is-non-breaking="">public ColorSpace (string name, float[] primaries, float[] whitePoint, double gamma);</span>
		<span class='added added-constructor ' data-is-non-breaking="">public ColorSpace (string name, float[] primaries, float[] whitePoint, Java.Util.Functions.IDoubleUnaryOperator oetf, Java.Util.Functions.IDoubleUnaryOperator eotf, float min, float max);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public virtual Java.Util.Functions.IDoubleUnaryOperator Eotf { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override bool IsWideGamut { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual Java.Util.Functions.IDoubleUnaryOperator Oetf { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] FromLinear (float[] v);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] FromLinear (float r, float g, float b);</span>
		<span class='added added-method ' data-is-non-breaking="">public override float[] FromXyz (float[] v);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetInverseTransform ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetInverseTransform (float[] inverseTransform);</span>
		<span class='added added-method ' data-is-non-breaking="">public override float GetMaxValue (int component);</span>
		<span class='added added-method ' data-is-non-breaking="">public override float GetMinValue (int component);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetPrimaries ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetPrimaries (float[] primaries);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual ColorSpace.Rgb.TransferParameters GetTransferParameters ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetTransform ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetTransform (float[] transform);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetWhitePoint ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetWhitePoint (float[] whitePoint);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] ToLinear (float[] v);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual float[] ToLinear (float r, float g, float b);</span>
		<span class='added added-method ' data-is-non-breaking="">public override float[] ToXyz (float[] v);</span>

		// inner types
		public class TransferParameters : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
			// constructors
			<span class='added added-constructor ' data-is-non-breaking="">protected ColorSpace (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
			<span class='added added-constructor ' data-is-non-breaking="">public ColorSpace (double a, double b, double c, double d, double g);</span>
			<span class='added added-constructor ' data-is-non-breaking="">public ColorSpace (double a, double b, double c, double d, double e, double f, double g);</span>
			// properties
			<span class='added added-property ' data-is-non-breaking="">public double A { get; set; }</span>
			<span class='added added-property ' data-is-non-breaking="">public double B { get; set; }</span>
			<span class='added added-property ' data-is-non-breaking="">public double C { get; set; }</span>
			<span class='added added-property ' data-is-non-breaking="">public double D { get; set; }</span>
			<span class='added added-property ' data-is-non-breaking="">public double E { get; set; }</span>
			<span class='added added-property ' data-is-non-breaking="">public double F { get; set; }</span>
			<span class='added added-property ' data-is-non-breaking="">public double G { get; set; }</span>
			<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
			<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
			<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		}
	}
}
</pre>





## Namespace Android.Graphics.Drawables

### Type Changed: Android.Graphics.Drawables.Icon

Added method:

```
public static Icon CreateWithAdaptiveBitmap (Android.Graphics.Bitmap bits);
```





### Type Changed: Android.Graphics.Drawables.InsetDrawable

Added constructors:

```
public InsetDrawable (Drawable drawable, float inset);
	public InsetDrawable (Drawable drawable, float insetLeftFraction, float insetTopFraction, float insetRightFraction, float insetBottomFraction);
```





### New Type Android.Graphics.Drawables.AdaptiveIconDrawable

<pre class='added' data-is-non-breaking="">
public class AdaptiveIconDrawable : Android.Graphics.Drawables.Drawable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AdaptiveIconDrawable (Drawable backgroundDrawable, Drawable foregroundDrawable);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AdaptiveIconDrawable (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Drawable Background { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static float ExtraInsetFraction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Drawable Foreground { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Android.Graphics.Path IconMask { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override int Opacity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override void Draw (Android.Graphics.Canvas canvas);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InvalidateDrawable (Drawable who);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleDrawable (Drawable who, Java.Lang.IRunnable what, long when);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void SetAlpha (int alpha);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void SetColorFilter (Android.Graphics.ColorFilter colorFilter);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetOpacity (int opacity);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnscheduleDrawable (Drawable who, Java.Lang.IRunnable what);</span>
}
</pre>





## Namespace Android.Graphics.Drawables.Shapes

### Type Changed: Android.Graphics.Drawables.Shapes.ArcShape

Added properties:

```
public float StartAngle { get; }
	public float SweepAngle { get; }
```







## Namespace Android.Hardware

### Type Changed: Android.Hardware.Sensor

Added fields:

```
public static const string StringTypeAccelerometerUncalibrated = "android.sensor.accelerometer_uncalibrated";
	public static const string StringTypeLowLatencyOffbodyDetect = "android.sensor.low_latency_offbody_detect";
```



Added property:

```
public virtual SensorDirectRateLevel HighestDirectReportRateLevel { get; }
```



Added method:

```
public virtual bool IsDirectChannelTypeSupported (SensorDirectChannelType sharedMemType);
```





### Type Changed: Android.Hardware.SensorManager

Added methods:

```
public virtual SensorDirectChannel CreateDirectChannel (HardwareBuffer mem);
	public virtual SensorDirectChannel CreateDirectChannel (Android.OS.MemoryFile mem);
```





### Type Changed: Android.Hardware.SensorType

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AccelerometerUncalibrated = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">LowLatencyOffbodyDetect = 34,</span>
</pre>





### New Type Android.Hardware.HardwareBuffer

<pre class='added' data-is-non-breaking="">
public sealed class HardwareBuffer : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageCpuReadOften;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageCpuReadRarely;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageCpuWriteOften;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageCpuWriteRarely;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageGpuColorOutput;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageGpuDataBuffer;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageGpuSampledImage;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageProtectedContent;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageSensorDirectData;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const long UsageVideoEncode;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HardwareBufferFormat Format { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsClosed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Layers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Hardware.HardwareBufferFormat

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HardwareBufferFormat {
	<span class='added added-field ' data-is-non-breaking="">Blob = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgb565 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgb888 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba1010102 = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba8888 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RgbaFp16 = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgbx8888 = 2,</span>
}
</pre>



### New Type Android.Hardware.SensorDirectChannel

<pre class='added' data-is-non-breaking="">
public sealed class SensorDirectChannel : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ICloseable, Java.Interop.IJavaPeerable, Java.Nio.Channels.IChannel, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOpen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public int Configure (Sensor sensor, SensorDirectRateLevel rateLevel);</span>
}
</pre>



### New Type Android.Hardware.SensorDirectChannelType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SensorDirectChannelType {
	<span class='added added-field ' data-is-non-breaking="">HardwareBuffer = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MemoryFile = 1,</span>
}
</pre>



### New Type Android.Hardware.SensorDirectRateLevel

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SensorDirectRateLevel {
	<span class='added added-field ' data-is-non-breaking="">Fast = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Stop = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">VeryFast = 3,</span>
}
</pre>





## Namespace Android.Hardware.Camera2

### Type Changed: Android.Hardware.Camera2.CameraCaptureSession

Added method:

```
public virtual void FinalizeOutputConfigurations (System.Collections.Generic.IList<Params.OutputConfiguration> outputConfigs);
```



### Type Changed: Android.Hardware.Camera2.CameraCaptureSession.StateCallback

Added method:

```
public virtual void OnCaptureQueueEmpty (CameraCaptureSession session);
```







### Type Changed: Android.Hardware.Camera2.CaptureRequest

Added property:

```
public static CaptureRequest.Key ControlEnableZsl { get; }
```





### Type Changed: Android.Hardware.Camera2.CaptureResult

Added property:

```
public static CaptureResult.Key ControlEnableZsl { get; }
```







## Namespace Android.Hardware.Camera2.Params

### Type Changed: Android.Hardware.Camera2.Params.OutputConfiguration

Added property:

```
public System.Collections.Generic.IList<Android.Views.Surface> Surfaces { get; }
```



Added methods:

```
public void AddSurface (Android.Views.Surface surface);
	public void EnableSurfaceSharing ();
```







## Namespace Android.Hardware.Usb

### Type Changed: Android.Hardware.Usb.UsbDeviceConnection

Added methods:

```
public virtual UsbRequest RequestWait (long timeout);
	public System.Threading.Tasks.Task<UsbRequest> RequestWaitAsync (long timeout);
```





### Type Changed: Android.Hardware.Usb.UsbRequest

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool Queue (Java.Nio.ByteBuffer buffer, int length);
```

Added method:

```
public virtual bool Queue (Java.Nio.ByteBuffer buffer);
```







## Namespace Android.Icu.Lang

### Type Changed: Android.Icu.Lang.UCharacter

### Type Changed: Android.Icu.Lang.UCharacter.GraphemeClusterBreak

Added fields:

```
public static const int EBase;
	public static const int EBaseGaz;
	public static const int EModifier;
	public static const int GlueAfterZwj;
	public static const int Zwj;
```





### Type Changed: Android.Icu.Lang.UCharacter.JoiningGroup

Added fields:

```
public static const int AfricanFeh;
	public static const int AfricanNoon;
	public static const int AfricanQaf;
```





### Type Changed: Android.Icu.Lang.UCharacter.LineBreak

Added fields:

```
public static const int EBase;
	public static const int EModifier;
	public static const int Zwj;
```





### Type Changed: Android.Icu.Lang.UCharacter.UnicodeBlock

Added fields:

```
public static const int AdlamId;
	public static const int BhaiksukiId;
	public static const int CyrillicExtendedCId;
	public static const int GlagoliticSupplementId;
	public static const int IdeographicSymbolsAndPunctuationId;
	public static const int MarchenId;
	public static const int MongolianSupplementId;
	public static const int NewaId;
	public static const int OsageId;
	public static const int TangutComponentsId;
	public static const int TangutId;
```



Added properties:

```
public static UCharacter.UnicodeBlock Adlam { get; }
	public static UCharacter.UnicodeBlock Bhaiksuki { get; }
	public static UCharacter.UnicodeBlock CyrillicExtendedC { get; }
	public static UCharacter.UnicodeBlock GlagoliticSupplement { get; }
	public static UCharacter.UnicodeBlock IdeographicSymbolsAndPunctuation { get; }
	public static UCharacter.UnicodeBlock Marchen { get; }
	public static UCharacter.UnicodeBlock MongolianSupplement { get; }
	public static UCharacter.UnicodeBlock Newa { get; }
	public static UCharacter.UnicodeBlock Osage { get; }
	public static UCharacter.UnicodeBlock Tangut { get; }
	public static UCharacter.UnicodeBlock TangutComponents { get; }
```





### Type Changed: Android.Icu.Lang.UCharacter.WordBreak

Added fields:

```
public static const int EBase;
	public static const int EBaseGaz;
	public static const int EModifier;
	public static const int GlueAfterZwj;
	public static const int Zwj;
```







### Type Changed: Android.Icu.Lang.UScript

Added fields:

```
public static const int Adlam;
	public static const int Bhaiksuki;
	public static const int HanWithBopomofo;
	public static const int Jamo;
	public static const int Marchen;
	public static const int Newa;
	public static const int Osage;
	public static const int SymbolsEmoji;
```







## Namespace Android.Icu.Text

### Type Changed: Android.Icu.Text.DateFormat

### Type Changed: Android.Icu.Text.DateFormat.BooleanAttribute

Added properties:

```
public static DateFormat.BooleanAttribute ParseMultiplePatternsForMatch { get; }
	public static DateFormat.BooleanAttribute ParsePartialLiteralMatch { get; }
```







### Type Changed: Android.Icu.Text.LocaleDisplayNames

Added methods:

```
public virtual System.Collections.Generic.IList<LocaleDisplayNames.UiListItem> GetUiList (System.Collections.Generic.ICollection<Android.Icu.Util.ULocale> localeSet, bool inSelf, Java.Util.IComparator collator);
	public virtual System.Collections.Generic.IList<LocaleDisplayNames.UiListItem> GetUiListCompareWholeItems (System.Collections.Generic.ICollection<Android.Icu.Util.ULocale> localeSet, Java.Util.IComparator comparator);
```



### New Type Android.Icu.Text.UiListItem

<pre class='added' data-is-non-breaking="">
public class UiListItem : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected LocaleDisplayNames (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public LocaleDisplayNames (Android.Icu.Util.ULocale minimized, Android.Icu.Util.ULocale modified, string nameInDisplayLocale, string nameInSelf);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Icu.Util.ULocale Minimized { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Icu.Util.ULocale Modified { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string NameInDisplayLocale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string NameInSelf { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Java.Util.IComparator GetComparator (Java.Util.IComparator comparator, bool inSelf);</span>
}
</pre>





### Type Changed: Android.Icu.Text.MeasureFormat

Added method:

```
public virtual Java.Lang.StringBuilder FormatMeasurePerUnit (Android.Icu.Util.Measure measure, Android.Icu.Util.MeasureUnit perUnit, Java.Lang.StringBuilder appendTo, Java.Text.FieldPosition pos);
```





### Type Changed: Android.Icu.Text.NumberFormat

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Text.NumberFormatStyles enum directly instead of this field.")]
	public static const NumberFormatStyles Standardcurrencystyle;
```





### Type Changed: Android.Icu.Text.NumberFormatStyles

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Standardcurrency = 9,</span>
</pre>





### New Type Android.Icu.Text.ListFormatter

<pre class='added' data-is-non-breaking="">
public sealed class ListFormatter : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static ListFormatter Instance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public string Format (Java.Lang.Object[] items);</span>
	<span class='added added-method ' data-is-non-breaking="">public string Format (System.Collections.Generic.ICollection&lt;object&gt; items);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ListFormatter GetInstance (Android.Icu.Util.ULocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ListFormatter GetInstance (Java.Util.Locale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public string GetPatternForNumItems (int count);</span>
}
</pre>



### New Type Android.Icu.Text.ScientificNumberFormatter

<pre class='added' data-is-non-breaking="">
public sealed class ScientificNumberFormatter : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public string Format (Java.Lang.Object number);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ScientificNumberFormatter GetMarkupInstance (DecimalFormat df, string beginMarkup, string endMarkup);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ScientificNumberFormatter GetMarkupInstance (Android.Icu.Util.ULocale locale, string beginMarkup, string endMarkup);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ScientificNumberFormatter GetSuperscriptInstance (DecimalFormat df);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ScientificNumberFormatter GetSuperscriptInstance (Android.Icu.Util.ULocale locale);</span>
}
</pre>





## Namespace Android.Icu.Util

### Type Changed: Android.Icu.Util.Calendar

Obsoleted fields:

```
[Obsolete ("deprecated")]
	protected static const int BaseFieldCount;
	[Obsolete ("deprecated")]
	protected static const int MaxFieldCount;
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	protected virtual int ComputeMillisInDay ();
	[Obsolete ("deprecated")]
	protected virtual int ComputeZoneOffset (long millis, int millisInDay);
```



### Type Changed: Android.Icu.Util.MeasureUnit

Added properties:

```
public static MeasureUnit Century { get; }
	public static MeasureUnit CupMetric { get; }
	public static MeasureUnit GenericTemperature { get; }
	public static MeasureUnit Knot { get; }
	public static MeasureUnit LiterPer100kilometers { get; }
	public static MeasureUnit MileScandinavian { get; }
	public static MeasureUnit PintMetric { get; }
	public static MeasureUnit RevolutionAngle { get; }
```





### Type Changed: Android.Icu.Util.TimeZone

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.TimeZoneType enum directly instead of this field.")]
	public static const TimeZoneType TimezoneIcu;

	[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.TimeZoneType enum directly instead of this field.")]
	public static const TimeZoneType TimezoneJdk;
```





### Type Changed: Android.Icu.Util.VersionInfo

Added property:

```
public static VersionInfo Unicode90 { get; }
```





### New Type Android.Icu.Util.EthiopicCalendar

<pre class='added' data-is-non-breaking="">
public sealed class EthiopicCalendar : Android.Icu.Util.CECalendar, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.ICloneable, Java.Lang.IComparable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar (TimeZone zone);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar (ULocale locale);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar (Java.Util.Date date);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar (Java.Util.Locale aLocale);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar (TimeZone zone, ULocale locale);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar (TimeZone zone, Java.Util.Locale aLocale);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar (int year, int month, int date);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EthiopicCalendar (int year, int month, int date, int hour, int minute, int second);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int Genbot;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Hamle;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Hedar;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Megabit;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Meskerem;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Miazia;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Nehasse;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Pagumen;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Sene;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Tahsas;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Tekemt;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Ter;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Yekatit;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool AmeteAlemEra { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("deprecated")]
	protected override int HandleGetExtendedYear ();</span>
}
</pre>



### New Type Android.Icu.Util.TimeZoneType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TimeZoneType {
	<span class='added added-field ' data-is-non-breaking="">Icu = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Jdk = 1,</span>
}
</pre>



### New Type Android.Icu.Util.UniversalTimeScale

<pre class='added' data-is-non-breaking="">
public sealed class UniversalTimeScale : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType Db2Time;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType DotnetDateTime;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleValue enum directly instead of this field.")]
	public static const UniversalTimeScaleValue EpochOffsetPlus1Value;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleValue enum directly instead of this field.")]
	public static const UniversalTimeScaleValue EpochOffsetValue;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType ExcelTime;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleValue enum directly instead of this field.")]
	public static const UniversalTimeScaleValue FromMaxValue;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleValue enum directly instead of this field.")]
	public static const UniversalTimeScaleValue FromMinValue;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType Icu4cTime;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType JavaTime;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType MacOldTime;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType MacTime;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType MaxScale;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleValue enum directly instead of this field.")]
	public static const UniversalTimeScaleValue ToMaxValue;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleValue enum directly instead of this field.")]
	public static const UniversalTimeScaleValue ToMinValue;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleValue enum directly instead of this field.")]
	public static const UniversalTimeScaleValue UnitsValue;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType UnixMicrosecondsTime;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType UnixTime;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.Icu.Util.UniversalTimeScaleType enum directly instead of this field.")]
	public static const UniversalTimeScaleType WindowsFileTime;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Android.Icu.Math.BigDecimal BigDecimalFrom (Android.Icu.Math.BigDecimal otherTime, UniversalTimeScaleType timeScale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Android.Icu.Math.BigDecimal BigDecimalFrom (double otherTime, UniversalTimeScaleType timeScale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Android.Icu.Math.BigDecimal BigDecimalFrom (long otherTime, UniversalTimeScaleType timeScale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static long From (long otherTime, UniversalTimeScaleType timeScale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static long GetTimeScaleValue (UniversalTimeScaleType scale, UniversalTimeScaleValue value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Android.Icu.Math.BigDecimal ToBigDecimal (Android.Icu.Math.BigDecimal universalTime, UniversalTimeScaleType timeScale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Android.Icu.Math.BigDecimal ToBigDecimal (long universalTime, UniversalTimeScaleType timeScale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static long ToLong (long universalTime, UniversalTimeScaleType timeScale);</span>
}
</pre>



### New Type Android.Icu.Util.UniversalTimeScaleType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UniversalTimeScaleType {
	<span class='added added-field ' data-is-non-breaking="">Db2Time = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">DotnetDateTime = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ExcelTime = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Icu4cTime = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">JavaTime = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">MacOldTime = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">MacTime = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">MaxScale = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">UnixMicrosecondsTime = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">UnixTime = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">WindowsFileTime = 3,</span>
}
</pre>



### New Type Android.Icu.Util.UniversalTimeScaleValue

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UniversalTimeScaleValue {
	<span class='added added-field ' data-is-non-breaking="">EpochOffset = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">EpochOffsetPlus1 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FromMax = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FromMin = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ToMax = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">ToMin = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Units = 0,</span>
}
</pre>





## Namespace Android.Locations

### Type Changed: Android.Locations.GnssMeasurement

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Locations.GnssState enum directly instead of this field.")]
	public static const GnssState StateGloTodKnown;

	[Obsolete ("This constant will be removed in the future version. Use Android.Locations.GnssState enum directly instead of this field.")]
	public static const GnssState StateTowKnown;
```



Added properties:

```
public double AutomaticGainControlLevelDb { get; }
	public bool HasAutomaticGainControlLevelDb { get; }
```





### Type Changed: Android.Locations.GnssState

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">GloTodKnown = 32768,</span>
	<span class='added added-field ' data-is-non-breaking="">TowKnown = 16384,</span>
</pre>





### Type Changed: Android.Locations.GnssStatus

Added methods:

```
public float GetCarrierFrequencyHz (int satIndex);
	public bool HasCarrierFrequencyHz (int satIndex);
```





### Type Changed: Android.Locations.Location

Added properties:

```
public virtual float BearingAccuracyDegrees { get; set; }
	public virtual bool HasBearingAccuracy { get; }
	public virtual bool HasSpeedAccuracy { get; }
	public virtual bool HasVerticalAccuracy { get; }
	public virtual float SpeedAccuracyMetersPerSecond { get; set; }
	public virtual float VerticalAccuracyMeters { get; set; }
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void RemoveAccuracy ();
	[Obsolete ("deprecated")]
	public virtual void RemoveAltitude ();
	[Obsolete ("deprecated")]
	public virtual void RemoveBearing ();
	[Obsolete ("deprecated")]
	public virtual void RemoveSpeed ();
```





## Namespace Android.Media

### Type Changed: Android.Media.AudioAttributes

Added property:

```
public Stream VolumeControlStream { get; }
```





### Type Changed: Android.Media.AudioDeviceType

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UsbHeadset = 22,</span>
</pre>





### Type Changed: Android.Media.AudioFocus

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
</pre>





### Type Changed: Android.Media.AudioFocusRequest

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Delayed = 2,</span>
</pre>





### Type Changed: Android.Media.AudioManager

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.AudioFocus enum directly instead of this field.")]
	public static const AudioFocus AudiofocusNone;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.AudioFocusRequest enum directly instead of this field.")]
	public static const AudioFocusRequest AudiofocusRequestDelayed;
	public static const int StreamAccessibility;
```



Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual bool BluetoothA2dpOn { get; set; }
```

Added property:

```
public virtual System.Collections.Generic.IList<AudioPlaybackConfiguration> ActivePlaybackConfigurations { get; }
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual AudioFocusRequest AbandonAudioFocus (AudioManager.IOnAudioFocusChangeListener l);
	[Obsolete ("deprecated")]
	public virtual AudioFocusRequest RequestAudioFocus (AudioManager.IOnAudioFocusChangeListener l, Stream streamType, AudioFocus durationHint);
```

Added methods:

```
public virtual AudioFocusRequest AbandonAudioFocusRequest (AudioFocusRequestClass focusRequest);
	public virtual void RegisterAudioPlaybackCallback (AudioManager.AudioPlaybackCallback cb, Android.OS.Handler handler);
	public virtual AudioFocusRequest RequestAudioFocus (AudioFocusRequestClass focusRequest);
	public virtual void UnregisterAudioPlaybackCallback (AudioManager.AudioPlaybackCallback cb);
```



### New Type Android.Media.AudioPlaybackCallback

<pre class='added' data-is-non-breaking="">
public abstract class AudioPlaybackCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AudioManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AudioManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnPlaybackConfigChanged (System.Collections.Generic.IList&lt;AudioPlaybackConfiguration&gt; configs);</span>
}
</pre>





### Type Changed: Android.Media.AudioTrack

Added interface:

```
IVolumeAutomation
```



Added property:

```
public virtual AudioTrackPerformanceMode PerformanceMode { get; }
```



Added method:

```
public virtual VolumeShaper CreateVolumeShaper (VolumeShaper.Configuration configuration);
```



### Type Changed: Android.Media.AudioTrack.Builder

Added method:

```
public virtual AudioTrack.Builder SetPerformanceMode (AudioTrackPerformanceMode performanceMode);
```







### Type Changed: Android.Media.AudioUsageKind

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Assistant = 16,</span>
</pre>





### Type Changed: Android.Media.ExifInterface

Added fields:

```
public static const string TagDefaultCropSize = "DefaultCropSize";
	public static const string TagDngVersion = "DNGVersion";
	public static const string TagNewSubfileType = "NewSubfileType";
	public static const string TagOrfAspectFrame = "AspectFrame";
	public static const string TagOrfPreviewImageLength = "PreviewImageLength";
	public static const string TagOrfPreviewImageStart = "PreviewImageStart";
	public static const string TagOrfThumbnailImage = "ThumbnailImage";
	public static const string TagRw2Iso = "ISO";
	public static const string TagRw2JpgFromRaw = "JpgFromRaw";
	public static const string TagRw2SensorBottomBorder = "SensorBottomBorder";
	public static const string TagRw2SensorLeftBorder = "SensorLeftBorder";
	public static const string TagRw2SensorRightBorder = "SensorRightBorder";
	public static const string TagRw2SensorTopBorder = "SensorTopBorder";
	public static const string TagSubfileType = "SubfileType";
```



Added properties:

```
public virtual bool IsThumbnailCompressed { get; }
	public virtual Android.Graphics.Bitmap ThumbnailBitmap { get; }
```



Added method:

```
public virtual byte[] GetThumbnailBytes ();
```





### Type Changed: Android.Media.MediaCodec

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecBufferFlags enum directly instead of this field.")]
	public static const MediaCodecBufferFlags BufferFlagPartialFrame;
```



Added property:

```
public Android.OS.PersistableBundle Metrics { get; }
```



Added method:

```
public void Configure (MediaFormat format, Android.Views.Surface surface, MediaCodecConfigFlags flags, MediaDescrambler descrambler);
```



### New Type Android.Media.MetricsConstants

<pre class='added' data-is-non-breaking="">
public sealed class MetricsConstants : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string Codec = "android.media.mediacodec.codec";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Encoder = "android.media.mediacodec.encoder";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Height = "android.media.mediacodec.height";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string MimeType = "android.media.mediacodec.mime";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Mode = "android.media.mediacodec.mode";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ModeAudio = "audio";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ModeVideo = "video";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Rotation = "android.media.mediacodec.rotation";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Secure = "android.media.mediacodec.secure";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Width = "android.media.mediacodec.width";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





### Type Changed: Android.Media.MediaCodecBufferFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">PartialFrame = 8,</span>
</pre>





### Type Changed: Android.Media.MediaCodecInfo

### Type Changed: Android.Media.MediaCodecInfo.CodecCapabilities

Added field:

```
public static const string FEATUREPartialFrame = "partial-frame";
```





### Type Changed: Android.Media.MediaCodecInfo.CodecProfileLevel

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileType enum directly instead of this field.")]
	public static const MediaCodecProfileType AACObjectERScalable;
```







### Type Changed: Android.Media.MediaCodecProfileType

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Aacobjecterscalable = 20,</span>
</pre>





### Type Changed: Android.Media.MediaDescription

Added fields:

```
public static const long BtFolderTypeAlbums;
	public static const long BtFolderTypeArtists;
	public static const long BtFolderTypeGenres;
	public static const long BtFolderTypeMixed;
	public static const long BtFolderTypePlaylists;
	public static const long BtFolderTypeTitles;
	public static const long BtFolderTypeYears;
	public static const string ExtraBtFolderType = "android.media.extra.BT_FOLDER_TYPE";
```





### Type Changed: Android.Media.MediaExtractor

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaExtractorSampleFlags enum directly instead of this field.")]
	public static const MediaExtractorSampleFlags SampleFlagPartialFrame;
```



Added property:

```
public Android.OS.PersistableBundle Metrics { get; }
```



Added methods:

```
public MediaExtractor.CasInfo GetCasInfo (int index);
	public void SetMediaCas (MediaCas mediaCas);
```





### Type Changed: Android.Media.MediaExtractorSampleFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">PartialFrame = 4,</span>
</pre>





### Type Changed: Android.Media.MediaFormat

Added fields:

```
public static const string KeyLatency = "latency";
	public static const string MimetypeAudioScrambled = "audio/scrambled";
	public static const string MimetypeVideoScrambled = "video/scrambled";
```





### Type Changed: Android.Media.MediaInfo

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AudioNotPlaying = 804,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoNotPlaying = 805,</span>
</pre>





### Type Changed: Android.Media.MediaMetadata

Added fields:

```
public static const string MetadataKeyBtFolderType = "android.media.metadata.BT_FOLDER_TYPE";
	public static const string MetadataKeyMediaUri = "android.media.metadata.MEDIA_URI";
```





### Type Changed: Android.Media.MediaMuxer

Added constructor:

```
public MediaMuxer (Java.IO.FileDescriptor fd, MuxerOutputType format);
```



### Type Changed: Android.Media.MediaMuxer.OutputFormat

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MuxerOutputType enum directly instead of this field.")]
	public static const MuxerOutputType MuxerOutput3gpp;
```







### Type Changed: Android.Media.MediaPlayer

Added interface:

```
IVolumeAutomation
```



Added property:

```
public virtual Android.OS.PersistableBundle Metrics { get; }
```



Added events:

```
public event System.EventHandler<MediaPlayer.DrmInfoEventArgs> DrmInfoEvent;
	public event System.EventHandler<MediaPlayer.DrmPreparedEventArgs> DrmPrepared;
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void SetAudioStreamType (Stream streamtype);
```

Added methods:

```
public virtual VolumeShaper CreateVolumeShaper (VolumeShaper.Configuration configuration);
	public virtual MediaPlayer.DrmInfo GetDrmInfo ();
	public virtual string GetDrmPropertyString (string propertyName);
	public virtual MediaDrm.KeyRequest GetKeyRequest (byte[] keySetId, byte[] initData, string mimeType, MediaDrmKeyType keyType, System.Collections.Generic.IDictionary<System.String,System.String> optionalParameters);
	public virtual void PrepareDrm (Java.Util.UUID uuid);
	public virtual byte[] ProvideKeyResponse (byte[] keySetId, byte[] response);
	public virtual void ReleaseDrm ();
	public virtual void RestoreKeys (byte[] keySetId);
	public virtual void SeekTo (long msec, MediaPlayerSeekMode mode);
	public virtual void SetDataSource (Android.Content.Context context, Android.Net.Uri uri, System.Collections.Generic.IDictionary<System.String,System.String> headers, System.Collections.Generic.IList<Java.Net.HttpCookie> cookies);
	public System.Threading.Tasks.Task SetDataSourceAsync (Android.Content.Context context, Android.Net.Uri uri, System.Collections.Generic.IDictionary<System.String,System.String> headers, System.Collections.Generic.IList<Java.Net.HttpCookie> cookies);
	public virtual void SetDrmPropertyString (string propertyName, string value);
	public virtual void SetOnDrmConfigHelper (MediaPlayer.IOnDrmConfigHelper listener);
	public virtual void SetOnDrmInfoListener (MediaPlayer.IOnDrmInfoListener listener);
	public virtual void SetOnDrmInfoListener (MediaPlayer.IOnDrmInfoListener listener, Android.OS.Handler handler);
	public virtual void SetOnDrmPreparedListener (MediaPlayer.IOnDrmPreparedListener listener);
	public virtual void SetOnDrmPreparedListener (MediaPlayer.IOnDrmPreparedListener listener, Android.OS.Handler handler);
```



### New Type Android.Media.DrmInfo

<pre class='added' data-is-non-breaking="">
public sealed class DrmInfo : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IDictionary&lt;Java.Util.UUID,System.Byte[]&gt; Pssh { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public Java.Util.UUID[] GetSupportedSchemes ();</span>
}
</pre>



### New Type Android.Media.DrmInfoEventArgs

<pre class='added' data-is-non-breaking="">
public class DrmInfoEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MediaPlayer (MediaPlayer mp, MediaPlayer.DrmInfo drmInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public MediaPlayer.DrmInfo DrmInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MediaPlayer Mp { get; }</span>
}
</pre>



### New Type Android.Media.DrmPreparedEventArgs

<pre class='added' data-is-non-breaking="">
public class DrmPreparedEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MediaPlayer (MediaPlayer mp, PrepareDrmStatus status);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public MediaPlayer Mp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PrepareDrmStatus Status { get; }</span>
}
</pre>



### New Type Android.Media.IOnDrmConfigHelper

<pre class='added' data-is-non-breaking="">
public interface IOnDrmConfigHelper : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnDrmConfig (MediaPlayer mp);</span>
}
</pre>



### New Type Android.Media.IOnDrmInfoListener

<pre class='added' data-is-non-breaking="">
public interface IOnDrmInfoListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnDrmInfo (MediaPlayer mp, MediaPlayer.DrmInfo drmInfo);</span>
}
</pre>



### New Type Android.Media.IOnDrmPreparedListener

<pre class='added' data-is-non-breaking="">
public interface IOnDrmPreparedListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnDrmPrepared (MediaPlayer mp, PrepareDrmStatus status);</span>
}
</pre>



### New Type Android.Media.MetricsConstants

<pre class='added' data-is-non-breaking="">
public sealed class MetricsConstants : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string CodecAudio = "android.media.mediaplayer.audio.codec";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string CodecVideo = "android.media.mediaplayer.video.codec";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Duration = "android.media.mediaplayer.durationMs";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ErrorCode = "android.media.mediaplayer.errcode";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Errors = "android.media.mediaplayer.err";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Frames = "android.media.mediaplayer.frames";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string FramesDropped = "android.media.mediaplayer.dropped";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Height = "android.media.mediaplayer.height";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string MimeTypeAudio = "android.media.mediaplayer.audio.mime";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string MimeTypeVideo = "android.media.mediaplayer.video.mime";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Playing = "android.media.mediaplayer.playingMs";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Width = "android.media.mediaplayer.width";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Android.Media.NoDrmSchemeException

<pre class='added' data-is-non-breaking="">
public sealed class NoDrmSchemeException : Android.Media.MediaDrmException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MediaPlayer (string detailMessage);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Android.Media.ProvisioningNetworkErrorException

<pre class='added' data-is-non-breaking="">
public sealed class ProvisioningNetworkErrorException : Android.Media.MediaDrmException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MediaPlayer (string detailMessage);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Android.Media.ProvisioningServerErrorException

<pre class='added' data-is-non-breaking="">
public sealed class ProvisioningServerErrorException : Android.Media.MediaDrmException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MediaPlayer (string detailMessage);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





### Type Changed: Android.Media.MediaRecorder

Added property:

```
public virtual Android.OS.PersistableBundle Metrics { get; }
```



Added methods:

```
public virtual void SetNextOutputFile (Java.IO.File file);
	public virtual void SetNextOutputFile (Java.IO.FileDescriptor fd);
	public virtual void SetOutputFile (Java.IO.File file);
	public virtual void SetVideoEncodingProfileLevel (MediaCodecProfileType profile, int level);
```



### New Type Android.Media.MetricsConstants

<pre class='added' data-is-non-breaking="">
public sealed class MetricsConstants : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string AudioBitrate = "android.media.mediarecorder.audio-bitrate";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string AudioChannels = "android.media.mediarecorder.audio-channels";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string AudioSamplerate = "android.media.mediarecorder.audio-samplerate";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string AudioTimescale = "android.media.mediarecorder.audio-timescale";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string CaptureFps = "android.media.mediarecorder.capture-fps";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string CaptureFpsEnable = "android.media.mediarecorder.capture-fpsenable";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Framerate = "android.media.mediarecorder.frame-rate";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Height = "android.media.mediarecorder.height";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string MovieTimescale = "android.media.mediarecorder.movie-timescale";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Rotation = "android.media.mediarecorder.rotation";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VideoBitrate = "android.media.mediarecorder.video-bitrate";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VideoIframeInterval = "android.media.mediarecorder.video-iframe-interval";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VideoLevel = "android.media.mediarecorder.video-encoder-level";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VideoProfile = "android.media.mediarecorder.video-encoder-profile";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VideoTimescale = "android.media.mediarecorder.video-timescale";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string Width = "android.media.mediarecorder.width";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





### Type Changed: Android.Media.MediaRecorderInfo

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MaxFilesizeApproaching = 802,</span>
	<span class='added added-field ' data-is-non-breaking="">NextOutputFileStarted = 803,</span>
</pre>





### Type Changed: Android.Media.MuxerOutputType

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">M3gpp = 2,</span>
</pre>





### Type Changed: Android.Media.OutputFormat

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Mpeg2Ts = 8,</span>
</pre>





### New Type Android.Media.AudioFocusRequestClass

<pre class='added' data-is-non-breaking="">
public sealed class AudioFocusRequestClass : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public AudioAttributes AudioAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AudioFocus FocusGain { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public bool AcceptsDelayedFocusGain ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool WillPauseWhenDucked ();</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public AudioFocusRequestClass (AudioFocus focusGain);</span>
		<span class='added added-constructor ' data-is-non-breaking="">public AudioFocusRequestClass (AudioFocusRequestClass requestToCopy);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public AudioFocusRequestClass Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public AudioFocusRequestClass.Builder SetAcceptsDelayedFocusGain (bool acceptsDelayedFocusGain);</span>
		<span class='added added-method ' data-is-non-breaking="">public AudioFocusRequestClass.Builder SetAudioAttributes (AudioAttributes attributes);</span>
		<span class='added added-method ' data-is-non-breaking="">public AudioFocusRequestClass.Builder SetFocusGain (AudioFocus focusGain);</span>
		<span class='added added-method ' data-is-non-breaking="">public AudioFocusRequestClass.Builder SetOnAudioFocusChangeListener (AudioManager.IOnAudioFocusChangeListener listener);</span>
		<span class='added added-method ' data-is-non-breaking="">public AudioFocusRequestClass.Builder SetOnAudioFocusChangeListener (AudioManager.IOnAudioFocusChangeListener listener, Android.OS.Handler handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public AudioFocusRequestClass.Builder SetWillPauseWhenDucked (bool pauseOnDuck);</span>
	}
}
</pre>



### New Type Android.Media.AudioPlaybackConfiguration

<pre class='added' data-is-non-breaking="">
public sealed class AudioPlaybackConfiguration : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public AudioAttributes AudioAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Media.AudioTrackPerformanceMode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AudioTrackPerformanceMode {
	<span class='added added-field ' data-is-non-breaking="">LowLatency = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PowerSaving = 2,</span>
}
</pre>



### New Type Android.Media.IVolumeAutomation

<pre class='added' data-is-non-breaking="">
public interface IVolumeAutomation : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual VolumeShaper CreateVolumeShaper (VolumeShaper.Configuration configuration);</span>
}
</pre>



### New Type Android.Media.MediaCas

<pre class='added' data-is-non-breaking="">
public sealed class MediaCas : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MediaCas (int CA_system_id);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MediaCas.PluginDescriptor[] EnumeratePlugins ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsSystemIdSupported (int CA_system_id);</span>
	<span class='added added-method ' data-is-non-breaking="">public MediaCas.Session OpenSession ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void ProcessEmm (byte[] data);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ProcessEmm (byte[] data, int offset, int length);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Provision (string provisionString);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RefreshEntitlements (int refreshType, byte[] refreshData);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SendEvent (int e, int arg, byte[] data);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetEventListener (MediaCas.IEventListener listener, Android.OS.Handler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetPrivateData (byte[] data);</span>

	// inner types
	public interface IEventListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnEvent (MediaCas mediaCas, int e, int arg, byte[] data);</span>
	}
	public class MediaCasEventArgs : System.EventArgs {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public MediaCas (MediaCas mediaCas, int e, int arg, byte[] data);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public int Arg { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public byte[] Data { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public int Event { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public MediaCas MediaCas { get; }</span>
	}
	public class PluginDescriptor : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MediaCas (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual int SystemId { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	}
	public sealed class Session : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
		<span class='added added-method ' data-is-non-breaking="">public void ProcessEcm (byte[] data);</span>
		<span class='added added-method ' data-is-non-breaking="">public void ProcessEcm (byte[] data, int offset, int length);</span>
		<span class='added added-method ' data-is-non-breaking="">public void SetPrivateData (byte[] data);</span>
	}
}
</pre>



### New Type Android.Media.MediaCasException

<pre class='added' data-is-non-breaking="">
public class MediaCasException : Java.Lang.Exception, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MediaCasException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>

	// inner types
	public sealed class DeniedByServerException : Android.Media.MediaCasException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	}
	public sealed class NotProvisionedException : Android.Media.MediaCasException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	}
	public sealed class ResourceBusyException : Android.Media.MediaCasException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	}
	public sealed class UnsupportedCasException : Android.Media.MediaCasException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	}
}
</pre>



### New Type Android.Media.MediaCasStateException

<pre class='added' data-is-non-breaking="">
public class MediaCasStateException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MediaCasStateException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string DiagnosticInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Android.Media.MediaDescrambler

<pre class='added' data-is-non-breaking="">
public sealed class MediaDescrambler : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MediaDescrambler (int CA_system_id);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public int Descramble (Java.Nio.ByteBuffer srcBuf, Java.Nio.ByteBuffer dstBuf, MediaCodec.CryptoInfo cryptoInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool RequiresSecureDecoderComponent (string mime);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetMediaCasSession (MediaCas.Session session);</span>
}
</pre>



### New Type Android.Media.MediaPlayerSeekMode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MediaPlayerSeekMode {
	<span class='added added-field ' data-is-non-breaking="">Closest = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ClosestSync = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NextSync = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PreviousSync = 0,</span>
}
</pre>



### New Type Android.Media.PrepareDrmStatus

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PrepareDrmStatus {
	<span class='added added-field ' data-is-non-breaking="">PreparationError = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ProvisioningNetworkError = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ProvisioningServerError = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>



### New Type Android.Media.VolumeInterpolatorType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VolumeInterpolatorType {
	<span class='added added-field ' data-is-non-breaking="">Cubic = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">CubicMonotonic = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Linear = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Step = 0,</span>
}
</pre>



### New Type Android.Media.VolumeShaper

<pre class='added' data-is-non-breaking="">
public sealed class VolumeShaper : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Volume { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Apply (VolumeShaper.Operation operation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Replace (VolumeShaper.Configuration configuration, VolumeShaper.Operation operation, bool join);</span>

	// inner types
	public sealed class Configuration : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static VolumeShaper.Configuration CubicRamp { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public long Duration { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public VolumeInterpolatorType InterpolatorType { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static VolumeShaper.Configuration LinearRamp { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static int MaximumCurvePoints { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static VolumeShaper.Configuration ScurveRamp { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static VolumeShaper.Configuration SineRamp { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
		<span class='added added-method ' data-is-non-breaking="">public float[] GetTimes ();</span>
		<span class='added added-method ' data-is-non-breaking="">public float[] GetVolumes ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

		// inner types
		public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
			// constructors
			<span class='added added-constructor ' data-is-non-breaking="">public VolumeShaper ();</span>
			<span class='added added-constructor ' data-is-non-breaking="">public VolumeShaper (VolumeShaper.Configuration configuration);</span>
			// properties
			<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
			<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
			<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
			// methods
			<span class='added added-method ' data-is-non-breaking="">public VolumeShaper.Configuration Build ();</span>
			<span class='added added-method ' data-is-non-breaking="">public VolumeShaper.Configuration.Builder InvertVolumes ();</span>
			<span class='added added-method ' data-is-non-breaking="">public VolumeShaper.Configuration.Builder ReflectTimes ();</span>
			<span class='added added-method ' data-is-non-breaking="">public VolumeShaper.Configuration.Builder ScaleToEndVolume (float volume);</span>
			<span class='added added-method ' data-is-non-breaking="">public VolumeShaper.Configuration.Builder ScaleToStartVolume (float volume);</span>
			<span class='added added-method ' data-is-non-breaking="">public VolumeShaper.Configuration.Builder SetCurve (float[] times, float[] volumes);</span>
			<span class='added added-method ' data-is-non-breaking="">public VolumeShaper.Configuration.Builder SetDuration (long durationMillis);</span>
			<span class='added added-method ' data-is-non-breaking="">public VolumeShaper.Configuration.Builder SetInterpolatorType (VolumeInterpolatorType interpolatorType);</span>
		}
		public static class InterfaceConsts {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

			<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
		}
	}
	public sealed class Operation : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static VolumeShaper.Operation Play { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static VolumeShaper.Operation Reverse { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

		// inner types
		public static class InterfaceConsts {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

			<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
		}
	}
}
</pre>





## Namespace Android.Media.Browse

### Type Changed: Android.Media.Browse.MediaBrowser

### Type Changed: Android.Media.Browse.MediaBrowser.ItemCallback

Modified methods:

```
public virtual void OnError (string itemId mediaId)
```







## Namespace Android.Media.TV

### Type Changed: Android.Media.TV.TvContract

Added fields:

```
public static const string ActionInitializePrograms = "android.media.tv.action.INITIALIZE_PROGRAMS";
	public static const string ActionPreviewProgramAddedToWatchNext = "android.media.tv.action.PREVIEW_PROGRAM_ADDED_TO_WATCH_NEXT";
	public static const string ActionPreviewProgramBrowsableDisabled = "android.media.tv.action.PREVIEW_PROGRAM_BROWSABLE_DISABLED";
	public static const string ActionRequestChannelBrowsable = "android.media.tv.action.REQUEST_CHANNEL_BROWSABLE";
	public static const string ActionWatchNextProgramBrowsableDisabled = "android.media.tv.action.WATCH_NEXT_PROGRAM_BROWSABLE_DISABLED";
	public static const string ExtraChannelId = "android.media.tv.extra.CHANNEL_ID";
	public static const string ExtraPreviewProgramId = "android.media.tv.extra.PREVIEW_PROGRAM_ID";
	public static const string ExtraWatchNextProgramId = "android.media.tv.extra.WATCH_NEXT_PROGRAM_ID";
```



Added methods:

```
public static Android.Net.Uri BuildPreviewProgramUri (long previewProgramId);
	public static Android.Net.Uri BuildPreviewProgramsUriForChannel (Android.Net.Uri channelUri);
	public static Android.Net.Uri BuildPreviewProgramsUriForChannel (long channelId);
	public static Android.Net.Uri BuildWatchNextProgramUri (long watchNextProgramId);
	public static void RequestChannelBrowsable (Android.Content.Context context, long channelId);
```



### Type Changed: Android.Media.TV.TvContract.Channels

Added fields:

```
public static const string ColumnBrowsable = "browsable";
	public static const string ColumnInternalProviderId = "internal_provider_id";
	public static const string ColumnLocked = "locked";
	public static const string ColumnTransient = "transient";
	public static const string TypePreview = "TYPE_PREVIEW";
```





### Type Changed: Android.Media.TV.TvContract.Programs

Added fields:

```
public static const string ColumnReviewRating = "review_rating";
	public static const string ColumnReviewRatingStyle = "review_rating_style";
```





### Type Changed: Android.Media.TV.TvContract.RecordedPrograms

Added fields:

```
public static const string ColumnReviewRating = "review_rating";
	public static const string ColumnReviewRatingStyle = "review_rating_style";
```





### New Type Android.Media.TV.PreviewPrograms

<pre class='added' data-is-non-breaking="">
public sealed class PreviewPrograms : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnAudioLanguage = "audio_language";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnAuthor = "author";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnAvailability = "availability";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnBrowsable = "browsable";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnCanonicalGenre = "canonical_genre";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnChannelId = "channel_id";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnContentId = "content_id";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnContentRating = "content_rating";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnDurationMillis = "duration_millis";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnEpisodeDisplayNumber = "episode_display_number";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnEpisodeTitle = "episode_title";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnIntentUri = "intent_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInteractionCount = "interaction_count";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInteractionType = "interaction_type";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderData = "internal_provider_data";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderFlag1 = "internal_provider_flag1";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderFlag2 = "internal_provider_flag2";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderFlag3 = "internal_provider_flag3";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderFlag4 = "internal_provider_flag4";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderId = "internal_provider_id";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnItemCount = "item_count";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLastPlaybackPositionMillis = "last_playback_position_millis";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLive = "live";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLogoUri = "logo_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLongDescription = "long_description";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnOfferPrice = "offer_price";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnPosterArtAspectRatio = "poster_art_aspect_ratio";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnPosterArtUri = "poster_art_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnPreviewVideoUri = "preview_video_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnReleaseDate = "release_date";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnReviewRating = "review_rating";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnReviewRatingStyle = "review_rating_style";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnSearchable = "searchable";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnSeasonDisplayNumber = "season_display_number";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnSeasonTitle = "season_title";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnShortDescription = "short_description";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnStartingPrice = "starting_price";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnThumbnailAspectRatio = "poster_thumbnail_aspect_ratio";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnThumbnailUri = "thumbnail_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnTitle = "title";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnTransient = "transient";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnType = "type";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnVersionNumber = "version_number";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnVideoHeight = "video_height";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnVideoWidth = "video_width";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnWeight = "weight";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ContentItemType = "vnd.android.cursor.item/preview_program";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ContentType = "vnd.android.cursor.dir/preview_program";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.Net.Uri ContentUri { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const string ColumnPackageName = "package_name";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string Count = "_count";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string Id = "_id";</span>
	}
}
</pre>



### New Type Android.Media.TV.WatchNextPrograms

<pre class='added' data-is-non-breaking="">
public sealed class WatchNextPrograms : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnAudioLanguage = "audio_language";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnAuthor = "author";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnAvailability = "availability";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnBrowsable = "browsable";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnCanonicalGenre = "canonical_genre";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnContentId = "content_id";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnContentRating = "content_rating";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnDurationMillis = "duration_millis";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnEpisodeDisplayNumber = "episode_display_number";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnEpisodeTitle = "episode_title";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnIntentUri = "intent_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInteractionCount = "interaction_count";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInteractionType = "interaction_type";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderData = "internal_provider_data";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderFlag1 = "internal_provider_flag1";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderFlag2 = "internal_provider_flag2";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderFlag3 = "internal_provider_flag3";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderFlag4 = "internal_provider_flag4";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnInternalProviderId = "internal_provider_id";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnItemCount = "item_count";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLastEngagementTimeUtcMillis = "last_engagement_time_utc_millis";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLastPlaybackPositionMillis = "last_playback_position_millis";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLive = "live";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLogoUri = "logo_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnLongDescription = "long_description";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnOfferPrice = "offer_price";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnPosterArtAspectRatio = "poster_art_aspect_ratio";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnPosterArtUri = "poster_art_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnPreviewVideoUri = "preview_video_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnReleaseDate = "release_date";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnReviewRating = "review_rating";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnReviewRatingStyle = "review_rating_style";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnSearchable = "searchable";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnSeasonDisplayNumber = "season_display_number";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnSeasonTitle = "season_title";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnShortDescription = "short_description";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnStartingPrice = "starting_price";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnThumbnailAspectRatio = "poster_thumbnail_aspect_ratio";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnThumbnailUri = "thumbnail_uri";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnTitle = "title";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnTransient = "transient";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnType = "type";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnVersionNumber = "version_number";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnVideoHeight = "video_height";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnVideoWidth = "video_width";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ColumnWatchNextType = "watch_next_type";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ContentItemType = "vnd.android.cursor.item/watch_next_program";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ContentType = "vnd.android.cursor.dir/watch_next_program";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.Net.Uri ContentUri { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const string ColumnPackageName = "package_name";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string Count = "_count";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string Id = "_id";</span>
	}
}
</pre>





### Type Changed: Android.Media.TV.TvInputInfo

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public Android.Content.Intent CreateSettingsIntent ();
```



### Type Changed: Android.Media.TV.TvInputManager

Added field:

```
public static const string ActionViewRecordingSchedules = "android.media.tv.action.VIEW_RECORDING_SCHEDULES";
```





### New Type Android.Media.TV.PreviewAspectRatio

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PreviewAspectRatio {
	<span class='added added-field ' data-is-non-breaking="">A11 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">A169 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">A23 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">A32 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">A43 = 2,</span>
}
</pre>



### New Type Android.Media.TV.PreviewAvailability

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PreviewAvailability {
	<span class='added added-field ' data-is-non-breaking="">Available = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">FreeWithSubscription = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PaidContent = 2,</span>
}
</pre>



### New Type Android.Media.TV.PreviewInteractionType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PreviewInteractionType {
	<span class='added added-field ' data-is-non-breaking="">Fans = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Followers = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Likes = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Listens = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Thumbs = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Viewers = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Views = 0,</span>
}
</pre>



### New Type Android.Media.TV.PreviewReviewRatingStyle

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PreviewReviewRatingStyle {
	<span class='added added-field ' data-is-non-breaking="">Percentage = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Stars = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ThumbsUpDown = 1,</span>
}
</pre>



### New Type Android.Media.TV.PreviewType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PreviewType {
	<span class='added added-field ' data-is-non-breaking="">Album = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Artist = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Channel = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Clip = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Event = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Movie = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Playlist = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Station = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Track = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">TvEpisode = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">TvSeason = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TvSeries = 1,</span>
}
</pre>



### New Type Android.Media.TV.RecordedReviewRatingStyle

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RecordedReviewRatingStyle {
	<span class='added added-field ' data-is-non-breaking="">Percentage = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Stars = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ThumbsUpDown = 1,</span>
}
</pre>



### New Type Android.Media.TV.ReviewRatingStyle

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ReviewRatingStyle {
	<span class='added added-field ' data-is-non-breaking="">Percentage = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Stars = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ThumbsUpDown = 1,</span>
}
</pre>



### New Type Android.Media.TV.WatchNextAspectRatio

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WatchNextAspectRatio {
	<span class='added added-field ' data-is-non-breaking="">A11 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">A169 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">A23 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">A32 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">A43 = 2,</span>
}
</pre>



### New Type Android.Media.TV.WatchNextAvailability

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WatchNextAvailability {
	<span class='added added-field ' data-is-non-breaking="">Available = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">FreeWithSubscription = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PaidContent = 2,</span>
}
</pre>



### New Type Android.Media.TV.WatchNextInteractionType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WatchNextInteractionType {
	<span class='added added-field ' data-is-non-breaking="">Fans = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Followers = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Likes = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Listens = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Thumbs = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Viewers = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Views = 0,</span>
}
</pre>



### New Type Android.Media.TV.WatchNextReviewRatingStyle

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WatchNextReviewRatingStyle {
	<span class='added added-field ' data-is-non-breaking="">Percentage = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Stars = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ThumbsUpDown = 1,</span>
}
</pre>



### New Type Android.Media.TV.WatchNextType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WatchNextType {
	<span class='added added-field ' data-is-non-breaking="">Album = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Artist = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Channel = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Clip = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Event = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Movie = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Playlist = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Station = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Track = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">TvEpisode = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">TvSeason = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TvSeries = 1,</span>
}
</pre>



### New Type Android.Media.TV.WatchNextWatchNextType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WatchNextWatchNextType {
	<span class='added added-field ' data-is-non-breaking="">Continue = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">New = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Next = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Watchlist = 3,</span>
}
</pre>





## Namespace Android.Net

### Type Changed: Android.Net.ConnectivityManager

Added methods:

```
public virtual MultipathPreference GetMultipathPreference (Network network);
	public virtual void RegisterDefaultNetworkCallback (ConnectivityManager.NetworkCallback networkCallback, Android.OS.Handler handler);
	public virtual void RegisterNetworkCallback (NetworkRequest request, ConnectivityManager.NetworkCallback networkCallback, Android.OS.Handler handler);
	public virtual void RequestNetwork (NetworkRequest request, ConnectivityManager.NetworkCallback networkCallback, Android.OS.Handler handler);
	public virtual void RequestNetwork (NetworkRequest request, ConnectivityManager.NetworkCallback networkCallback, int timeoutMs);
	public virtual void RequestNetwork (NetworkRequest request, ConnectivityManager.NetworkCallback networkCallback, Android.OS.Handler handler, int timeoutMs);
```



### Type Changed: Android.Net.ConnectivityManager.NetworkCallback

Added method:

```
public virtual void OnUnavailable ();
```







### Type Changed: Android.Net.NetworkCapabilities

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Net.TransportType enum directly instead of this field.")]
	public static const TransportType TransportWifiAware;
```





### Type Changed: Android.Net.NetworkRequest

### Type Changed: Android.Net.NetworkRequest.Builder

Added method:

```
public virtual NetworkRequest.Builder SetNetworkSpecifier (NetworkSpecifier networkSpecifier);
```







### Type Changed: Android.Net.TrafficStats

Added method:

```
public static int GetAndSetThreadStatsTag (int tag);
```





### Type Changed: Android.Net.TransportType

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">WifiAware = 5,</span>
</pre>





### New Type Android.Net.MultipathPreference

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MultipathPreference {
	<span class='added added-field ' data-is-non-breaking="">Handover = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Performance = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Reliability = 2,</span>
}
</pre>



### New Type Android.Net.NetworkSpecifier

<pre class='added' data-is-non-breaking="">
public abstract class NetworkSpecifier : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NetworkSpecifier (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





## Namespace Android.Net.Wifi

### Type Changed: Android.Net.Wifi.WifiConfiguration

Added properties:

```
public virtual Android.Net.ProxyInfo HttpProxy { get; set; }
	public bool IsHomeProviderNetwork { get; set; }
```





### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig

Added methods:

```
public virtual Java.Security.Cert.X509Certificate[] GetClientCertificateChain ();
	public virtual void SetClientKeyEntryWithCertificateChain (Java.Security.IPrivateKey privateKey, Java.Security.Cert.X509Certificate[] clientCertificateChain);
```



### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig.Phase2

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Net.Wifi.WifiPhase2Method enum directly instead of this field.")]
	public static const WifiPhase2Method Aka;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.Wifi.WifiPhase2Method enum directly instead of this field.")]
	public static const WifiPhase2Method AkaPrime;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.Wifi.WifiPhase2Method enum directly instead of this field.")]
	public static const WifiPhase2Method Sim;
```







### Type Changed: Android.Net.Wifi.WifiManager

Added property:

```
public virtual System.Collections.Generic.IList<Hotspot2.PasspointConfiguration> PasspointConfigurations { get; }
```



Modified methods:

```
public virtual bool EnableNetwork (int netId, bool disableOthers attemptConnect)
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool PingSupplicant ();
	[Obsolete ("deprecated")]
	public virtual bool SaveConfiguration ();
```

Added methods:

```
public virtual void AddOrUpdatePasspointConfiguration (Hotspot2.PasspointConfiguration config);
	public virtual void RemovePasspointConfiguration (string fqdn);
	public virtual void StartLocalOnlyHotspot (WifiManager.LocalOnlyHotspotCallback callback, Android.OS.Handler handler);
```



### New Type Android.Net.Wifi.LocalOnlyHotspotCallback

<pre class='added' data-is-non-breaking="">
public class LocalOnlyHotspotCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WifiManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WifiManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFailed (LocalOnlyHotspotCallbackErrorCode reason);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnStarted (WifiManager.LocalOnlyHotspotReservation reservation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnStopped ();</span>
}
</pre>



### New Type Android.Net.Wifi.LocalOnlyHotspotReservation

<pre class='added' data-is-non-breaking="">
public class LocalOnlyHotspotReservation : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected WifiManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual WifiConfiguration WifiConfiguration { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
}
</pre>





### Type Changed: Android.Net.Wifi.WifiPhase2Method

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Aka = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">AkaPrime = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Sim = 5,</span>
</pre>





### New Type Android.Net.Wifi.LocalOnlyHotspotCallbackErrorCode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum LocalOnlyHotspotCallbackErrorCode {
	<span class='added added-field ' data-is-non-breaking="">Generic = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompatibleMode = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NoChannel = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TetheringDisallowed = 4,</span>
}
</pre>





## Namespace Android.OS

### Type Changed: Android.OS.BatteryManager

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.OS.BatteryProperty enum directly instead of this field.")]
	public static const BatteryProperty BatteryPropertyStatus;
```





### Type Changed: Android.OS.BatteryProperty

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Status = 6,</span>
</pre>





### Type Changed: Android.OS.Build

### Type Changed: Android.OS.Build.VERSION_CODES

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.OS.BuildVersionCodes enum directly instead of this field.")]
	public static const BuildVersionCodes O;
```







### Type Changed: Android.OS.BuildVersionCodes

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">O = 26,</span>
</pre>





### Type Changed: Android.OS.Bundle

Added method:

```
public Bundle DeepCopy ();
```





### Type Changed: Android.OS.Pattern

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AdvancedGlob = 3,</span>
</pre>





### Type Changed: Android.OS.PersistableBundle

Added method:

```
public PersistableBundle DeepCopy ();
```





### Type Changed: Android.OS.RemoteCallbackList

Added methods:

```
public virtual Java.Lang.Object GetRegisteredCallbackCookie (int index);
	public virtual Java.Lang.Object GetRegisteredCallbackItem (int index);
```





### Type Changed: Android.OS.StrictMode

### Type Changed: Android.OS.StrictMode.ThreadPolicy

### Type Changed: Android.OS.StrictMode.Builder

Added methods:

```
public StrictMode.ThreadPolicy.Builder DetectUnbufferedIo ();
	public StrictMode.ThreadPolicy.Builder PermitUnbufferedIo ();
```







### Type Changed: Android.OS.StrictMode.VmPolicy

### Type Changed: Android.OS.StrictMode.Builder

Added methods:

```
public StrictMode.VmPolicy.Builder DetectContentUriWithoutPermission ();
	public StrictMode.VmPolicy.Builder DetectUntaggedSockets ();
```









### Type Changed: Android.OS.UserManager

Added fields:

```
public static const string DisallowAddManagedProfile = "no_add_managed_profile";
	public static const string DisallowAutofill = "no_autofill";
	public static const string DisallowBluetooth = "no_bluetooth";
	public static const string DisallowBluetoothSharing = "no_bluetooth_sharing";
	public static const string DisallowRemoveManagedProfile = "no_remove_managed_profile";
```





### Type Changed: Android.OS.Vibrator

Added property:

```
public virtual bool HasAmplitudeControl { get; }
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void Vibrate (long milliseconds);
	[Obsolete ("deprecated")]
	public virtual void Vibrate (long milliseconds, Android.Media.AudioAttributes attributes);
	[Obsolete ("deprecated")]
	public virtual void Vibrate (long[] pattern, int repeat);
	[Obsolete ("deprecated")]
	public virtual void Vibrate (long[] pattern, int repeat, Android.Media.AudioAttributes attributes);
```

Added methods:

```
public virtual void Vibrate (VibrationEffect vibe);
	public virtual void Vibrate (VibrationEffect vibe, Android.Media.AudioAttributes attributes);
```





### New Type Android.OS.ProxyFileDescriptorCallback

<pre class='added' data-is-non-breaking="">
public abstract class ProxyFileDescriptorCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ProxyFileDescriptorCallback ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ProxyFileDescriptorCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual long OnGetSize ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int OnRead (long offset, int size, byte[] data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnRelease ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int OnWrite (long offset, int size, byte[] data);</span>
}
</pre>



### New Type Android.OS.TestLooperManager

<pre class='added' data-is-non-breaking="">
public class TestLooperManager : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected TestLooperManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MessageQueue MessageQueue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Execute (Message message);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool HasMessages (Handler h, Java.Lang.Object object, Java.Lang.IRunnable r);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool HasMessages (Handler h, Java.Lang.Object object, int what);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Message Next ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Recycle (Message msg);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Release ();</span>
}
</pre>



### New Type Android.OS.VibrationEffect

<pre class='added' data-is-non-breaking="">
public abstract class VibrationEffect : Java.Lang.Object, IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VibrationEffect (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int DefaultAmplitude;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VibrationEffect CreateOneShot (long milliseconds, int amplitude);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VibrationEffect CreateWaveform (long[] timings, int repeat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VibrationEffect CreateWaveform (long[] timings, int[] amplitudes, int repeat);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Parcel dest, ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## Namespace Android.OS.Health

### Type Changed: Android.OS.Health.UidHealthStats

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const int MeasurementCpuPowerMams;
```





## Namespace Android.OS.Storage

### Type Changed: Android.OS.Storage.StorageManager

Added fields:

```
public static const string ExtraRequestedBytes = "android.os.storage.extra.REQUESTED_BYTES";
	public static const string ExtraUuid = "android.os.storage.extra.UUID";
```



Added property:

```
public static Java.Util.UUID UuidDefault { get; }
```



Added methods:

```
public virtual void AllocateBytes (Java.IO.FileDescriptor fd, long bytes);
	public virtual void AllocateBytes (Java.Util.UUID storageUuid, long bytes);
	public virtual long GetAllocatableBytes (Java.Util.UUID storageUuid);
	public virtual long GetCacheQuotaBytes (Java.Util.UUID storageUuid);
	public virtual long GetCacheSizeBytes (Java.Util.UUID storageUuid);
	public virtual Java.Util.UUID GetUuidForPath (Java.IO.File path);
	public virtual bool IsCacheBehaviorGroup (Java.IO.File path);
	public virtual bool IsCacheBehaviorTombstone (Java.IO.File path);
	public virtual Android.OS.ParcelFileDescriptor OpenProxyFileDescriptor (Android.OS.ParcelFileMode mode, Android.OS.ProxyFileDescriptorCallback callback, Android.OS.Handler handler);
	public virtual void SetCacheBehaviorGroup (Java.IO.File path, bool group);
	public virtual void SetCacheBehaviorTombstone (Java.IO.File path, bool tombstone);
```







## Namespace Android.Opengl

### Type Changed: Android.Opengl.EGL14

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static EGLSurface EglCreatePixmapSurface (EGLDisplay dpy, EGLConfig config, int pixmap, int[] attrib_list, int offset);
```



### Type Changed: Android.Opengl.EGLExt

Added field:

```
public static const int EglRecordableAndroid;
```





### Type Changed: Android.Opengl.GLSurfaceView

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void SurfaceRedrawNeeded (Android.Views.ISurfaceHolder holder);
```

Added method:

```
public virtual void SurfaceRedrawNeededAsync (Android.Views.ISurfaceHolder holder, Java.Lang.IRunnable finishDrawing);
```







## Namespace Android.Preferences

### Type Changed: Android.Preferences.Preference

Added properties:

```
public virtual bool IconSpaceReserved { get; set; }
	public virtual PreferenceGroup Parent { get; }
	public virtual IPreferenceDataStore PreferenceDataStore { get; set; }
	public virtual bool RecycleEnabled { get; set; }
	public virtual bool SingleLineTitle { get; set; }
```





### Type Changed: Android.Preferences.PreferenceManager

Added property:

```
public virtual IPreferenceDataStore PreferenceDataStore { get; set; }
```





### New Type Android.Preferences.IPreferenceDataStore

<pre class='added' data-is-non-breaking="">
public interface IPreferenceDataStore : Android.Runtime.IJavaObject, System.IDisposable {
}
</pre>





## Namespace Android.Print

### Type Changed: Android.Print.PrintJobInfo

Added methods:

```
public int GetAdvancedIntOption (string key);
	public string GetAdvancedStringOption (string key);
	public bool HasAdvancedOption (string key);
```







## Namespace Android.PrintServices

### Type Changed: Android.PrintServices.PrintService

Added fields:

```
public static const string ExtraCanSelectPrinter = "android.printservice.extra.CAN_SELECT_PRINTER";
	public static const string ExtraSelectPrinter = "android.printservice.extra.SELECT_PRINTER";
```







## Namespace Android.Provider

### Type Changed: Android.Provider.AlarmClock

Added field:

```
public static const string ActionShowTimers = "android.intent.action.SHOW_TIMERS";
```





### Type Changed: Android.Provider.CallLog

### Type Changed: Android.Provider.CallLog.Calls

Added fields:

```
public static const int FeaturesHdCall;
	public static const int FeaturesWifi;
```







### Type Changed: Android.Provider.ContactsContract

### Type Changed: Android.Provider.ContactsContract.Directory

Added field:

```
public static const string CallerPackageParamKey = "callerPackage";
```





### Type Changed: Android.Provider.ContactsContract.PhoneLookup

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string DisplayNameAlternative = "display_name_alt";
	public static const string DisplayNamePrimary = "display_name";
	public static const string DisplayNameSource = "display_name_source";
	public static const string PhoneticName = "phonetic_name";
	public static const string PhoneticNameStyle = "phonetic_name_style";
	public static const string SortKeyAlternative = "sort_key_alt";
	public static const string SortKeyPrimary = "sort_key";
```







### Type Changed: Android.Provider.ContactsContract.ProviderStatus

Added field:

```
public static const string DatabaseCreationTimestamp = "database_creation_timestamp";
```







### Type Changed: Android.Provider.DocumentContractFlags

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SupportsSettings = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">WebLinkable = 4096,</span>
</pre>





### Type Changed: Android.Provider.DocumentRootFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SupportsEject = 32,</span>
</pre>





### Type Changed: Android.Provider.DocumentsContract

Added fields:

```
public static const string ActionDocumentSettings = "android.provider.action.DOCUMENT_SETTINGS";
	public static const string ExtraInitialUri = "android.provider.extra.INITIAL_URI";
```



Added methods:

```
public static Android.Content.IntentSender CreateWebLinkIntent (Android.Content.ContentResolver resolver, Android.Net.Uri uri, Android.OS.Bundle options);
	public static void EjectRoot (Android.Content.ContentResolver resolver, Android.Net.Uri rootUri);
	public static DocumentsContract.Path FindDocumentPath (Android.Content.ContentResolver resolver, Android.Net.Uri treeUri);
```



### Type Changed: Android.Provider.DocumentsContract.Document

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Provider.DocumentContractFlags enum directly instead of this field.")]
	public static const DocumentContractFlags FlagSupportsSettings;

	[Obsolete ("This constant will be removed in the future version. Use Android.Provider.DocumentContractFlags enum directly instead of this field.")]
	public static const DocumentContractFlags FlagWebLinkable;
```





### Type Changed: Android.Provider.DocumentsContract.Root

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Provider.DocumentRootFlags enum directly instead of this field.")]
	public static const DocumentRootFlags FlagSupportsEject;
	public static const string MimeTypeItem = "vnd.android.document/root";
```





### New Type Android.Provider.Path

<pre class='added' data-is-non-breaking="">
public sealed class Path : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DocumentsContract (string rootId, System.Collections.Generic.IList&lt;string&gt; path);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string RootId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;string&gt; GetPath ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





### Type Changed: Android.Provider.DocumentsProvider

Added methods:

```
public virtual Android.Content.IntentSender CreateWebLinkIntent (string documentId, Android.OS.Bundle options);
	public virtual void EjectRoot (string rootId);
	public virtual DocumentsContract.Path FindDocumentPath (string parentDocumentId, string childDocumentId);
	public override Android.Database.ICursor Query (Android.Net.Uri uri, string[] projection, Android.OS.Bundle queryArgs, Android.OS.CancellationSignal cancellationSignal);
	public virtual Android.Database.ICursor QueryChildDocuments (string parentDocumentId, string[] projection, Android.OS.Bundle queryArgs);
```





### Type Changed: Android.Provider.MediaStore

Added method:

```
public static Android.Net.Uri GetDocumentUri (Android.Content.Context context, Android.Net.Uri mediaUri);
```





### Type Changed: Android.Provider.Settings

Added fields:

```
public static const string ActionAppNotificationSettings = "android.settings.APP_NOTIFICATION_SETTINGS";
	public static const string ActionChannelNotificationSettings = "android.settings.CHANNEL_NOTIFICATION_SETTINGS";
	public static const string ActionManageUnknownAppSources = "android.settings.MANAGE_UNKNOWN_APP_SOURCES";
	public static const string ActionNightDisplaySettings = "android.settings.NIGHT_DISPLAY_SETTINGS";
	public static const string ActionRequestSetAutofillService = "android.settings.REQUEST_SET_AUTOFILL_SERVICE";
	public static const string ActionZenModePrioritySettings = "android.settings.ZEN_MODE_PRIORITY_SETTINGS";
	public static const string ExtraAppPackage = "android.provider.extra.APP_PACKAGE";
	public static const string ExtraChannelId = "android.provider.extra.CHANNEL_ID";
```



### Type Changed: Android.Provider.Settings.Global

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string WifiNetworksAvailableNotificationOn = "wifi_networks_available_notification_on";
```



### Type Changed: Android.Provider.Settings.Secure

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string AccessibilitySpeakPassword = "speak_password";
	[Obsolete ("deprecated")]
	public static const string InstallNonMarketApps = "install_non_market_apps";
```





### Type Changed: Android.Provider.Telephony

### New Type Android.Provider.ServiceStateTable

<pre class='added' data-is-non-breaking="">
public sealed class ServiceStateTable : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string Authority = "service-state";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string IsManualNetworkSelection = "is_manual_network_selection";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VoiceOperatorNumeric = "voice_operator_numeric";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VoiceRegState = "voice_reg_state";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.Net.Uri ContentUri { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Android.Net.Uri GetUriForSubscriptionId (int subscriptionId);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Android.Net.Uri GetUriForSubscriptionIdAndField (int subscriptionId, string field);</span>
}
</pre>





### Type Changed: Android.Provider.VoicemailContract

### Type Changed: Android.Provider.VoicemailContract.Voicemails

Added fields:

```
public static const string Archived = "archived";
	public static const string BackedUp = "backed_up";
	public static const string IsOmtpVoicemail = "is_omtp_voicemail";
	public static const string Restored = "restored";
```







### New Type Android.Provider.FontFamilyResultStatus

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum FontFamilyResultStatus {
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Rejected = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">UnexpectedDataProvided = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WrongCertificates = 1,</span>
}
</pre>



### New Type Android.Provider.FontRequest

<pre class='added' data-is-non-breaking="">
public sealed class FontRequest : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FontRequest (string providerAuthority, string providerPackage, string query);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FontRequest (string providerAuthority, string providerPackage, string query, System.Collections.Generic.IList&lt;System.Collections.Generic.IList&lt;System.Byte[]&gt;&gt; certificates);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;System.Collections.Generic.IList&lt;System.Byte[]&gt;&gt; Certificates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ProviderAuthority { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ProviderPackage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Query { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Android.Provider.FontRequestFailureReason

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum FontRequestFailureReason {
	<span class='added added-field ' data-is-non-breaking="">FontLoadError = -3,</span>
	<span class='added added-field ' data-is-non-breaking="">FontNotFound = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FontUnavailable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MalformedQuery = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ProviderNotFound = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">WrongCertificates = -2,</span>
}
</pre>



### New Type Android.Provider.FontResultCode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum FontResultCode {
	<span class='added added-field ' data-is-non-breaking="">FontNotFound = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FontUnavailable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MalformedQuery = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
}
</pre>



### New Type Android.Provider.FontsContract

<pre class='added' data-is-non-breaking="">
public class FontsContract : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected FontsContract (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Android.Graphics.Typeface BuildTypeface (Android.Content.Context context, Android.OS.CancellationSignal cancellationSignal, FontsContract.FontInfo[] fonts);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FontsContract.FontFamilyResult FetchFonts (Android.Content.Context context, Android.OS.CancellationSignal cancellationSignal, FontRequest request);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestFonts (Android.Content.Context context, FontRequest request, Android.OS.Handler handler, Android.OS.CancellationSignal cancellationSignal, FontsContract.FontRequestCallback callback);</span>

	// inner types
	public sealed class Columns : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const string FileId = "file_id";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string Italic = "font_italic";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string ResultCode = "result_code";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string TtcIndex = "font_ttc_index";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string VariationSettings = "font_variation_settings";</span>
		<span class='added added-field ' data-is-non-breaking="">public static const string Weight = "font_weight";</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>

		// inner types
		public static class InterfaceConsts {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public static const string Count = "_count";</span>
			<span class='added added-field ' data-is-non-breaking="">public static const string Id = "_id";</span>
		}
	}
	public class FontFamilyResult : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected FontsContract (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual FontFamilyResultStatus StatusCode { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual FontsContract.FontInfo[] GetFonts ();</span>
	}
	public class FontInfo : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected FontsContract (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public virtual bool IsItalic { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual FontResultCode ResultCode { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual int TtcIndex { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual Android.Net.Uri Uri { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual int Weight { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual Android.Graphics.Fonts.FontVariationAxis[] GetAxes ();</span>
	}
	public class FontRequestCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public FontsContract ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">protected FontsContract (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnTypefaceRequestFailed (FontRequestFailureReason reason);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnTypefaceRetrieved (Android.Graphics.Typeface typeface);</span>
	}
}
</pre>





## Namespace Android.Security

### Type Changed: Android.Security.KeyChain

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string ActionStorageChanged = "android.security.STORAGE_CHANGED";
```

Added fields:

```
public static const string ActionKeyAccessChanged = "android.security.action.KEY_ACCESS_CHANGED";
	public static const string ActionKeychainChanged = "android.security.action.KEYCHAIN_CHANGED";
	public static const string ActionTrustStoreChanged = "android.security.action.TRUST_STORE_CHANGED";
	public static const string ExtraKeyAccessible = "android.security.extra.KEY_ACCESSIBLE";
	public static const string ExtraKeyAlias = "android.security.extra.KEY_ALIAS";
```







## Namespace Android.Service.Autofill

### Type Changed: Android.Service.Autofill.SaveFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SaveOnAllViewsInvisible = 1,</span>
</pre>





### New Type Android.Service.Autofill.AutofillService

<pre class='added' data-is-non-breaking="">
public abstract class AutofillService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AutofillService ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AutofillService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string ServiceInterface = "android.service.autofill.AutofillService";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ServiceMetaData = "android.autofill";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public FillEventHistory FillEventHistory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override Android.OS.IBinder OnBind (Android.Content.Intent intent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnConnected ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnDisconnected ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnFillRequest (FillRequest request, Android.OS.CancellationSignal cancellationSignal, FillCallback callback);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnSaveRequest (SaveRequest request, SaveCallback callback);</span>
}
</pre>



### New Type Android.Service.Autofill.Dataset

<pre class='added' data-is-non-breaking="">
public sealed class Dataset : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public Dataset ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">public Dataset (Android.Widget.RemoteViews presentation);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public Dataset Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public Dataset.Builder SetAuthentication (Android.Content.IntentSender authentication);</span>
		<span class='added added-method ' data-is-non-breaking="">public Dataset.Builder SetId (string id);</span>
		<span class='added added-method ' data-is-non-breaking="">public Dataset.Builder SetValue (Android.Views.Autofill.AutofillId id, Android.Views.Autofill.AutofillValue value);</span>
		<span class='added added-method ' data-is-non-breaking="">public Dataset.Builder SetValue (Android.Views.Autofill.AutofillId id, Android.Views.Autofill.AutofillValue value, Android.Widget.RemoteViews presentation);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Service.Autofill.EventType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum EventType {
	<span class='added added-field ' data-is-non-breaking="">AuthenticationSelected = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">DatasetAuthenticationSelected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">DatasetSelected = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SaveShown = 3,</span>
}
</pre>



### New Type Android.Service.Autofill.FillCallback

<pre class='added' data-is-non-breaking="">
public sealed class FillCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void OnFailure (Java.Lang.ICharSequence message);</span>
	<span class='added added-method ' data-is-non-breaking="">public void OnFailure (string message);</span>
	<span class='added added-method ' data-is-non-breaking="">public void OnSuccess (FillResponse response);</span>
}
</pre>



### New Type Android.Service.Autofill.FillContext

<pre class='added' data-is-non-breaking="">
public sealed class FillContext : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int RequestId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.App.Assist.AssistStructure Structure { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Service.Autofill.FillEventHistory

<pre class='added' data-is-non-breaking="">
public sealed class FillEventHistory : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Android.OS.Bundle ClientState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;FillEventHistory.Event&gt; Events { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Event : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public string DatasetId { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public EventType Type { get; }</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Service.Autofill.FillRequest

<pre class='added' data-is-non-breaking="">
public sealed class FillRequest : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int FlagManualRequest;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Android.OS.Bundle ClientState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;FillContext&gt; FillContexts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Flags { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Id { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Service.Autofill.FillResponse

<pre class='added' data-is-non-breaking="">
public sealed class FillResponse : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public FillResponse ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public FillResponse.Builder AddDataset (Dataset dataset);</span>
		<span class='added added-method ' data-is-non-breaking="">public FillResponse Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public FillResponse.Builder SetAuthentication (Android.Views.Autofill.AutofillId[] ids, Android.Content.IntentSender authentication, Android.Widget.RemoteViews presentation);</span>
		<span class='added added-method ' data-is-non-breaking="">public FillResponse.Builder SetClientState (Android.OS.Bundle clientState);</span>
		<span class='added added-method ' data-is-non-breaking="">public FillResponse.Builder SetIgnoredIds (Android.Views.Autofill.AutofillId[] ids);</span>
		<span class='added added-method ' data-is-non-breaking="">public FillResponse.Builder SetSaveInfo (SaveInfo saveInfo);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Service.Autofill.NegativeButtonStyle

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NegativeButtonStyle {
	<span class='added added-field ' data-is-non-breaking="">Cancel = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Reject = 1,</span>
}
</pre>



### New Type Android.Service.Autofill.SaveCallback

<pre class='added' data-is-non-breaking="">
public sealed class SaveCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void OnFailure (Java.Lang.ICharSequence message);</span>
	<span class='added added-method ' data-is-non-breaking="">public void OnFailure (string message);</span>
	<span class='added added-method ' data-is-non-breaking="">public void OnSuccess ();</span>
}
</pre>



### New Type Android.Service.Autofill.SaveDataType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SaveDataType {
	<span class='added added-field ' data-is-non-breaking="">Address = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">CreditCard = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">EmailAddress = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Generic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Password = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Username = 8,</span>
}
</pre>



### New Type Android.Service.Autofill.SaveInfo

<pre class='added' data-is-non-breaking="">
public sealed class SaveInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public SaveInfo (SaveDataType type, Android.Views.Autofill.AutofillId[] requiredIds);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public SaveInfo Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public SaveInfo.Builder SetDescription (Java.Lang.ICharSequence description);</span>
		<span class='added added-method ' data-is-non-breaking="">public SaveInfo.Builder SetDescription (string description);</span>
		<span class='added added-method ' data-is-non-breaking="">public SaveInfo.Builder SetFlags (SaveFlags flags);</span>
		<span class='added added-method ' data-is-non-breaking="">public SaveInfo.Builder SetNegativeAction (NegativeButtonStyle style, Android.Content.IntentSender listener);</span>
		<span class='added added-method ' data-is-non-breaking="">public SaveInfo.Builder SetOptionalIds (Android.Views.Autofill.AutofillId[] ids);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Service.Autofill.SaveRequest

<pre class='added' data-is-non-breaking="">
public sealed class SaveRequest : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Android.OS.Bundle ClientState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;FillContext&gt; FillContexts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## Namespace Android.Service.Notification

### Type Changed: Android.Service.Notification.ConditionProviderService

Added methods:

```
public static void RequestRebind (Android.Content.ComponentName componentName);
	public void RequestUnbind ();
```





### Type Changed: Android.Service.Notification.NotificationListenerService

Added methods:

```
public System.Collections.Generic.IList<Android.App.NotificationChannelGroup> GetNotificationChannelGroups (string pkg, Android.OS.UserHandle user);
	public System.Collections.Generic.IList<Android.App.NotificationChannel> GetNotificationChannels (string pkg, Android.OS.UserHandle user);
	public StatusBarNotification[] GetSnoozedNotifications ();
	public virtual void OnNotificationChannelGroupModified (string pkg, Android.OS.UserHandle user, Android.App.NotificationChannelGroup group, NotificationChannelOrGroupEventType modificationType);
	public virtual void OnNotificationChannelModified (string pkg, Android.OS.UserHandle user, Android.App.NotificationChannel channel, NotificationChannelOrGroupEventType modificationType);
	public virtual void OnNotificationRemoved (StatusBarNotification sbn, NotificationListenerService.RankingMap rankingMap, NotificationCancelReason reason);
	public void SnoozeNotification (string key, long durationMs);
	public void UpdateNotificationChannel (string pkg, Android.OS.UserHandle user, Android.App.NotificationChannel channel);
```



### Type Changed: Android.Service.Notification.NotificationListenerService.Ranking

Added property:

```
public virtual Android.App.NotificationChannel Channel { get; }
```



Added method:

```
public virtual bool CanShowBadge ();
```







### New Type Android.Service.Notification.NotificationCancelReason

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NotificationCancelReason {
	<span class='added added-field ' data-is-non-breaking="">AppCancel = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AppCancelAll = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Cancel = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">CancelAll = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ChannelBanned = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Click = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Error = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">GroupOptimization = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">GroupSummaryCanceled = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">ListenerCancel = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">ListenerCancelAll = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">PackageBanned = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">PackageChanged = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">PackageSuspended = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">ProfileTurnedOff = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Snoozed = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">Timeout = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Unautobundled = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">UserStopped = 6,</span>
}
</pre>



### New Type Android.Service.Notification.NotificationChannelOrGroupEventType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NotificationChannelOrGroupEventType {
	<span class='added added-field ' data-is-non-breaking="">Added = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Deleted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Updated = 2,</span>
}
</pre>





## Namespace Android.Service.Voice

### Type Changed: Android.Service.Voice.VoiceInteractionSession

Added methods:

```
public virtual void OnPrepareShow (Android.OS.Bundle args, ShowFlags showFlags);
	public virtual void SetUiEnabled (bool enabled);
	public virtual void StartAssistantActivity (Android.Content.Intent intent);
```







## Namespace Android.Speech.Tts

### Type Changed: Android.Speech.Tts.UtteranceProgressListener

Added method:

```
public virtual void OnRangeStart (string utteranceId, int start, int end, int frame);
```







## Namespace Android.Systems

### Type Changed: Android.Systems.Os

Added methods:

```
public static byte[] Getxattr (string path, string name);
	public static int If_nametoindex (string name);
	public static string[] Listxattr (string path);
	public static void Removexattr (string path, string name);
	public static void SetsockoptInt (Java.IO.FileDescriptor fd, int level, int option, int value);
	public static void Setxattr (string path, string name, byte[] value, int flags);
```





### Type Changed: Android.Systems.OsConstants

Added property:

```
public static int TcpUserTimeout { get; }
```







## Namespace Android.Telecom

### Type Changed: Android.Telecom.Call

Added field:

```
public static const string ExtraLastEmergencyCallbackTimeMillis = "android.telecom.extra.LAST_EMERGENCY_CALLBACK_TIME_MILLIS";
```



Added property:

```
public bool IsRttActive { get; }
```



Added methods:

```
public Call.RttCall GetRttCall ();
	public void RespondToRttRequest (int id, bool accept);
	public void SendRttRequest ();
	public void StopRtt ();
```



### Type Changed: Android.Telecom.Call.Callback

Added methods:

```
public virtual void OnRttInitiationFailure (Call call, RttSessionModifyResult reason);
	public virtual void OnRttModeChanged (Call call, RttMode mode);
	public virtual void OnRttRequest (Call call, int id);
	public virtual void OnRttStatusChanged (Call call, bool enabled, Call.RttCall rttCall);
```





### Type Changed: Android.Telecom.Call.Details

Added property:

```
public virtual long CreationTimeMillis { get; }
```





### New Type Android.Telecom.RttCall

<pre class='added' data-is-non-breaking="">
public sealed class RttCall : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public RttMode RttAudioMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public string Read ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetRttMode (RttMode mode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Write (string input);</span>
}
</pre>





### Type Changed: Android.Telecom.CallProperty

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SelfManaged = 256,</span>
</pre>





### Type Changed: Android.Telecom.Connection

Added fields:

```
public static const string ExtraAnsweringDropsFgCallAppName = "android.telecom.extra.ANSWERING_DROPS_FG_CALL_APP_NAME";

	[Obsolete ("This constant will be removed in the future version. Use Android.Telecom.ConnectionProperties enum directly instead of this field.")]
	public static const ConnectionProperties PropertySelfManaged;
```



Added methods:

```
public virtual void OnShowIncomingCallUi ();
	public void SetAudioRoute (CallAudioRoute route);
```



### New Type Android.Telecom.RttModifyStatus

<pre class='added' data-is-non-breaking="">
public sealed class RttModifyStatus : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





### Type Changed: Android.Telecom.ConnectionProperties

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SelfManaged = 128,</span>
</pre>





### Type Changed: Android.Telecom.ConnectionService

Added methods:

```
public virtual void OnCreateIncomingConnectionFailed (PhoneAccountHandle connectionManagerPhoneAccount, ConnectionRequest request);
	public virtual void OnCreateOutgoingConnectionFailed (PhoneAccountHandle connectionManagerPhoneAccount, ConnectionRequest request);
```





### Type Changed: Android.Telecom.PhoneAccountCapability

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Rtt = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">SelfManaged = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">SupportsVideoCalling = 1024,</span>
</pre>





### Type Changed: Android.Telecom.TelecomManager

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string ActionIncomingCall = "android.telecom.action.INCOMING_CALL";
```

Added fields:

```
public static const string ActionPhoneAccountRegistered = "android.telecom.action.PHONE_ACCOUNT_REGISTERED";
	public static const string ActionPhoneAccountUnregistered = "android.telecom.action.PHONE_ACCOUNT_UNREGISTERED";
	public static const string ExtraIncomingVideoState = "android.telecom.extra.INCOMING_VIDEO_STATE";
	public static const string ExtraStartCallWithRtt = "android.telecom.extra.START_CALL_WITH_RTT";
	public static const string MetadataIncludeSelfManagedCalls = "android.telecom.INCLUDE_SELF_MANAGED_CALLS";
```



Added properties:

```
public virtual bool IsInManagedCall { get; }
	public virtual System.Collections.Generic.IList<PhoneAccountHandle> SelfManagedPhoneAccounts { get; }
```



Added methods:

```
public virtual void AcceptRingingCall ();
	public virtual void AcceptRingingCall (int videoState);
	public virtual bool IsIncomingCallPermitted (PhoneAccountHandle phoneAccountHandle);
	public virtual bool IsOutgoingCallPermitted (PhoneAccountHandle phoneAccountHandle);
```





### Type Changed: Android.Telecom.VideoSessionEvent

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CameraPermissionError = 7,</span>
</pre>





### New Type Android.Telecom.RttMode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RttMode {
	<span class='added added-field ' data-is-non-breaking="">Full = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Hco = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Vco = 3,</span>
}
</pre>



### New Type Android.Telecom.RttSessionModifyResult

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RttSessionModifyResult {
	<span class='added added-field ' data-is-non-breaking="">Fail = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">RejectedByRemote = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TimedOut = 4,</span>
}
</pre>





## Namespace Android.Telephony

### Type Changed: Android.Telephony.CarrierConfigManager

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string KeyCarrierVvmPackageNameString = "carrier_vvm_package_name_string";
```

Added fields:

```
public static const int DataCycleThresholdDisabled;
	public static const string KeyCallForwardingBlocksWhileRoamingStringArray = "call_forwarding_blocks_while_roaming_string_array";
	public static const string KeyCarrierDataCallPermanentFailureStrings = "carrier_data_call_permanent_failure_strings";
	public static const string KeyCarrierVolteProvisionedBool = "carrier_volte_provisioned_bool";
	public static const string KeyCarrierVvmPackageNameStringArray = "carrier_vvm_package_name_string_array";
	public static const string KeyCdma3waycallFlashDelayInt = "cdma_3waycall_flash_delay_int";
	public static const string KeyConfigImsPackageOverrideString = "config_ims_package_override_string";
	public static const string KeyDataLimitThresholdBytesLong = "data_limit_threshold_bytes_long";
	public static const string KeyDataWarningThresholdBytesLong = "data_warning_threshold_bytes_long";
	public static const string KeyDefaultVmNumberString = "default_vm_number_string";
	public static const string KeyDialStringReplaceStringArray = "dial_string_replace_string_array";
	public static const string KeyEditableVoicemailNumberBool = "editable_voicemail_number_bool";
	public static const string KeyHideEnhanced4gLteBool = "hide_enhanced_4g_lte_bool";
	public static const string KeyImsConferenceSizeLimitInt = "ims_conference_size_limit_int";
	public static const string KeyIsImsConferenceSizeEnforcedBool = "is_ims_conference_size_enforced_bool";
	public static const string KeyMdnIsAdditionalVoicemailNumberBool = "mdn_is_additional_voicemail_number_bool";
	public static const string KeyMonthlyDataCycleDayInt = "monthly_data_cycle_day_int";
	public static const string KeyOnlySingleDcAllowedIntArray = "only_single_dc_allowed_int_array";
	public static const string KeyRcsConfigServerUrlString = "rcs_config_server_url_string";
	public static const string KeyRestartRadioOnPdpFailRegularDeactivationBool = "restart_radio_on_pdp_fail_regular_deactivation_bool";
	public static const string KeySimplifiedNetworkSettingsBool = "simplified_network_settings_bool";
	public static const string KeySmsRequiresDestinationNumberConversionBool = "sms_requires_destination_number_conversion_bool";
	public static const string KeySupport3gppCallForwardingWhileRoamingBool = "support_3gpp_call_forwarding_while_roaming_bool";
	public static const string KeyVvmClientPrefixString = "vvm_client_prefix_string";
	public static const string KeyVvmDisabledCapabilitiesStringArray = "vvm_disabled_capabilities_string_array";
	public static const string KeyVvmLegacyModeEnabledBool = "vvm_legacy_mode_enabled_bool";
	public static const string KeyVvmSslEnabledBool = "vvm_ssl_enabled_bool";
```





### Type Changed: Android.Telephony.CellSignalStrengthGsm

Added property:

```
public int TimingAdvance { get; }
```





### Type Changed: Android.Telephony.CellSignalStrengthLte

Added properties:

```
public int Cqi { get; }
	public int Rsrp { get; }
	public int Rsrq { get; }
	public int Rssnr { get; }
```





### Type Changed: Android.Telephony.SimState

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CardIoError = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">CardRestricted = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">NotReady = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">PermDisabled = 7,</span>
</pre>





### Type Changed: Android.Telephony.SmsManager

Added method:

```
public string CreateAppSpecificSmsToken (Android.App.PendingIntent intent);
```





### Type Changed: Android.Telephony.SubscriptionManager

Added fields:

```
public static const string ActionDefaultSmsSubscriptionChanged = "android.telephony.action.DEFAULT_SMS_SUBSCRIPTION_CHANGED";
	public static const string ActionDefaultSubscriptionChanged = "android.telephony.action.DEFAULT_SUBSCRIPTION_CHANGED";
	public static const string ExtraSubscriptionIndex = "android.telephony.extra.SUBSCRIPTION_INDEX";
```



Modified methods:

```
public virtual SubscriptionInfo GetActiveSubscriptionInfoForSimSlotIndex (int slotIdx slotIndex)
```



### Type Changed: Android.Telephony.TelephonyManager

Added fields:

```
public static const string ActionShowVoicemailNotification = "android.telephony.action.SHOW_VOICEMAIL_NOTIFICATION";
	public static const string ExtraCallVoicemailIntent = "android.telephony.extra.CALL_VOICEMAIL_INTENT";
	public static const string ExtraHidePublicSettings = "android.telephony.extra.HIDE_PUBLIC_SETTINGS";
	public static const string ExtraLaunchVoicemailSettingsIntent = "android.telephony.extra.LAUNCH_VOICEMAIL_SETTINGS_INTENT";
	public static const string ExtraNotificationCount = "android.telephony.extra.NOTIFICATION_COUNT";
	public static const string ExtraPhoneAccountHandle = "android.telephony.extra.PHONE_ACCOUNT_HANDLE";
	public static const string ExtraVoicemailNumber = "android.telephony.extra.VOICEMAIL_NUMBER";
	public static const string MetadataHideVoicemailSettingsMenu = "android.telephony.HIDE_VOICEMAIL_SETTINGS_MENU";
```



Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual CellLocation CellLocation { get; }
	[Obsolete ("deprecated")]
	public virtual string DeviceId { get; }
```

Added properties:

```
public virtual Android.OS.PersistableBundle CarrierConfig { get; }
	public virtual bool DataEnabled { get; set; }
	public virtual string Imei { get; }
	public virtual bool IsConcurrentVoiceAndDataSupported { get; }
	public virtual string Meid { get; }
	public virtual string NetworkSpecifier { get; }
	public virtual ServiceState ServiceState { get; }
	public virtual string VisualVoicemailPackageName { get; }
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual string GetDeviceId (int slotIndex);
	[Obsolete ("deprecated")]
	public virtual IccOpenLogicalChannelResponse IccOpenLogicalChannel (string AID);
```

Modified methods:

```
public virtual string GetDeviceId (int slotId slotIndex)
```

Added methods:

```
public virtual TelephonyManager CreateForPhoneAccountHandle (Android.Telecom.PhoneAccountHandle phoneAccountHandle);
	public virtual string[] GetForbiddenPlmns ();
	public virtual string GetImei (int slotIndex);
	public virtual string GetMeid (int slotIndex);
	public virtual SimState GetSimState (int slotIndex);
	public virtual IccOpenLogicalChannelResponse IccOpenLogicalChannel (string AID, int p2);
	public virtual void SendDialerSpecialCode (string inputCode);
	public virtual void SendUssdRequest (string ussdRequest, TelephonyManager.UssdResponseCallback callback, Android.OS.Handler handler);
	public virtual void SendVisualVoicemailSms (string number, int port, string text, Android.App.PendingIntent sentIntent);
	public virtual void SetVisualVoicemailSmsFilterSettings (VisualVoicemailSmsFilterSettings settings);
	public virtual void SetVoicemailRingtoneUri (Android.Telecom.PhoneAccountHandle phoneAccountHandle, Android.Net.Uri uri);
	public virtual void SetVoicemailVibrationEnabled (Android.Telecom.PhoneAccountHandle phoneAccountHandle, bool enabled);
```





### New Type Android.Telephony.UssdResultCode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UssdResultCode {
	<span class='added added-field ' data-is-non-breaking="">ErrorServiceUnavail = -2,</span>
	<span class='added added-field ' data-is-non-breaking="">ReturnFailure = -1,</span>
}
</pre>



### New Type Android.Telephony.VisualVoicemailService

<pre class='added' data-is-non-breaking="">
public abstract class VisualVoicemailService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VisualVoicemailService ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VisualVoicemailService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string ServiceInterface = "android.telephony.VisualVoicemailService";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override Android.OS.IBinder OnBind (Android.Content.Intent intent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnCellServiceConnected (VisualVoicemailService.VisualVoicemailTask task, Android.Telecom.PhoneAccountHandle phoneAccountHandle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnSimRemoved (VisualVoicemailService.VisualVoicemailTask task, Android.Telecom.PhoneAccountHandle phoneAccountHandle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnSmsReceived (VisualVoicemailService.VisualVoicemailTask task, VisualVoicemailSms sms);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnStopped (VisualVoicemailService.VisualVoicemailTask task);</span>

	// inner types
	public class VisualVoicemailTask : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected VisualVoicemailService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public void Finish ();</span>
	}
}
</pre>



### New Type Android.Telephony.VisualVoicemailSms

<pre class='added' data-is-non-breaking="">
public sealed class VisualVoicemailSms : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.OS.Bundle Fields { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string MessageBody { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Telecom.PhoneAccountHandle PhoneAccountHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Prefix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Telephony.VisualVoicemailSmsFilterSettings

<pre class='added' data-is-non-breaking="">
public sealed class VisualVoicemailSmsFilterSettings : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int DestinationPortAny;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int DestinationPortDataSms;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string ClientPrefix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int DestinationPort { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.IList OriginatingNumbers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public VisualVoicemailSmsFilterSettings ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">protected VisualVoicemailSmsFilterSettings (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual VisualVoicemailSmsFilterSettings Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual VisualVoicemailSmsFilterSettings.Builder SetClientPrefix (string clientPrefix);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual VisualVoicemailSmsFilterSettings.Builder SetDestinationPort (int destinationPort);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual VisualVoicemailSmsFilterSettings.Builder SetOriginatingNumbers (System.Collections.Generic.IList&lt;string&gt; originatingNumbers);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## Namespace Android.Test.Mock

### Type Changed: Android.Test.Mock.MockContext

Added methods:

```
public override Android.Content.Context CreateContextForSplit (string splitName);
	public override Android.Content.Intent RegisterReceiver (Android.Content.BroadcastReceiver receiver, Android.Content.IntentFilter filter, Android.Content.ActivityFlags flags);
	public override Android.Content.Intent RegisterReceiver (Android.Content.BroadcastReceiver receiver, Android.Content.IntentFilter filter, string broadcastPermission, Android.OS.Handler scheduler, Android.Content.ActivityFlags flags);
	public override void RevokeUriPermission (string targetPackage, Android.Net.Uri uri, Android.Content.ActivityFlags modeFlags);
	public override Android.Content.ComponentName StartForegroundService (Android.Content.Intent service);
```





### Type Changed: Android.Test.Mock.MockPackageManager

Added properties:

```
public override int InstantAppCookieMaxBytes { get; }
	public override bool IsInstantApp { get; }
```



Added methods:

```
public override bool CanRequestPackageInstalls ();
	public override void ClearInstantAppCookie ();
	public override Android.Content.PM.ChangedPackages GetChangedPackages (int sequenceNumber);
	public override byte[] GetInstantAppCookie ();
	public override Android.Content.PM.PackageInfo GetPackageInfo (Android.Content.PM.VersionedPackage versionedPackage, Android.Content.PM.PackageInfoFlags flags);
	public override System.Collections.Generic.IList<Android.Content.PM.SharedLibraryInfo> GetSharedLibraries (Android.Content.PM.PackageInstallReason flags);
	public override bool InvokeIsInstantApp (string packageName);
	public override void SetApplicationCategoryHint (string packageName, int categoryHint);
	public override void UpdateInstantAppCookie (byte[] cookie);
```







## Namespace Android.Text

### Type Changed: Android.Text.BidiFormatter

Added methods:

```
public bool IsRtl (Java.Lang.ICharSequence str);
	public Java.Lang.ICharSequence UnicodeWrapFormatted (Java.Lang.ICharSequence str);
	public Java.Lang.ICharSequence UnicodeWrapFormatted (Java.Lang.ICharSequence str, ITextDirectionHeuristic heuristic);
	public Java.Lang.ICharSequence UnicodeWrapFormatted (Java.Lang.ICharSequence str, bool isolate);
	public Java.Lang.ICharSequence UnicodeWrapFormatted (Java.Lang.ICharSequence str, ITextDirectionHeuristic heuristic, bool isolate);
```





### Type Changed: Android.Text.StaticLayout

### Type Changed: Android.Text.StaticLayout.Builder

Added method:

```
public StaticLayout.Builder SetJustificationMode (JustificationMode justificationMode);
```







### Type Changed: Android.Text.TextUtils

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static string CommaEllipsize (string text, TextPaint p, float avail, string oneMore, string more);
	[Obsolete ("deprecated")]
	public static Java.Lang.ICharSequence CommaEllipsizeFormatted (Java.Lang.ICharSequence text, TextPaint p, float avail, string oneMore, string more);
```



### New Type Android.Text.JustificationMode

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum JustificationMode {
	<span class='added added-field ' data-is-non-breaking="">InterWord = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>





## Namespace Android.Text.Method

### Type Changed: Android.Text.Method.DateKeyListener

Added constructor:

```
public DateKeyListener (Java.Util.Locale locale);
```



Obsoleted properties:

```
[Obsolete ("deprecated")]
	public static DateKeyListener Instance { get; }
```

Added method:

```
public static DateKeyListener GetInstance (Java.Util.Locale locale);
```





### Type Changed: Android.Text.Method.DateTimeKeyListener

Added constructor:

```
public DateTimeKeyListener (Java.Util.Locale locale);
```



Obsoleted properties:

```
[Obsolete ("deprecated")]
	public static DateTimeKeyListener Instance { get; }
```

Added method:

```
public static DateTimeKeyListener GetInstance (Java.Util.Locale locale);
```





### Type Changed: Android.Text.Method.DigitsKeyListener

Added constructors:

```
public DigitsKeyListener (Java.Util.Locale locale);
	public DigitsKeyListener (Java.Util.Locale locale, bool sign, bool decimal);
```



Obsoleted properties:

```
[Obsolete ("deprecated")]
	public static DigitsKeyListener Instance { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static DigitsKeyListener GetInstance (bool sign, bool decimal);
```

Added methods:

```
public static DigitsKeyListener GetInstance (Java.Util.Locale locale);
	public static DigitsKeyListener GetInstance (Java.Util.Locale locale, bool sign, bool decimal);
```





### Type Changed: Android.Text.Method.TimeKeyListener

Added constructor:

```
public TimeKeyListener (Java.Util.Locale locale);
```



Obsoleted properties:

```
[Obsolete ("deprecated")]
	public static TimeKeyListener Instance { get; }
```

Added method:

```
public static TimeKeyListener GetInstance (Java.Util.Locale locale);
```







## Namespace Android.Transitions

### New Type Android.Transitions.TransitionListenerAdapter

<pre class='added' data-is-non-breaking="">
public abstract class TransitionListenerAdapter : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TransitionListenerAdapter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TransitionListenerAdapter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnTransitionCancel (Transition transition);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnTransitionEnd (Transition transition);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnTransitionPause (Transition transition);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnTransitionResume (Transition transition);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnTransitionStart (Transition transition);</span>
}
</pre>





## Namespace Android.Util

### New Type Android.Util.Half

<pre class='added' data-is-non-breaking="">
public sealed class Half : Java.Lang.Number, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Half (double value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Half (short value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Half (float value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Half (string value);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const short Epsilon;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short LowestValue;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int MaxExponent;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short MaxValue;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int MinExponent;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short MinNormal;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short MinValue;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short NaN;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short NegativeInfinity;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short NegativeZero;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short PositiveInfinity;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const short PositiveZero;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const int Size;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsNaN { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static short Abs (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short Ceil (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int Compare (short x, short y);</span>
	<span class='added added-method ' data-is-non-breaking="">public int CompareTo (Half h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short CopySign (short magnitude, short sign);</span>
	<span class='added added-method ' data-is-non-breaking="">public override double DoubleValue ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Equals (short x, short y);</span>
	<span class='added added-method ' data-is-non-breaking="">public override float FloatValue ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static short Floor (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetExponent (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetSign (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetSignificand (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Greater (short x, short y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GreaterEquals (short x, short y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int HalfToIntBits (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int HalfToRawIntBits (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short HalfToShortBits (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public short HalfValue ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static int HashCode (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short IntBitsToHalf (int bits);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int IntValue ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool InvokeIsNaN (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsInfinite (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsNormalized (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Less (short x, short y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool LessEquals (short x, short y);</span>
	<span class='added added-method ' data-is-non-breaking="">public override long LongValue ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static short Max (short x, short y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short Min (short x, short y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short ParseHalf (string s);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short Round (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float ToFloat (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short ToHalf (float f);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string ToHexString (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string ToString (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static short Trunc (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Half ValueOf (short h);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Half ValueOf (float f);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Half ValueOf (string s);</span>
}
</pre>





## Namespace Android.Views

### Type Changed: Android.Views.AutofillFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">IncludeNotImportantViews = 1,</span>
</pre>





### Type Changed: Android.Views.Axis

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Scroll = 26,</span>
</pre>





### Type Changed: Android.Views.Display

Added properties:

```
public virtual bool IsHdr { get; }
	public virtual bool IsWideColorGamut { get; }
```





### Type Changed: Android.Views.DisplayState

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Vr = 5,</span>
</pre>





### Type Changed: Android.Views.FocusFinder

Added method:

```
public virtual View FindNextKeyboardNavigationCluster (View root, View currentCluster, FocusSearchDirection direction);
```





### Type Changed: Android.Views.FrameMetrics

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.FrameMetricsId enum directly instead of this field.")]
	public static const FrameMetricsId IntendedVsyncTimestamp;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.FrameMetricsId enum directly instead of this field.")]
	public static const FrameMetricsId VsyncTimestamp;
```





### Type Changed: Android.Views.FrameMetricsId

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">IntendedVsyncTimestamp = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">VsyncTimestamp = 11,</span>
</pre>





### Type Changed: Android.Views.IViewParent

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void InvalidateChild (View child, Android.Graphics.Rect r);
	[Obsolete ("deprecated")]
	public virtual IViewParent InvalidateChildInParent (int[] location, Android.Graphics.Rect r);
```

Added method:

```
public virtual View KeyboardNavigationClusterSearch (View currentCluster, FocusSearchDirection direction);
```





### Type Changed: Android.Views.InputDevice

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.InputSourceType enum directly instead of this field.")]
	public static const InputSourceType SourceMouseRelative;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.InputSourceType enum directly instead of this field.")]
	public static const InputSourceType SourceRotaryEncoder;
```





### Type Changed: Android.Views.InputSourceType

Added values:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MouseRelative = 131076,</span>
	<span class='added added-field ' data-is-non-breaking="">RotaryEncoder = 4194304,</span>
</pre>





### Type Changed: Android.Views.Menu

Added field:

```
public static const int SupportedModifiersMask;
```





### Type Changed: Android.Views.PixelCopy

Added methods:

```
public static void Request (Window source, Android.Graphics.Bitmap dest, PixelCopy.IOnPixelCopyFinishedListener listener, Android.OS.Handler listenerThread);
	public static void Request (Surface source, Android.Graphics.Rect srcRect, Android.Graphics.Bitmap dest, PixelCopy.IOnPixelCopyFinishedListener listener, Android.OS.Handler listenerThread);
	public static void Request (SurfaceView source, Android.Graphics.Rect srcRect, Android.Graphics.Bitmap dest, PixelCopy.IOnPixelCopyFinishedListener listener, Android.OS.Handler listenerThread);
	public static void Request (Window source, Android.Graphics.Rect srcRect, Android.Graphics.Bitmap dest, PixelCopy.IOnPixelCopyFinishedListener listener, Android.OS.Handler listenerThread);
```





### Type Changed: Android.Views.SystemUiFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">LightNavigationBar = 16,</span>
</pre>





### Type Changed: Android.Views.View

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.AutofillFlags enum directly instead of this field.")]
	public static const AutofillFlags AutofillFlagIncludeNotImportantViews;
	public static const string AutofillHintCreditCardExpirationDate = "creditCardExpirationDate";
	public static const string AutofillHintCreditCardExpirationDay = "creditCardExpirationDay";
	public static const string AutofillHintCreditCardExpirationMonth = "creditCardExpirationMonth";
	public static const string AutofillHintCreditCardExpirationYear = "creditCardExpirationYear";
	public static const string AutofillHintCreditCardNumber = "creditCardNumber";
	public static const string AutofillHintCreditCardSecurityCode = "creditCardSecurityCode";
	public static const string AutofillHintEmailAddress = "emailAddress";
	public static const string AutofillHintName = "name";
	public static const string AutofillHintPassword = "password";
	public static const string AutofillHintPhone = "phone";
	public static const string AutofillHintPostalAddress = "postalAddress";
	public static const string AutofillHintPostalCode = "postalCode";
	public static const string AutofillHintUsername = "username";

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.AutofillType enum directly instead of this field.")]
	public static const AutofillType AutofillTypeDate;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.AutofillType enum directly instead of this field.")]
	public static const AutofillType AutofillTypeList;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.AutofillType enum directly instead of this field.")]
	public static const AutofillType AutofillTypeNone;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.AutofillType enum directly instead of this field.")]
	public static const AutofillType AutofillTypeText;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.AutofillType enum directly instead of this field.")]
	public static const AutofillType AutofillTypeToggle;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ViewFocusability enum directly instead of this field.")]
	public static const ViewFocusability FocusableAuto;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ImportantForAutofill enum directly instead of this field.")]
	public static const ImportantForAutofill ImportantForAutofillAuto;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ImportantForAutofill enum directly instead of this field.")]
	public static const ImportantForAutofill ImportantForAutofillNo;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ImportantForAutofill enum directly instead of this field.")]
	public static const ImportantForAutofill ImportantForAutofillNoExcludeDescendants;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ImportantForAutofill enum directly instead of this field.")]
	public static const ImportantForAutofill ImportantForAutofillYes;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ImportantForAutofill enum directly instead of this field.")]
	public static const ImportantForAutofill ImportantForAutofillYesExcludeDescendants;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ViewFocusability enum directly instead of this field.")]
	public static const ViewFocusability NotFocusable;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.SystemUiFlags enum directly instead of this field.")]
	public static const SystemUiFlags SystemUiFlagLightNavigationBar;
```



Added properties:

```
public Autofill.AutofillId AutofillId { get; }
	public virtual AutofillType AutofillType { get; }
	public virtual Autofill.AutofillValue AutofillValue { get; }
	public bool DefaultFocusHighlightEnabled { get; set; }
	public bool FocusedByDefault { get; set; }
	public virtual bool HasExplicitFocusable { get; }
	public virtual bool HasPointerCapture { get; }
	public virtual ImportantForAutofill ImportantForAutofill { get; set; }
	public bool IsImportantForAutofill { get; }
	public bool KeyboardNavigationCluster { get; set; }
	public virtual int NextClusterForwardId { get; set; }
	public string TooltipText { get; set; }
	public virtual Java.Lang.ICharSequence TooltipTextFormatted { get; set; }
```



Added event:

```
public event System.EventHandler<View.CapturedPointerEventArgs> CapturedPointer;
```



Added methods:

```
public virtual void AddExtraDataToAccessibilityNodeInfo (Accessibility.AccessibilityNodeInfo info, string extraDataKey, Android.OS.Bundle arguments);
	public virtual void AddKeyboardNavigationClusters (System.Collections.Generic.ICollection<View> views, FocusSearchDirection direction);
	public virtual void Autofill (Android.Util.SparseArray values);
	public virtual void Autofill (Autofill.AutofillValue value);
	public virtual bool DispatchCapturedPointerEvent (MotionEvent e);
	public virtual void DispatchPointerCaptureChanged (bool hasCapture);
	public virtual void DispatchProvideAutofillStructure (ViewStructure structure, AutofillFlags flags);
	public virtual string[] GetAutofillHints ();
	public virtual ViewFocusability GetFocusable ();
	public virtual View KeyboardNavigationClusterSearch (View currentCluster, FocusSearchDirection direction);
	public virtual bool OnCapturedPointerEvent (MotionEvent e);
	public virtual void OnPointerCaptureChange (bool hasCapture);
	public virtual void OnProvideAutofillStructure (ViewStructure structure, AutofillFlags flags);
	public virtual void OnProvideAutofillVirtualStructure (ViewStructure structure, AutofillFlags flags);
	public virtual void ReleasePointerCapture ();
	public virtual void RequestPointerCapture ();
	public virtual bool RestoreDefaultFocus ();
	public virtual void SetAutofillHints (string[] autofillHints);
	public virtual void SetFocusable (ViewFocusability focusable);
	public virtual void SetOnCapturedPointerListener (View.IOnCapturedPointerListener l);
```



### Type Changed: Android.Views.View.AccessibilityDelegate

Added method:

```
public virtual void AddExtraDataToAccessibilityNodeInfo (View host, Accessibility.AccessibilityNodeInfo info, string extraDataKey, Android.OS.Bundle arguments);
```





### New Type Android.Views.CapturedPointerEventArgs

<pre class='added' data-is-non-breaking="">
public class CapturedPointerEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public View (bool handled, View view, MotionEvent e);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public MotionEvent Event { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool Handled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public View View { get; }</span>
}
</pre>



### New Type Android.Views.IOnCapturedPointerListener

<pre class='added' data-is-non-breaking="">
public interface IOnCapturedPointerListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool OnCapturedPointer (View view, MotionEvent e);</span>
}
</pre>





### Type Changed: Android.Views.ViewConfiguration

Added properties:

```
public virtual float ScaledHorizontalScrollFactor { get; }
	public virtual float ScaledVerticalScrollFactor { get; }
```





### Type Changed: Android.Views.ViewGroup

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void InvalidateChild (View child, Android.Graphics.Rect dirty);
	[Obsolete ("deprecated")]
	public virtual IViewParent InvalidateChildInParent (int[] location, Android.Graphics.Rect dirty);
```

Added method:

```
public virtual void OnDescendantInvalidated (View child, View target);
```





### Type Changed: Android.Views.ViewStructure

Added property:

```
public virtual Autofill.AutofillId AutofillId { get; set; }
```



Added methods:

```
public virtual ViewStructure.HtmlInfo.Builder NewHtmlInfoBuilder (string tagName);
	public virtual void SetAutofillHints (string[] hint);
	public virtual void SetAutofillId (Autofill.AutofillId parentId, int virtualId);
	public virtual void SetAutofillOptions (Java.Lang.ICharSequence[] options);
	public void SetAutofillOptions (string[] options);
	public virtual void SetAutofillType (AutofillType type);
	public virtual void SetAutofillValue (Autofill.AutofillValue value);
	public virtual void SetDataIsSensitive (bool sensitive);
	public virtual void SetHtmlInfo (ViewStructure.HtmlInfo htmlInfo);
	public virtual void SetInputType (int inputType);
	public virtual void SetLocaleList (Android.OS.LocaleList localeList);
	public virtual void SetOpaque (bool opaque);
	public virtual void SetWebDomain (string domain);
```





### Type Changed: Android.Views.Window

Added property:

```
public virtual Android.Content.PM.ActivityColorMode ColorMode { get; set; }
```





### Type Changed: Android.Views.WindowManagerLayoutParams

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.WindowRotationAnimation enum directly instead of this field.")]
	public static const WindowRotationAnimation RotationAnimationSeamless;
```



Added property:

```
public virtual Android.Content.PM.ActivityColorMode ColorMode { get; set; }
```





### Type Changed: Android.Views.WindowManagerTypes

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ApplicationOverlay = 2038,</span>
</pre>





### Type Changed: Android.Views.WindowRotationAnimation

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Seamless = 3,</span>
</pre>





### New Type Android.Views.AutofillType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AutofillType {
	<span class='added added-field ' data-is-non-breaking="">Date = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Toggle = 2,</span>
}
</pre>



### New Type Android.Views.ImportantForAutofill

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ImportantForAutofill {
	<span class='added added-field ' data-is-non-breaking="">Auto = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NoExcludeDescendants = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">YesExcludeDescendants = 4,</span>
}
</pre>



### New Type Android.Views.ViewFocusability

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ViewFocusability {
	<span class='added added-field ' data-is-non-breaking="">Focusable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FocusableAuto = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">NotFocusable = 0,</span>
}
</pre>





## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityManager

Added methods:

```
public void AddAccessibilityStateChangeListener (AccessibilityManager.IAccessibilityStateChangeListener listener, Android.OS.Handler handler);
	public void AddTouchExplorationStateChangeListener (AccessibilityManager.ITouchExplorationStateChangeListener listener, Android.OS.Handler handler);
```





### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo

Added fields:

```
public static const string ActionArgumentMoveWindowX = "ACTION_ARGUMENT_MOVE_WINDOW_X";
	public static const string ActionArgumentMoveWindowY = "ACTION_ARGUMENT_MOVE_WINDOW_Y";
	public static const string ExtraDataTextCharacterLocationArgLength = "android.view.accessibility.extra.DATA_TEXT_CHARACTER_LOCATION_ARG_LENGTH";
	public static const string ExtraDataTextCharacterLocationArgStartIndex = "android.view.accessibility.extra.DATA_TEXT_CHARACTER_LOCATION_ARG_START_INDEX";
	public static const string ExtraDataTextCharacterLocationKey = "android.view.accessibility.extra.DATA_TEXT_CHARACTER_LOCATION_KEY";
```



Added properties:

```
public virtual System.Collections.Generic.IList<string> AvailableExtraData { get; set; }
	public string HintText { get; set; }
	public virtual Java.Lang.ICharSequence HintTextFormatted { get; set; }
	public virtual bool ShowingHintText { get; set; }
```



Added method:

```
public virtual bool RefreshWithExtraData (string extraDataKey, Android.OS.Bundle args);
```



### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo.AccessibilityAction

Added property:

```
public static AccessibilityNodeInfo.AccessibilityAction ActionMoveWindow { get; }
```







### Type Changed: Android.Views.Accessibility.AccessibilityNodeProvider

Added method:

```
public virtual void AddExtraDataToAccessibilityNodeInfo (int virtualViewId, AccessibilityNodeInfo info, string extraDataKey, Android.OS.Bundle arguments);
```





### Type Changed: Android.Views.Accessibility.AccessibilityWindowInfo

Added property:

```
public bool IsInPictureInPictureMode { get; }
```







## Namespace Android.Views.InputMethods

### Type Changed: Android.Views.InputMethods.ImeFlags

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NoPersonalizedLearning = 16777216,</span>
</pre>







## Namespace Android.Webkit

### Type Changed: Android.Webkit.ClientError

Added value:

<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UnsafeResource = -16,</span>
</pre>





### Type Changed: Android.Webkit.WebSettings

Added property:

```
public virtual bool SafeBrowsingEnabled { get; set; }
```





### Type Changed: Android.Webkit.WebView

Added properties:

```
public static Android.Content.PM.PackageInfo CurrentWebViewPackage { get; }
	public virtual bool RendererPriorityWaivedWhenNotVisible { get; }
	public virtual RendererPriority RendererRequestedPriority { get; }
	public virtual WebChromeClient WebChromeClient { get; }
	public virtual WebViewClient WebViewClient { get; }
```



Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual string[] GetHttpAuthUsernamePassword (string host, string realm);
	[Obsolete ("deprecated")]
	public virtual void SetHttpAuthUsernamePassword (string host, string realm, string username, string password);
```

Added method:

```
public virtual void SetRendererPriorityPolicy (RendererPriority rendererRequestedPriority, bool waivedWhenNotVisible);
```





### Type Changed: Android.Webkit.WebViewClient

Added method:

```
public virtual bool OnRenderProcessGone (WebView view, RenderProcessGoneDetail detail);
```





### Type Changed: Android.Webkit.WebViewDatabase

Added methods:

```
public virtual string[] GetHttpAuthUsernamePassword (string host, string realm);
	public virtual void SetHttpAuthUsernamePassword (string host, string realm, string username, string password);
```





### New Type Android.Webkit.RenderProcessGoneDetail

<pre class='added' data-is-non-breaking="">
public abstract class RenderProcessGoneDetail : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RenderProcessGoneDetail ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RenderProcessGoneDetail (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DidCrash ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RendererPriorityAtExit ();</span>
}
</pre>



### New Type Android.Webkit.RendererPriority

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RendererPriority {
	<span class='added added-field ' data-is-non-breaking="">Bound = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Important = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Waived = 0,</span>
}
</pre>





## Namespace Android.Widget

### Type Changed: Android.Widget.ArrayAdapter

Added methods:

```
public string[] GetAutofillOptions ();
	public virtual Java.Lang.ICharSequence[] GetAutofillOptionsFormatted ();
```





### Type Changed: Android.Widget.Chronometer

Added property:

```
public virtual bool IsTheFinalCountDown { get; }
```





### Type Changed: Android.Widget.DatePicker

Added event:

```
public event System.EventHandler<DatePicker.DateChangedEventArgs> DateChanged;
```



Added method:

```
public virtual void SetOnDateChangedListener (DatePicker.IOnDateChangedListener onDateChangedListener);
```





### Type Changed: Android.Widget.ProgressBar

Added properties:

```
public virtual bool IsAnimating { get; }
	public virtual int Min { get; set; }
```





### Type Changed: Android.Widget.TextView

Added properties:

```
public virtual int AutoSizeMaxTextSize { get; }
	public virtual int AutoSizeMinTextSize { get; }
	public virtual int AutoSizeStepGranularity { get; }
	public virtual AutoSizeTextType AutoSizeTextType { get; }
	public virtual string FontVariationSettings { get; }
	public virtual Android.Text.JustificationMode JustificationMode { get; set; }
	public virtual Android.Views.TextClassifiers.ITextClassifier TextClassifier { get; set; }
```



Modified methods:

```
public virtual void SetMaxEms (int maxems maxEms)
	public virtual void SetMaxHeight (int maxHeight maxPixels)
	public virtual void SetMaxLines (int maxlines maxLines)
	public virtual void SetMaxWidth (int maxpixels maxPixels)
	public virtual void SetMinEms (int minems minEms)
	public virtual void SetMinHeight (int minHeight minPixels)
	public virtual void SetMinLines (int minlines minLines)
	public virtual void SetMinWidth (int minpixels minPixels)
```

Added methods:

```
public virtual int[] GetAutoSizeTextAvailableSizes ();
	public virtual void SetAutoSizeTextTypeUniformWithConfiguration (int autoSizeMinTextSize, int autoSizeMaxTextSize, int autoSizeStepGranularity, int unit);
	public virtual void SetAutoSizeTextTypeUniformWithPresetSizes (int[] presetSizes, int unit);
	public virtual void SetAutoSizeTextTypeWithDefaults (AutoSizeTextType autoSizeTextType);
	public virtual bool SetFontVariationSettings (string fontVariationSettings);
```





### Type Changed: Android.Widget.TimePicker

Added method:

```
public virtual bool ValidateInput ();
```





### Type Changed: Android.Widget.VideoView

Added methods:

```
public virtual void SetAudioAttributes (Android.Media.AudioAttributes attributes);
	public virtual void SetAudioFocusRequest (Android.Media.AudioFocus focusGain);
```





### New Type Android.Widget.AutoSizeTextType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AutoSizeTextType {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Uniform = 1,</span>
}
</pre>





## Namespace Dalvik.Bytecode

### Type Changed: Dalvik.Bytecode.Opcodes

Added fields:

```
public static const int OpInvokeCustom;
	public static const int OpInvokeCustomRange;
	public static const int OpInvokePolymorphic;
	public static const int OpInvokePolymorphicRange;
```







## Namespace Dalvik.SystemInterop

### Type Changed: Dalvik.SystemInterop.DexFile

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static DexFile LoadDex (string sourcePathName, string outputPathName, int flags);
```



### New Type Dalvik.SystemInterop.InMemoryDexClassLoader

<pre class='added' data-is-non-breaking="">
public sealed class InMemoryDexClassLoader : Dalvik.SystemInterop.BaseDexClassLoader, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public InMemoryDexClassLoader (Java.Nio.ByteBuffer dexBuffer, Java.Lang.ClassLoader parent);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





## Namespace Java.IO

### Type Changed: Java.IO.File

Added method:

```
public virtual Java.Nio.FileNio.IPath ToPath ();
```







## Namespace Java.Lang

### Type Changed: Java.Lang.AbstractStringBuilder

Added interface:

```
IAppendable
```



Added methods:

```
public virtual IAppendable Append (ICharSequence s);
	public virtual IAppendable Append (char c);
	public IAppendable Append (string s);
	public virtual IAppendable Append (ICharSequence s, int start, int end);
	public IAppendable Append (string s, int start, int end);
	public virtual string ToString ();
```





### Type Changed: Java.Lang.Byte

Added methods:

```
public static int ToUnsignedInt (sbyte x);
	public static long ToUnsignedLong (sbyte x);
```





### Type Changed: Java.Lang.Character

### Type Changed: Java.Lang.Character.UnicodeBlock

Added properties:

```
public static Character.UnicodeBlock ArabicExtendedA { get; }
	public static Character.UnicodeBlock ArabicMathematicalAlphabeticSymbols { get; }
	public static Character.UnicodeBlock Chakma { get; }
	public static Character.UnicodeBlock MeeteiMayekExtensions { get; }
	public static Character.UnicodeBlock MeroiticCursive { get; }
	public static Character.UnicodeBlock MeroiticHieroglyphs { get; }
	public static Character.UnicodeBlock Miao { get; }
	public static Character.UnicodeBlock Sharada { get; }
	public static Character.UnicodeBlock SoraSompeng { get; }
	public static Character.UnicodeBlock SundaneseSupplement { get; }
	public static Character.UnicodeBlock Takri { get; }
```





### Type Changed: Java.Lang.Character.UnicodeScript

Added properties:

```
public static Character.UnicodeScript Chakma { get; }
	public static Character.UnicodeScript MeroiticCursive { get; }
	public static Character.UnicodeScript MeroiticHieroglyphs { get; }
	public static Character.UnicodeScript Miao { get; }
	public static Character.UnicodeScript Sharada { get; }
	public static Character.UnicodeScript SoraSompeng { get; }
	public static Character.UnicodeScript Takri { get; }
```







### Type Changed: Java.Lang.Class

Added interface:

```
Reflect.IAnnotatedElement
```



Added property:

```
public string TypeName { get; }
```



Modified methods:

```
public bool IsAnnotationPresent (Class annotationType annotationClass)
	public bool IsAssignableFrom (Class c cls)
	public bool IsInstance (Object object obj)
```

Added method:

```
public string ToGenericString ();
```





### Type Changed: Java.Lang.Integer

Added methods:

```
public static int CompareUnsigned (int x, int y);
	public static int DivideUnsigned (int dividend, int divisor);
	public static int ParseUnsignedInt (string s);
	public static int ParseUnsignedInt (string s, int radix);
	public static int RemainderUnsigned (int dividend, int divisor);
	public static long ToUnsignedLong (int x);
	public static string ToUnsignedString (int i);
	public static string ToUnsignedString (int i, int radix);
```





### Type Changed: Java.Lang.Long

Added methods:

```
public static int CompareUnsigned (long x, long y);
	public static long DivideUnsigned (long dividend, long divisor);
	public static long ParseUnsignedLong (string s);
	public static long ParseUnsignedLong (string s, int radix);
	public static long RemainderUnsigned (long dividend, long divisor);
	public static string ToUnsignedString (long i);
	public static string ToUnsignedString (long i, int radix);
```





### Type Changed: Java.Lang.Package

Modified methods:

```
public virtual bool IsAnnotationPresent (Class annotationType annotationClass)
```



### Type Changed: Java.Lang.Process

Added property:

```
public virtual bool IsAlive { get; }
```



Added methods:

```
public virtual Process DestroyForcibly ();
	public virtual bool WaitFor (long timeout, Java.Util.Concurrent.TimeUnit unit);
	public System.Threading.Tasks.Task<bool> WaitForAsync (long timeout, Java.Util.Concurrent.TimeUnit unit);
```





### Type Changed: Java.Lang.ProcessBuilder

Added methods:

```
public ProcessBuilder InheritIO ();
	public ProcessBuilder.Redirect RedirectError ();
	public ProcessBuilder RedirectError (Java.IO.File file);
	public ProcessBuilder RedirectError (ProcessBuilder.Redirect destination);
	public ProcessBuilder.Redirect RedirectInput ();
	public ProcessBuilder RedirectInput (Java.IO.File file);
	public ProcessBuilder RedirectInput (ProcessBuilder.Redirect source);
	public ProcessBuilder.Redirect RedirectOutput ();
	public ProcessBuilder RedirectOutput (Java.IO.File file);
	public ProcessBuilder RedirectOutput (ProcessBuilder.Redirect destination);
```





### Type Changed: Java.Lang.Runtime

Modified methods:

```
public virtual void TraceInstructions (bool enable on)
	public virtual void TraceMethodCalls (bool enable on)
```



### Type Changed: Java.Lang.Short

Added methods:

```
public static int ToUnsignedInt (short x);
	public static long ToUnsignedLong (short x);
```





### Type Changed: Java.Lang.String

Added methods:

```
public static string Join (ICharSequence delimiter, ICharSequence[] elements);
	public static string Join (ICharSequence delimiter, IIterable elements);
	public static string Join (string delimiter, IIterable elements);
	public static string Join (string delimiter, string[] elements);
```





### Type Changed: Java.Lang.StringBuffer

Modified methods:

```
public virtual override final IAppendable Append (ICharSequence s)
	public virtual override final IAppendable Append (char c)
	public virtual override final IAppendable Append (ICharSequence s, int start, int end)
```



### Type Changed: Java.Lang.StringBuilder

Modified methods:

```
public virtual override final IAppendable Append (ICharSequence s)
	public virtual override final IAppendable Append (char c)
	public virtual override final IAppendable Append (ICharSequence s, int start, int end)
```



### Type Changed: Java.Lang.ThreadLocal

Added method:

```
public static ThreadLocal WithInitial (Java.Util.Functions.ISupplier supplier);
```





### New Type Java.Lang.BootstrapMethodError

<pre class='added' data-is-non-breaking="">
public class BootstrapMethodError : Java.Lang.LinkageError, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public BootstrapMethodError ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public BootstrapMethodError (Throwable cause);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public BootstrapMethodError (string s);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected BootstrapMethodError (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public BootstrapMethodError (string s, Throwable cause);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





## Namespace Java.Lang.Annotation

### Type Changed: Java.Lang.Annotation.ElementType

Added properties:

```
public static ElementType TypeParameter { get; }
	public static ElementType TypeUse { get; }
```





### New Type Java.Lang.Annotation.INative

<pre class='added' data-is-non-breaking="">
public interface INative : Android.Runtime.IJavaObject, IAnnotation, System.IDisposable {
}
</pre>



### New Type Java.Lang.Annotation.NativeAttribute

<pre class='added' data-is-non-breaking="">
public class NativeAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NativeAttribute ();</span>
}
</pre>





## Namespace Java.Lang.Reflect

### Type Changed: Java.Lang.Reflect.AccessibleObject

Modified methods:

```
public virtual bool IsAnnotationPresent (Java.Lang.Class annotationType annotationClass)
```

Added methods:

```
public virtual Java.Lang.Object[] GetAnnotationsByType (Java.Lang.Class annotationClass);
	public virtual Java.Lang.Object GetDeclaredAnnotation (Java.Lang.Class annotationClass);
	public virtual Java.Lang.Object[] GetDeclaredAnnotationsByType (Java.Lang.Class annotationClass);
```





### Type Changed: Java.Lang.Reflect.Constructor

Modified base type: <span class='removed removed-inline removed-breaking-inline'>Java.Lang.Reflect.AccessibleObject</span> <span class='added '>Java.Lang.Reflect.Executable</span>Modified properties:

```
public virtual override final Java.Lang.Class DeclaringClass { get; }
	public virtual override final bool IsSynthetic { get; }
	public override bool IsVarArgs { get; }
	public virtual override final int Modifiers { get; }
	public virtual override final string Name { get; }
```

Modified methods:

```
public override Java.Lang.Class[] GetExceptionTypes ()
	public override IType[] GetGenericExceptionTypes ()
	public override IType[] GetGenericParameterTypes ()
	public override Java.Lang.Annotation.IAnnotation[][] GetParameterAnnotations ()
	public override Java.Lang.Class[] GetParameterTypes ()
	public virtual override final ITypeVariable[] GetTypeParameters ()
	public Java.Lang.Object NewInstance (Java.Lang.Object[] args initargs)
	public override string ToGenericString ()
```

### Removed Type  <span class='breaking' data-is-breaking="">Java.Lang.Reflect.Constructor.InterfaceConsts</span>



### Type Changed: Java.Lang.Reflect.Field

Modified methods:

```
public Java.Lang.Object Get (Java.Lang.Object object obj)
	public bool GetBoolean (Java.Lang.Object object obj)
	public sbyte GetByte (Java.Lang.Object object obj)
	public char GetChar (Java.Lang.Object object obj)
	public double GetDouble (Java.Lang.Object object obj)
	public float GetFloat (Java.Lang.Object object obj)
	public int GetInt (Java.Lang.Object object obj)
	public long GetLong (Java.Lang.Object object obj)
	public short GetShort (Java.Lang.Object object obj)
	public void Set (Java.Lang.Object object obj, Java.Lang.Object value)
	public void SetBoolean (Java.Lang.Object object obj, bool value z)
	public void SetByte (Java.Lang.Object object obj, sbyte value b)
	public void SetChar (Java.Lang.Object object obj, char value c)
	public void SetDouble (Java.Lang.Object object obj, double value d)
	public void SetFloat (Java.Lang.Object object obj, float value f)
	public void SetInt (Java.Lang.Object object obj, int value i)
	public void SetLong (Java.Lang.Object object obj, long value l)
	public void SetShort (Java.Lang.Object object obj, short value s)
```



### Type Changed: Java.Lang.Reflect.GenericSignatureFormatError

Added constructor:

```
public GenericSignatureFormatError (string message);
```





### Type Changed: Java.Lang.Reflect.IGenericDeclaration

Added interface:

```
IAnnotatedElement
```





### Type Changed: Java.Lang.Reflect.Method

Modified base type: <span class='removed removed-inline removed-breaking-inline'>Java.Lang.Reflect.AccessibleObject</span> <span class='added '>Java.Lang.Reflect.Executable</span>Modified properties:

```
public virtual override final Java.Lang.Class DeclaringClass { get; }
	public virtual override final bool IsSynthetic { get; }
	public override bool IsVarArgs { get; }
	public virtual override final int Modifiers { get; }
	public virtual override final string Name { get; }
```

Modified methods:

```
public override Java.Lang.Class[] GetExceptionTypes ()
	public override IType[] GetGenericExceptionTypes ()
	public override IType[] GetGenericParameterTypes ()
	public override Java.Lang.Annotation.IAnnotation[][] GetParameterAnnotations ()
	public override Java.Lang.Class[] GetParameterTypes ()
	public virtual override final ITypeVariable[] GetTypeParameters ()
	public Java.Lang.Object Invoke (Java.Lang.Object receiver obj, Java.Lang.Object[] args)
	public override string ToGenericString ()
```

### Removed Type  <span class='breaking' data-is-breaking="">Java.Lang.Reflect.Method.InterfaceConsts</span>



### Type Changed: Java.Lang.Reflect.Modifier

Added method:

```
public static int ParameterModifiers ();
```





### New Type Java.Lang.Reflect.Executable

<pre class='added' data-is-non-breaking="">
public abstract class Executable : Java.Lang.Reflect.AccessibleObject, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, IAnnotatedElement, IGenericDeclaration, IMember, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected Executable (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Java.Lang.Class DeclaringClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsSynthetic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsVarArgs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int Modifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int ParameterCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Class[] GetExceptionTypes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IType[] GetGenericExceptionTypes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IType[] GetGenericParameterTypes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Annotation.IAnnotation[][] GetParameterAnnotations ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Class[] GetParameterTypes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Parameter[] GetParameters ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ITypeVariable[] GetTypeParameters ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool IsAnnotationPresent (Java.Lang.Class annotationType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToGenericString ();</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int Declared;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const int Public;</span>
	}
}
</pre>



### New Type Java.Lang.Reflect.Parameter

<pre class='added' data-is-non-breaking="">
public sealed class Parameter : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, IAnnotatedElement, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Executable DeclaringExecutable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsImplicit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsNamePresent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsSynthetic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsVarArgs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Modifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IType ParameterizedType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Lang.Class Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object GetAnnotation (Java.Lang.Class annotationClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Annotation.IAnnotation[] GetAnnotations ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Object[] GetAnnotationsByType (Java.Lang.Class annotationClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Object GetDeclaredAnnotation (Java.Lang.Class annotationClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Annotation.IAnnotation[] GetDeclaredAnnotations ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Object[] GetDeclaredAnnotationsByType (Java.Lang.Class annotationClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAnnotationPresent (Java.Lang.Class annotationClass);</span>
}
</pre>





## Namespace Java.Nio.Channels

### Type Changed: Java.Nio.Channels.Channels

Added methods:

```
public static System.IO.Stream NewInputStream (IAsynchronousByteChannel ch);
	public static System.IO.Stream NewOutputStream (IAsynchronousByteChannel ch);
```





### Type Changed: Java.Nio.Channels.DatagramChannel

Added property:

```
public virtual Java.Net.SocketAddress LocalAddress { get; }
```





### Type Changed: Java.Nio.Channels.FileChannel

Added methods:

```
public static FileChannel Open (Java.Nio.FileNio.IPath path, Java.Nio.FileNio.IOpenOption[] options);
	public static FileChannel Open (Java.Nio.FileNio.IPath path, System.Collections.Generic.ICollection<Java.Nio.FileNio.IOpenOption> options, Java.Nio.FileNio.Attributes.IFileAttribute[] attrs);
```





### Type Changed: Java.Nio.Channels.FileLock

Added constructor:

```
protected FileLock (AsynchronousFileChannel channel, long position, long size, bool shared);
```





### Type Changed: Java.Nio.Channels.ServerSocketChannel

Added property:

```
public virtual Java.Net.SocketAddress LocalAddress { get; }
```





### Type Changed: Java.Nio.Channels.SocketChannel

Added property:

```
public virtual Java.Net.SocketAddress LocalAddress { get; }
```





### New Type Java.Nio.Channels.AcceptPendingException

<pre class='added' data-is-non-breaking="">
public class AcceptPendingException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AcceptPendingException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AcceptPendingException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.Channels.AsynchronousChannelGroup

<pre class='added' data-is-non-breaking="">
public abstract class AsynchronousChannelGroup : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousChannelGroup (Spi.AsynchronousChannelProvider provider);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousChannelGroup (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsShutdown { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsTerminated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AwaitTermination (long timeout, Java.Util.Concurrent.TimeUnit unit);</span>
	<span class='added added-method ' data-is-non-breaking="">public Spi.AsynchronousChannelProvider Provider ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Shutdown ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ShutdownNow ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousChannelGroup WithCachedThreadPool (Java.Util.Concurrent.IExecutorService executor, int initialSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousChannelGroup WithFixedThreadPool (int nThreads, Java.Util.Concurrent.IThreadFactory threadFactory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousChannelGroup WithThreadPool (Java.Util.Concurrent.IExecutorService executor);</span>
}
</pre>



### New Type Java.Nio.Channels.AsynchronousFileChannel

<pre class='added' data-is-non-breaking="">
public abstract class AsynchronousFileChannel : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ICloseable, Java.Interop.IJavaPeerable, IAsynchronousChannel, IChannel, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousFileChannel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousFileChannel (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOpen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Force (bool metaData);</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Util.Concurrent.IFuture Lock ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Lock (Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Lock (long position, long size, bool shared);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Lock (long position, long size, bool shared, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousFileChannel Open (Java.Nio.FileNio.IPath file, Java.Nio.FileNio.IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousFileChannel Open (Java.Nio.FileNio.IPath file, System.Collections.Generic.ICollection&lt;Java.Nio.FileNio.IOpenOption&gt; options, Java.Util.Concurrent.IExecutorService executor, Java.Nio.FileNio.Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Read (Java.Nio.ByteBuffer dst, long position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Read (Java.Nio.ByteBuffer dst, long position, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual long Size ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AsynchronousFileChannel Truncate (long size);</span>
	<span class='added added-method ' data-is-non-breaking="">public FileLock TryLock ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileLock TryLock (long position, long size, bool shared);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Write (Java.Nio.ByteBuffer src, long position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Write (Java.Nio.ByteBuffer src, long position, Java.Lang.Object attachment, ICompletionHandler handler);</span>
}
</pre>



### New Type Java.Nio.Channels.AsynchronousServerSocketChannel

<pre class='added' data-is-non-breaking="">
public abstract class AsynchronousServerSocketChannel : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ICloseable, Java.Interop.IJavaPeerable, IAsynchronousChannel, IChannel, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousServerSocketChannel (Spi.AsynchronousChannelProvider provider);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousServerSocketChannel (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOpen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Java.Net.SocketAddress LocalAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Accept ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Accept (Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public AsynchronousServerSocketChannel Bind (Java.Net.SocketAddress local);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AsynchronousServerSocketChannel Bind (Java.Net.SocketAddress local, int backlog);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousServerSocketChannel Open ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousServerSocketChannel Open (AsynchronousChannelGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public Spi.AsynchronousChannelProvider Provider ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AsynchronousServerSocketChannel SetOption (Java.Net.ISocketOption name, Java.Lang.Object value);</span>
}
</pre>



### New Type Java.Nio.Channels.AsynchronousSocketChannel

<pre class='added' data-is-non-breaking="">
public abstract class AsynchronousSocketChannel : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ICloseable, Java.Interop.IJavaPeerable, IAsynchronousByteChannel, IAsynchronousChannel, IChannel, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousSocketChannel (Spi.AsynchronousChannelProvider provider);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousSocketChannel (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOpen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Java.Net.SocketAddress LocalAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Java.Net.SocketAddress RemoteAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual AsynchronousSocketChannel Bind (Java.Net.SocketAddress local);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Connect (Java.Net.SocketAddress remote);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Connect (Java.Net.SocketAddress remote, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousSocketChannel Open ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousSocketChannel Open (AsynchronousChannelGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public Spi.AsynchronousChannelProvider Provider ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Read (Java.Nio.ByteBuffer dst);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Read (Java.Nio.ByteBuffer dst, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Read (Java.Nio.ByteBuffer dst, long timeout, Java.Util.Concurrent.TimeUnit unit, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Read (Java.Nio.ByteBuffer[] dsts, int offset, int length, long timeout, Java.Util.Concurrent.TimeUnit unit, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AsynchronousSocketChannel SetOption (Java.Net.ISocketOption name, Java.Lang.Object value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AsynchronousSocketChannel ShutdownInput ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AsynchronousSocketChannel ShutdownOutput ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Write (Java.Nio.ByteBuffer src);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Write (Java.Nio.ByteBuffer src, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Write (Java.Nio.ByteBuffer src, long timeout, Java.Util.Concurrent.TimeUnit unit, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Write (Java.Nio.ByteBuffer[] srcs, int offset, int length, long timeout, Java.Util.Concurrent.TimeUnit unit, Java.Lang.Object attachment, ICompletionHandler handler);</span>
}
</pre>



### New Type Java.Nio.Channels.IAsynchronousByteChannel

<pre class='added' data-is-non-breaking="">
public interface IAsynchronousByteChannel : Android.Runtime.IJavaObject, Java.IO.ICloseable, IAsynchronousChannel, IChannel, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Read (Java.Nio.ByteBuffer dst);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Read (Java.Nio.ByteBuffer dst, Java.Lang.Object attachment, ICompletionHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.Concurrent.IFuture Write (Java.Nio.ByteBuffer src);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Write (Java.Nio.ByteBuffer src, Java.Lang.Object attachment, ICompletionHandler handler);</span>
}
</pre>



### New Type Java.Nio.Channels.IAsynchronousChannel

<pre class='added' data-is-non-breaking="">
public interface IAsynchronousChannel : Android.Runtime.IJavaObject, Java.IO.ICloseable, IChannel, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
}
</pre>



### New Type Java.Nio.Channels.ICompletionHandler

<pre class='added' data-is-non-breaking="">
public interface ICompletionHandler : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Completed (Java.Lang.Object result, Java.Lang.Object attachment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Failed (Java.Lang.Throwable exc, Java.Lang.Object attachment);</span>
}
</pre>



### New Type Java.Nio.Channels.IllegalChannelGroupException

<pre class='added' data-is-non-breaking="">
public class IllegalChannelGroupException : Java.Lang.IllegalArgumentException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public IllegalChannelGroupException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected IllegalChannelGroupException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.Channels.InterruptedByTimeoutException

<pre class='added' data-is-non-breaking="">
public class InterruptedByTimeoutException : Java.IO.IOException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public InterruptedByTimeoutException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected InterruptedByTimeoutException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.Channels.MembershipKey

<pre class='added' data-is-non-breaking="">
public abstract class MembershipKey : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MembershipKey ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MembershipKey (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsValid { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MembershipKey Block (Java.Net.InetAddress source);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Drop ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Net.InetAddress Group ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Net.NetworkInterface NetworkInterface ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Net.InetAddress SourceAddress ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MembershipKey Unblock (Java.Net.InetAddress source);</span>
}
</pre>



### New Type Java.Nio.Channels.ReadPendingException

<pre class='added' data-is-non-breaking="">
public class ReadPendingException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ReadPendingException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ReadPendingException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.Channels.ShutdownChannelGroupException

<pre class='added' data-is-non-breaking="">
public class ShutdownChannelGroupException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ShutdownChannelGroupException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ShutdownChannelGroupException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.Channels.WritePendingException

<pre class='added' data-is-non-breaking="">
public class WritePendingException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WritePendingException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WritePendingException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





## Namespace Java.Nio.Channels.Spi

### New Type Java.Nio.Channels.Spi.AsynchronousChannelProvider

<pre class='added' data-is-non-breaking="">
public abstract class AsynchronousChannelProvider : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousChannelProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AsynchronousChannelProvider (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.Channels.AsynchronousChannelGroup OpenAsynchronousChannelGroup (Java.Util.Concurrent.IExecutorService executor, int initialSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.Channels.AsynchronousChannelGroup OpenAsynchronousChannelGroup (int nThreads, Java.Util.Concurrent.IThreadFactory threadFactory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.Channels.AsynchronousServerSocketChannel OpenAsynchronousServerSocketChannel (Java.Nio.Channels.AsynchronousChannelGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.Channels.AsynchronousSocketChannel OpenAsynchronousSocketChannel (Java.Nio.Channels.AsynchronousChannelGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AsynchronousChannelProvider Provider ();</span>
}
</pre>





## Namespace Java.Security

### Type Changed: Java.Security.KeyStore

### Type Changed: Java.Security.KeyStore.PasswordProtection

Added constructor:

```
public KeyStore (char[] password, string protectionAlgorithm, Spec.IAlgorithmParameterSpec protectionParameters);
```



Added properties:

```
public virtual string ProtectionAlgorithm { get; }
	public virtual Spec.IAlgorithmParameterSpec ProtectionParameters { get; }
```





### Type Changed: Java.Security.KeyStore.PrivateKeyEntry

Added constructor:

```
public KeyStore (IPrivateKey privateKey, Cert.Certificate[] chain, System.Collections.Generic.ICollection<KeyStore.IEntryAttribute> attributes);
```



Added property:

```
public System.Collections.Generic.ICollection<KeyStore.IEntryAttribute> Attributes { get; }
```





### Type Changed: Java.Security.KeyStore.SecretKeyEntry

Added constructor:

```
public KeyStore (Javax.Crypto.ISecretKey secretKey, System.Collections.Generic.ICollection<KeyStore.IEntryAttribute> attributes);
```



Added property:

```
public System.Collections.Generic.ICollection<KeyStore.IEntryAttribute> Attributes { get; }
```





### Type Changed: Java.Security.KeyStore.TrustedCertificateEntry

Added constructor:

```
public KeyStore (Cert.Certificate trustedCert, System.Collections.Generic.ICollection<KeyStore.IEntryAttribute> attributes);
```



Added property:

```
public System.Collections.Generic.ICollection<KeyStore.IEntryAttribute> Attributes { get; }
```





### New Type Java.Security.IEntryAttribute

<pre class='added' data-is-non-breaking="">
public interface IEntryAttribute : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Value { get; }</span>
}
</pre>





### Type Changed: Java.Security.Provider

Added methods:

```
public virtual Java.Lang.Object Compute (Java.Lang.Object key, Java.Util.Functions.IBiFunction remappingFunction);
	public virtual Java.Lang.Object ComputeIfAbsent (Java.Lang.Object key, Java.Util.Functions.IFunction mappingFunction);
	public virtual Java.Lang.Object ComputeIfPresent (Java.Lang.Object key, Java.Util.Functions.IBiFunction remappingFunction);
	public virtual Java.Lang.Object GetOrDefault (Java.Lang.Object key, Java.Lang.Object defaultValue);
	public virtual Java.Lang.Object Merge (Java.Lang.Object key, Java.Lang.Object value, Java.Util.Functions.IBiFunction remappingFunction);
	public virtual Java.Lang.Object PutIfAbsent (Java.Lang.Object key, Java.Lang.Object value);
	public virtual Java.Lang.Object Replace (Java.Lang.Object key, Java.Lang.Object value);
	public virtual bool Replace (Java.Lang.Object key, Java.Lang.Object oldValue, Java.Lang.Object newValue);
	public virtual void ReplaceAll (Java.Util.Functions.IBiFunction function);
```





### Type Changed: Java.Security.SecureRandom

Added property:

```
public static SecureRandom InstanceStrong { get; }
```





### New Type Java.Security.DomainLoadStoreParameter

<pre class='added' data-is-non-breaking="">
public sealed class DomainLoadStoreParameter : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DomainLoadStoreParameter (Java.Net.URI configuration, System.Collections.Generic.IDictionary&lt;System.String,Java.Security.KeyStore.IProtectionParameter&gt; protectionParams);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Java.Net.URI Configuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual KeyStore.IProtectionParameter ProtectionParameter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IDictionary&lt;System.String,Java.Security.KeyStore.IProtectionParameter&gt; ProtectionParams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Security.PKCS12Attribute

<pre class='added' data-is-non-breaking="">
public sealed class PKCS12Attribute : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PKCS12Attribute (byte[] encoded);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PKCS12Attribute (string name, string value);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Value { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public byte[] GetEncoded ();</span>
}
</pre>





## Namespace Java.Security.Cert

### Type Changed: Java.Security.Cert.Certificate

Added method:

```
public virtual void Verify (Java.Security.IPublicKey key, Java.Security.Provider sigProvider);
```





### Type Changed: Java.Security.Cert.X509CRL

Added method:

```
public virtual void Verify (Java.Security.IPublicKey key, Java.Security.Provider sigProvider);
```





### Type Changed: Java.Security.Cert.X509Certificate

Modified methods:

```
public virtual override void Verify (Java.Security.IPublicKey key, Java.Security.Provider sigProvider)
```





## Namespace Java.Security.Spec

### Type Changed: Java.Security.Spec.MGF1ParameterSpec

Added property:

```
public static MGF1ParameterSpec Sha224 { get; }
```







## Namespace Java.Util

### Type Changed: Java.Util.Calendar

Added fields:

```
public static const int LongFormat;
	public static const int LongStandalone;
	public static const int NarrowFormat;
	public static const int NarrowStandalone;
	public static const int ShortFormat;
	public static const int ShortStandalone;
```



Added properties:

```
public static System.Collections.Generic.ICollection<string> AvailableCalendarTypes { get; }
	public virtual string CalendarType { get; }
```





### Type Changed: Java.Util.Collections

Added methods:

```
public static INavigableMap CheckedNavigableMap (INavigableMap m, Java.Lang.Class keyType, Java.Lang.Class valueType);
	public static INavigableSet CheckedNavigableSet (INavigableSet s, Java.Lang.Class type);
	public static IQueue CheckedQueue (IQueue queue, Java.Lang.Class type);
	public static INavigableMap EmptyNavigableMap ();
	public static INavigableSet EmptyNavigableSet ();
	public static System.Collections.IDictionary EmptySortedMap ();
	public static ISortedSet EmptySortedSet ();
	public static INavigableMap SynchronizedNavigableMap (INavigableMap m);
	public static INavigableSet SynchronizedNavigableSet (INavigableSet s);
	public static INavigableMap UnmodifiableNavigableMap (INavigableMap m);
	public static INavigableSet UnmodifiableNavigableSet (INavigableSet s);
```





### Type Changed: Java.Util.HashMap

Added methods:

```
public virtual Java.Lang.Object Compute (Java.Lang.Object key, Functions.IBiFunction remappingFunction);
	public virtual Java.Lang.Object ComputeIfAbsent (Java.Lang.Object key, Functions.IFunction mappingFunction);
	public virtual Java.Lang.Object ComputeIfPresent (Java.Lang.Object key, Functions.IBiFunction remappingFunction);
	public virtual Java.Lang.Object GetOrDefault (Java.Lang.Object key, Java.Lang.Object defaultValue);
	public virtual Java.Lang.Object Merge (Java.Lang.Object key, Java.Lang.Object value, Functions.IBiFunction remappingFunction);
	public virtual Java.Lang.Object PutIfAbsent (Java.Lang.Object key, Java.Lang.Object value);
	public virtual bool Remove (Java.Lang.Object key, Java.Lang.Object value);
	public virtual Java.Lang.Object Replace (Java.Lang.Object key, Java.Lang.Object value);
```





### Type Changed: Java.Util.Locale

Added property:

```
public bool HasExtensions { get; }
```



Modified methods:

```
public string GetDisplayScript (Locale locale inLocale)
	public string GetDisplayVariant (Locale locale inLocale)
```

Added methods:

```
public static System.Collections.Generic.IList<Locale> Filter (System.Collections.Generic.IList<Locale.LanguageRange> priorityList, System.Collections.Generic.ICollection<Locale> locales);
	public static System.Collections.Generic.IList<Locale> Filter (System.Collections.Generic.IList<Locale.LanguageRange> priorityList, System.Collections.Generic.ICollection<Locale> locales, Locale.FilteringMode mode);
	public static System.Collections.Generic.IList<string> FilterTags (System.Collections.Generic.IList<Locale.LanguageRange> priorityList, System.Collections.Generic.ICollection<string> tags);
	public static System.Collections.Generic.IList<string> FilterTags (System.Collections.Generic.IList<Locale.LanguageRange> priorityList, System.Collections.Generic.ICollection<string> tags, Locale.FilteringMode mode);
	public static Locale Lookup (System.Collections.Generic.IList<Locale.LanguageRange> priorityList, System.Collections.Generic.ICollection<Locale> locales);
	public static string LookupTag (System.Collections.Generic.IList<Locale.LanguageRange> priorityList, System.Collections.Generic.ICollection<string> tags);
	public Locale StripExtensions ();
```



### New Type Java.Util.FilteringMode

<pre class='added' data-is-non-breaking="">
public sealed class FilteringMode : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Locale.FilteringMode AutoselectFiltering { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Locale.FilteringMode ExtendedFiltering { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Locale.FilteringMode IgnoreExtendedRanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Locale.FilteringMode MapExtendedRanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Locale.FilteringMode RejectExtendedRanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Locale.FilteringMode ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Locale.FilteringMode[] Values ();</span>
}
</pre>



### New Type Java.Util.LanguageRange

<pre class='added' data-is-non-breaking="">
public sealed class LanguageRange : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Locale (string range);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Locale (string range, double weight);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const double MaxWeight;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const double MinWeight;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Range { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;Locale.LanguageRange&gt; MapEquivalents (System.Collections.Generic.IList&lt;Locale.LanguageRange&gt; priorityList, System.Collections.Generic.IDictionary&lt;System.String,System.Collections.Generic.IList&lt;string&gt;&gt; map);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;Locale.LanguageRange&gt; Parse (string ranges);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;Locale.LanguageRange&gt; Parse (string ranges, System.Collections.Generic.IDictionary&lt;System.String,System.Collections.Generic.IList&lt;string&gt;&gt; map);</span>
}
</pre>





### Type Changed: Java.Util.Random

Modified methods:

```
public virtual int NextInt (int n bound)
```



### Type Changed: Java.Util.ResourceBundle

Added property:

```
public virtual string BaseBundleName { get; }
```





### Type Changed: Java.Util.Scanner

Added constructors:

```
public Scanner (Java.Nio.FileNio.IPath source);
	public Scanner (Java.Nio.FileNio.IPath source, string charsetName);
```





### New Type Java.Util.Base64

<pre class='added' data-is-non-breaking="">
public class Base64 : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected Base64 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Base64.Decoder MimeDecoder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Base64.Encoder MimeEncoder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Base64.Decoder UrlDecoder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Base64.Encoder UrlEncoder { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Base64.Decoder GetDecoder ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Base64.Encoder GetEncoder ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Base64.Encoder GetMimeEncoder (int lineLength, byte[] lineSeparator);</span>

	// inner types
	public class Decoder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected Base64 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.ByteBuffer Decode (Java.Nio.ByteBuffer buffer);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual byte[] Decode (byte[] src);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual byte[] Decode (string src);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual int Decode (byte[] src, byte[] dst);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual System.IO.Stream Wrap (System.IO.Stream is);</span>
	}
	public class Encoder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected Base64 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.ByteBuffer Encode (Java.Nio.ByteBuffer buffer);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual byte[] Encode (byte[] src);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual int Encode (byte[] src, byte[] dst);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual string EncodeToString (byte[] src);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual Base64.Encoder WithoutPadding ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual System.IO.Stream Wrap (System.IO.Stream os);</span>
	}
}
</pre>





## Namespace Java.Util.Concurrent

### Type Changed: Java.Util.Concurrent.CopyOnWriteArrayList

Modified constructors:

```
public CopyOnWriteArrayList (Java.Lang.Object[] array toCopyIn)
	public CopyOnWriteArrayList (System.Collections.ICollection collection c)
```

Modified methods:

```
public virtual void Add (int index, Java.Lang.Object e element)
	public virtual bool AddAll (System.Collections.ICollection collection c)
	public virtual bool AddAll (int index, System.Collections.ICollection collection c)
	public virtual int AddAllAbsent (System.Collections.ICollection collection c)
	public virtual bool AddIfAbsent (Java.Lang.Object object e)
	public virtual bool ContainsAll (System.Collections.ICollection collection c)
	public virtual int IndexOf (Java.Lang.Object object o)
	public virtual int IndexOf (Java.Lang.Object object e, int from index)
	public virtual int LastIndexOf (Java.Lang.Object object o)
	public virtual int LastIndexOf (Java.Lang.Object object e, int to index)
	public virtual bool RemoveAll (System.Collections.ICollection collection c)
	public virtual bool RetainAll (System.Collections.ICollection collection c)
	public virtual Java.Lang.Object Set (int index, Java.Lang.Object e element)
	public virtual System.Collections.IList SubList (int from fromIndex, int to toIndex)
	public virtual Java.Lang.Object[] ToArray (Java.Lang.Object[] contents a)
```

Added methods:

```
public virtual bool RemoveIf (Java.Util.Functions.IPredicate filter);
	public virtual Java.Util.ISpliterator Spliterator ();
```







## Namespace Java.Util.Jar

### Type Changed: Java.Util.Jar.Pack200

### Type Changed: Java.Util.Jar.Pack200.IPacker

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void AddPropertyChangeListener (Java.Beans.IPropertyChangeListener listener);
	[Obsolete ("deprecated")]
	public virtual void RemovePropertyChangeListener (Java.Beans.IPropertyChangeListener listener);
```



### Type Changed: Java.Util.Jar.Pack200.IUnpacker

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void AddPropertyChangeListener (Java.Beans.IPropertyChangeListener listener);
	[Obsolete ("deprecated")]
	public virtual void RemovePropertyChangeListener (Java.Beans.IPropertyChangeListener listener);
```







## Namespace Java.Util.Logging

### Type Changed: Java.Util.Logging.LogManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void AddPropertyChangeListener (Java.Beans.IPropertyChangeListener l);
	[Obsolete ("deprecated")]
	public virtual void RemovePropertyChangeListener (Java.Beans.IPropertyChangeListener l);
```



### Type Changed: Java.Util.Logging.Logger

Modified properties:

```
public virtual Java.Util.ResourceBundle ResourceBundle { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void Logrb (Level level, string sourceClass, string sourceMethod, string bundleName, string msg);
	[Obsolete ("deprecated")]
	public virtual void Logrb (Level level, string sourceClass, string sourceMethod, string bundleName, string msg, Java.Lang.Object param1);
	[Obsolete ("deprecated")]
	public virtual void Logrb (Level level, string sourceClass, string sourceMethod, string bundleName, string msg, Java.Lang.Object[] params);
	[Obsolete ("deprecated")]
	public virtual void Logrb (Level level, string sourceClass, string sourceMethod, string bundleName, string msg, Java.Lang.Throwable thrown);
```

Added methods:

```
public virtual void Config (Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Fine (Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Finer (Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Finest (Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Info (Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Log (Level level, Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Log (Level level, Java.Lang.Throwable thrown, Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Logp (Level level, string sourceClass, string sourceMethod, Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Logp (Level level, string sourceClass, string sourceMethod, Java.Lang.Throwable thrown, Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Logrb (Level level, string sourceClass, string sourceMethod, Java.Util.ResourceBundle bundle, string msg, Java.Lang.Object[] params);
	public virtual void Logrb (Level level, string sourceClass, string sourceMethod, Java.Util.ResourceBundle bundle, string msg, Java.Lang.Throwable thrown);
	public virtual void Severe (Java.Util.Functions.ISupplier msgSupplier);
	public virtual void Warning (Java.Util.Functions.ISupplier msgSupplier);
```







## Namespace Java.Util.Regex

### Type Changed: Java.Util.Regex.Matcher

Added methods:

```
public int End (string name);
	public string Group (string name);
	public int Start (string name);
```







## Namespace Java.Util.Zip

### Type Changed: Java.Util.Zip.Adler32

Added method:

```
public virtual void Update (Java.Nio.ByteBuffer buffer);
```





### Type Changed: Java.Util.Zip.CRC32

Added method:

```
public virtual void Update (Java.Nio.ByteBuffer buffer);
```





### Type Changed: Java.Util.Zip.ZipEntry

Added properties:

```
public virtual Java.Nio.FileNio.Attributes.FileTime CreationTime { get; }
	public virtual Java.Nio.FileNio.Attributes.FileTime LastAccessTime { get; }
	public virtual Java.Nio.FileNio.Attributes.FileTime LastModifiedTime { get; }
```



Added methods:

```
public virtual ZipEntry SetCreationTime (Java.Nio.FileNio.Attributes.FileTime time);
	public virtual ZipEntry SetLastAccessTime (Java.Nio.FileNio.Attributes.FileTime time);
	public virtual ZipEntry SetLastModifiedTime (Java.Nio.FileNio.Attributes.FileTime time);
```







## Namespace Javax.Crypto.Spec

### Type Changed: Javax.Crypto.Spec.PBEParameterSpec

Added constructor:

```
public PBEParameterSpec (byte[] salt, int iterationCount, Java.Security.Spec.IAlgorithmParameterSpec paramSpec);
```



Added property:

```
public virtual Java.Security.Spec.IAlgorithmParameterSpec ParameterSpec { get; }
```







## Namespace Javax.Microedition.Khronos.Egl

### Type Changed: Javax.Microedition.Khronos.Egl.IEGL10

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual EGLSurface EglCreatePixmapSurface (EGLDisplay display, EGLConfig config, Java.Lang.Object native_pixmap, int[] attrib_list);
```





## New Namespace Android.Companion

### New Type Android.Companion.AssociationRequest

<pre class='added' data-is-non-breaking="">
public sealed class AssociationRequest : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public AssociationRequest ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public AssociationRequest.Builder AddDeviceFilter (IDeviceFilter deviceFilter);</span>
		<span class='added added-method ' data-is-non-breaking="">public AssociationRequest Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public AssociationRequest.Builder SetSingleDevice (bool singleDevice);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Companion.BluetoothDeviceFilter

<pre class='added' data-is-non-breaking="">
public sealed class BluetoothDeviceFilter : Java.Lang.Object, IDeviceFilter, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public BluetoothDeviceFilter ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public BluetoothDeviceFilter.Builder AddServiceUuid (Android.OS.ParcelUuid serviceUuid, Android.OS.ParcelUuid serviceUuidMask);</span>
		<span class='added added-method ' data-is-non-breaking="">public BluetoothDeviceFilter Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public BluetoothDeviceFilter.Builder SetAddress (string address);</span>
		<span class='added added-method ' data-is-non-breaking="">public BluetoothDeviceFilter.Builder SetNamePattern (Java.Util.Regex.Pattern regex);</span>
	}
}
</pre>



### New Type Android.Companion.BluetoothLeDeviceFilter

<pre class='added' data-is-non-breaking="">
public sealed class BluetoothLeDeviceFilter : Java.Lang.Object, IDeviceFilter, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int RenamePrefixLengthLimit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public BluetoothLeDeviceFilter ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public BluetoothLeDeviceFilter Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public BluetoothLeDeviceFilter.Builder SetNamePattern (Java.Util.Regex.Pattern regex);</span>
		<span class='added added-method ' data-is-non-breaking="">public BluetoothLeDeviceFilter.Builder SetRawDataFilter (byte[] rawDataFilter, byte[] rawDataFilterMask);</span>
		<span class='added added-method ' data-is-non-breaking="">public BluetoothLeDeviceFilter.Builder SetRenameFromBytes (string prefix, string suffix, int bytesFrom, int bytesLength, Java.Nio.ByteOrder byteOrder);</span>
		<span class='added added-method ' data-is-non-breaking="">public BluetoothLeDeviceFilter.Builder SetRenameFromName (string prefix, string suffix, int nameFrom, int nameLength);</span>
		<span class='added added-method ' data-is-non-breaking="">public BluetoothLeDeviceFilter.Builder SetScanFilter (Android.Bluetooth.LE.ScanFilter scanFilter);</span>
	}
}
</pre>



### New Type Android.Companion.CompanionDeviceManager

<pre class='added' data-is-non-breaking="">
public sealed class CompanionDeviceManager : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string ExtraDevice = "android.companion.extra.DEVICE";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;string&gt; Associations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Associate (AssociationRequest request, CompanionDeviceManager.Callback callback, Android.OS.Handler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Disassociate (string deviceMacAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool HasNotificationAccess (Android.Content.ComponentName component);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RequestNotificationAccess (Android.Content.ComponentName component);</span>

	// inner types
	public abstract class Callback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public CompanionDeviceManager ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">protected CompanionDeviceManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnDeviceFound (Android.Content.IntentSender chooserLauncher);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnFailure (Java.Lang.ICharSequence error);</span>
		<span class='added added-method ' data-is-non-breaking="">public void OnFailure (string error);</span>
	}
}
</pre>



### New Type Android.Companion.IDeviceFilter

<pre class='added' data-is-non-breaking="">
public interface IDeviceFilter : Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
}
</pre>



### New Type Android.Companion.WifiDeviceFilter

<pre class='added' data-is-non-breaking="">
public sealed class WifiDeviceFilter : Java.Lang.Object, IDeviceFilter, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public WifiDeviceFilter ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public WifiDeviceFilter Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public WifiDeviceFilter.Builder SetNamePattern (Java.Util.Regex.Pattern regex);</span>
	}
}
</pre>





## New Namespace Android.Graphics.Fonts

### New Type Android.Graphics.Fonts.FontVariationAxis

<pre class='added' data-is-non-breaking="">
public sealed class FontVariationAxis : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FontVariationAxis (string tagString, float styleValue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float StyleValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Tag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static FontVariationAxis[] FromFontVariationSettings (string settings);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string ToFontVariationSettings (FontVariationAxis[] axes);</span>
}
</pre>





## New Namespace Android.Net.Wifi.Aware

### New Type Android.Net.Wifi.Aware.AttachCallback

<pre class='added' data-is-non-breaking="">
public class AttachCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AttachCallback ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AttachCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnAttachFailed ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnAttached (WifiAwareSession session);</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.Characteristics

<pre class='added' data-is-non-breaking="">
public sealed class Characteristics : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxMatchFilterLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxServiceNameLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxServiceSpecificInfoLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Net.Wifi.Aware.DiscoverySession

<pre class='added' data-is-non-breaking="">
public class DiscoverySession : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected DiscoverySession (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Android.Net.NetworkSpecifier CreateNetworkSpecifierOpen (PeerHandle peerHandle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Android.Net.NetworkSpecifier CreateNetworkSpecifierPassphrase (PeerHandle peerHandle, string passphrase);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendMessage (PeerHandle peerHandle, int messageId, byte[] message);</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.DiscoverySessionCallback

<pre class='added' data-is-non-breaking="">
public class DiscoverySessionCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DiscoverySessionCallback ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DiscoverySessionCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnMessageReceived (PeerHandle peerHandle, byte[] message);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnMessageSendFailed (int messageId);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnMessageSendSucceeded (int messageId);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnPublishStarted (PublishDiscoverySession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnServiceDiscovered (PeerHandle peerHandle, byte[] serviceSpecificInfo, System.Collections.Generic.IList&lt;System.Byte[]&gt; matchFilter);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnSessionConfigFailed ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnSessionConfigUpdated ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnSessionTerminated ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnSubscribeStarted (SubscribeDiscoverySession session);</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.IdentityChangedListener

<pre class='added' data-is-non-breaking="">
public class IdentityChangedListener : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public IdentityChangedListener ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected IdentityChangedListener (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnIdentityChanged (byte[] mac);</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.PeerHandle

<pre class='added' data-is-non-breaking="">
public class PeerHandle : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PeerHandle (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.PublishConfig

<pre class='added' data-is-non-breaking="">
public sealed class PublishConfig : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public PublishConfig ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public PublishConfig Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public PublishConfig.Builder SetMatchFilter (System.Collections.Generic.IList&lt;System.Byte[]&gt; matchFilter);</span>
		<span class='added added-method ' data-is-non-breaking="">public PublishConfig.Builder SetPublishType (PublishType publishType);</span>
		<span class='added added-method ' data-is-non-breaking="">public PublishConfig.Builder SetServiceName (string serviceName);</span>
		<span class='added added-method ' data-is-non-breaking="">public PublishConfig.Builder SetServiceSpecificInfo (byte[] serviceSpecificInfo);</span>
		<span class='added added-method ' data-is-non-breaking="">public PublishConfig.Builder SetTerminateNotificationEnabled (bool enable);</span>
		<span class='added added-method ' data-is-non-breaking="">public PublishConfig.Builder SetTtlSec (int ttlSec);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Net.Wifi.Aware.PublishDiscoverySession

<pre class='added' data-is-non-breaking="">
public class PublishDiscoverySession : Android.Net.Wifi.Aware.DiscoverySession, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PublishDiscoverySession (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdatePublish (PublishConfig publishConfig);</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.PublishType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PublishType {
	<span class='added added-field ' data-is-non-breaking="">Solicited = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsolicited = 0,</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.SubscribeConfig

<pre class='added' data-is-non-breaking="">
public sealed class SubscribeConfig : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public SubscribeConfig ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public SubscribeConfig Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public SubscribeConfig.Builder SetMatchFilter (System.Collections.Generic.IList&lt;System.Byte[]&gt; matchFilter);</span>
		<span class='added added-method ' data-is-non-breaking="">public SubscribeConfig.Builder SetServiceName (string serviceName);</span>
		<span class='added added-method ' data-is-non-breaking="">public SubscribeConfig.Builder SetServiceSpecificInfo (byte[] serviceSpecificInfo);</span>
		<span class='added added-method ' data-is-non-breaking="">public SubscribeConfig.Builder SetSubscribeType (SubscribeType subscribeType);</span>
		<span class='added added-method ' data-is-non-breaking="">public SubscribeConfig.Builder SetTerminateNotificationEnabled (bool enable);</span>
		<span class='added added-method ' data-is-non-breaking="">public SubscribeConfig.Builder SetTtlSec (int ttlSec);</span>
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Net.Wifi.Aware.SubscribeDiscoverySession

<pre class='added' data-is-non-breaking="">
public class SubscribeDiscoverySession : Android.Net.Wifi.Aware.DiscoverySession, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SubscribeDiscoverySession (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateSubscribe (SubscribeConfig subscribeConfig);</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.SubscribeType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SubscribeType {
	<span class='added added-field ' data-is-non-breaking="">Active = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Passive = 0,</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.WifiAwareDataPathRole

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WifiAwareDataPathRole {
	<span class='added added-field ' data-is-non-breaking="">Initiator = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Responder = 1,</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.WifiAwareManager

<pre class='added' data-is-non-breaking="">
public class WifiAwareManager : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected WifiAwareManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string ActionWifiAwareStateChanged = "android.net.wifi.aware.action.WIFI_AWARE_STATE_CHANGED";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Characteristics Characteristics { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Attach (AttachCallback attachCallback, Android.OS.Handler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Attach (AttachCallback attachCallback, IdentityChangedListener identityChangedListener, Android.OS.Handler handler);</span>
}
</pre>



### New Type Android.Net.Wifi.Aware.WifiAwareSession

<pre class='added' data-is-non-breaking="">
public class WifiAwareSession : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IAutoCloseable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected WifiAwareSession (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Android.Net.NetworkSpecifier CreateNetworkSpecifierOpen (WifiAwareDataPathRole role, byte[] peer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Android.Net.NetworkSpecifier CreateNetworkSpecifierPassphrase (WifiAwareDataPathRole role, byte[] peer, string passphrase);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Publish (PublishConfig publishConfig, DiscoverySessionCallback callback, Android.OS.Handler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Subscribe (SubscribeConfig subscribeConfig, DiscoverySessionCallback callback, Android.OS.Handler handler);</span>
}
</pre>





## New Namespace Android.Net.Wifi.Hotspot2

### New Type Android.Net.Wifi.Hotspot2.ConfigParser

<pre class='added' data-is-non-breaking="">
public sealed class ConfigParser : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PasspointConfiguration ParsePasspointConfig (string mimeType, byte[] data);</span>
}
</pre>



### New Type Android.Net.Wifi.Hotspot2.PasspointConfiguration

<pre class='added' data-is-non-breaking="">
public sealed class PasspointConfiguration : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PasspointConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PasspointConfiguration (PasspointConfiguration source);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Pps.Credential Credential { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Pps.HomeSp HomeSp { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## New Namespace Android.Net.Wifi.Hotspot2.Omadm

### New Type Android.Net.Wifi.Hotspot2.Omadm.PpsMoParser

<pre class='added' data-is-non-breaking="">
public sealed class PpsMoParser : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Android.Net.Wifi.Hotspot2.PasspointConfiguration ParseMoText (string xmlString);</span>
}
</pre>





## New Namespace Android.Net.Wifi.Hotspot2.Pps

### New Type Android.Net.Wifi.Hotspot2.Pps.Credential

<pre class='added' data-is-non-breaking="">
public sealed class Credential : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Credential ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Credential (Credential source);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Java.Security.Cert.X509Certificate CaCertificate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Credential.CertificateCredential CertCredential { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Security.IPrivateKey ClientPrivateKey { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Realm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Security.Cert.X509Certificate[] GetClientCertificateChain ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Credential.SimCredential GetSimCredential ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Credential.UserCredential GetUserCredential ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetClientCertificateChain (Java.Security.Cert.X509Certificate[] certificateChain);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetSimCredential (Credential.SimCredential simCredential);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetUserCredential (Credential.UserCredential userCredential);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public sealed class CertificateCredential : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public Credential ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">public Credential (Credential.CertificateCredential source);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public string CertType { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
		<span class='added added-method ' data-is-non-breaking="">public byte[] GetCertSha256Fingerprint ();</span>
		<span class='added added-method ' data-is-non-breaking="">public void SetCertSha256Fingerprint (byte[] certSha256Fingerprint);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

		// inner types
		public static class InterfaceConsts {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

			<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
		}
	}
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
	public sealed class SimCredential : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public Credential ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">public Credential (Credential.SimCredential source);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public int EapType { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public string Imsi { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

		// inner types
		public static class InterfaceConsts {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

			<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
		}
	}
	public sealed class UserCredential : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public Credential ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">public Credential (Credential.UserCredential source);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public int EapType { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public string NonEapInnerMethod { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public string Password { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public string Username { get; set; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

		// inner types
		public static class InterfaceConsts {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

			<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
		}
	}
}
</pre>



### New Type Android.Net.Wifi.Hotspot2.Pps.HomeSp

<pre class='added' data-is-non-breaking="">
public sealed class HomeSp : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HomeSp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HomeSp (HomeSp source);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Fqdn { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string FriendlyName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public long[] GetRoamingConsortiumOis ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetRoamingConsortiumOis (long[] roamingConsortiumOis);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## New Namespace Android.Views.Autofill

### New Type Android.Views.Autofill.AutofillEventType

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AutofillEventType {
	<span class='added added-field ' data-is-non-breaking="">InputHidden = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">InputShown = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InputUnavailable = 3,</span>
}
</pre>



### New Type Android.Views.Autofill.AutofillId

<pre class='added' data-is-non-breaking="">
public sealed class AutofillId : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>



### New Type Android.Views.Autofill.AutofillManager

<pre class='added' data-is-non-breaking="">
public sealed class AutofillManager : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string ExtraAssistStructure = "android.view.autofill.extra.ASSIST_STRUCTURE";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ExtraAuthenticationResult = "android.view.autofill.extra.AUTHENTICATION_RESULT";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ExtraClientState = "android.view.autofill.extra.CLIENT_STATE";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool HasEnabledAutofillServices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsAutofillSupported { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Cancel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Commit ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void DisableAutofillServices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void NotifyValueChanged (Android.Views.View view);</span>
	<span class='added added-method ' data-is-non-breaking="">public void NotifyValueChanged (Android.Views.View view, int virtualId, AutofillValue value);</span>
	<span class='added added-method ' data-is-non-breaking="">public void NotifyViewEntered (Android.Views.View view);</span>
	<span class='added added-method ' data-is-non-breaking="">public void NotifyViewEntered (Android.Views.View view, int virtualId, Android.Graphics.Rect absBounds);</span>
	<span class='added added-method ' data-is-non-breaking="">public void NotifyViewExited (Android.Views.View view);</span>
	<span class='added added-method ' data-is-non-breaking="">public void NotifyViewExited (Android.Views.View view, int virtualId);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RegisterCallback (AutofillManager.AutofillCallback callback);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RequestAutofill (Android.Views.View view);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RequestAutofill (Android.Views.View view, int virtualId, Android.Graphics.Rect absBounds);</span>
	<span class='added added-method ' data-is-non-breaking="">public void UnregisterCallback (AutofillManager.AutofillCallback callback);</span>

	// inner types
	public abstract class AutofillCallback : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public AutofillManager ();</span>
		<span class='added added-constructor ' data-is-non-breaking="">protected AutofillManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnAutofillEvent (Android.Views.View view, AutofillEventType e);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void OnAutofillEvent (Android.Views.View view, int virtualId, AutofillEventType e);</span>
	}
}
</pre>



### New Type Android.Views.Autofill.AutofillValue

<pre class='added' data-is-non-breaking="">
public sealed class AutofillValue : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Android.OS.IParcelableCreator Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long DateValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsList { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsToggle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int ListValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string TextValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Lang.ICharSequence TextValueFormatted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool ToggleValue { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DescribeContents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AutofillValue ForDate (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AutofillValue ForList (int value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AutofillValue ForText (Java.Lang.ICharSequence value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AutofillValue ForText (string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AutofillValue ForToggle (bool value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);</span>

	// inner types
	public static class InterfaceConsts {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public static const int ContentsFileDescriptor;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;</span>
	}
}
</pre>





## New Namespace Android.Views.TextClassifiers

### New Type Android.Views.TextClassifiers.ITextClassifier

<pre class='added' data-is-non-breaking="">
public interface ITextClassifier : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual TextClassification ClassifyText (Java.Lang.ICharSequence text, int startIndex, int endIndex, Android.OS.LocaleList defaultLocales);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual TextSelection SuggestSelection (Java.Lang.ICharSequence text, int selectionStartIndex, int selectionEndIndex, Android.OS.LocaleList defaultLocales);</span>
}
</pre>



### New Type Android.Views.TextClassifiers.ITextClassifierExtensions

<pre class='added' data-is-non-breaking="">
public static class ITextClassifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static TextClassification ClassifyText (ITextClassifier self, string text, int startIndex, int endIndex, Android.OS.LocaleList defaultLocales);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TextSelection SuggestSelection (ITextClassifier self, string text, int selectionStartIndex, int selectionEndIndex, Android.OS.LocaleList defaultLocales);</span>
}
</pre>



### New Type Android.Views.TextClassifiers.TextClassification

<pre class='added' data-is-non-breaking="">
public sealed class TextClassification : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int EntityCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Graphics.Drawables.Drawable Icon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Content.Intent Intent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Lang.ICharSequence LabelFormatted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Android.Views.View.IOnClickListener OnClickListener { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Text { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public float GetConfidenceScore (string entity);</span>
	<span class='added added-method ' data-is-non-breaking="">public string GetEntity (int index);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public TextClassification ();</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public TextClassification Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public TextClassification.Builder SetEntityType (string type, float confidenceScore);</span>
		<span class='added added-method ' data-is-non-breaking="">public TextClassification.Builder SetIcon (Android.Graphics.Drawables.Drawable icon);</span>
		<span class='added added-method ' data-is-non-breaking="">public TextClassification.Builder SetIntent (Android.Content.Intent intent);</span>
		<span class='added added-method ' data-is-non-breaking="">public TextClassification.Builder SetLabel (string label);</span>
		<span class='added added-method ' data-is-non-breaking="">public TextClassification.Builder SetOnClickListener (Android.Views.View.IOnClickListener onClickListener);</span>
		<span class='added added-method ' data-is-non-breaking="">public TextClassification.Builder SetText (string text);</span>
	}
}
</pre>



### New Type Android.Views.TextClassifiers.TextClassificationManager

<pre class='added' data-is-non-breaking="">
public sealed class TextClassificationManager : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ITextClassifier TextClassifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Android.Views.TextClassifiers.TextClassifier

<pre class='added' data-is-non-breaking="">
public abstract class TextClassifier : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string TypeAddress = "address";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string TypeEmail = "email";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string TypeOther = "other";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string TypePhone = "phone";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string TypeUrl = "url";</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static ITextClassifier NoOp { get; }</span>
}
</pre>



### New Type Android.Views.TextClassifiers.TextClassifierConsts

<pre class='added' data-is-non-breaking="">
public abstract class TextClassifierConsts : Android.Views.TextClassifiers.TextClassifier, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
}
</pre>



### New Type Android.Views.TextClassifiers.TextSelection

<pre class='added' data-is-non-breaking="">
public sealed class TextSelection : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int EntityCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int SelectionEndIndex { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int SelectionStartIndex { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public float GetConfidenceScore (string entity);</span>
	<span class='added added-method ' data-is-non-breaking="">public string GetEntity (int index);</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public TextSelection (int startIndex, int endIndex);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public TextSelection Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public TextSelection.Builder SetEntityType (string type, float confidenceScore);</span>
	}
}
</pre>





## New Namespace Java.Lang.Invoke

### New Type Java.Lang.Invoke.CallSite

<pre class='added' data-is-non-breaking="">
public abstract class CallSite : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CallSite (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MethodHandle Target { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodHandle DynamicInvoker ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodType Type ();</span>
}
</pre>



### New Type Java.Lang.Invoke.ConstantCallSite

<pre class='added' data-is-non-breaking="">
public class ConstantCallSite : Java.Lang.Invoke.CallSite, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ConstantCallSite (MethodHandle target);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ConstantCallSite (MethodType targetType, MethodHandle createTargetHook);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ConstantCallSite (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override MethodHandle Target { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override MethodHandle DynamicInvoker ();</span>
}
</pre>



### New Type Java.Lang.Invoke.IMethodHandleInfo

<pre class='added' data-is-non-breaking="">
public interface IMethodHandleInfo : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Java.Lang.Class DeclaringClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MethodType MethodType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int Modifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ReferenceKind ReferenceKind { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object ReflectAs (Java.Lang.Class expected, MethodHandles.Lookup lookup);</span>
}
</pre>



### New Type Java.Lang.Invoke.LambdaConversionException

<pre class='added' data-is-non-breaking="">
public class LambdaConversionException : Java.Lang.Exception, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LambdaConversionException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public LambdaConversionException (Java.Lang.Throwable cause);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public LambdaConversionException (string message);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected LambdaConversionException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public LambdaConversionException (string message, Java.Lang.Throwable cause);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public LambdaConversionException (string message, Java.Lang.Throwable cause, bool enableSuppression, bool writableStackTrace);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Lang.Invoke.MethodHandle

<pre class='added' data-is-non-breaking="">
public abstract class MethodHandle : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MethodHandle (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsVarargsCollector { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodHandle AsCollector (Java.Lang.Class arrayType, int arrayLength);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodHandle AsFixedArity ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodHandle AsSpreader (Java.Lang.Class arrayType, int arrayLength);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodHandle AsType (MethodType newType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodHandle AsVarargsCollector (Java.Lang.Class arrayType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodHandle BindTo (Java.Lang.Object x);</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Object Invoke (Java.Lang.Object[] args);</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Object InvokeExact (Java.Lang.Object[] args);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object InvokeWithArguments (Java.Lang.Object[] arguments);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object InvokeWithArguments (System.Collections.Generic.IList&lt;object&gt; arguments);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MethodType Type ();</span>
}
</pre>



### New Type Java.Lang.Invoke.MethodHandleInfo

<pre class='added' data-is-non-breaking="">
public abstract class MethodHandleInfo : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// fields

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFGetField;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFGetStatic;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFInvokeInterface;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFInvokeSpecial;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFInvokeStatic;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFInvokeVirtual;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFNewInvokeSpecial;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFPutField;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.ReferenceKind enum directly instead of this field.")]
	public static const ReferenceKind REFPutStatic;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool RefKindIsField (ReferenceKind refKind);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool RefKindIsValid (ReferenceKind refKind);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string RefKindName (ReferenceKind refKind);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string ReferenceKindToString (ReferenceKind referenceKind);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string ToString (ReferenceKind kind, Java.Lang.Class defc, string name, MethodType type);</span>
}
</pre>



### New Type Java.Lang.Invoke.MethodHandleInfoConsts

<pre class='added' data-is-non-breaking="">
public abstract class MethodHandleInfoConsts : Java.Lang.Invoke.MethodHandleInfo, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
}
</pre>



### New Type Java.Lang.Invoke.MethodHandles

<pre class='added' data-is-non-breaking="">
public class MethodHandles : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MethodHandles (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle ArrayElementGetter (Java.Lang.Class arrayClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle ArrayElementSetter (Java.Lang.Class arrayClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle CatchException (MethodHandle target, Java.Lang.Class exType, MethodHandle handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle CollectArguments (MethodHandle target, int pos, MethodHandle filter);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle Constant (Java.Lang.Class type, Java.Lang.Object value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle DropArguments (MethodHandle target, int pos, Java.Lang.Class[] valueTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle DropArguments (MethodHandle target, int pos, System.Collections.Generic.IList&lt;Java.Lang.Class&gt; valueTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle ExactInvoker (MethodType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle ExplicitCastArguments (MethodHandle target, MethodType newType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle FilterArguments (MethodHandle target, int pos, MethodHandle[] filters);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle FilterReturnValue (MethodHandle target, MethodHandle filter);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle FoldArguments (MethodHandle target, MethodHandle combiner);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle GuardWithTest (MethodHandle test, MethodHandle target, MethodHandle fallback);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle Identity (Java.Lang.Class type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle InsertArguments (MethodHandle target, int pos, Java.Lang.Object[] values);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandles.Lookup InvokeLookup ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle Invoker (MethodType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle PermuteArguments (MethodHandle target, MethodType newType, int[] reorder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandles.Lookup PublicLookup ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.Lang.Object ReflectAs (Java.Lang.Class expected, MethodHandle target);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle SpreadInvoker (MethodType type, int leadingArgCount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodHandle ThrowException (Java.Lang.Class returnType, Java.Lang.Class exType);</span>

	// inner types
	public sealed class Lookup : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// fields

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.MethodLookupModes enum directly instead of this field.")]
		public static const MethodLookupModes Package;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.MethodLookupModes enum directly instead of this field.")]
		public static const MethodLookupModes Private;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.MethodLookupModes enum directly instead of this field.")]
		public static const MethodLookupModes Protected;</span>

		<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This constant will be removed in the future version. Use Java.Lang.Invoke.MethodLookupModes enum directly instead of this field.")]
		public static const MethodLookupModes Public;</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle Bind (Java.Lang.Object receiver, string name, MethodType type);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle FindConstructor (Java.Lang.Class refc, MethodType type);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle FindGetter (Java.Lang.Class refc, string name, Java.Lang.Class type);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle FindSetter (Java.Lang.Class refc, string name, Java.Lang.Class type);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle FindSpecial (Java.Lang.Class refc, string name, MethodType type, Java.Lang.Class specialCaller);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle FindStatic (Java.Lang.Class refc, string name, MethodType type);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle FindStaticGetter (Java.Lang.Class refc, string name, Java.Lang.Class type);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle FindStaticSetter (Java.Lang.Class refc, string name, Java.Lang.Class type);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle FindVirtual (Java.Lang.Class refc, string name, MethodType type);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandles.Lookup In (Java.Lang.Class requestedLookupClass);</span>
		<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Class LookupClass ();</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodLookupModes LookupModes ();</span>
		<span class='added added-method ' data-is-non-breaking="">public IMethodHandleInfo RevealDirect (MethodHandle target);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle Unreflect (Java.Lang.Reflect.Method m);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle UnreflectConstructor (Java.Lang.Reflect.Constructor c);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle UnreflectGetter (Java.Lang.Reflect.Field f);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle UnreflectSetter (Java.Lang.Reflect.Field f);</span>
		<span class='added added-method ' data-is-non-breaking="">public MethodHandle UnreflectSpecial (Java.Lang.Reflect.Method m, Java.Lang.Class specialCaller);</span>
	}
}
</pre>



### New Type Java.Lang.Invoke.MethodLookupModes

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MethodLookupModes {
	<span class='added added-field ' data-is-non-breaking="">Package = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Private = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Protected = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Public = 1,</span>
}
</pre>



### New Type Java.Lang.Invoke.MethodType

<pre class='added' data-is-non-breaking="">
public sealed class MethodType : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool HasPrimitives { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool HasWrappers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public MethodType AppendParameterTypes (Java.Lang.Class[] ptypesToInsert);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType AppendParameterTypes (System.Collections.Generic.IList&lt;Java.Lang.Class&gt; ptypesToInsert);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType ChangeParameterType (int num, Java.Lang.Class nptype);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType ChangeReturnType (Java.Lang.Class nrtype);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType DropParameterTypes (int start, int end);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType Erase ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType FromMethodDescriptorString (string descriptor, Java.Lang.ClassLoader loader);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType Generic ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType GenericMethodType (int objectArgCount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType GenericMethodType (int objectArgCount, bool finalArray);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType InsertParameterTypes (int num, Java.Lang.Class[] ptypesToInsert);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType InsertParameterTypes (int num, System.Collections.Generic.IList&lt;Java.Lang.Class&gt; ptypesToInsert);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType InvokeMethodType (Java.Lang.Class rtype);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType InvokeMethodType (Java.Lang.Class rtype, Java.Lang.Class ptype0);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType InvokeMethodType (Java.Lang.Class rtype, Java.Lang.Class[] ptypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType InvokeMethodType (Java.Lang.Class rtype, MethodType ptypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType InvokeMethodType (Java.Lang.Class rtype, System.Collections.Generic.IList&lt;Java.Lang.Class&gt; ptypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MethodType InvokeMethodType (Java.Lang.Class rtype, Java.Lang.Class ptype0, Java.Lang.Class[] ptypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Class[] ParameterArray ();</span>
	<span class='added added-method ' data-is-non-breaking="">public int ParameterCount ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;Java.Lang.Class&gt; ParameterList ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Class ParameterType (int num);</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Class ReturnType ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string ToMethodDescriptorString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType Unwrap ();</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodType Wrap ();</span>
}
</pre>



### New Type Java.Lang.Invoke.MutableCallSite

<pre class='added' data-is-non-breaking="">
public class MutableCallSite : Java.Lang.Invoke.CallSite, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MutableCallSite (MethodHandle target);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MutableCallSite (MethodType type);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MutableCallSite (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override MethodHandle Target { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override MethodHandle DynamicInvoker ();</span>
}
</pre>



### New Type Java.Lang.Invoke.ReferenceKind

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ReferenceKind {
	<span class='added added-field ' data-is-non-breaking="">Getfield = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Getstatic = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Invokeinterface = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Invokespecial = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Invokestatic = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Invokevirtual = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Newinvokespecial = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Putfield = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Putstatic = 4,</span>
}
</pre>



### New Type Java.Lang.Invoke.VolatileCallSite

<pre class='added' data-is-non-breaking="">
public class VolatileCallSite : Java.Lang.Invoke.CallSite, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VolatileCallSite (MethodHandle target);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VolatileCallSite (MethodType type);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VolatileCallSite (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override MethodHandle Target { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override MethodHandle DynamicInvoker ();</span>
}
</pre>



### New Type Java.Lang.Invoke.WrongMethodTypeException

<pre class='added' data-is-non-breaking="">
public class WrongMethodTypeException : Java.Lang.RuntimeException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WrongMethodTypeException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WrongMethodTypeException (string s);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WrongMethodTypeException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





## New Namespace Java.Nio.FileNio

### New Type Java.Nio.FileNio.AccessDeniedException

<pre class='added' data-is-non-breaking="">
public class AccessDeniedException : Java.Nio.FileNio.FileSystemException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AccessDeniedException (string file);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AccessDeniedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AccessDeniedException (string file, string other, string reason);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.AccessMode

<pre class='added' data-is-non-breaking="">
public sealed class AccessMode : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static AccessMode Execute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AccessMode Read { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AccessMode Write { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AccessMode ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AccessMode[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.AtomicMoveNotSupportedException

<pre class='added' data-is-non-breaking="">
public class AtomicMoveNotSupportedException : Java.Nio.FileNio.FileSystemException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AtomicMoveNotSupportedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AtomicMoveNotSupportedException (string source, string target, string reason);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.ClosedDirectoryStreamException

<pre class='added' data-is-non-breaking="">
public class ClosedDirectoryStreamException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ClosedDirectoryStreamException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ClosedDirectoryStreamException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.ClosedFileSystemException

<pre class='added' data-is-non-breaking="">
public class ClosedFileSystemException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ClosedFileSystemException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ClosedFileSystemException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.ClosedWatchServiceException

<pre class='added' data-is-non-breaking="">
public class ClosedWatchServiceException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ClosedWatchServiceException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ClosedWatchServiceException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.DirectoryIteratorException

<pre class='added' data-is-non-breaking="">
public sealed class DirectoryIteratorException : Java.Util.ConcurrentModificationException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DirectoryIteratorException (Java.IO.IOException cause);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.DirectoryNotEmptyException

<pre class='added' data-is-non-breaking="">
public class DirectoryNotEmptyException : Java.Nio.FileNio.FileSystemException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DirectoryNotEmptyException (string dir);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DirectoryNotEmptyException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.FileAlreadyExistsException

<pre class='added' data-is-non-breaking="">
public class FileAlreadyExistsException : Java.Nio.FileNio.FileSystemException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FileAlreadyExistsException (string file);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileAlreadyExistsException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FileAlreadyExistsException (string file, string other, string reason);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.FileStore

<pre class='added' data-is-non-breaking="">
public abstract class FileStore : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected FileStore ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileStore (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long TotalSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long UnallocatedSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long UsableSpace { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object GetAttribute (string attribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object GetFileStoreAttributeView (Java.Lang.Class type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SupportsFileAttributeView (Java.Lang.Class type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SupportsFileAttributeView (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string Type ();</span>
}
</pre>



### New Type Java.Nio.FileNio.FileSystem

<pre class='added' data-is-non-breaking="">
public abstract class FileSystem : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ICloseable, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected FileSystem ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileSystem (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Java.Lang.IIterable FileStores { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOpen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Java.Lang.IIterable RootDirectories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Separator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Attributes.UserPrincipalLookupService UserPrincipalLookupService { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath GetPath (string first, string[] more);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPathMatcher GetPathMatcher (string syntaxAndPattern);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchService NewWatchService ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Spi.FileSystemProvider Provider ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.Generic.ICollection&lt;string&gt; SupportedFileAttributeViews ();</span>
}
</pre>



### New Type Java.Nio.FileNio.FileSystemAlreadyExistsException

<pre class='added' data-is-non-breaking="">
public class FileSystemAlreadyExistsException : Java.Lang.RuntimeException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemAlreadyExistsException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemAlreadyExistsException (string msg);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileSystemAlreadyExistsException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.FileSystemException

<pre class='added' data-is-non-breaking="">
public class FileSystemException : Java.IO.IOException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemException (string file);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileSystemException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemException (string file, string other, string reason);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string File { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string OtherFile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Reason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.FileSystemLoopException

<pre class='added' data-is-non-breaking="">
public class FileSystemLoopException : Java.Nio.FileNio.FileSystemException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemLoopException (string file);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileSystemLoopException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.FileSystemNotFoundException

<pre class='added' data-is-non-breaking="">
public class FileSystemNotFoundException : Java.Lang.RuntimeException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemNotFoundException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemNotFoundException (string msg);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileSystemNotFoundException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.FileSystems

<pre class='added' data-is-non-breaking="">
public sealed class FileSystems : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static FileSystem Default { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static FileSystem GetFileSystem (Java.Net.URI uri);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FileSystem NewFileSystem (Java.Net.URI uri, System.Collections.Generic.IDictionary&lt;System.String,System.Object&gt; env);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FileSystem NewFileSystem (IPath path, Java.Lang.ClassLoader loader);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FileSystem NewFileSystem (Java.Net.URI uri, System.Collections.Generic.IDictionary&lt;System.String,System.Object&gt; env, Java.Lang.ClassLoader loader);</span>
}
</pre>



### New Type Java.Nio.FileNio.FileVisitOption

<pre class='added' data-is-non-breaking="">
public sealed class FileVisitOption : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static FileVisitOption FollowLinks { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static FileVisitOption ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FileVisitOption[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.FileVisitResult

<pre class='added' data-is-non-breaking="">
public sealed class FileVisitResult : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static FileVisitResult Continue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static FileVisitResult SkipSiblings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static FileVisitResult SkipSubtree { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static FileVisitResult Terminate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static FileVisitResult ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FileVisitResult[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Files

<pre class='added' data-is-non-breaking="">
public sealed class Files : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static long Copy (IPath source, System.IO.Stream out);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath Copy (IPath source, IPath target, ICopyOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static long Copy (System.IO.Stream in, IPath target, ICopyOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateDirectories (IPath dir, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateDirectory (IPath dir, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateFile (IPath path, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateLink (IPath link, IPath existing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateSymbolicLink (IPath link, IPath target, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateTempDirectory (string prefix, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateTempDirectory (IPath dir, string prefix, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateTempFile (string prefix, string suffix, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath CreateTempFile (IPath dir, string prefix, string suffix, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Delete (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool DeleteIfExists (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Exists (IPath path, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.Lang.Object GetAttribute (IPath path, string attribute, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.Lang.Object GetFileAttributeView (IPath path, Java.Lang.Class type, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FileStore GetFileStore (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Attributes.FileTime GetLastModifiedTime (IPath path, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Attributes.IUserPrincipal GetOwner (IPath path, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.ICollection&lt;Attributes.PosixFilePermission&gt; GetPosixFilePermissions (IPath path, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsDirectory (IPath path, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsExecutable (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsHidden (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsReadable (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsRegularFile (IPath path, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsSameFile (IPath path, IPath path2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsSymbolicLink (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsWritable (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath Move (IPath source, IPath target, ICopyOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.IO.BufferedReader NewBufferedReader (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.IO.BufferedReader NewBufferedReader (IPath path, Java.Nio.Charset.Charset cs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.IO.BufferedWriter NewBufferedWriter (IPath path, IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.IO.BufferedWriter NewBufferedWriter (IPath path, Java.Nio.Charset.Charset cs, IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.Nio.Channels.ISeekableByteChannel NewByteChannel (IPath path, IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.Nio.Channels.ISeekableByteChannel NewByteChannel (IPath path, System.Collections.Generic.ICollection&lt;IOpenOption&gt; options, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IDirectoryStream NewDirectoryStream (IPath dir);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IDirectoryStream NewDirectoryStream (IPath dir, IDirectoryStreamFilter filter);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IDirectoryStream NewDirectoryStream (IPath dir, string glob);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.IO.Stream NewInputStream (IPath path, IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.IO.Stream NewOutputStream (IPath path, IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool NotExists (IPath path, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string ProbeContentType (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static byte[] ReadAllBytes (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;string&gt; ReadAllLines (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;string&gt; ReadAllLines (IPath path, Java.Nio.Charset.Charset cs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Java.Lang.Object ReadAttributes (IPath path, Java.Lang.Class type, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IDictionary&lt;System.String,Java.Lang.Object&gt; ReadAttributes (IPath path, string attributes, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath ReadSymbolicLink (IPath link);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath SetAttribute (IPath path, string attribute, Java.Lang.Object value, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath SetLastModifiedTime (IPath path, Attributes.FileTime time);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath SetOwner (IPath path, Attributes.IUserPrincipal owner);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath SetPosixFilePermissions (IPath path, System.Collections.Generic.ICollection&lt;Attributes.PosixFilePermission&gt; perms);</span>
	<span class='added added-method ' data-is-non-breaking="">public static long Size (IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath WalkFileTree (IPath start, IFileVisitor visitor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath WalkFileTree (IPath start, System.Collections.Generic.ICollection&lt;FileVisitOption&gt; options, int maxDepth, IFileVisitor visitor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath Write (IPath path, Java.Lang.IIterable lines, IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath Write (IPath path, byte[] bytes, IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath Write (IPath path, Java.Lang.IIterable lines, Java.Nio.Charset.Charset cs, IOpenOption[] options);</span>
}
</pre>



### New Type Java.Nio.FileNio.ICopyOption

<pre class='added' data-is-non-breaking="">
public interface ICopyOption : Android.Runtime.IJavaObject, System.IDisposable {
}
</pre>



### New Type Java.Nio.FileNio.IDirectoryStream

<pre class='added' data-is-non-breaking="">
public interface IDirectoryStream : Android.Runtime.IJavaObject, Java.IO.ICloseable, Java.Lang.IIterable, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.IIterator Iterator ();</span>
}
</pre>



### New Type Java.Nio.FileNio.IDirectoryStreamFilter

<pre class='added' data-is-non-breaking="">
public interface IDirectoryStreamFilter : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Accept (Java.Lang.Object entry);</span>
}
</pre>



### New Type Java.Nio.FileNio.IFileVisitor

<pre class='added' data-is-non-breaking="">
public interface IFileVisitor : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual FileVisitResult PostVisitDirectory (Java.Lang.Object dir, Java.IO.IOException exc);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileVisitResult PreVisitDirectory (Java.Lang.Object dir, Attributes.IBasicFileAttributes attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileVisitResult VisitFile (Java.Lang.Object file, Attributes.IBasicFileAttributes attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileVisitResult VisitFileFailed (Java.Lang.Object file, Java.IO.IOException exc);</span>
}
</pre>



### New Type Java.Nio.FileNio.IOpenOption

<pre class='added' data-is-non-breaking="">
public interface IOpenOption : Android.Runtime.IJavaObject, System.IDisposable {
}
</pre>



### New Type Java.Nio.FileNio.IPath

<pre class='added' data-is-non-breaking="">
public interface IPath : Android.Runtime.IJavaObject, Java.Lang.IComparable, Java.Lang.IIterable, IWatchable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IPath FileName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual FileSystem FileSystem { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAbsolute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int NameCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IPath Parent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IPath Root { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (IPath other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndsWith (IPath other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndsWith (string other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (Java.Lang.Object other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath GetName (int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Util.IIterator Iterator ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath Normalize ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchKey Register (IWatchService watcher, IWatchEventKind[] events);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchKey Register (IWatchService watcher, IWatchEventKind[] events, IWatchEventModifier[] modifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath Relativize (IPath other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath Resolve (IPath other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath Resolve (string other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath ResolveSibling (IPath other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath ResolveSibling (string other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool StartsWith (IPath other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool StartsWith (string other);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath Subpath (int beginIndex, int endIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath ToAbsolutePath ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.IO.File ToFile ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPath ToRealPath (LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Net.URI ToUri ();</span>
}
</pre>



### New Type Java.Nio.FileNio.IPathMatcher

<pre class='added' data-is-non-breaking="">
public interface IPathMatcher : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Matches (IPath path);</span>
}
</pre>



### New Type Java.Nio.FileNio.ISecureDirectoryStream

<pre class='added' data-is-non-breaking="">
public interface ISecureDirectoryStream : Android.Runtime.IJavaObject, Java.IO.ICloseable, Java.Lang.IIterable, IDirectoryStream, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeleteDirectory (Java.Lang.Object path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeleteFile (Java.Lang.Object path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object GetFileAttributeView (Java.Lang.Class type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object GetFileAttributeView (Java.Lang.Object path, Java.Lang.Class type, LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Move (Java.Lang.Object srcpath, ISecureDirectoryStream targetdir, Java.Lang.Object targetpath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.Channels.ISeekableByteChannel NewByteChannel (Java.Lang.Object path, System.Collections.Generic.ICollection&lt;IOpenOption&gt; options, Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ISecureDirectoryStream NewDirectoryStream (Java.Lang.Object path, LinkOption[] options);</span>
}
</pre>



### New Type Java.Nio.FileNio.IWatchEvent

<pre class='added' data-is-non-breaking="">
public interface IWatchEvent : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object Context ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Count ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchEventKind Kind ();</span>
}
</pre>



### New Type Java.Nio.FileNio.IWatchEventKind

<pre class='added' data-is-non-breaking="">
public interface IWatchEventKind : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Class Type ();</span>
}
</pre>



### New Type Java.Nio.FileNio.IWatchEventModifier

<pre class='added' data-is-non-breaking="">
public interface IWatchEventModifier : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
}
</pre>



### New Type Java.Nio.FileNio.IWatchKey

<pre class='added' data-is-non-breaking="">
public interface IWatchKey : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsValid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Cancel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.Generic.IList&lt;IWatchEvent&gt; PollEvents ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Reset ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchable Watchable ();</span>
}
</pre>



### New Type Java.Nio.FileNio.IWatchService

<pre class='added' data-is-non-breaking="">
public interface IWatchService : Android.Runtime.IJavaObject, Java.IO.ICloseable, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchKey Poll ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchKey Poll (long timeout, Java.Util.Concurrent.TimeUnit unit);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchKey Take ();</span>
}
</pre>



### New Type Java.Nio.FileNio.IWatchable

<pre class='added' data-is-non-breaking="">
public interface IWatchable : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchKey Register (IWatchService watcher, IWatchEventKind[] events);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWatchKey Register (IWatchService watcher, IWatchEventKind[] events, IWatchEventModifier[] modifiers);</span>
}
</pre>



### New Type Java.Nio.FileNio.InvalidPathException

<pre class='added' data-is-non-breaking="">
public class InvalidPathException : Java.Lang.IllegalArgumentException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected InvalidPathException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public InvalidPathException (string input, string reason);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public InvalidPathException (string input, string reason, int index);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual int Index { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Input { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Reason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.LinkOption

<pre class='added' data-is-non-breaking="">
public sealed class LinkOption : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, ICopyOption, IOpenOption, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static LinkOption NofollowLinks { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static LinkOption ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static LinkOption[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.LinkPermission

<pre class='added' data-is-non-breaking="">
public sealed class LinkPermission : Java.Security.BasicPermission, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Security.IGuard, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LinkPermission (string name);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public LinkPermission (string name, string actions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.NoSuchFileException

<pre class='added' data-is-non-breaking="">
public class NoSuchFileException : Java.Nio.FileNio.FileSystemException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NoSuchFileException (string file);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NoSuchFileException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NoSuchFileException (string file, string other, string reason);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.NotDirectoryException

<pre class='added' data-is-non-breaking="">
public class NotDirectoryException : Java.Nio.FileNio.FileSystemException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NotDirectoryException (string file);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NotDirectoryException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.NotLinkException

<pre class='added' data-is-non-breaking="">
public class NotLinkException : Java.Nio.FileNio.FileSystemException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NotLinkException (string file);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NotLinkException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NotLinkException (string file, string other, string reason);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.Paths

<pre class='added' data-is-non-breaking="">
public sealed class Paths : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IPath Get (Java.Net.URI uri);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IPath Get (string first, string[] more);</span>
}
</pre>



### New Type Java.Nio.FileNio.ProviderMismatchException

<pre class='added' data-is-non-breaking="">
public class ProviderMismatchException : Java.Lang.IllegalArgumentException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ProviderMismatchException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ProviderMismatchException (string msg);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ProviderMismatchException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.ProviderNotFoundException

<pre class='added' data-is-non-breaking="">
public class ProviderNotFoundException : Java.Lang.RuntimeException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ProviderNotFoundException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ProviderNotFoundException (string msg);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ProviderNotFoundException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.ReadOnlyFileSystemException

<pre class='added' data-is-non-breaking="">
public class ReadOnlyFileSystemException : Java.Lang.UnsupportedOperationException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ReadOnlyFileSystemException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ReadOnlyFileSystemException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.SimpleFileVisitor

<pre class='added' data-is-non-breaking="">
public class SimpleFileVisitor : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, IFileVisitor, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SimpleFileVisitor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SimpleFileVisitor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual FileVisitResult PostVisitDirectory (Java.Lang.Object dir, Java.IO.IOException exc);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileVisitResult PreVisitDirectory (Java.Lang.Object dir, Attributes.IBasicFileAttributes attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileVisitResult VisitFile (Java.Lang.Object file, Attributes.IBasicFileAttributes attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileVisitResult VisitFileFailed (Java.Lang.Object file, Java.IO.IOException exc);</span>
}
</pre>



### New Type Java.Nio.FileNio.StandardCopyOption

<pre class='added' data-is-non-breaking="">
public sealed class StandardCopyOption : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, ICopyOption, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static StandardCopyOption AtomicMove { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardCopyOption CopyAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardCopyOption ReplaceExisting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static StandardCopyOption ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static StandardCopyOption[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.StandardOpenOption

<pre class='added' data-is-non-breaking="">
public sealed class StandardOpenOption : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, IOpenOption, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption Append { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption Create { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption CreateNew { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption DeleteOnClose { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption Dsync { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption Read { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption Sparse { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption Sync { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption TruncateExisting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static StandardOpenOption Write { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static StandardOpenOption ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static StandardOpenOption[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.StandardWatchEventKinds

<pre class='added' data-is-non-breaking="">
public sealed class StandardWatchEventKinds : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static IWatchEventKind EntryCreate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IWatchEventKind EntryDelete { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IWatchEventKind EntryModify { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IWatchEventKind Overflow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





## New Namespace Java.Nio.FileNio.Attributes

### New Type Java.Nio.FileNio.Attributes.AclEntry

<pre class='added' data-is-non-breaking="">
public sealed class AclEntry : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.Generic.ICollection&lt;AclEntryFlag&gt; Flags ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AclEntry.Builder NewBuilder ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AclEntry.Builder NewBuilder (AclEntry entry);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.Generic.ICollection&lt;AclEntryPermission&gt; Permissions ();</span>
	<span class='added added-method ' data-is-non-breaking="">public IUserPrincipal Principal ();</span>
	<span class='added added-method ' data-is-non-breaking="">public AclEntryType Type ();</span>

	// inner types
	public sealed class Builder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public AclEntry Build ();</span>
		<span class='added added-method ' data-is-non-breaking="">public AclEntry.Builder SetFlags (AclEntryFlag[] flags);</span>
		<span class='added added-method ' data-is-non-breaking="">public AclEntry.Builder SetFlags (System.Collections.Generic.ICollection&lt;AclEntryFlag&gt; flags);</span>
		<span class='added added-method ' data-is-non-breaking="">public AclEntry.Builder SetPermissions (AclEntryPermission[] perms);</span>
		<span class='added added-method ' data-is-non-breaking="">public AclEntry.Builder SetPermissions (System.Collections.Generic.ICollection&lt;AclEntryPermission&gt; perms);</span>
		<span class='added added-method ' data-is-non-breaking="">public AclEntry.Builder SetPrincipal (IUserPrincipal who);</span>
		<span class='added added-method ' data-is-non-breaking="">public AclEntry.Builder SetType (AclEntryType type);</span>
	}
}
</pre>



### New Type Java.Nio.FileNio.Attributes.AclEntryFlag

<pre class='added' data-is-non-breaking="">
public sealed class AclEntryFlag : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryFlag DirectoryInherit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryFlag FileInherit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryFlag InheritOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryFlag NoPropagateInherit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AclEntryFlag ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AclEntryFlag[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.AclEntryPermission

<pre class='added' data-is-non-breaking="">
public sealed class AclEntryPermission : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission AddFile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission AddSubdirectory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission AppendData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission Delete { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission DeleteChild { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission Execute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission ListDirectory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission ReadAcl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission ReadAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission ReadData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission ReadNamedAttrs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission Synchronize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission WriteAcl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission WriteAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission WriteData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission WriteNamedAttrs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryPermission WriteOwner { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AclEntryPermission ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AclEntryPermission[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.AclEntryType

<pre class='added' data-is-non-breaking="">
public sealed class AclEntryType : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryType Alarm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryType Allow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryType Audit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AclEntryType Deny { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AclEntryType ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AclEntryType[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.FileTime

<pre class='added' data-is-non-breaking="">
public sealed class FileTime : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public int CompareTo (FileTime other);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FileTime From (long value, Java.Util.Concurrent.TimeUnit unit);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FileTime FromMillis (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public long To (Java.Util.Concurrent.TimeUnit unit);</span>
	<span class='added added-method ' data-is-non-breaking="">public long ToMillis ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IAclFileAttributeView

<pre class='added' data-is-non-breaking="">
public interface IAclFileAttributeView : Android.Runtime.IJavaObject, IAttributeView, IFileAttributeView, IFileOwnerAttributeView, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Collections.Generic.IList&lt;AclEntry&gt; Acl { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IAttributeView

<pre class='added' data-is-non-breaking="">
public interface IAttributeView : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IBasicFileAttributeView

<pre class='added' data-is-non-breaking="">
public interface IBasicFileAttributeView : Android.Runtime.IJavaObject, IAttributeView, IFileAttributeView, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IBasicFileAttributes ReadAttributes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTimes (FileTime lastModifiedTime, FileTime lastAccessTime, FileTime createTime);</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IBasicFileAttributes

<pre class='added' data-is-non-breaking="">
public interface IBasicFileAttributes : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsDirectory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOther { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsRegularFile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsSymbolicLink { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual FileTime CreationTime ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object FileKey ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileTime LastAccessTime ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileTime LastModifiedTime ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual long Size ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IDosFileAttributeView

<pre class='added' data-is-non-breaking="">
public interface IDosFileAttributeView : Android.Runtime.IJavaObject, IAttributeView, IBasicFileAttributeView, IFileAttributeView, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IBasicFileAttributes ReadAttributes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetArchive (bool value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetHidden (bool value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetReadOnly (bool value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSystem (bool value);</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IDosFileAttributes

<pre class='added' data-is-non-breaking="">
public interface IDosFileAttributes : Android.Runtime.IJavaObject, IBasicFileAttributes, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsArchive { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsHidden { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsSystem { get; }</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IFileAttribute

<pre class='added' data-is-non-breaking="">
public interface IFileAttribute : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object Value ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IFileAttributeView

<pre class='added' data-is-non-breaking="">
public interface IFileAttributeView : Android.Runtime.IJavaObject, IAttributeView, System.IDisposable {
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IFileOwnerAttributeView

<pre class='added' data-is-non-breaking="">
public interface IFileOwnerAttributeView : Android.Runtime.IJavaObject, IAttributeView, IFileAttributeView, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IUserPrincipal Owner { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IFileStoreAttributeView

<pre class='added' data-is-non-breaking="">
public interface IFileStoreAttributeView : Android.Runtime.IJavaObject, IAttributeView, System.IDisposable {
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IGroupPrincipal

<pre class='added' data-is-non-breaking="">
public interface IGroupPrincipal : Android.Runtime.IJavaObject, IUserPrincipal, Java.Security.IPrincipal, System.IDisposable {
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IPosixFileAttributeView

<pre class='added' data-is-non-breaking="">
public interface IPosixFileAttributeView : Android.Runtime.IJavaObject, IAttributeView, IBasicFileAttributeView, IFileAttributeView, IFileOwnerAttributeView, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IBasicFileAttributes ReadAttributes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetGroup (IGroupPrincipal group);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetPermissions (System.Collections.Generic.ICollection&lt;PosixFilePermission&gt; perms);</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IPosixFileAttributes

<pre class='added' data-is-non-breaking="">
public interface IPosixFileAttributes : Android.Runtime.IJavaObject, IBasicFileAttributes, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IGroupPrincipal Group ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUserPrincipal Owner ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.Generic.ICollection&lt;PosixFilePermission&gt; Permissions ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IUserDefinedFileAttributeView

<pre class='added' data-is-non-breaking="">
public interface IUserDefinedFileAttributeView : Android.Runtime.IJavaObject, IAttributeView, IFileAttributeView, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Delete (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.Generic.IList&lt;string&gt; List ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string Name ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Read (string name, Java.Nio.ByteBuffer dst);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Size (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Write (string name, Java.Nio.ByteBuffer src);</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.IUserPrincipal

<pre class='added' data-is-non-breaking="">
public interface IUserPrincipal : Android.Runtime.IJavaObject, Java.Security.IPrincipal, System.IDisposable {
}
</pre>



### New Type Java.Nio.FileNio.Attributes.PosixFilePermission

<pre class='added' data-is-non-breaking="">
public sealed class PosixFilePermission : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission GroupExecute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission GroupRead { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission GroupWrite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission OthersExecute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission OthersRead { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission OthersWrite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission OwnerExecute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission OwnerRead { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PosixFilePermission OwnerWrite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PosixFilePermission ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PosixFilePermission[] Values ();</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.PosixFilePermissions

<pre class='added' data-is-non-breaking="">
public sealed class PosixFilePermissions : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IFileAttribute AsFileAttribute (System.Collections.Generic.ICollection&lt;PosixFilePermission&gt; perms);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.ICollection&lt;PosixFilePermission&gt; FromString (string perms);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string ToString (System.Collections.Generic.ICollection&lt;PosixFilePermission&gt; perms);</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.UserPrincipalLookupService

<pre class='added' data-is-non-breaking="">
public abstract class UserPrincipalLookupService : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UserPrincipalLookupService ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UserPrincipalLookupService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IGroupPrincipal LookupPrincipalByGroupName (string group);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUserPrincipal LookupPrincipalByName (string name);</span>
}
</pre>



### New Type Java.Nio.FileNio.Attributes.UserPrincipalNotFoundException

<pre class='added' data-is-non-breaking="">
public class UserPrincipalNotFoundException : Java.IO.IOException, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UserPrincipalNotFoundException (string name);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UserPrincipalNotFoundException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>





## New Namespace Java.Nio.FileNio.Spi

### New Type Java.Nio.FileNio.Spi.FileSystemProvider

<pre class='added' data-is-non-breaking="">
public abstract class FileSystemProvider : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected FileSystemProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileSystemProvider (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Scheme { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CheckAccess (Java.Nio.FileNio.IPath path, Java.Nio.FileNio.AccessMode[] modes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Copy (Java.Nio.FileNio.IPath source, Java.Nio.FileNio.IPath target, Java.Nio.FileNio.ICopyOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CreateDirectory (Java.Nio.FileNio.IPath dir, Java.Nio.FileNio.Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CreateLink (Java.Nio.FileNio.IPath link, Java.Nio.FileNio.IPath existing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CreateSymbolicLink (Java.Nio.FileNio.IPath link, Java.Nio.FileNio.IPath target, Java.Nio.FileNio.Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Delete (Java.Nio.FileNio.IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DeleteIfExists (Java.Nio.FileNio.IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object GetFileAttributeView (Java.Nio.FileNio.IPath path, Java.Lang.Class type, Java.Nio.FileNio.LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.FileNio.FileStore GetFileStore (Java.Nio.FileNio.IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.FileNio.FileSystem GetFileSystem (Java.Net.URI uri);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.FileNio.IPath GetPath (Java.Net.URI uri);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IList&lt;FileSystemProvider&gt; InstalledProviders ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsHidden (Java.Nio.FileNio.IPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsSameFile (Java.Nio.FileNio.IPath path, Java.Nio.FileNio.IPath path2);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Move (Java.Nio.FileNio.IPath source, Java.Nio.FileNio.IPath target, Java.Nio.FileNio.ICopyOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.Channels.AsynchronousFileChannel NewAsynchronousFileChannel (Java.Nio.FileNio.IPath path, System.Collections.Generic.ICollection&lt;Java.Nio.FileNio.IOpenOption&gt; options, Java.Util.Concurrent.IExecutorService executor, Java.Nio.FileNio.Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.Channels.ISeekableByteChannel NewByteChannel (Java.Nio.FileNio.IPath path, System.Collections.Generic.ICollection&lt;Java.Nio.FileNio.IOpenOption&gt; options, Java.Nio.FileNio.Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.FileNio.IDirectoryStream NewDirectoryStream (Java.Nio.FileNio.IPath dir, Java.Nio.FileNio.IDirectoryStreamFilter filter);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.Channels.FileChannel NewFileChannel (Java.Nio.FileNio.IPath path, System.Collections.Generic.ICollection&lt;Java.Nio.FileNio.IOpenOption&gt; options, Java.Nio.FileNio.Attributes.IFileAttribute[] attrs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.FileNio.FileSystem NewFileSystem (Java.Net.URI uri, System.Collections.Generic.IDictionary&lt;System.String,System.Object&gt; env);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.FileNio.FileSystem NewFileSystem (Java.Nio.FileNio.IPath path, System.Collections.Generic.IDictionary&lt;System.String,System.Object&gt; env);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IO.Stream NewInputStream (Java.Nio.FileNio.IPath path, Java.Nio.FileNio.IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IO.Stream NewOutputStream (Java.Nio.FileNio.IPath path, Java.Nio.FileNio.IOpenOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Lang.Object ReadAttributes (Java.Nio.FileNio.IPath path, Java.Lang.Class type, Java.Nio.FileNio.LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.Generic.IDictionary&lt;System.String,Java.Lang.Object&gt; ReadAttributes (Java.Nio.FileNio.IPath path, string attributes, Java.Nio.FileNio.LinkOption[] options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Java.Nio.FileNio.IPath ReadSymbolicLink (Java.Nio.FileNio.IPath link);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAttribute (Java.Nio.FileNio.IPath path, string attribute, Java.Lang.Object value, Java.Nio.FileNio.LinkOption[] options);</span>
}
</pre>



### New Type Java.Nio.FileNio.Spi.FileTypeDetector

<pre class='added' data-is-non-breaking="">
public abstract class FileTypeDetector : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected FileTypeDetector ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FileTypeDetector (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string ProbeContentType (Java.Nio.FileNio.IPath path);</span>
}
</pre>





## New Namespace Java.Time.Format

### New Type Java.Time.Format.DateTimeFormatter

<pre class='added' data-is-non-breaking="">
public sealed class DateTimeFormatter : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter BasicIsoDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public DecimalStyle DecimalStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoDateTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoInstant { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoLocalDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoLocalDateTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoLocalTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoOffsetDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoOffsetDateTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoOffsetTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoOrdinalDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoWeekDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter IsoZonedDateTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Java.Util.Locale Locale { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ResolverStyle ResolverStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DateTimeFormatter Rfc1123DateTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static DateTimeFormatter OfLocalizedDate (FormatStyle dateStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static DateTimeFormatter OfLocalizedDateTime (FormatStyle dateTimeStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static DateTimeFormatter OfLocalizedDateTime (FormatStyle dateStyle, FormatStyle timeStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static DateTimeFormatter OfLocalizedTime (FormatStyle timeStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static DateTimeFormatter OfPattern (string pattern);</span>
	<span class='added added-method ' data-is-non-breaking="">public static DateTimeFormatter OfPattern (string pattern, Java.Util.Locale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public Java.Text._Format ToFormat ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatter WithDecimalStyle (DecimalStyle decimalStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatter WithLocale (Java.Util.Locale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatter WithResolverStyle (ResolverStyle resolverStyle);</span>
}
</pre>



### New Type Java.Time.Format.DateTimeFormatterBuilder

<pre class='added' data-is-non-breaking="">
public sealed class DateTimeFormatterBuilder : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DateTimeFormatterBuilder ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder Append (DateTimeFormatter formatter);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendChronologyId ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendChronologyText (TextStyle textStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendInstant ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendInstant (int fractionalDigits);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendLiteral (char literal);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendLiteral (string literal);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendLocalized (FormatStyle dateStyle, FormatStyle timeStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendLocalizedOffset (TextStyle style);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendOffset (string pattern, string noOffsetText);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendOffsetId ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendOptional (DateTimeFormatter formatter);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendPattern (string pattern);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendZoneId ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendZoneOrOffsetId ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendZoneRegionId ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder AppendZoneText (TextStyle textStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder OptionalEnd ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder OptionalStart ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder PadNext (int padWidth);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder PadNext (int padWidth, char padChar);</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder ParseCaseInsensitive ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder ParseCaseSensitive ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder ParseLenient ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatterBuilder ParseStrict ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatter ToFormatter ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DateTimeFormatter ToFormatter (Java.Util.Locale locale);</span>
}
</pre>



### New Type Java.Time.Format.DecimalStyle

<pre class='added' data-is-non-breaking="">
public sealed class DecimalStyle : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static System.Collections.Generic.ICollection&lt;Java.Util.Locale&gt; AvailableLocales { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public char DecimalSeparator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public char NegativeSign { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public char PositiveSign { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DecimalStyle Standard { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public char ZeroDigit { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static DecimalStyle Of (Java.Util.Locale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static DecimalStyle OfDefaultLocale ();</span>
	<span class='added added-method ' data-is-non-breaking="">public DecimalStyle WithDecimalSeparator (char decimalSeparator);</span>
	<span class='added added-method ' data-is-non-breaking="">public DecimalStyle WithNegativeSign (char negativeSign);</span>
	<span class='added added-method ' data-is-non-breaking="">public DecimalStyle WithPositiveSign (char positiveSign);</span>
	<span class='added added-method ' data-is-non-breaking="">public DecimalStyle WithZeroDigit (char zeroDigit);</span>
}
</pre>



### New Type Java.Time.Format.FormatStyle

<pre class='added' data-is-non-breaking="">
public sealed class FormatStyle : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static FormatStyle Full { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static FormatStyle Long { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static FormatStyle Medium { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static FormatStyle Short { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static FormatStyle ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static FormatStyle[] Values ();</span>
}
</pre>



### New Type Java.Time.Format.ResolverStyle

<pre class='added' data-is-non-breaking="">
public sealed class ResolverStyle : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ResolverStyle Lenient { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ResolverStyle Smart { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ResolverStyle Strict { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static ResolverStyle ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ResolverStyle[] Values ();</span>
}
</pre>



### New Type Java.Time.Format.SignStyle

<pre class='added' data-is-non-breaking="">
public sealed class SignStyle : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static SignStyle Always { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SignStyle ExceedsPad { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SignStyle Never { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SignStyle Normal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SignStyle NotNegative { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SignStyle ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignStyle[] Values ();</span>
}
</pre>



### New Type Java.Time.Format.TextStyle

<pre class='added' data-is-non-breaking="">
public sealed class TextStyle : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static TextStyle Full { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static TextStyle FullStandalone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsStandalone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static TextStyle Narrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static TextStyle NarrowStandalone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static TextStyle Short { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static TextStyle ShortStandalone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public TextStyle AsNormal ();</span>
	<span class='added added-method ' data-is-non-breaking="">public TextStyle AsStandalone ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static TextStyle ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TextStyle[] Values ();</span>
}
</pre>





## New Namespace Java.Time.Temporal

### New Type Java.Time.Temporal.ChronoField

<pre class='added' data-is-non-breaking="">
public sealed class ChronoField : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField AlignedDayOfWeekInMonth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField AlignedDayOfWeekInYear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField AlignedWeekOfMonth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField AlignedWeekOfYear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField AmpmOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField ClockHourOfAmpm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField ClockHourOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField DayOfMonth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField DayOfWeek { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField DayOfYear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField EpochDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField Era { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField HourOfAmpm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField HourOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField InstantSeconds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsDateBased { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsTimeBased { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField MicroOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField MicroOfSecond { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField MilliOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField MilliOfSecond { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField MinuteOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField MinuteOfHour { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField MonthOfYear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField NanoOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField NanoOfSecond { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField OffsetSeconds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField ProlepticMonth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField SecondOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField SecondOfMinute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField Year { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoField YearOfEra { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Object AdjustInto (Java.Lang.Object temporal, long newValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public int CheckValidIntValue (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public long CheckValidValue (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public string GetDisplayName (Java.Util.Locale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public ValueRange Range ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static ChronoField ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ChronoField[] Values ();</span>
}
</pre>



### New Type Java.Time.Temporal.ChronoUnit

<pre class='added' data-is-non-breaking="">
public sealed class ChronoUnit : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Centuries { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Days { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Decades { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Eras { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Forever { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit HalfDays { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Hours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsDateBased { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsDurationEstimated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsTimeBased { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Micros { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Millennia { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Millis { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Minutes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Months { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Nanos { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Seconds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Weeks { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ChronoUnit Years { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public Java.Lang.Object AddTo (Java.Lang.Object temporal, long amount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ChronoUnit ValueOf (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ChronoUnit[] Values ();</span>
}
</pre>



### New Type Java.Time.Temporal.IsoFields

<pre class='added' data-is-non-breaking="">
public sealed class IsoFields : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Time.Temporal.JulianFields

<pre class='added' data-is-non-breaking="">
public sealed class JulianFields : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Time.Temporal.TemporalAdjusters

<pre class='added' data-is-non-breaking="">
public sealed class TemporalAdjusters : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Time.Temporal.TemporalQueries

<pre class='added' data-is-non-breaking="">
public sealed class TemporalQueries : Java.Lang.Object, Android.Runtime.IJavaObject, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
}
</pre>



### New Type Java.Time.Temporal.ValueRange

<pre class='added' data-is-non-breaking="">
public sealed class ValueRange : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsFixed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsIntValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long LargestMinimum { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long Maximum { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long Minimum { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long SmallestMaximum { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public bool IsValidIntValue (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool IsValidValue (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ValueRange Of (long min, long max);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ValueRange Of (long min, long maxSmallest, long maxLargest);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ValueRange Of (long minSmallest, long minLargest, long maxSmallest, long maxLargest);</span>
}
</pre>



### New Type Java.Time.Temporal.WeekFields

<pre class='added' data-is-non-breaking="">
public sealed class WeekFields : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static WeekFields Iso { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MinimalDaysInFirstWeek { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static WeekFields SundayStart { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static WeekFields Of (Java.Util.Locale locale);</span>
}
</pre>





## New Namespace Java.Time.Zone

### New Type Java.Time.Zone.ZoneOffsetTransition

<pre class='added' data-is-non-breaking="">
public sealed class ZoneOffsetTransition : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsGap { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsOverlap { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public int CompareTo (ZoneOffsetTransition transition);</span>
	<span class='added added-method ' data-is-non-breaking="">public long ToEpochSecond ();</span>
}
</pre>



### New Type Java.Time.Zone.ZoneOffsetTransitionRule

<pre class='added' data-is-non-breaking="">
public sealed class ZoneOffsetTransitionRule : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int DayOfMonthIndicator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsMidnightEndOfDay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public ZoneOffsetTransition CreateTransition (int year);</span>
	<span class='added added-method ' data-is-non-breaking="">public ZoneOffsetTransitionRule.TimeDefinition GetTimeDefinition ();</span>

	// inner types
	public sealed class TimeDefinition : Java.Lang.Enum, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, Java.Lang.IComparable, System.IDisposable {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ZoneOffsetTransitionRule.TimeDefinition Standard { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ZoneOffsetTransitionRule.TimeDefinition Utc { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ZoneOffsetTransitionRule.TimeDefinition Wall { get; }</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static ZoneOffsetTransitionRule.TimeDefinition ValueOf (string name);</span>
		<span class='added added-method ' data-is-non-breaking="">public static ZoneOffsetTransitionRule.TimeDefinition[] Values ();</span>
	}
}
</pre>



### New Type Java.Time.Zone.ZoneRules

<pre class='added' data-is-non-breaking="">
public sealed class ZoneRules : Java.Lang.Object, Android.Runtime.IJavaObject, Java.IO.ISerializable, Java.Interop.IJavaPeerable, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsFixedOffset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Java.Interop.JniPeerMembers JniPeerMembers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override IntPtr ThresholdClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.Type ThresholdType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;ZoneOffsetTransitionRule&gt; TransitionRules { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;ZoneOffsetTransition&gt; Transitions { get; }</span>
}
</pre>
