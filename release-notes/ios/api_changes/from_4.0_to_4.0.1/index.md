---
id: 82FEB984-0F45-5C5A-4F84-D85578564CF9
title: "From 4.0 to 4.0.1"
---

&nbsp;

 <a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Removed:

```
public const string Version = "4.0.0";
```

Added:

```
public const string Version = "4.0.1";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioSettings" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioSettings

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Removed:

```
public static readonly MonoTouch.Foundation.NSString AVFormatKey;
```

Added:

```
public static readonly MonoTouch.Foundation.NSString AVFormatIDKey;
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Removed:

```
public virtual bool LockForConfiguration (IntPtr ptrToHandleToError);
```

Added:

```
public virtual bool LockForConfiguration (out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableCompositionTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableCompositionTrack

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public virtual bool InsertTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange, AVAssetTrack ofTrack, MonoTouch.CoreMedia.CMTime atTime, out MonoTouch.Foundation.NSError error);
        public virtual bool ValidateTrackSegments (AVCompositionTrackSegment[] trackSegments, out MonoTouch.Foundation.NSError error);
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAEAGLLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAEAGLLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static CALayer Create ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAGradientLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAGradientLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static CALayer Create ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAReplicatorLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAReplicatorLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static CALayer Create ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAScrollLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAScrollLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static CALayer Create ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAShapeLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAShapeLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static CALayer Create ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CATextLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CATextLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static CALayer Create ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CATiledLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CATiledLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static CALayer Create ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CATransformLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CATransformLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static CALayer Create ();
```

 <a name="Namespace:_MonoTouch.CoreMedia" class="injected"></a>


# Namespace: MonoTouch.CoreMedia

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

 <a name="New_Type:_MonoTouch.CoreMedia.CMBlockBuffer" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMBlockBuffer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

```
public class CMBlockBuffer : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public int CopyDataBytes (uint offsetToData, uint dataLength, IntPtr destination);
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public uint DataLength {
                get;
        }
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMFormatDescription" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMFormatDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

```
public class CMFormatDescription : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static int GetTypeID ();
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public MonoTouch.Foundation.NSDictionary GetExtensions ();
        
        public IntPtr Handle {
                get;
        }
        public uint MediaSubType {
                get;
        }
        public CMMediaType MediaType {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMMediaType" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMMediaType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

```
[Serializable]
public enum CMMediaType : uint {
        Video,
        Audio,
        Muxed,
        Text,
        ClosedCaption,
        Subtitle,
        TimeCode,
        TimedMetadata
}
```

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMSampleBuffer" class="injected"></a>


## Type Changed: MonoTouch.CoreMedia.CMSampleBuffer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static int GetTypeID ();
        public CMBlockBuffer GetDataBuffer ();
        public CMFormatDescription GetFormatDescription ();
        public MonoTouch.Foundation.NSMutableDictionary[] GetSampleAttachments (bool createIfNecessary);
        public uint GetSampleSize (int sampleIndex);
        public int Invalidate ();
        public int MakeDataReady ();
        public int SetDataBuffer (CMBlockBuffer dataBuffer);
        public int SetDataReady ();
        public int SetOutputPresentationTimeStamp (CMTime outputPresentationTimeStamp);
        public int TrackDataReadiness (CMSampleBuffer bufferToTrack);
        public bool DataIsReady {
                get;
        }
        public CMTime DecodeTimeStamp {
                get;
        }
        public CMTime Duration {
                get;
        }
        public bool IsValid {
                get;
        }
        public int NumSamples {
                get;
        }
        public CMTime OutputDecodeTimeStamp {
                get;
        }
        public CMTime OutputDuration {
                get;
        }
        public CMTime OutputPresentationTimeStamp {
                get;
        }
        public CMTime PresentationTimeStamp {
                get;
        }
        public uint TotalSampleSize {
                get;
        }
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSAttributedString

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static NSString BackgroundColorAttributeName {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSLocale" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSLocale

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Removed:

```
public static string ISOCountryCodes {
```

Added:

```
public static string [] ISOCountryCodes {
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumberFormatter" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumberFormatter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public class NSNumberFormatter : NSFormatter {
        
        public NSNumberFormatter ();
        public NSNumberFormatter (NSCoder coder);
        public NSNumberFormatter (NSObjectFlag t);
        public NSNumberFormatter (IntPtr handle);
        
        public virtual string LocalizedStringFromNumbernumberStyle (NSNumber num, NSNumberFormatterStyle nstyle);
        public virtual NSNumber NumberFromString (string text);
        public virtual string StringFromNumber (NSNumber number);
        
        public static NSNumberFormatterBehavior DefaultFormatterBehavior {
                get;
                set;
        }
        public virtual bool AllowsFloats {
                get;
                set;
        }
        public virtual bool AlwaysShowsDecimalSeparator {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string CurrencyCode {
                get;
                set;
        }
        public virtual string CurrencyDecimalSeparator {
                get;
                set;
        }
        public virtual string CurrencyGroupingSeparator {
                get;
                set;
        }
        public virtual string CurrencySymbol {
                get;
                set;
        }
        public virtual string DecimalSeparator {
                get;
                set;
        }
        public virtual string ExponentSymbol {
                get;
                set;
        }
        public virtual NSNumberFormatterBehavior FormatterBehavior {
                get;
                set;
        }
        public virtual uint FormatWidth {
                get;
                set;
        }
        public virtual bool GeneratesDecimalNumbers {
                get;
                set;
        }
        public virtual string GroupingSeparator {
                get;
                set;
        }
        public virtual uint GroupingSize {
                get;
                set;
        }
        public virtual string InternationalCurrencySymbol {
                get;
                set;
        }
        public virtual bool Lenient {
                get;
                set;
        }
        public virtual NSLocale Locale {
                get;
                set;
        }
        public virtual NSNumber Maximum {
                get;
                set;
        }
        public virtual int MaximumFractionDigits {
                get;
                set;
        }
        public virtual int MaximumIntegerDigits {
                get;
                set;
        }
        public virtual uint MaximumSignificantDigits {
                get;
                set;
        }
        public virtual NSNumber Minimum {
                get;
                set;
        }
        public virtual int MinimumFractionDigits {
                get;
                set;
        }
        public virtual int MinimumIntegerDigits {
                get;
                set;
        }
        public virtual uint MinimumSignificantDigits {
                get;
                set;
        }
        public virtual string MinusSign {
                get;
                set;
        }
        public virtual NSNumber Multiplier {
                get;
                set;
        }
        public virtual string NegativeFormat {
                get;
                set;
        }
        public virtual string NegativeInfinitySymbol {
                get;
                set;
        }
        public virtual string NegativePrefix {
                get;
                set;
        }
        public virtual string NegativeSuffix {
                get;
                set;
        }
        public virtual string NilSymbol {
                get;
                set;
        }
        public virtual string NotANumberSymbol {
                get;
                set;
        }
        public virtual NSNumberFormatterStyle NumberStyle {
                get;
                set;
        }
        public virtual string PaddingCharacter {
                get;
                set;
        }
        public virtual NSNumberFormatterPadPosition PaddingPosition {
                get;
                set;
        }
        public virtual bool PartialStringValidationEnabled {
                get;
                set;
        }
        public virtual string PercentSymbol {
                get;
                set;
        }
        public virtual string PerMillSymbol {
                get;
                set;
        }
        public virtual string PlusSign {
                get;
                set;
        }
        public virtual string PositiveFormat {
                get;
                set;
        }
        public virtual string PositiveInfinitySymbol {
                get;
                set;
        }
        public virtual string PositivePrefix {
                get;
                set;
        }
        public virtual string PositiveSuffix {
                get;
                set;
        }
        public virtual NSNumber RoundingIncrement {
                get;
                set;
        }
        public virtual NSNumberFormatterRoundingMode RoundingMode {
                get;
                set;
        }
        public virtual uint SecondaryGroupingSize {
                get;
                set;
        }
        public virtual NSDictionary TextAttributesForNegativeInfinity {
                get;
                set;
        }
        public virtual NSDictionary TextAttributesForNegativeValues {
                get;
                set;
        }
        public virtual NSDictionary TextAttributesForNil {
                get;
                set;
        }
        public virtual NSDictionary TextAttributesForNotANumber {
                get;
                set;
        }
        public virtual NSDictionary TextAttributesForPositiveInfinity {
                get;
                set;
        }
        public virtual NSDictionary TextAttributesForPositiveValues {
                get;
                set;
        }
        public virtual NSDictionary TextAttributesForZero {
                get;
                set;
        }
        public virtual bool UsesGroupingSeparator {
                get;
                set;
        }
        public virtual bool UsesSignificantDigits {
                get;
                set;
        }
        public virtual string ZeroSymbol {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumberFormatterBehavior" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumberFormatterBehavior

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
[Serializable]
 public enum NSNumberFormatterBehavior {
        Default,
        Version_10_0,
        Version_10_4
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumberFormatterPadPosition" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumberFormatterPadPosition

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
[Serializable]
 public enum NSNumberFormatterPadPosition {
        BeforePrefix,
        AfterPrefix,
        BeforeSuffix,
        AfterSuffix
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumberFormatterRoundingMode" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumberFormatterRoundingMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
[Serializable]
 public enum NSNumberFormatterRoundingMode {
        Ceiling,
        Floor,
        Down,
        Up,
        HalfEven,
        HalfDown,
        HalfUp
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumberFormatterStyle" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumberFormatterStyle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
[Serializable]
 public enum NSNumberFormatterStyle {
        None,
        Decimal,
        Currency,
        Percent,
        Scientific,
        SpellOut
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRunLoop" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRunLoop

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public virtual bool RunUntil (NSString runLoopMode, NSDate limitdate);
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
set;
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public static bool bool_objc_msgSend_CMTimeRange_IntPtr_CMTime_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1, IntPtr arg2, MonoTouch.CoreMedia.CMTime arg3, IntPtr arg4);
        public static bool bool_objc_msgSendSuper_CMTimeRange_IntPtr_CMTime_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1, IntPtr arg2, MonoTouch.CoreMedia.CMTime arg3, IntPtr arg4);
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

 <a name="Type_Changed:_MonoTouch.UIKit.UIFont" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIFont

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0_to_4.0.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.1#)

Added:

```
public virtual float LineHeight {
                get;
        }
```
