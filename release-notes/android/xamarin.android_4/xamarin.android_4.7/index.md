---
id: 20DDF077-4274-4A71-AAE7-015BBE26A0E2
title: "Xamarin.Android 4.7"
---

The Xamarin.Android 4.7 series contains the upgrade of the Mono
	runtime engine to the Mono 3.0 system, and includes advanced
	features like C# and async programming.

First-class support for asynchronicity is a powerful and
	brilliantly simple language tool.

It makes it easy to write responsive user interfaces, which in
	turn makes for delighted users
	It makes complex workflows, with their error handling, natural
	to write.  This translates into proper error messages and
	proper program recovery; and finally
	By letting the compiler do the work for you, it eliminates
	bugs from your code, and enables you to enjoy your work and to
	focus on what really matters for your application.
	This is best seen by watching it in action.  See how this
	piece of old C# code turns into a piece of beauty.  Error
	handling and dealing with the UI thread go from painful to
	trivial. To learn more about how to use async start from this
	article.

While asynchronicity is the main theme of this release, we
	also pack two years of improvements to the Mono runtime spread
	over more than 7,000 individual commits that are now available
	to Android, Mac and iOS users.

Among the new features:-  New .NET 4.5 APIs 
-  iOS generic compiler improvements, fewer “Attempting to JIT compile method” errors. 
-  Async-friendly System.Net.Http 
-  Improved debugging stack 
-  Variant and contravariant interfaces 




 **New .NET 4.5 APIs:**

 We’re bringing in a huge refresh to the
	class libraries. Our current products have historically been
	an extension of the Silverlight API. Now our class libraries
	are based on the .NET 4.5 profile.

 **New System.Net.Http:**

 This is such a delightful async API that
	it deserves to be called out on its own. This is an
	async-friendly HTTP stack, and makes building clients apps
	trivial We now ship System.Net.Http, a new, async ready, HTTP
	stack that have been designed from the bottom up to work well
	with the new version of the language.

 **Debugging Upgrades:**

 Our debugger has received a lots of small
	improvements and fixes, they add up and you will notice how
	all the small details now work more smoothly than before.

 **Variance and Contravariance:**

 With the upgrade to our class
	libraries, we have introduced support for variance and
	contravariance in the core types. While this change enables a
	whole class of new code to be written, it also means that some
	old code that was not covariant/contravariance friendly will
	have to be adjusted. <a name="0"></a>


 <a name="Xamarin.Android_4.7.0"></a>


#  [Xamarin.Android 4.7.0](#Xamarin.Android_4.7.0)

First release of the Mono 3.0-based stack.

The product is now based on mono 3.0. This includes C# 5
          with async, two years of improvements in the runtime and
          class libs.

The class libs are now based on top of .NET 4.5 bringing in
          a lot of improvements. Some core generic interfaces are now
          using covariance.

 <a name="1"></a>


 <a name="Xamarin.Android_4.7.1"></a>


#  [Xamarin.Android 4.7.1](#Xamarin.Android_4.7.1)

Improve performance of some string copying, object cloning
	  and boxing.

Fixed some culture related bugs.

 <a name="2"></a>


 <a name="Xamarin.iOS_4.7.2"></a>


#  [Xamarin.Android 4.7.2](#Xamarin.Android_4.7.2)

Optimized LINQ with arrays.

Sgen can now return memory to the OS on 32bits systems.

System.Net.Http.dll is now been shipped.

 <a name="3"></a>


 <a name="Xamarin.Android_4.7.3"></a>


#  [Xamarin.Android 4.7.3](#Xamarin.Android_4.7.3)

Our classlib is now built with /optimize+, this saves up to 1Mb
         compared to the previous alpha release.

Fixed a few bugs in the C# compiler regarding async.

Multiple fixes to the AOT compiler involving generics and async.

Reduced the number of thread roundtrips that
       HttpClientHandler does in some cases.

Optimized Marshal code that read/write from native memory.

Fixed multiple bugs in culture handling and date parsing.

 <a name="4"></a>


 <a name="Xamarin.Android_4.7.4"></a>


#  [Xamarin.Android 4.7.4](#Xamarin.Android_4.7.4)

Windows builds are back

Improved diagnostics on deployment failures

Multiple linker issues fixed when building from inside Xamarin Studio

Faster KillProcess behavior

 <a name="5"></a>


 <a name="Xamarin.Android_4.7.5"></a>


#  [Xamarin.Android 4.7.5](#Xamarin.Android_4.7.5)

## New Features

-  Starter edition size limit bumped to 64KB.
-  F# support
-  Generated binding files now get  `Metadata.xml` XPath info.
-  C#5 Async overloads
-  Give meaningful message for missing  `//attr/@name` attribute in  `Metadata.xml`
-  Inclusion of  `Xamarin.Android.NUnitLite.dll` and ability to write NUnit-based projects within Xamarin Studio 4.0.8+.
-  Android SDK r22 support
-  Add  `Java.Interop.ObjectManager.GetSurfacedObjects_ForDiagnosticsOnly()`
-  Initial work on bringing async to the Android Framework, some types already have async overloads
-  Runtime now is built with proper hardware floating point on armv7 (managed code would already use it correctly)


## Integrated Mono features/fixes



Based on [Mono 3.0.11](https://github.com/mono/mono/commit/f956a83b65670179cd3d344abb6bdceac29e22fe)

.-  [Add System.Diagnostics.Switch/etc.](http://forums.xamarin.com/discussion/3300/rationale-behind-removal-of-system-diagnostics-trace-in-xa-and-xi)
-   [327](https://bugzilla.xamarin.com/show_bug.cgi?id=327) : if  `sqlite3_column_origin_name` is not found, omit the metadata, instead of exploding 
-   [4595](https://bugzilla.xamarin.com/show_bug.cgi?id=4595) : Clear entries referencing the domain in reference_queue_clear_for_domain () even if the object is already null 
-   [5598](https://bugzilla.xamarin.com/show_bug.cgi?id=5598) : Fix memleak by using a LruCache 
-   [10392](https://bugzilla.xamarin.com/show_bug.cgi?id=10392) : Don't try to merge interfaces between to non-interface types. 
-   [11294](https://bugzilla.xamarin.com/show_bug.cgi?id=11294) : Fix incompatibility with .NET's serialization of ObservableCollection 
-   [11362](https://bugzilla.xamarin.com/show_bug.cgi?id=11362) : Fail with an exception when loading the value of field of a broken class. 
-   [11694](https://bugzilla.xamarin.com/show_bug.cgi?id=11694) : Check interface implementation using all base types members. 
-   [11739](https://bugzilla.xamarin.com/show_bug.cgi?id=11739) : Fix quoted values parsing for custom tostring formats. 
-   [11796](https://bugzilla.xamarin.com/show_bug.cgi?id=11796) : Don't check public token on missing references. 
-   [11862](https://bugzilla.xamarin.com/show_bug.cgi?id=11862) : Fix the map of bool and char in runtime invoke signatures. 
-   [11867](https://bugzilla.xamarin.com/show_bug.cgi?id=11867) : Don't catch aggregate exception handle predicate exceptions. 
-   [11880](https://bugzilla.xamarin.com/show_bug.cgi?id=11880) : Ignore requests to set breakpoints at il offsets belonging to dead code. 
-   [11908](https://bugzilla.xamarin.com/show_bug.cgi?id=11908) : Task.Yield needs to continue on synchronization context if there is any. 
-   [11979](https://bugzilla.xamarin.com/show_bug.cgi?id=1197) : StreamWriter async methods cannot call base TextWriter async methods. 
-   [12001](https://bugzilla.xamarin.com/show_bug.cgi?id=12001) : Fix TraceSource constructor. 
-   [12008](https://bugzilla.xamarin.com/show_bug.cgi?id=12008) : Don't throw when trying to parse leading sign number only. 


## Bug fixes

-  Use  `Encoding.Default` for  `javac` response files.
-  More sanely select a working directory for  `mandroid` execution.
-  Fix license activation problem which occurs when both Xamarin.Android and Xamarin.iOS licenses are checked at the same time.
-  Fixed method lookup to avoid duplicate method bindings
-  Cecil is now vendorized. This fixes conflicts &amp; bugs in between VS, XS and xbuild.
-  Fixed a GC interop regression when you build a linked list out of user peers.
-  Fixed Typos in 'Publish Android Application' dialog
-  Better handle system with unavailable devices (VMs with a floppy drive)
-   [5037](https://bugzilla.xamarin.com/show_bug.cgi?id=5037) : Copy Satellite assemblies into obj/Release/assemblies. 
-   [8209](https://bugzilla.xamarin.com/show_bug.cgi?id=8209) : Generate .mdb files for libraries that only have .pdb 
-   [10693](https://bugzilla.xamarin.com/show_bug.cgi?id=10693) : Disable serialization assembly generation. 
-   [11401](https://bugzilla.xamarin.com/show_bug.cgi?id=11401) : Fastdev directory creation fails on API-12 devices. 
-   [11471](https://bugzilla.xamarin.com/show_bug.cgi?id=11471) : annotations need to be generated as interface, not class 
-   [11529](https://bugzilla.xamarin.com/show_bug.cgi?id=11529) : 'Publish Android Application' dialog window has multiple typos. 
-   [11608](https://bugzilla.xamarin.com/show_bug.cgi?id=11608) : move  `<activity-alias>` elements directly after their target activities 
-   [11694](https://bugzilla.xamarin.com/show_bug.cgi?id=11694) : Reject  `project.properties` file which is placed on an ancestor of obj/*. 
-   [11740](https://bugzilla.xamarin.com/show_bug.cgi?id=11740) : MSBuild error being thrown on release builds. 
-   [11744](https://bugzilla.xamarin.com/show_bug.cgi?id=11744) : When user add image to resources folder it displayed Build Action to Content. 
-   [11782](https://bugzilla.xamarin.com/show_bug.cgi?id=11782) : Fixed nested class names in nested interfaces. 
-   [11783](https://bugzilla.xamarin.com/show_bug.cgi?id=11783) : jcifs: binding generator tools miss some methods that involves derivation in different jars 
-   [11803](https://bugzilla.xamarin.com/show_bug.cgi?id=11803) : User is not able to deploy the application on the emulator/device, the app is closed immediately after launching. 
-   [11918](https://bugzilla.xamarin.com/show_bug.cgi?id=11918) : Trial users don't get Fast Deployment support. 
-   [11921](https://bugzilla.xamarin.com/show_bug.cgi?id=11921) : AndroidGameView lockups up when Stop is called 
-   [11921](https://bugzilla.xamarin.com/show_bug.cgi?id=11921) : Fixed an AndroidGameView lockup when Stop is called. 
-   [11964](https://bugzilla.xamarin.com/show_bug.cgi?id=11964) : MapsAndLocationDemo_v2 example causes recursive path build issue. 
-   [12007](https://bugzilla.xamarin.com/show_bug.cgi?id=12007) : float values are being corrupted/lost when inserted into a  `Queue<float>` . 
-   [12112](https://bugzilla.xamarin.com/show_bug.cgi?id=12112) : GC STW fix. 
-   [12243](https://bugzilla.xamarin.com/show_bug.cgi?id=12243) : ScanAssemblies build task counts referenced assembly twice. 
-   [12250](https://bugzilla.xamarin.com/show_bug.cgi?id=12250) : Invalid folders in setup.msi 


 <a name="6"></a>


 <a name="Xamarin.Android_4.7.6"></a>


#  [Xamarin.Android 4.7.6](#Xamarin.Android_4.7.6)

## New Features

-  Bind the  `java.lang.Void` type.
-  Bind the  `java.text` package.


## Integrated Mono features/fixes

Based on [Mono 3.0.12](https://github.com/mono/mono/commit/8cabf341f7172e7c96d7c4eb72636d9729bc2a2a).

-  Improved PCL support.
-   [5904](https://bugzilla.xamarin.com/show_bug.cgi?id=5904) ,  [12355](https://bugzilla.xamarin.com/show_bug.cgi?id=12355) ,  [12395](https://bugzilla.xamarin.com/show_bug.cgi?id=12395) : Fix incorrect end-of-stream with null callback. 
-   [11703](https://bugzilla.xamarin.com/show_bug.cgi?id=11703) : Mono.Security.X509Certificate.Hash does not support SHA2 digest algorithms, makes such certificates unusable with XSP. 
-   [12329](https://bugzilla.xamarin.com/show_bug.cgi?id=12329) : Using CountAsync on device with Parse 1.2.4 library crashes with JIT issue. 
-   [12342](https://bugzilla.xamarin.com/show_bug.cgi?id=12342) : NullReferenceException in IAsyncResult.AsyncWaitHandle.WaitOne. 
-   [12349](https://bugzilla.xamarin.com/show_bug.cgi?id=12349) : HttpClient.GetStringAsync throws NullReferenceException on concurrent requests. 


## Bug fixes

-  Fix detection of  `aapt.exe` on Windows. (Windows should build and install now!)
-   [360](https://bugzilla.xamarin.com/show_bug.cgi?id=360) : Generate property setters for array fields. 
-   [11051](https://bugzilla.xamarin.com/show_bug.cgi?id=11051) : Provide non-exceptional error messages for ACW generation. 
-   [11950](https://bugzilla.xamarin.com/show_bug.cgi?id=11950) : Properly handle null array fields. 
-   [12370](https://bugzilla.xamarin.com/show_bug.cgi?id=12370) : Fix detection of  `dx` on Windows. 
-   [12432](https://bugzilla.xamarin.com/show_bug.cgi?id=12432) : Fix slow builds due to touching  `res\values\styles.xml` . 


 <a name="7"></a>


 <a name="Xamarin.Android_4.7.7"></a>


#  [Xamarin.Android 4.7.7](#Xamarin.Android_4.7.7)

## New Features

-  Updated  `Mono.Android.Support.v4.dll` and  `Mono.Android.Support.v13.dll` to bind the  [Android Support Library](http://developer.android.com/tools/extras/support-library.html) , revision 13.
-  The Mono runtime is now built with the  [Android NDK](http://developer.android.com/tools/sdk/ndk/index.html) , revision 8e


## Integrated Mono features/fixes

Based on [Mono 3.0.12](https://github.com/mono/mono/commit/c72d1b7f0b2b24d57d64d9e682ceefc2d8889d05).

-   [12494](https://bugzilla.xamarin.com/show_bug.cgi?id=12494) : Keep the exception object alive during debugger suspensions. 


## Bug fixes

-  Fix installation of the Visual Studio add-on when Visual Studio is installed into a non-default location. 
-   [8369](https://bugzilla.xamarin.com/show_bug.cgi?id=8369) : BindingsGenerator couldn't not handle ApiXmlInput containing empty spaces. 
-   [10580](https://bugzilla.xamarin.com/show_bug.cgi?id=10580) : Always preserve Mono.Runtime. 
-   [10771](https://bugzilla.xamarin.com/show_bug.cgi?id=10771) : MakeBundleNativeCodeExternal task is broken 
-   [11797](https://bugzilla.xamarin.com/show_bug.cgi?id=11797) : Starter edition should support Android Library projects which use Android Resources. 
-   [12479](https://bugzilla.xamarin.com/show_bug.cgi?id=12479) : Fix lref leak in  `JNIEnv.NewArray(Array, Type)` . 


 <a name="8"></a>


 <a name="Xamarin.Android_4.7.8"></a>


#  [Xamarin.Android 4.7.8](#Xamarin.Android_4.7.8)

## New Features

<ul>
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

## Integrated Mono features/fixes

Based on [Mono 3.0.12](https://github.com/mono/mono/commit/322d5bd38fee6f63dbd16dec7f1385afe14d9111).

-   [12461](https://bugzilla.xamarin.com/show_bug.cgi?id=12461) : Make sure the behavior between GetFiles and EnumerateFiles are the same regarding symlinks. 


## Bug fixes

-   [8428](https://bugzilla.xamarin.com/show_bug.cgi?id=8428) , Linker needs to preserve IntentService default constructor. 
-   [12269](https://bugzilla.xamarin.com/show_bug.cgi?id=12269) ,  [12381](https://bugzilla.xamarin.com/show_bug.cgi?id=12381) ,  [12428](https://bugzilla.xamarin.com/show_bug.cgi?id=12428) ,  [12520](https://bugzilla.xamarin.com/show_bug.cgi?id=12520) : Fix  `Aes.Create()` . 
-   [10135](https://bugzilla.xamarin.com/show_bug.cgi?id=10135) , Generate XA4207 when a C# generic class (indirectly) subclasses  `Java.Lang.Object` and uses  `[Export]` or  `[ExportField]` . 


 <a name="9"></a>


 <a name="Xamarin.Android_4.7.9"></a>


#  [Xamarin.Android 4.7.9](#Xamarin.Android_4.7.9)

This release serves to bring compatibility to those who use both
  Xamarin.iOS and Xamarin.Android in Visual Studio. This release is
  compatible with Xamarin.iOS for Visual Studio 1.2.

 <a name="10"></a>


 <a name="Xamarin.Android_4.7.10"></a>


#  [Xamarin.Android 4.7.10](#Xamarin.Android_4.7.10)

## New Features

-  PCL support!   
 (Cross your fingers, sacrifice your favorite meal under the full moon, and your PCL projects should Just Work! Testing wanted.) 
-  Binding projects support Android  `.aar` files. Use a  **Build action** of  `LibraryProjectZip` .
-  Accessing the e.g.  [TextView.Text](http://androidapi.xamarin.com/?link=P%3aAndroid.Widget.TextView.Text) property getter should now dispose of the intermediate GREF. 
-  Rename  `Java.Interop.ObjectManager` to  `Java.Interop.Runtime` .
-  Add  `Java.Interop.Runtime.MaxGlobalReferenceCount`  `Java.Interop.Runtime.GlobalReferenceCount`  `Java.Interop.Runtime.LocalReferenceCount` properties. These are for diagnostic purposes and should not be relied upon. 
-  `$(AndroidUseLatestPlatformSdk)` : new MSBuild property; if  `True` , cause the build process to use the latest (highest numbered) Android Platform SDK. [Infrastructure]


## Integrated Mono features/fixes

Based on [Mono 3.0.12](https://github.com/mono/mono/commit/616f6d21782d63e6a382d7f22fe7260aad6d547c).

-  OS X 10.9 support.
-  Fix race condition in  `System.Net.WebConnectionStream` .
-  Fix  `new BigInteger().GetHashCode()` to not throw.
-  Fix delegate combine when left side has already been invoked.
-   [10887](https://bugzilla.xamarin.com/show_bug.cgi?id=10887) : Handle shifts by multiple of 32 correctly. 
-   [11945](https://bugzilla.xamarin.com/show_bug.cgi?id=11945) : Better handle default value BigInteger. 


## Bug fixes

-  Fix preservation of  `AesCryptoServiceProvider` .
-  Add  `[Flags]` to various enumerations.
-  Generate  `XA42303` for  `[Activity(Name=".Foo")]` .
-   [5980](https://bugzilla.xamarin.com/show_bug.cgi?id=5980) : Marshal non- `Java.Lang.Object` types as  `java.lang.Object` . 
-   [7774](https://bugzilla.xamarin.com/show_bug.cgi?id=7774) : Date property for DatePicker 
-   [8353](https://bugzilla.xamarin.com/show_bug.cgi?id=8353) : Add UI for  `$(JavaHeapSize)` ,  `$(JavaOptions)` . 
-   [9800](https://bugzilla.xamarin.com/show_bug.cgi?id=9800) : Fix  `.axml` IntelliSense within Visual Studio. 
-   [10153](https://bugzilla.xamarin.com/show_bug.cgi?id=10153) ,  [10978](https://bugzilla.xamarin.com/show_bug.cgi?id=10978) : Add ability to set minimum Android SDK. 
-   [10865](https://bugzilla.xamarin.com/show_bug.cgi?id=10865) : Re-enable the "Bundle assemblies into native code" checkbox. 
-   [11170#c3](https://bugzilla.xamarin.com/show_bug.cgi?id=11170#c3) : Fail more gracefully with invalid resource files. 
-   [12254](https://bugzilla.xamarin.com/show_bug.cgi?id=12254) : Fix event de-registration involving  `Add` and  `Remove` methods. 
-   [12594](https://bugzilla.xamarin.com/show_bug.cgi?id=12594) : Fix the "Build failure, register the machine, build failure" loop. 


 <a name="11"></a>


 <a name="Xamarin.Android_4.7.11"></a>


#  [Xamarin.Android 4.7.11](#Xamarin.Android_4.7.11)

## Integrated Mono features/fixes

Based on [Mono 3.0.12](https://github.com/mono/mono/commit/ac11abe18d6847807e5dbc7ca16c1530bb0fc517).

-  Implement  `System.Net.Http.WebRequestHandler` .
-   [12457](https://bugzilla.xamarin.com/show_bug.cgi?id=12457) :  `X509Certificate2` is not marked as  `Serializable` . 
-   [12609](https://bugzilla.xamarin.com/show_bug.cgi?id=12609) : Runtime assert  `condition `mono_defaults.iunknown_class != 0' not met` . 
-   [12856](https://bugzilla.xamarin.com/show_bug.cgi?id=12856) : Fix  `MethodInfo::ToString()` to properly format generic structs 


## Bug fixes

-  Fixed regression in the GUI builder.
-   [Support Java to C# rectangular array marshaling](http://stackoverflow.com/questions/17305522/mono-for-android-binding-jagged-array) . 
-   [7953](https://bugzilla.xamarin.com/show_bug.cgi?id=7953) : Fix  `TimeZoneInfo` id lookup. 
-   [10693](https://bugzilla.xamarin.com/show_bug.cgi?id=10693) :  *Really* disable serialization assembly generation. 
-   [11918](https://bugzilla.xamarin.com/show_bug.cgi?id=11918) : Trial users don't get Fast Deployment support.
