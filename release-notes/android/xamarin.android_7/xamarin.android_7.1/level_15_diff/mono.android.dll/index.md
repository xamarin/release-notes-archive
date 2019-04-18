---
id: 88D21BF0-EFD1-4B2D-955D-7CBACB9C288E
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Java.Util.Concurrent.Atomic

### Type Changed: Java.Util.Concurrent.Atomic.AtomicInteger

Obsoleted properties:

```
[Obsolete ("This property was generated for getAndDecrement() method, while it does not make sense. It will be removed in the future version")]
	public int AndDecrement { get; }
	[Obsolete ("This property was generated for getAndIncrement() method, while it does not make sense. It will be removed in the future version")]
	public int AndIncrement { get; }
```

Added methods:

```
public int GetAndDecrement ();
	public int GetAndIncrement ();
```





### Type Changed: Java.Util.Concurrent.Atomic.AtomicLong

Obsoleted properties:

```
[Obsolete ("This property was generated for getAndDecrement() method, while it does not make sense. It will be removed in the future version")]
	public long AndDecrement { get; }
	[Obsolete ("This property was generated for getAndIncrement() method, while it does not make sense. It will be removed in the future version")]
	public long AndIncrement { get; }
```

Added methods:

```
public long GetAndDecrement ();
	public long GetAndIncrement ();
```







## New Namespace Android.Service.Quicksettings

### New Type Android.Service.Quicksettings.TileState

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TileState {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Inactive = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unavailable = 0,</span>
}
</pre>
