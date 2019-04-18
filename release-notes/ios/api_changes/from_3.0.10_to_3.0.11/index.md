---
id: 3D53F68B-8BE8-82BD-E3A0-EE5A689E5291
title: "From 3.0.10 to 3.0.11"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "3.0.10";
        public const string iAdLibrary = 
            "/System/Library/Frameworks/AdLib.framework/AdLib";
```

Added:

```
public const string Version = "3.0.11";
        public const string iAdLibrary = 
            "/System/Library/Frameworks/iAd.framework/iAd";
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CALayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CALayer

Added:

```
public virtual float ContentsScale {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGColor" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGColor

Removed:

```
public CGColor (CGColorSpace cs, float [] components);
        public CGColor (CGColorSpace space, 
            CGPattern pattern, float [] components);
```

Added:

```
public CGColor (CGColorSpace colorspace, float [] components);
        public CGColor (CGColorSpace colorspace, 
            CGPattern pattern, float [] components);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGDataProvider" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGDataProvider

Added:

```
public MonoTouch.Foundation.NSData CopyData ();
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGImage" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGImage

Added:

```
public CGDataProvider DataProvider {
                get;
        }
```

 <a name="Namespace:_MonoTouch.CoreMotion" class="injected"></a>


# Namespace: MonoTouch.CoreMotion

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMAcceleration" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMAcceleration

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMAccelerometerData" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMAccelerometerData

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMQuaternion" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMQuaternion

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.10_to_3.0.11/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.11#)

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMRotationRate" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMRotationRate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.10_to_3.0.11/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.11#)

Added:

```
public override string ToString ();
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


# Namespace: MonoTouch.EventKit

 <a name="Type_Changed:_MonoTouch.EventKit.EKEventStore" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEventStore

Removed:

```
public virtual EKEvent[] EventsMatchin (MonoTouch.Foundation.NSPredicate predicate);
```

Added:

```
public virtual EKEvent[] EventsMatching (MonoTouch.Foundation.NSPredicate predicate);
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSDate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDate

Added:

```
public static NSDate FromTimeIntervalSinceNow (double secs);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimeZone" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimeZone

Removed:

```
public static NSTimeZone FromName (string timeZoneName);
                set;
```

Added:

```
public static NSTimeZone FromName (string tzName);
        public virtual string Description {
                get;
        }
        public virtual int GetSecondsFromGMT {
                get;
        }
```
