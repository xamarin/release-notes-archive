---
id: 8244F9B5-19EE-7753-CD0E-DC64C36FDC40
title: "from 6.0.1 to 6.0.2"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "6.0.1";
```

Added:

```
public const string Version = "6.0.2";
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewController

Removed:

```
[Obsolete("Deprecated in IOS6")]
        public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);
```

Added:

```
[Obsolete("Deprecated in iOS6. Replace it with both GetSupportedInterfaceOrientations and PreferredInterfaceOrientationForPresentation")]
        public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);
```
