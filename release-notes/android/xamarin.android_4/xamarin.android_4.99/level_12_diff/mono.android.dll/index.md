---
id: 22E2BB3C-F15C-46A1-9F8E-20A932CC3DD0
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

### Type Changed: Android.Accounts.AuthenticatorDescription

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
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
	public Android.Database.ICursor ManagedQuery (Android.Net.Uri uri, string[] projection, string selection, string[] selectionArgs, string sortOrder);

	[Obsolete ("deprecated")]
	protected virtual Dialog OnCreateDialog (int id);

	[Obsolete ("deprecated")]
	protected virtual void OnPrepareDialog (int id, Dialog dialog);

	[Obsolete ("deprecated")]
	public virtual void SetPersistent (bool isPersistent);

	[Obsolete ("deprecated")]
	public virtual void StartManagingCursor (Android.Database.ICursor c);

	[Obsolete ("deprecated")]
	public virtual void StopManagingCursor (Android.Database.ICursor c);
```

### Type Changed: Android.App.ActivityManager

Obsoleted method:

```
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

### Type Changed: Android.App.AlertDialog

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void SetButton (Java.Lang.ICharSequence text, Android.OS.Message msg);

	[Obsolete ("deprecated")]
	public virtual void SetButton2 (Java.Lang.ICharSequence text, Android.OS.Message msg);

	[Obsolete ("deprecated")]
	public virtual void SetButton3 (Java.Lang.ICharSequence text, Android.OS.Message msg);
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

### Type Changed: Android.App.Notification

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
	public virtual void SetLatestEventInfo (Android.Content.Context context, Java.Lang.ICharSequence contentTitle, Java.Lang.ICharSequence contentText, PendingIntent contentIntent);
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

### Type Changed: Android.Content.SyncAdapterType

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

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
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
	public virtual bool IsBlob (int row, int col);

	[Obsolete ("deprecated")]
	public virtual bool IsFloat (int row, int col);

	[Obsolete ("deprecated")]
	public virtual bool IsLong (int row, int col);

	[Obsolete ("deprecated")]
	public virtual bool IsNull (int row, int col);

	[Obsolete ("deprecated")]
	public virtual bool IsString (int row, int col);
```

## Namespace Android.Database.Sqlite

### Type Changed: Android.Database.Sqlite.SQLiteDatabase

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void MarkTableSyncable (string table, string deletedTable);

	[Obsolete ("deprecated")]
	public virtual void MarkTableSyncable (string table, string foreignKey, string updateTable);

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

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual string BuildQuery (string[] projectionIn, string selection, string[] selectionArgs, string groupBy, string having, string sortOrder, string limit);
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

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Graphics.Bitmap.CompressFormat

Removed properties:

```
public static Bitmap.CompressFormat Jpeg { get; set; }
	public static Bitmap.CompressFormat Png { get; set; }
```

Added properties:

```
public static Bitmap.CompressFormat Jpeg { get; }
	public static Bitmap.CompressFormat Png { get; }
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

## Namespace Android.Media

### Type Changed: Android.Media.AudioManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Route GetRouting (Mode mode);

	[Obsolete ("deprecated")]
	public virtual void SetRouting (Mode mode, Route routes, Route mask);
```

## Namespace Android.Net

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

### Type Changed: Android.Net.NetworkInfo

### Type Changed: Android.Net.NetworkInfo.DetailedState

Removed properties:

```
public static NetworkInfo.DetailedState Authenticating { get; set; }
	public static NetworkInfo.DetailedState Connected { get; set; }
	public static NetworkInfo.DetailedState Connecting { get; set; }
	public static NetworkInfo.DetailedState Disconnected { get; set; }
	public static NetworkInfo.DetailedState Disconnecting { get; set; }
	public static NetworkInfo.DetailedState Failed { get; set; }
	public static NetworkInfo.DetailedState Idle { get; set; }
	public static NetworkInfo.DetailedState ObtainingIpaddr { get; set; }
	public static NetworkInfo.DetailedState Scanning { get; set; }
	public static NetworkInfo.DetailedState Suspended { get; set; }
```

Added properties:

```
public static NetworkInfo.DetailedState Authenticating { get; }
	public static NetworkInfo.DetailedState Connected { get; }
	public static NetworkInfo.DetailedState Connecting { get; }
	public static NetworkInfo.DetailedState Disconnected { get; }
	public static NetworkInfo.DetailedState Disconnecting { get; }
	public static NetworkInfo.DetailedState Failed { get; }
	public static NetworkInfo.DetailedState Idle { get; }
	public static NetworkInfo.DetailedState ObtainingIpaddr { get; }
	public static NetworkInfo.DetailedState Scanning { get; }
	public static NetworkInfo.DetailedState Suspended { get; }
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

### Type Changed: Android.Net.Proxy

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static string GetHost (Android.Content.Context ctx);

	[Obsolete ("deprecated")]
	public static int GetPort (Android.Content.Context ctx);
```

### Type Changed: Android.Net.SSLCertificateSocketFactory

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public override Java.Net.Socket CreateSocket (Java.Net.InetAddress addr, int port);

	[Obsolete ("deprecated")]
	public override Java.Net.Socket CreateSocket (Java.Net.InetAddress addr, int port, Java.Net.InetAddress localAddr, int localPort);

	[Obsolete ("deprecated")]
	public static Javax.Net.Ssl.SSLSocketFactory GetInsecure (int handshakeTimeoutMillis, SSLSessionCache cache);
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
	public static SupplicantState Completed { get; set; }
	public static SupplicantState Disconnected { get; set; }
	public static SupplicantState Dormant { get; set; }
	public static SupplicantState FourWayHandshake { get; set; }
	public static SupplicantState GroupHandshake { get; set; }
	public static SupplicantState Inactive { get; set; }
	public static SupplicantState Invalid { get; set; }
	public static SupplicantState Scanning { get; set; }
	public static SupplicantState Uninitialized { get; set; }
```

Added properties:

```
public static SupplicantState Associated { get; }
	public static SupplicantState Associating { get; }
	public static SupplicantState Completed { get; }
	public static SupplicantState Disconnected { get; }
	public static SupplicantState Dormant { get; }
	public static SupplicantState FourWayHandshake { get; }
	public static SupplicantState GroupHandshake { get; }
	public static SupplicantState Inactive { get; }
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
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentUri { get; }
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
	public static Android.Net.Uri ContentGroupUri { get; set; }
	public static Android.Net.Uri ContentLookupUri { get; set; }
	public static Android.Net.Uri ContentStrequentFilterUri { get; set; }
	public static Android.Net.Uri ContentStrequentUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ContentVcardUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentGroupUri { get; }
	public static Android.Net.Uri ContentLookupUri { get; }
	public static Android.Net.Uri ContentStrequentFilterUri { get; }
	public static Android.Net.Uri ContentStrequentUri { get; }
	public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ContentVcardUri { get; }
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

### Type Changed: Android.Provider.ContactsContract.Directory

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
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

Removed property:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentFilterUri { get; }
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

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
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

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
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

### Type Changed: Android.Provider.Settings.Secure

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
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

## Namespace Android.Renderscripts

### Type Changed: Android.Renderscripts.Allocation

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

### Type Changed: Android.Renderscripts.Element.DataKind

Removed properties:

```
public static Element.DataKind PixelA { get; set; }
	public static Element.DataKind PixelL { get; set; }
	public static Element.DataKind PixelLa { get; set; }
	public static Element.DataKind PixelRgb { get; set; }
	public static Element.DataKind PixelRgba { get; set; }
	public static Element.DataKind User { get; set; }
```

Added properties:

```
public static Element.DataKind PixelA { get; }
	public static Element.DataKind PixelL { get; }
	public static Element.DataKind PixelLa { get; }
	public static Element.DataKind PixelRgb { get; }
	public static Element.DataKind PixelRgba { get; }
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
	public static Element.DataType RsAllocation { get; set; }
	public static Element.DataType RsElement { get; set; }
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
	public static Element.DataType RsAllocation { get; }
	public static Element.DataType RsElement { get; }
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

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction.Builder

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

### Type Changed: Android.Renderscripts.RenderScript

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

### Type Changed: Android.Renderscripts.Sampler

### Type Changed: Android.Renderscripts.Sampler.Value

Removed properties:

```
public static Sampler.Value Clamp { get; set; }
	public static Sampler.Value Linear { get; set; }
	public static Sampler.Value LinearMipLinear { get; set; }
	public static Sampler.Value LinearMipNearest { get; set; }
	public static Sampler.Value Nearest { get; set; }
	public static Sampler.Value Wrap { get; set; }
```

Added properties:

```
public static Sampler.Value Clamp { get; }
	public static Sampler.Value Linear { get; }
	public static Sampler.Value LinearMipLinear { get; }
	public static Sampler.Value LinearMipNearest { get; }
	public static Sampler.Value Nearest { get; }
	public static Sampler.Value Wrap { get; }
```

### Type Changed: Android.Renderscripts.Type

### Type Changed: Android.Renderscripts.Type.CubemapFace

Removed properties:

```
public static Type.CubemapFace NegativeX { get; set; }
	public static Type.CubemapFace NegativeY { get; set; }
	public static Type.CubemapFace NegativeZ { get; set; }
	public static Type.CubemapFace PositveX { get; set; }
	public static Type.CubemapFace PositveY { get; set; }
	public static Type.CubemapFace PositveZ { get; set; }
```

Added properties:

```
public static Type.CubemapFace NegativeX { get; }
	public static Type.CubemapFace NegativeY { get; }
	public static Type.CubemapFace NegativeZ { get; }
	public static Type.CubemapFace PositveX { get; }
	public static Type.CubemapFace PositveY { get; }
	public static Type.CubemapFace PositveZ { get; }
```

## Namespace Android.Telephony

### Type Changed: Android.Telephony.NeighboringCellInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
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
	public virtual int GetTextRunCursor (int contextStart, int contextEnd, int flags, int offset, int cursorOpt, Android.Graphics.Paint p);
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

### Type Changed: Android.Views.InputEvent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
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

### Type Changed: Android.Views.MotionEvent

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
	public static MotionEvent Obtain (long downTime, long eventTime, int action, int pointers, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
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
	protected static System.Collections.Generic.IList<int> PressedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> SelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> SelectedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> WindowFocusedStateSet { get; set; }
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
	protected static System.Collections.Generic.IList<int> PressedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> SelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> SelectedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> WindowFocusedStateSet { get; }
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

### Type Changed: Android.Views.WindowManagerLayoutParams

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityEvent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
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

### Type Changed: Android.Views.InputMethods.InputMethodSubtype

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

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void OnConsoleMessage (string message, int lineNumber, string sourceID);
```

### Type Changed: Android.Webkit.WebSettings

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual WebSettings.LayoutAlgorithm GetLayoutAlgorithm ();
```

### Type Changed: Android.Webkit.WebSettings.LayoutAlgorithm

Removed properties:

```
public static WebSettings.LayoutAlgorithm NarrowColumns { get; set; }
	public static WebSettings.LayoutAlgorithm Normal { get; set; }
	public static WebSettings.LayoutAlgorithm SingleColumn { get; set; }
```

Added properties:

```
public static WebSettings.LayoutAlgorithm NarrowColumns { get; }
	public static WebSettings.LayoutAlgorithm Normal { get; }
	public static WebSettings.LayoutAlgorithm SingleColumn { get; }
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

### Type Changed: Android.Webkit.WebView

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void DebugDump ();

	[Obsolete ("deprecated")]
	public static void DisablePlatformNotifications ();

	[Obsolete ("deprecated")]
	public virtual void EmulateShiftHeld ();

	[Obsolete ("deprecated")]
	public static void EnablePlatformNotifications ();

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
	public virtual bool SavePicture (Android.OS.Bundle b, Java.IO.File dest);
```

### Type Changed: Android.Webkit.WebViewClient

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void OnTooManyRedirects (WebView view, Android.OS.Message cancelMsg, Android.OS.Message continueMsg);
```

## Namespace Android.Widget

### Type Changed: Android.Widget.CursorAdapter

Obsoleted method:

```
[Obsolete ("deprecated")]
	protected virtual void Init (Android.Content.Context context, Android.Database.ICursor c, bool autoRequery);
```

### Type Changed: Android.Widget.ImageView

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

### Type Changed: Android.Widget.TextView

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
	public virtual void Send (DatagramPacket pack, sbyte ttl);
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
