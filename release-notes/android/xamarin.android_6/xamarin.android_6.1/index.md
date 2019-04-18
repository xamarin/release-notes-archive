---
id: 037099BB-F622-4C8B-A690-401FF27820E0
title: "Xamarin.Android 6.1"
---

Xamarin.Android 6.1 fixes numerous bugs.

**Note:** Xamarin.Android 6.1 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
to use Android Wear and API-21+.
JDK 1.6 may be used when targeting previous API levels.

***Note:***
Due to a change by Google,
[Android N will now only permit linking to NDK-provided native libraries][ndk].
`libsqlite.so` is *not* an NDK-provided native library. Consequently,
existing apps using e.g. `Mono.Data.Sqlite.dll` *will* ***crash*** when
running on Android N. This may include other SQLite-using assemblies,
not distributed with Xamarin.Android.

[ndk]: http://developer.android.com/preview/behavior-changes.html#ndk

Xamarin.Android 6.1.0 ("Cycle 7")
[updates `Mono.Data.Sqlite.dll`](#mono-data-sqlite) to include
a custom built version of `libsqlite.so`, named `libsqlite3_xamarin.so`.

**All Developers** need to audit their code for P/Invoke use and ensure that
referenced native libraries are either included in the Android NDK, or are
included within the `app.apk` itself. The only Xamarin.Android-provided
assembly impacted by this change is `Mono.Data.Sqlite.dll`.

<!--
  JONP: 6.1.2 last updated from commit monodroid/cycle7-sr1/f7057f639395ce7ddb5f1e8bdcdb99f9ee242657
-->

<a name="2"/>
<a name="Xamarin.Android_6.1.2"/>
# Xamarin.Android 6.1.2

<a name="Known_Issues_6.1.2"/>
## Known Issues

* [42082](https://bugzilla.xamarin.com/show_bug.cgi?id=42082):
    "Ionic.Zip.ZipException ... \_\_AndroidLibraryProjects\_\_.zip is not a
    valid zip file ---> System.TimeZoneNotFoundException" when building Android
    projects in certain Windows time zones.  **Temporary workaround**: Change
    the Windows time zone.  For example the _Central Time (US & Canada)_ time
    zone does not hit this error.

<a name="Upstream_Issues_6.1.2"/>
## Upstream Issues

* Upstream [215209](https://code.google.com/p/android/issues/detail?id=215209),
    (Xamarin tracking bug:
    [40156](https://bugzilla.xamarin.com/show_bug.cgi?id=40156)): ""aapt.exe"
    exited with code -1073741819" or "The file
    "obj\Debug\android\bin\packaged_resources" does not exist."  One reason
    these errors can appear is if version "24" of the Android SDK Build-tools
    package is installed.  That version of the Android Build-tools contains a
    bug which has been fixed in a more recent release (24.0.1).  See also the [corresponding Xamarin technical
    bulletin](https://releases.xamarin.com/technical-bulletin-android-sdk-build-tools-24/).
    **Recommended fix**: Upgrade to Android SDK Build-tools version 24.0.1+ or uninstall version 24 using the
    Android SDK Manager.

* "java.lang.UnsupportedClassVersionError: com/android/dx/command/Main  :
    Unsupported major.minor version 52.0".  One reason this error can
    appear is if version "24" of the Android SDK Build-tools package is
    installed, but Java JDK 1.8 is not installed.  Version "24" of the
    Android SDK Build-tools requires Java JDK 1.8 or higher.

<a name="Bug_Fixes_6.1.2"/>
## Bug Fixes

* Deploy `.dll.config` files during fast deployment.
* [40976](https://bugzilla.xamarin.com/show_bug.cgi?id=40976):
    Custom Application subclass does not extend MultiDexApplication when
    MultiDex is enabled
* [41100](https://bugzilla.xamarin.com/show_bug.cgi?id=41100):
    When Posting using Xamarin.Android.Net.AndroidClientHandler, receiving
    "Unexpected end of stream error"
* [41342](https://bugzilla.xamarin.com/show_bug.cgi?id=41342):
    The fix for [40976](https://bugzilla.xamarin.com/show_bug.cgi?id=40976)
    caused generation of incorrect Java Callable Wrappers for indirect
    subclasses of `Android.App.Application`, breaking Java callbacks into those
    subclasses.
* [42052](https://bugzilla.xamarin.com/show_bug.cgi?id=42052):
    Deployment fails with &quot;internal error: missing , in ID_SEND&quot; for
    Android N devices and emulators using the current Stable channel (Cycle 7)
* [42168](https://bugzilla.xamarin.com/show_bug.cgi?id=42168):
    A numeric comparison was attempted on
    &quot;$(\_DeviceSdkVersion)&quot; that evaluates to &quot;&quot; instead of a number, in condition &quot;$(\_DeviceSdkVersion) &gt;= 21&quot;.

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.4](http://www.mono-project.com/docs/about-mono/releases/4.4.0/)
[commit 7a80b708](https://github.com/mono/mono/commit/7a80b7082f5a3de2f9f99001d28ef62b8aabc180).

* Fixes to support .NET Standard 1.6
* [30686](https://bugzilla.xamarin.com/show_bug.cgi?id=30686):
    ZipArchive ctor throws InvalidDataException for WebConnectionStream
* [39282](https://bugzilla.xamarin.com/show_bug.cgi?id=39282):
    [System.IO.Compression] issues with ZipArchiveEntry streams
* [39669](https://bugzilla.xamarin.com/show_bug.cgi?id=39669):
    System.Configuration.DictionarySectionHandler is missing
* [40916](https://bugzilla.xamarin.com/show_bug.cgi?id=40916):
    [System.IO.Compression] ZipArchive can create an ZipArchiveEntry that has a modified time of DateTime.MinValue
* [41530](https://bugzilla.xamarin.com/show_bug.cgi?id=41530):
    [iOS]TimerTest failing randomly on devices,
* [41616](https://bugzilla.xamarin.com/show_bug.cgi?id=41616):
    Mono 4.4.0 crashes when using Socket.ConnectAsync to a unix domain socket if the path doesn't exist
* [41979](https://bugzilla.xamarin.com/show_bug.cgi?id=41979):
    CodeDom cannot call mcs because of invalid encoding configuration
* [42219](https://bugzilla.xamarin.com/show_bug.cgi?id=42219):
    [System.IO.Compression] Cannot create ZipArchive with duplicate entries with same name
* [42274](https://bugzilla.xamarin.com/show_bug.cgi?id=42274):
    System.IO.Compression.ZipArchive vs System.Xml.XmlReader


<!--
  JONP: 6.1.1 last updated from commit monodroid/c7sr0/7db2aac379d451ca08ebf968a715f32c2341afaf
-->

<a name="1"/>
<a name="Xamarin.Android_6.1.1"/>
# Xamarin.Android 6.1.1

<a name="Known_Issues_6.1.1"/>
## Known Issues

* [42082](https://bugzilla.xamarin.com/show_bug.cgi?id=42082):
    "Ionic.Zip.ZipException ... \_\_AndroidLibraryProjects\_\_.zip is not a
    valid zip file ---> System.TimeZoneNotFoundException" when building Android
    projects in certain Windows time zones.  **Temporary workaround**: Change
    the Window time zone.  For example the _Central Time (US & Canada)_ time
    zone does not hit this error.

<a name="Bug_Fixes_6.1.1"/>
## Bug Fixes

* [41665](https://bugzilla.xamarin.com/show_bug.cgi?id=41665):
    "`System.ComponentModel.INotifyPropertyChanged` is defined in an assembly
    that is not referenced. You must add a reference to assembly `System.ObjectModel`"
    for Android projects that reference PCLs that use `INotifyPropertyChanged`

<a name="integrated-mono-6.0.1" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.4](http://www.mono-project.com/docs/about-mono/releases/4.4.0/)
[commit 9bdc135c](https://github.com/mono/mono/commit/9bdc135cdf856ac9171a8a7e441a0775b1df51e3).

* [41775](https://bugzilla.xamarin.com/show_bug.cgi?id=41775):
    Zip version needed to extract not correct in System.IO.Compression
* [41782](https://bugzilla.xamarin.com/show_bug.cgi?id=41782):
    [Cycle 7] &quot;System.Net.WebException: Error: NameResolutionFailure&quot; when attempting web requests with certain raw IP addresses
* [41874](https://bugzilla.xamarin.com/show_bug.cgi?id=41874):
    Reflection throws `AmbiguousMatchException` when calling `GetProperty()` on a class that inherits from a generic base class.


<!--
  JONP: 6.1.0 last updated from commit monodroid/cycle7/4e275588a9819661d9e04b3d3b96db8fa6996816
-->

<a name="0"/>
<a name="Xamarin.Android_6.1.0"/>
# Xamarin.Android 6.1

<a name="new-features-6.1" />
## New Features

* [New Java Invocation Architecture](#Java_Interop).
* Visual Studio Community Edition is now supported.
* All editions may now make use of these features which were previously restricted:

    * Command-line builds, including headless builds
    * All types and assemblies may now be used, including System.Data.SqlClient
    * P/Invoke
    * Java interop, including .jar binding assemblies
    * No more application size limits

* Removed the splash screen which was shown at launch for apps built with Trial edition.
* [New Java Invocation Architecture](#Java_Interop).
* [`Mono.Data.Sqlite.dll` bundles SQLite](#mono-data-sqlite)
* [Improved Build Behavior](#Build_Behavior)
* [Improved Java Interface Versioning Support](#Java_Interface_Versioning)
* [Application Subclassing](#Application_Subclassing)
* [Native `HttpClientHandler`](#AndroidHttpClientHandler)
* [Enable soft breakpoints by default](#Soft_Breakpoints)
* [Improved LG Device Debugging Support](#LG_Debugging)
* Enable stack protector and related security features within `libmonodroid.so` and
    `libmonosgen-2.0.so`.


<a name="Java_Interop" />
### New Java Invocation Architecture

A new Java Invocation architecture has been developed that vastly improves the
Mono to Java bridge. It significantly reduces the amount of glue code
necessary, allowing the size of Mono.Android.dll for API-23 to be reduced by
nearly 2MB compared to previous releases.

This new architecture also permits additional caching opportunities, speeding
up "base" method invocation within method overrides to be take of 37% as long
as Xamarin.Android 6.0 and speeding up constructor execution times.

We have also fine tuned the bridge to reduce the number of round trips from
managed code to JNI when an exception may be thrown: instead of performing
two JNI calls --  one to invoke, one to retrieve a possible exception --
we perform a single call.  This will improve performance for applications
that must use chatty APIs.


<a name="mono-data-sqlite" />
### `Mono.Data.Sqlite.dll` and `libsqlite.so`

In previous releases, `Mono.Data.Sqlite.dll` would P/Invoke into the
OS-provided `/system/lib/libsqlite.so` native library.
[Starting with Android N][ndk], Android will no longer permit this behavior,
so previous versions of `Mono.Data.Sqlite.dll` will throw a
`DllNotFoundException` when attempting to use SQLite functionality
when executing on Android N.

`Mono.Data.Sqlite.dll` will now bundle and distribute a custom SQLite,
named `libsqlite3_xamarin.so`, which will automatically be bundled into
the `app.apk` when `Mono.Data.Sqlite.dll` is referenced.

*Existing users of `Mono.Data.Sqlite.dll` need only rebuild their app.*

*However*, if *any other assembly* is P/Invoking `sqlite`, `sqlite3`,
or variations thereof, these SQLite uses will *not* be updated.
Those other assemblies will need to be updated.
For example,
[SQLitePCL.raw 0.6.0](https://www.nuget.org/packages/SQLitePCL.raw_basic/0.6.0)
*will not* work on Android N, while the updated
[SQLitePCL.raw 0.8.6](https://www.nuget.org/packages/SQLitePCL.raw_basic/)
has been updated to distribute its own copy of SQLite, and *will* work
on Android N.


<a name="Build_Behavior" />
### Improved Build Behavior

The $(TargetFrameworkVersion) MSBuild Property is now checked for consistency
between Application projects and Library projects. If any Library project
`$(TargetFrameworkVersion)` exceeds the Application's value, then a warning
is printed and the maximum `$(TargetFrameworkVersion)` of all referenced
assemblies and the application project is used for the resulting application.

Assemblies may refer to external resources which are cached in the
`LocalApplicationData` folder instead of within the project structure.
Previously, this caching was performed only for `Xamarin` assemblies.
Starting in Xamarin.Android 6.1, this cachine is done for all assemblies,
which can reduce the number of resources which may need to be downloaded.

In addition a new SHA hash support has been added to allow the external
resource files to be checked for integrity before being extracted. Future
releases of Xamarin Nugets/Componets will support this new feature.


<a name="Soft_Breakpoints" />
### Enable soft breakpoints by default

Mono has two different ways to support
[single-step debugging][mono-single-stepping]:

[mono-single-stepping]: http://www.mono-project.com/docs/advanced/runtime/docs/soft-debugger/#single-stepping

1. "Hard" single stepping by relying on the SIGSEGV signal.
2. "Soft" single stepping by using a software mechanism.

Previous versions of Xamarin.Android relied on the SIGSEGV model, which
was determined to cause process aborts in a variety of scenarios
([27455](https://bugzilla.xamarin.com/show_bug.cgi?id=27455),
[35739](https://bugzilla.xamarin.com/show_bug.cgi?id=35739),
[35798](https://bugzilla.xamarin.com/show_bug.cgi?id=35798)).

To fix these scenarios, Xamarin.Android 6.1 changes the default single-stepping
mechanism to "soft" breakpoints. This should fix debugging on ART.

However, soft breakpoints are a relatively recent addition to mono and have
not received as much testing as "hard" breakpoints.

The new `debug.mono.soft_breakpoints` system property can be used to control
whether hard or soft breakpoints are used. If this system property has the
value `0`, then hard breakpoints will be used:

    # Use the SIGSEGV-based single-step mechanism
    adb shell setprop debug.mono.soft_breakpoints 0

*Any other value* will enable use of soft breakpoints. Using soft breakpoints
is now the default.


<a name="Java_Interface_Versioning" />
### Improved Java Interface Versioning Support

`Mono.Android.dll` assembly exposes Java interfaces as they existed in a
corresponding Android API level, and Java interfaces can change between API
levels, for example the
[android.database.Cursor](http://developer.android.com/reference/android/database/Cursor.html)
interface. As such, bound interfaces are *unstable*. Normally this isn’t an
issue, but if you have a class library which implements such an interface
from e.g. `$(TargetFrameworkVersion)` of v2.3, while the Application project
builds with `$(TargetFrameworkVersion)` of v6.0, the class library type could
not be loaded in previous versions. Starting with Xamarin.Android 6.1, all
classes will be checked to ensure they fully implement their Java interfaces,
and if they don’t then the missing members will be generated to throw an
`AbstractMethodError`.


<a name="Application_Subclassing" />
### Application Subclassing

It is now possible to inherit from arbitrary `android.app.Application`
subclasses which do not allow overriding `Application.onCreate()`, such
as the Microsoft Intune `MAMApplication` type, by using the new
[`$(AndroidApplicationJavaClass)`](/guides/android/under_the_hood/build_process/#AndroidApplicationJavaClass)
MSBuild property.


<a name="AndroidHttpClientHandler" />
### Native `HttpClientHandler`

Xamarin.Android 6.1 introduces a new `Xamarin.Android.Net.AndroidClientHandler`
type which can be used with
[`System.Net.Http.HttpClient`](https://msdn.microsoft.com/en-us/library/system.net.http.httpclient(v=vs.118).aspx):

```
var client = new HttpClient (
        new Xamarin.Android.Net.AndroidClientHandler ());
```

The new `XA_HTTP_CLIENT_HANDLER_TYPE` environment variable allows specifying
the default `HttpMessageHandler` type that `HttpClient` will use when the
[default `HttpClient` constructor is used](https://msdn.microsoft.com/en-us/library/hh138077(v=vs.118).aspx).
`XA_HTTP_CLIENT_HANDLER_TYPE` is an *Assembly Qualified Type Name*.
Environment variables can be specified by using the
[`@(AndroidEnvironment)`][env] build action:

[env]: /guides/android/advanced_topics/environment/

```
XA_HTTP_CLIENT_HANDLER_TYPE=Xamarin.Android.Net.AndroidClientHandler
```

By default, `XA_HTTP_CLIENT_HANDLER_TYPE` is not set, and the default
`HttpClient` constructor will construct an [`HttpClientHandler`][handler].

[handler]: https://msdn.microsoft.com/en-us/library/system.net.http.httpclienthandler(v=vs.118).aspx

`AndroidClientHandler` uses the native
[java.net.URLConnection](http://developer.android.com/reference/java/net/URLConnection.html)
type for network access instead of Mono’s normal networking stack. This allows
`HttpClient` to use any network protocols and encryption protocols that Android
knows how to handle, such as TLS 1.2.

*Note*: TLS 1.2 support requires that the underlying Android device support
TLS 1.2.

Android 5.0 and later support TLS 1.2.


<a name="LG_Debugging" />
### Improved LG Device Debugging Support

Certain LG devices do not support `adb shell setprop`, which is used for
debugging. Xamarin.Android 6.1 introduces a new mechanism which allows
debugging on these devices.


<a name="experimental-features" />
## Experimental Features

Xamarin.Android 6.1 introduces several experimental features:

* [Improved Fast Deployment](#Fast_Deployment)
* [File name and line number information in release builds](#Release_Stack_Traces)

<a name="Fast_Deployment" />
### Improved Fast Deployment

[Fast Deployment](/guides/android/under_the_hood/build_process/#Fast_Deployment)
is a way to avoid rebuilding and redeploying Android Packages (`.apk` files)
when assemblies have changed in a way that doesn’t require changing the generated
[Android Callable Wrappers](/guides/android/advanced_topics/java_integration_overview/android_callable_wrappers/)
or altered any included Android Assets and Resources.

Xamarin.Android 6.1 will optionally allow Android Assets, Resources, and
compiled Java libraries to particpate in fast deployment as well, further
reducing the number of situations in which a possibly slow `.apk` rebuild
and redeploy will be required.

This new behavior is *disabled* by default, but may be enabled by setting the
[`$(AndroidFastDeploymentType)`](/guides/android/under_the_hood/build_process/#AndroidFastDeploymentType)
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


<a name="Release_Stack_Traces" />
### File name and line number information in release builds

The Holy Grail!

File name and line number information in Release builds is supported through
the build-time generation of `.mdb` files (and `.msym` files for AOT builds). The generation of
the sequence points is controlled by the new `$(AndroidManagedSymbols)` MSBuild
property, which must be set to 'true' to enable generation:

```
<AndroidManagedSymbols>true</AndroidManagedSymbols>
```

You also need to set `$(DebugSymbols)` to True and `$(DebugType)` to `PdbOnly`
for your release build. This will ensure that your assemblies do NOT contain
debug information but that the required data is stored in the `.mdb`/`.msym` files.

When enabled, a new `$(OutputPath)\@PACKAGE_NAME@.msym` directory will be
created which contains all information required to correlate IL offset
information (found in stack traces) back to file name and line number
information through the use of the new mono-symbolicate tool.

Next, grab a crash log which an unhandled exception

```
adb logcat -d > errors.txt
```

Finally, use `mono-symbolicate` to convert the errors to contain file and
line numbers:

```
mono-symbolicate path-to-dll-in-.msym-directory path-to-errors.txt
```

`mono-symbolicate` can be found at:

* **OS X**: `/Library/Frameworks/Xamarin.Android.framework/Commands/mono-symbolicate`
* **Windows**: `%ProgramFiles(x86)%\MSBuild\Xamarin\Android\mono-symbolicate.exe`

For example, given an `errors.txt` with the contents:

```
I/MonoDroid( 1545): System.Exception: wow it broke
I/MonoDroid( 1545):   at CrashApp.MainActivity+<OnCreate>c__AnonStorey0.<>m__0 (System.Object , System.EventArgs ) [0x00030] in <filename unknown>:0
I/MonoDroid( 1545):   at Android.Views.View+IOnClickListenerImplementor.OnClick (Android.Views.View v) [0x00014] in <filename unknown>:0
I/MonoDroid( 1545):   at Android.Views.View+IOnClickListenerInvoker.n_OnClick_Landroid_view_View_ (IntPtr jnienv, IntPtr native__this, IntPtr native_v) [0x00011] in <filename unknown>:0
I/MonoDroid( 1545):   at (wrapper dynamic-method) System.Object:5616285d-461b-4005-a31b-d4637a8cdddc (intptr,intptr,intptr)
```

`mono-symbolicate` will translate the above into:

```
I/MonoDroid( 1545): System.Exception: wow it broke
I/MonoDroid( 1545):   at CrashApp.MainActivity+<OnCreate>c__AnonStorey0.<>m__0 (System.Object , System.EventArgs ) [0x00030] in /Users/dean/Projects/CrashApp/CrashApp/MainActivity.cs:30
I/MonoDroid( 1545):   at Android.Views.View+IOnClickListenerImplementor.OnClick (Android.Views.View v) [0x00014] in /Users/dean/Documents/Sandbox/Xamarin/dellismonodroid/src/Mono.Android/platforms/android-19/src/generated/Android.Webkit.WebBackForwardList.cs:68
I/MonoDroid( 1545):   at Android.Views.View+IOnClickListenerInvoker.n_OnClick_Landroid_view_View_ (IntPtr jnienv, IntPtr native__this, IntPtr native_v) [0x00011] in /Users/dean/Documents/Sandbox/Xamarin/dellismonodroid/src/Mono.Android/platforms/android-19/src/generated/Android.Webkit.WebBackForwardList.cs:23
I/MonoDroid( 1545):   at (wrapper dynamic-method) System.Object:5616285d-461b-4005-a31b-d4637a8cdddc (intptr,intptr,intptr)
```

Notice that the `<filename unknown>:0` messages were translated into
appropriate filename and line number information.

## Known Issues

* [AOT and AOT+LLVM support][aot-5.1] has always been experimental.
    It has been discovered that AOT+LLVM support hasn't worked since at least
    Xamarin.Android 6.0; the AOT+LLVM compiler executed but didn't do anything.
    During QA, it was determined that in attempting to fix the
    "AOT+LLVM didn't do anything" issue, the AOT+LLVM compiler instead crashed.

    <!--
      https://bugzilla.xamarin.com/show_bug.cgi?id=39270#c6
      https://bugzilla.xamarin.com/show_bug.cgi?id=41114
      -->

    Consequently, AOT+LLVM support has been *disabled* in the Xamarin.Android 6.1
release. It will be re-enabled in a future release.

[aot-5.1]: /releases/android/xamarin.android_5/xamarin.android_5.1/#AOT_Support

* [41665](https://bugzilla.xamarin.com/show_bug.cgi?id=41665):
    "'System.ComponentModel.INotifyPropertyChanged' is defined in an assembly
    that is not referenced. You must add a reference to assembly
    'System.ObjectModel" in _VS 2013 only_ when building Android projects that
    reference PCLs that use `INotifyPropertyChanged`.  This issue also causes
    similar error messages for other facade assemblies.  As discussed in the the
    bug report, the upcoming fix for this issue will set
    `$(DependsOnSystemRuntime)` to `true` automatically.  **Temporary
    workaround**: Until the fix is published, you can try applying the fix by
    hand if you like by adding the following line in the top `<PropertyGroup>`
    element in your Android app project `.csproj` file (with a caution that the
    normal MSBuild property evaluation rules apply, so evaluation of later
    MSBuild settings in your project could in theory override this setting):

        <DependsOnSystemRuntime Condition=" '$(DependsOnSystemRuntime)' == '' ">true</DependsOnSystemRuntime>

* [41782](https://bugzilla.xamarin.com/show_bug.cgi?id=41782):
    "System.Net.WebException: Error: NameResolutionFailure" when attempting web
    requests with certain raw IP addresses.  This is a bug in Mono, so it
    affects all platforms iOS, Android, and Mac.  **Partial temporary
    workaround**: If possible, use domain names rather than raw IP addresses
    for the web requests.

<a name="Bug_Fixes"/>
## Bug Fixes

* [14255](https://bugzilla.xamarin.com/show_bug.cgi?id=14255):
    App using Component with bundled resources fails to compile on Windows / VS
* [27455](https://bugzilla.xamarin.com/show_bug.cgi?id=27455),
    [35739](https://bugzilla.xamarin.com/show_bug.cgi?id=35739),
    [35798](https://bugzilla.xamarin.com/show_bug.cgi?id=35798):
    Process would abort from an ART message: `Check failed: !initialized_`.
* [28663](https://bugzilla.xamarin.com/show_bug.cgi?id=28663):
    Gdb.env contains the wrong file name for `app_process` when failing to pull `app_process`
* [31855](https://bugzilla.xamarin.com/show_bug.cgi?id=31855):
     Cannot debug with LG G4
* [32126](https://bugzilla.xamarin.com/show_bug.cgi?id=32126):
    Xamarin.Android call performance is 4 times slower on inherited views
* [33514](https://bugzilla.xamarin.com/show_bug.cgi?id=33514):
    `IntentFilterAttribute` does not allow specifying the equivalent of multiple `data` attributes
* [33967](https://bugzilla.xamarin.com/show_bug.cgi?id=33967):
    [Android] Resource files in obj directory are not removed when deleted from Project
* [34076](https://bugzilla.xamarin.com/show_bug.cgi?id=34076):
    Android.Runtime.JavaCollection&lt;T&gt;.CopyTo in Mono.Android.dll lacking null check
* [34139](https://bugzilla.xamarin.com/show_bug.cgi?id=34139):
    GZipStream (DeflateStreamNative) native exception after Flush() with no buffer data: Internal error (no progress possible) Flush
* [34391](https://bugzilla.xamarin.com/show_bug.cgi?id=34391):
    System.DllNotFoundException: sqlcipher
* [34776](https://bugzilla.xamarin.com/show_bug.cgi?id=34776):
    DateUtils.FormatSameDayTime expecting different values that the original Java version
* [34825](https://bugzilla.xamarin.com/show_bug.cgi?id=34825):
    NullPointerException when transferring byte array over IPC using AIDL
* [35397](https://bugzilla.xamarin.com/show_bug.cgi?id=35397):
    Make the zip download of Android libraries more reliable
* [35471](https://bugzilla.xamarin.com/show_bug.cgi?id=35471):
    JavaCast&lt;T&gt;() doesn't properly handle for ACW types.
* [35491](https://bugzilla.xamarin.com/show_bug.cgi?id=35491):
    Built APK crash below 5.0 - multidex
* [35595](https://bugzilla.xamarin.com/show_bug.cgi?id=35595):
    Missing the `autoVerify` property for intent filters.
* [35613](https://bugzilla.xamarin.com/show_bug.cgi?id=35613):
    error MSB4018: System.NotSupportedException: The given path's format is not supported.
* [35742](https://bugzilla.xamarin.com/show_bug.cgi?id=35742):
    Android TV App Banner cannot be set with tools
* [35744](https://bugzilla.xamarin.com/show_bug.cgi?id=35744):
    Android Support v4 throws Null Reference Exception when set as a ReferenceJar/EmbeddedReferenceJar
* [35775](https://bugzilla.xamarin.com/show_bug.cgi?id=35775):
    Android.Media.ToneGenerator does not allow for volume int
* [35896](https://bugzilla.xamarin.com/show_bug.cgi?id=35896):
    AndroidResgen: Warning while updating Resource XML &quot;.xml.tmp&quot; The filename, directory name, or volume label syntax is incorrect.
* [36036](https://bugzilla.xamarin.com/show_bug.cgi?id=36036):
    error MSB4018: The &quot;GenerateJavaStubs&quot; task failed unexpectedly, error MSB4018: System.InvalidOperationException: Sequence contains no matching element
* [36183](https://bugzilla.xamarin.com/show_bug.cgi?id=36183):
    Since upgrading to Xamarin Android 6 get error error MSB3733: Input file &quot;obj\Android\Debug\android\AndroidManifest.xml&quot; cannot be opened
* [36235](https://bugzilla.xamarin.com/show_bug.cgi?id=36235):
    Strange mdb filenames when using Visual Studio (Android/iOS)
* [36237](https://bugzilla.xamarin.com/show_bug.cgi?id=36237):
    If multiple mdb are generated at same time (i.e. two android executables), it results in IOException
* [36436](https://bugzilla.xamarin.com/show_bug.cgi?id=36436):
    XslCompiledTransform causes hang during execution
* [36514](https://bugzilla.xamarin.com/show_bug.cgi?id=36514):
    [VS only] The &quot;fast deployment&quot; process does not automatically update the class library assemblies on device after an upgrade from XA 5.1 to XA 6.0, leading to &quot;Assertion at ... class.c:5078, condition `class' not met&quot;
* [37019](https://bugzilla.xamarin.com/show_bug.cgi?id=37019):
    Exception while loading assemblies: Xamarin.Android.XamarinAndroidException: error XA0009
* [37331](https://bugzilla.xamarin.com/show_bug.cgi?id=37331):
    Edited AXML resources in a class library are not recompiled unless you Clean
* [37422](https://bugzilla.xamarin.com/show_bug.cgi?id=37422):
    Release Build Still Creates `.__override__` Directory
* [38529](https://bugzilla.xamarin.com/show_bug.cgi?id=38529):
    UpdateIdValues for the main assembly is called a lot of times
* [38726](https://bugzilla.xamarin.com/show_bug.cgi?id=38726):
    Error executing task LinkAssemblies: Object reference not set to an instance of an object
* [40749](https://bugzilla.xamarin.com/show_bug.cgi?id=40749):
    Translation with `.resx` files is broken in Xamarin.Android 6.1.0-48.
* [40982](https://bugzilla.xamarin.com/show_bug.cgi?id=40982):
    VS hangs/freezes when opening solutions containing Android Bindings
    Libraries that reference other libraries, during
    `GetAdditionalResourcesFromAssemblies.Execute()`
* [40976](https://bugzilla.xamarin.com/show_bug.cgi?id=40976):
    Custom Application subclass does not extend `MultiDexApplication` when
    MultiDex is enabled.


<a name="breaking-changes" />
## Breaking Changes

Projects which directly reference design time facade assemblies
(which already exist in `MonoAndroid\v1.0\Facades`) will now throw a
compilation error instead of only a warning.
([Bug 35582](https://bugzilla.xamarin.com/show_bug.cgi?id=35582))

Possible compilation errors when projects use a `Xamarin.` namespace,
because of conflict with the new `Xamarin.Android.Net` namespace.

`android.app.Instrumentation` subclasses used for app launching or
headless execution may not behave as expected when running on API 10 devices.
A workaround will be to change the target framework for any such project to v2.3.


<a name="integrated-mono" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.4](http://www.mono-project.com/docs/about-mono/releases/4.4.0/)
[commit f3253a0b](https://github.com/mono/mono/commit/f3253a0ba5991411dd6def16c2374cf75816664b).

* [2033](https://bugzilla.xamarin.com/show_bug.cgi?id=2033):
    UnicastAddress.IPv4Mask throws NotImplementedException on Mono 2.10 running on open-embedded Linux
* [4230](https://bugzilla.xamarin.com/show_bug.cgi?id=4230):
    DataContractJsonSerializer mishandles deserialization of null arrays
* [4938](https://bugzilla.xamarin.com/show_bug.cgi?id=4938):
    SignedXml reporting Malformed reference object where referenced attribute name is lowercase id, rather than Id
* [10205](https://bugzilla.xamarin.com/show_bug.cgi?id=10205):
    System.InvalidOperationException in FileSystemWatcher
* [10268](https://bugzilla.xamarin.com/show_bug.cgi?id=10268):
    Linker issue with horizontallistview project in release mode
* [12681](https://bugzilla.xamarin.com/show_bug.cgi?id=12681):
    Task.Wait() blocks forever, and I don't know why.
* [13538](https://bugzilla.xamarin.com/show_bug.cgi?id=13538):
    Extraneous lines in Application Output for `Debug.WriteLine()`.
* [13909](https://bugzilla.xamarin.com/show_bug.cgi?id=13909):
    RouteTable.Routes.Clear() doesn't really clear
* [15028](https://bugzilla.xamarin.com/show_bug.cgi?id=15028):
    DataMember - EmitDefaultValue is not working.
* [15153](https://bugzilla.xamarin.com/show_bug.cgi?id=15153):
    System.ServiceModel.NetTcpBinding properties are not pre-initialized while they are in .Net causing interoperability problems
* [19391](https://bugzilla.xamarin.com/show_bug.cgi?id=19391):
    `[Preserve(AllMembers=true)]` not working when another attribute,
    `[DataContract]` is after it.
* [20186](https://bugzilla.xamarin.com/show_bug.cgi?id=20186):
    Another AOT bug
* [22307](https://bugzilla.xamarin.com/show_bug.cgi?id=22307):
    Intermittent IndexOutOfRangeException when opening/closing connections rapidly
* [23617](https://bugzilla.xamarin.com/show_bug.cgi?id=23617):
    Can't build in Release mode: Error executing task GenerateJavaStubs: Could not load assembly 'Xamarin.Android.Support.v4
* [24958](https://bugzilla.xamarin.com/show_bug.cgi?id=24958):
    TimeZoneInfo.Local.Id and TimeZoneInfo.Local.DisplayName return &quot;Local&quot;
* [25480](https://bugzilla.xamarin.com/show_bug.cgi?id=25480):
    OutputPath property is not set for this project
* [27303](https://bugzilla.xamarin.com/show_bug.cgi?id=27303):
    NullReferenceException with ARMv7
* [27864](https://bugzilla.xamarin.com/show_bug.cgi?id=27864):
    [iOS 8.2] SQLite.net queries fail in iOS 8.2 if they contain UNION or COLLATE
* [28693](https://bugzilla.xamarin.com/show_bug.cgi?id=28693):
    IOException: kqueue() FileSystemWatcher has reached the maximum nunmber of files to watch.
* [29864](https://bugzilla.xamarin.com/show_bug.cgi?id=29864):
    public Uri(Uri baseUri, Uri relativeUri) strips . from path
* [30018](https://bugzilla.xamarin.com/show_bug.cgi?id=30018):
    Use &quot;Dns.GetHostEntry&quot; or &quot;Dns.GetHostByName&quot;,sometime throw error &quot;Cannot handle address family xxxxx&quot;
* [30023](https://bugzilla.xamarin.com/show_bug.cgi?id=30023):
    Using default constructor in watch window does not work
* [30360](https://bugzilla.xamarin.com/show_bug.cgi?id=30360):
    Error in handling of /etc/localtime file to retrieve time zone on Linux
* [30479](https://bugzilla.xamarin.com/show_bug.cgi?id=30479):
    Sgen counter for promoted not been reset across minor collections
* [30561](https://bugzilla.xamarin.com/show_bug.cgi?id=30561):
    Setting HttpContent in System.Net.Http does not set ContentLength header.
* [30594](https://bugzilla.xamarin.com/show_bug.cgi?id=30594):
    `* Assertion at sgen-alloc.c:558, condition `tlab_next_addr_offset != -1' not met`
* [31172](https://bugzilla.xamarin.com/show_bug.cgi?id=31172):
    Uri parsing exceptions when username or password has space in it
* [31209](https://bugzilla.xamarin.com/show_bug.cgi?id=31209):
    HttpConnection locks up if first line of request is empty
* [31432](https://bugzilla.xamarin.com/show_bug.cgi?id=31432):
    TimeZoneNotFoundException
* [31451](https://bugzilla.xamarin.com/show_bug.cgi?id=31451):
    mono_trace_set_printerr_handler calls g_set_print_handler instead of g_set_printerr_handler
* [31557](https://bugzilla.xamarin.com/show_bug.cgi?id=31557):
    Sockets with ReuseAddress does not seem to be working as expected
* [31875](https://bugzilla.xamarin.com/show_bug.cgi?id=31875):
    Android build fails
* [31877](https://bugzilla.xamarin.com/show_bug.cgi?id=31877):
    SendChunked - &quot;Method must be implemented&quot;
* [31900](https://bugzilla.xamarin.com/show_bug.cgi?id=31900):
    char.ToUpperInvariant fails to convert some characters to upper case and returns different values than in .NET
* [31932](https://bugzilla.xamarin.com/show_bug.cgi?id=31932):
    Regression: Stack Overflow with native P/Invoke Callback
* [31996](https://bugzilla.xamarin.com/show_bug.cgi?id=31996):
    AOT compiler fails if path to project has a comma
* [32137](https://bugzilla.xamarin.com/show_bug.cgi?id=32137):
    System.Text.Encoding.UTF8.EncodingName not the returning human-readable description of the current encoding
* [32539](https://bugzilla.xamarin.com/show_bug.cgi?id=32539):
    Process.ProcessName value fetched using Process.GetProcesses () is trimmed to 15 characters
* [32561](https://bugzilla.xamarin.com/show_bug.cgi?id=32561):
    Could not load file or assembly Microsoft.Build.Utilities
* [32579](https://bugzilla.xamarin.com/show_bug.cgi?id=32579):
    System.Diagnostics.Process.MainModule.FileName does not return full path of the executable and returns 15 chars trimmed value which is same as Process.ProcessName
* [32591](https://bugzilla.xamarin.com/show_bug.cgi?id=32591):
    AssemblyName .ctor doesn't accept quoted PublicKeyToken in the assembly name string
* [32609](https://bugzilla.xamarin.com/show_bug.cgi?id=32609):
    PropertyInfo.CanWrite behavior difference from MS.NET
* [32685](https://bugzilla.xamarin.com/show_bug.cgi?id=32685):
    NRE in ServicePoint.CheckAvaliableForRecycling
* [32712](https://bugzilla.xamarin.com/show_bug.cgi?id=32712):
    Incorrect compile error CS4016 when for async function that returns Task&lt;Task&gt;
* [32725](https://bugzilla.xamarin.com/show_bug.cgi?id=32725):
    Creating a new System.IO.Compression.ZipArchive fails on mono with SharpCompress.Common.ArchiveException
* [32815](https://bugzilla.xamarin.com/show_bug.cgi?id=32815):
    PropertyInfo.Module throws System.NotImplementedException
* [32886](https://bugzilla.xamarin.com/show_bug.cgi?id=32886):
    [Mono 3.12] Some WCF methods that do _not_ use &quot;ref&quot; parameters fail with &quot;InvalidOperationException&quot; during &quot;ClientRuntimeChannel.EndProcess&quot; when called via a ChannelFactory channel
* [32894](https://bugzilla.xamarin.com/show_bug.cgi?id=32894):
    Using-alias-directives throws NullReferenceException (Mono.CSharp)
* [32905](https://bugzilla.xamarin.com/show_bug.cgi?id=32905):
    System.IO.IOException : Write fault on path ... during ProcessTest.DisposeWithDisposedStreams
* [32907](https://bugzilla.xamarin.com/show_bug.cgi?id=32907):
    Accessing fields of `Random` object from IL code leads to mono crash.
* [32918](https://bugzilla.xamarin.com/show_bug.cgi?id=32918):
    StackTrace() missing original exception - ExceptionDispatchInfo
* [32931](https://bugzilla.xamarin.com/show_bug.cgi?id=32931):
    NullReferenceException in KeyValuePair.get_Key when using generic method and Linq
* [32947](https://bugzilla.xamarin.com/show_bug.cgi?id=32947):
    App just hangs on iOS9 device with iOS9 SDK
* [32955](https://bugzilla.xamarin.com/show_bug.cgi?id=32955):
    Random crash at aot-runtime.c:3144
* [33066](https://bugzilla.xamarin.com/show_bug.cgi?id=33066):
    Watch evaluations different in XS than VS
* [33080](https://bugzilla.xamarin.com/show_bug.cgi?id=33080):
    JIT error only on ARMV7
* [33142](https://bugzilla.xamarin.com/show_bug.cgi?id=33142):
    new float() without assignment raises CS0201 error
* [33218](https://bugzilla.xamarin.com/show_bug.cgi?id=33218):
    Action ReflectedType differs from Delegate ReflectedType
* [33324](https://bugzilla.xamarin.com/show_bug.cgi?id=33324):
    Casting List to IList causes argument exception on device build in Add method.
* [33400](https://bugzilla.xamarin.com/show_bug.cgi?id=33400):
    Setting Language to zh-Hant on iOS does not set UICulture to zh-TW or zh-Hant
* [33471](https://bugzilla.xamarin.com/show_bug.cgi?id=33471):
    onoTests.System.TimeZoneInfoTest+ConvertTimeTests.ConvertFromToLocal fails when machine is in UTC
* [33487](https://bugzilla.xamarin.com/show_bug.cgi?id=33487):
    'CS1591' is not a valid warning number (CS1904)
* [33550](https://bugzilla.xamarin.com/show_bug.cgi?id=33550):
    Portable PDB doesn't to work when Assembly.Load(byte[], byte[]) called
* [33551](https://bugzilla.xamarin.com/show_bug.cgi?id=33551):
    System.Net.SmtpClient uses an invalid HELO name
* [33553](https://bugzilla.xamarin.com/show_bug.cgi?id=33553):
    `System.IO.Compression.ZipArchive` produces bad archive files
* [33573](https://bugzilla.xamarin.com/show_bug.cgi?id=33573):
    Function call in fixed get called 3 times.
* [33591](https://bugzilla.xamarin.com/show_bug.cgi?id=33591):
    AOT compilation fails with condition `field-&gt;type-&gt;attrs &amp; FIELD_ATTRIBUTE_HAS_DEFAULT' not met
* [33600](https://bugzilla.xamarin.com/show_bug.cgi?id=33600):
    Auto properties broken in Mono 4.2.0
* [33809](https://bugzilla.xamarin.com/show_bug.cgi?id=33809):
    Exception with SignalR 2.2 and Mono 4.2.0
* [33952](https://bugzilla.xamarin.com/show_bug.cgi?id=33952):
    Debugger.Break() causes app to crash if Debugger is not attached,
* [34044](https://bugzilla.xamarin.com/show_bug.cgi?id=34044):
    HttpClient: any custom Host header is not used in requests
* [34047](https://bugzilla.xamarin.com/show_bug.cgi?id=34047):
    System.Globalization.CultureInfo.GetCultureInfo(&quot;es&quot;) returns incorrect NumberFormatInfo.NumberGroupSeparator
* [34147](https://bugzilla.xamarin.com/show_bug.cgi?id=34147):
    Serious AOT bug
* [34382](https://bugzilla.xamarin.com/show_bug.cgi?id=34382):
    Marshal.AllocHGlobal out of memory exception with 64-bit ptr
* [34409](https://bugzilla.xamarin.com/show_bug.cgi?id=34409):
    XML document generation
* [34604](https://bugzilla.xamarin.com/show_bug.cgi?id=34604):
    Compiler Crash in Mono.CSharp.CallEmitter.EmitPredefined with NRE
* [34750](https://bugzilla.xamarin.com/show_bug.cgi?id=34750):
    Debugger crash very often - debugger-agent.c:2587, condition `res' not met
* [34926](https://bugzilla.xamarin.com/show_bug.cgi?id=34926):
    AOT issue with await Task&lt;bool&gt; on Visual Studio 2015
* [35429](https://bugzilla.xamarin.com/show_bug.cgi?id=35429):
    Assertion at socket-io.c:2757 when cleanly exiting XS
* [35447](https://bugzilla.xamarin.com/show_bug.cgi?id=35447):
    Android Debugger Crashes on watch condition accessing &quot;Data&quot;
* [35545](https://bugzilla.xamarin.com/show_bug.cgi?id=35545):
    Mono cannot marshal a parameter that is a function pointer which takes a function pointer as a parameter
* [35579](https://bugzilla.xamarin.com/show_bug.cgi?id=35579):
    Recent xbuild changes result in breakages to F# compiler tools
* [35604](https://bugzilla.xamarin.com/show_bug.cgi?id=35604):
    [csharp] Bad using statements break all future REPL evaluations
* [35655](https://bugzilla.xamarin.com/show_bug.cgi?id=35655):
    Crash on simple try-catch with Mono.Posix
* [35674](https://bugzilla.xamarin.com/show_bug.cgi?id=35674):
    Silent discarding of code on syntax error in anonymous delegate
* [35828](https://bugzilla.xamarin.com/show_bug.cgi?id=35828):
    Thread.CurrentThread doesn't return correct object in appdomain
* [35844](https://bugzilla.xamarin.com/show_bug.cgi?id=35844):
    276824dd28c4b1 breaks Nexus5 on TestCloud
* [35855](https://bugzilla.xamarin.com/show_bug.cgi?id=35855):
    Attempting to JIT compile method '(wrapper unknown) System.Collections.ObjectModel.ObservableCollection`1&lt;tryfsharpforms.DoubleDoubleDataPoint&gt;[]:Get (int)' while running with --aot-only.
* [35857](https://bugzilla.xamarin.com/show_bug.cgi?id=35857):
    [Mono 4.2] NullReferenceException in SqlDataReader.GetValues()
* [35876](https://bugzilla.xamarin.com/show_bug.cgi?id=35876):
    Incorrect return of DateTime.ToUniversalTime method for DateTime.MaxValue.
* [35936](https://bugzilla.xamarin.com/show_bug.cgi?id=35936):
    Itermittent crash/hang with MonoTests.Mono.Unix.UnixSignalTest.TestWaitAny
* [35980](https://bugzilla.xamarin.com/show_bug.cgi?id=35980):
    CSharpCodeCompiler.CompileXYZ false positive error when warning is 'X hides inherited member'
* [36000](https://bugzilla.xamarin.com/show_bug.cgi?id=36000):
    Dictionary with IEqualityComparer is leaking in iOS 9.2.1.51 / Mono 4.2.1
* [36003](https://bugzilla.xamarin.com/show_bug.cgi?id=36003):
    Invalid DateTime format for Finnish and DateTime parser not supporting same separator for date and time
* [36052](https://bugzilla.xamarin.com/show_bug.cgi?id=36052):
    Using stackalloc zeros out the size variable when passed to another function
* [36080](https://bugzilla.xamarin.com/show_bug.cgi?id=36080):
    `System.ServiceModel.EndpointAddress10` does not have a static method `GetSchema` that takes a parameter of type `System.Xml.Schema.XmlSchemaSet` when using the Xamarin Mobile profile with some WCF client apps
* [36095](https://bugzilla.xamarin.com/show_bug.cgi?id=36095):
    Uri is longer than the maximum 32766 characters
* [36100](https://bugzilla.xamarin.com/show_bug.cgi?id=36100):
    DataContractSerializer broke in XI 9.2.1.51 STABLE
* [36128](https://bugzilla.xamarin.com/show_bug.cgi?id=36128):
    Native interop: LPArray output parameter becomes invalid after call
* [36161](https://bugzilla.xamarin.com/show_bug.cgi?id=36161):
    NPE with JSON.NET
* [36183](https://bugzilla.xamarin.com/show_bug.cgi?id=36183):
    Since upgrading to Xamarin Android 6 get error error MSB3733: Input file &quot;obj\Android\Debug\android\AndroidManifest.xml&quot; cannot be opened
* [36214](https://bugzilla.xamarin.com/show_bug.cgi?id=36214):
    UnixSignal.WaitAny can SIGPIPE under load
* [36247](https://bugzilla.xamarin.com/show_bug.cgi?id=36247):
    MT3001 Invalid octal number when not using LLVM
* [36256](https://bugzilla.xamarin.com/show_bug.cgi?id=36256):
    Memory leak related to KDTree.FromData&lt;int&gt;(points, distance)
* [36257](https://bugzilla.xamarin.com/show_bug.cgi?id=36257):
    Runtime crashes when debugging .ppdb(when requesting arguments)
* [36292](https://bugzilla.xamarin.com/show_bug.cgi?id=36292):
    Assignment operator (+=, ++, etc.) on generic items crashes with System.InvalidProgramException: Invalid IL code
* [36339](https://bugzilla.xamarin.com/show_bug.cgi?id=36339):
    Stepping is not working for .ppdb if /optimize+ is used
* [36356](https://bugzilla.xamarin.com/show_bug.cgi?id=36356):
    HTTP proxy wildcard for no_proxy
* [36370](https://bugzilla.xamarin.com/show_bug.cgi?id=36370):
    AOT: Can't insert into Dictionary&lt;UInt32Enum, object&gt;
* [36383](https://bugzilla.xamarin.com/show_bug.cgi?id=36383):
    async / await - Custom awaiter crashing on device
* [36384](https://bugzilla.xamarin.com/show_bug.cgi?id=36384):
    Mono does not recognise overloaded method with &quot;params object[]&quot;
* [36388](https://bugzilla.xamarin.com/show_bug.cgi?id=36388):
    Application settings produce extra XML headers during saving
* [36401](https://bugzilla.xamarin.com/show_bug.cgi?id=36401):
    [XM 2.4] &quot;System.Configuration.ConfigurationErrorsException: Failed to load configuration section for dataContractSerializer&quot; when using ChannelFactory with the &quot;Xamarin.Mac .NET 4.5 Framework&quot;
* [36414](https://bugzilla.xamarin.com/show_bug.cgi?id=36414):
    [Mono 4.2 Regression]: ThreadPool.SetMinThreads and ThreadPool.GetAvailableThreads don't works as expected
* [36425](https://bugzilla.xamarin.com/show_bug.cgi?id=36425):
    Erroneous CS0266 error
* [36436](https://bugzilla.xamarin.com/show_bug.cgi?id=36436):
    XslCompiledTransform causes hang during execution
* [36443](https://bugzilla.xamarin.com/show_bug.cgi?id=36443):
    counter warning printed when two threads terminate with exceptions simultaneously
* [36560](https://bugzilla.xamarin.com/show_bug.cgi?id=36560):
    Unhandled exceptions outside the main execution context are ignored
* [36589](https://bugzilla.xamarin.com/show_bug.cgi?id=36589):
    &quot;Compiler crashed with code 1&quot; when awaiting in interpolated string
* [36596](https://bugzilla.xamarin.com/show_bug.cgi?id=36596):
    Potential HttpClient Ntlm memory leak
* [36646](https://bugzilla.xamarin.com/show_bug.cgi?id=36646):
    Delegate.Remove for combined delegate works different from Microsoft .Net
* [36724](https://bugzilla.xamarin.com/show_bug.cgi?id=36724):
    Error when inserting SessionID into Uri on Linux
* [36829](https://bugzilla.xamarin.com/show_bug.cgi?id=36829):
    XmlSerializer does not support subclasses when serializing sequences of items
* [36848](https://bugzilla.xamarin.com/show_bug.cgi?id=36848):
    Frequent crash with XS master (roslyn enabled)
* [37035](https://bugzilla.xamarin.com/show_bug.cgi?id=37035):
    Creating service host with singleton fails
* [37080](https://bugzilla.xamarin.com/show_bug.cgi?id=37080):
    Compiler not evaluating elvis operator ?. correctly
* [37171](https://bugzilla.xamarin.com/show_bug.cgi?id=37171):
    DataContractSerializer does not handle ISerializable at all
* [37232](https://bugzilla.xamarin.com/show_bug.cgi?id=37232):
    Inconsistent accessibility not detected in partial classes in XS on Mac
* [37273](https://bugzilla.xamarin.com/show_bug.cgi?id=37273):
    Exceptions caught in incorrect catch blocks on LLVM builds
* [37313](https://bugzilla.xamarin.com/show_bug.cgi?id=37313):
    SIGABRT on System.Runtime.CompilerServices.RuntimeHelpers.RunClassConstructor
* [37412](https://bugzilla.xamarin.com/show_bug.cgi?id=37412):
    Attempting to JIT compile method PCLCrypto.DeriveBytes:GetBytes crash
* [37436](https://bugzilla.xamarin.com/show_bug.cgi?id=37436):
    Invocation of Func&lt;&gt; based delegates fails on v4.2.1.124 on OSX &amp; Linux: Delegate is never actually invoked by runtime
* [37547](https://bugzilla.xamarin.com/show_bug.cgi?id=37547):
    Exception in unhandled exception handler not catched after Thread.Abort
* [37681](https://bugzilla.xamarin.com/show_bug.cgi?id=37681):
    Fails to parse negative integers with Hebrew region set
* [37695](https://bugzilla.xamarin.com/show_bug.cgi?id=37695):
    Delegate references an overridden method in derived class misbehaves when marshalled as a parameter to native C function.
* [38012](https://bugzilla.xamarin.com/show_bug.cgi?id=38012):
    Using Task's under memory pressure leads to unexpected crashes inside the TPL on iOS
* [38161](https://bugzilla.xamarin.com/show_bug.cgi?id=38161):
    Instability/crash when using `DateTime` under cpu load
* [38250](https://bugzilla.xamarin.com/show_bug.cgi?id=38250):
    Stack Corruption in mono involving tailcalls (where code is fine on Windows)
* [38331](https://bugzilla.xamarin.com/show_bug.cgi?id=38331):
    No longer able to run unit test project from command line via 'mono nunit-console.exe'
* [38379](https://bugzilla.xamarin.com/show_bug.cgi?id=38379):
    Byte enums fail to compare correctly on 64 bit iOS devices when using the LLVM compiler
* [38408](https://bugzilla.xamarin.com/show_bug.cgi?id=38408):
    Error disposing of Filestream when leaving using statement
* [38525](https://bugzilla.xamarin.com/show_bug.cgi?id=38525):
    kill -QUIT produces a very broken stacktrace
* [38599](https://bugzilla.xamarin.com/show_bug.cgi?id=38599):
    Regression: SynchronizationContext.Current returns wrong value in delegate run by SynchronizationContext.Send.
* [38600](https://bugzilla.xamarin.com/show_bug.cgi?id=38600):
    mkbundle Doesn't support assemblies with spaces in their names.
* [38638](https://bugzilla.xamarin.com/show_bug.cgi?id=38638):
    Getting build error &quot;Error initializing task XmlPeek: Not registered task XmlPeek&quot;.
* [38712](https://bugzilla.xamarin.com/show_bug.cgi?id=38712):
    Mono 4.3 Cryptography.ProtectedData fails to decrypt data from Mono 4.2
* [38825](https://bugzilla.xamarin.com/show_bug.cgi?id=38825):
    `mono_image_open()` does not check header anymore
* [38933](https://bugzilla.xamarin.com/show_bug.cgi?id=38933):
    `CryptographicException` from `ProtectedData` in multi-threaded execution
* [39307](https://bugzilla.xamarin.com/show_bug.cgi?id=39307):
    HTTPS connections broken in recent Linux snapshot builds
* [39569](https://bugzilla.xamarin.com/show_bug.cgi?id=39569):
    Validation of ETag by `HttpHeaders.Add()` is too strict
* [39644](https://bugzilla.xamarin.com/show_bug.cgi?id=39644):
    `* Assertion at image.c:512, condition 'image-&gt;heap_guid.size &gt;= 16' not met`
* [40060](https://bugzilla.xamarin.com/show_bug.cgi?id=40060):
    `System.TypeSpec.Parse()` cannot parse generics + anonymous type name
* [40306](https://bugzilla.xamarin.com/show_bug.cgi?id=40306):
    Native crash in `System.Net.Sockets.Socket.Close_internal()`.


<a name="API_Changes" />
# API Changes

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

