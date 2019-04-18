---
id: AFAA199F-2F51-DF99-2E79-C500F7FD82F7
title: "From 5.3.3 to 5.3.4"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.3.3";
```

Added:

```
public const string Version = "5.3.4";
        public const string MobileCoreServicesLibrary = "/System/Library/Frameworks/MobileCoreServices.framework/MobileCoreServices";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetImageGenerator" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetImageGenerator

Removed:

```
public virtual MonoTouch.CoreGraphics.CGImage CopyCGImageAtTime (MonoTouch.CoreMedia.CMTime requestedTime, MonoTouch.CoreMedia.CMTime actualTime, MonoTouch.Foundation.NSError outError);
```

Added:

```
public virtual MonoTouch.CoreGraphics.CGImage CopyCGImageAtTime (MonoTouch.CoreMedia.CMTime requestedTime, out MonoTouch.CoreMedia.CMTime actualTime, out MonoTouch.Foundation.NSError outError);
                set;
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFileProperty" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFileProperty

Added:

```
ReadyToProducePackets,
        AverageBytesPerPacket
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

 <a name="New_Type:_MonoTouch.CoreFoundation.CFStreamClientContext" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFStreamClientContext

```
public struct CFStreamClientContext {
        
        public void Release ();
        public void Retain ();
        public override string ToString ();
        
        public int Version;
        public IntPtr Info;
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFStreamEventType" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFStreamEventType

```
[Serializable]
[Flags]
public enum CFStreamEventType {
        None,
        OpenCompleted,
        HasBytesAvailable,
        CanAcceptBytes,
        ErrorOccurred,
        EndEncountered
}
```

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


# Namespace: MonoTouch.CoreImage

 <a name="Type_Changed:_MonoTouch.CoreImage.CIImage" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIImage

Added:

```
public static CIImage FromCGImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
        public static implicit operator CIImage (MonoTouch.CoreGraphics.CGImage image);
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSAttributedStringEnumeration" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSAttributedStringEnumeration

Added:

```
[Serializable]
 [Flags]
 public enum NSAttributedStringEnumeration {
        None,
        Reverse,
        LongestEffectiveRangeNotRequired
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSBundle" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSBundle

Removed as they only exist in MacOS X and not iOS:

```
public static bool LoadNib (string nibName, NSObject owner);
        public virtual string PathForImageResource (string resource);
        public virtual string PathForSoundResource (string resource);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDate

Removed as it is now part of the base NSObject class:

```
public virtual string Description {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDictionary

Removed as it is now part of the NSObject class:

```
public virtual string Description {
```

Added:

```
public virtual string DescriptionInStringsFileFormat {
        public virtual NSObject this [NSString key] {
                get;
                set;
        }
        public virtual NSObject this [string key] {
                set;
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSInputStream" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSInputStream

Added:

```
protected override void Dispose (bool disposing);
        protected virtual bool GetBuffer (out IntPtr buffer, out uint len);
        public void Notify (MonoTouch.CoreFoundation.CFStreamEventType eventType);
        public virtual int Read (IntPtr buffer, uint len);
        public virtual void ScheduleInCFRunLoop (MonoTouch.CoreFoundation.CFRunLoop runloop, NSString mode);
        protected virtual bool SetCFClientFlags (MonoTouch.CoreFoundation.CFStreamEventType inFlags, IntPtr inCallback, IntPtr inContextPtr);
        public virtual void UnscheduleInCFRunLoop (MonoTouch.CoreFoundation.CFRunLoop runloop, NSString mode);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableDictionary

Added:

```
public override NSObject this [string key] {
                get;
                set;
        }
        public override NSObject this [NSString key] {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSObject

The NSObject class now overrides ToString() and by default returns the value
of Description that should provide a description of the element from
Objective-C.

Added:

```
public override string ToString ();
        public virtual string DebugDescription {
                get;
        }
        public virtual string Description {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRange" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRange

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSSet" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSSet

Removed as it is now part of the NSObject class:

```
public virtual string Description {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimeZone" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimeZone

Removed as it is now part of the NSObject class:

```
public virtual string Description {
                get;
        }
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

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIAppearance" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAppearance

Removed:

```
public override IntPtr ClassHandle {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIButton" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIButton

Added:

```
public virtual UIImage BackgroundImageForState (UIControlState state);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UILabelAppearance" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UILabelAppearance

Added:

```
public virtual UIFont Font {
                        get;
                        set;
                }
                public virtual UIColor HighlightedTextColor {
                        get;
                        set;
                }
                public virtual UIColor ShadowColor {
                        get;
                        set;
                }
                public virtual System.Drawing.SizeF ShadowOffset {
                        get;
                        set;
                }
                public virtual UIColor TextColor {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISliderAppearance" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISliderAppearance

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
