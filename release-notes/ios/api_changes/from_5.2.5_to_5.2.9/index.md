---
id: 3088D991-BB4B-B145-14CA-6A2A88CC338A
title: "From 5.2.5 to 5.2.9"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.2.5";
```

Added:

```
public const string Version = "5.2.9";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVError" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVError

Added:

```
InvalidOutputURLPathExtension
```

 <a name="Namespace:_MonoTouch.AddressBookUI" class="injected"></a>


# Namespace: MonoTouch.AddressBookUI

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController 

Added:

```
public static ABPeoplePickerNavigationControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static ABPeoplePickerNavigationControllerAppearance Appearance {
                get;
        }
        
        public class ABPeoplePickerNavigationControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetRepresentation" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetRepresentation

Added:

```
public virtual System.Drawing.SizeF Dimensions {
                get;
        }
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFormatType" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFormatType

Added:

```
MPEG4AAC_ELD_V2
```

 <a name="Namespace:_MonoTouch.CoreVideo" class="injected"></a>


# Namespace: MonoTouch.CoreVideo

 <a name="Type_Changed:_MonoTouch.CoreVideo.CVPixelFormatType" class="injected"></a>


## Type Changed: MonoTouch.CoreVideo.CVPixelFormatType

Removed:

```
CV4444AYpCbCr16
```

Added:

```
CV4444AYpCbCr16,
        OneComponent8,
        TwoComponent8
```

 <a name="Namespace:_MonoTouch.EventKitUI" class="injected"></a>


# Namespace: MonoTouch.EventKitUI

 <a name="Type_Changed:_MonoTouch.EventKitUI.EKEventEditViewController" class="injected"></a>


## Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Added:

```
public static EKEventEditViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static EKEventEditViewControllerAppearance Appearance {
                get;
        }
        
        public class EKEventEditViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSCachedUrlResponse" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCachedUrlResponse

Added:

```
public NSCachedUrlResponse (NSUrlResponse response, NSData data);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSHttpCookie" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSHttpCookie

Added:

```
public NSHttpCookie (string name, string value);
        public NSHttpCookie (string name, string value, string path);
        public NSHttpCookie (string name, string value, string path, string domain);
        public NSHttpCookie (System.Net.Cookie cookie);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSKeyedArchiver" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSKeyedArchiver

Removed:

```
public static NSData ArchiveRootObjectToFile (NSObject root, string file);
```

Added:

```
public static bool ArchiveRootObjectToFile (NSObject root, string file);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrl" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrl

Added:

```
public static NSString IsExcludedFromBackupKey {
                get;
        }
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementViewController

Added:

```
public static GKAchievementViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static GKAchievementViewControllerAppearance Appearance {
                get;
        }
        
        public class GKAchievementViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKFriendRequestComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Added:

```
public static GKFriendRequestComposeViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static GKFriendRequestComposeViewControllerAppearance Appearance {
                get;
        }
        
        public class GKFriendRequestComposeViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboardViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Added:

```
public static GKLeaderboardViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static GKLeaderboardViewControllerAppearance Appearance {
                get;
        }
        
        public class GKLeaderboardViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKTurnBasedMatchmakerViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Added:

```
public static GKTurnBasedMatchmakerViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static GKTurnBasedMatchmakerViewControllerAppearance Appearance {
                get;
        }
        
        public class GKTurnBasedMatchmakerViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Namespace:_MonoTouch.MessageUI" class="injected"></a>


# Namespace: MonoTouch.MessageUI

 <a name="Type_Changed:_MonoTouch.MessageUI.MFMailComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Added:

```
public static MFMailComposeViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MFMailComposeViewControllerAppearance Appearance {
                get;
        }
        
        public class MFMailComposeViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MessageUI.MFMessageComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added:

```
public static MFMessageComposeViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MFMessageComposeViewControllerAppearance Appearance {
                get;
        }
        
        public class MFMessageComposeViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Dlfcn" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Dlfcn

Added:

```
public static IntPtr dlsym (IntPtr handle, string symbol);
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="New_Type:_MonoTouch.UIKit.UIDictationPhrase" class="injected"></a>


## New Type: MonoTouch.UIKit.UIDictationPhrase

```
public class UIDictationPhrase : MonoTouch.Foundation.NSObject {
        
        public UIDictationPhrase ();
        public UIDictationPhrase (MonoTouch.Foundation.NSCoder coder);
        public UIDictationPhrase (MonoTouch.Foundation.NSObjectFlag t);
        public UIDictationPhrase (IntPtr handle);
        
        public virtual string [] AlternativeInterpretations {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string Text {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerMediaPickedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerMediaPickedEventArgs

Added:

```
public System.Nullable<System.Drawing.RectangleF> CropRect {
                get;
        }
        public UIImage EditedImage {
                get;
        }
        public string MediaType {
                get;
        }
        public MonoTouch.Foundation.NSUrl MediaUrl {
                get;
        }
        public UIImage OriginalImage {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISplitViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISplitViewController

Added:

```
public virtual bool PresentsWithGesture {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

Added:

```
public static void AnimateNotify (double duration, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void AnimateNotify (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void TransitionNotify (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void TransitionNotify (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, UICompletionHandler completion);
```
