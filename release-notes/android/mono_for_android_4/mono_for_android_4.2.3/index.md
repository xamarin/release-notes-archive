---
id: 4201404E-FB68-9434-403E-4F9FF5426A98
title: "Mono for Android 4.2.3"
---

<a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 3.0. Layout Designer fixes require MonoDevelop
3.0.3.

 <a name="New_Features" class="injected"></a>


# New Features

-  The layout designer in Visual Studio can now switch between layout view and source view. (Intellisense isn't supported yet.) 
-  Added support for scrolling in ScrollView.


 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-  Many fixes for issues with detecting and deploying to devices in the updated Visual Studio extension. 
-  Partial Revert of 4.2.2 "Reduce lifetime of wrapped  [Stream](http://androidapi.xamarin.com/?link=T:System.IO.Stream) s in  [InputStreamAdapter](http://androidapi.xamarin.com/?link=T:Android.Runtime.InputStreamAdapter) ,  [InputStreamInvoker](http://androidapi.xamarin.com/?link=T:Android.Runtime.InputStreamInvoker) ,  [OutputStreamAdapter](http://androidapi.xamarin.com/?link=T:Android.Runtime.OutputStreamAdapter) ,  [OutputStreamInvoker](http://androidapi.xamarin.com/?link=T:Android.Runtime.OutputStreamInvoker) ." Disposing of an Adapter will  *not* dispose of the wrapped Stream. 
-  Don't call  [IEGL10.EglGetError()](http://androidapi.xamarin.com/?link=M:Javax.Microedition.Khronos.Egl.IEGL10.EglGetError) twice.  [Should help prevent reporting of EGL_SUCCESS as an error](http://lists.ximian.com/pipermail/monodroid/2012-May/010484.html) . 
-   [242](https://bugzilla.xamarin.com/show_bug.cgi?id=242) :  <span><span><a href="http://androidapi.xamarin.com/?link=T:System.Runtime.Serialization.DataContractSerializer" target="_blank">DataContractSerializer</a> fails to deserialize <a href="http://androidapi.xamarin.com?link=t:system.collections.generic.list{t}">
    List&lt;T&gt;</a> properties</span></span> 
-   [4288](https://bugzilla.xamarin.com/show_bug.cgi?id=4288) : Binding errors due to visibility inconsistency and  [Android.Graphics.Color](http://androidapi.xamarin.com/?link=T:Android.Graphics.Color) support. 
-   [5011](https://bugzilla.xamarin.com/show_bug.cgi?id=5011) :  <span><span><a href="http://androidapi.xamarin.com/?link=M:System.IO.IsolatedStorage.IsolatedStorageFile.CreateDirectory" target="_blank">IsolatedStorageFile.CreateDirectory</a> throws an exception
    with rooted paths</span></span> 
-   [5020](https://bugzilla.xamarin.com/show_bug.cgi?id=5020) :  <span><span>Jar project creating duplicates in generated
    code.</span></span> 
-   [5021](https://bugzilla.xamarin.com/show_bug.cgi?id=5021) :  <span><span><a href="http://androidapi.xamarin.com/?link=E:System.ComponentModel.BackgroundWorker.RunWorkerCompleted" target="_blank">BackgroundWorker.RunWorkerCompleted</a> does not run within
    UI thread</span></span> 
-   [5091](https://bugzilla.xamarin.com/show_bug.cgi?id=5091) :  <span><span>Deploy shared runtime for target device
    architecture (regardless of configuration)</span></span> 
-   [5118](https://bugzilla.xamarin.com/show_bug.cgi?id=5118) : Allow $(IntermediateBuildPath) to be an absolute directory 
-   [5143](https://bugzilla.xamarin.com/show_bug.cgi?id=5143) :  <span><span>.jar binding shouldn't fail due to missing
    types</span></span> 
-   [5274](https://bugzilla.xamarin.com/show_bug.cgi?id=5274) :  <span><span>Deployment for a second device fails if
    project not rebuit</span></span> 
-   [5289](https://bugzilla.xamarin.com/show_bug.cgi?id=5289) : Fix for devices that report multi-line getprops 
-   [5304](https://bugzilla.xamarin.com/show_bug.cgi?id=5304) :  <span><span><a href="http://androidapi.xamarin.com?link=m:system.collections.concurrent.concurrentstack{t}.trypoprange%28t[]%29">
    ConcurrentStack.TryPopRange()</a> doesn't support arrays of length
    1</span></span> 
-   [5319](https://bugzilla.xamarin.com/show_bug.cgi?id=5319) : System.InvalidCastException: Value is not a convertible object: Java.Lang.String to System.Object. 
-   [5311](https://bugzilla.xamarin.com/show_bug.cgi?id=5311) :  <span><span>LockRecursionException is defined in
    mscorlib and System.Core</span></span> 
-   [5337](https://bugzilla.xamarin.com/show_bug.cgi?id=5337) :  <span><span><a href="http://androidapi.xamarin.com?link=t:system.componentmodel.inotifypropertychanging">
    INotifyPropertyChanging</a> and <a href="http://androidapi.xamarin.com?link=t:system.componentmodel.propertychangingeventargs">
    PropertyChangingEventArgs</a> not included</span></span> 
-   [5375](https://bugzilla.xamarin.com/show_bug.cgi?id=5375) :  <span><span>Deploy to a device failed with a "Failure
    [INSTALL_PARSE_FAILED_MANIFEST_MALFORMED]" error</span></span> 
-   [5396](https://bugzilla.xamarin.com/show_bug.cgi?id=5396) :  <span><span>Special uses-permission lost when updating
    the app's project properties</span></span> 
-   [5421](https://bugzilla.xamarin.com/show_bug.cgi?id=5421) :  <span><span>generator: ArgumentOutOfRangeException when
    binding .jar</span></span> 
-   [5461](https://bugzilla.xamarin.com/show_bug.cgi?id=5461) :  <span><span>Can't use <a href="http://androidapi.xamarin.com/?link=T:Java.Util.Zip.ZipInputStream" target="_blank">ZipInputStream</a></span></span> 


&nbsp;

 <a name="Layout_Designer_fixes" class="injected"></a>


# Layout Designer fixes

 **Visual Studio Users**: The Layout Designer is installed with
Mono for Android.

 **MonoDevelop Users**: The Layout Designer is not included in
the Mono for Android installer; the layout designer fixes are included in
MonoDevelop 3.0.3.

-  Themes defined in project resources are now properly rendered
-  The resource selector now doesn't show private framework resources
-   [4894](https://bugzilla.xamarin.com/show_bug.cgi?id=4894) : Switching project build target to API 10 throws exception (when editing existing layout) 
-   [4953](https://bugzilla.xamarin.com/show_bug.cgi?id=4953) : Numeric Password widget loads with an invalid input type 
-   [5290](https://bugzilla.xamarin.com/show_bug.cgi?id=5290) : Style attribute missing from View properties 
-   [5349](https://bugzilla.xamarin.com/show_bug.cgi?id=5349) : Activity modification causes axml files reload 
-   [5369](https://bugzilla.xamarin.com/show_bug.cgi?id=5369) 5369: Designer adds unrecognized android:placeholder on TableLayout 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
