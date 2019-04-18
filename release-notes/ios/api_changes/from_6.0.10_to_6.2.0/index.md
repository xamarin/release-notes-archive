---
id: (GUID)
title: "From 6.0.10 to 6.2.0"
---

<html><head><title>Comparison between monotouch-6.0.10.dll and monotouch-6.2.0.dll</title></head>
<body>
<a name="Namespace:_MonoTouch" class="injected"></a>
<h2>Namespace: MonoTouch</h2>
<a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.0.10";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.2.0";
</pre>
<a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<a name="New_Type:_MonoTouch.AudioToolbox.AudioClassDescription" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.AudioClassDescription</h3>
<pre>
public struct AudioClassDescription {
	
	public AudioClassDescription (AudioCodecComponentType type, AudioFormatType subType, MonoTouch.AudioUnit.AudioCodecManufacturer manufacturer);
	
	public bool IsHardwareCodec {
		get;
	}
	
	public AudioCodecComponentType Type;
	public AudioFormatType SubType;
	public MonoTouch.AudioUnit.AudioCodecManufacturer Manufacturer;
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.AudioCodecComponentType" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.AudioCodecComponentType</h3>
<pre>
[Serializable]
public enum AudioCodecComponentType {
	Decoder,
	Encoder
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.AudioFormatAvailability" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.AudioFormatAvailability</h3>
<pre>
public static class AudioFormatAvailability {
	
	public static AudioValueRange[] GetAvailableEncodeBitRates (AudioFormatType format);
	public static AudioValueRange[] GetAvailableEncodeSampleRates (AudioFormatType format);
	public static AudioClassDescription[] GetDecoders (AudioFormatType format);
	public static AudioClassDescription[] GetEncoders (AudioFormatType format);
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.ExtendedNoteOnEvent" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.ExtendedNoteOnEvent</h3>
<pre>
public struct ExtendedNoteOnEvent {
	
	public uint InstrumentID;
	public uint DeviceGroupID;
	public float Duration;
	public float Pitch;
	public float Velocity;
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MidiChannelMessage" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MidiChannelMessage</h3>
<pre>
public struct MidiChannelMessage {
	
	public MidiChannelMessage (byte status, byte data1, byte data2);
	
	public byte Status;
	public byte Data1;
	public byte Data2;
	public byte Reserved;
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MidiMetaEvent" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MidiMetaEvent</h3>
<pre>
public class MidiMetaEvent : _MidiData {
	
	public MidiMetaEvent ();
	
	public byte MetaEventType;
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MidiNoteMessage" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MidiNoteMessage</h3>
<pre>
public struct MidiNoteMessage {
	
	public MidiNoteMessage (byte channel, byte note, byte velocity, byte releaseVelocity, float duration);
	
	public byte Channel;
	public byte Note;
	public byte Velocity;
	public byte ReleaseVelocity;
	public float Duration;
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MidiRawData" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MidiRawData</h3>
<pre>
public class MidiRawData : _MidiData {
	
	public MidiRawData ();
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicEventType" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicEventType</h3>
<pre>
[Serializable]
public enum MusicEventType : uint {
	Null,
	ExtendedNote,
	ExtendedTempo,
	User,
	Meta,
	MidiNoteMessage,
	MidiChannelMessage,
	MidiRawData,
	Parameter,
	AUPreset
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicEventUserData" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicEventUserData</h3>
<pre>
public class MusicEventUserData : MidiRawData {
	
	public MusicEventUserData ();
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicPlayer" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicPlayer</h3>
<pre>
public class MusicPlayer : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public MusicPlayer ();
	
	public static MusicPlayer Create (out MusicPlayerStatus OSstatus);
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public MusicPlayerStatus GetBeatsForHostTime (long hostTime, out double beats);
	public MusicPlayerStatus GetHostTimeForBeats (double beats, out long hostTime);
	public MusicPlayerStatus Preroll ();
	public MusicPlayerStatus Start ();
	public MusicPlayerStatus Stop ();
	
	public IntPtr Handle {
		get;
	}
	public bool IsPlaying {
		get;
	}
	public MusicSequence MusicSequence {
		get;
		set;
	}
	public double PlayRateScalar {
		get;
		set;
	}
	public double Time {
		get;
		set;
	}
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicPlayerStatus" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicPlayerStatus</h3>
<pre>
[Serializable]
public enum MusicPlayerStatus {
	Success,
	InvalidSequenceType,
	TrackIndexError,
	TrackNotFound,
	EndOfTrack,
	StartOfTrack,
	IllegalTrackDestination,
	NoSequence,
	InvalidEventType,
	InvalidPlayerState,
	CannotDoInCurrentContext
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicSequence" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicSequence</h3>
<pre>
public class MusicSequence : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public MusicSequence ();
	
	public MusicPlayerStatus BarBeatTimeToBeats (MonoTouch.CoreAnimation.CABarBeatTime barBeatTime);
	public MusicPlayerStatus BeatsToBarBeatTime (double beats, int subbeatDivisor, out MonoTouch.CoreAnimation.CABarBeatTime barBeatTime);
	public MonoTouch.Foundation.NSData CreateData (MusicSequenceFileTypeID fileType, MusicSequenceFileFlags flags, ushort resolution);
	public MusicPlayerStatus CreateFile (MonoTouch.Foundation.NSUrl url, MusicSequenceFileTypeID fileType, MusicSequenceFileFlags flags, ushort resolution);
	public MusicTrack CreateTrack ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public double GetBeatsForSeconds (double seconds);
	public MonoTouch.Foundation.NSDictionary GetInfoDictionary ();
	public double GetSecondsForBeats (double beats);
	public void GetSmpteResolution (short resolution, out sbyte fps, out byte ticks);
	public MusicTrack GetTrack (int trackIndex);
	public int GetTrackIndex (MusicTrack track);
	public MusicPlayerStatus LoadData (MonoTouch.Foundation.NSData data, MusicSequenceFileTypeID fileTypeId, MusicSequenceLoadFlags loadFlags);
	public MusicPlayerStatus LoadFile (MonoTouch.Foundation.NSUrl url, MusicSequenceFileTypeID fileTypeId, MusicSequenceLoadFlags loadFlags);
	public MusicPlayerStatus Reverse ();
	public MusicPlayerStatus SetMidiEndpoint (MonoTouch.CoreMidi.MidiEndpoint endpoint);
	public short SetSmpteResolution (sbyte fps, byte ticks);
	
	public MonoTouch.AudioUnit.AUGraph AUGraph {
		get;
		set;
	}
	public IntPtr Handle {
		get;
	}
	public MusicSequenceType SequenceType {
		get;
		set;
	}
	public int TrackCount {
		get;
	}
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicSequenceFileFlags" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicSequenceFileFlags</h3>
<pre>
[Serializable]
[Flags]
public enum MusicSequenceFileFlags {
	EraseFile
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicSequenceFileTypeID" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicSequenceFileTypeID</h3>
<pre>
[Serializable]
public enum MusicSequenceFileTypeID : uint {
	Midi,
	iMelody
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicSequenceLoadFlags" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicSequenceLoadFlags</h3>
<pre>
[Serializable]
[Flags]
public enum MusicSequenceLoadFlags {
	ChannelsToTracks
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicSequenceType" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicSequenceType</h3>
<pre>
[Serializable]
public enum MusicSequenceType : uint {
	Beats,
	Seconds,
	Samples
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox.MusicTrack" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox.MusicTrack</h3>
<pre>
public class MusicTrack : MonoTouch.ObjCRuntime.INativeObject {
	
	public static MusicTrack FromSequence (MusicSequence sequence);
	public MusicPlayerStatus AddExtendedTempoEvent (double timestamp, double bmp);
	public MusicPlayerStatus AddMetaEvent (double timestamp, MidiMetaEvent metaEvent);
	public MusicPlayerStatus AddMidiChannelEvent (double timestamp, MidiChannelMessage channelMessage);
	public MusicPlayerStatus AddMidiNoteEvent (double timeStamp, MidiNoteMessage message);
	public MusicPlayerStatus AddMidiRawDataEvent (double timestamp, MidiRawData rawData);
	public MusicPlayerStatus AddNewExtendedNoteEvent (double timestamp, ExtendedNoteOnEvent evt);
	public MusicPlayerStatus AddUserEvent (double timestamp, MusicEventUserData userData);
	public MusicPlayerStatus Clear (double startTime, double endTime);
	public MusicPlayerStatus CopyInsert (double sourceStartTime, double sourceEndTime, MusicTrack targetTrack, double targetInsertTime);
	public MusicPlayerStatus Cut (double startTime, double endTime);
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public MusicPlayerStatus Merge (double sourceStartTime, double sourceEndTime, MusicTrack targetTrack, double targetInsertTime);
	public MusicPlayerStatus MoveEvents (double startTime, double endTime, double moveTime);
	public MusicPlayerStatus SetDestMidiEndpoint (MonoTouch.CoreMidi.MidiEndpoint endpoint);
	public MusicPlayerStatus SetDestNode (int node);
	
	public IntPtr Handle {
		get;
	}
	public bool MuteStatus {
		get;
		set;
	}
	public MusicSequence Sequence {
		get;
	}
	public bool SoloStatus {
		get;
		set;
	}
}
</pre>
<a name="New_Type:_MonoTouch.AudioToolbox._MidiData" class="injected"></a>
<h3>New Type: MonoTouch.AudioToolbox._MidiData</h3>
<pre>
public abstract class _MidiData {
	
	protected _MidiData ();
	
	public void SetData (byte [] Data);
	public void SetData (int len, int start, byte [] Data);
	public void SetData (int len, IntPtr buffer);
	
	protected int len;
	protected int start;
	protected byte [] data;
	protected IntPtr buffer;
}
</pre>
<a name="Namespace:_MonoTouch.Foundation" class="injected"></a>
<h2>Namespace: MonoTouch.Foundation</h2>
<a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>
<h3>Type Changed: MonoTouch.Foundation.NSObject</h3>
<p>Removed:</p><pre>
 	public static System.Reflection.Assembly MonoTouchAssembly;
</pre>
<p>Added:</p><pre>
 	public static readonly System.Reflection.Assembly MonoTouchAssembly;
</pre>
<a name="Type_Changed:_MonoTouch.Foundation.NSObjectFlag" class="injected"></a>
<h3>Type Changed: MonoTouch.Foundation.NSObjectFlag</h3>
<p>Removed:</p><pre>
 	public static NSObjectFlag Empty;
</pre>
<p>Added:</p><pre>
 	public static readonly NSObjectFlag Empty;
</pre>
<a name="Namespace:_MonoTouch.GameKit" class="injected"></a>
<h2>Namespace: MonoTouch.GameKit</h2>
<a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboard" class="injected"></a>
<h3>Type Changed: MonoTouch.GameKit.GKLeaderboard</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated iOS 6.0")]
	public static void LoadCategories (GKCategoryHandler categoryHandler);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated iOS 6.0, use loadLeaderboardsWithCompletionHandler")]
	public static void LoadCategories (GKCategoryHandler categoryHandler);
</pre>
<a name="Type_Changed:_MonoTouch.GameKit.GKMatch" class="injected"></a>
<h3>Type Changed: MonoTouch.GameKit.GKMatch</h3>
<p>Removed:</p><pre>
 	public event EventHandler&lt;GKPlayerErrorEventArgs&gt; ConnectionFailed;
</pre>
<p>Added:</p><pre>
 	[Obsolete("No longer on iOS")]
	public event EventHandler&lt;GKPlayerErrorEventArgs&gt; ConnectionFailed;
</pre>
<a name="Type_Changed:_MonoTouch.GameKit.GKMatchDelegate" class="injected"></a>
<h3>Type Changed: MonoTouch.GameKit.GKMatchDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void ConnectionFailed (GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
</pre>
<p>Added:</p><pre>
 	[Obsolete("No longer on iOS")]
	public virtual void ConnectionFailed (GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
</pre>
<a name="Type_Changed:_MonoTouch.GameKit.GKMatchmakerViewController" class="injected"></a>
<h3>Type Changed: MonoTouch.GameKit.GKMatchmakerViewController</h3>
<p>Removed:</p><pre>
 	public virtual void SetHostedPlayerReady (string playerID);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 5.0, use SetHostedPlayerConnected")]
	public virtual void SetHostedPlayerReady (string playerID);
</pre>
<a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>
<h2>Namespace: MonoTouch.MediaPlayer</h2>
<a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h3>
<p>Removed:</p><pre>
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler&lt;MPMoviePlayerFullScreenEventArgs&gt; handler);
</pre>
<p>Added:</p><pre>
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Added:</p><pre>
 	public static bool bool_objc_msgSend_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSend_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool bool_objc_msgSend_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool bool_objc_msgSendSuper_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSend_Double_float (IntPtr receiver, IntPtr selector, double arg1, float arg2);
 	public static void void_objc_msgSend_UInt32_UInt32 (IntPtr receiver, IntPtr selector, uint arg1, uint arg2);
 	public static void void_objc_msgSendSuper_Double_float (IntPtr receiver, IntPtr selector, double arg1, float arg2);
 	public static void void_objc_msgSendSuper_UInt32_UInt32 (IntPtr receiver, IntPtr selector, uint arg1, uint arg2);
</pre>
<a name="Type_Changed:_MonoTouch.ObjCRuntime.Runtime" class="injected"></a>
<h3>Type Changed: MonoTouch.ObjCRuntime.Runtime</h3>
<p>Added:</p><pre>
 	public static void ConnectMethod (Type type, System.Reflection.MethodInfo method, MonoTouch.Foundation.ExportAttribute export);
</pre>
<a name="Namespace:_MonoTouch.Security" class="injected"></a>
<h2>Namespace: MonoTouch.Security</h2>
<a name="Type_Changed:_MonoTouch.Security.SecKey" class="injected"></a>
<h3>Type Changed: MonoTouch.Security.SecKey</h3>
<p>Removed:</p><pre>
 	public SecKey (IntPtr handle);
 	public SecKey (IntPtr handle, bool owns);
 	
</pre>
<a name="Namespace:_MonoTouch.StoreKit" class="injected"></a>
<h2>Namespace: MonoTouch.StoreKit</h2>
<a name="Type_Changed:_MonoTouch.StoreKit.SKPayment" class="injected"></a>
<h3>Type Changed: MonoTouch.StoreKit.SKPayment</h3>
<p>Removed:</p><pre>
 	public static SKPayment PaymentWithProduct (string identifier);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 5.0. Use PaymentWithProduct(SKProduct) after fetching the list of available products from SKProductRequest")]
	public static SKPayment PaymentWithProduct (string identifier);
</pre>
<a name="Namespace:_MonoTouch.SystemConfiguration" class="injected"></a>
<h2>Namespace: MonoTouch.SystemConfiguration</h2>
<a name="Type_Changed:_MonoTouch.SystemConfiguration.CaptiveNetwork" class="injected"></a>
<h3>Type Changed: MonoTouch.SystemConfiguration.CaptiveNetwork</h3>
<p>Removed:</p><pre>
 	[Obsolete("Replaced by TryCopyCurrentNetworkInfo")]
	public static MonoTouch.Foundation.NSDictionary CopyCurrentNetworkInfo (string interfaceName);
 	[Obsolete("Replaced by TryGetSupportedInterfaces")]
	public static string [] GetSupportedInterfaces ();
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSDictionary CopyCurrentNetworkInfo (string interfaceName);
 	public static string [] GetSupportedInterfaces ();
</pre>
<a name="Type_Changed:_MonoTouch.SystemConfiguration.NetworkReachability" class="injected"></a>
<h3>Type Changed: MonoTouch.SystemConfiguration.NetworkReachability</h3>
<p>Removed:</p><pre>
 	[Obsolete("Replaced by SetNotification")]
	public bool SetCallback (Notification callback);
</pre>
<p>Added:</p><pre>
 	public bool SetCallback (Notification callback);
</pre>
<a name="Namespace:_MonoTouch.UIKit" class="injected"></a>
<h2>Namespace: MonoTouch.UIKit</h2>
<a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>
<h3>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h3>
<p>Removed:</p><pre>
 	public virtual bool FinishedLaunching (UIApplication application, MonoTouch.Foundation.NSDictionary launcOptions);
</pre>
<p>Added:</p><pre>
 	public virtual bool FinishedLaunching (UIApplication application, MonoTouch.Foundation.NSDictionary launchOptions);
</pre>
<a name="Type_Changed:_MonoTouch.UIKit.UIBarButtonItem" class="injected"></a>
<h3>Type Changed: MonoTouch.UIKit.UIBarButtonItem</h3>
<p>Removed:</p><pre>
 	public UIBarButtonItem (UIView customView);
</pre>
<p>Added:</p><pre>
 	public UIBarButtonItem (UIView customView);
</pre>
<a name="Type_Changed:_MonoTouch.UIKit.UIDevice" class="injected"></a>
<h3>Type Changed: MonoTouch.UIKit.UIDevice</h3>
<p>Removed:</p><pre>
 	[Obsolete("Available, but deprecated in iOS5")]
	public virtual string UniqueIdentifier {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 5.0")]
	public virtual string UniqueIdentifier {
</pre>
<a name="Type_Changed:_MonoTouch.UIKit.UIEvent" class="injected"></a>
<h3>Type Changed: MonoTouch.UIKit.UIEvent</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSSet TouchesForGestureRecognizer (UIGestureRecognizer gesture);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSSet TouchesForGestureRecognizer (UIGestureRecognizer window);
</pre>
<a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerController" class="injected"></a>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerController</h3>
<p>Removed:</p><pre>
 	[Obsolete("deprecated in iPhoneOS 3.1")]
	public virtual bool AllowsImageEditing {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 3.1")]
	public virtual bool AllowsImageEditing {
</pre>
<a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Removed:</p><pre>
 	[Obsolete("Use the version with a `ref float actualFontSize`")]
	public System.Drawing.SizeF DrawString (string str, System.Drawing.PointF point, float width, UIFont font, float minFontSize, float actualFontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
</pre>
<p>Added:</p><pre>
 	public System.Drawing.SizeF DrawString (string str, System.Drawing.PointF point, float width, UIFont font, float minFontSize, float actualFontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
</pre>
</body>
</html>
