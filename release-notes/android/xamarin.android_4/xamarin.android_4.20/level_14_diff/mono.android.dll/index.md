---
id: 62293DAA-E69B-409B-8089-A5475B82B3DC
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.App

### Type Changed: Android.App.ActivityManager

Removed method:

```
public virtual void MoveTaskToFront (int taskId, int flags);
```

Added methods:

```
public void MoveTaskToFront (int taskId, int flags);
	public virtual void MoveTaskToFront (int taskId, MoveTaskFlags flags);
```

## Namespace Android.App.Admin

### New Type Android.App.Admin.DevicePolicyManagerFlags

```
[Serializable]
public enum DevicePolicyManagerFlags {
	None = 0,
}
```

## Namespace Android.Drm

### Type Changed: Android.Drm.DrmManagerClient

Added methods:

```
public virtual DrmStoreObjectTypeCode GetDrmObjectType (string path, string mimeType);
	public virtual DrmStoreObjectTypeCode GetDrmObjectType (Android.Net.Uri uri, string mimeType);
```

## Namespace Android.Media

### Type Changed: Android.Media.MediaMetadataRetriever

Removed methods:

```
public virtual string ExtractMetadata (int keyCode);
	public virtual Android.Graphics.Bitmap GetFrameAtTime (long timeUs, int option);
```

Added methods:

```
public string ExtractMetadata (int keyCode);
	public virtual string ExtractMetadata (MetadataKey keyCode);
	public Android.Graphics.Bitmap GetFrameAtTime (long timeUs, int option);
	public virtual Android.Graphics.Bitmap GetFrameAtTime (long timeUs, Option option);
```

### New Type Android.Media.AudioFlags

```
[Serializable]
public enum AudioFlags {
	None = 0,
}
```

## Namespace Android.Telephony

### Type Changed: Android.Telephony.PhoneNumberUtils

Added method:

```
public static string StringFromStringAndTOA (string s, PhoneNumberToa TOA);
```

## Namespace Android.Util

### Type Changed: Android.Util.Base64InputStream

Added constructor:

```
public Base64InputStream (System.IO.Stream in, Base64Flags flags);
```

### Type Changed: Android.Util.Base64OutputStream

Added constructor:

```
public Base64OutputStream (System.IO.Stream out, Base64Flags flags);
```

## Namespace Android.Views

### Type Changed: Android.Views.KeyCharacterMap

Removed methods:

```
public virtual int Get (Keycode keyCode, int metaState);
	public virtual char GetMatch (Keycode keyCode, char[] chars, int metaState);
```

Added methods:

```
public int Get (Keycode keyCode, int metaState);
	public virtual int Get (Keycode keyCode, MetaKeyStates metaState);
	public virtual char GetMatch (Keycode keyCode, char[] chars, MetaKeyStates metaState);
	public char GetMatch (Keycode keyCode, char[] chars, int metaState);
```

### Type Changed: Android.Views.KeyEvent

Removed method:

```
public virtual char GetMatch (char[] chars, int metaState);
```

Added methods:

```
public char GetMatch (char[] chars, int metaState);
	public virtual char GetMatch (char[] chars, MetaKeyStates metaState);
```

### Type Changed: Android.Views.MotionEvent

Added methods:

```
public static MotionEvent Obtain (long downTime, long eventTime, int action, int pointers, int[] pointerIds, MotionEvent.PointerCoords[] pointerCoords, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags, int source, int flags);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, float x, float y, MetaKeyStates metaState);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, int pointers, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
```

### Type Changed: Android.Views.View

Removed method:

```
public virtual void DispatchSystemUiVisibilityChanged (int visibility);
```

Added methods:

```
public void DispatchSystemUiVisibilityChanged (int visibility);
	public virtual void DispatchSystemUiVisibilityChanged (SystemUiFlags visibility);
```

## Namespace Android.Views.InputMethods

### New Type Android.Views.InputMethods.CursorAnchorFlags

```
[Serializable]
public enum CursorAnchorFlags {
	None = 0,
}
```

## New Namespace Android.Media.Browse

### New Type Android.Media.Browse.MediaItemFlags

```
[Serializable]
public enum MediaItemFlags {
	None = 0,
}
```

## New Namespace Android.Media.Session

### New Type Android.Media.Session.MediaSessionFlags

```
[Serializable]
[Flags]
public enum MediaSessionFlags {
	None = 0,
}
```

## New Namespace Android.Service.Voice

### New Type Android.Service.Voice.RecognitionFlag

```
[Serializable]
public enum RecognitionFlag {
	None = 0,
}
```
