---
id: 40172F9A-39AC-8C5B-5F31-78D226DD81AA
title: "From 5.0 to 5.2"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


## Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


### Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.0.2";
```

Added:

```
public const string Version = "5.2.0";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioPlayer

Removed:

```
public AVAudioPlayer ();
```

 <a name="Type_Changed:_MonoTouch.4AVFoundation.AVPlayerItem" class="injected"></a>


## Type Changed: MonoTouch.4AVFoundation.AVPlayerItem

Added:

```
public virtual MonoTouch.Foundation.NSValue[] LoadedTimeRanges {
                get;
        }
        public virtual MonoTouch.Foundation.NSValue[] SeekableTimeRanges {
                get;
        }
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsLibrary" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary

Added:

```
public virtual void WriteImageToSavedPhotosAlbum (
                CGImage imageData,
                ALAssetOrientation orientation,
                ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public virtual void WriteImageToSavedPhotosAlbum (
                CGImage imageData, NSDictionary metadata,
                ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public static MonoTouch.Foundation.NSString ChangedNotification {
                get;
        }
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFile" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFile

Added:

```
public static AudioFile OpenRead (CFUrl url, AudioFileType fileTypeHint);
        public int WritePackets (bool useCache, long inStartingPacket,
                int numPackets, IntPtr buffer, int count);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSession" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSession

Added:

```
public static AudioSessionInputRouteKind InputRoute {
                get;
        }
        public static AudioSessionMode Mode {
                get;
                set;
        }
        public static AudioSessionOutputRouteKind[] OutputRoutes {
                get;
        }
        public static bool OverrideCategoryDefaultToSpeaker {
                get;
                set;
        }
        public static bool OverrideCategoryEnableBluetoothInput {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionInputRouteKind" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSessionInputRouteKind

Added:

```
[Serializable]
 public enum AudioSessionInputRouteKind {
        None,
        LineIn,
        BuiltInMic,
        HeadsetMic,
        BluetoothHFP,
        USBAudio
 }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionMode" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSessionMode

Added:

```
[Serializable]
 public enum AudioSessionMode {
        Default,
        VoiceChat,
        VideoRecording,
        Measurement
 }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionOutputRouteKind" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSessionOutputRouteKind

Added:

```
[Serializable]
 public enum AudioSessionOutputRouteKind {
        None,
        LineOut,
        Headphones,
        BluetoothHFP,
        BluetoothA2DP,
        BuiltInReceiver,
        BuiltInSpeaker,
        USBAudio,
        HDMI,
        AirPlay
 }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionProperty" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSessionProperty

Added:

```
AudioRouteDescription,
        OverrideCategoryDefaultToSpeaker,
        OverrideCategoryEnableBluetoothInput,
        Mode,
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CALayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CALayer

Removed:

```
public virtual CAAction ActionForKey (string eventKey);
        public virtual CAAction DefaultActionForKey (string eventKey);
```

Added:

```
public static NSObject DefaultActionForKey (string eventKey);
        public virtual NSObject ActionForKey (string eventKey);
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CALayerDelegate" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CALayerDelegate

Removed:

```
public virtual CAAction ActionForLAyer (CALayer layer, string eventKey);
```

Added:

```
public virtual NSObject ActionForLayer (CALayer layer, string eventKey);
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


# Namespace: MonoTouch.CoreFoundation

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFString" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFString

Added:

```
public CFString (IntPtr handle);
        public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFUrl" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFUrl

Added:

```
public override string ToString ();
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGColorSpace" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGColorSpace

Added:

```
public static CGColorSpace CreateIndexed (
                CGColorSpace baseSpace, int lastIndex, byte [] colorTable);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGLayer

Added:

```
public System.Drawing.SizeF Size {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFArray" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFArray

Added:

```
public bool GetString (int idx, out string result);
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="New_Type:_MonoTouch.Foundation.NSAlignmentOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSAlignmentOptions

```
[Serializable]
[Flags]
public enum NSAlignmentOptions : long {
        MinXInward,
        MinYInward,
        MaxXInward,
        MaxYInward,
        WidthInward,
        HeightInward,
        MinXOutward,
        MinYOutward,
        MaxXOutward,
        MaxYOutward,
        WidthOutward,
        HeightOutward,
        MinXNearest,
        MinYNearest,
        MaxXNearest,
        MaxYNearest,
        WidthNearest,
        HeightNearest,
        RectFlipped,
        AllEdgesInward,
        AllEdgesOutward,
        AllEdgesNearest
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSAttributedString

Added:

```
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

 <a name="Type_Changed:_MonoTouch.Foundation.NSData" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSData

Added:

```
public static NSData FromFile (string path, NSDataReadingOptions mask, out NSError error);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDate

Added:

```
public static NSDate FromTimeIntervalSince1970 (double secs);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileManager" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileManager

Added:

```
public static bool GetSkipBackupAttribute (string filename);
        public static bool GetSkipBackupAttribute (string filename, out NSError error);
        public static NSError SetSkipBackupAttribute (string filename, bool skipBackup);
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileWrapper" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileWrapper

```
public class NSFileWrapper : NSObject {
        
        public NSFileWrapper ();
        public NSFileWrapper (NSCoder coder);
        public NSFileWrapper (NSObjectFlag t);
        public NSFileWrapper (IntPtr handle);
        public NSFileWrapper (NSUrl url, NSFileWrapperReadingOptions options, out NSError outError);
        public NSFileWrapper (NSDictionary childrenByPreferredName);
        public NSFileWrapper (NSData contents);
        public NSFileWrapper (NSUrl urlToSymbolicLink);
        
        public virtual string AddFileWrapper (NSFileWrapper child);
        public virtual string AddRegularFile (NSData dataContents, string preferredFilename);
        protected override void Dispose (bool disposing);
        public virtual NSData GetRegularFileContents ();
        public virtual NSData GetSerializedRepresentation ();
        public virtual string KeyForFileWrapper (NSFileWrapper child);
        public virtual bool MatchesContentsOfURL (NSUrl url);
        public virtual bool Read (NSUrl url, NSFileWrapperReadingOptions options, 
                out NSError outError);
        public virtual void RemoveFileWrapper (NSFileWrapper child);
        public virtual bool Write (NSUrl url, NSFileWrapperWritingOptions options, 
                NSUrl originalContentsURL, out NSError outError);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSDictionary FileAttributes {
                get;
                set;
        }
        public virtual string Filename {
                get;
                set;
        }
        public virtual NSDictionary FileWrappers {
                get;
        }
        public virtual bool IsDirectory {
                get;
        }
        public virtual bool IsRegularFile {
                get;
        }
        public virtual bool IsSymbolicLink {
                get;
        }
        public virtual string PreferredFilename {
                get;
                set;
        }
        public virtual NSUrl SymbolicLinkDestinationURL {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileWrapperReadingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileWrapperReadingOptions

```
[Serializable]
[Flags]
public enum NSFileWrapperReadingOptions {
        Immediate,
        WithoutMapping
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileWrapperWritingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileWrapperWritingOptions

```
[Serializable]
[Flags]
public enum NSFileWrapperWritingOptions {
        Atomic,
        WithNameUpdating
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSLocale" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSLocale

Added:

```
public string AlternateQuotationBeginDelimiterKey {
                get;
        }
        public string AlternateQuotationEndDelimiterKey {
                get;
        }
        public NSCalendar Calendar {
                get;
        }
        public string CollationIdentifier {
                get;
        }
        public string CollatorIdentifier {
                get;
        }
        public string CountryCode {
                get;
        }
        public string CurrencyCode {
                get;
        }
        public string CurrencySymbol {
                get;
        }
        public string DecimalSeparator {
                get;
        }
        public NSCharacterSet ExemplarCharacterSet {
                get;
        }
        public string GroupingSeparator {
                get;
        }
        public string Identifier {
                get;
        }
        public string LanguageCode {
                get;
        }
        public string MeasurementSystem {
                get;
        }
        public string QuotationBeginDelimiterKey {
                get;
        }
        public string QuotationEndDelimiterKey {
                get;
        }
        public string ScriptCode {
                get;
        }
        public bool UsesMetricSystem {
                get;
        }
        public string VariantCode {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSMutableArray" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMutableArray

```
public class NSMutableArray : NSArray {
        
        public NSMutableArray ();
        public NSMutableArray (NSCoder coder);
        public NSMutableArray (NSObjectFlag t);
        public NSMutableArray (IntPtr handle);
        public NSMutableArray (int capacity);
        
        public virtual void Add (NSObject obj);
        public virtual void AddObjects (NSObject[] source);
        public virtual void Insert (NSObject obj, int index);
        public virtual void InsertObjects (NSObject[] objects, NSIndexSet atIndexes);
        public virtual void RemoveAllObjects ();
        public virtual void RemoveLastObject ();
        public virtual void RemoveObject (int index);
        public virtual void RemoveObjectsAtIndexes (NSIndexSet indexSet);
        public virtual void ReplaceObject (int index, NSObject withObject);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSObject

Added:

```
protected static bool IsNewRefcountEnabled ();
        protected void MarkDirty ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSString

Added:

```
public virtual NSComparisonResult Compare (NSString aString);
        public virtual NSComparisonResult Compare (NSString aString, NSStringCompareOptions mask);
        public virtual NSComparisonResult Compare (NSString aString, NSStringCompareOptions mask, 
                NSRange range);
        public virtual NSComparisonResult Compare (NSString aString, NSStringCompareOptions mask, 
                NSRange range, NSLocale locale);
        public virtual NSString Replace (NSRange range, NSString replacement);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSStringCompareOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSStringCompareOptions

Added:

```
[Serializable]
 public enum NSStringCompareOptions : uint {
        CaseInsensitiveSearch,
        LiteralSearch,
        BackwardsSearch,
        AnchoredSearch,
        NumericSearch,
        DiacriticInsensitiveSearch,
        WidthInsensitiveSearch,
        ForcedOrderingSearch,
        RegularExpressionSearch
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimeZone" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimeZone

Added:

```
public NSTimeZone (string name, NSData data);
        public static NSTimeZone FromName (string tzName, NSData data);
        public static string DataVersion {
                get;
        }
        public static System.Collections.ObjectModel.ReadOnlyCollection<string> KnownTimeZoneNames {
                get;
        }
```

 <a name="Namespace:_MonoTouch.GLKit" class="injected"></a>


# Namespace: MonoTouch.GLKit

 <a name="Type_Changed:_MonoTouch.GLKit.GLKView" class="injected"></a>


## Type Changed: MonoTouch.GLKit.GLKView

Added:

```
public GLKView (System.Drawing.RectangleF frame);
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="Type_Changed:_MonoTouch.MapKit.MKAnnotationView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKAnnotationView

Added:

```
public MKAnnotationView (System.Drawing.RectangleF frame);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKCircleView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKCircleView

Added:

```
public MKCircleView (System.Drawing.RectangleF frame);
```

 <a name="New_Type:_MonoTouch.MapKit.MKGeometry" class="injected"></a>


## New Type: MonoTouch.MapKit.MKGeometry

```
public static class MKGeometry {
        
        public static double MapPointsPerMeterAtLatitude (double latitude);
        public static double MetersBetweenMapPoints (MKMapPoint a, MKMapPoint b);
        public static double MetersPerMapPointAtLatitude (double latitude);
}
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapPoint" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapPoint

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapRect" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapRect

Added:

```
public static MKMapRect Intersection (MKMapRect rect1, MKMapRect rect2);
        public static bool Intersects (MKMapRect rect1, MKMapRect rect2);
        public static MKMapRect Union (MKMapRect rect1, MKMapRect rect2);
        public bool Contains (MKMapPoint point);
        public bool Contains (MKMapRect rect);
        public MKMapRect Divide (double amount, CGRectEdge edge, out MKMapRect remainder);
        public override bool Equals (object other);
        public override int GetHashCode ();
        public MKMapRect Inset (double dx, double dy);
        public MKMapRect Offset (double dx, double dy);
        public MKMapRect Remainder ();
        public override string ToString ();
        
        public static bool operator == (MKMapRect a, MKMapRect b);
        public static bool operator != (MKMapRect a, MKMapRect b);
        
        public bool Spans180thMeridian {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapSize" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapSize

Added:

```
public override bool Equals (object other);
        public override int GetHashCode ();
        public override string ToString ();
        
        public static bool operator == (MKMapSize a, MKMapSize b);
        public static bool operator != (MKMapSize a, MKMapSize b);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapView

Removed:

```
public virtual void DeselectAnnotation (MKAnnotation annotation, bool animated);
        public virtual MKAnnotationView ViewForAnnotation (MKAnnotation annotation);
```

Added:

```
public MKMapView (System.Drawing.RectangleF frame);
        public void AddAnnotations (MKAnnotation[] annotations);
        public virtual void DeselectAnnotation (Foundation.NSObject annotation, bool animated);
        public virtual MKAnnotationView ViewForAnnotation (Foundation.NSObject annotation);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKOverlayPathView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKOverlayPathView

Added:

```
public MKOverlayPathView (System.Drawing.RectangleF frame);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKOverlayView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKOverlayView

Added:

```
public MKOverlayView (System.Drawing.RectangleF frame);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolygon" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolygon

Added:

```
public virtual bool Intersects (MKMapRect rect);
        public virtual MKMapRect BoundingMapRect {
                get;
        }
        public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolygonView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolygonView

Added:

```
public MKPolygonView (System.Drawing.RectangleF frame);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolyline" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolyline

Removed:

```
set;
        }
        public virtual string Subtitle {
                get;
        }
        public virtual string Title {
                get;
```

Added:

```
public static MKPolyline FromPoints (MKMapPoint[] points);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolylineView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolylineView

Added:

```
public MKPolylineView (System.Drawing.RectangleF frame);
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

Added:

```
public static bool bool_objc_msgSend_IntPtr_int_IntPtr_IntPtr (
                IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3, IntPtr arg4);
        public static bool bool_objc_msgSendSuper_IntPtr_int_IntPtr_IntPtr (
                IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3, IntPtr arg4);
        public static int int_objc_msgSend_IntPtr_UInt32 (
                IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
        public static int int_objc_msgSend_IntPtr_UInt32_NSRange (
                IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, NSRange arg3);
        public static int int_objc_msgSend_IntPtr_UInt32_NSRange_IntPtr (
                IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, NSRange arg3, IntPtr arg4);
        public static int int_objc_msgSendSuper_IntPtr_UInt32 (
                IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
        public static int int_objc_msgSendSuper_IntPtr_UInt32_NSRange (
                IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, NSRange arg3);
        public static int int_objc_msgSendSuper_IntPtr_UInt32_NSRange_IntPtr (
                IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, NSRange arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSend_NSRange_IntPtr (
                IntPtr receiver, IntPtr selector, NSRange arg1, IntPtr arg2);
        public static IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr (
                IntPtr receiver, IntPtr selector, NSRange arg1, IntPtr arg2);
```

 <a name="Namespace:_MonoTouch.Security" class="injected"></a>


# Namespace: MonoTouch.Security

 <a name="New_Type:_MonoTouch.Security.SecImportExport" class="injected"></a>


## New Type: MonoTouch.Security.SecImportExport

```
public class SecImportExport {
        
        public SecImportExport ();
        
        public static SecStatusCode ImportPkcs12 (
                byte [] buffer, NSDictionary options, out NSDictionary[] array);
        public static SecStatusCode ImportPkcs12 (
                NSData data, NSDictionary options, out NSDictionary[] array);
        
        public static NSString CertChain {
                get;
        }
        public static NSString Identity {
                get;
        }
        public static NSString KeyId {
                get;
        }
        public static NSString Label {
                get;
        }
        public static NSString Passphrase {
                get;
        }
        public static NSString Trust {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Security.SecRecord" class="injected"></a>


## Type Changed: MonoTouch.Security.SecRecord

Added:

```
public NSObject ValueRef {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIAlertView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAlertView

Added:

```
public UIAlertView (System.Drawing.RectangleF frame);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

Removed:

```
public static NSString BackgroundTaskInvalid {
```

Added:

```
public static int BackgroundTaskInvalid {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIColor" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIColor

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImage" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImage

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISplitViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISplitViewController

Removed:

```
public virtual bool ShouldHideViewController (
                UISplitViewController svc, UIViewController viewController, UIInterfaceOrientation inOrientation);
```

Added:

```
public UISplitViewControllerHidePredicate ShouldHideViewController {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISplitViewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISplitViewControllerDelegate

Added:

```
public virtual bool ShouldHideViewController (
                UISplitViewController svc, UIViewController viewController, UIInterfaceOrientation inOrientation);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISplitViewControllerHidePredicate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISplitViewControllerHidePredicate

Added:

```
[Serializable]
 public delegate bool UISplitViewControllerHidePredicate (
                UISplitViewController svc, UIViewController viewController, UIInterfaceOrientation inOrientation);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIStepper" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIStepper

Added:

```
public UIStepper (System.Drawing.RectangleF frame);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISwitch" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISwitch

Added:

```
set;
                        set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableView

Added:

```
public UITableView (System.Drawing.RectangleF frame);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewCell" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewCell

Added:

```
public UITableViewCell (System.Drawing.RectangleF frame);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewAutoresizing" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewAutoresizing

Removed:

```
FlexibleBottomMargin
```

Added:

```
FlexibleBottomMargin,
        FlexibleMargins,
        FlexibleDimensions,
        All
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewController

Removed:

```
set;
```

 <a name="Namespace:_MonoTouch.iAd" class="injected"></a>


# Namespace: MonoTouch.iAd

 <a name="Type_Changed:_MonoTouch.iAd.ADBannerView" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADBannerView

Added:

```
public ADBannerView (System.Drawing.RectangleF frame);
```
