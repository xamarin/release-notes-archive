---
id: 294D0A60-EE63-A6DC-DD77-2AE907CB4322
title: "Preview 14"
---

<a name="API_Changes" class="injected"></a>


# API Changes

API Level 9 is no longer supported. API level 10 has been added as its
replacement.

The (IntPtr) constructor on sealed types have been removed.

 [Java.Lang.Object.GetObject&lt;T&gt;(IntPtr,bool)](http://docs.monodroid.net/index.aspx?link=M%3aJava.Lang.Object.GetObject%60%601(System.IntPtr%2cSystem.Boolean)) has been
added.

 <a name="General_Enhancements" class="injected"></a>


# General Enhancements

The Debug runtime and Platform packages now default to installing onto the SD
card instead of onto `/data`.

Aresgen.exe generates more constants.

The IDE can now kill debug processes on devices, thus improving the "restart
app" experience.

Internationalization assemblies (for Encoding instances) can now be bundled
using ` `mandroid.exe --i18n=value``, via either the `$(MandroidI18n)` or `$(MandroidExtraArgs)` MSBuild
properties. IDE support will follow in a future release.

Mandroid.exe now generates a better error message when e.g. [ActivityAttribute.Name](http://docs.monodroid.net/index.aspx?link=P%3aAndroid.App.ActivityAttribute.Name) contains a type without a package,
e.g. `[Activity(Name="Foo")]`.

Mandroid.exe now properly copies Linked assets and resources.

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

<table bgcolor="#FFFFFF" cellpadding="4" cellspacing="0" id="buglist" width="100%">
  <tbody>
    <tr>
      <td>
        &nbsp;
      </td>
      <td>
        &nbsp;
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=666736" target="_blank">666736</a>
      </td>
      <td>
        UDP Support
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=674209" target="_blank">674209</a>
      </td>
      <td>
        Compiling MonoDroid Application Fails
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=674881" target="_blank">674881</a>
      </td>
      <td>
        Allow shared runtime to be installed on SD card
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=661355" target="_blank">661355</a>
      </td>
      <td>
        Breakpoints are not hit when debugging from device
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=669836" target="_blank">669836</a>
      </td>
      <td>
        Unhandled exceptions thrown in threads other than the UI thread aren't
        caught by the debugger
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=672503" target="_blank">672503</a>
      </td>
      <td>
        Memory leak when repeatedly creating (and disposing of) bitmaps
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=675693" target="_blank">675693</a>
      </td>
      <td>
        Pointer Reuse Crash
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=676309" target="_blank">676309</a>
      </td>
      <td>
        [generator] string ICharSequence overloads don't support nulls
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=677250" target="_blank">677250</a>
      </td>
      <td>
        Random null pointer exceptions when constantly re-creating the default
        activity (through screen rotation)
      </td>
    </tr>
  </tbody>
</table>

&nbsp;
