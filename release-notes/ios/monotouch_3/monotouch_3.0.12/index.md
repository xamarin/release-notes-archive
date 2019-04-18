---
id: C96153EE-3EFA-0525-BC11-5B15669B36BA
title: "MonoTouch 3.0.12"
---

&nbsp;

 <a name="Highlights" class="injected"></a>


# Highlights

These are the higlights of this release:

-  Automatic memory management for UIAlertView and UIActionSheet.
-  CoreData API (MonoTouch.CoreData).
-  New Foundation types: -   MonoTouch.Foundation.NSExpression (for CoreData). 
-   Implicit conversions from integral data types to NSNumber.
-   Explicit conversions to extract values from an NSNumber.
-   Indexers for NSStrings


 


 <a name="Automatic_Memory_Management_for_UIAlertView_and_UIActionSheet" class="injected"></a>


# Automatic Memory Management for UIAlertView and UIActionSheet

Previously, when you created UIAlertView objects or UIActionSheet objects,
you needed to keep a reference to the object in a field or some structure to
prevent the instances from being garbage collected. For example, this code could
randomly fail depending on whether the Garbage Collector ran or not:

```
view plainprint?
var a = new UIActionSheet (...);  
a.Clicked += delegate {... }
```

In the above example, since the variable is a local variable (a is no longer
referenced when the function terminates) the Garbage Collector could release the
value of "a" before the user gets a chance to interact with the view.

With this release, when you use C# events to configure your UIActionSheet or
UIAlertView, the runtime will automatically keep a reference to the object and
release it when the view is dimissed.

 <a name="CoreData_APIs" class="injected"></a>


# CoreData APIs

The CoreData APIs came from the contributions done to MonoMac from the
Mono-OSX community and are now included with MonoTouch as well. These provide
access to the Objective-C APIs that support CoreData.
