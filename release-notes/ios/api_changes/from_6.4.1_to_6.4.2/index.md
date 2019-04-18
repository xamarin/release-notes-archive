---
id: 12E7074E-3010-4B0B-951F-36D323AC2A56
title: "From 6.4.1 to 6.4.2"
---

<html><head><title>Comparison between monotouch-6.4.1.1.dll and monotouch.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
	public const string Version = "6.4.1";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.4.2";
</pre>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioSession</h3>
<p>Removed:</p><pre>
 	public static void AddListener (AudioSessionProperty property, PropertyListener listener);
</pre>
<p>Added:</p><pre>
 	public static AudioSessionErrors AddListener (AudioSessionProperty property, PropertyListener listener);
 	public event Action&lt;bool&gt; AudioInputBecameAvailable;
 	public event Action&lt;float&gt; CurrentHardwareOutputVolumeChanged;
 	public event Action&lt;bool&gt; InputGainBecameAvailable;
 	public event Action&lt;float&gt; InputGainScalarChanged;
 	public event Action&lt;AccessoryInfo[]&gt; InputSourcesChanged;
 	public event Action&lt;AccessoryInfo[]&gt; OutputDestinationsChanged;
 	public event Action&lt;bool&gt; ServerDied;
</pre>
<h3>New Type: MonoTouch.AudioToolbox.InputSourceInfo</h3>
<pre>
public class InputSourceInfo {
	
	public InputSourceInfo ();
	
	public string Description {
		get;
	}
	public int ID {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSArray</h3>
<p>Added:</p><pre>
 	public static NSArray FromObjects (int count, params object [] items);
</pre>
<h3>New Type: MonoTouch.Foundation.NSInvocation</h3>
<pre>
public class NSInvocation : NSObject {
	
	public NSInvocation (NSCoder coder);
	public NSInvocation (NSObjectFlag t);
	public NSInvocation (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	public virtual void Invoke ();
	public virtual void Invoke (NSObject target);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSMethodSignature MethodSignature {
		get;
	}
	public virtual MonoTouch.ObjCRuntime.Selector Selector {
		get;
		set;
	}
	public virtual NSObject Target {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMachPort</h3>
<pre>
public class NSMachPort : NSPort {
	
	public NSMachPort ();
	public NSMachPort (NSCoder coder);
	public NSMachPort (NSObjectFlag t);
	public NSMachPort (IntPtr handle);
	
	public static NSPort FromMachPort (uint port);
	public static NSPort FromMachPort (uint port, NSMachPortRights options);
	protected override void Dispose (bool disposing);
	public virtual void RemoveFromRunLoop (NSRunLoop runLoop, NSString mode);
	public virtual void ScheduleInRunLoop (NSRunLoop runLoop, NSString mode);
	
	public override IntPtr ClassHandle {
		get;
	}
	public NSMachPortDelegate Delegate {
		get;
		set;
	}
	public virtual uint MachPort {
		get;
	}
	public virtual NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMachPortDelegate</h3>
<pre>
public class NSMachPortDelegate : NSPortDelegate {
	
	public NSMachPortDelegate ();
	public NSMachPortDelegate (NSCoder coder);
	public NSMachPortDelegate (NSObjectFlag t);
	public NSMachPortDelegate (IntPtr handle);
	
	public virtual void MachMessageReceived (IntPtr msgHeader);
	public override void MessageReceived (NSPortMessage message);
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMachPortRights</h3>
<pre>
[Serializable]
[Flags]
public enum NSMachPortRights {
	None,
	SendRight,
	ReceiveRight
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMethodSignature</h3>
<pre>
public class NSMethodSignature : NSObject {
	
	public NSMethodSignature (NSCoder coder);
	public NSMethodSignature (NSObjectFlag t);
	public NSMethodSignature (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual uint FrameLength {
		get;
	}
	public virtual bool IsOneway {
		get;
	}
	public virtual uint MethodReturnLength {
		get;
	}
	public virtual uint NumberOfArguments {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSObject</h3>
<p>Added:</p><pre>
 	public NSObject Autorelease ();
 	public void Release ();
 	public NSObject Retain ();
</pre>
<h3>New Type: MonoTouch.Foundation.NSPort</h3>
<pre>
public class NSPort : NSObject {
	
	public NSPort (NSCoder coder);
	public NSPort (NSObjectFlag t);
	public NSPort (IntPtr handle);
	
	public static NSPort Create ();
	protected override void Dispose (bool disposing);
	public virtual void Invalidate ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public NSPortDelegate Delegate {
		get;
		set;
	}
	public virtual bool IsValid {
		get;
	}
	public virtual NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSPortDelegate</h3>
<pre>
public class NSPortDelegate : NSObject {
	
	public NSPortDelegate ();
	public NSPortDelegate (NSCoder coder);
	public NSPortDelegate (NSObjectFlag t);
	public NSPortDelegate (IntPtr handle);
	
	public virtual void MessageReceived (NSPortMessage message);
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSPortMessage</h3>
<pre>
public class NSPortMessage : NSObject {
	
	public NSPortMessage ();
	public NSPortMessage (NSCoder coder);
	public NSPortMessage (NSObjectFlag t);
	public NSPortMessage (IntPtr handle);
	public NSPortMessage (NSPort sendPort, NSPort recvPort, NSArray components);
	
	protected override void Dispose (bool disposing);
	public virtual bool SendBefore (NSDate date);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSArray Components {
		get;
	}
	public virtual uint MsgId {
		get;
		set;
	}
	public virtual NSPort ReceivePort {
		get;
	}
	public virtual NSPort SendPort {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.MobileCoreServices</h2>
<h3>Type Changed: MonoTouch.MobileCoreServices.UTType</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString PICT;
</pre>
</body>
</html>
