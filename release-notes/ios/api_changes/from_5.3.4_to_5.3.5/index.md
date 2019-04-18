---
id: B2F77BD6-3AF4-4FA5-297D-E3D4DDDB7BF4
title: "From 5.3.4 to 5.3.5"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.3.4";
```

Added:

```
public const string Version = "5.3.5";
        public const string AudioUnitLibrary = "/System/Library/Frameworks/AudioToolbox.framework/AudioToolbox";
```

 <a name="New_Type:_MonoTouch.MonoNativeFunctionWrapperAttribute" class="injected"></a>


## New Type: MonoTouch.MonoNativeFunctionWrapperAttribute

```
public class MonoNativeFunctionWrapperAttribute : Attribute {
        
        public MonoNativeFunctionWrapperAttribute ();
}
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAsset

Removed:

```
public AVAsset ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetExportSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetExportSession

Removed:

```
public AVAssetExportSession ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetImageGenerator" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetImageGenerator

Removed:

```
public AVAssetImageGenerator ();
```

Added:

```
public virtual void GenerateCGImagesAsynchronously (MonoTouch.Foundation.NSValue[] cmTimesRequestedTimes, AVAssetImageGeneratorCompletionHandler handler);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReader" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReader

Removed:

```
public AVAssetReader ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput

Removed:

```
public AVAssetReaderAudioMixOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderOutput

Removed:

```
public AVAssetReaderOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderTrackOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderTrackOutput

Removed:

```
public AVAssetReaderTrackOutput ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput 

Removed:

```
public AVAssetReaderVideoCompositionOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetTrack

Removed:

```
public AVAssetTrack ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetWriter" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriter

Removed:

```
public AVAssetWriter ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetWriterInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput

Removed:

```
public AVAssetWriterInput ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriterInputPixelBufferAdaptor 

Removed:

```
public AVAssetWriterInputPixelBufferAdaptor ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Removed:

```
public AVCaptureDevice ();
```

Added:

```
public virtual bool IsFocusModeSupported (AVCaptureFocusMode focusMode);
        public virtual bool IsWhiteBalanceModeSupported (AVCaptureWhiteBalanceMode whiteBalanceMode);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDeviceInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDeviceInput

Removed:

```
public AVCaptureDeviceInput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureFileOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureFileOutput

Removed:

```
public AVCaptureFileOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureInput

Removed:

```
public AVCaptureInput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureOutput

Removed:

```
public AVCaptureOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVComposition" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVComposition

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCompositionTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCompositionTrack

Removed:

```
public AVCompositionTrack ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableCompositionTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableCompositionTrack

Removed:

```
public AVMutableCompositionTrack ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableVideoCompositionInstruction 

Added:

```
public virtual bool EnablePostProcessing {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayer

Removed:

```
public virtual void Seek (MonoTouch.CoreMedia.CMTime time, AVCompletionHandler completion);
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
                set;
```

Added:

```
public virtual void Seek (MonoTouch.CoreMedia.CMTime time, AVCompletion completion);
        public void Seek (MonoTouch.CoreMedia.CMTime time, AVCompletionHandler completion);
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletion completion);
        public void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItem

Removed:

```
public AVPlayerItem ();
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
                set;
```

Added:

```
public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletion completion);
        public void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVUrlAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVUrlAsset

Removed:

```
public AVUrlAsset ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideoCompositionValidationHandling 

Removed:

```
public AVVideoCompositionValidationHandling ();
```

 <a name="Namespace:_MonoTouch.Accounts" class="injected"></a>


# Namespace: MonoTouch.Accounts

 <a name="Type_Changed:_MonoTouch.Accounts.ACAccount" class="injected"></a>


## Type Changed: MonoTouch.Accounts.ACAccount

Removed:

```
public virtual string ErrorDomain {
                get;
        }
```

Added:

```
public static MonoTouch.Foundation.NSString ErrorDomain {
                get;
        }
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAAction" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAAction

Removed:

```
public CAAction ();
```

 <a name="Namespace:_MonoTouch.CoreData" class="injected"></a>


# Namespace: MonoTouch.CoreData

 <a name="Type_Changed:_MonoTouch.CoreData.NSAtomicStore" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSAtomicStore

Removed:

```
public NSAtomicStore ();
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSAtomicStoreCacheNode" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSAtomicStoreCacheNode

Removed:

```
public NSAtomicStoreCacheNode ();
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSManagedObject" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSManagedObject

Removed:

```
public NSManagedObject ();
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSManagedObjectID" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSManagedObjectID

Removed:

```
public NSManagedObjectID ();
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSPersistentStoreCoordinator" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator

Removed:

```
public static MonoTouch.Foundation.NSDictionary MetadataForPersistentStoreWithUrl (MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public static MonoTouch.Foundation.NSString ValidateXMLStoreOption {
                get;
        }
        public static MonoTouch.Foundation.NSString XMLStoreType {
                get;
        }
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


# Namespace: MonoTouch.CoreFoundation

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFRange" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFRange

Removed:

```
public CFRange (int l, int len);
        public int Location;
        public int Length;
```

Added:

```
public CFRange (int loc, int len);
        public CFRange (long l, long len);
        public override string ToString ();
        
        public int Length {
                get;
        }
        public int Location {
                get;
        }
        public long LongLength {
                get;
        }
        public long LongLocation {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFType" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFType

Added:

```
public string GetDescription (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFUrl" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFUrl

Added:

```
public string FileSystemPath {
                get;
        }
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPath" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPath

Added:

```
public void AddEllipseInRect (CGAffineTransform m, System.Drawing.RectangleF rect);
```

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


# Namespace: MonoTouch.CoreImage

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFeature" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFeature

Added:

```
public static MonoTouch.Foundation.NSString TypeFace {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFilter" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFilter

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFilterAttributes" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFilterAttributes

Removed:

```
public static MonoTouch.Foundation.NSString TypeOpaqueColor {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIImage" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIImage

Removed:

```
protected override void Dispose (bool disposing);
        public virtual CIImage ImageWithColor (CIColor color);
        public virtual MonoTouch.Foundation.NSObject IntPtr (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);
        public virtual MonoTouch.CoreGraphics.CGColorSpace ColorSpace {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
        }
```

Added:

```
public CIImage (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);
        public static CIImage ImageWithColor (CIColor color);
```

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


# Namespace: MonoTouch.CoreLocation

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLPlacemark" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLPlacemark

Removed:

```
public CLPlacemark ();
```

 <a name="Namespace:_MonoTouch.CoreMidi" class="injected"></a>


# Namespace: MonoTouch.CoreMidi

 <a name="Type_Changed:_MonoTouch.CoreMidi.MidiNetworkSession" class="injected"></a>


## Type Changed: MonoTouch.CoreMidi.MidiNetworkSession

Removed:

```
public MidiNetworkSession ();
```

 <a name="Namespace:_MonoTouch.CoreMotion" class="injected"></a>


# Namespace: MonoTouch.CoreMotion

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMAttitude" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMAttitude

Removed:

```
public CMAttitude ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMMotionManager" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMMotionManager

Removed:

```
public virtual void StartDeviceMotionUpdates (CMAttitudeReferenceFrame referenceFrame, MonoTouch.Foundation.NSOperationQueue queue, CMMagnetometerHandler handler);
                set;
```

Added:

```
public virtual void StartDeviceMotionUpdates (CMAttitudeReferenceFrame referenceFrame, MonoTouch.Foundation.NSOperationQueue queue, CMDeviceMotionHandler handler);
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


# Namespace: MonoTouch.EventKit

 <a name="Type_Changed:_MonoTouch.EventKit.EKEvent" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEvent

Removed:

```
public EKEvent ();
```

 <a name="Namespace:_MonoTouch.ExternalAccessory" class="injected"></a>


# Namespace: MonoTouch.ExternalAccessory

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EAAccessory" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EAAccessory

Removed:

```
public EAAccessory ();
```

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EAAccessoryManager" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager

Removed:

```
public EAAccessoryManager ();
```

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EASession" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EASession

Removed:

```
public EASession ();
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="New_Type:_MonoTouch.Foundation.NSAttributedRangeCallback" class="injected"></a>


## New Type: MonoTouch.Foundation.NSAttributedRangeCallback

```
[Serializable]
public delegate void NSAttributedRangeCallback (NSDictionary attrs, NSRange range, ref bool stop);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSAttributedString

Removed:

```
public static NSString BackgroundColorAttributeName {
                get;
        }
        public static NSString FontAttributeName {
                get;
        }
        public static NSString ForegroundColorAttributeName {
                get;
        }
        public static NSString LigatureAttributeName {
                get;
        }
        public static NSString LinkAttributeName {
                get;
        }
        public static NSString ParagraphStyleAttributeName {
                get;
        }
        public static NSString StrikethroughStyleAttributeName {
                get;
        }
        public static NSString StrokeWidthAttributeName {
                get;
        }
        public static NSString UnderlineStyleAttributeName {
                get;
        }
```

Added:

```
public virtual void EnumerateAttribute (NSString attributeName, NSRange inRange, NSAttributedStringEnumeration options, NSAttributedStringCallback callback);
        public virtual void EnumerateAttributes (NSRange range, NSAttributedStringEnumeration options, NSAttributedRangeCallback callback);
```

 <a name="New_Type:_MonoTouch.Foundation.NSAttributedStringCallback" class="injected"></a>


## New Type: MonoTouch.Foundation.NSAttributedStringCallback

```
[Serializable]
public delegate void NSAttributedStringCallback (NSObject value, NSRange range, ref bool stop);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSBundle" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSBundle

Added:

```
public virtual string [] Localizations {
                get;
        }
        public virtual string [] PreferredLocalizations {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSCachedUrlResponse" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCachedUrlResponse

Removed:

```
public NSCachedUrlResponse ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSCalendar" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCalendar

Removed:

```
public NSCalendar ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDecimalNumber" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDecimalNumber

Removed:

```
protected override void Dispose (bool disposing);
        public virtual NSDecimalNumber NaN {
                get;
        }
```

Added:

```
public static NSDecimalNumber NaN {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSException" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSException

Removed:

```
public NSException ();
```

Added:

```
public NSException (string name, string reason, NSDictionary userInfo);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSExpression" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSExpression

Removed:

```
public NSExpression ();
        public virtual NSExpression FromAggregate (NSExpression[] subexpressions);
```

Added:

```
public static NSExpression FromAggregate (NSExpression[] subexpressions);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileCoordinatorWritingOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileCoordinatorWritingOptions

Removed:

```
ForMerging
```

Added:

```
ForMerging,
        ForReplacing
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileVersion" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileVersion

Removed:

```
public NSFileVersion ();
        public virtual bool Discardable {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSHttpCookie" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSHttpCookie

Removed:

```
public NSHttpCookie ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSHttpCookieStorage" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSHttpCookieStorage

Removed:

```
public NSHttpCookieStorage ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSJsonSerialization" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSJsonSerialization

Removed:

```
public NSJsonSerialization ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSKeyedArchiver" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSKeyedArchiver

Removed:

```
public NSKeyedArchiver ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSKeyedUnarchiver" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSKeyedUnarchiver

Removed:

```
public NSKeyedUnarchiver ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSLocale" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSLocale

Removed:

```
public NSLocale ();
        public virtual string CanonicalLanguageIdentifierFromString (string str);
        public virtual string CanonicalLocaleIdentifierFromString (string str);
        public virtual NSLocaleLanguageDirection GetCharacterDirection (string isoLanguageCode);
        public virtual NSLocaleLanguageDirection GetLineDirection (string isoLanguageCode);
        public virtual string LocaleIdentifierFromComponents (NSDictionary dict);
```

Added:

```
public static string CanonicalLanguageIdentifierFromString (string str);
        public static string CanonicalLocaleIdentifierFromString (string str);
        public static NSLocaleLanguageDirection GetCharacterDirection (string isoLanguageCode);
        public static NSLocaleLanguageDirection GetLineDirection (string isoLanguageCode);
        public static string LocaleIdentifierFromComponents (NSDictionary dict);
        public string GetCountryCodeDisplayName (string value);
        public string GetIdentifierDisplayName (string value);
        public string GetLanguageCodeDisplayName (string value);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMetadataQuery" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMetadataQuery

Removed:

```
public static NSString LocalComputerScope {
                get;
        }
        public static NSString QueryLocalDocumentsScope {
                get;
        }
        public static NSString QueryNetworkScope {
                get;
        }
        public static NSString UserHomeScope {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNotification" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNotification

Removed:

```
public NSNotification ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumber" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumber

Removed:

```
public NSNumber ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumberFormatter" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumberFormatter

Removed:

```
public virtual string LocalizedStringFromNumbernumberStyle (NSNumber num, NSNumberFormatterStyle nstyle);
```

Added:

```
public static string LocalizedStringFromNumbernumberStyle (NSNumber num, NSNumberFormatterStyle nstyle);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSObject

Removed:

```
public static NSObject GetDefaultPlaceholder (NSObject marker, string binding);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSOrthography" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSOrthography

Removed:

```
public NSOrthography ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSPredicate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSPredicate

Removed:

```
public NSPredicate ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRunLoop" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRunLoop

Removed:

```
public NSRunLoop ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSThread" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSThread

Removed:

```
protected override void Dispose (bool disposing);
        public virtual NSThread MainThread {
                get;
        }
```

Added:

```
public static NSThread MainThread {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimeZone" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimeZone

Removed:

```
public NSTimeZone ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimer" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimer

Removed:

```
public NSTimer ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrl" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrl

Removed:

```
public NSUrl ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlAuthenticationChallenge" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlAuthenticationChallenge

Removed:

```
public NSUrlAuthenticationChallenge ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlCredential" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlCredential

Removed:

```
public NSUrlCredential ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlCredentialStorage" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlCredentialStorage

Removed:

```
public NSUrlCredentialStorage ();
        public virtual NSDictionary AllCredentials {
        public override IntPtr ClassHandle {
        public virtual NSUrlCredentialStorage SharedCredentialStorage {
```

Added:

```
public static NSUrlCredentialStorage SharedCredentialStorage {
        public virtual NSDictionary AllCredentials {
        public override IntPtr ClassHandle {
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtectionSpace" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtectionSpace

Removed:

```
public NSUrlProtectionSpace ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSValue" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSValue

Removed:

```
public NSValue ();
```

 <a name="Namespace:_MonoTouch.GLKit" class="injected"></a>


# Namespace: MonoTouch.GLKit

 <a name="Type_Changed:_MonoTouch.GLKit.GLKEffectPropertyTransform" class="injected"></a>


## Type Changed: MonoTouch.GLKit.GLKEffectPropertyTransform

Removed:

```
public virtual OpenTK.Matrix4 TextureMatrix {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.GLKit.GLKTextureInfo" class="injected"></a>


## Type Changed: MonoTouch.GLKit.GLKTextureInfo

Removed:

```
public virtual uint TextureName {
                get;
        }
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievement" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievement

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementDescription" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementDescription

Removed:

```
public virtual MonoTouch.UIKit.UIImage IncompleteAchievementImage {
                get;
        }
```

Added:

```
public static MonoTouch.UIKit.UIImage IncompleteAchievementImage {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKFriendRequestComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Removed:

```
public virtual void AddRecipientsFromAliases (string [] aliases);
        public virtual void AddRecipientsFromPlayerIDs (string [] emailAddresses);
```

Added:

```
public virtual void AddRecipientsFromPlayerIDs (string [] playerIDs);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatch" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatch

Removed:

```
public GKMatch ();
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPeerPickerController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPeerPickerController

Removed:

```
set;
```

 <a name="Namespace:_MonoTouch.ImageIO" class="injected"></a>


# Namespace: MonoTouch.ImageIO

 <a name="New_Type:_MonoTouch.ImageIO.CGImageProperties" class="injected"></a>


## New Type: MonoTouch.ImageIO.CGImageProperties

```
public class CGImageProperties {
        
        public CGImageProperties ();
        
        public static MonoTouch.Foundation.NSString CIFFCameraSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFContinuousDrive {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFFirmware {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFFlashExposureComp {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFFocusMode {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFImageFileName {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFImageName {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFImageSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFLensMaxMM {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFLensMinMM {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFLensModel {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFMeasuredEV {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFMeteringMode {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFOwnerName {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFRecordID {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFReleaseMethod {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFReleaseTiming {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFSelfTimingTime {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFShootingMode {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFWhiteBalanceIndex {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModel {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModelCMYK {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModelGray {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModelLab {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModelRGB {
                get;
        }
        public static MonoTouch.Foundation.NSString Depth {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGBackwardVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGCameraSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGLensInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGLocalizedCameraModel {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGUniqueCameraModel {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString DPIHeight {
                get;
        }
        public static MonoTouch.Foundation.NSString DPIWidth {
                get;
        }
        public static MonoTouch.Foundation.NSString EightBIMDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString EightBIMLayerNames {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifApertureValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxFirmware {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxFlashCompensation {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxImageNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxLensID {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxLensInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxLensModel {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxLensSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxOwnerName {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifBodySerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifBrightnessValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifCameraOwnerName {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifCFAPattern {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifColorSpace {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifComponentsConfiguration {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifCompressedBitsPerPixel {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifContrast {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifCustomRendered {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDateTimeDigitized {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDateTimeOriginal {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDeviceSettingDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDigitalZoomRatio {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureBiasValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureIndex {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureMode {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureProgram {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFileSource {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFlash {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFlashEnergy {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFlashPixVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalLength {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalLenIn35mmFilm {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalPlaneResolutionUnit {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalPlaneXResolution {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalPlaneYResolution {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifGainControl {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifGamma {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifImageUniqueID {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifISOSpeedRatings {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLensMake {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLensModel {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLensSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLensSpecification {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLightSource {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifMakerNote {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifMaxApertureValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifMeteringMode {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifOECF {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifPixelXDimension {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifPixelYDimension {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifRelatedSoundFile {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSaturation {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSceneCaptureType {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSceneType {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSensingMethod {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSharpness {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifShutterSpeedValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSpatialFrequencyResponse {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSpectralSensitivity {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubjectArea {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubjectDistance {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubjectDistRange {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubjectLocation {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubsecTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubsecTimeDigitized {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubsecTimeOrginal {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifUserComment {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifWhiteBalance {
                get;
        }
        public static MonoTouch.Foundation.NSString FileSize {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFDelayTime {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFHasGlobalColorMap {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFImageColorMap {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFLoopCount {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFUnclampedDelayTime {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSAltitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSAltitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSAreaInformation {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDateStamp {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestBearing {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestBearingRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestDistance {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestDistanceRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestLatitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestLatitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestLongitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestLongitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDifferental {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDOP {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSImgDirection {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSImgDirectionRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSLatitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSLatitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSLongitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSLongitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSMapDatum {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSMeasureMode {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSSatellites {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSSpeed {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSSpeedRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSStatus {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSTimeStamp {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSTrack {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSTrackRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString HasAlpha {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCActionAdvised {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCByline {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCBylineTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCaptionAbstract {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCategory {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCity {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContact {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoAddress {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoCity {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoCountry {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoEmails {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoPhones {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoPostalCode {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoStateProvince {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoWebURLs {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContentLocationCode {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContentLocationName {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCopyrightNotice {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCountryPrimaryLocationCode {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCountryPrimaryLocationName {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCreatorContactInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCredit {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCDateCreated {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCDigitalCreationDate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCDigitalCreationTime {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCEditorialUpdate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCEditStatus {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCExpirationDate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCExpirationTime {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCFixtureIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCHeadline {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCImageOrientation {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCImageType {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCKeywords {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCLanguageIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCObjectAttributeReference {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCObjectCycle {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCObjectName {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCObjectTypeReference {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCOriginalTransmissionReference {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCOriginatingProgram {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCProgramVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCProvinceState {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReferenceDate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReferenceNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReferenceService {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReleaseDate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReleaseTime {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCRightsUsageTerms {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCScene {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSource {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSpecialInstructions {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCStarRating {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSubjectReference {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSubLocation {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSupplementalCategory {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCTimeCreated {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCUrgency {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCWriterEditor {
                get;
        }
        public static MonoTouch.Foundation.NSString IsFloat {
                get;
        }
        public static MonoTouch.Foundation.NSString IsIndexed {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFDensityUnit {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFIsProgressive {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFXDensity {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFYDensity {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonAspectRatioInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonCameraSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonContinuousDrive {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonFirmware {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonFlashExposureComp {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonImageSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonLensModel {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonOwnerName {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerFujiDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerMinoltaDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonCameraSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonColorMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonDigitalZoom {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonFlashExposureComp {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonFlashSetting {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonFocusDistance {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonFocusMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonImageAdjustment {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonISOSelection {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonISOSetting {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonLensAdapter {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonLensInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonLensType {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonQuality {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonSharpenMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonShootingMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonShutterCount {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonWhiteBalanceMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerOlympusDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerPentaxDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString Orientation {
                get;
        }
        public static MonoTouch.Foundation.NSString PixelHeight {
                get;
        }
        public static MonoTouch.Foundation.NSString PixelWidth {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGAuthor {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGChromaticities {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGCopyright {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGCreationTime {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGGamma {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGInterlaceType {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGModificationTime {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGSoftware {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGsRGBIntent {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGXPixelsPerMeter {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGYPixelsPerMeter {
                get;
        }
        public static MonoTouch.Foundation.NSString ProfileName {
                get;
        }
        public static MonoTouch.Foundation.NSString RawDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFCompression {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFDateTime {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFDocumentName {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFHostComputer {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFImageDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFMake {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFModel {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFOrientation {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFPhotometricInterpretation {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFPrimaryChromaticities {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFResolutionUnit {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFSoftware {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFTransferFunction {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFWhitePoint {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFXResolution {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFYResolution {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.ImageIO.CGImageSource" class="injected"></a>


## Type Changed: MonoTouch.ImageIO.CGImageSource

Added:

```
public MonoTouch.Foundation.NSDictionary CopyProperties (CGImageOptions options);
        public MonoTouch.Foundation.NSDictionary CopyProperties (CGImageOptions options, int imageIndex);
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="Type_Changed:_MonoTouch.MapKit.MKOverlay" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKOverlay

Removed:

```
public MKOverlay ();
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPinAnnotationView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Removed:

```
public MKPinAnnotationView ();
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPlacemark" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPlacemark

Removed:

```
public MKPlacemark ();
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKReverseGeocoder" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKReverseGeocoder

Removed:

```
public MKReverseGeocoder ();
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItem" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItem

Added:

```
public MonoTouch.Foundation.NSString AlbumArtist {
                get;
        }
        public ulong AlbumArtistPersistentID {
                get;
        }
        public ulong AlbumPersistentID {
                get;
        }
        public MonoTouch.Foundation.NSString AlbumTitle {
                get;
        }
        public int AlbumTrackCount {
                get;
        }
        public int AlbumTrackNumber {
                get;
        }
        public MonoTouch.Foundation.NSString Artist {
                get;
        }
        public ulong ArtistPersistentID {
                get;
        }
        public MPMediaItemArtwork Artwork {
                get;
        }
        public MonoTouch.Foundation.NSUrl AssetURL {
                get;
        }
        public uint BeatsPerMinute {
                get;
        }
        public MonoTouch.Foundation.NSString Comments {
                get;
        }
        public MonoTouch.Foundation.NSString Composer {
                get;
        }
        public ulong ComposerPersistentID {
                get;
        }
        public int DiscCount {
                get;
        }
        public int DiscNumber {
                get;
        }
        public MonoTouch.Foundation.NSString Genre {
                get;
        }
        public ulong GenrePersistentID {
                get;
        }
        public bool IsCompilation {
                get;
        }
        public MonoTouch.Foundation.NSDate LastPlayedDate {
                get;
        }
        public MonoTouch.Foundation.NSString Lyrics {
                get;
        }
        public MPMediaType MediaType {
                get;
        }
        public ulong PersistentID {
                get;
        }
        public double PlaybackDuration {
                get;
        }
        public int PlayCount {
                get;
        }
        public ulong PodcastPersistentID {
                get;
        }
        public MonoTouch.Foundation.NSString PodcastTitle {
                get;
        }
        public uint Rating {
                get;
        }
        public MonoTouch.Foundation.NSDate ReleaseDate {
                get;
        }
        public int SkipCount {
                get;
        }
        public MonoTouch.Foundation.NSString Title {
                get;
        }
        public MonoTouch.Foundation.NSString UserGrouping {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItemCollection" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItemCollection

Removed:

```
public MPMediaItemCollection ();
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaPlaylist" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaPlaylist

Removed:

```
public MPMediaPlaylist ();
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaQuerySection" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaQuerySection

Removed:

```
public MPMediaQuerySection ();
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPNowPlayingInfoCenter" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPNowPlayingInfoCenter

Removed:

```
public MPNowPlayingInfoCenter ();
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPTimedMetadata" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPTimedMetadata

Removed:

```
public MPTimedMetadata ();
```

 <a name="Namespace:_MonoTouch.NewsstandKit" class="injected"></a>


# Namespace: MonoTouch.NewsstandKit

 <a name="Type_Changed:_MonoTouch.NewsstandKit.NKAssetDownload" class="injected"></a>


## Type Changed: MonoTouch.NewsstandKit.NKAssetDownload

Removed:

```
public NKAssetDownload ();
```

 <a name="Type_Changed:_MonoTouch.NewsstandKit.NKIssue" class="injected"></a>


## Type Changed: MonoTouch.NewsstandKit.NKIssue

Removed:

```
public NKIssue ();
```

 <a name="Type_Changed:_MonoTouch.NewsstandKit.NKLibrary" class="injected"></a>


## Type Changed: MonoTouch.NewsstandKit.NKLibrary

Removed:

```
public NKLibrary ();
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

Added:

```
public static void void_objc_msgSend_IntPtr_NSRange_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_IntPtr_NSRange_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, IntPtr arg4);
```

 <a name="Namespace:_MonoTouch.OpenGLES" class="injected"></a>


# Namespace: MonoTouch.OpenGLES

 <a name="Type_Changed:_MonoTouch.OpenGLES.EAGLSharegroup" class="injected"></a>


## Type Changed: MonoTouch.OpenGLES.EAGLSharegroup

Removed:

```
public EAGLSharegroup ();
```

 <a name="Type_Removed:_MonoTouch.QuickLook.QLThumbnailImage" class="injected"></a>


## Type Removed: MonoTouch.QuickLook.QLThumbnailImage

 <a name="Namespace:_MonoTouch.SystemConfiguration" class="injected"></a>


# Namespace: MonoTouch.SystemConfiguration

 <a name="Type_Changed:_MonoTouch.SystemConfiguration.CaptiveNetwork" class="injected"></a>


## Type Changed: MonoTouch.SystemConfiguration.CaptiveNetwork

Removed:

```
public class CaptiveNetwork {
        
        public CaptiveNetwork ();
```

Added:

```
public static class CaptiveNetwork {
        public static StatusCode TryCopyCurrentNetworkInfo (string interfaceName, out MonoTouch.Foundation.NSDictionary currentNetworkInfo);
        public static StatusCode TryGetSupportedInterfaces (out string [] supportedInterfaces);
```

 <a name="Type_Changed:_MonoTouch.SystemConfiguration.NetworkReachability" class="injected"></a>


## Type Changed: MonoTouch.SystemConfiguration.NetworkReachability

Added:

```
public NetworkReachability (System.Net.IPAddress localAddress, System.Net.IPAddress remoteAddress);
        public StatusCode GetFlags (out NetworkReachabilityFlags flags);
        public StatusCode SetNotification (Notification callback);
```

 <a name="New_Type:_MonoTouch.SystemConfiguration.StatusCode" class="injected"></a>


## New Type: MonoTouch.SystemConfiguration.StatusCode

```
[Serializable]
public enum StatusCode {
        OK,
        Failed,
        InvalidArgument,
        AccessError,
        NoKey,
        KeyExists,
        Locked,
        NeedLock,
        NoStoreSession,
        NoStoreServer,
        NotifierActive,
        NoPrefsSession,
        PrefsBusy,
        NoConfigFile,
        NoLink,
        Stale,
        MaxLink,
        ReachabilityUnknown,
        ConnectionNoService
}
```

 <a name="New_Type:_MonoTouch.SystemConfiguration.StatusCodeError" class="injected"></a>


## New Type: MonoTouch.SystemConfiguration.StatusCodeError

```
public static class StatusCodeError {
        
        public static string GetErrorDescription (StatusCode statusCode);
}
```

 <a name="New_Type:_MonoTouch.SystemConfiguration.SystemConfigurationException" class="injected"></a>


## New Type: MonoTouch.SystemConfiguration.SystemConfigurationException

```
public class SystemConfigurationException : Exception {
        
        public SystemConfigurationException (StatusCode statusErrorCode);
        
        public StatusCode StatusErrorCode {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIActionSheet" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIActionSheet

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIAlertView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAlertView

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIAppearance" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAppearance

Removed:

```
public UIAppearance ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

Removed:

```
public static MonoTouch.Foundation.NSString MinimumKeepAliveTimeout {
                set;
```

Added:

```
public static double MinimumKeepAliveTimeout {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBezierPath" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBezierPath

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIColor" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIColor

Removed:

```
public UIColor ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDocumentInteractionController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDocumentInteractionController

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerController

Removed:

```
public virtual MonoTouch.Foundation.NSNumber[] AvailableCaptureModesForCameraDevice (UIImagePickerControllerCameraDevice cameraDevice);
```

Added:

```
public static MonoTouch.Foundation.NSNumber[] AvailableCaptureModesForCameraDevice (UIImagePickerControllerCameraDevice cameraDevice);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIManagedDocument" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIManagedDocument

Removed:

```
public UIManagedDocument ();
```

Added:

```
public UIManagedDocument (MonoTouch.Foundation.NSUrl url);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPasteboard" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPasteboard

Removed:

```
public UIPasteboard ();
                set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPinchGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPinchGestureRecognizer

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPrintInfo" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPrintInfo

Removed:

```
public UIPrintInfo ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPrintInteractionController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPrintInteractionController

Removed:

```
public UIPrintInteractionController ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIReferenceLibraryViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIReferenceLibraryViewController

Removed:

```
public UIReferenceLibraryViewController ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIRotationGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIRotationGestureRecognizer

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScrollView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScrollView

Removed:

```
set;
                set;
                set;
                set;
                set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISimpleTextPrintFormatter" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISimpleTextPrintFormatter

Removed:

```
public virtual UILineBreakMode LineBreakMode {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISlider" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISlider

Removed:

```
set;
                set;
                set;
```

Added:

```
public virtual UIImage MaxValueImage {
                        get;
                        set;
                }
                public virtual UIImage MinValueImage {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBarController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBarController

Removed:

```
set;
```

 <a name="Type_Removed:_MonoTouch.iAd.ADManager" class="injected"></a>


## Type Removed: MonoTouch.iAd.ADManager
