---
id: 2DDECBDB-0A7F-4C0A-B862-5463C603A5BC
title: "Xamarin.Android 4.8"
---

The Xamarin.Android 4.8 series contains the upgrade of the Mono
runtime engine to [Mono 3.0](http://www.mono-project.com/Release_Notes_Mono_3.0). [12](http://www.mono-project.com/Release_Notes_Mono_3.0#New_in_Mono_3.0.12),
and includes advanced features like C# 5 and async programming.

First-class support for asynchronicity is a powerful and
brilliantly simple language tool.

It makes it easy to write responsive user interfaces, which in
turn makes for delighted users
It makes complex workflows, with their error handling, natural
to write.  This translates into proper error messages and
proper program recovery; and finally
by letting the compiler do the work for you, it eliminates
bugs from your code, and enables you to enjoy your work and to
focus on what really matters for your application.

While asynchronicity is the main theme of this release, we
also pack two years of improvements to the Mono runtime spread
over more than 7,000 individual commits that are now available
to Android, Mac and iOS users.

Among the new features:

-  New .NET 4.5 APIs
-  Async-friendly  `System.Net.Http`
-  Improved debugging stack
-  Variant and contravariant interfaces
-  Fewer unbound Java types


 **New .NET 4.5 APIs:** We’re bringing in a huge refresh to the
class libraries. Our current products have historically been
an extension of the Silverlight API. Now our class libraries
are based on the .NET 4.5 profile.

 **New System.Net.Http:** This is such a delightful async API that
it deserves to be called out on its own. This is an
async-friendly HTTP stack, and makes building clients apps
trivial. We now ship `System.Net.Http`, a new, async ready,
HTTP stack that have been designed from the bottom up to work well
with the new version of the language.



 **Debugging Upgrades:**

 Our debugger has received a lots of small
improvements and fixes, they add up and you will notice how
all the small details now work more smoothly than before. **Variance and Contravariance:** With the upgrade to our class
libraries, we have introduced support for variance and
contravariance in the core types. While this change enables a
whole class of new code to be written, it also means that some
old code that was not covariant/contravariance friendly will
have to be adjusted.

 **Fewer unbound Java types:** In prior releases, many Java
packages were omitted because they were "duplicative" of the .NET
stack, such as the `org.xml.sax` package and `java.lang.reflect`. Nearly all types are now bound.

# Installation

 **Known issue**: Immediately after upgrading, users may have
trouble loading Xamarin.Android projects. Please restart Xamarin Studio again
if you experience this.

 **Visual Studio Users**: You should be prompted with this update
when you open a Xamarin.Android project. You can also check manually in Tools
&gt; Options &gt; Xamarin.Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates.
IDE support requires Xamarin Studio 4.0.
Layout Designer fixes require MonoDevelop 3.0.4.

 <a name="3"></a>


 <a name="Xamarin.Android_4.8.3"></a>


#  [Xamarin.Android 4.8.3](#Xamarin.Android_4.8.3)

### Bug fixes

-  Fixed linking issues with PCL.
-   [13957](https://bugzilla.xamarin.com/show_bug.cgi?id=13957) : Xamarin.Android Apps are crashing on dual core x86 Devices. 
-   [14033](https://bugzilla.xamarin.com/show_bug.cgi?id=14033) : Cannot build Android project due to recursive activation. 
-   [15214](https://bugzilla.xamarin.com/show_bug.cgi?id=15214) :  `CultureInfo.CurrentCulture` returns Invariant culture. 
-   [15265](https://bugzilla.xamarin.com/show_bug.cgi?id=15265) : ResolveSdks/CheckProjectItems task failed unexpectedly: WaitAll for multiple handles on a STA thread is not supported 


 <a name="2"></a>


 <a name="Xamarin.Android_4.8.2"></a>


#  [Xamarin.Android 4.8.2](#Xamarin.Android_4.8.2)

### New Features

 **Note:** It is *strongly recommended* that all binding assemblies
be *rebuilt*, as this is required in order to fully fix [Bug #13521](https://bugzilla.xamarin.com/show_bug.cgi?id=13521).
Binding assemblies built with the 4.8.2 or later releases *will not work*
on previous releases.

-  [Android 4.3 (API level 18) binding](http://developer.android.com/about/versions/android-4.3.html) .
-  Add support for embedded assets in library assemblies.
-  Improve OpenTK-1.0.dll matrix inversion performance.


### Bug fixes

-   [7797](https://bugzilla.xamarin.com/show_bug.cgi?id=7797) : Support Java7 JavaDoc format for importing parameter names. Use the  `$(Java7DocPaths)` MSBuild property group to specify a directory which contains Java 7 JavaDoc documentation. 
-   [8754](https://bugzilla.xamarin.com/show_bug.cgi?id=8754) : Allow  `ExportAttribute` to be used on constructors, and allow custom code fragments to be used for the generated Java  `super` constructor invocation.  [Example](https://bugzilla.xamarin.com/show_bug.cgi?id=8754#c34) 
-   [11247](https://bugzilla.xamarin.com/show_bug.cgi?id=11247) : Build > Package in VS2012 hangs while building Android app. 
-   [13343](https://bugzilla.xamarin.com/show_bug.cgi?id=13343) : Allow  `FtpWebRequest` to interract with FTP servers which use  `\` as a directory separator char. 
-   [13397](https://bugzilla.xamarin.com/show_bug.cgi?id=13397) : Propertly set  `$(TargetFrameworkVersion)` in Binding projects. 
-   [13438](https://bugzilla.xamarin.com/show_bug.cgi?id=13438) : Enable satellite assemblies in bundled applications. 
-   [13440](https://bugzilla.xamarin.com/show_bug.cgi?id=13440) : Support building within Xamarin Studio when the project name is not a valid C# identifier. 
-   [13461](https://bugzilla.xamarin.com/show_bug.cgi?id=13461) : Fix  `System.Net.NetworkInformation.NetworkChange` . 
-   [13521](https://bugzilla.xamarin.com/show_bug.cgi?id=13521) : Don't die with a SIGSEGV if the JNIEnv interface pointer changes values. 
-   [13686](https://bugzilla.xamarin.com/show_bug.cgi?id=13686) : Fix  `System.TimeZoneInfo` when running on Android v4.3. 
-   [13687](https://bugzilla.xamarin.com/show_bug.cgi?id=13687) : Fixed Android OpenGL template to set the HardwareAccelerated flag on the Activity. 
-   [13697](https://bugzilla.xamarin.com/show_bug.cgi?id=13697) : Fix  `NullReferenceException` when starting NUnit Activity. 


### Integrated Mono features/fixes

Based on [Mono 3.2.1](http://www.mono-project.com/Release_Notes_Mono_3.2#New_in_Mono_3.2.1) [commit 7185894](https://github.com/mono/mono/commit/71858945c3415fcf38b940ad055ac6b25736d258).

-   [3924](https://bugzilla.xamarin.com/show_bug.cgi?id=3924) : WebClient - Incomplete download but DownloadFileCompleted is triggered without error. 
-   [11598](https://bugzilla.xamarin.com/show_bug.cgi?id=11598) : SemaphoreSlim.Wait uses 100% CPU. 
-   [12393](https://bugzilla.xamarin.com/show_bug.cgi?id=12393) : HttpWebRequest.Host does not understand IPv6 addresses. 
-   [12745](https://bugzilla.xamarin.com/show_bug.cgi?id=12745) : TaskAwaiter.GetResult() throws an exception if the task hasn't completed. 
-   [13110](https://bugzilla.xamarin.com/show_bug.cgi?id=13110) : StructuralComparisons.StructuralEqualityComparer doesn't compare array of integers correctly. 
-   [13466](https://bugzilla.xamarin.com/show_bug.cgi?id=13466) : Don't remove  `System.Net.HttpWebRequest.CachePolicy` . 
-   [13509](https://bugzilla.xamarin.com/show_bug.cgi?id=13509) : Mono throws exception trying to read CultureInfo when region is zh-TW. 


 <a name="1"></a>


 <a name="Xamarin.Android_4.8.1"></a>


#  [Xamarin.Android 4.8.1](#Xamarin.Android_4.8.1)

### Bug fixes

-  No longer fail to build with an  `XmlException` when linking a Release build in projects that reference  `System.Data.Services.Client.dll` . 
-   [13391](https://bugzilla.xamarin.com/show_bug.cgi?id=13391) : System.Net.dll is missing when using PCL on Android. 
-   [13460](https://bugzilla.xamarin.com/show_bug.cgi?id=13460) : Fix assert in  `bsearch` when running on Android v4.3. 
-   [13490](https://bugzilla.xamarin.com/show_bug.cgi?id=13490) : App crashes when culture is zh_TW. 
-   [13500](https://bugzilla.xamarin.com/show_bug.cgi?id=13500) : Fix assert  `mini/mini.c:3806, condition `l' not met` . 


 <a name="0"></a>


 <a name="Xamarin.Android_4.8.0"></a>


#  [Xamarin.Android 4.8.0](#Xamarin.Android_4.8.0)

### New Features

<ul>
  <li>F# support</li>
  <li>C#5 <code>Async</code> overloads</li>
  <li>Binding projects support Android <code>.aar</code> files. Use a
    <b>Build action</b> of <code>LibraryProjectZip</code>.</li>
  <li>Accessing the e.g. <a href="http://androidapi.xamarin.com/?link=P%3aAndroid.Widget.TextView.Text">TextView.Text</a> property getter (and other <code>string</code> property
    getters) should now dispose of the intermediate GREF.
  </li>
  <li>Add <code>Java.Interop.Runtime.MaxGlobalReferenceCount</code>
    <code>Java.Interop.Runtime.GlobalReferenceCount</code>
    <code>Java.Interop.Runtime.LocalReferenceCount</code> properties
    and
    <code>Java.Interop.Runtime.GetSurfacedObjects()</code>.
    These are for diagnostic purposes and should not be relied upon.
  </li>
  <li>Android SDK r22 support</li>
  <li>The Mono runtime is now built with the
    <a href="http://developer.android.com/tools/sdk/ndk/index.html">Android
    NDK</a>, revision 8e</li>
  <li>Generated binding files now get <code>Metadata.xml</code> XPath info.</li>
  <li>Give meaningful message for missing
    <code>//attr/@name</code> attribute in <code>Metadata.xml</code>.</li>
  <li>Inclusion of <code>Xamarin.Android.NUnitLite.dll</code> and ability to
    write NUnit-based projects within Xamarin Studio 4.0.8+.</li>
  <li><code>$(AndroidUseLatestPlatformSdk)</code>: new MSBuild property; if
    <code>True</code>, cause the build process to use the latest (highest
    numbered) Android Platform SDK. [Infrastructure]</li>
  <li>Runtime now is built with proper hardware floating point on armv7
    (managed code would already use it correctly)</li>
  <li>Within Android Java Library Binding projects, C# custom attributes can
    now be inserted into the generated code by adding a
    <code>customAttributes</code> attribute:
    <pre><code class=" syntax brush-C#">&lt;attr
        path="/api/package[@name='mono.android.app']/class[@name='IntentService']/constructor[count(parameter) = 0]"
        name="customAttributes"&gt;
    [Preserve(Conditional = true)]
&lt;/attr&gt;</code></pre>
  </li>
</ul>

### Bug fixes

-  Fix preservation of  `AesCryptoServiceProvider` .
-  Add  `[Flags]` to various enumerations.
-  Generate  `XA42303` for  `[Activity(Name=".Foo")]` .
-  Fix installation of the Visual Studio add-on when Visual Studio is installed into a non-default location. 
-  Use  `Encoding.Default` for  `javac` response files.
-  More sanely select a working directory for  `mandroid` execution.
-  Fix license activation problem which occurs when both Xamarin.Android and Xamarin.iOS licenses are checked at the same time.
-  Fixed method lookup to avoid duplicate method bindings
-  Cecil is now vendorized. This fixes conflicts &amp; bugs in between VS, XS and xbuild.
-  Fixed a GC interop regression when you build a linked list out of user peers.
-  Fixed Typos in 'Publish Android Application' dialog
-  Better handle system with unavailable devices (VMs with a floppy drive)
-  Improved diagnostics on deployment failures
-  Multiple linker issues fixed when building from inside Xamarin Studio
-  Faster KillProcess behavior
-   [Support Java to C# rectangular array marshaling](http://stackoverflow.com/questions/17305522/mono-for-android-binding-jagged-array) . 
-   [360](https://bugzilla.xamarin.com/show_bug.cgi?id=360) : Generate property setters for array fields. 
-   [5037](https://bugzilla.xamarin.com/show_bug.cgi?id=5037) : Copy Satellite assemblies into obj/Release/assemblies. 
-   [5980](https://bugzilla.xamarin.com/show_bug.cgi?id=5980) : Marshal non- `Java.Lang.Object` types as  `java.lang.Object` . 
-   [7774](https://bugzilla.xamarin.com/show_bug.cgi?id=7774) : Date property for DatePicker 
-   [7953](https://bugzilla.xamarin.com/show_bug.cgi?id=7953) : Fix  `TimeZoneInfo` id lookup. 
-   [8209](https://bugzilla.xamarin.com/show_bug.cgi?id=8209) : Generate .mdb files for libraries that only have .pdb 
-   [8353](https://bugzilla.xamarin.com/show_bug.cgi?id=8353) : Add UI for  `$(JavaHeapSize)` ,  `$(JavaOptions)` . 
-   [8369](https://bugzilla.xamarin.com/show_bug.cgi?id=8369) : BindingsGenerator couldn't not handle ApiXmlInput containing empty spaces. 
-   [8428](https://bugzilla.xamarin.com/show_bug.cgi?id=8428) : Linker needs to preserve IntentService default constructor. 
-   [9800](https://bugzilla.xamarin.com/show_bug.cgi?id=9800) : Fix  `.axml` IntelliSense within Visual Studio. 
-   [10135](https://bugzilla.xamarin.com/show_bug.cgi?id=10135) : Generate XA4207 when a C# generic class (indirectly) subclasses  `Java.Lang.Object` and uses  `[Export]` or  `[ExportField]` . 
-   [10153](https://bugzilla.xamarin.com/show_bug.cgi?id=10153) ,  [10978](https://bugzilla.xamarin.com/show_bug.cgi?id=10978) : Add ability to set minimum Android SDK. 
-   [10580](https://bugzilla.xamarin.com/show_bug.cgi?id=10580) : Always preserve Mono.Runtime. 
-   [10693](https://bugzilla.xamarin.com/show_bug.cgi?id=10693) : Disable serialization assembly generation. 
-   [10771](https://bugzilla.xamarin.com/show_bug.cgi?id=10771) : MakeBundleNativeCodeExternal task is broken 
-   [10865](https://bugzilla.xamarin.com/show_bug.cgi?id=10865) : Re-enable the "Bundle assemblies into native code" checkbox. 
-   [11051](https://bugzilla.xamarin.com/show_bug.cgi?id=11051) : Provide non-exceptional error messages for ACW generation. 
-   [11170#c3](https://bugzilla.xamarin.com/show_bug.cgi?id=11170#c3) : Fail more gracefully with invalid resource files. 
-   [11401](https://bugzilla.xamarin.com/show_bug.cgi?id=11401) : Fastdev directory creation fails on API-12 devices. 
-   [11471](https://bugzilla.xamarin.com/show_bug.cgi?id=11471) : annotations need to be generated as interface, not class 
-   [11529](https://bugzilla.xamarin.com/show_bug.cgi?id=11529) : 'Publish Android Application' dialog window has multiple typos. 
-   [11608](https://bugzilla.xamarin.com/show_bug.cgi?id=11608) : move  `<activity-alias/>` elements directly after their target activities 
-   [11694](https://bugzilla.xamarin.com/show_bug.cgi?id=11694) : Reject  `project.properties` file which is placed on an ancestor of obj/*. 
-   [11740](https://bugzilla.xamarin.com/show_bug.cgi?id=11740) : MSBuild error being thrown on release builds. 
-   [11744](https://bugzilla.xamarin.com/show_bug.cgi?id=11744) : When user add image to resources folder it displayed Build Action to Content. 
-   [11782](https://bugzilla.xamarin.com/show_bug.cgi?id=11782) : Fixed nested class names in nested interfaces. 
-   [11783](https://bugzilla.xamarin.com/show_bug.cgi?id=11783) : jcifs: binding generator tools miss some methods that involves derivation in different jars 
-   [11797](https://bugzilla.xamarin.com/show_bug.cgi?id=11797) : Starter edition should support Android Library projects which use Android Resources. 
-   [11803](https://bugzilla.xamarin.com/show_bug.cgi?id=11803) : User is not able to deploy the application on the emulator/device, the app is closed immediately after launching. 
-   [11918](https://bugzilla.xamarin.com/show_bug.cgi?id=11918) : Trial users don't get Fast Deployment support. 
-   [11921](https://bugzilla.xamarin.com/show_bug.cgi?id=11921) : AndroidGameView lockups up when Stop is called 
-   [11950](https://bugzilla.xamarin.com/show_bug.cgi?id=11950) : Properly handle null array fields. 
-   [11964](https://bugzilla.xamarin.com/show_bug.cgi?id=11964) : MapsAndLocationDemo_v2 example causes recursive path build issue. 
-   [12007](https://bugzilla.xamarin.com/show_bug.cgi?id=12007) : float values are being corrupted/lost when inserted into a  `Queue<float>` . 
-   [12112](https://bugzilla.xamarin.com/show_bug.cgi?id=12112) : GC STW fix. 
-   [12243](https://bugzilla.xamarin.com/show_bug.cgi?id=12243) : ScanAssemblies build task counts referenced assembly twice. 
-   [12250](https://bugzilla.xamarin.com/show_bug.cgi?id=12250) : Invalid folders in setup.msi 
-   [12254](https://bugzilla.xamarin.com/show_bug.cgi?id=12254) : Fix event de-registration involving  `Add` and  `Remove` methods. 
-   [12269](https://bugzilla.xamarin.com/show_bug.cgi?id=12269) ,  [12381](https://bugzilla.xamarin.com/show_bug.cgi?id=12381) ,  [12428](https://bugzilla.xamarin.com/show_bug.cgi?id=12428) ,  [12520](https://bugzilla.xamarin.com/show_bug.cgi?id=12520) : Fix  `Aes.Create()` . 
-   [12370](https://bugzilla.xamarin.com/show_bug.cgi?id=12370) : Fix detection of  `dx` on Windows. 
-   [12432](https://bugzilla.xamarin.com/show_bug.cgi?id=12432) : Fix slow builds due to touching  `res\values\styles.xml` . 
-   [12479](https://bugzilla.xamarin.com/show_bug.cgi?id=12479) : Fix lref leak in  `JNIEnv.NewArray(Array, Type)` . 
-   [12594](https://bugzilla.xamarin.com/show_bug.cgi?id=12594) : Fix the "Build failure, register the machine, build failure" loop. 
-   [12821](https://bugzilla.xamarin.com/show_bug.cgi?id=12821) : taskify resource designer touches and make it not crash. 
-   [12935](https://bugzilla.xamarin.com/show_bug.cgi?id=12935) : Generate  `sensorPortait` instead of  `sensorPortrait` . 
-   [12938](https://bugzilla.xamarin.com/show_bug.cgi?id=12938) : Ensure directories exist before searching them. 
-   [13064](https://bugzilla.xamarin.com/show_bug.cgi?id=13064) : Trial edition has access to Enterprise features. 
-   [13171](https://bugzilla.xamarin.com/show_bug.cgi?id=13171) : Fix F# build hang. 
-   [13299](https://bugzilla.xamarin.com/show_bug.cgi?id=13299) : Fix SIGILL with armeabi-v7a runtime when executing on the Motorola Xoom. 
-   [13391](https://bugzilla.xamarin.com/show_bug.cgi?id=13391) :  `System.Net.dll` is missing from Windows install. 


### Integrated Mono features/fixes

Based on [Mono 3.0.12](http://www.mono-project.com/Release_Notes_Mono_3.0#New_in_Mono_3.0.12) [commit ac11abe](https://github.com/mono/mono/commit/ac11abe18d6847807e5dbc7ca16c1530bb0fc517).

-  OS X 10.9 support.
-  Optimized Marshal code that read/write from native memory.
-  Fixed multiple bugs in culture handling and date parsing.
-  Optimized LINQ with arrays.
-  Sgen can now return memory to the OS on 32bits systems.
-  Fix race condition in  `System.Net.WebConnectionStream` .
-  Fix  `new BigInteger().GetHashCode()` to not throw.
-  Fix delegate combine when left side has already been invoked.
-  Implement  `System.Net.Http.WebRequestHandler` .
-  [Add System.Diagnostics.Switch/etc.](http://forums.xamarin.com/discussion/3300/rationale-behind-removal-of-system-diagnostics-trace-in-xa-and-xi)
-   [327](https://bugzilla.xamarin.com/show_bug.cgi?id=327) : if  `sqlite3_column_origin_name` is not found, omit the metadata, instead of exploding 
-   [4595](https://bugzilla.xamarin.com/show_bug.cgi?id=4595) : Clear entries referencing the domain in reference_queue_clear_for_domain () even if the object is already null 
-   [5598](https://bugzilla.xamarin.com/show_bug.cgi?id=5598) : Fix memleak by using a LruCache 
-   [5904](https://bugzilla.xamarin.com/show_bug.cgi?id=5904) ,  [12355](https://bugzilla.xamarin.com/show_bug.cgi?id=12355) ,  [12395](https://bugzilla.xamarin.com/show_bug.cgi?id=12395) : Fix incorrect end-of-stream with null callback. 
-   [6510#c10](https://bugzilla.xamarin.com/show_bug.cgi?id=6510#c10) : Really, actually, fully, use X.509 certificates instead of some random default provider. 
-   [10317](https://bugzilla.xamarin.com/show_bug.cgi?id=10317) : Preserve CustomAttributeData and related ctors. 
-   [10392](https://bugzilla.xamarin.com/show_bug.cgi?id=10392) : Don't try to merge interfaces between to non-interface types. 
-   [10887](https://bugzilla.xamarin.com/show_bug.cgi?id=10887) : Handle shifts by multiple of 32 correctly. 
-   [11294](https://bugzilla.xamarin.com/show_bug.cgi?id=11294) : Fix incompatibility with .NET's serialization of ObservableCollection 
-   [11362](https://bugzilla.xamarin.com/show_bug.cgi?id=11362) : Fail with an exception when loading the value of field of a broken class. 
-   [11694](https://bugzilla.xamarin.com/show_bug.cgi?id=11694) : Check interface implementation using all base types members. 
-   [11703](https://bugzilla.xamarin.com/show_bug.cgi?id=11703) : Mono.Security.X509Certificate.Hash does not support SHA2 digest algorithms, makes such certificates unusable with XSP. 
-   [11739](https://bugzilla.xamarin.com/show_bug.cgi?id=11739) : Fix quoted values parsing for custom tostring formats. 
-   [11796](https://bugzilla.xamarin.com/show_bug.cgi?id=11796) : Don't check public token on missing references. 
-   [11862](https://bugzilla.xamarin.com/show_bug.cgi?id=11862) : Fix the map of bool and char in runtime invoke signatures. 
-   [11867](https://bugzilla.xamarin.com/show_bug.cgi?id=11867) : Don't catch aggregate exception handle predicate exceptions. 
-   [11880](https://bugzilla.xamarin.com/show_bug.cgi?id=11880) : Ignore requests to set breakpoints at il offsets belonging to dead code. 
-   [11908](https://bugzilla.xamarin.com/show_bug.cgi?id=11908) : Task.Yield needs to continue on synchronization context if there is any. 
-   [11945](https://bugzilla.xamarin.com/show_bug.cgi?id=11945) : Better handle default value BigInteger. 
-   [11979](https://bugzilla.xamarin.com/show_bug.cgi?id=11979) : StreamWriter async methods cannot call base TextWriter async methods. 
-   [12001](https://bugzilla.xamarin.com/show_bug.cgi?id=12001) : Fix TraceSource constructor. 
-   [12008](https://bugzilla.xamarin.com/show_bug.cgi?id=12008) : Don't throw when trying to parse leading sign number only. 
-   [12329](https://bugzilla.xamarin.com/show_bug.cgi?id=12329) : Using CountAsync on device with Parse 1.2.4 library crashes with JIT issue. 
-   [12342](https://bugzilla.xamarin.com/show_bug.cgi?id=12342) : NullReferenceException in IAsyncResult.AsyncWaitHandle.WaitOne. 
-   [12349](https://bugzilla.xamarin.com/show_bug.cgi?id=12349) : HttpClient.GetStringAsync throws NullReferenceException on concurrent requests. 
-   [12457](https://bugzilla.xamarin.com/show_bug.cgi?id=12457) :  `X509Certificate2` is not marked as  `Serializable` . 
-   [12461](https://bugzilla.xamarin.com/show_bug.cgi?id=12461) : Make sure the behavior between GetFiles and EnumerateFiles are the same regarding symlinks. 
-   [12494](https://bugzilla.xamarin.com/show_bug.cgi?id=12494) : Keep the exception object alive during debugger suspensions. 
-   [12609](https://bugzilla.xamarin.com/show_bug.cgi?id=12609) : Runtime assert  `condition `mono_defaults.iunknown_class != 0' not met` . 
-   [12856](https://bugzilla.xamarin.com/show_bug.cgi?id=12856) : Fix  `MethodInfo::ToString()` to properly format generic structs 


 <a name="API_Changes" class="injected"></a>


### API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.8/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.8/level_7_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_7_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_7_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_7_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_4_diff/opentk-1.0.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.8/level_8_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_8_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_8_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_8_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_8_diff/opentk-1.0.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.8/level_10_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_10_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_10_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_10_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_10_diff/opentk-1.0.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.8/level_12_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_12_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_12_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_12_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_12_diff/opentk-1.0.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.8/level_14_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_14_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_14_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.8/level_14_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_14_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_14_diff/opentk-1.0.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.8/level_15_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_15_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_15_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.8/level_15_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_15_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_15_diff/opentk-1.0.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.8/level_16_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_16_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_16_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.8/level_16_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_16_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_16_diff/opentk-1.0.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.8/level_17_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.8/level_17_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.8/level_17_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.8/level_17_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.8/level_17_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.8/level_17_diff/opentk-1.0.dll)
