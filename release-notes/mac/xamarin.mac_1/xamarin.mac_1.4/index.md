---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 1.4"
---

##  []()Xamarin.Mac 1.4.22

### What's New?

-  Added bindings for  `NSComboBoxCell` and  `NSComboBoxCellDataSource` .
-  Fixed a  [regression](http://forums.xamarin.com/discussion/4717/any-good-examples-using-nsapplication-sharedapplication-beginsheet-sheet-window-enddelegate) where  `NSApplication.EndSheet` would crash when attempting to invoke the  `NSAction` passed to a corresponding  `NSApplication.BeginSheeet` call.
-  Fixed  [12597](https://bugzilla.xamarin.com/show_bug.cgi?id=12597) , preventing a crash when a managed method returns a null string to the native runtime, such as in  [ `NSComboBoxDataSource.CompletedString`](https://github.com/xamarin/mac-samples/blob/master/NSComboBoxTest/MainWindowController.cs#L33) .
-  Fixed  [12529](https://bugzilla.xamarin.com/show_bug.cgi?id=12529) , preventing a crash when setting an  `NSMenuItem.Activated` delegate.
-  Fixed  [12712](https://bugzilla.xamarin.com/show_bug.cgi?id=12712) , avoiding a crash in  `CGPath.EllipseFromRect` .
-  Added  `CMSampleBuffer.GetSampleTimingInfo` and  `CMSampleBuffer.CreateWithNewTiming` to allow adjusting the time of  `CMSampleBuffer` s.
-  Added linker support to preserve types using XML serialization and data contracts attributes.


### Samples

-  [Added a new sample](https://github.com/xamarin/mac-samples/blob/master/NSComboBoxTest) demonstrating  `NSComboBoxDataSource` with auto-completion.


##  []()Xamarin.Mac 1.4

The focus of this release was on providing strongly-typed notifications for
the AppKit framework, the introduction of three low-level C API bindings, and
general bug fixing.

You can check our [Roadmap](/releases/mac/roadmap) to learn where
Xamarin.Mac is headed.

### Highlights

#### AppKit Strongly-Typed Notifications

Full coverage and support for strongly-typed notifications has been introduced
for the AppKit framework. These provide a code-completion-friendly API design
for accessing dictionary entries on notifications through strong typing.

#### CFPreferences

&quot;High-Level&quot; app+user focused APIs for [ `CFPreferences`](https://developer.apple.com/library/mac/#documentation/CoreFoundation/Conceptual/CFPreferences/Tasks/UsingHighAPI.html#//apple_ref/doc/uid/20001169-CJBEHAAG)
have been introduced. `CFPreferences` is in the CoreFoundation
framework and is wrapped by the higher-level `NSUserDefaults` in the
Foundation framework.

Typically `NSUserDefaults` is preferred, but `CFPreferences` can be useful for lower-level operations. `CFPreferences` is thread safe.

#### NetworkReachability and CaptiveNetwork

The SystemConfiguration framework's [ `NetworkReachability`](http://developer.apple.com/library/ios/#documentation/SystemConfiguration/Reference/SCNetworkReachabilityRef/Reference/reference.html)
and [ `CaptiveNetwork`](http://developer.apple.com/library/ios/#documentation/SystemConfiguration/Reference/CaptiveNetworkRef/Reference/reference.html)
APIs are now supported.

 `NetworkReachability` allows an application to determine the status of a system's current network configuration and the reachability of a target host.

 `CaptiveNetwork` allows an application to interact with Captive
Network Support, the system component responsible for detecting networks that
require user interaction before providing internet access, such as those
typically found at WiFi hotspots in public locations such as airports and hotels.

#### HTML Forms in WebKit

The WebKit framework coverage was expanded to include `DomHtmlFormElement` and `DomHtmlTextAreaElement` to allow
fully interacting with HTML forms from C#. Additionally, `DomHtmlInputElement` now includes a `Files` property
exposing a `DomFileList` for supporting `input[type=file]`
elements.

#### Native Exception Marshalling

General support for marshalling native Objective-C exceptions
( `NSException`) has been introduced to on APIs annotated with `[MarshalNativeExceptions]`. Currently only a few APIs known for
throwing recoverable native exceptions support this feature:-  `MonoMac.CoreBluetooth.CBUUID.FromString` .
-  All  `MonoMac.AppKit.NSColor.<strong>*</strong>Component` properties.
-  `MonoMac.Foundation.NSKeyedUnarchiver` : its constructor and  `UnarchiveObject` and  `UnarchiveFile` methods.




If other APIs become known to be both problematic *and* recoverable,
they can be annotated in the future. Please let us know.

For more details, see the [Binding Types Reference Guide](http://docs.xamarin.com/guides/ios/advanced_topics/binding_objective-c_libraries/binding_types_reference_guide#MarshalNativeExceptions_(Xamarin.iOS_6.0.6)). Native `NSException` objects will be wrapped in a managed `ObjCException` which can be caught.

### Other Notable Fixes and Changes

-  `MonoMac.Foundation.NSOrderedSet` and  `MonoMac.Foundation.NSMutableOrderedSet` were added.
-  Stock template images are now supported through the new  `NSImageName` enum to be used in  `NSImage.ImageNamed(NSImageName)` .
-  Fixed bundling native libraries where some used absolute paths for their dependencies. This previously broke when the Mono runtime was absent on the target system.  [#11351](https://bugzilla.xamarin.com/show_bug.cgi?id=11351) .
-  Fixed issues when referencing mixed-mode (e.g. C++) .NET assemblies.  [#11448](https://bugzilla.xamarin.com/show_bug.cgi?id=11448) .
-  Added support for bundling internationalized assemblies even if the linker is disabled.


### Detailed API Differences

-  [Complete API changes from Xamarin.Mac 1.2 to 1.4](/releases/mac/api_changes/from_1.2_to_1.4) .


### Getting Started

-  Explore &quot; [Hello, Mac](/guides/mac/getting_started/hello%2C_mac) ,&quot; our tutorial on building your first Xamarin.Mac application. 
-  Launch the Documentation Browser from Xamarin Studio (Help-&gt;Help) and browse the API under the MonoMac namespace. 
-  Check our&nbsp; [extensive set of samples](/samples/mac/all) . 


### Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.
