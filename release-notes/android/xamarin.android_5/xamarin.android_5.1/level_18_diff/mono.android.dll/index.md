---
id: 3E53B8F6-B55B-4AD1-852A-F91E0FDA3C00
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

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Accounts

### Type Changed: Android.Accounts.Account

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Accounts.AccountAuthenticatorResponse

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Accounts.AccountManager

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual IAccountManagerFuture GetAuthToken (Account account, string authTokenType, bool notifyAuthFailure, IAccountManagerCallback callback, Android.OS.Handler handler);
```

### Type Changed: Android.Accounts.AuthenticatorDescription

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Animation

### Type Changed: Android.Animation.LayoutTransition

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void HideChild (Android.Views.ViewGroup parent, Android.Views.View child);
	[Obsolete ("deprecated"]
	public virtual void ShowChild (Android.Views.ViewGroup parent, Android.Views.View child);
```

## Namespace Android.App

### Type Changed: Android.App.Activity

Modified properties:

```
protected System.Collections.Generic.IList<int> FocusedStateSet { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public void DismissDialog (int id);
	[Obsolete ("deprecated"]
	public Android.Database.ICursor ManagedQuery (Android.Net.Uri uri, string[] projection, string selection, string[] selectionArgs, string sortOrder);
	[Obsolete ("deprecated"]
	protected virtual Dialog OnCreateDialog (int id, Android.OS.Bundle args);
	[Obsolete ("deprecated"]
	protected virtual Dialog OnCreateDialog (int id);
	[Obsolete ("deprecated"]
	protected virtual void OnPrepareDialog (int id, Dialog dialog, Android.OS.Bundle args);
	[Obsolete ("deprecated"]
	protected virtual void OnPrepareDialog (int id, Dialog dialog);
	[Obsolete ("deprecated"]
	public virtual Java.Lang.Object OnRetainNonConfigurationInstance ();
	[Obsolete ("deprecated"]
	public void RemoveDialog (int id);
	[Obsolete ("deprecated"]
	public virtual void SetPersistent (bool isPersistent);
	[Obsolete ("deprecated"]
	public void ShowDialog (int id);
	[Obsolete ("deprecated"]
	public bool ShowDialog (int id, Android.OS.Bundle args);
	[Obsolete ("deprecated"]
	public virtual void StartManagingCursor (Android.Database.ICursor c);
	[Obsolete ("deprecated"]
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
[Obsolete ("deprecated"]
	public virtual void RestartPackage (string packageName);
```

### Type Changed: Android.App.ActivityManager.MemoryInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.ActivityManager.ProcessErrorStateInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.ActivityManager.RecentTaskInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.ActivityManager.RunningAppProcessInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.ActivityManager.RunningServiceInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.ActivityManager.RunningTaskInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.AlertDialog

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void SetButton (Java.Lang.ICharSequence text, Android.Content.IDialogInterfaceOnClickListener listener);
	[Obsolete ("deprecated"]
	public virtual void SetButton (Java.Lang.ICharSequence text, Android.OS.Message msg);
	[Obsolete ("deprecated"]
	public virtual void SetButton2 (Java.Lang.ICharSequence text, Android.OS.Message msg);
	[Obsolete ("deprecated"]
	public virtual void SetButton2 (Java.Lang.ICharSequence text, Android.Content.IDialogInterfaceOnClickListener listener);
	[Obsolete ("deprecated"]
	public virtual void SetButton3 (Java.Lang.ICharSequence text, Android.OS.Message msg);
	[Obsolete ("deprecated"]
	public virtual void SetButton3 (Java.Lang.ICharSequence text, Android.Content.IDialogInterfaceOnClickListener listener);
```

### Type Changed: Android.App.ApplicationErrorReport

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.DownloadManager

### Type Changed: Android.App.DownloadManager.Request

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual DownloadManager.Request SetShowRunningNotification (bool show);
```

### Type Changed: Android.App.Fragment

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void OnInflate (Android.Util.IAttributeSet attrs, Android.OS.Bundle savedInstanceState);
```

### Type Changed: Android.App.Fragment.SavedState

Modified properties:

```
public Android.OS.IParcelableClassLoaderCreator Creator { get; set; }
```

### Type Changed: Android.App.KeyguardManager

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void ExitKeyguardSecurely (KeyguardManager.IOnKeyguardExitResult callback);
	[Obsolete ("deprecated"]
	public virtual KeyguardManager.KeyguardLock NewKeyguardLock (string tag);
```

### Type Changed: Android.App.Notification

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void SetLatestEventInfo (Android.Content.Context context, Java.Lang.ICharSequence contentTitle, Java.Lang.ICharSequence contentText, PendingIntent contentIntent);
```

### Type Changed: Android.App.PendingIntent

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.SearchableInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.App.SearchManager

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void OnCancel (Android.Content.IDialogInterface dialog);
	[Obsolete ("deprecated"]
	public virtual void OnDismiss (Android.Content.IDialogInterface dialog);
```

### Type Changed: Android.App.Service

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void OnStart (Android.Content.Intent intent, int startId);
	[Obsolete ("deprecated"]
	public void SetForeground (bool isForeground);
```

### Type Changed: Android.App.WallpaperInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.App.Admin

### Type Changed: Android.App.Admin.DeviceAdminInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Appwidget

### Type Changed: Android.Appwidget.AppWidgetProviderInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothClass

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Bluetooth.BluetoothDevice

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Bluetooth.BluetoothGattDescriptor

Modified properties:

```
public System.Collections.Generic.IList<byte> DisableNotificationValue { get; set; }
	public System.Collections.Generic.IList<byte> EnableIndicationValue { get; set; }
	public System.Collections.Generic.IList<byte> EnableNotificationValue { get; set; }
```

### Type Changed: Android.Bluetooth.BluetoothGattServer

Added method:

```
public bool SendResponse (BluetoothDevice device, int requestId, GattStatus status, int offset, byte[] value);
```

### Type Changed: Android.Bluetooth.BluetoothHealthAppConfiguration

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Content

### Type Changed: Android.Content.ClipData

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.ClipDescription

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.ComponentName

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.ContentProviderOperation

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.ContentProviderResult

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.ContentResolver

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void CancelSync (Android.Net.Uri uri);
	[Obsolete ("deprecated"]
	public virtual void StartSync (Android.Net.Uri uri, Android.OS.Bundle extras);
```

### Type Changed: Android.Content.ContentValues

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.Intent

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static Intent GetIntent (string uri);
	[Obsolete ("deprecated"]
	public virtual string ToURI ();
```

### Type Changed: Android.Content.Intent.ShortcutIconResource

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.IntentFilter

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.IntentSender

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PeriodicSync

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.RestrictionEntry

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.SyncAdapterType

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.SyncResult

Modified properties:

```
public SyncResult AlreadyInProgress { get; set; }
	public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.SyncStats

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ActivityInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.ApplicationInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.ConfigurationInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.FeatureInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.InstrumentationInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.LabeledIntent

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.PackageInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.PackageStats

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.PathPermission

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.PermissionGroupInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.PermissionInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.ProviderInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.ResolveInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.ServiceInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.PM.Signature

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.AssetFileDescriptor

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.Res.ColorStateList

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.Res.Configuration

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Content.Res.ObbInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Database

### Type Changed: Android.Database.AbstractCursor

Obsoleted methods:

```
[Obsolete ("deprecated"]
	protected virtual Java.Lang.Object GetUpdatedField (int columnIndex);
	[Obsolete ("deprecated"]
	protected virtual bool IsFieldUpdated (int columnIndex);
```

### Type Changed: Android.Database.AbstractWindowedCursor

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual bool IsBlob (int columnIndex);
	[Obsolete ("deprecated"]
	public virtual bool IsFloat (int columnIndex);
	[Obsolete ("deprecated"]
	public virtual bool IsLong (int columnIndex);
	[Obsolete ("deprecated"]
	public virtual bool IsString (int columnIndex);
```

### Type Changed: Android.Database.ContentObservable

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void DispatchChange (bool selfChange);
	[Obsolete ("deprecated"]
	public virtual void NotifyChange (bool selfChange);
```

### Type Changed: Android.Database.ContentObserver

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public void DispatchChange (bool selfChange);
```

### Type Changed: Android.Database.CursorJoiner

### Type Changed: Android.Database.CursorJoiner.Result

Modified properties:

```
public CursorJoiner.Result Both { get; set; }
	public CursorJoiner.Result Left { get; set; }
	public CursorJoiner.Result Right { get; set; }
```

### Type Changed: Android.Database.CursorWindow

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual bool IsBlob (int row, int column);
	[Obsolete ("deprecated"]
	public virtual bool IsFloat (int row, int column);
	[Obsolete ("deprecated"]
	public virtual bool IsLong (int row, int column);
	[Obsolete ("deprecated"]
	public virtual bool IsNull (int row, int column);
	[Obsolete ("deprecated"]
	public virtual bool IsString (int row, int column);
```

## Namespace Android.Database.Sqlite

### Type Changed: Android.Database.Sqlite.SQLiteClosable

Obsoleted methods:

```
[Obsolete ("deprecated"]
	protected virtual void OnAllReferencesReleasedFromContainer ();
	[Obsolete ("deprecated"]
	public virtual void ReleaseReferenceFromContainer ();
```

### Type Changed: Android.Database.Sqlite.SQLiteDatabase

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void MarkTableSyncable (string table, string foreignKey, string updateTable);
	[Obsolete ("deprecated"]
	public virtual void MarkTableSyncable (string table, string deletedTable);
	[Obsolete ("deprecated"]
	public virtual void SetLockingEnabled (bool lockingEnabled);
	[Obsolete ("deprecated"]
	public virtual bool YieldIfContended ();
```

### Type Changed: Android.Database.Sqlite.SQLiteProgram

Obsoleted methods:

```
[Obsolete ("deprecated"]
	protected virtual void Compile (string sql, bool forceCompilation);
	[Obsolete ("deprecated"]
	protected void Native_compile (string sql);
	[Obsolete ("deprecated"]
	protected void Native_finalize ();
```

### Type Changed: Android.Database.Sqlite.SQLiteQueryBuilder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual string BuildQuery (string[] projectionIn, string selection, string[] selectionArgs, string groupBy, string having, string sortOrder, string limit);
	[Obsolete ("deprecated"]
	public virtual string BuildUnionSubQuery (string typeDiscriminatorColumn, string[] unionColumns, System.Collections.Generic.ICollection<string> columnsPresentInTable, int computedColumnsOffset, string typeDiscriminatorValue, string selection, string[] selectionArgs, string groupBy, string having);
```

## Namespace Android.Gestures

### Type Changed: Android.Gestures.Gesture

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Graphics

### Type Changed: Android.Graphics.AvoidXfermode

### Type Changed: Android.Graphics.AvoidXfermode.Mode

Modified properties:

```
public AvoidXfermode.Mode Avoid { get; set; }
	public AvoidXfermode.Mode Target { get; set; }
```

### Type Changed: Android.Graphics.Bitmap

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Graphics.Bitmap.CompressFormat

Modified properties:

```
public Bitmap.CompressFormat Jpeg { get; set; }
	public Bitmap.CompressFormat Png { get; set; }
	public Bitmap.CompressFormat Webp { get; set; }
```

### Type Changed: Android.Graphics.Bitmap.Config

Modified properties:

```
public Bitmap.Config Alpha8 { get; set; }
	public Bitmap.Config Argb4444 { get; set; }
	public Bitmap.Config Argb8888 { get; set; }
	public Bitmap.Config Rgb565 { get; set; }
```

### Type Changed: Android.Graphics.BlurMaskFilter

### Type Changed: Android.Graphics.BlurMaskFilter.Blur

Modified properties:

```
public BlurMaskFilter.Blur Inner { get; set; }
	public BlurMaskFilter.Blur Normal { get; set; }
	public BlurMaskFilter.Blur Outer { get; set; }
	public BlurMaskFilter.Blur Solid { get; set; }
```

### Type Changed: Android.Graphics.Canvas

Obsoleted constructors:

```
[Obsolete ("This method does not exist in API-11+."]
	public Canvas (Javax.Microedition.Khronos.Opengles.IGL gl);
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void DrawPosText (char[] text, int index, int count, float[] pos, Paint paint);
	[Obsolete ("deprecated"]
	public virtual void DrawPosText (string text, float[] pos, Paint paint);
	[Obsolete ("deprecated"]
	public virtual void GetMatrix (Matrix ctm);
```

### Type Changed: Android.Graphics.Canvas.EdgeType

Modified properties:

```
public Canvas.EdgeType Aa { get; set; }
	public Canvas.EdgeType Bw { get; set; }
```

### Type Changed: Android.Graphics.Canvas.VertexMode

Modified properties:

```
public Canvas.VertexMode TriangleFan { get; set; }
	public Canvas.VertexMode Triangles { get; set; }
	public Canvas.VertexMode TriangleStrip { get; set; }
```

### Type Changed: Android.Graphics.Interpolator

### Type Changed: Android.Graphics.Interpolator.Result

Modified properties:

```
public Interpolator.Result FreezeEnd { get; set; }
	public Interpolator.Result FreezeStart { get; set; }
	public Interpolator.Result Normal { get; set; }
```

### Type Changed: Android.Graphics.Matrix

### Type Changed: Android.Graphics.Matrix.ScaleToFit

Modified properties:

```
public Matrix.ScaleToFit Center { get; set; }
	public Matrix.ScaleToFit End { get; set; }
	public Matrix.ScaleToFit Fill { get; set; }
	public Matrix.ScaleToFit Start { get; set; }
```

### Type Changed: Android.Graphics.Paint

### Type Changed: Android.Graphics.Paint.Align

Modified properties:

```
public Paint.Align Center { get; set; }
	public Paint.Align Left { get; set; }
	public Paint.Align Right { get; set; }
```

### Type Changed: Android.Graphics.Paint.Cap

Modified properties:

```
public Paint.Cap Butt { get; set; }
	public Paint.Cap Round { get; set; }
	public Paint.Cap Square { get; set; }
```

### Type Changed: Android.Graphics.Paint.Join

Modified properties:

```
public Paint.Join Bevel { get; set; }
	public Paint.Join Miter { get; set; }
	public Paint.Join Round { get; set; }
```

### Type Changed: Android.Graphics.Paint.Style

Modified properties:

```
public Paint.Style Fill { get; set; }
	public Paint.Style FillAndStroke { get; set; }
	public Paint.Style Stroke { get; set; }
```

### Type Changed: Android.Graphics.Path

### Type Changed: Android.Graphics.Path.Direction

Modified properties:

```
public Path.Direction Ccw { get; set; }
	public Path.Direction Cw { get; set; }
```

### Type Changed: Android.Graphics.Path.FillType

Modified properties:

```
public Path.FillType EvenOdd { get; set; }
	public Path.FillType InverseEvenOdd { get; set; }
	public Path.FillType InverseWinding { get; set; }
	public Path.FillType Winding { get; set; }
```

### Type Changed: Android.Graphics.PathDashPathEffect

### Type Changed: Android.Graphics.PathDashPathEffect.Style

Modified properties:

```
public PathDashPathEffect.Style Morph { get; set; }
	public PathDashPathEffect.Style Rotate { get; set; }
	public PathDashPathEffect.Style Translate { get; set; }
```

### Type Changed: Android.Graphics.Picture

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static Picture CreateFromStream (System.IO.Stream stream);
	[Obsolete ("deprecated"]
	public virtual void WriteToStream (System.IO.Stream stream);
```

### Type Changed: Android.Graphics.Point

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Graphics.PointF

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Graphics.PorterDuff

### Type Changed: Android.Graphics.PorterDuff.Mode

Modified properties:

```
public PorterDuff.Mode Add { get; set; }
	public PorterDuff.Mode Clear { get; set; }
	public PorterDuff.Mode Darken { get; set; }
	public PorterDuff.Mode Dst { get; set; }
	public PorterDuff.Mode DstAtop { get; set; }
	public PorterDuff.Mode DstIn { get; set; }
	public PorterDuff.Mode DstOut { get; set; }
	public PorterDuff.Mode DstOver { get; set; }
	public PorterDuff.Mode Lighten { get; set; }
	public PorterDuff.Mode Multiply { get; set; }
	public PorterDuff.Mode Overlay { get; set; }
	public PorterDuff.Mode Screen { get; set; }
	public PorterDuff.Mode Src { get; set; }
	public PorterDuff.Mode SrcAtop { get; set; }
	public PorterDuff.Mode SrcIn { get; set; }
	public PorterDuff.Mode SrcOut { get; set; }
	public PorterDuff.Mode SrcOver { get; set; }
	public PorterDuff.Mode Xor { get; set; }
```

### Type Changed: Android.Graphics.Rect

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Graphics.RectF

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Graphics.Region

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Graphics.Region.Op

Modified properties:

```
public Region.Op Difference { get; set; }
	public Region.Op Intersect { get; set; }
	public Region.Op Replace { get; set; }
	public Region.Op ReverseDifference { get; set; }
	public Region.Op Union { get; set; }
	public Region.Op Xor { get; set; }
```

### Type Changed: Android.Graphics.Shader

### Type Changed: Android.Graphics.Shader.TileMode

Modified properties:

```
public Shader.TileMode Clamp { get; set; }
	public Shader.TileMode Mirror { get; set; }
	public Shader.TileMode Repeat { get; set; }
```

### Type Changed: Android.Graphics.Typeface

Modified properties:

```
public Typeface Default { get; set; }
	public Typeface DefaultBold { get; set; }
	public Typeface Monospace { get; set; }
	public Typeface SansSerif { get; set; }
	public Typeface Serif { get; set; }
```

## Namespace Android.Graphics.Drawables

### Type Changed: Android.Graphics.Drawables.GradientDrawable

### Type Changed: Android.Graphics.Drawables.GradientDrawable.Orientation

Modified properties:

```
public GradientDrawable.Orientation BlTr { get; set; }
	public GradientDrawable.Orientation BottomTop { get; set; }
	public GradientDrawable.Orientation BrTl { get; set; }
	public GradientDrawable.Orientation LeftRight { get; set; }
	public GradientDrawable.Orientation RightLeft { get; set; }
	public GradientDrawable.Orientation TlBr { get; set; }
	public GradientDrawable.Orientation TopBottom { get; set; }
	public GradientDrawable.Orientation TrBl { get; set; }
```

## Namespace Android.Hardware

### Type Changed: Android.Hardware.SensorManager

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual bool RegisterListener (ISensorListener listener, int sensors);
	[Obsolete ("deprecated"]
	public virtual bool RegisterListener (ISensorListener listener, int sensors, SensorDelay rate);
	[Obsolete ("deprecated"]
	public virtual void UnregisterListener (ISensorListener listener);
	[Obsolete ("deprecated"]
	public virtual void UnregisterListener (ISensorListener listener, int sensors);
```

## Namespace Android.Hardware.Usb

### Type Changed: Android.Hardware.Usb.UsbAccessory

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Hardware.Usb.UsbDevice

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Hardware.Usb.UsbEndpoint

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Hardware.Usb.UsbInterface

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Locations

### Type Changed: Android.Locations.Address

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Locations.Criteria

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Locations.Location

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Media

### Type Changed: Android.Media.AudioManager

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual Route GetRouting (Mode mode);
	[Obsolete ("deprecated"]
	public virtual VibrateSetting GetVibrateSetting (VibrateType vibrateType);
	[Obsolete ("deprecated"]
	public virtual void SetRouting (Mode mode, Route routes, Route mask);
	[Obsolete ("deprecated"]
	public virtual void SetVibrateSetting (VibrateType vibrateType, VibrateSetting vibrateSetting);
	[Obsolete ("deprecated"]
	public virtual bool ShouldVibrate (VibrateType vibrateType);
```

### Type Changed: Android.Media.MediaRecorder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void SetAuxiliaryOutputFile (Java.IO.FileDescriptor fd);
	[Obsolete ("deprecated"]
	public virtual void SetAuxiliaryOutputFile (string path);
```

## Namespace Android.Media.Audiofx

### Type Changed: Android.Media.Audiofx.AudioEffect

Modified properties:

```
public Java.Util.UUID EffectTypeAec { get; set; }
	public Java.Util.UUID EffectTypeAgc { get; set; }
	public Java.Util.UUID EffectTypeBassBoost { get; set; }
	public Java.Util.UUID EffectTypeEnvReverb { get; set; }
	public Java.Util.UUID EffectTypeEqualizer { get; set; }
	public Java.Util.UUID EffectTypeNs { get; set; }
	public Java.Util.UUID EffectTypePresetReverb { get; set; }
	public Java.Util.UUID EffectTypeVirtualizer { get; set; }
```

## Namespace Android.Net

### Type Changed: Android.Net.LocalSocketAddress

### Type Changed: Android.Net.LocalSocketAddress.Namespace

Modified properties:

```
public LocalSocketAddress.Namespace Abstract { get; set; }
	public LocalSocketAddress.Namespace Filesystem { get; set; }
	public LocalSocketAddress.Namespace Reserved { get; set; }
```

### Type Changed: Android.Net.NetworkInfo

### Type Changed: Android.Net.NetworkInfo.DetailedState

Modified properties:

```
public NetworkInfo.DetailedState Authenticating { get; set; }
	public NetworkInfo.DetailedState Blocked { get; set; }
	public NetworkInfo.DetailedState CaptivePortalCheck { get; set; }
	public NetworkInfo.DetailedState Connected { get; set; }
	public NetworkInfo.DetailedState Connecting { get; set; }
	public NetworkInfo.DetailedState Disconnected { get; set; }
	public NetworkInfo.DetailedState Disconnecting { get; set; }
	public NetworkInfo.DetailedState Failed { get; set; }
	public NetworkInfo.DetailedState Idle { get; set; }
	public NetworkInfo.DetailedState ObtainingIpaddr { get; set; }
	public NetworkInfo.DetailedState Scanning { get; set; }
	public NetworkInfo.DetailedState Suspended { get; set; }
	public NetworkInfo.DetailedState VerifyingPoorLink { get; set; }
```

### Type Changed: Android.Net.NetworkInfo.State

Modified properties:

```
public NetworkInfo.State Connected { get; set; }
	public NetworkInfo.State Connecting { get; set; }
	public NetworkInfo.State Disconnected { get; set; }
	public NetworkInfo.State Disconnecting { get; set; }
	public NetworkInfo.State Suspended { get; set; }
	public NetworkInfo.State Unknown { get; set; }
```

### Type Changed: Android.Net.Proxy

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static string GetHost (Android.Content.Context ctx);
	[Obsolete ("deprecated"]
	public static int GetPort (Android.Content.Context ctx);
```

### Type Changed: Android.Net.TrafficStats

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static long GetUidTcpRxBytes (int uid);
	[Obsolete ("deprecated"]
	public static long GetUidTcpRxSegments (int uid);
	[Obsolete ("deprecated"]
	public static long GetUidTcpTxBytes (int uid);
	[Obsolete ("deprecated"]
	public static long GetUidTcpTxSegments (int uid);
	[Obsolete ("deprecated"]
	public static long GetUidUdpRxBytes (int uid);
	[Obsolete ("deprecated"]
	public static long GetUidUdpRxPackets (int uid);
	[Obsolete ("deprecated"]
	public static long GetUidUdpTxBytes (int uid);
	[Obsolete ("deprecated"]
	public static long GetUidUdpTxPackets (int uid);
```

### Type Changed: Android.Net.Uri

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
	public Uri Empty { get; set; }
```

## Namespace Android.Net.Nsd

### Type Changed: Android.Net.Nsd.NsdServiceInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Net.Rtp

### Type Changed: Android.Net.Rtp.AudioCodec

Modified properties:

```
public AudioCodec Amr { get; set; }
	public AudioCodec Gsm { get; set; }
	public AudioCodec GsmEfr { get; set; }
	public AudioCodec Pcma { get; set; }
	public AudioCodec Pcmu { get; set; }
```

## Namespace Android.Net.Sip

### Type Changed: Android.Net.Sip.SipProfile

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Net.Wifi

### Type Changed: Android.Net.Wifi.SupplicantState

Modified properties:

```
public SupplicantState Associated { get; set; }
	public SupplicantState Associating { get; set; }
	public SupplicantState Authenticating { get; set; }
	public SupplicantState Completed { get; set; }
	public SupplicantState Disconnected { get; set; }
	public SupplicantState Dormant { get; set; }
	public SupplicantState FourWayHandshake { get; set; }
	public SupplicantState GroupHandshake { get; set; }
	public SupplicantState Inactive { get; set; }
	public SupplicantState InterfaceDisabled { get; set; }
	public SupplicantState Invalid { get; set; }
	public SupplicantState Scanning { get; set; }
	public SupplicantState Uninitialized { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration

Added property:

```
public WifiStatus StatusField { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.AuthAlgorithm

Modified properties:

```
public System.Collections.Generic.IList<string> Strings { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.GroupCipher

Modified properties:

```
public System.Collections.Generic.IList<string> Strings { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.KeyMgmt

Modified properties:

```
public System.Collections.Generic.IList<string> Strings { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.PairwiseCipher

Modified properties:

```
public System.Collections.Generic.IList<string> Strings { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.Protocol

Modified properties:

```
public System.Collections.Generic.IList<string> Strings { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.Status

Modified properties:

```
public System.Collections.Generic.IList<string> Strings { get; set; }
```

### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Net.Wifi.WpsInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Net.Wifi.P2p

### Type Changed: Android.Net.Wifi.P2p.WifiP2pConfig

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Net.Wifi.P2p.WifiP2pDevice

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Net.Wifi.P2p.WifiP2pDeviceList

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Net.Wifi.P2p.WifiP2pGroup

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Net.Wifi.P2p.WifiP2pInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Nfc

### Type Changed: Android.Nfc.NdefMessage

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Nfc.NdefRecord

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
	public System.Collections.Generic.IList<byte> RtdAlternativeCarrier { get; set; }
	public System.Collections.Generic.IList<byte> RtdHandoverCarrier { get; set; }
	public System.Collections.Generic.IList<byte> RtdHandoverRequest { get; set; }
	public System.Collections.Generic.IList<byte> RtdHandoverSelect { get; set; }
	public System.Collections.Generic.IList<byte> RtdSmartPoster { get; set; }
	public System.Collections.Generic.IList<byte> RtdText { get; set; }
	public System.Collections.Generic.IList<byte> RtdUri { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public byte[] ToByteArray ();
```

### Type Changed: Android.Nfc.NfcAdapter

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public void DisableForegroundNdefPush (Android.App.Activity activity);
	[Obsolete ("deprecated"]
	public void EnableForegroundNdefPush (Android.App.Activity activity, NdefMessage message);
```

### Type Changed: Android.Nfc.Tag

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Nfc.Tech

### Type Changed: Android.Nfc.Tech.MifareClassic

Modified properties:

```
public System.Collections.Generic.IList<byte> KeyDefault { get; set; }
	public System.Collections.Generic.IList<byte> KeyMifareApplicationDirectory { get; set; }
	public System.Collections.Generic.IList<byte> KeyNfcForum { get; set; }
```

## Namespace Android.OS

### Type Changed: Android.OS.AsyncTask

Modified properties:

```
public Java.Util.Concurrent.IExecutor SerialExecutor { get; set; }
	public Java.Util.Concurrent.IExecutor ThreadPoolExecutor { get; set; }
```

### Type Changed: Android.OS.AsyncTask.Status

Modified properties:

```
public AsyncTask.Status Finished { get; set; }
	public AsyncTask.Status Pending { get; set; }
	public AsyncTask.Status Running { get; set; }
```

### Type Changed: Android.OS.Build

Modified properties:

```
public string Board { get; set; }
	public string Bootloader { get; set; }
	public string Brand { get; set; }
	public string CpuAbi { get; set; }
	public string CpuAbi2 { get; set; }
	public string Device { get; set; }
	public string Display { get; set; }
	public string Fingerprint { get; set; }
	public string Hardware { get; set; }
	public string Host { get; set; }
	public string Id { get; set; }
	public string Manufacturer { get; set; }
	public string Model { get; set; }
	public string Product { get; set; }
	public string Radio { get; set; }
	public string Serial { get; set; }
	public string Tags { get; set; }
	public long Time { get; set; }
	public string Type { get; set; }
	public string User { get; set; }
```

### Type Changed: Android.OS.Build.VERSION

Modified properties:

```
public string Codename { get; set; }
	public string Incremental { get; set; }
	public string Release { get; set; }
	public string Sdk { get; set; }
	public BuildVersionCodes SdkInt { get; set; }
```

### Type Changed: Android.OS.Bundle

Modified properties:

```
public IParcelableCreator Creator { get; set; }
	public Bundle Empty { get; set; }
```

### Type Changed: Android.OS.Debug

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static void ChangeDebugPort (int port);
	[Obsolete ("deprecated"]
	public static void ResetGlobalExternalAllocCount ();
	[Obsolete ("deprecated"]
	public static void ResetGlobalExternalAllocSize ();
	[Obsolete ("deprecated"]
	public static void ResetGlobalExternalFreedCount ();
	[Obsolete ("deprecated"]
	public static void ResetGlobalExternalFreedSize ();
	[Obsolete ("deprecated"]
	public static void ResetThreadExternalAllocCount ();
	[Obsolete ("deprecated"]
	public static void ResetThreadExternalAllocSize ();
	[Obsolete ("deprecated"]
	public static int SetAllocationLimit (int limit);
	[Obsolete ("deprecated"]
	public static int SetGlobalAllocationLimit (int limit);
	[Obsolete ("deprecated"]
	public static void StartAllocCounting ();
	[Obsolete ("deprecated"]
	public static void StopAllocCounting ();
```

### Type Changed: Android.OS.Debug.MemoryInfo

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.DropBoxManager

### Type Changed: Android.OS.DropBoxManager.Entry

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.Message

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.Messenger

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.Parcel

Modified properties:

```
public IParcelableCreator StringCreator { get; set; }
```

### Type Changed: Android.OS.ParcelFileDescriptor

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.ParcelUuid

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.PatternMatcher

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.Process

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static bool SupportsProcesses ();
```

### Type Changed: Android.OS.ResultReceiver

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.StrictMode

### Type Changed: Android.OS.StrictMode.ThreadPolicy

Modified properties:

```
public StrictMode.ThreadPolicy Lax { get; set; }
```

### Type Changed: Android.OS.StrictMode.VmPolicy

Modified properties:

```
public StrictMode.VmPolicy Lax { get; set; }
```

### Type Changed: Android.OS.UserHandle

Modified properties:

```
public IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.OS.WorkSource

Modified properties:

```
public IParcelableCreator Creator { get; set; }
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

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Preferences.PreferenceActivity

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void AddPreferencesFromIntent (Android.Content.Intent intent);
	[Obsolete ("deprecated"]
	public virtual void AddPreferencesFromResource (int preferencesResId);
	[Obsolete ("deprecated"]
	public virtual Preference FindPreference (Java.Lang.ICharSequence key);
	[Obsolete ("deprecated"]
	public virtual bool OnPreferenceTreeClick (PreferenceScreen preferenceScreen, Preference preference);
```

### Type Changed: Android.Preferences.PreferenceActivity.Header

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Provider

### Type Changed: Android.Provider.Browser

Modified properties:

```
public Android.Net.Uri BookmarksUri { get; set; }
	public System.Collections.Generic.IList<string> HistoryProjection { get; set; }
	public System.Collections.Generic.IList<string> SearchesProjection { get; set; }
	public Android.Net.Uri SearchesUri { get; set; }
	public System.Collections.Generic.IList<string> TruncateHistoryProjection { get; set; }
```

### Type Changed: Android.Provider.CalendarContract

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.Attendees

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.CalendarAlerts

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri ContentUriByInstance { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.CalendarCache

Modified properties:

```
public Android.Net.Uri Uri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.CalendarEntity

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.Calendars

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.Colors

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.EventDays

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.Events

Modified properties:

```
public Android.Net.Uri ContentExceptionUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.EventsEntity

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.ExtendedProperties

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.Instances

Modified properties:

```
public Android.Net.Uri ContentByDayUri { get; set; }
	public Android.Net.Uri ContentSearchByDayUri { get; set; }
	public Android.Net.Uri ContentSearchUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.Reminders

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CalendarContract.SyncState

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CallLog

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.CallLog.Calls

Modified properties:

```
public Android.Net.Uri ContentFilterUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.Contacts

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.Contacts.ContactMethods

Modified properties:

```
public Android.Net.Uri ContentEmailUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public void AddPostalLocation (Android.Content.Context context, long postalId, double latitude, double longitude);
	[Obsolete ("deprecated"]
	public static Java.Lang.Object DecodeImProtocol (string encodedString);
	[Obsolete ("deprecated"]
	public static string EncodeCustomImProtocol (string protocolString);
	[Obsolete ("deprecated"]
	public static string EncodePredefinedImProtocol (int protocol);
	[Obsolete ("deprecated"]
	public static Java.Lang.ICharSequence GetDisplayLabelFormatted (Android.Content.Context context, ContactKind kind, ContactMethodColumn type, Java.Lang.ICharSequence label);
```

### Type Changed: Android.Provider.Contacts.Extensions

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.Contacts.GroupMembership

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri RawContentUri { get; set; }
```

### Type Changed: Android.Provider.Contacts.Groups

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri DeletedContentUri { get; set; }
```

### Type Changed: Android.Provider.Contacts.Organizations

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static Java.Lang.ICharSequence GetDisplayLabelFormatted (Android.Content.Context context, ContactOrganizationColumn type, Java.Lang.ICharSequence label);
```

### Type Changed: Android.Provider.Contacts.People

Modified properties:

```
public Android.Net.Uri ContentFilterUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri DeletedContentUri { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static Android.Net.Uri AddToGroup (Android.Content.ContentResolver resolver, long personId, string groupName);
	[Obsolete ("deprecated"]
	public static Android.Net.Uri AddToGroup (Android.Content.ContentResolver resolver, long personId, long groupId);
	[Obsolete ("deprecated"]
	public static Android.Net.Uri AddToMyContactsGroup (Android.Content.ContentResolver resolver, long personId);
	[Obsolete ("deprecated"]
	public static Android.Net.Uri CreatePersonInMyContactsGroup (Android.Content.ContentResolver resolver, Android.Content.ContentValues values);
	[Obsolete ("deprecated"]
	public static Android.Graphics.Bitmap LoadContactPhoto (Android.Content.Context context, Android.Net.Uri person, int placeholderImageResource, Android.Graphics.BitmapFactory.Options options);
	[Obsolete ("deprecated"]
	public static void MarkAsContacted (Android.Content.ContentResolver resolver, long personId);
	[Obsolete ("deprecated"]
	public static System.IO.Stream OpenContactPhotoInputStream (Android.Content.ContentResolver cr, Android.Net.Uri person);
	[Obsolete ("deprecated"]
	public static Android.Database.ICursor QueryGroups (Android.Content.ContentResolver resolver, long person);
	[Obsolete ("deprecated"]
	public static void SetPhotoData (Android.Content.ContentResolver cr, Android.Net.Uri person, byte[] data);
```

### Type Changed: Android.Provider.Contacts.Phones

Modified properties:

```
public Android.Net.Uri ContentFilterUrl { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static Java.Lang.ICharSequence GetDisplayLabelFormatted (Android.Content.Context context, ContactPhoneColumn type, Java.Lang.ICharSequence label);
	[Obsolete ("deprecated"]
	public static Java.Lang.ICharSequence GetDisplayLabelFormatted (Android.Content.Context context, ContactPhoneColumn type, Java.Lang.ICharSequence label, Java.Lang.ICharSequence[] labelArray);
```

### Type Changed: Android.Provider.Contacts.Photos

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.Contacts.Settings

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static string GetSetting (Android.Content.ContentResolver cr, string account, string key);
	[Obsolete ("deprecated"]
	public static void SetSetting (Android.Content.ContentResolver cr, string account, string key, string value);
```

### Type Changed: Android.Provider.ContactsContract

Modified properties:

```
public Android.Net.Uri AuthorityUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.AggregationExceptions

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.CommonDataKinds

### Type Changed: Android.Provider.ContactsContract.Contactables

Modified properties:

```
public Android.Net.Uri ContentFilterUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.Email

Modified properties:

```
public Android.Net.Uri ContentFilterUri { get; set; }
	public Android.Net.Uri ContentLookupUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.Phone

Modified properties:

```
public Android.Net.Uri ContentFilterUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.StructuredPostal

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.Contacts

Modified properties:

```
public Android.Net.Uri ContentFilterUri { get; set; }
	public Android.Net.Uri ContentGroupUri { get; set; }
	public Android.Net.Uri ContentLookupUri { get; set; }
	public Android.Net.Uri ContentStrequentFilterUri { get; set; }
	public Android.Net.Uri ContentStrequentUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri ContentVcardUri { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static void MarkAsContacted (Android.Content.ContentResolver resolver, long contactId);
```

### Type Changed: Android.Provider.ContactsContract.Data

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.DataUsageFeedback

Modified properties:

```
public Android.Net.Uri DeleteUsageUri { get; set; }
	public Android.Net.Uri FeedbackUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.DeletedContacts

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.Directory

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.DisplayPhoto

Modified properties:

```
public Android.Net.Uri ContentMaxDimensionsUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.Groups

Modified properties:

```
public Android.Net.Uri ContentSummaryUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.PhoneLookup

Modified properties:

```
public Android.Net.Uri ContentFilterUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.Profile

Modified properties:

```
public Android.Net.Uri ContentRawContactsUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri ContentVcardUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.ProfileSyncState

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.RawContacts

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.RawContactsEntity

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri ProfileContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.Settings

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.StatusUpdates

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri ProfileContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.StreamItems

Modified properties:

```
public Android.Net.Uri ContentLimitUri { get; set; }
	public Android.Net.Uri ContentPhotoUri { get; set; }
	public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.ContactsContract.SyncState

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore

### Type Changed: Android.Provider.MediaStore.Audio

### Type Changed: Android.Provider.MediaStore.Albums

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore.Artists

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore.Genres

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore.Media

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore.Playlists

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore.Images

### Type Changed: Android.Provider.MediaStore.Media

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore.Thumbnails

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore.Video

### Type Changed: Android.Provider.MediaStore.Media

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.MediaStore.Thumbnails

Modified properties:

```
public Android.Net.Uri ExternalContentUri { get; set; }
	public Android.Net.Uri InternalContentUri { get; set; }
```

### Type Changed: Android.Provider.SearchRecentSuggestions

Modified properties:

```
public System.Collections.Generic.IList<string> QueriesProjection1line { get; set; }
	public System.Collections.Generic.IList<string> QueriesProjection2line { get; set; }
```

### Type Changed: Android.Provider.Settings

### Type Changed: Android.Provider.Settings.Global

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.Settings.Secure

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.Settings.System

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
	public Android.Net.Uri DefaultAlarmAlertUri { get; set; }
	public Android.Net.Uri DefaultNotificationUri { get; set; }
	public Android.Net.Uri DefaultRingtoneUri { get; set; }
	public System.Collections.Generic.IList<string> VolumeSettings { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static bool GetShowGTalkServiceStatus (Android.Content.ContentResolver cr);
	[Obsolete ("deprecated"]
	public static void SetShowGTalkServiceStatus (Android.Content.ContentResolver cr, bool flag);
```

### Type Changed: Android.Provider.UserDictionary

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.UserDictionary.Words

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static void AddWord (Android.Content.Context context, string word, int frequency, LocaleType localeType);
```

### Type Changed: Android.Provider.VoicemailContract

### Type Changed: Android.Provider.VoicemailContract.Status

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

### Type Changed: Android.Provider.VoicemailContract.Voicemails

Modified properties:

```
public Android.Net.Uri ContentUri { get; set; }
```

## Namespace Android.Renderscripts

### Type Changed: Android.Renderscripts.Allocation

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void Resize (int dimX);
```

### Type Changed: Android.Renderscripts.Allocation.MipmapControl

Modified properties:

```
public Allocation.MipmapControl MipmapFull { get; set; }
	public Allocation.MipmapControl MipmapNone { get; set; }
	public Allocation.MipmapControl MipmapOnSyncToTexture { get; set; }
```

### Type Changed: Android.Renderscripts.Element

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static Element MATRIX4X4 (RenderScript rs);
```

### Type Changed: Android.Renderscripts.Element.DataKind

Modified properties:

```
public Element.DataKind PixelA { get; set; }
	public Element.DataKind PixelDepth { get; set; }
	public Element.DataKind PixelL { get; set; }
	public Element.DataKind PixelLa { get; set; }
	public Element.DataKind PixelRgb { get; set; }
	public Element.DataKind PixelRgba { get; set; }
	public Element.DataKind PixelYuv { get; set; }
	public Element.DataKind User { get; set; }
```

### Type Changed: Android.Renderscripts.Element.DataType

Modified properties:

```
public Element.DataType Boolean { get; set; }
	public Element.DataType Float32 { get; set; }
	public Element.DataType Float64 { get; set; }
	public Element.DataType Matrix2x2 { get; set; }
	public Element.DataType Matrix3x3 { get; set; }
	public Element.DataType Matrix4x4 { get; set; }
	public Element.DataType None { get; set; }
	public Element.DataType RsAllocation { get; set; }
	public Element.DataType RsElement { get; set; }
	public Element.DataType RsFont { get; set; }
	public Element.DataType RsMesh { get; set; }
	public Element.DataType RsProgramFragment { get; set; }
	public Element.DataType RsProgramRaster { get; set; }
	public Element.DataType RsProgramStore { get; set; }
	public Element.DataType RsProgramVertex { get; set; }
	public Element.DataType RsSampler { get; set; }
	public Element.DataType RsScript { get; set; }
	public Element.DataType RsType { get; set; }
	public Element.DataType Signed16 { get; set; }
	public Element.DataType Signed32 { get; set; }
	public Element.DataType Signed64 { get; set; }
	public Element.DataType Signed8 { get; set; }
	public Element.DataType Unsigned16 { get; set; }
	public Element.DataType Unsigned32 { get; set; }
	public Element.DataType Unsigned4444 { get; set; }
	public Element.DataType Unsigned5551 { get; set; }
	public Element.DataType Unsigned565 { get; set; }
	public Element.DataType Unsigned64 { get; set; }
	public Element.DataType Unsigned8 { get; set; }
```

### Type Changed: Android.Renderscripts.FileA3D

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static FileA3D CreateFromAsset (RenderScript rs, Android.Content.Res.AssetManager mgr, string path);
	[Obsolete ("deprecated"]
	public static FileA3D CreateFromFile (RenderScript rs, Java.IO.File path);
	[Obsolete ("deprecated"]
	public static FileA3D CreateFromFile (RenderScript rs, string path);
	[Obsolete ("deprecated"]
	public static FileA3D CreateFromResource (RenderScript rs, Android.Content.Res.Resources res, int id);
	[Obsolete ("deprecated"]
	public virtual FileA3D.IndexEntry GetIndexEntry (int index);
```

### Type Changed: Android.Renderscripts.FileA3D.EntryType

Modified properties:

```
public FileA3D.EntryType Mesh { get; set; }
	public FileA3D.EntryType Unknown { get; set; }
```

### Type Changed: Android.Renderscripts.Font

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static Font Create (RenderScript rs, Android.Content.Res.Resources res, string familyName, Font.Style fontStyle, float pointSize);
	[Obsolete ("deprecated"]
	public static Font CreateFromAsset (RenderScript rs, Android.Content.Res.Resources res, string path, float pointSize);
	[Obsolete ("deprecated"]
	public static Font CreateFromFile (RenderScript rs, Android.Content.Res.Resources res, Java.IO.File path, float pointSize);
	[Obsolete ("deprecated"]
	public static Font CreateFromFile (RenderScript rs, Android.Content.Res.Resources res, string path, float pointSize);
	[Obsolete ("deprecated"]
	public static Font CreateFromResource (RenderScript rs, Android.Content.Res.Resources res, int id, float pointSize);
```

### Type Changed: Android.Renderscripts.Font.Style

Modified properties:

```
public Font.Style Bold { get; set; }
	public Font.Style BoldItalic { get; set; }
	public Font.Style Italic { get; set; }
	public Font.Style Normal { get; set; }
```

### Type Changed: Android.Renderscripts.Mesh

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual Allocation GetIndexSetAllocation (int slot);
	[Obsolete ("deprecated"]
	public virtual Mesh.Primitive GetPrimitive (int slot);
	[Obsolete ("deprecated"]
	public virtual Allocation GetVertexAllocation (int slot);
```

### Type Changed: Android.Renderscripts.Mesh.AllocationBuilder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual Mesh.AllocationBuilder AddIndexSetAllocation (Allocation a, Mesh.Primitive p);
	[Obsolete ("deprecated"]
	public virtual Mesh.AllocationBuilder AddIndexSetType (Mesh.Primitive p);
	[Obsolete ("deprecated"]
	public virtual Mesh.AllocationBuilder AddVertexAllocation (Allocation a);
	[Obsolete ("deprecated"]
	public virtual Mesh Create ();
```

### Type Changed: Android.Renderscripts.Mesh.Builder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual Mesh.Builder AddIndexSetType (Element e, int size, Mesh.Primitive p);
	[Obsolete ("deprecated"]
	public virtual Mesh.Builder AddIndexSetType (Mesh.Primitive p);
	[Obsolete ("deprecated"]
	public virtual Mesh.Builder AddIndexSetType (Type t, Mesh.Primitive p);
	[Obsolete ("deprecated"]
	public virtual Mesh.Builder AddVertexType (Element e, int size);
	[Obsolete ("deprecated"]
	public virtual Mesh.Builder AddVertexType (Type t);
	[Obsolete ("deprecated"]
	public virtual Mesh Create ();
```

### Type Changed: Android.Renderscripts.Mesh.Primitive

Modified properties:

```
public Mesh.Primitive Line { get; set; }
	public Mesh.Primitive LineStrip { get; set; }
	public Mesh.Primitive Point { get; set; }
	public Mesh.Primitive Triangle { get; set; }
	public Mesh.Primitive TriangleFan { get; set; }
	public Mesh.Primitive TriangleStrip { get; set; }
```

### Type Changed: Android.Renderscripts.Mesh.TriangleMeshBuilder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual Mesh.TriangleMeshBuilder AddTriangle (int idx1, int idx2, int idx3);
	[Obsolete ("deprecated"]
	public virtual Mesh.TriangleMeshBuilder AddVertex (float x, float y);
	[Obsolete ("deprecated"]
	public virtual Mesh.TriangleMeshBuilder AddVertex (float x, float y, float z);
	[Obsolete ("deprecated"]
	public virtual Mesh Create (bool uploadToBufferObject);
	[Obsolete ("deprecated"]
	public virtual Mesh.TriangleMeshBuilder SetColor (float r, float g, float b, float a);
	[Obsolete ("deprecated"]
	public virtual Mesh.TriangleMeshBuilder SetNormal (float x, float y, float z);
	[Obsolete ("deprecated"]
	public virtual Mesh.TriangleMeshBuilder SetTexture (float s, float t);
```

### Type Changed: Android.Renderscripts.Program

### Type Changed: Android.Renderscripts.Program.TextureType

Modified properties:

```
public Program.TextureType Texture2d { get; set; }
	public Program.TextureType TextureCube { get; set; }
```

### Type Changed: Android.Renderscripts.ProgramFragment

### Type Changed: Android.Renderscripts.ProgramFragment.Builder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual ProgramFragment Create ();
```

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction.Builder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual ProgramFragmentFixedFunction Create ();
	[Obsolete ("deprecated"]
	public virtual ProgramFragmentFixedFunction.Builder SetPointSpriteTexCoordinateReplacement (bool enable);
	[Obsolete ("deprecated"]
	public virtual ProgramFragmentFixedFunction.Builder SetTexture (ProgramFragmentFixedFunction.Builder.EnvMode env, ProgramFragmentFixedFunction.Builder.Format fmt, int slot);
	[Obsolete ("deprecated"]
	public virtual ProgramFragmentFixedFunction.Builder SetVaryingColor (bool enable);
```

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction.EnvMode

Modified properties:

```
public ProgramFragmentFixedFunction.Builder.EnvMode Decal { get; set; }
	public ProgramFragmentFixedFunction.Builder.EnvMode Modulate { get; set; }
	public ProgramFragmentFixedFunction.Builder.EnvMode Replace { get; set; }
```

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction.Format

Modified properties:

```
public ProgramFragmentFixedFunction.Builder.Format Alpha { get; set; }
	public ProgramFragmentFixedFunction.Builder.Format LuminanceAlpha { get; set; }
	public ProgramFragmentFixedFunction.Builder.Format Rgb { get; set; }
	public ProgramFragmentFixedFunction.Builder.Format Rgba { get; set; }
```

### Type Changed: Android.Renderscripts.ProgramRaster

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static ProgramRaster CULL_BACK (RenderScript rs);
	[Obsolete ("deprecated"]
	public static ProgramRaster CULL_FRONT (RenderScript rs);
	[Obsolete ("deprecated"]
	public static ProgramRaster CULL_NONE (RenderScript rs);
	[Obsolete ("deprecated"]
	public virtual ProgramRaster.CullMode GetCullMode ();
```

### Type Changed: Android.Renderscripts.ProgramRaster.Builder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual ProgramRaster Create ();
	[Obsolete ("deprecated"]
	public virtual ProgramRaster.Builder SetCullMode (ProgramRaster.CullMode m);
	[Obsolete ("deprecated"]
	public virtual ProgramRaster.Builder SetPointSpriteEnabled (bool enable);
```

### Type Changed: Android.Renderscripts.ProgramRaster.CullMode

Modified properties:

```
public ProgramRaster.CullMode Back { get; set; }
	public ProgramRaster.CullMode Front { get; set; }
	public ProgramRaster.CullMode None { get; set; }
```

### Type Changed: Android.Renderscripts.ProgramStore

### Type Changed: Android.Renderscripts.ProgramStore.BlendDstFunc

Modified properties:

```
public ProgramStore.BlendDstFunc DstAlpha { get; set; }
	public ProgramStore.BlendDstFunc One { get; set; }
	public ProgramStore.BlendDstFunc OneMinusDstAlpha { get; set; }
	public ProgramStore.BlendDstFunc OneMinusSrcAlpha { get; set; }
	public ProgramStore.BlendDstFunc OneMinusSrcColor { get; set; }
	public ProgramStore.BlendDstFunc SrcAlpha { get; set; }
	public ProgramStore.BlendDstFunc SrcColor { get; set; }
	public ProgramStore.BlendDstFunc Zero { get; set; }
```

### Type Changed: Android.Renderscripts.ProgramStore.BlendSrcFunc

Modified properties:

```
public ProgramStore.BlendSrcFunc DstAlpha { get; set; }
	public ProgramStore.BlendSrcFunc DstColor { get; set; }
	public ProgramStore.BlendSrcFunc One { get; set; }
	public ProgramStore.BlendSrcFunc OneMinusDstAlpha { get; set; }
	public ProgramStore.BlendSrcFunc OneMinusDstColor { get; set; }
	public ProgramStore.BlendSrcFunc OneMinusSrcAlpha { get; set; }
	public ProgramStore.BlendSrcFunc SrcAlpha { get; set; }
	public ProgramStore.BlendSrcFunc SrcAlphaSaturate { get; set; }
	public ProgramStore.BlendSrcFunc Zero { get; set; }
```

### Type Changed: Android.Renderscripts.ProgramStore.DepthFunc

Modified properties:

```
public ProgramStore.DepthFunc Always { get; set; }
	public ProgramStore.DepthFunc Equal { get; set; }
	public ProgramStore.DepthFunc Greater { get; set; }
	public ProgramStore.DepthFunc GreaterOrEqual { get; set; }
	public ProgramStore.DepthFunc Less { get; set; }
	public ProgramStore.DepthFunc LessOrEqual { get; set; }
	public ProgramStore.DepthFunc NotEqual { get; set; }
```

### Type Changed: Android.Renderscripts.ProgramVertex

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual Element GetInput (int slot);
```

### Type Changed: Android.Renderscripts.ProgramVertex.Builder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual ProgramVertex.Builder AddInput (Element e);
	[Obsolete ("deprecated"]
	public virtual ProgramVertex Create ();
```

### Type Changed: Android.Renderscripts.ProgramVertexFixedFunction

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void BindConstants (ProgramVertexFixedFunction.Constants va);
```

### Type Changed: Android.Renderscripts.ProgramVertexFixedFunction.Builder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual ProgramVertexFixedFunction Create ();
	[Obsolete ("deprecated"]
	public virtual ProgramVertexFixedFunction.Builder SetTextureMatrixEnable (bool enable);
```

### Type Changed: Android.Renderscripts.ProgramVertexFixedFunction.Constants

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void Destroy ();
	[Obsolete ("deprecated"]
	public virtual void SetModelview (Matrix4f m);
	[Obsolete ("deprecated"]
	public virtual void SetProjection (Matrix4f m);
	[Obsolete ("deprecated"]
	public virtual void SetTexture (Matrix4f m);
```

### Type Changed: Android.Renderscripts.RenderScript

### Type Changed: Android.Renderscripts.RenderScript.ContextType

Modified properties:

```
public RenderScript.ContextType Debug { get; set; }
	public RenderScript.ContextType Normal { get; set; }
	public RenderScript.ContextType Profile { get; set; }
```

### Type Changed: Android.Renderscripts.RenderScript.Priority

Modified properties:

```
public RenderScript.Priority Low { get; set; }
	public RenderScript.Priority Normal { get; set; }
```

### Type Changed: Android.Renderscripts.RenderScriptGL

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void BindProgramFragment (ProgramFragment p);
	[Obsolete ("deprecated"]
	public virtual void BindProgramRaster (ProgramRaster p);
	[Obsolete ("deprecated"]
	public virtual void BindProgramStore (ProgramStore p);
	[Obsolete ("deprecated"]
	public virtual void BindProgramVertex (ProgramVertex p);
	[Obsolete ("deprecated"]
	public virtual void BindRootScript (Script s);
	[Obsolete ("deprecated"]
	public virtual void Pause ();
	[Obsolete ("deprecated"]
	public virtual void Resume ();
	[Obsolete ("deprecated"]
	public virtual void SetSurface (Android.Views.ISurfaceHolder sur, int w, int h);
	[Obsolete ("deprecated"]
	public virtual void SetSurfaceTexture (Android.Graphics.SurfaceTexture sur, int w, int h);
```

### Type Changed: Android.Renderscripts.RenderScriptGL.SurfaceConfig

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void SetAlpha (int minimum, int preferred);
	[Obsolete ("deprecated"]
	public virtual void SetColor (int minimum, int preferred);
	[Obsolete ("deprecated"]
	public virtual void SetDepth (int minimum, int preferred);
	[Obsolete ("deprecated"]
	public virtual void SetSamples (int minimum, int preferred, float Q);
```

### Type Changed: Android.Renderscripts.RSSurfaceView

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual RenderScriptGL CreateRenderScriptGL (RenderScriptGL.SurfaceConfig sc);
	[Obsolete ("deprecated"]
	public virtual void DestroyRenderScriptGL ();
	[Obsolete ("deprecated"]
	public virtual void Pause ();
	[Obsolete ("deprecated"]
	public virtual void Resume ();
	[Obsolete ("deprecated"]
	public virtual void SurfaceChanged (Android.Views.ISurfaceHolder holder, Android.Graphics.Format format, int w, int h);
	[Obsolete ("deprecated"]
	public virtual void SurfaceCreated (Android.Views.ISurfaceHolder holder);
	[Obsolete ("deprecated"]
	public virtual void SurfaceDestroyed (Android.Views.ISurfaceHolder holder);
```

### Type Changed: Android.Renderscripts.RSTextureView

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual RenderScriptGL CreateRenderScriptGL (RenderScriptGL.SurfaceConfig sc);
	[Obsolete ("deprecated"]
	public virtual void DestroyRenderScriptGL ();
	[Obsolete ("deprecated"]
	public virtual void OnSurfaceTextureAvailable (Android.Graphics.SurfaceTexture surface, int width, int height);
	[Obsolete ("deprecated"]
	public virtual bool OnSurfaceTextureDestroyed (Android.Graphics.SurfaceTexture surface);
	[Obsolete ("deprecated"]
	public virtual void OnSurfaceTextureSizeChanged (Android.Graphics.SurfaceTexture surface, int width, int height);
	[Obsolete ("deprecated"]
	public virtual void OnSurfaceTextureUpdated (Android.Graphics.SurfaceTexture surface);
	[Obsolete ("deprecated"]
	public virtual void Pause ();
	[Obsolete ("deprecated"]
	public virtual void Resume ();
```

### Type Changed: Android.Renderscripts.Sampler

### Type Changed: Android.Renderscripts.Sampler.Value

Modified properties:

```
public Sampler.Value Clamp { get; set; }
	public Sampler.Value Linear { get; set; }
	public Sampler.Value LinearMipLinear { get; set; }
	public Sampler.Value LinearMipNearest { get; set; }
	public Sampler.Value MirroredRepeat { get; set; }
	public Sampler.Value Nearest { get; set; }
	public Sampler.Value Wrap { get; set; }
```

### Type Changed: Android.Renderscripts.Type

### Type Changed: Android.Renderscripts.Type.CubemapFace

Modified properties:

```
public Type.CubemapFace NegativeX { get; set; }
	public Type.CubemapFace NegativeY { get; set; }
	public Type.CubemapFace NegativeZ { get; set; }
	public Type.CubemapFace PositiveX { get; set; }
	public Type.CubemapFace PositiveY { get; set; }
	public Type.CubemapFace PositiveZ { get; set; }
	public Type.CubemapFace PositveX { get; set; }
	public Type.CubemapFace PositveY { get; set; }
	public Type.CubemapFace PositveZ { get; set; }
```

## Namespace Android.Runtime

### Type Changed: Android.Runtime.JNIEnv

Added methods:

```
public static bool CallBooleanMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static sbyte CallByteMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static char CallCharMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static double CallDoubleMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static float CallFloatMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static int CallIntMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static long CallLongMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static bool CallNonvirtualBooleanMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static sbyte CallNonvirtualByteMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static char CallNonvirtualCharMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static double CallNonvirtualDoubleMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static float CallNonvirtualFloatMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static int CallNonvirtualIntMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static long CallNonvirtualLongMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static IntPtr CallNonvirtualObjectMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static short CallNonvirtualShortMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static void CallNonvirtualVoidMethod (IntPtr jobject, IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static IntPtr CallObjectMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static short CallShortMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static bool CallStaticBooleanMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static sbyte CallStaticByteMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static char CallStaticCharMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static double CallStaticDoubleMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static float CallStaticFloatMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static int CallStaticIntMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static long CallStaticLongMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static IntPtr CallStaticObjectMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static short CallStaticShortMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static void CallStaticVoidMethod (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static void CallVoidMethod (IntPtr jobject, IntPtr jmethod, JValue* parms);
	public static IntPtr CreateInstance (IntPtr jniClass, string signature, JValue* constructorParameters);
	public static IntPtr CreateInstance (string jniClassName, string signature, JValue* constructorParameters);
	public static IntPtr CreateInstance (System.Type type, string signature, JValue* constructorParameters);
	public static void FinishCreateInstance (IntPtr instance, string jniCtorSignature, JValue* constructorParameters);
	public static void FinishCreateInstance (IntPtr instance, IntPtr jclass, IntPtr constructorId, JValue* constructorParameters);
	public static void InvokeConstructor (IntPtr instance, string jniCtorSignature, JValue* constructorParameters);
	public static IntPtr NewObject (IntPtr jclass, IntPtr jmethod, JValue* parms);
	public static IntPtr StartCreateInstance (IntPtr jclass, IntPtr constructorId, JValue* constructorParameters);
	public static IntPtr StartCreateInstance (System.Type type, string jniCtorSignature, JValue* constructorParameters);
	public static IntPtr StartCreateInstance (string jniClassName, string jniCtorSignature, JValue* constructorParameters);
```

### Type Changed: Android.Runtime.JniHandleOwnership

Added value:

```
DoNotRegister = 16,
```

## Namespace Android.Service.Notification

### Type Changed: Android.Service.Notification.StatusBarNotification

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Speech.Tts

### Type Changed: Android.Speech.Tts.TextToSpeech

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual OperationResult SetEngineByPackageName (string enginePackageName);
	[Obsolete ("deprecated"]
	public virtual OperationResult SetOnUtteranceCompletedListener (TextToSpeech.IOnUtteranceCompletedListener listener);
```

## Namespace Android.Telephony

### Type Changed: Android.Telephony.CellIdentityCdma

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellIdentityGsm

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellIdentityLte

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellIdentityWcdma

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellInfoCdma

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellInfoGsm

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellInfoLte

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellInfoWcdma

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellSignalStrengthCdma

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellSignalStrengthGsm

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellSignalStrengthLte

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.CellSignalStrengthWcdma

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.NeighboringCellInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.PhoneStateListener

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void OnSignalStrengthChanged (int asu);
```

### Type Changed: Android.Telephony.ServiceState

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Telephony.SmsMessage

### Type Changed: Android.Telephony.SmsMessage.MessageClass

Modified properties:

```
public SmsMessage.MessageClass Class0 { get; set; }
	public SmsMessage.MessageClass Class1 { get; set; }
	public SmsMessage.MessageClass Class2 { get; set; }
	public SmsMessage.MessageClass Class3 { get; set; }
	public SmsMessage.MessageClass Unknown { get; set; }
```

### Type Changed: Android.Telephony.TelephonyManager

Modified properties:

```
public string ExtraStateIdle { get; set; }
	public string ExtraStateOffhook { get; set; }
	public string ExtraStateRinging { get; set; }
```

## Namespace Android.Telephony.Gsm

### Type Changed: Android.Telephony.Gsm.SmsManager

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public System.Collections.Generic.IList<string> DivideMessage (string text);
	[Obsolete ("deprecated"]
	public void SendDataMessage (string destinationAddress, string scAddress, short destinationPort, byte[] data, Android.App.PendingIntent sentIntent, Android.App.PendingIntent deliveryIntent);
	[Obsolete ("deprecated"]
	public void SendMultipartTextMessage (string destinationAddress, string scAddress, System.Collections.Generic.IList<string> parts, System.Collections.Generic.IList<Android.App.PendingIntent> sentIntents, System.Collections.Generic.IList<Android.App.PendingIntent> deliveryIntents);
	[Obsolete ("deprecated"]
	public void SendTextMessage (string destinationAddress, string scAddress, string text, Android.App.PendingIntent sentIntent, Android.App.PendingIntent deliveryIntent);
```

### Type Changed: Android.Telephony.Gsm.SmsMessage

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static int[] CalculateLength (Java.Lang.ICharSequence messageBody, bool use7bitOnly);
	[Obsolete ("deprecated"]
	public static int[] CalculateLength (string messageBody, bool use7bitOnly);
	[Obsolete ("deprecated"]
	public static SmsMessage CreateFromPdu (byte[] pdu);
	[Obsolete ("deprecated"]
	public virtual SmsMessage.MessageClass GetMessageClass ();
	[Obsolete ("deprecated"]
	public virtual byte[] GetPdu ();
	[Obsolete ("deprecated"]
	public static SmsMessage.SubmitPdu GetSubmitPdu (string scAddress, string destinationAddress, string message, bool statusReportRequested);
	[Obsolete ("deprecated"]
	public static SmsMessage.SubmitPdu GetSubmitPdu (string scAddress, string destinationAddress, short destinationPort, byte[] data, bool statusReportRequested);
	[Obsolete ("deprecated"]
	public static int GetTPLayerLengthForPDU (string pdu);
	[Obsolete ("deprecated"]
	public virtual byte[] GetUserData ();
```

### Type Changed: Android.Telephony.Gsm.SmsMessage.MessageClass

Modified properties:

```
public SmsMessage.MessageClass Class0 { get; set; }
	public SmsMessage.MessageClass Class1 { get; set; }
	public SmsMessage.MessageClass Class2 { get; set; }
	public SmsMessage.MessageClass Class3 { get; set; }
	public SmsMessage.MessageClass Unknown { get; set; }
```

## Namespace Android.Text

### Type Changed: Android.Text.Layout

### Type Changed: Android.Text.Layout.Alignment

Modified properties:

```
public Layout.Alignment AlignCenter { get; set; }
	public Layout.Alignment AlignNormal { get; set; }
	public Layout.Alignment AlignOpposite { get; set; }
```

### Type Changed: Android.Text.Selection

Modified properties:

```
public Java.Lang.Object SelectionEnd { get; set; }
	public Java.Lang.Object SelectionStart { get; set; }
```

### Type Changed: Android.Text.SpannableStringBuilder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual int GetTextRunCursor (int contextStart, int contextEnd, int flags, int offset, int cursorOpt, Android.Graphics.Paint p);
```

### Type Changed: Android.Text.TextDirectionHeuristics

Modified properties:

```
public ITextDirectionHeuristic AnyrtlLtr { get; set; }
	public ITextDirectionHeuristic FirststrongLtr { get; set; }
	public ITextDirectionHeuristic FirststrongRtl { get; set; }
	public ITextDirectionHeuristic Locale { get; set; }
	public ITextDirectionHeuristic Ltr { get; set; }
	public ITextDirectionHeuristic Rtl { get; set; }
```

### Type Changed: Android.Text.TextUtils

Modified properties:

```
public Android.OS.IParcelableCreator CharSequenceCreator { get; set; }
```

### Type Changed: Android.Text.TextUtils.TruncateAt

Modified properties:

```
public TextUtils.TruncateAt End { get; set; }
	public TextUtils.TruncateAt Marquee { get; set; }
	public TextUtils.TruncateAt Middle { get; set; }
	public TextUtils.TruncateAt Start { get; set; }
```

## Namespace Android.Text.Format

### Type Changed: Android.Text.Format.DateUtils

Modified properties:

```
public System.Collections.Generic.IList<int> SameMonthTable { get; set; }
	public System.Collections.Generic.IList<int> SameYearTable { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static string GetAMPMString (int ampm);
	[Obsolete ("deprecated"]
	public static string GetDayOfWeekString (int dayOfWeek, AbbreviationLength abbrev);
	[Obsolete ("deprecated"]
	public static string GetMonthString (int month, AbbreviationLength abbrev);
```

### Type Changed: Android.Text.Format.Formatter

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static string FormatIpAddress (int ipv4Address);
```

## Namespace Android.Text.Method

### Type Changed: Android.Text.Method.DateKeyListener

Modified properties:

```
public System.Collections.Generic.IList<char> Characters { get; set; }
```

### Type Changed: Android.Text.Method.DateTimeKeyListener

Modified properties:

```
public System.Collections.Generic.IList<char> Characters { get; set; }
```

### Type Changed: Android.Text.Method.DialerKeyListener

Modified properties:

```
public System.Collections.Generic.IList<char> Characters { get; set; }
```

### Type Changed: Android.Text.Method.TextKeyListener

### Type Changed: Android.Text.Method.TextKeyListener.Capitalize

Modified properties:

```
public TextKeyListener.Capitalize Characters { get; set; }
	public TextKeyListener.Capitalize None { get; set; }
	public TextKeyListener.Capitalize Sentences { get; set; }
	public TextKeyListener.Capitalize Words { get; set; }
```

### Type Changed: Android.Text.Method.TimeKeyListener

Modified properties:

```
public System.Collections.Generic.IList<char> Characters { get; set; }
```

## Namespace Android.Text.Style

### Type Changed: Android.Text.Style.SuggestionSpan

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Text.Util

### Type Changed: Android.Text.Util.Linkify

Modified properties:

```
public Linkify.IMatchFilter SPhoneNumberMatchFilter { get; set; }
	public Linkify.ITransformFilter SPhoneNumberTransformFilter { get; set; }
	public Linkify.IMatchFilter SUrlMatchFilter { get; set; }
```

## Namespace Android.Util

### Type Changed: Android.Util.Config

Modified properties:

```
public bool Debug { get; set; }
	public bool Release { get; set; }
```

### Type Changed: Android.Util.JsonToken

Modified properties:

```
public JsonToken BeginArray { get; set; }
	public JsonToken BeginObject { get; set; }
	public JsonToken Boolean { get; set; }
	public JsonToken EndArray { get; set; }
	public JsonToken EndDocument { get; set; }
	public JsonToken EndObject { get; set; }
	public JsonToken Name { get; set; }
	public JsonToken Null { get; set; }
	public JsonToken Number { get; set; }
	public JsonToken String { get; set; }
```

### Type Changed: Android.Util.Patterns

Modified properties:

```
public Java.Util.Regex.Pattern DomainName { get; set; }
	public Java.Util.Regex.Pattern EmailAddress { get; set; }
	public Java.Util.Regex.Pattern IpAddress { get; set; }
	public Java.Util.Regex.Pattern Phone { get; set; }
	public Java.Util.Regex.Pattern TopLevelDomain { get; set; }
	public Java.Util.Regex.Pattern WebUrl { get; set; }
```

### Type Changed: Android.Util.StateSet

Modified properties:

```
public System.Collections.Generic.IList<int> Nothing { get; set; }
	public System.Collections.Generic.IList<int> WildCard { get; set; }
```

### Type Changed: Android.Util.Xml

### Type Changed: Android.Util.Xml.Encoding

Modified properties:

```
public Xml.Encoding Iso88591 { get; set; }
	public Xml.Encoding UsAscii { get; set; }
	public Xml.Encoding Utf16 { get; set; }
	public Xml.Encoding Utf8 { get; set; }
```

## Namespace Android.Views

### Type Changed: Android.Views.AbsSavedState

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
	public AbsSavedState EmptyState { get; set; }
```

### Type Changed: Android.Views.DragEvent

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.InputDevice

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Added method:

```
[Obsolete ("Please use GetMotionRange(Android.Views.Axis)")]
	public InputDevice.MotionRange GetMotionRange (int rangeType);
```

### Type Changed: Android.Views.InputEvent

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.KeyCharacterMap

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual bool GetKeyData (Keycode keyCode, KeyCharacterMap.KeyData results);
```

### Type Changed: Android.Views.KeyEvent

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public bool Dispatch (KeyEvent.ICallback receiver);
	[Obsolete ("deprecated"]
	public virtual bool GetKeyData (KeyCharacterMap.KeyData results);
	[Obsolete ("Please use GetMatch(char[], MetaKeyStates)"]
	public char GetMatch (char[] chars, int metaState);
```

Added method:

```
[Obsolete ("Please use GetUnicodeChar(MetaKeyStates)")]
	public int GetUnicodeChar (int meta);
```

### Type Changed: Android.Views.MotionEvent

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointerCount, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	[Obsolete ("deprecated"]
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointerCount, int[] pointerIds, MotionEvent.PointerCoords[] pointerCoords, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags, InputSourceType source, MotionEventFlags flags);
```

### Type Changed: Android.Views.Surface

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void UnlockCanvas (Android.Graphics.Canvas canvas);
```

### Type Changed: Android.Views.View

Modified properties:

```
protected System.Collections.Generic.IList<int> EmptyStateSet { get; set; }
	protected System.Collections.Generic.IList<int> EnabledFocusedSelectedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> EnabledFocusedSelectedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> EnabledFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> EnabledFocusedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> EnabledSelectedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> EnabledSelectedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> EnabledStateSet { get; set; }
	protected System.Collections.Generic.IList<int> EnabledWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> FocusedSelectedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> FocusedSelectedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> FocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> FocusedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedEnabledFocusedSelectedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedEnabledFocusedSelectedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedEnabledFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedEnabledFocusedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedEnabledSelectedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedEnabledSelectedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedEnabledStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedEnabledWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedFocusedSelectedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedFocusedSelectedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedFocusedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedSelectedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedSelectedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> PressedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> SelectedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> SelectedWindowFocusedStateSet { get; set; }
	protected System.Collections.Generic.IList<int> WindowFocusedStateSet { get; set; }
```

Obsoleted methods:

```
[Obsolete ("Please Use DispatchSystemUiVisibilityChanged(SystemUiFlags)"]
	public void DispatchSystemUiVisibilityChanged (int visibility);
	[Obsolete ("The View.fitsSystemWindows() method was REMOVED by Google in API-16. DO NOT USE."]
	public virtual bool InvokeFitsSystemWindows ();
	[Obsolete ("deprecated"]
	public virtual void SetBackgroundDrawable (Android.Graphics.Drawables.Drawable background);
```

### Type Changed: Android.Views.View.BaseSavedState

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.ViewDebug

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static void StartHierarchyTracing (string prefix, View view);
	[Obsolete ("deprecated"]
	public static void StartRecyclerTracing (string prefix, View view);
	[Obsolete ("deprecated"]
	public static void StopHierarchyTracing ();
	[Obsolete ("deprecated"]
	public static void StopRecyclerTracing ();
	[Obsolete ("deprecated"]
	public static void Trace (View view, ViewDebug.HierarchyTraceType type);
	[Obsolete ("deprecated"]
	public static void Trace (View view, ViewDebug.RecyclerTraceType type, int[] parameters);
```

### Type Changed: Android.Views.ViewDebug.HierarchyTraceType

Modified properties:

```
public ViewDebug.HierarchyTraceType BuildCache { get; set; }
	public ViewDebug.HierarchyTraceType Draw { get; set; }
	public ViewDebug.HierarchyTraceType Invalidate { get; set; }
	public ViewDebug.HierarchyTraceType InvalidateChild { get; set; }
	public ViewDebug.HierarchyTraceType InvalidateChildInParent { get; set; }
	public ViewDebug.HierarchyTraceType OnLayout { get; set; }
	public ViewDebug.HierarchyTraceType OnMeasure { get; set; }
	public ViewDebug.HierarchyTraceType RequestLayout { get; set; }
```

### Type Changed: Android.Views.ViewDebug.RecyclerTraceType

Modified properties:

```
public ViewDebug.RecyclerTraceType BindView { get; set; }
	public ViewDebug.RecyclerTraceType MoveFromActiveToScrapHeap { get; set; }
	public ViewDebug.RecyclerTraceType MoveToActiveHeap { get; set; }
	public ViewDebug.RecyclerTraceType MoveToScrapHeap { get; set; }
	public ViewDebug.RecyclerTraceType NewView { get; set; }
	public ViewDebug.RecyclerTraceType RecycleFromActiveHeap { get; set; }
	public ViewDebug.RecyclerTraceType RecycleFromScrapHeap { get; set; }
```

### Type Changed: Android.Views.ViewTreeObserver

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public void RemoveGlobalOnLayoutListener (ViewTreeObserver.IOnGlobalLayoutListener victim);
```

### Type Changed: Android.Views.WindowId

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.WindowManagerLayoutParams

Added field:

```
public static const int TypeKeyguard;
```

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.WindowManagerTypes

Removed value:

```
Keyguard = 2004,
```

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityEvent

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Added properties:

```
public string BeforeText { get; set; }
	public string ClassName { get; set; }
	public string ContentDescription { get; set; }
```

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Views.InputMethods

### Type Changed: Android.Views.InputMethods.CompletionInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.InputMethods.CorrectionInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.InputMethods.EditorInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.InputMethods.ExtractedText

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.InputMethods.ExtractedTextRequest

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.InputMethods.InputBinding

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.InputMethods.InputMethodInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.InputMethods.InputMethodSubtype

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Android.Views.TextService

### Type Changed: Android.Views.TextService.SentenceSuggestionsInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.TextService.SpellCheckerInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.TextService.SpellCheckerSession

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void GetSuggestions (TextInfo textInfo, int suggestionsLimit);
	[Obsolete ("deprecated"]
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

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.TextService.SuggestionsInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

### Type Changed: Android.Views.TextService.TextInfo

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```



## Namespace Android.Webkit

### Type Changed: Android.Webkit.CacheManager

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static bool CacheDisabled ();
	[Obsolete ("deprecated"]
	public static bool EndCacheTransaction ();
	[Obsolete ("deprecated"]
	public static CacheManager.CacheResult GetCacheFile (string url, System.Collections.Generic.IDictionary<System.String,System.String> headers);
	[Obsolete ("deprecated"]
	public static void SaveCacheFile (string url, CacheManager.CacheResult cacheResult);
	[Obsolete ("deprecated"]
	public static bool StartCacheTransaction ();
```

### Type Changed: Android.Webkit.ConsoleMessage

### Type Changed: Android.Webkit.ConsoleMessage.MessageLevel

Modified properties:

```
public ConsoleMessage.MessageLevel Debug { get; set; }
	public ConsoleMessage.MessageLevel Error { get; set; }
	public ConsoleMessage.MessageLevel Log { get; set; }
	public ConsoleMessage.MessageLevel Tip { get; set; }
	public ConsoleMessage.MessageLevel Warning { get; set; }
```

### Type Changed: Android.Webkit.Plugin

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void DispatchClickEvent (Android.Content.Context context);
```

### Type Changed: Android.Webkit.PluginList

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void AddPlugin (Plugin plugin);
	[Obsolete ("deprecated"]
	public virtual void Clear ();
	[Obsolete ("deprecated"]
	public virtual void PluginClicked (Android.Content.Context context, int position);
	[Obsolete ("deprecated"]
	public virtual void RemovePlugin (Plugin plugin);
```

### Type Changed: Android.Webkit.UrlInterceptRegistry

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static bool RegisterHandler (IUrlInterceptHandler handler);
	[Obsolete ("deprecated"]
	public static void SetUrlInterceptDisabled (bool disabled);
	[Obsolete ("deprecated"]
	public static bool UnregisterHandler (IUrlInterceptHandler handler);
	[Obsolete ("deprecated"]
	public static bool UrlInterceptDisabled ();
```

### Type Changed: Android.Webkit.URLUtil

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static bool IsCookielessProxyUrl (string url);
```

### Type Changed: Android.Webkit.WebChromeClient

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void OnConsoleMessage (string message, int lineNumber, string sourceID);
	[Obsolete ("deprecated"]
	public virtual bool OnJsTimeout ();
	[Obsolete ("deprecated"]
	public virtual void OnShowCustomView (Android.Views.View view, Android.Content.PM.ScreenOrientation requestedOrientation, WebChromeClient.ICustomViewCallback callback);
```

### Type Changed: Android.Webkit.WebSettings

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual bool EnableSmoothTransition ();
	[Obsolete ("deprecated"]
	public virtual WebSettings.PluginState GetPluginState ();
	[Obsolete ("deprecated"]
	public virtual WebSettings.TextSize GetTextSize ();
	[Obsolete ("deprecated"]
	public virtual void SetAppCacheMaxSize (long appCacheMaxSize);
	[Obsolete ("deprecated"]
	public virtual void SetEnableSmoothTransition (bool enable);
	[Obsolete ("deprecated"]
	public virtual void SetPluginState (WebSettings.PluginState state);
	[Obsolete ("deprecated"]
	public virtual void SetRenderPriority (WebSettings.RenderPriority priority);
	[Obsolete ("deprecated"]
	public virtual void SetTextSize (WebSettings.TextSize t);
```

### Type Changed: Android.Webkit.WebSettings.LayoutAlgorithm

Modified properties:

```
public WebSettings.LayoutAlgorithm NarrowColumns { get; set; }
	public WebSettings.LayoutAlgorithm Normal { get; set; }
	public WebSettings.LayoutAlgorithm SingleColumn { get; set; }
```

### Type Changed: Android.Webkit.WebSettings.PluginState

Modified properties:

```
public WebSettings.PluginState Off { get; set; }
	public WebSettings.PluginState On { get; set; }
	public WebSettings.PluginState OnDemand { get; set; }
```

### Type Changed: Android.Webkit.WebSettings.RenderPriority

Modified properties:

```
public WebSettings.RenderPriority High { get; set; }
	public WebSettings.RenderPriority Low { get; set; }
	public WebSettings.RenderPriority Normal { get; set; }
```

### Type Changed: Android.Webkit.WebSettings.TextSize

Modified properties:

```
public WebSettings.TextSize Larger { get; set; }
	public WebSettings.TextSize Largest { get; set; }
	public WebSettings.TextSize Normal { get; set; }
	public WebSettings.TextSize Smaller { get; set; }
	public WebSettings.TextSize Smallest { get; set; }
```

### Type Changed: Android.Webkit.WebSettings.ZoomDensity

Modified properties:

```
public WebSettings.ZoomDensity Close { get; set; }
	public WebSettings.ZoomDensity Far { get; set; }
	public WebSettings.ZoomDensity Medium { get; set; }
```

### Type Changed: Android.Webkit.WebStorage

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void SetQuotaForOrigin (string origin, long quota);
```

### Type Changed: Android.Webkit.WebView

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual bool CanZoomIn ();
	[Obsolete ("deprecated"]
	public virtual bool CanZoomOut ();
	[Obsolete ("deprecated"]
	public virtual void ClearView ();
	[Obsolete ("deprecated"]
	public virtual void DebugDump ();
	[Obsolete ("deprecated"]
	public static void DisablePlatformNotifications ();
	[Obsolete ("deprecated"]
	public virtual void EmulateShiftHeld ();
	[Obsolete ("deprecated"]
	public static void EnablePlatformNotifications ();
	[Obsolete ("deprecated"]
	public virtual int FindAll (string find);
	[Obsolete ("deprecated"]
	public virtual void OnChildViewAdded (Android.Views.View parent, Android.Views.View child);
	[Obsolete ("deprecated"]
	public virtual void OnChildViewRemoved (Android.Views.View p, Android.Views.View child);
	[Obsolete ("deprecated"]
	public virtual void OnGlobalFocusChanged (Android.Views.View oldFocus, Android.Views.View newFocus);
	[Obsolete ("deprecated"]
	public virtual void RefreshPlugins (bool reloadOpenPages);
	[Obsolete ("deprecated"]
	public virtual bool RestorePicture (Android.OS.Bundle b, Java.IO.File src);
	[Obsolete ("deprecated"]
	public virtual void SavePassword (string host, string username, string password);
	[Obsolete ("deprecated"]
	public virtual bool SavePicture (Android.OS.Bundle b, Java.IO.File dest);
	[Obsolete ("deprecated"]
	public virtual void SetMapTrackballToArrowKeys (bool setMap);
	[Obsolete ("deprecated"]
	public virtual void SetPictureListener (WebView.IPictureListener listener);
	[Obsolete ("deprecated"]
	public virtual bool ShowFindDialog (string text, bool showIme);
```

### Type Changed: Android.Webkit.WebViewClient

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void OnTooManyRedirects (WebView view, Android.OS.Message cancelMsg, Android.OS.Message continueMsg);
```

### Type Changed: Android.Webkit.WebViewDatabase

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void ClearUsernamePassword ();
```

## Namespace Android.Widget

### Type Changed: Android.Widget.CursorAdapter

Obsoleted methods:

```
[Obsolete ("deprecated"]
	protected virtual void Init (Android.Content.Context context, Android.Database.ICursor c, bool autoRequery);
```

### Type Changed: Android.Widget.GridLayout

Modified properties:

```
public GridLayout.Alignment BaselineAlighment { get; set; }
	public GridLayout.Alignment BottomAlighment { get; set; }
	public GridLayout.Alignment Center { get; set; }
	public GridLayout.Alignment End { get; set; }
	public GridLayout.Alignment Fill { get; set; }
	public GridLayout.Alignment LeftAlighment { get; set; }
	public GridLayout.Alignment RightAlighment { get; set; }
	public GridLayout.Alignment Start { get; set; }
	public GridLayout.Alignment TopAlighment { get; set; }
```

### Type Changed: Android.Widget.ImageView

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void SetAlpha (int alpha);
```

### Type Changed: Android.Widget.ImageView.ScaleType

Modified properties:

```
public ImageView.ScaleType Center { get; set; }
	public ImageView.ScaleType CenterCrop { get; set; }
	public ImageView.ScaleType CenterInside { get; set; }
	public ImageView.ScaleType FitCenter { get; set; }
	public ImageView.ScaleType FitEnd { get; set; }
	public ImageView.ScaleType FitStart { get; set; }
	public ImageView.ScaleType FitXy { get; set; }
	public ImageView.ScaleType Matrix { get; set; }
```

### Type Changed: Android.Widget.ListView

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual long[] GetCheckItemIds ();
```

### Type Changed: Android.Widget.RemoteViews

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void SetRemoteAdapter (int appWidgetId, int viewId, Android.Content.Intent intent);
```

### Type Changed: Android.Widget.TextClock

Modified properties:

```
public Java.Lang.ICharSequence DefaultFormat12Hour { get; set; }
	public Java.Lang.ICharSequence DefaultFormat24Hour { get; set; }
```

### Type Changed: Android.Widget.TextView

### Type Changed: Android.Widget.TextView.BufferType

Modified properties:

```
public TextView.BufferType Editable { get; set; }
	public TextView.BufferType Normal { get; set; }
	public TextView.BufferType Spannable { get; set; }
```

### Type Changed: Android.Widget.TextView.SavedState

Modified properties:

```
public Android.OS.IParcelableCreator Creator { get; set; }
```

## Namespace Dalvik.Bytecode

### Type Changed: Dalvik.Bytecode.OpcodeInfo

Modified properties:

```
public int MaximumPackedValue { get; set; }
	public int MaximumValue { get; set; }
```

## Namespace Dalvik.SystemInterop

### Type Changed: Dalvik.SystemInterop.VMDebug

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static void StartMethodTracing ();
```

### Type Changed: Dalvik.SystemInterop.Zygote

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static int ForkAndSpecialize (int uid, int gid, int[] gids, bool enableDebugger, int[][] rlimits);
	[Obsolete ("deprecated"]
	public static int ForkSystemServer (int uid, int gid, int[] gids, bool enableDebugger, int[][] rlimits);
```

## Namespace Java.Awt.Font

### Type Changed: Java.Awt.Font.TextAttribute

Modified properties:

```
public TextAttribute Background { get; set; }
	public TextAttribute BidiEmbedding { get; set; }
	public TextAttribute CharReplacement { get; set; }
	public TextAttribute Family { get; set; }
	public TextAttribute Font { get; set; }
	public TextAttribute Foreground { get; set; }
	public TextAttribute InputMethodHighlight { get; set; }
	public TextAttribute InputMethodUnderline { get; set; }
	public TextAttribute Justification { get; set; }
	public Java.Lang.Float JustificationFull { get; set; }
	public Java.Lang.Float JustificationNone { get; set; }
	public TextAttribute Kerning { get; set; }
	public Java.Lang.Integer KerningOn { get; set; }
	public TextAttribute Ligatures { get; set; }
	public Java.Lang.Integer LigaturesOn { get; set; }
	public TextAttribute NumericShaping { get; set; }
	public TextAttribute Posture { get; set; }
	public Java.Lang.Float PostureOblique { get; set; }
	public Java.Lang.Float PostureRegular { get; set; }
	public TextAttribute RunDirection { get; set; }
	public Java.Lang.Boolean RunDirectionLtr { get; set; }
	public Java.Lang.Boolean RunDirectionRtl { get; set; }
	public TextAttribute Size { get; set; }
	public TextAttribute Strikethrough { get; set; }
	public Java.Lang.Boolean StrikethroughOn { get; set; }
	public TextAttribute Superscript { get; set; }
	public Java.Lang.Integer SuperscriptSub { get; set; }
	public Java.Lang.Integer SuperscriptSuper { get; set; }
	public TextAttribute SwapColors { get; set; }
	public Java.Lang.Boolean SwapColorsOn { get; set; }
	public TextAttribute Tracking { get; set; }
	public Java.Lang.Float TrackingLoose { get; set; }
	public Java.Lang.Float TrackingTight { get; set; }
	public TextAttribute Transform { get; set; }
	public TextAttribute Underline { get; set; }
	public Java.Lang.Integer UnderlineLowDashed { get; set; }
	public Java.Lang.Integer UnderlineLowDotted { get; set; }
	public Java.Lang.Integer UnderlineLowGray { get; set; }
	public Java.Lang.Integer UnderlineLowOnePixel { get; set; }
	public Java.Lang.Integer UnderlineLowTwoPixel { get; set; }
	public Java.Lang.Integer UnderlineOn { get; set; }
	public TextAttribute Weight { get; set; }
	public Java.Lang.Float WeightBold { get; set; }
	public Java.Lang.Float WeightDemibold { get; set; }
	public Java.Lang.Float WeightDemilight { get; set; }
	public Java.Lang.Float WeightExtrabold { get; set; }
	public Java.Lang.Float WeightExtraLight { get; set; }
	public Java.Lang.Float WeightHeavy { get; set; }
	public Java.Lang.Float WeightLight { get; set; }
	public Java.Lang.Float WeightMedium { get; set; }
	public Java.Lang.Float WeightRegular { get; set; }
	public Java.Lang.Float WeightSemibold { get; set; }
	public Java.Lang.Float WeightUltrabold { get; set; }
	public TextAttribute Width { get; set; }
	public Java.Lang.Float WidthCondensed { get; set; }
	public Java.Lang.Float WidthExtended { get; set; }
	public Java.Lang.Float WidthRegular { get; set; }
	public Java.Lang.Float WidthSemiCondensed { get; set; }
	public Java.Lang.Float WidthSemiExtended { get; set; }
```

## Namespace Java.IO

### Type Changed: Java.IO.ByteArrayOutputStream

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual string ToString (int hibyte);
```

### Type Changed: Java.IO.DataInputStream

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual string ReadLine ();
```

### Type Changed: Java.IO.File

Modified properties:

```
public string PathSeparator { get; set; }
	public char PathSeparatorChar { get; set; }
	public string Separator { get; set; }
	public char SeparatorChar { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual Java.Net.URL ToURL ();
```

### Type Changed: Java.IO.FileDescriptor

Modified properties:

```
public FileDescriptor Err { get; set; }
	public FileDescriptor In { get; set; }
	public FileDescriptor Out { get; set; }
```

### Type Changed: Java.IO.ObjectInputStream

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual string ReadLine ();
```

### Type Changed: Java.IO.ObjectInputStream.InterfaceConsts

Modified properties:

```
public SerializablePermission SubclassImplementationPermission { get; set; }
	public SerializablePermission SubstitutionPermission { get; set; }
```

### Type Changed: Java.IO.ObjectOutputStream

### Type Changed: Java.IO.ObjectOutputStream.InterfaceConsts

Modified properties:

```
public SerializablePermission SubclassImplementationPermission { get; set; }
	public SerializablePermission SubstitutionPermission { get; set; }
```

### Type Changed: Java.IO.ObjectStreamClass

Modified properties:

```
public System.Collections.Generic.IList<ObjectStreamField> NoFields { get; set; }
```

### Type Changed: Java.IO.ObjectStreamConstants

Modified properties:

```
public SerializablePermission SubclassImplementationPermission { get; set; }
	public SerializablePermission SubstitutionPermission { get; set; }
```

## Namespace Java.Lang

### Type Changed: Java.Lang.Boolean

Modified properties:

```
public Boolean False { get; set; }
	public Boolean True { get; set; }
	public Class Type { get; set; }
```

### Type Changed: Java.Lang.Byte

Modified properties:

```
public Class Type { get; set; }
```

### Type Changed: Java.Lang.Character

Modified properties:

```
public Class Type { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static bool IsJavaLetter (char c);
	[Obsolete ("deprecated"]
	public static bool IsJavaLetterOrDigit (char c);
	[Obsolete ("deprecated"]
	public static bool IsSpace (char c);
```

### Type Changed: Java.Lang.Character.UnicodeBlock

Modified properties:

```
public Character.UnicodeBlock AegeanNumbers { get; set; }
	public Character.UnicodeBlock AlchemicalSymbols { get; set; }
	public Character.UnicodeBlock AlphabeticPresentationForms { get; set; }
	public Character.UnicodeBlock AncientGreekMusicalNotation { get; set; }
	public Character.UnicodeBlock AncientGreekNumbers { get; set; }
	public Character.UnicodeBlock AncientSymbols { get; set; }
	public Character.UnicodeBlock Arabic { get; set; }
	public Character.UnicodeBlock ArabicPresentationFormsA { get; set; }
	public Character.UnicodeBlock ArabicPresentationFormsB { get; set; }
	public Character.UnicodeBlock ArabicSupplement { get; set; }
	public Character.UnicodeBlock Armenian { get; set; }
	public Character.UnicodeBlock Arrows { get; set; }
	public Character.UnicodeBlock Avestan { get; set; }
	public Character.UnicodeBlock Balinese { get; set; }
	public Character.UnicodeBlock Bamum { get; set; }
	public Character.UnicodeBlock BamumSupplement { get; set; }
	public Character.UnicodeBlock BasicLatin { get; set; }
	public Character.UnicodeBlock Batak { get; set; }
	public Character.UnicodeBlock Bengali { get; set; }
	public Character.UnicodeBlock BlockElements { get; set; }
	public Character.UnicodeBlock Bopomofo { get; set; }
	public Character.UnicodeBlock BopomofoExtended { get; set; }
	public Character.UnicodeBlock BoxDrawing { get; set; }
	public Character.UnicodeBlock Brahmi { get; set; }
	public Character.UnicodeBlock BraillePatterns { get; set; }
	public Character.UnicodeBlock Buginese { get; set; }
	public Character.UnicodeBlock Buhid { get; set; }
	public Character.UnicodeBlock ByzantineMusicalSymbols { get; set; }
	public Character.UnicodeBlock Carian { get; set; }
	public Character.UnicodeBlock Cham { get; set; }
	public Character.UnicodeBlock Cherokee { get; set; }
	public Character.UnicodeBlock CjkCompatibility { get; set; }
	public Character.UnicodeBlock CjkCompatibilityForms { get; set; }
	public Character.UnicodeBlock CjkCompatibilityIdeographs { get; set; }
	public Character.UnicodeBlock CjkCompatibilityIdeographsSupplement { get; set; }
	public Character.UnicodeBlock CjkRadicalsSupplement { get; set; }
	public Character.UnicodeBlock CjkStrokes { get; set; }
	public Character.UnicodeBlock CjkSymbolsAndPunctuation { get; set; }
	public Character.UnicodeBlock CjkUnifiedIdeographs { get; set; }
	public Character.UnicodeBlock CjkUnifiedIdeographsExtensionA { get; set; }
	public Character.UnicodeBlock CjkUnifiedIdeographsExtensionB { get; set; }
	public Character.UnicodeBlock CjkUnifiedIdeographsExtensionC { get; set; }
	public Character.UnicodeBlock CjkUnifiedIdeographsExtensionD { get; set; }
	public Character.UnicodeBlock CombiningDiacriticalMarks { get; set; }
	public Character.UnicodeBlock CombiningDiacriticalMarksSupplement { get; set; }
	public Character.UnicodeBlock CombiningHalfMarks { get; set; }
	public Character.UnicodeBlock CombiningMarksForSymbols { get; set; }
	public Character.UnicodeBlock CommonIndicNumberForms { get; set; }
	public Character.UnicodeBlock ControlPictures { get; set; }
	public Character.UnicodeBlock Coptic { get; set; }
	public Character.UnicodeBlock CountingRodNumerals { get; set; }
	public Character.UnicodeBlock Cuneiform { get; set; }
	public Character.UnicodeBlock CuneiformNumbersAndPunctuation { get; set; }
	public Character.UnicodeBlock CurrencySymbols { get; set; }
	public Character.UnicodeBlock CypriotSyllabary { get; set; }
	public Character.UnicodeBlock Cyrillic { get; set; }
	public Character.UnicodeBlock CyrillicExtendedA { get; set; }
	public Character.UnicodeBlock CyrillicExtendedB { get; set; }
	public Character.UnicodeBlock CyrillicSupplementary { get; set; }
	public Character.UnicodeBlock Deseret { get; set; }
	public Character.UnicodeBlock Devanagari { get; set; }
	public Character.UnicodeBlock DevanagariExtended { get; set; }
	public Character.UnicodeBlock Dingbats { get; set; }
	public Character.UnicodeBlock DominoTiles { get; set; }
	public Character.UnicodeBlock EgyptianHieroglyphs { get; set; }
	public Character.UnicodeBlock Emoticons { get; set; }
	public Character.UnicodeBlock EnclosedAlphanumerics { get; set; }
	public Character.UnicodeBlock EnclosedAlphanumericSupplement { get; set; }
	public Character.UnicodeBlock EnclosedCjkLettersAndMonths { get; set; }
	public Character.UnicodeBlock EnclosedIdeographicSupplement { get; set; }
	public Character.UnicodeBlock Ethiopic { get; set; }
	public Character.UnicodeBlock EthiopicExtended { get; set; }
	public Character.UnicodeBlock EthiopicExtendedA { get; set; }
	public Character.UnicodeBlock EthiopicSupplement { get; set; }
	public Character.UnicodeBlock GeneralPunctuation { get; set; }
	public Character.UnicodeBlock GeometricShapes { get; set; }
	public Character.UnicodeBlock Georgian { get; set; }
	public Character.UnicodeBlock GeorgianSupplement { get; set; }
	public Character.UnicodeBlock Glagolitic { get; set; }
	public Character.UnicodeBlock Gothic { get; set; }
	public Character.UnicodeBlock Greek { get; set; }
	public Character.UnicodeBlock GreekExtended { get; set; }
	public Character.UnicodeBlock Gujarati { get; set; }
	public Character.UnicodeBlock Gurmukhi { get; set; }
	public Character.UnicodeBlock HalfwidthAndFullwidthForms { get; set; }
	public Character.UnicodeBlock HangulCompatibilityJamo { get; set; }
	public Character.UnicodeBlock HangulJamo { get; set; }
	public Character.UnicodeBlock HangulJamoExtendedA { get; set; }
	public Character.UnicodeBlock HangulJamoExtendedB { get; set; }
	public Character.UnicodeBlock HangulSyllables { get; set; }
	public Character.UnicodeBlock Hanunoo { get; set; }
	public Character.UnicodeBlock Hebrew { get; set; }
	public Character.UnicodeBlock HighPrivateUseSurrogates { get; set; }
	public Character.UnicodeBlock HighSurrogates { get; set; }
	public Character.UnicodeBlock Hiragana { get; set; }
	public Character.UnicodeBlock IdeographicDescriptionCharacters { get; set; }
	public Character.UnicodeBlock ImperialAramaic { get; set; }
	public Character.UnicodeBlock InscriptionalPahlavi { get; set; }
	public Character.UnicodeBlock InscriptionalParthian { get; set; }
	public Character.UnicodeBlock IpaExtensions { get; set; }
	public Character.UnicodeBlock Javanese { get; set; }
	public Character.UnicodeBlock Kaithi { get; set; }
	public Character.UnicodeBlock KanaSupplement { get; set; }
	public Character.UnicodeBlock Kanbun { get; set; }
	public Character.UnicodeBlock KangxiRadicals { get; set; }
	public Character.UnicodeBlock Kannada { get; set; }
	public Character.UnicodeBlock Katakana { get; set; }
	public Character.UnicodeBlock KatakanaPhoneticExtensions { get; set; }
	public Character.UnicodeBlock KayahLi { get; set; }
	public Character.UnicodeBlock Kharoshthi { get; set; }
	public Character.UnicodeBlock Khmer { get; set; }
	public Character.UnicodeBlock KhmerSymbols { get; set; }
	public Character.UnicodeBlock Lao { get; set; }
	public Character.UnicodeBlock Latin1Supplement { get; set; }
	public Character.UnicodeBlock LatinExtendedA { get; set; }
	public Character.UnicodeBlock LatinExtendedAdditional { get; set; }
	public Character.UnicodeBlock LatinExtendedB { get; set; }
	public Character.UnicodeBlock LatinExtendedC { get; set; }
	public Character.UnicodeBlock LatinExtendedD { get; set; }
	public Character.UnicodeBlock Lepcha { get; set; }
	public Character.UnicodeBlock LetterlikeSymbols { get; set; }
	public Character.UnicodeBlock Limbu { get; set; }
	public Character.UnicodeBlock LinearBIdeograms { get; set; }
	public Character.UnicodeBlock LinearBSyllabary { get; set; }
	public Character.UnicodeBlock Lisu { get; set; }
	public Character.UnicodeBlock LowSurrogates { get; set; }
	public Character.UnicodeBlock Lycian { get; set; }
	public Character.UnicodeBlock Lydian { get; set; }
	public Character.UnicodeBlock MahjongTiles { get; set; }
	public Character.UnicodeBlock Malayalam { get; set; }
	public Character.UnicodeBlock Mandaic { get; set; }
	public Character.UnicodeBlock MathematicalAlphanumericSymbols { get; set; }
	public Character.UnicodeBlock MathematicalOperators { get; set; }
	public Character.UnicodeBlock MeeteiMayek { get; set; }
	public Character.UnicodeBlock MiscellaneousMathematicalSymbolsA { get; set; }
	public Character.UnicodeBlock MiscellaneousMathematicalSymbolsB { get; set; }
	public Character.UnicodeBlock MiscellaneousSymbols { get; set; }
	public Character.UnicodeBlock MiscellaneousSymbolsAndArrows { get; set; }
	public Character.UnicodeBlock MiscellaneousSymbolsAndPictographs { get; set; }
	public Character.UnicodeBlock MiscellaneousTechnical { get; set; }
	public Character.UnicodeBlock ModifierToneLetters { get; set; }
	public Character.UnicodeBlock Mongolian { get; set; }
	public Character.UnicodeBlock MusicalSymbols { get; set; }
	public Character.UnicodeBlock Myanmar { get; set; }
	public Character.UnicodeBlock MyanmarExtendedA { get; set; }
	public Character.UnicodeBlock NewTaiLue { get; set; }
	public Character.UnicodeBlock Nko { get; set; }
	public Character.UnicodeBlock NumberForms { get; set; }
	public Character.UnicodeBlock Ogham { get; set; }
	public Character.UnicodeBlock OlChiki { get; set; }
	public Character.UnicodeBlock OldItalic { get; set; }
	public Character.UnicodeBlock OldPersian { get; set; }
	public Character.UnicodeBlock OldSouthArabian { get; set; }
	public Character.UnicodeBlock OldTurkic { get; set; }
	public Character.UnicodeBlock OpticalCharacterRecognition { get; set; }
	public Character.UnicodeBlock Oriya { get; set; }
	public Character.UnicodeBlock Osmanya { get; set; }
	public Character.UnicodeBlock PhagsPa { get; set; }
	public Character.UnicodeBlock PhaistosDisc { get; set; }
	public Character.UnicodeBlock Phoenician { get; set; }
	public Character.UnicodeBlock PhoneticExtensions { get; set; }
	public Character.UnicodeBlock PhoneticExtensionsSupplement { get; set; }
	public Character.UnicodeBlock PlayingCards { get; set; }
	public Character.UnicodeBlock PrivateUseArea { get; set; }
	public Character.UnicodeBlock Rejang { get; set; }
	public Character.UnicodeBlock RumiNumeralSymbols { get; set; }
	public Character.UnicodeBlock Runic { get; set; }
	public Character.UnicodeBlock Samaritan { get; set; }
	public Character.UnicodeBlock Saurashtra { get; set; }
	public Character.UnicodeBlock Shavian { get; set; }
	public Character.UnicodeBlock Sinhala { get; set; }
	public Character.UnicodeBlock SmallFormVariants { get; set; }
	public Character.UnicodeBlock SpacingModifierLetters { get; set; }
	public Character.UnicodeBlock Specials { get; set; }
	public Character.UnicodeBlock Sundanese { get; set; }
	public Character.UnicodeBlock SuperscriptsAndSubscripts { get; set; }
	public Character.UnicodeBlock SupplementalArrowsA { get; set; }
	public Character.UnicodeBlock SupplementalArrowsB { get; set; }
	public Character.UnicodeBlock SupplementalMathematicalOperators { get; set; }
	public Character.UnicodeBlock SupplementalPunctuation { get; set; }
	public Character.UnicodeBlock SupplementaryPrivateUseAreaA { get; set; }
	public Character.UnicodeBlock SupplementaryPrivateUseAreaB { get; set; }
	public Character.UnicodeBlock SurrogatesArea { get; set; }
	public Character.UnicodeBlock SylotiNagri { get; set; }
	public Character.UnicodeBlock Syriac { get; set; }
	public Character.UnicodeBlock Tagalog { get; set; }
	public Character.UnicodeBlock Tagbanwa { get; set; }
	public Character.UnicodeBlock Tags { get; set; }
	public Character.UnicodeBlock TaiLe { get; set; }
	public Character.UnicodeBlock TaiTham { get; set; }
	public Character.UnicodeBlock TaiViet { get; set; }
	public Character.UnicodeBlock TaiXuanJingSymbols { get; set; }
	public Character.UnicodeBlock Tamil { get; set; }
	public Character.UnicodeBlock Telugu { get; set; }
	public Character.UnicodeBlock Thaana { get; set; }
	public Character.UnicodeBlock Thai { get; set; }
	public Character.UnicodeBlock Tibetan { get; set; }
	public Character.UnicodeBlock Tifinagh { get; set; }
	public Character.UnicodeBlock TransportAndMapSymbols { get; set; }
	public Character.UnicodeBlock Ugaritic { get; set; }
	public Character.UnicodeBlock UnifiedCanadianAboriginalSyllabics { get; set; }
	public Character.UnicodeBlock UnifiedCanadianAboriginalSyllabicsExtended { get; set; }
	public Character.UnicodeBlock Vai { get; set; }
	public Character.UnicodeBlock VariationSelectors { get; set; }
	public Character.UnicodeBlock VariationSelectorsSupplement { get; set; }
	public Character.UnicodeBlock VedicExtensions { get; set; }
	public Character.UnicodeBlock VerticalForms { get; set; }
	public Character.UnicodeBlock YijingHexagramSymbols { get; set; }
	public Character.UnicodeBlock YiRadicals { get; set; }
	public Character.UnicodeBlock YiSyllables { get; set; }
```

### Type Changed: Java.Lang.ClassLoader

Obsoleted methods:

```
[Obsolete ("deprecated"]
	protected Class DefineClass (byte[] classRep, int offset, int length);
```

### Type Changed: Java.Lang.ClassNotFoundException

Added property:

```
[Obsolete ("Use the Cause property. The Clause property was bound in error, and DOES NOT EXIST.")]
	public virtual Throwable Clause { get; }
```

### Type Changed: Java.Lang.Double

Modified properties:

```
public int MaxExponent { get; set; }
	public int MinExponent { get; set; }
	public double MinNormal { get; set; }
	public Class Type { get; set; }
```

### Type Changed: Java.Lang.Exception

Obsoleted constructors:

```
[Obsolete ("This member does not exist on Android. It was erroneously bound."]
	protected Exception (string p0, Throwable p1, bool p2, bool p3);
```

### Type Changed: Java.Lang.Float

Modified properties:

```
public int MaxExponent { get; set; }
	public int MinExponent { get; set; }
	public float MinNormal { get; set; }
	public Class Type { get; set; }
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

Modified properties:

```
public Class Type { get; set; }
```

### Type Changed: Java.Lang.JavaSystem

Modified properties:

```
public Java.IO.PrintStream Err { get; set; }
	public System.IO.Stream In { get; set; }
	public Java.IO.PrintStream Out { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static void RunFinalizersOnExit (bool flag);
```

### Type Changed: Java.Lang.Long

Modified properties:

```
public Class Type { get; set; }
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
[Obsolete ("deprecated"]
	public virtual System.IO.Stream GetLocalizedInputStream (System.IO.Stream stream);
	[Obsolete ("deprecated"]
	public virtual System.IO.Stream GetLocalizedOutputStream (System.IO.Stream stream);
	[Obsolete ("deprecated"]
	public static void RunFinalizersOnExit (bool run);
```

### Type Changed: Java.Lang.RuntimeException

Obsoleted constructors:

```
[Obsolete ("This member does not exist on Android. It was erroneously bound."]
	protected RuntimeException (string p0, Throwable p1, bool p2, bool p3);
```

### Type Changed: Java.Lang.SecurityManager

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void CheckMulticast (Java.Net.InetAddress maddr, sbyte ttl);
	[Obsolete ("deprecated"]
	protected virtual int ClassDepth (string name);
	[Obsolete ("deprecated"]
	protected virtual int ClassLoaderDepth ();
	[Obsolete ("deprecated"]
	protected virtual ClassLoader CurrentClassLoader ();
	[Obsolete ("deprecated"]
	protected virtual Class CurrentLoadedClass ();
	[Obsolete ("deprecated"]
	protected virtual bool InClass (string name);
	[Obsolete ("deprecated"]
	protected virtual bool InClassLoader ();
```

### Type Changed: Java.Lang.Short

Modified properties:

```
public Class Type { get; set; }
```

### Type Changed: Java.Lang.String

Modified properties:

```
public Java.Util.IComparator CaseInsensitiveOrder { get; set; }
```

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public void GetBytes (int start, int end, byte[] data, int index);
```

### Type Changed: Java.Lang.Thread

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual int CountStackFrames ();
	[Obsolete ("deprecated"]
	public virtual void Destroy ();
	[Obsolete ("deprecated"]
	public void Resume ();
	[Obsolete ("deprecated"]
	public void Stop ();
	[Obsolete ("deprecated"]
	public void Stop (Throwable throwable);
	[Obsolete ("deprecated"]
	public void Suspend ();
```

### Type Changed: Java.Lang.Thread.State

Modified properties:

```
public Thread.State Blocked { get; set; }
	public Thread.State New { get; set; }
	public Thread.State Runnable { get; set; }
	public Thread.State Terminated { get; set; }
	public Thread.State TimedWaiting { get; set; }
	public Thread.State Waiting { get; set; }
```

### Type Changed: Java.Lang.ThreadGroup

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual bool AllowThreadSuspension (bool b);
	[Obsolete ("deprecated"]
	public void Resume ();
	[Obsolete ("deprecated"]
	public void Stop ();
	[Obsolete ("deprecated"]
	public void Suspend ();
```

### Type Changed: Java.Lang.Void

Modified properties:

```
public Class Type { get; set; }
```

## Namespace Java.Lang.Annotation

### Type Changed: Java.Lang.Annotation.ElementType

Modified properties:

```
public ElementType AnnotationType { get; set; }
	public ElementType Constructor { get; set; }
	public ElementType Field { get; set; }
	public ElementType LocalVariable { get; set; }
	public ElementType Method { get; set; }
	public ElementType Package { get; set; }
	public ElementType Parameter { get; set; }
	public ElementType Type { get; set; }
```

### Type Changed: Java.Lang.Annotation.RetentionPolicy

Modified properties:

```
public RetentionPolicy Runtime { get; set; }
	public RetentionPolicy Source { get; set; }
```

## Namespace Java.Lang.Reflect

### Type Changed: Java.Lang.Reflect.InvocationTargetException

Added property:

```
[Obsolete ("Use the Cause property. The Clause property was bound in error, and DOES NOT EXIST.")]
	public virtual Java.Lang.Throwable Clause { get; }
```

## Namespace Java.Math

### Type Changed: Java.Math.BigDecimal

Modified properties:

```
public BigDecimal One { get; set; }
	public BigDecimal Ten { get; set; }
	public BigDecimal Zero { get; set; }
```

### Type Changed: Java.Math.BigInteger

Modified properties:

```
public BigInteger One { get; set; }
	public BigInteger Ten { get; set; }
	public BigInteger Zero { get; set; }
```

### Type Changed: Java.Math.MathContext

Modified properties:

```
public MathContext Decimal128 { get; set; }
	public MathContext Decimal32 { get; set; }
	public MathContext Decimal64 { get; set; }
	public MathContext Unlimited { get; set; }
```

### Type Changed: Java.Math.RoundingMode

Modified properties:

```
public RoundingMode Ceiling { get; set; }
	public RoundingMode Down { get; set; }
	public RoundingMode Floor { get; set; }
	public RoundingMode HalfDown { get; set; }
	public RoundingMode HalfEven { get; set; }
	public RoundingMode HalfUp { get; set; }
	public RoundingMode Unnecessary { get; set; }
	public RoundingMode Up { get; set; }
```

## Namespace Java.Net

### Type Changed: Java.Net.Authenticator

### Type Changed: Java.Net.Authenticator.RequestorType

Modified properties:

```
public Authenticator.RequestorType Proxy { get; set; }
	public Authenticator.RequestorType Server { get; set; }
```

### Type Changed: Java.Net.CookiePolicy

Modified properties:

```
public ICookiePolicy AcceptAll { get; set; }
	public ICookiePolicy AcceptNone { get; set; }
	public ICookiePolicy AcceptOriginalServer { get; set; }
```

### Type Changed: Java.Net.MulticastSocket

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void Send (DatagramPacket packet, sbyte ttl);
```

### Type Changed: Java.Net.Proxy

Modified properties:

```
public Proxy NoProxy { get; set; }
```

### Type Changed: Java.Net.Proxy.Type

Modified properties:

```
public Proxy.Type Direct { get; set; }
	public Proxy.Type Http { get; set; }
	public Proxy.Type Socks { get; set; }
```

### Type Changed: Java.Net.URLConnection

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static string GetDefaultRequestProperty (string field);
	[Obsolete ("deprecated"]
	public static void SetDefaultRequestProperty (string field, string value);
```

### Type Changed: Java.Net.URLDecoder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static string Decode (string s);
```

### Type Changed: Java.Net.URLEncoder

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static string Encode (string s);
```

### Type Changed: Java.Net.URLStreamHandler

Obsoleted methods:

```
[Obsolete ("deprecated"]
	protected virtual void SetURL (URL u, string protocol, string host, int port, string file, string ref);
```

## Namespace Java.Nio

### Type Changed: Java.Nio.ByteOrder

Modified properties:

```
public ByteOrder BigEndian { get; set; }
	public ByteOrder LittleEndian { get; set; }
```

## Namespace Java.Nio.Channels

### Type Changed: Java.Nio.Channels.FileChannel

### Type Changed: Java.Nio.Channels.FileChannel.MapMode

Modified properties:

```
public FileChannel.MapMode Private { get; set; }
	public FileChannel.MapMode ReadOnly { get; set; }
	public FileChannel.MapMode ReadWrite { get; set; }
```

## Namespace Java.Nio.Charset

### Type Changed: Java.Nio.Charset.CoderResult

Modified properties:

```
public CoderResult Overflow { get; set; }
	public CoderResult Underflow { get; set; }
```

### Type Changed: Java.Nio.Charset.CodingErrorAction

Modified properties:

```
public CodingErrorAction Ignore { get; set; }
	public CodingErrorAction Replace { get; set; }
	public CodingErrorAction Report { get; set; }
```

## Namespace Java.Security

### Type Changed: Java.Security.KeyRep

### Type Changed: Java.Security.KeyRep.Type

Modified properties:

```
public KeyRep.Type Private { get; set; }
	public KeyRep.Type Public { get; set; }
	public KeyRep.Type Secret { get; set; }
```

### Type Changed: Java.Security.Policy

Modified properties:

```
public PermissionCollection UnsupportedEmptyCollection { get; set; }
```

### Type Changed: Java.Security.Security

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public static string GetAlgorithmProperty (string algName, string propName);
```

### Type Changed: Java.Security.Signature

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public Java.Lang.Object GetParameter (string param);
	[Obsolete ("deprecated"]
	public void SetParameter (string param, Java.Lang.Object value);
```

## Namespace Java.Security.Spec

### Type Changed: Java.Security.Spec.ECPoint

Modified properties:

```
public ECPoint PointInfinity { get; set; }
```

### Type Changed: Java.Security.Spec.MGF1ParameterSpec

Modified properties:

```
public MGF1ParameterSpec Sha1 { get; set; }
	public MGF1ParameterSpec Sha256 { get; set; }
	public MGF1ParameterSpec Sha384 { get; set; }
	public MGF1ParameterSpec Sha512 { get; set; }
```

### Type Changed: Java.Security.Spec.PSSParameterSpec

Modified properties:

```
public PSSParameterSpec Default { get; set; }
```

### Type Changed: Java.Security.Spec.RSAKeyGenParameterSpec

Modified properties:

```
public Java.Math.BigInteger F0 { get; set; }
	public Java.Math.BigInteger F4 { get; set; }
```

## Namespace Java.Sql

### Type Changed: Java.Sql.ClientInfoStatus

Modified properties:

```
public ClientInfoStatus ReasonUnknown { get; set; }
	public ClientInfoStatus ReasonUnknownProperty { get; set; }
	public ClientInfoStatus ReasonValueInvalid { get; set; }
	public ClientInfoStatus ReasonValueTruncated { get; set; }
```

### Type Changed: Java.Sql.DatabaseMetaData

Modified properties:

```
public int FunctionColumnIn { get; set; }
	public int FunctionColumnInOut { get; set; }
	public int FunctionColumnOut { get; set; }
	public int FunctionColumnResult { get; set; }
	public int FunctionColumnUnknown { get; set; }
	public int FunctionNoNulls { get; set; }
	public int FunctionNoTable { get; set; }
	public int FunctionNullable { get; set; }
	public int FunctionNullableUnknown { get; set; }
	public int FunctionResultUnknown { get; set; }
	public int FunctionReturn { get; set; }
	public int FunctionReturnsTable { get; set; }
	public int SqlStateSQL { get; set; }
```

### Type Changed: Java.Sql.RowIdLifetime

Modified properties:

```
public RowIdLifetime RowidUnsupported { get; set; }
	public RowIdLifetime RowidValidForever { get; set; }
	public RowIdLifetime RowidValidOther { get; set; }
	public RowIdLifetime RowidValidSession { get; set; }
	public RowIdLifetime RowidValidTransaction { get; set; }
```

### Type Changed: Java.Sql.Types

Modified properties:

```
public int Longnvarchar { get; set; }
	public int Nchar { get; set; }
	public int Nclob { get; set; }
	public int Nvarchar { get; set; }
	public int Rowid { get; set; }
	public int Sqlxml { get; set; }
```

## Namespace Java.Text

### Type Changed: Java.Text.AttributedCharacterIteratorAttribute

Modified properties:

```
public AttributedCharacterIteratorAttribute InputMethodSegment { get; set; }
	public AttributedCharacterIteratorAttribute Language { get; set; }
	public AttributedCharacterIteratorAttribute Reading { get; set; }
```

### Type Changed: Java.Text.DateFormat

### Type Changed: Java.Text.DateFormat.Field

Modified properties:

```
public DateFormat.Field AmPm { get; set; }
	public DateFormat.Field DayOfMonth { get; set; }
	public DateFormat.Field DayOfWeek { get; set; }
	public DateFormat.Field DayOfWeekInMonth { get; set; }
	public DateFormat.Field DayOfYear { get; set; }
	public DateFormat.Field Era { get; set; }
	public DateFormat.Field Hour0 { get; set; }
	public DateFormat.Field Hour1 { get; set; }
	public DateFormat.Field HourOfDay0 { get; set; }
	public DateFormat.Field HourOfDay1 { get; set; }
	public DateFormat.Field Millisecond { get; set; }
	public DateFormat.Field Minute { get; set; }
	public DateFormat.Field Month { get; set; }
	public DateFormat.Field Second { get; set; }
	public DateFormat.Field TimeZone { get; set; }
	public DateFormat.Field WeekOfMonth { get; set; }
	public DateFormat.Field WeekOfYear { get; set; }
	public DateFormat.Field Year { get; set; }
```

### Type Changed: Java.Text.MessageFormat

### Type Changed: Java.Text.MessageFormat.Field

Modified properties:

```
public MessageFormat.Field Argument { get; set; }
```

### Type Changed: Java.Text.Normalizer

### Type Changed: Java.Text.Normalizer.Form

Modified properties:

```
public Normalizer.Form Nfc { get; set; }
	public Normalizer.Form Nfd { get; set; }
	public Normalizer.Form Nfkc { get; set; }
	public Normalizer.Form Nfkd { get; set; }
```

### Type Changed: Java.Text.NumberFormat

### Type Changed: Java.Text.NumberFormat.Field

Modified properties:

```
public NumberFormat.Field Currency { get; set; }
	public NumberFormat.Field DecimalSeparator { get; set; }
	public NumberFormat.Field Exponent { get; set; }
	public NumberFormat.Field ExponentSign { get; set; }
	public NumberFormat.Field ExponentSymbol { get; set; }
	public NumberFormat.Field Fraction { get; set; }
	public NumberFormat.Field GroupingSeparator { get; set; }
	public NumberFormat.Field Integer { get; set; }
	public NumberFormat.Field Percent { get; set; }
	public NumberFormat.Field Permille { get; set; }
	public NumberFormat.Field Sign { get; set; }
```

## Namespace Java.Util

### Type Changed: Java.Util.Calendar

Modified properties:

```
public CalendarStyle AllStyles { get; set; }
	public CalendarStyle Long { get; set; }
	public CalendarStyle Short { get; set; }
```

### Type Changed: Java.Util.Date

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual int GetDate ();
	[Obsolete ("deprecated"]
	public static long Parse (string string);
	[Obsolete ("deprecated"]
	public virtual void SetDate (int day);
	[Obsolete ("deprecated"]
	public virtual string ToGMTString ();
	[Obsolete ("deprecated"]
	public virtual string ToLocaleString ();
	[Obsolete ("deprecated"]
	public static long UTC (int year, int month, int day, int hour, int minute, int second);
```

### Type Changed: Java.Util.Formatter

### Type Changed: Java.Util.Formatter.BigDecimalLayoutForm

Modified properties:

```
public Formatter.BigDecimalLayoutForm DecimalFloat { get; set; }
	public Formatter.BigDecimalLayoutForm Scientific { get; set; }
```

### Type Changed: Java.Util.Locale

Modified properties:

```
public Locale Canada { get; set; }
	public Locale CanadaFrench { get; set; }
	public Locale China { get; set; }
	public Locale Chinese { get; set; }
	public Locale English { get; set; }
	public Locale France { get; set; }
	public Locale French { get; set; }
	public Locale German { get; set; }
	public Locale Germany { get; set; }
	public Locale Italian { get; set; }
	public Locale Italy { get; set; }
	public Locale Japan { get; set; }
	public Locale Japanese { get; set; }
	public Locale Korea { get; set; }
	public Locale Korean { get; set; }
	public Locale Prc { get; set; }
	public char PrivateUseExtension { get; set; }
	public Locale Root { get; set; }
	public Locale SimplifiedChinese { get; set; }
	public Locale Taiwan { get; set; }
	public Locale TraditionalChinese { get; set; }
	public Locale Uk { get; set; }
	public char UnicodeLocaleExtension { get; set; }
	public Locale Us { get; set; }
```

### Type Changed: Java.Util.Properties

Obsoleted methods:

```
[Obsolete ("deprecated"]
	public virtual void Save (System.IO.Stream out, string comment);
```

### Type Changed: Java.Util.ResourceBundle

### Type Changed: Java.Util.ResourceBundle.Control

Modified properties:

```
public System.Collections.IList FormatClass { get; set; }
	public System.Collections.IList FormatDefault { get; set; }
	public System.Collections.IList FormatProperties { get; set; }
```

## Namespace Java.Util.Concurrent

### Type Changed: Java.Util.Concurrent.TimeUnit

Modified properties:

```
public TimeUnit Days { get; set; }
	public TimeUnit Hours { get; set; }
	public TimeUnit Microseconds { get; set; }
	public TimeUnit Milliseconds { get; set; }
	public TimeUnit Minutes { get; set; }
	public TimeUnit Nanoseconds { get; set; }
	public TimeUnit Seconds { get; set; }
```

## Namespace Java.Util.Jar

### Type Changed: Java.Util.Jar.Attributes

### Type Changed: Java.Util.Jar.Attributes.Name

Modified properties:

```
public Attributes.Name ClassPath { get; set; }
	public Attributes.Name ContentType { get; set; }
	public Attributes.Name ExtensionInstallation { get; set; }
	public Attributes.Name ExtensionList { get; set; }
	public Attributes.Name ExtensionName { get; set; }
	public Attributes.Name ImplementationTitle { get; set; }
	public Attributes.Name ImplementationUrl { get; set; }
	public Attributes.Name ImplementationVendor { get; set; }
	public Attributes.Name ImplementationVendorId { get; set; }
	public Attributes.Name ImplementationVersion { get; set; }
	public Attributes.Name MainClass { get; set; }
	public Attributes.Name ManifestVersion { get; set; }
	public Attributes.Name Sealed { get; set; }
	public Attributes.Name SignatureVersion { get; set; }
	public Attributes.Name SpecificationTitle { get; set; }
	public Attributes.Name SpecificationVendor { get; set; }
	public Attributes.Name SpecificationVersion { get; set; }
```

## Namespace Java.Util.Logging

### Type Changed: Java.Util.Logging.Level

Modified properties:

```
public Level All { get; set; }
	public Level Config { get; set; }
	public Level Fine { get; set; }
	public Level Finer { get; set; }
	public Level Finest { get; set; }
	public Level Info { get; set; }
	public Level Off { get; set; }
	public Level Severe { get; set; }
	public Level Warning { get; set; }
```

### Type Changed: Java.Util.Logging.Logger

Modified properties:

```
public string GlobalLoggerName { get; set; }
```

## Namespace Java.Util.Regex

### Type Changed: Java.Util.Regex.Pattern

Modified properties:

```
public int UnicodeCharacterClass { get; set; }
```

## Namespace Java.Util.Zip

### Type Changed: Java.Util.Zip.Deflater

Modified properties:

```
public int FullFlush { get; set; }
	public int NoFlush { get; set; }
	public int SyncFlush { get; set; }
```

## Namespace Javax.Crypto.Spec

### Type Changed: Javax.Crypto.Spec.OAEPParameterSpec

Modified properties:

```
public OAEPParameterSpec Default { get; set; }
```

### Type Changed: Javax.Crypto.Spec.PSource

### Type Changed: Javax.Crypto.Spec.PSource.PSpecified

Modified properties:

```
public PSource.PSpecified Default { get; set; }
```

## Namespace Javax.Microedition.Khronos.Egl

### Type Changed: Javax.Microedition.Khronos.Egl.EGL10

Modified properties:

```
public Java.Lang.Object EglDefaultDisplay { get; set; }
	public EGLContext EglNoContext { get; set; }
	public EGLDisplay EglNoDisplay { get; set; }
	public EGLSurface EglNoSurface { get; set; }
```

### Type Changed: Javax.Microedition.Khronos.Egl.EGL11

Modified properties:

```
public Java.Lang.Object EglDefaultDisplay { get; set; }
	public EGLContext EglNoContext { get; set; }
	public EGLDisplay EglNoDisplay { get; set; }
	public EGLSurface EglNoSurface { get; set; }
```

## Namespace Javax.Net.Ssl

### Type Changed: Javax.Net.Ssl.SSLEngineResult

### Type Changed: Javax.Net.Ssl.SSLEngineResult.HandshakeStatus

Modified properties:

```
public SSLEngineResult.HandshakeStatus Finished { get; set; }
	public SSLEngineResult.HandshakeStatus NeedTask { get; set; }
	public SSLEngineResult.HandshakeStatus NeedUnwrap { get; set; }
	public SSLEngineResult.HandshakeStatus NeedWrap { get; set; }
	public SSLEngineResult.HandshakeStatus NotHandshaking { get; set; }
```

### Type Changed: Javax.Net.Ssl.SSLEngineResult.Status

Modified properties:

```
public SSLEngineResult.Status BufferOverflow { get; set; }
	public SSLEngineResult.Status BufferUnderflow { get; set; }
	public SSLEngineResult.Status Closed { get; set; }
	public SSLEngineResult.Status Ok { get; set; }
```

## Namespace Javax.Xml.Datatype

### Type Changed: Javax.Xml.Datatype.DatatypeConstants

Modified properties:

```
public Javax.Xml.Namespace.QName Date { get; set; }
	public Javax.Xml.Namespace.QName Datetime { get; set; }
	public DatatypeConstants.Field Days { get; set; }
	public Javax.Xml.Namespace.QName Duration { get; set; }
	public Javax.Xml.Namespace.QName DurationDaytime { get; set; }
	public Javax.Xml.Namespace.QName DurationYearmonth { get; set; }
	public Javax.Xml.Namespace.QName Gday { get; set; }
	public Javax.Xml.Namespace.QName Gmonth { get; set; }
	public Javax.Xml.Namespace.QName Gmonthday { get; set; }
	public Javax.Xml.Namespace.QName Gyear { get; set; }
	public Javax.Xml.Namespace.QName Gyearmonth { get; set; }
	public DatatypeConstants.Field Hours { get; set; }
	public DatatypeConstants.Field Minutes { get; set; }
	public DatatypeConstants.Field Months { get; set; }
	public DatatypeConstants.Field Seconds { get; set; }
	public Javax.Xml.Namespace.QName Time { get; set; }
	public DatatypeConstants.Field Years { get; set; }
```

### Type Changed: Javax.Xml.Datatype.DatatypeFactory

Modified properties:

```
public string DatatypefactoryImplementationClass { get; set; }
```

## Namespace Javax.Xml.Xpath

### Type Changed: Javax.Xml.Xpath.XPathConstants

Modified properties:

```
public Javax.Xml.Namespace.QName Boolean { get; set; }
	public Javax.Xml.Namespace.QName Node { get; set; }
	public Javax.Xml.Namespace.QName Nodeset { get; set; }
	public Javax.Xml.Namespace.QName Number { get; set; }
	public Javax.Xml.Namespace.QName String { get; set; }
```

## Namespace Org.Apache.Http

### Type Changed: Org.Apache.Http.HttpVersion

Modified properties:

```
public HttpVersion Http09 { get; set; }
	public HttpVersion Http10 { get; set; }
	public HttpVersion Http11 { get; set; }
```

## Namespace Org.Apache.Http.Authentication

### Type Changed: Org.Apache.Http.Authentication.AuthScope

Modified properties:

```
public AuthScope Any { get; set; }
	public string AnyHost { get; set; }
	public string AnyRealm { get; set; }
	public string AnyScheme { get; set; }
```

## Namespace Org.Apache.Http.Conn.Params

### Type Changed: Org.Apache.Http.Conn.Params.ConnRouteParams

Modified properties:

```
public Org.Apache.Http.HttpHost NoHost { get; set; }
	public Org.Apache.Http.Conn.Routing.HttpRoute NoRoute { get; set; }
```

## Namespace Org.Apache.Http.Conn.Routing

### Type Changed: Org.Apache.Http.Conn.Routing.RouteInfoLayerType

Modified properties:

```
public RouteInfoLayerType Layered { get; set; }
	public RouteInfoLayerType Plain { get; set; }
```

### Type Changed: Org.Apache.Http.Conn.Routing.RouteInfoTunnelType

Modified properties:

```
public RouteInfoTunnelType Plain { get; set; }
	public RouteInfoTunnelType Tunnelled { get; set; }
```

## Namespace Org.Apache.Http.Conn.Ssl

### Type Changed: Org.Apache.Http.Conn.Ssl.SSLSocketFactory

Modified properties:

```
public IX509HostnameVerifier AllowAllHostnameVerifier { get; set; }
	public IX509HostnameVerifier BrowserCompatibleHostnameVerifier { get; set; }
	public IX509HostnameVerifier StrictHostnameVerifier { get; set; }
```

## Namespace Org.Apache.Http.Message

### Type Changed: Org.Apache.Http.Message.BasicHeaderValueFormatter

Modified properties:

```
public BasicHeaderValueFormatter Default { get; set; }
```

### Type Changed: Org.Apache.Http.Message.BasicHeaderValueParser

Modified properties:

```
public BasicHeaderValueParser Default { get; set; }
```

### Type Changed: Org.Apache.Http.Message.BasicLineFormatter

Modified properties:

```
public BasicLineFormatter Default { get; set; }
```

### Type Changed: Org.Apache.Http.Message.BasicLineParser

Modified properties:

```
public BasicLineParser Default { get; set; }
```

## Namespace Org.Apache.Http.Protocol

### Type Changed: Org.Apache.Http.Protocol.HttpDateGenerator

Modified properties:

```
public Java.Util.TimeZone Gmt { get; set; }
```

### Type Changed: Org.Apache.Http.Protocol.HttpRequestHandlerRegistry

Obsoleted methods:

```
[Obsolete ("deprecated"]
	protected virtual bool MatchUriRequestPattern (string pattern, string requestUri);
```

## Namespace Org.Json

### Type Changed: Org.Json.JSONObject

Modified properties:

```
public Java.Lang.Object Null { get; set; }
```

## Namespace Org.W3c.Dom

### Type Changed: Org.W3c.Dom.DOMException

Modified properties:

```
public short TypeMismatchErr { get; set; }
	public short ValidationErr { get; set; }
```

### Type Changed: Org.W3c.Dom.Node

Modified properties:

```
public short DocumentPositionContainedBy { get; set; }
	public short DocumentPositionContains { get; set; }
	public short DocumentPositionDisconnected { get; set; }
	public short DocumentPositionFollowing { get; set; }
	public short DocumentPositionImplementationSpecific { get; set; }
	public short DocumentPositionPreceding { get; set; }
```

## Namespace Org.XmlPull.V1

### Type Changed: Org.XmlPull.V1.XmlPullParser

Modified properties:

```
public System.Collections.Generic.IList<string> Types { get; set; }
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

## New Namespace Org.Apache.Http.Impl

### New Type Org.Apache.Http.Impl.AbstractHttpClientConnection

```
public abstract class AbstractHttpClientConnection : Java.Lang.Object, Org.Apache.Http.IHttpClientConnection, Org.Apache.Http.IHttpConnection, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractHttpClientConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractHttpClientConnection ();
	// properties
	public virtual bool IsOpen { get; }
	public virtual bool IsStale { get; }
	public virtual Org.Apache.Http.IHttpConnectionMetrics Metrics { get; }
	public virtual int SocketTimeout { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual void AssertOpen ();
	public virtual void Close ();
	protected virtual Entity.EntityDeserializer CreateEntityDeserializer ();
	protected virtual Entity.EntitySerializer CreateEntitySerializer ();
	protected virtual Org.Apache.Http.IHttpResponseFactory CreateHttpResponseFactory ();
	protected virtual Org.Apache.Http.IO.IHttpMessageWriter CreateRequestWriter (Org.Apache.Http.IO.ISessionOutputBuffer buffer, Org.Apache.Http.Params.IHttpParams params);
	protected virtual Org.Apache.Http.IO.IHttpMessageParser CreateResponseParser (Org.Apache.Http.IO.ISessionInputBuffer buffer, Org.Apache.Http.IHttpResponseFactory responseFactory, Org.Apache.Http.Params.IHttpParams params);
	protected virtual void DoFlush ();
	public virtual void Flush ();
	protected virtual void Init (Org.Apache.Http.IO.ISessionInputBuffer inbuffer, Org.Apache.Http.IO.ISessionOutputBuffer outbuffer, Org.Apache.Http.Params.IHttpParams params);
	public virtual bool IsResponseAvailable (int timeout);
	public virtual void ReceiveResponseEntity (Org.Apache.Http.IHttpResponse response);
	public virtual Org.Apache.Http.IHttpResponse ReceiveResponseHeader ();
	public virtual void SendRequestEntity (Org.Apache.Http.IHttpEntityEnclosingRequest request);
	public virtual void SendRequestHeader (Org.Apache.Http.IHttpRequest request);
	public virtual void Shutdown ();
}
```

### New Type Org.Apache.Http.Impl.AbstractHttpServerConnection

```
public abstract class AbstractHttpServerConnection : Java.Lang.Object, Org.Apache.Http.IHttpServerConnection, Org.Apache.Http.IHttpConnection, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractHttpServerConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractHttpServerConnection ();
	// properties
	public virtual bool IsOpen { get; }
	public virtual bool IsStale { get; }
	public virtual Org.Apache.Http.IHttpConnectionMetrics Metrics { get; }
	public virtual int SocketTimeout { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual void AssertOpen ();
	public virtual void Close ();
	protected virtual Entity.EntityDeserializer CreateEntityDeserializer ();
	protected virtual Entity.EntitySerializer CreateEntitySerializer ();
	protected virtual Org.Apache.Http.IHttpRequestFactory CreateHttpRequestFactory ();
	protected virtual Org.Apache.Http.IO.IHttpMessageParser CreateRequestParser (Org.Apache.Http.IO.ISessionInputBuffer buffer, Org.Apache.Http.IHttpRequestFactory requestFactory, Org.Apache.Http.Params.IHttpParams params);
	protected virtual Org.Apache.Http.IO.IHttpMessageWriter CreateResponseWriter (Org.Apache.Http.IO.ISessionOutputBuffer buffer, Org.Apache.Http.Params.IHttpParams params);
	protected virtual void DoFlush ();
	public virtual void Flush ();
	protected virtual void Init (Org.Apache.Http.IO.ISessionInputBuffer inbuffer, Org.Apache.Http.IO.ISessionOutputBuffer outbuffer, Org.Apache.Http.Params.IHttpParams params);
	public virtual void ReceiveRequestEntity (Org.Apache.Http.IHttpEntityEnclosingRequest request);
	public virtual Org.Apache.Http.IHttpRequest ReceiveRequestHeader ();
	public virtual void SendResponseEntity (Org.Apache.Http.IHttpResponse response);
	public virtual void SendResponseHeader (Org.Apache.Http.IHttpResponse response);
	public virtual void Shutdown ();
}
```

### New Type Org.Apache.Http.Impl.DefaultConnectionReuseStrategy

```
public class DefaultConnectionReuseStrategy : Java.Lang.Object, Org.Apache.Http.IConnectionReuseStrategy, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultConnectionReuseStrategy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultConnectionReuseStrategy ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual Org.Apache.Http.ITokenIterator CreateTokenIterator (Org.Apache.Http.IHeaderIterator hit);
	public virtual bool KeepAlive (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.DefaultHttpClientConnection

```
public class DefaultHttpClientConnection : Org.Apache.Http.Impl.SocketHttpClientConnection, Org.Apache.Http.IHttpInetConnection, Org.Apache.Http.IHttpConnection, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.IHttpClientConnection {
	// constructors
	protected DefaultHttpClientConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHttpClientConnection ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Bind (Java.Net.Socket socket, Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.DefaultHttpRequestFactory

```
public class DefaultHttpRequestFactory : Java.Lang.Object, Org.Apache.Http.IHttpRequestFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultHttpRequestFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHttpRequestFactory ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.IHttpRequest NewHttpRequest (string method, string uri);
	public virtual Org.Apache.Http.IHttpRequest NewHttpRequest (Org.Apache.Http.IRequestLine requestline);
}
```

### New Type Org.Apache.Http.Impl.DefaultHttpResponseFactory

```
public class DefaultHttpResponseFactory : Java.Lang.Object, Org.Apache.Http.IHttpResponseFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultHttpResponseFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHttpResponseFactory ();
	public DefaultHttpResponseFactory (Org.Apache.Http.IReasonPhraseCatalog catalog);
	// properties
	protected Org.Apache.Http.IReasonPhraseCatalog ReasonCatalog { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual Java.Util.Locale DetermineLocale (Org.Apache.Http.Protocol.IHttpContext context);
	public virtual Org.Apache.Http.IHttpResponse NewHttpResponse (Org.Apache.Http.ProtocolVersion ver, int status, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual Org.Apache.Http.IHttpResponse NewHttpResponse (Org.Apache.Http.IStatusLine statusline, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.DefaultHttpServerConnection

```
public class DefaultHttpServerConnection : Org.Apache.Http.Impl.SocketHttpServerConnection, Org.Apache.Http.IHttpInetConnection, Org.Apache.Http.IHttpConnection, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.IHttpServerConnection {
	// constructors
	protected DefaultHttpServerConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHttpServerConnection ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Bind (Java.Net.Socket socket, Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.EnglishReasonPhraseCatalog

```
public class EnglishReasonPhraseCatalog : Java.Lang.Object, Org.Apache.Http.IReasonPhraseCatalog, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected EnglishReasonPhraseCatalog (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected EnglishReasonPhraseCatalog ();
	// properties
	public static EnglishReasonPhraseCatalog Instance { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual string GetReason (int status, Java.Util.Locale loc);
}
```

### New Type Org.Apache.Http.Impl.HttpConnectionMetricsImpl

```
public class HttpConnectionMetricsImpl : Java.Lang.Object, Org.Apache.Http.IHttpConnectionMetrics, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected HttpConnectionMetricsImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpConnectionMetricsImpl (Org.Apache.Http.IO.IHttpTransportMetrics inTransportMetric, Org.Apache.Http.IO.IHttpTransportMetrics outTransportMetric);
	// properties
	public virtual long ReceivedBytesCount { get; }
	public virtual long RequestCount { get; }
	public virtual long ResponseCount { get; }
	public virtual long SentBytesCount { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Java.Lang.Object GetMetric (string metricName);
	public virtual void IncrementRequestCount ();
	public virtual void IncrementResponseCount ();
	public virtual void Reset ();
	public virtual void SetMetric (string metricName, Java.Lang.Object obj);
}
```

### New Type Org.Apache.Http.Impl.NoConnectionReuseStrategy

```
public class NoConnectionReuseStrategy : Java.Lang.Object, Org.Apache.Http.IConnectionReuseStrategy, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected NoConnectionReuseStrategy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NoConnectionReuseStrategy ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool KeepAlive (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.SocketHttpClientConnection

```
public class SocketHttpClientConnection : Org.Apache.Http.Impl.AbstractHttpClientConnection, Org.Apache.Http.IHttpInetConnection, Org.Apache.Http.IHttpConnection, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.IHttpClientConnection {
	// constructors
	protected SocketHttpClientConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SocketHttpClientConnection ();
	// properties
	public override bool IsOpen { get; }
	public virtual Java.Net.InetAddress LocalAddress { get; }
	public virtual int LocalPort { get; }
	public virtual Java.Net.InetAddress RemoteAddress { get; }
	public virtual int RemotePort { get; }
	protected virtual Java.Net.Socket Socket { get; }
	public override int SocketTimeout { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual void AssertNotOpen ();
	protected override void AssertOpen ();
	protected virtual void Bind (Java.Net.Socket socket, Org.Apache.Http.Params.IHttpParams params);
	public override void Close ();
	protected virtual Org.Apache.Http.IO.ISessionInputBuffer CreateSessionInputBuffer (Java.Net.Socket socket, int buffersize, Org.Apache.Http.Params.IHttpParams params);
	protected virtual Org.Apache.Http.IO.ISessionOutputBuffer CreateSessionOutputBuffer (Java.Net.Socket socket, int buffersize, Org.Apache.Http.Params.IHttpParams params);
	public override void Shutdown ();
}
```

### New Type Org.Apache.Http.Impl.SocketHttpServerConnection

```
public class SocketHttpServerConnection : Org.Apache.Http.Impl.AbstractHttpServerConnection, Org.Apache.Http.IHttpInetConnection, Org.Apache.Http.IHttpConnection, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.IHttpServerConnection {
	// constructors
	protected SocketHttpServerConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SocketHttpServerConnection ();
	// properties
	public override bool IsOpen { get; }
	public virtual Java.Net.InetAddress LocalAddress { get; }
	public virtual int LocalPort { get; }
	public virtual Java.Net.InetAddress RemoteAddress { get; }
	public virtual int RemotePort { get; }
	protected virtual Java.Net.Socket Socket { get; }
	public override int SocketTimeout { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual void AssertNotOpen ();
	protected override void AssertOpen ();
	protected virtual void Bind (Java.Net.Socket socket, Org.Apache.Http.Params.IHttpParams params);
	public override void Close ();
	protected virtual Org.Apache.Http.IO.ISessionInputBuffer CreateHttpDataReceiver (Java.Net.Socket socket, int buffersize, Org.Apache.Http.Params.IHttpParams params);
	protected virtual Org.Apache.Http.IO.ISessionOutputBuffer CreateHttpDataTransmitter (Java.Net.Socket socket, int buffersize, Org.Apache.Http.Params.IHttpParams params);
	public override void Shutdown ();
}
```

## New Namespace Org.Apache.Http.Impl.Auth

### New Type Org.Apache.Http.Impl.Auth.AuthSchemeBase

```
public abstract class AuthSchemeBase : Java.Lang.Object, Org.Apache.Http.Authentication.IAuthScheme, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AuthSchemeBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AuthSchemeBase ();
	// properties
	public virtual bool IsComplete { get; }
	public virtual bool IsConnectionBased { get; }
	public virtual bool IsProxy { get; }
	public virtual string Realm { get; }
	public virtual string SchemeName { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.IHeader Authenticate (Org.Apache.Http.Authentication.ICredentials credentials, Org.Apache.Http.IHttpRequest request);
	public virtual string GetParameter (string name);
	protected virtual void ParseChallenge (Org.Apache.Http.Util.CharArrayBuffer buffer, int pos, int len);
	public virtual void ProcessChallenge (Org.Apache.Http.IHeader header);
}
```

### New Type Org.Apache.Http.Impl.Auth.BasicScheme

```
public class BasicScheme : Org.Apache.Http.Impl.Auth.RFC2617Scheme, Org.Apache.Http.Authentication.IAuthScheme, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicScheme (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicScheme ();
	// properties
	public override bool IsComplete { get; }
	public override bool IsConnectionBased { get; }
	public override string SchemeName { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static Org.Apache.Http.IHeader Authenticate (Org.Apache.Http.Authentication.ICredentials credentials, string charset, bool proxy);
	public override Org.Apache.Http.IHeader Authenticate (Org.Apache.Http.Authentication.ICredentials credentials, Org.Apache.Http.IHttpRequest request);
}
```

### New Type Org.Apache.Http.Impl.Auth.BasicSchemeFactory

```
public class BasicSchemeFactory : Java.Lang.Object, Org.Apache.Http.Authentication.IAuthSchemeFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicSchemeFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicSchemeFactory ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Authentication.IAuthScheme NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Auth.DigestScheme

```
public class DigestScheme : Org.Apache.Http.Impl.Auth.RFC2617Scheme, Org.Apache.Http.Authentication.IAuthScheme, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DigestScheme (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DigestScheme ();
	// properties
	public override bool IsComplete { get; }
	public override bool IsConnectionBased { get; }
	public override string SchemeName { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Org.Apache.Http.IHeader Authenticate (Org.Apache.Http.Authentication.ICredentials credentials, Org.Apache.Http.IHttpRequest request);
	public static string CreateCnonce ();
	public virtual void OverrideParamter (string name, string value);
}
```

### New Type Org.Apache.Http.Impl.Auth.DigestSchemeFactory

```
public class DigestSchemeFactory : Java.Lang.Object, Org.Apache.Http.Authentication.IAuthSchemeFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DigestSchemeFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DigestSchemeFactory ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Authentication.IAuthScheme NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Auth.INTLMEngine

```
public interface INTLMEngine : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual string GenerateType1Msg (string domain, string workstation);
	public virtual string GenerateType3Msg (string username, string password, string domain, string workstation, string challenge);
}
```

### New Type Org.Apache.Http.Impl.Auth.NTLMEngineException

```
public class NTLMEngineException : Org.Apache.Http.Authentication.AuthenticationException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected NTLMEngineException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NTLMEngineException ();
	public NTLMEngineException (string message);
	public NTLMEngineException (string message, Java.Lang.Throwable cause);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Org.Apache.Http.Impl.Auth.NTLMScheme

```
public class NTLMScheme : Org.Apache.Http.Impl.Auth.AuthSchemeBase, Org.Apache.Http.Authentication.IAuthScheme, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected NTLMScheme (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NTLMScheme (INTLMEngine engine);
	// properties
	public override bool IsComplete { get; }
	public override bool IsConnectionBased { get; }
	public override string Realm { get; }
	public override string SchemeName { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Org.Apache.Http.IHeader Authenticate (Org.Apache.Http.Authentication.ICredentials credentials, Org.Apache.Http.IHttpRequest request);
	public override string GetParameter (string name);
	protected override void ParseChallenge (Org.Apache.Http.Util.CharArrayBuffer buffer, int pos, int len);
}
```

### New Type Org.Apache.Http.Impl.Auth.RFC2617Scheme

```
public abstract class RFC2617Scheme : Org.Apache.Http.Impl.Auth.AuthSchemeBase, Org.Apache.Http.Authentication.IAuthScheme, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2617Scheme (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2617Scheme ();
	// properties
	protected virtual System.Collections.Generic.IDictionary<System.String,System.String> Parameters { get; }
	public override string Realm { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override string GetParameter (string name);
	protected override void ParseChallenge (Org.Apache.Http.Util.CharArrayBuffer buffer, int pos, int len);
}
```

### New Type Org.Apache.Http.Impl.Auth.UnsupportedDigestAlgorithmException

```
public class UnsupportedDigestAlgorithmException : Java.Lang.RuntimeException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected UnsupportedDigestAlgorithmException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public UnsupportedDigestAlgorithmException ();
	public UnsupportedDigestAlgorithmException (string message);
	public UnsupportedDigestAlgorithmException (string message, Java.Lang.Throwable cause);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

## New Namespace Org.Apache.Http.Impl.Client

### New Type Org.Apache.Http.Impl.Client.AbstractAuthenticationHandler

```
public abstract class AbstractAuthenticationHandler : Java.Lang.Object, Org.Apache.Http.Client.IAuthenticationHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractAuthenticationHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractAuthenticationHandler ();
	// properties
	protected virtual System.Collections.Generic.IList<string> AuthPreferences { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual System.Collections.Generic.IDictionary<System.String,Org.Apache.Http.IHeader> GetChallenges (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual bool IsAuthenticationRequested (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual System.Collections.Generic.IDictionary<System.String,Org.Apache.Http.IHeader> ParseChallenges (Org.Apache.Http.IHeader[] headers);
	public virtual Org.Apache.Http.Authentication.IAuthScheme SelectScheme (System.Collections.Generic.IDictionary<System.String,Org.Apache.Http.IHeader> challenges, Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.Client.AbstractHttpClient

```
public abstract class AbstractHttpClient : Java.Lang.Object, Org.Apache.Http.Client.IHttpClient, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractHttpClient (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractHttpClient (Org.Apache.Http.Conn.IClientConnectionManager conman, Org.Apache.Http.Params.IHttpParams params);
	// properties
	public Org.Apache.Http.Authentication.AuthSchemeRegistry AuthSchemes { get; set; }
	public Org.Apache.Http.Conn.IConnectionKeepAliveStrategy ConnectionKeepAliveStrategy { get; }
	public virtual Org.Apache.Http.Conn.IClientConnectionManager ConnectionManager { get; }
	public Org.Apache.Http.IConnectionReuseStrategy ConnectionReuseStrategy { get; }
	public Org.Apache.Http.Cookies.CookieSpecRegistry CookieSpecs { get; set; }
	public Org.Apache.Http.Client.ICookieStore CookieStore { get; set; }
	public Org.Apache.Http.Client.ICredentialsProvider CredentialsProvider { get; set; }
	protected Org.Apache.Http.Protocol.BasicHttpProcessor HttpProcessor { get; }
	public Org.Apache.Http.Client.IHttpRequestRetryHandler HttpRequestRetryHandler { get; set; }
	public override Org.Apache.Http.Params.IHttpParams Params { get; set; }
	public Org.Apache.Http.Client.IAuthenticationHandler ProxyAuthenticationHandler { get; set; }
	public Org.Apache.Http.Client.IRedirectHandler RedirectHandler { get; set; }
	public Org.Apache.Http.Protocol.HttpRequestExecutor RequestExecutor { get; }
	public virtual int RequestInterceptorCount { get; }
	public virtual int ResponseInterceptorCount { get; }
	public Org.Apache.Http.Conn.Routing.IHttpRoutePlanner RoutePlanner { get; set; }
	public Org.Apache.Http.Client.IAuthenticationHandler TargetAuthenticationHandler { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public Org.Apache.Http.Client.IUserTokenHandler UserTokenHandler { get; set; }
	// methods
	public virtual void AddRequestInterceptor (Org.Apache.Http.IHttpRequestInterceptor itcp);
	public virtual void AddRequestInterceptor (Org.Apache.Http.IHttpRequestInterceptor itcp, int index);
	public virtual void AddResponseInterceptor (Org.Apache.Http.IHttpResponseInterceptor itcp);
	public virtual void AddResponseInterceptor (Org.Apache.Http.IHttpResponseInterceptor itcp, int index);
	public virtual void ClearRequestInterceptors ();
	public virtual void ClearResponseInterceptors ();
	protected virtual Org.Apache.Http.Authentication.AuthSchemeRegistry CreateAuthSchemeRegistry ();
	protected virtual Org.Apache.Http.Conn.IClientConnectionManager CreateClientConnectionManager ();
	protected virtual Org.Apache.Http.Conn.IConnectionKeepAliveStrategy CreateConnectionKeepAliveStrategy ();
	protected virtual Org.Apache.Http.IConnectionReuseStrategy CreateConnectionReuseStrategy ();
	protected virtual Org.Apache.Http.Cookies.CookieSpecRegistry CreateCookieSpecRegistry ();
	protected virtual Org.Apache.Http.Client.ICookieStore CreateCookieStore ();
	protected virtual Org.Apache.Http.Client.ICredentialsProvider CreateCredentialsProvider ();
	protected virtual Org.Apache.Http.Protocol.IHttpContext CreateHttpContext ();
	protected virtual Org.Apache.Http.Params.IHttpParams CreateHttpParams ();
	protected virtual Org.Apache.Http.Protocol.BasicHttpProcessor CreateHttpProcessor ();
	protected virtual Org.Apache.Http.Client.IHttpRequestRetryHandler CreateHttpRequestRetryHandler ();
	protected virtual Org.Apache.Http.Conn.Routing.IHttpRoutePlanner CreateHttpRoutePlanner ();
	protected virtual Org.Apache.Http.Client.IAuthenticationHandler CreateProxyAuthenticationHandler ();
	protected virtual Org.Apache.Http.Client.IRedirectHandler CreateRedirectHandler ();
	protected virtual Org.Apache.Http.Protocol.HttpRequestExecutor CreateRequestExecutor ();
	protected virtual Org.Apache.Http.Client.IAuthenticationHandler CreateTargetAuthenticationHandler ();
	protected virtual Org.Apache.Http.Client.IUserTokenHandler CreateUserTokenHandler ();
	protected virtual Org.Apache.Http.Params.IHttpParams DetermineParams (Org.Apache.Http.IHttpRequest req);
	public virtual Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual Java.Lang.Object Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual Java.Lang.Object Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler);
	public virtual Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request);
	public virtual Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual Java.Lang.Object Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual Java.Lang.Object Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler);
	public virtual Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request);
	public virtual Org.Apache.Http.IHttpRequestInterceptor GetRequestInterceptor (int index);
	public virtual Org.Apache.Http.IHttpResponseInterceptor GetResponseInterceptor (int index);
	public virtual void RemoveRequestInterceptorByClass (Java.Lang.Class clazz);
	public virtual void RemoveResponseInterceptorByClass (Java.Lang.Class clazz);
	public virtual void SetKeepAliveStrategy (Org.Apache.Http.Conn.IConnectionKeepAliveStrategy keepAliveStrategy);
	public virtual void SetReuseStrategy (Org.Apache.Http.IConnectionReuseStrategy reuseStrategy);
}
```

### New Type Org.Apache.Http.Impl.Client.BasicCookieStore

```
public class BasicCookieStore : Java.Lang.Object, Org.Apache.Http.Client.ICookieStore, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicCookieStore (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicCookieStore ();
	// properties
	public virtual System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> Cookies { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void AddCookie (Org.Apache.Http.Cookies.ICookie cookie);
	public virtual void AddCookies (Org.Apache.Http.Cookies.ICookie[] cookies);
	public virtual void Clear ();
	public virtual bool ClearExpired (Java.Util.Date date);
}
```

### New Type Org.Apache.Http.Impl.Client.BasicCredentialsProvider

```
public class BasicCredentialsProvider : Java.Lang.Object, Org.Apache.Http.Client.ICredentialsProvider, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicCredentialsProvider (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicCredentialsProvider ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Clear ();
	public virtual Org.Apache.Http.Authentication.ICredentials GetCredentials (Org.Apache.Http.Authentication.AuthScope authscope);
	public virtual void SetCredentials (Org.Apache.Http.Authentication.AuthScope authscope, Org.Apache.Http.Authentication.ICredentials credentials);
}
```

### New Type Org.Apache.Http.Impl.Client.BasicResponseHandler

```
public class BasicResponseHandler : Java.Lang.Object, Org.Apache.Http.Client.IResponseHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicResponseHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicResponseHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual string HandleResponse (Org.Apache.Http.IHttpResponse response);
}
```

### New Type Org.Apache.Http.Impl.Client.ClientParamsStack

```
public class ClientParamsStack : Org.Apache.Http.Params.AbstractHttpParams, Org.Apache.Http.Params.IHttpParams, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ClientParamsStack (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ClientParamsStack (ClientParamsStack stack);
	public ClientParamsStack (ClientParamsStack stack, Org.Apache.Http.Params.IHttpParams aparams, Org.Apache.Http.Params.IHttpParams cparams, Org.Apache.Http.Params.IHttpParams rparams, Org.Apache.Http.Params.IHttpParams oparams);
	public ClientParamsStack (Org.Apache.Http.Params.IHttpParams aparams, Org.Apache.Http.Params.IHttpParams cparams, Org.Apache.Http.Params.IHttpParams rparams, Org.Apache.Http.Params.IHttpParams oparams);
	// properties
	public Org.Apache.Http.Params.IHttpParams ApplicationParams { get; }
	public Org.Apache.Http.Params.IHttpParams ClientParams { get; }
	public Org.Apache.Http.Params.IHttpParams OverrideParams { get; }
	public Org.Apache.Http.Params.IHttpParams RequestParams { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Org.Apache.Http.Params.IHttpParams Copy ();
	public override Java.Lang.Object GetParameter (string name);
	public override bool RemoveParameter (string name);
	public override Org.Apache.Http.Params.IHttpParams SetParameter (string name, Java.Lang.Object value);
}
```

### New Type Org.Apache.Http.Impl.Client.DefaultConnectionKeepAliveStrategy

```
public class DefaultConnectionKeepAliveStrategy : Java.Lang.Object, Org.Apache.Http.Conn.IConnectionKeepAliveStrategy, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultConnectionKeepAliveStrategy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultConnectionKeepAliveStrategy ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual long GetKeepAliveDuration (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.Client.DefaultHttpClient

```
public class DefaultHttpClient : Org.Apache.Http.Impl.Client.AbstractHttpClient, Org.Apache.Http.Client.IHttpClient, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultHttpClient (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHttpClient ();
	public DefaultHttpClient (Org.Apache.Http.Conn.IClientConnectionManager conman, Org.Apache.Http.Params.IHttpParams params);
	public DefaultHttpClient (Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected override Org.Apache.Http.Authentication.AuthSchemeRegistry CreateAuthSchemeRegistry ();
	protected override Org.Apache.Http.Conn.IClientConnectionManager CreateClientConnectionManager ();
	protected override Org.Apache.Http.Conn.IConnectionKeepAliveStrategy CreateConnectionKeepAliveStrategy ();
	protected override Org.Apache.Http.IConnectionReuseStrategy CreateConnectionReuseStrategy ();
	protected override Org.Apache.Http.Cookies.CookieSpecRegistry CreateCookieSpecRegistry ();
	protected override Org.Apache.Http.Client.ICookieStore CreateCookieStore ();
	protected override Org.Apache.Http.Client.ICredentialsProvider CreateCredentialsProvider ();
	protected override Org.Apache.Http.Protocol.IHttpContext CreateHttpContext ();
	protected override Org.Apache.Http.Params.IHttpParams CreateHttpParams ();
	protected override Org.Apache.Http.Protocol.BasicHttpProcessor CreateHttpProcessor ();
	protected override Org.Apache.Http.Client.IHttpRequestRetryHandler CreateHttpRequestRetryHandler ();
	protected override Org.Apache.Http.Conn.Routing.IHttpRoutePlanner CreateHttpRoutePlanner ();
	protected override Org.Apache.Http.Client.IAuthenticationHandler CreateProxyAuthenticationHandler ();
	protected override Org.Apache.Http.Client.IRedirectHandler CreateRedirectHandler ();
	protected override Org.Apache.Http.Protocol.HttpRequestExecutor CreateRequestExecutor ();
	protected override Org.Apache.Http.Client.IAuthenticationHandler CreateTargetAuthenticationHandler ();
	protected override Org.Apache.Http.Client.IUserTokenHandler CreateUserTokenHandler ();
}
```

### New Type Org.Apache.Http.Impl.Client.DefaultHttpRequestRetryHandler

```
public class DefaultHttpRequestRetryHandler : Java.Lang.Object, Org.Apache.Http.Client.IHttpRequestRetryHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultHttpRequestRetryHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHttpRequestRetryHandler ();
	public DefaultHttpRequestRetryHandler (int retryCount, bool requestSentRetryEnabled);
	// properties
	public virtual bool IsRequestSentRetryEnabled { get; }
	public virtual int RetryCount { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool RetryRequest (Java.IO.IOException exception, int executionCount, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.Client.DefaultProxyAuthenticationHandler

```
public class DefaultProxyAuthenticationHandler : Org.Apache.Http.Impl.Client.AbstractAuthenticationHandler, Org.Apache.Http.Client.IAuthenticationHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultProxyAuthenticationHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultProxyAuthenticationHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override System.Collections.Generic.IDictionary<System.String,Org.Apache.Http.IHeader> GetChallenges (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	public override bool IsAuthenticationRequested (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.Client.DefaultRedirectHandler

```
public class DefaultRedirectHandler : Java.Lang.Object, Org.Apache.Http.Client.IRedirectHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultRedirectHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultRedirectHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Java.Net.URI GetLocationURI (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual bool IsRedirectRequested (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.Client.DefaultRequestDirector

```
public class DefaultRequestDirector : Java.Lang.Object, Org.Apache.Http.Client.IRequestDirector, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultRequestDirector (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	protected Org.Apache.Http.Conn.IClientConnectionManager ConnManager { get; set; }
	protected Org.Apache.Http.Protocol.IHttpProcessor HttpProcessor { get; set; }
	protected Org.Apache.Http.Conn.IConnectionKeepAliveStrategy KeepAliveStrategy { get; set; }
	protected Org.Apache.Http.Conn.IManagedClientConnection ManagedConn { get; set; }
	protected Org.Apache.Http.Params.IHttpParams Params { get; set; }
	protected Org.Apache.Http.Client.IRedirectHandler RedirectHandler { get; set; }
	protected Org.Apache.Http.Protocol.HttpRequestExecutor RequestExec { get; set; }
	protected Org.Apache.Http.Client.IHttpRequestRetryHandler RetryHandler { get; set; }
	protected Org.Apache.Http.IConnectionReuseStrategy ReuseStrategy { get; set; }
	protected Org.Apache.Http.Conn.Routing.IHttpRoutePlanner RoutePlanner { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual Org.Apache.Http.IHttpRequest CreateConnectRequest (Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual bool CreateTunnelToProxy (Org.Apache.Http.Conn.Routing.HttpRoute route, int hop, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual bool CreateTunnelToTarget (Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual Org.Apache.Http.Conn.Routing.HttpRoute DetermineRoute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual void EstablishRoute (Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual RoutedRequest HandleResponse (RoutedRequest roureq, Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual void ReleaseConnection ();
	protected virtual void RewriteRequestURI (RequestWrapper request, Org.Apache.Http.Conn.Routing.HttpRoute route);
}
```

### New Type Org.Apache.Http.Impl.Client.DefaultTargetAuthenticationHandler

```
public class DefaultTargetAuthenticationHandler : Org.Apache.Http.Impl.Client.AbstractAuthenticationHandler, Org.Apache.Http.Client.IAuthenticationHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultTargetAuthenticationHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultTargetAuthenticationHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override System.Collections.Generic.IDictionary<System.String,Org.Apache.Http.IHeader> GetChallenges (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	public override bool IsAuthenticationRequested (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.Client.DefaultUserTokenHandler

```
public class DefaultUserTokenHandler : Java.Lang.Object, Org.Apache.Http.Client.IUserTokenHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultUserTokenHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultUserTokenHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Java.Lang.Object GetUserToken (Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.Client.EntityEnclosingRequestWrapper

```
public class EntityEnclosingRequestWrapper : Org.Apache.Http.Impl.Client.RequestWrapper, Org.Apache.Http.IHttpEntityEnclosingRequest, Org.Apache.Http.IHttpRequest, Org.Apache.Http.IHttpMessage, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.Client.Methods.IHttpUriRequest {
	// constructors
	protected EntityEnclosingRequestWrapper (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public EntityEnclosingRequestWrapper (Org.Apache.Http.IHttpEntityEnclosingRequest request);
	// properties
	public virtual Org.Apache.Http.IHttpEntity Entity { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool ExpectContinue ();
}
```

### New Type Org.Apache.Http.Impl.Client.RedirectLocations

```
public class RedirectLocations : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected RedirectLocations (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RedirectLocations ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Add (Java.Net.URI uri);
	public virtual bool Contains (Java.Net.URI uri);
	public virtual bool Remove (Java.Net.URI uri);
}
```

### New Type Org.Apache.Http.Impl.Client.RequestWrapper

```
public class RequestWrapper : Org.Apache.Http.Message.AbstractHttpMessage, Org.Apache.Http.Client.Methods.IHttpUriRequest, Org.Apache.Http.IHttpRequest, Org.Apache.Http.IHttpMessage, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RequestWrapper (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestWrapper (Org.Apache.Http.IHttpRequest request);
	// properties
	public virtual int ExecCount { get; }
	public virtual bool IsAborted { get; }
	public virtual bool IsRepeatable { get; }
	public virtual string Method { get; set; }
	public virtual Org.Apache.Http.IHttpRequest Original { get; }
	public override Org.Apache.Http.ProtocolVersion ProtocolVersion { get; }
	public virtual Org.Apache.Http.IRequestLine RequestLine { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual Java.Net.URI URI { get; set; }
	// methods
	public virtual void Abort ();
	public virtual void IncrementExecCount ();
	public virtual void ResetHeaders ();
}
```

### New Type Org.Apache.Http.Impl.Client.RoutedRequest

```
public class RoutedRequest : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected RoutedRequest (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RoutedRequest (RequestWrapper req, Org.Apache.Http.Conn.Routing.HttpRoute route);
	// properties
	public RequestWrapper Request { get; }
	public Org.Apache.Http.Conn.Routing.HttpRoute Route { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Org.Apache.Http.Impl.Client.TunnelRefusedException

```
public class TunnelRefusedException : Org.Apache.Http.HttpException, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected TunnelRefusedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TunnelRefusedException (string message, Org.Apache.Http.IHttpResponse response);
	// properties
	public virtual Org.Apache.Http.IHttpResponse Response { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

## New Namespace Org.Apache.Http.Impl.Conn

### New Type Org.Apache.Http.Impl.Conn.AbstractClientConnAdapter

```
public abstract class AbstractClientConnAdapter : Java.Lang.Object, Org.Apache.Http.Conn.IManagedClientConnection, Org.Apache.Http.Conn.IConnectionReleaseTrigger, Org.Apache.Http.IHttpClientConnection, Org.Apache.Http.IHttpInetConnection, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.IHttpConnection {
	// constructors
	protected AbstractClientConnAdapter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractClientConnAdapter (Org.Apache.Http.Conn.IClientConnectionManager mgr, Org.Apache.Http.Conn.IOperatedClientConnection conn);
	// properties
	public virtual bool IsMarkedReusable { get; }
	public virtual bool IsOpen { get; }
	public virtual bool IsSecure { get; }
	public virtual bool IsStale { get; }
	public virtual Java.Net.InetAddress LocalAddress { get; }
	public virtual int LocalPort { get; }
	protected virtual Org.Apache.Http.Conn.IClientConnectionManager Manager { get; }
	public virtual Org.Apache.Http.IHttpConnectionMetrics Metrics { get; }
	public virtual Java.Net.InetAddress RemoteAddress { get; }
	public virtual int RemotePort { get; }
	public virtual Org.Apache.Http.Conn.Routing.HttpRoute Route { get; }
	public virtual int SocketTimeout { get; set; }
	public virtual Javax.Net.Ssl.ISSLSession SSLSession { get; }
	public virtual Java.Lang.Object State { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	protected virtual Org.Apache.Http.Conn.IOperatedClientConnection WrappedConnection { get; }
	// methods
	public virtual void AbortConnection ();
	protected void AssertNotAborted ();
	protected void AssertValid (Org.Apache.Http.Conn.IOperatedClientConnection wrappedConn);
	public virtual void Close ();
	protected virtual void Detach ();
	public virtual void Flush ();
	public virtual bool IsResponseAvailable (int timeout);
	public virtual void LayerProtocol (Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	public virtual void MarkReusable ();
	public virtual void Open (Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	public System.Threading.Tasks.Task OpenAsync (Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	public virtual void ReceiveResponseEntity (Org.Apache.Http.IHttpResponse response);
	public virtual Org.Apache.Http.IHttpResponse ReceiveResponseHeader ();
	public virtual void ReleaseConnection ();
	public virtual void SendRequestEntity (Org.Apache.Http.IHttpEntityEnclosingRequest request);
	public virtual void SendRequestHeader (Org.Apache.Http.IHttpRequest request);
	public virtual void SetIdleDuration (long duration, Java.Util.Concurrent.TimeUnit unit);
	public virtual void Shutdown ();
	public virtual void TunnelProxy (Org.Apache.Http.HttpHost next, bool secure, Org.Apache.Http.Params.IHttpParams params);
	public virtual void TunnelTarget (bool secure, Org.Apache.Http.Params.IHttpParams params);
	public virtual void UnmarkReusable ();
}
```

### New Type Org.Apache.Http.Impl.Conn.AbstractPooledConnAdapter

```
public abstract class AbstractPooledConnAdapter : Org.Apache.Http.Impl.Conn.AbstractClientConnAdapter, Org.Apache.Http.Conn.IManagedClientConnection, Org.Apache.Http.Conn.IConnectionReleaseTrigger, Org.Apache.Http.IHttpClientConnection, Org.Apache.Http.IHttpInetConnection, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.IHttpConnection {
	// constructors
	protected AbstractPooledConnAdapter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractPooledConnAdapter (Org.Apache.Http.Conn.IClientConnectionManager manager, AbstractPoolEntry entry);
	// properties
	protected AbstractPoolEntry PoolEntry { get; set; }
	public override Org.Apache.Http.Conn.Routing.HttpRoute Route { get; }
	public override Java.Lang.Object State { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected void AssertAttached ();
	public override void Close ();
	public override void LayerProtocol (Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	public override void Open (Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	public override void Shutdown ();
	public override void TunnelProxy (Org.Apache.Http.HttpHost next, bool secure, Org.Apache.Http.Params.IHttpParams params);
	public override void TunnelTarget (bool secure, Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Conn.AbstractPoolEntry

```
public abstract class AbstractPoolEntry : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected AbstractPoolEntry (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractPoolEntry (Org.Apache.Http.Conn.IClientConnectionOperator connOperator, Org.Apache.Http.Conn.Routing.HttpRoute route);
	// properties
	protected Org.Apache.Http.Conn.IOperatedClientConnection Connection { get; set; }
	protected Org.Apache.Http.Conn.IClientConnectionOperator ConnOperator { get; set; }
	protected Org.Apache.Http.Conn.Routing.HttpRoute Route { get; set; }
	public virtual Java.Lang.Object State { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	protected Org.Apache.Http.Conn.Routing.RouteTracker Tracker { get; set; }
	// methods
	public virtual void LayerProtocol (Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	public virtual void Open (Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	protected virtual void ShutdownEntry ();
	public virtual void TunnelProxy (Org.Apache.Http.HttpHost next, bool secure, Org.Apache.Http.Params.IHttpParams params);
	public virtual void TunnelTarget (bool secure, Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Conn.DefaultClientConnection

```
public class DefaultClientConnection : Org.Apache.Http.Impl.SocketHttpClientConnection, Org.Apache.Http.Conn.IOperatedClientConnection, Org.Apache.Http.IHttpClientConnection, Org.Apache.Http.IHttpInetConnection, Org.Apache.Http.IHttpConnection, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultClientConnection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultClientConnection ();
	// properties
	public virtual bool IsSecure { get; }
	protected override Java.Net.Socket Socket { get; }
	public virtual Org.Apache.Http.HttpHost TargetHost { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void OpenCompleted (bool secure, Org.Apache.Http.Params.IHttpParams params);
	public virtual void Opening (Java.Net.Socket sock, Org.Apache.Http.HttpHost target);
	public virtual void Update (Java.Net.Socket sock, Org.Apache.Http.HttpHost target, bool secure, Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Conn.DefaultClientConnectionOperator

```
public class DefaultClientConnectionOperator : Java.Lang.Object, Org.Apache.Http.Conn.IClientConnectionOperator, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultClientConnectionOperator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultClientConnectionOperator (Org.Apache.Http.Conn.Schemes.SchemeRegistry schemes);
	// properties
	protected Org.Apache.Http.Conn.Schemes.SchemeRegistry SchemeRegistry { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Conn.IOperatedClientConnection CreateConnection ();
	public virtual void OpenConnection (Org.Apache.Http.Conn.IOperatedClientConnection conn, Org.Apache.Http.HttpHost target, Java.Net.InetAddress local, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	protected virtual void PrepareSocket (Java.Net.Socket sock, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	public virtual void UpdateSecureConnection (Org.Apache.Http.Conn.IOperatedClientConnection conn, Org.Apache.Http.HttpHost target, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Conn.DefaultHttpRoutePlanner

```
public class DefaultHttpRoutePlanner : Java.Lang.Object, Org.Apache.Http.Conn.Routing.IHttpRoutePlanner, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultHttpRoutePlanner (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHttpRoutePlanner (Org.Apache.Http.Conn.Schemes.SchemeRegistry schreg);
	// properties
	protected Org.Apache.Http.Conn.Schemes.SchemeRegistry SchemeRegistry { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Conn.Routing.HttpRoute DetermineRoute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
}
```

### New Type Org.Apache.Http.Impl.Conn.DefaultResponseParser

```
public class DefaultResponseParser : Org.Apache.Http.Impl.IO.AbstractMessageParser, Org.Apache.Http.IO.IHttpMessageParser, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected DefaultResponseParser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultResponseParser (Org.Apache.Http.IO.ISessionInputBuffer buffer, Org.Apache.Http.Message.ILineParser parser, Org.Apache.Http.IHttpResponseFactory responseFactory, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected override Org.Apache.Http.IHttpMessage ParseHead (Org.Apache.Http.IO.ISessionInputBuffer sessionBuffer);
}
```

### New Type Org.Apache.Http.Impl.Conn.IdleConnectionHandler

```
public class IdleConnectionHandler : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected IdleConnectionHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public IdleConnectionHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Add (Org.Apache.Http.IHttpConnection connection, long validDuration, Java.Util.Concurrent.TimeUnit unit);
	public virtual void CloseExpiredConnections ();
	public virtual void CloseIdleConnections (long idleTime);
	public virtual bool Remove (Org.Apache.Http.IHttpConnection connection);
	public virtual void RemoveAll ();
}
```

### New Type Org.Apache.Http.Impl.Conn.LoggingSessionInputBuffer

```
public class LoggingSessionInputBuffer : Java.Lang.Object, Org.Apache.Http.IO.ISessionInputBuffer, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected LoggingSessionInputBuffer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LoggingSessionInputBuffer (Org.Apache.Http.IO.ISessionInputBuffer in, Wire wire);
	// properties
	public virtual Org.Apache.Http.IO.IHttpTransportMetrics Metrics { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool IsDataAvailable (int timeout);
	public virtual int Read ();
	public virtual int Read (byte[] b);
	public virtual int Read (byte[] b, int off, int len);
	public virtual string ReadLine ();
	public virtual int ReadLine (Org.Apache.Http.Util.CharArrayBuffer buffer);
}
```

### New Type Org.Apache.Http.Impl.Conn.LoggingSessionOutputBuffer

```
public class LoggingSessionOutputBuffer : Java.Lang.Object, Org.Apache.Http.IO.ISessionOutputBuffer, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected LoggingSessionOutputBuffer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LoggingSessionOutputBuffer (Org.Apache.Http.IO.ISessionOutputBuffer out, Wire wire);
	// properties
	public virtual Org.Apache.Http.IO.IHttpTransportMetrics Metrics { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Flush ();
	public virtual void Write (byte[] b);
	public virtual void Write (byte[] b, int off, int len);
	public virtual void Write (int b);
	public virtual void WriteLine (string s);
	public virtual void WriteLine (Org.Apache.Http.Util.CharArrayBuffer buffer);
}
```

### New Type Org.Apache.Http.Impl.Conn.ProxySelectorRoutePlanner

```
public class ProxySelectorRoutePlanner : Java.Lang.Object, Org.Apache.Http.Conn.Routing.IHttpRoutePlanner, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ProxySelectorRoutePlanner (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ProxySelectorRoutePlanner (Org.Apache.Http.Conn.Schemes.SchemeRegistry schreg, Java.Net.ProxySelector prosel);
	// properties
	public virtual Java.Net.ProxySelector ProxySelector { get; set; }
	protected Org.Apache.Http.Conn.Schemes.SchemeRegistry SchemeRegistry { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual Java.Net.Proxy ChooseProxy (System.Collections.Generic.IList<Java.Net.Proxy> proxies, Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual Org.Apache.Http.HttpHost DetermineProxy (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	public virtual Org.Apache.Http.Conn.Routing.HttpRoute DetermineRoute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	protected virtual string GetHost (Java.Net.InetSocketAddress isa);
}
```

### New Type Org.Apache.Http.Impl.Conn.SingleClientConnManager

```
public class SingleClientConnManager : Java.Lang.Object, Org.Apache.Http.Conn.IClientConnectionManager, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected SingleClientConnManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SingleClientConnManager (Org.Apache.Http.Params.IHttpParams params, Org.Apache.Http.Conn.Schemes.SchemeRegistry schreg);
	// fields
	public static const string MisuseMessage = "Invalid use of SingleClientConnManager: connection still allocated.
Make sure to release the connection before allocating another one.";
	// properties
	protected bool AlwaysShutDown { get; set; }
	protected long ConnectionExpiresTime { get; set; }
	protected Org.Apache.Http.Conn.IClientConnectionOperator ConnOperator { get; set; }
	protected bool IsShutDown { get; set; }
	protected long LastReleaseTime { get; set; }
	protected SingleClientConnManager.ConnAdapter ManagedConn { get; set; }
	public virtual Org.Apache.Http.Conn.Schemes.SchemeRegistry SchemeRegistry { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	protected SingleClientConnManager.PoolEntry UniquePoolEntry { get; set; }
	// methods
	protected void AssertStillUp ();
	public virtual void CloseExpiredConnections ();
	public virtual void CloseIdleConnections (long idletime, Java.Util.Concurrent.TimeUnit tunit);
	protected virtual Org.Apache.Http.Conn.IClientConnectionOperator CreateConnectionOperator (Org.Apache.Http.Conn.Schemes.SchemeRegistry schreg);
	public virtual Org.Apache.Http.Conn.IManagedClientConnection GetConnection (Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Object state);
	public virtual void ReleaseConnection (Org.Apache.Http.Conn.IManagedClientConnection conn, long validDuration, Java.Util.Concurrent.TimeUnit timeUnit);
	public virtual Org.Apache.Http.Conn.IClientConnectionRequest RequestConnection (Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Object state);
	protected virtual void RevokeConnection ();
	public virtual void Shutdown ();

	// inner types
	public class ConnAdapter : Org.Apache.Http.Impl.Conn.AbstractPooledConnAdapter, Org.Apache.Http.Conn.IManagedClientConnection, Org.Apache.Http.Conn.IConnectionReleaseTrigger, Org.Apache.Http.IHttpClientConnection, Org.Apache.Http.IHttpInetConnection, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.IHttpConnection {
		// constructors
		protected SingleClientConnManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		protected SingleClientConnManager (SingleClientConnManager __self, SingleClientConnManager.PoolEntry p1, Org.Apache.Http.Conn.Routing.HttpRoute p2);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
	public class PoolEntry : Org.Apache.Http.Impl.Conn.AbstractPoolEntry, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected SingleClientConnManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		protected SingleClientConnManager (SingleClientConnManager __self);
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		protected virtual void Close ();
		protected virtual void Shutdown ();
	}
}
```

### New Type Org.Apache.Http.Impl.Conn.Wire

```
public class Wire : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected Wire (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Wire (Org.Apache.Commons.Logging.ILog log);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Enabled ();
	public virtual void Input (string s);
	public virtual void Input (System.IO.Stream instream);
	public virtual void Input (int b);
	public virtual void Input (byte[] b, int off, int len);
	public virtual void Input (byte[] b);
	public virtual void Output (System.IO.Stream outstream);
	public virtual void Output (int b);
	public virtual void Output (byte[] b, int off, int len);
	public virtual void Output (byte[] b);
	public virtual void Output (string s);
}
```

## New Namespace Org.Apache.Http.Impl.Conn.Tsccm

### New Type Org.Apache.Http.Impl.Conn.Tsccm.AbstractConnPool

```
public abstract class AbstractConnPool : Java.Lang.Object, IRefQueueHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractConnPool (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractConnPool ();
	// properties
	protected Org.Apache.Http.Impl.Conn.IdleConnectionHandler IdleConnHandler { get; set; }
	protected bool IsShutDown { get; set; }
	protected System.Collections.ICollection IssuedConnections { get; set; }
	protected int NumConnections { get; set; }
	protected Java.Util.Concurrent.Locks.ILock PoolLock { get; set; }
	protected Java.Lang.Ref.ReferenceQueue RefQueue { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual void CloseConnection (Org.Apache.Http.Conn.IOperatedClientConnection conn);
	public virtual void CloseExpiredConnections ();
	public virtual void CloseIdleConnections (long idletime, Java.Util.Concurrent.TimeUnit tunit);
	public virtual void DeleteClosedConnections ();
	public virtual void EnableConnectionGC ();
	public virtual void FreeEntry (BasicPoolEntry entry, bool reusable, long validDuration, Java.Util.Concurrent.TimeUnit timeUnit);
	public BasicPoolEntry GetEntry (Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Object state, long timeout, Java.Util.Concurrent.TimeUnit tunit);
	protected virtual void HandleLostEntry (Org.Apache.Http.Conn.Routing.HttpRoute route);
	public virtual void HandleReference (Java.Lang.Ref.Reference ref);
	public virtual IPoolEntryRequest RequestPoolEntry (Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Object state);
	public virtual void Shutdown ();
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.BasicPooledConnAdapter

```
public class BasicPooledConnAdapter : Org.Apache.Http.Impl.Conn.AbstractPooledConnAdapter, Org.Apache.Http.Conn.IManagedClientConnection, Org.Apache.Http.Conn.IConnectionReleaseTrigger, Org.Apache.Http.IHttpClientConnection, Org.Apache.Http.IHttpInetConnection, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.IHttpConnection {
	// constructors
	protected BasicPooledConnAdapter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected BasicPooledConnAdapter (ThreadSafeClientConnManager tsccm, Org.Apache.Http.Impl.Conn.AbstractPoolEntry entry);
	// properties
	protected virtual Org.Apache.Http.Impl.Conn.AbstractPoolEntry PoolEntry { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.BasicPoolEntry

```
public class BasicPoolEntry : Org.Apache.Http.Impl.Conn.AbstractPoolEntry, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected BasicPoolEntry (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicPoolEntry (Org.Apache.Http.Conn.IClientConnectionOperator op, Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Ref.ReferenceQueue queue);
	// properties
	protected Org.Apache.Http.Conn.IOperatedClientConnection Connection { get; }
	protected Org.Apache.Http.Conn.Routing.HttpRoute PlannedRoute { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	protected BasicPoolEntryRef WeakRef { get; }
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.BasicPoolEntryRef

```
public class BasicPoolEntryRef : Java.Lang.Ref.WeakReference, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected BasicPoolEntryRef (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicPoolEntryRef (BasicPoolEntry entry, Java.Lang.Ref.ReferenceQueue queue);
	// properties
	public Org.Apache.Http.Conn.Routing.HttpRoute Route { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.ConnPoolByRoute

```
public class ConnPoolByRoute : Org.Apache.Http.Impl.Conn.Tsccm.AbstractConnPool, IRefQueueHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ConnPoolByRoute (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnPoolByRoute (Org.Apache.Http.Conn.IClientConnectionOperator oper, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected Java.Util.IQueue FreeConnections { get; set; }
	protected int MaxTotalConnections { get; set; }
	protected Org.Apache.Http.Conn.IClientConnectionOperator Operator { get; set; }
	protected System.Collections.IDictionary RouteToPool { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	protected Java.Util.IQueue WaitingThreads { get; set; }
	// methods
	protected virtual BasicPoolEntry CreateEntry (RouteSpecificPool rospl, Org.Apache.Http.Conn.IClientConnectionOperator op);
	protected virtual Java.Util.IQueue CreateFreeConnQueue ();
	protected virtual System.Collections.Generic.IDictionary<Org.Apache.Http.Conn.Routing.HttpRoute,Org.Apache.Http.Impl.Conn.Tsccm.RouteSpecificPool> CreateRouteToPoolMap ();
	protected virtual Java.Util.IQueue CreateWaitingThreadQueue ();
	public override void DeleteClosedConnections ();
	protected virtual void DeleteEntry (BasicPoolEntry entry);
	protected virtual void DeleteLeastUsedEntry ();
	public override void FreeEntry (BasicPoolEntry entry, bool reusable, long validDuration, Java.Util.Concurrent.TimeUnit timeUnit);
	public virtual int GetConnectionsInPool (Org.Apache.Http.Conn.Routing.HttpRoute route);
	protected virtual BasicPoolEntry GetEntryBlocking (Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Object state, long timeout, Java.Util.Concurrent.TimeUnit tunit, WaitingThreadAborter aborter);
	protected virtual BasicPoolEntry GetFreeEntry (RouteSpecificPool rospl, Java.Lang.Object state);
	protected virtual RouteSpecificPool GetRoutePool (Org.Apache.Http.Conn.Routing.HttpRoute route, bool create);
	protected override void HandleLostEntry (Org.Apache.Http.Conn.Routing.HttpRoute route);
	protected virtual RouteSpecificPool NewRouteSpecificPool (Org.Apache.Http.Conn.Routing.HttpRoute route);
	protected virtual WaitingThread NewWaitingThread (Java.Util.Concurrent.Locks.ICondition cond, RouteSpecificPool rospl);
	protected virtual void NotifyWaitingThread (RouteSpecificPool rospl);
	public override IPoolEntryRequest RequestPoolEntry (Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Object state);
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.IPoolEntryRequest

```
public interface IPoolEntryRequest : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void AbortRequest ();
	public virtual BasicPoolEntry GetPoolEntry (long timeout, Java.Util.Concurrent.TimeUnit tunit);
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.IRefQueueHandler

```
public interface IRefQueueHandler : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void HandleReference (Java.Lang.Ref.Reference ref);
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.RefQueueWorker

```
public class RefQueueWorker : Java.Lang.Object, Java.Lang.IRunnable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RefQueueWorker (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RefQueueWorker (Java.Lang.Ref.ReferenceQueue queue, IRefQueueHandler handler);
	// properties
	protected IRefQueueHandler RefHandler { get; set; }
	protected Java.Lang.Ref.ReferenceQueue RefQueue { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	protected Java.Lang.Thread WorkerThread { get; set; }
	// methods
	public virtual void Run ();
	public virtual void Shutdown ();
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.RouteSpecificPool

```
public class RouteSpecificPool : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected RouteSpecificPool (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RouteSpecificPool (Org.Apache.Http.Conn.Routing.HttpRoute route, int maxEntries);
	// properties
	public virtual int Capacity { get; }
	public int EntryCount { get; }
	protected Java.Util.LinkedList FreeEntries { get; set; }
	public virtual bool HasThread { get; }
	public virtual bool IsUnused { get; }
	public int MaxEntries { get; }
	protected int NumEntries { get; set; }
	public Org.Apache.Http.Conn.Routing.HttpRoute Route { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	protected Java.Util.IQueue WaitingThreads { get; set; }
	// methods
	public virtual BasicPoolEntry AllocEntry (Java.Lang.Object state);
	public virtual void CreatedEntry (BasicPoolEntry entry);
	public virtual bool DeleteEntry (BasicPoolEntry entry);
	public virtual void DropEntry ();
	public virtual void FreeEntry (BasicPoolEntry entry);
	public virtual WaitingThread NextThread ();
	public virtual void QueueThread (WaitingThread wt);
	public virtual void RemoveThread (WaitingThread wt);
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.ThreadSafeClientConnManager

```
public class ThreadSafeClientConnManager : Java.Lang.Object, Org.Apache.Http.Conn.IClientConnectionManager, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ThreadSafeClientConnManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ThreadSafeClientConnManager (Org.Apache.Http.Params.IHttpParams params, Org.Apache.Http.Conn.Schemes.SchemeRegistry schreg);
	// properties
	protected AbstractConnPool ConnectionPool { get; set; }
	public virtual int ConnectionsInPool { get; }
	protected Org.Apache.Http.Conn.IClientConnectionOperator ConnOperator { get; set; }
	public virtual Org.Apache.Http.Conn.Schemes.SchemeRegistry SchemeRegistry { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void CloseExpiredConnections ();
	public virtual void CloseIdleConnections (long idleTimeout, Java.Util.Concurrent.TimeUnit tunit);
	protected virtual Org.Apache.Http.Conn.IClientConnectionOperator CreateConnectionOperator (Org.Apache.Http.Conn.Schemes.SchemeRegistry schreg);
	protected virtual AbstractConnPool CreateConnectionPool (Org.Apache.Http.Params.IHttpParams params);
	public virtual int GetConnectionsInPool (Org.Apache.Http.Conn.Routing.HttpRoute route);
	public virtual void ReleaseConnection (Org.Apache.Http.Conn.IManagedClientConnection conn, long validDuration, Java.Util.Concurrent.TimeUnit timeUnit);
	public virtual Org.Apache.Http.Conn.IClientConnectionRequest RequestConnection (Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Object state);
	public virtual void Shutdown ();
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.WaitingThread

```
public class WaitingThread : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WaitingThread (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WaitingThread (Java.Util.Concurrent.Locks.ICondition cond, RouteSpecificPool pool);
	// properties
	public Java.Util.Concurrent.Locks.ICondition Condition { get; }
	public RouteSpecificPool Pool { get; }
	public Java.Lang.Thread Thread { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Await (Java.Util.Date deadline);
	public virtual void Interrupt ();
	public virtual void Wakeup ();
}
```

### New Type Org.Apache.Http.Impl.Conn.Tsccm.WaitingThreadAborter

```
public class WaitingThreadAborter : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected WaitingThreadAborter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WaitingThreadAborter ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Abort ();
	public virtual void SetWaitingThread (WaitingThread waitingThread);
}
```

## New Namespace Org.Apache.Http.Impl.Cookie

### New Type Org.Apache.Http.Impl.Cookie.AbstractCookieAttributeHandler

```
public abstract class AbstractCookieAttributeHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractCookieAttributeHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractCookieAttributeHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.AbstractCookieSpec

```
public abstract class AbstractCookieSpec : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractCookieSpec (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractCookieSpec ();
	// properties
	protected virtual System.Collections.Generic.ICollection<Org.Apache.Http.Cookies.ICookieAttributeHandler> AttribHandlers { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual int Version { get; }
	public virtual Org.Apache.Http.IHeader VersionHeader { get; }
	// methods
	protected virtual Org.Apache.Http.Cookies.ICookieAttributeHandler FindAttribHandler (string name);
	public virtual System.Collections.Generic.IList<Org.Apache.Http.IHeader> FormatCookies (System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> cookies);
	protected virtual Org.Apache.Http.Cookies.ICookieAttributeHandler GetAttribHandler (string name);
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> Parse (Org.Apache.Http.IHeader header, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void RegisterAttribHandler (string name, Org.Apache.Http.Cookies.ICookieAttributeHandler handler);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BasicClientCookie

```
public class BasicClientCookie : Java.Lang.Object, Java.Lang.ICloneable, Org.Apache.Http.Cookies.IClientCookie, Org.Apache.Http.Cookies.ISetCookie, Android.Runtime.IJavaObject, System.IDisposable, Org.Apache.Http.Cookies.ICookie {
	// constructors
	protected BasicClientCookie (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicClientCookie (string name, string value);
	// properties
	public virtual string Comment { get; set; }
	public virtual string CommentURL { get; }
	public virtual string Domain { get; set; }
	public virtual Java.Util.Date ExpiryDate { get; set; }
	public virtual bool IsPersistent { get; }
	public virtual bool IsSecure { get; }
	public virtual string Name { get; }
	public virtual string Path { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual string Value { get; set; }
	public virtual int Version { get; set; }
	// methods
	public virtual Java.Lang.Object Clone ();
	public virtual bool ContainsAttribute (string name);
	public virtual string GetAttribute (string name);
	public virtual int[] GetPorts ();
	public virtual bool IsExpired (Java.Util.Date date);
	public virtual void SetAttribute (string name, string value);
	public virtual void SetComment (string comment);
	public virtual void SetDomain (string domain);
	public virtual void SetExpiryDate (Java.Util.Date date);
	public virtual void SetPath (string path);
	public virtual void SetSecure (bool secure);
	public virtual void SetValue (string value);
	public virtual void SetVersion (int version);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const string CommentAttr = "comment";
		public static const string CommenturlAttr = "commenturl";
		public static const string DiscardAttr = "discard";
		public static const string DomainAttr = "domain";
		public static const string ExpiresAttr = "expires";
		public static const string MaxAgeAttr = "max-age";
		public static const string PathAttr = "path";
		public static const string PortAttr = "port";
		public static const string SecureAttr = "secure";
		public static const string VersionAttr = "version";
	}
}
```

### New Type Org.Apache.Http.Impl.Cookie.BasicClientCookie2

```
public class BasicClientCookie2 : Org.Apache.Http.Impl.Cookie.BasicClientCookie, Org.Apache.Http.Cookies.ISetCookie2, Org.Apache.Http.Cookies.ISetCookie, Org.Apache.Http.Cookies.ICookie, Android.Runtime.IJavaObject, System.IDisposable, Java.Lang.ICloneable, Org.Apache.Http.Cookies.IClientCookie {
	// constructors
	protected BasicClientCookie2 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicClientCookie2 (string name, string value);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void SetCommentURL (string commentURL);
	public virtual void SetDiscard (bool discard);
	public virtual void SetPorts (int[] ports);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BasicCommentHandler

```
public class BasicCommentHandler : Org.Apache.Http.Impl.Cookie.AbstractCookieAttributeHandler, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicCommentHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicCommentHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BasicDomainHandler

```
public class BasicDomainHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicDomainHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicDomainHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BasicExpiresHandler

```
public class BasicExpiresHandler : Org.Apache.Http.Impl.Cookie.AbstractCookieAttributeHandler, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicExpiresHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicExpiresHandler (string[] datepatterns);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BasicMaxAgeHandler

```
public class BasicMaxAgeHandler : Org.Apache.Http.Impl.Cookie.AbstractCookieAttributeHandler, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicMaxAgeHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicMaxAgeHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BasicPathHandler

```
public class BasicPathHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicPathHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicPathHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BasicSecureHandler

```
public class BasicSecureHandler : Org.Apache.Http.Impl.Cookie.AbstractCookieAttributeHandler, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BasicSecureHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicSecureHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BestMatchSpec

```
public class BestMatchSpec : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BestMatchSpec (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BestMatchSpec ();
	public BestMatchSpec (string[] datepatterns, bool oneHeader);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public virtual int Version { get; }
	public virtual Org.Apache.Http.IHeader VersionHeader { get; }
	// methods
	public virtual System.Collections.Generic.IList<Org.Apache.Http.IHeader> FormatCookies (System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> cookies);
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> Parse (Org.Apache.Http.IHeader header, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BestMatchSpecFactory

```
public class BestMatchSpecFactory : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieSpecFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BestMatchSpecFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BestMatchSpecFactory ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Cookies.ICookieSpec NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BrowserCompatSpec

```
public class BrowserCompatSpec : Org.Apache.Http.Impl.Cookie.CookieSpecBase, Org.Apache.Http.Cookies.ICookieSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BrowserCompatSpec (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BrowserCompatSpec ();
	public BrowserCompatSpec (string[] datepatterns);
	// properties
	protected static System.Collections.Generic.IList<string> DatePatterns { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public override int Version { get; }
	public override Org.Apache.Http.IHeader VersionHeader { get; }
	// methods
	public override System.Collections.Generic.IList<Org.Apache.Http.IHeader> FormatCookies (System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> cookies);
	public override System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> Parse (Org.Apache.Http.IHeader header, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.BrowserCompatSpecFactory

```
public class BrowserCompatSpecFactory : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieSpecFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BrowserCompatSpecFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BrowserCompatSpecFactory ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Cookies.ICookieSpec NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Cookie.CookieSpecBase

```
public abstract class CookieSpecBase : Org.Apache.Http.Impl.Cookie.AbstractCookieSpec, Org.Apache.Http.Cookies.ICookieSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected CookieSpecBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CookieSpecBase ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected static string GetDefaultDomain (Org.Apache.Http.Cookies.CookieOrigin origin);
	protected static string GetDefaultPath (Org.Apache.Http.Cookies.CookieOrigin origin);
	public override bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	protected virtual System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> Parse (Org.Apache.Http.IHeaderElement[] elems, Org.Apache.Http.Cookies.CookieOrigin origin);
	public override void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.DateParseException

```
public class DateParseException : Java.Lang.Exception, Android.Runtime.IJavaObject, System.IDisposable, Java.IO.ISerializable, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	protected DateParseException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DateParseException ();
	public DateParseException (string message);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Org.Apache.Http.Impl.Cookie.DateUtils

```
public sealed class DateUtils : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// fields
	public static const string PatternAsctime = "EEE MMM d HH:mm:ss yyyy";
	public static const string PatternRfc1036 = "EEEE, dd-MMM-yy HH:mm:ss zzz";
	public static const string PatternRfc1123 = "EEE, dd MMM yyyy HH:mm:ss zzz";
	// properties
	public static Java.Util.TimeZone Gmt { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public static string FormatDate (Java.Util.Date date);
	public static string FormatDate (Java.Util.Date date, string pattern);
	public static Java.Util.Date ParseDate (string dateValue);
	public static Java.Util.Date ParseDate (string dateValue, string[] dateFormats);
	public static Java.Util.Date ParseDate (string dateValue, string[] dateFormats, Java.Util.Date startDate);
}
```

### New Type Org.Apache.Http.Impl.Cookie.NetscapeDomainHandler

```
public class NetscapeDomainHandler : Org.Apache.Http.Impl.Cookie.BasicDomainHandler, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected NetscapeDomainHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NetscapeDomainHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Org.Apache.Http.Impl.Cookie.NetscapeDraftHeaderParser

```
public class NetscapeDraftHeaderParser : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected NetscapeDraftHeaderParser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NetscapeDraftHeaderParser ();
	// properties
	public static NetscapeDraftHeaderParser Default { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.IHeaderElement ParseHeader (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.Message.ParserCursor cursor);
}
```

### New Type Org.Apache.Http.Impl.Cookie.NetscapeDraftSpec

```
public class NetscapeDraftSpec : Org.Apache.Http.Impl.Cookie.CookieSpecBase, Org.Apache.Http.Cookies.ICookieSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected NetscapeDraftSpec (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NetscapeDraftSpec ();
	public NetscapeDraftSpec (string[] datepatterns);
	// fields
	protected static const string ExpiresPattern = "EEE, dd-MMM-yyyy HH:mm:ss z";
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public override int Version { get; }
	public override Org.Apache.Http.IHeader VersionHeader { get; }
	// methods
	public override System.Collections.Generic.IList<Org.Apache.Http.IHeader> FormatCookies (System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> cookies);
	public override System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> Parse (Org.Apache.Http.IHeader header, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.NetscapeDraftSpecFactory

```
public class NetscapeDraftSpecFactory : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieSpecFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected NetscapeDraftSpecFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NetscapeDraftSpecFactory ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Cookies.ICookieSpec NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2109DomainHandler

```
public class RFC2109DomainHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2109DomainHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2109DomainHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2109Spec

```
public class RFC2109Spec : Org.Apache.Http.Impl.Cookie.CookieSpecBase, Org.Apache.Http.Cookies.ICookieSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2109Spec (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2109Spec ();
	public RFC2109Spec (string[] datepatterns, bool oneHeader);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	public override int Version { get; }
	public override Org.Apache.Http.IHeader VersionHeader { get; }
	// methods
	protected virtual void FormatCookieAsVer (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.Cookies.ICookie cookie, int version);
	public override System.Collections.Generic.IList<Org.Apache.Http.IHeader> FormatCookies (System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> cookies);
	protected virtual void FormatParamAsVer (Org.Apache.Http.Util.CharArrayBuffer buffer, string name, string value, int version);
	public override System.Collections.Generic.IList<Org.Apache.Http.Cookies.ICookie> Parse (Org.Apache.Http.IHeader header, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2109SpecFactory

```
public class RFC2109SpecFactory : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieSpecFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2109SpecFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2109SpecFactory ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Cookies.ICookieSpec NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2109VersionHandler

```
public class RFC2109VersionHandler : Org.Apache.Http.Impl.Cookie.AbstractCookieAttributeHandler, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2109VersionHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2109VersionHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2965CommentUrlAttributeHandler

```
public class RFC2965CommentUrlAttributeHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2965CommentUrlAttributeHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2965CommentUrlAttributeHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string commenturl);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2965DiscardAttributeHandler

```
public class RFC2965DiscardAttributeHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2965DiscardAttributeHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2965DiscardAttributeHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string commenturl);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2965DomainAttributeHandler

```
public class RFC2965DomainAttributeHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2965DomainAttributeHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2965DomainAttributeHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool DomainMatch (string host, string domain);
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string domain);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2965PortAttributeHandler

```
public class RFC2965PortAttributeHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2965PortAttributeHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2965PortAttributeHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string portValue);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2965Spec

```
public class RFC2965Spec : Org.Apache.Http.Impl.Cookie.RFC2109Spec, Org.Apache.Http.Cookies.ICookieSpec, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2965Spec (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2965Spec ();
	public RFC2965Spec (string[] datepatterns, bool oneHeader);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2965SpecFactory

```
public class RFC2965SpecFactory : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieSpecFactory, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2965SpecFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2965SpecFactory ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.Cookies.ICookieSpec NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

### New Type Org.Apache.Http.Impl.Cookie.RFC2965VersionAttributeHandler

```
public class RFC2965VersionAttributeHandler : Java.Lang.Object, Org.Apache.Http.Cookies.ICookieAttributeHandler, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected RFC2965VersionAttributeHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RFC2965VersionAttributeHandler ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual bool Match (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
	public virtual void Parse (Org.Apache.Http.Cookies.ISetCookie cookie, string value);
	public virtual void Validate (Org.Apache.Http.Cookies.ICookie cookie, Org.Apache.Http.Cookies.CookieOrigin origin);
}
```

## New Namespace Org.Apache.Http.Impl.Entity

### New Type Org.Apache.Http.Impl.Entity.EntityDeserializer

```
public class EntityDeserializer : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected EntityDeserializer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public EntityDeserializer (Org.Apache.Http.Entity.IContentLengthStrategy lenStrategy);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.IHttpEntity Deserialize (Org.Apache.Http.IO.ISessionInputBuffer inbuffer, Org.Apache.Http.IHttpMessage message);
	protected virtual Org.Apache.Http.Entity.BasicHttpEntity DoDeserialize (Org.Apache.Http.IO.ISessionInputBuffer inbuffer, Org.Apache.Http.IHttpMessage message);
}
```

### New Type Org.Apache.Http.Impl.Entity.EntitySerializer

```
public class EntitySerializer : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected EntitySerializer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public EntitySerializer (Org.Apache.Http.Entity.IContentLengthStrategy lenStrategy);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual System.IO.Stream DoSerialize (Org.Apache.Http.IO.ISessionOutputBuffer outbuffer, Org.Apache.Http.IHttpMessage message);
	public virtual void Serialize (Org.Apache.Http.IO.ISessionOutputBuffer outbuffer, Org.Apache.Http.IHttpMessage message, Org.Apache.Http.IHttpEntity entity);
}
```

### New Type Org.Apache.Http.Impl.Entity.LaxContentLengthStrategy

```
public class LaxContentLengthStrategy : Java.Lang.Object, Org.Apache.Http.Entity.IContentLengthStrategy, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected LaxContentLengthStrategy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LaxContentLengthStrategy ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual long DetermineLength (Org.Apache.Http.IHttpMessage message);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int Chunked;
		public static const int Identity;
	}
}
```

### New Type Org.Apache.Http.Impl.Entity.StrictContentLengthStrategy

```
public class StrictContentLengthStrategy : Java.Lang.Object, Org.Apache.Http.Entity.IContentLengthStrategy, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected StrictContentLengthStrategy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StrictContentLengthStrategy ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual long DetermineLength (Org.Apache.Http.IHttpMessage message);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int Chunked;
		public static const int Identity;
	}
}
```

## New Namespace Org.Apache.Http.Impl.IO

### New Type Org.Apache.Http.Impl.IO.AbstractMessageParser

```
public abstract class AbstractMessageParser : Java.Lang.Object, Org.Apache.Http.IO.IHttpMessageParser, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractMessageParser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractMessageParser (Org.Apache.Http.IO.ISessionInputBuffer buffer, Org.Apache.Http.Message.ILineParser parser, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected Org.Apache.Http.Message.ILineParser LineParser { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.IHttpMessage Parse ();
	protected virtual Org.Apache.Http.IHttpMessage ParseHead (Org.Apache.Http.IO.ISessionInputBuffer sessionBuffer);
	public static Org.Apache.Http.IHeader[] ParseHeaders (Org.Apache.Http.IO.ISessionInputBuffer inbuffer, int maxHeaderCount, int maxLineLen, Org.Apache.Http.Message.ILineParser parser);
}
```

### New Type Org.Apache.Http.Impl.IO.AbstractMessageWriter

```
public abstract class AbstractMessageWriter : Java.Lang.Object, Org.Apache.Http.IO.IHttpMessageWriter, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractMessageWriter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractMessageWriter (Org.Apache.Http.IO.ISessionOutputBuffer buffer, Org.Apache.Http.Message.ILineFormatter formatter, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected Org.Apache.Http.Util.CharArrayBuffer LineBuf { get; set; }
	protected Org.Apache.Http.Message.ILineFormatter LineFormatter { get; set; }
	protected Org.Apache.Http.IO.ISessionOutputBuffer SessionBuffer { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Write (Org.Apache.Http.IHttpMessage message);
	protected virtual void WriteHeadLine (Org.Apache.Http.IHttpMessage message);
}
```

### New Type Org.Apache.Http.Impl.IO.AbstractSessionInputBuffer

```
public abstract class AbstractSessionInputBuffer : Java.Lang.Object, Org.Apache.Http.IO.ISessionInputBuffer, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractSessionInputBuffer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractSessionInputBuffer ();
	// properties
	protected virtual bool HasBufferedData { get; }
	public virtual Org.Apache.Http.IO.IHttpTransportMetrics Metrics { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected virtual int FillBuffer ();
	protected virtual void Init (System.IO.Stream instream, int buffersize, Org.Apache.Http.Params.IHttpParams params);
	public virtual bool IsDataAvailable (int timeout);
	public virtual int Read ();
	public virtual int Read (byte[] b, int off, int len);
	public virtual int Read (byte[] b);
	public virtual string ReadLine ();
	public virtual int ReadLine (Org.Apache.Http.Util.CharArrayBuffer charbuffer);
}
```

### New Type Org.Apache.Http.Impl.IO.AbstractSessionOutputBuffer

```
public abstract class AbstractSessionOutputBuffer : Java.Lang.Object, Org.Apache.Http.IO.ISessionOutputBuffer, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected AbstractSessionOutputBuffer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractSessionOutputBuffer ();
	// properties
	public virtual Org.Apache.Http.IO.IHttpTransportMetrics Metrics { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Flush ();
	protected virtual void FlushBuffer ();
	protected virtual void Init (System.IO.Stream outstream, int buffersize, Org.Apache.Http.Params.IHttpParams params);
	public virtual void Write (int b);
	public virtual void Write (byte[] b, int off, int len);
	public virtual void Write (byte[] b);
	public virtual void WriteLine (string s);
	public virtual void WriteLine (Org.Apache.Http.Util.CharArrayBuffer s);
}
```

### New Type Org.Apache.Http.Impl.IO.ChunkedInputStream

```
public class ChunkedInputStream : Java.IO.InputStream, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ChunkedInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ChunkedInputStream (Org.Apache.Http.IO.ISessionInputBuffer in);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Org.Apache.Http.IHeader[] GetFooters ();
	public override int Read ();
}
```

### New Type Org.Apache.Http.Impl.IO.ChunkedOutputStream

```
public class ChunkedOutputStream : Java.IO.OutputStream, Java.IO.ICloseable, Java.IO.IFlushable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ChunkedOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ChunkedOutputStream (Org.Apache.Http.IO.ISessionOutputBuffer out);
	public ChunkedOutputStream (Org.Apache.Http.IO.ISessionOutputBuffer out, int bufferSize);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void Finish ();
	protected virtual void FlushCache ();
	protected virtual void FlushCacheWithAppend (byte[] bufferToAppend, int off, int len);
	public override void Write (int b);
	protected virtual void WriteClosingChunk ();
}
```

### New Type Org.Apache.Http.Impl.IO.ContentLengthInputStream

```
public class ContentLengthInputStream : Java.IO.InputStream, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ContentLengthInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ContentLengthInputStream (Org.Apache.Http.IO.ISessionInputBuffer in, long contentLength);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override int Read ();
}
```

### New Type Org.Apache.Http.Impl.IO.ContentLengthOutputStream

```
public class ContentLengthOutputStream : Java.IO.OutputStream, Java.IO.ICloseable, Java.IO.IFlushable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected ContentLengthOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ContentLengthOutputStream (Org.Apache.Http.IO.ISessionOutputBuffer out, long contentLength);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Write (int b);
}
```

### New Type Org.Apache.Http.Impl.IO.HttpRequestParser

```
public class HttpRequestParser : Org.Apache.Http.Impl.IO.AbstractMessageParser, Org.Apache.Http.IO.IHttpMessageParser, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected HttpRequestParser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpRequestParser (Org.Apache.Http.IO.ISessionInputBuffer buffer, Org.Apache.Http.Message.ILineParser parser, Org.Apache.Http.IHttpRequestFactory requestFactory, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected override Org.Apache.Http.IHttpMessage ParseHead (Org.Apache.Http.IO.ISessionInputBuffer sessionBuffer);
}
```

### New Type Org.Apache.Http.Impl.IO.HttpRequestWriter

```
public class HttpRequestWriter : Org.Apache.Http.Impl.IO.AbstractMessageWriter, Org.Apache.Http.IO.IHttpMessageWriter, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected HttpRequestWriter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpRequestWriter (Org.Apache.Http.IO.ISessionOutputBuffer buffer, Org.Apache.Http.Message.ILineFormatter formatter, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected override void WriteHeadLine (Org.Apache.Http.IHttpMessage message);
}
```

### New Type Org.Apache.Http.Impl.IO.HttpResponseParser

```
public class HttpResponseParser : Org.Apache.Http.Impl.IO.AbstractMessageParser, Org.Apache.Http.IO.IHttpMessageParser, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected HttpResponseParser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpResponseParser (Org.Apache.Http.IO.ISessionInputBuffer buffer, Org.Apache.Http.Message.ILineParser parser, Org.Apache.Http.IHttpResponseFactory responseFactory, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected override Org.Apache.Http.IHttpMessage ParseHead (Org.Apache.Http.IO.ISessionInputBuffer sessionBuffer);
}
```

### New Type Org.Apache.Http.Impl.IO.HttpResponseWriter

```
public class HttpResponseWriter : Org.Apache.Http.Impl.IO.AbstractMessageWriter, Org.Apache.Http.IO.IHttpMessageWriter, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected HttpResponseWriter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpResponseWriter (Org.Apache.Http.IO.ISessionOutputBuffer buffer, Org.Apache.Http.Message.ILineFormatter formatter, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	protected override void WriteHeadLine (Org.Apache.Http.IHttpMessage message);
}
```

### New Type Org.Apache.Http.Impl.IO.HttpTransportMetricsImpl

```
public class HttpTransportMetricsImpl : Java.Lang.Object, Org.Apache.Http.IO.IHttpTransportMetrics, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected HttpTransportMetricsImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpTransportMetricsImpl ();
	// properties
	public virtual long BytesTransferred { get; set; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void IncrementBytesTransferred (long count);
	public virtual void Reset ();
}
```

### New Type Org.Apache.Http.Impl.IO.IdentityInputStream

```
public class IdentityInputStream : Java.IO.InputStream, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected IdentityInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public IdentityInputStream (Org.Apache.Http.IO.ISessionInputBuffer in);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override int Read ();
}
```

### New Type Org.Apache.Http.Impl.IO.IdentityOutputStream

```
public class IdentityOutputStream : Java.IO.OutputStream, Java.IO.ICloseable, Java.IO.IFlushable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected IdentityOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public IdentityOutputStream (Org.Apache.Http.IO.ISessionOutputBuffer out);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override void Write (int b);
}
```

### New Type Org.Apache.Http.Impl.IO.SocketInputBuffer

```
public class SocketInputBuffer : Org.Apache.Http.Impl.IO.AbstractSessionInputBuffer, Org.Apache.Http.IO.ISessionInputBuffer, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected SocketInputBuffer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SocketInputBuffer (Java.Net.Socket socket, int buffersize, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override bool IsDataAvailable (int timeout);
}
```

### New Type Org.Apache.Http.Impl.IO.SocketOutputBuffer

```
public class SocketOutputBuffer : Org.Apache.Http.Impl.IO.AbstractSessionOutputBuffer, Org.Apache.Http.IO.ISessionOutputBuffer, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected SocketOutputBuffer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SocketOutputBuffer (Java.Net.Socket socket, int buffersize, Org.Apache.Http.Params.IHttpParams params);
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
}
```
