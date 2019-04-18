---
id: 7D673027-48FF-4C06-80FD-7716C4E185DE
title: "Xamarin.Mac 2.8"
---

version:2.8.0
releasedate:2016-03-31

<div class="note">
	**Classic Profile Deprecation:**
	As new features are added in Xamarin.Mac we are starting to gradually deprecate features from the classic profile (xammac.dll).
	In this release the non-NRC (new-ref-count) option was removed. NRC has always been enabled for all unified applications (i.e. non-NRC was never an option) and has no known issues.
</div>

Requirements
============

- The latest features and API requires Xcode 7.2 and the bundled macosx10.11 SDK;
- Apple Xcode 7.2 requires a Mac running OSX 10.10 (Yosemite) or 10.11 (El Capitan)

What's New
==========

### Mac Binding Project

This release includes new support for Xamarin.Mac binding projects. They act very similar to the existing iOS binding projects, and most of the [iOS documentation](https://developer.xamarin.com/guides/ios/advanced_topics/binding_objective-c/walkthrough/) is applicable.

### HttpClient Improvements

NSUrlSessionHandler
-------------------

This release includes a new native `NSUrlSession`-based HTTP handler based on the popular [ModernHttpClient](https://github.com/paulcbetts/ModernHttpClient) open source library.

This was designed to be both a transparent (no source) change and to reduce the amount/size of application code required for the HTTP stack. As such some, non-default, options specific to ModernHttpClient are not provided. The use of [ModernHttpClient](https://github.com/paulcbetts/ModernHttpClient) is still possible from your applications as we avoided potential names/types conflicts.

An application that removes all usage of `System.Net.WebRequest` and use `HttpClient` with the new `NSUrlSessionHandler` can reduce it's size by about 850KB (per architecture) and benefit from the performance gains of the native stack.


Selecting the Default Handler
-----------------------------

To make it easier to adopt a specific handler across all `HttpClient` uses in your application Xamarin.iOS now allow you to set which handler should be used for `HttpClient`. The following options are available:

- `HttpClientHandler`: This is the fully managed `HttpClient` handler that has been shipped with previous Xamarin.iOS. It is the most compatible (features) with MS .NET and older Xamarin versions. However it's slower (e.g. encryption) and requires more code in the final application. To ensure maximum compatibility for existing applications this is the **default** handler.
- `CFNetworkHandler`: This handler uses native API (CFNetwork framework) for better performance and smaller executable size. However it requires iOS6 (or later) and it not available on watchOS. Not every `HttpClient` features/options are available;
- `NSUrlSessionHandler`: This handler uses native API (NSUrlSession) for better performance and smaller executable size. However it requires iOS7 (or later) and does not support every `HttpClient` features/options;

Selecting which default `HttpClient` handler can be done using the project's options in your IDE (XS or VS) or by providing `mtouch` with either `--http-message-handler=HttpClientHandler`, `--http-message-handler=CFNetworkHandler` or `--http-message-handler=NSUrlSessionHandler` command-line arguments.


### Apple TLS support

You can now select which **Transport Layer Security** (TLS) provider you want to use inside your iOS application, e.g. to support `SslStream`, which provides the SSL/TLS support for `System.Net.WebRequest` and it's friends.

By default your projects will now use the new **Apple TLS stack** which uses native code (better performance) and support the newest TLS 1.1 and 1.2 standards. **This is a change from previous preview releases of XM 2.8.**

You can also opt-out and continue to use the managed **Mono TLS** stack, which only supports up to TLS 1.0. This will continue to use the same stack that was shipped in previous versions of Xamarin.iOS.

Selecting which TLS provider to use can be can be done using the project's options in your IDE (XS or VS) or by providing `mtouch` with either `--tls-provider=legacy` or `--tls-provider=appletls` command-line arguments.


### Other Changes

Generic versions of NS* collections
-----------------------------------

This version adds generic versions of the following types:
- NSArray<TKey>
- NSOrderedSet<TKey>
- NSMutableOrderedSet<TKey>

### Known Issues

- Xamarin.Mac 2.8 is currently incompatible with Xcode8 when the static registrar is enabled due to the removal of header files by Apple.
   - This will be fixed in a future release.
   - Targeting Xcode 7.3 or downloading a XM from https://jenkins.mono-project.com/view/Xamarin.MaciOS/job/xamarin-macios-builds-xcode8/ are possible work arounds.
- Uses of NSLog (via p/invoke) will crash applications on macOS 10.12 Beta6 with _os_trace_location_for_address in the stack trace.

### Releases

- 2.8.2.19 - 2.8.2.22

Cycle 7 Service Release 1 Update

Fixed known issue in 2.8.2.15 with System.Security.dll and link errors.

- 2.8.2.15

Cycle 7 Service Release 1

Known Issue - Some Xamarin.Mac Unified Mobile applications may fail linking with errors related to System.Security.dll. This can be worked around by disabling linking or downgrading to SR0. This will be fix in a future update.

Fixed issue where in some cases mmp under the Mobile profile would incorrectly resolve assemblies from the GAC.

- 2.8.1.3 

Cycle 7 Service Release 0

Fixed "System.Configuration.DictionarySectionHandler is missing" error.  [#39669](https://bugzilla.xamarin.com/show_bug.cgi?id=39669)

Fixed "Mono.Security.Interface.TlsException: Unknown Secure Transport error \`ClosedGraceful'" in certain environments when using the _Managed_ setting for _HttpClient implementation_ in combination with the new default _Apple TLS_ setting for _SSL/TLS implementation_.  [#41206](https://bugzilla.xamarin.com/show_bug.cgi?id=41206)

Fixed [AppleTls] Certain calls to `HttpClient.SendAsync()` can hit a delay of about 60 seconds before completing if using the new default _Apple TLS_ setting for _SSL/TLS implementation_ (same fix as #41206).  [#41697](https://bugzilla.xamarin.com/show_bug.cgi?id=41697)

Fixed [registrar] "initWithCoder:' has been explicitly marked unavailable".  [#41319](https://bugzilla.xamarin.com/show_bug.cgi?id=41319)

Fixed [mono] "System.Net.WebException: Error: NameResolutionFailure" when attempting web requests with certain raw IP addresses.  [#41782](https://bugzilla.xamarin.com/show_bug.cgi?id=41782)

Fixed [mono] Reflection throws `AmbiguousMatchException` when calling `GetProperty()` on a class that inherits from a generic base class.  [#41874](https://bugzilla.xamarin.com/show_bug.cgi?id=41874)

Known issue: `CGRect.Inflate()` returns an unmodified `CGRect` regardless of the input parameters.  **Possible temporary workaround**: Modify the frame of the `CGRect` by hand using the `X`, `Y`, `Width`, and `Height` properties.  [#41684](https://bugzilla.xamarin.com/show_bug.cgi?id=41684)

- 2.8.0.323

Cycle 7 initial release.

Fixed major bug in mmp that allowed resolution of assemblies from GAC in supported profiles, including System.Drawing. - [#40436](https://bugzilla.xamarin.com/show_bug.cgi?id=40436)

Known issue: "Mono.Security.Interface.TlsException: Unknown Secure Transport error \`ClosedGraceful'" in certain environments when using the _Managed_ setting for _HttpClient implementation_ in combination with the new default _Apple TLS_ setting for _SSL/TLS implementation_.  **Workaround**: Under _Project Options > iOS Build_, either change the _SSL/TLS implementation_ setting back to the old default _Mono (TLS v1.0)_, or set the _HttpClient implementation_ to one of the new _CFNetwork_ or _NSUrlSession_ options.  [#41206](https://bugzilla.xamarin.com/show_bug.cgi?id=41206)

Known issue: Certain calls to `HttpClient.SendAsync()` can hit a delay of about 60 seconds before completing if using the new default _Apple TLS_ setting for _SSL/TLS implementation_.  Based on the information gathered so far, it seems the issue might only affect HTTPS requests that use authorization headers.  **Workaround**: Under _Project Options > iOS Build_, change the _SSL/TLS implementation_ setting back to the old default _Mono (TLS v1.0)_.  [#41697](https://bugzilla.xamarin.com/show_bug.cgi?id=41697)

Known issue: "System.Net.WebException: Error: NameResolutionFailure" when attempting web requests with certain raw IP addresses.  This is a bug in Mono, so it affects all platforms iOS, Android, and Mac.  **Partial temporary workaround**: If possible, use domain names rather than raw IP addresses for the web requests.  [#41782](https://bugzilla.xamarin.com/show_bug.cgi?id=41782)

- 2.8.0.294

Release Canidate released at Evolve 2016

### API diff

Will be published at a later date.

