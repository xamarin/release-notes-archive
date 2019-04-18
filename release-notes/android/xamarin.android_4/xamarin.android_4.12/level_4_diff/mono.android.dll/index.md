---
id: EC1FA221-22E8-46D5-B082-FA7918B1B659
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.FeedbackFlags

Removed values:

```
AllMask = -1,
	Braille = 32,
```

## Namespace Android.App

### Type Changed: Android.App.NotificationFlags

Removed values:

```
ForegroundService = 64,
```

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ApplicationInfoFlags

Added values:

```
None = 0,
```

### Type Changed: Android.Content.PM.PackageManager

Removed methods:

```
public virtual void SetApplicationEnabledSetting (string packageName, ComponentEnabledState newState, PackageInfoFlags flags);
	public virtual void SetComponentEnabledSetting (Android.Content.ComponentName componentName, ComponentEnabledState newState, PackageInfoFlags flags);
```

Added methods:

```
public virtual void SetApplicationEnabledSetting (string packageName, ComponentEnabledState newState, ComponentEnableOption flags);
	public virtual void SetComponentEnabledSetting (Android.Content.ComponentName componentName, ComponentEnabledState newState, ComponentEnableOption flags);
```

### New Type Android.Content.PM.UiOptions

```
[Serializable]
public enum UiOptions {
	None = 0,
}
```

## Namespace Android.Graphics

### Type Changed: Android.Graphics.Format

Removed values:

```
Ycbcr422I = 20,
```

## Namespace Android.Locations

### Type Changed: Android.Locations.Criteria

Added fields:

```
public static const int NoRequirement;
```

## Namespace Android.Net

### Type Changed: Android.Net.WifiMode

Removed values:

```
FullHighPerf = 3,
```

## Namespace Android.OS

### Type Changed: Android.OS.AsyncTask

Added methods:

```
public System.Threading.Tasks.Task<Java.Lang.Object> GetAsync (long timeout, Java.Util.Concurrent.TimeUnit unit);
	public System.Threading.Tasks.Task<Java.Lang.Object> GetAsync ();
```

## Namespace Android.Test.Mock

### Type Changed: Android.Test.Mock.MockPackageManager

Removed methods:

```
public override void SetApplicationEnabledSetting (string packageName, Android.Content.PM.ComponentEnabledState newState, Android.Content.PM.PackageInfoFlags flags);
	public override void SetComponentEnabledSetting (Android.Content.ComponentName componentName, Android.Content.PM.ComponentEnabledState newState, Android.Content.PM.PackageInfoFlags flags);
```

Added methods:

```
public override void SetApplicationEnabledSetting (string packageName, Android.Content.PM.ComponentEnabledState newState, Android.Content.PM.ComponentEnableOption flags);
	public override void SetComponentEnabledSetting (Android.Content.ComponentName componentName, Android.Content.PM.ComponentEnabledState newState, Android.Content.PM.ComponentEnableOption flags);
```

## Namespace Android.Text.Format

### Type Changed: Android.Text.Format.DayOfWeek

Removed values:

```
MondayBeforeJulianEpoch = 2440585,
```

## Namespace Android.Views

### Type Changed: Android.Views.Keycode

Removed values:

```
ThreeDMode = 206,
```

### Type Changed: Android.Views.MenuPerformFlags

Added values:

```
AppendToGroup = 1,
```

### Type Changed: Android.Views.WindowFeatures

Removed values:

```
ActionBar = 8,
	ActionBarOverlay = 9,
	ActionModeOverlay = 10,
```

### Type Changed: Android.Views.WindowManagerLayoutParams

Removed fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.WindowManagerEventType enum directly instead of this field.")]
	public static const WindowManagerEventType TypeChanged;
```

### Type Changed: Android.Views.WindowManagerTypes

Removed values:

```
Wallpaper = 2013,
```

Added values:

```
Changed = 2,
```

### Removed Type Android.Views.EffectsSurface ### Removed Type Android.Views.KeyModifierBehavior ### Removed Type Android.Views.LayerType ### Removed Type Android.Views.ScrollbarPosition ### Removed Type Android.Views.StatusBarVisibility 



## Namespace Android.Views.InputMethods



### Type Changed: Android.Views.InputMethods.EditorInfo

Added fields:

```
public static const int ImeMaskAction;
	public static const int ImeNull;
```

### Type Changed: Android.Views.InputMethods.ImeAction

Removed values:

```
ImeMaskAction = 255,
	Previous = 7,
```

## Namespace Android.Webkit



### Type Changed: Android.Webkit.WebViewClient

Removed methods:

```
public virtual void OnReceivedError (WebView view, ClientError errorCode, string description, string failingUrl);
```

### Removed Type Android.Webkit.ClientError 

## Namespace Android.Widget



### Type Changed: Android.Widget.AbsListViewChoiceMode

Removed values:

```
MultipleModal = 3,
```

### Type Changed: Android.Widget.AdapterView

Added fields:

```
public static const int ItemViewTypeHeaderOrFooter;
	public static const int ItemViewTypeIgnore;
```

### Type Changed: Android.Widget.CursorAdapterFlags

Removed values:

```
AutoRequery = 1,
	RegisterContentObserver = 2,
```

### Type Changed: Android.Widget.ListView

Added fields:

```
public static const int ChoiceModeMultiple;
	public static const int ChoiceModeNone;
	public static const int ChoiceModeSingle;
```

### Removed Type Android.Widget.ListPopupWindowInputMethodMode ### Removed Type Android.Widget.NumberPickerScrollState ### Removed Type Android.Widget.ShowDividers ### Removed Type Android.Widget.SpinnerMode 



## Namespace Java.Interop



### Type Changed: Java.Interop.JavaObjectExtensions

Removed methods:

```
public static Android.Runtime.JavaCollection ToInteroperableCollection (System.Collections.ICollection instance);
	public static Android.Runtime.JavaCollection<T> ToInteroperableCollection<T> (System.Collections.Generic.ICollection<T> instance);
	public static Android.Runtime.JavaList ToInteroperableCollection (System.Collections.IList instance);
	public static Android.Runtime.JavaList<T> ToInteroperableCollection<T> (System.Collections.Generic.IList<T> instance);
	public static Android.Runtime.JavaDictionary ToInteroperableCollection (System.Collections.IDictionary instance);
	public static Android.Runtime.JavaDictionary<K,V> ToInteroperableCollection<K, V> (System.Collections.Generic.IDictionary<K,V> instance);
```

Added methods:

```
[Obsolete ("Use Android.Runtime.JavaCollection.ToLocalJniHandle()")]
	public static Android.Runtime.JavaCollection ToInteroperableCollection (System.Collections.ICollection instance);

	[Obsolete ("Use Android.Runtime.JavaCollection.ToLocalJniHandle()")]
	public static Android.Runtime.JavaCollection<T> ToInteroperableCollection<T> (System.Collections.Generic.ICollection<T> instance);

	[Obsolete ("Use Android.Runtime.JavaList.ToLocalJniHandle()")]
	public static Android.Runtime.JavaList ToInteroperableCollection (System.Collections.IList instance);

	[Obsolete ("Use Android.Runtime.JavaList.ToLocalJniHandle()")]
	public static Android.Runtime.JavaList<T> ToInteroperableCollection<T> (System.Collections.Generic.IList<T> instance);

	[Obsolete ("Use Android.Runtime.JavaDictionary.ToLocalJniHandle()")]
	public static Android.Runtime.JavaDictionary ToInteroperableCollection (System.Collections.IDictionary instance);

	[Obsolete ("Use Android.Runtime.JavaDictionary.ToLocalJniHandle()")]
	public static Android.Runtime.JavaDictionary<K,V> ToInteroperableCollection<K, V> (System.Collections.Generic.IDictionary<K,V> instance);
```

## Namespace Java.Util.Prefs



### Type Changed: Java.Util.Prefs.Preferences

Added methods:

```
public System.Threading.Tasks.Task ExportNodeAsync (System.IO.Stream ostream);
	public System.Threading.Tasks.Task ExportSubtreeAsync (System.IO.Stream ostream);
	public System.Threading.Tasks.Task FlushAsync ();
	public static System.Threading.Tasks.Task ImportPreferencesAsync (System.IO.Stream istream);
	public System.Threading.Tasks.Task SyncAsync ();
```

## Namespace Org.Apache.Http.Conn.Ssl

### Type Changed: Org.Apache.Http.Conn.Ssl.SSLSocketFactory

Added methods:

```
public System.Threading.Tasks.Task<Java.Net.Socket> ConnectSocketAsync (Java.Net.Socket sock, string host, int port, Java.Net.InetAddress localAddress, int localPort, Org.Apache.Http.Params.IHttpParams params);
	public System.Threading.Tasks.Task<Java.Net.Socket> CreateSocketAsync ();
	public System.Threading.Tasks.Task<Java.Net.Socket> CreateSocketAsync (Java.Net.Socket socket, string host, int port, bool autoClose);
```
