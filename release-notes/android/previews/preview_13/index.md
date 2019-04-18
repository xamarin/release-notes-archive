---
id: AD672A04-9777-C0B2-0384-2146C4C87029
title: "Preview 13"
---

<a name="API_Changes" class="injected"></a>


# API Changes

 <a name="CharSequences" class="injected"></a>


## CharSequences

In response to user feedback, we have implemented a new approach to binding
the [java.lang.CharSequence](http://developer.android.com/reference/java/lang/CharSequence.html) interface exposed by Android. Most
of the Android API is exposed as `CharSequence`s instead of [java.lang.String](http://developer.android.com/reference/java/lang/String.html) to support formatted text. [SpannableString](http://docs.monodroid.net/index.aspx?link=T%3aAndroid.Text.SpannableString) and [SpannedString](http://docs.monodroid.net/index.aspx?link=T%3aAndroid.Text.SpannedString)are a couple of `CharSequence`
implementors exposed in [Android.Text](http://docs.monodroid.net/index.aspx?link=N%3aAndroid.Text) to support this capability.

Our new binding approach is to produce an overloaded API. Where the Android
API exposes methods with `CharSequence` parameters, we provide
overloaded methods for [string](http://docs.monodroid.net/index.aspx?link=T%3aSystem.String) and [Java.Lang.ICharSequence](http://docs.monodroid.net/index.aspx?link=T%3aJava.Lang.ICharSequence)variants of the method signature. For
properties and methods with `CharSequence` return values, we had to
create alternatively named elements. For example, [Android.Widget.TextView](http://docs.monodroid.net/index.aspx?link=T%3aAndroid.Widget.TextView) now has "overloaded" [TextView.Text](http://docs.monodroid.net/index.aspx?link=P%3aAndroid.Widget.TextView.Text) and [TextView.TextFormatted](http://docs.monodroid.net/index.aspx?link=P%3aAndroid.Widget.TextView.TextFormatted) properties:

```
public string Text { get; set; } 
public Java.Lang.ICharSequence TextFormatted { get; set; }
```

This means that you can now do things like:

```
EditText editText = new EditText (this);  
...
string text = editText.Text;
```

without have to use [Convert.ToString()](http://docs.monodroid.net/index.aspx?link=M%3aSystem.Convert.ToString) or [object.ToString()](http://docs.monodroid.net/index.aspx?link=M%3aSystem.Object.ToString) to get a string value as with the
previous `IEnumerable<char>` implementation. However, if you
want to set or manipulate formatted text in the view, you will have to use the `TextFormatted` property now.

 <a name="General_Enhancements" class="injected"></a>


# General Enhancements

 <a name="Mono.Android.dll_Moved_to_Debug_Shared_Runtime_Packages" class="injected"></a>


## Mono.Android.dll Moved to Debug Shared Runtime Packages

In addition to the regular shared runtime used for debug builds, there are
now target version specific ones that contain Mono.Android.dll. This
dramatically reduces the size of debug .apks, resulting in much faster deploys,
making the change/deploy/test cycle much quicker. Linking is now turned off by
default for debug builds.

 <a name="Versioned_Debug_Shared_Runtimes" class="injected"></a>


## Versioned Debug Shared Runtimes

Shared runtimes are now versioned, so the IDE can detect if you are running
an old shared runtime and automatically remove it. This means you should never
need to manually remove the shared runtime again.

 <a name="Visual_Studio_Plugin_Enhancements" class="injected"></a>


# Visual Studio Plugin Enhancements

 <a name="Debugging_Enhancements" class="injected"></a>


## Debugging Enhancements

-  Breakpoints in class libraries should now function as expected.
-  Disabled breakpoints are now skipped.
-  Starting the debugger via "Start New Instance" now works.


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

<table bgcolor="#FFFFFF" cellpadding="4" cellspacing="0" id="buglist" width="100%">
  <tbody>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=672350" target="_blank">672350</a>
      </td>
      <td>
        Linker: Mono.Android.mdb used by another process
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=673178" target="_blank">673178</a>
      </td>
      <td>
        Link out [MonoTodo] and friends
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=657617" target="_blank">657617</a>
      </td>
      <td>
        Monodroid project will not debug
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=657877" target="_blank">657877</a>
      </td>
      <td>
        Deploying application to emulator is very slow in P9
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=668504" target="_blank">668504</a>
      </td>
      <td>
        Change signature of Window.SetFormat to use Android.Graphics.Format
        enum
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=670361" target="_blank">670361</a>
      </td>
      <td>
        Mono Runtime on Android v2.3 Research Bug
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=672325" target="_blank">672325</a>
      </td>
      <td>
        Assets have filename case changed during compilation
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=672613" target="_blank">672613</a>
      </td>
      <td>
        Support mixed-cased package names.
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=641502" target="_blank">641502</a>
      </td>
      <td>
        Debugger doesn't stop at breakpoints in class libraries
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=671108" target="_blank">671108</a>
      </td>
      <td>
        Problem with deactivate breakpoint on Preview 12.
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=661858" target="_blank">661858</a>
      </td>
      <td>
        Allow the use of Jar files to be used in MonoDroid.
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=666610" target="_blank">666610</a>
      </td>
      <td>
        DirectoryNotFoundException when compiling - Preview 1
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=665893" target="_blank">665893</a>
      </td>
      <td>
        Application crashes when generic method that calls another generic
        method is called.
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://bugzilla.novell.com/show_bug.cgi?id=670839" target="_blank">670839</a>
      </td>
      <td>
        Building a Java file fails when encoding is not ANSI
      </td>
    </tr>
  </tbody>
</table>
