---
id: 1281209E-836A-7349-5858-140E57AAAE9D
title: "MonoTouch 1.1"
---

&nbsp;

 **Additions in 1.1.1**

-  Added GameKit bindings
-  Added MessageUI bindings
-  Added NSMutableData
-  Added additional NSData overloads
-  Added new mtouch flag -linkskip. If you are attempting to use a third party dll, you may need -linkskip to avoid missing references while linking. 


 **Fixes in 1.1.1**

-  Fixed over aggressive linker optimization (Guid.NewGuid () issue)
-  NSObservationCenter will now explicitly call Dispose() on the NSNotification posted when using the Action&lt;T&gt; overrides. Fixes the issue where it was impossible to play 2 videos in the MediaPlayer sample
