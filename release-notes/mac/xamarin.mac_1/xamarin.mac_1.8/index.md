---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 1.8"
---

Xamarin.Mac 1.8 supports many new APIs introduced in Mavericks and
Mountain Lion.

Under the hood many improvements have taken place that won't necessarily
be visible to developers using Xamarin.Mac. Many of these internal
improvements set the stage for Xamarin.Mac 2.0 which will introduce full
64-bit support along with many other developer-visible features.Explore our [Roadmap](/releases/mac/roadmap) to learn where
Xamarin.Mac is headed.

### Highlights

#### New Framework APIs

Major enhancements to the following frameworks have been introduced:

-  AppKit
-  Foundation
-  AudioToolbox
-  AudioUnit
-  AVFoundation
-  CoreImage
-  CoreMedia
-  CoreWlan
-  SceneKit


SceneKit has been improved with a more C#-friendly API - notably we
have implemented constructors (SceneKit uses static factory methods)
to allow for scene graph creation using C# object and collection
initializer syntax.

CoreWlan's new API is now fully supported. Apple has completely
removed support for the legacy API in Mac OS X 10.9. You should migrate
to the new API if you plan to support Mavericks.

#### Enhanced Protocol Support

This release provides enhanced support for better bridging Objective-C
protocols in our API and on third party bindings. Several new APIs are now
easier to use since they do not have to expose `NSObject` when
a protocol is needed. They can now expose a strongly-typed interface that
matches the Objective-C protocol.

See the [updated iOS documentation](/guides/ios/advanced_topics/binding_objective-c/binding_objc_libs#iOS7ProtocolSupport) for details on how this new feature works.

Internally, many objects now implement interfaces such as:

-  `INSCoding`
-  `INSCopying`
-  `INSSecureCoding`
-  `INSMutableCopying`


#### PCL Support

Xamarin.Mac applications should now be able to properly consume and
link PCL assemblies.

### Important Notes

In a few cases API has been broken where it has made most sense and
when the existing incorrect API could not have been marked as obsolete.
When rebuilding with Xamarin.Mac 1.8, many of these cases should not
even surface, but in cases that do, the changes that need to be made
should be obvious with a more desirable end result. Some notable
breaking changes:

-  `MonoMac.SceneKit.SCNLayer.HitTest ()` 's return value has changed from a weakly typed  `NSArray` to a strongly typed  `SCNHitTestResult []` .
-  `MonoMac.AppKit.NSErrorEventArgs` was renamed to  `MonoMac.Foundation.NSErrorEventArgs` .
-  The value of  `MonoMac.Foundation.NSAlignmentOptions.RectFlipped` has always been incorrect ( `Int32.MinValue` ). Its value is now correct ( `Int64.MinValue` ).
-  `MonoMac.AppKit.NSTreeController.Content` 's type has changed from an incorrect strongly-typed  `NSTreeController` to a weakly-typed  `NSObject` .
-  `MonoMac.AppKit.NSTreeNode.RepresentedObject` 's type has changed from an incorrect strongly-typed  `NSTreeNode` to a weakly-typed  `NSObject` .


<h2 id="1">Xamarin.Mac 1.8.1</h2>

In addition to many internal bug fixes, Xamarin.Mac 1.8.1 adds support
for new APIs and improvements to existing ones. It is a minor update to
the stable 1.8.0 release.

### Highlights



Native `CFNetwork`

 support for <coe>System.Net.Http.HttpClient
(by way of <code>MonoMac.CFNetwork.MessageHandler</code>) is now provided in
<code>XamMac.CFNetwork.dll</code> when targeting .NET 4.5, which can be found at
<i>/Library/Frameworks/Xamarin.Mac.framework/Versions/Current/lib/mono/XamMac.CFNetwork.dll</i>.<p>

<p>MonoMac.AppKit’s <code>NSTextFinder</code>, <code>NSTextFinderBarContainer</code>,
and <code>NSTextFinderClient</code> are now usable.</p>

<p><code>NSToolbarDelegate</code> members are now <code>virtual</code>
(optional) instead of <code>abstract</code> (required).</p>

<p>Many additional <code>MonoMac.CoreBluetooth</code> APIs are introduced
improving parity with Xamarin.iOS:</p>

<ul>
  <li><code>CBPeripheralManager</code></li>
  <li><code>CBCentral</code></li>
  <li><code>CBMutableCharacteristic</code></li>
  <li><code>CBMutableDescriptor</code></li>
  <li><code>CBMutableService</code></li>
  <li><code>CBATTRequest</code></li>
</ul>

<p>Low level Quartz Event Services support for event taps was introduced
(<code>CGEvent</code>, <code>CGEventSource</code>). See the
<a href="https://developer.apple.com/library/mac/documentation/Carbon/Reference/QuartzEventServicesRef/Reference/reference.html">Apple
documentation on Quartz Event Services for more detail</a>.</p>

<p>The low level <code>CFMachPort</code> API is now supported.</p>

<p>The <code>MonoMac.Security</code> API was updated and now has parity
with Xamarin.iOS.</p>

<p>Improvements to the <code>MonoMac.WebKit</code> API were made,
including support for detailed and strongly-typed DOM events:</p>

<ul>
  <li><code>DomEventTarget</code></li>
  <li><code>DomKeyboardEvent</code></li>
  <li><code>DomMouseEvent</code></li>
  <li><code>DomOverflowEvent</code></li>
  <li><code>DomProgressEvent</code></li>
  <li><code>DomUIEvent</code></li>
  <li><code>DomWheelEvent</code></li>
</ul>

<h3>API Changes</h3>

<ul>
  <li><a href="/releases/mac/api_changes/from_1.8.0_to_1.8.1/">From 1.8.0 to 1.8.1</a></li>
  <li><a href="/releases/mac/api_changes/from_1.6_to_1.8/">From 1.6.27 to 1.8.0</a></li>
</ul>

<h2>Getting Started</h2>

<ul>
  <li>Explore &quot;<a href="/guides/mac/getting_started/hello%2C_mac">Hello,
  Mac</a>,&quot; our tutorial on building your first Xamarin.Mac application.
  </li>
  <li>Launch the Documentation Browser from Xamarin Studio (Help-&gt;API
  Documentation) and browse the API under the MonoMac namespace.
  </li>
  <li>Check our&nbsp;<a href="/samples/mac/all">extensive set of samples</a>.
  </li>
</ul>

<h2>Community</h2>

<p><a href="http://forums.xamarin.com/categories/mac" target="_blank">Connect
with other Xamarin.Mac</a> users on our forums.</p>

<p>Join us at our <a href="http://chat.xamarin.com" target="_blank">Live
Chat</a> for live support and discussions.</p>
</coe>
