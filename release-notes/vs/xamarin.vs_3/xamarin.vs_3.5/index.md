---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.5"
---

##  <a name="0" id="0">Xamarin 3.5</a>


Xamarin 3.5 updates [Xamarin.iOS](/releases/ios/xamarin.ios_7/xamarin.ios_7.2/#6) and [Xamarin.Android](/releases/android/xamarin.android_4/xamarin.android_4.14/) releases,
    and introduces a new build system for iOS projects that works faster, incrementally and in the 
    background as you code in Visual Studio.

### Features

-  Unified Build: all-new MSBuild targets for iOS have been reworked so that all relevant compilation tasks are performed incrementally while you code, invoking the remote build host as needed. Local assembly compilation without a connection to the build host also works (just for the IL/code). 


#### iOS Designer

-  Made Xcode6 support much more robust. The designer should render reliably under all circumstances now. Support has been added for most of the new properties in iOS8.
-  Fixed an issue where the automatic reload of the design surface after rebuilding the solution could complain about custom controls causing errors.
-  Fixed an issue where UIViewControllers would sometimes render at the wrong size. i.e. one that should render as iPhone 4" might change to iPhone 3.5".
-  Optimised rendering is now working correctly when scenes are set to iPhone 4" size. This should improve drawing performance for large storyboards.
-  UITableViewCell.Style now always writes the correct value to the storyboard file.
-  The KeyboardType property of UITextField now works correctly.
-  Fixed many rendering issues with the Outline panel.
-  Added support for NSUnderline in attributed strings.
-  If a UIView inside a UICollectionViewCell is made an outlet, that outlet will be correctly generated on the UICollectionViewCell.
-  The drag images for items in the toolbox will now match the SDK set for the storyboard. For example if the storyboard is set to view as iOS6.1, the drag images will be themed using iOS 6.1.
-  Code generation will only generate C# code when in C# projects now.
-  A Deployment Target combobox has been added to the Storyboard properties so you can choose the minimum supported iOS version for each storyboard.
