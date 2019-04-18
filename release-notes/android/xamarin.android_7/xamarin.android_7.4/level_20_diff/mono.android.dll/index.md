---
id: ADEFD0AD-C0A9-4355-A46F-B92C75C71DB0
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Xamarin.Android.Net

### Type Changed: Xamarin.Android.Net.AndroidClientHandler

Added properties:

```
public System.TimeSpan ConnectTimeout { get; set; }
	public System.TimeSpan ReadTimeout { get; set; }
```



Added methods:

```
protected virtual Javax.Net.Ssl.SSLSocketFactory ConfigureCustomSSLSocketFactory (Javax.Net.Ssl.HttpsURLConnection connection);
	protected virtual Javax.Net.Ssl.IHostnameVerifier GetSSLHostnameVerifier (Javax.Net.Ssl.HttpsURLConnection connection);
	protected virtual System.Threading.Tasks.Task WriteRequestContentToOutput (System.Net.Http.HttpRequestMessage request, Java.Net.HttpURLConnection httpConnection, System.Threading.CancellationToken cancellationToken);
```
