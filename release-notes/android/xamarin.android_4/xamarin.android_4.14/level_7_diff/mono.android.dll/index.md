---
id: 38A567CF-3114-4DC8-9837-26347D5D7601
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

## Namespace Android.Views

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

### Type Changed: Java.Lang.JavaSystem

Added method:

```
public static Java.Nio.Channels.IChannel InheritedChannel ();
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

## Namespace Org.Apache.Http.Conn

### Type Changed: Org.Apache.Http.Conn.EofSensorInputStream

Added interface:

```
Java.IO.ICloseable
```
