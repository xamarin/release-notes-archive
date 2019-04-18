---
id: F91D9EED-7698-BA22-99A5-9B651C3BA3D9
title: "from 6.0.0 to 6.0.1"
---

Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "6.0.0";
```

Added:

```
public const string Version = "6.0.1";
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAMediaTimingFunction" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAMediaTimingFunction

Removed:

```
public CAMediaTimingFunction ();
        public static CAMediaTimingFunction FromName (string name);
```

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CAMediaTimingFunction ();
        public static CAMediaTimingFunction FromName (MonoTouch.Foundation.NSString name);
        [Obsolete("Use FromName(NSString) with one of the CAMediaTimingFunction fields")]
        public static CAMediaTimingFunction FromName (string name);
        public System.Drawing.PointF GetControlPoint (int index);
        public static MonoTouch.Foundation.NSString Default {
                get;
        }
```

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


# Namespace: MonoTouch.CoreImage

 <a name="Type_Changed:_MonoTouch.CoreImage.CIAdditionCompositing" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIAdditionCompositing

Removed:

```
public class CIAdditionCompositing : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIAdditionCompositing : CICompositingFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIAffineClamp" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIAffineClamp

```
public class CIAffineClamp : CIAffineFilter {
        
        public CIAffineClamp ();
        public CIAffineClamp (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIAffineFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIAffineFilter

```
public abstract class CIAffineFilter : CIFilter {
        
        protected CIAffineFilter (string name);
        protected CIAffineFilter (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public MonoTouch.CoreGraphics.CGAffineTransform Transform {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIAffineTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIAffineTile

```
public class CIAffineTile : CIAffineFilter {
        
        public CIAffineTile ();
        public CIAffineTile (IntPtr handle);
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIAffineTransform" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIAffineTransform

Removed:

```
public class CIAffineTransform : CIFilter {
        
        public CIImage Image {
                get;
                set;
        }
        public MonoTouch.CoreGraphics.CGAffineTransform Transform {
                get;
                set;
        }
```

Added:

```
public class CIAffineTransform : CIAffineFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIBarsSwipeTransition" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIBarsSwipeTransition

```
public class CIBarsSwipeTransition : CITransitionFilter {
        
        public CIBarsSwipeTransition ();
        public CIBarsSwipeTransition (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
        public float BarOffset {
                get;
                set;
        }
        public float Width {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIBlendFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIBlendFilter

```
public abstract class CIBlendFilter : CIFilter {
        
        protected CIBlendFilter (string name);
        protected CIBlendFilter (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIBlendWithMask" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIBlendWithMask

```
public class CIBlendWithMask : CIBlendFilter {
        
        public CIBlendWithMask ();
        public CIBlendWithMask (IntPtr handle);
        
        public CIImage Mask {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIBloom" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIBloom

```
public class CIBloom : CIFilter {
        
        public CIBloom ();
        public CIBloom (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Intensity {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CICircleSplashDistortion" class="injected"></a>


## New Type: MonoTouch.CoreImage.CICircleSplashDistortion

```
public class CICircleSplashDistortion : CIDistortionFilter {
        
        public CICircleSplashDistortion ();
        public CICircleSplashDistortion (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CICircularScreen" class="injected"></a>


## New Type: MonoTouch.CoreImage.CICircularScreen

```
public class CICircularScreen : CIScreenFilter {
        
        public CICircularScreen ();
        public CICircularScreen (IntPtr handle);
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIColor" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIColor

Removed:

```
public static CIColor FromRgb (float r, float g, float b);
        public static CIColor FromRgba (float r, float g, float b, float a);
```

Added:

```
public static CIColor FromRgb (float red, float green, float blue);
        public static CIColor FromRgba (float red, float green, float blue, float alpha);
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIColorBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIColorBlendMode

Removed:

```
public class CIColorBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIColorBlendMode : CIBlendFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIColorBurnBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIColorBurnBlendMode

Removed:

```
public class CIColorBurnBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIColorBurnBlendMode : CIBlendFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIColorDodgeBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIColorDodgeBlendMode

Removed:

```
public class CIColorDodgeBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIColorDodgeBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorMap" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorMap

```
public class CIColorMap : CIFilter {
        
        public CIColorMap ();
        public CIColorMap (IntPtr handle);
        
        public CIImage GradientImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorPosterize" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorPosterize

```
public class CIColorPosterize : CIFilter {
        
        public CIColorPosterize ();
        public CIColorPosterize (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Levels {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CICompositingFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CICompositingFilter

```
public abstract class CICompositingFilter : CIFilter {
        
        protected CICompositingFilter (string name);
        protected CICompositingFilter (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CICopyMachineTransition" class="injected"></a>


## New Type: MonoTouch.CoreImage.CICopyMachineTransition

```
public class CICopyMachineTransition : CITransitionFilter {
        
        public CICopyMachineTransition ();
        public CICopyMachineTransition (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
        public CIColor Color {
                get;
                set;
        }
        public CIVector Extent {
                get;
                set;
        }
        public float Opacity {
                get;
                set;
        }
        public float Width {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIDarkenBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIDarkenBlendMode

Removed:

```
public class CIDarkenBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIDarkenBlendMode : CIBlendFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIDifferenceBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIDifferenceBlendMode

Removed:

```
public class CIDifferenceBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIDifferenceBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIDisintegrateWithMaskTransition" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIDisintegrateWithMaskTransition

```
public class CIDisintegrateWithMaskTransition : CITransitionFilter {
        
        public CIDisintegrateWithMaskTransition ();
        public CIDisintegrateWithMaskTransition (IntPtr handle);
        
        public CIImage Mask {
                get;
                set;
        }
        public float ShadowDensity {
                get;
                set;
        }
        public CIVector ShadowOffset {
                get;
                set;
        }
        public float ShadowRadius {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIDissolveTransition" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIDissolveTransition

```
public class CIDissolveTransition : CITransitionFilter {
        
        public CIDissolveTransition ();
        public CIDissolveTransition (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIDistortionFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIDistortionFilter

```
public abstract class CIDistortionFilter : CIFilter {
        
        protected CIDistortionFilter (string name);
        protected CIDistortionFilter (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIDotScreen" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIDotScreen

```
public class CIDotScreen : CIScreenFilter {
        
        public CIDotScreen ();
        public CIDotScreen (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIEightfoldReflectedTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIEightfoldReflectedTile

```
public class CIEightfoldReflectedTile : CITileFilter {
        
        public CIEightfoldReflectedTile ();
        public CIEightfoldReflectedTile (IntPtr handle);
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIExclusionBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIExclusionBlendMode

Removed:

```
public class CIExclusionBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIExclusionBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFlashTransition" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFlashTransition

```
public class CIFlashTransition : CITransitionFilter {
        
        public CIFlashTransition ();
        public CIFlashTransition (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIColor Color {
                get;
                set;
        }
        public CIVector Extent {
                get;
                set;
        }
        public float FadeThreshold {
                get;
                set;
        }
        public float MaxStriationContrast {
                get;
                set;
        }
        public float MaxStriationRadius {
                get;
                set;
        }
        public float MaxStriationStrength {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFourfoldReflectedTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFourfoldReflectedTile

```
public class CIFourfoldReflectedTile : CITileFilter {
        
        public CIFourfoldReflectedTile ();
        public CIFourfoldReflectedTile (IntPtr handle);
        
        public float AcuteAngle {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFourfoldRotatedTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFourfoldRotatedTile

```
public class CIFourfoldRotatedTile : CITileFilter {
        
        public CIFourfoldRotatedTile ();
        public CIFourfoldRotatedTile (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFourfoldTranslatedTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFourfoldTranslatedTile

```
public class CIFourfoldTranslatedTile : CITileFilter {
        
        public CIFourfoldTranslatedTile ();
        public CIFourfoldTranslatedTile (IntPtr handle);
        
        public float AcuteAngle {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIGaussianBlur" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIGaussianBlur

```
public class CIGaussianBlur : CIFilter {
        
        public CIGaussianBlur ();
        public CIGaussianBlur (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIGlideReflectedTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIGlideReflectedTile

```
public class CIGlideReflectedTile : CITileFilter {
        
        public CIGlideReflectedTile ();
        public CIGlideReflectedTile (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIGloom" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIGloom

```
public class CIGloom : CIFilter {
        
        public CIGloom ();
        public CIGloom (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Intensity {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIHardLightBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIHardLightBlendMode

Removed:

```
public class CIHardLightBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIHardLightBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIHatchedScreen" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIHatchedScreen

```
public class CIHatchedScreen : CIScreenFilter {
        
        public CIHatchedScreen ();
        public CIHatchedScreen (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIHoleDistortion" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIHoleDistortion

```
public class CIHoleDistortion : CIDistortionFilter {
        
        public CIHoleDistortion ();
        public CIHoleDistortion (IntPtr handle);
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIHueBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIHueBlendMode

Removed:

```
public class CIHueBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIHueBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CILanczosScaleTransform" class="injected"></a>


## New Type: MonoTouch.CoreImage.CILanczosScaleTransform

```
public class CILanczosScaleTransform : CIFilter {
        
        public CILanczosScaleTransform ();
        public CILanczosScaleTransform (IntPtr handle);
        
        public float AspectRatio {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Scale {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CILightTunnel" class="injected"></a>


## New Type: MonoTouch.CoreImage.CILightTunnel

```
public class CILightTunnel : CIFilter {
        
        public CILightTunnel ();
        public CILightTunnel (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
        public float Rotation {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CILightenBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CILightenBlendMode

Removed:

```
public class CILightenBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CILightenBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CILineScreen" class="injected"></a>


## New Type: MonoTouch.CoreImage.CILineScreen

```
public class CILineScreen : CIScreenFilter {
        
        public CILineScreen ();
        public CILineScreen (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CILuminosityBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CILuminosityBlendMode

Removed:

```
public class CILuminosityBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CILuminosityBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIMaskToAlpha" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIMaskToAlpha

```
public class CIMaskToAlpha : CIFilter {
        
        public CIMaskToAlpha ();
        public CIMaskToAlpha (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIMaximumComponent" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIMaximumComponent

```
public class CIMaximumComponent : CIFilter {
        
        public CIMaximumComponent ();
        public CIMaximumComponent (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIMaximumCompositing" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIMaximumCompositing

Removed:

```
public class CIMaximumCompositing : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIMaximumCompositing : CICompositingFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIMinimumComponent" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIMinimumComponent

```
public class CIMinimumComponent : CIFilter {
        
        public CIMinimumComponent ();
        public CIMinimumComponent (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIMinimumCompositing" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIMinimumCompositing

Removed:

```
public class CIMinimumCompositing : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIMinimumCompositing : CICompositingFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIModTransition" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIModTransition

```
public class CIModTransition : CITransitionFilter {
        
        public CIModTransition ();
        public CIModTransition (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
        public CIVector Center {
                get;
                set;
        }
        public float Compression {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIMultiplyBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIMultiplyBlendMode

Removed:

```
public class CIMultiplyBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIMultiplyBlendMode : CIBlendFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIMultiplyCompositing" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIMultiplyCompositing

Removed:

```
public class CIMultiplyCompositing : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIMultiplyCompositing : CICompositingFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIOverlayBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIOverlayBlendMode

Removed:

```
public class CIOverlayBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIOverlayBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIPerspectiveTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIPerspectiveTile

```
public class CIPerspectiveTile : CIFilter {
        
        public CIPerspectiveTile ();
        public CIPerspectiveTile (IntPtr handle);
        
        public CIVector BottomLeft {
                get;
                set;
        }
        public CIVector BottomRight {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public CIVector TopLeft {
                get;
                set;
        }
        public CIVector TopRight {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIPerspectiveTransform" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIPerspectiveTransform

```
public class CIPerspectiveTransform : CIFilter {
        
        public CIPerspectiveTransform ();
        public CIPerspectiveTransform (IntPtr handle);
        
        public CIVector BottomLeft {
                get;
                set;
        }
        public CIVector BottomRight {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public CIVector TopLeft {
                get;
                set;
        }
        public CIVector TopRight {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIPinchDistortion" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIPinchDistortion

```
public class CIPinchDistortion : CIDistortionFilter {
        
        public CIPinchDistortion ();
        public CIPinchDistortion (IntPtr handle);
        
        public float Scale {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIPixellate" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIPixellate

```
public class CIPixellate : CIFilter {
        
        public CIPixellate ();
        public CIPixellate (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Scale {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIRandomGenerator" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIRandomGenerator

```
public class CIRandomGenerator : CIFilter {
        
        public CIRandomGenerator ();
        public CIRandomGenerator (IntPtr handle);
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CISaturationBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CISaturationBlendMode

Removed:

```
public class CISaturationBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CISaturationBlendMode : CIBlendFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIScreenBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIScreenBlendMode

Removed:

```
public class CIScreenBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CIScreenBlendMode : CIBlendFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIScreenFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIScreenFilter

```
public class CIScreenFilter : CIFilter {
        
        protected CIScreenFilter (string name);
        protected CIScreenFilter (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Sharpness {
                get;
                set;
        }
        public float Width {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISharpenLuminance" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISharpenLuminance

```
public class CISharpenLuminance : CIFilter {
        
        public CISharpenLuminance ();
        public CISharpenLuminance (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Sharpness {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISixfoldReflectedTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISixfoldReflectedTile

```
public class CISixfoldReflectedTile : CITileFilter {
        
        public CISixfoldReflectedTile ();
        public CISixfoldReflectedTile (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISixfoldRotatedTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISixfoldRotatedTile

```
public class CISixfoldRotatedTile : CITileFilter {
        
        public CISixfoldRotatedTile ();
        public CISixfoldRotatedTile (IntPtr handle);
}
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CISoftLightBlendMode" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CISoftLightBlendMode

Removed:

```
public class CISoftLightBlendMode : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CISoftLightBlendMode : CIBlendFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CISourceAtopCompositing" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CISourceAtopCompositing

Removed:

```
public class CISourceAtopCompositing : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CISourceAtopCompositing : CICompositingFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CISourceInCompositing" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CISourceInCompositing

Removed:

```
public class CISourceInCompositing : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CISourceInCompositing : CICompositingFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CISourceOutCompositing" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CISourceOutCompositing

Removed:

```
public class CISourceOutCompositing : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CISourceOutCompositing : CICompositingFilter {
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CISourceOverCompositing" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CISourceOverCompositing

Removed:

```
public class CISourceOverCompositing : CIFilter {
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
```

Added:

```
public class CISourceOverCompositing : CICompositingFilter {
```

 <a name="New_Type:_MonoTouch.CoreImage.CIStarShineGenerator" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIStarShineGenerator

```
public class CIStarShineGenerator : CIFilter {
        
        public CIStarShineGenerator ();
        public CIStarShineGenerator (IntPtr handle);
        
        public CIColor Color {
                get;
                set;
        }
        public float CrossAngle {
                get;
                set;
        }
        public float CrossOpacity {
                get;
                set;
        }
        public float CrossScale {
                get;
                set;
        }
        public float CrossWidth {
                get;
                set;
        }
        public float Epsilon {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISwipeTransition" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISwipeTransition

```
public class CISwipeTransition : CITransitionFilter {
        
        public CISwipeTransition ();
        public CISwipeTransition (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
        public CIColor Color {
                get;
                set;
        }
        public CIVector Extent {
                get;
                set;
        }
        public float Opacity {
                get;
                set;
        }
        public float Width {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CITileFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CITileFilter

```
public class CITileFilter : CIFilter {
        
        protected CITileFilter (string name);
        protected CITileFilter (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
        public CIVector Center {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Width {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CITransitionFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CITransitionFilter

```
public abstract class CITransitionFilter : CIFilter {
        
        protected CITransitionFilter (string name);
        protected CITransitionFilter (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public CIImage TargetImage {
                get;
                set;
        }
        public float Time {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CITriangleKaleidoscope" class="injected"></a>


## New Type: MonoTouch.CoreImage.CITriangleKaleidoscope

```
public class CITriangleKaleidoscope : CIFilter {
        
        public CITriangleKaleidoscope ();
        public CITriangleKaleidoscope (IntPtr handle);
        
        public float Decay {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public CIVector Point {
                get;
                set;
        }
        public float Rotation {
                get;
                set;
        }
        public float Size {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CITwelvefoldReflectedTile" class="injected"></a>


## New Type: MonoTouch.CoreImage.CITwelvefoldReflectedTile

```
public class CITwelvefoldReflectedTile : CITileFilter {
        
        public CITwelvefoldReflectedTile ();
        public CITwelvefoldReflectedTile (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CITwirlDistortion" class="injected"></a>


## New Type: MonoTouch.CoreImage.CITwirlDistortion

```
public class CITwirlDistortion : CIDistortionFilter {
        
        public CITwirlDistortion ();
        public CITwirlDistortion (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIUnsharpMask" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIUnsharpMask

```
public class CIUnsharpMask : CIFilter {
        
        public CIUnsharpMask ();
        public CIUnsharpMask (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Intensity {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIVortexDistortion" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIVortexDistortion

```
public class CIVortexDistortion : CIDistortionFilter {
        
        public CIVortexDistortion ();
        public CIVortexDistortion (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


# Namespace: MonoTouch.CoreLocation

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLHeading" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLHeading

Removed:

```
public CLHeading ();
```

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CLHeading ();
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLPlacemark" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLPlacemark

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CLPlacemark ();
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLRegion" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLRegion

Removed:

```
public CLRegion ();
```

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CLRegion ();
```

 <a name="Namespace:_MonoTouch.CoreMotion" class="injected"></a>


# Namespace: MonoTouch.CoreMotion

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMAccelerometerData" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMAccelerometerData

Removed:

```
public CMAccelerometerData ();
```

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CMAccelerometerData ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMAttitude" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMAttitude

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CMAttitude ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMDeviceMotion" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMDeviceMotion

Removed:

```
public CMDeviceMotion ();
```

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CMDeviceMotion ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMGyroData" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMGyroData

Removed:

```
public CMGyroData ();
```

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CMGyroData ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMLogItem" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMLogItem

Removed:

```
public CMLogItem ();
```

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CMLogItem ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMMagnetometerData" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMMagnetometerData

Removed:

```
public CMMagnetometerData ();
```

Added:

```
[Obsolete("This type is not meant to be created by application code")]
        public CMMagnetometerData ();
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSThread" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSThread

Added:

```
public static bool IsMain {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrl" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrl

Removed:

```
public NSUrl (string path, string relativeToUrl);
```

Added:

```
public NSUrl (string path, string relativeToUrl);
        public NSUrl (string path, NSUrl relativeToUrl);
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Added:

```
public static MonoTouch.Foundation.NSObject ObserveTypesAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

Added:

```
public static void RectangleF_objc_msgSend_stret_IntPtr_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
        public static void RectangleF_objc_msgSendSuper_stret_IntPtr_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
        public static void void_objc_msgSend_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
        public static void void_objc_msgSendSuper_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIFont" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIFont

Added:

```
public virtual UIFont WithSize (float size);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewController

Removed:

```
[Obsolete("Derecated in IOS6")]
        public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);
```

Added:

```
[Obsolete("Deprecated in IOS6")]
        public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);
```

&lt;/body&gt;
