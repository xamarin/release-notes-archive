---
id: D37FCC1E-58E0-4FA6-8031-451565E44886
title: "Preview 7"
---

This preview has a new shared runtime. To ensure you are using it, you will
need to delete the old shared runtime from your emulator/device:

Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime
-&gt; Uninstall

The new runtime will be deployed to the device the next time an application
is deployed.

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless.

 <a name="Bug_Fixes_/_Enhancements" class="injected"></a>


# Bug Fixes / Enhancements

 <a name="Activity_Proxies" class="injected"></a>


### Activity Proxies

Activities no longer require proxies to facilitate mono runtime
initialization, and no Mono Runtime service needs to be running in order to
launch apps. This should speed up app startup.

 <a name="ApplicationAttribute_Support" class="injected"></a>


### ApplicationAttribute Support

The [Android.App.ApplicationAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.ApplicationAttribute) can be used to generate the `/manifest/application` element within `AndroidManifest.xml`. There are two ways it can be used:

1.  As an assembly-level custom attribute.
1.  On an  [Android.App.Application](http://androidapi.xamarin.com/?link=T%3aAndroid.App.Application) subclass. 


There can be *only one* `ApplicationAttribute` within an
application.

 <a name="Application_Support" class="injected"></a>


### Application Support

 [Android.App.Application](http://androidapi.xamarin.com/?link=T%3aAndroid.App.Application) can be subclassed. If subclassed, *and* the type has the [Android.App.ApplicationAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.ApplicationAttribute) custom attribute, then a
single instance of this type will be created during application startup and [Android.Content.Context.ApplicationContext](http://androidapi.xamarin.com/?link=P%3aAndroid.Content.Context.ApplicationContext) will return this
instance.

 [Android.App.Application](http://androidapi.xamarin.com/?link=T%3aAndroid.App.Application) subclasses with the [Android.App.ApplicationAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.ApplicationAttribute) custom attribute *must*provide a constructor accepting a single IntPtr parameter, and must
chain this constructor to the [Android.App.Application(IntPtr)](http://androidapi.xamarin.com/?link=C%3aAndroid.App.Application%28System.IntPtr%29) constructor.

 <a name="BroadcastReceiver_Support" class="injected"></a>


### BroadcastReceiver Support

BroadcastReceivers can now be declared by subclassing [Android.Content.BroadcastReceiver](http://androidapi.xamarin.com/?link=T%3aAndroid.Content.BroadcastReceiver) and using the [Android.Content.BroadcastReceiverAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.Content.BroadcastReceiverAttribute) custom
attribute.

 <a name="ContentProvider_Support" class="injected"></a>


### ContentProvider Support

ContentProviders can now be declared by subclassing [Android.Content.ContentProvider](http://androidapi.xamarin.com/?link=T%3aAndroid.Content.ContentProvider) and using the [Android.Content.ContentProviderAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.Content.ContentProviderAttribute) custom
attribute.

 <a name="Packaging_Changes" class="injected"></a>


### Packaging Changes

 [Preview 5](http://android.xamarin.com/Releases/Previews/Preview_5) introduced a model in which assemblies were named to match the `lib*.so` glob, and placed into the `lib/ABI` directory
within the `.apk`. While this worked, it was deemed by many as a hack
(albeit an awesome one), and resulted in storing assemblies multiple times when
supporting multiple ABIs (as a set of assemblies would need to be stored in the `.apk` for each ABI).

This changes in **Preview 7**. Assemblies are now stored *uncompressed* within the `.apk` and loaded from
the `.apk` during app startup. This has two immediately visible
impacts:

1.  Application sizes will be larger. The "Hello, World" default template grows from 3.2MB to 12.8MB. 
1.  The  *installed* size be  *smaller* . Assemblies compress well; in Preview 5, the application assemblies would still need to be extracted, so the extracted size ($APPDIR/lib contents + .apk) is 15.9MB, while in Preview 7 the extracted size is 12.9MB.  *Total size* is thus reduced by 3MB. 


Note that this size is *not* indicative of what apps will be by 1.0.
Specifically, *no linking* is being done. Once the linker is integrated
and running, we expect app sizes to shrink significantly.

 <a name="Service_Support" class="injected"></a>


### Service Support

Services can now be declared by subclassing [Android.App.Service](http://androidapi.xamarin.com/?link=T%3aAndroid.App.Service) and using the [Android.App.ServiceAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.ServiceAttribute) custom attribute.

 <a name="Breaking_Changes" class="injected"></a>


## Breaking Changes

 <a name="Activity_Constructors" class="injected"></a>


### Activity Constructors

 [Android.App.Activity](http://androidapi.xamarin.com/?link=T%3aAndroid.App.Activity) subclasses no longer need a `(IntPtr)` constructor, and *must* have a default constructor.
If no default constructor is present, then you will see a `NotImplementedException` in the `adb logcat` output with
the message: Unable to find the default constructor on type *insert type here*. Please provide the missing constructor.

The only types which require `(IntPtr)` constructors are:

1.   [Android.App.Application](http://androidapi.xamarin.com/?link=T%3aAndroid.App.Application) subclasses. 
1.  Types which subclass an Android type which invokes an overridden non- `final` method in the constructor; see IntPtr Constructor Invocation, below. 


 <a name="Application_Package_Must_Be_Lowercase" class="injected"></a>


### Application Package Must Be Lowercase

Within `Properties\AndroidManifest.xml`, the value of the `/manifest/@package` attribute *must* be lowercase. Presence
of uppercase characters will result in build errors from monodroid.exe.

 <a name="" class="injected"></a>


<h3 id="intptr-constructor">
  IntPtr Constructor Invocation
</h3>

 *Usually*, an ( `IntPtr`) constructor is not required. (This
has been true since [Preview 3](/releases/android/previews/preview_3)
except for Activities, which was fixed in this release.) There are two
situations where an ( `IntPtr`) constructor is required:

1.  When subclassing  [Android.App.Application](http://androidapi.xamarin.com/?link=T%3aAndroid.App.Application) . 
1.   When subclassing an Android type (e.g.  [Android.Widget.TextView](http://androidapi.xamarin.com/?link=T%3aAndroid.Widget.TextView) )  *and* overriding a virtual method which is invoked by the base class constructor (e.g. [Android.Widget.TextView.DefaultMovementMethod](http://androidapi.xamarin.com/?link=P%3aAndroid.Widget.TextView.DefaultMovementMethod) )  *and* the type is created by Android (e.g. via an XML layout), e.g.  [LogTextBox.cs](https://github.com/xamarin/monodroid-samples/blob/master/ApiDemo/Text/LogTextBox.cs) and  [log_text_box_1.xml](https://github.com/xamarin/monodroid-samples/blob/master/ApiDemo/Resources/layout/log_text_box_1.xml) .

 


You'll know you need an ( `IntPtr`) constructor when your app
crashes and you investigate the `adb logcat`output.

 <a name="Package_Names" class="injected"></a>


### Package Names

The package names of Android Callable Wrappers generated by monodroid.exe are
now lowercase instead of camelCase. This was done to sanely support
case-insensitive filesystems.

In particular, developers should update their `Resources\layout\*.xml` files so that all XML elements use lowercase
package names. See e.g. the changes done in [ApiDemo\Resources\layout\log_text_box_1.xml](https://github.com/xamarin/monodroid-samples/commit/9692564031a1d3b8447a40912c5fa8fcaca2b164#diff-33).

 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

-   [633463](https://bugzilla.novell.com/show_bug.cgi?id=633463) - Application crashes on startup when Assembly Name contains spaces. 
-   [645603](https://bugzilla.novell.com/show_bug.cgi?id=645603) - MonoDroid doesn't support custom Application Classes 
-   [648893](https://bugzilla.novell.com/show_bug.cgi?id=648893) - EditText.Text.ToString() doesn't give you the contents of the text field 
-   [648896](https://bugzilla.novell.com/show_bug.cgi?id=648896) - KeyEventArgs.KeyCode should use Keycode enum instead of int 
-   [648898](https://bugzilla.novell.com/show_bug.cgi?id=648898) - Missing feature constants in Window class 
-   [649456](https://bugzilla.novell.com/show_bug.cgi?id=649456) - You can use java source files, but no R class is created, rendering it impossible to use layouts/resources/cocaine/etc. 
-   [649920](https://bugzilla.novell.com/show_bug.cgi?id=649920) - Runtime producing UnsatisfiedLinkError on JavaObject hashCode calls 
-   [650335](https://bugzilla.novell.com/show_bug.cgi?id=650335) - Keyboard shortcut does not work for SaveAll when code editor is active 
-   [650541](https://bugzilla.novell.com/show_bug.cgi?id=650541) - Device emulator hangs if AndroidManifest package name contains space char at the end
