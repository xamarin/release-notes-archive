---
id: 17775B8B-72E3-A191-2C55-F1AEE4AD4B00
title: "Mono for Android 4.1.0"
---

<a name="Installation" class="injected"></a>


# Installation

 **The 4.1.x series will be a series of alphas and betas leading up to the next big stable release, 4.2.**   
   
   
   
 **To see these updates, you have to switch to the Alpha channel in your IDE.**   
   
   
   
 **Visual Studio Users**: You should be prompted with
this update when you open a MFA project. You can also check manually in Tools
&gt; Options &gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="Draft_Documentation" class="injected"></a>


# Draft Documentation

In an effort to support developers trying out this release, we're releasing
draft versions of companion documentation for major features added in this
release. They can be downloaded as pdfs from the following links:

-   [Binding a Java Library](/guides/android/advanced_topics/binding-a-java-library/) - Describes how to use the new Java Library Binding project to create a Managed Callable Wrapper (Binding) for arbitray java libraries (jars). 
-   [API Metadata Reference](/guides/android/advanced_topics/binding-a-java-library/customizing-bindings/java-bindings-metadata/) - Companion documentation to the Binding a Java Library doc, this doc covers binding transformation file syntax. 
-   [Fragments Walkthrough](/guides/android/platform_features/fragments/fragments_walkthrough/) - Describes how to use fragments to reuse controls across different form factors. Also covers Android Compatibility Libraries to support fragments on older OS versions. 


 <a name="Changes_since_4.0.6" class="injected"></a>


# Changes since 4.0.6

 <a name="Java_Binding_Library_project_and_tool" class="injected"></a>


## Java Binding Library project and tool

In this release we introduced a new library generator tool that makes it
possible to bind existing Android Java library (.jar) to C# library (.dll). Now
you can consume external Java library from managed code.

This includes support for importing Android Library Project into managed
library, either via local library project description files (project.properties)
or archived bin files (.zip).

These new features are available in Visual Studio or MonoDevelop as a new
project type (Java Bindings Library project).

 [Java Binding Library tutorial](/guides/android/advanced_topics/java_integration_overview/binding_a_java_library_(.jar))

 <a name="Smaller_Shared_Runtime" class="injected"></a>


## Smaller Shared Runtime

The shared runtime needed is now about 50% smaller. This was accomplished by
splitting each architecture into it's own runtime and removing debug symbols for
Mono and the BCL. (Debug symbols for * **your*** code is
still used.) If you have a situation where debug symbols for Mono help you,
remove any existing shared runtime from your device, and turn on
" **Provide shared runtime debug symbols**" from **Tools-&gt;Options-&gt;Mono for Android**. Then re-deploy and full
debug symbols will be available.

 <a name="Visual_Studio_Integration_Enhancements" class="injected"></a>


## Visual Studio Integration Enhancements

 * **NOTE: If you are opening an existing MFA solution, you may need to set it to Deploy in Build -&gt; Configuration Manager.***

   


   


 <a name="Device_Toolbar" class="injected"></a>


### Device Toolbar

There is now a toolbar available that provides a dropdown list of all running
emulators and attached devices. This allows you to quickly set your default
device and avoid being prompted to choose your device for every run.

 ![](mono_for_android_4.1.0/Images/vs-refresh1.png)

The toolbar will remember your choice even if the device isn't available. For
example, you can set it to your phone, and it will switch to your phone every
time your phone is attached.

Choosing " **-- Prompt for Device --**" will utilize the current
behavior of prompting you on each run.

 <a name="Non-modal_Deployment" class="injected"></a>


### Non-modal Deployment

Deploying to an emulator/device no longer blocks your work. Deployment is now
done in the background, with updates displayed in the status bar. Deployment can
be cancelled via **Build-&gt;Cancel**, and should now cancel
immediately if requested.

 ![](mono_for_android_4.1.0/Images/vs-refresh2.png)

Which projects will be deployed follows the same model as Windows Phone 7,
and can be configured via the **Deploy** checkbox in **Build -&gt; Configuration Manager**.

 ![](mono_for_android_4.1.0/Images/vs-refresh4.png)

 <a name="Integrated_Logcat" class="injected"></a>


### Integrated Logcat

When running in **Debug** mode, Visual Studio will now
automatically attach to the device's logcat and display the results in the
Output pane. Many types of logging and exceptions may only show up in logcat.
Now they appear automatically instead of being another place to remember to
check.

 ![](mono_for_android_4.1.0/Images/vs-refresh3.png)

 <a name="Other_Improvements" class="injected"></a>


### Other Improvements

-  Additional parameters can be passed to emaulators started in Visual Studio: -    **Tools-&gt;Options-&gt;Mono for Android-&gt;Additional Emulator Launch Arguments**  


 
-  Project templates for Honeycomb/Ice Cream Sandwich applications.
-  Item template for a Fragment file.


 <a name="MonoDevelop_Improvements" class="injected"></a>


## MonoDevelop Improvements

-  Project templates for Honeycomb/Ice Cream Sandwich applications.
-  Item template for a Fragment file.
-  MonoDevelop got "Publish Android Application" signing wizard that lets you sign the application package (.apk) and get ready to publish to Google Play (formerly Android Market). 


 <a name="API_Improvements" class="injected"></a>


## API Improvements

 <a name="API_Level_15_support" class="injected"></a>


### API Level 15 support

This release contains support for API Level 15 (updated Ice Cream Sandwich
API).

 <a name="Almost_complete_enum_migration" class="injected"></a>


### Almost complete enum migration

Our API conversion from classic int constants to decent enum has always been
incomplete and changes were based on feedback. This time we took time to review
the entire API and introduced a lot of new enums, as well as fixed method
parameters and return values from int to enum.

Since this brings a lot of API breakage, we also introduced some transitive
fields whose name match the old int-based fields (with ObsoletedAttribute) for
soften application upgrades.

 <a name="Android_Compatibility_Library_binding" class="injected"></a>


### Android Compatibility Library binding

As we have received many requests for this, this release contains bindings
for Android compatibility library that brings Fragments, ViewPager and many
other useful stuff from Honeycomb to old Android platform.

 <a name="Exporting_arbitrary_Java_member_for_better_Java_integration" class="injected"></a>


### Exporting arbitrary Java member for better Java integration

It is now easier to export methods for invocation and fields for access by
Java. The new Mono.Android.Export.dll assembly allows using the new [Export]
custom attribute so that methods will be declared on the generated Android
Callable Wrapper, and the new [ExportField] custom attribute allows fields to be
declared in the generated Android Callable Wrapper.

These remove a couple of limitations in Mono for Android limitations:

-  You can implement Java.IO.ISerializable interface in managed code, as it is possible to give "readObject" and "writeObject" names in Java (Android Callable Wrapper) code. 
-  You can implement Android.OS.IParcelable interface in managed code, as it is possible to export CREATOR field explicitly. 
-  You can use android:onClick attribute to pass a Java method name as a click handler, as it is possible to export arbitrary managed method in Java code, unlike non-export methods which are ignored in Java. 


 <a name="Dynamic_support" class="injected"></a>


### Dynamic support

In this release, we added DLR support which also enables C# 4.0 dynamic
support. System.Core.dll is expanded to include them, and Microsoft.CSharp.dll
and Mono.CSharp.dll joined the framework assemblies party.

(Note that there is some [limitation](/guides/android/advanced_topics/limitations) on using dynamic types to
interoperate with Java code and the underlying dalvik runtime.)

 <a name="Instrumentation_support" class="injected"></a>


### Instrumentation support

In this release, we changed the bootstrap hook to initialize mono runtime to
support Instrumentation aside from existing ordinal applications. This means now
you can write your Instrumentation and start it from adb shell commands.

 <a name="Java_annotations_and_managed_attributes" class="injected"></a>


### Java annotations and managed attributes

This release supports generating managed attributes from Java annotations.
For example, we create Java.Lang.DeprecatedAttribute from java.lang.Deprecated
annotation type. This is achieved by new AnnotationAttribute
(Java.Lang.DeprecatedAttribute class has this managed attrubute).

When these annotation attributes were used in managed code, our build process
generates corresponding Java annotation in the Java code (Android Callable
Wrapper).

 <a name=".NET_names_can_now_be_used_in_Resource_XML" class="injected"></a>


### .NET names can now be used in Resource XML

In previous releases, when writing a Resource XML file that referenced a
managed class, the Java name of the Android Callable Wrapper had to be used. For
example, the [GLCube Resources\Layout\main.xml](https://github.com/xamarin/monodroid-samples/blob/master/GLCube/Resources/layout/main.xml#L21) file uses the *&lt;mono.samples.glcube.PaintingView/&gt;* element to refer to the [Mono.Samples.GLCube.PaingintView type](https://github.com/xamarin/monodroid-samples/blob/master/GLCube/PaintingView.cs#L16). Starting in this
release, the fully-qualified managed name can be used, resulting in *&lt;Mono.Samples.GLCube.PaintingView/&gt;*. Android v4.0 Fragments may
also use the fully-qualified managed name instead of the Android Callable
Wrapper Java name.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

-  IJavaObject now implements IDisposable
-  int to enum changes


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-  Java library binding assemblies will now register the Java package to C# type mapping during process startup. This allows  [Activity.FindViewById(int)](http://androidapi.xamarin.com/?link=M:Android.App.Activity.FindViewById) to e.g. return a  [MapView](http://androidapi.xamarin.com/?link=T:Android.GoogleMaps.MapView) instead of a  *ViewGroupInvoker* . 
-  GC fixes: TODO description regarding null handle check in libmonodroid, removal of JLO fields from Framework Peers 
-  Better gref behavior when using  *foreach* over  [Android.Runtime.JavaList](http://androidapi.xamarin.com/?link=T:Android.Runtime.JavaList) and related collection types. 
-   [Android.App.Application.SynchronizationContext](http://androidapi.xamarin.com/?link=P:Android.App.Application.SynchronizationContext) is now thread-aware, so that it won't deadlock when trying to  [Send()](http://androidapi.xamarin.com/?link=M%3aSystem.Threading.SynchronizationContext.Send(System.Threading.SendOrPostCallback%2cSystem.Object)) a message when already on the UI thread. 
-  Android Callable Wrappers no longer emit  *@Override* . This is to avoid the  [unmitigated evil that is declaring a custom Override annotation](http://stackoverflow.com/questions/9376142/mono-for-android-webview-input-field-filechooser-doesnt-work/9388508#9388508) . (Granted,  *[Export]* is a much better fix, but there's not any actual need for  *@Override* in the Android Callable Wrappers...) 
-  Java.Lang.Object coercion operators now null-check their parameters, so implicitly converting a  *null*  *System.String* to a  *Java.Lang.Object* now returns  *null* instead of throwing an exception. 
-  Application startup now performs a zipalign check to ensure that zipalign was run before installing the .apk. This helps reduce a source of really bizarre and obscure errors due to unaligned assemblies. 
-  System.Data.Services.Client now contains string resources. Exception messages should actually be useful now. 
-  NTLM authentication fixes: set the correct flags when the domain is not set. Allow  *domain\user* and  *domain/user* as the user name and set domain and user accordingly. 
-   [382](https://bugzilla.xamarin.com/show_bug.cgi?id=382) : Add [Export] support to mandroid. 
-   [638](https://bugzilla.xamarin.com/show_bug.cgi?id=638) : invalid format string when loading into a datatable records from the sqlite db where they have datetime fields with null values. 
-   [645:](https://bugzilla.xamarin.com/show_bug.cgi?id=645) : M4A should allow missing library at build/run steps. 
-   [795](https://bugzilla.xamarin.com/show_bug.cgi?id=795) : System.MethodAccessException when creating generic class. 
-   [981](https://bugzilla.xamarin.com/show_bug.cgi?id=981) : sbyte.Parse, short.Parse raise OverflowException when parsing hexadecimal negative numbers. 
-   [1164](https://bugzilla.xamarin.com/show_bug.cgi?id=1164) :  <span>TargetInvocationException / SerializationException
    on response from a web service (which works on MonoTouch).</span> 
-   [1416](https://bugzilla.xamarin.com/show_bug.cgi?id=1416) : Linker in 1.9.1 removing override methods? 
-   [1437](https://bugzilla.xamarin.com/show_bug.cgi?id=1437) : WCF FaultException&lt;TDetail&gt; support missing. 
-   [2190](https://bugzilla.xamarin.com/show_bug.cgi?id=2190) : sdb interrupt code not signal safe. 
-   [2191](https://bugzilla.xamarin.com/show_bug.cgi?id=2191) : SqliteDataReader throws on GetDecimal() 
-   [2769](https://bugzilla.xamarin.com/show_bug.cgi?id=2769) : System.Core does not include Task.Unwrap() 
-   [2775](https://bugzilla.xamarin.com/show_bug.cgi?id=2775) : Debugger tooltips for DateTimes are corrupted 
-   [2483](https://bugzilla.xamarin.com/show_bug.cgi?id=2483) : Calling CancelAsync when using DownloadDataAsync causes System.Threading.ThreadInterruptedException: Thread interrupted 
-   [2843](https://bugzilla.xamarin.com/show_bug.cgi?id=2843) : WCF: SerializationException when processing response that contains a nullable enum 
-   [2859](https://bugzilla.xamarin.com/show_bug.cgi?id=2859) : WCF: SerializationException trying to process FaultException 
-   [2926](https://bugzilla.xamarin.com/show_bug.cgi?id=2926) : DataTable.ImportRow causes InvalidCastException 
-   [2936](https://bugzilla.xamarin.com/show_bug.cgi?id=2936) : DateTime.FromFileTimeUTC has incorrect Kind set 
-   [3100](https://bugzilla.xamarin.com/show_bug.cgi?id=3100) : Error With System.Net.WebClient.UploadProgressChanged Event 
-   [3137](https://bugzilla.xamarin.com/show_bug.cgi?id=3137) : german country code creates a floating-point number problem 
-   [3476](https://bugzilla.xamarin.com/show_bug.cgi?id=3476) : culture-data return wrong values 
-   [3479](https://bugzilla.xamarin.com/show_bug.cgi?id=3479) : All linked assemblies need to check for IJavaObject 
-   [3497:](https://bugzilla.xamarin.com/show_bug.cgi?id=3497) : Package building step uses excessive memory that then is not GCed 
-   [3500:](https://bugzilla.xamarin.com/show_bug.cgi?id=3500) : Bindings generator crashes on Parse .jar 
-   [3634](https://bugzilla.xamarin.com/show_bug.cgi?id=3634) : XElement with decimal date get formatted has wrong ToString representation 
-   [3827](https://bugzilla.xamarin.com/show_bug.cgi?id=3827) : SortedSet missing from System.dll 
-   [3876](https://bugzilla.xamarin.com/show_bug.cgi?id=3876) : HttpWebRequest chunked reading problem 
-   [3894](https://bugzilla.xamarin.com/show_bug.cgi?id=3894) : Async HttpWebRequest with NTLM authentication does not auto redirect when a 301/303 response received 
-   [4040:](https://bugzilla.xamarin.com/show_bug.cgi?id=4040) : System.ArgumentException when inheriting AsyncTask&lt;,,&gt; and overriding RunInBackground but not DoInBackground 


 <a name="Warnings:" class="injected"></a>


# Warnings:

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
