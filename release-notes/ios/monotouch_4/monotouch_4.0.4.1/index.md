---
id: 7F9EC017-ACB8-50A7-5F25-012E2587B38B
title: "MonoTouch 4.0.4.1"
---

The MonoTouch 4.0.4.1 was the first release of MonoTouch done by Xamarin.
This release included the following changes:

-  Exceptions raised in callbacks that were not properly handled or caught by a global handler would silently terminate the application, without any indication of the problem. 
-  Fixed a problem that would randomly crash OpenGL applications on the simulator. 
-  Some invalid signatures for GameKit APIs have been fixed.
-  Fixed some bugs that would make mtouch abort with the message “mtouch exited with code 1″ on multi-core CPUs. 
-  Fixes Lion activation problems.


We’ve also included a couple of new features for our users:

-  System.IO.IsolatedStorage is now available to MonoTouch users, making it easier to share code with Windows Phone 7. 
-  MonoTouch will now warn users if they use debug and LLVM at the same time.
