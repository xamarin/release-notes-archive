---
id: DEFEF357-D7C1-4AA1-B961-74F36BE4201B
title: "Xamarin.iOS 7.4"
---

# Xamarin.iOS 7.4



The Xamarin.iOS 7.4.x series introduce support for building
	both 32 and 64 bits iOS applications.

This takes the form of a [new  *unified*assembly](/guides/cross-platform/macios/unified/)

, `Xamarin.iOS.dll`

, that
	can target both 32 and 64 bits iOS devices.
	This *unified*

 assembly is also closer to the new,
	32/64 bits compatible, `Xamarin.Mac.dll`

assembly
	provided with latest version of [Xamarin.Mac](http://xamarin.com/platform)

.
	This makes code sharing between iOS and OSX even easier than
	before.

Note that this new assembly is a **preview**

 and its
	API is not, at this time, frozen (breaking change might happen). [Feedback](http://xamarin.uservoice.com/forums/144858-xamarin-product-suggestions/category/65285-xamarin-ios-suggestions)


	and [bug reports](http://bugzilla.xamarin.com/)

 are
	welcome.

The *classic*

 `monotouch.dll`

 assembly
	remains **fully supported**

 and includes all new features.
	However it remains limited to build 32 bits applications. <a name="0"></a>


#  [Xamarin.iOS 7.4.0](#6)



Xamarin.iOS 7.4.0 is the first release to include a **preview**

 
	of the new 32/64 bits compatible Xamarin.iOS.dll assembly.The following document contains a list of the [API changes from 7.2.6 to 7.4.0](/releases/ios/api_changes/from_7.2.6_to_7.4.0)

## Enhancements

-  Product installation is now under /Library/Frameworks/Xamarin.iOS.framework instead of under /Developer/MonoTouch 
-  Mono runtime/BCL updated to 3.8 
-  F# updated to 3.1.1.21 
-  [uikit] Adopt UIAccessibilityIdentification on UIBarItem and UIImage [#21585] 
-  [foundation] Add NS[Input|Output]Stream overloads with offset [desk #81124] 
-  [foundation] Add several overloads for NSBundle.GetUrlForResource* 
-  [foundation] Add new NSData.Save helper methods 


## Bug fixes

-  [runtime] Fix a race during finalization [#7723][#16208][#19442c7] 
-  [coregraphics] Pin the byte[] buffer given to CGDataProviderCreateWithData [#21043] 
-  [uikit] UITextInput.GetCaretRectForPosition allows a null UITextPosition argument [#20572] 
-  [mtouch] Detect problems when creating the NOTICE file [#20607] 
-  [registrar] Use correct declaring type for InvokeConformsToProtocol [#20675] 
-  [foundation] Fix NSDecimal / decimal casting on locale using ',' as the separator [#20892] 
-  [avfoundation] Fix for AVAssetResourceLoadingRequest.Finished under iOS 6.x [#20909] 
-  [runtime] Fix Process.PrivateMemorySize64 to work on iOS sandbox for the current process [#21882] 
-  [jit] Fix enum->int casts in gsharedvt code [#21893] 
-  [generator] Fix UIAppearance protocol support in 3rd party bindings [desk #79124]
