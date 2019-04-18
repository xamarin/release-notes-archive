---
id: 4EF839EA-6E73-48AB-B6F8-3F938B45F00E
title: "Mono.Android.Support.v13.dll"
---

<a name="Mono.Android.Support.v13.dll" class="injected"></a>


# Mono.Android.Support.v13.dll

 <a name="Namespace:_Android.Support.V4.App" class="injected"></a>


<h2 id='Android.Support.V4.App'>Namespace: Android.Support.V4.App</h2>

 <a name="Type_Changed:_Android.Support.V4.App.Fragment" class="injected"></a>


<h3 id='Android.Support.V4.App.Fragment'>Type Changed: Android.Support.V4.App.Fragment</h3>

Removed:

```
public override bool Equals (Java.Lang.Object p0);
 	public override int GetHashCode ();
```

Added:

```
public bool Equals (Java.Lang.Object p0);
 	public int GetHashCode ();
```

 <a name="Type_Changed:_Android.Support.V4.App.FragmentActivity" class="injected"></a>


<h3 id='Android.Support.V4.App.FragmentActivity'>Type Changed: Android.Support.V4.App.FragmentActivity</h3>

Removed:

```
public override Java.Lang.Object OnRetainNonConfigurationInstance ();
```

Added:

```
public Java.Lang.Object OnRetainNonConfigurationInstance ();
```

 <a name="Type_Changed:_Android.Support.V4.App.TaskStackBuilder" class="injected"></a>


<h3 id='Android.Support.V4.App.TaskStackBuilder'>Type Changed: Android.Support.V4.App.TaskStackBuilder</h3>

Removed:

```
public class TaskStackBuilder : Java.Lang.Object {
```

Added:

```
public class TaskStackBuilder : Java.Lang.Object, Java.Lang.IIterable {
 	public virtual Java.Util.IIterator Iterator ();
```

 <a name="Namespace:_Android.Support.V4.OS" class="injected"></a>


<h2 id='Android.Support.V4.OS'>Namespace: Android.Support.V4.OS</h2>

 <a name="Type_Changed:_Android.Support.V4.OS.ParcelableCompat" class="injected"></a>


<h3 id='Android.Support.V4.OS.ParcelableCompat'>Type Changed: Android.Support.V4.OS.ParcelableCompat</h3>

Removed:

```
public class CompatCreator : Java.Lang.Object {
```

Added:

```
public static Android.OS.IParcelableCreator NewCreator (IParcelableCompatCreatorCallbacks p0);
 	
 	public class CompatCreator : Java.Lang.Object, Android.OS.IParcelableCreator {
```

 <a name="Namespace:_Android.Support.V4.Util" class="injected"></a>


<h2 id='Android.Support.V4.Util'>Namespace: Android.Support.V4.Util</h2>

 <a name="Type_Changed:_Android.Support.V4.Util.LruCache" class="injected"></a>


<h3 id='Android.Support.V4.Util.LruCache'>Type Changed: Android.Support.V4.Util.LruCache</h3>

Removed:

```
public override string ToString ();
```

Added:

```
public string ToString ();
```

 <a name="Namespace:_Android.Support.V4.View" class="injected"></a>


<h2 id='Android.Support.V4.View'>Namespace: Android.Support.V4.View</h2>

 <a name="Type_Changed:_Android.Support.V4.View.ViewPager" class="injected"></a>


<h3 id='Android.Support.V4.View.ViewPager'>Type Changed: Android.Support.V4.View.ViewPager</h3>

Removed:

```
public class ViewPositionComparator : Java.Lang.Object {
```

Added:

```
public class ViewPositionComparator : Java.Lang.Object, Java.Util.IComparator {
 		public virtual int Compare (Java.Lang.Object p0, Java.Lang.Object p1);
```
