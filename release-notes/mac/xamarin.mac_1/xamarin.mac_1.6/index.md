---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 1.6"
---

#  []()Xamarin.Mac 1.6

The primary focus for the 1.6 series of Xamarin.Mac is to introduce
full compatibility with the Mono 3.2 runtime which introduces full
support for the .NET 4.0 and 4.5 frameworks, including `async`
support.

Explore our [Roadmap](/releases/mac/roadmap) to learn where
Xamarin.Mac is headed.

### Highlights

#### Mono 3.2

While not many changes were made to Xamarin.Mac itself since 1.4.22,
Xamarin.Mac is now aligned with the other Xamarin products against the
Mono 3.2 runtime which supports the .NET 4.0 and 4.5 frameworks including
support for async/await.

As such, Xamarin.Mac applications can now take full advantage of these
modern .NET frameworks.

By default, Xamarin.Mac projects will target .NET 4.0, but can be
upgraded to 4.5 by changing the Target Framework option under the project's
general build settings in Xamarin Studio.

Older versions of Mono are no longer supported by Xamarin.Mac.

#### CoreBluetooth

Introduced in Xamarin.Mac 1.6 were convenience improvements to the
CoreBluetooth API for interacting with Bluetooth Low Energy devices on
compatible Mac OS X systems.

A number of convenience APIs were added along with major fixes to `CBUUID`, an essential data structure for interacting with
CoreBluetooth objects. Improvements include equality support and helper
static methods such as `FromPartial`. Example:

```
foreach (var characteristic in service.Characteristics) {
    if (characteristic.UUID == CBUUID.FromPartial (0x2A37)) {
      service.Peripheral.SetNotifyValue (true, characteristic);
    }
  }
```

 [A new detailed sample on using CoreBluetooth was written](https://github.com/xamarin/mac-samples/tree/master/HeartRateMonitor#monomaccorebluetooth), focusing
on Bluetooth LE Heart Rate Monitors. Explore and remix the code!

 [ ![CoreBluetooth Heart Rate Monitor](images/heart-rate-monitor.png "CoreBluetooth Heart Rate Monitor")](https://github.com/xamarin/mac-samples/tree/master/HeartRateMonitor#monomaccorebluetooth)

### Other Notable Fixes and Changes

-  `Retain` ,  `Release` , and  `Autorelease` are now supported on  `NSObject` . This allows supporting methods such as  `copyWithZone:` , where returned objects should be explicitly  `Retain` ed first.  [#1086](https://bugzilla.xamarin.com/show_bug.cgi?id=1086)


### Getting Started

-  Explore &quot; [Hello, Mac](/guides/mac/getting_started/hello%2C_mac) ,&quot; our tutorial on building your first Xamarin.Mac application. 
-  Launch the Documentation Browser from Xamarin Studio (Help-&gt;API Documentation) and browse the API under the MonoMac namespace. 
-  Check our&nbsp; [extensive set of samples](/samples/mac/all) . 


### Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.

 <a name="19"></a>


# Xamarin.Mac 1.6.19


Xamarin.Mac 1.6.19 is a bugfix only release.### Bug Fixes:

-  Add  `NSAttributedString.FromAttachment` ( [#14429](https://bugzilla.xamarin.com/show_bug.cgi?id=14429) ).
-  Fix for  `NSTextAttachmentCell` : provide constructor that takes an  `NSImage` , remove incorrect  `[Abstract]` attributes on  `DrawWithFrame` and  `WantsToTrackMouse` to allow  `NSTextAttachmentCell` to be instantiated without subclassing. ( [#14429](https://bugzilla.xamarin.com/show_bug.cgi?id=14429) ).
-  Fix  `CTFont` constructor to allow language argument to be null ( [#13346](https://bugzilla.xamarin.com/show_bug.cgi?id=13346) ).
-  Add  `PathsForResources` ,  `PathForResource` ,  `GetPathsForResources` to  `NSBundle` .
-  Enable RedRange, GreenRange, BlueRange, AlphaRange on CAEmitterCell (was previously iOS only).
-  Fix regression where  `CAEmitterCell.Contents` was removed ( [#10517](https://bugzilla.xamarin.com/show_bug.cgi?id=10517) ).
-  Enforce with an  `InvalidOperationException` that  `NSApplication.Initialize` can only be called once.
