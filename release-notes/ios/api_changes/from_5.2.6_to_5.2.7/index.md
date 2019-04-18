---
id: 62B31428-2CE2-B454-D5F4-CBA9CB82B344
title: "From 5.2.6 to 5.2.7"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.2.6";
```

Added:

```
public const string Version = "5.2.7";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVError" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVError

Added:

```
InvalidOutputURLPathExtension
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetRepresentation" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetRepresentation

Added:

```
public virtual System.Drawing.SizeF Dimensions {
                get;
        }
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFormatType" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFormatType

Added:

```
MPEG4AAC_ELD_V2
```

 <a name="Namespace:_MonoTouch.CoreVideo" class="injected"></a>


# Namespace: MonoTouch.CoreVideo

 <a name="Type_Changed:_MonoTouch.CoreVideo.CVPixelFormatType" class="injected"></a>


## Type Changed: MonoTouch.CoreVideo.CVPixelFormatType

Added:

```
OneComponent8,
        TwoComponent8
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrl" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrl

Added:

```
public static NSString IsExcludedFromBackupKey {
                get;
        }
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Dlfcn" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Dlfcn

Added:

```
public static IntPtr dlsym (IntPtr handle, string symbol);
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="New_Type:_MonoTouch.UIKit.UIDictationPhrase" class="injected"></a>


## New Type: MonoTouch.UIKit.UIDictationPhrase

```
public class UIDictationPhrase : MonoTouch.Foundation.NSObject {
        
        public UIDictationPhrase ();
        public UIDictationPhrase (MonoTouch.Foundation.NSCoder coder);
        public UIDictationPhrase (MonoTouch.Foundation.NSObjectFlag t);
        public UIDictationPhrase (IntPtr handle);
        
        public virtual string [] AlternativeInterpretations {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string Text {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerMediaPickedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerMediaPickedEventArgs

Added:

```
public System.Nullable<System.Drawing.RectangleF> CropRect {
                get;
        }
        public UIImage EditedImage {
                get;
        }
        public string MediaType {
                get;
        }
        public MonoTouch.Foundation.NSUrl MediaUrl {
                get;
        }
        public UIImage OriginalImage {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISplitViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISplitViewController

Added:

```
public virtual bool PresentsWithGesture {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

Added back:

```
public static void Animate (double duration, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Animate (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Transition (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Transition (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction completion);
```
