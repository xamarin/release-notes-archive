---
id: 8B63B9CD-79F1-ED9B-5E88-1C90FA546A9D
title: "Mono For Android 4.2.2"
---

<a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 3.0.

 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-  Provide additional context when an  [Android Callable Wrapper](/guides/android/advanced_topics/java_integration_overview/android_callable_wrappers) cannot be generated ( [Email thread](http://lists.ximian.com/pipermail/monodroid/2012-May/010280.html) ). 
-  Improve marshaling of Java builtin types. ( [Email thread](http://lists.ximian.com/pipermail/monodroid/2012-May/010406.html) ) 
-  Reduce lifetime of wrapped  [Stream](http://androidapi.xamarin.com/?link=T:System.IO.Stream) s in  [InputStreamAdapter](http://androidapi.xamarin.com/?link=T:Android.Runtime.InputStreamAdapter) ,  [InputStreamInvoker](http://androidapi.xamarin.com/?link=T:Android.Runtime.InputStreamInvoker) ,  [OutputStreamAdapter](http://androidapi.xamarin.com/?link=T:Android.Runtime.OutputStreamAdapter) ,  [OutputStreamInvoker](http://androidapi.xamarin.com/?link=T:Android.Runtime.OutputStreamInvoker) . Disposing of the wrapper instance will now dispose the wrapped instance. 
-  Don't generate a NullReferenceException in a .jar binding project if there are no types to bind. 
-   [992](https://bugzilla.xamarin.com/show_bug.cgi?id=992) :  <span><span>DateTime.ParseExact disregards valid format
    string.</span></span> 
-   [2564](https://bugzilla.xamarin.com/show_bug.cgi?id=2564) :  <span><span>XNamespace not matched
    correctly</span></span> 
-   [3258](https://bugzilla.xamarin.com/show_bug.cgi?id=3258) :  <span><span>Serialize Nullable
    datetimeoffset</span></span> 
-   [3972](https://bugzilla.xamarin.com/show_bug.cgi?id=3972) :  <span><span>XElement's ToString shows incorrect
    namespace</span></span> 
-   [4690](https://bugzilla.xamarin.com/show_bug.cgi?id=4690) :  <span><span>XNodeNavigator.MoveToRoot() stays on
    self</span></span> 
-   [4739](https://bugzilla.xamarin.com/show_bug.cgi?id=4739) :  <span><span>XPathNavigator.Select doesn't select child
    node embedded between text nodes</span></span> 
-   [4850](https://bugzilla.xamarin.com/show_bug.cgi?id=4850) :  <span><span>XDocument.WriteTo() does not write
    &lt;?xml?&gt; preamble/header (.NET does)</span></span> 
-   <span><span><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=5008" target="_blank">5008</a>:</span></span>  <span><span>Cannot load VS package
    when source.properties is missing</span></span> 
-   [5043](https://bugzilla.xamarin.com/show_bug.cgi?id=5043) : Expose the Java.Util.Zip namespace. 
-   [5052](https://bugzilla.xamarin.com/show_bug.cgi?id=5052) :  <span><span>Cannot load VS package when non-numeric API
    platform is present</span></span> 
-   [5058](https://bugzilla.xamarin.com/show_bug.cgi?id=5058) :  <span><span>SqliteConnection, SqliteCommand and
    SqliteReader can result in Error "Unable to open the database
    file"</span></span> 
-   <span><span><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=5063" target="_blank">5063</a>:</span></span>  <span><span>VS Crashes on Launch
    and Monodevelop Crashing when accessing .axml</span></span> 
-   <span><span><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=5066" target="_blank">5066</a>:</span></span>  <span><span>Breakpoints not hit
    when using anonymous code</span></span> 
-   [5078](https://bugzilla.xamarin.com/show_bug.cgi?id=5078) :  <span><span>Sqlite DateTime retrieved as
    String.</span></span> 
-   [5111](https://bugzilla.xamarin.com/show_bug.cgi?id=5111) :  <span><span>Unable to generate bindings for Google's
    Guice library</span></span> 
-   [5112](https://bugzilla.xamarin.com/show_bug.cgi?id=5112) :  <span><span>Inconsistent class name capitalization when
    generating bindings</span></span> 
-   [5142](https://bugzilla.xamarin.com/show_bug.cgi?id=5142) :  <span><span>.jar binding: string constants with embedded
    newlines, numeric class names</span></span> 
-   [5144](https://bugzilla.xamarin.com/show_bug.cgi?id=5144) : AdapterView&lt;T&gt; cannot be subclassed. 
-   [5151](https://bugzilla.xamarin.com/show_bug.cgi?id=5151) :  <span><span>Implicit assembly dependencies should be
    pulled in</span></span> 
-   <span><span><a href="https://bugzilla.novell.com/show_bug.cgi?id=650402" target="_blank">650402</a>: ForeignKeyConstraint enforced on deleted
    rows.</span></span> 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
