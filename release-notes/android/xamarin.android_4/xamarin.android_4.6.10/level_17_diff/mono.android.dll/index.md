---
id: BABB92DB-AA0E-4614-A9A1-B6C8A4D672B0
title: "Mono.Android.dll"
---

# Mono.Android.dll

<h2 id='Android'>Namespace: Android</h2>

<h3 id='Android.IncludeAndroidResourcesFromAttribute'>New Type: Android.IncludeAndroidResourcesFromAttribute</h3>

```
public class IncludeAndroidResourcesFromAttribute : Attribute {
	
	public IncludeAndroidResourcesFromAttribute (string path);
	
	public string InstallInstructions {
		get;
		set;
	}
	public string PackageName {
		get;
		set;
	}
	public string ResourceDirectory {
		get;
	}
}
```

<h2 id='Android.AccessibilityServices'>Namespace: Android.AccessibilityServices</h2>

<h3 id='Android.AccessibilityServices.AccessibilityServiceFlags'>Type Changed: Android.AccessibilityServices.AccessibilityServiceFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.AccessibilityServices.AccessibilityServiceInfo'>Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo</h3>

Added:

```
set;
```

<h3 id='Android.AccessibilityServices.FeedbackFlags'>Type Changed: Android.AccessibilityServices.FeedbackFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.App'>Namespace: Android.App</h2>

<h3 id='Android.App.Activity'>Type Changed: Android.App.Activity</h3>

Added:

```
set;
```

<h3 id='Android.App.ActivityManager'>Type Changed: Android.App.ActivityManager</h3>

Added:

```
set;
 			set;
```

<h3 id='Android.App.BreadCrumbClickFlags'>Type Changed: Android.App.BreadCrumbClickFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.DatePickerDialog'>Type Changed: Android.App.DatePickerDialog</h3>

Added:

```
public void UpdateDate (DateTime date);
```

<h3 id='Android.App.DisableCarModeFlags'>Type Changed: Android.App.DisableCarModeFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.EnableCarModeFlags'>Type Changed: Android.App.EnableCarModeFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.MoveTaskFlags'>Type Changed: Android.App.MoveTaskFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.NotificationDefaults'>Type Changed: Android.App.NotificationDefaults</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.NotificationFlags'>Type Changed: Android.App.NotificationFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.PendingIntentFlags'>Type Changed: Android.App.PendingIntentFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.PopBackStackFlags'>Type Changed: Android.App.PopBackStackFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.RecentTaskFlags'>Type Changed: Android.App.RecentTaskFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.ServiceInfoFlags'>Type Changed: Android.App.ServiceInfoFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.StartCommandFlags'>Type Changed: Android.App.StartCommandFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.StartCommandResult'>Type Changed: Android.App.StartCommandResult</h3>

Added:

```
[Flags]
```

<h2 id='Android.App.Admin'>Namespace: Android.App.Admin</h2>

<h3 id='Android.App.Admin.ResetPasswordFlags'>Type Changed: Android.App.Admin.ResetPasswordFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.App.Admin.WipeDataFlags'>Type Changed: Android.App.Admin.WipeDataFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Content'>Namespace: Android.Content</h2>

<h3 id='Android.Content.ActivityFlags'>Type Changed: Android.Content.ActivityFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.AsyncQueryHandler'>Type Changed: Android.Content.AsyncQueryHandler</h3>

Added:

```
set;
 			set;
```

<h3 id='Android.Content.FileCreationMode'>Type Changed: Android.Content.FileCreationMode</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.FillInFlags'>Type Changed: Android.Content.FillInFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PackageContextFlags'>Type Changed: Android.Content.PackageContextFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Content.PM'>Namespace: Android.Content.PM</h2>

<h3 id='Android.Content.PM.ActivityInfoFlags'>Type Changed: Android.Content.PM.ActivityInfoFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PM.ApplicationInfo'>Type Changed: Android.Content.PM.ApplicationInfo</h3>

Added:

```
set;
```

<h3 id='Android.Content.PM.ApplicationInfoFlags'>Type Changed: Android.Content.PM.ApplicationInfoFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PM.ConfigChanges'>Type Changed: Android.Content.PM.ConfigChanges</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PM.FeatureFlags'>Type Changed: Android.Content.PM.FeatureFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PM.PackageInfo'>Type Changed: Android.Content.PM.PackageInfo</h3>

Added:

```
set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
```

<h3 id='Android.Content.PM.PackageInfoFlags'>Type Changed: Android.Content.PM.PackageInfoFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PM.PermissionGroupInfoFlags'>Type Changed: Android.Content.PM.PermissionGroupInfoFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PM.PermissionInfoFlags'>Type Changed: Android.Content.PM.PermissionInfoFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PM.ProviderInfo'>Type Changed: Android.Content.PM.ProviderInfo</h3>

Added:

```
set;
 		set;
```

<h3 id='Android.Content.PM.ProviderInfoFlags'>Type Changed: Android.Content.PM.ProviderInfoFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Content.PM.ServiceInfoFlags'>Type Changed: Android.Content.PM.ServiceInfoFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Content.Res'>Namespace: Android.Content.Res</h2>

<h3 id='Android.Content.Res.ObbFlags'>Type Changed: Android.Content.Res.ObbFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Database'>Namespace: Android.Database</h2>

<h3 id='Android.Database.CharArrayBuffer'>Type Changed: Android.Database.CharArrayBuffer</h3>

Added:

```
set;
```

<h2 id='Android.Database.Sqlite'>Namespace: Android.Database.Sqlite</h2>

<h3 id='Android.Database.Sqlite.DatabaseOpenFlags'>Type Changed: Android.Database.Sqlite.DatabaseOpenFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Drm'>Namespace: Android.Drm</h2>

<h3 id='Android.Drm.DrmConvertedStatus'>Type Changed: Android.Drm.DrmConvertedStatus</h3>

Added:

```
set;
```

<h2 id='Android.Gestures'>Namespace: Android.Gestures</h2>

<h3 id='Android.Gestures.GestureStroke'>Type Changed: Android.Gestures.GestureStroke</h3>

Added:

```
set;
```

<h2 id='Android.Graphics'>Namespace: Android.Graphics</h2>

<h3 id='Android.Graphics.BitmapFactory'>Type Changed: Android.Graphics.BitmapFactory</h3>

Added:

```
set;
```

<h3 id='Android.Graphics.PaintFlags'>Type Changed: Android.Graphics.PaintFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Graphics.SaveFlags'>Type Changed: Android.Graphics.SaveFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Hardware'>Namespace: Android.Hardware</h2>

<h3 id='Android.Hardware.SensorEvent'>Type Changed: Android.Hardware.SensorEvent</h3>

Added:

```
set;
```

<h2 id='Android.InputMethodServices'>Namespace: Android.InputMethodServices</h2>

<h3 id='Android.InputMethodServices.Keyboard'>Type Changed: Android.InputMethodServices.Keyboard</h3>

Added:

```
set;
```

<h2 id='Android.Media'>Namespace: Android.Media</h2>

<h3 id='Android.Media.MediaCodec'>Type Changed: Android.Media.MediaCodec</h3>

Added:

```
set;
 			set;
 			set;
 			set;
```

<h3 id='Android.Media.MediaCodecBufferFlags'>Type Changed: Android.Media.MediaCodecBufferFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Media.MediaCodecConfigFlags'>Type Changed: Android.Media.MediaCodecConfigFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Media.MediaCodecInfo'>Type Changed: Android.Media.MediaCodecInfo</h3>

Added:

```
set;
 			set;
```

<h3 id='Android.Media.MediaExtractorSampleFlags'>Type Changed: Android.Media.MediaExtractorSampleFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Media.RemoteControlFlags'>Type Changed: Android.Media.RemoteControlFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Media.VolumeNotificationFlags'>Type Changed: Android.Media.VolumeNotificationFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Media.Audiofx'>Namespace: Android.Media.Audiofx</h2>

<h3 id='Android.Media.Audiofx.Equalizer'>Type Changed: Android.Media.Audiofx.Equalizer</h3>

Added:

```
set;
```

<h2 id='Android.Net'>Namespace: Android.Net</h2>

<h3 id='Android.Net.IllegalCharacterFlags'>Type Changed: Android.Net.IllegalCharacterFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Net.Wifi'>Namespace: Android.Net.Wifi</h2>

<h3 id='Android.Net.Wifi.WifiConfiguration'>Type Changed: Android.Net.Wifi.WifiConfiguration</h3>

Added:

```
set;
 			set;
 			set;
 			set;
 			set;
 			set;
 			set;
```

<h2 id='Android.Nfc'>Namespace: Android.Nfc</h2>

<h3 id='Android.Nfc.NdefRecord'>Type Changed: Android.Nfc.NdefRecord</h3>

Added:

```
set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
```

<h2 id='Android.Nfc.Tech'>Namespace: Android.Nfc.Tech</h2>

<h3 id='Android.Nfc.Tech.MifareClassic'>Type Changed: Android.Nfc.Tech.MifareClassic</h3>

Added:

```
set;
 		set;
 		set;
```

<h2 id='Android.OS'>Namespace: Android.OS</h2>

<h3 id='Android.OS.DropBoxManagerFlags'>Type Changed: Android.OS.DropBoxManagerFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.OS.ParcelableWriteFlags'>Type Changed: Android.OS.ParcelableWriteFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.OS.TransactionFlags'>Type Changed: Android.OS.TransactionFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.OS.WakeLockFlags'>Type Changed: Android.OS.WakeLockFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Opengl'>Namespace: Android.Opengl</h2>

<h3 id='Android.Opengl.DebugFlags'>Type Changed: Android.Opengl.DebugFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Provider'>Namespace: Android.Provider</h2>

<h3 id='Android.Provider.Browser'>Type Changed: Android.Provider.Browser</h3>

Added:

```
set;
 		set;
 		set;
```

<h3 id='Android.Provider.SearchRecentSuggestions'>Type Changed: Android.Provider.SearchRecentSuggestions</h3>

Added:

```
set;
 		set;
```

<h3 id='Android.Provider.Settings'>Type Changed: Android.Provider.Settings</h3>

Added:

```
set;
```

<h2 id='Android.Renderscripts'>Namespace: Android.Renderscripts</h2>

<h3 id='Android.Renderscripts.RenderScript'>Type Changed: Android.Renderscripts.RenderScript</h3>

Added:

```
set;
```

<h3 id='Android.Renderscripts.TriangleFlags'>Type Changed: Android.Renderscripts.TriangleFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Telephony'>Namespace: Android.Telephony</h2>

<h3 id='Android.Telephony.PhoneStateListenerFlags'>Type Changed: Android.Telephony.PhoneStateListenerFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Telephony.SmsMessage'>Type Changed: Android.Telephony.SmsMessage</h3>

Added:

```
set;
 			set;
```

<h2 id='Android.Telephony.Gsm'>Namespace: Android.Telephony.Gsm</h2>

<h3 id='Android.Telephony.Gsm.SmsMessage'>Type Changed: Android.Telephony.Gsm.SmsMessage</h3>

Added:

```
set;
 			set;
```

<h2 id='Android.Text'>Namespace: Android.Text</h2>

<h3 id='Android.Text.InputTypes'>Type Changed: Android.Text.InputTypes</h3>

Added:

```
[Flags]
```

<h3 id='Android.Text.TextPaint'>Type Changed: Android.Text.TextPaint</h3>

Added:

```
set;
```

<h2 id='Android.Text.Format'>Namespace: Android.Text.Format</h2>

<h3 id='Android.Text.Format.DateUtils'>Type Changed: Android.Text.Format.DateUtils</h3>

Added:

```
set;
 		set;
```

<h3 id='Android.Text.Format.FormatStyleFlags'>Type Changed: Android.Text.Format.FormatStyleFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Text.Method'>Namespace: Android.Text.Method</h2>

<h3 id='Android.Text.Method.DateKeyListener'>Type Changed: Android.Text.Method.DateKeyListener</h3>

Added:

```
set;
```

<h3 id='Android.Text.Method.DateTimeKeyListener'>Type Changed: Android.Text.Method.DateTimeKeyListener</h3>

Added:

```
set;
```

<h3 id='Android.Text.Method.DialerKeyListener'>Type Changed: Android.Text.Method.DialerKeyListener</h3>

Added:

```
set;
```

<h3 id='Android.Text.Method.TimeKeyListener'>Type Changed: Android.Text.Method.TimeKeyListener</h3>

Added:

```
set;
```

<h2 id='Android.Text.Style'>Namespace: Android.Text.Style</h2>

<h3 id='Android.Text.Style.SuggestionSpanFlags'>Type Changed: Android.Text.Style.SuggestionSpanFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Util'>Namespace: Android.Util</h2>

<h3 id='Android.Util.Base64Flags'>Type Changed: Android.Util.Base64Flags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Util.StateSet'>Type Changed: Android.Util.StateSet</h3>

Added:

```
set;
 		set;
```

<h2 id='Android.Views'>Namespace: Android.Views</h2>

<h3 id='Android.Views.DisplayFlags'>Type Changed: Android.Views.DisplayFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.FeedbackFlags'>Type Changed: Android.Views.FeedbackFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.FocusablesFlags'>Type Changed: Android.Views.FocusablesFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.GravityFlags'>Type Changed: Android.Views.GravityFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.KeyCharacterMap'>Type Changed: Android.Views.KeyCharacterMap</h3>

Added:

```
set;
```

<h3 id='Android.Views.KeyEventFlags'>Type Changed: Android.Views.KeyEventFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.MenuAppendFlags'>Type Changed: Android.Views.MenuAppendFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.MenuPerformFlags'>Type Changed: Android.Views.MenuPerformFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.MotionEventFlags'>Type Changed: Android.Views.MotionEventFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.ShowAsAction'>Type Changed: Android.Views.ShowAsAction</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.SystemUiFlags'>Type Changed: Android.Views.SystemUiFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.View'>Type Changed: Android.Views.View</h3>

Removed:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, ICallback, Drawable.Android.Graphics.Drawables.ICallback {
 	public T FindViewById<T> (int id) where T : View;
```

Added:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, Drawable.Android.Graphics.Drawables.ICallback, ICallback {
 	public T FindViewById<T> (int id) where T : View;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
 		set;
```

<h3 id='Android.Views.WindowManagerFlags'>Type Changed: Android.Views.WindowManagerFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Views.InputMethods'>Namespace: Android.Views.InputMethods</h2>

<h3 id='Android.Views.InputMethods.ExtractedTextFlags'>Type Changed: Android.Views.InputMethods.ExtractedTextFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.InputMethods.GetTextFlags'>Type Changed: Android.Views.InputMethods.GetTextFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.InputMethods.HideSoftInputFlags'>Type Changed: Android.Views.InputMethods.HideSoftInputFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.InputMethods.ImeFlags'>Type Changed: Android.Views.InputMethods.ImeFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.InputMethods.ShowFlags'>Type Changed: Android.Views.InputMethods.ShowFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.InputMethods.ShowSoftInputFlags'>Type Changed: Android.Views.InputMethods.ShowSoftInputFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Views.InputMethods.TextExtractFlags'>Type Changed: Android.Views.InputMethods.TextExtractFlags</h3>

Added:

```
[Flags]
```

<h2 id='Android.Widget'>Namespace: Android.Widget</h2>

<h3 id='Android.Widget.CursorAdapterFlags'>Type Changed: Android.Widget.CursorAdapterFlags</h3>

Added:

```
[Flags]
```

<h3 id='Android.Widget.DatePicker'>Type Changed: Android.Widget.DatePicker</h3>

Added:

```
public DateTime DateTime {
 		get;
 		set;
 	}
 	public DateTime MaxDateTime {
 		get;
 	}
 	public DateTime MinDateTime {
 		get;
 	}
```

<h3 id='Android.Widget.QuickContactBadge'>Type Changed: Android.Widget.QuickContactBadge</h3>

Added:

```
set;
```

<h2 id='Java.IO'>Namespace: Java.IO</h2>

<h3 id='Java.IO.CharArrayReader'>Type Changed: Java.IO.CharArrayReader</h3>

Added:

```
set;
```

<h3 id='Java.IO.CharArrayWriter'>Type Changed: Java.IO.CharArrayWriter</h3>

Added:

```
set;
```

<h3 id='Java.IO.ObjectStreamClass'>Type Changed: Java.IO.ObjectStreamClass</h3>

Added:

```
set;
```

<h2 id='Java.Interop'>Namespace: Java.Interop</h2>

<h3 id='Java.Interop.AndroidEventHelper'>Type Changed: Java.Interop.AndroidEventHelper</h3>

Removed:

```
public static class AndroidEventHelper {
```

Added:

```
[Obsolete]
public static class AndroidEventHelper {
```

<h3 id='Java.Interop.EventHelper'>New Type: Java.Interop.EventHelper</h3>

```
public static class EventHelper {
	
	public static void AddEventHandler (ref WeakReference implementor, Func creator, Action setListener, Action add) where TImplementor : Java.Lang.Object;
	public static void RemoveEventHandler (ref WeakReference implementor, Func empty, Action unsetListener, Action remove) where TImplementor : Java.Lang.Object;
}
```

<h3 id='Java.Interop.JavaLibraryReferenceAttribute'>New Type: Java.Interop.JavaLibraryReferenceAttribute</h3>

```
public class JavaLibraryReferenceAttribute : Attribute {
	
	public JavaLibraryReferenceAttribute (string filename);
	
	public string InstallInstructions {
		get;
		set;
	}
	public string LibraryFileName {
		get;
	}
	public string PackageName {
		get;
		set;
	}
}
```

<h3 id='Java.Interop.JavaObjectExtensions'>Type Changed: Java.Interop.JavaObjectExtensions</h3>

Removed:

```
public static System.Collections.IDictionary ToInteroperableCollection (System.Collections.IDictionary instance);
```

Added:

```
public static Android.Runtime.JavaDictionary ToInteroperableCollection (System.Collections.IDictionary instance);
```

<h3 id='Java.Interop.Runtime'>New Type: Java.Interop.Runtime</h3>

```
public static class Runtime {
	
	public static System.Collections.Generic.List GetSurfacedObjects ();
	public static bool IsGCUserPeer (Android.Runtime.IJavaObject value);
	public static bool IsGCUserPeer (IntPtr value);
	
	public static int GlobalReferenceCount {
		get;
	}
	public static int LocalReferenceCount {
		get;
	}
	public static int MaxGlobalReferenceCount {
		get;
	}
}
```

<h2 id='Java.Lang'>Namespace: Java.Lang</h2>

<h3 id='Java.Lang.Void'>New Type: Java.Lang.Void</h3>

```
public sealed class Void : Object {
	
	public static Class Type {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Java.Net'>Namespace: Java.Net</h2>

<h3 id='Java.Net.IDNFlags'>Type Changed: Java.Net.IDNFlags</h3>

Added:

```
[Flags]
```

<h2 id='Java.Util'>Namespace: Java.Util</h2>

<h3 id='Java.Util.Calendar'>Type Changed: Java.Util.Calendar</h3>

Added:

```
set;
```

<h3 id='Java.Util.FormatFlags'>Type Changed: Java.Util.FormatFlags</h3>

Added:

```
[Flags]
```

<h2 id='Java.Util.Zip'>Namespace: Java.Util.Zip</h2>

<h3 id='Java.Util.Zip.DeflaterInputStream'>Type Changed: Java.Util.Zip.DeflaterInputStream</h3>

Added:

```
set;
```

<h3 id='Java.Util.Zip.DeflaterOutputStream'>Type Changed: Java.Util.Zip.DeflaterOutputStream</h3>

Added:

```
set;
```

<h3 id='Java.Util.Zip.InflaterInputStream'>Type Changed: Java.Util.Zip.InflaterInputStream</h3>

Added:

```
set;
```

<h3 id='Java.Util.Zip.InflaterOutputStream'>Type Changed: Java.Util.Zip.InflaterOutputStream</h3>

Added:

```
set;
```

<h2 id='Javax.Crypto'>Namespace: Javax.Crypto</h2>

<h3 id='Javax.Crypto.SealedObject'>Type Changed: Javax.Crypto.SealedObject</h3>

Added:

```
set;
```

<h2 id='Org.XmlPull.V1'>Namespace: Org.XmlPull.V1</h2>

<h3 id='Org.XmlPull.V1.XmlPullParser'>Type Changed: Org.XmlPull.V1.XmlPullParser</h3>

Added:

```
set;
```
