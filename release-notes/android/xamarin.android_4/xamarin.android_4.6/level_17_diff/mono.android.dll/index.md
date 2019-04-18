---
id: A81B4E3E-F923-4B58-957E-798BB4037013
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

 <a name="Namespace:_Android.Animation" class="injected"></a>


<h2 id='Android.Animation'>Namespace: Android.Animation</h2>

 <a name="Type_Changed:_Android.Animation.ObjectAnimator" class="injected"></a>


<h3 id='Android.Animation.ObjectAnimator'>Type Changed: Android.Animation.ObjectAnimator</h3>

Added:

```
public static ObjectAnimator OfObject (Java.Lang.Object target, Android.Util.Property property, ITypeEvaluator evaluator, params Java.Lang.Object[] values);
```

 <a name="Type_Changed:_Android.Animation.PropertyValuesHolder" class="injected"></a>


<h3 id='Android.Animation.PropertyValuesHolder'>Type Changed: Android.Animation.PropertyValuesHolder</h3>

Added:

```
public static PropertyValuesHolder OfObject (Android.Util.Property property, ITypeEvaluator evaluator, params Java.Lang.Object[] values);
```

 <a name="Namespace:_Android.App" class="injected"></a>


<h2 id='Android.App'>Namespace: Android.App</h2>

 <a name="Type_Changed:_Android.App.Activity" class="injected"></a>


<h3 id='Android.App.Activity'>Type Changed: Android.App.Activity</h3>

Removed:

```
public class Activity : Android.Views.ContextThemeWrapper, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, LayoutInflater.Android.Views.IFactory, LayoutInflater.Android.Views.IFactory2, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Activity : Android.Views.ContextThemeWrapper, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, LayoutInflater.Android.Views.IFactory, LayoutInflater.Android.Views.IFactory2, View.Android.Views.IOnCreateContextMenuListener {
```

 <a name="Type_Changed:_Android.App.ActivityAttribute" class="injected"></a>


<h3 id='Android.App.ActivityAttribute'>Type Changed: Android.App.ActivityAttribute</h3>

Added:

```
public Android.Views.LayoutDirection LayoutDirection {
 		get;
 		set;
 	}
 	public Android.Content.PM.UiOptions UiOptions {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_Android.App.ApplicationAttribute" class="injected"></a>


<h3 id='Android.App.ApplicationAttribute'>Type Changed: Android.App.ApplicationAttribute</h3>

Added:

```
public bool LargeHeap {
 		get;
 		set;
 	}
 	public bool SupportsRtl {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_Android.App.Dialog" class="injected"></a>


<h3 id='Android.App.Dialog'>Type Changed: Android.App.Dialog</h3>

Removed:

```
public class Dialog : Java.Lang.Object, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Dialog : Java.Lang.Object, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
 	public T FindViewById<T> (int id) where T : Android.Views.View;
```

 <a name="Type_Changed:_Android.App.Fragment" class="injected"></a>


<h3 id='Android.App.Fragment'>Type Changed: Android.App.Fragment</h3>

Removed:

```
public override bool Equals (Java.Lang.Object o);
 	public override int GetHashCode ();
```

Added:

```
public bool Equals (Java.Lang.Object o);
 	public int GetHashCode ();
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
	public bool Required {
		get;
		set;
	}
}
```

 <a name="Namespace:_Android.Graphics.Drawables" class="injected"></a>


<h2 id='Android.Graphics.Drawables'>Namespace: Android.Graphics.Drawables</h2>

 <a name="Type_Changed:_Android.Graphics.Drawables.BitmapDrawable" class="injected"></a>


<h3 id='Android.Graphics.Drawables.BitmapDrawable'>Type Changed: Android.Graphics.Drawables.BitmapDrawable</h3>

Removed:

```
public override ConstantState GetConstantState ();
```

Added:

```
public ConstantState GetConstantState ();
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

 <a name="Namespace:_Android.Service.Dreams" class="injected"></a>


<h2 id='Android.Service.Dreams'>Namespace: Android.Service.Dreams</h2>

 <a name="Type_Changed:_Android.Service.Dreams.DreamService" class="injected"></a>


<h3 id='Android.Service.Dreams.DreamService'>Type Changed: Android.Service.Dreams.DreamService</h3>

Removed:

```
public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

Added:

```
public Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

 <a name="Namespace:_Android.Service.Textservice" class="injected"></a>


<h2 id='Android.Service.Textservice'>Namespace: Android.Service.Textservice</h2>

 <a name="Type_Changed:_Android.Service.Textservice.SpellCheckerService" class="injected"></a>


<h3 id='Android.Service.Textservice.SpellCheckerService'>Type Changed: Android.Service.Textservice.SpellCheckerService</h3>

Removed:

```
public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

Added:

```
public Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

 <a name="Namespace:_Android.Service.Wallpaper" class="injected"></a>


<h2 id='Android.Service.Wallpaper'>Namespace: Android.Service.Wallpaper</h2>

 <a name="Type_Changed:_Android.Service.Wallpaper.WallpaperService" class="injected"></a>


<h3 id='Android.Service.Wallpaper.WallpaperService'>Type Changed: Android.Service.Wallpaper.WallpaperService</h3>

Removed:

```
public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

Added:

```
public Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

 <a name="Namespace:_Android.Speech" class="injected"></a>


<h2 id='Android.Speech'>Namespace: Android.Speech</h2>

 <a name="Type_Changed:_Android.Speech.RecognitionService" class="injected"></a>


<h3 id='Android.Speech.RecognitionService'>Type Changed: Android.Speech.RecognitionService</h3>

Removed:

```
public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

Added:

```
public Android.OS.IBinder OnBind (Android.Content.Intent intent);
```

 <a name="Namespace:_Android.Telephony" class="injected"></a>


<h2 id='Android.Telephony'>Namespace: Android.Telephony</h2>

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
public override Directions GetLineDirections (int line);
```

Added:

```
public Directions GetLineDirections (int line);
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
public override Directions GetLineDirections (int line);
```

Added:

```
public Directions GetLineDirections (int line);
```

 <a name="Namespace:_Android.Util" class="injected"></a>


<h2 id='Android.Util'>Namespace: Android.Util</h2>

 <a name="Type_Changed:_Android.Util.LruCache" class="injected"></a>


<h3 id='Android.Util.LruCache'>Type Changed: Android.Util.LruCache</h3>

Removed:

```
public override string ToString ();
```

Added:

```
public string ToString ();
```

 <a name="Namespace:_Android.Views" class="injected"></a>


<h2 id='Android.Views'>Namespace: Android.Views</h2>

 <a name="Type_Changed:_Android.Views.TextureView" class="injected"></a>


<h3 id='Android.Views.TextureView'>Type Changed: Android.Views.TextureView</h3>

Removed:

```
public override void Draw (Android.Graphics.Canvas canvas);
 	protected override void OnDraw (Android.Graphics.Canvas canvas);
```

Added:

```
public void Draw (Android.Graphics.Canvas canvas);
 	protected void OnDraw (Android.Graphics.Canvas canvas);
```

 <a name="Type_Changed:_Android.Views.View" class="injected"></a>


<h3 id='Android.Views.View'>Type Changed: Android.Views.View</h3>

Removed:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, ICallback, Drawable.Android.Graphics.Drawables.ICallback {
```

Added:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, Drawable.Android.Graphics.Drawables.ICallback, ICallback {
```

 <a name="Type_Changed:_Android.Views.ViewDebug" class="injected"></a>


<h3 id='Android.Views.ViewDebug'>Type Changed: Android.Views.ViewDebug</h3>

Added:

```
public abstract bool RetrieveReturn ();
 		public abstract string Category ();
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
public override void Layout (int l, int t, int r, int b);
```

Added:

```
public void Layout (int l, int t, int r, int b);
```

 <a name="Type_Changed:_Android.Views.Window" class="injected"></a>


<h3 id='Android.Views.Window'>Type Changed: Android.Views.Window</h3>

Added:

```
public T FindViewById<T> (int id) where T : View;
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

 <a name="Namespace:_Android.Widget" class="injected"></a>


<h2 id='Android.Widget'>Namespace: Android.Widget</h2>

 <a name="Type_Changed:_Android.Widget.TextClock" class="injected"></a>


<h3 id='Android.Widget.TextClock'>Type Changed: Android.Widget.TextClock</h3>

Removed:

```
public TextClock (Android.Content.Context context);
 	public TextClock (Android.Content.Context context, Android.Util.IAttributeSet attrs);
```

Added:

```
public TextClock (Android.Content.Context context, Android.Util.IAttributeSet attrs);
 	public TextClock (Android.Content.Context context);
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

 <a name="Namespace:_Java.Lang" class="injected"></a>


<h2 id='Java.Lang'>Namespace: Java.Lang</h2>

 <a name="Type_Changed:_Java.Lang.ClassNotFoundException" class="injected"></a>


<h3 id='Java.Lang.ClassNotFoundException'>Type Changed: Java.Lang.ClassNotFoundException</h3>

Added:

```
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

 <a name="Type_Changed:_Java.Lang.IllegalAccessException" class="injected"></a>


<h3 id='Java.Lang.IllegalAccessException'>Type Changed: Java.Lang.IllegalAccessException</h3>

Added:

```
public virtual Throwable Clause {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.InstantiationException" class="injected"></a>


<h3 id='Java.Lang.InstantiationException'>Type Changed: Java.Lang.InstantiationException</h3>

Added:

```
public virtual Throwable Clause {
 		get;
 	}
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

 <a name="Type_Changed:_Java.Lang.SuppressWarnings" class="injected"></a>


<h3 id='Java.Lang.SuppressWarnings'>Type Changed: Java.Lang.SuppressWarnings</h3>

Added:

```
public abstract string [] Value ();
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

 <a name="Namespace:_Java.Net" class="injected"></a>


<h2 id='Java.Net'>Namespace: Java.Net</h2>

 <a name="Type_Changed:_Java.Net.InetSocketAddress" class="injected"></a>


<h3 id='Java.Net.InetSocketAddress'>Type Changed: Java.Net.InetSocketAddress</h3>

Removed:

```
public override bool Equals (Java.Lang.Object socketAddr);
 	public override int GetHashCode ();
```

Added:

```
public bool Equals (Java.Lang.Object socketAddr);
 	public int GetHashCode ();
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

 <a name="Type_Changed:_Java.Nio.Channels.DatagramChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.DatagramChannel'>Type Changed: Java.Nio.Channels.DatagramChannel</h3>

Removed:

```
public override Operations ValidOps ();
```

Added:

```
public Operations ValidOps ();
```

 <a name="Type_Changed:_Java.Nio.Channels.FileChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.FileChannel'>Type Changed: Java.Nio.Channels.FileChannel</h3>

Removed:

```
public abstract class FileChannel : Java.Nio.Channels.Spi.AbstractInterruptibleChannel, IByteChannel, IGatheringByteChannel, IReadableByteChannel, IScatteringByteChannel, IWritableByteChannel {
```

Added:

```
public abstract class FileChannel : Java.Nio.Channels.Spi.AbstractInterruptibleChannel, IGatheringByteChannel, IReadableByteChannel, IScatteringByteChannel, IWritableByteChannel {
```

 <a name="Type_Changed:_Java.Nio.Channels.FileLock" class="injected"></a>


<h3 id='Java.Nio.Channels.FileLock'>Type Changed: Java.Nio.Channels.FileLock</h3>

Removed:

```
public override string ToString ();
```

Added:

```
public string ToString ();
```

 <a name="Type_Changed:_Java.Nio.Channels.Pipe" class="injected"></a>


<h3 id='Java.Nio.Channels.Pipe'>Type Changed: Java.Nio.Channels.Pipe</h3>

Removed:

```
public override Operations ValidOps ();
 		public override Operations ValidOps ();
```

Added:

```
public Operations ValidOps ();
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
public Operations ValidOps ();
```

 <a name="Type_Changed:_Java.Nio.Channels.SocketChannel" class="injected"></a>


<h3 id='Java.Nio.Channels.SocketChannel'>Type Changed: Java.Nio.Channels.SocketChannel</h3>

Removed:

```
public override Operations ValidOps ();
```

Added:

```
public Operations ValidOps ();
```

 <a name="Namespace:_Java.Nio.Channels.Spi" class="injected"></a>


<h2 id='Java.Nio.Channels.Spi'>Namespace: Java.Nio.Channels.Spi</h2>

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

 <a name="Type_Changed:_Java.Security.Identity" class="injected"></a>


<h3 id='Java.Security.Identity'>Type Changed: Java.Security.Identity</h3>

Removed:

```
public override bool Equals (Java.Lang.Object obj);
```

Added:

```
public bool Equals (Java.Lang.Object obj);
```

 <a name="Type_Changed:_Java.Security.SecureRandom" class="injected"></a>


<h3 id='Java.Security.SecureRandom'>Type Changed: Java.Security.SecureRandom</h3>

Removed:

```
protected override int Next (int numBits);
```

Added:

```
protected int Next (int numBits);
```

 <a name="Namespace:_Java.Util" class="injected"></a>


<h2 id='Java.Util'>Namespace: Java.Util</h2>

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
public override string ToString ();
```

Added:

```
public string ToString ();
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
