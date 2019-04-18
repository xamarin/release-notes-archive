---
id: 2731C29E-0178-4148-98B7-D206DB411F7F
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android

### Type Changed: Android.Manifest

### Type Changed: Android.Manifest.Permission

Obsoleted fields:

```
[Obsolete ()]
	public static const string GetTasks = "android.permission.GET_TASKS";
	[Obsolete ()]
	public static const string ReadSocialStream = "android.permission.READ_SOCIAL_STREAM";
	[Obsolete ()]
	public static const string WriteSocialStream = "android.permission.WRITE_SOCIAL_STREAM";
```

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Added method:

<pre style='color: green'>
	public static string FeedbackTypeToString (FeedbackFlags feedbackType);
</pre>

## Namespace Android.App

### Type Changed: Android.App.ActivityOptions

Modified methods:

```
public ActivityOptions MakeScaleUpAnimation (Android.Views.View source, int startX, int startY, int startWidth width, int startHeight height)
```

### Type Changed: Android.App.DatePickerDialog

Modified constructors:

```
public DatePickerDialog (Android.Content.Context context, int theme, DatePickerDialog.IOnDateSetListener callBack listener, int year, int monthOfYear, int dayOfMonth)
```

### Type Changed: Android.App.Notification

### Type Changed: Android.App.Notification.Builder

Obsoleted methods:

```
[Obsolete ()]
	public virtual Notification.Builder SetSound (Android.Net.Uri sound, Android.Media.Stream streamType);
```

### Type Changed: Android.App.TimePickerDialog

Modified methods:

```
public virtual void UpdateTime (int hourOfDay, int minutOfHour minuteOfHour)
```

## Namespace Android.Content

### Type Changed: Android.Content.ContextWrapper

Obsoleted methods:

```
[Obsolete ()]
	public override void RemoveStickyBroadcast (Intent intent);
	[Obsolete ()]
	public override void RemoveStickyBroadcastAsUser (Intent intent, Android.OS.UserHandle user);
	[Obsolete ()]
	public override void SendStickyBroadcast (Intent intent);
	[Obsolete ()]
	public override void SendStickyBroadcastAsUser (Intent intent, Android.OS.UserHandle user);
	[Obsolete ()]
	public override void SendStickyOrderedBroadcast (Intent intent, BroadcastReceiver resultReceiver, Android.OS.Handler scheduler, Android.App.Result initialCode, string initialData, Android.OS.Bundle initialExtras);
	[Obsolete ()]
	public override void SendStickyOrderedBroadcastAsUser (Intent intent, Android.OS.UserHandle user, BroadcastReceiver resultReceiver, Android.OS.Handler scheduler, Android.App.Result initialCode, string initialData, Android.OS.Bundle initialExtras);
```

## Namespace Android.Graphics

### Type Changed: Android.Graphics.Canvas

Obsoleted methods:

```
[Obsolete ()]
	public virtual bool ClipRegion (Region region);
```

### Type Changed: Android.Graphics.Paint

Modified methods:

```
public virtual void SetShadowLayer (float radius, float dx, float dy, Color color shadowColor)
```

### Type Changed: Android.Graphics.RadialGradient

Modified constructors:

```
public RadialGradient (float x centerX, float y centerY, float radius, Color color0 centerColor, Color color1 edgeColor, Shader.TileMode tile tileMode)
	public RadialGradient (float x centerX, float y centerY, float radius, int[] colors, float[] positions stops, Shader.TileMode tile tileMode)
```

## Namespace Android.InputMethodServices

### Type Changed: Android.InputMethodServices.InputMethodService

Obsoleted methods:

```
[Obsolete ()]
	public virtual bool EnableHardwareAcceleration ();
	[Obsolete ()]
	public virtual void OnUpdateCursor (Android.Graphics.Rect newCursor);
```

## Namespace Android.Media

### Type Changed: Android.Media.AudioManager

Obsoleted methods:

```
[Obsolete ()]
	public virtual void RegisterMediaButtonEventReceiver (Android.Content.ComponentName eventReceiver);
	[Obsolete ()]
	public virtual void RegisterMediaButtonEventReceiver (Android.App.PendingIntent eventReceiver);
	[Obsolete ()]
	public virtual void RegisterRemoteControlClient (RemoteControlClient rcClient);
	[Obsolete ()]
	public virtual bool RegisterRemoteController (RemoteController rctlr);
	[Obsolete ()]
	public virtual void UnregisterMediaButtonEventReceiver (Android.App.PendingIntent eventReceiver);
	[Obsolete ()]
	public virtual void UnregisterMediaButtonEventReceiver (Android.Content.ComponentName eventReceiver);
	[Obsolete ()]
	public virtual void UnregisterRemoteControlClient (RemoteControlClient rcClient);
	[Obsolete ()]
	public virtual void UnregisterRemoteController (RemoteController rctlr);
```

### Type Changed: Android.Media.MediaCodec

Obsoleted methods:

```
[Obsolete ()]
	public Java.Nio.ByteBuffer[] GetInputBuffers ();
	[Obsolete ()]
	public Java.Nio.ByteBuffer[] GetOutputBuffers ();
```

### Type Changed: Android.Media.MediaCodecList

Obsoleted properties:

```
[Obsolete ()]
	public static int CodecCount { get; }
```

Obsoleted methods:

```
[Obsolete ()]
	public static MediaCodecInfo GetCodecInfoAt (int index);
```

### Type Changed: Android.Media.MediaPlayer

Modified methods:

```
public virtual void AddTimedTextSource (Java.IO.FileDescriptor fd, long offset, long length, string mimeType mime)
```

### Type Changed: Android.Media.MediaRecorder

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetCamera (Android.Hardware.Camera c);
```

### Type Changed: Android.Media.Ringtone

Obsoleted properties:

```
[Obsolete ()]
	public virtual Stream StreamType { get; set; }
```

## Namespace Android.OS

### Type Changed: Android.OS.UserManager

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetUserRestriction (string key, bool value);
	[Obsolete ()]
	public virtual void SetUserRestrictions (Bundle restrictions, UserHandle userHandle);
```

## Namespace Android.Provider

### Type Changed: Android.Provider.ContactsContract

### Type Changed: Android.Provider.ContactsContract.Contacts

### Type Changed: Android.Provider.ContactsContract.StreamItems

Obsoleted fields:

```
[Obsolete ()]
	public static const string ContentDirectory = "stream_items";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ()]
	public static const string AccountName = "account_name";
	[Obsolete ()]
	public static const string AccountType = "account_type";
	[Obsolete ()]
	public static const string Comments = "comments";
	[Obsolete ()]
	public static const string ContactId = "contact_id";
	[Obsolete ()]
	public static const string ContactLookupKey = "contact_lookup";
	[Obsolete ()]
	public static const string DataSet = "data_set";
	[Obsolete ()]
	public static const string RawContactId = "raw_contact_id";
	[Obsolete ()]
	public static const string RawContactSourceId = "raw_contact_source_id";
	[Obsolete ()]
	public static const string ResIcon = "icon";
	[Obsolete ()]
	public static const string ResLabel = "label";
	[Obsolete ()]
	public static const string ResPackage = "res_package";
	[Obsolete ()]
	public static const string Sync1 = "stream_item_sync1";
	[Obsolete ()]
	public static const string Sync2 = "stream_item_sync2";
	[Obsolete ()]
	public static const string Sync3 = "stream_item_sync3";
	[Obsolete ()]
	public static const string Sync4 = "stream_item_sync4";
	[Obsolete ()]
	public static const string Text = "text";
	[Obsolete ()]
	public static const string Timestamp = "timestamp";
```

### Type Changed: Android.Provider.ContactsContract.RawContacts

### Type Changed: Android.Provider.ContactsContract.StreamItems

Obsoleted fields:

```
[Obsolete ()]
	public static const string ContentDirectory = "stream_items";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ()]
	public static const string AccountName = "account_name";
	[Obsolete ()]
	public static const string AccountType = "account_type";
	[Obsolete ()]
	public static const string Comments = "comments";
	[Obsolete ()]
	public static const string ContactId = "contact_id";
	[Obsolete ()]
	public static const string ContactLookupKey = "contact_lookup";
	[Obsolete ()]
	public static const string DataSet = "data_set";
	[Obsolete ()]
	public static const string RawContactId = "raw_contact_id";
	[Obsolete ()]
	public static const string RawContactSourceId = "raw_contact_source_id";
	[Obsolete ()]
	public static const string ResIcon = "icon";
	[Obsolete ()]
	public static const string ResLabel = "label";
	[Obsolete ()]
	public static const string ResPackage = "res_package";
	[Obsolete ()]
	public static const string Sync1 = "stream_item_sync1";
	[Obsolete ()]
	public static const string Sync2 = "stream_item_sync2";
	[Obsolete ()]
	public static const string Sync3 = "stream_item_sync3";
	[Obsolete ()]
	public static const string Sync4 = "stream_item_sync4";
	[Obsolete ()]
	public static const string Text = "text";
	[Obsolete ()]
	public static const string Timestamp = "timestamp";
```

### Type Changed: Android.Provider.ContactsContract.StreamItemPhotos

Obsoleted fields:

```
[Obsolete ()]
	public static const string Photo = "photo";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ()]
	public static const string PhotoFileId = "photo_file_id";
	[Obsolete ()]
	public static const string PhotoUri = "photo_uri";
	[Obsolete ()]
	public static const string SortIndex = "sort_index";
	[Obsolete ()]
	public static const string StreamItemId = "stream_item_id";
	[Obsolete ()]
	public static const string Sync1 = "stream_item_photo_sync1";
	[Obsolete ()]
	public static const string Sync2 = "stream_item_photo_sync2";
	[Obsolete ()]
	public static const string Sync3 = "stream_item_photo_sync3";
	[Obsolete ()]
	public static const string Sync4 = "stream_item_photo_sync4";
```

### Type Changed: Android.Provider.ContactsContract.StreamItemPhotosColumns

Obsoleted fields:

```
[Obsolete ()]
	public static const string PhotoFileId = "photo_file_id";
	[Obsolete ()]
	public static const string PhotoUri = "photo_uri";
	[Obsolete ()]
	public static const string SortIndex = "sort_index";
	[Obsolete ()]
	public static const string StreamItemId = "stream_item_id";
	[Obsolete ()]
	public static const string Sync1 = "stream_item_photo_sync1";
	[Obsolete ()]
	public static const string Sync2 = "stream_item_photo_sync2";
	[Obsolete ()]
	public static const string Sync3 = "stream_item_photo_sync3";
	[Obsolete ()]
	public static const string Sync4 = "stream_item_photo_sync4";
```

### Type Changed: Android.Provider.ContactsContract.StreamItems

Obsoleted fields:

```
[Obsolete ()]
	public static const string ContentItemType = "vnd.android.cursor.item/stream_item";
	[Obsolete ()]
	public static const string ContentType = "vnd.android.cursor.dir/stream_item";
	[Obsolete ()]
	public static const string MaxItems = "max_items";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ()]
	public static const string AccountName = "account_name";
	[Obsolete ()]
	public static const string AccountType = "account_type";
	[Obsolete ()]
	public static const string Comments = "comments";
	[Obsolete ()]
	public static const string ContactId = "contact_id";
	[Obsolete ()]
	public static const string ContactLookupKey = "contact_lookup";
	[Obsolete ()]
	public static const string DataSet = "data_set";
	[Obsolete ()]
	public static const string RawContactId = "raw_contact_id";
	[Obsolete ()]
	public static const string RawContactSourceId = "raw_contact_source_id";
	[Obsolete ()]
	public static const string ResIcon = "icon";
	[Obsolete ()]
	public static const string ResLabel = "label";
	[Obsolete ()]
	public static const string ResPackage = "res_package";
	[Obsolete ()]
	public static const string Sync1 = "stream_item_sync1";
	[Obsolete ()]
	public static const string Sync2 = "stream_item_sync2";
	[Obsolete ()]
	public static const string Sync3 = "stream_item_sync3";
	[Obsolete ()]
	public static const string Sync4 = "stream_item_sync4";
	[Obsolete ()]
	public static const string Text = "text";
	[Obsolete ()]
	public static const string Timestamp = "timestamp";
```

### Type Changed: Android.Provider.ContactsContract.StreamItemPhotos

Obsoleted fields:

```
[Obsolete ()]
	public static const string ContentDirectory = "photo";
	[Obsolete ()]
	public static const string ContentItemType = "vnd.android.cursor.item/stream_item_photo";
	[Obsolete ()]
	public static const string ContentType = "vnd.android.cursor.dir/stream_item_photo";
```

### Type Changed: Android.Provider.ContactsContract.InterfaceConsts

Obsoleted fields:

```
[Obsolete ()]
	public static const string PhotoFileId = "photo_file_id";
	[Obsolete ()]
	public static const string PhotoUri = "photo_uri";
	[Obsolete ()]
	public static const string SortIndex = "sort_index";
	[Obsolete ()]
	public static const string StreamItemId = "stream_item_id";
	[Obsolete ()]
	public static const string Sync1 = "stream_item_photo_sync1";
	[Obsolete ()]
	public static const string Sync2 = "stream_item_photo_sync2";
	[Obsolete ()]
	public static const string Sync3 = "stream_item_photo_sync3";
	[Obsolete ()]
	public static const string Sync4 = "stream_item_photo_sync4";
```

### Type Changed: Android.Provider.ContactsContract.StreamItemsColumns

Obsoleted fields:

```
[Obsolete ()]
	public static const string AccountName = "account_name";
	[Obsolete ()]
	public static const string AccountType = "account_type";
	[Obsolete ()]
	public static const string Comments = "comments";
	[Obsolete ()]
	public static const string ContactId = "contact_id";
	[Obsolete ()]
	public static const string ContactLookupKey = "contact_lookup";
	[Obsolete ()]
	public static const string DataSet = "data_set";
	[Obsolete ()]
	public static const string RawContactId = "raw_contact_id";
	[Obsolete ()]
	public static const string RawContactSourceId = "raw_contact_source_id";
	[Obsolete ()]
	public static const string ResIcon = "icon";
	[Obsolete ()]
	public static const string ResLabel = "label";
	[Obsolete ()]
	public static const string ResPackage = "res_package";
	[Obsolete ()]
	public static const string Sync1 = "stream_item_sync1";
	[Obsolete ()]
	public static const string Sync2 = "stream_item_sync2";
	[Obsolete ()]
	public static const string Sync3 = "stream_item_sync3";
	[Obsolete ()]
	public static const string Sync4 = "stream_item_sync4";
	[Obsolete ()]
	public static const string Text = "text";
	[Obsolete ()]
	public static const string Timestamp = "timestamp";
```

### Type Changed: Android.Provider.Settings

### Type Changed: Android.Provider.Settings.System

Obsoleted fields:

```
[Obsolete ()]
	public static const string NextAlarmFormatted = "next_alarm_formatted";
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

## Namespace Android.Speech.Tts

### Type Changed: Android.Speech.Tts.SynthesisRequest

Obsoleted properties:

```
[Obsolete ()]
	public string Text { get; }
```

### Type Changed: Android.Speech.Tts.TextToSpeech

Obsoleted properties:

```
[Obsolete ()]
	public virtual Java.Util.Locale DefaultLanguage { get; }
	[Obsolete ()]
	public virtual Java.Util.Locale Language { get; }
```

Obsoleted methods:

```
[Obsolete ()]
	public virtual OperationResult AddEarcon (string earcon, string filename);
	[Obsolete ()]
	public virtual System.Collections.Generic.ICollection<string> GetFeatures (Java.Util.Locale locale);
```

### Type Changed: Android.Speech.Tts.TextToSpeech.Engine

Obsoleted fields:

```
[Obsolete ()]
	public static const string KeyFeatureEmbeddedSynthesis = "embeddedTts";
	[Obsolete ()]
	public static const string KeyFeatureNetworkSynthesis = "networkTts";
```

## Namespace Android.Test.Mock

### Type Changed: Android.Test.Mock.MockContext

Obsoleted methods:

```
[Obsolete ()]
	public override void RemoveStickyBroadcast (Android.Content.Intent intent);
	[Obsolete ()]
	public override void RemoveStickyBroadcastAsUser (Android.Content.Intent intent, Android.OS.UserHandle user);
	[Obsolete ()]
	public override void SendStickyBroadcast (Android.Content.Intent intent);
	[Obsolete ()]
	public override void SendStickyBroadcastAsUser (Android.Content.Intent intent, Android.OS.UserHandle user);
	[Obsolete ()]
	public override void SendStickyOrderedBroadcast (Android.Content.Intent intent, Android.Content.BroadcastReceiver resultReceiver, Android.OS.Handler scheduler, Android.App.Result initialCode, string initialData, Android.OS.Bundle initialExtras);
	[Obsolete ()]
	public override void SendStickyOrderedBroadcastAsUser (Android.Content.Intent intent, Android.OS.UserHandle user, Android.Content.BroadcastReceiver resultReceiver, Android.OS.Handler scheduler, Android.App.Result initialCode, string initialData, Android.OS.Bundle initialExtras);
```

## Namespace Android.Text

### Type Changed: Android.Text.SpannableStringBuilder

Modified methods:

```
public virtual int GetTextRunCursor (int contextStart, int contextEnd, int flags dir, int offset, int cursorOpt, Android.Graphics.Paint p)
```

## Namespace Android.Text.Format

### Type Changed: Android.Text.Format.Time

Modified constructors:

```
public Time (string timezone timezoneId)
```

Modified methods:

```
public virtual void Clear (string timezone timezoneId)
```

## Namespace Android.Transitions

### Type Changed: Android.Transitions.ChangeBounds

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetReparent (bool reparent);
```

## Namespace Android.Views.InputMethods

### Type Changed: Android.Views.InputMethods.InputMethodManager

Obsoleted methods:

```
[Obsolete ()]
	public bool IsWatchingCursor (Android.Views.View view);
	[Obsolete ()]
	public void UpdateCursor (Android.Views.View view, int left, int top, int right, int bottom);
```

## Namespace Android.Views.TextService

### Type Changed: Android.Views.TextService.TextInfo

Modified constructors:

```
public TextInfo (string text, int cookie, int sequence sequenceNumber)
```

## Namespace Android.Webkit

### Type Changed: Android.Webkit.CookieManager

Obsoleted methods:

```
[Obsolete ()]
	public virtual void RemoveAllCookie ();
	[Obsolete ()]
	public virtual void RemoveExpiredCookie ();
	[Obsolete ()]
	public virtual void RemoveSessionCookie ();
```

### Type Changed: Android.Webkit.CookieSyncManager

Obsoleted methods:

```
[Obsolete ()]
	public override void ResetSync ();
	[Obsolete ()]
	public override void StartSync ();
	[Obsolete ()]
	public override void StopSync ();
	[Obsolete ()]
	public override void Sync ();
	[Obsolete ()]
	protected void SyncFromRamToFlash ();
```

### Type Changed: Android.Webkit.WebViewClient

Obsoleted methods:

```
[Obsolete ()]
	public virtual WebResourceResponse ShouldInterceptRequest (WebView view, string url);
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

## Namespace Java.Lang

### Type Changed: Java.Lang.JavaSystem

Modified methods:

```
public string MapLibraryName (string userLibName nickname)
```

### Type Changed: Java.Lang.Runtime

Modified methods:

```
public virtual void Load (string pathName absolutePath)
	public System.Threading.Tasks.Task LoadAsync (string pathName absolutePath)
	public virtual void LoadLibrary (string libName nickname)
	public System.Threading.Tasks.Task LoadLibraryAsync (string libName nickname)
```

### Type Changed: Java.Lang.String

Modified methods:

```
public bool ContentEquals (StringBuffer strbuf sb)
```

## Namespace Java.Lang.Reflect

### Type Changed: Java.Lang.Reflect.Proxy

Modified methods:

```
public Java.Lang.Object NewProxyInstance (Java.Lang.ClassLoader loader, Java.Lang.Class[] interfaces, IInvocationHandler h invocationHandler)
```

## Namespace Java.Text

### Type Changed: Java.Text.BreakIterator

Modified methods:

```
public BreakIterator GetCharacterInstance (Java.Util.Locale where locale)
	public BreakIterator GetLineInstance (Java.Util.Locale where locale)
	public BreakIterator GetSentenceInstance (Java.Util.Locale where locale)
	public BreakIterator GetWordInstance (Java.Util.Locale where locale)
```

## Namespace Java.Util

### Type Changed: Java.Util.Locale

Modified methods:

```
public Locale ForLanguageTag (string p0 languageTag)
	public string GetDisplayScript (Locale p0 locale)
	public string GetExtension (char p0 extensionKey)
	public string GetUnicodeLocaleType (string p0 keyWord)
```
