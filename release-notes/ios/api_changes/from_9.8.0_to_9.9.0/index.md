---
id: 1F8C51A3-6CAD-4CF7-B304-CFC9433F0DC0
title: "From 9.8.0 to 9.9.0"
---

# API diff

 [(Classic) mscorlib.dll](#diff/xi/2.1/mscorlib.html)

   


 [(Classic) System.dll](#diff/xi/2.1/System.html)

   


 [(Classic) System.Core.dll](#diff/xi/2.1/System.Core.html)

   


 [(Classic) System.Transactions.dll](#diff/xi/2.1/System.Transactions.html)

   


 [(Classic) monotouch.dll](#diff/xi/2.1/monotouch.html)

   


 [(Classic) MonoTouch.NUnitLite.dll](#diff/xi/2.1/MonoTouch.NUnitLite.html)

   


 [(Unified) MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.iOS/MonoTouch.NUnitLite.html)

   


 [(Unified) Xamarin.iOS.dll](#diff/xi/Xamarin.iOS/Xamarin.iOS.html)

   


   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/2.1/mscorlib.html'>mscorlib.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Microsoft.Win32.SafeHandles --> <div> 
<h2>Namespace Microsoft.Win32.SafeHandles</h2>
<div> <!-- start type SafeAccessTokenHandle -->
<h3>New Type Microsoft.Win32.SafeHandles.SafeAccessTokenHandle</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SafeAccessTokenHandle : System.Runtime.InteropServices.SafeHandle, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SafeAccessTokenHandle ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override bool IsInvalid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override bool ReleaseHandle ();</span>
}
</pre>
</div> <!-- end type SafeAccessTokenHandle -->

</div> <!-- end namespace Microsoft.Win32.SafeHandles -->
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type AppContext --> <div>
<h3>Type Changed: System.AppContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string BaseDirectory { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSwitch (string switchName, bool isEnabled);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryGetSwitch (string switchName, out bool isEnabled);</span>
</pre>
</div>

</div> <!-- end type AppContext -->

</div> <!-- end namespace System -->
<!-- start namespace System.Diagnostics --> <div> 
<h2>Namespace System.Diagnostics</h2>
<!-- start type StackTrace --> <div>
<h3>Type Changed: System.Diagnostics.StackTrace</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void GetFullNameForStackTrace (System.Text.StringBuilder sb, System.Reflection.MethodBase mi);</span>
</pre>
</div>

</div> <!-- end type StackTrace -->

</div> <!-- end namespace System.Diagnostics -->
<!-- start namespace System.Diagnostics.Tracing --> <div> 
<h2>Namespace System.Diagnostics.Tracing</h2>
<!-- start type EventAttribute --> <div>
<h3>Type Changed: System.Diagnostics.Tracing.EventAttribute</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public EventChannel Channel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventOpcode Opcode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventTask Task { get; set; }</span>
</pre>
</div>

</div> <!-- end type EventAttribute -->
<div> <!-- start type EventListener -->
<h3>New Type System.Diagnostics.Tracing.EventListener</h3>
<pre class='added' data-is-non-breaking="">
public abstract class EventListener : System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected EventListener ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void DisableEvents (EventSource eventSource);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void EnableEvents (EventSource eventSource, EventLevel level);</span>
	<span class='added added-method ' data-is-non-breaking="">public void EnableEvents (EventSource eventSource, EventLevel level, EventKeywords matchAnyKeyword);</span>
	<span class='added added-method ' data-is-non-breaking="">public void EnableEvents (EventSource eventSource, EventLevel level, EventKeywords matchAnyKeyword, System.Collections.Generic.IDictionary&lt;System.String,System.String&gt; arguments);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int EventSourceIndex (EventSource eventSource);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void OnEventSourceCreated (EventSource eventSource);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void OnEventWritten (EventWrittenEventArgs eventData);</span>
}
</pre>
</div> <!-- end type EventListener -->
<div> <!-- start type EventWrittenEventArgs -->
<h3>New Type System.Diagnostics.Tracing.EventWrittenEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class EventWrittenEventArgs : System.EventArgs {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Guid ActivityId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventChannel Channel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int EventId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string EventName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventSource EventSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventKeywords Keywords { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventLevel Level { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventOpcode Opcode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.ObjectModel.ReadOnlyCollection&lt;object&gt; Payload { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.ObjectModel.ReadOnlyCollection&lt;string&gt; PayloadNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Guid RelatedActivityId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventTags Tags { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventTask Task { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte Version { get; }</span>
}
</pre>
</div> <!-- end type EventWrittenEventArgs -->

</div> <!-- end namespace System.Diagnostics.Tracing -->
<!-- start namespace System.IO --> <div> 
<h2>Namespace System.IO</h2>
<!-- start type DirectoryInfo --> <div>
<h3>Type Changed: System.IO.DirectoryInfo</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.Runtime.Serialization.ISerializable</span>
</pre>
</div>

</div> <!-- end type DirectoryInfo -->
<!-- start type FileInfo --> <div>
<h3>Type Changed: System.IO.FileInfo</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.Runtime.Serialization.ISerializable</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public FileInfo Replace (string destinationFileName, string destinationBackupFileName);</span>
	<span class='added added-method ' data-is-non-breaking="">public FileInfo Replace (string destinationFileName, string destinationBackupFileName, bool ignoreMetadataErrors);</span>
</pre>
</div>

</div> <!-- end type FileInfo -->
<!-- start type FileSystemInfo --> <div>
<h3>Type Changed: System.IO.FileSystemInfo</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.Runtime.Serialization.ISerializable</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);</span>
</pre>
</div>

</div> <!-- end type FileSystemInfo -->

</div> <!-- end namespace System.IO -->
<!-- start namespace System.Runtime.InteropServices --> <div> 
<h2>Namespace System.Runtime.InteropServices</h2>
<!-- start type ExternalException --> <div>
<h3>Type Changed: System.Runtime.InteropServices.ExternalException</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type ExternalException -->
<div> <!-- start type CustomQueryInterfaceResult -->
<h3>New Type System.Runtime.InteropServices.CustomQueryInterfaceResult</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CustomQueryInterfaceResult {
	<span class='added added-field ' data-is-non-breaking="">Failed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Handled = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NotHandled = 1,</span>
}
</pre>
</div> <!-- end type CustomQueryInterfaceResult -->
<div> <!-- start type ICustomQueryInterface -->
<h3>New Type System.Runtime.InteropServices.ICustomQueryInterface</h3>
<pre class='added' data-is-non-breaking="">
public interface ICustomQueryInterface {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CustomQueryInterfaceResult GetInterface (ref System.Guid iid, out IntPtr ppv);</span>
}
</pre>
</div> <!-- end type ICustomQueryInterface -->

</div> <!-- end namespace System.Runtime.InteropServices -->
<!-- start namespace System.Security --> <div> 
<h2>Namespace System.Security</h2>
<!-- start type CodeAccessPermission --> <div>
<h3>Type Changed: System.Security.CodeAccessPermission</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("CAS support is removed by linker")]
	public virtual void Assert ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("CAS support is removed by linker")]
	public virtual void Demand ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("CAS support is removed by linker")]
	public virtual void Deny ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("CAS support is removed by linker")]
	public virtual void PermitOnly ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("CAS support is removed by linker")]
	public static void RevertAll ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("CAS support is removed by linker")]
	public static void RevertAssert ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("CAS support is removed by linker")]
	public static void RevertDeny ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("CAS support is removed by linker")]
	public static void RevertPermitOnly ();</span>
</div></pre>

</div> <!-- end type CodeAccessPermission -->

</div> <!-- end namespace System.Security -->
<!-- start namespace System.Security.Principal --> <div> 
<h2>Namespace System.Security.Principal</h2>
<!-- start type WindowsIdentity --> <div>
<h3>Type Changed: System.Security.Principal.WindowsIdentity</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeAccessTokenHandle AccessToken { get; }</span>
</pre>
</div>

</div> <!-- end type WindowsIdentity -->

</div> <!-- end namespace System.Security.Principal -->
<!-- start namespace System.Threading --> <div> 
<h2>Namespace System.Threading</h2>
<!-- start type EventWaitHandle --> <div>
<h3>Type Changed: System.Threading.EventWaitHandle</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool explicitDisposing);</span>
</pre>
</div>

</div> <!-- end type EventWaitHandle -->

</div> <!-- end namespace System.Threading -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/2.1/System.html'>System.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type Uri --> <div>
<h3>Type Changed: System.Uri</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string IdnHost { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("The method has been deprecated. It is not used by the system. http://go.microsoft.com/fwlink/?linkid=14202")]
	protected virtual void Canonicalize ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("The method has been deprecated. It is not used by the system. http://go.microsoft.com/fwlink/?linkid=14202")]
	protected virtual void CheckSecurity ();</span>
</pre>
</div>

</div> <!-- end type Uri -->
<!-- start type UriParser --> <div>
<h3>Type Changed: System.UriParser</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual string GetComponents (Uri uri, UriComponents components, UriFormat format)
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual void InitializeAndValidate (Uri uri, out UriFormatException parsingError)
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual bool IsBaseOf (Uri baseUri, Uri relativeUri)
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual bool IsWellFormedOriginalString (Uri uri)
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual UriParser OnNewUri ()
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual string Resolve (Uri baseUri, Uri relativeUri, out UriFormatException parsingError)
</div></pre>

</div> <!-- end type UriParser -->
<div> <!-- start type GopherStyleUriParser -->
<h3>New Type System.GopherStyleUriParser</h3>
<pre class='added' data-is-non-breaking="">
public class GopherStyleUriParser : System.UriParser {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GopherStyleUriParser ();</span>
}
</pre>
</div> <!-- end type GopherStyleUriParser -->
<div> <!-- start type LdapStyleUriParser -->
<h3>New Type System.LdapStyleUriParser</h3>
<pre class='added' data-is-non-breaking="">
public class LdapStyleUriParser : System.UriParser {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LdapStyleUriParser ();</span>
}
</pre>
</div> <!-- end type LdapStyleUriParser -->

</div> <!-- end namespace System -->
<!-- start namespace System.Diagnostics --> <div> 
<h2>Namespace System.Diagnostics</h2>
<!-- start type Process --> <div>
<h3>Type Changed: System.Diagnostics.Process</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeProcessHandle SafeHandle { get; }</span>
</pre>
</div>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">protected override void ~Process ();</span>
</pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public Process Start (string fileName, string <span class='removed removed-inline '>username</span> <span class='added '>userName</span>, System.Security.SecureString password, string domain)
</div><div data-is-non-breaking="">	public Process Start (string fileName, string arguments, string <span class='removed removed-inline '>username</span> <span class='added '>userName</span>, System.Security.SecureString password, string domain)
</div></pre>

</div> <!-- end type Process -->
<!-- start type ProcessStartInfo --> <div>
<h3>Type Changed: System.Diagnostics.ProcessStartInfo</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public ProcessStartInfo (string <span class='removed removed-inline '>filename</span> <span class='added '>fileName</span>)
</div><div data-is-non-breaking="">	public ProcessStartInfo (string <span class='removed removed-inline '>filename</span> <span class='added '>fileName</span>, string arguments)
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IDictionary&lt;System.String,System.String&gt; Environment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string PasswordInClearText { get; set; }</span>
</pre>
</div>

</div> <!-- end type ProcessStartInfo -->

</div> <!-- end namespace System.Diagnostics -->
<!-- start namespace System.Net --> <div> 
<h2>Namespace System.Net</h2>
<!-- start type FileWebResponse --> <div>
<h3>Type Changed: System.Net.FileWebResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override bool SupportsHeaders { get; }</span>
</pre>
</div>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='removed removed-method breaking' data-is-breaking="">protected override void ~FileWebResponse ();</span>
</pre>

</div> <!-- end type FileWebResponse -->
<!-- start type FtpWebResponse --> <div>
<h3>Type Changed: System.Net.FtpWebResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override bool SupportsHeaders { get; }</span>
</pre>
</div>

</div> <!-- end type FtpWebResponse -->
<!-- start type HttpWebResponse --> <div>
<h3>Type Changed: System.Net.HttpWebResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override bool SupportsHeaders { get; }</span>
</pre>
</div>

</div> <!-- end type HttpWebResponse -->
<!-- start type IPAddress --> <div>
<h3>Type Changed: System.Net.IPAddress</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool IsIPv4MappedToIPv6 { get; }</span>
</pre>
</div>

</div> <!-- end type IPAddress -->
<!-- start type TransportContext --> <div>
<h3>Type Changed: System.Net.TransportContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.Generic.IEnumerable&lt;System.Security.Authentication.ExtendedProtection.TokenBinding&gt; GetTlsTokenBindings ();</span>
</pre>
</div>

</div> <!-- end type TransportContext -->

</div> <!-- end namespace System.Net -->
<!-- start namespace System.Net.NetworkInformation --> <div> 
<h2>Namespace System.Net.NetworkInformation</h2>
<!-- start type GatewayIPAddressInformationCollection --> <div>
<h3>Type Changed: System.Net.NetworkInformation.GatewayIPAddressInformationCollection</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> GatewayIPAddressInformationCollection ()
</div></pre>

</div> <!-- end type GatewayIPAddressInformationCollection -->
<!-- start type IPGlobalProperties --> <div>
<h3>Type Changed: System.Net.NetworkInformation.IPGlobalProperties</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginGetUnicastAddresses (System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UnicastIPAddressInformationCollection EndGetUnicastAddresses (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UnicastIPAddressInformationCollection GetUnicastAddresses ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;UnicastIPAddressInformationCollection&gt; GetUnicastAddressesAsync ();</span>
</pre>
</div>

</div> <!-- end type IPGlobalProperties -->
<!-- start type IPv6InterfaceProperties --> <div>
<h3>Type Changed: System.Net.NetworkInformation.IPv6InterfaceProperties</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual long GetScopeId (ScopeLevel scopeLevel);</span>
</pre>
</div>

</div> <!-- end type IPv6InterfaceProperties -->
<!-- start type NetworkInformationException --> <div>
<h3>Type Changed: System.Net.NetworkInformation.NetworkInformationException</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Exception</span> <span class='added '>System.ComponentModel.Win32Exception</span>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected NetworkInformationException (System.Runtime.Serialization.SerializationInfo serializationInfo, System.Runtime.Serialization.StreamingContext streamingContext);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>override</span> int ErrorCode { get; }
</div></pre>

</div> <!-- end type NetworkInformationException -->
<!-- start type NetworkInterface --> <div>
<h3>Type Changed: System.Net.NetworkInformation.NetworkInterface</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> string Description { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> string Id { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> bool IsReceiveOnly { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> string Name { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> NetworkInterfaceType NetworkInterfaceType { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> OperationalStatus OperationalStatus { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> long Speed { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> bool SupportsMulticast { get; }
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static int IPv6LoopbackInterfaceIndex { get; }</span>
</pre>
</div>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static System.Net.IPAddress GetNetMask (System.Net.IPAddress address);</span>
</pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> IPInterfaceProperties GetIPProperties ()
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> IPv4InterfaceStatistics GetIPv4Statistics ()
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> PhysicalAddress GetPhysicalAddress ()
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> bool Supports (NetworkInterfaceComponent networkInterfaceComponent)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPInterfaceStatistics GetIPStatistics ();</span>
</pre>
</div>

</div> <!-- end type NetworkInterface -->
<!-- start type NetworkInterfaceType --> <div>
<h3>Type Changed: System.Net.NetworkInformation.NetworkInterfaceType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Wman = 237,</span>
	<span class='added added-field ' data-is-non-breaking="">Wwanpp = 243,</span>
	<span class='added added-field ' data-is-non-breaking="">Wwanpp2 = 244,</span>
</pre>
</div>

</div> <!-- end type NetworkInterfaceType -->
<div> <!-- start type NetworkInformationPermission -->
<h3>New Type System.Net.NetworkInformation.NetworkInformationPermission</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class NetworkInformationPermission : System.Security.CodeAccessPermission, System.Security.IPermission, System.Security.ISecurityEncodable, System.Security.IStackWalk, System.Security.Permissions.IUnrestrictedPermission {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NetworkInformationPermission (NetworkInformationAccess access);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NetworkInformationPermission (System.Security.Permissions.PermissionState state);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NetworkInformationAccess Access { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AddPermission (NetworkInformationAccess access);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.IPermission Copy ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override void FromXml (System.Security.SecurityElement securityElement);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.IPermission Intersect (System.Security.IPermission target);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool IsSubsetOf (System.Security.IPermission target);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsUnrestricted ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.SecurityElement ToXml ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.IPermission Union (System.Security.IPermission target);</span>
}
</pre>
</div> <!-- end type NetworkInformationPermission -->
<div> <!-- start type NetworkInformationPermissionAttribute -->
<h3>New Type System.Net.NetworkInformation.NetworkInformationPermissionAttribute</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class NetworkInformationPermissionAttribute : System.Security.Permissions.CodeAccessSecurityAttribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NetworkInformationPermissionAttribute (System.Security.Permissions.SecurityAction action);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Access { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.IPermission CreatePermission ();</span>
}
</pre>
</div> <!-- end type NetworkInformationPermissionAttribute -->

</div> <!-- end namespace System.Net.NetworkInformation -->
<!-- start namespace System.Net.Security --> <div> 
<h2>Namespace System.Net.Security</h2>
<!-- start type NegotiateStream --> <div>
<h3>Type Changed: System.Net.Security.NegotiateStream</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (System.Net.NetworkCredential credential, string targetName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ChannelBinding binding, string targetName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (System.Net.NetworkCredential credential, string targetName, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel allowedImpersonationLevel);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ChannelBinding binding, string targetName, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel allowedImpersonationLevel);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync (System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy policy);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync (System.Net.NetworkCredential credential, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel requiredImpersonationLevel);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy policy, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel requiredImpersonationLevel);</span>
</pre>
</div>

</div> <!-- end type NegotiateStream -->

</div> <!-- end namespace System.Net.Security -->
<!-- start namespace System.Security.Authentication.ExtendedProtection --> <div> 
<h2>Namespace System.Security.Authentication.ExtendedProtection</h2>
<div> <!-- start type TokenBinding -->
<h3>New Type System.Security.Authentication.ExtendedProtection.TokenBinding</h3>
<pre class='added' data-is-non-breaking="">
public class TokenBinding {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public TokenBindingType BindingType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public byte[] GetRawTokenBindingId ();</span>
}
</pre>
</div> <!-- end type TokenBinding -->
<div> <!-- start type TokenBindingType -->
<h3>New Type System.Security.Authentication.ExtendedProtection.TokenBindingType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TokenBindingType {
	<span class='added added-field ' data-is-non-breaking="">Provided = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Referred = 1,</span>
}
</pre>
</div> <!-- end type TokenBindingType -->

</div> <!-- end namespace System.Security.Authentication.ExtendedProtection -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type Oid --> <div>
<h3>Type Changed: System.Security.Cryptography.Oid</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Oid FromFriendlyName (string friendlyName, OidGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Oid FromOidValue (string oidValue, OidGroup group);</span>
</pre>
</div>

</div> <!-- end type Oid -->

</div> <!-- end namespace System.Security.Cryptography -->
<!-- start namespace Microsoft.Win32.SafeHandles --> <div> 
<h2>New Namespace Microsoft.Win32.SafeHandles</h2>

<div> <!-- start type SafeProcessHandle -->
<h3>New Type Microsoft.Win32.SafeHandles.SafeProcessHandle</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SafeProcessHandle : Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SafeProcessHandle (IntPtr existingHandle, bool ownsHandle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override bool ReleaseHandle ();</span>
}
</pre>
</div> <!-- end type SafeProcessHandle -->
</div> <!-- end namespace Microsoft.Win32.SafeHandles -->

</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/2.1/System.Core.html'>System.Core.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<div> <!-- start type CngKeyBlobFormat -->
<h3>New Type System.Security.Cryptography.CngKeyBlobFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class CngKeyBlobFormat : System.IEquatable&lt;CngKeyBlobFormat&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngKeyBlobFormat (string format);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat EccPrivateBlob { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat EccPublicBlob { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Format { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat GenericPrivateBlob { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat GenericPublicBlob { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat OpaqueTransportBlob { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat Pkcs8PrivateBlob { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (CngKeyBlobFormat other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (CngKeyBlobFormat left, CngKeyBlobFormat right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (CngKeyBlobFormat left, CngKeyBlobFormat right);</span>
}
</pre>
</div> <!-- end type CngKeyBlobFormat -->

</div> <!-- end namespace System.Security.Cryptography -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/2.1/System.Transactions.html'>System.Transactions.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Transactions --> <div> 
<h2>Namespace System.Transactions</h2>
<!-- start type TransactionScope --> <div>
<h3>Type Changed: System.Transactions.TransactionScope</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public TransactionScope (TransactionScopeAsyncFlowOption asyncFlow);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TransactionScope (TransactionScopeOption option, TransactionScopeAsyncFlowOption asyncFlow);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TransactionScope (TransactionScopeOption option, System.TimeSpan timeout, TransactionScopeAsyncFlowOption asyncFlow);</span>
</pre>
</div>

</div> <!-- end type TransactionScope -->
<div> <!-- start type TransactionScopeAsyncFlowOption -->
<h3>New Type System.Transactions.TransactionScopeAsyncFlowOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TransactionScopeAsyncFlowOption {
	<span class='added added-field ' data-is-non-breaking="">Enabled = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Suppress = 0,</span>
}
</pre>
</div> <!-- end type TransactionScopeAsyncFlowOption -->

</div> <!-- end namespace System.Transactions -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/2.1/monotouch.html'>monotouch.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoTouch --> <div> 
<h2>Namespace MonoTouch</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"9.8.0"</span> <span class='added '>"9.9.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace MonoTouch -->
<!-- start namespace MonoTouch.AudioToolbox --> <div> 
<h2>Namespace MonoTouch.AudioToolbox</h2>
<!-- start type MusicSequence --> <div>
<h3>Type Changed: MonoTouch.AudioToolbox.MusicSequence</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public MusicTrack GetTempoTrack ();</span>
</pre>
</div>

</div> <!-- end type MusicSequence -->

</div> <!-- end namespace MonoTouch.AudioToolbox -->
<!-- start namespace MonoTouch.AudioUnit --> <div> 
<h2>Namespace MonoTouch.AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: MonoTouch.AudioUnit.AUAudioUnit</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUHostTransportStateBlock TransportStateBlock { get; set; }</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit -->
<!-- start type AUAudioUnit_AUAudioInputOutputUnit --> <div>
<h3>Type Changed: MonoTouch.AudioUnit.AUAudioUnit_AUAudioInputOutputUnit</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AUInputHandler GetInputHandler (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AURenderPullInputBlock GetOutputProvider (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetInputHandler (AUAudioUnit This, AUInputHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetOutputProvider (AUAudioUnit This, AURenderPullInputBlock provider);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit_AUAudioInputOutputUnit -->
<!-- start type AUImplementorStringFromValueCallback --> <div>
<h3>Type Changed: MonoTouch.AudioUnit.AUImplementorStringFromValueCallback</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual MonoTouch.Foundation.NSString EndInvoke (System.Single]? value, System.IAsyncResult result);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual MonoTouch.Foundation.NSString Invoke (AUParameter param, System.Single]? value);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual string EndInvoke (System.Single]? value, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string Invoke (AUParameter param, System.Single]? value);</span>
</pre>
</div>

</div> <!-- end type AUImplementorStringFromValueCallback -->
<!-- start type AUParameter --> <div>
<h3>Type Changed: MonoTouch.AudioUnit.AUParameter</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (float value, IntPtr originator);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (float value, IntPtr originator, ulong hostTime);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (float value, AUParameterObserverToken originator);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (float value, AUParameterObserverToken originator, ulong hostTime);</span>
</pre>
</div>

</div> <!-- end type AUParameter -->
<!-- start type AUParameterNode --> <div>
<h3>Type Changed: MonoTouch.AudioUnit.AUParameterNode</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>virtual</span> AUImplementorStringFromValueCallback ImplementorStringFromValueCallback { get; set; }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUImplementorDisplayNameWithLengthCallback ImplementorDisplayNameWithLengthCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUImplementorValueFromStringCallback ImplementorValueFromStringCallback { get; set; }</span>
</pre>
</div>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RemoveParameterObserver (IntPtr token);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual IntPtr TokenByAddingParameterObserver (AUParameterObserver observer);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterObserver (AUParameterObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterRecordingObserver (AUParameterRecordingObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveParameterObserver (AUParameterObserverToken token);</span>
</pre>
</div>

</div> <!-- end type AUParameterNode -->
<h3>Removed Type <span class='breaking' data-is-breaking="">MonoTouch.AudioUnit._AUImplementorStringFromValueCallback</span></h3><div> <!-- start type AUHostTransportStateBlock -->
<h3>New Type MonoTouch.AudioUnit.AUHostTransportStateBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUHostTransportStateBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUHostTransportStateBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition);</span>
}
</pre>
</div> <!-- end type AUHostTransportStateBlock -->
<div> <!-- start type AUImplementorDisplayNameWithLengthCallback -->
<h3>New Type MonoTouch.AudioUnit.AUImplementorDisplayNameWithLengthCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUImplementorDisplayNameWithLengthCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUImplementorDisplayNameWithLengthCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AUParameterNode node, int desiredLength, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string Invoke (AUParameterNode node, int desiredLength);</span>
}
</pre>
</div> <!-- end type AUImplementorDisplayNameWithLengthCallback -->
<div> <!-- start type AUImplementorValueFromStringCallback -->
<h3>New Type MonoTouch.AudioUnit.AUImplementorValueFromStringCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUImplementorValueFromStringCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUImplementorValueFromStringCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AUParameter param, string str, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float Invoke (AUParameter param, string str);</span>
}
</pre>
</div> <!-- end type AUImplementorValueFromStringCallback -->
<div> <!-- start type AUInputHandler -->
<h3>New Type MonoTouch.AudioUnit.AUInputHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUInputHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUInputHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ref AudioUnitRenderActionFlags actionFlags, ref MonoTouch.AudioToolbox.AudioTimeStamp timestamp, uint frameCount, int inputBusNumber, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref AudioUnitRenderActionFlags actionFlags, ref MonoTouch.AudioToolbox.AudioTimeStamp timestamp, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (ref AudioUnitRenderActionFlags actionFlags, ref MonoTouch.AudioToolbox.AudioTimeStamp timestamp, uint frameCount, int inputBusNumber);</span>
}
</pre>
</div> <!-- end type AUInputHandler -->
<div> <!-- start type AUParameterObserverToken -->
<h3>New Type MonoTouch.AudioUnit.AUParameterObserverToken</h3>
<pre class='added' data-is-non-breaking="">
public struct AUParameterObserverToken {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public IntPtr ObserverToken;</span>
}
</pre>
</div> <!-- end type AUParameterObserverToken -->
<div> <!-- start type AUParameterRecordingObserver -->
<h3>New Type MonoTouch.AudioUnit.AUParameterRecordingObserver</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUParameterRecordingObserver : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUParameterRecordingObserver (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (int numberOfEvents, ref AURecordedParameterEvent events, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref AURecordedParameterEvent events, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (int numberOfEvents, ref AURecordedParameterEvent events);</span>
}
</pre>
</div> <!-- end type AUParameterRecordingObserver -->
<div> <!-- start type AURecordedParameterEvent -->
<h3>New Type MonoTouch.AudioUnit.AURecordedParameterEvent</h3>
<pre class='added' data-is-non-breaking="">
public struct AURecordedParameterEvent {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ulong Address;</span>
	<span class='added added-field ' data-is-non-breaking="">public ulong HostTime;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Value;</span>
}
</pre>
</div> <!-- end type AURecordedParameterEvent -->

</div> <!-- end namespace MonoTouch.AudioUnit -->
<!-- start namespace MonoTouch.CoreData --> <div> 
<h2>Namespace MonoTouch.CoreData</h2>
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: MonoTouch.CoreData.NSEntityDescription</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RenamingIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSManagedObject --> <div>
<h3>Type Changed: MonoTouch.CoreData.NSManagedObject</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FaultingState { get; }</span>
</pre>
</div>

</div> <!-- end type NSManagedObject -->
<!-- start type NSMappingModel --> <div>
<h3>Type Changed: MonoTouch.CoreData.NSMappingModel</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSMappingModel GetInferredMappingModel (NSManagedObjectModel source, NSManagedObjectModel destination, out MonoTouch.Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSMappingModel -->
<!-- start type NSPropertyDescription --> <div>
<h3>Type Changed: MonoTouch.CoreData.NSPropertyDescription</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RenamingIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSPropertyDescription -->
<div> <!-- start type NSExpressionDescription -->
<h3>New Type MonoTouch.CoreData.NSExpressionDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSExpressionDescription : MonoTouch.CoreData.NSPropertyDescription, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionDescription (MonoTouch.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionDescription (MonoTouch.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoTouch.Foundation.NSExpression Expression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAttributeType ResultType { get; set; }</span>
}
</pre>
</div> <!-- end type NSExpressionDescription -->
<div> <!-- start type NSFetchRequestExpression -->
<h3>New Type MonoTouch.CoreData.NSFetchRequestExpression</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchRequestExpression : MonoTouch.Foundation.NSExpression, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchRequestExpression (MonoTouch.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchRequestExpression (MonoTouch.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchRequestExpression (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoTouch.Foundation.NSExpression Context { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsCountOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoTouch.Foundation.NSExpression Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFetchRequestExpression FromFetch (MonoTouch.Foundation.NSExpression fetch, MonoTouch.Foundation.NSExpression context, bool countOnly);</span>
}
</pre>
</div> <!-- end type NSFetchRequestExpression -->
<div> <!-- start type NSSnapshotEventType -->
<h3>New Type MonoTouch.CoreData.NSSnapshotEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSSnapshotEventType {
	<span class='added added-field ' data-is-non-breaking="">MergePolicy = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">Refresh = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Rollback = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoDeletion = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoInsertion = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoUpdate = 8,</span>
}
</pre>
</div> <!-- end type NSSnapshotEventType -->

</div> <!-- end namespace MonoTouch.CoreData -->
<!-- start namespace MonoTouch.CoreImage --> <div> 
<h2>Namespace MonoTouch.CoreImage</h2>
<!-- start type CIDetectorOptions --> <div>
<h3>Type Changed: MonoTouch.CoreImage.CIDetectorOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CIImageOrientation? ImageOrientation { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIDetectorOptions -->

</div> <!-- end namespace MonoTouch.CoreImage -->
<!-- start namespace MonoTouch.CoreLocation --> <div> 
<h2>Namespace MonoTouch.CoreLocation</h2>
<!-- start type CLLocationCoordinate2D --> <div>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationCoordinate2D</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type CLLocationCoordinate2D -->

</div> <!-- end namespace MonoTouch.CoreLocation -->
<!-- start namespace MonoTouch.CoreMedia --> <div> 
<h2>Namespace MonoTouch.CoreMedia</h2>
<!-- start type CMBlockBuffer --> <div>
<h3>Type Changed: MonoTouch.CoreMedia.CMBlockBuffer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICMAttachmentBearer</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError AppendMemoryBlock (byte[] data, uint offsetToData, CMBlockBufferFlags flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError CopyDataBytes (uint offsetToData, uint dataLength, out byte[] destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CMBlockBuffer FromMemoryBlock (byte[] data, uint offsetToData, CMBlockBufferFlags flags, out CMBlockBufferError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError ReplaceDataBytes (byte[] sourceBytes, uint offsetIntoDestination);</span>
</pre>
</div>

</div> <!-- end type CMBlockBuffer -->
<!-- start type CMSampleBuffer --> <div>
<h3>Type Changed: MonoTouch.CoreMedia.CMSampleBuffer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICMAttachmentBearer</span>
</pre>
</div>

</div> <!-- end type CMSampleBuffer -->
<div> <!-- start type CMAttachmentBearer -->
<h3>New Type MonoTouch.CoreMedia.CMAttachmentBearer</h3>
<pre class='added' data-is-non-breaking="">
public static class CMAttachmentBearer {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static T GetAttachment&lt;T&gt; (ICMAttachmentBearer target, string key, out CMAttachmentMode attachmentModeOut);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MonoTouch.Foundation.NSDictionary GetAttachments (ICMAttachmentBearer target, CMAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PropagateAttachments (ICMAttachmentBearer source, ICMAttachmentBearer destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAllAttachments (ICMAttachmentBearer target);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAttachment (ICMAttachmentBearer target, string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAttachment (ICMAttachmentBearer target, string key, MonoTouch.ObjCRuntime.INativeObject value, CMAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAttachments (ICMAttachmentBearer target, MonoTouch.Foundation.NSDictionary theAttachments, CMAttachmentMode attachmentMode);</span>
}
</pre>
</div> <!-- end type CMAttachmentBearer -->
<div> <!-- start type CMAttachmentMode -->
<h3>New Type MonoTouch.CoreMedia.CMAttachmentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CMAttachmentMode {
	<span class='added added-field ' data-is-non-breaking="">ShouldNotPropagate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ShouldPropagate = 1,</span>
}
</pre>
</div> <!-- end type CMAttachmentMode -->
<div> <!-- start type ICMAttachmentBearer -->
<h3>New Type MonoTouch.CoreMedia.ICMAttachmentBearer</h3>
<pre class='added' data-is-non-breaking="">
public interface ICMAttachmentBearer : MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
</div> <!-- end type ICMAttachmentBearer -->

</div> <!-- end namespace MonoTouch.CoreMedia -->
<!-- start namespace MonoTouch.CoreMidi --> <div> 
<h2>Namespace MonoTouch.CoreMidi</h2>
<div> <!-- start type MidiControlTransform -->
<h3>New Type MonoTouch.CoreMidi.MidiControlTransform</h3>
<pre class='added' data-is-non-breaking="">
public struct MidiControlTransform {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MidiControlTransform (MidiTransformControlType controlType, MidiTransformControlType remappedControlType, ushort controlNumber, MidiTransformType transform, short param);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ushort ControlNumber;</span>
	<span class='added added-field ' data-is-non-breaking="">public MidiTransformControlType ControlType;</span>
	<span class='added added-field ' data-is-non-breaking="">public short Param;</span>
	<span class='added added-field ' data-is-non-breaking="">public MidiTransformControlType RemappedControlType;</span>
	<span class='added added-field ' data-is-non-breaking="">public MidiTransformType Transform;</span>
}
</pre>
</div> <!-- end type MidiControlTransform -->
<div> <!-- start type MidiThruConnection -->
<h3>New Type MonoTouch.CoreMidi.MidiThruConnection</h3>
<pre class='added' data-is-non-breaking="">
public class MidiThruConnection : System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MidiThruConnection (uint handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public uint Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MidiThruConnection Create (string persistentOwnerID, MidiThruConnectionParams connectionParams);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MidiThruConnection Create (string persistentOwnerID, MidiThruConnectionParams connectionParams, out MidiError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MidiThruConnection[] Find (string persistentOwnerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MidiThruConnection[] Find (string persistentOwnerID, out MidiError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public MidiThruConnectionParams GetParams ();</span>
	<span class='added added-method ' data-is-non-breaking="">public MidiThruConnectionParams GetParams (out MidiError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public MidiError SetParams (MidiThruConnectionParams connectionParams);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~MidiThruConnection ();</span>
}
</pre>
</div> <!-- end type MidiThruConnection -->
<div> <!-- start type MidiThruConnectionEndpoint -->
<h3>New Type MonoTouch.CoreMidi.MidiThruConnectionEndpoint</h3>
<pre class='added' data-is-non-breaking="">
public struct MidiThruConnectionEndpoint {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MidiThruConnectionEndpoint (int endpointRef, int uniqueID);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public int EndpointRef;</span>
	<span class='added added-field ' data-is-non-breaking="">public int UniqueID;</span>
}
</pre>
</div> <!-- end type MidiThruConnectionEndpoint -->
<div> <!-- start type MidiThruConnectionParams -->
<h3>New Type MonoTouch.CoreMidi.MidiThruConnectionParams</h3>
<pre class='added' data-is-non-breaking="">
public class MidiThruConnectionParams {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MidiThruConnectionParams ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public byte[] ChannelMap { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform ChannelPressure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiControlTransform[] Controls { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiThruConnectionEndpoint[] Destinations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutAllControls { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutBeatClock { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutMtc { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutSysEx { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutTuneRequest { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte HighNote { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte HighVelocity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform KeyPressure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte LowNote { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte LowVelocity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiValueMap[] Maps { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform NoteNumber { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform PitchBend { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform ProgramChange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiThruConnectionEndpoint[] Sources { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform Velocity { get; set; }</span>
}
</pre>
</div> <!-- end type MidiThruConnectionParams -->
<div> <!-- start type MidiTransform -->
<h3>New Type MonoTouch.CoreMidi.MidiTransform</h3>
<pre class='added' data-is-non-breaking="">
public struct MidiTransform {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MidiTransform (MidiTransformType transform, short param);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public short Param;</span>
	<span class='added added-field ' data-is-non-breaking="">public MidiTransformType Transform;</span>
}
</pre>
</div> <!-- end type MidiTransform -->
<div> <!-- start type MidiTransformControlType -->
<h3>New Type MonoTouch.CoreMidi.MidiTransformControlType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MidiTransformControlType {
	<span class='added added-field ' data-is-non-breaking="">FourteenBit = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FourteenBitNRpn = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FourteenBitRpn = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SevenBit = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SevenBitNRpn = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">SevenBitRpn = 2,</span>
}
</pre>
</div> <!-- end type MidiTransformControlType -->
<div> <!-- start type MidiTransformType -->
<h3>New Type MonoTouch.CoreMidi.MidiTransformType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MidiTransformType {
	<span class='added added-field ' data-is-non-breaking="">Add = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">FilterOut = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">MapControl = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MapValue = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">MaxValue = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">MinValue = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Scale = 9,</span>
}
</pre>
</div> <!-- end type MidiTransformType -->
<div> <!-- start type MidiValueMap -->
<h3>New Type MonoTouch.CoreMidi.MidiValueMap</h3>
<pre class='added' data-is-non-breaking="">
public struct MidiValueMap {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public byte[] Value { get; set; }</span>
}
</pre>
</div> <!-- end type MidiValueMap -->

</div> <!-- end namespace MonoTouch.CoreMidi -->
<!-- start namespace MonoTouch.Foundation --> <div> 
<h2>Namespace MonoTouch.Foundation</h2>
<!-- start type NSExpression --> <div>
<h3>Type Changed: MonoTouch.Foundation.NSExpression</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSExpressionCallbackHandler Block { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("ValueWithObject is deprecated, please use EvaluateWith instead.")]
	public NSExpression ExpressionValueWithObject (NSObject object1, NSMutableDictionary context);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFormat (string, NSExpression[]) is deprecated, please use FromFormat (string, NSObject[]) instead.")]
	public NSExpression FromFormat (string format, NSExpression[] parameters);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFunction (NSExpressionHandler, NSExpression[]) is deprecated, please use FromFunction (NSExpressionCallbackHandler, NSExpression[]) instead.")]
	public NSExpression FromFunction (NSExpressionHandler target, NSExpression[] parameters);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> NSExpression ExpressionValueWithObject (NSObject object1, NSMutableDictionary context)
</div><div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>static</span> public NSExpression FromFormat (string format, NSExpression[] parameters)
</div><div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>static</span> public NSExpression FromFunction (NSExpressionHandler target, NSExpression[] parameters)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject EvaluateWith (NSObject obj, NSMutableDictionary context);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFormat (string expressionFormat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFormat (string format, NSObject[] parameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFunction (NSExpressionCallbackHandler target, NSExpression[] parameters);</span>
</pre>
</div>

</div> <!-- end type NSExpression -->
<!-- start type NSObject --> <div>
<h3>Type Changed: MonoTouch.Foundation.NSObject</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use PlatformAssembly for easier code sharing across platforms")]
	public static System.Reflection.Assembly MonoTouchAssembly;</span>
</div></pre>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static System.Reflection.Assembly PlatformAssembly;</span>
</pre>
</div>

</div> <!-- end type NSObject -->
<!-- start type NSUrl --> <div>
<h3>Type Changed: MonoTouch.Foundation.NSUrl</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NSUrl x, NSUrl y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NSUrl x, NSUrl y);</span>
</pre>
</div>

</div> <!-- end type NSUrl -->
<div> <!-- start type NSExpressionCallbackHandler -->
<h3>New Type MonoTouch.Foundation.NSExpressionCallbackHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSExpressionCallbackHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionCallbackHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSObject evaluatedObject, NSExpression[] expressions, NSMutableDictionary context, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Invoke (NSObject evaluatedObject, NSExpression[] expressions, NSMutableDictionary context);</span>
}
</pre>
</div> <!-- end type NSExpressionCallbackHandler -->

</div> <!-- end namespace MonoTouch.Foundation -->
<!-- start namespace MonoTouch.GameKit --> <div> 
<h2>Namespace MonoTouch.GameKit</h2>
<!-- start type GKLocalPlayerListener --> <div>
<h3>Type Changed: MonoTouch.GameKit.GKLocalPlayerListener</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);</span>
</pre>

</div> <!-- end type GKLocalPlayerListener -->

</div> <!-- end namespace MonoTouch.GameKit -->
<!-- start namespace MonoTouch.MapKit --> <div> 
<h2>Namespace MonoTouch.MapKit</h2>
<!-- start type MKCoordinateRegion --> <div>
<h3>Type Changed: MonoTouch.MapKit.MKCoordinateRegion</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type MKCoordinateRegion -->
<!-- start type MKCoordinateSpan --> <div>
<h3>Type Changed: MonoTouch.MapKit.MKCoordinateSpan</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type MKCoordinateSpan -->

</div> <!-- end namespace MonoTouch.MapKit -->
<!-- start namespace MonoTouch.MediaPlayer --> <div> 
<h2>Namespace MonoTouch.MediaPlayer</h2>
<!-- start type MPMoviePlayerController --> <div>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AirPlayVideoActive { get; }</span>
</pre>
</div>

</div> <!-- end type MPMoviePlayerController -->
<!-- start type MPMusicPlayerController --> <div>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint IndexOfNowPlayingItem { get; }</span>
</pre>
</div>

</div> <!-- end type MPMusicPlayerController -->
<div> <!-- start type MPErrorCodeExtensions -->
<h3>New Type MonoTouch.MediaPlayer.MPErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MonoTouch.Foundation.NSString GetDomain (MPErrorCode self);</span>
}
</pre>
</div> <!-- end type MPErrorCodeExtensions -->

</div> <!-- end namespace MonoTouch.MediaPlayer -->
<!-- start namespace MonoTouch.ObjCRuntime --> <div> 
<h2>Namespace MonoTouch.ObjCRuntime</h2>
<!-- start type Runtime --> <div>
<h3>Type Changed: MonoTouch.ObjCRuntime.Runtime</h3>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event MarshalManagedExceptionHandler MarshalManagedException;</span>
	<span class='added added-event ' data-is-non-breaking="">public event MarshalObjectiveCExceptionHandler MarshalObjectiveCException;</span>
</pre>
</div>

</div> <!-- end type Runtime -->
<div> <!-- start type MarshalManagedExceptionEventArgs -->
<h3>New Type MonoTouch.ObjCRuntime.MarshalManagedExceptionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class MarshalManagedExceptionEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalManagedExceptionEventArgs ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Exception Exception { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MarshalManagedExceptionMode ExceptionMode { get; set; }</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionEventArgs -->
<div> <!-- start type MarshalManagedExceptionHandler -->
<h3>New Type MonoTouch.ObjCRuntime.MarshalManagedExceptionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MarshalManagedExceptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalManagedExceptionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, MarshalManagedExceptionEventArgs args, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, MarshalManagedExceptionEventArgs args);</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionHandler -->
<div> <!-- start type MarshalManagedExceptionMode -->
<h3>New Type MonoTouch.ObjCRuntime.MarshalManagedExceptionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MarshalManagedExceptionMode {
	<span class='added added-field ' data-is-non-breaking="">Abort = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ThrowObjectiveCException = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UnwindNativeCode = 1,</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionMode -->
<div> <!-- start type MarshalObjectiveCExceptionEventArgs -->
<h3>New Type MonoTouch.ObjCRuntime.MarshalObjectiveCExceptionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class MarshalObjectiveCExceptionEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalObjectiveCExceptionEventArgs ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public MonoTouch.Foundation.NSException Exception { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MarshalObjectiveCExceptionMode ExceptionMode { get; set; }</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionEventArgs -->
<div> <!-- start type MarshalObjectiveCExceptionHandler -->
<h3>New Type MonoTouch.ObjCRuntime.MarshalObjectiveCExceptionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MarshalObjectiveCExceptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalObjectiveCExceptionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, MarshalObjectiveCExceptionEventArgs args, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, MarshalObjectiveCExceptionEventArgs args);</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionHandler -->
<div> <!-- start type MarshalObjectiveCExceptionMode -->
<h3>New Type MonoTouch.ObjCRuntime.MarshalObjectiveCExceptionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MarshalObjectiveCExceptionMode {
	<span class='added added-field ' data-is-non-breaking="">Abort = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ThrowManagedException = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UnwindManagedCode = 1,</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionMode -->

</div> <!-- end namespace MonoTouch.ObjCRuntime -->
<!-- start namespace MonoTouch.Security --> <div> 
<h2>Namespace MonoTouch.Security</h2>
<div> <!-- start type SecSharedCredential -->
<h3>New Type MonoTouch.Security.SecSharedCredential</h3>
<pre class='added' data-is-non-breaking="">
public static class SecSharedCredential {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MonoTouch.Foundation.NSString SharedPassword { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AddSharedWebCredential (string domainName, string account, string password, System.Action&lt;MonoTouch.Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string CreateSharedWebCredentialPassword ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestSharedWebCredential (string domainName, string account, System.Action&lt;System.String[],MonoTouch.Foundation.NSError&gt; handler);</span>
}
</pre>
</div> <!-- end type SecSharedCredential -->

</div> <!-- end namespace MonoTouch.Security -->
<!-- start namespace MonoTouch.SpriteKit --> <div> 
<h2>Namespace MonoTouch.SpriteKit</h2>
<!-- start type SKVideoNode --> <div>
<h3>Type Changed: MonoTouch.SpriteKit.SKVideoNode</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public SKVideoNode FromUrl (MonoTouch.Foundation.NSUrl <span class='removed removed-inline '>videoURL</span> <span class='added '>videoUrl</span>)
</div></pre>

</div> <!-- end type SKVideoNode -->

</div> <!-- end namespace MonoTouch.SpriteKit -->
<!-- start namespace MonoTouch.UIKit --> <div> 
<h2>Namespace MonoTouch.UIKit</h2>
<!-- start type UIMenuController --> <div>
<h3>Type Changed: MonoTouch.UIKit.UIMenuController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoTouch.Foundation.NSString MenuFrameDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type UIMenuController.Notifications --> <div>
<h3>Type Changed: MonoTouch.UIKit.UIMenuController.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MonoTouch.Foundation.NSObject ObserveMenuFrameDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIMenuController.Notifications -->

</div> <!-- end type UIMenuController -->
<!-- start type UIPopoverPresentationController --> <div>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverPresentationController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public UIAdaptivePresentationStyleWithTraitsRequested GetAdaptivePresentationStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public UIAdaptivePresentationWithStyleRequested GetViewControllerForAdaptivePresentation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ShouldDismiss ShouldDismissPopover { get; set; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidDismiss;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler PrepareForPresentation;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;UIWillPresentAdaptiveStyleEventArgs&gt; WillPresentController;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;UIPopoverPresentationControllerRepositionEventArgs&gt; WillReposition;</span>
</pre>
</div>

</div> <!-- end type UIPopoverPresentationController -->
<!-- start type UIUserNotificationAction --> <div>
<h3>Type Changed: MonoTouch.UIKit.UIUserNotificationAction</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoTouch.Foundation.NSString ResponseTypedTextKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoTouch.Foundation.NSString TextInputActionButtonTitleKey { get; }</span>
</pre>
</div>

</div> <!-- end type UIUserNotificationAction -->
<div> <!-- start type ShouldDismiss -->
<h3>New Type MonoTouch.UIKit.ShouldDismiss</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ShouldDismiss : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ShouldDismiss (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UIPopoverPresentationController popoverPresentationController, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (UIPopoverPresentationController popoverPresentationController);</span>
}
</pre>
</div> <!-- end type ShouldDismiss -->
<div> <!-- start type UIAdaptivePresentationStyleWithTraitsRequested -->
<h3>New Type MonoTouch.UIKit.UIAdaptivePresentationStyleWithTraitsRequested</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UIAdaptivePresentationStyleWithTraitsRequested : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIAdaptivePresentationStyleWithTraitsRequested (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UIPresentationController controller, UITraitCollection traitCollection, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIModalPresentationStyle EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIModalPresentationStyle Invoke (UIPresentationController controller, UITraitCollection traitCollection);</span>
}
</pre>
</div> <!-- end type UIAdaptivePresentationStyleWithTraitsRequested -->
<div> <!-- start type UIAdaptivePresentationWithStyleRequested -->
<h3>New Type MonoTouch.UIKit.UIAdaptivePresentationWithStyleRequested</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UIAdaptivePresentationWithStyleRequested : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIAdaptivePresentationWithStyleRequested (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UIPresentationController controller, UIModalPresentationStyle style, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIViewController EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIViewController Invoke (UIPresentationController controller, UIModalPresentationStyle style);</span>
}
</pre>
</div> <!-- end type UIAdaptivePresentationWithStyleRequested -->
<div> <!-- start type UIPasteboardNames -->
<h3>New Type MonoTouch.UIKit.UIPasteboardNames</h3>
<pre class='added' data-is-non-breaking="">
public static class UIPasteboardNames {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MonoTouch.Foundation.NSString Find { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoTouch.Foundation.NSString General { get; }</span>
}
</pre>
</div> <!-- end type UIPasteboardNames -->
<div> <!-- start type UIPopoverPresentationControllerRepositionEventArgs -->
<h3>New Type MonoTouch.UIKit.UIPopoverPresentationControllerRepositionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class UIPopoverPresentationControllerRepositionEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIPopoverPresentationControllerRepositionEventArgs (System.Drawing.RectangleF targetRect, UIView inView);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public UIView InView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Drawing.RectangleF TargetRect { get; set; }</span>
}
</pre>
</div> <!-- end type UIPopoverPresentationControllerRepositionEventArgs -->
<div> <!-- start type UIWillPresentAdaptiveStyleEventArgs -->
<h3>New Type MonoTouch.UIKit.UIWillPresentAdaptiveStyleEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class UIWillPresentAdaptiveStyleEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIWillPresentAdaptiveStyleEventArgs (UIModalPresentationStyle style, IUIViewControllerTransitionCoordinator transitionCoordinator);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public UIModalPresentationStyle Style { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IUIViewControllerTransitionCoordinator TransitionCoordinator { get; set; }</span>
}
</pre>
</div> <!-- end type UIWillPresentAdaptiveStyleEventArgs -->

</div> <!-- end namespace MonoTouch.UIKit -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/2.1/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoTouch.NUnit.UI --> <div> 
<h2>Namespace MonoTouch.NUnit.UI</h2>
<!-- start type TouchOptions --> <div>
<h3>Type Changed: MonoTouch.NUnit.UI.TouchOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string Transport { get; set; }</span>
</pre>
</div>

</div> <!-- end type TouchOptions -->

</div> <!-- end namespace MonoTouch.NUnit.UI -->
<!-- start namespace NUnit.Framework --> <div> 
<h2>Namespace NUnit.Framework</h2>
<!-- start type Assert --> <div>
<h3>Type Changed: NUnit.Framework.Assert</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (object anObject, string message, object[] args);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual, string message);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual, string message, object[] args);</span>
</pre>
</div>

</div> <!-- end type Assert -->

</div> <!-- end namespace NUnit.Framework -->
<!-- start namespace NUnit.Framework.Internal --> <div> 
<h2>Namespace NUnit.Framework.Internal</h2>
<!-- start type NUnitLiteTestAssemblyRunner --> <div>
<h3>Type Changed: NUnit.Framework.Internal.NUnitLiteTestAssemblyRunner</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public NUnitLiteTestAssemblyRunner (NUnit.Framework.Api.ITestAssemblyBuilder builder);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NUnitLiteTestAssemblyRunner (NUnit.Framework.Api.ITestAssemblyBuilder builder, FinallyDelegate finallyDelegate);</span>
</pre>
</div>

</div> <!-- end type NUnitLiteTestAssemblyRunner -->
<!-- start type Test --> <div>
<h3>Type Changed: NUnit.Framework.Internal.Test</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate finD);</span>
</pre>
</div>

</div> <!-- end type Test -->
<!-- start type TestMethod --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestMethod</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type TestMethod -->
<!-- start type TestResult --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestResult</h3>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public bool ThreadCrashFail;</span>
</pre>
</div>

</div> <!-- end type TestResult -->
<!-- start type TestSuite --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestSuite</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate finD);</span>
</pre>
</div>

</div> <!-- end type TestSuite -->
<div> <!-- start type FinallyDelegate -->
<h3>New Type NUnit.Framework.Internal.FinallyDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class FinallyDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FinallyDelegate ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Complete ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void HandleUnhandledExc (System.Exception ex);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Set (TestExecutionContext context, long startTicks, TestResult result);</span>
}
</pre>
</div> <!-- end type FinallyDelegate -->

</div> <!-- end namespace NUnit.Framework.Internal -->
<!-- start namespace NUnit.Framework.Internal.WorkItems --> <div> 
<h2>Namespace NUnit.Framework.Internal.WorkItems</h2>
<!-- start type CompositeWorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.CompositeWorkItem</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CompositeWorkItem (NUnit.Framework.Internal.TestSuite suite, NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CompositeWorkItem (NUnit.Framework.Internal.TestSuite suite, NUnit.Framework.Api.ITestFilter childFilter, NUnit.Framework.Internal.FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type CompositeWorkItem -->
<!-- start type SimpleWorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.SimpleWorkItem</h3>
<p>Removed constructors:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.Commands.TestCommand command);</span>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.TestMethod test);</span>
</pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.Commands.TestCommand command, NUnit.Framework.Internal.FinallyDelegate fd);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.TestMethod test, NUnit.Framework.Internal.FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type SimpleWorkItem -->
<!-- start type WorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.WorkItem</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public WorkItem (NUnit.Framework.Internal.Test test);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public WorkItem (NUnit.Framework.Internal.Test test, NUnit.Framework.Internal.FinallyDelegate finallyDelegate);</span>
</pre>
</div>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">protected NUnit.Framework.Internal.FinallyDelegate finD;</span>
</pre>
</div>

</div> <!-- end type WorkItem -->

</div> <!-- end namespace NUnit.Framework.Internal.WorkItems -->
<!-- start namespace NUnitLite.Runner --> <div> 
<h2>Namespace NUnitLite.Runner</h2>
<!-- start type TextUI --> <div>
<h3>Type Changed: NUnitLite.Runner.TextUI</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void TopLevelHandler (object sender, System.UnhandledExceptionEventArgs e);</span>
</pre>
</div>

</div> <!-- end type TextUI -->

</div> <!-- end namespace NUnitLite.Runner -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.iOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoTouch.NUnit.UI --> <div> 
<h2>Namespace MonoTouch.NUnit.UI</h2>
<!-- start type TouchOptions --> <div>
<h3>Type Changed: MonoTouch.NUnit.UI.TouchOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string Transport { get; set; }</span>
</pre>
</div>

</div> <!-- end type TouchOptions -->

</div> <!-- end namespace MonoTouch.NUnit.UI -->
<!-- start namespace NUnit.Framework --> <div> 
<h2>Namespace NUnit.Framework</h2>
<!-- start type Assert --> <div>
<h3>Type Changed: NUnit.Framework.Assert</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (object anObject, string message, object[] args);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual, string message);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual, string message, object[] args);</span>
</pre>
</div>

</div> <!-- end type Assert -->

</div> <!-- end namespace NUnit.Framework -->
<!-- start namespace NUnit.Framework.Internal --> <div> 
<h2>Namespace NUnit.Framework.Internal</h2>
<!-- start type NUnitLiteTestAssemblyRunner --> <div>
<h3>Type Changed: NUnit.Framework.Internal.NUnitLiteTestAssemblyRunner</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public NUnitLiteTestAssemblyRunner (NUnit.Framework.Api.ITestAssemblyBuilder builder);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NUnitLiteTestAssemblyRunner (NUnit.Framework.Api.ITestAssemblyBuilder builder, FinallyDelegate finallyDelegate);</span>
</pre>
</div>

</div> <!-- end type NUnitLiteTestAssemblyRunner -->
<!-- start type Test --> <div>
<h3>Type Changed: NUnit.Framework.Internal.Test</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate finD);</span>
</pre>
</div>

</div> <!-- end type Test -->
<!-- start type TestMethod --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestMethod</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type TestMethod -->
<!-- start type TestResult --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestResult</h3>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public bool ThreadCrashFail;</span>
</pre>
</div>

</div> <!-- end type TestResult -->
<!-- start type TestSuite --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestSuite</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate finD);</span>
</pre>
</div>

</div> <!-- end type TestSuite -->
<div> <!-- start type FinallyDelegate -->
<h3>New Type NUnit.Framework.Internal.FinallyDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class FinallyDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FinallyDelegate ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Complete ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void HandleUnhandledExc (System.Exception ex);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Set (TestExecutionContext context, long startTicks, TestResult result);</span>
}
</pre>
</div> <!-- end type FinallyDelegate -->

</div> <!-- end namespace NUnit.Framework.Internal -->
<!-- start namespace NUnit.Framework.Internal.WorkItems --> <div> 
<h2>Namespace NUnit.Framework.Internal.WorkItems</h2>
<!-- start type CompositeWorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.CompositeWorkItem</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CompositeWorkItem (NUnit.Framework.Internal.TestSuite suite, NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CompositeWorkItem (NUnit.Framework.Internal.TestSuite suite, NUnit.Framework.Api.ITestFilter childFilter, NUnit.Framework.Internal.FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type CompositeWorkItem -->
<!-- start type SimpleWorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.SimpleWorkItem</h3>
<p>Removed constructors:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.Commands.TestCommand command);</span>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.TestMethod test);</span>
</pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.Commands.TestCommand command, NUnit.Framework.Internal.FinallyDelegate fd);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.TestMethod test, NUnit.Framework.Internal.FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type SimpleWorkItem -->
<!-- start type WorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.WorkItem</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public WorkItem (NUnit.Framework.Internal.Test test);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public WorkItem (NUnit.Framework.Internal.Test test, NUnit.Framework.Internal.FinallyDelegate finallyDelegate);</span>
</pre>
</div>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">protected NUnit.Framework.Internal.FinallyDelegate finD;</span>
</pre>
</div>

</div> <!-- end type WorkItem -->

</div> <!-- end namespace NUnit.Framework.Internal.WorkItems -->
<!-- start namespace NUnitLite.Runner --> <div> 
<h2>Namespace NUnitLite.Runner</h2>
<!-- start type TextUI --> <div>
<h3>Type Changed: NUnitLite.Runner.TextUI</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void TopLevelHandler (object sender, System.UnhandledExceptionEventArgs e);</span>
</pre>
</div>

</div> <!-- end type TextUI -->

</div> <!-- end namespace NUnitLite.Runner -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.iOS/Xamarin.iOS.html'>Xamarin.iOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AudioToolbox --> <div> 
<h2>Namespace AudioToolbox</h2>
<!-- start type MusicSequence --> <div>
<h3>Type Changed: AudioToolbox.MusicSequence</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public MusicTrack GetTempoTrack ();</span>
</pre>
</div>

</div> <!-- end type MusicSequence -->

</div> <!-- end namespace AudioToolbox -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUHostTransportStateBlock TransportStateBlock { get; set; }</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit -->
<!-- start type AUAudioUnit_AUAudioInputOutputUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit_AUAudioInputOutputUnit</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AUInputHandler GetInputHandler (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AURenderPullInputBlock GetOutputProvider (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetInputHandler (AUAudioUnit This, AUInputHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetOutputProvider (AUAudioUnit This, AURenderPullInputBlock provider);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit_AUAudioInputOutputUnit -->
<!-- start type AUImplementorStringFromValueCallback --> <div>
<h3>Type Changed: AudioUnit.AUImplementorStringFromValueCallback</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual Foundation.NSString EndInvoke (System.Single]? value, System.IAsyncResult result);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual Foundation.NSString Invoke (AUParameter param, System.Single]? value);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual string EndInvoke (System.Single]? value, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string Invoke (AUParameter param, System.Single]? value);</span>
</pre>
</div>

</div> <!-- end type AUImplementorStringFromValueCallback -->
<!-- start type AUParameter --> <div>
<h3>Type Changed: AudioUnit.AUParameter</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (float value, IntPtr originator);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (float value, IntPtr originator, ulong hostTime);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (float value, AUParameterObserverToken originator);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (float value, AUParameterObserverToken originator, ulong hostTime);</span>
</pre>
</div>

</div> <!-- end type AUParameter -->
<!-- start type AUParameterNode --> <div>
<h3>Type Changed: AudioUnit.AUParameterNode</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>virtual</span> AUImplementorStringFromValueCallback ImplementorStringFromValueCallback { get; set; }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUImplementorDisplayNameWithLengthCallback ImplementorDisplayNameWithLengthCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUImplementorValueFromStringCallback ImplementorValueFromStringCallback { get; set; }</span>
</pre>
</div>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RemoveParameterObserver (IntPtr token);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual IntPtr TokenByAddingParameterObserver (AUParameterObserver observer);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterObserver (AUParameterObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterRecordingObserver (AUParameterRecordingObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveParameterObserver (AUParameterObserverToken token);</span>
</pre>
</div>

</div> <!-- end type AUParameterNode -->
<h3>Removed Type <span class='breaking' data-is-breaking="">AudioUnit._AUImplementorStringFromValueCallback</span></h3><div> <!-- start type AUHostTransportStateBlock -->
<h3>New Type AudioUnit.AUHostTransportStateBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUHostTransportStateBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUHostTransportStateBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition);</span>
}
</pre>
</div> <!-- end type AUHostTransportStateBlock -->
<div> <!-- start type AUImplementorDisplayNameWithLengthCallback -->
<h3>New Type AudioUnit.AUImplementorDisplayNameWithLengthCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUImplementorDisplayNameWithLengthCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUImplementorDisplayNameWithLengthCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AUParameterNode node, nint desiredLength, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string Invoke (AUParameterNode node, nint desiredLength);</span>
}
</pre>
</div> <!-- end type AUImplementorDisplayNameWithLengthCallback -->
<div> <!-- start type AUImplementorValueFromStringCallback -->
<h3>New Type AudioUnit.AUImplementorValueFromStringCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUImplementorValueFromStringCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUImplementorValueFromStringCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AUParameter param, string str, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float Invoke (AUParameter param, string str);</span>
}
</pre>
</div> <!-- end type AUImplementorValueFromStringCallback -->
<div> <!-- start type AUInputHandler -->
<h3>New Type AudioUnit.AUInputHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUInputHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUInputHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ref AudioUnitRenderActionFlags actionFlags, ref AudioToolbox.AudioTimeStamp timestamp, uint frameCount, nint inputBusNumber, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref AudioUnitRenderActionFlags actionFlags, ref AudioToolbox.AudioTimeStamp timestamp, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (ref AudioUnitRenderActionFlags actionFlags, ref AudioToolbox.AudioTimeStamp timestamp, uint frameCount, nint inputBusNumber);</span>
}
</pre>
</div> <!-- end type AUInputHandler -->
<div> <!-- start type AUParameterObserverToken -->
<h3>New Type AudioUnit.AUParameterObserverToken</h3>
<pre class='added' data-is-non-breaking="">
public struct AUParameterObserverToken {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public IntPtr ObserverToken;</span>
}
</pre>
</div> <!-- end type AUParameterObserverToken -->
<div> <!-- start type AUParameterRecordingObserver -->
<h3>New Type AudioUnit.AUParameterRecordingObserver</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUParameterRecordingObserver : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUParameterRecordingObserver (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (nint numberOfEvents, ref AURecordedParameterEvent events, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref AURecordedParameterEvent events, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (nint numberOfEvents, ref AURecordedParameterEvent events);</span>
}
</pre>
</div> <!-- end type AUParameterRecordingObserver -->
<div> <!-- start type AURecordedParameterEvent -->
<h3>New Type AudioUnit.AURecordedParameterEvent</h3>
<pre class='added' data-is-non-breaking="">
public struct AURecordedParameterEvent {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ulong Address;</span>
	<span class='added added-field ' data-is-non-breaking="">public ulong HostTime;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Value;</span>
}
</pre>
</div> <!-- end type AURecordedParameterEvent -->
<div> <!-- start type IAUAudioUnitFactory -->
<h3>New Type AudioUnit.IAUAudioUnitFactory</h3>
<pre class='added' data-is-non-breaking="">
public interface IAUAudioUnitFactory : Foundation.INSExtensionRequestHandling, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual AUAudioUnit CreateAudioUnit (AudioComponentDescription desc, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type IAUAudioUnitFactory -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContactStore --> <div>
<h3>Type Changed: Contacts.CNContactStore</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload that takes CNContactStoreListContactsHandler instead")]
	public virtual bool EnumerateContacts (CNContactFetchRequest fetchRequest, out Foundation.NSError error, CNContactStoreEnumerateContactsHandler handler);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool EnumerateContacts (CNContactFetchRequest fetchRequest, out Foundation.NSError error, CNContactStoreListContactsHandler handler);</span>
</pre>
</div>

</div> <!-- end type CNContactStore -->
<div> <!-- start type CNContactStoreListContactsHandler -->
<h3>New Type Contacts.CNContactStoreListContactsHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CNContactStoreListContactsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CNContactStoreListContactsHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CNContact contact, ref bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CNContact contact, ref bool stop);</span>
}
</pre>
</div> <!-- end type CNContactStoreListContactsHandler -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: CoreData.NSEntityDescription</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RenamingIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSManagedObject --> <div>
<h3>Type Changed: CoreData.NSManagedObject</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FaultingState { get; }</span>
</pre>
</div>

</div> <!-- end type NSManagedObject -->
<!-- start type NSMappingModel --> <div>
<h3>Type Changed: CoreData.NSMappingModel</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSMappingModel GetInferredMappingModel (NSManagedObjectModel source, NSManagedObjectModel destination, out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSMappingModel -->
<!-- start type NSPropertyDescription --> <div>
<h3>Type Changed: CoreData.NSPropertyDescription</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RenamingIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSPropertyDescription -->
<div> <!-- start type NSExpressionDescription -->
<h3>New Type CoreData.NSExpressionDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSExpressionDescription : CoreData.NSPropertyDescription, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSExpressionDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSExpressionDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression Expression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAttributeType ResultType { get; set; }</span>
}
</pre>
</div> <!-- end type NSExpressionDescription -->
<div> <!-- start type NSFetchRequestExpression -->
<h3>New Type CoreData.NSFetchRequestExpression</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchRequestExpression : Foundation.NSExpression, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchRequestExpression (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchRequestExpression (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchRequestExpression (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression Context { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsCountOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFetchRequestExpression FromFetch (Foundation.NSExpression fetch, Foundation.NSExpression context, bool countOnly);</span>
}
</pre>
</div> <!-- end type NSFetchRequestExpression -->
<div> <!-- start type NSSnapshotEventType -->
<h3>New Type CoreData.NSSnapshotEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSSnapshotEventType {
	<span class='added added-field ' data-is-non-breaking="">MergePolicy = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">Refresh = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Rollback = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoDeletion = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoInsertion = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoUpdate = 8,</span>
}
</pre>
</div> <!-- end type NSSnapshotEventType -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIDetectorOptions --> <div>
<h3>Type Changed: CoreImage.CIDetectorOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CIImageOrientation? ImageOrientation { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIDetectorOptions -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLLocationCoordinate2D --> <div>
<h3>Type Changed: CoreLocation.CLLocationCoordinate2D</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type CLLocationCoordinate2D -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
<!-- start type CMBlockBuffer --> <div>
<h3>Type Changed: CoreMedia.CMBlockBuffer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICMAttachmentBearer</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError AppendMemoryBlock (byte[] data, uint offsetToData, CMBlockBufferFlags flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError CopyDataBytes (uint offsetToData, uint dataLength, out byte[] destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CMBlockBuffer FromMemoryBlock (byte[] data, uint offsetToData, CMBlockBufferFlags flags, out CMBlockBufferError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError ReplaceDataBytes (byte[] sourceBytes, uint offsetIntoDestination);</span>
</pre>
</div>

</div> <!-- end type CMBlockBuffer -->
<!-- start type CMSampleBuffer --> <div>
<h3>Type Changed: CoreMedia.CMSampleBuffer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICMAttachmentBearer</span>
</pre>
</div>

</div> <!-- end type CMSampleBuffer -->
<div> <!-- start type CMAttachmentBearer -->
<h3>New Type CoreMedia.CMAttachmentBearer</h3>
<pre class='added' data-is-non-breaking="">
public static class CMAttachmentBearer {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static T GetAttachment&lt;T&gt; (ICMAttachmentBearer target, string key, out CMAttachmentMode attachmentModeOut);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary GetAttachments (ICMAttachmentBearer target, CMAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PropagateAttachments (ICMAttachmentBearer source, ICMAttachmentBearer destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAllAttachments (ICMAttachmentBearer target);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAttachment (ICMAttachmentBearer target, string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAttachment (ICMAttachmentBearer target, string key, ObjCRuntime.INativeObject value, CMAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAttachments (ICMAttachmentBearer target, Foundation.NSDictionary theAttachments, CMAttachmentMode attachmentMode);</span>
}
</pre>
</div> <!-- end type CMAttachmentBearer -->
<div> <!-- start type CMAttachmentMode -->
<h3>New Type CoreMedia.CMAttachmentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CMAttachmentMode {
	<span class='added added-field ' data-is-non-breaking="">ShouldNotPropagate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ShouldPropagate = 1,</span>
}
</pre>
</div> <!-- end type CMAttachmentMode -->
<div> <!-- start type ICMAttachmentBearer -->
<h3>New Type CoreMedia.ICMAttachmentBearer</h3>
<pre class='added' data-is-non-breaking="">
public interface ICMAttachmentBearer : ObjCRuntime.INativeObject {
}
</pre>
</div> <!-- end type ICMAttachmentBearer -->

</div> <!-- end namespace CoreMedia -->
<!-- start namespace CoreMidi --> <div> 
<h2>Namespace CoreMidi</h2>
<div> <!-- start type MidiControlTransform -->
<h3>New Type CoreMidi.MidiControlTransform</h3>
<pre class='added' data-is-non-breaking="">
public struct MidiControlTransform {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MidiControlTransform (MidiTransformControlType controlType, MidiTransformControlType remappedControlType, ushort controlNumber, MidiTransformType transform, short param);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ushort ControlNumber;</span>
	<span class='added added-field ' data-is-non-breaking="">public MidiTransformControlType ControlType;</span>
	<span class='added added-field ' data-is-non-breaking="">public short Param;</span>
	<span class='added added-field ' data-is-non-breaking="">public MidiTransformControlType RemappedControlType;</span>
	<span class='added added-field ' data-is-non-breaking="">public MidiTransformType Transform;</span>
}
</pre>
</div> <!-- end type MidiControlTransform -->
<div> <!-- start type MidiThruConnection -->
<h3>New Type CoreMidi.MidiThruConnection</h3>
<pre class='added' data-is-non-breaking="">
public class MidiThruConnection : System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MidiThruConnection (uint handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public uint Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MidiThruConnection Create (string persistentOwnerID, MidiThruConnectionParams connectionParams);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MidiThruConnection Create (string persistentOwnerID, MidiThruConnectionParams connectionParams, out MidiError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MidiThruConnection[] Find (string persistentOwnerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MidiThruConnection[] Find (string persistentOwnerID, out MidiError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public MidiThruConnectionParams GetParams ();</span>
	<span class='added added-method ' data-is-non-breaking="">public MidiThruConnectionParams GetParams (out MidiError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public MidiError SetParams (MidiThruConnectionParams connectionParams);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~MidiThruConnection ();</span>
}
</pre>
</div> <!-- end type MidiThruConnection -->
<div> <!-- start type MidiThruConnectionEndpoint -->
<h3>New Type CoreMidi.MidiThruConnectionEndpoint</h3>
<pre class='added' data-is-non-breaking="">
public struct MidiThruConnectionEndpoint {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MidiThruConnectionEndpoint (int endpointRef, int uniqueID);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public int EndpointRef;</span>
	<span class='added added-field ' data-is-non-breaking="">public int UniqueID;</span>
}
</pre>
</div> <!-- end type MidiThruConnectionEndpoint -->
<div> <!-- start type MidiThruConnectionParams -->
<h3>New Type CoreMidi.MidiThruConnectionParams</h3>
<pre class='added' data-is-non-breaking="">
public class MidiThruConnectionParams {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MidiThruConnectionParams ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public byte[] ChannelMap { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform ChannelPressure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiControlTransform[] Controls { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiThruConnectionEndpoint[] Destinations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutAllControls { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutBeatClock { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutMtc { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutSysEx { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FilterOutTuneRequest { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte HighNote { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte HighVelocity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform KeyPressure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte LowNote { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte LowVelocity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiValueMap[] Maps { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform NoteNumber { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform PitchBend { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform ProgramChange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiThruConnectionEndpoint[] Sources { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MidiTransform Velocity { get; set; }</span>
}
</pre>
</div> <!-- end type MidiThruConnectionParams -->
<div> <!-- start type MidiTransform -->
<h3>New Type CoreMidi.MidiTransform</h3>
<pre class='added' data-is-non-breaking="">
public struct MidiTransform {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MidiTransform (MidiTransformType transform, short param);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public short Param;</span>
	<span class='added added-field ' data-is-non-breaking="">public MidiTransformType Transform;</span>
}
</pre>
</div> <!-- end type MidiTransform -->
<div> <!-- start type MidiTransformControlType -->
<h3>New Type CoreMidi.MidiTransformControlType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MidiTransformControlType {
	<span class='added added-field ' data-is-non-breaking="">FourteenBit = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FourteenBitNRpn = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FourteenBitRpn = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SevenBit = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SevenBitNRpn = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">SevenBitRpn = 2,</span>
}
</pre>
</div> <!-- end type MidiTransformControlType -->
<div> <!-- start type MidiTransformType -->
<h3>New Type CoreMidi.MidiTransformType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MidiTransformType {
	<span class='added added-field ' data-is-non-breaking="">Add = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">FilterOut = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">MapControl = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MapValue = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">MaxValue = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">MinValue = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Scale = 9,</span>
}
</pre>
</div> <!-- end type MidiTransformType -->
<div> <!-- start type MidiValueMap -->
<h3>New Type CoreMidi.MidiValueMap</h3>
<pre class='added' data-is-non-breaking="">
public struct MidiValueMap {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public byte[] Value { get; set; }</span>
}
</pre>
</div> <!-- end type MidiValueMap -->

</div> <!-- end namespace CoreMidi -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSExpression --> <div>
<h3>Type Changed: Foundation.NSExpression</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSExpressionCallbackHandler Block { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("ValueWithObject is deprecated, please use EvaluateWith instead.")]
	public NSExpression ExpressionValueWithObject (NSObject object1, NSMutableDictionary context);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFormat (string, NSExpression[]) is deprecated, please use FromFormat (string, NSObject[]) instead.")]
	public NSExpression FromFormat (string format, NSExpression[] parameters);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFunction (NSExpressionHandler, NSExpression[]) is deprecated, please use FromFunction (NSExpressionCallbackHandler, NSExpression[]) instead.")]
	public NSExpression FromFunction (NSExpressionHandler target, NSExpression[] parameters);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> NSExpression ExpressionValueWithObject (NSObject object1, NSMutableDictionary context)
</div><div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>static</span> public NSExpression FromFormat (string format, NSExpression[] parameters)
</div><div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>static</span> public NSExpression FromFunction (NSExpressionHandler target, NSExpression[] parameters)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject EvaluateWith (NSObject obj, NSMutableDictionary context);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFormat (string expressionFormat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFormat (string format, NSObject[] parameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFunction (NSExpressionCallbackHandler target, NSExpression[] parameters);</span>
</pre>
</div>

</div> <!-- end type NSExpression -->
<!-- start type NSObject --> <div>
<h3>Type Changed: Foundation.NSObject</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use PlatformAssembly for easier code sharing across platforms")]
	public static System.Reflection.Assembly MonoTouchAssembly;</span>
</div></pre>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static System.Reflection.Assembly PlatformAssembly;</span>
</pre>
</div>

</div> <!-- end type NSObject -->
<!-- start type NSUrl --> <div>
<h3>Type Changed: Foundation.NSUrl</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NSUrl x, NSUrl y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NSUrl x, NSUrl y);</span>
</pre>
</div>

</div> <!-- end type NSUrl -->
<div> <!-- start type NSExpressionCallbackHandler -->
<h3>New Type Foundation.NSExpressionCallbackHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSExpressionCallbackHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionCallbackHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSObject evaluatedObject, NSExpression[] expressions, NSMutableDictionary context, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Invoke (NSObject evaluatedObject, NSExpression[] expressions, NSMutableDictionary context);</span>
}
</pre>
</div> <!-- end type NSExpressionCallbackHandler -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKLocalPlayerListener --> <div>
<h3>Type Changed: GameKit.GKLocalPlayerListener</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use DidRequestMatch(GKPlayer player, GKPlayer[] recipientPlayers) instead")]
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);</span>
</div></pre>

</div> <!-- end type GKLocalPlayerListener -->

</div> <!-- end namespace GameKit -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKCoordinateRegion --> <div>
<h3>Type Changed: MapKit.MKCoordinateRegion</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type MKCoordinateRegion -->
<!-- start type MKCoordinateSpan --> <div>
<h3>Type Changed: MapKit.MKCoordinateSpan</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type MKCoordinateSpan -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPMoviePlayerController --> <div>
<h3>Type Changed: MediaPlayer.MPMoviePlayerController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AirPlayVideoActive { get; }</span>
</pre>
</div>

</div> <!-- end type MPMoviePlayerController -->
<!-- start type MPMusicPlayerController --> <div>
<h3>Type Changed: MediaPlayer.MPMusicPlayerController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint IndexOfNowPlayingItem { get; }</span>
</pre>
</div>

</div> <!-- end type MPMusicPlayerController -->
<div> <!-- start type MPErrorCodeExtensions -->
<h3>New Type MediaPlayer.MPErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (MPErrorCode self);</span>
}
</pre>
</div> <!-- end type MPErrorCodeExtensions -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"9.8.0"</span> <span class='added '>"9.9.0"</span>;
</div></pre>

</div> <!-- end type Constants -->
<!-- start type Runtime --> <div>
<h3>Type Changed: ObjCRuntime.Runtime</h3>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event MarshalManagedExceptionHandler MarshalManagedException;</span>
	<span class='added added-event ' data-is-non-breaking="">public event MarshalObjectiveCExceptionHandler MarshalObjectiveCException;</span>
</pre>
</div>

</div> <!-- end type Runtime -->
<div> <!-- start type MarshalManagedExceptionEventArgs -->
<h3>New Type ObjCRuntime.MarshalManagedExceptionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class MarshalManagedExceptionEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalManagedExceptionEventArgs ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Exception Exception { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MarshalManagedExceptionMode ExceptionMode { get; set; }</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionEventArgs -->
<div> <!-- start type MarshalManagedExceptionHandler -->
<h3>New Type ObjCRuntime.MarshalManagedExceptionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MarshalManagedExceptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalManagedExceptionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, MarshalManagedExceptionEventArgs args, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, MarshalManagedExceptionEventArgs args);</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionHandler -->
<div> <!-- start type MarshalManagedExceptionMode -->
<h3>New Type ObjCRuntime.MarshalManagedExceptionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MarshalManagedExceptionMode {
	<span class='added added-field ' data-is-non-breaking="">Abort = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ThrowObjectiveCException = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UnwindNativeCode = 1,</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionMode -->
<div> <!-- start type MarshalObjectiveCExceptionEventArgs -->
<h3>New Type ObjCRuntime.MarshalObjectiveCExceptionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class MarshalObjectiveCExceptionEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalObjectiveCExceptionEventArgs ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSException Exception { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MarshalObjectiveCExceptionMode ExceptionMode { get; set; }</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionEventArgs -->
<div> <!-- start type MarshalObjectiveCExceptionHandler -->
<h3>New Type ObjCRuntime.MarshalObjectiveCExceptionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MarshalObjectiveCExceptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalObjectiveCExceptionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, MarshalObjectiveCExceptionEventArgs args, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, MarshalObjectiveCExceptionEventArgs args);</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionHandler -->
<div> <!-- start type MarshalObjectiveCExceptionMode -->
<h3>New Type ObjCRuntime.MarshalObjectiveCExceptionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MarshalObjectiveCExceptionMode {
	<span class='added added-field ' data-is-non-breaking="">Abort = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ThrowManagedException = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UnwindManagedCode = 1,</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionMode -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<div> <!-- start type SecSharedCredential -->
<h3>New Type Security.SecSharedCredential</h3>
<pre class='added' data-is-non-breaking="">
public static class SecSharedCredential {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SharedPassword { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AddSharedWebCredential (string domainName, string account, string password, System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string CreateSharedWebCredentialPassword ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestSharedWebCredential (string domainName, string account, System.Action&lt;System.String[],Foundation.NSError&gt; handler);</span>
}
</pre>
</div> <!-- end type SecSharedCredential -->

</div> <!-- end namespace Security -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKVideoNode --> <div>
<h3>Type Changed: SpriteKit.SKVideoNode</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public SKVideoNode FromUrl (Foundation.NSUrl <span class='removed removed-inline '>videoURL</span> <span class='added '>videoUrl</span>)
</div></pre>

</div> <!-- end type SKVideoNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type UIMenuController --> <div>
<h3>Type Changed: UIKit.UIMenuController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MenuFrameDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type UIMenuController.Notifications --> <div>
<h3>Type Changed: UIKit.UIMenuController.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMenuFrameDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIMenuController.Notifications -->

</div> <!-- end type UIMenuController -->
<!-- start type UIPopoverPresentationController --> <div>
<h3>Type Changed: UIKit.UIPopoverPresentationController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public ShouldDismiss ShouldDismissPopover { get; set; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidDismiss;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler PrepareForPresentation;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;UIPopoverPresentationControllerRepositionEventArgs&gt; WillReposition;</span>
</pre>
</div>

</div> <!-- end type UIPopoverPresentationController -->
<!-- start type UIUserNotificationAction --> <div>
<h3>Type Changed: UIKit.UIUserNotificationAction</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResponseTypedTextKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextInputActionButtonTitleKey { get; }</span>
</pre>
</div>

</div> <!-- end type UIUserNotificationAction -->
<div> <!-- start type ShouldDismiss -->
<h3>New Type UIKit.ShouldDismiss</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ShouldDismiss : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ShouldDismiss (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UIPopoverPresentationController popoverPresentationController, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (UIPopoverPresentationController popoverPresentationController);</span>
}
</pre>
</div> <!-- end type ShouldDismiss -->
<div> <!-- start type UIPasteboardNames -->
<h3>New Type UIKit.UIPasteboardNames</h3>
<pre class='added' data-is-non-breaking="">
public static class UIPasteboardNames {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Find { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString General { get; }</span>
}
</pre>
</div> <!-- end type UIPasteboardNames -->
<div> <!-- start type UIPopoverPresentationControllerRepositionEventArgs -->
<h3>New Type UIKit.UIPopoverPresentationControllerRepositionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class UIPopoverPresentationControllerRepositionEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIPopoverPresentationControllerRepositionEventArgs (CoreGraphics.CGRect targetRect, UIView inView);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public UIView InView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGRect TargetRect { get; set; }</span>
}
</pre>
</div> <!-- end type UIPopoverPresentationControllerRepositionEventArgs -->

</div> <!-- end namespace UIKit -->
</div>



   


 <hr>
