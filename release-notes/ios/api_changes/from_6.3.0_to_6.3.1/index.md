---
id: C93855D0-DBC4-4C81-B6E2-978C34EB1373
title: "From 6.3.0 to 6.3.1"
---

<html><head><title>Comparison between monotouch-6.3.0.255.dll and monotouch-6.3.1.0.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.3.0";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.3.1";
</pre>
<h3>New Type: MonoTouch.MonoTouchException</h3>
<pre>
public class MonoTouchException : Exception {
	
	public MonoTouchException (string message, params object [] args);
	public MonoTouchException (int code, string message, params object [] args);
	public MonoTouchException (int code, bool error, string message, params object [] args);
	public MonoTouchException (int code, bool error, Exception innerException, string message, params object [] args);
	
	public int Code {
		get;
	}
	public bool Error {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.ExportAttribute</h3>
<p>Added:</p><pre>
 	public bool IsVariadic {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.FieldAttribute</h3>
<pre>
public class FieldAttribute : Attribute {
	
	public FieldAttribute (string symbolName);
	public FieldAttribute (string symbolName, string libraryName);
	
	public string LibraryName {
		get;
		set;
	}
	public string SymbolName {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.ProtocolAttribute</h3>
<pre>
public sealed class ProtocolAttribute : Attribute {
	
	public ProtocolAttribute ();
}
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>Type Changed: MonoTouch.UIKit.UITableViewDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSIndexPath WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewSource</h3>
<p>Removed:</p><pre>
 	public virtual void WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSIndexPath WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
</body>
</html>
