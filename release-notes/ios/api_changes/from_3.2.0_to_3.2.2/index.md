---
id: FA00B626-68CF-46A4-8B0B-2CD3B1C67B8C
title: "From 3.2.0 to 3.2.2"
---

<html><head><title>Comparison between monotouch.dll and monotouch.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "3.2.0";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.2.2";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h2>Type Changed: MonoTouch.AVFoundation.AVUrlAsset</h2>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString PreferPreciseDurationAndTimingKey {
 		get;
 	}
</pre>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h1>Namespace: MonoTouch.AssetsLibrary</h1>
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h1>Namespace: MonoTouch.AudioUnit</h1>
<h1>Namespace: MonoTouch.AudioUnitWrapper</h1>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h2>Type Changed: MonoTouch.CoreAnimation.CATiledLayer</h2>
<p>Removed:</p><pre>
 		set;
</pre>
<h1>Namespace: MonoTouch.CoreData</h1>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h2>Type Changed: MonoTouch.CoreGraphics.CGPDFDocument</h2>
<p>Added:</p><pre>
 	public CGPDFPage GetPage (int page);
</pre>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h1>Namespace: MonoTouch.CoreMedia</h1>
<h1>Namespace: MonoTouch.CoreMotion</h1>
<h1>Namespace: MonoTouch.CoreTelephony</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.EventKit</h1>
<h1>Namespace: MonoTouch.EventKitUI</h1>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>New Type: MonoTouch.Foundation.NSComparisonPredicate</h2>
<pre>
public class NSComparisonPredicate : NSPredicate {
	
	public NSComparisonPredicate ();
	public NSComparisonPredicate (NSCoder coder);
	public NSComparisonPredicate (NSObjectFlag t);
	public NSComparisonPredicate (IntPtr handle);
	public NSComparisonPredicate (NSExpression leftExpression, NSExpression rightExpression, NSComparisonPredicateModifier comparisonModifier, NSPredicateOperatorType operatorType, NSComparisonPredicateOptions comparisonOptions);
	public NSComparisonPredicate (NSExpression leftExpression, NSExpression rightExpression, MonoTouch.ObjCRuntime.Selector selector);
	
	public static NSPredicate Create (NSExpression leftExpression, NSExpression rightExpression, NSComparisonPredicateModifier comparisonModifier, NSPredicateOperatorType operatorType, NSComparisonPredicateOptions comparisonOptions);
	public static NSPredicate FromSelector (NSExpression leftExpression, NSExpression rightExpression, MonoTouch.ObjCRuntime.Selector selector);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSComparisonPredicateModifier ComparisonPredicateModifier {
		get;
	}
	public virtual MonoTouch.ObjCRuntime.Selector CustomSelector {
		get;
	}
	public virtual NSExpression LeftExpression {
		get;
	}
	public virtual NSComparisonPredicateOptions Options {
		get;
	}
	public virtual NSPredicateOperatorType PredicateOperatorType {
		get;
	}
	public virtual NSExpression RightExpression {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.Foundation.NSComparisonPredicateModifier</h2>
<pre>
[Serializable]
public enum NSComparisonPredicateModifier {
	Direct,
	All,
	Any
}
</pre>
<h2>New Type: MonoTouch.Foundation.NSComparisonPredicateOptions</h2>
<pre>
[Serializable]
[Flags]
public enum NSComparisonPredicateOptions {
	CaseInsensitive,
	DiacriticInsensitive
}
</pre>
<h2>New Type: MonoTouch.Foundation.NSCompoundPredicate</h2>
<pre>
public class NSCompoundPredicate : NSPredicate {
	
	public NSCompoundPredicate ();
	public NSCompoundPredicate (NSCoder coder);
	public NSCompoundPredicate (NSObjectFlag t);
	public NSCompoundPredicate (IntPtr handle);
	public NSCompoundPredicate (NSCompoundPredicateType type, NSPredicate[] subpredicates);
	
	public static NSPredicate CreateAndPredicate (NSPredicate[] subpredicates);
	public static NSPredicate CreateNotPredicate (NSPredicate predicate);
	public static NSPredicate CreateOrPredicate (NSPredicate[] subpredicates);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSPredicate[] Subpredicates {
		get;
	}
	public virtual NSCompoundPredicateType Type {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.Foundation.NSCompoundPredicateType</h2>
<pre>
[Serializable]
public enum NSCompoundPredicateType {
	Not,
	And,
	Or
}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSDictionary</h2>
<p>Added:</p><pre>
 	public static NSDictionary FromObjectsAndKeys (NSObject[] objects, NSObject[] keys);
 	public static NSDictionary FromObjectsAndKeys (NSObject[] objects, NSObject[] keys, int count);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSError</h2>
<p>Added:</p><pre>
 	public NSError (NSString domain, int code);
 	public NSError (NSString domain, int code, NSDictionary userInfo);
 	public static NSError FromDomain (NSString domain, int code);
 	public static NSError FromDomain (NSString domain, int code, NSDictionary userInfo);
 	public static NSString CocoaErrorDomain {
 		get;
 	}
 	public static NSString FilePathErrorKey {
 		get;
 	}
 	public static NSString HelpAnchorErrorKey {
 		get;
 	}
 	public static NSString LocalizedDescriptionKey {
 		get;
 	}
 	public static NSString LocalizedFailureReasonErrorKey {
 		get;
 	}
 	public static NSString LocalizedRecoveryOptionsErrorKey {
 		get;
 	}
 	public static NSString LocalizedRecoverySuggestionErrorKey {
 		get;
 	}
 	public static NSString MachErrorDomain {
 		get;
 	}
 	public static NSString OsStatusErrorDomain {
 		get;
 	}
 	public static NSString PosixErrorDomain {
 		get;
 	}
 	public static NSString RecoveryAttempterErrorKey {
 		get;
 	}
 	public static NSString StringEncodingErrorKey {
 		get;
 	}
 	public static NSString UnderlyingErrorKey {
 		get;
 	}
 	public static NSString UrlErrorKey {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSFileManager</h2>
<p>Removed:</p><pre>
 	public virtual bool CopyPath (string src, string dest, IntPtr handler);
 	public virtual bool LinkPath (string src, string dest, IntPtr handler);
 	public virtual bool MovePath (string src, string dest, IntPtr handler);
 	public virtual bool RemoveFileAtPath (string path, IntPtr handler);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSMutableData</h2>
<p>Added:</p><pre>
 	public static NSMutableData Create ();
 	public static NSMutableData FromCapacity (int capacity);
 	public static NSMutableData FromLength (int length);
 	public void AppendBytes (byte [] bytes);
 	public void AppendBytes (byte [] bytes, int start, int len);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSMutableDictionary</h2>
<p>Removed:</p><pre>
 	public bool ContainsKey (NSObject key);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSNotificationCenter</h2>
<p>Removed:</p><pre>
 	public virtual void AddObserver (NSObject observer, MonoTouch.ObjCRuntime.Selector aSelector, string aName, NSObject anObject);
</pre>
<p>Added:</p><pre>
 	public virtual void AddObserver (NSObject observer, MonoTouch.ObjCRuntime.Selector aSelector, NSString aName, NSObject anObject);
 	public void AddObserver (NSObject observer, MonoTouch.ObjCRuntime.Selector aSelector, string aname, NSObject anObject);
 	public NSObject AddObserver (NSString aName, Action&lt;NSNotification&gt; notify);
 	public NSObject AddObserver (NSString aName, Action&lt;NSNotification&gt; notify, NSObject fromObject);
 	public void RemoveObservers (System.Collections.Generic.IEnumerable&lt;NSObject&gt; keys);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSObject</h2>
<p>Added:</p><pre>
 	public static NSObject GetDefaultPlaceholder (NSObject marker, string binding);
 	public virtual void Bind (string binding, NSObject observable, string keyPath, NSDictionary options);
 	public virtual NSDictionary BindingInfo (string binding);
 	public virtual NSObject[] BindingOptionDescriptions (string aBinding);
 	public virtual MonoTouch.ObjCRuntime.Class BindingValueClass (string binding);
 	public virtual bool CommitEditing ();
 	public virtual void CommitEditing (NSObject objDelegate, MonoTouch.ObjCRuntime.Selector didCommitSelector, IntPtr contextInfo);
 	public virtual NSString[] ExposedBindings ();
 	public virtual void ObjectDidEndEditing (NSObject editor);
 	public virtual void Unbind (string binding);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSPredicate</h2>
<p>Added:</p><pre>
 	public static NSPredicate FromExpression (NSPredicateEvaluator evaluator);
 	public static NSPredicate FromFormat (string predicateFormat, NSObject[] arguments);
 	public static NSPredicate FromValue (bool value);
 	public virtual bool EvaluateWithObject (NSObject obj, NSDictionary substitutionVariables);
 	public virtual NSPredicate PredicateWithSubstitutionVariables (NSDictionary substitutionVariables);
 	public virtual string PredicateFormat {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSPredicateEvaluator</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSPredicateEvaluator
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool NSPredicateEvaluator (NSObject evaluatedObject, NSDictionary bindings);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSPredicateOperatorType</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSPredicateOperatorType
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum NSPredicateOperatorType {
 	LessThan,
 	LessThanOrEqualTo,
 	GreaterThan,
 	GreaterThanOrEqualTo,
 	EqualTo,
 	NotEqualTo,
 	Matches,
 	Like,
 	BeginsWith,
 	EndsWith,
 	In,
 	CustomSelector,
 	Contains,
 	Between
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSRunLoop</h2>
<p>Removed:</p><pre>
 	public virtual void AcceptInputForMode (string mode, NSDate limitDate);
 	public virtual void AddTimer (NSTimer timer, string forMode);
 	public virtual NSDate LimitDateForMode (string mode);
 	public virtual string CurrentMode {
</pre>
<p>Added:</p><pre>
 	public void AcceptInputForMode (NSRunLoopMode mode, NSDate limitDate);
 	public virtual void AcceptInputForMode (NSString mode, NSDate limitDate);
 	public void AcceptInputForMode (string mode, NSDate limitDate);
 	public void AddTimer (NSTimer timer, NSRunLoopMode forMode);
 	public virtual void AddTimer (NSTimer timer, NSString forMode);
 	public void AddTimer (NSTimer timer, string forMode);
 	public NSDate LimitDateForMode (NSRunLoopMode mode);
 	public virtual NSDate LimitDateForMode (NSString mode);
 	public NSDate LimitDateForMode (string mode);
 	public virtual NSString CurrentMode {
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSRunLoopMode</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSRunLoopMode
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum NSRunLoopMode {
 	Default,
 	Common
 }
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h1>Namespace: MonoTouch.ImageIO</h1>
<h1>Namespace: MonoTouch.MapKit</h1>
<h2>Type Changed: MonoTouch.MapKit.MKShape</h2>
<p>Removed:</p><pre>
 	public override string Subtitle {
 	public override string Title {
</pre>
<p>Added:</p><pre>
 	public virtual string Subtitle {
 		set;
 	public virtual string Title {
 		set;
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKUserLocation</h2>
<p>Removed:</p><pre>
 	public override string Subtitle {
 	public override string Title {
</pre>
<p>Added:</p><pre>
 	public virtual string Subtitle {
 		set;
 	public virtual string Title {
 		set;
</pre>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h2>Type Changed: MonoTouch.ObjCRuntime.Messaging</h2>
<p>Added:</p><pre>
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_int_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4, int arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4, int arg5);
</pre>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h1>Namespace: MonoTouch.Security</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h2>Type Changed: MonoTouch.UIKit.UIFont</h2>
<p>Added:</p><pre>
 	public virtual float LineHeight {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIPrintInteractionController</h2>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject[] PrintingItems {
 	public virtual MonoTouch.Foundation.NSObject PrintItem {
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject PrintingItem {
 	public virtual MonoTouch.Foundation.NSObject[] PrintingItems {
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIScreen</h2>
<p>Removed:</p><pre>
 	public virtual MonoTouch.CoreAnimation.CADisplayLink DisplayLink (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector sel);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.CoreAnimation.CADisplayLink CreateDisplayLink (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector sel);
</pre>
<h1>Namespace: MonoTouch.iAd</h1>
<h2>Type Changed: MonoTouch.iAd.ADBannerView</h2>
<p>Added:</p><pre>
 		set;
</pre>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
