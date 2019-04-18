---
id: B98AA696-A9E0-C676-4E05-CA7350206904
title: "MonoTouch 5.1"
---

&nbsp;

MonoTouch 5.1 is the series of beta releases that will culminate with
MonoTouch 5.2, our next stable release. [ <span class="icon"><img src="monotouch_5.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/MonoTouch_5.1#)

-   [MonoTouch.Dialog](http://github.com/migueldeicaza/MonoTouch.Dialog) library is now part of MonoTouch   
    
 The version included with MonoTouch is named MonoTouch.Dialog-1.dll, to avoid conflicts with any existing uses your application might already have. 
-  Unit testing framework  [Touch.Unit](http://spouliot.wordpress.com/2011/09/28/unit-testing-and-monotouch/) to create unit tests for your MonoTouch applications. 
-   [System.Numerics](http://msdn.microsoft.com/en-us/library/system.numerics) library that contains BigInt and Complex data types. 
-   [System.IO.MemoryMappedFiles](http://msdn.microsoft.com/en-us/library/system.io.memorymappedfiles.aspx) 
-  New MapKit APIs
-   [Our Generation Collector](http://www.mono-project.com/Generational_GC) now works. 
-  Linker Improvements: -   Backing Fields: reduces the sizes of managed objects that wrap native Objective-C libraries. 
-    [Serialization](http://spouliot.wordpress.com/2011/11/12/linker-vs-serialization/)  : [DataMember] and [Xml*] attributes will preserve fields in classes. 


 
-  Parallel LINQ preview   
    
 Notice that there are some limitations due to Generics that we will be improving on future releases 


There are some other features in MonoTouch that require updates on the IDE
side to work, but are present on the runtime: Memory Profiling support and
templates for MonoTouch.Dialog uses.

You can review the API changes from 5.0 to 5.1 in our Beta 5.1 Changes.

 <a name="Changes_in_MonoTouch_5.1.1" class="injected"></a>


# Changes in MonoTouch 5.1.1

This release brings the same fixes that were made to the stable 5.0.3 release
to the beta release.

Added:

-  Support for iOS 5.0.1's skip file from being backed up to iCloud
-  Bring a monotonic Stopwatch to iOS. Fix #1366
-  Added new iOS5 AudioSession properties (Mode, OverrideCategoryDefaultToSpeaker, OverrideCategoryEnableBluetoothInput) 
-  Added NSFileWrapper APIs for iCloud package storage


Bug fixes:

-  Add missing constructors to MapKit
-  Fixes the bindings for ALAssetsLibrary.WriteImageToSavedPhotosAlbum (bug #2166). 
-  Registrar fixes for callback methods that use out or ref parameters
-  Fixes UIAppearance.WhenFoundIn API (bug #1978)
-  Fixes UIAppearance to work with subclasses
-  Fixes SQLite leak
-  Fixes iCloud callbacks


Unique Features for the Beta:

-  Updated MonoTouch.Dialog to the latest version from GitHub.
-  System.IO.MemoryMappedFiles that were previously announced are actually integrated (due to a mistake, 5.1.0 did not include the binding, it is now in this release). 
-  Various components under the covers that are required for the upcoming MonoDevelop UI. 


 <a name="Changes_in_MonoTouch_5.1.2" class="injected"></a>


# Changes in MonoTouch 5.1.2

 <a name="New_in_this_release:" class="injected"></a>


# New in this release:

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="monotouch_5.1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/MonoTouch_5.1#)

-  Updated OpenTK to version 1.0. This change can potentially break some user code. 
-  NSMutableArray is exposed. We advise users to avoid using this collection in public APIs, just like it should be avoided in public APIs in Objective-C. We are exposing it merely because some badly designed third-party APIs require it. But it should in general be avoided. 
-  Improved diagnostics for objects that have been garbage collected.
-  MKPoly[line|gon] inherit read/write [Sub]Title properties from MKShape.


 <a name="OpenTK_Upgrade" class="injected"></a>


# OpenTK Upgrade

With this release, we updated the OpenTK stack to version 1.0. This brings
several bug fixes and improvements to OpenTK, but also introduces a couple of
source-code level incompatible changes:

These two methods:

-  Vector3 Vector3.Transform(Vector3, Matrix4)
-  Vector3d Vector3d.Transform(Vector3d, Matrix4d)


have changed return type (they return Vector4 and Vector4d, respectively,
now). There is another Transform overload that can be used to get the old
behavior:

-  void Vector3.Transform (ref Vector3, ref Matrix4, out Vector3)
-  void Vector3d.Transform (ref Vector3, ref Matrix4, out Vector3d)


These new overloads are also available in the latest stable version of
MonoTouch, so you can use the new overloads and still be backwards
compatible.

 <a name="New_Reference_Counting_System" class="injected"></a>


# New Reference Counting System

This version features a new reference counting system that developers can
enable to remove a series of problems that have existed historically in
MonoTouch.

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


# Bug Fixes

-  Memory leak fixes when using the ThreadPool and the Web stack (#2619, #386, #2473), some manifestations of the bug: -   Memory leak when WebClient's async APIs were used 
-   Memory leak with WCF clients
-   Memory leak when the WebClient was used on background threads.


 
-  Fix crasher for ABPerson.SetUrl (#2728)
-  UITabBarItem.SelectedItem can now be assigned the null value
-  Bring Mono fixes to ObservableCollection
-  Fixes NSDistributedNotificationCenter methods to allow nulls.
-  CALayer's DefaultActionForKey, ActionForKey, ActionForLayer and Actions now return NSObjects instead of CAAction, since not more types than those that implement CAAction directly support this (#2441) 
-  CALayer.Mask can now be assigned the null value (#2310)
-  NSFileManager.GetUrlForUbiquityContainer can now take a null value (#2354). 
-  UIImage.Size is now readonly (#2757)
-  UIBarButtonItem.CustomView can now be assigned the null value (#2766)
-  UIApplication.BackgroundTaskInvalid is an int, not a string (#2661)
-  Fix value of UIViewAutoresizing.All (#2706)
-  UIViewController.DisablesAutomaticKeyboardDismissal is a getter only (#2713) 
-  Better diagnostics for readonly Sqlite databases.
-  Add Export support for static properties (#2443)
-  Fixes SGen+Release builds.
-  Fixes HitTest when used with UIAutomation (#2450)
-  The 5.0 ShouldHideViewController that should have been on the delegate class, was accidentally left on the class itself for UISplitViewController 
-  Fixed the creation of an NSAutoreleasePool (#2384)
-  Fix CFNetwork/WebRequest integration
-  Fixes the new application startup/shutdown introduced in the previous beta (#2371) 
-  Add MKOverlay and MKAnnotation support for MKPolygon (#2336)
-  Add missing setter on UISwitch.OnTintColor.
-  Fix a GC retention problem with SetLeftBarButtonItems and SetRightBarButtonItems 
-  Fix retrieving MAC address (#2010)
-  Fix WebClient.OnDownloadProgressedChanged (#2482) Fix support for read-only SQLite databases
