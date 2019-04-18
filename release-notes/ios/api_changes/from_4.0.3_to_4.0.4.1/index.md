---
id: AC56D886-8875-49C5-8DF9-835BCD4A4C3E
title: "From 4.0.3 to 4.0.4.1"
---

<html><head><title>Comparison between monotouch-4.0.3.dll and monotouch-4.0.4.1.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "4.0.3";
</pre>
<p>Added:</p><pre>
 	public const string Version = "4.0.4.1";
</pre>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>New Type: MonoTouch.Foundation.ActionAttribute</h2>
<pre>
public sealed class ActionAttribute : ExportAttribute {
	
	public ActionAttribute ();
	public ActionAttribute (string selector);
}
</pre>
<h2>Type Changed: MonoTouch.Foundation.ExportAttribute</h2>
<p>Removed:</p><pre>
 public sealed class ExportAttribute : Attribute {
</pre>
<p>Added:</p><pre>
 public class ExportAttribute : Attribute {
 	public ExportAttribute ToGetter (System.Reflection.PropertyInfo prop);
 	public ExportAttribute ToSetter (System.Reflection.PropertyInfo prop);
 	
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSArray</h2>
<p>Added:</p><pre>
 	public static T[] FromArray&lt;T&gt; (NSArray weakArray) where T : NSObject;
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSValue</h2>
<p>Added:</p><pre>
 	public string ObjCType {
 		get;
 	}
</pre>
<h2>New Type: MonoTouch.Foundation.OutletAttribute</h2>
<pre>
public sealed class OutletAttribute : ExportAttribute {
	
	public OutletAttribute ();
	public OutletAttribute (string name);
}
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h2>Type Changed: MonoTouch.GameKit.GKDataEventArgs</h2>
<p>Removed:</p><pre>
 	public GKDataEventArgs (MonoTouch.Foundation.NSData data, GKPlayer player);
 	public GKPlayer Player { }
</pre>
<p>Added:</p><pre>
 	public GKDataEventArgs (MonoTouch.Foundation.NSData data, string playerId);
 	public string PlayerId { } 
</pre>
<h2>Type Changed: MonoTouch.GameKit.GKError</h2>
<p>Fixed this enumeration values.
<p>Added:</p><pre>
 	AuthenticationInProgress,
 	UnexpectedConnection
</pre>
<h2>Type Changed: MonoTouch.GameKit.GKMatchDelegate</h2>
<p>Removed:</p><pre>
 	public abstract void ConnectionFailed (GKMatch match, GKPlayer player, MonoTouch.Foundation.NSError error);
 	public abstract void DataReceived (GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer player);
 	public abstract void Failed (GKMatch match, MonoTouch.Foundation.NSError error);
 	public abstract void StateChanged (GKMatch match, GKPlayer player, GKPlayerConnectionState state);
</pre>
<p>Added:</p><pre>
 	public virtual void ConnectionFailed (GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
 	public abstract void DataReceived (GKMatch match, MonoTouch.Foundation.NSData data, string playerId);
 	public virtual void Failed (GKMatch match, MonoTouch.Foundation.NSError error);
 	public virtual void StateChanged (GKMatch match, string playerId, GKPlayerConnectionState state);
</pre>
<h2>Type Changed: MonoTouch.GameKit.GKPlayerErrorEventArgs</h2>
<p>Removed:</p><pre>
 	public GKPlayerErrorEventArgs (GKPlayer player, MonoTouch.Foundation.NSError error);
 	public GKPlayer Player {
</pre>
<p>Added:</p><pre>
 	public GKPlayerErrorEventArgs (string playerId, MonoTouch.Foundation.NSError error);
 	public string PlayerId {
</pre>
<h2>Type Changed: MonoTouch.GameKit.GKStateEventArgs</h2>
<p>Removed:</p><pre>
 	public GKStateEventArgs (GKPlayer player, GKPlayerConnectionState state);
 	public GKPlayer Player {
</pre>
<p>Added:</p><pre>
 	public GKStateEventArgs (string playerId, GKPlayerConnectionState state);
 	public string PlayerId {
</pre>
<h2>Type Changed: MonoTouch.ObjCRuntime.Dlfcn</h2>
<p>Added:</p><pre>
 	public static float GetFloat (IntPtr handle, string symbol);
</pre>
</body>
</html>
