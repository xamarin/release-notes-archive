---
id: 23025D83-1B79-4133-932E-01A06AA4698D
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

Obsoleted field:

```
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

## Namespace Android.App.Backup

### Type Changed: Android.App.Backup.BackupDataInputStream

Added interface:

```
Java.IO.ICloseable
```

## Namespace Android.Bluetooth

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

## Namespace Android.Media

### Type Changed: Android.Media.AudioTrack

Added constructor:

```
public AudioTrack (Stream streamType, int sampleRateInHz, ChannelOut channelConfig, Encoding audioFormat, int bufferSizeInBytes, AudioTrackMode mode);
```

Obsoleted constructor:

```
[Obsolete ("ChannelConfiguration is obsolete. Please use another overload with ChannelOut instead")]
	public AudioTrack (Stream streamType, int sampleRateInHz, ChannelConfiguration channelConfig, Encoding audioFormat, int bufferSizeInBytes, AudioTrackMode mode);
```

## Namespace Android.Net

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

## Namespace Android.OS

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

## Namespace Android.Provider

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

## Namespace Android.Views

### Type Changed: Android.Views.Display

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual int Orientation { get; }
```

### Type Changed: Android.Views.KeyCharacterMap

Removed methods:

```
public virtual int Get (Keycode keyCode, int meta);
	public virtual char GetMatch (Keycode keyCode, char[] chars, int modifiers);
```

Added methods:

```
public virtual int Get (Keycode keyCode, MetaKeyStates meta);
	public virtual char GetMatch (Keycode keyCode, char[] chars, MetaKeyStates modifiers);
```

### Type Changed: Android.Views.KeyEvent

Removed methods:

```
public virtual char GetMatch (char[] chars, int modifiers);
	public virtual int GetUnicodeChar (int meta);
```

Added methods:

```
public virtual char GetMatch (char[] chars, MetaKeyStates modifiers);
	public virtual int GetUnicodeChar (MetaKeyStates meta);
```

### Type Changed: Android.Views.MenuPerformFlags

Removed value:

```
AppendToGroup = 1,
```

### Type Changed: Android.Views.MotionEvent

Removed methods:

```
public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointers, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, float x, float y, MetaKeyStates metaState);
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
```

Added methods:

```
public static MotionEvent Obtain (long downTime, long eventTime, int action, int pointers, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, float x, float y, MetaKeyStates metaState);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
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

### Type Changed: Android.Webkit.WebSettings

Obsoleted property:

```
[Obsolete ("deprecated")]
	public virtual bool PluginsEnabled { get; set; }
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

### Type Changed: Java.IO.DataInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.DataOutputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FileInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.FileOutputStream

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

### Type Changed: Java.IO.InputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.InputStreamReader

Added interface:

```
ICloseable
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

Removed method:

```
public Java.Lang.Object ReadObject ();
```

Added method:

```
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

### Type Changed: Java.IO.PipedInputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PipedOutputStream

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PipedReader

Added interface:

```
ICloseable
```

### Type Changed: Java.IO.PipedWriter

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

### Type Changed: Java.IO.Reader

Added interface:

```
ICloseable
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
	public virtual long Skip (long toSkip);
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
	public static System.Threading.Tasks.Task<long> SkipAsync (IObjectInput self, long toSkip);
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

Added method:

```
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

## Namespace Java.Net

### Type Changed: Java.Net.DatagramSocket

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Net.MulticastSocket

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Net.ServerSocket

Added interface:

```
Java.IO.ICloseable
```

### Type Changed: Java.Net.Socket

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

### Type Changed: Java.Net.URLClassLoader

Added interface:

```
Java.IO.ICloseable
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

## Namespace Java.Security

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

## Namespace Java.Util

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
public static int BinarySearch (Java.Lang.Object[] array, Java.Lang.Object object);
	public static int BinarySearch (Java.Lang.Object[] array, Java.Lang.Object object, IComparator comparator);
```

Added methods:

```
public static int BinarySearch (Java.Lang.Object[] array, Java.Lang.Object value);
	public static int BinarySearch (Java.Lang.Object[] array, Java.Lang.Object value, IComparator comparator);
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

## Namespace Java.Util.Concurrent

### Removed Type Java.Util.Concurrent.IBlockingQueueExtensions 

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

## Namespace Java.Util.Zip

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

### Type Changed: Java.Util.Zip.InflaterInputStream

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

## Namespace Javax.Net.Ssl

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
