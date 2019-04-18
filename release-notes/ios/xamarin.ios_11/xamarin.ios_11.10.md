---
id: 710e3483-db85-4226-bb05-e1b4df75c095
title: "Xamarin.iOS 11.10"
---

# Xamarin.iOS 11.10
Last Update: 5/15/2018


[Getting Started](https://developer.xamarin.com/guides/ios/getting_started/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Feedback](#feedback) [Open Source](#open-source)

> ⚠️  **Update to macOS High Sierra**
> The most recent version of Xcode (9.3) requires macOS High Sierra (10.13).
> developers should update to macOS High Sierra as soon as possible
> in order to support the Xcode 9.3 SDKs and API.

#### Requirements

* The latest features and API requires Xcode 9.3 and the bundled iOS, tvOS and watchOS SDKs
* Apple Xcode 9.3 requires a Mac running macOS 10.13.2 (High-Sierra) or newer

## What's New in this Release

* [Registrar Optimizations](#registrar-optimizations)
* [Xamarin.Analysis Use LLVM rule](#xamarinanalysis-use-llvm-rule)
* [WeakAttribute](#WeakAttribute)
* [API Enhancements](#api-enhancements)
* [Tooling Enhancements](#tooling-enhancements)

### Registrar Optimizations

This is a set of optimizations that makes the dynamic registrar removable by the linker (under most circumstances). This results in:

* **Smaller applications** - The linked `Xamarin.iOS.dll` is between 30-50% smaller than before since the information (e.g. custom attributes) needed only at build time can now be removed. This also allows the linker to remove more code than before (since less code is being referenced);
* **Faster application startup** - More registration work is being done at build time instead of at runtime. E.g. this removes the need to use (slow) reflection on custom attributes to register types and methods;
* **Reduced memory usage** - The avoided work also reduces the memory required for applications. Initial (startup) memory requirement is down 30% for a minimal application and 20% for extensions. This makes it easier to create some type of extensions where iOS imposes memory limits (e.g. 16MB for Today extensions).

### Xamarin.Analysis: Use LLVM rule

We added a new rule to our project analysis tool which recommends enabling the LLVM compiler for Release|iPhone configuration. LLVM generates code that is faster to execute at the expense of build time.

As a reminder to run the rules, in Visual Studio for Mac's menu, select **Project > Run Code Analysis**.

*Note: all existing rules are documented [here](https://developer.xamarin.com/guides/ios/troubleshooting/xamarin-ios-analysis).*

### WeakAttribute

`WeakAttribute` can be used to decorate reference type fields in a class. Like `WeakReference <T>`, `WeakAttribute` will help you break [strong circular references](https://docs.microsoft.com/en-us/xamarin/ios/deploy-test/performance#avoid-strong-circular-references), but with with even less code.

Consider the following code, which uses `WeakReference <T>`:

```csharp
public class MyFooDelegate : FooDelegate {

	WeakReference<MyViewController> container;

	public MyFooDelegate (MyViewController ctrl) => container = new WeakReference<MyViewController> (ctrl);

	public void CallDoSomething ()
	{
		MyViewController controller;
		if (container.TryGetTarget (out controller)) {
			controller.DoSomething ();
		}
	}
}
```

Equivalent code using `WeakAttribute` is far more concise:

```csharp
public class MyFooDelegate : FooDelegate {
	[Weak] MyViewController controller;

	public MyFooDelegate (MyViewController ctrl) => controller = ctrl;
	public void CallDoSomething () => controller.DoSomething ();
}
```

Notice that in this case it is not necessary to implement a null check before calling `controller.DoSomething ();`. This is because of the the context of the call; since `MyFooDelegate` participates in Apple's [delegation pattern](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Delegation.html) as a delegate for `controller`, it should only exist as long as `controller` does.

The following code snippet demonstrates more of a real-world example of using `WeakAttribute` in context of the [delegation](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Delegation.html) pattern:

```csharp
public class MyViewController : UIViewController {
	protected MyViewController (IntPtr handle) : base (handle) { }

	WKWebView webView;
	public override void ViewDidLoad ()
	{
		base.ViewDidLoad ();
		webView = new WKWebView (View.Bounds, new WKWebViewConfiguration ());
		webView.UIDelegate = new UIDelegate (this);
		View.AddSubview (webView);
	}
}

public class UIDelegate : WKUIDelegate {

	[Weak] MyViewController controller;

	public UIDelegate (MyViewController ctrl) => controller = ctrl;
	public override void RunJavaScriptAlertPanel (WKWebView webView, string message, WKFrameInfo frame, Action completionHandler)
	{
		var msg = $"Hello from: {controller.Title}";
		var alertController = UIAlertController.Create (null, msg, UIAlertControllerStyle.Alert);
		alertController.AddAction (UIAlertAction.Create ("Ok", UIAlertActionStyle.Default, null));
		controller.PresentViewController (alertController, true, null);
		completionHandler ();
	}
}
```

### API Enhancements

* [3127](https://github.com/xamarin/xamarin-macios/pull/3127) -  [watchos][accelerate] Enable Accelerate framework on watchOS
* [3247](https://github.com/xamarin/xamarin-macios/issues/3247) -  [generator] Add support for `[DesignatedDefaultCtorAttribute]` as a type-level attribute
* [3392](https://github.com/xamarin/xamarin-macios/issues/3392) -  [scenekit] Adds `[NullAllowed]` to `ISCNSceneRenderer.OverlayScene`
* [34135](https://bugzilla.xamarin.com/show_bug.cgi?id=34135) -  [security] Add new `SecKey.GenerateKeyPair` overloads
* [35009](https://bugzilla.xamarin.com/show_bug.cgi?id=35009) -  [foundation] Add `NSLinguisticAnalysis` category
* [40520](https://bugzilla.xamarin.com/show_bug.cgi?id=40520) -  [uikit] Add `[Advice]` on `UIImage.FromBundle` to mention it was not thread safe before iOS9
* [41292](https://bugzilla.xamarin.com/show_bug.cgi?id=41292) -  [foundation] Add `NSBundle.GetLocalizedString` returning an `NSString`
* [59294](https://bugzilla.xamarin.com/show_bug.cgi?id=59294) -  [coreimage] Enable `ImageRepresentation` strong dictionary helpers
* [60740](https://bugzilla.xamarin.com/show_bug.cgi?id=60740) -  [foundation] Add `NSDateComponentUndefined` constant

### Tooling Enhancements

* [3200](https://github.com/xamarin/xamarin-macios/issues/3200) -  [mtouch][mmp] Warn for invalid debug symbols files (e.g. out of sync)
* [56501](https://bugzilla.xamarin.com/show_bug.cgi?id=56501) -  [mtouch][mmp][bgen] Add support for response files
* [57531](https://bugzilla.xamarin.com/show_bug.cgi?id=57531) -  [generator] Support the use of `[Async]` attributes inside `[Category]`-decorated types
* [57870](https://bugzilla.xamarin.com/show_bug.cgi?id=57870) -  [generator] Teach generator about `[WrapAttribute]` on getters and setters
* [58350](https://bugzilla.xamarin.com/show_bug.cgi?id=58350) -  [generator] Handle sharpie's `[RequiresSuper]` attribute


## Release History

This version of Xamarin.iOS corresponds to our **15.7** (`d15-7`) milestone.

* May 15, 2018 - Xamarin.iOS 11.10.1.178
* May 7, 2018 - Xamarin.iOS 11.10.1.177
* May 3, 2018 - Xamarin.iOS 11.10.1.177
* April 25, 2018 - Xamarin.iOS 11.10.1.174
* April 18, 2018 - Xamarin.iOS 11.10.1.170
* April 4, 2018 - Xamarin.iOS 11.10.0.50
* March 19, 2018 - Xamarin.iOS 11.10.0.32
* March 8, 2018 - Xamarin.iOS 11.10.0.15 

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## May 15, 2018 - Xamarin.iOS 11.10.1.178

> This version is included in the Visual Studio 2017 version 15.7 service release 2.

### Issues Fixed

* [4033](https://github.com/mono/mono/issues/4033) - [mtouch] Take into account the contents of response files when determining whether the cache is valid or not

## May 7, 2018 - Xamarin.iOS 11.10.1.177

> This version is included in the Visual Studio 2017 version 15.7 release.

## May 3, 2018 - Xamarin.iOS 11.10.1.177

> This version is included in the Visual Studio 2017 version 15.7 Preview 6 release.

### Issues Fixed

* [7685](https://github.com/mono/mono/issues/7685) - [mono][watchos] Align `cinfo->stack_usage` to 16 bytes on watchOS
* [8403](https://github.com/mono/mono/issues/8403) - [mono] Fix invalid IL when running .NET Standard 1.5 code
* [58413](https://bugzilla.xamarin.com/show_bug.cgi?id=58413) - [mono] Replace `mono_msec_boottime()` with CoreCLR implementation

## April 25, 2018 - Xamarin.iOS 11.10.1.174

> This version is included in the Visual Studio 2017 version 15.7 Preview 5 release.

### Issues Fixed

* [3930](https://github.com/xamarin/xamarin-macios/issues/3930) - [watchos] Fix MT4116 / NullReferenceException building a watchOS app extension including an extension

## April 18, 2018 - Xamarin.iOS 11.10.1.170

> This version is included in the Visual Studio 2017 version 15.7 Preview 4 release.

### Xcode 9.3 Support

This preview is the first, 15.7-based release, to support Xcode 9.3 and the bundled iOS (11.3), tvOS (11.3) and watchOS (4.3) SDKs. More information on Xcode 9.3 support can be found in the (15.6-based) [Xamarin.iOS 11.9](xamarin.ios_11.9) release notes.

### Issues Fixed

* [3199](https://github.com/xamarin/xamarin-macios/issues/3199) - [msbuild] Skip (nuget) reference assemblies passed to `mtouch`
* [3742](https://github.com/xamarin/xamarin-macios/issues/3742) - [foundation] Ensure we do raise 401 on NTLM when no credentials are present

### API Enhancements

* [3870](https://github.com/xamarin/xamarin-macios/issues/3870) - [arkit] Add missing `ARHitTestResultType` binding

### Tooling Enhancements

* [3875](https://github.com/xamarin/xamarin-macios/pull/3875) - [generator] Register models with unique names to not match platform types. Related to issue [3832](https://github.com/xamarin/xamarin-macios/issues/3832)

## April 4, 2018 - Xamarin.iOS 11.10.0.50

> This version is included in the Visual Studio 2017 version 15.7 Preview 3 release.

### Issues Fixed

* [3653](https://github.com/xamarin/xamarin-macios/issues/3653) - [mtouch] mono-symbolicate errors "Warning: MVID directory does not exist"
* [7364](https://github.com/mono/mono/issues/7364) - [runtime] watchOS/LLVM crashes at launch on device in Release
* [61054](https://bugzilla.xamarin.com/show_bug.cgi?id=61054) - [Foundation] Ensure that we do not dispose the possibly shared data in the NSUrlSessionHandler
* [3717](https://github.com/xamarin/xamarin-macios/pull/3717) - [ObjCRuntime] Don't double-retain blocks
* [7472](https://github.com/mono/mono/issues/7472) - [runtime] `NullReferenceException` when trying to use an extension method on a `null` object as an assignment value for an `Action` or `Func` variable

### API Enhancements

* [3732](https://github.com/xamarin/xamarin-macios/issues/3732) - [Security] Adding new SecAccessControlCreateFlags 

## March 19, 2018 - Xamarin.iOS 11.10.0.32

> This version is included in the Visual Studio 2017 version 15.7 Preview 2 release.

### Issues Fixed

* Fixed generated profiling logs to be compatible with the Xamarin Profiler
* [PR3658](https://github.com/xamarin/xamarin-macios/pull/3658) - [Registrar] Show warning instead of NRE when code almost implements optional protocols

### API Enhancements

* [PR3502](https://github.com/xamarin/xamarin-macios/pull/3502) - [Security] Strongly-typed key generation APIs

## March 8, 2018 - Xamarin.iOS 11.10.0.15

> This version is included in the Visual Studio 2017 version 15.7 Preview 1 release.

### Issues Fixed

* [3265](https://github.com/xamarin/xamarin-macios/issues/3265) - [mtouch] Make sure the `xamarin_localized_string_format*` functions are available in `simlauncher`
* [3372](https://github.com/xamarin/xamarin-macios/issues/3372) -  [linker] Mark all `TypeConverter` if `TypeDescriptor` is used
* [60088](https://bugzilla.xamarin.com/show_bug.cgi?id=60088) -  [debugger] Fixed `Assertion at ../../../../external/mono/mono/mini/debugger-agent.c:4765, condition `array->len == 1` not met
* [60771](https://bugzilla.xamarin.com/show_bug.cgi?id=60771) -  [aot] Fixed `Attempting to JIT compile method 'System.Runtime.CompilerServices.Unsafe:Add (byte&,int)' while running in aot-only mode`

### Breaking Changes

* [PR3170:](https://github.com/xamarin/xamarin-macios/pull/3170) [metalperformanceshaders] Fix `MPSImageLanczosScale` base class. As part of the fix the `MPSImageScale.ScaleTransform` property changed to be a nullable value-type. The previous API did not work correctly so this should not affect applications being re-compiled.
* [3832](https://github.com/xamarin/xamarin-macios/issues/3832) - error MT4116: Could not register the assembly '\*': error MT4118: Cannot register two managed types ('\*, \*' and '\*, \*') with the same native name ('\*'). See below for more information.
* [4065](https://github.com/xamarin/xamarin-macios/issues/4065) - The 'isWrapper' argument to the [Register] attribute must be correct for models (causing 'error MT5211: Native linking failed, undefined Objective-C class ...' if not correct).

#### More information about [#3832](https://github.com/xamarin/xamarin-macios/issues/3832)

When binding Objective-C protocols, a typical binding would additionally
create a managed type whose name matched the Objective-C protocol.
Xamarin.iOS would then try to create a corresponding Objective-C type for
this managed type.

Unfortunately this leads to a undetermined behavior, because there might
already be an existing Objective-C type with the same name, defined by
Apple (or someone else). If two Objective-C types with the same name would
be encountered at runtime, only one of them would be loaded and used
everywhere. This would lead to random behavior, because the loaded type
might not match the code: for instance the type defined by Xamarin.iOS
could end up being used in Apple's code (or vice versa).

In this version of Xamarin.iOS we've changed how we create such
Objective-C types: when using the static registrar they're created at
build time. This means that the Objective-C runtime will detect any such
duplicates, and issue a warning at launch, like this [1]:

```
Class MTLCaptureScope is implemented in both /System/Library/Frameworks/Metal.framework/Versions/A/Metal (0x7fffa806f1d0) and /path/to/myapp (0x10d8aa858). One of the two will be used. Which one is undefined.
```

An additional consequence is that we'll detect if there are multiple
models with the same Objective-C name at build time, leading to the MT4116
build error.

One potential cause for this is if there are multiple binding projects
binding the same protocol:

```csharp
[Protocol, Model]
[BaseType (typeof (NSObject))]
interface MyProtocol {}
```

Which would result in:

```
error MT4116: Could not register the assembly 'MyBindingLibrary2': error MT4118: Cannot register two managed types ('MyProtocol, MyBindingLibrary1' and 'MyProtocol, MyBindingLibrary2') with the same native name ('MyProtocol')
```

In order to resolve this problem, we've implemented a way to specify the
Objective-C names for models:

```csharp
[Protocol, Model (AutoGeneratedName = true)]
[BaseType (typeof (NSObject))]
interface MyProtocol {}
```

This will auto-generate a unique name for the model (currently the name
of the assembly + the full name of the type, but it may change in the
future).

It's also possible to specify the Objective-C name explicitly:

```csharp
[Protocol, Model (Name = "MyProtocol1")]
[BaseType (typeof (NSObject))]
interface MyProtocol {}
```

Implementing either of these solutions in one of the binding projects
will fix the MT4116 error.

[1] All instances of these warnings (where one library mentioned in the
warning is a system library, and another is the app) should have been
fixed; if that's not the case, please 
[file an issue](https://github.com/xamarin/xamarin-macios/wiki/Submitting-Bugs-&-Suggestions).

### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from [Mono 5.10](https://github.com/mono/mono/commits/2017-12) ([hash](https://github.com/mono/mono/commit/hash)).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.10/).

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#Requirements)) is often possible, but some features may not be available. Also some limitations might requires workarounds, e.g:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

### Changing build options may not rebuild correctly

Due to [a bug](https://github.com/xamarin/xamarin-macios/issues/4033) in our
logic to determine whether build options changed, we're not always detecting
when a full build is needed (as opposed to an incremental build).

This means that when changing build options in the executable project's
project configuration, it might be necessary to clean the project before any
changes take effect.

```
> ℹ️  **Note:** This is *only* applicable to changes in the project itself;
> code changes are not affected and continue to trigger correct builds.
```
## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.8 stable release:

* [iOS](/releases/ios/api_changes/ios-11-9-1-11-10-1)
* [tvOS](/releases/ios/api_changes/tvos-11-9-1-11-10-1)
* [watchOS](/releases/ios/api_changes/watchos-11-9-1-11-10-1)

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios) and [GitHub Issues](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d15-7`
* [mono](https://github.com/mono/mono/tree/2017-12) branch `2017-12`

### A big Thank You! to the following folks that helped to make Xamarin.iOS and Xamarin.Mac even better:

* [@mdbech](https://github.com/mdbech)
* [@cwensley](https://github.com/cwensley)

