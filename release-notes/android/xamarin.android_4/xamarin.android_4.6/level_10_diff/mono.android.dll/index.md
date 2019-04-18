---
id: 2831BA08-07B0-448E-8B53-9C7A18377F5F
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

 <a name="Type_Changed:_Android.App.Dialog" class="injected"></a>


<h3 id='Android.App.Dialog'>Type Changed: Android.App.Dialog</h3>

Added:

```
public T FindViewById<T> (int id) where T : Android.Views.View;
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

 <a name="Namespace:_Android.Bluetooth" class="injected"></a>


<h2 id='Android.Bluetooth'>Namespace: Android.Bluetooth</h2>

 <a name="Type_Changed:_Android.Bluetooth.BluetoothServerSocket" class="injected"></a>


<h3 id='Android.Bluetooth.BluetoothServerSocket'>Type Changed: Android.Bluetooth.BluetoothServerSocket</h3>

Removed:

```
public sealed class BluetoothServerSocket : Java.Lang.Object, Java.IO.ICloseable {
```

Added:

```
public sealed class BluetoothServerSocket : Java.Lang.Object {
```

 <a name="Type_Changed:_Android.Bluetooth.BluetoothSocket" class="injected"></a>


<h3 id='Android.Bluetooth.BluetoothSocket'>Type Changed: Android.Bluetooth.BluetoothSocket</h3>

Removed:

```
public sealed class BluetoothSocket : Java.Lang.Object, Java.IO.ICloseable {
```

Added:

```
public sealed class BluetoothSocket : Java.Lang.Object {
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

 <a name="Namespace:_Android.Net.Sip" class="injected"></a>


<h2 id='Android.Net.Sip'>Namespace: Android.Net.Sip</h2>

 <a name="Type_Changed:_Android.Net.Sip.SipProfile" class="injected"></a>


<h3 id='Android.Net.Sip.SipProfile'>Type Changed: Android.Net.Sip.SipProfile</h3>

Removed:

```
public Builder (SipProfile profile);
 		public Builder (string uriString);
```

Added:

```
public Builder (string uriString);
 		public Builder (SipProfile profile);
```

 <a name="Namespace:_Android.Nfc.Tech" class="injected"></a>


<h2 id='Android.Nfc.Tech'>Namespace: Android.Nfc.Tech</h2>

 <a name="Type_Changed:_Android.Nfc.Tech.BasicTagTechnology" class="injected"></a>


<h3 id='Android.Nfc.Tech.BasicTagTechnology'>Type Changed: Android.Nfc.Tech.BasicTagTechnology</h3>

Removed:

```
public abstract class BasicTagTechnology : Java.Lang.Object, Java.IO.ICloseable, ITagTechnology {
```

Added:

```
public abstract class BasicTagTechnology : Java.Lang.Object {
```

 <a name="Type_Removed:_Android.Nfc.Tech.ITagTechnology" class="injected"></a>


<h3 id='Android.Nfc.Tech.ITagTechnology'>Type Removed: Android.Nfc.Tech.ITagTechnology</h3>

 <a name="Namespace:_Android.OS" class="injected"></a>


<h2 id='Android.OS'>Namespace: Android.OS</h2>

 <a name="Type_Changed:_Android.OS.DropBoxManager" class="injected"></a>


<h3 id='Android.OS.DropBoxManager'>Type Changed: Android.OS.DropBoxManager</h3>

Removed:

```
public class Entry : Java.Lang.Object, Java.IO.ICloseable, IParcelable {
```

Added:

```
public class Entry : Java.Lang.Object, IParcelable {
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

 <a name="Namespace:_Android.Views" class="injected"></a>


<h2 id='Android.Views'>Namespace: Android.Views</h2>

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

 <a name="Type_Changed:_Android.Widget.OverScroller" class="injected"></a>


<h3 id='Android.Widget.OverScroller'>Type Changed: Android.Widget.OverScroller</h3>

Removed:

```
public OverScroller (Android.Content.Context context);
 	public OverScroller (Android.Content.Context context, Android.Views.Animations.IInterpolator interpolator);
```

Added:

```
public OverScroller (Android.Content.Context context, Android.Views.Animations.IInterpolator interpolator);
 	public OverScroller (Android.Content.Context context);
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

 <a name="Type_Removed:_Java.IO.ICloseable" class="injected"></a>


<h3 id='Java.IO.ICloseable'>Type Removed: Java.IO.ICloseable</h3>

 <a name="Type_Removed:_Java.IO.IExternalizable" class="injected"></a>


<h3 id='Java.IO.IExternalizable'>Type Removed: Java.IO.IExternalizable</h3>

 <a name="Type_Removed:_Java.IO.IObjectInput" class="injected"></a>


<h3 id='Java.IO.IObjectInput'>Type Removed: Java.IO.IObjectInput</h3>

 <a name="Type_Removed:_Java.IO.IObjectOutput" class="injected"></a>


<h3 id='Java.IO.IObjectOutput'>Type Removed: Java.IO.IObjectOutput</h3>

 <a name="Namespace:_Java.IO" class="injected"></a>


<h2 id='Java.IO'>Namespace: Java.IO</h2>

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

Added:

```
public AssertionError (string p0, Throwable p1);
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

 <a name="Type_Changed:_Java.Lang.Error" class="injected"></a>


<h3 id='Java.Lang.Error'>Type Changed: Java.Lang.Error</h3>

Added:

```
protected Error (string p0, Throwable p1, bool p2, bool p3);
```

 <a name="Type_Changed:_Java.Lang.Exception" class="injected"></a>


<h3 id='Java.Lang.Exception'>Type Changed: Java.Lang.Exception</h3>

Added:

```
protected Exception (string p0, Throwable p1, bool p2, bool p3);
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

Added:

```
protected RuntimeException (string p0, Throwable p1, bool p2, bool p3);
```

 <a name="Type_Changed:_Java.Lang.Short" class="injected"></a>


<h3 id='Java.Lang.Short'>Type Changed: Java.Lang.Short</h3>

Added:

```
public static int Compare (short p0, short p1);
```

 <a name="Type_Changed:_Java.Lang.SuppressWarnings" class="injected"></a>


<h3 id='Java.Lang.SuppressWarnings'>Type Changed: Java.Lang.SuppressWarnings</h3>

Added:

```
public abstract string [] Value ();
```

 <a name="Type_Changed:_Java.Lang.Throwable" class="injected"></a>


<h3 id='Java.Lang.Throwable'>Type Changed: Java.Lang.Throwable</h3>

Added:

```
protected Throwable (string p0, Throwable p1, bool p2, bool p3);
 	public void AddSuppressed (Throwable p0);
 	public Throwable[] GetSuppressed ();
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

 <a name="Type_Changed:_Java.Net.HttpCookie" class="injected"></a>


<h3 id='Java.Net.HttpCookie'>Type Changed: Java.Net.HttpCookie</h3>

Added:

```
public bool HttpOnly {
 		get;
 		set;
 	}
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
public override bool Equals (Java.Lang.Object socketAddr);
 	public override int GetHashCode ();
```

Added:

```
public bool Equals (Java.Lang.Object socketAddr);
 	public int GetHashCode ();
 	public string HostString {
 		get;
 	}
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

 <a name="Type_Changed:_Java.Net.URLClassLoader" class="injected"></a>


<h3 id='Java.Net.URLClassLoader'>Type Changed: Java.Net.URLClassLoader</h3>

Added:

```
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

 <a name="Type_Changed:_Java.Util.BitSet" class="injected"></a>


<h3 id='Java.Util.BitSet'>Type Changed: Java.Util.BitSet</h3>

Added:

```
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

Added:

```
public ConcurrentModificationException (string p0, Java.Lang.Throwable p1);
 	public ConcurrentModificationException (Java.Lang.Throwable p0);
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
```

Added:

```
public sealed class Formatter : Java.Lang.Object, Java.IO.IFlushable {
```

 <a name="Type_Changed:_Java.Util.GregorianCalendar" class="injected"></a>


<h3 id='Java.Util.GregorianCalendar'>Type Changed: Java.Util.GregorianCalendar</h3>

Added:

```
public override bool IsWeekDateSupported {
 		get;
 	}
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
public Scanner (Java.Nio.Channels.IReadableByteChannel src);
 	public Scanner (Java.Nio.Channels.IReadableByteChannel src, string charsetName);
```

 <a name="Type_Changed:_Java.Util.TimeZone" class="injected"></a>


<h3 id='Java.Util.TimeZone'>Type Changed: Java.Util.TimeZone</h3>

Added:

```
public virtual bool ObservesDaylightTime ();
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

Added:

```
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

 <a name="Type_Changed:_Java.Util.Zip.DeflaterInputStream" class="injected"></a>


<h3 id='Java.Util.Zip.DeflaterInputStream'>Type Changed: Java.Util.Zip.DeflaterInputStream</h3>

Removed:

```
public DeflaterInputStream (System.IO.Stream in);
```

Added:

```
public DeflaterInputStream (System.IO.Stream in);
```

 <a name="Type_Changed:_Java.Util.Zip.DeflaterOutputStream" class="injected"></a>


<h3 id='Java.Util.Zip.DeflaterOutputStream'>Type Changed: Java.Util.Zip.DeflaterOutputStream</h3>

Added:

```
public DeflaterOutputStream (System.IO.Stream p0, bool p1);
 	public DeflaterOutputStream (System.IO.Stream p0, Deflater p1, bool p2);
 	public DeflaterOutputStream (System.IO.Stream p0, Deflater p1, int p2, bool p3);
```

 <a name="Type_Changed:_Java.Util.Zip.GZIPOutputStream" class="injected"></a>


<h3 id='Java.Util.Zip.GZIPOutputStream'>Type Changed: Java.Util.Zip.GZIPOutputStream</h3>

Added:

```
public GZIPOutputStream (System.IO.Stream p0, bool p1);
 	public GZIPOutputStream (System.IO.Stream p0, int p1, bool p2);
```

 <a name="Type_Changed:_Java.Util.Zip.InflaterOutputStream" class="injected"></a>


<h3 id='Java.Util.Zip.InflaterOutputStream'>Type Changed: Java.Util.Zip.InflaterOutputStream</h3>

Removed:

```
public InflaterOutputStream (System.IO.Stream out, Inflater inf, int bufferSize);
```

Added:

```
public InflaterOutputStream (System.IO.Stream out, Inflater inf, int bufferSize);
```

 <a name="Type_Changed:_Java.Util.Zip.ZipFile" class="injected"></a>


<h3 id='Java.Util.Zip.ZipFile'>Type Changed: Java.Util.Zip.ZipFile</h3>

Added:

```
public ZipFile (Java.IO.File p0, int p1, Java.Nio.Charset.Charset p2);
 	public ZipFile (Java.IO.File p0, Java.Nio.Charset.Charset p1);
 	public ZipFile (string p0, Java.Nio.Charset.Charset p1);
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

 <a name="Type_Changed:_Javax.Net.Ssl.SSLParameters" class="injected"></a>


<h3 id='Javax.Net.Ssl.SSLParameters'>Type Changed: Javax.Net.Ssl.SSLParameters</h3>

Removed:

```
public SSLParameters ();
 	public SSLParameters (string [] cipherSuites);
```

Added:

```
public SSLParameters (string [] cipherSuites);
 	public SSLParameters ();
 	public virtual string EndpointIdentificationAlgorithm {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_Javax.Net.Ssl.SSLServerSocket" class="injected"></a>


<h3 id='Javax.Net.Ssl.SSLServerSocket'>Type Changed: Javax.Net.Ssl.SSLServerSocket</h3>

Added:

```
public virtual SSLParameters SSLParameters {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_Javax.Net.Ssl.SSLSocket" class="injected"></a>


<h3 id='Javax.Net.Ssl.SSLSocket'>Type Changed: Javax.Net.Ssl.SSLSocket</h3>

Added:

```
public virtual ISSLSession HandshakeSession {
 		get;
 	}
```
