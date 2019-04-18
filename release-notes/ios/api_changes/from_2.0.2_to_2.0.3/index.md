---
id: 14E66DEB-D688-48EF-97E3-C15BB86F74A4
title: "From 2.0.2 to 2.0.3"
---

<html><head><title>Comparison between monotouch-202.dll and monotouch-203.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "2.0.2";
</pre>
<p>Added:</p><pre>
 	public const string Version = "2.0.3";
 	public const string FoundationLibrary = "/System/Library/Frameworks/Foundation.framework/Foundation";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h2>Type Changed: MonoTouch.CoreGraphics.CGLayer</h2>
<p>Added:</p><pre>
 	public CGContext Context {
 		get;
 	}
</pre>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h2>New Type: MonoTouch.ExternalAccessory.EAAccessory</h2>
<pre>
public class EAAccessory : MonoTouch.Foundation.NSObject {
	
	public EAAccessory ();
	public EAAccessory (MonoTouch.Foundation.NSCoder coder);
	public EAAccessory (MonoTouch.Foundation.NSObjectFlag t);
	public EAAccessory (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Connected {
		get;
	}
	public virtual uint ConnectionID {
		get;
	}
	public EAAccessoryDelegate Delegate {
		get;
		set;
	}
	public virtual string FirmwareRevision {
		get;
	}
	public virtual string HardwareRevision {
		get;
	}
	public virtual string Manufacturer {
		get;
	}
	public virtual string ModelNumber {
		get;
	}
	public virtual string Name {
		get;
	}
	public virtual string [] ProtocolStrings {
		get;
	}
	public virtual string SerialNumber {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler Disconnected;
}
</pre>
<h2>New Type: MonoTouch.ExternalAccessory.EAAccessoryDelegate</h2>
<pre>
public class EAAccessoryDelegate : MonoTouch.Foundation.NSObject {
	
	public EAAccessoryDelegate ();
	public EAAccessoryDelegate (MonoTouch.Foundation.NSCoder coder);
	public EAAccessoryDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public EAAccessoryDelegate (IntPtr handle);
	
	public virtual void Disconnected (EAAccessory accessory);
}
</pre>
<h2>New Type: MonoTouch.ExternalAccessory.EAAccessoryManager</h2>
<pre>
public class EAAccessoryManager : MonoTouch.Foundation.NSObject {
	
	public EAAccessoryManager ();
	public EAAccessoryManager (MonoTouch.Foundation.NSCoder coder);
	public EAAccessoryManager (MonoTouch.Foundation.NSObjectFlag t);
	public EAAccessoryManager (IntPtr handle);
	
	public virtual void RegisterForLocalNotifications ();
	public virtual void UnregisterForLocalNotifications ();
	
	public static EAAccessoryManager SharedAccessoryManager {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual EAAccessory[] ConnectedAccessories {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.ExternalAccessory.EASession</h2>
<pre>
public class EASession : MonoTouch.Foundation.NSObject {
	
	public EASession ();
	public EASession (MonoTouch.Foundation.NSCoder coder);
	public EASession (MonoTouch.Foundation.NSObjectFlag t);
	public EASession (IntPtr handle);
	public EASession (EAAccessory accessory, string protocol);
	
	public virtual EAAccessory Accessory {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSInputStream InputStream {
		get;
	}
	public virtual MonoTouch.Foundation.NSOutputStream OutputStream {
		get;
	}
	public virtual string ProtocolString {
		get;
	}
}
</pre>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>Type Changed: MonoTouch.Foundation.NSAttributedString</h2>
<p>Added:</p><pre>
 	public static string FontAttributeName {
 		get;
 	}
 	public static string ParagraphStyleAttributeName {
 		get;
 	}
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h1>Namespace: MonoTouch.MapKit</h1>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h2>Type Changed: MonoTouch.MediaPlayer.ItemsPickedEventArgs</h2>
<p>Added:</p><pre>
 		set;
</pre>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h2>Type Changed: MonoTouch.UIKit.UIImage</h2>
<p>Added:</p><pre>
 	public static UIImage FromResource (System.Reflection.Assembly assembly, string name);
 	public UIImage Scale (System.Drawing.SizeF newSize);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIWindow</h2>
<p>Added:</p><pre>
 		set;
</pre>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
