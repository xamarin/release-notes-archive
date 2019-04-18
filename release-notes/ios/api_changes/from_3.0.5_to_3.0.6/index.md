---
id: 043BBFCD-55F5-4E01-B860-F04D2513A9C6
title: "From 3.0.5 to 3.0.6"
---

<html><head><title>Comparison between monotouch-305.dll and monotouch-306.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "3.0.5";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.0.4";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h2>Type Changed: MonoTouch.AVFoundation.AVAssetExportSession</h2>
<p>Removed:</p><pre>
 	public static string LocalizedNameForExportPreset (string presetName);
 	public virtual string LocalizedExportSessionOutputSummary {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureConnection</h2>
<p>Added:</p><pre>
 	public virtual bool SupportsVideoMirroring {
 		get;
 	}
 	public virtual bool SupportsVideoOrientation {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer</h2>
<p>Added:</p><pre>
 	public virtual bool MirroringSupported {
 		get;
 	}
 	public virtual bool OrientationSupported {
 		get;
 	}
 	public virtual string VideoGravity {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVFileType</h2>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString Mpeg4Audio {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString AppleM4A {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h2>
<p>Removed:</p><pre>
 	public virtual System.Drawing.SizeF NaturalSize {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public virtual System.Drawing.SizeF PresentationSize {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerLayer</h2>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString VideoGravityResize {
 	public static MonoTouch.Foundation.NSString VideoGravityResizeAspect {
 	public static MonoTouch.Foundation.NSString VideoGravityResizeAspectFill {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString GravityResize {
 	public static MonoTouch.Foundation.NSString GravityResizeAspect {
 	public static MonoTouch.Foundation.NSString GravityResizeAspectFill {
 	public virtual bool ReadyForDisplay {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVVideoCompositionInstruction</h2>
<p>Added:</p><pre>
 	public virtual bool EnablePostProcessing {
 		get;
 	}
</pre>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h1>Namespace: MonoTouch.CoreMedia</h1>
<h1>Namespace: MonoTouch.CoreTelephony</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.EventKit</h1>
<h2>Type Changed: MonoTouch.EventKit.EKEvent</h2>
<p>Removed:</p><pre>
 	public static EKEvent Create ();
</pre>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>Type Changed: MonoTouch.Foundation.NSRange</h2>
<p>Added:</p><pre>
 	public const int NotFound = 2147483647;
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h1>Namespace: MonoTouch.MapKit</h1>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h2>Type Changed: MonoTouch.UIKit.UIApplication</h2>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString InvalidBackgroundTaskIdentifier {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString BackgroundTaskInvalid {
 		get;
 	}
</pre>
<h1>Namespace: MonoTouch.iAd</h1>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
