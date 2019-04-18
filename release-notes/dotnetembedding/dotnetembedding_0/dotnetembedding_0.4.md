---
id: E4FE272C-F319-489D-8543-F39FFDBEFAE9
title: ".NET Embedding 0.4"
---

Updated: 04/17/2018

[Getting Started](https://docs.microsoft.com/xamarin/tools/dotnet-embedding/get-started/) | [What's New](#Whats_new_in_this_release) | [Known Issues](#Known_issues) | [Blogs](https://blog.xamarin.com/) | [Feedback](#Feedback) | [Open Source](#Open_source)

## What's new in this release

* [Objective-C tooling via NuGet](#Objective-C_tooling_via_NuGet)
* [Xamarin.Mac bundling format change](#Xamarin.Mac_bundling_format_change)

### Objective-C tooling via NuGet

In 0.4 we've moved to unify the Objective-C tools with the Java/C tooling in a single NuGet. 

This replaces the previous installer that installed to:

`/Library/Frameworks/Xamarin.Embeddinator-4000.framework/`

[Detailed instructions](https://docs.microsoft.com/xamarin/tools/dotnet-embedding/get-started/install/install) on how to move to the NuGet packaged tools have been posted. 

### Xamarin.Mac bundling format change

In 0.4 libraries targetting Xamarin.Mac (not just "raw" macOS) join Xamarin.iOS in both defaulting to and only supporting "framework" style packaging. The other formats (static and dynamic library) have systemic usability issues with dependencies.

The new [getting started](https://docs.microsoft.com/xamarin/tools/dotnet-embedding/get-started/objective-c/macos) for macOS has been updated to use frameworks.  

## Release history

* April 18, 2017 - .NET Embedding 0.4

### Objective-C support

- [405](https://github.com/mono/Embeddinator-4000/issues/405) - Handle "Interfaces within interfaces" in generated code
- [484](https://github.com/mono/Embeddinator-4000/issues/484) - Native Exception Handling Support
- [561](https://github.com/mono/Embeddinator-4000/issues/561) & [641](https://github.com/mono/Embeddinator-4000/pull/641) - Arrays of enums and structures now generate more correct bindings
- [604](https://github.com/mono/Embeddinator-4000/pull/604) - Resolve compile issues when targetting Xamairn.Mac "System" [Target Framework](https://developer.xamarin.com/guides/mac/advanced_topics/target-framework/)
- [610](https://github.com/mono/Embeddinator-4000/pull/610) - Restrict use of "auto" and "static" in selector names
- [610](https://github.com/mono/Embeddinator-4000/pull/610) - Skip with warning selectors that would duplicate in generated code
- [613](https://github.com/mono/Embeddinator-4000/pull/613) - Fix compiler errors related to local variable names used for parameter conversion.
- [619](https://github.com/mono/Embeddinator-4000/pull/619) - Improve help to show macos-[modern|full|system] platforms
- [627](https://github.com/mono/Embeddinator-4000/pull/627) - Default to and enforce framework style packaging
- [632](https://github.com/mono/Embeddinator-4000/pull/632) - Improve F# support

### Java support

- [542](https://github.com/mono/Embeddinator-4000/pull/542) - Improved overload generation for Java methods
- [573](https://github.com/mono/Embeddinator-4000/issues/573) - Fix code generation of long literals in enums

### Android support

- [527](https://github.com/mono/Embeddinator-4000/pull/527) - Support for latest Android Studio 3.0
- [532](https://github.com/mono/Embeddinator-4000/pull/532) - Added missing Xamarin.Android `MonoPackageManager.setContext` method
- [616](https://github.com/mono/Embeddinator-4000/pull/616) - Manually load monosgen-2.0 library to support API < 18

### Windows support

- [506](https://github.com/mono/Embeddinator-4000/pull/506) - Improved support for finding Mono SDK on Windows

### Linux support

- [500](https://github.com/mono/Embeddinator-4000/pull/500) - Improved support for Linux platforms

### Other features and fixes

- [503](https://github.com/mono/Embeddinator-4000/pull/503) - We now provide an API for setting Mono runtime assembly paths

## Known issues

- There are a number of [documented limitations](https://docs.microsoft.com/xamarin/tools/dotnet-embedding/limitations) to consider.
- In some rare cases the generator produces duplicate symbols, which will fail to compile. Please file an [issue](https://github.com/mono/Embeddinator-4000/issues) on github if this occurs.
- There are a number C# features that are not supported currently. Consider exposing a [simplified subset](https://docs.microsoft.com/xamarin/tools/dotnet-embedding/objective-c/best-practices#exposing-a-subset-of-the-managed-code) of managed code.

## Feedback

We'd love to hear from you! If there are any problems with this release, check [GitHub](https://github.com/mono/Embeddinator-4000/issues) for existing issues. 

Report new issues and suggestions [on GitHub](https://github.com/mono/Embeddinator-4000/issues). 

## Open source

.NET Embedding is based on the following open-source repositories:

* [Embeddinator-4000](https://github.com/mono/Embeddinator-4000) branch `0.4`

### A big Thank You! to the following folks that helped to make the Embeddinator-4000 even better:

* [@equinox2k](https://github.com/equinox2k)
* [@tombly](https://github.com/tombly)
* [@lemonmojo](https://github.com/lemonmojo)
