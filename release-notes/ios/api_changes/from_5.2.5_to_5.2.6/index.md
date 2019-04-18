---
id: 88DEEC5D-4DBB-BD13-B2AE-1436B705B6D5
title: "From 5.2.5 to 5.2.6"
---

API changes from MonoTouch 5.2.5 to MonoTouch 5.2.6 <a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.2.5";
```

Added:

```
public const string Version = "5.2.6";
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

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

Removed:

```
public static void Animate (double duration, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Animate (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Transition (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Transition (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction completion);
```

Added:

```
public static void Animate (double duration, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void Animate (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void Transition (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void Transition (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, UICompletionHandler completion);
```
