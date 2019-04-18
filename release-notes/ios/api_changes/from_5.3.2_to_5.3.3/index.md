---
id: 99E97ED6-8A28-17CD-43D2-6BDC868ED7A7
title: "From 5.3.2 to 5.3.3"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.3.2";
```

Added:

```
public const string Version = "5.3.3";
        public const string NewsstandKitLibrary = "/System/Library/Frameworks/NewsstandKit.framework/NewsstandKit";
        public const string ExternalAccessoryLibrary = "/System/Library/Frameworks/ExternalAccessory.framework/ExternalAccessory";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAsset

Added:

```
public virtual void LoadValuesAsynchronously (string [] keys, MonoTouch.Foundation.NSAction handler);
        public virtual AVKeyValueStatus StatusOfValue (string key, out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveSubjectAreaDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWasConnected (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWasDisconnected (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureInput

Added:

```
public static MonoTouch.Foundation.NSString PortFormatDescriptionDidChangeNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObservePortFormatDescriptionDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureSession

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidStartRunning (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidStopRunning (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveInterruptionEnded (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveRuntimeError (EventHandler<AVCaptureSessionRuntimeErrorEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWasInterrupted (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureSessionRuntimeErrorEventArgs 

Added:

```
public class AVCaptureSessionRuntimeErrorEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public AVCaptureSessionRuntimeErrorEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MonoTouch.Foundation.NSError Error {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureVideoOrientation" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureVideoOrientation

Removed:

```
LandscapeLeft,
        LandscapeRight
```

Added:

```
LandscapeRight,
        LandscapeLeft
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItem

Removed:

```
public static MonoTouch.Foundation.NSString DidPLayToEndTimeNotification {
```

Added:

```
public static MonoTouch.Foundation.NSString DidPlayToEndTimeNotification {
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidPlayToEndTime (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveItemFailedToPlayToEndTime (EventHandler<AVPlayerItemErrorEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTimeJumped (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItemErrorEventArgs" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItemErrorEventArgs

Added:

```
public class AVPlayerItemErrorEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public AVPlayerItemErrorEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MonoTouch.Foundation.NSError Error {
                get;
        }
 }
```

 <a name="Namespace:_MonoTouch.Accounts" class="injected"></a>


# Namespace: MonoTouch.Accounts

 <a name="Type_Changed:_MonoTouch.Accounts.ACAccountStore" class="injected"></a>


## Type Changed: MonoTouch.Accounts.ACAccountStore

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsLibrary" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveChanged (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioBufferList" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioBufferList

Added:

```
public AudioBufferList (int count);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFile" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFile

Added:

```
public AudioStreamPacketDescription[] ReadPacketData (bool useCache, long inStartingPacket, ref int nPackets, byte [] buffer, int offset, ref int count);
        public AudioStreamPacketDescription[] ReadPacketData (bool useCache, long inStartingPacket, ref int nPackets, IntPtr buffer, ref int count);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueue

Added:

```
public AudioQueueStatus AllocateBuffer (int bufferSize, out AudioQueueBuffer* audioQueueBuffer);
        public AudioQueueStatus EnqueueBuffer (AudioQueueBuffer* audioQueueBuffer, AudioStreamPacketDescription[] desc);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.OutputAudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.OutputAudioQueue

Added:

```
public OutputAudioQueue (AudioStreamBasicDescription desc, MonoTouch.CoreFoundation.CFRunLoop runLoop, MonoTouch.CoreFoundation.CFString runMode);
        public AudioQueueStatus DisableOfflineRender ();
        public AudioQueueStatus RenderOffline (double timeStamp, AudioQueueBuffer* audioQueueBuffer, int frameCount);
        public AudioQueueStatus SetOfflineRenderFormat (AudioStreamBasicDescription desc, AudioChannelLayout layout);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.OutputCompletedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.OutputCompletedEventArgs

Added:

```
public OutputCompletedEventArgs (AudioQueueBuffer* audioQueueBuffer);
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CALayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CALayer

Removed:

```
public virtual System.Drawing.RectangleF ConvertRectfromLayer (System.Drawing.RectangleF rect, CALayer layer);
        public virtual double ConvertTimeFromLayer (double rect, CALayer layer);
        public virtual double ConvertTimeToLayer (double t, CALayer layer);
```

Added:

```
public System.Drawing.RectangleF ConvertRectfromLayer (System.Drawing.RectangleF rect, CALayer layer);
        public virtual System.Drawing.RectangleF ConvertRectFromLayer (System.Drawing.RectangleF rect, CALayer layer);
        public virtual double ConvertTimeFromLayer (double timeInterval, CALayer layer);
        public virtual double ConvertTimeToLayer (double timeInterval, CALayer layer);
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGColorSpace" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGColorSpace

Added:

```
public byte [] GetColorTable ();
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGGradient" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGGradient

Added:

```
public CGGradient (CGColorSpace colorspace, CGColor[] colors, float [] locations);
        public CGGradient (CGColorSpace colorspace, CGColor[] colors);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFDocument" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFDocument

Added:

```
public CGPDFDocument (CGDataProvider provider);
```

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


# Namespace: MonoTouch.CoreImage

Removed various default constructors that should not be called without
arguments. They should not break any existing code, as code would have
crashed.

 <a name="Type_Changed:_MonoTouch.CoreImage.CIColor" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIColor

Removed:

```
public CIColor ();
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIContext" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIContext

Removed:

```
public CIContext ();
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIDetector" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIDetector

Removed:

```
public CIDetector ();
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFaceFeature" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFaceFeature

Removed:

```
public CIFaceFeature ();
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFeature" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFeature

Removed:

```
public CIFeature ();
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFilter" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFilter

Removed:

```
public CIFilter ();
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIImage" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIImage

Removed:

```
public CIImage ();
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIVector" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIVector

Removed:

```
public CIVector ();
```

 <a name="Namespace:_MonoTouch.CoreMidi" class="injected"></a>


# Namespace: MonoTouch.CoreMidi

Many of the properties that used to be in MidiObject have been moved to the
classes that actually support those properties, instead of throwing exceptions
in the cases where they would have not worked.

 <a name="Type_Changed:_MonoTouch.CoreMidi.Midi" class="injected"></a>


## Type Changed: MonoTouch.CoreMidi.Midi

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveNetworkNotificationContactsDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveNetworkNotificationSessionDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.CoreMidi.MidiDevice" class="injected"></a>


## Type Changed: MonoTouch.CoreMidi.MidiDevice

Added:

```
public int AdvanceScheduleTimeMuSec {
                get;
                set;
        }
        public bool CanRoute {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData ConnectionUniqueIDData {
                get;
                set;
        }
        public int ConnectionUniqueIDInt {
                get;
                set;
        }
        public int DeviceID {
                get;
                set;
        }
        public string DisplayName {
                get;
                set;
        }
        public string DriverDeviceEditorApp {
                get;
                set;
        }
        public string DriverOwner {
                get;
                set;
        }
        public int DriverVersion {
                get;
                set;
        }
        public string Image {
                get;
                set;
        }
        public bool IsDrumMachine {
                get;
        }
        public bool IsEffectUnit {
                get;
        }
        public bool IsEmbeddedEntity {
                get;
        }
        public bool IsMixer {
                get;
        }
        public bool IsSampler {
                get;
        }
        public string Manufacturer {
                get;
                set;
        }
        public int MaxReceiveChannels {
                get;
        }
        public int MaxSysExSpeed {
                get;
                set;
        }
        public int MaxTransmitChannels {
                get;
                set;
        }
        public string Model {
                get;
                set;
        }
        public string Name {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDictionary NameConfiguration {
                get;
                set;
        }
        public bool Offline {
                get;
                set;
        }
        public bool PanDisruptsStereo {
                get;
                set;
        }
        public bool Private {
                get;
                set;
        }
        public bool ReceivesBankSelectLSB {
                get;
                set;
        }
        public bool ReceivesBankSelectMSB {
                get;
                set;
        }
        public bool ReceivesClock {
                get;
                set;
        }
        public bool ReceivesMTC {
                get;
                set;
        }
        public bool ReceivesNotes {
                get;
                set;
        }
        public bool ReceivesProgramChanges {
                get;
                set;
        }
        public int SingleRealtimeEntity {
                get;
                set;
        }
        public bool SupportsGeneralMidi {
                get;
                set;
        }
        public bool SupportsMMC {
                get;
                set;
        }
        public bool SupportsShowControl {
                get;
                set;
        }
        public bool TransmitsBankSelectLSB {
                get;
                set;
        }
        public bool TransmitsBankSelectMSB {
                get;
                set;
        }
        public bool TransmitsClock {
                get;
                set;
        }
        public bool TransmitsMTC {
                get;
                set;
        }
        public bool TransmitsNotes {
                get;
                set;
        }
        public bool TransmitsProgramChanges {
                get;
                set;
        }
        public int UniqueID {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreMidi.MidiEndpoint" class="injected"></a>


## Type Changed: MonoTouch.CoreMidi.MidiEndpoint

Added:

```
public int AdvanceScheduleTimeMuSec {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData ConnectionUniqueIDData {
                get;
                set;
        }
        public int ConnectionUniqueIDInt {
                get;
                set;
        }
        public string DisplayName {
                get;
                set;
        }
        public string DriverOwner {
                get;
                set;
        }
        public int DriverVersion {
                get;
                set;
        }
        public int IsBroadcast {
                get;
                set;
        }
        public string Manufacturer {
                get;
                set;
        }
        public int MaxSysExSpeed {
                get;
                set;
        }
        public string Name {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDictionary NameConfiguration {
                get;
                set;
        }
        public bool Offline {
                get;
                set;
        }
        public bool Private {
                get;
                set;
        }
        public int ReceiveChannels {
                get;
                set;
        }
        public int TransmitChannels {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreMidi.MidiEntity" class="injected"></a>


## Type Changed: MonoTouch.CoreMidi.MidiEntity

Added:

```
public int AdvanceScheduleTimeMuSec {
                get;
                set;
        }
        public bool CanRoute {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData ConnectionUniqueIDData {
                get;
                set;
        }
        public int ConnectionUniqueIDInt {
                get;
                set;
        }
        public int DeviceID {
                get;
                set;
        }
        public string DisplayName {
                get;
                set;
        }
        public string DriverOwner {
                get;
                set;
        }
        public int DriverVersion {
                get;
                set;
        }
        public int IsBroadcast {
                get;
                set;
        }
        public bool IsDrumMachine {
                get;
        }
        public bool IsEffectUnit {
                get;
        }
        public bool IsEmbeddedEntity {
                get;
        }
        public bool IsMixer {
                get;
        }
        public bool IsSampler {
                get;
        }
        public int MaxReceiveChannels {
                get;
        }
        public int MaxSysExSpeed {
                get;
                set;
        }
        public int MaxTransmitChannels {
                get;
                set;
        }
        public string Model {
                get;
                set;
        }
        public string Name {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDictionary NameConfiguration {
                get;
                set;
        }
        public bool Offline {
                get;
                set;
        }
        public bool PanDisruptsStereo {
                get;
                set;
        }
        public bool Private {
                get;
                set;
        }
        public bool ReceivesBankSelectLSB {
                get;
                set;
        }
        public bool ReceivesBankSelectMSB {
                get;
                set;
        }
        public bool ReceivesClock {
                get;
                set;
        }
        public bool ReceivesMTC {
                get;
                set;
        }
        public bool ReceivesNotes {
                get;
                set;
        }
        public bool ReceivesProgramChanges {
                get;
                set;
        }
        public bool SupportsGeneralMidi {
                get;
                set;
        }
        public bool SupportsMMC {
                get;
                set;
        }
        public bool SupportsShowControl {
                get;
                set;
        }
        public bool TransmitsBankSelectLSB {
                get;
                set;
        }
        public bool TransmitsBankSelectMSB {
                get;
                set;
        }
        public bool TransmitsClock {
                get;
                set;
        }
        public bool TransmitsMTC {
                get;
                set;
        }
        public bool TransmitsNotes {
                get;
                set;
        }
        public bool TransmitsProgramChanges {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreMidi.MidiObject" class="injected"></a>


## Type Changed: MonoTouch.CoreMidi.MidiObject

Removed:

```
public int AdvanceScheduleTimeMuSec {
                get;
                set;
        }
        public bool CanRoute {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData ConnectionUniqueIDData {
                get;
                set;
        }
        public int ConnectionUniqueIDInt {
                get;
                set;
        }
        public int DeviceID {
                get;
                set;
        }
        public string DisplayName {
                get;
                set;
        }
        public string DriverDeviceEditorApp {
                get;
                set;
        }
        public string DriverOwner {
                get;
                set;
        }
        public int DriverVersion {
                get;
                set;
        }
        public string Image {
                get;
                set;
        }
        public int IsBroadcast {
                get;
                set;
        }
        public bool IsDrumMachine {
                get;
        }
        public bool IsEffectUnit {
                get;
        }
        public bool IsEmbeddedEntity {
                get;
        }
        public bool IsMixer {
                get;
        }
        public bool IsSampler {
                get;
        }
        public string Manufacturer {
                get;
                set;
        }
        public int MaxReceiveChannels {
                get;
        }
        public int MaxSysExSpeed {
                get;
                set;
        }
        public int MaxTransmitChannels {
                get;
                set;
        }
        public string Model {
                get;
                set;
        }
        public string Name {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDictionary NameConfiguration {
                get;
                set;
        }
        public bool Offline {
                get;
                set;
        }
        public bool PanDisruptsStereo {
                get;
                set;
        }
        public bool Private {
                get;
        }
        public int ReceiveChannels {
                get;
                set;
        }
        public bool ReceivesBankSelectLSB {
                get;
                set;
        }
        public bool ReceivesBankSelectMSB {
                get;
                set;
        }
        public bool ReceivesClock {
                get;
                set;
        }
        public bool ReceivesMTC {
                get;
                set;
        }
        public bool ReceivesNotes {
                get;
                set;
        }
        public bool ReceivesProgramChanges {
                get;
                set;
        }
        public int SingleRealtimeEntity {
                get;
                set;
        }
        public bool SupportsGeneralMidi {
                get;
                set;
        }
        public bool SupportsMMC {
                get;
                set;
        }
        public bool SupportsShowControl {
                get;
                set;
        }
        public int TransmitChannels {
                get;
                set;
        }
        public bool TransmitsBankSelectLSB {
                get;
                set;
        }
        public bool TransmitsBankSelectMSB {
                get;
                set;
        }
        public bool TransmitsClock {
                get;
                set;
        }
        public bool TransmitsMTC {
                get;
                set;
        }
        public bool TransmitsNotes {
                get;
                set;
        }
        public bool TransmitsProgramChanges {
                get;
                set;
        }
        public int UniqueID {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


# Namespace: MonoTouch.EventKit

 <a name="Type_Changed:_MonoTouch.EventKit.EKEventStore" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEventStore

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveChanged (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.ExternalAccessory" class="injected"></a>


# Namespace: MonoTouch.ExternalAccessory

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EAAccessoryEventArgs" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EAAccessoryEventArgs

Added:

```
public class EAAccessoryEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public EAAccessoryEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public EAAccessory Accessory {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EAAccessoryManager" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager

Added:

```
public static MonoTouch.Foundation.NSString DidConnectNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString DidDisconnectNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidConnect (EventHandler<EAAccessoryEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidDisconnect (EventHandler<EAAccessoryEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSArray" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSArray

Added:

```
public virtual NSArray Filter (NSPredicate predicate);
        public virtual NSArray Sort (NSComparator cmptr);
```

 <a name="New_Type:_MonoTouch.Foundation.NSComparator" class="injected"></a>


## New Type: MonoTouch.Foundation.NSComparator

```
[Serializable]
public delegate int NSComparator (NSObject obj1, NSObject obj2);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileCoordinator" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileCoordinator

Removed:

```
public virtual void CoordinateBatc (NSUrl[] readingURLs, NSFileCoordinatorReadingOptions readingOptions, NSUrl[] writingURLs, NSFileCoordinatorWritingOptions writingOptions, NSError error, NSAction batchHandler);
```

Added:

```
public virtual void CoordinateBatc (NSUrl[] readingURLs, NSFileCoordinatorReadingOptions readingOptions, NSUrl[] writingURLs, NSFileCoordinatorWritingOptions writingOptions, out NSError error, NSAction batchHandler);
        public virtual void CoordinateWriteWrite (NSUrl writingURL, NSFileCoordinatorWritingOptions writingOptions, NSUrl writingURL2, NSFileCoordinatorWritingOptions writingOptions2, out NSError error, NSFileCoordinatorWorkerRW writeWriteWorker);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSLocale" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSLocale

Added:

```
public static class Notifications {
                
                public static NSObject ObserveCurrentLocaleDidChange (EventHandler<NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMetadataQuery" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMetadataQuery

Added:

```
public static class Notifications {
                
                public static NSObject ObserveDidFinishGathering (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidStartGathering (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidUpdate (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveGatheringProgress (EventHandler<NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNotificationEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNotificationEventArgs

Added:

```
public class NSNotificationEventArgs : EventArgs {
        
        public NSNotificationEventArgs (NSNotification notification);
        
        public NSNotification Notification {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSString

Added:

```
public static IntPtr CreateNative (string str);
        public static void ReleaseNative (IntPtr handle);
        public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, MonoTouch.UIKit.UIFont font, float minFontSize, ref float actualFontSize, MonoTouch.UIKit.UILineBreakMode breakMode, MonoTouch.UIKit.UIBaselineAdjustment adjustment);
        public System.Drawing.SizeF StringSize (MonoTouch.UIKit.UIFont font, float minFontSize, ref float actualFontSize, float forWidth, MonoTouch.UIKit.UILineBreakMode lineBreakMode);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUbiquitousKeyValueStore" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUbiquitousKeyValueStore

Added:

```
public static class Notifications {
                
                public static NSObject ObserveDidChangeExternally (EventHandler<NSUbiquitousKeyValueStoreChangeEventArgs> handler);
        }
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUbiquitousKeyValueStoreChangeEventArgs 

Added:

```
public class NSUbiquitousKeyValueStoreChangeEventArgs : NSNotificationEventArgs {
        
        public NSUbiquitousKeyValueStoreChangeEventArgs (NSNotification notification);
        
        public string [] ChangedKeys {
                get;
        }
        public NSUbiquitousKeyValueStoreChangeReason ChangeReason {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUndoManager" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUndoManager

Added:

```
public static class Notifications {
                
                public static NSObject ObserveCheckpoint (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidCloseUndoGroup (EventHandler<NSUndoManagerCloseUndoGroupEventArgs> handler);
                public static NSObject ObserveDidOpenUndoGroup (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidRedoChange (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidUndoChange (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveWillCloseUndoGroup (EventHandler<NSUndoManagerCloseUndoGroupEventArgs> handler);
                public static NSObject ObserveWillRedoChange (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveWillUndoChange (EventHandler<NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUndoManagerCloseUndoGroupEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUndoManagerCloseUndoGroupEventArgs

Added:

```
public class NSUndoManagerCloseUndoGroupEventArgs : NSNotificationEventArgs {
        
        public NSUndoManagerCloseUndoGroupEventArgs (NSNotification notification);
        
        public Nullable<bool> Discardable {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocol" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocol

Removed:

```
public class NSUrlProtocol : NSObject {
                set;
        
        public event EventHandler<NSUrlProtocolCachedResponseEventArgs> CachedResponseIsValid;
        public event EventHandler<NSUrlProtocolChallengeEventArgs> CancelledAuthenticationChallenge;
        public event EventHandler<NSUrlProtocolDataEventArgs> DataLoaded;
        public event EventHandler<NSUrlProtocolErrorEventArgs> FailedWithError;
        public event EventHandler FinishedLoading;
        public event EventHandler<NSUrlProtocolChallengeEventArgs> ReceivedAuthenticationChallenge;
        public event EventHandler<NSUrlProtocolResponseEventArgs> ReceivedResponse;
        public event EventHandler<NSUrlProtocolRedirectEventArgs> Redirected;
```

Added:

```
public abstract class NSUrlProtocol : NSObject {
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolClient" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolClient

Removed:

```
public abstract class NSUrlProtocolClient : NSObject {
        public NSUrlProtocolClient ();
        public NSUrlProtocolClient (NSCoder coder);
        public NSUrlProtocolClient (NSObjectFlag t);
        public abstract void CachedResponseIsValid (NSUrlProtocol protocol, NSCachedUrlResponse cachedResponse);
        public abstract void CancelledAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public abstract void DataLoaded (NSUrlProtocol protocol, NSData data);
        public abstract void FailedWithError (NSUrlProtocol protocol, NSError error);
        public abstract void FinishedLoading (NSUrlProtocol protocol);
        public abstract void ReceivedAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public abstract void ReceivedResponse (NSUrlProtocol protocol, NSUrlResponse response, NSUrlCacheStoragePolicy policy);
        public abstract void Redirected (NSUrlProtocol protocol, NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
```

Added:

```
public sealed class NSUrlProtocolClient : NSObject {
        public void CachedResponseIsValid (NSUrlProtocol protocol, NSCachedUrlResponse cachedResponse);
        public void CancelledAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public void DataLoaded (NSUrlProtocol protocol, NSData data);
        public void FailedWithError (NSUrlProtocol protocol, NSError error);
        public void FinishedLoading (NSUrlProtocol protocol);
        public void ReceivedAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public void ReceivedResponse (NSUrlProtocol protocol, NSUrlResponse response, NSUrlCacheStoragePolicy policy);
        public void Redirected (NSUrlProtocol protocol, NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="Type_Changed:_MonoTouch.GameKit.GKLocalPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLocalPlayer

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveAuthenticationDidChangeNotificationName (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayer

Removed:

```
public static MonoTouch.Foundation.NSString DidChangeNotificationName {
```

Added:

```
public static MonoTouch.Foundation.NSString DidChangeNotificationNameNotification {
        public MonoTouch.Foundation.NSString DidChangeNotificationName {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidChangeNotificationName (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaLibrary" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaLibrary

Removed:

```
public static readonly MonoTouch.Foundation.NSString DidChangeNotification;
        public static readonly MonoTouch.Foundation.NSString ChangeTypePlaylists;
        public static readonly MonoTouch.Foundation.NSString ChangeTypesUserInfoKey;
```

Added:

```
public static MonoTouch.Foundation.NSString DidChangeNotification {
                get;
        }
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Added:

```
public static MonoTouch.Foundation.NSString MediaPlaybackIsPreparedToPlayDidChangeNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidEnterFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidExitFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDurationAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveLoadStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveMediaPlaybackIsPreparedToPlayDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveNaturalSizeAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveNowPlayingMovieDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObservePlaybackDidFinish (EventHandler<MPMoviePlayerFinishedEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObservePlaybackStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveScalingModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveSourceTypeAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveThumbnailImageRequestDidFinish (EventHandler<MPMoviePlayerThumbnailEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTimedMetadataUpdated (EventHandler<MPMoviePlayerTimedMetadataEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillExitFullscreen (EventHandler<MPMoviePlayerFullScreenEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMoviePlayerFinishedEventArgs" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMoviePlayerFinishedEventArgs

```
public class MPMoviePlayerFinishedEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MPMoviePlayerFinishedEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MPMovieFinishReason FinishReason {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMoviePlayerFullScreenEventArgs" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMoviePlayerFullScreenEventArgs

```
public class MPMoviePlayerFullScreenEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MPMoviePlayerFullScreenEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MonoTouch.UIKit.UIViewAnimationCurve AnimationCurve {
                get;
        }
        public double AnimationDuration {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMoviePlayerThumbnailEventArgs" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMoviePlayerThumbnailEventArgs

```
public class MPMoviePlayerThumbnailEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MPMoviePlayerThumbnailEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MonoTouch.Foundation.NSError Error {
                get;
        }
        public MonoTouch.UIKit.UIImage Image {
                get;
        }
        public double Time {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMoviePlayerTimedMetadataEventArgs" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMoviePlayerTimedMetadataEventArgs

```
public class MPMoviePlayerTimedMetadataEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MPMoviePlayerTimedMetadataEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MPTimedMetadata[] TimedMetadata {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMusicPlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController

Added:

```
public static MonoTouch.Foundation.NSString NowPlayingItemDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString PlaybackStateDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString VolumeDidChangeNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveNowPlayingItemDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObservePlaybackStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveVolumeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.MessageUI" class="injected"></a>


# Namespace: MonoTouch.MessageUI

 <a name="New_Type:_MonoTouch.MessageUI.MFMessageAvailabilityChangedEventArgs" class="injected"></a>


## New Type: MonoTouch.MessageUI.MFMessageAvailabilityChangedEventArgs

```
public class MFMessageAvailabilityChangedEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MFMessageAvailabilityChangedEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public bool TextMessageAvailability {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.MessageUI.MFMessageComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveTextMessageAvailabilityDidChange (EventHandler<MFMessageAvailabilityChangedEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.NewsstandKit" class="injected"></a>


# Namespace: MonoTouch.NewsstandKit

 <a name="Type_Changed:_MonoTouch.NewsstandKit.NKIssue" class="injected"></a>


## Type Changed: MonoTouch.NewsstandKit.NKIssue

Added:

```
public static MonoTouch.Foundation.NSString DownloadCompletedNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDownloadCompleted (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Runtime" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Runtime

Added:

```
public static void StartWWAN (Uri uri, Action<Exception> callback);
```

 <a name="Namespace:_MonoTouch.QuickLook" class="injected"></a>


# Namespace: MonoTouch.QuickLook

 <a name="New_Type:_MonoTouch.QuickLook.QLFrame" class="injected"></a>


## New Type: MonoTouch.QuickLook.QLFrame

```
[Serializable]
public delegate System.Drawing.RectangleF QLFrame (QLPreviewItem item, MonoTouch.UIKit.UIView view);
```

 <a name="Type_Changed:_MonoTouch.QuickLook.QLPreviewController" class="injected"></a>


## Type Changed: MonoTouch.QuickLook.QLPreviewController

Added:

```
public QLFrame FrameForPreviewItem {
                get;
                set;
        }
        public QLTransition TransitionImageForPreviewItem {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.QuickLook.QLPreviewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.QuickLook.QLPreviewControllerDelegate

Added:

```
public virtual System.Drawing.RectangleF FrameForPreviewItem (QLPreviewItem item, MonoTouch.UIKit.UIView view);
        public virtual MonoTouch.UIKit.UIImage TransitionImageForPreviewItem (QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

 <a name="New_Type:_MonoTouch.QuickLook.QLTransition" class="injected"></a>


## New Type: MonoTouch.QuickLook.QLTransition

```
[Serializable]
public delegate MonoTouch.UIKit.UIImage QLTransition (QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidBecomeActive (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidChangeStatusBarFrame (EventHandler<UIStatusBarFrameChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidChangeStatusBarOrientation (EventHandler<UIStatusBarOrientationChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidEnterBackground (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidFinishLaunching (EventHandler<UIApplicationLaunchEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidReceiveMemoryWarning (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveProtectedDataDidBecomeAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveProtectedDataWillBecomeUnavailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveSignificantTimeChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillChangeStatusBarFrame (EventHandler<UIStatusBarFrameChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillChangeStatusBarOrientation (EventHandler<UIStatusBarOrientationChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillEnterForeground (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillResignActive (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillTerminate (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Removed:

```
public virtual void HandleOpenURL (UIApplication application, MonoTouch.Foundation.NSUrl url);
        public virtual void OpenUrl (UIApplication application, MonoTouch.Foundation.NSUrl url, string sourceApplication, MonoTouch.Foundation.NSObject annotation);
```

Added:

```
public virtual bool HandleOpenURL (UIApplication application, MonoTouch.Foundation.NSUrl url);
        public virtual bool OpenUrl (UIApplication application, MonoTouch.Foundation.NSUrl url, string sourceApplication, MonoTouch.Foundation.NSObject annotation);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationLaunchEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationLaunchEventArgs

Removed:

```
Could not find MonoTouch.UIKit.UIApplicationLaunchEventArgs
```

Added:

```
public class UIApplicationLaunchEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIApplicationLaunchEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public bool LocationLaunch {
                get;
        }
        public MonoTouch.Foundation.NSDictionary RemoteNotifications {
                get;
        }
        public string SourceApplication {
                get;
        }
        public MonoTouch.Foundation.NSUrl Url {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIButton" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIButton

Added:

```
public UIButton (UIButtonType type);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDevice" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDevice

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveBatteryLevelDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveBatteryStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveOrientationDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveProximityStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDocument" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDocument

Added:

```
public static MonoTouch.Foundation.NSString StateChangedNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveStateChanged (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIKeyboard" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIKeyboard

Added:

```
public static MonoTouch.Foundation.NSString DidChangeFrameNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString WillChangeFrameNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidChangeFrame (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidHide (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidShow (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillChangeFrame (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillHide (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillShow (EventHandler<UIKeyboardEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIKeyboardEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIKeyboardEventArgs

Added:

```
public class UIKeyboardEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIKeyboardEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public UIViewAnimationCurve AnimationCurve {
                get;
        }
        public double AnimationDuration {
                get;
        }
        public System.Drawing.RectangleF FrameBegin {
                get;
        }
        public System.Drawing.RectangleF FrameEnd {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIMenuController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIMenuController

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidHideMenu (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidShowMenu (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillHideMenu (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillShowMenu (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPasteboard" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPasteboard

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveChanged (EventHandler<UIPasteboardChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveRemoved (EventHandler<UIPasteboardChangeEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPasteboardChangeEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPasteboardChangeEventArgs

Added:

```
public class UIPasteboardChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIPasteboardChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public string [] TypesAdded {
                get;
        }
        public string [] TypesRemoved {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScreen" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScreen

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveBrightnessDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidConnect (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidDisconnect (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIStatusBarFrameChangeEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStatusBarFrameChangeEventArgs

```
public class UIStatusBarFrameChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIStatusBarFrameChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public System.Drawing.RectangleF StatusBarFrame {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIStatusBarOrientationChangeEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStatusBarOrientationChangeEventArgs

```
public class UIStatusBarOrientationChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIStatusBarOrientationChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public UIInterfaceOrientation StatusBarOrientation {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableView

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveSelectionDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextField" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextField

Added:

```
public virtual MonoTouch.Foundation.NSComparisonResult ComparePosition (UITextPosition first, UITextPosition second);
        public virtual void DeleteBackward ();
        public virtual void DictationRecognitionFailed ();
        public virtual void DictationRecordingDidEnd ();
        public virtual UITextWritingDirection GetBaseWritingDirection (UITextPosition forPosition, UITextStorageDirection direction);
        public virtual System.Drawing.RectangleF GetCaretRectForPosition (UITextPosition position);
        public virtual int GetCharacterOffsetOfPosition (UITextPosition position, UITextRange range);
        public virtual UITextRange GetCharacterRange (UITextPosition byExtendingPosition, UITextLayoutDirection direction);
        public virtual UITextRange GetCharacterRangeAtPoint (System.Drawing.PointF point);
        public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point);
        public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point, UITextRange withinRange);
        public virtual System.Drawing.RectangleF GetFirstRectForRange (UITextRange range);
        public virtual int GetOffsetFromPosition (UITextPosition fromPosition, UITextPosition toPosition);
        public virtual UITextPosition GetPosition (UITextPosition fromPosition, int offset);
        public virtual UITextPosition GetPosition (UITextPosition fromPosition, UITextLayoutDirection inDirection, int offset);
        public virtual UITextPosition GetPosition (UITextRange withinRange, int atCharacterOffset);
        public virtual UITextPosition GetPositionWithinRange (UITextRange range, UITextLayoutDirection direction);
        public virtual UITextRange GetTextRange (UITextPosition fromPosition, UITextPosition toPosition);
        public virtual MonoTouch.Foundation.NSDictionary GetTextStyling (UITextPosition atPosition, UITextStorageDirection inDirection);
        public virtual void InsertDictationResult (MonoTouch.Foundation.NSArray dictationResult);
        public virtual void InsertText (string text);
        public virtual void ReplaceText (UITextRange range, string text);
        public virtual void SetBaseWritingDirectionforRange (UITextWritingDirection writingDirection, UITextRange range);
        public virtual void SetMarkedText (string markedText, MonoTouch.Foundation.NSRange selectedRange);
        public virtual string TextInRange (UITextRange range);
        public virtual void UnmarkText ();
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveCurrentInputModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidBeginEditing (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidEndEditing (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextFieldTextDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextInputMode" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextInputMode

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveCurrentInputModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextView

Added:

```
public virtual MonoTouch.Foundation.NSComparisonResult ComparePosition (UITextPosition first, UITextPosition second);
        public virtual void DeleteBackward ();
        public virtual void DictationRecognitionFailed ();
        public virtual void DictationRecordingDidEnd ();
        public virtual UITextWritingDirection GetBaseWritingDirection (UITextPosition forPosition, UITextStorageDirection direction);
        public virtual System.Drawing.RectangleF GetCaretRectForPosition (UITextPosition position);
        public virtual int GetCharacterOffsetOfPosition (UITextPosition position, UITextRange range);
        public virtual UITextRange GetCharacterRange (UITextPosition byExtendingPosition, UITextLayoutDirection direction);
        public virtual UITextRange GetCharacterRangeAtPoint (System.Drawing.PointF point);
        public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point);
        public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point, UITextRange withinRange);
        public virtual System.Drawing.RectangleF GetFirstRectForRange (UITextRange range);
        public virtual int GetOffsetFromPosition (UITextPosition fromPosition, UITextPosition toPosition);
        public virtual UITextPosition GetPosition (UITextPosition fromPosition, int offset);
        public virtual UITextPosition GetPosition (UITextPosition fromPosition, UITextLayoutDirection inDirection, int offset);
        public virtual UITextPosition GetPosition (UITextRange withinRange, int atCharacterOffset);
        public virtual UITextPosition GetPositionWithinRange (UITextRange range, UITextLayoutDirection direction);
        public virtual UITextRange GetTextRange (UITextPosition fromPosition, UITextPosition toPosition);
        public virtual MonoTouch.Foundation.NSDictionary GetTextStyling (UITextPosition atPosition, UITextStorageDirection inDirection);
        public virtual void InsertDictationResult (MonoTouch.Foundation.NSArray dictationResult);
        public virtual void InsertText (string text);
        public virtual void ReplaceText (UITextRange range, string text);
        public virtual void SetBaseWritingDirectionforRange (UITextWritingDirection writingDirection, UITextRange range);
        public virtual void SetMarkedText (string markedText, MonoTouch.Foundation.NSRange selectedRange);
        public virtual string TextInRange (UITextRange range);
        public virtual void UnmarkText ();
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveCurrentInputModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidBeginEditing (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidEndEditing (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWindow" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWindow

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidBecomeHidden (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidBecomeKey (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidBecomeVisible (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidResignKey (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```
