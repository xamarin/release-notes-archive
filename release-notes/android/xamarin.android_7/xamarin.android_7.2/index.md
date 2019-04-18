---
id: B751CD9B-84AB-4518-9752-2F33A776EF71
title: "Xamarin.Android 7.2"
---

Xamarin.Android 7.2: Yay, fixes!

# OSS Core

Xamarin.Android 7.0 is the first release to use the open-source
repositories:

* Core JNI interaction logic is in the
    [Java.Interop](https://github.com/xamarin/Java.Interop) repo
* Android bindings and MSBuild tooling are in the
    [xamarin-android](https://github.com/xamarin/xamarin-android) repo.
* Chat is in the
    [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android?at=57c487782dcc4f312942a519).

# System Requirements

Xamarin.Android 7.1 requires
[JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
to use the Android Nougat (API 24) APIs. Using the Android build-tools r24+ package may also
require using JDK 1.8.
You can continue to use earlier versions of the JDK when using earlier build-tools packages
and when targeting earlier Android API levels:

* [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) - up to API 24+

* [JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) - up to API 23

* [JDK 1.6](http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase6-419409.html) - up to API 20

Additionally, a 64-bit version of the JDK is required to use
[custom controls in the Android designer][gui-designer].

[gui-designer]: https://developer.xamarin.com/releases/vs/xamarin.vs_4/xamarin.vs_4.2/#androiddesignercustomcontrols

**The simplest option is to install the 64-bit version of JDK 1.8 since it is
backwards compatible with all of the previous API levels and supports the new
Android designer features.**

(One unfortunate complication with JDK 1.8 is that is **not** compatible with
the outdated version of Proguard that is included in the Android SDK. Currently
this will cause an error "Unsupported class version number \[52.0\]" when
attempting to use the Proguard or Multidex features in Xamarin.Android. See
[44187](https://bugzilla.xamarin.com/show_bug.cgi?id=44187).)


# Vulkan Support

Android v7.0 Nougat adds support for the
[Vulkan API](https://developer.android.com/ndk/guides/graphics/index.html).
Vulkan support will *not* be distributed as part of the core Xamarin.Android
binding. Instead, please use the
[VulkanSharp](https://www.nuget.org/packages/VulkanSharp/) NuGet package, and the
[XLogo sample app](https://github.com/mono/VulkanSharp/tree/master/samples/XLogo).


# Native Library Use

Due to a change by Google,
[Android N will now only permit linking to NDK-provided native libraries][ndk].
`libsqlite.so` is *not* an NDK-provided native library. Consequently,
existing apps using e.g. `Mono.Data.Sqlite.dll` *will* ***crash*** when
running on Android N. This may include other SQLite-using assemblies,
not distributed with Xamarin.Android.

[ndk]: https://developer.android.com/about/versions/nougat/android-7.0-changes.html#ndk

Xamarin.Android 7.0, which is part of Cycle 8,
[updates `Mono.Data.Sqlite.dll`](#mono-data-sqlite) to include
a custom built version of `libsqlite.so`, named `libsqlite3_xamarin.so`.

**All Developers** need to audit their code for P/Invoke and ensure that referenced
native libraries are either included in the Android NDK, or are included within
the `app.apk` itself. The only Xamarin.Android-provided assembly impacted by
this change is `Mono.Data.Sqlite.dll`.


# Known Issues

Xamarin.Android [changed the default GC Bridge](#gc-bridge-tarjan) from
`old` to `tarjan`.

Unfortunately, a [few bugs](https://bugzilla.xamarin.com/show_bug.cgi?id=47577)
have been reported which suggest a bug within the Tarjan GC bridge.

If this happens, [create an `@(AndroidEnvironment)` file](/guides/android/advanced_topics/environment/)
and add the following line:

    MONO_GC_PARAMS=bridge-implementation=old

This will cause the app to use the previous GC bridge.

<!--
  JONP: 7.2.0 last updated from commit monodroid/d15-1/b8e38845fbf92114125a07f938d47739facdc779
-->

<a name="0"/>
<a name="Xamarin.Android_7.2.0"/>

# Xamarin.Android 7.2

The Xamarin.Android 7.2 release primarily includes bug fixes.


<a name="experimental-features"/>

## Experimental Features

Xamarin.Android 7.0 introduces several experimental features, which are still experimental:

* [TLS 1.2 support in `WebRequest`](#btls)
* [Concurrent GC Support](#concurrent-gc)
* [Improved Fast Deployment](#Fast_Deployment)

<a name="btls" />

### TLS 1.2 support in `WebRequest`

[Xamarin.Android 7.1 added `AndroidClientHandler`][xa71-AndroidClientHandler],
which uses the native Java APIs to provide TLS 1.2 support. However, there are
two problems with `AndroidClientHandler`:

1. It can only be used with [`HttpClient`][httpclient], and
2. It requires Android 5.0 and later to operate. (Prior Android versions might
    not support TLS 1.2, and since `AndroidClientHandler` uses the native Java
    TLS stack...)

[xa71-AndroidClientHandler]: /releases/android/xamarin.android_6/xamarin.android_6.1/#Native_HttpClientHandler
[httpclient]: https://msdn.microsoft.com/en-us/library/system.net.http.httpclient(v=vs.118).aspx

To solve these problems, [Boring SSL][boring-ssl] can be used as the
lowest-level TLS implementation. Originally announced
[last September][btls-announce], Boring SSL can be embedded within
a Xamarin.Android application, allowing [`HttpWebRequest`][HttpWebRequest]
to communicate with TLS 1.2 endpoints. When enabled, the normal
`HttpClient` stack also uses Boring SSL.

[boring-ssl]: https://boringssl.googlesource.com/boringssl/
[btls-announce]: http://tirania.org/blog/archive/2016/Sep-30.html
[HttpWebRequest]: https://msdn.microsoft.com/en-us/library/system.net.httpwebrequest.aspx

To enable use of BoringSSL, add the `$(AndroidTlsProvider)` MSBuild property
to the application project, with a value of `btls`:

    <PropertyGroup>
      <AndroidTlsProvider>btls</AndroidTlsProvider>
    </PropertyGroup>

When enabled, a new `libmono-btls-shared.so` shared library will be present
within the `.apk`.

The default value of the `$(AndroidTlsProvider)` MSBuild property is the empty
string, i.e. not set, which will use the managed TLS implementation, which
*does not* support TLS 1.2.

The default value may change in a future release.

<a name="concurrent-gc">

### Concurrent GC Support

The new `$(AndroidEnableSGenConcurrent)` MSBuild property which controls
whether or not the concurrent GC is enabled.

`$(AndroidEnableSGenConcurrent)` is a boolean value. When `True`, then
Mono's GC is set to `marksweep-conc`; when `False`, then
Mono's GC is set to `marksweep`.

The default value is `False`.

See [Mono's **ConcurrentSGen** documentation][mono-marksweep-conc]
for more information.

[mono-marksweep-conc]: http://www.mono-project.com/docs/about-mono/releases/4.8.0/#concurrent-sgen

<a name="Fast_Deployment"/>

### Improved Fast Deployment

[Fast Deployment](https://developer.xamarin.com/guides/android/under_the_hood/build_process/#Fast_Deployment)
is a way to avoid rebuilding and redeploying Android Packages (`.apk` files)
when assemblies have changed in a way that doesn’t require changing the generated
[Android Callable Wrappers](https://developer.xamarin.com/guides/android/advanced_topics/java_integration_overview/android_callable_wrappers/)
or altered any included Android Assets and Resources.

Xamarin.Android 7.0 will optionally allow Android Assets, Resources, and
compiled Java libraries to particpate in fast deployment as well, further
reducing the number of situations in which a possibly slow `.apk` rebuild
and redeploy will be required.

This new behavior is disabled by default.
It will be enabled by default in the Xamarin.Android 7.1 series.

To enable this new functionality, set the `$(AndroidFastDeploymentType)`
MSBuild property to `Assemblies:Dexes`:

```
<AndroidFastDeploymentType>Assemblies:Dexes</AndroidFastDeploymentType>
```

#### Adding Resources to the Default Project

For example, assume a new (default) Application project which has already been
deployed to a target device.

1. Copy `Resources\layout\Main.axml` to `Resources\layout\Another.axml`,
    and add `Resources\layout\Another.axml` to the project.
2. Run the project.

(2) will require that the `.apk` be rebuilt and re-deployed to the target.
In previous versions, (2) could take 16 seconds.

With the new system


TODO:

Add some small benchmarks about what happens during dev when code changes,
or a resource changes, numbers before/after

<a name="Workflow_Changes" />

## Workflow Changes

The `mcw-gen`/`mcw-gen.exe` utility is deprecated and will not be provided
in future releases.

We believe that this won't actually break anybody, because as far as we can
tell nobody was ever actually using that utility.


<a name="Known_Issues"/>

## Known Issues


<a name="Bug_Fixes"/>

## Bug Fixes

* [5979](https://bugzilla.xamarin.com/show_bug.cgi?id=5979):
    List support in generic method instantiation in binding got broken by JavaObjectExtensions.JavaCast()
* [43513](https://bugzilla.xamarin.com/show_bug.cgi?id=43513):
    Android Binding Adding Generic Arg where one does not exist
* [44673](https://bugzilla.xamarin.com/show_bug.cgi?id=44673):
    AndroidClientHandler ignores Timeout value and CancellationToken
* [46397](https://bugzilla.xamarin.com/show_bug.cgi?id=46397):
    Xamarin.Forms build failed with &quot;Error executing task ResolveAssemblies: Out of memory&quot;
* [46454](https://bugzilla.xamarin.com/show_bug.cgi?id=46454):
    need to escape C# keywords in some parameter reference
* [46931](https://bugzilla.xamarin.com/show_bug.cgi?id=46931):
    'Error: no package specified' message with 7.0.2.37
* [48016](https://bugzilla.xamarin.com/show_bug.cgi?id=48016):
    System.Net.NetworkInformation.DnsAddresses is always empty. Fix included.
* [48508](https://bugzilla.xamarin.com/show_bug.cgi?id=48508):
    Archiving Android application is archiving old builds
* [48678](https://bugzilla.xamarin.com/show_bug.cgi?id=48678):
    NDK r12b+ is not supported
* [51356](https://bugzilla.xamarin.com/show_bug.cgi?id=51356):
    Unable to run Multi-Dex
* [51480](https://bugzilla.xamarin.com/show_bug.cgi?id=51480):
    Improved fast deployment doesn't build my app
* [51774](https://bugzilla.xamarin.com/show_bug.cgi?id=51774):
    AndroidClientHandler throws NetworkOnMainThreadException on Cancelation via cancelation delegate call
* [51175](https://bugzilla.xamarin.com/show_bug.cgi?id=51175):
    Fallback to portable pdb with roslyn doesn't work if csproj is missing &lt;DebugType&gt;
* [52259](https://bugzilla.xamarin.com/show_bug.cgi?id=52259):
    XA depends on random source file from the mono tree that is gone on master

<!-- Access Denied bugs:
* [31985](https://bugzilla.xamarin.com/show_bug.cgi?id=31985):
* [32457](https://bugzilla.xamarin.com/show_bug.cgi?id=32457):
* [41860](https://bugzilla.xamarin.com/show_bug.cgi?id=41860):
* [44185](https://bugzilla.xamarin.com/show_bug.cgi?id=44185):
* [44217](https://bugzilla.xamarin.com/show_bug.cgi?id=44217):
* [46344](https://bugzilla.xamarin.com/show_bug.cgi?id=46344):
* [46375](https://bugzilla.xamarin.com/show_bug.cgi?id=46375):
* [46509](https://bugzilla.xamarin.com/show_bug.cgi?id=46509):
* [46698](https://bugzilla.xamarin.com/show_bug.cgi?id=46698):
* [46707](https://bugzilla.xamarin.com/show_bug.cgi?id=46707):
* [51337](https://bugzilla.xamarin.com/show_bug.cgi?id=51337):
* [51415](https://bugzilla.xamarin.com/show_bug.cgi?id=51415):
* [51431](https://bugzilla.xamarin.com/show_bug.cgi?id=51431):
* [51604](https://bugzilla.xamarin.com/show_bug.cgi?id=51604):
* [51636](https://bugzilla.xamarin.com/show_bug.cgi?id=51636):
* [52673](https://bugzilla.xamarin.com/show_bug.cgi?id=52673):
* [53122](https://bugzilla.xamarin.com/show_bug.cgi?id=53122):
* [53163](https://bugzilla.xamarin.com/show_bug.cgi?id=53163):
 -->


<a name="integrated-mono" />

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.8](http://www.mono-project.com/docs/about-mono/releases/4.8.0/)
[commit e464ddae](https://github.com/mono/mono/commit/e464ddae64cd181c360d4cf93d087db79c4fb192).


* [46929](https://bugzilla.xamarin.com/show_bug.cgi?id=46929):
    Datetime error on Mono.data.Sqlite
* [52437](https://bugzilla.xamarin.com/show_bug.cgi?id=52437):
    Random NullReferenceExceptions in StringBuilder.ThreadSafeCopy
* [52590](https://bugzilla.xamarin.com/show_bug.cgi?id=52590):
    Cannot compile for iOS, TypeBuilder exists in two places.
* [52845](https://bugzilla.xamarin.com/show_bug.cgi?id=52845):
    [Cycle 9] Satellite assemblies not bundled when using &quot;Bundle assemblies into native code&quot; due to &quot;unknown escape sequence&quot; error from gcc during mkbundle step
* [53066](https://bugzilla.xamarin.com/show_bug.cgi?id=53066):
    Can't Build Project in Debug with &quot;Could not AOT the assembly&quot;

<!-- Access Denied bugs:
* [52846](https://bugzilla.xamarin.com/show_bug.cgi?id=52846):
 -->


<a name="API_Changes" />

# API Changes

TODO

* API Level 10:
    [Mono.Android.dll](level_10_diff/mono.android.dll),
    [OpenTK.dll](level_10_diff/opentk.dll),
    [OpenTK-1.0.dll](level_10_diff/opentk-1.0.dll)
* API Level 15:
    [Mono.Android.dll](level_15_diff/mono.android.dll)
* API Level 16:
    [Mono.Android.dll](level_16_diff/mono.android.dll)
* API Level 17:
    [Mono.Android.dll](level_17_diff/mono.android.dll)
* API Level 18:
    [Mono.Android.dll](level_18_diff/mono.android.dll)
* API Level 19:
    [Mono.Android.dll](level_19_diff/mono.android.dll)
* API Level 20:
    [Mono.Android.dll](level_20_diff/mono.android.dll)
* API Level 21:
    [Mono.Android.dll](level_21_diff/mono.android.dll)
* API Level 22:
    [Mono.Android.dll](level_22_diff/mono.android.dll)
* API Level 23:
    [Mono.Android.dll](level_23_diff/mono.android.dll)
* API Level 24:
    [Mono.Android.dll](level_24_diff/mono.android.dll)
* API Level 25 (vs. API Level 24):
    [Mono.Android.dll](level_25_diff/mono.android.dll)

