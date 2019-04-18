---
id: 968DDADC-BCDD-3C7C-CB05-DCA7AB5C3299
title: "MonoTouch 3.0.4"
---

This is Preview release of MonoTouch that supports the iPhoneOS 4.0 and binds
the new **iPhoneOS 4.0 Beta 3** APIs.

Detailed changes for this release are only available on your local file
system after you install MonoTouch 3.0.4 due to the confidential nature of
iPhoneOS 4.0 changes. Once you have MonoTouch 3.0.4 installed, open this file in
your local browser for the full details of what new changes MonoTouch
introduced:

 [file:///Developer/MonoTouch/usr/share/doc/MonoTouch/compare-full.html](/guides//file:///developer/monotouch/usr/share/doc/monotouch/compare-full)

Keep in mind that this is a preview: this is not a final release for the
MonoTouch 3.0 series, this is the first release and should not be used for final
production development.

 <a name="New_Features" class="injected"></a>


# New Features

The new APIs in iPhoneOS 4.0 that were introduced at Apple's iPhoneOS event,
the list gathered from public announcements:

-  Background application support
-  iAd support
-  Local notifications
-  Game Center support
-  Support for enterprise data protection


In addition to the support for iPhoneOS 4.0, this release has a few new
features:

-  Size reduction: -   Linker updates to reduce executable size 
-   More fat trimmed from the final executable.
-   "Hello world" is 500k slimmer now


 
-  Native support for Objective-C blocks on the binding generator: -   Exposed as C# delegates 
-   Both lambdas and anonymous methods can be used as blocks
-   Standard C# semantics for variable capturing


 
-  Better support for managing provisioning profiles: -   mtouch will automatically install the provisioning profile of an application if it is not present on the device. 
-   mtouch will warn if you attempt to upload an application signed with a provisioning profile which does not include the device. 


 


 <a name="" class="injected"></a>


# Getting MonoTouch 3.0.4 <span class="icon"><a href="http://ios.xamarin.com/Releases/MonoTouch_3.0.0#"><img src="monotouch_3.0.4/Images/icon-trans.gif"></a></span>

At this point, MonoTouch 3.0.4 is only available to users that have installed
the iPhoneOS 4.0 SDK, see the instructions in our Preview Page.
