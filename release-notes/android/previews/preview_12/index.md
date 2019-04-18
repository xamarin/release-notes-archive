---
id: 0EE2D345-96B2-4A85-32D3-7B33CEA7C88B
title: "Preview 12"
---

This preview has a new shared runtime. To ensure you are using it, you will
need to delete the old shared runtime from your emulator/device:

Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime
-&gt; Uninstall

The new runtime will be deployed to the device the next time an application
is deployed.

 <a name="General_Enhancements" class="injected"></a>


# General Enhancements

 <a name="Garbage_Collection" class="injected"></a>


## Garbage Collection

The Garbage Collector (GC) is back and better than ever. It has been
rewritten from the ground up to be able to accurately track and dispose .Net and
Java objects.

Please file bugs if you find issues with things not getting properly
collected or things getting collected when they shouldn't.

 <a name="Listeners/Events" class="injected"></a>


## Listeners/Events

The API produced from Listeners has been refined. We now follow the approach
from Monotouch regarding listeners with non-void callbacks. Instead of
EventHandler&lt;EventArgs&gt;, we generate strongly typed delegate signatures,
and the SetListener methods are used to produce properties instead of events. On
example:

public delegate bool KeyHandler (Android.Views.View v, int keyCode,
Android.Views.KeyEvent e);

public Android.Views.View.KeyHandler KeyPress { get; set; }


Expect more refinements here as we expand the usage to multi-callback
listeners, and method/ctor overloads for those members exposing listeners. <a name="Visual_Studio_Plugin_Enhancements" class="injected"></a>


# Visual Studio Plugin Enhancements

 <a name="Default_Device" class="injected"></a>


## Default Device

If you generally only test on one emulator/device, you can set this as the
default device in Tools-&gt;Options-&gt;MonoDroid, so you don't need to select
it on every run/debug.

 <a name="Additional_Profiles" class="injected"></a>


## Additional Profiles

We now ship Android 1.6 and 2.1 profiles so you can target them and get the
proper IntelliSense.

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

<table bgcolor="#FFFFFF" cellpadding="4" cellspacing="0" id="buglist" width="100%">
  <tbody>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=666456" target="_blank">666456</a>
      </td>
      <td>
        monodroid.exe throws NullReferenceException from
        Mono.Linker.Annotations.GetAction() when a class library is referenced
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=632510" target="_blank">632510</a>
      </td>
      <td>
        Enhancement: Allow Default Device to be set
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=666655" target="_blank">666655</a>
      </td>
      <td>
        framework versions are set incorrectly for VS2010
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=668730" target="_blank">668730</a>
      </td>
      <td>
        MonoDroidFlavorProject.GetFile is returning E_FAIL instead of sending
        it on to the inner hierarchy
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=655342" target="_blank">655342</a>
      </td>
      <td>
        System.InvalidOperationException When Inheriting From IntentService
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=666280" target="_blank">666280</a>
      </td>
      <td>
        [aresgen] Resource variants need to be renamed as well.
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=666461" target="_blank">666461</a>
      </td>
      <td>
        Log.Debug() doesn't seem to be working in P11
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=648893" target="_blank">648893</a>
      </td>
      <td>
        EditText.Text.ToString() doesn't give you the contents of the text
        field
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=658698" target="_blank">658698</a>
      </td>
      <td>
        System.MissingMethodException: No constructor found for **classname**
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=664986" target="_blank">664986</a>
      </td>
      <td>
        Android.Resource Types incorrectly cased / transformed
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=666149" target="_blank">666149</a>
      </td>
      <td>
        System.Xml.XmlDocument.SelectSingleNode throws
        System.TypeInitializationException
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=667073" target="_blank">667073</a>
      </td>
      <td>
        NotificationManager.Get() would be nice
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=667451" target="_blank">667451</a>
      </td>
      <td>
        HelloLinearLayout Tutorial inaccurate
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=667520" target="_blank">667520</a>
      </td>
      <td>
        AlarmManager.FromContext(...) needed...
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=667523" target="_blank">667523</a>
      </td>
      <td>
        Cannot build Monodroid project in Visual Studio - missing
        AndroidManifest.xml
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=668123" target="_blank">668123</a>
      </td>
      <td>
        [MSBuild] Clean doesn't Clean
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=657820" target="_blank">657820</a>
      </td>
      <td>
        ReferenceTable overflow (max=512) scrolling GridView at GetView()
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=667055" target="_blank">667055</a>
      </td>
      <td>
        Can't Add .Net References to an Monodroid App in P11
      </td>
    </tr>
  </tbody>
</table>

&nbsp;

&nbsp;
