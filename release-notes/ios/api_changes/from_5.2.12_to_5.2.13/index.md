---
id: E4681BB7-03C9-CABB-CAA8-7146ACD72AFC
title: "from 5.2.12 to 5.2.13"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.2.12";
```

Added:

```
public const string Version = "5.2.13";
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
        public virtual void GenerateCGImagesAsynchronously (MonoTouch.Foundation.NSValue[] cmTimesRequestedTimes, AVAssetImageGeneratorCompletionHandler handler);
                set;
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Added:

```
public virtual bool IsFocusModeSupported (AVCaptureFocusMode focusMode);
        public virtual bool IsWhiteBalanceModeSupported (AVCaptureWhiteBalanceMode whiteBalanceMode);
```

 <a name="Namespace:_MonoTouch.CoreMotion" class="injected"></a>


# Namespace: MonoTouch.CoreMotion

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMMotionManager" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMMotionManager

Removed:

```
public virtual void StartDeviceMotionUpdates (CMAttitudeReferenceFrame referenceFrame, MonoTouch.Foundation.NSOperationQueue queue, CMMagnetometerHandler handler);
```

Added:

```
public virtual void StartDeviceMotionUpdates (CMAttitudeReferenceFrame referenceFrame, MonoTouch.Foundation.NSOperationQueue queue, CMDeviceMotionHandler handler);
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSBundle" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSBundle

Removed:

```
public static bool LoadNib (string nibName, NSObject owner);
        public virtual string PathForImageResource (string resource);
        public virtual string PathForSoundResource (string resource);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileCoordinatorWritingOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileCoordinatorWritingOptions

Added:

```
ForReplacing
```

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

 <a name="Type_Changed:_MonoTouch.UIKit.UISlider" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISlider

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
