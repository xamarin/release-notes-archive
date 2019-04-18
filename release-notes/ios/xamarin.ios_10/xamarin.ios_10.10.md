---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 10.10"
---

version:10.10.0
releasedate:2017-05-10

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled iOS, tvOS and watchOS SDKs;
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


### Code sharing between Applications and Extensions

We've added support for compiling assemblies into embedded frameworks, which
makes it possible to share the AOT-compiled code for assemblies between
extensions and the containing app.

Code sharing is automatically enabled whenever it makes sense (for apps with
extensions), but if for some reason Xamarin.iOS detects that code sharing
can't be enabled (there are many build options that makes code sharing
impossible if they differ between projects), a warning explaining why will be
shown.

If Xamarin.iOS determines that code sharing can occur, then it builds one
framework for all the assemblies in the SDK, and this framework is shared
between extensions and the main app. This significantly reduces total code
size of the app (and the build time, since every assembly is only AOT-compiled
once per architecture).

Additionally, when code sharing is enabled, Xamarin.iOS will also AOT-compile
every assembly (not only SDK assemblies) only once (per architecture), which
greatly speeds up compilation time.

#### App size and build time improvements with code sharing

For an extreme test project with 7 extensions ([embedded-frameworks][1]):

<!--
|            |  cycle 9   | with code sharing   |  difference                   |
|------------|-----------:|--------------------:|------------------------------:|
|build time  |    3m 33s  |    1m 47s           |      -1m 46s = ~50% faster    |
|app size    |    131 MB  |     26 MB           |     -105 MB  = ~80% smaller   |
-->

<table>
<thead><tr><th></th><th align="right">cycle 9</th><th align="right">with code sharing</th><th align="right">difference</th></tr></thead>
<tbody>
<tr><td>build time</td><td align="right">3m 33s</td><td align="right">1m 47s</td><td align="right">-1m 46s = ~50% faster</td></tr>
<tr><td>app size</td><td align="right">131 MB</td><td align="right">26 MB</td><td align="right">-105 MB  = ~80% smaller</td></tr>
</tbody>
</table>

For a more normal test project ([MyTabbedApplication][2]) - this is a simple
application with 1 extension:

<!--
|            |  cycle 9   | with code sharing   |  difference                   |
|------------|-----------:|--------------------:|------------------------------:|
|build time  |    0m 52s  |    0m 46s           |          -8s = ~12% faster    |
|app size    |     37 MB  |     25 MB           |       -12 MB = ~32% smaller   |
-->

<table>
<thead><tr><th></th><th align="right">cycle 9</th><th align="right">with code sharing</th><th align="right">difference</th></tr></thead>
<tbody>
<tr><td>build time</td><td align="right">0m 52s</td><td align="right">0m 46s</td><td align="right">-8s = ~12% faster</td></tr>
<tr><td>app size</td><td align="right">37 MB</td><td align="right">25 MB</td><td align="right">-12 MB = ~32% smaller</td></tr>
</tbody>
</table>

A tvOS app with one extension also show similar gains ([MyTVApp][3]):

<!--
|            |  cycle 9   | with code sharing   |  difference                   |
|------------|-----------:|--------------------:|------------------------------:|
|build time  |    0m 28s  |     0m 20s          |         -8s  = ~29% faster    |
|app size    |     42 MB  |      33 MB          |       -9 MB  = ~21% smaller   |
-->

<table>
<thead><tr><th></th><th align="right">cycle 9</th><th align="right">with code sharing</th><th align="right">difference</th></tr></thead>
<tbody>
<tr><td>build time</td><td align="right">0m 28s</td><td align="right">0m 20s</td><td align="right">-8s  = ~29% faster</td></tr>
<tr><td>app size</td><td align="right">42 MB</td><td align="right">33 MB</td><td align="right">-9 MB  = ~21% smaller</td></tr>
</tbody>
</table>

[1]: https://github.com/rolfbjarne/embedded-frameworks
[2]: https://github.com/xamarin/xamarin-macios/tree/cycle9/msbuild/tests/MyTabbedApplication
[3]: https://github.com/xamarin/xamarin-macios/tree/cycle9/msbuild/tests/MyTVApp
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


### Xamarin Analysis

We added a new rule to our project analysis tool which ensures that the supported architecture for `release | device` is 64 bit compatible (includes ARM64). This is important as Apple does not accept 32 bits only iOS apps in the AppStore.

*As a reminder you can run the Xamarin Analysis rules from Xamarin Studio's menu bar by selecting Project > Run Code Analysis.*

### Miscellaneous Enhancements

**API**

* [33504](https://bugzilla.xamarin.com/show_bug.cgi?id=33504) - [uikit] Add `==` and `!=` operators on `UIEdgeInsets`
* [33997](https://bugzilla.xamarin.com/show_bug.cgi?id=33997) - [coregraphics] Add missing `[Flags]` on `CGGradientDrawingOptions`
* [43628](https://bugzilla.xamarin.com/show_bug.cgi?id=43628) - [coregraphics] Add bindings for `CGRect.Null` and `CGRect.Infinite`
* [52571](https://bugzilla.xamarin.com/show_bug.cgi?id=52571) - [contacts] Provide better API for CNContainer_PredicatesExtension and CNGroup_PredicatesExtension categories
* [52730](https://bugzilla.xamarin.com/show_bug.cgi?id=52730) - [AVFoundation] Enable `AVAudioSessionInterruptionEventArgs.WasSuspended`
* [53083](https://bugzilla.xamarin.com/show_bug.cgi?id=53083) - [mapkit] Add missing (from unified API) `MKLocalSearchRequest initWithCompletion:`
* [pr1527](https://github.com/xamarin/xamarin-macios/pull/1527) - Several new `*Async` methods were added across all framework and platforms (see API diff for complete list);

**Tools**

* [pr1947](https://github.com/xamarin/xamarin-macios/pull/1947) - [linker] Capture and show more information when a MT2001 error occurs


### Bug Fixes

* [56260](https://bugzilla.xamarin.com/show_bug.cgi?id=56260) - This stream does not support writing at System.IO.Compression.DeflateStream.BeginWrite
* [52308](https://bugzilla.xamarin.com/show_bug.cgi?id=52308) - [runtime] `Console.WriteLine` output not showing in the Device Log of some iOS versions
* [53058](https://bugzilla.xamarin.com/show_bug.cgi?id=53058) - [generator] Fix native enum in native delegates return types
* [53075](https://bugzilla.xamarin.com/show_bug.cgi?id=53075) - [uikit] Mark `NSFileProviderExtension` as `[ThreadSafe]`

* [52545](https://bugzilla.xamarin.com/show_bug.cgi?id=52545) - [mtouch] Remove workaround for mono bug #43462 and fix slow builds on large projects **(10.10.0.6+)**
* [54409](https://bugzilla.xamarin.com/show_bug.cgi?id=54409) - [cecil] Update Cecil to fix a `NotImplementedException` in `ReadPrimitiveValue` **(10.10.0.6+)**
* [54499](https://bugzilla.xamarin.com/show_bug.cgi?id=54499) - [mtouch] Copy aot data to the app even for assemblies that aren't copied **(10.10.0.6+)**
* [54148](https://bugzilla.xamarin.com/show_bug.cgi?id=54148) - [coretext] `CTParagraphStyle` does not pick up settings from `CTParagraphStyleSettings` **(10.10.0.6+)**
* [53813](https://bugzilla.xamarin.com/show_bug.cgi?id=53813) - [mtouch] Fix how we build shared frameworks with bitcode enabled (e.g. tvOS and watchOS) **(10.10.0.11+)**

* [54578](https://bugzilla.xamarin.com/show_bug.cgi?id=54578) - [cecil] Assemblies are duplicated in fat apps when built with .pdb **(10.10.0.21+)**
* [54914](https://bugzilla.xamarin.com/show_bug.cgi?id=54914) - [msbuild] Avoid Dictionary clashes in IBToolTask's mapping dictionary **(10.10.0.21+)**
* [55316](https://bugzilla.xamarin.com/show_bug.cgi?id=55316) - [msbuild] Fixed msbuild logic to properly codesign watchos2 intents extensions **(10.10.0.21+)**

* [55480](https://bugzilla.xamarin.com/show_bug.cgi?id=55480) - [msbuild] Fix CompileSceneKitAssetsTaskBase with msbuild (versus xbuild) **(10.10.0.30+)**
* [55555](https://bugzilla.xamarin.com/show_bug.cgi?id=55555) - [mtouch] Don't remove information when collecting all architectures **(10.10.0.30+)**
* [55698](https://bugzilla.xamarin.com/show_bug.cgi?id=55698) - [mtouch] Look for dynamic libraries in the container application **(10.10.0.30+)**

* [55676](https://bugzilla.xamarin.com/show_bug.cgi?id=55676) - [msbuild] Remove stale CodeSignatures when cloning appex's into parent app bundle **(10.10.0.33+)**


### API diff

The following documents contains a complete list of the API changes since our previous 10.8 release:

* [iOS](/releases/ios/api_changes/ios_10.8.0_to_10.10.0);
* [tvOS](/releases/ios/api_changes/tvos_10.8.0_to_10.10.0);
* [watchOS](/releases/ios/api_changes/watchos_10.8.0_to_10.10.0)

