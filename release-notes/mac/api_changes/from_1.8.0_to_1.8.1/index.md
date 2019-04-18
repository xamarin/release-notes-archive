---
id: 079AEBE6-4493-4F7B-962C-9DABA50C3C1C
title: "From 1.8.0 to 1.8.1"
---

<html><head><title>API changes from Xamarin.Mac 1.8.0 to Xamarin.Mac 1.8.1</title></head>
<body>

<p>This document describes the API changes from Xamarin.Mac 1.8.0 to Xamarin.Mac 1.8.1</p>

<h1>XamMac.dll</h1>
<h2>Namespace MonoMac</h2>
<h3>Type Changed: MonoMac.Constants</h3>
<p>Added fields:</p><pre>
	public static const string ApplicationServicesCoreGraphicsLibrary = "/System/Library/Frameworks/ApplicationServices.framework/Frameworks/CoreGraphics.framework/CoreGraphics";
</pre>


<h2>Namespace MonoMac.AppKit</h2>
<h3>Type Changed: MonoMac.AppKit.NSButton</h3>
<p>Added methods:</p><pre>
	public virtual void SetShowsBorderOnlyWhileMouseInside (bool showsBorder);
</pre>

<h3>Type Changed: MonoMac.AppKit.NSNib</h3>
<p>Added methods:</p><pre>
	public virtual bool InstantiateNibWithOwner (MonoMac.Foundation.NSObject owner, MonoMac.Foundation.NSArray& topLevelObjects);
</pre>

<h3>Type Changed: MonoMac.AppKit.NSScrollView</h3>
<p>Added interfaces:</p><pre>
	INSTextFinderBarContainer
</pre>

<h3>New Type MonoMac.AppKit.INSTextFinderBarContainer</h3>
<pre>
public interface INSTextFinderBarContainer : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual NSView FindBarView { get; set; }
	public virtual bool FindBarVisible { get; set; }
	// methods
	public virtual void FindBarViewDidChangeHeight ();
}
</pre>
<h3>New Type MonoMac.AppKit.NSTextFinder</h3>
<pre>
public class NSTextFinder : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSTextFinder ();
	public NSTextFinder (MonoMac.Foundation.NSCoder coder);
	public NSTextFinder (MonoMac.Foundation.NSObjectFlag t);
	public NSTextFinder (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSTextFinderClient Client { set; }
	public virtual NSTextFinderBarContainer FindBarContainer { set; }
	public virtual bool FindIndicatorNeedsUpdate { get; set; }
	public virtual MonoMac.Foundation.NSArray IncrementalMatchRanges { get; }
	public virtual bool IncrementalSearchingEnabled { get; set; }
	// methods
	public virtual void CancelFindIndicator ();
	protected override void Dispose (bool disposing);
	public static void DrawIncrementalMatchHighlightInRect (System.Drawing.RectangleF rect);
	public virtual void NoteClientStringWillChange ();
	public virtual void PerformAction (NSTextFinderAction op);
	public virtual bool ValidateAction (NSTextFinderAction op);
}
</pre>
<h3>New Type MonoMac.AppKit.NSTextFinderBarContainer</h3>
<pre>
public abstract class NSTextFinderBarContainer : MonoMac.Foundation.NSObject, INSTextFinderBarContainer, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSTextFinderBarContainer ();
	public NSTextFinderBarContainer (MonoMac.Foundation.NSCoder coder);
	public NSTextFinderBarContainer (MonoMac.Foundation.NSObjectFlag t);
	public NSTextFinderBarContainer (System.IntPtr handle);
	// properties
	public virtual NSView FindBarView { get; set; }
	public virtual bool FindBarVisible { get; set; }
	// methods
	public virtual void FindBarViewDidChangeHeight ();
}
</pre>
<h3>New Type MonoMac.AppKit.NSTextFinderBarContainer_Extensions</h3>
<pre>
public static class NSTextFinderBarContainer_Extensions {
}
</pre>
<h3>New Type MonoMac.AppKit.NSTextFinderClient</h3>
<pre>
public abstract class NSTextFinderClient : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSTextFinderClient ();
	public NSTextFinderClient (MonoMac.Foundation.NSCoder coder);
	public NSTextFinderClient (MonoMac.Foundation.NSObjectFlag t);
	public NSTextFinderClient (System.IntPtr handle);
	// properties
	public virtual bool AllowsMultipleSelection { get; }
	public virtual bool Editable { get; }
	public virtual MonoMac.Foundation.NSRange FirstSelectedRange { get; }
	public virtual bool Selectable { get; }
	public virtual MonoMac.Foundation.NSArray SelectedRanges { get; set; }
	public virtual string String { get; }
	public virtual MonoMac.Foundation.NSArray VisibleCharacterRanges { get; }
	// methods
	public virtual NSView ContentViewAtIndexeffectiveCharacterRange (uint index, MonoMac.Foundation.NSRange& outRange);
	public virtual void DidReplaceCharacters ();
	public virtual void DrawCharactersInRangeforContentView (MonoMac.Foundation.NSRange range, NSView view);
	public virtual MonoMac.Foundation.NSArray RectsForCharacterRange (MonoMac.Foundation.NSRange range);
	public virtual void ReplaceCharactersInRangewithString (MonoMac.Foundation.NSRange range, string str);
	public virtual void ScrollRangeToVisible (MonoMac.Foundation.NSRange range);
	public virtual bool ShouldReplaceCharactersInRangeswithStrings (MonoMac.Foundation.NSArray ranges, MonoMac.Foundation.NSArray strings);
	public virtual string StringAtIndexeffectiveRangeendsWithSearchBoundary (uint characterIndex, MonoMac.Foundation.NSRange& outRange, bool outFlag);
	public virtual uint StringLength ();
}
</pre>

<h2>Namespace MonoMac.CoreBluetooth</h2>
<h3>Type Changed: MonoMac.CoreBluetooth.CBAdvertisement</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString DataOverflowServiceUUIDsKey { get; }
	public static MonoMac.Foundation.NSString DataSolicitedServiceUUIDsKey { get; }
	public static MonoMac.Foundation.NSString IsConnectable { get; }
</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.CBCentralManager</h3>
<p>Added constructors:</p><pre>
	public CBCentralManager (CBCentralManagerDelegate centralDelegate, MonoMac.CoreFoundation.DispatchQueue queue, MonoMac.Foundation.NSDictionary options);
</pre>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString OptionShowPowerAlertKey { get; }
	public static MonoMac.Foundation.NSString ScanOptionSolicitedServiceUUIDsKey { get; }
</pre>
<p>Added methods:</p><pre>
	public virtual CBPeripheral[] RetrieveConnectedPeripherals (CBUUID[] serviceUUIDs);
	public virtual CBPeripheral[] RetrievePeripheralsWithIdentifiers (MonoMac.Foundation.NSUuid[] identifiers);
</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.CBCharacteristic</h3>
<p>Removed properties:</p><pre>
	public virtual CBUUID UUID { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual CBCentral[] SubscribedCentrals { get; }
	public virtual CBUUID UUID { get; set; }
</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.CBService</h3>
<p>Added properties:</p><pre>
	public virtual bool Primary { get; }
</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.PeripheralConnectionOptions</h3>
<p>Removed properties:</p><pre>
	public bool NotifyOnDisconnectionKey { set; }
</pre>
<p>Added properties:</p><pre>
	public System.Boolean? NotifyOnDisconnection { get; set; }
	[Obsolete ("Use NotifyOnDisconnection property instead")]
	public bool NotifyOnDisconnectionKey { set; }

</pre>

<h3>New Type MonoMac.CoreBluetooth.CBATTRequest</h3>
<pre>
public class CBATTRequest : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBATTRequest (MonoMac.Foundation.NSCoder coder);
	public CBATTRequest (MonoMac.Foundation.NSObjectFlag t);
	public CBATTRequest (System.IntPtr handle);
	// properties
	public virtual CBCentral Central { get; }
	public virtual CBCharacteristic Characteristic { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int Offset { get; }
	public virtual MonoMac.Foundation.NSData Value { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBATTRequestEventArgs</h3>
<pre>
public class CBATTRequestEventArgs : System.EventArgs {
	// constructors
	public CBATTRequestEventArgs (CBATTRequest request);
	// properties
	public CBATTRequest Request { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBATTRequestsEventArgs</h3>
<pre>
public class CBATTRequestsEventArgs : System.EventArgs {
	// constructors
	public CBATTRequestsEventArgs (CBATTRequest[] requests);
	// properties
	public CBATTRequest[] Requests { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBCentral</h3>
<pre>
public class CBCentral : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBCentral (MonoMac.Foundation.NSCoder coder);
	public CBCentral (MonoMac.Foundation.NSObjectFlag t);
	public CBCentral (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSUuid Identifier { get; }
	public virtual uint MaximumUpdateValueLength { get; }
	[Obsolete ("Deprecated in iOS7")]
	public virtual System.IntPtr UUID { get; }

	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBMutableCharacteristic</h3>
<pre>
public class CBMutableCharacteristic : MonoMac.CoreBluetooth.CBCharacteristic, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBMutableCharacteristic (MonoMac.Foundation.NSCoder coder);
	public CBMutableCharacteristic (MonoMac.Foundation.NSObjectFlag t);
	public CBMutableCharacteristic (System.IntPtr handle);
	public CBMutableCharacteristic (CBUUID uuid, CBCharacteristicProperties properties, MonoMac.Foundation.NSData value, CBAttributePermissions permissions);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CBDescriptor[] Descriptors { get; set; }
	public virtual CBAttributePermissions Permissions { get; set; }
	public virtual CBCharacteristicProperties Properties { get; set; }
	public override CBUUID UUID { get; set; }
	public virtual MonoMac.Foundation.NSData Value { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBMutableDescriptor</h3>
<pre>
public class CBMutableDescriptor : MonoMac.CoreBluetooth.CBDescriptor, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBMutableDescriptor (MonoMac.Foundation.NSCoder coder);
	public CBMutableDescriptor (MonoMac.Foundation.NSObjectFlag t);
	public CBMutableDescriptor (System.IntPtr handle);
	public CBMutableDescriptor (CBUUID uuid, MonoMac.Foundation.NSObject descriptorValue);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBMutableService</h3>
<pre>
public class CBMutableService : MonoMac.CoreBluetooth.CBService, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBMutableService (MonoMac.Foundation.NSCoder coder);
	public CBMutableService (MonoMac.Foundation.NSObjectFlag t);
	public CBMutableService (System.IntPtr handle);
	public CBMutableService (CBUUID uuid, bool primary);
	// properties
	public virtual CBCharacteristic[] Characteristics { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual CBService[] IncludedServices { get; set; }
	public virtual bool Primary { get; set; }
	public virtual CBUUID UUID { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralManager</h3>
<pre>
public class CBPeripheralManager : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBPeripheralManager (MonoMac.Foundation.NSCoder coder);
	public CBPeripheralManager (MonoMac.Foundation.NSObjectFlag t);
	public CBPeripheralManager (System.IntPtr handle);
	public CBPeripheralManager (CBPeripheralManagerDelegate peripheralDelegate, MonoMac.CoreFoundation.DispatchQueue queue);
	public CBPeripheralManager (CBPeripheralManagerDelegate peripheralDelegate, MonoMac.CoreFoundation.DispatchQueue queue, MonoMac.Foundation.NSDictionary options);
	// properties
	public virtual bool Advertising { get; }
	public static CBPeripheralManagerAuthorizationStatus AuthorizationStatus { get; }
	public override System.IntPtr ClassHandle { get; }
	public CBPeripheralManagerDelegate Delegate { get; set; }
	public static MonoMac.Foundation.NSString OptionRestoreIdentifierKey { get; }
	public static MonoMac.Foundation.NSString OptionShowPowerAlertKey { get; }
	public static MonoMac.Foundation.NSString RestoredStateAdvertisementDataKey { get; }
	public static MonoMac.Foundation.NSString RestoredStateServicesKey { get; }
	public virtual CBPeripheralManagerState State { get; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler&lt;NSErrorEventArgs&gt; AdvertisingStarted;
	public event System.EventHandler&lt;CBPeripheralManagerSubscriptionEventArgs&gt; CharacteristicSubscribed;
	public event System.EventHandler&lt;CBPeripheralManagerSubscriptionEventArgs&gt; CharacteristicUnsubscribed;
	public event System.EventHandler&lt;CBATTRequestEventArgs&gt; ReadRequestReceived;
	public event System.EventHandler ReadyToUpdateSubscribers;
	public event System.EventHandler&lt;CBPeripheralManagerServiceEventArgs&gt; ServiceAdded;
	public event System.EventHandler StateUpdated;
	public event System.EventHandler&lt;CBWillRestoreEventArgs&gt; WillRestoreState;
	public event System.EventHandler&lt;CBATTRequestsEventArgs&gt; WriteRequestsReceived;
	// methods
	public virtual void AddService (CBMutableService service);
	protected override void Dispose (bool disposing);
	public virtual void RemoveAllServices ();
	public virtual void RemoveService (CBMutableService service);
	public virtual void RespondToRequest (CBATTRequest request, CBATTError result);
	public virtual void SetDesiredConnectionLatency (CBPeripheralManagerConnectionLatency latency, CBCentral connectedCentral);
	public void StartAdvertising (StartAdvertisingOptions options);
	public virtual void StartAdvertising (MonoMac.Foundation.NSDictionary options);
	public virtual void StopAdvertising ();
	public virtual bool UpdateValue (MonoMac.Foundation.NSData value, CBMutableCharacteristic characteristic, CBCentral[] subscribedCentrals);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralManagerDelegate</h3>
<pre>
public abstract class CBPeripheralManagerDelegate : MonoMac.Foundation.NSObject, ICBPeripheralManagerDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBPeripheralManagerDelegate ();
	public CBPeripheralManagerDelegate (MonoMac.Foundation.NSCoder coder);
	public CBPeripheralManagerDelegate (MonoMac.Foundation.NSObjectFlag t);
	public CBPeripheralManagerDelegate (System.IntPtr handle);
	// methods
	public virtual void AdvertisingStarted (CBPeripheralManager peripheral, MonoMac.Foundation.NSError error);
	public virtual void CharacteristicSubscribed (CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);
	public virtual void CharacteristicUnsubscribed (CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);
	public virtual void ReadRequestReceived (CBPeripheralManager peripheral, CBATTRequest request);
	public virtual void ReadyToUpdateSubscribers (CBPeripheralManager peripheral);
	public virtual void ServiceAdded (CBPeripheralManager peripheral, CBService service, MonoMac.Foundation.NSError error);
	public virtual void StateUpdated (CBPeripheralManager peripheral);
	public virtual void WillRestoreState (CBPeripheralManager peripheral, MonoMac.Foundation.NSDictionary dict);
	public virtual void WriteRequestsReceived (CBPeripheralManager peripheral, CBATTRequest[] requests);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralManagerDelegate_Extensions</h3>
<pre>
public static class CBPeripheralManagerDelegate_Extensions {
	// methods
	public static void AdvertisingStarted (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, MonoMac.Foundation.NSError error);
	public static void CharacteristicSubscribed (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);
	public static void CharacteristicUnsubscribed (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);
	public static void ReadRequestReceived (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBATTRequest request);
	public static void ReadyToUpdateSubscribers (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral);
	public static void ServiceAdded (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBService service, MonoMac.Foundation.NSError error);
	public static void WillRestoreState (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, MonoMac.Foundation.NSDictionary dict);
	public static void WriteRequestsReceived (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBATTRequest[] requests);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralManagerServiceEventArgs</h3>
<pre>
public class CBPeripheralManagerServiceEventArgs : System.EventArgs {
	// constructors
	public CBPeripheralManagerServiceEventArgs (CBService service, MonoMac.Foundation.NSError error);
	// properties
	public MonoMac.Foundation.NSError Error { get; set; }
	public CBService Service { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralManagerSubscriptionEventArgs</h3>
<pre>
public class CBPeripheralManagerSubscriptionEventArgs : System.EventArgs {
	// constructors
	public CBPeripheralManagerSubscriptionEventArgs (CBCentral central, CBCharacteristic characteristic);
	// properties
	public CBCentral Central { get; set; }
	public CBCharacteristic Characteristic { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.ICBPeripheralManagerDelegate</h3>
<pre>
public interface ICBPeripheralManagerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void StateUpdated (CBPeripheralManager peripheral);
}
</pre>

<h2>Namespace MonoMac.CoreData</h2>
<h3>Type Changed: MonoMac.CoreData.NSMergeConflict</h3>
<p>Removed interfaces:</p><pre>
	MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
</pre>


<h2>Namespace MonoMac.CoreFoundation</h2>
<h3>Type Changed: MonoMac.CoreFoundation.CFReadStream</h3>
<p>Removed methods:</p><pre>
	protected override bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, System.IntPtr context);
</pre>
<p>Added methods:</p><pre>
	protected override bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, System.IntPtr context);
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.CFRunLoop</h3>
<p>Removed fields:</p><pre>
	public static const string ModeCommon = "kCFRunLoopCommonModes";
	public static const string ModeDefault = "kCFRunLoopDefaultMode";
</pre>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString ModeCommon { get; }
	public static MonoMac.Foundation.NSString ModeDefault { get; }
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.CFStream</h3>
<p>Removed methods:</p><pre>
	protected virtual bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, System.IntPtr context);
</pre>
<p>Added methods:</p><pre>
	protected virtual bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, System.IntPtr context);
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.CFWriteStream</h3>
<p>Removed methods:</p><pre>
	protected override bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, System.IntPtr context);
</pre>
<p>Added methods:</p><pre>
	protected override bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, System.IntPtr context);
</pre>

<h3>New Type MonoMac.CoreFoundation.CFMachPort</h3>
<pre>
public class CFMachPort : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CFMachPort (System.IntPtr handle);
	public CFMachPort (System.IntPtr handle, bool ownsHandle);
	// properties
	public virtual System.IntPtr Handle { get; }
	public bool IsValid { get; }
	public System.IntPtr MachPort { get; }
	// methods
	protected override void ~CFMachPort ();
	public CFRunLoopSource CreateRunLoopSource ();
	public virtual void Dispose ();
	public virtual void Dispose (bool disposing);
	public void Invalidate ();
}
</pre>

<h2>Namespace MonoMac.CoreGraphics</h2>
<h3>New Type MonoMac.CoreGraphics.CGEvent</h3>
<pre>
public sealed class CGEvent : System.IDisposable, MonoMac.ObjCRuntime.INativeObject {
	// constructors
	public CGEvent (MonoMac.Foundation.NSData source);
	// properties
	public CGEventFlags Flags { get; }
	public virtual System.IntPtr Handle { get; }
	public System.Drawing.PointF Location { get; }
	public long MouseEventButtonNumber { get; }
	public long MouseEventClickState { get; }
	public long MouseEventDeltaX { get; }
	public long MouseEventDeltaY { get; }
	public bool MouseEventInstantMouser { get; }
	public long MouseEventNumber { get; }
	public double MouseEventPressure { get; }
	public long MouseEventSubtype { get; }
	// methods
	protected override void ~CGEvent ();
	public static System.IntPtr CGEventTapCreate (CGEventTapLocation location, CGEventTapPlacement place, CGEventTapOptions options, CGEventMask mask, CGEvent.CGEventTapCallback cback, System.IntPtr data);
	public CGEvent Copy ();
	public static MonoMac.CoreFoundation.CFMachPort CreateTap (CGEventTapLocation location, CGEventTapPlacement place, CGEventTapOptions options, CGEventMask mask, CGEvent.CGEventTapCallback cback, System.IntPtr data);
	public void Dispose (bool disposing);
	public virtual void Dispose ();
	public static CGEventFlags GetFlags (System.IntPtr eventHandle);
	public MonoMac.Foundation.NSData ToData ();

	// inner types
	public sealed delegate CGEventTapCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public CGEvent (object object, System.IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (System.IntPtr proxy, CGEventType eventType, System.IntPtr eventRef, System.IntPtr userInfo, System.AsyncCallback callback, object object);
		public virtual System.IntPtr EndInvoke (System.IAsyncResult result);
		public virtual System.IntPtr Invoke (System.IntPtr proxy, CGEventType eventType, System.IntPtr eventRef, System.IntPtr userInfo);
	}
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventFilterMask</h3>
<pre>
[Serializable]
[Flags]
public enum CGEventFilterMask {
	PermitLocalKeyboardEvents = 2,
	PermitLocalMouseEvents = 1,
	PermitSystemDefinedEvents = 4,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventFlags</h3>
<pre>
[Serializable]
[Flags]
public enum CGEventFlags {
	AlphaShift = 65536,
	Alternate = 524288,
	Command = 1048576,
	Control = 262144,
	Help = 4194304,
	NonCoalesced = 256,
	NumericPad = 2097152,
	SecondaryFn = 8388608,
	Shift = 131072,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventMask</h3>
<pre>
[Serializable]
[Flags]
public enum CGEventMask {
	FlagsChanged = 4096,
	KeyDown = 1024,
	KeyUp = 2048,
	LeftMouseDown = 2,
	LeftMouseDragged = 64,
	LeftMouseUp = 4,
	MouseMoved = 32,
	Null = 1,
	OtherMouseDown = 33554432,
	OtherMouseDragged = 134217728,
	OtherMouseUp = 67108864,
	RightMouseDown = 8,
	RightMouseDragged = 128,
	RightMouseUp = 16,
	ScrollWheel = 4194304,
	TabletPointer = 8388608,
	TabletProximity = 16777216,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventMouseSubtype</h3>
<pre>
[Serializable]
public enum CGEventMouseSubtype {
	Default = 0,
	TabletPoint = 1,
	TabletProximity = 2,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventSource</h3>
<pre>
public sealed class CGEventSource : System.IDisposable, MonoMac.ObjCRuntime.INativeObject {
	// constructors
	public CGEventSource (System.IntPtr handle);
	public CGEventSource (System.IntPtr handle, bool ownsHandle);
	public CGEventSource (CGEventSourceStateID stateID);
	// properties
	public virtual System.IntPtr Handle { get; }
	public int KeyboardType { get; set; }
	public double LocalEventsSupressionInterval { get; set; }
	public double PixelsPerLine { get; set; }
	public CGEventSourceStateID StateID { get; }
	public long UserData { get; set; }
	// methods
	protected override void ~CGEventSource ();
	public virtual void Dispose ();
	public void Dispose (bool disposing);
	public static bool GetButtonState (CGEventSourceStateID stateID, CGMouseButton button);
	public static uint GetCounterForEventType (CGEventSourceStateID stateID, CGEventType eventType);
	public static CGEventFlags GetFlagsState (CGEventSourceStateID stateID);
	public static bool GetKeyState (CGEventSourceStateID stateID, ushort keycode);
	public CGEventFilterMask GetLocalEventsFilterDuringSupressionState (CGEventSuppressionState state);
	public static double GetSecondsSinceLastEventType (CGEventSourceStateID stateID, CGEventType eventType);
	public void SetLocalEventsFilterDuringSupressionState (CGEventFilterMask filter, CGEventSuppressionState state);
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventSourceStateID</h3>
<pre>
[Serializable]
public enum CGEventSourceStateID {
	CombinedSession = 0,
	HidSystem = 1,
	Private = -1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventSuppressionState</h3>
<pre>
[Serializable]
public enum CGEventSuppressionState {
	RemoteMouseDrag = 1,
	SuppressionInterval = 0,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventTapLocation</h3>
<pre>
[Serializable]
public enum CGEventTapLocation {
	AnnotatedSession = 2,
	HID = 0,
	Session = 1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventTapOptions</h3>
<pre>
[Serializable]
public enum CGEventTapOptions {
	Default = 0,
	ListenOnly = 1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventTapPlacement</h3>
<pre>
[Serializable]
public enum CGEventTapPlacement {
	HeadInsert = 0,
	TailAppend = 1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventType</h3>
<pre>
[Serializable]
public enum CGEventType {
	FlagsChanged = 12,
	KeyDown = 10,
	KeyUp = 11,
	LeftMouseDown = 1,
	LeftMouseDragged = 6,
	LeftMouseUp = 2,
	MouseMoved = 5,
	Null = 0,
	OtherMouseDown = 25,
	OtherMouseDragged = 27,
	OtherMouseUp = 26,
	RightMouseDown = 3,
	RightMouseDragged = 7,
	RightMouseUp = 4,
	ScrollWheel = 22,
	TabletPointer = 23,
	TabletProximity = 24,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGMouseButton</h3>
<pre>
[Serializable]
public enum CGMouseButton {
	Center = 2,
	Left = 0,
	Right = 1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGScrollEventUnit</h3>
<pre>
[Serializable]
public enum CGScrollEventUnit {
	Line = 1,
	Pixel = 0,
}
</pre>

<h2>Namespace MonoMac.ObjCRuntime</h2>
<h3>Type Changed: MonoMac.ObjCRuntime.AvailabilityAttribute</h3>
<p>Added properties:</p><pre>
	public Platform DeprecatedArchitecture { get; }
	public Platform DeprecatedVersion { get; }
	public Platform IntroducedArchitecture { get; }
	public Platform IntroducedVersion { get; }
	public Platform ObsoletedArchitecture { get; }
	public Platform ObsoletedVersion { get; }
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.LionAttribute</h3>
<p>Added constructors:</p><pre>
	public LionAttribute (bool onlyOn64);
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.MavericksAttribute</h3>
<p>Added constructors:</p><pre>
	public MavericksAttribute (bool onlyOn64);
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.Messaging</h3>
<p>Added methods:</p><pre>
	public static System.IntPtr IntPtr_objc_msgSend_UInt32_ref_NSRange (System.IntPtr receiver, System.IntPtr selector, uint arg1, MonoMac.Foundation.NSRange& arg2);
	public static System.IntPtr IntPtr_objc_msgSend_UInt32_ref_NSRange_bool (System.IntPtr receiver, System.IntPtr selector, uint arg1, MonoMac.Foundation.NSRange& arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_UInt32_ref_NSRange (System.IntPtr receiver, System.IntPtr selector, uint arg1, MonoMac.Foundation.NSRange& arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_UInt32_ref_NSRange_bool (System.IntPtr receiver, System.IntPtr selector, uint arg1, MonoMac.Foundation.NSRange& arg2, bool arg3);
	public static void void_objc_msgSend_int_int_IntPtr_int_int_int_int_bool_bool_bool_bool (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, int arg4, int arg5, int arg6, int arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static void void_objc_msgSend_IntPtr_bool_bool_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, System.IntPtr arg4, int arg5);
	public static void void_objc_msgSend_IntPtr_bool_bool_IntPtr_int_int_int_int_int_bool_bool_bool_bool_UInt16_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, System.IntPtr arg4, int arg5, int arg6, int arg7, int arg8, int arg9, bool arg10, bool arg11, bool arg12, bool arg13, ushort arg14, System.IntPtr arg15);
	public static void void_objc_msgSend_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, System.IntPtr arg4, System.IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10);
	public static void void_objc_msgSend_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, System.IntPtr arg4, System.IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static void void_objc_msgSend_UInt16 (System.IntPtr receiver, System.IntPtr selector, ushort arg1);
	public static void void_objc_msgSend_UInt16_bool_bool (System.IntPtr receiver, System.IntPtr selector, ushort arg1, bool arg2, bool arg3);
	public static void void_objc_msgSendSuper_int_int_IntPtr_int_int_int_int_bool_bool_bool_bool (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, int arg4, int arg5, int arg6, int arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static void void_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, System.IntPtr arg4, int arg5);
	public static void void_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_int_int_int_int_int_bool_bool_bool_bool_UInt16_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, System.IntPtr arg4, int arg5, int arg6, int arg7, int arg8, int arg9, bool arg10, bool arg11, bool arg12, bool arg13, ushort arg14, System.IntPtr arg15);
	public static void void_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, System.IntPtr arg4, System.IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10);
	public static void void_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, System.IntPtr arg4, System.IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static void void_objc_msgSendSuper_UInt16 (System.IntPtr receiver, System.IntPtr selector, ushort arg1);
	public static void void_objc_msgSendSuper_UInt16_bool_bool (System.IntPtr receiver, System.IntPtr selector, ushort arg1, bool arg2, bool arg3);
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.MountainLionAttribute</h3>
<p>Added constructors:</p><pre>
	public MountainLionAttribute (bool onlyOn64);
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.Platform</h3>
<p>Removed values:</p><pre>
	iOS = 4294967295,
	Mac = 18446744069414584320,
</pre>
<p>Added values:</p><pre>
	[Obsolete ("Use iOS_Version")]
	iOS = 4294967295,

	iOS_8_0 = 524288,
	iOS_Arch = 4278190080,
	iOS_Arch32 = 16777216,
	iOS_Arch64 = 33554432,
	iOS_Version = 16777215,
	[Obsolete ("Use Mac_Version")]
	Mac = 18446744069414584320,

	Mac_10_0 = 2814749767106560,
	Mac_10_1 = 2815849278734336,
	Mac_10_2 = 2816948790362112,
	Mac_10_3 = 2818048301989888,
	Mac_10_4 = 2819147813617664,
	Mac_10_5 = 2820247325245440,
	Mac_Arch = 18374686479671623680,
	Mac_Arch32 = 72057594037927936,
	Mac_Arch64 = 144115188075855872,
	Mac_Version = 72057589742960640,
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.PlatformHelper</h3>
<p>Removed methods:</p><pre>
	public static int CompareIos (Platform a, Platform b);
	public static int CompareMac (Platform a, Platform b);
	public static Platform ToIos (Platform platform);
	public static Platform ToMac (Platform platform);
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("UseCompareIosVersion")]
	public static int CompareIos (Platform a, Platform b);

	public static int CompareIosVersion (Platform a, Platform b);
	[Obsolete ("Use CompareMacVersion")]
	public static int CompareMac (Platform a, Platform b);

	public static int CompareMacVersion (Platform a, Platform b);
	public static Platform ToArch (Platform platform);
	[Obsolete ("Use ToIosVersion")]
	public static Platform ToIos (Platform platform);

	public static Platform ToIosArch (Platform platform);
	public static Platform ToIosVersion (Platform platform);
	[Obsolete ("Use ToMacVersion")]
	public static Platform ToMac (Platform platform);

	public static Platform ToMacArch (Platform platform);
	public static Platform ToMacVersion (Platform platform);
	public static Platform ToVersion (Platform platform);
</pre>

<h3>New Type MonoMac.ObjCRuntime.iOSAttribute</h3>
<pre>
public sealed class iOSAttribute : MonoMac.ObjCRuntime.AvailabilityAttribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public iOSAttribute (byte major, byte minor);
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.MacAttribute</h3>
<pre>
public sealed class MacAttribute : MonoMac.ObjCRuntime.AvailabilityAttribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public MacAttribute (byte major, byte minor, bool onlyOn64);
}
</pre>

<h2>Namespace MonoMac.Security</h2>
<h3>Type Changed: MonoMac.Security.SecAccessible</h3>
<p>Added values:</p><pre>
	Invalid = -1,
</pre>

<h3>Type Changed: MonoMac.Security.SecAuthenticationType</h3>
<p>Added values:</p><pre>
	Invalid = -1,
</pre>

<h3>Type Changed: MonoMac.Security.SecKey</h3>
<p>Removed methods:</p><pre>
	public SecStatusCode Decrypt (SecPadding padding, System.Byte[] cipherText, System.Byte[] plainText);
	public SecStatusCode Decrypt (SecPadding padding, System.IntPtr cipherText, int cipherLen, System.IntPtr plainText, int playLen);
	public SecStatusCode Encrypt (SecPadding padding, System.IntPtr plainText, int playLen, System.IntPtr cipherText, int cipherLen);
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Use the Decrypt overload which returns (out) the plainText array so you can adjust it if needed")]
	public SecStatusCode Decrypt (SecPadding padding, System.Byte[] cipherText, System.Byte[] plainText);

	[Obsolete ("Use the Decrypt overload which returns (ref) the plainTextLen value so you can adjust it if needed")]
	public SecStatusCode Decrypt (SecPadding padding, System.IntPtr cipherText, int cipherTextLen, System.IntPtr plainText, int plainTextLen);

	public SecStatusCode Decrypt (SecPadding padding, System.Byte[] cipherText, System.Byte[]& plainText);
	public SecStatusCode Decrypt (SecPadding padding, System.IntPtr cipherText, int cipherTextLen, System.IntPtr plainText, System.Int32& plainTextLen);
	public SecStatusCode Encrypt (SecPadding padding, System.IntPtr plainText, int plainTextLen, System.IntPtr cipherText, System.Int32& cipherTextLen);
	[Obsolete ("Use the Encrypt overload which returns (out) the cipherTextLen value so you can adjust it if needed")]
	public SecStatusCode Encrypt (SecPadding padding, System.IntPtr plainText, int plainTextLen, System.IntPtr cipherText, int cipherTextLen);

	public SecStatusCode RawSign (SecPadding padding, System.Byte[] dataToSign, System.Byte[]& result);
	public SecStatusCode RawSign (SecPadding padding, System.IntPtr dataToSign, int dataToSignLen, System.Byte[]& result);
</pre>

<h3>Type Changed: MonoMac.Security.SecKeyClass</h3>
<p>Added values:</p><pre>
	Invalid = -1,
</pre>

<h3>Type Changed: MonoMac.Security.SecKeyType</h3>
<p>Added values:</p><pre>
	Invalid = -1,
</pre>

<h3>Type Changed: MonoMac.Security.SecProtocol</h3>
<p>Added values:</p><pre>
	Invalid = -1,
</pre>

<h3>Type Changed: MonoMac.Security.SecRecord</h3>
<p>Added methods:</p><pre>
	public MonoMac.Foundation.NSDictionary ToDictionary ();
</pre>

<h3>Type Changed: MonoMac.Security.SslProtocol</h3>
<p>Removed values:</p><pre>
	Ssl3_0 = 2,
</pre>
<p>Added values:</p><pre>
	Ssl_3_0 = 2,
	[Obsolete ("Use Ssl_3_0")]
	Ssl3_0 = 2,

</pre>

<h3>New Type MonoMac.Security.SslAuthenticate</h3>
<pre>
[Serializable]
public enum SslAuthenticate {
	Always = 1,
	Never = 0,
	Try = 2,
}
</pre>
<h3>New Type MonoMac.Security.SslCipherSuite</h3>
<pre>
[Serializable]
public enum SslCipherSuite {
	SSL_DH_anon_EXPORT_WITH_RC4_40_MD5 = 23,
	SSL_DH_anon_WITH_3DES_EDE_CBC_SHA = 27,
	SSL_DH_anon_WITH_RC4_128_MD5 = 24,
	SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA = 22,
	SSL_NULL_WITH_NULL_NULL = 0,
	SSL_RSA_EXPORT_WITH_RC4_40_MD5 = 3,
	SSL_RSA_WITH_3DES_EDE_CBC_SHA = 10,
	SSL_RSA_WITH_NULL_MD5 = 1,
	SSL_RSA_WITH_NULL_SHA = 2,
	SSL_RSA_WITH_RC4_128_MD5 = 4,
	SSL_RSA_WITH_RC4_128_SHA = 5,
	TLS_DH_anon_WITH_3DES_EDE_CBC_SHA = 27,
	TLS_DH_anon_WITH_AES_128_CBC_SHA = 52,
	TLS_DH_anon_WITH_AES_128_CBC_SHA256 = 108,
	TLS_DH_anon_WITH_AES_128_GCM_SHA256 = 166,
	TLS_DH_anon_WITH_AES_256_CBC_SHA = 58,
	TLS_DH_anon_WITH_AES_256_CBC_SHA256 = 109,
	TLS_DH_anon_WITH_AES_256_GCM_SHA384 = 167,
	TLS_DH_anon_WITH_RC4_128_MD5 = 24,
	TLS_DHE_RSA_WITH_3DES_EDE_CBC_SHA = 22,
	TLS_DHE_RSA_WITH_AES_128_CBC_SHA = 51,
	TLS_DHE_RSA_WITH_AES_128_CBC_SHA256 = 103,
	TLS_DHE_RSA_WITH_AES_256_CBC_SHA = 57,
	TLS_DHE_RSA_WITH_AES_256_CBC_SHA256 = 107,
	TLS_ECDH_ECDSA_WITH_3DES_EDE_CBC_SHA = 49155,
	TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA = 49156,
	TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA256 = 49189,
	TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA = 49157,
	TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA384 = 49190,
	TLS_ECDH_ECDSA_WITH_NULL_SHA = 49153,
	TLS_ECDH_ECDSA_WITH_RC4_128_SHA = 49154,
	TLS_ECDH_RSA_WITH_3DES_EDE_CBC_SHA = 49165,
	TLS_ECDH_RSA_WITH_AES_128_CBC_SHA = 49166,
	TLS_ECDH_RSA_WITH_AES_128_CBC_SHA256 = 49193,
	TLS_ECDH_RSA_WITH_AES_256_CBC_SHA = 49167,
	TLS_ECDH_RSA_WITH_AES_256_CBC_SHA384 = 49194,
	TLS_ECDH_RSA_WITH_NULL_SHA = 49163,
	TLS_ECDH_RSA_WITH_RC4_128_SHA = 49164,
	TLS_ECDHE_ECDSA_WITH_3DES_EDE_CBC_SHA = 49160,
	TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA = 49161,
	TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256 = 49187,
	TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA = 49162,
	TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384 = 49188,
	TLS_ECDHE_ECDSA_WITH_NULL_SHA = 49158,
	TLS_ECDHE_ECDSA_WITH_RC4_128_SHA = 49159,
	TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA = 49170,
	TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA = 49171,
	TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 = 49191,
	TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA = 49172,
	TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 = 49192,
	TLS_ECDHE_RSA_WITH_NULL_SHA = 49168,
	TLS_ECDHE_RSA_WITH_RC4_128_SHA = 49169,
	TLS_NULL_WITH_NULL_NULL = 0,
	TLS_PSK_WITH_3DES_EDE_CBC_SHA = 139,
	TLS_PSK_WITH_AES_128_CBC_SHA = 140,
	TLS_PSK_WITH_AES_128_CBC_SHA256 = 174,
	TLS_PSK_WITH_AES_256_CBC_SHA = 141,
	TLS_PSK_WITH_AES_256_CBC_SHA384 = 175,
	TLS_PSK_WITH_NULL_SHA = 44,
	TLS_PSK_WITH_NULL_SHA256 = 176,
	TLS_PSK_WITH_NULL_SHA384 = 177,
	TLS_PSK_WITH_RC4_128_SHA = 138,
	TLS_RSA_WITH_3DES_EDE_CBC_SHA = 10,
	TLS_RSA_WITH_AES_128_CBC_SHA = 47,
	TLS_RSA_WITH_AES_128_CBC_SHA256 = 60,
	TLS_RSA_WITH_AES_256_CBC_SHA = 53,
	TLS_RSA_WITH_AES_256_CBC_SHA256 = 61,
	TLS_RSA_WITH_NULL_MD5 = 1,
	TLS_RSA_WITH_NULL_SHA = 2,
	TLS_RSA_WITH_NULL_SHA256 = 59,
	TLS_RSA_WITH_RC4_128_MD5 = 4,
	TLS_RSA_WITH_RC4_128_SHA = 5,
}
</pre>
<h3>New Type MonoMac.Security.SslClientCertificateState</h3>
<pre>
[Serializable]
public enum SslClientCertificateState {
	None = 0,
	Rejected = 3,
	Requested = 1,
	Sent = 2,
}
</pre>
<h3>New Type MonoMac.Security.SslConnection</h3>
<pre>
public abstract class SslConnection : System.IDisposable {
	// constructors
	protected SslConnection ();
	// properties
	public System.IntPtr ConnectionId { get; }
	// methods
	protected override void ~SslConnection ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public virtual SslStatus Read (System.IntPtr data, System.Int32& dataLength);
	public virtual SslStatus Write (System.IntPtr data, System.Int32& dataLength);
}
</pre>
<h3>New Type MonoMac.Security.SslConnectionType</h3>
<pre>
[Serializable]
public enum SslConnectionType {
	Datagram = 1,
	Stream = 0,
}
</pre>
<h3>New Type MonoMac.Security.SslContext</h3>
<pre>
public class SslContext : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SslContext (SslProtocolSide protocolSide, SslConnectionType connectionType);
	// properties
	public int BufferedReadSize { get; }
	public SslClientCertificateState ClientCertificateState { get; }
	public SslConnection Connection { get; set; }
	public int DatagramWriteSize { get; }
	public virtual System.IntPtr Handle { get; }
	public int MaxDatagramRecordSize { get; set; }
	[Obsolete ("Deprecated in 10.8")]
	public SslProtocol MaxProtocol { get; set; }

	[Obsolete ("Deprecated in 10.8")]
	public SslProtocol MinProtocol { get; set; }

	public SslCipherSuite NegotiatedCipher { get; }
	public SslProtocol NegotiatedProtocol { get; }
	public string PeerDomainName { get; set; }
	public System.Byte[] PeerId { get; set; }
	public SecTrust PeerTrust { get; }
	public SslSessionState SessionState { get; }
	// methods
	protected override void ~SslContext ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public System.Collections.Generic.IList&lt;SslCipherSuite&gt; GetEnabledCiphers ();
	public SslStatus GetLastStatus ();
	public SslStatus GetSessionOption (SslSessionOption option, System.Boolean& value);
	public System.Collections.Generic.IList&lt;SslCipherSuite&gt; GetSupportedCiphers ();
	public static System.IntPtr GetTypeId ();
	public SslStatus Handshake ();
	public SslStatus Read (System.Byte[] data, System.Int32& processed);
	public SslStatus SetCertificate (SecIdentity identify, System.Collections.Generic.IEnumerable&lt;SecCertificate&gt; certificates);
	public SslStatus SetClientSideAuthenticate (SslAuthenticate auth);
	public SslStatus SetDatagramHelloCookie (System.Byte[] cookie);
	public SslStatus SetEnabledCiphers (System.Collections.Generic.IEnumerable&lt;SslCipherSuite&gt; ciphers);
	public SslStatus SetEncryptionCertificate (SecIdentity identify, System.Collections.Generic.IEnumerable&lt;SecCertificate&gt; certificates);
	public SslStatus SetSessionOption (SslSessionOption option, bool value);
	public SslStatus Write (System.Byte[] data, System.Int32& processed);
}
</pre>
<h3>New Type MonoMac.Security.SslProtocolSide</h3>
<pre>
[Serializable]
public enum SslProtocolSide {
	Client = 1,
	Server = 0,
}
</pre>
<h3>New Type MonoMac.Security.SslSessionOption</h3>
<pre>
[Serializable]
public enum SslSessionOption {
	BreakOnCertRequested = 1,
	BreakOnClientAuth = 2,
	BreakOnServerAuth = 0,
	FalseStart = 3,
	SendOneByteRecord = 4,
}
</pre>
<h3>New Type MonoMac.Security.SslSessionState</h3>
<pre>
[Serializable]
public enum SslSessionState {
	Aborted = 4,
	Closed = 3,
	Connected = 2,
	Handshake = 1,
	Idle = 0,
	Invalid = -1,
}
</pre>
<h3>New Type MonoMac.Security.SslStatus</h3>
<pre>
[Serializable]
public enum SslStatus {
	BadCert = -9808,
	BadCipherSuite = -9818,
	BadConfiguration = -9848,
	BadRecordMac = -9846,
	BufferOverflow = -9817,
	CertExpired = -9814,
	CertNotYetValid = -9815,
	ClosedAbort = -9806,
	ClosedGraceful = -9805,
	ClosedNotNotified = -9816,
	ConnectionRefused = -9844,
	Crypto = -9809,
	DecryptionFail = -9845,
	FatalAlert = -9802,
	HostNameMismatch = -9843,
	IllegalParam = -9830,
	Internal = -9810,
	ModuleAttach = -9811,
	Negotiation = -9801,
	NoRootCert = -9813,
	PeerAccessDenied = -9832,
	PeerAuthCompleted = -9841,
	PeerBadCert = -9825,
	PeerBadRecordMac = -9820,
	PeerCertExpired = -9828,
	PeerCertRevoked = -9827,
	PeerCertUnknown = -9829,
	PeerClientCertRequested = -9842,
	PeerDecodeError = -9833,
	PeerDecompressFail = -9823,
	PeerDecryptError = -9834,
	PeerDecryptionFail = -9821,
	PeerExportRestriction = -9835,
	PeerHandshakeFail = -9824,
	PeerInsufficientSecurity = -9837,
	PeerInternalError = -9838,
	PeerNoRenegotiation = -9840,
	PeerProtocolVersion = -9836,
	PeerRecordOverflow = -9822,
	PeerUnexpectedMsg = -9819,
	PeerUnknownCA = -9831,
	PeerUnsupportedCert = -9826,
	PeerUserCancelled = -9839,
	Protocol = -9800,
	RecordOverflow = -9847,
	SessionNotFound = -9804,
	Success = 0,
	UnexpectedRecord = -9849,
	UnknownRootCert = -9812,
	WouldBlock = -9803,
	XCertChainInvalid = -9807,
}
</pre>
<h3>New Type MonoMac.Security.SslStreamConnection</h3>
<pre>
public class SslStreamConnection : MonoMac.Security.SslConnection, System.IDisposable {
	// constructors
	public SslStreamConnection (System.IO.Stream stream);
	// properties
	public System.IO.Stream InnerStream { get; }
	// methods
	public override SslStatus Read (System.IntPtr data, System.Int32& dataLength);
	public override SslStatus Write (System.IntPtr data, System.Int32& dataLength);
}
</pre>

<h2>Namespace MonoMac.WebKit</h2>
<h3>Type Changed: MonoMac.WebKit.DomAttr</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomCDataSection</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomCharacterData</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomComment</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomDocument</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomDocumentFragment</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomDocumentType</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomElement</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>
<p>Added properties:</p><pre>
	public virtual string ClassName { get; set; }
	public virtual DomCssStyleDeclaration Style { get; }
	public virtual string TagName { get; }
</pre>
<p>Added methods:</p><pre>
	public virtual void WebKitRequestFullScreen (ushort flags);
</pre>

<h3>Type Changed: MonoMac.WebKit.DomEntityReference</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomEvent</h3>
<p>Removed properties:</p><pre>
	public virtual MonoMac.Foundation.NSObject CurrentTarget { get; }
	public virtual MonoMac.Foundation.NSObject SourceElement { get; }
	public virtual MonoMac.Foundation.NSObject Target { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual DomEventTarget CurrentTarget { get; }
	public virtual DomEventTarget SourceElement { get; }
	public virtual DomEventTarget Target { get; }
</pre>

<h3>Type Changed: MonoMac.WebKit.DomHtmlDocument</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomHtmlElement</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>
<p>Removed properties:</p><pre>
	public virtual string ClassName { get; set; }
</pre>

<h3>Type Changed: MonoMac.WebKit.DomHtmlFormElement</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomHtmlInputElement</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomHtmlTextAreaElement</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomNode</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>
<p>Added methods:</p><pre>
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
</pre>

<h3>Type Changed: MonoMac.WebKit.DomProcessingInstruction</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>Type Changed: MonoMac.WebKit.DomText</h3>
<p>Added interfaces:</p><pre>
	IDomEventTarget
</pre>

<h3>New Type MonoMac.WebKit.DomDelta</h3>
<pre>
[Serializable]
public enum DomDelta {
	Line = 1,
	Page = 2,
	Pixel = 0,
}
</pre>
<h3>New Type MonoMac.WebKit.DomEventTarget</h3>
<pre>
public class DomEventTarget : MonoMac.Foundation.NSObject, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public DomEventTarget ();
	public DomEventTarget (MonoMac.Foundation.NSCoder coder);
	public DomEventTarget (MonoMac.Foundation.NSObjectFlag t);
	public DomEventTarget (System.IntPtr handle);
	// methods
	public virtual void AddEventListener (string type, DomEventListener listener, bool useCapture);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual bool DispatchEvent (DomEvent evt);
	public virtual void RemoveEventListener (string type, DomEventListener listener, bool useCapture);
}
</pre>
<h3>New Type MonoMac.WebKit.DomEventTarget_Extensions</h3>
<pre>
public static class DomEventTarget_Extensions {
	// methods
	public static void AddEventListener (IDomEventTarget This, string type, DomEventListener listener, bool useCapture);
	public static bool DispatchEvent (IDomEventTarget This, DomEvent evt);
	public static void RemoveEventListener (IDomEventTarget This, string type, DomEventListener listener, bool useCapture);
}
</pre>
<h3>New Type MonoMac.WebKit.DomKeyboardEvent</h3>
<pre>
public class DomKeyboardEvent : MonoMac.WebKit.DomUIEvent, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public DomKeyboardEvent (MonoMac.Foundation.NSCoder coder);
	public DomKeyboardEvent (MonoMac.Foundation.NSObjectFlag t);
	public DomKeyboardEvent (System.IntPtr handle);
	// properties
	public virtual bool AltGraphKey { get; }
	public virtual bool AltKey { get; }
	public virtual int CharCode { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool CtrlKey { get; }
	public virtual int KeyCode { get; }
	public virtual string KeyIdentifier { get; }
	public virtual DomKeyLocation KeyLocation { get; }
	public virtual bool MetaKey { get; }
	public virtual bool ShiftKey { get; }
	// methods
	public virtual bool GetModifierState (string keyIdentifier);
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
}
</pre>
<h3>New Type MonoMac.WebKit.DomKeyLocation</h3>
<pre>
[Serializable]
public enum DomKeyLocation {
	Left = 1,
	NumberPad = 3,
	Right = 2,
	Standard = 0,
}
</pre>
<h3>New Type MonoMac.WebKit.DomMouseEvent</h3>
<pre>
public class DomMouseEvent : MonoMac.WebKit.DomUIEvent, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public DomMouseEvent (MonoMac.Foundation.NSCoder coder);
	public DomMouseEvent (MonoMac.Foundation.NSObjectFlag t);
	public DomMouseEvent (System.IntPtr handle);
	// properties
	public virtual bool AltKey { get; }
	public virtual ushort Button { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int ClientX { get; }
	public virtual int ClientY { get; }
	public virtual bool CtrlKey { get; }
	public virtual DomNode FromElement { get; }
	public virtual bool MetaKey { get; }
	public virtual int OffsetX { get; }
	public virtual int OffsetY { get; }
	public virtual DomEventTarget RelatedTarget { get; }
	public virtual int ScreenX { get; }
	public virtual int ScreenY { get; }
	public virtual bool ShiftKey { get; }
	public virtual DomNode ToElement { get; }
	public virtual int X { get; }
	public virtual int Y { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, DomEventTarget relatedTarget);
}
</pre>
<h3>New Type MonoMac.WebKit.DomOverflowEvent</h3>
<pre>
public class DomOverflowEvent : MonoMac.WebKit.DomEvent, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public DomOverflowEvent (MonoMac.Foundation.NSCoder coder);
	public DomOverflowEvent (MonoMac.Foundation.NSObjectFlag t);
	public DomOverflowEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool HasHorizontalOverflow { get; }
	public virtual bool HasVerticalOverflow { get; }
	public virtual ushort Orient { get; }
	// methods
	public virtual void InitEvent (ushort orient, bool hasHorizontalOverflow, bool hasVerticalOverflow);
}
</pre>
<h3>New Type MonoMac.WebKit.DomProgressEvent</h3>
<pre>
public class DomProgressEvent : MonoMac.WebKit.DomEvent, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public DomProgressEvent (MonoMac.Foundation.NSCoder coder);
	public DomProgressEvent (MonoMac.Foundation.NSObjectFlag t);
	public DomProgressEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsLengthComputable { get; }
	public virtual ulong Loaded { get; }
	public virtual ulong Total { get; }
}
</pre>
<h3>New Type MonoMac.WebKit.DomUIEvent</h3>
<pre>
public class DomUIEvent : MonoMac.WebKit.DomEvent, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public DomUIEvent (MonoMac.Foundation.NSCoder coder);
	public DomUIEvent (MonoMac.Foundation.NSObjectFlag t);
	public DomUIEvent (System.IntPtr handle);
	// properties
	public virtual int CharCode { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int Detail { get; }
	public virtual int KeyCode { get; }
	public virtual int LayerX { get; }
	public virtual int LayerY { get; }
	public virtual int PageX { get; }
	public virtual DomAbstractView View { get; }
	public virtual int Which { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail);
}
</pre>
<h3>New Type MonoMac.WebKit.DomWheelEvent</h3>
<pre>
public class DomWheelEvent : MonoMac.WebKit.DomMouseEvent, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public DomWheelEvent (MonoMac.Foundation.NSCoder coder);
	public DomWheelEvent (MonoMac.Foundation.NSObjectFlag t);
	public DomWheelEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsHorizontal { get; }
	public virtual DomDelta WheelDelta { get; }
	public virtual int WheelDeltaX { get; }
	public virtual int WheelDeltaY { get; }
	// methods
	public virtual void InitEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
}
</pre>
<h3>New Type MonoMac.WebKit.IDomEventTarget</h3>
<pre>
public interface IDomEventTarget : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

</body>
</html>
