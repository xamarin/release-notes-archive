---
id: AAD6B769-B2C0-4658-8ADB-5E937D3AA2CD
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.App

### Type Changed: Android.App.DatePickerDialog

### Type Changed: Android.App.DatePickerDialog.DateSetEventArgs

Added property:

```
public int Month { get; }
```







### New Type Android.App.UiAutomationFlags

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UiAutomationFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>





## Namespace Android.App.Admin

### New Type Android.App.Admin.UserManagementFlags

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UserManagementFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>





## Namespace Android.Webkit

### Removed Type  <span class='breaking' data-is-breaking="">Android.Webkit.JavascriptInterfaceAttribute</span>



## Namespace Java.Interop

### New Type Java.Interop.JavaInterfaceDefaultMethodAttribute

<pre class='added' data-is-non-breaking="">
public sealed class JavaInterfaceDefaultMethodAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public JavaInterfaceDefaultMethodAttribute ();</span>
}
</pre>





## Namespace Javax.Xml.Datatype

### Type Changed: Javax.Xml.Datatype.XMLGregorianCalendar

Modified properties:

```
public virtual int Millisecond { get; set; }
```

Added method:

```
public virtual void SetMillisecond (int millisecond);
```







## Namespace Xamarin.Android.Net

### Type Changed: Xamarin.Android.Net.AndroidHttpResponseMessage

Added constructor:

```
public AndroidHttpResponseMessage (Java.Net.URL javaUrl, Java.Net.HttpURLConnection httpConnection);
```



Added method:

```
protected override void Dispose (bool disposing);
```







## New Namespace Android.App.Job

### New Type Android.App.Job.TriggerContentUriFlags

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TriggerContentUriFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>





## New Namespace Android.Icu.Lang

### New Type Android.Icu.Lang.FoldCaseOptions

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum FoldCaseOptions {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>



### New Type Android.Icu.Lang.TitlecaseOptions

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TitlecaseOptions {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>





## New Namespace Android.Service.Notification

### New Type Android.Service.Notification.ConditionFlags

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ConditionFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
