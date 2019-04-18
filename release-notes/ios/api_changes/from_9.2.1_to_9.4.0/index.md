---
id: 90441005-3D7C-49C6-A73E-4A4F3AB234BC
title: "From 9.2.1 to 9.4.0"
---

# API diff

 [(Classic) monotouch.dll](#compat/monotouch)

   


 [(Unified) Xamarin.iOS.dll](#reference/Xamarin.iOS)

   


   


 <hr>

<h1 id='compat/monotouch'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string SdkVersion = "9.1" "9.2";
	public const string Version = "9.2.1" "9.4.0";
```

## Namespace MonoTouch.CloudKit

### New Type MonoTouch.CloudKit.CKFetchWebAuthTokenOperation

<pre style='color: green'>
public class CKFetchWebAuthTokenOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchWebAuthTokenOperation ();
	public CKFetchWebAuthTokenOperation (MonoTouch.Foundation.NSCoder coder);
	public CKFetchWebAuthTokenOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKFetchWebAuthTokenOperation (IntPtr handle);
	public CKFetchWebAuthTokenOperation (string token);
	// properties
	public virtual string ApiToken { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual CKFetchWebAuthTokenOperationHandler Completed { get; set; }
}
</pre>

### New Type MonoTouch.CloudKit.CKFetchWebAuthTokenOperationHandler

<pre style='color: green'>
public sealed delegate CKFetchWebAuthTokenOperationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchWebAuthTokenOperationHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (string webAuthToken, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (string webAuthToken, MonoTouch.Foundation.NSError operationError);
}
</pre>

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMediaItem

Added properties:

<pre style='color: green'>
	public bool HasProtectedAsset { get; }
	public static MonoTouch.Foundation.NSString HasProtectedAssetProperty { get; }
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPMediaPickerController

Added property:

<pre style='color: green'>
	public virtual bool ShowsItemsWithProtectedAssets { get; set; }
</pre>

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added value:

<pre style='color: green'>
	iOS_9_2 = 590336,
</pre>

## Namespace MonoTouch.PassKit

### Type Changed: MonoTouch.PassKit.PKContact

Added property:

<pre style='color: green'>
	public virtual string SupplementarySubLocality { get; set; }
</pre>

### Type Changed: MonoTouch.PassKit.PKPaymentAuthorizationStatus

Added values:

<pre style='color: green'>
	PinIncorrect = 6,
	PinLockout = 7,
	PinRequired = 5,
</pre>

### Type Changed: MonoTouch.PassKit.PKPaymentNetwork

Added properties:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString ChinaUnionPay { get; }
	public static MonoTouch.Foundation.NSString Interac { get; }
</pre>

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SslSessionStrengthPolicy

Added value:

<pre style='color: green'>
	ATSv1NoPFS = 2,
</pre>

## Namespace MonoTouch.WatchKit

### Type Changed: MonoTouch.WatchKit.WKErrorCode

Added value:

<pre style='color: green'>
	RecordingFailedError = 6,
</pre>

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace CloudKit

### New Type CloudKit.CKFetchWebAuthTokenOperation

<pre style='color: green'>
public class CKFetchWebAuthTokenOperation : CloudKit.CKDatabaseOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CKFetchWebAuthTokenOperation ();
	protected CKFetchWebAuthTokenOperation (Foundation.NSObjectFlag t);
	protected CKFetchWebAuthTokenOperation (IntPtr handle);
	public CKFetchWebAuthTokenOperation (string token);
	// properties
	public virtual string ApiToken { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual CKFetchWebAuthTokenOperationHandler Completed { get; set; }
}
</pre>

### New Type CloudKit.CKFetchWebAuthTokenOperationHandler

<pre style='color: green'>
public sealed delegate CKFetchWebAuthTokenOperationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchWebAuthTokenOperationHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (string webAuthToken, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (string webAuthToken, Foundation.NSError operationError);
}
</pre>

## Namespace MediaPlayer

### Type Changed: MediaPlayer.MPMediaItem

Added properties:

<pre style='color: green'>
	public bool HasProtectedAsset { get; }
	public static Foundation.NSString HasProtectedAssetProperty { get; }
</pre>

### Type Changed: MediaPlayer.MPMediaPickerController

Added property:

<pre style='color: green'>
	public virtual bool ShowsItemsWithProtectedAssets { get; set; }
</pre>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string SdkVersion = "9.1" "9.2";
	public const string Version = "9.2.1" "9.4.0";
```

### Type Changed: ObjCRuntime.Platform

Added value:

<pre style='color: green'>
	iOS_9_2 = 590336,
</pre>

## Namespace PassKit

### Type Changed: PassKit.PKContact

Added property:

<pre style='color: green'>
	public virtual string SupplementarySubLocality { get; set; }
</pre>

### Type Changed: PassKit.PKPaymentAuthorizationStatus

Added values:

<pre style='color: green'>
	PinIncorrect = 6,
	PinLockout = 7,
	PinRequired = 5,
</pre>

### Type Changed: PassKit.PKPaymentNetwork

Added properties:

<pre style='color: green'>
	public static Foundation.NSString ChinaUnionPay { get; }
	public static Foundation.NSString Interac { get; }
</pre>

## Namespace Security

### Type Changed: Security.SslSessionStrengthPolicy

Added value:

<pre style='color: green'>
	ATSv1NoPFS = 2,
</pre>

## Namespace WatchKit

### Type Changed: WatchKit.WKErrorCode

Added value:

<pre style='color: green'>
	RecordingFailedError = 6,
</pre>

   


 <hr>
