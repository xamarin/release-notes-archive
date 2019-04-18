---
id: B873CFAC-1C1C-58AE-737B-F6A1431A922E
title: "Xamarin.iOS 6.4"
---

# Xamarin.iOS 6.4



The Xamarin.iOS 6.4 **stable**

 series is the result of months
	of hard work on Xamarin.iOS and years of works on Mono 3 runtime,
	tools and class libraries.### Mono 3 based



Xamarin.iOS 6.4 includes the Mono 3 runtime engine with advanced
	features like the latest C# and async programming.

First-class support for asynchronicity is a powerful and
	brilliantly simple language tool.

It makes it easy to write responsive user interfaces, which
	in turn makes for delighted users. It makes complex workflows,
	with their error handling, natural to write. This translates
	into proper error messages and proper program recovery; and
	finally by letting the compiler do the work for you, it
	eliminates bugs from your code, and enables you to enjoy your
	work and focus on what really matters for your application.
	This is best seen by watching it in action. See how error
	handling and dealing with the UI thread go from painful to
	trivial.

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

 **Variance and Contravariance:**

 With the upgrade to our class
	libraries, we have introduced support for variance and
	contravariance in the core types. While this change enables a
	whole class of new code to be written, it also means that some
	old code that was not covariant/contravariance friendly will
	have to be adjusted.

 **F# support:**

 FSharpCore.dll is now shipped. This is a *blessed*

 assembly (like other SDK assemblies) and will
	not be considered against the 64KB limit for the Starter edition.### iOS specific enhancements



 **Position Independent Executables (PIE):**


	Native executable are now Position Independent
	Executable by default.

 **iOS Batch Compiler Improvements:**

 On iOS we now generate
	“shareable code” for value types, a truly revolutionary
	innovation in code generation technology. In practical terms
	this means that a whole range of code that previously crashed
	with a “Attempting to JIT compile method” now works. While we
	still provide the high-performance, and fine-tuned generic
	code that we can infer –for example direct calls to a method <tt>Foo&lt;T&gt;(T x)</tt>

– we generate a value-type shared version of <tt>Foo&lt;T&gt;(T x)</tt>

 that can be used in dynamic cases that previously
	failed. What was once a dream, is now a reality.

We call this "Generic Value Type Sharing" and it is an
	option enabled by default.  If you do not need this
	functionality, you can reduce your executable size by
	disabling this optimization by passing the <tt>-O=-gsharedvt</tt>


	option to the "extra mtouch arguments" in the IDE.

 **MonoTouch.Dialog**

 was updated to support C#
	covariance and contravariance. **CFNetwork-backed handler for HttpClient**

### Tools enhancements



 **Added PCL support and facade assemblies**

: This
	means that Xamarin.iOS can now consume any PCL libraries
	that you created elsewhere (modulo the usual iOS and
	Mono limitations: no dynamic code generation, and
	limited WCF support).

 **Revamped Build System:**

 Major improvements
	to the build process in mtouch.  Every partial build
	product is now cached in order to rebuild as little as
	possible. This results in significant speed gains when
	doing rebuilds - depending on what has been modified
	in a project, a build/deploy/run cycle on device can
	be over twice as fast as previously.

 **Incremental Builds/Uploads:**

 When using the
	mtouch argument <tt>--fastdev</tt>

 and turning off
	linking, we will now only compile the assemblies that
	were modified, and only upload the delta.  Notice that
	when using incremental builds, the resulting
	binary **must be connected to your Mac**

.
	Binaries compiled with the incremental support are not
	able to run when your device is unplugged.

 **Debugging Upgrades:**

 Our debugger has received a lots of small
	improvements and fixes, they add up and you will notice how
	all the small details now work more smoothly than before.

 **Updated Touch.Unit:**

 Now with support for
	testing async methods using the latest NUnitLite 0.9### Optimizations

 **Performance:** Beside all the advantages of Mono 3.0
	some iOS specific performance optimizations are now available:-  ARMv7S support for hardware division with LLVM    
 When building for ARMv7s, Xamarin.iOS will now generate the code necessary to use the hardware instructions for division and remainder operations. This feature is only enabled when compiling with LLVM. 
-  Improve performance of some string copying, object cloning and boxing. 
-  Major performance improvement on AudioToolbox. Previously it was not fast enough to use on the iPhone4 and now it should work just fine. 
-  Removal of reflection usage for  <tt>StartWWAN</tt> (implicit for  <tt>System.Net.WebConnection</tt> ),  <tt>TimeZone</tt> and accessing the current locale. 


 **Size:** A lot of work was done to ensure all the new
	features did not come at the expense of larger applications.-  An "Hello World" application is now less than 3MB, 12% smaller than 6.2.x.  
-  Partial Sharing Support    
 Usually our compiler shares the code for generic instantiations of reference types ( <tt>List&lt;object&gt;</tt> and  <tt>List&lt;string&gt;</tt> share the same code), and now it is able to do this when value types are involved ( <tt>Dictionary&lt;object,int&gt;</tt> and  <tt>Dictionary&lt;string,int&gt;</tt> ) this helps reduce the size of executables.    
 Since our new Generic Value Type Sharing code increased the size of executables compared to the 6.2.xx series, this optimization reduces the code generated by 30%-40% on those cases. 
-  Using SSL/TLS requires much less code than before, leading to (up to 20%) smaller native executables; 
-  The linker now removes all serialization constructors if the application does not create any SerializationInfo instances. 
-  Removed internal code for unsupported capabilities of the framework. This further reduces binary sizes. 


 <a name="5">
    <h1><a href="#4">Xamarin.iOS 6.4.5</a></h1>
    Xamarin.iOS 6.4.5 is a hotfix release.

    <h3>Bug Fixes:</h3>
    <ul>
      <li>Fix a nullref when casting a null object to a complex type when using --debug=casts. [#14552/#14493]</li>
    </ul>

  
 <a name="4">
    <h1><a href="#4">Xamarin.iOS 6.4.4</a></h1>
    Xamarin.iOS 6.4.4 is a hotfix release.

    <h3>New Features:</h3>
    <ul>
      <li>Additional CoreBluetooth convenience API to ease development</li>
      <li>Several missing [Since] attributes were added on existing API</li>
    </ul>

    <h3>Bug Fixes:</h3>
    <ul>
      <li>AOT Add support for constrained gsharedvt calls which return a reference value [#13030]</li>
      <li>Fix linker when PCL assemblies are used only for their [TypeForwardedTo] attributes [#13488]</li>
      <li>CBPeripheralManager.UpdateValue allow null for its subscribedCentrals argument [#13530]</li>
      <li>Fix leaks in CGImageDestination creation [#13671]</li>
      <li>Add alternative to deprecated (6.0) UILabel.MinimumFontSize API [#13904]</li>
      <li>Reload debugging symbols (if required) after reloading an assembly [#13913]</li>
      <li>Fix for the return value type of CVPixelFormatDescription.AllTypes [#13917]</li>
      <li>Use the invariant Calendar if the exact one is not available [#13977]</li>
      <li>Added missing method FromContext for 'contextWithEAGLContext:options:' selector [#13983]</li>
      <li>Linker will not remove [ParamArray] attribute [#14165]</li>
      <li>Fixed [#14194]</li>
      <li>Also includes several fixes and enhancements made to Mono 3.2.x</li>
    </ul>

  
 <a name="3">
    <h1><a href="#3">Xamarin.iOS 6.4.3</a></h1>
     
    Xamarin.iOS 6.4.3 is a hotfix release.
     
    <h3>Bug fixes</h3>  
    <ul>
      <li>Crash with NSObject.InvokeInBackground [#13612].</li>
      <li>Could not AOT the assembly MicrosoftWindowsAzureMobileServices.dll [#13191].</li>
    </ul>
     
	<p>There are no API changes in this release.</p>

  
 <a name="2">
    <h1><a href="#2">Xamarin.iOS 6.4.2</a></h1>
     
    Xamarin.iOS 6.4.2 is a hotfix release.
     
    <h3>Bug fixes</h3>  
    <ul>
      <li>Extraneous invalid cast exceptions [#13518]</li>
      <li>LLVM fails when project has spaces in its path [#13603]</li>
      <li>UTType.GIF returns Pict instead of Gif. Pict is missing. [#13628]</li>
      <li>Resources generated from RESX files no longer copied to IPA packages [#13665]</li>
      <li>CGImageDestination leaks the Handle, creating a memory leak [#13671]</li>
      <li>NSDictionary.FromObjectsAndKeys(Object [] objects, NSObject [] keys, int count) ignores the "count" parameter [#13680]</li>
      <li>LLVM conflicts with Task.Run [#13734]</li>
      <li>Don't strip a cached binary (it was done the first time).</li>
      <li>Fix enum->int unbox casts in gsharedvt code.</li>
      <li>Link with each binding library's linker flags even with fastdev enabled.</li>
      <li>Update CFNetworkHandler to support concurrent requests.</li>
    </ul>
     
    <h3>API Changes</h3>
     
    <p>For a detailed list of the changes in the API, see our document 
    
 [API changes from 6.4.1 to 6.4.2](/releases/ios/api_changes/from_6.4.1_to_6.4.2).

 <a name="1">
<h1><a href="#1">Xamarin.iOS 6.4.1</a></h1>
 
Xamarin.iOS 6.4.1 is a hotfix release.

<h3>Bug fixes</h3>	
<ul>
<li>Json serialization with ServiceStack throws NRE on device [#13341]</li>
<li>Stack overflock in CultureInfo with region set to zh_TW [#13509]</li>
<li>DllNotFoundException when instantiating a GLKViewController subclass [#13512]</li>
<li>Don't assume property accessors (in IL) start with "get_" or "set_" [#13520]</li>
<li>User unable to deploy application on Device on Build Host using iOS for VS [#13050]</li>
</ul>

<p>There are no API changes in this release.</p>


 <a name="8">
<h1><a href="#8">Xamarin.iOS 6.4.0</a></h1>

<h3>API Changes</h3>

<p>For a detailed list of the changes in the API, see our document 

 [API changes from 6.2.7 to 6.4.0](/releases/ios/api_changes/from_6.2.7_to_6.4.0). There is no change between 6.4.0 and 6.3.8.

### Bug fixes



Consult the [6.3.x release notes](/releases/ios/xamarin.ios_6/xamarin.ios_6.3)

 to see the
list of bug fixes made between this release and the last 6.2 stable release
