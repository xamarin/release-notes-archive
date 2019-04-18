---
id: 7B9F4C0A-1759-4E00-9C9F-3EED2E8B020F
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
