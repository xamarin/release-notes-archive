---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 1.10"
---

# Xamarin.Mac 1.10.0.18 

Xamarin.Mac 1.10.0.18 is a maintance update fixing a few commonly reported problems.

-  Fixed an issue where some APIs would throw xamarin_IntPtr_objc_msgSend errors. Xamarin Bug 22729 and 22714.
-  Fixed an issue where some licenses would have issues accessing Classic projects.
-  Added some rpath support to the linker/packager mmp.
-  Fixed a libgdiplus+ regression that comes with mono 3.10.0.28. Xamarin Bug 23553.


# Xamarin.Mac 1.10.0 

Xamarin.Mac 1.10 supports many new APIs introduced in
	Mavericks, moves Xamarin.Mac to the activation system used by
	Xamarin.iOS and Xamarin.Android, and provides a preview of the
	new [Unified APIs](/guides/cross-platform/macios/unified), extending our support to 64-bit frameworks.

Explore our [Roadmap](/releases/mac/roadmap) to
	learn where Xamarin.Mac is headed.

### Highlights

#### New Unified APIs



As
	reported [here](http://tirania.org/monomac/archive/2013/Nov-11.html)

,
	we’ve been hard at work creating support for running your
	application against Apple’s 64-bit frameworks and runtime and
	we’re excited to provide a preview release in 1.10. Here are
	the details:-  Please note, unlike our normal stable API policy, this is a preview release so API/ABI compatibility is not guaranteed.
-  Projects can be migrated to the new profile via:    
  ![](images/migrate.png)  ![](images/migrate2.png) 
-  Projects using the new profile can be created from the newly reorganized project templates    
  ![](images/new-project-type.png) 
-  The new profile links against a new  `Xamarin.Mac.dll` instead of  `XamMac.dll`
-  To improve code sharing with iOS project, the new assembly drops the "MonoMac" namespace from our types, so you’ll need to change things like  `using MonoMac.ObjCRuntime` to  `using ObjCRuntime`
-  In the future there will be tooling to help automate this conversion.
-  Many APIs that return types that vary on the bitness (32-bit or 64-bit) will now return nint or nfloat instead of int or float. For more information read our  [Native Types Guide](/guides/cross-platform/macios/nativetypes) 


#### Licensing / Activation



	Xamarin.Mac is moving to the activation system used by
	Xamarin.iOS and Xamarin.Android. Some noticeable changes
	include:-  Activation will no longer occur at the end of installation and require an activation code. Instead, activation will occur within Xamarin Studio by logging into your Xamarin account. 
-  Activation status and license level will show up in Xamarin Studio -&gt; Account now    
  ![](images/activation.png) 
-  Xamarin.Mac gains a full 30-day trial mode, with similar restrictions as the Xamarin.iOS’s trial. 


#### New Framework APIs

New 64-bit only framework APIs (only available to unified projects)

-  JavaScriptCore


#### Significant API Changes

-  NSComboBox has support for new events and the associated delegate NSComboBoxDelegate. 
-  Additional bindings in CoreGraphics for CGPath, CGEvent APIs, and NSStream. 
-  New support for the CoreGraphics PDF APIs.
-  MonoMac.ObjCRuntime.Messaging has been removed from the new Unified API.
-  Removed ABAddressBook from Xamarin.Mac bindings. It bound the iOS API which was not available on OS X. A binding to the obj-c OS X address book API will be provided in the  [future](https://bugzilla.xamarin.com/show_bug.cgi?id=1392) .


### Important Notes

In a few cases API has been broken where it has made most
	sense and when the existing incorrect API could not have been
	marked as obsolete.  When rebuilding with Xamarin.Mac 1.10,
	many of these cases should not even surface, but in cases that
	do, the changes that need to be made should be obvious with a
	more desirable end result. Some notable breaking changes:

-  Tightening up the return of some properties and methods to return specific types instead of NSObject when only that type is possible.
-  Some parameters in CoreFoundation have been changed from int to CFIndex to support the new Unified profile.
-  The constructor for MidiObject was changed from IntPtr to int. This is not a mistake, this is matching the underlying API.


### Known Issues 

-  Unified projects do not generate installer packages yet. 
-  OS X Lion can not build unified projects due to the age of the associated Xcode. Lion can still run Xamarin.Mac applications, but you will need to upgrade any development machines past Lion. 


### API Changes

-  [From 1.8.1 to 1.10.0](/releases/mac/api_changes/from_1.8.1_to_1.10.0)


## Getting Started

-  Explore &quot; [Hello, Mac](/guides/mac/getting_started/hello%2C_mac) ,&quot; our tutorial on building your first Xamarin.Mac application. 
-  Launch the Documentation Browser from Xamarin Studio (Help-&gt;API Documentation) and browse the API under the MonoMac namespace. 
-  Check our&nbsp; [extensive set of samples](/samples/mac/all) . 


## Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.
