---
id: FA1E9F79-5D05-4AEC-945B-D649982F106F
title: "From 3.0.1 to 3.0.2"
---

<html><head><title>Comparison between monotouch-301.dll and monotouch.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "3.0.1";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.0.0";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h1>Namespace: MonoTouch.AdLib</h1>
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
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>New Type: MonoTouch.Foundation.NSSortDescriptor</h2>
<pre>
public class NSSortDescriptor : NSObject {
	
	public NSSortDescriptor ();
	public NSSortDescriptor (NSCoder coder);
	public NSSortDescriptor (NSObjectFlag t);
	public NSSortDescriptor (IntPtr handle);
	public NSSortDescriptor (string key, bool ascending);
	public NSSortDescriptor (string key, bool ascending, MonoTouch.ObjCRuntime.Selector selector);
	
	public virtual NSComparisonResult Compare (NSObject object1, NSObject object2);
	
	public virtual bool Ascending {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Key {
		get;
	}
	public virtual NSObject ReversedSortDescriptor {
		get;
	}
	public virtual MonoTouch.ObjCRuntime.Selector Selector {
		get;
	}
}
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h1>Namespace: MonoTouch.MapKit</h1>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h2>Type Changed: MonoTouch.ObjCRuntime.Messaging</h2>
<p>Added:</p><pre>
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
</pre>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h1>Namespace: MonoTouch.iAd</h1>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
