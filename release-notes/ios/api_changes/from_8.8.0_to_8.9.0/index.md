---
id: 7E55D472-9BA3-47A3-BDEB-AD9C367BD5AE
title: "From 8.8.0 to 8.9.0"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.8.0" "8.9.0";
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVError

Added values:

```
AirPlayControllerRequiresInternet = -11856,
	AirPlayReceiverRequiresInternet = -11857,
```

## Namespace MonoTouch.CoreAudioKit

### Type Changed: MonoTouch.CoreAudioKit.CABTMidiCentralViewController


Modified base type: <s><font color='red'>MonoTouch.UIKit.UIViewController</font></s>

 <font color='green'>MonoTouch.UIKit.UITableViewController</font>

## Namespace MonoTouch.CoreImage

### New Type MonoTouch.CoreImage.CIMotionBlur

```
public class CIMotionBlur : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIMotionBlur ();
	public CIMotionBlur (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public float Radius { get; set; }
}
```

### New Type MonoTouch.CoreImage.CIZoomBlur

```
public class CIZoomBlur : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIZoomBlur ();
	public CIZoomBlur (IntPtr handle);
	// properties
	public float Amount { get; set; }
	public CIVector Center { get; set; }
}
```

## Namespace MonoTouch.HomeKit

### Type Changed: MonoTouch.HomeKit.HMCharacteristicMetadataUnits

Added value:

```
Seconds = 5,
```

### Type Changed: MonoTouch.HomeKit.HMCharacteristicValueLockMechanism

Added values:

```
LastKnownActionSecuredUsingPhysicalMovement = 9,
	LastKnownActionUnsecuredUsingPhysicalMovement = 10,
```

### Type Changed: MonoTouch.HomeKit.HMError

Added values:

```
CannotUnblockNonBridgeAccessory = 81,
	DeviceLocked = 82,
```

## Namespace MonoTouch.LocalAuthentication

### Type Changed: MonoTouch.LocalAuthentication.LAContext

Added property:

```
public virtual MonoTouch.Foundation.NSNumber MaxBiometryFailures { get; set; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

## Namespace MonoTouch.Metal

### Type Changed: MonoTouch.Metal.IMTLComputeCommandEncoder

Added methods:

```
public virtual void SetBufferOffset (uint offset, uint index);
	public virtual void SetBytes (IntPtr bytes, uint length, uint index);
```

### Type Changed: MonoTouch.Metal.IMTLRenderCommandEncoder

Added methods:

```
public virtual void SetFragmentBufferOffset (uint offset, uint index);
	public virtual void SetFragmentBytes (IntPtr bytes, uint length, uint index);
	public virtual void SetVertexBufferOffset (uint offset, uint index);
	public virtual void SetVertexBytes (IntPtr bytes, uint length, uint index);
```

### Type Changed: MonoTouch.Metal.MTLVertexAttribute

Added property:

```
public virtual MTLDataType AttributeType { get; }
```

## Namespace MonoTouch.NetworkExtension

### Type Changed: MonoTouch.NetworkExtension.NEVpnIke2DiffieHellman

Added values:

```
Group19 = 19,
	Group20 = 20,
	Group21 = 21,
```

### Type Changed: MonoTouch.NetworkExtension.NEVpnIke2EncryptionAlgorithm

Added values:

```
AES128GCM = 5,
	AES256GCM = 6,
```

### Type Changed: MonoTouch.NetworkExtension.NEVpnProtocolIke2

Added property:

```
public virtual NEVpnIke2CertificateType CertificateType { get; set; }
```

### New Type MonoTouch.NetworkExtension.NEVpnIke2CertificateType

```
[Serializable]
public enum NEVpnIke2CertificateType {
	ECDSA256 = 2,
	ECDSA384 = 3,
	ECDSA521 = 4,
	RSA = 1,
}
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added value:

```
iOS_8_3 = 525056,
```

## Namespace MonoTouch.PassKit

### Type Changed: MonoTouch.PassKit.IPKPaymentAuthorizationViewControllerDelegate

Added method:

```
public virtual void WillAuthorizePayment (PKPaymentAuthorizationViewController controller);
```

### Type Changed: MonoTouch.PassKit.PKAddressField

Modified fields:

```
All = 7 15
```

Added value:

```
Name = 8,
```

### Type Changed: MonoTouch.PassKit.PKPassLibrary

Added method:

```
public virtual void OpenPaymentSetup ();
```

### Type Changed: MonoTouch.PassKit.PKPaymentAuthorizationViewController

Added event:

```
public event System.EventHandler WillAuthorizePayment;
```

### Type Changed: MonoTouch.PassKit.PKPaymentAuthorizationViewControllerDelegate

Added method:

```
public virtual void WillAuthorizePayment (PKPaymentAuthorizationViewController controller);
```

### Type Changed: MonoTouch.PassKit.PKPaymentRequest

Added property:

```
public virtual PKShippingType ShippingType { get; set; }
```

### New Type MonoTouch.PassKit.PKPaymentButton

```
public class PKPaymentButton : MonoTouch.UIKit.UIButton, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAccessibilityIdentification, MonoTouch.UIKit.IUICoordinateSpace, MonoTouch.UIKit.IUIDynamicItem, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public PKPaymentButton (MonoTouch.Foundation.NSCoder coder);
	public PKPaymentButton (MonoTouch.Foundation.NSObjectFlag t);
	public PKPaymentButton (IntPtr handle);
	// properties
	public static PKPaymentButton.PKPaymentButtonAppearance Appearance { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public static PKPaymentButton.PKPaymentButtonAppearance AppearanceWhenContainedIn (System.Type[] containers);
	public static PKPaymentButton FromType (PKPaymentButtonType buttonType, PKPaymentButtonStyle buttonStyle);
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T> ();
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);

	[Obsolete ("Use the non-generic overload instead")]
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);

	[Obsolete ("Use the non-generic overload instead")]
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);

	// inner types
	public class PKPaymentButtonAppearance : MonoTouch.UIKit.UIButton+UIButtonAppearance, MonoTouch.UIKit.IUIAppearance, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	}
}
```

### New Type MonoTouch.PassKit.PKPaymentButtonStyle

```
[Serializable]
public enum PKPaymentButtonStyle {
	Black = 2,
	White = 0,
	WhiteOutline = 1,
}
```

### New Type MonoTouch.PassKit.PKPaymentButtonType

```
[Serializable]
public enum PKPaymentButtonType {
	Buy = 1,
	Plain = 0,
}
```

### New Type MonoTouch.PassKit.PKShippingType

```
[Serializable]
public enum PKShippingType {
	Delivery = 1,
	ServicePickup = 3,
	Shipping = 0,
	StorePickup = 2,
}
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecPadding

Added value:

```
Raw = 16384,
```

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.SKMutablePayment

Added property:

```
public virtual bool SimulatesAskToBuyInSandbox { get; set; }
```

### Type Changed: MonoTouch.StoreKit.SKPayment

Added property:

```
public virtual bool SimulatesAskToBuyInSandbox { get; set; }
```

### Type Changed: MonoTouch.StoreKit.SKStoreProductParameterKey

Added property:

```
public static MonoTouch.Foundation.NSString ProviderToken { get; }
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIAdaptivePresentationControllerDelegate

Added methods:

```
public virtual UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style);
	public virtual void WillPresent (UIPresentationController presentationController, UIModalPresentationStyle style, IUIViewControllerTransitionCoordinator transitionCoordinator);
```

### Type Changed: MonoTouch.UIKit.UIAdaptivePresentationControllerDelegate_Extensions

Added methods:

```
public static UIViewController GetAdaptivePresentationStyle (IUIAdaptivePresentationControllerDelegate This, UIPresentationController controller, UIModalPresentationStyle style);
	public static void WillPresent (IUIAdaptivePresentationControllerDelegate This, UIPresentationController presentationController, UIModalPresentationStyle style, IUIViewControllerTransitionCoordinator transitionCoordinator);
```

### Type Changed: MonoTouch.UIKit.UIPopoverPresentationControllerDelegate

Added methods:

```
public override UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style);
	public override void WillPresent (UIPresentationController presentationController, UIModalPresentationStyle style, IUIViewControllerTransitionCoordinator transitionCoordinator);
```

### Type Changed: MonoTouch.UIKit.UIPresentationController

Added method:

```
public virtual UIModalPresentationStyle AdaptivePresentationStyle (UITraitCollection traitCollection);
```

   


 <hr>

# Xamarin.iOS.dll

## Namespace AVFoundation

### Type Changed: AVFoundation.AVError

Added values:

```
AirPlayControllerRequiresInternet = -11856,
	AirPlayReceiverRequiresInternet = -11857,
```

## Namespace CoreAudioKit

### Type Changed: CoreAudioKit.CABTMidiCentralViewController


Modified base type: <s><font color='red'>UIKit.UIViewController</font></s>

 <font color='green'>UIKit.UITableViewController</font>

## Namespace CoreImage

### New Type CoreImage.CIMotionBlur

```
public class CIMotionBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public CIMotionBlur ();
	public CIMotionBlur (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public float Radius { get; set; }
}
```

### New Type CoreImage.CIZoomBlur

```
public class CIZoomBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public CIZoomBlur ();
	public CIZoomBlur (IntPtr handle);
	// properties
	public float Amount { get; set; }
	public CIVector Center { get; set; }
}
```

## Namespace HomeKit

### Type Changed: HomeKit.HMCharacteristicMetadataUnits

Added value:

```
Seconds = 5,
```

### Type Changed: HomeKit.HMCharacteristicValueLockMechanism

Added values:

```
LastKnownActionSecuredUsingPhysicalMovement = 9,
	LastKnownActionUnsecuredUsingPhysicalMovement = 10,
```

### Type Changed: HomeKit.HMError

Added values:

```
CannotUnblockNonBridgeAccessory = 81,
	DeviceLocked = 82,
```

## Namespace LocalAuthentication

### Type Changed: LocalAuthentication.LAContext

Added property:

```
public virtual Foundation.NSNumber MaxBiometryFailures { get; set; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

## Namespace Metal

### Type Changed: Metal.IMTLComputeCommandEncoder

Added methods:

```
public virtual void SetBufferOffset (uint offset, uint index);
	public virtual void SetBytes (IntPtr bytes, uint length, uint index);
```

### Type Changed: Metal.IMTLRenderCommandEncoder

Added methods:

```
public virtual void SetFragmentBufferOffset (uint offset, uint index);
	public virtual void SetFragmentBytes (IntPtr bytes, uint length, uint index);
	public virtual void SetVertexBufferOffset (uint offset, uint index);
	public virtual void SetVertexBytes (IntPtr bytes, uint length, uint index);
```

### Type Changed: Metal.MTLVertexAttribute

Added property:

```
public virtual MTLDataType AttributeType { get; }
```

## Namespace NetworkExtension

### Type Changed: NetworkExtension.NEVpnIke2DiffieHellman

Added values:

```
Group19 = 19,
	Group20 = 20,
	Group21 = 21,
```

### Type Changed: NetworkExtension.NEVpnIke2EncryptionAlgorithm

Added values:

```
AES128GCM = 5,
	AES256GCM = 6,
```

### Type Changed: NetworkExtension.NEVpnProtocolIke2

Added property:

```
public virtual NEVpnIke2CertificateType CertificateType { get; set; }
```

### New Type NetworkExtension.NEVpnIke2CertificateType

```
[Serializable]
public enum NEVpnIke2CertificateType {
	ECDSA256 = 2,
	ECDSA384 = 3,
	ECDSA521 = 4,
	RSA = 1,
}
```

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.8.0" "8.9.0";
```

### Type Changed: ObjCRuntime.Platform

Added value:

```
iOS_8_3 = 525056,
```

## Namespace PassKit

### Type Changed: PassKit.IPKPaymentAuthorizationViewControllerDelegate

Added method:

```
public virtual void WillAuthorizePayment (PKPaymentAuthorizationViewController controller);
```

### Type Changed: PassKit.PKAddressField

Modified fields:

```
All = 7 15
```

Added value:

```
Name = 8,
```

### Type Changed: PassKit.PKPassLibrary

Added method:

```
public virtual void OpenPaymentSetup ();
```

### Type Changed: PassKit.PKPaymentAuthorizationViewController

Added event:

```
public event System.EventHandler WillAuthorizePayment;
```

### Type Changed: PassKit.PKPaymentAuthorizationViewControllerDelegate

Added method:

```
public virtual void WillAuthorizePayment (PKPaymentAuthorizationViewController controller);
```

### Type Changed: PassKit.PKPaymentRequest

Added property:

```
public virtual PKShippingType ShippingType { get; set; }
```

### New Type PassKit.PKPaymentButton

```
public class PKPaymentButton : UIKit.UIButton, System.Collections.IEnumerable, Foundation.INSCoding, UIKit.IUIAccessibilityIdentification, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public PKPaymentButton (Foundation.NSCoder coder);
	protected PKPaymentButton (Foundation.NSObjectFlag t);
	protected PKPaymentButton (IntPtr handle);
	// properties
	public static PKPaymentButton.PKPaymentButtonAppearance Appearance { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public static PKPaymentButton.PKPaymentButtonAppearance AppearanceWhenContainedIn (System.Type[] containers);
	public static PKPaymentButton FromType (PKPaymentButtonType buttonType, PKPaymentButtonStyle buttonStyle);
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T> ();
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);

	[Obsolete ("Use the non-generic overload instead")]
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T> (UIKit.UITraitCollection traits);

	[Obsolete ("Use the non-generic overload instead")]
	public static PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);

	// inner types
	public class PKPaymentButtonAppearance : UIKit.UIButton+UIButtonAppearance, UIKit.IUIAppearance, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	}
}
```

### New Type PassKit.PKPaymentButtonStyle

```
[Serializable]
public enum PKPaymentButtonStyle {
	Black = 2,
	White = 0,
	WhiteOutline = 1,
}
```

### New Type PassKit.PKPaymentButtonType

```
[Serializable]
public enum PKPaymentButtonType {
	Buy = 1,
	Plain = 0,
}
```

### New Type PassKit.PKShippingType

```
[Serializable]
public enum PKShippingType {
	Delivery = 1,
	ServicePickup = 3,
	Shipping = 0,
	StorePickup = 2,
}
```

## Namespace Security

### Type Changed: Security.SecPadding

Added value:

```
Raw = 16384,
```

## Namespace StoreKit

### Type Changed: StoreKit.SKMutablePayment

Added property:

```
public virtual bool SimulatesAskToBuyInSandbox { get; set; }
```

### Type Changed: StoreKit.SKPayment

Added property:

```
public virtual bool SimulatesAskToBuyInSandbox { get; set; }
```

### Type Changed: StoreKit.SKStoreProductParameterKey

Added property:

```
public static Foundation.NSString ProviderToken { get; }
```

## Namespace UIKit

### Type Changed: UIKit.UIAdaptivePresentationControllerDelegate

Added methods:

```
public virtual UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style);
	public virtual void WillPresent (UIPresentationController presentationController, UIModalPresentationStyle style, IUIViewControllerTransitionCoordinator transitionCoordinator);
```

### Type Changed: UIKit.UIAdaptivePresentationControllerDelegate_Extensions

Added methods:

```
public static UIViewController GetAdaptivePresentationStyle (IUIAdaptivePresentationControllerDelegate This, UIPresentationController controller, UIModalPresentationStyle style);
	public static void WillPresent (IUIAdaptivePresentationControllerDelegate This, UIPresentationController presentationController, UIModalPresentationStyle style, IUIViewControllerTransitionCoordinator transitionCoordinator);
```

### Type Changed: UIKit.UIPresentationController

Added method:

```
public virtual UIModalPresentationStyle AdaptivePresentationStyle (UITraitCollection traitCollection);
```

   


 <hr>
