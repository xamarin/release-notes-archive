---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin Preview"
---

##  <a name="0" id="0">Xamarin for Visual Studio Preview</a>


 ![](Preview.png)

 **This is a preview of the upcoming Xamarin for Visual Studio 4.1 release. Those previews are very early, unsupported builds to allow developers to test the new features, and to gather feedback and bug reports. Your help is very appreciated! **

This release updates

 [Xamarin.iOS 9.8](/releases/ios/xamarin.ios_9/xamarin.ios_9.8/)

 and [Xamarin.Android 6.1](/releases/android/xamarin.android_6/xamarin.android_6.0/)

 releases. This early preview includes:

-  [Improved iOS Assets Catalog support](#assetscatalog)
-  [tvOS.](#tvos)
-  [Android XML Editor.](#androidxml)
-  [New SSL/TLS implementation build option.](#ssltls)
-  [New HttpClient stack selector.](#httpclient)
-  [Bug Fixes.](#bugfixes)


###  <a id="assetscatalog"></a>
Improved iOS Assets Catalog support

Our Assets Catalog editor got several new features on this release. Since the integration with the Properties Window,
   keeping a natural Visual Studio experience, selection improvements and hierarchy of assets support.

 ![](assetseditor.png)

XamarinVS 4.1 now includes support for:

#### Sprite Atlas

You can now create Sprite Atlas from Visual Studio, add, modify or remove Sprites or additional Image Sets. To change the properties just select the Atlas, a Sprite or an Image and use the Properties Window.

 ![](spriteatlas.png)

#### Data Set

You can now create Data Sets from Visual Studio, add, modify or remove arbitrary data files for different configurations, and modify its properties from the VS Properties Window.

 ![](datasets.png)

#### Image Sets

You can create Image Sets from Visual Studio, add, modify or remove arbitrary image files for different configurations, and modify its properties from the VS Properties Window.

#### On Demand Resource Tags

Our Assets Catalog Editor allows setting "On Demand Resource Tags" from the Properties Window, allowing developers to tag their resources.

###  <a id="tvos"></a>
tvOS

#### Introducing support for tvOS

When coupled with the Xamarin.iOS tvOS previews, it is now possible to create tvOS applications from Visual Studio.

 ![](tvosnpd.png)

 We have included new project types, file templates and designer support for it. We're also including support for binding projects for tvOS, which allow your projects to easily consume native libraries in tvOS, in the same way that you do for iOS.

 ![](tvosdesigner.png)

You can run and debug your applications on both the tvOS simulator as well as a physical tvOS device. We've also customized our Assets Catalog Editor for tvOS specific assets:

 ![](tvosassets.png)

###  <a id="androidxml"></a>
Android XML Editor 

We're now customizing the Visual Studio built-in XML editor for editing .axml files.

 ![](androidxmleditor.png)

Now, when switching to the "Source" Tab You can take advantage of all those great standard features from the built-in Visual Studio XML Editor:

-  Intellisense  *(in progress)* .
-  Text coloring.
-  Other standard XML editor features like Find, Replace and vertical selection.


###  <a id="ssltls"></a>
New SSL/TLS implementation build option

Available for Alpha previews of Xamarin.IOS: this controls the SSL/TLS backend used by Xamarin.iOS, and switches between Mono’s own TLS stack, and one powered by Apple’s TLS stack present in Mac and iOS.

 ![](ssltls.png)

###  <a id="httpclient"></a>
New HttpClient stack selector

Available for Alpha previews of Xamarin.iOS: this controls which HttpClient implementation to use. The default continues to be an HttpClient that is powered by HttpWebRequest, while we can now optionally switch to an implementation that uses iOS’s native transports (NSUrlSession or CFNetwork depending on the OS). The upside is smaller binaries, and faster downloads, the downside is that it requires the event loop to be running for async operations to be executed.

 ![](httpclient.png)

### ###  <a id="bugfixes"></a>
Bug fixes

This release fixes the following issues:



#### XVS 4.1.0.111

-  Getting build error when trying to build WatchKit Application in Notification Mode with VS 2015.
-  User is not able to open interface.Storyboard for Watchkit Application in VS2012/VS2013.
-  Profiler does not start when start profiler on apple TV device.


#### XVS 4.1.0.87

-  Getting run-time error while deploying watchkit application in VS.
-  Unable to connect after reboot Mac Server.
-  Xamarin iOS DocSync never finishes.
-  Entitlement.plist file editor shows incorrect values in some cases.
-  Breakpoints will not be hit debugging some specific projects.
-  Missing Rename options of UI for Asset Catalogs.
-  Unable to add image in Image View widget.
-  Linked files not copied to build directory on Mac build host.
-  The Asset Catalog entry is not displayed in the Solution Explorer when Visual Studio UI is set to a language other than English.
-  Visual Studio occasionally quits unexpectedly caused by unhandled exceptions.
-  User is not able to save file after making changes on iOS designer with VS2012/VS2013
-  Installer creates misplaced  **C:\ImportAfter\Xamarin.Command.targets** file.
-  User should not be able to create a blank asset catalog in VS.
-  Getting run-time error while deploying WK app in VS.
-  For tvOS, on changing build version in Info.plist, it doesn't reflect in XML editor of info.plist file.
-  "System.NullReferenceException: Object reference not set to an instance of an object" at AD7Events.cs line 433 thrown by the IDE extension when processing AD7DebugExceptionEvent debugger events from the Android application


#### XVS 99.0.0.1562

-  Enterprise "In House" provisioning profiles do not appear in the drop-down menu in the iOS project settings editor.
-  VS getting hanged while deploying Android application on device.
-  Unable to debug an iOS library project running from VS 2013 where async/await is used.
-  Left-hand menu of info.plist keeps disappearing in VS.
-  Incremental Build Setting causes app crash on launch: "Library not loaded ... *.exe.dylib".
-  Several iOS templates issues.
-  Test Cloud error after unfolding the project on VS error list.
-  Not having a selected iPhone causing crashes in some scenarios.
-  Unable to connect after reboot Mac server.
-  F Sharp projects in solution causes an exception when iOS simulator is selected.
