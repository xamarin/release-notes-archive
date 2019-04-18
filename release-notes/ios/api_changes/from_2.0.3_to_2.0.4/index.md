---
id: 7CB07A13-BA65-4E53-A1A2-250764206ACF
title: "From 2.0.3 to 2.0.4"
---

<html><head><title>Comparison between monotouch-203.dll and monotouch-204.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "2.0.3";
</pre>
<p>Added:</p><pre>
 	public const string Version = "2.0.4";
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
 	public virtual MonoTouch.Foundation.NSValue[] Values {
</pre>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h2>Type Changed: MonoTouch.CoreGraphics.CGContext</h2>
<p>Added:</p><pre>
 	public void DrawLayer (CGLayer layer, System.Drawing.PointF point);
 	public void DrawLayer (CGLayer layer, System.Drawing.RectangleF rect);
</pre>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h1>Namespace: MonoTouch.GameKit</h1>
<h2>Type Changed: MonoTouch.GameKit.GKSessionDelegate</h2>
<p>Removed:</p><pre>
 	public virtual void PeerConnectionFailed (GKSession session, MonoTouch.Foundation.NSError error);
</pre>
<p>Added:</p><pre>
 	public virtual void PeerConnectionFailed (GKSession session, string peerId, MonoTouch.Foundation.NSError error);
</pre>
<h1>Namespace: MonoTouch.MapKit</h1>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h1>Namespace: MonoTouch.OpenGLES</h1>
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
<h2>Type Changed: MonoTouch.UIKit.UITabBarController</h2>
<p>Added:</p><pre>
 	public UITabBarSelection ShouldSelectViewController {
 		get;
 		set;
 	}
 	
 	public event EventHandler&lt;UITabBarCustomizeChangeEventArgs&gt; FinishedCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarCustomizeEventArgs&gt; OnCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarCustomizeChangeEventArgs&gt; OnEndCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarSelectionEventArgs&gt; ViewControllerSelected;
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarCustomizeChangeEventArgs : EventArgs {
 	
 	public UITabBarCustomizeChangeEventArgs (UIViewController[] viewControllers, bool changed);
 	
 	public bool Changed {
 		get;
 		set;
 	}
 	public UIViewController[] ViewControllers {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarCustomizeEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarCustomizeEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarCustomizeEventArgs : EventArgs {
 	
 	public UITabBarCustomizeEventArgs (UIViewController[] viewControllers);
 	
 	public UIViewController[] ViewControllers {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarSelection</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarSelection
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool UITabBarSelection (UITabBarController tabBarController, UIViewController viewController);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarSelectionEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarSelectionEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarSelectionEventArgs : EventArgs {
 	
 	public UITabBarSelectionEventArgs (UIViewController viewController);
 	
 	public UIViewController ViewController {
 		get;
 		set;
 	}
 }
</pre>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
