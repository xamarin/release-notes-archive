---
id: DCF703A5-0E4B-4DA2-BB45-0D1BDA1ABA82
title: "Mono.Android.dll"
---

# Mono.Android.dll

<h2 id='Android.Accounts'>Namespace: Android.Accounts</h2>

<h3 id='Android.Accounts.IAccountManagerFutureExtensions'>New Type: Android.Accounts.IAccountManagerFutureExtensions</h3>

```
public static class IAccountManagerFutureExtensions {
	
	public static System.Threading.Tasks.Task GetResultAsync (IAccountManagerFuture self, long timeout, Java.Util.Concurrent.TimeUnit unit);
}
```

<h2 id='Android.App'>Namespace: Android.App</h2>

<h3 id='Android.App.Activity'>Type Changed: Android.App.Activity</h3>

Removed:

```
public class Activity : Android.Views.ContextThemeWrapper, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, LayoutInflater.Android.Views.IFactory, LayoutInflater.Android.Views.IFactory2, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Activity : Android.Views.ContextThemeWrapper, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, LayoutInflater.Android.Views.IFactory, LayoutInflater.Android.Views.IFactory2, View.Android.Views.IOnCreateContextMenuListener {
```

<h3 id='Android.App.Dialog'>Type Changed: Android.App.Dialog</h3>

Removed:

```
public class Dialog : Java.Lang.Object, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
 	public T FindViewById<T> (int id) where T : Android.Views.View;
```

Added:

```
public class Dialog : Java.Lang.Object, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
 	public T FindViewById<T> (int id) where T : Android.Views.View;
```

<h3 id='Android.App.ProgressDialog'>Type Changed: Android.App.ProgressDialog</h3>

Added:

```
public virtual void SetProgressPercentFormat (Java.Text.NumberFormat format);
```

<h2 id='Android.App.Backup'>Namespace: Android.App.Backup</h2>

<h3 id='Android.App.Backup.BackupAgent'>Type Changed: Android.App.Backup.BackupAgent</h3>

Added:

```
public System.Threading.Tasks.Task FullBackupFileAsync (Java.IO.File file, FullBackupDataOutput output);
```

<h3 id='Android.App.Backup.BackupDataInput'>Type Changed: Android.App.Backup.BackupDataInput</h3>

Added:

```
public System.Threading.Tasks.Task<int> ReadEntityDataAsync (byte [] data, int offset, int size);
 	public System.Threading.Tasks.Task<bool> ReadNextHeaderAsync ();
 	public System.Threading.Tasks.Task SkipEntityDataAsync ();
```

<h3 id='Android.App.Backup.BackupDataOutput'>Type Changed: Android.App.Backup.BackupDataOutput</h3>

Added:

```
public System.Threading.Tasks.Task<int> WriteEntityDataAsync (byte [] data, int size);
 	public System.Threading.Tasks.Task<int> WriteEntityHeaderAsync (string key, int dataSize);
```

<h3 id='Android.App.Backup.IBackupHelperExtensions'>New Type: Android.App.Backup.IBackupHelperExtensions</h3>

```
public static class IBackupHelperExtensions {
	
	public static System.Threading.Tasks.Task PerformBackupAsync (IBackupHelper self, Android.OS.ParcelFileDescriptor oldState, BackupDataOutput data, Android.OS.ParcelFileDescriptor newState);
}
```

<h2 id='Android.Bluetooth'>Namespace: Android.Bluetooth</h2>

<h3 id='Android.Bluetooth.BluetoothServerSocket'>Type Changed: Android.Bluetooth.BluetoothServerSocket</h3>

Added:

```
public System.Threading.Tasks.Task<BluetoothSocket> AcceptAsync ();
 	public System.Threading.Tasks.Task<BluetoothSocket> AcceptAsync (int timeout);
```

<h3 id='Android.Bluetooth.BluetoothSocket'>Type Changed: Android.Bluetooth.BluetoothSocket</h3>

Added:

```
public System.Threading.Tasks.Task ConnectAsync ();
```

<h2 id='Android.Content'>Namespace: Android.Content</h2>

<h3 id='Android.Content.IntentFilter'>Type Changed: Android.Content.IntentFilter</h3>

Added:

```
public virtual void WriteToXml (Org.XmlPull.V1.IXmlSerializer serializer);
```

<h3 id='Android.Content.Loader'>Type Changed: Android.Content.Loader</h3>

Added:

```
public System.Threading.Tasks.Task DumpAsync (string prefix, Java.IO.FileDescriptor fd, Java.IO.PrintWriter writer, string [] args);
```

<h2 id='Android.Content.Res'>Namespace: Android.Content.Res</h2>

<h3 id='Android.Content.Res.AssetManager'>Type Changed: Android.Content.Res.AssetManager</h3>

Added:

```
public System.Threading.Tasks.Task<string []> ListAsync (string path);
```

<h2 id='Android.Gestures'>Namespace: Android.Gestures</h2>

<h3 id='Android.Gestures.GestureStore'>Type Changed: Android.Gestures.GestureStore</h3>

Added:

```
public System.Threading.Tasks.Task LoadAsync (System.IO.Stream stream);
 	public System.Threading.Tasks.Task LoadAsync (System.IO.Stream stream, bool closeStream);
 	public System.Threading.Tasks.Task SaveAsync (System.IO.Stream stream);
 	public System.Threading.Tasks.Task SaveAsync (System.IO.Stream stream, bool closeStream);
```

<h2 id='Android.Graphics'>Namespace: Android.Graphics</h2>

<h3 id='Android.Graphics.Bitmap'>Type Changed: Android.Graphics.Bitmap</h3>

Added:

```
public System.Threading.Tasks.Task<bool> CompressAsync (CompressFormat format, int quality, System.IO.Stream stream);
 	public System.Threading.Tasks.Task CopyPixelsFromBufferAsync (Java.Nio.Buffer src);
 	public System.Threading.Tasks.Task CopyPixelsToBufferAsync (Java.Nio.Buffer dst);
```

<h3 id='Android.Graphics.BitmapFactory'>Type Changed: Android.Graphics.BitmapFactory</h3>

Added:

```
public static System.Threading.Tasks.Task<Bitmap> DecodeByteArrayAsync (byte [] data, int offset, int length);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeByteArrayAsync (byte [] data, int offset, int length, Options opts);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeFileAsync (string pathName);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeFileAsync (string pathName, Options opts);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeFileDescriptorAsync (Java.IO.FileDescriptor fd);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeFileDescriptorAsync (Java.IO.FileDescriptor fd, Rect outPadding, Options opts);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeResourceAsync (Android.Content.Res.Resources res, int id);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeResourceAsync (Android.Content.Res.Resources res, int id, Options opts);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeResourceStreamAsync (Android.Content.Res.Resources res, Android.Util.TypedValue value, System.IO.Stream is, Rect pad, Options opts);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeStreamAsync (System.IO.Stream is);
 	public static System.Threading.Tasks.Task<Bitmap> DecodeStreamAsync (System.IO.Stream is, Rect outPadding, Options opts);
```

<h3 id='Android.Graphics.Movie'>Type Changed: Android.Graphics.Movie</h3>

Added:

```
public static System.Threading.Tasks.Task<Movie> DecodeByteArrayAsync (byte [] data, int offset, int length);
 	public static System.Threading.Tasks.Task<Movie> DecodeFileAsync (string pathName);
 	public static System.Threading.Tasks.Task<Movie> DecodeStreamAsync (System.IO.Stream is);
```

<h3 id='Android.Graphics.Picture'>Type Changed: Android.Graphics.Picture</h3>

Added:

```
public static System.Threading.Tasks.Task<Picture> CreateFromStreamAsync (System.IO.Stream stream);
 	public System.Threading.Tasks.Task WriteToStreamAsync (System.IO.Stream stream);
```

<h3 id='Android.Graphics.YuvImage'>Type Changed: Android.Graphics.YuvImage</h3>

Added:

```
public System.Threading.Tasks.Task<bool> CompressToJpegAsync (Rect rectangle, int quality, System.IO.Stream stream);
```

<h2 id='Android.Graphics.Drawables'>Namespace: Android.Graphics.Drawables</h2>

<h3 id='Android.Graphics.Drawables.Drawable'>Type Changed: Android.Graphics.Drawables.Drawable</h3>

Added:

```
public static System.Threading.Tasks.Task<Drawable> CreateFromPathAsync (string pathName);
 	public static System.Threading.Tasks.Task<Drawable> CreateFromResourceStreamAsync (Android.Content.Res.Resources res, Android.Util.TypedValue value, System.IO.Stream is, string srcName);
 	public static System.Threading.Tasks.Task<Drawable> CreateFromResourceStreamAsync (Android.Content.Res.Resources res, Android.Util.TypedValue value, System.IO.Stream is, string srcName, BitmapFactory.Android.Graphics.Options opts);
 	public static System.Threading.Tasks.Task<Drawable> CreateFromStreamAsync (System.IO.Stream is, string srcName);
 	public static System.Threading.Tasks.Task<Drawable> CreateFromXmlAsync (Android.Content.Res.Resources r, System.Xml.XmlReader parser);
 	public System.Threading.Tasks.Task InflateAsync (Android.Content.Res.Resources r, System.Xml.XmlReader parser, Android.Util.IAttributeSet attrs);
```

<h2 id='Android.Hardware.Usb'>Namespace: Android.Hardware.Usb</h2>

<h3 id='Android.Hardware.Usb.UsbDeviceConnection'>Type Changed: Android.Hardware.Usb.UsbDeviceConnection</h3>

Added:

```
public System.Threading.Tasks.Task<int> BulkTransferAsync (UsbEndpoint endpoint, byte [] buffer, int length, int timeout);
 	public System.Threading.Tasks.Task<UsbRequest> RequestWaitAsync ();
```

<h2 id='Android.Locations'>Namespace: Android.Locations</h2>

<h3 id='Android.Locations.Geocoder'>Type Changed: Android.Locations.Geocoder</h3>

Added:

```
public System.Threading.Tasks.Task<System.Collections.Generic.IList<Address>> GetFromLocationAsync (double latitude, double longitude, int maxResults);
 	public System.Threading.Tasks.Task<System.Collections.Generic.IList<Address>> GetFromLocationNameAsync (string locationName, int maxResults);
 	public System.Threading.Tasks.Task<System.Collections.Generic.IList<Address>> GetFromLocationNameAsync (string locationName, int maxResults, double lowerLeftLatitude, double lowerLeftLongitude, double upperRightLatitude, double upperRightLongitude);
```

<h2 id='Android.Media'>Namespace: Android.Media</h2>

<h3 id='Android.Media.AudioManager'>Type Changed: Android.Media.AudioManager</h3>

Added:

```
public System.Threading.Tasks.Task LoadSoundEffectsAsync ();
```

<h3 id='Android.Media.AudioRecord'>Type Changed: Android.Media.AudioRecord</h3>

Added:

```
public System.Threading.Tasks.Task<int> ReadAsync (byte [] audioData, int offsetInBytes, int sizeInBytes);
 	public System.Threading.Tasks.Task<int> ReadAsync (Java.Nio.ByteBuffer audioBuffer, int sizeInBytes);
 	public System.Threading.Tasks.Task<int> ReadAsync (short [] audioData, int offsetInShorts, int sizeInShorts);
```

<h3 id='Android.Media.AudioTrack'>Type Changed: Android.Media.AudioTrack</h3>

Added:

```
public System.Threading.Tasks.Task<int> WriteAsync (byte [] audioData, int offsetInBytes, int sizeInBytes);
 	public System.Threading.Tasks.Task<int> WriteAsync (short [] audioData, int offsetInShorts, int sizeInShorts);
```

<h3 id='Android.Media.FaceDetector'>Type Changed: Android.Media.FaceDetector</h3>

Added:

```
public System.Threading.Tasks.Task<int> FindFacesAsync (Android.Graphics.Bitmap bitmap, Face[] faces);
```

<h3 id='Android.Media.JetPlayer'>Type Changed: Android.Media.JetPlayer</h3>

Added:

```
public System.Threading.Tasks.Task<bool> LoadJetFileAsync (Android.Content.Res.AssetFileDescriptor afd);
 	public System.Threading.Tasks.Task<bool> LoadJetFileAsync (string path);
```

<h3 id='Android.Media.MediaMetadataRetriever'>Type Changed: Android.Media.MediaMetadataRetriever</h3>

Added:

```
public System.Threading.Tasks.Task SetDataSourceAsync (Android.Content.Context p0, Android.Net.Uri p1);
 	public System.Threading.Tasks.Task SetDataSourceAsync (Java.IO.FileDescriptor p0);
 	public System.Threading.Tasks.Task SetDataSourceAsync (Java.IO.FileDescriptor p0, long p1, long p2);
 	public System.Threading.Tasks.Task SetDataSourceAsync (string p0);
 	public System.Threading.Tasks.Task SetDataSourceAsync (string uri, System.Collections.Generic.IDictionary<string,string> headers);
```

<h3 id='Android.Media.MediaPlayer'>Type Changed: Android.Media.MediaPlayer</h3>

Added:

```
public System.Threading.Tasks.Task SetDataSourceAsync (Android.Content.Context context, Android.Net.Uri uri);
 	public System.Threading.Tasks.Task SetDataSourceAsync (Android.Content.Context context, Android.Net.Uri uri, System.Collections.Generic.IDictionary<string,string> headers);
 	public System.Threading.Tasks.Task SetDataSourceAsync (Java.IO.FileDescriptor fd);
 	public System.Threading.Tasks.Task SetDataSourceAsync (Java.IO.FileDescriptor fd, long offset, long length);
 	public System.Threading.Tasks.Task SetDataSourceAsync (string path);
```

<h3 id='Android.Media.SoundPool'>Type Changed: Android.Media.SoundPool</h3>

Added:

```
public System.Threading.Tasks.Task<int> LoadAsync (Android.Content.Res.AssetFileDescriptor afd, int priority);
 	public System.Threading.Tasks.Task<int> LoadAsync (Android.Content.Context context, int resId, int priority);
 	public System.Threading.Tasks.Task<int> LoadAsync (Java.IO.FileDescriptor fd, long offset, long length, int priority);
 	public System.Threading.Tasks.Task<int> LoadAsync (string path, int priority);
```

<h3 id='Android.Media.ThumbnailUtils'>Type Changed: Android.Media.ThumbnailUtils</h3>

Added:

```
public static System.Threading.Tasks.Task<Android.Graphics.Bitmap> CreateVideoThumbnailAsync (string filePath, Android.Provider.ThumbnailKind kind);
 	public static System.Threading.Tasks.Task<Android.Graphics.Bitmap> ExtractThumbnailAsync (Android.Graphics.Bitmap source, int width, int height);
 	public static System.Threading.Tasks.Task<Android.Graphics.Bitmap> ExtractThumbnailAsync (Android.Graphics.Bitmap source, int width, int height, ThumnailExtractOptions options);
```

<h2 id='Android.Mtp'>Namespace: Android.Mtp</h2>

<h3 id='Android.Mtp.MtpDevice'>Type Changed: Android.Mtp.MtpDevice</h3>

Added:

```
public System.Threading.Tasks.Task<bool> DeleteObjectAsync (int objectHandle);
 	public System.Threading.Tasks.Task<byte []> GetObjectAsync (int objectHandle, int objectSize);
 	public System.Threading.Tasks.Task<byte []> GetThumbnailAsync (int objectHandle);
 	public System.Threading.Tasks.Task<bool> ImportFileAsync (int objectHandle, string destPath);
```

<h2 id='Android.Net'>Namespace: Android.Net</h2>

<h3 id='Android.Net.ConnectivityManager'>Type Changed: Android.Net.ConnectivityManager</h3>

Added:

```
public System.Threading.Tasks.Task<bool> RequestRouteToHostAsync (ConnectivityType networkType, int hostAddress);
```

<h3 id='Android.Net.LocalServerSocket'>Type Changed: Android.Net.LocalServerSocket</h3>

Added:

```
public System.Threading.Tasks.Task<LocalSocket> AcceptAsync ();
```

<h3 id='Android.Net.LocalSocket'>Type Changed: Android.Net.LocalSocket</h3>

Added:

```
public System.Threading.Tasks.Task ConnectAsync (LocalSocketAddress endpoint);
 	public System.Threading.Tasks.Task ConnectAsync (LocalSocketAddress endpoint, int timeout);
```

<h3 id='Android.Net.SSLCertificateSocketFactory'>Type Changed: Android.Net.SSLCertificateSocketFactory</h3>

Added:

```
public static Org.Apache.Http.Conn.Ssl.SSLSocketFactory GetHttpSocketFactory (int handshakeTimeoutMillis, SSLSessionCache cache);
```

<h2 id='Android.Net.Http'>Namespace: Android.Net.Http</h2>

<h3 id='Android.Net.Http.AndroidHttpClient'>Type Changed: Android.Net.Http.AndroidHttpClient</h3>

Removed:

```
public sealed class AndroidHttpClient : Java.Lang.Object {
```

Added:

```
public sealed class AndroidHttpClient : Java.Lang.Object, Org.Apache.Http.Client.IHttpClient {
 	public static Org.Apache.Http.Entity.AbstractHttpEntity GetCompressedEntity (byte [] data, Android.Content.ContentResolver resolver);
 	public static System.IO.Stream GetUngzippedContent (Org.Apache.Http.IHttpEntity entity);
 	public static void ModifyRequestToAcceptGzipResponse (Org.Apache.Http.IHttpRequest request);
 	public Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request);
 	public Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
 	public Java.Lang.Object Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler);
 	public Java.Lang.Object Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
 	public Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request);
 	public Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Protocol.IHttpContext context);
 	public Java.Lang.Object Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler);
 	public Java.Lang.Object Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
 	public System.Threading.Tasks.Task<Org.Apache.Http.IHttpResponse> ExecuteAsync (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request);
 	public System.Threading.Tasks.Task<Org.Apache.Http.IHttpResponse> ExecuteAsync (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
 	public System.Threading.Tasks.Task<Java.Lang.Object> ExecuteAsync (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler);
 	public System.Threading.Tasks.Task<Java.Lang.Object> ExecuteAsync (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
 	public System.Threading.Tasks.Task<Org.Apache.Http.IHttpResponse> ExecuteAsync (Org.Apache.Http.Client.Methods.IHttpUriRequest request);
 	public System.Threading.Tasks.Task<Org.Apache.Http.IHttpResponse> ExecuteAsync (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Protocol.IHttpContext context);
 	public System.Threading.Tasks.Task<Java.Lang.Object> ExecuteAsync (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler);
 	public System.Threading.Tasks.Task<Java.Lang.Object> ExecuteAsync (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Client.IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
 	public Org.Apache.Http.Conn.IClientConnectionManager ConnectionManager {
 		get;
 	}
 	public Org.Apache.Http.Params.IHttpParams Params {
 		get;
 	}
```

<h2 id='Android.Nfc.Tech'>Namespace: Android.Nfc.Tech</h2>

<h3 id='Android.Nfc.Tech.ITagTechnologyExtensions'>New Type: Android.Nfc.Tech.ITagTechnologyExtensions</h3>

```
public static class ITagTechnologyExtensions {
	
	public static System.Threading.Tasks.Task ConnectAsync (ITagTechnology self);
}
```

<h3 id='Android.Nfc.Tech.IsoDep'>Type Changed: Android.Nfc.Tech.IsoDep</h3>

Added:

```
public System.Threading.Tasks.Task<byte []> TransceiveAsync (byte [] p0);
```

<h3 id='Android.Nfc.Tech.MifareClassic'>Type Changed: Android.Nfc.Tech.MifareClassic</h3>

Added:

```
public System.Threading.Tasks.Task DecrementAsync (int p0, int p1);
 	public System.Threading.Tasks.Task IncrementAsync (int p0, int p1);
 	public System.Threading.Tasks.Task<byte []> ReadBlockAsync (int p0);
 	public System.Threading.Tasks.Task RestoreAsync (int p0);
 	public System.Threading.Tasks.Task<byte []> TransceiveAsync (byte [] p0);
 	public System.Threading.Tasks.Task TransferAsync (int p0);
 	public System.Threading.Tasks.Task WriteBlockAsync (int p0, byte [] p1);
```

<h3 id='Android.Nfc.Tech.MifareUltralight'>Type Changed: Android.Nfc.Tech.MifareUltralight</h3>

Added:

```
public System.Threading.Tasks.Task<byte []> ReadPagesAsync (int p0);
 	public System.Threading.Tasks.Task<byte []> TransceiveAsync (byte [] p0);
 	public System.Threading.Tasks.Task WritePageAsync (int p0, byte [] p1);
```

<h3 id='Android.Nfc.Tech.Ndef'>Type Changed: Android.Nfc.Tech.Ndef</h3>

Added:

```
public System.Threading.Tasks.Task<bool> MakeReadOnlyAsync ();
 	public System.Threading.Tasks.Task WriteNdefMessageAsync (Android.Nfc.NdefMessage p0);
```

<h3 id='Android.Nfc.Tech.NdefFormatable'>Type Changed: Android.Nfc.Tech.NdefFormatable</h3>

Added:

```
public System.Threading.Tasks.Task FormatAsync (Android.Nfc.NdefMessage p0);
 	public System.Threading.Tasks.Task FormatReadOnlyAsync (Android.Nfc.NdefMessage p0);
```

<h3 id='Android.Nfc.Tech.NfcA'>Type Changed: Android.Nfc.Tech.NfcA</h3>

Added:

```
public System.Threading.Tasks.Task<byte []> TransceiveAsync (byte [] p0);
```

<h3 id='Android.Nfc.Tech.NfcB'>Type Changed: Android.Nfc.Tech.NfcB</h3>

Added:

```
public System.Threading.Tasks.Task<byte []> TransceiveAsync (byte [] p0);
```

<h3 id='Android.Nfc.Tech.NfcF'>Type Changed: Android.Nfc.Tech.NfcF</h3>

Added:

```
public System.Threading.Tasks.Task<byte []> TransceiveAsync (byte [] p0);
```

<h3 id='Android.Nfc.Tech.NfcV'>Type Changed: Android.Nfc.Tech.NfcV</h3>

Added:

```
public System.Threading.Tasks.Task<byte []> TransceiveAsync (byte [] p0);
```

<h2 id='Android.OS'>Namespace: Android.OS</h2>

<h3 id='Android.OS.AsyncTask'>Type Changed: Android.OS.AsyncTask</h3>

Added:

```
public AsyncTask ExecuteOnExecutor (Java.Util.Concurrent.IExecutor exec, params Java.Lang.Object[] params);
 	public static Java.Util.Concurrent.IExecutor SerialExecutor {
 		get;
 		set;
 	}
 	public static Java.Util.Concurrent.IExecutor ThreadPoolExecutor {
 		get;
 		set;
 	}
```

<h3 id='Android.OS.Debug'>Type Changed: Android.OS.Debug</h3>

Added:

```
public static System.Threading.Tasks.Task DumpHprofDataAsync (string fileName);
 	public static System.Threading.Tasks.Task<bool> DumpServiceAsync (string name, Java.IO.FileDescriptor fd, string [] args);
```

<h3 id='Android.OS.Handler'>Type Changed: Android.OS.Handler</h3>

Added:

```
public System.Threading.Tasks.Task DumpAsync (Android.Util.IPrinter pw, string prefix);
```

<h2 id='Android.Runtime'>Namespace: Android.Runtime</h2>

<h3 id='Android.Runtime.JavaList'>Type Changed: Android.Runtime.JavaList</h3>

Removed:

```
public int Add (object item);
 	public virtual int IndexOf (object item);
```

Added:

```
public int Add (object item);
 	public virtual int IndexOf (object item);
```

<h2 id='Android.Sax'>Namespace: Android.Sax</h2>

<h3 id='Android.Sax.Element'>Type Changed: Android.Sax.Element</h3>

Added:

```
public virtual void SetElementListener (IElementListener elementListener);
 	public virtual void SetStartElementListener (IStartElementListener startElementListener);
 	public virtual void SetTextElementListener (ITextElementListener elementListener);
 	public event EventHandler<StartElementEventArgs> StartElement;
```

<h3 id='Android.Sax.IElementListener'>New Type: Android.Sax.IElementListener</h3>

```
public interface IElementListener : IDisposable, IEndElementListener, Android.Runtime.IJavaObject, IStartElementListener {
}
```

<h3 id='Android.Sax.IStartElementListener'>New Type: Android.Sax.IStartElementListener</h3>

```
public interface IStartElementListener : IDisposable, Android.Runtime.IJavaObject {
	
	void Start (Org.Xml.Sax.IAttributes attributes);
}
```

<h3 id='Android.Sax.ITextElementListener'>New Type: Android.Sax.ITextElementListener</h3>

```
public interface ITextElementListener : IDisposable, IEndTextElementListener, Android.Runtime.IJavaObject, IStartElementListener {
}
```

<h3 id='Android.Sax.RootElement'>Type Changed: Android.Sax.RootElement</h3>

Added:

```
public virtual Org.Xml.Sax.IContentHandler ContentHandler {
 		get;
 	}
```

<h3 id='Android.Sax.StartElementEventArgs'>New Type: Android.Sax.StartElementEventArgs</h3>

```
public class StartElementEventArgs : EventArgs {
	
	public StartElementEventArgs (Org.Xml.Sax.IAttributes attributes);
	
	public Org.Xml.Sax.IAttributes Attributes {
		get;
	}
}
```

<h2 id='Android.Test'>Namespace: Android.Test</h2>

<h3 id='Android.Test.FlakyTest'>Type Changed: Android.Test.FlakyTest</h3>

Removed:

```
public abstract class FlakyTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class FlakyTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h3 id='Android.Test.IFlakyTest'>New Type: Android.Test.IFlakyTest</h3>

```
public interface IFlakyTest : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
	
	int Tolerance ();
}
```

<h3 id='Android.Test.IUiThreadTest'>New Type: Android.Test.IUiThreadTest</h3>

```
public interface IUiThreadTest : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Android.Test.UiThreadTest'>Type Changed: Android.Test.UiThreadTest</h3>

Removed:

```
public abstract class UiThreadTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class UiThreadTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h2 id='Android.Test.Suitebuilder.Annotation'>Namespace: Android.Test.Suitebuilder.Annotation</h2>

<h3 id='Android.Test.Suitebuilder.Annotation.ILargeTest'>New Type: Android.Test.Suitebuilder.Annotation.ILargeTest</h3>

```
public interface ILargeTest : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Android.Test.Suitebuilder.Annotation.IMediumTest'>New Type: Android.Test.Suitebuilder.Annotation.IMediumTest</h3>

```
public interface IMediumTest : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Android.Test.Suitebuilder.Annotation.ISmallTest'>New Type: Android.Test.Suitebuilder.Annotation.ISmallTest</h3>

```
public interface ISmallTest : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Android.Test.Suitebuilder.Annotation.ISmoke'>New Type: Android.Test.Suitebuilder.Annotation.ISmoke</h3>

```
public interface ISmoke : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Android.Test.Suitebuilder.Annotation.ISuppress'>New Type: Android.Test.Suitebuilder.Annotation.ISuppress</h3>

```
public interface ISuppress : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Android.Test.Suitebuilder.Annotation.LargeTest'>Type Changed: Android.Test.Suitebuilder.Annotation.LargeTest</h3>

Removed:

```
public abstract class LargeTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class LargeTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h3 id='Android.Test.Suitebuilder.Annotation.MediumTest'>Type Changed: Android.Test.Suitebuilder.Annotation.MediumTest</h3>

Removed:

```
public abstract class MediumTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class MediumTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h3 id='Android.Test.Suitebuilder.Annotation.SmallTest'>Type Changed: Android.Test.Suitebuilder.Annotation.SmallTest</h3>

Removed:

```
public abstract class SmallTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class SmallTest : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h3 id='Android.Test.Suitebuilder.Annotation.Smoke'>Type Changed: Android.Test.Suitebuilder.Annotation.Smoke</h3>

Removed:

```
public abstract class Smoke : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class Smoke : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h3 id='Android.Test.Suitebuilder.Annotation.Suppress'>Type Changed: Android.Test.Suitebuilder.Annotation.Suppress</h3>

Removed:

```
public abstract class Suppress : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class Suppress : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h2 id='Android.Text'>Namespace: Android.Text</h2>

<h3 id='Android.Text.Html'>Type Changed: Android.Text.Html</h3>

Added:

```
public static ISpanned FromHtml (string source, IImageGetter imageGetter, ITagHandler tagHandler);
 	public interface ITagHandler : IDisposable, Android.Runtime.IJavaObject {
 		
 		void HandleTag (bool opening, string tag, IEditable output, Org.Xml.Sax.IXMLReader xmlReader);
 	}
```

<h2 id='Android.Text.Format'>Namespace: Android.Text.Format</h2>

<h3 id='Android.Text.Format.DateFormat'>Type Changed: Android.Text.Format.DateFormat</h3>

Added:

```
public static Java.Text.DateFormat GetDateFormat (Android.Content.Context context);
 	public static Java.Text.DateFormat GetLongDateFormat (Android.Content.Context context);
 	public static Java.Text.DateFormat GetMediumDateFormat (Android.Content.Context context);
 	public static Java.Text.DateFormat GetTimeFormat (Android.Content.Context context);
```

<h2 id='Android.Util'>Namespace: Android.Util</h2>

<h3 id='Android.Util.Base64InputStream'>New Type: Android.Util.Base64InputStream</h3>

```
public class Base64InputStream : Java.IO.FilterInputStream {
	
	protected Base64InputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Base64InputStream (System.IO.Stream in, int flags);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Android.Util.Base64OutputStream'>New Type: Android.Util.Base64OutputStream</h3>

```
public class Base64OutputStream : Java.IO.FilterOutputStream {
	
	protected Base64OutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Base64OutputStream (System.IO.Stream out, int flags);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Android.Util.EventLog'>Type Changed: Android.Util.EventLog</h3>

Added:

```
public static System.Threading.Tasks.Task ReadEventsAsync (int [] tags, System.Collections.Generic.ICollection<Event> output);
 	public static System.Threading.Tasks.Task<int> WriteEventAsync (int tag, int value);
 	public static System.Threading.Tasks.Task<int> WriteEventAsync (int tag, long value);
 	public static System.Threading.Tasks.Task<int> WriteEventAsync (int tag, params Java.Lang.Object[] list);
 	public static System.Threading.Tasks.Task<int> WriteEventAsync (int tag, string str);
```

<h3 id='Android.Util.IPrinterExtensions'>New Type: Android.Util.IPrinterExtensions</h3>

```
public static class IPrinterExtensions {
	
	public static System.Threading.Tasks.Task PrintlnAsync (IPrinter self, string x);
}
```

<h3 id='Android.Util.JsonReader'>Type Changed: Android.Util.JsonReader</h3>

Added:

```
public System.Threading.Tasks.Task BeginArrayAsync ();
 	public System.Threading.Tasks.Task BeginObjectAsync ();
 	public System.Threading.Tasks.Task EndArrayAsync ();
 	public System.Threading.Tasks.Task EndObjectAsync ();
 	public System.Threading.Tasks.Task<bool> NextBooleanAsync ();
 	public System.Threading.Tasks.Task<double> NextDoubleAsync ();
 	public System.Threading.Tasks.Task<int> NextIntAsync ();
 	public System.Threading.Tasks.Task<long> NextLongAsync ();
 	public System.Threading.Tasks.Task<string> NextNameAsync ();
 	public System.Threading.Tasks.Task NextNullAsync ();
 	public System.Threading.Tasks.Task<string> NextStringAsync ();
 	public System.Threading.Tasks.Task<JsonToken> PeekAsync ();
 	public System.Threading.Tasks.Task SkipValueAsync ();
```

<h3 id='Android.Util.JsonWriter'>Type Changed: Android.Util.JsonWriter</h3>

Added:

```
public System.Threading.Tasks.Task<JsonWriter> BeginArrayAsync ();
 	public System.Threading.Tasks.Task<JsonWriter> BeginObjectAsync ();
 	public System.Threading.Tasks.Task<JsonWriter> EndArrayAsync ();
 	public System.Threading.Tasks.Task<JsonWriter> EndObjectAsync ();
 	public System.Threading.Tasks.Task FlushAsync ();
 	public System.Threading.Tasks.Task<JsonWriter> NameAsync (string name);
 	public System.Threading.Tasks.Task<JsonWriter> NullValueAsync ();
 	public System.Threading.Tasks.Task<JsonWriter> ValueAsync (bool value);
 	public System.Threading.Tasks.Task<JsonWriter> ValueAsync (double value);
 	public System.Threading.Tasks.Task<JsonWriter> ValueAsync (long value);
 	public System.Threading.Tasks.Task<JsonWriter> ValueAsync (Java.Lang.Number value);
 	public System.Threading.Tasks.Task<JsonWriter> ValueAsync (string value);
```

<h3 id='Android.Util.Xml'>Type Changed: Android.Util.Xml</h3>

Added:

```
public static Org.XmlPull.V1.IXmlSerializer NewSerializer ();
 	public static void Parse (Java.IO.Reader in, Org.Xml.Sax.IContentHandler contentHandler);
 	public static void Parse (System.IO.Stream in, Encoding encoding, Org.Xml.Sax.IContentHandler contentHandler);
 	public static void Parse (string xml, Org.Xml.Sax.IContentHandler contentHandler);
 	public static System.Threading.Tasks.Task ParseAsync (Java.IO.Reader in, Org.Xml.Sax.IContentHandler contentHandler);
 	public static System.Threading.Tasks.Task ParseAsync (System.IO.Stream in, Encoding encoding, Org.Xml.Sax.IContentHandler contentHandler);
 	public static System.Threading.Tasks.Task ParseAsync (string xml, Org.Xml.Sax.IContentHandler contentHandler);
```

<h2 id='Android.Views'>Namespace: Android.Views</h2>

<h3 id='Android.Views.View'>Type Changed: Android.Views.View</h3>

Removed:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, ICallback, Drawable.Android.Graphics.Drawables.ICallback {
```

Added:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, Drawable.Android.Graphics.Drawables.ICallback, ICallback {
 	public static Android.Util.Property ScaleXs {
 		get;
 		set;
 	}
 	public static Android.Util.Property ScaleYs {
 		get;
 		set;
 	}
```

<h3 id='Android.Views.ViewDebug'>Type Changed: Android.Views.ViewDebug</h3>

Removed:

```
public abstract class CapturedViewProperty : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
 	public abstract class ExportedProperty : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
 	public abstract class FlagToString : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
 	public abstract class IntToString : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
	public abstract class CapturedViewProperty : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
 	[Obsolete]
	public abstract class ExportedProperty : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
 	[Obsolete]
	public abstract class FlagToString : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
 	[Obsolete]
	public abstract class IntToString : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h2 id='Android.Webkit'>Namespace: Android.Webkit</h2>

<h3 id='Android.Webkit.JavascriptInterface'>New Type: Android.Webkit.JavascriptInterface</h3>

```
[Obsolete]
public abstract class JavascriptInterface : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
	
	protected JavascriptInterface (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public abstract Java.Lang.Class AnnotationType ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Android.Webkit.JavascriptInterfaceAttribute'>New Type: Android.Webkit.JavascriptInterfaceAttribute</h3>

```
public class JavascriptInterfaceAttribute : Attribute {
	
	public JavascriptInterfaceAttribute ();
}
```

<h2 id='Android.Widget'>Namespace: Android.Widget</h2>

<h3 id='Android.Widget.RemoteViews'>Type Changed: Android.Widget.RemoteViews</h3>

Removed:

```
public abstract class RemoteView : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
	public abstract class RemoteView : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h2 id='Dalvik.Annotation'>Namespace: Dalvik.Annotation</h2>

<h3 id='Dalvik.Annotation.ITestTarget'>New Type: Dalvik.Annotation.ITestTarget</h3>

```
public interface ITestTarget : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
	
	string ConceptName ();
	Java.Lang.Class[] MethodArgs ();
	string MethodName ();
}
```

<h3 id='Dalvik.Annotation.ITestTargetClass'>New Type: Dalvik.Annotation.ITestTargetClass</h3>

```
public interface ITestTargetClass : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Class Value ();
}
```

<h3 id='Dalvik.Annotation.TestTarget'>Type Changed: Dalvik.Annotation.TestTarget</h3>

Removed:

```
public abstract class TestTarget : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class TestTarget : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h3 id='Dalvik.Annotation.TestTargetClass'>Type Changed: Dalvik.Annotation.TestTargetClass</h3>

Removed:

```
public abstract class TestTargetClass : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class TestTargetClass : Java.Lang.Object, Java.Lang.Annotation.IAnnotation {
```

<h2 id='Dalvik.SystemInterop'>Namespace: Dalvik.SystemInterop</h2>

<h3 id='Dalvik.SystemInterop.AllocationLimitError'>New Type: Dalvik.SystemInterop.AllocationLimitError</h3>

```
public class AllocationLimitError : Java.Lang.VirtualMachineError {
	
	protected AllocationLimitError (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AllocationLimitError ();
	public AllocationLimitError (string detailMessage);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.BaseDexClassLoader'>New Type: Dalvik.SystemInterop.BaseDexClassLoader</h3>

```
public class BaseDexClassLoader : Java.Lang.ClassLoader {
	
	protected BaseDexClassLoader (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BaseDexClassLoader (string dexPath, Java.IO.File optimizedDirectory, string libraryPath, Java.Lang.ClassLoader parent);
	
	public virtual string FindLibrary (string name);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.DexClassLoader'>New Type: Dalvik.SystemInterop.DexClassLoader</h3>

```
public class DexClassLoader : BaseDexClassLoader {
	
	protected DexClassLoader (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DexClassLoader (string dexPath, string dexOutputDir, string libPath, Java.Lang.ClassLoader parent);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.DexFile'>New Type: Dalvik.SystemInterop.DexFile</h3>

```
public sealed class DexFile : Java.Lang.Object {
	
	public DexFile (Java.IO.File file);
	public DexFile (string fileName);
	
	public static bool IsDexOptNeeded (string fileName);
	public static DexFile LoadDex (string sourcePathName, string outputPathName, int flags);
	public void Close ();
	public Java.Util.IEnumeration Entries ();
	public Java.Lang.Class LoadClass (string name, Java.Lang.ClassLoader loader);
	
	public string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.PathClassLoader'>New Type: Dalvik.SystemInterop.PathClassLoader</h3>

```
public class PathClassLoader : BaseDexClassLoader {
	
	protected PathClassLoader (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PathClassLoader (string path, Java.Lang.ClassLoader parent);
	public PathClassLoader (string path, string libPath, Java.Lang.ClassLoader parent);
	
	public override string FindLibrary (string libname);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.PotentialDeadlockError'>New Type: Dalvik.SystemInterop.PotentialDeadlockError</h3>

```
public class PotentialDeadlockError : Java.Lang.VirtualMachineError {
	
	protected PotentialDeadlockError (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PotentialDeadlockError ();
	public PotentialDeadlockError (string detailMessage);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.StaleDexCacheError'>New Type: Dalvik.SystemInterop.StaleDexCacheError</h3>

```
public class StaleDexCacheError : Java.Lang.VirtualMachineError {
	
	protected StaleDexCacheError (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StaleDexCacheError ();
	public StaleDexCacheError (string detailMessage);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.TemporaryDirectory'>New Type: Dalvik.SystemInterop.TemporaryDirectory</h3>

```
public class TemporaryDirectory : Java.Lang.Object {
	
	protected TemporaryDirectory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TemporaryDirectory ();
	
	public static void SetUpDirectory (Java.IO.File baseDir);
	public static void SetUpDirectory (string baseDir);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.TouchDex'>New Type: Dalvik.SystemInterop.TouchDex</h3>

```
public class TouchDex : Java.Lang.Object {
	
	protected TouchDex (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TouchDex ();
	
	public static void Main (string [] args);
	public static int Start (string dexFiles);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.VMDebug'>New Type: Dalvik.SystemInterop.VMDebug</h3>

```
public sealed class VMDebug : Java.Lang.Object {
	
	public static void DumpHprofData (string fileName);
	public static int GetAllocCount (int kind);
	public static void GetInstructionCount (int [] counts);
	public static long LastDebuggerActivity ();
	public static void PrintLoadedClasses (int flags);
	public static void ResetAllocCount (int kinds);
	public static void ResetInstructionCount ();
	public static int SetAllocationLimit (int limit);
	public static int SetGlobalAllocationLimit (int limit);
	public static void StartAllocCounting ();
	public static void StartEmulatorTracing ();
	public static void StartInstructionCounting ();
	public static void StartMethodTracing ();
	public static void StartMethodTracing (string traceFileName, int bufferSize, int flags);
	public static void StopAllocCounting ();
	public static void StopEmulatorTracing ();
	public static void StopInstructionCounting ();
	public static void StopMethodTracing ();
	public static long ThreadCpuTimeNanos ();
	
	public static bool IsDebuggerConnected {
		get;
	}
	public static bool IsDebuggingEnabled {
		get;
	}
	public static int LoadedClassCount {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string DefaultMethodTraceFileName = "/sdcard/dmtrace.trace";
	public const int KindAllCounts = -1;
	public const int KindGlobalAllocatedBytes = 2;
	public const int KindGlobalAllocatedObjects = 1;
	public const int KindGlobalClassInitCount = 32;
	public const int KindGlobalClassInitTime = 64;
	public const int KindGlobalExtAllocatedBytes = 8192;
	public const int KindGlobalExtAllocatedObjects = 4096;
	public const int KindGlobalExtFreedBytes = 32768;
	public const int KindGlobalExtFreedObjects = 16384;
	public const int KindGlobalFreedBytes = 8;
	public const int KindGlobalFreedObjects = 4;
	public const int KindGlobalGcInvocations = 16;
	public const int KindThreadAllocatedBytes = 131072;
	public const int KindThreadAllocatedObjects = 65536;
	public const int KindThreadClassInitCount = 2097152;
	public const int KindThreadClassInitTime = 4194304;
	public const int KindThreadExtAllocatedBytes = 536870912;
	public const int KindThreadExtAllocatedObjects = 268435456;
	public const int KindThreadExtFreedBytes = -2147483648;
	public const int KindThreadExtFreedObjects = 1073741824;
	public const int KindThreadFreedBytes = 524288;
	public const int KindThreadFreedObjects = 262144;
	public const int KindThreadGcInvocations = 1048576;
	public const int TraceCountAllocs = 1;
}
```

<h3 id='Dalvik.SystemInterop.VMRuntime'>New Type: Dalvik.SystemInterop.VMRuntime</h3>

```
public sealed class VMRuntime : Java.Lang.Object {
	
	public void GcSoftReferences ();
	public void RunFinalizationSync ();
	public long SetMinimumHeapSize (long size);
	public float SetTargetHeapUtilization (float newTarget);
	
	public static VMRuntime Runtime {
		get;
	}
	public long ExternalBytesAllocated {
		get;
	}
	public long MinimumHeapSize {
		get;
	}
	public float TargetHeapUtilization {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.VMStack'>New Type: Dalvik.SystemInterop.VMStack</h3>

```
public sealed class VMStack : Java.Lang.Object {
	
	public VMStack ();
	
	public static Java.Lang.Class[] GetClasses (int maxDepth, bool stopAtPrivileged);
	public static Java.Lang.StackTraceElement[] GetThreadStackTrace (Java.Lang.Thread t);
	
	public static Java.Lang.ClassLoader CallingClassLoader {
		get;
	}
	public static Java.Lang.ClassLoader CallingClassLoader2 {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Dalvik.SystemInterop.Zygote'>New Type: Dalvik.SystemInterop.Zygote</h3>

```
public class Zygote : Java.Lang.Object {
	
	protected Zygote (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static int Fork ();
	public static int ForkAndSpecialize (int uid, int gid, int [] gids, bool enableDebugger, int [] [] rlimits);
	public static int ForkAndSpecialize (int uid, int gid, int [] gids, int debugFlags, int [] [] rlimits);
	public static int ForkSystemServer (int uid, int gid, int [] gids, bool enableDebugger, int [] [] rlimits);
	public static int ForkSystemServer (int uid, int gid, int [] gids, int debugFlags, int [] [] rlimits);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int DebugEnableAssert = 4;
	public const int DebugEnableCheckjni = 2;
	public const int DebugEnableDebugger = 1;
	public const int DebugEnableSafemode = 8;
}
```

<h2 id='Java.Awt.Font'>Namespace: Java.Awt.Font</h2>

<h3 id='Java.Awt.Font.TextAttribute'>New Type: Java.Awt.Font.TextAttribute</h3>

```
public sealed class TextAttribute : Java.Text.AttributedCharacterIteratorAttribute {
	
	public static TextAttribute Background {
		get;
		set;
	}
	public static TextAttribute BidiEmbedding {
		get;
		set;
	}
	public static TextAttribute CharReplacement {
		get;
		set;
	}
	public static TextAttribute Family {
		get;
		set;
	}
	public static TextAttribute Font {
		get;
		set;
	}
	public static TextAttribute Foreground {
		get;
		set;
	}
	public static TextAttribute InputMethodHighlight {
		get;
		set;
	}
	public static TextAttribute InputMethodUnderline {
		get;
		set;
	}
	public static TextAttribute Justification {
		get;
		set;
	}
	public static Java.Lang.Float JustificationFull {
		get;
		set;
	}
	public static Java.Lang.Float JustificationNone {
		get;
		set;
	}
	public static TextAttribute Kerning {
		get;
		set;
	}
	public static Java.Lang.Integer KerningOn {
		get;
		set;
	}
	public static TextAttribute Ligatures {
		get;
		set;
	}
	public static Java.Lang.Integer LigaturesOn {
		get;
		set;
	}
	public static TextAttribute NumericShaping {
		get;
		set;
	}
	public static TextAttribute Posture {
		get;
		set;
	}
	public static Java.Lang.Float PostureOblique {
		get;
		set;
	}
	public static Java.Lang.Float PostureRegular {
		get;
		set;
	}
	public static TextAttribute RunDirection {
		get;
		set;
	}
	public static Java.Lang.Boolean RunDirectionLtr {
		get;
		set;
	}
	public static Java.Lang.Boolean RunDirectionRtl {
		get;
		set;
	}
	public static TextAttribute Size {
		get;
		set;
	}
	public static TextAttribute Strikethrough {
		get;
		set;
	}
	public static Java.Lang.Boolean StrikethroughOn {
		get;
		set;
	}
	public static TextAttribute Superscript {
		get;
		set;
	}
	public static Java.Lang.Integer SuperscriptSub {
		get;
		set;
	}
	public static Java.Lang.Integer SuperscriptSuper {
		get;
		set;
	}
	public static TextAttribute SwapColors {
		get;
		set;
	}
	public static Java.Lang.Boolean SwapColorsOn {
		get;
		set;
	}
	public static TextAttribute Tracking {
		get;
		set;
	}
	public static Java.Lang.Float TrackingLoose {
		get;
		set;
	}
	public static Java.Lang.Float TrackingTight {
		get;
		set;
	}
	public static TextAttribute Transform {
		get;
		set;
	}
	public static TextAttribute Underline {
		get;
		set;
	}
	public static Java.Lang.Integer UnderlineLowDashed {
		get;
		set;
	}
	public static Java.Lang.Integer UnderlineLowDotted {
		get;
		set;
	}
	public static Java.Lang.Integer UnderlineLowGray {
		get;
		set;
	}
	public static Java.Lang.Integer UnderlineLowOnePixel {
		get;
		set;
	}
	public static Java.Lang.Integer UnderlineLowTwoPixel {
		get;
		set;
	}
	public static Java.Lang.Integer UnderlineOn {
		get;
		set;
	}
	public static TextAttribute Weight {
		get;
		set;
	}
	public static Java.Lang.Float WeightBold {
		get;
		set;
	}
	public static Java.Lang.Float WeightDemibold {
		get;
		set;
	}
	public static Java.Lang.Float WeightDemilight {
		get;
		set;
	}
	public static Java.Lang.Float WeightExtrabold {
		get;
		set;
	}
	public static Java.Lang.Float WeightExtraLight {
		get;
		set;
	}
	public static Java.Lang.Float WeightHeavy {
		get;
		set;
	}
	public static Java.Lang.Float WeightLight {
		get;
		set;
	}
	public static Java.Lang.Float WeightMedium {
		get;
		set;
	}
	public static Java.Lang.Float WeightRegular {
		get;
		set;
	}
	public static Java.Lang.Float WeightSemibold {
		get;
		set;
	}
	public static Java.Lang.Float WeightUltrabold {
		get;
		set;
	}
	public static TextAttribute Width {
		get;
		set;
	}
	public static Java.Lang.Float WidthCondensed {
		get;
		set;
	}
	public static Java.Lang.Float WidthExtended {
		get;
		set;
	}
	public static Java.Lang.Float WidthRegular {
		get;
		set;
	}
	public static Java.Lang.Float WidthSemiCondensed {
		get;
		set;
	}
	public static Java.Lang.Float WidthSemiExtended {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Java.IO'>Namespace: Java.IO</h2>

<h3 id='Java.IO.BufferedInputStream'>New Type: Java.IO.BufferedInputStream</h3>

```
public class BufferedInputStream : FilterInputStream {
	
	protected BufferedInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BufferedInputStream (System.IO.Stream in);
	public BufferedInputStream (System.IO.Stream in, int size);
	
	protected System.Collections.Generic.IList Buf {
		get;
		set;
	}
	protected int Count {
		get;
		set;
	}
	protected int Marklimit {
		get;
		set;
	}
	protected int Markpos {
		get;
		set;
	}
	protected int Pos {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.BufferedOutputStream'>New Type: Java.IO.BufferedOutputStream</h3>

```
public class BufferedOutputStream : FilterOutputStream {
	
	protected BufferedOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BufferedOutputStream (System.IO.Stream out);
	public BufferedOutputStream (System.IO.Stream out, int size);
	
	protected System.Collections.Generic.IList Buf {
		get;
		set;
	}
	protected int Count {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.BufferedReader'>Type Changed: Java.IO.BufferedReader</h3>

Added:

```
public System.Threading.Tasks.Task<string> ReadLineAsync ();
```

<h3 id='Java.IO.BufferedWriter'>Type Changed: Java.IO.BufferedWriter</h3>

Added:

```
public System.Threading.Tasks.Task NewLineAsync ();
```

<h3 id='Java.IO.ByteArrayInputStream'>New Type: Java.IO.ByteArrayInputStream</h3>

```
public class ByteArrayInputStream : InputStream {
	
	protected ByteArrayInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ByteArrayInputStream (byte [] buf);
	public ByteArrayInputStream (byte [] buf, int offset, int length);
	
	public override int Read ();
	
	protected System.Collections.Generic.IList Buf {
		get;
		set;
	}
	protected int Count {
		get;
		set;
	}
	protected int Mark {
		get;
		set;
	}
	protected int Pos {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.ByteArrayOutputStream'>New Type: Java.IO.ByteArrayOutputStream</h3>

```
public class ByteArrayOutputStream : OutputStream {
	
	protected ByteArrayOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ByteArrayOutputStream ();
	public ByteArrayOutputStream (int size);
	
	public virtual void Reset ();
	public virtual int Size ();
	public virtual byte [] ToByteArray ();
	public virtual string ToString (int hibyte);
	public virtual string ToString (string enc);
	public override void Write (int oneByte);
	public virtual void WriteTo (System.IO.Stream out);
	public System.Threading.Tasks.Task WriteToAsync (System.IO.Stream out);
	
	protected System.Collections.Generic.IList Buf {
		get;
		set;
	}
	protected int Count {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.CharArrayWriter'>Type Changed: Java.IO.CharArrayWriter</h3>

Added:

```
public System.Threading.Tasks.Task WriteToAsync (Writer out);
```

<h3 id='Java.IO.Console'>Type Changed: Java.IO.Console</h3>

Added:

```
public System.Threading.Tasks.Task<Console> FormatAsync (string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task<Console> PrintfAsync (string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task<string> ReadLineAsync ();
 	public System.Threading.Tasks.Task<string> ReadLineAsync (string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task<char []> ReadPasswordAsync ();
 	public System.Threading.Tasks.Task<char []> ReadPasswordAsync (string format, params Java.Lang.Object[] args);
```

<h3 id='Java.IO.DataInputStream'>New Type: Java.IO.DataInputStream</h3>

```
public class DataInputStream : FilterInputStream, IDataInput {
	
	protected DataInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DataInputStream (System.IO.Stream in);
	
	public static string ReadUTF (IDataInput in);
	public int Read (byte [] buffer);
	public int Read (byte [] buffer, int offset, int length);
	public bool ReadBoolean ();
	public sbyte ReadByte ();
	public char ReadChar ();
	public double ReadDouble ();
	public float ReadFloat ();
	public void ReadFully (byte [] buffer);
	public void ReadFully (byte [] buffer, int offset, int length);
	public int ReadInt ();
	public string ReadLine ();
	public long ReadLong ();
	public short ReadShort ();
	public int ReadUnsignedByte ();
	public int ReadUnsignedShort ();
	public string ReadUTF ();
	public int SkipBytes (int count);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.DataOutputStream'>New Type: Java.IO.DataOutputStream</h3>

```
public class DataOutputStream : FilterOutputStream, IDataOutput {
	
	protected DataOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DataOutputStream (System.IO.Stream out);
	
	public int Size ();
	public void WriteBoolean (bool val);
	public void WriteByte (int val);
	public void WriteBytes (string str);
	public void WriteChar (int val);
	public void WriteChars (string str);
	public void WriteDouble (double val);
	public void WriteFloat (float val);
	public void WriteInt (int val);
	public void WriteLong (long val);
	public void WriteShort (int val);
	public void WriteUTF (string str);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	protected int Written {
		get;
		set;
	}
}
```

<h3 id='Java.IO.File'>Type Changed: Java.IO.File</h3>

Added:

```
public static System.Threading.Tasks.Task<File[]> ListRootsAsync ();
 	public System.Threading.Tasks.Task<string []> ListAsync ();
 	public System.Threading.Tasks.Task<string []> ListAsync (IFilenameFilter filter);
 	public System.Threading.Tasks.Task<File[]> ListFilesAsync ();
 	public System.Threading.Tasks.Task<File[]> ListFilesAsync (IFileFilter filter);
 	public System.Threading.Tasks.Task<File[]> ListFilesAsync (IFilenameFilter filter);
```

<h3 id='Java.IO.IDataInputExtensions'>New Type: Java.IO.IDataInputExtensions</h3>

```
public static class IDataInputExtensions {
	
	public static System.Threading.Tasks.Task ReadBooleanAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadByteAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadCharAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadDoubleAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadFloatAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadFullyAsync (IDataInput self, byte [] buffer);
	public static System.Threading.Tasks.Task ReadFullyAsync (IDataInput self, byte [] buffer, int offset, int count);
	public static System.Threading.Tasks.Task ReadIntAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadLineAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadLongAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadShortAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadUnsignedByteAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadUnsignedShortAsync (IDataInput self);
	public static System.Threading.Tasks.Task ReadUTFAsync (IDataInput self);
	public static System.Threading.Tasks.Task SkipBytesAsync (IDataInput self, int count);
}
```

<h3 id='Java.IO.IDataOutputExtensions'>New Type: Java.IO.IDataOutputExtensions</h3>

```
public static class IDataOutputExtensions {
	
	public static System.Threading.Tasks.Task WriteAsync (IDataOutput self, byte [] buffer);
	public static System.Threading.Tasks.Task WriteAsync (IDataOutput self, byte [] buffer, int offset, int count);
	public static System.Threading.Tasks.Task WriteAsync (IDataOutput self, int oneByte);
	public static System.Threading.Tasks.Task WriteBooleanAsync (IDataOutput self, bool val);
	public static System.Threading.Tasks.Task WriteByteAsync (IDataOutput self, int val);
	public static System.Threading.Tasks.Task WriteBytesAsync (IDataOutput self, string str);
	public static System.Threading.Tasks.Task WriteCharAsync (IDataOutput self, int val);
	public static System.Threading.Tasks.Task WriteCharsAsync (IDataOutput self, string str);
	public static System.Threading.Tasks.Task WriteDoubleAsync (IDataOutput self, double val);
	public static System.Threading.Tasks.Task WriteFloatAsync (IDataOutput self, float val);
	public static System.Threading.Tasks.Task WriteIntAsync (IDataOutput self, int val);
	public static System.Threading.Tasks.Task WriteLongAsync (IDataOutput self, long val);
	public static System.Threading.Tasks.Task WriteShortAsync (IDataOutput self, int val);
	public static System.Threading.Tasks.Task WriteUTFAsync (IDataOutput self, string str);
}
```

<h3 id='Java.IO.IExternalizableExtensions'>New Type: Java.IO.IExternalizableExtensions</h3>

```
public static class IExternalizableExtensions {
	
	public static System.Threading.Tasks.Task ReadExternalAsync (IExternalizable self, IObjectInput input);
	public static System.Threading.Tasks.Task WriteExternalAsync (IExternalizable self, IObjectOutput output);
}
```

<h3 id='Java.IO.IFlushableExtensions'>New Type: Java.IO.IFlushableExtensions</h3>

```
public static class IFlushableExtensions {
	
	public static System.Threading.Tasks.Task FlushAsync (IFlushable self);
}
```

<h3 id='Java.IO.IObjectInputExtensions'>New Type: Java.IO.IObjectInputExtensions</h3>

```
public static class IObjectInputExtensions {
	
	public static System.Threading.Tasks.Task ReadAsync (IObjectInput self);
	public static System.Threading.Tasks.Task ReadAsync (IObjectInput self, byte [] buffer);
	public static System.Threading.Tasks.Task ReadAsync (IObjectInput self, byte [] buffer, int offset, int count);
	public static System.Threading.Tasks.Task ReadObjectAsync (IObjectInput self);
	public static System.Threading.Tasks.Task SkipAsync (IObjectInput self, long toSkip);
}
```

<h3 id='Java.IO.IObjectOutputExtensions'>New Type: Java.IO.IObjectOutputExtensions</h3>

```
public static class IObjectOutputExtensions {
	
	public static System.Threading.Tasks.Task FlushAsync (IObjectOutput self);
	public static System.Threading.Tasks.Task WriteObjectAsync (IObjectOutput self, Java.Lang.Object obj);
}
```

<h3 id='Java.IO.InputStream'>Type Changed: Java.IO.InputStream</h3>

Added:

```
public System.Threading.Tasks.Task<int> ReadAsync ();
 	public System.Threading.Tasks.Task<int> ReadAsync (byte [] b);
 	public System.Threading.Tasks.Task<int> ReadAsync (byte [] b, int offset, int length);
 	public System.Threading.Tasks.Task<long> SkipAsync (long n);
```

<h3 id='Java.IO.LineNumberInputStream'>New Type: Java.IO.LineNumberInputStream</h3>

```
[Obsolete]
public class LineNumberInputStream : FilterInputStream {
	
	protected LineNumberInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LineNumberInputStream (System.IO.Stream in);
	
	public virtual int LineNumber {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.OutputStream'>Type Changed: Java.IO.OutputStream</h3>

Added:

```
public System.Threading.Tasks.Task WriteAsync (byte [] buffer);
 	public System.Threading.Tasks.Task WriteAsync (byte [] buffer, int offset, int count);
 	public System.Threading.Tasks.Task WriteAsync (int oneByte);
```

<h3 id='Java.IO.PipedInputStream'>New Type: Java.IO.PipedInputStream</h3>

```
public class PipedInputStream : InputStream {
	
	protected PipedInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PipedInputStream ();
	public PipedInputStream (int p0);
	public PipedInputStream (PipedOutputStream out);
	public PipedInputStream (PipedOutputStream p0, int p1);
	
	public virtual void Connect (PipedOutputStream src);
	public override int Read ();
	protected virtual void Receive (int oneByte);
	protected System.Threading.Tasks.Task ReceiveAsync (int oneByte);
	
	protected System.Collections.Generic.IList Buffer {
		get;
		set;
	}
	protected int In {
		get;
		set;
	}
	protected int Out {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	protected const int PipeSize = 1024;
}
```

<h3 id='Java.IO.PipedOutputStream'>New Type: Java.IO.PipedOutputStream</h3>

```
public class PipedOutputStream : OutputStream {
	
	protected PipedOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PipedOutputStream ();
	public PipedOutputStream (PipedInputStream dest);
	
	public virtual void Connect (PipedInputStream stream);
	public override void Write (int oneByte);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.PrintStream'>Type Changed: Java.IO.PrintStream</h3>

Added:

```
public System.Threading.Tasks.Task<Java.Lang.IAppendable> AppendAsync (char c);
 	public System.Threading.Tasks.Task<Java.Lang.IAppendable> AppendAsync (Java.Lang.ICharSequence csq);
 	public System.Threading.Tasks.Task<Java.Lang.IAppendable> AppendAsync (Java.Lang.ICharSequence csq, int start, int end);
 	public System.Threading.Tasks.Task<PrintStream> FormatAsync (Java.Util.Locale l, string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task<PrintStream> FormatAsync (string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task PrintAsync (bool bool);
 	public System.Threading.Tasks.Task PrintAsync (char ch);
 	public System.Threading.Tasks.Task PrintAsync (char [] charArray);
 	public System.Threading.Tasks.Task PrintAsync (double dnum);
 	public System.Threading.Tasks.Task PrintAsync (int inum);
 	public System.Threading.Tasks.Task PrintAsync (long lnum);
 	public System.Threading.Tasks.Task PrintAsync (Java.Lang.Object obj);
 	public System.Threading.Tasks.Task PrintAsync (float fnum);
 	public System.Threading.Tasks.Task PrintAsync (string str);
 	public System.Threading.Tasks.Task<PrintStream> PrintfAsync (Java.Util.Locale l, string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task<PrintStream> PrintfAsync (string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task PrintlnAsync ();
 	public System.Threading.Tasks.Task PrintlnAsync (bool bool);
 	public System.Threading.Tasks.Task PrintlnAsync (char ch);
 	public System.Threading.Tasks.Task PrintlnAsync (char [] charArray);
 	public System.Threading.Tasks.Task PrintlnAsync (double dnum);
 	public System.Threading.Tasks.Task PrintlnAsync (int inum);
 	public System.Threading.Tasks.Task PrintlnAsync (long lnum);
 	public System.Threading.Tasks.Task PrintlnAsync (Java.Lang.Object obj);
 	public System.Threading.Tasks.Task PrintlnAsync (float fnum);
 	public System.Threading.Tasks.Task PrintlnAsync (string str);
```

<h3 id='Java.IO.PrintWriter'>Type Changed: Java.IO.PrintWriter</h3>

Added:

```
public System.Threading.Tasks.Task<PrintWriter> FormatAsync (Java.Util.Locale l, string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task<PrintWriter> FormatAsync (string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task PrintAsync (bool bool);
 	public System.Threading.Tasks.Task PrintAsync (char ch);
 	public System.Threading.Tasks.Task PrintAsync (char [] charArray);
 	public System.Threading.Tasks.Task PrintAsync (double dnum);
 	public System.Threading.Tasks.Task PrintAsync (int inum);
 	public System.Threading.Tasks.Task PrintAsync (long lnum);
 	public System.Threading.Tasks.Task PrintAsync (Java.Lang.Object obj);
 	public System.Threading.Tasks.Task PrintAsync (float fnum);
 	public System.Threading.Tasks.Task PrintAsync (string str);
 	public System.Threading.Tasks.Task<PrintWriter> PrintfAsync (Java.Util.Locale l, string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task<PrintWriter> PrintfAsync (string format, params Java.Lang.Object[] args);
 	public System.Threading.Tasks.Task PrintlnAsync ();
 	public System.Threading.Tasks.Task PrintlnAsync (bool bool);
 	public System.Threading.Tasks.Task PrintlnAsync (char ch);
 	public System.Threading.Tasks.Task PrintlnAsync (char [] charArray);
 	public System.Threading.Tasks.Task PrintlnAsync (double dnum);
 	public System.Threading.Tasks.Task PrintlnAsync (int inum);
 	public System.Threading.Tasks.Task PrintlnAsync (long lnum);
 	public System.Threading.Tasks.Task PrintlnAsync (Java.Lang.Object obj);
 	public System.Threading.Tasks.Task PrintlnAsync (float fnum);
 	public System.Threading.Tasks.Task PrintlnAsync (string str);
```

<h3 id='Java.IO.PushbackInputStream'>New Type: Java.IO.PushbackInputStream</h3>

```
public class PushbackInputStream : FilterInputStream {
	
	protected PushbackInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PushbackInputStream (System.IO.Stream in);
	public PushbackInputStream (System.IO.Stream in, int size);
	
	public virtual void Unread (byte [] buffer);
	public virtual void Unread (byte [] buffer, int offset, int length);
	public virtual void Unread (int oneByte);
	
	protected System.Collections.Generic.IList Buf {
		get;
		set;
	}
	protected int Pos {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.RandomAccessFile'>Type Changed: Java.IO.RandomAccessFile</h3>

Added:

```
public System.Threading.Tasks.Task<int> ReadAsync ();
 	public System.Threading.Tasks.Task<int> ReadAsync (byte [] buffer);
 	public System.Threading.Tasks.Task<int> ReadAsync (byte [] buffer, int offset, int count);
 	public System.Threading.Tasks.Task<bool> ReadBooleanAsync ();
 	public System.Threading.Tasks.Task<sbyte> ReadByteAsync ();
 	public System.Threading.Tasks.Task<char> ReadCharAsync ();
 	public System.Threading.Tasks.Task<double> ReadDoubleAsync ();
 	public System.Threading.Tasks.Task<float> ReadFloatAsync ();
 	public System.Threading.Tasks.Task ReadFullyAsync (byte [] buffer);
 	public System.Threading.Tasks.Task ReadFullyAsync (byte [] buffer, int offset, int count);
 	public System.Threading.Tasks.Task<int> ReadIntAsync ();
 	public System.Threading.Tasks.Task<string> ReadLineAsync ();
 	public System.Threading.Tasks.Task<long> ReadLongAsync ();
 	public System.Threading.Tasks.Task<short> ReadShortAsync ();
 	public System.Threading.Tasks.Task<int> ReadUnsignedByteAsync ();
 	public System.Threading.Tasks.Task<int> ReadUnsignedShortAsync ();
 	public System.Threading.Tasks.Task<string> ReadUTFAsync ();
 	public System.Threading.Tasks.Task<int> SkipBytesAsync (int count);
 	public System.Threading.Tasks.Task WriteAsync (byte [] buffer);
 	public System.Threading.Tasks.Task WriteAsync (byte [] buffer, int offset, int count);
 	public System.Threading.Tasks.Task WriteAsync (int oneByte);
 	public System.Threading.Tasks.Task WriteBooleanAsync (bool val);
 	public System.Threading.Tasks.Task WriteByteAsync (int val);
 	public System.Threading.Tasks.Task WriteBytesAsync (string str);
 	public System.Threading.Tasks.Task WriteCharAsync (int val);
 	public System.Threading.Tasks.Task WriteCharsAsync (string str);
 	public System.Threading.Tasks.Task WriteDoubleAsync (double val);
 	public System.Threading.Tasks.Task WriteFloatAsync (float val);
 	public System.Threading.Tasks.Task WriteIntAsync (int val);
 	public System.Threading.Tasks.Task WriteLongAsync (long val);
 	public System.Threading.Tasks.Task WriteShortAsync (int val);
 	public System.Threading.Tasks.Task WriteUTFAsync (string str);
```

<h3 id='Java.IO.Reader'>Type Changed: Java.IO.Reader</h3>

Added:

```
public System.Threading.Tasks.Task<int> ReadAsync ();
 	public System.Threading.Tasks.Task<int> ReadAsync (char [] buf);
 	public System.Threading.Tasks.Task<int> ReadAsync (char [] buf, int offset, int count);
 	public System.Threading.Tasks.Task<int> ReadAsync (Java.Nio.CharBuffer target);
 	public System.Threading.Tasks.Task<long> SkipAsync (long count);
```

<h3 id='Java.IO.SequenceInputStream'>New Type: Java.IO.SequenceInputStream</h3>

```
public class SequenceInputStream : InputStream {
	
	protected SequenceInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SequenceInputStream (System.IO.Stream s1, System.IO.Stream s2);
	public SequenceInputStream (Java.Util.IEnumeration e);
	
	public override int Read ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.StringBufferInputStream'>New Type: Java.IO.StringBufferInputStream</h3>

```
[Obsolete]
public class StringBufferInputStream : InputStream {
	
	protected StringBufferInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StringBufferInputStream (string str);
	
	public override int Read ();
	
	protected string Buffer {
		get;
		set;
	}
	protected int Count {
		get;
		set;
	}
	protected int Pos {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.IO.Writer'>Type Changed: Java.IO.Writer</h3>

Added:

```
public System.Threading.Tasks.Task<Java.Lang.IAppendable> AppendAsync (char c);
 	public System.Threading.Tasks.Task<Java.Lang.IAppendable> AppendAsync (Java.Lang.ICharSequence csq);
 	public System.Threading.Tasks.Task<Java.Lang.IAppendable> AppendAsync (Java.Lang.ICharSequence csq, int start, int end);
 	public System.Threading.Tasks.Task WriteAsync (char [] buf);
 	public System.Threading.Tasks.Task WriteAsync (char [] buf, int offset, int count);
 	public System.Threading.Tasks.Task WriteAsync (int oneChar);
 	public System.Threading.Tasks.Task WriteAsync (string str);
 	public System.Threading.Tasks.Task WriteAsync (string str, int offset, int count);
```

<h2 id='Java.Lang'>Namespace: Java.Lang</h2>

<h3 id='Java.Lang.Character'>Type Changed: Java.Lang.Character</h3>

Added:

```
public class Subset : Object {
 		
 		protected Subset (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
 		protected Subset (string string);
 		
 		public bool Equals (Object object);
 		public int GetHashCode ();
 		public string ToString ();
 		
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 	}
 	public sealed class UnicodeBlock : Subset {
 		
 		public static UnicodeBlock ForName (string blockName);
 		public static UnicodeBlock Of (char c);
 		public static UnicodeBlock Of (int codePoint);
 		
 		public static UnicodeBlock AegeanNumbers {
 			get;
 			set;
 		}
 		public static UnicodeBlock AlchemicalSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock AlphabeticPresentationForms {
 			get;
 			set;
 		}
 		public static UnicodeBlock AncientGreekMusicalNotation {
 			get;
 			set;
 		}
 		public static UnicodeBlock AncientGreekNumbers {
 			get;
 			set;
 		}
 		public static UnicodeBlock AncientSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock Arabic {
 			get;
 			set;
 		}
 		public static UnicodeBlock ArabicPresentationFormsA {
 			get;
 			set;
 		}
 		public static UnicodeBlock ArabicPresentationFormsB {
 			get;
 			set;
 		}
 		public static UnicodeBlock ArabicSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock Armenian {
 			get;
 			set;
 		}
 		public static UnicodeBlock Arrows {
 			get;
 			set;
 		}
 		public static UnicodeBlock Avestan {
 			get;
 			set;
 		}
 		public static UnicodeBlock Balinese {
 			get;
 			set;
 		}
 		public static UnicodeBlock Bamum {
 			get;
 			set;
 		}
 		public static UnicodeBlock BamumSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock BasicLatin {
 			get;
 			set;
 		}
 		public static UnicodeBlock Batak {
 			get;
 			set;
 		}
 		public static UnicodeBlock Bengali {
 			get;
 			set;
 		}
 		public static UnicodeBlock BlockElements {
 			get;
 			set;
 		}
 		public static UnicodeBlock Bopomofo {
 			get;
 			set;
 		}
 		public static UnicodeBlock BopomofoExtended {
 			get;
 			set;
 		}
 		public static UnicodeBlock BoxDrawing {
 			get;
 			set;
 		}
 		public static UnicodeBlock Brahmi {
 			get;
 			set;
 		}
 		public static UnicodeBlock BraillePatterns {
 			get;
 			set;
 		}
 		public static UnicodeBlock Buginese {
 			get;
 			set;
 		}
 		public static UnicodeBlock Buhid {
 			get;
 			set;
 		}
 		public static UnicodeBlock ByzantineMusicalSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock Carian {
 			get;
 			set;
 		}
 		public static UnicodeBlock Cham {
 			get;
 			set;
 		}
 		public static UnicodeBlock Cherokee {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkCompatibility {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkCompatibilityForms {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkCompatibilityIdeographs {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkCompatibilityIdeographsSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkRadicalsSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkStrokes {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkSymbolsAndPunctuation {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkUnifiedIdeographs {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkUnifiedIdeographsExtensionA {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkUnifiedIdeographsExtensionB {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkUnifiedIdeographsExtensionC {
 			get;
 			set;
 		}
 		public static UnicodeBlock CjkUnifiedIdeographsExtensionD {
 			get;
 			set;
 		}
 		public static UnicodeBlock CombiningDiacriticalMarks {
 			get;
 			set;
 		}
 		public static UnicodeBlock CombiningDiacriticalMarksSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock CombiningHalfMarks {
 			get;
 			set;
 		}
 		public static UnicodeBlock CombiningMarksForSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock CommonIndicNumberForms {
 			get;
 			set;
 		}
 		public static UnicodeBlock ControlPictures {
 			get;
 			set;
 		}
 		public static UnicodeBlock Coptic {
 			get;
 			set;
 		}
 		public static UnicodeBlock CountingRodNumerals {
 			get;
 			set;
 		}
 		public static UnicodeBlock Cuneiform {
 			get;
 			set;
 		}
 		public static UnicodeBlock CuneiformNumbersAndPunctuation {
 			get;
 			set;
 		}
 		public static UnicodeBlock CurrencySymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock CypriotSyllabary {
 			get;
 			set;
 		}
 		public static UnicodeBlock Cyrillic {
 			get;
 			set;
 		}
 		public static UnicodeBlock CyrillicExtendedA {
 			get;
 			set;
 		}
 		public static UnicodeBlock CyrillicExtendedB {
 			get;
 			set;
 		}
 		public static UnicodeBlock CyrillicSupplementary {
 			get;
 			set;
 		}
 		public static UnicodeBlock Deseret {
 			get;
 			set;
 		}
 		public static UnicodeBlock Devanagari {
 			get;
 			set;
 		}
 		public static UnicodeBlock DevanagariExtended {
 			get;
 			set;
 		}
 		public static UnicodeBlock Dingbats {
 			get;
 			set;
 		}
 		public static UnicodeBlock DominoTiles {
 			get;
 			set;
 		}
 		public static UnicodeBlock EgyptianHieroglyphs {
 			get;
 			set;
 		}
 		public static UnicodeBlock Emoticons {
 			get;
 			set;
 		}
 		public static UnicodeBlock EnclosedAlphanumerics {
 			get;
 			set;
 		}
 		public static UnicodeBlock EnclosedAlphanumericSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock EnclosedCjkLettersAndMonths {
 			get;
 			set;
 		}
 		public static UnicodeBlock EnclosedIdeographicSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock Ethiopic {
 			get;
 			set;
 		}
 		public static UnicodeBlock EthiopicExtended {
 			get;
 			set;
 		}
 		public static UnicodeBlock EthiopicExtendedA {
 			get;
 			set;
 		}
 		public static UnicodeBlock EthiopicSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock GeneralPunctuation {
 			get;
 			set;
 		}
 		public static UnicodeBlock GeometricShapes {
 			get;
 			set;
 		}
 		public static UnicodeBlock Georgian {
 			get;
 			set;
 		}
 		public static UnicodeBlock GeorgianSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock Glagolitic {
 			get;
 			set;
 		}
 		public static UnicodeBlock Gothic {
 			get;
 			set;
 		}
 		public static UnicodeBlock Greek {
 			get;
 			set;
 		}
 		public static UnicodeBlock GreekExtended {
 			get;
 			set;
 		}
 		public static UnicodeBlock Gujarati {
 			get;
 			set;
 		}
 		public static UnicodeBlock Gurmukhi {
 			get;
 			set;
 		}
 		public static UnicodeBlock HalfwidthAndFullwidthForms {
 			get;
 			set;
 		}
 		public static UnicodeBlock HangulCompatibilityJamo {
 			get;
 			set;
 		}
 		public static UnicodeBlock HangulJamo {
 			get;
 			set;
 		}
 		public static UnicodeBlock HangulJamoExtendedA {
 			get;
 			set;
 		}
 		public static UnicodeBlock HangulJamoExtendedB {
 			get;
 			set;
 		}
 		public static UnicodeBlock HangulSyllables {
 			get;
 			set;
 		}
 		public static UnicodeBlock Hanunoo {
 			get;
 			set;
 		}
 		public static UnicodeBlock Hebrew {
 			get;
 			set;
 		}
 		public static UnicodeBlock HighPrivateUseSurrogates {
 			get;
 			set;
 		}
 		public static UnicodeBlock HighSurrogates {
 			get;
 			set;
 		}
 		public static UnicodeBlock Hiragana {
 			get;
 			set;
 		}
 		public static UnicodeBlock IdeographicDescriptionCharacters {
 			get;
 			set;
 		}
 		public static UnicodeBlock ImperialAramaic {
 			get;
 			set;
 		}
 		public static UnicodeBlock InscriptionalPahlavi {
 			get;
 			set;
 		}
 		public static UnicodeBlock InscriptionalParthian {
 			get;
 			set;
 		}
 		public static UnicodeBlock IpaExtensions {
 			get;
 			set;
 		}
 		public static UnicodeBlock Javanese {
 			get;
 			set;
 		}
 		public static UnicodeBlock Kaithi {
 			get;
 			set;
 		}
 		public static UnicodeBlock KanaSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock Kanbun {
 			get;
 			set;
 		}
 		public static UnicodeBlock KangxiRadicals {
 			get;
 			set;
 		}
 		public static UnicodeBlock Kannada {
 			get;
 			set;
 		}
 		public static UnicodeBlock Katakana {
 			get;
 			set;
 		}
 		public static UnicodeBlock KatakanaPhoneticExtensions {
 			get;
 			set;
 		}
 		public static UnicodeBlock KayahLi {
 			get;
 			set;
 		}
 		public static UnicodeBlock Kharoshthi {
 			get;
 			set;
 		}
 		public static UnicodeBlock Khmer {
 			get;
 			set;
 		}
 		public static UnicodeBlock KhmerSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock Lao {
 			get;
 			set;
 		}
 		public static UnicodeBlock Latin1Supplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock LatinExtendedA {
 			get;
 			set;
 		}
 		public static UnicodeBlock LatinExtendedAdditional {
 			get;
 			set;
 		}
 		public static UnicodeBlock LatinExtendedB {
 			get;
 			set;
 		}
 		public static UnicodeBlock LatinExtendedC {
 			get;
 			set;
 		}
 		public static UnicodeBlock LatinExtendedD {
 			get;
 			set;
 		}
 		public static UnicodeBlock Lepcha {
 			get;
 			set;
 		}
 		public static UnicodeBlock LetterlikeSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock Limbu {
 			get;
 			set;
 		}
 		public static UnicodeBlock LinearBIdeograms {
 			get;
 			set;
 		}
 		public static UnicodeBlock LinearBSyllabary {
 			get;
 			set;
 		}
 		public static UnicodeBlock Lisu {
 			get;
 			set;
 		}
 		public static UnicodeBlock LowSurrogates {
 			get;
 			set;
 		}
 		public static UnicodeBlock Lycian {
 			get;
 			set;
 		}
 		public static UnicodeBlock Lydian {
 			get;
 			set;
 		}
 		public static UnicodeBlock MahjongTiles {
 			get;
 			set;
 		}
 		public static UnicodeBlock Malayalam {
 			get;
 			set;
 		}
 		public static UnicodeBlock Mandaic {
 			get;
 			set;
 		}
 		public static UnicodeBlock MathematicalAlphanumericSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock MathematicalOperators {
 			get;
 			set;
 		}
 		public static UnicodeBlock MeeteiMayek {
 			get;
 			set;
 		}
 		public static UnicodeBlock MiscellaneousMathematicalSymbolsA {
 			get;
 			set;
 		}
 		public static UnicodeBlock MiscellaneousMathematicalSymbolsB {
 			get;
 			set;
 		}
 		public static UnicodeBlock MiscellaneousSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock MiscellaneousSymbolsAndArrows {
 			get;
 			set;
 		}
 		public static UnicodeBlock MiscellaneousSymbolsAndPictographs {
 			get;
 			set;
 		}
 		public static UnicodeBlock MiscellaneousTechnical {
 			get;
 			set;
 		}
 		public static UnicodeBlock ModifierToneLetters {
 			get;
 			set;
 		}
 		public static UnicodeBlock Mongolian {
 			get;
 			set;
 		}
 		public static UnicodeBlock MusicalSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock Myanmar {
 			get;
 			set;
 		}
 		public static UnicodeBlock MyanmarExtendedA {
 			get;
 			set;
 		}
 		public static UnicodeBlock NewTaiLue {
 			get;
 			set;
 		}
 		public static UnicodeBlock Nko {
 			get;
 			set;
 		}
 		public static UnicodeBlock NumberForms {
 			get;
 			set;
 		}
 		public static UnicodeBlock Ogham {
 			get;
 			set;
 		}
 		public static UnicodeBlock OlChiki {
 			get;
 			set;
 		}
 		public static UnicodeBlock OldItalic {
 			get;
 			set;
 		}
 		public static UnicodeBlock OldPersian {
 			get;
 			set;
 		}
 		public static UnicodeBlock OldSouthArabian {
 			get;
 			set;
 		}
 		public static UnicodeBlock OldTurkic {
 			get;
 			set;
 		}
 		public static UnicodeBlock OpticalCharacterRecognition {
 			get;
 			set;
 		}
 		public static UnicodeBlock Oriya {
 			get;
 			set;
 		}
 		public static UnicodeBlock Osmanya {
 			get;
 			set;
 		}
 		public static UnicodeBlock PhagsPa {
 			get;
 			set;
 		}
 		public static UnicodeBlock PhaistosDisc {
 			get;
 			set;
 		}
 		public static UnicodeBlock Phoenician {
 			get;
 			set;
 		}
 		public static UnicodeBlock PhoneticExtensions {
 			get;
 			set;
 		}
 		public static UnicodeBlock PhoneticExtensionsSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock PlayingCards {
 			get;
 			set;
 		}
 		public static UnicodeBlock PrivateUseArea {
 			get;
 			set;
 		}
 		public static UnicodeBlock Rejang {
 			get;
 			set;
 		}
 		public static UnicodeBlock RumiNumeralSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock Runic {
 			get;
 			set;
 		}
 		public static UnicodeBlock Samaritan {
 			get;
 			set;
 		}
 		public static UnicodeBlock Saurashtra {
 			get;
 			set;
 		}
 		public static UnicodeBlock Shavian {
 			get;
 			set;
 		}
 		public static UnicodeBlock Sinhala {
 			get;
 			set;
 		}
 		public static UnicodeBlock SmallFormVariants {
 			get;
 			set;
 		}
 		public static UnicodeBlock SpacingModifierLetters {
 			get;
 			set;
 		}
 		public static UnicodeBlock Specials {
 			get;
 			set;
 		}
 		public static UnicodeBlock Sundanese {
 			get;
 			set;
 		}
 		public static UnicodeBlock SuperscriptsAndSubscripts {
 			get;
 			set;
 		}
 		public static UnicodeBlock SupplementalArrowsA {
 			get;
 			set;
 		}
 		public static UnicodeBlock SupplementalArrowsB {
 			get;
 			set;
 		}
 		public static UnicodeBlock SupplementalMathematicalOperators {
 			get;
 			set;
 		}
 		public static UnicodeBlock SupplementalPunctuation {
 			get;
 			set;
 		}
 		public static UnicodeBlock SupplementaryPrivateUseAreaA {
 			get;
 			set;
 		}
 		public static UnicodeBlock SupplementaryPrivateUseAreaB {
 			get;
 			set;
 		}
 		public static UnicodeBlock SurrogatesArea {
 			get;
 			set;
 		}
 		public static UnicodeBlock SylotiNagri {
 			get;
 			set;
 		}
 		public static UnicodeBlock Syriac {
 			get;
 			set;
 		}
 		public static UnicodeBlock Tagalog {
 			get;
 			set;
 		}
 		public static UnicodeBlock Tagbanwa {
 			get;
 			set;
 		}
 		public static UnicodeBlock Tags {
 			get;
 			set;
 		}
 		public static UnicodeBlock TaiLe {
 			get;
 			set;
 		}
 		public static UnicodeBlock TaiTham {
 			get;
 			set;
 		}
 		public static UnicodeBlock TaiViet {
 			get;
 			set;
 		}
 		public static UnicodeBlock TaiXuanJingSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock Tamil {
 			get;
 			set;
 		}
 		public static UnicodeBlock Telugu {
 			get;
 			set;
 		}
 		public static UnicodeBlock Thaana {
 			get;
 			set;
 		}
 		public static UnicodeBlock Thai {
 			get;
 			set;
 		}
 		public static UnicodeBlock Tibetan {
 			get;
 			set;
 		}
 		public static UnicodeBlock Tifinagh {
 			get;
 			set;
 		}
 		public static UnicodeBlock TransportAndMapSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock Ugaritic {
 			get;
 			set;
 		}
 		public static UnicodeBlock UnifiedCanadianAboriginalSyllabics {
 			get;
 			set;
 		}
 		public static UnicodeBlock UnifiedCanadianAboriginalSyllabicsExtended {
 			get;
 			set;
 		}
 		public static UnicodeBlock Vai {
 			get;
 			set;
 		}
 		public static UnicodeBlock VariationSelectors {
 			get;
 			set;
 		}
 		public static UnicodeBlock VariationSelectorsSupplement {
 			get;
 			set;
 		}
 		public static UnicodeBlock VedicExtensions {
 			get;
 			set;
 		}
 		public static UnicodeBlock VerticalForms {
 			get;
 			set;
 		}
 		public static UnicodeBlock YijingHexagramSymbols {
 			get;
 			set;
 		}
 		public static UnicodeBlock YiRadicals {
 			get;
 			set;
 		}
 		public static UnicodeBlock YiSyllables {
 			get;
 			set;
 		}
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 	}
```

<h3 id='Java.Lang.Class'>Type Changed: Java.Lang.Class</h3>

Removed:

```
public sealed class Class : Object, Java.IO.ISerializable {
```

Added:

```
public sealed class Class : Object, Java.Lang.Reflect.IGenericDeclaration, Java.IO.ISerializable, Java.Lang.Reflect.IType {
 	public Class[] GetClasses ();
 	public Java.Lang.Reflect.Constructor GetConstructor (params Class[] p0);
 	public Java.Lang.Reflect.Constructor[] GetConstructors ();
 	public Class[] GetDeclaredClasses ();
 	public Java.Lang.Reflect.Constructor GetDeclaredConstructor (params Class[] p0);
 	public Java.Lang.Reflect.Constructor[] GetDeclaredConstructors ();
 	public Java.Lang.Reflect.Field GetDeclaredField (string name);
 	public Java.Lang.Reflect.Field[] GetDeclaredFields ();
 	public Java.Lang.Reflect.Method GetDeclaredMethod (string p0, params Class[] p1);
 	public Java.Lang.Reflect.Method[] GetDeclaredMethods ();
 	public Java.Lang.Reflect.Field GetField (string name);
 	public Java.Lang.Reflect.Field[] GetFields ();
 	public Java.Lang.Reflect.IType[] GetGenericInterfaces ();
 	public Class[] GetInterfaces ();
 	public Java.Lang.Reflect.Method GetMethod (string p0, params Class[] p1);
 	public Java.Lang.Reflect.Method[] GetMethods ();
 	public Java.Lang.Reflect.ITypeVariable[] GetTypeParameters ();
 	public Java.Lang.Reflect.Constructor EnclosingConstructor {
 		get;
 	}
 	public Java.Lang.Reflect.Method EnclosingMethod {
 		get;
 	}
 	public Java.Lang.Reflect.IType GenericSuperclass {
 		get;
 	}
```

<h3 id='Java.Lang.ClassLoader'>Type Changed: Java.Lang.ClassLoader</h3>

Added:

```
public System.Threading.Tasks.Task<Class> LoadClassAsync (string className);
 	protected System.Threading.Tasks.Task<Class> LoadClassAsync (string className, bool resolve);
```

<h3 id='Java.Lang.Deprecated'>Type Changed: Java.Lang.Deprecated</h3>

Removed:

```
public abstract class Deprecated : Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class Deprecated : Object, Java.Lang.Annotation.IAnnotation {
```

<h3 id='Java.Lang.IDeprecated'>New Type: Java.Lang.IDeprecated</h3>

```
public interface IDeprecated : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Java.Lang.IOverride'>New Type: Java.Lang.IOverride</h3>

```
public interface IOverride : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Java.Lang.ISuppressWarnings'>New Type: Java.Lang.ISuppressWarnings</h3>

```
public interface ISuppressWarnings : Java.Lang.Annotation.IAnnotation, IDisposable, Android.Runtime.IJavaObject {
	
	string [] Value ();
}
```

<h3 id='Java.Lang.JavaSystem'>Type Changed: Java.Lang.JavaSystem</h3>

Added:

```
public static System.Threading.Tasks.Task LoadAsync (string pathName);
 	public static System.Threading.Tasks.Task LoadLibraryAsync (string libName);
```

<h3 id='Java.Lang.Override'>Type Changed: Java.Lang.Override</h3>

Removed:

```
public abstract class Override : Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class Override : Object, Java.Lang.Annotation.IAnnotation {
```

<h3 id='Java.Lang.Package'>Type Changed: Java.Lang.Package</h3>

Removed:

```
public class Package : Object {
```

Added:

```
public class Package : Object, Java.Lang.Reflect.IAnnotatedElement {
```

<h3 id='Java.Lang.Process'>Type Changed: Java.Lang.Process</h3>

Added:

```
public System.Threading.Tasks.Task<int> WaitForAsync ();
```

<h3 id='Java.Lang.Runtime'>Type Changed: Java.Lang.Runtime</h3>

Added:

```
public System.Threading.Tasks.Task LoadAsync (string pathName);
 	public System.Threading.Tasks.Task LoadLibraryAsync (string libName);
```

<h3 id='Java.Lang.SuppressWarnings'>Type Changed: Java.Lang.SuppressWarnings</h3>

Removed:

```
public abstract class SuppressWarnings : Object, Java.Lang.Annotation.IAnnotation {
```

Added:

```
[Obsolete]
public abstract class SuppressWarnings : Object, Java.Lang.Annotation.IAnnotation {
```

<h2 id='Java.Lang.Annotation'>Namespace: Java.Lang.Annotation</h2>

<h3 id='Java.Lang.Annotation.AnnotationTypeMismatchException'>Type Changed: Java.Lang.Annotation.AnnotationTypeMismatchException</h3>

Added:

```
public AnnotationTypeMismatchException (Java.Lang.Reflect.Method element, string foundType);
 	public virtual Java.Lang.Reflect.Method Element ();
```

<h3 id='Java.Lang.Annotation.Documented'>Type Changed: Java.Lang.Annotation.Documented</h3>

Removed:

```
public abstract class Documented : Java.Lang.Object, IAnnotation {
```

Added:

```
[Obsolete]
public abstract class Documented : Java.Lang.Object, IAnnotation {
```

<h3 id='Java.Lang.Annotation.IDocumented'>New Type: Java.Lang.Annotation.IDocumented</h3>

```
public interface IDocumented : IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Java.Lang.Annotation.IInherited'>New Type: Java.Lang.Annotation.IInherited</h3>

```
public interface IInherited : IAnnotation, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Java.Lang.Annotation.IRetention'>New Type: Java.Lang.Annotation.IRetention</h3>

```
public interface IRetention : IAnnotation, IDisposable, Android.Runtime.IJavaObject {
	
	RetentionPolicy Value ();
}
```

<h3 id='Java.Lang.Annotation.ITarget'>New Type: Java.Lang.Annotation.ITarget</h3>

```
public interface ITarget : IAnnotation, IDisposable, Android.Runtime.IJavaObject {
	
	ElementType[] Value ();
}
```

<h3 id='Java.Lang.Annotation.Inherited'>Type Changed: Java.Lang.Annotation.Inherited</h3>

Removed:

```
public abstract class Inherited : Java.Lang.Object, IAnnotation {
```

Added:

```
[Obsolete]
public abstract class Inherited : Java.Lang.Object, IAnnotation {
```

<h3 id='Java.Lang.Annotation.Retention'>Type Changed: Java.Lang.Annotation.Retention</h3>

Removed:

```
public abstract class Retention : Java.Lang.Object, IAnnotation {
```

Added:

```
[Obsolete]
public abstract class Retention : Java.Lang.Object, IAnnotation {
```

<h3 id='Java.Lang.Annotation.Target'>Type Changed: Java.Lang.Annotation.Target</h3>

Removed:

```
public abstract class Target : Java.Lang.Object, IAnnotation {
```

Added:

```
[Obsolete]
public abstract class Target : Java.Lang.Object, IAnnotation {
```

<h2 id='Java.Lang.Ref'>Namespace: Java.Lang.Ref</h2>

<h3 id='Java.Lang.Ref.PhantomReference'>New Type: Java.Lang.Ref.PhantomReference</h3>

```
public class PhantomReference : Reference {
	
	protected PhantomReference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PhantomReference (Java.Lang.Object r, ReferenceQueue q);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Ref.Reference'>New Type: Java.Lang.Ref.Reference</h3>

```
public abstract class Reference : Java.Lang.Object {
	
	protected Reference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public virtual void Clear ();
	public virtual bool Enqueue ();
	public virtual Java.Lang.Object Get ();
	
	public virtual bool IsEnqueued {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Ref.ReferenceQueue'>New Type: Java.Lang.Ref.ReferenceQueue</h3>

```
public class ReferenceQueue : Java.Lang.Object {
	
	protected ReferenceQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ReferenceQueue ();
	
	public virtual Reference Poll ();
	public virtual Reference Remove ();
	public virtual Reference Remove (long timeout);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Ref.SoftReference'>New Type: Java.Lang.Ref.SoftReference</h3>

```
public class SoftReference : Reference {
	
	protected SoftReference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SoftReference (Java.Lang.Object r);
	public SoftReference (Java.Lang.Object r, ReferenceQueue q);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Ref.WeakReference'>New Type: Java.Lang.Ref.WeakReference</h3>

```
public class WeakReference : Reference {
	
	protected WeakReference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WeakReference (Java.Lang.Object r);
	public WeakReference (Java.Lang.Object r, ReferenceQueue q);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Java.Lang.Reflect'>Namespace: Java.Lang.Reflect</h2>

<h3 id='Java.Lang.Reflect.AccessibleObject'>New Type: Java.Lang.Reflect.AccessibleObject</h3>

```
public class AccessibleObject : Java.Lang.Object, IAnnotatedElement {
	
	protected AccessibleObject (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AccessibleObject ();
	
	public static void SetAccessible (AccessibleObject[] objects, bool flag);
	public virtual Java.Lang.Object GetAnnotation (Java.Lang.Class annotationType);
	public virtual Java.Lang.Annotation.IAnnotation[] GetAnnotations ();
	public virtual Java.Lang.Annotation.IAnnotation[] GetDeclaredAnnotations ();
	public virtual bool IsAnnotationPresent (Java.Lang.Class annotationType);
	
	public virtual bool Accessible {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.Array'>New Type: Java.Lang.Reflect.Array</h3>

```
public sealed class Array : Java.Lang.Object {
	
	public static Java.Lang.Object Get (Java.Lang.Object array, int index);
	public static bool GetBoolean (Java.Lang.Object array, int index);
	public static sbyte GetByte (Java.Lang.Object array, int index);
	public static char GetChar (Java.Lang.Object array, int index);
	public static double GetDouble (Java.Lang.Object array, int index);
	public static float GetFloat (Java.Lang.Object array, int index);
	public static int GetInt (Java.Lang.Object array, int index);
	public static int GetLength (Java.Lang.Object array);
	public static long GetLong (Java.Lang.Object array, int index);
	public static short GetShort (Java.Lang.Object array, int index);
	public static Java.Lang.Object NewInstance (Java.Lang.Class componentType, int size);
	public static Java.Lang.Object NewInstance (Java.Lang.Class p0, params int [] p1);
	public static void Set (Java.Lang.Object array, int index, Java.Lang.Object value);
	public static void SetBoolean (Java.Lang.Object array, int index, bool value);
	public static void SetByte (Java.Lang.Object array, int index, sbyte value);
	public static void SetChar (Java.Lang.Object array, int index, char value);
	public static void SetDouble (Java.Lang.Object array, int index, double value);
	public static void SetFloat (Java.Lang.Object array, int index, float value);
	public static void SetInt (Java.Lang.Object array, int index, int value);
	public static void SetLong (Java.Lang.Object array, int index, long value);
	public static void SetShort (Java.Lang.Object array, int index, short value);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.Constructor'>New Type: Java.Lang.Reflect.Constructor</h3>

```
public sealed class Constructor : AccessibleObject, IGenericDeclaration, IMember {
	
	public Java.Lang.Class[] GetExceptionTypes ();
	public IType[] GetGenericExceptionTypes ();
	public IType[] GetGenericParameterTypes ();
	public Java.Lang.Annotation.IAnnotation[][] GetParameterAnnotations ();
	public Java.Lang.Class[] GetParameterTypes ();
	public ITypeVariable[] GetTypeParameters ();
	public Java.Lang.Object NewInstance (params Java.Lang.Object[] args);
	public string ToGenericString ();
	
	public Java.Lang.Class DeclaringClass {
		get;
	}
	public bool IsSynthetic {
		get;
	}
	public bool IsVarArgs {
		get;
	}
	public int Modifiers {
		get;
	}
	public string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const int Declared = 1;
		public const int Public = 0;
	}
}
```

<h3 id='Java.Lang.Reflect.Field'>New Type: Java.Lang.Reflect.Field</h3>

```
public sealed class Field : AccessibleObject, IMember {
	
	public Java.Lang.Object Get (Java.Lang.Object object);
	public bool GetBoolean (Java.Lang.Object object);
	public sbyte GetByte (Java.Lang.Object object);
	public char GetChar (Java.Lang.Object object);
	public double GetDouble (Java.Lang.Object object);
	public float GetFloat (Java.Lang.Object object);
	public int GetInt (Java.Lang.Object object);
	public long GetLong (Java.Lang.Object object);
	public short GetShort (Java.Lang.Object object);
	public void Set (Java.Lang.Object object, Java.Lang.Object value);
	public void SetBoolean (Java.Lang.Object object, bool value);
	public void SetByte (Java.Lang.Object object, sbyte value);
	public void SetChar (Java.Lang.Object object, char value);
	public void SetDouble (Java.Lang.Object object, double value);
	public void SetFloat (Java.Lang.Object object, float value);
	public void SetInt (Java.Lang.Object object, int value);
	public void SetLong (Java.Lang.Object object, long value);
	public void SetShort (Java.Lang.Object object, short value);
	public string ToGenericString ();
	
	public Java.Lang.Class DeclaringClass {
		get;
	}
	public IType GenericType {
		get;
	}
	public bool IsEnumConstant {
		get;
	}
	public bool IsSynthetic {
		get;
	}
	public int Modifiers {
		get;
	}
	public string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public Java.Lang.Class Type {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const int Declared = 1;
		public const int Public = 0;
	}
}
```

<h3 id='Java.Lang.Reflect.GenericSignatureFormatError'>New Type: Java.Lang.Reflect.GenericSignatureFormatError</h3>

```
public class GenericSignatureFormatError : Java.Lang.ClassFormatError {
	
	protected GenericSignatureFormatError (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public GenericSignatureFormatError ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.IAnnotatedElement'>New Type: Java.Lang.Reflect.IAnnotatedElement</h3>

```
public interface IAnnotatedElement : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object GetAnnotation (Java.Lang.Class annotationType);
	Java.Lang.Annotation.IAnnotation[] GetAnnotations ();
	Java.Lang.Annotation.IAnnotation[] GetDeclaredAnnotations ();
	bool IsAnnotationPresent (Java.Lang.Class annotationType);
}
```

<h3 id='Java.Lang.Reflect.IGenericArrayType'>New Type: Java.Lang.Reflect.IGenericArrayType</h3>

```
public interface IGenericArrayType : IDisposable, Android.Runtime.IJavaObject, IType {
	
	IType GenericComponentType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.IGenericDeclaration'>New Type: Java.Lang.Reflect.IGenericDeclaration</h3>

```
public interface IGenericDeclaration : IDisposable, Android.Runtime.IJavaObject {
	
	ITypeVariable[] GetTypeParameters ();
}
```

<h3 id='Java.Lang.Reflect.IInvocationHandler'>New Type: Java.Lang.Reflect.IInvocationHandler</h3>

```
public interface IInvocationHandler : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object Invoke (Java.Lang.Object proxy, Method method, Java.Lang.Object[] args);
}
```

<h3 id='Java.Lang.Reflect.IMember'>New Type: Java.Lang.Reflect.IMember</h3>

```
public interface IMember : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Class DeclaringClass {
		get;
	}
	bool IsSynthetic {
		get;
	}
	int Modifiers {
		get;
	}
	string Name {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.IParameterizedType'>New Type: Java.Lang.Reflect.IParameterizedType</h3>

```
public interface IParameterizedType : IDisposable, Android.Runtime.IJavaObject, IType {
	
	IType[] GetActualTypeArguments ();
	
	IType OwnerType {
		get;
	}
	IType RawType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.IType'>New Type: Java.Lang.Reflect.IType</h3>

```
public interface IType : IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Java.Lang.Reflect.ITypeVariable'>New Type: Java.Lang.Reflect.ITypeVariable</h3>

```
public interface ITypeVariable : IDisposable, Android.Runtime.IJavaObject, IType {
	
	IType[] GetBounds ();
	
	Java.Lang.Object GenericDeclaration {
		get;
	}
	string Name {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.IWildcardType'>New Type: Java.Lang.Reflect.IWildcardType</h3>

```
public interface IWildcardType : IDisposable, Android.Runtime.IJavaObject, IType {
	
	IType[] GetLowerBounds ();
	IType[] GetUpperBounds ();
}
```

<h3 id='Java.Lang.Reflect.InvocationTargetException'>New Type: Java.Lang.Reflect.InvocationTargetException</h3>

```
public class InvocationTargetException : Java.Lang.Exception {
	
	protected InvocationTargetException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected InvocationTargetException ();
	public InvocationTargetException (Java.Lang.Throwable exception);
	public InvocationTargetException (Java.Lang.Throwable exception, string detailMessage);
	
	public virtual Java.Lang.Throwable Clause {
		get;
	}
	public virtual Java.Lang.Throwable TargetException {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.MalformedParameterizedTypeException'>New Type: Java.Lang.Reflect.MalformedParameterizedTypeException</h3>

```
public class MalformedParameterizedTypeException : Java.Lang.RuntimeException {
	
	protected MalformedParameterizedTypeException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MalformedParameterizedTypeException ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.Member'>New Type: Java.Lang.Reflect.Member</h3>

```
public abstract class Member {
	
	public const int Declared = 1;
	public const int Public = 0;
}
```

<h3 id='Java.Lang.Reflect.MemberConsts'>New Type: Java.Lang.Reflect.MemberConsts</h3>

```
[Obsolete]
public abstract class MemberConsts : Member {
}
```

<h3 id='Java.Lang.Reflect.Method'>New Type: Java.Lang.Reflect.Method</h3>

```
public sealed class Method : AccessibleObject, IGenericDeclaration, IMember {
	
	public Java.Lang.Class[] GetExceptionTypes ();
	public IType[] GetGenericExceptionTypes ();
	public IType[] GetGenericParameterTypes ();
	public Java.Lang.Annotation.IAnnotation[][] GetParameterAnnotations ();
	public Java.Lang.Class[] GetParameterTypes ();
	public ITypeVariable[] GetTypeParameters ();
	public Java.Lang.Object Invoke (Java.Lang.Object receiver, params Java.Lang.Object[] args);
	public string ToGenericString ();
	
	public Java.Lang.Class DeclaringClass {
		get;
	}
	public Java.Lang.Object DefaultValue {
		get;
	}
	public IType GenericReturnType {
		get;
	}
	public bool IsBridge {
		get;
	}
	public bool IsSynthetic {
		get;
	}
	public bool IsVarArgs {
		get;
	}
	public int Modifiers {
		get;
	}
	public string Name {
		get;
	}
	public Java.Lang.Class ReturnType {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const int Declared = 1;
		public const int Public = 0;
	}
}
```

<h3 id='Java.Lang.Reflect.Modifier'>New Type: Java.Lang.Reflect.Modifier</h3>

```
public class Modifier : Java.Lang.Object {
	
	protected Modifier (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Modifier ();
	
	public static int ClassModifiers ();
	public static int ConstructorModifiers ();
	public static int FieldModifiers ();
	public static int InterfaceModifiers ();
	public static bool IsAbstract (int modifiers);
	public static bool IsFinal (int modifiers);
	public static bool IsInterface (int modifiers);
	public static bool IsNative (int modifiers);
	public static bool IsPrivate (int modifiers);
	public static bool IsProtected (int modifiers);
	public static bool IsPublic (int modifiers);
	public static bool IsStatic (int modifiers);
	public static bool IsStrict (int modifiers);
	public static bool IsSynchronized (int modifiers);
	public static bool IsTransient (int modifiers);
	public static bool IsVolatile (int modifiers);
	public static int MethodModifiers ();
	public static string ToString (int modifiers);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int Abstract = 1024;
	public const int Final = 16;
	public const int Interface = 512;
	public const int Native = 256;
	public const int Private = 2;
	public const int Protected = 4;
	public const int Public = 1;
	public const int Static = 8;
	public const int Strict = 2048;
	public const int Synchronized = 32;
	public const int Transient = 128;
	public const int Volatile = 64;
}
```

<h3 id='Java.Lang.Reflect.Proxy'>New Type: Java.Lang.Reflect.Proxy</h3>

```
public class Proxy : Java.Lang.Object, Java.IO.ISerializable {
	
	protected Proxy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Proxy (IInvocationHandler h);
	
	public static IInvocationHandler GetInvocationHandler (Java.Lang.Object proxy);
	public static Java.Lang.Class GetProxyClass (Java.Lang.ClassLoader loader, params Java.Lang.Class[] interfaces);
	public static bool IsProxyClass (Java.Lang.Class cl);
	public static Java.Lang.Object NewProxyInstance (Java.Lang.ClassLoader loader, Java.Lang.Class[] interfaces, IInvocationHandler h);
	
	protected IInvocationHandler H {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.ReflectPermission'>New Type: Java.Lang.Reflect.ReflectPermission</h3>

```
public sealed class ReflectPermission : Java.Security.BasicPermission {
	
	public ReflectPermission (string permissionName);
	public ReflectPermission (string name, string actions);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Lang.Reflect.UndeclaredThrowableException'>New Type: Java.Lang.Reflect.UndeclaredThrowableException</h3>

```
public class UndeclaredThrowableException : Java.Lang.RuntimeException {
	
	protected UndeclaredThrowableException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public UndeclaredThrowableException (Java.Lang.Throwable exception);
	public UndeclaredThrowableException (Java.Lang.Throwable exception, string detailMessage);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual Java.Lang.Throwable UndeclaredThrowable {
		get;
	}
}
```

<h2 id='Java.Net'>Namespace: Java.Net</h2>

<h3 id='Java.Net.DatagramSocket'>Type Changed: Java.Net.DatagramSocket</h3>

Added:

```
public System.Threading.Tasks.Task ConnectAsync (InetAddress anAddress, int aPort);
 	public System.Threading.Tasks.Task ConnectAsync (SocketAddress remoteAddr);
 	public System.Threading.Tasks.Task ReceiveAsync (DatagramPacket pack);
 	public System.Threading.Tasks.Task SendAsync (DatagramPacket pack);
```

<h3 id='Java.Net.DatagramSocketImpl'>Type Changed: Java.Net.DatagramSocketImpl</h3>

Added:

```
protected System.Threading.Tasks.Task ConnectAsync (InetAddress inetAddr, int port);
 	protected System.Threading.Tasks.Task<int> PeekAsync (InetAddress sender);
 	protected System.Threading.Tasks.Task<int> PeekDataAsync (DatagramPacket pack);
 	protected System.Threading.Tasks.Task ReceiveAsync (DatagramPacket pack);
 	protected System.Threading.Tasks.Task SendAsync (DatagramPacket pack);
```

<h3 id='Java.Net.JarURLConnection'>Type Changed: Java.Net.JarURLConnection</h3>

Added:

```
public virtual Java.Util.Jar.Attributes Attributes {
 		get;
 	}
 	public virtual Java.Util.Jar.JarEntry JarEntry {
 		get;
 	}
 	public abstract Java.Util.Jar.JarFile JarFile {
 		get;
 	}
 	public virtual Java.Util.Jar.Attributes MainAttributes {
 		get;
 	}
 	public virtual Java.Util.Jar.Manifest Manifest {
 		get;
 	}
```

<h3 id='Java.Net.ServerSocket'>Type Changed: Java.Net.ServerSocket</h3>

Added:

```
public System.Threading.Tasks.Task<Socket> AcceptAsync ();
 	protected System.Threading.Tasks.Task ImplAcceptAsync (Socket aSocket);
```

<h3 id='Java.Net.Socket'>Type Changed: Java.Net.Socket</h3>

Added:

```
public System.Threading.Tasks.Task ConnectAsync (SocketAddress remoteAddr);
 	public System.Threading.Tasks.Task ConnectAsync (SocketAddress remoteAddr, int timeout);
 	public System.Threading.Tasks.Task SendUrgentDataAsync (int value);
```

<h3 id='Java.Net.SocketImpl'>Type Changed: Java.Net.SocketImpl</h3>

Added:

```
protected System.Threading.Tasks.Task AcceptAsync (SocketImpl newSocket);
 	protected System.Threading.Tasks.Task ConnectAsync (InetAddress address, int port);
 	protected System.Threading.Tasks.Task ConnectAsync (SocketAddress remoteAddr, int timeout);
 	protected System.Threading.Tasks.Task ConnectAsync (string host, int port);
 	protected System.Threading.Tasks.Task SendUrgentDataAsync (int value);
```

<h3 id='Java.Net.URLClassLoader'>Type Changed: Java.Net.URLClassLoader</h3>

Added:

```
protected virtual Java.Lang.Package DefinePackage (string packageName, Java.Util.Jar.Manifest manifest, URL url);
```

<h3 id='Java.Net.URLConnection'>Type Changed: Java.Net.URLConnection</h3>

Added:

```
public System.Threading.Tasks.Task ConnectAsync ();
```

<h2 id='Java.Nio'>Namespace: Java.Nio</h2>

<h3 id='Java.Nio.MappedByteBuffer'>Type Changed: Java.Nio.MappedByteBuffer</h3>

Added:

```
public System.Threading.Tasks.Task<MappedByteBuffer> ForceAsync ();
 	public System.Threading.Tasks.Task<MappedByteBuffer> LoadAsync ();
```

<h2 id='Java.Nio.Channels'>Namespace: Java.Nio.Channels</h2>

<h3 id='Java.Nio.Channels.DatagramChannel'>Type Changed: Java.Nio.Channels.DatagramChannel</h3>

Added:

```
public System.Threading.Tasks.Task<DatagramChannel> ConnectAsync (Java.Net.SocketAddress address);
 	public System.Threading.Tasks.Task<Java.Net.SocketAddress> ReceiveAsync (Java.Nio.ByteBuffer target);
 	public System.Threading.Tasks.Task<int> SendAsync (Java.Nio.ByteBuffer source, Java.Net.SocketAddress address);
```

<h3 id='Java.Nio.Channels.FileChannel'>Type Changed: Java.Nio.Channels.FileChannel</h3>

Added:

```
public System.Threading.Tasks.Task ForceAsync (bool metadata);
 	public System.Threading.Tasks.Task<int> ReadAsync (Java.Nio.ByteBuffer buffer);
 	public System.Threading.Tasks.Task<int> ReadAsync (Java.Nio.ByteBuffer buffer, long position);
 	public System.Threading.Tasks.Task<long> ReadAsync (Java.Nio.ByteBuffer[] buffers);
 	public System.Threading.Tasks.Task<long> ReadAsync (Java.Nio.ByteBuffer[] buffers, int start, int number);
 	public System.Threading.Tasks.Task<long> TransferFromAsync (IReadableByteChannel src, long position, long count);
 	public System.Threading.Tasks.Task<long> TransferToAsync (long position, long count, IWritableByteChannel target);
 	public System.Threading.Tasks.Task<FileChannel> TruncateAsync (long size);
 	public System.Threading.Tasks.Task<int> WriteAsync (Java.Nio.ByteBuffer src);
 	public System.Threading.Tasks.Task<int> WriteAsync (Java.Nio.ByteBuffer buffer, long position);
 	public System.Threading.Tasks.Task<long> WriteAsync (Java.Nio.ByteBuffer[] buffers);
 	public System.Threading.Tasks.Task<long> WriteAsync (Java.Nio.ByteBuffer[] buffers, int offset, int length);
```

<h3 id='Java.Nio.Channels.IGatheringByteChannelExtensions'>New Type: Java.Nio.Channels.IGatheringByteChannelExtensions</h3>

```
public static class IGatheringByteChannelExtensions {
	
	public static System.Threading.Tasks.Task WriteAsync (IGatheringByteChannel self, Java.Nio.ByteBuffer[] buffers);
	public static System.Threading.Tasks.Task WriteAsync (IGatheringByteChannel self, Java.Nio.ByteBuffer[] buffers, int offset, int length);
}
```

<h3 id='Java.Nio.Channels.IReadableByteChannelExtensions'>New Type: Java.Nio.Channels.IReadableByteChannelExtensions</h3>

```
public static class IReadableByteChannelExtensions {
	
	public static System.Threading.Tasks.Task ReadAsync (IReadableByteChannel self, Java.Nio.ByteBuffer buffer);
}
```

<h3 id='Java.Nio.Channels.IScatteringByteChannelExtensions'>New Type: Java.Nio.Channels.IScatteringByteChannelExtensions</h3>

```
public static class IScatteringByteChannelExtensions {
	
	public static System.Threading.Tasks.Task ReadAsync (IScatteringByteChannel self, Java.Nio.ByteBuffer[] buffers);
	public static System.Threading.Tasks.Task ReadAsync (IScatteringByteChannel self, Java.Nio.ByteBuffer[] buffers, int offset, int length);
}
```

<h3 id='Java.Nio.Channels.IWritableByteChannelExtensions'>New Type: Java.Nio.Channels.IWritableByteChannelExtensions</h3>

```
public static class IWritableByteChannelExtensions {
	
	public static System.Threading.Tasks.Task WriteAsync (IWritableByteChannel self, Java.Nio.ByteBuffer buffer);
}
```

<h3 id='Java.Nio.Channels.Pipe'>Type Changed: Java.Nio.Channels.Pipe</h3>

Added:

```
public System.Threading.Tasks.Task<int> WriteAsync (Java.Nio.ByteBuffer buffer);
 		public System.Threading.Tasks.Task<long> WriteAsync (Java.Nio.ByteBuffer[] buffers);
 		public System.Threading.Tasks.Task<long> WriteAsync (Java.Nio.ByteBuffer[] buffers, int offset, int length);
 		public System.Threading.Tasks.Task<int> ReadAsync (Java.Nio.ByteBuffer buffer);
 		public System.Threading.Tasks.Task<long> ReadAsync (Java.Nio.ByteBuffer[] buffers);
 		public System.Threading.Tasks.Task<long> ReadAsync (Java.Nio.ByteBuffer[] buffers, int offset, int length);
```

<h3 id='Java.Nio.Channels.ServerSocketChannel'>Type Changed: Java.Nio.Channels.ServerSocketChannel</h3>

Added:

```
public System.Threading.Tasks.Task<SocketChannel> AcceptAsync ();
```

<h3 id='Java.Nio.Channels.SocketChannel'>Type Changed: Java.Nio.Channels.SocketChannel</h3>

Added:

```
public System.Threading.Tasks.Task<bool> ConnectAsync (Java.Net.SocketAddress address);
 	public System.Threading.Tasks.Task<bool> FinishConnectAsync ();
```

<h2 id='Java.Security'>Namespace: Java.Security</h2>

<h3 id='Java.Security.DigestInputStream'>New Type: Java.Security.DigestInputStream</h3>

```
public class DigestInputStream : Java.IO.FilterInputStream {
	
	protected DigestInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DigestInputStream (System.IO.Stream stream, MessageDigest digest);
	
	public virtual void On (bool on);
	
	protected MessageDigest Digest {
		get;
		set;
	}
	public virtual MessageDigest MessageDigest {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Security.DigestOutputStream'>New Type: Java.Security.DigestOutputStream</h3>

```
public class DigestOutputStream : Java.IO.FilterOutputStream {
	
	protected DigestOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DigestOutputStream (System.IO.Stream stream, MessageDigest digest);
	
	public virtual void On (bool on);
	
	protected MessageDigest Digest {
		get;
		set;
	}
	public virtual MessageDigest MessageDigest {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Java.Security.Cert'>Namespace: Java.Security.Cert</h2>

<h3 id='Java.Security.Cert.CertificateFactory'>Type Changed: Java.Security.Cert.CertificateFactory</h3>

Added:

```
public System.Threading.Tasks.Task<Certificate> GenerateCertificateAsync (System.IO.Stream inStream);
 	public System.Threading.Tasks.Task<System.Collections.Generic.ICollection<Certificate>> GenerateCertificatesAsync (System.IO.Stream inStream);
 	public System.Threading.Tasks.Task<CertPath> GenerateCertPathAsync (System.Collections.Generic.IList<Certificate> certificates);
 	public System.Threading.Tasks.Task<CertPath> GenerateCertPathAsync (System.IO.Stream inStream);
 	public System.Threading.Tasks.Task<CertPath> GenerateCertPathAsync (System.IO.Stream inStream, string encoding);
 	public System.Threading.Tasks.Task<CRL> GenerateCRLAsync (System.IO.Stream inStream);
```

<h2 id='Java.Sql'>Namespace: Java.Sql</h2>

<h3 id='Java.Sql.BatchUpdateException'>New Type: Java.Sql.BatchUpdateException</h3>

```
public class BatchUpdateException : SQLException {
	
	protected BatchUpdateException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BatchUpdateException ();
	public BatchUpdateException (int [] updateCounts);
	public BatchUpdateException (int [] p0, Java.Lang.Throwable p1);
	public BatchUpdateException (string reason, int [] updateCounts);
	public BatchUpdateException (string p0, int [] p1, Java.Lang.Throwable p2);
	public BatchUpdateException (string reason, string SQLState, int vendorCode, int [] updateCounts);
	public BatchUpdateException (string p0, string p1, int p2, int [] p3, Java.Lang.Throwable p4);
	public BatchUpdateException (string reason, string SQLState, int [] updateCounts);
	public BatchUpdateException (string p0, string p1, int [] p2, Java.Lang.Throwable p3);
	public BatchUpdateException (Java.Lang.Throwable p0);
	
	public virtual int [] GetUpdateCounts ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.ClientInfoStatus'>New Type: Java.Sql.ClientInfoStatus</h3>

```
public sealed class ClientInfoStatus : Java.Lang.Enum {
	
	public static ClientInfoStatus ValueOf (string name);
	public static ClientInfoStatus[] Values ();
	
	public static ClientInfoStatus ReasonUnknown {
		get;
		set;
	}
	public static ClientInfoStatus ReasonUnknownProperty {
		get;
		set;
	}
	public static ClientInfoStatus ReasonValueInvalid {
		get;
		set;
	}
	public static ClientInfoStatus ReasonValueTruncated {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.Connection'>New Type: Java.Sql.Connection</h3>

```
public abstract class Connection {
	
	public const int TransactionNone = 0;
	public const int TransactionReadCommitted = 2;
	public const int TransactionReadUncommitted = 1;
	public const int TransactionRepeatableRead = 4;
	public const int TransactionSerializable = 8;
}
```

<h3 id='Java.Sql.ConnectionConsts'>New Type: Java.Sql.ConnectionConsts</h3>

```
[Obsolete]
public abstract class ConnectionConsts : Connection {
}
```

<h3 id='Java.Sql.DataTruncation'>New Type: Java.Sql.DataTruncation</h3>

```
public class DataTruncation : SQLWarning {
	
	protected DataTruncation (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DataTruncation (int index, bool parameter, bool read, int dataSize, int transferSize);
	public DataTruncation (int p0, bool p1, bool p2, int p3, int p4, Java.Lang.Throwable p5);
	
	public virtual int DataSize {
		get;
	}
	public virtual int Index {
		get;
	}
	public virtual bool Parameter {
		get;
	}
	public virtual bool Read {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual int TransferSize {
		get;
	}
}
```

<h3 id='Java.Sql.DatabaseMetaData'>New Type: Java.Sql.DatabaseMetaData</h3>

```
public abstract class DatabaseMetaData {
	
	public static int FunctionColumnIn {
		get;
		set;
	}
	public static int FunctionColumnInOut {
		get;
		set;
	}
	public static int FunctionColumnOut {
		get;
		set;
	}
	public static int FunctionColumnResult {
		get;
		set;
	}
	public static int FunctionColumnUnknown {
		get;
		set;
	}
	public static int FunctionNoNulls {
		get;
		set;
	}
	public static int FunctionNoTable {
		get;
		set;
	}
	public static int FunctionNullable {
		get;
		set;
	}
	public static int FunctionNullableUnknown {
		get;
		set;
	}
	public static int FunctionResultUnknown {
		get;
		set;
	}
	public static int FunctionReturn {
		get;
		set;
	}
	public static int FunctionReturnsTable {
		get;
		set;
	}
	public static int SqlStateSQL {
		get;
		set;
	}
	
	public const short AttributeNoNulls = 0;
	public const short AttributeNullable = 1;
	public const short AttributeNullableUnknown = 2;
	public const int BestRowNotPseudo = 1;
	public const int BestRowPseudo = 2;
	public const int BestRowSession = 2;
	public const int BestRowTemporary = 0;
	public const int BestRowTransaction = 1;
	public const int BestRowUnknown = 0;
	public const int ColumnNoNulls = 0;
	public const int ColumnNullable = 1;
	public const int ColumnNullableUnknown = 2;
	public const int ImportedKeyCascade = 0;
	public const int ImportedKeyInitiallyDeferred = 5;
	public const int ImportedKeyInitiallyImmediate = 6;
	public const int ImportedKeyNoAction = 3;
	public const int ImportedKeyNotDeferrable = 7;
	public const int ImportedKeyRestrict = 1;
	public const int ImportedKeySetDefault = 4;
	public const int ImportedKeySetNull = 2;
	public const int ProcedureColumnIn = 1;
	public const int ProcedureColumnInOut = 2;
	public const int ProcedureColumnOut = 4;
	public const int ProcedureColumnResult = 3;
	public const int ProcedureColumnReturn = 5;
	public const int ProcedureColumnUnknown = 0;
	public const int ProcedureNoNulls = 0;
	public const int ProcedureNoResult = 1;
	public const int ProcedureNullable = 1;
	public const int ProcedureNullableUnknown = 2;
	public const int ProcedureResultUnknown = 0;
	public const int ProcedureReturnsResult = 2;
	public const int SqlStateSQL99 = 2;
	public const int SqlStateXOpen = 1;
	public const short TableIndexClustered = 1;
	public const short TableIndexHashed = 2;
	public const short TableIndexOther = 3;
	public const short TableIndexStatistic = 0;
	public const int TypeNoNulls = 0;
	public const int TypeNullable = 1;
	public const int TypeNullableUnknown = 2;
	public const int TypePredBasic = 2;
	public const int TypePredChar = 1;
	public const int TypePredNone = 0;
	public const int TypeSearchable = 3;
	public const int VersionColumnNotPseudo = 1;
	public const int VersionColumnPseudo = 2;
	public const int VersionColumnUnknown = 0;
}
```

<h3 id='Java.Sql.DatabaseMetaDataConsts'>New Type: Java.Sql.DatabaseMetaDataConsts</h3>

```
[Obsolete]
public abstract class DatabaseMetaDataConsts : DatabaseMetaData {
}
```

<h3 id='Java.Sql.Date'>New Type: Java.Sql.Date</h3>

```
public class Date : Java.Util.Date {
	
	protected Date (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Date (int theYear, int theMonth, int theDay);
	public Date (long theDate);
	
	public static Date ValueOf (string dateString);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.DriverManager'>New Type: Java.Sql.DriverManager</h3>

```
public class DriverManager : Java.Lang.Object {
	
	protected DriverManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static void DeregisterDriver (IDriver driver);
	public static IConnection GetConnection (string url);
	public static IConnection GetConnection (string url, Java.Util.Properties info);
	public static IConnection GetConnection (string url, string user, string password);
	public static IDriver GetDriver (string url);
	public static void Println (string message);
	public static System.Threading.Tasks.Task PrintlnAsync (string message);
	public static void RegisterDriver (IDriver driver);
	
	public static Java.Util.IEnumeration Drivers {
		get;
	}
	public static int LoginTimeout {
		get;
		set;
	}
	[Obsolete("deprecated")]
	public static Java.IO.PrintStream LogStream {
		get;
		set;
	}
	public static Java.IO.PrintWriter LogWriter {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.DriverPropertyInfo'>New Type: Java.Sql.DriverPropertyInfo</h3>

```
public class DriverPropertyInfo : Java.Lang.Object {
	
	protected DriverPropertyInfo (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DriverPropertyInfo (string name, string value);
	
	public System.Collections.Generic.IList Choices {
		get;
		set;
	}
	public string Description {
		get;
		set;
	}
	public string Name {
		get;
		set;
	}
	public bool Required {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public string Value {
		get;
		set;
	}
}
```

<h3 id='Java.Sql.IArray'>New Type: Java.Sql.IArray</h3>

```
public interface IArray : IDisposable, Android.Runtime.IJavaObject {
	
	void Free ();
	Java.Lang.Object GetArray (System.Collections.Generic.IDictionary map);
	Java.Lang.Object GetArray (long index, int count);
	Java.Lang.Object GetArray (long index, int count, System.Collections.Generic.IDictionary map);
	IResultSet GetResultSet (System.Collections.Generic.IDictionary map);
	IResultSet GetResultSet (long index, int count);
	IResultSet GetResultSet (long index, int count, System.Collections.Generic.IDictionary map);
	
	Java.Lang.Object Array {
		get;
	}
	int BaseType {
		get;
	}
	string BaseTypeName {
		get;
	}
	IResultSet ResultSet {
		get;
	}
}
```

<h3 id='Java.Sql.IBlob'>New Type: Java.Sql.IBlob</h3>

```
public interface IBlob : IDisposable, Android.Runtime.IJavaObject {
	
	void Free ();
	System.IO.Stream GetBinaryStream (long p0, long p1);
	byte [] GetBytes (long pos, int length);
	long Length ();
	long Position (byte [] pattern, long start);
	long Position (IBlob pattern, long start);
	System.IO.Stream SetBinaryStream (long pos);
	int SetBytes (long pos, byte [] theBytes);
	int SetBytes (long pos, byte [] theBytes, int offset, int len);
	void Truncate (long len);
	
	System.IO.Stream BinaryStream {
		get;
	}
}
```

<h3 id='Java.Sql.ICallableStatement'>New Type: Java.Sql.ICallableStatement</h3>

```
public interface ICallableStatement : IDisposable, Android.Runtime.IJavaObject, IPreparedStatement, IStatement, IWrapper {
	
	IArray GetArray (int parameterIndex);
	IArray GetArray (string parameterName);
	Java.Math.BigDecimal GetBigDecimal (int parameterIndex);
	[Obsolete("deprecated")]
	Java.Math.BigDecimal GetBigDecimal (int parameterIndex, int scale);
	Java.Math.BigDecimal GetBigDecimal (string parameterName);
	IBlob GetBlob (int parameterIndex);
	IBlob GetBlob (string parameterName);
	bool GetBoolean (int parameterIndex);
	bool GetBoolean (string parameterName);
	sbyte GetByte (int parameterIndex);
	sbyte GetByte (string parameterName);
	byte [] GetBytes (int parameterIndex);
	byte [] GetBytes (string parameterName);
	Java.IO.Reader GetCharacterStream (int p0);
	Java.IO.Reader GetCharacterStream (string p0);
	IClob GetClob (int parameterIndex);
	IClob GetClob (string parameterName);
	Date GetDate (int parameterIndex);
	Date GetDate (int parameterIndex, Java.Util.Calendar cal);
	Date GetDate (string parameterName);
	Date GetDate (string parameterName, Java.Util.Calendar cal);
	double GetDouble (int parameterIndex);
	double GetDouble (string parameterName);
	float GetFloat (int parameterIndex);
	float GetFloat (string parameterName);
	int GetInt (int parameterIndex);
	int GetInt (string parameterName);
	long GetLong (int parameterIndex);
	long GetLong (string parameterName);
	Java.IO.Reader GetNCharacterStream (int p0);
	Java.IO.Reader GetNCharacterStream (string p0);
	INClob GetNClob (int p0);
	INClob GetNClob (string p0);
	string GetNString (int p0);
	string GetNString (string p0);
	Java.Lang.Object GetObject (int parameterIndex);
	Java.Lang.Object GetObject (int p0, Java.Lang.Class p1);
	Java.Lang.Object GetObject (int parameterIndex, System.Collections.Generic.IDictionary map);
	Java.Lang.Object GetObject (string parameterName);
	Java.Lang.Object GetObject (string p0, Java.Lang.Class p1);
	Java.Lang.Object GetObject (string parameterName, System.Collections.Generic.IDictionary map);
	IRef GetRef (int parameterIndex);
	IRef GetRef (string parameterName);
	IRowId GetRowId (int p0);
	IRowId GetRowId (string p0);
	short GetShort (int parameterIndex);
	short GetShort (string parameterName);
	ISQLXML GetSQLXML (int p0);
	ISQLXML GetSQLXML (string p0);
	string GetString (int parameterIndex);
	string GetString (string parameterName);
	Time GetTime (int parameterIndex);
	Time GetTime (int parameterIndex, Java.Util.Calendar cal);
	Time GetTime (string parameterName);
	Time GetTime (string parameterName, Java.Util.Calendar cal);
	Timestamp GetTimestamp (int parameterIndex);
	Timestamp GetTimestamp (int parameterIndex, Java.Util.Calendar cal);
	Timestamp GetTimestamp (string parameterName);
	Timestamp GetTimestamp (string parameterName, Java.Util.Calendar cal);
	Java.Net.URL GetURL (int parameterIndex);
	Java.Net.URL GetURL (string parameterName);
	void RegisterOutParameter (int parameterIndex, int sqlType);
	void RegisterOutParameter (int parameterIndex, int sqlType, int scale);
	void RegisterOutParameter (int paramIndex, int sqlType, string typeName);
	void RegisterOutParameter (string parameterName, int sqlType);
	void RegisterOutParameter (string parameterName, int sqlType, int scale);
	void RegisterOutParameter (string parameterName, int sqlType, string typeName);
	void SetAsciiStream (string p0, System.IO.Stream p1);
	void SetAsciiStream (string parameterName, System.IO.Stream theInputStream, int length);
	void SetAsciiStream (string p0, System.IO.Stream p1, long p2);
	void SetBigDecimal (string parameterName, Java.Math.BigDecimal theBigDecimal);
	void SetBinaryStream (string p0, System.IO.Stream p1);
	void SetBinaryStream (string parameterName, System.IO.Stream theInputStream, int length);
	void SetBinaryStream (string p0, System.IO.Stream p1, long p2);
	void SetBlob (string p0, IBlob p1);
	void SetBlob (string p0, System.IO.Stream p1);
	void SetBlob (string p0, System.IO.Stream p1, long p2);
	void SetBoolean (string parameterName, bool theBoolean);
	void SetByte (string parameterName, sbyte theByte);
	void SetBytes (string parameterName, byte [] theBytes);
	void SetCharacterStream (string p0, Java.IO.Reader p1);
	void SetCharacterStream (string parameterName, Java.IO.Reader reader, int length);
	void SetCharacterStream (string p0, Java.IO.Reader p1, long p2);
	void SetClob (string p0, IClob p1);
	void SetClob (string p0, Java.IO.Reader p1);
	void SetClob (string p0, Java.IO.Reader p1, long p2);
	void SetDate (string parameterName, Date theDate);
	void SetDate (string parameterName, Date theDate, Java.Util.Calendar cal);
	void SetDouble (string parameterName, double theDouble);
	void SetFloat (string parameterName, float theFloat);
	void SetInt (string parameterName, int theInt);
	void SetLong (string parameterName, long theLong);
	void SetNCharacterStream (string p0, Java.IO.Reader p1);
	void SetNCharacterStream (string p0, Java.IO.Reader p1, long p2);
	void SetNClob (string p0, INClob p1);
	void SetNClob (string p0, Java.IO.Reader p1);
	void SetNClob (string p0, Java.IO.Reader p1, long p2);
	void SetNString (string p0, string p1);
	void SetNull (string parameterName, int sqlType);
	void SetNull (string parameterName, int sqlType, string typeName);
	void SetObject (string parameterName, Java.Lang.Object theObject);
	void SetObject (string parameterName, Java.Lang.Object theObject, int targetSqlType);
	void SetObject (string parameterName, Java.Lang.Object theObject, int targetSqlType, int scale);
	void SetRowId (string p0, IRowId p1);
	void SetShort (string parameterName, short theShort);
	void SetSQLXML (string p0, ISQLXML p1);
	void SetString (string parameterName, string theString);
	void SetTime (string parameterName, Time theTime);
	void SetTime (string parameterName, Time theTime, Java.Util.Calendar cal);
	void SetTimestamp (string parameterName, Timestamp theTimestamp);
	void SetTimestamp (string parameterName, Timestamp theTimestamp, Java.Util.Calendar cal);
	void SetURL (string parameterName, Java.Net.URL theURL);
	bool WasNull ();
}
```

<h3 id='Java.Sql.IClob'>New Type: Java.Sql.IClob</h3>

```
public interface IClob : IDisposable, Android.Runtime.IJavaObject {
	
	void Free ();
	Java.IO.Reader GetCharacterStream (long p0, long p1);
	string GetSubString (long pos, int length);
	long Length ();
	long Position (IClob searchstr, long start);
	long Position (string searchstr, long start);
	System.IO.Stream SetAsciiStream (long pos);
	Java.IO.Writer SetCharacterStream (long pos);
	int SetString (long pos, string str);
	int SetString (long pos, string str, int offset, int len);
	void Truncate (long len);
	
	System.IO.Stream AsciiStream {
		get;
	}
	Java.IO.Reader CharacterStream {
		get;
	}
}
```

<h3 id='Java.Sql.IConnection'>New Type: Java.Sql.IConnection</h3>

```
public interface IConnection : IDisposable, Android.Runtime.IJavaObject, IWrapper {
	
	void Abort (Java.Util.Concurrent.IExecutor p0);
	void ClearWarnings ();
	void Close ();
	void Commit ();
	IArray CreateArrayOf (string p0, Java.Lang.Object[] p1);
	IBlob CreateBlob ();
	IClob CreateClob ();
	INClob CreateNClob ();
	ISQLXML CreateSQLXML ();
	IStatement CreateStatement ();
	IStatement CreateStatement (int resultSetType, int resultSetConcurrency);
	IStatement CreateStatement (int resultSetType, int resultSetConcurrency, int resultSetHoldability);
	IStruct CreateStruct (string p0, Java.Lang.Object[] p1);
	string GetClientInfo (string p0);
	bool IsValid (int p0);
	string NativeSQL (string sql);
	ICallableStatement PrepareCall (string sql);
	ICallableStatement PrepareCall (string sql, int resultSetType, int resultSetConcurrency);
	ICallableStatement PrepareCall (string sql, int resultSetType, int resultSetConcurrency, int resultSetHoldability);
	IPreparedStatement PrepareStatement (string sql);
	IPreparedStatement PrepareStatement (string sql, int autoGeneratedKeys);
	IPreparedStatement PrepareStatement (string sql, int resultSetType, int resultSetConcurrency);
	IPreparedStatement PrepareStatement (string sql, int resultSetType, int resultSetConcurrency, int resultSetHoldability);
	IPreparedStatement PrepareStatement (string sql, int [] columnIndexes);
	IPreparedStatement PrepareStatement (string sql, string [] columnNames);
	void ReleaseSavepoint (ISavepoint savepoint);
	void Rollback ();
	void Rollback (ISavepoint savepoint);
	void SetClientInfo (string p0, string p1);
	void SetNetworkTimeout (Java.Util.Concurrent.IExecutor p0, int p1);
	ISavepoint SetSavepoint ();
	ISavepoint SetSavepoint (string name);
	
	bool AutoCommit {
		get;
		set;
	}
	string Catalog {
		get;
		set;
	}
	Java.Util.Properties ClientInfo {
		get;
		set;
	}
	int Holdability {
		get;
		set;
	}
	bool IsClosed {
		get;
	}
	IDatabaseMetaData MetaData {
		get;
	}
	int NetworkTimeout {
		get;
	}
	bool ReadOnly {
		get;
		set;
	}
	string Schema {
		get;
		set;
	}
	int TransactionIsolation {
		get;
		set;
	}
	System.Collections.Generic.IDictionary TypeMap {
		get;
		set;
	}
	SQLWarning Warnings {
		get;
	}
}
```

<h3 id='Java.Sql.IDatabaseMetaData'>New Type: Java.Sql.IDatabaseMetaData</h3>

```
public interface IDatabaseMetaData : IDisposable, Android.Runtime.IJavaObject, IWrapper {
	
	bool AllProceduresAreCallable ();
	bool AllTablesAreSelectable ();
	bool AutoCommitFailureClosesAllResultSets ();
	bool DataDefinitionCausesTransactionCommit ();
	bool DataDefinitionIgnoredInTransactions ();
	bool DeletesAreDetected (int type);
	bool DoesMaxRowSizeIncludeBlobs ();
	bool GeneratedKeyAlwaysReturned ();
	IResultSet GetAttributes (string catalog, string schemaPattern, string typeNamePattern, string attributeNamePattern);
	IResultSet GetBestRowIdentifier (string catalog, string schema, string table, int scope, bool nullable);
	IResultSet GetColumnPrivileges (string catalog, string schema, string table, string columnNamePattern);
	IResultSet GetColumns (string catalog, string schemaPattern, string tableNamePattern, string columnNamePattern);
	IResultSet GetCrossReference (string primaryCatalog, string primarySchema, string primaryTable, string foreignCatalog, string foreignSchema, string foreignTable);
	IResultSet GetExportedKeys (string catalog, string schema, string table);
	IResultSet GetFunctionColumns (string p0, string p1, string p2, string p3);
	IResultSet GetFunctions (string p0, string p1, string p2);
	IResultSet GetImportedKeys (string catalog, string schema, string table);
	IResultSet GetIndexInfo (string catalog, string schema, string table, bool unique, bool approximate);
	IResultSet GetPrimaryKeys (string catalog, string schema, string table);
	IResultSet GetProcedureColumns (string catalog, string schemaPattern, string procedureNamePattern, string columnNamePattern);
	IResultSet GetProcedures (string catalog, string schemaPattern, string procedureNamePattern);
	IResultSet GetPseudoColumns (string p0, string p1, string p2, string p3);
	IResultSet GetSchemas (string p0, string p1);
	IResultSet GetSuperTables (string catalog, string schemaPattern, string tableNamePattern);
	IResultSet GetSuperTypes (string catalog, string schemaPattern, string typeNamePattern);
	IResultSet GetTablePrivileges (string catalog, string schemaPattern, string tableNamePattern);
	IResultSet GetTables (string catalog, string schemaPattern, string tableNamePattern, string [] types);
	IResultSet GetUDTs (string catalog, string schemaPattern, string typeNamePattern, int [] types);
	IResultSet GetVersionColumns (string catalog, string schema, string table);
	bool InsertsAreDetected (int type);
	bool LocatorsUpdateCopy ();
	bool NullPlusNonNullIsNull ();
	bool NullsAreSortedAtEnd ();
	bool NullsAreSortedAtStart ();
	bool NullsAreSortedHigh ();
	bool NullsAreSortedLow ();
	bool OthersDeletesAreVisible (int type);
	bool OthersInsertsAreVisible (int type);
	bool OthersUpdatesAreVisible (int type);
	bool OwnDeletesAreVisible (int type);
	bool OwnInsertsAreVisible (int type);
	bool OwnUpdatesAreVisible (int type);
	bool StoresLowerCaseIdentifiers ();
	bool StoresLowerCaseQuotedIdentifiers ();
	bool StoresMixedCaseIdentifiers ();
	bool StoresMixedCaseQuotedIdentifiers ();
	bool StoresUpperCaseIdentifiers ();
	bool StoresUpperCaseQuotedIdentifiers ();
	bool SupportsAlterTableWithAddColumn ();
	bool SupportsAlterTableWithDropColumn ();
	bool SupportsANSI92EntryLevelSQL ();
	bool SupportsANSI92FullSQL ();
	bool SupportsANSI92IntermediateSQL ();
	bool SupportsBatchUpdates ();
	bool SupportsCatalogsInDataManipulation ();
	bool SupportsCatalogsInIndexDefinitions ();
	bool SupportsCatalogsInPrivilegeDefinitions ();
	bool SupportsCatalogsInProcedureCalls ();
	bool SupportsCatalogsInTableDefinitions ();
	bool SupportsColumnAliasing ();
	bool SupportsConvert ();
	bool SupportsConvert (int fromType, int toType);
	bool SupportsCoreSQLGrammar ();
	bool SupportsCorrelatedSubqueries ();
	bool SupportsDataDefinitionAndDataManipulationTransactions ();
	bool SupportsDataManipulationTransactionsOnly ();
	bool SupportsDifferentTableCorrelationNames ();
	bool SupportsExpressionsInOrderBy ();
	bool SupportsExtendedSQLGrammar ();
	bool SupportsFullOuterJoins ();
	bool SupportsGetGeneratedKeys ();
	bool SupportsGroupBy ();
	bool SupportsGroupByBeyondSelect ();
	bool SupportsGroupByUnrelated ();
	bool SupportsIntegrityEnhancementFacility ();
	bool SupportsLikeEscapeClause ();
	bool SupportsLimitedOuterJoins ();
	bool SupportsMinimumSQLGrammar ();
	bool SupportsMixedCaseIdentifiers ();
	bool SupportsMixedCaseQuotedIdentifiers ();
	bool SupportsMultipleOpenResults ();
	bool SupportsMultipleResultSets ();
	bool SupportsMultipleTransactions ();
	bool SupportsNamedParameters ();
	bool SupportsNonNullableColumns ();
	bool SupportsOpenCursorsAcrossCommit ();
	bool SupportsOpenCursorsAcrossRollback ();
	bool SupportsOpenStatementsAcrossCommit ();
	bool SupportsOpenStatementsAcrossRollback ();
	bool SupportsOrderByUnrelated ();
	bool SupportsOuterJoins ();
	bool SupportsPositionedDelete ();
	bool SupportsPositionedUpdate ();
	bool SupportsResultSetConcurrency (int type, int concurrency);
	bool SupportsResultSetHoldability (int holdability);
	bool SupportsResultSetType (int type);
	bool SupportsSavepoints ();
	bool SupportsSchemasInDataManipulation ();
	bool SupportsSchemasInIndexDefinitions ();
	bool SupportsSchemasInPrivilegeDefinitions ();
	bool SupportsSchemasInProcedureCalls ();
	bool SupportsSchemasInTableDefinitions ();
	bool SupportsSelectForUpdate ();
	bool SupportsStatementPooling ();
	bool SupportsStoredFunctionsUsingCallSyntax ();
	bool SupportsStoredProcedures ();
	bool SupportsSubqueriesInComparisons ();
	bool SupportsSubqueriesInExists ();
	bool SupportsSubqueriesInIns ();
	bool SupportsSubqueriesInQuantifieds ();
	bool SupportsTableCorrelationNames ();
	bool SupportsTransactionIsolationLevel (int level);
	bool SupportsTransactions ();
	bool SupportsUnion ();
	bool SupportsUnionAll ();
	bool UpdatesAreDetected (int type);
	bool UsesLocalFilePerTable ();
	bool UsesLocalFiles ();
	
	IResultSet Catalogs {
		get;
	}
	string CatalogSeparator {
		get;
	}
	string CatalogTerm {
		get;
	}
	IResultSet ClientInfoProperties {
		get;
	}
	IConnection Connection {
		get;
	}
	int DatabaseMajorVersion {
		get;
	}
	int DatabaseMinorVersion {
		get;
	}
	string DatabaseProductName {
		get;
	}
	string DatabaseProductVersion {
		get;
	}
	int DefaultTransactionIsolation {
		get;
	}
	int DriverMajorVersion {
		get;
	}
	int DriverMinorVersion {
		get;
	}
	string DriverName {
		get;
	}
	string DriverVersion {
		get;
	}
	string ExtraNameCharacters {
		get;
	}
	string IdentifierQuoteString {
		get;
	}
	bool IsCatalogAtStart {
		get;
	}
	bool IsReadOnly {
		get;
	}
	int JDBCMajorVersion {
		get;
	}
	int JDBCMinorVersion {
		get;
	}
	int MaxBinaryLiteralLength {
		get;
	}
	int MaxCatalogNameLength {
		get;
	}
	int MaxCharLiteralLength {
		get;
	}
	int MaxColumnNameLength {
		get;
	}
	int MaxColumnsInGroupBy {
		get;
	}
	int MaxColumnsInIndex {
		get;
	}
	int MaxColumnsInOrderBy {
		get;
	}
	int MaxColumnsInSelect {
		get;
	}
	int MaxColumnsInTable {
		get;
	}
	int MaxConnections {
		get;
	}
	int MaxCursorNameLength {
		get;
	}
	int MaxIndexLength {
		get;
	}
	int MaxProcedureNameLength {
		get;
	}
	int MaxRowSize {
		get;
	}
	int MaxSchemaNameLength {
		get;
	}
	int MaxStatementLength {
		get;
	}
	int MaxStatements {
		get;
	}
	int MaxTableNameLength {
		get;
	}
	int MaxTablesInSelect {
		get;
	}
	int MaxUserNameLength {
		get;
	}
	string NumericFunctions {
		get;
	}
	string ProcedureTerm {
		get;
	}
	int ResultSetHoldability {
		get;
	}
	RowIdLifetime RowIdLifetime {
		get;
	}
	IResultSet Schemas {
		get;
	}
	string SchemaTerm {
		get;
	}
	string SearchStringEscape {
		get;
	}
	string SQLKeywords {
		get;
	}
	int SQLStateType {
		get;
	}
	string StringFunctions {
		get;
	}
	string SystemFunctions {
		get;
	}
	IResultSet TableTypes {
		get;
	}
	string TimeDateFunctions {
		get;
	}
	IResultSet TypeInfo {
		get;
	}
	string URL {
		get;
	}
	string UserName {
		get;
	}
}
```

<h3 id='Java.Sql.IDriver'>New Type: Java.Sql.IDriver</h3>

```
public interface IDriver : IDisposable, Android.Runtime.IJavaObject {
	
	bool AcceptsURL (string url);
	IConnection Connect (string url, Java.Util.Properties info);
	DriverPropertyInfo[] GetPropertyInfo (string url, Java.Util.Properties info);
	bool JdbcCompliant ();
	
	int MajorVersion {
		get;
	}
	int MinorVersion {
		get;
	}
	Java.Util.Logging.Logger ParentLogger {
		get;
	}
}
```

<h3 id='Java.Sql.IDriverExtensions'>New Type: Java.Sql.IDriverExtensions</h3>

```
public static class IDriverExtensions {
	
	public static System.Threading.Tasks.Task ConnectAsync (IDriver self, string url, Java.Util.Properties info);
}
```

<h3 id='Java.Sql.INClob'>New Type: Java.Sql.INClob</h3>

```
public interface INClob : IClob, IDisposable, Android.Runtime.IJavaObject {
}
```

<h3 id='Java.Sql.IParameterMetaData'>New Type: Java.Sql.IParameterMetaData</h3>

```
public interface IParameterMetaData : IDisposable, Android.Runtime.IJavaObject, IWrapper {
	
	string GetParameterClassName (int paramIndex);
	int GetParameterMode (int paramIndex);
	int GetParameterType (int paramIndex);
	string GetParameterTypeName (int paramIndex);
	int GetPrecision (int paramIndex);
	int GetScale (int paramIndex);
	int IsNullable (int paramIndex);
	bool IsSigned (int paramIndex);
	
	int ParameterCount {
		get;
	}
}
```

<h3 id='Java.Sql.IPreparedStatement'>New Type: Java.Sql.IPreparedStatement</h3>

```
public interface IPreparedStatement : IDisposable, Android.Runtime.IJavaObject, IStatement, IWrapper {
	
	void AddBatch ();
	void ClearParameters ();
	bool Execute ();
	IResultSet ExecuteQuery ();
	int ExecuteUpdate ();
	void SetArray (int parameterIndex, IArray theArray);
	void SetAsciiStream (int p0, System.IO.Stream p1);
	void SetAsciiStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	void SetAsciiStream (int p0, System.IO.Stream p1, long p2);
	void SetBigDecimal (int parameterIndex, Java.Math.BigDecimal theBigDecimal);
	void SetBinaryStream (int p0, System.IO.Stream p1);
	void SetBinaryStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	void SetBinaryStream (int p0, System.IO.Stream p1, long p2);
	void SetBlob (int parameterIndex, IBlob theBlob);
	void SetBlob (int p0, System.IO.Stream p1);
	void SetBlob (int p0, System.IO.Stream p1, long p2);
	void SetBoolean (int parameterIndex, bool theBoolean);
	void SetByte (int parameterIndex, sbyte theByte);
	void SetBytes (int parameterIndex, byte [] theBytes);
	void SetCharacterStream (int p0, Java.IO.Reader p1);
	void SetCharacterStream (int parameterIndex, Java.IO.Reader reader, int length);
	void SetCharacterStream (int p0, Java.IO.Reader p1, long p2);
	void SetClob (int parameterIndex, IClob theClob);
	void SetClob (int p0, Java.IO.Reader p1);
	void SetClob (int p0, Java.IO.Reader p1, long p2);
	void SetDate (int parameterIndex, Date theDate);
	void SetDate (int parameterIndex, Date theDate, Java.Util.Calendar cal);
	void SetDouble (int parameterIndex, double theDouble);
	void SetFloat (int parameterIndex, float theFloat);
	void SetInt (int parameterIndex, int theInt);
	void SetLong (int parameterIndex, long theLong);
	void SetNCharacterStream (int p0, Java.IO.Reader p1);
	void SetNCharacterStream (int p0, Java.IO.Reader p1, long p2);
	void SetNClob (int p0, INClob p1);
	void SetNClob (int p0, Java.IO.Reader p1);
	void SetNClob (int p0, Java.IO.Reader p1, long p2);
	void SetNString (int p0, string p1);
	void SetNull (int parameterIndex, int sqlType);
	void SetNull (int paramIndex, int sqlType, string typeName);
	void SetObject (int parameterIndex, Java.Lang.Object theObject);
	void SetObject (int parameterIndex, Java.Lang.Object theObject, int targetSqlType);
	void SetObject (int parameterIndex, Java.Lang.Object theObject, int targetSqlType, int scale);
	void SetRef (int parameterIndex, IRef theRef);
	void SetRowId (int p0, IRowId p1);
	void SetShort (int parameterIndex, short theShort);
	void SetSQLXML (int p0, ISQLXML p1);
	void SetString (int parameterIndex, string theString);
	void SetTime (int parameterIndex, Time theTime);
	void SetTime (int parameterIndex, Time theTime, Java.Util.Calendar cal);
	void SetTimestamp (int parameterIndex, Timestamp theTimestamp);
	void SetTimestamp (int parameterIndex, Timestamp theTimestamp, Java.Util.Calendar cal);
	[Obsolete("deprecated")]
	void SetUnicodeStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	void SetURL (int parameterIndex, Java.Net.URL theURL);
	
	IResultSetMetaData MetaData {
		get;
	}
	IParameterMetaData ParameterMetaData {
		get;
	}
}
```

<h3 id='Java.Sql.IRef'>New Type: Java.Sql.IRef</h3>

```
public interface IRef : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object GetObject (System.Collections.Generic.IDictionary map);
	
	string BaseTypeName {
		get;
	}
	Java.Lang.Object Object {
		get;
		set;
	}
}
```

<h3 id='Java.Sql.IResultSet'>New Type: Java.Sql.IResultSet</h3>

```
public interface IResultSet : IDisposable, Android.Runtime.IJavaObject, IWrapper {
	
	bool Absolute (int row);
	void AfterLast ();
	void BeforeFirst ();
	void CancelRowUpdates ();
	void ClearWarnings ();
	void Close ();
	void DeleteRow ();
	int FindColumn (string columnName);
	bool First ();
	IArray GetArray (int columnIndex);
	IArray GetArray (string colName);
	System.IO.Stream GetAsciiStream (int columnIndex);
	System.IO.Stream GetAsciiStream (string columnName);
	Java.Math.BigDecimal GetBigDecimal (int columnIndex);
	[Obsolete("deprecated")]
	Java.Math.BigDecimal GetBigDecimal (int columnIndex, int scale);
	Java.Math.BigDecimal GetBigDecimal (string columnName);
	[Obsolete("deprecated")]
	Java.Math.BigDecimal GetBigDecimal (string columnName, int scale);
	System.IO.Stream GetBinaryStream (int columnIndex);
	System.IO.Stream GetBinaryStream (string columnName);
	IBlob GetBlob (int columnIndex);
	IBlob GetBlob (string columnName);
	bool GetBoolean (int columnIndex);
	bool GetBoolean (string columnName);
	sbyte GetByte (int columnIndex);
	sbyte GetByte (string columnName);
	byte [] GetBytes (int columnIndex);
	byte [] GetBytes (string columnName);
	Java.IO.Reader GetCharacterStream (int columnIndex);
	Java.IO.Reader GetCharacterStream (string columnName);
	IClob GetClob (int columnIndex);
	IClob GetClob (string colName);
	Date GetDate (int columnIndex);
	Date GetDate (int columnIndex, Java.Util.Calendar cal);
	Date GetDate (string columnName);
	Date GetDate (string columnName, Java.Util.Calendar cal);
	double GetDouble (int columnIndex);
	double GetDouble (string columnName);
	float GetFloat (int columnIndex);
	float GetFloat (string columnName);
	int GetInt (int columnIndex);
	int GetInt (string columnName);
	long GetLong (int columnIndex);
	long GetLong (string columnName);
	Java.IO.Reader GetNCharacterStream (int p0);
	Java.IO.Reader GetNCharacterStream (string p0);
	INClob GetNClob (int p0);
	INClob GetNClob (string p0);
	string GetNString (int p0);
	string GetNString (string p0);
	Java.Lang.Object GetObject (int columnIndex);
	Java.Lang.Object GetObject (int p0, Java.Lang.Class p1);
	Java.Lang.Object GetObject (int columnIndex, System.Collections.Generic.IDictionary map);
	Java.Lang.Object GetObject (string columnName);
	Java.Lang.Object GetObject (string p0, Java.Lang.Class p1);
	Java.Lang.Object GetObject (string columnName, System.Collections.Generic.IDictionary map);
	IRef GetRef (int columnIndex);
	IRef GetRef (string colName);
	IRowId GetRowId (int p0);
	IRowId GetRowId (string p0);
	short GetShort (int columnIndex);
	short GetShort (string columnName);
	ISQLXML GetSQLXML (int p0);
	ISQLXML GetSQLXML (string p0);
	string GetString (int columnIndex);
	string GetString (string columnName);
	Time GetTime (int columnIndex);
	Time GetTime (int columnIndex, Java.Util.Calendar cal);
	Time GetTime (string columnName);
	Time GetTime (string columnName, Java.Util.Calendar cal);
	Timestamp GetTimestamp (int columnIndex);
	Timestamp GetTimestamp (int columnIndex, Java.Util.Calendar cal);
	Timestamp GetTimestamp (string columnName);
	Timestamp GetTimestamp (string columnName, Java.Util.Calendar cal);
	[Obsolete("deprecated")]
	System.IO.Stream GetUnicodeStream (int columnIndex);
	[Obsolete("deprecated")]
	System.IO.Stream GetUnicodeStream (string columnName);
	Java.Net.URL GetURL (int columnIndex);
	Java.Net.URL GetURL (string columnName);
	void InsertRow ();
	bool Last ();
	void MoveToCurrentRow ();
	void MoveToInsertRow ();
	bool Next ();
	bool Previous ();
	void RefreshRow ();
	bool Relative (int rows);
	bool RowDeleted ();
	bool RowInserted ();
	bool RowUpdated ();
	void UpdateArray (int columnIndex, IArray x);
	void UpdateArray (string columnName, IArray x);
	void UpdateAsciiStream (int p0, System.IO.Stream p1);
	void UpdateAsciiStream (int columnIndex, System.IO.Stream x, int length);
	void UpdateAsciiStream (int p0, System.IO.Stream p1, long p2);
	void UpdateAsciiStream (string p0, System.IO.Stream p1);
	void UpdateAsciiStream (string columnName, System.IO.Stream x, int length);
	void UpdateAsciiStream (string p0, System.IO.Stream p1, long p2);
	void UpdateBigDecimal (int columnIndex, Java.Math.BigDecimal x);
	void UpdateBigDecimal (string columnName, Java.Math.BigDecimal x);
	void UpdateBinaryStream (int p0, System.IO.Stream p1);
	void UpdateBinaryStream (int columnIndex, System.IO.Stream x, int length);
	void UpdateBinaryStream (int p0, System.IO.Stream p1, long p2);
	void UpdateBinaryStream (string p0, System.IO.Stream p1);
	void UpdateBinaryStream (string columnName, System.IO.Stream x, int length);
	void UpdateBinaryStream (string p0, System.IO.Stream p1, long p2);
	void UpdateBlob (int columnIndex, IBlob x);
	void UpdateBlob (int p0, System.IO.Stream p1);
	void UpdateBlob (int p0, System.IO.Stream p1, long p2);
	void UpdateBlob (string columnName, IBlob x);
	void UpdateBlob (string p0, System.IO.Stream p1);
	void UpdateBlob (string p0, System.IO.Stream p1, long p2);
	void UpdateBoolean (int columnIndex, bool x);
	void UpdateBoolean (string columnName, bool x);
	void UpdateByte (int columnIndex, sbyte x);
	void UpdateByte (string columnName, sbyte x);
	void UpdateBytes (int columnIndex, byte [] x);
	void UpdateBytes (string columnName, byte [] x);
	void UpdateCharacterStream (int p0, Java.IO.Reader p1);
	void UpdateCharacterStream (int columnIndex, Java.IO.Reader x, int length);
	void UpdateCharacterStream (int p0, Java.IO.Reader p1, long p2);
	void UpdateCharacterStream (string p0, Java.IO.Reader p1);
	void UpdateCharacterStream (string columnName, Java.IO.Reader reader, int length);
	void UpdateCharacterStream (string p0, Java.IO.Reader p1, long p2);
	void UpdateClob (int columnIndex, IClob x);
	void UpdateClob (int p0, Java.IO.Reader p1);
	void UpdateClob (int p0, Java.IO.Reader p1, long p2);
	void UpdateClob (string columnName, IClob x);
	void UpdateClob (string p0, Java.IO.Reader p1);
	void UpdateClob (string p0, Java.IO.Reader p1, long p2);
	void UpdateDate (int columnIndex, Date x);
	void UpdateDate (string columnName, Date x);
	void UpdateDouble (int columnIndex, double x);
	void UpdateDouble (string columnName, double x);
	void UpdateFloat (int columnIndex, float x);
	void UpdateFloat (string columnName, float x);
	void UpdateInt (int columnIndex, int x);
	void UpdateInt (string columnName, int x);
	void UpdateLong (int columnIndex, long x);
	void UpdateLong (string columnName, long x);
	void UpdateNCharacterStream (int p0, Java.IO.Reader p1);
	void UpdateNCharacterStream (int p0, Java.IO.Reader p1, long p2);
	void UpdateNCharacterStream (string p0, Java.IO.Reader p1);
	void UpdateNCharacterStream (string p0, Java.IO.Reader p1, long p2);
	void UpdateNClob (int p0, INClob p1);
	void UpdateNClob (int p0, Java.IO.Reader p1);
	void UpdateNClob (int p0, Java.IO.Reader p1, long p2);
	void UpdateNClob (string p0, INClob p1);
	void UpdateNClob (string p0, Java.IO.Reader p1);
	void UpdateNClob (string p0, Java.IO.Reader p1, long p2);
	void UpdateNString (int p0, string p1);
	void UpdateNString (string p0, string p1);
	void UpdateNull (int columnIndex);
	void UpdateNull (string columnName);
	void UpdateObject (int columnIndex, Java.Lang.Object x);
	void UpdateObject (int columnIndex, Java.Lang.Object x, int scale);
	void UpdateObject (string columnName, Java.Lang.Object x);
	void UpdateObject (string columnName, Java.Lang.Object x, int scale);
	void UpdateRef (int columnIndex, IRef x);
	void UpdateRef (string columnName, IRef x);
	void UpdateRow ();
	void UpdateRowId (int p0, IRowId p1);
	void UpdateRowId (string p0, IRowId p1);
	void UpdateShort (int columnIndex, short x);
	void UpdateShort (string columnName, short x);
	void UpdateSQLXML (int p0, ISQLXML p1);
	void UpdateSQLXML (string p0, ISQLXML p1);
	void UpdateString (int columnIndex, string x);
	void UpdateString (string columnName, string x);
	void UpdateTime (int columnIndex, Time x);
	void UpdateTime (string columnName, Time x);
	void UpdateTimestamp (int columnIndex, Timestamp x);
	void UpdateTimestamp (string columnName, Timestamp x);
	bool WasNull ();
	
	int Concurrency {
		get;
	}
	string CursorName {
		get;
	}
	int FetchDirection {
		get;
		set;
	}
	int FetchSize {
		get;
		set;
	}
	int Holdability {
		get;
	}
	bool IsAfterLast {
		get;
	}
	bool IsBeforeFirst {
		get;
	}
	bool IsClosed {
		get;
	}
	bool IsFirst {
		get;
	}
	bool IsLast {
		get;
	}
	IResultSetMetaData MetaData {
		get;
	}
	int Row {
		get;
	}
	IStatement Statement {
		get;
	}
	int Type {
		get;
	}
	SQLWarning Warnings {
		get;
	}
}
```

<h3 id='Java.Sql.IResultSetMetaData'>New Type: Java.Sql.IResultSetMetaData</h3>

```
public interface IResultSetMetaData : IDisposable, Android.Runtime.IJavaObject, IWrapper {
	
	string GetCatalogName (int column);
	string GetColumnClassName (int column);
	int GetColumnDisplaySize (int column);
	string GetColumnLabel (int column);
	string GetColumnName (int column);
	int GetColumnType (int column);
	string GetColumnTypeName (int column);
	int GetPrecision (int column);
	int GetScale (int column);
	string GetSchemaName (int column);
	string GetTableName (int column);
	bool IsAutoIncrement (int column);
	bool IsCaseSensitive (int column);
	bool IsCurrency (int column);
	bool IsDefinitelyWritable (int column);
	int IsNullable (int column);
	bool IsReadOnly (int column);
	bool IsSearchable (int column);
	bool IsSigned (int column);
	bool IsWritable (int column);
	
	int ColumnCount {
		get;
	}
}
```

<h3 id='Java.Sql.IRowId'>New Type: Java.Sql.IRowId</h3>

```
public interface IRowId : IDisposable, Android.Runtime.IJavaObject {
	
	bool Equals (Java.Lang.Object obj);
	byte [] GetBytes ();
	int GetHashCode ();
	string ToString ();
}
```

<h3 id='Java.Sql.ISQLData'>New Type: Java.Sql.ISQLData</h3>

```
public interface ISQLData : IDisposable, Android.Runtime.IJavaObject {
	
	void ReadSQL (ISQLInput stream, string typeName);
	void WriteSQL (ISQLOutput stream);
	
	string SQLTypeName {
		get;
	}
}
```

<h3 id='Java.Sql.ISQLInput'>New Type: Java.Sql.ISQLInput</h3>

```
public interface ISQLInput : IDisposable, Android.Runtime.IJavaObject {
	
	IArray ReadArray ();
	System.IO.Stream ReadAsciiStream ();
	Java.Math.BigDecimal ReadBigDecimal ();
	System.IO.Stream ReadBinaryStream ();
	IBlob ReadBlob ();
	bool ReadBoolean ();
	sbyte ReadByte ();
	byte [] ReadBytes ();
	Java.IO.Reader ReadCharacterStream ();
	IClob ReadClob ();
	Date ReadDate ();
	double ReadDouble ();
	float ReadFloat ();
	int ReadInt ();
	long ReadLong ();
	INClob ReadNClob ();
	string ReadNString ();
	Java.Lang.Object ReadObject ();
	IRef ReadRef ();
	IRowId ReadRowId ();
	short ReadShort ();
	ISQLXML ReadSQLXML ();
	string ReadString ();
	Time ReadTime ();
	Timestamp ReadTimestamp ();
	Java.Net.URL ReadURL ();
	bool WasNull ();
}
```

<h3 id='Java.Sql.ISQLOutput'>New Type: Java.Sql.ISQLOutput</h3>

```
public interface ISQLOutput : IDisposable, Android.Runtime.IJavaObject {
	
	void WriteArray (IArray theArray);
	void WriteAsciiStream (System.IO.Stream theStream);
	void WriteBigDecimal (Java.Math.BigDecimal theBigDecimal);
	void WriteBinaryStream (System.IO.Stream theStream);
	void WriteBlob (IBlob theBlob);
	void WriteBoolean (bool theFlag);
	void WriteByte (sbyte theByte);
	void WriteBytes (byte [] theBytes);
	void WriteCharacterStream (Java.IO.Reader theStream);
	void WriteClob (IClob theClob);
	void WriteDate (Date theDate);
	void WriteDouble (double theDouble);
	void WriteFloat (float theFloat);
	void WriteInt (int theInt);
	void WriteLong (long theLong);
	void WriteNClob (INClob p0);
	void WriteNString (string p0);
	void WriteObject (ISQLData theObject);
	void WriteRef (IRef theRef);
	void WriteRowId (IRowId p0);
	void WriteShort (short theShort);
	void WriteSQLXML (ISQLXML p0);
	void WriteString (string theString);
	void WriteStruct (IStruct theStruct);
	void WriteTime (Time theTime);
	void WriteTimestamp (Timestamp theTimestamp);
	void WriteURL (Java.Net.URL theURL);
}
```

<h3 id='Java.Sql.ISQLXML'>New Type: Java.Sql.ISQLXML</h3>

```
public interface ISQLXML : IDisposable, Android.Runtime.IJavaObject {
	
	void Free ();
	Java.Lang.Object GetSource (Java.Lang.Class sourceClass);
	System.IO.Stream SetBinaryStream ();
	Java.IO.Writer SetCharacterStream ();
	Java.Lang.Object SetResult (Java.Lang.Class resultClass);
	
	System.IO.Stream BinaryStream {
		get;
	}
	Java.IO.Reader CharacterStream {
		get;
	}
	string String {
		get;
		set;
	}
}
```

<h3 id='Java.Sql.ISavepoint'>New Type: Java.Sql.ISavepoint</h3>

```
public interface ISavepoint : IDisposable, Android.Runtime.IJavaObject {
	
	int SavepointId {
		get;
	}
	string SavepointName {
		get;
	}
}
```

<h3 id='Java.Sql.IStatement'>New Type: Java.Sql.IStatement</h3>

```
public interface IStatement : IDisposable, Android.Runtime.IJavaObject, IWrapper {
	
	void AddBatch (string sql);
	void Cancel ();
	void ClearBatch ();
	void ClearWarnings ();
	void Close ();
	void CloseOnCompletion ();
	bool Execute (string sql);
	bool Execute (string sql, int autoGeneratedKeys);
	bool Execute (string sql, int [] columnIndexes);
	bool Execute (string sql, string [] columnNames);
	int [] ExecuteBatch ();
	IResultSet ExecuteQuery (string sql);
	int ExecuteUpdate (string sql);
	int ExecuteUpdate (string sql, int autoGeneratedKeys);
	int ExecuteUpdate (string sql, int [] columnIndexes);
	int ExecuteUpdate (string sql, string [] columnNames);
	bool GetMoreResults (int current);
	void SetCursorName (string name);
	void SetEscapeProcessing (bool enable);
	
	IConnection Connection {
		get;
	}
	int FetchDirection {
		get;
		set;
	}
	int FetchSize {
		get;
		set;
	}
	IResultSet GeneratedKeys {
		get;
	}
	bool IsClosed {
		get;
	}
	bool IsCloseOnCompletion {
		get;
	}
	int MaxFieldSize {
		get;
		set;
	}
	int MaxRows {
		get;
		set;
	}
	bool MoreResults {
		get;
	}
	bool Poolable {
		get;
		set;
	}
	int QueryTimeout {
		get;
		set;
	}
	IResultSet ResultSet {
		get;
	}
	int ResultSetConcurrency {
		get;
	}
	int ResultSetHoldability {
		get;
	}
	int ResultSetType {
		get;
	}
	int UpdateCount {
		get;
	}
	SQLWarning Warnings {
		get;
	}
}
```

<h3 id='Java.Sql.IStruct'>New Type: Java.Sql.IStruct</h3>

```
public interface IStruct : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object[] GetAttributes ();
	Java.Lang.Object[] GetAttributes (System.Collections.Generic.IDictionary theMap);
	
	string SQLTypeName {
		get;
	}
}
```

<h3 id='Java.Sql.IWrapper'>New Type: Java.Sql.IWrapper</h3>

```
public interface IWrapper : IDisposable, Android.Runtime.IJavaObject {
	
	bool IsWrapperFor (Java.Lang.Class iface);
	Java.Lang.Object Unwrap (Java.Lang.Class iface);
}
```

<h3 id='Java.Sql.ParameterMetaData'>New Type: Java.Sql.ParameterMetaData</h3>

```
public abstract class ParameterMetaData {
	
	public const int ParameterModeIn = 1;
	public const int ParameterModeInOut = 2;
	public const int ParameterModeOut = 4;
	public const int ParameterModeUnknown = 0;
	public const int ParameterNoNulls = 0;
	public const int ParameterNullable = 1;
	public const int ParameterNullableUnknown = 2;
}
```

<h3 id='Java.Sql.ParameterMetaDataConsts'>New Type: Java.Sql.ParameterMetaDataConsts</h3>

```
[Obsolete]
public abstract class ParameterMetaDataConsts : ParameterMetaData {
}
```

<h3 id='Java.Sql.ResultSet'>New Type: Java.Sql.ResultSet</h3>

```
public abstract class ResultSet {
	
	public const int CloseCursorsAtCommit = 2;
	public const int ConcurReadOnly = 1007;
	public const int ConcurUpdatable = 1008;
	public const int FetchForward = 1000;
	public const int FetchReverse = 1001;
	public const int FetchUnknown = 1002;
	public const int HoldCursorsOverCommit = 1;
	public const int TypeForwardOnly = 1003;
	public const int TypeScrollInsensitive = 1004;
	public const int TypeScrollSensitive = 1005;
}
```

<h3 id='Java.Sql.ResultSetConsts'>New Type: Java.Sql.ResultSetConsts</h3>

```
[Obsolete]
public abstract class ResultSetConsts : ResultSet {
}
```

<h3 id='Java.Sql.ResultSetMetaData'>New Type: Java.Sql.ResultSetMetaData</h3>

```
public abstract class ResultSetMetaData {
	
	public const int ColumnNoNulls = 0;
	public const int ColumnNullable = 1;
	public const int ColumnNullableUnknown = 2;
}
```

<h3 id='Java.Sql.ResultSetMetaDataConsts'>New Type: Java.Sql.ResultSetMetaDataConsts</h3>

```
[Obsolete]
public abstract class ResultSetMetaDataConsts : ResultSetMetaData {
}
```

<h3 id='Java.Sql.RowIdLifetime'>New Type: Java.Sql.RowIdLifetime</h3>

```
public sealed class RowIdLifetime : Java.Lang.Enum {
	
	public static RowIdLifetime ValueOf (string name);
	public static RowIdLifetime[] Values ();
	
	public static RowIdLifetime RowidUnsupported {
		get;
		set;
	}
	public static RowIdLifetime RowidValidForever {
		get;
		set;
	}
	public static RowIdLifetime RowidValidOther {
		get;
		set;
	}
	public static RowIdLifetime RowidValidSession {
		get;
		set;
	}
	public static RowIdLifetime RowidValidTransaction {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLClientInfoException'>New Type: Java.Sql.SQLClientInfoException</h3>

```
public class SQLClientInfoException : SQLException {
	
	protected SQLClientInfoException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLClientInfoException ();
	public SQLClientInfoException (string reason, string sqlState, int vendorCode, System.Collections.Generic.IDictionary failedProperties);
	public SQLClientInfoException (string reason, string sqlState, int vendorCode, System.Collections.Generic.IDictionary failedProperties, Java.Lang.Throwable cause);
	public SQLClientInfoException (string reason, string sqlState, System.Collections.Generic.IDictionary failedProperties);
	public SQLClientInfoException (string reason, string sqlState, System.Collections.Generic.IDictionary failedProperties, Java.Lang.Throwable cause);
	public SQLClientInfoException (string reason, System.Collections.Generic.IDictionary failedProperties);
	public SQLClientInfoException (string reason, System.Collections.Generic.IDictionary failedProperties, Java.Lang.Throwable cause);
	public SQLClientInfoException (System.Collections.Generic.IDictionary failedProperties);
	public SQLClientInfoException (System.Collections.Generic.IDictionary failedProperties, Java.Lang.Throwable cause);
	
	public virtual System.Collections.Generic.IDictionary FailedProperties {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLDataException'>New Type: Java.Sql.SQLDataException</h3>

```
public class SQLDataException : SQLNonTransientException {
	
	protected SQLDataException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLDataException ();
	public SQLDataException (string reason);
	public SQLDataException (string reason, string sqlState);
	public SQLDataException (string reason, string sqlState, int vendorCode);
	public SQLDataException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLDataException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLDataException (string reason, Java.Lang.Throwable cause);
	public SQLDataException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLException'>New Type: Java.Sql.SQLException</h3>

```
public class SQLException : Java.Lang.Exception, Java.Lang.IIterable {
	
	protected SQLException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLException ();
	public SQLException (string theReason);
	public SQLException (string theReason, string theSQLState);
	public SQLException (string theReason, string theSQLState, int theErrorCode);
	public SQLException (string p0, string p1, int p2, Java.Lang.Throwable p3);
	public SQLException (string p0, string p1, Java.Lang.Throwable p2);
	public SQLException (string p0, Java.Lang.Throwable p1);
	public SQLException (Java.Lang.Throwable p0);
	
	public virtual Java.Util.IIterator Iterator ();
	Java.Util.IIterator Java.Lang.IIterable.Iterator ();
	
	public virtual int ErrorCode {
		get;
	}
	public virtual SQLException NextException {
		get;
		set;
	}
	public virtual string SQLState {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLFeatureNotSupportedException'>New Type: Java.Sql.SQLFeatureNotSupportedException</h3>

```
public class SQLFeatureNotSupportedException : SQLNonTransientException {
	
	protected SQLFeatureNotSupportedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLFeatureNotSupportedException ();
	public SQLFeatureNotSupportedException (string reason);
	public SQLFeatureNotSupportedException (string reason, string sqlState);
	public SQLFeatureNotSupportedException (string reason, string sqlState, int vendorCode);
	public SQLFeatureNotSupportedException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLFeatureNotSupportedException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLFeatureNotSupportedException (string reason, Java.Lang.Throwable cause);
	public SQLFeatureNotSupportedException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLIntegrityConstraintViolationException'>New Type: Java.Sql.SQLIntegrityConstraintViolationException</h3>

```
public class SQLIntegrityConstraintViolationException : SQLNonTransientException {
	
	protected SQLIntegrityConstraintViolationException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLIntegrityConstraintViolationException ();
	public SQLIntegrityConstraintViolationException (string reason);
	public SQLIntegrityConstraintViolationException (string reason, string sqlState);
	public SQLIntegrityConstraintViolationException (string reason, string sqlState, int vendorCode);
	public SQLIntegrityConstraintViolationException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLIntegrityConstraintViolationException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLIntegrityConstraintViolationException (string reason, Java.Lang.Throwable cause);
	public SQLIntegrityConstraintViolationException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLInvalidAuthorizationSpecException'>New Type: Java.Sql.SQLInvalidAuthorizationSpecException</h3>

```
public class SQLInvalidAuthorizationSpecException : SQLNonTransientException {
	
	protected SQLInvalidAuthorizationSpecException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLInvalidAuthorizationSpecException ();
	public SQLInvalidAuthorizationSpecException (string reason);
	public SQLInvalidAuthorizationSpecException (string reason, string sqlState);
	public SQLInvalidAuthorizationSpecException (string reason, string sqlState, int vendorCode);
	public SQLInvalidAuthorizationSpecException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLInvalidAuthorizationSpecException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLInvalidAuthorizationSpecException (string reason, Java.Lang.Throwable cause);
	public SQLInvalidAuthorizationSpecException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLNonTransientConnectionException'>New Type: Java.Sql.SQLNonTransientConnectionException</h3>

```
public class SQLNonTransientConnectionException : SQLNonTransientException {
	
	protected SQLNonTransientConnectionException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLNonTransientConnectionException ();
	public SQLNonTransientConnectionException (string reason);
	public SQLNonTransientConnectionException (string reason, string sqlState);
	public SQLNonTransientConnectionException (string reason, string sqlState, int vendorCode);
	public SQLNonTransientConnectionException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLNonTransientConnectionException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLNonTransientConnectionException (string reason, Java.Lang.Throwable cause);
	public SQLNonTransientConnectionException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLNonTransientException'>New Type: Java.Sql.SQLNonTransientException</h3>

```
public class SQLNonTransientException : SQLException {
	
	protected SQLNonTransientException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLNonTransientException ();
	public SQLNonTransientException (string reason);
	public SQLNonTransientException (string reason, string sqlState);
	public SQLNonTransientException (string reason, string sqlState, int vendorCode);
	public SQLNonTransientException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLNonTransientException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLNonTransientException (string reason, Java.Lang.Throwable cause);
	public SQLNonTransientException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLPermission'>New Type: Java.Sql.SQLPermission</h3>

```
public sealed class SQLPermission : Java.Security.BasicPermission {
	
	public SQLPermission (string name);
	public SQLPermission (string name, string actions);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLRecoverableException'>New Type: Java.Sql.SQLRecoverableException</h3>

```
public class SQLRecoverableException : SQLException {
	
	protected SQLRecoverableException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLRecoverableException ();
	public SQLRecoverableException (string reason);
	public SQLRecoverableException (string reason, string sqlState);
	public SQLRecoverableException (string reason, string sqlState, int vendorCode);
	public SQLRecoverableException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLRecoverableException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLRecoverableException (string reason, Java.Lang.Throwable cause);
	public SQLRecoverableException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLSyntaxErrorException'>New Type: Java.Sql.SQLSyntaxErrorException</h3>

```
public class SQLSyntaxErrorException : SQLNonTransientException {
	
	protected SQLSyntaxErrorException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLSyntaxErrorException ();
	public SQLSyntaxErrorException (string reason);
	public SQLSyntaxErrorException (string reason, string sqlState);
	public SQLSyntaxErrorException (string reason, string sqlState, int vendorCode);
	public SQLSyntaxErrorException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLSyntaxErrorException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLSyntaxErrorException (string reason, Java.Lang.Throwable cause);
	public SQLSyntaxErrorException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLTimeoutException'>New Type: Java.Sql.SQLTimeoutException</h3>

```
public class SQLTimeoutException : SQLTransientException {
	
	protected SQLTimeoutException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLTimeoutException ();
	public SQLTimeoutException (string reason);
	public SQLTimeoutException (string reason, string sqlState);
	public SQLTimeoutException (string reason, string sqlState, int vendorCode);
	public SQLTimeoutException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLTimeoutException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLTimeoutException (string reason, Java.Lang.Throwable cause);
	public SQLTimeoutException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLTransactionRollbackException'>New Type: Java.Sql.SQLTransactionRollbackException</h3>

```
public class SQLTransactionRollbackException : SQLTransientException {
	
	protected SQLTransactionRollbackException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLTransactionRollbackException ();
	public SQLTransactionRollbackException (string reason);
	public SQLTransactionRollbackException (string reason, string sqlState);
	public SQLTransactionRollbackException (string reason, string sqlState, int vendorCode);
	public SQLTransactionRollbackException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLTransactionRollbackException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLTransactionRollbackException (string reason, Java.Lang.Throwable cause);
	public SQLTransactionRollbackException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLTransientConnectionException'>New Type: Java.Sql.SQLTransientConnectionException</h3>

```
public class SQLTransientConnectionException : SQLTransientException {
	
	protected SQLTransientConnectionException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLTransientConnectionException ();
	public SQLTransientConnectionException (string reason);
	public SQLTransientConnectionException (string reason, string sqlState);
	public SQLTransientConnectionException (string reason, string sqlState, int vendorCode);
	public SQLTransientConnectionException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLTransientConnectionException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLTransientConnectionException (string reason, Java.Lang.Throwable cause);
	public SQLTransientConnectionException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLTransientException'>New Type: Java.Sql.SQLTransientException</h3>

```
public class SQLTransientException : SQLException {
	
	protected SQLTransientException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLTransientException ();
	public SQLTransientException (string reason);
	public SQLTransientException (string reason, string sqlState);
	public SQLTransientException (string reason, string sqlState, int vendorCode);
	public SQLTransientException (string reason, string sqlState, int vendorCode, Java.Lang.Throwable cause);
	public SQLTransientException (string reason, string sqlState, Java.Lang.Throwable cause);
	public SQLTransientException (string reason, Java.Lang.Throwable cause);
	public SQLTransientException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.SQLWarning'>New Type: Java.Sql.SQLWarning</h3>

```
public class SQLWarning : SQLException {
	
	protected SQLWarning (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SQLWarning ();
	public SQLWarning (string theReason);
	public SQLWarning (string theReason, string theSQLState);
	public SQLWarning (string theReason, string theSQLState, int theErrorCode);
	public SQLWarning (string p0, string p1, int p2, Java.Lang.Throwable p3);
	public SQLWarning (string p0, string p1, Java.Lang.Throwable p2);
	public SQLWarning (string p0, Java.Lang.Throwable p1);
	public SQLWarning (Java.Lang.Throwable p0);
	
	public virtual SQLWarning NextWarning {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.Statement'>New Type: Java.Sql.Statement</h3>

```
public abstract class Statement {
	
	public const int CloseAllResults = 3;
	public const int CloseCurrentResult = 1;
	public const int ExecuteFailed = -3;
	public const int KeepCurrentResult = 2;
	public const int NoGeneratedKeys = 2;
	public const int ReturnGeneratedKeys = 1;
	public const int SuccessNoInfo = -2;
}
```

<h3 id='Java.Sql.StatementConsts'>New Type: Java.Sql.StatementConsts</h3>

```
[Obsolete]
public abstract class StatementConsts : Statement {
}
```

<h3 id='Java.Sql.Time'>New Type: Java.Sql.Time</h3>

```
public class Time : Java.Util.Date {
	
	protected Time (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Time (int theHour, int theMinute, int theSecond);
	public Time (long theTime);
	
	public static Time ValueOf (string timeString);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.Timestamp'>New Type: Java.Sql.Timestamp</h3>

```
public class Timestamp : Java.Util.Date {
	
	protected Timestamp (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Timestamp (int theYear, int theMonth, int theDate, int theHour, int theMinute, int theSecond, int theNano);
	public Timestamp (long theTime);
	
	public static Timestamp ValueOf (string s);
	public virtual bool After (Timestamp theTimestamp);
	public virtual bool Before (Timestamp theTimestamp);
	public virtual int CompareTo (Timestamp theTimestamp);
	public virtual bool Equals (Timestamp theTimestamp);
	
	public virtual int Nanos {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Sql.Types'>New Type: Java.Sql.Types</h3>

```
public class Types : Java.Lang.Object {
	
	protected Types (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static int Longnvarchar {
		get;
		set;
	}
	public static int Nchar {
		get;
		set;
	}
	public static int Nclob {
		get;
		set;
	}
	public static int Nvarchar {
		get;
		set;
	}
	public static int Rowid {
		get;
		set;
	}
	public static int Sqlxml {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int Array = 2003;
	public const int Bigint = -5;
	public const int Binary = -2;
	public const int Bit = -7;
	public const int Blob = 2004;
	public const int Boolean = 16;
	public const int Char = 1;
	public const int Clob = 2005;
	public const int Datalink = 70;
	public const int Date = 91;
	public const int Decimal = 3;
	public const int Distinct = 2001;
	public const int Double = 8;
	public const int Float = 6;
	public const int Integer = 4;
	public const int JavaObject = 2000;
	public const int Longvarbinary = -4;
	public const int Longvarchar = -1;
	public const int Null = 0;
	public const int Numeric = 2;
	public const int Other = 1111;
	public const int Real = 7;
	public const int Ref = 2006;
	public const int Smallint = 5;
	public const int Struct = 2002;
	public const int Time = 92;
	public const int Timestamp = 93;
	public const int Tinyint = -6;
	public const int Varbinary = -3;
	public const int Varchar = 12;
}
```

<h2 id='Java.Text'>Namespace: Java.Text</h2>

<h3 id='Java.Text.Annotation'>New Type: Java.Text.Annotation</h3>

```
public class Annotation : Java.Lang.Object {
	
	protected Annotation (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Annotation (Java.Lang.Object attribute);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual Java.Lang.Object Value {
		get;
	}
}
```

<h3 id='Java.Text.AttributedCharacterIteratorAttribute'>New Type: Java.Text.AttributedCharacterIteratorAttribute</h3>

```
public class AttributedCharacterIteratorAttribute : Java.Lang.Object, Java.IO.ISerializable {
	
	protected AttributedCharacterIteratorAttribute (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AttributedCharacterIteratorAttribute (string name);
	
	public bool Equals (Java.Lang.Object object);
	public int GetHashCode ();
	protected virtual Java.Lang.Object ReadResolve ();
	
	public static AttributedCharacterIteratorAttribute InputMethodSegment {
		get;
		set;
	}
	public static AttributedCharacterIteratorAttribute Language {
		get;
		set;
	}
	public static AttributedCharacterIteratorAttribute Reading {
		get;
		set;
	}
	protected virtual string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.AttributedString'>New Type: Java.Text.AttributedString</h3>

```
public class AttributedString : Java.Lang.Object {
	
	protected AttributedString (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AttributedString (string value);
	public AttributedString (string value, System.Collections.Generic.IDictionary attributes);
	public AttributedString (IAttributedCharacterIterator iterator);
	public AttributedString (IAttributedCharacterIterator iterator, int start, int end);
	public AttributedString (IAttributedCharacterIterator iterator, int start, int end, AttributedCharacterIteratorAttribute[] attributes);
	
	public virtual void AddAttribute (AttributedCharacterIteratorAttribute attribute, Java.Lang.Object value);
	public virtual void AddAttribute (AttributedCharacterIteratorAttribute attribute, Java.Lang.Object value, int start, int end);
	public virtual void AddAttributes (System.Collections.Generic.IDictionary attributes, int start, int end);
	public virtual IAttributedCharacterIterator GetIterator (AttributedCharacterIteratorAttribute[] attributes);
	public virtual IAttributedCharacterIterator GetIterator (AttributedCharacterIteratorAttribute[] attributes, int start, int end);
	
	public virtual IAttributedCharacterIterator Iterator {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.Bidi'>New Type: Java.Text.Bidi</h3>

```
public sealed class Bidi : Java.Lang.Object {
	
	public Bidi (char [] text, int textStart, byte [] embeddings, int embStart, int paragraphLength, int flags);
	public Bidi (string paragraph, int flags);
	public Bidi (IAttributedCharacterIterator paragraph);
	
	public static void ReorderVisually (byte [] levels, int levelStart, Java.Lang.Object[] objects, int objectStart, int count);
	public static bool RequiresBidi (char [] text, int start, int limit);
	public bool BaseIsLeftToRight ();
	public Bidi CreateLineBidi (int lineStart, int lineLimit);
	public int GetLevelAt (int offset);
	public int GetRunLevel (int run);
	public int GetRunLimit (int run);
	public int GetRunStart (int run);
	
	public int BaseLevel {
		get;
	}
	public bool IsLeftToRight {
		get;
	}
	public bool IsMixed {
		get;
	}
	public bool IsRightToLeft {
		get;
	}
	public int Length {
		get;
	}
	public int RunCount {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int DirectionDefaultLeftToRight = -2;
	public const int DirectionDefaultRightToLeft = -1;
	public const int DirectionLeftToRight = 0;
	public const int DirectionRightToLeft = 1;
}
```

<h3 id='Java.Text.BreakIterator'>New Type: Java.Text.BreakIterator</h3>

```
public abstract class BreakIterator : Java.Lang.Object, Java.Lang.ICloneable {
	
	protected BreakIterator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected BreakIterator ();
	
	public static Java.Util.Locale[] GetAvailableLocales ();
	public static BreakIterator GetCharacterInstance (Java.Util.Locale where);
	public static BreakIterator GetLineInstance (Java.Util.Locale where);
	public static BreakIterator GetSentenceInstance (Java.Util.Locale where);
	public static BreakIterator GetWordInstance (Java.Util.Locale where);
	public virtual Java.Lang.Object Clone ();
	public abstract int Current ();
	public abstract int First ();
	public abstract int Following (int offset);
	public virtual bool IsBoundary (int offset);
	public abstract int Last ();
	public abstract int Next ();
	public abstract int Next (int n);
	public virtual int Preceding (int offset);
	public abstract int Previous ();
	public virtual void SetText (string newText);
	
	public static BreakIterator CharacterInstance {
		get;
	}
	public static BreakIterator LineInstance {
		get;
	}
	public static BreakIterator SentenceInstance {
		get;
	}
	public static BreakIterator WordInstance {
		get;
	}
	public abstract ICharacterIterator Text {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int Done = -1;
}
```

<h3 id='Java.Text.CharacterIterator'>New Type: Java.Text.CharacterIterator</h3>

```
public abstract class CharacterIterator {
	
	public const char Done = '￿';
}
```

<h3 id='Java.Text.CharacterIteratorConsts'>New Type: Java.Text.CharacterIteratorConsts</h3>

```
[Obsolete]
public abstract class CharacterIteratorConsts : CharacterIterator {
}
```

<h3 id='Java.Text.ChoiceFormat'>New Type: Java.Text.ChoiceFormat</h3>

```
public class ChoiceFormat : NumberFormat {
	
	protected ChoiceFormat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ChoiceFormat (double [] limits, string [] formats);
	public ChoiceFormat (string template);
	
	public static double NextDouble (double value);
	public static double NextDouble (double value, bool increment);
	public static double PreviousDouble (double value);
	public virtual void ApplyPattern (string template);
	public override Java.Lang.StringBuffer Format (double value, Java.Lang.StringBuffer buffer, FieldPosition field);
	public override Java.Lang.StringBuffer Format (long value, Java.Lang.StringBuffer buffer, FieldPosition field);
	public virtual Java.Lang.Object[] GetFormats ();
	public virtual double [] GetLimits ();
	public override Java.Lang.Number Parse (string string, ParsePosition position);
	public virtual void SetChoices (double [] limits, string [] formats);
	public virtual string ToPattern ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.CollationElementIterator'>New Type: Java.Text.CollationElementIterator</h3>

```
public sealed class CollationElementIterator : Java.Lang.Object {
	
	public static int PrimaryOrder (int order);
	public static short SecondaryOrder (int order);
	public static short TertiaryOrder (int order);
	public int GetMaxExpansion (int order);
	public int Next ();
	public int Previous ();
	public void Reset ();
	public void SetText (ICharacterIterator source);
	public void SetText (string source);
	
	public int Offset {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int Nullorder = -1;
}
```

<h3 id='Java.Text.CollationKey'>New Type: Java.Text.CollationKey</h3>

```
public abstract class CollationKey : Java.Lang.Object, Java.Lang.IComparable {
	
	protected CollationKey (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected CollationKey (string p0);
	
	public abstract int CompareTo (CollationKey value);
	int Java.Lang.IComparable.CompareTo (Java.Lang.Object another);
	public abstract byte [] ToByteArray ();
	
	public virtual string SourceString {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.Collator'>New Type: Java.Text.Collator</h3>

```
public abstract class Collator : Java.Lang.Object, Java.Lang.ICloneable, Java.Util.IComparator {
	
	protected Collator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Collator ();
	
	public static Java.Util.Locale[] GetAvailableLocales ();
	public static Collator GetInstance (Java.Util.Locale locale);
	public virtual Java.Lang.Object Clone ();
	public virtual int Compare (Java.Lang.Object object1, Java.Lang.Object object2);
	public abstract int Compare (string string1, string string2);
	public virtual bool Equals (string string1, string string2);
	public abstract CollationKey GetCollationKey (string string);
	public abstract int GetHashCode ();
	int Java.Util.IComparator.Compare (Java.Lang.Object object1, Java.Lang.Object object2);
	
	public static Collator Instance {
		get;
	}
	public virtual int Decomposition {
		get;
		set;
	}
	public virtual int Strength {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int CanonicalDecomposition = 1;
	public const int FullDecomposition = 2;
	public const int Identical = 3;
	public const int NoDecomposition = 0;
	public const int Primary = 0;
	public const int Secondary = 1;
	public const int Tertiary = 2;
}
```

<h3 id='Java.Text.DateFormat'>New Type: Java.Text.DateFormat</h3>

```
public abstract class DateFormat : _Format {
	
	protected DateFormat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected DateFormat ();
	
	public static Java.Util.Locale[] GetAvailableLocales ();
	public static DateFormat GetDateInstance (int style);
	public static DateFormat GetDateInstance (int style, Java.Util.Locale locale);
	public static DateFormat GetDateTimeInstance (int dateStyle, int timeStyle);
	public static DateFormat GetDateTimeInstance (int dateStyle, int timeStyle, Java.Util.Locale locale);
	public static DateFormat GetTimeInstance (int style);
	public static DateFormat GetTimeInstance (int style, Java.Util.Locale locale);
	public string Format (Java.Util.Date date);
	public abstract Java.Lang.StringBuffer Format (Java.Util.Date date, Java.Lang.StringBuffer buffer, FieldPosition field);
	public Java.Lang.StringBuffer Format (Java.Lang.Object object, Java.Lang.StringBuffer buffer, FieldPosition field);
	public virtual Java.Util.Date Parse (string string);
	public abstract Java.Util.Date Parse (string string, ParsePosition position);
	public override Java.Lang.Object ParseObject (string string, ParsePosition position);
	
	public static DateFormat DateInstance {
		get;
	}
	public static DateFormat DateTimeInstance {
		get;
	}
	public static DateFormat Instance {
		get;
	}
	public static DateFormat TimeInstance {
		get;
	}
	public virtual Java.Util.Calendar Calendar {
		get;
		set;
	}
	public virtual bool Lenient {
		get;
		set;
	}
	public virtual NumberFormat NumberFormat {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual Java.Util.TimeZone TimeZone {
		get;
		set;
	}
	
	public const int AmPmField = 14;
	public const int DateField = 3;
	public const int DayOfWeekField = 9;
	public const int DayOfWeekInMonthField = 11;
	public const int DayOfYearField = 10;
	public const int Default = 2;
	public const int EraField = 0;
	public const int Full = 0;
	public const int HourOfDay0Field = 5;
	public const int HourOfDay1Field = 4;
	public const int Hour0Field = 16;
	public const int Hour1Field = 15;
	public const int Long = 1;
	public const int Medium = 2;
	public const int MillisecondField = 8;
	public const int MinuteField = 6;
	public const int MonthField = 2;
	public const int SecondField = 7;
	public const int Short = 3;
	public const int TimezoneField = 17;
	public const int WeekOfMonthField = 13;
	public const int WeekOfYearField = 12;
	public const int YearField = 1;
	
	public class Field : Field {
		
		protected Field (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		protected Field (string fieldName, int calendarField);
		
		public static Field OfCalendarField (int calendarField);
		
		public static Field AmPm {
			get;
			set;
		}
		public static Field DayOfMonth {
			get;
			set;
		}
		public static Field DayOfWeek {
			get;
			set;
		}
		public static Field DayOfWeekInMonth {
			get;
			set;
		}
		public static Field DayOfYear {
			get;
			set;
		}
		public static Field Era {
			get;
			set;
		}
		public static Field Hour0 {
			get;
			set;
		}
		public static Field Hour1 {
			get;
			set;
		}
		public static Field HourOfDay0 {
			get;
			set;
		}
		public static Field HourOfDay1 {
			get;
			set;
		}
		public static Field Millisecond {
			get;
			set;
		}
		public static Field Minute {
			get;
			set;
		}
		public static Field Month {
			get;
			set;
		}
		public static Field Second {
			get;
			set;
		}
		public static Field TimeZone {
			get;
			set;
		}
		public static Field WeekOfMonth {
			get;
			set;
		}
		public static Field WeekOfYear {
			get;
			set;
		}
		public static Field Year {
			get;
			set;
		}
		public virtual int CalendarField {
			get;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Java.Text.DateFormatSymbols'>New Type: Java.Text.DateFormatSymbols</h3>

```
public class DateFormatSymbols : Java.Lang.Object, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected DateFormatSymbols (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DateFormatSymbols ();
	public DateFormatSymbols (Java.Util.Locale locale);
	
	public static Java.Util.Locale[] GetAvailableLocales ();
	public static DateFormatSymbols GetInstance (Java.Util.Locale p0);
	public virtual Java.Lang.Object Clone ();
	public virtual string [] GetAmPmStrings ();
	public virtual string [] GetEras ();
	public virtual string [] GetMonths ();
	public virtual string [] GetShortMonths ();
	public virtual string [] GetShortWeekdays ();
	public virtual string [] GetWeekdays ();
	public virtual string [] [] GetZoneStrings ();
	public virtual void SetAmPmStrings (string [] data);
	public virtual void SetEras (string [] data);
	public virtual void SetMonths (string [] data);
	public virtual void SetShortMonths (string [] data);
	public virtual void SetShortWeekdays (string [] data);
	public virtual void SetWeekdays (string [] data);
	public virtual void SetZoneStrings (string [] [] data);
	
	public static DateFormatSymbols Instance {
		get;
	}
	public virtual string LocalPatternChars {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.DecimalFormat'>New Type: Java.Text.DecimalFormat</h3>

```
public class DecimalFormat : NumberFormat {
	
	protected DecimalFormat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DecimalFormat ();
	public DecimalFormat (string pattern);
	public DecimalFormat (string pattern, DecimalFormatSymbols value);
	
	public virtual void ApplyLocalizedPattern (string pattern);
	public virtual void ApplyPattern (string pattern);
	public override Java.Lang.StringBuffer Format (double value, Java.Lang.StringBuffer buffer, FieldPosition position);
	public override Java.Lang.StringBuffer Format (long value, Java.Lang.StringBuffer buffer, FieldPosition position);
	public Java.Lang.StringBuffer Format (Java.Lang.Object number, Java.Lang.StringBuffer toAppendTo, FieldPosition pos);
	public override Java.Lang.Number Parse (string string, ParsePosition position);
	public virtual string ToLocalizedPattern ();
	public virtual string ToPattern ();
	
	public virtual DecimalFormatSymbols DecimalFormatSymbols {
		get;
		set;
	}
	public virtual bool DecimalSeparatorAlwaysShown {
		get;
		set;
	}
	public virtual int GroupingSize {
		get;
		set;
	}
	public virtual int Multiplier {
		get;
		set;
	}
	public virtual string NegativePrefix {
		get;
		set;
	}
	public virtual string NegativeSuffix {
		get;
		set;
	}
	public virtual bool ParseBigDecimal {
		get;
		set;
	}
	public virtual string PositivePrefix {
		get;
		set;
	}
	public virtual string PositiveSuffix {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.DecimalFormatSymbols'>New Type: Java.Text.DecimalFormatSymbols</h3>

```
public class DecimalFormatSymbols : Java.Lang.Object, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected DecimalFormatSymbols (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DecimalFormatSymbols ();
	public DecimalFormatSymbols (Java.Util.Locale locale);
	
	public static Java.Util.Locale[] GetAvailableLocales ();
	public static DecimalFormatSymbols GetInstance (Java.Util.Locale p0);
	public virtual Java.Lang.Object Clone ();
	
	public static DecimalFormatSymbols Instance {
		get;
	}
	public virtual Java.Util.Currency Currency {
		get;
		set;
	}
	public virtual string CurrencySymbol {
		get;
		set;
	}
	public virtual char DecimalSeparator {
		get;
		set;
	}
	public virtual char Digit {
		get;
		set;
	}
	public virtual string ExponentSeparator {
		get;
		set;
	}
	public virtual char GroupingSeparator {
		get;
		set;
	}
	public virtual string Infinity {
		get;
		set;
	}
	public virtual string InternationalCurrencySymbol {
		get;
		set;
	}
	public virtual char MinusSign {
		get;
		set;
	}
	public virtual char MonetaryDecimalSeparator {
		get;
		set;
	}
	public virtual string NaN {
		get;
		set;
	}
	public virtual char PatternSeparator {
		get;
		set;
	}
	public virtual char Percent {
		get;
		set;
	}
	public virtual char PerMill {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual char ZeroDigit {
		get;
		set;
	}
}
```

<h3 id='Java.Text.FieldPosition'>New Type: Java.Text.FieldPosition</h3>

```
public class FieldPosition : Java.Lang.Object {
	
	protected FieldPosition (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FieldPosition (int field);
	public FieldPosition (Field attribute);
	public FieldPosition (Field attribute, int field);
	
	public virtual int BeginIndex {
		get;
		set;
	}
	public virtual int EndIndex {
		get;
		set;
	}
	public virtual int Field {
		get;
	}
	public virtual Field FieldAttribute {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.IAttributedCharacterIterator'>New Type: Java.Text.IAttributedCharacterIterator</h3>

```
public interface IAttributedCharacterIterator : ICharacterIterator, Java.Lang.ICloneable, IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object GetAttribute (AttributedCharacterIteratorAttribute attribute);
	int GetRunLimit (AttributedCharacterIteratorAttribute attribute);
	int GetRunLimit (System.Collections.Generic.ICollection attributes);
	int GetRunStart (AttributedCharacterIteratorAttribute attribute);
	int GetRunStart (System.Collections.Generic.ICollection attributes);
	
	System.Collections.Generic.ICollection AllAttributeKeys {
		get;
	}
	System.Collections.Generic.IDictionary Attributes {
		get;
	}
	int RunLimit {
		get;
	}
	int RunStart {
		get;
	}
}
```

<h3 id='Java.Text.ICharacterIterator'>New Type: Java.Text.ICharacterIterator</h3>

```
public interface ICharacterIterator : Java.Lang.ICloneable, IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object Clone ();
	char Current ();
	char First ();
	char Last ();
	char Next ();
	char Previous ();
	char SetIndex (int location);
	
	int BeginIndex {
		get;
	}
	int EndIndex {
		get;
	}
	int Index {
		get;
	}
}
```

<h3 id='Java.Text.MessageFormat'>New Type: Java.Text.MessageFormat</h3>

```
public class MessageFormat : _Format {
	
	protected MessageFormat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MessageFormat (string template);
	public MessageFormat (string template, Java.Util.Locale locale);
	
	public static string Format (string template, params Java.Lang.Object[] objects);
	public virtual void ApplyPattern (string template);
	public Java.Lang.StringBuffer Format (Java.Lang.Object object, Java.Lang.StringBuffer buffer, FieldPosition field);
	public Java.Lang.StringBuffer Format (Java.Lang.Object[] objects, Java.Lang.StringBuffer buffer, FieldPosition field);
	public virtual _Format[] GetFormats ();
	public virtual _Format[] GetFormatsByArgumentIndex ();
	public virtual Java.Lang.Object[] Parse (string string);
	public virtual Java.Lang.Object[] Parse (string string, ParsePosition position);
	public override Java.Lang.Object ParseObject (string string, ParsePosition position);
	public virtual void SetFormat (int offset, _Format format);
	public virtual void SetFormatByArgumentIndex (int argIndex, _Format format);
	public virtual void SetFormats (_Format[] formats);
	public virtual void SetFormatsByArgumentIndex (_Format[] formats);
	public virtual string ToPattern ();
	
	public virtual Java.Util.Locale Locale {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class Field : Field {
		
		protected Field (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		protected Field (string fieldName);
		
		public static Field Argument {
			get;
			set;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Java.Text.Normalizer'>New Type: Java.Text.Normalizer</h3>

```
public sealed class Normalizer : Java.Lang.Object {
	
	public static bool IsNormalized (Java.Lang.ICharSequence src, Form form);
	public static bool IsNormalized (string src, Form form);
	public static string Normalize (Java.Lang.ICharSequence src, Form form);
	public static string Normalize (string src, Form form);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public sealed class Form : Java.Lang.Enum {
		
		public static Form ValueOf (string name);
		public static Form[] Values ();
		
		public static Form Nfc {
			get;
			set;
		}
		public static Form Nfd {
			get;
			set;
		}
		public static Form Nfkc {
			get;
			set;
		}
		public static Form Nfkd {
			get;
			set;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Java.Text.NumberFormat'>New Type: Java.Text.NumberFormat</h3>

```
public abstract class NumberFormat : _Format {
	
	protected NumberFormat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected NumberFormat ();
	
	public static Java.Util.Locale[] GetAvailableLocales ();
	public static NumberFormat GetCurrencyInstance (Java.Util.Locale locale);
	public static NumberFormat GetInstance (Java.Util.Locale locale);
	public static NumberFormat GetIntegerInstance (Java.Util.Locale locale);
	public static NumberFormat GetNumberInstance (Java.Util.Locale locale);
	public static NumberFormat GetPercentInstance (Java.Util.Locale locale);
	public string Format (double value);
	public abstract Java.Lang.StringBuffer Format (double value, Java.Lang.StringBuffer buffer, FieldPosition field);
	public string Format (long value);
	public abstract Java.Lang.StringBuffer Format (long value, Java.Lang.StringBuffer buffer, FieldPosition field);
	public override Java.Lang.StringBuffer Format (Java.Lang.Object object, Java.Lang.StringBuffer buffer, FieldPosition field);
	public virtual Java.Lang.Number Parse (string string);
	public abstract Java.Lang.Number Parse (string string, ParsePosition position);
	public Java.Lang.Object ParseObject (string string, ParsePosition position);
	
	public static NumberFormat CurrencyInstance {
		get;
	}
	public static NumberFormat Instance {
		get;
	}
	public static NumberFormat IntegerInstance {
		get;
	}
	public static NumberFormat NumberInstance {
		get;
	}
	public static NumberFormat PercentInstance {
		get;
	}
	public virtual Java.Util.Currency Currency {
		get;
		set;
	}
	public virtual bool GroupingUsed {
		get;
		set;
	}
	public virtual int MaximumFractionDigits {
		get;
		set;
	}
	public virtual int MaximumIntegerDigits {
		get;
		set;
	}
	public virtual int MinimumFractionDigits {
		get;
		set;
	}
	public virtual int MinimumIntegerDigits {
		get;
		set;
	}
	public virtual bool ParseIntegerOnly {
		get;
		set;
	}
	public virtual Java.Math.RoundingMode RoundingMode {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int FractionField = 1;
	public const int IntegerField = 0;
	
	public class Field : Field {
		
		protected Field (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		protected Field (string fieldName);
		
		public static Field Currency {
			get;
			set;
		}
		public static Field DecimalSeparator {
			get;
			set;
		}
		public static Field Exponent {
			get;
			set;
		}
		public static Field ExponentSign {
			get;
			set;
		}
		public static Field ExponentSymbol {
			get;
			set;
		}
		public static Field Fraction {
			get;
			set;
		}
		public static Field GroupingSeparator {
			get;
			set;
		}
		public static Field Integer {
			get;
			set;
		}
		public static Field Percent {
			get;
			set;
		}
		public static Field Permille {
			get;
			set;
		}
		public static Field Sign {
			get;
			set;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Java.Text.ParseException'>New Type: Java.Text.ParseException</h3>

```
public class ParseException : Java.Lang.Exception {
	
	protected ParseException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ParseException (string detailMessage, int location);
	
	public virtual int ErrorOffset {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.ParsePosition'>New Type: Java.Text.ParsePosition</h3>

```
public class ParsePosition : Java.Lang.Object {
	
	protected ParsePosition (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ParsePosition (int index);
	
	public virtual int ErrorIndex {
		get;
		set;
	}
	public virtual int Index {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.RuleBasedCollator'>New Type: Java.Text.RuleBasedCollator</h3>

```
public class RuleBasedCollator : Collator {
	
	protected RuleBasedCollator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RuleBasedCollator (string rules);
	
	public override int Compare (string source, string target);
	public virtual CollationElementIterator GetCollationElementIterator (ICharacterIterator source);
	public virtual CollationElementIterator GetCollationElementIterator (string source);
	public override CollationKey GetCollationKey (string source);
	public override int GetHashCode ();
	
	public virtual string Rules {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.SimpleDateFormat'>New Type: Java.Text.SimpleDateFormat</h3>

```
public class SimpleDateFormat : DateFormat {
	
	protected SimpleDateFormat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SimpleDateFormat ();
	public SimpleDateFormat (string pattern);
	public SimpleDateFormat (string template, DateFormatSymbols value);
	public SimpleDateFormat (string template, Java.Util.Locale locale);
	
	public virtual void ApplyLocalizedPattern (string template);
	public virtual void ApplyPattern (string template);
	public override Java.Lang.StringBuffer Format (Java.Util.Date date, Java.Lang.StringBuffer buffer, FieldPosition fieldPos);
	public virtual Java.Util.Date Get2DigitYearStart ();
	public override Java.Util.Date Parse (string string, ParsePosition position);
	public virtual void Set2DigitYearStart (Java.Util.Date date);
	public virtual string ToLocalizedPattern ();
	public virtual string ToPattern ();
	
	public virtual DateFormatSymbols DateFormatSymbols {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Text.StringCharacterIterator'>New Type: Java.Text.StringCharacterIterator</h3>

```
public sealed class StringCharacterIterator : Java.Lang.Object, ICharacterIterator, Java.Lang.ICloneable {
	
	public StringCharacterIterator (string value);
	public StringCharacterIterator (string value, int location);
	public StringCharacterIterator (string value, int start, int end, int location);
	
	public Java.Lang.Object Clone ();
	public char Current ();
	public char First ();
	public char Last ();
	public char Next ();
	public char Previous ();
	public char SetIndex (int location);
	public void SetText (string value);
	
	public int BeginIndex {
		get;
	}
	public int EndIndex {
		get;
	}
	public int Index {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const char Done = '￿';
	}
}
```

<h3 id='Java.Text._Format'>New Type: Java.Text._Format</h3>

```
public abstract class _Format : Java.Lang.Object, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected _Format (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected _Format ();
	
	public virtual Java.Lang.Object Clone ();
	public string Format (Java.Lang.Object object);
	public abstract Java.Lang.StringBuffer Format (Java.Lang.Object object, Java.Lang.StringBuffer buffer, FieldPosition field);
	public virtual IAttributedCharacterIterator FormatToCharacterIterator (Java.Lang.Object object);
	public virtual Java.Lang.Object ParseObject (string string);
	public abstract Java.Lang.Object ParseObject (string string, ParsePosition position);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class Field : AttributedCharacterIteratorAttribute {
		
		protected Field (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		protected Field (string fieldName);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h2 id='Java.Util'>Namespace: Java.Util</h2>

<h3 id='Java.Util.AbstractCollection'>New Type: Java.Util.AbstractCollection</h3>

```
public abstract class AbstractCollection : Java.Lang.Object, ICollection, Java.Lang.IIterable {
	
	protected AbstractCollection (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractCollection ();
	
	public virtual bool Add (Java.Lang.Object object);
	public virtual bool AddAll (System.Collections.ICollection collection);
	public virtual void Clear ();
	public virtual bool Contains (Java.Lang.Object object);
	public virtual bool ContainsAll (System.Collections.ICollection collection);
	public abstract IIterator Iterator ();
	public virtual bool Remove (Java.Lang.Object object);
	public virtual bool RemoveAll (System.Collections.ICollection collection);
	public virtual bool RetainAll (System.Collections.ICollection collection);
	public abstract int Size ();
	public virtual Java.Lang.Object[] ToArray ();
	public virtual Java.Lang.Object[] ToArray (Java.Lang.Object[] contents);
	
	public virtual bool IsEmpty {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.AbstractList'>New Type: Java.Util.AbstractList</h3>

```
public abstract class AbstractList : AbstractCollection, IList {
	
	protected AbstractList (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractList ();
	
	public virtual void Add (int location, Java.Lang.Object object);
	public virtual bool AddAll (int location, System.Collections.ICollection collection);
	public abstract Java.Lang.Object Get (int location);
	public virtual int IndexOf (Java.Lang.Object object);
	public override IIterator Iterator ();
	public virtual int LastIndexOf (Java.Lang.Object object);
	public virtual IListIterator ListIterator ();
	public virtual IListIterator ListIterator (int location);
	public virtual Java.Lang.Object Remove (int location);
	protected virtual void RemoveRange (int start, int end);
	public virtual Java.Lang.Object Set (int location, Java.Lang.Object object);
	public virtual System.Collections.IList SubList (int start, int end);
	
	protected int ModCount {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.AbstractMap'>New Type: Java.Util.AbstractMap</h3>

```
public abstract class AbstractMap : Java.Lang.Object, IMap {
	
	protected AbstractMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractMap ();
	
	public virtual void Clear ();
	public virtual bool ContainsKey (Java.Lang.Object key);
	public virtual bool ContainsValue (Java.Lang.Object value);
	public abstract System.Collections.ICollection EntrySet ();
	public virtual Java.Lang.Object Get (Java.Lang.Object key);
	public virtual System.Collections.ICollection KeySet ();
	public virtual Java.Lang.Object Put (Java.Lang.Object key, Java.Lang.Object value);
	public virtual void PutAll (System.Collections.IDictionary map);
	public virtual Java.Lang.Object Remove (Java.Lang.Object key);
	public virtual int Size ();
	public virtual System.Collections.ICollection Values ();
	
	public virtual bool IsEmpty {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class SimpleEntry : Java.Lang.Object, IMapEntry, Java.IO.ISerializable {
		
		protected SimpleEntry (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public SimpleEntry (IMapEntry copyFrom);
		public SimpleEntry (Java.Lang.Object theKey, Java.Lang.Object theValue);
		
		public virtual Java.Lang.Object SetValue (Java.Lang.Object object);
		
		public virtual Java.Lang.Object Key {
			get;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
		public virtual Java.Lang.Object Value {
			get;
		}
	}
	public class SimpleImmutableEntry : Java.Lang.Object, IMapEntry, Java.IO.ISerializable {
		
		protected SimpleImmutableEntry (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public SimpleImmutableEntry (IMapEntry copyFrom);
		public SimpleImmutableEntry (Java.Lang.Object theKey, Java.Lang.Object theValue);
		
		public virtual Java.Lang.Object SetValue (Java.Lang.Object object);
		
		public virtual Java.Lang.Object Key {
			get;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
		public virtual Java.Lang.Object Value {
			get;
		}
	}
}
```

<h3 id='Java.Util.AbstractQueue'>New Type: Java.Util.AbstractQueue</h3>

```
public abstract class AbstractQueue : AbstractCollection, IQueue {
	
	protected AbstractQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractQueue ();
	
	public virtual Java.Lang.Object Element ();
	public abstract bool Offer (Java.Lang.Object o);
	public abstract Java.Lang.Object Peek ();
	public abstract Java.Lang.Object Poll ();
	public virtual Java.Lang.Object Remove ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.AbstractSequentialList'>New Type: Java.Util.AbstractSequentialList</h3>

```
public abstract class AbstractSequentialList : AbstractList {
	
	protected AbstractSequentialList (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractSequentialList ();
	
	public override Java.Lang.Object Get (int location);
	public abstract IListIterator ListIterator (int location);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.AbstractSet'>New Type: Java.Util.AbstractSet</h3>

```
public abstract class AbstractSet : AbstractCollection, ISet {
	
	protected AbstractSet (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractSet ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.ArrayDeque'>New Type: Java.Util.ArrayDeque</h3>

```
public class ArrayDeque : AbstractCollection, Java.Lang.ICloneable, IDeque, IQueue, Java.IO.ISerializable {
	
	protected ArrayDeque (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ArrayDeque ();
	public ArrayDeque (int minSize);
	public ArrayDeque (System.Collections.ICollection c);
	
	public virtual void AddFirst (Java.Lang.Object e);
	public virtual void AddLast (Java.Lang.Object e);
	public virtual ArrayDeque Clone ();
	public virtual IIterator DescendingIterator ();
	public virtual Java.Lang.Object Element ();
	public override IIterator Iterator ();
	public virtual bool Offer (Java.Lang.Object e);
	public virtual bool OfferFirst (Java.Lang.Object e);
	public virtual bool OfferLast (Java.Lang.Object e);
	public virtual Java.Lang.Object Peek ();
	public virtual Java.Lang.Object PeekFirst ();
	public virtual Java.Lang.Object PeekLast ();
	public virtual Java.Lang.Object Poll ();
	public virtual Java.Lang.Object PollFirst ();
	public virtual Java.Lang.Object PollLast ();
	public virtual Java.Lang.Object Pop ();
	public virtual void Push (Java.Lang.Object e);
	public virtual Java.Lang.Object Remove ();
	public virtual Java.Lang.Object RemoveFirst ();
	public virtual bool RemoveFirstOccurrence (Java.Lang.Object obj);
	public virtual Java.Lang.Object RemoveLast ();
	public virtual bool RemoveLastOccurrence (Java.Lang.Object obj);
	public override int Size ();
	
	public virtual Java.Lang.Object First {
		get;
	}
	public virtual Java.Lang.Object Last {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.ArrayList'>New Type: Java.Util.ArrayList</h3>

```
public class ArrayList : AbstractList, Java.Lang.ICloneable, IRandomAccess, Java.IO.ISerializable {
	
	protected ArrayList (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ArrayList ();
	public ArrayList (int capacity);
	public ArrayList (System.Collections.ICollection collection);
	
	public virtual Java.Lang.Object Clone ();
	public virtual void EnsureCapacity (int minimumCapacity);
	public override Java.Lang.Object Get (int location);
	public override int Size ();
	public virtual void TrimToSize ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Collections'>New Type: Java.Util.Collections</h3>

```
public class Collections : Java.Lang.Object {
	
	protected Collections (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static bool AddAll (System.Collections.ICollection c, params Java.Lang.Object[] a);
	public static IQueue AsLifoQueue (IDeque p0);
	public static int BinarySearch (System.Collections.IList list, Java.Lang.Object object);
	public static int BinarySearch (System.Collections.IList list, Java.Lang.Object object, IComparator comparator);
	public static System.Collections.ICollection CheckedCollection (System.Collections.ICollection c, Java.Lang.Class type);
	public static System.Collections.IList CheckedList (System.Collections.IList list, Java.Lang.Class type);
	public static System.Collections.IDictionary CheckedMap (System.Collections.IDictionary m, Java.Lang.Class keyType, Java.Lang.Class valueType);
	public static System.Collections.ICollection CheckedSet (System.Collections.ICollection s, Java.Lang.Class type);
	public static System.Collections.IDictionary CheckedSortedMap (System.Collections.IDictionary m, Java.Lang.Class keyType, Java.Lang.Class valueType);
	public static ISortedSet CheckedSortedSet (ISortedSet s, Java.Lang.Class type);
	public static void Copy (System.Collections.IList destination, System.Collections.IList source);
	public static bool Disjoint (System.Collections.Generic.ICollection c1, System.Collections.Generic.ICollection c2);
	public static IEnumeration EmptyEnumeration ();
	public static IIterator EmptyIterator ();
	public static System.Collections.IList EmptyList ();
	public static IListIterator EmptyListIterator ();
	public static System.Collections.IDictionary EmptyMap ();
	public static System.Collections.ICollection EmptySet ();
	public static IEnumeration Enumeration (System.Collections.ICollection collection);
	public static void Fill (System.Collections.IList list, Java.Lang.Object object);
	public static int Frequency (System.Collections.Generic.ICollection c, Java.Lang.Object o);
	public static int IndexOfSubList (System.Collections.Generic.IList list, System.Collections.Generic.IList sublist);
	public static int LastIndexOfSubList (System.Collections.Generic.IList list, System.Collections.Generic.IList sublist);
	public static System.Collections.IList List (IEnumeration enumeration);
	public static Java.Lang.Object Max (System.Collections.ICollection collection);
	public static Java.Lang.Object Max (System.Collections.ICollection collection, IComparator comparator);
	public static Java.Lang.Object Min (System.Collections.ICollection collection);
	public static Java.Lang.Object Min (System.Collections.ICollection collection, IComparator comparator);
	public static System.Collections.IList NCopies (int length, Java.Lang.Object object);
	public static System.Collections.ICollection NewSetFromMap (System.Collections.IDictionary p0);
	public static bool ReplaceAll (System.Collections.IList list, Java.Lang.Object obj, Java.Lang.Object obj2);
	public static void Reverse (System.Collections.Generic.IList list);
	public static IComparator ReverseOrder ();
	public static IComparator ReverseOrder (IComparator c);
	public static void Rotate (System.Collections.Generic.IList lst, int dist);
	public static void Shuffle (System.Collections.Generic.IList list);
	public static void Shuffle (System.Collections.Generic.IList list, Random random);
	public static System.Collections.ICollection Singleton (Java.Lang.Object p0);
	public static System.Collections.IList SingletonList (Java.Lang.Object p0);
	public static System.Collections.IDictionary SingletonMap (Java.Lang.Object key, Java.Lang.Object value);
	public static void Sort (System.Collections.IList list);
	public static void Sort (System.Collections.IList list, IComparator comparator);
	public static void Swap (System.Collections.Generic.IList list, int index1, int index2);
	public static System.Collections.ICollection SynchronizedCollection (System.Collections.ICollection collection);
	public static System.Collections.IList SynchronizedList (System.Collections.IList list);
	public static System.Collections.IDictionary SynchronizedMap (System.Collections.IDictionary map);
	public static System.Collections.ICollection SynchronizedSet (System.Collections.ICollection p0);
	public static System.Collections.IDictionary SynchronizedSortedMap (System.Collections.IDictionary map);
	public static ISortedSet SynchronizedSortedSet (ISortedSet p0);
	public static System.Collections.ICollection UnmodifiableCollection (System.Collections.ICollection p0);
	public static System.Collections.IList UnmodifiableList (System.Collections.IList p0);
	public static System.Collections.IDictionary UnmodifiableMap (System.Collections.IDictionary map);
	public static System.Collections.ICollection UnmodifiableSet (System.Collections.ICollection p0);
	public static System.Collections.IDictionary UnmodifiableSortedMap (System.Collections.IDictionary map);
	public static ISortedSet UnmodifiableSortedSet (ISortedSet p0);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.EnumMap'>New Type: Java.Util.EnumMap</h3>

```
public class EnumMap : AbstractMap, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected EnumMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public EnumMap (Java.Lang.Class keyType);
	public EnumMap (EnumMap map);
	public EnumMap (System.Collections.IDictionary map);
	
	public virtual EnumMap Clone ();
	public override System.Collections.ICollection EntrySet ();
	public override Java.Lang.Object Put (Java.Lang.Object key, Java.Lang.Object value);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.EnumSet'>New Type: Java.Util.EnumSet</h3>

```
public abstract class EnumSet : AbstractSet, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected EnumSet (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static EnumSet AllOf (Java.Lang.Class elementType);
	public static EnumSet ComplementOf (EnumSet s);
	public static EnumSet CopyOf (EnumSet s);
	public static EnumSet CopyOf (System.Collections.ICollection c);
	public static EnumSet NoneOf (Java.Lang.Class elementType);
	public static EnumSet Of (Java.Lang.Object e);
	public static EnumSet Of (Java.Lang.Object e1, Java.Lang.Object e2);
	public static EnumSet Of (Java.Lang.Object e1, Java.Lang.Object e2, Java.Lang.Object e3);
	public static EnumSet Of (Java.Lang.Object e1, Java.Lang.Object e2, Java.Lang.Object e3, Java.Lang.Object e4);
	public static EnumSet Of (Java.Lang.Object e1, Java.Lang.Object e2, Java.Lang.Object e3, Java.Lang.Object e4, Java.Lang.Object e5);
	public static EnumSet Of (Java.Lang.Object start, params Java.Lang.Object[] others);
	public static EnumSet Range (Java.Lang.Object start, Java.Lang.Object end);
	public virtual EnumSet Clone ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.HashMap'>New Type: Java.Util.HashMap</h3>

```
public class HashMap : AbstractMap, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected HashMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HashMap ();
	public HashMap (int capacity);
	public HashMap (int capacity, float loadFactor);
	public HashMap (System.Collections.IDictionary map);
	
	public virtual Java.Lang.Object Clone ();
	public override System.Collections.ICollection EntrySet ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.HashSet'>New Type: Java.Util.HashSet</h3>

```
public class HashSet : AbstractSet, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected HashSet (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HashSet ();
	public HashSet (int capacity);
	public HashSet (int capacity, float loadFactor);
	public HashSet (System.Collections.ICollection collection);
	
	public virtual Java.Lang.Object Clone ();
	public override IIterator Iterator ();
	public override int Size ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.ICollection'>Type Changed: Java.Util.ICollection</h3>

Added:

```
IIterator Iterator ();
```

<h3 id='Java.Util.IDeque'>New Type: Java.Util.IDeque</h3>

```
public interface IDeque : ICollection, IDisposable, Java.Lang.IIterable, Android.Runtime.IJavaObject, IQueue {
	
	bool Add (Java.Lang.Object p0);
	void AddFirst (Java.Lang.Object e);
	void AddLast (Java.Lang.Object e);
	bool Contains (Java.Lang.Object p0);
	IIterator DescendingIterator ();
	Java.Lang.Object Element ();
	IIterator Iterator ();
	bool Offer (Java.Lang.Object p0);
	bool OfferFirst (Java.Lang.Object e);
	bool OfferLast (Java.Lang.Object e);
	Java.Lang.Object Peek ();
	Java.Lang.Object PeekFirst ();
	Java.Lang.Object PeekLast ();
	Java.Lang.Object Poll ();
	Java.Lang.Object PollFirst ();
	Java.Lang.Object PollLast ();
	Java.Lang.Object Pop ();
	void Push (Java.Lang.Object e);
	Java.Lang.Object Remove ();
	bool Remove (Java.Lang.Object p0);
	Java.Lang.Object RemoveFirst ();
	bool RemoveFirstOccurrence (Java.Lang.Object o);
	Java.Lang.Object RemoveLast ();
	bool RemoveLastOccurrence (Java.Lang.Object o);
	int Size ();
	
	Java.Lang.Object First {
		get;
	}
	Java.Lang.Object Last {
		get;
	}
}
```

<h3 id='Java.Util.IList'>New Type: Java.Util.IList</h3>

```
public interface IList : ICollection, IDisposable, Java.Lang.IIterable, Android.Runtime.IJavaObject {
	
	void Add (int location, Java.Lang.Object object);
	bool Add (Java.Lang.Object object);
	bool AddAll (System.Collections.ICollection collection);
	bool AddAll (int location, System.Collections.ICollection collection);
	void Clear ();
	bool Contains (Java.Lang.Object object);
	bool ContainsAll (System.Collections.ICollection collection);
	bool Equals (Java.Lang.Object object);
	Java.Lang.Object Get (int location);
	int GetHashCode ();
	int IndexOf (Java.Lang.Object object);
	IIterator Iterator ();
	int LastIndexOf (Java.Lang.Object object);
	IListIterator ListIterator ();
	IListIterator ListIterator (int location);
	Java.Lang.Object Remove (int location);
	bool Remove (Java.Lang.Object object);
	bool RemoveAll (System.Collections.ICollection collection);
	bool RetainAll (System.Collections.ICollection collection);
	Java.Lang.Object Set (int location, Java.Lang.Object object);
	int Size ();
	System.Collections.IList SubList (int start, int end);
	Java.Lang.Object[] ToArray ();
	Java.Lang.Object[] ToArray (Java.Lang.Object[] array);
	
	bool IsEmpty {
		get;
	}
}
```

<h3 id='Java.Util.IListIterator'>New Type: Java.Util.IListIterator</h3>

```
public interface IListIterator : IDisposable, IIterator, Android.Runtime.IJavaObject {
	
	void Add (Java.Lang.Object object);
	Java.Lang.Object Next ();
	int NextIndex ();
	Java.Lang.Object Previous ();
	int PreviousIndex ();
	void Remove ();
	void Set (Java.Lang.Object object);
	
	bool HasNext {
		get;
	}
	bool HasPrevious {
		get;
	}
}
```

<h3 id='Java.Util.INavigableMap'>New Type: Java.Util.INavigableMap</h3>

```
public interface INavigableMap : IDisposable, Android.Runtime.IJavaObject, IMap, ISortedMap {
	
	IMapEntry CeilingEntry (Java.Lang.Object key);
	Java.Lang.Object CeilingKey (Java.Lang.Object key);
	INavigableSet DescendingKeySet ();
	INavigableMap DescendingMap ();
	IMapEntry FirstEntry ();
	IMapEntry FloorEntry (Java.Lang.Object key);
	Java.Lang.Object FloorKey (Java.Lang.Object key);
	System.Collections.IDictionary HeadMap (Java.Lang.Object p0);
	INavigableMap HeadMap (Java.Lang.Object endKey, bool inclusive);
	IMapEntry HigherEntry (Java.Lang.Object key);
	Java.Lang.Object HigherKey (Java.Lang.Object key);
	IMapEntry LastEntry ();
	IMapEntry LowerEntry (Java.Lang.Object key);
	Java.Lang.Object LowerKey (Java.Lang.Object key);
	INavigableSet NavigableKeySet ();
	IMapEntry PollFirstEntry ();
	IMapEntry PollLastEntry ();
	INavigableMap SubMap (Java.Lang.Object startKey, bool startInclusive, Java.Lang.Object endKey, bool endInclusive);
	System.Collections.IDictionary SubMap (Java.Lang.Object p0, Java.Lang.Object p1);
	System.Collections.IDictionary TailMap (Java.Lang.Object p0);
	INavigableMap TailMap (Java.Lang.Object startKey, bool inclusive);
}
```

<h3 id='Java.Util.INavigableSet'>New Type: Java.Util.INavigableSet</h3>

```
public interface INavigableSet : ICollection, IDisposable, Java.Lang.IIterable, Android.Runtime.IJavaObject, ISet, ISortedSet {
	
	Java.Lang.Object Ceiling (Java.Lang.Object e);
	IIterator DescendingIterator ();
	INavigableSet DescendingSet ();
	Java.Lang.Object Floor (Java.Lang.Object e);
	ISortedSet HeadSet (Java.Lang.Object p0);
	INavigableSet HeadSet (Java.Lang.Object end, bool endInclusive);
	Java.Lang.Object Higher (Java.Lang.Object e);
	IIterator Iterator ();
	Java.Lang.Object Lower (Java.Lang.Object e);
	Java.Lang.Object PollFirst ();
	Java.Lang.Object PollLast ();
	INavigableSet SubSet (Java.Lang.Object start, bool startInclusive, Java.Lang.Object end, bool endInclusive);
	ISortedSet SubSet (Java.Lang.Object p0, Java.Lang.Object p1);
	ISortedSet TailSet (Java.Lang.Object p0);
	INavigableSet TailSet (Java.Lang.Object start, bool startInclusive);
}
```

<h3 id='Java.Util.IQueue'>New Type: Java.Util.IQueue</h3>

```
public interface IQueue : ICollection, IDisposable, Java.Lang.IIterable, Android.Runtime.IJavaObject {
	
	bool Add (Java.Lang.Object p0);
	Java.Lang.Object Element ();
	bool Offer (Java.Lang.Object o);
	Java.Lang.Object Peek ();
	Java.Lang.Object Poll ();
	Java.Lang.Object Remove ();
}
```

<h3 id='Java.Util.ISet'>New Type: Java.Util.ISet</h3>

```
public interface ISet : ICollection, IDisposable, Java.Lang.IIterable, Android.Runtime.IJavaObject {
	
	bool Add (Java.Lang.Object object);
	bool AddAll (System.Collections.ICollection collection);
	void Clear ();
	bool Contains (Java.Lang.Object object);
	bool ContainsAll (System.Collections.ICollection collection);
	bool Equals (Java.Lang.Object object);
	int GetHashCode ();
	IIterator Iterator ();
	bool Remove (Java.Lang.Object object);
	bool RemoveAll (System.Collections.ICollection collection);
	bool RetainAll (System.Collections.ICollection collection);
	int Size ();
	Java.Lang.Object[] ToArray ();
	Java.Lang.Object[] ToArray (Java.Lang.Object[] array);
	
	bool IsEmpty {
		get;
	}
}
```

<h3 id='Java.Util.ISortedMap'>New Type: Java.Util.ISortedMap</h3>

```
public interface ISortedMap : IDisposable, Android.Runtime.IJavaObject, IMap {
	
	IComparator Comparator ();
	System.Collections.ICollection EntrySet ();
	Java.Lang.Object FirstKey ();
	System.Collections.IDictionary HeadMap (Java.Lang.Object endKey);
	System.Collections.ICollection KeySet ();
	Java.Lang.Object LastKey ();
	System.Collections.IDictionary SubMap (Java.Lang.Object startKey, Java.Lang.Object endKey);
	System.Collections.IDictionary TailMap (Java.Lang.Object startKey);
	System.Collections.ICollection Values ();
}
```

<h3 id='Java.Util.ISortedSet'>New Type: Java.Util.ISortedSet</h3>

```
public interface ISortedSet : ICollection, IDisposable, Java.Lang.IIterable, Android.Runtime.IJavaObject, ISet {
	
	IComparator Comparator ();
	Java.Lang.Object First ();
	ISortedSet HeadSet (Java.Lang.Object end);
	Java.Lang.Object Last ();
	ISortedSet SubSet (Java.Lang.Object start, Java.Lang.Object end);
	ISortedSet TailSet (Java.Lang.Object start);
}
```

<h3 id='Java.Util.IdentityHashMap'>New Type: Java.Util.IdentityHashMap</h3>

```
public class IdentityHashMap : AbstractMap, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected IdentityHashMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public IdentityHashMap ();
	public IdentityHashMap (int maxSize);
	public IdentityHashMap (System.Collections.IDictionary map);
	
	public virtual Java.Lang.Object Clone ();
	public override System.Collections.ICollection EntrySet ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.LinkedHashMap'>New Type: Java.Util.LinkedHashMap</h3>

```
public class LinkedHashMap : HashMap {
	
	protected LinkedHashMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LinkedHashMap ();
	public LinkedHashMap (int initialCapacity);
	public LinkedHashMap (int initialCapacity, float loadFactor);
	public LinkedHashMap (int initialCapacity, float loadFactor, bool accessOrder);
	public LinkedHashMap (System.Collections.IDictionary map);
	
	protected virtual bool RemoveEldestEntry (IMapEntry eldest);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.LinkedHashSet'>New Type: Java.Util.LinkedHashSet</h3>

```
public class LinkedHashSet : HashSet {
	
	protected LinkedHashSet (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LinkedHashSet ();
	public LinkedHashSet (int capacity);
	public LinkedHashSet (int capacity, float loadFactor);
	public LinkedHashSet (System.Collections.ICollection collection);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.LinkedList'>New Type: Java.Util.LinkedList</h3>

```
public class LinkedList : AbstractSequentialList, Java.Lang.ICloneable, IDeque, IQueue, Java.IO.ISerializable {
	
	protected LinkedList (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LinkedList ();
	public LinkedList (System.Collections.ICollection collection);
	
	public virtual void AddFirst (Java.Lang.Object object);
	public virtual void AddLast (Java.Lang.Object object);
	public virtual Java.Lang.Object Clone ();
	public virtual IIterator DescendingIterator ();
	public virtual Java.Lang.Object Element ();
	public override IListIterator ListIterator (int location);
	public virtual bool Offer (Java.Lang.Object o);
	public virtual bool OfferFirst (Java.Lang.Object p0);
	public virtual bool OfferLast (Java.Lang.Object p0);
	public virtual Java.Lang.Object Peek ();
	public virtual Java.Lang.Object PeekFirst ();
	public virtual Java.Lang.Object PeekLast ();
	public virtual Java.Lang.Object Poll ();
	public virtual Java.Lang.Object PollFirst ();
	public virtual Java.Lang.Object PollLast ();
	public virtual Java.Lang.Object Pop ();
	public virtual void Push (Java.Lang.Object p0);
	public virtual Java.Lang.Object Remove ();
	public virtual Java.Lang.Object RemoveFirst ();
	public virtual bool RemoveFirstOccurrence (Java.Lang.Object p0);
	public virtual Java.Lang.Object RemoveLast ();
	public virtual bool RemoveLastOccurrence (Java.Lang.Object p0);
	public override int Size ();
	
	public virtual Java.Lang.Object First {
		get;
	}
	public virtual Java.Lang.Object Last {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.PriorityQueue'>New Type: Java.Util.PriorityQueue</h3>

```
public class PriorityQueue : AbstractQueue, Java.IO.ISerializable {
	
	protected PriorityQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PriorityQueue ();
	public PriorityQueue (int initialCapacity);
	public PriorityQueue (int initialCapacity, IComparator comparator);
	public PriorityQueue (System.Collections.ICollection c);
	public PriorityQueue (PriorityQueue c);
	public PriorityQueue (ISortedSet c);
	
	public virtual IComparator Comparator ();
	public override IIterator Iterator ();
	public override bool Offer (Java.Lang.Object o);
	public override Java.Lang.Object Peek ();
	public override Java.Lang.Object Poll ();
	public override int Size ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Stack'>New Type: Java.Util.Stack</h3>

```
public class Stack : Vector {
	
	protected Stack (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Stack ();
	
	public virtual bool Empty ();
	public virtual Java.Lang.Object Peek ();
	public virtual Java.Lang.Object Pop ();
	public virtual Java.Lang.Object Push (Java.Lang.Object object);
	public virtual int Search (Java.Lang.Object o);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.TreeMap'>New Type: Java.Util.TreeMap</h3>

```
public class TreeMap : AbstractMap, Java.Lang.ICloneable, INavigableMap, Java.IO.ISerializable, ISortedMap {
	
	protected TreeMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TreeMap ();
	public TreeMap (IComparator comparator);
	public TreeMap (System.Collections.IDictionary map);
	
	public virtual IMapEntry CeilingEntry (Java.Lang.Object p0);
	public virtual Java.Lang.Object CeilingKey (Java.Lang.Object p0);
	public virtual Java.Lang.Object Clone ();
	public virtual IComparator Comparator ();
	public virtual INavigableSet DescendingKeySet ();
	public virtual INavigableMap DescendingMap ();
	public override System.Collections.ICollection EntrySet ();
	public virtual IMapEntry FirstEntry ();
	public virtual Java.Lang.Object FirstKey ();
	public virtual IMapEntry FloorEntry (Java.Lang.Object p0);
	public virtual Java.Lang.Object FloorKey (Java.Lang.Object p0);
	public virtual System.Collections.IDictionary HeadMap (Java.Lang.Object endKey);
	public virtual INavigableMap HeadMap (Java.Lang.Object p0, bool p1);
	public virtual IMapEntry HigherEntry (Java.Lang.Object p0);
	public virtual Java.Lang.Object HigherKey (Java.Lang.Object p0);
	public virtual IMapEntry LastEntry ();
	public virtual Java.Lang.Object LastKey ();
	public virtual IMapEntry LowerEntry (Java.Lang.Object p0);
	public virtual Java.Lang.Object LowerKey (Java.Lang.Object p0);
	public virtual INavigableSet NavigableKeySet ();
	public virtual IMapEntry PollFirstEntry ();
	public virtual IMapEntry PollLastEntry ();
	public virtual INavigableMap SubMap (Java.Lang.Object p0, bool p1, Java.Lang.Object p2, bool p3);
	public virtual System.Collections.IDictionary SubMap (Java.Lang.Object startKey, Java.Lang.Object endKey);
	public virtual System.Collections.IDictionary TailMap (Java.Lang.Object startKey);
	public virtual INavigableMap TailMap (Java.Lang.Object p0, bool p1);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.TreeSet'>New Type: Java.Util.TreeSet</h3>

```
public class TreeSet : AbstractSet, Java.Lang.ICloneable, INavigableSet, Java.IO.ISerializable, ISortedSet {
	
	protected TreeSet (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TreeSet ();
	public TreeSet (System.Collections.ICollection collection);
	public TreeSet (IComparator comparator);
	public TreeSet (ISortedSet set);
	
	public virtual Java.Lang.Object Ceiling (Java.Lang.Object p0);
	public virtual Java.Lang.Object Clone ();
	public virtual IComparator Comparator ();
	public virtual IIterator DescendingIterator ();
	public virtual INavigableSet DescendingSet ();
	public virtual Java.Lang.Object First ();
	public virtual Java.Lang.Object Floor (Java.Lang.Object p0);
	public virtual ISortedSet HeadSet (Java.Lang.Object end);
	public virtual INavigableSet HeadSet (Java.Lang.Object p0, bool p1);
	public virtual Java.Lang.Object Higher (Java.Lang.Object p0);
	public override IIterator Iterator ();
	public virtual Java.Lang.Object Last ();
	public virtual Java.Lang.Object Lower (Java.Lang.Object p0);
	public virtual Java.Lang.Object PollFirst ();
	public virtual Java.Lang.Object PollLast ();
	public override int Size ();
	public virtual INavigableSet SubSet (Java.Lang.Object p0, bool p1, Java.Lang.Object p2, bool p3);
	public virtual ISortedSet SubSet (Java.Lang.Object start, Java.Lang.Object end);
	public virtual ISortedSet TailSet (Java.Lang.Object start);
	public virtual INavigableSet TailSet (Java.Lang.Object p0, bool p1);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Vector'>New Type: Java.Util.Vector</h3>

```
public class Vector : AbstractList, Java.Lang.ICloneable, IRandomAccess, Java.IO.ISerializable {
	
	protected Vector (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Vector ();
	public Vector (int capacity);
	public Vector (int capacity, int capacityIncrement);
	public Vector (System.Collections.ICollection collection);
	
	public virtual void AddElement (Java.Lang.Object object);
	public virtual int Capacity ();
	public virtual Java.Lang.Object Clone ();
	public virtual void CopyInto (Java.Lang.Object[] elements);
	public virtual Java.Lang.Object ElementAt (int location);
	public virtual IEnumeration Elements ();
	public virtual void EnsureCapacity (int minimumCapacity);
	public virtual Java.Lang.Object FirstElement ();
	public override Java.Lang.Object Get (int location);
	public virtual int IndexOf (Java.Lang.Object object, int location);
	public virtual void InsertElementAt (Java.Lang.Object object, int location);
	public virtual Java.Lang.Object LastElement ();
	public virtual int LastIndexOf (Java.Lang.Object object, int location);
	public virtual void RemoveAllElements ();
	public virtual bool RemoveElement (Java.Lang.Object object);
	public virtual void RemoveElementAt (int location);
	public virtual void SetElementAt (Java.Lang.Object object, int location);
	public virtual void SetSize (int length);
	public override int Size ();
	public virtual void TrimToSize ();
	
	protected int CapacityIncrement {
		get;
		set;
	}
	protected int ElementCount {
		get;
		set;
	}
	protected System.Collections.Generic.IList ElementData {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.WeakHashMap'>New Type: Java.Util.WeakHashMap</h3>

```
public class WeakHashMap : AbstractMap {
	
	protected WeakHashMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public WeakHashMap ();
	public WeakHashMap (int capacity);
	public WeakHashMap (int capacity, float loadFactor);
	public WeakHashMap (System.Collections.IDictionary map);
	
	public override System.Collections.ICollection EntrySet ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Java.Util.Concurrent'>Namespace: Java.Util.Concurrent</h2>

<h3 id='Java.Util.Concurrent.AbstractExecutorService'>New Type: Java.Util.Concurrent.AbstractExecutorService</h3>

```
public abstract class AbstractExecutorService : Java.Lang.Object, IExecutor, IExecutorService {
	
	protected AbstractExecutorService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractExecutorService ();
	
	public abstract bool AwaitTermination (long timeout, TimeUnit unit);
	public System.Threading.Tasks.Task AwaitTerminationAsync (long timeout, TimeUnit unit);
	public abstract void Execute (Java.Lang.IRunnable command);
	public virtual System.Collections.IList InvokeAll (System.Collections.ICollection p0);
	public virtual System.Collections.IList InvokeAll (System.Collections.ICollection p0, long p1, TimeUnit p2);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection p0);
	public virtual Java.Lang.Object InvokeAny (System.Collections.ICollection p0, long p1, TimeUnit p2);
	protected virtual IRunnableFuture NewTaskFor (ICallable p0);
	protected virtual IRunnableFuture NewTaskFor (Java.Lang.IRunnable p0, Java.Lang.Object p1);
	public abstract void Shutdown ();
	public abstract System.Collections.Generic.IList ShutdownNow ();
	public virtual IFuture Submit (ICallable task);
	public virtual IFuture Submit (Java.Lang.IRunnable task);
	public virtual IFuture Submit (Java.Lang.IRunnable task, Java.Lang.Object result);
	
	public abstract bool IsShutdown {
		get;
	}
	public abstract bool IsTerminated {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.ArrayBlockingQueue'>New Type: Java.Util.Concurrent.ArrayBlockingQueue</h3>

```
public class ArrayBlockingQueue : Java.Util.AbstractQueue, IBlockingQueue, Java.IO.ISerializable {
	
	protected ArrayBlockingQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ArrayBlockingQueue (int capacity);
	public ArrayBlockingQueue (int capacity, bool fair);
	public ArrayBlockingQueue (int capacity, bool fair, System.Collections.ICollection c);
	
	public virtual int DrainTo (System.Collections.ICollection c);
	public virtual int DrainTo (System.Collections.ICollection c, int maxElements);
	public override Java.Util.IIterator Iterator ();
	public override bool Offer (Java.Lang.Object e);
	public virtual bool Offer (Java.Lang.Object e, long timeout, TimeUnit unit);
	public override Java.Lang.Object Peek ();
	public override Java.Lang.Object Poll ();
	public virtual Java.Lang.Object Poll (long timeout, TimeUnit unit);
	public virtual void Put (Java.Lang.Object e);
	public virtual int RemainingCapacity ();
	public override int Size ();
	public virtual Java.Lang.Object Take ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.BrokenBarrierException'>New Type: Java.Util.Concurrent.BrokenBarrierException</h3>

```
public class BrokenBarrierException : Java.Lang.Exception {
	
	protected BrokenBarrierException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BrokenBarrierException ();
	public BrokenBarrierException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.CancellationException'>New Type: Java.Util.Concurrent.CancellationException</h3>

```
public class CancellationException : Java.Lang.IllegalStateException {
	
	protected CancellationException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CancellationException ();
	public CancellationException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.ConcurrentHashMap'>New Type: Java.Util.Concurrent.ConcurrentHashMap</h3>

```
public class ConcurrentHashMap : Java.Util.AbstractMap, IConcurrentMap, Java.IO.ISerializable {
	
	protected ConcurrentHashMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConcurrentHashMap ();
	public ConcurrentHashMap (int initialCapacity);
	public ConcurrentHashMap (int p0, float p1);
	public ConcurrentHashMap (int initialCapacity, float loadFactor, int concurrencyLevel);
	public ConcurrentHashMap (System.Collections.IDictionary m);
	
	public virtual bool Contains (Java.Lang.Object value);
	public virtual Java.Util.IEnumeration Elements ();
	public override System.Collections.ICollection EntrySet ();
	public virtual Java.Util.IEnumeration Keys ();
	public virtual Java.Lang.Object PutIfAbsent (Java.Lang.Object key, Java.Lang.Object value);
	public virtual bool Remove (Java.Lang.Object key, Java.Lang.Object value);
	public virtual Java.Lang.Object Replace (Java.Lang.Object key, Java.Lang.Object value);
	public virtual bool Replace (Java.Lang.Object key, Java.Lang.Object oldValue, Java.Lang.Object newValue);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.ConcurrentLinkedQueue'>New Type: Java.Util.Concurrent.ConcurrentLinkedQueue</h3>

```
public class ConcurrentLinkedQueue : Java.Util.AbstractQueue, Java.IO.ISerializable {
	
	protected ConcurrentLinkedQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConcurrentLinkedQueue ();
	public ConcurrentLinkedQueue (System.Collections.ICollection c);
	
	public override Java.Util.IIterator Iterator ();
	public override bool Offer (Java.Lang.Object e);
	public override Java.Lang.Object Peek ();
	public override Java.Lang.Object Poll ();
	public override int Size ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.ConcurrentSkipListMap'>New Type: Java.Util.Concurrent.ConcurrentSkipListMap</h3>

```
public class ConcurrentSkipListMap : Java.Util.AbstractMap, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected ConcurrentSkipListMap (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConcurrentSkipListMap ();
	public ConcurrentSkipListMap (Java.Util.IComparator comparator);
	public ConcurrentSkipListMap (System.Collections.IDictionary m);
	
	public virtual Java.Util.IMapEntry CeilingEntry (Java.Lang.Object key);
	public virtual Java.Lang.Object CeilingKey (Java.Lang.Object key);
	public virtual ConcurrentSkipListMap Clone ();
	public virtual Java.Util.IComparator Comparator ();
	public virtual Java.Util.INavigableSet DescendingKeySet ();
	public override System.Collections.ICollection EntrySet ();
	public virtual Java.Util.IMapEntry FirstEntry ();
	public virtual Java.Lang.Object FirstKey ();
	public virtual Java.Util.IMapEntry FloorEntry (Java.Lang.Object key);
	public virtual Java.Lang.Object FloorKey (Java.Lang.Object key);
	public virtual Java.Util.IMapEntry HigherEntry (Java.Lang.Object key);
	public virtual Java.Lang.Object HigherKey (Java.Lang.Object key);
	public virtual Java.Util.IMapEntry LastEntry ();
	public virtual Java.Lang.Object LastKey ();
	public virtual Java.Util.IMapEntry LowerEntry (Java.Lang.Object key);
	public virtual Java.Lang.Object LowerKey (Java.Lang.Object key);
	public virtual Java.Util.INavigableSet NavigableKeySet ();
	public virtual Java.Util.IMapEntry PollFirstEntry ();
	public virtual Java.Util.IMapEntry PollLastEntry ();
	public virtual Java.Lang.Object PutIfAbsent (Java.Lang.Object key, Java.Lang.Object value);
	public virtual bool Remove (Java.Lang.Object key, Java.Lang.Object value);
	public virtual Java.Lang.Object Replace (Java.Lang.Object key, Java.Lang.Object value);
	public virtual bool Replace (Java.Lang.Object key, Java.Lang.Object oldValue, Java.Lang.Object newValue);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.CopyOnWriteArrayList'>New Type: Java.Util.Concurrent.CopyOnWriteArrayList</h3>

```
public class CopyOnWriteArrayList : Java.Lang.Object, Java.Lang.ICloneable, Java.Util.ICollection, Java.Lang.IIterable, Java.Util.IList, Java.Util.IRandomAccess, Java.IO.ISerializable {
	
	protected CopyOnWriteArrayList (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CopyOnWriteArrayList ();
	public CopyOnWriteArrayList (Java.Lang.Object[] toCopyIn);
	public CopyOnWriteArrayList (System.Collections.ICollection c);
	
	public virtual void Add (int index, Java.Lang.Object element);
	public virtual bool Add (Java.Lang.Object e);
	public virtual bool AddAll (System.Collections.ICollection c);
	public virtual bool AddAll (int index, System.Collections.ICollection c);
	public virtual int AddAllAbsent (System.Collections.ICollection c);
	public virtual bool AddIfAbsent (Java.Lang.Object e);
	public virtual void Clear ();
	public virtual Java.Lang.Object Clone ();
	public virtual bool Contains (Java.Lang.Object o);
	public virtual bool ContainsAll (System.Collections.ICollection c);
	public virtual Java.Lang.Object Get (int index);
	public virtual int IndexOf (Java.Lang.Object o);
	public virtual int IndexOf (Java.Lang.Object e, int index);
	public virtual Java.Util.IIterator Iterator ();
	public virtual int LastIndexOf (Java.Lang.Object o);
	public virtual int LastIndexOf (Java.Lang.Object e, int index);
	public virtual Java.Util.IListIterator ListIterator ();
	public virtual Java.Util.IListIterator ListIterator (int index);
	public virtual Java.Lang.Object Remove (int index);
	public virtual bool Remove (Java.Lang.Object o);
	public virtual bool RemoveAll (System.Collections.ICollection c);
	public virtual bool RetainAll (System.Collections.ICollection c);
	public virtual Java.Lang.Object Set (int index, Java.Lang.Object element);
	public virtual int Size ();
	public virtual System.Collections.IList SubList (int fromIndex, int toIndex);
	public virtual Java.Lang.Object[] ToArray ();
	public virtual Java.Lang.Object[] ToArray (Java.Lang.Object[] a);
	
	public virtual bool IsEmpty {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.CopyOnWriteArraySet'>New Type: Java.Util.Concurrent.CopyOnWriteArraySet</h3>

```
public class CopyOnWriteArraySet : Java.Util.AbstractSet, Java.IO.ISerializable {
	
	protected CopyOnWriteArraySet (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CopyOnWriteArraySet ();
	public CopyOnWriteArraySet (System.Collections.ICollection c);
	
	public override Java.Util.IIterator Iterator ();
	public override int Size ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.CountDownLatch'>New Type: Java.Util.Concurrent.CountDownLatch</h3>

```
public class CountDownLatch : Java.Lang.Object {
	
	protected CountDownLatch (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CountDownLatch (int count);
	
	public virtual void Await ();
	public virtual bool Await (long timeout, TimeUnit unit);
	public System.Threading.Tasks.Task AwaitAsync ();
	public System.Threading.Tasks.Task AwaitAsync (long timeout, TimeUnit unit);
	public virtual void CountDown ();
	
	public virtual long Count {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.CyclicBarrier'>New Type: Java.Util.Concurrent.CyclicBarrier</h3>

```
public class CyclicBarrier : Java.Lang.Object {
	
	protected CyclicBarrier (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CyclicBarrier (int parties);
	public CyclicBarrier (int parties, Java.Lang.IRunnable barrierAction);
	
	public virtual int Await ();
	public virtual int Await (long timeout, TimeUnit unit);
	public System.Threading.Tasks.Task AwaitAsync ();
	public System.Threading.Tasks.Task AwaitAsync (long timeout, TimeUnit unit);
	public virtual void Reset ();
	
	public virtual bool IsBroken {
		get;
	}
	public virtual int NumberWaiting {
		get;
	}
	public virtual int Parties {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.DelayQueue'>New Type: Java.Util.Concurrent.DelayQueue</h3>

```
public class DelayQueue : Java.Util.AbstractQueue, IBlockingQueue {
	
	protected DelayQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DelayQueue ();
	public DelayQueue (System.Collections.ICollection c);
	
	public override bool Add (Java.Lang.Object e);
	public virtual int DrainTo (System.Collections.ICollection c);
	public virtual int DrainTo (System.Collections.ICollection c, int maxElements);
	public override Java.Util.IIterator Iterator ();
	public override bool Offer (Java.Lang.Object e);
	public virtual bool Offer (Java.Lang.Object e, long timeout, TimeUnit unit);
	public override Java.Lang.Object Peek ();
	public override Java.Lang.Object Poll ();
	public virtual Java.Lang.Object Poll (long timeout, TimeUnit unit);
	public virtual void Put (Java.Lang.Object e);
	public virtual int RemainingCapacity ();
	public override int Size ();
	public virtual Java.Lang.Object Take ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Exchanger'>New Type: Java.Util.Concurrent.Exchanger</h3>

```
public class Exchanger : Java.Lang.Object {
	
	protected Exchanger (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Exchanger ();
	
	public virtual Java.Lang.Object Exchange (Java.Lang.Object x);
	public virtual Java.Lang.Object Exchange (Java.Lang.Object x, long timeout, TimeUnit unit);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.ExecutionException'>New Type: Java.Util.Concurrent.ExecutionException</h3>

```
public class ExecutionException : Java.Lang.Exception {
	
	protected ExecutionException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected ExecutionException ();
	protected ExecutionException (string message);
	public ExecutionException (string message, Java.Lang.Throwable cause);
	public ExecutionException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.ExecutorCompletionService'>New Type: Java.Util.Concurrent.ExecutorCompletionService</h3>

```
public class ExecutorCompletionService : Java.Lang.Object, ICompletionService {
	
	protected ExecutorCompletionService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ExecutorCompletionService (IExecutor executor);
	public ExecutorCompletionService (IExecutor executor, IBlockingQueue completionQueue);
	
	public virtual IFuture Poll ();
	public virtual IFuture Poll (long timeout, TimeUnit unit);
	public System.Threading.Tasks.Task PollAsync ();
	public System.Threading.Tasks.Task PollAsync (long timeout, TimeUnit unit);
	public virtual IFuture Submit (ICallable task);
	public virtual IFuture Submit (Java.Lang.IRunnable task, Java.Lang.Object result);
	public virtual IFuture Take ();
	public System.Threading.Tasks.Task TakeAsync ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Executors'>New Type: Java.Util.Concurrent.Executors</h3>

```
public class Executors : Java.Lang.Object {
	
	protected Executors (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static ICallable Callable (Java.Security.IPrivilegedAction p0);
	public static ICallable Callable (Java.Security.IPrivilegedExceptionAction p0);
	public static ICallable Callable (Java.Lang.IRunnable task);
	public static ICallable Callable (Java.Lang.IRunnable task, Java.Lang.Object result);
	public static IThreadFactory DefaultThreadFactory ();
	public static IExecutorService NewCachedThreadPool ();
	public static IExecutorService NewCachedThreadPool (IThreadFactory threadFactory);
	public static IExecutorService NewFixedThreadPool (int nThreads);
	public static IExecutorService NewFixedThreadPool (int nThreads, IThreadFactory threadFactory);
	public static IScheduledExecutorService NewScheduledThreadPool (int corePoolSize);
	public static IScheduledExecutorService NewScheduledThreadPool (int corePoolSize, IThreadFactory threadFactory);
	public static IExecutorService NewSingleThreadExecutor ();
	public static IExecutorService NewSingleThreadExecutor (IThreadFactory threadFactory);
	public static IScheduledExecutorService NewSingleThreadScheduledExecutor ();
	public static IScheduledExecutorService NewSingleThreadScheduledExecutor (IThreadFactory threadFactory);
	public static ICallable PrivilegedCallable (ICallable callable);
	public static ICallable PrivilegedCallableUsingCurrentClassLoader (ICallable callable);
	public static IThreadFactory PrivilegedThreadFactory ();
	public static IExecutorService UnconfigurableExecutorService (IExecutorService executor);
	public static IScheduledExecutorService UnconfigurableScheduledExecutorService (IScheduledExecutorService executor);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.FutureTask'>New Type: Java.Util.Concurrent.FutureTask</h3>

```
public class FutureTask : Java.Lang.Object, IFuture, Java.Lang.IRunnable, IRunnableFuture {
	
	protected FutureTask (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FutureTask (Java.Lang.IRunnable runnable, Java.Lang.Object result);
	public FutureTask (ICallable callable);
	
	public virtual bool Cancel (bool mayInterruptIfRunning);
	protected virtual void Done ();
	public virtual Java.Lang.Object Get ();
	public virtual Java.Lang.Object Get (long timeout, TimeUnit unit);
	public virtual void Run ();
	protected virtual bool RunAndReset ();
	protected virtual void Set (Java.Lang.Object v);
	protected virtual void SetException (Java.Lang.Throwable t);
	
	public virtual bool IsCancelled {
		get;
	}
	public virtual bool IsDone {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.IBlockingDeque'>New Type: Java.Util.Concurrent.IBlockingDeque</h3>

```
public interface IBlockingDeque : IBlockingQueue, Java.Util.ICollection, Java.Util.IDeque, IDisposable, Java.Lang.IIterable, Android.Runtime.IJavaObject, Java.Util.IQueue {
	
	bool Add (Java.Lang.Object e);
	void AddFirst (Java.Lang.Object e);
	void AddLast (Java.Lang.Object e);
	bool Contains (Java.Lang.Object o);
	Java.Lang.Object Element ();
	Java.Util.IIterator Iterator ();
	bool Offer (Java.Lang.Object e);
	bool Offer (Java.Lang.Object e, long timeout, TimeUnit unit);
	bool OfferFirst (Java.Lang.Object e);
	bool OfferFirst (Java.Lang.Object e, long timeout, TimeUnit unit);
	bool OfferLast (Java.Lang.Object e);
	bool OfferLast (Java.Lang.Object e, long timeout, TimeUnit unit);
	Java.Lang.Object Peek ();
	Java.Lang.Object Poll ();
	Java.Lang.Object Poll (long timeout, TimeUnit unit);
	Java.Lang.Object PollFirst (long timeout, TimeUnit unit);
	Java.Lang.Object PollLast (long timeout, TimeUnit unit);
	void Push (Java.Lang.Object e);
	void Put (Java.Lang.Object e);
	void PutFirst (Java.Lang.Object e);
	void PutLast (Java.Lang.Object e);
	Java.Lang.Object Remove ();
	bool Remove (Java.Lang.Object o);
	bool RemoveFirstOccurrence (Java.Lang.Object o);
	bool RemoveLastOccurrence (Java.Lang.Object o);
	int Size ();
	Java.Lang.Object Take ();
	Java.Lang.Object TakeFirst ();
	Java.Lang.Object TakeLast ();
}
```

<h3 id='Java.Util.Concurrent.IBlockingDequeExtensions'>New Type: Java.Util.Concurrent.IBlockingDequeExtensions</h3>

```
public static class IBlockingDequeExtensions {
	
	public static System.Threading.Tasks.Task OfferFirstAsync (IBlockingDeque self, Java.Lang.Object e);
	public static System.Threading.Tasks.Task OfferFirstAsync (IBlockingDeque self, Java.Lang.Object e, long timeout, TimeUnit unit);
	public static System.Threading.Tasks.Task OfferLastAsync (IBlockingDeque self, Java.Lang.Object e);
	public static System.Threading.Tasks.Task OfferLastAsync (IBlockingDeque self, Java.Lang.Object e, long timeout, TimeUnit unit);
	public static System.Threading.Tasks.Task PollFirstAsync (IBlockingDeque self, long timeout, TimeUnit unit);
	public static System.Threading.Tasks.Task PollLastAsync (IBlockingDeque self, long timeout, TimeUnit unit);
	public static System.Threading.Tasks.Task PutFirstAsync (IBlockingDeque self, Java.Lang.Object e);
	public static System.Threading.Tasks.Task PutLastAsync (IBlockingDeque self, Java.Lang.Object e);
	public static System.Threading.Tasks.Task TakeFirstAsync (IBlockingDeque self);
	public static System.Threading.Tasks.Task TakeLastAsync (IBlockingDeque self);
}
```

<h3 id='Java.Util.Concurrent.IBlockingQueue'>New Type: Java.Util.Concurrent.IBlockingQueue</h3>

```
public interface IBlockingQueue : Java.Util.ICollection, IDisposable, Java.Lang.IIterable, Android.Runtime.IJavaObject, Java.Util.IQueue {
	
	bool Add (Java.Lang.Object e);
	bool Contains (Java.Lang.Object o);
	int DrainTo (System.Collections.ICollection c);
	int DrainTo (System.Collections.ICollection c, int maxElements);
	bool Offer (Java.Lang.Object e);
	bool Offer (Java.Lang.Object e, long timeout, TimeUnit unit);
	Java.Lang.Object Poll (long timeout, TimeUnit unit);
	void Put (Java.Lang.Object e);
	int RemainingCapacity ();
	bool Remove (Java.Lang.Object o);
	Java.Lang.Object Take ();
}
```

<h3 id='Java.Util.Concurrent.IBlockingQueueExtensions'>New Type: Java.Util.Concurrent.IBlockingQueueExtensions</h3>

```
public static class IBlockingQueueExtensions {
	
	public static System.Threading.Tasks.Task OfferAsync (IBlockingQueue self, Java.Lang.Object e);
	public static System.Threading.Tasks.Task OfferAsync (IBlockingQueue self, Java.Lang.Object e, long timeout, TimeUnit unit);
	public static System.Threading.Tasks.Task PollAsync (IBlockingQueue self, long timeout, TimeUnit unit);
	public static System.Threading.Tasks.Task PutAsync (IBlockingQueue self, Java.Lang.Object e);
	public static System.Threading.Tasks.Task TakeAsync (IBlockingQueue self);
}
```

<h3 id='Java.Util.Concurrent.ICallable'>New Type: Java.Util.Concurrent.ICallable</h3>

```
public interface ICallable : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object Call ();
}
```

<h3 id='Java.Util.Concurrent.ICompletionService'>New Type: Java.Util.Concurrent.ICompletionService</h3>

```
public interface ICompletionService : IDisposable, Android.Runtime.IJavaObject {
	
	IFuture Poll ();
	IFuture Poll (long timeout, TimeUnit unit);
	IFuture Submit (ICallable task);
	IFuture Submit (Java.Lang.IRunnable task, Java.Lang.Object result);
	IFuture Take ();
}
```

<h3 id='Java.Util.Concurrent.IConcurrentMap'>New Type: Java.Util.Concurrent.IConcurrentMap</h3>

```
public interface IConcurrentMap : IDisposable, Android.Runtime.IJavaObject, Java.Util.IMap {
	
	Java.Lang.Object PutIfAbsent (Java.Lang.Object key, Java.Lang.Object value);
	bool Remove (Java.Lang.Object key, Java.Lang.Object value);
	Java.Lang.Object Replace (Java.Lang.Object key, Java.Lang.Object value);
	bool Replace (Java.Lang.Object key, Java.Lang.Object oldValue, Java.Lang.Object newValue);
}
```

<h3 id='Java.Util.Concurrent.IDelayed'>New Type: Java.Util.Concurrent.IDelayed</h3>

```
public interface IDelayed : Java.Lang.IComparable, IDisposable, Android.Runtime.IJavaObject {
	
	long GetDelay (TimeUnit unit);
}
```

<h3 id='Java.Util.Concurrent.IExecutor'>New Type: Java.Util.Concurrent.IExecutor</h3>

```
public interface IExecutor : IDisposable, Android.Runtime.IJavaObject {
	
	void Execute (Java.Lang.IRunnable command);
}
```

<h3 id='Java.Util.Concurrent.IExecutorService'>New Type: Java.Util.Concurrent.IExecutorService</h3>

```
public interface IExecutorService : IDisposable, IExecutor, Android.Runtime.IJavaObject {
	
	bool AwaitTermination (long timeout, TimeUnit unit);
	System.Collections.IList InvokeAll (System.Collections.ICollection p0);
	System.Collections.IList InvokeAll (System.Collections.ICollection p0, long p1, TimeUnit p2);
	Java.Lang.Object InvokeAny (System.Collections.ICollection p0);
	Java.Lang.Object InvokeAny (System.Collections.ICollection p0, long p1, TimeUnit p2);
	void Shutdown ();
	System.Collections.Generic.IList ShutdownNow ();
	IFuture Submit (ICallable task);
	IFuture Submit (Java.Lang.IRunnable task);
	IFuture Submit (Java.Lang.IRunnable task, Java.Lang.Object result);
	
	bool IsShutdown {
		get;
	}
	bool IsTerminated {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.IExecutorServiceExtensions'>New Type: Java.Util.Concurrent.IExecutorServiceExtensions</h3>

```
public static class IExecutorServiceExtensions {
	
	public static System.Threading.Tasks.Task AwaitTerminationAsync (IExecutorService self, long timeout, TimeUnit unit);
	public static System.Threading.Tasks.Task InvokeAnyAsync (IExecutorService self, System.Collections.ICollection p0);
	public static System.Threading.Tasks.Task InvokeAnyAsync (IExecutorService self, System.Collections.ICollection p0, long p1, TimeUnit p2);
}
```

<h3 id='Java.Util.Concurrent.IFuture'>New Type: Java.Util.Concurrent.IFuture</h3>

```
public interface IFuture : IDisposable, Android.Runtime.IJavaObject {
	
	bool Cancel (bool mayInterruptIfRunning);
	Java.Lang.Object Get ();
	Java.Lang.Object Get (long timeout, TimeUnit unit);
	
	bool IsCancelled {
		get;
	}
	bool IsDone {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.IFutureExtensions'>New Type: Java.Util.Concurrent.IFutureExtensions</h3>

```
public static class IFutureExtensions {
	
	public static System.Threading.Tasks.Task GetAsync (IFuture self);
	public static System.Threading.Tasks.Task GetAsync (IFuture self, long timeout, TimeUnit unit);
}
```

<h3 id='Java.Util.Concurrent.IRejectedExecutionHandler'>New Type: Java.Util.Concurrent.IRejectedExecutionHandler</h3>

```
public interface IRejectedExecutionHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void RejectedExecution (Java.Lang.IRunnable r, ThreadPoolExecutor executor);
}
```

<h3 id='Java.Util.Concurrent.IRunnableFuture'>New Type: Java.Util.Concurrent.IRunnableFuture</h3>

```
public interface IRunnableFuture : IDisposable, IFuture, Android.Runtime.IJavaObject, Java.Lang.IRunnable {
	
	void Run ();
}
```

<h3 id='Java.Util.Concurrent.IRunnableScheduledFuture'>New Type: Java.Util.Concurrent.IRunnableScheduledFuture</h3>

```
public interface IRunnableScheduledFuture : Java.Lang.IComparable, IDelayed, IDisposable, IFuture, Android.Runtime.IJavaObject, Java.Lang.IRunnable, IRunnableFuture, IScheduledFuture {
	
	bool IsPeriodic {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.IScheduledExecutorService'>New Type: Java.Util.Concurrent.IScheduledExecutorService</h3>

```
public interface IScheduledExecutorService : IDisposable, IExecutor, IExecutorService, Android.Runtime.IJavaObject {
	
	IScheduledFuture Schedule (ICallable callable, long delay, TimeUnit unit);
	IScheduledFuture Schedule (Java.Lang.IRunnable command, long delay, TimeUnit unit);
	IScheduledFuture ScheduleAtFixedRate (Java.Lang.IRunnable command, long initialDelay, long period, TimeUnit unit);
	IScheduledFuture ScheduleWithFixedDelay (Java.Lang.IRunnable command, long initialDelay, long delay, TimeUnit unit);
}
```

<h3 id='Java.Util.Concurrent.IScheduledFuture'>New Type: Java.Util.Concurrent.IScheduledFuture</h3>

```
public interface IScheduledFuture : Java.Lang.IComparable, IDelayed, IDisposable, IFuture, Android.Runtime.IJavaObject {
}
```

<h3 id='Java.Util.Concurrent.IThreadFactory'>New Type: Java.Util.Concurrent.IThreadFactory</h3>

```
public interface IThreadFactory : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Thread NewThread (Java.Lang.IRunnable r);
}
```

<h3 id='Java.Util.Concurrent.LinkedBlockingDeque'>New Type: Java.Util.Concurrent.LinkedBlockingDeque</h3>

```
public class LinkedBlockingDeque : Java.Util.AbstractQueue, IBlockingDeque, IBlockingQueue, Java.Util.IDeque, Java.IO.ISerializable {
	
	protected LinkedBlockingDeque (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LinkedBlockingDeque ();
	public LinkedBlockingDeque (int capacity);
	public LinkedBlockingDeque (System.Collections.ICollection c);
	
	public virtual void AddFirst (Java.Lang.Object e);
	public virtual void AddLast (Java.Lang.Object e);
	public virtual Java.Util.IIterator DescendingIterator ();
	public virtual int DrainTo (System.Collections.ICollection c);
	public virtual int DrainTo (System.Collections.ICollection c, int maxElements);
	public override Java.Util.IIterator Iterator ();
	public override bool Offer (Java.Lang.Object e);
	public virtual bool Offer (Java.Lang.Object e, long timeout, TimeUnit unit);
	public virtual bool OfferFirst (Java.Lang.Object e);
	public virtual bool OfferFirst (Java.Lang.Object e, long timeout, TimeUnit unit);
	public virtual bool OfferLast (Java.Lang.Object e);
	public virtual bool OfferLast (Java.Lang.Object e, long timeout, TimeUnit unit);
	public override Java.Lang.Object Peek ();
	public virtual Java.Lang.Object PeekFirst ();
	public virtual Java.Lang.Object PeekLast ();
	public override Java.Lang.Object Poll ();
	public virtual Java.Lang.Object Poll (long timeout, TimeUnit unit);
	public virtual Java.Lang.Object PollFirst ();
	public virtual Java.Lang.Object PollFirst (long timeout, TimeUnit unit);
	public virtual Java.Lang.Object PollLast ();
	public virtual Java.Lang.Object PollLast (long timeout, TimeUnit unit);
	public virtual Java.Lang.Object Pop ();
	public virtual void Push (Java.Lang.Object e);
	public virtual void Put (Java.Lang.Object e);
	public virtual void PutFirst (Java.Lang.Object e);
	public virtual void PutLast (Java.Lang.Object e);
	public virtual int RemainingCapacity ();
	public virtual Java.Lang.Object RemoveFirst ();
	public virtual bool RemoveFirstOccurrence (Java.Lang.Object o);
	public virtual Java.Lang.Object RemoveLast ();
	public virtual bool RemoveLastOccurrence (Java.Lang.Object o);
	public override int Size ();
	public virtual Java.Lang.Object Take ();
	public virtual Java.Lang.Object TakeFirst ();
	public virtual Java.Lang.Object TakeLast ();
	
	public virtual Java.Lang.Object First {
		get;
	}
	public virtual Java.Lang.Object Last {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.LinkedBlockingQueue'>New Type: Java.Util.Concurrent.LinkedBlockingQueue</h3>

```
public class LinkedBlockingQueue : Java.Util.AbstractQueue, IBlockingQueue, Java.IO.ISerializable {
	
	protected LinkedBlockingQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LinkedBlockingQueue ();
	public LinkedBlockingQueue (int capacity);
	public LinkedBlockingQueue (System.Collections.ICollection c);
	
	public virtual int DrainTo (System.Collections.ICollection c);
	public virtual int DrainTo (System.Collections.ICollection c, int maxElements);
	public override Java.Util.IIterator Iterator ();
	public override bool Offer (Java.Lang.Object e);
	public virtual bool Offer (Java.Lang.Object e, long timeout, TimeUnit unit);
	public override Java.Lang.Object Peek ();
	public override Java.Lang.Object Poll ();
	public virtual Java.Lang.Object Poll (long timeout, TimeUnit unit);
	public virtual void Put (Java.Lang.Object e);
	public virtual int RemainingCapacity ();
	public override int Size ();
	public virtual Java.Lang.Object Take ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.PriorityBlockingQueue'>New Type: Java.Util.Concurrent.PriorityBlockingQueue</h3>

```
public class PriorityBlockingQueue : Java.Util.AbstractQueue, IBlockingQueue, Java.IO.ISerializable {
	
	protected PriorityBlockingQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PriorityBlockingQueue ();
	public PriorityBlockingQueue (int initialCapacity);
	public PriorityBlockingQueue (int initialCapacity, Java.Util.IComparator comparator);
	public PriorityBlockingQueue (System.Collections.ICollection c);
	
	public virtual Java.Util.IComparator Comparator ();
	public virtual int DrainTo (System.Collections.ICollection c);
	public virtual int DrainTo (System.Collections.ICollection c, int maxElements);
	public override Java.Util.IIterator Iterator ();
	public override bool Offer (Java.Lang.Object e);
	public virtual bool Offer (Java.Lang.Object e, long timeout, TimeUnit unit);
	public override Java.Lang.Object Peek ();
	public override Java.Lang.Object Poll ();
	public virtual Java.Lang.Object Poll (long timeout, TimeUnit unit);
	public virtual void Put (Java.Lang.Object e);
	public virtual int RemainingCapacity ();
	public override int Size ();
	public virtual Java.Lang.Object Take ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.RejectedExecutionException'>New Type: Java.Util.Concurrent.RejectedExecutionException</h3>

```
public class RejectedExecutionException : Java.Lang.RuntimeException {
	
	protected RejectedExecutionException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RejectedExecutionException ();
	public RejectedExecutionException (string message);
	public RejectedExecutionException (string message, Java.Lang.Throwable cause);
	public RejectedExecutionException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.ScheduledThreadPoolExecutor'>New Type: Java.Util.Concurrent.ScheduledThreadPoolExecutor</h3>

```
public class ScheduledThreadPoolExecutor : ThreadPoolExecutor, IScheduledExecutorService {
	
	protected ScheduledThreadPoolExecutor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ScheduledThreadPoolExecutor (int corePoolSize);
	public ScheduledThreadPoolExecutor (int corePoolSize, IRejectedExecutionHandler handler);
	public ScheduledThreadPoolExecutor (int corePoolSize, IThreadFactory threadFactory);
	public ScheduledThreadPoolExecutor (int corePoolSize, IThreadFactory threadFactory, IRejectedExecutionHandler handler);
	
	protected virtual IRunnableScheduledFuture DecorateTask (ICallable p0, IRunnableScheduledFuture p1);
	protected virtual IRunnableScheduledFuture DecorateTask (Java.Lang.IRunnable p0, IRunnableScheduledFuture p1);
	public virtual IScheduledFuture Schedule (ICallable callable, long delay, TimeUnit unit);
	public virtual IScheduledFuture Schedule (Java.Lang.IRunnable command, long delay, TimeUnit unit);
	public virtual IScheduledFuture ScheduleAtFixedRate (Java.Lang.IRunnable command, long initialDelay, long period, TimeUnit unit);
	public virtual IScheduledFuture ScheduleWithFixedDelay (Java.Lang.IRunnable command, long initialDelay, long delay, TimeUnit unit);
	
	public virtual bool ContinueExistingPeriodicTasksAfterShutdownPolicy {
		get;
		set;
	}
	public virtual bool ExecuteExistingDelayedTasksAfterShutdownPolicy {
		get;
		set;
	}
	public virtual bool RemoveOnCancelPolicy {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Semaphore'>New Type: Java.Util.Concurrent.Semaphore</h3>

```
public class Semaphore : Java.Lang.Object, Java.IO.ISerializable {
	
	protected Semaphore (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Semaphore (int permits);
	public Semaphore (int permits, bool fair);
	
	public virtual void Acquire ();
	public virtual void Acquire (int permits);
	public virtual void AcquireUninterruptibly ();
	public virtual void AcquireUninterruptibly (int permits);
	public virtual int AvailablePermits ();
	public virtual int DrainPermits ();
	protected virtual void ReducePermits (int reduction);
	public virtual void Release ();
	public virtual void Release (int permits);
	public virtual bool TryAcquire ();
	public virtual bool TryAcquire (int permits);
	public virtual bool TryAcquire (int permits, long timeout, TimeUnit unit);
	public virtual bool TryAcquire (long timeout, TimeUnit unit);
	
	public bool HasQueuedThreads {
		get;
	}
	public virtual bool IsFair {
		get;
	}
	protected virtual System.Collections.Generic.ICollection QueuedThreads {
		get;
	}
	public int QueueLength {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.SynchronousQueue'>New Type: Java.Util.Concurrent.SynchronousQueue</h3>

```
public class SynchronousQueue : Java.Util.AbstractQueue, IBlockingQueue, Java.IO.ISerializable {
	
	protected SynchronousQueue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SynchronousQueue ();
	public SynchronousQueue (bool fair);
	
	public virtual int DrainTo (System.Collections.ICollection c);
	public virtual int DrainTo (System.Collections.ICollection c, int maxElements);
	public override Java.Util.IIterator Iterator ();
	public override bool Offer (Java.Lang.Object e);
	public virtual bool Offer (Java.Lang.Object o, long timeout, TimeUnit unit);
	public override Java.Lang.Object Peek ();
	public override Java.Lang.Object Poll ();
	public virtual Java.Lang.Object Poll (long timeout, TimeUnit unit);
	public virtual void Put (Java.Lang.Object o);
	public virtual int RemainingCapacity ();
	public override int Size ();
	public virtual Java.Lang.Object Take ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.ThreadPoolExecutor'>New Type: Java.Util.Concurrent.ThreadPoolExecutor</h3>

```
public class ThreadPoolExecutor : AbstractExecutorService {
	
	protected ThreadPoolExecutor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ThreadPoolExecutor (int corePoolSize, int maximumPoolSize, long keepAliveTime, TimeUnit unit, IBlockingQueue workQueue);
	public ThreadPoolExecutor (int corePoolSize, int maximumPoolSize, long keepAliveTime, TimeUnit unit, IBlockingQueue workQueue, IRejectedExecutionHandler handler);
	public ThreadPoolExecutor (int corePoolSize, int maximumPoolSize, long keepAliveTime, TimeUnit unit, IBlockingQueue workQueue, IThreadFactory threadFactory);
	public ThreadPoolExecutor (int corePoolSize, int maximumPoolSize, long keepAliveTime, TimeUnit unit, IBlockingQueue workQueue, IThreadFactory threadFactory, IRejectedExecutionHandler handler);
	
	protected virtual void AfterExecute (Java.Lang.IRunnable r, Java.Lang.Throwable t);
	public virtual void AllowCoreThreadTimeOut (bool p0);
	public virtual bool AllowsCoreThreadTimeOut ();
	public override bool AwaitTermination (long timeout, TimeUnit unit);
	protected virtual void BeforeExecute (Java.Lang.Thread t, Java.Lang.IRunnable r);
	public override void Execute (Java.Lang.IRunnable command);
	public virtual long GetKeepAliveTime (TimeUnit unit);
	public virtual int PrestartAllCoreThreads ();
	public virtual bool PrestartCoreThread ();
	public virtual void Purge ();
	public virtual bool Remove (Java.Lang.IRunnable task);
	public virtual void SetKeepAliveTime (long time, TimeUnit unit);
	public override void Shutdown ();
	public override System.Collections.Generic.IList ShutdownNow ();
	protected virtual void Terminated ();
	
	public virtual int ActiveCount {
		get;
	}
	public virtual long CompletedTaskCount {
		get;
	}
	public virtual int CorePoolSize {
		get;
		set;
	}
	public override bool IsShutdown {
		get;
	}
	public override bool IsTerminated {
		get;
	}
	public virtual bool IsTerminating {
		get;
	}
	public virtual int LargestPoolSize {
		get;
	}
	public virtual int MaximumPoolSize {
		get;
		set;
	}
	public virtual int PoolSize {
		get;
	}
	public virtual IBlockingQueue Queue {
		get;
	}
	public virtual IRejectedExecutionHandler RejectedExecutionHandler {
		get;
		set;
	}
	public virtual long TaskCount {
		get;
	}
	public virtual IThreadFactory ThreadFactory {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class AbortPolicy : Java.Lang.Object, IRejectedExecutionHandler {
		
		protected AbortPolicy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public AbortPolicy ();
		
		public virtual void RejectedExecution (Java.Lang.IRunnable r, ThreadPoolExecutor e);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class CallerRunsPolicy : Java.Lang.Object, IRejectedExecutionHandler {
		
		protected CallerRunsPolicy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public CallerRunsPolicy ();
		
		public virtual void RejectedExecution (Java.Lang.IRunnable r, ThreadPoolExecutor e);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class DiscardOldestPolicy : Java.Lang.Object, IRejectedExecutionHandler {
		
		protected DiscardOldestPolicy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public DiscardOldestPolicy ();
		
		public virtual void RejectedExecution (Java.Lang.IRunnable r, ThreadPoolExecutor e);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class DiscardPolicy : Java.Lang.Object, IRejectedExecutionHandler {
		
		protected DiscardPolicy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public DiscardPolicy ();
		
		public virtual void RejectedExecution (Java.Lang.IRunnable r, ThreadPoolExecutor e);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Java.Util.Concurrent.TimeoutException'>New Type: Java.Util.Concurrent.TimeoutException</h3>

```
public class TimeoutException : Java.Lang.Exception {
	
	protected TimeoutException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TimeoutException ();
	public TimeoutException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Java.Util.Concurrent.Atomic'>Namespace: Java.Util.Concurrent.Atomic</h2>

<h3 id='Java.Util.Concurrent.Atomic.AtomicBoolean'>New Type: Java.Util.Concurrent.Atomic.AtomicBoolean</h3>

```
public class AtomicBoolean : Java.Lang.Object, Java.IO.ISerializable {
	
	protected AtomicBoolean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicBoolean ();
	public AtomicBoolean (bool initialValue);
	
	public bool CompareAndSet (bool expect, bool update);
	public bool Get ();
	public bool GetAndSet (bool newValue);
	public void LazySet (bool p0);
	public void Set (bool newValue);
	public virtual bool WeakCompareAndSet (bool expect, bool update);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicInteger'>New Type: Java.Util.Concurrent.Atomic.AtomicInteger</h3>

```
public class AtomicInteger : Java.Lang.Number {
	
	protected AtomicInteger (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicInteger ();
	public AtomicInteger (int initialValue);
	
	public int AddAndGet (int delta);
	public bool CompareAndSet (int expect, int update);
	public int DecrementAndGet ();
	public override double DoubleValue ();
	public override float FloatValue ();
	public int Get ();
	public int GetAndAdd (int delta);
	public int GetAndSet (int newValue);
	public int IncrementAndGet ();
	public override int IntValue ();
	public void LazySet (int p0);
	public override long LongValue ();
	public void Set (int newValue);
	public bool WeakCompareAndSet (int expect, int update);
	
	public int AndDecrement {
		get;
	}
	public int AndIncrement {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicIntegerArray'>New Type: Java.Util.Concurrent.Atomic.AtomicIntegerArray</h3>

```
public class AtomicIntegerArray : Java.Lang.Object, Java.IO.ISerializable {
	
	protected AtomicIntegerArray (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicIntegerArray (int length);
	public AtomicIntegerArray (int [] array);
	
	public int AddAndGet (int i, int delta);
	public bool CompareAndSet (int i, int expect, int update);
	public int DecrementAndGet (int i);
	public int Get (int i);
	public int GetAndAdd (int i, int delta);
	public int GetAndDecrement (int i);
	public int GetAndIncrement (int i);
	public int GetAndSet (int i, int newValue);
	public int IncrementAndGet (int i);
	public void LazySet (int p0, int p1);
	public int Length ();
	public void Set (int i, int newValue);
	public bool WeakCompareAndSet (int i, int expect, int update);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicIntegerFieldUpdater'>New Type: Java.Util.Concurrent.Atomic.AtomicIntegerFieldUpdater</h3>

```
public abstract class AtomicIntegerFieldUpdater : Java.Lang.Object {
	
	protected AtomicIntegerFieldUpdater (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AtomicIntegerFieldUpdater ();
	
	public static AtomicIntegerFieldUpdater NewUpdater (Java.Lang.Class tclass, string fieldName);
	public virtual int AddAndGet (Java.Lang.Object obj, int delta);
	public abstract bool CompareAndSet (Java.Lang.Object obj, int expect, int update);
	public virtual int DecrementAndGet (Java.Lang.Object obj);
	public abstract int Get (Java.Lang.Object obj);
	public virtual int GetAndAdd (Java.Lang.Object obj, int delta);
	public virtual int GetAndDecrement (Java.Lang.Object obj);
	public virtual int GetAndIncrement (Java.Lang.Object obj);
	public virtual int GetAndSet (Java.Lang.Object obj, int newValue);
	public virtual int IncrementAndGet (Java.Lang.Object obj);
	public abstract void LazySet (Java.Lang.Object p0, int p1);
	public abstract void Set (Java.Lang.Object obj, int newValue);
	public abstract bool WeakCompareAndSet (Java.Lang.Object obj, int expect, int update);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicLong'>New Type: Java.Util.Concurrent.Atomic.AtomicLong</h3>

```
public class AtomicLong : Java.Lang.Number {
	
	protected AtomicLong (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicLong ();
	public AtomicLong (long initialValue);
	
	public long AddAndGet (long delta);
	public bool CompareAndSet (long expect, long update);
	public long DecrementAndGet ();
	public override double DoubleValue ();
	public override float FloatValue ();
	public long Get ();
	public long GetAndAdd (long delta);
	public long GetAndSet (long newValue);
	public long IncrementAndGet ();
	public override int IntValue ();
	public void LazySet (long p0);
	public override long LongValue ();
	public void Set (long newValue);
	public bool WeakCompareAndSet (long expect, long update);
	
	public long AndDecrement {
		get;
	}
	public long AndIncrement {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicLongArray'>New Type: Java.Util.Concurrent.Atomic.AtomicLongArray</h3>

```
public class AtomicLongArray : Java.Lang.Object, Java.IO.ISerializable {
	
	protected AtomicLongArray (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicLongArray (int length);
	public AtomicLongArray (long [] array);
	
	public virtual long AddAndGet (int i, long delta);
	public bool CompareAndSet (int i, long expect, long update);
	public long DecrementAndGet (int i);
	public long Get (int i);
	public long GetAndAdd (int i, long delta);
	public long GetAndDecrement (int i);
	public long GetAndIncrement (int i);
	public long GetAndSet (int i, long newValue);
	public long IncrementAndGet (int i);
	public void LazySet (int p0, long p1);
	public int Length ();
	public void Set (int i, long newValue);
	public bool WeakCompareAndSet (int i, long expect, long update);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicLongFieldUpdater'>New Type: Java.Util.Concurrent.Atomic.AtomicLongFieldUpdater</h3>

```
public abstract class AtomicLongFieldUpdater : Java.Lang.Object {
	
	protected AtomicLongFieldUpdater (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AtomicLongFieldUpdater ();
	
	public static AtomicLongFieldUpdater NewUpdater (Java.Lang.Class tclass, string fieldName);
	public virtual long AddAndGet (Java.Lang.Object obj, long delta);
	public abstract bool CompareAndSet (Java.Lang.Object obj, long expect, long update);
	public virtual long DecrementAndGet (Java.Lang.Object obj);
	public abstract long Get (Java.Lang.Object obj);
	public virtual long GetAndAdd (Java.Lang.Object obj, long delta);
	public virtual long GetAndDecrement (Java.Lang.Object obj);
	public virtual long GetAndIncrement (Java.Lang.Object obj);
	public virtual long GetAndSet (Java.Lang.Object obj, long newValue);
	public virtual long IncrementAndGet (Java.Lang.Object obj);
	public abstract void LazySet (Java.Lang.Object p0, long p1);
	public abstract void Set (Java.Lang.Object obj, long newValue);
	public abstract bool WeakCompareAndSet (Java.Lang.Object obj, long expect, long update);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicMarkableReference'>New Type: Java.Util.Concurrent.Atomic.AtomicMarkableReference</h3>

```
public class AtomicMarkableReference : Java.Lang.Object {
	
	protected AtomicMarkableReference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicMarkableReference (Java.Lang.Object initialRef, bool initialMark);
	
	public virtual bool AttemptMark (Java.Lang.Object expectedReference, bool newMark);
	public virtual bool CompareAndSet (Java.Lang.Object expectedReference, Java.Lang.Object newReference, bool expectedMark, bool newMark);
	public virtual Java.Lang.Object Get (bool [] markHolder);
	public virtual void Set (Java.Lang.Object newReference, bool newMark);
	public virtual bool WeakCompareAndSet (Java.Lang.Object expectedReference, Java.Lang.Object newReference, bool expectedMark, bool newMark);
	
	public virtual bool IsMarked {
		get;
	}
	public virtual Java.Lang.Object Reference {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicReference'>New Type: Java.Util.Concurrent.Atomic.AtomicReference</h3>

```
public class AtomicReference : Java.Lang.Object, Java.IO.ISerializable {
	
	protected AtomicReference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicReference ();
	public AtomicReference (Java.Lang.Object initialValue);
	
	public bool CompareAndSet (Java.Lang.Object expect, Java.Lang.Object update);
	public Java.Lang.Object Get ();
	public Java.Lang.Object GetAndSet (Java.Lang.Object newValue);
	public void LazySet (Java.Lang.Object p0);
	public void Set (Java.Lang.Object newValue);
	public bool WeakCompareAndSet (Java.Lang.Object expect, Java.Lang.Object update);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicReferenceArray'>New Type: Java.Util.Concurrent.Atomic.AtomicReferenceArray</h3>

```
public class AtomicReferenceArray : Java.Lang.Object, Java.IO.ISerializable {
	
	protected AtomicReferenceArray (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicReferenceArray (Java.Lang.Object[] array);
	public AtomicReferenceArray (int length);
	
	public bool CompareAndSet (int i, Java.Lang.Object expect, Java.Lang.Object update);
	public Java.Lang.Object Get (int i);
	public Java.Lang.Object GetAndSet (int i, Java.Lang.Object newValue);
	public void LazySet (int p0, Java.Lang.Object p1);
	public int Length ();
	public void Set (int i, Java.Lang.Object newValue);
	public bool WeakCompareAndSet (int i, Java.Lang.Object expect, Java.Lang.Object update);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicReferenceFieldUpdater'>New Type: Java.Util.Concurrent.Atomic.AtomicReferenceFieldUpdater</h3>

```
public abstract class AtomicReferenceFieldUpdater : Java.Lang.Object {
	
	protected AtomicReferenceFieldUpdater (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AtomicReferenceFieldUpdater ();
	
	public static AtomicReferenceFieldUpdater NewUpdater (Java.Lang.Class tclass, Java.Lang.Class vclass, string fieldName);
	public abstract bool CompareAndSet (Java.Lang.Object obj, Java.Lang.Object expect, Java.Lang.Object update);
	public abstract Java.Lang.Object Get (Java.Lang.Object obj);
	public virtual Java.Lang.Object GetAndSet (Java.Lang.Object obj, Java.Lang.Object newValue);
	public abstract void LazySet (Java.Lang.Object p0, Java.Lang.Object p1);
	public abstract void Set (Java.Lang.Object obj, Java.Lang.Object newValue);
	public abstract bool WeakCompareAndSet (Java.Lang.Object obj, Java.Lang.Object expect, Java.Lang.Object update);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Atomic.AtomicStampedReference'>New Type: Java.Util.Concurrent.Atomic.AtomicStampedReference</h3>

```
public class AtomicStampedReference : Java.Lang.Object {
	
	protected AtomicStampedReference (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AtomicStampedReference (Java.Lang.Object initialRef, int initialStamp);
	
	public virtual bool AttemptStamp (Java.Lang.Object expectedReference, int newStamp);
	public virtual bool CompareAndSet (Java.Lang.Object expectedReference, Java.Lang.Object newReference, int expectedStamp, int newStamp);
	public virtual Java.Lang.Object Get (int [] stampHolder);
	public virtual void Set (Java.Lang.Object newReference, int newStamp);
	public virtual bool WeakCompareAndSet (Java.Lang.Object expectedReference, Java.Lang.Object newReference, int expectedStamp, int newStamp);
	
	public virtual Java.Lang.Object Reference {
		get;
	}
	public virtual int Stamp {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Java.Util.Concurrent.Locks'>Namespace: Java.Util.Concurrent.Locks</h2>

<h3 id='Java.Util.Concurrent.Locks.AbstractOwnableSynchronizer'>New Type: Java.Util.Concurrent.Locks.AbstractOwnableSynchronizer</h3>

```
public abstract class AbstractOwnableSynchronizer : Java.Lang.Object, Java.IO.ISerializable {
	
	protected AbstractOwnableSynchronizer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractOwnableSynchronizer ();
	
	protected Java.Lang.Thread ExclusiveOwnerThread {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Locks.AbstractQueuedLongSynchronizer'>New Type: Java.Util.Concurrent.Locks.AbstractQueuedLongSynchronizer</h3>

```
public abstract class AbstractQueuedLongSynchronizer : AbstractOwnableSynchronizer {
	
	protected AbstractQueuedLongSynchronizer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractQueuedLongSynchronizer ();
	
	public void Acquire (long arg);
	public void AcquireInterruptibly (long arg);
	public void AcquireShared (long arg);
	public void AcquireSharedInterruptibly (long arg);
	protected bool CompareAndSetState (long expect, long update);
	public System.Collections.Generic.ICollection GetWaitingThreads (ConditionObject condition);
	public int GetWaitQueueLength (ConditionObject condition);
	public bool HasWaiters (ConditionObject condition);
	public bool IsQueued (Java.Lang.Thread thread);
	public bool Owns (ConditionObject condition);
	public bool Release (long arg);
	public bool ReleaseShared (long arg);
	protected virtual bool TryAcquire (long arg);
	public bool TryAcquireNanos (long arg, long nanosTimeout);
	protected virtual long TryAcquireShared (long arg);
	public bool TryAcquireSharedNanos (long arg, long nanosTimeout);
	protected virtual bool TryRelease (long arg);
	protected virtual bool TryReleaseShared (long arg);
	
	public System.Collections.Generic.ICollection ExclusiveQueuedThreads {
		get;
	}
	public Java.Lang.Thread FirstQueuedThread {
		get;
	}
	public bool HasContended {
		get;
	}
	public bool HasQueuedPredecessors {
		get;
	}
	public bool HasQueuedThreads {
		get;
	}
	protected virtual bool IsHeldExclusively {
		get;
	}
	public System.Collections.Generic.ICollection QueuedThreads {
		get;
	}
	public int QueueLength {
		get;
	}
	public System.Collections.Generic.ICollection SharedQueuedThreads {
		get;
	}
	protected long State {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class ConditionObject : Java.Lang.Object, ICondition, Java.IO.ISerializable {
		
		protected ConditionObject (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public ConditionObject (AbstractQueuedLongSynchronizer __self);
		
		public void Await ();
		public bool Await (long time, Java.Util.Concurrent.TimeUnit unit);
		public long AwaitNanos (long nanosTimeout);
		public void AwaitUninterruptibly ();
		public bool AwaitUntil (Java.Util.Date deadline);
		public void Signal ();
		public void SignalAll ();
		
		protected bool HasWaiters {
			get;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
		protected System.Collections.Generic.ICollection WaitingThreads {
			get;
		}
		protected int WaitQueueLength {
			get;
		}
	}
}
```

<h3 id='Java.Util.Concurrent.Locks.AbstractQueuedSynchronizer'>New Type: Java.Util.Concurrent.Locks.AbstractQueuedSynchronizer</h3>

```
public abstract class AbstractQueuedSynchronizer : AbstractOwnableSynchronizer {
	
	protected AbstractQueuedSynchronizer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractQueuedSynchronizer ();
	
	public void Acquire (int arg);
	public void AcquireInterruptibly (int arg);
	public void AcquireShared (int arg);
	public void AcquireSharedInterruptibly (int arg);
	protected bool CompareAndSetState (int expect, int update);
	public System.Collections.Generic.ICollection GetWaitingThreads (ConditionObject condition);
	public int GetWaitQueueLength (ConditionObject condition);
	public bool HasWaiters (ConditionObject condition);
	public bool IsQueued (Java.Lang.Thread thread);
	public bool Owns (ConditionObject condition);
	public bool Release (int arg);
	public bool ReleaseShared (int arg);
	protected virtual bool TryAcquire (int arg);
	public bool TryAcquireNanos (int arg, long nanosTimeout);
	protected virtual int TryAcquireShared (int arg);
	public bool TryAcquireSharedNanos (int arg, long nanosTimeout);
	protected virtual bool TryRelease (int arg);
	protected virtual bool TryReleaseShared (int arg);
	
	public System.Collections.Generic.ICollection ExclusiveQueuedThreads {
		get;
	}
	public Java.Lang.Thread FirstQueuedThread {
		get;
	}
	public bool HasContended {
		get;
	}
	public bool HasQueuedPredecessors {
		get;
	}
	public bool HasQueuedThreads {
		get;
	}
	protected virtual bool IsHeldExclusively {
		get;
	}
	public System.Collections.Generic.ICollection QueuedThreads {
		get;
	}
	public int QueueLength {
		get;
	}
	public System.Collections.Generic.ICollection SharedQueuedThreads {
		get;
	}
	protected int State {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class ConditionObject : Java.Lang.Object, ICondition, Java.IO.ISerializable {
		
		protected ConditionObject (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public ConditionObject (AbstractQueuedSynchronizer __self);
		
		public void Await ();
		public bool Await (long time, Java.Util.Concurrent.TimeUnit unit);
		public long AwaitNanos (long nanosTimeout);
		public void AwaitUninterruptibly ();
		public bool AwaitUntil (Java.Util.Date deadline);
		public void Signal ();
		public void SignalAll ();
		
		protected bool HasWaiters {
			get;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
		protected System.Collections.Generic.ICollection WaitingThreads {
			get;
		}
		protected int WaitQueueLength {
			get;
		}
	}
}
```

<h3 id='Java.Util.Concurrent.Locks.ICondition'>New Type: Java.Util.Concurrent.Locks.ICondition</h3>

```
public interface ICondition : IDisposable, Android.Runtime.IJavaObject {
	
	void Await ();
	bool Await (long time, Java.Util.Concurrent.TimeUnit unit);
	long AwaitNanos (long nanosTimeout);
	void AwaitUninterruptibly ();
	bool AwaitUntil (Java.Util.Date deadline);
	void Signal ();
	void SignalAll ();
}
```

<h3 id='Java.Util.Concurrent.Locks.ILock'>New Type: Java.Util.Concurrent.Locks.ILock</h3>

```
public interface ILock : IDisposable, Android.Runtime.IJavaObject {
	
	void Lock ();
	void LockInterruptibly ();
	ICondition NewCondition ();
	bool TryLock ();
	bool TryLock (long time, Java.Util.Concurrent.TimeUnit unit);
	void Unlock ();
}
```

<h3 id='Java.Util.Concurrent.Locks.IReadWriteLock'>New Type: Java.Util.Concurrent.Locks.IReadWriteLock</h3>

```
public interface IReadWriteLock : IDisposable, Android.Runtime.IJavaObject {
	
	ILock ReadLock ();
	ILock WriteLock ();
}
```

<h3 id='Java.Util.Concurrent.Locks.LockSupport'>New Type: Java.Util.Concurrent.Locks.LockSupport</h3>

```
public class LockSupport : Java.Lang.Object {
	
	protected LockSupport (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static Java.Lang.Object GetBlocker (Java.Lang.Thread p0);
	public static void Park ();
	public static void Park (Java.Lang.Object p0);
	public static void ParkNanos (long nanos);
	public static void ParkNanos (Java.Lang.Object p0, long p1);
	public static void ParkUntil (long deadline);
	public static void ParkUntil (Java.Lang.Object p0, long p1);
	public static void Unpark (Java.Lang.Thread thread);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Locks.ReentrantLock'>New Type: Java.Util.Concurrent.Locks.ReentrantLock</h3>

```
public class ReentrantLock : Java.Lang.Object, ILock, Java.IO.ISerializable {
	
	protected ReentrantLock (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ReentrantLock ();
	public ReentrantLock (bool fair);
	
	protected virtual System.Collections.Generic.ICollection GetWaitingThreads (ICondition condition);
	public virtual int GetWaitQueueLength (ICondition condition);
	public bool HasQueuedThread (Java.Lang.Thread thread);
	public virtual bool HasWaiters (ICondition condition);
	public virtual void Lock ();
	public virtual void LockInterruptibly ();
	public virtual ICondition NewCondition ();
	public virtual bool TryLock ();
	public virtual bool TryLock (long timeout, Java.Util.Concurrent.TimeUnit unit);
	public virtual void Unlock ();
	
	public bool HasQueuedThreads {
		get;
	}
	public virtual int HoldCount {
		get;
	}
	public bool IsFair {
		get;
	}
	public virtual bool IsHeldByCurrentThread {
		get;
	}
	public virtual bool IsLocked {
		get;
	}
	protected virtual Java.Lang.Thread Owner {
		get;
	}
	protected virtual System.Collections.Generic.ICollection QueuedThreads {
		get;
	}
	public int QueueLength {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Concurrent.Locks.ReentrantReadWriteLock'>New Type: Java.Util.Concurrent.Locks.ReentrantReadWriteLock</h3>

```
public class ReentrantReadWriteLock : Java.Lang.Object, IReadWriteLock, Java.IO.ISerializable {
	
	protected ReentrantReadWriteLock (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ReentrantReadWriteLock ();
	public ReentrantReadWriteLock (bool fair);
	
	protected virtual System.Collections.Generic.ICollection GetWaitingThreads (ICondition condition);
	public virtual int GetWaitQueueLength (ICondition condition);
	public bool HasQueuedThread (Java.Lang.Thread thread);
	public virtual bool HasWaiters (ICondition condition);
	public virtual ILock ReadLock ();
	public virtual ILock WriteLock ();
	
	public bool HasQueuedThreads {
		get;
	}
	public bool IsFair {
		get;
	}
	public virtual bool IsWriteLocked {
		get;
	}
	public virtual bool IsWriteLockedByCurrentThread {
		get;
	}
	protected virtual Java.Lang.Thread Owner {
		get;
	}
	protected virtual System.Collections.Generic.ICollection QueuedReaderThreads {
		get;
	}
	protected virtual System.Collections.Generic.ICollection QueuedThreads {
		get;
	}
	protected virtual System.Collections.Generic.ICollection QueuedWriterThreads {
		get;
	}
	public int QueueLength {
		get;
	}
	public virtual int ReadHoldCount {
		get;
	}
	public virtual int ReadLockCount {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual int WriteHoldCount {
		get;
	}
	
	public class ReentrantReadLock : Java.Lang.Object, ILock, Java.IO.ISerializable {
		
		protected ReentrantReadLock (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		protected ReentrantReadLock (ReentrantReadWriteLock lock);
		
		public virtual void Lock ();
		public virtual void LockInterruptibly ();
		public virtual ICondition NewCondition ();
		public virtual bool TryLock ();
		public virtual bool TryLock (long timeout, Java.Util.Concurrent.TimeUnit unit);
		public virtual void Unlock ();
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class ReentrantWriteLock : Java.Lang.Object, ILock, Java.IO.ISerializable {
		
		protected ReentrantWriteLock (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		protected ReentrantWriteLock (ReentrantReadWriteLock lock);
		
		public virtual void Lock ();
		public virtual void LockInterruptibly ();
		public virtual ICondition NewCondition ();
		public virtual bool TryLock ();
		public virtual bool TryLock (long timeout, Java.Util.Concurrent.TimeUnit unit);
		public virtual void Unlock ();
		
		public virtual int HoldCount {
			get;
		}
		public virtual bool IsHeldByCurrentThread {
			get;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h2 id='Java.Util.Jar'>Namespace: Java.Util.Jar</h2>

<h3 id='Java.Util.Jar.Attributes'>New Type: Java.Util.Jar.Attributes</h3>

```
public class Attributes : Java.Lang.Object, Java.Lang.ICloneable, Java.Util.IMap {
	
	protected Attributes (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Attributes ();
	public Attributes (int size);
	public Attributes (Attributes attrib);
	
	public virtual void Clear ();
	public virtual Java.Lang.Object Clone ();
	public virtual bool ContainsKey (Java.Lang.Object key);
	public virtual bool ContainsValue (Java.Lang.Object value);
	public virtual System.Collections.ICollection EntrySet ();
	public virtual Java.Lang.Object Get (Java.Lang.Object key);
	public virtual string GetValue (Name name);
	public virtual string GetValue (string name);
	bool Java.Util.IMap.ContainsKey (Java.Lang.Object key);
	bool Java.Util.IMap.ContainsValue (Java.Lang.Object value);
	Java.Lang.Object Java.Util.IMap.Get (Java.Lang.Object key);
	Java.Lang.Object Java.Util.IMap.Put (Java.Lang.Object key, Java.Lang.Object value);
	Java.Lang.Object Java.Util.IMap.Remove (Java.Lang.Object key);
	public virtual System.Collections.ICollection KeySet ();
	public virtual Java.Lang.Object Put (Java.Lang.Object key, Java.Lang.Object value);
	public virtual void PutAll (System.Collections.IDictionary attrib);
	public virtual string PutValue (string name, string val);
	public virtual Java.Lang.Object Remove (Java.Lang.Object key);
	public virtual int Size ();
	public virtual System.Collections.ICollection Values ();
	
	public virtual bool IsEmpty {
		get;
	}
	protected System.Collections.IDictionary Map {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class Name : Java.Lang.Object {
		
		protected Name (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public Name (string s);
		
		public static Name ClassPath {
			get;
			set;
		}
		public static Name ContentType {
			get;
			set;
		}
		public static Name ExtensionInstallation {
			get;
			set;
		}
		public static Name ExtensionList {
			get;
			set;
		}
		public static Name ExtensionName {
			get;
			set;
		}
		public static Name ImplementationTitle {
			get;
			set;
		}
		public static Name ImplementationUrl {
			get;
			set;
		}
		public static Name ImplementationVendor {
			get;
			set;
		}
		public static Name ImplementationVendorId {
			get;
			set;
		}
		public static Name ImplementationVersion {
			get;
			set;
		}
		public static Name MainClass {
			get;
			set;
		}
		public static Name ManifestVersion {
			get;
			set;
		}
		public static Name Sealed {
			get;
			set;
		}
		public static Name SignatureVersion {
			get;
			set;
		}
		public static Name SpecificationTitle {
			get;
			set;
		}
		public static Name SpecificationVendor {
			get;
			set;
		}
		public static Name SpecificationVersion {
			get;
			set;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Java.Util.Jar.JarEntry'>New Type: Java.Util.Jar.JarEntry</h3>

```
public class JarEntry : Java.Util.Zip.ZipEntry {
	
	protected JarEntry (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JarEntry (string name);
	public JarEntry (JarEntry je);
	public JarEntry (Java.Util.Zip.ZipEntry entry);
	
	public virtual Java.Security.Cert.Certificate[] GetCertificates ();
	public virtual Java.Security.CodeSigner[] GetCodeSigners ();
	
	public virtual Attributes Attributes {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Jar.JarException'>New Type: Java.Util.Jar.JarException</h3>

```
public class JarException : Java.Util.Zip.ZipException {
	
	protected JarException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JarException ();
	public JarException (string detailMessage);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Jar.JarFile'>New Type: Java.Util.Jar.JarFile</h3>

```
public class JarFile : Java.Util.Zip.ZipFile {
	
	protected JarFile (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JarFile (Java.IO.File file);
	public JarFile (Java.IO.File file, bool verify);
	public JarFile (Java.IO.File file, bool verify, int mode);
	public JarFile (string filename);
	public JarFile (string filename, bool verify);
	
	public virtual JarEntry GetJarEntry (string name);
	
	public virtual Manifest Manifest {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string ManifestName = "META-INF/MANIFEST.MF";
}
```

<h3 id='Java.Util.Jar.JarInputStream'>New Type: Java.Util.Jar.JarInputStream</h3>

```
public class JarInputStream : Java.Util.Zip.ZipInputStream {
	
	protected JarInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JarInputStream (System.IO.Stream stream);
	public JarInputStream (System.IO.Stream stream, bool verify);
	
	public virtual Manifest Manifest {
		get;
	}
	public virtual JarEntry NextJarEntry {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Jar.JarOutputStream'>New Type: Java.Util.Jar.JarOutputStream</h3>

```
public class JarOutputStream : Java.Util.Zip.ZipOutputStream {
	
	protected JarOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JarOutputStream (System.IO.Stream os);
	public JarOutputStream (System.IO.Stream os, Manifest mf);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Jar.Manifest'>New Type: Java.Util.Jar.Manifest</h3>

```
public class Manifest : Java.Lang.Object, Java.Lang.ICloneable {
	
	protected Manifest (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Manifest ();
	public Manifest (System.IO.Stream is);
	public Manifest (Manifest man);
	
	public virtual void Clear ();
	public virtual Java.Lang.Object Clone ();
	public virtual Attributes GetAttributes (string name);
	public virtual void Read (System.IO.Stream is);
	public System.Threading.Tasks.Task ReadAsync (System.IO.Stream is);
	public virtual void Write (System.IO.Stream os);
	public System.Threading.Tasks.Task WriteAsync (System.IO.Stream os);
	
	public virtual System.Collections.Generic.IDictionary Entries {
		get;
	}
	public virtual Attributes MainAttributes {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Jar.Pack200'>New Type: Java.Util.Jar.Pack200</h3>

```
public abstract class Pack200 : Java.Lang.Object {
	
	protected Pack200 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static IPacker NewPacker ();
	public static IUnpacker NewUnpacker ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public interface IPacker : IDisposable, Android.Runtime.IJavaObject {
		
		void AddPropertyChangeListener (Java.Beans.IPropertyChangeListener listener);
		void Pack (JarFile in, System.IO.Stream out);
		void Pack (JarInputStream in, System.IO.Stream out);
		System.Collections.Generic.IDictionary Properties ();
		void RemovePropertyChangeListener (Java.Beans.IPropertyChangeListener listener);
	}
	public interface IUnpacker : IDisposable, Android.Runtime.IJavaObject {
		
		void AddPropertyChangeListener (Java.Beans.IPropertyChangeListener listener);
		System.Collections.Generic.IDictionary Properties ();
		void RemovePropertyChangeListener (Java.Beans.IPropertyChangeListener listener);
		void Unpack (Java.IO.File in, JarOutputStream out);
		void Unpack (System.IO.Stream in, JarOutputStream out);
	}
	public abstract class Packer {
		
		public const string ClassAttributePfx = "pack.class.attribute.";
		public const string CodeAttributePfx = "pack.code.attribute.";
		public const string DeflateHint = "pack.deflate.hint";
		public const string Effort = "pack.effort";
		public const string Error = "error";
		public const string False = "false";
		public const string FieldAttributePfx = "pack.field.attribute.";
		public const string Keep = "keep";
		public const string KeepFileOrder = "pack.keep.file.order";
		public const string Latest = "latest";
		public const string MethodAttributePfx = "pack.method.attribute.";
		public const string ModificationTime = "pack.modification.time";
		public const string Pass = "pass";
		public const string PassFilePfx = "pack.pass.file.";
		public const string Progress = "pack.progress";
		public const string SegmentLimit = "pack.segment.limit";
		public const string Strip = "strip";
		public const string True = "true";
		public const string UnknownAttribute = "pack.unknown.attribute";
	}
	[Obsolete]
	public abstract class PackerConsts : Packer {
	}
	public abstract class Unpacker {
		
		public const string DeflateHint = "unpack.deflate.hint";
		public const string False = "false";
		public const string Keep = "keep";
		public const string Progress = "unpack.progress";
		public const string True = "true";
	}
	[Obsolete]
	public abstract class UnpackerConsts : Unpacker {
	}
}
```

<h3 id='Java.Util.Jar.Pack200IPackerExtensions'>New Type: Java.Util.Jar.Pack200IPackerExtensions</h3>

```
public static class Pack200IPackerExtensions {
	
	public static System.Threading.Tasks.Task PackAsync (IPacker self, JarFile in, System.IO.Stream out);
	public static System.Threading.Tasks.Task PackAsync (IPacker self, JarInputStream in, System.IO.Stream out);
}
```

<h3 id='Java.Util.Jar.Pack200IUnpackerExtensions'>New Type: Java.Util.Jar.Pack200IUnpackerExtensions</h3>

```
public static class Pack200IUnpackerExtensions {
	
	public static System.Threading.Tasks.Task UnpackAsync (IUnpacker self, Java.IO.File in, JarOutputStream out);
	public static System.Threading.Tasks.Task UnpackAsync (IUnpacker self, System.IO.Stream in, JarOutputStream out);
}
```

<h2 id='Java.Util.Logging'>Namespace: Java.Util.Logging</h2>

<h3 id='Java.Util.Logging.ConsoleHandler'>New Type: Java.Util.Logging.ConsoleHandler</h3>

```
public class ConsoleHandler : StreamHandler {
	
	protected ConsoleHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConsoleHandler ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.ErrorManager'>New Type: Java.Util.Logging.ErrorManager</h3>

```
public class ErrorManager : Java.Lang.Object {
	
	protected ErrorManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ErrorManager ();
	
	public virtual void Error (string message, Java.Lang.Exception exception, int errorCode);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int CloseFailure = 3;
	public const int FlushFailure = 2;
	public const int FormatFailure = 5;
	public const int GenericFailure = 0;
	public const int OpenFailure = 4;
	public const int WriteFailure = 1;
}
```

<h3 id='Java.Util.Logging.FileHandler'>New Type: Java.Util.Logging.FileHandler</h3>

```
public class FileHandler : StreamHandler {
	
	protected FileHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FileHandler ();
	public FileHandler (string pattern);
	public FileHandler (string pattern, bool append);
	public FileHandler (string pattern, int limit, int count);
	public FileHandler (string pattern, int limit, int count, bool append);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.Formatter'>New Type: Java.Util.Logging.Formatter</h3>

```
public abstract class Formatter : Java.Lang.Object {
	
	protected Formatter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Formatter ();
	
	public abstract string Format (LogRecord r);
	public virtual string FormatMessage (LogRecord r);
	public virtual string GetHead (Handler h);
	public virtual string GetTail (Handler h);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.Handler'>New Type: Java.Util.Logging.Handler</h3>

```
public abstract class Handler : Java.Lang.Object {
	
	protected Handler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Handler ();
	
	public abstract void Close ();
	public abstract void Flush ();
	public virtual bool IsLoggable (LogRecord record);
	public abstract void Publish (LogRecord record);
	protected virtual void ReportError (string msg, Java.Lang.Exception ex, int code);
	
	public virtual string Encoding {
		get;
		set;
	}
	public virtual ErrorManager ErrorManager {
		get;
		set;
	}
	public virtual IFilter Filter {
		get;
		set;
	}
	public virtual Formatter Formatter {
		get;
		set;
	}
	public virtual Level Level {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.IFilter'>New Type: Java.Util.Logging.IFilter</h3>

```
public interface IFilter : IDisposable, Android.Runtime.IJavaObject {
	
	bool IsLoggable (LogRecord record);
}
```

<h3 id='Java.Util.Logging.ILoggingMXBean'>New Type: Java.Util.Logging.ILoggingMXBean</h3>

```
public interface ILoggingMXBean : IDisposable, Android.Runtime.IJavaObject {
	
	string GetLoggerLevel (string loggerName);
	string GetParentLoggerName (string loggerName);
	void SetLoggerLevel (string loggerName, string levelName);
	
	System.Collections.Generic.IList LoggerNames {
		get;
	}
}
```

<h3 id='Java.Util.Logging.Level'>New Type: Java.Util.Logging.Level</h3>

```
public class Level : Java.Lang.Object, Java.IO.ISerializable {
	
	protected Level (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Level (string name, int level);
	protected Level (string name, int level, string resourceBundleName);
	
	public static Level Parse (string name);
	public int IntValue ();
	public string ToString ();
	
	public static Level All {
		get;
		set;
	}
	public static Level Config {
		get;
		set;
	}
	public static Level Fine {
		get;
		set;
	}
	public static Level Finer {
		get;
		set;
	}
	public static Level Finest {
		get;
		set;
	}
	public static Level Info {
		get;
		set;
	}
	public static Level Off {
		get;
		set;
	}
	public static Level Severe {
		get;
		set;
	}
	public static Level Warning {
		get;
		set;
	}
	public virtual string LocalizedName {
		get;
	}
	public virtual string Name {
		get;
	}
	public virtual string ResourceBundleName {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.LogManager'>New Type: Java.Util.Logging.LogManager</h3>

```
public class LogManager : Java.Lang.Object {
	
	protected LogManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected LogManager ();
	
	public static LogManager GetLogManager ();
	public virtual bool AddLogger (Logger logger);
	public virtual void AddPropertyChangeListener (Java.Beans.IPropertyChangeListener l);
	public virtual void CheckAccess ();
	public virtual Logger GetLogger (string name);
	public virtual string GetProperty (string name);
	public virtual void ReadConfiguration ();
	public virtual void ReadConfiguration (System.IO.Stream ins);
	public virtual void RemovePropertyChangeListener (Java.Beans.IPropertyChangeListener l);
	public virtual void Reset ();
	
	public static ILoggingMXBean LoggingMXBean {
		get;
	}
	public virtual Java.Util.IEnumeration LoggerNames {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string LoggingMxbeanName = "java.util.logging:type=Logging";
}
```

<h3 id='Java.Util.Logging.LogRecord'>New Type: Java.Util.Logging.LogRecord</h3>

```
public class LogRecord : Java.Lang.Object, Java.IO.ISerializable {
	
	protected LogRecord (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LogRecord (Level level, string msg);
	
	public virtual Java.Lang.Object[] GetParameters ();
	public virtual void SetParameters (Java.Lang.Object[] parameters);
	
	public virtual Level Level {
		get;
		set;
	}
	public virtual string LoggerName {
		get;
		set;
	}
	public virtual string Message {
		get;
		set;
	}
	public virtual long Millis {
		get;
		set;
	}
	public virtual Java.Util.ResourceBundle ResourceBundle {
		get;
		set;
	}
	public virtual string ResourceBundleName {
		get;
		set;
	}
	public virtual long SequenceNumber {
		get;
		set;
	}
	public virtual string SourceClassName {
		get;
		set;
	}
	public virtual string SourceMethodName {
		get;
		set;
	}
	public virtual int ThreadID {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual Java.Lang.Throwable Thrown {
		get;
		set;
	}
}
```

<h3 id='Java.Util.Logging.Logger'>New Type: Java.Util.Logging.Logger</h3>

```
public class Logger : Java.Lang.Object {
	
	protected Logger (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Logger (string name, string resourceBundleName);
	
	public static Logger GetAnonymousLogger (string resourceBundleName);
	public static Logger GetLogger (string name);
	public static Logger GetLogger (string name, string resourceBundleName);
	public virtual void AddHandler (Handler handler);
	public virtual void Config (string msg);
	public virtual void Entering (string sourceClass, string sourceMethod);
	public virtual void Entering (string sourceClass, string sourceMethod, Java.Lang.Object param);
	public virtual void Entering (string sourceClass, string sourceMethod, Java.Lang.Object[] params);
	public virtual void Exiting (string sourceClass, string sourceMethod);
	public virtual void Exiting (string sourceClass, string sourceMethod, Java.Lang.Object result);
	public virtual void Fine (string msg);
	public virtual void Finer (string msg);
	public virtual void Finest (string msg);
	public virtual Handler[] GetHandlers ();
	public virtual void Info (string msg);
	public virtual bool IsLoggable (Level l);
	public virtual void Log (Level logLevel, string msg);
	public virtual void Log (Level logLevel, string msg, Java.Lang.Object param);
	public virtual void Log (Level logLevel, string msg, Java.Lang.Object[] params);
	public virtual void Log (Level logLevel, string msg, Java.Lang.Throwable thrown);
	public virtual void Log (LogRecord record);
	public virtual void Logp (Level logLevel, string sourceClass, string sourceMethod, string msg);
	public virtual void Logp (Level logLevel, string sourceClass, string sourceMethod, string msg, Java.Lang.Object param);
	public virtual void Logp (Level logLevel, string sourceClass, string sourceMethod, string msg, Java.Lang.Object[] params);
	public virtual void Logp (Level logLevel, string sourceClass, string sourceMethod, string msg, Java.Lang.Throwable thrown);
	public virtual void Logrb (Level logLevel, string sourceClass, string sourceMethod, string bundleName, string msg);
	public virtual void Logrb (Level logLevel, string sourceClass, string sourceMethod, string bundleName, string msg, Java.Lang.Object param);
	public virtual void Logrb (Level logLevel, string sourceClass, string sourceMethod, string bundleName, string msg, Java.Lang.Object[] params);
	public virtual void Logrb (Level logLevel, string sourceClass, string sourceMethod, string bundleName, string msg, Java.Lang.Throwable thrown);
	public virtual void RemoveHandler (Handler handler);
	public virtual void Severe (string msg);
	public virtual void Throwing (string sourceClass, string sourceMethod, Java.Lang.Throwable thrown);
	public virtual void Warning (string msg);
	
	public static Logger AnonymousLogger {
		get;
	}
	public static Logger Global {
		get;
	}
	public static string GlobalLoggerName {
		get;
		set;
	}
	public virtual IFilter Filter {
		get;
		set;
	}
	public virtual Level Level {
		get;
		set;
	}
	public virtual string Name {
		get;
	}
	public virtual Logger Parent {
		get;
		set;
	}
	public virtual Java.Util.ResourceBundle ResourceBundle {
		get;
	}
	public virtual string ResourceBundleName {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual bool UseParentHandlers {
		get;
		set;
	}
}
```

<h3 id='Java.Util.Logging.LoggingPermission'>New Type: Java.Util.Logging.LoggingPermission</h3>

```
public sealed class LoggingPermission : Java.Security.BasicPermission {
	
	public LoggingPermission (string name, string actions);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.MemoryHandler'>New Type: Java.Util.Logging.MemoryHandler</h3>

```
public class MemoryHandler : Handler {
	
	protected MemoryHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MemoryHandler ();
	public MemoryHandler (Handler target, int size, Level pushLevel);
	
	public override void Close ();
	public override void Flush ();
	public override void Publish (LogRecord record);
	public virtual void Push ();
	
	public virtual Level PushLevel {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.SimpleFormatter'>New Type: Java.Util.Logging.SimpleFormatter</h3>

```
public class SimpleFormatter : Formatter {
	
	protected SimpleFormatter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SimpleFormatter ();
	
	public override string Format (LogRecord r);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.SocketHandler'>New Type: Java.Util.Logging.SocketHandler</h3>

```
public class SocketHandler : StreamHandler {
	
	protected SocketHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SocketHandler ();
	public SocketHandler (string host, int port);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.StreamHandler'>New Type: Java.Util.Logging.StreamHandler</h3>

```
public class StreamHandler : Handler {
	
	protected StreamHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StreamHandler ();
	public StreamHandler (System.IO.Stream os, Formatter formatter);
	
	public override void Close ();
	public override void Flush ();
	public override void Publish (LogRecord record);
	protected virtual void SetOutputStream (System.IO.Stream os);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Logging.XMLFormatter'>New Type: Java.Util.Logging.XMLFormatter</h3>

```
public class XMLFormatter : Formatter {
	
	protected XMLFormatter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public XMLFormatter ();
	
	public override string Format (LogRecord r);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Java.Util.Prefs'>Namespace: Java.Util.Prefs</h2>

<h3 id='Java.Util.Prefs.AbstractPreferences'>New Type: Java.Util.Prefs.AbstractPreferences</h3>

```
public abstract class AbstractPreferences : Preferences {
	
	protected AbstractPreferences (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractPreferences (AbstractPreferences parent, string name);
	
	public override string AbsolutePath ();
	public override void AddNodeChangeListener (INodeChangeListener ncl);
	public override void AddPreferenceChangeListener (IPreferenceChangeListener pcl);
	protected AbstractPreferences[] CachedChildren ();
	public override string [] ChildrenNames ();
	protected abstract string [] ChildrenNamesSpi ();
	protected abstract AbstractPreferences ChildSpi (string name);
	public override void Clear ();
	public override void ExportNode (System.IO.Stream ostream);
	public override void ExportSubtree (System.IO.Stream ostream);
	public override void Flush ();
	protected abstract void FlushSpi ();
	public override string Get (string key, string deflt);
	public override bool GetBoolean (string key, bool deflt);
	public override byte [] GetByteArray (string key, byte [] deflt);
	protected virtual AbstractPreferences GetChild (string name);
	public override double GetDouble (string key, double deflt);
	public override float GetFloat (string key, float deflt);
	public override int GetInt (string key, int deflt);
	public override long GetLong (string key, long deflt);
	protected abstract string GetSpi (string key);
	public override string [] Keys ();
	protected abstract string [] KeysSpi ();
	public override string Name ();
	public override Preferences Node (string name);
	public override bool NodeExists (string name);
	public override Preferences Parent ();
	public override void Put (string key, string value);
	public override void PutBoolean (string key, bool value);
	public override void PutByteArray (string key, byte [] value);
	public override void PutDouble (string key, double value);
	public override void PutFloat (string key, float value);
	public override void PutInt (string key, int value);
	public override void PutLong (string key, long value);
	protected abstract void PutSpi (string name, string value);
	public override void Remove (string key);
	public override void RemoveNode ();
	public override void RemoveNodeChangeListener (INodeChangeListener ncl);
	protected abstract void RemoveNodeSpi ();
	public override void RemovePreferenceChangeListener (IPreferenceChangeListener pcl);
	protected abstract void RemoveSpi (string key);
	public override void Sync ();
	protected abstract void SyncSpi ();
	public override string ToString ();
	
	protected virtual bool IsRemoved {
		get;
	}
	public override bool IsUserNode {
		get;
	}
	protected Java.Lang.Object Lock {
		get;
		set;
	}
	protected bool NewNode {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Prefs.BackingStoreException'>New Type: Java.Util.Prefs.BackingStoreException</h3>

```
public class BackingStoreException : Java.Lang.Exception {
	
	protected BackingStoreException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BackingStoreException (string s);
	public BackingStoreException (Java.Lang.Throwable t);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Prefs.INodeChangeListener'>New Type: Java.Util.Prefs.INodeChangeListener</h3>

```
public interface INodeChangeListener : IDisposable, Java.Util.IEventListener, Android.Runtime.IJavaObject {
	
	void ChildAdded (NodeChangeEvent e);
	void ChildRemoved (NodeChangeEvent e);
}
```

<h3 id='Java.Util.Prefs.IPreferenceChangeListener'>New Type: Java.Util.Prefs.IPreferenceChangeListener</h3>

```
public interface IPreferenceChangeListener : IDisposable, Java.Util.IEventListener, Android.Runtime.IJavaObject {
	
	void PreferenceChange (PreferenceChangeEvent pce);
}
```

<h3 id='Java.Util.Prefs.IPreferencesFactory'>New Type: Java.Util.Prefs.IPreferencesFactory</h3>

```
public interface IPreferencesFactory : IDisposable, Android.Runtime.IJavaObject {
	
	Preferences SystemRoot ();
	Preferences UserRoot ();
}
```

<h3 id='Java.Util.Prefs.InvalidPreferencesFormatException'>New Type: Java.Util.Prefs.InvalidPreferencesFormatException</h3>

```
public class InvalidPreferencesFormatException : Java.Lang.Exception {
	
	protected InvalidPreferencesFormatException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public InvalidPreferencesFormatException (string s);
	public InvalidPreferencesFormatException (string s, Java.Lang.Throwable t);
	public InvalidPreferencesFormatException (Java.Lang.Throwable t);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Prefs.NodeChangeEvent'>New Type: Java.Util.Prefs.NodeChangeEvent</h3>

```
public class NodeChangeEvent : Java.Util.EventObject {
	
	protected NodeChangeEvent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NodeChangeEvent (Preferences p, Preferences c);
	
	public virtual Preferences Child {
		get;
	}
	public virtual Preferences Parent {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Prefs.PreferenceChangeEvent'>New Type: Java.Util.Prefs.PreferenceChangeEvent</h3>

```
public class PreferenceChangeEvent : Java.Util.EventObject {
	
	protected PreferenceChangeEvent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public PreferenceChangeEvent (Preferences p, string k, string v);
	
	public virtual string Key {
		get;
	}
	public virtual string NewValue {
		get;
	}
	public virtual Preferences Node {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Java.Util.Prefs.Preferences'>New Type: Java.Util.Prefs.Preferences</h3>

```
public abstract class Preferences : Java.Lang.Object {
	
	protected Preferences (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Preferences ();
	
	public static void ImportPreferences (System.IO.Stream istream);
	public static Preferences SystemNodeForPackage (Java.Lang.Class c);
	public static Preferences SystemRoot ();
	public static Preferences UserNodeForPackage (Java.Lang.Class c);
	public static Preferences UserRoot ();
	public abstract string AbsolutePath ();
	public abstract void AddNodeChangeListener (INodeChangeListener ncl);
	public abstract void AddPreferenceChangeListener (IPreferenceChangeListener pcl);
	public abstract string [] ChildrenNames ();
	public abstract void Clear ();
	public abstract void ExportNode (System.IO.Stream ostream);
	public abstract void ExportSubtree (System.IO.Stream ostream);
	public abstract void Flush ();
	public abstract string Get (string key, string deflt);
	public abstract bool GetBoolean (string key, bool deflt);
	public abstract byte [] GetByteArray (string key, byte [] deflt);
	public abstract double GetDouble (string key, double deflt);
	public abstract float GetFloat (string key, float deflt);
	public abstract int GetInt (string key, int deflt);
	public abstract long GetLong (string key, long deflt);
	public abstract string [] Keys ();
	public abstract string Name ();
	public abstract Preferences Node (string path);
	public abstract bool NodeExists (string path);
	public abstract Preferences Parent ();
	public abstract void Put (string key, string value);
	public abstract void PutBoolean (string key, bool value);
	public abstract void PutByteArray (string key, byte [] value);
	public abstract void PutDouble (string key, double value);
	public abstract void PutFloat (string key, float value);
	public abstract void PutInt (string key, int value);
	public abstract void PutLong (string key, long value);
	public abstract void Remove (string key);
	public abstract void RemoveNode ();
	public abstract void RemoveNodeChangeListener (INodeChangeListener ncl);
	public abstract void RemovePreferenceChangeListener (IPreferenceChangeListener pcl);
	public abstract void Sync ();
	public abstract string ToString ();
	
	public abstract bool IsUserNode {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int MaxKeyLength = 80;
	public const int MaxNameLength = 80;
	public const int MaxValueLength = 8192;
}
```

<h2 id='Java.Util.Zip'>Namespace: Java.Util.Zip</h2>

<h3 id='Java.Util.Zip.Deflater'>Type Changed: Java.Util.Zip.Deflater</h3>

Added:

```
public System.Threading.Tasks.Task<int> DeflateAsync (byte [] buf);
 	public System.Threading.Tasks.Task<int> DeflateAsync (byte [] buf, int off, int nbytes);
 	public System.Threading.Tasks.Task<int> DeflateAsync (byte [] p0, int p1, int p2, int p3);
```

<h3 id='Java.Util.Zip.Inflater'>Type Changed: Java.Util.Zip.Inflater</h3>

Added:

```
public System.Threading.Tasks.Task<int> InflateAsync (byte [] buf);
 	public System.Threading.Tasks.Task<int> InflateAsync (byte [] buf, int off, int nbytes);
```

<h3 id='Java.Util.Zip.ZipOutputStream'>Type Changed: Java.Util.Zip.ZipOutputStream</h3>

Added:

```
public System.Threading.Tasks.Task PutNextEntryAsync (ZipEntry ze);
```

<h2 id='Javax.Crypto'>Namespace: Javax.Crypto</h2>

<h3 id='Javax.Crypto.CipherInputStream'>New Type: Javax.Crypto.CipherInputStream</h3>

```
public class CipherInputStream : Java.IO.FilterInputStream {
	
	protected CipherInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected CipherInputStream (System.IO.Stream is);
	public CipherInputStream (System.IO.Stream is, Cipher c);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Crypto.CipherOutputStream'>New Type: Javax.Crypto.CipherOutputStream</h3>

```
public class CipherOutputStream : Java.IO.FilterOutputStream {
	
	protected CipherOutputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected CipherOutputStream (System.IO.Stream os);
	public CipherOutputStream (System.IO.Stream os, Cipher c);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Javax.Security.Cert'>Namespace: Javax.Security.Cert</h2>

<h3 id='Javax.Security.Cert.X509Certificate'>Type Changed: Javax.Security.Cert.X509Certificate</h3>

Added:

```
public static System.Threading.Tasks.Task<X509Certificate> GetInstanceAsync (byte [] certData);
 	public static System.Threading.Tasks.Task<X509Certificate> GetInstanceAsync (System.IO.Stream inStream);
```

<h2 id='Javax.Sql'>Namespace: Javax.Sql</h2>

<h3 id='Javax.Sql.ConnectionEvent'>New Type: Javax.Sql.ConnectionEvent</h3>

```
public class ConnectionEvent : Java.Util.EventObject {
	
	protected ConnectionEvent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnectionEvent (IPooledConnection theConnection);
	public ConnectionEvent (IPooledConnection theConnection, Java.Sql.SQLException theException);
	
	public virtual Java.Sql.SQLException SQLException {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Sql.ICommonDataSource'>New Type: Javax.Sql.ICommonDataSource</h3>

```
public interface ICommonDataSource : IDisposable, Android.Runtime.IJavaObject {
	
	int LoginTimeout {
		get;
		set;
	}
	Java.IO.PrintWriter LogWriter {
		get;
		set;
	}
	Java.Util.Logging.Logger ParentLogger {
		get;
	}
}
```

<h3 id='Javax.Sql.IConnectionEventListener'>New Type: Javax.Sql.IConnectionEventListener</h3>

```
public interface IConnectionEventListener : IDisposable, Java.Util.IEventListener, Android.Runtime.IJavaObject {
	
	void ConnectionClosed (ConnectionEvent theEvent);
	void ConnectionErrorOccurred (ConnectionEvent theEvent);
}
```

<h3 id='Javax.Sql.IConnectionPoolDataSource'>New Type: Javax.Sql.IConnectionPoolDataSource</h3>

```
public interface IConnectionPoolDataSource : ICommonDataSource, IDisposable, Android.Runtime.IJavaObject {
	
	IPooledConnection GetPooledConnection (string theUser, string thePassword);
	
	IPooledConnection PooledConnection {
		get;
	}
}
```

<h3 id='Javax.Sql.IDataSource'>New Type: Javax.Sql.IDataSource</h3>

```
public interface IDataSource : ICommonDataSource, IDisposable, Android.Runtime.IJavaObject, Java.Sql.IWrapper {
	
	Java.Sql.IConnection GetConnection (string theUsername, string thePassword);
	
	Java.Sql.IConnection Connection {
		get;
	}
}
```

<h3 id='Javax.Sql.IPooledConnection'>New Type: Javax.Sql.IPooledConnection</h3>

```
public interface IPooledConnection : IDisposable, Android.Runtime.IJavaObject {
	
	void AddConnectionEventListener (IConnectionEventListener theListener);
	void AddStatementEventListener (IStatementEventListener p0);
	void Close ();
	void RemoveConnectionEventListener (IConnectionEventListener theListener);
	void RemoveStatementEventListener (IStatementEventListener p0);
	
	Java.Sql.IConnection Connection {
		get;
	}
}
```

<h3 id='Javax.Sql.IRowSet'>New Type: Javax.Sql.IRowSet</h3>

```
public interface IRowSet : IDisposable, Android.Runtime.IJavaObject, Java.Sql.IResultSet, Java.Sql.IWrapper {
	
	void AddRowSetListener (IRowSetListener theListener);
	void ClearParameters ();
	void Execute ();
	void RemoveRowSetListener (IRowSetListener theListener);
	void SetArray (int parameterIndex, Java.Sql.IArray theArray);
	void SetAsciiStream (int p0, System.IO.Stream p1);
	void SetAsciiStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	void SetAsciiStream (string p0, System.IO.Stream p1);
	void SetAsciiStream (string p0, System.IO.Stream p1, int p2);
	void SetBigDecimal (int parameterIndex, Java.Math.BigDecimal theBigDecimal);
	void SetBigDecimal (string p0, Java.Math.BigDecimal p1);
	void SetBinaryStream (int p0, System.IO.Stream p1);
	void SetBinaryStream (int parameterIndex, System.IO.Stream theInputStream, int length);
	void SetBinaryStream (string p0, System.IO.Stream p1);
	void SetBinaryStream (string p0, System.IO.Stream p1, int p2);
	void SetBlob (int parameterIndex, Java.Sql.IBlob theBlob);
	void SetBlob (int p0, System.IO.Stream p1);
	void SetBlob (int p0, System.IO.Stream p1, long p2);
	void SetBlob (string p0, Java.Sql.IBlob p1);
	void SetBlob (string p0, System.IO.Stream p1);
	void SetBlob (string p0, System.IO.Stream p1, long p2);
	void SetBoolean (int parameterIndex, bool theBoolean);
	void SetBoolean (string p0, bool p1);
	void SetByte (int parameterIndex, sbyte theByte);
	void SetByte (string p0, sbyte p1);
	void SetBytes (int parameterIndex, byte [] theByteArray);
	void SetBytes (string p0, byte [] p1);
	void SetCharacterStream (int p0, Java.IO.Reader p1);
	void SetCharacterStream (int parameterIndex, Java.IO.Reader theReader, int length);
	void SetCharacterStream (string p0, Java.IO.Reader p1);
	void SetCharacterStream (string p0, Java.IO.Reader p1, int p2);
	void SetClob (int parameterIndex, Java.Sql.IClob theClob);
	void SetClob (int p0, Java.IO.Reader p1);
	void SetClob (int p0, Java.IO.Reader p1, long p2);
	void SetClob (string p0, Java.Sql.IClob p1);
	void SetClob (string p0, Java.IO.Reader p1);
	void SetClob (string p0, Java.IO.Reader p1, long p2);
	void SetConcurrency (int concurrency);
	void SetDate (int parameterIndex, Java.Sql.Date theDate);
	void SetDate (int parameterIndex, Java.Sql.Date theDate, Java.Util.Calendar theCalendar);
	void SetDate (string p0, Java.Sql.Date p1);
	void SetDate (string p0, Java.Sql.Date p1, Java.Util.Calendar p2);
	void SetDouble (int parameterIndex, double theDouble);
	void SetDouble (string p0, double p1);
	void SetFloat (int parameterIndex, float theFloat);
	void SetFloat (string p0, float p1);
	void SetInt (int parameterIndex, int theInteger);
	void SetInt (string p0, int p1);
	void SetLong (int parameterIndex, long theLong);
	void SetLong (string p0, long p1);
	void SetNCharacterStream (int p0, Java.IO.Reader p1);
	void SetNCharacterStream (int p0, Java.IO.Reader p1, long p2);
	void SetNCharacterStream (string p0, Java.IO.Reader p1);
	void SetNCharacterStream (string p0, Java.IO.Reader p1, long p2);
	void SetNClob (int p0, Java.Sql.INClob p1);
	void SetNClob (int p0, Java.IO.Reader p1);
	void SetNClob (int p0, Java.IO.Reader p1, long p2);
	void SetNClob (string p0, Java.Sql.INClob p1);
	void SetNClob (string p0, Java.IO.Reader p1);
	void SetNClob (string p0, Java.IO.Reader p1, long p2);
	void SetNString (int p0, string p1);
	void SetNString (string p0, string p1);
	void SetNull (int parameterIndex, int sqlType);
	void SetNull (int parameterIndex, int sqlType, string typeName);
	void SetNull (string p0, int p1);
	void SetNull (string p0, int p1, string p2);
	void SetObject (int parameterIndex, Java.Lang.Object theObject);
	void SetObject (int parameterIndex, Java.Lang.Object theObject, int targetSqlType);
	void SetObject (int parameterIndex, Java.Lang.Object theObject, int targetSqlType, int scale);
	void SetObject (string p0, Java.Lang.Object p1);
	void SetObject (string p0, Java.Lang.Object p1, int p2);
	void SetObject (string p0, Java.Lang.Object p1, int p2, int p3);
	void SetRef (int parameterIndex, Java.Sql.IRef theRef);
	void SetRowId (int p0, Java.Sql.IRowId p1);
	void SetRowId (string p0, Java.Sql.IRowId p1);
	void SetShort (int parameterIndex, short theShort);
	void SetShort (string p0, short p1);
	void SetSQLXML (int p0, Java.Sql.ISQLXML p1);
	void SetSQLXML (string p0, Java.Sql.ISQLXML p1);
	void SetString (int parameterIndex, string theString);
	void SetString (string p0, string p1);
	void SetTime (int parameterIndex, Java.Sql.Time theTime);
	void SetTime (int parameterIndex, Java.Sql.Time theTime, Java.Util.Calendar theCalendar);
	void SetTime (string p0, Java.Sql.Time p1);
	void SetTime (string p0, Java.Sql.Time p1, Java.Util.Calendar p2);
	void SetTimestamp (int parameterIndex, Java.Sql.Timestamp theTimestamp);
	void SetTimestamp (int parameterIndex, Java.Sql.Timestamp theTimestamp, Java.Util.Calendar theCalendar);
	void SetTimestamp (string p0, Java.Sql.Timestamp p1);
	void SetTimestamp (string p0, Java.Sql.Timestamp p1, Java.Util.Calendar p2);
	void SetType (int type);
	void SetURL (int p0, Java.Net.URL p1);
	
	string Command {
		get;
		set;
	}
	string DataSourceName {
		get;
		set;
	}
	bool EscapeProcessing {
		get;
		set;
	}
	int MaxFieldSize {
		get;
		set;
	}
	int MaxRows {
		get;
		set;
	}
	string Password {
		get;
		set;
	}
	int QueryTimeout {
		get;
		set;
	}
	bool ReadOnly {
		get;
		set;
	}
	int TransactionIsolation {
		get;
		set;
	}
	System.Collections.Generic.IDictionary TypeMap {
		get;
		set;
	}
	string Url {
		get;
		set;
	}
	string Username {
		get;
		set;
	}
}
```

<h3 id='Javax.Sql.IRowSetInternal'>New Type: Javax.Sql.IRowSetInternal</h3>

```
public interface IRowSetInternal : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object[] GetParams ();
	void SetMetaData (IRowSetMetaData theMetaData);
	
	Java.Sql.IConnection Connection {
		get;
	}
	Java.Sql.IResultSet Original {
		get;
	}
	Java.Sql.IResultSet OriginalRow {
		get;
	}
}
```

<h3 id='Javax.Sql.IRowSetListener'>New Type: Javax.Sql.IRowSetListener</h3>

```
public interface IRowSetListener : IDisposable, Java.Util.IEventListener, Android.Runtime.IJavaObject {
	
	void CursorMoved (RowSetEvent theEvent);
	void RowChanged (RowSetEvent theEvent);
	void RowSetChanged (RowSetEvent theEvent);
}
```

<h3 id='Javax.Sql.IRowSetMetaData'>New Type: Javax.Sql.IRowSetMetaData</h3>

```
public interface IRowSetMetaData : IDisposable, Android.Runtime.IJavaObject, Java.Sql.IResultSetMetaData, Java.Sql.IWrapper {
	
	void SetAutoIncrement (int columnIndex, bool autoIncrement);
	void SetCaseSensitive (int columnIndex, bool caseSensitive);
	void SetCatalogName (int columnIndex, string catalogName);
	void SetColumnCount (int columnCount);
	void SetColumnDisplaySize (int columnIndex, int displaySize);
	void SetColumnLabel (int columnIndex, string theLabel);
	void SetColumnName (int columnIndex, string theColumnName);
	void SetColumnType (int columnIndex, int theSQLType);
	void SetColumnTypeName (int columnIndex, string theTypeName);
	void SetCurrency (int columnIndex, bool isCurrency);
	void SetNullable (int columnIndex, int nullability);
	void SetPrecision (int columnIndex, int thePrecision);
	void SetScale (int columnIndex, int theScale);
	void SetSchemaName (int columnIndex, string theSchemaName);
	void SetSearchable (int columnIndex, bool isSearchable);
	void SetSigned (int columnIndex, bool isSigned);
	void SetTableName (int columnIndex, string theTableName);
}
```

<h3 id='Javax.Sql.IRowSetReader'>New Type: Javax.Sql.IRowSetReader</h3>

```
public interface IRowSetReader : IDisposable, Android.Runtime.IJavaObject {
	
	void ReadData (IRowSetInternal theCaller);
}
```

<h3 id='Javax.Sql.IRowSetWriter'>New Type: Javax.Sql.IRowSetWriter</h3>

```
public interface IRowSetWriter : IDisposable, Android.Runtime.IJavaObject {
	
	bool WriteData (IRowSetInternal theRowSet);
}
```

<h3 id='Javax.Sql.IStatementEventListener'>New Type: Javax.Sql.IStatementEventListener</h3>

```
public interface IStatementEventListener : IDisposable, Java.Util.IEventListener, Android.Runtime.IJavaObject {
	
	void StatementClosed (StatementEvent e);
	void StatementErrorOccurred (StatementEvent e);
}
```

<h3 id='Javax.Sql.RowSetEvent'>New Type: Javax.Sql.RowSetEvent</h3>

```
public class RowSetEvent : Java.Util.EventObject {
	
	protected RowSetEvent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RowSetEvent (IRowSet theSource);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Sql.StatementEvent'>New Type: Javax.Sql.StatementEvent</h3>

```
public class StatementEvent : Java.Util.EventObject {
	
	protected StatementEvent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StatementEvent (IPooledConnection con, Java.Sql.IPreparedStatement statement);
	public StatementEvent (IPooledConnection con, Java.Sql.IPreparedStatement statement, Java.Sql.SQLException exception);
	
	public virtual Java.Sql.SQLException SQLException {
		get;
	}
	public virtual Java.Sql.IPreparedStatement Statement {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Javax.Xml'>Namespace: Javax.Xml</h2>

<h3 id='Javax.Xml.XMLConstants'>New Type: Javax.Xml.XMLConstants</h3>

```
public sealed class XMLConstants : Java.Lang.Object {
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string DefaultNsPrefix = "";
	public const string FeatureSecureProcessing = "http://javax.xml.XMLConstants/feature/secure-processing";
	public const string NullNsUri = "";
	public const string RelaxngNsUri = "http://relaxng.org/ns/structure/1.0";
	public const string W3cXmlSchemaInstanceNsUri = "http://www.w3.org/2001/XMLSchema-instance";
	public const string W3cXmlSchemaNsUri = "http://www.w3.org/2001/XMLSchema";
	public const string W3cXpathDatatypeNsUri = "http://www.w3.org/2003/11/xpath-datatypes";
	public const string XmlDtdNsUri = "http://www.w3.org/TR/REC-xml";
	public const string XmlNsPrefix = "xml";
	public const string XmlNsUri = "http://www.w3.org/XML/1998/namespace";
	public const string XmlnsAttribute = "xmlns";
	public const string XmlnsAttributeNsUri = "http://www.w3.org/2000/xmlns/";
}
```

<h2 id='Javax.Xml.Datatype'>Namespace: Javax.Xml.Datatype</h2>

<h3 id='Javax.Xml.Datatype.DatatypeConfigurationException'>New Type: Javax.Xml.Datatype.DatatypeConfigurationException</h3>

```
public class DatatypeConfigurationException : Java.Lang.Exception {
	
	protected DatatypeConfigurationException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DatatypeConfigurationException ();
	public DatatypeConfigurationException (string message);
	public DatatypeConfigurationException (string message, Java.Lang.Throwable cause);
	public DatatypeConfigurationException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Datatype.DatatypeConstants'>New Type: Javax.Xml.Datatype.DatatypeConstants</h3>

```
public sealed class DatatypeConstants : Java.Lang.Object {
	
	public static Javax.Xml.Namespace.QName Date {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Datetime {
		get;
		set;
	}
	public static Field Days {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Duration {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName DurationDaytime {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName DurationYearmonth {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Gday {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Gmonth {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Gmonthday {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Gyear {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Gyearmonth {
		get;
		set;
	}
	public static Field Hours {
		get;
		set;
	}
	public static Field Minutes {
		get;
		set;
	}
	public static Field Months {
		get;
		set;
	}
	public static Field Seconds {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Time {
		get;
		set;
	}
	public static Field Years {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int April = 4;
	public const int August = 8;
	public const int December = 12;
	public const int Equal = 0;
	public const int February = 2;
	public const int FieldUndefined = -2147483648;
	public const int Greater = 1;
	public const int Indeterminate = 2;
	public const int January = 1;
	public const int July = 7;
	public const int June = 6;
	public const int Lesser = -1;
	public const int March = 3;
	public const int MaxTimezoneOffset = -840;
	public const int May = 5;
	public const int MinTimezoneOffset = 840;
	public const int November = 11;
	public const int October = 10;
	public const int September = 9;
	
	public sealed class Field : Java.Lang.Object {
		
		public int Id {
			get;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Javax.Xml.Datatype.DatatypeFactory'>New Type: Javax.Xml.Datatype.DatatypeFactory</h3>

```
public abstract class DatatypeFactory : Java.Lang.Object {
	
	protected DatatypeFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected DatatypeFactory ();
	
	public static DatatypeFactory NewInstance ();
	public static DatatypeFactory NewInstance (string p0, Java.Lang.ClassLoader p1);
	public abstract Duration NewDuration (bool isPositive, Java.Math.BigInteger years, Java.Math.BigInteger months, Java.Math.BigInteger days, Java.Math.BigInteger hours, Java.Math.BigInteger minutes, Java.Math.BigDecimal seconds);
	public virtual Duration NewDuration (bool isPositive, int years, int months, int days, int hours, int minutes, int seconds);
	public abstract Duration NewDuration (long durationInMilliSeconds);
	public abstract Duration NewDuration (string lexicalRepresentation);
	public virtual Duration NewDurationDayTime (bool isPositive, Java.Math.BigInteger day, Java.Math.BigInteger hour, Java.Math.BigInteger minute, Java.Math.BigInteger second);
	public virtual Duration NewDurationDayTime (bool isPositive, int day, int hour, int minute, int second);
	public virtual Duration NewDurationDayTime (long durationInMilliseconds);
	public virtual Duration NewDurationDayTime (string lexicalRepresentation);
	public virtual Duration NewDurationYearMonth (bool isPositive, Java.Math.BigInteger year, Java.Math.BigInteger month);
	public virtual Duration NewDurationYearMonth (bool isPositive, int year, int month);
	public virtual Duration NewDurationYearMonth (long durationInMilliseconds);
	public virtual Duration NewDurationYearMonth (string lexicalRepresentation);
	public abstract XMLGregorianCalendar NewXMLGregorianCalendar ();
	public abstract XMLGregorianCalendar NewXMLGregorianCalendar (Java.Math.BigInteger year, int month, int day, int hour, int minute, int second, Java.Math.BigDecimal fractionalSecond, int timezone);
	public abstract XMLGregorianCalendar NewXMLGregorianCalendar (Java.Util.GregorianCalendar cal);
	public virtual XMLGregorianCalendar NewXMLGregorianCalendar (int year, int month, int day, int hour, int minute, int second, int millisecond, int timezone);
	public abstract XMLGregorianCalendar NewXMLGregorianCalendar (string lexicalRepresentation);
	public virtual XMLGregorianCalendar NewXMLGregorianCalendarDate (int year, int month, int day, int timezone);
	public virtual XMLGregorianCalendar NewXMLGregorianCalendarTime (int hours, int minutes, int seconds, Java.Math.BigDecimal fractionalSecond, int timezone);
	public virtual XMLGregorianCalendar NewXMLGregorianCalendarTime (int hours, int minutes, int seconds, int timezone);
	public virtual XMLGregorianCalendar NewXMLGregorianCalendarTime (int hours, int minutes, int seconds, int milliseconds, int timezone);
	
	public static string DatatypefactoryImplementationClass {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string DatatypefactoryProperty = "javax.xml.datatype.DatatypeFactory";
}
```

<h3 id='Javax.Xml.Datatype.Duration'>New Type: Javax.Xml.Datatype.Duration</h3>

```
public abstract class Duration : Java.Lang.Object {
	
	protected Duration (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Duration ();
	
	public abstract Duration Add (Duration rhs);
	public abstract void AddTo (Java.Util.Calendar calendar);
	public virtual void AddTo (Java.Util.Date date);
	public abstract int Compare (Duration duration);
	public abstract Java.Lang.Number GetField (Field field);
	public abstract int GetHashCode ();
	public virtual long GetTimeInMillis (Java.Util.Calendar startInstant);
	public virtual long GetTimeInMillis (Java.Util.Date startInstant);
	public virtual bool IsLongerThan (Duration duration);
	public abstract bool IsSet (Field field);
	public virtual bool IsShorterThan (Duration duration);
	public abstract Duration Multiply (Java.Math.BigDecimal factor);
	public virtual Duration Multiply (int factor);
	public abstract Duration Negate ();
	public abstract Duration NormalizeWith (Java.Util.Calendar startTimeInstant);
	public virtual Duration Subtract (Duration rhs);
	
	public virtual int Days {
		get;
	}
	public virtual int Hours {
		get;
	}
	public virtual int Minutes {
		get;
	}
	public virtual int Months {
		get;
	}
	public virtual int Seconds {
		get;
	}
	public abstract int Sign {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual Javax.Xml.Namespace.QName XMLSchemaType {
		get;
	}
	public virtual int Years {
		get;
	}
}
```

<h3 id='Javax.Xml.Datatype.XMLGregorianCalendar'>New Type: Javax.Xml.Datatype.XMLGregorianCalendar</h3>

```
public abstract class XMLGregorianCalendar : Java.Lang.Object, Java.Lang.ICloneable {
	
	protected XMLGregorianCalendar (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public XMLGregorianCalendar ();
	
	public abstract void Add (Duration duration);
	public abstract void Clear ();
	public abstract Java.Lang.Object Clone ();
	public abstract int Compare (XMLGregorianCalendar xmlGregorianCalendar);
	public abstract Java.Util.TimeZone GetTimeZone (int defaultZoneoffset);
	public abstract XMLGregorianCalendar Normalize ();
	public abstract void Reset ();
	public virtual void SetTime (int hour, int minute, int second);
	public virtual void SetTime (int hour, int minute, int second, Java.Math.BigDecimal fractional);
	public virtual void SetTime (int hour, int minute, int second, int millisecond);
	public abstract void SetYear (Java.Math.BigInteger year);
	public abstract Java.Util.GregorianCalendar ToGregorianCalendar ();
	public abstract Java.Util.GregorianCalendar ToGregorianCalendar (Java.Util.TimeZone timezone, Java.Util.Locale aLocale, XMLGregorianCalendar defaults);
	public abstract string ToXMLFormat ();
	
	public abstract int Day {
		get;
		set;
	}
	public abstract Java.Math.BigInteger Eon {
		get;
	}
	public abstract Java.Math.BigInteger EonAndYear {
		get;
	}
	public abstract Java.Math.BigDecimal FractionalSecond {
		get;
		set;
	}
	public abstract int Hour {
		get;
		set;
	}
	public abstract bool IsValid {
		get;
	}
	public virtual int Millisecond {
		get;
		set;
	}
	public abstract int Minute {
		get;
		set;
	}
	public abstract int Month {
		get;
		set;
	}
	public abstract int Second {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public abstract int Timezone {
		get;
		set;
	}
	public abstract Javax.Xml.Namespace.QName XMLSchemaType {
		get;
	}
	public abstract int Year {
		get;
		set;
	}
}
```

<h2 id='Javax.Xml.Namespace'>Namespace: Javax.Xml.Namespace</h2>

<h3 id='Javax.Xml.Namespace.INamespaceContext'>New Type: Javax.Xml.Namespace.INamespaceContext</h3>

```
public interface INamespaceContext : IDisposable, Android.Runtime.IJavaObject {
	
	string GetNamespaceURI (string prefix);
	string GetPrefix (string namespaceURI);
	Java.Util.IIterator GetPrefixes (string namespaceURI);
}
```

<h3 id='Javax.Xml.Namespace.QName'>New Type: Javax.Xml.Namespace.QName</h3>

```
public class QName : Java.Lang.Object, Java.IO.ISerializable {
	
	protected QName (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public QName (string localPart);
	public QName (string namespaceURI, string localPart);
	public QName (string namespaceURI, string localPart, string prefix);
	
	public static QName ValueOf (string qNameAsString);
	public bool Equals (Java.Lang.Object objectToTest);
	public int GetHashCode ();
	
	public virtual string LocalPart {
		get;
	}
	public virtual string NamespaceURI {
		get;
	}
	public virtual string Prefix {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Javax.Xml.Parsers'>Namespace: Javax.Xml.Parsers</h2>

<h3 id='Javax.Xml.Parsers.DocumentBuilder'>New Type: Javax.Xml.Parsers.DocumentBuilder</h3>

```
public abstract class DocumentBuilder : Java.Lang.Object {
	
	protected DocumentBuilder (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected DocumentBuilder ();
	
	public abstract Org.W3c.Dom.IDocument NewDocument ();
	public virtual Org.W3c.Dom.IDocument Parse (Java.IO.File file);
	public abstract Org.W3c.Dom.IDocument Parse (Org.Xml.Sax.InputSource source);
	public virtual Org.W3c.Dom.IDocument Parse (System.IO.Stream stream);
	public virtual Org.W3c.Dom.IDocument Parse (System.IO.Stream stream, string systemId);
	public virtual Org.W3c.Dom.IDocument Parse (string uri);
	public System.Threading.Tasks.Task ParseAsync (Java.IO.File file);
	public System.Threading.Tasks.Task ParseAsync (Org.Xml.Sax.InputSource source);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, string systemId);
	public System.Threading.Tasks.Task ParseAsync (string uri);
	public virtual void Reset ();
	public abstract void SetEntityResolver (Org.Xml.Sax.IEntityResolver resolver);
	public abstract void SetErrorHandler (Org.Xml.Sax.IErrorHandler handler);
	
	public abstract Org.W3c.Dom.IDOMImplementation DOMImplementation {
		get;
	}
	public abstract bool IsNamespaceAware {
		get;
	}
	public abstract bool IsValidating {
		get;
	}
	public virtual bool IsXIncludeAware {
		get;
	}
	public virtual Javax.Xml.Validation.Schema Schema {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Parsers.DocumentBuilderFactory'>New Type: Javax.Xml.Parsers.DocumentBuilderFactory</h3>

```
public abstract class DocumentBuilderFactory : Java.Lang.Object {
	
	protected DocumentBuilderFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected DocumentBuilderFactory ();
	
	public static DocumentBuilderFactory NewInstance ();
	public static DocumentBuilderFactory NewInstance (string p0, Java.Lang.ClassLoader p1);
	public abstract Java.Lang.Object GetAttribute (string name);
	public abstract bool GetFeature (string name);
	public abstract DocumentBuilder NewDocumentBuilder ();
	public abstract void SetAttribute (string name, Java.Lang.Object value);
	public abstract void SetFeature (string name, bool value);
	
	public virtual bool Coalescing {
		get;
		set;
	}
	public virtual bool ExpandEntityReferences {
		get;
		set;
	}
	public virtual bool IgnoringComments {
		get;
		set;
	}
	public virtual bool IgnoringElementContentWhitespace {
		get;
		set;
	}
	public virtual bool NamespaceAware {
		get;
		set;
	}
	public virtual Javax.Xml.Validation.Schema Schema {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual bool Validating {
		get;
		set;
	}
	public virtual bool XIncludeAware {
		get;
		set;
	}
}
```

<h3 id='Javax.Xml.Parsers.FactoryConfigurationError'>New Type: Javax.Xml.Parsers.FactoryConfigurationError</h3>

```
public class FactoryConfigurationError : Java.Lang.Error {
	
	protected FactoryConfigurationError (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FactoryConfigurationError ();
	public FactoryConfigurationError (Java.Lang.Exception cause);
	public FactoryConfigurationError (Java.Lang.Exception cause, string message);
	public FactoryConfigurationError (string message);
	
	public virtual Java.Lang.Exception Exception {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Parsers.ParserConfigurationException'>New Type: Javax.Xml.Parsers.ParserConfigurationException</h3>

```
public class ParserConfigurationException : Java.Lang.Exception {
	
	protected ParserConfigurationException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ParserConfigurationException ();
	public ParserConfigurationException (string msg);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Parsers.SAXParser'>New Type: Javax.Xml.Parsers.SAXParser</h3>

```
public abstract class SAXParser : Java.Lang.Object {
	
	protected SAXParser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected SAXParser ();
	
	public abstract Java.Lang.Object GetProperty (string name);
	public virtual void Parse (Java.IO.File file, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public virtual void Parse (Java.IO.File file, Org.Xml.Sax.HandlerBase handler);
	public virtual void Parse (Org.Xml.Sax.InputSource source, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public virtual void Parse (Org.Xml.Sax.InputSource source, Org.Xml.Sax.HandlerBase handler);
	public virtual void Parse (System.IO.Stream stream, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public virtual void Parse (System.IO.Stream stream, Org.Xml.Sax.Helpers.DefaultHandler handler, string systemId);
	public virtual void Parse (System.IO.Stream stream, Org.Xml.Sax.HandlerBase handler);
	public virtual void Parse (System.IO.Stream stream, Org.Xml.Sax.HandlerBase handler, string systemId);
	public virtual void Parse (string uri, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public virtual void Parse (string uri, Org.Xml.Sax.HandlerBase handler);
	public System.Threading.Tasks.Task ParseAsync (Java.IO.File file, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public System.Threading.Tasks.Task ParseAsync (Java.IO.File file, Org.Xml.Sax.HandlerBase handler);
	public System.Threading.Tasks.Task ParseAsync (Org.Xml.Sax.InputSource source, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public System.Threading.Tasks.Task ParseAsync (Org.Xml.Sax.InputSource source, Org.Xml.Sax.HandlerBase handler);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, Org.Xml.Sax.Helpers.DefaultHandler handler, string systemId);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, Org.Xml.Sax.HandlerBase handler);
	public System.Threading.Tasks.Task ParseAsync (System.IO.Stream stream, Org.Xml.Sax.HandlerBase handler, string systemId);
	public System.Threading.Tasks.Task ParseAsync (string uri, Org.Xml.Sax.Helpers.DefaultHandler handler);
	public System.Threading.Tasks.Task ParseAsync (string uri, Org.Xml.Sax.HandlerBase handler);
	public virtual void Reset ();
	public abstract void SetProperty (string name, Java.Lang.Object value);
	
	public abstract bool IsNamespaceAware {
		get;
	}
	public abstract bool IsValidating {
		get;
	}
	public virtual bool IsXIncludeAware {
		get;
	}
	public abstract Org.Xml.Sax.IParser Parser {
		get;
	}
	public virtual Javax.Xml.Validation.Schema Schema {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public abstract Org.Xml.Sax.IXMLReader XMLReader {
		get;
	}
}
```

<h3 id='Javax.Xml.Parsers.SAXParserFactory'>New Type: Javax.Xml.Parsers.SAXParserFactory</h3>

```
public abstract class SAXParserFactory : Java.Lang.Object {
	
	protected SAXParserFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected SAXParserFactory ();
	
	public static SAXParserFactory NewInstance ();
	public static SAXParserFactory NewInstance (string p0, Java.Lang.ClassLoader p1);
	public abstract bool GetFeature (string name);
	public abstract SAXParser NewSAXParser ();
	public abstract void SetFeature (string name, bool value);
	
	public virtual bool NamespaceAware {
		get;
		set;
	}
	public virtual Javax.Xml.Validation.Schema Schema {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual bool Validating {
		get;
		set;
	}
	public virtual bool XIncludeAware {
		get;
		set;
	}
}
```

<h2 id='Javax.Xml.Transform'>Namespace: Javax.Xml.Transform</h2>

<h3 id='Javax.Xml.Transform.ErrorEventArgs'>New Type: Javax.Xml.Transform.ErrorEventArgs</h3>

```
public class ErrorEventArgs : EventArgs {
	
	public ErrorEventArgs (TransformerException exception);
	
	public TransformerException Exception {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.FatalErrorEventArgs'>New Type: Javax.Xml.Transform.FatalErrorEventArgs</h3>

```
public class FatalErrorEventArgs : EventArgs {
	
	public FatalErrorEventArgs (TransformerException exception);
	
	public TransformerException Exception {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.IErrorListener'>New Type: Javax.Xml.Transform.IErrorListener</h3>

```
public interface IErrorListener : IDisposable, Android.Runtime.IJavaObject {
	
	void Error (TransformerException exception);
	void FatalError (TransformerException exception);
	void Warning (TransformerException exception);
}
```

<h3 id='Javax.Xml.Transform.IResult'>New Type: Javax.Xml.Transform.IResult</h3>

```
public interface IResult : IDisposable, Android.Runtime.IJavaObject {
	
	string SystemId {
		get;
		set;
	}
}
```

<h3 id='Javax.Xml.Transform.ISource'>New Type: Javax.Xml.Transform.ISource</h3>

```
public interface ISource : IDisposable, Android.Runtime.IJavaObject {
	
	string SystemId {
		get;
		set;
	}
}
```

<h3 id='Javax.Xml.Transform.ISourceLocator'>New Type: Javax.Xml.Transform.ISourceLocator</h3>

```
public interface ISourceLocator : IDisposable, Android.Runtime.IJavaObject {
	
	int ColumnNumber {
		get;
	}
	int LineNumber {
		get;
	}
	string PublicId {
		get;
	}
	string SystemId {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.ITemplates'>New Type: Javax.Xml.Transform.ITemplates</h3>

```
public interface ITemplates : IDisposable, Android.Runtime.IJavaObject {
	
	Transformer NewTransformer ();
	
	Java.Util.Properties OutputProperties {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.IURIResolver'>New Type: Javax.Xml.Transform.IURIResolver</h3>

```
public interface IURIResolver : IDisposable, Android.Runtime.IJavaObject {
	
	ISource Resolve (string href, string base);
}
```

<h3 id='Javax.Xml.Transform.OutputKeys'>New Type: Javax.Xml.Transform.OutputKeys</h3>

```
public class OutputKeys : Java.Lang.Object {
	
	protected OutputKeys (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string CdataSectionElements = "cdata-section-elements";
	public const string DoctypePublic = "doctype-public";
	public const string DoctypeSystem = "doctype-system";
	public const string Encoding = "encoding";
	public const string Indent = "indent";
	public const string MediaType = "media-type";
	public const string Method = "method";
	public const string OmitXmlDeclaration = "omit-xml-declaration";
	public const string Standalone = "standalone";
	public const string Version = "version";
}
```

<h3 id='Javax.Xml.Transform.Result'>New Type: Javax.Xml.Transform.Result</h3>

```
public abstract class Result {
	
	public const string PiDisableOutputEscaping = "javax.xml.transform.disable-output-escaping";
	public const string PiEnableOutputEscaping = "javax.xml.transform.enable-output-escaping";
}
```

<h3 id='Javax.Xml.Transform.ResultConsts'>New Type: Javax.Xml.Transform.ResultConsts</h3>

```
[Obsolete]
public abstract class ResultConsts : Result {
}
```

<h3 id='Javax.Xml.Transform.Transformer'>New Type: Javax.Xml.Transform.Transformer</h3>

```
public abstract class Transformer : Java.Lang.Object {
	
	protected Transformer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Transformer ();
	
	public abstract void ClearParameters ();
	public abstract string GetOutputProperty (string name);
	public abstract Java.Lang.Object GetParameter (string name);
	public virtual void Reset ();
	public abstract void SetOutputProperty (string name, string value);
	public abstract void SetParameter (string name, Java.Lang.Object value);
	public abstract void Transform (ISource xmlSource, IResult outputTarget);
	
	public abstract IErrorListener ErrorListener {
		get;
		set;
	}
	public abstract Java.Util.Properties OutputProperties {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public abstract IURIResolver URIResolver {
		get;
		set;
	}
	
	public event EventHandler Error;
	public event EventHandler FatalError;
	public event EventHandler Warning;
}
```

<h3 id='Javax.Xml.Transform.TransformerConfigurationException'>New Type: Javax.Xml.Transform.TransformerConfigurationException</h3>

```
public class TransformerConfigurationException : TransformerException {
	
	protected TransformerConfigurationException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TransformerConfigurationException ();
	public TransformerConfigurationException (string msg);
	public TransformerConfigurationException (string msg, Java.Lang.Throwable e);
	public TransformerConfigurationException (string message, ISourceLocator locator);
	public TransformerConfigurationException (string message, ISourceLocator locator, Java.Lang.Throwable e);
	public TransformerConfigurationException (Java.Lang.Throwable e);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.TransformerException'>New Type: Javax.Xml.Transform.TransformerException</h3>

```
public class TransformerException : Java.Lang.Exception {
	
	protected TransformerException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TransformerException (string message);
	public TransformerException (string message, Java.Lang.Throwable e);
	public TransformerException (string message, ISourceLocator locator);
	public TransformerException (string message, ISourceLocator locator, Java.Lang.Throwable e);
	public TransformerException (Java.Lang.Throwable e);
	
	public virtual Java.Lang.Throwable Exception {
		get;
	}
	public virtual string LocationAsString {
		get;
	}
	public virtual ISourceLocator Locator {
		get;
		set;
	}
	public virtual string MessageAndLocation {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.TransformerFactory'>New Type: Javax.Xml.Transform.TransformerFactory</h3>

```
public abstract class TransformerFactory : Java.Lang.Object {
	
	protected TransformerFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected TransformerFactory ();
	
	public static TransformerFactory NewInstance ();
	public static TransformerFactory NewInstance (string p0, Java.Lang.ClassLoader p1);
	public abstract ISource GetAssociatedStylesheet (ISource source, string media, string title, string charset);
	public abstract Java.Lang.Object GetAttribute (string name);
	public abstract bool GetFeature (string name);
	public abstract ITemplates NewTemplates (ISource source);
	public abstract Transformer NewTransformer ();
	public abstract Transformer NewTransformer (ISource source);
	public abstract void SetAttribute (string name, Java.Lang.Object value);
	public abstract void SetFeature (string name, bool value);
	
	public abstract IErrorListener ErrorListener {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public abstract IURIResolver URIResolver {
		get;
		set;
	}
	
	public event EventHandler Error;
	public event EventHandler FatalError;
	public event EventHandler Warning;
}
```

<h3 id='Javax.Xml.Transform.TransformerFactoryConfigurationError'>New Type: Javax.Xml.Transform.TransformerFactoryConfigurationError</h3>

```
public class TransformerFactoryConfigurationError : Java.Lang.Error {
	
	protected TransformerFactoryConfigurationError (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public TransformerFactoryConfigurationError ();
	public TransformerFactoryConfigurationError (Java.Lang.Exception e);
	public TransformerFactoryConfigurationError (Java.Lang.Exception e, string msg);
	public TransformerFactoryConfigurationError (string msg);
	
	public virtual Java.Lang.Exception Exception {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.WarningEventArgs'>New Type: Javax.Xml.Transform.WarningEventArgs</h3>

```
public class WarningEventArgs : EventArgs {
	
	public WarningEventArgs (TransformerException exception);
	
	public TransformerException Exception {
		get;
	}
}
```

<h2 id='Javax.Xml.Transform.Dom'>Namespace: Javax.Xml.Transform.Dom</h2>

<h3 id='Javax.Xml.Transform.Dom.DOMResult'>New Type: Javax.Xml.Transform.Dom.DOMResult</h3>

```
public class DOMResult : Java.Lang.Object, Javax.Xml.Transform.IResult {
	
	protected DOMResult (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DOMResult ();
	public DOMResult (Org.W3c.Dom.INode node);
	public DOMResult (Org.W3c.Dom.INode node, string systemId);
	public DOMResult (Org.W3c.Dom.INode node, Org.W3c.Dom.INode nextSibling);
	public DOMResult (Org.W3c.Dom.INode node, Org.W3c.Dom.INode nextSibling, string systemId);
	
	public virtual Org.W3c.Dom.INode NextSibling {
		get;
		set;
	}
	public virtual Org.W3c.Dom.INode Node {
		get;
		set;
	}
	public virtual string SystemId {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Feature = "http://javax.xml.transform.dom.DOMResult/feature";
	
	public static class InterfaceConsts {
		
		public const string PiDisableOutputEscaping = "javax.xml.transform.disable-output-escaping";
		public const string PiEnableOutputEscaping = "javax.xml.transform.enable-output-escaping";
	}
}
```

<h3 id='Javax.Xml.Transform.Dom.DOMSource'>New Type: Javax.Xml.Transform.Dom.DOMSource</h3>

```
public class DOMSource : Java.Lang.Object, Javax.Xml.Transform.ISource {
	
	protected DOMSource (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DOMSource ();
	public DOMSource (Org.W3c.Dom.INode n);
	public DOMSource (Org.W3c.Dom.INode node, string systemID);
	
	public virtual Org.W3c.Dom.INode Node {
		get;
		set;
	}
	public virtual string SystemId {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Feature = "http://javax.xml.transform.dom.DOMSource/feature";
}
```

<h3 id='Javax.Xml.Transform.Dom.IDOMLocator'>New Type: Javax.Xml.Transform.Dom.IDOMLocator</h3>

```
public interface IDOMLocator : IDisposable, Android.Runtime.IJavaObject, Javax.Xml.Transform.ISourceLocator {
	
	Org.W3c.Dom.INode OriginatingNode {
		get;
	}
}
```

<h2 id='Javax.Xml.Transform.Sax'>Namespace: Javax.Xml.Transform.Sax</h2>

<h3 id='Javax.Xml.Transform.Sax.ITemplatesHandler'>New Type: Javax.Xml.Transform.Sax.ITemplatesHandler</h3>

```
public interface ITemplatesHandler : Org.Xml.Sax.IContentHandler, IDisposable, Android.Runtime.IJavaObject {
	
	string SystemId {
		get;
		set;
	}
	Javax.Xml.Transform.ITemplates Templates {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.Sax.ITransformerHandler'>New Type: Javax.Xml.Transform.Sax.ITransformerHandler</h3>

```
public interface ITransformerHandler : Org.Xml.Sax.IContentHandler, IDisposable, Org.Xml.Sax.IDTDHandler, Android.Runtime.IJavaObject, Org.Xml.Sax.Ext.ILexicalHandler {
	
	void SetResult (Javax.Xml.Transform.IResult result);
	
	string SystemId {
		get;
		set;
	}
	Javax.Xml.Transform.Transformer Transformer {
		get;
	}
}
```

<h3 id='Javax.Xml.Transform.Sax.SAXResult'>New Type: Javax.Xml.Transform.Sax.SAXResult</h3>

```
public class SAXResult : Java.Lang.Object, Javax.Xml.Transform.IResult {
	
	protected SAXResult (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SAXResult ();
	public SAXResult (Org.Xml.Sax.IContentHandler handler);
	
	public virtual Org.Xml.Sax.IContentHandler Handler {
		get;
		set;
	}
	public virtual Org.Xml.Sax.Ext.ILexicalHandler LexicalHandler {
		get;
		set;
	}
	public virtual string SystemId {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Feature = "http://javax.xml.transform.sax.SAXResult/feature";
	
	public static class InterfaceConsts {
		
		public const string PiDisableOutputEscaping = "javax.xml.transform.disable-output-escaping";
		public const string PiEnableOutputEscaping = "javax.xml.transform.enable-output-escaping";
	}
}
```

<h3 id='Javax.Xml.Transform.Sax.SAXSource'>New Type: Javax.Xml.Transform.Sax.SAXSource</h3>

```
public class SAXSource : Java.Lang.Object, Javax.Xml.Transform.ISource {
	
	protected SAXSource (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SAXSource ();
	public SAXSource (Org.Xml.Sax.InputSource inputSource);
	public SAXSource (Org.Xml.Sax.IXMLReader reader, Org.Xml.Sax.InputSource inputSource);
	
	public static Org.Xml.Sax.InputSource SourceToInputSource (Javax.Xml.Transform.ISource source);
	
	public virtual Org.Xml.Sax.InputSource InputSource {
		get;
		set;
	}
	public virtual string SystemId {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual Org.Xml.Sax.IXMLReader XMLReader {
		get;
		set;
	}
	
	public const string Feature = "http://javax.xml.transform.sax.SAXSource/feature";
}
```

<h3 id='Javax.Xml.Transform.Sax.SAXTransformerFactory'>New Type: Javax.Xml.Transform.Sax.SAXTransformerFactory</h3>

```
public abstract class SAXTransformerFactory : Javax.Xml.Transform.TransformerFactory {
	
	protected SAXTransformerFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected SAXTransformerFactory ();
	
	public abstract ITemplatesHandler NewTemplatesHandler ();
	public abstract ITransformerHandler NewTransformerHandler ();
	public abstract ITransformerHandler NewTransformerHandler (Javax.Xml.Transform.ISource src);
	public abstract ITransformerHandler NewTransformerHandler (Javax.Xml.Transform.ITemplates templates);
	public abstract Org.Xml.Sax.IXMLFilter NewXMLFilter (Javax.Xml.Transform.ISource src);
	public abstract Org.Xml.Sax.IXMLFilter NewXMLFilter (Javax.Xml.Transform.ITemplates templates);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Feature = "http://javax.xml.transform.sax.SAXTransformerFactory/feature";
	public const string FeatureXmlfilter = "http://javax.xml.transform.sax.SAXTransformerFactory/feature/xmlfilter";
}
```

<h2 id='Javax.Xml.Transform.Stream'>Namespace: Javax.Xml.Transform.Stream</h2>

<h3 id='Javax.Xml.Transform.Stream.StreamResult'>New Type: Javax.Xml.Transform.Stream.StreamResult</h3>

```
public class StreamResult : Java.Lang.Object, Javax.Xml.Transform.IResult {
	
	protected StreamResult (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StreamResult ();
	public StreamResult (Java.IO.File f);
	public StreamResult (System.IO.Stream outputStream);
	public StreamResult (Java.IO.Writer writer);
	public StreamResult (string systemId);
	
	public virtual void SetSystemId (Java.IO.File f);
	
	public virtual System.IO.Stream OutputStream {
		get;
		set;
	}
	public virtual string SystemId {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual Java.IO.Writer Writer {
		get;
		set;
	}
	
	public const string Feature = "http://javax.xml.transform.stream.StreamResult/feature";
	
	public static class InterfaceConsts {
		
		public const string PiDisableOutputEscaping = "javax.xml.transform.disable-output-escaping";
		public const string PiEnableOutputEscaping = "javax.xml.transform.enable-output-escaping";
	}
}
```

<h3 id='Javax.Xml.Transform.Stream.StreamSource'>New Type: Javax.Xml.Transform.Stream.StreamSource</h3>

```
public class StreamSource : Java.Lang.Object, Javax.Xml.Transform.ISource {
	
	protected StreamSource (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StreamSource ();
	public StreamSource (Java.IO.File f);
	public StreamSource (System.IO.Stream inputStream);
	public StreamSource (System.IO.Stream inputStream, string systemId);
	public StreamSource (Java.IO.Reader reader);
	public StreamSource (Java.IO.Reader reader, string systemId);
	public StreamSource (string systemId);
	
	public virtual void SetSystemId (Java.IO.File f);
	
	public virtual System.IO.Stream InputStream {
		get;
		set;
	}
	public virtual string PublicId {
		get;
		set;
	}
	public virtual Java.IO.Reader Reader {
		get;
		set;
	}
	public virtual string SystemId {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Feature = "http://javax.xml.transform.stream.StreamSource/feature";
}
```

<h2 id='Javax.Xml.Validation'>Namespace: Javax.Xml.Validation</h2>

<h3 id='Javax.Xml.Validation.Schema'>New Type: Javax.Xml.Validation.Schema</h3>

```
public abstract class Schema : Java.Lang.Object {
	
	protected Schema (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Schema ();
	
	public abstract Validator NewValidator ();
	public abstract ValidatorHandler NewValidatorHandler ();
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Validation.SchemaFactory'>New Type: Javax.Xml.Validation.SchemaFactory</h3>

```
public abstract class SchemaFactory : Java.Lang.Object {
	
	protected SchemaFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected SchemaFactory ();
	
	public static SchemaFactory NewInstance (string schemaLanguage);
	public static SchemaFactory NewInstance (string p0, string p1, Java.Lang.ClassLoader p2);
	public virtual bool GetFeature (string name);
	public virtual Java.Lang.Object GetProperty (string name);
	public abstract bool IsSchemaLanguageSupported (string schemaLanguage);
	public abstract Schema NewSchema ();
	public virtual Schema NewSchema (Java.IO.File schema);
	public virtual Schema NewSchema (Javax.Xml.Transform.ISource schema);
	public abstract Schema NewSchema (Javax.Xml.Transform.ISource[] schemas);
	public virtual Schema NewSchema (Java.Net.URL schema);
	public virtual void SetFeature (string name, bool value);
	public virtual void SetProperty (string name, Java.Lang.Object object);
	
	public abstract Org.Xml.Sax.IErrorHandler ErrorHandler {
		get;
		set;
	}
	public abstract Org.W3c.Dom.LS.ILSResourceResolver ResourceResolver {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Validation.SchemaFactoryLoader'>New Type: Javax.Xml.Validation.SchemaFactoryLoader</h3>

```
public abstract class SchemaFactoryLoader : Java.Lang.Object {
	
	protected SchemaFactoryLoader (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected SchemaFactoryLoader ();
	
	public abstract SchemaFactory NewFactory (string schemaLanguage);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Validation.TypeInfoProvider'>New Type: Javax.Xml.Validation.TypeInfoProvider</h3>

```
public abstract class TypeInfoProvider : Java.Lang.Object {
	
	protected TypeInfoProvider (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected TypeInfoProvider ();
	
	public abstract Org.W3c.Dom.ITypeInfo GetAttributeTypeInfo (int index);
	public abstract bool IsIdAttribute (int index);
	public abstract bool IsSpecified (int index);
	
	public abstract Org.W3c.Dom.ITypeInfo ElementTypeInfo {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Validation.Validator'>New Type: Javax.Xml.Validation.Validator</h3>

```
public abstract class Validator : Java.Lang.Object {
	
	protected Validator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected Validator ();
	
	public virtual bool GetFeature (string name);
	public virtual Java.Lang.Object GetProperty (string name);
	public abstract void Reset ();
	public virtual void SetFeature (string name, bool value);
	public virtual void SetProperty (string name, Java.Lang.Object object);
	public virtual void Validate (Javax.Xml.Transform.ISource source);
	public abstract void Validate (Javax.Xml.Transform.ISource source, Javax.Xml.Transform.IResult result);
	public System.Threading.Tasks.Task ValidateAsync (Javax.Xml.Transform.ISource source);
	public System.Threading.Tasks.Task ValidateAsync (Javax.Xml.Transform.ISource source, Javax.Xml.Transform.IResult result);
	
	public abstract Org.Xml.Sax.IErrorHandler ErrorHandler {
		get;
		set;
	}
	public abstract Org.W3c.Dom.LS.ILSResourceResolver ResourceResolver {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Validation.ValidatorHandler'>New Type: Javax.Xml.Validation.ValidatorHandler</h3>

```
public abstract class ValidatorHandler : Java.Lang.Object, Org.Xml.Sax.IContentHandler {
	
	protected ValidatorHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected ValidatorHandler ();
	
	public abstract void Characters (char [] ch, int start, int length);
	public abstract void EndDocument ();
	public abstract void EndElement (string uri, string localName, string qName);
	public abstract void EndPrefixMapping (string prefix);
	public virtual bool GetFeature (string name);
	public virtual Java.Lang.Object GetProperty (string name);
	public abstract void IgnorableWhitespace (char [] ch, int start, int length);
	public abstract void ProcessingInstruction (string target, string data);
	public abstract void SetDocumentLocator (Org.Xml.Sax.ILocator locator);
	public virtual void SetFeature (string name, bool value);
	public virtual void SetProperty (string name, Java.Lang.Object object);
	public abstract void SkippedEntity (string name);
	public abstract void StartDocument ();
	public abstract void StartElement (string uri, string localName, string qName, Org.Xml.Sax.IAttributes atts);
	public abstract void StartPrefixMapping (string prefix, string uri);
	
	public abstract Org.Xml.Sax.IContentHandler ContentHandler {
		get;
		set;
	}
	public abstract Org.Xml.Sax.IErrorHandler ErrorHandler {
		get;
		set;
	}
	public abstract Org.W3c.Dom.LS.ILSResourceResolver ResourceResolver {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public abstract TypeInfoProvider TypeInfoProvider {
		get;
	}
}
```

<h2 id='Javax.Xml.Xpath'>Namespace: Javax.Xml.Xpath</h2>

<h3 id='Javax.Xml.Xpath.IXPath'>New Type: Javax.Xml.Xpath.IXPath</h3>

```
public interface IXPath : IDisposable, Android.Runtime.IJavaObject {
	
	IXPathExpression Compile (string expression);
	string Evaluate (string expression, Org.Xml.Sax.InputSource source);
	Java.Lang.Object Evaluate (string expression, Org.Xml.Sax.InputSource source, Javax.Xml.Namespace.QName returnType);
	string Evaluate (string expression, Java.Lang.Object item);
	Java.Lang.Object Evaluate (string expression, Java.Lang.Object item, Javax.Xml.Namespace.QName returnType);
	void Reset ();
	
	Javax.Xml.Namespace.INamespaceContext NamespaceContext {
		get;
		set;
	}
	IXPathFunctionResolver XPathFunctionResolver {
		get;
		set;
	}
	IXPathVariableResolver XPathVariableResolver {
		get;
		set;
	}
}
```

<h3 id='Javax.Xml.Xpath.IXPathExpression'>New Type: Javax.Xml.Xpath.IXPathExpression</h3>

```
public interface IXPathExpression : IDisposable, Android.Runtime.IJavaObject {
	
	string Evaluate (Org.Xml.Sax.InputSource source);
	Java.Lang.Object Evaluate (Org.Xml.Sax.InputSource source, Javax.Xml.Namespace.QName returnType);
	string Evaluate (Java.Lang.Object item);
	Java.Lang.Object Evaluate (Java.Lang.Object item, Javax.Xml.Namespace.QName returnType);
}
```

<h3 id='Javax.Xml.Xpath.IXPathFunction'>New Type: Javax.Xml.Xpath.IXPathFunction</h3>

```
public interface IXPathFunction : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object Evaluate (System.Collections.IList args);
}
```

<h3 id='Javax.Xml.Xpath.IXPathFunctionResolver'>New Type: Javax.Xml.Xpath.IXPathFunctionResolver</h3>

```
public interface IXPathFunctionResolver : IDisposable, Android.Runtime.IJavaObject {
	
	IXPathFunction ResolveFunction (Javax.Xml.Namespace.QName functionName, int arity);
}
```

<h3 id='Javax.Xml.Xpath.IXPathVariableResolver'>New Type: Javax.Xml.Xpath.IXPathVariableResolver</h3>

```
public interface IXPathVariableResolver : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object ResolveVariable (Javax.Xml.Namespace.QName variableName);
}
```

<h3 id='Javax.Xml.Xpath.XPathConstants'>New Type: Javax.Xml.Xpath.XPathConstants</h3>

```
public class XPathConstants : Java.Lang.Object {
	
	protected XPathConstants (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static Javax.Xml.Namespace.QName Boolean {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Node {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Nodeset {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName Number {
		get;
		set;
	}
	public static Javax.Xml.Namespace.QName String {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string DomObjectModel = "http://java.sun.com/jaxp/xpath/dom";
}
```

<h3 id='Javax.Xml.Xpath.XPathException'>New Type: Javax.Xml.Xpath.XPathException</h3>

```
public class XPathException : Java.Lang.Exception {
	
	protected XPathException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public XPathException (string message);
	public XPathException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Xpath.XPathExpressionException'>New Type: Javax.Xml.Xpath.XPathExpressionException</h3>

```
public class XPathExpressionException : XPathException {
	
	protected XPathExpressionException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public XPathExpressionException (string message);
	public XPathExpressionException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Xpath.XPathFactory'>New Type: Javax.Xml.Xpath.XPathFactory</h3>

```
public abstract class XPathFactory : Java.Lang.Object {
	
	protected XPathFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected XPathFactory ();
	
	public static XPathFactory NewInstance ();
	public static XPathFactory NewInstance (string uri);
	public static XPathFactory NewInstance (string uri, string factoryClassName, Java.Lang.ClassLoader classLoader);
	public abstract bool GetFeature (string name);
	public abstract bool IsObjectModelSupported (string objectModel);
	public abstract IXPath NewXPath ();
	public abstract void SetFeature (string name, bool value);
	public abstract void SetXPathFunctionResolver (IXPathFunctionResolver resolver);
	public abstract void SetXPathVariableResolver (IXPathVariableResolver resolver);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string DefaultObjectModelUri = "http://java.sun.com/jaxp/xpath/dom";
	public const string DefaultPropertyName = "javax.xml.xpath.XPathFactory";
}
```

<h3 id='Javax.Xml.Xpath.XPathFactoryConfigurationException'>New Type: Javax.Xml.Xpath.XPathFactoryConfigurationException</h3>

```
public class XPathFactoryConfigurationException : XPathException {
	
	protected XPathFactoryConfigurationException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public XPathFactoryConfigurationException (string message);
	public XPathFactoryConfigurationException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Javax.Xml.Xpath.XPathFunctionException'>New Type: Javax.Xml.Xpath.XPathFunctionException</h3>

```
public class XPathFunctionException : XPathExpressionException {
	
	protected XPathFunctionException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public XPathFunctionException (string message);
	public XPathFunctionException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Commons.Logging'>Namespace: Org.Apache.Commons.Logging</h2>

<h3 id='Org.Apache.Commons.Logging.ILog'>New Type: Org.Apache.Commons.Logging.ILog</h3>

```
public interface ILog : IDisposable, Android.Runtime.IJavaObject {
	
	void Debug (Java.Lang.Object p0);
	void Debug (Java.Lang.Object p0, Java.Lang.Throwable p1);
	void Error (Java.Lang.Object p0);
	void Error (Java.Lang.Object p0, Java.Lang.Throwable p1);
	void Fatal (Java.Lang.Object p0);
	void Fatal (Java.Lang.Object p0, Java.Lang.Throwable p1);
	void Info (Java.Lang.Object p0);
	void Info (Java.Lang.Object p0, Java.Lang.Throwable p1);
	void Trace (Java.Lang.Object p0);
	void Trace (Java.Lang.Object p0, Java.Lang.Throwable p1);
	void Warn (Java.Lang.Object p0);
	void Warn (Java.Lang.Object p0, Java.Lang.Throwable p1);
	
	bool IsDebugEnabled {
		get;
	}
	bool IsErrorEnabled {
		get;
	}
	bool IsFatalEnabled {
		get;
	}
	bool IsInfoEnabled {
		get;
	}
	bool IsTraceEnabled {
		get;
	}
	bool IsWarnEnabled {
		get;
	}
}
```

<h2 id='Org.Apache.Http'>Namespace: Org.Apache.Http</h2>

<h3 id='Org.Apache.Http.ConnectionClosedException'>New Type: Org.Apache.Http.ConnectionClosedException</h3>

```
public class ConnectionClosedException : Java.IO.IOException {
	
	protected ConnectionClosedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnectionClosedException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.HttpException'>New Type: Org.Apache.Http.HttpException</h3>

```
public class HttpException : Java.Lang.Exception {
	
	protected HttpException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpException ();
	public HttpException (string message);
	public HttpException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.HttpHost'>New Type: Org.Apache.Http.HttpHost</h3>

```
public sealed class HttpHost : Java.Lang.Object, Java.Lang.ICloneable {
	
	public HttpHost (string hostname);
	public HttpHost (string hostname, int port);
	public HttpHost (string hostname, int port, string scheme);
	public HttpHost (HttpHost httphost);
	
	public Java.Lang.Object Clone ();
	public string ToHostString ();
	public string ToURI ();
	
	protected string Hostname {
		get;
		set;
	}
	public string HostName {
		get;
	}
	protected string LcHostname {
		get;
		set;
	}
	public int Port {
		get;
	}
	public string SchemeName {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string DefaultSchemeName = "http";
}
```

<h3 id='Org.Apache.Http.HttpStatus'>New Type: Org.Apache.Http.HttpStatus</h3>

```
public abstract class HttpStatus {
	
	public const int ScAccepted = 202;
	public const int ScBadGateway = 502;
	public const int ScBadRequest = 400;
	public const int ScConflict = 409;
	public const int ScContinue = 100;
	public const int ScCreated = 201;
	public const int ScExpectationFailed = 417;
	public const int ScFailedDependency = 424;
	public const int ScForbidden = 403;
	public const int ScGatewayTimeout = 504;
	public const int ScGone = 410;
	public const int ScHttpVersionNotSupported = 505;
	public const int ScInsufficientSpaceOnResource = 419;
	public const int ScInsufficientStorage = 507;
	public const int ScInternalServerError = 500;
	public const int ScLengthRequired = 411;
	public const int ScLocked = 423;
	public const int ScMethodFailure = 420;
	public const int ScMethodNotAllowed = 405;
	public const int ScMovedPermanently = 301;
	public const int ScMovedTemporarily = 302;
	public const int ScMultiStatus = 207;
	public const int ScMultipleChoices = 300;
	public const int ScNoContent = 204;
	public const int ScNonAuthoritativeInformation = 203;
	public const int ScNotAcceptable = 406;
	public const int ScNotFound = 404;
	public const int ScNotImplemented = 501;
	public const int ScNotModified = 304;
	public const int ScOk = 200;
	public const int ScPartialContent = 206;
	public const int ScPaymentRequired = 402;
	public const int ScPreconditionFailed = 412;
	public const int ScProcessing = 102;
	public const int ScProxyAuthenticationRequired = 407;
	public const int ScRequestTimeout = 408;
	public const int ScRequestTooLong = 413;
	public const int ScRequestUriTooLong = 414;
	public const int ScRequestedRangeNotSatisfiable = 416;
	public const int ScResetContent = 205;
	public const int ScSeeOther = 303;
	public const int ScServiceUnavailable = 503;
	public const int ScSwitchingProtocols = 101;
	public const int ScTemporaryRedirect = 307;
	public const int ScUnauthorized = 401;
	public const int ScUnprocessableEntity = 422;
	public const int ScUnsupportedMediaType = 415;
	public const int ScUseProxy = 305;
}
```

<h3 id='Org.Apache.Http.HttpStatusConsts'>New Type: Org.Apache.Http.HttpStatusConsts</h3>

```
[Obsolete]
public abstract class HttpStatusConsts : HttpStatus {
}
```

<h3 id='Org.Apache.Http.HttpVersion'>New Type: Org.Apache.Http.HttpVersion</h3>

```
public sealed class HttpVersion : ProtocolVersion {
	
	public HttpVersion (int major, int minor);
	
	public static HttpVersion Http09 {
		get;
		set;
	}
	public static HttpVersion Http10 {
		get;
		set;
	}
	public static HttpVersion Http11 {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Http = "HTTP";
}
```

<h3 id='Org.Apache.Http.IConnectionReuseStrategy'>New Type: Org.Apache.Http.IConnectionReuseStrategy</h3>

```
public interface IConnectionReuseStrategy : IDisposable, Android.Runtime.IJavaObject {
	
	bool KeepAlive (IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.IFormattedHeader'>New Type: Org.Apache.Http.IFormattedHeader</h3>

```
public interface IFormattedHeader : IDisposable, IHeader, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.Util.CharArrayBuffer Buffer {
		get;
	}
	int ValuePos {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHeader'>New Type: Org.Apache.Http.IHeader</h3>

```
public interface IHeader : IDisposable, Android.Runtime.IJavaObject {
	
	IHeaderElement[] GetElements ();
	
	string Name {
		get;
	}
	string Value {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHeaderElement'>New Type: Org.Apache.Http.IHeaderElement</h3>

```
public interface IHeaderElement : IDisposable, Android.Runtime.IJavaObject {
	
	INameValuePair GetParameter (int index);
	INameValuePair GetParameterByName (string name);
	INameValuePair[] GetParameters ();
	
	string Name {
		get;
	}
	int ParameterCount {
		get;
	}
	string Value {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHeaderElementIterator'>New Type: Org.Apache.Http.IHeaderElementIterator</h3>

```
public interface IHeaderElementIterator : IDisposable, Java.Util.IIterator, Android.Runtime.IJavaObject {
	
	IHeaderElement NextElement ();
	
	bool HasNext {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHeaderIterator'>New Type: Org.Apache.Http.IHeaderIterator</h3>

```
public interface IHeaderIterator : IDisposable, Java.Util.IIterator, Android.Runtime.IJavaObject {
	
	IHeader NextHeader ();
	
	bool HasNext {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHttpClientConnection'>New Type: Org.Apache.Http.IHttpClientConnection</h3>

```
public interface IHttpClientConnection : IDisposable, IHttpConnection, Android.Runtime.IJavaObject {
	
	void Flush ();
	bool IsResponseAvailable (int timeout);
	void ReceiveResponseEntity (IHttpResponse response);
	IHttpResponse ReceiveResponseHeader ();
	void SendRequestEntity (IHttpEntityEnclosingRequest request);
	void SendRequestHeader (IHttpRequest request);
}
```

<h3 id='Org.Apache.Http.IHttpClientConnectionExtensions'>New Type: Org.Apache.Http.IHttpClientConnectionExtensions</h3>

```
public static class IHttpClientConnectionExtensions {
	
	public static System.Threading.Tasks.Task FlushAsync (IHttpClientConnection self);
	public static System.Threading.Tasks.Task ReceiveResponseHeaderAsync (IHttpClientConnection self);
	public static System.Threading.Tasks.Task SendRequestEntityAsync (IHttpClientConnection self, IHttpEntityEnclosingRequest request);
	public static System.Threading.Tasks.Task SendRequestHeaderAsync (IHttpClientConnection self, IHttpRequest request);
}
```

<h3 id='Org.Apache.Http.IHttpConnection'>New Type: Org.Apache.Http.IHttpConnection</h3>

```
public interface IHttpConnection : IDisposable, Android.Runtime.IJavaObject {
	
	void Close ();
	void Shutdown ();
	
	bool IsOpen {
		get;
	}
	bool IsStale {
		get;
	}
	IHttpConnectionMetrics Metrics {
		get;
	}
	int SocketTimeout {
		get;
		set;
	}
}
```

<h3 id='Org.Apache.Http.IHttpConnectionMetrics'>New Type: Org.Apache.Http.IHttpConnectionMetrics</h3>

```
public interface IHttpConnectionMetrics : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object GetMetric (string metricName);
	void Reset ();
	
	long ReceivedBytesCount {
		get;
	}
	long RequestCount {
		get;
	}
	long ResponseCount {
		get;
	}
	long SentBytesCount {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHttpEntity'>New Type: Org.Apache.Http.IHttpEntity</h3>

```
public interface IHttpEntity : IDisposable, Android.Runtime.IJavaObject {
	
	void ConsumeContent ();
	void WriteTo (System.IO.Stream outstream);
	
	System.IO.Stream Content {
		get;
	}
	IHeader ContentEncoding {
		get;
	}
	long ContentLength {
		get;
	}
	IHeader ContentType {
		get;
	}
	bool IsChunked {
		get;
	}
	bool IsRepeatable {
		get;
	}
	bool IsStreaming {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHttpEntityEnclosingRequest'>New Type: Org.Apache.Http.IHttpEntityEnclosingRequest</h3>

```
public interface IHttpEntityEnclosingRequest : IDisposable, IHttpMessage, IHttpRequest, Android.Runtime.IJavaObject {
	
	bool ExpectContinue ();
	
	IHttpEntity Entity {
		get;
		set;
	}
}
```

<h3 id='Org.Apache.Http.IHttpEntityExtensions'>New Type: Org.Apache.Http.IHttpEntityExtensions</h3>

```
public static class IHttpEntityExtensions {
	
	public static System.Threading.Tasks.Task WriteToAsync (IHttpEntity self, System.IO.Stream outstream);
}
```

<h3 id='Org.Apache.Http.IHttpInetConnection'>New Type: Org.Apache.Http.IHttpInetConnection</h3>

```
public interface IHttpInetConnection : IDisposable, IHttpConnection, Android.Runtime.IJavaObject {
	
	Java.Net.InetAddress LocalAddress {
		get;
	}
	int LocalPort {
		get;
	}
	Java.Net.InetAddress RemoteAddress {
		get;
	}
	int RemotePort {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHttpMessage'>New Type: Org.Apache.Http.IHttpMessage</h3>

```
public interface IHttpMessage : IDisposable, Android.Runtime.IJavaObject {
	
	void AddHeader (IHeader header);
	void AddHeader (string name, string value);
	bool ContainsHeader (string name);
	IHeader[] GetAllHeaders ();
	IHeader GetFirstHeader (string name);
	IHeader[] GetHeaders (string name);
	IHeader GetLastHeader (string name);
	IHeaderIterator HeaderIterator ();
	IHeaderIterator HeaderIterator (string name);
	void RemoveHeader (IHeader header);
	void RemoveHeaders (string name);
	void SetHeader (IHeader header);
	void SetHeader (string name, string value);
	void SetHeaders (IHeader[] headers);
	
	Org.Apache.Http.Params.IHttpParams Params {
		get;
		set;
	}
	ProtocolVersion ProtocolVersion {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHttpRequest'>New Type: Org.Apache.Http.IHttpRequest</h3>

```
public interface IHttpRequest : IDisposable, IHttpMessage, Android.Runtime.IJavaObject {
	
	IRequestLine RequestLine {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IHttpRequestFactory'>New Type: Org.Apache.Http.IHttpRequestFactory</h3>

```
public interface IHttpRequestFactory : IDisposable, Android.Runtime.IJavaObject {
	
	IHttpRequest NewHttpRequest (IRequestLine requestline);
	IHttpRequest NewHttpRequest (string method, string uri);
}
```

<h3 id='Org.Apache.Http.IHttpRequestInterceptor'>New Type: Org.Apache.Http.IHttpRequestInterceptor</h3>

```
public interface IHttpRequestInterceptor : IDisposable, Android.Runtime.IJavaObject {
	
	void Process (IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.IHttpResponse'>New Type: Org.Apache.Http.IHttpResponse</h3>

```
public interface IHttpResponse : IDisposable, IHttpMessage, Android.Runtime.IJavaObject {
	
	void SetReasonPhrase (string reason);
	void SetStatusCode (int code);
	void SetStatusLine (ProtocolVersion ver, int code);
	void SetStatusLine (ProtocolVersion ver, int code, string reason);
	
	IHttpEntity Entity {
		get;
		set;
	}
	Java.Util.Locale Locale {
		get;
		set;
	}
	IStatusLine StatusLine {
		get;
		set;
	}
}
```

<h3 id='Org.Apache.Http.IHttpResponseFactory'>New Type: Org.Apache.Http.IHttpResponseFactory</h3>

```
public interface IHttpResponseFactory : IDisposable, Android.Runtime.IJavaObject {
	
	IHttpResponse NewHttpResponse (IStatusLine statusline, Org.Apache.Http.Protocol.IHttpContext context);
	IHttpResponse NewHttpResponse (ProtocolVersion ver, int status, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.IHttpResponseInterceptor'>New Type: Org.Apache.Http.IHttpResponseInterceptor</h3>

```
public interface IHttpResponseInterceptor : IDisposable, Android.Runtime.IJavaObject {
	
	void Process (IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.IHttpServerConnection'>New Type: Org.Apache.Http.IHttpServerConnection</h3>

```
public interface IHttpServerConnection : IDisposable, IHttpConnection, Android.Runtime.IJavaObject {
	
	void Flush ();
	void ReceiveRequestEntity (IHttpEntityEnclosingRequest request);
	IHttpRequest ReceiveRequestHeader ();
	void SendResponseEntity (IHttpResponse response);
	void SendResponseHeader (IHttpResponse response);
}
```

<h3 id='Org.Apache.Http.IHttpServerConnectionExtensions'>New Type: Org.Apache.Http.IHttpServerConnectionExtensions</h3>

```
public static class IHttpServerConnectionExtensions {
	
	public static System.Threading.Tasks.Task FlushAsync (IHttpServerConnection self);
	public static System.Threading.Tasks.Task ReceiveRequestHeaderAsync (IHttpServerConnection self);
	public static System.Threading.Tasks.Task SendResponseEntityAsync (IHttpServerConnection self, IHttpResponse response);
	public static System.Threading.Tasks.Task SendResponseHeaderAsync (IHttpServerConnection self, IHttpResponse response);
}
```

<h3 id='Org.Apache.Http.INameValuePair'>New Type: Org.Apache.Http.INameValuePair</h3>

```
public interface INameValuePair : IDisposable, Android.Runtime.IJavaObject {
	
	string Name {
		get;
	}
	string Value {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IReasonPhraseCatalog'>New Type: Org.Apache.Http.IReasonPhraseCatalog</h3>

```
public interface IReasonPhraseCatalog : IDisposable, Android.Runtime.IJavaObject {
	
	string GetReason (int status, Java.Util.Locale loc);
}
```

<h3 id='Org.Apache.Http.IRequestLine'>New Type: Org.Apache.Http.IRequestLine</h3>

```
public interface IRequestLine : IDisposable, Android.Runtime.IJavaObject {
	
	string Method {
		get;
	}
	ProtocolVersion ProtocolVersion {
		get;
	}
	string Uri {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IStatusLine'>New Type: Org.Apache.Http.IStatusLine</h3>

```
public interface IStatusLine : IDisposable, Android.Runtime.IJavaObject {
	
	ProtocolVersion ProtocolVersion {
		get;
	}
	string ReasonPhrase {
		get;
	}
	int StatusCode {
		get;
	}
}
```

<h3 id='Org.Apache.Http.ITokenIterator'>New Type: Org.Apache.Http.ITokenIterator</h3>

```
public interface ITokenIterator : IDisposable, Java.Util.IIterator, Android.Runtime.IJavaObject {
	
	string NextToken ();
	
	bool HasNext {
		get;
	}
}
```

<h3 id='Org.Apache.Http.MalformedChunkCodingException'>New Type: Org.Apache.Http.MalformedChunkCodingException</h3>

```
public class MalformedChunkCodingException : Java.IO.IOException {
	
	protected MalformedChunkCodingException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MalformedChunkCodingException ();
	public MalformedChunkCodingException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.MethodNotSupportedException'>New Type: Org.Apache.Http.MethodNotSupportedException</h3>

```
public class MethodNotSupportedException : HttpException {
	
	protected MethodNotSupportedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MethodNotSupportedException (string message);
	public MethodNotSupportedException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.NoHttpResponseException'>New Type: Org.Apache.Http.NoHttpResponseException</h3>

```
public class NoHttpResponseException : Java.IO.IOException {
	
	protected NoHttpResponseException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NoHttpResponseException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.ParseException'>New Type: Org.Apache.Http.ParseException</h3>

```
public class ParseException : Java.Lang.RuntimeException {
	
	protected ParseException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ParseException ();
	public ParseException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.ProtocolException'>New Type: Org.Apache.Http.ProtocolException</h3>

```
public class ProtocolException : HttpException {
	
	protected ProtocolException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ProtocolException ();
	public ProtocolException (string message);
	public ProtocolException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.ProtocolVersion'>New Type: Org.Apache.Http.ProtocolVersion</h3>

```
public class ProtocolVersion : Java.Lang.Object, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	protected ProtocolVersion (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ProtocolVersion (string protocol, int major, int minor);
	
	public virtual Java.Lang.Object Clone ();
	public virtual int CompareToVersion (ProtocolVersion that);
	public bool Equals (Java.Lang.Object obj);
	public virtual ProtocolVersion ForVersion (int major, int minor);
	public int GetHashCode ();
	public bool GreaterEquals (ProtocolVersion version);
	public virtual bool IsComparable (ProtocolVersion that);
	public bool LessEquals (ProtocolVersion version);
	
	public int Major {
		get;
	}
	public int Minor {
		get;
	}
	public string Protocol {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.UnsupportedHttpVersionException'>New Type: Org.Apache.Http.UnsupportedHttpVersionException</h3>

```
public class UnsupportedHttpVersionException : ProtocolException {
	
	protected UnsupportedHttpVersionException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public UnsupportedHttpVersionException ();
	public UnsupportedHttpVersionException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Auth.Params'>Namespace: Org.Apache.Http.Auth.Params</h2>

<h3 id='Org.Apache.Http.Auth.Params.AuthPNames'>New Type: Org.Apache.Http.Auth.Params.AuthPNames</h3>

```
public abstract class AuthPNames {
	
	public const string CredentialCharset = "http.auth.credential-charset";
}
```

<h3 id='Org.Apache.Http.Auth.Params.AuthPNamesConsts'>New Type: Org.Apache.Http.Auth.Params.AuthPNamesConsts</h3>

```
[Obsolete]
public abstract class AuthPNamesConsts : AuthPNames {
}
```

<h3 id='Org.Apache.Http.Auth.Params.AuthParamBean'>New Type: Org.Apache.Http.Auth.Params.AuthParamBean</h3>

```
public class AuthParamBean : Org.Apache.Http.Params.HttpAbstractParamBean {
	
	protected AuthParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AuthParamBean (Org.Apache.Http.Params.IHttpParams params);
	
	public virtual void SetCredentialCharset (string charset);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Auth.Params.AuthParams'>New Type: Org.Apache.Http.Auth.Params.AuthParams</h3>

```
public sealed class AuthParams : Java.Lang.Object {
	
	public static string GetCredentialCharset (Org.Apache.Http.Params.IHttpParams params);
	public static void SetCredentialCharset (Org.Apache.Http.Params.IHttpParams params, string charset);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Authentication'>Namespace: Org.Apache.Http.Authentication</h2>

<h3 id='Org.Apache.Http.Authentication.AUTH'>New Type: Org.Apache.Http.Authentication.AUTH</h3>

```
public sealed class AUTH : Java.Lang.Object {
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string ProxyAuth = "Proxy-Authenticate";
	public const string ProxyAuthResp = "Proxy-Authorization";
	public const string WwwAuth = "WWW-Authenticate";
	public const string WwwAuthResp = "Authorization";
}
```

<h3 id='Org.Apache.Http.Authentication.AuthSchemeRegistry'>New Type: Org.Apache.Http.Authentication.AuthSchemeRegistry</h3>

```
public sealed class AuthSchemeRegistry : Java.Lang.Object {
	
	public AuthSchemeRegistry ();
	
	public IAuthScheme GetAuthScheme (string name, Org.Apache.Http.Params.IHttpParams params);
	public void Register (string name, IAuthSchemeFactory factory);
	public void SetItems (System.Collections.Generic.IDictionary map);
	public void Unregister (string name);
	
	public System.Collections.Generic.IList SchemeNames {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.AuthScope'>New Type: Org.Apache.Http.Authentication.AuthScope</h3>

```
public class AuthScope : Java.Lang.Object {
	
	protected AuthScope (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AuthScope (string host, int port);
	public AuthScope (string host, int port, string realm);
	public AuthScope (string host, int port, string realm, string scheme);
	public AuthScope (AuthScope authscope);
	
	public virtual int Match (AuthScope that);
	
	public static AuthScope Any {
		get;
		set;
	}
	public static string AnyHost {
		get;
		set;
	}
	public static string AnyRealm {
		get;
		set;
	}
	public static string AnyScheme {
		get;
		set;
	}
	public virtual string Host {
		get;
	}
	public virtual int Port {
		get;
	}
	public virtual string Realm {
		get;
	}
	public virtual string Scheme {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int AnyPort = -1;
}
```

<h3 id='Org.Apache.Http.Authentication.AuthState'>New Type: Org.Apache.Http.Authentication.AuthState</h3>

```
public class AuthState : Java.Lang.Object {
	
	protected AuthState (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AuthState ();
	
	public virtual void Invalidate ();
	
	public virtual IAuthScheme AuthScheme {
		get;
		set;
	}
	public virtual AuthScope AuthScope {
		get;
		set;
	}
	public virtual ICredentials Credentials {
		get;
		set;
	}
	public virtual bool IsValid {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.AuthenticationException'>New Type: Org.Apache.Http.Authentication.AuthenticationException</h3>

```
public class AuthenticationException : Org.Apache.Http.ProtocolException {
	
	protected AuthenticationException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AuthenticationException ();
	public AuthenticationException (string message);
	public AuthenticationException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.BasicUserPrincipal'>New Type: Org.Apache.Http.Authentication.BasicUserPrincipal</h3>

```
public sealed class BasicUserPrincipal : Java.Lang.Object, Java.Security.IPrincipal {
	
	public BasicUserPrincipal (string username);
	
	public string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.IAuthScheme'>New Type: Org.Apache.Http.Authentication.IAuthScheme</h3>

```
public interface IAuthScheme : IDisposable, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.IHeader Authenticate (ICredentials credentials, Org.Apache.Http.IHttpRequest request);
	string GetParameter (string name);
	void ProcessChallenge (Org.Apache.Http.IHeader header);
	
	bool IsComplete {
		get;
	}
	bool IsConnectionBased {
		get;
	}
	string Realm {
		get;
	}
	string SchemeName {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.IAuthSchemeFactory'>New Type: Org.Apache.Http.Authentication.IAuthSchemeFactory</h3>

```
public interface IAuthSchemeFactory : IDisposable, Android.Runtime.IJavaObject {
	
	IAuthScheme NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

<h3 id='Org.Apache.Http.Authentication.ICredentials'>New Type: Org.Apache.Http.Authentication.ICredentials</h3>

```
public interface ICredentials : IDisposable, Android.Runtime.IJavaObject {
	
	string Password {
		get;
	}
	Java.Security.IPrincipal UserPrincipal {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.InvalidCredentialsException'>New Type: Org.Apache.Http.Authentication.InvalidCredentialsException</h3>

```
public class InvalidCredentialsException : AuthenticationException {
	
	protected InvalidCredentialsException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public InvalidCredentialsException ();
	public InvalidCredentialsException (string message);
	public InvalidCredentialsException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.MalformedChallengeException'>New Type: Org.Apache.Http.Authentication.MalformedChallengeException</h3>

```
public class MalformedChallengeException : Org.Apache.Http.ProtocolException {
	
	protected MalformedChallengeException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MalformedChallengeException ();
	public MalformedChallengeException (string message);
	public MalformedChallengeException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.NTCredentials'>New Type: Org.Apache.Http.Authentication.NTCredentials</h3>

```
public class NTCredentials : Java.Lang.Object, ICredentials {
	
	protected NTCredentials (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NTCredentials (string usernamePassword);
	public NTCredentials (string userName, string password, string workstation, string domain);
	
	public virtual string Domain {
		get;
	}
	public virtual string Password {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string UserName {
		get;
	}
	public virtual Java.Security.IPrincipal UserPrincipal {
		get;
	}
	public virtual string Workstation {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.NTUserPrincipal'>New Type: Org.Apache.Http.Authentication.NTUserPrincipal</h3>

```
public class NTUserPrincipal : Java.Lang.Object, Java.Security.IPrincipal {
	
	protected NTUserPrincipal (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NTUserPrincipal (string domain, string username);
	
	public virtual string Domain {
		get;
	}
	public virtual string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string Username {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Authentication.UsernamePasswordCredentials'>New Type: Org.Apache.Http.Authentication.UsernamePasswordCredentials</h3>

```
public class UsernamePasswordCredentials : Java.Lang.Object, ICredentials {
	
	protected UsernamePasswordCredentials (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public UsernamePasswordCredentials (string usernamePassword);
	public UsernamePasswordCredentials (string userName, string password);
	
	public virtual string Password {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string UserName {
		get;
	}
	public virtual Java.Security.IPrincipal UserPrincipal {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Client'>Namespace: Org.Apache.Http.Client</h2>

<h3 id='Org.Apache.Http.Client.CircularRedirectException'>New Type: Org.Apache.Http.Client.CircularRedirectException</h3>

```
public class CircularRedirectException : RedirectException {
	
	protected CircularRedirectException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CircularRedirectException ();
	public CircularRedirectException (string message);
	public CircularRedirectException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.ClientProtocolException'>New Type: Org.Apache.Http.Client.ClientProtocolException</h3>

```
public class ClientProtocolException : Java.IO.IOException {
	
	protected ClientProtocolException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ClientProtocolException ();
	public ClientProtocolException (string s);
	public ClientProtocolException (string message, Java.Lang.Throwable cause);
	public ClientProtocolException (Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.HttpResponseException'>New Type: Org.Apache.Http.Client.HttpResponseException</h3>

```
public class HttpResponseException : ClientProtocolException {
	
	protected HttpResponseException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpResponseException (int statusCode, string s);
	
	public virtual int StatusCode {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.IAuthenticationHandler'>New Type: Org.Apache.Http.Client.IAuthenticationHandler</h3>

```
public interface IAuthenticationHandler : IDisposable, Android.Runtime.IJavaObject {
	
	System.Collections.Generic.IDictionary GetChallenges (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	bool IsAuthenticationRequested (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	Org.Apache.Http.Authentication.IAuthScheme SelectScheme (System.Collections.Generic.IDictionary challenges, Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Client.ICookieStore'>New Type: Org.Apache.Http.Client.ICookieStore</h3>

```
public interface ICookieStore : IDisposable, Android.Runtime.IJavaObject {
	
	void AddCookie (Org.Apache.Http.Cookies.ICookie cookie);
	void Clear ();
	bool ClearExpired (Java.Util.Date date);
	
	System.Collections.Generic.IList Cookies {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.ICredentialsProvider'>New Type: Org.Apache.Http.Client.ICredentialsProvider</h3>

```
public interface ICredentialsProvider : IDisposable, Android.Runtime.IJavaObject {
	
	void Clear ();
	Org.Apache.Http.Authentication.ICredentials GetCredentials (Org.Apache.Http.Authentication.AuthScope authscope);
	void SetCredentials (Org.Apache.Http.Authentication.AuthScope authscope, Org.Apache.Http.Authentication.ICredentials credentials);
}
```

<h3 id='Org.Apache.Http.Client.IHttpClient'>New Type: Org.Apache.Http.Client.IHttpClient</h3>

```
public interface IHttpClient : IDisposable, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request);
	Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	Java.Lang.Object Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, IResponseHandler responseHandler);
	Java.Lang.Object Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
	Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request);
	Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	Java.Lang.Object Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, IResponseHandler responseHandler);
	Java.Lang.Object Execute (Org.Apache.Http.Client.Methods.IHttpUriRequest request, IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
	
	Org.Apache.Http.Conn.IClientConnectionManager ConnectionManager {
		get;
	}
	Org.Apache.Http.Params.IHttpParams Params {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.IHttpClientExtensions'>New Type: Org.Apache.Http.Client.IHttpClientExtensions</h3>

```
public static class IHttpClientExtensions {
	
	public static System.Threading.Tasks.Task ExecuteAsync (IHttpClient self, Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request);
	public static System.Threading.Tasks.Task ExecuteAsync (IHttpClient self, Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	public static System.Threading.Tasks.Task ExecuteAsync (IHttpClient self, Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, IResponseHandler responseHandler);
	public static System.Threading.Tasks.Task ExecuteAsync (IHttpClient self, Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
	public static System.Threading.Tasks.Task ExecuteAsync (IHttpClient self, Org.Apache.Http.Client.Methods.IHttpUriRequest request);
	public static System.Threading.Tasks.Task ExecuteAsync (IHttpClient self, Org.Apache.Http.Client.Methods.IHttpUriRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	public static System.Threading.Tasks.Task ExecuteAsync (IHttpClient self, Org.Apache.Http.Client.Methods.IHttpUriRequest request, IResponseHandler responseHandler);
	public static System.Threading.Tasks.Task ExecuteAsync (IHttpClient self, Org.Apache.Http.Client.Methods.IHttpUriRequest request, IResponseHandler responseHandler, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Client.IHttpRequestRetryHandler'>New Type: Org.Apache.Http.Client.IHttpRequestRetryHandler</h3>

```
public interface IHttpRequestRetryHandler : IDisposable, Android.Runtime.IJavaObject {
	
	bool RetryRequest (Java.IO.IOException exception, int executionCount, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Client.IRedirectHandler'>New Type: Org.Apache.Http.Client.IRedirectHandler</h3>

```
public interface IRedirectHandler : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Net.URI GetLocationURI (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	bool IsRedirectRequested (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Client.IRequestDirector'>New Type: Org.Apache.Http.Client.IRequestDirector</h3>

```
public interface IRequestDirector : IDisposable, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Client.IResponseHandler'>New Type: Org.Apache.Http.Client.IResponseHandler</h3>

```
public interface IResponseHandler : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object HandleResponse (Org.Apache.Http.IHttpResponse response);
}
```

<h3 id='Org.Apache.Http.Client.IUserTokenHandler'>New Type: Org.Apache.Http.Client.IUserTokenHandler</h3>

```
public interface IUserTokenHandler : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object GetUserToken (Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Client.NonRepeatableRequestException'>New Type: Org.Apache.Http.Client.NonRepeatableRequestException</h3>

```
public class NonRepeatableRequestException : Org.Apache.Http.ProtocolException {
	
	protected NonRepeatableRequestException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NonRepeatableRequestException ();
	public NonRepeatableRequestException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.RedirectException'>New Type: Org.Apache.Http.Client.RedirectException</h3>

```
public class RedirectException : Org.Apache.Http.ProtocolException {
	
	protected RedirectException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RedirectException ();
	public RedirectException (string message);
	public RedirectException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Client.Entity'>Namespace: Org.Apache.Http.Client.Entity</h2>

<h3 id='Org.Apache.Http.Client.Entity.UrlEncodedFormEntity'>New Type: Org.Apache.Http.Client.Entity.UrlEncodedFormEntity</h3>

```
public class UrlEncodedFormEntity : Org.Apache.Http.Entity.StringEntity {
	
	protected UrlEncodedFormEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public UrlEncodedFormEntity (System.Collections.Generic.IList parameters);
	public UrlEncodedFormEntity (System.Collections.Generic.IList parameters, string encoding);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Client.Methods'>Namespace: Org.Apache.Http.Client.Methods</h2>

<h3 id='Org.Apache.Http.Client.Methods.HttpDelete'>New Type: Org.Apache.Http.Client.Methods.HttpDelete</h3>

```
public class HttpDelete : HttpRequestBase {
	
	protected HttpDelete (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpDelete ();
	public HttpDelete (string uri);
	public HttpDelete (Java.Net.URI uri);
	
	public override string Method {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string MethodName = "DELETE";
}
```

<h3 id='Org.Apache.Http.Client.Methods.HttpEntityEnclosingRequestBase'>New Type: Org.Apache.Http.Client.Methods.HttpEntityEnclosingRequestBase</h3>

```
public abstract class HttpEntityEnclosingRequestBase : HttpRequestBase, Org.Apache.Http.IHttpEntityEnclosingRequest {
	
	protected HttpEntityEnclosingRequestBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpEntityEnclosingRequestBase ();
	
	public virtual bool ExpectContinue ();
	
	public virtual Org.Apache.Http.IHttpEntity Entity {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.Methods.HttpGet'>New Type: Org.Apache.Http.Client.Methods.HttpGet</h3>

```
public class HttpGet : HttpRequestBase {
	
	protected HttpGet (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpGet ();
	public HttpGet (string uri);
	public HttpGet (Java.Net.URI uri);
	
	public override string Method {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string MethodName = "GET";
}
```

<h3 id='Org.Apache.Http.Client.Methods.HttpHead'>New Type: Org.Apache.Http.Client.Methods.HttpHead</h3>

```
public class HttpHead : HttpRequestBase {
	
	protected HttpHead (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpHead ();
	public HttpHead (string uri);
	public HttpHead (Java.Net.URI uri);
	
	public override string Method {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string MethodName = "HEAD";
}
```

<h3 id='Org.Apache.Http.Client.Methods.HttpOptions'>New Type: Org.Apache.Http.Client.Methods.HttpOptions</h3>

```
public class HttpOptions : HttpRequestBase {
	
	protected HttpOptions (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpOptions ();
	public HttpOptions (string uri);
	public HttpOptions (Java.Net.URI uri);
	
	public virtual System.Collections.Generic.ICollection GetAllowedMethods (Org.Apache.Http.IHttpResponse response);
	
	public override string Method {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string MethodName = "OPTIONS";
}
```

<h3 id='Org.Apache.Http.Client.Methods.HttpPost'>New Type: Org.Apache.Http.Client.Methods.HttpPost</h3>

```
public class HttpPost : HttpEntityEnclosingRequestBase {
	
	protected HttpPost (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpPost ();
	public HttpPost (string uri);
	public HttpPost (Java.Net.URI uri);
	
	public override string Method {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string MethodName = "POST";
}
```

<h3 id='Org.Apache.Http.Client.Methods.HttpPut'>New Type: Org.Apache.Http.Client.Methods.HttpPut</h3>

```
public class HttpPut : HttpEntityEnclosingRequestBase {
	
	protected HttpPut (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpPut ();
	public HttpPut (string uri);
	public HttpPut (Java.Net.URI uri);
	
	public override string Method {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string MethodName = "PUT";
}
```

<h3 id='Org.Apache.Http.Client.Methods.HttpRequestBase'>New Type: Org.Apache.Http.Client.Methods.HttpRequestBase</h3>

```
public abstract class HttpRequestBase : Org.Apache.Http.Message.AbstractHttpMessage, IAbortableHttpRequest, Java.Lang.ICloneable, Org.Apache.Http.IHttpRequest, IHttpUriRequest {
	
	protected HttpRequestBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpRequestBase ();
	
	public virtual void Abort ();
	public virtual Java.Lang.Object Clone ();
	public virtual void SetConnectionRequest (Org.Apache.Http.Conn.IClientConnectionRequest connRequest);
	public virtual void SetReleaseTrigger (Org.Apache.Http.Conn.IConnectionReleaseTrigger releaseTrigger);
	
	public virtual bool IsAborted {
		get;
	}
	public abstract string Method {
		get;
	}
	public override Org.Apache.Http.ProtocolVersion ProtocolVersion {
		get;
	}
	public virtual Org.Apache.Http.IRequestLine RequestLine {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual Java.Net.URI URI {
		get;
		set;
	}
}
```

<h3 id='Org.Apache.Http.Client.Methods.HttpTrace'>New Type: Org.Apache.Http.Client.Methods.HttpTrace</h3>

```
public class HttpTrace : HttpRequestBase {
	
	protected HttpTrace (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpTrace ();
	public HttpTrace (string uri);
	public HttpTrace (Java.Net.URI uri);
	
	public override string Method {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string MethodName = "TRACE";
}
```

<h3 id='Org.Apache.Http.Client.Methods.IAbortableHttpRequest'>New Type: Org.Apache.Http.Client.Methods.IAbortableHttpRequest</h3>

```
public interface IAbortableHttpRequest : IDisposable, Android.Runtime.IJavaObject {
	
	void Abort ();
	void SetConnectionRequest (Org.Apache.Http.Conn.IClientConnectionRequest connRequest);
	void SetReleaseTrigger (Org.Apache.Http.Conn.IConnectionReleaseTrigger releaseTrigger);
}
```

<h3 id='Org.Apache.Http.Client.Methods.IHttpUriRequest'>New Type: Org.Apache.Http.Client.Methods.IHttpUriRequest</h3>

```
public interface IHttpUriRequest : IDisposable, Org.Apache.Http.IHttpMessage, Org.Apache.Http.IHttpRequest, Android.Runtime.IJavaObject {
	
	void Abort ();
	
	bool IsAborted {
		get;
	}
	string Method {
		get;
	}
	Java.Net.URI URI {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Client.Params'>Namespace: Org.Apache.Http.Client.Params</h2>

<h3 id='Org.Apache.Http.Client.Params.AuthPolicy'>New Type: Org.Apache.Http.Client.Params.AuthPolicy</h3>

```
public sealed class AuthPolicy : Java.Lang.Object {
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Basic = "Basic";
	public const string Digest = "Digest";
	public const string Ntlm = "NTLM";
}
```

<h3 id='Org.Apache.Http.Client.Params.ClientPNames'>New Type: Org.Apache.Http.Client.Params.ClientPNames</h3>

```
public abstract class ClientPNames {
	
	public const string AllowCircularRedirects = "http.protocol.allow-circular-redirects";
	public const string ConnectionManagerFactory = "http.connection-manager.factory-object";
	public const string ConnectionManagerFactoryClassName = "http.connection-manager.factory-class-name";
	public const string CookiePolicy = "http.protocol.cookie-policy";
	public const string DefaultHeaders = "http.default-headers";
	public const string DefaultHost = "http.default-host";
	public const string HandleAuthentication = "http.protocol.handle-authentication";
	public const string HandleRedirects = "http.protocol.handle-redirects";
	public const string MaxRedirects = "http.protocol.max-redirects";
	public const string RejectRelativeRedirect = "http.protocol.reject-relative-redirect";
	public const string VirtualHost = "http.virtual-host";
}
```

<h3 id='Org.Apache.Http.Client.Params.ClientPNamesConsts'>New Type: Org.Apache.Http.Client.Params.ClientPNamesConsts</h3>

```
[Obsolete]
public abstract class ClientPNamesConsts : ClientPNames {
}
```

<h3 id='Org.Apache.Http.Client.Params.ClientParamBean'>New Type: Org.Apache.Http.Client.Params.ClientParamBean</h3>

```
public class ClientParamBean : Org.Apache.Http.Params.HttpAbstractParamBean {
	
	protected ClientParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ClientParamBean (Org.Apache.Http.Params.IHttpParams params);
	
	public virtual void SetAllowCircularRedirects (bool allow);
	public virtual void SetConnectionManagerFactory (Org.Apache.Http.Conn.IClientConnectionManagerFactory factory);
	public virtual void SetConnectionManagerFactoryClassName (string factory);
	public virtual void SetCookiePolicy (string policy);
	public virtual void SetDefaultHeaders (System.Collections.Generic.ICollection headers);
	public virtual void SetDefaultHost (Org.Apache.Http.HttpHost host);
	public virtual void SetHandleAuthentication (bool handle);
	public virtual void SetHandleRedirects (bool handle);
	public virtual void SetMaxRedirects (int maxRedirects);
	public virtual void SetRejectRelativeRedirect (bool reject);
	public virtual void SetVirtualHost (Org.Apache.Http.HttpHost host);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.Params.CookiePolicy'>New Type: Org.Apache.Http.Client.Params.CookiePolicy</h3>

```
public sealed class CookiePolicy : Java.Lang.Object {
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string BestMatch = "best-match";
	public const string BrowserCompatibility = "compatibility";
	public const string Netscape = "netscape";
	public const string Rfc2109 = "rfc2109";
	public const string Rfc2965 = "rfc2965";
}
```

<h3 id='Org.Apache.Http.Client.Params.HttpClientParams'>New Type: Org.Apache.Http.Client.Params.HttpClientParams</h3>

```
public class HttpClientParams : Java.Lang.Object {
	
	protected HttpClientParams (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static string GetCookiePolicy (Org.Apache.Http.Params.IHttpParams params);
	public static bool IsAuthenticating (Org.Apache.Http.Params.IHttpParams params);
	public static bool IsRedirecting (Org.Apache.Http.Params.IHttpParams params);
	public static void SetAuthenticating (Org.Apache.Http.Params.IHttpParams params, bool value);
	public static void SetCookiePolicy (Org.Apache.Http.Params.IHttpParams params, string cookiePolicy);
	public static void SetRedirecting (Org.Apache.Http.Params.IHttpParams params, bool value);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Client.Protocol'>Namespace: Org.Apache.Http.Client.Protocol</h2>

<h3 id='Org.Apache.Http.Client.Protocol.ClientContext'>New Type: Org.Apache.Http.Client.Protocol.ClientContext</h3>

```
public abstract class ClientContext {
	
	public const string AuthSchemePref = "http.auth.scheme-pref";
	public const string AuthschemeRegistry = "http.authscheme-registry";
	public const string CookieOrigin = "http.cookie-origin";
	public const string CookieSpec = "http.cookie-spec";
	public const string CookieStore = "http.cookie-store";
	public const string CookiespecRegistry = "http.cookiespec-registry";
	public const string CredsProvider = "http.auth.credentials-provider";
	public const string ProxyAuthState = "http.auth.proxy-scope";
	public const string TargetAuthState = "http.auth.target-scope";
	public const string UserToken = "http.user-token";
}
```

<h3 id='Org.Apache.Http.Client.Protocol.ClientContextConfigurer'>New Type: Org.Apache.Http.Client.Protocol.ClientContextConfigurer</h3>

```
public class ClientContextConfigurer : Java.Lang.Object {
	
	protected ClientContextConfigurer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ClientContextConfigurer (Org.Apache.Http.Protocol.IHttpContext context);
	
	public virtual void SetAuthSchemePref (System.Collections.Generic.IList list);
	public virtual void SetAuthSchemeRegistry (Org.Apache.Http.Authentication.AuthSchemeRegistry registry);
	public virtual void SetCookieSpecRegistry (Org.Apache.Http.Cookies.CookieSpecRegistry registry);
	public virtual void SetCookieStore (Org.Apache.Http.Client.ICookieStore store);
	public virtual void SetCredentialsProvider (Org.Apache.Http.Client.ICredentialsProvider provider);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const string AuthSchemePref = "http.auth.scheme-pref";
		public const string AuthschemeRegistry = "http.authscheme-registry";
		public const string CookieOrigin = "http.cookie-origin";
		public const string CookieSpec = "http.cookie-spec";
		public const string CookieStore = "http.cookie-store";
		public const string CookiespecRegistry = "http.cookiespec-registry";
		public const string CredsProvider = "http.auth.credentials-provider";
		public const string ProxyAuthState = "http.auth.proxy-scope";
		public const string TargetAuthState = "http.auth.target-scope";
		public const string UserToken = "http.user-token";
	}
}
```

<h3 id='Org.Apache.Http.Client.Protocol.ClientContextConsts'>New Type: Org.Apache.Http.Client.Protocol.ClientContextConsts</h3>

```
[Obsolete]
public abstract class ClientContextConsts : ClientContext {
}
```

<h3 id='Org.Apache.Http.Client.Protocol.RequestAddCookies'>New Type: Org.Apache.Http.Client.Protocol.RequestAddCookies</h3>

```
public class RequestAddCookies : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestAddCookies (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestAddCookies ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.Protocol.RequestDefaultHeaders'>New Type: Org.Apache.Http.Client.Protocol.RequestDefaultHeaders</h3>

```
public class RequestDefaultHeaders : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestDefaultHeaders (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestDefaultHeaders ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.Protocol.RequestProxyAuthentication'>New Type: Org.Apache.Http.Client.Protocol.RequestProxyAuthentication</h3>

```
public class RequestProxyAuthentication : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestProxyAuthentication (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestProxyAuthentication ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.Protocol.RequestTargetAuthentication'>New Type: Org.Apache.Http.Client.Protocol.RequestTargetAuthentication</h3>

```
public class RequestTargetAuthentication : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestTargetAuthentication (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestTargetAuthentication ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.Protocol.ResponseProcessCookies'>New Type: Org.Apache.Http.Client.Protocol.ResponseProcessCookies</h3>

```
public class ResponseProcessCookies : Java.Lang.Object, Org.Apache.Http.IHttpResponseInterceptor {
	
	protected ResponseProcessCookies (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ResponseProcessCookies ();
	
	public virtual void Process (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Client.Utils'>Namespace: Org.Apache.Http.Client.Utils</h2>

<h3 id='Org.Apache.Http.Client.Utils.CloneUtils'>New Type: Org.Apache.Http.Client.Utils.CloneUtils</h3>

```
public class CloneUtils : Java.Lang.Object {
	
	protected CloneUtils (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static Java.Lang.Object Clone (Java.Lang.Object obj);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.Utils.URIUtils'>New Type: Org.Apache.Http.Client.Utils.URIUtils</h3>

```
public class URIUtils : Java.Lang.Object {
	
	protected URIUtils (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static Java.Net.URI CreateURI (string scheme, string host, int port, string path, string query, string fragment);
	public static Java.Net.URI Resolve (Java.Net.URI baseURI, string reference);
	public static Java.Net.URI Resolve (Java.Net.URI baseURI, Java.Net.URI reference);
	public static Java.Net.URI RewriteURI (Java.Net.URI uri, Org.Apache.Http.HttpHost target);
	public static Java.Net.URI RewriteURI (Java.Net.URI uri, Org.Apache.Http.HttpHost target, bool dropFragment);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Client.Utils.URLEncodedUtils'>New Type: Org.Apache.Http.Client.Utils.URLEncodedUtils</h3>

```
public class URLEncodedUtils : Java.Lang.Object {
	
	protected URLEncodedUtils (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public URLEncodedUtils ();
	
	public static string Format (System.Collections.Generic.IList parameters, string encoding);
	public static bool IsEncoded (Org.Apache.Http.IHttpEntity entity);
	public static System.Collections.Generic.IList Parse (Org.Apache.Http.IHttpEntity entity);
	public static void Parse (System.Collections.Generic.IList parameters, Java.Util.Scanner scanner, string encoding);
	public static System.Collections.Generic.IList Parse (Java.Net.URI uri, string encoding);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string ContentType = "application/x-www-form-urlencoded";
}
```

<h2 id='Org.Apache.Http.Conn'>Namespace: Org.Apache.Http.Conn</h2>

<h3 id='Org.Apache.Http.Conn.BasicEofSensorWatcher'>New Type: Org.Apache.Http.Conn.BasicEofSensorWatcher</h3>

```
public class BasicEofSensorWatcher : Java.Lang.Object, IEofSensorWatcher {
	
	protected BasicEofSensorWatcher (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicEofSensorWatcher (IManagedClientConnection conn, bool reuse);
	
	public virtual bool EofDetected (System.IO.Stream wrapped);
	public virtual bool StreamAbort (System.IO.Stream wrapped);
	public virtual bool StreamClosed (System.IO.Stream wrapped);
	
	protected bool AttemptReuse {
		get;
		set;
	}
	protected IManagedClientConnection ManagedConn {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.BasicManagedEntity'>New Type: Org.Apache.Http.Conn.BasicManagedEntity</h3>

```
public class BasicManagedEntity : Org.Apache.Http.Entity.HttpEntityWrapper, IConnectionReleaseTrigger, IEofSensorWatcher {
	
	protected BasicManagedEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicManagedEntity (Org.Apache.Http.IHttpEntity entity, IManagedClientConnection conn, bool reuse);
	
	public virtual void AbortConnection ();
	public virtual bool EofDetected (System.IO.Stream wrapped);
	public virtual void ReleaseConnection ();
	protected virtual void ReleaseManagedConnection ();
	public virtual bool StreamAbort (System.IO.Stream wrapped);
	public virtual bool StreamClosed (System.IO.Stream wrapped);
	
	protected bool AttemptReuse {
		get;
		set;
	}
	protected IManagedClientConnection ManagedConn {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.ConnectTimeoutException'>New Type: Org.Apache.Http.Conn.ConnectTimeoutException</h3>

```
public class ConnectTimeoutException : Java.IO.InterruptedIOException {
	
	protected ConnectTimeoutException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnectTimeoutException ();
	public ConnectTimeoutException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.ConnectionPoolTimeoutException'>New Type: Org.Apache.Http.Conn.ConnectionPoolTimeoutException</h3>

```
public class ConnectionPoolTimeoutException : ConnectTimeoutException {
	
	protected ConnectionPoolTimeoutException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnectionPoolTimeoutException ();
	public ConnectionPoolTimeoutException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.EofSensorInputStream'>New Type: Org.Apache.Http.Conn.EofSensorInputStream</h3>

```
public class EofSensorInputStream : Java.IO.InputStream, IConnectionReleaseTrigger {
	
	protected EofSensorInputStream (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public EofSensorInputStream (System.IO.Stream in, IEofSensorWatcher watcher);
	
	public virtual void AbortConnection ();
	protected virtual void CheckAbort ();
	protected virtual void CheckClose ();
	protected virtual void CheckEOF (int eof);
	public override int Read ();
	public virtual void ReleaseConnection ();
	
	protected virtual bool IsReadAllowed {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	protected System.IO.Stream WrappedStream {
		get;
		set;
	}
}
```

<h3 id='Org.Apache.Http.Conn.HttpHostConnectException'>New Type: Org.Apache.Http.Conn.HttpHostConnectException</h3>

```
public class HttpHostConnectException : Java.Net.ConnectException {
	
	protected HttpHostConnectException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpHostConnectException (Org.Apache.Http.HttpHost host, Java.Net.ConnectException cause);
	
	public virtual Org.Apache.Http.HttpHost Host {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.IClientConnectionManager'>New Type: Org.Apache.Http.Conn.IClientConnectionManager</h3>

```
public interface IClientConnectionManager : IDisposable, Android.Runtime.IJavaObject {
	
	void CloseExpiredConnections ();
	void CloseIdleConnections (long idletime, Java.Util.Concurrent.TimeUnit tunit);
	void ReleaseConnection (IManagedClientConnection conn, long validDuration, Java.Util.Concurrent.TimeUnit timeUnit);
	IClientConnectionRequest RequestConnection (Org.Apache.Http.Conn.Routing.HttpRoute route, Java.Lang.Object state);
	void Shutdown ();
	
	Org.Apache.Http.Conn.Schemes.SchemeRegistry SchemeRegistry {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.IClientConnectionManagerFactory'>New Type: Org.Apache.Http.Conn.IClientConnectionManagerFactory</h3>

```
public interface IClientConnectionManagerFactory : IDisposable, Android.Runtime.IJavaObject {
	
	IClientConnectionManager NewInstance (Org.Apache.Http.Params.IHttpParams params, Org.Apache.Http.Conn.Schemes.SchemeRegistry schemeRegistry);
}
```

<h3 id='Org.Apache.Http.Conn.IClientConnectionOperator'>New Type: Org.Apache.Http.Conn.IClientConnectionOperator</h3>

```
public interface IClientConnectionOperator : IDisposable, Android.Runtime.IJavaObject {
	
	IOperatedClientConnection CreateConnection ();
	void OpenConnection (IOperatedClientConnection conn, Org.Apache.Http.HttpHost target, Java.Net.InetAddress local, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	void UpdateSecureConnection (IOperatedClientConnection conn, Org.Apache.Http.HttpHost target, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
}
```

<h3 id='Org.Apache.Http.Conn.IClientConnectionOperatorExtensions'>New Type: Org.Apache.Http.Conn.IClientConnectionOperatorExtensions</h3>

```
public static class IClientConnectionOperatorExtensions {
	
	public static System.Threading.Tasks.Task OpenConnectionAsync (IClientConnectionOperator self, IOperatedClientConnection conn, Org.Apache.Http.HttpHost target, Java.Net.InetAddress local, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	public static System.Threading.Tasks.Task UpdateSecureConnectionAsync (IClientConnectionOperator self, IOperatedClientConnection conn, Org.Apache.Http.HttpHost target, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
}
```

<h3 id='Org.Apache.Http.Conn.IClientConnectionRequest'>New Type: Org.Apache.Http.Conn.IClientConnectionRequest</h3>

```
public interface IClientConnectionRequest : IDisposable, Android.Runtime.IJavaObject {
	
	void AbortRequest ();
	IManagedClientConnection GetConnection (long timeout, Java.Util.Concurrent.TimeUnit tunit);
}
```

<h3 id='Org.Apache.Http.Conn.IConnectionKeepAliveStrategy'>New Type: Org.Apache.Http.Conn.IConnectionKeepAliveStrategy</h3>

```
public interface IConnectionKeepAliveStrategy : IDisposable, Android.Runtime.IJavaObject {
	
	long GetKeepAliveDuration (Org.Apache.Http.IHttpResponse response, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Conn.IConnectionReleaseTrigger'>New Type: Org.Apache.Http.Conn.IConnectionReleaseTrigger</h3>

```
public interface IConnectionReleaseTrigger : IDisposable, Android.Runtime.IJavaObject {
	
	void AbortConnection ();
	void ReleaseConnection ();
}
```

<h3 id='Org.Apache.Http.Conn.IEofSensorWatcher'>New Type: Org.Apache.Http.Conn.IEofSensorWatcher</h3>

```
public interface IEofSensorWatcher : IDisposable, Android.Runtime.IJavaObject {
	
	bool EofDetected (System.IO.Stream wrapped);
	bool StreamAbort (System.IO.Stream wrapped);
	bool StreamClosed (System.IO.Stream wrapped);
}
```

<h3 id='Org.Apache.Http.Conn.IManagedClientConnection'>New Type: Org.Apache.Http.Conn.IManagedClientConnection</h3>

```
public interface IManagedClientConnection : IConnectionReleaseTrigger, IDisposable, Org.Apache.Http.IHttpClientConnection, Org.Apache.Http.IHttpConnection, Org.Apache.Http.IHttpInetConnection, Android.Runtime.IJavaObject {
	
	void LayerProtocol (Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	void MarkReusable ();
	void Open (Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
	void SetIdleDuration (long duration, Java.Util.Concurrent.TimeUnit unit);
	void TunnelProxy (Org.Apache.Http.HttpHost next, bool secure, Org.Apache.Http.Params.IHttpParams params);
	void TunnelTarget (bool secure, Org.Apache.Http.Params.IHttpParams params);
	void UnmarkReusable ();
	
	bool IsMarkedReusable {
		get;
	}
	bool IsSecure {
		get;
	}
	Org.Apache.Http.Conn.Routing.HttpRoute Route {
		get;
	}
	Javax.Net.Ssl.ISSLSession SSLSession {
		get;
	}
	Java.Lang.Object State {
		get;
		set;
	}
}
```

<h3 id='Org.Apache.Http.Conn.IManagedClientConnectionExtensions'>New Type: Org.Apache.Http.Conn.IManagedClientConnectionExtensions</h3>

```
public static class IManagedClientConnectionExtensions {
	
	public static System.Threading.Tasks.Task OpenAsync (IManagedClientConnection self, Org.Apache.Http.Conn.Routing.HttpRoute route, Org.Apache.Http.Protocol.IHttpContext context, Org.Apache.Http.Params.IHttpParams params);
}
```

<h3 id='Org.Apache.Http.Conn.IOperatedClientConnection'>New Type: Org.Apache.Http.Conn.IOperatedClientConnection</h3>

```
public interface IOperatedClientConnection : IDisposable, Org.Apache.Http.IHttpClientConnection, Org.Apache.Http.IHttpConnection, Org.Apache.Http.IHttpInetConnection, Android.Runtime.IJavaObject {
	
	void OpenCompleted (bool secure, Org.Apache.Http.Params.IHttpParams params);
	void Opening (Java.Net.Socket sock, Org.Apache.Http.HttpHost target);
	void Update (Java.Net.Socket sock, Org.Apache.Http.HttpHost target, bool secure, Org.Apache.Http.Params.IHttpParams params);
	
	bool IsSecure {
		get;
	}
	Java.Net.Socket Socket {
		get;
	}
	Org.Apache.Http.HttpHost TargetHost {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.MultihomePlainSocketFactory'>New Type: Org.Apache.Http.Conn.MultihomePlainSocketFactory</h3>

```
public sealed class MultihomePlainSocketFactory : Java.Lang.Object, Org.Apache.Http.Conn.Schemes.ISocketFactory {
	
	public Java.Net.Socket ConnectSocket (Java.Net.Socket sock, string host, int port, Java.Net.InetAddress localAddress, int localPort, Org.Apache.Http.Params.IHttpParams params);
	public Java.Net.Socket CreateSocket ();
	public bool IsSecure (Java.Net.Socket sock);
	
	public static MultihomePlainSocketFactory SocketFactory {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Conn.Params'>Namespace: Org.Apache.Http.Conn.Params</h2>

<h3 id='Org.Apache.Http.Conn.Params.ConnConnectionPNames'>New Type: Org.Apache.Http.Conn.Params.ConnConnectionPNames</h3>

```
public abstract class ConnConnectionPNames {
	
	public const string MaxStatusLineGarbage = "http.connection.max-status-line-garbage";
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnConnectionPNamesConsts'>New Type: Org.Apache.Http.Conn.Params.ConnConnectionPNamesConsts</h3>

```
[Obsolete]
public abstract class ConnConnectionPNamesConsts : ConnConnectionPNames {
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnConnectionParamBean'>New Type: Org.Apache.Http.Conn.Params.ConnConnectionParamBean</h3>

```
public class ConnConnectionParamBean : Org.Apache.Http.Params.HttpAbstractParamBean {
	
	protected ConnConnectionParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnConnectionParamBean (Org.Apache.Http.Params.IHttpParams params);
	
	public virtual void SetMaxStatusLineGarbage (int maxStatusLineGarbage);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnManagerPNames'>New Type: Org.Apache.Http.Conn.Params.ConnManagerPNames</h3>

```
public abstract class ConnManagerPNames {
	
	public const string MaxConnectionsPerRoute = "http.conn-manager.max-per-route";
	public const string MaxTotalConnections = "http.conn-manager.max-total";
	public const string Timeout = "http.conn-manager.timeout";
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnManagerPNamesConsts'>New Type: Org.Apache.Http.Conn.Params.ConnManagerPNamesConsts</h3>

```
[Obsolete]
public abstract class ConnManagerPNamesConsts : ConnManagerPNames {
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnManagerParamBean'>New Type: Org.Apache.Http.Conn.Params.ConnManagerParamBean</h3>

```
public class ConnManagerParamBean : Org.Apache.Http.Params.HttpAbstractParamBean {
	
	protected ConnManagerParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnManagerParamBean (Org.Apache.Http.Params.IHttpParams params);
	
	public virtual void SetConnectionsPerRoute (ConnPerRouteBean connPerRoute);
	public virtual void SetMaxTotalConnections (int maxConnections);
	public virtual void SetTimeout (long timeout);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnManagerParams'>New Type: Org.Apache.Http.Conn.Params.ConnManagerParams</h3>

```
public sealed class ConnManagerParams : Java.Lang.Object {
	
	public ConnManagerParams ();
	
	public static IConnPerRoute GetMaxConnectionsPerRoute (Org.Apache.Http.Params.IHttpParams params);
	public static int GetMaxTotalConnections (Org.Apache.Http.Params.IHttpParams params);
	public static long GetTimeout (Org.Apache.Http.Params.IHttpParams params);
	public static void SetMaxConnectionsPerRoute (Org.Apache.Http.Params.IHttpParams params, IConnPerRoute connPerRoute);
	public static void SetMaxTotalConnections (Org.Apache.Http.Params.IHttpParams params, int maxTotalConnections);
	public static void SetTimeout (Org.Apache.Http.Params.IHttpParams params, long timeout);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int DefaultMaxTotalConnections = 20;
	
	public static class InterfaceConsts {
		
		public const string MaxConnectionsPerRoute = "http.conn-manager.max-per-route";
		public const string MaxTotalConnections = "http.conn-manager.max-total";
		public const string Timeout = "http.conn-manager.timeout";
	}
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnPerRouteBean'>New Type: Org.Apache.Http.Conn.Params.ConnPerRouteBean</h3>

```
public sealed class ConnPerRouteBean : Java.Lang.Object, IConnPerRoute {
	
	public ConnPerRouteBean ();
	public ConnPerRouteBean (int defaultMax);
	
	public int GetMaxForRoute (Org.Apache.Http.Conn.Routing.HttpRoute route);
	public void SetDefaultMaxPerRoute (int max);
	public void SetMaxForRoute (Org.Apache.Http.Conn.Routing.HttpRoute route, int max);
	public void SetMaxForRoutes (System.Collections.Generic.IDictionary map);
	
	public int DefaultMax {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int DefaultMaxConnectionsPerRoute = 2;
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnRoutePNames'>New Type: Org.Apache.Http.Conn.Params.ConnRoutePNames</h3>

```
public abstract class ConnRoutePNames {
	
	public const string DefaultProxy = "http.route.default-proxy";
	public const string ForcedRoute = "http.route.forced-route";
	public const string LocalAddress = "http.route.local-address";
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnRoutePNamesConsts'>New Type: Org.Apache.Http.Conn.Params.ConnRoutePNamesConsts</h3>

```
[Obsolete]
public abstract class ConnRoutePNamesConsts : ConnRoutePNames {
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnRouteParamBean'>New Type: Org.Apache.Http.Conn.Params.ConnRouteParamBean</h3>

```
public class ConnRouteParamBean : Org.Apache.Http.Params.HttpAbstractParamBean {
	
	protected ConnRouteParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ConnRouteParamBean (Org.Apache.Http.Params.IHttpParams params);
	
	public virtual void SetDefaultProxy (Org.Apache.Http.HttpHost defaultProxy);
	public virtual void SetForcedRoute (Org.Apache.Http.Conn.Routing.HttpRoute route);
	public virtual void SetLocalAddress (Java.Net.InetAddress address);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Params.ConnRouteParams'>New Type: Org.Apache.Http.Conn.Params.ConnRouteParams</h3>

```
public class ConnRouteParams : Java.Lang.Object {
	
	protected ConnRouteParams (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static Org.Apache.Http.HttpHost GetDefaultProxy (Org.Apache.Http.Params.IHttpParams params);
	public static Org.Apache.Http.Conn.Routing.HttpRoute GetForcedRoute (Org.Apache.Http.Params.IHttpParams params);
	public static Java.Net.InetAddress GetLocalAddress (Org.Apache.Http.Params.IHttpParams params);
	public static void SetDefaultProxy (Org.Apache.Http.Params.IHttpParams params, Org.Apache.Http.HttpHost proxy);
	public static void SetForcedRoute (Org.Apache.Http.Params.IHttpParams params, Org.Apache.Http.Conn.Routing.HttpRoute route);
	public static void SetLocalAddress (Org.Apache.Http.Params.IHttpParams params, Java.Net.InetAddress local);
	
	public static Org.Apache.Http.HttpHost NoHost {
		get;
		set;
	}
	public static Org.Apache.Http.Conn.Routing.HttpRoute NoRoute {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const string DefaultProxy = "http.route.default-proxy";
		public const string ForcedRoute = "http.route.forced-route";
		public const string LocalAddress = "http.route.local-address";
	}
}
```

<h3 id='Org.Apache.Http.Conn.Params.IConnPerRoute'>New Type: Org.Apache.Http.Conn.Params.IConnPerRoute</h3>

```
public interface IConnPerRoute : IDisposable, Android.Runtime.IJavaObject {
	
	int GetMaxForRoute (Org.Apache.Http.Conn.Routing.HttpRoute route);
}
```

<h2 id='Org.Apache.Http.Conn.Routing'>Namespace: Org.Apache.Http.Conn.Routing</h2>

<h3 id='Org.Apache.Http.Conn.Routing.BasicRouteDirector'>New Type: Org.Apache.Http.Conn.Routing.BasicRouteDirector</h3>

```
public class BasicRouteDirector : Java.Lang.Object, IHttpRouteDirector {
	
	protected BasicRouteDirector (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicRouteDirector ();
	
	protected virtual int DirectStep (IRouteInfo plan, IRouteInfo fact);
	protected virtual int FirstStep (IRouteInfo plan);
	public virtual int NextStep (IRouteInfo plan, IRouteInfo fact);
	protected virtual int ProxiedStep (IRouteInfo plan, IRouteInfo fact);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const int Complete = 0;
		public const int ConnectProxy = 2;
		public const int ConnectTarget = 1;
		public const int LayerProtocol = 5;
		public const int TunnelProxy = 4;
		public const int TunnelTarget = 3;
		public const int Unreachable = -1;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Routing.HttpRoute'>New Type: Org.Apache.Http.Conn.Routing.HttpRoute</h3>

```
public sealed class HttpRoute : Java.Lang.Object, Java.Lang.ICloneable, IRouteInfo {
	
	public HttpRoute (Org.Apache.Http.HttpHost target);
	public HttpRoute (Org.Apache.Http.HttpHost target, Java.Net.InetAddress local, bool secure);
	public HttpRoute (Org.Apache.Http.HttpHost target, Java.Net.InetAddress local, Org.Apache.Http.HttpHost proxy, bool secure);
	public HttpRoute (Org.Apache.Http.HttpHost target, Java.Net.InetAddress local, Org.Apache.Http.HttpHost proxy, bool secure, RouteInfoTunnelType tunnelled, RouteInfoLayerType layered);
	public HttpRoute (Org.Apache.Http.HttpHost target, Java.Net.InetAddress local, Org.Apache.Http.HttpHost[] proxies, bool secure, RouteInfoTunnelType tunnelled, RouteInfoLayerType layered);
	
	public Java.Lang.Object Clone ();
	public bool Equals (Java.Lang.Object o);
	public int GetHashCode ();
	public Org.Apache.Http.HttpHost GetHopTarget (int hop);
	public string ToString ();
	
	public int HopCount {
		get;
	}
	public bool IsLayered {
		get;
	}
	public bool IsSecure {
		get;
	}
	public bool IsTunnelled {
		get;
	}
	public RouteInfoLayerType LayerType {
		get;
	}
	public Java.Net.InetAddress LocalAddress {
		get;
	}
	public Org.Apache.Http.HttpHost ProxyHost {
		get;
	}
	public Org.Apache.Http.HttpHost TargetHost {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public RouteInfoTunnelType TunnelType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Routing.HttpRouteDirector'>New Type: Org.Apache.Http.Conn.Routing.HttpRouteDirector</h3>

```
public abstract class HttpRouteDirector {
	
	public const int Complete = 0;
	public const int ConnectProxy = 2;
	public const int ConnectTarget = 1;
	public const int LayerProtocol = 5;
	public const int TunnelProxy = 4;
	public const int TunnelTarget = 3;
	public const int Unreachable = -1;
}
```

<h3 id='Org.Apache.Http.Conn.Routing.HttpRouteDirectorConsts'>New Type: Org.Apache.Http.Conn.Routing.HttpRouteDirectorConsts</h3>

```
[Obsolete]
public abstract class HttpRouteDirectorConsts : HttpRouteDirector {
}
```

<h3 id='Org.Apache.Http.Conn.Routing.IHttpRouteDirector'>New Type: Org.Apache.Http.Conn.Routing.IHttpRouteDirector</h3>

```
public interface IHttpRouteDirector : IDisposable, Android.Runtime.IJavaObject {
	
	int NextStep (IRouteInfo plan, IRouteInfo fact);
}
```

<h3 id='Org.Apache.Http.Conn.Routing.IHttpRoutePlanner'>New Type: Org.Apache.Http.Conn.Routing.IHttpRoutePlanner</h3>

```
public interface IHttpRoutePlanner : IDisposable, Android.Runtime.IJavaObject {
	
	HttpRoute DetermineRoute (Org.Apache.Http.HttpHost target, Org.Apache.Http.IHttpRequest request, Org.Apache.Http.Protocol.IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Conn.Routing.IRouteInfo'>New Type: Org.Apache.Http.Conn.Routing.IRouteInfo</h3>

```
public interface IRouteInfo : IDisposable, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.HttpHost GetHopTarget (int hop);
	
	int HopCount {
		get;
	}
	bool IsLayered {
		get;
	}
	bool IsSecure {
		get;
	}
	bool IsTunnelled {
		get;
	}
	RouteInfoLayerType LayerType {
		get;
	}
	Java.Net.InetAddress LocalAddress {
		get;
	}
	Org.Apache.Http.HttpHost ProxyHost {
		get;
	}
	Org.Apache.Http.HttpHost TargetHost {
		get;
	}
	RouteInfoTunnelType TunnelType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Routing.RouteInfoLayerType'>New Type: Org.Apache.Http.Conn.Routing.RouteInfoLayerType</h3>

```
public sealed class RouteInfoLayerType : Java.Lang.Enum {
	
	public static RouteInfoLayerType ValueOf (string name);
	public static RouteInfoLayerType[] Values ();
	
	public static RouteInfoLayerType Layered {
		get;
		set;
	}
	public static RouteInfoLayerType Plain {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Routing.RouteInfoTunnelType'>New Type: Org.Apache.Http.Conn.Routing.RouteInfoTunnelType</h3>

```
public sealed class RouteInfoTunnelType : Java.Lang.Enum {
	
	public static RouteInfoTunnelType ValueOf (string name);
	public static RouteInfoTunnelType[] Values ();
	
	public static RouteInfoTunnelType Plain {
		get;
		set;
	}
	public static RouteInfoTunnelType Tunnelled {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Routing.RouteTracker'>New Type: Org.Apache.Http.Conn.Routing.RouteTracker</h3>

```
public sealed class RouteTracker : Java.Lang.Object, Java.Lang.ICloneable, IRouteInfo {
	
	public RouteTracker (HttpRoute route);
	public RouteTracker (Org.Apache.Http.HttpHost target, Java.Net.InetAddress local);
	
	public Java.Lang.Object Clone ();
	public void ConnectProxy (Org.Apache.Http.HttpHost proxy, bool secure);
	public void ConnectTarget (bool secure);
	public bool Equals (Java.Lang.Object o);
	public int GetHashCode ();
	public Org.Apache.Http.HttpHost GetHopTarget (int hop);
	public void LayerProtocol (bool secure);
	public HttpRoute ToRoute ();
	public string ToString ();
	public void TunnelProxy (Org.Apache.Http.HttpHost proxy, bool secure);
	public void TunnelTarget (bool secure);
	
	public int HopCount {
		get;
	}
	public bool IsConnected {
		get;
	}
	public bool IsLayered {
		get;
	}
	public bool IsSecure {
		get;
	}
	public bool IsTunnelled {
		get;
	}
	public RouteInfoLayerType LayerType {
		get;
	}
	public Java.Net.InetAddress LocalAddress {
		get;
	}
	public Org.Apache.Http.HttpHost ProxyHost {
		get;
	}
	public Org.Apache.Http.HttpHost TargetHost {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public RouteInfoTunnelType TunnelType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Conn.Schemes'>Namespace: Org.Apache.Http.Conn.Schemes</h2>

<h3 id='Org.Apache.Http.Conn.Schemes.IHostNameResolver'>New Type: Org.Apache.Http.Conn.Schemes.IHostNameResolver</h3>

```
public interface IHostNameResolver : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Net.InetAddress Resolve (string hostname);
}
```

<h3 id='Org.Apache.Http.Conn.Schemes.ILayeredSocketFactory'>New Type: Org.Apache.Http.Conn.Schemes.ILayeredSocketFactory</h3>

```
public interface ILayeredSocketFactory : IDisposable, Android.Runtime.IJavaObject, ISocketFactory {
	
	Java.Net.Socket CreateSocket (Java.Net.Socket socket, string host, int port, bool autoClose);
}
```

<h3 id='Org.Apache.Http.Conn.Schemes.ILayeredSocketFactoryExtensions'>New Type: Org.Apache.Http.Conn.Schemes.ILayeredSocketFactoryExtensions</h3>

```
public static class ILayeredSocketFactoryExtensions {
	
	public static System.Threading.Tasks.Task CreateSocketAsync (ILayeredSocketFactory self, Java.Net.Socket socket, string host, int port, bool autoClose);
}
```

<h3 id='Org.Apache.Http.Conn.Schemes.ISocketFactory'>New Type: Org.Apache.Http.Conn.Schemes.ISocketFactory</h3>

```
public interface ISocketFactory : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Net.Socket ConnectSocket (Java.Net.Socket sock, string host, int port, Java.Net.InetAddress localAddress, int localPort, Org.Apache.Http.Params.IHttpParams params);
	Java.Net.Socket CreateSocket ();
	bool IsSecure (Java.Net.Socket sock);
}
```

<h3 id='Org.Apache.Http.Conn.Schemes.ISocketFactoryExtensions'>New Type: Org.Apache.Http.Conn.Schemes.ISocketFactoryExtensions</h3>

```
public static class ISocketFactoryExtensions {
	
	public static System.Threading.Tasks.Task ConnectSocketAsync (ISocketFactory self, Java.Net.Socket sock, string host, int port, Java.Net.InetAddress localAddress, int localPort, Org.Apache.Http.Params.IHttpParams params);
}
```

<h3 id='Org.Apache.Http.Conn.Schemes.PlainSocketFactory'>New Type: Org.Apache.Http.Conn.Schemes.PlainSocketFactory</h3>

```
public sealed class PlainSocketFactory : Java.Lang.Object, ISocketFactory {
	
	public PlainSocketFactory ();
	public PlainSocketFactory (IHostNameResolver nameResolver);
	
	public Java.Net.Socket ConnectSocket (Java.Net.Socket sock, string host, int port, Java.Net.InetAddress localAddress, int localPort, Org.Apache.Http.Params.IHttpParams params);
	public Java.Net.Socket CreateSocket ();
	public bool IsSecure (Java.Net.Socket sock);
	
	public static PlainSocketFactory SocketFactory {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Schemes.Scheme'>New Type: Org.Apache.Http.Conn.Schemes.Scheme</h3>

```
public sealed class Scheme : Java.Lang.Object {
	
	public Scheme (string name, ISocketFactory factory, int port);
	
	public bool Equals (Java.Lang.Object obj);
	public int ResolvePort (int port);
	public string ToString ();
	
	public int DefaultPort {
		get;
	}
	public bool IsLayered {
		get;
	}
	public string Name {
		get;
	}
	public ISocketFactory SocketFactory {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Schemes.SchemeRegistry'>New Type: Org.Apache.Http.Conn.Schemes.SchemeRegistry</h3>

```
public sealed class SchemeRegistry : Java.Lang.Object {
	
	public SchemeRegistry ();
	
	public Scheme Get (string name);
	public Scheme GetScheme (Org.Apache.Http.HttpHost host);
	public Scheme GetScheme (string name);
	public Scheme Register (Scheme sch);
	public void SetItems (System.Collections.Generic.IDictionary map);
	public Scheme Unregister (string name);
	
	public System.Collections.Generic.IList SchemeNames {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Conn.Ssl'>Namespace: Org.Apache.Http.Conn.Ssl</h2>

<h3 id='Org.Apache.Http.Conn.Ssl.AbstractVerifier'>New Type: Org.Apache.Http.Conn.Ssl.AbstractVerifier</h3>

```
public abstract class AbstractVerifier : Java.Lang.Object, Javax.Net.Ssl.IHostnameVerifier, IX509HostnameVerifier {
	
	protected AbstractVerifier (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AbstractVerifier ();
	
	public static bool AcceptableCountryWildcard (string cn);
	public static int CountDots (string s);
	public static string [] GetCNs (Java.Security.Cert.X509Certificate cert);
	public static string [] GetDNSSubjectAlts (Java.Security.Cert.X509Certificate cert);
	public bool Verify (string host, Javax.Net.Ssl.ISSLSession session);
	public void Verify (string host, Javax.Net.Ssl.SSLSocket ssl);
	public abstract void Verify (string host, string [] cns, string [] subjectAlts);
	public void Verify (string host, string [] cns, string [] subjectAlts, bool strictWithSubDomains);
	public void Verify (string host, Java.Security.Cert.X509Certificate cert);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Ssl.AllowAllHostnameVerifier'>New Type: Org.Apache.Http.Conn.Ssl.AllowAllHostnameVerifier</h3>

```
public class AllowAllHostnameVerifier : AbstractVerifier {
	
	protected AllowAllHostnameVerifier (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AllowAllHostnameVerifier ();
	
	public string ToString ();
	public void Verify (string host, string [] cns, string [] subjectAlts);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Ssl.BrowserCompatHostnameVerifier'>New Type: Org.Apache.Http.Conn.Ssl.BrowserCompatHostnameVerifier</h3>

```
public class BrowserCompatHostnameVerifier : AbstractVerifier {
	
	protected BrowserCompatHostnameVerifier (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BrowserCompatHostnameVerifier ();
	
	public string ToString ();
	public void Verify (string host, string [] cns, string [] subjectAlts);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Conn.Ssl.IX509HostnameVerifier'>New Type: Org.Apache.Http.Conn.Ssl.IX509HostnameVerifier</h3>

```
public interface IX509HostnameVerifier : IDisposable, Javax.Net.Ssl.IHostnameVerifier, Android.Runtime.IJavaObject {
	
	bool Verify (string host, Javax.Net.Ssl.ISSLSession session);
	void Verify (string host, Javax.Net.Ssl.SSLSocket ssl);
	void Verify (string host, string [] cns, string [] subjectAlts);
	void Verify (string host, Java.Security.Cert.X509Certificate cert);
}
```

<h3 id='Org.Apache.Http.Conn.Ssl.SSLSocketFactory'>New Type: Org.Apache.Http.Conn.Ssl.SSLSocketFactory</h3>

```
public class SSLSocketFactory : Java.Lang.Object, Org.Apache.Http.Conn.Schemes.ILayeredSocketFactory, Org.Apache.Http.Conn.Schemes.ISocketFactory {
	
	protected SSLSocketFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SSLSocketFactory (string algorithm, Java.Security.KeyStore keystore, string keystorePassword, Java.Security.KeyStore truststore, Java.Security.SecureRandom random, Org.Apache.Http.Conn.Schemes.IHostNameResolver nameResolver);
	public SSLSocketFactory (Java.Security.KeyStore truststore);
	public SSLSocketFactory (Java.Security.KeyStore keystore, string keystorePassword);
	public SSLSocketFactory (Java.Security.KeyStore keystore, string keystorePassword, Java.Security.KeyStore truststore);
	
	public virtual Java.Net.Socket ConnectSocket (Java.Net.Socket sock, string host, int port, Java.Net.InetAddress localAddress, int localPort, Org.Apache.Http.Params.IHttpParams params);
	public virtual Java.Net.Socket CreateSocket ();
	public virtual Java.Net.Socket CreateSocket (Java.Net.Socket socket, string host, int port, bool autoClose);
	public virtual bool IsSecure (Java.Net.Socket sock);
	
	public static IX509HostnameVerifier AllowAllHostnameVerifier {
		get;
		set;
	}
	public static IX509HostnameVerifier BrowserCompatibleHostnameVerifier {
		get;
		set;
	}
	public static SSLSocketFactory SocketFactory {
		get;
	}
	public static IX509HostnameVerifier StrictHostnameVerifier {
		get;
		set;
	}
	public virtual IX509HostnameVerifier HostnameVerifier {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Ssl = "SSL";
	public const string Sslv2 = "SSLv2";
	public const string Tls = "TLS";
}
```

<h3 id='Org.Apache.Http.Conn.Ssl.StrictHostnameVerifier'>New Type: Org.Apache.Http.Conn.Ssl.StrictHostnameVerifier</h3>

```
public class StrictHostnameVerifier : AbstractVerifier {
	
	protected StrictHostnameVerifier (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StrictHostnameVerifier ();
	
	public string ToString ();
	public void Verify (string host, string [] cns, string [] subjectAlts);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Conn.Util'>Namespace: Org.Apache.Http.Conn.Util</h2>

<h3 id='Org.Apache.Http.Conn.Util.InetAddressUtils'>New Type: Org.Apache.Http.Conn.Util.InetAddressUtils</h3>

```
public class InetAddressUtils : Java.Lang.Object {
	
	protected InetAddressUtils (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static bool IsIPv4Address (string input);
	public static bool IsIPv6Address (string input);
	public static bool IsIPv6HexCompressedAddress (string input);
	public static bool IsIPv6StdAddress (string input);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Cookie.Params'>Namespace: Org.Apache.Http.Cookie.Params</h2>

<h3 id='Org.Apache.Http.Cookie.Params.CookieSpecPNames'>New Type: Org.Apache.Http.Cookie.Params.CookieSpecPNames</h3>

```
public abstract class CookieSpecPNames {
	
	public const string DatePatterns = "http.protocol.cookie-datepatterns";
	public const string SingleCookieHeader = "http.protocol.single-cookie-header";
}
```

<h3 id='Org.Apache.Http.Cookie.Params.CookieSpecPNamesConsts'>New Type: Org.Apache.Http.Cookie.Params.CookieSpecPNamesConsts</h3>

```
[Obsolete]
public abstract class CookieSpecPNamesConsts : CookieSpecPNames {
}
```

<h3 id='Org.Apache.Http.Cookie.Params.CookieSpecParamBean'>New Type: Org.Apache.Http.Cookie.Params.CookieSpecParamBean</h3>

```
public class CookieSpecParamBean : Org.Apache.Http.Params.HttpAbstractParamBean {
	
	protected CookieSpecParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CookieSpecParamBean (Org.Apache.Http.Params.IHttpParams params);
	
	public virtual void SetDatePatterns (System.Collections.Generic.ICollection patterns);
	public virtual void SetSingleHeader (bool singleHeader);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Cookies'>Namespace: Org.Apache.Http.Cookies</h2>

<h3 id='Org.Apache.Http.Cookies.ClientCookie'>New Type: Org.Apache.Http.Cookies.ClientCookie</h3>

```
public abstract class ClientCookie {
	
	public const string CommentAttr = "comment";
	public const string CommenturlAttr = "commenturl";
	public const string DiscardAttr = "discard";
	public const string DomainAttr = "domain";
	public const string ExpiresAttr = "expires";
	public const string MaxAgeAttr = "max-age";
	public const string PathAttr = "path";
	public const string PortAttr = "port";
	public const string SecureAttr = "secure";
	public const string VersionAttr = "version";
}
```

<h3 id='Org.Apache.Http.Cookies.ClientCookieConsts'>New Type: Org.Apache.Http.Cookies.ClientCookieConsts</h3>

```
[Obsolete]
public abstract class ClientCookieConsts : ClientCookie {
}
```

<h3 id='Org.Apache.Http.Cookies.CookieOrigin'>New Type: Org.Apache.Http.Cookies.CookieOrigin</h3>

```
public sealed class CookieOrigin : Java.Lang.Object {
	
	public CookieOrigin (string host, int port, string path, bool secure);
	
	public string Host {
		get;
	}
	public bool IsSecure {
		get;
	}
	public string Path {
		get;
	}
	public int Port {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Cookies.CookieSpecRegistry'>New Type: Org.Apache.Http.Cookies.CookieSpecRegistry</h3>

```
public sealed class CookieSpecRegistry : Java.Lang.Object {
	
	public CookieSpecRegistry ();
	
	public ICookieSpec GetCookieSpec (string name);
	public ICookieSpec GetCookieSpec (string name, Org.Apache.Http.Params.IHttpParams params);
	public void Register (string name, ICookieSpecFactory factory);
	public void SetItems (System.Collections.Generic.IDictionary map);
	public void Unregister (string id);
	
	public System.Collections.Generic.IList SpecNames {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Cookies.IClientCookie'>New Type: Org.Apache.Http.Cookies.IClientCookie</h3>

```
public interface IClientCookie : ICookie, IDisposable, Android.Runtime.IJavaObject {
	
	bool ContainsAttribute (string name);
	string GetAttribute (string name);
}
```

<h3 id='Org.Apache.Http.Cookies.ICookie'>New Type: Org.Apache.Http.Cookies.ICookie</h3>

```
public interface ICookie : IDisposable, Android.Runtime.IJavaObject {
	
	int [] GetPorts ();
	bool IsExpired (Java.Util.Date date);
	
	string Comment {
		get;
	}
	string CommentURL {
		get;
	}
	string Domain {
		get;
	}
	Java.Util.Date ExpiryDate {
		get;
	}
	bool IsPersistent {
		get;
	}
	bool IsSecure {
		get;
	}
	string Name {
		get;
	}
	string Path {
		get;
	}
	string Value {
		get;
	}
	int Version {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Cookies.ICookieAttributeHandler'>New Type: Org.Apache.Http.Cookies.ICookieAttributeHandler</h3>

```
public interface ICookieAttributeHandler : IDisposable, Android.Runtime.IJavaObject {
	
	bool Match (ICookie cookie, CookieOrigin origin);
	void Parse (ISetCookie cookie, string value);
	void Validate (ICookie cookie, CookieOrigin origin);
}
```

<h3 id='Org.Apache.Http.Cookies.ICookieSpec'>New Type: Org.Apache.Http.Cookies.ICookieSpec</h3>

```
public interface ICookieSpec : IDisposable, Android.Runtime.IJavaObject {
	
	System.Collections.Generic.IList FormatCookies (System.Collections.Generic.IList cookies);
	bool Match (ICookie cookie, CookieOrigin origin);
	System.Collections.Generic.IList Parse (Org.Apache.Http.IHeader header, CookieOrigin origin);
	void Validate (ICookie cookie, CookieOrigin origin);
	
	int Version {
		get;
	}
	Org.Apache.Http.IHeader VersionHeader {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Cookies.ICookieSpecFactory'>New Type: Org.Apache.Http.Cookies.ICookieSpecFactory</h3>

```
public interface ICookieSpecFactory : IDisposable, Android.Runtime.IJavaObject {
	
	ICookieSpec NewInstance (Org.Apache.Http.Params.IHttpParams params);
}
```

<h3 id='Org.Apache.Http.Cookies.ISetCookie'>New Type: Org.Apache.Http.Cookies.ISetCookie</h3>

```
public interface ISetCookie : ICookie, IDisposable, Android.Runtime.IJavaObject {
	
	void SetComment (string comment);
	void SetDomain (string domain);
	void SetExpiryDate (Java.Util.Date expiryDate);
	void SetPath (string path);
	void SetSecure (bool secure);
	void SetValue (string value);
	void SetVersion (int version);
}
```

<h3 id='Org.Apache.Http.Cookies.ISetCookie2'>New Type: Org.Apache.Http.Cookies.ISetCookie2</h3>

```
public interface ISetCookie2 : ICookie, IDisposable, Android.Runtime.IJavaObject, ISetCookie {
	
	void SetCommentURL (string commentURL);
	void SetDiscard (bool discard);
	void SetPorts (int [] ports);
}
```

<h3 id='Org.Apache.Http.Cookies.MalformedCookieException'>New Type: Org.Apache.Http.Cookies.MalformedCookieException</h3>

```
public class MalformedCookieException : Org.Apache.Http.ProtocolException {
	
	protected MalformedCookieException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public MalformedCookieException ();
	public MalformedCookieException (string message);
	public MalformedCookieException (string message, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Cookies.SM'>New Type: Org.Apache.Http.Cookies.SM</h3>

```
public abstract class SM {
	
	public const string Cookie = "Cookie";
	public const string Cookie2 = "Cookie2";
	public const string SetCookie = "Set-Cookie";
	public const string SetCookie2 = "Set-Cookie2";
}
```

<h3 id='Org.Apache.Http.Cookies.SMConsts'>New Type: Org.Apache.Http.Cookies.SMConsts</h3>

```
[Obsolete]
public abstract class SMConsts : SM {
}
```

<h2 id='Org.Apache.Http.Entity'>Namespace: Org.Apache.Http.Entity</h2>

<h3 id='Org.Apache.Http.Entity.AbstractHttpEntity'>New Type: Org.Apache.Http.Entity.AbstractHttpEntity</h3>

```
public abstract class AbstractHttpEntity : Java.Lang.Object, Org.Apache.Http.IHttpEntity {
	
	protected AbstractHttpEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractHttpEntity ();
	
	public virtual void ConsumeContent ();
	public virtual void SetChunked (bool b);
	public virtual void SetContentEncoding (string ceString);
	public virtual void SetContentType (string ctString);
	public abstract void WriteTo (System.IO.Stream outstream);
	public System.Threading.Tasks.Task WriteToAsync (System.IO.Stream outstream);
	
	protected bool ChunkedField {
		get;
		set;
	}
	public abstract System.IO.Stream Content {
		get;
	}
	public virtual Org.Apache.Http.IHeader ContentEncoding {
		get;
		set;
	}
	protected Org.Apache.Http.IHeader ContentEncodingField {
		get;
		set;
	}
	public abstract long ContentLength {
		get;
	}
	public virtual Org.Apache.Http.IHeader ContentType {
		get;
		set;
	}
	protected Org.Apache.Http.IHeader ContentTypeField {
		get;
		set;
	}
	public virtual bool IsChunked {
		get;
	}
	public abstract bool IsRepeatable {
		get;
	}
	public abstract bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Entity.BasicHttpEntity'>New Type: Org.Apache.Http.Entity.BasicHttpEntity</h3>

```
public class BasicHttpEntity : AbstractHttpEntity {
	
	protected BasicHttpEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHttpEntity ();
	
	public override void WriteTo (System.IO.Stream outstream);
	
	public override System.IO.Stream Content {
		get;
	}
	public override long ContentLength {
		get;
	}
	public override bool IsRepeatable {
		get;
	}
	public override bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Entity.BufferedHttpEntity'>New Type: Org.Apache.Http.Entity.BufferedHttpEntity</h3>

```
public class BufferedHttpEntity : HttpEntityWrapper {
	
	protected BufferedHttpEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BufferedHttpEntity (Org.Apache.Http.IHttpEntity entity);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Entity.ByteArrayEntity'>New Type: Org.Apache.Http.Entity.ByteArrayEntity</h3>

```
public class ByteArrayEntity : AbstractHttpEntity, Java.Lang.ICloneable {
	
	protected ByteArrayEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ByteArrayEntity (byte [] b);
	
	public virtual Java.Lang.Object Clone ();
	public override void WriteTo (System.IO.Stream outstream);
	
	public override System.IO.Stream Content {
		get;
	}
	public override long ContentLength {
		get;
	}
	public override bool IsRepeatable {
		get;
	}
	public override bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Entity.ContentLengthStrategy'>New Type: Org.Apache.Http.Entity.ContentLengthStrategy</h3>

```
public abstract class ContentLengthStrategy {
	
	public const int Chunked = -2;
	public const int Identity = -1;
}
```

<h3 id='Org.Apache.Http.Entity.ContentLengthStrategyConsts'>New Type: Org.Apache.Http.Entity.ContentLengthStrategyConsts</h3>

```
[Obsolete]
public abstract class ContentLengthStrategyConsts : ContentLengthStrategy {
}
```

<h3 id='Org.Apache.Http.Entity.EntityTemplate'>New Type: Org.Apache.Http.Entity.EntityTemplate</h3>

```
public class EntityTemplate : AbstractHttpEntity {
	
	protected EntityTemplate (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public EntityTemplate (IContentProducer contentproducer);
	
	public override void WriteTo (System.IO.Stream outstream);
	
	public override System.IO.Stream Content {
		get;
	}
	public override long ContentLength {
		get;
	}
	public override bool IsRepeatable {
		get;
	}
	public override bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Entity.FileEntity'>New Type: Org.Apache.Http.Entity.FileEntity</h3>

```
public class FileEntity : AbstractHttpEntity, Java.Lang.ICloneable {
	
	protected FileEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FileEntity (Java.IO.File file, string contentType);
	
	public virtual Java.Lang.Object Clone ();
	public override void WriteTo (System.IO.Stream outstream);
	
	public override System.IO.Stream Content {
		get;
	}
	public override long ContentLength {
		get;
	}
	protected Java.IO.File File {
		get;
		set;
	}
	public override bool IsRepeatable {
		get;
	}
	public override bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Entity.HttpEntityWrapper'>New Type: Org.Apache.Http.Entity.HttpEntityWrapper</h3>

```
public class HttpEntityWrapper : Java.Lang.Object, Org.Apache.Http.IHttpEntity {
	
	protected HttpEntityWrapper (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpEntityWrapper (Org.Apache.Http.IHttpEntity wrapped);
	
	public virtual void ConsumeContent ();
	public virtual void WriteTo (System.IO.Stream outstream);
	
	public virtual System.IO.Stream Content {
		get;
	}
	public virtual Org.Apache.Http.IHeader ContentEncoding {
		get;
	}
	public virtual long ContentLength {
		get;
	}
	public virtual Org.Apache.Http.IHeader ContentType {
		get;
	}
	public virtual bool IsChunked {
		get;
	}
	public virtual bool IsRepeatable {
		get;
	}
	public virtual bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	protected Org.Apache.Http.IHttpEntity WrappedEntity {
		get;
		set;
	}
}
```

<h3 id='Org.Apache.Http.Entity.IContentLengthStrategy'>New Type: Org.Apache.Http.Entity.IContentLengthStrategy</h3>

```
public interface IContentLengthStrategy : IDisposable, Android.Runtime.IJavaObject {
	
	long DetermineLength (Org.Apache.Http.IHttpMessage message);
}
```

<h3 id='Org.Apache.Http.Entity.IContentProducer'>New Type: Org.Apache.Http.Entity.IContentProducer</h3>

```
public interface IContentProducer : IDisposable, Android.Runtime.IJavaObject {
	
	void WriteTo (System.IO.Stream outstream);
}
```

<h3 id='Org.Apache.Http.Entity.InputStreamEntity'>New Type: Org.Apache.Http.Entity.InputStreamEntity</h3>

```
public class InputStreamEntity : AbstractHttpEntity {
	
	protected InputStreamEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public InputStreamEntity (System.IO.Stream instream, long length);
	
	public override void WriteTo (System.IO.Stream outstream);
	
	public override System.IO.Stream Content {
		get;
	}
	public override long ContentLength {
		get;
	}
	public override bool IsRepeatable {
		get;
	}
	public override bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Entity.SerializableEntity'>New Type: Org.Apache.Http.Entity.SerializableEntity</h3>

```
public class SerializableEntity : AbstractHttpEntity {
	
	protected SerializableEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SerializableEntity (Java.IO.ISerializable ser, bool bufferize);
	
	public override void WriteTo (System.IO.Stream outstream);
	
	public override System.IO.Stream Content {
		get;
	}
	public override long ContentLength {
		get;
	}
	public override bool IsRepeatable {
		get;
	}
	public override bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Entity.StringEntity'>New Type: Org.Apache.Http.Entity.StringEntity</h3>

```
public class StringEntity : AbstractHttpEntity, Java.Lang.ICloneable {
	
	protected StringEntity (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public StringEntity (string s);
	public StringEntity (string s, string charset);
	
	public virtual Java.Lang.Object Clone ();
	public override void WriteTo (System.IO.Stream outstream);
	
	public override System.IO.Stream Content {
		get;
	}
	public override long ContentLength {
		get;
	}
	public override bool IsRepeatable {
		get;
	}
	public override bool IsStreaming {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.IO'>Namespace: Org.Apache.Http.IO</h2>

<h3 id='Org.Apache.Http.IO.IHttpMessageParser'>New Type: Org.Apache.Http.IO.IHttpMessageParser</h3>

```
public interface IHttpMessageParser : IDisposable, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.IHttpMessage Parse ();
}
```

<h3 id='Org.Apache.Http.IO.IHttpMessageParserExtensions'>New Type: Org.Apache.Http.IO.IHttpMessageParserExtensions</h3>

```
public static class IHttpMessageParserExtensions {
	
	public static System.Threading.Tasks.Task ParseAsync (IHttpMessageParser self);
}
```

<h3 id='Org.Apache.Http.IO.IHttpMessageWriter'>New Type: Org.Apache.Http.IO.IHttpMessageWriter</h3>

```
public interface IHttpMessageWriter : IDisposable, Android.Runtime.IJavaObject {
	
	void Write (Org.Apache.Http.IHttpMessage message);
}
```

<h3 id='Org.Apache.Http.IO.IHttpMessageWriterExtensions'>New Type: Org.Apache.Http.IO.IHttpMessageWriterExtensions</h3>

```
public static class IHttpMessageWriterExtensions {
	
	public static System.Threading.Tasks.Task WriteAsync (IHttpMessageWriter self, Org.Apache.Http.IHttpMessage message);
}
```

<h3 id='Org.Apache.Http.IO.IHttpTransportMetrics'>New Type: Org.Apache.Http.IO.IHttpTransportMetrics</h3>

```
public interface IHttpTransportMetrics : IDisposable, Android.Runtime.IJavaObject {
	
	void Reset ();
	
	long BytesTransferred {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IO.ISessionInputBuffer'>New Type: Org.Apache.Http.IO.ISessionInputBuffer</h3>

```
public interface ISessionInputBuffer : IDisposable, Android.Runtime.IJavaObject {
	
	bool IsDataAvailable (int timeout);
	int Read ();
	int Read (byte [] b);
	int Read (byte [] b, int off, int len);
	string ReadLine ();
	int ReadLine (Org.Apache.Http.Util.CharArrayBuffer buffer);
	
	IHttpTransportMetrics Metrics {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IO.ISessionInputBufferExtensions'>New Type: Org.Apache.Http.IO.ISessionInputBufferExtensions</h3>

```
public static class ISessionInputBufferExtensions {
	
	public static System.Threading.Tasks.Task ReadAsync (ISessionInputBuffer self);
	public static System.Threading.Tasks.Task ReadAsync (ISessionInputBuffer self, byte [] b);
	public static System.Threading.Tasks.Task ReadAsync (ISessionInputBuffer self, byte [] b, int off, int len);
	public static System.Threading.Tasks.Task ReadLineAsync (ISessionInputBuffer self);
	public static System.Threading.Tasks.Task ReadLineAsync (ISessionInputBuffer self, Org.Apache.Http.Util.CharArrayBuffer buffer);
}
```

<h3 id='Org.Apache.Http.IO.ISessionOutputBuffer'>New Type: Org.Apache.Http.IO.ISessionOutputBuffer</h3>

```
public interface ISessionOutputBuffer : IDisposable, Android.Runtime.IJavaObject {
	
	void Flush ();
	void Write (byte [] b);
	void Write (byte [] b, int off, int len);
	void Write (int b);
	void WriteLine (Org.Apache.Http.Util.CharArrayBuffer buffer);
	void WriteLine (string s);
	
	IHttpTransportMetrics Metrics {
		get;
	}
}
```

<h3 id='Org.Apache.Http.IO.ISessionOutputBufferExtensions'>New Type: Org.Apache.Http.IO.ISessionOutputBufferExtensions</h3>

```
public static class ISessionOutputBufferExtensions {
	
	public static System.Threading.Tasks.Task WriteAsync (ISessionOutputBuffer self, byte [] b);
	public static System.Threading.Tasks.Task WriteAsync (ISessionOutputBuffer self, byte [] b, int off, int len);
	public static System.Threading.Tasks.Task WriteAsync (ISessionOutputBuffer self, int b);
	public static System.Threading.Tasks.Task WriteLineAsync (ISessionOutputBuffer self, Org.Apache.Http.Util.CharArrayBuffer buffer);
	public static System.Threading.Tasks.Task WriteLineAsync (ISessionOutputBuffer self, string s);
}
```

<h2 id='Org.Apache.Http.Message'>Namespace: Org.Apache.Http.Message</h2>

<h3 id='Org.Apache.Http.Message.AbstractHttpMessage'>New Type: Org.Apache.Http.Message.AbstractHttpMessage</h3>

```
public abstract class AbstractHttpMessage : Java.Lang.Object, Org.Apache.Http.IHttpMessage {
	
	protected AbstractHttpMessage (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractHttpMessage ();
	protected AbstractHttpMessage (Org.Apache.Http.Params.IHttpParams params);
	
	public virtual void AddHeader (Org.Apache.Http.IHeader header);
	public virtual void AddHeader (string name, string value);
	public virtual bool ContainsHeader (string name);
	public virtual Org.Apache.Http.IHeader[] GetAllHeaders ();
	public virtual Org.Apache.Http.IHeader GetFirstHeader (string name);
	public virtual Org.Apache.Http.IHeader[] GetHeaders (string name);
	public virtual Org.Apache.Http.IHeader GetLastHeader (string name);
	public virtual Org.Apache.Http.IHeaderIterator HeaderIterator ();
	public virtual Org.Apache.Http.IHeaderIterator HeaderIterator (string name);
	public virtual void RemoveHeader (Org.Apache.Http.IHeader header);
	public virtual void RemoveHeaders (string name);
	public virtual void SetHeader (Org.Apache.Http.IHeader header);
	public virtual void SetHeader (string name, string value);
	public virtual void SetHeaders (Org.Apache.Http.IHeader[] headers);
	
	protected HeaderGroup Headergroup {
		get;
		set;
	}
	public virtual Org.Apache.Http.Params.IHttpParams Params {
		get;
		set;
	}
	public abstract Org.Apache.Http.ProtocolVersion ProtocolVersion {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicHeader'>New Type: Org.Apache.Http.Message.BasicHeader</h3>

```
public class BasicHeader : Java.Lang.Object, Java.Lang.ICloneable, Org.Apache.Http.IHeader {
	
	protected BasicHeader (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHeader (string name, string value);
	
	public virtual Java.Lang.Object Clone ();
	public virtual Org.Apache.Http.IHeaderElement[] GetElements ();
	
	public virtual string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string Value {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicHeaderElement'>New Type: Org.Apache.Http.Message.BasicHeaderElement</h3>

```
public class BasicHeaderElement : Java.Lang.Object, Java.Lang.ICloneable, Org.Apache.Http.IHeaderElement {
	
	protected BasicHeaderElement (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHeaderElement (string name, string value);
	public BasicHeaderElement (string name, string value, Org.Apache.Http.INameValuePair[] parameters);
	
	public virtual Java.Lang.Object Clone ();
	public virtual Org.Apache.Http.INameValuePair GetParameter (int index);
	public virtual Org.Apache.Http.INameValuePair GetParameterByName (string name);
	public virtual Org.Apache.Http.INameValuePair[] GetParameters ();
	
	public virtual string Name {
		get;
	}
	public virtual int ParameterCount {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string Value {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicHeaderElementIterator'>New Type: Org.Apache.Http.Message.BasicHeaderElementIterator</h3>

```
public class BasicHeaderElementIterator : Java.Lang.Object, Org.Apache.Http.IHeaderElementIterator, Java.Util.IIterator {
	
	protected BasicHeaderElementIterator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHeaderElementIterator (Org.Apache.Http.IHeaderIterator headerIterator);
	public BasicHeaderElementIterator (Org.Apache.Http.IHeaderIterator headerIterator, IHeaderValueParser parser);
	
	public Java.Lang.Object Next ();
	public virtual Org.Apache.Http.IHeaderElement NextElement ();
	public virtual void Remove ();
	
	public virtual bool HasNext {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicHeaderIterator'>New Type: Org.Apache.Http.Message.BasicHeaderIterator</h3>

```
public class BasicHeaderIterator : Java.Lang.Object, Org.Apache.Http.IHeaderIterator, Java.Util.IIterator {
	
	protected BasicHeaderIterator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHeaderIterator (Org.Apache.Http.IHeader[] headers, string name);
	
	protected virtual bool FilterHeader (int index);
	protected virtual int FindNext (int from);
	public Java.Lang.Object Next ();
	public virtual Org.Apache.Http.IHeader NextHeader ();
	public virtual void Remove ();
	
	protected System.Collections.Generic.IList AllHeaders {
		get;
		set;
	}
	protected int CurrentIndex {
		get;
		set;
	}
	public virtual bool HasNext {
		get;
	}
	protected string HeaderName {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicHeaderValueFormatter'>New Type: Org.Apache.Http.Message.BasicHeaderValueFormatter</h3>

```
public class BasicHeaderValueFormatter : Java.Lang.Object, IHeaderValueFormatter {
	
	protected BasicHeaderValueFormatter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHeaderValueFormatter ();
	
	public static string FormatElements (Org.Apache.Http.IHeaderElement[] elems, bool quote, IHeaderValueFormatter formatter);
	public static string FormatHeaderElement (Org.Apache.Http.IHeaderElement elem, bool quote, IHeaderValueFormatter formatter);
	public static string FormatNameValuePair (Org.Apache.Http.INameValuePair nvp, bool quote, IHeaderValueFormatter formatter);
	public static string FormatParameters (Org.Apache.Http.INameValuePair[] nvps, bool quote, IHeaderValueFormatter formatter);
	protected virtual void DoFormatValue (Org.Apache.Http.Util.CharArrayBuffer buffer, string value, bool quote);
	protected virtual int EstimateElementsLen (Org.Apache.Http.IHeaderElement[] elems);
	protected virtual int EstimateHeaderElementLen (Org.Apache.Http.IHeaderElement elem);
	protected virtual int EstimateNameValuePairLen (Org.Apache.Http.INameValuePair nvp);
	protected virtual int EstimateParametersLen (Org.Apache.Http.INameValuePair[] nvps);
	public virtual Org.Apache.Http.Util.CharArrayBuffer FormatElements (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IHeaderElement[] elems, bool quote);
	public virtual Org.Apache.Http.Util.CharArrayBuffer FormatHeaderElement (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IHeaderElement elem, bool quote);
	public virtual Org.Apache.Http.Util.CharArrayBuffer FormatNameValuePair (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.INameValuePair nvp, bool quote);
	public virtual Org.Apache.Http.Util.CharArrayBuffer FormatParameters (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.INameValuePair[] nvps, bool quote);
	protected virtual bool IsSeparator (char ch);
	protected virtual bool IsUnsafe (char ch);
	
	public static BasicHeaderValueFormatter Default {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Separators = " ;,:@()<>\"/[]?={}	";
	public const string UnsafeChars = ""\";
}
```

<h3 id='Org.Apache.Http.Message.BasicHeaderValueParser'>New Type: Org.Apache.Http.Message.BasicHeaderValueParser</h3>

```
public class BasicHeaderValueParser : Java.Lang.Object, IHeaderValueParser {
	
	protected BasicHeaderValueParser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHeaderValueParser ();
	
	public static Org.Apache.Http.IHeaderElement[] ParseElements (string value, IHeaderValueParser parser);
	public static Org.Apache.Http.IHeaderElement ParseHeaderElement (string value, IHeaderValueParser parser);
	public static Org.Apache.Http.INameValuePair ParseNameValuePair (string value, IHeaderValueParser parser);
	public static Org.Apache.Http.INameValuePair[] ParseParameters (string value, IHeaderValueParser parser);
	protected virtual Org.Apache.Http.IHeaderElement CreateHeaderElement (string name, string value, Org.Apache.Http.INameValuePair[] params);
	protected virtual Org.Apache.Http.INameValuePair CreateNameValuePair (string name, string value);
	public virtual Org.Apache.Http.IHeaderElement[] ParseElements (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	public virtual Org.Apache.Http.IHeaderElement ParseHeaderElement (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	public virtual Org.Apache.Http.INameValuePair ParseNameValuePair (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	public virtual Org.Apache.Http.INameValuePair ParseNameValuePair (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor, char [] delimiters);
	public virtual Org.Apache.Http.INameValuePair[] ParseParameters (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	
	public static BasicHeaderValueParser Default {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicHttpEntityEnclosingRequest'>New Type: Org.Apache.Http.Message.BasicHttpEntityEnclosingRequest</h3>

```
public class BasicHttpEntityEnclosingRequest : BasicHttpRequest, Org.Apache.Http.IHttpEntityEnclosingRequest {
	
	protected BasicHttpEntityEnclosingRequest (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHttpEntityEnclosingRequest (string method, string uri);
	public BasicHttpEntityEnclosingRequest (string method, string uri, Org.Apache.Http.ProtocolVersion ver);
	public BasicHttpEntityEnclosingRequest (Org.Apache.Http.IRequestLine requestline);
	
	public virtual bool ExpectContinue ();
	
	public virtual Org.Apache.Http.IHttpEntity Entity {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicHttpRequest'>New Type: Org.Apache.Http.Message.BasicHttpRequest</h3>

```
public class BasicHttpRequest : AbstractHttpMessage, Org.Apache.Http.IHttpRequest {
	
	protected BasicHttpRequest (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHttpRequest (string method, string uri);
	public BasicHttpRequest (string method, string uri, Org.Apache.Http.ProtocolVersion ver);
	public BasicHttpRequest (Org.Apache.Http.IRequestLine requestline);
	
	public override Org.Apache.Http.ProtocolVersion ProtocolVersion {
		get;
	}
	public virtual Org.Apache.Http.IRequestLine RequestLine {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicHttpResponse'>New Type: Org.Apache.Http.Message.BasicHttpResponse</h3>

```
public class BasicHttpResponse : AbstractHttpMessage, Org.Apache.Http.IHttpResponse {
	
	protected BasicHttpResponse (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHttpResponse (Org.Apache.Http.ProtocolVersion ver, int code, string reason);
	public BasicHttpResponse (Org.Apache.Http.IStatusLine statusline);
	public BasicHttpResponse (Org.Apache.Http.IStatusLine statusline, Org.Apache.Http.IReasonPhraseCatalog catalog, Java.Util.Locale locale);
	
	protected virtual string GetReason (int code);
	public virtual void SetReasonPhrase (string reason);
	public virtual void SetStatusCode (int code);
	public virtual void SetStatusLine (Org.Apache.Http.ProtocolVersion ver, int code);
	public virtual void SetStatusLine (Org.Apache.Http.ProtocolVersion ver, int code, string reason);
	
	public virtual Org.Apache.Http.IHttpEntity Entity {
		get;
		set;
	}
	public virtual Java.Util.Locale Locale {
		get;
		set;
	}
	public override Org.Apache.Http.ProtocolVersion ProtocolVersion {
		get;
	}
	public virtual Org.Apache.Http.IStatusLine StatusLine {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicLineFormatter'>New Type: Org.Apache.Http.Message.BasicLineFormatter</h3>

```
public class BasicLineFormatter : Java.Lang.Object, ILineFormatter {
	
	protected BasicLineFormatter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicLineFormatter ();
	
	public static string FormatHeader (Org.Apache.Http.IHeader header, ILineFormatter formatter);
	public static string FormatProtocolVersion (Org.Apache.Http.ProtocolVersion version, ILineFormatter formatter);
	public static string FormatRequestLine (Org.Apache.Http.IRequestLine reqline, ILineFormatter formatter);
	public static string FormatStatusLine (Org.Apache.Http.IStatusLine statline, ILineFormatter formatter);
	public virtual Org.Apache.Http.Util.CharArrayBuffer AppendProtocolVersion (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.ProtocolVersion version);
	protected virtual void DoFormatHeader (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IHeader header);
	protected virtual void DoFormatRequestLine (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IRequestLine reqline);
	protected virtual void DoFormatStatusLine (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IStatusLine statline);
	protected virtual int EstimateProtocolVersionLen (Org.Apache.Http.ProtocolVersion version);
	public virtual Org.Apache.Http.Util.CharArrayBuffer FormatHeader (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IHeader header);
	public virtual Org.Apache.Http.Util.CharArrayBuffer FormatRequestLine (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IRequestLine reqline);
	public virtual Org.Apache.Http.Util.CharArrayBuffer FormatStatusLine (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IStatusLine statline);
	protected virtual Org.Apache.Http.Util.CharArrayBuffer InitBuffer (Org.Apache.Http.Util.CharArrayBuffer buffer);
	
	public static BasicLineFormatter Default {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicLineParser'>New Type: Org.Apache.Http.Message.BasicLineParser</h3>

```
public class BasicLineParser : Java.Lang.Object, ILineParser {
	
	protected BasicLineParser (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicLineParser ();
	public BasicLineParser (Org.Apache.Http.ProtocolVersion proto);
	
	public static Org.Apache.Http.IHeader ParseHeader (string value, ILineParser parser);
	public static Org.Apache.Http.ProtocolVersion ParseProtocolVersion (string value, ILineParser parser);
	public static Org.Apache.Http.IRequestLine ParseRequestLine (string value, ILineParser parser);
	public static Org.Apache.Http.IStatusLine ParseStatusLine (string value, ILineParser parser);
	protected virtual Org.Apache.Http.ProtocolVersion CreateProtocolVersion (int major, int minor);
	protected virtual Org.Apache.Http.IRequestLine CreateRequestLine (string method, string uri, Org.Apache.Http.ProtocolVersion ver);
	protected virtual Org.Apache.Http.IStatusLine CreateStatusLine (Org.Apache.Http.ProtocolVersion ver, int status, string reason);
	public virtual bool HasProtocolVersion (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	public virtual Org.Apache.Http.IHeader ParseHeader (Org.Apache.Http.Util.CharArrayBuffer buffer);
	public virtual Org.Apache.Http.ProtocolVersion ParseProtocolVersion (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	public virtual Org.Apache.Http.IRequestLine ParseRequestLine (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	public virtual Org.Apache.Http.IStatusLine ParseStatusLine (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	protected virtual void SkipWhitespace (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	
	public static BasicLineParser Default {
		get;
		set;
	}
	protected Org.Apache.Http.ProtocolVersion Protocol {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicListHeaderIterator'>New Type: Org.Apache.Http.Message.BasicListHeaderIterator</h3>

```
public class BasicListHeaderIterator : Java.Lang.Object, Org.Apache.Http.IHeaderIterator, Java.Util.IIterator {
	
	protected BasicListHeaderIterator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicListHeaderIterator (System.Collections.IList headers, string name);
	
	protected virtual bool FilterHeader (int index);
	protected virtual int FindNext (int from);
	public Java.Lang.Object Next ();
	public virtual Org.Apache.Http.IHeader NextHeader ();
	public virtual void Remove ();
	
	protected System.Collections.IList AllHeaders {
		get;
		set;
	}
	protected int CurrentIndex {
		get;
		set;
	}
	public virtual bool HasNext {
		get;
	}
	protected string HeaderName {
		get;
		set;
	}
	protected int LastIndex {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicNameValuePair'>New Type: Org.Apache.Http.Message.BasicNameValuePair</h3>

```
public class BasicNameValuePair : Java.Lang.Object, Java.Lang.ICloneable, Org.Apache.Http.INameValuePair {
	
	protected BasicNameValuePair (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicNameValuePair (string name, string value);
	
	public virtual Java.Lang.Object Clone ();
	
	public virtual string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string Value {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicRequestLine'>New Type: Org.Apache.Http.Message.BasicRequestLine</h3>

```
public class BasicRequestLine : Java.Lang.Object, Java.Lang.ICloneable, Org.Apache.Http.IRequestLine {
	
	protected BasicRequestLine (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicRequestLine (string method, string uri, Org.Apache.Http.ProtocolVersion version);
	
	public virtual Java.Lang.Object Clone ();
	
	public virtual string Method {
		get;
	}
	public virtual Org.Apache.Http.ProtocolVersion ProtocolVersion {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string Uri {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicStatusLine'>New Type: Org.Apache.Http.Message.BasicStatusLine</h3>

```
public class BasicStatusLine : Java.Lang.Object, Java.Lang.ICloneable, Org.Apache.Http.IStatusLine {
	
	protected BasicStatusLine (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicStatusLine (Org.Apache.Http.ProtocolVersion version, int statusCode, string reasonPhrase);
	
	public virtual Java.Lang.Object Clone ();
	
	public virtual Org.Apache.Http.ProtocolVersion ProtocolVersion {
		get;
	}
	public virtual string ReasonPhrase {
		get;
	}
	public virtual int StatusCode {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.BasicTokenIterator'>New Type: Org.Apache.Http.Message.BasicTokenIterator</h3>

```
public class BasicTokenIterator : Java.Lang.Object, Java.Util.IIterator, Org.Apache.Http.ITokenIterator {
	
	protected BasicTokenIterator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicTokenIterator (Org.Apache.Http.IHeaderIterator headerIterator);
	
	protected virtual string CreateToken (string value, int start, int end);
	protected virtual int FindNext (int from);
	protected virtual int FindTokenEnd (int from);
	protected virtual int FindTokenSeparator (int from);
	protected virtual int FindTokenStart (int from);
	protected virtual bool IsHttpSeparator (char ch);
	protected virtual bool IsTokenChar (char ch);
	protected virtual bool IsTokenSeparator (char ch);
	protected virtual bool IsWhitespace (char ch);
	public Java.Lang.Object Next ();
	public virtual string NextToken ();
	public void Remove ();
	
	protected string CurrentHeader {
		get;
		set;
	}
	protected string CurrentToken {
		get;
		set;
	}
	public virtual bool HasNext {
		get;
	}
	protected Org.Apache.Http.IHeaderIterator HeaderIt {
		get;
		set;
	}
	protected int SearchPos {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string HttpSeparators = " ,;=()<>@:\"/[]?{}	";
}
```

<h3 id='Org.Apache.Http.Message.BufferedHeader'>New Type: Org.Apache.Http.Message.BufferedHeader</h3>

```
public class BufferedHeader : Java.Lang.Object, Java.Lang.ICloneable, Org.Apache.Http.IFormattedHeader, Org.Apache.Http.IHeader {
	
	protected BufferedHeader (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BufferedHeader (Org.Apache.Http.Util.CharArrayBuffer buffer);
	
	public virtual Java.Lang.Object Clone ();
	public virtual Org.Apache.Http.IHeaderElement[] GetElements ();
	
	public virtual Org.Apache.Http.Util.CharArrayBuffer Buffer {
		get;
	}
	public virtual string Name {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string Value {
		get;
	}
	public virtual int ValuePos {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.HeaderGroup'>New Type: Org.Apache.Http.Message.HeaderGroup</h3>

```
public class HeaderGroup : Java.Lang.Object, Java.Lang.ICloneable {
	
	protected HeaderGroup (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HeaderGroup ();
	
	public virtual void AddHeader (Org.Apache.Http.IHeader header);
	public virtual void Clear ();
	public virtual Java.Lang.Object Clone ();
	public virtual bool ContainsHeader (string name);
	public virtual HeaderGroup Copy ();
	public virtual Org.Apache.Http.IHeader[] GetAllHeaders ();
	public virtual Org.Apache.Http.IHeader GetCondensedHeader (string name);
	public virtual Org.Apache.Http.IHeader GetFirstHeader (string name);
	public virtual Org.Apache.Http.IHeader[] GetHeaders (string name);
	public virtual Org.Apache.Http.IHeader GetLastHeader (string name);
	public virtual Org.Apache.Http.IHeaderIterator Iterator ();
	public virtual Org.Apache.Http.IHeaderIterator Iterator (string name);
	public virtual void RemoveHeader (Org.Apache.Http.IHeader header);
	public virtual void SetHeaders (Org.Apache.Http.IHeader[] headers);
	public virtual void UpdateHeader (Org.Apache.Http.IHeader header);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Message.IHeaderValueFormatter'>New Type: Org.Apache.Http.Message.IHeaderValueFormatter</h3>

```
public interface IHeaderValueFormatter : IDisposable, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.Util.CharArrayBuffer FormatElements (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IHeaderElement[] elems, bool quote);
	Org.Apache.Http.Util.CharArrayBuffer FormatHeaderElement (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IHeaderElement elem, bool quote);
	Org.Apache.Http.Util.CharArrayBuffer FormatNameValuePair (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.INameValuePair nvp, bool quote);
	Org.Apache.Http.Util.CharArrayBuffer FormatParameters (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.INameValuePair[] nvps, bool quote);
}
```

<h3 id='Org.Apache.Http.Message.IHeaderValueParser'>New Type: Org.Apache.Http.Message.IHeaderValueParser</h3>

```
public interface IHeaderValueParser : IDisposable, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.IHeaderElement[] ParseElements (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	Org.Apache.Http.IHeaderElement ParseHeaderElement (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	Org.Apache.Http.INameValuePair ParseNameValuePair (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	Org.Apache.Http.INameValuePair[] ParseParameters (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
}
```

<h3 id='Org.Apache.Http.Message.ILineFormatter'>New Type: Org.Apache.Http.Message.ILineFormatter</h3>

```
public interface ILineFormatter : IDisposable, Android.Runtime.IJavaObject {
	
	Org.Apache.Http.Util.CharArrayBuffer AppendProtocolVersion (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.ProtocolVersion version);
	Org.Apache.Http.Util.CharArrayBuffer FormatHeader (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IHeader header);
	Org.Apache.Http.Util.CharArrayBuffer FormatRequestLine (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IRequestLine reqline);
	Org.Apache.Http.Util.CharArrayBuffer FormatStatusLine (Org.Apache.Http.Util.CharArrayBuffer buffer, Org.Apache.Http.IStatusLine statline);
}
```

<h3 id='Org.Apache.Http.Message.ILineParser'>New Type: Org.Apache.Http.Message.ILineParser</h3>

```
public interface ILineParser : IDisposable, Android.Runtime.IJavaObject {
	
	bool HasProtocolVersion (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	Org.Apache.Http.IHeader ParseHeader (Org.Apache.Http.Util.CharArrayBuffer buffer);
	Org.Apache.Http.ProtocolVersion ParseProtocolVersion (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	Org.Apache.Http.IRequestLine ParseRequestLine (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
	Org.Apache.Http.IStatusLine ParseStatusLine (Org.Apache.Http.Util.CharArrayBuffer buffer, ParserCursor cursor);
}
```

<h3 id='Org.Apache.Http.Message.ParserCursor'>New Type: Org.Apache.Http.Message.ParserCursor</h3>

```
public class ParserCursor : Java.Lang.Object {
	
	protected ParserCursor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ParserCursor (int lowerBound, int upperBound);
	
	public virtual bool AtEnd ();
	public virtual void UpdatePos (int pos);
	
	public virtual int LowerBound {
		get;
	}
	public virtual int Pos {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual int UpperBound {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Params'>Namespace: Org.Apache.Http.Params</h2>

<h3 id='Org.Apache.Http.Params.AbstractHttpParams'>New Type: Org.Apache.Http.Params.AbstractHttpParams</h3>

```
public abstract class AbstractHttpParams : Java.Lang.Object, IHttpParams {
	
	protected AbstractHttpParams (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected AbstractHttpParams ();
	
	public abstract IHttpParams Copy ();
	public virtual bool GetBooleanParameter (string name, bool defaultValue);
	public virtual double GetDoubleParameter (string name, double defaultValue);
	public virtual int GetIntParameter (string name, int defaultValue);
	public virtual long GetLongParameter (string name, long defaultValue);
	public abstract Java.Lang.Object GetParameter (string name);
	public virtual bool IsParameterFalse (string name);
	public virtual bool IsParameterTrue (string name);
	public abstract bool RemoveParameter (string name);
	public virtual IHttpParams SetBooleanParameter (string name, bool value);
	public virtual IHttpParams SetDoubleParameter (string name, double value);
	public virtual IHttpParams SetIntParameter (string name, int value);
	public virtual IHttpParams SetLongParameter (string name, long value);
	public abstract IHttpParams SetParameter (string name, Java.Lang.Object value);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Params.BasicHttpParams'>New Type: Org.Apache.Http.Params.BasicHttpParams</h3>

```
public sealed class BasicHttpParams : AbstractHttpParams, Java.Lang.ICloneable, Java.IO.ISerializable {
	
	public BasicHttpParams ();
	
	public void Clear ();
	public Java.Lang.Object Clone ();
	public override IHttpParams Copy ();
	protected void CopyParams (IHttpParams target);
	public override Java.Lang.Object GetParameter (string name);
	public bool IsParameterSet (string name);
	public bool IsParameterSetLocally (string name);
	public override bool RemoveParameter (string name);
	public override IHttpParams SetParameter (string name, Java.Lang.Object value);
	public void SetParameters (string [] names, Java.Lang.Object value);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Params.CoreConnectionPNames'>New Type: Org.Apache.Http.Params.CoreConnectionPNames</h3>

```
public abstract class CoreConnectionPNames {
	
	public const string ConnectionTimeout = "http.connection.timeout";
	public const string MaxHeaderCount = "http.connection.max-header-count";
	public const string MaxLineLength = "http.connection.max-line-length";
	public const string SoLinger = "http.socket.linger";
	public const string SoTimeout = "http.socket.timeout";
	public const string SocketBufferSize = "http.socket.buffer-size";
	public const string StaleConnectionCheck = "http.connection.stalecheck";
	public const string TcpNodelay = "http.tcp.nodelay";
}
```

<h3 id='Org.Apache.Http.Params.CoreConnectionPNamesConsts'>New Type: Org.Apache.Http.Params.CoreConnectionPNamesConsts</h3>

```
[Obsolete]
public abstract class CoreConnectionPNamesConsts : CoreConnectionPNames {
}
```

<h3 id='Org.Apache.Http.Params.CoreProtocolPNames'>New Type: Org.Apache.Http.Params.CoreProtocolPNames</h3>

```
public abstract class CoreProtocolPNames {
	
	public const string HttpContentCharset = "http.protocol.content-charset";
	public const string HttpElementCharset = "http.protocol.element-charset";
	public const string OriginServer = "http.origin-server";
	public const string ProtocolVersion = "http.protocol.version";
	public const string StrictTransferEncoding = "http.protocol.strict-transfer-encoding";
	public const string UseExpectContinue = "http.protocol.expect-continue";
	public const string UserAgent = "http.useragent";
	public const string WaitForContinue = "http.protocol.wait-for-continue";
}
```

<h3 id='Org.Apache.Http.Params.CoreProtocolPNamesConsts'>New Type: Org.Apache.Http.Params.CoreProtocolPNamesConsts</h3>

```
[Obsolete]
public abstract class CoreProtocolPNamesConsts : CoreProtocolPNames {
}
```

<h3 id='Org.Apache.Http.Params.DefaultedHttpParams'>New Type: Org.Apache.Http.Params.DefaultedHttpParams</h3>

```
public sealed class DefaultedHttpParams : AbstractHttpParams {
	
	public DefaultedHttpParams (IHttpParams local, IHttpParams defaults);
	
	public override IHttpParams Copy ();
	public override Java.Lang.Object GetParameter (string name);
	public override bool RemoveParameter (string name);
	public override IHttpParams SetParameter (string name, Java.Lang.Object value);
	
	public IHttpParams Defaults {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Params.HttpAbstractParamBean'>New Type: Org.Apache.Http.Params.HttpAbstractParamBean</h3>

```
public abstract class HttpAbstractParamBean : Java.Lang.Object {
	
	protected HttpAbstractParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpAbstractParamBean (IHttpParams params);
	
	protected IHttpParams Params {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Params.HttpConnectionParamBean'>New Type: Org.Apache.Http.Params.HttpConnectionParamBean</h3>

```
public class HttpConnectionParamBean : HttpAbstractParamBean {
	
	protected HttpConnectionParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpConnectionParamBean (IHttpParams params);
	
	public virtual void SetConnectionTimeout (int connectionTimeout);
	public virtual void SetLinger (int linger);
	public virtual void SetSocketBufferSize (int socketBufferSize);
	public virtual void SetSoTimeout (int soTimeout);
	public virtual void SetStaleCheckingEnabled (bool staleCheckingEnabled);
	public virtual void SetTcpNoDelay (bool tcpNoDelay);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Params.HttpConnectionParams'>New Type: Org.Apache.Http.Params.HttpConnectionParams</h3>

```
public sealed class HttpConnectionParams : Java.Lang.Object {
	
	public static int GetConnectionTimeout (IHttpParams params);
	public static int GetLinger (IHttpParams params);
	public static int GetSocketBufferSize (IHttpParams params);
	public static int GetSoTimeout (IHttpParams params);
	public static bool GetTcpNoDelay (IHttpParams params);
	public static bool IsStaleCheckingEnabled (IHttpParams params);
	public static void SetConnectionTimeout (IHttpParams params, int timeout);
	public static void SetLinger (IHttpParams params, int value);
	public static void SetSocketBufferSize (IHttpParams params, int size);
	public static void SetSoTimeout (IHttpParams params, int timeout);
	public static void SetStaleCheckingEnabled (IHttpParams params, bool value);
	public static void SetTcpNoDelay (IHttpParams params, bool value);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const string ConnectionTimeout = "http.connection.timeout";
		public const string MaxHeaderCount = "http.connection.max-header-count";
		public const string MaxLineLength = "http.connection.max-line-length";
		public const string SoLinger = "http.socket.linger";
		public const string SoTimeout = "http.socket.timeout";
		public const string SocketBufferSize = "http.socket.buffer-size";
		public const string StaleConnectionCheck = "http.connection.stalecheck";
		public const string TcpNodelay = "http.tcp.nodelay";
	}
}
```

<h3 id='Org.Apache.Http.Params.HttpProtocolParamBean'>New Type: Org.Apache.Http.Params.HttpProtocolParamBean</h3>

```
public class HttpProtocolParamBean : HttpAbstractParamBean {
	
	protected HttpProtocolParamBean (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpProtocolParamBean (IHttpParams params);
	
	public virtual void SetContentCharset (string contentCharset);
	public virtual void SetHttpElementCharset (string httpElementCharset);
	public virtual void SetUseExpectContinue (bool useExpectContinue);
	public virtual void SetUserAgent (string userAgent);
	public virtual void SetVersion (Org.Apache.Http.HttpVersion version);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Params.HttpProtocolParams'>New Type: Org.Apache.Http.Params.HttpProtocolParams</h3>

```
public sealed class HttpProtocolParams : Java.Lang.Object {
	
	public static string GetContentCharset (IHttpParams params);
	public static string GetHttpElementCharset (IHttpParams params);
	public static string GetUserAgent (IHttpParams params);
	public static Org.Apache.Http.ProtocolVersion GetVersion (IHttpParams params);
	public static void SetContentCharset (IHttpParams params, string charset);
	public static void SetHttpElementCharset (IHttpParams params, string charset);
	public static void SetUseExpectContinue (IHttpParams params, bool b);
	public static void SetUserAgent (IHttpParams params, string useragent);
	public static void SetVersion (IHttpParams params, Org.Apache.Http.ProtocolVersion version);
	public static bool UseExpectContinue (IHttpParams params);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const string HttpContentCharset = "http.protocol.content-charset";
		public const string HttpElementCharset = "http.protocol.element-charset";
		public const string OriginServer = "http.origin-server";
		public const string ProtocolVersion = "http.protocol.version";
		public const string StrictTransferEncoding = "http.protocol.strict-transfer-encoding";
		public const string UseExpectContinue = "http.protocol.expect-continue";
		public const string UserAgent = "http.useragent";
		public const string WaitForContinue = "http.protocol.wait-for-continue";
	}
}
```

<h3 id='Org.Apache.Http.Params.IHttpParams'>New Type: Org.Apache.Http.Params.IHttpParams</h3>

```
public interface IHttpParams : IDisposable, Android.Runtime.IJavaObject {
	
	IHttpParams Copy ();
	bool GetBooleanParameter (string name, bool defaultValue);
	double GetDoubleParameter (string name, double defaultValue);
	int GetIntParameter (string name, int defaultValue);
	long GetLongParameter (string name, long defaultValue);
	Java.Lang.Object GetParameter (string name);
	bool IsParameterFalse (string name);
	bool IsParameterTrue (string name);
	bool RemoveParameter (string name);
	IHttpParams SetBooleanParameter (string name, bool value);
	IHttpParams SetDoubleParameter (string name, double value);
	IHttpParams SetIntParameter (string name, int value);
	IHttpParams SetLongParameter (string name, long value);
	IHttpParams SetParameter (string name, Java.Lang.Object value);
}
```

<h2 id='Org.Apache.Http.Protocol'>Namespace: Org.Apache.Http.Protocol</h2>

<h3 id='Org.Apache.Http.Protocol.BasicHttpContext'>New Type: Org.Apache.Http.Protocol.BasicHttpContext</h3>

```
public class BasicHttpContext : Java.Lang.Object, IHttpContext {
	
	protected BasicHttpContext (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BasicHttpContext ();
	public BasicHttpContext (IHttpContext parentContext);
	
	public virtual Java.Lang.Object GetAttribute (string id);
	public virtual Java.Lang.Object RemoveAttribute (string id);
	public virtual void SetAttribute (string id, Java.Lang.Object obj);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const string ReservedPrefix = "http.";
	}
}
```

<h3 id='Org.Apache.Http.Protocol.BasicHttpProcessor'>New Type: Org.Apache.Http.Protocol.BasicHttpProcessor</h3>

```
public sealed class BasicHttpProcessor : Java.Lang.Object, Java.Lang.ICloneable, IHttpProcessor, Org.Apache.Http.IHttpRequestInterceptor, IHttpRequestInterceptorList, Org.Apache.Http.IHttpResponseInterceptor, IHttpResponseInterceptorList {
	
	public BasicHttpProcessor ();
	
	public void AddInterceptor (Org.Apache.Http.IHttpRequestInterceptor interceptor);
	public void AddInterceptor (Org.Apache.Http.IHttpRequestInterceptor interceptor, int index);
	public void AddInterceptor (Org.Apache.Http.IHttpResponseInterceptor interceptor);
	public void AddInterceptor (Org.Apache.Http.IHttpResponseInterceptor interceptor, int index);
	public void AddRequestInterceptor (Org.Apache.Http.IHttpRequestInterceptor itcp);
	public void AddRequestInterceptor (Org.Apache.Http.IHttpRequestInterceptor itcp, int index);
	public void AddResponseInterceptor (Org.Apache.Http.IHttpResponseInterceptor itcp);
	public void AddResponseInterceptor (Org.Apache.Http.IHttpResponseInterceptor itcp, int index);
	public void ClearInterceptors ();
	public void ClearRequestInterceptors ();
	public void ClearResponseInterceptors ();
	public Java.Lang.Object Clone ();
	public BasicHttpProcessor Copy ();
	protected void CopyInterceptors (BasicHttpProcessor target);
	public Org.Apache.Http.IHttpRequestInterceptor GetRequestInterceptor (int index);
	public Org.Apache.Http.IHttpResponseInterceptor GetResponseInterceptor (int index);
	public void Process (Org.Apache.Http.IHttpRequest request, IHttpContext context);
	public void Process (Org.Apache.Http.IHttpResponse response, IHttpContext context);
	public void RemoveRequestInterceptorByClass (Java.Lang.Class clazz);
	public void RemoveResponseInterceptorByClass (Java.Lang.Class clazz);
	public void SetInterceptors (System.Collections.IList list);
	
	public int RequestInterceptorCount {
		get;
	}
	public int ResponseInterceptorCount {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.DefaultedHttpContext'>New Type: Org.Apache.Http.Protocol.DefaultedHttpContext</h3>

```
public sealed class DefaultedHttpContext : Java.Lang.Object, IHttpContext {
	
	public DefaultedHttpContext (IHttpContext local, IHttpContext defaults);
	
	public Java.Lang.Object GetAttribute (string id);
	public Java.Lang.Object RemoveAttribute (string id);
	public void SetAttribute (string id, Java.Lang.Object obj);
	
	public IHttpContext Defaults {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public static class InterfaceConsts {
		
		public const string ReservedPrefix = "http.";
	}
}
```

<h3 id='Org.Apache.Http.Protocol.ExecutionContext'>New Type: Org.Apache.Http.Protocol.ExecutionContext</h3>

```
public abstract class ExecutionContext {
	
	public const string HttpConnection = "http.connection";
	public const string HttpProxyHost = "http.proxy_host";
	public const string HttpReqSent = "http.request_sent";
	public const string HttpRequest = "http.request";
	public const string HttpResponse = "http.response";
	public const string HttpTargetHost = "http.target_host";
}
```

<h3 id='Org.Apache.Http.Protocol.ExecutionContextConsts'>New Type: Org.Apache.Http.Protocol.ExecutionContextConsts</h3>

```
[Obsolete]
public abstract class ExecutionContextConsts : ExecutionContext {
}
```

<h3 id='Org.Apache.Http.Protocol.HTTP'>New Type: Org.Apache.Http.Protocol.HTTP</h3>

```
public sealed class HTTP : Java.Lang.Object {
	
	public static bool IsWhitespace (char ch);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Ascii = "ASCII";
	public const string CharsetParam = "; charset=";
	public const string ChunkCoding = "chunked";
	public const string ConnClose = "Close";
	public const string ConnDirective = "Connection";
	public const string ConnKeepAlive = "Keep-Alive";
	public const string ContentEncoding = "Content-Encoding";
	public const string ContentLen = "Content-Length";
	public const string ContentType = "Content-Type";
	public const int Cr = 13;
	public const string DateHeader = "Date";
	public const string DefaultContentCharset = "ISO-8859-1";
	public const string DefaultContentType = "application/octet-stream";
	public const string DefaultProtocolCharset = "US-ASCII";
	public const string ExpectContinue = "100-Continue";
	public const string ExpectDirective = "Expect";
	public const int Ht = 9;
	public const string IdentityCoding = "identity";
	public const string Iso88591 = "ISO-8859-1";
	public const int Lf = 10;
	public const string OctetStreamType = "application/octet-stream";
	public const string PlainTextType = "text/plain";
	public const string ServerHeader = "Server";
	public const int Sp = 32;
	public const string TargetHost = "Host";
	public const string TransferEncoding = "Transfer-Encoding";
	public const string UsAscii = "US-ASCII";
	public const string UserAgent = "User-Agent";
	public const string Utf16 = "UTF-16";
	public const string Utf8 = "UTF-8";
}
```

<h3 id='Org.Apache.Http.Protocol.HttpContext'>New Type: Org.Apache.Http.Protocol.HttpContext</h3>

```
public abstract class HttpContext {
	
	public const string ReservedPrefix = "http.";
}
```

<h3 id='Org.Apache.Http.Protocol.HttpContextConsts'>New Type: Org.Apache.Http.Protocol.HttpContextConsts</h3>

```
[Obsolete]
public abstract class HttpContextConsts : HttpContext {
}
```

<h3 id='Org.Apache.Http.Protocol.HttpDateGenerator'>New Type: Org.Apache.Http.Protocol.HttpDateGenerator</h3>

```
public class HttpDateGenerator : Java.Lang.Object {
	
	protected HttpDateGenerator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpDateGenerator ();
	
	public static Java.Util.TimeZone Gmt {
		get;
		set;
	}
	public virtual string CurrentDate {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string PatternRfc1123 = "EEE, dd MMM yyyy HH:mm:ss zzz";
}
```

<h3 id='Org.Apache.Http.Protocol.HttpRequestExecutor'>New Type: Org.Apache.Http.Protocol.HttpRequestExecutor</h3>

```
public class HttpRequestExecutor : Java.Lang.Object {
	
	protected HttpRequestExecutor (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpRequestExecutor ();
	
	protected virtual bool CanResponseHaveBody (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.IHttpResponse response);
	protected virtual Org.Apache.Http.IHttpResponse DoReceiveResponse (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.IHttpClientConnection conn, IHttpContext context);
	protected virtual Org.Apache.Http.IHttpResponse DoSendRequest (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.IHttpClientConnection conn, IHttpContext context);
	public virtual Org.Apache.Http.IHttpResponse Execute (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.IHttpClientConnection conn, IHttpContext context);
	public virtual void PostProcess (Org.Apache.Http.IHttpResponse response, IHttpProcessor processor, IHttpContext context);
	public virtual void PreProcess (Org.Apache.Http.IHttpRequest request, IHttpProcessor processor, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.HttpRequestHandlerRegistry'>New Type: Org.Apache.Http.Protocol.HttpRequestHandlerRegistry</h3>

```
public class HttpRequestHandlerRegistry : Java.Lang.Object, IHttpRequestHandlerResolver {
	
	protected HttpRequestHandlerRegistry (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpRequestHandlerRegistry ();
	
	public virtual IHttpRequestHandler Lookup (string requestURI);
	protected virtual bool MatchUriRequestPattern (string pattern, string requestUri);
	public virtual void Register (string pattern, IHttpRequestHandler handler);
	public virtual void SetHandlers (System.Collections.IDictionary map);
	public virtual void Unregister (string pattern);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.HttpService'>New Type: Org.Apache.Http.Protocol.HttpService</h3>

```
public class HttpService : Java.Lang.Object {
	
	protected HttpService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HttpService (IHttpProcessor proc, Org.Apache.Http.IConnectionReuseStrategy connStrategy, Org.Apache.Http.IHttpResponseFactory responseFactory);
	
	protected virtual void DoService (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.IHttpResponse response, IHttpContext context);
	protected virtual void HandleException (Org.Apache.Http.HttpException ex, Org.Apache.Http.IHttpResponse response);
	public virtual void HandleRequest (Org.Apache.Http.IHttpServerConnection conn, IHttpContext context);
	public virtual void SetConnReuseStrategy (Org.Apache.Http.IConnectionReuseStrategy connStrategy);
	public virtual void SetExpectationVerifier (IHttpExpectationVerifier expectationVerifier);
	public virtual void SetHandlerResolver (IHttpRequestHandlerResolver handlerResolver);
	public virtual void SetHttpProcessor (IHttpProcessor processor);
	public virtual void SetResponseFactory (Org.Apache.Http.IHttpResponseFactory responseFactory);
	
	public virtual Org.Apache.Http.Params.IHttpParams Params {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.IHttpContext'>New Type: Org.Apache.Http.Protocol.IHttpContext</h3>

```
public interface IHttpContext : IDisposable, Android.Runtime.IJavaObject {
	
	Java.Lang.Object GetAttribute (string id);
	Java.Lang.Object RemoveAttribute (string id);
	void SetAttribute (string id, Java.Lang.Object obj);
}
```

<h3 id='Org.Apache.Http.Protocol.IHttpExpectationVerifier'>New Type: Org.Apache.Http.Protocol.IHttpExpectationVerifier</h3>

```
public interface IHttpExpectationVerifier : IDisposable, Android.Runtime.IJavaObject {
	
	void Verify (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.IHttpResponse response, IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Protocol.IHttpProcessor'>New Type: Org.Apache.Http.Protocol.IHttpProcessor</h3>

```
public interface IHttpProcessor : IDisposable, Org.Apache.Http.IHttpRequestInterceptor, Org.Apache.Http.IHttpResponseInterceptor, Android.Runtime.IJavaObject {
}
```

<h3 id='Org.Apache.Http.Protocol.IHttpRequestHandler'>New Type: Org.Apache.Http.Protocol.IHttpRequestHandler</h3>

```
public interface IHttpRequestHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void handleRequest (Org.Apache.Http.IHttpRequest request, Org.Apache.Http.IHttpResponse response, IHttpContext context);
}
```

<h3 id='Org.Apache.Http.Protocol.IHttpRequestHandlerResolver'>New Type: Org.Apache.Http.Protocol.IHttpRequestHandlerResolver</h3>

```
public interface IHttpRequestHandlerResolver : IDisposable, Android.Runtime.IJavaObject {
	
	IHttpRequestHandler Lookup (string requestURI);
}
```

<h3 id='Org.Apache.Http.Protocol.IHttpRequestInterceptorList'>New Type: Org.Apache.Http.Protocol.IHttpRequestInterceptorList</h3>

```
public interface IHttpRequestInterceptorList : IDisposable, Android.Runtime.IJavaObject {
	
	void AddRequestInterceptor (Org.Apache.Http.IHttpRequestInterceptor itcp);
	void AddRequestInterceptor (Org.Apache.Http.IHttpRequestInterceptor itcp, int index);
	void ClearRequestInterceptors ();
	Org.Apache.Http.IHttpRequestInterceptor GetRequestInterceptor (int index);
	void RemoveRequestInterceptorByClass (Java.Lang.Class clazz);
	void SetInterceptors (System.Collections.IList itcps);
	
	int RequestInterceptorCount {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.IHttpResponseInterceptorList'>New Type: Org.Apache.Http.Protocol.IHttpResponseInterceptorList</h3>

```
public interface IHttpResponseInterceptorList : IDisposable, Android.Runtime.IJavaObject {
	
	void AddResponseInterceptor (Org.Apache.Http.IHttpResponseInterceptor itcp);
	void AddResponseInterceptor (Org.Apache.Http.IHttpResponseInterceptor itcp, int index);
	void ClearResponseInterceptors ();
	Org.Apache.Http.IHttpResponseInterceptor GetResponseInterceptor (int index);
	void RemoveResponseInterceptorByClass (Java.Lang.Class clazz);
	void SetInterceptors (System.Collections.IList itcps);
	
	int ResponseInterceptorCount {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.RequestConnControl'>New Type: Org.Apache.Http.Protocol.RequestConnControl</h3>

```
public class RequestConnControl : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestConnControl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestConnControl ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.RequestContent'>New Type: Org.Apache.Http.Protocol.RequestContent</h3>

```
public class RequestContent : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestContent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestContent ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.RequestDate'>New Type: Org.Apache.Http.Protocol.RequestDate</h3>

```
public class RequestDate : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestDate (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestDate ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.RequestExpectContinue'>New Type: Org.Apache.Http.Protocol.RequestExpectContinue</h3>

```
public class RequestExpectContinue : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestExpectContinue (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestExpectContinue ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.RequestTargetHost'>New Type: Org.Apache.Http.Protocol.RequestTargetHost</h3>

```
public class RequestTargetHost : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestTargetHost (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestTargetHost ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.RequestUserAgent'>New Type: Org.Apache.Http.Protocol.RequestUserAgent</h3>

```
public class RequestUserAgent : Java.Lang.Object, Org.Apache.Http.IHttpRequestInterceptor {
	
	protected RequestUserAgent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public RequestUserAgent ();
	
	public virtual void Process (Org.Apache.Http.IHttpRequest request, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.ResponseConnControl'>New Type: Org.Apache.Http.Protocol.ResponseConnControl</h3>

```
public class ResponseConnControl : Java.Lang.Object, Org.Apache.Http.IHttpResponseInterceptor {
	
	protected ResponseConnControl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ResponseConnControl ();
	
	public virtual void Process (Org.Apache.Http.IHttpResponse response, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.ResponseContent'>New Type: Org.Apache.Http.Protocol.ResponseContent</h3>

```
public class ResponseContent : Java.Lang.Object, Org.Apache.Http.IHttpResponseInterceptor {
	
	protected ResponseContent (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ResponseContent ();
	
	public virtual void Process (Org.Apache.Http.IHttpResponse response, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.ResponseDate'>New Type: Org.Apache.Http.Protocol.ResponseDate</h3>

```
public class ResponseDate : Java.Lang.Object, Org.Apache.Http.IHttpResponseInterceptor {
	
	protected ResponseDate (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ResponseDate ();
	
	public virtual void Process (Org.Apache.Http.IHttpResponse response, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.ResponseServer'>New Type: Org.Apache.Http.Protocol.ResponseServer</h3>

```
public class ResponseServer : Java.Lang.Object, Org.Apache.Http.IHttpResponseInterceptor {
	
	protected ResponseServer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ResponseServer ();
	
	public virtual void Process (Org.Apache.Http.IHttpResponse response, IHttpContext context);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.SyncBasicHttpContext'>New Type: Org.Apache.Http.Protocol.SyncBasicHttpContext</h3>

```
public class SyncBasicHttpContext : BasicHttpContext {
	
	protected SyncBasicHttpContext (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SyncBasicHttpContext (IHttpContext parentContext);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Protocol.UriPatternMatcher'>New Type: Org.Apache.Http.Protocol.UriPatternMatcher</h3>

```
public class UriPatternMatcher : Java.Lang.Object {
	
	protected UriPatternMatcher (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public UriPatternMatcher ();
	
	public virtual Java.Lang.Object Lookup (string requestURI);
	protected virtual bool MatchUriRequestPattern (string pattern, string requestUri);
	public virtual void Register (string pattern, Java.Lang.Object handler);
	public virtual void SetHandlers (System.Collections.IDictionary map);
	public virtual void Unregister (string pattern);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Apache.Http.Util'>Namespace: Org.Apache.Http.Util</h2>

<h3 id='Org.Apache.Http.Util.ByteArrayBuffer'>New Type: Org.Apache.Http.Util.ByteArrayBuffer</h3>

```
public sealed class ByteArrayBuffer : Java.Lang.Object {
	
	public ByteArrayBuffer (int capacity);
	
	public void Append (byte [] b, int off, int len);
	public void Append (char [] b, int off, int len);
	public void Append (CharArrayBuffer b, int off, int len);
	public void Append (int b);
	public byte [] Buffer ();
	public int ByteAt (int i);
	public int Capacity ();
	public void Clear ();
	public int Length ();
	public void SetLength (int len);
	public byte [] ToByteArray ();
	
	public bool IsEmpty {
		get;
	}
	public bool IsFull {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Util.CharArrayBuffer'>New Type: Org.Apache.Http.Util.CharArrayBuffer</h3>

```
public sealed class CharArrayBuffer : Java.Lang.Object {
	
	public CharArrayBuffer (int capacity);
	
	public void Append (byte [] b, int off, int len);
	public void Append (ByteArrayBuffer b, int off, int len);
	public void Append (char ch);
	public void Append (char [] b, int off, int len);
	public void Append (CharArrayBuffer b);
	public void Append (CharArrayBuffer b, int off, int len);
	public void Append (Java.Lang.Object obj);
	public void Append (string str);
	public char [] Buffer ();
	public int Capacity ();
	public char CharAt (int i);
	public void Clear ();
	public void EnsureCapacity (int required);
	public int IndexOf (int ch);
	public int IndexOf (int ch, int beginIndex, int endIndex);
	public int Length ();
	public void SetLength (int len);
	public string Substring (int beginIndex, int endIndex);
	public string SubstringTrimmed (int beginIndex, int endIndex);
	public char [] ToCharArray ();
	
	public bool IsEmpty {
		get;
	}
	public bool IsFull {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Util.EncodingUtils'>New Type: Org.Apache.Http.Util.EncodingUtils</h3>

```
public sealed class EncodingUtils : Java.Lang.Object {
	
	public static byte [] GetAsciiBytes (string data);
	public static string GetAsciiString (byte [] data);
	public static string GetAsciiString (byte [] data, int offset, int length);
	public static byte [] GetBytes (string data, string charset);
	public static string GetString (byte [] data, int offset, int length, string charset);
	public static string GetString (byte [] data, string charset);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Util.EntityUtils'>New Type: Org.Apache.Http.Util.EntityUtils</h3>

```
public sealed class EntityUtils : Java.Lang.Object {
	
	public static string GetContentCharSet (Org.Apache.Http.IHttpEntity entity);
	public static byte [] ToByteArray (Org.Apache.Http.IHttpEntity entity);
	public static string ToString (Org.Apache.Http.IHttpEntity entity);
	public static string ToString (Org.Apache.Http.IHttpEntity entity, string defaultCharset);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Util.ExceptionUtils'>New Type: Org.Apache.Http.Util.ExceptionUtils</h3>

```
public sealed class ExceptionUtils : Java.Lang.Object {
	
	public static void InitCause (Java.Lang.Throwable throwable, Java.Lang.Throwable cause);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Apache.Http.Util.LangUtils'>New Type: Org.Apache.Http.Util.LangUtils</h3>

```
public sealed class LangUtils : Java.Lang.Object {
	
	public static bool Equals (Java.Lang.Object obj1, Java.Lang.Object obj2);
	public static bool Equals (Java.Lang.Object[] a1, Java.Lang.Object[] a2);
	public static int HashCode (int seed, bool b);
	public static int HashCode (int seed, int hashcode);
	public static int HashCode (int seed, Java.Lang.Object obj);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int HashOffset = 37;
	public const int HashSeed = 17;
}
```

<h3 id='Org.Apache.Http.Util.VersionInfo'>New Type: Org.Apache.Http.Util.VersionInfo</h3>

```
public class VersionInfo : Java.Lang.Object {
	
	protected VersionInfo (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected VersionInfo (string pckg, string module, string release, string time, string clsldr);
	
	protected static VersionInfo FromMap (string pckg, System.Collections.IDictionary info, Java.Lang.ClassLoader clsldr);
	public static VersionInfo LoadVersionInfo (string pckg, Java.Lang.ClassLoader clsldr);
	public static VersionInfo[] LoadVersionInfo (string [] pckgs, Java.Lang.ClassLoader clsldr);
	
	public string Classloader {
		get;
	}
	public string Module {
		get;
	}
	public string Package {
		get;
	}
	public string Release {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public string Timestamp {
		get;
	}
	
	public const string PropertyModule = "info.module";
	public const string PropertyRelease = "info.release";
	public const string PropertyTimestamp = "info.timestamp";
	public const string Unavailable = "UNAVAILABLE";
	public const string VersionPropertyFile = "version.properties";
}
```

<h2 id='Org.Json'>Namespace: Org.Json</h2>

<h3 id='Org.Json.JSONArray'>New Type: Org.Json.JSONArray</h3>

```
public class JSONArray : Java.Lang.Object {
	
	protected JSONArray (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JSONArray ();
	public JSONArray (string string);
	public JSONArray (System.Collections.ICollection collection);
	public JSONArray (JSONTokener x);
	
	public virtual Java.Lang.Object Get (int index);
	public virtual bool GetBoolean (int index);
	public virtual double GetDouble (int index);
	public virtual int GetInt (int index);
	public virtual JSONArray GetJSONArray (int index);
	public virtual JSONObject GetJSONObject (int index);
	public virtual long GetLong (int index);
	public virtual string GetString (int index);
	public virtual bool IsNull (int index);
	public virtual string Join (string separator);
	public virtual int Length ();
	public virtual Java.Lang.Object Opt (int index);
	public virtual bool OptBoolean (int index);
	public virtual bool OptBoolean (int index, bool defaultValue);
	public virtual double OptDouble (int index);
	public virtual double OptDouble (int index, double defaultValue);
	public virtual int OptInt (int index);
	public virtual int OptInt (int index, int defaultValue);
	public virtual JSONArray OptJSONArray (int index);
	public virtual JSONObject OptJSONObject (int index);
	public virtual long OptLong (int index);
	public virtual long OptLong (int index, long defaultValue);
	public virtual string OptString (int index);
	public virtual string OptString (int index, string defaultValue);
	public virtual JSONArray Put (bool value);
	public virtual JSONArray Put (double value);
	public virtual JSONArray Put (int value);
	public virtual JSONArray Put (int index, bool value);
	public virtual JSONArray Put (int index, double value);
	public virtual JSONArray Put (int index, int value);
	public virtual JSONArray Put (int index, long value);
	public virtual JSONArray Put (int index, Java.Lang.Object value);
	public virtual JSONArray Put (long value);
	public virtual JSONArray Put (Java.Lang.Object value);
	public virtual JSONObject ToJSONObject (JSONArray names);
	public virtual string ToString (int indentFactor);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Json.JSONException'>New Type: Org.Json.JSONException</h3>

```
public class JSONException : Java.Lang.Exception {
	
	protected JSONException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JSONException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Json.JSONObject'>New Type: Org.Json.JSONObject</h3>

```
public class JSONObject : Java.Lang.Object {
	
	protected JSONObject (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JSONObject ();
	public JSONObject (string string);
	public JSONObject (System.Collections.IDictionary map);
	public JSONObject (JSONObject jo, string [] sa);
	public JSONObject (JSONTokener x);
	
	public static string NumberToString (Java.Lang.Number n);
	public static string Quote (string string);
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
	public virtual Java.Util.IIterator Keys ();
	public virtual int Length ();
	public virtual JSONArray Names ();
	public virtual Java.Lang.Object Opt (string key);
	public virtual bool OptBoolean (string key);
	public virtual bool OptBoolean (string key, bool defaultValue);
	public virtual double OptDouble (string key);
	public virtual double OptDouble (string key, double defaultValue);
	public virtual int OptInt (string key);
	public virtual int OptInt (string key, int defaultValue);
	public virtual JSONArray OptJSONArray (string key);
	public virtual JSONObject OptJSONObject (string key);
	public virtual long OptLong (string key);
	public virtual long OptLong (string key, long defaultValue);
	public virtual string OptString (string key);
	public virtual string OptString (string key, string defaultValue);
	public virtual JSONObject Put (string key, bool value);
	public virtual JSONObject Put (string key, double value);
	public virtual JSONObject Put (string key, int value);
	public virtual JSONObject Put (string key, long value);
	public virtual JSONObject Put (string key, Java.Lang.Object value);
	public virtual JSONObject PutOpt (string key, Java.Lang.Object value);
	public virtual Java.Lang.Object Remove (string key);
	public virtual JSONArray ToJSONArray (JSONArray names);
	public virtual string ToString (int indentFactor);
	
	public static Java.Lang.Object Null {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Json.JSONStringer'>New Type: Org.Json.JSONStringer</h3>

```
public class JSONStringer : Java.Lang.Object {
	
	protected JSONStringer (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JSONStringer ();
	
	public virtual JSONStringer Array ();
	public virtual JSONStringer EndArray ();
	public virtual JSONStringer EndObject ();
	public virtual JSONStringer Key (string s);
	public virtual JSONStringer Object ();
	public virtual JSONStringer Value (bool b);
	public virtual JSONStringer Value (double d);
	public virtual JSONStringer Value (long l);
	public virtual JSONStringer Value (Java.Lang.Object o);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Json.JSONTokener'>New Type: Org.Json.JSONTokener</h3>

```
public class JSONTokener : Java.Lang.Object {
	
	protected JSONTokener (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public JSONTokener (string s);
	
	public static int Dehexchar (char c);
	public virtual void Back ();
	public virtual bool More ();
	public virtual char Next ();
	public virtual char Next (char c);
	public virtual string Next (int n);
	public virtual char NextClean ();
	public virtual string NextString (char quote);
	public virtual string NextTo (char d);
	public virtual string NextTo (string delimiters);
	public virtual Java.Lang.Object NextValue ();
	public virtual void SkipPast (string to);
	public virtual char SkipTo (char to);
	public virtual JSONException SyntaxError (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.W3c.Dom'>Namespace: Org.W3c.Dom</h2>

<h3 id='Org.W3c.Dom.DOMError'>New Type: Org.W3c.Dom.DOMError</h3>

```
public abstract class DOMError {
	
	public const short SeverityError = 2;
	public const short SeverityFatalError = 3;
	public const short SeverityWarning = 1;
}
```

<h3 id='Org.W3c.Dom.DOMErrorConsts'>New Type: Org.W3c.Dom.DOMErrorConsts</h3>

```
[Obsolete]
public abstract class DOMErrorConsts : DOMError {
}
```

<h3 id='Org.W3c.Dom.DOMException'>New Type: Org.W3c.Dom.DOMException</h3>

```
public class DOMException : Java.Lang.RuntimeException {
	
	protected DOMException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DOMException (short code, string message);
	
	public static short TypeMismatchErr {
		get;
		set;
	}
	public static short ValidationErr {
		get;
		set;
	}
	public short Code {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const short DomstringSizeErr = 2;
	public const short HierarchyRequestErr = 3;
	public const short IndexSizeErr = 1;
	public const short InuseAttributeErr = 10;
	public const short InvalidAccessErr = 15;
	public const short InvalidCharacterErr = 5;
	public const short InvalidModificationErr = 13;
	public const short InvalidStateErr = 11;
	public const short NamespaceErr = 14;
	public const short NoDataAllowedErr = 6;
	public const short NoModificationAllowedErr = 7;
	public const short NotFoundErr = 8;
	public const short NotSupportedErr = 9;
	public const short SyntaxErr = 12;
	public const short WrongDocumentErr = 4;
}
```

<h3 id='Org.W3c.Dom.IAttr'>New Type: Org.W3c.Dom.IAttr</h3>

```
public interface IAttr : IDisposable, Android.Runtime.IJavaObject, INode {
	
	bool IsId {
		get;
	}
	string Name {
		get;
	}
	IElement OwnerElement {
		get;
	}
	ITypeInfo SchemaTypeInfo {
		get;
	}
	bool Specified {
		get;
	}
	string Value {
		get;
		set;
	}
}
```

<h3 id='Org.W3c.Dom.ICDATASection'>New Type: Org.W3c.Dom.ICDATASection</h3>

```
public interface ICDATASection : ICharacterData, IDisposable, Android.Runtime.IJavaObject, INode, IText {
}
```

<h3 id='Org.W3c.Dom.ICharacterData'>New Type: Org.W3c.Dom.ICharacterData</h3>

```
public interface ICharacterData : IDisposable, Android.Runtime.IJavaObject, INode {
	
	void AppendData (string arg);
	void DeleteData (int offset, int count);
	void InsertData (int offset, string arg);
	void ReplaceData (int offset, int count, string arg);
	string SubstringData (int offset, int count);
	
	string Data {
		get;
		set;
	}
	int Length {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IComment'>New Type: Org.W3c.Dom.IComment</h3>

```
public interface IComment : ICharacterData, IDisposable, Android.Runtime.IJavaObject, INode {
}
```

<h3 id='Org.W3c.Dom.IDOMConfiguration'>New Type: Org.W3c.Dom.IDOMConfiguration</h3>

```
public interface IDOMConfiguration : IDisposable, Android.Runtime.IJavaObject {
	
	bool CanSetParameter (string name, Java.Lang.Object value);
	Java.Lang.Object GetParameter (string name);
	void SetParameter (string name, Java.Lang.Object value);
	
	IDOMStringList ParameterNames {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IDOMError'>New Type: Org.W3c.Dom.IDOMError</h3>

```
public interface IDOMError : IDisposable, Android.Runtime.IJavaObject {
	
	IDOMLocator Location {
		get;
	}
	string Message {
		get;
	}
	Java.Lang.Object RelatedData {
		get;
	}
	Java.Lang.Object RelatedException {
		get;
	}
	short Severity {
		get;
	}
	string Type {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IDOMErrorHandler'>New Type: Org.W3c.Dom.IDOMErrorHandler</h3>

```
public interface IDOMErrorHandler : IDisposable, Android.Runtime.IJavaObject {
	
	bool HandleError (IDOMError error);
}
```

<h3 id='Org.W3c.Dom.IDOMImplementation'>New Type: Org.W3c.Dom.IDOMImplementation</h3>

```
public interface IDOMImplementation : IDisposable, Android.Runtime.IJavaObject {
	
	IDocument CreateDocument (string namespaceURI, string qualifiedName, IDocumentType doctype);
	IDocumentType CreateDocumentType (string qualifiedName, string publicId, string systemId);
	Java.Lang.Object GetFeature (string p0, string p1);
	bool HasFeature (string feature, string version);
}
```

<h3 id='Org.W3c.Dom.IDOMImplementationList'>New Type: Org.W3c.Dom.IDOMImplementationList</h3>

```
public interface IDOMImplementationList : IDisposable, Android.Runtime.IJavaObject {
	
	IDOMImplementation Item (int index);
	
	int Length {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IDOMImplementationSource'>New Type: Org.W3c.Dom.IDOMImplementationSource</h3>

```
public interface IDOMImplementationSource : IDisposable, Android.Runtime.IJavaObject {
	
	IDOMImplementation GetDOMImplementation (string features);
	IDOMImplementationList GetDOMImplementationList (string features);
}
```

<h3 id='Org.W3c.Dom.IDOMLocator'>New Type: Org.W3c.Dom.IDOMLocator</h3>

```
public interface IDOMLocator : IDisposable, Android.Runtime.IJavaObject {
	
	int ByteOffset {
		get;
	}
	int ColumnNumber {
		get;
	}
	int LineNumber {
		get;
	}
	INode RelatedNode {
		get;
	}
	string Uri {
		get;
	}
	int Utf16Offset {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IDOMStringList'>New Type: Org.W3c.Dom.IDOMStringList</h3>

```
public interface IDOMStringList : IDisposable, Android.Runtime.IJavaObject {
	
	bool Contains (string str);
	string Item (int index);
	
	int Length {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IDocument'>New Type: Org.W3c.Dom.IDocument</h3>

```
public interface IDocument : IDisposable, Android.Runtime.IJavaObject, INode {
	
	INode AdoptNode (INode p0);
	IAttr CreateAttribute (string name);
	IAttr CreateAttributeNS (string namespaceURI, string qualifiedName);
	ICDATASection CreateCDATASection (string data);
	IComment CreateComment (string data);
	IDocumentFragment CreateDocumentFragment ();
	IElement CreateElement (string tagName);
	IElement CreateElementNS (string namespaceURI, string qualifiedName);
	IEntityReference CreateEntityReference (string name);
	IProcessingInstruction CreateProcessingInstruction (string target, string data);
	IText CreateTextNode (string data);
	IElement GetElementById (string elementId);
	INodeList GetElementsByTagName (string tagname);
	INodeList GetElementsByTagNameNS (string namespaceURI, string localName);
	INode ImportNode (INode importedNode, bool deep);
	void NormalizeDocument ();
	INode RenameNode (INode p0, string p1, string p2);
	
	IDocumentType Doctype {
		get;
	}
	IElement DocumentElement {
		get;
	}
	string DocumentURI {
		get;
		set;
	}
	IDOMConfiguration DomConfig {
		get;
	}
	IDOMImplementation Implementation {
		get;
	}
	string InputEncoding {
		get;
	}
	bool StrictErrorChecking {
		get;
		set;
	}
	string XmlEncoding {
		get;
	}
	bool XmlStandalone {
		get;
		set;
	}
	string XmlVersion {
		get;
		set;
	}
}
```

<h3 id='Org.W3c.Dom.IDocumentFragment'>New Type: Org.W3c.Dom.IDocumentFragment</h3>

```
public interface IDocumentFragment : IDisposable, Android.Runtime.IJavaObject, INode {
}
```

<h3 id='Org.W3c.Dom.IDocumentType'>New Type: Org.W3c.Dom.IDocumentType</h3>

```
public interface IDocumentType : IDisposable, Android.Runtime.IJavaObject, INode {
	
	INamedNodeMap Entities {
		get;
	}
	string InternalSubset {
		get;
	}
	string Name {
		get;
	}
	INamedNodeMap Notations {
		get;
	}
	string PublicId {
		get;
	}
	string SystemId {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IElement'>New Type: Org.W3c.Dom.IElement</h3>

```
public interface IElement : IDisposable, Android.Runtime.IJavaObject, INode {
	
	string GetAttribute (string name);
	IAttr GetAttributeNode (string name);
	IAttr GetAttributeNodeNS (string namespaceURI, string localName);
	string GetAttributeNS (string namespaceURI, string localName);
	INodeList GetElementsByTagName (string name);
	INodeList GetElementsByTagNameNS (string namespaceURI, string localName);
	bool HasAttribute (string name);
	bool HasAttributeNS (string namespaceURI, string localName);
	void RemoveAttribute (string name);
	IAttr RemoveAttributeNode (IAttr oldAttr);
	void RemoveAttributeNS (string namespaceURI, string localName);
	void SetAttribute (string name, string value);
	IAttr SetAttributeNode (IAttr newAttr);
	IAttr SetAttributeNodeNS (IAttr newAttr);
	void SetAttributeNS (string namespaceURI, string qualifiedName, string value);
	void SetIdAttribute (string p0, bool p1);
	void SetIdAttributeNode (IAttr p0, bool p1);
	void SetIdAttributeNS (string p0, string p1, bool p2);
	
	ITypeInfo SchemaTypeInfo {
		get;
	}
	string TagName {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IEntity'>New Type: Org.W3c.Dom.IEntity</h3>

```
public interface IEntity : IDisposable, Android.Runtime.IJavaObject, INode {
	
	string InputEncoding {
		get;
	}
	string NotationName {
		get;
	}
	string PublicId {
		get;
	}
	string SystemId {
		get;
	}
	string XmlEncoding {
		get;
	}
	string XmlVersion {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IEntityReference'>New Type: Org.W3c.Dom.IEntityReference</h3>

```
public interface IEntityReference : IDisposable, Android.Runtime.IJavaObject, INode {
}
```

<h3 id='Org.W3c.Dom.INameList'>New Type: Org.W3c.Dom.INameList</h3>

```
public interface INameList : IDisposable, Android.Runtime.IJavaObject {
	
	bool Contains (string str);
	bool ContainsNS (string namespaceURI, string name);
	string GetName (int index);
	string GetNamespaceURI (int index);
	
	int Length {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.INamedNodeMap'>New Type: Org.W3c.Dom.INamedNodeMap</h3>

```
public interface INamedNodeMap : IDisposable, Android.Runtime.IJavaObject {
	
	INode GetNamedItem (string name);
	INode GetNamedItemNS (string namespaceURI, string localName);
	INode Item (int index);
	INode RemoveNamedItem (string name);
	INode RemoveNamedItemNS (string namespaceURI, string localName);
	INode SetNamedItem (INode arg);
	INode SetNamedItemNS (INode arg);
	
	int Length {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.INode'>New Type: Org.W3c.Dom.INode</h3>

```
public interface INode : IDisposable, Android.Runtime.IJavaObject {
	
	INode AppendChild (INode newChild);
	INode CloneNode (bool deep);
	short CompareDocumentPosition (INode p0);
	Java.Lang.Object GetFeature (string p0, string p1);
	Java.Lang.Object GetUserData (string p0);
	INode InsertBefore (INode newChild, INode refChild);
	bool IsDefaultNamespace (string p0);
	bool IsEqualNode (INode p0);
	bool IsSameNode (INode p0);
	bool IsSupported (string feature, string version);
	string LookupNamespaceURI (string p0);
	string LookupPrefix (string p0);
	void Normalize ();
	INode RemoveChild (INode oldChild);
	INode ReplaceChild (INode newChild, INode oldChild);
	Java.Lang.Object SetUserData (string p0, Java.Lang.Object p1, IUserDataHandler p2);
	
	INamedNodeMap Attributes {
		get;
	}
	string BaseURI {
		get;
	}
	INodeList ChildNodes {
		get;
	}
	INode FirstChild {
		get;
	}
	bool HasAttributes {
		get;
	}
	bool HasChildNodes {
		get;
	}
	INode LastChild {
		get;
	}
	string LocalName {
		get;
	}
	string NamespaceURI {
		get;
	}
	INode NextSibling {
		get;
	}
	string NodeName {
		get;
	}
	short NodeType {
		get;
	}
	string NodeValue {
		get;
		set;
	}
	IDocument OwnerDocument {
		get;
	}
	INode ParentNode {
		get;
	}
	string Prefix {
		get;
		set;
	}
	INode PreviousSibling {
		get;
	}
	string TextContent {
		get;
		set;
	}
}
```

<h3 id='Org.W3c.Dom.INodeList'>New Type: Org.W3c.Dom.INodeList</h3>

```
public interface INodeList : IDisposable, Android.Runtime.IJavaObject {
	
	INode Item (int index);
	
	int Length {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.INotation'>New Type: Org.W3c.Dom.INotation</h3>

```
public interface INotation : IDisposable, Android.Runtime.IJavaObject, INode {
	
	string PublicId {
		get;
	}
	string SystemId {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IProcessingInstruction'>New Type: Org.W3c.Dom.IProcessingInstruction</h3>

```
public interface IProcessingInstruction : IDisposable, Android.Runtime.IJavaObject, INode {
	
	string Data {
		get;
		set;
	}
	string Target {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IText'>New Type: Org.W3c.Dom.IText</h3>

```
public interface IText : ICharacterData, IDisposable, Android.Runtime.IJavaObject, INode {
	
	IText ReplaceWholeText (string p0);
	IText SplitText (int offset);
	
	bool IsElementContentWhitespace {
		get;
	}
	string WholeText {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.ITypeInfo'>New Type: Org.W3c.Dom.ITypeInfo</h3>

```
public interface ITypeInfo : IDisposable, Android.Runtime.IJavaObject {
	
	bool IsDerivedFrom (string typeNamespaceArg, string typeNameArg, int derivationMethod);
	
	string TypeName {
		get;
	}
	string TypeNamespace {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.IUserDataHandler'>New Type: Org.W3c.Dom.IUserDataHandler</h3>

```
public interface IUserDataHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void handleData (short operation, string key, Java.Lang.Object data, INode src, INode dst);
}
```

<h3 id='Org.W3c.Dom.Node'>New Type: Org.W3c.Dom.Node</h3>

```
public abstract class Node {
	
	public static short DocumentPositionContainedBy {
		get;
		set;
	}
	public static short DocumentPositionContains {
		get;
		set;
	}
	public static short DocumentPositionDisconnected {
		get;
		set;
	}
	public static short DocumentPositionFollowing {
		get;
		set;
	}
	public static short DocumentPositionImplementationSpecific {
		get;
		set;
	}
	public static short DocumentPositionPreceding {
		get;
		set;
	}
	
	public const short AttributeNode = 2;
	public const short CdataSectionNode = 4;
	public const short CommentNode = 8;
	public const short DocumentFragmentNode = 11;
	public const short DocumentNode = 9;
	public const short DocumentTypeNode = 10;
	public const short ElementNode = 1;
	public const short EntityNode = 6;
	public const short EntityReferenceNode = 5;
	public const short NotationNode = 12;
	public const short ProcessingInstructionNode = 7;
	public const short TextNode = 3;
}
```

<h3 id='Org.W3c.Dom.NodeConsts'>New Type: Org.W3c.Dom.NodeConsts</h3>

```
[Obsolete]
public abstract class NodeConsts : Node {
}
```

<h3 id='Org.W3c.Dom.TypeInfo'>New Type: Org.W3c.Dom.TypeInfo</h3>

```
public abstract class TypeInfo {
	
	public const int DerivationExtension = 2;
	public const int DerivationList = 8;
	public const int DerivationRestriction = 1;
	public const int DerivationUnion = 4;
}
```

<h3 id='Org.W3c.Dom.TypeInfoConsts'>New Type: Org.W3c.Dom.TypeInfoConsts</h3>

```
[Obsolete]
public abstract class TypeInfoConsts : TypeInfo {
}
```

<h3 id='Org.W3c.Dom.UserDataHandler'>New Type: Org.W3c.Dom.UserDataHandler</h3>

```
public abstract class UserDataHandler {
	
	public const short NodeAdopted = 5;
	public const short NodeCloned = 1;
	public const short NodeDeleted = 3;
	public const short NodeImported = 2;
	public const short NodeRenamed = 4;
}
```

<h3 id='Org.W3c.Dom.UserDataHandlerConsts'>New Type: Org.W3c.Dom.UserDataHandlerConsts</h3>

```
[Obsolete]
public abstract class UserDataHandlerConsts : UserDataHandler {
}
```

<h2 id='Org.W3c.Dom.LS'>Namespace: Org.W3c.Dom.LS</h2>

<h3 id='Org.W3c.Dom.LS.ILSInput'>New Type: Org.W3c.Dom.LS.ILSInput</h3>

```
public interface ILSInput : IDisposable, Android.Runtime.IJavaObject {
	
	string BaseURI {
		get;
		set;
	}
	System.IO.Stream ByteStream {
		get;
		set;
	}
	bool CertifiedText {
		get;
		set;
	}
	Java.IO.Reader CharacterStream {
		get;
		set;
	}
	string Encoding {
		get;
		set;
	}
	string PublicId {
		get;
		set;
	}
	string StringData {
		get;
		set;
	}
	string SystemId {
		get;
		set;
	}
}
```

<h3 id='Org.W3c.Dom.LS.ILSOutput'>New Type: Org.W3c.Dom.LS.ILSOutput</h3>

```
public interface ILSOutput : IDisposable, Android.Runtime.IJavaObject {
	
	System.IO.Stream ByteStream {
		get;
		set;
	}
	Java.IO.Writer CharacterStream {
		get;
		set;
	}
	string Encoding {
		get;
		set;
	}
	string SystemId {
		get;
		set;
	}
}
```

<h3 id='Org.W3c.Dom.LS.ILSParser'>New Type: Org.W3c.Dom.LS.ILSParser</h3>

```
public interface ILSParser : IDisposable, Android.Runtime.IJavaObject {
	
	void Abort ();
	Org.W3c.Dom.IDocument Parse (ILSInput input);
	Org.W3c.Dom.IDocument ParseURI (string uri);
	Org.W3c.Dom.INode ParseWithContext (ILSInput input, Org.W3c.Dom.INode contextArg, short action);
	
	bool Async {
		get;
	}
	bool Busy {
		get;
	}
	Org.W3c.Dom.IDOMConfiguration DomConfig {
		get;
	}
	ILSParserFilter Filter {
		get;
		set;
	}
}
```

<h3 id='Org.W3c.Dom.LS.ILSParserExtensions'>New Type: Org.W3c.Dom.LS.ILSParserExtensions</h3>

```
public static class ILSParserExtensions {
	
	public static System.Threading.Tasks.Task ParseAsync (ILSParser self, ILSInput input);
	public static System.Threading.Tasks.Task ParseURIAsync (ILSParser self, string uri);
	public static System.Threading.Tasks.Task ParseWithContextAsync (ILSParser self, ILSInput input, Org.W3c.Dom.INode contextArg, short action);
}
```

<h3 id='Org.W3c.Dom.LS.ILSParserFilter'>New Type: Org.W3c.Dom.LS.ILSParserFilter</h3>

```
public interface ILSParserFilter : IDisposable, Android.Runtime.IJavaObject {
	
	short AcceptNode (Org.W3c.Dom.INode nodeArg);
	short StartElement (Org.W3c.Dom.IElement elementArg);
	
	int WhatToShow {
		get;
	}
}
```

<h3 id='Org.W3c.Dom.LS.ILSResourceResolver'>New Type: Org.W3c.Dom.LS.ILSResourceResolver</h3>

```
public interface ILSResourceResolver : IDisposable, Android.Runtime.IJavaObject {
	
	ILSInput ResolveResource (string type, string namespaceURI, string publicId, string systemId, string baseURI);
}
```

<h3 id='Org.W3c.Dom.LS.LSException'>New Type: Org.W3c.Dom.LS.LSException</h3>

```
public class LSException : Java.Lang.RuntimeException {
	
	protected LSException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LSException (short code, string message);
	
	public short Code {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const short ParseErr = 81;
	public const short SerializeErr = 82;
}
```

<h3 id='Org.W3c.Dom.LS.LSParser'>New Type: Org.W3c.Dom.LS.LSParser</h3>

```
public abstract class LSParser {
	
	public const short ActionAppendAsChildren = 1;
	public const short ActionInsertAfter = 4;
	public const short ActionInsertBefore = 3;
	public const short ActionReplace = 5;
	public const short ActionReplaceChildren = 2;
}
```

<h3 id='Org.W3c.Dom.LS.LSParserConsts'>New Type: Org.W3c.Dom.LS.LSParserConsts</h3>

```
[Obsolete]
public abstract class LSParserConsts : LSParser {
}
```

<h3 id='Org.W3c.Dom.LS.LSParserFilter'>New Type: Org.W3c.Dom.LS.LSParserFilter</h3>

```
public abstract class LSParserFilter {
	
	public const short FilterAccept = 1;
	public const short FilterInterrupt = 4;
	public const short FilterReject = 2;
	public const short FilterSkip = 3;
}
```

<h3 id='Org.W3c.Dom.LS.LSParserFilterConsts'>New Type: Org.W3c.Dom.LS.LSParserFilterConsts</h3>

```
[Obsolete]
public abstract class LSParserFilterConsts : LSParserFilter {
}
```

<h2 id='Org.Xml.Sax'>Namespace: Org.Xml.Sax</h2>

<h3 id='Org.Xml.Sax.HandlerBase'>New Type: Org.Xml.Sax.HandlerBase</h3>

```
public class HandlerBase : Java.Lang.Object, IDocumentHandler, IDTDHandler, IEntityResolver, IErrorHandler {
	
	protected HandlerBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public HandlerBase ();
	
	public virtual void Characters (char [] ch, int start, int length);
	public virtual void EndDocument ();
	public virtual void EndElement (string name);
	public virtual void Error (SAXParseException e);
	public virtual void FatalError (SAXParseException e);
	public virtual void IgnorableWhitespace (char [] ch, int start, int length);
	public virtual void NotationDecl (string name, string publicId, string systemId);
	public virtual void ProcessingInstruction (string target, string data);
	public virtual InputSource ResolveEntity (string publicId, string systemId);
	public virtual void SetDocumentLocator (ILocator locator);
	public virtual void StartDocument ();
	public virtual void StartElement (string name, IAttributeList attributes);
	public virtual void UnparsedEntityDecl (string name, string publicId, string systemId, string notationName);
	public virtual void Warning (SAXParseException e);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.IAttributeList'>New Type: Org.Xml.Sax.IAttributeList</h3>

```
public interface IAttributeList : IDisposable, Android.Runtime.IJavaObject {
	
	string GetName (int i);
	string GetType (int i);
	string GetType (string name);
	string GetValue (int i);
	string GetValue (string name);
	
	int Length {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.IAttributes'>New Type: Org.Xml.Sax.IAttributes</h3>

```
public interface IAttributes : IDisposable, Android.Runtime.IJavaObject {
	
	int GetIndex (string qName);
	int GetIndex (string uri, string localName);
	string GetLocalName (int index);
	string GetQName (int index);
	string GetType (int index);
	string GetType (string qName);
	string GetType (string uri, string localName);
	string GetURI (int index);
	string GetValue (int index);
	string GetValue (string qName);
	string GetValue (string uri, string localName);
	
	int Length {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.IContentHandler'>New Type: Org.Xml.Sax.IContentHandler</h3>

```
public interface IContentHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void Characters (char [] ch, int start, int length);
	void EndDocument ();
	void EndElement (string uri, string localName, string qName);
	void EndPrefixMapping (string prefix);
	void IgnorableWhitespace (char [] ch, int start, int length);
	void ProcessingInstruction (string target, string data);
	void SetDocumentLocator (ILocator locator);
	void SkippedEntity (string name);
	void StartDocument ();
	void StartElement (string uri, string localName, string qName, IAttributes atts);
	void StartPrefixMapping (string prefix, string uri);
}
```

<h3 id='Org.Xml.Sax.IDTDHandler'>New Type: Org.Xml.Sax.IDTDHandler</h3>

```
public interface IDTDHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void NotationDecl (string name, string publicId, string systemId);
	void UnparsedEntityDecl (string name, string publicId, string systemId, string notationName);
}
```

<h3 id='Org.Xml.Sax.IDocumentHandler'>New Type: Org.Xml.Sax.IDocumentHandler</h3>

```
public interface IDocumentHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void Characters (char [] ch, int start, int length);
	void EndDocument ();
	void EndElement (string name);
	void IgnorableWhitespace (char [] ch, int start, int length);
	void ProcessingInstruction (string target, string data);
	void SetDocumentLocator (ILocator locator);
	void StartDocument ();
	void StartElement (string name, IAttributeList atts);
}
```

<h3 id='Org.Xml.Sax.IEntityResolver'>New Type: Org.Xml.Sax.IEntityResolver</h3>

```
public interface IEntityResolver : IDisposable, Android.Runtime.IJavaObject {
	
	InputSource ResolveEntity (string publicId, string systemId);
}
```

<h3 id='Org.Xml.Sax.IErrorHandler'>New Type: Org.Xml.Sax.IErrorHandler</h3>

```
public interface IErrorHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void Error (SAXParseException exception);
	void FatalError (SAXParseException exception);
	void Warning (SAXParseException exception);
}
```

<h3 id='Org.Xml.Sax.ILocator'>New Type: Org.Xml.Sax.ILocator</h3>

```
public interface ILocator : IDisposable, Android.Runtime.IJavaObject {
	
	int ColumnNumber {
		get;
	}
	int LineNumber {
		get;
	}
	string PublicId {
		get;
	}
	string SystemId {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.IParser'>New Type: Org.Xml.Sax.IParser</h3>

```
public interface IParser : IDisposable, Android.Runtime.IJavaObject {
	
	void Parse (InputSource source);
	void Parse (string systemId);
	void SetDocumentHandler (IDocumentHandler handler);
	void SetDTDHandler (IDTDHandler handler);
	void SetEntityResolver (IEntityResolver resolver);
	void SetErrorHandler (IErrorHandler handler);
	void SetLocale (Java.Util.Locale locale);
}
```

<h3 id='Org.Xml.Sax.IParserExtensions'>New Type: Org.Xml.Sax.IParserExtensions</h3>

```
public static class IParserExtensions {
	
	public static System.Threading.Tasks.Task ParseAsync (IParser self, InputSource source);
	public static System.Threading.Tasks.Task ParseAsync (IParser self, string systemId);
}
```

<h3 id='Org.Xml.Sax.IXMLFilter'>New Type: Org.Xml.Sax.IXMLFilter</h3>

```
public interface IXMLFilter : IDisposable, Android.Runtime.IJavaObject, IXMLReader {
	
	IXMLReader Parent {
		get;
		set;
	}
}
```

<h3 id='Org.Xml.Sax.IXMLReader'>New Type: Org.Xml.Sax.IXMLReader</h3>

```
public interface IXMLReader : IDisposable, Android.Runtime.IJavaObject {
	
	bool GetFeature (string name);
	Java.Lang.Object GetProperty (string name);
	void Parse (InputSource input);
	void Parse (string systemId);
	void SetFeature (string name, bool value);
	void SetProperty (string name, Java.Lang.Object value);
	
	IContentHandler ContentHandler {
		get;
		set;
	}
	IDTDHandler DTDHandler {
		get;
		set;
	}
	IEntityResolver EntityResolver {
		get;
		set;
	}
	IErrorHandler ErrorHandler {
		get;
		set;
	}
}
```

<h3 id='Org.Xml.Sax.IXMLReaderExtensions'>New Type: Org.Xml.Sax.IXMLReaderExtensions</h3>

```
public static class IXMLReaderExtensions {
	
	public static System.Threading.Tasks.Task ParseAsync (IXMLReader self, InputSource input);
	public static System.Threading.Tasks.Task ParseAsync (IXMLReader self, string systemId);
}
```

<h3 id='Org.Xml.Sax.InputSource'>New Type: Org.Xml.Sax.InputSource</h3>

```
public class InputSource : Java.Lang.Object {
	
	protected InputSource (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public InputSource ();
	public InputSource (System.IO.Stream byteStream);
	public InputSource (Java.IO.Reader characterStream);
	public InputSource (string systemId);
	
	public virtual System.IO.Stream ByteStream {
		get;
		set;
	}
	public virtual Java.IO.Reader CharacterStream {
		get;
		set;
	}
	public virtual string Encoding {
		get;
		set;
	}
	public virtual string PublicId {
		get;
		set;
	}
	public virtual string SystemId {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.SAXException'>New Type: Org.Xml.Sax.SAXException</h3>

```
public class SAXException : Java.Lang.Exception {
	
	protected SAXException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SAXException ();
	public SAXException (Java.Lang.Exception e);
	public SAXException (string message);
	public SAXException (string message, Java.Lang.Exception e);
	
	public virtual Java.Lang.Exception Exception {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.SAXNotRecognizedException'>New Type: Org.Xml.Sax.SAXNotRecognizedException</h3>

```
public class SAXNotRecognizedException : SAXException {
	
	protected SAXNotRecognizedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SAXNotRecognizedException ();
	public SAXNotRecognizedException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.SAXNotSupportedException'>New Type: Org.Xml.Sax.SAXNotSupportedException</h3>

```
public class SAXNotSupportedException : SAXException {
	
	protected SAXNotSupportedException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SAXNotSupportedException ();
	public SAXNotSupportedException (string message);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.SAXParseException'>New Type: Org.Xml.Sax.SAXParseException</h3>

```
public class SAXParseException : SAXException {
	
	protected SAXParseException (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SAXParseException (string message, string publicId, string systemId, int lineNumber, int columnNumber);
	public SAXParseException (string message, string publicId, string systemId, int lineNumber, int columnNumber, Java.Lang.Exception e);
	public SAXParseException (string message, ILocator locator);
	public SAXParseException (string message, ILocator locator, Java.Lang.Exception e);
	
	public virtual int ColumnNumber {
		get;
	}
	public virtual int LineNumber {
		get;
	}
	public virtual string PublicId {
		get;
	}
	public virtual string SystemId {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.Xml.Sax.Ext'>Namespace: Org.Xml.Sax.Ext</h2>

<h3 id='Org.Xml.Sax.Ext.Attributes2Impl'>New Type: Org.Xml.Sax.Ext.Attributes2Impl</h3>

```
public class Attributes2Impl : Org.Xml.Sax.Helpers.AttributesImpl, IAttributes2 {
	
	protected Attributes2Impl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Attributes2Impl ();
	public Attributes2Impl (Org.Xml.Sax.IAttributes atts);
	
	public virtual bool IsDeclared (int index);
	public virtual bool IsDeclared (string qName);
	public virtual bool IsDeclared (string uri, string localName);
	public virtual bool IsSpecified (int index);
	public virtual bool IsSpecified (string qName);
	public virtual bool IsSpecified (string uri, string localName);
	public virtual void SetDeclared (int index, bool value);
	public virtual void SetSpecified (int index, bool value);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Ext.DefaultHandler2'>New Type: Org.Xml.Sax.Ext.DefaultHandler2</h3>

```
public class DefaultHandler2 : Org.Xml.Sax.Helpers.DefaultHandler, IDeclHandler, IEntityResolver2, ILexicalHandler {
	
	protected DefaultHandler2 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHandler2 ();
	
	public virtual void AttributeDecl (string eName, string aName, string type, string mode, string value);
	public virtual void Comment (char [] ch, int start, int length);
	public virtual void ElementDecl (string name, string model);
	public virtual void EndCDATA ();
	public virtual void EndDTD ();
	public virtual void EndEntity (string name);
	public virtual void ExternalEntityDecl (string name, string publicId, string systemId);
	public virtual Org.Xml.Sax.InputSource GetExternalSubset (string name, string baseURI);
	public virtual void InternalEntityDecl (string name, string value);
	public virtual Org.Xml.Sax.InputSource ResolveEntity (string name, string publicId, string baseURI, string systemId);
	public virtual void StartCDATA ();
	public virtual void StartDTD (string name, string publicId, string systemId);
	public virtual void StartEntity (string name);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Ext.IAttributes2'>New Type: Org.Xml.Sax.Ext.IAttributes2</h3>

```
public interface IAttributes2 : Org.Xml.Sax.IAttributes, IDisposable, Android.Runtime.IJavaObject {
	
	bool IsDeclared (int index);
	bool IsDeclared (string qName);
	bool IsDeclared (string uri, string localName);
	bool IsSpecified (int index);
	bool IsSpecified (string qName);
	bool IsSpecified (string uri, string localName);
}
```

<h3 id='Org.Xml.Sax.Ext.IDeclHandler'>New Type: Org.Xml.Sax.Ext.IDeclHandler</h3>

```
public interface IDeclHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void AttributeDecl (string eName, string aName, string type, string mode, string value);
	void ElementDecl (string name, string model);
	void ExternalEntityDecl (string name, string publicId, string systemId);
	void InternalEntityDecl (string name, string value);
}
```

<h3 id='Org.Xml.Sax.Ext.IEntityResolver2'>New Type: Org.Xml.Sax.Ext.IEntityResolver2</h3>

```
public interface IEntityResolver2 : IDisposable, Org.Xml.Sax.IEntityResolver, Android.Runtime.IJavaObject {
	
	Org.Xml.Sax.InputSource GetExternalSubset (string name, string baseURI);
	Org.Xml.Sax.InputSource ResolveEntity (string name, string publicId, string baseURI, string systemId);
}
```

<h3 id='Org.Xml.Sax.Ext.ILexicalHandler'>New Type: Org.Xml.Sax.Ext.ILexicalHandler</h3>

```
public interface ILexicalHandler : IDisposable, Android.Runtime.IJavaObject {
	
	void Comment (char [] ch, int start, int length);
	void EndCDATA ();
	void EndDTD ();
	void EndEntity (string name);
	void StartCDATA ();
	void StartDTD (string name, string publicId, string systemId);
	void StartEntity (string name);
}
```

<h3 id='Org.Xml.Sax.Ext.ILocator2'>New Type: Org.Xml.Sax.Ext.ILocator2</h3>

```
public interface ILocator2 : IDisposable, Android.Runtime.IJavaObject, Org.Xml.Sax.ILocator {
	
	string Encoding {
		get;
	}
	string XMLVersion {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Ext.Locator2Impl'>New Type: Org.Xml.Sax.Ext.Locator2Impl</h3>

```
public class Locator2Impl : Org.Xml.Sax.Helpers.LocatorImpl, ILocator2 {
	
	protected Locator2Impl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Locator2Impl ();
	public Locator2Impl (Org.Xml.Sax.ILocator locator);
	
	public virtual string Encoding {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual string XMLVersion {
		get;
		set;
	}
}
```

<h2 id='Org.Xml.Sax.Helpers'>Namespace: Org.Xml.Sax.Helpers</h2>

<h3 id='Org.Xml.Sax.Helpers.AttributeListImpl'>New Type: Org.Xml.Sax.Helpers.AttributeListImpl</h3>

```
public class AttributeListImpl : Java.Lang.Object, Org.Xml.Sax.IAttributeList {
	
	protected AttributeListImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AttributeListImpl ();
	public AttributeListImpl (Org.Xml.Sax.IAttributeList atts);
	
	public virtual void AddAttribute (string name, string type, string value);
	public virtual void Clear ();
	public virtual string GetName (int i);
	public virtual string GetType (int i);
	public virtual string GetType (string name);
	public virtual string GetValue (int i);
	public virtual string GetValue (string name);
	public virtual void RemoveAttribute (string name);
	public virtual void SetAttributeList (Org.Xml.Sax.IAttributeList atts);
	
	public virtual int Length {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Helpers.AttributesImpl'>New Type: Org.Xml.Sax.Helpers.AttributesImpl</h3>

```
public class AttributesImpl : Java.Lang.Object, Org.Xml.Sax.IAttributes {
	
	protected AttributesImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public AttributesImpl ();
	public AttributesImpl (Org.Xml.Sax.IAttributes atts);
	
	public virtual void AddAttribute (string uri, string localName, string qName, string type, string value);
	public virtual void Clear ();
	public virtual int GetIndex (string qName);
	public virtual int GetIndex (string uri, string localName);
	public virtual string GetLocalName (int index);
	public virtual string GetQName (int index);
	public virtual string GetType (int index);
	public virtual string GetType (string qName);
	public virtual string GetType (string uri, string localName);
	public virtual string GetURI (int index);
	public virtual string GetValue (int index);
	public virtual string GetValue (string qName);
	public virtual string GetValue (string uri, string localName);
	public virtual void RemoveAttribute (int index);
	public virtual void SetAttribute (int index, string uri, string localName, string qName, string type, string value);
	public virtual void SetAttributes (Org.Xml.Sax.IAttributes atts);
	public virtual void SetLocalName (int index, string localName);
	public virtual void SetQName (int index, string qName);
	public virtual void SetType (int index, string type);
	public virtual void SetURI (int index, string uri);
	public virtual void SetValue (int index, string value);
	
	public virtual int Length {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Helpers.DefaultHandler'>New Type: Org.Xml.Sax.Helpers.DefaultHandler</h3>

```
public class DefaultHandler : Java.Lang.Object, Org.Xml.Sax.IContentHandler, Org.Xml.Sax.IDTDHandler, Org.Xml.Sax.IEntityResolver, Org.Xml.Sax.IErrorHandler {
	
	protected DefaultHandler (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DefaultHandler ();
	
	public virtual void Characters (char [] ch, int start, int length);
	public virtual void EndDocument ();
	public virtual void EndElement (string uri, string localName, string qName);
	public virtual void EndPrefixMapping (string prefix);
	public virtual void Error (Org.Xml.Sax.SAXParseException e);
	public virtual void FatalError (Org.Xml.Sax.SAXParseException e);
	public virtual void IgnorableWhitespace (char [] ch, int start, int length);
	public virtual void NotationDecl (string name, string publicId, string systemId);
	public virtual void ProcessingInstruction (string target, string data);
	public virtual Org.Xml.Sax.InputSource ResolveEntity (string publicId, string systemId);
	public virtual void SetDocumentLocator (Org.Xml.Sax.ILocator locator);
	public virtual void SkippedEntity (string name);
	public virtual void StartDocument ();
	public virtual void StartElement (string uri, string localName, string qName, Org.Xml.Sax.IAttributes attributes);
	public virtual void StartPrefixMapping (string prefix, string uri);
	public virtual void UnparsedEntityDecl (string name, string publicId, string systemId, string notationName);
	public virtual void Warning (Org.Xml.Sax.SAXParseException e);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Helpers.LocatorImpl'>New Type: Org.Xml.Sax.Helpers.LocatorImpl</h3>

```
public class LocatorImpl : Java.Lang.Object, Org.Xml.Sax.ILocator {
	
	protected LocatorImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public LocatorImpl ();
	public LocatorImpl (Org.Xml.Sax.ILocator locator);
	
	public virtual int ColumnNumber {
		get;
		set;
	}
	public virtual int LineNumber {
		get;
		set;
	}
	public virtual string PublicId {
		get;
		set;
	}
	public virtual string SystemId {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Helpers.NamespaceSupport'>New Type: Org.Xml.Sax.Helpers.NamespaceSupport</h3>

```
public class NamespaceSupport : Java.Lang.Object {
	
	protected NamespaceSupport (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public NamespaceSupport ();
	
	public virtual bool DeclarePrefix (string prefix, string uri);
	public virtual string GetPrefix (string uri);
	public virtual Java.Util.IEnumeration GetPrefixes (string uri);
	public virtual string GetURI (string prefix);
	public virtual void PopContext ();
	public virtual string [] ProcessName (string qName, string [] parts, bool isAttribute);
	public virtual void PushContext ();
	public virtual void Reset ();
	
	public virtual Java.Util.IEnumeration DeclaredPrefixes {
		get;
	}
	public virtual bool NamespaceDeclUris {
		get;
		set;
	}
	public virtual Java.Util.IEnumeration Prefixes {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const string Nsdecl = "http://www.w3.org/xmlns/2000/";
	public const string Xmlns = "http://www.w3.org/XML/1998/namespace";
}
```

<h3 id='Org.Xml.Sax.Helpers.ParserAdapter'>New Type: Org.Xml.Sax.Helpers.ParserAdapter</h3>

```
public class ParserAdapter : Java.Lang.Object, Org.Xml.Sax.IDocumentHandler, Org.Xml.Sax.IXMLReader {
	
	protected ParserAdapter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ParserAdapter ();
	public ParserAdapter (Org.Xml.Sax.IParser parser);
	
	public virtual void Characters (char [] ch, int start, int length);
	public virtual void EndDocument ();
	public virtual void EndElement (string qName);
	public virtual bool GetFeature (string name);
	public virtual Java.Lang.Object GetProperty (string name);
	public virtual void IgnorableWhitespace (char [] ch, int start, int length);
	public virtual void Parse (Org.Xml.Sax.InputSource input);
	public virtual void Parse (string systemId);
	public virtual void ProcessingInstruction (string target, string data);
	public virtual void SetDocumentLocator (Org.Xml.Sax.ILocator locator);
	public virtual void SetFeature (string name, bool value);
	public virtual void SetProperty (string name, Java.Lang.Object value);
	public virtual void StartDocument ();
	public virtual void StartElement (string qName, Org.Xml.Sax.IAttributeList qAtts);
	
	public virtual Org.Xml.Sax.IContentHandler ContentHandler {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IDTDHandler DTDHandler {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IEntityResolver EntityResolver {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IErrorHandler ErrorHandler {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Helpers.ParserFactory'>New Type: Org.Xml.Sax.Helpers.ParserFactory</h3>

```
public class ParserFactory : Java.Lang.Object {
	
	protected ParserFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static Org.Xml.Sax.IParser MakeParser ();
	public static Org.Xml.Sax.IParser MakeParser (string className);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Helpers.XMLFilterImpl'>New Type: Org.Xml.Sax.Helpers.XMLFilterImpl</h3>

```
public class XMLFilterImpl : Java.Lang.Object, Org.Xml.Sax.IContentHandler, Org.Xml.Sax.IDTDHandler, Org.Xml.Sax.IEntityResolver, Org.Xml.Sax.IErrorHandler, Org.Xml.Sax.IXMLFilter, Org.Xml.Sax.IXMLReader {
	
	protected XMLFilterImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public XMLFilterImpl ();
	public XMLFilterImpl (Org.Xml.Sax.IXMLReader parent);
	
	public virtual void Characters (char [] ch, int start, int length);
	public virtual void EndDocument ();
	public virtual void EndElement (string uri, string localName, string qName);
	public virtual void EndPrefixMapping (string prefix);
	public virtual void Error (Org.Xml.Sax.SAXParseException e);
	public virtual void FatalError (Org.Xml.Sax.SAXParseException e);
	public virtual bool GetFeature (string name);
	public virtual Java.Lang.Object GetProperty (string name);
	public virtual void IgnorableWhitespace (char [] ch, int start, int length);
	public virtual void NotationDecl (string name, string publicId, string systemId);
	public virtual void Parse (Org.Xml.Sax.InputSource input);
	public virtual void Parse (string systemId);
	public virtual void ProcessingInstruction (string target, string data);
	public virtual Org.Xml.Sax.InputSource ResolveEntity (string publicId, string systemId);
	public virtual void SetDocumentLocator (Org.Xml.Sax.ILocator locator);
	public virtual void SetFeature (string name, bool value);
	public virtual void SetProperty (string name, Java.Lang.Object value);
	public virtual void SkippedEntity (string name);
	public virtual void StartDocument ();
	public virtual void StartElement (string uri, string localName, string qName, Org.Xml.Sax.IAttributes atts);
	public virtual void StartPrefixMapping (string prefix, string uri);
	public virtual void UnparsedEntityDecl (string name, string publicId, string systemId, string notationName);
	public virtual void Warning (Org.Xml.Sax.SAXParseException e);
	
	public virtual Org.Xml.Sax.IContentHandler ContentHandler {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IDTDHandler DTDHandler {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IEntityResolver EntityResolver {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IErrorHandler ErrorHandler {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IXMLReader Parent {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Helpers.XMLReaderAdapter'>New Type: Org.Xml.Sax.Helpers.XMLReaderAdapter</h3>

```
public class XMLReaderAdapter : Java.Lang.Object, Org.Xml.Sax.IContentHandler, Org.Xml.Sax.IParser {
	
	protected XMLReaderAdapter (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public XMLReaderAdapter ();
	public XMLReaderAdapter (Org.Xml.Sax.IXMLReader xmlReader);
	
	public virtual void Characters (char [] ch, int start, int length);
	public virtual void EndDocument ();
	public virtual void EndElement (string uri, string localName, string qName);
	public virtual void EndPrefixMapping (string prefix);
	public virtual void IgnorableWhitespace (char [] ch, int start, int length);
	public virtual void Parse (Org.Xml.Sax.InputSource input);
	public virtual void Parse (string systemId);
	public virtual void ProcessingInstruction (string target, string data);
	public virtual void SetDocumentHandler (Org.Xml.Sax.IDocumentHandler handler);
	public virtual void SetDocumentLocator (Org.Xml.Sax.ILocator locator);
	public virtual void SetDTDHandler (Org.Xml.Sax.IDTDHandler handler);
	public virtual void SetEntityResolver (Org.Xml.Sax.IEntityResolver resolver);
	public virtual void SetErrorHandler (Org.Xml.Sax.IErrorHandler handler);
	public virtual void SetLocale (Java.Util.Locale locale);
	public virtual void SkippedEntity (string name);
	public virtual void StartDocument ();
	public virtual void StartElement (string uri, string localName, string qName, Org.Xml.Sax.IAttributes atts);
	public virtual void StartPrefixMapping (string prefix, string uri);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h3 id='Org.Xml.Sax.Helpers.XMLReaderFactory'>New Type: Org.Xml.Sax.Helpers.XMLReaderFactory</h3>

```
public sealed class XMLReaderFactory : Java.Lang.Object {
	
	public static Org.Xml.Sax.IXMLReader CreateXMLReader ();
	public static Org.Xml.Sax.IXMLReader CreateXMLReader (string className);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
}
```

<h2 id='Org.XmlPull.V1'>Namespace: Org.XmlPull.V1</h2>

<h3 id='Org.XmlPull.V1.IXmlPullParserExtensions'>New Type: Org.XmlPull.V1.IXmlPullParserExtensions</h3>

```
public static class IXmlPullParserExtensions {
	
	public static System.Threading.Tasks.Task NextAsync (IXmlPullParser self);
	public static System.Threading.Tasks.Task NextTagAsync (IXmlPullParser self);
	public static System.Threading.Tasks.Task NextTextAsync (IXmlPullParser self);
	public static System.Threading.Tasks.Task NextTokenAsync (IXmlPullParser self);
}
```

<h3 id='Org.XmlPull.V1.IXmlSerializer'>New Type: Org.XmlPull.V1.IXmlSerializer</h3>

```
public interface IXmlSerializer : IDisposable, Android.Runtime.IJavaObject {
	
	IXmlSerializer Attribute (string namespace, string name, string value);
	void Cdsect (string text);
	void Comment (string text);
	void Docdecl (string text);
	void EndDocument ();
	IXmlSerializer EndTag (string namespace, string name);
	void EntityRef (string text);
	void Flush ();
	bool GetFeature (string name);
	string GetPrefix (string namespace, bool generatePrefix);
	Java.Lang.Object GetProperty (string name);
	void IgnorableWhitespace (string text);
	void ProcessingInstruction (string text);
	void SetFeature (string name, bool state);
	void SetOutput (System.IO.Stream os, string encoding);
	void SetOutput (Java.IO.Writer writer);
	void SetPrefix (string prefix, string namespace);
	void SetProperty (string name, Java.Lang.Object value);
	void StartDocument (string encoding, Java.Lang.Boolean standalone);
	IXmlSerializer StartTag (string namespace, string name);
	IXmlSerializer Text (char [] buf, int start, int len);
	IXmlSerializer Text (string text);
	
	int Depth {
		get;
	}
	string Name {
		get;
	}
	string Namespace {
		get;
	}
}
```

<h3 id='Org.XmlPull.V1.IXmlSerializerExtensions'>New Type: Org.XmlPull.V1.IXmlSerializerExtensions</h3>

```
public static class IXmlSerializerExtensions {
	
	public static System.Threading.Tasks.Task AttributeAsync (IXmlSerializer self, string namespace, string name, string value);
	public static System.Threading.Tasks.Task CdsectAsync (IXmlSerializer self, string text);
	public static System.Threading.Tasks.Task CommentAsync (IXmlSerializer self, string text);
	public static System.Threading.Tasks.Task DocdeclAsync (IXmlSerializer self, string text);
	public static System.Threading.Tasks.Task EndDocumentAsync (IXmlSerializer self);
	public static System.Threading.Tasks.Task EndTagAsync (IXmlSerializer self, string namespace, string name);
	public static System.Threading.Tasks.Task EntityRefAsync (IXmlSerializer self, string text);
	public static System.Threading.Tasks.Task FlushAsync (IXmlSerializer self);
	public static System.Threading.Tasks.Task IgnorableWhitespaceAsync (IXmlSerializer self, string text);
	public static System.Threading.Tasks.Task ProcessingInstructionAsync (IXmlSerializer self, string text);
	public static System.Threading.Tasks.Task StartDocumentAsync (IXmlSerializer self, string encoding, Java.Lang.Boolean standalone);
	public static System.Threading.Tasks.Task StartTagAsync (IXmlSerializer self, string namespace, string name);
	public static System.Threading.Tasks.Task TextAsync (IXmlSerializer self, char [] buf, int start, int len);
	public static System.Threading.Tasks.Task TextAsync (IXmlSerializer self, string text);
}
```

<h3 id='Org.XmlPull.V1.XmlPullParserFactory'>New Type: Org.XmlPull.V1.XmlPullParserFactory</h3>

```
public class XmlPullParserFactory : Java.Lang.Object {
	
	protected XmlPullParserFactory (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected XmlPullParserFactory ();
	
	public static XmlPullParserFactory NewInstance ();
	public static XmlPullParserFactory NewInstance (string classNames, Java.Lang.Class context);
	public virtual bool GetFeature (string name);
	public virtual System.Xml.XmlReader NewPullParser ();
	public virtual IXmlSerializer NewSerializer ();
	public virtual void SetFeature (string name, bool state);
	
	protected string ClassNamesLocation {
		get;
		set;
	}
	protected System.Collections.IDictionary Features {
		get;
		set;
	}
	public virtual bool NamespaceAware {
		get;
		set;
	}
	protected System.Collections.IList ParserClasses {
		get;
		set;
	}
	protected System.Collections.IList SerializerClasses {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual bool Validating {
		get;
		set;
	}
	
	public const string PropertyName = "org.xmlpull.v1.XmlPullParserFactory";
}
```

<h2 id='Org.Xmlpull.V1.Sax2'>Namespace: Org.Xmlpull.V1.Sax2</h2>

<h3 id='Org.Xmlpull.V1.Sax2.Driver'>New Type: Org.Xmlpull.V1.Sax2.Driver</h3>

```
public class Driver : Java.Lang.Object, Org.Xml.Sax.IAttributes, Org.Xml.Sax.ILocator, Org.Xml.Sax.IXMLReader {
	
	protected Driver (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public Driver ();
	public Driver (System.Xml.XmlReader pp);
	
	public virtual bool GetFeature (string name);
	public virtual int GetIndex (string qName);
	public virtual int GetIndex (string uri, string localName);
	public virtual string GetLocalName (int index);
	public virtual Java.Lang.Object GetProperty (string name);
	public virtual string GetQName (int index);
	public virtual string GetType (int index);
	public virtual string GetType (string qName);
	public virtual string GetType (string uri, string localName);
	public virtual string GetURI (int index);
	public virtual string GetValue (int index);
	public virtual string GetValue (string qName);
	public virtual string GetValue (string uri, string localName);
	public virtual void Parse (Org.Xml.Sax.InputSource source);
	public virtual void Parse (string systemId);
	public System.Threading.Tasks.Task ParseAsync (Org.Xml.Sax.InputSource source);
	public System.Threading.Tasks.Task ParseAsync (string systemId);
	public virtual void ParseSubTree (System.Xml.XmlReader pp);
	public System.Threading.Tasks.Task ParseSubTreeAsync (System.Xml.XmlReader pp);
	public virtual void SetFeature (string name, bool value);
	public virtual void SetProperty (string name, Java.Lang.Object value);
	protected virtual void StartElement (string namespace, string localName, string qName);
	
	public virtual int ColumnNumber {
		get;
	}
	public virtual Org.Xml.Sax.IContentHandler ContentHandler {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IDTDHandler DTDHandler {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IEntityResolver EntityResolver {
		get;
		set;
	}
	public virtual Org.Xml.Sax.IErrorHandler ErrorHandler {
		get;
		set;
	}
	public virtual int Length {
		get;
	}
	public virtual int LineNumber {
		get;
	}
	protected System.Xml.XmlReader Pp {
		get;
		set;
	}
	public virtual string PublicId {
		get;
	}
	public virtual string SystemId {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	protected const string ApacheDynamicValidationFeature = "http://apache.org/xml/features/validation/dynamic";
	protected const string ApacheSchemaValidationFeature = "http://apache.org/xml/features/validation/schema";
	protected const string DeclarationHandlerProperty = "http://xml.org/sax/properties/declaration-handler";
	protected const string LexicalHandlerProperty = "http://xml.org/sax/properties/lexical-handler";
	protected const string NamespacePrefixesFeature = "http://xml.org/sax/features/namespace-prefixes";
	protected const string NamespacesFeature = "http://xml.org/sax/features/namespaces";
	protected const string ValidationFeature = "http://xml.org/sax/features/validation";
}
```
