---
id: B873CFAC-1C1C-58AE-737B-F6A1431A922E
title: "Xamarin.iOS 8.2"
---

# Xamarin.iOS 8.2



Xamarin.iOS 8.2 is the first update to our iOS 8 support, introduced in
	September with [Xamarin.iOS 8.0](../xamarin.ios_8/xamarin.ios_8.0)

.

Additional IDE support comes from the [new Xamarin Studio (5.5)](../../studio/xamarin.studio_5.5/xamarin.studio_5.5)


	and [updated (3.7) VS support](../../vs/xamarin.vs_3/xamarin.vs_3.7)

.## Major features

-  Mono runtime/BCL updated to 3.10 
-  F# updated to  [3.1.1.25](https://github.com/fsharp/fsharp/blob/3.1.1.25/CHANGES.txt) 


## Enhancements

-  [foundation] Added  `NSTimeZone Abbreviation` and  `Abbreviations` [#20520] 


## Bug fixes

-  [foundation] Add back  `NSMutableArray.ctor(int)` constructor [#21901] 
-  [aot] Always pass the imt arg to interface calls in gsharedvt methods [#22624] 
-  [runtime] Look for  `[BlockProxy]` attributes on implemented protocol interfaces [#22888] 
-  [aot] Fix for ARM64 support [#23026] 
-  [btouch] Properly handle protocols inheritance using  `[BaseType]` [#23041] 
-  [corelocation]  `CLBeacon.Major/Minor` misidentified as introduced in iOS 8 [#23066] 
-  [mtouch] Fix OSX/iOS frameworks mixup that can prevent older simulator to launch apps properly [#22750] 
-  [dialog] Fix  `DialogViewController.RefreshRequested` (unified 64bits only) [#23089] 
-  [metal] Add missing [Native] on two enums (unified 32bits only) [#23256] 
-  [runtime] Use the right target type when marshalling array elements [#23289] 
-  [extensions] Do not look for .exe in simulator builds for extensions 


## Important Notes



Apple Xcode 6 requires Mac OSX 10.9.4+ (Mavericks) or 10.10 (Yosemite).
