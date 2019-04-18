---
id: 956DD716-A227-4EB7-A3CC-B67E86BD3F89
title: "Xamarin.Android 4.6.7"
---

# Installation

 **Known issue**: Immediately after upgrading, users may have
trouble loading Xamarin.Android projects. Please restart Xamarin Studio again
if you experience this.

 **Visual Studio Users**: You should be prompted with this update
when you open a Xamarin.Android project. You can also check manually in Tools
&gt; Options &gt; Xamarin.Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates.
IDE support requires Xamarin Studio 4.0.
Layout Designer fixes require MonoDevelop 3.0.4.

# New Features

-  Starter edition size limit has been increased to 64KB.


# Bug fixes

-  Added more information to the warning shown when using native linking as a starter user.
-  Give meaningful message for missing  `//attr/@name` attribute value within  `Metadata.xml` .
-  Filter for non-existent drives when choosing a working directory. 
-  Enhanced assembly duplicate check while calculating assembly size. Some assemblies were previously being counted twice against the size limit.
-   [5037](https://bugzilla.xamarin.com/show_bug.cgi?id=5037) : Copy Satellite assemblies into obj/Release/assemblies. 
-   [5827](https://bugzilla.xamarin.com/show_bug.cgi?id=5827) : Deserializing xml with strange ASCII characters throws an exception. 
-   [7477](https://bugzilla.xamarin.com/show_bug.cgi?id=7477) ,  [12087](https://bugzilla.xamarin.com/show_bug.cgi?id=12087) : Enhanced user experience when both using the Android designer and manually modifying the .axml. 
-   [7899](https://bugzilla.xamarin.com/show_bug.cgi?id=7899) : Make table name comparison dataset locale specific. 
-   [10693](https://bugzilla.xamarin.com/show_bug.cgi?id=10693) : Disabled serialization assembly generation. 
-   [11401](https://bugzilla.xamarin.com/show_bug.cgi?id=11401) : Fix Fast Deployment on API 12 devices. 
-   [11608](https://bugzilla.xamarin.com/show_bug.cgi?id=11608) : Activity-alias elements will now be directly after their target activities. 
-   [11803](https://bugzilla.xamarin.com/show_bug.cgi?id=11803) : Application closes immediately after deploying to device. 
-   [11921](https://bugzilla.xamarin.com/show_bug.cgi?id=11921) : No more crash when removing an AndroidGameView without calling Pause(). 
-   [11964](https://bugzilla.xamarin.com/show_bug.cgi?id=11964) : Added sanity check on project.properties container directory. 
-   [12250](https://bugzilla.xamarin.com/show_bug.cgi?id=12250) : Use non-shortname paths when installing on Windows.
