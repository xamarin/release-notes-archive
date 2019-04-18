---
id: 67C9DE40-BC24-4C49-8C4E-CE1FA4A31073
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Added method:

<pre style='color: green'>
	public static string FeedbackTypeToString (FeedbackFlags feedbackType);
</pre>

## Namespace Android.Media

### Type Changed: Android.Media.AudioAttributes

Added property:

<pre style='color: green'>
	public AudioUsageKind Usage { get; }
</pre>

### Type Changed: Android.Media.AudioAttributes.Builder

Added method:

<pre style='color: green'>
	public virtual AudioAttributes.Builder SetUsage (AudioUsageKind usage);
</pre>

## Namespace Android.Opengl

### Type Changed: Android.Opengl.GLES20

Modified methods:

```
public void GlGetActiveAttrib (int p0 program, int p1 index, int p2 bufsize, Java.Nio.IntBuffer p3 length, Java.Nio.IntBuffer p4 size, Java.Nio.IntBuffer p5 type, sbyte p6 name)
	public void GlGetActiveUniform (int p0 program, int p1 index, int p2 bufsize, Java.Nio.IntBuffer p3 length, Java.Nio.IntBuffer p4 size, Java.Nio.IntBuffer p5 type, sbyte p6 name)
	public void GlGetShaderSource (int p0 shader, int p1 bufsize, Java.Nio.IntBuffer p2 length, sbyte p3 source)
```

## Namespace Android.OS

### Type Changed: Android.OS.Build

### Type Changed: Android.OS.Build.VERSION_CODES

Removed field:

<pre style='color: red'>
	public static const int L;
</pre>

### Type Changed: Android.OS.Bundle

Modified methods:

```
public override bool ContainsKey (string p0 key)
	public override Java.Lang.Object Get (string p0 key)
	public override double GetDouble (string p0 key)
	public override double GetDouble (string p0 key, double p1 defaultValue)
	public override double[] GetDoubleArray (string p0 key)
	public override int GetInt (string p0 key)
	public override int GetInt (string p0 key, int p1 defaultValue)
	public override int[] GetIntArray (string p0 key)
	public override long GetLong (string p0 key)
	public override long GetLong (string p0 key, long p1 defaultValue)
	public override long[] GetLongArray (string p0 key)
	public override string GetString (string p0 key)
	public override string GetString (string p0 key, string p1 defaultValue)
	public override string[] GetStringArray (string p0 key)
	public override void PutDouble (string p0 key, double p1 value)
	public override void PutDoubleArray (string p0 key, double[] p1 value)
	public override void PutInt (string p0 key, int p1 value)
	public override void PutIntArray (string p0 key, int[] p1 value)
	public override void PutLong (string p0 key, long p1 value)
	public override void PutLongArray (string p0 key, long[] p1 value)
	public override void PutString (string p0 key, string p1 value)
	public override void PutStringArray (string p0 key, string[] p1 value)
	public override void Remove (string p0 key)
```

### Type Changed: Android.OS.Parcel

Modified methods:

```
protected Parcel Obtain (int p0 obj)
```

## Namespace Android.Runtime

### Type Changed: Android.Runtime.RegisterAttribute

Added property:

<pre style='color: green'>
	public int ApiSince { get; set; }
</pre>

### New Type Android.Runtime.IntDefAttribute

<pre style='color: green'>
public class IntDefAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public IntDefAttribute ();
	// properties
	public string[] Fields { get; set; }
	public bool Flag { get; set; }
	public string Type { get; set; }
}
</pre>

### New Type Android.Runtime.IntDefinitionAttribute

<pre style='color: green'>
public class IntDefinitionAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public IntDefinitionAttribute (string constantMember);
	// properties
	public string ConstantMember { get; set; }
}
</pre>

### New Type Android.Runtime.StringDefAttribute

<pre style='color: green'>
public class StringDefAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public StringDefAttribute ();
	// properties
	public string[] Fields { get; set; }
	public string Type { get; set; }
}
</pre>

## Namespace Android.Service.Voice

### Type Changed: Android.Service.Voice.AlwaysOnHotwordDetector

Added property:

<pre style='color: green'>
	public virtual RecognitionMode SupportedRecognitionModes { get; }
</pre>

## Namespace Android.Widget

### Type Changed: Android.Widget.ListView

Modified methods:

```
public override void SetSelectionFromTop (int p0 position, int p1 y)
```

## Namespace Java.Interop

### New Type Java.Interop.JavaTypeParametersAttribute

<pre style='color: green'>
public class JavaTypeParametersAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public JavaTypeParametersAttribute (string[] typeParameters);
	// properties
	public string[] TypeParameters { get; set; }
}
</pre>

## Namespace Java.IO

### Type Changed: Java.IO.FilePermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

## Namespace Java.Net

### Type Changed: Java.Net.SocketPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 other)
```

## Namespace Java.Security

### Type Changed: Java.Security.AllPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

### Type Changed: Java.Security.BasicPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

### Type Changed: Java.Security.Permission

Modified methods:

```
public abstract bool Equals (Java.Lang.Object p0 obj)
```

### Type Changed: Java.Security.UnresolvedPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

## Namespace Javax.Security.Auth

### Type Changed: Javax.Security.Auth.PrivateCredentialPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```
