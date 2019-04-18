---
id: 64DFF880-2267-04F4-DFF5-F358DE4DC349
title: "Mono for Android 4.2.7"
---

<a name="Installation" class="injected"></a>


# Installation

 **Known issue**: Immediately after upgrading, users may have
trouble loading Mono for Android projects. Please restart MonoDevelop again if
you experience this.

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 3.0. Layout Designer fixes require MonoDevelop
3.0.4.

 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

 <a name="Web_Services,_Serialization,_and_WCF_Bug_Fixes:" class="injected"></a>


### Web Services, Serialization, and WCF Bug Fixes:

-   [1340](https://bugzilla.xamarin.com/show_bug.cgi?id=1340) : NullReferenceException when calling WCF service with HTTP method other than GET or POST 
-   [4511](https://bugzilla.xamarin.com/show_bug.cgi?id=4511) : DuplexClientBase Channel Initialization Broken 
-   [4993](https://bugzilla.xamarin.com/show_bug.cgi?id=4993) :  <span>Basic Authentication without
    &lt;serviceCredentials&gt;</span> 
-   [5935](https://bugzilla.xamarin.com/show_bug.cgi?id=5935) :  <span>Serialization bug</span> 
-   [6041](https://bugzilla.xamarin.com/show_bug.cgi?id=6041) : wsdl and wsdl2 fails to generate 
-   [6187](https://bugzilla.xamarin.com/show_bug.cgi?id=6187) : Using WebGetAttribute on inherited wcf operations causes ArgumentException in mono-2.10.9 
-   [6201](https://bugzilla.xamarin.com/show_bug.cgi?id=6201) : NullReferenceException using ChannelFactory created with ServiceEndpoint constructor (regression) 
-   [6489](https://bugzilla.xamarin.com/show_bug.cgi?id=6489) : Mono implementation of SoapFormatter behaves differently from .Net implementation 
-   [6515](https://bugzilla.xamarin.com/show_bug.cgi?id=6515) : Custom headers are not included in call to web service 
-   [7177](https://bugzilla.xamarin.com/show_bug.cgi?id=7177) : Non generic derivations of the generic FaultException are not serialized correctly 
-   [7299](https://bugzilla.xamarin.com/show_bug.cgi?id=7299) : DataContractSerializer cannot deserialize ReadOnlyCollection&lt;T&gt; 


 <a name="HTTP_Stack_fixes" class="injected"></a>


### HTTP Stack fixes

-   [5655](https://bugzilla.xamarin.com/show_bug.cgi?id=5655) : HttpWebRequest not sending WebDAV headers 
-   [5899](https://bugzilla.xamarin.com/show_bug.cgi?id=5899) : WebClient.DownloadStringAsync seems to ignore QueryString values 
-   [6122](https://bugzilla.xamarin.com/show_bug.cgi?id=6122) : Different resullt from Monotouch and .net code 
-   [7200](https://bugzilla.xamarin.com/show_bug.cgi?id=7200) : HttpWebRequest returns result of a request in another thread 
-   [7424](https://bugzilla.xamarin.com/show_bug.cgi?id=7424) : HTTPWebRequest CookieContainer support not working in MonoTouch 6.0 (vs 5.4) 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
