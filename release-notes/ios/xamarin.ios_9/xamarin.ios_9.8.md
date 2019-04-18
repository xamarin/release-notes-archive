---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 9.8"
---

version:9.8.1
releasedate:2016-06-21

<div class="note">
	<b>Classic Profile Deprecation:</b>
	As new platforms are added in Xamarin.iOS we are starting to gradually deprecate features from the classic profile (monotouch.dll).
	
	In this release the non-NRC (new-ref-count) option was removed. NRC has always been enabled for all unified applications (i.e. non-NRC was never an option) and has no known issues.
	
	The next release will remove the option of using Boehm as the garbage collector. This was also an option never available to unified applications.
	The complete removal of classic support is scheduled for next fall with the release of Xamarin.iOS 10.0.
</div>

Requirements
============

- The latest features and API requires Xcode 7.3 and the bundled iOS 9.3 SDK;
- Apple Xcode 7.3 requires a Mac running OSX 10.11 (El Capitan)

What's New
==========

### tvOS Support

The latest (4th) generation of AppleTV allows developers to create and submit applications to the Apple App Store.

tvOS is generally a subset of the iOS 9.x API where frameworks/API non-applicable to the AppleTV platform and deprecated API were removed. This includes:

- Accounts.framework
- AddressBook.framework
- AddressBookUI.framework
- AssetsLibrary.framework
- Contacts.framework
- ContactsUI.framework
- CoreAudioKit.framework
- CoreMIDI.framework
- CoreMotion.framework
- CoreTelephony.framework
- EventKit.framework
- ExternalAccessory.framework
- HealthKit.framework
- HomeKit.framework
- LocalAuthentication.framework
- MapKit.framework
- MessageUI.framework
- MobileCoreServices.framework
- MultipeerConnectivity.framework
- NetworkExtension.framework
- NewsstandKit.framework
- Photos.framework
- PhotosUI.framework
- PushKit.framework
- QuickLook.framework
- ReplayKit.framework
- SafariServices.framework
- Social.framework
- VideoToolbox.framework
- WatchConnectivity.framework
- WatchKit.framework
- WebKit.framework
- iAd.framework
- Audio/video input/capture API (e.g. AVFoundation.framework)
- Device orientation API (e.g. UIKit.framework)

with the addition of a few frameworks and types

- TVServices.framework;
- TVMLKit.framework;
- GCMicroGamepad* types;


Xamarin.TVOS.dll
----------------

Xamarin.iOS 9.8 supports the latest tvOS 9.2 SDK that ships with Apple's Xcode 7.3.

Along with the required API changes for tvOS several `[Obsolete]` API were removed from the new assembly.

The following document contains a list of the
[API differences between iOS and tvOS](/releases/ios/api_changes/ios-to-tvos).


### HttpClient Improvements

The `HttpClient` class can now use a native HTTP engine, instead of using Mono's `HttpWebRequest`.   The section
covers the details on what you need to be aware of.

NSUrlSessionHandler
-------------------

This release includes a new native `NSUrlSession`-based HTTP handler based on the popular [ModernHttpClient](https://github.com/paulcbetts/ModernHttpClient) open source library.

When you use `NSUrlSessionHandler`, the `HttpClient` stack will use the iOS native
`NSURLSession` class to perform all of its HTTP operations, instead of using the
.NET `HttpWebRequest`.   This has several advantages, among them, secure connections
are a lot faster, as they use the native implementation of the crypto stack, and
support for TLS 1.2 is enabled by default.    Developers need to know that by using
this new stack, the iOS 9 enforcement for secure server connection will be in effect.

This was designed to be both a transparent (no source) change and to reduce the amount of code
required for the HTTP stack. As such some, non-default, options specific to ModernHttpClient are not provided. The use of [ModernHttpClient](https://github.com/paulcbetts/ModernHttpClient) is still possible from your applications as we avoided potential names/types conflicts.

An application that removes all usage of `System.Net.WebRequest` and use `HttpClient` with the new `NSUrlSessionHandler` can reduce its size by about 850KB (per architecture) and benefit from the performance gains of the native stack.


Selecting the Default Handler
-----------------------------

To make it easier to adopt a specific handler across all `HttpClient` uses in your application Xamarin.iOS now allow you to set which handler should be used for `HttpClient`. The following options are available:

- `HttpClientHandler`: This is the fully managed `HttpClient` handler that has been shipped with previous Xamarin.iOS. It is the most compatible (features) with MS .NET and older Xamarin versions. However it's slower (e.g. encryption) and requires more code in the final application. To ensure maximum compatibility for existing applications this is the **default** handler.
- `CFNetworkHandler`: This handler uses native API (CFNetwork framework) for better performance and smaller executable size. However it requires iOS6 (or later) and it not available on watchOS. Not every `HttpClient` features/options are available;
- `NSUrlSessionHandler`: This handler uses native API (NSUrlSession) for better performance and smaller executable size. However it requires iOS7 (or later) and does not support every `HttpClient` features/options;

Selecting which default `HttpClient` handler can be done using the project's options in your IDE (XS or VS) or by providing `mtouch` with either `--http-message-handler=HttpClientHandler`, `--http-message-handler=CFNetworkHandler` or `--http-message-handler=NSUrlSessionHandler` command-line arguments.


### Apple TLS support

You can now select which **Transport Layer Security** (TLS) provider you want to use inside your iOS application, e.g. to support `SslStream`, which provides the SSL/TLS support for `System.Net.WebRequest` and it's friends.

By default your projects will now use the new **Apple TLS stack** which uses native code (better performance) and support the newest TLS 1.1 and 1.2 standards. **This is a change from previous preview releases of XI 9.8.**

You can also opt-out and continue to use the managed **Mono TLS** stack, which only supports up to TLS 1.0. This will continue to use the same stack that was shipped in previous versions of Xamarin.iOS.

Selecting which TLS provider to use can be can be done using the project's options in your IDE (XS or VS) or by providing `mtouch` with either `--tls-provider=legacy` or `--tls-provider=appletls` command-line arguments.


### Other Changes

Generic versions of NS* collections
-----------------------------------

This version adds generic versions of the following types:
- `NSArray<TKey>`
- `NSOrderedSet<TKey>`
- `NSMutableOrderedSet<TKey>`


Size Reduction
--------------

The AOT compiler now produces `{arch}.aotdata` files alongside the assemblies. This reduce the size of the native executable and helps when natively linking large object files, particularly for 32 bits architectures.


Resource Assemblies
-------------------

Applications using resource assemblies should see a decrease in their size as the `.resources.dll` files are now deduplicated inside fat (32/64 bits) applications.


### Xamarin.iOS 9.8.2 (Service Release 1)

What's New
==========

* Initial support for [netstandard](https://github.com/dotnet/corefx/blob/master/Documentation/architecture/net-platform-standard.md#list-of-net-corefx-apis-and-their-associated-net-platform-standard-version)

The following document contains a complete list of the
[API changes from 9.8.0 to 9.8.2](/releases/ios/api_changes/from_9.8.0_to_9.8.2).

Bug Fixes
=========

* [41597](https://bugzilla.xamarin.com/show_bug.cgi?id=41597) - \[tvos\] The SDK version for _LC\_VERSION\_MIN\_TVOS_ in Mono.framework/Mono has an invalid value of _73_, causing Xamarin tvOS apps to be rejected from the app store.
* [41653](https://bugzilla.xamarin.com/show_bug.cgi?id=41653) - [AppleTls] Call SSLSetPeerDomainName() to support virtual domains
* [41655](https://bugzilla.xamarin.com/show_bug.cgi?id=41655) - \[mtouch\] "Could not kill the application ... You may have to kill the application manually ... Details:  Failed to start Instruments daemon on device" when attempting to deploy to certain iOS devices in certain environments.  The fix for this issue provides a fallback mechanism that automatically tries the old (Xamarin.iOS 9.6) approach for launching apps if the new Instruments-based approach fails.
* [41656](https://bugzilla.xamarin.com/show_bug.cgi?id=41656) - \[httpclient\] Unlike other handlers `NSUrlSessionHandler.AllowAutoRedirect` is `false` by default
* \[httpclient\] Unlike other handlers, `CFNetworkHandler.CookieContainer` is `null` by default.
* [41684](https://bugzilla.xamarin.com/show_bug.cgi?id=41684) - \[coregraphics\] `CGRect.Inflate()` returns an unmodified `CGRect` regardless of the input parameters.
* [41963](https://bugzilla.xamarin.com/show_bug.cgi?id=41963) - \[msbuild\] The fix for non-public Bug 35667 changes the output path of **.ipa** packages to omit version numbers and instead place the packages in timestamped subdirectories.  That change breaks many CI scripts that depend on the old location of the **.ipa** files.  This release adds a new `IpaPackageDir` MSBuild property to make it easier to customize the **.ipa** file output location when adjusting CI scripts to account for that change.  For additional details, see the "New MSBuild property `IpaPackageDir`" section below.

#### New MSBuild property `IpaPackageDir` to customize **.ipa** output location

A new MSBuild property `IpaPackageDir` has been added to make it easy to customize the **.ipa** file output location.  If `IpaPackageDir` is set to a custom location, the **.ipa** file will be placed in that location instead of the default timestamped subdirectory.  This feature can be used to simplify the changes needed to handle the Xamarin.iOS 9.8 breaking change in the default **.ipa** output location ([41963](https://bugzilla.xamarin.com/show_bug.cgi?id=41963)).  There are several possible ways to use the new property.

- For example, to output the **.ipa** file to the old default directory (as in Xamarin.iOS 9.6 and lower), you can set the `IpaPackageDir` property to `$(OutputPath)` using one of the following approaches.  Both approaches are compatible with all Unified API Xamarin.iOS builds, including IDE builds as well as command line builds that use `xbuild`, `msbuild`, or `mdtool`.

    - The first option is to set the `IpaPackageDir` property within a `<PropertyGroup>` element in an MSBuild file.  For example, you could add the following `<PropertyGroup>` to the bottom of the iOS app project `.csproj` file (just before the closing `</Project>` tag):

            <PropertyGroup>
              <IpaPackageDir>$(OutputPath)</IpaPackageDir>
            </PropertyGroup>

    - An even better approach is to add a `<IpaPackageDir>` element to the bottom of the existing `<PropertyGroup>` that corresponds to the configuration used to build the **.ipa** file.  This is "better" because it will prepare the project for future compatibility with a planned setting on the _iOS IPA Options_ project properties page.

        If you currently use the "Release|iPhone" configuration to build the **.ipa** file, the complete updated property group might look similar to the following:

            <PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Release|iPhone' ">
              <Optimize>true</Optimize>
              <OutputPath>bin\iPhone\Release</OutputPath>
              <ErrorReport>prompt</ErrorReport>
              <WarningLevel>4</WarningLevel>
              <ConsolePause>false</ConsolePause>
              <CodesignKey>iPhone Developer</CodesignKey>
              <MtouchUseSGen>true</MtouchUseSGen>
              <MtouchUseRefCounting>true</MtouchUseRefCounting>
              <MtouchFloat32>true</MtouchFloat32>
              <CodesignEntitlements>Entitlements.plist</CodesignEntitlements>
              <MtouchLink>SdkOnly</MtouchLink>
              <MtouchArch>ARMv7, ARM64</MtouchArch>
              <MtouchHttpClientHandler>HttpClientHandler</MtouchHttpClientHandler>
              <MtouchTlsProvider>Default</MtouchTlsProvider>
              <PlatformTarget>x86</PlatformTarget>
              <BuildIpa>true</BuildIpa>
              <IpaPackageDir>$(OutputPath)</IpaPackageDir>
            </PropertyGroup>

- An alternate technique for `msbuild` or `xbuild` command line builds is to add a `/p:` command line argument to set the `IpaPackageDir` property.  In this case note that `msbuild` does not expand `$()` expressions passed in on the command line, so it is not possible to use the `$(OutputPath)` syntax.  You must instead provide a full path name.  Mono's `xbuild` command _does_ expand `$()` expressions, but it is still preferable to use a full path name because `xbuild` will eventually be deprecated in favor of the [cross-platform version of `msbuild`](http://www.mono-project.com/docs/about-mono/releases/4.4.0/#msbuild-preview-for-os-x).

    A complete example that uses this approach might look similar to the following on Windows:

        msbuild /p:Configuration="Release" /p:Platform="iPhone" /p:ServerAddress="192.168.1.3" /p:ServerUser="macuser" /p:IpaPackageDir="%USERPROFILE%\Builds" /t:Build SingleViewIphone1.sln

    Or the following on Mac:

        xbuild /p:Configuration="Release" /p:Platform="iPhone" /p:IpaPackageDir="$HOME/Builds" /t:Build SingleViewIphone1.sln

### Xamarin.iOS 9.8.1 (Service Release 0)

Known Issues
============

* [41963](https://bugzilla.xamarin.com/show_bug.cgi?id=41963) - The fix for non-public Bug 35667 changes the output path of `.ipa` packages to omit version numbers and instead place the packages in timestamped subdirectories.  (This more closely resembles Xcode's default output paths for `.ipa` packages.)  **CI scripts that depend on the old location of the `.ipa` files will need to be updated to accommodate this change**.  The final path of the `.ipa` package can be obtained from the `IpaPackagePath` MSBuild property any time after the `_CoreCreateIpa` target has run.  For example, if you add the following lines to the bottom of an iOS app project `.csproj` file (just before the closing `</Project>` tag), the path of the `.ipa` package will be printed at the end of the build output:

        <PropertyGroup>
          <BuildDependsOn>
            $(BuildDependsOn);
            DisplayIpaPackagePath
          </BuildDependsOn>
        </PropertyGroup>
        <Target Name="DisplayIpaPackagePath">
          <Message Text="IpaPackagePath: $(IpaPackagePath)" />
        </Target>

* [41684](https://bugzilla.xamarin.com/show_bug.cgi?id=41684) - `CGRect.Inflate()` returns an unmodified `CGRect` regardless of the input parameters.  **Possible temporary workaround**: Modify the frame of the `CGRect` by hand using the `X`, `Y`, `Width`, and `Height` properties.

Bug Fixes
=========

* [41206](https://bugzilla.xamarin.com/show_bug.cgi?id=41206) - [AppleTls] Correctly handle large read/write sizes
* [41697](https://bugzilla.xamarin.com/show_bug.cgi?id=41697) - [AppleTls] Certain calls to `HttpClient.SendAsync()` can hit a delay of about 60 seconds before completing if using the new default _Apple TLS_ setting for _SSL/TLS implementation_ (same fix as #41206)
* [41319](https://bugzilla.xamarin.com/show_bug.cgi?id=41319) - [registrar] "initWithCoder:' has been explicitly marked unavailable"
* [41782](https://bugzilla.xamarin.com/show_bug.cgi?id=41782) - [mono] "System.Net.WebException: Error: NameResolutionFailure" when attempting web requests with certain raw IP addresses.
* [41874](https://bugzilla.xamarin.com/show_bug.cgi?id=41874) - [mono] Reflection throws `AmbiguousMatchException` when calling `GetProperty()` on a class that inherits from a generic base class.


### Xamarin.iOS 9.8

The following document contains a complete list of the
[API changes from 9.6.0 to 9.8.0](/releases/ios/api_changes/from_9.6.0_to_9.8.0).

Known Issues
============

* [41206](https://bugzilla.xamarin.com/show_bug.cgi?id=41206) - "Mono.Security.Interface.TlsException: Unknown Secure Transport error \`ClosedGraceful'" in certain environments when using the _Managed_ setting for _HttpClient implementation_ in combination with the new default _Apple TLS_ setting for _SSL/TLS implementation_.  **Workaround**: Under _Project Options > iOS Build_, either change the _SSL/TLS implementation_ setting back to the old default _Mono (TLS v1.0)_, or set the _HttpClient implementation_ to one of the new _CFNetwork_ or _NSUrlSession_ options.

* [41697](https://bugzilla.xamarin.com/show_bug.cgi?id=41697) - Certain calls to `HttpClient.SendAsync()` can hit a delay of about 60 seconds before completing if using the new default _Apple TLS_ setting for _SSL/TLS implementation_.  Based on the information gathered so far, it seems the issue might only affect HTTPS requests that use authorization headers.  **Workaround**: Under _Project Options > iOS Build_, change the _SSL/TLS implementation_ setting back to the old default _Mono (TLS v1.0)_.

* [41782](https://bugzilla.xamarin.com/show_bug.cgi?id=41782) - "System.Net.WebException: Error: NameResolutionFailure" when attempting web requests with certain raw IP addresses.  This is a bug in Mono, so it affects all platforms iOS, Android, and Mac.  **Partial temporary workaround**: If possible, use domain names rather than raw IP addresses for the web requests.

* [41963](https://bugzilla.xamarin.com/show_bug.cgi?id=41963) - The fix for non-public Bug 35667 changes the output path of `.ipa` packages to omit version numbers and instead place the packages in timestamped subdirectories.  (This more closely resembles Xcode's default output paths for `.ipa` packages.)  **CI scripts that depend on the old location of the `.ipa` files will need to be updated to accommodate this change**.  The final path of the `.ipa` package can be obtained from the `IpaPackagePath` MSBuild property any time after the `_CoreCreateIpa` target has run.  For example, if you add the following lines to the bottom of an iOS app project `.csproj` file (just before the closing `</Project>` tag), the path of the `.ipa` package will be printed at the end of the build output:

        <PropertyGroup>
          <BuildDependsOn>
            $(BuildDependsOn);
            DisplayIpaPackagePath
          </BuildDependsOn>
        </PropertyGroup>
        <Target Name="DisplayIpaPackagePath">
          <Message Text="IpaPackagePath: $(IpaPackagePath)" />
        </Target>

* [41684](https://bugzilla.xamarin.com/show_bug.cgi?id=41684) - `CGRect.Inflate()` returns an unmodified `CGRect` regardless of the input parameters.  **Possible temporary workaround**: Modify the frame of the `CGRect` by hand using the `X`, `Y`, `Width`, and `Height` properties.

Bug Fixes
=========

* [2508](https://bugzilla.xamarin.com/show_bug.cgi?id=2508) - [foundation] Deprecate (iOS) / remove (tvOS) NSObject.[Get|Set]NativeField
* [3229](https://bugzilla.xamarin.com/show_bug.cgi?id=3229) - [foundation] Fix NSUbiquitousKeyValueStore's indexer to accept a 'string'
* [12337](https://bugzilla.xamarin.com/show_bug.cgi?id=12337) - [mtouch] Workaround 0 length files on FAT file system
* [19428](https://bugzilla.xamarin.com/show_bug.cgi?id=19428) - [coregraphics] Add missing CGPath methods
* [24212](https://bugzilla.xamarin.com/show_bug.cgi?id=24212) - [corefoundation] Provide CFBundle bindings
* [24677](https://bugzilla.xamarin.com/show_bug.cgi?id=24677) - [registrar] Report an error if a type is used that isn't present in the current SDK
* [28610](https://bugzilla.xamarin.com/show_bug.cgi?id=28610) - [audiotoolbox] AudioQueue.AudioStreamPacketDescription property has ambiguous name
* [29977](https://bugzilla.xamarin.com/show_bug.cgi?id=29977) - [security] Add SecItem.ReturnData when querying several SecRecord
* [31427](https://bugzilla.xamarin.com/show_bug.cgi?id=31427) - [foundation] Make NSSession.CreateDownloadTaskAsync keep track of the file so that it's not deleted too early
* [31484](https://bugzilla.xamarin.com/show_bug.cgi?id=31484) - [audiotoolbox] AudioConverter properties unnecessary read-only
* [32084](https://bugzilla.xamarin.com/show_bug.cgi?id=32084) - [registrar] Sanitize exported names a bit better
* [32511](https://bugzilla.xamarin.com/show_bug.cgi?id=32511) - [registrar] Fix use properties on JSValue objects
* [33695](https://bugzilla.xamarin.com/show_bug.cgi?id=33695) - [mtouch] Provide better error message for kApplicationVerificationFailedError
* [33709](https://bugzilla.xamarin.com/show_bug.cgi?id=33709) - [objcruntime] Add a ctor to Protocol so that protocols can be marshalled
* [33789](https://bugzilla.xamarin.com/show_bug.cgi?id=33789) - [runtime] Disable the GC pump when a profiler is attached
* [33800](https://bugzilla.xamarin.com/show_bug.cgi?id=33800) - [mtouch] Add MT1110 for when the app couldn't be launched due to lack of trust
* [34106](https://bugzilla.xamarin.com/show_bug.cgi?id=34106) - [simulator] Resolve symlinks when checking if a running simulator matches the simulator we want to launch
* [34313](https://bugzilla.xamarin.com/show_bug.cgi?id=34313) - [mtouch] Improve MT1019 / 0xe8008016 error to suggest the device might not be part of the current provisioning profile
* [34363](https://bugzilla.xamarin.com/show_bug.cgi?id=34363) - [msbuild] Explicitly resolve more paths to their real paths
* [34372](https://bugzilla.xamarin.com/show_bug.cgi?id=34372) - [healthkit] Add missing constant (#define) for HKAnchoredObjectQueryNoAnchor
* [34378](https://bugzilla.xamarin.com/show_bug.cgi?id=34378) - [mtouch] Detect and report properly when trying to export structures containing classes
* [34449](https://bugzilla.xamarin.com/show_bug.cgi?id=34449) - [foundation] Expose NSSetService.GetStreams
* [34464](https://bugzilla.xamarin.com/show_bug.cgi?id=34464) - [foundation] NSOrderedSet has wrong implementations for == and != operators
* [34519](https://bugzilla.xamarin.com/show_bug.cgi?id=34519) - [runtime] Don't create a XamarinAssociatedObject to hold a gchandle if there's no gchandle to hold
* [34687](https://bugzilla.xamarin.com/show_bug.cgi?id=34687) - [msbuild] strip depends on xcode-select path
* [34806](https://bugzilla.xamarin.com/show_bug.cgi?id=34806) - [registrar] Show a nice error if the user tries to export a property that matches an Objective-C keyword
* [34913](https://bugzilla.xamarin.com/show_bug.cgi?id=34913) - [uikit] Add missing UITextInput SelectionAffinity property
* [35011](https://bugzilla.xamarin.com/show_bug.cgi?id=35011) - [foundation] Add missing members for NSFileVersion
* [35013](https://bugzilla.xamarin.com/show_bug.cgi?id=35013) - [foundation] Add missing members for NSCalendar
* [35030](https://bugzilla.xamarin.com/show_bug.cgi?id=35030) - [mtouch] Xcode path with space causes build failure
* [35048](https://bugzilla.xamarin.com/show_bug.cgi?id=35048) - [coretext] Fix char marshaling in CTFontGetGlyphsForCharacters
* [35214](https://bugzilla.xamarin.com/show_bug.cgi?id=35214) - [msbuild] Don't try to parse device-specific build properties for WatchOS apps
* [35283](https://bugzilla.xamarin.com/show_bug.cgi?id=35283) - [generator] Allow processing enums that lives outside a namespaces
* [35304](https://bugzilla.xamarin.com/show_bug.cgi?id=35304) - [mtouch] Improve MT0034 to detect more variations of incorrect references
* [35372](https://bugzilla.xamarin.com/show_bug.cgi?id=35372) - [linker] Don't remove external module references from non-linked assemblies
* [35458](https://bugzilla.xamarin.com/show_bug.cgi?id=35458) - [registrar] Call the super's constructor if we already have a managed object
* [35562](https://bugzilla.xamarin.com/show_bug.cgi?id=35562) - [mtouch/mmp] Use full paths in DllImports
* [35599](https://bugzilla.xamarin.com/show_bug.cgi?id=35599) - [uikit] Add UIControl event for PrimaryActionTriggered
* [35648](https://bugzilla.xamarin.com/show_bug.cgi?id=35648) - [coreanimation] Treat CALayer subclasses as toggle ref objects
* [35825](https://bugzilla.xamarin.com/show_bug.cgi?id=35825) - [coretext] Add missing CTFontManagerCreateFontDescriptorsFromURL binding
* [35829](https://bugzilla.xamarin.com/show_bug.cgi?id=35829) - [cfnetwork] Read data every time we get a HasBytesAvailable event
* [35846](https://bugzilla.xamarin.com/show_bug.cgi?id=35846) - [uikit] Fix wrong signature for UIPopoverPresentationControllerDelegate.WillRepositionPopover
* [35855](https://bugzilla.xamarin.com/show_bug.cgi?id=35855) - [aot] Fix support for runtime invokes to array accessors of reference arrays
* [35864](https://bugzilla.xamarin.com/show_bug.cgi?id=35864) - [mtouch] Only allow -bitcode if -llvm is also provided
* [35924](https://bugzilla.xamarin.com/show_bug.cgi?id=35924) - [foundation] Allow null in NSObject *Protocol* members
* [35946](https://bugzilla.xamarin.com/show_bug.cgi?id=35946) - [mtouch] The --enable-repl option should give an error if linking is enabled
* [36148](https://bugzilla.xamarin.com/show_bug.cgi?id=36148) - [registrar] Only upper-case a-z when uppercasing the first character of getters for setters.
* [36208](https://bugzilla.xamarin.com/show_bug.cgi?id=36208) - [simulator] Watch 1 apps don't have to be named 'WatchApp.app'
* [36247](https://bugzilla.xamarin.com/show_bug.cgi?id=36247) - [aot] Escape some characters in method names to avoid assembler problems with obfuscated assemblies
* [36263](https://bugzilla.xamarin.com/show_bug.cgi?id=36263) - [llvm] Zero extend array indexes when targeting llvm, codegen problem on arm64
* [36293](https://bugzilla.xamarin.com/show_bug.cgi?id=36293) - [mtouch] Add -framework and -l[ibrary] based on assemblies too
* [36370](https://bugzilla.xamarin.com/show_bug.cgi?id=36370) - [aot] Add instances of EnumEqualityCompater<T> for all integer types
* [36457](https://bugzilla.xamarin.com/show_bug.cgi?id=36457) - [generator] Add support for returning System.String from delegates/blocks
* [36505](https://bugzilla.xamarin.com/show_bug.cgi?id=36505) - [mtouch] Add support for pseudo frameworks that contain static libraries
* [36571](https://bugzilla.xamarin.com/show_bug.cgi?id=36571) - [security] Fix SecAccessControl to behave like an INativeObject
* [36575](https://bugzilla.xamarin.com/show_bug.cgi?id=36575) - [metalperformanceshaders] Expose missing MPSRectNoClip
* [36577](https://bugzilla.xamarin.com/show_bug.cgi?id=36577) - [linker] Re-saving forwarders (e.g. PCL facades) must exclude removed types
* [36723](https://bugzilla.xamarin.com/show_bug.cgi?id=36723) - [aot] Fix the check in mono_aot_get_plt_entry () for thumb code
* [36768](https://bugzilla.xamarin.com/show_bug.cgi?id=36768) - [coreimage] Add missing FromContext(EAGLContext) overload that accept a CIContextOptions
* [36992](https://bugzilla.xamarin.com/show_bug.cgi?id=36992) - [security] Fix RawSign not to predict the required size (as it won't work for EC)
* [37004](https://bugzilla.xamarin.com/show_bug.cgi?id=37004) - [msbuild] CreateAssetPackManifest: Fix creation of OnDemandResources.plist
* [37079](https://bugzilla.xamarin.com/show_bug.cgi?id=37079) - [jit] Fix the support for gshared types in mini_emit_initobj ()
* [37105](https://bugzilla.xamarin.com/show_bug.cgi?id=37105) - [runtime] Wrap threadpool work in an NSAutoreleasePool
* [37118](https://bugzilla.xamarin.com/show_bug.cgi?id=37118) - [linker] Avoid an NRE when rewriting bindings
* [37121](https://bugzilla.xamarin.com/show_bug.cgi?id=37121) - [social] Add missing async version of SLRequest.PerformRequest
* [37174](https://bugzilla.xamarin.com/show_bug.cgi?id=37174) - [uikit] Make UITextAttributes thread safe
* [37187](https://bugzilla.xamarin.com/show_bug.cgi?id=37187) - [generator] Be a bit more defensive when converting pointers to CMSampleBuffers
* [37236](https://bugzilla.xamarin.com/show_bug.cgi?id=37236) - [llvm][arm64] Fix hfa structures / skipped fp registers
* [37246](https://bugzilla.xamarin.com/show_bug.cgi?id=37246) - [bcl][system] Make SmtpClient fallback to it's old behaviour if the hostname cannot be resolved
* [37273](https://bugzilla.xamarin.com/show_bug.cgi?id=37273) - [llvm] Disable support for nested clauses
* [37310](https://bugzilla.xamarin.com/show_bug.cgi?id=37310) - [healthkit] Fix incorrect signature for HKStatisticsCollectionQuery.StatisticsUpdateHandler
* [37412](https://bugzilla.xamarin.com/show_bug.cgi?id=37412) - [llvm] Fix the linking of the bblocks containing endfinally instructions
* [37536](https://bugzilla.xamarin.com/show_bug.cgi?id=37536) - [coregraphics] Copy the input buffer in CGDataProvider when we don't own it
* [37596](https://bugzilla.xamarin.com/show_bug.cgi?id=37596) - [uikit] Use the correct protocol type for UIImagePickerController's ImagePickerControllerDelegate and NavigationControllerDelegate properties
* [37611](https://bugzilla.xamarin.com/show_bug.cgi?id=37611) - [mtouch] Gather assemblies referenced only by custom attributes
* [37670](https://bugzilla.xamarin.com/show_bug.cgi?id=37670) - [objcruntime] Don't return a non-user type from Runtime.TryGetNSObject if it's being collected
* [37732](https://bugzilla.xamarin.com/show_bug.cgi?id=37732) - [bcl][system] Avoid reflection use to create NtlmSession
* [37774](https://bugzilla.xamarin.com/show_bug.cgi?id=37774) - [simulator][odr] Launch asset provider after installing the app
* [37993](https://bugzilla.xamarin.com/show_bug.cgi?id=37993) - [foundation] Fix support for NSFileManager.ProtectionKey
* [38259](https://bugzilla.xamarin.com/show_bug.cgi?id=38259) - [coreimage] Fix CIFilter check for inputImage support
* [38379](https://bugzilla.xamarin.com/show_bug.cgi?id=38379) - [llvm] Zero extend unsigned enum arguments
* [38484](https://bugzilla.xamarin.com/show_bug.cgi?id=38484) - [coremedia] Fix constructor for CMVideoFormatDescription
* [38612](https://bugzilla.xamarin.com/show_bug.cgi?id=38612) - [registrar] 'export' is a keyword in Objective-C, so report it as such
* [38742](https://bugzilla.xamarin.com/show_bug.cgi?id=38742) - [opentk] Add ES30 overload to CVOpenGLESTextureCache.TextureFromImage

* [7728](https://bugzilla.xamarin.com/show_bug.cgi?id=7728) - [mtouch] Validate that an app is signed with a valid provisioning profile for a device **[9.8.0.43+]**
* [35888](https://bugzilla.xamarin.com/show_bug.cgi?id=35888) - [registrar] Detect 'template' as an ObjC++ keyword **[9.8.0.43+]**
* [37527](https://bugzilla.xamarin.com/show_bug.cgi?id=37527) - [generator] Provide more information when Delegates are not correctly defined **[9.8.0.43+]**
* [37563](https://bugzilla.xamarin.com/show_bug.cgi?id=37563) - [linker] Queryable.AsQueryable uses reflection and needs help **[9.8.0.43+]**
* [38244](https://bugzilla.xamarin.com/show_bug.cgi?id=38244) - [msbuild] Always add unpacked resources from library projects **[9.8.0.43+]**
* [38267](https://bugzilla.xamarin.com/show_bug.cgi?id=38267) - [msbuild] Fix actool task **[9.8.0.43+]**
* [38434](https://bugzilla.xamarin.com/show_bug.cgi?id=38434) - [msbuild] ACToolTask - Changes output AssetPack plist path to relative **[9.8.0.43+]**
* [38542](https://bugzilla.xamarin.com/show_bug.cgi?id=38542) - [mtouch] Take into account assemblies added by the linker when loading cached linker results **[9.8.0.43+]**
* [38673](https://bugzilla.xamarin.com/show_bug.cgi?id=38673) - [msbuild] Validate each extension's CFBundleShortVersionString and CFBundleVersion **[9.8.0.43+]**
* [38834](https://bugzilla.xamarin.com/show_bug.cgi?id=38834) - [mtouch] libapp/extension/watch-extension.a need to be force-loaded **[9.8.0.43+]**
* [38886](https://bugzilla.xamarin.com/show_bug.cgi?id=38886) - [avfoundation] AVCaptureMetadataOutput.SetDelegate should accept null parameters **[9.8.0.43+]**
* [39137](https://bugzilla.xamarin.com/show_bug.cgi?id=38267) - [aot] Set null uw_info for tramps without unwind info **[9.8.0.43+]**
* [39179](https://bugzilla.xamarin.com/show_bug.cgi?id=39179) - [mtouch][tvos] Map P/Invokes from openal32 to OpenAL **[9.8.0.43+]**

* [35667](https://bugzilla.xamarin.com/show_bug.cgi?id=35667) - [msbuild] Output the *.ipa w/o a version and inside of a timestamped directory **[9.8.0.58+]**
* [39427](https://bugzilla.xamarin.com/show_bug.cgi?id=39427) - [msbuild] Add back logic for the obsoleted ObjCBindingNativeFramework build action **[9.8.0.58+]**

* [39706](https://bugzilla.xamarin.com/show_bug.cgi?id=39706) - [spritekit] Provide better bindings for SKShapeNode.FromPoints **[9.8.0.156+]**
* [39822](https://bugzilla.xamarin.com/show_bug.cgi?id=39822) - [audiounit] Have AUGraph implements INativeObject to ease 3rd party bindings **[9.8.0.156+]**
* [39869](https://bugzilla.xamarin.com/show_bug.cgi?id=39869) - [msbuild] Don't duplicate actool specification entries for on-demand resources **[9.8.0.156+]**

* [13538](https://bugzilla.xamarin.com/show_bug.cgi?id=13538) - [bcl] Avoid printing debug messages to stdout in the default trace listener when a debugger is connected **[9.8.0.236+]**
* [34880](https://bugzilla.xamarin.com/show_bug.cgi?id=34880) - [uikit] UIImage.Size will put the UIImage on an autorelease pool, so make sure we free that early **[9.8.0.236+]**
* [40019](https://bugzilla.xamarin.com/show_bug.cgi?id=40019) - [photos] Add missing enum SmartAlbumSelfPortraits and SmartAlbumSelfPortraits values **[9.8.0.236+]**

* [39974](https://bugzilla.xamarin.com/show_bug.cgi?id=39974) - [coremedia] Do not free provided (like managed) memory given to CMBlockBuffer **[9.8.0.244+]**
* [40108](https://bugzilla.xamarin.com/show_bug.cgi?id=40108) - [runtime] ConditionalWeakTable collects values when the key is kept alive as toggle-ref **[9.8.0.244+]**

* [18334](https://bugzilla.xamarin.com/show_bug.cgi?id=18334) - [foundation] Add "missing" NSAttributedString::attributedStringWithAttachment **[9.8.0.294+]**
* [37979](https://bugzilla.xamarin.com/show_bug.cgi?id=37979) - [msbuild] ACTool task needs to know if it is a WatchOS1 app to use correct --platform value **[9.8.0.294+]**
* [39172](https://bugzilla.xamarin.com/show_bug.cgi?id=39172) - [jit] Avoid returning trampolines from mini_jit_info_table_find since they might have no unwind info **[9.8.0.294+]**
* [40137](https://bugzilla.xamarin.com/show_bug.cgi?id=40137) - [msbuild] Set an ArchiveDir property when the archive target is run **[9.8.0.294+]**
* [40318](https://bugzilla.xamarin.com/show_bug.cgi?id=40318) - [msbuild] Application with entitlements do not start on simulator anymore **[9.8.0.294+]**
* [40458](https://bugzilla.xamarin.com/show_bug.cgi?id=40458) - [linker] Do not remove parameter names (metadata) if it's used thru reflection **[9.8.0.294+]**
* [40534](https://bugzilla.xamarin.com/show_bug.cgi?id=40534) - [msbuild] iOS build targets cannot be used with non-default keychain **[9.8.0.294+]**

* [40535](https://bugzilla.xamarin.com/show_bug.cgi?id=40535) - [Xamarin.Hosting] Make errors 1901 and 1902 warnings **[9.8.0.318+]**
* [40641](https://bugzilla.xamarin.com/show_bug.cgi?id=40641) - [linker] Fix debugging of watchOS apps when **link all** is used **[9.8.0.318+]**
* [40774](https://bugzilla.xamarin.com/show_bug.cgi?id=40774) - [repl] Ensure Aes.Create works, otherwise SSL/TLS will break **[9.8.0.318+]**
* [40961](https://bugzilla.xamarin.com/show_bug.cgi?id=40961) - [msbuild] Don't treat unsupported iCloud entitlements as errors in the build **[9.8.0.318+]**
* [41019](https://bugzilla.xamarin.com/show_bug.cgi?id=41019) - [msbuild] Fixed Optimize parsing logic for BundleResources **[9.8.0.318+]**

* [40306](https://bugzilla.xamarin.com/show_bug.cgi?id=40306) - [threadpool-io] Fix crash on shutdownin System.Net.Sockets.Socket:Close_internal **[9.8.0.319+]**

