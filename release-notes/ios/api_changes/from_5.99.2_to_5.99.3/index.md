---
id: FED6606C-36B5-4941-B81F-53C0EEF7E56E
title: "From 5.99.2 to 5.99.3"
---

<html><head><title>Comparison between MonoTouch 5.99.2 and 5.99.3</title><link href="prettify.css" type="text/css" rel="stylesheet">
<style type="text/css">
body {
color: #333;
  min-width: 80em;
  max-width: 120em;
}

.release-notes {
}

.release-notes p {
margin-left: 1em;
margin-right: 1em;
}
pre {
background-color: #eee;
padding-top: .5em;
padding-bottom: .5em;
margin-left: 1em;
margin-right: 1em;
overflow: auto;
}

p {
    max-width: 40em;
}
</style>
<script type="text/javascript" src="prettify.js">
</script>
</head>

<body onload="prettyPrint()">

<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "5.99.2";
</pre>
<p>Added:</p><pre>
 	public const string Version = "5.99.3";
 	public const string AddressBookUILibrary = "/System/Library/Frameworks/AddressBookUI.framework/AddressBookUI";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVAsset</h3>
<p>Added:</p><pre>
 	public virtual AVAssetResourceLoader ResourceLoader {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput</h3>
<p>Added:</p><pre>
 	public static AVAssetWriterInput Create (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioPlayerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void EndInterruption (AVAudioPlayer player);
 	public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS6")]
	public virtual void EndInterruption (AVAudioPlayer player);
 	[Obsolete("Deprecated in iOS6")]
	public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureOutput</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject[] Connections {
</pre>
<p>Added:</p><pre>
 	public virtual AVCaptureConnection[] Connections {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVFileType</h3>
<p>Removed:</p><pre>
 public class AVFileType {
 	
 	public AVFileType ();
</pre>
<p>Added:</p><pre>
 public static class AVFileType {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMediaCharacteristic</h3>
<p>Removed:</p><pre>
 public class AVMediaCharacteristic {
 	
 	public AVMediaCharacteristic ();
</pre>
<p>Added:</p><pre>
 public static class AVMediaCharacteristic {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMediaType</h3>
<p>Removed:</p><pre>
 public class AVMediaType {
 	
 	public AVMediaType ();
</pre>
<p>Added:</p><pre>
 public static class AVMediaType {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMetadata</h3>
<p>Removed:</p><pre>
 public class AVMetadata {
 	
 	public AVMetadata ();
</pre>
<p>Added:</p><pre>
 public static class AVMetadata {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVUrlAsset</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString ReferenceRestrictionsKey {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideo</h3>
<p>Removed:</p><pre>
 public class AVVideo {
 	
 	public AVVideo ();
</pre>
<p>Added:</p><pre>
 public static class AVVideo {
</pre>
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>Type Changed: MonoTouch.Accounts.ACFacebook</h3>
<p>Removed:</p><pre>
 public class ACFacebook {
 	
 	public ACFacebook ();
 	public static MonoTouch.Foundation.NSString AudienceEveryone {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AudienceFriends {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AudienceOnlyMe {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 public static class ACFacebook {
</pre>
<h3>New Type: MonoTouch.Accounts.ACFacebookAudience</h3>
<pre>
public static class ACFacebookAudience {
	
	public static MonoTouch.Foundation.NSString Everyone {
		get;
	}
	public static MonoTouch.Foundation.NSString Friends {
		get;
	}
	public static MonoTouch.Foundation.NSString OnlyMe {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.AddressBook</h2>
<h3>Type Changed: MonoTouch.AddressBook.ABAddressBook</h3>
<p>Removed:</p><pre>
 	public ABAddressBook ();
 	public static ABAddressBook FromOptions (MonoTouch.Foundation.NSDictionary dictionary, out MonoTouch.Foundation.NSError outError);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use static Create method in iOS 6.0")]
	public ABAddressBook ();
 	public static ABAddressBook Create (out MonoTouch.Foundation.NSError error);
 	public ABGroup[] GetGroups (ABRecord source);
 	public ABPerson[] GetPeople (ABRecord source);
 	public ABPerson[] GetPeople (ABRecord source, ABPersonSortBy sortOrdering);
</pre>
<h3>Type Changed: MonoTouch.AddressBook.ABGroup</h3>
<p>Added:</p><pre>
 	public ABGroup (ABRecord source);
 	public ABRecord Source {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AddressBook.ABPerson</h3>
<p>Removed:</p><pre>
 	public ABMultiValue`1 GetAddresses ();
 	public ABMultiValue`1 GetInstantMessages ();
 	public ABMultiValue`1 GetSocialProfile ();
</pre>
<p>Added:</p><pre>
 	public ABPerson (ABRecord source);
 	public static ABPerson[] CreateFromVCard (ABRecord source, MonoTouch.Foundation.NSData vCardData);
 	public static MonoTouch.Foundation.NSData GetVCards (params ABPerson[] people);
 	[Obsolete("Use GetAllAddresses")]
	public ABMultiValue`1 GetAddresses ();
 	public ABMultiValue`1 GetAllAddresses ();
 	public MonoTouch.Foundation.NSData GetImage (ABPersonImageFormat format);
 	[Obsolete("Use GetInstantMessageServices")]
	public ABMultiValue`1 GetInstantMessages ();
 	public ABMultiValue`1 GetInstantMessageServices ();
 	public ABPerson[] GetLinkedPeople ();
 	[Obsolete("Use GetSocialProfiles")]
	public ABMultiValue`1 GetSocialProfile ();
 	public ABMultiValue`1 GetSocialProfiles ();
 	public void SetAddresses (ABMultiValue`1 addresses);
 	public void SetInstantMessages (ABMultiValue`1 services);
 	public void SetSocialProfile (ABMultiValue`1 profiles);
 	public ABRecord Source {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AddressBook.ABPersonInstantMessageService</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString Facebook {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GaduGadu {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GoogleTalk {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString QQ {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Skype {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AddressBook.ABPersonPhoneLabel</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString OtherFax {
 		get;
 	}
</pre>
<h3>Type Removed: MonoTouch.AddressBook.ABPersonSocialProfile</h3>
<h3>New Type: MonoTouch.AddressBook.ABPersonSocialProfileService</h3>
<pre>
public static class ABPersonSocialProfileService {
	
	public static readonly MonoTouch.Foundation.NSString Twitter;
	public static readonly MonoTouch.Foundation.NSString GameCenter;
	public static readonly MonoTouch.Foundation.NSString Facebook;
	public static readonly MonoTouch.Foundation.NSString Myspace;
	public static readonly MonoTouch.Foundation.NSString LinkedIn;
	public static readonly MonoTouch.Foundation.NSString Flickr;
	public static readonly MonoTouch.Foundation.NSString SinaWeibo;
}
</pre>
<h3>Type Changed: MonoTouch.AddressBook.ABPropertyType</h3>
<p>Removed:</p><pre>
 public enum ABPropertyType : ushort {
</pre>
<p>Added:</p><pre>
 public enum ABPropertyType : uint {
</pre>
<h3>Type Changed: MonoTouch.AddressBook.ABSource</h3>
<p>Removed:</p><pre>
 	public const int SearchableMask = 16777216;
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use ABSourceType.SearchableMask")]
	public const int SearchableMask = 16777216;
</pre>
<h3>Type Changed: MonoTouch.AddressBook.ABSourceType</h3>
<p>Added:</p><pre>
 	SearchableMask
</pre>
<h3>New Type: MonoTouch.AddressBook.DictionaryContainer</h3>
<pre>
public abstract class DictionaryContainer {
	
	protected DictionaryContainer ();
	protected DictionaryContainer (MonoTouch.Foundation.NSDictionary dictionary);
	
	protected string GetStringValue (MonoTouch.Foundation.NSString key);
	protected void SetStringValue (MonoTouch.Foundation.NSString key, MonoTouch.Foundation.NSString value);
	protected void SetStringValue (MonoTouch.Foundation.NSString key, string value);
	
	public MonoTouch.Foundation.NSDictionary Dictionary {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.AddressBook.InstantMessageService</h3>
<pre>
public class InstantMessageService : DictionaryContainer {
	
	public InstantMessageService ();
	public InstantMessageService (MonoTouch.Foundation.NSDictionary dictionary);
	
	public MonoTouch.Foundation.NSString Service {
		set;
	}
	public string ServiceName {
		get;
		set;
	}
	public string Username {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.AddressBook.PersonAddress</h3>
<pre>
public class PersonAddress : DictionaryContainer {
	
	public PersonAddress ();
	public PersonAddress (MonoTouch.Foundation.NSDictionary dictionary);
	
	public string City {
		get;
		set;
	}
	public string Country {
		get;
		set;
	}
	public string CountryCode {
		get;
		set;
	}
	public string State {
		get;
		set;
	}
	public string Street {
		get;
		set;
	}
	public string Zip {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.AddressBook.SocialProfile</h3>
<pre>
public class SocialProfile : DictionaryContainer {
	
	public SocialProfile ();
	public SocialProfile (MonoTouch.Foundation.NSDictionary dictionary);
	
	public MonoTouch.Foundation.NSString Service {
		set;
	}
	public string ServiceName {
		get;
		set;
	}
	public string Url {
		get;
		set;
	}
	public string UserIdentifier {
		get;
		set;
	}
	public string Username {
		get;
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.AddressBookUI</h2>
<h3>New Type: MonoTouch.AddressBookUI.ABAddressFormatting</h3>
<pre>
public static class ABAddressFormatting {
	
	public static string ToString (MonoTouch.Foundation.NSDictionary address, bool addCountryName);
}
</pre>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioQueue</h3>
<p>Removed:</p><pre>
 	public AudioStreamPacketDescription AudioStreamPacketDescription {
</pre>
<p>Added:</p><pre>
 	public AudioQueueStatus EnqueueBuffer (AudioQueueBuffer* audioQueueBuffer, int bytes, AudioStreamPacketDescription[] desc, int trimFramesAtStart, int trimFramesAtEnd, AudioQueueParameterEvent[] parameterEvents, ref AudioTimeStamp startTime, out AudioTimeStamp actualStartTime);
 	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, int bytes, AudioStreamPacketDescription[] desc, int trimFramesAtStart, int trimFramesAtEnd, AudioQueueParameterEvent[] parameterEvents, ref AudioTimeStamp startTime, out AudioTimeStamp actualStartTime);
 	public AudioStreamBasicDescription AudioStreamPacketDescription {
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBAdvertisement</h3>
<p>Removed:</p><pre>
 public class CBAdvertisement {
 	
 	public CBAdvertisement ();
</pre>
<p>Added:</p><pre>
 public static class CBAdvertisement {
</pre>
<h2>Namespace: MonoTouch.CoreFoundation</h2>
<h3>New Type: MonoTouch.CoreFoundation.CFIndex</h3>
<pre>
public struct CFIndex {
	
	public static implicit operator int (CFIndex index);
	public static implicit operator CFIndex (int value);
	public static implicit operator long (CFIndex index);
}
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFReadStream</h3>
<pre>
public class CFReadStream : CFStream {
	
	public CFReadStream (IntPtr handle);
	
	protected override void DoClose ();
	protected override IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
	protected override CFStreamStatus DoGetStatus ();
	protected override bool DoOpen ();
	protected override bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
	protected override bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
	public override CFException GetError ();
	public bool HasBytesAvailable ();
	public int Read (byte [] buffer);
	public int Read (byte [] buffer, int offset, int count);
	protected override void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	protected override void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
}
</pre>
<h3>Type Changed: MonoTouch.CoreFoundation.CFRunLoop</h3>
<p>Added:</p><pre>
 	public void AddSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
 	public bool ContainsSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
 	public bool RemoveSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFRunLoopSource</h3>
<pre>
public class CFRunLoopSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public void Dispose ();
	public virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public void Invalidate ();
	public void Signal ();
	
	public IntPtr Handle {
		get;
	}
	public bool IsValid {
		get;
	}
	public int Order {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFRunLoopSourceCustom</h3>
<pre>
public abstract class CFRunLoopSourceCustom : CFRunLoopSource {
	
	protected CFRunLoopSourceCustom ();
	
	public override void Dispose (bool disposing);
	protected abstract void OnCancel (CFRunLoop loop, string mode);
	protected abstract void OnPerform ();
	protected abstract void OnSchedule (CFRunLoop loop, string mode);
}
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFSocket</h3>
<pre>
public class CFSocket : CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public CFSocket ();
	public CFSocket (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto);
	public CFSocket (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, CFRunLoop loop);
	
	public static CFSocket CreateConnectedToSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, double timeout);
	public void Connect (System.Net.IPAddress address, int port, double timeout);
	public void Connect (System.Net.IPEndPoint endpoint, double timeout);
	public void DisableCallBacks (CFSocketCallBackType types);
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void EnableCallBacks (CFSocketCallBackType types);
	protected override void Finalize ();
	public CFSocketFlags GetSocketFlags ();
	public void SendData (byte [] data, double timeout);
	public void SetAddress (System.Net.IPAddress address, int port);
	public void SetAddress (System.Net.IPEndPoint endpoint);
	public void SetSocketFlags (CFSocketFlags flags);
	
	public IntPtr Handle {
		get;
	}
	
	public event EventHandler<cfsocketaccepteventargs> AcceptEvent;
	public event EventHandler<cfsocketconnecteventargs> ConnectEvent;
	
	public class CFSocketAcceptEventArgs : EventArgs {
		
		public CFSocketAcceptEventArgs (CFSocketNativeHandle handle, System.Net.IPEndPoint remote);
		
		public CFSocket CreateSocket ();
		public override string ToString ();
		
		public System.Net.IPEndPoint RemoteEndPoint {
			get;
		}
	}
	public class CFSocketConnectEventArgs : EventArgs {
		
		public CFSocketConnectEventArgs (CFSocketError result);
		
		public override string ToString ();
		
		public CFSocketError Result {
			get;
		}
	}
}
</cfsocketconnecteventargs></cfsocketaccepteventargs></pre>
<h3>New Type: MonoTouch.CoreFoundation.CFSocketCallBackType</h3>
<pre>
[Serializable]
[Flags]
public enum CFSocketCallBackType {
	NoCallBack,
	ReadCallBack,
	AcceptCallBack,
	DataCallBack,
	ConnectCallBack,
	WriteCallBack
}
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFSocketError</h3>
<pre>
[Serializable]
public enum CFSocketError {
	Success,
	Error,
	Timeout
}
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFSocketException</h3>
<pre>
public class CFSocketException : Exception {
	
	public CFSocketException (CFSocketError error);
	
	public CFSocketError Error {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFSocketFlags</h3>
<pre>
[Serializable]
[Flags]
public enum CFSocketFlags {
	AutomaticallyReenableReadCallBack,
	AutomaticallyReenableAcceptCallBack,
	AutomaticallyReenableDataCallBack,
	AutomaticallyReenableWriteCallBack,
	LeaveErrors,
	CloseOnInvalidate
}
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFSocketNativeHandle</h3>
<pre>
public struct CFSocketNativeHandle {
	
	public override string ToString ();
}
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFStream</h3>
<pre>
public abstract class CFStream : CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	protected CFStream (IntPtr handle);
	
	public static void CreateBoundPair (out CFReadStream readStream, out CFWriteStream writeStream, int bufferSize);
	public static MonoTouch.CoreServices.CFHTTPStream CreateForHTTPRequest (MonoTouch.CoreServices.CFHTTPMessage request);
	public static MonoTouch.CoreServices.CFHTTPStream CreateForStreamedHTTPRequest (MonoTouch.CoreServices.CFHTTPMessage request, CFReadStream body);
	public static void CreatePairWithPeerSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, out CFReadStream readStream, out CFWriteStream writeStream);
	public static void CreatePairWithSocket (CFSocket socket, out CFReadStream readStream, out CFWriteStream writeStream);
	public static void CreatePairWithSocketToHost (System.Net.IPEndPoint endpoint, out CFReadStream readStream, out CFWriteStream writeStream);
	protected void CheckError ();
	protected void CheckHandle ();
	public void Close ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected abstract void DoClose ();
	protected abstract IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
	protected abstract CFStreamStatus DoGetStatus ();
	protected abstract bool DoOpen ();
	protected abstract bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
	protected abstract bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
	public void EnableEvents (CFRunLoop runLoop, MonoTouch.Foundation.NSString runLoopMode);
	protected override void Finalize ();
	public abstract CFException GetError ();
	public CFStreamStatus GetStatus ();
	protected virtual void OnCallback (CFStreamEventType type);
	protected virtual void OnCanAcceptBytesEvent (StreamEventArgs args);
	protected virtual void OnClosedEvent (StreamEventArgs args);
	protected virtual void OnErrorEvent (StreamEventArgs args);
	protected virtual void OnHasBytesAvailableEvent (StreamEventArgs args);
	protected virtual void OnOpenCompleted (StreamEventArgs args);
	public void Open ();
	protected abstract void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	protected abstract void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	
	public IntPtr Handle {
		get;
	}
	
	public event EventHandler<streameventargs> CanAcceptBytesEvent;
	public event EventHandler<streameventargs> ClosedEvent;
	public event EventHandler<streameventargs> ErrorEvent;
	public event EventHandler<streameventargs> HasBytesAvailableEvent;
	public event EventHandler<streameventargs> OpenCompletedEvent;
	
	[Serializable]
	protected delegate void CFStreamCallback (IntPtr s, CFStreamEventType type, IntPtr info);
	public class StreamEventArgs : EventArgs {
		
		public StreamEventArgs (CFStreamEventType type);
		
		public override string ToString ();
		
		public CFStreamEventType EventType {
			get;
		}
	}
}
</streameventargs></streameventargs></streameventargs></streameventargs></streameventargs></pre>
<h3>New Type: MonoTouch.CoreFoundation.CFStreamStatus</h3>
<pre>
[Serializable]
public enum CFStreamStatus {
	NotOpen,
	Opening,
	Open,
	Reading,
	Writing,
	AtEnd,
	Closed,
	Error
}
</pre>
<h3>Type Changed: MonoTouch.CoreFoundation.CFUrl</h3>
<p>Removed:</p><pre>
 public class CFUrl : IDisposable {
</pre>
<p>Added:</p><pre>
 public class CFUrl : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
 	public static int GetTypeID ();
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFWriteStream</h3>
<pre>
public class CFWriteStream : CFStream {
	
	public bool CanAcceptBytes ();
	protected override void DoClose ();
	protected override IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
	protected override CFStreamStatus DoGetStatus ();
	protected override bool DoOpen ();
	protected override bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
	protected override bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
	public override CFException GetError ();
	protected override void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	protected override void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	public int Write (byte [] buffer);
	public int Write (byte [] buffer, int offset, int count);
}
</pre>
<h2>Namespace: MonoTouch.CoreImage</h2>
<h3>Type Changed: MonoTouch.CoreImage.CIContext</h3>
<p>Removed:</p><pre>
 	public static CIContext FromContext (MonoTouch.CoreGraphics.CGContext ctx);
 	public static CIContext FromContext (MonoTouch.CoreGraphics.CGContext ctx, CIContextOptions options);
 	public MonoTouch.CoreGraphics.CGLayer CreateCGLayer (System.Drawing.SizeF size);
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIFilterInputKey</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString Versionkey {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString Version {
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIImage</h3>
<p>Removed:</p><pre>
 	public CIImage (MonoTouch.Foundation.NSData d, int bpr, System.Drawing.SizeF size, int f, MonoTouch.CoreGraphics.CGColorSpace c);
 	public CIImage (int glTextureName, System.Drawing.SizeF size, bool flipped, MonoTouch.CoreGraphics.CGColorSpace cs);
</pre>
<p>Added:</p><pre>
 	public CIImage (MonoTouch.Foundation.NSData d, int bpr, System.Drawing.SizeF size, int f, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
 	public CIImage (int glTextureName, System.Drawing.SizeF size, bool flipped, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
</pre>
<h2>Namespace: MonoTouch.CoreLocation</h2>
<h3>Type Changed: MonoTouch.CoreLocation.CLError</h3>
<p>Added:</p><pre>
 	RegionMonitoringResponseDelayed,
 	GeocodeFoundNoResult,
 	GeocodeFoundPartialResult,
 	GeocodeCanceled
</pre>
<h2>Namespace: MonoTouch.CoreServices</h2>
<h3>New Type: MonoTouch.CoreServices.CFHTTPAuthentication</h3>
<pre>
public class CFHTTPAuthentication : MonoTouch.CoreFoundation.CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public static CFHTTPAuthentication CreateFromResponse (CFHTTPMessage response);
	public static int GetTypeID ();
	public bool AppliesToRequest (CFHTTPMessage request);
	protected void CheckHandle ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public string GetMethod ();
	
	public IntPtr Handle {
		get;
	}
	public bool IsValid {
		get;
	}
	public bool RequiresAccountDomain {
		get;
	}
	public bool RequiresOrderedRequests {
		get;
	}
	public bool RequiresUserNameAndPassword {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreServices.CFHTTPMessage</h3>
<pre>
public class CFHTTPMessage : MonoTouch.CoreFoundation.CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public static CFHTTPMessage CreateRequest (MonoTouch.CoreFoundation.CFUrl url, MonoTouch.Foundation.NSString method, Version version);
	public static CFHTTPMessage CreateRequest (Uri uri, string method);
	public static CFHTTPMessage CreateRequest (Uri uri, string method, Version version);
	public static int GetTypeID ();
	public bool AddAuthentication (CFHTTPMessage failureResponse, MonoTouch.Foundation.NSString username, MonoTouch.Foundation.NSString password, AuthenticationScheme scheme, bool forProxy);
	public void ApplyCredentialDictionary (CFHTTPAuthentication auth, System.Net.NetworkCredential credential);
	public void ApplyCredentials (CFHTTPAuthentication auth, System.Net.NetworkCredential credential);
	protected void CheckHandle ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public MonoTouch.Foundation.NSDictionary GetAllHeaderFields ();
	public void SetBody (byte [] buffer);
	public void SetHeaderFieldValue (string name, string value);
	
	public IntPtr Handle {
		get;
	}
	public bool IsHeaderComplete {
		get;
	}
	public bool IsRequest {
		get;
	}
	public System.Net.HttpStatusCode ResponseStatusCode {
		get;
	}
	public string ResponseStatusLine {
		get;
	}
	public Version Version {
		get;
	}
	
	[Serializable]
	public enum AuthenticationScheme {
		Default,
		Basic,
		Negotiate,
		NTLM,
		Digest
	}
}
</pre>
<h3>New Type: MonoTouch.CoreServices.CFHTTPStream</h3>
<pre>
public class CFHTTPStream : MonoTouch.CoreFoundation.CFReadStream {
	
	public CFHTTPMessage GetFinalRequest ();
	public CFHTTPMessage GetResponseHeader ();
	
	public bool AttemptPersistentConnection {
		get;
		set;
	}
	public Uri FinalURL {
		get;
	}
	public int RequestBytesWrittenCount {
		get;
	}
	public bool ShouldAutoredirect {
		get;
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreText</h2>
<h3>Type Changed: MonoTouch.CoreText.CTFont</h3>
<p>Removed:</p><pre>
 	public CTFontDescriptor[] DefaultCascadeList (string [] languages);
</pre>
<p>Added:</p><pre>
 	public CTFontDescriptor[] GetDefaultCascadeList (string [] languages);
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTFontDescriptor</h3>
<p>Added:</p><pre>
 	public static bool MatchFontDescriptors (CTFontDescriptor[] descriptors, MonoTouch.Foundation.NSSet mandatoryAttributes, Func&lt;CTFontDescriptorMatchingState,IntPtr,bool&gt; progressHandler);
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTFontDescriptorMatchingState</h3>
<p>Removed:</p><pre>
 public enum CTFontDescriptorMatchingState {
 	DidBegin,
 	DidFinish,
 	DidFinishDownloading,
 	DidMatch,
 	DidFailWithError
</pre>
<p>Added:</p><pre>
 public enum CTFontDescriptorMatchingState : uint {
 	Started,
 	Finished,
 	DownloadingFinished,
 	Matched,
 	FailedWithError
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTFontManager</h3>
<p>Added:</p><pre>
 	public static bool RegisterGraphicsFont (MonoTouch.CoreGraphics.CGFont font, out MonoTouch.Foundation.NSError error);
 	public static bool UnregisterGraphicsFont (MonoTouch.CoreGraphics.CGFont font, out MonoTouch.Foundation.NSError error);
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTTypesetterOptionKey</h3>
<p>Removed:</p><pre>
 	[Obsolete]
	public static readonly MonoTouch.Foundation.NSString DisableBidiProcessing;
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 6.0")]
	public static readonly MonoTouch.Foundation.NSString DisableBidiProcessing;
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTTypesetterOptions</h3>
<p>Removed:</p><pre>
 	[Obsolete]
	public bool DisableBidiProcessing {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 6.0")]
	public bool DisableBidiProcessing {
</pre>
<h2>Namespace: MonoTouch.CoreVideo</h2>
<h3>Type Changed: MonoTouch.CoreVideo.CVImageBuffer</h3>
<p>Added:</p><pre>
 	public MonoTouch.CoreGraphics.CGColorSpace ColorSpace {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSArray</h3>
<p>Added:</p><pre>
 	public static NSArray FromNSObjects (int count, params NSObject[] items);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSAttributedString</h3>
<p>These properties are now part of the MonoTouch.UIKit.UIStringAttributeKey class.
<p>Removed:</p><pre>
 	public static NSString BackgroundColorAttributeName {
 		get;
 	}
 	public static NSString FontAttributeName {
 		get;
 	}
 	public static NSString ForegroundColorAttributeName {
 		get;
 	}
 	public static NSString KernAttributeName {
 		get;
 	}
 	public static NSString LigatureAttributeName {
 		get;
 	}
 	public static NSString ParagraphStyleAttributeName {
 		get;
 	}
 	public static NSString ShadowAttributeName {
 		get;
 	}
 	public static NSString StrikethroughStyleAttributeName {
 		get;
 	}
 	public static NSString StrokeColorAttributeName {
 		get;
 	}
 	public static NSString StrokeWidthAttributeName {
 		get;
 	}
 	public static NSString UnderlineStyleAttributeName {
 		get;
 	}
 	public static NSString VerticalGlyphFormAttributeName {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public NSAttributedString (string str, MonoTouch.UIKit.UIStringAttributes attributes);
 	public NSAttributedString (string str, MonoTouch.UIKit.UIFont font, MonoTouch.UIKit.UIColor foregroundColor, MonoTouch.UIKit.UIColor backgroundColor, MonoTouch.UIKit.UIColor strokeColor, MonoTouch.UIKit.NSParagraphStyle paragraphStyle, NSLigatureType ligatures, float kerning, NSUnderlineStyle underlineStyle, MonoTouch.UIKit.NSShadow shadow, float strokeWidth, NSUnderlineStyle strikethroughStyle);
 	public MonoTouch.CoreText.CTStringAttributes GetCoreTextAttributes (int location, out NSRange effectiveRange);
 	public MonoTouch.CoreText.CTStringAttributes GetCoreTextAttributes (int location, out NSRange longestEffectiveRange, NSRange rangeLimit);
 	public MonoTouch.UIKit.UIStringAttributes GetUIKitAttributes (int location, out NSRange effectiveRange);
 	public MonoTouch.UIKit.UIStringAttributes GetUIKitAttributes (int location, out NSRange longestEffectiveRange, NSRange rangeLimit);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSCoder</h3>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	public virtual bool RequiresSecureCoding ();
 	public virtual NSSet AllowedClasses {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSDataWritingOptions</h3>
<p>Added:</p><pre>
 	WithoutOverwriting,
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSDateComponents</h3>
<p>Added:</p><pre>
 	public virtual bool IsLeapMonth {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSDictionary</h3>
<p>Added:</p><pre>
 	public NSDictionary (NSObject first, NSObject second, params NSObject[] args);
 	public NSDictionary (object first, object second, params object [] args);
 	public static NSObject GetSharedKeySetForKeys (NSObject[] keys);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSFileCoordinator</h3>
<p>Added:</p><pre>
 	public virtual void WillMove (NSUrl oldUrl, NSUrl newUrl);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSFileManager</h3>
<p>Added:</p><pre>
 	public static NSString UbiquityIdentityDidChangeNotification {
 		get;
 	}
 	public virtual NSObject UbiquityIdentityToken {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static NSObject ObserveUbiquityIdentityDidChange (EventHandler&lt;NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.NSLigatureType</h3>
<pre>
[Serializable]
public enum NSLigatureType {
	None,
	Default,
	All
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSLinguisticTag</h3>
<p>Removed:</p><pre>
 public class NSLinguisticTag {
 	
 	public NSLinguisticTag ();
</pre>
<p>Added:</p><pre>
 public static class NSLinguisticTag {
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSLocale</h3>
<p>Added:</p><pre>
 	public string GetCurrencyCodeDisplayName (string value);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMutableAttributedString</h3>
<p>Added:</p><pre>
 	public NSMutableAttributedString (string str, MonoTouch.UIKit.UIStringAttributes attributes);
 	public NSMutableAttributedString (string str, MonoTouch.UIKit.UIFont font, MonoTouch.UIKit.UIColor foregroundColor, MonoTouch.UIKit.UIColor backgroundColor, MonoTouch.UIKit.UIColor strokeColor, MonoTouch.UIKit.NSParagraphStyle paragraphStyle, NSLigatureType ligatures, float kerning, NSUnderlineStyle underlineStyle, MonoTouch.UIKit.NSShadow shadow, float strokeWidth, NSUnderlineStyle strikethroughStyle);
 	public void Append (NSAttributedString first, params object [] rest);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMutableDictionary</h3>
<p>Added:</p><pre>
 	public static NSDictionary FromSharedKeySet (NSObject sharedKeyToken);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMutableSet</h3>
<p>Added:</p><pre>
 	public NSMutableSet (NSObject[] objs);
 	public NSMutableSet (params string [] strings);
 	public NSMutableSet (NSArray other);
 	public NSMutableSet (NSSet other);
 	public NSMutableSet (int capacity);
 	public virtual void AddObjects (NSObject[] objects);
 	public virtual void RemoveAll ();
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSRunLoop</h3>
<p>Removed:</p><pre>
 	[Obsolete("Use AcceptInputForMode (NSString, NSDate)")]
	public void AcceptInputForMode (string mode, NSDate limitDate);
 	[Obsolete("Use AddTimer (NSTimer, NSString)")]
	public void AddTimer (NSTimer timer, string forMode);
 	[Obsolete("Use LimitDateForMode (NSString) instead")]
	public NSDate LimitDateForMode (string mode);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use AcceptInputForMode (NSRunLoopMode, NSDate)")]
	public void AcceptInputForMode (string mode, NSDate limitDate);
 	[Obsolete("Use AddTimer (NSTimer, NSRunLoopMode)")]
	public void AddTimer (NSTimer timer, string forMode);
 	[Obsolete("Use LimitDateForMode (NSRunLoopMode) instead")]
	public NSDate LimitDateForMode (string mode);
 	public bool RunUntil (NSRunLoopMode mode, NSDate limitDate);
 	public static NSString UITrackingRunLoopMode {
 		get;
 	}
 	public NSRunLoopMode CurrentRunLoopMode {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSRunLoopMode</h3>
<p>Added:</p><pre>
 	UITracking,
 	Other
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSSet</h3>
<p>Removed:</p><pre>
 public class NSSet : NSObject {
 	public NSSet (NSObject[] objs);
</pre>
<p>Added:</p><pre>
 public class NSSet : NSObject, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable&lt;NSObject&gt; {
 	public NSSet (params NSObject[] objs);
 	public NSSet (params object [] objs);
 	public NSSet (NSSet other);
 	public bool Contains (object obj);
 	public System.Collections.Generic.IEnumerator&lt;NSObject&gt; GetEnumerator ();
 	public virtual bool IntersectsSet (NSSet other);
 	System.Collections.IEnumerator System.Collections.IEnumerable.GetEnumerator ();
 	public static NSSet operator + (NSSet first, NSSet second);
 	public static NSSet operator - (NSSet first, NSSet second);
 	
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSString</h3>
<p>Removed:</p><pre>
 	public virtual string CapitalizeWithLocale (NSLocale locale);
 	public virtual string LowercaseWithLocale (NSLocale locale);
 	public virtual string UppercaseWithLocale (NSLocale locale);
</pre>
<p>Added:</p><pre>
 	public virtual string Capitalize (NSLocale locale);
 	public virtual string ToLower (NSLocale locale);
 	public virtual string ToUpper (NSLocale locale);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrl</h3>
<p>Added:</p><pre>
 	public NSUrl (NSData bookmarkData, NSUrlBookmarkResolutionOptions resolutionOptions, NSUrl relativeUrl, out bool bookmarkIsStale, out NSError error);
 	public virtual NSData CreateBookmarkData (NSUrlBookmarkCreationOptions options, string [] resourceValues, NSUrl relativeUrl, out NSError error);
 	public static NSString PathKey {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlBookmarkCreationOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSUrlBookmarkCreationOptions {
	PreferFileIDResolution,
	MinimalBookmark,
	SuitableForBookmarkFile,
	WithSecurityScope,
	SecurityScopeAllowOnlyReadAccess
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlBookmarkResolutionOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSUrlBookmarkResolutionOptions {
	WithoutUI,
	WithoutMounting,
	WithSecurityScope
}
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>New Type: MonoTouch.GameKit.GKAchievementChallenge</h3>
<pre>
public class GKAchievementChallenge : GKChallenge {
	
	public GKAchievementChallenge ();
	public GKAchievementChallenge (MonoTouch.Foundation.NSCoder coder);
	public GKAchievementChallenge (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievementChallenge (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual GKAchievement Achievement {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKGameCenterControllerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void Finished (GKGameCenterViewController gameCenterViewController);
</pre>
<p>Added:</p><pre>
 	public virtual void Finished (GKGameCenterViewController controller);
</pre>
<h2>Namespace: MonoTouch.ImageIO</h2>
<h3>Type Changed: MonoTouch.ImageIO.CGImageProperties</h3>
<p>Removed:</p><pre>
 public class CGImageProperties {
 	
 	public CGImageProperties ();
</pre>
<p>Added:</p><pre>
 public static class CGImageProperties {
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>Type Changed: MonoTouch.MapKit.MKLaunchOptions</h3>
<p>Removed:</p><pre>
 	public Nullable&lt;MKDirectionsMode&gt; Directions;
 	public Nullable&lt;MKMapType&gt; MapType;
 	public System.Nullable&lt;MonoTouch.CoreLocation.CLLocationCoordinate2D&gt; MapCenter;
 	public Nullable&lt;MKCoordinateSpan&gt; MapSpan;
 	public Nullable&lt;bool&gt; ShowsTraffic;
</pre>
<p>Added:</p><pre>
 	public Nullable&lt;MKDirectionsMode&gt; DirectionsMode {
 		get;
 		set;
 	}
 	public System.Nullable&lt;MonoTouch.CoreLocation.CLLocationCoordinate2D&gt; MapCenter {
 		get;
 		set;
 	}
 	public Nullable&lt;MKCoordinateSpan&gt; MapSpan {
 		get;
 		set;
 	}
 	public Nullable&lt;MKMapType&gt; MapType {
 		get;
 		set;
 	}
 	public Nullable&lt;bool&gt; ShowTraffic {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapView</h3>
<p>Removed:</p><pre>
 	public void AddAnnotation (MKAnnotation[] annotations);
 	public void AddAnnotation (MKPlacemark[] placemarks);
 	public virtual MKCoordinateRegion ConvertRect (System.Drawing.RectangleF rect, MonoTouch.UIKit.UIView toRegiontFromView);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use AddAnnotations")]
	public void AddAnnotation (MKAnnotation[] annotations);
 	[Obsolete("Use AddPlacemarks")]
	public void AddAnnotation (MKPlacemark[] placemarks);
 	public void AddPlacemarks (MKPlacemark[] placemarks);
 	public virtual MKCoordinateRegion ConvertRect (System.Drawing.RectangleF rect, MonoTouch.UIKit.UIView toRegionFromView);
</pre>
<h2>Namespace: MonoTouch.MediaToolbox</h2>
<h3>Type Changed: MonoTouch.MediaToolbox.MTAudioProcessingTapCallbacks</h3>
<p>Removed:</p><pre>
 	public void SetInitialize (MTAudioProcessingTapInitCallback callback, void * clientInfo);
 	
</pre>
<p>Added:</p><pre>
 		set;
</pre>
<h3>Type Changed: MonoTouch.MediaToolbox.MTAudioProcessingTapInitCallback</h3>
<p>Removed:</p><pre>
 public delegate void MTAudioProcessingTapInitCallback (MTAudioProcessingTap tap, void * clientInfo, out void * tapStorage);
</pre>
<p>Added:</p><pre>
 public delegate void MTAudioProcessingTapInitCallback (MTAudioProcessingTap tap, out void * tapStorage);
</pre>
<h3>New Type: MonoTouch.ObjCRuntime.ThreadSafeAttribute</h3>
<p>This attribute is not actually used by the runtime, it is mostly
used for documentation purposes and to provide some of our upcoming
tooling to assist developers with their code.
<pre>
public class ThreadSafeAttribute : Attribute {
	
	public ThreadSafeAttribute ();
}
</pre>
<h2>Namespace: MonoTouch.PassKit</h2>
<h3>Type Changed: MonoTouch.PassKit.PKAddPassesViewController</h3>
<p>Removed:</p><pre>
 	public event EventHandler DidFinish;
</pre>
<p>Added:</p><pre>
 	public event EventHandler Finished;
</pre>
<h3>Type Changed: MonoTouch.PassKit.PKAddPassesViewControllerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidFinish (PKAddPassesViewController controller);
</pre>
<p>Added:</p><pre>
 	public virtual void Finished (PKAddPassesViewController controller);
</pre>
<h3>Type Changed: MonoTouch.PassKit.PKPass</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject LocalizedValueForFieldKey (MonoTouch.Foundation.NSString key);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject GetLocalizedValue (MonoTouch.Foundation.NSString key);
</pre>
<h3>Type Changed: MonoTouch.PassKit.PKPassLibrary</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString AddedPassesUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PassTypeIdentifierUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RemovedPassInfosUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ReplacementPassesUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SerialNumberUserInfoKey {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public static class Notifications {
 		
 		public static MonoTouch.Foundation.NSObject ObserveDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoTouch.PassKit.PKPassLibraryUserInfoKey</h3>
<pre>
public static class PKPassLibraryUserInfoKey {
	
	public static MonoTouch.Foundation.NSString AddedPasses {
		get;
	}
	public static MonoTouch.Foundation.NSString PassTypeIdentifier {
		get;
	}
	public static MonoTouch.Foundation.NSString RemovedPassInfos {
		get;
	}
	public static MonoTouch.Foundation.NSString ReplacementPasses {
		get;
	}
	public static MonoTouch.Foundation.NSString SerialNumber {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.QuickLook</h2>
<h3>Type Changed: MonoTouch.QuickLook.QLFrame</h3>
<p>Removed:</p><pre>
 public delegate System.Drawing.RectangleF QLFrame (QLPreviewItem item, MonoTouch.UIKit.UIView view);
</pre>
<p>Added:</p><pre>
 public delegate System.Drawing.RectangleF QLFrame (QLPreviewController controller, QLPreviewItem item, ref MonoTouch.UIKit.UIView view);
</pre>
<h3>Type Changed: MonoTouch.QuickLook.QLPreviewControllerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual System.Drawing.RectangleF FrameForPreviewItem (QLPreviewItem item, MonoTouch.UIKit.UIView view);
 	public virtual MonoTouch.UIKit.UIImage TransitionImageForPreviewItem (QLPreviewItem item, System.Drawing.RectangleF contentRect);
</pre>
<p>Added:</p><pre>
 	public virtual System.Drawing.RectangleF FrameForPreviewItem (QLPreviewController controller, QLPreviewItem item, ref MonoTouch.UIKit.UIView view);
 	public virtual MonoTouch.UIKit.UIImage TransitionImageForPreviewItem (QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect);
</pre>
<h3>Type Changed: MonoTouch.QuickLook.QLTransition</h3>
<p>Removed:</p><pre>
 public delegate MonoTouch.UIKit.UIImage QLTransition (QLPreviewItem item, System.Drawing.RectangleF contentRect);
</pre>
<p>Added:</p><pre>
 public delegate MonoTouch.UIKit.UIImage QLTransition (QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect);
</pre>
<h2>Namespace: MonoTouch.Social</h2>
<h3>Type Changed: MonoTouch.Social.SLComposeViewController</h3>
<p>Removed:</p><pre>
 	public virtual bool AddURL (MonoTouch.Foundation.NSUrl url);
 	public virtual bool RemoveAllURLs ();
</pre>
<p>Added:</p><pre>
 	public virtual bool AddUrl (MonoTouch.Foundation.NSUrl url);
 	public virtual bool RemoveAllUrls ();
</pre>
<h3>Type Changed: MonoTouch.Social.SLRequest</h3>
<p>Removed:</p><pre>
 	public static SLRequest Create (MonoTouch.Foundation.NSString slServiceType, SLRequestMethod requestMethod, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary parameters);
 	public virtual MonoTouch.Foundation.NSUrlRequest PreparedUrlRequest ();
 	public virtual MonoTouch.Foundation.NSUrl URL {
</pre>
<p>Added:</p><pre>
 	public static SLRequest Create (MonoTouch.Foundation.NSString serviceType, SLRequestMethod requestMethod, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary parameters);
 	public virtual MonoTouch.Foundation.NSUrlRequest GetPreparedUrlRequest ();
 	public virtual MonoTouch.Foundation.NSUrl Url {
</pre>
<h3>Type Changed: MonoTouch.Social.SLServiceType</h3>
<p>Removed:</p><pre>
 public class SLServiceType {
 	
 	public SLServiceType ();
</pre>
<p>Added:</p><pre>
 public static class SLServiceType {
</pre>
<h2>Namespace: MonoTouch.StoreKit</h2>
<h3>Type Changed: MonoTouch.StoreKit.SKDownload</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSUrl ContentURL {
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSUrl ContentUrl {
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKStoreProductViewController</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString ParameterITunesItemIdentifier {
 	public event EventHandler DidFinish;
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString ITunesItemIdentifier {
 	public event EventHandler Finished;
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKStoreProductViewControllerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidFinish (SKStoreProductViewController viewController);
</pre>
<p>Added:</p><pre>
 	public virtual void Finished (SKStoreProductViewController controller);
</pre>
<h3>Type Removed: MonoTouch.UIKit.NSLineBreakMode</h3>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>New Type: MonoTouch.UIKit.NSMutableParagraphStyle</h3>
<pre>
public class NSMutableParagraphStyle : NSParagraphStyle {
	
	public NSMutableParagraphStyle ();
	public NSMutableParagraphStyle (MonoTouch.Foundation.NSCoder coder);
	public NSMutableParagraphStyle (MonoTouch.Foundation.NSObjectFlag t);
	public NSMutableParagraphStyle (IntPtr handle);
	
	public override UITextAlignment Alignment {
		get;
		set;
	}
	public override MonoTouch.Foundation.NSWritingDirection BaseWritingDirection {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public override float FirstLineHeadIndent {
		get;
		set;
	}
	public override float HeadIndent {
		get;
		set;
	}
	public override float HyphenationFactor {
		get;
		set;
	}
	public override UILineBreakMode LineBreakMode {
		get;
		set;
	}
	public override float LineHeightMultiple {
		get;
		set;
	}
	public override float LineSpacing {
		get;
		set;
	}
	public override float MaximumLineHeight {
		get;
		set;
	}
	public override float MinimumLineHeight {
		get;
		set;
	}
	public override float ParagraphSpacingBefore {
		get;
		set;
	}
	public override float TailIndent {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSParagraphStyle</h3>
<pre>
public class NSParagraphStyle : MonoTouch.Foundation.NSObject {
	
	public NSParagraphStyle ();
	public NSParagraphStyle (MonoTouch.Foundation.NSCoder coder);
	public NSParagraphStyle (MonoTouch.Foundation.NSObjectFlag t);
	public NSParagraphStyle (IntPtr handle);
	
	public static MonoTouch.Foundation.NSWritingDirection GetDefaultWritingDirection (string languageName);
	
	public static NSParagraphStyle Default {
		get;
	}
	public virtual UITextAlignment Alignment {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSWritingDirection BaseWritingDirection {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float FirstLineHeadIndent {
		get;
		set;
	}
	public virtual float HeadIndent {
		get;
		set;
	}
	public virtual float HyphenationFactor {
		get;
		set;
	}
	public virtual UILineBreakMode LineBreakMode {
		get;
		set;
	}
	public virtual float LineHeightMultiple {
		get;
		set;
	}
	public virtual float LineSpacing {
		get;
		set;
	}
	public virtual float MaximumLineHeight {
		get;
		set;
	}
	public virtual float MinimumLineHeight {
		get;
		set;
	}
	public virtual float ParagraphSpacing {
		get;
	}
	public virtual float ParagraphSpacingBefore {
		get;
		set;
	}
	public virtual float TailIndent {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSShadow</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject ShadowColor {
</pre>
<p>Added:</p><pre>
 	public virtual UIColor ShadowColor {
</pre>
<h3>Type Removed: MonoTouch.UIKit.NSTextAlignment</h3>
<h3>Type Changed: MonoTouch.UIKit.UIActivity</h3>
<p>Removed:</p><pre>
 	public virtual void ActivityDidFinish (bool completed);
 	public virtual void PerformActivity ();
 	public static MonoTouch.Foundation.NSString TypeAssignToContact {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeCopyToPasteboard {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeMail {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeMessage {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypePostToFacebook {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypePostToTwitter {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypePostToWeibo {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypePrint {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeSaveToCameraRoll {
 		get;
 	}
 	public virtual UIImage ActivityImage {
 	public virtual string ActivityTitle {
 	public virtual string ActivityType {
 	public virtual UIViewController ActivityViewController {
 	public override IntPtr ClassHandle {
</pre>
<p>Added:</p><pre>
 	public virtual void Finished (bool completed);
 	public virtual void Perform ();
 	public override IntPtr ClassHandle {
 	public virtual UIImage Image {
 	public virtual string Title {
 	public virtual MonoTouch.Foundation.NSString Type {
 	public virtual UIViewController ViewController {
</pre>
<h3>New Type: MonoTouch.UIKit.UIActivityType</h3>
<pre>
public static class UIActivityType {
	
	public static MonoTouch.Foundation.NSString AssignToContact {
		get;
	}
	public static MonoTouch.Foundation.NSString CopyToPasteboard {
		get;
	}
	public static MonoTouch.Foundation.NSString Mail {
		get;
	}
	public static MonoTouch.Foundation.NSString Message {
		get;
	}
	public static MonoTouch.Foundation.NSString PostToFacebook {
		get;
	}
	public static MonoTouch.Foundation.NSString PostToTwitter {
		get;
	}
	public static MonoTouch.Foundation.NSString PostToWeibo {
		get;
	}
	public static MonoTouch.Foundation.NSString Print {
		get;
	}
	public static MonoTouch.Foundation.NSString SaveToCameraRoll {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplication</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString UITrackingRunLoopMode {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIButton</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSAttributedString AttributedTitleForState (UIControlState state);
 	public virtual void SetAttributedTitleforState (MonoTouch.Foundation.NSAttributedString title, UIControlState state);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSAttributedString GetAttributedTitle (UIControlState state);
 	public virtual void SetAttributedTitle (MonoTouch.Foundation.NSAttributedString title, UIControlState state);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionView</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSIndexPath[] IndexPathsForSelectedItems ();
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSIndexPath[] GetIndexPathsForSelectedItems ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewController</h3>
<p>Removed:</p><pre>
 	public virtual void DidDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidEndDisplayingCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidEndDisplayingSupplementaryView (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidUnhighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual int ItemsInSection (UICollectionView collectionView, int section);
 	public virtual int NumberOfSections (UICollectionView collectionView);
</pre>
<p>Added:</p><pre>
 	public UICollectionViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
 	public virtual void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual int GetItemsCount (UICollectionView collectionView, int section);
 	public virtual int GetSectionsCount (UICollectionView collectionView);
 	public virtual UICollectionReusableView GetView (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemDeselected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemHighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemSelected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemUnhighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDataSource</h3>
<p>Removed:</p><pre>
 	public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public abstract int ItemsInSection (UICollectionView collectionView, int section);
 	public virtual int NumberOfSections (UICollectionView collectionView);
</pre>
<p>Added:</p><pre>
 	public abstract int GetItemsCount (UICollectionView collectionView, int section);
 	public virtual int GetSectionsCount (UICollectionView collectionView);
 	public virtual UICollectionReusableView GetView (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidEndDisplayingCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidEndDisplayingSupplementaryView (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidUnhighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<p>Added:</p><pre>
 	public virtual void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemDeselected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemHighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemSelected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemUnhighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout</h3>
<p>Removed:</p><pre>
 	public override void DidDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void DidEndDisplayingCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void DidEndDisplayingSupplementaryView (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void DidHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void DidSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void DidUnhighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<p>Added:</p><pre>
 	public override void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void ItemDeselected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void ItemHighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void ItemSelected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void ItemUnhighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public override void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutAttributes</h3>
<p>Removed:</p><pre>
 	public static UICollectionViewLayoutAttributes FromIndexPath (MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<p>Added:</p><pre>
 	public static UICollectionViewLayoutAttributes CreateForCell (MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewSource</h3>
<p>Removed:</p><pre>
 	public virtual void DidDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidEndDisplayingCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidEndDisplayingSupplementaryView (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidUnhighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual int ItemsInSection (UICollectionView collectionView, int section);
 	public virtual int NumberOfSections (UICollectionView collectionView);
</pre>
<p>Added:</p><pre>
 	public virtual void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual int GetItemsCount (UICollectionView collectionView, int section);
 	public virtual int GetSectionsCount (UICollectionView collectionView);
 	public virtual UICollectionReusableView GetView (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemDeselected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemHighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemSelected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void ItemUnhighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIKeyboard</h3>
<p>Removed:</p><pre>
 public class UIKeyboard {
 	
 	public UIKeyboard ();
</pre>
<p>Added:</p><pre>
 public static class UIKeyboard {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINib</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString ExternalObjectsKey {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewController</h3>
<p>Added:</p><pre>
 	public UIPageViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPickerViewDelegate</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSAttributedString GetAttribytedTitle (UIPickerView pickerView, int row, int component);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSAttributedString GetAttributedTitle (UIPickerView pickerView, int row, int component);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIReferenceLibraryViewController</h3>
<p>Added:</p><pre>
 	public UIReferenceLibraryViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBar</h3>
<p>Added:</p><pre>
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>New Type: MonoTouch.UIKit.UIStringAttributeKey</h3>
<pre>
public static class UIStringAttributeKey {
	
	public static readonly MonoTouch.Foundation.NSString Font;
	public static readonly MonoTouch.Foundation.NSString ForegroundColor;
	public static readonly MonoTouch.Foundation.NSString BackgroundColor;
	public static readonly MonoTouch.Foundation.NSString StrikethroughStyle;
	public static readonly MonoTouch.Foundation.NSString StrokeColor;
	public static readonly MonoTouch.Foundation.NSString Shadow;
	public static readonly MonoTouch.Foundation.NSString ParagraphStyle;
	public static readonly MonoTouch.Foundation.NSString Ligature;
	public static readonly MonoTouch.Foundation.NSString KerningAdjustment;
	public static readonly MonoTouch.Foundation.NSString UnderlineStyle;
	public static readonly MonoTouch.Foundation.NSString StrokeWidth;
	public static readonly MonoTouch.Foundation.NSString VerticalGlyphForm;
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIStringAttributes</h3>
<pre>
public class UIStringAttributes {
	
	public UIStringAttributes ();
	public UIStringAttributes (MonoTouch.Foundation.NSDictionary dictionary);
	
	public UIColor BackgroundColor {
		get;
		set;
	}
	public MonoTouch.Foundation.NSDictionary Dictionary {
		get;
	}
	public UIFont Font {
		get;
		set;
	}
	public UIColor ForegroundColor {
		get;
		set;
	}
	public Nullable<float> KerningAdjustment {
		get;
		set;
	}
	public System.Nullable<monotouch.foundation.nsligaturetype> Ligature {
		get;
		set;
	}
	public NSParagraphStyle ParagraphStyle {
		get;
		set;
	}
	public NSShadow Shadow {
		get;
		set;
	}
	public System.Nullable<monotouch.foundation.nsunderlinestyle> StrikethroughStyle {
		get;
		set;
	}
	public UIColor StrokeColor {
		get;
		set;
	}
	public Nullable<float> StrokeWidth {
		get;
		set;
	}
	public System.Nullable<monotouch.foundation.nsunderlinestyle> UnderlineStyle {
		get;
		set;
	}
}
</monotouch.foundation.nsunderlinestyle></float></monotouch.foundation.nsunderlinestyle></monotouch.foundation.nsligaturetype></float></pre>
<h3>Type Changed: MonoTouch.UIKit.UITableView</h3>
<p>Removed:</p><pre>
 	public virtual UITableViewHeaderFooterView FooterViewForSection (int section);
 	public virtual UITableViewHeaderFooterView HeaderViewForSection (int section);
</pre>
<p>Added:</p><pre>
 	public virtual UITableViewHeaderFooterView GetFooterView (int section);
 	public virtual UITableViewHeaderFooterView GetHeaderView (int section);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidEndDisplayingCell (UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void DidEndDisplayingFooterView (UITableView tableView, UIView footerView, int section);
 	public virtual void DidEndDisplayingHeaderView (UITableView tableView, UIView headerView, int section);
 	public virtual void DidHighlightRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
 	public virtual void DidUnhighlightRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
</pre>
<p>Added:</p><pre>
 	public virtual void CellDisplayingEnded (UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void FooterViewDisplayingEnded (UITableView tableView, UIView footerView, int section);
 	public virtual void HeaderViewDisplayingEnded (UITableView tableView, UIView headerView, int section);
 	public virtual void RowHighlighted (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
 	public virtual void RowUnhighlighted (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextField</h3>
<p>Removed:</p><pre>
 	public virtual UITextSelectionRect[] SelectionRectsForRange (UITextRange range);
</pre>
<p>Added:</p><pre>
 	public virtual UITextSelectionRect[] GetSelectionRects (UITextRange range);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextView</h3>
<p>Removed:</p><pre>
 	public virtual UITextSelectionRect[] SelectionRectsForRange (UITextRange range);
</pre>
<p>Added:</p><pre>
 	public virtual UITextSelectionRect[] GetSelectionRects (UITextRange range);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Removed:</p><pre>
 	public static void BeginAnimations (string s, IntPtr context);
 	public virtual NSLayoutConstraint[] ConstraintsAffectingLayout (UILayoutConstraintAxis axis);
</pre>
<p>Added:</p><pre>
 	public static void BeginAnimations (string animationID, IntPtr context);
 	public virtual NSLayoutConstraint[] GetConstraintsAffectingLayout (UILayoutConstraintAxis axis);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewController</h3>
<p>Removed:</p><pre>
 	public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations ();
</pre>
<p>Added:</p><pre>
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations ();
</pre>
</body>
</html>
