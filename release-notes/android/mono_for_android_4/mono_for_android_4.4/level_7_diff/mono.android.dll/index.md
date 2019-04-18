---
id: A5B74EAD-82BE-4AEB-8970-E1F70706FF4D
title: "Mono.Android.dll"
---

<a name="Mono.Android.dll" class="injected"></a>


# Mono.Android.dll

 <a name="Namespace:_Android.App" class="injected"></a>


<h2 id="Android.App">Namespace: Android.App</h2>

 <a name="Type_Changed:_Android.App.Activity" class="injected"></a>


<h3 id="Android.App.Activity">Type Changed: Android.App.Activity</h3>

Removed:

```
public class Activity : Android.Views.ContextThemeWrapper, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IComponentCallbacks, LayoutInflater.Android.Views.IFactory, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Activity : Android.Views.ContextThemeWrapper, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IComponentCallbacks, LayoutInflater.Android.Views.IFactory, View.Android.Views.IOnCreateContextMenuListener {
```

 <a name="Type_Changed:_Android.App.Dialog" class="injected"></a>


<h3 id="Android.App.Dialog">Type Changed: Android.App.Dialog</h3>

Removed:

```
public class Dialog : Java.Lang.Object, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Dialog : Java.Lang.Object, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
```

 <a name="Type_Changed:_Android.App.Notification" class="injected"></a>


<h3 id="Android.App.Notification">Type Changed: Android.App.Notification</h3>

Removed:

```
public NotificationFlags LedARGB {
```

Added:

```
public int LedARGB {
```

 <a name="New_Type:_Android.App.PermissionAttribute" class="injected"></a>


<h3 id="Android.App.PermissionAttribute">New Type: Android.App.PermissionAttribute</h3>

```
[Serializable]
public sealed class PermissionAttribute : Attribute {
	
	public PermissionAttribute ();
	
	public string Description {
		get;
		set;
	}
	public string Icon {
		get;
		set;
	}
	public string Label {
		get;
		set;
	}
	public string Name {
		get;
		set;
	}
	public string PermissionGroup {
		get;
		set;
	}
	public Android.Content.PM.Protection ProtectionLevel {
		get;
		set;
	}
}
```

 <a name="New_Type:_Android.App.PermissionGroupAttribute" class="injected"></a>


<h3 id="Android.App.PermissionGroupAttribute">New Type: Android.App.PermissionGroupAttribute</h3>

```
[Serializable]
public sealed class PermissionGroupAttribute : Attribute {
	
	public PermissionGroupAttribute ();
	
	public string Description {
		get;
		set;
	}
	public string Icon {
		get;
		set;
	}
	public string Label {
		get;
		set;
	}
	public string Name {
		get;
		set;
	}
}
```

 <a name="New_Type:_Android.App.PermissionTreeAttribute" class="injected"></a>


<h3 id="Android.App.PermissionTreeAttribute">New Type: Android.App.PermissionTreeAttribute</h3>

```
[Serializable]
public sealed class PermissionTreeAttribute : Attribute {
	
	public PermissionTreeAttribute ();
	
	public string Icon {
		get;
		set;
	}
	public string Label {
		get;
		set;
	}
	public string Name {
		get;
		set;
	}
}
```

 <a name="Namespace:_Android.Runtime" class="injected"></a>


<h2 id="Android.Runtime">Namespace: Android.Runtime</h2>

 <a name="Type_Changed:_Android.Runtime.JNIEnv" class="injected"></a>


<h3 id="Android.Runtime.JNIEnv">Type Changed: Android.Runtime.JNIEnv</h3>

Added:

```
public static void WaitForBridgeProcessing ();
```

 <a name="Type_Changed:_Android.Runtime.JavaList" class="injected"></a>


<h3 id="Android.Runtime.JavaList">Type Changed: Android.Runtime.JavaList</h3>

Removed:

```
public int IndexOf (object item);
```

Added:

```
public virtual bool Add (int index, Java.Lang.Object item);
 	public virtual bool Add (JavaList collection);
 	public virtual bool Add (Java.Lang.Object item);
 	public virtual bool AddAll (int location, JavaList collection);
 	public virtual bool Contains (Java.Lang.Object item);
 	public virtual bool ContainsAll (JavaList collection);
 	public virtual bool Equals (Java.Lang.Object obj);
 	public virtual Java.Lang.Object Get (int location);
 	public virtual int IndexOf (object item);
 	public virtual int IndexOf (Java.Lang.Object item);
 	public virtual Java.Util.IIterator Iterator ();
 	public virtual int LastIndexOf (object item);
 	public virtual Java.Lang.Object Remove (int location);
 	public virtual bool Remove (Java.Lang.Object item);
 	public virtual bool RemoveAll (JavaList collection);
 	public virtual bool RetainAll (JavaList collection);
 	public virtual Java.Lang.Object Set (int location, Java.Lang.Object item);
 	public virtual int Size ();
 	public virtual JavaList SubList (int start, int end);
 	public virtual Java.Lang.Object[] ToArray ();
 	public virtual Java.Lang.Object[] ToArray (Java.Lang.Object[] array);
 	public virtual bool IsEmpty {
 		get;
 	}
```

 <a name="New_Type:_Android.Runtime.ResourceDesignerAttribute" class="injected"></a>


<h3 id="Android.Runtime.ResourceDesignerAttribute">New Type: Android.Runtime.ResourceDesignerAttribute</h3>

```
public class ResourceDesignerAttribute : Attribute {
	
	public ResourceDesignerAttribute (string fullName);
	
	public string FullName {
		get;
		set;
	}
	public bool IsApplication {
		get;
		set;
	}
}
```

 <a name="New_Type:_Android.Runtime.ResourceIdManager" class="injected"></a>


<h3 id="Android.Runtime.ResourceIdManager">New Type: Android.Runtime.ResourceIdManager</h3>

```
public static class ResourceIdManager {
	
	public static void UpdateIdValues ();
}
```

 <a name="Namespace:_Android.Test" class="injected"></a>


<h2 id="Android.Test">Namespace: Android.Test</h2>

 <a name="Type_Changed:_Android.Test.FlakyTest" class="injected"></a>


<h3 id="Android.Test.FlakyTest">Type Changed: Android.Test.FlakyTest</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Android.Test.UiThreadTest" class="injected"></a>


<h3 id="Android.Test.UiThreadTest">Type Changed: Android.Test.UiThreadTest</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Namespace:_Android.Test.Suitebuilder.Annotation" class="injected"></a>


<h2 id="Android.Test.Suitebuilder.Annotation">Namespace: Android.Test.Suitebuilder.Annotation</h2>

 <a name="Type_Changed:_Android.Test.Suitebuilder.Annotation.LargeTest" class="injected"></a>


<h3 id="Android.Test.Suitebuilder.Annotation.LargeTest">Type Changed: Android.Test.Suitebuilder.Annotation.LargeTest</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Android.Test.Suitebuilder.Annotation.MediumTest" class="injected"></a>


<h3 id="Android.Test.Suitebuilder.Annotation.MediumTest">Type Changed: Android.Test.Suitebuilder.Annotation.MediumTest</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Android.Test.Suitebuilder.Annotation.SmallTest" class="injected"></a>


<h3 id="Android.Test.Suitebuilder.Annotation.SmallTest">Type Changed: Android.Test.Suitebuilder.Annotation.SmallTest</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Android.Test.Suitebuilder.Annotation.Smoke" class="injected"></a>


<h3 id="Android.Test.Suitebuilder.Annotation.Smoke">Type Changed: Android.Test.Suitebuilder.Annotation.Smoke</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Android.Test.Suitebuilder.Annotation.Suppress" class="injected"></a>


<h3 id="Android.Test.Suitebuilder.Annotation.Suppress">Type Changed: Android.Test.Suitebuilder.Annotation.Suppress</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Namespace:_Android.Views" class="injected"></a>


<h2 id="Android.Views">Namespace: Android.Views</h2>

 <a name="Type_Changed:_Android.Views.ViewDebug" class="injected"></a>


<h3 id="Android.Views.ViewDebug">Type Changed: Android.Views.ViewDebug</h3>

Added:

```
protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 		
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 		
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 		
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
```

 <a name="Namespace:_Android.Widget" class="injected"></a>


<h2 id="Android.Widget">Namespace: Android.Widget</h2>

 <a name="Type_Changed:_Android.Widget.RemoteViews" class="injected"></a>


<h3 id="Android.Widget.RemoteViews">Type Changed: Android.Widget.RemoteViews</h3>

Added:

```
protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
```

 <a name="Namespace:_Dalvik.Annotation" class="injected"></a>


<h2 id="Dalvik.Annotation">Namespace: Dalvik.Annotation</h2>

 <a name="Type_Changed:_Dalvik.Annotation.TestTarget" class="injected"></a>


<h3 id="Dalvik.Annotation.TestTarget">Type Changed: Dalvik.Annotation.TestTarget</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Dalvik.Annotation.TestTargetClass" class="injected"></a>


<h3 id="Dalvik.Annotation.TestTargetClass">Type Changed: Dalvik.Annotation.TestTargetClass</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Namespace:_Java.Lang" class="injected"></a>


<h2 id="Java.Lang">Namespace: Java.Lang</h2>

 <a name="Type_Changed:_Java.Lang.Deprecated" class="injected"></a>


<h3 id="Java.Lang.Deprecated">Type Changed: Java.Lang.Deprecated</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.Override" class="injected"></a>


<h3 id="Java.Lang.Override">Type Changed: Java.Lang.Override</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.SuppressWarnings" class="injected"></a>


<h3 id="Java.Lang.SuppressWarnings">Type Changed: Java.Lang.SuppressWarnings</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Namespace:_Java.Lang.Annotation" class="injected"></a>


<h2 id="Java.Lang.Annotation">Namespace: Java.Lang.Annotation</h2>

 <a name="Type_Changed:_Java.Lang.Annotation.Documented" class="injected"></a>


<h3 id="Java.Lang.Annotation.Documented">Type Changed: Java.Lang.Annotation.Documented</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.Annotation.Inherited" class="injected"></a>


<h3 id="Java.Lang.Annotation.Inherited">Type Changed: Java.Lang.Annotation.Inherited</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.Annotation.Retention" class="injected"></a>


<h3 id="Java.Lang.Annotation.Retention">Type Changed: Java.Lang.Annotation.Retention</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Lang.Annotation.Target" class="injected"></a>


<h3 id="Java.Lang.Annotation.Target">Type Changed: Java.Lang.Annotation.Target</h3>

Added:

```
protected override IntPtr ThresholdClass {
 		get;
 	}
 	protected override Type ThresholdType {
 		get;
 	}
```

 <a name="Namespace:_Java.Nio" class="injected"></a>


<h2 id="Java.Nio">Namespace: Java.Nio</h2>

 <a name="Type_Changed:_Java.Nio.ByteBuffer" class="injected"></a>


<h3 id="Java.Nio.ByteBuffer">Type Changed: Java.Nio.ByteBuffer</h3>

Removed:

```
public abstract bool IsDirect {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Nio.CharBuffer" class="injected"></a>


<h3 id="Java.Nio.CharBuffer">Type Changed: Java.Nio.CharBuffer</h3>

Removed:

```
public abstract bool IsDirect {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Nio.DoubleBuffer" class="injected"></a>


<h3 id="Java.Nio.DoubleBuffer">Type Changed: Java.Nio.DoubleBuffer</h3>

Removed:

```
public abstract bool IsDirect {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Nio.FloatBuffer" class="injected"></a>


<h3 id="Java.Nio.FloatBuffer">Type Changed: Java.Nio.FloatBuffer</h3>

Removed:

```
public abstract bool IsDirect {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Nio.IntBuffer" class="injected"></a>


<h3 id="Java.Nio.IntBuffer">Type Changed: Java.Nio.IntBuffer</h3>

Removed:

```
public abstract bool IsDirect {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Nio.LongBuffer" class="injected"></a>


<h3 id="Java.Nio.LongBuffer">Type Changed: Java.Nio.LongBuffer</h3>

Removed:

```
public abstract bool IsDirect {
 		get;
 	}
```

 <a name="Type_Changed:_Java.Nio.ShortBuffer" class="injected"></a>


<h3 id="Java.Nio.ShortBuffer">Type Changed: Java.Nio.ShortBuffer</h3>

Removed:

```
public abstract bool IsDirect {
 		get;
 	}
```

&nbsp;
