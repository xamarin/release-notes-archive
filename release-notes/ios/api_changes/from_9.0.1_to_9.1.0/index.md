---
id: 0A6CC6B7-E961-46EF-BA1F-F83C9106628C
title: "From 9.0.1 to 9.1.0"
---

# API diff

 [(Xamarin.iOS/Classic) System.Net.Http.dll](#diff/xi/2.1/System.Net.Http.html)

   


 [(Xamarin.iOS/Classic) monotouch.dll](#diff/xi/2.1/monotouch.html)

   


 [(Xamarin.iOS/Classic) MonoTouch.Dialog-1.dll](#diff/xi/2.1/MonoTouch.Dialog-1.html)

   


 [(Xamarin.iOS/Classic) MonoTouch.NUnitLite.dll](#diff/xi/2.1/MonoTouch.NUnitLite.html)

   


 [(Xamarin.iOS/Classic) OpenTK.dll](#diff/xi/2.1/OpenTK.html)

   


 [(Xamarin.iOS/Classic) OpenTK-1.0.dll](#diff/xi/2.1/OpenTK-1.0.html)

   


 [(Xamarin.iOS/Unified) MonoTouch.Dialog-1.dll](#diff/xi/Xamarin.iOS/MonoTouch.Dialog-1.html)

   


 [(Xamarin.iOS/Unified) MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.iOS/MonoTouch.NUnitLite.html)

   


 [(Xamarin.iOS/Unified) OpenTK-1.0.dll](#diff/xi/Xamarin.iOS/OpenTK-1.0.html)

   


 [(Xamarin.iOS/Unified) System.Net.Http.dll](#diff/xi/Xamarin.iOS/System.Net.Http.html)

   


 [(Xamarin.iOS/Unified) Xamarin.iOS.dll](#diff/xi/Xamarin.iOS/Xamarin.iOS.html)

   


   


 <hr>

<h1 id='diff/xi/2.1/System.Net.Http.html'>System.Net.Http.dll</h1>

## Namespace System.Net.Http

### New Type System.Net.Http.CFNetworkHandler

```
public class CFNetworkHandler : System.Net.Http.HttpMessageHandler, System.IDisposable {
	// constructors
	public CFNetworkHandler ();
	// properties
	public bool AllowAutoRedirect { get; set; }
	public System.Net.CookieContainer CookieContainer { get; set; }
	public bool UseSystemProxy { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	protected override System.Threading.Tasks.Task<HttpResponseMessage> SendAsync (HttpRequestMessage request, System.Threading.CancellationToken cancellationToken);
}
```

   


 <hr>

<h1 id='diff/xi/2.1/monotouch.html'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string SdkVersion = "9.0" "9.1";
	public const string Version = "9.0.1" "9.1.0";
```

### Type Changed: MonoTouch.MonoNativeFunctionWrapperAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.MonoPInvokeCallbackAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.RuntimeException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABNewPersonViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.AddressBookUI.ABPersonViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.AddressBookUI.ABUnknownPersonViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.AudioQueueException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.AudioToolbox.AudioSessionException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioUnitException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.AVKit

### Type Changed: MonoTouch.AVKit.AVPlayerViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.CoreAudioKit

### Type Changed: MonoTouch.CoreAudioKit.AUViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CABTMidiCentralViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CABTMidiLocalPeripheralViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioSwitcherView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioTransportView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.CoreBluetooth

### New Type MonoTouch.CoreBluetooth.CBATTErrorExtensions

```
public static class CBATTErrorExtensions {
	// methods
	public static MonoTouch.Foundation.NSString GetDomain (CBATTError self);
}
```

### New Type MonoTouch.CoreBluetooth.CBErrorExtensions

```
public static class CBErrorExtensions {
	// methods
	public static MonoTouch.Foundation.NSString GetDomain (CBError self);
}
```

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.CoreFoundation.CFSocketException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.CoreMidi

### Type Changed: MonoTouch.CoreMidi.MidiException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.EventKitUI

### Type Changed: MonoTouch.EventKitUI.EKCalendarChooser

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.EventKitUI.EKEventViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.ActionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.AdviceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ConnectAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ExportAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.FieldAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.LinkerSafeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ModelAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ModelNotImplementedException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.Foundation.MonoTouchException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.Foundation.NSAttributedString

Added properties:

<pre style='color: green'>
	public static NSString TextLayoutSectionOrientation { get; }
	public static NSString TextLayoutSectionRange { get; }
	public static NSString TextLayoutSectionsAttribute { get; }
</pre>

### Type Changed: MonoTouch.Foundation.NSErrorException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionConfiguration

Modified properties:

```
public virtual bool ShouldUseExtendedBackgroundIdleMode { get; set; }
```

### Type Changed: MonoTouch.Foundation.OutletAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.PreserveAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ProtocolAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ProtocolMemberAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.RegisterAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.You_Should_Not_Call_base_In_This_Method

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKAchievementViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.GameKit.GKGameCenterViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.GameKit.GKMatchmakerViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.GameplayKit

### Type Changed: MonoTouch.GameplayKit.GKGameModel_Extensions

Added method:

<pre style='color: green'>
	public static void UnapplyGameModelUpdate (IGKGameModel This, IGKGameModelUpdate gameModelUpdate);
</pre>

### Type Changed: MonoTouch.GameplayKit.GKMinMaxStrategist

Added interface:

<pre style='color: green'>
	IGKStrategist
</pre>

Added method:

<pre style='color: green'>
	public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();
</pre>

### New Type MonoTouch.GameplayKit.GKHybridStrategist

```
public class GKHybridStrategist : MonoTouch.Foundation.NSObject, IGKStrategist, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public GKHybridStrategist ();
	public GKHybridStrategist (MonoTouch.Foundation.NSCoder coder);
	public GKHybridStrategist (MonoTouch.Foundation.NSObjectFlag t);
	public GKHybridStrategist (IntPtr handle);
	// properties
	public virtual uint Budget { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual uint ExplorationParameter { get; set; }
	public virtual IGKGameModel GameModel { get; set; }
	public virtual uint MaxLookAheadDepth { get; set; }
	public virtual IGKRandom RandomSource { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();
}
```

### New Type MonoTouch.GameplayKit.GKMonteCarloStrategist

```
public class GKMonteCarloStrategist : MonoTouch.Foundation.NSObject, IGKStrategist, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public GKMonteCarloStrategist ();
	public GKMonteCarloStrategist (MonoTouch.Foundation.NSCoder coder);
	public GKMonteCarloStrategist (MonoTouch.Foundation.NSObjectFlag t);
	public GKMonteCarloStrategist (IntPtr handle);
	// properties
	public virtual uint Budget { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual uint ExplorationParameter { get; set; }
	public virtual IGKGameModel GameModel { get; set; }
	public virtual IGKRandom RandomSource { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();
}
```

### New Type MonoTouch.GameplayKit.GKQuadTree

```
public class GKQuadTree : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public GKQuadTree (MonoTouch.Foundation.NSCoder coder);
	public GKQuadTree (MonoTouch.Foundation.NSObjectFlag t);
	public GKQuadTree (IntPtr handle);
	public GKQuadTree (OpenTK.Vector2 min, OpenTK.Vector2 max, float minCellSize);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual GKQuadTreeNode AddData (MonoTouch.Foundation.NSObject data, OpenTK.Vector2 point);
	public virtual GKQuadTreeNode AddData (MonoTouch.Foundation.NSObject data, OpenTK.Vector2 quadOrigin, OpenTK.Vector2 quadSize);
	public static GKQuadTree QuadTreeWithMinPosition (OpenTK.Vector2 min, OpenTK.Vector2 max, float minCellSize);
	public virtual MonoTouch.Foundation.NSObject[] QueryData (OpenTK.Vector2 point);
	public virtual MonoTouch.Foundation.NSObject[] QueryData (OpenTK.Vector2 quadOrigin, OpenTK.Vector2 quadSize);
	public virtual bool RemoveData (MonoTouch.Foundation.NSObject data);
	public virtual bool RemoveData (MonoTouch.Foundation.NSObject data, GKQuadTreeNode node);
}
```

### New Type MonoTouch.GameplayKit.GKQuadTreeNode

```
public class GKQuadTreeNode : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public GKQuadTreeNode ();
	public GKQuadTreeNode (MonoTouch.Foundation.NSCoder coder);
	public GKQuadTreeNode (MonoTouch.Foundation.NSObjectFlag t);
	public GKQuadTreeNode (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.GameplayKit.GKStrategist_Extensions

```
public static class GKStrategist_Extensions {
}
```

### New Type MonoTouch.GameplayKit.IGKStrategist

```
public interface IGKStrategist : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IGKGameModel GameModel { get; set; }
	public virtual IGKRandom RandomSource { get; set; }
	// methods
	public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();
}
```

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.GLKit.GLKViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.HealthKit

### New Type MonoTouch.HealthKit.HKErrorCodeExtensions

```
public static class HKErrorCodeExtensions {
	// methods
	public static MonoTouch.Foundation.NSString GetDomain (HKErrorCode self);
}
```

## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADBannerView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MapKit.MKCircleView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MapKit.MKMapView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MapKit.MKOverlayView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MapKit.MKPolygonView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MapKit.MKPolylineView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMediaPickerController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPNowPlayingInfoLanguageOption

Added property:

<pre style='color: green'>
	public virtual bool IsAutomaticAudibleLanguageOption { get; }
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPRemoteCommandCenter

Added property:

<pre style='color: green'>
	public virtual MPChangePlaybackPositionCommand ChangePlaybackPositionCommand { get; }
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPRemoteCommandHandlerStatus

Added value:

```
NoActionableNowPlayingItem = 110,
```

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### New Type MonoTouch.MediaPlayer.MPChangePlaybackPositionCommand

```
public class MPChangePlaybackPositionCommand : MonoTouch.MediaPlayer.MPRemoteCommand, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MPChangePlaybackPositionCommand (MonoTouch.Foundation.NSCoder coder);
	public MPChangePlaybackPositionCommand (MonoTouch.Foundation.NSObjectFlag t);
	public MPChangePlaybackPositionCommand (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.MediaPlayer.MPChangePlaybackPositionCommandEvent

```
public class MPChangePlaybackPositionCommandEvent : MonoTouch.MediaPlayer.MPRemoteCommandEvent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MPChangePlaybackPositionCommandEvent (MonoTouch.Foundation.NSCoder coder);
	public MPChangePlaybackPositionCommandEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPChangePlaybackPositionCommandEvent (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual double PositionTime { get; }
}
```

## Namespace MonoTouch.MessageUI

### Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.Metal

### Type Changed: MonoTouch.Metal.MTLFeatureSet

Added values:

```
OSX_GPUFamily1_v1 = 10000,
	TVOS_GPUFamily1_v1 = 30000,
```

## Namespace MonoTouch.MetalKit

### Type Changed: MonoTouch.MetalKit.MTKView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.MobileCoreServices

### Type Changed: MonoTouch.MobileCoreServices.UTType

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString LivePhoto { get; }
</pre>

## Namespace MonoTouch.MultipeerConnectivity

### Type Changed: MonoTouch.MultipeerConnectivity.MCBrowserViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.AdoptsAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.AlphaAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.AvailabilityAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.BlockProxyAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.CategoryAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.DesignatedInitializerAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.iOSAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.LinkWithAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.LionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.MacAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.MavericksAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

<pre style='color: green'>
	public static int int_objc_msgSend_IntPtr_IntPtr_SizeF_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.SizeF arg3, int arg4, IntPtr arg5);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_SizeF_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.SizeF arg3, int arg4, IntPtr arg5);
	public static void void_objc_msgSend_IntPtr_out_Int32_out_Single (IntPtr receiver, IntPtr selector, IntPtr arg1, out int arg2, out float arg3);
	public static void void_objc_msgSendSuper_IntPtr_out_Int32_out_Single (IntPtr receiver, IntPtr selector, IntPtr arg1, out int arg2, out float arg3);
	public static IntPtr xamarin_simd__IntPtr_objc_msgSend_IntPtr_Vector2 (IntPtr receiver, IntPtr selector, IntPtr arg1, OpenTK.Vector2 arg2);
	public static IntPtr xamarin_simd__IntPtr_objc_msgSend_IntPtr_Vector2_Vector2 (IntPtr receiver, IntPtr selector, IntPtr arg1, OpenTK.Vector2 arg2, OpenTK.Vector2 arg3);
	public static IntPtr xamarin_simd__IntPtr_objc_msgSend_Vector2_Vector2 (IntPtr receiver, IntPtr selector, OpenTK.Vector2 arg1, OpenTK.Vector2 arg2);
	public static IntPtr xamarin_simd__IntPtr_objc_msgSend_Vector2_Vector2_float (IntPtr receiver, IntPtr selector, OpenTK.Vector2 arg1, OpenTK.Vector2 arg2, float arg3);
	public static IntPtr xamarin_simd__IntPtr_objc_msgSendSuper_IntPtr_Vector2 (IntPtr receiver, IntPtr selector, IntPtr arg1, OpenTK.Vector2 arg2);
	public static IntPtr xamarin_simd__IntPtr_objc_msgSendSuper_IntPtr_Vector2_Vector2 (IntPtr receiver, IntPtr selector, IntPtr arg1, OpenTK.Vector2 arg2, OpenTK.Vector2 arg3);
	public static IntPtr xamarin_simd__IntPtr_objc_msgSendSuper_Vector2_Vector2 (IntPtr receiver, IntPtr selector, OpenTK.Vector2 arg1, OpenTK.Vector2 arg2);
	public static IntPtr xamarin_simd__IntPtr_objc_msgSendSuper_Vector2_Vector2_float (IntPtr receiver, IntPtr selector, OpenTK.Vector2 arg1, OpenTK.Vector2 arg2, float arg3);
</pre>

### Type Changed: MonoTouch.ObjCRuntime.MountainLionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.NativeAttribute

Added constructor:

<pre style='color: green'>
	public NativeAttribute (string name);
</pre>

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

Added property:

<pre style='color: green'>
	public string NativeName { get; set; }
</pre>

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added value:

```
iOS_9_1 = 590080,
```

### Type Changed: MonoTouch.ObjCRuntime.ReleaseAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.SinceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.ThreadSafeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.TransientAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### New Type MonoTouch.ObjCRuntime.AvailabilityBaseAttribute

```
public abstract class AvailabilityBaseAttribute : System.Attribute {
	// properties
	public PlatformArchitecture Architecture { get; }
	public AvailabilityKind AvailabilityKind { get; }
	public string Message { get; }
	public PlatformName Platform { get; }
	public System.Version Version { get; }
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.ObjCRuntime.AvailabilityKind

```
[Serializable]
public enum AvailabilityKind {
	Deprecated = 1,
	Introduced = 0,
	Obsoleted = 2,
	Unavailable = 3,
}
```

### New Type MonoTouch.ObjCRuntime.DeprecatedAttribute

```
public sealed class DeprecatedAttribute : MonoTouch.ObjCRuntime.AvailabilityBaseAttribute {
	// constructors
	public DeprecatedAttribute (PlatformName platform, PlatformArchitecture architecture, string message);
	public DeprecatedAttribute (PlatformName platform, int majorVersion, int minorVersion, PlatformArchitecture architecture, string message);
	public DeprecatedAttribute (PlatformName platform, int majorVersion, int minorVersion, int subminorVersion, PlatformArchitecture architecture, string message);
}
```

### New Type MonoTouch.ObjCRuntime.IntroducedAttribute

```
public sealed class IntroducedAttribute : MonoTouch.ObjCRuntime.AvailabilityBaseAttribute {
	// constructors
	public IntroducedAttribute (PlatformName platform, PlatformArchitecture architecture, string message);
	public IntroducedAttribute (PlatformName platform, int majorVersion, int minorVersion, PlatformArchitecture architecture, string message);
	public IntroducedAttribute (PlatformName platform, int majorVersion, int minorVersion, int subminorVersion, PlatformArchitecture architecture, string message);
}
```

### New Type MonoTouch.ObjCRuntime.ObsoletedAttribute

```
public sealed class ObsoletedAttribute : MonoTouch.ObjCRuntime.AvailabilityBaseAttribute {
	// constructors
	public ObsoletedAttribute (PlatformName platform, PlatformArchitecture architecture, string message);
	public ObsoletedAttribute (PlatformName platform, int majorVersion, int minorVersion, PlatformArchitecture architecture, string message);
	public ObsoletedAttribute (PlatformName platform, int majorVersion, int minorVersion, int subminorVersion, PlatformArchitecture architecture, string message);
}
```

### New Type MonoTouch.ObjCRuntime.PlatformArchitecture

```
[Serializable]
[Flags]
public enum PlatformArchitecture {
	All = 255,
	Arch32 = 1,
	Arch64 = 2,
	None = 0,
}
```

### New Type MonoTouch.ObjCRuntime.PlatformName

```
[Serializable]
public enum PlatformName {
	iOS = 2,
	MacOSX = 1,
	None = 0,
	TvOS = 4,
	WatchOS = 3,
}
```

### New Type MonoTouch.ObjCRuntime.UnavailableAttribute

```
public sealed class UnavailableAttribute : MonoTouch.ObjCRuntime.AvailabilityBaseAttribute {
	// constructors
	public UnavailableAttribute (PlatformName platform, PlatformArchitecture architecture, string message);
}
```

## Namespace MonoTouch.PassKit

### Type Changed: MonoTouch.PassKit.PKAddPassButton

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.PassKit.PKAddPassesViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.PassKit.PKAddPaymentPassViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.PassKit.PKPaymentAuthorizationViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.PassKit.PKPaymentButton

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.Photos

### Type Changed: MonoTouch.Photos.PHAssetMediaSubtype

Added value:

```
PhotoLive = 8,
```

### Type Changed: MonoTouch.Photos.PHAssetResource

Added method:

<pre style='color: green'>
	public static PHAssetResource[] GetAssetResources (PHLivePhoto livePhoto);
</pre>

### Type Changed: MonoTouch.Photos.PHAssetResourceType

Added value:

```
PairedVideo = 9,
```

### Type Changed: MonoTouch.Photos.PHImageManager

Added method:

<pre style='color: green'>
	public virtual int RequestLivePhoto (PHAsset asset, System.Drawing.SizeF targetSize, PHImageContentMode contentMode, PHLivePhotoRequestOptions options, PHImageManagerRequestLivePhoto resultHandler);
</pre>

### New Type MonoTouch.Photos.PHImageManagerRequestLivePhoto

```
public sealed delegate PHImageManagerRequestLivePhoto : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHImageManagerRequestLivePhoto (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (PHLivePhoto livePhoto, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (PHLivePhoto livePhoto, MonoTouch.Foundation.NSDictionary info);
}
```

### New Type MonoTouch.Photos.PHLivePhoto

```
public class PHLivePhoto : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public PHLivePhoto ();
	public PHLivePhoto (MonoTouch.Foundation.NSCoder coder);
	public PHLivePhoto (MonoTouch.Foundation.NSObjectFlag t);
	public PHLivePhoto (IntPtr handle);
	// fields
	public static const int RequestIdInvalid;
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual System.Drawing.SizeF Size { get; }
	// methods
	public static void CancelLivePhotoRequest (int requestID);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static int RequestLivePhoto (MonoTouch.Foundation.NSUrl[] fileUrls, MonoTouch.UIKit.UIImage image, System.Drawing.SizeF targetSize, PHImageContentMode contentMode, System.Action<PHLivePhoto,MonoTouch.Foundation.NSDictionary> resultHandler);
}
```

### New Type MonoTouch.Photos.PHLivePhotoInfo

```
public static class PHLivePhotoInfo {
	// properties
	public static MonoTouch.Foundation.NSString CancelledKey { get; }
	public static MonoTouch.Foundation.NSString ErrorKey { get; }
	public static MonoTouch.Foundation.NSString IsDegradedKey { get; }
}
```

### New Type MonoTouch.Photos.PHLivePhotoRequestOptions

```
public class PHLivePhotoRequestOptions : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public PHLivePhotoRequestOptions ();
	public PHLivePhotoRequestOptions (MonoTouch.Foundation.NSCoder coder);
	public PHLivePhotoRequestOptions (MonoTouch.Foundation.NSObjectFlag t);
	public PHLivePhotoRequestOptions (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }
	public virtual bool NetworkAccessAllowed { get; set; }
	public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

## Namespace MonoTouch.PhotosUI

### New Type MonoTouch.PhotosUI.IPHLivePhotoViewDelegate

```
public interface IPHLivePhotoViewDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.PhotosUI.PHLivePhotoBadgeOptions

```
[Serializable]
[Flags]
public enum PHLivePhotoBadgeOptions {
	LiveOff = 2,
	None = 0,
	OverContent = 1,
}
```

### New Type MonoTouch.PhotosUI.PHLivePhotoView

```
public class PHLivePhotoView : MonoTouch.UIKit.UIView, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAccessibilityIdentification, MonoTouch.UIKit.IUIAppearance, MonoTouch.UIKit.IUIAppearanceContainer, MonoTouch.UIKit.IUICoordinateSpace, MonoTouch.UIKit.IUIDynamicItem, MonoTouch.UIKit.IUIFocusEnvironment, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public PHLivePhotoView ();
	public PHLivePhotoView (MonoTouch.Foundation.NSCoder coder);
	public PHLivePhotoView (MonoTouch.Foundation.NSObjectFlag t);
	public PHLivePhotoView (System.Drawing.RectangleF frame);
	public PHLivePhotoView (IntPtr handle);
	// properties
	public static PHLivePhotoView.PHLivePhotoViewAppearance Appearance { get; }
	public override IntPtr ClassHandle { get; }
	public PHLivePhotoViewDelegate Delegate { get; set; }
	public virtual MonoTouch.Photos.PHLivePhoto LivePhoto { get; set; }
	public virtual bool Muted { get; set; }
	public virtual MonoTouch.UIKit.UIGestureRecognizer PlaybackGestureRecognizer { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public static PHLivePhotoView.PHLivePhotoViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance<T> ();
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static MonoTouch.UIKit.UIImage GetLivePhotoBadgeImage (PHLivePhotoBadgeOptions badgeOptions);
	public virtual void StartPlayback (PHLivePhotoViewPlaybackStyle playbackStyle);
	public virtual void StopPlayback ();

	// inner types
	public class PHLivePhotoViewAppearance : MonoTouch.UIKit.UIView+UIViewAppearance, MonoTouch.UIKit.IUIAppearance, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
		// constructors
		protected PHLivePhotoView (IntPtr handle);
	}
}
```

### New Type MonoTouch.PhotosUI.PHLivePhotoViewDelegate

```
public class PHLivePhotoViewDelegate : MonoTouch.Foundation.NSObject, IPHLivePhotoViewDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public PHLivePhotoViewDelegate ();
	public PHLivePhotoViewDelegate (MonoTouch.Foundation.NSCoder coder);
	public PHLivePhotoViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public PHLivePhotoViewDelegate (IntPtr handle);
	// methods
	public virtual void DidEndPlayback (PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);
	public virtual void WillBeginPlayback (PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);
}
```

### New Type MonoTouch.PhotosUI.PHLivePhotoViewDelegate_Extensions

```
public static class PHLivePhotoViewDelegate_Extensions {
	// methods
	public static void DidEndPlayback (IPHLivePhotoViewDelegate This, PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);
	public static void WillBeginPlayback (IPHLivePhotoViewDelegate This, PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);
}
```

### New Type MonoTouch.PhotosUI.PHLivePhotoViewPlaybackStyle

```
[Serializable]
public enum PHLivePhotoViewPlaybackStyle {
	Full = 1,
	Hint = 2,
	Undefined = 0,
}
```

## Namespace MonoTouch.QuickLook

### Type Changed: MonoTouch.QuickLook.QLPreviewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.ReplayKit

### Type Changed: MonoTouch.ReplayKit.RPPreviewViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.SafariServices

### Type Changed: MonoTouch.SafariServices.SFSafariViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.SceneKit

### Type Changed: MonoTouch.SceneKit.SCNView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecurityException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.Social

### Type Changed: MonoTouch.Social.SLComposeServiceViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Social.SLComposeViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.SKStoreProductViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.SystemConfiguration

### Type Changed: MonoTouch.SystemConfiguration.SystemConfigurationException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.Twitter

### Type Changed: MonoTouch.Twitter.TWTweetComposeViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIActionSheet

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIActivityViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIAlertController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIAlertView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIApplicationShortcutIconType

Added values:

```
Alarm = 24,
	Audio = 27,
	Bookmark = 25,
	CapturePhoto = 20,
	CaptureVideo = 21,
	Cloud = 13,
	Confirmation = 15,
	Contact = 8,
	Date = 18,
	Favorite = 11,
	Home = 9,
	Invitation = 14,
	Love = 12,
	Mail = 16,
	MarkLocation = 10,
	Message = 17,
	Prohibit = 7,
	Shuffle = 26,
	Task = 22,
	TaskCompleted = 23,
	Time = 19,
	Update = 28,
```

### Type Changed: MonoTouch.UIKit.UIBezierPath

Added method:

<pre style='color: green'>
	public void GetLineDash (out float[] pattern, out float phase);
</pre>

### Type Changed: MonoTouch.UIKit.UIButton

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual bool RemembersLastFocusedIndexPath { get; set; }
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UICollectionView collectionView);
	public virtual bool ShouldUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewDelegate

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UICollectionView collectionView);
	public virtual bool ShouldUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static bool CanFocusItem (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void DidUpdateFocus (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public static MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (IUICollectionViewDelegate This, UICollectionView collectionView);
	public static bool ShouldUpdateFocus (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout

Added methods:

<pre style='color: green'>
	public override bool CanFocusItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public override void DidUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public override MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UICollectionView collectionView);
	public override bool ShouldUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewSource

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UICollectionView collectionView);
	public virtual bool ShouldUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UIControl

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIControlState

Added value:

```
Focused = 8,
```

### Type Changed: MonoTouch.UIKit.UIDatePicker

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIDocumentMenuViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIDocumentPickerExtensionViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIDocumentPickerViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIEventType

Added value:

```
Presses = 3,
```

### Type Changed: MonoTouch.UIKit.UIGestureRecognizer

Added properties:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSNumber[] AllowedPressTypes { get; set; }
	public virtual MonoTouch.Foundation.NSNumber[] AllowedTouchTypes { get; set; }
	public UIGesturesPress ShouldReceivePress { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public void IgnorePress (UIPress button, UIPressesEvent event);
	public virtual void PressesBegan (MonoTouch.Foundation.NSSet presses, UIPressesEvent evt);
	public virtual void PressesCancelled (MonoTouch.Foundation.NSSet presses, UIPressesEvent evt);
	public virtual void PressesChanged (MonoTouch.Foundation.NSSet presses, UIPressesEvent evt);
	public virtual void PressesEnded (MonoTouch.Foundation.NSSet presses, UIPressesEvent evt);
	public virtual void TouchesEstimatedPropertiesUpdated (MonoTouch.Foundation.NSSet touches);
</pre>

### Type Changed: MonoTouch.UIKit.UIGestureRecognizerDelegate

Added method:

<pre style='color: green'>
	public virtual bool ShouldReceivePress (UIGestureRecognizer gestureRecognizer, UIPress press);
</pre>

### Type Changed: MonoTouch.UIKit.UIGestureRecognizerDelegate_Extensions

Added method:

<pre style='color: green'>
	public static bool ShouldReceivePress (IUIGestureRecognizerDelegate This, UIGestureRecognizer gestureRecognizer, UIPress press);
</pre>

### Type Changed: MonoTouch.UIKit.UIImagePickerController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString LivePhoto { get; }
</pre>

### Type Changed: MonoTouch.UIKit.UIImagePickerMediaPickedEventArgs

Added property:

<pre style='color: green'>
	public MonoTouch.Photos.PHLivePhoto LivePhoto { get; }
</pre>

### Type Changed: MonoTouch.UIKit.UIImageView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIInputView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIInputViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIKitThreadAccessException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.UIKit.UILabel

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UINavigationBar

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UINavigationController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIOffset

Added field:

<pre style='color: green'>
	public static UIOffset Zero;
</pre>

### Type Changed: MonoTouch.UIKit.UIPageControl

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIPageViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIPickerView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIPopoverPresentationController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIPresentationController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual UIView PreferredFocusedView { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidUpdateFocus (UIFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual void SetNeedsFocusUpdate ();
	public virtual bool ShouldUpdateFocus (UIFocusUpdateContext context);
	public virtual void UpdateFocusIfNeeded ();
</pre>

### Type Changed: MonoTouch.UIKit.UIProgressView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIReferenceLibraryViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIResponder

Added methods:

<pre style='color: green'>
	public virtual void PressesBegan (MonoTouch.Foundation.NSSet presses, UIPressesEvent evt);
	public virtual void PressesCancelled (MonoTouch.Foundation.NSSet presses, UIPressesEvent evt);
	public virtual void PressesChanged (MonoTouch.Foundation.NSSet presses, UIPressesEvent evt);
	public virtual void PressesEnded (MonoTouch.Foundation.NSSet presses, UIPressesEvent evt);
	public virtual void TouchesEstimatedPropertiesUpdated (MonoTouch.Foundation.NSSet touches);
</pre>

### Type Changed: MonoTouch.UIKit.UIScreen

Added properties:

<pre style='color: green'>
	public virtual UIView FocusedView { get; }
	public virtual bool SupportsFocus { get; }
</pre>

### Type Changed: MonoTouch.UIKit.UIScrollView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UISearchBar

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UISearchController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual bool ObscuresBackgroundDuringPresentation { get; set; }
</pre>

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UISlider

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UISplitViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIStackView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIStepper

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UISwitch

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UITabBar

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UITabBarController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UITableView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual bool RemembersLastFocusedIndexPath { get; set; }
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewCell

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual UITableViewCellFocusStyle FocusStyle { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual bool ShouldReceivePress (UIGestureRecognizer gestureRecognizer, UIPress press);
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UITableView tableView);
	public virtual bool ShouldUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewDelegate

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UITableView tableView);
	public virtual bool ShouldUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static bool CanFocusRow (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void DidUpdateFocus (IUITableViewDelegate This, UITableView tableView, UITableViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public static MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (IUITableViewDelegate This, UITableView tableView);
	public static bool ShouldUpdateFocus (IUITableViewDelegate This, UITableView tableView, UITableViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewSource

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual MonoTouch.Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UITableView tableView);
	public virtual bool ShouldUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context);
</pre>

### Type Changed: MonoTouch.UIKit.UITextField

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UITextView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIToolbar

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UITouch

Added properties:

<pre style='color: green'>
	public virtual float AltitudeAngle { get; }
	public virtual UITouchProperties EstimatedProperties { get; }
	public virtual UITouchProperties EstimatedPropertiesExpectingUpdates { get; }
	public virtual MonoTouch.Foundation.NSNumber EstimationUpdateIndex { get; }
	public virtual UITouchType Type { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual float GetAzimuthAngle (UIView view);
	public virtual MonoTouch.CoreGraphics.CGVector GetAzimuthUnitVector (UIView view);
	public virtual System.Drawing.PointF GetPreciseLocation (UIView view);
	public virtual System.Drawing.PointF GetPrecisePreviousLocation (UIView view);
</pre>

### Type Changed: MonoTouch.UIKit.UIUserInterfaceIdiom

Added value:

```
TV = 2,
```

### Type Changed: MonoTouch.UIKit.UIVideoEditorController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added properties:

<pre style='color: green'>
	public virtual bool CanBecomeFocused { get; }
	public virtual bool Focused { get; }
	public virtual UIView PreferredFocusedView { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidUpdateFocus (UIFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual void SetNeedsFocusUpdate ();
	public virtual bool ShouldUpdateFocus (UIFocusUpdateContext context);
	public virtual void UpdateFocusIfNeeded ();
</pre>

### Type Changed: MonoTouch.UIKit.UIViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual UIView PreferredFocusedView { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidUpdateFocus (UIFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual void SetNeedsFocusUpdate ();
	public virtual bool ShouldUpdateFocus (UIFocusUpdateContext context);
	public virtual void UpdateFocusIfNeeded ();
</pre>

### Type Changed: MonoTouch.UIKit.UIVisualEffectView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Modified properties:

```
public virtual UIVisualEffect Effect { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIWebView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.UIKit.UIWindow

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### New Type MonoTouch.UIKit.IUIFocusEnvironment

```
public interface IUIFocusEnvironment : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual UIView PreferredFocusedView { get; }
	// methods
	public virtual void DidUpdateFocus (UIFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual void SetNeedsFocusUpdate ();
	public virtual bool ShouldUpdateFocus (UIFocusUpdateContext context);
	public virtual void UpdateFocusIfNeeded ();
}
```

### New Type MonoTouch.UIKit.UICollectionViewFocusUpdateContext

```
public class UICollectionViewFocusUpdateContext : MonoTouch.UIKit.UIFocusUpdateContext, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UICollectionViewFocusUpdateContext ();
	public UICollectionViewFocusUpdateContext (MonoTouch.Foundation.NSCoder coder);
	public UICollectionViewFocusUpdateContext (MonoTouch.Foundation.NSObjectFlag t);
	public UICollectionViewFocusUpdateContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSIndexPath NextFocusedIndexPath { get; }
	public virtual MonoTouch.Foundation.NSIndexPath PreviouslyFocusedIndexPath { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIFocusAnimationCoordinator

```
public class UIFocusAnimationCoordinator : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIFocusAnimationCoordinator ();
	public UIFocusAnimationCoordinator (MonoTouch.Foundation.NSCoder coder);
	public UIFocusAnimationCoordinator (MonoTouch.Foundation.NSObjectFlag t);
	public UIFocusAnimationCoordinator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void AddCoordinatedAnimations (System.Action animations, System.Action completion);
}
```

### New Type MonoTouch.UIKit.UIFocusEnvironment_Extensions

```
public static class UIFocusEnvironment_Extensions {
}
```

### New Type MonoTouch.UIKit.UIFocusGuide

```
public class UIFocusGuide : MonoTouch.UIKit.UILayoutGuide, MonoTouch.Foundation.INSCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIFocusGuide ();
	public UIFocusGuide (MonoTouch.Foundation.NSCoder coder);
	public UIFocusGuide (MonoTouch.Foundation.NSObjectFlag t);
	public UIFocusGuide (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual UIView PreferredFocusedView { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIFocusHeading

```
[Serializable]
[Flags]
public enum UIFocusHeading {
	Down = 2,
	Left = 4,
	Next = 16,
	Previous = 32,
	Right = 8,
	Up = 1,
}
```

### New Type MonoTouch.UIKit.UIFocusUpdateContext

```
public class UIFocusUpdateContext : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIFocusUpdateContext ();
	public UIFocusUpdateContext (MonoTouch.Foundation.NSCoder coder);
	public UIFocusUpdateContext (MonoTouch.Foundation.NSObjectFlag t);
	public UIFocusUpdateContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual UIFocusHeading FocusHeading { get; }
	public virtual UIView NextFocusedView { get; }
	public virtual UIView PreviouslyFocusedView { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIGesturesPress

```
public sealed delegate UIGesturesPress : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UIGesturesPress (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (UIGestureRecognizer gestureRecognizer, UIPress press, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (UIGestureRecognizer gestureRecognizer, UIPress press);
}
```

### New Type MonoTouch.UIKit.UIPress

```
public class UIPress : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIPress ();
	public UIPress (MonoTouch.Foundation.NSCoder coder);
	public UIPress (MonoTouch.Foundation.NSObjectFlag t);
	public UIPress (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual float Force { get; }
	public virtual UIGestureRecognizer[] GestureRecognizers { get; }
	public virtual UIPressPhase Phase { get; }
	public virtual UIResponder Responder { get; }
	public virtual double Timestamp { get; }
	public virtual UIPressType Type { get; }
	public virtual UIWindow Window { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIPressesEvent

```
public class UIPressesEvent : MonoTouch.UIKit.UIEvent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIPressesEvent ();
	public UIPressesEvent (MonoTouch.Foundation.NSCoder coder);
	public UIPressesEvent (MonoTouch.Foundation.NSObjectFlag t);
	public UIPressesEvent (IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSSet AllPresses { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.Foundation.NSSet GetPresses (UIGestureRecognizer gesture);
}
```

### New Type MonoTouch.UIKit.UIPressPhase

```
[Serializable]
public enum UIPressPhase {
	Began = 0,
	Cancelled = 4,
	Changed = 1,
	Ended = 3,
	Stationary = 2,
}
```

### New Type MonoTouch.UIKit.UIPressType

```
[Serializable]
public enum UIPressType {
	DownArrow = 1,
	LeftArrow = 2,
	Menu = 5,
	PlayPause = 6,
	RightArrow = 3,
	Select = 4,
	UpArrow = 0,
}
```

### New Type MonoTouch.UIKit.UIPrintErrorExtensions

```
public static class UIPrintErrorExtensions {
	// methods
	public static MonoTouch.Foundation.NSString GetDomain (UIPrintError self);
}
```

### New Type MonoTouch.UIKit.UISearchContainerViewController

```
public class UISearchContainerViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, IUIAppearanceContainer, IUIContentContainer, IUIFocusEnvironment, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UISearchContainerViewController ();
	public UISearchContainerViewController (MonoTouch.Foundation.NSCoder coder);
	public UISearchContainerViewController (MonoTouch.Foundation.NSObjectFlag t);
	public UISearchContainerViewController (UISearchController searchController);
	public UISearchContainerViewController (IntPtr handle);
	public UISearchContainerViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual UISearchController SearchController { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UITableViewCellFocusStyle

```
[Serializable]
public enum UITableViewCellFocusStyle {
	Custom = 1,
	Default = 0,
}
```

### New Type MonoTouch.UIKit.UITableViewFocusUpdateContext

```
public class UITableViewFocusUpdateContext : MonoTouch.UIKit.UIFocusUpdateContext, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UITableViewFocusUpdateContext ();
	public UITableViewFocusUpdateContext (MonoTouch.Foundation.NSCoder coder);
	public UITableViewFocusUpdateContext (MonoTouch.Foundation.NSObjectFlag t);
	public UITableViewFocusUpdateContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSIndexPath NextFocusedIndexPath { get; }
	public virtual MonoTouch.Foundation.NSIndexPath PreviouslyFocusedIndexPath { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UITouchProperties

```
[Serializable]
[Flags]
public enum UITouchProperties {
	Altitude = 4,
	Azimuth = 2,
	Force = 1,
	Location = 8,
}
```

### New Type MonoTouch.UIKit.UITouchType

```
[Serializable]
public enum UITouchType {
	Direct = 0,
	Indirect = 1,
	Stylus = 2,
}
```

## Namespace MonoTouch.WebKit

### Type Changed: MonoTouch.WebKit.WKWebView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

   


 <hr>

<h1 id='diff/xi/2.1/MonoTouch.Dialog-1.html'>MonoTouch.Dialog-1.dll</h1>

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.AlignmentAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement.TextWithImageCellView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.CaptionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.CheckboxAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.DateAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.DialogViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.EntryAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.GlassButton

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.HtmlAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.MessageSummaryView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.MultilineAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.OnTapAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.PasswordAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.RadioSelectionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.RangeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.RefreshTableHeaderView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.SectionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.SkipAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.TimeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

   


 <hr>

<h1 id='diff/xi/2.1/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

## Namespace Mono.Options

### Type Changed: Mono.Options.OptionException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.NUnit.UI

### Type Changed: MonoTouch.NUnit.UI.TouchViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

## Namespace NUnit

### Type Changed: NUnit.ObjectList

Added interfaces:

<pre style='color: green'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

## Namespace NUnit.Framework

### Type Changed: NUnit.Framework.AssertionException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.CategoryAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.CombinatorialAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.CultureAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DataAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DatapointAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DatapointsAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DatapointSourceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DescriptionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.ExpectedExceptionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.ExplicitAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.IgnoreAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.IgnoreException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.IncludeExcludeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.InconclusiveException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.MaxTimeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.NUnitAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PairwiseAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PlatformAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PostTestAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PreTestAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PropertyAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.RandomAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.RangeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SequentialAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SetCultureAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SetUICultureAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SetUpAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SuccessException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.TearDownAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestCaseAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestCaseSourceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestFixtureAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestFixtureSetUpAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestFixtureTearDownAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TheoryAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TimeoutAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.ValuesAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.ValueSourceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

## Namespace NUnit.Framework.Api

### Type Changed: NUnit.Framework.Api.AttributeDictionary

Added interfaces:

<pre style='color: green'>
	System.Collections.Generic.IReadOnlyDictionary&lt;TKey,TValue&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt;
</pre>

### Type Changed: NUnit.Framework.Api.NodeList

Added interfaces:

<pre style='color: green'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

## Namespace NUnit.Framework.Internal

### Type Changed: NUnit.Framework.Internal.InvalidTestFixtureException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.Internal.NUnitException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace NUnit.Framework.Internal.Commands

### Type Changed: NUnit.Framework.Internal.Commands.CommandDecoratorList

Added interfaces:

<pre style='color: green'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

   


 <hr>

<h1 id='diff/xi/2.1/OpenTK.html'>OpenTK.dll</h1>

## Namespace OpenTK

### Type Changed: OpenTK.AutoGeneratedAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

## Namespace OpenTK.Audio

### Type Changed: OpenTK.Audio.AudioContextException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioDeviceException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioValueException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.GraphicsContextException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Graphics.GraphicsContextMissingException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Graphics.GraphicsModeException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

   


 <hr>

<h1 id='diff/xi/2.1/OpenTK-1.0.html'>OpenTK-1.0.dll</h1>

## Namespace OpenTK

### Type Changed: OpenTK.AutoGeneratedAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

## Namespace OpenTK.Audio

### Type Changed: OpenTK.Audio.AudioContextException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioDeviceException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioValueException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.GraphicsContextException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Graphics.GraphicsContextMissingException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Graphics.GraphicsModeException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIFocusEnvironment
</pre>

   


 <hr>

<h1 id='diff/xi/Xamarin.iOS/MonoTouch.Dialog-1.html'>MonoTouch.Dialog-1.dll</h1>

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.AlignmentAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement.TextWithImageCellView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.CaptionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.CheckboxAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.DateAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.DialogViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.EntryAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.GlassButton

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.HtmlAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.MessageSummaryView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.MultilineAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.OnTapAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.PasswordAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.RadioSelectionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.RangeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.RefreshTableHeaderView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MonoTouch.Dialog.SectionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.SkipAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Dialog.TimeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

   


 <hr>

<h1 id='diff/xi/Xamarin.iOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

## Namespace Mono.Options

### Type Changed: Mono.Options.OptionException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.NUnit.UI

### Type Changed: MonoTouch.NUnit.UI.TouchViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace NUnit

### Type Changed: NUnit.ObjectList

Added interfaces:

<pre style='color: green'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

## Namespace NUnit.Framework

### Type Changed: NUnit.Framework.AssertionException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.CategoryAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.CombinatorialAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.CultureAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DataAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DatapointAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DatapointsAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DatapointSourceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.DescriptionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.ExpectedExceptionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.ExplicitAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.IgnoreAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.IgnoreException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.IncludeExcludeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.InconclusiveException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.MaxTimeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.NUnitAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PairwiseAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PlatformAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PostTestAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PreTestAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.PropertyAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.RandomAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.RangeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SequentialAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SetCultureAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SetUICultureAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SetUpAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.SuccessException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.TearDownAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestCaseAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestCaseSourceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestFixtureAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestFixtureSetUpAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TestFixtureTearDownAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TheoryAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.TimeoutAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.ValuesAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: NUnit.Framework.ValueSourceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

## Namespace NUnit.Framework.Api

### Type Changed: NUnit.Framework.Api.AttributeDictionary

Added interfaces:

<pre style='color: green'>
	System.Collections.Generic.IReadOnlyDictionary&lt;TKey,TValue&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt;
</pre>

### Type Changed: NUnit.Framework.Api.NodeList

Added interfaces:

<pre style='color: green'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

## Namespace NUnit.Framework.Internal

### Type Changed: NUnit.Framework.Internal.InvalidTestFixtureException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: NUnit.Framework.Internal.NUnitException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace NUnit.Framework.Internal.Commands

### Type Changed: NUnit.Framework.Internal.Commands.CommandDecoratorList

Added interfaces:

<pre style='color: green'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

   


 <hr>

<h1 id='diff/xi/Xamarin.iOS/OpenTK-1.0.html'>OpenTK-1.0.dll</h1>

## Namespace OpenTK

### Type Changed: OpenTK.AutoGeneratedAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

## Namespace OpenTK.Audio

### Type Changed: OpenTK.Audio.AudioContextException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioDeviceException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Audio.AudioValueException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.GraphicsContextException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Graphics.GraphicsContextMissingException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: OpenTK.Graphics.GraphicsModeException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

   


 <hr>

<h1 id='diff/xi/Xamarin.iOS/System.Net.Http.html'>System.Net.Http.dll</h1>

## Namespace System.Net.Http

### Type Changed: System.Net.Http.HttpRequestException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

   


 <hr>

<h1 id='diff/xi/Xamarin.iOS/Xamarin.iOS.html'>Xamarin.iOS.dll</h1>

## Namespace AddressBookUI

### Type Changed: AddressBookUI.ABNewPersonViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: AddressBookUI.ABPeoplePickerNavigationController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: AddressBookUI.ABPersonViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: AddressBookUI.ABUnknownPersonViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace AudioToolbox

### Type Changed: AudioToolbox.AudioQueueException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: AudioToolbox.AudioSessionException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace AudioUnit

### Type Changed: AudioUnit.AudioUnitException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace AVKit

### Type Changed: AVKit.AVPlayerViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace Contacts

### Type Changed: Contacts.CNGroup_PredicatesExtension

Obsoleted methods:

```
[Obsolete ("This API is only available on OSX 10.11+")]
	public static Foundation.NSPredicate GetPredicateForSubgroupsInGroup (CNGroup This, string parentGroupIdentifier);
```

## Namespace ContactsUI

### Type Changed: ContactsUI.CNContactPickerViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: ContactsUI.CNContactViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace CoreAudioKit

### Type Changed: CoreAudioKit.AUViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: CoreAudioKit.CABTMidiCentralViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: CoreAudioKit.CABTMidiLocalPeripheralViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: CoreAudioKit.CAInterAppAudioSwitcherView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: CoreAudioKit.CAInterAppAudioTransportView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace CoreBluetooth

### New Type CoreBluetooth.CBATTErrorExtensions

```
public static class CBATTErrorExtensions {
	// methods
	public static Foundation.NSString GetDomain (CBATTError self);
}
```

### New Type CoreBluetooth.CBErrorExtensions

```
public static class CBErrorExtensions {
	// methods
	public static Foundation.NSString GetDomain (CBError self);
}
```

## Namespace CoreFoundation

### Type Changed: CoreFoundation.CFException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: CoreFoundation.CFSocketException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace CoreMidi

### Type Changed: CoreMidi.MidiException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace EventKitUI

### Type Changed: EventKitUI.EKCalendarChooser

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: EventKitUI.EKEventEditViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: EventKitUI.EKEventViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace Foundation

### Type Changed: Foundation.ActionAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.AdviceAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.ConnectAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.ExportAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.FieldAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.LinkerSafeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.ModelAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.ModelNotImplementedException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: Foundation.MonoTouchException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: Foundation.NSAttributedString

Added properties:

<pre style='color: green'>
	public static NSString TextLayoutSectionOrientation { get; }
	public static NSString TextLayoutSectionRange { get; }
	public static NSString TextLayoutSectionsAttribute { get; }
</pre>

### Type Changed: Foundation.NSErrorException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: Foundation.NSUrlSessionConfiguration

Modified properties:

```
public virtual bool ShouldUseExtendedBackgroundIdleMode { get; set; }
```

### Type Changed: Foundation.OutletAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.PreserveAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.ProtocolAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.ProtocolMemberAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.RegisterAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: Foundation.You_Should_Not_Call_base_In_This_Method

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace GameKit

### Type Changed: GameKit.GKAchievementViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: GameKit.GKFriendRequestComposeViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: GameKit.GKGameCenterViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: GameKit.GKLeaderboardViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: GameKit.GKMatchmakerViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: GameKit.GKTurnBasedMatchmakerViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace GameplayKit

### Type Changed: GameplayKit.GKGameModel_Extensions

Added method:

<pre style='color: green'>
	public static void UnapplyGameModelUpdate (IGKGameModel This, IGKGameModelUpdate gameModelUpdate);
</pre>

### Type Changed: GameplayKit.GKMinMaxStrategist

Added interface:

<pre style='color: green'>
	IGKStrategist
</pre>

Added method:

<pre style='color: green'>
	public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();
</pre>

### New Type GameplayKit.GKHybridStrategist

```
public class GKHybridStrategist : Foundation.NSObject, IGKStrategist, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public GKHybridStrategist ();
	protected GKHybridStrategist (Foundation.NSObjectFlag t);
	protected GKHybridStrategist (IntPtr handle);
	// properties
	public virtual uint Budget { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual uint ExplorationParameter { get; set; }
	public virtual IGKGameModel GameModel { get; set; }
	public virtual uint MaxLookAheadDepth { get; set; }
	public virtual IGKRandom RandomSource { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();
}
```

### New Type GameplayKit.GKMonteCarloStrategist

```
public class GKMonteCarloStrategist : Foundation.NSObject, IGKStrategist, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public GKMonteCarloStrategist ();
	protected GKMonteCarloStrategist (Foundation.NSObjectFlag t);
	protected GKMonteCarloStrategist (IntPtr handle);
	// properties
	public virtual uint Budget { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual uint ExplorationParameter { get; set; }
	public virtual IGKGameModel GameModel { get; set; }
	public virtual IGKRandom RandomSource { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();
}
```

### New Type GameplayKit.GKQuadTree

```
public class GKQuadTree : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	protected GKQuadTree (Foundation.NSObjectFlag t);
	protected GKQuadTree (IntPtr handle);
	public GKQuadTree (OpenTK.Vector2 min, OpenTK.Vector2 max, float minCellSize);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual GKQuadTreeNode AddData (Foundation.NSObject data, OpenTK.Vector2 point);
	public virtual GKQuadTreeNode AddData (Foundation.NSObject data, OpenTK.Vector2 quadOrigin, OpenTK.Vector2 quadSize);
	public static GKQuadTree QuadTreeWithMinPosition (OpenTK.Vector2 min, OpenTK.Vector2 max, float minCellSize);
	public virtual Foundation.NSObject[] QueryData (OpenTK.Vector2 point);
	public virtual Foundation.NSObject[] QueryData (OpenTK.Vector2 quadOrigin, OpenTK.Vector2 quadSize);
	public virtual bool RemoveData (Foundation.NSObject data);
	public virtual bool RemoveData (Foundation.NSObject data, GKQuadTreeNode node);
}
```

### New Type GameplayKit.GKQuadTreeNode

```
public class GKQuadTreeNode : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public GKQuadTreeNode ();
	protected GKQuadTreeNode (Foundation.NSObjectFlag t);
	protected GKQuadTreeNode (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
```

### New Type GameplayKit.IGKStrategist

```
public interface IGKStrategist : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IGKGameModel GameModel { get; set; }
	public virtual IGKRandom RandomSource { get; set; }
	// methods
	public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();
}
```

## Namespace GLKit

### Type Changed: GLKit.GLKView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: GLKit.GLKViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace HealthKit

### New Type HealthKit.HKErrorCodeExtensions

```
public static class HKErrorCodeExtensions {
	// methods
	public static Foundation.NSString GetDomain (HKErrorCode self);
}
```

## Namespace iAd

### Type Changed: iAd.ADBannerView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace MapKit

### Type Changed: MapKit.MKAnnotationView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MapKit.MKCircleView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MapKit.MKMapView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MapKit.MKOverlayPathView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MapKit.MKOverlayView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MapKit.MKPinAnnotationView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MapKit.MKPolygonView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MapKit.MKPolylineView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace MediaPlayer

### Type Changed: MediaPlayer.MPMediaPickerController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MediaPlayer.MPMoviePlayerViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MediaPlayer.MPNowPlayingInfoLanguageOption

Added property:

<pre style='color: green'>
	public virtual bool IsAutomaticAudibleLanguageOption { get; }
</pre>

### Type Changed: MediaPlayer.MPRemoteCommandCenter

Added property:

<pre style='color: green'>
	public virtual MPChangePlaybackPositionCommand ChangePlaybackPositionCommand { get; }
</pre>

### Type Changed: MediaPlayer.MPRemoteCommandHandlerStatus

Added value:

```
NoActionableNowPlayingItem = 110,
```

### Type Changed: MediaPlayer.MPVolumeView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### New Type MediaPlayer.MPChangePlaybackPositionCommand

```
public class MPChangePlaybackPositionCommand : MediaPlayer.MPRemoteCommand, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	protected MPChangePlaybackPositionCommand (Foundation.NSObjectFlag t);
	protected MPChangePlaybackPositionCommand (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
```

### New Type MediaPlayer.MPChangePlaybackPositionCommandEvent

```
public class MPChangePlaybackPositionCommandEvent : MediaPlayer.MPRemoteCommandEvent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	protected MPChangePlaybackPositionCommandEvent (Foundation.NSObjectFlag t);
	protected MPChangePlaybackPositionCommandEvent (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual double PositionTime { get; }
}
```

## Namespace MessageUI

### Type Changed: MessageUI.MFMailComposeViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: MessageUI.MFMessageComposeViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace Metal

### Type Changed: Metal.MTLFeatureSet

Added values:

```
OSX_GPUFamily1_v1 = 10000,
	TVOS_GPUFamily1_v1 = 30000,
```

## Namespace MetalKit

### Type Changed: MetalKit.MTKView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace MobileCoreServices

### Type Changed: MobileCoreServices.UTType

Added property:

<pre style='color: green'>
	public static Foundation.NSString LivePhoto { get; }
</pre>

## Namespace MultipeerConnectivity

### Type Changed: MultipeerConnectivity.MCBrowserViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.AdoptsAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.AvailabilityAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.BlockProxyAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.CategoryAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string SdkVersion = "9.0" "9.1";
	public const string Version = "9.0.1" "9.1.0";
```

### Type Changed: ObjCRuntime.DesignatedInitializerAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.iOSAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.LinkWithAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.MacAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.MonoNativeFunctionWrapperAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.MonoPInvokeCallbackAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.NativeAttribute

Added constructor:

<pre style='color: green'>
	public NativeAttribute (string name);
</pre>

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

Added property:

<pre style='color: green'>
	public string NativeName { get; set; }
</pre>

### Type Changed: ObjCRuntime.Platform

Added value:

```
iOS_9_1 = 590080,
```

### Type Changed: ObjCRuntime.ReleaseAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.RuntimeException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: ObjCRuntime.ThreadSafeAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: ObjCRuntime.TransientAttribute

Removed interface:

```
System.Runtime.InteropServices._Attribute
```

### New Type ObjCRuntime.AvailabilityBaseAttribute

```
public abstract class AvailabilityBaseAttribute : System.Attribute {
	// properties
	public PlatformArchitecture Architecture { get; }
	public AvailabilityKind AvailabilityKind { get; }
	public string Message { get; }
	public PlatformName Platform { get; }
	public System.Version Version { get; }
	// methods
	public override string ToString ();
}
```

### New Type ObjCRuntime.AvailabilityKind

```
[Serializable]
public enum AvailabilityKind {
	Deprecated = 1,
	Introduced = 0,
	Obsoleted = 2,
	Unavailable = 3,
}
```

### New Type ObjCRuntime.DeprecatedAttribute

```
public sealed class DeprecatedAttribute : ObjCRuntime.AvailabilityBaseAttribute {
	// constructors
	public DeprecatedAttribute (PlatformName platform, PlatformArchitecture architecture, string message);
	public DeprecatedAttribute (PlatformName platform, int majorVersion, int minorVersion, PlatformArchitecture architecture, string message);
	public DeprecatedAttribute (PlatformName platform, int majorVersion, int minorVersion, int subminorVersion, PlatformArchitecture architecture, string message);
}
```

### New Type ObjCRuntime.IntroducedAttribute

```
public sealed class IntroducedAttribute : ObjCRuntime.AvailabilityBaseAttribute {
	// constructors
	public IntroducedAttribute (PlatformName platform, PlatformArchitecture architecture, string message);
	public IntroducedAttribute (PlatformName platform, int majorVersion, int minorVersion, PlatformArchitecture architecture, string message);
	public IntroducedAttribute (PlatformName platform, int majorVersion, int minorVersion, int subminorVersion, PlatformArchitecture architecture, string message);
}
```

### New Type ObjCRuntime.ObsoletedAttribute

```
public sealed class ObsoletedAttribute : ObjCRuntime.AvailabilityBaseAttribute {
	// constructors
	public ObsoletedAttribute (PlatformName platform, PlatformArchitecture architecture, string message);
	public ObsoletedAttribute (PlatformName platform, int majorVersion, int minorVersion, PlatformArchitecture architecture, string message);
	public ObsoletedAttribute (PlatformName platform, int majorVersion, int minorVersion, int subminorVersion, PlatformArchitecture architecture, string message);
}
```

### New Type ObjCRuntime.PlatformArchitecture

```
[Serializable]
[Flags]
public enum PlatformArchitecture {
	All = 255,
	Arch32 = 1,
	Arch64 = 2,
	None = 0,
}
```

### New Type ObjCRuntime.PlatformName

```
[Serializable]
public enum PlatformName {
	iOS = 2,
	MacOSX = 1,
	None = 0,
	TvOS = 4,
	WatchOS = 3,
}
```

### New Type ObjCRuntime.UnavailableAttribute

```
public sealed class UnavailableAttribute : ObjCRuntime.AvailabilityBaseAttribute {
	// constructors
	public UnavailableAttribute (PlatformName platform, PlatformArchitecture architecture, string message);
}
```

## Namespace PassKit

### Type Changed: PassKit.PKAddPassButton

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: PassKit.PKAddPassesViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: PassKit.PKAddPaymentPassViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: PassKit.PKPaymentAuthorizationViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: PassKit.PKPaymentButton

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace Photos

### Type Changed: Photos.PHAssetMediaSubtype

Added value:

```
PhotoLive = 8,
```

### Type Changed: Photos.PHAssetResource

Added method:

<pre style='color: green'>
	public static PHAssetResource[] GetAssetResources (PHLivePhoto livePhoto);
</pre>

### Type Changed: Photos.PHAssetResourceType

Added value:

```
PairedVideo = 9,
```

### Type Changed: Photos.PHImageManager

Added method:

<pre style='color: green'>
	public virtual int RequestLivePhoto (PHAsset asset, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHLivePhotoRequestOptions options, PHImageManagerRequestLivePhoto resultHandler);
</pre>

### New Type Photos.PHImageManagerRequestLivePhoto

```
public sealed delegate PHImageManagerRequestLivePhoto : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHImageManagerRequestLivePhoto (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (PHLivePhoto livePhoto, Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (PHLivePhoto livePhoto, Foundation.NSDictionary info);
}
```

### New Type Photos.PHLivePhoto

```
public class PHLivePhoto : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public PHLivePhoto ();
	public PHLivePhoto (Foundation.NSCoder coder);
	protected PHLivePhoto (Foundation.NSObjectFlag t);
	protected PHLivePhoto (IntPtr handle);
	// fields
	public static const int RequestIdInvalid;
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGSize Size { get; }
	// methods
	public static void CancelLivePhotoRequest (int requestID);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static int RequestLivePhoto (Foundation.NSUrl[] fileUrls, UIKit.UIImage image, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, System.Action<PHLivePhoto,Foundation.NSDictionary> resultHandler);
}
```

### New Type Photos.PHLivePhotoInfo

```
public static class PHLivePhotoInfo {
	// properties
	public static Foundation.NSString CancelledKey { get; }
	public static Foundation.NSString ErrorKey { get; }
	public static Foundation.NSString IsDegradedKey { get; }
}
```

### New Type Photos.PHLivePhotoRequestOptions

```
public class PHLivePhotoRequestOptions : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public PHLivePhotoRequestOptions ();
	protected PHLivePhotoRequestOptions (Foundation.NSObjectFlag t);
	protected PHLivePhotoRequestOptions (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }
	public virtual bool NetworkAccessAllowed { get; set; }
	public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
```

## Namespace PhotosUI

### New Type PhotosUI.IPHLivePhotoViewDelegate

```
public interface IPHLivePhotoViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type PhotosUI.PHLivePhotoBadgeOptions

```
[Serializable]
[Flags]
public enum PHLivePhotoBadgeOptions {
	LiveOff = 2,
	None = 0,
	OverContent = 1,
}
```

### New Type PhotosUI.PHLivePhotoView

```
public class PHLivePhotoView : UIKit.UIView, System.Collections.IEnumerable, Foundation.INSCoding, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public PHLivePhotoView ();
	public PHLivePhotoView (CoreGraphics.CGRect frame);
	public PHLivePhotoView (Foundation.NSCoder coder);
	protected PHLivePhotoView (Foundation.NSObjectFlag t);
	protected PHLivePhotoView (IntPtr handle);
	// properties
	public static PHLivePhotoView.PHLivePhotoViewAppearance Appearance { get; }
	public override IntPtr ClassHandle { get; }
	public IPHLivePhotoViewDelegate Delegate { get; set; }
	public virtual Photos.PHLivePhoto LivePhoto { get; set; }
	public virtual bool Muted { get; set; }
	public virtual UIKit.UIGestureRecognizer PlaybackGestureRecognizer { get; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public static PHLivePhotoView.PHLivePhotoViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance<T> ();
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
	public static UIKit.UIImage GetLivePhotoBadgeImage (PHLivePhotoBadgeOptions badgeOptions);
	public virtual void StartPlayback (PHLivePhotoViewPlaybackStyle playbackStyle);
	public virtual void StopPlayback ();

	// inner types
	public class PHLivePhotoViewAppearance : UIKit.UIView+UIViewAppearance, UIKit.IUIAppearance, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
		// constructors
		protected PHLivePhotoView (IntPtr handle);
	}
}
```

### New Type PhotosUI.PHLivePhotoViewDelegate

```
public class PHLivePhotoViewDelegate : Foundation.NSObject, IPHLivePhotoViewDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public PHLivePhotoViewDelegate ();
	protected PHLivePhotoViewDelegate (Foundation.NSObjectFlag t);
	protected PHLivePhotoViewDelegate (IntPtr handle);
	// methods
	public virtual void DidEndPlayback (PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);
	public virtual void WillBeginPlayback (PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);
}
```

### New Type PhotosUI.PHLivePhotoViewDelegate_Extensions

```
public static class PHLivePhotoViewDelegate_Extensions {
	// methods
	public static void DidEndPlayback (IPHLivePhotoViewDelegate This, PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);
	public static void WillBeginPlayback (IPHLivePhotoViewDelegate This, PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);
}
```

### New Type PhotosUI.PHLivePhotoViewPlaybackStyle

```
[Serializable]
public enum PHLivePhotoViewPlaybackStyle {
	Full = 1,
	Hint = 2,
	Undefined = 0,
}
```

## Namespace QuickLook

### Type Changed: QuickLook.QLPreviewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace ReplayKit

### Type Changed: ReplayKit.RPPreviewViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace SafariServices

### Type Changed: SafariServices.SFSafariViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace SceneKit

### Type Changed: SceneKit.SCNView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace Security

### Type Changed: Security.SecurityException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace Social

### Type Changed: Social.SLComposeServiceViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

### Type Changed: Social.SLComposeViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace SpriteKit

### Type Changed: SpriteKit.SKView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace StoreKit

### Type Changed: StoreKit.SKStoreProductViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace SystemConfiguration

### Type Changed: SystemConfiguration.SystemConfigurationException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace Twitter

### Type Changed: Twitter.TWTweetComposeViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

## Namespace UIKit

### Type Changed: UIKit.UIActionSheet

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIActivityIndicatorView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIActivityViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIAlertController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIAlertView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIApplicationShortcutIconType

Added values:

```
Alarm = 24,
	Audio = 27,
	Bookmark = 25,
	CapturePhoto = 20,
	CaptureVideo = 21,
	Cloud = 13,
	Confirmation = 15,
	Contact = 8,
	Date = 18,
	Favorite = 11,
	Home = 9,
	Invitation = 14,
	Love = 12,
	Mail = 16,
	MarkLocation = 10,
	Message = 17,
	Prohibit = 7,
	Shuffle = 26,
	Task = 22,
	TaskCompleted = 23,
	Time = 19,
	Update = 28,
```

### Type Changed: UIKit.UIBezierPath

Added method:

<pre style='color: green'>
	public void GetLineDash (out nfloat[] pattern, out nfloat phase);
</pre>

### Type Changed: UIKit.UIButton

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UICollectionReusableView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UICollectionView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual bool RemembersLastFocusedIndexPath { get; set; }
</pre>

### Type Changed: UIKit.UICollectionViewCell

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UICollectionViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UICollectionView collectionView);
	public virtual bool ShouldUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: UIKit.UICollectionViewDelegate

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UICollectionView collectionView);
	public virtual bool ShouldUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: UIKit.UICollectionViewDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static bool CanFocusItem (IUICollectionViewDelegate This, UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public static void DidUpdateFocus (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public static Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (IUICollectionViewDelegate This, UICollectionView collectionView);
	public static bool ShouldUpdateFocus (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: UIKit.UICollectionViewSource

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UICollectionView collectionView);
	public virtual bool ShouldUpdateFocus (UICollectionView collectionView, UICollectionViewFocusUpdateContext context);
</pre>

### Type Changed: UIKit.UIControl

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIControlState

Added value:

```
Focused = 8,
```

### Type Changed: UIKit.UIDatePicker

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIDocumentMenuViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIDocumentPickerExtensionViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIDocumentPickerViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIEventType

Added value:

```
Presses = 3,
```

### Type Changed: UIKit.UIGestureRecognizer

Added properties:

<pre style='color: green'>
	public virtual Foundation.NSNumber[] AllowedPressTypes { get; set; }
	public virtual Foundation.NSNumber[] AllowedTouchTypes { get; set; }
	public UIGesturesPress ShouldReceivePress { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public void IgnorePress (UIPress button, UIPressesEvent event);
	public virtual void PressesBegan (Foundation.NSSet&lt;UIPress&gt; presses, UIPressesEvent evt);
	public virtual void PressesCancelled (Foundation.NSSet&lt;UIPress&gt; presses, UIPressesEvent evt);
	public virtual void PressesChanged (Foundation.NSSet&lt;UIPress&gt; presses, UIPressesEvent evt);
	public virtual void PressesEnded (Foundation.NSSet&lt;UIPress&gt; presses, UIPressesEvent evt);
	public virtual void TouchesEstimatedPropertiesUpdated (Foundation.NSSet touches);
</pre>

### Type Changed: UIKit.UIGestureRecognizerDelegate

Added method:

<pre style='color: green'>
	public virtual bool ShouldReceivePress (UIGestureRecognizer gestureRecognizer, UIPress press);
</pre>

### Type Changed: UIKit.UIGestureRecognizerDelegate_Extensions

Added method:

<pre style='color: green'>
	public static bool ShouldReceivePress (IUIGestureRecognizerDelegate This, UIGestureRecognizer gestureRecognizer, UIPress press);
</pre>

### Type Changed: UIKit.UIImagePickerController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public static Foundation.NSString LivePhoto { get; }
</pre>

### Type Changed: UIKit.UIImagePickerMediaPickedEventArgs

Added property:

<pre style='color: green'>
	public Photos.PHLivePhoto LivePhoto { get; }
</pre>

### Type Changed: UIKit.UIImageView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIInputView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIInputViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIKitThreadAccessException

Removed interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: UIKit.UILabel

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UINavigationBar

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UINavigationController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIOffset

Added field:

<pre style='color: green'>
	public static UIOffset Zero;
</pre>

### Type Changed: UIKit.UIPageControl

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIPageViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIPickerView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIPopoverBackgroundView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIPopoverPresentationController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIPresentationController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual UIView PreferredFocusedView { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidUpdateFocus (UIFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual void SetNeedsFocusUpdate ();
	public virtual bool ShouldUpdateFocus (UIFocusUpdateContext context);
	public virtual void UpdateFocusIfNeeded ();
</pre>

### Type Changed: UIKit.UIProgressView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIReferenceLibraryViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIRefreshControl

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIResponder

Added methods:

<pre style='color: green'>
	public virtual void PressesBegan (Foundation.NSSet&lt;UIPress&gt; presses, UIPressesEvent evt);
	public virtual void PressesCancelled (Foundation.NSSet&lt;UIPress&gt; presses, UIPressesEvent evt);
	public virtual void PressesChanged (Foundation.NSSet&lt;UIPress&gt; presses, UIPressesEvent evt);
	public virtual void PressesEnded (Foundation.NSSet&lt;UIPress&gt; presses, UIPressesEvent evt);
	public virtual void TouchesEstimatedPropertiesUpdated (Foundation.NSSet touches);
</pre>

### Type Changed: UIKit.UIScreen

Added properties:

<pre style='color: green'>
	public virtual UIView FocusedView { get; }
	public virtual bool SupportsFocus { get; }
</pre>

### Type Changed: UIKit.UIScrollView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UISearchBar

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UISearchController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual bool ObscuresBackgroundDuringPresentation { get; set; }
</pre>

### Type Changed: UIKit.UISegmentedControl

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UISlider

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UISplitViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIStackView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIStepper

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UISwitch

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UITabBar

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UITabBarController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UITableView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual bool RemembersLastFocusedIndexPath { get; set; }
</pre>

### Type Changed: UIKit.UITableViewCell

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual UITableViewCellFocusStyle FocusStyle { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual bool ShouldReceivePress (UIGestureRecognizer gestureRecognizer, UIPress press);
</pre>

### Type Changed: UIKit.UITableViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusRow (UITableView tableView, Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UITableView tableView);
	public virtual bool ShouldUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context);
</pre>

### Type Changed: UIKit.UITableViewDelegate

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusRow (UITableView tableView, Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UITableView tableView);
	public virtual bool ShouldUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context);
</pre>

### Type Changed: UIKit.UITableViewDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static bool CanFocusRow (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);
	public static void DidUpdateFocus (IUITableViewDelegate This, UITableView tableView, UITableViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public static Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (IUITableViewDelegate This, UITableView tableView);
	public static bool ShouldUpdateFocus (IUITableViewDelegate This, UITableView tableView, UITableViewFocusUpdateContext context);
</pre>

### Type Changed: UIKit.UITableViewHeaderFooterView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UITableViewSource

Added methods:

<pre style='color: green'>
	public virtual bool CanFocusRow (UITableView tableView, Foundation.NSIndexPath indexPath);
	public virtual void DidUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual Foundation.NSIndexPath GetIndexPathForPreferredFocusedView (UITableView tableView);
	public virtual bool ShouldUpdateFocus (UITableView tableView, UITableViewFocusUpdateContext context);
</pre>

### Type Changed: UIKit.UITextField

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UITextView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIToolbar

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UITouch

Added properties:

<pre style='color: green'>
	public virtual nfloat AltitudeAngle { get; }
	public virtual UITouchProperties EstimatedProperties { get; }
	public virtual UITouchProperties EstimatedPropertiesExpectingUpdates { get; }
	public virtual Foundation.NSNumber EstimationUpdateIndex { get; }
	public virtual UITouchType Type { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual nfloat GetAzimuthAngle (UIView view);
	public virtual CoreGraphics.CGVector GetAzimuthUnitVector (UIView view);
	public virtual CoreGraphics.CGPoint GetPreciseLocation (UIView view);
	public virtual CoreGraphics.CGPoint GetPrecisePreviousLocation (UIView view);
</pre>

### Type Changed: UIKit.UIUserInterfaceIdiom

Added value:

```
TV = 2,
```

### Type Changed: UIKit.UIVideoEditorController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added properties:

<pre style='color: green'>
	public virtual bool CanBecomeFocused { get; }
	public virtual bool Focused { get; }
	public virtual UIView PreferredFocusedView { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidUpdateFocus (UIFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual void SetNeedsFocusUpdate ();
	public virtual bool ShouldUpdateFocus (UIFocusUpdateContext context);
	public virtual void UpdateFocusIfNeeded ();
</pre>

### Type Changed: UIKit.UIViewController

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Added property:

<pre style='color: green'>
	public virtual UIView PreferredFocusedView { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidUpdateFocus (UIFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual void SetNeedsFocusUpdate ();
	public virtual bool ShouldUpdateFocus (UIFocusUpdateContext context);
	public virtual void UpdateFocusIfNeeded ();
</pre>

### Type Changed: UIKit.UIVisualEffectView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

Modified properties:

```
public virtual UIVisualEffect Effect { get; set; }
```

### Type Changed: UIKit.UIWebView

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### Type Changed: UIKit.UIWindow

Added interface:

<pre style='color: green'>
	IUIFocusEnvironment
</pre>

### New Type UIKit.IUIFocusEnvironment

```
public interface IUIFocusEnvironment : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual UIView PreferredFocusedView { get; }
	// methods
	public virtual void DidUpdateFocus (UIFocusUpdateContext context, UIFocusAnimationCoordinator coordinator);
	public virtual void SetNeedsFocusUpdate ();
	public virtual bool ShouldUpdateFocus (UIFocusUpdateContext context);
	public virtual void UpdateFocusIfNeeded ();
}
```

### New Type UIKit.UICollectionViewFocusUpdateContext

```
public class UICollectionViewFocusUpdateContext : UIKit.UIFocusUpdateContext, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public UICollectionViewFocusUpdateContext ();
	protected UICollectionViewFocusUpdateContext (Foundation.NSObjectFlag t);
	protected UICollectionViewFocusUpdateContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSIndexPath NextFocusedIndexPath { get; }
	public virtual Foundation.NSIndexPath PreviouslyFocusedIndexPath { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type UIKit.UIFocusAnimationCoordinator

```
public class UIFocusAnimationCoordinator : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public UIFocusAnimationCoordinator ();
	protected UIFocusAnimationCoordinator (Foundation.NSObjectFlag t);
	protected UIFocusAnimationCoordinator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void AddCoordinatedAnimations (System.Action animations, System.Action completion);
}
```

### New Type UIKit.UIFocusGuide

```
public class UIFocusGuide : UIKit.UILayoutGuide, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public UIFocusGuide ();
	public UIFocusGuide (Foundation.NSCoder coder);
	protected UIFocusGuide (Foundation.NSObjectFlag t);
	protected UIFocusGuide (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual UIView PreferredFocusedView { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type UIKit.UIFocusHeading

```
[Serializable]
[Flags]
public enum UIFocusHeading {
	Down = 2,
	Left = 4,
	Next = 16,
	Previous = 32,
	Right = 8,
	Up = 1,
}
```

### New Type UIKit.UIFocusUpdateContext

```
public class UIFocusUpdateContext : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public UIFocusUpdateContext ();
	protected UIFocusUpdateContext (Foundation.NSObjectFlag t);
	protected UIFocusUpdateContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual UIFocusHeading FocusHeading { get; }
	public virtual UIView NextFocusedView { get; }
	public virtual UIView PreviouslyFocusedView { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type UIKit.UIGesturesPress

```
public sealed delegate UIGesturesPress : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UIGesturesPress (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (UIGestureRecognizer gestureRecognizer, UIPress press, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (UIGestureRecognizer gestureRecognizer, UIPress press);
}
```

### New Type UIKit.UIPress

```
public class UIPress : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public UIPress ();
	protected UIPress (Foundation.NSObjectFlag t);
	protected UIPress (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nfloat Force { get; }
	public virtual UIGestureRecognizer[] GestureRecognizers { get; }
	public virtual UIPressPhase Phase { get; }
	public virtual UIResponder Responder { get; }
	public virtual double Timestamp { get; }
	public virtual UIPressType Type { get; }
	public virtual UIWindow Window { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type UIKit.UIPressesEvent

```
public class UIPressesEvent : UIKit.UIEvent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public UIPressesEvent ();
	protected UIPressesEvent (Foundation.NSObjectFlag t);
	protected UIPressesEvent (IntPtr handle);
	// properties
	public virtual Foundation.NSSet<UIPress> AllPresses { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual Foundation.NSSet<UIPress> GetPresses (UIGestureRecognizer gesture);
}
```

### New Type UIKit.UIPressPhase

```
[Serializable]
public enum UIPressPhase {
	Began = 0,
	Cancelled = 4,
	Changed = 1,
	Ended = 3,
	Stationary = 2,
}
```

### New Type UIKit.UIPressType

```
[Serializable]
public enum UIPressType {
	DownArrow = 1,
	LeftArrow = 2,
	Menu = 5,
	PlayPause = 6,
	RightArrow = 3,
	Select = 4,
	UpArrow = 0,
}
```

### New Type UIKit.UIPrintErrorExtensions

```
public static class UIPrintErrorExtensions {
	// methods
	public static Foundation.NSString GetDomain (UIPrintError self);
}
```

### New Type UIKit.UISearchContainerViewController

```
public class UISearchContainerViewController : UIKit.UIViewController, System.Collections.IEnumerable, Foundation.INSCoding, IUIAppearanceContainer, IUIContentContainer, IUIFocusEnvironment, IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public UISearchContainerViewController ();
	public UISearchContainerViewController (Foundation.NSCoder coder);
	protected UISearchContainerViewController (Foundation.NSObjectFlag t);
	protected UISearchContainerViewController (IntPtr handle);
	public UISearchContainerViewController (UISearchController searchController);
	public UISearchContainerViewController (string nibName, Foundation.NSBundle bundle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual UISearchController SearchController { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type UIKit.UITableViewCellFocusStyle

```
[Serializable]
public enum UITableViewCellFocusStyle {
	Custom = 1,
	Default = 0,
}
```

### New Type UIKit.UITableViewFocusUpdateContext

```
public class UITableViewFocusUpdateContext : UIKit.UIFocusUpdateContext, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public UITableViewFocusUpdateContext ();
	protected UITableViewFocusUpdateContext (Foundation.NSObjectFlag t);
	protected UITableViewFocusUpdateContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSIndexPath NextFocusedIndexPath { get; }
	public virtual Foundation.NSIndexPath PreviouslyFocusedIndexPath { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type UIKit.UITouchProperties

```
[Serializable]
[Flags]
public enum UITouchProperties {
	Altitude = 4,
	Azimuth = 2,
	Force = 1,
	Location = 8,
}
```

### New Type UIKit.UITouchType

```
[Serializable]
public enum UITouchType {
	Direct = 0,
	Indirect = 1,
	Stylus = 2,
}
```

## Namespace WebKit

### Type Changed: WebKit.WKWebView

Added interface:

<pre style='color: green'>
	UIKit.IUIFocusEnvironment
</pre>

   


 <hr>
