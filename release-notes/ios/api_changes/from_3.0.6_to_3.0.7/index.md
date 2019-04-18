---
id: 10AF8FA4-44A8-4430-8274-3B069C4215CE
title: "From 3.0.6 to 3.0.7"
---

<html><head><title>Comparison between mt-306 and mt-307</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "3.0.6";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.0.7";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h2>Type Changed: MonoTouch.CoreAnimation.CABasicAnimation</h2>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSNumber By {
 	public virtual MonoTouch.Foundation.NSNumber From {
 	public virtual MonoTouch.Foundation.NSNumber To {
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSValue By {
 	public virtual MonoTouch.Foundation.NSValue From {
 	public virtual MonoTouch.Foundation.NSValue To {
</pre>
<h2>Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation</h2>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSNumber[] Values {
</pre>
<p>Added:</p><pre>
 	public static CAPropertyAnimation FromKeyPath (string path);
 	
 	public virtual MonoTouch.Foundation.NSValue[] Values {
</pre>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h1>Namespace: MonoTouch.CoreMedia</h1>
<h1>Namespace: MonoTouch.CoreMotion</h1>
<h2>New Type: MonoTouch.CoreMotion.CMAcceleration</h2>
<pre>
public struct CMAcceleration {
	
	public CMAcceleration (double x, double y, double z);
	
	public double X;
	public double Y;
	public double Z;
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMAccelerometerData</h2>
<pre>
public class CMAccelerometerData : CMLogItem {
	
	public CMAccelerometerData ();
	public CMAccelerometerData (MonoTouch.Foundation.NSCoder coder);
	public CMAccelerometerData (MonoTouch.Foundation.NSObjectFlag t);
	public CMAccelerometerData (IntPtr handle);
	
	public virtual CMAcceleration Acceleration {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMAccelerometerHandler</h2>
<pre>
[Serializable]
public delegate void CMAccelerometerHandler (CMAccelerometerData data, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMAttitude</h2>
<pre>
public class CMAttitude : MonoTouch.Foundation.NSObject {
	
	public CMAttitude ();
	public CMAttitude (MonoTouch.Foundation.NSCoder coder);
	public CMAttitude (MonoTouch.Foundation.NSObjectFlag t);
	public CMAttitude (IntPtr handle);
	
	public virtual void MultiplyByInverseOfAttitude (CMAttitude attitude);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Pitch {
		get;
	}
	public virtual CMQuaternion Quaternion {
		get;
	}
	public virtual double Roll {
		get;
	}
	public virtual CMRotationMatrix RotationMatrix {
		get;
	}
	public virtual double Yaw {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMDeviceMotion</h2>
<pre>
public class CMDeviceMotion : CMLogItem {
	
	public CMDeviceMotion ();
	public CMDeviceMotion (MonoTouch.Foundation.NSCoder coder);
	public CMDeviceMotion (MonoTouch.Foundation.NSObjectFlag t);
	public CMDeviceMotion (IntPtr handle);
	
	public virtual CMAttitude Attitude {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual CMAcceleration Gravity {
		get;
	}
	public virtual CMRotationRate RotationRate {
		get;
	}
	public virtual CMAcceleration UserAcceleration {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMDeviceMotionHandler</h2>
<pre>
[Serializable]
public delegate void CMDeviceMotionHandler (CMDeviceMotion motion, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMError</h2>
<pre>
[Serializable]
public enum CMError {
	Null
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMGyroData</h2>
<pre>
public class CMGyroData : CMLogItem {
	
	public CMGyroData ();
	public CMGyroData (MonoTouch.Foundation.NSCoder coder);
	public CMGyroData (MonoTouch.Foundation.NSObjectFlag t);
	public CMGyroData (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual CMRotationRate RotationRate {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMGyroHandler</h2>
<pre>
[Serializable]
public delegate void CMGyroHandler (CMGyroData gyroData, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMLogItem</h2>
<pre>
public class CMLogItem : MonoTouch.Foundation.NSObject {
	
	public CMLogItem ();
	public CMLogItem (MonoTouch.Foundation.NSCoder coder);
	public CMLogItem (MonoTouch.Foundation.NSObjectFlag t);
	public CMLogItem (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Timestamp {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMMotionManager</h2>
<pre>
public class CMMotionManager : MonoTouch.Foundation.NSObject {
	
	public CMMotionManager ();
	public CMMotionManager (MonoTouch.Foundation.NSCoder coder);
	public CMMotionManager (MonoTouch.Foundation.NSObjectFlag t);
	public CMMotionManager (IntPtr handle);
	
	public virtual void StartAccelerometerUpdates ();
	public virtual void StartAccelerometerUpdates (MonoTouch.Foundation.NSOperationQueue queue, CMAccelerometerHandler handler);
	public virtual void StartDeviceMotionUpdates ();
	public virtual void StartDeviceMotionUpdates (MonoTouch.Foundation.NSOperationQueue toQueue, CMDeviceMotionHandler handler);
	public virtual void StartGyroUpdates ();
	public virtual void StartGyroUpdates (MonoTouch.Foundation.NSOperationQueue toQueue, CMGyroHandler handler);
	public virtual void StopAccelerometerUpdates ();
	public virtual void StopDeviceMotionUpdates ();
	public virtual void StopGyroUpdates ();
	
	public virtual bool AccelerometerActive {
		get;
	}
	public virtual bool AccelerometerAvailable {
		get;
	}
	public virtual CMAccelerometerData AccelerometerData {
		get;
	}
	public virtual double AccelerometerUpdateInterval {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual CMDeviceMotion DeviceMotion {
		get;
	}
	public virtual bool DeviceMotionActive {
		get;
	}
	public virtual bool DeviceMotionAvailable {
		get;
	}
	public virtual double DeviceMotionUpdateInterval {
		get;
		set;
	}
	public virtual bool GyroActive {
		get;
	}
	public virtual bool GyroAvailable {
		get;
	}
	public virtual CMGyroData GyroData {
		get;
	}
	public virtual double GyroUpdateInterval {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMQuaternion</h2>
<pre>
public struct CMQuaternion {
	
	public CMQuaternion (double x, double y, double z, double w);
	
	public double x;
	public double y;
	public double z;
	public double w;
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMRotationMatrix</h2>
<pre>
public struct CMRotationMatrix {
	
	public double m11;
	public double m12;
	public double m13;
	public double m21;
	public double m22;
	public double m23;
	public double m31;
	public double m32;
	public double m33;
}
</pre>
<h2>New Type: MonoTouch.CoreMotion.CMRotationRate</h2>
<pre>
public struct CMRotationRate {
	
	public CMRotationRate (double x, double y, double z);
	
	public double x;
	public double y;
	public double z;
}
</pre>
<h1>Namespace: MonoTouch.CoreTelephony</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.EventKit</h1>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>Type Changed: MonoTouch.Foundation.NSNotificationCoalescing</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSNotificationCoalescing
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum NSNotificationCoalescing {
 	NoCoalescing,
 	CoalescingOnName,
 	CoalescingOnSender
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSNotificationQueue</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSNotificationQueue
</pre>
<p>Added:</p><pre>
 public class NSNotificationQueue : NSObject {
 	
 	public NSNotificationQueue ();
 	public NSNotificationQueue (NSCoder coder);
 	public NSNotificationQueue (NSObjectFlag t);
 	public NSNotificationQueue (IntPtr handle);
 	public NSNotificationQueue (NSNotificationCenter notificationCenter);
 	
 	public virtual void DequeueNotificationsMatchingcoalesceMask (NSNotification notification, NSNotificationCoalescing coalesceMask);
 	public virtual void EnqueueNotification (NSNotification notification, NSPostingStyle postingStyle);
 	public virtual void EnqueueNotification (NSNotification notification, NSPostingStyle postingStyle, NSNotificationCoalescing coalesceMask, string [] modes);
 	
 	public static NSObject DefaultQueue {
 		get;
 	}
 	public override IntPtr ClassHandle {
 		get;
 	}
 }
</pre>
<h2>New Type: MonoTouch.Foundation.NSPostingStyle</h2>
<pre>
[Serializable]
public enum NSPostingStyle {
	PostWhenIdle,
	PostASAP,
	Now
}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSString</h2>
<p>Removed:</p><pre>
 	public string Format (MonoTouch.UIKit.UIFont withFont, float width, MonoTouch.UIKit.UILineBreakMode breakMode);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSTimer</h2>
<p>Added:</p><pre>
 	public static NSTimer CreateRepeatingScheduledTimer (double seconds, NSAction action);
 	public static NSTimer CreateRepeatingTimer (double seconds, NSAction action);
 	public static NSTimer CreateScheduledTimer (double seconds, NSAction action);
 	public static NSTimer CreateTimer (double seconds, NSAction action);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSValue</h2>
<p>Added:</p><pre>
 	public static NSValue FromCATransform3D (MonoTouch.CoreAnimation.CATransform3D transform);
 	public virtual MonoTouch.CoreAnimation.CATransform3D CATransform3DValue {
 		get;
 	}
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h2>Type Changed: MonoTouch.GameKit.GKSessionDelegate</h2>
<p>Removed:</p><pre>
 	public virtual void PeerConnectionFailed (GKSession session, MonoTouch.Foundation.NSError error);
</pre>
<p>Added:</p><pre>
 	public virtual void PeerConnectionFailed (GKSession session, string peerID, MonoTouch.Foundation.NSError error);
</pre>
<h1>Namespace: MonoTouch.MapKit</h1>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h2>Type Changed: MonoTouch.ObjCRuntime.Messaging</h2>
<p>Removed:</p><pre>
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, int arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, int arg3);
</pre>
<p>Added:</p><pre>
 	public static void CMAcceleration_objc_msgSend_stret (out MonoTouch.CoreMotion.CMAcceleration retval, IntPtr receiver, IntPtr selector);
 	public static void CMAcceleration_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMAcceleration retval, IntPtr receiver, IntPtr selector);
 	public static void CMQuaternion_objc_msgSend_stret (out MonoTouch.CoreMotion.CMQuaternion retval, IntPtr receiver, IntPtr selector);
 	public static void CMQuaternion_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMQuaternion retval, IntPtr receiver, IntPtr selector);
 	public static void CMRotationMatrix_objc_msgSend_stret (out MonoTouch.CoreMotion.CMRotationMatrix retval, IntPtr receiver, IntPtr selector);
 	public static void CMRotationMatrix_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMRotationMatrix retval, IntPtr receiver, IntPtr selector);
 	public static void CMRotationRate_objc_msgSend_stret (out MonoTouch.CoreMotion.CMRotationRate retval, IntPtr receiver, IntPtr selector);
 	public static void CMRotationRate_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMRotationRate retval, IntPtr receiver, IntPtr selector);
 	public static IntPtr IntPtr_objc_msgSend_CATransform3D (IntPtr receiver, IntPtr selector, MonoTouch.CoreAnimation.CATransform3D arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_CATransform3D (IntPtr receiver, IntPtr selector, MonoTouch.CoreAnimation.CATransform3D arg1);
 	public static void void_objc_msgSend_IntPtr_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_IntPtr_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3, IntPtr arg4);
</pre>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h2>Type Changed: MonoTouch.UIKit.UIButton</h2>
<p>Removed:</p><pre>
 	public virtual UIEdgeInsets imageEdgeInsets {
</pre>
<p>Added:</p><pre>
 	public virtual UIEdgeInsets ImageEdgeInsets {
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIImagePickerController</h2>
<p>Added:</p><pre>
 	public static bool IsCameraDeviceAvailable (UIImagePickerControllerCameraDevice cameraDevice);
 	public static bool IsFlashAvailableForCameraDevice (UIImagePickerControllerCameraDevice cameraDevice);
 	public virtual MonoTouch.Foundation.NSNumber[] AvailableCaptureModesForCameraDevice (UIImagePickerControllerCameraDevice cameraDevice);
 	public virtual UIImagePickerControllerCameraDevice CameraDevice {
 		get;
 		set;
 	}
 	public virtual UIImagePickerControllerCameraFlashMode CameraFlashMode {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraDevice</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIImagePickerControllerCameraDevice
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum UIImagePickerControllerCameraDevice {
 	Rear,
 	Front
 }
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraFlashMode</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIImagePickerControllerCameraFlashMode
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum UIImagePickerControllerCameraFlashMode {
 	Off,
 	Auto,
 	On
 }
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIPasteboard</h2>
<p>Removed:</p><pre>
 	public virtual void Remove (string name);
</pre>
<p>Added:</p><pre>
 	public static void Remove (string name);
 	public virtual void AddItems (MonoTouch.Foundation.NSDictionary[] items);
 	public virtual bool Contains (string [] pasteboadTypes, MonoTouch.Foundation.NSIndexSet itemSet);
 	public virtual MonoTouch.Foundation.NSData DataForPasteboardType (string pasteboardType);
 	public virtual MonoTouch.Foundation.NSData[] GetDataForPasteboardType (string pasteboardType, MonoTouch.Foundation.NSIndexSet itemSet);
 	public virtual MonoTouch.Foundation.NSData[] GetValuesForPasteboardType (string pasteboardType, MonoTouch.Foundation.NSIndexSet itemSet);
 	public virtual MonoTouch.Foundation.NSIndexSet ItemSetWithPasteboardTypes (string [] pasteboardTypes);
 	public virtual MonoTouch.Foundation.NSArray[] PasteBoardTypesForSet (MonoTouch.Foundation.NSIndexSet itemSet);
 	public virtual void SetData (MonoTouch.Foundation.NSData data, string forPasteboardType);
 	public static MonoTouch.Foundation.NSString ChangedNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ChangedTypesAddedKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ChangedTypesRemovedKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RemovedNotification {
 		get;
 	}
 	public virtual UIColor Color {
 		get;
 		set;
 	}
 	public virtual UIColor[] Colors {
 		get;
 		set;
 	}
 	public virtual UIImage Image {
 		get;
 		set;
 	}
 	public virtual UIImage[] Images {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary[] Items {
 		get;
 		set;
 	}
 	public virtual string String {
 		get;
 		set;
 	}
 	public virtual string [] Strings {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSUrl Url {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSUrl[] Urls {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIWindow</h2>
<p>Removed:</p><pre>
 	public virtual UIViewController RootViewController {
 		get;
 		set;
 	}
</pre>
<h1>Namespace: MonoTouch.iAd</h1>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
