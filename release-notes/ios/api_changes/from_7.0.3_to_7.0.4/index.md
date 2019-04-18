---
id: E69BB31A-033C-4C75-8EB2-72E292170695
title: "From 7.0.3 to 7.0.4"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string Version = "7.0.3";
```

Added fields:

```
public static const string Version = "7.0.4";
```

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGContextPDF

Added constructors:

```
public CGContextPDF (CGDataConsumer dataConsumer, System.Drawing.RectangleF mediaBox, CGPDFInfo info);
```

### New Type MonoTouch.CoreGraphics.CGDataConsumer

```
public class CGDataConsumer : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGDataConsumer (System.IntPtr handle);
	public CGDataConsumer (MonoTouch.Foundation.NSMutableData data);
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CGDataConsumer ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
```

## Namespace MonoTouch.ObjCRuntime

### New Type MonoTouch.ObjCRuntime.TransientAttribute

```
public class TransientAttribute : System.Attribute {
	// constructors
	public TransientAttribute ();
}
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.NSMutableParagraphStyle

Removed properties:

```
public override NSTextTab TabStops { get; set; }
```

Added properties:

```
public override NSTextTab[] TabStops { get; set; }
```

### Type Changed: MonoTouch.UIKit.NSParagraphStyle

Removed properties:

```
public virtual NSTextTab TabStops { get; set; }
```

Added properties:

```
public virtual NSTextTab[] TabStops { get; set; }
```

   


 <hr>
