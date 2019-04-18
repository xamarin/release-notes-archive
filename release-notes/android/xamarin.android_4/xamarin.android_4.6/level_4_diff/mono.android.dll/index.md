---
id: A882E383-3273-4814-9E0A-EB3BD6B2E7B2
title: "Mono.Android.dll"
---

<a name="Mono.Android.dll" class="injected"></a>


# Mono.Android.dll

 <a name="Namespace:_Android.AccessibilityServices" class="injected"></a>


<h2 id='Android.AccessibilityServices'>Namespace: Android.AccessibilityServices</h2>

 <a name="Type_Changed:_Android.AccessibilityServices.AccessibilityService" class="injected"></a>


<h3 id='Android.AccessibilityServices.AccessibilityService'>Type Changed: Android.AccessibilityServices.AccessibilityService</h3>

Removed:

```
public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

Added:

```
public Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

 <a name="Namespace:_Android.App" class="injected"></a>


<h2 id='Android.App'>Namespace: Android.App</h2>

 <a name="Type_Changed:_Android.App.Activity" class="injected"></a>


<h3 id='Android.App.Activity'>Type Changed: Android.App.Activity</h3>

Removed:

```
public class Activity : Android.Views.ContextThemeWrapper, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IComponentCallbacks, LayoutInflater.Android.Views.IFactory, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Activity : Android.Views.ContextThemeWrapper, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IComponentCallbacks, LayoutInflater.Android.Views.IFactory, View.Android.Views.IOnCreateContextMenuListener {
```

 <a name="Type_Changed:_Android.App.AlertDialog" class="injected"></a>


<h3 id='Android.App.AlertDialog'>Type Changed: Android.App.AlertDialog</h3>

Removed:

```
protected AlertDialog (Android.Content.Context context);
 	protected AlertDialog (Android.Content.Context context, int theme);
```

Added:

```
protected AlertDialog (Android.Content.Context context, int theme);
 	protected AlertDialog (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.App.Dialog" class="injected"></a>


<h3 id='Android.App.Dialog'>Type Changed: Android.App.Dialog</h3>

Removed:

```
public Dialog (Android.Content.Context context);
 	public Dialog (Android.Content.Context context, int theme);
```

Added:

```
public Dialog (Android.Content.Context context, int theme);
 	public Dialog (Android.Content.Context context);
 	public T FindViewById<T> (int id) where T : Android.Views.View;
```

 <a name="Type_Changed:_Android.App.Notification" class="injected"></a>


<h3 id='Android.App.Notification'>Type Changed: Android.App.Notification</h3>

Removed:

```
public Notification ();
 	public Notification (Android.OS.Parcel parcel);
```

Added:

```
public Notification (Android.OS.Parcel parcel);
 	public Notification ();
```

 <a name="New_Type:_Android.App.SupportsGLTextureAttribute" class="injected"></a>


<h3 id='Android.App.SupportsGLTextureAttribute'>New Type: Android.App.SupportsGLTextureAttribute</h3>

```
[Serializable]
public sealed class SupportsGLTextureAttribute : Attribute {
	
	public SupportsGLTextureAttribute (string name);
	
	public string Name {
		get;
	}
}
```

 <a name="New_Type:_Android.App.UsesFeatureAttribute" class="injected"></a>


<h3 id='Android.App.UsesFeatureAttribute'>New Type: Android.App.UsesFeatureAttribute</h3>

```
[Serializable]
public sealed class UsesFeatureAttribute : Attribute {
	
	public UsesFeatureAttribute ();
	public UsesFeatureAttribute (string name);
	
	public int GLESVersion {
		get;
		set;
	}
	public string Name {
		get;
	}
}
```

 <a name="Namespace:_Android.Content" class="injected"></a>


<h2 id='Android.Content'>Namespace: Android.Content</h2>

 <a name="Type_Changed:_Android.Content.ComponentName" class="injected"></a>


<h3 id='Android.Content.ComponentName'>Type Changed: Android.Content.ComponentName</h3>

Removed:

```
public ComponentName (string pkg, string cls);
 	public ComponentName (Context pkg, string cls);
 	public ComponentName (Context pkg, Java.Lang.Class cls);
```

Added:

```
public ComponentName (Context pkg, Java.Lang.Class cls);
 	public ComponentName (Context pkg, string cls);
 	public ComponentName (string pkg, string cls);
```

 <a name="Type_Changed:_Android.Content.ContentValues" class="injected"></a>


<h3 id='Android.Content.ContentValues'>Type Changed: Android.Content.ContentValues</h3>

Removed:

```
public ContentValues ();
 	public ContentValues (int size);
```

Added:

```
public ContentValues (int size);
 	public ContentValues ();
```

 <a name="Type_Changed:_Android.Content.Intent" class="injected"></a>


<h3 id='Android.Content.Intent'>Type Changed: Android.Content.Intent</h3>

Removed:

```
public Intent (string action, Android.Net.Uri uri);
 	public Intent (Context packageContext, Java.Lang.Class cls);
 	public Intent (string action, Android.Net.Uri uri, Context packageContext, Java.Lang.Class cls);
```

Added:

```
public Intent (string action, Android.Net.Uri uri, Context packageContext, Java.Lang.Class cls);
 	public Intent (Context packageContext, Java.Lang.Class cls);
 	public Intent (string action, Android.Net.Uri uri);
```

 <a name="Type_Changed:_Android.Content.IntentFilter" class="injected"></a>


<h3 id='Android.Content.IntentFilter'>Type Changed: Android.Content.IntentFilter</h3>

Removed:

```
public IntentFilter ();
 	public IntentFilter (string action);
 	public IntentFilter (string action, string dataType);
```

Added:

```
public IntentFilter (string action, string dataType);
 	public IntentFilter (string action);
 	public IntentFilter ();
```

 <a name="Namespace:_Android.Content.PM" class="injected"></a>


<h2 id='Android.Content.PM'>Namespace: Android.Content.PM</h2>

 <a name="Type_Changed:_Android.Content.PM.ComponentInfo" class="injected"></a>


<h3 id='Android.Content.PM.ComponentInfo'>Type Changed: Android.Content.PM.ComponentInfo</h3>

Removed:

```
public ComponentInfo ();
 	public ComponentInfo (ComponentInfo orig);
```

Added:

```
public ComponentInfo (ComponentInfo orig);
 	public ComponentInfo ();
```

 <a name="Type_Changed:_Android.Content.PM.PackageItemInfo" class="injected"></a>


<h3 id='Android.Content.PM.PackageItemInfo'>Type Changed: Android.Content.PM.PackageItemInfo</h3>

Removed:

```
public PackageItemInfo ();
 	public PackageItemInfo (PackageItemInfo orig);
```

Added:

```
public PackageItemInfo (PackageItemInfo orig);
 	public PackageItemInfo ();
```

 <a name="Type_Changed:_Android.Content.PM.PackageStats" class="injected"></a>


<h3 id='Android.Content.PM.PackageStats'>Type Changed: Android.Content.PM.PackageStats</h3>

Removed:

```
public PackageStats (string pkgName);
 	public PackageStats (Android.OS.Parcel source);
```

Added:

```
public PackageStats (Android.OS.Parcel source);
 	public PackageStats (string pkgName);
```

 <a name="Namespace:_Android.Gestures" class="injected"></a>


<h2 id='Android.Gestures'>Namespace: Android.Gestures</h2>

 <a name="Type_Changed:_Android.Gestures.GestureOverlayView" class="injected"></a>


<h3 id='Android.Gestures.GestureOverlayView'>Type Changed: Android.Gestures.GestureOverlayView</h3>

Removed:

```
public GestureOverlayView (Android.Content.Context context);
 	public GestureOverlayView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public GestureOverlayView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public GestureOverlayView (Android.Content.Context context);
```

 <a name="Namespace:_Android.Graphics" class="injected"></a>


<h2 id='Android.Graphics'>Namespace: Android.Graphics</h2>

 <a name="Type_Changed:_Android.Graphics.Canvas" class="injected"></a>


<h3 id='Android.Graphics.Canvas'>Type Changed: Android.Graphics.Canvas</h3>

Removed:

```
public Canvas ();
 	public Canvas (Bitmap bitmap);
```

Added:

```
public Canvas (Bitmap bitmap);
 	public Canvas ();
```

 <a name="Type_Changed:_Android.Graphics.ColorMatrix" class="injected"></a>


<h3 id='Android.Graphics.ColorMatrix'>Type Changed: Android.Graphics.ColorMatrix</h3>

Removed:

```
public ColorMatrix ();
 	public ColorMatrix (float [] src);
```

Added:

```
public ColorMatrix (float [] src);
 	public ColorMatrix ();
```

 <a name="Type_Changed:_Android.Graphics.Paint" class="injected"></a>


<h3 id='Android.Graphics.Paint'>Type Changed: Android.Graphics.Paint</h3>

Removed:

```
public Paint ();
 	public Paint (PaintFlags flags);
```

Added:

```
public Paint (PaintFlags flags);
 	public Paint ();
```

 <a name="Type_Changed:_Android.Graphics.Point" class="injected"></a>


<h3 id='Android.Graphics.Point'>Type Changed: Android.Graphics.Point</h3>

Removed:

```
public Point ();
 	public Point (int x, int y);
```

Added:

```
public Point (int x, int y);
 	public Point ();
```

 <a name="Type_Changed:_Android.Graphics.PointF" class="injected"></a>


<h3 id='Android.Graphics.PointF'>Type Changed: Android.Graphics.PointF</h3>

Removed:

```
public PointF ();
 	public PointF (float x, float y);
```

Added:

```
public PointF (float x, float y);
 	public PointF ();
```

 <a name="Type_Changed:_Android.Graphics.Rect" class="injected"></a>


<h3 id='Android.Graphics.Rect'>Type Changed: Android.Graphics.Rect</h3>

Removed:

```
public Rect ();
 	public Rect (int left, int top, int right, int bottom);
```

Added:

```
public Rect (int left, int top, int right, int bottom);
 	public Rect ();
```

 <a name="Type_Changed:_Android.Graphics.RectF" class="injected"></a>


<h3 id='Android.Graphics.RectF'>Type Changed: Android.Graphics.RectF</h3>

Removed:

```
public RectF ();
 	public RectF (float left, float top, float right, float bottom);
 	public RectF (RectF r);
```

Added:

```
public RectF (RectF r);
 	public RectF (float left, float top, float right, float bottom);
 	public RectF ();
```

 <a name="Type_Changed:_Android.Graphics.Region" class="injected"></a>


<h3 id='Android.Graphics.Region'>Type Changed: Android.Graphics.Region</h3>

Removed:

```
public Region ();
 	public Region (Region region);
 	public Region (Rect r);
```

Added:

```
public Region (Rect r);
 	public Region (Region region);
 	public Region ();
```

 <a name="Namespace:_Android.Graphics.Drawables" class="injected"></a>


<h2 id='Android.Graphics.Drawables'>Namespace: Android.Graphics.Drawables</h2>

 <a name="Type_Changed:_Android.Graphics.Drawables.BitmapDrawable" class="injected"></a>


<h3 id='Android.Graphics.Drawables.BitmapDrawable'>Type Changed: Android.Graphics.Drawables.BitmapDrawable</h3>

Removed:

```
public BitmapDrawable (Android.Content.Res.Resources res, Android.Graphics.Bitmap bitmap);
 	public BitmapDrawable (string filepath);
 	public BitmapDrawable (System.IO.Stream is);
 	public override ConstantState GetConstantState ();
```

Added:

```
public BitmapDrawable (System.IO.Stream is);
 	public BitmapDrawable (string filepath);
 	public BitmapDrawable (Android.Content.Res.Resources res, Android.Graphics.Bitmap bitmap);
 	public ConstantState GetConstantState ();
```

 <a name="Type_Changed:_Android.Graphics.Drawables.NinePatchDrawable" class="injected"></a>


<h3 id='Android.Graphics.Drawables.NinePatchDrawable'>Type Changed: Android.Graphics.Drawables.NinePatchDrawable</h3>

Removed:

```
public NinePatchDrawable (Android.Graphics.Bitmap bitmap, byte [] chunk, Android.Graphics.Rect padding, string srcName);
 	public NinePatchDrawable (Android.Content.Res.Resources res, Android.Graphics.Bitmap bitmap, byte [] chunk, Android.Graphics.Rect padding, string srcName);
 	public NinePatchDrawable (Android.Graphics.NinePatch patch);
```

Added:

```
public NinePatchDrawable (Android.Graphics.NinePatch patch);
 	public NinePatchDrawable (Android.Content.Res.Resources res, Android.Graphics.Bitmap bitmap, byte [] chunk, Android.Graphics.Rect padding, string srcName);
 	public NinePatchDrawable (Android.Graphics.Bitmap bitmap, byte [] chunk, Android.Graphics.Rect padding, string srcName);
```

 <a name="Namespace:_Android.InputMethodServices" class="injected"></a>


<h2 id='Android.InputMethodServices'>Namespace: Android.InputMethodServices</h2>

 <a name="Type_Changed:_Android.InputMethodServices.AbstractInputMethodService" class="injected"></a>


<h3 id='Android.InputMethodServices.AbstractInputMethodService'>Type Changed: Android.InputMethodServices.AbstractInputMethodService</h3>

Removed:

```
public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

Added:

```
public Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

 <a name="Type_Changed:_Android.InputMethodServices.ExtractEditText" class="injected"></a>


<h3 id='Android.InputMethodServices.ExtractEditText'>Type Changed: Android.InputMethodServices.ExtractEditText</h3>

Removed:

```
public ExtractEditText (Android.Content.Context context);
 	public ExtractEditText (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ExtractEditText (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ExtractEditText (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.InputMethodServices.Keyboard" class="injected"></a>


<h3 id='Android.InputMethodServices.Keyboard'>Type Changed: Android.InputMethodServices.Keyboard</h3>

Removed:

```
public Keyboard (Android.Content.Context context, int xmlLayoutResId);
 	public Keyboard (Android.Content.Context context, int xmlLayoutResId, int modeId);
```

Added:

```
public Keyboard (Android.Content.Context context, int xmlLayoutResId, int modeId);
 	public Keyboard (Android.Content.Context context, int xmlLayoutResId);
```

 <a name="Namespace:_Android.OS" class="injected"></a>


<h2 id='Android.OS'>Namespace: Android.OS</h2>

 <a name="Type_Changed:_Android.OS.Bundle" class="injected"></a>


<h3 id='Android.OS.Bundle'>Type Changed: Android.OS.Bundle</h3>

Removed:

```
public Bundle ();
 	public Bundle (Java.Lang.ClassLoader loader);
 	public Bundle (int capacity);
```

Added:

```
public Bundle (int capacity);
 	public Bundle (Java.Lang.ClassLoader loader);
 	public Bundle ();
```

 <a name="Type_Changed:_Android.OS.Handler" class="injected"></a>


<h3 id='Android.OS.Handler'>Type Changed: Android.OS.Handler</h3>

Removed:

```
public Handler ();
 	public Handler (ICallback callback);
 	public Handler (Looper looper);
```

Added:

```
public Handler (Looper looper);
 	public Handler (ICallback callback);
 	public Handler ();
```

 <a name="Namespace:_Android.Preferences" class="injected"></a>


<h2 id='Android.Preferences'>Namespace: Android.Preferences</h2>

 <a name="Type_Changed:_Android.Preferences.CheckBoxPreference" class="injected"></a>


<h3 id='Android.Preferences.CheckBoxPreference'>Type Changed: Android.Preferences.CheckBoxPreference</h3>

Removed:

```
public CheckBoxPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public CheckBoxPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public CheckBoxPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public CheckBoxPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

 <a name="Type_Changed:_Android.Preferences.EditTextPreference" class="injected"></a>


<h3 id='Android.Preferences.EditTextPreference'>Type Changed: Android.Preferences.EditTextPreference</h3>

Removed:

```
public EditTextPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public EditTextPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public EditTextPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public EditTextPreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

 <a name="Type_Changed:_Android.Preferences.Preference" class="injected"></a>


<h3 id='Android.Preferences.Preference'>Type Changed: Android.Preferences.Preference</h3>

Removed:

```
public Preference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public Preference (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public Preference (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public Preference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

 <a name="Type_Changed:_Android.Preferences.PreferenceCategory" class="injected"></a>


<h3 id='Android.Preferences.PreferenceCategory'>Type Changed: Android.Preferences.PreferenceCategory</h3>

Removed:

```
public PreferenceCategory (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public PreferenceCategory (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public PreferenceCategory (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public PreferenceCategory (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

 <a name="Type_Changed:_Android.Preferences.RingtonePreference" class="injected"></a>


<h3 id='Android.Preferences.RingtonePreference'>Type Changed: Android.Preferences.RingtonePreference</h3>

Removed:

```
public RingtonePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public RingtonePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public RingtonePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public RingtonePreference (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

 <a name="Namespace:_Android.Telephony" class="injected"></a>


<h2 id='Android.Telephony'>Namespace: Android.Telephony</h2>

 <a name="Type_Changed:_Android.Telephony.NeighboringCellInfo" class="injected"></a>


<h3 id='Android.Telephony.NeighboringCellInfo'>Type Changed: Android.Telephony.NeighboringCellInfo</h3>

Removed:

```
public NeighboringCellInfo ();
 	public NeighboringCellInfo (int rssi, int cid);
```

Added:

```
public NeighboringCellInfo (int rssi, int cid);
 	public NeighboringCellInfo ();
```

 <a name="New_Type:_Android.Telephony.PhoneNumberFormattingTextWatcher" class="injected"></a>


<h3 id='Android.Telephony.PhoneNumberFormattingTextWatcher'>New Type: Android.Telephony.PhoneNumberFormattingTextWatcher</h3>

```
public class PhoneNumberFormattingTextWatcher : Java.Lang.Object, Android.Text.INoCopySpan, Android.Text.ITextWatcher {
	
	protected PhoneNumberFormattingTextWatcher (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PhoneNumberFormattingTextWatcher ();
	
	public virtual void AfterTextChanged (Android.Text.IEditable text);
	public virtual void BeforeTextChanged (Java.Lang.ICharSequence s, int start, int count, int after);
	public void BeforeTextChanged (string s, int start, int count, int after);
	public virtual void OnTextChanged (Java.Lang.ICharSequence s, int start, int before, int count);
	public void OnTextChanged (string s, int start, int before, int count);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

 <a name="Type_Changed:_Android.Telephony.ServiceState" class="injected"></a>


<h3 id='Android.Telephony.ServiceState'>Type Changed: Android.Telephony.ServiceState</h3>

Removed:

```
public ServiceState ();
 	public ServiceState (ServiceState s);
```

Added:

```
public ServiceState (ServiceState s);
 	public ServiceState ();
```

 <a name="Namespace:_Android.Test" class="injected"></a>


<h2 id='Android.Test'>Namespace: Android.Test</h2>

 <a name="Type_Changed:_Android.Test.FlakyTest" class="injected"></a>


<h3 id='Android.Test.FlakyTest'>Type Changed: Android.Test.FlakyTest</h3>

Added:

```
public abstract int Tolerance ();
```

 <a name="Namespace:_Android.Text" class="injected"></a>


<h2 id='Android.Text'>Namespace: Android.Text</h2>

 <a name="Type_Changed:_Android.Text.BoringLayout" class="injected"></a>


<h3 id='Android.Text.BoringLayout'>Type Changed: Android.Text.BoringLayout</h3>

Removed:

```
public override Directions GetLineDirections (int line);
```

Added:

```
public Directions GetLineDirections (int line);
```

 <a name="Type_Changed:_Android.Text.DynamicLayout" class="injected"></a>


<h3 id='Android.Text.DynamicLayout'>Type Changed: Android.Text.DynamicLayout</h3>

Removed:

```
public DynamicLayout (Java.Lang.ICharSequence base, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public DynamicLayout (string base, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public DynamicLayout (Java.Lang.ICharSequence base, Java.Lang.ICharSequence display, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public DynamicLayout (string base, string display, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public override Directions GetLineDirections (int line);
```

Added:

```
public DynamicLayout (Java.Lang.ICharSequence base, Java.Lang.ICharSequence display, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public DynamicLayout (string base, string display, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public DynamicLayout (Java.Lang.ICharSequence base, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public DynamicLayout (string base, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public Directions GetLineDirections (int line);
```

 <a name="Type_Changed:_Android.Text.SpannableStringBuilder" class="injected"></a>


<h3 id='Android.Text.SpannableStringBuilder'>Type Changed: Android.Text.SpannableStringBuilder</h3>

Removed:

```
public SpannableStringBuilder ();
 	public SpannableStringBuilder (Java.Lang.ICharSequence text);
 	public SpannableStringBuilder (string text);
```

Added:

```
public SpannableStringBuilder (Java.Lang.ICharSequence text);
 	public SpannableStringBuilder (string text);
 	public SpannableStringBuilder ();
```

 <a name="Type_Changed:_Android.Text.SpannableStringInternal" class="injected"></a>


<h3 id='Android.Text.SpannableStringInternal'>Type Changed: Android.Text.SpannableStringInternal</h3>

Removed:

```
public override string ToString ();
```

Added:

```
public string ToString ();
```

 <a name="Type_Changed:_Android.Text.StaticLayout" class="injected"></a>


<h3 id='Android.Text.StaticLayout'>Type Changed: Android.Text.StaticLayout</h3>

Removed:

```
public StaticLayout (Java.Lang.ICharSequence source, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public StaticLayout (string source, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public StaticLayout (Java.Lang.ICharSequence source, int bufstart, int bufend, TextPaint paint, int outerwidth, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public StaticLayout (string source, int bufstart, int bufend, TextPaint paint, int outerwidth, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public override Directions GetLineDirections (int line);
```

Added:

```
public StaticLayout (Java.Lang.ICharSequence source, int bufstart, int bufend, TextPaint paint, int outerwidth, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public StaticLayout (string source, int bufstart, int bufend, TextPaint paint, int outerwidth, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public StaticLayout (Java.Lang.ICharSequence source, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public StaticLayout (string source, TextPaint paint, int width, Alignment align, float spacingmult, float spacingadd, bool includepad);
 	public Directions GetLineDirections (int line);
```

 <a name="Type_Changed:_Android.Text.TextPaint" class="injected"></a>


<h3 id='Android.Text.TextPaint'>Type Changed: Android.Text.TextPaint</h3>

Removed:

```
public TextPaint ();
 	public TextPaint (Android.Graphics.PaintFlags flags);
```

Added:

```
public TextPaint (Android.Graphics.PaintFlags flags);
 	public TextPaint ();
```

 <a name="Namespace:_Android.Text.Format" class="injected"></a>


<h2 id='Android.Text.Format'>Namespace: Android.Text.Format</h2>

 <a name="Type_Changed:_Android.Text.Format.Time" class="injected"></a>


<h3 id='Android.Text.Format.Time'>Type Changed: Android.Text.Format.Time</h3>

Removed:

```
public Time (string timezone);
 	public Time ();
```

Added:

```
public Time ();
 	public Time (string timezone);
```

 <a name="Namespace:_Android.Text.Style" class="injected"></a>


<h2 id='Android.Text.Style'>Namespace: Android.Text.Style</h2>

 <a name="Type_Changed:_Android.Text.Style.BulletSpan" class="injected"></a>


<h3 id='Android.Text.Style.BulletSpan'>Type Changed: Android.Text.Style.BulletSpan</h3>

Removed:

```
public BulletSpan ();
 	public BulletSpan (int gapWidth);
 	public BulletSpan (int gapWidth, Android.Graphics.Color color);
```

Added:

```
public BulletSpan (int gapWidth, Android.Graphics.Color color);
 	public BulletSpan (int gapWidth);
 	public BulletSpan ();
```

 <a name="Type_Changed:_Android.Text.Style.ImageSpan" class="injected"></a>


<h3 id='Android.Text.Style.ImageSpan'>Type Changed: Android.Text.Style.ImageSpan</h3>

Removed:

```
public ImageSpan (Android.Graphics.Bitmap b);
 	public ImageSpan (Android.Graphics.Bitmap b, SpanAlign verticalAlignment);
 	public ImageSpan (Android.Content.Context context, Android.Graphics.Bitmap b);
 	public ImageSpan (Android.Content.Context context, Android.Graphics.Bitmap b, SpanAlign verticalAlignment);
 	public ImageSpan (Android.Graphics.Drawables.Drawable d);
 	public ImageSpan (Android.Graphics.Drawables.Drawable d, SpanAlign verticalAlignment);
```

Added:

```
public ImageSpan (Android.Graphics.Bitmap b);
 	public ImageSpan (Android.Graphics.Bitmap b, SpanAlign verticalAlignment);
 	public ImageSpan (Android.Content.Context context, Android.Graphics.Bitmap b);
 	public ImageSpan (Android.Graphics.Drawables.Drawable d, SpanAlign verticalAlignment);
 	public ImageSpan (Android.Graphics.Drawables.Drawable d);
 	public ImageSpan (Android.Content.Context context, Android.Graphics.Bitmap b, SpanAlign verticalAlignment);
```

 <a name="Type_Changed:_Android.Text.Style.LeadingMarginSpanStandard" class="injected"></a>


<h3 id='Android.Text.Style.LeadingMarginSpanStandard'>Type Changed: Android.Text.Style.LeadingMarginSpanStandard</h3>

Removed:

```
public LeadingMarginSpanStandard (int first, int rest);
 	public LeadingMarginSpanStandard (int every);
```

Added:

```
public LeadingMarginSpanStandard (int every);
 	public LeadingMarginSpanStandard (int first, int rest);
```

 <a name="Type_Changed:_Android.Text.Style.QuoteSpan" class="injected"></a>


<h3 id='Android.Text.Style.QuoteSpan'>Type Changed: Android.Text.Style.QuoteSpan</h3>

Removed:

```
public QuoteSpan ();
 	public QuoteSpan (Android.Graphics.Color color);
```

Added:

```
public QuoteSpan (Android.Graphics.Color color);
 	public QuoteSpan ();
```

 <a name="Type_Changed:_Android.Text.Style.TextAppearanceSpan" class="injected"></a>


<h3 id='Android.Text.Style.TextAppearanceSpan'>Type Changed: Android.Text.Style.TextAppearanceSpan</h3>

Removed:

```
public TextAppearanceSpan (Android.Content.Context context, int appearance);
 	public TextAppearanceSpan (Android.Content.Context context, int appearance, int colorList);
 	public TextAppearanceSpan (string family, Android.Graphics.TypefaceStyle style, int size, Android.Content.Res.ColorStateList color, Android.Content.Res.ColorStateList linkColor);
```

Added:

```
public TextAppearanceSpan (string family, Android.Graphics.TypefaceStyle style, int size, Android.Content.Res.ColorStateList color, Android.Content.Res.ColorStateList linkColor);
 	public TextAppearanceSpan (Android.Content.Context context, int appearance, int colorList);
 	public TextAppearanceSpan (Android.Content.Context context, int appearance);
```

 <a name="Namespace:_Android.Views" class="injected"></a>


<h2 id='Android.Views'>Namespace: Android.Views</h2>

 <a name="Type_Changed:_Android.Views.GestureDetector" class="injected"></a>


<h3 id='Android.Views.GestureDetector'>Type Changed: Android.Views.GestureDetector</h3>

Removed:

```
public GestureDetector (IOnGestureListener listener, Android.OS.Handler handler);
 	public GestureDetector (IOnGestureListener listener);
 	public GestureDetector (Android.Content.Context context, IOnGestureListener listener);
```

Added:

```
public GestureDetector (Android.Content.Context context, IOnGestureListener listener);
 	public GestureDetector (IOnGestureListener listener);
 	public GestureDetector (IOnGestureListener listener, Android.OS.Handler handler);
```

 <a name="Type_Changed:_Android.Views.InflateException" class="injected"></a>


<h3 id='Android.Views.InflateException'>Type Changed: Android.Views.InflateException</h3>

Removed:

```
public InflateException ();
 	public InflateException (string detailMessage, Java.Lang.Throwable throwable);
 	public InflateException (string detailMessage);
```

Added:

```
public InflateException (string detailMessage);
 	public InflateException (string detailMessage, Java.Lang.Throwable throwable);
 	public InflateException ();
```

 <a name="Type_Changed:_Android.Views.KeyEvent" class="injected"></a>


<h3 id='Android.Views.KeyEvent'>Type Changed: Android.Views.KeyEvent</h3>

Removed:

```
public KeyEvent (KeyEventActions action, Keycode code);
 	public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat);
 	public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat, MetaKeyStates metaState);
 	public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat, MetaKeyStates metaState, int device, int scancode);
```

Added:

```
public KeyEvent (KeyEventActions action, Keycode code);
 	public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat);
 	public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat, MetaKeyStates metaState);
 	public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat, MetaKeyStates metaState, int device, int scancode);
```

 <a name="Type_Changed:_Android.Views.SurfaceView" class="injected"></a>


<h3 id='Android.Views.SurfaceView'>Type Changed: Android.Views.SurfaceView</h3>

Removed:

```
public SurfaceView (Android.Content.Context context);
 	public SurfaceView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public SurfaceView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public SurfaceView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Views.View" class="injected"></a>


<h3 id='Android.Views.View'>Type Changed: Android.Views.View</h3>

Removed:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, Drawable.Android.Graphics.Drawables.ICallback, ICallback {
 	public View (Android.Content.Context context);
 	public View (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, ICallback, Drawable.Android.Graphics.Drawables.ICallback {
 	public View (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public View (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Views.ViewDebug" class="injected"></a>


<h3 id='Android.Views.ViewDebug'>Type Changed: Android.Views.ViewDebug</h3>

Added:

```
public abstract bool RetrieveReturn ();
 		public abstract bool DeepExport ();
 		public abstract FlagToString[] FlagMapping ();
 		public abstract IntToString[] IndexMapping ();
 		public abstract IntToString[] Mapping ();
 		public abstract string Prefix ();
 		public abstract bool ResolveId ();
 		public abstract int Equals ();
 		public abstract int Mask ();
 		public abstract string Name ();
 		public abstract bool OutputIf ();
 		public abstract int From ();
 		public abstract string To ();
```

 <a name="Type_Changed:_Android.Views.ViewGroup" class="injected"></a>


<h3 id='Android.Views.ViewGroup'>Type Changed: Android.Views.ViewGroup</h3>

Removed:

```
public ViewGroup (Android.Content.Context context);
 	public ViewGroup (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int width, int height);
 		public MarginLayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public MarginLayoutParams (int width, int height);
 		public MarginLayoutParams (MarginLayoutParams source);
```

Added:

```
public ViewGroup (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ViewGroup (Android.Content.Context context);
 		public LayoutParams (int width, int height);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public MarginLayoutParams (MarginLayoutParams source);
 		public MarginLayoutParams (int width, int height);
 		public MarginLayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Views.ViewStub" class="injected"></a>


<h3 id='Android.Views.ViewStub'>Type Changed: Android.Views.ViewStub</h3>

Removed:

```
public ViewStub (Android.Content.Context context);
 	public ViewStub (Android.Content.Context context, int layoutResource);
 	public ViewStub (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ViewStub (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ViewStub (Android.Content.Context context, int layoutResource);
 	public ViewStub (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Views.Window" class="injected"></a>


<h3 id='Android.Views.Window'>Type Changed: Android.Views.Window</h3>

Added:

```
public T FindViewById<T> (int id) where T : View;
```

 <a name="Type_Changed:_Android.Views.WindowManagerLayoutParams" class="injected"></a>


<h3 id='Android.Views.WindowManagerLayoutParams'>Type Changed: Android.Views.WindowManagerLayoutParams</h3>

Removed:

```
public WindowManagerLayoutParams ();
 	public WindowManagerLayoutParams (WindowManagerTypes _type);
 	public WindowManagerLayoutParams (WindowManagerTypes _type, WindowManagerFlags _flags);
```

Added:

```
public WindowManagerLayoutParams ();
 	public WindowManagerLayoutParams (WindowManagerTypes _type);
 	public WindowManagerLayoutParams (WindowManagerTypes _type, WindowManagerFlags _flags);
```

 <a name="Namespace:_Android.Views.Animations" class="injected"></a>


<h2 id='Android.Views.Animations'>Namespace: Android.Views.Animations</h2>

 <a name="Type_Changed:_Android.Views.Animations.AccelerateInterpolator" class="injected"></a>


<h3 id='Android.Views.Animations.AccelerateInterpolator'>Type Changed: Android.Views.Animations.AccelerateInterpolator</h3>

Removed:

```
public AccelerateInterpolator ();
 	public AccelerateInterpolator (float factor);
```

Added:

```
public AccelerateInterpolator (float factor);
 	public AccelerateInterpolator ();
```

 <a name="Type_Changed:_Android.Views.Animations.AnticipateInterpolator" class="injected"></a>


<h3 id='Android.Views.Animations.AnticipateInterpolator'>Type Changed: Android.Views.Animations.AnticipateInterpolator</h3>

Removed:

```
public AnticipateInterpolator ();
 	public AnticipateInterpolator (float tension);
```

Added:

```
public AnticipateInterpolator (float tension);
 	public AnticipateInterpolator ();
```

 <a name="Type_Changed:_Android.Views.Animations.AnticipateOvershootInterpolator" class="injected"></a>


<h3 id='Android.Views.Animations.AnticipateOvershootInterpolator'>Type Changed: Android.Views.Animations.AnticipateOvershootInterpolator</h3>

Removed:

```
public AnticipateOvershootInterpolator ();
 	public AnticipateOvershootInterpolator (float tension);
 	public AnticipateOvershootInterpolator (float tension, float extraTension);
```

Added:

```
public AnticipateOvershootInterpolator (float tension, float extraTension);
 	public AnticipateOvershootInterpolator (float tension);
 	public AnticipateOvershootInterpolator ();
```

 <a name="Type_Changed:_Android.Views.Animations.DecelerateInterpolator" class="injected"></a>


<h3 id='Android.Views.Animations.DecelerateInterpolator'>Type Changed: Android.Views.Animations.DecelerateInterpolator</h3>

Removed:

```
public DecelerateInterpolator ();
 	public DecelerateInterpolator (float factor);
```

Added:

```
public DecelerateInterpolator (float factor);
 	public DecelerateInterpolator ();
```

 <a name="Type_Changed:_Android.Views.Animations.GridLayoutAnimationController" class="injected"></a>


<h3 id='Android.Views.Animations.GridLayoutAnimationController'>Type Changed: Android.Views.Animations.GridLayoutAnimationController</h3>

Removed:

```
public GridLayoutAnimationController (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public GridLayoutAnimationController (Animation animation);
```

Added:

```
public GridLayoutAnimationController (Animation animation);
 	public GridLayoutAnimationController (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Views.Animations.LayoutAnimationController" class="injected"></a>


<h3 id='Android.Views.Animations.LayoutAnimationController'>Type Changed: Android.Views.Animations.LayoutAnimationController</h3>

Removed:

```
public LayoutAnimationController (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public LayoutAnimationController (Animation animation);
```

Added:

```
public LayoutAnimationController (Animation animation);
 	public LayoutAnimationController (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Views.Animations.OvershootInterpolator" class="injected"></a>


<h3 id='Android.Views.Animations.OvershootInterpolator'>Type Changed: Android.Views.Animations.OvershootInterpolator</h3>

Removed:

```
public OvershootInterpolator ();
 	public OvershootInterpolator (float tension);
```

Added:

```
public OvershootInterpolator (float tension);
 	public OvershootInterpolator ();
```

 <a name="Type_Changed:_Android.Views.Animations.RotateAnimation" class="injected"></a>


<h3 id='Android.Views.Animations.RotateAnimation'>Type Changed: Android.Views.Animations.RotateAnimation</h3>

Removed:

```
public RotateAnimation (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public RotateAnimation (float fromDegrees, float toDegrees);
 	public RotateAnimation (float fromDegrees, float toDegrees, float pivotX, float pivotY);
```

Added:

```
public RotateAnimation (float fromDegrees, float toDegrees, float pivotX, float pivotY);
 	public RotateAnimation (float fromDegrees, float toDegrees);
 	public RotateAnimation (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Views.Animations.ScaleAnimation" class="injected"></a>


<h3 id='Android.Views.Animations.ScaleAnimation'>Type Changed: Android.Views.Animations.ScaleAnimation</h3>

Removed:

```
public ScaleAnimation (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ScaleAnimation (float fromX, float toX, float fromY, float toY);
 	public ScaleAnimation (float fromX, float toX, float fromY, float toY, float pivotX, float pivotY);
```

Added:

```
public ScaleAnimation (float fromX, float toX, float fromY, float toY, float pivotX, float pivotY);
 	public ScaleAnimation (float fromX, float toX, float fromY, float toY);
 	public ScaleAnimation (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Views.Animations.TranslateAnimation" class="injected"></a>


<h3 id='Android.Views.Animations.TranslateAnimation'>Type Changed: Android.Views.Animations.TranslateAnimation</h3>

Removed:

```
public TranslateAnimation (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public TranslateAnimation (float fromXDelta, float toXDelta, float fromYDelta, float toYDelta);
```

Added:

```
public TranslateAnimation (float fromXDelta, float toXDelta, float fromYDelta, float toYDelta);
 	public TranslateAnimation (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

 <a name="Namespace:_Android.Views.InputMethods" class="injected"></a>


<h2 id='Android.Views.InputMethods'>Namespace: Android.Views.InputMethods</h2>

 <a name="Type_Changed:_Android.Views.InputMethods.InputMethodManager" class="injected"></a>


<h3 id='Android.Views.InputMethods.InputMethodManager'>Type Changed: Android.Views.InputMethods.InputMethodManager</h3>

Removed:

```
public void ToggleSoftInput (ShowSoftInputFlags showFlags, HideSoftInputFlags hideFlags);
```

Added:

```
public void ToggleSoftInput (ShowFlags showFlags, HideSoftInputFlags hideFlags);
```

 <a name="Namespace:_Android.Webkit" class="injected"></a>


<h2 id='Android.Webkit'>Namespace: Android.Webkit</h2>

 <a name="Type_Changed:_Android.Webkit.WebView" class="injected"></a>


<h3 id='Android.Webkit.WebView'>Type Changed: Android.Webkit.WebView</h3>

Removed:

```
public WebView (Android.Content.Context context);
 	public WebView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public WebView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public WebView (Android.Content.Context context);
```

 <a name="Namespace:_Android.Widget" class="injected"></a>


<h2 id='Android.Widget'>Namespace: Android.Widget</h2>

 <a name="Type_Changed:_Android.Widget.AbsListView" class="injected"></a>


<h3 id='Android.Widget.AbsListView'>Type Changed: Android.Widget.AbsListView</h3>

Removed:

```
public AbsListView (Android.Content.Context context);
 	public AbsListView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int w, int h);
 		public LayoutParams (int w, int h, int viewType);
```

Added:

```
public AbsListView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public AbsListView (Android.Content.Context context);
 		public LayoutParams (int w, int h, int viewType);
 		public LayoutParams (int w, int h);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Widget.AbsSeekBar" class="injected"></a>


<h3 id='Android.Widget.AbsSeekBar'>Type Changed: Android.Widget.AbsSeekBar</h3>

Removed:

```
public AbsSeekBar (Android.Content.Context context);
 	public AbsSeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public AbsSeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public AbsSeekBar (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.AbsSpinner" class="injected"></a>


<h3 id='Android.Widget.AbsSpinner'>Type Changed: Android.Widget.AbsSpinner</h3>

Removed:

```
public AbsSpinner (Android.Content.Context context);
 	public AbsSpinner (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public AbsSpinner (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public AbsSpinner (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.AbsoluteLayout" class="injected"></a>


<h3 id='Android.Widget.AbsoluteLayout'>Type Changed: Android.Widget.AbsoluteLayout</h3>

Removed:

```
public AbsoluteLayout (Android.Content.Context context);
 	public AbsoluteLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int width, int height, int x, int y);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
```

Added:

```
public AbsoluteLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public AbsoluteLayout (Android.Content.Context context);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int width, int height, int x, int y);
```

 <a name="Type_Changed:_Android.Widget.AdapterView" class="injected"></a>


<h3 id='Android.Widget.AdapterView'>Type Changed: Android.Widget.AdapterView</h3>

Removed:

```
public AdapterView (Android.Content.Context context);
 	public AdapterView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public AdapterView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public AdapterView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.AnalogClock" class="injected"></a>


<h3 id='Android.Widget.AnalogClock'>Type Changed: Android.Widget.AnalogClock</h3>

Removed:

```
public AnalogClock (Android.Content.Context context);
 	public AnalogClock (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public AnalogClock (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public AnalogClock (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.ArrayAdapter" class="injected"></a>


<h3 id='Android.Widget.ArrayAdapter'>Type Changed: Android.Widget.ArrayAdapter</h3>

Removed:

```
public ArrayAdapter (Android.Content.Context context, int resource, int textViewResourceId, Java.Lang.Object[] objects);
 	public ArrayAdapter (Android.Content.Context context, int textViewResourceId, System.Collections.IList objects);
 	public ArrayAdapter (Android.Content.Context context, int resource, int textViewResourceId, System.Collections.IList objects);
```

Added:

```
public ArrayAdapter (Android.Content.Context context, int resource, int textViewResourceId, System.Collections.IList objects);
 	public ArrayAdapter (Android.Content.Context context, int textViewResourceId, System.Collections.IList objects);
 	public ArrayAdapter (Android.Content.Context context, int resource, int textViewResourceId, Java.Lang.Object[] objects);
```

 <a name="Type_Changed:_Android.Widget.AutoCompleteTextView" class="injected"></a>


<h3 id='Android.Widget.AutoCompleteTextView'>Type Changed: Android.Widget.AutoCompleteTextView</h3>

Removed:

```
public AutoCompleteTextView (Android.Content.Context context);
 	public AutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public AutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public AutoCompleteTextView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.CheckedTextView" class="injected"></a>


<h3 id='Android.Widget.CheckedTextView'>Type Changed: Android.Widget.CheckedTextView</h3>

Removed:

```
public CheckedTextView (Android.Content.Context context);
 	public CheckedTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public CheckedTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public CheckedTextView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.Chronometer" class="injected"></a>


<h3 id='Android.Widget.Chronometer'>Type Changed: Android.Widget.Chronometer</h3>

Removed:

```
public Chronometer (Android.Content.Context context);
 	public Chronometer (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public Chronometer (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public Chronometer (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.CompoundButton" class="injected"></a>


<h3 id='Android.Widget.CompoundButton'>Type Changed: Android.Widget.CompoundButton</h3>

Removed:

```
public CompoundButton (Android.Content.Context context);
 	public CompoundButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public CompoundButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public CompoundButton (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.DatePicker" class="injected"></a>


<h3 id='Android.Widget.DatePicker'>Type Changed: Android.Widget.DatePicker</h3>

Removed:

```
public DatePicker (Android.Content.Context context);
 	public DatePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public DatePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public DatePicker (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.EditText" class="injected"></a>


<h3 id='Android.Widget.EditText'>Type Changed: Android.Widget.EditText</h3>

Removed:

```
public EditText (Android.Content.Context context);
 	public EditText (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public EditText (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public EditText (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.ExpandableListView" class="injected"></a>


<h3 id='Android.Widget.ExpandableListView'>Type Changed: Android.Widget.ExpandableListView</h3>

Removed:

```
public ExpandableListView (Android.Content.Context context);
 	public ExpandableListView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ExpandableListView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ExpandableListView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.FrameLayout" class="injected"></a>


<h3 id='Android.Widget.FrameLayout'>Type Changed: Android.Widget.FrameLayout</h3>

Removed:

```
public FrameLayout (Android.Content.Context context);
 	public FrameLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int width, int height);
 		public LayoutParams (int width, int height, Android.Views.GravityFlags gravity);
 		public LayoutParams (ViewGroup.Android.Views.LayoutParams source);
```

Added:

```
public FrameLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public FrameLayout (Android.Content.Context context);
 		public LayoutParams (ViewGroup.Android.Views.LayoutParams source);
 		public LayoutParams (int width, int height, Android.Views.GravityFlags gravity);
 		public LayoutParams (int width, int height);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Widget.Gallery" class="injected"></a>


<h3 id='Android.Widget.Gallery'>Type Changed: Android.Widget.Gallery</h3>

Removed:

```
public Gallery (Android.Content.Context context);
 	public Gallery (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public Gallery (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public Gallery (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.GridView" class="injected"></a>


<h3 id='Android.Widget.GridView'>Type Changed: Android.Widget.GridView</h3>

Removed:

```
public GridView (Android.Content.Context context);
 	public GridView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public GridView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public GridView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.HorizontalScrollView" class="injected"></a>


<h3 id='Android.Widget.HorizontalScrollView'>Type Changed: Android.Widget.HorizontalScrollView</h3>

Removed:

```
public HorizontalScrollView (Android.Content.Context context);
 	public HorizontalScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public HorizontalScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public HorizontalScrollView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.ImageButton" class="injected"></a>


<h3 id='Android.Widget.ImageButton'>Type Changed: Android.Widget.ImageButton</h3>

Removed:

```
public ImageButton (Android.Content.Context context);
 	public ImageButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ImageButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ImageButton (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.ImageView" class="injected"></a>


<h3 id='Android.Widget.ImageView'>Type Changed: Android.Widget.ImageView</h3>

Removed:

```
public ImageView (Android.Content.Context context);
 	public ImageView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ImageView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ImageView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.LinearLayout" class="injected"></a>


<h3 id='Android.Widget.LinearLayout'>Type Changed: Android.Widget.LinearLayout</h3>

Removed:

```
public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int width, int height);
 		public LayoutParams (int width, int height, float weight);
 		public LayoutParams (ViewGroup.Android.Views.LayoutParams p);
```

Added:

```
public LayoutParams (ViewGroup.Android.Views.LayoutParams p);
 		public LayoutParams (int width, int height, float weight);
 		public LayoutParams (int width, int height);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Widget.ListView" class="injected"></a>


<h3 id='Android.Widget.ListView'>Type Changed: Android.Widget.ListView</h3>

Removed:

```
public ListView (Android.Content.Context context);
 	public ListView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ListView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ListView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.MediaController" class="injected"></a>


<h3 id='Android.Widget.MediaController'>Type Changed: Android.Widget.MediaController</h3>

Removed:

```
public MediaController (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public MediaController (Android.Content.Context context, bool useFastForward);
```

Added:

```
public MediaController (Android.Content.Context context, bool useFastForward);
 	public MediaController (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Widget.MultiAutoCompleteTextView" class="injected"></a>


<h3 id='Android.Widget.MultiAutoCompleteTextView'>Type Changed: Android.Widget.MultiAutoCompleteTextView</h3>

Removed:

```
public MultiAutoCompleteTextView (Android.Content.Context context);
 	public MultiAutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public MultiAutoCompleteTextView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public MultiAutoCompleteTextView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.PopupWindow" class="injected"></a>


<h3 id='Android.Widget.PopupWindow'>Type Changed: Android.Widget.PopupWindow</h3>

Removed:

```
public PopupWindow (Android.Content.Context context);
 	public PopupWindow (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public PopupWindow (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public PopupWindow ();
```

Added:

```
public PopupWindow (Android.Content.Context context);
 	public PopupWindow (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public PopupWindow (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public PopupWindow ();
```

 <a name="Type_Changed:_Android.Widget.ProgressBar" class="injected"></a>


<h3 id='Android.Widget.ProgressBar'>Type Changed: Android.Widget.ProgressBar</h3>

Removed:

```
public ProgressBar (Android.Content.Context context);
 	public ProgressBar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ProgressBar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ProgressBar (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.RadioButton" class="injected"></a>


<h3 id='Android.Widget.RadioButton'>Type Changed: Android.Widget.RadioButton</h3>

Removed:

```
public RadioButton (Android.Content.Context context);
 	public RadioButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public RadioButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public RadioButton (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.RadioGroup" class="injected"></a>


<h3 id='Android.Widget.RadioGroup'>Type Changed: Android.Widget.RadioGroup</h3>

Removed:

```
public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int w, int h);
 		public LayoutParams (int w, int h, float initWeight);
 		public LayoutParams (ViewGroup.Android.Views.LayoutParams p);
```

Added:

```
public LayoutParams (ViewGroup.Android.Views.LayoutParams p);
 		public LayoutParams (int w, int h, float initWeight);
 		public LayoutParams (int w, int h);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Widget.RatingBar" class="injected"></a>


<h3 id='Android.Widget.RatingBar'>Type Changed: Android.Widget.RatingBar</h3>

Removed:

```
public RatingBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public RatingBar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public RatingBar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public RatingBar (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

 <a name="Type_Changed:_Android.Widget.RelativeLayout" class="injected"></a>


<h3 id='Android.Widget.RelativeLayout'>Type Changed: Android.Widget.RelativeLayout</h3>

Removed:

```
public RelativeLayout (Android.Content.Context context);
 	public RelativeLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int w, int h);
 		public LayoutParams (ViewGroup.Android.Views.LayoutParams source);
```

Added:

```
public RelativeLayout (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public RelativeLayout (Android.Content.Context context);
 		public LayoutParams (ViewGroup.Android.Views.LayoutParams source);
 		public LayoutParams (int w, int h);
 		public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
```

 <a name="Type_Changed:_Android.Widget.ResourceCursorTreeAdapter" class="injected"></a>


<h3 id='Android.Widget.ResourceCursorTreeAdapter'>Type Changed: Android.Widget.ResourceCursorTreeAdapter</h3>

Removed:

```
public ResourceCursorTreeAdapter (Android.Content.Context context, Android.Database.ICursor cursor, int collapsedGroupLayout, int expandedGroupLayout, int childLayout, int lastChildLayout);
 	public ResourceCursorTreeAdapter (Android.Content.Context context, Android.Database.ICursor cursor, int collapsedGroupLayout, int expandedGroupLayout, int childLayout);
```

Added:

```
public ResourceCursorTreeAdapter (Android.Content.Context context, Android.Database.ICursor cursor, int collapsedGroupLayout, int expandedGroupLayout, int childLayout);
 	public ResourceCursorTreeAdapter (Android.Content.Context context, Android.Database.ICursor cursor, int collapsedGroupLayout, int expandedGroupLayout, int childLayout, int lastChildLayout);
```

 <a name="Type_Changed:_Android.Widget.ScrollView" class="injected"></a>


<h3 id='Android.Widget.ScrollView'>Type Changed: Android.Widget.ScrollView</h3>

Removed:

```
public ScrollView (Android.Content.Context context);
 	public ScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ScrollView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ScrollView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.SeekBar" class="injected"></a>


<h3 id='Android.Widget.SeekBar'>Type Changed: Android.Widget.SeekBar</h3>

Removed:

```
public SeekBar (Android.Content.Context context);
 	public SeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public SeekBar (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public SeekBar (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.SimpleCursorTreeAdapter" class="injected"></a>


<h3 id='Android.Widget.SimpleCursorTreeAdapter'>Type Changed: Android.Widget.SimpleCursorTreeAdapter</h3>

Removed:

```
public SimpleCursorTreeAdapter (Android.Content.Context context, Android.Database.ICursor cursor, int collapsedGroupLayout, int expandedGroupLayout, string [] groupFrom, int [] groupTo, int childLayout, int lastChildLayout, string [] childFrom, int [] childTo);
 	public SimpleCursorTreeAdapter (Android.Content.Context context, Android.Database.ICursor cursor, int collapsedGroupLayout, int expandedGroupLayout, string [] groupFrom, int [] groupTo, int childLayout, string [] childFrom, int [] childTo);
```

Added:

```
public SimpleCursorTreeAdapter (Android.Content.Context context, Android.Database.ICursor cursor, int collapsedGroupLayout, int expandedGroupLayout, string [] groupFrom, int [] groupTo, int childLayout, string [] childFrom, int [] childTo);
 	public SimpleCursorTreeAdapter (Android.Content.Context context, Android.Database.ICursor cursor, int collapsedGroupLayout, int expandedGroupLayout, string [] groupFrom, int [] groupTo, int childLayout, int lastChildLayout, string [] childFrom, int [] childTo);
```

 <a name="Type_Changed:_Android.Widget.SimpleExpandableListAdapter" class="injected"></a>


<h3 id='Android.Widget.SimpleExpandableListAdapter'>Type Changed: Android.Widget.SimpleExpandableListAdapter</h3>

Removed:

```
public SimpleExpandableListAdapter (Android.Content.Context context, System.Collections.Generic.IList<System.Collections.Generic.IDictionary<string,object>> groupData, int groupLayout, string [] groupFrom, int [] groupTo, System.Collections.Generic.IList<System.Collections.Generic.IList<System.Collections.Generic.IDictionary<string,object>>> childData, int childLayout, string [] childFrom, int [] childTo);
 	public SimpleExpandableListAdapter (Android.Content.Context context, System.Collections.Generic.IList<System.Collections.Generic.IDictionary<string,object>> groupData, int expandedGroupLayout, int collapsedGroupLayout, string [] groupFrom, int [] groupTo, System.Collections.Generic.IList<System.Collections.Generic.IList<System.Collections.Generic.IDictionary<string,object>>> childData, int childLayout, string [] childFrom, int [] childTo);
```

Added:

```
public SimpleExpandableListAdapter (Android.Content.Context context, System.Collections.Generic.IList<System.Collections.Generic.IDictionary<string,object>> groupData, int expandedGroupLayout, int collapsedGroupLayout, string [] groupFrom, int [] groupTo, System.Collections.Generic.IList<System.Collections.Generic.IList<System.Collections.Generic.IDictionary<string,object>>> childData, int childLayout, string [] childFrom, int [] childTo);
 	public SimpleExpandableListAdapter (Android.Content.Context context, System.Collections.Generic.IList<System.Collections.Generic.IDictionary<string,object>> groupData, int groupLayout, string [] groupFrom, int [] groupTo, System.Collections.Generic.IList<System.Collections.Generic.IList<System.Collections.Generic.IDictionary<string,object>>> childData, int childLayout, string [] childFrom, int [] childTo);
```

 <a name="Type_Changed:_Android.Widget.Spinner" class="injected"></a>


<h3 id='Android.Widget.Spinner'>Type Changed: Android.Widget.Spinner</h3>

Removed:

```
public Spinner (Android.Content.Context context);
 	public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public Spinner (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public Spinner (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.TabWidget" class="injected"></a>


<h3 id='Android.Widget.TabWidget'>Type Changed: Android.Widget.TabWidget</h3>

Removed:

```
public TabWidget (Android.Content.Context context);
 	public TabWidget (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public TabWidget (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public TabWidget (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.TableLayout" class="injected"></a>


<h3 id='Android.Widget.TableLayout'>Type Changed: Android.Widget.TableLayout</h3>

Removed:

```
public LayoutParams ();
 		public LayoutParams (ViewGroup.Android.Views.LayoutParams p);
 		public LayoutParams (ViewGroup.Android.Views.MarginLayoutParams source);
```

Added:

```
public LayoutParams (ViewGroup.Android.Views.MarginLayoutParams source);
 		public LayoutParams (ViewGroup.Android.Views.LayoutParams p);
 		public LayoutParams ();
```

 <a name="Type_Changed:_Android.Widget.TableRow" class="injected"></a>


<h3 id='Android.Widget.TableRow'>Type Changed: Android.Widget.TableRow</h3>

Removed:

```
public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int w, int h);
 		public LayoutParams (int w, int h, float initWeight);
```

Added:

```
public LayoutParams (Android.Content.Context c, Android.Util.IAttributeSet attrs);
 		public LayoutParams (int w, int h);
 		public LayoutParams (int w, int h, float initWeight);
```

 <a name="Type_Changed:_Android.Widget.TextView" class="injected"></a>


<h3 id='Android.Widget.TextView'>Type Changed: Android.Widget.TextView</h3>

Removed:

```
public TextView (Android.Content.Context context);
 	public TextView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public TextView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public TextView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.TimePicker" class="injected"></a>


<h3 id='Android.Widget.TimePicker'>Type Changed: Android.Widget.TimePicker</h3>

Removed:

```
public TimePicker (Android.Content.Context context);
 	public TimePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public TimePicker (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public TimePicker (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.ToggleButton" class="injected"></a>


<h3 id='Android.Widget.ToggleButton'>Type Changed: Android.Widget.ToggleButton</h3>

Removed:

```
public ToggleButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
 	public ToggleButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ToggleButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ToggleButton (Android.Content.Context context, Android.Util.IAttributeSet attrs, int defStyle);
```

 <a name="Type_Changed:_Android.Widget.TwoLineListItem" class="injected"></a>


<h3 id='Android.Widget.TwoLineListItem'>Type Changed: Android.Widget.TwoLineListItem</h3>

Removed:

```
public TwoLineListItem (Android.Content.Context context);
 	public TwoLineListItem (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public TwoLineListItem (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public TwoLineListItem (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.VideoView" class="injected"></a>


<h3 id='Android.Widget.VideoView'>Type Changed: Android.Widget.VideoView</h3>

Removed:

```
public VideoView (Android.Content.Context context);
 	public VideoView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public VideoView (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public VideoView (Android.Content.Context context);
```

 <a name="Type_Changed:_Android.Widget.ZoomButton" class="injected"></a>


<h3 id='Android.Widget.ZoomButton'>Type Changed: Android.Widget.ZoomButton</h3>

Removed:

```
public ZoomButton (Android.Content.Context context);
 	public ZoomButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public ZoomButton (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public ZoomButton (Android.Content.Context context);
```

 <a name="Namespace:_Dalvik.Annotation" class="injected"></a>


<h2 id='Dalvik.Annotation'>Namespace: Dalvik.Annotation</h2>

 <a name="Type_Changed:_Dalvik.Annotation.TestTarget" class="injected"></a>


<h3 id='Dalvik.Annotation.TestTarget'>Type Changed: Dalvik.Annotation.TestTarget</h3>

Added:

```
public abstract string ConceptName ();
 	public abstract Java.Lang.Class[] MethodArgs ();
 	public abstract string MethodName ();
```

 <a name="Type_Changed:_Dalvik.Annotation.TestTargetClass" class="injected"></a>


<h3 id='Dalvik.Annotation.TestTargetClass'>Type Changed: Dalvik.Annotation.TestTargetClass</h3>

Added:

```
public abstract Java.Lang.Class Value ();
```

 <a name="Namespace:_Java.IO" class="injected"></a>


<h2 id='Java.IO'>Namespace: Java.IO</h2>

 <a name="Type_Changed:_Java.IO.File" class="injected"></a>


<h3 id='Java.IO.File'>Type Changed: Java.IO.File</h3>

Removed:

```
public File (string path);
 	public File (string dirPath, string name);
```

Added:

```
public File (string dirPath, string name);
 	public File (string path);
```

 <a name="Type_Changed:_Java.IO.FileInputStream" class="injected"></a>


<h3 id='Java.IO.FileInputStream'>Type Changed: Java.IO.FileInputStream</h3>

Removed:

```
public FileInputStream (string fileName);
```

Added:

```
public FileInputStream (string fileName);
```

 <a name="Type_Changed:_Java.IO.FileOutputStream" class="injected"></a>


<h3 id='Java.IO.FileOutputStream'>Type Changed: Java.IO.FileOutputStream</h3>

Removed:

```
public FileOutputStream (string filename);
 	public FileOutputStream (string filename, bool append);
 	public FileOutputStream (File file);
```

Added:

```
public FileOutputStream (string filename, bool append);
 	public FileOutputStream (string filename);
 	public FileOutputStream (File file);
```

 <a name="Type_Changed:_Java.IO.FileWriter" class="injected"></a>


<h3 id='Java.IO.FileWriter'>Type Changed: Java.IO.FileWriter</h3>

Removed:

```
public FileWriter (string filename);
 	public FileWriter (string filename, bool append);
 	public FileWriter (File file);
 	public FileWriter (File file, bool append);
```

Added:

```
public FileWriter (File file, bool append);
 	public FileWriter (File file);
 	public FileWriter (string filename, bool append);
 	public FileWriter (string filename);
```

 <a name="Type_Removed:_Java.IO.ICloseable" class="injected"></a>


<h3 id='Java.IO.ICloseable'>Type Removed: Java.IO.ICloseable</h3>

 <a name="Type_Removed:_Java.IO.IExternalizable" class="injected"></a>


<h3 id='Java.IO.IExternalizable'>Type Removed: Java.IO.IExternalizable</h3>

 <a name="Type_Changed:_Java.IO.IOException" class="injected"></a>


<h3 id='Java.IO.IOException'>Type Changed: Java.IO.IOException</h3>

Removed:

```
public IOException ();
 	public IOException (string detailMessage);
 	public IOException (string p0, Java.Lang.Throwable p1);
```

Added:

```
public IOException (string p0, Java.Lang.Throwable p1);
 	public IOException (string detailMessage);
 	public IOException ();
```

 <a name="Type_Removed:_Java.IO.IObjectInput" class="injected"></a>


<h3 id='Java.IO.IObjectInput'>Type Removed: Java.IO.IObjectInput</h3>

 <a name="Type_Removed:_Java.IO.IObjectOutput" class="injected"></a>


<h3 id='Java.IO.IObjectOutput'>Type Removed: Java.IO.IObjectOutput</h3>

 <a name="Type_Changed:_Java.IO.InputStream" class="injected"></a>


<h3 id='Java.IO.InputStream'>Type Changed: Java.IO.InputStream</h3>

Removed:

```
public abstract class InputStream : Java.Lang.Object, ICloseable {
```

Added:

```
public abstract class InputStream : Java.Lang.Object {
```

 <a name="Type_Changed:_Java.IO.InputStreamReader" class="injected"></a>


<h3 id='Java.IO.InputStreamReader'>Type Changed: Java.IO.InputStreamReader</h3>

Removed:

```
public InputStreamReader (System.IO.Stream in);
 	public InputStreamReader (System.IO.Stream in, string enc);
 	public InputStreamReader (System.IO.Stream in, Java.Nio.Charset.Charset charset);
```

Added:

```
public InputStreamReader (System.IO.Stream in, Java.Nio.Charset.Charset charset);
 	public InputStreamReader (System.IO.Stream in, string enc);
 	public InputStreamReader (System.IO.Stream in);
```

 <a name="Type_Changed:_Java.IO.ObjectInputStream" class="injected"></a>


<h3 id='Java.IO.ObjectInputStream'>Type Changed: Java.IO.ObjectInputStream</h3>

Removed:

```
public class ObjectInputStream : InputStream, IDataInput, IObjectInput {
```

Added:

```
public class ObjectInputStream : InputStream {
```

 <a name="Type_Changed:_Java.IO.ObjectOutputStream" class="injected"></a>


<h3 id='Java.IO.ObjectOutputStream'>Type Changed: Java.IO.ObjectOutputStream</h3>

Removed:

```
public class ObjectOutputStream : OutputStream, IDataOutput, IObjectOutput {
 		public abstract void Write (IObjectOutput out);
```

Added:

```
public class ObjectOutputStream : OutputStream {
```

 <a name="Type_Changed:_Java.IO.ObjectStreamField" class="injected"></a>


<h3 id='Java.IO.ObjectStreamField'>Type Changed: Java.IO.ObjectStreamField</h3>

Removed:

```
public ObjectStreamField (string name, Java.Lang.Class cl);
```

Added:

```
public ObjectStreamField (string name, Java.Lang.Class cl);
```

 <a name="Type_Changed:_Java.IO.OutputStream" class="injected"></a>


<h3 id='Java.IO.OutputStream'>Type Changed: Java.IO.OutputStream</h3>

Removed:

```
public abstract class OutputStream : Java.Lang.Object, ICloseable, IFlushable {
```

Added:

```
public abstract class OutputStream : Java.Lang.Object, IFlushable {
```

 <a name="Type_Changed:_Java.IO.OutputStreamWriter" class="injected"></a>


<h3 id='Java.IO.OutputStreamWriter'>Type Changed: Java.IO.OutputStreamWriter</h3>

Removed:

```
public OutputStreamWriter (System.IO.Stream out, string enc);
 	public OutputStreamWriter (System.IO.Stream out);
 	public OutputStreamWriter (System.IO.Stream out, Java.Nio.Charset.Charset cs);
```

Added:

```
public OutputStreamWriter (System.IO.Stream out, Java.Nio.Charset.Charset cs);
 	public OutputStreamWriter (System.IO.Stream out);
 	public OutputStreamWriter (System.IO.Stream out, string enc);
```

 <a name="Type_Changed:_Java.IO.PipedReader" class="injected"></a>


<h3 id='Java.IO.PipedReader'>Type Changed: Java.IO.PipedReader</h3>

Removed:

```
public PipedReader (PipedWriter out);
 	public PipedReader (PipedWriter p0, int p1);
 	public PipedReader ();
```

Added:

```
public PipedReader ();
 	public PipedReader (PipedWriter p0, int p1);
 	public PipedReader (PipedWriter out);
```

 <a name="Type_Changed:_Java.IO.PrintStream" class="injected"></a>


<h3 id='Java.IO.PrintStream'>Type Changed: Java.IO.PrintStream</h3>

Removed:

```
public PrintStream (File file);
```

Added:

```
public PrintStream (File file);
```

 <a name="Type_Changed:_Java.IO.PrintWriter" class="injected"></a>


<h3 id='Java.IO.PrintWriter'>Type Changed: Java.IO.PrintWriter</h3>

Removed:

```
public PrintWriter (Writer wr);
 	public PrintWriter (Writer wr, bool autoflush);
 	public PrintWriter (System.IO.Stream out);
 	public PrintWriter (string fileName, string csn);
```

Added:

```
public PrintWriter (string fileName, string csn);
 	public PrintWriter (Writer wr);
 	public PrintWriter (System.IO.Stream out);
 	public PrintWriter (Writer wr, bool autoflush);
```

 <a name="Type_Changed:_Java.IO.RandomAccessFile" class="injected"></a>


<h3 id='Java.IO.RandomAccessFile'>Type Changed: Java.IO.RandomAccessFile</h3>

Removed:

```
public class RandomAccessFile : Java.Lang.Object, ICloseable, IDataInput, IDataOutput {
```

Added:

```
public class RandomAccessFile : Java.Lang.Object, IDataInput, IDataOutput {
```

 <a name="Type_Changed:_Java.IO.Reader" class="injected"></a>


<h3 id='Java.IO.Reader'>Type Changed: Java.IO.Reader</h3>

Removed:

```
public abstract class Reader : Java.Lang.Object, ICloseable, Java.Lang.IReadable {
```

Added:

```
public abstract class Reader : Java.Lang.Object, Java.Lang.IReadable {
```

 <a name="Type_Changed:_Java.IO.StreamTokenizer" class="injected"></a>


<h3 id='Java.IO.StreamTokenizer'>Type Changed: Java.IO.StreamTokenizer</h3>

Removed:

```
public StreamTokenizer (System.IO.Stream is);
```

Added:

```
public StreamTokenizer (System.IO.Stream is);
```

 <a name="Type_Changed:_Java.IO.Writer" class="injected"></a>


<h3 id='Java.IO.Writer'>Type Changed: Java.IO.Writer</h3>

Removed:

```
public abstract class Writer : Java.Lang.Object, Java.Lang.IAppendable, ICloseable, IFlushable {
```

Added:

```
public abstract class Writer : Java.Lang.Object, Java.Lang.IAppendable, IFlushable {
```

 <a name="Namespace:_Java.Lang" class="injected"></a>


<h2 id='Java.Lang'>Namespace: Java.Lang</h2>

 <a name="Type_Changed:_Java.Lang.AssertionError" class="injected"></a>


<h3 id='Java.Lang.AssertionError'>Type Changed: Java.Lang.AssertionError</h3>

Removed:

```
public AssertionError ();
 	public AssertionError (Object detailMessage);
 	public AssertionError (bool detailMessage);
 	public AssertionError (char detailMessage);
```

Added:

```
public AssertionError (string p0, Throwable p1);
 	public AssertionError ();
 	public AssertionError (Object detailMessage);
 	public AssertionError (bool detailMessage);
 	public AssertionError (char detailMessage);
```

 <a name="Type_Changed:_Java.Lang.Boolean" class="injected"></a>


<h3 id='Java.Lang.Boolean'>Type Changed: Java.Lang.Boolean</h3>

Added:

```
public static int Compare (bool p0, bool p1);
```

 <a name="Type_Changed:_Java.Lang.Byte" class="injected"></a>


<h3 id='Java.Lang.Byte'>Type Changed: Java.Lang.Byte</h3>

Added:

```
public static int Compare (sbyte p0, sbyte p1);
```

 <a name="Type_Changed:_Java.Lang.Character" class="injected"></a>


<h3 id='Java.Lang.Character'>Type Changed: Java.Lang.Character</h3>

Added:

```
public static int Compare (char p0, char p1);
 	public static string GetName (int p0);
 	public static char HighSurrogate (int p0);
 	public static bool IsAlphabetic (int p0);
 	public static bool IsBmpCodePoint (int p0);
 	public static bool IsIdeographic (int p0);
 	public static bool IsSurrogate (char p0);
 	public static char LowSurrogate (int p0);
```

 <a name="Type_Changed:_Java.Lang.ClassLoader" class="injected"></a>


<h3 id='Java.Lang.ClassLoader'>Type Changed: Java.Lang.ClassLoader</h3>

Added:

```
protected static bool RegisterAsParallelCapable ();
 	protected virtual Object GetClassLoadingLock (string p0);
```

 <a name="Type_Changed:_Java.Lang.ClassNotFoundException" class="injected"></a>


<h3 id='Java.Lang.ClassNotFoundException'>Type Changed: Java.Lang.ClassNotFoundException</h3>

Removed:

```
public ClassNotFoundException ();
 	public ClassNotFoundException (string detailMessage);
```

Added:

```
public ClassNotFoundException (string detailMessage);
 	public ClassNotFoundException ();
 	public virtual Throwable Clause {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.Enum" class="injected"></a>


<h3 id='Java.Lang.Enum'>Type Changed: Java.Lang.Enum</h3>

Removed:

```
protected override Object Clone ();
 	public override bool Equals (Object other);
 	public override int GetHashCode ();
```

Added:

```
protected Object Clone ();
 	public bool Equals (Object other);
 	public int GetHashCode ();
```

 <a name="Type_Changed:_Java.Lang.Error" class="injected"></a>


<h3 id='Java.Lang.Error'>Type Changed: Java.Lang.Error</h3>

Removed:

```
public Error ();
 	public Error (string detailMessage);
 	public Error (string detailMessage, Throwable throwable);
```

Added:

```
protected Error (string p0, Throwable p1, bool p2, bool p3);
 	public Error (string detailMessage, Throwable throwable);
 	public Error (string detailMessage);
 	public Error ();
```

 <a name="Type_Changed:_Java.Lang.Exception" class="injected"></a>


<h3 id='Java.Lang.Exception'>Type Changed: Java.Lang.Exception</h3>

Removed:

```
public Exception ();
 	public Exception (string detailMessage);
 	public Exception (string detailMessage, Throwable throwable);
```

Added:

```
protected Exception (string p0, Throwable p1, bool p2, bool p3);
 	public Exception (string detailMessage, Throwable throwable);
 	public Exception (string detailMessage);
 	public Exception ();
```

 <a name="Type_Changed:_Java.Lang.ExceptionInInitializerError" class="injected"></a>


<h3 id='Java.Lang.ExceptionInInitializerError'>Type Changed: Java.Lang.ExceptionInInitializerError</h3>

Removed:

```
public ExceptionInInitializerError ();
 	public ExceptionInInitializerError (Throwable exception);
```

Added:

```
public ExceptionInInitializerError (Throwable exception);
 	public ExceptionInInitializerError ();
```

 <a name="Type_Changed:_Java.Lang.Float" class="injected"></a>


<h3 id='Java.Lang.Float'>Type Changed: Java.Lang.Float</h3>

Removed:

```
public Float (float value);
 	public Float (double value);
```

Added:

```
public Float (double value);
 	public Float (float value);
```

 <a name="Type_Changed:_Java.Lang.IllegalAccessException" class="injected"></a>


<h3 id='Java.Lang.IllegalAccessException'>Type Changed: Java.Lang.IllegalAccessException</h3>

Added:

```
public virtual Throwable Clause {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.IllegalArgumentException" class="injected"></a>


<h3 id='Java.Lang.IllegalArgumentException'>Type Changed: Java.Lang.IllegalArgumentException</h3>

Removed:

```
public IllegalArgumentException ();
 	public IllegalArgumentException (string detailMessage);
 	public IllegalArgumentException (string message, Throwable cause);
```

Added:

```
public IllegalArgumentException (string message, Throwable cause);
 	public IllegalArgumentException (string detailMessage);
 	public IllegalArgumentException ();
```

 <a name="Type_Changed:_Java.Lang.IllegalStateException" class="injected"></a>


<h3 id='Java.Lang.IllegalStateException'>Type Changed: Java.Lang.IllegalStateException</h3>

Removed:

```
public IllegalStateException ();
 	public IllegalStateException (string detailMessage);
 	public IllegalStateException (string message, Throwable cause);
```

Added:

```
public IllegalStateException (string message, Throwable cause);
 	public IllegalStateException (string detailMessage);
 	public IllegalStateException ();
```

 <a name="Type_Changed:_Java.Lang.InstantiationException" class="injected"></a>


<h3 id='Java.Lang.InstantiationException'>Type Changed: Java.Lang.InstantiationException</h3>

Added:

```
public virtual Throwable Clause {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.Integer" class="injected"></a>


<h3 id='Java.Lang.Integer'>Type Changed: Java.Lang.Integer</h3>

Added:

```
public static int Compare (int p0, int p1);
```

 <a name="Type_Changed:_Java.Lang.JavaSystem" class="injected"></a>


<h3 id='Java.Lang.JavaSystem'>Type Changed: Java.Lang.JavaSystem</h3>

Removed:

```
public static Java.Nio.Channels.IChannel InheritedChannel ();
```

Added:

```
public static string LineSeparator ();
```

 <a name="Type_Changed:_Java.Lang.LinkageError" class="injected"></a>


<h3 id='Java.Lang.LinkageError'>Type Changed: Java.Lang.LinkageError</h3>

Added:

```
public LinkageError (string p0, Throwable p1);
```

 <a name="Type_Changed:_Java.Lang.Long" class="injected"></a>


<h3 id='Java.Lang.Long'>Type Changed: Java.Lang.Long</h3>

Added:

```
public static int Compare (long p0, long p1);
```

 <a name="Type_Changed:_Java.Lang.NoSuchFieldException" class="injected"></a>


<h3 id='Java.Lang.NoSuchFieldException'>Type Changed: Java.Lang.NoSuchFieldException</h3>

Added:

```
public virtual Throwable Clause {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.NoSuchMethodException" class="injected"></a>


<h3 id='Java.Lang.NoSuchMethodException'>Type Changed: Java.Lang.NoSuchMethodException</h3>

Added:

```
public virtual Throwable Clause {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.ProcessBuilder" class="injected"></a>


<h3 id='Java.Lang.ProcessBuilder'>Type Changed: Java.Lang.ProcessBuilder</h3>

Added:

```
public ProcessBuilder InheritIO ();
 	public ProcessBuilder RedirectError (Java.IO.File p0);
 	public ProcessBuilder RedirectInput (Java.IO.File p0);
 	public ProcessBuilder RedirectOutput (Java.IO.File p0);
```

 <a name="Type_Changed:_Java.Lang.RuntimeException" class="injected"></a>


<h3 id='Java.Lang.RuntimeException'>Type Changed: Java.Lang.RuntimeException</h3>

Removed:

```
public RuntimeException ();
 	public RuntimeException (string detailMessage);
 	public RuntimeException (string detailMessage, Throwable throwable);
```

Added:

```
protected RuntimeException (string p0, Throwable p1, bool p2, bool p3);
 	public RuntimeException (string detailMessage, Throwable throwable);
 	public RuntimeException (string detailMessage);
 	public RuntimeException ();
```

 <a name="Type_Changed:_Java.Lang.SecurityException" class="injected"></a>


<h3 id='Java.Lang.SecurityException'>Type Changed: Java.Lang.SecurityException</h3>

Removed:

```
public SecurityException ();
 	public SecurityException (string detailMessage);
 	public SecurityException (string message, Throwable cause);
```

Added:

```
public SecurityException (string message, Throwable cause);
 	public SecurityException (string detailMessage);
 	public SecurityException ();
```

 <a name="Type_Changed:_Java.Lang.Short" class="injected"></a>


<h3 id='Java.Lang.Short'>Type Changed: Java.Lang.Short</h3>

Added:

```
public static int Compare (short p0, short p1);
```

 <a name="Type_Changed:_Java.Lang.String" class="injected"></a>


<h3 id='Java.Lang.String'>Type Changed: Java.Lang.String</h3>

Removed:

```
public String ();
 	public String (string string);
 	public String (char [] data);
 	public String (char [] data, int start, int length);
 	public String (int [] codePoints, int offset, int count);
 	public String (byte [] data, int high, int start, int length);
 	public String (byte [] data, int high);
 	public String (byte [] data, int start, int length, string encoding);
 	public String (byte [] p0, int p1, int p2, Java.Nio.Charset.Charset p3);
 	public String (byte [] data, string encoding);
 	public String (byte [] p0, Java.Nio.Charset.Charset p1);
 	public String (byte [] data, int start, int length);
 	public String (StringBuffer stringbuffer);
```

Added:

```
public String (byte [] data, int start, int length);
 	public String (byte [] p0, Java.Nio.Charset.Charset p1);
 	public String (byte [] data, string encoding);
 	public String (byte [] p0, int p1, int p2, Java.Nio.Charset.Charset p3);
 	public String (StringBuffer stringbuffer);
 	public String (int [] codePoints, int offset, int count);
 	public String (char [] data, int start, int length);
 	public String (char [] data);
 	public String (string string);
 	public String ();
 	public String (byte [] data, int start, int length, string encoding);
 	public String (byte [] data, int high);
 	public String (byte [] data, int high, int start, int length);
```

 <a name="Type_Changed:_Java.Lang.StringBuffer" class="injected"></a>


<h3 id='Java.Lang.StringBuffer'>Type Changed: Java.Lang.StringBuffer</h3>

Removed:

```
public StringBuffer ();
 	public StringBuffer (int capacity);
 	public StringBuffer (string string);
```

Added:

```
public StringBuffer (string string);
 	public StringBuffer (int capacity);
 	public StringBuffer ();
```

 <a name="Type_Changed:_Java.Lang.StringBuilder" class="injected"></a>


<h3 id='Java.Lang.StringBuilder'>Type Changed: Java.Lang.StringBuilder</h3>

Removed:

```
public StringBuilder ();
 	public StringBuilder (int capacity);
 	public StringBuilder (string str);
```

Added:

```
public StringBuilder (string str);
 	public StringBuilder (int capacity);
 	public StringBuilder ();
```

 <a name="Type_Changed:_Java.Lang.SuppressWarnings" class="injected"></a>


<h3 id='Java.Lang.SuppressWarnings'>Type Changed: Java.Lang.SuppressWarnings</h3>

Added:

```
public abstract string [] Value ();
```

 <a name="Type_Changed:_Java.Lang.Thread" class="injected"></a>


<h3 id='Java.Lang.Thread'>Type Changed: Java.Lang.Thread</h3>

Removed:

```
public Thread ();
 	public Thread (IRunnable runnable);
 	public Thread (ThreadGroup group, IRunnable runnable);
 	public Thread (ThreadGroup group, string threadName);
 	public Thread (IRunnable runnable, string threadName);
 	public Thread (ThreadGroup group, IRunnable runnable, string threadName);
```

Added:

```
public Thread (ThreadGroup group, IRunnable runnable);
 	public Thread (IRunnable runnable);
 	public Thread ();
 	public Thread (ThreadGroup group, IRunnable runnable, string threadName);
 	public Thread (IRunnable runnable, string threadName);
 	public Thread (ThreadGroup group, string threadName);
```

 <a name="Type_Changed:_Java.Lang.ThreadGroup" class="injected"></a>


<h3 id='Java.Lang.ThreadGroup'>Type Changed: Java.Lang.ThreadGroup</h3>

Removed:

```
public ThreadGroup (string name);
```

Added:

```
public ThreadGroup (string name);
```

 <a name="Type_Changed:_Java.Lang.Throwable" class="injected"></a>


<h3 id='Java.Lang.Throwable'>Type Changed: Java.Lang.Throwable</h3>

Removed:

```
public Throwable ();
 	public Throwable (string detailMessage);
 	public Throwable (string detailMessage, Throwable throwable);
```

Added:

```
protected Throwable (string p0, Throwable p1, bool p2, bool p3);
 	public Throwable (string detailMessage, Throwable throwable);
 	public Throwable (string detailMessage);
 	public Throwable ();
 	public void AddSuppressed (Throwable p0);
 	public Throwable[] GetSuppressed ();
```

 <a name="Type_Changed:_Java.Lang.UnsupportedOperationException" class="injected"></a>


<h3 id='Java.Lang.UnsupportedOperationException'>Type Changed: Java.Lang.UnsupportedOperationException</h3>

Removed:

```
public UnsupportedOperationException ();
 	public UnsupportedOperationException (string detailMessage);
 	public UnsupportedOperationException (string message, Throwable cause);
```

Added:

```
public UnsupportedOperationException (string message, Throwable cause);
 	public UnsupportedOperationException (string detailMessage);
 	public UnsupportedOperationException ();
```

 <a name="Namespace:_Java.Lang.Annotation" class="injected"></a>


<h2 id='Java.Lang.Annotation'>Namespace: Java.Lang.Annotation</h2>

 <a name="Type_Changed:_Java.Lang.Annotation.Retention" class="injected"></a>


<h3 id='Java.Lang.Annotation.Retention'>Type Changed: Java.Lang.Annotation.Retention</h3>

Added:

```
public abstract RetentionPolicy Value ();
```

 <a name="Type_Changed:_Java.Lang.Annotation.Target" class="injected"></a>


<h3 id='Java.Lang.Annotation.Target'>Type Changed: Java.Lang.Annotation.Target</h3>

Added:

```
public abstract ElementType[] Value ();
```

 <a name="Namespace:_Java.Math" class="injected"></a>


<h2 id='Java.Math'>Namespace: Java.Math</h2>

 <a name="Type_Changed:_Java.Math.BigDecimal" class="injected"></a>


<h3 id='Java.Math.BigDecimal'>Type Changed: Java.Math.BigDecimal</h3>

Removed:

```
public BigDecimal (char [] in, int offset, int len);
 	public BigDecimal (char [] in, int offset, int len, MathContext mc);
 	public BigDecimal (char [] in);
 	public BigDecimal (char [] in, MathContext mc);
 	public BigDecimal (string val);
 	public BigDecimal (string val, MathContext mc);
 	public BigDecimal (double val);
 	public BigDecimal (double val, MathContext mc);
 	public BigDecimal (BigInteger val);
 	public BigDecimal (BigInteger val, MathContext mc);
 	public BigDecimal (BigInteger unscaledVal, int scale);
 	public BigDecimal (int val);
 	public BigDecimal (int val, MathContext mc);
 	public BigDecimal (long val);
```

Added:

```
public BigDecimal (BigInteger unscaledVal, int scale);
 	public BigDecimal (BigInteger val, MathContext mc);
 	public BigDecimal (BigInteger val);
 	public BigDecimal (double val, MathContext mc);
 	public BigDecimal (long val);
 	public BigDecimal (int val, MathContext mc);
 	public BigDecimal (int val);
 	public BigDecimal (char [] in);
 	public BigDecimal (char [] in, int offset, int len, MathContext mc);
 	public BigDecimal (char [] in, int offset, int len);
 	public BigDecimal (double val);
 	public BigDecimal (string val, MathContext mc);
 	public BigDecimal (string val);
 	public BigDecimal (char [] in, MathContext mc);
```

 <a name="Type_Changed:_Java.Math.BigInteger" class="injected"></a>


<h3 id='Java.Math.BigInteger'>Type Changed: Java.Math.BigInteger</h3>

Removed:

```
public BigInteger (byte [] val);
 	public BigInteger (int signum, byte [] magnitude);
 	public BigInteger (string val, int radix);
```

Added:

```
public BigInteger (byte [] val);
 	public BigInteger (int signum, byte [] magnitude);
 	public BigInteger (string val, int radix);
```

 <a name="Type_Changed:_Java.Math.MathContext" class="injected"></a>


<h3 id='Java.Math.MathContext'>Type Changed: Java.Math.MathContext</h3>

Removed:

```
public MathContext (int precision);
 	public MathContext (int precision, RoundingMode roundingMode);
```

Added:

```
public MathContext (int precision, RoundingMode roundingMode);
 	public MathContext (int precision);
```

 <a name="Namespace:_Java.Net" class="injected"></a>


<h2 id='Java.Net'>Namespace: Java.Net</h2>

 <a name="Type_Changed:_Java.Net.DatagramPacket" class="injected"></a>


<h3 id='Java.Net.DatagramPacket'>Type Changed: Java.Net.DatagramPacket</h3>

Removed:

```
public DatagramPacket (byte [] data, int offset, int length, SocketAddress sockAddr);
 	public DatagramPacket (byte [] data, int length, InetAddress host, int port);
 	public DatagramPacket (byte [] data, int length, SocketAddress sockAddr);
```

Added:

```
public DatagramPacket (byte [] data, int length, SocketAddress sockAddr);
 	public DatagramPacket (byte [] data, int length, InetAddress host, int port);
 	public DatagramPacket (byte [] data, int offset, int length, SocketAddress sockAddr);
```

 <a name="Type_Changed:_Java.Net.DatagramSocket" class="injected"></a>


<h3 id='Java.Net.DatagramSocket'>Type Changed: Java.Net.DatagramSocket</h3>

Removed:

```
public DatagramSocket ();
 	protected DatagramSocket (DatagramSocketImpl socketImpl);
 	public DatagramSocket (SocketAddress localAddr);
```

Added:

```
public DatagramSocket (SocketAddress localAddr);
 	protected DatagramSocket (DatagramSocketImpl socketImpl);
 	public DatagramSocket ();
```

 <a name="Type_Changed:_Java.Net.HttpURLConnection" class="injected"></a>


<h3 id='Java.Net.HttpURLConnection'>Type Changed: Java.Net.HttpURLConnection</h3>

Added:

```
public virtual void SetFixedLengthStreamingMode (long p0);
 	protected long FixedContentLengthLong {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_Java.Net.InetAddress" class="injected"></a>


<h3 id='Java.Net.InetAddress'>Type Changed: Java.Net.InetAddress</h3>

Added:

```
public static InetAddress LoopbackAddress {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Net.InetSocketAddress" class="injected"></a>


<h3 id='Java.Net.InetSocketAddress'>Type Changed: Java.Net.InetSocketAddress</h3>

Removed:

```
public InetSocketAddress (int port);
 	public InetSocketAddress (InetAddress address, int port);
 	public override bool Equals (Java.Lang.Object socketAddr);
 	public override int GetHashCode ();
```

Added:

```
public InetSocketAddress (InetAddress address, int port);
 	public InetSocketAddress (int port);
 	public bool Equals (Java.Lang.Object socketAddr);
 	public int GetHashCode ();
 	public string HostString {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Net.MulticastSocket" class="injected"></a>


<h3 id='Java.Net.MulticastSocket'>Type Changed: Java.Net.MulticastSocket</h3>

Removed:

```
public MulticastSocket ();
 	public MulticastSocket (int aPort);
```

Added:

```
public MulticastSocket (int aPort);
 	public MulticastSocket ();
```

 <a name="Type_Changed:_Java.Net.NetworkInterface" class="injected"></a>


<h3 id='Java.Net.NetworkInterface'>Type Changed: Java.Net.NetworkInterface</h3>

Added:

```
public static NetworkInterface GetByIndex (int p0);
 	public int Index {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Net.Proxy" class="injected"></a>


<h3 id='Java.Net.Proxy'>Type Changed: Java.Net.Proxy</h3>

Removed:

```
public override bool Equals (Java.Lang.Object obj);
 	public override int GetHashCode ();
```

Added:

```
public bool Equals (Java.Lang.Object obj);
 	public int GetHashCode ();
```

 <a name="Type_Changed:_Java.Net.ServerSocket" class="injected"></a>


<h3 id='Java.Net.ServerSocket'>Type Changed: Java.Net.ServerSocket</h3>

Removed:

```
public ServerSocket ();
 	public ServerSocket (int aport);
 	public ServerSocket (int aport, int backlog);
```

Added:

```
public ServerSocket (int aport, int backlog);
 	public ServerSocket (int aport);
 	public ServerSocket ();
```

 <a name="Type_Changed:_Java.Net.Socket" class="injected"></a>


<h3 id='Java.Net.Socket'>Type Changed: Java.Net.Socket</h3>

Removed:

```
public Socket (string dstName, int dstPort, InetAddress localAddress, int localPort);
 	public Socket (InetAddress dstAddress, int dstPort, InetAddress localAddress, int localPort);
 	public Socket (string hostName, int port, bool streaming);
 	public Socket (InetAddress addr, int port, bool streaming);
```

Added:

```
public Socket (string dstName, int dstPort, InetAddress localAddress, int localPort);
 	public Socket (InetAddress dstAddress, int dstPort, InetAddress localAddress, int localPort);
 	public Socket (string hostName, int port, bool streaming);
 	public Socket (InetAddress addr, int port, bool streaming);
```

 <a name="Type_Changed:_Java.Net.URI" class="injected"></a>


<h3 id='Java.Net.URI'>Type Changed: Java.Net.URI</h3>

Removed:

```
public URI (string scheme, string authority, string path, string query, string fragment);
 	public URI (string scheme, string host, string path, string fragment);
 	public URI (string scheme, string ssp, string frag);
```

Added:

```
public URI (string scheme, string ssp, string frag);
 	public URI (string scheme, string host, string path, string fragment);
 	public URI (string scheme, string authority, string path, string query, string fragment);
```

 <a name="Type_Changed:_Java.Net.URL" class="injected"></a>


<h3 id='Java.Net.URL'>Type Changed: Java.Net.URL</h3>

Removed:

```
public URL (string spec);
 	public URL (URL context, string spec);
 	public URL (URL context, string spec, URLStreamHandler handler);
```

Added:

```
public URL (URL context, string spec, URLStreamHandler handler);
 	public URL (URL context, string spec);
 	public URL (string spec);
```

 <a name="Type_Changed:_Java.Net.URLClassLoader" class="injected"></a>


<h3 id='Java.Net.URLClassLoader'>Type Changed: Java.Net.URLClassLoader</h3>

Removed:

```
public URLClassLoader (URL[] urls, Java.Lang.ClassLoader parent);
 	public URLClassLoader (URL[] urls);
```

Added:

```
public URLClassLoader (URL[] urls);
 	public URLClassLoader (URL[] urls, Java.Lang.ClassLoader parent);
 	public virtual void Close ();
```

 <a name="Type_Changed:_Java.Net.URLConnection" class="injected"></a>


<h3 id='Java.Net.URLConnection'>Type Changed: Java.Net.URLConnection</h3>

Added:

```
public virtual long GetHeaderFieldLong (string p0, long p1);
 	public virtual long ContentLengthLong {
 		get;
 	}
```

 <a name="Namespace:_Java.Nio" class="injected"></a>


<h2 id='Java.Nio'>Namespace: Java.Nio</h2>

 <a name="Type_Changed:_Java.Nio.ByteBuffer" class="injected"></a>


<h3 id='Java.Nio.ByteBuffer'>Type Changed: Java.Nio.ByteBuffer</h3>

Removed:

```
public override int ArrayOffset ();
```

Added:

```
public int ArrayOffset ();
```

 <a name="Type_Changed:_Java.Nio.CharBuffer" class="injected"></a>


<h3 id='Java.Nio.CharBuffer'>Type Changed: Java.Nio.CharBuffer</h3>

Removed:

```
public override int ArrayOffset ();
 	public virtual int CompareTo (Java.Lang.Object p0);
```

Added:

```
public int ArrayOffset ();
```

 <a name="Type_Changed:_Java.Nio.DoubleBuffer" class="injected"></a>


<h3 id='Java.Nio.DoubleBuffer'>Type Changed: Java.Nio.DoubleBuffer</h3>

Removed:

```
public override int ArrayOffset ();
```

Added:

```
public int ArrayOffset ();
```

 <a name="Type_Changed:_Java.Nio.FloatBuffer" class="injected"></a>


<h3 id='Java.Nio.FloatBuffer'>Type Changed: Java.Nio.FloatBuffer</h3>

Removed:

```
public override int ArrayOffset ();
```

Added:

```
public int ArrayOffset ();
```

 <a name="Type_Changed:_Java.Nio.IntBuffer" class="injected"></a>


<h3 id='Java.Nio.IntBuffer'>Type Changed: Java.Nio.IntBuffer</h3>

Removed:

```
public override int ArrayOffset ();
```

Added:

```
public int ArrayOffset ();
```

 <a name="Type_Changed:_Java.Nio.LongBuffer" class="injected"></a>


<h3 id='Java.Nio.LongBuffer'>Type Changed: Java.Nio.LongBuffer</h3>

Removed:

```
public override int ArrayOffset ();
```

Added:

```
public int ArrayOffset ();
```

 <a name="Type_Changed:_Java.Nio.ShortBuffer" class="injected"></a>


<h3 id='Java.Nio.ShortBuffer'>Type Changed: Java.Nio.ShortBuffer</h3>

Removed:

```
public override int ArrayOffset ();
```

Added:

```
public int ArrayOffset ();
```

 <a name="Namespace:_Java.Nio.Channels" class="injected"></a>


<h2 id='Java.Nio.Channels'>Namespace: Java.Nio.Channels</h2>

 <a name="Type_Changed:_Java.Nio.Channels.Channels" class="injected"></a>


<h3 id='Java.Nio.Channels.Channels'>Type Changed: Java.Nio.Channels.Channels</h3>

Removed:

```
public static System.IO.Stream NewInputStream (IReadableByteChannel channel);
 	public static System.IO.Stream NewOutputStream (IWritableByteChannel channel);
 	public static IReadableByteChannel NewReadableChannel (System.IO.Stream inputStream);
 	public static Java.IO.Reader NewReader (IReadableByteChannel channel, Java.Nio.Charset.CharsetDecoder decoder, int minBufferCapacity);
 	public static Java.IO.Reader NewReader (IReadableByteChannel channel, string charsetName);
 	public static IWritableByteChannel NewWritableChannel (System.IO.Stream outputStream);
 	public static Java.IO.Writer NewWriter (IWritableByteChannel channel, Java.Nio.Charset.CharsetEncoder encoder, int minBufferCapacity);
 	public static Java.IO.Writer NewWriter (IWritableByteChannel channel, string charsetName);
 	
 	protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Nio.Channels.DatagramChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.DatagramChannel'>Type Changed: Java.Nio.Channels.DatagramChannel</h3>

Removed:

```
public abstract class DatagramChannel : Java.Nio.Channels.Spi.AbstractSelectableChannel, IByteChannel, IGatheringByteChannel, IReadableByteChannel, IScatteringByteChannel, IWritableByteChannel {
 	public override Operations ValidOps ();
```

Added:

```
public abstract class DatagramChannel : Java.Nio.Channels.Spi.AbstractSelectableChannel {
 	public abstract DatagramChannel Bind (Java.Net.SocketAddress p0);
 	public Operations ValidOps ();
 	public abstract Java.Net.SocketAddress RemoteAddress {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Nio.Channels.FileChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.FileChannel'>Type Changed: Java.Nio.Channels.FileChannel</h3>

Removed:

```
public abstract class FileChannel : Java.Nio.Channels.Spi.AbstractInterruptibleChannel, IByteChannel, IGatheringByteChannel, IReadableByteChannel, IScatteringByteChannel, IWritableByteChannel {
 	public abstract long TransferFrom (IReadableByteChannel src, long position, long count);
 	public abstract long TransferTo (long position, long count, IWritableByteChannel target);
```

Added:

```
public abstract class FileChannel : Java.Nio.Channels.Spi.AbstractInterruptibleChannel {
```

 <a name="Type_Changed:_Java.Nio.Channels.FileLock" class="injected"></a>


<h3 id='Java.Nio.Channels.FileLock'>Type Changed: Java.Nio.Channels.FileLock</h3>

Removed:

```
public override string ToString ();
```

Added:

```
public void Close ();
 	public string ToString ();
```

 <a name="Type_Removed:_Java.Nio.Channels.IByteChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.IByteChannel'>Type Removed: Java.Nio.Channels.IByteChannel</h3>

 <a name="Type_Removed:_Java.Nio.Channels.IChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.IChannel'>Type Removed: Java.Nio.Channels.IChannel</h3>

 <a name="Type_Removed:_Java.Nio.Channels.IGatheringByteChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.IGatheringByteChannel'>Type Removed: Java.Nio.Channels.IGatheringByteChannel</h3>

 <a name="Type_Removed:_Java.Nio.Channels.IInterruptibleChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.IInterruptibleChannel'>Type Removed: Java.Nio.Channels.IInterruptibleChannel</h3>

 <a name="Type_Removed:_Java.Nio.Channels.IReadableByteChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.IReadableByteChannel'>Type Removed: Java.Nio.Channels.IReadableByteChannel</h3>

 <a name="Type_Removed:_Java.Nio.Channels.IScatteringByteChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.IScatteringByteChannel'>Type Removed: Java.Nio.Channels.IScatteringByteChannel</h3>

 <a name="Type_Removed:_Java.Nio.Channels.IWritableByteChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.IWritableByteChannel'>Type Removed: Java.Nio.Channels.IWritableByteChannel</h3>

 <a name="Type_Changed:_Java.Nio.Channels.Pipe" class="injected"></a>


<h3 id='Java.Nio.Channels.Pipe'>Type Changed: Java.Nio.Channels.Pipe</h3>

Removed:

```
public abstract class SinkChannel : Java.Nio.Channels.Spi.AbstractSelectableChannel, IGatheringByteChannel, IWritableByteChannel {
 		public override Operations ValidOps ();
 		public abstract int Write (Java.Nio.ByteBuffer buffer);
 		public abstract long Write (Java.Nio.ByteBuffer[] buffers);
 		public abstract long Write (Java.Nio.ByteBuffer[] buffers, int offset, int length);
 	public abstract class SourceChannel : Java.Nio.Channels.Spi.AbstractSelectableChannel, IReadableByteChannel, IScatteringByteChannel {
 		public abstract int Read (Java.Nio.ByteBuffer buffer);
 		public abstract long Read (Java.Nio.ByteBuffer[] buffers);
 		public abstract long Read (Java.Nio.ByteBuffer[] buffers, int offset, int length);
 		public override Operations ValidOps ();
```

Added:

```
public abstract class SinkChannel : Java.Nio.Channels.Spi.AbstractSelectableChannel {
 		public Operations ValidOps ();
 	public abstract class SourceChannel : Java.Nio.Channels.Spi.AbstractSelectableChannel {
 		public Operations ValidOps ();
```

 <a name="Type_Changed:_Java.Nio.Channels.ServerSocketChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.ServerSocketChannel'>Type Changed: Java.Nio.Channels.ServerSocketChannel</h3>

Removed:

```
public override Operations ValidOps ();
```

Added:

```
public ServerSocketChannel Bind (Java.Net.SocketAddress p0);
 	public abstract ServerSocketChannel Bind (Java.Net.SocketAddress p0, int p1);
 	public Operations ValidOps ();
```

 <a name="Type_Changed:_Java.Nio.Channels.SocketChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.SocketChannel'>Type Changed: Java.Nio.Channels.SocketChannel</h3>

Removed:

```
public abstract class SocketChannel : Java.Nio.Channels.Spi.AbstractSelectableChannel, IByteChannel, IGatheringByteChannel, IReadableByteChannel, IScatteringByteChannel, IWritableByteChannel {
 	public override Operations ValidOps ();
```

Added:

```
public abstract class SocketChannel : Java.Nio.Channels.Spi.AbstractSelectableChannel {
 	public abstract SocketChannel Bind (Java.Net.SocketAddress p0);
 	public abstract SocketChannel ShutdownInput ();
 	public abstract SocketChannel ShutdownOutput ();
 	public Operations ValidOps ();
 	public abstract Java.Net.SocketAddress RemoteAddress {
 		get;
 	}
```

 <a name="Namespace:_Java.Nio.Channels.Spi" class="injected"></a>


<h2 id='Java.Nio.Channels.Spi'>Namespace: Java.Nio.Channels.Spi</h2>

 <a name="Type_Changed:_Java.Nio.Channels.Spi.AbstractInterruptibleChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.Spi.AbstractInterruptibleChannel'>Type Changed: Java.Nio.Channels.Spi.AbstractInterruptibleChannel</h3>

Removed:

```
public abstract class AbstractInterruptibleChannel : Java.Lang.Object, Java.Nio.Channels.IChannel, Java.IO.ICloseable, Java.Nio.Channels.IInterruptibleChannel {
```

Added:

```
public abstract class AbstractInterruptibleChannel : Java.Lang.Object {
```

 <a name="Type_Changed:_Java.Nio.Channels.Spi.AbstractSelectableChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.Spi.AbstractSelectableChannel'>Type Changed: Java.Nio.Channels.Spi.AbstractSelectableChannel</h3>

Removed:

```
public override Java.Lang.Object BlockingLock ();
 	public override Java.Nio.Channels.SelectableChannel ConfigureBlocking (bool blockingMode);
 	protected override void ImplCloseChannel ();
 	public override Java.Nio.Channels.SelectionKey KeyFor (Java.Nio.Channels.Selector selector);
 	public override SelectorProvider Provider ();
 	public override Java.Nio.Channels.SelectionKey Register (Java.Nio.Channels.Selector selector, Java.Nio.Channels.Operations interestSet, Java.Lang.Object attachment);
```

Added:

```
public Java.Lang.Object BlockingLock ();
 	public Java.Nio.Channels.SelectableChannel ConfigureBlocking (bool blockingMode);
 	protected void ImplCloseChannel ();
 	public Java.Nio.Channels.SelectionKey KeyFor (Java.Nio.Channels.Selector selector);
 	public SelectorProvider Provider ();
 	public Java.Nio.Channels.SelectionKey Register (Java.Nio.Channels.Selector selector, Java.Nio.Channels.Operations interestSet, Java.Lang.Object attachment);
```

 <a name="Type_Changed:_Java.Nio.Channels.Spi.AbstractSelectionKey" class="injected"></a>


<h3 id='Java.Nio.Channels.Spi.AbstractSelectionKey'>Type Changed: Java.Nio.Channels.Spi.AbstractSelectionKey</h3>

Removed:

```
public override void Cancel ();
```

Added:

```
public void Cancel ();
```

 <a name="Type_Changed:_Java.Nio.Channels.Spi.AbstractSelector" class="injected"></a>


<h3 id='Java.Nio.Channels.Spi.AbstractSelector'>Type Changed: Java.Nio.Channels.Spi.AbstractSelector</h3>

Removed:

```
public override void Close ();
 	public override SelectorProvider Provider ();
```

Added:

```
public void Close ();
 	public SelectorProvider Provider ();
```

 <a name="Type_Changed:_Java.Nio.Channels.Spi.SelectorProvider" class="injected"></a>


<h3 id='Java.Nio.Channels.Spi.SelectorProvider'>Type Changed: Java.Nio.Channels.Spi.SelectorProvider</h3>

Removed:

```
public virtual Java.Nio.Channels.IChannel InheritedChannel ();
```

 <a name="Namespace:_Java.Nio.Charset" class="injected"></a>


<h2 id='Java.Nio.Charset'>Namespace: Java.Nio.Charset</h2>

 <a name="Type_Changed:_Java.Nio.Charset.Charset" class="injected"></a>


<h3 id='Java.Nio.Charset.Charset'>Type Changed: Java.Nio.Charset.Charset</h3>

Removed:

```
public override bool Equals (Java.Lang.Object obj);
 	public override int GetHashCode ();
 	public override string ToString ();
```

Added:

```
public bool Equals (Java.Lang.Object obj);
 	public int GetHashCode ();
 	public string ToString ();
```

 <a name="Namespace:_Java.Security" class="injected"></a>


<h2 id='Java.Security'>Namespace: Java.Security</h2>

 <a name="Type_Changed:_Java.Security.AccessControlContext" class="injected"></a>


<h3 id='Java.Security.AccessControlContext'>Type Changed: Java.Security.AccessControlContext</h3>

Removed:

```
public AccessControlContext (ProtectionDomain[] context);
```

Added:

```
public AccessControlContext (ProtectionDomain[] context);
```

 <a name="Type_Changed:_Java.Security.AlgorithmParameters" class="injected"></a>


<h3 id='Java.Security.AlgorithmParameters'>Type Changed: Java.Security.AlgorithmParameters</h3>

Removed:

```
public override string ToString ();
```

Added:

```
public string ToString ();
```

 <a name="Type_Changed:_Java.Security.BasicPermission" class="injected"></a>


<h3 id='Java.Security.BasicPermission'>Type Changed: Java.Security.BasicPermission</h3>

Removed:

```
public BasicPermission (string name);
```

Added:

```
public BasicPermission (string name);
```

 <a name="Type_Changed:_Java.Security.DigestException" class="injected"></a>


<h3 id='Java.Security.DigestException'>Type Changed: Java.Security.DigestException</h3>

Removed:

```
public DigestException ();
 	public DigestException (string msg);
 	public DigestException (string message, Java.Lang.Throwable cause);
```

Added:

```
public DigestException (string message, Java.Lang.Throwable cause);
 	public DigestException (string msg);
 	public DigestException ();
```

 <a name="Type_Changed:_Java.Security.GeneralSecurityException" class="injected"></a>


<h3 id='Java.Security.GeneralSecurityException'>Type Changed: Java.Security.GeneralSecurityException</h3>

Removed:

```
public GeneralSecurityException ();
 	public GeneralSecurityException (string msg);
 	public GeneralSecurityException (string message, Java.Lang.Throwable cause);
```

Added:

```
public GeneralSecurityException (string message, Java.Lang.Throwable cause);
 	public GeneralSecurityException (string msg);
 	public GeneralSecurityException ();
```

 <a name="Type_Changed:_Java.Security.Identity" class="injected"></a>


<h3 id='Java.Security.Identity'>Type Changed: Java.Security.Identity</h3>

Removed:

```
protected Identity ();
 	public Identity (string name, IdentityScope scope);
 	public override bool Equals (Java.Lang.Object obj);
```

Added:

```
public Identity (string name, IdentityScope scope);
 	protected Identity ();
 	public bool Equals (Java.Lang.Object obj);
```

 <a name="Type_Changed:_Java.Security.IdentityScope" class="injected"></a>


<h3 id='Java.Security.IdentityScope'>Type Changed: Java.Security.IdentityScope</h3>

Removed:

```
protected IdentityScope ();
```

Added:

```
protected IdentityScope ();
```

 <a name="Type_Changed:_Java.Security.InvalidAlgorithmParameterException" class="injected"></a>


<h3 id='Java.Security.InvalidAlgorithmParameterException'>Type Changed: Java.Security.InvalidAlgorithmParameterException</h3>

Removed:

```
public InvalidAlgorithmParameterException ();
 	public InvalidAlgorithmParameterException (string msg);
 	public InvalidAlgorithmParameterException (string message, Java.Lang.Throwable cause);
```

Added:

```
public InvalidAlgorithmParameterException (string message, Java.Lang.Throwable cause);
 	public InvalidAlgorithmParameterException (string msg);
 	public InvalidAlgorithmParameterException ();
```

 <a name="Type_Changed:_Java.Security.InvalidKeyException" class="injected"></a>


<h3 id='Java.Security.InvalidKeyException'>Type Changed: Java.Security.InvalidKeyException</h3>

Removed:

```
public InvalidKeyException ();
 	public InvalidKeyException (string msg);
 	public InvalidKeyException (string message, Java.Lang.Throwable cause);
```

Added:

```
public InvalidKeyException (string message, Java.Lang.Throwable cause);
 	public InvalidKeyException (string msg);
 	public InvalidKeyException ();
```

 <a name="Type_Changed:_Java.Security.KeyException" class="injected"></a>


<h3 id='Java.Security.KeyException'>Type Changed: Java.Security.KeyException</h3>

Removed:

```
public KeyException ();
 	public KeyException (string msg);
 	public KeyException (string message, Java.Lang.Throwable cause);
```

Added:

```
public KeyException (string message, Java.Lang.Throwable cause);
 	public KeyException (string msg);
 	public KeyException ();
```

 <a name="Type_Changed:_Java.Security.KeyManagementException" class="injected"></a>


<h3 id='Java.Security.KeyManagementException'>Type Changed: Java.Security.KeyManagementException</h3>

Removed:

```
public KeyManagementException ();
 	public KeyManagementException (string msg);
 	public KeyManagementException (string message, Java.Lang.Throwable cause);
```

Added:

```
public KeyManagementException (string message, Java.Lang.Throwable cause);
 	public KeyManagementException (string msg);
 	public KeyManagementException ();
```

 <a name="Type_Changed:_Java.Security.KeyStoreException" class="injected"></a>


<h3 id='Java.Security.KeyStoreException'>Type Changed: Java.Security.KeyStoreException</h3>

Removed:

```
public KeyStoreException ();
 	public KeyStoreException (string msg);
 	public KeyStoreException (string message, Java.Lang.Throwable cause);
```

Added:

```
public KeyStoreException (string message, Java.Lang.Throwable cause);
 	public KeyStoreException (string msg);
 	public KeyStoreException ();
```

 <a name="Type_Changed:_Java.Security.NoSuchAlgorithmException" class="injected"></a>


<h3 id='Java.Security.NoSuchAlgorithmException'>Type Changed: Java.Security.NoSuchAlgorithmException</h3>

Removed:

```
public NoSuchAlgorithmException ();
 	public NoSuchAlgorithmException (string msg);
 	public NoSuchAlgorithmException (string message, Java.Lang.Throwable cause);
```

Added:

```
public NoSuchAlgorithmException (string message, Java.Lang.Throwable cause);
 	public NoSuchAlgorithmException (string msg);
 	public NoSuchAlgorithmException ();
```

 <a name="Type_Changed:_Java.Security.ProviderException" class="injected"></a>


<h3 id='Java.Security.ProviderException'>Type Changed: Java.Security.ProviderException</h3>

Removed:

```
public ProviderException ();
 	public ProviderException (string msg);
 	public ProviderException (string message, Java.Lang.Throwable cause);
```

Added:

```
public ProviderException (string message, Java.Lang.Throwable cause);
 	public ProviderException (string msg);
 	public ProviderException ();
```

 <a name="Type_Changed:_Java.Security.SecureRandom" class="injected"></a>


<h3 id='Java.Security.SecureRandom'>Type Changed: Java.Security.SecureRandom</h3>

Removed:

```
public SecureRandom ();
 	public SecureRandom (byte [] seed);
 	protected override int Next (int numBits);
```

Added:

```
public SecureRandom (byte [] seed);
 	public SecureRandom ();
 	protected int Next (int numBits);
```

 <a name="Type_Changed:_Java.Security.SignatureException" class="injected"></a>


<h3 id='Java.Security.SignatureException'>Type Changed: Java.Security.SignatureException</h3>

Removed:

```
public SignatureException ();
 	public SignatureException (string msg);
 	public SignatureException (string message, Java.Lang.Throwable cause);
```

Added:

```
public SignatureException (string message, Java.Lang.Throwable cause);
 	public SignatureException (string msg);
 	public SignatureException ();
```

 <a name="Type_Changed:_Java.Security.Signer" class="injected"></a>


<h3 id='Java.Security.Signer'>Type Changed: Java.Security.Signer</h3>

Removed:

```
protected Signer ();
 	public Signer (string name);
```

Added:

```
public Signer (string name);
 	protected Signer ();
```

 <a name="Namespace:_Java.Security.Cert" class="injected"></a>


<h2 id='Java.Security.Cert'>Namespace: Java.Security.Cert</h2>

 <a name="Type_Changed:_Java.Security.Cert.CRLException" class="injected"></a>


<h3 id='Java.Security.Cert.CRLException'>Type Changed: Java.Security.Cert.CRLException</h3>

Removed:

```
public CRLException ();
 	public CRLException (string msg);
 	public CRLException (string message, Java.Lang.Throwable cause);
```

Added:

```
public CRLException (string message, Java.Lang.Throwable cause);
 	public CRLException (string msg);
 	public CRLException ();
```

 <a name="Type_Changed:_Java.Security.Cert.CertPathBuilderException" class="injected"></a>


<h3 id='Java.Security.Cert.CertPathBuilderException'>Type Changed: Java.Security.Cert.CertPathBuilderException</h3>

Removed:

```
public CertPathBuilderException ();
 	public CertPathBuilderException (string msg);
 	public CertPathBuilderException (Java.Lang.Throwable cause);
```

Added:

```
public CertPathBuilderException (Java.Lang.Throwable cause);
 	public CertPathBuilderException (string msg);
 	public CertPathBuilderException ();
```

 <a name="Type_Changed:_Java.Security.Cert.CertPathValidatorException" class="injected"></a>


<h3 id='Java.Security.Cert.CertPathValidatorException'>Type Changed: Java.Security.Cert.CertPathValidatorException</h3>

Removed:

```
public CertPathValidatorException (string msg, Java.Lang.Throwable cause);
 	public CertPathValidatorException (string msg, Java.Lang.Throwable cause, CertPath certPath, int index);
```

Added:

```
public CertPathValidatorException (string msg, Java.Lang.Throwable cause, CertPath certPath, int index);
 	public CertPathValidatorException (string msg, Java.Lang.Throwable cause);
```

 <a name="Type_Changed:_Java.Security.Cert.CertStoreException" class="injected"></a>


<h3 id='Java.Security.Cert.CertStoreException'>Type Changed: Java.Security.Cert.CertStoreException</h3>

Removed:

```
public CertStoreException ();
 	public CertStoreException (string msg);
 	public CertStoreException (Java.Lang.Throwable cause);
```

Added:

```
public CertStoreException (Java.Lang.Throwable cause);
 	public CertStoreException (string msg);
 	public CertStoreException ();
```

 <a name="Type_Changed:_Java.Security.Cert.CertificateEncodingException" class="injected"></a>


<h3 id='Java.Security.Cert.CertificateEncodingException'>Type Changed: Java.Security.Cert.CertificateEncodingException</h3>

Removed:

```
public CertificateEncodingException ();
 	public CertificateEncodingException (string msg);
 	public CertificateEncodingException (string message, Java.Lang.Throwable cause);
```

Added:

```
public CertificateEncodingException (string message, Java.Lang.Throwable cause);
 	public CertificateEncodingException (string msg);
 	public CertificateEncodingException ();
```

 <a name="Type_Changed:_Java.Security.Cert.CertificateException" class="injected"></a>


<h3 id='Java.Security.Cert.CertificateException'>Type Changed: Java.Security.Cert.CertificateException</h3>

Removed:

```
public CertificateException ();
 	public CertificateException (string msg);
 	public CertificateException (string message, Java.Lang.Throwable cause);
```

Added:

```
public CertificateException (string message, Java.Lang.Throwable cause);
 	public CertificateException (string msg);
 	public CertificateException ();
```

 <a name="Type_Changed:_Java.Security.Cert.CertificateParsingException" class="injected"></a>


<h3 id='Java.Security.Cert.CertificateParsingException'>Type Changed: Java.Security.Cert.CertificateParsingException</h3>

Removed:

```
public CertificateParsingException ();
 	public CertificateParsingException (string msg);
 	public CertificateParsingException (string message, Java.Lang.Throwable cause);
```

Added:

```
public CertificateParsingException (string message, Java.Lang.Throwable cause);
 	public CertificateParsingException (string msg);
 	public CertificateParsingException ();
```

 <a name="Type_Changed:_Java.Security.Cert.LDAPCertStoreParameters" class="injected"></a>


<h3 id='Java.Security.Cert.LDAPCertStoreParameters'>Type Changed: Java.Security.Cert.LDAPCertStoreParameters</h3>

Removed:

```
public LDAPCertStoreParameters (string serverName, int port);
 	public LDAPCertStoreParameters (string serverName);
```

Added:

```
public LDAPCertStoreParameters (string serverName);
 	public LDAPCertStoreParameters (string serverName, int port);
```

 <a name="Type_Changed:_Java.Security.Cert.TrustAnchor" class="injected"></a>


<h3 id='Java.Security.Cert.TrustAnchor'>Type Changed: Java.Security.Cert.TrustAnchor</h3>

Removed:

```
public TrustAnchor (X509Certificate trustedCert, byte [] nameConstraints);
 	public TrustAnchor (Javax.Security.Auth.X500.X500Principal caPrincipal, Java.Security.IPublicKey caPublicKey, byte [] nameConstraints);
```

Added:

```
public TrustAnchor (Javax.Security.Auth.X500.X500Principal caPrincipal, Java.Security.IPublicKey caPublicKey, byte [] nameConstraints);
 	public TrustAnchor (X509Certificate trustedCert, byte [] nameConstraints);
```

 <a name="Namespace:_Java.Security.Spec" class="injected"></a>


<h2 id='Java.Security.Spec'>Namespace: Java.Security.Spec</h2>

 <a name="Type_Changed:_Java.Security.Spec.ECFieldF2m" class="injected"></a>


<h3 id='Java.Security.Spec.ECFieldF2m'>Type Changed: Java.Security.Spec.ECFieldF2m</h3>

Removed:

```
public ECFieldF2m (int m);
 	public ECFieldF2m (int m, Java.Math.BigInteger rp);
```

Added:

```
public ECFieldF2m (int m, Java.Math.BigInteger rp);
 	public ECFieldF2m (int m);
```

 <a name="Type_Changed:_Java.Security.Spec.EllipticCurve" class="injected"></a>


<h3 id='Java.Security.Spec.EllipticCurve'>Type Changed: Java.Security.Spec.EllipticCurve</h3>

Removed:

```
public EllipticCurve (IECField field, Java.Math.BigInteger a, Java.Math.BigInteger b);
```

Added:

```
public EllipticCurve (IECField field, Java.Math.BigInteger a, Java.Math.BigInteger b);
```

 <a name="Type_Changed:_Java.Security.Spec.InvalidKeySpecException" class="injected"></a>


<h3 id='Java.Security.Spec.InvalidKeySpecException'>Type Changed: Java.Security.Spec.InvalidKeySpecException</h3>

Removed:

```
public InvalidKeySpecException ();
 	public InvalidKeySpecException (string msg);
 	public InvalidKeySpecException (string message, Java.Lang.Throwable cause);
```

Added:

```
public InvalidKeySpecException (string message, Java.Lang.Throwable cause);
 	public InvalidKeySpecException (string msg);
 	public InvalidKeySpecException ();
```

 <a name="Type_Changed:_Java.Security.Spec.PSSParameterSpec" class="injected"></a>


<h3 id='Java.Security.Spec.PSSParameterSpec'>Type Changed: Java.Security.Spec.PSSParameterSpec</h3>

Removed:

```
public PSSParameterSpec (string mdName, string mgfName, IAlgorithmParameterSpec mgfSpec, int saltLen, int trailerField);
```

Added:

```
public PSSParameterSpec (string mdName, string mgfName, IAlgorithmParameterSpec mgfSpec, int saltLen, int trailerField);
```

 <a name="Namespace:_Java.Util" class="injected"></a>


<h2 id='Java.Util'>Namespace: Java.Util</h2>

 <a name="Type_Changed:_Java.Util.BitSet" class="injected"></a>


<h3 id='Java.Util.BitSet'>Type Changed: Java.Util.BitSet</h3>

Removed:

```
public BitSet ();
```

Added:

```
public BitSet ();
 	public static BitSet ValueOf (byte [] p0);
 	public static BitSet ValueOf (Java.Nio.ByteBuffer p0);
 	public static BitSet ValueOf (long [] p0);
 	public static BitSet ValueOf (Java.Nio.LongBuffer p0);
 	public virtual int PreviousClearBit (int p0);
 	public virtual int PreviousSetBit (int p0);
 	public virtual byte [] ToByteArray ();
 	public virtual long [] ToLongArray ();
```

 <a name="Type_Changed:_Java.Util.Calendar" class="injected"></a>


<h3 id='Java.Util.Calendar'>Type Changed: Java.Util.Calendar</h3>

Added:

```
public virtual void SetWeekDate (int p0, int p1, int p2);
 	public virtual bool IsWeekDateSupported {
 		get;
 	}
 	public virtual int WeeksInWeekYear {
 		get;
 	}
 	public virtual int WeekYear {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Util.ConcurrentModificationException" class="injected"></a>


<h3 id='Java.Util.ConcurrentModificationException'>Type Changed: Java.Util.ConcurrentModificationException</h3>

Removed:

```
public ConcurrentModificationException ();
```

Added:

```
public ConcurrentModificationException (string p0, Java.Lang.Throwable p1);
 	public ConcurrentModificationException (Java.Lang.Throwable p0);
 	public ConcurrentModificationException ();
```

 <a name="Type_Changed:_Java.Util.Currency" class="injected"></a>


<h3 id='Java.Util.Currency'>Type Changed: Java.Util.Currency</h3>

Added:

```
public string GetDisplayName (Locale p0);
 	public static System.Collections.Generic.ICollection<Currency> AvailableCurrencies {
 		get;
 	}
 	public string DisplayName {
 		get;
 	}
 	public int NumericCode {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Util.Date" class="injected"></a>


<h3 id='Java.Util.Date'>Type Changed: Java.Util.Date</h3>

Removed:

```
public Date (int year, int month, int day, int hour, int minute);
 	public Date (int year, int month, int day, int hour, int minute, int second);
 	public Date (string string);
```

Added:

```
public Date (string string);
 	public Date (int year, int month, int day, int hour, int minute, int second);
 	public Date (int year, int month, int day, int hour, int minute);
```

 <a name="Type_Changed:_Java.Util.EventListenerProxy" class="injected"></a>


<h3 id='Java.Util.EventListenerProxy'>Type Changed: Java.Util.EventListenerProxy</h3>

Removed:

```
public EventListenerProxy (IEventListener listener);
 	public virtual IEventListener Listener {
```

Added:

```
public EventListenerProxy (Java.Lang.Object p0);
 	public virtual Java.Lang.Object Listener {
```

 <a name="Type_Changed:_Java.Util.Formatter" class="injected"></a>


<h3 id='Java.Util.Formatter'>Type Changed: Java.Util.Formatter</h3>

Removed:

```
public sealed class Formatter : Java.Lang.Object, Java.IO.ICloseable, Java.IO.IFlushable {
 	public Formatter ();
 	public Formatter (Java.Lang.IAppendable a);
 	public Formatter (Locale l);
 	public Formatter (Java.Lang.IAppendable a, Locale l);
 	public Formatter (string fileName);
 	public Formatter (string fileName, string csn);
 	public Formatter (string fileName, string csn, Locale l);
 	public Formatter (Java.IO.File file);
 	public Formatter (Java.IO.File file, string csn, Locale l);
 	public Formatter (Java.IO.PrintStream ps);
 	public Formatter (System.IO.Stream os);
```

Added:

```
public sealed class Formatter : Java.Lang.Object, Java.IO.IFlushable {
 	public Formatter (Java.IO.File file);
 	public Formatter (string fileName, string csn, Locale l);
 	public Formatter (string fileName, string csn);
 	public Formatter (string fileName);
 	public Formatter (System.IO.Stream os);
 	public Formatter (Java.IO.PrintStream ps);
 	public Formatter (Java.IO.File file, string csn, Locale l);
 	public Formatter ();
 	public Formatter (Java.Lang.IAppendable a, Locale l);
 	public Formatter (Locale l);
 	public Formatter (Java.Lang.IAppendable a);
```

 <a name="Type_Changed:_Java.Util.GregorianCalendar" class="injected"></a>


<h3 id='Java.Util.GregorianCalendar'>Type Changed: Java.Util.GregorianCalendar</h3>

Removed:

```
public GregorianCalendar (int year, int month, int day);
 	public GregorianCalendar (int year, int month, int day, int hour, int minute);
 	public GregorianCalendar (int year, int month, int day, int hour, int minute, int second);
```

Added:

```
public GregorianCalendar (int year, int month, int day);
 	public GregorianCalendar (int year, int month, int day, int hour, int minute);
 	public GregorianCalendar (int year, int month, int day, int hour, int minute, int second);
 	public override bool IsWeekDateSupported {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Util.Hashtable" class="injected"></a>


<h3 id='Java.Util.Hashtable'>Type Changed: Java.Util.Hashtable</h3>

Removed:

```
public Hashtable (int capacity, float loadFactor);
 	public Hashtable (int capacity);
```

Added:

```
public Hashtable (int capacity);
 	public Hashtable (int capacity, float loadFactor);
```

 <a name="Type_Changed:_Java.Util.ListResourceBundle" class="injected"></a>


<h3 id='Java.Util.ListResourceBundle'>Type Changed: Java.Util.ListResourceBundle</h3>

Removed:

```
public override Java.Lang.Object HandleGetObject (string key);
```

Added:

```
public Java.Lang.Object HandleGetObject (string key);
```

 <a name="Type_Changed:_Java.Util.Locale" class="injected"></a>


<h3 id='Java.Util.Locale'>Type Changed: Java.Util.Locale</h3>

Removed:

```
public Locale (string language, string country, string variant);
 	public Locale (string language, string country);
 	public override string ToString ();
```

Added:

```
public Locale (string language, string country);
 	public Locale (string language, string country, string variant);
 	public static Locale ForLanguageTag (string p0);
 	public string GetDisplayScript (Locale p0);
 	public string GetExtension (char p0);
 	public string GetUnicodeLocaleType (string p0);
 	public string ToLanguageTag ();
 	public string ToString ();
 	public static char PrivateUseExtension {
 		get;
 		set;
 	}
 	public static char UnicodeLocaleExtension {
 		get;
 		set;
 	}
 	public string DisplayScript {
 		get;
 	}
 	public System.Collections.Generic.ICollection<Java.Lang.Character> ExtensionKeys {
 		get;
 	}
 	public string Script {
 		get;
 	}
 	public System.Collections.Generic.ICollection<string> UnicodeLocaleAttributes {
 		get;
 	}
 	public System.Collections.Generic.ICollection<string> UnicodeLocaleKeys {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Util.Scanner" class="injected"></a>


<h3 id='Java.Util.Scanner'>Type Changed: Java.Util.Scanner</h3>

Removed:

```
public Scanner (Java.Lang.IReadable src);
 	public Scanner (Java.IO.File src);
 	public Scanner (Java.Nio.Channels.IReadableByteChannel src);
 	public Scanner (Java.Nio.Channels.IReadableByteChannel src, string charsetName);
```

Added:

```
public Scanner (Java.Lang.IReadable src);
 	public Scanner (Java.IO.File src);
```

 <a name="Type_Changed:_Java.Util.SimpleTimeZone" class="injected"></a>


<h3 id='Java.Util.SimpleTimeZone'>Type Changed: Java.Util.SimpleTimeZone</h3>

Removed:

```
public SimpleTimeZone (int offset, string name);
 	public SimpleTimeZone (int offset, string name, int startMonth, int startDay, int startDayOfWeek, int startTime, int endMonth, int endDay, int endDayOfWeek, int endTime);
 	public SimpleTimeZone (int offset, string name, int startMonth, int startDay, int startDayOfWeek, int startTime, int endMonth, int endDay, int endDayOfWeek, int endTime, int daylightSavings);
```

Added:

```
public SimpleTimeZone (int offset, string name, int startMonth, int startDay, int startDayOfWeek, int startTime, int endMonth, int endDay, int endDayOfWeek, int endTime, int daylightSavings);
 	public SimpleTimeZone (int offset, string name, int startMonth, int startDay, int startDayOfWeek, int startTime, int endMonth, int endDay, int endDayOfWeek, int endTime);
 	public SimpleTimeZone (int offset, string name);
```

 <a name="Type_Changed:_Java.Util.StringTokenizer" class="injected"></a>


<h3 id='Java.Util.StringTokenizer'>Type Changed: Java.Util.StringTokenizer</h3>

Removed:

```
public StringTokenizer (string string, string delimiters, bool returnDelimiters);
```

Added:

```
public StringTokenizer (string string, string delimiters, bool returnDelimiters);
```

 <a name="Type_Changed:_Java.Util.TimeZone" class="injected"></a>


<h3 id='Java.Util.TimeZone'>Type Changed: Java.Util.TimeZone</h3>

Added:

```
public virtual bool ObservesDaylightTime ();
```

 <a name="Type_Changed:_Java.Util.Timer" class="injected"></a>


<h3 id='Java.Util.Timer'>Type Changed: Java.Util.Timer</h3>

Removed:

```
public Timer ();
 	public Timer (string name, bool isDaemon);
```

Added:

```
public Timer (string name, bool isDaemon);
 	public Timer ();
```

 <a name="Namespace:_Java.Util.Regex" class="injected"></a>


<h2 id='Java.Util.Regex'>Namespace: Java.Util.Regex</h2>

 <a name="Type_Changed:_Java.Util.Regex.Matcher" class="injected"></a>


<h3 id='Java.Util.Regex.Matcher'>Type Changed: Java.Util.Regex.Matcher</h3>

Added:

```
public string Group (string p0);
```

 <a name="Type_Changed:_Java.Util.Regex.Pattern" class="injected"></a>


<h3 id='Java.Util.Regex.Pattern'>Type Changed: Java.Util.Regex.Pattern</h3>

Added:

```
public static int UnicodeCharacterClass {
 		get;
 		set;
 	}
```

 <a name="Namespace:_Java.Util.Zip" class="injected"></a>


<h2 id='Java.Util.Zip'>Namespace: Java.Util.Zip</h2>

 <a name="Type_Changed:_Java.Util.Zip.Deflater" class="injected"></a>


<h3 id='Java.Util.Zip.Deflater'>Type Changed: Java.Util.Zip.Deflater</h3>

Removed:

```
public Deflater (int level, bool noHeader);
 	public Deflater (int level);
```

Added:

```
public Deflater (int level);
 	public Deflater (int level, bool noHeader);
 	public virtual int Deflate (byte [] p0, int p1, int p2, int p3);
 	public static int FullFlush {
 		get;
 		set;
 	}
 	public static int NoFlush {
 		get;
 		set;
 	}
 	public static int SyncFlush {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_Java.Util.Zip.DeflaterOutputStream" class="injected"></a>


<h3 id='Java.Util.Zip.DeflaterOutputStream'>Type Changed: Java.Util.Zip.DeflaterOutputStream</h3>

Removed:

```
public DeflaterOutputStream (System.IO.Stream os, Deflater def, int bsize);
 	public DeflaterOutputStream (System.IO.Stream os, Deflater def);
```

Added:

```
public DeflaterOutputStream (System.IO.Stream p0, bool p1);
 	public DeflaterOutputStream (System.IO.Stream os, Deflater def);
 	public DeflaterOutputStream (System.IO.Stream p0, Deflater p1, int p2, bool p3);
 	public DeflaterOutputStream (System.IO.Stream os, Deflater def, int bsize);
 	public DeflaterOutputStream (System.IO.Stream p0, Deflater p1, bool p2);
```

 <a name="Type_Changed:_Java.Util.Zip.GZIPInputStream" class="injected"></a>


<h3 id='Java.Util.Zip.GZIPInputStream'>Type Changed: Java.Util.Zip.GZIPInputStream</h3>

Removed:

```
public GZIPInputStream (System.IO.Stream is, int size);
```

Added:

```
public GZIPInputStream (System.IO.Stream is, int size);
```

 <a name="Type_Changed:_Java.Util.Zip.GZIPOutputStream" class="injected"></a>


<h3 id='Java.Util.Zip.GZIPOutputStream'>Type Changed: Java.Util.Zip.GZIPOutputStream</h3>

Removed:

```
public GZIPOutputStream (System.IO.Stream os, int size);
```

Added:

```
public GZIPOutputStream (System.IO.Stream p0, bool p1);
 	public GZIPOutputStream (System.IO.Stream p0, int p1, bool p2);
 	public GZIPOutputStream (System.IO.Stream os, int size);
```

 <a name="Type_Changed:_Java.Util.Zip.InflaterInputStream" class="injected"></a>


<h3 id='Java.Util.Zip.InflaterInputStream'>Type Changed: Java.Util.Zip.InflaterInputStream</h3>

Removed:

```
public InflaterInputStream (System.IO.Stream is, Inflater inf, int bsize);
```

Added:

```
public InflaterInputStream (System.IO.Stream is, Inflater inf, int bsize);
```

 <a name="Type_Changed:_Java.Util.Zip.ZipEntry" class="injected"></a>


<h3 id='Java.Util.Zip.ZipEntry'>Type Changed: Java.Util.Zip.ZipEntry</h3>

Removed:

```
public ZipEntry (string name);
```

Added:

```
public ZipEntry (string name);
```

 <a name="Type_Changed:_Java.Util.Zip.ZipFile" class="injected"></a>


<h3 id='Java.Util.Zip.ZipFile'>Type Changed: Java.Util.Zip.ZipFile</h3>

Removed:

```
public ZipFile (string name);
 	public ZipFile (Java.IO.File file, int mode);
```

Added:

```
public ZipFile (string p0, Java.Nio.Charset.Charset p1);
 	public ZipFile (Java.IO.File p0, Java.Nio.Charset.Charset p1);
 	public ZipFile (Java.IO.File file, int mode);
 	public ZipFile (string name);
 	public ZipFile (Java.IO.File p0, int p1, Java.Nio.Charset.Charset p2);
 	public virtual string Comment {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Util.Zip.ZipInputStream" class="injected"></a>


<h3 id='Java.Util.Zip.ZipInputStream'>Type Changed: Java.Util.Zip.ZipInputStream</h3>

Added:

```
public ZipInputStream (System.IO.Stream p0, Java.Nio.Charset.Charset p1);
```

 <a name="Type_Changed:_Java.Util.Zip.ZipOutputStream" class="injected"></a>


<h3 id='Java.Util.Zip.ZipOutputStream'>Type Changed: Java.Util.Zip.ZipOutputStream</h3>

Added:

```
public ZipOutputStream (System.IO.Stream p0, Java.Nio.Charset.Charset p1);
```

 <a name="Namespace:_Javax.Crypto" class="injected"></a>


<h2 id='Javax.Crypto'>Namespace: Javax.Crypto</h2>

 <a name="Type_Changed:_Javax.Crypto.Cipher" class="injected"></a>


<h3 id='Javax.Crypto.Cipher'>Type Changed: Javax.Crypto.Cipher</h3>

Added:

```
public void UpdateAAD (byte [] p0);
 	public void UpdateAAD (byte [] p0, int p1, int p2);
 	public void UpdateAAD (Java.Nio.ByteBuffer p0);
```

 <a name="Type_Changed:_Javax.Crypto.CipherSpi" class="injected"></a>


<h3 id='Javax.Crypto.CipherSpi'>Type Changed: Javax.Crypto.CipherSpi</h3>

Added:

```
protected virtual void EngineUpdateAAD (byte [] p0, int p1, int p2);
 	protected virtual void EngineUpdateAAD (Java.Nio.ByteBuffer p0);
```

 <a name="Type_Changed:_Javax.Crypto.EncryptedPrivateKeyInfo" class="injected"></a>


<h3 id='Javax.Crypto.EncryptedPrivateKeyInfo'>Type Changed: Javax.Crypto.EncryptedPrivateKeyInfo</h3>

Removed:

```
public EncryptedPrivateKeyInfo (byte [] encoded);
 	public EncryptedPrivateKeyInfo (string encrAlgName, byte [] encryptedData);
```

Added:

```
public EncryptedPrivateKeyInfo (string encrAlgName, byte [] encryptedData);
 	public EncryptedPrivateKeyInfo (byte [] encoded);
```

 <a name="Namespace:_Javax.Crypto.Spec" class="injected"></a>


<h2 id='Javax.Crypto.Spec'>Namespace: Javax.Crypto.Spec</h2>

 <a name="Type_Changed:_Javax.Crypto.Spec.PBEKeySpec" class="injected"></a>


<h3 id='Javax.Crypto.Spec.PBEKeySpec'>Type Changed: Javax.Crypto.Spec.PBEKeySpec</h3>

Removed:

```
public PBEKeySpec (char [] password);
 	public PBEKeySpec (char [] password, byte [] salt, int iterationCount, int keyLength);
```

Added:

```
public PBEKeySpec (char [] password, byte [] salt, int iterationCount, int keyLength);
 	public PBEKeySpec (char [] password);
```

 <a name="Type_Changed:_Javax.Crypto.Spec.RC2ParameterSpec" class="injected"></a>


<h3 id='Javax.Crypto.Spec.RC2ParameterSpec'>Type Changed: Javax.Crypto.Spec.RC2ParameterSpec</h3>

Removed:

```
public RC2ParameterSpec (int effectiveKeyBits);
 	public RC2ParameterSpec (int effectiveKeyBits, byte [] iv);
```

Added:

```
public RC2ParameterSpec (int effectiveKeyBits, byte [] iv);
 	public RC2ParameterSpec (int effectiveKeyBits);
```

 <a name="Type_Changed:_Javax.Crypto.Spec.RC5ParameterSpec" class="injected"></a>


<h3 id='Javax.Crypto.Spec.RC5ParameterSpec'>Type Changed: Javax.Crypto.Spec.RC5ParameterSpec</h3>

Removed:

```
public RC5ParameterSpec (int version, int rounds, int wordSize);
 	public RC5ParameterSpec (int version, int rounds, int wordSize, byte [] iv);
```

Added:

```
public RC5ParameterSpec (int version, int rounds, int wordSize, byte [] iv);
 	public RC5ParameterSpec (int version, int rounds, int wordSize);
```

 <a name="Namespace:_Javax.Microedition.Khronos.Opengles" class="injected"></a>


<h2 id='Javax.Microedition.Khronos.Opengles'>Namespace: Javax.Microedition.Khronos.Opengles</h2>

 <a name="Type_Changed:_Javax.Microedition.Khronos.Opengles.GL10" class="injected"></a>


<h3 id='Javax.Microedition.Khronos.Opengles.GL10'>Type Changed: Javax.Microedition.Khronos.Opengles.GL10</h3>

Added:

```
public const int GlCullFaceCapability = 2884;
```

 <a name="Type_Changed:_Javax.Microedition.Khronos.Opengles.GL11" class="injected"></a>


<h3 id='Javax.Microedition.Khronos.Opengles.GL11'>Type Changed: Javax.Microedition.Khronos.Opengles.GL11</h3>

Added:

```
public const int GlCullFaceCapability = 2884;
```

 <a name="Namespace:_Javax.Net.Ssl" class="injected"></a>


<h2 id='Javax.Net.Ssl'>Namespace: Javax.Net.Ssl</h2>

 <a name="Type_Changed:_Javax.Net.Ssl.SSLEngine" class="injected"></a>


<h3 id='Javax.Net.Ssl.SSLEngine'>Type Changed: Javax.Net.Ssl.SSLEngine</h3>

Added:

```
public virtual ISSLSession HandshakeSession {
 		get;
 	}
```

 <a name="Type_Changed:_Javax.Net.Ssl.SSLServerSocket" class="injected"></a>


<h3 id='Javax.Net.Ssl.SSLServerSocket'>Type Changed: Javax.Net.Ssl.SSLServerSocket</h3>

Removed:

```
protected SSLServerSocket ();
 	protected SSLServerSocket (int port);
 	protected SSLServerSocket (int port, int backlog);
```

Added:

```
protected SSLServerSocket (int port, int backlog);
 	protected SSLServerSocket (int port);
 	protected SSLServerSocket ();
```

 <a name="Type_Changed:_Javax.Net.Ssl.SSLSocket" class="injected"></a>


<h3 id='Javax.Net.Ssl.SSLSocket'>Type Changed: Javax.Net.Ssl.SSLSocket</h3>

Removed:

```
protected SSLSocket ();
 	protected SSLSocket (string host, int port);
 	protected SSLSocket (Java.Net.InetAddress address, int port);
 	protected SSLSocket (string host, int port, Java.Net.InetAddress clientAddress, int clientPort);
```

Added:

```
protected SSLSocket (string host, int port, Java.Net.InetAddress clientAddress, int clientPort);
 	protected SSLSocket (Java.Net.InetAddress address, int port);
 	protected SSLSocket (string host, int port);
 	protected SSLSocket ();
 	public virtual ISSLSession HandshakeSession {
 		get;
 	}
```

 <a name="Namespace:_Javax.Security.Auth.X500" class="injected"></a>


<h2 id='Javax.Security.Auth.X500'>Namespace: Javax.Security.Auth.X500</h2>

 <a name="Type_Changed:_Javax.Security.Auth.X500.X500Principal" class="injected"></a>


<h3 id='Javax.Security.Auth.X500.X500Principal'>Type Changed: Javax.Security.Auth.X500.X500Principal</h3>

Removed:

```
public X500Principal (string name);
 	public X500Principal (string p0, System.Collections.Generic.IDictionary<string,string> p1);
 	public X500Principal (byte [] name);
```

Added:

```
public X500Principal (byte [] name);
 	public X500Principal (string p0, System.Collections.Generic.IDictionary<string,string> p1);
 	public X500Principal (string name);
```
