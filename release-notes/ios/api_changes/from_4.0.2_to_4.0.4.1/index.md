---
id: 59354F33-21F2-DB67-3D71-4F8827B09994
title: "From 4.0.2 to 4.0.4.1"
---

The following is a detailed list of the changes in the `monotouch.dll` library:

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "4.0.3";
```

Added:

```
public const string Version = "4.0.4.1";
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="New_Type:_MonoTouch.Foundation.ActionAttribute" class="injected"></a>


## New Type: MonoTouch.Foundation.ActionAttribute

```
public sealed class ActionAttribute : ExportAttribute {
        
        public ActionAttribute ();
        public ActionAttribute (string selector);
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.ExportAttribute" class="injected"></a>


## Type Changed: MonoTouch.Foundation.ExportAttribute

Removed:

```
public sealed class ExportAttribute : Attribute {
```

Added:

```
public class ExportAttribute : Attribute {
        public ExportAttribute ToGetter (System.Reflection.PropertyInfo prop);
        public ExportAttribute ToSetter (System.Reflection.PropertyInfo prop);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSArray" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSArray

Added:

```
public static T[] FromArray<T> (NSArray weakArray) where T : NSObject;
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSValue" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSValue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

Added:

```
public string ObjCType {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.OutletAttribute" class="injected"></a>


## New Type: MonoTouch.Foundation.OutletAttribute

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

```
public sealed class OutletAttribute : ExportAttribute {
        
        public OutletAttribute ();
        public OutletAttribute (string name);
}
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKDataEventArgs" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKDataEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

Removed:

```
public GKDataEventArgs (MonoTouch.Foundation.NSData data, GKPlayer player);
        public GKPlayer Player { }
```

Added:

```
public GKDataEventArgs (MonoTouch.Foundation.NSData data, string playerId);
        public string PlayerId { }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKError" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

Fixed this enumeration values.

Added:

```
AuthenticationInProgress,
        UnexpectedConnection
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchDelegate" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

Removed:

```
public abstract void ConnectionFailed (GKMatch match, GKPlayer player, MonoTouch.Foundation.NSError error);
        public abstract void DataReceived (GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer player);
        public abstract void Failed (GKMatch match, MonoTouch.Foundation.NSError error);
        public abstract void StateChanged (GKMatch match, GKPlayer player, GKPlayerConnectionState state);
```

Added:

```
public virtual void ConnectionFailed (GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
        public abstract void DataReceived (GKMatch match, MonoTouch.Foundation.NSData data, string playerId);
        public virtual void Failed (GKMatch match, MonoTouch.Foundation.NSError error);
        public virtual void StateChanged (GKMatch match, string playerId, GKPlayerConnectionState state);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayerErrorEventArgs" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayerErrorEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

Removed:

```
public GKPlayerErrorEventArgs (GKPlayer player, MonoTouch.Foundation.NSError error);
        public GKPlayer Player {
```

Added:

```
public GKPlayerErrorEventArgs (string playerId, MonoTouch.Foundation.NSError error);
        public string PlayerId {
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKStateEventArgs" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKStateEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

Removed:

```
public GKStateEventArgs (GKPlayer player, GKPlayerConnectionState state);
        public GKPlayer Player {
```

Added:

```
public GKStateEventArgs (string playerId, GKPlayerConnectionState state);
        public string PlayerId {
```

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Dlfcn" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Dlfcn

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.0.2_to_4.0.4.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.4.1#)

Added:

```
public static float GetFloat (IntPtr handle, string symbol);
```
