---
id: B873CFAC-1C1C-58AE-737B-F6A1431A922E
title: "Xamarin.iOS 6.3"
---

The Xamarin.iOS 6.3 series contains the upgrade of the Mono
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

 **iOS Batch Compiler Improvements:**

 On iOS we now generate
	“shareable code” for value types, a truly revolutionary
	innovation in code generation technology. In practical terms
	this means that a whole range of code that previously crashed
	with a “Attempting to JIT compile method” now works. While we
	still provide the high-performance, and fine-tuned generic
	code that we can infer –for example direct calls to a method
	Foo&lt;T&gt;(T x)– we generate a value-type shared version of
	Foo&lt;T&gt;(T x) that can be used in dynamic cases that previously
	failed. What was once a dream, is now a reality.

We call this "Generic Value Type Sharing" and it is an
	option enabled by default.  If you do not need this
	functionality, you can reduce your executable size by
	disabling this optimization by passing the "-O=-gsharedvt"
	option to the "extra mtouch arguments" in the IDE.

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
	have to be adjusted. <a name="8">
<h1><a href="#8">Xamarin.iOS 6.3.8</a></h1>

<h3>New features</h3>
<ul>
  <li>Add support for dispatch_set_target_queue [#12591]</li>
</ul>

<h3>Bug fixes</h3>
<ul>
  <li>Properly install and update MonoTouchActivation.app [#10565]</li>
  <li>Always use OldDynamic for simulator [#11934]</li>
  <li>Avoid passing class pointers to some marshal icalls since its not AOT compatible [#12595]</li>
  <li>Fix encoding (Windows) file paths so gcc can process them [#13050] </li>
  <li>Fix implicit Uri to NSUrl conversion and add unit tests [#13069]</li>
  <li>Fix for natively linking large applications [#13097]</li>
  <li>Fix case where Subviews can be null [#13119]</li>
  <li>Add back arm-darwin-mono since MD, XS and VS depends on its presence [#13172]</li>
  <li>Fix LLVM not to assert on an assembly without methods [#13178]</li>
  <li>Fix Touch.Unit execution duration scale</li>
</ul>




 <a name="7">
<h1><a href="#7">Xamarin iOS 6.3.7</a></h1>

	<p>This release contains many improvements and bug fixes:

<h3>New Features</h3>

	<p>New in this release:

	<ul>
		<li><b>Revamped Build System:</b> Major improvements
		to the build process in mtouch.  Every partial build
		product is now cached in order to rebuild as little as
		possible. This results in significant speed gains when
		doing rebuilds - depending on what has been modified
		in a project, a build/deploy/run cycle on device can
		be over twice as fast as previously.

		</li><li><b>Incremental Builds/Uploads:</b> When using the
		mtouch argument <tt>--fastdev</tt> and turning off
		linking, we will now only compile the assemblies that
		were modified, and only upload the delta.  Notice that
		when using incremental builds, the resulting
		binary <b>must be connected to your Mac</b>.
		Binaries compiled with the incremental support are not
		able to run when your device is unplugged.

		</li><li><b>Added PCL support and facade assemblies</b>:   This
		means that MonoTouch can now consume any PCL libraries
		that you created elsewhere (modulo the usual iOS and
		Mono limitations: no dynamic code generation, and
		limited WCF support).

		</li><li><b>Generic Code Sharing Improvements:</b> no
		longer has a limit on the size of value types.  Now,
		in addition to the type-specific generic methods, the
		general purpose fallback generic code will work with
		any value type size. Generic  sharing now supports Nullable.Box and
		Unbox to be compiled.

		</li><li><b>Position Independent Executables (PIE):</b>
		Native executable are now Position Independent
		Executable by default.

		</li><li><b>F#:</b> FSharpCode.dll is now "blessed" and
		does not count on the 64KB limit for the Starter
		edition.

		</li><li><b>Updated Touch.Unit:</b> Now with support for
		testing async methods:
		<ul>
			<li>Add back the device UDID inside the logs
			<li>Add the locale identifier inside the logs
			<li>Updated to NUnitLite 0.9
		</li></li></li></ul>

<h3>Optimizations</h3>

	<p>Size optimizations, reducing your binary size:

	<ul>
		<li>Using SSL/TLS requires much less code than before,
		leading to smaller native executables

		<li>The use of StartWWAN (implicit for
		System.Net.WebConnection) does not require reflection
		anymore
	</li></li></ul>

<h3>Bug fixes</h3>

	<p>The most notable bug fixes in this release include:

	<ul>
		<li>Make WebClient report an error when the download
		aborted prematurely [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=3904">#3904</a>]
		<li>Do not construct a Selector directly if we want it
		to return null when unassigned [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=10876">#10876</a>]
		<li>Improve InvalidCastException to include the ObjC
		type name and the name of the managed method [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12518">#12518</a>]
		<li>Properly fetch handle from INativeObject instances
		[<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12531">#12531</a>]
		<li>Fix empty BigInteger with more than one 0x0 byte
		[<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12579">#12579</a>]
		<li>Fix proxy issue switching from 3G and Wifi [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12640">#12640</a>]
		<li>Fix to avoid using SlowGetIntPtr for events and
		use __Internal when producing 3rd party bindings [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12707">#12707</a>]
		<li>Fix pinvoke symbol name for CGPath.EllipseFromRect
		[<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12712">#12712</a>]
		<li>Fix synchronized wrappers of generic methods [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12727">#12727</a>]
		<li>Emit DWARF line numbers info using .file/.loc
		assembler directives on OS X [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12731">#12731</a>]
		<li>Fix register allocation for hw remainder opcodes
		on armv7s [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12741">#12741</a>]
		<li>Remove methods from UIImage that don't actually
		exist on UIImage [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12803">#12803</a>]
		<li>Fix an issue where LLVM and clang could not
		compile a project [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12805">#12805</a>]
		<li>Override RespondsToSelector instead of registering
		the selector another time [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12833">#12833</a>]
		<li>Disable the parameter type check when marshalling
		from ObjC to managed
		[<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12834">#12834</a>][<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=13006">#13006</a>]
		<li>Do not enable PIE automatically when deployment
		target &lt; 4.2 [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12840">#12840</a>]
		<li>Do not retain retained result of CopyPixelBuffer
		[<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12846">#12846</a>]
		<li>Fixed AVPlayerItem.Options return type [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12847">#12847</a>]
		<li>Fixes to use the clang compiler
		[<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12941">#12941</a>][<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12723c2">#12723c2</a>]
		<li>AOT compiler moved read-only data into a separate
		section [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=13005">#13005</a>]
		<li>Add missing NSUserDefaults fields as requested in http://forums.xamarin.com/discussion/comment/18488
		<li>and several other bug fixes filled against Mono 3.0
	</li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></ul>

<a name="6">
<h1><a href="#6">Xamarin iOS 6.3.6</a></h1>
<p>
  The 6.3.6 beta release contains all enhancements and bug fixes
  released with 6.2.7 (stable).
</p>
<h3>New features</h3>

	<ul>
		<li>ARMV7S support for hardware division with LLVM
		<br>When building for ARMv7s, MonoTouch will now
		generate the code necessary to use the hardware
		instructions for division and remainder operations.
		This feature is only enabled when compiling with LLVM.
		</li>
		<li>Support for Position Independent Executables (PIE)</li>
		<li>Smaller executables - Partial Sharing Support
		<br>
		  Usually our compiler shares the code for generic instantiations of
		  reference types (List&lt;object&gt; and List&lt;string&gt; share the same
		  code), and now it is able to do this when value types are involved
		  (Dictionary&lt;object,int&gt; and Dictionary&lt;string,int&gt;) this helps
		  reduce the size of executables.
		<br>
		  Since our new Generic Value Type Sharing code
		  increased the size of executables compared to the
		  6.2.xx series, this optimization reduces the code
		  generated by 30%-40% on those cases.
		</li>
		<li>New bindings for the Foundation types NSOrderedSet and NSMutableOrderedSet</li>
		<li>More strongly typed dictionaries for
		CoreBluetooth's CBCentralManager [#11743]</li>
		<li>X509Certificate now supports SHA2 and RIPEMD160 [#12303][#11703]</li>
		<li>mtouch now supports --listapps to list apps installed on a device</li>
		<li>Touch.Unit server now supports --devname to select a specific device</li>
		<li>UIDevice.UniqueIdentifier now returns String.Empty since the selector is now blacklisted by Apple</li>
	</ul>

<h3>Bug fixes</h3>
	<ul>
		<li>Fix disposal of EAGLContext and GraphicsContext to avoid exceptions [#12212]</li>
		<li>Fix SetLineDash to allow null values [#12291]</li>
		<li>Add a specific error message if no SDK version is specified when using mtouch on the command-line [#12305]</li>
		<li>Avoid the class name check in is_async_state_machine_class (), csc seems to generate a different name [#12329]</li>
		<li>Add missing [NullAllowed] on AVAssetReaderVideoCompositionOutput constructors [#12360]</li>
		<li>OpenTK's GL.DeleteTexture missing uint overload [#12401]</li>
		<li>Use a different function for emitting write barriers for gsharedvt types which can handle reference types too [#12429]</li>
		<li>Do not use the /usr/bin/mono-cil-strip script [#12459]</li>
		<li>UIImage.AsJPEG and AsPNG are thread-safe [#12472]</li>
		<li>Keep the exception object alive during debugger suspensions [#12494]</li>
		<li>Multiple bug reports for AOT limitations were closed</li>
		<li>Fix VS.NET support for Xcode 4.6.2 with non-English locale</li>
		<li>Fix AddressBook constants to work without authorization (iOS6+)</li>
		<li>Fix removal of static libraries and resources from assemblies (too large IPA sizes)</li>
	</ul>

</a><a name="5">
<h1><a href="#5">Xamarin iOS 6.3.5</a></h1>

	<p>Improved the new Generic ValueType Sharing
	(</a><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=11933">#11933</a>).

	<p>New MonoTouch.Dialog copes with C# upgrade to support
	covariance and contravariance.

	<p>Changes that reduce binary sizes:
	<ul>
		<li>Runtime dead code elimination, 4-8k in savings.

		<li>The linker now removes all serialization
		constructors if the application does not create any
		SerializationInfo instances.  This reduces an
		application like "Hello World" by about 110kb.
	</li></li></ul>

	<p>Fixes since the last release:
	<ul>
		<li>Multiple debugger fixes.
		<li>Fixes linking of assemblies with resources or
		static libraries.
		(<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=11676">#11676</a>,
		<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=11700">#11700</a>).
		<li>Fixes issues related to thread cleanup and
		shutdown.
		<li>Fixed LLVM support on Lion.
		<li>Resolved an SGen/threading interaction bug that
		prevented AVCaptureVideoDataOutputSampleBufferDelegate
		and CoreBluetooth from working
		(<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=11732">#11732</a>,
		<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=11836">#11836</a>).
		<li>Fixed CAKeyFrameAnimation.FromKeyPath and
		CFRelease pinvoke signatures.
	</li></li></li></li></li></li></ul>

<a name="4"></a>
<a name="Xamarin.iOS_6.3.4"></a>
<h1><a href="#Xamarin.iOS_6.3.4">Xamarin.iOS 6.3.4</a></h1>
       <p>CFNetwork handler for HttpClient</p>
       <p>Multiple issues fixed in the AOT compiler with LLVM</p>
       <p>Multiple issues fixed in the linker</p>
       <p>Xamarin.iOS assemblies are now built with optimization enabled.</p>
       <p>
         Fixed compatibility issue between MonoTouch.Dialog and the
         new 4.5 based BCL. It previously would fail to compile
         existing code due to changes in IEnumerable.
       </p>

<a name="3"></a>
<a name="Xamarin.iOS_6.3.3"></a>
<h1><a href="#Xamarin.iOS_6.3.3">Xamarin.iOS 6.3.3</a></h1>
       <p>
         Major performance improvement on AudioToolbox. Previously it was not
         fast enough to use on the iPhone4 and now it should work just fine.
       </p>

       <p>Multiple fixes to the AOT compiler involving generics and async.</p>

       <p>Fixed a few bugs in the C# compiler regarding async.</p>

       <p>
         Multiple performance improvements in genetics code involving
         delegates or array allocation.
       </p>

       <p>Add more generic overloads for subclasses of
       UICollectionViewLayoutAttributes</p>

       <p>Reduced the number of thread roundtrips that
       HttpClientHandler does in some cases.</p>

       <p>Optimized integer division and modulus by some constants under LLVM.</p>

       <p>Optimized Marshal code that read/write from native memory.</p>

       <p>Fixed multiple bugs in culture handling and date parsing.</p>

       <p>Introduced async versions of multiple iOS APIs.</p>

<a name="2"></a>
<a name="Xamarin.iOS_6.3.2"></a>
<h1><a href="#Xamarin.iOS_6.3.2">Xamarin.iOS 6.3.2</a></h1>

	<p>Optimized LINQ with arrays.</p>

        <p>Multiple fixes for mscorlib linking.</p>

        <p>Sgen can now return memory to the OS on 32bits systems.</p>

        <p>Multiple improvements in the linker to produce smaller binaries.</p>

        <p>Fix multiple crashers in the AOT compiler.</p>

        <p>Fix AOT compilation of async generic methods.</p>

<a name="1"></a>
<a name="Xamarin.iOS_6.3.1"></a>
<h1><a href="#Xamarin.iOS_6.3.1">Xamarin.iOS 6.3.1</a></h1>

	<p>
          Improve performance of some string copying, object cloning
	  and boxing.
        </p>

        <p>
          Removed internal code for unsupported capabilities of the
          framework. This further reduces binary sizes.
        </p>

        <p>Fixed some culture related bugs.</p>

<a name="0"></a>
<a name="Xamarin.iOS_6.3.0"></a>
<h1><a href="#Xamarin.iOS_6.3.0">Xamarin.iOS 6.3.0</a></h1>

	<p>First release of the Mono 3.0-based stack.</p>

        <p>
          The product is now based on mono 3.0. This includes C# 5
          with async, two years of improvements in the runtime and
          class libs.
        </p>

        <p>
          The class libs are now based on top of .NET 4.5 bringing in
          a lot of improvements. Some core generic interfaces are now
          using covariance.
        </p>
</li></ul>
</a>
