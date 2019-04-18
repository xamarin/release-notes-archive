---
id: EC5135DD-A9B7-473E-9780-B00CFA0B5DBA
title: "Xamarin.Mac 3.2"
---

version:3.2.0
releasedate:2017-04-05

<div class="note">
	<b>Mono TLS Removal:</b>
	This version of Xamarin.Mac does <b>not</b> ship with the old Mono (managed) SSL/TLS provider, which
	only supported the SSLv3 and TLSv1 standards. TLS support (up to version 1.2) is provided by the 
	newer AppleTLS provider (already the default since XI 2.4 / C7).
</div>

<div class="note">
	<b>Release mode defaults change</b>
	This version of Xamarin.Mac changes the default setting for disable-lldb-attach and registrar if not 
	explicilty set in your project to new settings. See below for details.
	</div>

<div class="note">
	<b>XM 4.5, HttpClient, and System.Configuration crash</b>
	There is a rare known issue where applications using HttpClient can crash with a NullReferenceException inside FindLocationConfiguration in System.Configuration. See below for details. 
	</div>


Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled macOS SDKs;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-1` branch, and is based on Mono 4.8.0.

### Ahead of Time Compilation (Experimental)

Xamarin.Mac applications have historically been Just in Time (JIT) compiled, which means the C# code is compiled down to machine code during launch. This diffs from Ahead of Time (AOT) compliation that Xamarin.iOS applications have done to meet device requirements.

In many cases the cost in start up time is unnoticable. However, very large applications can see a second or two pause during startup as they JIT hundreds of assemblies. In addition, interations with native debugging and profiling tools can be difficult with JIT code, as stack frames show up with no symbol information from their perspective. 

This support is somewhat experimental, and currently lacks options in Xamarin Studio IDE. It can be enabled by passing --aot= in the "Additional MMP Arguments" field in the project Mac Build settings. The options include:

```
    --aot[=VALUE]          Specify assemblies that should be compiled via
                               experimental AOT.
                               - none - No AOT (default)
                               - all - Every assembly in MonoBundle not ignored
                               - core - Just Xamarin.Mac.dll, System.dll, and
                               mscorlib.dll
                                sdk - Xamarin.Mac.dll and all BCL assemblies
                               Individual files can be included for AOT via +
                               FileName.dll and excluded via -FileName.dll
```

### Partial Static Registrar

The Partial Static Registrar is a performance optimization which drastically improves Xamarin.Mac launch times when using the dynamic registrar (the default in Debug configuration).

This can often improve launch times by up to a 5x factor, giving much of the performance boost of the static registrar without increasing build times.

### Release Mode MMP Default Changes

The default settings in Release builds for two features are changing in 3.2 to better fit user expectations:

- --disable-lldb-attach now defaults to true in Release builds if not set. LLDB attach is generally not useful in Release builds, and it often prompts users to install Xcode, which is not ideal behavior for application users.
- --registrar now defaults to static in Release builds if not set. The Release build configuration trades longer build time for improved application performance, and use of the static registrar improves launch time greatly. 

Building with the static registrar can imposes addition requirements upon your application. If your applications uses QTKit, for example, you can not use the static registrar since Apple has removed the headers for that framework from the SDK. This can be changed to the previous setting by adding --registrar=dynamic to your Additional MMP Argument setting.

### Improved Printing Support

A number of C APIs in ApplicationServices.framework / PrintCore.framework have been bound in a new PrintCore namespace. In addition, helper methods have been added to NSPrintInfo to obtain the relevent PMPrintSession object.

### MSBuild error codes

The **7xxx** range of errors is now reserved for MSBuild errors and we started documenting the first ones. Their description include the task that generated the error as well as some troubleshooting steps when applicable. 

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

### mmp warnings

We've added support for treating `mmp` warnings as errors, as well as ignoring `mmp` warnings.

This support is modeled after the same feature in the C# compiler, and can be
configured by passing the following options as an additional mmp argument
in the project's iOS Build options:

* `--nowarn` will disable all warnings.
* `--nowarn:16,43` will disable the warnings MM0016 and MM0043.
* `--warnaserror` will report all warnings as errors.
* `--warnaserror:16,43` will make the warnings MM0016 and MM0043 show up as errors.

### XM 4.5, HttpClient, and System.Configuration crash

In rare cases, users of the XM 4.5 (Full) target framework can crash on first use of HttpClient with a NullReferenceException (inside FindLocationConfiguration in System.Configuration).

A fix is currently in work. As a workaround, the following can be run after NSApplication.Init to prevent the race condition bug from occuring.

```
  try {
  	Assembly.Load ("System.Configuration")
  		?.GetType ("System.Configuration.ConfigurationManager")
  		?.GetMethod ("GetSection", BindingFlags.Static | BindingFlags.Public)
  		?.Invoke (null, new [] { "configuration" });
  } catch {
  }
```

### Miscellaneous Enhancements

**Performance**

* [51298](https://bugzilla.xamarin.com/show_bug.cgi?id=51298) - [msbuild] Parallelized codesigning of *.dylibs and frameworks

**Tools**

* [28106](https://bugzilla.xamarin.com/show_bug.cgi?id=28106) - [msbuild] Added support for `<Link>`'d ImageAsset project files
* [43165](https://bugzilla.xamarin.com/show_bug.cgi?id=43165) - [generator] Allow the use of `[Async]` attribute on [Abstract] decorated methods
* [43995](https://bugzilla.xamarin.com/show_bug.cgi?id=43995) - [generator] Support `[Sealed]` attribute on types (not just methods)
* [46285](https://bugzilla.xamarin.com/show_bug.cgi?id=46285) - [generator] Allow identical (numeric) values in smart enums
* [46292](https://bugzilla.xamarin.com/show_bug.cgi?id=46292) - [generator] Copy `[Obsolete]` attributes on smart enums
* [PR1249](https://github.com/xamarin/xamarin-macios/pull/1249) - [generator] Optimize smart enums support to reduce the required metadata
* [PR1446](https://github.com/xamarin/xamarin-macios/pull/1446) - [generator] Remove internal `*Wrapper.ctor(IntPtr)` constructors
* [PR1557](https://github.com/xamarin/xamarin-macios/pull/1557) - [msbuild] Added `ProcessEnums` property for ObjC binding projects
* [PR1707](https://github.com/xamarin/xamarin-macios/pull/1707) - [generator] Have `[WrapAttribute]` optionally generate virtual members when `IsVirtual=true`

**API**

* [39789](https://bugzilla.xamarin.com/show_bug.cgi?id=39789) - [foundation] Add a number of missing `[Flags]` in various enums
* [43250](https://bugzilla.xamarin.com/show_bug.cgi?id=43250) - NSOpenGLPixelFormat doesn't support NSOpenGLProfile argument

**Better error/warnings reporting**

* [PR1174](https://github.com/xamarin/xamarin-macios/pull/1174) - [generator] Improve warning about missing `[CCallback]` or `[BlockCallback]` attributes
* [PR1188](https://github.com/xamarin/xamarin-macios/pull/1188) - [msbuild] Log warnings and errors for the ibtool --link stage as well
* [51212](https://bugzilla.xamarin.com/show_bug.cgi?id=51212) - [generator] Provide a better error than BI0000 for `TypeloadException` in NeedStret
* [45696](https://bugzilla.xamarin.com/show_bug.cgi?id=45696) - XM MSBuild is not copying in resx localization output into bundle 

**External Contributions**

* [PR1545](https://github.com/xamarin/xamarin-macios/pull/1545) - [msbuild] Recognize networkextension extensions (and avoid build warning)

### Bug Fixes

* [25499](https://bugzilla.xamarin.com/show_bug.cgi?id=25499) - [msbuild] Fixed EmbedMobileProvision to lookup provisions by name/uuid correctly
* [46626](https://bugzilla.xamarin.com/show_bug.cgi?id=46626) - [corefoundation] Store strings in the exception data when converting `CFError` to `CFException`
* [50407](https://bugzilla.xamarin.com/show_bug.cgi?id=50407) - [foundation] Fix `NSFormatter.IsPartialStringValid`
* [51514](https://bugzilla.xamarin.com/show_bug.cgi?id=51514) - [generator] Missing `[Wrap]` from protocol/interface when parent has a `[Wrap]` itself 
* [52279](https://bugzilla.xamarin.com/show_bug.cgi?id=52279) - [corefoundation] Fix `CallbackDelegate` signature to be 32bits safe (enum)

### Releases

- 3.2.0.175

 Add new APIs from Xcode 8.3.

 Release Canidate for Xamarin.Mac 3.2.

- 3.2.0.26 - 3.2.0.33

Compatibility releases aligning with the rest of the Xamarin Platform. No XM specific fixes have been included as part of these.

- 3.2.0.20

Initial 15.1 Beta

* Improve netstandard13 compatibility with XM 4.5 (Full) profile

- 3.2.0.1 - 3.2.0.10

Initial 15.1 Alpha


### API diff

The following documents contains a complete list of the API changes since our latest stable release: XM 3.0 (C9)

* [macOS](/releases/mac/api_changes/mac_3.0_to_3.2);

