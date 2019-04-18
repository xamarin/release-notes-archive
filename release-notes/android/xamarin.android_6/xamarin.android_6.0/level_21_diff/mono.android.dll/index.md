---
id: 61869BEB-DFE3-4D05-919A-816D2F667A88
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

## Namespace Android.OS

### Type Changed: Android.OS.Build

### Type Changed: Android.OS.Build.VERSION_CODES

Removed field:

<pre style='color: red'>
	public static const int L;
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

## Namespace Android.Service.Voice

### Type Changed: Android.Service.Voice.AlwaysOnHotwordDetector

Added property:

<pre style='color: green'>
	public virtual RecognitionMode SupportedRecognitionModes { get; }
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
