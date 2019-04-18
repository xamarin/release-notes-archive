---
id: 1B479775-80D5-496A-B393-6520C5EEB865
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Added method:

<pre style='color: green'>
	public static string FeedbackTypeToString (FeedbackFlags feedbackType);
</pre>

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

## Namespace Javax.Xml

### Type Changed: Javax.Xml.XMLConstants

Added properties:

<pre style='color: green'>
	public static string AccessExternalDtd { get; }
	public static string AccessExternalSchema { get; }
	public static string AccessExternalStylesheet { get; }
</pre>
