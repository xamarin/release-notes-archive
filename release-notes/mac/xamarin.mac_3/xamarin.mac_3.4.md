---
id: BF9EDE0A-6EFC-4A23-8C34-6600241B0F44
title: "Xamarin.Mac 3.4"
---

version:3.4.0
releasedate:2017-04-04

<div class="note">
	<b>Xamarin.Mac Facade Loading Bug</b>
	Some projects using nugets that reference facades such as System.ValueTuple or System.Text.Encoding.CodePages may crash on launch with Xamarin.Mac 3.4. See the "Nuget Facade Loading Bug" section below for details and a work around.
</div>

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled macOS SDK;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-2` branch, and include some additional IDE integration tools.

Breaking Changes
----------------

The new version of Mono (shipping in sync) changed it's C# compiler to use Roslyn, providing all C# 7 features on macOS. Projects that manually removed the `System.dll` assembly reference will have to add it back if any type from it was used inside the project.

### Mono 5.0

This release is based on the new Mono 5.0 release. This offers many exciting new features like:

* Roslyn based C# compiler offering all the lovely featues of C# 7;
* Support for portable pdb (.ppdb), a single debugging format available across all platforms;
* Increased support for netstandard 2.0 for the base class libraries (BCL) shipped with our platform's SDK;
* Official support for `msbuild` over, now deprecated, `xbuild`;

### Improved msbuild and netstandard13/20 Support

In Xamarin.Mac 3.4 the msbuild targets have been rewritten to better support use of msbuild and nuget libraries that ship on netstandard13. Please report build regressions to [bugzilla](https://bugzilla.xamarin.com/index.cgi).

### csc and ppdb support

Xamarin.Mac 3.4 adds supports for compiling with csc instead of mcs and debugging with [ppdb](https://github.com/dotnet/roslyn/blob/portable-pdb/docs/specs/PortablePdb-Metadata.md) format symbols.

### Assembly Registration Event

During startup the Xamarin.Mac runtime must register all NSObject based classes with the Cocoa runtime. You can read about some detail (here)[https://developer.xamarin.com/guides/ios/advanced_topics/registrar/#Registration_of_managed_classes_and_methods].

In a vast majority of cases the default behavior of using the Dynamic Registrar in Debug configuration and Static Registrar in Release is acceptable. However, some very large applications may want to customize this behavior, so a registration event has been added ObjCRuntime.Runtime.AssemblyRegistration.

Applications that register with this event can return false to skip registration of types in a given assemblies (and it's dependencies). Be aware any NSObject derived types declared in any skipped assembly may be subtly broken, so caution is advised with this feature.

### Nuget Facade Loading Bug

Due to this [bug](https://bugzilla.xamarin.com/show_bug.cgi?id=55988), the mono runtime will refuse to load certain facade assemblies which will crash applications that depend upon them. These facades are commonly packaged as nuget packages, and some nugets such as Roslyn depend on them. The list of assemblies in question include:

- System.Runtime.InteropServices.RuntimeInformation.dll
- System.Globalization.Extensions.dll
- System.IO.Compression.dll
- System.Net.Http.dll
- System.Text.Encoding.CodePages.dll
- System.Reflection.DispatchProxy.dll
- System.ValueTuple.dll

You can determine if you are hitting this bug by running your application with MONO\_LOG\_MASK=asm MONO\_LOG\_DLL=debug set and look for "Denying load of problematic image".

As a work around, create a [post build script] (https://github.com/xamarin/mac-samples/tree/master/UseMSBuildToCopyFilesToBundleExample) that copies the required assemblies from either:

- /Library/Frameworks/Xamarin.Mac.framework/Versions/Current/lib/mono/Xamarin.Mac/Facades (If your project is Modern (Mobile))
- /Library/Frameworks/Xamarin.Mac.framework/Versions/Current/lib/mono/4.5/Facades (If your project is Full (XM 4.5))

### Binding Generator

The generator now uses `IKVM.Reflection` instead of `System.Reflection` as its introspection engine. This allowed us to remove several tricks required to have the generator work on several platforms. This is largely an invisible change for most developers, unless you notice the smaller tool size, since the generated code remains identical. The main benefit is that it is now possible to debug the generator using Xamarin Studio, which makes it much easier to work and contribute on.

Other generator improvements are:

* [53273](https://bugzilla.xamarin.com/show_bug.cgi?id=53273) The command-line tools (`btouch`, `btv`, `bwatch` and `bmac`) now support `nowarn` and `warnaserror` arguments;
* `[Async]` methods inside `[Protocol]` are turned into extension methods, so the interface does not include them (it must match the protocol), but the nice async version remains available to developers;
* `[Async]` members from internal `BaseWrapper`-derived types are no longer generated, since they are not reachable;
* [53076](https://bugzilla.xamarin.com/show_bug.cgi?id=53076) Remove `[Async]` members from `[Model]` types, they are not part of the protocol - but the extensions methods (mentioned earlier) are available to file the gap;
* [42742](https://bugzilla.xamarin.com/show_bug.cgi?id=42742) The `[Advice]` attributes are now copied into the generated code - making available for the IDE to suggest better alternatives;
* [52570](https://bugzilla.xamarin.com/show_bug.cgi?id=52570) A warning is reported when a `[Static]` method is used inside a `[Category]` - since they are extension methods (already `static`) the resulting API is hard to use;
* [42855](https://bugzilla.xamarin.com/show_bug.cgi?id=42855) A warning is reported when a `[Protocol]`-decorated type has a `[BaseType]` but no `[Model]` - the interface for the protocol cannot inherit from a concrete type (like the `[Model]` would);
* [42699](https://bugzilla.xamarin.com/show_bug.cgi?id=42699) Allow basic support of nullable types inside our trampolines - needed when exposing nullable for native C API;


### Miscellaneous Enhancements

**API**

* [33997](https://bugzilla.xamarin.com/show_bug.cgi?id=33997) - [coregraphics] Add missing `[Flags]` on `CGGradientDrawingOptions`
* [43628](https://bugzilla.xamarin.com/show_bug.cgi?id=43628) - [coregraphics] Add bindings for `CGRect.Null` and `CGRect.Infinite`
* [52571](https://bugzilla.xamarin.com/show_bug.cgi?id=52571) - [contacts] Provide better API for CNContainer_PredicatesExtension and CNGroup_PredicatesExtension categories 
* [52730](https://bugzilla.xamarin.com/show_bug.cgi?id=52730) - [AVFoundation] Enable `AVAudioSessionInterruptionEventArgs.WasSuspended`
* [53083](https://bugzilla.xamarin.com/show_bug.cgi?id=53083) - [mapkit] Add missing (from unified API) `MKLocalSearchRequest initWithCompletion:`
* [pr1527](https://github.com/xamarin/xamarin-macios/pull/1527) - Several new `*Async` methods were added across all framework and platforms (see API diff for complete list);
* [pr2042](https://github.com/xamarin/xamarin-macios/pull/2042) - Fix casting in NSApplication.NextEvent on 64-bit systems

### Bug Fixes

* [55988](https://bugzilla.xamarin.com/show_bug.cgi?id=55988) - Prevent "problematic" facade crashes on startup by default to XM's version
* [56260](https://bugzilla.xamarin.com/show_bug.cgi?id=56260) - This stream does not support writing at System.IO.Compression.DeflateStream.BeginWrite
* [53058](https://bugzilla.xamarin.com/show_bug.cgi?id=53058) - [generator] Fix native enum in native delegates return types

* [54409](https://bugzilla.xamarin.com/show_bug.cgi?id=54409) - [cecil] Update Cecil to fix a `NotImplementedException` in `ReadPrimitiveValue`
* [54148](https://bugzilla.xamarin.com/show_bug.cgi?id=54148) - [coretext] `CTParagraphStyle` does not pick up settings from `CTParagraphStyleSettings`
* [pr2002](https://github.com/xamarin/xamarin-macios/pull/2002) - Update code that only considered .mdb (not .pdb)

* [54914](https://bugzilla.xamarin.com/show_bug.cgi?id=54914) - [msbuild] Avoid Dictionary clashes in IBToolTask's mapping dictionary

* [55480](https://bugzilla.xamarin.com/show_bug.cgi?id=55480) - [msbuild] Fix CompileSceneKitAssetsTaskBase with msbuild (versus xbuild)

### API diff

The following documents contains a complete list of the API changes since our latest stable release: XM 3.2 (15.1)

* [macOS](/releases/mac/api_changes/mac_3.2_to_3.4);

