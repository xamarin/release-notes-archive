---
id: 81AB47C0-481A-1D6D-C5EE-E6B56AC0440D
title: "From 4.0.1 to 4.0.2"
---

&nbsp;

 <a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

Removed:

```
public const string Version = "4.0.1";
```

Added:

```
public const string Version = "4.0.2";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriterInputPixelBufferAdaptor 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

Added:

```
public virtual bool AppendPixelBufferWithPresentationTime (MonoTouch.CoreVideo.CVPixelBuffer pixelBuffer, MonoTouch.CoreMedia.CMTime presentationTime);
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSData" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSData

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

Added:

```
public static NSData FromUrl (NSUrl url, NSDataReadingOptions mask, out NSError error);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDataReadingOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDataReadingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

Removed:

```
Could not find MonoTouch.Foundation.NSDataReadingOptions
```

Added:

```
[Serializable]
 [Flags]
 public enum NSDataReadingOptions : uint {
    Mapped,
    Uncached
 }
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.1_to_4.0.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.2#)

Added:

```
public static bool bool_objc_msgSend_IntPtr_CMTime (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreMedia.CMTime arg2);
    public static bool bool_objc_msgSendSuper_IntPtr_CMTime (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreMedia.CMTime arg2);
    public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3);
    public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3);
```
