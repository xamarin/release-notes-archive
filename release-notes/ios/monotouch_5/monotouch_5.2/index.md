---
id: 89750B3A-049C-EE1D-7315-05E8897E1816
title: "MonoTouch 5.2"
---

<a name="New_features_in_MonoTouch_5.2" class="injected"></a>


## New features in MonoTouch 5.2

-   **Automatically starting and stopping applications on device**   
    
 MonoTouch will now start and stop your applications on device when running or debugging without any user intervention.   
    
 
-   **Memory Profiler**   
    
 A new memory profiler is now part of MonoDevelop and MonoTouch and allows developers to track managed objects memory usage, growth and track which objects are still referenced and where they are being referenced from.  [Check our tutorial](/guides/ios/application_fundamentals/monotouch_profiler) for a step-by-step guide on using it.   
    
 
-   **OpenTK 1.0**   
    
 We have updated OpenTK -- the OpenGL binding to C# to version 1.0.   
    
 
-   **Updated MonoDevelop**   
    
 The new MonoDevelop features a faster debugging interface to MonoTouch and fixes many of the reported problems. 


 <a name="New_APIs_in_MonoTouch_5.2" class="injected"></a>


## New APIs in MonoTouch 5.2

-   ** [MonoTouch.Dialog](http://github.com/migueldeicaza/MonoTouch.Dialog)is now part of MonoTouch**   
    
 The popular library that helps developers quickly develop user interfaces with MonoTouch is now part of the . The version included with MonoTouch is named MonoTouch.Dialog-1.dll, to avoid conflicts with any existing uses your application might already have.   
    
 
-   [ **Unit testing framework**](/guides/ios/application_fundamentals/unit_testing)   
    
 We have introduced a new unit testing framework for MonoTouch applications called  [Touch.Unit](http://spouliot.wordpress.com/2011/09/28/unit-testing-and-monotouch/)   
    
 
-   ** [System.Numerics](http://msdn.microsoft.com/en-us/library/system.numerics)library**   
    
 This library contains the big integer and complex data types.   
    
 
-   ** [System.IO.MemoryMappedFiles](http://msdn.microsoft.com/en-us/library/system.io.memorymappedfiles.aspx)**   
    
 Developers can now map files into their address space using the standard .NET MemoryMappedFiles APIs.   
    
 
-   ** [Generation Garbage Collector](http://www.mono-project.com/Generational_GC)**   
    
 Mono's Generation Collector works on this release and it is the foundation for both our new memory profiler and will be the foundation for a new and improved memory management system (details below).   
    
 
-   **Linker Improvements** -   Backing Fields: reduces the sizes of managed objects that wrap native Objective-C libraries. 
-    [Serialization](http://spouliot.wordpress.com/2011/11/12/linker-vs-serialization/)  : [DataMember] and [Xml*] attributes will preserve fields in classes.   
     
  


 
-   **Parallel LINQ preview**   
    
 We are previewing the Parallel LINQ APIs on this release. There a handful of limitations imposed by the lack of JITing on iOS. We will be incrementally improving our Parallel LINQ preview to remove the iOS limitations.   
    
 
-   **Support SDKs installed in different prefixes.**   
    
 MonoTouch can now use different Apple SDKs installed in different system prefixes. This can be configured from MonoDevelop's  *Option* dialog in the  *SDK Location* tab.   
    
 
-   **Updated MonoTouch APIs**   
    
 For a detailed list for the updates in MonoTouch's APIs and the new iOS APIs that are exposed in this release see our API changes document. 


 <a name="" class="injected"></a>


## iOS Specific Updates [ <span class="icon"><img src="monotouch_5.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/MonoTouch_5.2#)

-   **iCloud Skip Backup**   
    
 Support for iOS 5.0.1's skip file from being backed up to iCloud (Use NSFileManager class's new SetSkipBackupAttribute and GetSkipBackupAttribute) 


-   **NSMutableArray is exposed.**   
    
 We advise users to avoid using this collection in public APIs, just like it should be avoided in public APIs in Objective-C. We are exposing it merely because some badly designed third-party APIs require it. But it should in general be avoided.   
    
 
-   **Improved diagnostics**   
    
 We have improved the diagnostics for objects that have been garbage collected. 


 <a name="OpenTK_Upgrade" class="injected"></a>


## OpenTK Upgrade

With this release, we updated the OpenTK stack to version 1.0. This brings
several bug fixes and improvements to OpenTK, but also introduces a couple of
source-code level incompatible changes:

These two methods:

```
Vector3 Vector3.Transform(Vector3, Matrix4)
Vector3d Vector3d.Transform(Vector3d, Matrix4d)
```

have changed return type (they return Vector4 and Vector4d, respectively,
now). There is another Transform overload that can be used to get the old
behavior:

```
void Vector3.Transform (ref Vector3, ref Matrix4, out Vector3)
void Vector3d.Transform (ref Vector3, ref Matrix4, out Vector3d)
```

These new overloads are also available in the latest stable version of
MonoTouch, so you can use the new overloads and still be backwards
compatible.

 <a name="New_Reference_Counting_System" class="injected"></a>


## New Reference Counting System

This version features a *preview* of our new reference counting system
that developers can enable to remove a series of problems that have existed
historically in MonoTouch.

To enable this new Reference Counting System, you must be using Mono's SGen
Garbage Collector, and pass the "--new-refcount" flag in "Additional mtouch
arguments" in your iPhone Build project tab.

Historically there have been two kinds of objects managed by MonoTouch: those
that were merely a wrapper around a native object (peer objects) and those that
extended or incorporated new functionality (derived objects) usually by keeping
extra in-memory state. Before it was possible that we could augment a peer
object with state (for example by adding a C# event handler) but that we let the
object go unreferenced and then collected. This would cause a crash later
on.

This new system automatically upgrades peer objects into objects that are
managed by the runtime when they store any extra information.

This new setup solves various crashes that happened in situations like
this:

```
class MyTableSource :UITableViewSource {
   …
   public override UITableViewCell GetCell (UITableView tableView, NSIndexPath indexPath) {
        var cell = tableView.DequeueReusableCell ("myId");
        if (cell != null)
                return cell;

        cell = new UITableViewCell (UITableViewCellStyle.Default, "myId");
        var txt = new UITextField ();
        txt.TouchDown += delegate { Console.WriteLine ("...."); };
        cell.ContentView.AddSubview (txt);
        return cell;
   }
}
```

This code will crash because cell becomes collectible and so its delegate,
which will translate into a dangling pointer.

 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

This release contains an extensive set of bugs that have been fixed in the
past few months and vastly improves memory usage and reduces the retention of
memory that was caused in some multi-threaded scenarios using web services.

 <a name="MonoTouch_5.2.4" class="injected"></a>


#  [MonoTouch 5.2.4]()

 <a name="New_features" class="injected"></a>


## New features

-  Avoid created unrequired backing fields on [Model] decorated types
-  Bug Fixes


 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

-  Bug #3303: Fix possible NRE when using [LinkWith] attributes
-  Ignore UnauthorizedAccessException on Console.WriteLine
-  Fix selector names typos for NSFilePresenter
-  Bug #3275: Fix Thumb2 support when using LLVM
-  Bug #3189: Fix references to modal views
-  Bug #3286: Marshalling of out NSError parameters
-  HtmlElement sizing fix in MonoTouch.Dialog


 <a name="MonoTouch_5.2.5" class="injected"></a>


#  [MonoTouch 5.2.5]()

This release adds support for Xcode 4.3

 []() []() []() []()

 <a name="MonoTouch_5.2.9" class="injected"></a>


# MonoTouch 5.2.9

This is a new stable release, the changes include:

 <a name="" class="injected"></a>


### New Features [ <span class="icon"><img src="monotouch_5.2/Images/icon-trans.gif"></span>](/releases/ios/monotouch_5/monotouch_5.2)

-  MonoTouch.Dialog now ships with JsonElement to create user interfaces from Json data 
-  Some ViewControlles now implement the UIAppearance protocol, this was previously missing: ABPeoplePickerNavigationController, EKEventEditViewController, GKLeaderboardViewController, GKAchievementViewController, GKFriendRequestComposeViewController, GKTurnBasedMatchmakerViewController, MFMailComposeViewController and MFMessageComposeViewController ( [3226](https://bugzilla.xamarin.com/show_bug.cgi?id=3226) ) 
-  Better error reporting from the [LinkWith] attribute, it now issues warnings/errors if no matching architecture is available on the embedded package. ( [3597](https://bugzilla.xamarin.com/show_bug.cgi?id=3597) ) 
-  Added .NET-style APIs to create NSHttpCookies instead of requiring NSDictionary APIs ( [3603](https://bugzilla.xamarin.com/show_bug.cgi?id=3603) ) 
-  Introduces support for iOS 5.1 APIs
-  Introduces support for the new "Skip backup" flag on documents on iOS 5.1 ( [NSFileManager.SetSkipBackupAttribute](http://iosapi.xamarin.com/?link=M%3aMonoTouch.Foundation.NSFileManager.SetSkipBackupAttribute(System.String%2cSystem.Boolean)) ). 
-  Introduces strongly typed UIImagePickerMediaPickedEventArgs method accessors for easily picking media selected, media types and any user-edited media. 


 <a name="" class="injected"></a>


### Bug Fixes: [ <span class="icon"><img src="monotouch_5.2/Images/icon-trans.gif"></span>](/releases/ios/monotouch_5/monotouch_5.2)

-  Fix (again) references to modal views  [3189](https://bugzilla.xamarin.com/show_bug.cgi?id=3189) ,  [3489](https://bugzilla.xamarin.com/show_bug.cgi?id=3489) 
-  Stack traces contain numbers, even when not running in debug mode  [3357](https://bugzilla.xamarin.com/show_bug.cgi?id=3357) 
-  Can't set CAShapeLayer Color and Path properties to null  [3579](https://bugzilla.xamarin.com/show_bug.cgi?id=3579) 
-  Fixes CIVector constructor when passing array of floats
-  Add supports for more cases of LINQ's FirstOrDefault  [#3710](https://bugzilla.xamarin.com/show_bug.cgi?id=3710) . 
-  Improves AOT support for some generic uses  [#3285](https://bugzilla.xamarin.com/show_bug.cgi?id=3285) . 
-  Allow null to be passed to various CGImageSource APIs  [3717](https://bugzilla.xamarin.com/show_bug.cgi?id=3717) 
-  Avoids keeping a reference when accessing UIGestureRecognizer.View  [#3359](https://bugzilla.xamarin.com/show_bug.cgi?id=3359) 
-  Add new Animation/Transition overloads that were removed in the 5.2.6 beta. 


 <a name="" class="injected"></a>


### Other Changes [ <span class="icon"><img src="monotouch_5.2/Images/icon-trans.gif"></span>](/releases/ios/monotouch_5/monotouch_5.2)

-  Fix API signature for ArchiveRootObjectToFile
-  Look for `strip` and `dsymutil` in more places for people who installed Xcode 4.3 without the "Command-Line Tools"; 
-  Link all default type converters when System.Component.TypeDescriptor is used. 


 <a name="Detailed_API_changes" class="injected"></a>


### Detailed API changes

 [From 5.2.5 to 5.2.9](/ios/releases/api_changes/from_5.2.5_to_5.2.9) [ ![](monotouch_5.2/Images/icon-trans.gif)](/releases/ios/monotouch_5/monotouch_5.2)

 <a name="<a_name=" 10"_href="" _id="10">MonoTouch_5.2.10</a>


" class="injected">#  [MonoTouch 5.2.10]()

 <a name="Bug_Fixes" class="injected"></a>


### Bug Fixes

-  WCF supports serializing nullable enums (#2843)
-  Fix for HttpWebRequest and NTLM (#3894)
-  Fix regression in UIView.Animate when a null completion was passed
-  UIPopoverController now references the ContentViewController
-  UIAppearance.WhenContainedIn is no longer ambiguous with user-defined classes 


 <a name="<a_name=" 11"_href="" _id="11">MonoTouch_5.2.11</a>


" class="injected">#  [MonoTouch 5.2.11]()

 <a name="Changes_in_MonoTouch" class="injected"></a>


### Changes in MonoTouch

-  Added missing selectors to QLPreviewControllerDelegate (FrameForPreviewItem and TransitionImageForPreviewItem) 
-  CALayer.Contents can now be set to null.
-  Binding of NSString static fields is no longer limited to the MonoTouch namespace ( [#4333](https://bugzilla.xamarin.com/show_bug.cgi?id=4333) ) 
-  Brings missing methods to the UITextField and UITextView from the protocols they adopt 
-  Added more NSString overloads (StringSize and DrawString)
-  CoreAnimation's CALayer.Convert methods now allow a null to be specified for the layer ( [#4181](https://bugzilla.xamarin.com/show_bug.cgi?id=4181) ) 
-  Faster string marshaling (5%)
-  UIControl.CancelTracking can now take a null parameter


 <a name="Fixes_in_MonoTouch" class="injected"></a>


### Fixes in MonoTouch

-  HeapShot profiler has been fixed (before, it could fail when grabing the data from the target) 
-  Fixes enumeration values for AVCaptureVideoOrientation.
-  Fixes the return value for UIApplicationDelegate.HandleOpenURL (now it is a bool) 
-  Fix IsolatedStorage's GetUserStoreForApplication ( [#4101](https://bugzilla.xamarin.com/show_bug.cgi?id=4101) ) 
-  Fixes HttpWebRequest chunked reader for some comet requests ( [#3876](https://bugzilla.xamarin.com/show_bug.cgi?id=3876) ) 
-  WebClient now raises UploadProgressChanged when uploading a file ( [#3100](https://bugzilla.xamarin.com/show_bug.cgi?id=3100) ) 
-  Fixed NSUrlProtocol to work
-  Fixes Path.Canonicalize to not canonicalize the root path to an empty string 
-  Fixes Aes.Create
-  Performance optimization to SHA224
-  Fixes builds when time stamp changes ( [#2699](https://bugzilla.xamarin.com/show_bug.cgi?id=2699) ) 
-  UIViewController.PresentViewController allows a null completion handler
-  UIButton.SetImage and SetBackgroundImage can now set the images to null
-  Fixes an overload of NSString.DrawString to return the actual font size used ( [#4197](https://bugzilla.xamarin.com/show_bug.cgi?id=4197) ) 
-  Fixes marshaling of some byref/out parameters ( [#3992](https://bugzilla.xamarin.com/show_bug.cgi?id=3992) ) 
-  Fixes UIColor.GetHSBA so the values can roundtrip with UIColor.FromHSBA


 <a name="Changes_in_MonoTouch.Dialog:" class="injected"></a>


### Changes in MonoTouch.Dialog:

-  Fixes multiline elements in MonoTouch.Dialog ( [#3529](https://bugzilla.xamarin.com/show_bug.cgi?id=3529) ,  [#4132](https://bugzilla.xamarin.com/show_bug.cgi?id=4132) ) 
-  DateTimeElement now assumes that the DateKind is unspecified, to address timezone problems ( [#3983](https://bugzilla.xamarin.com/show_bug.cgi?id=3983) ) 
-  Improved PickerElement, added ClearButtonMode, events to raise on changes. 
-  EntryElements now will automatically fetch the contents of the entry line without requiring a FetchValue() call, or a focus change. 
-  Fix for arrays of BooleanElements not responding ( [#3970](https://bugzilla.xamarin.com/show_bug.cgi?id=3970) ) 
-  Date elements now raise a DateSelected event


 <a name="Minor_Changes" class="injected"></a>


### Minor Changes

-  Touch.Unit now reports the status of execution on the console at the end. 
-  Touch.Server now reports failures when running unit tests.
-  Touch.Unit now renders messages using multiple lines.
-  Fix the Assert.Ignore in NUnitLite


 <a name="Detailed_API_Changes" class="injected"></a>


### Detailed API Changes

You can browse the detailed API changes between [MonoTouch 5.2.10 and MonoTouch 5.2.11](/releases/ios/api_changes/from_5.2.10_to_5.2.11)   
   


 <a name="<a_name=" 12"_href="" _id="12">MonoTouch_5.2.12</a>


" class="injected">#  [MonoTouch 5.2.12]()

 <a name="Changes_in_MonoTouch" class="injected"></a>


### Changes in MonoTouch

-  Any class decorated with StructLayout attribute is now automatically [Preserved], it is no longer necessary to set this manually (x#5034). 
-  Added UTType constants, with the known values for all Uniform Type Identifiers in iOS (x#4988) 
-  Added setters to the UISlider appearance class.
-  Improved compatibility with Portable Library Projects.
-  Allows null in various SetBackgroundImage calls.
-  New UIView.StringSize method
-  Provides warnings to users trying to use .NET 4.0 binaries in MonoTouch.
-  Added a couple of protocol methods from AVAsynchronousKeyValueLoading to AVAsset 
-  Added support for WCF FaultException&lt;tdetail&gt; (x#1437, x#2859)
-  Added CGColorSpace.GetColorTable
-  Added new CGGradient constructors
-  We now use Mono in LARGE_FILE_SUPPORT configuration (x#4238)


 <a name="Fixes_in_MonoTouch" class="injected"></a>


### Fixes in MonoTouch

-  Fix for DateTime.ParseExact (x#922, x#5160)
-  Fix the designer when used in Turkish locales (x#5101)
-  Fix ForeignKeyConstraint enforced on deleted rows in System.Data (n#650402) 
-  Fix for SqliteClient.SqliteDataReader to honor CommandBehavior.CloseConnection (x#5058) 
-  NSHttpCookie now uses the path argument, to bridge HttpCookie and NSHttpCookie (x#4990) 
-  Fixes GLKBaseEffect invocations that take vectors (x#5053)
-  Fixes AudioUnit callbacks on device (x#5034)
-  NSUrlConnection.Schedule now takes an NSString argument, instead of a string, since it is treated as an internal token. 
-  CFProxy will not crash, in case some keys are not present in the Proxy configuration (#4784, #4715) 
-  Fixes rendering of NSUrl objects in the debugger when the AbsoluteString is null. 
-  Fixes HttpWebRequest support for keep-alive requests when streaming (x#4669) 
-  Fixes CTFrame's retention of its CGPath (x#4677)
-  Fixes NetworkInterface.GetAllNetworkInterfaces (x#4631)
-  Fixed a bug in the alpha bits for NewRefCount (x#4572)
-  Plugged leaks for CFNetwork.GetSystemProxySettings and SecPKCS12Import.
-  Plugged leak when Mono.Data.SqliteClient returned an error.
-  Fixes the return value for UIApplicationDelegate.OpenUrl
-  Fix https support for CFNetwork+CFWebProxy (x#4488)
-  LocalizedString now allows null parameters
-  Fix System.Json parser for negative exponential values (x#4415)
-  CoreAnimation AnimationTimingFunction and CompletionBlock can now take null values (#4393) 
-  Fix definition for BackgroundColor, to allow overriding the method (x#4414) 
-  PresentViewController and DimissViewController now allow null callbacks (x#4393) 
-  Fix CGPDFStream.Data property.


 <a name="Fixes_in_MonoTouch.Dialog" class="injected"></a>


### Fixes in MonoTouch.Dialog

-  Fixed EntryElement editing in password mode and edit in the middle of the text (x#4972, x#4736) 
-  Fixed rendering of StyledStringElement (x#3976)


 <a name="Detailed_API_Changes" class="injected"></a>


### Detailed API Changes

You can browse the detailed API changes between [MonoTouch 5.2.11 and MonoTouch 5.2.12](/releases/ios/api_changes/from_5.2.11_to_5.2.12)

 <a name="MonoTouch_5.2.13" class="injected"></a>


# MonoTouch 5.2.13

 <a name="Changes_in_MonoTouch" class="injected"></a>


### Changes in MonoTouch

-  Add INotifyPropertyChanging (bug #5337)
-  Add UIAppearance support for UISlider.[Min|Max]ValueImage 


 <a name="Fixes_in_MonoTouch" class="injected"></a>


### Fixes in MonoTouch

-  #242 DataContractSerializer fails to deserialize List&lt;T&gt; properties 
-  #992/#5160 Fix DateTime.[Try]ParseExact 
-  #1553 Fix NRE in WebConnection[Stream] 
-  #4721 Fix Guid.CompareTo returning wrong result 
-  #5058 Fix "Unable to open the database file" in sqlite 
-  #5199 Fix UIWindow.IsKeyWindow binding 
-  #5200 System.Reflection.Pointer is now preserved by the linker 
-  #5216/#5218 Fix AVAssetImageGenerator bindings 
-  #5311 Fix LockRecursionException (defined in mscorlib and System.Core) 
-  #5410 AudioUnit Dispose method throws EntryPointNotFound exception 
-  #5543 Fix linking of properties/fields using generics wrt XML serialization 
-  #5546 Fix ServicePointManager.ServerCertificateValidationCallback 
-  #5567 Enum.ToString behaves incorrectly in corner cases 
-  #5581 Remove null checks on UIDatePicker 
-  #5610 Fix typo in ADInterstitialAdDelegate.AdUnloaded selector 
-  #5615 Fix NSFileCoordinatorWritingOptions missing ForReplacing 
-  #5805 Fix wrong type in signature for CMMotionManager.StartDeviceMotionUpdates 
-  #5696/#5803/#5808 Allow null for a few CoreBluetooth.CBCentralManager API 
-  #5898 Allow null for a few UIButton properties 
-  #6086 GKSession's ctor can take a null sessionID or displayName 
-  #6118 Linker now preserve MonoIOStat structure 
-  #6203 Accept spaces in the framework directory name 
-  Add System.Service.FaultException`1 ctor 
-  Fixed GKMatch.PlayersIDs selector typo 
-  #650402 ForeignKeyConstraint enforced on deleted rows 


 <a name="Detailed_API_Changes" class="injected"></a>


### Detailed API Changes

You can browse the detailed API changes between [MonoTouch 5.2.12 and MonoTouch 5.2.13](/releases/ios/api_changes/from_5.2.12_to_5.2.13)
