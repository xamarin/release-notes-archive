---
id: 27C74214-83C7-368C-A911-C3560CD4D57F
title: "MonoTouch 4.1.0"
---

MonoTouch 4.1.0 is part of our Beta Series that will lead up to MonoTouch
4.2.

As any other beta updates, you can install it by selecting the Beta channel
on MonoDevelop and installing your MonoTouch package.

 <a name="New_Features" class="injected"></a>


# New Features

Device debugging is now done over the USB cable instead of Wi-Fi:

-  To debug over USB, you will need MonoDevelop 2.6 RC 1 installed
-  If you are using older MonoDevelop versions, it will continue to use WiFi 


This solves the problems that users had with WiFi configurations between
their Macs and their iOS devices and removes all the configuration components
from the development process (no need to configure the debugger on the device if
you happened to have a separate network)

 <a name="Improvements:" class="injected"></a>


# Improvements:

<ol id="internal-source-marker_0.8516868778970093">
  <li>Upgraded Mono engine to 2.10.4</li>
  <li>Working generic variance and generic virtual methods<br>
    <br>
    Those CLR features are now supported on device.<br>
    <br>
    Note: The mobile profile still won’t feature the .NET 4.0 variance change
    as those might cause unwanted regressions.
  </li>
  <li>Smaller applications based on our improved linker, <a href="http://spouliot.wordpress.com/2011/07/21/smaller-monotouch-applications/" target="_blank">see this blog post for details</a>.
  </li>
  <li>MonoTouch.MessageUI.MFMessageComposeViewController now has .NET-style
  events.
  </li>
  <li>Improved diagnostics in error conditions, such as:
    <ol>
      <li>When managed objects are collected but the objective-c object are
      still alive
      </li>
      <li>When objective-c types are missing from the executable due to
      improper linking
      </li>
    </ol>

  </li>
  <li>Reduced memory allocation for per-assembly AOT structures slightly</li>
</ol>

 <a name="Bug_Fixes:" class="injected"></a>


# Bug Fixes:

Memory Retention/GC fixes:

<ol id="internal-source-marker_0.8516868778970093">
  <li>Fix UIControl retention problem when events were wired up</li>
  <li>Views are no longer retained if they were previously removed with
  RemoveFromSuperview ()
  </li>
  <li>UIGestureRecognizers can now remove targets</li>
  <li>The AOT compiler was incorrectly serializing some types and missing
  finalizer references.
  </li>
</ol>

Other fixes:

<ol id="internal-source-marker_0.8516868778970093">
  <li>Fixes for sqlite3.dylib when running in the simulator on newer sdk
  releases
  </li>
  <li>Simulator is once again activated when running the application, this
  wasbroken after the XCode 4.1 update (<a href="http://bugzilla.xamarin.com/show_bug.cgi?id=202" target="_blank">#202</a>).
  </li>
  <li>Added a default SynchronizationContext for the main UI thread so that you
  can use the TPL to schedule tasks which update the UI (#690944)
  </li>
  <li>LLVM fix for assemblies with hyphens (‘-’) in their name.</li>
</ol>

 <a name="Known_Problems" class="injected"></a>


# Known Problems

With this release, we know that Console.WriteLine does not output any
messages to the Application output.
