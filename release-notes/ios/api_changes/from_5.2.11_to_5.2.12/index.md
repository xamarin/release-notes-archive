---
id: 7BBCE5E1-B4F7-FA3C-A186-8E888A2E4575
title: "From 5.2.11 to 5.2.12"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.2.11";
```

Added:

```
public const string Version = "5.2.12";
        public const string MobileCoreServicesLibrary = "/System/Library/Frameworks/MobileCoreServices.framework/MobileCoreServices";
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

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CALayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CALayer

Added:

```
public System.Drawing.RectangleF ConvertRectfromLayer (System.Drawing.RectangleF rect, CALayer layer);
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


# Namespace: MonoTouch.CoreFoundation

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFProxySettings" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFProxySettings

Added:

```
public MonoTouch.Foundation.NSDictionary Dictionary {
                get;
        }
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

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


# Namespace: MonoTouch.CoreImage

Many default constructors were exposed that did not work. Users must use
either factory methods, or constructors with parameters. It is not a breaking
change, as previous uses of these APIs would have crashed the application upon
use.

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

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

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

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlConnection" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlConnection

Added:

```
public virtual void Schedule (NSRunLoop aRunLoop, NSString forMode);
        public virtual void Unschedule (NSRunLoop aRunLoop, NSString forMode);
```

 <a name="Namespace:_MonoTouch.MobileCoreServices" class="injected"></a>


# Namespace: MonoTouch.MobileCoreServices

 <a name="New_Type:_MonoTouch.MobileCoreServices.UTType" class="injected"></a>


## New Type: MonoTouch.MobileCoreServices.UTType

```
public class UTType {
        
        public UTType ();
        
        public static MonoTouch.Foundation.NSString ExportedTypeDeclarationsKey;
        public static MonoTouch.Foundation.NSString ImportedTypeDeclarationsKey;
        public static MonoTouch.Foundation.NSString IdentifierKey;
        public static MonoTouch.Foundation.NSString TagSpecificationKey;
        public static MonoTouch.Foundation.NSString ConformsToKey;
        public static MonoTouch.Foundation.NSString DescriptionKey;
        public static MonoTouch.Foundation.NSString IconFileKey;
        public static MonoTouch.Foundation.NSString ReferenceURLKey;
        public static MonoTouch.Foundation.NSString VersionKey;
        public static MonoTouch.Foundation.NSString TagClassFilenameExtension;
        public static MonoTouch.Foundation.NSString TagClassMIMEType;
        public static MonoTouch.Foundation.NSString Item;
        public static MonoTouch.Foundation.NSString Content;
        public static MonoTouch.Foundation.NSString CompositeContent;
        public static MonoTouch.Foundation.NSString Application;
        public static MonoTouch.Foundation.NSString Message;
        public static MonoTouch.Foundation.NSString Contact;
        public static MonoTouch.Foundation.NSString Archive;
        public static MonoTouch.Foundation.NSString DiskImage;
        public static MonoTouch.Foundation.NSString Data;
        public static MonoTouch.Foundation.NSString Directory;
        public static MonoTouch.Foundation.NSString Resolvable;
        public static MonoTouch.Foundation.NSString SymLink;
        public static MonoTouch.Foundation.NSString MountPoint;
        public static MonoTouch.Foundation.NSString AliasFile;
        public static MonoTouch.Foundation.NSString AliasRecord;
        public static MonoTouch.Foundation.NSString URL;
        public static MonoTouch.Foundation.NSString FileURL;
        public static MonoTouch.Foundation.NSString Text;
        public static MonoTouch.Foundation.NSString PlainText;
        public static MonoTouch.Foundation.NSString UTF8PlainText;
        public static MonoTouch.Foundation.NSString UTF16ExternalPlainText;
        public static MonoTouch.Foundation.NSString UTF16PlainText;
        public static MonoTouch.Foundation.NSString RTF;
        public static MonoTouch.Foundation.NSString HTML;
        public static MonoTouch.Foundation.NSString XML;
        public static MonoTouch.Foundation.NSString SourceCode;
        public static MonoTouch.Foundation.NSString CSource;
        public static MonoTouch.Foundation.NSString ObjectiveCSource;
        public static MonoTouch.Foundation.NSString CPlusPlusSource;
        public static MonoTouch.Foundation.NSString ObjectiveCPlusPlusSource;
        public static MonoTouch.Foundation.NSString CHeader;
        public static MonoTouch.Foundation.NSString CPlusPlusHeader;
        public static MonoTouch.Foundation.NSString JavaSource;
        public static MonoTouch.Foundation.NSString PDF;
        public static MonoTouch.Foundation.NSString RTFD;
        public static MonoTouch.Foundation.NSString FlatRTFD;
        public static MonoTouch.Foundation.NSString TXNTextAndMultimediaData;
        public static MonoTouch.Foundation.NSString WebArchive;
        public static MonoTouch.Foundation.NSString Image;
        public static MonoTouch.Foundation.NSString JPEG;
        public static MonoTouch.Foundation.NSString JPEG2000;
        public static MonoTouch.Foundation.NSString TIFF;
        public static MonoTouch.Foundation.NSString GIF;
        public static MonoTouch.Foundation.NSString PNG;
        public static MonoTouch.Foundation.NSString QuickTimeImage;
        public static MonoTouch.Foundation.NSString AppleICNS;
        public static MonoTouch.Foundation.NSString BMP;
        public static MonoTouch.Foundation.NSString ICO;
        public static MonoTouch.Foundation.NSString AudiovisualContent;
        public static MonoTouch.Foundation.NSString Movie;
        public static MonoTouch.Foundation.NSString Video;
        public static MonoTouch.Foundation.NSString Audio;
        public static MonoTouch.Foundation.NSString QuickTimeMovie;
        public static MonoTouch.Foundation.NSString MPEG;
        public static MonoTouch.Foundation.NSString MPEG4;
        public static MonoTouch.Foundation.NSString MP3;
        public static MonoTouch.Foundation.NSString MPEG4Audio;
        public static MonoTouch.Foundation.NSString AppleProtectedMPEG4Audio;
        public static MonoTouch.Foundation.NSString Folder;
        public static MonoTouch.Foundation.NSString Volume;
        public static MonoTouch.Foundation.NSString Package;
        public static MonoTouch.Foundation.NSString Bundle;
        public static MonoTouch.Foundation.NSString Framework;
        public static MonoTouch.Foundation.NSString ApplicationBundle;
        public static MonoTouch.Foundation.NSString ApplicationFile;
        public static MonoTouch.Foundation.NSString VCard;
        public static MonoTouch.Foundation.NSString InkText;
}
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Removed:

```
public virtual void OpenUrl (UIApplication application, MonoTouch.Foundation.NSUrl url, string sourceApplication, MonoTouch.Foundation.NSObject annotation);
```

Added:

```
public virtual bool OpenUrl (UIApplication application, MonoTouch.Foundation.NSUrl url, string sourceApplication, MonoTouch.Foundation.NSObject annotation);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISlider" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISlider

Added:

```
public virtual UIImage MaxTrackImage (UIControlState forState);
                public virtual UIImage MinTrackImage (UIControlState forState);
                public virtual void SetMaxTrackImage (UIImage image, UIControlState forState);
                public virtual void SetMinTrackImage (UIImage image, UIControlState forState);
                public virtual void SetThumbImage (UIImage image, UIControlState forState);
                public virtual UIImage ThumbImage (UIControlState forState);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

Added:

```
public System.Drawing.SizeF DrawString (string str, System.Drawing.PointF point, float width, UIFont font, float minFontSize, ref float actualFontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
        public System.Drawing.SizeF StringSize (string str, UIFont font, float minFontSize, ref float actualFontSize, float forWidth, UILineBreakMode lineBreakMode);
```
