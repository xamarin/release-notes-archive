---
id: A73A69C8-B3FC-4F04-BF89-C8BCB20746D2
---

## Namespace Android

### Type Changed: Android.Manifest

### Type Changed: Android.Manifest.Permission

Added field:

```
public static const string BodySensors = "android.permission.BODY_SENSORS";
```

### Type Changed: Android.Resource

### Type Changed: Android.Resource.Attribute

Added fields:

```
public static const int AllowEmbedded;
	public static const int WindowSwipeToDismiss;
```

### Type Changed: Android.Resource.Style

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const int TextAppearanceDeviceDefaultWidgetActionBarSubtitleInverse;

	[Obsolete ("deprecated")]
	public static const int TextAppearanceDeviceDefaultWidgetActionBarTitleInverse;

	[Obsolete ("deprecated")]
	public static const int TextAppearanceDeviceDefaultWidgetActionModeSubtitleInverse;

	[Obsolete ("deprecated")]
	public static const int TextAppearanceDeviceDefaultWidgetActionModeTitleInverse;

	[Obsolete ("deprecated")]
	public static const int WidgetDeviceDefaultLightActionBarSolidInverse;

	[Obsolete ("deprecated")]
	public static const int WidgetDeviceDefaultLightActionBarTabBarInverse;

	[Obsolete ("deprecated")]
	public static const int WidgetDeviceDefaultLightActionBarTabTextInverse;

	[Obsolete ("deprecated")]
	public static const int WidgetDeviceDefaultLightActionBarTabViewInverse;

	[Obsolete ("deprecated")]
	public static const int WidgetDeviceDefaultLightActionModeInverse;
```

## Namespace Android.App

### Type Changed: Android.App.ActivityAttribute

Added property:

```
public bool AllowEmbedded { get; set; }
```

### Type Changed: Android.App.FragmentBreadCrumbs

Removed constructor:

```
public FragmentBreadCrumbs (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public FragmentBreadCrumbs (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.App.Notification

Added properties:

```
public virtual string Group { get; }
	public virtual string SortKey { get; }
```

### Type Changed: Android.App.Notification.Action

Added property:

```
public virtual Android.OS.Bundle Extras { get; }
```

Added method:

```
public virtual RemoteInput[] GetRemoteInputs ();
```

### New Type Android.App.Builder

```
public sealed class Builder : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public Notification (int icon, Java.Lang.ICharSequence title, PendingIntent intent);
	public Notification (int icon, string title, PendingIntent intent);
	public Notification (Notification.Action action);
	// properties
	public Android.OS.Bundle Extras { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public Notification.Action.Builder AddExtras (Android.OS.Bundle extras);
	public Notification.Action.Builder AddRemoteInput (RemoteInput remoteInput);
	public Notification.Action Build ();
	public Notification.Action.Builder Extend (Notification.Action.IExtender extender);
}
```

### New Type Android.App.IExtender

```
public interface IExtender : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual Notification.Action.Builder Extend (Notification.Action.Builder builder);
}
```

### New Type Android.App.WearableExtender

```
public sealed class WearableExtender : Java.Lang.Object, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public Notification ();
	public Notification (Notification.Action action);
	// properties
	public bool IsAvailableOffline { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public Notification.Action.WearableExtender Clone ();
	public virtual Notification.Action.Builder Extend (Notification.Action.Builder builder);
	public Notification.Action.WearableExtender SetAvailableOffline (bool availableOffline);
}
```

### Type Changed: Android.App.Notification.Builder

Added property:

```
public virtual Android.OS.Bundle Extras { get; }
```

Removed method:

```
public virtual Notification.Builder SetExtras (Android.OS.Bundle bag);
```

Added methods:

```
public virtual Notification.Builder AddAction (Notification.Action action);
	public virtual Notification.Builder AddExtras (Android.OS.Bundle extras);
	public virtual Notification.Builder Extend (Notification.IExtender extender);
	public virtual Notification.Builder SetExtras (Android.OS.Bundle extras);
	public virtual Notification.Builder SetGroup (string groupKey);
	public virtual Notification.Builder SetGroupSummary (bool isGroupSummary);
	public virtual Notification.Builder SetLocalOnly (bool localOnly);
	public virtual Notification.Builder SetSortKey (string sortKey);
```

### New Type Android.App.IExtender

```
public interface IExtender : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual Notification.Builder Extend (Notification.Builder builder);
}
```

### New Type Android.App.WearableExtender

```
public sealed class WearableExtender : Java.Lang.Object, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public Notification ();
	public Notification (Notification notif);
	// fields
	public static const int UnsetActionIndex;
	// properties
	public System.Collections.Generic.IList<Notification.Action> Actions { get; }
	public Android.Graphics.Bitmap Background { get; }
	public int ContentAction { get; }
	public int ContentIcon { get; }
	public Android.Views.GravityFlags ContentIconGravity { get; }
	public bool ContentIntentAvailableOffline { get; }
	public int CustomContentHeight { get; }
	public WearableSizePreset CustomSizePreset { get; }
	public PendingIntent DisplayIntent { get; }
	public Android.Views.GravityFlags Gravity { get; }
	public bool HintHideIcon { get; }
	public bool HintShowBackgroundOnly { get; }
	public System.Collections.Generic.IList<Notification> Pages { get; }
	public bool StartScrollBottom { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public Notification.WearableExtender AddAction (Notification.Action action);
	public Notification.WearableExtender AddActions (System.Collections.Generic.IList<Notification.Action> actions);
	public Notification.WearableExtender AddPage (Notification page);
	public Notification.WearableExtender AddPages (System.Collections.Generic.IList<Notification> pages);
	public Notification.WearableExtender ClearActions ();
	public Notification.WearableExtender ClearPages ();
	public Notification.WearableExtender Clone ();
	public virtual Notification.Builder Extend (Notification.Builder builder);
	public Notification.WearableExtender SetBackground (Android.Graphics.Bitmap background);
	public Notification.WearableExtender SetContentAction (int actionIndex);
	public Notification.WearableExtender SetContentIcon (int icon);
	public Notification.WearableExtender SetContentIconGravity (Android.Views.GravityFlags contentIconGravity);
	public Notification.WearableExtender SetContentIntentAvailableOffline (bool contentIntentAvailableOffline);
	public Notification.WearableExtender SetCustomContentHeight (int height);
	public Notification.WearableExtender SetCustomSizePreset (WearableSizePreset sizePreset);
	public Notification.WearableExtender SetDisplayIntent (PendingIntent intent);
	public Notification.WearableExtender SetGravity (Android.Views.GravityFlags gravity);
	public Notification.WearableExtender SetHintHideIcon (bool hintHideIcon);
	public Notification.WearableExtender SetHintShowBackgroundOnly (bool hintShowBackgroundOnly);
	public Notification.WearableExtender SetStartScrollBottom (bool startScrollBottom);
}
```

### Type Changed: Android.App.NotificationFlags

Added values:

```
GroupSummary = 512,
	LocalOnly = 256,
```

### New Type Android.App.RemoteInput

```
public sealed class RemoteInput : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// fields
	public static const string ExtraResultsData = "android.remoteinput.resultsData";
	public static const string ResultsClipLabel = "android.remoteinput.results";
	// properties
	public bool AllowFreeFormInput { get; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public Android.OS.Bundle Extras { get; }
	public string Label { get; }
	public Java.Lang.ICharSequence LabelFormatted { get; }
	public string ResultKey { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static void AddResultsToIntent (RemoteInput[] remoteInputs, Android.Content.Intent intent, Android.OS.Bundle results);
	public virtual int DescribeContents ();
	public string[] GetChoices ();
	public Java.Lang.ICharSequence[] GetChoicesFormatted ();
	public static Android.OS.Bundle GetResultsFromIntent (Android.Content.Intent intent);
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
		public RemoteInput (string resultKey);
		// properties
		public Android.OS.Bundle Extras { get; }
		protected override System.IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public RemoteInput.Builder AddExtras (Android.OS.Bundle extras);
		public RemoteInput Build ();
		public RemoteInput.Builder SetAllowFreeFormInput (bool allowFreeFormInput);
		public RemoteInput.Builder SetChoices (Java.Lang.ICharSequence[] choices);
		public RemoteInput.Builder SetChoices (string[] choices);
		public RemoteInput.Builder SetLabel (Java.Lang.ICharSequence label);
		public RemoteInput.Builder SetLabel (string label);
	}
}
```

### New Type Android.App.WearableSizePreset

```
[Serializable]
public enum WearableSizePreset {
	Default = 0,
	FullScreen = 5,
	Large = 4,
	Medium = 3,
	Small = 2,
	Xsmall = 1,
}
```

## Namespace Android.Content

### Type Changed: Android.Content.ContextWrapper

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public override Android.Graphics.Drawables.Drawable Wallpaper { get; }

	[Obsolete ("deprecated")]
	public override int WallpaperDesiredMinimumHeight { get; }

	[Obsolete ("deprecated")]
	public override int WallpaperDesiredMinimumWidth { get; }
```

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ComponentInfo

Added property:

```
public int BannerResource { get; }
```

### Type Changed: Android.Content.PM.PackageItemInfo

Added property:

```
public int Banner { get; set; }
```

Added method:

```
public virtual Android.Graphics.Drawables.Drawable LoadBanner (PackageManager pm);
```

### Type Changed: Android.Content.PM.PackageManager

Added fields:

```
public static const string FeatureBackup = "android.software.backup";
	public static const string FeatureCameraExternal = "android.hardware.camera.external";
	public static const string FeaturePrinting = "android.software.print";
	public static const string FeatureSensorHeartRate = "android.hardware.sensor.heartrate";
	public static const string FeatureWatch = "android.hardware.type.watch";
	public static const string FeatureWebview = "android.software.webview";
```

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const string FeatureTelevision = "android.hardware.type.television";
```

Added methods:

```
public virtual Android.Graphics.Drawables.Drawable GetActivityBanner (Android.Content.ComponentName activityName);
	public virtual Android.Graphics.Drawables.Drawable GetActivityBanner (Android.Content.Intent intent);
	public virtual Android.Graphics.Drawables.Drawable GetApplicationBanner (ApplicationInfo info);
	public virtual Android.Graphics.Drawables.Drawable GetApplicationBanner (string packageName);
```

## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.Configuration

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Content.Res.UiMode enum directly instead of this field.")]
	public static const UiMode UiModeTypeWatch;
```

### Type Changed: Android.Content.Res.Resources

### Type Changed: Android.Content.Res.Resources.Theme

Removed method:

```
public void ApplyStyle (int resid, bool force);
```

Added method:

```
public void ApplyStyle (int resId, bool force);
```

### Type Changed: Android.Content.Res.UiMode

Added value:

```
TypeWatch = 6,
```

## Namespace Android.Database.Sqlite

### Type Changed: Android.Database.Sqlite.SQLiteOpenHelper

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual SQLiteDatabase ReadableDatabase { get; }

	[Obsolete ("deprecated")]
	public virtual SQLiteDatabase WritableDatabase { get; }
```

## Namespace Android.Gestures

### Type Changed: Android.Gestures.GestureOverlayView

Removed constructor:

```
public GestureOverlayView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public GestureOverlayView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

## Namespace Android.Graphics

### Type Changed: Android.Graphics.Paint

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual Rasterizer Rasterizer { get; }
```

### Type Changed: Android.Graphics.PorterDuffColorFilter

Removed constructor:

```
public PorterDuffColorFilter (Color srcColor, PorterDuff.Mode mode);
```

Added constructor:

```
public PorterDuffColorFilter (Color color, PorterDuff.Mode mode);
```

### Type Changed: Android.Graphics.SurfaceTexture

Removed method:

```
public virtual void SetOnFrameAvailableListener (SurfaceTexture.IOnFrameAvailableListener l);
```

Added method:

```
public virtual void SetOnFrameAvailableListener (SurfaceTexture.IOnFrameAvailableListener listener);
```

## Namespace Android.Hardware

### Type Changed: Android.Hardware.Sensor

Added fields:

```
public static const string StringTypeAccelerometer = "android.sensor.accelerometer";
	public static const string StringTypeAmbientTemperature = "android.sensor.ambient_temperature";
	public static const string StringTypeGameRotationVector = "android.sensor.game_rotation_vector";
	public static const string StringTypeGeomagneticRotationVector = "android.sensor.geomagnetic_rotation_vector";
	public static const string StringTypeGravity = "android.sensor.gravity";
	public static const string StringTypeGyroscope = "android.sensor.gyroscope";
	public static const string StringTypeGyroscopeUncalibrated = "android.sensor.gyroscope_uncalibrated";
	public static const string StringTypeHeartRate = "android.sensor.heart_rate";
	public static const string StringTypeLight = "android.sensor.light";
	public static const string StringTypeLinearAcceleration = "android.sensor.linear_acceleration";
	public static const string StringTypeMagneticField = "android.sensor.magnetic_field";
	public static const string StringTypeMagneticFieldUncalibrated = "android.sensor.magnetic_field_uncalibrated";

	[Obsolete ("deprecated")]
	public static const string StringTypeOrientation = "android.sensor.orientation";
	public static const string StringTypePressure = "android.sensor.pressure";
	public static const string StringTypeProximity = "android.sensor.proximity";
	public static const string StringTypeRelativeHumidity = "android.sensor.relative_humidity";
	public static const string StringTypeRotationVector = "android.sensor.rotation_vector";
	public static const string StringTypeSignificantMotion = "android.sensor.significant_motion";
	public static const string StringTypeStepCounter = "android.sensor.step_counter";
	public static const string StringTypeStepDetector = "android.sensor.step_detector";

	[Obsolete ("deprecated")]
	public static const string StringTypeTemperature = "android.sensor.temperature";
```

Added property:

```
public virtual string StringType { get; }
```

### Type Changed: Android.Hardware.SensorStatus

Added value:

```
NoContact = -1,
```

### Type Changed: Android.Hardware.SensorType

Added value:

```
HeartRate = 21,
```

## Namespace Android.Hardware.Display

### Type Changed: Android.Hardware.Display.DisplayManager

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Display.VirtualDisplayFlags enum directly instead of this field.")]
	public static const VirtualDisplayFlags VirtualDisplayFlagOwnContentOnly;
```

### Type Changed: Android.Hardware.Display.VirtualDisplay

Added property:

```
public Android.Views.Surface Surface { get; set; }
```

### Type Changed: Android.Hardware.Display.VirtualDisplayFlags

Added value:

```
OwnContentOnly = 8,
```

## Namespace Android.InputMethodServices

### Type Changed: Android.InputMethodServices.ExtractEditText

Removed constructor:

```
public ExtractEditText (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ExtractEditText (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.InputMethodServices.KeyboardView

Removed constructor:

```
public KeyboardView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public KeyboardView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

## Namespace Android.Media

### Type Changed: Android.Media.AudioTrack

Removed method:

```
public virtual TrackStatus SetStereoVolume (float leftVolume, float rightVolume);
```

Added method:

```
public virtual TrackStatus SetStereoVolume (float leftGain, float rightGain);
```

## Namespace Android.Net

### Type Changed: Android.Net.ConnectivityManager

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual ConnectivityType NetworkPreference { get; set; }
```

## Namespace Android.Opengl

### Type Changed: Android.Opengl.GLES20

Removed methods:

```
public static void GlGetActiveAttrib (int program, int index, int bufsize, Java.Nio.IntBuffer length, Java.Nio.IntBuffer size, Java.Nio.IntBuffer type, sbyte name);
	public static void GlGetActiveUniform (int program, int index, int bufsize, Java.Nio.IntBuffer length, Java.Nio.IntBuffer size, Java.Nio.IntBuffer type, sbyte name);
	public static void GlGetShaderSource (int shader, int bufsize, Java.Nio.IntBuffer length, sbyte source);
```

Added methods:

```
public static void GlGetActiveAttrib (int p0, int p1, int p2, Java.Nio.IntBuffer p3, Java.Nio.IntBuffer p4, Java.Nio.IntBuffer p5, sbyte p6);
	public static void GlGetActiveUniform (int p0, int p1, int p2, Java.Nio.IntBuffer p3, Java.Nio.IntBuffer p4, Java.Nio.IntBuffer p5, sbyte p6);
	public static void GlGetShaderSource (int p0, int p1, Java.Nio.IntBuffer p2, sbyte p3);
```

## Namespace Android.OS

### Type Changed: Android.OS.Build

### Type Changed: Android.OS.Build.VERSION_CODES

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.OS.BuildVersionCodes enum directly instead of this field.")]
	public static const BuildVersionCodes KitkatWatch;
```

### Type Changed: Android.OS.BuildVersionCodes

Added value:

```
KitkatWatch = 20,
```

### Type Changed: Android.OS.Bundle

Removed methods:

```
public bool ContainsKey (string key);
	public Java.Lang.Object Get (string key);
	public double GetDouble (string key, double defaultValue);
	public double GetDouble (string key);
	public double[] GetDoubleArray (string key);
	public int GetInt (string key, int defaultValue);
	public int GetInt (string key);
	public int[] GetIntArray (string key);
	public long GetLong (string key);
	public long GetLong (string key, long defaultValue);
	public long[] GetLongArray (string key);
	public string GetString (string key);
	public string GetString (string key, string defaultValue);
	public string[] GetStringArray (string key);
	public void PutAll (Bundle map);
	public void PutDouble (string key, double value);
	public void PutDoubleArray (string key, double[] value);
	public void PutInt (string key, int value);
	public void PutIntArray (string key, int[] value);
	public void PutLong (string key, long value);
	public void PutLongArray (string key, long[] value);
	public void PutString (string key, string value);
	public void PutStringArray (string key, string[] value);
	public void Remove (string key);
```

Added methods:

```
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
	public void PutAll (Bundle bundle);
	public void PutDouble (string p0, double p1);
	public void PutDoubleArray (string p0, double[] p1);
	public void PutInt (string p0, int p1);
	public void PutIntArray (string p0, int[] p1);
	public void PutLong (string p0, long p1);
	public void PutLongArray (string p0, long[] p1);
	public void PutString (string p0, string p1);
	public void PutStringArray (string p0, string[] p1);
	public void Remove (string p0);
```

### Type Changed: Android.OS.Parcel

Removed method:

```
protected static Parcel Obtain (int obj);
```

Added method:

```
protected static Parcel Obtain (int p0);
```

### Type Changed: Android.OS.PowerManager

Added property:

```
public virtual bool IsInteractive { get; }
```

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual bool IsScreenOn { get; }
```

## Namespace Android.Preferences

### Type Changed: Android.Preferences.CheckBoxPreference

Removed constructor:

```
public CheckBoxPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public CheckBoxPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Preferences.DialogPreference

Removed constructor:

```
public DialogPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public DialogPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Preferences.EditTextPreference

Removed constructor:

```
public EditTextPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public EditTextPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Preferences.Preference

Removed constructor:

```
public Preference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public Preference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Preferences.PreferenceCategory

Removed constructor:

```
public PreferenceCategory (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public PreferenceCategory (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Preferences.PreferenceGroup

Removed constructor:

```
public PreferenceGroup (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public PreferenceGroup (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Preferences.RingtonePreference

Removed constructor:

```
public RingtonePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public RingtonePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Preferences.SwitchPreference

Removed constructor:

```
public SwitchPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public SwitchPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Preferences.TwoStatePreference

Removed constructor:

```
public TwoStatePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public TwoStatePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

## Namespace Android.Provider

### Type Changed: Android.Provider.Settings

### Type Changed: Android.Provider.Settings.Global

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const string InstallNonMarketApps = "install_non_market_apps";
```

## Namespace Android.Renderscripts

### Type Changed: Android.Renderscripts.Double2

Removed constructor:

```
public Double2 (double initX, double initY);
```

Added constructor:

```
public Double2 (double x, double y);
```

### Type Changed: Android.Renderscripts.Double3

Removed constructor:

```
public Double3 (double initX, double initY, double initZ);
```

Added constructor:

```
public Double3 (double x, double y, double z);
```

### Type Changed: Android.Renderscripts.Double4

Removed constructor:

```
public Double4 (double initX, double initY, double initZ, double initW);
```

Added constructor:

```
public Double4 (double x, double y, double z, double w);
```

### Type Changed: Android.Renderscripts.Float2

Removed constructor:

```
public Float2 (float initX, float initY);
```

Added constructor:

```
public Float2 (float x, float y);
```

### Type Changed: Android.Renderscripts.Float3

Removed constructor:

```
public Float3 (float initX, float initY, float initZ);
```

Added constructor:

```
public Float3 (float x, float y, float z);
```

### Type Changed: Android.Renderscripts.Float4

Removed constructor:

```
public Float4 (float initX, float initY, float initZ, float initW);
```

Added constructor:

```
public Float4 (float x, float y, float z, float w);
```

### Type Changed: Android.Renderscripts.Int2

Removed constructor:

```
public Int2 (int initX, int initY);
```

Added constructor:

```
public Int2 (int x, int y);
```

### Type Changed: Android.Renderscripts.Int3

Removed constructor:

```
public Int3 (int initX, int initY, int initZ);
```

Added constructor:

```
public Int3 (int x, int y, int z);
```

### Type Changed: Android.Renderscripts.Int4

Removed constructor:

```
public Int4 (int initX, int initY, int initZ, int initW);
```

Added constructor:

```
public Int4 (int x, int y, int z, int w);
```

### Type Changed: Android.Renderscripts.Long2

Removed constructor:

```
public Long2 (long initX, long initY);
```

Added constructor:

```
public Long2 (long x, long y);
```

### Type Changed: Android.Renderscripts.Long3

Removed constructor:

```
public Long3 (long initX, long initY, long initZ);
```

Added constructor:

```
public Long3 (long x, long y, long z);
```

### Type Changed: Android.Renderscripts.Long4

Removed constructor:

```
public Long4 (long initX, long initY, long initZ, long initW);
```

Added constructor:

```
public Long4 (long x, long y, long z, long w);
```

### Type Changed: Android.Renderscripts.Short2

Removed constructor:

```
public Short2 (short initX, short initY);
```

Added constructor:

```
public Short2 (short x, short y);
```

### Type Changed: Android.Renderscripts.Short3

Removed constructor:

```
public Short3 (short initX, short initY, short initZ);
```

Added constructor:

```
public Short3 (short x, short y, short z);
```

### Type Changed: Android.Renderscripts.Short4

Removed constructor:

```
public Short4 (short initX, short initY, short initZ, short initW);
```

Added constructor:

```
public Short4 (short x, short y, short z, short w);
```

### New Type Android.Renderscripts.ScriptIntrinsicResize

```
public sealed class ScriptIntrinsicResize : Android.Renderscripts.ScriptIntrinsic, System.IDisposable, Android.Runtime.IJavaObject {
	// properties
	public Script.FieldID FieldID_Input { get; }
	public Script.KernelID KernelID_bicubic { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static ScriptIntrinsicResize Create (RenderScript rs);
	public void ForEach_bicubic (Allocation aout);
	public void ForEach_bicubic (Allocation aout, Script.LaunchOptions opt);
	public void SetInput (Allocation ain);
}
```

## Namespace Android.Service.Notification

### Type Changed: Android.Service.Notification.StatusBarNotification

Removed constructor:

```
public StatusBarNotification (string pkg, string basePkg, int id, string tag, int uid, int initialPid, int score, Android.App.Notification notification, Android.OS.UserHandle user, long postTime);
```

Added constructor:

```
public StatusBarNotification (string pkg, string opPkg, int id, string tag, int uid, int initialPid, int score, Android.App.Notification notification, Android.OS.UserHandle user, long postTime);
```

Added property:

```
public virtual string Key { get; }
```

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual int UserId { get; }
```

## Namespace Android.Test.Mock

### Type Changed: Android.Test.Mock.MockContext

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public override Android.Graphics.Drawables.Drawable Wallpaper { get; }

	[Obsolete ("deprecated")]
	public override int WallpaperDesiredMinimumHeight { get; }

	[Obsolete ("deprecated")]
	public override int WallpaperDesiredMinimumWidth { get; }
```

### Type Changed: Android.Test.Mock.MockPackageManager

Added methods:

```
public override Android.Graphics.Drawables.Drawable GetActivityBanner (Android.Content.ComponentName activityName);
	public override Android.Graphics.Drawables.Drawable GetActivityBanner (Android.Content.Intent intent);
	public override Android.Graphics.Drawables.Drawable GetApplicationBanner (Android.Content.PM.ApplicationInfo info);
	public override Android.Graphics.Drawables.Drawable GetApplicationBanner (string packageName);
```

## Namespace Android.Util

### Type Changed: Android.Util.Patterns

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string TopLevelDomainStr = "((aero|arpa|asia|a[cdefgilmnoqrstuwxz])|(biz|b[abdefghijmnorstvwyz])|(cat|com|coop|c[acdfghiklmnoruvxyz])|d[ejkmoz]|(edu|e[cegrstu])|f[ijkmor]|(gov|g[abdefghilmnpqrstuwy])|h[kmnrtu]|(info|int|i[delmnoqrst])|(jobs|j[emop])|k[eghimnprwyz]|l[abcikrstuvy]|(mil|mobi|museum|m[acdeghklmnopqrstuvwxyz])|(name|net|n[acefgilopruz])|(org|om)|(pro|p[aefghklmnrstwy])|qa|r[eosuw]|s[abcdeghijklmnortuvyz]|(tel|travel|t[cdfghjklmnoprtvwz])|u[agksyz]|v[aceginu]|w[fs]|(xn\-\-0zwm56d|xn\-\-11b5bs3a9aj6g|xn\-\-80akhbyknj4f|xn\-\-9t4b11yi5a|xn\-\-deba0ad|xn\-\-g6w251d|xn\-\-hgbk6aj7f53bba|xn\-\-hlcj6aya9esc7a|xn\-\-jxalpdlp|xn\-\-kgbechtv|xn\-\-zckzah)|y[etu]|z[amw])";

	[Obsolete ("deprecated")]
	public static const string TopLevelDomainStrForWebUrl = "(?:(?:aero|arpa|asia|a[cdefgilmnoqrstuwxz])|(?:biz|b[abdefghijmnorstvwyz])|(?:cat|com|coop|c[acdfghiklmnoruvxyz])|d[ejkmoz]|(?:edu|e[cegrstu])|f[ijkmor]|(?:gov|g[abdefghilmnpqrstuwy])|h[kmnrtu]|(?:info|int|i[delmnoqrst])|(?:jobs|j[emop])|k[eghimnprwyz]|l[abcikrstuvy]|(?:mil|mobi|museum|m[acdeghklmnopqrstuvwxyz])|(?:name|net|n[acefgilopruz])|(?:org|om)|(?:pro|p[aefghklmnrstwy])|qa|r[eosuw]|s[abcdeghijklmnortuvyz]|(?:tel|travel|t[cdfghjklmnoprtvwz])|u[agksyz]|v[aceginu]|w[fs]|(?:xn\-\-0zwm56d|xn\-\-11b5bs3a9aj6g|xn\-\-80akhbyknj4f|xn\-\-9t4b11yi5a|xn\-\-deba0ad|xn\-\-g6w251d|xn\-\-hgbk6aj7f53bba|xn\-\-hlcj6aya9esc7a|xn\-\-jxalpdlp|xn\-\-kgbechtv|xn\-\-zckzah)|y[etu]|z[amw]))";
```

## Namespace Android.Views

### Type Changed: Android.Views.Display

Added field:

```
public static const int StateDozing;
```

Added property:

```
public virtual DisplayState State { get; }
```

### Type Changed: Android.Views.Keycode

Added values:

```
Sleep = 223,
	Wakeup = 224,
```

### Type Changed: Android.Views.SurfaceView

Removed constructor:

```
public SurfaceView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public SurfaceView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Views.TextureView

Removed constructor:

```
public TextureView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public TextureView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Views.View

Added property:

```
public View.ApplyWindowInsetsHandler ApplyWindowInsets { get; set; }
```

Added methods:

```
public virtual WindowInsets DispatchApplyWindowInsets (WindowInsets insets);
	public virtual WindowInsets OnApplyWindowInsets (WindowInsets insets);
	public virtual void RequestApplyInsets ();
	public virtual void SetOnApplyWindowInsetsListener (View.IOnApplyWindowInsetsListener listener);
```

### New Type Android.Views.IOnApplyWindowInsetsListener

```
public interface IOnApplyWindowInsetsListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual WindowInsets OnApplyWindowInsets (View v, WindowInsets insets);
}
```

### New Type Android.Views.ApplyWindowInsetsHandler

```
public sealed delegate ApplyWindowInsetsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public View (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (View v, WindowInsets insets, System.AsyncCallback callback, object object);
	public virtual WindowInsets EndInvoke (System.IAsyncResult result);
	public virtual WindowInsets Invoke (View v, WindowInsets insets);
}
```

### Type Changed: Android.Views.ViewConfiguration

Obsoleted property:

```
[Obsolete ("deprecated")]
	public static long GlobalActionKeyTimeout { get; }
```

### Type Changed: Android.Views.ViewGroup

Removed constructor:

```
public ViewGroup (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ViewGroup (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Views.ViewStub

Removed constructor:

```
public ViewStub (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ViewStub (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Views.WindowFeatures

Added value:

```
SwipeToDismiss = 11,
```

### New Type Android.Views.DisplayState

```
[Serializable]
public enum DisplayState {
	Off = 1,
	On = 2,
	Unknown = 0,
}
```

### New Type Android.Views.WindowInsets

```
public sealed class WindowInsets : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	public WindowInsets (WindowInsets src);
	// properties
	public bool HasInsets { get; }
	public bool HasSystemWindowInsets { get; }
	public bool IsRound { get; }
	public int SystemWindowInsetBottom { get; }
	public int SystemWindowInsetLeft { get; }
	public int SystemWindowInsetRight { get; }
	public int SystemWindowInsetTop { get; }
	protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public WindowInsets ConsumeSystemWindowInsets ();
	public WindowInsets ReplaceSystemWindowInsets (int left, int top, int right, int bottom);
}
```

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual Action Actions { get; }
```

## Namespace Android.Webkit

### Type Changed: Android.Webkit.WebView

Removed constructors:

```
public WebView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
	public WebView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle, bool privateBrowsing);
```

Added constructors:

```
public WebView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public WebView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, bool privateBrowsing);
```

## Namespace Android.Widget

### Type Changed: Android.Widget.AbsListView

Removed constructor:

```
public AbsListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public AbsListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.AbsoluteLayout

Removed constructor:

```
public AbsoluteLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public AbsoluteLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.AbsSeekBar

Removed constructor:

```
public AbsSeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public AbsSeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.AbsSpinner

Removed constructor:

```
public AbsSpinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public AbsSpinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.AdapterView

Removed constructor:

```
public AdapterView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public AdapterView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.AnalogClock

Removed constructor:

```
public AnalogClock (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public AnalogClock (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.AutoCompleteTextView

Removed constructor:

```
public AutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public AutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.Button

Removed constructor:

```
public Button (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public Button (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.CalendarView

Removed constructor:

```
public CalendarView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public CalendarView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.CheckBox

Removed constructor:

```
public CheckBox (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public CheckBox (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.CheckedTextView

Removed constructor:

```
public CheckedTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public CheckedTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.Chronometer

Removed constructor:

```
public Chronometer (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public Chronometer (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.CompoundButton

Removed constructor:

```
public CompoundButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public CompoundButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.DatePicker

Removed constructor:

```
public DatePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public DatePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.EditText

Removed constructor:

```
public EditText (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public EditText (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.ExpandableListView

Removed constructor:

```
public ExpandableListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ExpandableListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.FrameLayout

Removed constructor:

```
public FrameLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public FrameLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.Gallery

Removed constructor:

```
public Gallery (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public Gallery (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.GridLayout

Removed constructor:

```
public GridLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public GridLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.GridView

Removed constructor:

```
public GridView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public GridView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.HorizontalScrollView

Removed constructor:

```
public HorizontalScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public HorizontalScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.ImageButton

Removed constructor:

```
public ImageButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ImageButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.ImageView

Removed constructor:

```
public ImageView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ImageView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.LinearLayout

Removed constructor:

```
public LinearLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public LinearLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.ListView

Removed constructor:

```
public ListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ListView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

Removed method:

```
public virtual void SetSelectionFromTop (int position, int y);
```

Added method:

```
public virtual void SetSelectionFromTop (int p0, int p1);
```

### Type Changed: Android.Widget.MultiAutoCompleteTextView

Removed constructor:

```
public MultiAutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public MultiAutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.NumberPicker

Removed constructor:

```
public NumberPicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public NumberPicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.PopupWindow

Removed constructor:

```
public PopupWindow (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public PopupWindow (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.ProgressBar

Removed constructor:

```
public ProgressBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ProgressBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.QuickContactBadge

Removed constructor:

```
public QuickContactBadge (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public QuickContactBadge (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.RadioButton

Removed constructor:

```
public RadioButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public RadioButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.RatingBar

Removed constructor:

```
public RatingBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public RatingBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.RelativeLayout

Removed constructor:

```
public RelativeLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public RelativeLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.ScrollView

Removed constructor:

```
public ScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.SeekBar

Removed constructor:

```
public SeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public SeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.SlidingDrawer

Removed constructor:

```
public SlidingDrawer (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public SlidingDrawer (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.Space

Removed constructor:

```
public Space (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public Space (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.Spinner

Removed constructors:

```
public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
	public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle, SpinnerMode mode);
```

Added constructors:

```
public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
	public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr, SpinnerMode mode);
```

### Type Changed: Android.Widget.Switch

Removed constructor:

```
public Switch (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public Switch (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.TabWidget

Removed constructor:

```
public TabWidget (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public TabWidget (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.TextClock

Removed constructor:

```
public TextClock (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public TextClock (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.TextView

Removed constructor:

```
public TextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public TextView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.TimePicker

Removed constructor:

```
public TimePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public TimePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.ToggleButton

Removed constructor:

```
public ToggleButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ToggleButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.TwoLineListItem

Removed constructor:

```
public TwoLineListItem (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public TwoLineListItem (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.VideoView

Removed constructor:

```
public VideoView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public VideoView (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

### Type Changed: Android.Widget.ZoomButton

Removed constructor:

```
public ZoomButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

Added constructor:

```
public ZoomButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyleAttr);
```

## Namespace Java.Nio.Channels

### Type Changed: Java.Nio.Channels.FileChannel

Removed method:

```
public virtual FileChannel Position (long offset);
```

Added method:

```
public virtual FileChannel Position (long newPosition);
```

## Namespace Java.Sql

### Type Changed: Java.Sql.DriverManager

Obsoleted property:

```
[Obsolete ("deprecated")]
	public static Java.IO.PrintStream LogStream { get; set; }
```

### Type Changed: Java.Sql.ICallableStatement

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual Java.Math.BigDecimal GetBigDecimal (int parameterIndex, int scale);
```

### Type Changed: Java.Sql.IPreparedStatement

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void SetUnicodeStream (int parameterIndex, System.IO.Stream theInputStream, int length);
```

### Type Changed: Java.Sql.IResultSet

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Java.Math.BigDecimal GetBigDecimal (string columnName, int scale);

	[Obsolete ("deprecated")]
	public virtual Java.Math.BigDecimal GetBigDecimal (int columnIndex, int scale);

	[Obsolete ("deprecated")]
	public virtual System.IO.Stream GetUnicodeStream (string columnName);

	[Obsolete ("deprecated")]
	public virtual System.IO.Stream GetUnicodeStream (int columnIndex);
```

## Namespace Org.XmlPull.V1

### Type Changed: Org.XmlPull.V1.XmlPullParserFactory

Removed method:

```
public static XmlPullParserFactory NewInstance (string classNames, Java.Lang.Class context);
```

Added method:

```
public static XmlPullParserFactory NewInstance (string unused, Java.Lang.Class unused2);
```
