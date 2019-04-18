---
id: 36C49953-9D39-483E-9EB2-494D47A75929
title: "From 6.3.3 to 6.3.4"
---

<html><head><title>Comparison between monotouch-6.3.3.dll and monotouch-6.3.4.36.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.3.3";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.3.4";
</pre>
<h2>Namespace: MonoTouch.CoreServices</h2>
<h3>Type Changed: MonoTouch.CoreServices.CFHTTPMessage</h3>
<p>Added:</p><pre>
 	public static CFHTTPMessage CreateEmpty (bool request);
 	public bool AppendBytes (byte [] bytes);
 	public bool AppendBytes (byte [] bytes, int count);
</pre>
</body>
</html>
