---
id: AD2995ED-7574-B2D4-3080-C4F2714D7C1B
title: "MonoTouch 3.1.2"
---

&nbsp;

This fixes the following issues reported by some users:

-  Unable to have linked simulator builds
-  Erroneous messages in the simulator debugger when targetting iOS 4.1


NOTE: This release REQUIRES the latest iOS 4.1 SDK from apple and OS X
10.6

 <a name="Details" class="injected"></a>


# Details

The Apple iOS SDK 4.1 release for the iPhone Simulator no longer includes the
UNIX 2003 stubs for system calls.

Historically MonoTouch has tried to support the most several recent iOS SDKs
in 1 package, but the change in the iOS SDK 4.1 Simulator has made this
significantly more difficult as the iOS 4.0 SDK and iOS 4.1 SDK are now
significantly different.

This release addresses the incompatibility with the iOS 4.1 simulator SDK by
specifically compiling the simulator mono against the new SDK, rather than the
lowest common denominator as we have historically done.
