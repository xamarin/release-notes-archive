---
id: 45EFB32B-820F-9022-1D1A-DBD16B1FA416
title: "from 6.0.4 to 6.0.5"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


## Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


### Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "6.0.4";
```

Added:

```
public const string Version = "6.0.5";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


## Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureConnection" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVCaptureConnection

Removed:

```
public virtual AVCaptureInputPort[] inputPorts {
```

Added:

```
[Obsolete("Use InputPorts")]
        public AVCaptureInputPort[] inputPorts {
                get;
        }
        public virtual AVCaptureInputPort[] InputPorts {
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Added:

```
public virtual bool IsExposureModeSupported (AVCaptureExposureMode exposureMode);
```

 <a name="Namespace:_MonoTouch.AddressBookUI" class="injected"></a>


## Namespace: MonoTouch.AddressBookUI

 <a name="" class="injected"></a>


### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController 

Removed:

```
public virtual IntPtr _AddressBook {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


## Namespace: MonoTouch.AudioToolbox

 <a name="New_Type:_MonoTouch.AudioToolbox.AccessoryInfo" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AccessoryInfo

```
public class AccessoryInfo {

        public string Description {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioBufferList" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioBufferList

Removed:

```
public AudioBufferList ();
        public AudioBufferList (int count);
        public override string ToString ();
        public int BufferCount {
                get;
        }
```

Added:

```
public AudioBufferList (int bufferSize);
        public IntPtr ToPointer ();
                set;
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFormatFlags" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioFormatFlags

Removed:

```
public enum AudioFormatFlags {
```

Added:

```
public enum AudioFormatFlags : uint {
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueue" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioQueue

Removed:

```
public class AudioQueue : IDisposable {
        public void AddListener (AudioQueueProperty id, AudioQueuePropertyChanged callback);
        public T GetProperty<T> (AudioQueueProperty property);
        public IntPtr GetProperty (AudioQueueProperty property, out int size);
        public bool GetProperty (AudioQueueProperty property, ref int dataSize, IntPtr outdata);
        public void RemoveListener (AudioQueueProperty id, AudioQueuePropertyChanged callback);
        public bool SetProperty (AudioQueueProperty property, int dataSize, IntPtr propertyData);
        public delegate void AudioQueuePropertyChanged (AudioQueueProperty id);
```

Added:

```
public abstract class AudioQueue : IDisposable {
        public AudioQueueStatus AddListener (AudioQueueProperty property, AudioQueuePropertyChanged callback);
        public AudioQueueProcessingTap CreateProcessingTap (AudioQueueProcessingTapCallback processingCallback, AudioQueueProcessingTapFlags flags, out AudioQueueStatus status);
        public AudioQueueStatus EnqueueBuffer (AudioQueueBuffer* audioQueueBuffer, int bytes, AudioStreamPacketDescription[] desc, int trimFramesAtStart, int trimFramesAtEnd, AudioQueueParameterEvent[] parameterEvents, out AudioTimeStamp actualStartTime);
        public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, int bytes, AudioStreamPacketDescription[] desc, int trimFramesAtStart, int trimFramesAtEnd, AudioQueueParameterEvent[] parameterEvents, out AudioTimeStamp actualStartTime);
        [Obsolete]
        public T GetProperty<T> (AudioQueueProperty property);
        [Obsolete]
        public IntPtr GetProperty (AudioQueueProperty property, out int size);
        [Obsolete]
        public bool GetProperty (AudioQueueProperty property, ref int dataSize, IntPtr outdata);
        public void RemoveListener (AudioQueueProperty property, AudioQueuePropertyChanged callback);
        public AudioQueueStatus SetChannelAssignments (params AudioQueueChannelAssignment[] channelAssignments);
        [Obsolete]
        public bool SetProperty (AudioQueueProperty property, int dataSize, IntPtr propertyData);
        public AudioQueueHardwareCodecPolicy HardwareCodecPolicy {
                get;
                set;
        }
        public float Pan {
                get;
                set;
        }
        public float VolumeRampTime {
                get;
                set;
        }
        public delegate void AudioQueuePropertyChanged (AudioQueueProperty property);
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioQueueChannelAssignment" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioQueueChannelAssignment

```
public struct AudioQueueChannelAssignment {

        public AudioQueueChannelAssignment (MonoTouch.CoreFoundation.CFString deviceUID, uint channelNumber);
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueParameterEvent" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioQueueParameterEvent

Removed:

```
public uint ID;
```

Added:

```
public AudioQueueParameterEvent (AudioQueueParameter parameter, float value);

        [Obsolete("Use Parameter")]
        public uint ID;
        public AudioQueueParameter Parameter;
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioQueueProcessingTap" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioQueueProcessingTap

```
public class AudioQueueProcessingTap : IDisposable {

        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public AudioQueueStatus GetQueueTime (out double sampleTime, out uint frameCount);
        public AudioQueueStatus GetSourceAudio (uint numberOfFrames, ref AudioTimeStamp timeStamp, out AudioQueueProcessingTapFlags flags, out uint parentNumberOfFrames, AudioBufferList data);

        public uint MaxFrames {
                get;
        }
        public AudioStreamBasicDescription ProcessingFormat {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioQueueProcessingTapCallback" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioQueueProcessingTapCallback

```
[Serializable]
public delegate uint AudioQueueProcessingTapCallback (AudioQueueProcessingTap audioQueueTap, uint numberOfFrames, ref AudioTimeStamp timeStamp, ref AudioQueueProcessingTapFlags flags, AudioBufferList data);
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioQueueProcessingTapFlags" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioQueueProcessingTapFlags

```
[Serializable]
[Flags]
public enum AudioQueueProcessingTapFlags : uint {
        PreEffects,
        PostEffects,
        Siphon,
        StartOfStream,
        EndOfStream
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueProperty" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioQueueProperty

Added:

```
public enum AudioQueueProperty : uint {
        HardwareCodecPolicy,
        ChannelAssignments
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueStatus" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioQueueStatus

Added:

```
TooManyTaps,
        InvalidTapContext,
        InvalidTapType,
        InvalidOfflineMode,
        DataFormatError,
        UnsupportedProperty,
        GeneralParamError
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioServicesError" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioServicesError

```
[Serializable]
public enum AudioServicesError {
        None,
        UnsupportedProperty,
        BadPropertySize,
        BadSpecifierSizeError,
        SystemSoundUnspecifiedError,
        SystemSoundClientTimedOutError
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSession" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioSession

Removed:

```
public static string AudioRoute {
```

Added:

```
public static AudioSessionErrors SetActive (bool active, AudioSessionActiveFlags flags);
        [Obsolete("Use InputRoute or OutputRoute instead")]
        public static string AudioRoute {
        public static bool InputGainAvailable {
                get;
        }
        public static float InputGainScalar {
                get;
                set;
        }
        public static AccessoryInfo[] InputSources {
                get;
        }
        public static AccessoryInfo[] OutputDestinations {
                get;
        }
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioSessionActiveFlags" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioSessionActiveFlags

```
[Serializable]
public enum AudioSessionActiveFlags : uint {
        NotifyOthersOnDeactivation
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionErrors" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioSessionErrors

Added:

```
UnspecifiedError
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionMode" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioSessionMode

Added:

```
GameChat
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionProperty" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioSessionProperty

Added:

```
InputSources,
        OutputDestinations,
        InputSource,
        OutputDestination,
        InputGainAvailable,
        InputGainScalar,
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionRouteChangeReason" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioSessionRouteChangeReason

Added:

```
NoSuitableRouteForCategory
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioStreamBasicDescription" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioStreamBasicDescription

Removed:

```
public override string ToString ();
        [Obsolete("Use the strongly-typed Format property instead")]
        public int FormatID {
                get;
                set;
        }
```

Added:

```
public AudioStreamBasicDescription (AudioFormatType formatType);
        public static AudioStreamBasicDescription CreateLinearPCM (double sampleRate, uint channelsPerFrame, uint bitsPerChannel);
        public override string ToString ();
        public const double AudioStreamAnyRate = 0;
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.InputAudioQueue" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.InputAudioQueue

Added:

```
public AudioQueueStatus EnqueueBuffer (AudioQueueBuffer* buffer);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.MutableAudioBufferList" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.MutableAudioBufferList

Removed:

```
public class MutableAudioBufferList : AudioBufferList, IDisposable {
```

Added:

```
[Obsolete]
public class MutableAudioBufferList : AudioBufferList, IDisposable {
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.SystemSound" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.SystemSound

Added:

```
public AudioServicesError AddSystemSoundCompletion (Action routine, MonoTouch.CoreFoundation.CFRunLoop runLoop);
        public void RemoveSystemSoundCompletion ();
        public bool CompletePlaybackIfAppDies {
                get;
                set;
        }
        public bool IsUISound {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.CoreData" class="injected"></a>


## Namespace: MonoTouch.CoreData

 <a name="New_Type:_MonoTouch.CoreData.NSFetchedResultsChangeType" class="injected"></a>


### New Type: MonoTouch.CoreData.NSFetchedResultsChangeType

```
[Serializable]
public enum NSFetchedResultsChangeType {
        Insert,
        Delete,
        Move,
        Update
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSFetchedResultsController" class="injected"></a>


### New Type: MonoTouch.CoreData.NSFetchedResultsController

```
public class NSFetchedResultsController : MonoTouch.Foundation.NSObject {

        public NSFetchedResultsController ();
        public NSFetchedResultsController (MonoTouch.Foundation.NSCoder coder);
        public NSFetchedResultsController (MonoTouch.Foundation.NSObjectFlag t);
        public NSFetchedResultsController (IntPtr handle);
        public NSFetchedResultsController (NSFetchRequest fetchRequest, NSManagedObjectContext context, string sectionNameKeyPath, string name);

        public static void DeleteCache (string name);
        protected override void Dispose (bool disposing);
        public virtual MonoTouch.Foundation.NSIndexPath FromObject (MonoTouch.Foundation.NSObject obj);
        public virtual MonoTouch.Foundation.NSObject ObjectAt (MonoTouch.Foundation.NSIndexPath path);
        public virtual bool PerformFetch (out MonoTouch.Foundation.NSError error);
        public virtual int SectionFor (string title, int atIndex);
        public virtual string SectionIndexTitles (string sectionName);

        public virtual string CacheName {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public NSFetchedResultsControllerDelegate Delegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject[] FetchedObjects {
                get;
        }
        public virtual NSFetchRequest FetchRequest {
                get;
        }
        public virtual NSManagedObjectContext ManagedObjectContext {
                get;
        }
        public virtual string SectionNameKeyPath {
                get;
        }
        public virtual NSFetchedResultsSectionInfo[] Sections {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSFetchedResultsControllerDelegate" class="injected"></a>


### New Type: MonoTouch.CoreData.NSFetchedResultsControllerDelegate

```
public class NSFetchedResultsControllerDelegate : MonoTouch.Foundation.NSObject {

        public NSFetchedResultsControllerDelegate ();
        public NSFetchedResultsControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public NSFetchedResultsControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public NSFetchedResultsControllerDelegate (IntPtr handle);

        public virtual void DidChangeContent (NSFetchedResultsController controller);
        public virtual void DidChangeObject (NSFetchedResultsController controller, MonoTouch.Foundation.NSObject anObject, MonoTouch.Foundation.NSIndexPath indexPath, NSFetchedResultsChangeType type, MonoTouch.Foundation.NSIndexPath newIndexPath);
        public virtual void DidChangeSection (NSFetchedResultsController controller, NSFetchedResultsSectionInfo sectionInfo, uint sectionIndex, NSFetchedResultsChangeType type);
        public virtual string SectionFor (NSFetchedResultsController controller, string sectionName);
        public virtual void WillChangeContent (NSFetchedResultsController controller);
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSFetchedResultsSectionInfo" class="injected"></a>


### New Type: MonoTouch.CoreData.NSFetchedResultsSectionInfo

```
public class NSFetchedResultsSectionInfo : MonoTouch.Foundation.NSObject {

        public NSFetchedResultsSectionInfo ();
        public NSFetchedResultsSectionInfo (MonoTouch.Foundation.NSCoder coder);
        public NSFetchedResultsSectionInfo (MonoTouch.Foundation.NSObjectFlag t);
        public NSFetchedResultsSectionInfo (IntPtr handle);

        public virtual int Count {
                get;
        }
        public virtual string IndexTitle {
                get;
        }
        public virtual string Name {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject[] Objects {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


## Namespace: MonoTouch.CoreFoundation

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFStream" class="injected"></a>


### Type Changed: MonoTouch.CoreFoundation.CFStream

Added:

```
public static void CreatePairWithSocketToHost (string host, int port, out CFReadStream readStream, out CFWriteStream writeStream);
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


## Namespace: MonoTouch.CoreGraphics

 <a name="New_Type:_MonoTouch.CoreGraphics.CGImageColorModel" class="injected"></a>


### New Type: MonoTouch.CoreGraphics.CGImageColorModel

```
[Serializable]
public enum CGImageColorModel {
        RGB,
        Gray,
        CMYK,
        Lab
}
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGImageProperties" class="injected"></a>


### New Type: MonoTouch.CoreGraphics.CGImageProperties

```
public class CGImageProperties : MonoTouch.Foundation.DictionaryContainer {

        public CGImageProperties ();
        public CGImageProperties (MonoTouch.Foundation.NSDictionary dictionary);

        public Nullable<bool> Alpha {
                get;
                set;
        }
        public Nullable<cgimagecolormodel> ColorModel {
                get;
                set;
        }
        public Nullable<int> Depth {
                get;
                set;
        }
        public Nullable<int> DPIHeight {
                get;
                set;
        }
        public Nullable<int> DPIWidth {
                get;
                set;
        }
        public CGImagePropertiesExif Exif {
                get;
        }
        public Nullable<int> FileSize {
                get;
                set;
        }
        public CGImagePropertiesGps Gps {
                get;
        }
        public CGImagePropertiesIptc Iptc {
                get;
        }
        public Nullable<bool> IsFloat {
                get;
                set;
        }
        public Nullable<bool> IsIndexed {
                get;
                set;
        }
        public CGImagePropertiesJfif Jfif {
                get;
        }
        public System.Nullable<monotouch.coreimage.ciimageorientation> Orientation {
                get;
                set;
        }
        public Nullable<int> PixelHeight {
                get;
                set;
        }
        public Nullable<int> PixelWidth {
                get;
                set;
        }
        public CGImagePropertiesPng Png {
                get;
        }
        public string ProfileName {
                get;
                set;
        }
        public CGImagePropertiesTiff Tiff {
                get;
        }
}
</int></int></monotouch.coreimage.ciimageorientation></bool></bool></int></int></int></int></cgimagecolormodel></bool>
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGImagePropertiesExif" class="injected"></a>


### New Type: MonoTouch.CoreGraphics.CGImagePropertiesExif

```
public class CGImagePropertiesExif : MonoTouch.Foundation.DictionaryContainer {

        public CGImagePropertiesExif ();
        public CGImagePropertiesExif (MonoTouch.Foundation.NSDictionary dictionary);

        public Nullable<float> Aperture {
                get;
                set;
        }
        public Nullable<float> Brightness {
                get;
                set;
        }
        public Nullable<float> CompressedBitsPerPixel {
                get;
                set;
        }
        public Nullable<float> DigitalZoomRatio {
                get;
                set;
        }
        public Nullable<float> ExposureBias {
                get;
                set;
        }
        public Nullable<float> ExposureIndex {
                get;
                set;
        }
        public Nullable<int> ExposureProgram {
                get;
                set;
        }
        public Nullable<float> ExposureTime {
                get;
                set;
        }
        public Nullable<bool> Flash {
                get;
                set;
        }
        public Nullable<float> FlashEnergy {
                get;
                set;
        }
        public Nullable<float> FocalPlaneXResolution {
                get;
                set;
        }
        public Nullable<float> FocalPlaneYResolution {
                get;
                set;
        }
        public Nullable<float> GainControl {
                get;
                set;
        }
        public int [] ISOSpeedRatings {
                get;
        }
        public Nullable<float> MaximumLensAperture {
                get;
                set;
        }
        public Nullable<int> PixelXDimension {
                get;
                set;
        }
        public Nullable<int> PixelYDimension {
                get;
                set;
        }
        public Nullable<float> ShutterSpeed {
                get;
                set;
        }
        public Nullable<float> SubjectDistance {
                get;
                set;
        }
}
</float></float></int></int></float></float></float></float></float></bool></float></int></float></float></float></float></float></float>
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGImagePropertiesGps" class="injected"></a>


### New Type: MonoTouch.CoreGraphics.CGImagePropertiesGps

```
public class CGImagePropertiesGps : MonoTouch.Foundation.DictionaryContainer {

        public CGImagePropertiesGps ();
        public CGImagePropertiesGps (MonoTouch.Foundation.NSDictionary dictionary);

        public Nullable<int> Altitude {
                get;
                set;
        }
        public Nullable<float> Latitude {
                get;
                set;
        }
        public Nullable<float> Longitude {
                get;
                set;
        }
}
</float></float></int>
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGImagePropertiesIptc" class="injected"></a>


### New Type: MonoTouch.CoreGraphics.CGImagePropertiesIptc

```
public class CGImagePropertiesIptc : MonoTouch.Foundation.DictionaryContainer {

        public CGImagePropertiesIptc ();
        public CGImagePropertiesIptc (MonoTouch.Foundation.NSDictionary dictionary);

        public string Byline {
                get;
                set;
        }
        public string BylineTitle {
                get;
                set;
        }
        public string CaptionAbstract {
                get;
                set;
        }
        public string City {
                get;
                set;
        }
        public string ContentLocationName {
                get;
                set;
        }
        public string CopyrightNotice {
                get;
                set;
        }
        public string CountryPrimaryLocationName {
                get;
                set;
        }
        public string Credit {
                get;
                set;
        }
        public string Source {
                get;
                set;
        }
        public string WriterEditor {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGImagePropertiesJfif" class="injected"></a>


### New Type: MonoTouch.CoreGraphics.CGImagePropertiesJfif

```
public class CGImagePropertiesJfif : MonoTouch.Foundation.DictionaryContainer {

        public CGImagePropertiesJfif ();
        public CGImagePropertiesJfif (MonoTouch.Foundation.NSDictionary dictionary);

        public Nullable<int> XDensity {
                get;
                set;
        }
        public Nullable<int> YDensity {
                get;
                set;
        }
}
</int></int>
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGImagePropertiesPng" class="injected"></a>


### New Type: MonoTouch.CoreGraphics.CGImagePropertiesPng

```
public class CGImagePropertiesPng : MonoTouch.Foundation.DictionaryContainer {

        public CGImagePropertiesPng ();
        public CGImagePropertiesPng (MonoTouch.Foundation.NSDictionary dictionary);

        public string Author {
                get;
                set;
        }
        public string Description {
                get;
                set;
        }
        public Nullable<float> Gamma {
                get;
                set;
        }
        public string Software {
                get;
                set;
        }
        public string Title {
                get;
                set;
        }
        public Nullable<int> XPixelsPerMeter {
                get;
                set;
        }
        public Nullable<int> YPixelsPerMeter {
                get;
                set;
        }
}
</int></int></float>
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGImagePropertiesTiff" class="injected"></a>


### New Type: MonoTouch.CoreGraphics.CGImagePropertiesTiff

```
public class CGImagePropertiesTiff : MonoTouch.Foundation.DictionaryContainer {

        public CGImagePropertiesTiff ();
        public CGImagePropertiesTiff (MonoTouch.Foundation.NSDictionary dictionary);

        public System.Nullable<monotouch.coreimage.ciimageorientation> Orientation {
                get;
                set;
        }
        public string Software {
                get;
                set;
        }
        public Nullable<int> XResolution {
                get;
                set;
        }
        public Nullable<int> YResolution {
                get;
                set;
        }
}
</int></int></monotouch.coreimage.ciimageorientation>
```

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


## Namespace: MonoTouch.CoreImage

 <a name="Type_Changed:_MonoTouch.CoreImage.CIDetector" class="injected"></a>


### Type Changed: MonoTouch.CoreImage.CIDetector

Added:

```
public static CIDetector CreateFaceDetector (CIContext context, Nullable<FaceDetectorAccuracy> accuracy, Nullable<float> minFeatureSize, Nullable<bool> trackingEnabled);
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIImage" class="injected"></a>


### Type Changed: MonoTouch.CoreImage.CIImage

Removed:

```
public CIImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.Foundation.NSData d, int bpr, System.Drawing.SizeF size, int f, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
        public CIImage (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, MonoTouch.Foundation.NSDictionary dict);
        public CIImage (MonoTouch.UIKit.UIImage image, MonoTouch.Foundation.NSDictionary options);
        public static CIImage FromCGImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary d);
        public static CIImage FromData (MonoTouch.Foundation.NSData bitmapData, int bpr, System.Drawing.SizeF size, int ciImageFormat, MonoTouch.CoreGraphics.CGColorSpace colorspace);
        public static CIImage FromData (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary d);
        public static CIImage FromImageBuffer (MonoTouch.CoreVideo.CVPixelBuffer buffer, MonoTouch.Foundation.NSDictionary dict);
        public static CIImage FromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary d);
```

Added:

```
[Obsolete("Use constructor with CIImageInitializationOptionsWithMetadata")]
        public CIImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.CoreGraphics.CGImage image, CIImageInitializationOptionsWithMetadata options);
        [Obsolete("Use constructor with CIImageInitializationOptions")]
        public CIImage (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.CoreGraphics.CGLayer layer, CIImageInitializationOptions options);
        [Obsolete("Use constructor with CIImageInitializationOptionsWithMetadata")]
        public CIImage (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.Foundation.NSData data, CIImageInitializationOptionsWithMetadata options);
        public CIImage (MonoTouch.Foundation.NSData d, int bytesPerRow, System.Drawing.SizeF size, int pixelFormat, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
        [Obsolete("Use constructor with CIImageInitializationOptions")]
        public CIImage (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.Foundation.NSUrl url, CIImageInitializationOptions options);
        [Obsolete("Use constructor with CIImageInitializationOptions")]
        public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, MonoTouch.Foundation.NSDictionary dict);
        public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, CIImageInitializationOptions options);
        [Obsolete("Use constructor with CIImageInitializationOptions")]
        public CIImage (MonoTouch.UIKit.UIImage image, MonoTouch.Foundation.NSDictionary options);
        public CIImage (MonoTouch.UIKit.UIImage image, CIImageInitializationOptions options);
        public static CIImage FromCGImage (MonoTouch.CoreGraphics.CGImage image, CIImageInitializationOptionsWithMetadata options);
        [Obsolete("Use FromCGImage (CGImage, CIImageInitializationOptionsWithMetadata) overload")]
        public static CIImage FromCGImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary d);
        public static CIImage FromData (MonoTouch.Foundation.NSData data, CIImageInitializationOptionsWithMetadata options);
        public static CIImage FromData (MonoTouch.Foundation.NSData bitmapData, int bytesPerRow, System.Drawing.SizeF size, int pixelFormat, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
        [Obsolete("Use FromData (NSData, CIImageInitializationOptionsWithMetadata) overload")]
        public static CIImage FromData (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary d);
        public static CIImage FromImageBuffer (MonoTouch.CoreVideo.CVPixelBuffer buffer, CIImageInitializationOptions options);
        [Obsolete("Use FromImageBuffer (CVPixelBuffer, CIImageInitializationOptions) overload")]
        public static CIImage FromImageBuffer (MonoTouch.CoreVideo.CVPixelBuffer buffer, MonoTouch.Foundation.NSDictionary dict);
        public static CIImage FromUrl (MonoTouch.Foundation.NSUrl url, CIImageInitializationOptions options);
        [Obsolete("Use FromUrl (NSUrl, CIImageInitializationOptions) overload")]
        public static CIImage FromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary d);
        protected override void Dispose (bool disposing);
        public MonoTouch.CoreGraphics.CGImageProperties Properties {
                get;
        }
```

 <a name="New_Type:_MonoTouch.CoreImage.CIImageInitializationOptions" class="injected"></a>


### New Type: MonoTouch.CoreImage.CIImageInitializationOptions

```
public class CIImageInitializationOptions : MonoTouch.Foundation.DictionaryContainer {

        public CIImageInitializationOptions ();
        public CIImageInitializationOptions (MonoTouch.Foundation.NSDictionary dictionary);

        public MonoTouch.CoreGraphics.CGColorSpace ColorSpace {
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIImageInitializationOptionsWithMetadata" class="injected"></a>


### New Type: MonoTouch.CoreImage.CIImageInitializationOptionsWithMetadata

```
public class CIImageInitializationOptionsWithMetadata : CIImageInitializationOptions {

        public CIImageInitializationOptionsWithMetadata ();
        public CIImageInitializationOptionsWithMetadata (MonoTouch.Foundation.NSDictionary dictionary);

        public MonoTouch.CoreGraphics.CGImageProperties Properties {
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.FaceDetectorAccuracy" class="injected"></a>


### New Type: MonoTouch.CoreImage.FaceDetectorAccuracy

```
[Serializable]
public enum FaceDetectorAccuracy {
        High,
        Low
}
```

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


## Namespace: MonoTouch.CoreLocation

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManager" class="injected"></a>


### Type Changed: MonoTouch.CoreLocation.CLLocationManager

Removed:

```
public event EventHandler<CLLocationUpdatedEventArgs> UpdatedLocation;
```

Added:

```
[Obsolete("Deprecated in iOS 6.0")]
        public event EventHandler<CLLocationUpdatedEventArgs> UpdatedLocation;
```

 <a name="Namespace:_MonoTouch.CoreText" class="injected"></a>


## Namespace: MonoTouch.CoreText

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontDescriptor" class="injected"></a>


### Type Changed: MonoTouch.CoreText.CTFontDescriptor

Removed:

```
public CTFontDescriptor WithFeature (MonoTouch.Foundation.NSNumber featureTypeIdentifier, MonoTouch.Foundation.NSNumber featureSelectorIdentifier);
```

Added:

```
[Obsolete]
        public CTFontDescriptor WithFeature (MonoTouch.Foundation.NSNumber featureTypeIdentifier, MonoTouch.Foundation.NSNumber featureSelectorIdentifier);
        public CTFontDescriptor WithFeature (CTFontFeature*.Selector featureSelector);
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureAllTypographicFeatures" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureAllTypographicFeatures

```
public class CTFontFeatureAllTypographicFeatures : CTFontFeatureSelectors {

        public CTFontFeatureAllTypographicFeatures (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                AllTypeFeaturesOn,
                AllTypeFeaturesOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureAlternateKana" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureAlternateKana

```
public class CTFontFeatureAlternateKana : CTFontFeatureSelectors {

        public CTFontFeatureAlternateKana (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                AlternateHorizKanaOn,
                AlternateHorizKanaOff,
                AlternateVertKanaOn,
                AlternateVertKanaOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureAnnotation" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureAnnotation

```
public class CTFontFeatureAnnotation : CTFontFeatureSelectors {

        public CTFontFeatureAnnotation (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoAnnotation,
                BoxAnnotation,
                RoundedBoxAnnotation,
                CircleAnnotation,
                InvertedCircleAnnotation,
                ParenthesisAnnotation,
                PeriodAnnotation,
                RomanNumeralAnnotation,
                DiamondAnnotation,
                InvertedBoxAnnotation,
                InvertedRoundedBoxAnnotation
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureCJKRomanSpacing" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureCJKRomanSpacing

```
public class CTFontFeatureCJKRomanSpacing : CTFontFeatureSelectors {

        public CTFontFeatureCJKRomanSpacing (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                HalfWidthCJKRoman,
                ProportionalCJKRoman,
                DefaultCJKRoman,
                FullWidthCJKRoman
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureCJKSymbolAlternatives" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureCJKSymbolAlternatives

```
public class CTFontFeatureCJKSymbolAlternatives : CTFontFeatureSelectors {

        public CTFontFeatureCJKSymbolAlternatives (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoCJKSymbolAlternatives,
                CJKSymbolAltOne,
                CJKSymbolAltTwo,
                CJKSymbolAltThree,
                CJKSymbolAltFour,
                CJKSymbolAltFive
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureCJKVerticalRomanPlacement" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureCJKVerticalRomanPlacement

```
public class CTFontFeatureCJKVerticalRomanPlacement : CTFontFeatureSelectors {

        public CTFontFeatureCJKVerticalRomanPlacement (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                CJKVerticalRomanCentered,
                CJKVerticalRomanHBaseline
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureCaseSensitiveLayout" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureCaseSensitiveLayout

```
public class CTFontFeatureCaseSensitiveLayout : CTFontFeatureSelectors {

        public CTFontFeatureCaseSensitiveLayout (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                CaseSensitiveLayoutOn,
                CaseSensitiveLayoutOff,
                CaseSensitiveSpacingOn,
                CaseSensitiveSpacingOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureCharacterAlternatives" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureCharacterAlternatives

```
public class CTFontFeatureCharacterAlternatives : CTFontFeatureSelectors {

        public CTFontFeatureCharacterAlternatives (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoAlternates
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureCharacterShape" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureCharacterShape

```
public class CTFontFeatureCharacterShape : CTFontFeatureSelectors {

        public CTFontFeatureCharacterShape (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                TraditionalCharacters,
                SimplifiedCharacters,
                JIS1978Characters,
                JIS1983Characters,
                JIS1990Characters,
                TraditionalAltOne,
                TraditionalAltTwo,
                TraditionalAltThree,
                TraditionalAltFour,
                TraditionalAltFive,
                ExpertCharacters,
                JIS2004Characters,
                HojoCharacters,
                NLCCharacters,
                TraditionalNamesCharacters
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureContextualAlternates" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureContextualAlternates

```
public class CTFontFeatureContextualAlternates : CTFontFeatureSelectors {

        public CTFontFeatureContextualAlternates (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                ContextualAlternatesOn,
                ContextualAlternatesOff,
                SwashAlternatesOn,
                SwashAlternatesOff,
                ContextualSwashAlternatesOn,
                ContextualSwashAlternatesOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureCursiveConnection" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureCursiveConnection

```
public class CTFontFeatureCursiveConnection : CTFontFeatureSelectors {

        public CTFontFeatureCursiveConnection (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                Unconnected,
                PartiallyConnected,
                Cursive
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureDesignComplexity" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureDesignComplexity

```
public class CTFontFeatureDesignComplexity : CTFontFeatureSelectors {

        public CTFontFeatureDesignComplexity (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                DesignLevel1,
                DesignLevel2,
                DesignLevel3,
                DesignLevel4,
                DesignLevel5
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureDiacritics" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureDiacritics

```
public class CTFontFeatureDiacritics : CTFontFeatureSelectors {

        public CTFontFeatureDiacritics (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                ShowDiacritics,
                HideDiacritics,
                DecomposeDiacritics
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureFractions" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureFractions

```
public class CTFontFeatureFractions : CTFontFeatureSelectors {

        public CTFontFeatureFractions (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoFractions,
                VerticalFractions,
                DiagonalFractions
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureIdeographicAlternatives" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureIdeographicAlternatives

```
public class CTFontFeatureIdeographicAlternatives : CTFontFeatureSelectors {

        public CTFontFeatureIdeographicAlternatives (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoIdeographicAlternatives,
                IdeographicAltOne,
                IdeographicAltTwo,
                IdeographicAltThree,
                IdeographicAltFour,
                IdeographicAltFive
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureIdeographicSpacing" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureIdeographicSpacing

```
public class CTFontFeatureIdeographicSpacing : CTFontFeatureSelectors {

        public CTFontFeatureIdeographicSpacing (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                FullWidthIdeographs,
                ProportionalIdeographs,
                HalfWidthIdeographs
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureItalicCJKRoman" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureItalicCJKRoman

```
public class CTFontFeatureItalicCJKRoman : CTFontFeatureSelectors {

        public CTFontFeatureItalicCJKRoman (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoCJKItalicRoman,
                CJKItalicRoman,
                CJKItalicRomanOn,
                CJKItalicRomanOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureKanaSpacing" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureKanaSpacing

```
public class CTFontFeatureKanaSpacing : CTFontFeatureSelectors {

        public CTFontFeatureKanaSpacing (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                FullWidthKana,
                ProportionalKana
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureLetterCase" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureLetterCase

```
[Obsolete]
public class CTFontFeatureLetterCase : CTFontFeatureSelectors {

        public CTFontFeatureLetterCase (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                UpperAndLowerCase,
                AllCaps,
                AllLowerCase,
                SmallCaps,
                InitialCaps,
                InitialCapsAndSmallCaps
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureLigatures" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureLigatures

```
public class CTFontFeatureLigatures : CTFontFeatureSelectors {

        public CTFontFeatureLigatures (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                RequiredLigaturesOn,
                RequiredLigaturesOff,
                CommonLigaturesOn,
                CommonLigaturesOff,
                RareLigaturesOn,
                RareLigaturesOff,
                LogosOn,
                LogosOff,
                RebusPicturesOn,
                RebusPicturesOff,
                DiphthongLigaturesOn,
                DiphthongLigaturesOff,
                SquaredLigaturesOn,
                SquaredLigaturesOff,
                AbbrevSquaredLigaturesOn,
                AbbrevSquaredLigaturesOff,
                SymbolLigaturesOn,
                SymbolLigaturesOff,
                ContextualLigaturesOn,
                ContextualLigaturesOff,
                HistoricalLigaturesOn,
                HistoricalLigaturesOff
        }
}
```

 <a name="" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureLinguisticRearrangementConnection 

```
public class CTFontFeatureLinguisticRearrangementConnection : CTFontFeatureSelectors {

        public CTFontFeatureLinguisticRearrangementConnection (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                LinguisticRearrangementOn,
                LinguisticRearrangementOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureLowerCase" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureLowerCase

```
public class CTFontFeatureLowerCase : CTFontFeatureSelectors {

        public CTFontFeatureLowerCase (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                DefaultLowerCase,
                LowerCaseSmallCaps,
                LowerCasePetiteCaps
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureMathematicalExtras" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureMathematicalExtras

```
public class CTFontFeatureMathematicalExtras : CTFontFeatureSelectors {

        public CTFontFeatureMathematicalExtras (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                HyphenToMinusOn,
                HyphenToMinusOff,
                AsteriskToMultiplyOn,
                AsteriskToMultiplyOff,
                SlashToDivideOn,
                SlashToDivideOff,
                InequalityLigaturesOn,
                InequalityLigaturesOff,
                ExponentsOn,
                ExponentsOff,
                MathematicalGreekOn,
                MathematicalGreekOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureNumberCase" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureNumberCase

```
public class CTFontFeatureNumberCase : CTFontFeatureSelectors {

        public CTFontFeatureNumberCase (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                LowerCaseNumbers,
                UpperCaseNumbers
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureNumberSpacing" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureNumberSpacing

```
public class CTFontFeatureNumberSpacing : CTFontFeatureSelectors {

        public CTFontFeatureNumberSpacing (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                MonospacedNumbers,
                ProportionalNumbers,
                ThirdWidthNumbers,
                QuarterWidthNumbers
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureOrnamentSets" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureOrnamentSets

```
public class CTFontFeatureOrnamentSets : CTFontFeatureSelectors {

        public CTFontFeatureOrnamentSets (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoOrnaments,
                Dingbats,
                PiCharacters,
                Fleurons,
                DecorativeBorders,
                InternationalSymbols,
                MathSymbols
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureOverlappingCharacters" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureOverlappingCharacters

```
public class CTFontFeatureOverlappingCharacters : CTFontFeatureSelectors {

        public CTFontFeatureOverlappingCharacters (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                PreventOverlapOn,
                PreventOverlapOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureRubyKana" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureRubyKana

```
public class CTFontFeatureRubyKana : CTFontFeatureSelectors {

        public CTFontFeatureRubyKana (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoRubyKana,
                RubyKana,
                RubyKanaOn,
                RubyKanaOff
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontFeatureSelectors" class="injected"></a>


### Type Changed: MonoTouch.CoreText.CTFontFeatureSelectors

Removed:

```
public MonoTouch.Foundation.NSNumber Identifier {
```

Added:

```
protected int FeatureWeak {
                get;
        }
        [Obsolete("Use one of descendant classes")]
        public MonoTouch.Foundation.NSNumber Identifier {
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontFeatureSettings" class="injected"></a>


### Type Changed: MonoTouch.CoreText.CTFontFeatureSettings

Removed:

```
public CTFontFeatureSettings ();
        public MonoTouch.Foundation.NSNumber SelectorIdentifier {
        public MonoTouch.Foundation.NSNumber TypeIdentifier {
```

Added:

```
public FontFeatureGroup FeatureGroup {
                get;
        }
        public int FeatureWeak {
                get;
        }
        [Obsolete("Use FeatureWeak instead")]
        public MonoTouch.Foundation.NSNumber SelectorIdentifier {
        [Obsolete("Use Type")]
        public MonoTouch.Foundation.NSNumber TypeIdentifier {
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureSmartSwash" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureSmartSwash

```
public class CTFontFeatureSmartSwash : CTFontFeatureSelectors {

        public CTFontFeatureSmartSwash (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                WordInitialSwashesOn,
                WordInitialSwashesOff,
                WordFinalSwashesOn,
                WordFinalSwashesOff,
                LineInitialSwashesOn,
                LineInitialSwashesOff,
                LineFinalSwashesOn,
                LineFinalSwashesOff,
                NonFinalSwashesOn,
                NonFinalSwashesOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureStyleOptions" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureStyleOptions

```
public class CTFontFeatureStyleOptions : CTFontFeatureSelectors {

        public CTFontFeatureStyleOptions (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoStyleOptions,
                DisplayText,
                EngravedText,
                IlluminatedCaps,
                TitlingCaps,
                TallCaps
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureStylisticAlternatives" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureStylisticAlternatives

```
public class CTFontFeatureStylisticAlternatives : CTFontFeatureSelectors {

        public CTFontFeatureStylisticAlternatives (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoStylisticAlternates,
                StylisticAltOneOn,
                StylisticAltOneOff,
                StylisticAltTwoOn,
                StylisticAltTwoOff,
                StylisticAltThreeOn,
                StylisticAltThreeOff,
                StylisticAltFourOn,
                StylisticAltFourOff,
                StylisticAltFiveOn,
                StylisticAltFiveOff,
                StylisticAltSixOn,
                StylisticAltSixOff,
                StylisticAltSevenOn,
                StylisticAltSevenOff,
                StylisticAltEightOn,
                StylisticAltEightOff,
                StylisticAltNineOn,
                StylisticAltNineOff,
                StylisticAltTenOn,
                StylisticAltTenOff,
                StylisticAltElevenOn,
                StylisticAltElevenOff,
                StylisticAltTwelveOn,
                StylisticAltTwelveOff,
                StylisticAltThirteenOn,
                StylisticAltThirteenOff,
                StylisticAltFourteenOn,
                StylisticAltFourteenOff,
                StylisticAltFifteenOn,
                StylisticAltFifteenOff,
                StylisticAltSixteenOn,
                StylisticAltSixteenOff,
                StylisticAltSeventeenOn,
                StylisticAltSeventeenOff,
                StylisticAltEighteenOn,
                StylisticAltEighteenOff,
                StylisticAltNineteenOn,
                StylisticAltNineteenOff,
                StylisticAltTwentyOn,
                StylisticAltTwentyOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureTextSpacing" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureTextSpacing

```
public class CTFontFeatureTextSpacing : CTFontFeatureSelectors {

        public CTFontFeatureTextSpacing (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                ProportionalText,
                MonospacedText,
                HalfWidthText,
                ThirdWidthText,
                QuarterWidthText,
                AltProportionalText,
                AltHalfWidthText
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureTransliteration" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureTransliteration

```
public class CTFontFeatureTransliteration : CTFontFeatureSelectors {

        public CTFontFeatureTransliteration (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NoTransliteration,
                HanjaToHangul,
                HiraganaToKatakana,
                KatakanaToHiragana,
                KanaToRomanization,
                RomanizationToHiragana,
                RomanizationToKatakana,
                HanjaToHangulAltOne,
                HanjaToHangulAltTwo,
                HanjaToHangulAltThree
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureTypographicExtras" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureTypographicExtras

```
public class CTFontFeatureTypographicExtras : CTFontFeatureSelectors {

        public CTFontFeatureTypographicExtras (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                HyphensToEmDashOn,
                HyphensToEmDashOff,
                HyphenToEnDashOn,
                HyphenToEnDashOff,
                SlashedZeroOn,
                SlashedZeroOff,
                FormInterrobangOn,
                FormInterrobangOff,
                SmartQuotesOn,
                SmartQuotesOff,
                PeriodsToEllipsisOn,
                PeriodsToEllipsisOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureUnicodeDecomposition" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureUnicodeDecomposition

```
public class CTFontFeatureUnicodeDecomposition : CTFontFeatureSelectors {

        public CTFontFeatureUnicodeDecomposition (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                CanonicalCompositionOn,
                CanonicalCompositionOff,
                CompatibilityCompositionOn,
                CompatibilityCompositionOff,
                TranscodingCompositionOn,
                TranscodingCompositionOff
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureUpperCase" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureUpperCase

```
public class CTFontFeatureUpperCase : CTFontFeatureSelectors {

        public CTFontFeatureUpperCase (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                DefaultUpperCase,
                UpperCaseSmallCaps,
                UpperCasePetiteCaps
        }
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontFeatureVerticalPosition" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureVerticalPosition

```
public class CTFontFeatureVerticalPosition : CTFontFeatureSelectors {

        public CTFontFeatureVerticalPosition (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                NormalPosition,
                Superiors,
                Inferiors,
                Ordinals,
                ScientificInferiors
        }
}
```

 <a name="" class="injected"></a>


### New Type: MonoTouch.CoreText.CTFontFeatureVerticalSubstitutionConnection 

```
public class CTFontFeatureVerticalSubstitutionConnection : CTFontFeatureSelectors {

        public CTFontFeatureVerticalSubstitutionConnection (MonoTouch.Foundation.NSDictionary dictionary);

        public Selector Feature {
                get;
        }

        [Serializable]
        public enum Selector {
                SubstituteVerticalFormsOn,
                SubstituteVerticalFormsOff
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontFeatures" class="injected"></a>


### Type Changed: MonoTouch.CoreText.CTFontFeatures

Removed:

```
public MonoTouch.Foundation.NSNumber Identifier {
```

Added:

```
public FontFeatureGroup FeatureGroup {
                get;
        }
        [Obsolete("Use Type instead")]
        public MonoTouch.Foundation.NSNumber Identifier {
```

 <a name="New_Type:_MonoTouch.CoreText.FontFeatureGroup" class="injected"></a>


### New Type: MonoTouch.CoreText.FontFeatureGroup

```
[Serializable]
public enum FontFeatureGroup {
        AllTypographicFeatures,
        Ligatures,
        CursiveConnection,
        LetterCase,
        VerticalSubstitution,
        LinguisticRearrangement,
        NumberSpacing,
        SmartSwash,
        Diacritics,
        VerticalPosition,
        Fractions,
        OverlappingCharacters,
        TypographicExtras,
        MathematicalExtras,
        OrnamentSets,
        CharacterAlternatives,
        DesignComplexity,
        StyleOptions,
        CharacterShape,
        NumberCase,
        TextSpacing,
        Transliteration,
        Annotation,
        KanaSpacing,
        IdeographicSpacing,
        UnicodeDecomposition,
        RubyKana,
        CJKSymbolAlternatives,
        IdeographicAlternatives,
        CJKVerticalRomanPlacement,
        ItalicCJKRoman,
        CaseSensitiveLayout,
        AlternateKana,
        StylisticAlternatives,
        ContextualAlternates,
        LowerCase,
        UpperCase,
        CJKRomanSpacing
}
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


## Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.DictionaryContainer" class="injected"></a>


### Type Changed: MonoTouch.Foundation.DictionaryContainer

Removed:

```
protected void SetNativeValue (NSString key, MonoTouch.ObjCRuntime.INativeObject value);
        protected void SetNumberValue (NSString key, Nullable<int> value);
        protected void SetNumberValue (NSString key, Nullable<uint> value);
```

Added:

```
protected T[] GetArray<T> (NSString key, Func<IntPtr,T> creator);
        protected NSDictionary GetNSDictionary (NSString key);
        protected string GetNSStringValue (NSString key);
        protected void SetNativeValue (NSString key, MonoTouch.ObjCRuntime.INativeObject value, bool removeNullValue);
        protected void SetNumberValue (NSString key, Nullable<uint> value);
        protected void SetNumberValue (NSString key, Nullable<int> value);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSIndexPath" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSIndexPath

Added:

```
public virtual int Item {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocol" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSUrlProtocol

Removed:

```
public virtual bool CanInitWithRequest (NSUrlRequest request);
```

Added:

```
public static bool CanInitWithRequest (NSUrlRequest request);
```

 <a name="Namespace:_MonoTouch.ImageIO" class="injected"></a>


## Namespace: MonoTouch.ImageIO

 <a name="Type_Changed:_MonoTouch.ImageIO.CGImageSource" class="injected"></a>


### Type Changed: MonoTouch.ImageIO.CGImageSource

Removed:

```
public MonoTouch.Foundation.NSDictionary CopyProperties (CGImageOptions options);
        public MonoTouch.Foundation.NSDictionary CopyProperties (CGImageOptions options, int imageIndex);
        public MonoTouch.Foundation.NSDictionary CopyProperties (MonoTouch.Foundation.NSDictionary dict);
        public MonoTouch.Foundation.NSDictionary CopyProperties (MonoTouch.Foundation.NSDictionary dict, int imageIndex);
```

Added:

```
[Obsolete("Use GetProperties")]
        public MonoTouch.Foundation.NSDictionary CopyProperties (CGImageOptions options);
        [Obsolete("Use GetProperties")]
        public MonoTouch.Foundation.NSDictionary CopyProperties (CGImageOptions options, int imageIndex);
        [Obsolete("Use GetProperties")]
        public MonoTouch.Foundation.NSDictionary CopyProperties (MonoTouch.Foundation.NSDictionary dict);
        [Obsolete("Use GetProperties")]
        public MonoTouch.Foundation.NSDictionary CopyProperties (MonoTouch.Foundation.NSDictionary dict, int imageIndex);
        public MonoTouch.CoreGraphics.CGImageProperties GetProperties (CGImageOptions options);
        public MonoTouch.CoreGraphics.CGImageProperties GetProperties (int index, CGImageOptions options);
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


## Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.LinkTarget" class="injected"></a>


### Type Changed: MonoTouch.ObjCRuntime.LinkTarget

Added:

```
ArmV7s
```

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added:

```
public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, int arg4, IntPtr arg5);
        public static void void_objc_msgSend_IntPtr_IntPtr_UInt32_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, uint arg3, int arg4);
        public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, int arg4, IntPtr arg5);
        public static void void_objc_msgSendSuper_IntPtr_IntPtr_UInt32_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, uint arg3, int arg4);
```

 <a name="Namespace:_MonoTouch.Security" class="injected"></a>


## Namespace: MonoTouch.Security

 <a name="Type_Changed:_MonoTouch.Security.SecCertificate" class="injected"></a>


### Type Changed: MonoTouch.Security.SecCertificate

Added:

```
public SecCertificate (byte [] data);
        public SecCertificate (System.Security.Cryptography.X509Certificates.X509Certificate certificate);
        public SecCertificate (System.Security.Cryptography.X509Certificates.X509Certificate2 certificate);
```

 <a name="Type_Changed:_MonoTouch.Security.SecPolicy" class="injected"></a>


### Type Changed: MonoTouch.Security.SecPolicy

Added:

```
public static SecPolicy CreateBasicX509Policy ();
        public static SecPolicy CreateSslPolicy (bool server, string hostName);
```

 <a name="Type_Changed:_MonoTouch.Security.SecTrust" class="injected"></a>


### Type Changed: MonoTouch.Security.SecTrust

Removed:

```
public class SecTrust {
        public SecTrust ();
```

Added:

```
public class SecTrust : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        public SecTrust (System.Security.Cryptography.X509Certificates.X509Certificate certificate, SecPolicy policy);
        public SecTrust (System.Security.Cryptography.X509Certificates.X509Certificate2 certificate, SecPolicy policy);
        public SecTrust (System.Security.Cryptography.X509Certificates.X509CertificateCollection certificates, SecPolicy policy);
        public SecTrust (System.Security.Cryptography.X509Certificates.X509Certificate2Collection certificates, SecPolicy policy);
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        public SecTrustResult Evaluate ();
        protected override void Finalize ();
        public MonoTouch.Foundation.NSData GetExceptions ();
        public SecKey GetPublicKey ();
        public double GetVerifyTime ();
        public SecStatusCode SetAnchorCertificates (System.Security.Cryptography.X509Certificates.X509Certificate2Collection certificates);
        public SecStatusCode SetAnchorCertificates (System.Security.Cryptography.X509Certificates.X509CertificateCollection certificates);
        public SecStatusCode SetAnchorCertificatesOnly (bool anchorCertificatesOnly);
        public bool SetExceptions (MonoTouch.Foundation.NSData data);
        public SecStatusCode SetVerifyDate (DateTime date);

        public int Count {
                get;
        }
        public IntPtr Handle {
                get;
        }
        public SecCertificate this [int index] {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Security.SecTrustResult" class="injected"></a>


### New Type: MonoTouch.Security.SecTrustResult

```
[Serializable]
public enum SecTrustResult {
        Invalid,
        Proceed,
        Confirm,
        Deny,
        Unspecified,
        RecoverableTrustFailure,
        FatalTrustFailure,
        ResultOtherError
}
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


## Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UICollectionViewController" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UICollectionViewController

Added:

```
public virtual void DecelerationEnded (UIScrollView scrollView);
        public virtual void DecelerationStarted (UIScrollView scrollView);
        public virtual void DidZoom (UIScrollView scrollView);
        public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
        public virtual void DraggingStarted (UIScrollView scrollView);
        public virtual void ScrollAnimationEnded (UIScrollView scrollView);
        public virtual void Scrolled (UIScrollView scrollView);
        public virtual void ScrolledToTop (UIScrollView scrollView);
        public virtual bool ShouldScrollToTop (UIScrollView scrollView);
        public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);
        public virtual void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
        public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
        public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UICollectionViewDelegate" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UICollectionViewDelegate

Added:

```
public virtual void DecelerationEnded (UIScrollView scrollView);
        public virtual void DecelerationStarted (UIScrollView scrollView);
        public virtual void DidZoom (UIScrollView scrollView);
        public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
        public virtual void DraggingStarted (UIScrollView scrollView);
        public virtual void ScrollAnimationEnded (UIScrollView scrollView);
        public virtual void Scrolled (UIScrollView scrollView);
        public virtual void ScrolledToTop (UIScrollView scrollView);
        public virtual bool ShouldScrollToTop (UIScrollView scrollView);
        public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);
        public virtual void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
        public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
        public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UICollectionViewSource" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UICollectionViewSource

Added:

```
public virtual void DecelerationEnded (UIScrollView scrollView);
        public virtual void DecelerationStarted (UIScrollView scrollView);
        public virtual void DidZoom (UIScrollView scrollView);
        public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
        public virtual void DraggingStarted (UIScrollView scrollView);
        public virtual void ScrollAnimationEnded (UIScrollView scrollView);
        public virtual void Scrolled (UIScrollView scrollView);
        public virtual void ScrolledToTop (UIScrollView scrollView);
        public virtual bool ShouldScrollToTop (UIScrollView scrollView);
        public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);
        public virtual void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
        public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
        public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIEvent" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIEvent

Removed:

```
public virtual MonoTouch.Foundation.NSSet TouchesForGestureRecognizer (UIGestureRecognizer window);
```

Added:

```
public virtual MonoTouch.Foundation.NSSet TouchesForGestureRecognizer (UIGestureRecognizer gesture);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIView

Removed:

```
public virtual bool TranslatesAutoresizingMaskIntoConstrainst {
```

Added:

```
public virtual bool TranslatesAutoresizingMaskIntoConstraints {
```
