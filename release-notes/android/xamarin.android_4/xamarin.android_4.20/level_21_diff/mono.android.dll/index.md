---
id: F94783C3-B750-45F7-ADBE-410032A50CB7
---

## Namespace Android

### Type Changed: Android.Manifest

### Type Changed: Android.Manifest.Permission

Added fields:

```
public static const string BindDreamService = "android.permission.BIND_DREAM_SERVICE";
	public static const string BindTvInput = "android.permission.BIND_TV_INPUT";
	public static const string BindVoiceInteraction = "android.permission.BIND_VOICE_INTERACTION";
	public static const string ReadVoicemail = "com.android.voicemail.permission.READ_VOICEMAIL";
	public static const string WriteVoicemail = "com.android.voicemail.permission.WRITE_VOICEMAIL";
```

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string GetTasks = "android.permission.GET_TASKS";

	[Obsolete ("deprecated")]
	public static const string ReadSocialStream = "android.permission.READ_SOCIAL_STREAM";

	[Obsolete ("deprecated")]
	public static const string WriteSocialStream = "android.permission.WRITE_SOCIAL_STREAM";
```

### Type Changed: Android.Resource

### Type Changed: Android.Resource.Attribute

Added fields:

```
public static const int ActionBarPopupTheme;
	public static const int ActionBarTheme;
	public static const int ActionModeFindDrawable;
	public static const int ActionModeShareDrawable;
	public static const int ActionModeWebSearchDrawable;
	public static const int ActionOverflowMenuStyle;
	public static const int AmbientShadowAlpha;
	public static const int AmPmBackgroundColor;
	public static const int AmPmTextColor;
	public static const int AutoRemoveFromRecents;
	public static const int BackgroundTint;
	public static const int BackgroundTintMode;
	public static const int Banner;
	public static const int ButtonBarNegativeButtonStyle;
	public static const int ButtonBarNeutralButtonStyle;
	public static const int ButtonBarPositiveButtonStyle;
	public static const int ButtonTint;
	public static const int ButtonTintMode;
	public static const int CalendarTextColor;
	public static const int CheckMarkTint;
	public static const int CheckMarkTintMode;
	public static const int CloseIcon;
	public static const int ColorAccent;
	public static const int ColorButtonNormal;
	public static const int ColorControlActivated;
	public static const int ColorControlHighlight;
	public static const int ColorControlNormal;
	public static const int ColorEdgeEffect;
	public static const int ColorPrimary;
	public static const int ColorPrimaryDark;
	public static const int CommitIcon;
	public static const int ContentAgeHint;
	public static const int ContentInsetEnd;
	public static const int ContentInsetLeft;
	public static const int ContentInsetRight;
	public static const int ContentInsetStart;
	public static const int ControlX1;
	public static const int ControlX2;
	public static const int ControlY1;
	public static const int ControlY2;
	public static const int Country;
	public static const int DatePickerDialogTheme;
	public static const int DatePickerMode;
	public static const int DayOfWeekBackground;
	public static const int DayOfWeekTextAppearance;
	public static const int DocumentLaunchMode;
	public static const int ElegantTextHeight;
	public static const int Elevation;
	public static const int ExcludeClass;
	public static const int ExcludeId;
	public static const int ExcludeName;
	public static const int FastScrollStyle;
	public static const int FillAlpha;
	public static const int FillColor;
	public static const int FontFeatureSettings;
	public static const int ForegroundTint;
	public static const int ForegroundTintMode;
	public static const int FragmentAllowEnterTransitionOverlap;
	public static const int FragmentAllowReturnTransitionOverlap;
	public static const int FragmentEnterTransition;
	public static const int FragmentExitTransition;
	public static const int FragmentReenterTransition;
	public static const int FragmentReturnTransition;
	public static const int FragmentSharedElementEnterTransition;
	public static const int FragmentSharedElementReturnTransition;
	public static const int FromId;
	public static const int FullBackupOnly;
	public static const int GoIcon;
	public static const int HeaderAmPmTextAppearance;
	public static const int HeaderDayOfMonthTextAppearance;
	public static const int HeaderMonthTextAppearance;
	public static const int HeaderTimeTextAppearance;
	public static const int HeaderYearTextAppearance;
	public static const int HideOnContentScroll;
	public static const int IndeterminateTint;
	public static const int IndeterminateTintMode;
	public static const int Inset;
	public static const int IsGame;
	public static const int LaunchTaskBehindSourceAnimation;
	public static const int LaunchTaskBehindTargetAnimation;
	public static const int LayoutColumnWeight;
	public static const int LayoutRowWeight;
	public static const int LetterSpacing;
	public static const int MatchOrder;
	public static const int MaximumAngle;
	public static const int MaxRecents;
	public static const int MinimumHorizontalAngle;
	public static const int MinimumVerticalAngle;
	public static const int MultiArch;
	public static const int NavigationBarColor;
	public static const int NavigationContentDescription;
	public static const int NavigationIcon;
	public static const int NestedScrollingEnabled;
	public static const int NumbersBackgroundColor;
	public static const int NumbersSelectorColor;
	public static const int NumbersTextColor;
	public static const int OutlineProvider;
	public static const int OverlapAnchor;
	public static const int PaddingMode;
	public static const int PathData;
	public static const int PatternPathData;
	public static const int PersistableMode;
	public static const int PopupElevation;
	public static const int PopupTheme;
	public static const int ProgressBackgroundTint;
	public static const int ProgressBackgroundTintMode;
	public static const int ProgressTint;
	public static const int ProgressTintMode;
	public static const int PropertyXName;
	public static const int PropertyYName;
	public static const int QueryBackground;
	public static const int RecognitionService;
	public static const int RelinquishTaskIdentity;
	public static const int Reparent;
	public static const int ReparentWithOverlay;
	public static const int RestrictionType;
	public static const int ResumeWhilePausing;
	public static const int Reversible;
	public static const int SearchIcon;
	public static const int SearchViewStyle;
	public static const int SecondaryProgressTint;
	public static const int SecondaryProgressTintMode;
	public static const int SelectableItemBackgroundBorderless;
	public static const int SessionService;
	public static const int SetupActivity;
	public static const int ShowText;
	public static const int SlideEdge;
	public static const int SplitTrack;
	public static const int SpotShadowAlpha;
	public static const int StackViewStyle;
	public static const int StateListAnimator;
	public static const int StatusBarColor;
	public static const int StrokeAlpha;
	public static const int StrokeColor;
	public static const int StrokeLineCap;
	public static const int StrokeLineJoin;
	public static const int StrokeMiterLimit;
	public static const int StrokeWidth;
	public static const int SubmitBackground;
	public static const int SubtitleTextAppearance;
	public static const int SuggestionRowLayout;
	public static const int SwitchStyle;
	public static const int TargetName;
	public static const int TextAppearanceListItemSecondary;
	public static const int ThumbTint;
	public static const int ThumbTintMode;
	public static const int TileModeX;
	public static const int TileModeY;
	public static const int TimePickerDialogTheme;
	public static const int TimePickerMode;
	public static const int TimePickerStyle;
	public static const int TintMode;
	public static const int TitleTextAppearance;
	public static const int ToId;
	public static const int ToolbarStyle;
	public static const int TouchscreenBlocksFocus;
	public static const int TransitionGroup;
	public static const int TransitionName;
	public static const int TransitionVisibilityMode;
	public static const int TranslateX;
	public static const int TranslateY;
	public static const int TranslationZ;
	public static const int TrimPathEnd;
	public static const int TrimPathOffset;
	public static const int TrimPathStart;
	public static const int ViewportHeight;
	public static const int ViewportWidth;
	public static const int VoiceIcon;
	public static const int WindowActivityTransitions;
	public static const int WindowAllowEnterTransitionOverlap;
	public static const int WindowAllowReturnTransitionOverlap;
	public static const int WindowClipToOutline;
	public static const int WindowContentTransitionManager;
	public static const int WindowContentTransitions;
	public static const int WindowDrawsSystemBarBackgrounds;
	public static const int WindowElevation;
	public static const int WindowEnterTransition;
	public static const int WindowExitTransition;
	public static const int WindowReenterTransition;
	public static const int WindowReturnTransition;
	public static const int WindowSharedElementEnterTransition;
	public static const int WindowSharedElementExitTransition;
	public static const int WindowSharedElementReenterTransition;
	public static const int WindowSharedElementReturnTransition;
	public static const int WindowSharedElementsUseOverlay;
	public static const int WindowTransitionBackgroundFadeDuration;
	public static const int YearListItemTextAppearance;
	public static const int YearListSelectorColor;
```

### Type Changed: Android.Resource.Id

Added fields:

```
public static const int Mask;
	public static const int NavigationBarBackground;
	public static const int StatusBarBackground;
```

### Type Changed: Android.Resource.Interpolator

Added fields:

```
public static const int FastOutLinearIn;
	public static const int FastOutSlowIn;
	public static const int LinearOutSlowIn;
```

### Type Changed: Android.Resource.Style

Added fields:

```
public static const int TextAppearanceMaterial;
	public static const int TextAppearanceMaterialBody1;
	public static const int TextAppearanceMaterialBody2;
	public static const int TextAppearanceMaterialButton;
	public static const int TextAppearanceMaterialCaption;
	public static const int TextAppearanceMaterialDialogWindowTitle;
	public static const int TextAppearanceMaterialDisplay1;
	public static const int TextAppearanceMaterialDisplay2;
	public static const int TextAppearanceMaterialDisplay3;
	public static const int TextAppearanceMaterialDisplay4;
	public static const int TextAppearanceMaterialHeadline;
	public static const int TextAppearanceMaterialInverse;
	public static const int TextAppearanceMaterialLarge;
	public static const int TextAppearanceMaterialLargeInverse;
	public static const int TextAppearanceMaterialMedium;
	public static const int TextAppearanceMaterialMediumInverse;
	public static const int TextAppearanceMaterialMenu;
	public static const int TextAppearanceMaterialNotification;
	public static const int TextAppearanceMaterialNotificationEmphasis;
	public static const int TextAppearanceMaterialNotificationInfo;
	public static const int TextAppearanceMaterialNotificationLine2;
	public static const int TextAppearanceMaterialNotificationTime;
	public static const int TextAppearanceMaterialNotificationTitle;
	public static const int TextAppearanceMaterialSearchResultSubtitle;
	public static const int TextAppearanceMaterialSearchResultTitle;
	public static const int TextAppearanceMaterialSmall;
	public static const int TextAppearanceMaterialSmallInverse;
	public static const int TextAppearanceMaterialSubhead;
	public static const int TextAppearanceMaterialTitle;
	public static const int TextAppearanceMaterialWidget;
	public static const int TextAppearanceMaterialWidgetActionBarMenu;
	public static const int TextAppearanceMaterialWidgetActionBarSubtitle;
	public static const int TextAppearanceMaterialWidgetActionBarSubtitleInverse;
	public static const int TextAppearanceMaterialWidgetActionBarTitle;
	public static const int TextAppearanceMaterialWidgetActionBarTitleInverse;
	public static const int TextAppearanceMaterialWidgetActionModeSubtitle;
	public static const int TextAppearanceMaterialWidgetActionModeSubtitleInverse;
	public static const int TextAppearanceMaterialWidgetActionModeTitle;
	public static const int TextAppearanceMaterialWidgetActionModeTitleInverse;
	public static const int TextAppearanceMaterialWidgetButton;
	public static const int TextAppearanceMaterialWidgetDropDownHint;
	public static const int TextAppearanceMaterialWidgetDropDownItem;
	public static const int TextAppearanceMaterialWidgetEditText;
	public static const int TextAppearanceMaterialWidgetIconMenuItem;
	public static const int TextAppearanceMaterialWidgetPopupMenu;
	public static const int TextAppearanceMaterialWidgetPopupMenuLarge;
	public static const int TextAppearanceMaterialWidgetPopupMenuSmall;
	public static const int TextAppearanceMaterialWidgetTabWidget;
	public static const int TextAppearanceMaterialWidgetTextView;
	public static const int TextAppearanceMaterialWidgetTextViewPopupMenu;
	public static const int TextAppearanceMaterialWidgetTextViewSpinnerItem;
	public static const int TextAppearanceMaterialWidgetToolbarSubtitle;
	public static const int TextAppearanceMaterialWidgetToolbarTitle;
	public static const int TextAppearanceMaterialWindowTitle;
	public static const int ThemeDeviceDefaultSettings;
	public static const int ThemeMaterial;
	public static const int ThemeMaterialDialog;
	public static const int ThemeMaterialDialogAlert;
	public static const int ThemeMaterialDialogMinWidth;
	public static const int ThemeMaterialDialogNoActionBar;
	public static const int ThemeMaterialDialogNoActionBarMinWidth;
	public static const int ThemeMaterialDialogPresentation;
	public static const int ThemeMaterialDialogWhenLarge;
	public static const int ThemeMaterialDialogWhenLargeNoActionBar;
	public static const int ThemeMaterialInputMethod;
	public static const int ThemeMaterialLight;
	public static const int ThemeMaterialLightDarkActionBar;
	public static const int ThemeMaterialLightDialog;
	public static const int ThemeMaterialLightDialogAlert;
	public static const int ThemeMaterialLightDialogMinWidth;
	public static const int ThemeMaterialLightDialogNoActionBar;
	public static const int ThemeMaterialLightDialogNoActionBarMinWidth;
	public static const int ThemeMaterialLightDialogPresentation;
	public static const int ThemeMaterialLightDialogWhenLarge;
	public static const int ThemeMaterialLightDialogWhenLargeNoActionBar;
	public static const int ThemeMaterialLightNoActionBar;
	public static const int ThemeMaterialLightNoActionBarFullscreen;
	public static const int ThemeMaterialLightNoActionBarOverscan;
	public static const int ThemeMaterialLightNoActionBarTranslucentDecor;
	public static const int ThemeMaterialLightPanel;
	public static const int ThemeMaterialLightVoice;
	public static const int ThemeMaterialNoActionBar;
	public static const int ThemeMaterialNoActionBarFullscreen;
	public static const int ThemeMaterialNoActionBarOverscan;
	public static const int ThemeMaterialNoActionBarTranslucentDecor;
	public static const int ThemeMaterialPanel;
	public static const int ThemeMaterialSettings;
	public static const int ThemeMaterialVoice;
	public static const int ThemeMaterialWallpaper;
	public static const int ThemeMaterialWallpaperNoTitleBar;
	public static const int ThemeOverlay;
	public static const int ThemeOverlayMaterial;
	public static const int ThemeOverlayMaterialActionBar;
	public static const int ThemeOverlayMaterialDark;
	public static const int ThemeOverlayMaterialDarkActionBar;
	public static const int ThemeOverlayMaterialLight;
	public static const int WidgetDeviceDefaultFastScroll;
	public static const int WidgetDeviceDefaultLightFastScroll;
	public static const int WidgetDeviceDefaultLightStackView;
	public static const int WidgetDeviceDefaultStackView;
	public static const int WidgetFastScroll;
	public static const int WidgetMaterial;
	public static const int WidgetMaterialActionBar;
	public static const int WidgetMaterialActionBarSolid;
	public static const int WidgetMaterialActionBarTabBar;
	public static const int WidgetMaterialActionBarTabText;
	public static const int WidgetMaterialActionBarTabView;
	public static const int WidgetMaterialActionButton;
	public static const int WidgetMaterialActionButtonCloseMode;
	public static const int WidgetMaterialActionButtonOverflow;
	public static const int WidgetMaterialActionMode;
	public static const int WidgetMaterialAutoCompleteTextView;
	public static const int WidgetMaterialButton;
	public static const int WidgetMaterialButtonBar;
	public static const int WidgetMaterialButtonBarAlertDialog;
	public static const int WidgetMaterialButtonBorderless;
	public static const int WidgetMaterialButtonBorderlessColored;
	public static const int WidgetMaterialButtonBorderlessSmall;
	public static const int WidgetMaterialButtonInset;
	public static const int WidgetMaterialButtonSmall;
	public static const int WidgetMaterialButtonToggle;
	public static const int WidgetMaterialCalendarView;
	public static const int WidgetMaterialCheckedTextView;
	public static const int WidgetMaterialCompoundButtonCheckBox;
	public static const int WidgetMaterialCompoundButtonRadioButton;
	public static const int WidgetMaterialCompoundButtonStar;
	public static const int WidgetMaterialDatePicker;
	public static const int WidgetMaterialDropDownItem;
	public static const int WidgetMaterialDropDownItemSpinner;
	public static const int WidgetMaterialEditText;
	public static const int WidgetMaterialExpandableListView;
	public static const int WidgetMaterialFastScroll;
	public static const int WidgetMaterialGridView;
	public static const int WidgetMaterialHorizontalScrollView;
	public static const int WidgetMaterialImageButton;
	public static const int WidgetMaterialLight;
	public static const int WidgetMaterialLightActionBar;
	public static const int WidgetMaterialLightActionBarSolid;
	public static const int WidgetMaterialLightActionBarTabBar;
	public static const int WidgetMaterialLightActionBarTabText;
	public static const int WidgetMaterialLightActionBarTabView;
	public static const int WidgetMaterialLightActionButton;
	public static const int WidgetMaterialLightActionButtonCloseMode;
	public static const int WidgetMaterialLightActionButtonOverflow;
	public static const int WidgetMaterialLightActionMode;
	public static const int WidgetMaterialLightAutoCompleteTextView;
	public static const int WidgetMaterialLightButton;
	public static const int WidgetMaterialLightButtonBar;
	public static const int WidgetMaterialLightButtonBarAlertDialog;
	public static const int WidgetMaterialLightButtonBorderless;
	public static const int WidgetMaterialLightButtonBorderlessColored;
	public static const int WidgetMaterialLightButtonBorderlessSmall;
	public static const int WidgetMaterialLightButtonInset;
	public static const int WidgetMaterialLightButtonSmall;
	public static const int WidgetMaterialLightButtonToggle;
	public static const int WidgetMaterialLightCalendarView;
	public static const int WidgetMaterialLightCheckedTextView;
	public static const int WidgetMaterialLightCompoundButtonCheckBox;
	public static const int WidgetMaterialLightCompoundButtonRadioButton;
	public static const int WidgetMaterialLightCompoundButtonStar;
	public static const int WidgetMaterialLightDatePicker;
	public static const int WidgetMaterialLightDropDownItem;
	public static const int WidgetMaterialLightDropDownItemSpinner;
	public static const int WidgetMaterialLightEditText;
	public static const int WidgetMaterialLightExpandableListView;
	public static const int WidgetMaterialLightFastScroll;
	public static const int WidgetMaterialLightGridView;
	public static const int WidgetMaterialLightHorizontalScrollView;
	public static const int WidgetMaterialLightImageButton;
	public static const int WidgetMaterialLightListPopupWindow;
	public static const int WidgetMaterialLightListView;
	public static const int WidgetMaterialLightListViewDropDown;
	public static const int WidgetMaterialLightMediaRouteButton;
	public static const int WidgetMaterialLightPopupMenu;
	public static const int WidgetMaterialLightPopupMenuOverflow;
	public static const int WidgetMaterialLightPopupWindow;
	public static const int WidgetMaterialLightProgressBar;
	public static const int WidgetMaterialLightProgressBarHorizontal;
	public static const int WidgetMaterialLightProgressBarInverse;
	public static const int WidgetMaterialLightProgressBarLarge;
	public static const int WidgetMaterialLightProgressBarLargeInverse;
	public static const int WidgetMaterialLightProgressBarSmall;
	public static const int WidgetMaterialLightProgressBarSmallInverse;
	public static const int WidgetMaterialLightProgressBarSmallTitle;
	public static const int WidgetMaterialLightRatingBar;
	public static const int WidgetMaterialLightRatingBarIndicator;
	public static const int WidgetMaterialLightRatingBarSmall;
	public static const int WidgetMaterialLightScrollView;
	public static const int WidgetMaterialLightSearchView;
	public static const int WidgetMaterialLightSeekBar;
	public static const int WidgetMaterialLightSegmentedButton;
	public static const int WidgetMaterialLightSpinner;
	public static const int WidgetMaterialLightSpinnerUnderlined;
	public static const int WidgetMaterialLightStackView;
	public static const int WidgetMaterialLightTab;
	public static const int WidgetMaterialLightTabWidget;
	public static const int WidgetMaterialLightTextView;
	public static const int WidgetMaterialLightTextViewSpinnerItem;
	public static const int WidgetMaterialLightTimePicker;
	public static const int WidgetMaterialLightWebTextView;
	public static const int WidgetMaterialLightWebView;
	public static const int WidgetMaterialListPopupWindow;
	public static const int WidgetMaterialListView;
	public static const int WidgetMaterialListViewDropDown;
	public static const int WidgetMaterialMediaRouteButton;
	public static const int WidgetMaterialPopupMenu;
	public static const int WidgetMaterialPopupMenuOverflow;
	public static const int WidgetMaterialPopupWindow;
	public static const int WidgetMaterialProgressBar;
	public static const int WidgetMaterialProgressBarHorizontal;
	public static const int WidgetMaterialProgressBarLarge;
	public static const int WidgetMaterialProgressBarSmall;
	public static const int WidgetMaterialProgressBarSmallTitle;
	public static const int WidgetMaterialRatingBar;
	public static const int WidgetMaterialRatingBarIndicator;
	public static const int WidgetMaterialRatingBarSmall;
	public static const int WidgetMaterialScrollView;
	public static const int WidgetMaterialSearchView;
	public static const int WidgetMaterialSeekBar;
	public static const int WidgetMaterialSegmentedButton;
	public static const int WidgetMaterialSpinner;
	public static const int WidgetMaterialSpinnerUnderlined;
	public static const int WidgetMaterialStackView;
	public static const int WidgetMaterialTab;
	public static const int WidgetMaterialTabWidget;
	public static const int WidgetMaterialTextView;
	public static const int WidgetMaterialTextViewSpinnerItem;
	public static const int WidgetMaterialTimePicker;
	public static const int WidgetMaterialToolbar;
	public static const int WidgetMaterialToolbarButtonNavigation;
	public static const int WidgetMaterialWebTextView;
	public static const int WidgetMaterialWebView;
	public static const int WidgetStackView;
	public static const int WidgetToolbar;
	public static const int WidgetToolbarButtonNavigation;
```

### New Type Android.Transition

```
public sealed class Transition : Java.Lang.Object, System.IDisposable, Runtime.IJavaObject {
	// constructors
	public Resource ();
	// fields
	public static const int Explode;
	public static const int Fade;
	public static const int Move;
	public static const int NoTransition;
	public static const int SlideBottom;
	public static const int SlideLeft;
	public static const int SlideRight;
	public static const int SlideTop;
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityService

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.AccessibilityServices.GlobalAction enum directly instead of this field.")]
	public static const GlobalAction GlobalActionPowerDialog;
```

Added property:

```
public virtual System.Collections.Generic.IList<Android.Views.Accessibility.AccessibilityWindowInfo> Windows { get; }
```

Added method:

```
public virtual Android.Views.Accessibility.AccessibilityNodeInfo FindFocus (Android.Views.Accessibility.NodeFocus focus);
```

### Type Changed: Android.AccessibilityServices.AccessibilityServiceFlags

Added value:

```
RetrieveInteractiveWindows = 64,
```

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.AccessibilityServices.AccessibilityServiceFlags enum directly instead of this field.")]
	public static const AccessibilityServiceFlags FlagRetrieveInteractiveWindows;
```

### Type Changed: Android.AccessibilityServices.GlobalAction

Added value:

```
PowerDialog = 6,
```

## Namespace Android.Accounts

### Type Changed: Android.Accounts.AccountManager

Added methods:

```
public virtual string GetPreviousName (Account account);
	public virtual IAccountManagerFuture RenameAccount (Account account, string newName, IAccountManagerCallback callback, Android.OS.Handler handler);
```

## Namespace Android.Animation

### Type Changed: Android.Animation.AnimatorInflater

Added method:

```
public static StateListAnimator LoadStateListAnimator (Android.Content.Context context, int id);
```

### Type Changed: Android.Animation.ObjectAnimator

Added methods:

```
public static ObjectAnimator OfArgb (Java.Lang.Object target, string propertyName, int[] values);
	public static ObjectAnimator OfArgb (Java.Lang.Object target, Android.Util.Property property, int[] values);
	public static ObjectAnimator OfFloat (Java.Lang.Object target, Android.Util.Property xProperty, Android.Util.Property yProperty, Android.Graphics.Path path);
	public static ObjectAnimator OfFloat (Java.Lang.Object target, string xPropertyName, string yPropertyName, Android.Graphics.Path path);
	public static ObjectAnimator OfInt (Java.Lang.Object target, Android.Util.Property xProperty, Android.Util.Property yProperty, Android.Graphics.Path path);
	public static ObjectAnimator OfInt (Java.Lang.Object target, string xPropertyName, string yPropertyName, Android.Graphics.Path path);
	public static ObjectAnimator OfMultiFloat (Java.Lang.Object target, string propertyName, float[][] values);
	public static ObjectAnimator OfMultiFloat (Java.Lang.Object target, string propertyName, Android.Graphics.Path path);
	public static ObjectAnimator OfMultiFloat (Java.Lang.Object target, string propertyName, TypeConverter converter, ITypeEvaluator evaluator, Java.Lang.Object[] values);
	public static ObjectAnimator OfMultiInt (Java.Lang.Object target, string propertyName, int[][] values);
	public static ObjectAnimator OfMultiInt (Java.Lang.Object target, string propertyName, Android.Graphics.Path path);
	public static ObjectAnimator OfMultiInt (Java.Lang.Object target, string propertyName, TypeConverter converter, ITypeEvaluator evaluator, Java.Lang.Object[] values);
	public static ObjectAnimator OfObject (Java.Lang.Object target, Android.Util.Property property, TypeConverter converter, Android.Graphics.Path path);
	public static ObjectAnimator OfObject (Java.Lang.Object target, Android.Util.Property property, TypeConverter converter, ITypeEvaluator evaluator, Java.Lang.Object[] values);
	public static ObjectAnimator OfObject (Java.Lang.Object target, string propertyName, TypeConverter converter, Android.Graphics.Path path);
```

### Type Changed: Android.Animation.PropertyValuesHolder

Added methods:

```
public static PropertyValuesHolder OfMultiFloat (string propertyName, float[][] values);
	public static PropertyValuesHolder OfMultiFloat (string propertyName, Android.Graphics.Path path);
	public static PropertyValuesHolder OfMultiFloat (string propertyName, TypeConverter converter, ITypeEvaluator evaluator, Java.Lang.Object[] values);
	public static PropertyValuesHolder OfMultiFloat (string propertyName, TypeConverter converter, ITypeEvaluator evaluator, Keyframe[] values);
	public static PropertyValuesHolder OfMultiInt (string propertyName, int[][] values);
	public static PropertyValuesHolder OfMultiInt (string propertyName, Android.Graphics.Path path);
	public static PropertyValuesHolder OfMultiInt (string propertyName, TypeConverter converter, ITypeEvaluator evaluator, Java.Lang.Object[] values);
	public static PropertyValuesHolder OfMultiInt (string propertyName, TypeConverter converter, ITypeEvaluator evaluator, Keyframe[] values);
	public static PropertyValuesHolder OfObject (string propertyName, TypeConverter converter, Android.Graphics.Path path);
	public static PropertyValuesHolder OfObject (Android.Util.Property property, TypeConverter converter, ITypeEvaluator evaluator, Java.Lang.Object[] values);
	public static PropertyValuesHolder OfObject (Android.Util.Property property, TypeConverter converter, Android.Graphics.Path path);
	public virtual void SetConverter (TypeConverter converter);
```

### Type Changed: Android.Animation.RectEvaluator

Added constructor:

```
public RectEvaluator (Android.Graphics.Rect reuseRect);
```

### Type Changed: Android.Animation.ValueAnimator

Added method:

```
public static ValueAnimator OfArgb (int[] values);
```

### New Type Android.Animation.BidirectionalTypeConverter

```
public abstract class BidirectionalTypeConverter : Android.Animation.TypeConverter, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected BidirectionalTypeConverter (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BidirectionalTypeConverter (Java.Lang.Class fromClass, Java.Lang.Class toClass);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Java.Lang.Object ConvertBack (Java.Lang.Object value);
	public virtual BidirectionalTypeConverter Invert ();
}
```

### New Type Android.Animation.FloatArrayEvaluator

```
public class FloatArrayEvaluator : Java.Lang.Object, ITypeEvaluator, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected FloatArrayEvaluator (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FloatArrayEvaluator ();
	public FloatArrayEvaluator (float[] reuseArray);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual float[] Evaluate (float fraction, float[] startValue, float[] endValue);
}
```

### New Type Android.Animation.IntArrayEvaluator

```
public class IntArrayEvaluator : Java.Lang.Object, ITypeEvaluator, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected IntArrayEvaluator (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public IntArrayEvaluator ();
	public IntArrayEvaluator (int[] reuseArray);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int[] Evaluate (float fraction, int[] startValue, int[] endValue);
}
```

### New Type Android.Animation.PointFEvaluator

```
public class PointFEvaluator : Java.Lang.Object, ITypeEvaluator, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected PointFEvaluator (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PointFEvaluator ();
	public PointFEvaluator (Android.Graphics.PointF reuse);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.Graphics.PointF Evaluate (float fraction, Android.Graphics.PointF startValue, Android.Graphics.PointF endValue);
}
```

### New Type Android.Animation.StateListAnimator

```
public class StateListAnimator : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected StateListAnimator (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StateListAnimator ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void AddState (int[] specs, Animator animator);
	public virtual void JumpToCurrentState ();
}
```

### New Type Android.Animation.TypeConverter

```
public abstract class TypeConverter : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected TypeConverter (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TypeConverter (Java.Lang.Class fromClass, Java.Lang.Class toClass);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Java.Lang.Object Convert (Java.Lang.Object value);
}
```

## Namespace Android.App

### Type Changed: Android.App.ActionBar

Added properties:

```
public virtual float Elevation { get; set; }
	public virtual int HideOffset { get; set; }
	public virtual bool HideOnContentScrollEnabled { get; set; }
```

### Type Changed: Android.App.Activity

Added properties:

```
public virtual Android.Transitions.Scene ContentScene { get; }
	public virtual Android.Transitions.TransitionManager ContentTransitionManager { get; set; }
	public Android.Media.Session.MediaController MediaController { get; set; }
```

Added methods:

```
public virtual void FinishAfterTransition ();
	public virtual void FinishAndRemoveTask ();
	public virtual void OnActivityReenter (int resultCode, Android.Content.Intent data);
	public virtual void OnCreate (Android.OS.Bundle savedInstanceState, Android.OS.PersistableBundle persistentState);
	public virtual void OnEnterAnimationComplete ();
	public virtual void OnPostCreate (Android.OS.Bundle savedInstanceState, Android.OS.PersistableBundle persistentState);
	public virtual void OnRestoreInstanceState (Android.OS.Bundle savedInstanceState, Android.OS.PersistableBundle persistentState);
	public virtual void OnSaveInstanceState (Android.OS.Bundle outState, Android.OS.PersistableBundle outPersistentState);
	public virtual void OnVisibleBehindCanceled ();
	public virtual void PostponeEnterTransition ();
	public virtual bool ReleaseInstance ();
	public virtual bool RequestVisibleBehind (bool visible);
	public virtual void SetActionBar (Android.Widget.Toolbar toolbar);
	public virtual void SetEnterSharedElementCallback (SharedElementCallback callback);
	public virtual void SetExitSharedElementCallback (SharedElementCallback callback);
	public virtual void SetTaskDescription (ActivityManager.TaskDescription taskDescription);
	public virtual void StartLockTask ();
	public virtual void StartPostponedEnterTransition ();
	public virtual void StopLockTask ();
```

### Type Changed: Android.App.ActivityManager

Added properties:

```
public virtual System.Collections.Generic.IList<ActivityManager.AppTask> AppTasks { get; }
	public virtual Android.Util.Size AppTaskThumbnailSize { get; }
	public virtual bool IsInLockTaskMode { get; }
```

Added method:

```
public virtual int AddAppTask (Activity activity, Android.Content.Intent intent, ActivityManager.TaskDescription description, Android.Graphics.Bitmap thumbnail);
```

### Type Changed: Android.App.ActivityManager.RecentTaskInfo

Added properties:

```
public int AffiliatedTaskId { get; set; }
	public ActivityManager.TaskDescription TaskDescription { get; set; }
```

### Type Changed: Android.App.ActivityManager.RunningAppProcessInfo

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.App.Importance enum directly instead of this field.")]
	public static const Importance ImportanceGone;
```

### New Type Android.App.AppTask

```
public class AppTask : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ActivityManager (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual ActivityManager.RecentTaskInfo TaskInfo { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void FinishAndRemoveTask ();
	public virtual void MoveToFront ();
	public virtual void SetExcludeFromRecents (bool exclude);
	public virtual void StartActivity (Android.Content.Context context, Android.Content.Intent intent, Android.OS.Bundle options);
}
```

### New Type Android.App.TaskDescription

```
public class TaskDescription : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ActivityManager (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ActivityManager (ActivityManager.TaskDescription td);
	public ActivityManager ();
	public ActivityManager (string label);
	public ActivityManager (string label, Android.Graphics.Bitmap icon);
	public ActivityManager (string label, Android.Graphics.Bitmap icon, Android.Graphics.Color colorPrimary);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual Android.Graphics.Bitmap Icon { get; }
	public virtual string Label { get; }
	public virtual int PrimaryColor { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void ReadFromParcel (Android.OS.Parcel source);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### Type Changed: Android.App.ActivityOptions

Removed method:

```
public static ActivityOptions MakeScaleUpAnimation (Android.Views.View source, int startX, int startY, int startWidth, int startHeight);
```

Added methods:

```
public static ActivityOptions MakeScaleUpAnimation (Android.Views.View source, int startX, int startY, int width, int height);
	public static ActivityOptions MakeSceneTransitionAnimation (Activity activity, Android.Views.View sharedElement, string sharedElementName);
	public static ActivityOptions MakeSceneTransitionAnimation (Activity activity, Android.Util.Pair[] sharedElements);
	public static ActivityOptions MakeTaskLaunchBehind ();
```

### Type Changed: Android.App.AlarmManager

Added field:

```
public static const string ActionNextAlarmClockChanged = "android.app.action.NEXT_ALARM_CLOCK_CHANGED";
```

Added property:

```
public virtual AlarmManager.AlarmClockInfo NextAlarmClock { get; }
```

Added method:

```
public virtual void SetAlarmClock (AlarmManager.AlarmClockInfo info, PendingIntent operation);
```

### Type Changed: Android.App.AlertDialog

### Type Changed: Android.App.AlertDialog.Builder

Added method:

```
public virtual AlertDialog.Builder SetView (int layoutResId);
```

### Type Changed: Android.App.AppOpsManager

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.App.AppOpsManagerMode enum directly instead of this field.")]
	public static const AppOpsManagerMode ModeDefault;
	public static const string OpstrGetUsageStats = "android:get_usage_stats";
```

### Type Changed: Android.App.AppOpsManagerMode

Added value:

```
Default = 3,
```

### Type Changed: Android.App.DatePickerDialog

Removed constructor:

```
public DatePickerDialog (Android.Content.Context context, int theme, DatePickerDialog.IOnDateSetListener callBack, int year, int monthOfYear, int dayOfMonth);
```

Added constructor:

```
public DatePickerDialog (Android.Content.Context context, int theme, DatePickerDialog.IOnDateSetListener listener, int year, int monthOfYear, int dayOfMonth);
```

### Type Changed: Android.App.Dialog

Added method:

```
public virtual void Create ();
```

### Type Changed: Android.App.EnableCarModeFlags

Added value:

```
AllowSleep = 2,
```

### Type Changed: Android.App.Fragment

Added properties:

```
public virtual bool AllowEnterTransitionOverlap { get; set; }
	public virtual bool AllowReturnTransitionOverlap { get; set; }
	public virtual Android.Transitions.Transition EnterTransition { get; set; }
	public virtual Android.Transitions.Transition ExitTransition { get; set; }
	public virtual Android.Transitions.Transition ReenterTransition { get; set; }
	public virtual Android.Transitions.Transition ReturnTransition { get; set; }
	public virtual Android.Transitions.Transition SharedElementEnterTransition { get; set; }
	public virtual Android.Transitions.Transition SharedElementReturnTransition { get; set; }
```

Added methods:

```
public virtual void SetEnterSharedElementCallback (SharedElementCallback callback);
	public virtual void SetExitSharedElementCallback (SharedElementCallback callback);
```

### Type Changed: Android.App.FragmentTransaction

Added method:

```
public virtual FragmentTransaction AddSharedElement (Android.Views.View sharedElement, string name);
```

### Type Changed: Android.App.Importance

Added value:

```
Gone = 1000,
```

### Type Changed: Android.App.Instrumentation

Added methods:

```
public virtual void CallActivityOnCreate (Activity activity, Android.OS.Bundle icicle, Android.OS.PersistableBundle persistentState);
	public virtual void CallActivityOnPostCreate (Activity activity, Android.OS.Bundle icicle, Android.OS.PersistableBundle persistentState);
	public virtual void CallActivityOnRestoreInstanceState (Activity activity, Android.OS.Bundle savedInstanceState, Android.OS.PersistableBundle persistentState);
	public virtual void CallActivityOnSaveInstanceState (Activity activity, Android.OS.Bundle outState, Android.OS.PersistableBundle outPersistentState);
```

### Type Changed: Android.App.KeyguardManager

Added methods:

```
public virtual Android.Content.Intent CreateConfirmDeviceCredentialIntent (Java.Lang.ICharSequence title, Java.Lang.ICharSequence description);
	public Android.Content.Intent CreateConfirmDeviceCredentialIntent (string title, string description);
```

### Type Changed: Android.App.MediaRouteButton

Added constructor:

```
public MediaRouteButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.App.Notification

Added fields:

```
public static const string CategoryAlarm = "alarm";
	public static const string CategoryCall = "call";
	public static const string CategoryEmail = "email";
	public static const string CategoryError = "err";
	public static const string CategoryEvent = "event";
	public static const string CategoryMessage = "msg";
	public static const string CategoryProgress = "progress";
	public static const string CategoryPromo = "promo";
	public static const string CategoryRecommendation = "recommendation";
	public static const string CategoryService = "service";
	public static const string CategorySocial = "social";
	public static const string CategoryStatus = "status";
	public static const string CategorySystem = "sys";
	public static const string CategoryTransport = "transport";
	public static const int ColorDefault;
	public static const string ExtraBackgroundImageUri = "android.backgroundImageUri";
	public static const string ExtraBigText = "android.bigText";
	public static const string ExtraCompactActions = "android.compactActions";
	public static const string ExtraMediaSession = "android.mediaSession";
	public static const string ExtraTemplate = "android.template";
	public static const string IntentCategoryNotificationPreferences = "android.intent.category.NOTIFICATION_PREFERENCES";
```

Added properties:

```
public Android.Media.AudioAttributes AudioAttributes { get; set; }
	public static Android.Media.AudioAttributes AudioAttributesDefault { get; set; }
	public string Category { get; set; }
	public int Color { get; set; }
	public Android.Widget.RemoteViews HeadsUpContentView { get; set; }
	public Notification PublicVersion { get; set; }
	public NotificationVisibility Visibility { get; set; }
```

### Type Changed: Android.App.Notification.Builder

Added methods:

```
public virtual Notification.Builder AddPerson (string uri);
	public virtual Notification.Builder SetCategory (string category);
	public virtual Notification.Builder SetColor (int argb);
	public virtual Notification.Builder SetPublicVersion (Notification n);
	public virtual Notification.Builder SetSound (Android.Net.Uri sound, Android.Media.AudioAttributes audioAttributes);
	public virtual Notification.Builder SetVisibility (NotificationVisibility visibility);
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public Notification.Builder SetTicker (string tickerText, Android.Widget.RemoteViews views);
```

### New Type Android.App.MediaStyle

```
public class MediaStyle : Android.App.Notification+Style, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected Notification (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Notification ();
	public Notification (Notification.Builder builder);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Notification.MediaStyle SetMediaSession (Android.Media.Session.MediaSession.Token token);
	public virtual Notification.MediaStyle SetShowActionsInCompactView (int[] actions);
}
```

### Type Changed: Android.App.SearchManager

Added fields:

```
public static const string SuggestColumnAudioChannelConfig = "suggest_audio_channel_config";
	public static const string SuggestColumnContentType = "suggest_content_type";
	public static const string SuggestColumnDuration = "suggest_duration";
	public static const string SuggestColumnIsLive = "suggest_is_live";
	public static const string SuggestColumnProductionYear = "suggest_production_year";
	public static const string SuggestColumnPurchasePrice = "suggest_purchase_price";
	public static const string SuggestColumnRatingScore = "suggest_rating_score";
	public static const string SuggestColumnRatingStyle = "suggest_rating_style";
	public static const string SuggestColumnRentalPrice = "suggest_rental_price";
	public static const string SuggestColumnResultCardImage = "suggest_result_card_image";
	public static const string SuggestColumnVideoHeight = "suggest_video_height";
	public static const string SuggestColumnVideoWidth = "suggest_video_width";
```

### Type Changed: Android.App.TimePickerDialog

Removed method:

```
public virtual void UpdateTime (int hourOfDay, int minutOfHour);
```

Added method:

```
public virtual void UpdateTime (int hourOfDay, int minuteOfHour);
```

### Type Changed: Android.App.UiAutomation

Added properties:

```
public Android.Views.WindowAnimationFrameStats WindowAnimationFrameStats { get; }
	public System.Collections.Generic.IList<Android.Views.Accessibility.AccessibilityWindowInfo> Windows { get; }
```

Added methods:

```
public void ClearWindowAnimationFrameStats ();
	public bool ClearWindowContentFrameStats (int windowId);
	public Android.OS.ParcelFileDescriptor ExecuteShellCommand (string command);
	public Android.Views.Accessibility.AccessibilityNodeInfo FindFocus (Android.Views.Accessibility.NodeFocus focus);
	public Android.Views.WindowContentFrameStats GetWindowContentFrameStats (int windowId);
```

### Type Changed: Android.App.UiModeManager

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.App.EnableCarModeFlags enum directly instead of this field.")]
	public static const EnableCarModeFlags EnableCarModeAllowSleep;
```

### New Type Android.App.NotificationVisibility

```
[Serializable]
public enum NotificationVisibility {
	Private = 0,
	Public = 1,
	Secret = -1,
}
```

### New Type Android.App.SharedElementCallback

```
public abstract class SharedElementCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected SharedElementCallback (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SharedElementCallback ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.OS.IParcelable OnCaptureSharedElementSnapshot (Android.Views.View sharedElement, Android.Graphics.Matrix viewToGlobalMatrix, Android.Graphics.RectF screenBounds);
	public virtual Android.Views.View OnCreateSnapshotView (Android.Content.Context context, Android.OS.IParcelable snapshot);
	public virtual void OnMapSharedElements (System.Collections.Generic.IList<string> names, System.Collections.Generic.IDictionary<System.String,Android.Views.View> sharedElements);
	public virtual void OnRejectSharedElements (System.Collections.Generic.IList<Android.Views.View> rejectedSharedElements);
	public virtual void OnSharedElementEnd (System.Collections.Generic.IList<string> sharedElementNames, System.Collections.Generic.IList<Android.Views.View> sharedElements, System.Collections.Generic.IList<Android.Views.View> sharedElementSnapshots);
	public virtual void OnSharedElementStart (System.Collections.Generic.IList<string> sharedElementNames, System.Collections.Generic.IList<Android.Views.View> sharedElements, System.Collections.Generic.IList<Android.Views.View> sharedElementSnapshots);
}
```

## Namespace Android.App.Admin

### Type Changed: Android.App.Admin.DeviceAdminReceiver

Added fields:

```
public static const string ActionLockTaskEntering = "android.app.action.LOCK_TASK_ENTERING";
	public static const string ActionLockTaskExiting = "android.app.action.LOCK_TASK_EXITING";
	public static const string ActionProfileProvisioningComplete = "android.app.action.PROFILE_PROVISIONING_COMPLETE";
	public static const string ExtraLockTaskPackage = "android.app.extra.LOCK_TASK_PACKAGE";
```

Added methods:

```
public virtual void OnLockTaskModeEntering (Android.Content.Context context, Android.Content.Intent intent, string pkg);
	public virtual void OnLockTaskModeExiting (Android.Content.Context context, Android.Content.Intent intent);
	public virtual void OnProfileProvisioningComplete (Android.Content.Context context, Android.Content.Intent intent);
```

### Type Changed: Android.App.Admin.DevicePolicyManager

Added fields:

```
public static const string ActionProvisionManagedProfile = "android.app.action.PROVISION_MANAGED_PROFILE";
	public static const string ExtraProvisioningAdminExtrasBundle = "android.app.extra.PROVISIONING_ADMIN_EXTRAS_BUNDLE";
	public static const string ExtraProvisioningDeviceAdminPackageChecksum = "android.app.extra.PROVISIONING_DEVICE_ADMIN_PACKAGE_CHECKSUM";
	public static const string ExtraProvisioningDeviceAdminPackageDownloadCookieHeader = "android.app.extra.PROVISIONING_DEVICE_ADMIN_PACKAGE_DOWNLOAD_COOKIE_HEADER";
	public static const string ExtraProvisioningDeviceAdminPackageDownloadLocation = "android.app.extra.PROVISIONING_DEVICE_ADMIN_PACKAGE_DOWNLOAD_LOCATION";
	public static const string ExtraProvisioningDeviceAdminPackageName = "android.app.extra.PROVISIONING_DEVICE_ADMIN_PACKAGE_NAME";
	public static const string ExtraProvisioningEmailAddress = "android.app.extra.PROVISIONING_EMAIL_ADDRESS";
	public static const string ExtraProvisioningLocale = "android.app.extra.PROVISIONING_LOCALE";
	public static const string ExtraProvisioningLocalTime = "android.app.extra.PROVISIONING_LOCAL_TIME";
	public static const string ExtraProvisioningTimeZone = "android.app.extra.PROVISIONING_TIME_ZONE";
	public static const string ExtraProvisioningWifiHidden = "android.app.extra.PROVISIONING_WIFI_HIDDEN";
	public static const string ExtraProvisioningWifiPacUrl = "android.app.extra.PROVISIONING_WIFI_PAC_URL";
	public static const string ExtraProvisioningWifiPassword = "android.app.extra.PROVISIONING_WIFI_PASSWORD";
	public static const string ExtraProvisioningWifiProxyBypass = "android.app.extra.PROVISIONING_WIFI_PROXY_BYPASS";
	public static const string ExtraProvisioningWifiProxyHost = "android.app.extra.PROVISIONING_WIFI_PROXY_HOST";
	public static const string ExtraProvisioningWifiProxyPort = "android.app.extra.PROVISIONING_WIFI_PROXY_PORT";
	public static const string ExtraProvisioningWifiSecurityType = "android.app.extra.PROVISIONING_WIFI_SECURITY_TYPE";
	public static const string ExtraProvisioningWifiSsid = "android.app.extra.PROVISIONING_WIFI_SSID";

	[Obsolete ("This constant will be removed in the future version. Use Android.App.Admin.DevicePolicyManagerFlags enum directly instead of this field.")]
	public static const DevicePolicyManagerFlags FlagManagedCanAccessParent;

	[Obsolete ("This constant will be removed in the future version. Use Android.App.Admin.DevicePolicyManagerFlags enum directly instead of this field.")]
	public static const DevicePolicyManagerFlags FlagParentCanAccessManaged;

	[Obsolete ("This constant will be removed in the future version. Use Android.App.Admin.KeyguardDisable enum directly instead of this field.")]
	public static const KeyguardDisable KeyguardDisableFingerprint;

	[Obsolete ("This constant will be removed in the future version. Use Android.App.Admin.KeyguardDisable enum directly instead of this field.")]
	public static const KeyguardDisable KeyguardDisableSecureNotifications;

	[Obsolete ("This constant will be removed in the future version. Use Android.App.Admin.KeyguardDisable enum directly instead of this field.")]
	public static const KeyguardDisable KeyguardDisableTrustAgents;

	[Obsolete ("This constant will be removed in the future version. Use Android.App.Admin.KeyguardDisable enum directly instead of this field.")]
	public static const KeyguardDisable KeyguardDisableUnredactedNotifications;
	public static const string MimeTypeProvisioningNfc = "application/com.android.managedprovisioning";
```

Added property:

```
public virtual bool AutoTimeRequired { get; }
```

Added methods:

```
public virtual void AddCrossProfileIntentFilter (Android.Content.ComponentName admin, Android.Content.IntentFilter filter, DevicePolicyManagerFlags flags);
	public virtual bool AddCrossProfileWidgetProvider (Android.Content.ComponentName admin, string packageName);
	public virtual void AddPersistentPreferredActivity (Android.Content.ComponentName admin, Android.Content.IntentFilter filter, Android.Content.ComponentName activity);
	public virtual void AddUserRestriction (Android.Content.ComponentName admin, string key);
	public virtual void ClearCrossProfileIntentFilters (Android.Content.ComponentName admin);
	public virtual void ClearDeviceOwnerApp (string packageName);
	public virtual void ClearPackagePersistentPreferredActivities (Android.Content.ComponentName admin, string packageName);
	public virtual void ClearUserRestriction (Android.Content.ComponentName admin, string key);
	public virtual Android.OS.UserHandle CreateAndInitializeUser (Android.Content.ComponentName admin, string name, string ownerName, Android.Content.ComponentName profileOwnerComponent, Android.OS.Bundle adminExtras);
	public virtual Android.OS.UserHandle CreateUser (Android.Content.ComponentName admin, string name);
	public virtual int EnableSystemApp (Android.Content.ComponentName admin, Android.Content.Intent intent);
	public virtual void EnableSystemApp (Android.Content.ComponentName admin, string packageName);
	public virtual string[] GetAccountTypesWithManagementDisabled ();
	public virtual Android.OS.Bundle GetApplicationRestrictions (Android.Content.ComponentName admin, string packageName);
	public virtual bool GetCrossProfileCallerIdDisabled (Android.Content.ComponentName who);
	public virtual System.Collections.Generic.IList<string> GetCrossProfileWidgetProviders (Android.Content.ComponentName admin);
	public virtual System.Collections.Generic.IList<System.Byte[]> GetInstalledCaCerts (Android.Content.ComponentName admin);
	public virtual System.Collections.Generic.IList<string> GetPermittedAccessibilityServices (Android.Content.ComponentName admin);
	public virtual System.Collections.Generic.IList<string> GetPermittedInputMethods (Android.Content.ComponentName admin);
	public virtual bool GetScreenCaptureDisabled (Android.Content.ComponentName admin);
	public virtual bool HasCaCertInstalled (Android.Content.ComponentName admin, byte[] certBuffer);
	public virtual bool InstallCaCert (Android.Content.ComponentName admin, byte[] certBuffer);
	public virtual bool InstallKeyPair (Android.Content.ComponentName who, Java.Security.IPrivateKey privKey, Java.Security.Cert.Certificate cert, string alias);
	public virtual bool IsApplicationHidden (Android.Content.ComponentName admin, string packageName);
	public virtual bool IsLockTaskPermitted (string pkg);
	public virtual bool IsMasterVolumeMuted (Android.Content.ComponentName admin);
	public virtual bool IsProfileOwnerApp (string packageName);
	public virtual bool IsUninstallBlocked (Android.Content.ComponentName admin, string packageName);
	public virtual bool RemoveCrossProfileWidgetProvider (Android.Content.ComponentName admin, string packageName);
	public virtual bool RemoveUser (Android.Content.ComponentName admin, Android.OS.UserHandle userHandle);
	public virtual void SetAccountManagementDisabled (Android.Content.ComponentName admin, string accountType, bool disabled);
	public virtual bool SetApplicationHidden (Android.Content.ComponentName admin, string packageName, bool hidden);
	public virtual void SetApplicationRestrictions (Android.Content.ComponentName admin, string packageName, Android.OS.Bundle settings);
	public virtual void SetAutoTimeRequired (Android.Content.ComponentName admin, bool required);
	public virtual void SetCrossProfileCallerIdDisabled (Android.Content.ComponentName who, bool disabled);
	public virtual void SetGlobalSetting (Android.Content.ComponentName admin, string setting, string value);
	public virtual void SetLockTaskPackages (Android.Content.ComponentName admin, string[] packages);
	public virtual void SetMasterVolumeMuted (Android.Content.ComponentName admin, bool on);
	public virtual bool SetPermittedAccessibilityServices (Android.Content.ComponentName admin, System.Collections.Generic.IList<string> packageNames);
	public virtual bool SetPermittedInputMethods (Android.Content.ComponentName admin, System.Collections.Generic.IList<string> packageNames);
	public virtual void SetProfileEnabled (Android.Content.ComponentName admin);
	public virtual void SetProfileName (Android.Content.ComponentName who, string profileName);
	public virtual void SetRecommendedGlobalProxy (Android.Content.ComponentName admin, Android.Net.ProxyInfo proxyInfo);
	public virtual void SetRestrictionsProvider (Android.Content.ComponentName admin, Android.Content.ComponentName provider);
	public virtual void SetScreenCaptureDisabled (Android.Content.ComponentName admin, bool disabled);
	public virtual void SetSecureSetting (Android.Content.ComponentName admin, string setting, string value);
	public virtual void SetUninstallBlocked (Android.Content.ComponentName admin, string packageName, bool uninstallBlocked);
	public virtual bool SwitchUser (Android.Content.ComponentName admin, Android.OS.UserHandle userHandle);
	public virtual void UninstallAllUserCaCerts (Android.Content.ComponentName admin);
	public virtual void UninstallCaCert (Android.Content.ComponentName admin, byte[] certBuffer);
```

### Type Changed: Android.App.Admin.DevicePolicyManagerFlags

Added values:

```
ManagedCanAccessParent = 2,
	ParentCanAccessManaged = 1,
```

### Type Changed: Android.App.Admin.KeyguardDisable

Added values:

```
Fingerprint = 32,
	SecureNotifications = 4,
	TrustAgents = 16,
	UnredactedNotifications = 8,
```

### Type Changed: Android.App.Admin.PasswordQuality

Added value:

```
NumericComplex = 196608,
```

## Namespace Android.App.Backup

### Type Changed: Android.App.Backup.BackupAgent

Added method:

```
public virtual void OnRestoreFinished ();
```

## Namespace Android.Appwidget

### Type Changed: Android.Appwidget.AppWidgetCategory

Added value:

```
Searchbox = 4,
```

### Type Changed: Android.Appwidget.AppWidgetHost

Added method:

```
public void StartAppWidgetConfigureActivityForResult (Android.App.Activity activity, int appWidgetId, Android.Content.ActivityFlags intentFlags, int requestCode, Android.OS.Bundle options);
```

### Type Changed: Android.Appwidget.AppWidgetManager

Added fields:

```
public static const string ActionAppwidgetHostRestored = "android.appwidget.action.APPWIDGET_HOST_RESTORED";
	public static const string ActionAppwidgetRestored = "android.appwidget.action.APPWIDGET_RESTORED";
	public static const string ExtraAppwidgetOldIds = "appWidgetOldIds";
	public static const string ExtraAppwidgetProviderProfile = "appWidgetProviderProfile";
	public static const string ExtraHostId = "hostId";
```

Added methods:

```
public virtual bool BindAppWidgetIdIfAllowed (int appWidgetId, Android.OS.UserHandle user, Android.Content.ComponentName provider, Android.OS.Bundle options);
	public virtual System.Collections.Generic.IList<AppWidgetProviderInfo> GetInstalledProvidersForProfile (Android.OS.UserHandle profile);
```

### Type Changed: Android.Appwidget.AppWidgetProvider

Added method:

```
public virtual void OnRestored (Android.Content.Context context, int[] oldWidgetIds, int[] newWidgetIds);
```

### Type Changed: Android.Appwidget.AppWidgetProviderInfo

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Appwidget.AppWidgetCategory enum directly instead of this field.")]
	public static const AppWidgetCategory WidgetCategorySearchbox;
```

Added property:

```
public Android.OS.UserHandle Profile { get; }
```

Added methods:

```
public Android.Graphics.Drawables.Drawable LoadIcon (Android.Content.Context context, int density);
	public string LoadLabel (Android.Content.PM.PackageManager packageManager);
	public Android.Graphics.Drawables.Drawable LoadPreviewImage (Android.Content.Context context, int density);
```

## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothAdapter

Added properties:

```
public LE.BluetoothLeAdvertiser BluetoothLeAdvertiser { get; }
	public LE.BluetoothLeScanner BluetoothLeScanner { get; }
	public bool IsMultipleAdvertisementSupported { get; }
	public bool IsOffloadedFilteringSupported { get; }
	public bool IsOffloadedScanBatchingSupported { get; }
```

### Type Changed: Android.Bluetooth.BluetoothGatt

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Bluetooth.GattConnectionPriority enum directly instead of this field.")]
	public static const GattConnectionPriority ConnectionPriorityBalanced;

	[Obsolete ("This constant will be removed in the future version. Use Android.Bluetooth.GattConnectionPriority enum directly instead of this field.")]
	public static const GattConnectionPriority ConnectionPriorityHigh;

	[Obsolete ("This constant will be removed in the future version. Use Android.Bluetooth.GattConnectionPriority enum directly instead of this field.")]
	public static const GattConnectionPriority ConnectionPriorityLowPower;

	[Obsolete ("This constant will be removed in the future version. Use Android.Bluetooth.GattStatus enum directly instead of this field.")]
	public static const GattStatus GattConnectionCongested;
```

Added methods:

```
public bool RequestConnectionPriority (GattConnectionPriority connectionPriority);
	public bool RequestMtu (int mtu);
```

### Type Changed: Android.Bluetooth.BluetoothGattCallback

Added method:

```
public virtual void OnMtuChanged (BluetoothGatt gatt, int mtu, GattStatus status);
```

### Type Changed: Android.Bluetooth.BluetoothGattServerCallback

Added method:

```
public virtual void OnNotificationSent (BluetoothDevice device, GattStatus status);
```

### Type Changed: Android.Bluetooth.GattStatus

Added value:

```
ConnectionCongested = 143,
```

### New Type Android.Bluetooth.GattConnectionPriority

```
[Serializable]
public enum GattConnectionPriority {
	Balanced = 0,
	High = 1,
	LowPower = 2,
}
```

## Namespace Android.Content

### Type Changed: Android.Content.ActivityFlags

Added values:

```
GrantPrefixUriPermission = 128,
	NewDocument = 524288,
	RetainInRecents = 8192,
```

### Type Changed: Android.Content.ContentResolver

Added fields:

```
public static const string AnyCursorItemType = "vnd.android.cursor.item/*";
	public static const string ExtraSize = "android.content.extra.SIZE";
```

Added method:

```
public static void CancelSync (SyncRequest request);
```

### Type Changed: Android.Content.Context

Added fields:

```
public static const string AppwidgetService = "appwidget";
	public static const string BatteryService = "batterymanager";
	public static const string CameraService = "camera";
	public static const string JobSchedulerService = "jobscheduler";
	public static const string LauncherAppsService = "launcherapps";
	public static const string MediaProjectionService = "media_projection";
	public static const string MediaSessionService = "media_session";
	public static const string RestrictionsService = "restrictions";
	public static const string TelecomService = "telecom";
	public static const string TvInputService = "tv_input";
```

Added properties:

```
public virtual Java.IO.File CodeCacheDir { get; }
	public virtual Java.IO.File NoBackupFilesDir { get; }
```

Added methods:

```
public Android.Graphics.Drawables.Drawable GetDrawable (int id);
	public virtual Java.IO.File[] GetExternalMediaDirs ();
```

### Type Changed: Android.Content.ContextWrapper

Added properties:

```
public override Java.IO.File CodeCacheDir { get; }
	public override Java.IO.File NoBackupFilesDir { get; }
```

Added method:

```
public override Java.IO.File[] GetExternalMediaDirs ();
```

### Type Changed: Android.Content.Intent

Added fields:

```
public static const string ActionApplicationRestrictionsChanged = "android.intent.action.APPLICATION_RESTRICTIONS_CHANGED";
	public static const string ActionManagedProfileAdded = "android.intent.action.MANAGED_PROFILE_ADDED";
	public static const string ActionManagedProfileRemoved = "android.intent.action.MANAGED_PROFILE_REMOVED";
	public static const string ActionOpenDocumentTree = "android.intent.action.OPEN_DOCUMENT_TREE";
	public static const string CategoryLeanbackLauncher = "android.intent.category.LEANBACK_LAUNCHER";
	public static const string ExtraAssistInputHintKeyboard = "android.intent.extra.ASSIST_INPUT_HINT_KEYBOARD";
	public static const string ExtraReplacementExtras = "android.intent.extra.REPLACEMENT_EXTRAS";
	public static const string ExtraUser = "android.intent.extra.USER";
```

### Type Changed: Android.Content.RestrictionEntry

Added constructors:

```
public RestrictionEntry (RestrictionEntryType type, string key);
	public RestrictionEntry (string key, int selectedInt);
```

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Content.RestrictionEntryType enum directly instead of this field.")]
	public static const RestrictionEntryType TypeInteger;

	[Obsolete ("This constant will be removed in the future version. Use Android.Content.RestrictionEntryType enum directly instead of this field.")]
	public static const RestrictionEntryType TypeString;
```

Added property:

```
public virtual int IntValue { get; set; }
```

### Type Changed: Android.Content.RestrictionEntryType

Added values:

```
Integer = 5,
	String = 6,
```

### New Type Android.Content.RestrictionResults

```
[Serializable]
public enum RestrictionResults {
	Approved = 1,
	Denied = 2,
	Error = 5,
	ErrorBadRequest = 1,
	ErrorInternal = 3,
	ErrorNetwork = 2,
	NoResponse = 3,
	UnknownRequest = 4,
}
```

### New Type Android.Content.RestrictionsManager

```
public class RestrictionsManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected RestrictionsManager (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const string ActionPermissionResponseReceived = "android.content.action.PERMISSION_RESPONSE_RECEIVED";
	public static const string ActionRequestLocalApproval = "android.content.action.REQUEST_LOCAL_APPROVAL";
	public static const string ActionRequestPermission = "android.content.action.REQUEST_PERMISSION";
	public static const string ExtraPackageName = "android.content.extra.PACKAGE_NAME";
	public static const string ExtraRequestBundle = "android.content.extra.REQUEST_BUNDLE";
	public static const string ExtraRequestId = "android.content.extra.REQUEST_ID";
	public static const string ExtraRequestType = "android.content.extra.REQUEST_TYPE";
	public static const string ExtraResponseBundle = "android.content.extra.RESPONSE_BUNDLE";
	public static const string MetaDataAppRestrictions = "android.content.APP_RESTRICTIONS";
	public static const string RequestKeyApproveLabel = "android.request.approve_label";
	public static const string RequestKeyData = "android.request.data";
	public static const string RequestKeyDenyLabel = "android.request.deny_label";
	public static const string RequestKeyIcon = "android.request.icon";
	public static const string RequestKeyId = "android.request.id";
	public static const string RequestKeyMessage = "android.request.mesg";
	public static const string RequestKeyNewRequest = "android.request.new_request";
	public static const string RequestKeyTitle = "android.request.title";
	public static const string RequestTypeApproval = "android.request.type.approval";
	public static const string ResponseKeyErrorCode = "android.response.errorcode";
	public static const string ResponseKeyMessage = "android.response.msg";
	public static const string ResponseKeyResponseTimestamp = "android.response.timestamp";
	public static const string ResponseKeyResult = "android.response.result";
	// properties
	public virtual Android.OS.Bundle ApplicationRestrictions { get; }
	public virtual bool HasRestrictionsProvider { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Intent CreateLocalApprovalIntent ();
	public virtual System.Collections.Generic.IList<RestrictionEntry> GetManifestRestrictions (string packageName);
	public virtual void NotifyPermissionResponse (string packageName, Android.OS.PersistableBundle response);
	public virtual void RequestPermission (string requestType, string requestId, Android.OS.PersistableBundle request);
}
```

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ActivityInfo

Added properties:

```
public DocumentLaunchMode DocumentLaunchMode { get; set; }
	public int MaxRecents { get; set; }
	public ActivityPersistableMode PersistableMode { get; set; }
```

### Type Changed: Android.Content.PM.ActivityInfoFlags

Added values:

```
AutoRemoveFromRecents = 8192,
	RelinquishTaskIdentity = 4096,
	ResumeWhilePausing = 16384,
```

### Type Changed: Android.Content.PM.ApplicationInfo

Added properties:

```
public System.Collections.Generic.IList<string> SplitPublicSourceDirs { get; set; }
	public System.Collections.Generic.IList<string> SplitSourceDirs { get; set; }
```

### Type Changed: Android.Content.PM.ApplicationInfoFlags

Added values:

```
FullBackupOnly = 67108864,
	IsGame = 33554432,
	Multiarch = -2147483648,
```

### Type Changed: Android.Content.PM.InstrumentationInfo

Added properties:

```
public System.Collections.Generic.IList<string> SplitPublicSourceDirs { get; set; }
	public System.Collections.Generic.IList<string> SplitSourceDirs { get; set; }
```

### Type Changed: Android.Content.PM.PackageInfo

Added properties:

```
public System.Collections.Generic.IList<FeatureGroupInfo> FeatureGroups { get; set; }
	public PackageInstallLocation InstallLocation { get; set; }
	public System.Collections.Generic.IList<string> SplitNames { get; set; }
```

### Type Changed: Android.Content.PM.PackageManager

Added fields:

```
public static const string FeatureAudioOutput = "android.hardware.audio.output";
	public static const string FeatureCameraCapabilityManualPostProcessing = "android.hardware.camera.capability.manual_post_processing";
	public static const string FeatureCameraCapabilityManualSensor = "android.hardware.camera.capability.manual_sensor";
	public static const string FeatureCameraCapabilityRaw = "android.hardware.camera.capability.raw";
	public static const string FeatureCameraLevelFull = "android.hardware.camera.level.full";
	public static const string FeatureConnectionService = "android.software.connectionservice";
	public static const string FeatureGamepad = "android.hardware.gamepad";
	public static const string FeatureLeanback = "android.software.leanback";
	public static const string FeatureLiveTv = "android.software.live_tv";
	public static const string FeatureManagedUsers = "android.software.managed_users";
	public static const string FeatureOpenglesExtensionPack = "android.hardware.opengles.aep";
	public static const string FeatureSecurelyRemovesUsers = "android.software.securely_removes_users";
	public static const string FeatureSensorAmbientTemperature = "android.hardware.sensor.ambient_temperature";
	public static const string FeatureSensorHeartRateEcg = "android.hardware.sensor.heartrate.ecg";
	public static const string FeatureSensorRelativeHumidity = "android.hardware.sensor.relative_humidity";
	public static const string FeatureVerifiedBoot = "android.software.verified_boot";
```

Added property:

```
public virtual PackageInstaller PackageInstaller { get; }
```

Added methods:

```
public virtual Android.Content.Intent GetLeanbackLaunchIntentForPackage (string packageName);
	public virtual Android.Graphics.Drawables.Drawable GetUserBadgedDrawableForDensity (Android.Graphics.Drawables.Drawable drawable, Android.OS.UserHandle user, Android.Graphics.Rect badgeLocation, int badgeDensity);
	public virtual Android.Graphics.Drawables.Drawable GetUserBadgedIcon (Android.Graphics.Drawables.Drawable icon, Android.OS.UserHandle user);
	public string GetUserBadgedLabel (string label, Android.OS.UserHandle user);
	public virtual Java.Lang.ICharSequence GetUserBadgedLabelFormatted (Java.Lang.ICharSequence label, Android.OS.UserHandle user);
```

### Type Changed: Android.Content.PM.Protection

Added value:

```
FlagAppop = 64,
```

### New Type Android.Content.PM.ActivityPersistableMode

```
[Serializable]
public enum ActivityPersistableMode {
	AcrossReboots = 2,
	Never = 1,
	RootOnly = 0,
}
```

### New Type Android.Content.PM.DocumentLaunchMode

```
[Serializable]
public enum DocumentLaunchMode {
	Always = 2,
	IntoExisting = 1,
	Never = 3,
	None = 0,
}
```

### New Type Android.Content.PM.FeatureGroupInfo

```
public sealed class FeatureGroupInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public FeatureGroupInfo ();
	public FeatureGroupInfo (FeatureGroupInfo other);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public System.Collections.Generic.IList<FeatureInfo> Features { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Content.PM.LauncherActivityInfo

```
public class LauncherActivityInfo : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected LauncherActivityInfo (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual ApplicationInfo ApplicationInfo { get; }
	public virtual Android.Content.ComponentName ComponentName { get; }
	public virtual long FirstInstallTime { get; }
	public string Label { get; }
	public virtual Java.Lang.ICharSequence LabelFormatted { get; }
	public virtual string Name { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual Android.OS.UserHandle User { get; }
	// methods
	public virtual Android.Graphics.Drawables.Drawable GetBadgedIcon (int density);
	public virtual Android.Graphics.Drawables.Drawable GetIcon (int density);
}
```

### New Type Android.Content.PM.LauncherApps

```
public class LauncherApps : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected LauncherApps (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual System.Collections.Generic.IList<LauncherActivityInfo> GetActivityList (string packageName, Android.OS.UserHandle user);
	public virtual bool IsActivityEnabled (Android.Content.ComponentName component, Android.OS.UserHandle user);
	public virtual bool IsPackageEnabled (string packageName, Android.OS.UserHandle user);
	public virtual void RegisterCallback (LauncherApps.Callback callback, Android.OS.Handler handler);
	public virtual void RegisterCallback (LauncherApps.Callback callback);
	public virtual LauncherActivityInfo ResolveActivity (Android.Content.Intent intent, Android.OS.UserHandle user);
	public virtual void StartAppDetailsActivity (Android.Content.ComponentName component, Android.OS.UserHandle user, Android.Graphics.Rect sourceBounds, Android.OS.Bundle opts);
	public virtual void StartMainActivity (Android.Content.ComponentName component, Android.OS.UserHandle user, Android.Graphics.Rect sourceBounds, Android.OS.Bundle opts);
	public virtual void UnregisterCallback (LauncherApps.Callback callback);

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected LauncherApps (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public LauncherApps ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnPackageAdded (string packageName, Android.OS.UserHandle user);
		public virtual void OnPackageChanged (string packageName, Android.OS.UserHandle user);
		public virtual void OnPackageRemoved (string packageName, Android.OS.UserHandle user);
		public virtual void OnPackagesAvailable (string[] packageNames, Android.OS.UserHandle user, bool replacing);
		public virtual void OnPackagesUnavailable (string[] packageNames, Android.OS.UserHandle user, bool replacing);
	}
}
```

### New Type Android.Content.PM.PackageInstaller

```
public class PackageInstaller : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected PackageInstaller (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const string ActionSessionDetails = "android.content.pm.action.SESSION_DETAILS";
	public static const string ExtraOtherPackageName = "android.content.pm.extra.OTHER_PACKAGE_NAME";
	public static const string ExtraPackageName = "android.content.pm.extra.PACKAGE_NAME";
	public static const string ExtraSessionId = "android.content.pm.extra.SESSION_ID";
	public static const string ExtraStatus = "android.content.pm.extra.STATUS";
	public static const string ExtraStatusMessage = "android.content.pm.extra.STATUS_MESSAGE";
	public static const string ExtraStoragePath = "android.content.pm.extra.STORAGE_PATH";
	// properties
	public virtual System.Collections.Generic.IList<PackageInstaller.SessionInfo> AllSessions { get; }
	public virtual System.Collections.Generic.IList<PackageInstaller.SessionInfo> MySessions { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void AbandonSession (int sessionId);
	public virtual int CreateSession (PackageInstaller.SessionParams params);
	public virtual PackageInstaller.SessionInfo GetSessionInfo (int sessionId);
	public virtual PackageInstaller.Session OpenSession (int sessionId);
	public virtual void RegisterSessionCallback (PackageInstaller.SessionCallback callback, Android.OS.Handler handler);
	public virtual void RegisterSessionCallback (PackageInstaller.SessionCallback callback);
	public virtual void Uninstall (string packageName, Android.Content.IntentSender statusReceiver);
	public virtual void UnregisterSessionCallback (PackageInstaller.SessionCallback callback);
	public virtual void UpdateSessionAppIcon (int sessionId, Android.Graphics.Bitmap appIcon);
	public virtual void UpdateSessionAppLabel (int sessionId, Java.Lang.ICharSequence appLabel);
	public void UpdateSessionAppLabel (int sessionId, string appLabel);

	// inner types
	public class Session : Java.Lang.Object, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		protected PackageInstaller (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void Abandon ();
		public virtual void Close ();
		public virtual void Commit (Android.Content.IntentSender statusReceiver);
		public virtual void Fsync (System.IO.Stream out);
		public virtual string[] GetNames ();
		public virtual System.IO.Stream OpenRead (string name);
		public virtual System.IO.Stream OpenWrite (string name, long offsetBytes, long lengthBytes);
		public virtual void SetStagingProgress (float progress);
	}
	public abstract class SessionCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected PackageInstaller (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public PackageInstaller ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnActiveChanged (int sessionId, bool active);
		public virtual void OnBadgingChanged (int sessionId);
		public virtual void OnCreated (int sessionId);
		public virtual void OnFinished (int sessionId, bool success);
		public virtual void OnProgressChanged (int sessionId, float progress);
	}
	public class SessionInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		protected PackageInstaller (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		public virtual Android.Graphics.Bitmap AppIcon { get; }
		public string AppLabel { get; }
		public virtual Java.Lang.ICharSequence AppLabelFormatted { get; }
		public virtual string AppPackageName { get; }
		public static Android.OS.IParcelableCreator Creator { get; set; }
		public virtual string InstallerPackageName { get; }
		public virtual bool IsActive { get; }
		public virtual float Progress { get; }
		public virtual int SessionId { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual Android.Content.Intent CreateDetailsIntent ();
		public virtual int DescribeContents ();
		public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const int ContentsFileDescriptor;

			[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
		}
	}
	public class SessionParams : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		protected PackageInstaller (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public PackageInstaller (PackageInstallMode mode);
		// properties
		public static Android.OS.IParcelableCreator Creator { get; set; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual int DescribeContents ();
		public virtual void SetAppIcon (Android.Graphics.Bitmap appIcon);
		public virtual void SetAppLabel (Java.Lang.ICharSequence appLabel);
		public void SetAppLabel (string appLabel);
		public virtual void SetAppPackageName (string appPackageName);
		public virtual void SetInstallLocation (PackageInstallLocation installLocation);
		public virtual void SetOriginatingUri (Android.Net.Uri originatingUri);
		public virtual void SetReferrerUri (Android.Net.Uri referrerUri);
		public virtual void SetSize (long sizeBytes);
		public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const int ContentsFileDescriptor;

			[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
		}
	}
}
```

### New Type Android.Content.PM.PackageInstallLocation

```
[Serializable]
public enum PackageInstallLocation {
	Auto = 0,
	InternalOnly = 1,
	PreferExternal = 2,
}
```

### New Type Android.Content.PM.PackageInstallMode

```
[Serializable]
public enum PackageInstallMode {
	FullInstall = 1,
	InheritExisting = 2,
}
```

### New Type Android.Content.PM.PackageInstallStatus

```
[Serializable]
public enum PackageInstallStatus {
	Failure = 1,
	FailureAborted = 3,
	FailureBlocked = 2,
	FailureConflict = 5,
	FailureIncompatible = 7,
	FailureInvalid = 4,
	FailureStorage = 6,
	PendingUserAction = -1,
	Success = 0,
}
```

## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.ColorStateList

Added property:

```
public virtual bool IsOpaque { get; }
```

### Type Changed: Android.Content.Res.Resources

Added methods:

```
public virtual Android.Graphics.Drawables.Drawable GetDrawable (int id, Resources.Theme theme);
	public virtual Android.Graphics.Drawables.Drawable GetDrawableForDensity (int id, int density, Resources.Theme theme);
```

### Type Changed: Android.Content.Res.Resources.Theme

Added property:

```
public Resources Resources { get; }
```

Added method:

```
public Android.Graphics.Drawables.Drawable GetDrawable (int id);
```

### Type Changed: Android.Content.Res.TypedArray

Added property:

```
public virtual int ChangingConfigurations { get; }
```

Added method:

```
public virtual int GetType (int index);
```

## Namespace Android.Gestures

### Type Changed: Android.Gestures.GestureOverlayView

Added constructor:

```
public GestureOverlayView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

## Namespace Android.Graphics

### Type Changed: Android.Graphics.Canvas

Added methods:

```
public virtual void DrawArc (float left, float top, float right, float bottom, float startAngle, float sweepAngle, bool useCenter, Paint paint);
	public virtual void DrawOval (float left, float top, float right, float bottom, Paint paint);
	public virtual void DrawRoundRect (float left, float top, float right, float bottom, float rx, float ry, Paint paint);
	public virtual int SaveLayer (float left, float top, float right, float bottom, Paint paint);
	public virtual int SaveLayer (RectF bounds, Paint paint);
	public virtual int SaveLayerAlpha (float left, float top, float right, float bottom, int alpha);
	public virtual int SaveLayerAlpha (RectF bounds, int alpha);
```

### Type Changed: Android.Graphics.ImageFormat

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Graphics.ImageFormatType enum directly instead of this field.")]
	public static const ImageFormatType Raw10;

	[Obsolete ("This constant will be removed in the future version. Use Android.Graphics.ImageFormatType enum directly instead of this field.")]
	public static const ImageFormatType RawSensor;
```

### Type Changed: Android.Graphics.ImageFormatType

Added values:

```
Raw10 = 37,
	RawSensor = 32,
```

### Type Changed: Android.Graphics.Matrix

Added property:

```
public virtual bool IsAffine { get; }
```

### Type Changed: Android.Graphics.Paint

Added properties:

```
public virtual bool ElegantTextHeight { get; set; }
	public virtual string FontFeatureSettings { get; set; }
	public virtual float LetterSpacing { get; set; }
```

Removed method:

```
public virtual void SetShadowLayer (float radius, float dx, float dy, Color color);
```

Added method:

```
public virtual void SetShadowLayer (float radius, float dx, float dy, Color shadowColor);
```

### Type Changed: Android.Graphics.Path

Added property:

```
public virtual bool IsConvex { get; }
```

Added methods:

```
public virtual void AddArc (float left, float top, float right, float bottom, float startAngle, float sweepAngle);
	public virtual void AddOval (float left, float top, float right, float bottom, Path.Direction dir);
	public virtual void AddRoundRect (float left, float top, float right, float bottom, float[] radii, Path.Direction dir);
	public virtual void AddRoundRect (float left, float top, float right, float bottom, float rx, float ry, Path.Direction dir);
	public virtual void ArcTo (float left, float top, float right, float bottom, float startAngle, float sweepAngle, bool forceMoveTo);
```

### Type Changed: Android.Graphics.RadialGradient

Removed constructors:

```
public RadialGradient (float x, float y, float radius, Color color0, Color color1, Shader.TileMode tile);
	public RadialGradient (float x, float y, float radius, int[] colors, float[] positions, Shader.TileMode tile);
```

Added constructors:

```
public RadialGradient (float centerX, float centerY, float radius, Color centerColor, Color edgeColor, Shader.TileMode tileMode);
	public RadialGradient (float centerX, float centerY, float radius, int[] colors, float[] stops, Shader.TileMode tileMode);
```

### Type Changed: Android.Graphics.SurfaceTexture

Added method:

```
public virtual void SetOnFrameAvailableListener (SurfaceTexture.IOnFrameAvailableListener listener, Android.OS.Handler handler);
```

### New Type Android.Graphics.Outline

```
public sealed class Outline : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public Outline ();
	public Outline (Outline src);
	// properties
	public float Alpha { get; set; }
	public bool IsEmpty { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public bool CanClip ();
	public void Set (Outline src);
	public void SetConvexPath (Path convexPath);
	public void SetEmpty ();
	public void SetOval (int left, int top, int right, int bottom);
	public void SetOval (Rect rect);
	public void SetRect (Rect rect);
	public void SetRect (int left, int top, int right, int bottom);
	public void SetRoundRect (Rect rect, float radius);
	public void SetRoundRect (int left, int top, int right, int bottom, float radius);
}
```

## Namespace Android.Graphics.Drawables

### Type Changed: Android.Graphics.Drawables.Drawable

Added properties:

```
public virtual Android.Graphics.ColorFilter ColorFilter { get; }
	public virtual Android.Graphics.Rect DirtyBounds { get; }
```

Added methods:

```
public virtual void ApplyTheme (Android.Content.Res.Resources.Theme t);
	public virtual bool CanApplyTheme ();
	public static Drawable CreateFromXml (Android.Content.Res.Resources r, System.Xml.XmlReader parser, Android.Content.Res.Resources.Theme theme);
	public static System.Threading.Tasks.Task<Drawable> CreateFromXmlAsync (Android.Content.Res.Resources r, System.Xml.XmlReader parser, Android.Content.Res.Resources.Theme theme);
	public static Drawable CreateFromXmlInner (Android.Content.Res.Resources r, System.Xml.XmlReader parser, Android.Util.IAttributeSet attrs, Android.Content.Res.Resources.Theme theme);
	public virtual void GetOutline (Android.Graphics.Outline outline);
	public virtual void Inflate (Android.Content.Res.Resources r, System.Xml.XmlReader parser, Android.Util.IAttributeSet attrs, Android.Content.Res.Resources.Theme theme);
	public System.Threading.Tasks.Task InflateAsync (Android.Content.Res.Resources r, System.Xml.XmlReader parser, Android.Util.IAttributeSet attrs, Android.Content.Res.Resources.Theme theme);
	public virtual void SetHotspot (float x, float y);
	public virtual void SetHotspotBounds (int left, int top, int right, int bottom);
	public virtual void SetTint (int tint);
	public virtual void SetTintList (Android.Content.Res.ColorStateList tint);
	public virtual void SetTintMode (Android.Graphics.PorterDuff.Mode tintMode);
```

### Type Changed: Android.Graphics.Drawables.Drawable.ConstantState

Added methods:

```
public virtual bool CanApplyTheme ();
	public virtual Drawable NewDrawable (Android.Content.Res.Resources res, Android.Content.Res.Resources.Theme theme);
```

### Type Changed: Android.Graphics.Drawables.GradientDrawable

Added property:

```
public virtual float GradientRadius { get; }
```

Added methods:

```
public virtual void SetColor (Android.Content.Res.ColorStateList colorStateList);
	public virtual void SetStroke (int width, Android.Content.Res.ColorStateList colorStateList);
	public virtual void SetStroke (int width, Android.Content.Res.ColorStateList colorStateList, float dashWidth, float dashGap);
```

### Type Changed: Android.Graphics.Drawables.LayerDrawable

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Graphics.Drawables.LayerDrawablePaddingMode enum directly instead of this field.")]
	public static const LayerDrawablePaddingMode PaddingModeNest;

	[Obsolete ("This constant will be removed in the future version. Use Android.Graphics.Drawables.LayerDrawablePaddingMode enum directly instead of this field.")]
	public static const LayerDrawablePaddingMode PaddingModeStack;
```

Added property:

```
public virtual int PaddingMode { get; set; }
```

### Type Changed: Android.Graphics.Drawables.RotateDrawable

Removed property:

```
public virtual Drawable Drawable { get; }
```

Added properties:

```
public virtual Drawable Drawable { get; set; }
	public virtual float FromDegrees { get; set; }
	public virtual float PivotX { get; set; }
	public virtual bool PivotXRelative { get; set; }
	public virtual float PivotY { get; set; }
	public virtual bool PivotYRelative { get; set; }
	public virtual float ToDegrees { get; set; }
```

### New Type Android.Graphics.Drawables.AnimatedStateListDrawable

```
public class AnimatedStateListDrawable : Android.Graphics.Drawables.StateListDrawable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AnimatedStateListDrawable (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AnimatedStateListDrawable ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void AddState (int[] stateSet, Drawable drawable, int id);
	public virtual void AddTransition (int fromId, int toId, Java.Lang.Object transition, bool reversible);
}
```

### New Type Android.Graphics.Drawables.AnimatedVectorDrawable

```
public class AnimatedVectorDrawable : Android.Graphics.Drawables.Drawable, IAnimatable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AnimatedVectorDrawable (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AnimatedVectorDrawable ();
	// properties
	public virtual bool IsRunning { get; }
	public override int Opacity { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Draw (Android.Graphics.Canvas canvas);
	public override void SetAlpha (int alpha);
	public override void SetColorFilter (Android.Graphics.ColorFilter colorFilter);
	public virtual void Start ();
	public virtual void Stop ();
}
```

### New Type Android.Graphics.Drawables.LayerDrawablePaddingMode

```
[Serializable]
public enum LayerDrawablePaddingMode {
	Nest = 0,
	Stack = 1,
}
```

### New Type Android.Graphics.Drawables.RippleDrawable

```
public class RippleDrawable : Android.Graphics.Drawables.LayerDrawable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RippleDrawable (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RippleDrawable (Android.Content.Res.ColorStateList color, Drawable content, Drawable mask);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void SetColor (Android.Content.Res.ColorStateList color);
}
```

### New Type Android.Graphics.Drawables.VectorDrawable

```
public class VectorDrawable : Android.Graphics.Drawables.Drawable, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected VectorDrawable (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public VectorDrawable ();
	// properties
	public override int Opacity { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Draw (Android.Graphics.Canvas canvas);
	public override void SetAlpha (int alpha);
	public override void SetColorFilter (Android.Graphics.ColorFilter colorFilter);
}
```

## Namespace Android.Graphics.Drawables.Shapes

### Type Changed: Android.Graphics.Drawables.Shapes.Shape

Added method:

```
public virtual void GetOutline (Android.Graphics.Outline outline);
```

## Namespace Android.Graphics.Pdf

### New Type Android.Graphics.Pdf.PdfRenderer

```
public sealed class PdfRenderer : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public PdfRenderer (Android.OS.ParcelFileDescriptor input);
	// properties
	public int PageCount { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void Close ();
	public PdfRenderer.Page OpenPage (int index);
	public bool ShouldScaleForPrinting ();

	// inner types
	public sealed class Page : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// fields

		[Obsolete ("This constant will be removed in the future version. Use Android.Graphics.Pdf.PdfRenderMode enum directly instead of this field.")]
		public static const PdfRenderMode RenderModeForDisplay;

		[Obsolete ("This constant will be removed in the future version. Use Android.Graphics.Pdf.PdfRenderMode enum directly instead of this field.")]
		public static const PdfRenderMode RenderModeForPrint;
		// properties
		public int Height { get; }
		public int Index { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public int Width { get; }
		// methods
		public void Close ();
		public void Render (Android.Graphics.Bitmap destination, Android.Graphics.Rect destClip, Android.Graphics.Matrix transform, PdfRenderMode renderMode);
	}
}
```

### New Type Android.Graphics.Pdf.PdfRenderMode

```
[Serializable]
public enum PdfRenderMode {
	ForDisplay = 1,
	ForPrint = 2,
}
```

## Namespace Android.Hardware

### Type Changed: Android.Hardware.Sensor

Added properties:

```
public virtual bool IsWakeUpSensor { get; }
	public virtual int MaxDelay { get; }
	public virtual ReportingMode ReportingMode { get; }
```

### Type Changed: Android.Hardware.SensorManager

Added method:

```
public virtual Sensor GetDefaultSensor (SensorType type, bool wakeUp);
```

### New Type Android.Hardware.ReportingMode

```
[Serializable]
public enum ReportingMode {
	Continuous = 0,
	OnChange = 1,
	OneShot = 2,
	SpecialTrigger = 3,
}
```

## Namespace Android.Hardware.Display

### Type Changed: Android.Hardware.Display.DisplayManager

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Display.VirtualDisplayFlags enum directly instead of this field.")]
	public static const VirtualDisplayFlags VirtualDisplayFlagAutoMirror;
```

Added method:

```
public VirtualDisplay CreateVirtualDisplay (string name, int width, int height, int densityDpi, Android.Views.Surface surface, VirtualDisplayFlags flags, VirtualDisplay.Callback callback, Android.OS.Handler handler);
```

### Type Changed: Android.Hardware.Display.VirtualDisplay

Added method:

```
public void Resize (int width, int height, int densityDpi);
```

### Type Changed: Android.Hardware.Display.VirtualDisplayFlags

Added value:

```
AutoMirror = 16,
```

## Namespace Android.Hardware.Usb

### Type Changed: Android.Hardware.Usb.UsbDevice

Added properties:

```
public virtual int ConfigurationCount { get; }
	public virtual string ManufacturerName { get; }
	public virtual string ProductName { get; }
	public virtual string SerialNumber { get; }
```

Added method:

```
public virtual UsbConfiguration GetConfiguration (int index);
```

### Type Changed: Android.Hardware.Usb.UsbDeviceConnection

Added methods:

```
public virtual bool SetConfiguration (UsbConfiguration configuration);
	public virtual bool SetInterface (UsbInterface intf);
```

### Type Changed: Android.Hardware.Usb.UsbInterface

Added properties:

```
public virtual int AlternateSetting { get; }
	public virtual string Name { get; }
```

### New Type Android.Hardware.Usb.UsbConfiguration

```
public class UsbConfiguration : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected UsbConfiguration (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual int Id { get; }
	public virtual int InterfaceCount { get; }
	public virtual bool IsRemoteWakeup { get; }
	public virtual bool IsSelfPowered { get; }
	public virtual int MaxPower { get; }
	public virtual string Name { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual UsbInterface GetInterface (int index);
	public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

## Namespace Android.InputMethodServices

### Type Changed: Android.InputMethodServices.AbstractInputMethodService

### Type Changed: Android.InputMethodServices.AbstractInputMethodService.AbstractInputMethodSessionImpl

Added method:

```
public virtual void UpdateCursorAnchorInfo (Android.Views.InputMethods.CursorAnchorInfo cursorAnchorInfo);
```

### Type Changed: Android.InputMethodServices.ExtractEditText

Added constructor:

```
public ExtractEditText (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.InputMethodServices.InputMethodService

Added property:

```
public virtual int InputMethodWindowRecommendedHeight { get; }
```

Added method:

```
public virtual void OnUpdateCursorAnchorInfo (Android.Views.InputMethods.CursorAnchorInfo cursorAnchorInfo);
```

### Type Changed: Android.InputMethodServices.InputMethodService.InputMethodSessionImpl

Added method:

```
public override void UpdateCursorAnchorInfo (Android.Views.InputMethods.CursorAnchorInfo info);
```

### Type Changed: Android.InputMethodServices.KeyboardView

Added constructor:

```
public KeyboardView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

## Namespace Android.Media

### Type Changed: Android.Media.AudioEncoder

Added value:

```
Vorbis = 6,
```

### Type Changed: Android.Media.AudioFlags

Added values:

```
AudibilityEnforced = 1,
	HwAvSync = 16,
```

### Type Changed: Android.Media.AudioFormat

Added properties:

```
public virtual ChannelOut ChannelMask { get; }
	public virtual Encoding Encoding { get; }
	public virtual int SampleRate { get; }
```

### Type Changed: Android.Media.AudioManager

Added fields:

```
public static const string ActionHdmiAudioPlug = "android.media.action.HDMI_AUDIO_PLUG";
	public static const string ActionHeadsetPlug = "android.intent.action.HEADSET_PLUG";
	public static const int AudioSessionIdGenerate;
	public static const int Error;
	public static const int ErrorDeadObject;
	public static const string ExtraAudioPlugState = "android.media.extra.AUDIO_PLUG_STATE";
	public static const string ExtraEncodings = "android.media.extra.ENCODINGS";
	public static const string ExtraMaxChannelCount = "android.media.extra.MAX_CHANNEL_COUNT";
```

Added property:

```
public virtual bool IsVolumeFixed { get; }
```

Added method:

```
public virtual int GenerateAudioSessionId ();
```

### Type Changed: Android.Media.AudioTrack

Added constructor:

```
public AudioTrack (AudioAttributes attributes, AudioFormat format, int bufferSizeInBytes, AudioTrackMode mode, int sessionId);
```

Added methods:

```
public virtual TrackStatus SetVolume (float gain);
	public virtual int Write (float[] audioData, int offsetInFloats, int sizeInFloats, WriteMode writeMode);
	public virtual int Write (Java.Nio.ByteBuffer audioData, int sizeInBytes, WriteMode writeMode);
	public System.Threading.Tasks.Task<int> WriteAsync (Java.Nio.ByteBuffer audioData, int sizeInBytes, WriteMode writeMode);
	public System.Threading.Tasks.Task<int> WriteAsync (float[] audioData, int offsetInFloats, int sizeInFloats, WriteMode writeMode);
```

### Type Changed: Android.Media.CamcorderQuality

Added values:

```
HighSpeed1080p = 2004,
	HighSpeed2160p = 2005,
	HighSpeed480p = 2002,
	HighSpeed720p = 2003,
	HighSpeedHigh = 2001,
	HighSpeedLow = 2000,
	Q2160p = 8,
	TimeLapse2160p = 1008,
```

### Type Changed: Android.Media.ChannelOut

Added values:

```
SideLeft = 2048,
	SideRight = 4096,
```

### Type Changed: Android.Media.Encoding

Added values:

```
Ac3 = 5,
	EAc3 = 6,
	PcmFloat = 4,
```

### Type Changed: Android.Media.Image

Added property:

```
public virtual Android.Graphics.Rect CropRect { get; set; }
```

### Type Changed: Android.Media.MediaCodec

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecBufferFlags enum directly instead of this field.")]
	public static const MediaCodecBufferFlags BufferFlagKeyFrame;
```

Added property:

```
public MediaFormat InputFormat { get; }
```

Added methods:

```
public Java.Nio.ByteBuffer GetInputBuffer (int index);
	public Image GetInputImage (int index);
	public Java.Nio.ByteBuffer GetOutputBuffer (int index);
	public MediaFormat GetOutputFormat (int index);
	public Image GetOutputImage (int index);
	public void ReleaseOutputBuffer (int index, long renderTimestampNs);
	public void Reset ();
	public void SetCallback (MediaCodec.Callback cb);
```

### Type Changed: Android.Media.MediaCodec.CryptoException

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecCryptoErrorType enum directly instead of this field.")]
	public static const MediaCodecCryptoErrorType ErrorInsufficientOutputProtection;
```

### New Type Android.Media.Callback

```
public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected MediaCodec (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MediaCodec ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnError (MediaCodec codec, MediaCodec.CodecException e);
	public virtual void OnInputBufferAvailable (MediaCodec codec, int index);
	public virtual void OnOutputBufferAvailable (MediaCodec codec, int index, MediaCodec.BufferInfo info);
	public virtual void OnOutputFormatChanged (MediaCodec codec, MediaFormat format);
}
```

### New Type Android.Media.CodecException

```
public sealed class CodecException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// properties
	public string DiagnosticInfo { get; }
	public bool IsRecoverable { get; }
	public bool IsTransient { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### Type Changed: Android.Media.MediaCodecBufferFlags

Added value:

```
KeyFrame = 1,
```

### Type Changed: Android.Media.MediaCodecCapabilities

Added value:

```
Formatyuv420flexible = 2135033992,
```

### Type Changed: Android.Media.MediaCodecCryptoErrorType

Added value:

```
InsufficientOutputProtection = 4,
```

### Type Changed: Android.Media.MediaCodecInfo

### Type Changed: Android.Media.MediaCodecInfo.CodecCapabilities

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecCapabilities enum directly instead of this field.")]
	public static const MediaCodecCapabilities COLORFormatYUV420Flexible;
	public static const string FEATURESecurePlayback = "secure-playback";
	public static const string FEATURETunneledPlayback = "tunneled-playback";
```

Added properties:

```
public MediaCodecInfo.AudioCapabilities AudioCapabilities { get; }
	public MediaFormat DefaultFormat { get; }
	public MediaCodecInfo.EncoderCapabilities EncoderCapabilities { get; }
	public string MimeType { get; }
	public MediaCodecInfo.VideoCapabilities VideoCapabilities { get; }
```

Added methods:

```
public static MediaCodecInfo.CodecCapabilities CreateFromProfileLevel (string mime, MediaCodecProfileLevel profile, int level);
	public bool IsFeatureRequired (string name);
	public bool IsFormatSupported (MediaFormat format);
```

### Type Changed: Android.Media.MediaCodecInfo.CodecProfileLevel

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel AVCLevel52;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel1;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel2;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel21;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel3;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel31;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel4;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel41;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel5;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel51;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel52;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel6;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel61;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCHighTierLevel62;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel1;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel2;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel21;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel3;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel31;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel4;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel41;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel5;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel51;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel52;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel6;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel61;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileLevel enum directly instead of this field.")]
	public static const MediaCodecProfileLevel HEVCMainTierLevel62;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileType enum directly instead of this field.")]
	public static const MediaCodecProfileType HEVCProfileMain;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaCodecProfileType enum directly instead of this field.")]
	public static const MediaCodecProfileType HEVCProfileMain10;
```

### New Type Android.Media.AudioCapabilities

```
public sealed class AudioCapabilities : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public Android.Util.Range BitrateRange { get; }
	public int MaxInputChannelCount { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public Android.Util.Range[] GetSupportedSampleRateRanges ();
	public int[] GetSupportedSampleRates ();
	public bool IsSampleRateSupported (int sampleRate);
}
```

### New Type Android.Media.EncoderCapabilities

```
public sealed class EncoderCapabilities : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public Android.Util.Range ComplexityRange { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public bool IsBitrateModeSupported (BitrateMode mode);
}
```

### New Type Android.Media.VideoCapabilities

```
public sealed class VideoCapabilities : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public Android.Util.Range BitrateRange { get; }
	public int HeightAlignment { get; }
	public Android.Util.Range SupportedFrameRates { get; }
	public Android.Util.Range SupportedHeights { get; }
	public Android.Util.Range SupportedWidths { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int WidthAlignment { get; }
	// methods
	public bool AreSizeAndRateSupported (int width, int height, double frameRate);
	public Android.Util.Range GetSupportedFrameRatesFor (int width, int height);
	public Android.Util.Range GetSupportedHeightsFor (int width);
	public Android.Util.Range GetSupportedWidthsFor (int height);
	public bool IsSizeSupported (int width, int height);
}
```

### Type Changed: Android.Media.MediaCodecList

Added constructor:

```
public MediaCodecList (MediaCodecListKind kind);
```

Obsoleted property:

```
[Obsolete ("deprecated")]
	public static int CodecCount { get; }
```

Added methods:

```
public string FindDecoderForFormat (MediaFormat format);
	public string FindEncoderForFormat (MediaFormat format);
	public MediaCodecInfo[] GetCodecInfos ();
```

### Type Changed: Android.Media.MediaCodecProfileLevel

Added values:

```
Avclevel52 = 65536,
	Hevchightierlevel1 = 2,
	Hevchightierlevel2 = 8,
	Hevchightierlevel21 = 32,
	Hevchightierlevel3 = 128,
	Hevchightierlevel31 = 512,
	Hevchightierlevel4 = 2048,
	Hevchightierlevel41 = 8192,
	Hevchightierlevel5 = 32768,
	Hevchightierlevel51 = 131072,
	Hevchightierlevel52 = 524288,
	Hevchightierlevel6 = 2097152,
	Hevchightierlevel61 = 8388608,
	Hevchightierlevel62 = 33554432,
	Hevcmaintierlevel1 = 1,
	Hevcmaintierlevel2 = 4,
	Hevcmaintierlevel21 = 16,
	Hevcmaintierlevel3 = 64,
	Hevcmaintierlevel31 = 256,
	Hevcmaintierlevel4 = 1024,
	Hevcmaintierlevel41 = 4096,
	Hevcmaintierlevel5 = 16384,
	Hevcmaintierlevel51 = 65536,
	Hevcmaintierlevel52 = 262144,
	Hevcmaintierlevel6 = 1048576,
	Hevcmaintierlevel61 = 4194304,
	Hevcmaintierlevel62 = 16777216,
```

### Type Changed: Android.Media.MediaCodecProfileType

Added values:

```
Hevcprofilemain = 1,
	Hevcprofilemain10 = 2,
```

### Type Changed: Android.Media.MediaDrm

### New Type Android.Media.MediaDrmStateException

```
public sealed class MediaDrmStateException : Java.Lang.IllegalStateException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// properties
	public string DiagnosticInfo { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### Type Changed: Android.Media.MediaFormat

Added fields:

```
public static const string KeyAacDrcAttenuationFactor = "aac-drc-cut-level";
	public static const string KeyAacDrcBoostFactor = "aac-drc-boost-level";
	public static const string KeyAacDrcHeavyCompression = "aac-drc-heavy-compression";
	public static const string KeyAacDrcTargetReferenceLevel = "aac-target-ref-level";
	public static const string KeyAacEncodedTargetLevel = "aac-encoded-target-level";
	public static const string KeyAacMaxOutputChannelCount = "aac-max-output-channel_count";
	public static const string KeyAacSbrMode = "aac-sbr-mode";
	public static const string KeyAudioSessionId = "audio-session-id";
	public static const string KeyBitrateMode = "bitrate-mode";
	public static const string KeyCaptureRate = "capture-rate";
	public static const string KeyComplexity = "complexity";
	public static const string KeyProfile = "profile";
	public static const string KeyTemporalLayering = "ts-schema";
	public static const string MimetypeAudioAac = "audio/mp4a-latm";
	public static const string MimetypeAudioAc3 = "audio/ac3";
	public static const string MimetypeAudioAmrNb = "audio/3gpp";
	public static const string MimetypeAudioAmrWb = "audio/amr-wb";
	public static const string MimetypeAudioFlac = "audio/flac";
	public static const string MimetypeAudioG711Alaw = "audio/g711-alaw";
	public static const string MimetypeAudioG711Mlaw = "audio/g711-mlaw";
	public static const string MimetypeAudioMpeg = "audio/mpeg";
	public static const string MimetypeAudioMsgsm = "audio/gsm";
	public static const string MimetypeAudioOpus = "audio/opus";
	public static const string MimetypeAudioQcelp = "audio/qcelp";
	public static const string MimetypeAudioRaw = "audio/raw";
	public static const string MimetypeAudioVorbis = "audio/vorbis";
	public static const string MimetypeTextCea608 = "text/cea-608";
	public static const string MimetypeTextVtt = "text/vtt";
	public static const string MimetypeVideoAvc = "video/avc";
	public static const string MimetypeVideoH263 = "video/3gpp";
	public static const string MimetypeVideoHevc = "video/hevc";
	public static const string MimetypeVideoMpeg2 = "video/mpeg2";
	public static const string MimetypeVideoMpeg4 = "video/mp4v-es";
	public static const string MimetypeVideoRaw = "video/raw";
	public static const string MimetypeVideoVp8 = "video/x-vnd.on2.vp8";
	public static const string MimetypeVideoVp9 = "video/x-vnd.on2.vp9";
```

Added methods:

```
public bool GetFeatureEnabled (string feature);
	public void SetFeatureEnabled (string feature, bool enabled);
```

### Type Changed: Android.Media.MediaMuxer

### Type Changed: Android.Media.MediaMuxer.OutputFormat

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MuxerOutputType enum directly instead of this field.")]
	public static const MuxerOutputType MuxerOutputWebm;
```

### Type Changed: Android.Media.MediaPlayer

Removed method:

```
public virtual void AddTimedTextSource (Java.IO.FileDescriptor fd, long offset, long length, string mimeType);
```

Added methods:

```
public virtual void AddTimedTextSource (Java.IO.FileDescriptor fd, long offset, long length, string mime);
	public static MediaPlayer Create (Android.Content.Context context, int resid, AudioAttributes audioAttributes, int audioSessionId);
	public static MediaPlayer Create (Android.Content.Context context, Android.Net.Uri uri, Android.Views.ISurfaceHolder holder, AudioAttributes audioAttributes, int audioSessionId);
	public virtual int GetSelectedTrack (MediaTrackType trackType);
	public virtual void SetAudioAttributes (AudioAttributes attributes);
```

### Type Changed: Android.Media.MediaPlayer.TrackInfo

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.MediaTrackType enum directly instead of this field.")]
	public static const MediaTrackType MediaTrackTypeSubtitle;
```

### Type Changed: Android.Media.MediaRecorder

Added property:

```
public virtual Android.Views.Surface Surface { get; }
```

### Type Changed: Android.Media.MediaTrackType

Added value:

```
Subtitle = 4,
```

### Type Changed: Android.Media.MuxerOutputType

Added value:

```
Webm = 1,
```

### Type Changed: Android.Media.OutputFormat

Added value:

```
Webm = 9,
```

### Type Changed: Android.Media.Rating

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Media.RatingStyle enum directly instead of this field.")]
	public static const RatingStyle RatingNone;
```

### Type Changed: Android.Media.RatingStyle

Added value:

```
None = 0,
```

### Type Changed: Android.Media.RemoteControlClient

Added property:

```
public virtual Session.MediaSession MediaSession { get; }
```

### Type Changed: Android.Media.Ringtone

Added property:

```
public virtual AudioAttributes AudioAttributes { get; set; }
```

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual Stream StreamType { get; set; }
```

### Type Changed: Android.Media.SoundPool

### New Type Android.Media.Builder

```
public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected SoundPool (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SoundPool ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual SoundPool Build ();
	public virtual SoundPool.Builder SetAudioAttributes (AudioAttributes attributes);
	public virtual SoundPool.Builder SetMaxStreams (int maxStreams);
}
```

### Type Changed: Android.Media.VideoEncoder

Added value:

```
Vp8 = 4,
```

### Type Changed: Android.Media.VideoSource

Added value:

```
Surface = 2,
```

### New Type Android.Media.AudioAttributes

```
public sealed class AudioAttributes : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public AudioContentType ContentType { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public AudioFlags Flags { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected AudioAttributes (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public AudioAttributes ();
		public AudioAttributes (AudioAttributes aa);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual AudioAttributes Build ();
		public virtual AudioAttributes.Builder SetContentType (AudioContentType contentType);
		public virtual AudioAttributes.Builder SetFlags (AudioFlags flags);
		public virtual AudioAttributes.Builder SetLegacyStreamType (Stream streamType);
	}
}
```

### New Type Android.Media.AudioContentType

```
[Serializable]
public enum AudioContentType {
	Movie = 3,
	Music = 2,
	Sonification = 4,
	Speech = 1,
	Unknown = 0,
}
```

### New Type Android.Media.AudioUsageKind

```
[Serializable]
public enum AudioUsageKind {
	Alarm = 4,
	AssistanceAccessibility = 11,
	AssistanceNavigationGuidance = 12,
	AssistanceSonification = 13,
	Game = 14,
	Media = 1,
	Notification = 5,
	NotificationCommunicationDelayed = 9,
	NotificationCommunicationInstant = 8,
	NotificationCommunicationRequest = 7,
	NotificationEvent = 10,
	NotificationRingtone = 6,
	Unknown = 0,
	VoiceCommunication = 2,
	VoiceCommunicationSignalling = 3,
}
```

### New Type Android.Media.BitrateMode

```
[Serializable]
public enum BitrateMode {
	Cbr = 2,
	Cq = 0,
	Vbr = 1,
}
```

### New Type Android.Media.MediaCodecListKind

```
[Serializable]
public enum MediaCodecListKind {
	AllCodecs = 1,
	RegularCodecs = 0,
}
```

### New Type Android.Media.MediaDescription

```
public class MediaDescription : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected MediaDescription (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public string Description { get; }
	public virtual Java.Lang.ICharSequence DescriptionFormatted { get; }
	public virtual Android.OS.Bundle Extras { get; }
	public virtual Android.Graphics.Bitmap IconBitmap { get; }
	public virtual Android.Net.Uri IconUri { get; }
	public virtual string MediaId { get; }
	public string Subtitle { get; }
	public virtual Java.Lang.ICharSequence SubtitleFormatted { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public string Title { get; }
	public virtual Java.Lang.ICharSequence TitleFormatted { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MediaDescription (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MediaDescription ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual MediaDescription Build ();
		public virtual MediaDescription.Builder SetDescription (Java.Lang.ICharSequence description);
		public MediaDescription.Builder SetDescription (string description);
		public virtual MediaDescription.Builder SetExtras (Android.OS.Bundle extras);
		public virtual MediaDescription.Builder SetIconBitmap (Android.Graphics.Bitmap icon);
		public virtual MediaDescription.Builder SetIconUri (Android.Net.Uri iconUri);
		public virtual MediaDescription.Builder SetMediaId (string mediaId);
		public virtual MediaDescription.Builder SetSubtitle (Java.Lang.ICharSequence subtitle);
		public MediaDescription.Builder SetSubtitle (string subtitle);
		public virtual MediaDescription.Builder SetTitle (Java.Lang.ICharSequence title);
		public MediaDescription.Builder SetTitle (string title);
	}
}
```

### New Type Android.Media.MediaMetadata

```
public sealed class MediaMetadata : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields
	public static const string MetadataKeyAlbum = "android.media.metadata.ALBUM";
	public static const string MetadataKeyAlbumArt = "android.media.metadata.ALBUM_ART";
	public static const string MetadataKeyAlbumArtist = "android.media.metadata.ALBUM_ARTIST";
	public static const string MetadataKeyAlbumArtUri = "android.media.metadata.ALBUM_ART_URI";
	public static const string MetadataKeyArt = "android.media.metadata.ART";
	public static const string MetadataKeyArtist = "android.media.metadata.ARTIST";
	public static const string MetadataKeyArtUri = "android.media.metadata.ART_URI";
	public static const string MetadataKeyAuthor = "android.media.metadata.AUTHOR";
	public static const string MetadataKeyCompilation = "android.media.metadata.COMPILATION";
	public static const string MetadataKeyComposer = "android.media.metadata.COMPOSER";
	public static const string MetadataKeyDate = "android.media.metadata.DATE";
	public static const string MetadataKeyDiscNumber = "android.media.metadata.DISC_NUMBER";
	public static const string MetadataKeyDisplayDescription = "android.media.metadata.DISPLAY_DESCRIPTION";
	public static const string MetadataKeyDisplayIcon = "android.media.metadata.DISPLAY_ICON";
	public static const string MetadataKeyDisplayIconUri = "android.media.metadata.DISPLAY_ICON_URI";
	public static const string MetadataKeyDisplaySubtitle = "android.media.metadata.DISPLAY_SUBTITLE";
	public static const string MetadataKeyDisplayTitle = "android.media.metadata.DISPLAY_TITLE";
	public static const string MetadataKeyDuration = "android.media.metadata.DURATION";
	public static const string MetadataKeyGenre = "android.media.metadata.GENRE";
	public static const string MetadataKeyMediaId = "android.media.metadata.MEDIA_ID";
	public static const string MetadataKeyNumTracks = "android.media.metadata.NUM_TRACKS";
	public static const string MetadataKeyRating = "android.media.metadata.RATING";
	public static const string MetadataKeyTitle = "android.media.metadata.TITLE";
	public static const string MetadataKeyTrackNumber = "android.media.metadata.TRACK_NUMBER";
	public static const string MetadataKeyUserRating = "android.media.metadata.USER_RATING";
	public static const string MetadataKeyWriter = "android.media.metadata.WRITER";
	public static const string MetadataKeyYear = "android.media.metadata.YEAR";
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public MediaDescription Description { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public bool ContainsKey (string key);
	public virtual int DescribeContents ();
	public Android.Graphics.Bitmap GetBitmap (string key);
	public long GetLong (string key);
	public Rating GetRating (string key);
	public string GetString (string key);
	public string GetText (string key);
	public Java.Lang.ICharSequence GetTextFormatted (string key);
	public System.Collections.Generic.ICollection<string> KeySet ();
	public int Size ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public MediaMetadata ();
		public MediaMetadata (MediaMetadata source);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public MediaMetadata Build ();
		public MediaMetadata.Builder PutBitmap (string key, Android.Graphics.Bitmap value);
		public MediaMetadata.Builder PutLong (string key, long value);
		public MediaMetadata.Builder PutRating (string key, Rating value);
		public MediaMetadata.Builder PutString (string key, string value);
		public MediaMetadata.Builder PutText (string key, Java.Lang.ICharSequence value);
		public MediaMetadata.Builder PutText (string key, string value);
	}
}
```

### New Type Android.Media.VolumeControl

```
[Serializable]
public enum VolumeControl {
	Absolute = 2,
	Fixed = 0,
	Relative = 1,
}
```

### New Type Android.Media.VolumeProvider

```
public abstract class VolumeProvider : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected VolumeProvider (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public int CurrentVolume { get; set; }
	public int MaxVolume { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnAdjustVolume (Adjust direction);
	public virtual void OnSetVolumeTo (int volume);
}
```

### New Type Android.Media.WriteMode

```
[Serializable]
public enum WriteMode {
	Blocking = 0,
	NonBlocking = 1,
}
```

## Namespace Android.Media.Audiofx

### Type Changed: Android.Media.Audiofx.Virtualizer

Added property:

```
public virtual VirtualizationMode VirtualizationMode { get; }
```

Added methods:

```
public virtual bool CanVirtualize (Android.Media.ChannelIn inputChannelMask, VirtualizationMode virtualizationMode);
	public virtual bool ForceVirtualizationMode (VirtualizationMode virtualizationMode);
	public virtual bool GetSpeakerAngles (Android.Media.ChannelIn inputChannelMask, VirtualizationMode virtualizationMode, int[] angles);
```

### New Type Android.Media.Audiofx.VirtualizationMode

```
[Serializable]
public enum VirtualizationMode {
	Auto = 1,
	Binaural = 2,
	Off = 0,
	Transaural = 3,
}
```

## Namespace Android.Media.Browse

### Type Changed: Android.Media.Browse.MediaItemFlags

Added values:

```
Browsable = 1,
	Playable = 2,
```

### New Type Android.Media.Browse.MediaBrowser

```
public sealed class MediaBrowser : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MediaBrowser (Android.Content.Context context, Android.Content.ComponentName serviceComponent, MediaBrowser.ConnectionCallback callback, Android.OS.Bundle rootHints);
	// properties
	public Android.OS.Bundle Extras { get; }
	public bool IsConnected { get; }
	public string Root { get; }
	public Android.Content.ComponentName ServiceComponent { get; }
	public Android.Media.Session.MediaSession.Token SessionToken { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void Connect ();
	public void Disconnect ();
	public void Subscribe (string parentId, MediaBrowser.SubscriptionCallback callback);
	public void Unsubscribe (string parentId);

	// inner types
	public class ConnectionCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MediaBrowser (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MediaBrowser ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnConnected ();
		public virtual void OnConnectionFailed ();
		public virtual void OnConnectionSuspended ();
	}
	public class MediaItem : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		protected MediaBrowser (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MediaBrowser (Android.Media.MediaDescription description, MediaItemFlags flags);
		// properties
		public static Android.OS.IParcelableCreator Creator { get; set; }
		public virtual Android.Media.MediaDescription Description { get; }
		public virtual MediaItemFlags Flags { get; }
		public virtual bool IsBrowsable { get; }
		public virtual bool IsPlayable { get; }
		public virtual string MediaId { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual int DescribeContents ();
		public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const int ContentsFileDescriptor;

			[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
		}
	}
	public abstract class SubscriptionCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MediaBrowser (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MediaBrowser ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnChildrenLoaded (string parentId, System.Collections.Generic.IList<MediaBrowser.MediaItem> children);
		public virtual void OnError (string id);
	}
}
```

## Namespace Android.Media.Session

### Type Changed: Android.Media.Session.MediaSessionFlags

Added values:

```
HandlesMediaButtons = 1,
	HandlesTransportControls = 2,
```

### New Type Android.Media.Session.MediaController

```
public sealed class MediaController : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MediaController (Android.Content.Context context, MediaSession.Token token);
	// properties
	public Android.OS.Bundle Extras { get; }
	public long Flags { get; }
	public Android.Media.MediaMetadata Metadata { get; }
	public string PackageName { get; }
	public PlaybackState PlaybackState { get; }
	public System.Collections.Generic.IList<MediaSession.QueueItem> Queue { get; }
	public string QueueTitle { get; }
	public Java.Lang.ICharSequence QueueTitleFormatted { get; }
	public Android.Media.RatingStyle RatingType { get; }
	public Android.App.PendingIntent SessionActivity { get; }
	public MediaSession.Token SessionToken { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void AdjustVolume (Android.Media.Adjust direction, Android.Media.AudioFlags flags);
	public bool DispatchMediaButtonEvent (Android.Views.KeyEvent keyEvent);
	public MediaController.PlaybackInfo GetPlaybackInfo ();
	public MediaController.TransportControls GetTransportControls ();
	public void RegisterCallback (MediaController.Callback callback, Android.OS.Handler handler);
	public void RegisterCallback (MediaController.Callback callback);
	public void SendCommand (string command, Android.OS.Bundle args, Android.OS.ResultReceiver cb);
	public void SetVolumeTo (int value, Android.Media.AudioFlags flags);
	public void UnregisterCallback (MediaController.Callback callback);

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MediaController (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MediaController ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnAudioInfoChanged (MediaController.PlaybackInfo info);
		public virtual void OnExtrasChanged (Android.OS.Bundle extras);
		public virtual void OnMetadataChanged (Android.Media.MediaMetadata metadata);
		public virtual void OnPlaybackStateChanged (PlaybackState state);
		public virtual void OnQueueChanged (System.Collections.Generic.IList<MediaSession.QueueItem> queue);
		public virtual void OnQueueTitleChanged (Java.Lang.ICharSequence title);
		public void OnQueueTitleChanged (string title);
		public virtual void OnSessionDestroyed ();
		public virtual void OnSessionEvent (string e, Android.OS.Bundle extras);
	}
	public sealed class PlaybackInfo : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// properties
		public Android.Media.AudioAttributes AudioAttributes { get; }
		public int CurrentVolume { get; }
		public int MaxVolume { get; }
		public Android.Media.MediaPlaybackType PlaybackType { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
	public sealed class TransportControls : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public void FastForward ();
		public void Pause ();
		public void Play ();
		public void PlayFromMediaId (string mediaId, Android.OS.Bundle extras);
		public void PlayFromSearch (string query, Android.OS.Bundle extras);
		public void Rewind ();
		public void SeekTo (long pos);
		public void SendCustomAction (PlaybackState.CustomAction customAction, Android.OS.Bundle args);
		public void SendCustomAction (string action, Android.OS.Bundle args);
		public void SetRating (Android.Media.Rating rating);
		public void SkipToNext ();
		public void SkipToPrevious ();
		public void SkipToQueueItem (long id);
		public void Stop ();
	}
}
```

### New Type Android.Media.Session.MediaPlaybackType

```
[Serializable]
public enum MediaPlaybackType {
	Local = 1,
	Remote = 2,
}
```

### New Type Android.Media.Session.MediaSession

```
public sealed class MediaSession : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MediaSession (Android.Content.Context context, string tag);
	// fields

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.MediaSessionFlags enum directly instead of this field.")]
	public static const MediaSessionFlags FlagHandlesMediaButtons;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.MediaSessionFlags enum directly instead of this field.")]
	public static const MediaSessionFlags FlagHandlesTransportControls;
	// properties
	public bool Active { get; set; }
	public MediaController Controller { get; }
	public MediaSession.Token SessionToken { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void Release ();
	public void SendSessionEvent (string e, Android.OS.Bundle extras);
	public void SetCallback (MediaSession.Callback callback, Android.OS.Handler handler);
	public void SetCallback (MediaSession.Callback callback);
	public void SetExtras (Android.OS.Bundle extras);
	public void SetFlags (MediaSessionFlags flags);
	public void SetMediaButtonReceiver (Android.App.PendingIntent mbr);
	public void SetMetadata (Android.Media.MediaMetadata metadata);
	public void SetPlaybackState (PlaybackState state);
	public void SetPlaybackToLocal (Android.Media.AudioAttributes attributes);
	public void SetPlaybackToRemote (Android.Media.VolumeProvider volumeProvider);
	public void SetQueue (System.Collections.Generic.IList<MediaSession.QueueItem> queue);
	public void SetQueueTitle (Java.Lang.ICharSequence title);
	public void SetQueueTitle (string title);
	public void SetSessionActivity (Android.App.PendingIntent pi);

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MediaSession (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MediaSession ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnCommand (string command, Android.OS.Bundle args, Android.OS.ResultReceiver cb);
		public virtual void OnCustomAction (string action, Android.OS.Bundle extras);
		public virtual void OnFastForward ();
		public virtual bool OnMediaButtonEvent (Android.Content.Intent mediaButtonIntent);
		public virtual void OnPause ();
		public virtual void OnPlay ();
		public virtual void OnPlayFromMediaId (string mediaId, Android.OS.Bundle extras);
		public virtual void OnPlayFromSearch (string query, Android.OS.Bundle extras);
		public virtual void OnRewind ();
		public virtual void OnSeekTo (long pos);
		public virtual void OnSetRating (Android.Media.Rating rating);
		public virtual void OnSkipToNext ();
		public virtual void OnSkipToPrevious ();
		public virtual void OnSkipToQueueItem (long id);
		public virtual void OnStop ();
	}
	public sealed class QueueItem : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		public MediaSession (Android.Media.MediaDescription description, long id);
		// fields
		public static const int UnknownId;
		// properties
		public static Android.OS.IParcelableCreator Creator { get; set; }
		public Android.Media.MediaDescription Description { get; }
		public long QueueId { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual int DescribeContents ();
		public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const int ContentsFileDescriptor;

			[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
		}
	}
	public sealed class Token : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
		// properties
		public static Android.OS.IParcelableCreator Creator { get; set; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual int DescribeContents ();
		public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const int ContentsFileDescriptor;

			[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
		}
	}
}
```

### New Type Android.Media.Session.MediaSessionManager

```
public sealed class MediaSessionManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void AddOnActiveSessionsChangedListener (MediaSessionManager.IOnActiveSessionsChangedListener sessionListener, Android.Content.ComponentName notificationListener);
	public void AddOnActiveSessionsChangedListener (MediaSessionManager.IOnActiveSessionsChangedListener sessionListener, Android.Content.ComponentName notificationListener, Android.OS.Handler handler);
	public System.Collections.Generic.IList<MediaController> GetActiveSessions (Android.Content.ComponentName notificationListener);
	public void RemoveOnActiveSessionsChangedListener (MediaSessionManager.IOnActiveSessionsChangedListener listener);

	// inner types
	public interface IOnActiveSessionsChangedListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual void OnActiveSessionsChanged (System.Collections.Generic.IList<MediaController> controllers);
	}
	public class ActiveSessionsChangedEventArgs : System.EventArgs {
		// constructors
		public MediaSessionManager (System.Collections.Generic.IList<MediaController> controllers);
		// properties
		public System.Collections.Generic.IList<MediaController> Controllers { get; }
	}
}
```

### New Type Android.Media.Session.PlaybackState

```
public sealed class PlaybackState : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields
	public static const long ActionFastForward;
	public static const long ActionPause;
	public static const long ActionPlay;
	public static const long ActionPlayFromMediaId;
	public static const long ActionPlayFromSearch;
	public static const long ActionPlayPause;
	public static const long ActionRewind;
	public static const long ActionSeekTo;
	public static const long ActionSetRating;
	public static const long ActionSkipToNext;
	public static const long ActionSkipToPrevious;
	public static const long ActionSkipToQueueItem;
	public static const long ActionStop;
	public static const long PlaybackPositionUnknown;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateBuffering;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateConnecting;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateError;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateFastForwarding;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateNone;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StatePaused;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StatePlaying;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateRewinding;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateSkippingToNext;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateSkippingToPrevious;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateSkippingToQueueItem;

	[Obsolete ("This constant will be removed in the future version. Use Android.Media.Session.PlaybackStateCode enum directly instead of this field.")]
	public static const PlaybackStateCode StateStopped;
	// properties
	public long Actions { get; }
	public long ActiveQueueItemId { get; }
	public long BufferedPosition { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public System.Collections.Generic.IList<PlaybackState.CustomAction> CustomActions { get; }
	public string ErrorMessage { get; }
	public Java.Lang.ICharSequence ErrorMessageFormatted { get; }
	public long LastPositionUpdateTime { get; }
	public float PlaybackSpeed { get; }
	public long Position { get; }
	public PlaybackStateCode State { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public PlaybackState ();
		public PlaybackState (PlaybackState from);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public PlaybackState.Builder AddCustomAction (PlaybackState.CustomAction customAction);
		public PlaybackState.Builder AddCustomAction (string action, string name, int icon);
		public PlaybackState Build ();
		public PlaybackState.Builder SetActions (long actions);
		public PlaybackState.Builder SetActiveQueueItemId (long id);
		public PlaybackState.Builder SetBufferedPosition (long bufferedPosition);
		public PlaybackState.Builder SetErrorMessage (Java.Lang.ICharSequence error);
		public PlaybackState.Builder SetErrorMessage (string error);
		public PlaybackState.Builder SetState (PlaybackStateCode state, long position, float playbackSpeed);
		public PlaybackState.Builder SetState (PlaybackStateCode state, long position, float playbackSpeed, long updateTime);
	}
	public sealed class CustomAction : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
		// properties
		public string Action { get; }
		public static Android.OS.IParcelableCreator Creator { get; set; }
		public Android.OS.Bundle Extras { get; }
		public int Icon { get; }
		public string Name { get; }
		public Java.Lang.ICharSequence NameFormatted { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual int DescribeContents ();
		public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const int ContentsFileDescriptor;

			[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
			public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
		}
		public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
			// constructors
			public PlaybackState (string action, Java.Lang.ICharSequence name, int icon);
			public PlaybackState (string action, string name, int icon);
			// properties
			protected override System.IntPtr ThresholdClass { get; }
			protected override System.Type ThresholdType { get; }
			// methods
			public PlaybackState.CustomAction Build ();
			public PlaybackState.CustomAction.Builder SetExtras (Android.OS.Bundle extras);
		}
	}
}
```

### New Type Android.Media.Session.PlaybackStateCode

```
[Serializable]
public enum PlaybackStateCode {
	Buffering = 6,
	Connecting = 8,
	Error = 7,
	FastForwarding = 4,
	None = 0,
	Paused = 2,
	Playing = 3,
	Rewinding = 5,
	SkippingToNext = 10,
	SkippingToPrevious = 9,
	SkippingToQueueItem = 11,
	Stopped = 1,
}
```

## Namespace Android.Net

### Type Changed: Android.Net.ConnectivityManager

Added properties:

```
public virtual bool IsDefaultNetworkActive { get; }
	public static Network ProcessDefaultNetwork { get; }
```

Added event:

```
public event System.EventHandler DefaultNetworkActive;
```

Added methods:

```
public virtual void AddDefaultNetworkActiveListener (ConnectivityManager.IOnNetworkActiveListener l);
	public virtual Network[] GetAllNetworks ();
	public virtual LinkProperties GetLinkProperties (Network network);
	public virtual NetworkCapabilities GetNetworkCapabilities (Network network);
	public virtual NetworkInfo GetNetworkInfo (Network network);
	public virtual void RegisterNetworkCallback (NetworkRequest request, ConnectivityManager.NetworkCallback networkCallback);
	public virtual void RemoveDefaultNetworkActiveListener (ConnectivityManager.IOnNetworkActiveListener l);
	public virtual void ReportBadNetwork (Network network);
	public virtual void RequestNetwork (NetworkRequest request, ConnectivityManager.NetworkCallback networkCallback);
	public static bool SetProcessDefaultNetwork (Network network);
	public virtual void UnregisterNetworkCallback (ConnectivityManager.NetworkCallback networkCallback);
```

### Type Changed: Android.Net.ConnectivityType

Added value:

```
Vpn = 17,
```

### Type Changed: Android.Net.Proxy

Added field:

```
public static const string ExtraProxyInfo = "android.intent.extra.PROXY_INFO";
```

### Type Changed: Android.Net.VpnService

### Type Changed: Android.Net.VpnService.Builder

Added methods:

```
public virtual VpnService.Builder AddAllowedApplication (string packageName);
	public virtual VpnService.Builder AddDisallowedApplication (string packageName);
	public virtual VpnService.Builder AllowBypass ();
	public virtual VpnService.Builder AllowFamily (int family);
	public virtual VpnService.Builder SetBlocking (bool blocking);
```

### New Type Android.Net.IpPrefix

```
public sealed class IpPrefix : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public Java.Net.InetAddress Address { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public int PrefixLength { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public byte[] GetRawAddress ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Net.LinkAddress

```
public class LinkAddress : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected LinkAddress (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual Java.Net.InetAddress Address { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual int Flags { get; }
	public virtual int PrefixLength { get; }
	public virtual int Scope { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Net.LinkProperties

```
public sealed class LinkProperties : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public System.Collections.Generic.IList<Java.Net.InetAddress> DnsServers { get; }
	public string Domains { get; }
	public ProxyInfo HttpProxy { get; }
	public string InterfaceName { get; }
	public System.Collections.Generic.IList<LinkAddress> LinkAddresses { get; }
	public System.Collections.Generic.IList<RouteInfo> Routes { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Net.NetCapability

```
[Serializable]
public enum NetCapability {
	Cbs = 5,
	Dun = 2,
	Eims = 10,
	Fota = 3,
	Ia = 7,
	Ims = 4,
	Internet = 12,
	Mms = 0,
	NotMetered = 11,
	NotRestricted = 13,
	NotVpn = 15,
	Rcs = 8,
	Supl = 1,
	Trusted = 14,
	WifiP2p = 6,
	Xcap = 9,
}
```

### New Type Android.Net.Network

```
public class Network : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected Network (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual Javax.Net.SocketFactory SocketFactory { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void BindSocket (Java.Net.Socket socket);
	public virtual int DescribeContents ();
	public virtual Java.Net.InetAddress[] GetAllByName (string host);
	public virtual Java.Net.InetAddress GetByName (string host);
	public virtual Java.Net.URLConnection OpenConnection (Java.Net.URL url);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Net.NetworkCapabilities

```
public sealed class NetworkCapabilities : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public NetworkCapabilities (NetworkCapabilities nc);
	// fields

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityCbs;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityDun;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityEims;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityFota;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityIa;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityIms;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityInternet;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityMms;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityNotMetered;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityNotRestricted;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityNotVpn;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityRcs;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilitySupl;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityTrusted;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityWifiP2p;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.NetCapability enum directly instead of this field.")]
	public static const NetCapability NetCapabilityXcap;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.TransportType enum directly instead of this field.")]
	public static const TransportType TransportBluetooth;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.TransportType enum directly instead of this field.")]
	public static const TransportType TransportCellular;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.TransportType enum directly instead of this field.")]
	public static const TransportType TransportEthernet;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.TransportType enum directly instead of this field.")]
	public static const TransportType TransportVpn;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.TransportType enum directly instead of this field.")]
	public static const TransportType TransportWifi;
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public int LinkDownstreamBandwidthKbps { get; }
	public int LinkUpstreamBandwidthKbps { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public bool HasCapability (NetCapability capability);
	public bool HasTransport (TransportType transportType);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Net.NetworkRequest

```
public class NetworkRequest : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected NetworkRequest (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected NetworkRequest (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public NetworkRequest ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual NetworkRequest.Builder AddCapability (NetCapability capability);
		public virtual NetworkRequest.Builder AddTransportType (TransportType transportType);
		public virtual NetworkRequest Build ();
		public virtual NetworkRequest.Builder RemoveCapability (NetCapability capability);
		public virtual NetworkRequest.Builder RemoveTransportType (TransportType transportType);
		public virtual NetworkRequest.Builder SetNetworkSpecifier (string networkSpecifier);
	}
}
```

### New Type Android.Net.ProxyInfo

```
public class ProxyInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ProxyInfo (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual string Host { get; }
	public virtual Uri PacFileUrl { get; }
	public virtual int Port { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static ProxyInfo BuildDirectProxy (string host, int port);
	public static ProxyInfo BuildDirectProxy (string host, int port, System.Collections.Generic.IList<string> exclList);
	public static ProxyInfo BuildPacProxy (Uri pacUri);
	public virtual int DescribeContents ();
	public virtual string[] GetExclusionList ();
	public virtual void WriteToParcel (Android.OS.Parcel p0, Android.OS.ParcelableWriteFlags p1);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Net.PskKeyManager

```
public abstract class PskKeyManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected PskKeyManager (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PskKeyManager ();
	// fields
	public static const int MaxIdentityHintLengthBytes;
	public static const int MaxIdentityLengthBytes;
	public static const int MaxKeyLengthBytes;
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual string ChooseClientKeyIdentity (string identityHint, Java.Net.Socket socket);
	public virtual string ChooseClientKeyIdentity (string identityHint, Javax.Net.Ssl.SSLEngine engine);
	public virtual string ChooseServerKeyIdentityHint (Java.Net.Socket socket);
	public virtual string ChooseServerKeyIdentityHint (Javax.Net.Ssl.SSLEngine engine);
	public virtual Javax.Crypto.ISecretKey GetKey (string identityHint, string identity, Java.Net.Socket socket);
	public virtual Javax.Crypto.ISecretKey GetKey (string identityHint, string identity, Javax.Net.Ssl.SSLEngine engine);
}
```

### New Type Android.Net.RouteInfo

```
public sealed class RouteInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public IpPrefix Destination { get; }
	public Java.Net.InetAddress Gateway { get; }
	public string Interface { get; }
	public bool IsDefaultRoute { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public bool Matches (Java.Net.InetAddress destination);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Net.TransportType

```
[Serializable]
public enum TransportType {
	Bluetooth = 2,
	Cellular = 0,
	Ethernet = 3,
	Vpn = 4,
	Wifi = 1,
}
```

## Namespace Android.Net.Http

### Type Changed: Android.Net.Http.X509TrustManagerExtensions

Added method:

```
public virtual bool IsUserAddedCertificate (Java.Security.Cert.X509Certificate cert);
```

## Namespace Android.Net.Nsd

### Type Changed: Android.Net.Nsd.NsdServiceInfo

Added property:

```
public System.Collections.Generic.IDictionary<System.String,System.Byte[]> Attributes { get; }
```

Added methods:

```
public void RemoveAttribute (string key);
	public void SetAttribute (string key, string value);
```

## Namespace Android.Net.Wifi

### Type Changed: Android.Net.Wifi.WifiConfiguration

Added property:

```
public string Fqdn { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiEapMethod

Added values:

```
Aka = 5,
	Sim = 4,
```

### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig

### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig.Eap

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Net.Wifi.WifiEapMethod enum directly instead of this field.")]
	public static const WifiEapMethod Aka;

	[Obsolete ("This constant will be removed in the future version. Use Android.Net.Wifi.WifiEapMethod enum directly instead of this field.")]
	public static const WifiEapMethod Sim;
```

### Type Changed: Android.Net.Wifi.WifiInfo

Added field:

```
public static const string FrequencyUnits = "MHz";
```

Added property:

```
public virtual int Frequency { get; }
```

### Type Changed: Android.Net.Wifi.WifiManager

Added properties:

```
public virtual bool IsDeviceToApRttSupported { get; }
	public virtual bool IsEnhancedPowerReportingSupported { get; }
	public virtual bool IsP2pSupported { get; }
	public virtual bool IsPreferredNetworkOffloadSupported { get; }
	public virtual bool IsTdlsSupported { get; }
```

Added methods:

```
public virtual void CancelWps (WifiManager.WpsCallback listener);
	public virtual bool Is5GHzBandSupported ();
	public virtual void StartWps (WpsInfo config, WifiManager.WpsCallback listener);
```

### New Type Android.Net.Wifi.WpsCallback

```
public abstract class WpsCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WifiManager (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WifiManager ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnStarted (string pin);
	public virtual void OnSucceeded ();
}
```

### Type Changed: Android.Net.Wifi.WpsInfo

Added property:

```
public string Bssid { get; set; }
```

### New Type Android.Net.Wifi.WpsFailureReason

```
[Serializable]
public enum WpsFailureReason {
	AuthFailure = 6,
	OverlapError = 3,
	TimedOut = 7,
	TkipOnlyProhibited = 5,
	WepProhibited = 4,
}
```

## Namespace Android.Nfc

### Type Changed: Android.Nfc.NdefRecord

Added method:

```
public static NdefRecord CreateTextRecord (string languageCode, string text);
```

### Type Changed: Android.Nfc.NfcAdapter

Added method:

```
public bool InvokeBeam (Android.App.Activity activity);
```

## Namespace Android.Nfc.CardEmulators

### Type Changed: Android.Nfc.CardEmulators.CardEmulation

Added methods:

```
public bool CategoryAllowsForegroundPreference (string category);
	public System.Collections.Generic.IList<string> GetAidsForService (Android.Content.ComponentName service, string category);
	public bool RegisterAidsForService (Android.Content.ComponentName service, string category, System.Collections.Generic.IList<string> aids);
	public bool RemoveAidsForService (Android.Content.ComponentName service, string category);
	public bool SetPreferredService (Android.App.Activity activity, Android.Content.ComponentName service);
	public bool SupportsAidPrefixRegistration ();
	public bool UnsetPreferredService (Android.App.Activity activity);
```

## Namespace Android.Opengl

### Type Changed: Android.Opengl.EGLObjectHandle

Added constructor:

```
protected EGLObjectHandle (long handle);
```

Added property:

```
public virtual long NativeHandle { get; }
```

### New Type Android.Opengl.GLES31

```
public class GLES31 : Android.Opengl.GLES30, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected GLES31 (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const int GlActiveAtomicCounterBuffers;
	public static const int GlActiveProgram;
	public static const int GlActiveResources;
	public static const int GlActiveVariables;
	public static const int GlAllShaderBits;
	public static const int GlArraySize;
	public static const int GlArrayStride;
	public static const int GlAtomicCounterBarrierBit;
	public static const int GlAtomicCounterBuffer;
	public static const int GlAtomicCounterBufferBinding;
	public static const int GlAtomicCounterBufferIndex;
	public static const int GlAtomicCounterBufferSize;
	public static const int GlAtomicCounterBufferStart;
	public static const int GlBlockIndex;
	public static const int GlBufferBinding;
	public static const int GlBufferDataSize;
	public static const int GlBufferUpdateBarrierBit;
	public static const int GlBufferVariable;
	public static const int GlCommandBarrierBit;
	public static const int GlComputeShader;
	public static const int GlComputeShaderBit;
	public static const int GlComputeWorkGroupSize;
	public static const int GlDepthStencilTextureMode;
	public static const int GlDispatchIndirectBuffer;
	public static const int GlDispatchIndirectBufferBinding;
	public static const int GlDrawIndirectBuffer;
	public static const int GlDrawIndirectBufferBinding;
	public static const int GlFragmentShaderBit;
	public static const int GlFramebufferBarrierBit;
	public static const int GlFramebufferDefaultFixedSampleLocations;
	public static const int GlFramebufferDefaultHeight;
	public static const int GlFramebufferDefaultSamples;
	public static const int GlFramebufferDefaultWidth;
	public static const int GlImage2d;
	public static const int GlImage2dArray;
	public static const int GlImage3d;
	public static const int GlImageBindingAccess;
	public static const int GlImageBindingFormat;
	public static const int GlImageBindingLayer;
	public static const int GlImageBindingLayered;
	public static const int GlImageBindingLevel;
	public static const int GlImageBindingName;
	public static const int GlImageCube;
	public static const int GlImageFormatCompatibilityByClass;
	public static const int GlImageFormatCompatibilityBySize;
	public static const int GlImageFormatCompatibilityType;
	public static const int GlIntImage2d;
	public static const int GlIntImage2dArray;
	public static const int GlIntImage3d;
	public static const int GlIntImageCube;
	public static const int GlIntSampler2dMultisample;
	public static const int GlIsRowMajor;
	public static const int GlLocation;
	public static const int GlMatrixStride;
	public static const int GlMaxAtomicCounterBufferBindings;
	public static const int GlMaxAtomicCounterBufferSize;
	public static const int GlMaxColorTextureSamples;
	public static const int GlMaxCombinedAtomicCounterBuffers;
	public static const int GlMaxCombinedAtomicCounters;
	public static const int GlMaxCombinedComputeUniformComponents;
	public static const int GlMaxCombinedImageUniforms;
	public static const int GlMaxCombinedShaderOutputResources;
	public static const int GlMaxCombinedShaderStorageBlocks;
	public static const int GlMaxComputeAtomicCounterBuffers;
	public static const int GlMaxComputeAtomicCounters;
	public static const int GlMaxComputeImageUniforms;
	public static const int GlMaxComputeShaderStorageBlocks;
	public static const int GlMaxComputeSharedMemorySize;
	public static const int GlMaxComputeTextureImageUnits;
	public static const int GlMaxComputeUniformBlocks;
	public static const int GlMaxComputeUniformComponents;
	public static const int GlMaxComputeWorkGroupCount;
	public static const int GlMaxComputeWorkGroupInvocations;
	public static const int GlMaxComputeWorkGroupSize;
	public static const int GlMaxDepthTextureSamples;
	public static const int GlMaxFragmentAtomicCounterBuffers;
	public static const int GlMaxFragmentAtomicCounters;
	public static const int GlMaxFragmentImageUniforms;
	public static const int GlMaxFragmentShaderStorageBlocks;
	public static const int GlMaxFramebufferHeight;
	public static const int GlMaxFramebufferSamples;
	public static const int GlMaxFramebufferWidth;
	public static const int GlMaxImageUnits;
	public static const int GlMaxIntegerSamples;
	public static const int GlMaxNameLength;
	public static const int GlMaxNumActiveVariables;
	public static const int GlMaxProgramTextureGatherOffset;
	public static const int GlMaxSampleMaskWords;
	public static const int GlMaxShaderStorageBlockSize;
	public static const int GlMaxShaderStorageBufferBindings;
	public static const int GlMaxUniformLocations;
	public static const int GlMaxVertexAtomicCounterBuffers;
	public static const int GlMaxVertexAtomicCounters;
	public static const int GlMaxVertexAttribBindings;
	public static const int GlMaxVertexAttribRelativeOffset;
	public static const int GlMaxVertexAttribStride;
	public static const int GlMaxVertexImageUniforms;
	public static const int GlMaxVertexShaderStorageBlocks;
	public static const int GlMinProgramTextureGatherOffset;
	public static const int GlNameLength;
	public static const int GlNumActiveVariables;
	public static const int GlOffset;
	public static const int GlPixelBufferBarrierBit;
	public static const int GlProgramInput;
	public static const int GlProgramOutput;
	public static const int GlProgramPipelineBinding;
	public static const int GlProgramSeparable;
	public static const int GlReadOnly;
	public static const int GlReadWrite;
	public static const int GlReferencedByComputeShader;
	public static const int GlReferencedByFragmentShader;
	public static const int GlReferencedByVertexShader;
	public static const int GlSampleMask;
	public static const int GlSampleMaskValue;
	public static const int GlSamplePosition;
	public static const int GlSampler2dMultisample;
	public static const int GlShaderStorageBarrierBit;
	public static const int GlShaderStorageBlock;
	public static const int GlShaderStorageBuffer;
	public static const int GlShaderStorageBufferBinding;
	public static const int GlShaderStorageBufferOffsetAlignment;
	public static const int GlShaderStorageBufferSize;
	public static const int GlShaderStorageBufferStart;
	public static const int GlStencilIndex;
	public static const int GlTexture2dMultisample;
	public static const int GlTextureAlphaSize;
	public static const int GlTextureAlphaType;
	public static const int GlTextureBinding2dMultisample;
	public static const int GlTextureBlueSize;
	public static const int GlTextureBlueType;
	public static const int GlTextureCompressed;
	public static const int GlTextureDepth;
	public static const int GlTextureDepthSize;
	public static const int GlTextureDepthType;
	public static const int GlTextureFetchBarrierBit;
	public static const int GlTextureFixedSampleLocations;
	public static const int GlTextureGreenSize;
	public static const int GlTextureGreenType;
	public static const int GlTextureHeight;
	public static const int GlTextureInternalFormat;
	public static const int GlTextureRedSize;
	public static const int GlTextureRedType;
	public static const int GlTextureSamples;
	public static const int GlTextureSharedSize;
	public static const int GlTextureStencilSize;
	public static const int GlTextureUpdateBarrierBit;
	public static const int GlTextureWidth;
	public static const int GlTopLevelArraySize;
	public static const int GlTopLevelArrayStride;
	public static const int GlTransformFeedbackBarrierBit;
	public static const int GlTransformFeedbackVarying;
	public static const int GlType;
	public static const int GlUniform;
	public static const int GlUniformBarrierBit;
	public static const int GlUniformBlock;
	public static const int GlUnsignedIntAtomicCounter;
	public static const int GlUnsignedIntImage2d;
	public static const int GlUnsignedIntImage2dArray;
	public static const int GlUnsignedIntImage3d;
	public static const int GlUnsignedIntImageCube;
	public static const int GlUnsignedIntSampler2dMultisample;
	public static const int GlVertexAttribRelativeOffset;
	public static const int GlVertexBindingBuffer;
	public static const int GlVertexBindingOffset;
	public static const int GlVertexBindingStride;
	public static const int GlVertexShaderBit;
	public static const int GlWriteOnly;
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static void GlActiveShaderProgram (int pipeline, int program);
	public static void GlBindImageTexture (int unit, int texture, int level, bool layered, int layer, int access, int format);
	public static void GlBindProgramPipeline (int pipeline);
	public static void GlBindVertexBuffer (int bindingindex, int buffer, long offset, int stride);
	public static int GlCreateShaderProgramv (int type, string[] strings);
	public static void GlDeleteProgramPipelines (int n, Java.Nio.IntBuffer pipelines);
	public static void GlDeleteProgramPipelines (int n, int[] pipelines, int offset);
	public static void GlDispatchCompute (int num_groups_x, int num_groups_y, int num_groups_z);
	public static void GlDispatchComputeIndirect (long indirect);
	public static void GlDrawArraysIndirect (int mode, long indirect);
	public static void GlDrawElementsIndirect (int mode, int type, long indirect);
	public static void GlFramebufferParameteri (int target, int pname, int param);
	public static void GlGenProgramPipelines (int n, int[] pipelines, int offset);
	public static void GlGenProgramPipelines (int n, Java.Nio.IntBuffer pipelines);
	public static void GlGetBooleani_v (int target, int index, bool[] data, int offset);
	public static void GlGetBooleani_v (int target, int index, Java.Nio.IntBuffer data);
	public static void GlGetFramebufferParameteriv (int target, int pname, Java.Nio.IntBuffer params);
	public static void GlGetFramebufferParameteriv (int target, int pname, int[] params, int offset);
	public static void GlGetMultisamplefv (int pname, int index, Java.Nio.FloatBuffer val);
	public static void GlGetMultisamplefv (int pname, int index, float[] val, int offset);
	public static void GlGetProgramInterfaceiv (int program, int programInterface, int pname, int[] params, int offset);
	public static void GlGetProgramInterfaceiv (int program, int programInterface, int pname, Java.Nio.IntBuffer params);
	public static string GlGetProgramPipelineInfoLog (int program);
	public static void GlGetProgramPipelineiv (int pipeline, int pname, Java.Nio.IntBuffer params);
	public static void GlGetProgramPipelineiv (int pipeline, int pname, int[] params, int offset);
	public static int GlGetProgramResourceIndex (int program, int programInterface, string name);
	public static void GlGetProgramResourceiv (int program, int programInterface, int index, int propCount, Java.Nio.IntBuffer props, int bufSize, Java.Nio.IntBuffer length, Java.Nio.IntBuffer params);
	public static void GlGetProgramResourceiv (int program, int programInterface, int index, int propCount, int[] props, int propsOffset, int bufSize, int[] length, int lengthOffset, int[] params, int paramsOffset);
	public static int GlGetProgramResourceLocation (int program, int programInterface, string name);
	public static string GlGetProgramResourceName (int program, int programInterface, int index);
	public static void GlGetTexLevelParameterfv (int target, int level, int pname, Java.Nio.FloatBuffer params);
	public static void GlGetTexLevelParameterfv (int target, int level, int pname, float[] params, int offset);
	public static void GlGetTexLevelParameteriv (int target, int level, int pname, int[] params, int offset);
	public static void GlGetTexLevelParameteriv (int target, int level, int pname, Java.Nio.IntBuffer params);
	public static bool GlIsProgramPipeline (int pipeline);
	public static void GlMemoryBarrier (int barriers);
	public static void GlMemoryBarrierByRegion (int barriers);
	public static void GlProgramUniform1f (int program, int location, float v0);
	public static void GlProgramUniform1fv (int program, int location, int count, float[] value, int offset);
	public static void GlProgramUniform1fv (int program, int location, int count, Java.Nio.FloatBuffer value);
	public static void GlProgramUniform1i (int program, int location, int v0);
	public static void GlProgramUniform1iv (int program, int location, int count, Java.Nio.IntBuffer value);
	public static void GlProgramUniform1iv (int program, int location, int count, int[] value, int offset);
	public static void GlProgramUniform1ui (int program, int location, int v0);
	public static void GlProgramUniform1uiv (int program, int location, int count, Java.Nio.IntBuffer value);
	public static void GlProgramUniform1uiv (int program, int location, int count, int[] value, int offset);
	public static void GlProgramUniform2f (int program, int location, float v0, float v1);
	public static void GlProgramUniform2fv (int program, int location, int count, float[] value, int offset);
	public static void GlProgramUniform2fv (int program, int location, int count, Java.Nio.FloatBuffer value);
	public static void GlProgramUniform2i (int program, int location, int v0, int v1);
	public static void GlProgramUniform2iv (int program, int location, int count, int[] value, int offset);
	public static void GlProgramUniform2iv (int program, int location, int count, Java.Nio.IntBuffer value);
	public static void GlProgramUniform2ui (int program, int location, int v0, int v1);
	public static void GlProgramUniform2uiv (int program, int location, int count, int[] value, int offset);
	public static void GlProgramUniform2uiv (int program, int location, int count, Java.Nio.IntBuffer value);
	public static void GlProgramUniform3f (int program, int location, float v0, float v1, float v2);
	public static void GlProgramUniform3fv (int program, int location, int count, float[] value, int offset);
	public static void GlProgramUniform3fv (int program, int location, int count, Java.Nio.FloatBuffer value);
	public static void GlProgramUniform3i (int program, int location, int v0, int v1, int v2);
	public static void GlProgramUniform3iv (int program, int location, int count, int[] value, int offset);
	public static void GlProgramUniform3iv (int program, int location, int count, Java.Nio.IntBuffer value);
	public static void GlProgramUniform3ui (int program, int location, int v0, int v1, int v2);
	public static void GlProgramUniform3uiv (int program, int location, int count, int[] value, int offset);
	public static void GlProgramUniform3uiv (int program, int location, int count, Java.Nio.IntBuffer value);
	public static void GlProgramUniform4f (int program, int location, float v0, float v1, float v2, float v3);
	public static void GlProgramUniform4fv (int program, int location, int count, float[] value, int offset);
	public static void GlProgramUniform4fv (int program, int location, int count, Java.Nio.FloatBuffer value);
	public static void GlProgramUniform4i (int program, int location, int v0, int v1, int v2, int v3);
	public static void GlProgramUniform4iv (int program, int location, int count, int[] value, int offset);
	public static void GlProgramUniform4iv (int program, int location, int count, Java.Nio.IntBuffer value);
	public static void GlProgramUniform4ui (int program, int location, int v0, int v1, int v2, int v3);
	public static void GlProgramUniform4uiv (int program, int location, int count, int[] value, int offset);
	public static void GlProgramUniform4uiv (int program, int location, int count, Java.Nio.IntBuffer value);
	public static void GlProgramUniformMatrix2fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlProgramUniformMatrix2fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix2x3fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix2x3fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlProgramUniformMatrix2x4fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix2x4fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlProgramUniformMatrix3fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlProgramUniformMatrix3fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix3x2fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix3x2fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlProgramUniformMatrix3x4fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix3x4fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlProgramUniformMatrix4fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlProgramUniformMatrix4fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix4x2fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix4x2fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlProgramUniformMatrix4x3fv (int program, int location, int count, bool transpose, float[] value, int offset);
	public static void GlProgramUniformMatrix4x3fv (int program, int location, int count, bool transpose, Java.Nio.FloatBuffer value);
	public static void GlSampleMaski (int maskNumber, int mask);
	public static void GlTexStorage2DMultisample (int target, int samples, int internalformat, int width, int height, bool fixedsamplelocations);
	public static void GlUseProgramStages (int pipeline, int stages, int program);
	public static void GlValidateProgramPipeline (int pipeline);
	public static void GlVertexAttribBinding (int attribindex, int bindingindex);
	public static void GlVertexAttribFormat (int attribindex, int size, int type, bool normalized, int relativeoffset);
	public static void GlVertexAttribIFormat (int attribindex, int size, int type, int relativeoffset);
	public static void GlVertexBindingDivisor (int bindingindex, int divisor);
}
```

### New Type Android.Opengl.GLES31Ext

```
public class GLES31Ext : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected GLES31Ext (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const int GlBlendAdvancedCoherentKhr;
	public static const int GlBufferKhr;
	public static const int GlClampToBorderExt;
	public static const int GlColorburnKhr;
	public static const int GlColordodgeKhr;
	public static const int GLCOMPRESSEDRGBAASTC10x10KHR;
	public static const int GLCOMPRESSEDRGBAASTC10x5KHR;
	public static const int GLCOMPRESSEDRGBAASTC10x6KHR;
	public static const int GLCOMPRESSEDRGBAASTC10x8KHR;
	public static const int GLCOMPRESSEDRGBAASTC12x10KHR;
	public static const int GLCOMPRESSEDRGBAASTC12x12KHR;
	public static const int GLCOMPRESSEDRGBAASTC4x4KHR;
	public static const int GLCOMPRESSEDRGBAASTC5x4KHR;
	public static const int GLCOMPRESSEDRGBAASTC5x5KHR;
	public static const int GLCOMPRESSEDRGBAASTC6x5KHR;
	public static const int GLCOMPRESSEDRGBAASTC6x6KHR;
	public static const int GLCOMPRESSEDRGBAASTC8x5KHR;
	public static const int GLCOMPRESSEDRGBAASTC8x6KHR;
	public static const int GLCOMPRESSEDRGBAASTC8x8KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC10x10KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC10x5KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC10x6KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC10x8KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC12x10KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC12x12KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC4x4KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC5x4KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC5x5KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC6x5KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC6x6KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC8x5KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC8x6KHR;
	public static const int GLCOMPRESSEDSRGB8ALPHA8ASTC8x8KHR;
	public static const int GlContextFlagDebugBitKhr;
	public static const int GlDarkenKhr;
	public static const int GlDebugCallbackFunctionKhr;
	public static const int GlDebugCallbackUserParamKhr;
	public static const int GlDebugGroupStackDepthKhr;
	public static const int GlDebugLoggedMessagesKhr;
	public static const int GlDebugNextLoggedMessageLengthKhr;
	public static const int GlDebugOutputKhr;
	public static const int GlDebugOutputSynchronousKhr;
	public static const int GlDebugSeverityHighKhr;
	public static const int GlDebugSeverityLowKhr;
	public static const int GlDebugSeverityMediumKhr;
	public static const int GlDebugSeverityNotificationKhr;
	public static const int GlDebugSourceApiKhr;
	public static const int GlDebugSourceApplicationKhr;
	public static const int GlDebugSourceOtherKhr;
	public static const int GlDebugSourceShaderCompilerKhr;
	public static const int GlDebugSourceThirdPartyKhr;
	public static const int GlDebugSourceWindowSystemKhr;
	public static const int GlDebugTypeDeprecatedBehaviorKhr;
	public static const int GlDebugTypeErrorKhr;
	public static const int GlDebugTypeMarkerKhr;
	public static const int GlDebugTypeOtherKhr;
	public static const int GlDebugTypePerformanceKhr;
	public static const int GlDebugTypePopGroupKhr;
	public static const int GlDebugTypePortabilityKhr;
	public static const int GlDebugTypePushGroupKhr;
	public static const int GlDebugTypeUndefinedBehaviorKhr;
	public static const int GlDecodeExt;
	public static const int GlDifferenceKhr;
	public static const int GlExclusionKhr;
	public static const int GlFirstVertexConventionExt;
	public static const int GlFractionalEvenExt;
	public static const int GlFractionalOddExt;
	public static const int GlFragmentInterpolationOffsetBitsOes;
	public static const int GlFramebufferAttachmentLayeredExt;
	public static const int GlFramebufferDefaultLayersExt;
	public static const int GlFramebufferIncompleteLayerTargetsExt;
	public static const int GlGeometryLinkedInputTypeExt;
	public static const int GlGeometryLinkedOutputTypeExt;
	public static const int GlGeometryLinkedVerticesOutExt;
	public static const int GlGeometryShaderBitExt;
	public static const int GlGeometryShaderExt;
	public static const int GlGeometryShaderInvocationsExt;
	public static const int GlHardlightKhr;
	public static const int GlHslColorKhr;
	public static const int GlHslHueKhr;
	public static const int GlHslLuminosityKhr;
	public static const int GlHslSaturationKhr;
	public static const int GlImageBufferExt;
	public static const int GlImageCubeMapArrayExt;
	public static const int GlIntImageBufferExt;
	public static const int GlIntImageCubeMapArrayExt;
	public static const int GlIntSampler2dMultisampleArrayOes;
	public static const int GlIntSamplerBufferExt;
	public static const int GlIntSamplerCubeMapArrayExt;
	public static const int GlIsolinesExt;
	public static const int GlIsPerPatchExt;
	public static const int GlLastVertexConventionExt;
	public static const int GlLayerProvokingVertexExt;
	public static const int GlLightenKhr;
	public static const int GlLinesAdjacencyExt;
	public static const int GlLineStripAdjacencyExt;
	public static const int GlMaxCombinedGeometryUniformComponentsExt;
	public static const int GlMaxCombinedTessControlUniformComponentsExt;
	public static const int GlMaxCombinedTessEvaluationUniformComponentsExt;
	public static const int GlMaxDebugGroupStackDepthKhr;
	public static const int GlMaxDebugLoggedMessagesKhr;
	public static const int GlMaxDebugMessageLengthKhr;
	public static const int GlMaxFragmentInterpolationOffsetOes;
	public static const int GlMaxFramebufferLayersExt;
	public static const int GlMaxGeometryAtomicCounterBuffersExt;
	public static const int GlMaxGeometryAtomicCountersExt;
	public static const int GlMaxGeometryImageUniformsExt;
	public static const int GlMaxGeometryInputComponentsExt;
	public static const int GlMaxGeometryOutputComponentsExt;
	public static const int GlMaxGeometryOutputVerticesExt;
	public static const int GlMaxGeometryShaderInvocationsExt;
	public static const int GlMaxGeometryShaderStorageBlocksExt;
	public static const int GlMaxGeometryTextureImageUnitsExt;
	public static const int GlMaxGeometryTotalOutputComponentsExt;
	public static const int GlMaxGeometryUniformBlocksExt;
	public static const int GlMaxGeometryUniformComponentsExt;
	public static const int GlMaxLabelLengthKhr;
	public static const int GlMaxPatchVerticesExt;
	public static const int GlMaxTessControlAtomicCounterBuffersExt;
	public static const int GlMaxTessControlAtomicCountersExt;
	public static const int GlMaxTessControlImageUniformsExt;
	public static const int GlMaxTessControlInputComponentsExt;
	public static const int GlMaxTessControlOutputComponentsExt;
	public static const int GlMaxTessControlShaderStorageBlocksExt;
	public static const int GlMaxTessControlTextureImageUnitsExt;
	public static const int GlMaxTessControlTotalOutputComponentsExt;
	public static const int GlMaxTessControlUniformBlocksExt;
	public static const int GlMaxTessControlUniformComponentsExt;
	public static const int GlMaxTessEvaluationAtomicCounterBuffersExt;
	public static const int GlMaxTessEvaluationAtomicCountersExt;
	public static const int GlMaxTessEvaluationImageUniformsExt;
	public static const int GlMaxTessEvaluationInputComponentsExt;
	public static const int GlMaxTessEvaluationOutputComponentsExt;
	public static const int GlMaxTessEvaluationShaderStorageBlocksExt;
	public static const int GlMaxTessEvaluationTextureImageUnitsExt;
	public static const int GlMaxTessEvaluationUniformBlocksExt;
	public static const int GlMaxTessEvaluationUniformComponentsExt;
	public static const int GlMaxTessGenLevelExt;
	public static const int GlMaxTessPatchComponentsExt;
	public static const int GlMaxTextureBufferSizeExt;
	public static const int GlMinFragmentInterpolationOffsetOes;
	public static const int GlMinSampleShadingValueOes;
	public static const int GlMultiplyKhr;
	public static const int GlOverlayKhr;
	public static const int GlPatchesExt;
	public static const int GlPatchVerticesExt;
	public static const int GlPrimitiveBoundingBoxExt;
	public static const int GlPrimitiveRestartForPatchesSupported;
	public static const int GlPrimitivesGeneratedExt;
	public static const int GlProgramKhr;
	public static const int GlQuadsExt;
	public static const int GlQueryKhr;
	public static const int GlReferencedByGeometryShaderExt;
	public static const int GlReferencedByTessControlShaderExt;
	public static const int GlReferencedByTessEvaluationShaderExt;
	public static const int GlSampler2dMultisampleArrayOes;
	public static const int GlSamplerBufferExt;
	public static const int GlSamplerCubeMapArrayExt;
	public static const int GlSamplerCubeMapArrayShadowExt;
	public static const int GlSamplerKhr;
	public static const int GlSampleShadingOes;
	public static const int GlScreenKhr;
	public static const int GlShaderKhr;
	public static const int GlSkipDecodeExt;
	public static const int GlSoftlightKhr;
	public static const int GlStackOverflowKhr;
	public static const int GlStackUnderflowKhr;
	public static const int GlStencilIndex8Oes;
	public static const int GlStencilIndexOes;
	public static const int GlTessControlOutputVerticesExt;
	public static const int GlTessControlShaderBitExt;
	public static const int GlTessControlShaderExt;
	public static const int GlTessEvaluationShaderBitExt;
	public static const int GlTessEvaluationShaderExt;
	public static const int GlTessGenModeExt;
	public static const int GlTessGenPointModeExt;
	public static const int GlTessGenSpacingExt;
	public static const int GlTessGenVertexOrderExt;
	public static const int GlTexture2dMultisampleArrayOes;
	public static const int GlTextureBinding2dMultisampleArrayOes;
	public static const int GlTextureBindingBufferExt;
	public static const int GlTextureBindingCubeMapArrayExt;
	public static const int GlTextureBorderColorExt;
	public static const int GlTextureBufferBindingExt;
	public static const int GlTextureBufferDataStoreBindingExt;
	public static const int GlTextureBufferExt;
	public static const int GlTextureBufferOffsetAlignmentExt;
	public static const int GlTextureBufferOffsetExt;
	public static const int GlTextureBufferSizeExt;
	public static const int GlTextureCubeMapArrayExt;
	public static const int GlTextureSrgbDecodeExt;
	public static const int GlTrianglesAdjacencyExt;
	public static const int GlTriangleStripAdjacencyExt;
	public static const int GlUndefinedVertexExt;
	public static const int GlUnsignedIntImageBufferExt;
	public static const int GlUnsignedIntImageCubeMapArrayExt;
	public static const int GlUnsignedIntSampler2dMultisampleArrayOes;
	public static const int GlUnsignedIntSamplerBufferExt;
	public static const int GlUnsignedIntSamplerCubeMapArrayExt;
	public static const int GlVertexArrayKhr;
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static void GlBlendBarrierKHR ();
	public static void GlBlendEquationiEXT (int buf, int mode);
	public static void GlBlendEquationSeparateiEXT (int buf, int modeRGB, int modeAlpha);
	public static void GlBlendFunciEXT (int buf, int src, int dst);
	public static void GlBlendFuncSeparateiEXT (int buf, int srcRGB, int dstRGB, int srcAlpha, int dstAlpha);
	public static void GlColorMaskiEXT (int index, bool r, bool g, bool b, bool a);
	public static void GlDebugMessageCallbackKHR (GLES31Ext.IDebugProcKHR callback);
	public static void GlDebugMessageControlKHR (int source, int type, int severity, int count, int[] ids, int offset, bool enabled);
	public static void GlDebugMessageControlKHR (int source, int type, int severity, int count, Java.Nio.IntBuffer ids, bool enabled);
	public static void GlDebugMessageInsertKHR (int source, int type, int id, int severity, string buf);
	public static void GlDisableiEXT (int target, int index);
	public static void GlEnableiEXT (int target, int index);
	public static void GlFramebufferTextureEXT (int target, int attachment, int texture, int level);
	public static GLES31Ext.IDebugProcKHR GlGetDebugMessageCallbackKHR ();
	public static int GlGetDebugMessageLogKHR (int count, Java.Nio.IntBuffer sources, Java.Nio.IntBuffer types, Java.Nio.IntBuffer ids, Java.Nio.IntBuffer severities, Java.Nio.IntBuffer lengths, Java.Nio.ByteBuffer messageLog);
	public static string[] GlGetDebugMessageLogKHR (int count, Java.Nio.IntBuffer sources, Java.Nio.IntBuffer types, Java.Nio.IntBuffer ids, Java.Nio.IntBuffer severities);
	public static string[] GlGetDebugMessageLogKHR (int count, int[] sources, int sourcesOffset, int[] types, int typesOffset, int[] ids, int idsOffset, int[] severities, int severitiesOffset);
	public static int GlGetDebugMessageLogKHR (int count, int bufSize, int[] sources, int sourcesOffset, int[] types, int typesOffset, int[] ids, int idsOffset, int[] severities, int severitiesOffset, int[] lengths, int lengthsOffset, byte[] messageLog, int messageLogOffset);
	public static string GlGetObjectLabelKHR (int identifier, int name);
	public static string GlGetObjectPtrLabelKHR (long ptr);
	public static void GlGetSamplerParameterIivEXT (int sampler, int pname, int[] params, int offset);
	public static void GlGetSamplerParameterIivEXT (int sampler, int pname, Java.Nio.IntBuffer params);
	public static void GlGetSamplerParameterIuivEXT (int sampler, int pname, Java.Nio.IntBuffer params);
	public static void GlGetSamplerParameterIuivEXT (int sampler, int pname, int[] params, int offset);
	public static void GlGetTexParameterIivEXT (int target, int pname, int[] params, int offset);
	public static void GlGetTexParameterIivEXT (int target, int pname, Java.Nio.IntBuffer params);
	public static void GlGetTexParameterIuivEXT (int target, int pname, int[] params, int offset);
	public static void GlGetTexParameterIuivEXT (int target, int pname, Java.Nio.IntBuffer params);
	public static bool GlIsEnablediEXT (int target, int index);
	public static void GlMinSampleShadingOES (float value);
	public static void GlObjectLabelKHR (int identifier, int name, int length, string label);
	public static void GlObjectPtrLabelKHR (long ptr, string label);
	public static void GlPatchParameteriEXT (int pname, int value);
	public static void GlPopDebugGroupKHR ();
	public static void GlPrimitiveBoundingBoxEXT (float minX, float minY, float minZ, float minW, float maxX, float maxY, float maxZ, float maxW);
	public static void GlPushDebugGroupKHR (int source, int id, int length, string message);
	public static void GlSamplerParameterIivEXT (int sampler, int pname, int[] param, int offset);
	public static void GlSamplerParameterIivEXT (int sampler, int pname, Java.Nio.IntBuffer param);
	public static void GlSamplerParameterIuivEXT (int sampler, int pname, int[] param, int offset);
	public static void GlSamplerParameterIuivEXT (int sampler, int pname, Java.Nio.IntBuffer param);
	public static void GlTexBufferEXT (int target, int internalformat, int buffer);
	public static void GlTexBufferRangeEXT (int target, int internalformat, int buffer, int offset, int size);
	public static void GlTexParameterIivEXT (int target, int pname, int[] params, int offset);
	public static void GlTexParameterIivEXT (int target, int pname, Java.Nio.IntBuffer params);
	public static void GlTexParameterIuivEXT (int target, int pname, int[] params, int offset);
	public static void GlTexParameterIuivEXT (int target, int pname, Java.Nio.IntBuffer params);
	public static void GlTexStorage3DMultisampleOES (int target, int samples, int internalformat, int width, int height, int depth, bool fixedsamplelocations);

	// inner types
	public interface IDebugProcKHR : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual void OnMessage (int source, int type, int id, int severity, string message);
	}
}
```

## Namespace Android.OS

### Type Changed: Android.OS.BatteryManager

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.OS.BatteryProperty enum directly instead of this field.")]
	public static const BatteryProperty BatteryPropertyCapacity;

	[Obsolete ("This constant will be removed in the future version. Use Android.OS.BatteryProperty enum directly instead of this field.")]
	public static const BatteryProperty BatteryPropertyChargeCounter;

	[Obsolete ("This constant will be removed in the future version. Use Android.OS.BatteryProperty enum directly instead of this field.")]
	public static const BatteryProperty BatteryPropertyCurrentAverage;

	[Obsolete ("This constant will be removed in the future version. Use Android.OS.BatteryProperty enum directly instead of this field.")]
	public static const BatteryProperty BatteryPropertyCurrentNow;

	[Obsolete ("This constant will be removed in the future version. Use Android.OS.BatteryProperty enum directly instead of this field.")]
	public static const BatteryProperty BatteryPropertyEnergyCounter;
```

Added methods:

```
public virtual int GetIntProperty (int id);
	public virtual long GetLongProperty (int id);
```

### Type Changed: Android.OS.Build

Added properties:

```
public static System.Collections.Generic.IList<string> Supported32BitAbis { get; set; }
	public static System.Collections.Generic.IList<string> Supported64BitAbis { get; set; }
	public static System.Collections.Generic.IList<string> SupportedAbis { get; set; }
```

### Type Changed: Android.OS.Build.VERSION_CODES

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.OS.BuildVersionCodes enum directly instead of this field.")]
	public static const BuildVersionCodes L;

	[Obsolete ("This constant will be removed in the future version. Use Android.OS.BuildVersionCodes enum directly instead of this field.")]
	public static const BuildVersionCodes Lollipop;
```

### Type Changed: Android.OS.BuildVersionCodes

Added values:

```
L = 21,
	Lollipop = 21,
```

### Type Changed: Android.OS.Bundle

Added constructor:

```
public Bundle (PersistableBundle b);
```

Removed property:

```
public bool IsEmpty { get; }
```

Added property:

```
public override bool IsEmpty { get; }
```

Removed methods:

```
public void Clear ();
	public bool ContainsKey (string p0);
	public Java.Lang.Object Get (string p0);
	public double GetDouble (string p0, double p1);
	public double GetDouble (string p0);
	public double[] GetDoubleArray (string p0);
	public int GetInt (string p0, int p1);
	public int GetInt (string p0);
	public int[] GetIntArray (string p0);
	public long GetLong (string p0);
	public long GetLong (string p0, long p1);
	public long[] GetLongArray (string p0);
	public string GetString (string p0);
	public string GetString (string p0, string p1);
	public string[] GetStringArray (string p0);
	public System.Collections.Generic.ICollection<string> KeySet ();
	public void PutDouble (string p0, double p1);
	public void PutDoubleArray (string p0, double[] p1);
	public void PutInt (string p0, int p1);
	public void PutIntArray (string p0, int[] p1);
	public void PutLong (string p0, long p1);
	public void PutLongArray (string p0, long[] p1);
	public void PutString (string p0, string p1);
	public void PutStringArray (string p0, string[] p1);
	public void Remove (string p0);
	public int Size ();
```

Added methods:

```
public override void Clear ();
	public override bool ContainsKey (string p0);
	public override Java.Lang.Object Get (string p0);
	public override double GetDouble (string p0);
	public override double GetDouble (string p0, double p1);
	public override double[] GetDoubleArray (string p0);
	public override int GetInt (string p0);
	public override int GetInt (string p0, int p1);
	public override int[] GetIntArray (string p0);
	public override long GetLong (string p0);
	public override long GetLong (string p0, long p1);
	public override long[] GetLongArray (string p0);
	public Android.Util.Size GetSize (string key);
	public Android.Util.SizeF GetSizeF (string key);
	public override string GetString (string p0);
	public override string GetString (string p0, string p1);
	public override string[] GetStringArray (string p0);
	public override System.Collections.Generic.ICollection<string> KeySet ();
	public override void PutDouble (string p0, double p1);
	public override void PutDoubleArray (string p0, double[] p1);
	public override void PutInt (string p0, int p1);
	public override void PutIntArray (string p0, int[] p1);
	public override void PutLong (string p0, long p1);
	public override void PutLongArray (string p0, long[] p1);
	public void PutSize (string key, Android.Util.Size value);
	public void PutSizeF (string key, Android.Util.SizeF value);
	public override void PutString (string p0, string p1);
	public override void PutStringArray (string p0, string[] p1);
	public override void Remove (string p0);
	public override int Size ();
```

### Type Changed: Android.OS.Debug

Added method:

```
public static void StartMethodTracingSampling (string traceName, int bufferSize, int intervalUs);
```

### Type Changed: Android.OS.Environment

Added methods:

```
public static string GetExternalStorageState (Java.IO.File path);
	public static bool InvokeIsExternalStorageEmulated (Java.IO.File path);
	public static bool InvokeIsExternalStorageRemovable (Java.IO.File path);
```

### Type Changed: Android.OS.Message

Added property:

```
public int SendingUid { get; set; }
```

### Type Changed: Android.OS.Parcel

Added methods:

```
public PersistableBundle ReadPersistableBundle (Java.Lang.ClassLoader loader);
	public PersistableBundle ReadPersistableBundle ();
	public Android.Util.Size ReadSize ();
	public Android.Util.SizeF ReadSizeF ();
	public void WritePersistableBundle (PersistableBundle val);
	public void WriteSize (Android.Util.Size val);
	public void WriteSizeF (Android.Util.SizeF val);
```

### Type Changed: Android.OS.PowerManager

Added field:

```
public static const string ActionPowerSaveModeChanged = "android.os.action.POWER_SAVE_MODE_CHANGED";
```

Added property:

```
public virtual bool IsPowerSaveMode { get; }
```

Added method:

```
public virtual bool IsWakeLockLevelSupported (int level);
```

### Type Changed: Android.OS.PowerManager.WakeLock

Added method:

```
public virtual void Release (WakeLockFlags flags);
```

### Type Changed: Android.OS.UserManager

Added fields:

```
public static const string DisallowAddUser = "no_add_user";
	public static const string DisallowAdjustVolume = "no_adjust_volume";
	public static const string DisallowAppsControl = "no_control_apps";
	public static const string DisallowConfigCellBroadcasts = "no_config_cell_broadcasts";
	public static const string DisallowConfigMobileNetworks = "no_config_mobile_networks";
	public static const string DisallowConfigTethering = "no_config_tethering";
	public static const string DisallowConfigVpn = "no_config_vpn";
	public static const string DisallowCreateWindows = "no_create_windows";
	public static const string DisallowCrossProfileCopyPaste = "no_cross_profile_copy_paste";
	public static const string DisallowDebuggingFeatures = "no_debugging_features";
	public static const string DisallowFactoryReset = "no_factory_reset";
	public static const string DisallowMountPhysicalMedia = "no_physical_media";
	public static const string DisallowOutgoingCalls = "no_outgoing_calls";
	public static const string DisallowSms = "no_sms";
	public static const string DisallowUnmuteMicrophone = "no_unmute_microphone";
	public static const string EnsureVerifyApps = "ensure_verify_apps";
```

Added property:

```
public virtual System.Collections.Generic.IList<UserHandle> UserProfiles { get; }
```

Added method:

```
public virtual bool HasUserRestriction (string restrictionKey);
```

### Type Changed: Android.OS.Vibrator

Added methods:

```
public virtual void Vibrate (long milliseconds, Android.Media.AudioAttributes attributes);
	public virtual void Vibrate (long[] pattern, int repeat, Android.Media.AudioAttributes attributes);
```

### Type Changed: Android.OS.WakeLockFlags

Added values:

```
ProximityScreenOff = 32,
	ReleaseFlagWaitForNoProximity = 1,
```

### New Type Android.OS.BaseBundle

```
public class BaseBundle : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected BaseBundle (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual bool IsEmpty { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Clear ();
	public virtual bool ContainsKey (string key);
	public virtual Java.Lang.Object Get (string key);
	public virtual double GetDouble (string key);
	public virtual double GetDouble (string key, double defaultValue);
	public virtual double[] GetDoubleArray (string key);
	public virtual int GetInt (string key, int defaultValue);
	public virtual int GetInt (string key);
	public virtual int[] GetIntArray (string key);
	public virtual long GetLong (string key);
	public virtual long GetLong (string key, long defaultValue);
	public virtual long[] GetLongArray (string key);
	public virtual string GetString (string key, string defaultValue);
	public virtual string GetString (string key);
	public virtual string[] GetStringArray (string key);
	public virtual System.Collections.Generic.ICollection<string> KeySet ();
	public virtual void PutAll (PersistableBundle bundle);
	public virtual void PutDouble (string key, double value);
	public virtual void PutDoubleArray (string key, double[] value);
	public virtual void PutInt (string key, int value);
	public virtual void PutIntArray (string key, int[] value);
	public virtual void PutLong (string key, long value);
	public virtual void PutLongArray (string key, long[] value);
	public virtual void PutString (string key, string value);
	public virtual void PutStringArray (string key, string[] value);
	public virtual void Remove (string key);
	public virtual int Size ();
}
```

### New Type Android.OS.BatteryProperty

```
[Serializable]
public enum BatteryProperty {
	Capacity = 4,
	ChargeCounter = 1,
	CurrentAverage = 3,
	CurrentNow = 2,
	EnergyCounter = 5,
}
```

### New Type Android.OS.PersistableBundle

```
public sealed class PersistableBundle : Android.OS.BaseBundle, IParcelable, Java.Lang.ICloneable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public PersistableBundle (PersistableBundle b);
	public PersistableBundle (int capacity);
	public PersistableBundle ();
	// properties
	public static IParcelableCreator Creator { get; set; }
	public static PersistableBundle Empty { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public Java.Lang.Object Clone ();
	public virtual int DescribeContents ();
	public PersistableBundle GetPersistableBundle (string key);
	public void PutPersistableBundle (string key, PersistableBundle value);
	public virtual void WriteToParcel (Parcel parcel, ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

## Namespace Android.Preferences

### Type Changed: Android.Preferences.CheckBoxPreference

Added constructor:

```
public CheckBoxPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.DialogPreference

Added constructors:

```
public DialogPreference (Android.Content.Context context);
	public DialogPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.EditTextPreference

Added constructor:

```
public EditTextPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.ListPreference

Added constructors:

```
public ListPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public ListPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.MultiSelectListPreference

Added constructors:

```
public MultiSelectListPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public MultiSelectListPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.Preference

Added constructor:

```
public Preference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.PreferenceCategory

Added constructor:

```
public PreferenceCategory (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.PreferenceGroup

Added constructor:

```
public PreferenceGroup (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.RingtonePreference

Added constructor:

```
public RingtonePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.SwitchPreference

Added constructor:

```
public SwitchPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Preferences.TwoStatePreference

Added constructor:

```
public TwoStatePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

## Namespace Android.PrintServices

### Type Changed: Android.PrintServices.PrintService

Added field:

```
public static const string ExtraPrinterInfo = "android.intent.extra.print.EXTRA_PRINTER_INFO";
```

## Namespace Android.Provider

### Type Changed: Android.Provider.CallLog

### Type Changed: Android.Provider.CallLog.Calls

Added fields:

```
public static const string CachedFormattedNumber = "formatted_number";
	public static const string CachedLookupUri = "lookup_uri";
	public static const string CachedMatchedNumber = "matched_number";
	public static const string CachedNormalizedNumber = "normalized_number";
	public static const string CachedPhotoId = "photo_id";
	public static const string CountryIso = "countryiso";
	public static const string DataUsage = "data_usage";
	public static const string ExtraCallTypeFilter = "android.provider.extra.CALL_TYPE_FILTER";
	public static const string Features = "features";
	public static const int FeaturesVideo;
	public static const string GeocodedLocation = "geocoded_location";
	public static const string PhoneAccountComponentName = "subscription_component_name";
	public static const string PhoneAccountId = "subscription_id";
	public static const string Transcription = "transcription";
	public static const string VoicemailUri = "voicemail_uri";
```

Added property:

```
public static Android.Net.Uri ContentUriWithVoicemail { get; set; }
```

### Type Changed: Android.Provider.CallType

Added value:

```
Voicemail = 4,
```

### Type Changed: Android.Provider.ContactsContract

Added fields:

```
public static const string DeferredSnippeting = "deferred_snippeting";
	public static const string DeferredSnippetingQuery = "deferred_snippeting_query";
	public static const string RemoveDuplicateEntries = "remove_duplicate_entries";
	public static const string StrequentPhoneOnly = "strequent_phone_only";
```

### Type Changed: Android.Provider.ContactsContract.CommonDataKinds

### Type Changed: Android.Provider.ContactsContract.Contactables

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Email

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Event

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

Added methods:

```
public static string GetTypeLabel (Android.Content.Res.Resources res, EventDataKind type, string label);
	public static Java.Lang.ICharSequence GetTypeLabelFormatted (Android.Content.Res.Resources res, EventDataKind type, Java.Lang.ICharSequence label);
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.GroupMembership

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Identity

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Im

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Nickname

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Note

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Organization

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Phone

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Photo

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Relation

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.SipAddress

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.StructuredName

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
	public static const string FullNameStyle = "data10";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.StructuredPostal

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Website

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### New Type Android.Provider.Callable

```
public sealed class Callable : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public ContactsContract ();
	// fields
	public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
	// properties
	public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const string AccountTypeAndDataSet = "account_type_and_data_set";
		public static const string AggregationMode = "aggregation_mode";

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.StatusPresence enum directly instead of this field.")]
		public static const StatusPresence Available;

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.StatusPresence enum directly instead of this field.")]
		public static const StatusPresence Away;

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.ChatCapability enum directly instead of this field.")]
		public static const ChatCapability CapabilityHasCamera;

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.ChatCapability enum directly instead of this field.")]
		public static const ChatCapability CapabilityHasVideo;

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.ChatCapability enum directly instead of this field.")]
		public static const ChatCapability CapabilityHasVoice;
		public static const string ChatCapability = "chat_capability";
		public static const string ContactChatCapability = "contact_chat_capability";
		public static const string ContactId = "contact_id";
		public static const string ContactLastUpdatedTimestamp = "contact_last_updated_timestamp";
		public static const string ContactPresence = "contact_presence";
		public static const string ContactStatus = "contact_status";
		public static const string ContactStatusIcon = "contact_status_icon";
		public static const string ContactStatusLabel = "contact_status_label";
		public static const string ContactStatusResPackage = "contact_status_res_package";
		public static const string ContactStatusTimestamp = "contact_status_ts";
		public static const string Count = "_count";
		public static const string CustomRingtone = "custom_ringtone";
		public static const string Data = "data1";
		public static const string Data1 = "data1";
		public static const string Data10 = "data10";
		public static const string Data11 = "data11";
		public static const string Data12 = "data12";
		public static const string Data13 = "data13";
		public static const string Data14 = "data14";
		public static const string Data15 = "data15";
		public static const string Data2 = "data2";
		public static const string Data3 = "data3";
		public static const string Data4 = "data4";
		public static const string Data5 = "data5";
		public static const string Data6 = "data6";
		public static const string Data7 = "data7";
		public static const string Data8 = "data8";
		public static const string Data9 = "data9";
		public static const string DataSet = "data_set";
		public static const string DataVersion = "data_version";
		public static const string Deleted = "deleted";
		public static const string DisplayName = "display_name";
		public static const string DisplayNameAlternative = "display_name_alt";
		public static const string DisplayNamePrimary = "display_name";
		public static const string DisplayNameSource = "display_name_source";

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.StatusPresence enum directly instead of this field.")]
		public static const StatusPresence DoNotDisturb;
		public static const string HasPhoneNumber = "has_phone_number";
		public static const string Id = "_id";

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.StatusPresence enum directly instead of this field.")]
		public static const StatusPresence Idle;
		public static const string InDefaultDirectory = "in_default_directory";

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.StatusPresence enum directly instead of this field.")]
		public static const StatusPresence Invisible;
		public static const string InVisibleGroup = "in_visible_group";
		public static const string IsPrimary = "is_primary";
		public static const string IsReadOnly = "is_read_only";
		public static const string IsSuperPrimary = "is_super_primary";
		public static const string IsUserProfile = "is_user_profile";
		public static const string Label = "data3";
		public static const string LastTimeContacted = "last_time_contacted";
		public static const string LastTimeUsed = "last_time_used";
		public static const string LookupKey = "lookup";
		public static const string Mimetype = "mimetype";
		public static const string NameRawContactId = "name_raw_contact_id";

		[Obsolete ("This constant will be removed in the future version. Use Android.Provider.StatusPresence enum directly instead of this field.")]
		public static const StatusPresence Offline;
		public static const string PhoneticName = "phonetic_name";
		public static const string PhoneticNameStyle = "phonetic_name_style";
		public static const string PhotoFileId = "photo_file_id";
		public static const string PhotoId = "photo_id";
		public static const string PhotoThumbnailUri = "photo_thumb_uri";
		public static const string PhotoUri = "photo_uri";
		public static const string Pinned = "pinned";
		public static const string Presence = "mode";

		[Obsolete ("deprecated")]
		public static const string PresenceCustomStatus = "status";

		[Obsolete ("deprecated")]
		public static const string PresenceStatus = "mode";
		public static const string RawContactId = "raw_contact_id";
		public static const string RawContactIsReadOnly = "raw_contact_is_read_only";
		public static const string RawContactIsUserProfile = "raw_contact_is_user_profile";
		public static const string ResPackage = "res_package";
		public static const string SendToVoicemail = "send_to_voicemail";
		public static const string SortKeyAlternative = "sort_key_alt";
		public static const string SortKeyPrimary = "sort_key";
		public static const string Starred = "starred";
		public static const string Status = "status";
		public static const string StatusIcon = "status_icon";
		public static const string StatusLabel = "status_label";
		public static const string StatusResPackage = "status_res_package";
		public static const string StatusTimestamp = "status_ts";
		public static const string Sync1 = "data_sync1";
		public static const string Sync2 = "data_sync2";
		public static const string Sync3 = "data_sync3";
		public static const string Sync4 = "data_sync4";
		public static const string TimesContacted = "times_contacted";
		public static const string TimesUsed = "times_used";
		public static const string Type = "data2";
		public static const int TypeCustom;
	}
}
```

### Type Changed: Android.Provider.ContactsContract.ContactOptionsColumns

Added field:

```
public static const string Pinned = "pinned";
```

### Type Changed: Android.Provider.ContactsContract.Contacts

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

Added properties:

```
public static Android.Net.Uri ContentFrequentUri { get; set; }
	public static Android.Net.Uri ContentMultiVcardUri { get; set; }
```

Added method:

```
public static bool IsEnterpriseContactId (long contactId);
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
```

### Type Changed: Android.Provider.ContactsContract.AggregationSuggestions

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
```

### Type Changed: Android.Provider.ContactsContract.Data

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added field:

```
public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Entity

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string LastTimeUsed = "last_time_used";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
	public static const string TimesUsed = "times_used";
```

### Type Changed: Android.Provider.ContactsContract.Photo

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.StreamItems

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const string ContentDirectory = "stream_items";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string AccountName = "account_name";

	[Obsolete ("deprecated")]
	public static const string AccountType = "account_type";

	[Obsolete ("deprecated")]
	public static const string Comments = "comments";

	[Obsolete ("deprecated")]
	public static const string ContactId = "contact_id";

	[Obsolete ("deprecated")]
	public static const string ContactLookupKey = "contact_lookup";

	[Obsolete ("deprecated")]
	public static const string DataSet = "data_set";

	[Obsolete ("deprecated")]
	public static const string RawContactId = "raw_contact_id";

	[Obsolete ("deprecated")]
	public static const string RawContactSourceId = "raw_contact_source_id";

	[Obsolete ("deprecated")]
	public static const string ResIcon = "icon";

	[Obsolete ("deprecated")]
	public static const string ResLabel = "label";

	[Obsolete ("deprecated")]
	public static const string ResPackage = "res_package";

	[Obsolete ("deprecated")]
	public static const string Sync1 = "stream_item_sync1";

	[Obsolete ("deprecated")]
	public static const string Sync2 = "stream_item_sync2";

	[Obsolete ("deprecated")]
	public static const string Sync3 = "stream_item_sync3";

	[Obsolete ("deprecated")]
	public static const string Sync4 = "stream_item_sync4";

	[Obsolete ("deprecated")]
	public static const string Text = "text";

	[Obsolete ("deprecated")]
	public static const string Timestamp = "timestamp";
```

### Type Changed: Android.Provider.ContactsContract.ContactsColumns

Added fields:

```
public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
```

### Type Changed: Android.Provider.ContactsContract.Data

Added fields:

```
public static const string ExtraAddressBookIndex = "android.provider.extra.ADDRESS_BOOK_INDEX";
	public static const string ExtraAddressBookIndexCounts = "android.provider.extra.ADDRESS_BOOK_INDEX_COUNTS";
	public static const string ExtraAddressBookIndexTitles = "android.provider.extra.ADDRESS_BOOK_INDEX_TITLES";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.DataColumns

Added field:

```
public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Groups

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string ResPackage = "res_package";
	public static const string TitleRes = "title_res";
```

### Type Changed: Android.Provider.ContactsContract.GroupsColumns

Added fields:

```
public static const string ResPackage = "res_package";
	public static const string TitleRes = "title_res";
```

### Type Changed: Android.Provider.ContactsContract.PhoneLookup

Added field:

```
public static const string QueryParameterSipAddress = "sip";
```

Added property:

```
public static Android.Net.Uri EnterpriseContentFilterUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
```

### Type Changed: Android.Provider.ContactsContract.Profile

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string InDefaultDirectory = "in_default_directory";
	public static const string NameRawContactId = "name_raw_contact_id";
	public static const string Pinned = "pinned";
```

### Type Changed: Android.Provider.ContactsContract.QuickContact

Added fields:

```
public static const string ActionQuickContact = "android.provider.action.QUICK_CONTACT";
	public static const string ExtraExcludeMimes = "android.provider.extra.EXCLUDE_MIMES";
```

### Type Changed: Android.Provider.ContactsContract.RawContacts

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string Pinned = "pinned";
```

### Type Changed: Android.Provider.ContactsContract.Data

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added field:

```
public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.Entity

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added field:

```
public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.StreamItems

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const string ContentDirectory = "stream_items";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string AccountName = "account_name";

	[Obsolete ("deprecated")]
	public static const string AccountType = "account_type";

	[Obsolete ("deprecated")]
	public static const string Comments = "comments";

	[Obsolete ("deprecated")]
	public static const string ContactId = "contact_id";

	[Obsolete ("deprecated")]
	public static const string ContactLookupKey = "contact_lookup";

	[Obsolete ("deprecated")]
	public static const string DataSet = "data_set";

	[Obsolete ("deprecated")]
	public static const string RawContactId = "raw_contact_id";

	[Obsolete ("deprecated")]
	public static const string RawContactSourceId = "raw_contact_source_id";

	[Obsolete ("deprecated")]
	public static const string ResIcon = "icon";

	[Obsolete ("deprecated")]
	public static const string ResLabel = "label";

	[Obsolete ("deprecated")]
	public static const string ResPackage = "res_package";

	[Obsolete ("deprecated")]
	public static const string Sync1 = "stream_item_sync1";

	[Obsolete ("deprecated")]
	public static const string Sync2 = "stream_item_sync2";

	[Obsolete ("deprecated")]
	public static const string Sync3 = "stream_item_sync3";

	[Obsolete ("deprecated")]
	public static const string Sync4 = "stream_item_sync4";

	[Obsolete ("deprecated")]
	public static const string Text = "text";

	[Obsolete ("deprecated")]
	public static const string Timestamp = "timestamp";
```

### Type Changed: Android.Provider.ContactsContract.RawContactsColumns

Added field:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
```

### Type Changed: Android.Provider.ContactsContract.RawContactsEntity

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Added fields:

```
public static const string AccountTypeAndDataSet = "account_type_and_data_set";
	public static const string ResPackage = "res_package";
```

### Type Changed: Android.Provider.ContactsContract.StreamItemPhotos

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const string Photo = "photo";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string PhotoFileId = "photo_file_id";

	[Obsolete ("deprecated")]
	public static const string PhotoUri = "photo_uri";

	[Obsolete ("deprecated")]
	public static const string SortIndex = "sort_index";

	[Obsolete ("deprecated")]
	public static const string StreamItemId = "stream_item_id";

	[Obsolete ("deprecated")]
	public static const string Sync1 = "stream_item_photo_sync1";

	[Obsolete ("deprecated")]
	public static const string Sync2 = "stream_item_photo_sync2";

	[Obsolete ("deprecated")]
	public static const string Sync3 = "stream_item_photo_sync3";

	[Obsolete ("deprecated")]
	public static const string Sync4 = "stream_item_photo_sync4";
```

### Type Changed: Android.Provider.ContactsContract.StreamItemPhotosColumns

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string PhotoFileId = "photo_file_id";

	[Obsolete ("deprecated")]
	public static const string PhotoUri = "photo_uri";

	[Obsolete ("deprecated")]
	public static const string SortIndex = "sort_index";

	[Obsolete ("deprecated")]
	public static const string StreamItemId = "stream_item_id";

	[Obsolete ("deprecated")]
	public static const string Sync1 = "stream_item_photo_sync1";

	[Obsolete ("deprecated")]
	public static const string Sync2 = "stream_item_photo_sync2";

	[Obsolete ("deprecated")]
	public static const string Sync3 = "stream_item_photo_sync3";

	[Obsolete ("deprecated")]
	public static const string Sync4 = "stream_item_photo_sync4";
```

### Type Changed: Android.Provider.ContactsContract.StreamItems

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string ContentItemType = "vnd.android.cursor.item/stream_item";

	[Obsolete ("deprecated")]
	public static const string ContentType = "vnd.android.cursor.dir/stream_item";

	[Obsolete ("deprecated")]
	public static const string MaxItems = "max_items";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string AccountName = "account_name";

	[Obsolete ("deprecated")]
	public static const string AccountType = "account_type";

	[Obsolete ("deprecated")]
	public static const string Comments = "comments";

	[Obsolete ("deprecated")]
	public static const string ContactId = "contact_id";

	[Obsolete ("deprecated")]
	public static const string ContactLookupKey = "contact_lookup";

	[Obsolete ("deprecated")]
	public static const string DataSet = "data_set";

	[Obsolete ("deprecated")]
	public static const string RawContactId = "raw_contact_id";

	[Obsolete ("deprecated")]
	public static const string RawContactSourceId = "raw_contact_source_id";

	[Obsolete ("deprecated")]
	public static const string ResIcon = "icon";

	[Obsolete ("deprecated")]
	public static const string ResLabel = "label";

	[Obsolete ("deprecated")]
	public static const string ResPackage = "res_package";

	[Obsolete ("deprecated")]
	public static const string Sync1 = "stream_item_sync1";

	[Obsolete ("deprecated")]
	public static const string Sync2 = "stream_item_sync2";

	[Obsolete ("deprecated")]
	public static const string Sync3 = "stream_item_sync3";

	[Obsolete ("deprecated")]
	public static const string Sync4 = "stream_item_sync4";

	[Obsolete ("deprecated")]
	public static const string Text = "text";

	[Obsolete ("deprecated")]
	public static const string Timestamp = "timestamp";
```

### Type Changed: Android.Provider.ContactsContract.StreamItemPhotos

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string ContentDirectory = "photo";

	[Obsolete ("deprecated")]
	public static const string ContentItemType = "vnd.android.cursor.item/stream_item_photo";

	[Obsolete ("deprecated")]
	public static const string ContentType = "vnd.android.cursor.dir/stream_item_photo";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string PhotoFileId = "photo_file_id";

	[Obsolete ("deprecated")]
	public static const string PhotoUri = "photo_uri";

	[Obsolete ("deprecated")]
	public static const string SortIndex = "sort_index";

	[Obsolete ("deprecated")]
	public static const string StreamItemId = "stream_item_id";

	[Obsolete ("deprecated")]
	public static const string Sync1 = "stream_item_photo_sync1";

	[Obsolete ("deprecated")]
	public static const string Sync2 = "stream_item_photo_sync2";

	[Obsolete ("deprecated")]
	public static const string Sync3 = "stream_item_photo_sync3";

	[Obsolete ("deprecated")]
	public static const string Sync4 = "stream_item_photo_sync4";
```

### Type Changed: Android.Provider.ContactsContract.StreamItemsColumns

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string AccountName = "account_name";

	[Obsolete ("deprecated")]
	public static const string AccountType = "account_type";

	[Obsolete ("deprecated")]
	public static const string Comments = "comments";

	[Obsolete ("deprecated")]
	public static const string ContactId = "contact_id";

	[Obsolete ("deprecated")]
	public static const string ContactLookupKey = "contact_lookup";

	[Obsolete ("deprecated")]
	public static const string DataSet = "data_set";

	[Obsolete ("deprecated")]
	public static const string RawContactId = "raw_contact_id";

	[Obsolete ("deprecated")]
	public static const string RawContactSourceId = "raw_contact_source_id";

	[Obsolete ("deprecated")]
	public static const string ResIcon = "icon";

	[Obsolete ("deprecated")]
	public static const string ResLabel = "label";

	[Obsolete ("deprecated")]
	public static const string ResPackage = "res_package";

	[Obsolete ("deprecated")]
	public static const string Sync1 = "stream_item_sync1";

	[Obsolete ("deprecated")]
	public static const string Sync2 = "stream_item_sync2";

	[Obsolete ("deprecated")]
	public static const string Sync3 = "stream_item_sync3";

	[Obsolete ("deprecated")]
	public static const string Sync4 = "stream_item_sync4";

	[Obsolete ("deprecated")]
	public static const string Text = "text";

	[Obsolete ("deprecated")]
	public static const string Timestamp = "timestamp";
```

### New Type Android.Provider.PinnedPositions

```
public sealed class PinnedPositions : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public ContactsContract ();
	// fields
	public static const int Demoted;
	public static const int Unpinned;
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static void Pin (Android.Content.ContentResolver contentResolver, long contactId, int pinnedPosition);
	public static void Undemote (Android.Content.ContentResolver contentResolver, long contactId);
}
```

### New Type Android.Provider.SearchSnippets

```
public class SearchSnippets : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ContactsContract (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ContactsContract ();
	// fields
	public static const string DeferredSnippetingKey = "deferred_snippeting";
	public static const string Snippet = "snippet";
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### Type Changed: Android.Provider.DocumentContractFlags

Added value:

```
SupportsRename = 64,
```

### Type Changed: Android.Provider.DocumentRootFlags

Added value:

```
SupportsIsChild = 16,
```

### Type Changed: Android.Provider.DocumentsContract

Added methods:

```
public static Android.Net.Uri BuildChildDocumentsUriUsingTree (Android.Net.Uri treeUri, string parentDocumentId);
	public static Android.Net.Uri BuildDocumentUriUsingTree (Android.Net.Uri treeUri, string documentId);
	public static Android.Net.Uri BuildTreeDocumentUri (string authority, string documentId);
	public static Android.Net.Uri CreateDocument (Android.Content.ContentResolver resolver, Android.Net.Uri parentDocumentUri, string mimeType, string displayName);
	public static string GetTreeDocumentId (Android.Net.Uri documentUri);
	public static Android.Net.Uri RenameDocument (Android.Content.ContentResolver resolver, Android.Net.Uri documentUri, string displayName);
```

### Type Changed: Android.Provider.DocumentsContract.Document

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Provider.DocumentContractFlags enum directly instead of this field.")]
	public static const DocumentContractFlags FlagSupportsRename;
```

### Type Changed: Android.Provider.DocumentsContract.Root

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Provider.DocumentRootFlags enum directly instead of this field.")]
	public static const DocumentRootFlags FlagSupportsIsChild;
```

### Type Changed: Android.Provider.DocumentsProvider

Added methods:

```
public virtual bool IsChildDocument (string parentDocumentId, string documentId);
	public override Android.Content.Res.AssetFileDescriptor OpenAssetFile (Android.Net.Uri uri, string mode);
	public override Android.Content.Res.AssetFileDescriptor OpenAssetFile (Android.Net.Uri uri, string mode, Android.OS.CancellationSignal signal);
	public virtual string RenameDocument (string documentId, string displayName);
	public void RevokeDocumentPermission (string documentId);
```

### Type Changed: Android.Provider.MediaStore

Added fields:

```
public static const string ExtraMediaGenre = "android.intent.extra.genre";
	public static const string ExtraMediaPlaylist = "android.intent.extra.playlist";
	public static const string ExtraMediaRadioChannel = "android.intent.extra.radio_channel";
```

### Type Changed: Android.Provider.MediaStore.Audio

### Type Changed: Android.Provider.MediaStore.Media

Added field:

```
public static const string EntryContentType = "vnd.android.cursor.item/audio";
```

### New Type Android.Provider.Radio

```
public sealed class Radio : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const string EntryContentType = "vnd.android.cursor.item/radio";
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### Type Changed: Android.Provider.MessageBoxType

Added value:

```
Failed = 5,
```

### Type Changed: Android.Provider.Settings

Added fields:

```
public static const string ActionCastSettings = "android.settings.CAST_SETTINGS";
	public static const string ActionHomeSettings = "android.settings.HOME_SETTINGS";
	public static const string ActionShowRegulatoryInfo = "android.settings.SHOW_REGULATORY_INFO";
	public static const string ActionUsageAccessSettings = "android.settings.USAGE_ACCESS_SETTINGS";
	public static const string ActionVoiceInputSettings = "android.settings.VOICE_INPUT_SETTINGS";
```

### Type Changed: Android.Provider.Settings.Secure

Added fields:

```
public static const string AccessibilityDisplayInversionEnabled = "accessibility_display_inversion_enabled";
	public static const string SkipFirstUseHints = "skip_first_use_hints";
```

### Type Changed: Android.Provider.Settings.System

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const string NextAlarmFormatted = "next_alarm_formatted";
```

### Type Changed: Android.Provider.Telephony

### Type Changed: Android.Provider.Telephony.BaseMmsColumns

Added fields:

```
public static const string Creator = "creator";

	[Obsolete ("This constant will be removed in the future version. Use Android.Provider.MessageBoxType enum directly instead of this field.")]
	public static const MessageBoxType MessageBoxFailed;
```

### Type Changed: Android.Provider.Telephony.Mms

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added fields:

```
public static const string Creator = "creator";

	[Obsolete ("This constant will be removed in the future version. Use Android.Provider.MessageBoxType enum directly instead of this field.")]
	public static const MessageBoxType MessageBoxFailed;
```

### Type Changed: Android.Provider.Telephony.Draft

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added fields:

```
public static const string Creator = "creator";

	[Obsolete ("This constant will be removed in the future version. Use Android.Provider.MessageBoxType enum directly instead of this field.")]
	public static const MessageBoxType MessageBoxFailed;
```

### Type Changed: Android.Provider.Telephony.Inbox

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added fields:

```
public static const string Creator = "creator";

	[Obsolete ("This constant will be removed in the future version. Use Android.Provider.MessageBoxType enum directly instead of this field.")]
	public static const MessageBoxType MessageBoxFailed;
```

### Type Changed: Android.Provider.Telephony.Outbox

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added fields:

```
public static const string Creator = "creator";

	[Obsolete ("This constant will be removed in the future version. Use Android.Provider.MessageBoxType enum directly instead of this field.")]
	public static const MessageBoxType MessageBoxFailed;
```

### Type Changed: Android.Provider.Telephony.Sent

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added fields:

```
public static const string Creator = "creator";

	[Obsolete ("This constant will be removed in the future version. Use Android.Provider.MessageBoxType enum directly instead of this field.")]
	public static const MessageBoxType MessageBoxFailed;
```

### Type Changed: Android.Provider.Telephony.Sms

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

```
public static const string Creator = "creator";
```

### Type Changed: Android.Provider.Telephony.Conversations

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

```
public static const string Creator = "creator";
```

### Type Changed: Android.Provider.Telephony.Draft

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

```
public static const string Creator = "creator";
```

### Type Changed: Android.Provider.Telephony.Inbox

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

```
public static const string Creator = "creator";
```

### Type Changed: Android.Provider.Telephony.Outbox

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

```
public static const string Creator = "creator";
```

### Type Changed: Android.Provider.Telephony.Sent

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

```
public static const string Creator = "creator";
```

### Type Changed: Android.Provider.Telephony.TextBasedSmsColumns

Added field:

```
public static const string Creator = "creator";
```

### Type Changed: Android.Provider.Telephony.Threads

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

```
public static const string Archived = "archived";
```

### Type Changed: Android.Provider.Telephony.ThreadsColumns

Added field:

```
public static const string Archived = "archived";
```

### Type Changed: Android.Provider.VoicemailContract

### Type Changed: Android.Provider.VoicemailContract.Voicemails

Added field:

```
public static const string Transcription = "transcription";
```

## Namespace Android.Renderscripts

### Type Changed: Android.Renderscripts.Allocation

Added methods:

```
public virtual void Copy1DRangeFrom (int off, int count, Java.Lang.Object array);
	public virtual void Copy1DRangeFromUnchecked (int off, int count, Java.Lang.Object array);
	public virtual void Copy2DRangeFrom (int xoff, int yoff, int w, int h, Java.Lang.Object array);
	public virtual void CopyFrom (Java.Lang.Object array);
	public virtual void CopyFromUnchecked (Java.Lang.Object array);
	public virtual void CopyTo (Java.Lang.Object array);
```

### Type Changed: Android.Renderscripts.RenderScript

Added method:

```
public static RenderScript Create (Android.Content.Context ctx, RenderScript.ContextType ct, int flags);
```

### Type Changed: Android.Renderscripts.ScriptC

Added constructors:

```
protected ScriptC (RenderScript rs, string resName, byte[] bitcode32, byte[] bitcode64);
	protected ScriptC (long id, RenderScript rs);
```

### Type Changed: Android.Renderscripts.ScriptIntrinsic3DLUT

Added method:

```
public void ForEach (Allocation ain, Allocation aout, Script.LaunchOptions opt);
```

### Type Changed: Android.Renderscripts.ScriptIntrinsicBlend

Added methods:

```
public virtual void ForEachAdd (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachClear (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachDst (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachDstAtop (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachDstIn (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachDstOut (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachDstOver (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachMultiply (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachSrc (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachSrcAtop (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachSrcIn (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachSrcOut (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachSrcOver (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachSubtract (Allocation ain, Allocation aout, Script.LaunchOptions opt);
	public virtual void ForEachXor (Allocation ain, Allocation aout, Script.LaunchOptions opt);
```

### Type Changed: Android.Renderscripts.ScriptIntrinsicBlur

Added method:

```
public void ForEach (Allocation aout, Script.LaunchOptions opt);
```

### Type Changed: Android.Renderscripts.ScriptIntrinsicColorMatrix

Added method:

```
public void ForEach (Allocation ain, Allocation aout, Script.LaunchOptions opt);
```

### Type Changed: Android.Renderscripts.ScriptIntrinsicConvolve3x3

Added method:

```
public void ForEach (Allocation aout, Script.LaunchOptions opt);
```

### Type Changed: Android.Renderscripts.ScriptIntrinsicConvolve5x5

Added method:

```
public void ForEach (Allocation aout, Script.LaunchOptions opt);
```

### Type Changed: Android.Renderscripts.ScriptIntrinsicHistogram

Added methods:

```
public void ForEach (Allocation ain, Script.LaunchOptions opt);
	public void ForEach_Dot (Allocation ain, Script.LaunchOptions opt);
```

### Type Changed: Android.Renderscripts.ScriptIntrinsicLUT

Added method:

```
public void ForEach (Allocation ain, Allocation aout, Script.LaunchOptions opt);
```

### Type Changed: Android.Renderscripts.Type

Added methods:

```
public static Type CreateX (RenderScript rs, Element e, int dimX);
	public static Type CreateXY (RenderScript rs, Element e, int dimX, int dimY);
	public static Type CreateXYZ (RenderScript rs, Element e, int dimX, int dimY, int dimZ);
```

### New Type Android.Renderscripts.CreateFlag

```
[Serializable]
public enum CreateFlag {
	LowLatency = 2,
	LowPower = 4,
	None = 0,
}
```

## Namespace Android.Service.Dreams

### Type Changed: Android.Service.Dreams.DreamService

Added methods:

```
public virtual void OnWakeUp ();
	public void WakeUp ();
```

## Namespace Android.Service.Notification

### Type Changed: Android.Service.Notification.NotificationListenerService

Added properties:

```
public InterruptionFilterType CurrentInterruptionFilter { get; }
	public NotificationListenerServiceHint CurrentListenerHints { get; }
	public virtual NotificationListenerService.RankingMap CurrentRanking { get; }
```

Added methods:

```
public void CancelNotification (string key);
	public void CancelNotifications (string[] keys);
	public virtual StatusBarNotification[] GetActiveNotifications (string[] keys);
	public virtual void OnInterruptionFilterChanged (InterruptionFilterType interruptionFilter);
	public virtual void OnListenerConnected ();
	public virtual void OnListenerHintsChanged (NotificationListenerServiceHint hints);
	public virtual void OnNotificationPosted (StatusBarNotification sbn, NotificationListenerService.RankingMap rankingMap);
	public virtual void OnNotificationRankingUpdate (NotificationListenerService.RankingMap rankingMap);
	public virtual void OnNotificationRemoved (StatusBarNotification sbn, NotificationListenerService.RankingMap rankingMap);
	public void RequestInterruptionFilter (InterruptionFilterType interruptionFilter);
	public void RequestListenerHints (NotificationListenerServiceHint hints);
```

### Type Changed: Android.Service.Notification.StatusBarNotification

Added properties:

```
public virtual string GroupKey { get; }
	public virtual Android.OS.UserHandle User { get; }
```

### New Type Android.Service.Notification.InterruptionFilterType

```
[Serializable]
public enum InterruptionFilterType {
	All = 1,
	None = 3,
	Priority = 2,
}
```

### New Type Android.Service.Notification.NotificationListenerServiceHint

```
[Serializable]
public enum NotificationListenerServiceHint {
	HostDisableEffects = 1,
}
```

## Namespace Android.Service.Voice

### Type Changed: Android.Service.Voice.RecognitionFlag

Added values:

```
AllowMultipleTriggers = 2,
	CaptureTriggerAudio = 1,
```

### New Type Android.Service.Voice.AlwaysOnHotwordDetector

```
public class AlwaysOnHotwordDetector : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected AlwaysOnHotwordDetector (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.Content.Intent CreateEnrollIntent ();
	public virtual Android.Content.Intent CreateReEnrollIntent ();
	public virtual Android.Content.Intent CreateUnEnrollIntent ();
	public virtual bool StartRecognition (RecognitionFlag recognitionFlags);
	public virtual bool StopRecognition ();

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected AlwaysOnHotwordDetector (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public AlwaysOnHotwordDetector ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnAvailabilityChanged (HotwordDetectorState status);
		public virtual void OnDetected (AlwaysOnHotwordDetector.EventPayload eventPayload);
		public virtual void OnError ();
		public virtual void OnRecognitionPaused ();
		public virtual void OnRecognitionResumed ();
	}
	public class EventPayload : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected AlwaysOnHotwordDetector (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		public virtual Android.Media.AudioFormat CaptureAudioFormat { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual byte[] GetTriggerAudio ();
	}
}
```

### New Type Android.Service.Voice.HotwordDetectorState

```
[Serializable]
public enum HotwordDetectorState {
	HardwareUnavailable = -2,
	KeyphraseEnrolled = 2,
	KeyphraseUnenrolled = 1,
	KeyphraseUnsupported = -1,
}
```

### New Type Android.Service.Voice.RecognitionMode

```
[Serializable]
public enum RecognitionMode {
	UserIdentification = 2,
	VoiceTrigger = 1,
}
```

### New Type Android.Service.Voice.VoiceInteractionService

```
public class VoiceInteractionService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected VoiceInteractionService (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public VoiceInteractionService ();
	// fields
	public static const string ServiceInterface = "android.service.voice.VoiceInteractionService";
	public static const string ServiceMetaData = "android.voice_interaction";
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public AlwaysOnHotwordDetector CreateAlwaysOnHotwordDetector (string keyphrase, Java.Util.Locale locale, AlwaysOnHotwordDetector.Callback callback);
	public static bool IsActiveService (Android.Content.Context context, Android.Content.ComponentName service);
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual void OnReady ();
	public virtual void OnShutdown ();
	public virtual void StartSession (Android.OS.Bundle args);
}
```

### New Type Android.Service.Voice.VoiceInteractionSession

```
public abstract class VoiceInteractionSession : Java.Lang.Object, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected VoiceInteractionSession (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public VoiceInteractionSession (Android.Content.Context context);
	public VoiceInteractionSession (Android.Content.Context context, Android.OS.Handler handler);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Finish ();
	public virtual void OnCloseSystemDialogs ();
	public virtual void OnCreate (Android.OS.Bundle args);
	public virtual void OnDestroy ();
	public virtual bool OnKeyDown (Android.Views.Keycode p0, Android.Views.KeyEvent p1);
	public virtual bool OnKeyLongPress (Android.Views.Keycode p0, Android.Views.KeyEvent p1);
	public virtual bool OnKeyMultiple (Android.Views.Keycode p0, int p1, Android.Views.KeyEvent p2);
	public virtual bool OnKeyUp (Android.Views.Keycode p0, Android.Views.KeyEvent p1);
	public virtual void SetContentView (Android.Views.View view);
}
```

### New Type Android.Service.Voice.VoiceInteractionSessionService

```
public abstract class VoiceInteractionSessionService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected VoiceInteractionSessionService (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public VoiceInteractionSessionService ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual VoiceInteractionSession OnNewSession (Android.OS.Bundle args);
}
```

## Namespace Android.Service.Wallpaper

### Type Changed: Android.Service.Wallpaper.WallpaperService

### Type Changed: Android.Service.Wallpaper.WallpaperService.Engine

Added method:

```
public virtual void OnApplyWindowInsets (Android.Views.WindowInsets insets);
```

## Namespace Android.Speech.Tts

### Type Changed: Android.Speech.Tts.ISynthesisCallback

Added properties:

```
public virtual bool HasFinished { get; }
	public virtual bool HasStarted { get; }
```

Added method:

```
public virtual void Error (TextToSpeechError errorCode);
```

### Type Changed: Android.Speech.Tts.OperationResult

Added value:

```
Stopped = -2,
```

### Type Changed: Android.Speech.Tts.SynthesisRequest

Added constructor:

```
public SynthesisRequest (Java.Lang.ICharSequence text, Android.OS.Bundle params);
```

Added properties:

```
public string CharSequenceText { get; }
	public Java.Lang.ICharSequence CharSequenceTextFormatted { get; }
	public string VoiceName { get; }
```

Obsoleted property:

```
[Obsolete ("deprecated")]
	public string Text { get; }
```

### Type Changed: Android.Speech.Tts.TextToSpeech

Added properties:

```
public virtual System.Collections.Generic.ICollection<Java.Util.Locale> AvailableLanguages { get; }
	public virtual Voice DefaultVoice { get; }
	public virtual Voice Voice { get; }
	public virtual System.Collections.Generic.ICollection<Voice> Voices { get; }
```

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual Java.Util.Locale DefaultLanguage { get; }

	[Obsolete ("deprecated")]
	public virtual Java.Util.Locale Language { get; }
```

Added methods:

```
public virtual OperationResult AddEarcon (string earcon, Java.IO.File file);
	public virtual OperationResult AddSpeech (Java.Lang.ICharSequence text, string packagename, int resourceId);
	public OperationResult AddSpeech (string text, Java.IO.File file);
	public virtual OperationResult AddSpeech (Java.Lang.ICharSequence text, Java.IO.File file);
	public virtual OperationResult PlayEarcon (string earcon, QueueMode queueMode, Android.OS.Bundle params, string utteranceId);
	public virtual OperationResult PlaySilentUtterance (long durationInMs, QueueMode queueMode, string utteranceId);
	public virtual OperationResult SetAudioAttributes (Android.Media.AudioAttributes audioAttributes);
	public virtual OperationResult SetVoice (Voice voice);
	public OperationResult Speak (string text, QueueMode queueMode, Android.OS.Bundle params, string utteranceId);
	public virtual OperationResult Speak (Java.Lang.ICharSequence text, QueueMode queueMode, Android.OS.Bundle params, string utteranceId);
	public virtual OperationResult SynthesizeToFile (Java.Lang.ICharSequence text, Android.OS.Bundle params, Java.IO.File file, string utteranceId);
	public OperationResult SynthesizeToFile (string text, Android.OS.Bundle params, Java.IO.File file, string utteranceId);
```

### Type Changed: Android.Speech.Tts.TextToSpeech.Engine

Added fields:

```
public static const string KeyFeatureNetworkRetriesCount = "networkRetriesCount";
	public static const string KeyFeatureNetworkTimeoutMs = "networkTimeoutMs";
	public static const string KeyFeatureNotInstalled = "notInstalled";
	public static const string KeyParamSessionId = "sessionId";
```

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string KeyFeatureEmbeddedSynthesis = "embeddedTts";

	[Obsolete ("deprecated")]
	public static const string KeyFeatureNetworkSynthesis = "networkTts";
```

### Type Changed: Android.Speech.Tts.TextToSpeechService

Added methods:

```
public virtual string OnGetDefaultVoiceNameFor (string lang, string country, string variant);
	public virtual System.Collections.Generic.IList<Voice> OnGetVoices ();
	public virtual OperationResult OnIsValidVoiceName (string voiceName);
	public virtual OperationResult OnLoadVoice (string voiceName);
```

### Type Changed: Android.Speech.Tts.UtteranceProgressListener

Added method:

```
public virtual void OnError (string utteranceId, TextToSpeechError errorCode);
```

### New Type Android.Speech.Tts.TextToSpeechError

```
[Serializable]
public enum TextToSpeechError {
	InvalidRequest = -8,
	Network = -6,
	NetworkTimeout = -7,
	NotInstalledYet = -9,
	Output = -5,
	Service = -4,
	Synthesis = -3,
}
```

### New Type Android.Speech.Tts.Voice

```
public class Voice : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected Voice (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Voice (string name, Java.Util.Locale locale, VoiceQuality quality, VoiceLatency latency, bool requiresNetworkConnection, System.Collections.Generic.ICollection<string> features);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual System.Collections.Generic.ICollection<string> Features { get; }
	public virtual bool IsNetworkConnectionRequired { get; }
	public virtual VoiceLatency Latency { get; }
	public virtual Java.Util.Locale Locale { get; }
	public virtual string Name { get; }
	public virtual VoiceQuality Quality { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Speech.Tts.VoiceLatency

```
[Serializable]
public enum VoiceLatency {
	High = 400,
	Low = 200,
	Normal = 300,
	VeryHigh = 500,
	VeryLow = 100,
}
```

### New Type Android.Speech.Tts.VoiceQuality

```
[Serializable]
public enum VoiceQuality {
	High = 400,
	Low = 200,
	Normal = 300,
	VeryHigh = 500,
	VeryLow = 100,
}
```

## Namespace Android.Telephony

### Type Changed: Android.Telephony.PhoneNumberFormattingTextWatcher

Added constructor:

```
public PhoneNumberFormattingTextWatcher (string countryCode);
```

### Type Changed: Android.Telephony.PhoneNumberUtils

Added methods:

```
public static string FormatNumber (string phoneNumber, string phoneNumberE164, string defaultCountryIso);
	public static string FormatNumber (string phoneNumber, string defaultCountryIso);
	public static string FormatNumberToE164 (string phoneNumber, string defaultCountryIso);
	public static bool IsLocalEmergencyNumber (Android.Content.Context context, string number);
	public static bool IsVoiceMailNumber (string number);
	public static string NormalizeNumber (string phoneNumber);
	public static string ReplaceUnicodeDigits (string number);
```

### Type Changed: Android.Telephony.SmsManager

Added fields:

```
public static const string ExtraMmsData = "android.telephony.extra.MMS_DATA";
	public static const string MmsConfigAliasEnabled = "aliasEnabled";
	public static const string MmsConfigAliasMaxChars = "aliasMaxChars";
	public static const string MmsConfigAliasMinChars = "aliasMinChars";
	public static const string MmsConfigAllowAttachAudio = "allowAttachAudio";
	public static const string MmsConfigAppendTransactionId = "enabledTransID";
	public static const string MmsConfigEmailGatewayNumber = "emailGatewayNumber";
	public static const string MmsConfigGroupMmsEnabled = "enableGroupMms";
	public static const string MmsConfigHttpParams = "httpParams";
	public static const string MmsConfigHttpSocketTimeout = "httpSocketTimeout";
	public static const string MmsConfigMaxImageHeight = "maxImageHeight";
	public static const string MmsConfigMaxImageWidth = "maxImageWidth";
	public static const string MmsConfigMaxMessageSize = "maxMessageSize";
	public static const string MmsConfigMessageTextMaxSize = "maxMessageTextSize";
	public static const string MmsConfigMmsDeliveryReportEnabled = "enableMMSDeliveryReports";
	public static const string MmsConfigMmsEnabled = "enabledMMS";
	public static const string MmsConfigMmsReadReportEnabled = "enableMMSReadReports";
	public static const string MmsConfigMultipartSmsEnabled = "enableMultipartSMS";
	public static const string MmsConfigNaiSuffix = "naiSuffix";
	public static const string MmsConfigNotifyWapMmscEnabled = "enabledNotifyWapMMSC";
	public static const string MmsConfigRecipientLimit = "recipientLimit";
	public static const string MmsConfigSendMultipartSmsAsSeparateMessages = "sendMultipartSmsAsSeparateMessages";
	public static const string MmsConfigSmsDeliveryReportEnabled = "enableSMSDeliveryReports";
	public static const string MmsConfigSmsToMmsTextLengthThreshold = "smsToMmsTextLengthThreshold";
	public static const string MmsConfigSmsToMmsTextThreshold = "smsToMmsTextThreshold";
	public static const string MmsConfigSubjectMaxLength = "maxSubjectLength";
	public static const string MmsConfigSupportMmsContentDisposition = "supportMmsContentDisposition";
	public static const string MmsConfigUaProfTagName = "uaProfTagName";
	public static const string MmsConfigUaProfUrl = "uaProfUrl";
	public static const string MmsConfigUserAgent = "userAgent";
```

Added property:

```
public Android.OS.Bundle CarrierConfigValues { get; }
```

Added methods:

```
public void DownloadMultimediaMessage (Android.Content.Context context, string locationUrl, Android.Net.Uri contentUri, Android.OS.Bundle configOverrides, Android.App.PendingIntent downloadedIntent);
	public void SendMultimediaMessage (Android.Content.Context context, Android.Net.Uri contentUri, string locationUrl, Android.OS.Bundle configOverrides, Android.App.PendingIntent sentIntent);
```

### Type Changed: Android.Telephony.TelephonyManager

Added property:

```
public virtual bool IsSmsCapable { get; }
```

Added methods:

```
public virtual bool IccCloseLogicalChannel (int channel);
	public virtual byte[] IccExchangeSimIO (int fileID, int command, int p1, int p2, int p3, string filePath);
	public virtual IccOpenLogicalChannelResponse IccOpenLogicalChannel (string AID);
	public virtual string IccTransmitApduBasicChannel (int cla, int instruction, int p1, int p2, int p3, string data);
	public virtual string IccTransmitApduLogicalChannel (int channel, int cla, int instruction, int p1, int p2, int p3, string data);
	public virtual string SendEnvelopeWithStatus (string content);
```

### New Type Android.Telephony.IccOpenLogicalChannelResponse

```
public class IccOpenLogicalChannelResponse : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected IccOpenLogicalChannelResponse (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const int InvalidChannel;

	[Obsolete ("This constant will be removed in the future version. Use Android.Telephony.IccOpenLogicalChannelResponseStatus enum directly instead of this field.")]
	public static const IccOpenLogicalChannelResponseStatus StatusMissingResource;

	[Obsolete ("This constant will be removed in the future version. Use Android.Telephony.IccOpenLogicalChannelResponseStatus enum directly instead of this field.")]
	public static const IccOpenLogicalChannelResponseStatus StatusNoError;

	[Obsolete ("This constant will be removed in the future version. Use Android.Telephony.IccOpenLogicalChannelResponseStatus enum directly instead of this field.")]
	public static const IccOpenLogicalChannelResponseStatus StatusNoSuchElement;

	[Obsolete ("This constant will be removed in the future version. Use Android.Telephony.IccOpenLogicalChannelResponseStatus enum directly instead of this field.")]
	public static const IccOpenLogicalChannelResponseStatus StatusUnknownError;
	// properties
	public virtual int Channel { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual int Status { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual byte[] GetSelectResponse ();
	public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Telephony.IccOpenLogicalChannelResponseStatus

```
[Serializable]
public enum IccOpenLogicalChannelResponseStatus {
	MissingResource = 2,
	NoError = 1,
	NoSuchElement = 3,
	UnknownError = 4,
}
```

### New Type Android.Telephony.MmsError

```
[Serializable]
public enum MmsError {
	ConfigurationError = 7,
	HttpFailure = 4,
	InvalidApn = 2,
	IoError = 5,
	Retry = 6,
	UnableConnectMms = 3,
	Unspecified = 1,
}
```

## Namespace Android.Test.Mock

### Type Changed: Android.Test.Mock.MockContext

Added properties:

```
public override Java.IO.File CodeCacheDir { get; }
	public override Java.IO.File NoBackupFilesDir { get; }
```

Added method:

```
public override Java.IO.File[] GetExternalMediaDirs ();
```

### Type Changed: Android.Test.Mock.MockPackageManager

Added property:

```
public override Android.Content.PM.PackageInstaller PackageInstaller { get; }
```

Added methods:

```
public override Android.Content.Intent GetLeanbackLaunchIntentForPackage (string packageName);
	public override Android.Graphics.Drawables.Drawable GetUserBadgedDrawableForDensity (Android.Graphics.Drawables.Drawable drawable, Android.OS.UserHandle user, Android.Graphics.Rect badgeLocation, int badgeDensity);
	public override Android.Graphics.Drawables.Drawable GetUserBadgedIcon (Android.Graphics.Drawables.Drawable icon, Android.OS.UserHandle user);
	public string GetUserBadgedLabel (string label, Android.OS.UserHandle user);
	public override Java.Lang.ICharSequence GetUserBadgedLabelFormatted (Java.Lang.ICharSequence label, Android.OS.UserHandle user);
```

## Namespace Android.Text

### Type Changed: Android.Text.InputFilterLengthFilter

Added property:

```
public virtual int Max { get; }
```

### Type Changed: Android.Text.SpannableStringBuilder

Removed method:

```
public virtual int GetTextRunCursor (int contextStart, int contextEnd, int flags, int offset, int cursorOpt, Android.Graphics.Paint p);
```

Added methods:

```
public Java.Lang.IAppendable Append (string text, Java.Lang.Object what, SpanTypes flags);
	public virtual Java.Lang.IAppendable Append (Java.Lang.ICharSequence text, Java.Lang.Object what, SpanTypes flags);
	public virtual int GetTextRunCursor (int contextStart, int contextEnd, int dir, int offset, int cursorOpt, Android.Graphics.Paint p);
```

## Namespace Android.Text.Format

### Type Changed: Android.Text.Format.Time

Removed constructor:

```
public Time (string timezone);
```

Added constructor:

```
public Time (string timezoneId);
```

Removed method:

```
public virtual void Clear (string timezone);
```

Added method:

```
public virtual void Clear (string timezoneId);
```

## Namespace Android.Text.Style

### New Type Android.Text.Style.TtsSpan

```
public class TtsSpan : Java.Lang.Object, Android.Text.IParcelableSpan, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TtsSpan (string type, Android.OS.PersistableBundle args);
	public TtsSpan (Android.OS.Parcel src);
	// fields
	public static const string AnimacyAnimate = "android.animate";
	public static const string AnimacyInanimate = "android.inanimate";
	public static const string ArgAnimacy = "android.arg.animacy";
	public static const string ArgCase = "android.arg.case";
	public static const string ArgCountryCode = "android.arg.country_code";
	public static const string ArgCurrency = "android.arg.money";
	public static const string ArgDay = "android.arg.day";
	public static const string ArgDenominator = "android.arg.denominator";
	public static const string ArgDigits = "android.arg.digits";
	public static const string ArgDomain = "android.arg.domain";
	public static const string ArgExtension = "android.arg.extension";
	public static const string ArgFractionalPart = "android.arg.fractional_part";
	public static const string ArgFragmentId = "android.arg.fragment_id";
	public static const string ArgGender = "android.arg.gender";
	public static const string ArgHours = "android.arg.hours";
	public static const string ArgIntegerPart = "android.arg.integer_part";
	public static const string ArgMinutes = "android.arg.minutes";
	public static const string ArgMonth = "android.arg.month";
	public static const string ArgMultiplicity = "android.arg.multiplicity";
	public static const string ArgNumber = "android.arg.number";
	public static const string ArgNumberParts = "android.arg.number_parts";
	public static const string ArgNumerator = "android.arg.numerator";
	public static const string ArgPassword = "android.arg.password";
	public static const string ArgPath = "android.arg.path";
	public static const string ArgPort = "android.arg.port";
	public static const string ArgProtocol = "android.arg.protocol";
	public static const string ArgQuantity = "android.arg.quantity";
	public static const string ArgQueryString = "android.arg.query_string";
	public static const string ArgText = "android.arg.text";
	public static const string ArgUnit = "android.arg.unit";
	public static const string ArgUsername = "android.arg.username";
	public static const string ArgVerbatim = "android.arg.verbatim";
	public static const string ArgWeekday = "android.arg.weekday";
	public static const string ArgYear = "android.arg.year";
	public static const string CaseAblative = "android.ablative";
	public static const string CaseAccusative = "android.accusative";
	public static const string CaseDative = "android.dative";
	public static const string CaseGenitive = "android.genitive";
	public static const string CaseInstrumental = "android.instrumental";
	public static const string CaseLocative = "android.locative";
	public static const string CaseNominative = "android.nominative";
	public static const string CaseVocative = "android.vocative";
	public static const string GenderFemale = "android.female";
	public static const string GenderMale = "android.male";
	public static const string GenderNeutral = "android.neutral";
	public static const string MultiplicityDual = "android.dual";
	public static const string MultiplicityPlural = "android.plural";
	public static const string MultiplicitySingle = "android.single";
	public static const string TypeCardinal = "android.type.cardinal";
	public static const string TypeDate = "android.type.date";
	public static const string TypeDecimal = "android.type.decimal";
	public static const string TypeDigits = "android.type.digits";
	public static const string TypeElectronic = "android.type.electronic";
	public static const string TypeFraction = "android.type.fraction";
	public static const string TypeMeasure = "android.type.measure";
	public static const string TypeMoney = "android.type.money";
	public static const string TypeOrdinal = "android.type.ordinal";
	public static const string TypeTelephone = "android.type.telephone";
	public static const string TypeText = "android.type.text";
	public static const string TypeTime = "android.type.time";
	public static const string TypeVerbatim = "android.type.verbatim";
	// properties
	public virtual Android.OS.PersistableBundle Args { get; }
	public virtual int SpanTypeId { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual string Type { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan (string type);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan Build ();
		public virtual Java.Lang.Object SetIntArgument (string arg, int value);
		public virtual Java.Lang.Object SetLongArgument (string arg, long value);
		public virtual Java.Lang.Object SetStringArgument (string arg, string value);
	}
	public class CardinalBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan (string number);
		public TtsSpan (long number);
		public TtsSpan ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.CardinalBuilder SetNumber (string number);
		public virtual TtsSpan.CardinalBuilder SetNumber (long number);
	}
	public class DateBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		public TtsSpan (Java.Lang.Integer weekday, Java.Lang.Integer day, Java.Lang.Integer month, Java.Lang.Integer year);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.DateBuilder SetDay (int day);
		public virtual TtsSpan.DateBuilder SetMonth (int month);
		public virtual TtsSpan.DateBuilder SetWeekday (Android.Text.Format.DayOfWeek weekday);
		public virtual TtsSpan.DateBuilder SetYear (int year);
	}
	public class DecimalBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan (string integerPart, string fractionalPart);
		public TtsSpan (double number, int minimumFractionDigits, int maximumFractionDigits);
		public TtsSpan ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.DecimalBuilder SetArgumentsFromDouble (double number, int minimumFractionDigits, int maximumFractionDigits);
		public virtual TtsSpan.DecimalBuilder SetFractionalPart (string fractionalPart);
		public virtual TtsSpan.DecimalBuilder SetIntegerPart (string integerPart);
		public virtual TtsSpan.DecimalBuilder SetIntegerPart (long integerPart);
	}
	public class DigitsBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		public TtsSpan (string digits);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.DigitsBuilder SetDigits (string digits);
	}
	public class ElectronicBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.ElectronicBuilder SetDomain (string domain);
		public virtual TtsSpan.ElectronicBuilder SetEmailArguments (string username, string domain);
		public virtual TtsSpan.ElectronicBuilder SetFragmentId (string fragmentId);
		public virtual TtsSpan.ElectronicBuilder SetPassword (string password);
		public virtual TtsSpan.ElectronicBuilder SetPath (string path);
		public virtual TtsSpan.ElectronicBuilder SetPort (int port);
		public virtual TtsSpan.ElectronicBuilder SetProtocol (string protocol);
		public virtual TtsSpan.ElectronicBuilder SetQueryString (string queryString);
		public virtual TtsSpan.ElectronicBuilder SetUsername (string username);
	}
	public class FractionBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		public TtsSpan (long integerPart, long numerator, long denominator);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.FractionBuilder SetDenominator (string denominator);
		public virtual TtsSpan.FractionBuilder SetDenominator (long denominator);
		public virtual TtsSpan.FractionBuilder SetIntegerPart (string integerPart);
		public virtual TtsSpan.FractionBuilder SetIntegerPart (long integerPart);
		public virtual TtsSpan.FractionBuilder SetNumerator (string numerator);
		public virtual TtsSpan.FractionBuilder SetNumerator (long numerator);
	}
	public class MeasureBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.MeasureBuilder SetDenominator (string denominator);
		public virtual TtsSpan.MeasureBuilder SetDenominator (long denominator);
		public virtual TtsSpan.MeasureBuilder SetFractionalPart (string fractionalPart);
		public virtual TtsSpan.MeasureBuilder SetIntegerPart (long integerPart);
		public virtual TtsSpan.MeasureBuilder SetIntegerPart (string integerPart);
		public virtual TtsSpan.MeasureBuilder SetNumber (string number);
		public virtual TtsSpan.MeasureBuilder SetNumber (long number);
		public virtual TtsSpan.MeasureBuilder SetNumerator (string numerator);
		public virtual TtsSpan.MeasureBuilder SetNumerator (long numerator);
		public virtual TtsSpan.MeasureBuilder SetUnit (string unit);
	}
	public class MoneyBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.MoneyBuilder SetCurrency (string currency);
		public virtual TtsSpan.MoneyBuilder SetFractionalPart (string fractionalPart);
		public virtual TtsSpan.MoneyBuilder SetIntegerPart (string integerPart);
		public virtual TtsSpan.MoneyBuilder SetIntegerPart (long integerPart);
		public virtual TtsSpan.MoneyBuilder SetQuantity (string quantity);
	}
	public class OrdinalBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan (string number);
		public TtsSpan (long number);
		public TtsSpan ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.OrdinalBuilder SetNumber (string number);
		public virtual TtsSpan.OrdinalBuilder SetNumber (long number);
	}
	public class SemioticClassBuilder : Android.Text.Style.TtsSpan+Builder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan (string type);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual Java.Lang.Object SetAnimacy (string animacy);
		public virtual Java.Lang.Object SetCase (string grammaticalCase);
		public virtual Java.Lang.Object SetGender (string gender);
		public virtual Java.Lang.Object SetMultiplicity (string multiplicity);
	}
	public class TelephoneBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		public TtsSpan (string numberParts);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.TelephoneBuilder SetCountryCode (string countryCode);
		public virtual TtsSpan.TelephoneBuilder SetExtension (string extension);
		public virtual TtsSpan.TelephoneBuilder SetNumberParts (string numberParts);
	}
	public class TextBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		public TtsSpan (string text);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.TextBuilder SetText (string text);
	}
	public class TimeBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		public TtsSpan (int hours, int minutes);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.TimeBuilder SetHours (int hours);
		public virtual TtsSpan.TimeBuilder SetMinutes (int minutes);
	}
	public class VerbatimBuilder : Android.Text.Style.TtsSpan+SemioticClassBuilder, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TtsSpan (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TtsSpan ();
		public TtsSpan (string verbatim);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual TtsSpan.VerbatimBuilder SetVerbatim (string verbatim);
	}
}
```

### New Type Android.Text.Style.TtsSpanMonth

```
[Serializable]
public enum TtsSpanMonth {
	April = 3,
	August = 7,
	December = 11,
	February = 1,
	January = 0,
	July = 6,
	June = 5,
	March = 2,
	May = 4,
	November = 10,
	October = 9,
	September = 8,
}
```

### New Type Android.Text.Style.TtsSpanWeekday

```
[Serializable]
public enum TtsSpanWeekday {
	Friday = 6,
	Monday = 2,
	Saturday = 7,
	Sunday = 1,
	Thursday = 5,
	Tuesday = 3,
	Wednesday = 4,
}
```

## Namespace Android.Transitions

### Type Changed: Android.Transitions.AutoTransition

Added constructor:

```
public AutoTransition (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

### Type Changed: Android.Transitions.ChangeBounds

Added constructor:

```
public ChangeBounds (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

### Type Changed: Android.Transitions.Fade

Added constructor:

```
public Fade (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

### Type Changed: Android.Transitions.Scene

Added constructor:

```
public Scene (Android.Views.ViewGroup sceneRoot, Android.Views.View layout);
```

### Type Changed: Android.Transitions.Transition

Added constructor:

```
public Transition (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Transitions.MatchTarget enum directly instead of this field.")]
	public static const MatchTarget MatchId;

	[Obsolete ("This constant will be removed in the future version. Use Android.Transitions.MatchTarget enum directly instead of this field.")]
	public static const MatchTarget MatchInstance;

	[Obsolete ("This constant will be removed in the future version. Use Android.Transitions.MatchTarget enum directly instead of this field.")]
	public static const MatchTarget MatchItemId;

	[Obsolete ("This constant will be removed in the future version. Use Android.Transitions.MatchTarget enum directly instead of this field.")]
	public static const MatchTarget MatchName;
```

Added properties:

```
public virtual Android.Graphics.Rect Epicenter { get; }
	public virtual PathMotion PathMotion { get; set; }
	public virtual TransitionPropagation Propagation { get; set; }
	public virtual System.Collections.Generic.IList<string> TargetNames { get; }
	public virtual System.Collections.Generic.IList<Java.Lang.Class> TargetTypes { get; }
```

Added methods:

```
public virtual Transition AddTarget (string targetName);
	public virtual Transition AddTarget (Java.Lang.Class targetType);
	public virtual bool CanRemoveViews ();
	public virtual Transition ExcludeTarget (string targetName, bool exclude);
	public virtual Transition.EpicenterCallback GetEpicenterCallback ();
	public virtual Transition RemoveTarget (string targetName);
	public virtual Transition RemoveTarget (Java.Lang.Class target);
	public virtual void SetEpicenterCallback (Transition.EpicenterCallback epicenterCallback);
	public virtual void SetMatchOrder (int[] matches);
```

### New Type Android.Transitions.EpicenterCallback

```
public abstract class EpicenterCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected Transition (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Transition ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.Graphics.Rect OnGetEpicenter (Transition transition);
}
```

### Type Changed: Android.Transitions.TransitionSet

Added constructor:

```
public TransitionSet (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added property:

```
public virtual int TransitionCount { get; }
```

Added method:

```
public virtual Transition GetTransitionAt (int index);
```

### Type Changed: Android.Transitions.Visibility

Added constructor:

```
public Visibility (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added property:

```
public virtual VisibilityMode Mode { get; set; }
```

Added methods:

```
public virtual Android.Animation.Animator OnAppear (Android.Views.ViewGroup sceneRoot, Android.Views.View view, TransitionValues startValues, TransitionValues endValues);
	public virtual Android.Animation.Animator OnDisappear (Android.Views.ViewGroup sceneRoot, Android.Views.View view, TransitionValues startValues, TransitionValues endValues);
```

### New Type Android.Transitions.ArcMotion

```
public class ArcMotion : Android.Transitions.PathMotion, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ArcMotion (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ArcMotion ();
	public ArcMotion (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	// properties
	public virtual float MaximumAngle { get; set; }
	public virtual float MinimumHorizontalAngle { get; set; }
	public virtual float MinimumVerticalAngle { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Android.Graphics.Path GetPath (float startX, float startY, float endX, float endY);
}
```

### New Type Android.Transitions.ChangeClipBounds

```
public class ChangeClipBounds : Android.Transitions.Transition, Java.Lang.ICloneable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ChangeClipBounds (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ChangeClipBounds ();
	public ChangeClipBounds (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void CaptureEndValues (TransitionValues transitionValues);
	public override void CaptureStartValues (TransitionValues transitionValues);
}
```

### New Type Android.Transitions.ChangeImageTransform

```
public class ChangeImageTransform : Android.Transitions.Transition, Java.Lang.ICloneable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ChangeImageTransform (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ChangeImageTransform ();
	public ChangeImageTransform (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void CaptureEndValues (TransitionValues transitionValues);
	public override void CaptureStartValues (TransitionValues transitionValues);
}
```

### New Type Android.Transitions.ChangeTransform

```
public class ChangeTransform : Android.Transitions.Transition, Java.Lang.ICloneable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ChangeTransform (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ChangeTransform ();
	public ChangeTransform (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	// properties
	public virtual bool Reparent { get; set; }
	public virtual bool ReparentWithOverlay { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void CaptureEndValues (TransitionValues transitionValues);
	public override void CaptureStartValues (TransitionValues transitionValues);
}
```

### New Type Android.Transitions.CircularPropagation

```
public class CircularPropagation : Android.Transitions.VisibilityPropagation, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CircularPropagation (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CircularPropagation ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override long GetStartDelay (Android.Views.ViewGroup sceneRoot, Transition transition, TransitionValues startValues, TransitionValues endValues);
	public virtual void SetPropagationSpeed (float propagationSpeed);
}
```

### New Type Android.Transitions.Explode

```
public class Explode : Android.Transitions.Visibility, Java.Lang.ICloneable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected Explode (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Explode ();
	public Explode (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Android.Transitions.MatchTarget

```
[Serializable]
public enum MatchTarget {
	Id = 3,
	Instance = 1,
	ItemId = 4,
	Name = 2,
}
```

### New Type Android.Transitions.PathMotion

```
public abstract class PathMotion : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected PathMotion (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PathMotion ();
	public PathMotion (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.Graphics.Path GetPath (float startX, float startY, float endX, float endY);
}
```

### New Type Android.Transitions.PatternPathMotion

```
public class PatternPathMotion : Android.Transitions.PathMotion, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected PatternPathMotion (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PatternPathMotion (Android.Graphics.Path patternPath);
	public PatternPathMotion (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	public PatternPathMotion ();
	// properties
	public virtual Android.Graphics.Path PatternPath { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Android.Graphics.Path GetPath (float startX, float startY, float endX, float endY);
}
```

### New Type Android.Transitions.SidePropagation

```
public class SidePropagation : Android.Transitions.VisibilityPropagation, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected SidePropagation (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SidePropagation ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override long GetStartDelay (Android.Views.ViewGroup sceneRoot, Transition transition, TransitionValues startValues, TransitionValues endValues);
	public virtual void SetPropagationSpeed (float propagationSpeed);
	public virtual void SetSide (Android.Views.GravityFlags side);
}
```

### New Type Android.Transitions.Slide

```
public class Slide : Android.Transitions.Visibility, Java.Lang.ICloneable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected Slide (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Slide (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	public Slide (Android.Views.GravityFlags slideEdge);
	public Slide ();
	// properties
	public virtual Android.Views.GravityFlags SlideEdge { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Android.Transitions.TransitionPropagation

```
public abstract class TransitionPropagation : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected TransitionPropagation (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TransitionPropagation ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void CaptureValues (TransitionValues transitionValues);
	public virtual string[] GetPropagationProperties ();
	public virtual long GetStartDelay (Android.Views.ViewGroup sceneRoot, Transition transition, TransitionValues startValues, TransitionValues endValues);
}
```

### New Type Android.Transitions.VisibilityMode

```
[Serializable]
public enum VisibilityMode {
	In = 1,
	Out = 2,
}
```

### New Type Android.Transitions.VisibilityPropagation

```
public abstract class VisibilityPropagation : Android.Transitions.TransitionPropagation, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected VisibilityPropagation (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public VisibilityPropagation ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void CaptureValues (TransitionValues values);
	public override string[] GetPropagationProperties ();
	public virtual Android.Views.ViewStates GetViewVisibility (TransitionValues values);
	public virtual int GetViewX (TransitionValues values);
	public virtual int GetViewY (TransitionValues values);
}
```

## Namespace Android.Util

### Type Changed: Android.Util.ArrayMap

Added method:

```
public int IndexOfKey (Java.Lang.Object key);
```

### Type Changed: Android.Util.DisplayMetrics

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Util.DisplayMetricsDensity enum directly instead of this field.")]
	public static const DisplayMetricsDensity Density560;
```

### Type Changed: Android.Util.DisplayMetricsDensity

Added value:

```
D560 = 560,
```

### Type Changed: Android.Util.LruCache

Added method:

```
public virtual void Resize (int maxSize);
```

### New Type Android.Util.MutableBoolean

```
public sealed class MutableBoolean : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MutableBoolean (bool value);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public bool Value { get; set; }
}
```

### New Type Android.Util.MutableByte

```
public sealed class MutableByte : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MutableByte (sbyte value);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public sbyte Value { get; set; }
}
```

### New Type Android.Util.MutableChar

```
public sealed class MutableChar : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MutableChar (char value);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public char Value { get; set; }
}
```

### New Type Android.Util.MutableDouble

```
public sealed class MutableDouble : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MutableDouble (double value);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public double Value { get; set; }
}
```

### New Type Android.Util.MutableFloat

```
public sealed class MutableFloat : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MutableFloat (float value);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public float Value { get; set; }
}
```

### New Type Android.Util.MutableInt

```
public sealed class MutableInt : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MutableInt (int value);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int Value { get; set; }
}
```

### New Type Android.Util.MutableLong

```
public sealed class MutableLong : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MutableLong (long value);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public long Value { get; set; }
}
```

### New Type Android.Util.MutableShort

```
public sealed class MutableShort : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MutableShort (short value);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public short Value { get; set; }
}
```

### New Type Android.Util.Range

```
public sealed class Range : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public Range (Java.Lang.Object lower, Java.Lang.Object upper);
	// properties
	public Java.Lang.Object Lower { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public Java.Lang.Object Upper { get; }
	// methods
	public Java.Lang.Object Clamp (Java.Lang.Object value);
	public bool Contains (Java.Lang.Object value);
	public bool Contains (Range range);
	public static Range Create (Java.Lang.Object lower, Java.Lang.Object upper);
	public Range Extend (Range range);
	public Range Extend (Java.Lang.Object lower, Java.Lang.Object upper);
	public Range Extend (Java.Lang.Object value);
	public Range Intersect (Java.Lang.Object lower, Java.Lang.Object upper);
	public Range Intersect (Range range);
}
```

### New Type Android.Util.Rational

```
public sealed class Rational : Java.Lang.Number, Java.Lang.IComparable, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable {
	// constructors
	public Rational (int numerator, int denominator);
	// properties
	public int Denominator { get; }
	public bool IsFinite { get; }
	public bool IsInfinite { get; }
	public bool IsNaN { get; }
	public bool IsZero { get; }
	public static Rational NaN { get; set; }
	public static Rational NegativeInfinity { get; set; }
	public int Numerator { get; }
	public static Rational PositiveInfinity { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public static Rational Zero { get; set; }
	// methods
	public int CompareTo (Rational another);
	public override double DoubleValue ();
	public override float FloatValue ();
	public override int IntValue ();
	public override long LongValue ();
	public static Rational ParseRational (string string);
}
```

### New Type Android.Util.Size

```
public sealed class Size : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public Size (int width, int height);
	// properties
	public int Height { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int Width { get; }
	// methods
	public static Size ParseSize (string string);
}
```

### New Type Android.Util.SizeF

```
public sealed class SizeF : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public SizeF (float width, float height);
	// properties
	public float Height { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public float Width { get; }
	// methods
	public static SizeF ParseSizeF (string string);
}
```

## Namespace Android.Views

### Type Changed: Android.Views.Display

Added properties:

```
public virtual long AppVsyncOffsetNanos { get; }
	public virtual long PresentationDeadlineNanos { get; }
```

Added method:

```
public virtual float[] GetSupportedRefreshRates ();
```

### Type Changed: Android.Views.DisplayState

Added values:

```
Doze = 3,
	DozeSuspend = 4,
```

### Type Changed: Android.Views.HapticFeedbackConstants

Added field:

```
public static const int ClockTick;
```

Added properties:

```
protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
```

### Type Changed: Android.Views.InputDevice

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.InputSourceType enum directly instead of this field.")]
	public static const InputSourceType SourceHdmi;
```

Added method:

```
public bool SupportsSource (InputSourceType source);
```

### Type Changed: Android.Views.InputSourceType

Added value:

```
Hdmi = 33554433,
```

### Type Changed: Android.Views.IViewParent

Added methods:

```
public virtual bool OnNestedFling (View target, float velocityX, float velocityY, bool consumed);
	public virtual bool OnNestedPreFling (View target, float velocityX, float velocityY);
	public virtual void OnNestedPreScroll (View target, int dx, int dy, int[] consumed);
	public virtual void OnNestedScroll (View target, int dxConsumed, int dyConsumed, int dxUnconsumed, int dyUnconsumed);
	public virtual void OnNestedScrollAccepted (View child, View target, ScrollAxis nestedScrollAxes);
	public virtual bool OnStartNestedScroll (View child, View target, ScrollAxis nestedScrollAxes);
	public virtual void OnStopNestedScroll (View target);
```

### Type Changed: Android.Views.Keycode

Added values:

```
Help = 259,
	K11 = 227,
	K12 = 228,
	LastChannel = 229,
	MediaTopMenu = 226,
	Pairing = 225,
	TvAntennaCable = 242,
	TvAudioDescription = 252,
	TvAudioDescriptionMixDown = 254,
	TvAudioDescriptionMixUp = 253,
	TvContentsMenu = 256,
	TvDataService = 230,
	TvInputComponent1 = 249,
	TvInputComponent2 = 250,
	TvInputComposite1 = 247,
	TvInputComposite2 = 248,
	TvInputHdmi1 = 243,
	TvInputHdmi2 = 244,
	TvInputHdmi3 = 245,
	TvInputHdmi4 = 246,
	TvInputVga1 = 251,
	TvMediaContextMenu = 257,
	TvNetwork = 241,
	TvNumberEntry = 234,
	TvRadioService = 232,
	TvSatellite = 237,
	TvSatelliteBs = 238,
	TvSatelliteCs = 239,
	TvSatelliteService = 240,
	TvTeletext = 233,
	TvTerrestrialAnalog = 235,
	TvTerrestrialDigital = 236,
	TvTimerProgramming = 258,
	TvZoomMode = 255,
	VoiceAssist = 231,
```

### Type Changed: Android.Views.MotionEvent

Added method:

```
public bool IsButtonPressed (MotionEventButtonState button);
```

### Type Changed: Android.Views.SurfaceView

Added constructor:

```
public SurfaceView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Views.TextureView

Added constructor:

```
public TextureView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Views.View

Added constructor:

```
public View (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.ScrollAxis enum directly instead of this field.")]
	public static const ScrollAxis ScrollAxisHorizontal;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ScrollAxis enum directly instead of this field.")]
	public static const ScrollAxis ScrollAxisNone;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.ScrollAxis enum directly instead of this field.")]
	public static const ScrollAxis ScrollAxisVertical;
```

Added properties:

```
public virtual Android.Content.Res.ColorStateList BackgroundTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode BackgroundTintMode { get; set; }
	public bool ClipToOutline { get; set; }
	public virtual float Elevation { get; set; }
	public virtual bool HasNestedScrollingParent { get; }
	public virtual bool IsAccessibilityFocused { get; }
	public virtual bool IsImportantForAccessibility { get; }
	public virtual bool NestedScrollingEnabled { get; set; }
	public virtual ViewOutlineProvider OutlineProvider { get; set; }
	public virtual Android.Animation.StateListAnimator StateListAnimator { get; set; }
	public string TransitionName { get; set; }
	public virtual float TranslationZ { get; set; }
	public static Android.Util.Property Z { get; set; }
```

Added methods:

```
public virtual WindowInsets ComputeSystemWindowInsets (WindowInsets in, Android.Graphics.Rect outLocalInsets);
	public virtual bool DispatchNestedFling (float velocityX, float velocityY, bool consumed);
	public virtual bool DispatchNestedPreFling (float velocityX, float velocityY);
	public virtual bool DispatchNestedPreScroll (int dx, int dy, int[] consumed, int[] offsetInWindow);
	public virtual bool DispatchNestedScroll (int dxConsumed, int dyConsumed, int dxUnconsumed, int dyUnconsumed, int[] offsetInWindow);
	public virtual void DrawableHotspotChanged (float x, float y);
	public virtual float GetZ ();
	public virtual void InvalidateOutline ();
	public void RequestUnbufferedDispatch (MotionEvent e);
	public virtual void SetZ (float z);
	public virtual bool StartNestedScroll (ScrollAxis axes);
	public virtual void StopNestedScroll ();
```

### Type Changed: Android.Views.ViewGroup

Added constructor:

```
public ViewGroup (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual bool ClipToPadding { get; }
	public virtual ScrollAxis NestedScrollAxes { get; }
	public virtual bool TouchscreenBlocksFocus { get; set; }
	public virtual bool TransitionGroup { get; set; }
```

Added methods:

```
public virtual bool OnNestedFling (View target, float velocityX, float velocityY, bool consumed);
	public virtual bool OnNestedPreFling (View target, float velocityX, float velocityY);
	public virtual void OnNestedPreScroll (View target, int dx, int dy, int[] consumed);
	public virtual void OnNestedScroll (View target, int dxConsumed, int dyConsumed, int dxUnconsumed, int dyUnconsumed);
	public virtual void OnNestedScrollAccepted (View child, View target, ScrollAxis axes);
	public virtual bool OnStartNestedScroll (View child, View target, ScrollAxis nestedScrollAxes);
	public virtual void OnStopNestedScroll (View child);
```

### Type Changed: Android.Views.ViewPropertyAnimator

Added methods:

```
public virtual ViewPropertyAnimator TranslationZ (float value);
	public virtual ViewPropertyAnimator TranslationZBy (float value);
	public virtual ViewPropertyAnimator Z (float value);
	public virtual ViewPropertyAnimator ZBy (float value);
```

### Type Changed: Android.Views.ViewStub

Added constructor:

```
public ViewStub (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Views.Window

Added fields:

```
public static const string NavigationBarBackgroundTransitionName = "android:navigation:background";
	public static const string StatusBarBackgroundTransitionName = "android:status:background";
```

Added properties:

```
public virtual bool AllowEnterTransitionOverlap { get; set; }
	public virtual bool AllowReturnTransitionOverlap { get; set; }
	public virtual Android.Transitions.Scene ContentScene { get; }
	public virtual Android.Transitions.Transition EnterTransition { get; set; }
	public virtual Android.Transitions.Transition ExitTransition { get; set; }
	public virtual Android.Media.Session.MediaController MediaController { get; set; }
	public virtual int NavigationBarColor { get; }
	public virtual Android.Transitions.Transition ReenterTransition { get; set; }
	public virtual Android.Transitions.Transition ReturnTransition { get; set; }
	public virtual Android.Transitions.Transition SharedElementEnterTransition { get; set; }
	public virtual Android.Transitions.Transition SharedElementExitTransition { get; set; }
	public virtual Android.Transitions.Transition SharedElementReenterTransition { get; set; }
	public virtual Android.Transitions.Transition SharedElementReturnTransition { get; set; }
	public virtual bool SharedElementsUseOverlay { get; set; }
	public virtual int StatusBarColor { get; }
	public virtual long TransitionBackgroundFadeDuration { get; set; }
	public virtual Android.Transitions.TransitionManager TransitionManager { get; set; }
```

Added methods:

```
public virtual void SetNavigationBarColor (Android.Graphics.Color color);
	public virtual void SetStatusBarColor (Android.Graphics.Color color);
```

### Type Changed: Android.Views.WindowFeatures

Added values:

```
ActivityTransitions = 13,
	ContentTransitions = 12,
```

### Type Changed: Android.Views.WindowInsets

Added properties:

```
public bool HasStableInsets { get; }
	public bool IsConsumed { get; }
	public int StableInsetBottom { get; }
	public int StableInsetLeft { get; }
	public int StableInsetRight { get; }
	public int StableInsetTop { get; }
```

Added methods:

```
public WindowInsets ConsumeStableInsets ();
	public WindowInsets ReplaceSystemWindowInsets (Android.Graphics.Rect systemWindowInsets);
```

### Type Changed: Android.Views.WindowManagerFlags

Added value:

```
DrawsSystemBarBackgrounds = -2147483648,
```

### Type Changed: Android.Views.WindowManagerLayoutParams

Added property:

```
public float PreferredRefreshRate { get; set; }
```

### New Type Android.Views.FrameStats

```
public abstract class FrameStats : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected FrameStats (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FrameStats ();
	// fields
	public static const long UndefinedTimeNano;
	// properties
	public long EndTimeNano { get; }
	public int FrameCount { get; }
	public long RefreshPeriodNano { get; }
	public long StartTimeNano { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public long GetFramePresentedTimeNano (int index);
}
```

### New Type Android.Views.ScrollAxis

```
[Serializable]
[Flags]
public enum ScrollAxis {
	Horizontal = 1,
	None = 0,
	Vertical = 2,
}
```

### New Type Android.Views.ViewAnimationUtils

```
public sealed class ViewAnimationUtils : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static Android.Animation.Animator CreateCircularReveal (View view, int centerX, int centerY, float startRadius, float endRadius);
}
```

### New Type Android.Views.ViewOutlineProvider

```
public abstract class ViewOutlineProvider : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ViewOutlineProvider (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ViewOutlineProvider ();
	// properties
	public static ViewOutlineProvider Background { get; set; }
	public static ViewOutlineProvider Bounds { get; set; }
	public static ViewOutlineProvider PaddedBounds { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void GetOutline (View view, Android.Graphics.Outline outline);
}
```

### New Type Android.Views.WindowAnimationFrameStats

```
public sealed class WindowAnimationFrameStats : Android.Views.FrameStats, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Views.WindowContentFrameStats

```
public sealed class WindowContentFrameStats : Android.Views.FrameStats, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public long GetFramePostedTimeNano (int index);
	public long GetFrameReadyTimeNano (int index);
	public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo

Added fields:

```
public static const string ActionArgumentSetTextCharsequence = "ACTION_ARGUMENT_SET_TEXT_CHARSEQUENCE";

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.Action enum directly instead of this field.")]
	public static const Action ActionSetText;
```

Added properties:

```
public virtual System.Collections.Generic.IList<AccessibilityNodeInfo.AccessibilityAction> ActionList { get; }
	public string Error { get; set; }
	public virtual Java.Lang.ICharSequence ErrorFormatted { get; set; }
	public virtual int MaxTextLength { get; set; }
	public virtual AccessibilityWindowInfo Window { get; }
```

Added methods:

```
public virtual bool RemoveAction (AccessibilityNodeInfo.AccessibilityAction action);
	public virtual void RemoveAction (int action);
	public virtual bool RemoveChild (Android.Views.View root, int virtualDescendantId);
	public virtual bool RemoveChild (Android.Views.View child);
```

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo.CollectionInfo

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.SelectionMode enum directly instead of this field.")]
	public static const SelectionMode SelectionModeMultiple;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.SelectionMode enum directly instead of this field.")]
	public static const SelectionMode SelectionModeNone;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.SelectionMode enum directly instead of this field.")]
	public static const SelectionMode SelectionModeSingle;
```

Added property:

```
public int SelectionMode { get; }
```

Added method:

```
public static AccessibilityNodeInfo.CollectionInfo Obtain (int rowCount, int columnCount, bool hierarchical, SelectionMode selectionMode);
```

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo.CollectionItemInfo

Added property:

```
public bool IsSelected { get; }
```

Added method:

```
public static AccessibilityNodeInfo.CollectionItemInfo Obtain (int rowIndex, int rowSpan, int columnIndex, int columnSpan, bool heading, bool selected);
```

### New Type Android.Views.Accessibility.AccessibilityAction

```
public sealed class AccessibilityAction : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public AccessibilityNodeInfo (int actionId, Java.Lang.ICharSequence label);
	public AccessibilityNodeInfo (int actionId, string label);
	// properties
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
	public int Id { get; }
	public string Label { get; }
	public Java.Lang.ICharSequence LabelFormatted { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### Type Changed: Android.Views.Accessibility.AccessibilityNodeProvider

Added field:

```
public static const int HostViewId;
```

### Type Changed: Android.Views.Accessibility.Action

Added value:

```
SetText = 2097152,
```

### Type Changed: Android.Views.Accessibility.CaptioningManager

### Type Changed: Android.Views.Accessibility.CaptioningManager.CaptionStyle

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.CaptionStyles enum directly instead of this field.")]
	public static const CaptionStyles EdgeTypeDepressed;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.CaptionStyles enum directly instead of this field.")]
	public static const CaptionStyles EdgeTypeRaised;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.CaptionStyles enum directly instead of this field.")]
	public static const CaptionStyles EdgeTypeUnspecified;
```

Added properties:

```
public bool HasBackgroundColor { get; }
	public bool HasEdgeColor { get; }
	public bool HasEdgeType { get; }
	public bool HasForegroundColor { get; }
	public bool HasWindowColor { get; }
	public int WindowColor { get; set; }
```

### Type Changed: Android.Views.Accessibility.CaptionStyles

Added values:

```
Depressed = 4,
	Raised = 3,
	Unspecified = -1,
```

### Type Changed: Android.Views.Accessibility.EventTypes

Added value:

```
WindowsChanged = 4194304,
```

### New Type Android.Views.Accessibility.AccessibilityWindowInfo

```
public sealed class AccessibilityWindowInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.AccessibilityWindowType enum directly instead of this field.")]
	public static const AccessibilityWindowType TypeApplication;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.AccessibilityWindowType enum directly instead of this field.")]
	public static const AccessibilityWindowType TypeInputMethod;

	[Obsolete ("This constant will be removed in the future version. Use Android.Views.Accessibility.AccessibilityWindowType enum directly instead of this field.")]
	public static const AccessibilityWindowType TypeSystem;
	// properties
	public int ChildCount { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public int Id { get; }
	public bool IsAccessibilityFocused { get; }
	public bool IsActive { get; }
	public bool IsFocused { get; }
	public int Layer { get; }
	public AccessibilityWindowInfo Parent { get; }
	public AccessibilityNodeInfo Root { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public AccessibilityWindowType Type { get; }
	// methods
	public virtual int DescribeContents ();
	public void GetBoundsInScreen (Android.Graphics.Rect outBounds);
	public AccessibilityWindowInfo GetChild (int index);
	public static AccessibilityWindowInfo Obtain ();
	public static AccessibilityWindowInfo Obtain (AccessibilityWindowInfo info);
	public void Recycle ();
	public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Views.Accessibility.AccessibilityWindowType

```
[Serializable]
public enum AccessibilityWindowType {
	Application = 1,
	InputMethod = 2,
	System = 3,
}
```

### New Type Android.Views.Accessibility.SelectionMode

```
[Serializable]
public enum SelectionMode {
	Multiple = 2,
	None = 0,
	Single = 1,
}
```

## Namespace Android.Views.Animations

### New Type Android.Views.Animations.PathInterpolator

```
public class PathInterpolator : Java.Lang.Object, IInterpolator, Android.Animation.ITimeInterpolator, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected PathInterpolator (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PathInterpolator (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	public PathInterpolator (float controlX1, float controlY1, float controlX2, float controlY2);
	public PathInterpolator (float controlX, float controlY);
	public PathInterpolator (Android.Graphics.Path path);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual float GetInterpolation (float t);
}
```

## Namespace Android.Views.InputMethods

### Type Changed: Android.Views.InputMethods.BaseInputConnection

Added method:

```
public virtual bool RequestCursorUpdates (int cursorUpdateMode);
```

### Type Changed: Android.Views.InputMethods.CursorAnchorFlags

Added values:

```
HasInvisibleRegion = 2,
	HasVisibleRegion = 1,
	IsRtl = 4,
```

### Type Changed: Android.Views.InputMethods.IInputConnection

Added method:

```
public virtual bool RequestCursorUpdates (int cursorUpdateMode);
```

### Type Changed: Android.Views.InputMethods.IInputMethodSession

Added method:

```
public virtual void UpdateCursorAnchorInfo (CursorAnchorInfo cursorAnchorInfo);
```

### Type Changed: Android.Views.InputMethods.InputConnectionWrapper

Added method:

```
public virtual bool RequestCursorUpdates (int cursorUpdateMode);
```

### Type Changed: Android.Views.InputMethods.InputMethodManager

Added method:

```
public void UpdateCursorAnchorInfo (Android.Views.View view, CursorAnchorInfo cursorAnchorInfo);
```

### New Type Android.Views.InputMethods.CursorAnchorInfo

```
public sealed class CursorAnchorInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public CursorAnchorInfo (Android.OS.Parcel source);
	// properties
	public string ComposingText { get; }
	public Java.Lang.ICharSequence ComposingTextFormatted { get; }
	public int ComposingTextStart { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public float InsertionMarkerBaseline { get; }
	public float InsertionMarkerBottom { get; }
	public CursorAnchorFlags InsertionMarkerFlags { get; }
	public float InsertionMarkerHorizontal { get; }
	public float InsertionMarkerTop { get; }
	public Android.Graphics.Matrix Matrix { get; }
	public int SelectionEnd { get; }
	public int SelectionStart { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public Android.Graphics.RectF GetCharacterBounds (int index);
	public CursorAnchorFlags GetCharacterBoundsFlags (int index);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public CursorAnchorInfo ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public CursorAnchorInfo.Builder AddCharacterBounds (int index, float left, float top, float right, float bottom, CursorAnchorFlags flags);
		public CursorAnchorInfo Build ();
		public void Reset ();
		public CursorAnchorInfo.Builder SetComposingText (int composingTextStart, string composingText);
		public CursorAnchorInfo.Builder SetComposingText (int composingTextStart, Java.Lang.ICharSequence composingText);
		public CursorAnchorInfo.Builder SetInsertionMarkerLocation (float horizontalPosition, float lineTop, float lineBaseline, float lineBottom, CursorAnchorFlags flags);
		public CursorAnchorInfo.Builder SetMatrix (Android.Graphics.Matrix matrix);
		public CursorAnchorInfo.Builder SetSelectionRange (int newStart, int newEnd);
	}
}
```

### New Type Android.Views.InputMethods.CursorUpdate

```
[Serializable]
public enum CursorUpdate {
	Immediate = 1,
	Monitor = 2,
}
```

## Namespace Android.Views.TextService

### Type Changed: Android.Views.TextService.TextInfo

Removed constructor:

```
public TextInfo (string text, int cookie, int sequence);
```

Added constructors:

```
public TextInfo (Java.Lang.ICharSequence charSequence, int start, int end, int cookie, int sequenceNumber);
	public TextInfo (string charSequence, int start, int end, int cookie, int sequenceNumber);
	public TextInfo (string text, int cookie, int sequenceNumber);
```

Added properties:

```
public string CharacterSequence { get; }
	public Java.Lang.ICharSequence CharacterSequenceFormatted { get; }
```

## Namespace Android.Webkit

### Type Changed: Android.Webkit.CookieManager

Added methods:

```
public virtual bool AcceptThirdPartyCookies (WebView webview);
	public virtual void Flush ();
	public virtual void RemoveAllCookies (IValueCallback callback);
	public virtual void RemoveSessionCookies (IValueCallback callback);
	public virtual void SetAcceptThirdPartyCookies (WebView webview, bool accept);
	public virtual void SetCookie (string url, string value, IValueCallback callback);
```

### Type Changed: Android.Webkit.CookieSyncManager

Added field:

```
protected static const string Logtag = "websync";
```

Added properties:

```
protected WebViewDatabase MDataBase { get; set; }
	protected Android.OS.Handler MHandler { get; set; }
```

### Type Changed: Android.Webkit.WebChromeClient

Added methods:

```
public virtual void OnPermissionRequest (PermissionRequest request);
	public virtual void OnPermissionRequestCanceled (PermissionRequest request);
	public virtual bool OnShowFileChooser (WebView webView, IValueCallback filePathCallback, WebChromeClient.FileChooserParams fileChooserParams);
```

### New Type Android.Webkit.FileChooserParams

```
public abstract class FileChooserParams : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WebChromeClient (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WebChromeClient ();
	// properties
	public virtual string FilenameHint { get; }
	public virtual bool IsCaptureEnabled { get; }
	public virtual ChromeFileChooserMode Mode { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public string Title { get; }
	public virtual Java.Lang.ICharSequence TitleFormatted { get; }
	// methods
	public virtual Android.Content.Intent CreateIntent ();
	public virtual string[] GetAcceptTypes ();
	public static Android.Net.Uri[] ParseResult (int resultCode, Android.Content.Intent data);
}
```

### Type Changed: Android.Webkit.WebResourceResponse

Added constructor:

```
public WebResourceResponse (string mimeType, string encoding, int statusCode, string reasonPhrase, System.Collections.Generic.IDictionary<System.String,System.String> responseHeaders, System.IO.Stream data);
```

Added properties:

```
public virtual string ReasonPhrase { get; }
	public virtual System.Collections.Generic.IDictionary<System.String,System.String> ResponseHeaders { get; set; }
	public virtual int StatusCode { get; }
```

Added method:

```
public virtual void SetStatusCodeAndReasonPhrase (int statusCode, string reasonPhrase);
```

### Type Changed: Android.Webkit.WebSettings

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Webkit.MixedContentHandling enum directly instead of this field.")]
	public static const MixedContentHandling MixedContentAlwaysAllow;

	[Obsolete ("This constant will be removed in the future version. Use Android.Webkit.MixedContentHandling enum directly instead of this field.")]
	public static const MixedContentHandling MixedContentCompatibilityMode;

	[Obsolete ("This constant will be removed in the future version. Use Android.Webkit.MixedContentHandling enum directly instead of this field.")]
	public static const MixedContentHandling MixedContentNeverAllow;
```

Added property:

```
public virtual MixedContentHandling MixedContentMode { get; set; }
```

### Type Changed: Android.Webkit.WebView

Added constructor:

```
public WebView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added methods:

```
public static void ClearClientCertPreferences (Java.Lang.IRunnable onCleared);
	public virtual Android.Print.PrintDocumentAdapter CreatePrintDocumentAdapter (string documentName);
	public static void EnableSlowWholeDocumentDraw ();
	public virtual void ZoomBy (float zoomFactor);
```

### Type Changed: Android.Webkit.WebViewClient

Added methods:

```
public virtual void OnReceivedClientCertRequest (WebView view, ClientCertRequest request);
	public virtual void OnUnhandledInputEvent (WebView view, Android.Views.InputEvent e);
	public virtual WebResourceResponse ShouldInterceptRequest (WebView view, IWebResourceRequest request);
```

### New Type Android.Webkit.ChromeFileChooserMode

```
[Serializable]
public enum ChromeFileChooserMode {
	Open = 0,
	OpenMultiple = 1,
	Save = 3,
}
```

### New Type Android.Webkit.ClientCertRequest

```
public abstract class ClientCertRequest : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ClientCertRequest (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ClientCertRequest ();
	// properties
	public virtual string Host { get; }
	public virtual int Port { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Cancel ();
	public virtual string[] GetKeyTypes ();
	public virtual Java.Security.IPrincipal[] GetPrincipals ();
	public virtual void Ignore ();
	public virtual void Proceed (Java.Security.IPrivateKey privateKey, Java.Security.Cert.X509Certificate[] chain);
}
```

### New Type Android.Webkit.IWebResourceRequest

```
public interface IWebResourceRequest : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual bool HasGesture { get; }
	public virtual bool IsForMainFrame { get; }
	public virtual string Method { get; }
	public virtual System.Collections.Generic.IDictionary<System.String,System.String> RequestHeaders { get; }
	public virtual Android.Net.Uri Url { get; }
}
```

### New Type Android.Webkit.MixedContentHandling

```
[Serializable]
public enum MixedContentHandling {
	AlwaysAllow = 0,
	CompatibilityMode = 2,
	NeverAllow = 1,
}
```

### New Type Android.Webkit.PermissionRequest

```
public abstract class PermissionRequest : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected PermissionRequest (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PermissionRequest ();
	// fields
	public static const string ResourceAudioCapture = "android.webkit.resource.AUDIO_CAPTURE";
	public static const string ResourceProtectedMediaId = "android.webkit.resource.PROTECTED_MEDIA_ID";
	public static const string ResourceVideoCapture = "android.webkit.resource.VIDEO_CAPTURE";
	// properties
	public virtual Android.Net.Uri Origin { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Deny ();
	public virtual string[] GetResources ();
	public virtual void Grant (string[] resources);
}
```

## Namespace Android.Widget

### Type Changed: Android.Widget.AbsListView

Added constructor:

```
public AbsListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added methods:

```
public virtual void Fling (int velocityY);
	public virtual void SetFastScrollStyle (int styleResId);
	public virtual void SetSelectionFromTop (int position, int y);
```

### Type Changed: Android.Widget.AbsoluteLayout

Added constructor:

```
public AbsoluteLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.AbsSeekBar

Added constructor:

```
public AbsSeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual bool SplitTrack { get; set; }
	public virtual Android.Content.Res.ColorStateList ThumbTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ThumbTintMode { get; set; }
```

### Type Changed: Android.Widget.AbsSpinner

Added constructor:

```
public AbsSpinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.AdapterView

Added constructor:

```
public AdapterView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.AdapterViewAnimator

Added constructor:

```
public AdapterViewAnimator (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.AdapterViewFlipper

Added constructors:

```
public AdapterViewFlipper (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public AdapterViewFlipper (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.AnalogClock

Added constructor:

```
public AnalogClock (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.AutoCompleteTextView

Added constructor:

```
public AutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.Button

Added constructor:

```
public Button (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.CalendarView

Added constructor:

```
public CalendarView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.CheckBox

Added constructor:

```
public CheckBox (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.CheckedTextView

Added constructor:

```
public CheckedTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual Android.Content.Res.ColorStateList CheckMarkTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode CheckMarkTintMode { get; set; }
```

### Type Changed: Android.Widget.Chronometer

Added constructor:

```
public Chronometer (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.CompoundButton

Added constructor:

```
public CompoundButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual Android.Content.Res.ColorStateList ButtonTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ButtonTintMode { get; set; }
```

### Type Changed: Android.Widget.DatePicker

Added constructor:

```
public DatePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added property:

```
public virtual int FirstDayOfWeek { get; set; }
```

### Type Changed: Android.Widget.EdgeEffect

Added properties:

```
public virtual int Color { get; }
	public virtual int MaxHeight { get; }
```

Added methods:

```
public virtual void OnPull (float deltaDistance, float displacement);
	public virtual void SetColor (Android.Graphics.Color color);
```

### Type Changed: Android.Widget.EditText

Added constructor:

```
public EditText (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.ExpandableListView

Added constructor:

```
public ExpandableListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.FrameLayout

Added constructor:

```
public FrameLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual Android.Content.Res.ColorStateList ForegroundTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ForegroundTintMode { get; set; }
```

### Type Changed: Android.Widget.Gallery

Added constructor:

```
public Gallery (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.GridLayout

Added constructor:

```
public GridLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added methods:

```
public static GridLayout.Spec InvokeSpec (int start, float weight);
	public static GridLayout.Spec InvokeSpec (int start, int size, GridLayout.Alignment alignment, float weight);
	public static GridLayout.Spec InvokeSpec (int start, int size, float weight);
	public static GridLayout.Spec InvokeSpec (int start, GridLayout.Alignment alignment, float weight);
```

### Type Changed: Android.Widget.GridView

Added constructor:

```
public GridView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.HorizontalScrollView

Added constructor:

```
public HorizontalScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.ImageButton

Added constructor:

```
public ImageButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.ImageView

Added constructor:

```
public ImageView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual Android.Content.Res.ColorStateList ImageTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ImageTintMode { get; set; }
```

### Type Changed: Android.Widget.LinearLayout

Added constructor:

```
public LinearLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.ListView

Added constructor:

```
public ListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Removed method:

```
public virtual void SetSelectionFromTop (int p0, int p1);
```

Added method:

```
public override void SetSelectionFromTop (int p0, int p1);
```

### Type Changed: Android.Widget.MultiAutoCompleteTextView

Added constructor:

```
public MultiAutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.NumberPicker

Added constructor:

```
public NumberPicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.PopupWindow

Added property:

```
public virtual float Elevation { get; set; }
```

### Type Changed: Android.Widget.ProgressBar

Added constructor:

```
public ProgressBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual Android.Content.Res.ColorStateList IndeterminateTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode IndeterminateTintMode { get; set; }
	public virtual Android.Content.Res.ColorStateList ProgressBackgroundTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ProgressBackgroundTintMode { get; set; }
	public virtual Android.Content.Res.ColorStateList ProgressTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode ProgressTintMode { get; set; }
	public virtual Android.Content.Res.ColorStateList SecondaryProgressTintList { get; set; }
	public virtual Android.Graphics.PorterDuff.Mode SecondaryProgressTintMode { get; set; }
```

Added methods:

```
public virtual void SetIndeterminateDrawableTiled (Android.Graphics.Drawables.Drawable d);
	public virtual void SetProgressDrawableTiled (Android.Graphics.Drawables.Drawable d);
```

### Type Changed: Android.Widget.QuickContactBadge

Added constructor:

```
public QuickContactBadge (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added method:

```
public virtual void SetOverlay (Android.Graphics.Drawables.Drawable overlay);
```

### Type Changed: Android.Widget.RadioButton

Added constructor:

```
public RadioButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.RatingBar

Added constructor:

```
public RatingBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.RelativeLayout

Added constructor:

```
public RelativeLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.ScrollView

Added constructor:

```
public ScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.SearchView

Added constructors:

```
public SearchView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public SearchView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.SeekBar

Added constructor:

```
public SeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.SlidingDrawer

Added constructor:

```
public SlidingDrawer (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.Space

Added constructor:

```
public Space (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.Spinner

Added constructor:

```
public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes, SpinnerMode mode);
```

### Type Changed: Android.Widget.StackView

Added constructor:

```
public StackView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.Switch

Added constructor:

```
public Switch (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual bool ShowText { get; set; }
	public virtual bool SplitTrack { get; set; }
```

### Type Changed: Android.Widget.TabHost

Added constructors:

```
public TabHost (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public TabHost (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.TabWidget

Added constructor:

```
public TabWidget (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.TextClock

Added constructor:

```
public TextClock (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.TextView

Added constructor:

```
public TextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added properties:

```
public virtual string FontFeatureSettings { get; set; }
	public virtual float LetterSpacing { get; set; }
	public bool ShowSoftInputOnFocus { get; set; }
```

Added method:

```
public virtual void SetElegantTextHeight (bool elegant);
```

### Type Changed: Android.Widget.TimePicker

Added constructor:

```
public TimePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.ToggleButton

Added constructor:

```
public ToggleButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.TwoLineListItem

Added constructor:

```
public TwoLineListItem (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### Type Changed: Android.Widget.VideoView

Added constructor:

```
public VideoView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

Added method:

```
public virtual void SetVideoURI (Android.Net.Uri uri, System.Collections.Generic.IDictionary<System.String,System.String> headers);
```

### Type Changed: Android.Widget.ZoomButton

Added constructor:

```
public ZoomButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
```

### New Type Android.Widget.ActionMenuView

```
public class ActionMenuView : Android.Widget.LinearLayout, Android.Views.IViewManager, Android.Views.IViewParent, Android.Runtime.IJavaObject, System.IDisposable, Android.Views.Accessibility.IAccessibilityEventSource {
	// constructors
	protected ActionMenuView (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ActionMenuView (Android.Content.Context context);
	public ActionMenuView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	// properties
	public virtual bool IsOverflowMenuShowing { get; }
	public virtual Android.Views.IMenu Menu { get; }
	public virtual int PopupTheme { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// events
	public event System.EventHandler<ActionMenuView.MenuItemClickEventArgs> MenuItemClick;
	// methods
	public virtual void DismissPopupMenus ();
	public virtual bool HideOverflowMenu ();
	public virtual void OnConfigurationChanged (Android.Content.Res.Configuration newConfig);
	public virtual void OnDetachedFromWindow ();
	public virtual void SetOnMenuItemClickListener (ActionMenuView.IOnMenuItemClickListener listener);
	public virtual bool ShowOverflowMenu ();

	// inner types
	public class LayoutParams : Android.Widget.LinearLayout+LayoutParams, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected ActionMenuView (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public ActionMenuView (int width, int height);
		public ActionMenuView (ActionMenuView.LayoutParams other);
		public ActionMenuView (Android.Views.ViewGroup.LayoutParams other);
		public ActionMenuView (Android.Content.Context c, Android.Util.IAttributeSet attrs);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
	public interface IOnMenuItemClickListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual bool OnMenuItemClick (Android.Views.IMenuItem item);
	}
	public class MenuItemClickEventArgs : System.EventArgs {
		// constructors
		public ActionMenuView (bool handled, Android.Views.IMenuItem item);
		// properties
		public bool Handled { get; set; }
		public Android.Views.IMenuItem Item { get; }
	}
}
```

### New Type Android.Widget.Toolbar

```
public class Toolbar : Android.Views.ViewGroup, Android.Views.IViewManager, Android.Views.IViewParent, Android.Runtime.IJavaObject, System.IDisposable, Android.Views.Accessibility.IAccessibilityEventSource {
	// constructors
	protected Toolbar (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Toolbar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, int defStyleRes);
	public Toolbar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public Toolbar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	public Toolbar (Android.Content.Context context);
	// properties
	public virtual int ContentInsetEnd { get; }
	public virtual int ContentInsetLeft { get; }
	public virtual int ContentInsetRight { get; }
	public virtual int ContentInsetStart { get; }
	public virtual bool HasExpandedActionView { get; }
	public virtual bool IsOverflowMenuShowing { get; }
	public virtual Android.Graphics.Drawables.Drawable Logo { get; set; }
	public string LogoDescription { get; set; }
	public virtual Java.Lang.ICharSequence LogoDescriptionFormatted { get; set; }
	public virtual Android.Views.IMenu Menu { get; }
	public string NavigationContentDescription { get; set; }
	public virtual Java.Lang.ICharSequence NavigationContentDescriptionFormatted { get; set; }
	public virtual Android.Graphics.Drawables.Drawable NavigationIcon { get; set; }
	public virtual int PopupTheme { get; set; }
	public string Subtitle { get; set; }
	public virtual Java.Lang.ICharSequence SubtitleFormatted { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public string Title { get; set; }
	public virtual Java.Lang.ICharSequence TitleFormatted { get; set; }
	// events
	public event System.EventHandler<Toolbar.MenuItemClickEventArgs> MenuItemClick;
	public event System.EventHandler NavigationOnClick;
	// methods
	public virtual void CollapseActionView ();
	public virtual void DismissPopupMenus ();
	public virtual bool HideOverflowMenu ();
	public virtual void InflateMenu (int resId);
	protected override void OnLayout (bool changed, int l, int t, int r, int b);
	public virtual void SetContentInsetsAbsolute (int contentInsetLeft, int contentInsetRight);
	public virtual void SetContentInsetsRelative (int contentInsetStart, int contentInsetEnd);
	public virtual void SetLogo (int resId);
	public virtual void SetLogoDescription (int resId);
	public virtual void SetNavigationContentDescription (int resId);
	public virtual void SetNavigationIcon (int resId);
	public virtual void SetNavigationOnClickListener (Android.Views.View.IOnClickListener listener);
	public virtual void SetOnMenuItemClickListener (Toolbar.IOnMenuItemClickListener listener);
	public virtual void SetSubtitle (int resId);
	public virtual void SetSubtitleTextAppearance (Android.Content.Context context, int resId);
	public virtual void SetSubtitleTextColor (Android.Graphics.Color color);
	public virtual void SetTitle (int resId);
	public virtual void SetTitleTextAppearance (Android.Content.Context context, int resId);
	public virtual void SetTitleTextColor (Android.Graphics.Color color);
	public virtual bool ShowOverflowMenu ();

	// inner types
	public class LayoutParams : Android.App.ActionBar+LayoutParams, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected Toolbar (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public Toolbar (int width, int height, Android.Views.GravityFlags gravity);
		public Toolbar (int width, int height);
		public Toolbar (Android.Content.Context c, Android.Util.IAttributeSet attrs);
		public Toolbar (Android.Views.ViewGroup.LayoutParams source);
		public Toolbar (Android.Views.ViewGroup.MarginLayoutParams source);
		public Toolbar (Android.App.ActionBar.LayoutParams source);
		public Toolbar (Toolbar.LayoutParams source);
		public Toolbar (Android.Views.GravityFlags gravity);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
	public interface IOnMenuItemClickListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual bool OnMenuItemClick (Android.Views.IMenuItem item);
	}
	public class MenuItemClickEventArgs : System.EventArgs {
		// constructors
		public Toolbar (bool handled, Android.Views.IMenuItem item);
		// properties
		public bool Handled { get; set; }
		public Android.Views.IMenuItem Item { get; }
	}
}
```

## Namespace Java.Lang

### Type Changed: Java.Lang.JavaSystem

Removed method:

```
public static string MapLibraryName (string userLibName);
```

Added method:

```
public static string MapLibraryName (string nickname);
```

### Type Changed: Java.Lang.Runtime

Removed methods:

```
public virtual void Load (string pathName);
	public System.Threading.Tasks.Task LoadAsync (string pathName);
	public virtual void LoadLibrary (string libName);
	public System.Threading.Tasks.Task LoadLibraryAsync (string libName);
```

Added methods:

```
public virtual void Load (string absolutePath);
	public System.Threading.Tasks.Task LoadAsync (string absolutePath);
	public virtual void LoadLibrary (string nickname);
	public System.Threading.Tasks.Task LoadLibraryAsync (string nickname);
```

### Type Changed: Java.Lang.String

Removed method:

```
public bool ContentEquals (StringBuffer strbuf);
```

Added method:

```
public bool ContentEquals (StringBuffer sb);
```

## Namespace Java.Lang.Reflect

### Type Changed: Java.Lang.Reflect.Proxy

Removed method:

```
public static Java.Lang.Object NewProxyInstance (Java.Lang.ClassLoader loader, Java.Lang.Class[] interfaces, IInvocationHandler h);
```

Added method:

```
public static Java.Lang.Object NewProxyInstance (Java.Lang.ClassLoader loader, Java.Lang.Class[] interfaces, IInvocationHandler invocationHandler);
```

## Namespace Java.Text

### Type Changed: Java.Text.BreakIterator

Removed methods:

```
public static BreakIterator GetCharacterInstance (Java.Util.Locale where);
	public static BreakIterator GetLineInstance (Java.Util.Locale where);
	public static BreakIterator GetSentenceInstance (Java.Util.Locale where);
	public static BreakIterator GetWordInstance (Java.Util.Locale where);
```

Added methods:

```
public static BreakIterator GetCharacterInstance (Java.Util.Locale locale);
	public static BreakIterator GetLineInstance (Java.Util.Locale locale);
	public static BreakIterator GetSentenceInstance (Java.Util.Locale locale);
	public static BreakIterator GetWordInstance (Java.Util.Locale locale);
```

## Namespace Java.Util

### Type Changed: Java.Util.Locale

Removed methods:

```
public static Locale ForLanguageTag (string p0);
	public string GetDisplayScript (Locale p0);
	public string GetExtension (char p0);
	public string GetUnicodeLocaleType (string p0);
```

Added methods:

```
public static Locale ForLanguageTag (string languageTag);
	public string GetDisplayScript (Locale locale);
	public string GetExtension (char extensionKey);
	public string GetUnicodeLocaleType (string keyWord);
```

### New Type Java.Util.IllformedLocaleException

```
public class IllformedLocaleException : Java.Lang.RuntimeException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected IllformedLocaleException (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public IllformedLocaleException (string message, int errorIndex);
	public IllformedLocaleException (string message);
	public IllformedLocaleException ();
	// properties
	public virtual int ErrorIndex { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

## Namespace Java.Util.Concurrent

### New Type Java.Util.Concurrent.ConcurrentLinkedDeque

```
public class ConcurrentLinkedDeque : Java.Util.AbstractCollection, Java.IO.ISerializable, Java.Util.IDeque, Android.Runtime.IJavaObject, System.IDisposable, Java.Util.IQueue, Java.Util.ICollection, Java.Lang.IIterable {
	// constructors
	protected ConcurrentLinkedDeque (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConcurrentLinkedDeque ();
	public ConcurrentLinkedDeque (System.Collections.ICollection c);
	// properties
	public virtual Java.Lang.Object First { get; }
	public virtual Java.Lang.Object Last { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void AddFirst (Java.Lang.Object e);
	public virtual void AddLast (Java.Lang.Object e);
	public virtual Java.Util.IIterator DescendingIterator ();
	public virtual Java.Lang.Object Element ();
	public override Java.Util.IIterator Iterator ();
	public virtual bool Offer (Java.Lang.Object e);
	public virtual bool OfferFirst (Java.Lang.Object e);
	public virtual bool OfferLast (Java.Lang.Object e);
	public virtual Java.Lang.Object Peek ();
	public virtual Java.Lang.Object PeekFirst ();
	public virtual Java.Lang.Object PeekLast ();
	public virtual Java.Lang.Object Poll ();
	public virtual Java.Lang.Object PollFirst ();
	public virtual Java.Lang.Object PollLast ();
	public virtual Java.Lang.Object Pop ();
	public virtual void Push (Java.Lang.Object e);
	public virtual Java.Lang.Object Remove ();
	public virtual Java.Lang.Object RemoveFirst ();
	public virtual bool RemoveFirstOccurrence (Java.Lang.Object o);
	public virtual Java.Lang.Object RemoveLast ();
	public virtual bool RemoveLastOccurrence (Java.Lang.Object o);
	public override int Size ();
}
```

### New Type Java.Util.Concurrent.ForkJoinPool

```
public class ForkJoinPool : Java.Util.Concurrent.AbstractExecutorService, IExecutorService, IExecutor, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ForkJoinPool (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ForkJoinPool ();
	public ForkJoinPool (int parallelism, ForkJoinPool.IForkJoinWorkerThreadFactory factory, Java.Lang.Thread.IUncaughtExceptionHandler handler, bool asyncMode);
	public ForkJoinPool (int parallelism);
	// properties
	public virtual int ActiveThreadCount { get; }
	public virtual bool AsyncMode { get; }
	public static ForkJoinPool.IForkJoinWorkerThreadFactory DefaultForkJoinWorkerThreadFactory { get; set; }
	public virtual ForkJoinPool.IForkJoinWorkerThreadFactory Factory { get; }
	public virtual bool HasQueuedSubmissions { get; }
	public virtual bool IsQuiescent { get; }
	public override bool IsShutdown { get; }
	public override bool IsTerminated { get; }
	public virtual bool IsTerminating { get; }
	public virtual int Parallelism { get; }
	public virtual int PoolSize { get; }
	public virtual int QueuedSubmissionCount { get; }
	public virtual long QueuedTaskCount { get; }
	public virtual int RunningThreadCount { get; }
	public virtual long StealCount { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual Java.Lang.Thread.IUncaughtExceptionHandler UncaughtExceptionHandler { get; }
	// methods
	public override bool AwaitTermination (long timeout, TimeUnit unit);
	protected virtual int DrainTasksTo (System.Collections.Generic.ICollection<ForkJoinTask> c);
	public override void Execute (Java.Lang.IRunnable task);
	public virtual void Execute (ForkJoinTask task);
	public virtual Java.Lang.Object Invoke (ForkJoinTask task);
	public static void ManagedBlock (ForkJoinPool.IManagedBlocker blocker);
	protected virtual ForkJoinTask PollSubmission ();
	public override void Shutdown ();
	public override System.Collections.Generic.IList<Java.Lang.IRunnable> ShutdownNow ();
	public virtual ForkJoinTask Submit (ForkJoinTask task);

	// inner types
	public interface IForkJoinWorkerThreadFactory : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual ForkJoinWorkerThread NewThread (ForkJoinPool pool);
	}
	public interface IManagedBlocker : Android.Runtime.IJavaObject, System.IDisposable {
		// properties
		public virtual bool IsReleasable { get; }
		// methods
		public virtual bool Block ();
	}
}
```

### New Type Java.Util.Concurrent.ForkJoinTask

```
public abstract class ForkJoinTask : Java.Lang.Object, Java.IO.ISerializable, IFuture, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ForkJoinTask (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ForkJoinTask ();
	// properties
	public Java.Lang.Throwable Exception { get; }
	public virtual bool IsCancelled { get; }
	public bool IsCompletedAbnormally { get; }
	public bool IsCompletedNormally { get; }
	public virtual bool IsDone { get; }
	public static ForkJoinPool Pool { get; }
	public static int QueuedTaskCount { get; }
	protected virtual Java.Lang.Object RawRawResult { get; }
	public static int SurplusQueuedTaskCount { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static ForkJoinTask Adapt (Java.Lang.IRunnable runnable);
	public static ForkJoinTask Adapt (Java.Lang.IRunnable runnable, Java.Lang.Object result);
	public static ForkJoinTask Adapt (ICallable callable);
	public virtual bool Cancel (bool mayInterruptIfRunning);
	public virtual void Complete (Java.Lang.Object value);
	public virtual void CompleteExceptionally (Java.Lang.Throwable ex);
	protected virtual bool Exec ();
	public ForkJoinTask Fork ();
	public virtual Java.Lang.Object Get ();
	public virtual Java.Lang.Object Get (long timeout, TimeUnit unit);
	public static void HelpQuiesce ();
	public static bool InForkJoinPool ();
	public Java.Lang.Object Invoke ();
	public static System.Collections.ICollection InvokeAll (System.Collections.ICollection tasks);
	public static void InvokeAll (ForkJoinTask t1, ForkJoinTask t2);
	public static void InvokeAll (ForkJoinTask[] tasks);
	public Java.Lang.Object Join ();
	protected static ForkJoinTask PeekNextLocalTask ();
	protected static ForkJoinTask PollNextLocalTask ();
	protected static ForkJoinTask PollTask ();
	public void QuietlyInvoke ();
	public void QuietlyJoin ();
	public virtual void Reinitialize ();
	protected virtual void SetRawResult (Java.Lang.Object value);
	public virtual bool TryUnfork ();
}
```

### New Type Java.Util.Concurrent.ForkJoinWorkerThread

```
public class ForkJoinWorkerThread : Java.Lang.Thread, Java.Lang.IRunnable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ForkJoinWorkerThread (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected ForkJoinWorkerThread (ForkJoinPool pool);
	// properties
	public virtual ForkJoinPool Pool { get; }
	public virtual int PoolIndex { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual void OnStart ();
	protected virtual void OnTermination (Java.Lang.Throwable exception);
}
```

### New Type Java.Util.Concurrent.ITransferQueue

```
public interface ITransferQueue : IBlockingQueue, Java.Util.IQueue, Java.Util.ICollection, Java.Lang.IIterable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual bool HasWaitingConsumer { get; }
	public virtual int WaitingConsumerCount { get; }
	// methods
	public virtual void Transfer (Java.Lang.Object e);
	public virtual bool TryTransfer (Java.Lang.Object e);
	public virtual bool TryTransfer (Java.Lang.Object e, long timeout, TimeUnit unit);
}
```

### New Type Java.Util.Concurrent.LinkedTransferQueue

```
public class LinkedTransferQueue : Java.Util.AbstractQueue, Java.IO.ISerializable, ITransferQueue, Android.Runtime.IJavaObject, System.IDisposable, IBlockingQueue, Java.Util.IQueue, Java.Util.ICollection, Java.Lang.IIterable {
	// constructors
	protected LinkedTransferQueue (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LinkedTransferQueue ();
	public LinkedTransferQueue (System.Collections.ICollection c);
	// properties
	public virtual bool HasWaitingConsumer { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual int WaitingConsumerCount { get; }
	// methods
	public virtual int DrainTo (System.Collections.ICollection c);
	public virtual int DrainTo (System.Collections.ICollection c, int maxElements);
	public override Java.Util.IIterator Iterator ();
	public override bool Offer (Java.Lang.Object e);
	public virtual bool Offer (Java.Lang.Object e, long timeout, TimeUnit unit);
	public override Java.Lang.Object Peek ();
	public virtual Java.Lang.Object Poll (long timeout, TimeUnit unit);
	public override Java.Lang.Object Poll ();
	public virtual void Put (Java.Lang.Object e);
	public virtual int RemainingCapacity ();
	public override int Size ();
	public virtual Java.Lang.Object Take ();
	public virtual void Transfer (Java.Lang.Object e);
	public virtual bool TryTransfer (Java.Lang.Object e);
	public virtual bool TryTransfer (Java.Lang.Object e, long timeout, TimeUnit unit);
}
```

### New Type Java.Util.Concurrent.Phaser

```
public class Phaser : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected Phaser (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Phaser (Phaser parent, int parties);
	public Phaser (Phaser parent);
	public Phaser ();
	public Phaser (int parties);
	// properties
	public virtual int ArrivedParties { get; }
	public virtual bool IsTerminated { get; }
	public virtual Phaser Parent { get; }
	public int Phase { get; }
	public virtual int RegisteredParties { get; }
	public virtual Phaser Root { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual int UnarrivedParties { get; }
	// methods
	public virtual int Arrive ();
	public virtual int ArriveAndAwaitAdvance ();
	public virtual int ArriveAndDeregister ();
	public virtual int AwaitAdvance (int phase);
	public virtual int AwaitAdvanceInterruptibly (int phase, long timeout, TimeUnit unit);
	public virtual int AwaitAdvanceInterruptibly (int phase);
	public virtual int BulkRegister (int parties);
	public virtual void ForceTermination ();
	protected virtual bool OnAdvance (int phase, int registeredParties);
	public virtual int Register ();
}
```

### New Type Java.Util.Concurrent.RecursiveAction

```
public abstract class RecursiveAction : Java.Util.Concurrent.ForkJoinTask, Java.IO.ISerializable, IFuture, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RecursiveAction (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RecursiveAction ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual void Compute ();
	protected override bool Exec ();
}
```

### New Type Java.Util.Concurrent.RecursiveTask

```
public abstract class RecursiveTask : Java.Util.Concurrent.ForkJoinTask, Java.IO.ISerializable, IFuture, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RecursiveTask (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RecursiveTask ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual Java.Lang.Object Compute ();
	protected override bool Exec ();
}
```

### New Type Java.Util.Concurrent.ThreadLocalRandom

```
public class ThreadLocalRandom : Java.Util.Random, Java.IO.ISerializable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ThreadLocalRandom (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static ThreadLocalRandom Current ();
	public virtual double NextDouble (double n);
	public virtual double NextDouble (double least, double bound);
	public virtual int NextInt (int least, int bound);
	public virtual long NextLong (long n);
	public virtual long NextLong (long least, long bound);
}
```

## New Namespace Android.App.Job

### New Type Android.App.Job.BackoffPolicy

```
[Serializable]
public enum BackoffPolicy {
	Exponential = 1,
	Linear = 0,
}
```

### New Type Android.App.Job.JobInfo

```
public class JobInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected JobInfo (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const long DefaultInitialBackoffMillis;
	public static const long MaxBackoffDelayMillis;
	// properties
	public virtual BackoffPolicy BackoffPolicyValue { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual Android.OS.PersistableBundle Extras { get; }
	public virtual int Id { get; }
	public virtual long InitialBackoffMillis { get; }
	public virtual long IntervalMillis { get; }
	public virtual bool IsPeriodic { get; }
	public virtual bool IsPersisted { get; }
	public virtual bool IsRequireCharging { get; }
	public virtual bool IsRequireDeviceIdle { get; }
	public virtual long MaxExecutionDelayMillis { get; }
	public virtual long MinLatencyMillis { get; }
	public virtual NetworkType NetworkType { get; }
	public virtual Android.Content.ComponentName Service { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel out, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public JobInfo (int jobId, Android.Content.ComponentName jobService);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public JobInfo Build ();
		public JobInfo.Builder SetBackoffCriteria (long initialBackoffMillis, BackoffPolicy backoffPolicy);
		public JobInfo.Builder SetExtras (Android.OS.PersistableBundle extras);
		public JobInfo.Builder SetMinimumLatency (long minLatencyMillis);
		public JobInfo.Builder SetOverrideDeadline (long maxExecutionDelayMillis);
		public JobInfo.Builder SetPeriodic (long intervalMillis);
		public JobInfo.Builder SetPersisted (bool isPersisted);
		public JobInfo.Builder SetRequiredNetworkType (NetworkType networkType);
		public JobInfo.Builder SetRequiresCharging (bool requiresCharging);
		public JobInfo.Builder SetRequiresDeviceIdle (bool requiresDeviceIdle);
	}
}
```

### New Type Android.App.Job.JobParameters

```
public class JobParameters : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected JobParameters (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual Android.OS.PersistableBundle Extras { get; }
	public virtual bool IsOverrideDeadlineExpired { get; }
	public virtual int JobId { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.App.Job.JobScheduler

```
public abstract class JobScheduler : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected JobScheduler (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JobScheduler ();
	// fields
	public static const int ResultFailure;
	public static const int ResultSuccess;
	// properties
	public virtual System.Collections.Generic.IList<JobInfo> AllPendingJobs { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Cancel (int jobId);
	public virtual void CancelAll ();
	public virtual int Schedule (JobInfo job);
}
```

### New Type Android.App.Job.JobService

```
public abstract class JobService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected JobService (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JobService ();
	// fields
	public static const string PermissionBind = "android.permission.BIND_JOB_SERVICE";
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void JobFinished (JobParameters params, bool needsReschedule);
	public override Android.OS.IBinder OnBind (Android.Content.Intent p0);
	public virtual bool OnStartJob (JobParameters params);
	public virtual bool OnStopJob (JobParameters params);
}
```

### New Type Android.App.Job.NetworkType

```
[Serializable]
public enum NetworkType {
	Any = 1,
	None = 0,
	Unmetered = 2,
}
```

## New Namespace Android.App.Usage

### New Type Android.App.Usage.ConfigurationStats

```
public sealed class ConfigurationStats : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public ConfigurationStats (ConfigurationStats stats);
	// properties
	public int ActivationCount { get; }
	public Android.Content.Res.Configuration Configuration { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public long FirstTimeStamp { get; }
	public long LastTimeActive { get; }
	public long LastTimeStamp { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public long TotalTimeActive { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.App.Usage.UsageEvents

```
public sealed class UsageEvents : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public bool HasNextEvent { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public bool GetNextEvent (UsageEvents.Event eventOut);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Event : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public UsageEvents ();
		// properties
		public string ClassName { get; }
		public Android.Content.Res.Configuration Configuration { get; }
		public UsageEventType EventType { get; }
		public string PackageName { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		public long TimeStamp { get; }
	}
}
```

### New Type Android.App.Usage.UsageEventType

```
[Serializable]
public enum UsageEventType {
	ConfigurationChange = 5,
	MoveToBackground = 2,
	MoveToForeground = 1,
	None = 0,
}
```

### New Type Android.App.Usage.UsageStats

```
public sealed class UsageStats : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public UsageStats (UsageStats stats);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public long FirstTimeStamp { get; }
	public long LastTimeStamp { get; }
	public long LastTimeUsed { get; }
	public string PackageName { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public long TotalTimeInForeground { get; }
	// methods
	public void Add (UsageStats right);
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.App.Usage.UsageStatsInterval

```
[Serializable]
public enum UsageStatsInterval {
	Best = 4,
	Daily = 0,
	Monthly = 2,
	Weekly = 1,
	Yearly = 3,
}
```

### New Type Android.App.Usage.UsageStatsManager

```
public sealed class UsageStatsManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public System.Collections.Generic.IDictionary<System.String,Android.App.Usage.UsageStats> QueryAndAggregateUsageStats (long beginTime, long endTime);
	public System.Collections.Generic.IList<ConfigurationStats> QueryConfigurations (UsageStatsInterval intervalType, long beginTime, long endTime);
	public UsageEvents QueryEvents (long beginTime, long endTime);
	public System.Collections.Generic.IList<UsageStats> QueryUsageStats (UsageStatsInterval intervalType, long beginTime, long endTime);
}
```

## New Namespace Android.Bluetooth.LE

### New Type Android.Bluetooth.LE.AdvertiseCallback

```
public abstract class AdvertiseCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected AdvertiseCallback (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AdvertiseCallback ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnStartFailure (AdvertiseFailure errorCode);
	public virtual void OnStartSuccess (AdvertiseSettings settingsInEffect);
}
```

### New Type Android.Bluetooth.LE.AdvertiseData

```
public sealed class AdvertiseData : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public bool IncludeDeviceName { get; }
	public bool IncludeTxPowerLevel { get; }
	public Android.Util.SparseArray ManufacturerSpecificData { get; }
	public System.Collections.Generic.IDictionary<Android.OS.ParcelUuid,System.Byte[]> ServiceData { get; }
	public System.Collections.Generic.IList<Android.OS.ParcelUuid> ServiceUuids { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public AdvertiseData ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public AdvertiseData.Builder AddManufacturerData (int manufacturerId, byte[] manufacturerSpecificData);
		public AdvertiseData.Builder AddServiceData (Android.OS.ParcelUuid serviceDataUuid, byte[] serviceData);
		public AdvertiseData.Builder AddServiceUuid (Android.OS.ParcelUuid serviceUuid);
		public AdvertiseData Build ();
		public AdvertiseData.Builder SetIncludeDeviceName (bool includeDeviceName);
		public AdvertiseData.Builder SetIncludeTxPowerLevel (bool includeTxPowerLevel);
	}
}
```

### New Type Android.Bluetooth.LE.AdvertiseFailure

```
[Serializable]
public enum AdvertiseFailure {
	AlreadyStarted = 3,
	DataTooLarge = 1,
	FeatureUnsupported = 5,
	InternalError = 4,
	TooManyAdvertisers = 2,
}
```

### New Type Android.Bluetooth.LE.AdvertiseMode

```
[Serializable]
public enum AdvertiseMode {
	Balanced = 1,
	LowLatency = 2,
	LowPower = 0,
}
```

### New Type Android.Bluetooth.LE.AdvertiseSettings

```
public sealed class AdvertiseSettings : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public bool IsConnectable { get; }
	public AdvertiseMode Mode { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public int Timeout { get; }
	public AdvertiseTx TxPowerLevel { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public AdvertiseSettings ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public AdvertiseSettings Build ();
		public AdvertiseSettings.Builder SetAdvertiseMode (AdvertiseMode advertiseMode);
		public AdvertiseSettings.Builder SetConnectable (bool connectable);
		public AdvertiseSettings.Builder SetTimeout (int timeoutMillis);
		public AdvertiseSettings.Builder SetTxPowerLevel (AdvertiseTx txPowerLevel);
	}
}
```

### New Type Android.Bluetooth.LE.AdvertiseTx

```
[Serializable]
public enum AdvertiseTx {
	PowerHigh = 3,
	PowerLow = 1,
	PowerMedium = 2,
	PowerUltraLow = 0,
}
```

### New Type Android.Bluetooth.LE.BluetoothLeAdvertiser

```
public sealed class BluetoothLeAdvertiser : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void StartAdvertising (AdvertiseSettings settings, AdvertiseData advertiseData, AdvertiseCallback callback);
	public void StartAdvertising (AdvertiseSettings settings, AdvertiseData advertiseData, AdvertiseData scanResponse, AdvertiseCallback callback);
	public void StopAdvertising (AdvertiseCallback callback);
}
```

### New Type Android.Bluetooth.LE.BluetoothLeScanner

```
public sealed class BluetoothLeScanner : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void FlushPendingScanResults (ScanCallback callback);
	public void StartScan (ScanCallback callback);
	public void StartScan (System.Collections.Generic.IList<ScanFilter> filters, ScanSettings settings, ScanCallback callback);
	public void StopScan (ScanCallback callback);
}
```

### New Type Android.Bluetooth.LE.ScanCallback

```
public abstract class ScanCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected ScanCallback (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ScanCallback ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OnBatchScanResults (System.Collections.Generic.IList<ScanResult> results);
	public virtual void OnScanFailed (ScanFailure errorCode);
	public virtual void OnScanResult (ScanCallbackType callbackType, ScanResult result);
}
```

### New Type Android.Bluetooth.LE.ScanCallbackType

```
[Serializable]
public enum ScanCallbackType {
	AllMatches = 1,
}
```

### New Type Android.Bluetooth.LE.ScanFailure

```
[Serializable]
public enum ScanFailure {
	AlreadyStarted = 1,
	ApplicationRegistrationFailed = 2,
	FeatureUnsupported = 4,
	InternalError = 3,
}
```

### New Type Android.Bluetooth.LE.ScanFilter

```
public sealed class ScanFilter : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public string DeviceAddress { get; }
	public string DeviceName { get; }
	public int ManufacturerId { get; }
	public Android.OS.ParcelUuid ServiceDataUuid { get; }
	public Android.OS.ParcelUuid ServiceUuid { get; }
	public Android.OS.ParcelUuid ServiceUuidMask { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public byte[] GetManufacturerData ();
	public byte[] GetManufacturerDataMask ();
	public byte[] GetServiceData ();
	public byte[] GetServiceDataMask ();
	public bool Matches (ScanResult scanResult);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public ScanFilter ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public ScanFilter Build ();
		public ScanFilter.Builder SetDeviceAddress (string deviceAddress);
		public ScanFilter.Builder SetDeviceName (string deviceName);
		public ScanFilter.Builder SetManufacturerData (int manufacturerId, byte[] manufacturerData, byte[] manufacturerDataMask);
		public ScanFilter.Builder SetManufacturerData (int manufacturerId, byte[] manufacturerData);
		public ScanFilter.Builder SetServiceData (Android.OS.ParcelUuid serviceDataUuid, byte[] serviceData);
		public ScanFilter.Builder SetServiceData (Android.OS.ParcelUuid serviceDataUuid, byte[] serviceData, byte[] serviceDataMask);
		public ScanFilter.Builder SetServiceUuid (Android.OS.ParcelUuid serviceUuid);
		public ScanFilter.Builder SetServiceUuid (Android.OS.ParcelUuid serviceUuid, Android.OS.ParcelUuid uuidMask);
	}
}
```

### New Type Android.Bluetooth.LE.ScanMode

```
[Serializable]
public enum ScanMode {
	Balanced = 1,
	LowLatency = 2,
	LowPower = 0,
}
```

### New Type Android.Bluetooth.LE.ScanRecord

```
public sealed class ScanRecord : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public int AdvertiseFlags { get; }
	public string DeviceName { get; }
	public Android.Util.SparseArray ManufacturerSpecificData { get; }
	public System.Collections.Generic.IDictionary<Android.OS.ParcelUuid,System.Byte[]> ServiceData { get; }
	public System.Collections.Generic.IList<Android.OS.ParcelUuid> ServiceUuids { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public AdvertiseTx TxPowerLevel { get; }
	// methods
	public byte[] GetBytes ();
	public byte[] GetManufacturerSpecificData (int manufacturerId);
	public byte[] GetServiceData (Android.OS.ParcelUuid serviceDataUuid);
}
```

### New Type Android.Bluetooth.LE.ScanResult

```
public sealed class ScanResult : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public ScanResult (Android.Bluetooth.BluetoothDevice device, ScanRecord scanRecord, int rssi, long timestampNanos);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public Android.Bluetooth.BluetoothDevice Device { get; }
	public int Rssi { get; }
	public ScanRecord ScanRecord { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public long TimestampNanos { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Bluetooth.LE.ScanSettings

```
public sealed class ScanSettings : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public ScanCallbackType CallbackType { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public long ReportDelayMillis { get; }
	public ScanMode ScanMode { get; }
	public int ScanResultType { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public ScanSettings ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public ScanSettings Build ();
		public ScanSettings.Builder SetReportDelay (long reportDelayMillis);
		public ScanSettings.Builder SetScanMode (ScanMode scanMode);
	}
}
```

## New Namespace Android.Hardware.Camera2

### New Type Android.Hardware.Camera2.CameraAccessErrorType

```
[Serializable]
public enum CameraAccessErrorType {
	Disabled = 1,
	Disconnected = 2,
	Error = 3,
}
```

### New Type Android.Hardware.Camera2.CameraAccessException

```
public class CameraAccessException : Android.Util.AndroidException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected CameraAccessException (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CameraAccessException (CameraAccessErrorType problem, Java.Lang.Throwable cause);
	public CameraAccessException (CameraAccessErrorType problem, string message, Java.Lang.Throwable cause);
	public CameraAccessException (CameraAccessErrorType problem, string message);
	public CameraAccessException (CameraAccessErrorType problem);
	// properties
	public CameraAccessErrorType Reason { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Android.Hardware.Camera2.CameraCaptureSession

```
public abstract class CameraCaptureSession : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CameraCaptureSession (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CameraCaptureSession ();
	// properties
	public virtual CameraDevice Device { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void AbortCaptures ();
	public virtual int Capture (CaptureRequest request, CameraCaptureSession.CaptureCallback listener, Android.OS.Handler handler);
	public virtual int CaptureBurst (System.Collections.Generic.IList<CaptureRequest> requests, CameraCaptureSession.CaptureCallback listener, Android.OS.Handler handler);
	public virtual void Close ();
	public virtual int SetRepeatingBurst (System.Collections.Generic.IList<CaptureRequest> requests, CameraCaptureSession.CaptureCallback listener, Android.OS.Handler handler);
	public virtual int SetRepeatingRequest (CaptureRequest request, CameraCaptureSession.CaptureCallback listener, Android.OS.Handler handler);
	public virtual void StopRepeating ();

	// inner types
	public abstract class CaptureCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected CameraCaptureSession (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public CameraCaptureSession ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnCaptureCompleted (CameraCaptureSession session, CaptureRequest request, TotalCaptureResult result);
		public virtual void OnCaptureFailed (CameraCaptureSession session, CaptureRequest request, CaptureFailure failure);
		public virtual void OnCaptureProgressed (CameraCaptureSession session, CaptureRequest request, CaptureResult partialResult);
		public virtual void OnCaptureSequenceAborted (CameraCaptureSession session, int sequenceId);
		public virtual void OnCaptureSequenceCompleted (CameraCaptureSession session, int sequenceId, long frameNumber);
		public virtual void OnCaptureStarted (CameraCaptureSession session, CaptureRequest request, long timestamp, long frameNumber);
	}
	public abstract class StateCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected CameraCaptureSession (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public CameraCaptureSession ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnActive (CameraCaptureSession session);
		public virtual void OnClosed (CameraCaptureSession session);
		public virtual void OnConfigured (CameraCaptureSession session);
		public virtual void OnConfigureFailed (CameraCaptureSession session);
		public virtual void OnReady (CameraCaptureSession session);
	}
}
```

### New Type Android.Hardware.Camera2.CameraCharacteristics

```
public sealed class CameraCharacteristics : Android.Hardware.Camera2.CameraMetadata, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public System.Collections.Generic.IList<CaptureRequest.Key> AvailableCaptureRequestKeys { get; }
	public System.Collections.Generic.IList<CaptureResult.Key> AvailableCaptureResultKeys { get; }
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
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public static CameraCharacteristics.Key TonemapAvailableToneMapModes { get; set; }
	public static CameraCharacteristics.Key TonemapMaxCurvePoints { get; set; }
	// methods
	public Java.Lang.Object Get (CameraCharacteristics.Key key);

	// inner types
	public sealed class Key : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// properties
		public string Name { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public override bool Equals (Java.Lang.Object o);
		public override int GetHashCode ();
	}
}
```

### New Type Android.Hardware.Camera2.CameraDevice

```
public abstract class CameraDevice : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CameraDevice (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual string Id { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Close ();
	public virtual CaptureRequest.Builder CreateCaptureRequest (CameraTemplate templateType);
	public virtual void CreateCaptureSession (System.Collections.Generic.IList<Android.Views.Surface> outputs, CameraCaptureSession.StateCallback callback, Android.OS.Handler handler);

	// inner types
	public abstract class StateCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected CameraDevice (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public CameraDevice ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnClosed (CameraDevice camera);
		public virtual void OnDisconnected (CameraDevice camera);
		public virtual void OnError (CameraDevice camera, CameraError error);
		public virtual void OnOpened (CameraDevice camera);
	}
}
```

### New Type Android.Hardware.Camera2.CameraError

```
[Serializable]
public enum CameraError {
	CameraDevice = 4,
	CameraDisabled = 3,
	CameraInUse = 1,
	CameraService = 5,
	MaxCamerasInUse = 2,
}
```

### New Type Android.Hardware.Camera2.CameraManager

```
public sealed class CameraManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public CameraCharacteristics GetCameraCharacteristics (string cameraId);
	public string[] GetCameraIdList ();
	public void OpenCamera (string cameraId, CameraDevice.StateCallback callback, Android.OS.Handler handler);
	public void RegisterAvailabilityCallback (CameraManager.AvailabilityCallback callback, Android.OS.Handler handler);
	public void UnregisterAvailabilityCallback (CameraManager.AvailabilityCallback callback);

	// inner types
	public abstract class AvailabilityCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected CameraManager (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public CameraManager ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnCameraAvailable (string cameraId);
		public virtual void OnCameraUnavailable (string cameraId);
	}
}
```

### New Type Android.Hardware.Camera2.CameraMetadata

```
public abstract class CameraMetadata : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CameraMetadata (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual System.Collections.IList Keys { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Android.Hardware.Camera2.CameraTemplate

```
[Serializable]
public enum CameraTemplate {
	Manual = 6,
	Preview = 1,
	Record = 3,
	StillCapture = 2,
	VideoSnapshot = 4,
	ZeroShutterLag = 5,
}
```

### New Type Android.Hardware.Camera2.CaptureFailure

```
public class CaptureFailure : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CaptureFailure (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual long FrameNumber { get; }
	public virtual CaptureFailureReason Reason { get; }
	public virtual CaptureRequest Request { get; }
	public virtual int SequenceId { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool WasImageCaptured ();
}
```

### New Type Android.Hardware.Camera2.CaptureFailureReason

```
[Serializable]
public enum CaptureFailureReason {
	Error = 0,
	Flushed = 1,
}
```

### New Type Android.Hardware.Camera2.CaptureRequest

```
public sealed class CaptureRequest : Android.Hardware.Camera2.CameraMetadata, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
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
	public Java.Lang.Object Tag { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public static CaptureRequest.Key TonemapCurve { get; set; }
	public static CaptureRequest.Key TonemapMode { get; set; }
	// methods
	public virtual int DescribeContents ();
	public Java.Lang.Object Get (CaptureRequest.Key key);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public void AddTarget (Android.Views.Surface outputTarget);
		public CaptureRequest Build ();
		public Java.Lang.Object Get (CaptureRequest.Key key);
		public void RemoveTarget (Android.Views.Surface outputTarget);
		public void Set (CaptureRequest.Key key, Java.Lang.Object value);
		public void SetTag (Java.Lang.Object tag);
	}
	public sealed class Key : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// properties
		public string Name { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public override bool Equals (Java.Lang.Object o);
		public override int GetHashCode ();
	}
}
```

### New Type Android.Hardware.Camera2.CaptureResult

```
public class CaptureResult : Android.Hardware.Camera2.CameraMetadata, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected CaptureResult (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
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
	public virtual long FrameNumber { get; }
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
	public virtual CaptureRequest Request { get; }
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
	public virtual int SequenceId { get; }
	public static CaptureResult.Key ShadingMode { get; set; }
	public static CaptureResult.Key StatisticsFaceDetectMode { get; set; }
	public static CaptureResult.Key StatisticsFaces { get; set; }
	public static CaptureResult.Key StatisticsHotPixelMap { get; set; }
	public static CaptureResult.Key StatisticsHotPixelMapMode { get; set; }
	public static CaptureResult.Key StatisticsLensShadingCorrectionMap { get; set; }
	public static CaptureResult.Key StatisticsLensShadingMapMode { get; set; }
	public static CaptureResult.Key StatisticsSceneFlicker { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public static CaptureResult.Key TonemapCurve { get; set; }
	public static CaptureResult.Key TonemapMode { get; set; }
	// methods
	public virtual Java.Lang.Object Get (CaptureResult.Key key);

	// inner types
	public sealed class Key : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// properties
		public string Name { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public override bool Equals (Java.Lang.Object o);
		public override int GetHashCode ();
	}
}
```

### New Type Android.Hardware.Camera2.ColorCorrectionAberrationMode

```
[Serializable]
public enum ColorCorrectionAberrationMode {
	Fast = 1,
	HighQuality = 2,
	Off = 0,
}
```

### New Type Android.Hardware.Camera2.ColorCorrectionMode

```
[Serializable]
public enum ColorCorrectionMode {
	Fast = 1,
	HighQuality = 2,
	TransformMatrix = 0,
}
```

### New Type Android.Hardware.Camera2.ControlAEAntibanding

```
[Serializable]
public enum ControlAEAntibanding {
	Mode50hz = 1,
	Mode60hz = 2,
	ModeAuto = 3,
	ModeOff = 0,
}
```

### New Type Android.Hardware.Camera2.ControlAEMode

```
[Serializable]
public enum ControlAEMode {
	Off = 0,
	On = 1,
	OnAlwaysFlash = 3,
	OnAutoFlash = 2,
	OnAutoFlashRedeye = 4,
}
```

### New Type Android.Hardware.Camera2.ControlAEPrecaptureTrigger

```
[Serializable]
public enum ControlAEPrecaptureTrigger {
	Idle = 0,
	Start = 1,
}
```

### New Type Android.Hardware.Camera2.ControlAEState

```
[Serializable]
public enum ControlAEState {
	Converged = 2,
	FlashRequired = 4,
	Inactive = 0,
	Locked = 3,
	Precapture = 5,
	Searching = 1,
}
```

### New Type Android.Hardware.Camera2.ControlAFMode

```
[Serializable]
public enum ControlAFMode {
	Auto = 1,
	ContinuousPicture = 4,
	ContinuousVideo = 3,
	Edof = 5,
	Macro = 2,
	Off = 0,
}
```

### New Type Android.Hardware.Camera2.ControlAFState

```
[Serializable]
public enum ControlAFState {
	ActiveScan = 3,
	FocusedLocked = 4,
	Inactive = 0,
	NotFocusedLocked = 5,
	PassiveFocused = 2,
	PassiveScan = 1,
	PassiveUnfocused = 6,
}
```

### New Type Android.Hardware.Camera2.ControlAFTrigger

```
[Serializable]
public enum ControlAFTrigger {
	Cancel = 2,
	Idle = 0,
	Start = 1,
}
```

### New Type Android.Hardware.Camera2.ControlAwbMode

```
[Serializable]
public enum ControlAwbMode {
	Auto = 1,
	CloudyDaylight = 6,
	Daylight = 5,
	Fluorescent = 3,
	Incandescent = 2,
	Off = 0,
	Shade = 8,
	Twilight = 7,
	WarmFluorescent = 4,
}
```

### New Type Android.Hardware.Camera2.ControlAwbState

```
[Serializable]
public enum ControlAwbState {
	Converged = 2,
	Inactive = 0,
	Locked = 3,
	Searching = 1,
}
```

### New Type Android.Hardware.Camera2.ControlCaptureIntent

```
[Serializable]
public enum ControlCaptureIntent {
	Custom = 0,
	Manual = 6,
	Preview = 1,
	StillCapture = 2,
	VideoRecord = 3,
	VideoSnapshot = 4,
	ZeroShutterLag = 5,
}
```

### New Type Android.Hardware.Camera2.ControlEffectMode

```
[Serializable]
public enum ControlEffectMode {
	Aqua = 8,
	Blackboard = 7,
	Mono = 1,
	Negative = 2,
	Off = 0,
	Posterize = 5,
	Sepia = 4,
	Solarize = 3,
	Whiteboard = 6,
}
```

### New Type Android.Hardware.Camera2.ControlMode

```
[Serializable]
public enum ControlMode {
	Auto = 1,
	Off = 0,
	OffKeepState = 3,
	UseSceneMode = 2,
}
```

### New Type Android.Hardware.Camera2.ControlSceneMode

```
[Serializable]
public enum ControlSceneMode {
	Action = 2,
	Barcode = 16,
	Beach = 8,
	Candlelight = 15,
	Disabled = 0,
	FacePriority = 1,
	Fireworks = 12,
	HighSpeedVideo = 17,
	Landscape = 4,
	Night = 5,
	NightPortrait = 6,
	Party = 14,
	Portrait = 3,
	Snow = 9,
	Sports = 13,
	Steadyphoto = 11,
	Sunset = 10,
	Theatre = 7,
}
```

### New Type Android.Hardware.Camera2.ControlVideoStabilizationMode

```
[Serializable]
public enum ControlVideoStabilizationMode {
	Off = 0,
	On = 1,
}
```

### New Type Android.Hardware.Camera2.DngCreator

```
public sealed class DngCreator : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public DngCreator (CameraCharacteristics characteristics, CaptureResult metadata);
	// fields
	public static const int MaxThumbnailDimension;
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void Close ();
	public DngCreator SetDescription (string description);
	public DngCreator SetLocation (Android.Locations.Location location);
	public DngCreator SetOrientation (Android.Media.Orientation orientation);
	public DngCreator SetThumbnail (Android.Media.Image pixels);
	public DngCreator SetThumbnail (Android.Graphics.Bitmap pixels);
	public void WriteByteBuffer (System.IO.Stream dngOutput, Android.Util.Size size, Java.Nio.ByteBuffer pixels, long offset);
	public void WriteImage (System.IO.Stream dngOutput, Android.Media.Image pixels);
	public void WriteInputStream (System.IO.Stream dngOutput, Android.Util.Size size, System.IO.Stream pixels, long offset);
}
```

### New Type Android.Hardware.Camera2.EdgeMode

```
[Serializable]
public enum EdgeMode {
	Fast = 1,
	HighQuality = 2,
	Off = 0,
}
```

### New Type Android.Hardware.Camera2.FlashMode

```
[Serializable]
public enum FlashMode {
	Off = 0,
	Single = 1,
	Torch = 2,
}
```

### New Type Android.Hardware.Camera2.FlashState

```
[Serializable]
public enum FlashState {
	Charging = 1,
	Fired = 3,
	Partial = 4,
	Ready = 2,
	Unavailable = 0,
}
```

### New Type Android.Hardware.Camera2.HotPixelMode

```
[Serializable]
public enum HotPixelMode {
	Fast = 1,
	HighQuality = 2,
	Off = 0,
}
```

### New Type Android.Hardware.Camera2.InfoSupportedHardwareLevel

```
[Serializable]
public enum InfoSupportedHardwareLevel {
	Full = 1,
	Legacy = 2,
	Limited = 0,
}
```

### New Type Android.Hardware.Camera2.LensFacing

```
[Serializable]
public enum LensFacing {
	Back = 1,
	Front = 0,
}
```

### New Type Android.Hardware.Camera2.LensInfoFocusDistanceCalibration

```
[Serializable]
public enum LensInfoFocusDistanceCalibration {
	Approximate = 1,
	Calibrated = 2,
	Uncalibrated = 0,
}
```

### New Type Android.Hardware.Camera2.LensOpticalStabilizationMode

```
[Serializable]
public enum LensOpticalStabilizationMode {
	Off = 0,
	On = 1,
}
```

### New Type Android.Hardware.Camera2.LensState

```
[Serializable]
public enum LensState {
	Moving = 1,
	Stationary = 0,
}
```

### New Type Android.Hardware.Camera2.NoiseReductionMode

```
[Serializable]
public enum NoiseReductionMode {
	Fast = 1,
	HighQuality = 2,
	Off = 0,
}
```

### New Type Android.Hardware.Camera2.RequestAvailableCapabilities

```
[Serializable]
public enum RequestAvailableCapabilities {
	BackwardCompatible = 0,
	ManualPostProcessing = 2,
	ManualSensor = 1,
	Raw = 3,
}
```

### New Type Android.Hardware.Camera2.ScalerCroppingType

```
[Serializable]
public enum ScalerCroppingType {
	CenterOnly = 0,
	Freeform = 1,
}
```

### New Type Android.Hardware.Camera2.SensorInfoColorFilterArrangement

```
[Serializable]
public enum SensorInfoColorFilterArrangement {
	Bggr = 3,
	Gbrg = 2,
	Grbg = 1,
	Rgb = 4,
	Rggb = 0,
}
```

### New Type Android.Hardware.Camera2.SensorInfoTimestampSource

```
[Serializable]
public enum SensorInfoTimestampSource {
	Realtime = 1,
	Unknown = 0,
}
```

### New Type Android.Hardware.Camera2.SensorReferenceIlluminant1

```
[Serializable]
public enum SensorReferenceIlluminant1 {
	CloudyWeather = 10,
	CoolWhiteFluorescent = 14,
	D50 = 23,
	D55 = 20,
	D65 = 21,
	D75 = 22,
	Daylight = 1,
	DaylightFluorescent = 12,
	DayWhiteFluorescent = 13,
	FineWeather = 9,
	Flash = 4,
	Fluorescent = 2,
	IsoStudioTungsten = 24,
	Shade = 11,
	StandardA = 17,
	StandardB = 18,
	StandardC = 19,
	Tungsten = 3,
	WhiteFluorescent = 15,
}
```

### New Type Android.Hardware.Camera2.SensorTestPatternMode

```
[Serializable]
public enum SensorTestPatternMode {
	ColorBars = 2,
	ColorBarsFadeToGray = 3,
	Custom1 = 256,
	Off = 0,
	Pn9 = 4,
	SolidColor = 1,
}
```

### New Type Android.Hardware.Camera2.ShadingMode

```
[Serializable]
public enum ShadingMode {
	Fast = 1,
	HighQuality = 2,
	Off = 0,
}
```

### New Type Android.Hardware.Camera2.StatisticsFaceDetectMode

```
[Serializable]
public enum StatisticsFaceDetectMode {
	Full = 2,
	Off = 0,
	Simple = 1,
}
```

### New Type Android.Hardware.Camera2.StatisticsLensShadingMapMode

```
[Serializable]
public enum StatisticsLensShadingMapMode {
	Off = 0,
	On = 1,
}
```

### New Type Android.Hardware.Camera2.StatisticsSceneFlicker

```
[Serializable]
public enum StatisticsSceneFlicker {
	None = 0,
	S50hz = 1,
	S60hz = 2,
}
```

### New Type Android.Hardware.Camera2.SyncMaxLatency

```
[Serializable]
public enum SyncMaxLatency {
	PerFrameControl = 0,
	Unknown = -1,
}
```

### New Type Android.Hardware.Camera2.TonemapMode

```
[Serializable]
public enum TonemapMode {
	ContrastCurve = 0,
	Fast = 1,
	HighQuality = 2,
}
```

### New Type Android.Hardware.Camera2.TotalCaptureResult

```
public sealed class TotalCaptureResult : Android.Hardware.Camera2.CaptureResult, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public System.Collections.Generic.IList<CaptureResult> PartialResults { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

## New Namespace Android.Hardware.Camera2.Params

### New Type Android.Hardware.Camera2.Params.BlackLevelPattern

```
public sealed class BlackLevelPattern : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const int Count;
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void CopyTo (int[] destination, int offset);
	public int GetOffsetForIndex (int column, int row);
}
```

### New Type Android.Hardware.Camera2.Params.ColorSpaceTransform

```
public sealed class ColorSpaceTransform : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public ColorSpaceTransform (Android.Util.Rational[] elements);
	public ColorSpaceTransform (int[] elements);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void CopyElements (Android.Util.Rational[] destination, int offset);
	public void CopyElements (int[] destination, int offset);
	public Android.Util.Rational GetElement (int column, int row);
}
```

### New Type Android.Hardware.Camera2.Params.Face

```
public sealed class Face : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const int IdUnsupported;
	public static const int ScoreMax;
	public static const int ScoreMin;
	// properties
	public Android.Graphics.Rect Bounds { get; }
	public int Id { get; }
	public Android.Graphics.Point LeftEyePosition { get; }
	public Android.Graphics.Point MouthPosition { get; }
	public Android.Graphics.Point RightEyePosition { get; }
	public int Score { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Android.Hardware.Camera2.Params.LensShadingMap

```
public sealed class LensShadingMap : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const float MinimumGainFactor;
	// properties
	public int ColumnCount { get; }
	public int GainFactorCount { get; }
	public int RowCount { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void CopyGainFactors (float[] destination, int offset);
	public float GetGainFactor (int colorChannel, int column, int row);
	public RggbChannelVector GetGainFactorVector (int column, int row);
}
```

### New Type Android.Hardware.Camera2.Params.MeteringRectangle

```
public sealed class MeteringRectangle : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public MeteringRectangle (Android.Graphics.Rect rect, int meteringWeight);
	public MeteringRectangle (Android.Graphics.Point xy, Android.Util.Size dimensions, int meteringWeight);
	public MeteringRectangle (int x, int y, int width, int height, int meteringWeight);
	// fields
	public static const int MeteringWeightDontCare;
	public static const int MeteringWeightMax;
	public static const int MeteringWeightMin;
	// properties
	public int Height { get; }
	public int MeteringWeight { get; }
	public Android.Graphics.Rect Rect { get; }
	public Android.Util.Size Size { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public Android.Graphics.Point UpperLeftPoint { get; }
	public int Width { get; }
	// methods
	public bool Equals (MeteringRectangle other);
	public int GetX ();
	public int GetY ();
}
```

### New Type Android.Hardware.Camera2.Params.RggbChannelVector

```
public sealed class RggbChannelVector : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public RggbChannelVector (float red, float greenEven, float greenOdd, float blue);
	// fields
	public static const int Count;
	// properties
	public float Blue { get; }
	public float GreenEven { get; }
	public float GreenOdd { get; }
	public float Red { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void CopyTo (float[] destination, int offset);
	public float GetComponent (int colorChannel);
}
```

### New Type Android.Hardware.Camera2.Params.StreamConfigurationMap

```
public sealed class StreamConfigurationMap : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public Android.Util.Range[] GetHighSpeedVideoFpsRanges ();
	public Android.Util.Range[] GetHighSpeedVideoFpsRangesFor (Android.Util.Size size);
	public Android.Util.Size[] GetHighSpeedVideoSizes ();
	public Android.Util.Size[] GetHighSpeedVideoSizesFor (Android.Util.Range fpsRange);
	public int[] GetOutputFormats ();
	public long GetOutputMinFrameDuration (Java.Lang.Class klass, Android.Util.Size size);
	public long GetOutputMinFrameDuration (int format, Android.Util.Size size);
	public Android.Util.Size[] GetOutputSizes (int format);
	public Android.Util.Size[] GetOutputSizes (Java.Lang.Class klass);
	public long GetOutputStallDuration (Java.Lang.Class klass, Android.Util.Size size);
	public long GetOutputStallDuration (int format, Android.Util.Size size);
	public bool IsOutputSupportedFor (Android.Views.Surface surface);
	public bool IsOutputSupportedFor (int format);
	public static bool IsOutputSupportedFor (Java.Lang.Class klass);
}
```

### New Type Android.Hardware.Camera2.Params.TonemapCurve

```
public sealed class TonemapCurve : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public TonemapCurve (float[] red, float[] green, float[] blue);
	// fields
	public static const float LevelBlack;
	public static const float LevelWhite;
	public static const int PointSize;
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public void CopyColorCurve (int colorChannel, float[] destination, int offset);
	public Android.Graphics.PointF GetPoint (int colorChannel, int index);
	public int GetPointCount (int colorChannel);
}
```

### New Type Android.Hardware.Camera2.Params.TonemapCurveChannel

```
[Serializable]
public enum TonemapCurveChannel {
	Blue = 2,
	Green = 1,
	Red = 0,
}
```

## New Namespace Android.Media.Projection

### New Type Android.Media.Projection.MediaProjection

```
public sealed class MediaProjection : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public Android.Hardware.Display.VirtualDisplay CreateVirtualDisplay (string name, int width, int height, int dpi, Android.Views.DisplayFlags flags, Android.Views.Surface surface, Android.Hardware.Display.VirtualDisplay.Callback callback, Android.OS.Handler handler);
	public void RegisterCallback (MediaProjection.Callback callback, Android.OS.Handler handler);
	public void Stop ();
	public void UnregisterCallback (MediaProjection.Callback callback);

	// inner types
	public abstract class Callback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MediaProjection (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public MediaProjection ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnStop ();
	}
}
```

### New Type Android.Media.Projection.MediaProjectionManager

```
public sealed class MediaProjectionManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public Android.Content.Intent CreateScreenCaptureIntent ();
	public MediaProjection GetMediaProjection (int resultCode, Android.Content.Intent resultData);
}
```

## New Namespace Android.Media.TV

### New Type Android.Media.TV.TvContentRating

```
public sealed class TvContentRating : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public string Domain { get; }
	public string MainRating { get; }
	public string RatingSystem { get; }
	public System.Collections.Generic.IList<string> SubRatings { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static TvContentRating CreateRating (string domain, string ratingSystem, string rating, string[] subRatings);
	public string FlattenToString ();
	public static TvContentRating UnflattenFromString (string ratingString);
}
```

### New Type Android.Media.TV.TvContract

```
public sealed class TvContract : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const string Authority = "android.media.tv";
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static Android.Net.Uri BuildChannelLogoUri (Android.Net.Uri channelUri);
	public static Android.Net.Uri BuildChannelLogoUri (long channelId);
	public static Android.Net.Uri BuildChannelsUriForInput (string inputId);
	public static Android.Net.Uri BuildChannelUri (long channelId);
	public static Android.Net.Uri BuildChannelUriForPassthroughInput (string inputId);
	public static string BuildInputId (Android.Content.ComponentName name);
	public static Android.Net.Uri BuildProgramsUriForChannel (Android.Net.Uri channelUri);
	public static Android.Net.Uri BuildProgramsUriForChannel (Android.Net.Uri channelUri, long startTime, long endTime);
	public static Android.Net.Uri BuildProgramsUriForChannel (long channelId);
	public static Android.Net.Uri BuildProgramsUriForChannel (long channelId, long startTime, long endTime);
	public static Android.Net.Uri BuildProgramUri (long programId);

	// inner types
	public abstract class BaseTvColumns {
		// fields
		public static const string ColumnPackageName = "package_name";
		public static const string Count = "_count";
		public static const string Id = "_id";
	}
	public abstract class BaseTvColumnsConsts : Android.Media.TV.TvContract+BaseTvColumns {
	}
	public sealed class Channels : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// fields
		public static const string ColumnDescription = "description";
		public static const string ColumnDisplayName = "display_name";
		public static const string ColumnDisplayNumber = "display_number";
		public static const string ColumnInputId = "input_id";
		public static const string ColumnInternalProviderData = "internal_provider_data";
		public static const string ColumnNetworkAffiliation = "network_affiliation";
		public static const string ColumnOriginalNetworkId = "original_network_id";
		public static const string ColumnSearchable = "searchable";
		public static const string ColumnServiceId = "service_id";
		public static const string ColumnServiceType = "service_type";
		public static const string ColumnTransportStreamId = "transport_stream_id";
		public static const string ColumnType = "type";
		public static const string ColumnVersionNumber = "version_number";
		public static const string ColumnVideoFormat = "video_format";
		public static const string ContentItemType = "vnd.android.cursor.item/channel";
		public static const string ContentType = "vnd.android.cursor.dir/channel";
		public static const string ServiceTypeAudio = "SERVICE_TYPE_AUDIO";
		public static const string ServiceTypeAudioVideo = "SERVICE_TYPE_AUDIO_VIDEO";
		public static const string ServiceTypeOther = "SERVICE_TYPE_OTHER";
		public static const string Type1seg = "TYPE_1SEG";
		public static const string TypeAtscC = "TYPE_ATSC_C";
		public static const string TypeAtscMH = "TYPE_ATSC_M_H";
		public static const string TypeAtscT = "TYPE_ATSC_T";
		public static const string TypeCmmb = "TYPE_CMMB";
		public static const string TypeDtmb = "TYPE_DTMB";
		public static const string TypeDvbC = "TYPE_DVB_C";
		public static const string TypeDvbC2 = "TYPE_DVB_C2";
		public static const string TypeDvbH = "TYPE_DVB_H";
		public static const string TypeDvbS = "TYPE_DVB_S";
		public static const string TypeDvbS2 = "TYPE_DVB_S2";
		public static const string TypeDvbSh = "TYPE_DVB_SH";
		public static const string TypeDvbT = "TYPE_DVB_T";
		public static const string TypeDvbT2 = "TYPE_DVB_T2";
		public static const string TypeIsdbC = "TYPE_ISDB_C";
		public static const string TypeIsdbS = "TYPE_ISDB_S";
		public static const string TypeIsdbT = "TYPE_ISDB_T";
		public static const string TypeIsdbTb = "TYPE_ISDB_TB";
		public static const string TypeNtsc = "TYPE_NTSC";
		public static const string TypeOther = "TYPE_OTHER";
		public static const string TypePal = "TYPE_PAL";
		public static const string TypeSDmb = "TYPE_S_DMB";
		public static const string TypeSecam = "TYPE_SECAM";
		public static const string TypeTDmb = "TYPE_T_DMB";
		public static const string VideoFormat1080i = "VIDEO_FORMAT_1080I";
		public static const string VideoFormat1080p = "VIDEO_FORMAT_1080P";
		public static const string VideoFormat2160p = "VIDEO_FORMAT_2160P";
		public static const string VideoFormat240p = "VIDEO_FORMAT_240P";
		public static const string VideoFormat360p = "VIDEO_FORMAT_360P";
		public static const string VideoFormat4320p = "VIDEO_FORMAT_4320P";
		public static const string VideoFormat480i = "VIDEO_FORMAT_480I";
		public static const string VideoFormat480p = "VIDEO_FORMAT_480P";
		public static const string VideoFormat576i = "VIDEO_FORMAT_576I";
		public static const string VideoFormat576p = "VIDEO_FORMAT_576P";
		public static const string VideoFormat720p = "VIDEO_FORMAT_720P";
		public static const string VideoResolutionEd = "VIDEO_RESOLUTION_ED";
		public static const string VideoResolutionFhd = "VIDEO_RESOLUTION_FHD";
		public static const string VideoResolutionHd = "VIDEO_RESOLUTION_HD";
		public static const string VideoResolutionSd = "VIDEO_RESOLUTION_SD";
		public static const string VideoResolutionUhd = "VIDEO_RESOLUTION_UHD";
		// properties
		public static Android.Net.Uri ContentUri { get; set; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public static string GetVideoResolution (string videoFormat);

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const string ColumnPackageName = "package_name";
			public static const string Count = "_count";
			public static const string Id = "_id";
		}
		public sealed class Logo : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
			// fields
			public static const string ContentDirectory = "logo";
			// properties
			protected override System.IntPtr ThresholdClass { get; }
			protected override System.Type ThresholdType { get; }
		}
	}
	public sealed class Programs : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// fields
		public static const string ColumnAudioLanguage = "audio_language";
		public static const string ColumnBroadcastGenre = "broadcast_genre";
		public static const string ColumnCanonicalGenre = "canonical_genre";
		public static const string ColumnChannelId = "channel_id";
		public static const string ColumnContentRating = "content_rating";
		public static const string ColumnEndTimeUtcMillis = "end_time_utc_millis";
		public static const string ColumnEpisodeNumber = "episode_number";
		public static const string ColumnEpisodeTitle = "episode_title";
		public static const string ColumnInternalProviderData = "internal_provider_data";
		public static const string ColumnLongDescription = "long_description";
		public static const string ColumnPosterArtUri = "poster_art_uri";
		public static const string ColumnSeasonNumber = "season_number";
		public static const string ColumnShortDescription = "short_description";
		public static const string ColumnStartTimeUtcMillis = "start_time_utc_millis";
		public static const string ColumnThumbnailUri = "thumbnail_uri";
		public static const string ColumnTitle = "title";
		public static const string ColumnVersionNumber = "version_number";
		public static const string ColumnVideoHeight = "video_height";
		public static const string ColumnVideoWidth = "video_width";
		public static const string ContentItemType = "vnd.android.cursor.item/program";
		public static const string ContentType = "vnd.android.cursor.dir/program";
		// properties
		public static Android.Net.Uri ContentUri { get; set; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }

		// inner types
		public static class InterfaceConsts {
			// fields
			public static const string ColumnPackageName = "package_name";
			public static const string Count = "_count";
			public static const string Id = "_id";
		}
		public sealed class Genres : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
			// fields
			public static const string AnimalWildlife = "ANIMAL_WILDLIFE";
			public static const string Comedy = "COMEDY";
			public static const string Drama = "DRAMA";
			public static const string Education = "EDUCATION";
			public static const string FamilyKids = "FAMILY_KIDS";
			public static const string Gaming = "GAMING";
			public static const string Movies = "MOVIES";
			public static const string News = "NEWS";
			public static const string Shopping = "SHOPPING";
			public static const string Sports = "SPORTS";
			public static const string Travel = "TRAVEL";
			// properties
			protected override System.IntPtr ThresholdClass { get; }
			protected override System.Type ThresholdType { get; }
			// methods
			public static string[] Decode (string genres);
			public static string Encode (string[] genres);
		}
	}
}
```

### New Type Android.Media.TV.TvInputInfo

```
public sealed class TvInputInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields
	public static const string ExtraInputId = "android.media.tv.extra.INPUT_ID";
	// properties
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public string Id { get; }
	public bool IsPassthroughInput { get; }
	public string ParentId { get; }
	public Android.Content.PM.ServiceInfo ServiceInfo { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public TvInputType Type { get; }
	// methods
	public Android.Content.Intent CreateSettingsIntent ();
	public Android.Content.Intent CreateSetupIntent ();
	public virtual int DescribeContents ();
	public Android.Graphics.Drawables.Drawable LoadIcon (Android.Content.Context context);
	public string LoadLabel (Android.Content.Context context);
	public Java.Lang.ICharSequence LoadLabelFormatted (Android.Content.Context context);
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
```

### New Type Android.Media.TV.TvInputManager

```
public sealed class TvInputManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const string ActionBlockedRatingsChanged = "android.media.tv.action.BLOCKED_RATINGS_CHANGED";
	public static const string ActionParentalControlsEnabledChanged = "android.media.tv.action.PARENTAL_CONTROLS_ENABLED_CHANGED";
	public static const string ActionQueryContentRatingSystems = "android.media.tv.action.QUERY_CONTENT_RATING_SYSTEMS";
	public static const string MetaDataContentRatingSystems = "android.media.tv.metadata.CONTENT_RATING_SYSTEMS";
	// properties
	public bool IsParentalControlsEnabled { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public System.Collections.Generic.IList<TvInputInfo> TvInputList { get; }
	// methods
	public TvInputState GetInputState (string inputId);
	public TvInputInfo GetTvInputInfo (string inputId);
	public bool IsRatingBlocked (TvContentRating rating);
	public void RegisterCallback (TvInputManager.TvInputCallback callback, Android.OS.Handler handler);
	public void UnregisterCallback (TvInputManager.TvInputCallback callback);

	// inner types
	public abstract class TvInputCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TvInputManager (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TvInputManager ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnInputAdded (string inputId);
		public virtual void OnInputRemoved (string inputId);
		public virtual void OnInputStateChanged (string inputId, TvInputState state);
	}
}
```

### New Type Android.Media.TV.TvInputService

```
public abstract class TvInputService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected TvInputService (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TvInputService ();
	// fields
	public static const string ServiceInterface = "android.media.tv.TvInputService";
	public static const string ServiceMetaData = "android.media.tv.input";
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual TvInputService.Session OnCreateSession (string inputId);

	// inner types
	public abstract class HardwareSession : Android.Media.TV.TvInputService+Session, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		protected TvInputService (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TvInputService (Android.Content.Context context);
		// properties
		public virtual string HardwareInputId { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnHardwareVideoAvailable ();
		public virtual void OnHardwareVideoUnavailable (VideoUnavailableReason reason);
		public override bool OnSetSurface (Android.Views.Surface surface);
	}
	public abstract class Session : Java.Lang.Object, Android.Runtime.IJavaObject, System.IDisposable {
		// constructors
		protected TvInputService (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TvInputService (Android.Content.Context context);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void NotifyChannelRetuned (Android.Net.Uri channelUri);
		public virtual void NotifyContentAllowed ();
		public virtual void NotifyContentBlocked (TvContentRating rating);
		public virtual void NotifyTracksChanged (System.Collections.Generic.IList<TvTrackInfo> tracks);
		public virtual void NotifyTrackSelected (TvTrackInfoType type, string trackId);
		public virtual void NotifyVideoAvailable ();
		public virtual void NotifyVideoUnavailable (VideoUnavailableReason reason);
		public virtual Android.Views.View OnCreateOverlayView ();
		public virtual bool OnGenericMotionEvent (Android.Views.MotionEvent e);
		public virtual bool OnKeyDown (Android.Views.Keycode keyCode, Android.Views.KeyEvent e);
		public virtual bool OnKeyLongPress (Android.Views.Keycode keyCode, Android.Views.KeyEvent e);
		public virtual bool OnKeyMultiple (Android.Views.Keycode keyCode, int count, Android.Views.KeyEvent e);
		public virtual bool OnKeyUp (Android.Views.Keycode keyCode, Android.Views.KeyEvent e);
		public virtual void OnRelease ();
		public virtual bool OnSelectTrack (TvTrackInfoType type, string trackId);
		public virtual void OnSetCaptionEnabled (bool enabled);
		public virtual void OnSetStreamVolume (float volume);
		public virtual bool OnSetSurface (Android.Views.Surface surface);
		public virtual void OnSurfaceChanged (Android.Graphics.Format format, int width, int height);
		public virtual bool OnTouchEvent (Android.Views.MotionEvent e);
		public virtual bool OnTrackballEvent (Android.Views.MotionEvent e);
		public virtual bool OnTune (Android.Net.Uri channelUri);
		public virtual void OnUnblockContent (TvContentRating unblockedRating);
		public virtual void SetOverlayViewEnabled (bool enable);
	}
}
```

### New Type Android.Media.TV.TvInputState

```
[Serializable]
public enum TvInputState {
	Connected = 0,
	ConnectedStandby = 1,
	Disconnected = 2,
}
```

### New Type Android.Media.TV.TvInputType

```
[Serializable]
public enum TvInputType {
	Component = 1004,
	Composite = 1001,
	DisplayPort = 1008,
	Dvi = 1006,
	Hdmi = 1007,
	Other = 1000,
	Scart = 1003,
	Svideo = 1002,
	Tuner = 0,
	Vga = 1005,
}
```

### New Type Android.Media.TV.TvTrackInfo

```
public sealed class TvTrackInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public int AudioChannelCount { get; }
	public int AudioSampleRate { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public Android.OS.Bundle Extra { get; }
	public string Id { get; }
	public string Language { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public TvTrackInfoType Type { get; }
	public float VideoFrameRate { get; }
	public int VideoHeight { get; }
	public int VideoWidth { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete ("This constant will be removed in the future version. Use Android.OS.ParcelableWriteFlags enum directly instead of this field.")]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
	public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public TvTrackInfo (TvTrackInfoType type, string id);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public TvTrackInfo Build ();
		public TvTrackInfo.Builder SetAudioChannelCount (int audioChannelCount);
		public TvTrackInfo.Builder SetAudioSampleRate (int audioSampleRate);
		public TvTrackInfo.Builder SetExtra (Android.OS.Bundle extra);
		public TvTrackInfo.Builder SetLanguage (string language);
		public TvTrackInfo.Builder SetVideoFrameRate (float videoFrameRate);
		public TvTrackInfo.Builder SetVideoHeight (int videoHeight);
		public TvTrackInfo.Builder SetVideoWidth (int videoWidth);
	}
}
```

### New Type Android.Media.TV.TvTrackInfoType

```
[Serializable]
public enum TvTrackInfoType {
	Audio = 0,
	Subtitle = 2,
	Video = 1,
}
```

### New Type Android.Media.TV.TvView

```
public class TvView : Android.Views.ViewGroup, Android.Views.IViewManager, Android.Views.IViewParent, Android.Runtime.IJavaObject, System.IDisposable, Android.Views.Accessibility.IAccessibilityEventSource {
	// constructors
	protected TvView (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TvView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public TvView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
	public TvView (Android.Content.Context context);
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// events
	public event System.EventHandler<TvView.UnhandledInputEventEventArgs> UnhandledInputEvent;
	// methods
	public virtual bool DispatchUnhandledInputEvent (Android.Views.InputEvent e);
	public virtual string GetSelectedTrack (TvTrackInfoType type);
	public virtual System.Collections.Generic.IList<TvTrackInfo> GetTracks (TvTrackInfoType type);
	protected override void OnLayout (bool changed, int left, int top, int right, int bottom);
	public virtual bool OnUnhandledInputEvent (Android.Views.InputEvent e);
	public virtual void Reset ();
	public virtual void SelectTrack (TvTrackInfoType type, string trackId);
	public virtual void SetCallback (TvView.TvInputCallback callback);
	public virtual void SetCaptionEnabled (bool enabled);
	public virtual void SetOnUnhandledInputEventListener (TvView.IOnUnhandledInputEventListener listener);
	public virtual void SetStreamVolume (float volume);
	public virtual void Tune (string inputId, Android.Net.Uri channelUri);

	// inner types
	public interface IOnUnhandledInputEventListener : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual bool OnUnhandledInputEvent (Android.Views.InputEvent e);
	}
	public class UnhandledInputEventEventArgs : System.EventArgs {
		// constructors
		public TvView (bool handled, Android.Views.InputEvent e);
		// properties
		public Android.Views.InputEvent Event { get; }
		public bool Handled { get; set; }
	}
	public abstract class TvInputCallback : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected TvView (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public TvView ();
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnChannelRetuned (string inputId, Android.Net.Uri channelUri);
		public virtual void OnConnectionFailed (string inputId);
		public virtual void OnContentAllowed (string inputId);
		public virtual void OnContentBlocked (string inputId, TvContentRating rating);
		public virtual void OnDisconnected (string inputId);
		public virtual void OnTracksChanged (string inputId, System.Collections.Generic.IList<TvTrackInfo> tracks);
		public virtual void OnTrackSelected (string inputId, TvTrackInfoType type, string trackId);
		public virtual void OnVideoAvailable (string inputId);
		public virtual void OnVideoSizeChanged (string inputId, int width, int height);
		public virtual void OnVideoUnavailable (string inputId, VideoUnavailableReason reason);
	}
}
```

### New Type Android.Media.TV.VideoUnavailableReason

```
[Serializable]
public enum VideoUnavailableReason {
	Buffering = 3,
	Tuning = 1,
	Unknown = 0,
	WeakSignal = 2,
}
```

## New Namespace Android.Service.Media

### New Type Android.Service.Media.MediaBrowserService

```
public abstract class MediaBrowserService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected MediaBrowserService (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MediaBrowserService ();
	// fields
	public static const string ServiceInterface = "android.media.browse.MediaBrowserService";
	// properties
	public virtual Android.Media.Session.MediaSession.Token SessionToken { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Dump (Java.IO.FileDescriptor fd, Java.IO.PrintWriter writer, string[] args);
	public virtual void NotifyChildrenChanged (string parentId);
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual MediaBrowserService.BrowserRoot OnGetRoot (string clientPackageName, int clientUid, Android.OS.Bundle rootHints);
	public virtual void OnLoadChildren (string parentId, MediaBrowserService.Result result);

	// inner types
	public sealed class BrowserRoot : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public MediaBrowserService (string rootId, Android.OS.Bundle extras);
		// properties
		public Android.OS.Bundle Extras { get; }
		public string RootId { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
	public class Result : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected MediaBrowserService (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		// properties
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void Detach ();
		public virtual void SendResult (Java.Lang.Object result);
	}
}
```

## New Namespace Android.Service.Restrictions

### New Type Android.Service.Restrictions.RestrictionsReceiver

```
public abstract class RestrictionsReceiver : Android.Content.BroadcastReceiver, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected RestrictionsReceiver (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RestrictionsReceiver ();
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void OnReceive (Android.Content.Context context, Android.Content.Intent intent);
	public virtual void OnRequestPermission (Android.Content.Context context, string packageName, string requestType, string requestId, Android.OS.PersistableBundle request);
}
```

## New Namespace Android.Systems

### New Type Android.Systems.ErrnoException

```
public sealed class ErrnoException : Java.Lang.Exception, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	public ErrnoException (string functionName, int errno);
	public ErrnoException (string functionName, int errno, Java.Lang.Throwable cause);
	// properties
	public int Errno { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Android.Systems.Os

```
public sealed class Os : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static Java.IO.FileDescriptor Accept (Java.IO.FileDescriptor fd, Java.Net.InetSocketAddress peerAddress);
	public static bool Access (string path, int mode);
	public static void Bind (Java.IO.FileDescriptor fd, Java.Net.InetAddress address, int port);
	public static void Chmod (string path, int mode);
	public static void Chown (string path, int uid, int gid);
	public static void Close (Java.IO.FileDescriptor fd);
	public static void Connect (Java.IO.FileDescriptor fd, Java.Net.InetAddress address, int port);
	public static Java.IO.FileDescriptor Dup (Java.IO.FileDescriptor oldFd);
	public static Java.IO.FileDescriptor Dup2 (Java.IO.FileDescriptor oldFd, int newFd);
	public static string[] Environ ();
	public static void Execv (string filename, string[] argv);
	public static void Execve (string filename, string[] argv, string[] envp);
	public static void Fchmod (Java.IO.FileDescriptor fd, int mode);
	public static void Fchown (Java.IO.FileDescriptor fd, int uid, int gid);
	public static void Fdatasync (Java.IO.FileDescriptor fd);
	public static StructStat Fstat (Java.IO.FileDescriptor fd);
	public static StructStatVfs Fstatvfs (Java.IO.FileDescriptor fd);
	public static void Fsync (Java.IO.FileDescriptor fd);
	public static void Ftruncate (Java.IO.FileDescriptor fd, long length);
	public static string Gai_strerror (int error);
	public static int Getegid ();
	public static string Getenv (string name);
	public static int Geteuid ();
	public static int Getgid ();
	public static Java.Net.SocketAddress Getpeername (Java.IO.FileDescriptor fd);
	public static int Getpid ();
	public static int Getppid ();
	public static Java.Net.SocketAddress Getsockname (Java.IO.FileDescriptor fd);
	public static int Gettid ();
	public static int Getuid ();
	public static string If_indextoname (int index);
	public static Java.Net.InetAddress Inet_pton (int family, string address);
	public static bool Isatty (Java.IO.FileDescriptor fd);
	public static void Kill (int pid, int signal);
	public static void Lchown (string path, int uid, int gid);
	public static void Link (string oldPath, string newPath);
	public static void Listen (Java.IO.FileDescriptor fd, int backlog);
	public static long Lseek (Java.IO.FileDescriptor fd, long offset, int whence);
	public static StructStat Lstat (string path);
	public static void Mincore (long address, long byteCount, byte[] vector);
	public static void Mkdir (string path, int mode);
	public static void Mkfifo (string path, int mode);
	public static void Mlock (long address, long byteCount);
	public static long Mmap (long address, long byteCount, int prot, int flags, Java.IO.FileDescriptor fd, long offset);
	public static void Msync (long address, long byteCount, int flags);
	public static void Munlock (long address, long byteCount);
	public static void Munmap (long address, long byteCount);
	public static Java.IO.FileDescriptor Open (string path, int flags, int mode);
	public static Java.IO.FileDescriptor[] Pipe ();
	public static int Poll (StructPollfd[] fds, int timeoutMs);
	public static void Posix_fallocate (Java.IO.FileDescriptor fd, long offset, long length);
	public static int Prctl (int option, long arg2, long arg3, long arg4, long arg5);
	public static int Pread (Java.IO.FileDescriptor fd, byte[] bytes, int byteOffset, int byteCount, long offset);
	public static int Pread (Java.IO.FileDescriptor fd, Java.Nio.ByteBuffer buffer, long offset);
	public static int Pwrite (Java.IO.FileDescriptor fd, byte[] bytes, int byteOffset, int byteCount, long offset);
	public static int Pwrite (Java.IO.FileDescriptor fd, Java.Nio.ByteBuffer buffer, long offset);
	public static int Read (Java.IO.FileDescriptor fd, Java.Nio.ByteBuffer buffer);
	public static int Read (Java.IO.FileDescriptor fd, byte[] bytes, int byteOffset, int byteCount);
	public static string Readlink (string path);
	public static int Readv (Java.IO.FileDescriptor fd, Java.Lang.Object[] buffers, int[] offsets, int[] byteCounts);
	public static int Recvfrom (Java.IO.FileDescriptor fd, Java.Nio.ByteBuffer buffer, int flags, Java.Net.InetSocketAddress srcAddress);
	public static int Recvfrom (Java.IO.FileDescriptor fd, byte[] bytes, int byteOffset, int byteCount, int flags, Java.Net.InetSocketAddress srcAddress);
	public static void Remove (string path);
	public static void Rename (string oldPath, string newPath);
	public static long Sendfile (Java.IO.FileDescriptor outFd, Java.IO.FileDescriptor inFd, Android.Util.MutableLong inOffset, long byteCount);
	public static int Sendto (Java.IO.FileDescriptor fd, byte[] bytes, int byteOffset, int byteCount, int flags, Java.Net.InetAddress inetAddress, int port);
	public static int Sendto (Java.IO.FileDescriptor fd, Java.Nio.ByteBuffer buffer, int flags, Java.Net.InetAddress inetAddress, int port);
	public static void Setegid (int egid);
	public static void Setenv (string name, string value, bool overwrite);
	public static void Seteuid (int euid);
	public static void Setgid (int gid);
	public static int Setsid ();
	public static void Setuid (int uid);
	public static void Shutdown (Java.IO.FileDescriptor fd, int how);
	public static Java.IO.FileDescriptor Socket (int domain, int type, int protocol);
	public static void Socketpair (int domain, int type, int protocol, Java.IO.FileDescriptor fd1, Java.IO.FileDescriptor fd2);
	public static StructStat Stat (string path);
	public static StructStatVfs Statvfs (string path);
	public static string Strerror (int errno);
	public static string Strsignal (int signal);
	public static void Symlink (string oldPath, string newPath);
	public static long Sysconf (int name);
	public static void Tcdrain (Java.IO.FileDescriptor fd);
	public static void Tcsendbreak (Java.IO.FileDescriptor fd, int duration);
	public static int Umask (int mask);
	public static StructUtsname Uname ();
	public static void Unsetenv (string name);
	public static int Waitpid (int pid, Android.Util.MutableInt status, int options);
	public static int Write (Java.IO.FileDescriptor fd, byte[] bytes, int byteOffset, int byteCount);
	public static int Write (Java.IO.FileDescriptor fd, Java.Nio.ByteBuffer buffer);
	public static int Writev (Java.IO.FileDescriptor fd, Java.Lang.Object[] buffers, int[] offsets, int[] byteCounts);
}
```

### New Type Android.Systems.OsConstants

```
public sealed class OsConstants : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
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
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public static int Wcontinued { get; set; }
	public static int Wexited { get; set; }
	public static int Wnohang { get; set; }
	public static int Wnowait { get; set; }
	public static int WOk { get; set; }
	public static int Wstopped { get; set; }
	public static int Wuntraced { get; set; }
	public static int XOk { get; set; }
	// methods
	public static string ErrnoName (int errno);
	public static string GaiName (int error);
	public static bool S_ISBLK (int mode);
	public static bool S_ISCHR (int mode);
	public static bool S_ISDIR (int mode);
	public static bool S_ISFIFO (int mode);
	public static bool S_ISLNK (int mode);
	public static bool S_ISREG (int mode);
	public static bool S_ISSOCK (int mode);
	public static bool WCOREDUMP (int status);
	public static int WEXITSTATUS (int status);
	public static bool WIFEXITED (int status);
	public static bool WIFSIGNALED (int status);
	public static bool WIFSTOPPED (int status);
	public static int WSTOPSIG (int status);
	public static int WTERMSIG (int status);
}
```

### New Type Android.Systems.StructPollfd

```
public sealed class StructPollfd : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public StructPollfd ();
	// properties
	public short Events { get; set; }
	public Java.IO.FileDescriptor Fd { get; set; }
	public short Revents { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public Java.Lang.Object UserData { get; set; }
}
```

### New Type Android.Systems.StructStat

```
public sealed class StructStat : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public StructStat (long st_dev, long st_ino, int st_mode, long st_nlink, int st_uid, int st_gid, long st_rdev, long st_size, long st_atime, long st_mtime, long st_ctime, long st_blksize, long st_blocks);
	// properties
	public long StAtime { get; set; }
	public long StBlksize { get; set; }
	public long StBlocks { get; set; }
	public long StCtime { get; set; }
	public long StDev { get; set; }
	public int StGid { get; set; }
	public long StIno { get; set; }
	public int StMode { get; set; }
	public long StMtime { get; set; }
	public long StNlink { get; set; }
	public long StRdev { get; set; }
	public long StSize { get; set; }
	public int StUid { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Android.Systems.StructStatVfs

```
public sealed class StructStatVfs : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public StructStatVfs (long f_bsize, long f_frsize, long f_blocks, long f_bfree, long f_bavail, long f_files, long f_ffree, long f_favail, long f_fsid, long f_flag, long f_namemax);
	// properties
	public long FBavail { get; set; }
	public long FBfree { get; set; }
	public long FBlocks { get; set; }
	public long FBsize { get; set; }
	public long FFavail { get; set; }
	public long FFfree { get; set; }
	public long FFiles { get; set; }
	public long FFlag { get; set; }
	public long FFrsize { get; set; }
	public long FFsid { get; set; }
	public long FNamemax { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Android.Systems.StructUtsname

```
public sealed class StructUtsname : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public StructUtsname (string sysname, string nodename, string release, string version, string machine);
	// properties
	public string Machine { get; set; }
	public string Nodename { get; set; }
	public string Release { get; set; }
	public string Sysname { get; set; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public string Version { get; set; }
}
```

## New Namespace Android.Telecom

### New Type Android.Telecom.Presentation

```
[Serializable]
public enum Presentation {
	Allowed = 1,
	Payphone = 4,
	Restricted = 2,
	Unknown = 3,
}
```

### New Type Android.Telecom.TelecomManager

```
public class TelecomManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected TelecomManager (System.IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// fields
	public static const string ActionShowCallSettings = "android.telecom.action.SHOW_CALL_SETTINGS";
	public static const char DtmfCharacterPause;
	public static const char DtmfCharacterWait;
	public static const string ExtraCallDisconnectCause = "android.telecom.extra.CALL_DISCONNECT_CAUSE";
	public static const string ExtraCallDisconnectMessage = "android.telecom.extra.CALL_DISCONNECT_MESSAGE";
	public static const string ExtraStartCallWithSpeakerphone = "android.telecom.extra.START_CALL_WITH_SPEAKERPHONE";
	public static const string GatewayOriginalAddress = "android.telecom.extra.GATEWAY_ORIGINAL_ADDRESS";
	public static const string GatewayProviderPackage = "android.telecom.extra.GATEWAY_PROVIDER_PACKAGE";
	// properties
	public virtual bool IsInCall { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void CancelMissedCallsNotification ();
	public virtual bool HandleMmi (string dialString);
	public virtual void ShowInCallScreen (bool showDialpad);
}
```
