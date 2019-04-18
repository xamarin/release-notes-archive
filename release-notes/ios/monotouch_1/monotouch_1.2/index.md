---
id: 87A94A4B-7EBE-CD29-9CC5-5A3ED425CDBD
title: "MonoTouch 1.2"
---

<a name="New_Features" class="injected"></a>


# New Features

-  Debugger, works on Simulator and Device (using Wifi)
-  C# binding generator for Objective-C Libraries.
-  stdout/stderr are now redirected from the device to MonoDevelop.


 <a name="MonoTouch_API_additions:" class="injected"></a>


# MonoTouch API additions:

-  UITableView now has a new property "Source" that allows a new UITableViewSource type to be assigned to it, it is a Model that implements both the UITableViewDelegate and the UITableViewDataSource, this should reduce clutter in existing code. Brent has written a detailed update on using the UITableView with this new property. 
-  NSTimer.Dispose will now call Invalidate first, and then dispose the timer. 
-  UIActionSheet now can be initialized like this: -   new UIActionSheet ("Title") { "Help", "Open in Browser", "Bookmark" } 


 
-  Added NSKeyedArchiver, NSKeyedUnarchiver.
-  Added Encoder virtual method on NSObject


 <a name="Mono_Runtime_API_additions:" class="injected"></a>


# Mono Runtime API additions:

-  Added System.Timers.Timer
-  Added System.Threading.Semaphore
-  Added System.Threading types to System.dll


 <a name="API_fixes" class="injected"></a>


# API fixes

Updated OpenTK to r2350.

-  This fixes some function overloads so that they're usable
-  Fixed AVAudioPlayer factory methods to be static.
-  Fixed typo in UITableView.DidEndEditing
-  Fixed typo in AVAudioRecorder.Pecord -&gt; Record
-  Fixed BadgeValue to allow null
-  The helper class NSNotificationHandler is no longer public.
-  Flagged a NSString.DataUsingEncoding as Obsolete, introduced instead Encode methods. 


 <a name="" class="injected"></a>


#  **System.Data** [ <span class="icon"><img src="monotouch_1.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_1/MonoTouch_1.2#)

A preview of the [System.Data and SQLite for MonoTouch](http://ios.xamarin.com/Documentation/System.Data) is now available.

-  Mono.Data.Sqlite.dll: unchanged. Note that this binding is against SQLite 3.6, while iPhone has SQLite 3.0, so use of some functionality will result in EntryPointNotFoundExceptions. Such missing functionality appears to include DataSet support. 
-  Mono.Data.Tds.dll: unchanged.
-  System.Data.dll: Removes code-generation capabilities (System.Data.TypedDataSetGenerator), .config handling support, System.Data.Common.DbProviderFactories, System.Data.OleDb, System.Data.Odbc. -   System.Data.SqlClient  *is*  present. 


 
-  System.Transactions.dll: unchanged.


 <a name="Fixes" class="injected"></a>


# Fixes

-  Fixed crash using async socket operations
-  Fixed i18n in mtouch : read the documentation
-  iPhoneOSGameView.Run() will no longer truncate the timeout to have 1ms resolution. It will now have 100ns resolution.
