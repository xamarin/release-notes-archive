---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 1.12"
---

# Xamarin.Mac 1.12.0.14 

This update fixes a number of issues associated with code signing and packaging in Unified.

# Xamarin.Mac 1.12.0.8 

This update fixes a number of issues associated with code signing and packaging in Unified.

Known Issue - In some situtations the "Automatic" option on Identity / Provisioning Profile may fail to select the correct entry during code signing. [26955](https://bugzilla.xamarin.com/show_bug.cgi?id=26955)

# Xamarin.Mac 1.12.0.4 

Xamarin.Mac 1.12 supports many new APIs introduced with Yosemite and 
	moves to a unified runtime shared with Xamarin.iOS that fixes some
	longstanding issues and builds the foundation for future improvements.

1.12.0.4 is the graduation of our extended [1.11 alpha](/releases/mac/xamarin.mac_1/xamarin.mac_1.11.html) that was run
	to shake out any issues with the new runtime.

Explore our [Roadmap](/releases/mac/roadmap) to
	learn where Xamarin.Mac is headed.

### Highlights

-  Support for many of the new APIs introduced with Yosemite to our stable branch.
-  Additional support for Xamarin's new 32 and 64 bit  [Unified APIs](/guides/cross-platform/macios/unified) .
-  This release adds the ability for Unified projects to build against the Full .NET profile (this configuration is unsupported however)
-  This will be the last Xamarin.Mac release in which the Unified API will be considered unstable. We do not anticipate any major changes (the parts shared with iOS are already frozen) but we will be removing some deprecated APIs and doing some fine tuning to the Mac Unified API in the coming months.
-  Due to the move to a unified runtime with Xamarin.iOS, we've improved validation on exported selectors. Incorrect selectors, such as ones with a missing/extra ':' may need to be manually fixed in source code and associated nib files.


#### New Framework APIs

New 64-bit only framework APIs (only available to [unified projects](/guides/cross-platform/macios/unified))

-  JavaScriptCore
-  GLKit
-  SpriteKit


New 32 and 64-bit framework APIs (only available to unified projects)

-  CloudKit
-  LocalAuthentication


### Known Issues 

-  Migrations from the Classic profile to Unified need a manual clean before building to work around errors such as "System.DllNotFoundException: libxammac.dylib or mismatch between Xamarin.Mac.dll and XamMac.dll". This will be automated in future Xamarin Studio releases.
-  Full Profile Unified projects can run into issues when built as 64-bit applications. We are looking into this fixing this in a future release.


### API Changes



You can see the changes from:-  Classic API:  [1.10.0 to 1.12.0](/releases/mac/api_changes/from_1.10.0_to_1.12.0)
-  Unified API:  [1.10.0 to 1.12.0](/releases/mac/api_changes/from_1.10.0_to_1.12.0_unified)


## Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.
