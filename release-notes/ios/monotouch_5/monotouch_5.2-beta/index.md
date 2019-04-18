---
id: 530F9959-DEE5-34A0-A740-3F58107AF73C
title: "MonoTouch 5.2-Beta"
---

&nbsp;

 <a name="MonoTouch_5.2.6" class="injected"></a>


#  [MonoTouch 5.2.6]()

This was a beta release.

 <a name="New_Features" class="injected"></a>


### New Features

-  MonoTouch.Dialog now ships with JsonElement to create user interfaces from Json data 
-  Some ViewControlles now implement the UIAppearance protocol, this was previously missing: ABPeoplePickerNavigationController, EKEventEditViewController, GKLeaderboardViewController, GKAchievementViewController, GKFriendRequestComposeViewController, GKTurnBasedMatchmakerViewController, MFMailComposeViewController and MFMessageComposeViewController ( [3226](https://bugzilla.xamarin.com/show_bug.cgi?id=3226) ) 
-  Better error reporting from the [LinkWith] attribute, it now issues warnings/errors if no matching architecture is available on the embedded package. ( [3597](https://bugzilla.xamarin.com/show_bug.cgi?id=3597) ) 
-  Added .NET-style APIs to create NSHttpCookies instead of requiring NSDictionary APIs ( [3603](https://bugzilla.xamarin.com/show_bug.cgi?id=3603) ) 


 <a name="Bug_Fixes:" class="injected"></a>


### Bug Fixes:

-   [3189](https://bugzilla.xamarin.com/show_bug.cgi?id=3189) ,  [3489](https://bugzilla.xamarin.com/show_bug.cgi?id=3489) : Fix (again) references to modal views 
-   [3357](https://bugzilla.xamarin.com/show_bug.cgi?id=3357) : Stack traces contain numbers, even when not running in debug mode 
-   [3579](https://bugzilla.xamarin.com/show_bug.cgi?id=3579) : Can't set CAShapeLayer Color and Path properties to null 


 <a name="Other_Changes" class="injected"></a>


### Other Changes

-  Fix API signature for ArchiveRootObjectToFile
-  Look for `strip` and `dsymutil` in more places for people who installed Xcode 4.3 without the "Command-Line Tools"; 
-  Link all default type converters when System.Component.TypeDescriptor is used. 


 <a name="Detailed_API_changes" class="injected"></a>


### Detailed API changes

-   [From 5.2.5 to 5.2.6](/releases/ios/api_changes/from_5.2.5_to_5.2.6) 


 <a name="MonoTouch_5.2.7" class="injected"></a>


#  [MonoTouch 5.2.7]()

 **MonoTouch 5.2.7 is currently available in the Beta channel**

 <a name="New_features" class="injected"></a>


## New features

-  Introduces support for iOS 5.1 APIs
-  Introduces support for the new "Skip backup" flag on documents on iOS 5.1 ( [NSFileManager.SetSkipBackupAttribute](http://iosapi.xamarin.com/?link=M%3aMonoTouch.Foundation.NSFileManager.SetSkipBackupAttribute(System.String%2cSystem.Boolean)) ). 
-  Introduces strongly typed UIImagePickerMediaPickedEventArgs method accessors for easily picking media selected, media types and any user-edited media. 


 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

-  Fixes CIVector constructor when passing array of floats
-  Add supports for more cases of LINQ's FirstOrDefault [#3710](https://bugzilla.xamarin.com/show_bug.cgi?id=3710) . 
-  Improves AOT support for some generic uses  [#3285](https://bugzilla.xamarin.com/show_bug.cgi?id=3285) . 
-  Allow null to be passed to various CGImageSource APIs  [3717](https://bugzilla.xamarin.com/show_bug.cgi?id=3717) 
-  Avoids keeping a reference when accessing UIGestureRecognizer.View  [#3359](https://bugzilla.xamarin.com/show_bug.cgi?id=3359) 
-  Add new Animation/Transition overloads that were removed in the 5.2.6 beta. 


 <a name="Detailed_API_changes" class="injected"></a>


## Detailed API changes

-  From  [5.2.6 to 5.2.7](/releases/ios/api_changes/from_5.2.6_to_5.2.7)
