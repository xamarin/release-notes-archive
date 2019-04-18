---
id: E5C9BBDF-AA79-C58B-C544-9BCD8D3BF993
title: "MonoTouch 1.2 Beta 1"
---

&nbsp;

The beta for MonoTouch 1.2 is now available for developers interested in
trying out the upcoming features in MonoTouch. This is a beta release, not a
fully tested release, we are doing this release to give users early access to
the new debugging support in MonoTouch.

 <a name="The_Software" class="injected"></a>


# The Software

The beta of MonoTouch 1.2 includes:

-  MonoDevelop debugging update.
-  MonoTouch 1.2 Beta 1: -   Trial edition
-   Full edition


 


To download the full edition, you will need to enter the email address that
you used to buy MonoTouch and the password is the activation code that you
received on the email when you purchased MonoTouch (notice that the password is
case sensitive).

 <a name="New_Features" class="injected"></a>


# New Features

-  Debugger, works on Simulator and Device (using Wifi)
-  C# binding generator for Objective-C Libraries.
-  stdout/stderr are now redirected from the device to MonoDevelop.


 <a name="MonoTouch_API_additions:" class="injected"></a>


# MonoTouch API additions:

-  UITableView now has a new property "Source" that allows a new UITableViewSource type to be assigned to it, it is a Model that implements both the UITableViewDelegate and the UITableViewDataSource, this should reduce clutter in existing code. Brent has written a  [detailed update](http://www.codesnack.com/blog/2009/11/2/uitableviewcontroller-uitvc-template-updated-for-uitableview.html) on using the UITableView with this new property. 
-  NSTimer.Dispose will now call Invalidate first, and then dispose the timer. 
-  UIActionSheet now can be initialized like this: -   new UIActionSheet ("Title") { "Help", "Open in Browser", "Bookmark" } 


 
-  Added NSKeyedArchiver, NSKeyedUnarchiver.
-  Added Encoder virtual method on NSObject.
-  NSData and NSMutableData now have indexers.
-  Added ShouldHandleCookies setter to NSMutableUrlRequest.
-  Made Class:.ctor(IntPtr) public for the binding generator


 <a name="Mono_Runtime_API_additions:" class="injected"></a>


# Mono Runtime API additions:

-  Added System.Timers.Timer
-  Added System.Threading.Semaphore
-  Added System.Threading types to System.dll


 <a name="API_fixes" class="injected"></a>


# API fixes

Updated OpenTK to r2350.

-  This fixes some function overloads so that they're usable.
-  Binary serialization should now work, we disabled the Reflection.Emit based serializer and replaced it with a pure reflection-based one. 
-  Fixed AVAudioPlayer factory methods to be static.
-  Fixed typo in UITableView.DidEndEditing
-  Fixed typo in AVAudioRecorder.Pecord -&gt; Record
-  Fixed BadgeValue to allow null
-  The helper class NSNotificationHandler is no longer public.
-  Flagged a NSString.DataUsingEncoding as Obsolete, introduced instead Encode methods. 
-  Fixed UIControl and UILabel Hilighted typo to Highlighted.
-  Fixed the MFMailComposeViewController's delegate handler.


 <a name="" class="injected"></a>


#  **System.Data** [ <span class="icon"><img src="monotouch_1.2_beta_1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_1/MonoTouch_1.2_Beta_1#)

A preview of the System.Data and SQLite for MonoTouch is now available.

-  Mono.Data.Sqlite.dll: unchanged. Note that this binding is against SQLite 3.6, while iPhone has SQLite 3.0, so use of some functionality will result in EntryPointNotFoundExceptions. Such missing functionality appears to include DataSet support. 
-  Mono.Data.Tds.dll: unchanged.
-  System.Data.dll: Removes code-generation capabilities (System.Data.TypedDataSetGenerator), .config handling support, System.Data.Common.DbProviderFactories, System.Data.OleDb, System.Data.Odbc. -   System.Data.SqlClient  *is*  present. 


 
-  System.Transactions.dll: unchanged.


 <a name="" class="injected"></a>


# Fixes [ <span class="icon"><img src="monotouch_1.2_beta_1/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_1/MonoTouch_1.2_Beta_1#)

-  Fixed crash using async socket operations
-  Fixed i18n in mtouch (Please provide documentation!)
-  iPhoneOSGameView.Run() will no longer truncate the timeout to have 1ms resolution. It will now have 100ns resolution. 
-  Fixed crash with multi-threaded apps that could break the app on startup on 3G phones.
