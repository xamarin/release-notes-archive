---
id: 7FA0F3C0-9633-172C-2994-95484F80FC2F
title: "From 3.2.3 to 3.2.4"
---

&nbsp;

 <a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Removed:

```
public const string Version = "3.2.3";
```

Added:

```
public const string Version = "3.2.4";
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsError" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
[Serializable]
 public enum ALAssetsError {
        UnknownError,
        WriteFailedError,
        WriteBusyError,
        WriteInvalidDataError,
        WriteIncompatibleDataError,
        WriteDataEncodingError,
        WriteDiskSpaceError,
        DataUnavailableError,
        AccessUserDeniedError,
        AccessGloballyDeniedError
 }
```

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsLibrary" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public class ALAssetsLibrary : MonoTouch.Foundation.NSObject {
        
        public ALAssetsLibrary ();
        public ALAssetsLibrary (MonoTouch.Foundation.NSCoder coder);
        public ALAssetsLibrary (MonoTouch.Foundation.NSObjectFlag t);
        public ALAssetsLibrary (IntPtr handle);
        
        public virtual void AssetForUrl (MonoTouch.Foundation.NSUrl assetURL, ALAssetsLibraryAssetForURLResultDelegate resultBlock, ALAssetsLibraryAccessFailureDelegate failureBlock);
        public virtual void Enumerate (ALAssetsGroupType types, ALAssetsLibraryGroupsEnumerationResultsDelegate enumerationBlock, ALAssetsLibraryAccessFailureDelegate failureBlock);
        public virtual bool VideoAtPathIsIsCompatibleWithSavedPhotosAlbum (MonoTouch.Foundation.NSUrl videoPathURL);
        public virtual void WriteImageToSavedPhotosAlbum (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public virtual void WriteImageToSavedPhotosAlbum (MonoTouch.UIKit.UIImage imageData, ALAssetOrientation orientation, ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public virtual void WriteImageToSavedPhotosAlbum (MonoTouch.UIKit.UIImage imageData, MonoTouch.Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public virtual void WriteVideoToSavedPhotosAlbum (MonoTouch.Foundation.NSUrl videoPathURL, ALAssetsLibraryWriteCompletionDelegate completionBlock);
        
        public override IntPtr ClassHandle {
                get;
        }
 }
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibraryAccessFailureDelegate 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
[Serializable]
 public delegate void ALAssetsLibraryAccessFailureDelegate (MonoTouch.Foundation.NSError error);
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibraryAssetForURLResultDelegate 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
[Serializable]
 public delegate void ALAssetsLibraryAssetForURLResultDelegate (ALAsset asset);
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibraryGroupsEnumerationResultsDelegate 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
[Serializable]
 public delegate void ALAssetsLibraryGroupsEnumerationResultsDelegate (ALAssetsGroup group, ref bool stop);
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibraryWriteCompletionDelegate 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
[Serializable]
 public delegate void ALAssetsLibraryWriteCompletionDelegate (MonoTouch.Foundation.NSUrl assetURL, MonoTouch.Foundation.NSError error);
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGColor" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGColor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGColor (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGColorSpace" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGColorSpace

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGColorSpace (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGContext" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGContext

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGContext (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGDataProvider" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGDataProvider

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGDataProvider (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGImage" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGImage

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGImage (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPath" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPath

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGPath (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPattern" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPattern

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGPattern (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFArray" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFArray

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGPDFArray (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFDictionary" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFDictionary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGPDFDictionary (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFDocument" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFDocument

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGPDFDocument (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGShading" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGShading

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public CGShading (IntPtr handle);
```

 <a name="Namespace:_MonoTouch.CoreTelephony" class="injected"></a>


# Namespace: MonoTouch.CoreTelephony

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="New_Type:_MonoTouch.CoreTelephony.CTTelephonyNetworkInfo" class="injected"></a>


## New Type: MonoTouch.CoreTelephony.CTTelephonyNetworkInfo

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

```
public class CTTelephonyNetworkInfo : MonoTouch.Foundation.NSObject {
        
        public CTTelephonyNetworkInfo ();
        public CTTelephonyNetworkInfo (MonoTouch.Foundation.NSCoder coder);
        public CTTelephonyNetworkInfo (MonoTouch.Foundation.NSObjectFlag t);
        public CTTelephonyNetworkInfo (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual CTCarrier SubscriberCellularProvider {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableDictionary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Removed:

```
public static NSDictionary FromObjectsAndKeys (object [] objects, object [] keys);
        public static NSDictionary FromObjectsAndKeys (object [] objects, object [] keys, int count);
```

Added:

```
public static NSMutableDictionary FromObjectsAndKeys (object [] objects, object [] keys);
        public static NSMutableDictionary FromObjectsAndKeys (object [] objects, object [] keys, int count);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlRequest" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public override string ToString ();
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchmakerViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchmakerViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Removed:

```
public GKMatchmakerViewControllerDelegate Delegate {
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
```

Added:

```
public GKMatchmakerViewControllerDelegate MatchmakerDelegate {
        public virtual MonoTouch.Foundation.NSObject WeakMatchmakerDelegate {
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItemArtwork" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItemArtwork

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Removed:

```
public virtual MonoTouch.UIKit.UIImage ImageWithSize (System.Drawing.PointF size);
```

Added:

```
public virtual MonoTouch.UIKit.UIImage ImageWithSize (System.Drawing.RectangleF size);
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public static void void_objc_msgSend_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2, IntPtr arg3);
        public static void void_objc_msgSendSuper_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2, IntPtr arg3);
```

 <a name="Namespace:_MonoTouch.StoreKit" class="injected"></a>


# Namespace: MonoTouch.StoreKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.StoreKit.SKProductsRequest" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKProductsRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public event EventHandler<SKRequestErrorEventArgs> RequestFailed;
        public event EventHandler RequestFinished;
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public event EventHandler Canceled;
        public event EventHandler<UINavigationControllerEventArgs> DidShowViewController;
        public event EventHandler<UIImagePickerImagePickedEventArgs> FinishedPickingImage;
        public event EventHandler<UIImagePickerMediaPickedEventArgs> FinishedPickingMedia;
        public event EventHandler<UINavigationControllerEventArgs> WillShowViewController;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerImagePickedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerImagePickedEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public class UIImagePickerImagePickedEventArgs : EventArgs {
        
        public UIImagePickerImagePickedEventArgs (UIImage image, MonoTouch.Foundation.NSDictionary editingInfo);
        
        public MonoTouch.Foundation.NSDictionary EditingInfo {
                get;
                set;
        }
        public UIImage Image {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerMediaPickedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerMediaPickedEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public class UIImagePickerMediaPickedEventArgs : EventArgs {
        
        public UIImagePickerMediaPickedEventArgs (MonoTouch.Foundation.NSDictionary info);
        
        public MonoTouch.Foundation.NSDictionary Info {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UINavigationControllerEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UINavigationControllerEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public class UINavigationControllerEventArgs : EventArgs {
        
        public UINavigationControllerEventArgs (UIViewController viewController, bool animated);
        
        public bool Animated {
                get;
                set;
        }
        public UIViewController ViewController {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public UIScrollViewCondition ShouldScrollToTop {
                get;
                set;
        }
        public UIScrollViewGetZoomView ViewForZoomingInScrollView {
                get;
                set;
        }
        public event EventHandler DecelerationEnded;
        public event EventHandler DecelerationStarted;
        public event EventHandler DidZoom;
        public event EventHandler<DraggingEventArgs> DraggingEnded;
        public event EventHandler DraggingStarted;
        public event EventHandler ScrollAnimationEnded;
        public event EventHandler Scrolled;
        public event EventHandler ScrolledToTop;
        public event EventHandler<ZoomingEndedEventArgs> ZoomingEnded;
        public event EventHandler<UIScrollViewZoomingEventArgs> ZoomingStarted;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIVideoEditorController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIVideoEditorController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public event EventHandler<UINavigationControllerEventArgs> DidShowViewController;
        public event EventHandler<UINavigationControllerEventArgs> WillShowViewController;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWindow" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWindow

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.2.3_to_3.2.4/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2.4#)

Added:

```
public virtual UIViewController RootViewController {
                get;
        }
```
