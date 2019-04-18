---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 1.2"
---

##  []()Xamarin.Mac 1.2

This release contains many API additions and refinements including full
Mountain Lion and Lion coverage for the AppKit framework, along with many other
bug fixes and improvements.

You can check our [Roadmap](/releases/mac/roadmap) to learn where
Xamarin.Mac is headed.

### Highlights

<ul>
  <li>Lion and Mountain Lion APIs are introduced for AppKit.</li>
  <li><a href="https://developer.apple.com/library/mac/#documentation/Darwin/Conceptual/FSEvents_ProgGuide/Introduction/Introduction.html">FSEvents</a>
  from Core Services was introduced for monitoring file system changes. <a href="/samples/FSEvents">Explore a sample application</a>.</li>
  <li>Enhancements were made to the WebKit binding around DOM APIs and
  Navigation Policy APIs such as <code>WebView.DecidePolicyForNavigation</code>
  and <code>WebNavigationPolicyEventArgs</code>. <a href="/samples/MarkdownViewer/">Explore a sample
  application</a>.</li>
  <li>New dispose semantics were added to match the behavior <a href="/releases/ios/monotouch_6/monotouch_6.0#MonoTouch_6.0.8">introduced in
  MonoTouch/Xamarin.iOS 6.0.8</a>.</li>
  <li>Cross-thread UI checks are now supported in Debug builds <a href="/releases/ios/monotouch_6/monotouch_6.0#2.1.1.cross-thread-ui-checks">similar
  to those supported in MonoTouch/Xamarin.iOS</a>.</li>
  <li>Shared memory usage is now disabled
  (<code>MONO_DISABLE_SHARED_AREA</code>) when linking applications for App
  Store distribution as Apple no longer allows using shared memory
  (<code>/dev/shm</code>).</li>
  <li>Multi-thread support is now enabled automatically in order to <a href="https://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/Multithreading/CreatingThreads/CreatingThreads.html#//apple_ref/doc/uid/10000057i-CH15-SW21">protect
  the Cocoa Frameworks</a> when mixing POSIX/.NET threads
  (<code>System.Threading.Thread</code>) and <code>NSThread</code>s in the same
  application.</li>
  <li>Other notable API improvements:
    <ul>
      <li><code>NSThread.Start (NSAction)</code> was added for lambda-friendly
      thread spawning:
        <pre><code class=" syntax brush-C#">NSThread.Start (() =&gt; Console.WriteLine ("Hello from an NSThread"));</code></pre>
      </li>
      <li>Added <a href="https://gist.github.com/abock/0493449d133be0caeb60">many convenience
      constructors</a> to <code>NSPredicateEditorRowTemplate</code>.</li>
      <li>Added many convenience constructors to
      <code>NSAttributedString</code>.</li>
      <li>Added <code>NSTableViewDelegate.GetToolTip</code></li>
      <li>Many APIs were renamed to ensure future API naming consistency.
      Renamed APIs are marked with <code>[Obsolete]</code> to ensure existing
      code does not break however.</li>
    </ul>
  </li>
</ul>

### Detailed API Differences

-  [Complete API changes from Xamarin.Mac 1.0 to 1.2](/releases/mac/api_changes/from_1.0_to_1.2) .


### Getting Started

-  Explore &quot; [Hello, Mac](/guides/mac/getting_started/hello%2C_mac) ,&quot; our tutorial on building your first Xamarin.Mac application. 
-  Launch the Documentation Browser from Xamarin Studio (Help-&gt;Help) and browse the API under the MonoMac namespace. 
-  Check our&nbsp; [extensive set of samples](/samples/mac/all) . 


### Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.
