---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 4.1"
---

##  <a name="0" id="0">Xamarin for Visual Studio 4.1</a>


This release updates

 [Xamarin.iOS 9.8](/releases/ios/xamarin.ios_9/xamarin.ios_9.8/)

 and [Xamarin.Android 6.1](/releases/android/xamarin.android_6/xamarin.android_6.0/)

 releases. and includes:

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

When coupled with the Xamarin.iOS tvOS, it is now possible to create tvOS applications from Visual Studio.

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

Available for Xamarin.IOS: this controls the SSL/TLS backend used by Xamarin.iOS, and switches between Mono’s own TLS stack, and one powered by Apple’s TLS stack present in Mac and iOS.

 ![](ssltls.png)

###  <a id="httpclient"></a>
New HttpClient stack selector

Available for Xamarin.iOS: this controls which HttpClient implementation to use. The default continues to be an HttpClient that is powered by HttpWebRequest, while we can now optionally switch to an implementation that uses iOS’s native transports (NSUrlSession or CFNetwork depending on the OS). The upside is smaller binaries, and faster downloads, the downside is that it requires the event loop to be running for async operations to be executed.

 ![](httpclient.png)

### ###  <a id="bugfixes"></a>
Bug fixes

This release fixes the following issues:



#### XVS 4.1.2 (Cycle 7 Service Release 1)

-  Setting the IpaPackageDir property to a custom value breaks the logic that automatically copies the .ipa file to Windows from the Mac.
-  Improved missing dependency message if MS Build Tools 2015 is not found.
-  Breakpoints in async methods in PCL projects are not hit if the linker is enabled when debugging iOS projects.
-  Clicking "Xamarin for Visual Studio Update Available" notification toolbar icon in the system tray has no effect
-  Mac Agent auto-reconnection mechanism issues.
-  Visual Studio crashes due to NullReferenceException in Renci.SshNet.BaseClient.Disconnect() if network connection is lost after deployment to simulator but before debugger connects.
-  Could not find a part of the path warning building an iOS project.
-  Android N device does not show in device drop down list on VS.
-  **Known issues:**
-    
-  "Unable to connect to Address='192.168.1.2:22' with User='macuser'" or "Private key is encrypted but passphrase is empty." after downgrading back to the previous version Xamarin 4.0. This is an  *intentional* change due to a new security feature in Xamarin 4.1.  **Recommended fix** : Delete  **id_rsa** and  **id_rsa.pub** from  **%LOCALAPPDATA%\Xamarin\MonoTouch** , and then reconnect to the Mac build host.
-  After installing this version, connecting to the Mac might ask for Mac credentials once, even if it's a known Mac 
-  **New Requirements for Xamarin Designer:**
-  <u>Only if Visual Studio 2015, or Visual Studio 15 Preview is not installed</u> on the same machine, and for using the Xamarin designer on Visual Studio 2012 or 2013, the following products are required:
-    
-  [Microsoft .Net 4.6.](https://www.microsoft.com/en-us/download/details.aspx?id=48137)
-  [Microsoft MSBuild Tools 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48159)


#### XVS 4.1.1 (Cycle 7 Service Release 0)

-  Fixes issue installing Xamarin VS extension on Dev15 if VS 2015 is not installed on the same machine.
-  Fixes  [41665](https://bugzilla.xamarin.com/show_bug.cgi?id=41665) : "'System.ComponentModel.INotifyPropertyChanged' is defined in an assembly that is not referenced. You must add a reference to assembly 'System.ObjectModel" when building Android projects. The fix adjusts the Xamarin.Android MSBuild files to set  `$(DependsOnSystemRuntime)` to  `true` automatically.
-  **Known issues:**
-     
-  "Unable to connect to Address='192.168.1.2:22' with User='macuser'" or "Private key is encrypted but passphrase is empty." after downgrading back to the previous version Xamarin 4.0. This is an  *intentional* change due to a new security feature in Xamarin 4.1.  **Recommended fix** : Delete  **id_rsa** and  **id_rsa.pub** from  **%LOCALAPPDATA%\Xamarin\MonoTouch** , and then reconnect to the Mac build host.
-  After installing this version, connecting to the Mac might ask for Mac credentials once, even if it's a known Mac.
-  [41836](https://bugzilla.xamarin.com/show_bug.cgi?id=41836) : For iOS apps, breakpoints within  `async` methods in PCL projects are not hit if the linker is enabled.  **Partial temporary workaround** : Set  <span class="UIItem">Project Properties &gt; iOS Build &gt; Linker behavior</span> to  <span class="UIItem">Don't link</span> . (For device builds this workaround does unfortunately create significantly larger  `.app` bundles and can lengthen deployment times.)
-  **New Requirements for Xamarin Designer:**
-  <u>Only if Visual Studio 2015, or Visual Studio 15 Preview is not installed</u> on the same machine, and for using the Xamarin designer on Visual Studio 2012 or 2013, the following products are required:
-    
-  [Microsoft .Net 4.6.](https://www.microsoft.com/en-us/download/details.aspx?id=48137)
-  [Microsoft MSBuild Tools 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48159)


#### XVS 4.1.0.530

<ul>
    <li>No AppleTV entry for launch image in Asset Catalog.</li>
    <li>tvOS template is missing mandatory keys in info.plist file.</li>
    <li>tvOS provisioning profiles are not appearing in Visual Studio.</li>
    <li>Fixes Visual Studio crash disconnecting from VPN.</li>
    <p><b>Known issues:</b></p>
    <ul>
    	
        
        
        
    </ul><li>"Unable to connect to Address='192.168.1.2:22' with User='macuser'" or "Private key is encrypted but passphrase is empty." after downgrading back to the previous version Xamarin 4.0. This is an <em>intentional</em> change due to a new security feature in Xamarin 4.1. <strong>Recommended fix</strong>: Delete <strong>id_rsa</strong> and <strong>id_rsa.pub</strong> from <strong>%LOCALAPPDATA%\Xamarin\MonoTouch</strong>, and then reconnect to the Mac build host.</li><li>After installing this version, connecting to the Mac might ask for Mac credentials once, even if it's a known Mac.</li><li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=41836">41836</a>: For iOS apps, breakpoints within <code>async</code> methods in PCL projects are not hit if the linker is enabled.  <strong>Partial temporary workaround</strong>: Set <span class="UIItem">Project Properties &gt; iOS Build &gt; Linker behavior</span> to <span class="UIItem">Don't link</span>.  (For device builds this workaround does unfortunately create significantly larger <code>.app</code> bundles and can lengthen deployment times.)</li><li>
            <p><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=41665">41665</a>: "'System.ComponentModel.INotifyPropertyChanged' is defined in an assembly that is not referenced. You must add a reference to assembly 'System.ObjectModel" in <em>VS 2013 only</em> when building Android projects that reference PCLs that use <code>INotifyPropertyChanged</code>.  This issue also causes similar error messages for other facade assemblies.  As discussed in the the bug report, the upcoming fix for this issue will set <code>$(DependsOnSystemRuntime)</code> to <code>true</code> automatically.  <strong>Temporary workaround</strong>: Until the fix is published, you can temporarily apply the fix by hand if you like by adding the following line in the top <code>&lt;PropertyGroup&gt;</code> element in your Android app project <code>.csproj</code> file:</p>
            <pre><code class=" syntax brush-C#">&lt;DependsOnSystemRuntime Condition=" '$(DependsOnSystemRuntime)' == '' "&gt;true&lt;/DependsOnSystemRuntime&gt;</code></pre>
        </li>
    <p><b>New Requirements for Xamarin Designer:</b></p>
    <p><u>Only if Visual Studio 2015 is not installed</u> on the same machine, and for using the Xamarin designer on Visual Studio 2012 or 2013, the following products are required:</p>
    <ul>
        
        
    </ul><li><a href="https://www.microsoft.com/en-us/download/details.aspx?id=48137">Microsoft .Net 4.6.</a></li><li><a href="https://www.microsoft.com/en-us/download/details.aspx?id=48159">Microsoft MSBuild Tools 2015</a></li>
</ul>

#### XVS 4.1.0.517

-  List of iOS simulators disappears if you close the solution and reopen it.
-  Info.plist Universal icons fails to preview read-only images in Visual Studio.
-  Asset Catalog failing to load when an image is read-only.
-  Android Designer tab labels kept as Designer and Source.
-  Bring Android emulator to front when launched.
-  **Known issues:**
-    
-  After installing this version, connecting to the Mac might ask for Mac credentials once, even if it's a known Mac.
-  Downgrading or switching channels after installing this version can require deleting files id_rsa and id_rsa.pub from "%localappdata%/Xamarin/Monotouch" to connect successfully with Mac servers using older versions.
-  **New Requirements for Xamarin Designer:**
-  <u>Only if Visual Studio 2015 is not installed</u> on the same machine, and for using the Xamarin designer on Visual Studio 2012 or 2013, the following products are required:
-    
-  [Microsoft .Net 4.6.](https://www.microsoft.com/en-us/download/details.aspx?id=48137)
-  [Microsoft MSBuild Tools 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48159)


#### XVS 4.1.0.496

-  Very slow iOS build times due to PackLibraryResources.
-  Sets Apple TLS as default TLS provider.
-  Updates UITest nuget package to 1.3.8 in Xamarin for Visual Studio templates.
-  Breakpoint not getting hit for WatchKit application.
-  Visual Studio is Unable to Connect to Mac ("Couldn't connect to *********. Please try again."), due to wrong Mac path.
-  Visual Studio installer now detects and informs if required MSBuild Tools 2015 is missing.
-  Fixed C# Android Templates causing unfolding failures in some environments.
-  AdHoc app with On-Demand Resources can't be installed on device via iTunes.
-  Access to the path (csproj) is denied when iOS project with Assets Catalogs is opened in XS Mac and then with VS2015.
-  "Select Device" dropdown for Android doesn't show several devices which have same model number.
-  DocSync fails or waits indefinitely during "extracting" if username contains spaces.
-  Show ipa file on Build server fails if the Assembly name does not match the Project name.
-  **Known issues:**
-    
-  After installing this version, connecting to the Mac might ask for Mac credentials once, even if it's a known Mac.
-  Downgrading or switching channels after installing this version can require deleting files id_rsa and id_rsa.pub from "%localappdata%/Xamarin/Monotouch" to connect successfully with Mac servers using older versions.
-  **New Requirements for Xamarin Designer:**
-  <u>Only if Visual Studio 2015 is not installed</u> on the same machine, and for using the Xamarin designer on Visual Studio 2012 or 2013, the following products are required:
-    
-  [Microsoft .Net 4.6.](https://www.microsoft.com/en-us/download/details.aspx?id=48137)
-  [Microsoft MSBuild Tools 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48159)


#### XVS 4.1.0.462

-  Simplified licensing checks, making any Xamarin License to prevail over running VS SKU.
-  Fixes issue building tvOS application with "Build ad-hoc/enterprise package" on "AppStore" config.
-  Getting error deploying WatchKit app in Visual Studio
-  "Method not found: 'System.Reactive.Subjects.AsyncSubject`1&lt;!!0&gt; System.Reactive.Linq.Observable.GetAwaiter(System.IObservable`1&lt;!!0&gt;)'." prevents successful build host connection.
-  "Building from the command-line requires a Business license." When building iOS App via TFS
-  Updated iOS Binding Project template.
-  Assets Catalog: Adding multiple Image sets in Sprite and double clicking it results in VS Crash.
-  IPA files are being created in a sub folder, not in the root build folder. This causes the build to fail
-  iOS Embedded Framework Support: Getting build error, after adding Native Static Reference ".a" file to an iOS project in VS.
-  "The Collection View cell" file template has been removed from VS for tvOS project.
-  Visual Studio not recognizing native library.
-  User is not allowed to add an image set to SpriteAtlas, if there is an imageset already added to AssetCatalog
-  Not getting icon on deploying watchkit application in notification mode in VS.
-  Getting error with "Unit Test App(iOS)" template on VS.
-  Assets Catalogs: Data Set properties panel contains image properties.
-  Adding new Sprite Atlas doesn't reflect under Asset catalog [in unsaved Media state]
-  DocSync crashing, missing CommandLine.dll
-  Added Support for PCL Profiles 44, 151
-  **Known issues:**
-    
-  "Unable to connect to Address='192.168.1.2:22' with User='macuser'" or "Private key is encrypted but passphrase is empty." after downgrading back to the previous version Xamarin 4.0. This is an  *intentional* change due to a new security feature in Xamarin 4.1.  **Recommended fix** : Delete  **id_rsa** and  **id_rsa.pub** from  **%LOCALAPPDATA%\Xamarin\MonoTouch** , and then reconnect to the Mac build host.
-  After installing this version, connecting to the Mac might ask for Mac credentials once, even if it's a known Mac.
-  **New Requirements for Xamarin Designer:**
-  <u>Only if Visual Studio 2015 is not installed</u> on the same machine, and for using the Xamarin designer on Visual Studio 2012 or 2013, the following products are required:
-    
-  [Microsoft .Net 4.6.](https://www.microsoft.com/en-us/download/details.aspx?id=48137)
-  [Microsoft MSBuild Tools 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48159)


#### XVS 4.1.0.313

-  Updates Xamarin for Visual Studio licensing checks  [as announced](https://blog.xamarin.com/xamarin-for-all/) on Microsoft //Build 2016.
-  User is not able to deploy WatchKit Application in Notification Mode with VS
-  IPA file for tvOS gets uploaded successfully but getting error "This build is invalid" in "iTune Connect".
-  iOS 6 and iOS 7 devices are not displayed in the devices drop-down menu.
-  On fresh install, user is unable to connect with Mac.
-  Clicking on "Xamarin for Visual Studio Update Available" notification toolbar icon in the system tray has no effect.
-  Fixed "Shared Links Extensions (iOS)" project template name.
-  iOS Assets Catalog: Fixed issue saving Sprite Atlas after renaming.
-  iOS Assets Catalog: Fixed issue after adding an image into Sprite Atlas showing size 0x0 for WatchKit projects.
-  iOS Assets Catalog: Fixed issue after adding new Sprite Atlas, the view is not refreshed.
-  Known issues:
-    
-  After installing this version, connecting to the Mac will ask for Mac credentials once, even if it's a known Mac.
-  Downgrading or switching channels after installing this version can require deleting files id_rsa and id_rsa.pub from "%localappdata%/Xamarin/Monotouch" to connect successfully with Mac servers using older versions.


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
