---
id: 4FAACD6A-18AB-7485-8B89-E3DCA3497283
title: "From 5.2.10 to 5.2.11"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.2.10";
```

Added:

```
public const string Version = "5.2.11";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureVideoOrientation" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureVideoOrientation

Fixed the values for LandscapeLeft and LandscapeRight

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSString

Added:

```
public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, MonoTouch.UIKit.UIFont font, float minFontSize, ref float actualFontSize, MonoTouch.UIKit.UILineBreakMode breakMode, MonoTouch.UIKit.UIBaselineAdjustment adjustment);
        public System.Drawing.SizeF StringSize (MonoTouch.UIKit.UIFont font, float minFontSize, ref float actualFontSize, float forWidth, MonoTouch.UIKit.UILineBreakMode lineBreakMode);
```

 <a name="Namespace:_MonoTouch.QuickLook" class="injected"></a>


# Namespace: MonoTouch.QuickLook

 <a name="New_Type:_MonoTouch.QuickLook.QLFrame" class="injected"></a>


## New Type: MonoTouch.QuickLook.QLFrame

```
[Serializable]
public delegate System.Drawing.RectangleF QLFrame (QLPreviewItem item, MonoTouch.UIKit.UIView view);
```

 <a name="Type_Changed:_MonoTouch.QuickLook.QLPreviewController" class="injected"></a>


## Type Changed: MonoTouch.QuickLook.QLPreviewController

Added:

```
public QLFrame FrameForPreviewItem {
                get;
                set;
        }
        public QLTransition TransitionImageForPreviewItem {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.QuickLook.QLPreviewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.QuickLook.QLPreviewControllerDelegate

Added:

```
public virtual System.Drawing.RectangleF FrameForPreviewItem (QLPreviewItem item, MonoTouch.UIKit.UIView view);
        public virtual MonoTouch.UIKit.UIImage TransitionImageForPreviewItem (QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

 <a name="New_Type:_MonoTouch.QuickLook.QLTransition" class="injected"></a>


## New Type: MonoTouch.QuickLook.QLTransition

```
[Serializable]
public delegate MonoTouch.UIKit.UIImage QLTransition (QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Removed:

```
public virtual void HandleOpenURL (UIApplication application, MonoTouch.Foundation.NSUrl url);
```

Added:

```
public virtual bool HandleOpenURL (UIApplication application, MonoTouch.Foundation.NSUrl url);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDocument" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDocument

Removed the public constructor, as it is not possible to create instances of
UIDocument like this.   
   
   
   
 Removed:

```
public UIDocument ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDocumentInteractionController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDocumentInteractionController

Added:

```
public virtual void DismissPreview (bool animated);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextField" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextField

It now implements the methods from base protocols that it adopts.   
   
   
   
 Added:

```
public virtual MonoTouch.Foundation.NSComparisonResult ComparePosition (UITextPosition first, UITextPosition second);
        public virtual void DeleteBackward ();
        public virtual void DictationRecognitionFailed ();
        public virtual void DictationRecordingDidEnd ();
        public virtual UITextWritingDirection GetBaseWritingDirection (UITextPosition forPosition, UITextStorageDirection direction);
        public virtual System.Drawing.RectangleF GetCaretRectForPosition (UITextPosition position);
        public virtual int GetCharacterOffsetOfPosition (UITextPosition position, UITextRange range);
        public virtual UITextRange GetCharacterRange (UITextPosition byExtendingPosition, UITextLayoutDirection direction);
        public virtual UITextRange GetCharacterRangeAtPoint (System.Drawing.PointF point);
        public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point);
        public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point, UITextRange withinRange);
        public virtual System.Drawing.RectangleF GetFirstRectForRange (UITextRange range);
        public virtual int GetOffsetFromPosition (UITextPosition fromPosition, UITextPosition toPosition);
        public virtual UITextPosition GetPosition (UITextPosition fromPosition, int offset);
        public virtual UITextPosition GetPosition (UITextPosition fromPosition, UITextLayoutDirection inDirection, int offset);
        public virtual UITextPosition GetPosition (UITextRange withinRange, int atCharacterOffset);
        public virtual UITextPosition GetPositionWithinRange (UITextRange range, UITextLayoutDirection direction);
        public virtual UITextRange GetTextRange (UITextPosition fromPosition, UITextPosition toPosition);
        public virtual MonoTouch.Foundation.NSDictionary GetTextStyling (UITextPosition atPosition, UITextStorageDirection inDirection);
        public virtual void InsertDictationResult (MonoTouch.Foundation.NSArray dictationResult);
        public virtual void InsertText (string text);
        public virtual void ReplaceText (UITextRange range, string text);
        public virtual void SetBaseWritingDirectionforRange (UITextWritingDirection writingDirection, UITextRange range);
        public virtual void SetMarkedText (string markedText, MonoTouch.Foundation.NSRange selectedRange);
        public virtual string TextInRange (UITextRange range);
        public virtual void UnmarkText ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextView

It now implements the methods from base protocols that it adopts.   
   
   
   
 Added:

```
public virtual MonoTouch.Foundation.NSComparisonResult ComparePosition (UITextPosition first, UITextPosition second);
        public virtual void DeleteBackward ();
        public virtual void DictationRecognitionFailed ();
        public virtual void DictationRecordingDidEnd ();
        public virtual UITextWritingDirection GetBaseWritingDirection (UITextPosition forPosition, UITextStorageDirection direction);
        public virtual System.Drawing.RectangleF GetCaretRectForPosition (UITextPosition position);
        public virtual int GetCharacterOffsetOfPosition (UITextPosition position, UITextRange range);
        public virtual UITextRange GetCharacterRange (UITextPosition byExtendingPosition, UITextLayoutDirection direction);
        public virtual UITextRange GetCharacterRangeAtPoint (System.Drawing.PointF point);
        public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point);
        public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point, UITextRange withinRange);
        public virtual System.Drawing.RectangleF GetFirstRectForRange (UITextRange range);
        public virtual int GetOffsetFromPosition (UITextPosition fromPosition, UITextPosition toPosition);
        public virtual UITextPosition GetPosition (UITextPosition fromPosition, int offset);
        public virtual UITextPosition GetPosition (UITextPosition fromPosition, UITextLayoutDirection inDirection, int offset);
        public virtual UITextPosition GetPosition (UITextRange withinRange, int atCharacterOffset);
        public virtual UITextPosition GetPositionWithinRange (UITextRange range, UITextLayoutDirection direction);
        public virtual UITextRange GetTextRange (UITextPosition fromPosition, UITextPosition toPosition);
        public virtual MonoTouch.Foundation.NSDictionary GetTextStyling (UITextPosition atPosition, UITextStorageDirection inDirection);
        public virtual void InsertDictationResult (MonoTouch.Foundation.NSArray dictationResult);
        public virtual void InsertText (string text);
        public virtual void ReplaceText (UITextRange range, string text);
        public virtual void SetBaseWritingDirectionforRange (UITextWritingDirection writingDirection, UITextRange range);
        public virtual void SetMarkedText (string markedText, MonoTouch.Foundation.NSRange selectedRange);
        public virtual string TextInRange (UITextRange range);
        public virtual void UnmarkText ();
```
