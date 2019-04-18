---
id: DF38BC10-AE59-49D3-A4E2-B4FFC20E2D88
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android

### Type Changed: Android.IncludeAndroidResourcesFromAttribute

Removed properties:

```
public string InstallInstructions { get; set; }
	public string PackageName { get; set; }
	public string SourceUrl { get; set; }
	public string Version { get; set; }
```

### Type Changed: Android.Manifest

### Type Changed: Android.Manifest.Permission

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string PersistentActivity = "android.permission.PERSISTENT_ACTIVITY";

	[Obsolete ("deprecated")]
	public static const string RestartPackages = "android.permission.RESTART_PACKAGES";
```

### Type Changed: Android.Resource

### Type Changed: Android.Resource.Attribute

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const int RestoreNeedsApplication;
```

### Type Changed: Android.Resource.Drawable

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const int StatSysPhoneCall;

	[Obsolete ("deprecated")]
	public static const int StatSysPhoneCallForward;

	[Obsolete ("deprecated")]
	public static const int StatSysPhoneCallOnHold;

	[Obsolete ("deprecated")]
	public static const int StatSysVpPhoneCall;

	[Obsolete ("deprecated")]
	public static const int StatSysVpPhoneCallOnHold;
```

### New Type Android.NativeLibraryReferenceAttribute

```
public sealed class NativeLibraryReferenceAttribute : Android.ReferenceFilesAttribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public NativeLibraryReferenceAttribute (string filename);
	// properties
	public string LibraryFileName { get; }
}
```

### New Type Android.ReferenceFilesAttribute

```
public abstract class ReferenceFilesAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// properties
	public string EmbeddedArchive { get; set; }
	public string InstallInstructions { get; set; }
	public string PackageName { get; set; }
	public string SourceUrl { get; set; }
	public string Version { get; set; }
}
```

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Removed method:

```
public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flags);
```

Added method:

```
public virtual void WriteToParcel (Android.OS.Parcel parcel, Android.OS.ParcelableWriteFlags flagz);
```

## Namespace Android.Accounts

### Type Changed: Android.Accounts.AccountManager

Removed method:

```
public virtual IAccountManagerFuture GetAuthTokenByFeatures (string accountType, string authTokenType, string[] features, Android.App.Activity activityForPrompting, Android.OS.Bundle addAccountOptions, Android.OS.Bundle getAuthTokenOptions, IAccountManagerCallback callback, Android.OS.Handler handler);
```

Added method:

```
public virtual IAccountManagerFuture GetAuthTokenByFeatures (string accountType, string authTokenType, string[] features, Android.App.Activity activity, Android.OS.Bundle addAccountOptions, Android.OS.Bundle getAuthTokenOptions, IAccountManagerCallback callback, Android.OS.Handler handler);
```

## Namespace Android.App

### Type Changed: Android.App.ActivityManager

Removed method:

```
public virtual void MoveTaskToFront (int taskId, MoveTaskFlags flags);
```

Added method:

```
public virtual void MoveTaskToFront (int taskId, int flags);
```

### Type Changed: Android.App.Notification

Obsoleted method:

```
[Obsolete ("deprecated")]
	public void SetLatestEventInfo (Android.Content.Context context, string contentTitle, string contentText, PendingIntent contentIntent);
```

## Namespace Android.App.Backup

### Type Changed: Android.App.Backup.BackupDataInputStream

Added interface:

```
Java.IO.ICloseable
```

## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothAdapter

Removed method:

```
public BluetoothServerSocket ListenUsingInsecureRfcommWithServiceRecord (string p0, Java.Util.UUID p1);
```

Added method:

```
public BluetoothServerSocket ListenUsingInsecureRfcommWithServiceRecord (string name, Java.Util.UUID uuid);
```

### Type Changed: Android.Bluetooth.BluetoothDevice

Removed method:

```
public BluetoothSocket CreateInsecureRfcommSocketToServiceRecord (Java.Util.UUID p0);
```

Added method:

```
public BluetoothSocket CreateInsecureRfcommSocketToServiceRecord (Java.Util.UUID uuid);
```

### Type Changed: Android.Bluetooth.BluetoothServerSocket

Added interface:

```
Java.IO.ICloseable
```

Removed method:

```
public void Close ();
```

Added method:

```
public virtual void Close ();
```

### Type Changed: Android.Bluetooth.BluetoothSocket

Added interface:

```
Java.IO.ICloseable
```

Removed method:

```
public void Close ();
```

Added method:

```
public virtual void Close ();
```

## Namespace Android.Content

### Type Changed: Android.Content.AbstractThreadedSyncAdapter

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const int LogSyncDetails;
```

### Type Changed: Android.Content.ContentResolver

Obsoleted property:

```
[Obsolete ("deprecated")]
	public static SyncInfo CurrentSync { get; }
```

### Type Changed: Android.Content.SyncStats

Removed constructor:

```
public SyncStats (Android.OS.Parcel p0);
```

Added constructor:

```
public SyncStats (Android.OS.Parcel in);
```

Removed method:

```
public virtual void WriteToParcel (Android.OS.Parcel p0, Android.OS.ParcelableWriteFlags p1);
```

Added method:

```
public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);
```

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.PackageManager

Removed methods:

```
public virtual ActivityInfo GetActivityInfo (Android.Content.ComponentName className, PackageInfoFlags flags);
	public virtual ActivityInfo GetReceiverInfo (Android.Content.ComponentName className, PackageInfoFlags flags);
	public virtual ServiceInfo GetServiceInfo (Android.Content.ComponentName className, PackageInfoFlags flags);
```

Added methods:

```
public virtual ActivityInfo GetActivityInfo (Android.Content.ComponentName component, PackageInfoFlags flags);
	public virtual ActivityInfo GetReceiverInfo (Android.Content.ComponentName component, PackageInfoFlags flags);
	public virtual ServiceInfo GetServiceInfo (Android.Content.ComponentName component, PackageInfoFlags flags);
```

## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.AssetFileDescriptor

### Type Changed: Android.Content.Res.AssetFileDescriptor.AutoCloseInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Android.Content.Res.AssetFileDescriptor.AutoCloseOutputStream

Added interface:

```
Java.IO.ICloseable
```

## Namespace Android.Database

### Type Changed: Android.Database.ICursor

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual bool Requery ();
```

## Namespace Android.Database.Sqlite

### Type Changed: Android.Database.Sqlite.SQLiteDatabase

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual System.Collections.Generic.IDictionary<System.String,System.String> SyncedTables { get; }
```

### Type Changed: Android.Database.Sqlite.SQLiteOpenHelper

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual SQLiteDatabase ReadableDatabase { get; }

	[Obsolete ("deprecated")]
	public virtual SQLiteDatabase WritableDatabase { get; }
```

### Type Changed: Android.Database.Sqlite.SQLiteProgram

Obsoleted property:

```
[Obsolete ("deprecated")]
	public int UniqueId { get; }
```

## Namespace Android.Graphics

### Type Changed: Android.Graphics.BitmapRegionDecoder

Removed methods:

```
public Bitmap DecodeRegion (Rect p0, BitmapFactory.Options p1);
	public static BitmapRegionDecoder NewInstance (byte[] p0, int p1, int p2, bool p3);
	public static BitmapRegionDecoder NewInstance (Java.IO.FileDescriptor p0, bool p1);
	public static BitmapRegionDecoder NewInstance (System.IO.Stream p0, bool p1);
	public static BitmapRegionDecoder NewInstance (string p0, bool p1);
```

Added methods:

```
public Bitmap DecodeRegion (Rect rect, BitmapFactory.Options options);
	public static BitmapRegionDecoder NewInstance (byte[] data, int offset, int length, bool isShareable);
	public static BitmapRegionDecoder NewInstance (Java.IO.FileDescriptor fd, bool isShareable);
	public static BitmapRegionDecoder NewInstance (System.IO.Stream is, bool isShareable);
	public static BitmapRegionDecoder NewInstance (string pathName, bool isShareable);
```

## Namespace Android.Hardware

### Type Changed: Android.Hardware.Camera

### Type Changed: Android.Hardware.Camera.Parameters

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual int PreviewFrameRate { get; set; }

	[Obsolete ("deprecated")]
	public virtual System.Collections.Generic.IList<Java.Lang.Integer> SupportedPreviewFrameRates { get; }
```

## Namespace Android.Media

### Type Changed: Android.Media.AudioTrack

Added constructors:

```
public AudioTrack (Stream streamType, int sampleRateInHz, ChannelOut channelConfig, Encoding audioFormat, int bufferSizeInBytes, AudioTrackMode mode);
	public AudioTrack (Stream streamType, int sampleRateInHz, ChannelOut channelConfig, Encoding audioFormat, int bufferSizeInBytes, AudioTrackMode mode, int sessionId);
```

Obsoleted constructors:

```
[Obsolete ("ChannelConfiguration is obsolete. Please use another overload with ChannelOut instead")]
	public AudioTrack (Stream streamType, int sampleRateInHz, ChannelConfiguration channelConfig, Encoding audioFormat, int bufferSizeInBytes, AudioTrackMode mode);

	[Obsolete ("ChannelConfiguration is obsolete. Please use another overload with ChannelOut instead")]
	public AudioTrack (Stream streamType, int sampleRateInHz, ChannelConfiguration channelConfig, Encoding audioFormat, int bufferSizeInBytes, AudioTrackMode mode, int sessionId);
```

### Type Changed: Android.Media.MediaMetadataRetriever

Removed methods:

```
public virtual string ExtractMetadata (MetadataKey p0);
	public virtual Android.Graphics.Bitmap GetFrameAtTime (long p0);
	public virtual Android.Graphics.Bitmap GetFrameAtTime (long p0, int p1);
	public virtual void SetDataSource (Android.Content.Context p0, Android.Net.Uri p1);
	public virtual void SetDataSource (string p0);
	public virtual void SetDataSource (Java.IO.FileDescriptor p0);
	public virtual void SetDataSource (Java.IO.FileDescriptor p0, long p1, long p2);
	public System.Threading.Tasks.Task SetDataSourceAsync (Java.IO.FileDescriptor p0, long p1, long p2);
	public System.Threading.Tasks.Task SetDataSourceAsync (Java.IO.FileDescriptor p0);
	public System.Threading.Tasks.Task SetDataSourceAsync (Android.Content.Context p0, Android.Net.Uri p1);
	public System.Threading.Tasks.Task SetDataSourceAsync (string p0);
```

Added methods:

```
public virtual string ExtractMetadata (int keyCode);
	public virtual Android.Graphics.Bitmap GetFrameAtTime (long timeUs);
	public virtual Android.Graphics.Bitmap GetFrameAtTime (long timeUs, int option);
	public virtual void SetDataSource (Android.Content.Context context, Android.Net.Uri uri);
	public virtual void SetDataSource (string path);
	public virtual void SetDataSource (Java.IO.FileDescriptor fd);
	public virtual void SetDataSource (Java.IO.FileDescriptor fd, long offset, long length);
	public System.Threading.Tasks.Task SetDataSourceAsync (Java.IO.FileDescriptor fd, long offset, long length);
	public System.Threading.Tasks.Task SetDataSourceAsync (Java.IO.FileDescriptor fd);
	public System.Threading.Tasks.Task SetDataSourceAsync (Android.Content.Context context, Android.Net.Uri uri);
	public System.Threading.Tasks.Task SetDataSourceAsync (string path);
```

## Namespace Android.Net

### Type Changed: Android.Net.Proxy

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public static string DefaultHost { get; }

	[Obsolete ("deprecated")]
	public static int DefaultPort { get; }
```

### Type Changed: Android.Net.SSLCertificateSocketFactory

Removed constructor:

```
public SSLCertificateSocketFactory (int socketReadTimeoutForSslHandshake);
```

Added constructor:

```
public SSLCertificateSocketFactory (int handshakeTimeoutMillis);
```

Removed methods:

```
public override Java.Net.Socket CreateSocket (string s, int i);
	public override Java.Net.Socket CreateSocket (string s, int i, Java.Net.InetAddress inaddr, int j);
	public override Java.Net.Socket CreateSocket (Java.Net.InetAddress inaddr, int i);
	public override Java.Net.Socket CreateSocket (Java.Net.InetAddress inaddr, int i, Java.Net.InetAddress inaddr2, int j);
	public override Java.Net.Socket CreateSocket (Java.Net.Socket socket, string s, int i, bool flag);
	public static Javax.Net.SocketFactory GetDefault (int socketReadTimeoutForSslHandshake);
```

Added methods:

```
public override Java.Net.Socket CreateSocket (string host, int port);
	public override Java.Net.Socket CreateSocket (string host, int port, Java.Net.InetAddress localAddr, int localPort);
	public override Java.Net.Socket CreateSocket (Java.Net.InetAddress addr, int port);
	public override Java.Net.Socket CreateSocket (Java.Net.InetAddress addr, int port, Java.Net.InetAddress localAddr, int localPort);
	public override Java.Net.Socket CreateSocket (Java.Net.Socket k, string host, int port, bool close);
	public static Javax.Net.SocketFactory GetDefault (int handshakeTimeoutMillis);
```

## Namespace Android.Net.Http

### Type Changed: Android.Net.Http.SslCertificate

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual string ValidNotAfter { get; }

	[Obsolete ("deprecated")]
	public virtual string ValidNotBefore { get; }
```

## Namespace Android.Nfc

### Type Changed: Android.Nfc.NfcAdapter

Obsoleted property:

```
[Obsolete ("deprecated")]
	public static NfcAdapter DefaultAdapter { get; }
```

Removed methods:

```
public void DisableForegroundDispatch (Android.App.Activity p0);
	public void DisableForegroundNdefPush (Android.App.Activity p0);
	public void EnableForegroundDispatch (Android.App.Activity p0, Android.App.PendingIntent p1, Android.Content.IntentFilter[] p2, string[][] p3);
	public void EnableForegroundNdefPush (Android.App.Activity p0, NdefMessage p1);
	public static NfcAdapter GetDefaultAdapter (Android.Content.Context p0);
```

Added methods:

```
public void DisableForegroundDispatch (Android.App.Activity activity);
	public void DisableForegroundNdefPush (Android.App.Activity activity);
	public void EnableForegroundDispatch (Android.App.Activity activity, Android.App.PendingIntent intent, Android.Content.IntentFilter[] filters, string[][] techLists);
	public void EnableForegroundNdefPush (Android.App.Activity activity, NdefMessage msg);
	public static NfcAdapter GetDefaultAdapter (Android.Content.Context context);
```

### Type Changed: Android.Nfc.Tag

Removed method:

```
public virtual void WriteToParcel (Android.OS.Parcel p0, Android.OS.ParcelableWriteFlags p1);
```

Added method:

```
public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);
```

### Type Changed: Android.Nfc.TagLostException

Removed constructor:

```
public TagLostException (string p0);
```

Added constructor:

```
public TagLostException (string message);
```

## Namespace Android.Nfc.Tech

### Type Changed: Android.Nfc.Tech.BasicTagTechnology

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

### Type Changed: Android.Nfc.Tech.IsoDep

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public static IsoDep Get (Android.Nfc.Tag p0);
	public void SetTimeout (int p0);
	public byte[] Transceive (byte[] p0);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] p0);
```

Added methods:

```
public static IsoDep Get (Android.Nfc.Tag tag);
	public void SetTimeout (int timeout);
	public byte[] Transceive (byte[] data);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] data);
```

### Type Changed: Android.Nfc.Tech.MifareClassic

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public bool AuthenticateSectorWithKeyA (int p0, byte[] p1);
	public bool AuthenticateSectorWithKeyB (int p0, byte[] p1);
	public int BlockToSector (int p0);
	public void Decrement (int p0, int p1);
	public System.Threading.Tasks.Task DecrementAsync (int p0, int p1);
	public static MifareClassic Get (Android.Nfc.Tag p0);
	public int GetBlockCountInSector (int p0);
	public void Increment (int p0, int p1);
	public System.Threading.Tasks.Task IncrementAsync (int p0, int p1);
	public byte[] ReadBlock (int p0);
	public System.Threading.Tasks.Task<System.Byte[]> ReadBlockAsync (int p0);
	public void Restore (int p0);
	public System.Threading.Tasks.Task RestoreAsync (int p0);
	public int SectorToBlock (int p0);
	public byte[] Transceive (byte[] p0);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] p0);
	public void Transfer (int p0);
	public System.Threading.Tasks.Task TransferAsync (int p0);
	public void WriteBlock (int p0, byte[] p1);
	public System.Threading.Tasks.Task WriteBlockAsync (int p0, byte[] p1);
```

Added methods:

```
public bool AuthenticateSectorWithKeyA (int sectorIndex, byte[] key);
	public bool AuthenticateSectorWithKeyB (int sectorIndex, byte[] key);
	public int BlockToSector (int blockIndex);
	public void Decrement (int blockIndex, int value);
	public System.Threading.Tasks.Task DecrementAsync (int blockIndex, int value);
	public static MifareClassic Get (Android.Nfc.Tag tag);
	public int GetBlockCountInSector (int sectorIndex);
	public void Increment (int blockIndex, int value);
	public System.Threading.Tasks.Task IncrementAsync (int blockIndex, int value);
	public byte[] ReadBlock (int blockIndex);
	public System.Threading.Tasks.Task<System.Byte[]> ReadBlockAsync (int blockIndex);
	public void Restore (int blockIndex);
	public System.Threading.Tasks.Task RestoreAsync (int blockIndex);
	public int SectorToBlock (int sectorIndex);
	public byte[] Transceive (byte[] data);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] data);
	public void Transfer (int blockIndex);
	public System.Threading.Tasks.Task TransferAsync (int blockIndex);
	public void WriteBlock (int blockIndex, byte[] data);
	public System.Threading.Tasks.Task WriteBlockAsync (int blockIndex, byte[] data);
```

### Type Changed: Android.Nfc.Tech.MifareUltralight

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public static MifareUltralight Get (Android.Nfc.Tag p0);
	public byte[] ReadPages (int p0);
	public System.Threading.Tasks.Task<System.Byte[]> ReadPagesAsync (int p0);
	public byte[] Transceive (byte[] p0);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] p0);
	public void WritePage (int p0, byte[] p1);
	public System.Threading.Tasks.Task WritePageAsync (int p0, byte[] p1);
```

Added methods:

```
public static MifareUltralight Get (Android.Nfc.Tag tag);
	public byte[] ReadPages (int pageOffset);
	public System.Threading.Tasks.Task<System.Byte[]> ReadPagesAsync (int pageOffset);
	public byte[] Transceive (byte[] data);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] data);
	public void WritePage (int pageOffset, byte[] data);
	public System.Threading.Tasks.Task WritePageAsync (int pageOffset, byte[] data);
```

### Type Changed: Android.Nfc.Tech.Ndef

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public static Ndef Get (Android.Nfc.Tag p0);
	public void WriteNdefMessage (Android.Nfc.NdefMessage p0);
	public System.Threading.Tasks.Task WriteNdefMessageAsync (Android.Nfc.NdefMessage p0);
```

Added methods:

```
public static Ndef Get (Android.Nfc.Tag tag);
	public void WriteNdefMessage (Android.Nfc.NdefMessage msg);
	public System.Threading.Tasks.Task WriteNdefMessageAsync (Android.Nfc.NdefMessage msg);
```

### Type Changed: Android.Nfc.Tech.NdefFormatable

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public void Format (Android.Nfc.NdefMessage p0);
	public System.Threading.Tasks.Task FormatAsync (Android.Nfc.NdefMessage p0);
	public void FormatReadOnly (Android.Nfc.NdefMessage p0);
	public System.Threading.Tasks.Task FormatReadOnlyAsync (Android.Nfc.NdefMessage p0);
	public static NdefFormatable Get (Android.Nfc.Tag p0);
```

Added methods:

```
public void Format (Android.Nfc.NdefMessage firstMessage);
	public System.Threading.Tasks.Task FormatAsync (Android.Nfc.NdefMessage firstMessage);
	public void FormatReadOnly (Android.Nfc.NdefMessage firstMessage);
	public System.Threading.Tasks.Task FormatReadOnlyAsync (Android.Nfc.NdefMessage firstMessage);
	public static NdefFormatable Get (Android.Nfc.Tag tag);
```

### Type Changed: Android.Nfc.Tech.NfcA

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public static NfcA Get (Android.Nfc.Tag p0);
	public byte[] Transceive (byte[] p0);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] p0);
```

Added methods:

```
public static NfcA Get (Android.Nfc.Tag tag);
	public byte[] Transceive (byte[] data);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] data);
```

### Type Changed: Android.Nfc.Tech.NfcB

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public static NfcB Get (Android.Nfc.Tag p0);
	public byte[] Transceive (byte[] p0);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] p0);
```

Added methods:

```
public static NfcB Get (Android.Nfc.Tag tag);
	public byte[] Transceive (byte[] data);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] data);
```

### Type Changed: Android.Nfc.Tech.NfcF

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public static NfcF Get (Android.Nfc.Tag p0);
	public byte[] Transceive (byte[] p0);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] p0);
```

Added methods:

```
public static NfcF Get (Android.Nfc.Tag tag);
	public byte[] Transceive (byte[] data);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] data);
```

### Type Changed: Android.Nfc.Tech.NfcV

Added interfaces:

```
ITagTechnology
	Java.IO.ICloseable
```

Removed methods:

```
public static NfcV Get (Android.Nfc.Tag p0);
	public byte[] Transceive (byte[] p0);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] p0);
```

Added methods:

```
public static NfcV Get (Android.Nfc.Tag tag);
	public byte[] Transceive (byte[] data);
	public System.Threading.Tasks.Task<System.Byte[]> TransceiveAsync (byte[] data);
```

### New Type Android.Nfc.Tech.ITagTechnology

```
public interface ITagTechnology : Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual bool IsConnected { get; }
	public virtual Android.Nfc.Tag Tag { get; }
	// methods
	public virtual void Close ();
	public virtual void Connect ();
}
```

### New Type Android.Nfc.Tech.ITagTechnologyExtensions

```
public static class ITagTechnologyExtensions {
	// methods
	public static System.Threading.Tasks.Task ConnectAsync (ITagTechnology self);
}
```

## Namespace Android.OS

### Type Changed: Android.OS.Debug

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public static int GlobalExternalAllocCount { get; }

	[Obsolete ("deprecated")]
	public static int GlobalExternalAllocSize { get; }

	[Obsolete ("deprecated")]
	public static int GlobalExternalFreedCount { get; }

	[Obsolete ("deprecated")]
	public static int GlobalExternalFreedSize { get; }

	[Obsolete ("deprecated")]
	public static int ThreadExternalAllocCount { get; }

	[Obsolete ("deprecated")]
	public static int ThreadExternalAllocSize { get; }
```

### Type Changed: Android.OS.DropBoxManager

### Type Changed: Android.OS.DropBoxManager.Entry

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Android.OS.ParcelFileDescriptor

### Type Changed: Android.OS.ParcelFileDescriptor.AutoCloseInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Android.OS.ParcelFileDescriptor.AutoCloseOutputStream

Added interface:

```
Java.IO.ICloseable
```

## Namespace Android.Preferences

### Type Changed: Android.Preferences.PreferenceActivity

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual PreferenceManager PreferenceManager { get; }

	[Obsolete ("deprecated")]
	public virtual PreferenceScreen PreferenceScreen { get; set; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public Preference FindPreference (string key);
```

## Namespace Android.Provider

### Type Changed: Android.Provider.Browser

Removed method:

```
public static void SendString (Android.Content.Context c, string s);
```

Added method:

```
public static void SendString (Android.Content.Context context, string string);
```

### Type Changed: Android.Provider.Browser.SearchColumns

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const string Url = "url";
```

### Type Changed: Android.Provider.Settings

### Type Changed: Android.Provider.Settings.System

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const string LockPatternEnabled = "lock_pattern_autolock";

	[Obsolete ("deprecated")]
	public static const string LockPatternTactileFeedbackEnabled = "lock_pattern_tactile_feedback_enabled";

	[Obsolete ("deprecated")]
	public static const string LockPatternVisible = "lock_pattern_visible_pattern";

	[Obsolete ("deprecated")]
	public static const string ShowWebSuggestions = "show_web_suggestions";
```

## Namespace Android.Runtime

### Type Changed: Android.Runtime.InputStreamAdapter

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Android.Runtime.JNIEnv

Added method:

```
public static System.IntPtr NewString (char[] text, int length);
```

### Type Changed: Android.Runtime.OutputStreamAdapter

Added interface:

```
Java.IO.ICloseable
```

## Namespace Android.Telephony

### Type Changed: Android.Telephony.PhoneNumberFormattingTextWatcher

Removed method:

```
public virtual void AfterTextChanged (Android.Text.IEditable text);
```

Added method:

```
public virtual void AfterTextChanged (Android.Text.IEditable s);
```

## Namespace Android.Telephony.Cdma

### Type Changed: Android.Telephony.Cdma.CdmaCellLocation

Removed constructor:

```
public CdmaCellLocation (Android.OS.Bundle bundleWithValues);
```

Added constructor:

```
public CdmaCellLocation (Android.OS.Bundle bundle);
```

## Namespace Android.Text

### Type Changed: Android.Text.Layout

Removed constructors:

```
protected Layout (Java.Lang.ICharSequence text, TextPaint paint, int width, Layout.Alignment align, float spacingmult, float spacingadd);
	protected Layout (string text, TextPaint paint, int width, Layout.Alignment align, float spacingmult, float spacingadd);
```

Added constructors:

```
protected Layout (Java.Lang.ICharSequence text, TextPaint paint, int width, Layout.Alignment align, float spacingMult, float spacingAdd);
	protected Layout (string text, TextPaint paint, int width, Layout.Alignment align, float spacingMult, float spacingAdd);
```

Removed method:

```
public virtual void Draw (Android.Graphics.Canvas c, Android.Graphics.Path highlight, Android.Graphics.Paint highlightpaint, int cursorOffsetVertical);
```

Added method:

```
public virtual void Draw (Android.Graphics.Canvas c, Android.Graphics.Path highlight, Android.Graphics.Paint highlightPaint, int cursorOffsetVertical);
```

### Type Changed: Android.Text.TextUtils

Removed methods:

```
public static string Ellipsize (string text, TextPaint p, float avail, TextUtils.TruncateAt where, bool preserveLength, TextUtils.IEllipsizeCallback callback);
	public static Java.Lang.ICharSequence EllipsizeFormatted (Java.Lang.ICharSequence text, TextPaint p, float avail, TextUtils.TruncateAt where, bool preserveLength, TextUtils.IEllipsizeCallback callback);
```

Added methods:

```
public static string Ellipsize (string text, TextPaint paint, float avail, TextUtils.TruncateAt where, bool preserveLength, TextUtils.IEllipsizeCallback callback);
	public static Java.Lang.ICharSequence EllipsizeFormatted (Java.Lang.ICharSequence text, TextPaint paint, float avail, TextUtils.TruncateAt where, bool preserveLength, TextUtils.IEllipsizeCallback callback);
```

## Namespace Android.Text.Format

### Type Changed: Android.Text.Format.Formatter

Removed method:

```
public static string FormatIpAddress (int addr);
```

Added method:

```
public static string FormatIpAddress (int ipv4Address);
```

## Namespace Android.Text.Method

### Type Changed: Android.Text.Method.BaseMovementMethod

Removed method:

```
protected virtual bool HandleMovementKey (Android.Widget.TextView widget, Android.Text.ISpannable buffer, int keyCode, int movementMetaState, Android.Views.KeyEvent e);
```

Added method:

```
protected virtual bool HandleMovementKey (Android.Widget.TextView widget, Android.Text.ISpannable buffer, Android.Views.Keycode keyCode, int movementMetaState, Android.Views.KeyEvent e);
```

### Type Changed: Android.Text.Method.QwertyKeyListener

Removed constructor:

```
public QwertyKeyListener (TextKeyListener.Capitalize cap, bool autotext);
```

Added constructor:

```
public QwertyKeyListener (TextKeyListener.Capitalize cap, bool autoText);
```

Removed method:

```
public static QwertyKeyListener GetInstance (bool autotext, TextKeyListener.Capitalize cap);
```

Added method:

```
public static QwertyKeyListener GetInstance (bool autoText, TextKeyListener.Capitalize cap);
```

## Namespace Android.Util

### Type Changed: Android.Util.Base64InputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Android.Util.Base64OutputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Android.Util.JsonReader

Added interface:

```
Java.IO.ICloseable
```

Removed method:

```
public void Close ();
```

Added method:

```
public virtual void Close ();
```

### Type Changed: Android.Util.JsonWriter

Added interface:

```
Java.IO.ICloseable
```

Removed method:

```
public void Close ();
```

Added method:

```
public virtual void Close ();
```

## Namespace Android.Views

### Type Changed: Android.Views.Display

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual int Orientation { get; }
```

### Type Changed: Android.Views.InputDevice

Removed method:

```
public InputDevice.MotionRange GetMotionRange (Axis rangeType);
```

Added method:

```
public InputDevice.MotionRange GetMotionRange (Axis axis);
```

### Type Changed: Android.Views.ISurfaceHolder

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void SetType (SurfaceType type);
```

### Type Changed: Android.Views.KeyCharacterMap

Removed methods:

```
public virtual int Get (Keycode keyCode, int meta);
	public virtual char GetMatch (Keycode keyCode, char[] chars, int modifiers);
	public static KeyCharacterMap Load (int keyboard);
```

Added methods:

```
public virtual int Get (Keycode keyCode, int metaState);
	public virtual char GetMatch (Keycode keyCode, char[] chars, int metaState);
	public static KeyCharacterMap Load (int deviceId);
```

### Type Changed: Android.Views.KeyEvent

Removed constructors:

```
public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat, MetaKeyStates metaState, int device, int scancode, KeyEventFlags flags);
	public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat, MetaKeyStates metaState, int device, int scancode);
	public KeyEvent (long time, string characters, int device, KeyEventFlags flags);
```

Added constructors:

```
public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat, MetaKeyStates metaState, int deviceId, int scancode, KeyEventFlags flags);
	public KeyEvent (long downTime, long eventTime, KeyEventActions action, Keycode code, int repeat, MetaKeyStates metaState, int deviceId, int scancode);
	public KeyEvent (long time, string characters, int deviceId, KeyEventFlags flags);
```

Removed methods:

```
public virtual char GetMatch (char[] chars, int modifiers);
	public virtual int GetUnicodeChar (int meta);
```

Added methods:

```
public virtual char GetMatch (char[] chars, int metaState);
	public virtual int GetUnicodeChar (int metaState);
```

### Type Changed: Android.Views.MenuPerformFlags

Removed value:

```
AppendToGroup = 1,
```

### Type Changed: Android.Views.MotionEvent

Removed methods:

```
public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointers, int[] pointerIds, MotionEvent.PointerCoords[] pointerCoords, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags, InputSourceType source, MotionEventFlags flags);
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointers, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, float x, float y, MetaKeyStates metaState);
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (MotionEvent o);
	public static MotionEvent ObtainNoHistory (MotionEvent o);
```

Added methods:

```
public static MotionEvent Obtain (long downTime, long eventTime, int action, int pointers, int[] pointerIds, MotionEvent.PointerCoords[] pointerCoords, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags, int source, int flags);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, int pointers, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, float x, float y, MetaKeyStates metaState);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (MotionEvent other);
	public static MotionEvent ObtainNoHistory (MotionEvent other);
```

### Type Changed: Android.Views.Surface

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const int PushBuffers;
```

### Type Changed: Android.Views.View

Added method:

```
public virtual void DispatchSystemUiVisibilityChanged (int visibility);
```

### Type Changed: Android.Views.WindowManagerLayoutParams

Added field:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Views.WindowManagerEventType enum directly instead of this field.")]
	public static const WindowManagerEventType TypeChanged;
```

### Type Changed: Android.Views.WindowManagerTypes

Removed value:

```
Changed = 2,
```

## Namespace Android.Views.InputMethods

### Type Changed: Android.Views.InputMethods.EditorInfo

Removed fields:

```
public static const int ImeMaskAction;
	public static const int ImeNull;
```

### Type Changed: Android.Views.InputMethods.ImeAction

Added value:

```
ImeMaskAction = 255,
```

## Namespace Android.Webkit

### Type Changed: Android.Webkit.CacheManager

Obsoleted property:

```
[Obsolete ("deprecated")]
	public static Java.IO.File CacheFileBaseDir { get; }
```

### Type Changed: Android.Webkit.WebHistoryItem

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual int Id { get; }
```

### Type Changed: Android.Webkit.WebSettings

Obsoleted properties:

```
[Obsolete ("deprecated")]
	public virtual bool NavDump { get; set; }

	[Obsolete ("deprecated")]
	public virtual bool PluginsEnabled { get; set; }

	[Obsolete ("deprecated")]
	public virtual string PluginsPath { get; set; }

	[Obsolete ("deprecated")]
	public virtual bool UseWebViewBackgroundForOverscrollBackground { get; set; }
```

### Type Changed: Android.Webkit.WebView

Removed method:

```
public virtual void LoadDataWithBaseURL (string baseUrl, string data, string mimeType, string encoding, string failUrl);
```

Added method:

```
public virtual void LoadDataWithBaseURL (string baseUrl, string data, string mimeType, string encoding, string historyUrl);
```

### Type Changed: Android.Webkit.WebView.IPictureListener

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void OnNewPicture (WebView view, Android.Graphics.Picture picture);
```

## Namespace Android.Widget

### Type Changed: Android.Widget.DatePicker

Removed method:

```
public virtual void UpdateDate (int year, int monthOfYear, int dayOfMonth);
```

Added method:

```
public virtual void UpdateDate (int year, int month, int dayOfMonth);
```

## Namespace Dalvik.Bytecode

### Type Changed: Dalvik.Bytecode.Opcodes

Obsoleted fields:

```
[Obsolete ("deprecated")]
	public static const int OpBreakpoint;

	[Obsolete ("deprecated")]
	public static const int OpExecuteInline;

	[Obsolete ("deprecated")]
	public static const int OpExecuteInlineRange;

	[Obsolete ("deprecated")]
	public static const int OpIgetObjectQuick;

	[Obsolete ("deprecated")]
	public static const int OpIgetQuick;

	[Obsolete ("deprecated")]
	public static const int OpIgetWideQuick;

	[Obsolete ("deprecated")]
	public static const int OpIgetWideVolatile;

	[Obsolete ("deprecated")]
	public static const int OpInvokeDirectEmpty;

	[Obsolete ("deprecated")]
	public static const int OpInvokeSuperQuick;

	[Obsolete ("deprecated")]
	public static const int OpInvokeSuperQuickRange;

	[Obsolete ("deprecated")]
	public static const int OpInvokeVirtualQuick;

	[Obsolete ("deprecated")]
	public static const int OpInvokeVirtualQuickRange;

	[Obsolete ("deprecated")]
	public static const int OpIputObjectQuick;

	[Obsolete ("deprecated")]
	public static const int OpIputQuick;

	[Obsolete ("deprecated")]
	public static const int OpIputWideQuick;

	[Obsolete ("deprecated")]
	public static const int OpIputWideVolatile;

	[Obsolete ("deprecated")]
	public static const int OpSgetWideVolatile;

	[Obsolete ("deprecated")]
	public static const int OpSputWideVolatile;

	[Obsolete ("deprecated")]
	public static const int OpThrowVerificationError;
```

## Namespace Dalvik.SystemInterop

### Type Changed: Dalvik.SystemInterop.VMDebug

Obsoleted field:

```
[Obsolete ("deprecated")]
	public static const string DefaultMethodTraceFileName = "/sdcard/dmtrace.trace";
```

## Namespace Java.Interop

### Type Changed: Java.Interop.JavaLibraryReferenceAttribute

Removed properties:

```
public string InstallInstructions { get; set; }
	public string PackageName { get; set; }
	public string SourceUrl { get; set; }
	public string Version { get; set; }
```

## Namespace Java.IO

### Type Changed: Java.IO.BufferedInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.BufferedOutputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.BufferedReader

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.BufferedWriter

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.ByteArrayInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.ByteArrayOutputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.CharArrayReader

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.CharArrayWriter

Added interface:

```
ICloseable
```

Removed method:

```
public override void Write (char[] c, int offset, int len);
```

Added method:

```
public override void Write (char[] buffer, int offset, int len);
```

### Type Changed: Java.IO.DataInputStream

Added interface:

```
ICloseable
```

Removed methods:

```
public virtual void ReadFully (byte[] buffer, int offset, int length);
	public virtual void ReadFully (byte[] buffer);
```

Added methods:

```
public virtual void ReadFully (byte[] dst, int offset, int byteCount);
	public virtual void ReadFully (byte[] dst);
```

### Type Changed: Java.IO.DataOutputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.File

Removed methods:

```
public virtual bool RenameTo (File dest);
	public virtual bool SetExecutable (bool p0);
	public virtual bool SetExecutable (bool p0, bool p1);
	public virtual bool SetReadable (bool p0, bool p1);
	public virtual bool SetReadable (bool p0);
	public virtual bool SetWritable (bool p0);
	public virtual bool SetWritable (bool p0, bool p1);
```

Added methods:

```
public virtual bool RenameTo (File newPath);
	public virtual bool SetExecutable (bool executable);
	public virtual bool SetExecutable (bool executable, bool ownerOnly);
	public virtual bool SetReadable (bool readable, bool ownerOnly);
	public virtual bool SetReadable (bool readable);
	public virtual bool SetWritable (bool writable);
	public virtual bool SetWritable (bool writable, bool ownerOnly);
```

### Type Changed: Java.IO.FileInputStream

Removed constructor:

```
public FileInputStream (string fileName);
```

Added constructor:

```
public FileInputStream (string path);
```

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FileOutputStream

Removed constructors:

```
public FileOutputStream (string filename);
	public FileOutputStream (string filename, bool append);
```

Added constructors:

```
public FileOutputStream (string path);
	public FileOutputStream (string path, bool append);
```

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FileReader

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FileWriter

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FilterInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FilterOutputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FilterReader

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FilterWriter

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.IDataInput

Removed methods:

```
public virtual void ReadFully (byte[] buffer);
	public virtual void ReadFully (byte[] buffer, int offset, int count);
```

Added methods:

```
public virtual void ReadFully (byte[] dst);
	public virtual void ReadFully (byte[] dst, int offset, int byteCount);
```

### Type Changed: Java.IO.IDataInputExtensions

Removed methods:

```
public static System.Threading.Tasks.Task ReadFullyAsync (IDataInput self, byte[] buffer);
	public static System.Threading.Tasks.Task ReadFullyAsync (IDataInput self, byte[] buffer, int offset, int count);
```

Added methods:

```
public static System.Threading.Tasks.Task ReadFullyAsync (IDataInput self, byte[] dst);
	public static System.Threading.Tasks.Task ReadFullyAsync (IDataInput self, byte[] dst, int offset, int byteCount);
```

### Type Changed: Java.IO.InputStream

Added interface:

```
ICloseable
```

Removed methods:

```
public virtual int Read (byte[] b, int offset, int length);
	public System.Threading.Tasks.Task<int> ReadAsync (byte[] b, int offset, int length);
	public virtual long Skip (long n);
	public System.Threading.Tasks.Task<long> SkipAsync (long n);
```

Added methods:

```
public virtual int Read (byte[] buffer, int offset, int length);
	public System.Threading.Tasks.Task<int> ReadAsync (byte[] buffer, int offset, int length);
	public virtual long Skip (long byteCount);
	public System.Threading.Tasks.Task<long> SkipAsync (long byteCount);
```

### Type Changed: Java.IO.InputStreamReader

Added interface:

```
ICloseable
```

Removed method:

```
public override int Read (char[] buf, int offset, int length);
```

Added method:

```
public override int Read (char[] buffer, int offset, int length);
```

### Type Changed: Java.IO.IOException

Removed constructors:

```
public IOException (string p0, Java.Lang.Throwable p1);
	public IOException (Java.Lang.Throwable p0);
```

Added constructors:

```
public IOException (string message, Java.Lang.Throwable cause);
	public IOException (Java.Lang.Throwable cause);
```

### Type Changed: Java.IO.LineNumberInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.LineNumberReader

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.ObjectInputStream

Added interfaces:

```
IObjectInput
	IDataInput
	ICloseable
```

Removed methods:

```
public virtual void ReadFully (byte[] buffer);
	public virtual void ReadFully (byte[] buffer, int offset, int length);
	public Java.Lang.Object ReadObject ();
```

Added methods:

```
public virtual void ReadFully (byte[] dst);
	public virtual void ReadFully (byte[] dst, int offset, int byteCount);
	public virtual Java.Lang.Object ReadObject ();
```

### Type Changed: Java.IO.ObjectOutputStream

Added interfaces:

```
IObjectOutput
	IDataOutput
	ICloseable
```

Removed method:

```
public void WriteObject (Java.Lang.Object object);
```

Added method:

```
public virtual void WriteObject (Java.Lang.Object object);
```

### Type Changed: Java.IO.ObjectOutputStream.PutField

Added method:

```
public virtual void Write (IObjectOutput out);
```

### Type Changed: Java.IO.ObjectStreamClass

Removed method:

```
public static ObjectStreamClass LookupAny (Java.Lang.Class p0);
```

Added method:

```
public static ObjectStreamClass LookupAny (Java.Lang.Class cl);
```

### Type Changed: Java.IO.OutputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.OutputStreamWriter

Added interface:

```
ICloseable
```

Removed method:

```
public override void Write (char[] buf, int offset, int count);
```

Added method:

```
public override void Write (char[] buffer, int offset, int count);
```

### Type Changed: Java.IO.PipedInputStream

Removed constructors:

```
public PipedInputStream (int p0);
	public PipedInputStream (PipedOutputStream p0, int p1);
```

Added constructors:

```
public PipedInputStream (int pipeSize);
	public PipedInputStream (PipedOutputStream out, int pipeSize);
```

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PipedOutputStream

Removed constructor:

```
public PipedOutputStream (PipedInputStream dest);
```

Added constructor:

```
public PipedOutputStream (PipedInputStream target);
```

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PipedReader

Removed constructors:

```
public PipedReader (int p0);
	public PipedReader (PipedWriter p0, int p1);
```

Added constructors:

```
public PipedReader (int pipeSize);
	public PipedReader (PipedWriter out, int pipeSize);
```

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PipedWriter

Removed constructor:

```
public PipedWriter (PipedReader dest);
```

Added constructor:

```
public PipedWriter (PipedReader destination);
```

Added interface:

```
ICloseable
```

Removed method:

```
public virtual void Connect (PipedReader stream);
```

Added method:

```
public virtual void Connect (PipedReader reader);
```

### Type Changed: Java.IO.PrintStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PrintWriter

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PushbackInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PushbackReader

Added interface:

```
ICloseable
```

Removed method:

```
public virtual void Unread (char[] buffer, int offset, int count);
```

Added method:

```
public virtual void Unread (char[] buffer, int offset, int length);
```

### Type Changed: Java.IO.RandomAccessFile

Added interface:

```
ICloseable
```

Removed methods:

```
public virtual void ReadFully (byte[] buffer, int offset, int count);
	public virtual void ReadFully (byte[] buffer);
	public System.Threading.Tasks.Task ReadFullyAsync (byte[] buffer);
	public System.Threading.Tasks.Task ReadFullyAsync (byte[] buffer, int offset, int count);
	public virtual void Seek (long pos);
```

Added methods:

```
public virtual void ReadFully (byte[] dst, int offset, int byteCount);
	public virtual void ReadFully (byte[] dst);
	public System.Threading.Tasks.Task ReadFullyAsync (byte[] dst);
	public System.Threading.Tasks.Task ReadFullyAsync (byte[] dst, int offset, int byteCount);
	public virtual void Seek (long offset);
```

### Type Changed: Java.IO.Reader

Added interface:

```
ICloseable
```

Removed methods:

```
public virtual long Skip (long count);
	public System.Threading.Tasks.Task<long> SkipAsync (long count);
```

Added methods:

```
public virtual long Skip (long charCount);
	public System.Threading.Tasks.Task<long> SkipAsync (long charCount);
```

### Type Changed: Java.IO.SequenceInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.StringBufferInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.StringReader

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.StringWriter

Added interface:

```
ICloseable
```

Removed method:

```
public override void Write (char[] cbuf, int offset, int count);
```

Added method:

```
public override void Write (char[] chars, int offset, int count);
```

### Type Changed: Java.IO.Writer

Added interface:

```
ICloseable
```

### New Type Java.IO.ICloseable

```
public interface ICloseable : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void Close ();
}
```

### New Type Java.IO.IExternalizable

```
public interface IExternalizable : ISerializable, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void ReadExternal (IObjectInput input);
	public virtual void WriteExternal (IObjectOutput output);
}
```

### New Type Java.IO.IExternalizableExtensions

```
public static class IExternalizableExtensions {
	// methods
	public static System.Threading.Tasks.Task ReadExternalAsync (IExternalizable self, IObjectInput input);
	public static System.Threading.Tasks.Task WriteExternalAsync (IExternalizable self, IObjectOutput output);
}
```

### New Type Java.IO.IObjectInput

```
public interface IObjectInput : IDataInput, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual int Available ();
	public virtual void Close ();
	public virtual int Read ();
	public virtual int Read (byte[] buffer);
	public virtual int Read (byte[] buffer, int offset, int count);
	public virtual Java.Lang.Object ReadObject ();
	public virtual long Skip (long byteCount);
}
```

### New Type Java.IO.IObjectInputExtensions

```
public static class IObjectInputExtensions {
	// methods
	public static System.Threading.Tasks.Task<int> ReadAsync (IObjectInput self);
	public static System.Threading.Tasks.Task<int> ReadAsync (IObjectInput self, byte[] buffer);
	public static System.Threading.Tasks.Task<int> ReadAsync (IObjectInput self, byte[] buffer, int offset, int count);
	public static System.Threading.Tasks.Task<Java.Lang.Object> ReadObjectAsync (IObjectInput self);
	public static System.Threading.Tasks.Task<long> SkipAsync (IObjectInput self, long byteCount);
}
```

### New Type Java.IO.IObjectOutput

```
public interface IObjectOutput : IDataOutput, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void Close ();
	public virtual void Flush ();
	public virtual void WriteObject (Java.Lang.Object obj);
}
```

### New Type Java.IO.IObjectOutputExtensions

```
public static class IObjectOutputExtensions {
	// methods
	public static System.Threading.Tasks.Task FlushAsync (IObjectOutput self);
	public static System.Threading.Tasks.Task WriteObjectAsync (IObjectOutput self, Java.Lang.Object obj);
}
```

## Namespace Java.Lang

### Type Changed: Java.Lang.AbstractStringBuilder

Removed methods:

```
public virtual IAppendable Append (ICharSequence csq);
	public IAppendable Append (string csq);
	public virtual IAppendable Append (ICharSequence csq, int start, int end);
	public IAppendable Append (string csq, int start, int end);
	public virtual IAppendable Append (char c);
```

Added methods:

```
public virtual IAppendable Append (char p0);
	public virtual IAppendable Append (ICharSequence p0);
	public IAppendable Append (string p0);
	public virtual IAppendable Append (ICharSequence p0, int p1, int p2);
	public IAppendable Append (string p0, int p1, int p2);
```

### Type Changed: Java.Lang.Class

Removed methods:

```
public Reflect.Constructor GetConstructor (Class[] p0);
	public Reflect.Constructor GetDeclaredConstructor (Class[] p0);
	public Reflect.Method GetDeclaredMethod (string p0, Class[] p1);
	public Reflect.Method GetMethod (string p0, Class[] p1);
```

Added methods:

```
public Reflect.Constructor GetConstructor (Class[] parameterTypes);
	public Reflect.Constructor GetDeclaredConstructor (Class[] parameterTypes);
	public Reflect.Method GetDeclaredMethod (string name, Class[] parameterTypes);
	public Reflect.Method GetMethod (string name, Class[] parameterTypes);
```

### Type Changed: Java.Lang.Integer

Removed method:

```
public static string ToString (int value);
```

Added method:

```
public static string ToString (int i);
```

### Type Changed: Java.Lang.JavaSystem

Removed methods:

```
public static void Arraycopy (Object src, int srcPos, Object dest, int destPos, int length);
	public static string GetProperty (string prop);
```

Added methods:

```
public static void Arraycopy (Object src, int srcPos, Object dst, int dstPos, int length);
	public static string GetProperty (string propertyName);
	public static Java.Nio.Channels.IChannel InheritedChannel ();
```

### Type Changed: Java.Lang.Long

Removed methods:

```
public static int BitCount (long lng);
	public static long HighestOneBit (long lng);
	public static long LowestOneBit (long lng);
	public static int NumberOfLeadingZeros (long lng);
	public static int NumberOfTrailingZeros (long lng);
	public static long Reverse (long lng);
	public static long ReverseBytes (long lng);
	public static long RotateLeft (long lng, int distance);
	public static long RotateRight (long lng, int distance);
	public static int Signum (long lng);
	public static string ToBinaryString (long l);
	public static string ToHexString (long l);
	public static string ToOctalString (long l);
	public static string ToString (long l, int radix);
	public static string ToString (long l);
	public static Long ValueOf (long lng);
```

Added methods:

```
public static int BitCount (long v);
	public static long HighestOneBit (long v);
	public static long LowestOneBit (long v);
	public static int NumberOfLeadingZeros (long v);
	public static int NumberOfTrailingZeros (long v);
	public static long Reverse (long v);
	public static long ReverseBytes (long v);
	public static long RotateLeft (long v, int distance);
	public static long RotateRight (long v, int distance);
	public static int Signum (long v);
	public static string ToBinaryString (long v);
	public static string ToHexString (long v);
	public static string ToOctalString (long v);
	public static string ToString (long v, int radix);
	public static string ToString (long n);
	public static Long ValueOf (long v);
```

### Type Changed: Java.Lang.Math

Removed methods:

```
public static double Atan2 (double x, double y);
	public static double CopySign (double p0, double p1);
	public static float CopySign (float p0, float p1);
	public static int GetExponent (float p0);
	public static int GetExponent (double p0);
	public static float NextAfter (float p0, double p1);
	public static double NextAfter (double p0, double p1);
	public static float NextUp (float p0);
	public static double NextUp (double p0);
	public static float Scalb (float p0, int p1);
	public static double Scalb (double p0, int p1);
```

Added methods:

```
public static double Atan2 (double y, double x);
	public static double CopySign (double magnitude, double sign);
	public static float CopySign (float magnitude, float sign);
	public static int GetExponent (float f);
	public static int GetExponent (double d);
	public static float NextAfter (float start, double direction);
	public static double NextAfter (double start, double direction);
	public static float NextUp (float f);
	public static double NextUp (double d);
	public static float Scalb (float d, int scaleFactor);
	public static double Scalb (double d, int scaleFactor);
```

### Type Changed: Java.Lang.Package

Removed method:

```
public virtual Object GetAnnotation (Class p0);
```

Added method:

```
public virtual Object GetAnnotation (Class annotationType);
```

### Type Changed: Java.Lang.StrictMath

Removed methods:

```
public static double CopySign (double p0, double p1);
	public static float CopySign (float p0, float p1);
	public static int GetExponent (float p0);
	public static int GetExponent (double p0);
	public static float NextAfter (float p0, double p1);
	public static double NextAfter (double p0, double p1);
	public static float NextUp (float p0);
	public static double NextUp (double p0);
	public static float Scalb (float p0, int p1);
	public static double Scalb (double p0, int p1);
```

Added methods:

```
public static double CopySign (double magnitude, double sign);
	public static float CopySign (float magnitude, float sign);
	public static int GetExponent (float f);
	public static int GetExponent (double d);
	public static float NextAfter (float start, double direction);
	public static double NextAfter (double start, double direction);
	public static float NextUp (float f);
	public static double NextUp (double d);
	public static float Scalb (float d, int scaleFactor);
	public static double Scalb (double d, int scaleFactor);
```

### Type Changed: Java.Lang.String

Removed constructors:

```
public String (byte[] p0, Java.Nio.Charset.Charset p1);
	public String (char[] data, int start, int length);
	public String (string string);
	public String (StringBuffer stringbuffer);
	public String (byte[] data, string encoding);
	public String (byte[] data, int start, int length);
	public String (byte[] data, int high, int start, int length);
	public String (byte[] data, int start, int length, string encoding);
	public String (byte[] p0, int p1, int p2, Java.Nio.Charset.Charset p3);
	public String (StringBuilder sb);
```

Added constructors:

```
public String (byte[] data, Java.Nio.Charset.Charset charset);
	public String (char[] data, int offset, int charCount);
	public String (string toCopy);
	public String (StringBuffer stringBuffer);
	public String (byte[] data, string charsetName);
	public String (byte[] data, int offset, int byteCount);
	public String (byte[] data, int high, int offset, int byteCount);
	public String (byte[] data, int offset, int byteCount, string charsetName);
	public String (byte[] data, int offset, int byteCount, Java.Nio.Charset.Charset charset);
	public String (StringBuilder stringBuilder);
```

Removed methods:

```
public int CodePointCount (int beginIndex, int endIndex);
	public static string Format (Java.Util.Locale loc, string format, Object[] args);
	public byte[] GetBytes (string encoding);
	public byte[] GetBytes (Java.Nio.Charset.Charset p0);
	public bool Matches (string expr);
	public string ReplaceAll (string expr, string substitute);
	public string ReplaceFirst (string expr, string substitute);
	public string[] Split (string expr);
	public string[] Split (string expr, int max);
```

Added methods:

```
public int CodePointCount (int start, int end);
	public static string Format (Java.Util.Locale locale, string format, Object[] args);
	public byte[] GetBytes (string charsetName);
	public byte[] GetBytes (Java.Nio.Charset.Charset charset);
	public bool Matches (string regularExpression);
	public string ReplaceAll (string regularExpression, string replacement);
	public string ReplaceFirst (string regularExpression, string replacement);
	public string[] Split (string regularExpression);
	public string[] Split (string regularExpression, int limit);
```

### Type Changed: Java.Lang.StringBuilder

Removed methods:

```
public IAppendable Append (long lng);
	public IAppendable Append (char[] ch);
	public override int CodePointCount (int beginIndex, int endIndex);
	public override void GetChars (int start, int end, char[] dest, int destStart);
```

Added methods:

```
public IAppendable Append (long l);
	public IAppendable Append (char[] chars);
	public override int CodePointCount (int start, int end);
	public override void GetChars (int start, int end, char[] dst, int dstStart);
```

## Namespace Java.Lang.Reflect

### Type Changed: Java.Lang.Reflect.Array

Removed method:

```
public static Java.Lang.Object NewInstance (Java.Lang.Class p0, int[] p1);
```

Added method:

```
public static Java.Lang.Object NewInstance (Java.Lang.Class componentType, int[] dimensions);
```

## Namespace Java.Math

### Type Changed: Java.Math.BigInteger

Removed constructors:

```
public BigInteger (byte[] val);
	public BigInteger (int bitLength, int certainty, Java.Util.Random rnd);
	public BigInteger (int numBits, Java.Util.Random rnd);
	public BigInteger (string val);
	public BigInteger (string val, int radix);
```

Added constructors:

```
public BigInteger (byte[] value);
	public BigInteger (int bitLength, int certainty, Java.Util.Random unused);
	public BigInteger (int numBits, Java.Util.Random random);
	public BigInteger (string value);
	public BigInteger (string value, int radix);
```

Removed methods:

```
public virtual BigInteger Add (BigInteger val);
	public virtual BigInteger And (BigInteger val);
	public virtual BigInteger AndNot (BigInteger val);
	public virtual int CompareTo (BigInteger val);
	public virtual BigInteger Gcd (BigInteger val);
	public virtual BigInteger Max (BigInteger val);
	public virtual BigInteger Min (BigInteger val);
	public virtual BigInteger Multiply (BigInteger val);
	public virtual BigInteger Or (BigInteger val);
	public static BigInteger ProbablePrime (int bitLength, Java.Util.Random rnd);
	public virtual BigInteger Subtract (BigInteger val);
	public static BigInteger ValueOf (long val);
	public virtual BigInteger Xor (BigInteger val);
```

Added methods:

```
public virtual BigInteger Add (BigInteger value);
	public virtual BigInteger And (BigInteger value);
	public virtual BigInteger AndNot (BigInteger value);
	public virtual int CompareTo (BigInteger value);
	public virtual BigInteger Gcd (BigInteger value);
	public virtual BigInteger Max (BigInteger value);
	public virtual BigInteger Min (BigInteger value);
	public virtual BigInteger Multiply (BigInteger value);
	public virtual BigInteger Or (BigInteger value);
	public static BigInteger ProbablePrime (int bitLength, Java.Util.Random unused);
	public virtual BigInteger Subtract (BigInteger value);
	public static BigInteger ValueOf (long value);
	public virtual BigInteger Xor (BigInteger value);
```

## Namespace Java.Net

### Type Changed: Java.Net.DatagramPacket

Removed method:

```
public void SetData (byte[] buf, int anOffset, int aLength);
```

Added method:

```
public void SetData (byte[] data, int offset, int byteCount);
```

### Type Changed: Java.Net.DatagramSocket

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Net.HttpURLConnection

Removed method:

```
public virtual void SetChunkedStreamingMode (int chunklen);
```

Added method:

```
public virtual void SetChunkedStreamingMode (int chunkLength);
```

### Type Changed: Java.Net.IFileNameMap

Removed method:

```
public virtual string GetContentTypeFor (string fileName);
```

Added method:

```
public virtual string GetContentTypeFor (string filename);
```

### Type Changed: Java.Net.InetAddress

Removed method:

```
public virtual bool IsReachable (NetworkInterface netif, int ttl, int timeout);
```

Added method:

```
public virtual bool IsReachable (NetworkInterface networkInterface, int ttl, int timeout);
```

### Type Changed: Java.Net.MulticastSocket

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Net.ProxySelector

Removed method:

```
public virtual void ConnectFailed (URI uri, SocketAddress sa, Java.IO.IOException ioe);
```

Added method:

```
public virtual void ConnectFailed (URI uri, SocketAddress address, Java.IO.IOException failure);
```

### Type Changed: Java.Net.ResponseCache

Removed methods:

```
public virtual CacheResponse Get (URI uri, string rqstMethod, System.Collections.Generic.IDictionary<System.String,System.Collections.Generic.IList<string>> rqstHeaders);
	public virtual CacheRequest Put (URI uri, URLConnection conn);
```

Added methods:

```
public virtual CacheResponse Get (URI uri, string requestMethod, System.Collections.Generic.IDictionary<System.String,System.Collections.Generic.IList<string>> requestHeaders);
	public virtual CacheRequest Put (URI uri, URLConnection connection);
```

### Type Changed: Java.Net.ServerSocket

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Net.Socket

Removed constructor:

```
protected Socket (SocketImpl anImpl);
```

Added constructor:

```
protected Socket (SocketImpl impl);
```

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Net.SocketPermission

Removed method:

```
public override bool Equals (Java.Lang.Object o);
```

Added method:

```
public override bool Equals (Java.Lang.Object other);
```

### Type Changed: Java.Net.URI

Removed constructor:

```
public URI (string scheme, string userinfo, string host, int port, string path, string query, string fragment);
```

Added constructor:

```
public URI (string scheme, string userInfo, string host, int port, string path, string query, string fragment);
```

### Type Changed: Java.Net.URLClassLoader

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Net.URLDecoder

Removed method:

```
public static string Decode (string s, string enc);
```

Added method:

```
public static string Decode (string s, string encoding);
```

### Type Changed: Java.Net.URLStreamHandler

Removed method:

```
protected virtual bool HostsEqual (URL url1, URL url2);
```

Added method:

```
protected virtual bool HostsEqual (URL a, URL b);
```

## Namespace Java.Nio

### Type Changed: Java.Nio.ByteBuffer

Removed methods:

```
public virtual ByteBuffer Get (byte[] dest, int off, int len);
	public virtual ByteBuffer Get (byte[] dest);
	public virtual ByteBuffer Put (byte[] src, int off, int len);
	public static ByteBuffer Wrap (byte[] array, int start, int len);
```

Added methods:

```
public virtual ByteBuffer Get (byte[] dst, int dstOffset, int byteCount);
	public virtual ByteBuffer Get (byte[] dst);
	public virtual ByteBuffer Put (byte[] src, int srcOffset, int byteCount);
	public static ByteBuffer Wrap (byte[] array, int start, int byteCount);
```

### Type Changed: Java.Nio.CharBuffer

Removed methods:

```
public virtual CharBuffer Get (char[] dest, int off, int len);
	public virtual CharBuffer Get (char[] dest);
	public virtual CharBuffer Put (char[] src, int off, int len);
	public static CharBuffer Wrap (Java.Lang.ICharSequence chseq, int start, int end);
	public static CharBuffer Wrap (string chseq, int start, int end);
	public static CharBuffer Wrap (char[] array, int start, int len);
```

Added methods:

```
public virtual CharBuffer Get (char[] dst, int dstOffset, int charCount);
	public virtual CharBuffer Get (char[] dst);
	public virtual CharBuffer Put (char[] src, int srcOffset, int charCount);
	public static CharBuffer Wrap (Java.Lang.ICharSequence cs, int start, int end);
	public static CharBuffer Wrap (string cs, int start, int end);
	public static CharBuffer Wrap (char[] array, int start, int charCount);
```

### Type Changed: Java.Nio.DoubleBuffer

Removed methods:

```
public virtual DoubleBuffer Get (double[] dest, int off, int len);
	public virtual DoubleBuffer Get (double[] dest);
	public virtual DoubleBuffer Put (double[] src, int off, int len);
	public static DoubleBuffer Wrap (double[] array, int start, int len);
```

Added methods:

```
public virtual DoubleBuffer Get (double[] dst, int dstOffset, int doubleCount);
	public virtual DoubleBuffer Get (double[] dst);
	public virtual DoubleBuffer Put (double[] src, int srcOffset, int doubleCount);
	public static DoubleBuffer Wrap (double[] array, int start, int doubleCount);
```

### Type Changed: Java.Nio.FloatBuffer

Removed methods:

```
public virtual FloatBuffer Get (float[] dest, int off, int len);
	public virtual FloatBuffer Get (float[] dest);
	public virtual FloatBuffer Put (float[] src, int off, int len);
	public static FloatBuffer Wrap (float[] array, int start, int len);
```

Added methods:

```
public virtual FloatBuffer Get (float[] dst, int dstOffset, int floatCount);
	public virtual FloatBuffer Get (float[] dst);
	public virtual FloatBuffer Put (float[] src, int srcOffset, int floatCount);
	public static FloatBuffer Wrap (float[] array, int start, int floatCount);
```

### Type Changed: Java.Nio.IntBuffer

Removed methods:

```
public virtual IntBuffer Get (int[] dest, int off, int len);
	public virtual IntBuffer Get (int[] dest);
	public virtual IntBuffer Put (int[] src, int off, int len);
	public static IntBuffer Wrap (int[] array, int start, int len);
```

Added methods:

```
public virtual IntBuffer Get (int[] dst, int dstOffset, int intCount);
	public virtual IntBuffer Get (int[] dst);
	public virtual IntBuffer Put (int[] src, int srcOffset, int intCount);
	public static IntBuffer Wrap (int[] array, int start, int intCount);
```

### Type Changed: Java.Nio.LongBuffer

Removed methods:

```
public virtual LongBuffer Get (long[] dest, int off, int len);
	public virtual LongBuffer Get (long[] dest);
	public virtual LongBuffer Put (long[] src, int off, int len);
	public static LongBuffer Wrap (long[] array, int start, int len);
```

Added methods:

```
public virtual LongBuffer Get (long[] dst, int dstOffset, int longCount);
	public virtual LongBuffer Get (long[] dst);
	public virtual LongBuffer Put (long[] src, int srcOffset, int longCount);
	public static LongBuffer Wrap (long[] array, int start, int longCount);
```

### Type Changed: Java.Nio.ShortBuffer

Removed methods:

```
public virtual ShortBuffer Get (short[] dest, int off, int len);
	public virtual ShortBuffer Get (short[] dest);
	public virtual ShortBuffer Put (short[] src, int off, int len);
	public static ShortBuffer Wrap (short[] array, int start, int len);
```

Added methods:

```
public virtual ShortBuffer Get (short[] dst, int dstOffset, int shortCount);
	public virtual ShortBuffer Get (short[] dst);
	public virtual ShortBuffer Put (short[] src, int srcOffset, int shortCount);
	public static ShortBuffer Wrap (short[] array, int start, int shortCount);
```

## Namespace Java.Nio.Channels

### Type Changed: Java.Nio.Channels.Channels

Added properties:

```
protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
```

Added methods:

```
public static System.IO.Stream NewInputStream (IReadableByteChannel channel);
	public static System.IO.Stream NewOutputStream (IWritableByteChannel channel);
	public static IReadableByteChannel NewReadableChannel (System.IO.Stream inputStream);
	public static Java.IO.Reader NewReader (IReadableByteChannel channel, string charsetName);
	public static Java.IO.Reader NewReader (IReadableByteChannel channel, Java.Nio.Charset.CharsetDecoder decoder, int minBufferCapacity);
	public static IWritableByteChannel NewWritableChannel (System.IO.Stream outputStream);
	public static Java.IO.Writer NewWriter (IWritableByteChannel channel, string charsetName);
	public static Java.IO.Writer NewWriter (IWritableByteChannel channel, Java.Nio.Charset.CharsetEncoder encoder, int minBufferCapacity);
```

### Type Changed: Java.Nio.Channels.DatagramChannel

Added interfaces:

```
IByteChannel
	IGatheringByteChannel
	IScatteringByteChannel
	IReadableByteChannel
	IWritableByteChannel
	IChannel
	Java.IO.ICloseable
	IInterruptibleChannel
```

Removed methods:

```
public long Read (Java.Nio.ByteBuffer[] targets);
	public long Write (Java.Nio.ByteBuffer[] sources);
```

Added methods:

```
public virtual long Read (Java.Nio.ByteBuffer[] targets);
	public virtual long Write (Java.Nio.ByteBuffer[] sources);
```

### Type Changed: Java.Nio.Channels.FileChannel

Added interfaces:

```
IGatheringByteChannel
	IScatteringByteChannel
	IWritableByteChannel
	IChannel
	Java.IO.ICloseable
	IReadableByteChannel
	IInterruptibleChannel
```

Removed methods:

```
public long Read (Java.Nio.ByteBuffer[] buffers);
	public long Write (Java.Nio.ByteBuffer[] buffers);
```

Added methods:

```
public virtual long Read (Java.Nio.ByteBuffer[] buffers);
	public virtual long TransferFrom (IReadableByteChannel src, long position, long count);
	public System.Threading.Tasks.Task<long> TransferFromAsync (IReadableByteChannel src, long position, long count);
	public virtual long TransferTo (long position, long count, IWritableByteChannel target);
	public System.Threading.Tasks.Task<long> TransferToAsync (long position, long count, IWritableByteChannel target);
	public virtual long Write (Java.Nio.ByteBuffer[] buffers);
```

### Type Changed: Java.Nio.Channels.FileLock

Added method:

```
public virtual IChannel AcquiredBy ();
```

### Type Changed: Java.Nio.Channels.Pipe

### Type Changed: Java.Nio.Channels.Pipe.SinkChannel

Added interfaces:

```
IGatheringByteChannel
	IWritableByteChannel
	IChannel
	Java.IO.ICloseable
	IInterruptibleChannel
```

Added methods:

```
public virtual long Write (Java.Nio.ByteBuffer[] buffers);
	public virtual long Write (Java.Nio.ByteBuffer[] buffers, int offset, int length);
	public virtual int Write (Java.Nio.ByteBuffer buffer);
	public System.Threading.Tasks.Task<long> WriteAsync (Java.Nio.ByteBuffer[] buffers);
	public System.Threading.Tasks.Task<long> WriteAsync (Java.Nio.ByteBuffer[] buffers, int offset, int length);
	public System.Threading.Tasks.Task<int> WriteAsync (Java.Nio.ByteBuffer buffer);
```

### Type Changed: Java.Nio.Channels.Pipe.SourceChannel

Added interfaces:

```
IReadableByteChannel
	IScatteringByteChannel
	IChannel
	Java.IO.ICloseable
	IInterruptibleChannel
```

Added methods:

```
public virtual int Read (Java.Nio.ByteBuffer buffer);
	public virtual long Read (Java.Nio.ByteBuffer[] buffers);
	public virtual long Read (Java.Nio.ByteBuffer[] buffers, int offset, int length);
	public System.Threading.Tasks.Task<int> ReadAsync (Java.Nio.ByteBuffer buffer);
	public System.Threading.Tasks.Task<long> ReadAsync (Java.Nio.ByteBuffer[] buffers);
	public System.Threading.Tasks.Task<long> ReadAsync (Java.Nio.ByteBuffer[] buffers, int offset, int length);
```

### Type Changed: Java.Nio.Channels.SelectableChannel

Added interfaces:

```
IChannel
	Java.IO.ICloseable
	IInterruptibleChannel
```

### Type Changed: Java.Nio.Channels.Selector

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Nio.Channels.ServerSocketChannel

Added interfaces:

```
IChannel
	Java.IO.ICloseable
	IInterruptibleChannel
```

### Type Changed: Java.Nio.Channels.SocketChannel

Added interfaces:

```
IByteChannel
	IGatheringByteChannel
	IScatteringByteChannel
	IReadableByteChannel
	IWritableByteChannel
	IChannel
	Java.IO.ICloseable
	IInterruptibleChannel
```

Removed methods:

```
public long Read (Java.Nio.ByteBuffer[] targets);
	public long Write (Java.Nio.ByteBuffer[] sources);
```

Added methods:

```
public virtual long Read (Java.Nio.ByteBuffer[] targets);
	public virtual long Write (Java.Nio.ByteBuffer[] sources);
```

### New Type Java.Nio.Channels.IByteChannel

```
public interface IByteChannel : IReadableByteChannel, IWritableByteChannel, IChannel, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
}
```

### New Type Java.Nio.Channels.IChannel

```
public interface IChannel : Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual bool IsOpen { get; }
	// methods
	public virtual void Close ();
}
```

### New Type Java.Nio.Channels.IGatheringByteChannel

```
public interface IGatheringByteChannel : IWritableByteChannel, IChannel, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual long Write (Java.Nio.ByteBuffer[] buffers);
	public virtual long Write (Java.Nio.ByteBuffer[] buffers, int offset, int length);
}
```

### New Type Java.Nio.Channels.IGatheringByteChannelExtensions

```
public static class IGatheringByteChannelExtensions {
	// methods
	public static System.Threading.Tasks.Task<long> WriteAsync (IGatheringByteChannel self, Java.Nio.ByteBuffer[] buffers);
	public static System.Threading.Tasks.Task<long> WriteAsync (IGatheringByteChannel self, Java.Nio.ByteBuffer[] buffers, int offset, int length);
}
```

### New Type Java.Nio.Channels.IInterruptibleChannel

```
public interface IInterruptibleChannel : IChannel, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void Close ();
}
```

### New Type Java.Nio.Channels.IReadableByteChannel

```
public interface IReadableByteChannel : IChannel, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual int Read (Java.Nio.ByteBuffer buffer);
}
```

### New Type Java.Nio.Channels.IReadableByteChannelExtensions

```
public static class IReadableByteChannelExtensions {
	// methods
	public static System.Threading.Tasks.Task<int> ReadAsync (IReadableByteChannel self, Java.Nio.ByteBuffer buffer);
}
```

### New Type Java.Nio.Channels.IScatteringByteChannel

```
public interface IScatteringByteChannel : IReadableByteChannel, IChannel, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual long Read (Java.Nio.ByteBuffer[] buffers);
	public virtual long Read (Java.Nio.ByteBuffer[] buffers, int offset, int length);
}
```

### New Type Java.Nio.Channels.IScatteringByteChannelExtensions

```
public static class IScatteringByteChannelExtensions {
	// methods
	public static System.Threading.Tasks.Task<long> ReadAsync (IScatteringByteChannel self, Java.Nio.ByteBuffer[] buffers);
	public static System.Threading.Tasks.Task<long> ReadAsync (IScatteringByteChannel self, Java.Nio.ByteBuffer[] buffers, int offset, int length);
}
```

### New Type Java.Nio.Channels.IWritableByteChannel

```
public interface IWritableByteChannel : IChannel, Java.IO.ICloseable, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual int Write (Java.Nio.ByteBuffer buffer);
}
```

### New Type Java.Nio.Channels.IWritableByteChannelExtensions

```
public static class IWritableByteChannelExtensions {
	// methods
	public static System.Threading.Tasks.Task<int> WriteAsync (IWritableByteChannel self, Java.Nio.ByteBuffer buffer);
}
```

## Namespace Java.Nio.Channels.Spi

### Type Changed: Java.Nio.Channels.Spi.AbstractInterruptibleChannel

Added interfaces:

```
Java.Nio.Channels.IChannel
	Java.Nio.Channels.IInterruptibleChannel
	Java.IO.ICloseable
```

Removed property:

```
public bool IsOpen { get; }
```

Added property:

```
public virtual bool IsOpen { get; }
```

Removed method:

```
public void Close ();
```

Added method:

```
public virtual void Close ();
```

### Type Changed: Java.Nio.Channels.Spi.AbstractSelectableChannel

Added interfaces:

```
Java.Nio.Channels.IChannel
	Java.IO.ICloseable
	Java.Nio.Channels.IInterruptibleChannel
```

### Type Changed: Java.Nio.Channels.Spi.AbstractSelector

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Nio.Channels.Spi.SelectorProvider

Added method:

```
public virtual Java.Nio.Channels.IChannel InheritedChannel ();
```

## Namespace Java.Nio.Charset

### Type Changed: Java.Nio.Charset.CharsetEncoder

Removed method:

```
public virtual bool IsLegalReplacement (byte[] repl);
```

Added method:

```
public virtual bool IsLegalReplacement (byte[] replacement);
```

### Type Changed: Java.Nio.Charset.IllegalCharsetNameException

Removed constructor:

```
public IllegalCharsetNameException (string charset);
```

Added constructor:

```
public IllegalCharsetNameException (string charsetName);
```

### Type Changed: Java.Nio.Charset.UnsupportedCharsetException

Removed constructor:

```
public UnsupportedCharsetException (string charset);
```

Added constructor:

```
public UnsupportedCharsetException (string charsetName);
```

## Namespace Java.Security

### Type Changed: Java.Security.AccessController

Removed methods:

```
public static void CheckPermission (Permission perm);
	public static Java.Lang.Object DoPrivilegedWithCombiner (IPrivilegedAction p0);
	public static Java.Lang.Object DoPrivilegedWithCombiner (IPrivilegedExceptionAction p0);
```

Added methods:

```
public static void CheckPermission (Permission permission);
	public static Java.Lang.Object DoPrivilegedWithCombiner (IPrivilegedAction action);
	public static Java.Lang.Object DoPrivilegedWithCombiner (IPrivilegedExceptionAction action);
```

### Type Changed: Java.Security.DigestInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Security.DigestOutputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Security.Policy

Removed methods:

```
public static Policy GetInstance (string p0, Policy.IParameters p1);
	public static Policy GetInstance (string p0, Policy.IParameters p1, string p2);
	public static Policy GetInstance (string p0, Policy.IParameters p1, Provider p2);
```

Added methods:

```
public static Policy GetInstance (string type, Policy.IParameters params);
	public static Policy GetInstance (string type, Policy.IParameters params, string provider);
	public static Policy GetInstance (string type, Policy.IParameters params, Provider provider);
```

## Namespace Java.Sql

### Type Changed: Java.Sql.BatchUpdateException

Removed constructors:

```
public BatchUpdateException (string p0, string p1, int[] p2, Java.Lang.Throwable p3);
	public BatchUpdateException (string p0, string p1, int p2, int[] p3, Java.Lang.Throwable p4);
	public BatchUpdateException (string p0, int[] p1, Java.Lang.Throwable p2);
	public BatchUpdateException (int[] p0, Java.Lang.Throwable p1);
	public BatchUpdateException (Java.Lang.Throwable p0);
```

Added constructors:

```
public BatchUpdateException (string reason, string SQLState, int[] updateCounts, Java.Lang.Throwable cause);
	public BatchUpdateException (string reason, string SQLState, int vendorCode, int[] updateCounts, Java.Lang.Throwable cause);
	public BatchUpdateException (string reason, int[] updateCounts, Java.Lang.Throwable cause);
	public BatchUpdateException (int[] updateCounts, Java.Lang.Throwable cause);
	public BatchUpdateException (Java.Lang.Throwable cause);
```

### Type Changed: Java.Sql.DataTruncation

Removed constructor:

```
public DataTruncation (int p0, bool p1, bool p2, int p3, int p4, Java.Lang.Throwable p5);
```

Added constructor:

```
public DataTruncation (int index, bool parameter, bool read, int dataSize, int transferSize, Java.Lang.Throwable cause);
```

### Type Changed: Java.Sql.DriverManager

Added property:

```
public static Java.Util.IEnumeration Drivers { get; }
```

Added methods:

```
public static void DeregisterDriver (IDriver driver);
	public static IConnection GetConnection (string url, Java.Util.Properties info);
	public static IConnection GetConnection (string url, string user, string password);
	public static IConnection GetConnection (string url);
	public static IDriver GetDriver (string url);
	public static void RegisterDriver (IDriver driver);
```

### Type Changed: Java.Sql.IBlob

Removed method:

```
public virtual System.IO.Stream GetBinaryStream (long p0, long p1);
```

Added method:

```
public virtual System.IO.Stream GetBinaryStream (long pos, long length);
```

### Type Changed: Java.Sql.IClob

Removed method:

```
public virtual Java.IO.Reader GetCharacterStream (long p0, long p1);
```

Added method:

```
public virtual Java.IO.Reader GetCharacterStream (long pos, long length);
```

### Type Changed: Java.Sql.SQLException

Removed constructors:

```
public SQLException (string p0, Java.Lang.Throwable p1);
	public SQLException (string p0, string p1, Java.Lang.Throwable p2);
	public SQLException (string p0, string p1, int p2, Java.Lang.Throwable p3);
	public SQLException (Java.Lang.Throwable p0);
```

Added constructors:

```
public SQLException (string theReason, Java.Lang.Throwable theCause);
	public SQLException (string theReason, string theSQLState, Java.Lang.Throwable theCause);
	public SQLException (string theReason, string theSQLState, int theErrorCode, Java.Lang.Throwable theCause);
	public SQLException (Java.Lang.Throwable theCause);
```

### Type Changed: Java.Sql.SQLWarning

Removed constructors:

```
public SQLWarning (string p0, Java.Lang.Throwable p1);
	public SQLWarning (string p0, string p1, Java.Lang.Throwable p2);
	public SQLWarning (string p0, string p1, int p2, Java.Lang.Throwable p3);
	public SQLWarning (Java.Lang.Throwable p0);
```

Added constructors:

```
public SQLWarning (string reason, Java.Lang.Throwable cause);
	public SQLWarning (string reason, string SQLState, Java.Lang.Throwable cause);
	public SQLWarning (string reason, string SQLState, int vendorCode, Java.Lang.Throwable cause);
	public SQLWarning (Java.Lang.Throwable cause);
```

### New Type Java.Sql.Connection

```
public abstract class Connection {
	// fields
	public static const int TransactionNone;
	public static const int TransactionReadCommitted;
	public static const int TransactionReadUncommitted;
	public static const int TransactionRepeatableRead;
	public static const int TransactionSerializable;
}
```

### New Type Java.Sql.ConnectionConsts

```
public abstract class ConnectionConsts : Java.Sql.Connection {
}
```

### New Type Java.Sql.DatabaseMetaData

```
public abstract class DatabaseMetaData {
	// fields
	public static const short AttributeNoNulls;
	public static const short AttributeNullable;
	public static const short AttributeNullableUnknown;
	public static const int BestRowNotPseudo;
	public static const int BestRowPseudo;
	public static const int BestRowSession;
	public static const int BestRowTemporary;
	public static const int BestRowTransaction;
	public static const int BestRowUnknown;
	public static const int ColumnNoNulls;
	public static const int ColumnNullable;
	public static const int ColumnNullableUnknown;
	public static const int ImportedKeyCascade;
	public static const int ImportedKeyInitiallyDeferred;
	public static const int ImportedKeyInitiallyImmediate;
	public static const int ImportedKeyNoAction;
	public static const int ImportedKeyNotDeferrable;
	public static const int ImportedKeyRestrict;
	public static const int ImportedKeySetDefault;
	public static const int ImportedKeySetNull;
	public static const int ProcedureColumnIn;
	public static const int ProcedureColumnInOut;
	public static const int ProcedureColumnOut;
	public static const int ProcedureColumnResult;
	public static const int ProcedureColumnReturn;
	public static const int ProcedureColumnUnknown;
	public static const int ProcedureNoNulls;
	public static const int ProcedureNoResult;
	public static const int ProcedureNullable;
	public static const int ProcedureNullableUnknown;
	public static const int ProcedureResultUnknown;
	public static const int ProcedureReturnsResult;
	public static const int SqlStateSQL99;
	public static const int SqlStateXOpen;
	public static const short TableIndexClustered;
	public static const short TableIndexHashed;
	public static const short TableIndexOther;
	public static const short TableIndexStatistic;
	public static const int TypeNoNulls;
	public static const int TypeNullable;
	public static const int TypeNullableUnknown;
	public static const int TypePredBasic;
	public static const int TypePredChar;
	public static const int TypePredNone;
	public static const int TypeSearchable;
	public static const int VersionColumnNotPseudo;
	public static const int VersionColumnPseudo;
	public static const int VersionColumnUnknown;
	// properties
	public static int FunctionColumnIn { get; set; }
	public static int FunctionColumnInOut { get; set; }
	public static int FunctionColumnOut { get; set; }
	public static int FunctionColumnResult { get; set; }
	public static int FunctionColumnUnknown { get; set; }
	public static int FunctionNoNulls { get; set; }
	public static int FunctionNoTable { get; set; }
	public static int FunctionNullable { get; set; }
	public static int FunctionNullableUnknown { get; set; }
	public static int FunctionResultUnknown { get; set; }
	public static int FunctionReturn { get; set; }
	public static int FunctionReturnsTable { get; set; }
	public static int SqlStateSQL { get; set; }
}
```

### New Type Java.Sql.DatabaseMetaDataConsts

```
public abstract class DatabaseMetaDataConsts : Java.Sql.DatabaseMetaData {
}
```

### New Type Java.Sql.IArray

```
public interface IArray : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual Java.Lang.Object Array { get; }
	public virtual int BaseType { get; }
	public virtual string BaseTypeName { get; }
	public virtual IResultSet ResultSet { get; }
	// methods
	public virtual void Free ();
	public virtual Java.Lang.Object GetArray (System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> map);
	public virtual Java.Lang.Object GetArray (long index, int count);
	public virtual Java.Lang.Object GetArray (long index, int count, System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> map);
	public virtual IResultSet GetResultSet (System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> map);
	public virtual IResultSet GetResultSet (long index, int count);
	public virtual IResultSet GetResultSet (long index, int count, System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> map);
}
```

### New Type Java.Sql.ICallableStatement

```
public interface ICallableStatement : IPreparedStatement, IStatement, IWrapper, Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual IArray GetArray (int parameterIndex);
	public virtual IArray GetArray (string parameterName);
	public virtual Java.Math.BigDecimal GetBigDecimal (int parameterIndex);

	[Obsolete ("deprecated")]
	public virtual Java.Math.BigDecimal GetBigDecimal (int parameterIndex, int scale);
	public virtual Java.Math.BigDecimal GetBigDecimal (string parameterName);
	public virtual IBlob GetBlob (string parameterName);
	public virtual IBlob GetBlob (int parameterIndex);
	public virtual bool GetBoolean (int parameterIndex);
	public virtual bool GetBoolean (string parameterName);
	public virtual sbyte GetByte (string parameterName);
	public virtual sbyte GetByte (int parameterIndex);
	public virtual byte[] GetBytes (int parameterIndex);
	public virtual byte[] GetBytes (string parameterName);
	public virtual Java.IO.Reader GetCharacterStream (string parameterName);
	public virtual Java.IO.Reader GetCharacterStream (int parameterIndex);
	public virtual IClob GetClob (int parameterIndex);
	public virtual IClob GetClob (string parameterName);
	public virtual Date GetDate (string parameterName, Java.Util.Calendar cal);
	public virtual Date GetDate (string parameterName);
	public virtual Date GetDate (int parameterIndex, Java.Util.Calendar cal);
	public virtual Date GetDate (int parameterIndex);
	public virtual double GetDouble (string parameterName);
	public virtual double GetDouble (int parameterIndex);
	public virtual float GetFloat (int parameterIndex);
	public virtual float GetFloat (string parameterName);
	public virtual int GetInt (int parameterIndex);
	public virtual int GetInt (string parameterName);
	public virtual long GetLong (string parameterName);
	public virtual long GetLong (int parameterIndex);
	public virtual Java.IO.Reader GetNCharacterStream (int parameterIndex);
	public virtual Java.IO.Reader GetNCharacterStream (string parameterName);
	public virtual INClob GetNClob (int parameterIndex);
	public virtual INClob GetNClob (string parameterName);
	public virtual string GetNString (string parameterName);
	public virtual string GetNString (int parameterIndex);
	public virtual Java.Lang.Object GetObject (string parameterName, System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> map);
	public virtual Java.Lang.Object GetObject (string p0, Java.Lang.Class p1);
	public virtual Java.Lang.Object GetObject (string parameterName);
	public virtual Java.Lang.Object GetObject (int parameterIndex, System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> map);
	public virtual Java.Lang.Object GetObject (int p0, Java.Lang.Class p1);
	public virtual Java.Lang.Object GetObject (int parameterIndex);
	public virtual IRef GetRef (string parameterName);
	public virtual IRef GetRef (int parameterIndex);
	public virtual IRowId GetRowId (int parameterIndex);
	public virtual IRowId GetRowId (string parameterName);
	public virtual short GetShort (int parameterIndex);
	public virtual short GetShort (string parameterName);
	public virtual ISQLXML GetSQLXML (string parameterName);
	public virtual ISQLXML GetSQLXML (int parameterIndex);
	public virtual string GetString (int parameterIndex);
	public virtual string GetString (string parameterName);
	public virtual Time GetTime (string parameterName, Java.Util.Calendar cal);
	public virtual Time GetTime (string parameterName);
	public virtual Time GetTime (int parameterIndex, Java.Util.Calendar cal);
	public virtual Time GetTime (int parameterIndex);
	public virtual Timestamp GetTimestamp (string parameterName, Java.Util.Calendar cal);
	public virtual Timestamp GetTimestamp (string parameterName);
	public virtual Timestamp GetTimestamp (int parameterIndex, Java.Util.Calendar cal);
	public virtual Timestamp GetTimestamp (int parameterIndex);
	public virtual Java.Net.URL GetURL (string parameterName);
	public virtual Java.Net.URL GetURL (int parameterIndex);
	public virtual void RegisterOutParameter (string parameterName, int sqlType, string typeName);
	public virtual void RegisterOutParameter (string parameterName, int sqlType, int scale);
	public virtual void RegisterOutParameter (string parameterName, int sqlType);
	public virtual void RegisterOutParameter (int parameterIndex, int sqlType);
	public virtual void RegisterOutParameter (int parameterIndex, int sqlType, int scale);
	public virtual void RegisterOutParameter (int paramIndex, int sqlType, string typeName);
	public virtual void SetAsciiStream (string parameterName, System.IO.Stream x);
	public virtual void SetAsciiStream (string parameterName, System.IO.Stream theInputStream, int length);
	public virtual void SetAsciiStream (string parameterName, System.IO.Stream x, long length);
	public virtual void SetBigDecimal (string parameterName, Java.Math.BigDecimal theBigDecimal);
	public virtual void SetBinaryStream (string parameterName, System.IO.Stream x, long length);
	public virtual void SetBinaryStream (string parameterName, System.IO.Stream theInputStream, int length);
	public virtual void SetBinaryStream (string parameterName, System.IO.Stream x);
	public virtual void SetBlob (string parameterName, System.IO.Stream inputStream);
	public virtual void SetBlob (string parameterName, System.IO.Stream inputStream, long length);
	public virtual void SetBlob (string parameterName, IBlob blob);
	public virtual void SetBoolean (string parameterName, bool theBoolean);
	public virtual void SetByte (string parameterName, sbyte theByte);
	public virtual void SetBytes (string parameterName, byte[] theBytes);
	public virtual void SetCharacterStream (string parameterName, Java.IO.Reader reader, long length);
	public virtual void SetCharacterStream (string parameterName, Java.IO.Reader reader, int length);
	public virtual void SetCharacterStream (string parameterName, Java.IO.Reader reader);
	public virtual void SetClob (string parameterName, IClob clob);
	public virtual void SetClob (string parameterName, Java.IO.Reader reader, long length);
	public virtual void SetClob (string parameterName, Java.IO.Reader reader);
	public virtual void SetDate (string parameterName, Date theDate, Java.Util.Calendar cal);
	public virtual void SetDate (string parameterName, Date theDate);
	public virtual void SetDouble (string parameterName, double theDouble);
	public virtual void SetFloat (string parameterName, float theFloat);
	public virtual void SetInt (string parameterName, int theInt);
	public virtual void SetLong (string parameterName, long theLong);
	public virtual void SetNCharacterStream (string parameterName, Java.IO.Reader value);
	public virtual void SetNCharacterStream (string parameterName, Java.IO.Reader reader, long length);
	public virtual void SetNClob (string parameterName, INClob nclob);
	public virtual void SetNClob (string parameterName, Java.IO.Reader reader, long length);
	public virtual void SetNClob (string parameterName, Java.IO.Reader reader);
	public virtual void SetNString (string parameterName, string string);
	public virtual void SetNull (string parameterName, int sqlType, string typeName);
	public virtual void SetNull (string parameterName, int sqlType);
	public virtual void SetObject (string parameterName, Java.Lang.Object theObject, int targetSqlType, int scale);
	public virtual void SetObject (string parameterName, Java.Lang.Object theObject, int targetSqlType);
	public virtual void SetObject (string parameterName, Java.Lang.Object theObject);
	public virtual void SetRowId (string parameterName, IRowId rowId);
	public virtual void SetShort (string parameterName, short theShort);
	public virtual void SetSQLXML (string parameterName, ISQLXML sqlXml);
	public virtual void SetString (string parameterName, string theString);
	public virtual void SetTime (string parameterName, Time theTime, Java.Util.Calendar cal);
	public virtual void SetTime (string parameterName, Time theTime);
	public virtual void SetTimestamp (string parameterName, Timestamp theTimestamp);
	public virtual void SetTimestamp (string parameterName, Timestamp theTimestamp, Java.Util.Calendar cal);
	public virtual void SetURL (string parameterName, Java.Net.URL theURL);
	public virtual bool WasNull ();
}
```

### New Type Java.Sql.IConnection

```
public interface IConnection : IWrapper, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual bool AutoCommit { get; set; }
	public virtual string Catalog { get; set; }
	public virtual Java.Util.Properties ClientInfo { get; set; }
	public virtual int Holdability { get; set; }
	public virtual bool IsClosed { get; }
	public virtual IDatabaseMetaData MetaData { get; }
	public virtual int NetworkTimeout { get; }
	public virtual bool ReadOnly { get; set; }
	public virtual string Schema { get; set; }
	public virtual int TransactionIsolation { get; set; }
	public virtual System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> TypeMap { get; set; }
	public virtual SQLWarning Warnings { get; }
	// methods
	public virtual void Abort (Java.Util.Concurrent.IExecutor p0);
	public virtual void ClearWarnings ();
	public virtual void Close ();
	public virtual void Commit ();
	public virtual IArray CreateArrayOf (string typeName, Java.Lang.Object[] elements);
	public virtual IBlob CreateBlob ();
	public virtual IClob CreateClob ();
	public virtual INClob CreateNClob ();
	public virtual ISQLXML CreateSQLXML ();
	public virtual IStatement CreateStatement (int resultSetType, int resultSetConcurrency, int resultSetHoldability);
	public virtual IStatement CreateStatement (int resultSetType, int resultSetConcurrency);
	public virtual IStatement CreateStatement ();
	public virtual IStruct CreateStruct (string typeName, Java.Lang.Object[] attributes);
	public virtual string GetClientInfo (string name);
	public virtual bool IsValid (int timeout);
	public virtual string NativeSQL (string sql);
	public virtual ICallableStatement PrepareCall (string sql);
	public virtual ICallableStatement PrepareCall (string sql, int resultSetType, int resultSetConcurrency);
	public virtual ICallableStatement PrepareCall (string sql, int resultSetType, int resultSetConcurrency, int resultSetHoldability);
	public virtual IPreparedStatement PrepareStatement (string sql, string[] columnNames);
	public virtual IPreparedStatement PrepareStatement (string sql, int[] columnIndexes);
	public virtual IPreparedStatement PrepareStatement (string sql, int resultSetType, int resultSetConcurrency, int resultSetHoldability);
	public virtual IPreparedStatement PrepareStatement (string sql, int resultSetType, int resultSetConcurrency);
	public virtual IPreparedStatement PrepareStatement (string sql, int autoGeneratedKeys);
	public virtual IPreparedStatement PrepareStatement (string sql);
	public virtual void ReleaseSavepoint (ISavepoint savepoint);
	public virtual void Rollback (ISavepoint savepoint);
	public virtual void Rollback ();
	public virtual void SetClientInfo (string name, string value);
	public virtual void SetNetworkTimeout (Java.Util.Concurrent.IExecutor p0, int p1);
	public virtual ISavepoint SetSavepoint ();
	public virtual ISavepoint SetSavepoint (string name);
}
```

### New Type Java.Sql.IDatabaseMetaData

```
public interface IDatabaseMetaData : IWrapper, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual IResultSet Catalogs { get; }
	public virtual string CatalogSeparator { get; }
	public virtual string CatalogTerm { get; }
	public virtual IResultSet ClientInfoProperties { get; }
	public virtual IConnection Connection { get; }
	public virtual int DatabaseMajorVersion { get; }
	public virtual int DatabaseMinorVersion { get; }
	public virtual string DatabaseProductName { get; }
	public virtual string DatabaseProductVersion { get; }
	public virtual int DefaultTransactionIsolation { get; }
	public virtual int DriverMajorVersion { get; }
	public virtual int DriverMinorVersion { get; }
	public virtual string DriverName { get; }
	public virtual string DriverVersion { get; }
	public virtual string ExtraNameCharacters { get; }
	public virtual string IdentifierQuoteString { get; }
	public virtual bool IsCatalogAtStart { get; }
	public virtual bool IsReadOnly { get; }
	public virtual int JDBCMajorVersion { get; }
	public virtual int JDBCMinorVersion { get; }
	public virtual int MaxBinaryLiteralLength { get; }
	public virtual int MaxCatalogNameLength { get; }
	public virtual int MaxCharLiteralLength { get; }
	public virtual int MaxColumnNameLength { get; }
	public virtual int MaxColumnsInGroupBy { get; }
	public virtual int MaxColumnsInIndex { get; }
	public virtual int MaxColumnsInOrderBy { get; }
	public virtual int MaxColumnsInSelect { get; }
	public virtual int MaxColumnsInTable { get; }
	public virtual int MaxConnections { get; }
	public virtual int MaxCursorNameLength { get; }
	public virtual int MaxIndexLength { get; }
	public virtual int MaxProcedureNameLength { get; }
	public virtual int MaxRowSize { get; }
	public virtual int MaxSchemaNameLength { get; }
	public virtual int MaxStatementLength { get; }
	public virtual int MaxStatements { get; }
	public virtual int MaxTableNameLength { get; }
	public virtual int MaxTablesInSelect { get; }
	public virtual int MaxUserNameLength { get; }
	public virtual string NumericFunctions { get; }
	public virtual string ProcedureTerm { get; }
	public virtual int ResultSetHoldability { get; }
	public virtual RowIdLifetime RowIdLifetime { get; }
	public virtual IResultSet Schemas { get; }
	public virtual string SchemaTerm { get; }
	public virtual string SearchStringEscape { get; }
	public virtual string SQLKeywords { get; }
	public virtual int SQLStateType { get; }
	public virtual string StringFunctions { get; }
	public virtual string SystemFunctions { get; }
	public virtual IResultSet TableTypes { get; }
	public virtual string TimeDateFunctions { get; }
	public virtual IResultSet TypeInfo { get; }
	public virtual string URL { get; }
	public virtual string UserName { get; }
	// methods
	public virtual bool AllProceduresAreCallable ();
	public virtual bool AllTablesAreSelectable ();
	public virtual bool AutoCommitFailureClosesAllResultSets ();
	public virtual bool DataDefinitionCausesTransactionCommit ();
	public virtual bool DataDefinitionIgnoredInTransactions ();
	public virtual bool DeletesAreDetected (int type);
	public virtual bool DoesMaxRowSizeIncludeBlobs ();
	public virtual bool GeneratedKeyAlwaysReturned ();
	public virtual IResultSet GetAttributes (string catalog, string schemaPattern, string typeNamePattern, string attributeNamePattern);
	public virtual IResultSet GetBestRowIdentifier (string catalog, string schema, string table, int scope, bool nullable);
	public virtual IResultSet GetColumnPrivileges (string catalog, string schema, string table, string columnNamePattern);
	public virtual IResultSet GetColumns (string catalog, string schemaPattern, string tableNamePattern, string columnNamePattern);
	public virtual IResultSet GetCrossReference (string primaryCatalog, string primarySchema, string primaryTable, string foreignCatalog, string foreignSchema, string foreignTable);
	public virtual IResultSet GetExportedKeys (string catalog, string schema, string table);
	public virtual IResultSet GetFunctionColumns (string catalog, string schemaPattern, string functionNamePattern, string columnNamePattern);
	public virtual IResultSet GetFunctions (string catalog, string schemaPattern, string functionNamePattern);
	public virtual IResultSet GetImportedKeys (string catalog, string schema, string table);
	public virtual IResultSet GetIndexInfo (string catalog, string schema, string table, bool unique, bool approximate);
	public virtual IResultSet GetPrimaryKeys (string catalog, string schema, string table);
	public virtual IResultSet GetProcedureColumns (string catalog, string schemaPattern, string procedureNamePattern, string columnNamePattern);
	public virtual IResultSet GetProcedures (string catalog, string schemaPattern, string procedureNamePattern);
	public virtual IResultSet GetPseudoColumns (string p0, string p1, string p2, string p3);
	public virtual IResultSet GetSchemas (string catalog, string schemaPattern);
	public virtual IResultSet GetSuperTables (string catalog, string schemaPattern, string tableNamePattern);
	public virtual IResultSet GetSuperTypes (string catalog, string schemaPattern, string typeNamePattern);
	public virtual IResultSet GetTablePrivileges (string catalog, string schemaPattern, string tableNamePattern);
	public virtual IResultSet GetTables (string catalog, string schemaPattern, string tableNamePattern, string[] types);
	public virtual IResultSet GetUDTs (string catalog, string schemaPattern, string typeNamePattern, int[] types);
	public virtual IResultSet GetVersionColumns (string catalog, string schema, string table);
	public virtual bool InsertsAreDetected (int type);
	public virtual bool LocatorsUpdateCopy ();
	public virtual bool NullPlusNonNullIsNull ();
	public virtual bool NullsAreSortedAtEnd ();
	public virtual bool NullsAreSortedAtStart ();
	public virtual bool NullsAreSortedHigh ();
	public virtual bool NullsAreSortedLow ();
	public virtual bool OthersDeletesAreVisible (int type);
	public virtual bool OthersInsertsAreVisible (int type);
	public virtual bool OthersUpdatesAreVisible (int type);
	public virtual bool OwnDeletesAreVisible (int type);
	public virtual bool OwnInsertsAreVisible (int type);
	public virtual bool OwnUpdatesAreVisible (int type);
	public virtual bool StoresLowerCaseIdentifiers ();
	public virtual bool StoresLowerCaseQuotedIdentifiers ();
	public virtual bool StoresMixedCaseIdentifiers ();
	public virtual bool StoresMixedCaseQuotedIdentifiers ();
	public virtual bool StoresUpperCaseIdentifiers ();
	public virtual bool StoresUpperCaseQuotedIdentifiers ();
	public virtual bool SupportsAlterTableWithAddColumn ();
	public virtual bool SupportsAlterTableWithDropColumn ();
	public virtual bool SupportsANSI92EntryLevelSQL ();
	public virtual bool SupportsANSI92FullSQL ();
	public virtual bool SupportsANSI92IntermediateSQL ();
	public virtual bool SupportsBatchUpdates ();
	public virtual bool SupportsCatalogsInDataManipulation ();
	public virtual bool SupportsCatalogsInIndexDefinitions ();
	public virtual bool SupportsCatalogsInPrivilegeDefinitions ();
	public virtual bool SupportsCatalogsInProcedureCalls ();
	public virtual bool SupportsCatalogsInTableDefinitions ();
	public virtual bool SupportsColumnAliasing ();
	public virtual bool SupportsConvert (int fromType, int toType);
	public virtual bool SupportsConvert ();
	public virtual bool SupportsCoreSQLGrammar ();
	public virtual bool SupportsCorrelatedSubqueries ();
	public virtual bool SupportsDataDefinitionAndDataManipulationTransactions ();
	public virtual bool SupportsDataManipulationTransactionsOnly ();
	public virtual bool SupportsDifferentTableCorrelationNames ();
	public virtual bool SupportsExpressionsInOrderBy ();
	public virtual bool SupportsExtendedSQLGrammar ();
	public virtual bool SupportsFullOuterJoins ();
	public virtual bool SupportsGetGeneratedKeys ();
	public virtual bool SupportsGroupBy ();
	public virtual bool SupportsGroupByBeyondSelect ();
	public virtual bool SupportsGroupByUnrelated ();
	public virtual bool SupportsIntegrityEnhancementFacility ();
	public virtual bool SupportsLikeEscapeClause ();
	public virtual bool SupportsLimitedOuterJoins ();
	public virtual bool SupportsMinimumSQLGrammar ();
	public virtual bool SupportsMixedCaseIdentifiers ();
	public virtual bool SupportsMixedCaseQuotedIdentifiers ();
	public virtual bool SupportsMultipleOpenResults ();
	public virtual bool SupportsMultipleResultSets ();
	public virtual bool SupportsMultipleTransactions ();
	public virtual bool SupportsNamedParameters ();
	public virtual bool SupportsNonNullableColumns ();
	public virtual bool SupportsOpenCursorsAcrossCommit ();
	public virtual bool SupportsOpenCursorsAcrossRollback ();
	public virtual bool SupportsOpenStatementsAcrossCommit ();
	public virtual bool SupportsOpenStatementsAcrossRollback ();
	public virtual bool SupportsOrderByUnrelated ();
	public virtual bool SupportsOuterJoins ();
	public virtual bool SupportsPositionedDelete ();
	public virtual bool SupportsPositionedUpdate ();
	public virtual bool SupportsResultSetConcurrency (int type, int concurrency);
	public virtual bool SupportsResultSetHoldability (int holdability);
	public virtual bool SupportsResultSetType (int type);
	public virtual bool SupportsSavepoints ();
	public virtual bool SupportsSchemasInDataManipulation ();
	public virtual bool SupportsSchemasInIndexDefinitions ();
	public virtual bool SupportsSchemasInPrivilegeDefinitions ();
	public virtual bool SupportsSchemasInProcedureCalls ();
	public virtual bool SupportsSchemasInTableDefinitions ();
	public virtual bool SupportsSelectForUpdate ();
	public virtual bool SupportsStatementPooling ();
	public virtual bool SupportsStoredFunctionsUsingCallSyntax ();
	public virtual bool SupportsStoredProcedures ();
	public virtual bool SupportsSubqueriesInComparisons ();
	public virtual bool SupportsSubqueriesInExists ();
	public virtual bool SupportsSubqueriesInIns ();
	public virtual bool SupportsSubqueriesInQuantifieds ();
	public virtual bool SupportsTableCorrelationNames ();
	public virtual bool SupportsTransactionIsolationLevel (int level);
	public virtual bool SupportsTransactions ();
	public virtual bool SupportsUnion ();
	public virtual bool SupportsUnionAll ();
	public virtual bool UpdatesAreDetected (int type);
	public virtual bool UsesLocalFilePerTable ();
	public virtual bool UsesLocalFiles ();
}
```

### New Type Java.Sql.IDriver

```
public interface IDriver : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual int MajorVersion { get; }
	public virtual int MinorVersion { get; }
	public virtual Java.Util.Logging.Logger ParentLogger { get; }
	// methods
	public virtual bool AcceptsURL (string url);
	public virtual IConnection Connect (string url, Java.Util.Properties info);
	public virtual DriverPropertyInfo[] GetPropertyInfo (string url, Java.Util.Properties info);
	public virtual bool JdbcCompliant ();
}
```

### New Type Java.Sql.IDriverExtensions

```
public static class IDriverExtensions {
	// methods
	public static System.Threading.Tasks.Task<IConnection> ConnectAsync (IDriver self, string url, Java.Util.Properties info);
}
```

### New Type Java.Sql.IPreparedStatement

```
public interface IPreparedStatement : IStatement, IWrapper, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual IResultSetMetaData MetaData { get; }
	public virtual IParameterMetaData ParameterMetaData { get; }
	// methods
	public virtual void AddBatch ();
	public virtual void ClearParameters ();
	public virtual bool Execute ();
	public virtual IResultSet ExecuteQuery ();
	public virtual int ExecuteUpdate ();
	public virtual void SetArray (int parameterIndex, IArray theArray);
	public virtual void SetAsciiStream (int parameterIndex, System.IO.Stream inputStream);
	public virtual void SetAsciiStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	public virtual void SetAsciiStream (int parameterIndex, System.IO.Stream inputStream, long length);
	public virtual void SetBigDecimal (int parameterIndex, Java.Math.BigDecimal theBigDecimal);
	public virtual void SetBinaryStream (int parameterIndex, System.IO.Stream inputStream, long length);
	public virtual void SetBinaryStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	public virtual void SetBinaryStream (int parameterIndex, System.IO.Stream inputStream);
	public virtual void SetBlob (int parameterIndex, IBlob theBlob);
	public virtual void SetBlob (int parameterIndex, System.IO.Stream inputStream, long length);
	public virtual void SetBlob (int parameterIndex, System.IO.Stream inputStream);
	public virtual void SetBoolean (int parameterIndex, bool theBoolean);
	public virtual void SetByte (int parameterIndex, sbyte theByte);
	public virtual void SetBytes (int parameterIndex, byte[] theBytes);
	public virtual void SetCharacterStream (int parameterIndex, Java.IO.Reader reader, long length);
	public virtual void SetCharacterStream (int parameterIndex, Java.IO.Reader reader, int length);
	public virtual void SetCharacterStream (int parameterIndex, Java.IO.Reader reader);
	public virtual void SetClob (int parameterIndex, Java.IO.Reader reader);
	public virtual void SetClob (int parameterIndex, Java.IO.Reader reader, long length);
	public virtual void SetClob (int parameterIndex, IClob theClob);
	public virtual void SetDate (int parameterIndex, Date theDate, Java.Util.Calendar cal);
	public virtual void SetDate (int parameterIndex, Date theDate);
	public virtual void SetDouble (int parameterIndex, double theDouble);
	public virtual void SetFloat (int parameterIndex, float theFloat);
	public virtual void SetInt (int parameterIndex, int theInt);
	public virtual void SetLong (int parameterIndex, long theLong);
	public virtual void SetNCharacterStream (int parameterIndex, Java.IO.Reader reader, long length);
	public virtual void SetNCharacterStream (int parameterIndex, Java.IO.Reader reader);
	public virtual void SetNClob (int parameterIndex, Java.IO.Reader reader);
	public virtual void SetNClob (int parameterIndex, Java.IO.Reader reader, long length);
	public virtual void SetNClob (int parameterIndex, INClob value);
	public virtual void SetNString (int parameterIndex, string theString);
	public virtual void SetNull (int paramIndex, int sqlType, string typeName);
	public virtual void SetNull (int parameterIndex, int sqlType);
	public virtual void SetObject (int parameterIndex, Java.Lang.Object theObject, int targetSqlType, int scale);
	public virtual void SetObject (int parameterIndex, Java.Lang.Object theObject, int targetSqlType);
	public virtual void SetObject (int parameterIndex, Java.Lang.Object theObject);
	public virtual void SetRef (int parameterIndex, IRef theRef);
	public virtual void SetRowId (int parameterIndex, IRowId theRowId);
	public virtual void SetShort (int parameterIndex, short theShort);
	public virtual void SetSQLXML (int parameterIndex, ISQLXML xmlObject);
	public virtual void SetString (int parameterIndex, string theString);
	public virtual void SetTime (int parameterIndex, Time theTime, Java.Util.Calendar cal);
	public virtual void SetTime (int parameterIndex, Time theTime);
	public virtual void SetTimestamp (int parameterIndex, Timestamp theTimestamp);
	public virtual void SetTimestamp (int parameterIndex, Timestamp theTimestamp, Java.Util.Calendar cal);

	[Obsolete ("deprecated")]
	public virtual void SetUnicodeStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	public virtual void SetURL (int parameterIndex, Java.Net.URL theURL);
}
```

### New Type Java.Sql.IResultSet

```
public interface IResultSet : IWrapper, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual int Concurrency { get; }
	public virtual string CursorName { get; }
	public virtual int FetchDirection { get; set; }
	public virtual int FetchSize { get; set; }
	public virtual int Holdability { get; }
	public virtual bool IsAfterLast { get; }
	public virtual bool IsBeforeFirst { get; }
	public virtual bool IsClosed { get; }
	public virtual bool IsFirst { get; }
	public virtual bool IsLast { get; }
	public virtual IResultSetMetaData MetaData { get; }
	public virtual int Row { get; }
	public virtual IStatement Statement { get; }
	public virtual int Type { get; }
	public virtual SQLWarning Warnings { get; }
	// methods
	public virtual bool Absolute (int row);
	public virtual void AfterLast ();
	public virtual void BeforeFirst ();
	public virtual void CancelRowUpdates ();
	public virtual void ClearWarnings ();
	public virtual void Close ();
	public virtual void DeleteRow ();
	public virtual int FindColumn (string columnName);
	public virtual bool First ();
	public virtual IArray GetArray (string colName);
	public virtual IArray GetArray (int columnIndex);
	public virtual System.IO.Stream GetAsciiStream (int columnIndex);
	public virtual System.IO.Stream GetAsciiStream (string columnName);

	[Obsolete ("deprecated")]
	public virtual Java.Math.BigDecimal GetBigDecimal (string columnName, int scale);
	public virtual Java.Math.BigDecimal GetBigDecimal (string columnName);

	[Obsolete ("deprecated")]
	public virtual Java.Math.BigDecimal GetBigDecimal (int columnIndex, int scale);
	public virtual Java.Math.BigDecimal GetBigDecimal (int columnIndex);
	public virtual System.IO.Stream GetBinaryStream (int columnIndex);
	public virtual System.IO.Stream GetBinaryStream (string columnName);
	public virtual IBlob GetBlob (string columnName);
	public virtual IBlob GetBlob (int columnIndex);
	public virtual bool GetBoolean (int columnIndex);
	public virtual bool GetBoolean (string columnName);
	public virtual sbyte GetByte (string columnName);
	public virtual sbyte GetByte (int columnIndex);
	public virtual byte[] GetBytes (int columnIndex);
	public virtual byte[] GetBytes (string columnName);
	public virtual Java.IO.Reader GetCharacterStream (int columnIndex);
	public virtual Java.IO.Reader GetCharacterStream (string columnName);
	public virtual IClob GetClob (string colName);
	public virtual IClob GetClob (int columnIndex);
	public virtual Date GetDate (int columnIndex);
	public virtual Date GetDate (int columnIndex, Java.Util.Calendar cal);
	public virtual Date GetDate (string columnName);
	public virtual Date GetDate (string columnName, Java.Util.Calendar cal);
	public virtual double GetDouble (string columnName);
	public virtual double GetDouble (int columnIndex);
	public virtual float GetFloat (int columnIndex);
	public virtual float GetFloat (string columnName);
	public virtual int GetInt (int columnIndex);
	public virtual int GetInt (string columnName);
	public virtual long GetLong (string columnName);
	public virtual long GetLong (int columnIndex);
	public virtual Java.IO.Reader GetNCharacterStream (int columnIndex);
	public virtual Java.IO.Reader GetNCharacterStream (string columnLabel);
	public virtual INClob GetNClob (string columnLabel);
	public virtual INClob GetNClob (int columnIndex);
	public virtual string GetNString (int columnIndex);
	public virtual string GetNString (string columnLabel);
	public virtual Java.Lang.Object GetObject (string columnName, System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> map);
	public virtual Java.Lang.Object GetObject (string p0, Java.Lang.Class p1);
	public virtual Java.Lang.Object GetObject (string columnName);
	public virtual Java.Lang.Object GetObject (int columnIndex, System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> map);
	public virtual Java.Lang.Object GetObject (int p0, Java.Lang.Class p1);
	public virtual Java.Lang.Object GetObject (int columnIndex);
	public virtual IRef GetRef (int columnIndex);
	public virtual IRef GetRef (string colName);
	public virtual IRowId GetRowId (string columnLabel);
	public virtual IRowId GetRowId (int columnIndex);
	public virtual short GetShort (int columnIndex);
	public virtual short GetShort (string columnName);
	public virtual ISQLXML GetSQLXML (int columnIndex);
	public virtual ISQLXML GetSQLXML (string columnLabel);
	public virtual string GetString (string columnName);
	public virtual string GetString (int columnIndex);
	public virtual Time GetTime (string columnName, Java.Util.Calendar cal);
	public virtual Time GetTime (string columnName);
	public virtual Time GetTime (int columnIndex, Java.Util.Calendar cal);
	public virtual Time GetTime (int columnIndex);
	public virtual Timestamp GetTimestamp (string columnName, Java.Util.Calendar cal);
	public virtual Timestamp GetTimestamp (string columnName);
	public virtual Timestamp GetTimestamp (int columnIndex, Java.Util.Calendar cal);
	public virtual Timestamp GetTimestamp (int columnIndex);

	[Obsolete ("deprecated")]
	public virtual System.IO.Stream GetUnicodeStream (string columnName);

	[Obsolete ("deprecated")]
	public virtual System.IO.Stream GetUnicodeStream (int columnIndex);
	public virtual Java.Net.URL GetURL (int columnIndex);
	public virtual Java.Net.URL GetURL (string columnName);
	public virtual void InsertRow ();
	public virtual bool Last ();
	public virtual void MoveToCurrentRow ();
	public virtual void MoveToInsertRow ();
	public virtual bool Next ();
	public virtual bool Previous ();
	public virtual void RefreshRow ();
	public virtual bool Relative (int rows);
	public virtual bool RowDeleted ();
	public virtual bool RowInserted ();
	public virtual bool RowUpdated ();
	public virtual void UpdateArray (string columnName, IArray x);
	public virtual void UpdateArray (int columnIndex, IArray x);
	public virtual void UpdateAsciiStream (string columnLabel, System.IO.Stream x, long length);
	public virtual void UpdateAsciiStream (string columnName, System.IO.Stream x, int length);
	public virtual void UpdateAsciiStream (string columnLabel, System.IO.Stream x);
	public virtual void UpdateAsciiStream (int columnIndex, System.IO.Stream x, long length);
	public virtual void UpdateAsciiStream (int columnIndex, System.IO.Stream x, int length);
	public virtual void UpdateAsciiStream (int columnIndex, System.IO.Stream x);
	public virtual void UpdateBigDecimal (string columnName, Java.Math.BigDecimal x);
	public virtual void UpdateBigDecimal (int columnIndex, Java.Math.BigDecimal x);
	public virtual void UpdateBinaryStream (string columnLabel, System.IO.Stream x, long length);
	public virtual void UpdateBinaryStream (string columnName, System.IO.Stream x, int length);
	public virtual void UpdateBinaryStream (string columnLabel, System.IO.Stream x);
	public virtual void UpdateBinaryStream (int columnIndex, System.IO.Stream x, long length);
	public virtual void UpdateBinaryStream (int columnIndex, System.IO.Stream x, int length);
	public virtual void UpdateBinaryStream (int columnIndex, System.IO.Stream x);
	public virtual void UpdateBlob (string columnName, IBlob x);
	public virtual void UpdateBlob (string columnLabel, System.IO.Stream inputStream, long length);
	public virtual void UpdateBlob (string columnLabel, System.IO.Stream inputStream);
	public virtual void UpdateBlob (int columnIndex, IBlob x);
	public virtual void UpdateBlob (int columnIndex, System.IO.Stream inputStream, long length);
	public virtual void UpdateBlob (int columnIndex, System.IO.Stream inputStream);
	public virtual void UpdateBoolean (int columnIndex, bool x);
	public virtual void UpdateBoolean (string columnName, bool x);
	public virtual void UpdateByte (string columnName, sbyte x);
	public virtual void UpdateByte (int columnIndex, sbyte x);
	public virtual void UpdateBytes (int columnIndex, byte[] x);
	public virtual void UpdateBytes (string columnName, byte[] x);
	public virtual void UpdateCharacterStream (string columnLabel, Java.IO.Reader reader, long length);
	public virtual void UpdateCharacterStream (string columnName, Java.IO.Reader reader, int length);
	public virtual void UpdateCharacterStream (string columnLabel, Java.IO.Reader reader);
	public virtual void UpdateCharacterStream (int columnIndex, Java.IO.Reader x, long length);
	public virtual void UpdateCharacterStream (int columnIndex, Java.IO.Reader x, int length);
	public virtual void UpdateCharacterStream (int columnIndex, Java.IO.Reader x);
	public virtual void UpdateClob (string columnName, IClob x);
	public virtual void UpdateClob (string columnLabel, Java.IO.Reader reader, long length);
	public virtual void UpdateClob (string columnLabel, Java.IO.Reader reader);
	public virtual void UpdateClob (int columnIndex, IClob x);
	public virtual void UpdateClob (int columnIndex, Java.IO.Reader reader, long length);
	public virtual void UpdateClob (int columnIndex, Java.IO.Reader reader);
	public virtual void UpdateDate (string columnName, Date x);
	public virtual void UpdateDate (int columnIndex, Date x);
	public virtual void UpdateDouble (int columnIndex, double x);
	public virtual void UpdateDouble (string columnName, double x);
	public virtual void UpdateFloat (string columnName, float x);
	public virtual void UpdateFloat (int columnIndex, float x);
	public virtual void UpdateInt (string columnName, int x);
	public virtual void UpdateInt (int columnIndex, int x);
	public virtual void UpdateLong (int columnIndex, long x);
	public virtual void UpdateLong (string columnName, long x);
	public virtual void UpdateNCharacterStream (string columnLabel, Java.IO.Reader reader, long length);
	public virtual void UpdateNCharacterStream (string columnLabel, Java.IO.Reader reader);
	public virtual void UpdateNCharacterStream (int columnIndex, Java.IO.Reader x, long length);
	public virtual void UpdateNCharacterStream (int columnIndex, Java.IO.Reader x);
	public virtual void UpdateNClob (string columnLabel, INClob nClob);
	public virtual void UpdateNClob (string columnLabel, Java.IO.Reader reader, long length);
	public virtual void UpdateNClob (string columnLabel, Java.IO.Reader reader);
	public virtual void UpdateNClob (int columnIndex, INClob nClob);
	public virtual void UpdateNClob (int columnIndex, Java.IO.Reader reader, long length);
	public virtual void UpdateNClob (int columnIndex, Java.IO.Reader reader);
	public virtual void UpdateNString (string columnLabel, string nString);
	public virtual void UpdateNString (int columnIndex, string nString);
	public virtual void UpdateNull (int columnIndex);
	public virtual void UpdateNull (string columnName);
	public virtual void UpdateObject (string columnName, Java.Lang.Object x, int scale);
	public virtual void UpdateObject (string columnName, Java.Lang.Object x);
	public virtual void UpdateObject (int columnIndex, Java.Lang.Object x, int scale);
	public virtual void UpdateObject (int columnIndex, Java.Lang.Object x);
	public virtual void UpdateRef (int columnIndex, IRef x);
	public virtual void UpdateRef (string columnName, IRef x);
	public virtual void UpdateRow ();
	public virtual void UpdateRowId (string columnLabel, IRowId value);
	public virtual void UpdateRowId (int columnIndex, IRowId value);
	public virtual void UpdateShort (int columnIndex, short x);
	public virtual void UpdateShort (string columnName, short x);
	public virtual void UpdateSQLXML (int columnIndex, ISQLXML xmlObject);
	public virtual void UpdateSQLXML (string columnLabel, ISQLXML xmlObject);
	public virtual void UpdateString (string columnName, string x);
	public virtual void UpdateString (int columnIndex, string x);
	public virtual void UpdateTime (int columnIndex, Time x);
	public virtual void UpdateTime (string columnName, Time x);
	public virtual void UpdateTimestamp (int columnIndex, Timestamp x);
	public virtual void UpdateTimestamp (string columnName, Timestamp x);
	public virtual bool WasNull ();
}
```

### New Type Java.Sql.ISQLData

```
public interface ISQLData : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual string SQLTypeName { get; }
	// methods
	public virtual void ReadSQL (ISQLInput stream, string typeName);
	public virtual void WriteSQL (ISQLOutput stream);
}
```

### New Type Java.Sql.ISQLInput

```
public interface ISQLInput : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual IArray ReadArray ();
	public virtual System.IO.Stream ReadAsciiStream ();
	public virtual Java.Math.BigDecimal ReadBigDecimal ();
	public virtual System.IO.Stream ReadBinaryStream ();
	public virtual IBlob ReadBlob ();
	public virtual bool ReadBoolean ();
	public virtual sbyte ReadByte ();
	public virtual byte[] ReadBytes ();
	public virtual Java.IO.Reader ReadCharacterStream ();
	public virtual IClob ReadClob ();
	public virtual Date ReadDate ();
	public virtual double ReadDouble ();
	public virtual float ReadFloat ();
	public virtual int ReadInt ();
	public virtual long ReadLong ();
	public virtual INClob ReadNClob ();
	public virtual string ReadNString ();
	public virtual Java.Lang.Object ReadObject ();
	public virtual IRef ReadRef ();
	public virtual IRowId ReadRowId ();
	public virtual short ReadShort ();
	public virtual ISQLXML ReadSQLXML ();
	public virtual string ReadString ();
	public virtual Time ReadTime ();
	public virtual Timestamp ReadTimestamp ();
	public virtual Java.Net.URL ReadURL ();
	public virtual bool WasNull ();
}
```

### New Type Java.Sql.ISQLOutput

```
public interface ISQLOutput : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void WriteArray (IArray theArray);
	public virtual void WriteAsciiStream (System.IO.Stream theStream);
	public virtual void WriteBigDecimal (Java.Math.BigDecimal theBigDecimal);
	public virtual void WriteBinaryStream (System.IO.Stream theStream);
	public virtual void WriteBlob (IBlob theBlob);
	public virtual void WriteBoolean (bool theFlag);
	public virtual void WriteByte (sbyte theByte);
	public virtual void WriteBytes (byte[] theBytes);
	public virtual void WriteCharacterStream (Java.IO.Reader theStream);
	public virtual void WriteClob (IClob theClob);
	public virtual void WriteDate (Date theDate);
	public virtual void WriteDouble (double theDouble);
	public virtual void WriteFloat (float theFloat);
	public virtual void WriteInt (int theInt);
	public virtual void WriteLong (long theLong);
	public virtual void WriteNClob (INClob theNClob);
	public virtual void WriteNString (string theString);
	public virtual void WriteObject (ISQLData theObject);
	public virtual void WriteRef (IRef theRef);
	public virtual void WriteRowId (IRowId theRowId);
	public virtual void WriteShort (short theShort);
	public virtual void WriteSQLXML (ISQLXML theXml);
	public virtual void WriteString (string theString);
	public virtual void WriteStruct (IStruct theStruct);
	public virtual void WriteTime (Time theTime);
	public virtual void WriteTimestamp (Timestamp theTimestamp);
	public virtual void WriteURL (Java.Net.URL theURL);
}
```

### New Type Java.Sql.IStatement

```
public interface IStatement : IWrapper, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual IConnection Connection { get; }
	public virtual int FetchDirection { get; set; }
	public virtual int FetchSize { get; set; }
	public virtual IResultSet GeneratedKeys { get; }
	public virtual bool IsClosed { get; }
	public virtual bool IsCloseOnCompletion { get; }
	public virtual int MaxFieldSize { get; set; }
	public virtual int MaxRows { get; set; }
	public virtual bool MoreResults { get; }
	public virtual bool Poolable { get; set; }
	public virtual int QueryTimeout { get; set; }
	public virtual IResultSet ResultSet { get; }
	public virtual int ResultSetConcurrency { get; }
	public virtual int ResultSetHoldability { get; }
	public virtual int ResultSetType { get; }
	public virtual int UpdateCount { get; }
	public virtual SQLWarning Warnings { get; }
	// methods
	public virtual void AddBatch (string sql);
	public virtual void Cancel ();
	public virtual void ClearBatch ();
	public virtual void ClearWarnings ();
	public virtual void Close ();
	public virtual void CloseOnCompletion ();
	public virtual bool Execute (string sql, string[] columnNames);
	public virtual bool Execute (string sql, int[] columnIndexes);
	public virtual bool Execute (string sql, int autoGeneratedKeys);
	public virtual bool Execute (string sql);
	public virtual int[] ExecuteBatch ();
	public virtual IResultSet ExecuteQuery (string sql);
	public virtual int ExecuteUpdate (string sql, string[] columnNames);
	public virtual int ExecuteUpdate (string sql, int[] columnIndexes);
	public virtual int ExecuteUpdate (string sql, int autoGeneratedKeys);
	public virtual int ExecuteUpdate (string sql);
	public virtual bool GetMoreResults (int current);
	public virtual void SetCursorName (string name);
	public virtual void SetEscapeProcessing (bool enable);
}
```

### New Type Java.Sql.ResultSet

```
public abstract class ResultSet {
	// fields
	public static const int CloseCursorsAtCommit;
	public static const int ConcurReadOnly;
	public static const int ConcurUpdatable;
	public static const int FetchForward;
	public static const int FetchReverse;
	public static const int FetchUnknown;
	public static const int HoldCursorsOverCommit;
	public static const int TypeForwardOnly;
	public static const int TypeScrollInsensitive;
	public static const int TypeScrollSensitive;
}
```

### New Type Java.Sql.ResultSetConsts

```
public abstract class ResultSetConsts : Java.Sql.ResultSet {
}
```

### New Type Java.Sql.Statement

```
public abstract class Statement {
	// fields
	public static const int CloseAllResults;
	public static const int CloseCurrentResult;
	public static const int ExecuteFailed;
	public static const int KeepCurrentResult;
	public static const int NoGeneratedKeys;
	public static const int ReturnGeneratedKeys;
	public static const int SuccessNoInfo;
}
```

### New Type Java.Sql.StatementConsts

```
public abstract class StatementConsts : Java.Sql.Statement {
}
```

## Namespace Java.Text

### Type Changed: Java.Text.CollationKey

Removed constructor:

```
protected CollationKey (string p0);
```

Added constructor:

```
protected CollationKey (string source);
```

### Type Changed: Java.Text.DateFormatSymbols

Removed methods:

```
public static DateFormatSymbols GetInstance (Java.Util.Locale p0);
	public virtual void SetZoneStrings (string[][] data);
```

Added methods:

```
public static DateFormatSymbols GetInstance (Java.Util.Locale locale);
	public virtual void SetZoneStrings (string[][] zoneStrings);
```

### Type Changed: Java.Text.DecimalFormat

Removed method:

```
public override Java.Lang.StringBuffer Format (Java.Lang.Object number, Java.Lang.StringBuffer toAppendTo, FieldPosition pos);
```

Added method:

```
public override Java.Lang.StringBuffer Format (Java.Lang.Object number, Java.Lang.StringBuffer buffer, FieldPosition position);
```

### Type Changed: Java.Text.DecimalFormatSymbols

Removed method:

```
public static DecimalFormatSymbols GetInstance (Java.Util.Locale p0);
```

Added method:

```
public static DecimalFormatSymbols GetInstance (Java.Util.Locale locale);
```

### Type Changed: Java.Text.MessageFormat

Removed method:

```
public static string Format (string template, Java.Lang.Object[] objects);
```

Added method:

```
public static string Format (string format, Java.Lang.Object[] args);
```

## Namespace Java.Util

### Type Changed: Java.Util.AbstractQueue

Removed method:

```
public virtual bool Offer (Java.Lang.Object o);
```

Added method:

```
public virtual bool Offer (Java.Lang.Object e);
```

### Type Changed: Java.Util.ArrayDeque

Removed constructor:

```
public ArrayDeque (int minSize);
```

Added constructor:

```
public ArrayDeque (int numElements);
```

Removed methods:

```
public virtual bool RemoveFirstOccurrence (Java.Lang.Object obj);
	public virtual bool RemoveLastOccurrence (Java.Lang.Object obj);
```

Added methods:

```
public virtual bool RemoveFirstOccurrence (Java.Lang.Object o);
	public virtual bool RemoveLastOccurrence (Java.Lang.Object o);
```

### Type Changed: Java.Util.ArrayList

Removed method:

```
public override Java.Lang.Object Get (int location);
```

Added method:

```
public override Java.Lang.Object Get (int index);
```

### Type Changed: Java.Util.Arrays

Removed methods:

```
public static int BinarySearch (Java.Lang.Object[] p0, int p1, int p2, Java.Lang.Object p3);
	public static int BinarySearch (Java.Lang.Object[] array, Java.Lang.Object object);
	public static int BinarySearch (long[] p0, int p1, int p2, long p3);
	public static int BinarySearch (short[] p0, int p1, int p2, short p3);
	public static int BinarySearch (Java.Lang.Object[] p0, int p1, int p2, Java.Lang.Object p3, IComparator p4);
	public static int BinarySearch (Java.Lang.Object[] array, Java.Lang.Object object, IComparator comparator);
	public static int BinarySearch (int[] p0, int p1, int p2, int p3);
	public static int BinarySearch (byte[] p0, int p1, int p2, sbyte p3);
	public static int BinarySearch (char[] p0, int p1, int p2, char p3);
	public static int BinarySearch (float[] p0, int p1, int p2, float p3);
	public static int BinarySearch (double[] p0, int p1, int p2, double p3);
	public static long[] CopyOf (long[] p0, int p1);
	public static short[] CopyOf (short[] p0, int p1);
	public static Java.Lang.Object[] CopyOf (Java.Lang.Object[] p0, int p1);
	public static Java.Lang.Object[] CopyOf (Java.Lang.Object[] p0, int p1, Java.Lang.Class p2);
	public static int[] CopyOf (int[] p0, int p1);
	public static bool[] CopyOf (bool[] p0, int p1);
	public static byte[] CopyOf (byte[] p0, int p1);
	public static char[] CopyOf (char[] p0, int p1);
	public static double[] CopyOf (double[] p0, int p1);
	public static float[] CopyOf (float[] p0, int p1);
	public static long[] CopyOfRange (long[] p0, int p1, int p2);
	public static short[] CopyOfRange (short[] p0, int p1, int p2);
	public static Java.Lang.Object[] CopyOfRange (Java.Lang.Object[] p0, int p1, int p2);
	public static Java.Lang.Object[] CopyOfRange (Java.Lang.Object[] p0, int p1, int p2, Java.Lang.Class p3);
	public static int[] CopyOfRange (int[] p0, int p1, int p2);
	public static float[] CopyOfRange (float[] p0, int p1, int p2);
	public static double[] CopyOfRange (double[] p0, int p1, int p2);
	public static char[] CopyOfRange (char[] p0, int p1, int p2);
	public static byte[] CopyOfRange (byte[] p0, int p1, int p2);
	public static bool[] CopyOfRange (bool[] p0, int p1, int p2);
```

Added methods:

```
public static int BinarySearch (Java.Lang.Object[] array, int startIndex, int endIndex, Java.Lang.Object value);
	public static int BinarySearch (Java.Lang.Object[] array, Java.Lang.Object value);
	public static int BinarySearch (long[] array, int startIndex, int endIndex, long value);
	public static int BinarySearch (short[] array, int startIndex, int endIndex, short value);
	public static int BinarySearch (Java.Lang.Object[] array, int startIndex, int endIndex, Java.Lang.Object value, IComparator comparator);
	public static int BinarySearch (Java.Lang.Object[] array, Java.Lang.Object value, IComparator comparator);
	public static int BinarySearch (int[] array, int startIndex, int endIndex, int value);
	public static int BinarySearch (byte[] array, int startIndex, int endIndex, sbyte value);
	public static int BinarySearch (char[] array, int startIndex, int endIndex, char value);
	public static int BinarySearch (float[] array, int startIndex, int endIndex, float value);
	public static int BinarySearch (double[] array, int startIndex, int endIndex, double value);
	public static long[] CopyOf (long[] original, int newLength);
	public static short[] CopyOf (short[] original, int newLength);
	public static Java.Lang.Object[] CopyOf (Java.Lang.Object[] original, int newLength);
	public static Java.Lang.Object[] CopyOf (Java.Lang.Object[] original, int newLength, Java.Lang.Class newType);
	public static int[] CopyOf (int[] original, int newLength);
	public static bool[] CopyOf (bool[] original, int newLength);
	public static byte[] CopyOf (byte[] original, int newLength);
	public static char[] CopyOf (char[] original, int newLength);
	public static double[] CopyOf (double[] original, int newLength);
	public static float[] CopyOf (float[] original, int newLength);
	public static long[] CopyOfRange (long[] original, int start, int end);
	public static short[] CopyOfRange (short[] original, int start, int end);
	public static Java.Lang.Object[] CopyOfRange (Java.Lang.Object[] original, int start, int end);
	public static Java.Lang.Object[] CopyOfRange (Java.Lang.Object[] original, int start, int end, Java.Lang.Class newType);
	public static int[] CopyOfRange (int[] original, int start, int end);
	public static float[] CopyOfRange (float[] original, int start, int end);
	public static double[] CopyOfRange (double[] original, int start, int end);
	public static char[] CopyOfRange (char[] original, int start, int end);
	public static byte[] CopyOfRange (byte[] original, int start, int end);
	public static bool[] CopyOfRange (bool[] original, int start, int end);
```

### Type Changed: Java.Util.BitSet

Removed methods:

```
public virtual void Clear (int pos1, int pos2);
	public virtual void Clear (int pos);
	public virtual void Flip (int pos1, int pos2);
	public virtual void Flip (int pos);
	public virtual BitSet Get (int pos1, int pos2);
	public virtual bool Get (int pos);
	public virtual int NextClearBit (int pos);
	public virtual int NextSetBit (int pos);
	public virtual void Set (int pos1, int pos2, bool val);
	public virtual void Set (int pos1, int pos2);
	public virtual void Set (int pos, bool val);
	public virtual void Set (int pos);
```

Added methods:

```
public virtual void Clear (int fromIndex, int toIndex);
	public virtual void Clear (int index);
	public virtual void Flip (int fromIndex, int toIndex);
	public virtual void Flip (int index);
	public virtual BitSet Get (int fromIndex, int toIndex);
	public virtual bool Get (int index);
	public virtual int NextClearBit (int index);
	public virtual int NextSetBit (int index);
	public virtual void Set (int fromIndex, int toIndex, bool val);
	public virtual void Set (int fromIndex, int toIndex);
	public virtual void Set (int index, bool val);
	public virtual void Set (int index);
```

### Type Changed: Java.Util.Calendar

Removed methods:

```
public virtual string GetDisplayName (int p0, int p1, Locale p2);
	public virtual System.Collections.Generic.IDictionary<System.String,Java.Lang.Integer> GetDisplayNames (int p0, int p1, Locale p2);
```

Added methods:

```
public virtual string GetDisplayName (int field, int style, Locale locale);
	public virtual System.Collections.Generic.IDictionary<System.String,Java.Lang.Integer> GetDisplayNames (int field, int style, Locale locale);
```

### Type Changed: Java.Util.Collections

Removed methods:

```
public static IQueue AsLifoQueue (IDeque p0);
	public static System.Collections.ICollection NewSetFromMap (System.Collections.IDictionary p0);
```

Added methods:

```
public static IQueue AsLifoQueue (IDeque deque);
	public static System.Collections.ICollection NewSetFromMap (System.Collections.IDictionary map);
```

### Type Changed: Java.Util.EventListenerProxy

Removed constructor:

```
public EventListenerProxy (Java.Lang.Object p0);
```

### Type Changed: Java.Util.Formatter

Added interface:

```
Java.IO.ICloseable
```

Removed method:

```
public void Close ();
```

Added method:

```
public virtual void Close ();
```

### Type Changed: Java.Util.IDeque

Removed methods:

```
public virtual bool Add (Java.Lang.Object p0);
	public virtual bool Contains (Java.Lang.Object p0);
	public virtual bool Offer (Java.Lang.Object p0);
	public virtual bool Remove (Java.Lang.Object p0);
```

Added methods:

```
public virtual bool Add (Java.Lang.Object e);
	public virtual bool Contains (Java.Lang.Object o);
	public virtual bool Offer (Java.Lang.Object e);
	public virtual bool Remove (Java.Lang.Object o);
```

### Type Changed: Java.Util.IllegalFormatFlagsException

Removed constructor:

```
public IllegalFormatFlagsException (string f);
```

Added constructor:

```
public IllegalFormatFlagsException (string flags);
```

### Type Changed: Java.Util.INavigableMap

Removed methods:

```
public virtual System.Collections.IDictionary HeadMap (Java.Lang.Object p0);
	public virtual INavigableMap HeadMap (Java.Lang.Object endKey, bool inclusive);
	public virtual INavigableMap SubMap (Java.Lang.Object startKey, bool startInclusive, Java.Lang.Object endKey, bool endInclusive);
	public virtual System.Collections.IDictionary SubMap (Java.Lang.Object p0, Java.Lang.Object p1);
	public virtual System.Collections.IDictionary TailMap (Java.Lang.Object p0);
	public virtual INavigableMap TailMap (Java.Lang.Object startKey, bool inclusive);
```

Added methods:

```
public virtual System.Collections.IDictionary HeadMap (Java.Lang.Object toKey);
	public virtual INavigableMap HeadMap (Java.Lang.Object toKey, bool inclusive);
	public virtual INavigableMap SubMap (Java.Lang.Object fromKey, bool fromInclusive, Java.Lang.Object toKey, bool toInclusive);
	public virtual System.Collections.IDictionary SubMap (Java.Lang.Object fromKey, Java.Lang.Object toKey);
	public virtual System.Collections.IDictionary TailMap (Java.Lang.Object fromKey);
	public virtual INavigableMap TailMap (Java.Lang.Object fromKey, bool inclusive);
```

### Type Changed: Java.Util.INavigableSet

Removed methods:

```
public virtual ISortedSet HeadSet (Java.Lang.Object p0);
	public virtual INavigableSet HeadSet (Java.Lang.Object end, bool endInclusive);
	public virtual INavigableSet SubSet (Java.Lang.Object start, bool startInclusive, Java.Lang.Object end, bool endInclusive);
	public virtual ISortedSet SubSet (Java.Lang.Object p0, Java.Lang.Object p1);
	public virtual ISortedSet TailSet (Java.Lang.Object p0);
	public virtual INavigableSet TailSet (Java.Lang.Object start, bool startInclusive);
```

Added methods:

```
public virtual ISortedSet HeadSet (Java.Lang.Object toElement);
	public virtual INavigableSet HeadSet (Java.Lang.Object toElement, bool inclusive);
	public virtual INavigableSet SubSet (Java.Lang.Object fromElement, bool fromInclusive, Java.Lang.Object toElement, bool toInclusive);
	public virtual ISortedSet SubSet (Java.Lang.Object fromElement, Java.Lang.Object toElement);
	public virtual ISortedSet TailSet (Java.Lang.Object fromElement);
	public virtual INavigableSet TailSet (Java.Lang.Object fromElement, bool inclusive);
```

### Type Changed: Java.Util.IQueue

Removed methods:

```
public virtual bool Add (Java.Lang.Object p0);
	public virtual bool Offer (Java.Lang.Object o);
```

Added methods:

```
public virtual bool Add (Java.Lang.Object e);
	public virtual bool Offer (Java.Lang.Object e);
```

### Type Changed: Java.Util.LinkedList

Removed methods:

```
public virtual bool OfferFirst (Java.Lang.Object p0);
	public virtual bool OfferLast (Java.Lang.Object p0);
	public virtual void Push (Java.Lang.Object p0);
	public virtual bool RemoveFirstOccurrence (Java.Lang.Object p0);
	public virtual bool RemoveLastOccurrence (Java.Lang.Object p0);
```

Added methods:

```
public virtual bool OfferFirst (Java.Lang.Object e);
	public virtual bool OfferLast (Java.Lang.Object e);
	public virtual void Push (Java.Lang.Object e);
	public virtual bool RemoveFirstOccurrence (Java.Lang.Object o);
	public virtual bool RemoveLastOccurrence (Java.Lang.Object o);
```

### Type Changed: Java.Util.Properties

Removed methods:

```
public virtual void Load (Java.IO.Reader p0);
	public virtual void Store (Java.IO.Writer p0, string p1);
```

Added methods:

```
public virtual void Load (Java.IO.Reader in);
	public virtual void Store (Java.IO.Writer writer, string comment);
```

### Type Changed: Java.Util.PropertyResourceBundle

Removed constructor:

```
public PropertyResourceBundle (Java.IO.Reader p0);
```

Added constructor:

```
public PropertyResourceBundle (Java.IO.Reader reader);
```

### Type Changed: Java.Util.ResourceBundle

Removed methods:

```
public static void ClearCache (Java.Lang.ClassLoader p0);
	public virtual bool ContainsKey (string p0);
	public static ResourceBundle GetBundle (string p0, ResourceBundle.Control p1);
	public static ResourceBundle GetBundle (string p0, Locale p1, ResourceBundle.Control p2);
	public static ResourceBundle GetBundle (string p0, Locale p1, Java.Lang.ClassLoader p2, ResourceBundle.Control p3);
```

Added methods:

```
public static void ClearCache (Java.Lang.ClassLoader loader);
	public virtual bool ContainsKey (string key);
	public static ResourceBundle GetBundle (string baseName, ResourceBundle.Control control);
	public static ResourceBundle GetBundle (string baseName, Locale targetLocale, ResourceBundle.Control control);
	public static ResourceBundle GetBundle (string baseName, Locale targetLocale, Java.Lang.ClassLoader loader, ResourceBundle.Control control);
```

### Type Changed: Java.Util.Scanner

Added constructors:

```
public Scanner (Java.Nio.Channels.IReadableByteChannel src);
	public Scanner (Java.Nio.Channels.IReadableByteChannel src, string charsetName);
```

Added interface:

```
Java.IO.ICloseable
```

Removed method:

```
public void Close ();
```

Added method:

```
public virtual void Close ();
```

### Type Changed: Java.Util.TimeZone

Removed methods:

```
public static string[] GetAvailableIDs (int offset);
	public virtual int GetOffset (int era, int year, int month, int day, int dayOfWeek, int time);
	public static TimeZone GetTimeZone (string name);
	public virtual bool HasSameRules (TimeZone zone);
```

Added methods:

```
public static string[] GetAvailableIDs (int offsetMillis);
	public virtual int GetOffset (int era, int year, int month, int day, int dayOfWeek, int timeOfDayMillis);
	public static TimeZone GetTimeZone (string id);
	public virtual bool HasSameRules (TimeZone timeZone);
```

### Type Changed: Java.Util.TreeMap

Removed constructor:

```
public TreeMap (System.Collections.IDictionary map);
```

Added constructor:

```
public TreeMap (System.Collections.IDictionary copyFrom);
```

Removed methods:

```
public virtual IMapEntry CeilingEntry (Java.Lang.Object p0);
	public virtual Java.Lang.Object CeilingKey (Java.Lang.Object p0);
	public virtual IMapEntry FloorEntry (Java.Lang.Object p0);
	public virtual Java.Lang.Object FloorKey (Java.Lang.Object p0);
	public virtual INavigableMap HeadMap (Java.Lang.Object p0, bool p1);
	public virtual System.Collections.IDictionary HeadMap (Java.Lang.Object endKey);
	public virtual IMapEntry HigherEntry (Java.Lang.Object p0);
	public virtual Java.Lang.Object HigherKey (Java.Lang.Object p0);
	public virtual IMapEntry LowerEntry (Java.Lang.Object p0);
	public virtual Java.Lang.Object LowerKey (Java.Lang.Object p0);
	public virtual INavigableMap SubMap (Java.Lang.Object p0, bool p1, Java.Lang.Object p2, bool p3);
	public virtual System.Collections.IDictionary SubMap (Java.Lang.Object startKey, Java.Lang.Object endKey);
	public virtual System.Collections.IDictionary TailMap (Java.Lang.Object startKey);
	public virtual INavigableMap TailMap (Java.Lang.Object p0, bool p1);
```

Added methods:

```
public virtual IMapEntry CeilingEntry (Java.Lang.Object key);
	public virtual Java.Lang.Object CeilingKey (Java.Lang.Object key);
	public virtual IMapEntry FloorEntry (Java.Lang.Object key);
	public virtual Java.Lang.Object FloorKey (Java.Lang.Object key);
	public virtual INavigableMap HeadMap (Java.Lang.Object to, bool inclusive);
	public virtual System.Collections.IDictionary HeadMap (Java.Lang.Object toExclusive);
	public virtual IMapEntry HigherEntry (Java.Lang.Object key);
	public virtual Java.Lang.Object HigherKey (Java.Lang.Object key);
	public virtual IMapEntry LowerEntry (Java.Lang.Object key);
	public virtual Java.Lang.Object LowerKey (Java.Lang.Object key);
	public virtual INavigableMap SubMap (Java.Lang.Object from, bool fromInclusive, Java.Lang.Object to, bool toInclusive);
	public virtual System.Collections.IDictionary SubMap (Java.Lang.Object fromInclusive, Java.Lang.Object toExclusive);
	public virtual System.Collections.IDictionary TailMap (Java.Lang.Object fromInclusive);
	public virtual INavigableMap TailMap (Java.Lang.Object from, bool inclusive);
```

### Type Changed: Java.Util.TreeSet

Removed methods:

```
public virtual Java.Lang.Object Ceiling (Java.Lang.Object p0);
	public virtual Java.Lang.Object Floor (Java.Lang.Object p0);
	public virtual INavigableSet HeadSet (Java.Lang.Object p0, bool p1);
	public virtual Java.Lang.Object Higher (Java.Lang.Object p0);
	public virtual Java.Lang.Object Lower (Java.Lang.Object p0);
	public virtual INavigableSet SubSet (Java.Lang.Object p0, bool p1, Java.Lang.Object p2, bool p3);
	public virtual INavigableSet TailSet (Java.Lang.Object p0, bool p1);
```

Added methods:

```
public virtual Java.Lang.Object Ceiling (Java.Lang.Object e);
	public virtual Java.Lang.Object Floor (Java.Lang.Object e);
	public virtual INavigableSet HeadSet (Java.Lang.Object end, bool endInclusive);
	public virtual Java.Lang.Object Higher (Java.Lang.Object e);
	public virtual Java.Lang.Object Lower (Java.Lang.Object e);
	public virtual INavigableSet SubSet (Java.Lang.Object start, bool startInclusive, Java.Lang.Object end, bool endInclusive);
	public virtual INavigableSet TailSet (Java.Lang.Object start, bool startInclusive);
```

## Namespace Java.Util.Concurrent

### Type Changed: Java.Util.Concurrent.AbstractExecutorService

Removed methods:

```
public virtual System.Collections.IList InvokeAll (System.Collections.ICollection p0);
	public virtual System.Collections.IList InvokeAll (System.Collections.ICollection p0, long p1, TimeUnit p2);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection p0, long p1, TimeUnit p2);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection p0);
	protected virtual IRunnableFuture NewTaskFor (Java.Lang.IRunnable p0, Java.Lang.Object p1);
	protected virtual IRunnableFuture NewTaskFor (ICallable p0);
```

Added methods:

```
public virtual System.Collections.IList InvokeAll (System.Collections.ICollection tasks);
	public virtual System.Collections.IList InvokeAll (System.Collections.ICollection tasks, long timeout, TimeUnit unit);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection tasks, long timeout, TimeUnit unit);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection tasks);
	protected virtual IRunnableFuture NewTaskFor (Java.Lang.IRunnable runnable, Java.Lang.Object value);
	protected virtual IRunnableFuture NewTaskFor (ICallable callable);
```

### Type Changed: Java.Util.Concurrent.ConcurrentHashMap

Removed constructor:

```
public ConcurrentHashMap (int p0, float p1);
```

Added constructor:

```
public ConcurrentHashMap (int initialCapacity, float loadFactor);
```

### Type Changed: Java.Util.Concurrent.CopyOnWriteArrayList

Removed constructors:

```
public CopyOnWriteArrayList (Java.Lang.Object[] toCopyIn);
	public CopyOnWriteArrayList (System.Collections.ICollection c);
```

Added constructors:

```
public CopyOnWriteArrayList (Java.Lang.Object[] array);
	public CopyOnWriteArrayList (System.Collections.ICollection collection);
```

Removed methods:

```
public virtual void Add (int index, Java.Lang.Object element);
	public virtual bool AddAll (int index, System.Collections.ICollection c);
	public virtual bool AddAll (System.Collections.ICollection c);
	public virtual int AddAllAbsent (System.Collections.ICollection c);
	public virtual bool AddIfAbsent (Java.Lang.Object e);
	public virtual bool ContainsAll (System.Collections.ICollection c);
	public virtual int IndexOf (Java.Lang.Object e, int index);
	public virtual int IndexOf (Java.Lang.Object o);
	public virtual int LastIndexOf (Java.Lang.Object e, int index);
	public virtual int LastIndexOf (Java.Lang.Object o);
	public virtual bool RemoveAll (System.Collections.ICollection c);
	public virtual bool RetainAll (System.Collections.ICollection c);
	public virtual Java.Lang.Object Set (int index, Java.Lang.Object element);
	public virtual System.Collections.IList SubList (int fromIndex, int toIndex);
	public virtual Java.Lang.Object[] ToArray (Java.Lang.Object[] a);
```

Added methods:

```
public virtual void Add (int index, Java.Lang.Object e);
	public virtual bool AddAll (int index, System.Collections.ICollection collection);
	public virtual bool AddAll (System.Collections.ICollection collection);
	public virtual int AddAllAbsent (System.Collections.ICollection collection);
	public virtual bool AddIfAbsent (Java.Lang.Object object);
	public virtual bool ContainsAll (System.Collections.ICollection collection);
	public virtual int IndexOf (Java.Lang.Object object, int from);
	public virtual int IndexOf (Java.Lang.Object object);
	public virtual int LastIndexOf (Java.Lang.Object object, int to);
	public virtual int LastIndexOf (Java.Lang.Object object);
	public virtual bool RemoveAll (System.Collections.ICollection collection);
	public virtual bool RetainAll (System.Collections.ICollection collection);
	public virtual Java.Lang.Object Set (int index, Java.Lang.Object e);
	public virtual System.Collections.IList SubList (int from, int to);
	public virtual Java.Lang.Object[] ToArray (Java.Lang.Object[] contents);
```

### Type Changed: Java.Util.Concurrent.Executors

Removed methods:

```
public static ICallable Callable (Java.Security.IPrivilegedAction p0);
	public static ICallable Callable (Java.Security.IPrivilegedExceptionAction p0);
```

Added methods:

```
public static ICallable Callable (Java.Security.IPrivilegedAction action);
	public static ICallable Callable (Java.Security.IPrivilegedExceptionAction action);
```

### Type Changed: Java.Util.Concurrent.IExecutorService

Removed methods:

```
public virtual System.Collections.IList InvokeAll (System.Collections.ICollection p0);
	public virtual System.Collections.IList InvokeAll (System.Collections.ICollection p0, long p1, TimeUnit p2);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection p0, long p1, TimeUnit p2);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection p0);
```

Added methods:

```
public virtual System.Collections.IList InvokeAll (System.Collections.ICollection tasks);
	public virtual System.Collections.IList InvokeAll (System.Collections.ICollection tasks, long timeout, TimeUnit unit);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection tasks, long timeout, TimeUnit unit);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection tasks);
```

### Type Changed: Java.Util.Concurrent.IExecutorServiceExtensions

Removed methods:

```
public static System.Threading.Tasks.Task<Java.Lang.Object> InvokeAnyAsync (IExecutorService self, System.Collections.ICollection p0);
	public static System.Threading.Tasks.Task<Java.Lang.Object> InvokeAnyAsync (IExecutorService self, System.Collections.ICollection p0, long p1, TimeUnit p2);
```

Added methods:

```
public static System.Threading.Tasks.Task<Java.Lang.Object> InvokeAnyAsync (IExecutorService self, System.Collections.ICollection tasks);
	public static System.Threading.Tasks.Task<Java.Lang.Object> InvokeAnyAsync (IExecutorService self, System.Collections.ICollection tasks, long timeout, TimeUnit unit);
```

### Type Changed: Java.Util.Concurrent.ScheduledThreadPoolExecutor

Removed methods:

```
protected virtual IRunnableScheduledFuture DecorateTask (Java.Lang.IRunnable p0, IRunnableScheduledFuture p1);
	protected virtual IRunnableScheduledFuture DecorateTask (ICallable p0, IRunnableScheduledFuture p1);
```

Added methods:

```
protected virtual IRunnableScheduledFuture DecorateTask (Java.Lang.IRunnable runnable, IRunnableScheduledFuture task);
	protected virtual IRunnableScheduledFuture DecorateTask (ICallable callable, IRunnableScheduledFuture task);
```

### Type Changed: Java.Util.Concurrent.ThreadPoolExecutor

Removed method:

```
public virtual void AllowCoreThreadTimeOut (bool p0);
```

Added method:

```
public virtual void AllowCoreThreadTimeOut (bool value);
```

### Type Changed: Java.Util.Concurrent.TimeUnit

Removed methods:

```
public virtual long ToDays (long p0);
	public virtual long ToHours (long p0);
	public virtual long ToMinutes (long p0);
```

Added methods:

```
public virtual long ToDays (long duration);
	public virtual long ToHours (long duration);
	public virtual long ToMinutes (long duration);
```

## Namespace Java.Util.Concurrent.Atomic

### Type Changed: Java.Util.Concurrent.Atomic.AtomicBoolean

Removed method:

```
public void LazySet (bool p0);
```

Added method:

```
public void LazySet (bool newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicInteger

Removed method:

```
public void LazySet (int p0);
```

Added method:

```
public void LazySet (int newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicIntegerArray

Removed method:

```
public void LazySet (int p0, int p1);
```

Added method:

```
public void LazySet (int i, int newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicIntegerFieldUpdater

Removed method:

```
public virtual void LazySet (Java.Lang.Object p0, int p1);
```

Added method:

```
public virtual void LazySet (Java.Lang.Object obj, int newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicLong

Removed method:

```
public void LazySet (long p0);
```

Added method:

```
public void LazySet (long newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicLongArray

Removed method:

```
public void LazySet (int p0, long p1);
```

Added method:

```
public void LazySet (int i, long newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicLongFieldUpdater

Removed method:

```
public virtual void LazySet (Java.Lang.Object p0, long p1);
```

Added method:

```
public virtual void LazySet (Java.Lang.Object obj, long newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicReference

Removed method:

```
public void LazySet (Java.Lang.Object p0);
```

Added method:

```
public void LazySet (Java.Lang.Object newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicReferenceArray

Removed method:

```
public void LazySet (int p0, Java.Lang.Object p1);
```

Added method:

```
public void LazySet (int i, Java.Lang.Object newValue);
```

### Type Changed: Java.Util.Concurrent.Atomic.AtomicReferenceFieldUpdater

Removed method:

```
public virtual void LazySet (Java.Lang.Object p0, Java.Lang.Object p1);
```

Added method:

```
public virtual void LazySet (Java.Lang.Object obj, Java.Lang.Object newValue);
```

## Namespace Java.Util.Concurrent.Locks

### Type Changed: Java.Util.Concurrent.Locks.LockSupport

Removed methods:

```
public static Java.Lang.Object GetBlocker (Java.Lang.Thread p0);
	public static void Park (Java.Lang.Object p0);
	public static void ParkNanos (Java.Lang.Object p0, long p1);
	public static void ParkUntil (Java.Lang.Object p0, long p1);
```

Added methods:

```
public static Java.Lang.Object GetBlocker (Java.Lang.Thread t);
	public static void Park (Java.Lang.Object blocker);
	public static void ParkNanos (Java.Lang.Object blocker, long nanos);
	public static void ParkUntil (Java.Lang.Object blocker, long deadline);
```

## Namespace Java.Util.Jar

### Type Changed: Java.Util.Jar.JarFile

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Jar.JarInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Jar.JarOutputStream

Added interface:

```
Java.IO.ICloseable
```

## Namespace Java.Util.Regex

### Type Changed: Java.Util.Regex.Pattern

Removed methods:

```
public static Pattern Compile (string pattern, RegexOptions flags);
	public static bool Matches (string regex, string input);
	public static bool Matches (string regex, Java.Lang.ICharSequence input);
	public static string Quote (string s);
	public string[] Split (Java.Lang.ICharSequence inputSeq, int limit);
	public string[] Split (string inputSeq, int limit);
```

Added methods:

```
public static Pattern Compile (string regularExpression, RegexOptions flags);
	public static bool Matches (string regularExpression, string input);
	public static bool Matches (string regularExpression, Java.Lang.ICharSequence input);
	public static string Quote (string string);
	public string[] Split (Java.Lang.ICharSequence input, int limit);
	public string[] Split (string input, int limit);
```

## Namespace Java.Util.Zip

### Type Changed: Java.Util.Zip.Adler32

Removed method:

```
public virtual void Update (byte[] buf, int off, int nbytes);
```

Added method:

```
public virtual void Update (byte[] buf, int offset, int byteCount);
```

### Type Changed: Java.Util.Zip.CheckedInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.CheckedOutputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.CRC32

Removed method:

```
public virtual void Update (byte[] buf, int off, int nbytes);
```

Added method:

```
public virtual void Update (byte[] buf, int offset, int byteCount);
```

### Type Changed: Java.Util.Zip.Deflater

Removed methods:

```
public virtual int Deflate (byte[] buf, int off, int nbytes);
	public System.Threading.Tasks.Task<int> DeflateAsync (byte[] buf, int off, int nbytes);
	public virtual void SetDictionary (byte[] buf, int off, int nbytes);
	public virtual void SetDictionary (byte[] buf);
	public virtual void SetInput (byte[] buf, int off, int nbytes);
```

Added methods:

```
public virtual int Deflate (byte[] buf, int offset, int byteCount);
	public System.Threading.Tasks.Task<int> DeflateAsync (byte[] buf, int offset, int byteCount);
	public virtual void SetDictionary (byte[] buf, int offset, int byteCount);
	public virtual void SetDictionary (byte[] dictionary);
	public virtual void SetInput (byte[] buf, int offset, int byteCount);
```

### Type Changed: Java.Util.Zip.DeflaterInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.DeflaterOutputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.GZIPInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.GZIPOutputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.Inflater

Removed methods:

```
public virtual int Inflate (byte[] buf, int off, int nbytes);
	public System.Threading.Tasks.Task<int> InflateAsync (byte[] buf, int off, int nbytes);
	public virtual void SetDictionary (byte[] buf);
	public virtual void SetDictionary (byte[] buf, int off, int nbytes);
	public virtual void SetInput (byte[] buf, int off, int nbytes);
```

Added methods:

```
public virtual int Inflate (byte[] buf, int offset, int byteCount);
	public System.Threading.Tasks.Task<int> InflateAsync (byte[] buf, int offset, int byteCount);
	public virtual void SetDictionary (byte[] dictionary);
	public virtual void SetDictionary (byte[] dictionary, int offset, int byteCount);
	public virtual void SetInput (byte[] buf, int offset, int byteCount);
```

### Type Changed: Java.Util.Zip.InflaterInputStream

Removed constructors:

```
public InflaterInputStream (System.IO.Stream is, Inflater inf);
	public InflaterInputStream (System.IO.Stream is, Inflater inf, int bsize);
```

Added constructors:

```
public InflaterInputStream (System.IO.Stream is, Inflater inflater);
	public InflaterInputStream (System.IO.Stream is, Inflater inflater, int bsize);
```

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.InflaterOutputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.ZipFile

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.ZipInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Util.Zip.ZipOutputStream

Added interface:

```
Java.IO.ICloseable
```

## Namespace Javax.Crypto

### Type Changed: Javax.Crypto.CipherInputStream

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Javax.Crypto.CipherOutputStream

Added interface:

```
Java.IO.ICloseable
```

## Namespace Javax.Crypto.Spec

### Type Changed: Javax.Crypto.Spec.IvParameterSpec

Removed constructor:

```
public IvParameterSpec (byte[] iv, int offset, int len);
```

Added constructor:

```
public IvParameterSpec (byte[] iv, int offset, int byteCount);
```

## Namespace Javax.Net.Ssl

### Type Changed: Javax.Net.Ssl.KeyStoreBuilderParameters

Removed constructor:

```
public KeyStoreBuilderParameters (System.Collections.Generic.IList<Java.Security.KeyStore.Builder> p0);
```

Added constructor:

```
public KeyStoreBuilderParameters (System.Collections.Generic.IList<Java.Security.KeyStore.Builder> parameters);
```

### Type Changed: Javax.Net.Ssl.SSLServerSocket

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Javax.Net.Ssl.SSLSocket

Added interface:

```
Java.IO.ICloseable
```

## Namespace Javax.Security.Auth

### Type Changed: Javax.Security.Auth.Subject

Removed methods:

```
public static Java.Lang.Object DoAs (Subject p0, Java.Security.IPrivilegedAction p1);
	public static Java.Lang.Object DoAs (Subject p0, Java.Security.IPrivilegedExceptionAction p1);
	public static Java.Lang.Object DoAsPrivileged (Subject p0, Java.Security.IPrivilegedAction p1, Java.Security.AccessControlContext p2);
	public static Java.Lang.Object DoAsPrivileged (Subject p0, Java.Security.IPrivilegedExceptionAction p1, Java.Security.AccessControlContext p2);
```

Added methods:

```
public static Java.Lang.Object DoAs (Subject subject, Java.Security.IPrivilegedAction action);
	public static Java.Lang.Object DoAs (Subject subject, Java.Security.IPrivilegedExceptionAction action);
	public static Java.Lang.Object DoAsPrivileged (Subject subject, Java.Security.IPrivilegedAction action, Java.Security.AccessControlContext context);
	public static Java.Lang.Object DoAsPrivileged (Subject subject, Java.Security.IPrivilegedExceptionAction action, Java.Security.AccessControlContext context);
```

## Namespace Javax.Security.Auth.X500

### Type Changed: Javax.Security.Auth.X500.X500Principal

Removed constructor:

```
public X500Principal (string p0, System.Collections.Generic.IDictionary<System.String,System.String> p1);
```

Added constructor:

```
public X500Principal (string name, System.Collections.Generic.IDictionary<System.String,System.String> keywordMap);
```

Removed method:

```
public string GetName (string p0, System.Collections.Generic.IDictionary<System.String,System.String> p1);
```

Added method:

```
public string GetName (string format, System.Collections.Generic.IDictionary<System.String,System.String> oidMap);
```

## Namespace Javax.Sql

### Type Changed: Javax.Sql.ConnectionEvent

Added constructors:

```
public ConnectionEvent (IPooledConnection theConnection);
	public ConnectionEvent (IPooledConnection theConnection, Java.Sql.SQLException theException);
```

### Type Changed: Javax.Sql.RowSetEvent

Added constructor:

```
public RowSetEvent (IRowSet theSource);
```

Added properties:

```
protected override System.IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
```

### Type Changed: Javax.Sql.StatementEvent

Added constructors:

```
public StatementEvent (IPooledConnection con, Java.Sql.IPreparedStatement statement);
	public StatementEvent (IPooledConnection con, Java.Sql.IPreparedStatement statement, Java.Sql.SQLException exception);
```

Added property:

```
public virtual Java.Sql.IPreparedStatement Statement { get; }
```

### New Type Javax.Sql.IConnectionPoolDataSource

```
public interface IConnectionPoolDataSource : ICommonDataSource, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual IPooledConnection PooledConnection { get; }
	// methods
	public virtual IPooledConnection GetPooledConnection (string theUser, string thePassword);
}
```

### New Type Javax.Sql.IDataSource

```
public interface IDataSource : Java.Sql.IWrapper, ICommonDataSource, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual Java.Sql.IConnection Connection { get; }
	// methods
	public virtual Java.Sql.IConnection GetConnection (string theUsername, string thePassword);
}
```

### New Type Javax.Sql.IPooledConnection

```
public interface IPooledConnection : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual Java.Sql.IConnection Connection { get; }
	// methods
	public virtual void AddConnectionEventListener (IConnectionEventListener theListener);
	public virtual void AddStatementEventListener (IStatementEventListener listener);
	public virtual void Close ();
	public virtual void RemoveConnectionEventListener (IConnectionEventListener theListener);
	public virtual void RemoveStatementEventListener (IStatementEventListener listener);
}
```

### New Type Javax.Sql.IRowSet

```
public interface IRowSet : Java.Sql.IResultSet, Java.Sql.IWrapper, Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual string Command { get; set; }
	public virtual string DataSourceName { get; set; }
	public virtual bool EscapeProcessing { get; set; }
	public virtual int MaxFieldSize { get; set; }
	public virtual int MaxRows { get; set; }
	public virtual string Password { get; set; }
	public virtual int QueryTimeout { get; set; }
	public virtual bool ReadOnly { get; set; }
	public virtual int TransactionIsolation { get; set; }
	public virtual System.Collections.Generic.IDictionary<System.String,Java.Lang.Class> TypeMap { get; set; }
	public virtual string Url { get; set; }
	public virtual string Username { get; set; }
	// methods
	public virtual void AddRowSetListener (IRowSetListener theListener);
	public virtual void ClearParameters ();
	public virtual void Execute ();
	public virtual void RemoveRowSetListener (IRowSetListener theListener);
	public virtual void SetArray (int parameterIndex, Java.Sql.IArray theArray);
	public virtual void SetAsciiStream (int parameterIndex, System.IO.Stream theInputStream);
	public virtual void SetAsciiStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	public virtual void SetAsciiStream (string parameterName, System.IO.Stream theInputStream);
	public virtual void SetAsciiStream (string parameterName, System.IO.Stream theInputStream, int length);
	public virtual void SetBigDecimal (string parameterName, Java.Math.BigDecimal theBigDecimal);
	public virtual void SetBigDecimal (int parameterIndex, Java.Math.BigDecimal theBigDecimal);
	public virtual void SetBinaryStream (string parameterName, System.IO.Stream theInputStream, int length);
	public virtual void SetBinaryStream (string parameterName, System.IO.Stream theInputStream);
	public virtual void SetBinaryStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	public virtual void SetBinaryStream (int parameterIndex, System.IO.Stream theInputStream);
	public virtual void SetBlob (string parameterName, Java.Sql.IBlob theBlob);
	public virtual void SetBlob (string parameterName, System.IO.Stream theInputStream, long length);
	public virtual void SetBlob (string parameterName, System.IO.Stream theInputStream);
	public virtual void SetBlob (int parameterIndex, Java.Sql.IBlob theBlob);
	public virtual void SetBlob (int parameterIndex, System.IO.Stream theInputStream, long length);
	public virtual void SetBlob (int parameterIndex, System.IO.Stream theInputStream);
	public virtual void SetBoolean (string parameterName, bool theBoolean);
	public virtual void SetBoolean (int parameterIndex, bool theBoolean);
	public virtual void SetByte (string parameterName, sbyte theByte);
	public virtual void SetByte (int parameterIndex, sbyte theByte);
	public virtual void SetBytes (int parameterIndex, byte[] theByteArray);
	public virtual void SetBytes (string parameterName, byte[] theByteArray);
	public virtual void SetCharacterStream (string parameterName, Java.IO.Reader theReader, int length);
	public virtual void SetCharacterStream (string parameterName, Java.IO.Reader theReader);
	public virtual void SetCharacterStream (int parameterIndex, Java.IO.Reader theReader, int length);
	public virtual void SetCharacterStream (int parameterIndex, Java.IO.Reader theReader);
	public virtual void SetClob (string parameterName, Java.Sql.IClob theClob);
	public virtual void SetClob (string parameterName, Java.IO.Reader theReader, long length);
	public virtual void SetClob (string parameterName, Java.IO.Reader theReader);
	public virtual void SetClob (int parameterIndex, Java.Sql.IClob theClob);
	public virtual void SetClob (int parameterIndex, Java.IO.Reader theReader, long length);
	public virtual void SetClob (int parameterIndex, Java.IO.Reader theReader);
	public virtual void SetConcurrency (int concurrency);
	public virtual void SetDate (string parameterName, Java.Sql.Date theDate, Java.Util.Calendar theCalendar);
	public virtual void SetDate (string parameterName, Java.Sql.Date theDate);
	public virtual void SetDate (int parameterIndex, Java.Sql.Date theDate, Java.Util.Calendar theCalendar);
	public virtual void SetDate (int parameterIndex, Java.Sql.Date theDate);
	public virtual void SetDouble (int parameterIndex, double theDouble);
	public virtual void SetDouble (string parameterName, double theDouble);
	public virtual void SetFloat (string parameterName, float theFloat);
	public virtual void SetFloat (int parameterIndex, float theFloat);
	public virtual void SetInt (string parameterName, int theInteger);
	public virtual void SetInt (int parameterIndex, int theInteger);
	public virtual void SetLong (int parameterIndex, long theLong);
	public virtual void SetLong (string parameterName, long theLong);
	public virtual void SetNCharacterStream (string parameterName, Java.IO.Reader theReader, long length);
	public virtual void SetNCharacterStream (string parameterName, Java.IO.Reader theReader);
	public virtual void SetNCharacterStream (int parameterIndex, Java.IO.Reader theReader, long length);
	public virtual void SetNCharacterStream (int parameterIndex, Java.IO.Reader theReader);
	public virtual void SetNClob (string parameterName, Java.Sql.INClob theNClob);
	public virtual void SetNClob (string parameterName, Java.IO.Reader theReader, long length);
	public virtual void SetNClob (string parameterName, Java.IO.Reader theReader);
	public virtual void SetNClob (int parameterIndex, Java.IO.Reader theReader);
	public virtual void SetNClob (int parameterIndex, Java.IO.Reader theReader, long length);
	public virtual void SetNClob (int parameterIndex, Java.Sql.INClob theNClob);
	public virtual void SetNString (int parameterIndex, string theNString);
	public virtual void SetNString (string parameterName, string theNString);
	public virtual void SetNull (string parameterName, int sqlType, string typeName);
	public virtual void SetNull (string parameterName, int sqlType);
	public virtual void SetNull (int parameterIndex, int sqlType, string typeName);
	public virtual void SetNull (int parameterIndex, int sqlType);
	public virtual void SetObject (string parameterName, Java.Lang.Object theObject, int targetSqlType, int scale);
	public virtual void SetObject (string parameterName, Java.Lang.Object theObject, int targetSqlType);
	public virtual void SetObject (string parameterName, Java.Lang.Object theObject);
	public virtual void SetObject (int parameterIndex, Java.Lang.Object theObject, int targetSqlType, int scale);
	public virtual void SetObject (int parameterIndex, Java.Lang.Object theObject, int targetSqlType);
	public virtual void SetObject (int parameterIndex, Java.Lang.Object theObject);
	public virtual void SetRef (int parameterIndex, Java.Sql.IRef theRef);
	public virtual void SetRowId (string parameterName, Java.Sql.IRowId theRowId);
	public virtual void SetRowId (int parameterIndex, Java.Sql.IRowId theRowId);
	public virtual void SetShort (int parameterIndex, short theShort);
	public virtual void SetShort (string parameterName, short theShort);
	public virtual void SetSQLXML (int parameterIndex, Java.Sql.ISQLXML theSQLXML);
	public virtual void SetSQLXML (string parameterName, Java.Sql.ISQLXML theSQLXML);
	public virtual void SetString (string parameterName, string theString);
	public virtual void SetString (int parameterIndex, string theString);
	public virtual void SetTime (string parameterName, Java.Sql.Time theTime, Java.Util.Calendar theCalendar);
	public virtual void SetTime (string parameterName, Java.Sql.Time theTime);
	public virtual void SetTime (int parameterIndex, Java.Sql.Time theTime, Java.Util.Calendar theCalendar);
	public virtual void SetTime (int parameterIndex, Java.Sql.Time theTime);
	public virtual void SetTimestamp (string parameterName, Java.Sql.Timestamp theTimestamp, Java.Util.Calendar theCalendar);
	public virtual void SetTimestamp (string parameterName, Java.Sql.Timestamp theTimestamp);
	public virtual void SetTimestamp (int parameterIndex, Java.Sql.Timestamp theTimestamp, Java.Util.Calendar theCalendar);
	public virtual void SetTimestamp (int parameterIndex, Java.Sql.Timestamp theTimestamp);
	public virtual void SetType (int type);
	public virtual void SetURL (int parameterIndex, Java.Net.URL theURL);
}
```

### New Type Javax.Sql.IRowSetInternal

```
public interface IRowSetInternal : Android.Runtime.IJavaObject, System.IDisposable {
	// properties
	public virtual Java.Sql.IConnection Connection { get; }
	public virtual Java.Sql.IResultSet Original { get; }
	public virtual Java.Sql.IResultSet OriginalRow { get; }
	// methods
	public virtual Java.Lang.Object[] GetParams ();
	public virtual void SetMetaData (IRowSetMetaData theMetaData);
}
```

### New Type Javax.Sql.IRowSetReader

```
public interface IRowSetReader : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void ReadData (IRowSetInternal theCaller);
}
```

### New Type Javax.Sql.IRowSetWriter

```
public interface IRowSetWriter : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual bool WriteData (IRowSetInternal theRowSet);
}
```

## Namespace Javax.Xml.Datatype

### Type Changed: Javax.Xml.Datatype.DatatypeFactory

Removed method:

```
public static DatatypeFactory NewInstance (string p0, Java.Lang.ClassLoader p1);
```

Added method:

```
public static DatatypeFactory NewInstance (string factoryClassName, Java.Lang.ClassLoader classLoader);
```

## Namespace Javax.Xml.Parsers

### Type Changed: Javax.Xml.Parsers.DocumentBuilder

Removed methods:

```
public virtual Org.W3c.Dom.IDocument Parse (System.IO.Stream stream, string systemId);
	public virtual Org.W3c.Dom.IDocument Parse (Org.Xml.Sax.InputSource source);
	public virtual Org.W3c.Dom.IDocument Parse (System.IO.Stream stream);
	public virtual Org.W3c.Dom.IDocument Parse (Java.IO.File file);
	public System.Threading.Tasks.Task<Org.W3c.Dom.IDocument> ParseAsync (Org.Xml.Sax.InputSource source);
	public System.Threading.Tasks.Task<Org.W3c.Dom.IDocument> ParseAsync (System.IO.Stream stream, string systemId);
	public System.Threading.Tasks.Task<Org.W3c.Dom.IDocument> ParseAsync (System.IO.Stream stream);
	public System.Threading.Tasks.Task<Org.W3c.Dom.IDocument> ParseAsync (Java.IO.File file);
	public virtual void SetEntityResolver (Org.Xml.Sax.IEntityResolver resolver);
	public virtual void SetErrorHandler (Org.Xml.Sax.IErrorHandler handler);
```

Added methods:

```
public virtual Org.W3c.Dom.IDocument Parse (System.IO.Stream is, string systemId);
	public virtual Org.W3c.Dom.IDocument Parse (Org.Xml.Sax.InputSource is);
	public virtual Org.W3c.Dom.IDocument Parse (System.IO.Stream is);
	public virtual Org.W3c.Dom.IDocument Parse (Java.IO.File f);
	public System.Threading.Tasks.Task<Org.W3c.Dom.IDocument> ParseAsync (Org.Xml.Sax.InputSource is);
	public System.Threading.Tasks.Task<Org.W3c.Dom.IDocument> ParseAsync (System.IO.Stream is, string systemId);
	public System.Threading.Tasks.Task<Org.W3c.Dom.IDocument> ParseAsync (System.IO.Stream is);
	public System.Threading.Tasks.Task<Org.W3c.Dom.IDocument> ParseAsync (Java.IO.File f);
	public virtual void SetEntityResolver (Org.Xml.Sax.IEntityResolver er);
	public virtual void SetErrorHandler (Org.Xml.Sax.IErrorHandler eh);
```

### Type Changed: Javax.Xml.Parsers.DocumentBuilderFactory

Removed method:

```
public static DocumentBuilderFactory NewInstance (string p0, Java.Lang.ClassLoader p1);
```

Added method:

```
public static DocumentBuilderFactory NewInstance (string factoryClassName, Java.Lang.ClassLoader classLoader);
```

### Type Changed: Javax.Xml.Parsers.FactoryConfigurationError

Removed constructors:

```
public FactoryConfigurationError (Java.Lang.Exception cause);
	public FactoryConfigurationError (Java.Lang.Exception cause, string message);
	public FactoryConfigurationError (string message);
```

Added constructors:

```
public FactoryConfigurationError (Java.Lang.Exception e);
	public FactoryConfigurationError (Java.Lang.Exception e, string msg);
	public FactoryConfigurationError (string msg);
```

### Type Changed: Javax.Xml.Parsers.SAXParser

Removed methods:

```
public virtual void Parse (System.IO.Stream stream, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public virtual void Parse (System.IO.Stream stream, Org.Xml.Sax.Helpers.DefaultHandler handler, string systemId);
	public virtual void Parse (string uri, Org.Xml.Sax.HandlerBase handler);
	public virtual void Parse (string uri, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public virtual void Parse (Org.Xml.Sax.InputSource source, Org.Xml.Sax.HandlerBase handler);
	public virtual void Parse (Org.Xml.Sax.InputSource source, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public virtual void Parse (System.IO.Stream stream, Org.Xml.Sax.HandlerBase handler, string systemId);
	public virtual void Parse (System.IO.Stream stream, Org.Xml.Sax.HandlerBase handler);
	public virtual void Parse (Java.IO.File file, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public virtual void Parse (Java.IO.File file, Org.Xml.Sax.HandlerBase handler);
	public System.Threading.Tasks.Task ParseAsync (Org.Xml.Sax.InputSource source, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public System.Threading.Tasks.Task ParseAsync (Java.IO.File file, Org.Xml.Sax.HandlerBase handler);
	public System.Threading.Tasks.Task ParseAsync (string uri, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public System.Threading.Tasks.Task ParseAsync (Org.Xml.Sax.InputSource source, Org.Xml.Sax.HandlerBase handler);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, Org.Xml.Sax.HandlerBase handler, string systemId);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, Org.Xml.Sax.HandlerBase handler);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, Org.Xml.Sax.Helpers.DefaultHandler handler, string systemId);
	public System.Threading.Tasks.Task ParseAsync (Java.IO.File file, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public System.Threading.Tasks.Task ParseAsync (string uri, Org.Xml.Sax.HandlerBase handler);
```

Added methods:

```
public virtual void Parse (System.IO.Stream is, Org.Xml.Sax.Helpers.DefaultHandler dh);
	public virtual void Parse (System.IO.Stream is, Org.Xml.Sax.Helpers.DefaultHandler dh, string systemId);
	public virtual void Parse (string uri, Org.Xml.Sax.HandlerBase hb);
	public virtual void Parse (string uri, Org.Xml.Sax.Helpers.DefaultHandler dh);
	public virtual void Parse (Org.Xml.Sax.InputSource is, Org.Xml.Sax.HandlerBase hb);
	public virtual void Parse (Org.Xml.Sax.InputSource is, Org.Xml.Sax.Helpers.DefaultHandler dh);
	public virtual void Parse (System.IO.Stream is, Org.Xml.Sax.HandlerBase hb, string systemId);
	public virtual void Parse (System.IO.Stream is, Org.Xml.Sax.HandlerBase hb);
	public virtual void Parse (Java.IO.File f, Org.Xml.Sax.Helpers.DefaultHandler dh);
	public virtual void Parse (Java.IO.File f, Org.Xml.Sax.HandlerBase hb);
	public System.Threading.Tasks.Task ParseAsync (Org.Xml.Sax.InputSource is, Org.Xml.Sax.Helpers.DefaultHandler dh);
	public System.Threading.Tasks.Task ParseAsync (Java.IO.File f, Org.Xml.Sax.HandlerBase hb);
	public System.Threading.Tasks.Task ParseAsync (string uri, Org.Xml.Sax.Helpers.DefaultHandler dh);
	public System.Threading.Tasks.Task ParseAsync (Org.Xml.Sax.InputSource is, Org.Xml.Sax.HandlerBase hb);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream is, Org.Xml.Sax.HandlerBase hb, string systemId);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream is, Org.Xml.Sax.HandlerBase hb);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream is, Org.Xml.Sax.Helpers.DefaultHandler dh);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream is, Org.Xml.Sax.Helpers.DefaultHandler dh, string systemId);
	public System.Threading.Tasks.Task ParseAsync (Java.IO.File f, Org.Xml.Sax.Helpers.DefaultHandler dh);
	public System.Threading.Tasks.Task ParseAsync (string uri, Org.Xml.Sax.HandlerBase hb);
```

### Type Changed: Javax.Xml.Parsers.SAXParserFactory

Removed method:

```
public static SAXParserFactory NewInstance (string p0, Java.Lang.ClassLoader p1);
```

Added method:

```
public static SAXParserFactory NewInstance (string factoryClassName, Java.Lang.ClassLoader classLoader);
```

## Namespace Javax.Xml.Transform

### Type Changed: Javax.Xml.Transform.TransformerFactory

Removed method:

```
public static TransformerFactory NewInstance (string p0, Java.Lang.ClassLoader p1);
```

Added method:

```
public static TransformerFactory NewInstance (string factoryClassName, Java.Lang.ClassLoader classLoader);
```

## Namespace Javax.Xml.Validation

### Type Changed: Javax.Xml.Validation.SchemaFactory

Removed method:

```
public static SchemaFactory NewInstance (string p0, string p1, Java.Lang.ClassLoader p2);
```

Added method:

```
public static SchemaFactory NewInstance (string schemaLanguage, string factoryClassName, Java.Lang.ClassLoader classLoader);
```

## Namespace Org.Apache.Http.Conn

### Type Changed: Org.Apache.Http.Conn.EofSensorInputStream

Added interface:

```
Java.IO.ICloseable
```

## Namespace Org.Json

### Type Changed: Org.Json.JSONArray

Removed constructors:

```
public JSONArray (string string);
	public JSONArray (System.Collections.ICollection collection);
	public JSONArray (JSONTokener x);
```

Added constructors:

```
public JSONArray (string json);
	public JSONArray (System.Collections.ICollection copyFrom);
	public JSONArray (JSONTokener readFrom);
```

Removed methods:

```
public virtual bool OptBoolean (int index, bool defaultValue);
	public virtual double OptDouble (int index, double defaultValue);
	public virtual int OptInt (int index, int defaultValue);
	public virtual long OptLong (int index, long defaultValue);
	public virtual string OptString (int index, string defaultValue);
	public virtual string ToString (int indentFactor);
```

Added methods:

```
public virtual bool OptBoolean (int index, bool fallback);
	public virtual double OptDouble (int index, double fallback);
	public virtual int OptInt (int index, int fallback);
	public virtual long OptLong (int index, long fallback);
	public virtual string OptString (int index, string fallback);
	public virtual string ToString (int indentSpaces);
```

### Type Changed: Org.Json.JSONException

Removed constructor:

```
public JSONException (string message);
```

Added constructor:

```
public JSONException (string s);
```

### Type Changed: Org.Json.JSONObject

Removed constructors:

```
public JSONObject (string string);
	public JSONObject (System.Collections.IDictionary map);
	public JSONObject (JSONObject jo, string[] sa);
	public JSONObject (JSONTokener x);
```

Added constructors:

```
public JSONObject (string json);
	public JSONObject (System.Collections.IDictionary copyFrom);
	public JSONObject (JSONObject copyFrom, string[] names);
	public JSONObject (JSONTokener readFrom);
```

Removed methods:

```
public virtual JSONObject Accumulate (string key, Java.Lang.Object value);
	public virtual Java.Lang.Object Get (string key);
	public virtual bool GetBoolean (string key);
	public virtual double GetDouble (string key);
	public virtual int GetInt (string key);
	public virtual JSONArray GetJSONArray (string key);
	public virtual JSONObject GetJSONObject (string key);
	public virtual long GetLong (string key);
	public virtual string GetString (string key);
	public virtual bool Has (string key);
	public virtual bool IsNull (string key);
	public static string NumberToString (Java.Lang.Number n);
	public virtual Java.Lang.Object Opt (string key);
	public virtual bool OptBoolean (string key);
	public virtual bool OptBoolean (string key, bool defaultValue);
	public virtual double OptDouble (string key, double defaultValue);
	public virtual double OptDouble (string key);
	public virtual int OptInt (string key);
	public virtual int OptInt (string key, int defaultValue);
	public virtual JSONArray OptJSONArray (string key);
	public virtual JSONObject OptJSONObject (string key);
	public virtual long OptLong (string key);
	public virtual long OptLong (string key, long defaultValue);
	public virtual string OptString (string key, string defaultValue);
	public virtual string OptString (string key);
	public virtual JSONObject Put (string key, long value);
	public virtual JSONObject Put (string key, Java.Lang.Object value);
	public virtual JSONObject Put (string key, int value);
	public virtual JSONObject Put (string key, double value);
	public virtual JSONObject Put (string key, bool value);
	public virtual JSONObject PutOpt (string key, Java.Lang.Object value);
	public static string Quote (string string);
	public virtual Java.Lang.Object Remove (string key);
	public virtual string ToString (int indentFactor);
```

Added methods:

```
public virtual JSONObject Accumulate (string name, Java.Lang.Object value);
	public virtual Java.Lang.Object Get (string name);
	public virtual bool GetBoolean (string name);
	public virtual double GetDouble (string name);
	public virtual int GetInt (string name);
	public virtual JSONArray GetJSONArray (string name);
	public virtual JSONObject GetJSONObject (string name);
	public virtual long GetLong (string name);
	public virtual string GetString (string name);
	public virtual bool Has (string name);
	public virtual bool IsNull (string name);
	public static string NumberToString (Java.Lang.Number number);
	public virtual Java.Lang.Object Opt (string name);
	public virtual bool OptBoolean (string name);
	public virtual bool OptBoolean (string name, bool fallback);
	public virtual double OptDouble (string name, double fallback);
	public virtual double OptDouble (string name);
	public virtual int OptInt (string name);
	public virtual int OptInt (string name, int fallback);
	public virtual JSONArray OptJSONArray (string name);
	public virtual JSONObject OptJSONObject (string name);
	public virtual long OptLong (string name);
	public virtual long OptLong (string name, long fallback);
	public virtual string OptString (string name, string fallback);
	public virtual string OptString (string name);
	public virtual JSONObject Put (string name, long value);
	public virtual JSONObject Put (string name, Java.Lang.Object value);
	public virtual JSONObject Put (string name, int value);
	public virtual JSONObject Put (string name, double value);
	public virtual JSONObject Put (string name, bool value);
	public virtual JSONObject PutOpt (string name, Java.Lang.Object value);
	public static string Quote (string data);
	public virtual Java.Lang.Object Remove (string name);
	public virtual string ToString (int indentSpaces);
```

### Type Changed: Org.Json.JSONStringer

Removed methods:

```
public virtual JSONStringer Key (string s);
	public virtual JSONStringer Value (bool b);
	public virtual JSONStringer Value (double d);
	public virtual JSONStringer Value (Java.Lang.Object o);
	public virtual JSONStringer Value (long l);
```

Added methods:

```
public virtual JSONStringer Key (string name);
	public virtual JSONStringer Value (bool value);
	public virtual JSONStringer Value (double value);
	public virtual JSONStringer Value (Java.Lang.Object value);
	public virtual JSONStringer Value (long value);
```

### Type Changed: Org.Json.JSONTokener

Removed constructor:

```
public JSONTokener (string s);
```

Added constructor:

```
public JSONTokener (string in);
```

Removed methods:

```
public static int Dehexchar (char c);
	public virtual string Next (int n);
	public virtual string NextTo (string delimiters);
	public virtual string NextTo (char d);
	public virtual void SkipPast (string to);
```

Added methods:

```
public static int Dehexchar (char hex);
	public virtual string Next (int length);
	public virtual string NextTo (string excluded);
	public virtual string NextTo (char excluded);
	public virtual void SkipPast (string thru);
```

## Namespace Org.W3c.Dom

### Type Changed: Org.W3c.Dom.IDocument

Removed methods:

```
public virtual INode AdoptNode (INode p0);
	public virtual INode RenameNode (INode p0, string p1, string p2);
```

Added methods:

```
public virtual INode AdoptNode (INode source);
	public virtual INode RenameNode (INode n, string namespaceURI, string qualifiedName);
```

### Type Changed: Org.W3c.Dom.IDOMImplementation

Removed method:

```
public virtual Java.Lang.Object GetFeature (string p0, string p1);
```

Added method:

```
public virtual Java.Lang.Object GetFeature (string feature, string version);
```

### Type Changed: Org.W3c.Dom.IElement

Removed methods:

```
public virtual void SetIdAttribute (string p0, bool p1);
	public virtual void SetIdAttributeNode (IAttr p0, bool p1);
	public virtual void SetIdAttributeNS (string p0, string p1, bool p2);
```

Added methods:

```
public virtual void SetIdAttribute (string name, bool isId);
	public virtual void SetIdAttributeNode (IAttr idAttr, bool isId);
	public virtual void SetIdAttributeNS (string namespaceURI, string localName, bool isId);
```

### Type Changed: Org.W3c.Dom.INode

Removed methods:

```
public virtual short CompareDocumentPosition (INode p0);
	public virtual Java.Lang.Object GetFeature (string p0, string p1);
	public virtual Java.Lang.Object GetUserData (string p0);
	public virtual bool IsDefaultNamespace (string p0);
	public virtual bool IsEqualNode (INode p0);
	public virtual bool IsSameNode (INode p0);
	public virtual string LookupNamespaceURI (string p0);
	public virtual string LookupPrefix (string p0);
	public virtual Java.Lang.Object SetUserData (string p0, Java.Lang.Object p1, IUserDataHandler p2);
```

Added methods:

```
public virtual short CompareDocumentPosition (INode other);
	public virtual Java.Lang.Object GetFeature (string feature, string version);
	public virtual Java.Lang.Object GetUserData (string key);
	public virtual bool IsDefaultNamespace (string namespaceURI);
	public virtual bool IsEqualNode (INode arg);
	public virtual bool IsSameNode (INode other);
	public virtual string LookupNamespaceURI (string prefix);
	public virtual string LookupPrefix (string namespaceURI);
	public virtual Java.Lang.Object SetUserData (string key, Java.Lang.Object data, IUserDataHandler handler);
```

### Type Changed: Org.W3c.Dom.IText

Removed method:

```
public virtual IText ReplaceWholeText (string p0);
```

Added method:

```
public virtual IText ReplaceWholeText (string content);
```
