---
id: 72C1079A-4672-9353-128C-9C0ECA47E2A7
title: "MonoTouch 1.4.6"
---

&nbsp;

 <a name="New_APIs:" class="injected"></a>


# New APIs:

-  Added NSIndexSet


-  Added NSHttpCookie


-  Added NSHttpCookieStorage


-  Added NSMutableDictionary


-   NSDictionary now has constructors in addition to factory methods.

 
-  CLLocation constants for accuracy.


-   Added factory overloads for NSIndexPath (Create (int []) and Create (uint []).

 
-   Added Runtime.StartWWAN (Uri uri) API for developers to explicitly awake the WWAN

 


 <a name="API_fixes:" class="injected"></a>


# API fixes:

-   UITableViewDelegate and UITableViewSource's AccessoryForRow and EditingStyleForRow return types are now enums instead of integer values.

 
-   AVAudioRecorder and AVAudioSession APIs exposed a few entrypoints that returned errors, but we were discarding them.

 
-   AVAudioRecorder now must be created with the factory method ToUrl

 
-   Fixed Full AOT compiler to handle Marshalling structs with enums.

 
-   Fixed FromObjectsAndKeys method (it never worked).

 
-   Fixed UITableView (Insert|Delete|Reload)Sections to take a NSIndexSet

 
-  Fixed linker handing of managed resources


-   Fixed CGImage.ScreenImage binding to return a valid image

 
-  Fixed WebClient to properly wake up WWAN


-  Fixed memory leak in CGImage




 <a name="General_fixes:" class="injected"></a>


# General fixes:

-   The btouch command will now preserve enum return values for method invocations.
