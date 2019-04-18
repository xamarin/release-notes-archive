---
id: FA92990B-7447-3AFD-1625-C3D4CD5EDB44
title: "MonoTouch 4.2"
---

<a name="New_Features_in_MonoTouch_4.2.2" class="injected"></a>


# New Features in MonoTouch 4.2.2

This is a minor update to MonoTouch 4.2, with the following bug fixes:

 <a name="Changes_in_MonoTouch_4.2.2" class="injected"></a>


## Changes in MonoTouch 4.2.2

Bug fixes:

-   [#587](http://bugzilla.xamarin.com/show_bug.cgi?id=587) - Full-AOT failure when *not* linking the application 
-   [#923](http://bugzilla.xamarin.com/show_bug.cgi?id=923) - UISegmentedControl: -[NSCFString BridgeSelector]: unrecognized selector sent to instance 0xe084860 
-   [#931](http://bugzilla.xamarin.com/show_bug.cgi?id=931) - UITapGestureRecognizer fails with "unrecognized selector sent" 
-   [#942](http://bugzilla.xamarin.com/show_bug.cgi?id=942) - Wrong binding for CGPDFArray.GetDictionary() 
-   [#975](http://bugzilla.xamarin.com/show_bug.cgi?id=975) - CGPDFDictionary.GetString() returns invalid strings 
-   [#980](http://bugzilla.xamarin.com/show_bug.cgi?id=980) - Cannot use ABPeoplePickerNavigationController after update to 4.2 


 <a name="New_Features_in_MonoTouch_4.2" class="injected"></a>


## New Features in MonoTouch 4.2

 **Debugging over USB:** Device debugging is now done over the
USB cable instead of Wi-Fi:

-  To debug over USB, you need MonoDevelop 2.6 installed
-  If you are using older MonoDevelop versions, it will continue to use WiFi 


This solves the problems that users had with WiFi configurations between
their Macs and their iOS devices and removes all the configuration components
from the development process (no need to configure the debugger on the device if
you happened to have a separate network)

 **Upgraded Mono Engine:** By upgrading the Mono engine to
version 2.10.5, we bring hundreds of minor optimizations and bug fixes.

 **iOS Proxy support**: we now pick the system proxy settings and
use those in .NET APIs. The new CFProxy type can be used to get to all the
details.

 **Smaller Executables:** Our improved linker reduces the size of
the executables, this will depend on your executable, but on samples like
MonoTouch.Dialog's sample this reduces the size in some 178k.

 **Smaller Downloads:** a fine tuned packaging system has reduced
the download size by 34% even while including the entire base class library
source code to assist debugging.

 **Bundled Source Code for Base Class Libraries:** Now we
distribute the source code for the base class libraries on every package
allowing developers to [single-step into the Base Class Library source code](/guides/ios/getting_started/debugging#DebuggingClassLibraries).

 <a name="Improvements:" class="injected"></a>


## Improvements:

<ol id="internal-source-marker_0.8516868778970093">
  <li>Upgraded Mono engine to <a href="http://www.mono-project.com/Release_Notes_Mono_2.10.5" target="_blank">2.10.5</a>
  </li>
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
  <li>Improves startup performance (we no longer probe the file system for
  assemblies that we ship with)
  </li>
  <li>Added AVMutableComposition</li>
  <li>New strongly typed UIGraphics.BeginPDFContext method.</li>
  <li>New MKCoordinate.FromMapRect API</li>
  <li>Improved mtouch diagnostic messages when deploying apps to the device</li>
</ol>

 <a name="Bug_Fixes:" class="injected"></a>


## Bug Fixes:

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
  <li>GC Fixes for long-lived objects.</li>
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
  can use the TPL to schedule tasks which update the UI (#<a href="https://bugzilla.novell.com/show_bug.cgi?id=690944" target="_blank">690944</a>)
  </li>
  <li>LLVM fix for assemblies with hyphens (‘-’) in their name.</li>
  <li>Fixes Application Output: Standard output and standard error are once
  again working.
  </li>
  <li>Works with the latest XCode beta release (xamarin bug #346)</li>
  <li>If you are using our XCode4 support with MonoDevelop 2.8, fixes on device
  deployment
  </li>
</ol>
