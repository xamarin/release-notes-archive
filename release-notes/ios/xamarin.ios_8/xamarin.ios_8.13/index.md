---
id: 77259859-F920-4E15-9421-E0ED79F54AD3
title: "Xamarin.iOS 8.13"
brief: "Xamarin 8.13.x Releases"
---

# Xamarin.iOS 8.13



The Xamarin.iOS 8.13.0 series upgrades the Mono stack from
	the Mono 4.0.xx
	series to the [Mono 4.2.xx](http://www.mono-project.com/docs/about-mono/releases/4.2.0/)

 series.   One of the major themes in
	Mono 4.2.xx series is the continued adoption of Microsoft's
	open sourced .NET code to improve the conformance, speed and
	memory usage of our stack.# New Features

## Visual Studio: New Mac Build Agent



We have rewritten the Mac Build agent that Visual Studio
	uses to connect to.

The user experience is vastly superior.   Not only because
	it is now easier, more convenient and more reliable to link
	your Windows and Mac computers, but because we have addressed
	many of the fundamental design limitations, shortcomings and
	bugs from our previous implementation.   This means more
	reliable builds, debugging and runs.

We have replaced our pairing and authentication system with
	one powered by SSH, which now encrypts all data transfers and
	uses the MacOS provided SSH server as the mechanism to connect
	your Windows and Mac computers.## Support for Embedded Frameworks



It is now possible to use iOS Frameworks with your iOS
	projects.  This is Apple's way of packaging shared libraries,
	they are useful for sharing code between multiple components
	of your app (your main application and your extensions) or to
	easily add third party frameworks without doing native
	linking [[1]](note-1)

.

Xamarin.iOS will automatically switch to using
	Mono.framework instead of statically linking the Mono
	framework into your executable when you use extensions.

Embedded frameworks only work on iOS 8.0 and higher.

This behavior can be controlled with
	the `--mono=`

 command line option to mtouch, you can
	select `--mono=static`

 to force static linking
	or `--mono=framework`

 to force the use of a shared --
	--Mono.framework in your project.

Some examples showing how this can be used for linking with
	native frameworks and invoking manually, using it for C#
	bindings to Objective-C APIs and how this is used with many
	extensions can be found
	in [embedded-frameworks](https://github.com/xamarin/embedded-frameworks)


	github module. <a name="note-1"></a>




[1] While frameworks are convenient units of deployment,
	they do not participate in the linking process, so if you are
	merely using a limited set of features from a framework, you
	wont get the beneifts that come from statically linking, which
	would only include the pieces that you actually use.# Improvements

## Build Time Improvements: Partial Static Registrar



This is an optimization we made to the runtime to improve
	the development speed for iOS simulator builds.   It uses
	the static registration system for the system, and uses
	dynamic registration for user code, which does not require any
	new native code to be compiled on each iteration.## Code Generation Optimizations



When compiling with LLVM, Xamarin.iOS will no longer
	generate intermediate files, and instead will generate object
	code directly.   This allowed us to generate more efficient
	code (in some large application scenarios, LLVM produced
	binaries are 3% smaller) and slightly improved build times. <a name="0"></a>


##  [Xamarin iOS 8.13.0](#0)



The following document contains a complete list of the [API changes from 8.10 to 8.13.0](/releases/ios/api_changes/from_8.10.3_to_8.13.0)

.
