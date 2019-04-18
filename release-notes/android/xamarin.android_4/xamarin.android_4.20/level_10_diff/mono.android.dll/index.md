---
id: EA3E1AE0-9122-4C55-BD7E-03DFA2E464DF
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.App.Admin

### New Type Android.App.Admin.DevicePolicyManagerFlags

```
[Serializable]
public enum DevicePolicyManagerFlags {
	None = 0,
}
```

## Namespace Android.Media

### Type Changed: Android.Media.MediaMetadataRetriever

Added methods:

```
public string ExtractMetadata (int keyCode);
	public Android.Graphics.Bitmap GetFrameAtTime (long timeUs, int option);
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

Added methods:

```
public int Get (Keycode keyCode, int metaState);
	public char GetMatch (Keycode keyCode, char[] chars, int metaState);
```

### Type Changed: Android.Views.KeyEvent

Added method:

```
public char GetMatch (char[] chars, int metaState);
```

### Type Changed: Android.Views.MotionEvent

Added methods:

```
public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, float x, float y, MetaKeyStates metaState);
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointers, int[] pointerIds, MotionEvent.PointerCoords[] pointerCoords, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags, InputSourceType source, MotionEventFlags flags);
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointers, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
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
