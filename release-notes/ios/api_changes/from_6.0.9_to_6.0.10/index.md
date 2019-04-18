---
id: (GUID)
title: "From 6.0.9 to 6.0.10"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


## Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


### Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "6.0.9";
```

Added:

```
public const string Version = "6.0.10";
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


## Namespace: MonoTouch.MapKit

 <a name="New_Type:_MonoTouch.MapKit.MKLocalSearch" class="injected"></a>


### New Type: MonoTouch.MapKit.MKLocalSearch

```
public class MKLocalSearch : MonoTouch.Foundation.NSObject {
	
	public MKLocalSearch ();
	public MKLocalSearch (MonoTouch.Foundation.NSCoder coder);
	public MKLocalSearch (MonoTouch.Foundation.NSObjectFlag t);
	public MKLocalSearch (IntPtr handle);
	public MKLocalSearch (MKLocalSearchRequest request);
	
	public virtual void Cancel ();
	public virtual void Start (MKLocalSearchCompletionHandler completionHandler);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool IsSearching {
		get;
	}
}
```

 <a name="New_Type:_MonoTouch.MapKit.MKLocalSearchCompletionHandler" class="injected"></a>


### New Type: MonoTouch.MapKit.MKLocalSearchCompletionHandler

```
[Serializable]
public delegate void MKLocalSearchCompletionHandler (MKLocalSearchResponse response, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.MapKit.MKLocalSearchRequest" class="injected"></a>


### New Type: MonoTouch.MapKit.MKLocalSearchRequest

```
public class MKLocalSearchRequest : MonoTouch.Foundation.NSObject {
	
	public MKLocalSearchRequest ();
	public MKLocalSearchRequest (MonoTouch.Foundation.NSCoder coder);
	public MKLocalSearchRequest (MonoTouch.Foundation.NSObjectFlag t);
	public MKLocalSearchRequest (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string NaturalLanguageQuery {
		get;
		set;
	}
	public virtual MKCoordinateRegion Region {
		get;
		set;
	}
}
```

 <a name="New_Type:_MonoTouch.MapKit.MKLocalSearchResponse" class="injected"></a>


### New Type: MonoTouch.MapKit.MKLocalSearchResponse

```
public class MKLocalSearchResponse : MonoTouch.Foundation.NSObject {
	
	public MKLocalSearchResponse (MonoTouch.Foundation.NSCoder coder);
	public MKLocalSearchResponse (MonoTouch.Foundation.NSObjectFlag t);
	public MKLocalSearchResponse (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKMapItem[] MapItems {
		get;
	}
	public virtual MKCoordinateRegion Region {
		get;
	}
}
```
