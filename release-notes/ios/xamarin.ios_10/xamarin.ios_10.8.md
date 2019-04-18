---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 10.8"
---

version:10.8.0
releasedate:2017-04-05

<div class="note">
	<b>Mono TLS Removal:</b>
	This version of Xamarin.iOS does <b>not</b> ship with the old Mono (managed) SSL/TLS provider, which
	only supported the SSLv3 and TLSv1 standards. TLS support (up to version 1.2) is provided by the 
	newer AppleTLS provider (already the default since XI 9.8 / C7).
</div>

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-1` branch, and is based on Mono 4.8.0.

### Debugging extensions on devices

We now support debugging extensions on devices (earlier versions already supported the simulator). You need to use the latest version of [Xamarin Studio](https://developer.xamarin.com/releases/studio/xamarin.studio_6.3/xamarin.studio_6.3/#Debug_App_Extensions_on_Device) or [Xamarin for Visual Studio](https://developer.xamarin.com/releases/vs/xamarin.vs_4/xamarin.vs_4.3/#mpdebugging) to enable the feature. You need to make sure a different debugging port is used for the container (main) application and each extensions.

### Memory usage and executable size improvements

We have <a href="https://github.com/xamarin/xamarin-macios/commit/7728c4cd196e605e036ecf531a8bd81072094412">reworked how managed types are registered</a> with the Objective-C runtime, improving executable size and memory usage significantly (for a sample application the executable size decreased by ~200 kb and the memory usage decreased by ~400 kb).

### Binding NSValue, NSNumber and NSString to better managed types

The `[BindAs]` attribute allows binding `NSNumber`, `NSValue` and `NSString` (enums) into more accurate C# types. The attribute can be used to create a nicer .NET API over the native API.

You can decorate properties and methods (on return value and parameters) with `[BindAs]` attributes. The only restriction is that your member **must not** be inside a `[Protocol]` or `[Model]` interface.

For example:

```
[return: BindAs (typeof (bool?))]
[Export ("shouldDrawAt:")]
NSNumber ShouldDraw ([BindAs (typeof (CGRect))] NSValue rect);
```

Would output:

```
[Export ("shouldDrawAt:")]
bool? ShouldDraw (CGRect rect) { ... }
```

Internally the generated code will do the required `bool?` <-> `NSNumber` and `CGRect` <-> `NSValue` conversions.

The `[BindAs]` attribute also supports arrays of `NSNumber` `NSValue` and `NSString` (enums).

For example:

```
[BindAs (typeof (CAScroll []))]
[Export ("supportedScrollModes")]
NSString [] SupportedScrollModes { get; set; }
```

Would output:

```
[Export ("supportedScrollModes")]
CAScroll [] SupportedScrollModes { get; set; }
```

`CAScroll` is a `NSString` backed enum, we will fetch the right `NSString` value and handle the type conversion.

Please see our [[BindAs] documentation](https://github.com/xamarin/xamarin-macios/blob/master/docs/website/binding_types_reference_guide.md#bindasattribute) to see supported conversion types.

### Single object strong notifications support 

When [Binding Notifications](https://developer.xamarin.com/guides/cross-platform/macios/binding/objective-c-libraries/#Binding_Notifications) we generate a nested class `MyClass.Notifications` that holds strongly typed notifications. In the past it was only possible to observe a notification posted to all objects.

```
var token = MyClass.Notifications.ObserverDidStart ((notification) => {
    Console.WriteLine ("Observed the 'DidStart' event!");
});
```

But now it is possible to observe a specific object notifications by using the provided overload. 

```
var token = MyClass.Notifications.ObserverDidStart (objectToObserve, (notification) => { 
    Console.WriteLine ("Observed the 'DidStart' event on objectToObserve!");
});
```

### Experimental control over native optimizations of watchOS applications

We are now providing *optional* control over the `clang` compiler optimizations used to generate **bitcode**. For a basic test, changing the default `-O2` to `-Oz` (optimize for size) reduces the application size by approximatively 5%.

This option is manually passed as an additional `mtouch` argument in the project's iOS Build options:

    --llvm-opt=assembly1.dll=<optimization> --llvm-opt=assembly2.dll=<optimization>

or it's possible to change the optimizations for all assemblies at once:

    --llvm-opt=all=<optimization>

For example:

    --llvm-opt=all=-Oz

is what showed a 5% application size reduction.

The valid options are the same ones that `clang` accepts. Keep in mind that `clang` optimization options are vast and some are not compatible with Mono and may break the application at runtime. For this release the only supported optimizations is the default set, but you can experiment and share your results on our [mailing list](http://lists.dot.net/pipermail/macios-devel/).


### Experimental support for Concurrent SGen

[Concurrent SGen](http://www.mono-project.com/docs/about-mono/releases/4.8.0/#concurrent-sgen) is now available as an experimental option. Using it GC latency should be shorter for major GCs, however memory usage might be higher.

The feature can be enabled in the project options (IDE) or manually by giving the `-sgen-conc` argument to `mtouch`.


### mtouch warnings

We've added support for treating `mtouch` warnings as errors, as well as ignoring `mtouch` warnings.

This support is modeled after the same feature in the C# compiler, and can be
configured by passing the following options as an additional mtouch argument
in the project's iOS Build options:

* `--nowarn` will disable all warnings.
* `--nowarn:30,32` will disable the warnings MT0030 and MT0032.
* `--warnaserror` will report all warnings as errors.
* `--warnaserror:30,32` will make the warnings MT0030 and MT0032 show up as errors.

### MSBuild error codes

The **7xxx** range of errors is now reserved for MSBuild errors and we started documenting the first ones. Their description include the task that generated the error as well as some troubleshooting steps when applicable. 

Note that this range of error is handled by `msbuild` (or `xbuild`) tool and the new `mtouch` options (above) cannot be used on them.

### Xamarin Analysis

We added a new rule to our project analysis tool which ensures that no IPA is generated in debug mode as it's only needed for distribution.

*As a reminder you can run the Xamarin Analysis rules from Xamarin Studio's menu bar by selecting Project > Run Code Analysis.*

### Known issues

* [53845](https://bugzilla.xamarin.com/show_bug.cgi?id=53845) - Build error: The file 'LaunchScreen.storyboard' conflicts with 'Resources/LaunchScreen.storyboard'
    * This occurs because there are multiple storyboards with the same name in the project. The fix is to remove the duplicated storyboards.

### Miscellaneous Enhancements

**Performance**

* [49087](https://bugzilla.xamarin.com/show_bug.cgi?id=49087) - [mtouch] Speed up marking types referenced in attributes
* [51298](https://bugzilla.xamarin.com/show_bug.cgi?id=51298) - [msbuild] Parallelized codesigning of *.dylibs and frameworks
* [PR1011](https://github.com/xamarin/xamarin-macios/pull/1011) - [msbuild] Do not process `mscorlib.dll` in UnpackLibraryResources

**Tools**

* [28106](https://bugzilla.xamarin.com/show_bug.cgi?id=28106) - [msbuild] Added support for `<Link>`'d ImageAsset project files
* [43165](https://bugzilla.xamarin.com/show_bug.cgi?id=43165) - [generator] Allow the use of `[Async]` attribute on `[Abstract]` decorated methods
* [43995](https://bugzilla.xamarin.com/show_bug.cgi?id=43995) - [generator] Support `[Sealed]` attribute on types (not just methods)
* [46285](https://bugzilla.xamarin.com/show_bug.cgi?id=46285) - [generator] Allow identical (numeric) values in smart enums
* [46292](https://bugzilla.xamarin.com/show_bug.cgi?id=46292) - [generator] Copy `[Obsolete]` attributes on smart enums
* [52241](https://bugzilla.xamarin.com/show_bug.cgi?id=52241) - [mtouch][watchos] Automatically enable bitcode if LLVM is enabled
* [PR1249](https://github.com/xamarin/xamarin-macios/pull/1249) - [generator] Optimize smart enums support to reduce the required metadata
* [PR1446](https://github.com/xamarin/xamarin-macios/pull/1446) - [generator] Remove internal `*Wrapper.ctor(IntPtr)` constructors
* [PR1557](https://github.com/xamarin/xamarin-macios/pull/1557) - [msbuild] Added `ProcessEnums` property for ObjC binding projects
* [PR1707](https://github.com/xamarin/xamarin-macios/pull/1707) - [generator] Have `[Wrap]` optionally generate virtual members when `IsVirtual=true`

**API**

* [33163](https://bugzilla.xamarin.com/show_bug.cgi?id=33163) - [uikit] Add convenience constructors for `UISegmentedControl`
* [39789](https://bugzilla.xamarin.com/show_bug.cgi?id=39789) - [foundation] Add a number of missing `[Flags]` in various enums

**Better error/warnings reporting**

* [PR1174](https://github.com/xamarin/xamarin-macios/pull/1174) - [generator] Improve warning about missing `[CCallback]` or `[BlockCallback]` attributes
* [PR1188](https://github.com/xamarin/xamarin-macios/pull/1188) - [msbuild] Log warnings and errors for the `ibtool --link` stage as well
* [PR1507](https://github.com/xamarin/xamarin-macios/pull/1507) - [linker] Less general `MT2001` errors in favor of precise (step/metadata) `MT2xxx` errors
* [40835](https://bugzilla.xamarin.com/show_bug.cgi?id=40835) - [mtouch] Improve enable managed linker error message (`MT0091`)
* [46552](https://bugzilla.xamarin.com/show_bug.cgi?id=46552) - [mtouch][watchos] Make `MT2015` (invalid `HttpMessageHandler`) a warning
* [51212](https://bugzilla.xamarin.com/show_bug.cgi?id=51212) - [generator] Provide a better error than `BI0000` for `TypeloadException` in NeedStret

**External Contributions**

* [PR1545](https://github.com/xamarin/xamarin-macios/pull/1545) - [msbuild] Recognize networkextension extensions (and avoid build warning)


### Bug Fixes

* [25499](https://bugzilla.xamarin.com/show_bug.cgi?id=25499) - [msbuild] Fixed EmbedMobileProvision to lookup provisions by name/uuid correctly
* [39535](https://bugzilla.xamarin.com/show_bug.cgi?id=39535) - [mtouch] Update .mdb files even if the corresponding assembly didn't change
* [46626](https://bugzilla.xamarin.com/show_bug.cgi?id=46626) - [corefoundation] Store strings in the exception data when converting `CFError` to `CFException`
* [50407](https://bugzilla.xamarin.com/show_bug.cgi?id=50407) - [foundation] Fix `NSFormatter.IsPartialStringValid`
* [51514](https://bugzilla.xamarin.com/show_bug.cgi?id=51514) - [generator] Missing `[Wrap]` from protocol/interface when parent has a `[Wrap]` itself 
* [52279](https://bugzilla.xamarin.com/show_bug.cgi?id=52279) - [corefoundation] Fix `CallbackDelegate` signature to be 32bits safe (enum)

* [52682](https://bugzilla.xamarin.com/show_bug.cgi?id=52682) - [foundation] Fix POST/PUT issues with `NSUrlSessionHandler` **(10.8.0.10+)**
* [52745](https://bugzilla.xamarin.com/show_bug.cgi?id=52745) - [msbuild] Make sure to codesign appex dylibs **(10.8.0.10+)**
* [52847](https://bugzilla.xamarin.com/show_bug.cgi?id=52847) - [msbuild] sanity check TargetiOSDevice property for conflicts **(10.8.0.10+)**
* [52851](https://bugzilla.xamarin.com/show_bug.cgi?id=52851) - [msbuild] Ignore `.DS_Store` files when cloning asset catalogs **(10.8.0.10+)**
* [52860](https://bugzilla.xamarin.com/show_bug.cgi?id=52860) - [msbuild] Index into the correct item array when printing an error message **(10.8.0.10+)**
* [52868](https://bugzilla.xamarin.com/show_bug.cgi?id=52868) - [registrar] Fix generic argument check to allow INativeObject **(10.8.0.10+)**

* [52758](https://bugzilla.xamarin.com/show_bug.cgi?id=52758) - [msbuild] Ensure the MainAssembly path is absolute **(10.8.0.20+)**
* [53007](https://bugzilla.xamarin.com/show_bug.cgi?id=53007) - [msbuild] Run the _ComputeTargetArchitectures target before cleaning **(10.8.0.20+)**
* [53066](https://bugzilla.xamarin.com/show_bug.cgi?id=53066) - [mono] Fix a MT3001 Could not AOT the assembly error **(10.8.0.20+)**
* [53176](https://bugzilla.xamarin.com/show_bug.cgi?id=53176) - [msbuild] Fixed PathUtils.AbsoluteToRelative() logic **(10.8.0.20+)**
* [53232](https://bugzilla.xamarin.com/show_bug.cgi?id=53232) - [mtouch] Don't put frameworks in WatchKit 1 extensions **(10.8.0.20+)**

* [53174](https://bugzilla.xamarin.com/show_bug.cgi?id=53174) - [uikit] Fix contest between `UITextField.Ended[WithReason]` events **(10.8.0.26+)**
* [53303](https://bugzilla.xamarin.com/show_bug.cgi?id=53303) - [msbuild] Use stamp files to force container app's `_CompileToNative` **(10.8.0.26+)**

* [51423](https://bugzilla.xamarin.com/show_bug.cgi?id=51423) - [foundation] Honor the cancellation token win the async requests in `NSUrlSessionHandler` **(10.8.0.33+)**
* [53410](https://bugzilla.xamarin.com/show_bug.cgi?id=53410) - [msbuild] Implemented `GetFiles` and `GetFullPath` tasks to fix the vs build **(10.8.0.33+)**
* [53794](https://bugzilla.xamarin.com/show_bug.cgi?id=53794) - [foundation] Ensure that if a request is canceled we cancel the `NSUrlSessionTask` **(10.8.0.33+)**


### API diff

The following documents contains a complete list of the API changes since our latest stable release: XI 10.6.0

* [iOS](/releases/ios/api_changes/ios_10.6.0_to_10.8.0);
* [tvOS](/releases/ios/api_changes/tvos_10.6.0_to_10.8.0);
* [watchOS](/releases/ios/api_changes/watchos_10.6.0_to_10.8.0)

