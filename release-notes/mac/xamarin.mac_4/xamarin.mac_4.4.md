---
id: d1a41574-ec47-4499-a7fc-ad9a8719f142
title: "Xamarin.Mac 4.4"
---

# Xamarin.Mac 4.4
Last Update: 5/30/2018


[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

> ⚠️  **Update to macOS High Sierra**
> The most recent version of Xcode (9.3) requires macOS High Sierra (10.13).
> developers should update to macOS High Sierra as soon as possible
> in order to support the Xcode 9.3 SDKs and API.

#### Requirements

* The latest features and API requires Xcode 9.3 and the bundled macOS SDKs;
* Apple Xcode 9.3 requires a Mac running macOS 10.13.2 (High-Sierra) or newer;

## What's New in this Release

* [32-bit Warnings and Stripping](#32-bit-warnings-and-stripping)
* [Registrar Optimizations](#registrar-optimizations)
* [Xcode 9.3 Support](#xcode-9.3-support)
* [New Bindings](#new-bindings)
* [WeakAttribute](#WeakAttribute)
* [API Enhancements](#api-enhancements)
* [Tooling Enhancements](#tooling-enhancements)

### 32-bit Warnings and Stripping

Apple has [announced](https://developer.apple.com/news/?id=06282017a) that it will not allow macOS App Store submissions of 32-bit apps (starting January 2018). 

In addition 32-bit applications will not run on the version of macOS after High Sierra "without compromises". 

Two related changes are included in Xamarin.Mac 4.4:

* Warnings are included when building 32-bit applications to help prepare developers for the transition.
* Release mode configurations will, by default, strip unused architectures from bundled native libraries. In addition to reduce application size, this is needed for acceptance into the macOS App Store. This can be disabled by adding "--optimize=-trim-architectures" to the Additional MMP Arguments in the Mac Build project settings.

### Registrar Optimizations

This is a set of optimizations that improves the output from the static registrar. This results in:

* **Smaller applications** - The linked `Xamarin.Mac.dll` is smaller than before since the information (e.g. custom attributes) needed only at build time can now be removed. This also allows the linker to remove more code than before (since less code is being referenced);
* **Faster application startup** - More registration work is being done at build time instead of at runtime. E.g. this removes the need to use (slow) reflection on custom attributes to register types and methods;
* **Reduced memory usage** - The avoided work also reduces the memory required for applications.

### Xcode 9.3 Support

The macOS 10.13.4 SDK added support for a new **BusinessChat** framework (shared with iOS). Bindings for BusinessChat and several other, smaller API additions are included in this new release.

### New Bindings

Beside the new API added for macOS 10.13.4 in Xcode 9.3 this release also provides:

* CoreSpotlight.framework API have been enabled (available in High Sierra and above);
* Additional `MusicPlayer` related types in AudioToolbox.framework;
* Additional macOS-only types in CoreAudioKit.framework;
* Additional support for `GCMicroGamepad` in GameController.framework;
* Additional support for `PHLivePhotoView` API in PhotoUI.framework;
* `SLComposeServiceViewController` in Social.framework;

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
 
* [3206](https://github.com/xamarin/xamarin-macios/issues/3206) - [webkit] Allow `null` for `DomRange` inside `WebView.SetSelectedDomRange`
* [3247](https://github.com/xamarin/xamarin-macios/issues/3247) -  [generator] Add support for `[DesignatedDefaultCtorAttribute]` as a type-level attribute
* [3392](https://github.com/xamarin/xamarin-macios/issues/3392) -  [scenekit] Adds `[NullAllowed]` to `ISCNSceneRenderer.OverlayScene`
* [34135](https://bugzilla.xamarin.com/show_bug.cgi?id=34135) -  [security] Add new `SecKey.GenerateKeyPair` overloads
* [35009](https://bugzilla.xamarin.com/show_bug.cgi?id=35009) -  [foundation] Add `NSLinguisticAnalysis` category
* [41292](https://bugzilla.xamarin.com/show_bug.cgi?id=41292) -  [foundation] Add `NSBundle.GetLocalizedString` returning an `NSString`
* [59294](https://bugzilla.xamarin.com/show_bug.cgi?id=59294) -  [coreimage] Enable `ImageRepresentation` strong dictionary helpers
* [60740](https://bugzilla.xamarin.com/show_bug.cgi?id=60740) -  [foundation] Add `NSDateComponentUndefined` constant
* [60826](https://bugzilla.xamarin.com/show_bug.cgi?id=60826) -  [appkit] Change some `NSOpenGL*` types to be thread safe

### Tooling Enhancements

* [3200](https://github.com/xamarin/xamarin-macios/issues/3200) -  [mtouch][mmp] Warn for invalid debug symbols files (e.g. out of sync)
* [3325](https://github.com/xamarin/xamarin-macios/issues/3325) -  [mmp] Warn when building 32-bit macOS applications
* [3367](https://github.com/xamarin/xamarin-macios/issues/3367) - [mmp] Add stripping of 32-bit dylibs to work with new App Store restrictions
* [56501](https://bugzilla.xamarin.com/show_bug.cgi?id=56501) -  [mtouch][mmp][bgen] Add support for response files
* [57531](https://bugzilla.xamarin.com/show_bug.cgi?id=57531) -  [generator] Support the use of `[Async]` attributes inside `[Category]`-decorated types
* [57870](https://bugzilla.xamarin.com/show_bug.cgi?id=57870) -  [generator] Teach generator about `[WrapAttribute]` on getters and setters
* [58350](https://bugzilla.xamarin.com/show_bug.cgi?id=58350) -  [generator] Handle sharpie's `[RequiresSuper]` attribute
* The command-line tool `mmp` [now](https://github.com/xamarin/xamarin-macios/commit/e8d16c925bb74636366b00b5c6603514c94af763) accepts response files for arguments.

### Release History

This version of Xamarin.Mac corresponds to our **15.7** (`d15-7`) milestone.

* May 30, 2018 - Xamarin.Mac 4.4.1.193
* May 15, 2018 - Xamarin.Mac 4.4.1.178
* May 7, 2018 - Xamarin.Mac 4.4.1.176
* May 3, 2018 - Xamarin.Mac 4.4.1.176
* April 25, 2018 - Xamarin.Mac 4.4.1.173
* April 18, 2018 - Xamarin.Mac 4.4.1.169
* April 4, 2018 - Xamarin.Mac 4.4.0.49
* March 19, 2018 - Xamarin.Mac 4.4.0.31
* March 8, 2018 - Xamarin.Mac 4.4.0.14 

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## May 30, 2018 - Xamarin.Mac 4.4.1.193

> This version is included in the Visual Studio 2017 version 15.7 service release 3.

### Issues Fixed

* [3882](https://github.com/xamarin/xamarin-macios/pull/3882) - [mmp] Properly link with BusinessChat framework

## May 15, 2018 - Xamarin.Mac 4.4.1.178

> This version is included in the Visual Studio 2017 version 15.7 service release 2.

### Issues Fixed

* [4074](https://github.com/mono/mono/issues/4074) - [appkit] Fix default values for touchbar APIs in `NSTextViewDelegate`

## May 7, 2018 - Xamarin.Mac 4.4.1.176

> This version is included in the Visual Studio 2017 version 15.7 release.

## May 3, 2018 - Xamarin.Mac 4.4.1.176

> This version is included in the Visual Studio 2017 version 15.7 Preview 6 release.

### Issues Fixed

* [8403](https://github.com/mono/mono/issues/8403) - [mono] Fix invalid IL when running .NET Standard 1.5 code
* [58413](https://bugzilla.xamarin.com/show_bug.cgi?id=58413) - [mono] Replace `mono_msec_boottime()` with CoreCLR implementation

## April 25, 2018 - Xamarin.Mac 4.4.1.173

> This version is included in the Visual Studio 2017 version 15.7 Preview 5 release.

### Issue Fixed

* [3920](https://github.com/xamarin/xamarin-macios/issues/3920) - [msbuild] Fix reading AOT options from IDE

## April 18, 2018 - Xamarin.Mac 4.4.1.169

> This version is included in the Visual Studio 2017 version 15.7 Preview 4 release.

This preview is the first, 15.7-based release, to support Xcode 9.3 and the bundled macOS (10.13.4).

### Issues Fixed

* [3199](https://github.com/xamarin/xamarin-macios/issues/3199) - [msbuild] Skip (nuget) reference assemblies passed to `mtouch`
* [3742](https://github.com/xamarin/xamarin-macios/issues/3742) - [foundation] Ensure we do raise 401 on NTLM when no credentials are present

### Tooling Enhancements

* [3875](https://github.com/xamarin/xamarin-macios/pull/3875) - [generator] Register models with unique names to not match platform types. Related to issue [3832](https://github.com/xamarin/xamarin-macios/issues/3832)

## April 4, 2018 - Xamarin.Mac 4.4.0.49

> This version is included in the Visual Studio 2017 version 15.7 Preview 3 release.

### Issues Fixed

* [3674](https://github.com/xamarin/xamarin-macios/issues/3674) - [msbuild] Fail to sign Mac OS project with Entitlements properly
* [3725](https://github.com/xamarin/xamarin-macios/issues/3725) - [mmp] Xamarin.Mac New Project does not link on 10.11.6 without linking enabled
* [61054](https://bugzilla.xamarin.com/show_bug.cgi?id=61054) - [Foundation] Ensure that we do not dispose the possibly shared data in the NSUrlSessionHandler
* [3717](https://github.com/xamarin/xamarin-macios/pull/3717) - [ObjCRuntime] Don't double-retain blocks
* [7472](https://github.com/mono/mono/issues/7472) - [runtime] `NullReferenceException` when trying to use an extension method on a `null` object as an assignment value for an `Action` or `Func` variable

### API Enhancements

* [3792](https://github.com/xamarin/xamarin-macios/issues/3792) - [Appkit] Adds NullAllowed to NSTableCellView.ObjectValue
* [3777](https://github.com/xamarin/xamarin-macios/issues/3777) - [Appkit] Adds NullAllowed to NSGridCell.ContentView
* [3776](https://github.com/xamarin/xamarin-macios/issues/3776) - [Appkit] Adds NullAllowed to NSTableView.RegisterNib
* [3732](https://github.com/xamarin/xamarin-macios/issues/3732) - [Security] Adding new SecAccessControlCreateFlags

## March 19, 2018 - Xamarin.Mac 4.4.0.31

> This version is included in the Visual Studio 2017 version 15.7 Preview 2 release.

### Issues Fixed

* Fixed generated profiling logs to be compatible with the Xamarin Profiler
* [PR3658](https://github.com/xamarin/xamarin-macios/pull/3658) - [Registrar] Show warning instead of NRE when code almost implements optional protocols
* [PR3631](https://github.com/xamarin/xamarin-macios/pull/3631) - [Runtime] Enable signal chaining for Xamarin.Mac

### API Enhancements

* [PR3502](https://github.com/xamarin/xamarin-macios/pull/3502) - [Security] Strongly-typed key generation APIs

### Tooling Enhancements

* [PR3575](https://github.com/xamarin/xamarin-macios/pull/3575) - [MMP] Allow resolving of assemblies passed in as references

## March 8, 2018 - Xamarin.Mac 4.4.0.14

> This version is included in the Visual Studio 2017 version 15.7 Preview 1 release.

### Issues Fixed

* [3303](https://github.com/xamarin/xamarin-macios/issues/3303) - [avfoundation] Fix `AVAudioUnitComponentManager` default .ctor crash
* [3372](https://github.com/xamarin/xamarin-macios/issues/3372) - [linker] Mark all `TypeConverter` if `TypeDescriptor` is used
* [60634](https://bugzilla.xamarin.com/show_bug.cgi?id=60634) - [runtime] Fixed `Assertion failure 'align > 0`

### Breaking Changes

* [PR3170:](https://github.com/xamarin/xamarin-macios/pull/3170) [metalperformanceshaders] Fix `MPSImageLanczosScale` base class. As part of the fix the `MPSImageScale.ScaleTransform` property changed to be a nullable value-type. The previous API did not work correctly so this should not affect applications being re-compiled.
* [3832](https://github.com/xamarin/xamarin-macios/issues/3832) - error MT4116: Could not register the assembly '\*': error MT4118: Cannot register two managed types ('\*, \*' and '\*, \*') with the same native name ('\*'). See below for more information.

#### More information about [#3832](https://github.com/xamarin/xamarin-macios/issues/3832)

When binding Objective-C protocols, a typical binding would additionally
create a managed type whose name matched the Objective-C protocol.
Xamarin.Mac would then try to create a corresponding Objective-C type for
this managed type.

Unfortunately this leads to a undetermined behavior, because there might
already be an existing Objective-C type with the same name, defined by
Apple (or someone else). If two Objective-C types with the same name would
be encountered at runtime, only one of them would be loaded and used
everywhere. This would lead to random behavior, because the loaded type
might not match the code: for instance the type defined by Xamarin.Mac
could end up being used in Apple's code (or vice versa).

In this version of Xamarin.Mac we've changed how we create such
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


## Known Issues

### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from [Mono 5.10](https://github.com/mono/mono/commits/2017-12) ([hash](https://github.com/mono/mono/commit/hash)).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.10/).


## API Diff

This [document](/releases/mac/api_changes/macos-4-2-1-4-4-99) contains a complete list of the API changes since the Xamarin.Mac 4.2 stable release.

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [GitHub Issues](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `master`
* [mono](https://github.com/mono/mono/tree/2017-12) branch `2017-12`

### A big Thank You! to the following folks that helped to make Xamarin.iOS and Xamarin.Mac even better:

* [@mdbech](https://github.com/mdbech)
* [@cwensley](https://github.com/cwensley)

