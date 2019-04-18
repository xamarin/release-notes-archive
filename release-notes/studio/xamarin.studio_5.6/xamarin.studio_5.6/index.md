---
id: E52232FD-FEC9-4724-BF61-434C51ED6836
title: "Xamarin Studio 5.6"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.6"></head><body>
  
  

<h2><a name="0" id="0">Xamarin Studio 5.6</a></h2>

<h3>Sketches</h3>

<p>Experiment and learn with a live, interactive Sketch file. Create C# code,
and see the results right next to each line. You can even test your code right
in the simulator, without even creating a project.</p>

<p>Cool bonus features:</p>
<ul>
<li>Try using the built-in static CaptureValue(string groupName, object value)
  method to build a graph.
</li><li>In Android and iOS (Classic), try adding Xamarin.Forms pages to the static
  RootPage property (it's a TabbedPage, so you can do RootPage.Children.Add
  (new ContentPage { Title = "empty" }); for example)
</li><li>In iOS (Unified), try out RootView
</li><li>In Android (with the Android toolkit selected), try out RootActivity.
</li></ul>

<p>Play with our sample sketches in <a href='https://github.com/xamarin/sketches'>https://github.com/xamarin/sketches</a>.</p>

<p>Requirements:</p>
<ul>
  <li>iOS: Xcode 6, properly configured in Xamarin Studio’s SDK preferences.
  </li><li>Android: Xamarin Android Player is the only supported emulator at this
    time. You must be running a screen-unlocked image in the Player before
    opening or creating an Android Sketch.
</li></ul>

<p>Known issues:</p>
<ul>
  <li>You can only have one Sketch file of a particular platform type open at a time.
  </li><li>Creating classes or anonymous types in a Sketch is not currently supported.
    Try using a Tuple for now. Instead of creating methods, make Func&lt;&gt; delegates.
  </li><li>Sketches are evaluated line-by-line, just like the C# REPL. Keep this in mind,
    as a simple if/else statement may result in an error if the else is on its own line.
  </li><li>Android support is a VERY early preview. Our Sketch agent app takes some time
    to start up before the first evaluations come back to Xamarin Studio. Less code
    works better, currently. Try a bit more editing, or closing and reopening, if evaluation stalls.
  </li><li>64-bit APIs on Mac (like SceneKit) are not yet supported.
</li></ul>

<h3>Profiler</h3>

<p>Integration with Xamarin Profiler has been added for iOS and Android applications.
To start profiling an application, you can use either the Run menu or Right click
on a project and select Start Profiling. You can also launch the profile as a
standalone application from Tools -&gt; Launch Profiler.</p>

<p>New options to enable developer instrumentation have been added into Android
and iOS projects’ Build Options. These are not retroactive and you will be
asked to enable them if the project’s build configuration doesn’t have them
when profiling is requested for it.</p>

</body></html>
