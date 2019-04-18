---
id: E69268DA-C1FF-01C8-B33D-A725F03CA727
title: "MonoTouch 4.0.6"
---

&nbsp;

MonoTouch 4.0.6 is a stable release, and it includes the following changes
since version 4.0.5:

-  ThreadPool has been fixed.   
    
 This is a major fix and it affected multiple component in Mono's stack. This change fixes several problems ranging from the HTTP stack to asynchronous operations and any other consumer of the Mono ThreadPool. Users are encouraged to upgrade to this release for this fix alone.   
    
 
-  We now report an error when the MonoPInvokeCallbackAttribute is applied to instance methods (only static methods are allowed to have that attribute)   
    
 
-  Activation has been fixed.
