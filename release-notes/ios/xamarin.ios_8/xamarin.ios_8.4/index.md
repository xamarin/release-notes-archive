---
id: B873CFAC-1C1C-58AE-737B-F6A1431A922F
title: "Xamarin.iOS 8.4"
---

# Xamarin.iOS 8.4



Xamarin.iOS 8.4 adds support for Apple's iOS 8.1 APIs and Xcode 6.1, 
	while it remains identical to the previous 8.2 release in other aspects.The following document contains a list of the API changes from [API changes from 8.2 to 8.4](/releases/ios/api_changes/from_8.2.0_to_8.4.0).

## Major features

-  Adds new iOS 8.1 API and Xcode 6.1 support 
-  Support for the NetworkExtension.framework 


## Enhancements

-  [pcl] Enable PCL facades assemblies for  [unified](/guides/cross-platform/macios/unified/) [#23451]
-  Starter edition size limit raised to 128KB [8.4.0.23+] 


## Bug fixes

-  [mscorlib] Fixed Environment.GetFolderPath wrt  [iOS8 location changes for Document and Library directories](https://developer.apple.com/library/ios/technotes/tn2406/_index.html) [#24083]  **[8.4.0.27+]** 
-  [debugger] Fix the lookup of nested types which have a namespace [#21653][#23830]  **[8.4.0.31+]** 
-  [arm] Fix OP_LOCALLOC on ARM even if the size is large [#24221]  **[8.4.0.37+]** 
-  [objcruntime] Fix PlatformHelper.ParseApiPlatform not to throw on unknown/future iOS versions [#25211]  **[8.4.0.47+]** 


## Important Notes



Apple Xcode 6.1 requires Mac OSX 10.9.4+ (Mavericks) or 10.10 (Yosemite).Apple releases notes contains a list of changes and known issues for both [iOS 8.1](https://developer.apple.com/library/ios/releasenotes/Miscellaneous/RN-iOSSDK-8.1/index.html)
	and [Xcode 6.1](https://developer.apple.com/library/ios/releasenotes/DeveloperTools/RN-Xcode/Chapters/Introduction.html#//apple_ref/doc/uid/TP40001051)
	that you should review.
