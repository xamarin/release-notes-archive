---
id: D5F076DB-262E-47BE-BF1C-46BD9F82A30A
title: "Mac 3.4 to 3.99.1"
---

# API diff

 [(Mobile profile) mscorlib.dll](#diff/xm/Xamarin.Mac/mscorlib.html)

   


 [(Mobile profile) System.dll](#diff/xm/Xamarin.Mac/System.html)

   


 [(Mobile profile) System.Core.dll](#diff/xm/Xamarin.Mac/System.Core.html)

   


 [(Mobile profile) System.Data.dll](#diff/xm/Xamarin.Mac/System.Data.html)

   


 [(Mobile profile) System.ServiceModel.dll](#diff/xm/Xamarin.Mac/System.ServiceModel.html)

   


 [(Mobile profile) System.ServiceModel.Web.dll](#diff/xm/Xamarin.Mac/System.ServiceModel.Web.html)

   


 [(Mobile profile) System.Web.Services.dll](#diff/xm/Xamarin.Mac/System.Web.Services.html)

   


 [(Mobile profile) System.Transactions.dll](#diff/xm/Xamarin.Mac/System.Transactions.html)

   


 [(Classic profile) XamMac.dll](#diff/xm/XamMac.html)

   


 [(Mobile profile) Xamarin.Mac.dll](#diff/xm/Xamarin.Mac/Xamarin.Mac.html)

   


 [(Full profile) Xamarin.Mac.dll](#diff/xm/4.5/Xamarin.Mac.html)

   


   


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
</script><h1 id='diff/xm/Xamarin.Mac/mscorlib.html'>mscorlib.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Microsoft.Win32 --> <div> 
<h2>Namespace Microsoft.Win32</h2>
<!-- start type RegistryKey --> <div>
<h3>Type Changed: Microsoft.Win32.RegistryKey</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey, RegistryKeyPermissionCheck permissionCheck);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey, RegistryKeyPermissionCheck permissionCheck, RegistryOptions registryOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey, RegistryKeyPermissionCheck permissionCheck, System.Security.AccessControl.RegistrySecurity registrySecurity);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey, RegistryKeyPermissionCheck permissionCheck, RegistryOptions registryOptions, System.Security.AccessControl.RegistrySecurity registrySecurity);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Security.AccessControl.RegistrySecurity GetAccessControl ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Security.AccessControl.RegistrySecurity GetAccessControl (System.Security.AccessControl.AccessControlSections includeSections);</span>
	<span class='added added-method ' data-is-non-breaking="">public static RegistryKey OpenRemoteBaseKey (RegistryHive hKey, string machineName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static RegistryKey OpenRemoteBaseKey (RegistryHive hKey, string machineName, RegistryView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey OpenSubKey (string name, RegistryKeyPermissionCheck permissionCheck);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey OpenSubKey (string name, RegistryKeyPermissionCheck permissionCheck, System.Security.AccessControl.RegistryRights rights);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAccessControl (System.Security.AccessControl.RegistrySecurity registrySecurity);</span>
</pre>
</div>

</div> <!-- end type RegistryKey -->
<div> <!-- start type RegistryKeyPermissionCheck -->
<h3>New Type Microsoft.Win32.RegistryKeyPermissionCheck</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RegistryKeyPermissionCheck {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadSubTree = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadWriteSubTree = 2,</span>
}
</pre>
</div> <!-- end type RegistryKeyPermissionCheck -->

</div> <!-- end namespace Microsoft.Win32 -->
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type Array --> <div>
<h3>Type Changed: System.Array</h3>
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> bool IsReadOnly { get; }
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void Fill&lt;T&gt; (T[] array, T value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Fill&lt;T&gt; (T[] array, T value, int startIndex, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Reverse&lt;T&gt; (T[] array);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Reverse&lt;T&gt; (T[] array, int index, int length);</span>
</pre>
</div>

</div> <!-- end type Array -->
<!-- start type Type --> <div>
<h3>Type Changed: System.Type</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsSZArray { get; }</span>
</pre>
</div>

</div> <!-- end type Type -->

</div> <!-- end namespace System -->
<!-- start namespace System.Collections.Concurrent --> <div> 
<h2>Namespace System.Collections.Concurrent</h2>
<!-- start type ConcurrentDictionary`2 --> <div>
<h3>Type Changed: System.Collections.Concurrent.ConcurrentDictionary`2</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public TValue AddOrUpdate&lt;TArg&gt; (TKey key, System.Func&lt;TKey,TArg,TValue&gt; addValueFactory, System.Func&lt;TKey,TValue,TArg,TValue&gt; updateValueFactory, TArg factoryArgument);</span>
	<span class='added added-method ' data-is-non-breaking="">public TValue GetOrAdd&lt;TArg&gt; (TKey key, System.Func&lt;TKey,TArg,TValue&gt; valueFactory, TArg factoryArgument);</span>
</pre>
</div>

</div> <!-- end type ConcurrentDictionary`2 -->
<!-- start type ConcurrentQueue`1 --> <div>
<h3>Type Changed: System.Collections.Concurrent.ConcurrentQueue`1</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Clear ();</span>
</pre>
</div>

</div> <!-- end type ConcurrentQueue`1 -->

</div> <!-- end namespace System.Collections.Concurrent -->
<!-- start namespace System.Collections.Generic --> <div> 
<h2>Namespace System.Collections.Generic</h2>
<!-- start type Dictionary`2 --> <div>
<h3>Type Changed: System.Collections.Generic.Dictionary`2</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public Dictionary`2 (System.Collections.Generic.IEnumerable&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt; collection);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Dictionary`2 (System.Collections.Generic.IEnumerable&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt; collection, System.Collections.Generic.IEqualityComparer&lt;TKey&gt; comparer);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public TValue GetValueOrDefault (TKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public TValue GetValueOrDefault (TKey key, TValue defaultValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool TryAdd (TKey key, TValue value);</span>
</pre>
</div>

</div> <!-- end type Dictionary`2 -->

</div> <!-- end namespace System.Collections.Generic -->
<!-- start namespace System.Reflection --> <div> 
<h2>Namespace System.Reflection</h2>
<!-- start type TypeDelegator --> <div>
<h3>Type Changed: System.Reflection.TypeDelegator</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override bool IsSZArray { get; }</span>
</pre>
</div>

</div> <!-- end type TypeDelegator -->

</div> <!-- end namespace System.Reflection -->
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<!-- start type RuntimeHelpers --> <div>
<h3>Type Changed: System.Runtime.CompilerServices.RuntimeHelpers</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsReferenceOrContainsReferences&lt;T&gt; ();</span>
</pre>
</div>

</div> <!-- end type RuntimeHelpers -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
<!-- start namespace System.Security.Cryptography.X509Certificates --> <div> 
<h2>Namespace System.Security.Cryptography.X509Certificates</h2>
<!-- start type X509KeyStorageFlags --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509KeyStorageFlags</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EphemeralKeySet = 32,</span>
</pre>
</div>

</div> <!-- end type X509KeyStorageFlags -->

</div> <!-- end namespace System.Security.Cryptography.X509Certificates -->
<!-- start namespace System.Security.Principal --> <div> 
<h2>Namespace System.Security.Principal</h2>
<!-- start type WellKnownSidType --> <div>
<h3>Type Changed: System.Security.Principal.WellKnownSidType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">WinAccountReadonlyControllersSid = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">WinApplicationPackageAuthoritySid = 83,</span>
	<span class='added added-field ' data-is-non-breaking="">WinBuiltinAnyPackageSid = 84,</span>
	<span class='added added-field ' data-is-non-breaking="">WinBuiltinCertSvcDComAccessGroup = 78,</span>
	<span class='added added-field ' data-is-non-breaking="">WinBuiltinCryptoOperatorsSid = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">WinBuiltinDCOMUsersSid = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">WinBuiltinEventLogReadersGroup = 76,</span>
	<span class='added added-field ' data-is-non-breaking="">WinBuiltinIUsersSid = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCacheablePrincipalsGroupSid = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityDocumentsLibrarySid = 91,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityEnterpriseAuthenticationSid = 93,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityInternetClientServerSid = 86,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityInternetClientSid = 85,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityMusicLibrarySid = 90,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityPicturesLibrarySid = 88,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityPrivateNetworkClientServerSid = 87,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityRemovableStorageSid = 94,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilitySharedUserCertificatesSid = 92,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCapabilityVideosLibrarySid = 89,</span>
	<span class='added added-field ' data-is-non-breaking="">WinConsoleLogonSid = 81,</span>
	<span class='added added-field ' data-is-non-breaking="">WinCreatorOwnerRightsSid = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">WinEnterpriseReadonlyControllersSid = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">WinHighLabelSid = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">WinIUserSid = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">WinLocalLogonSid = 80,</span>
	<span class='added added-field ' data-is-non-breaking="">WinLowLabelSid = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">WinMediumLabelSid = 67,</span>
	<span class='added added-field ' data-is-non-breaking="">WinMediumPlusLabelSid = 79,</span>
	<span class='added added-field ' data-is-non-breaking="">WinNewEnterpriseReadonlyControllersSid = 77,</span>
	<span class='added added-field ' data-is-non-breaking="">WinNonCacheablePrincipalsGroupSid = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">WinSystemLabelSid = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">WinThisOrganizationCertificateSid = 82,</span>
	<span class='added added-field ' data-is-non-breaking="">WinUntrustedLabelSid = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">WinWriteRestrictedCodeSid = 70,</span>
</pre>
</div>

</div> <!-- end type WellKnownSidType -->

</div> <!-- end namespace System.Security.Principal -->
<!-- start namespace System.Threading --> <div> 
<h2>Namespace System.Threading</h2>
<div> <!-- start type PreAllocatedOverlapped -->
<h3>New Type System.Threading.PreAllocatedOverlapped</h3>
<pre class='added' data-is-non-breaking="">
public sealed class PreAllocatedOverlapped : System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PreAllocatedOverlapped (IOCompletionCallback callback, object state, object pinData);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
}
</pre>
</div> <!-- end type PreAllocatedOverlapped -->
<div> <!-- start type ThreadPoolBoundHandle -->
<h3>New Type System.Threading.ThreadPoolBoundHandle</h3>
<pre class='added' data-is-non-breaking="">
public sealed class ThreadPoolBoundHandle : System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Runtime.InteropServices.SafeHandle Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public NativeOverlapped* AllocateNativeOverlapped (PreAllocatedOverlapped preAllocated);</span>
	<span class='added added-method ' data-is-non-breaking="">public NativeOverlapped* AllocateNativeOverlapped (IOCompletionCallback callback, object state, object pinData);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ThreadPoolBoundHandle BindHandle (System.Runtime.InteropServices.SafeHandle handle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void FreeNativeOverlapped (NativeOverlapped* overlapped);</span>
	<span class='added added-method ' data-is-non-breaking="">public static object GetNativeOverlappedState (NativeOverlapped* overlapped);</span>
}
</pre>
</div> <!-- end type ThreadPoolBoundHandle -->

</div> <!-- end namespace System.Threading -->
<!-- start namespace System.Runtime.Loader --> <div>
<h2>Removed Namespace System.Runtime.Loader</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">System.Runtime.Loader.AssemblyLoadContext</span></h3></div> <!-- end namespace System.Runtime.Loader -->

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
</script><h1 id='diff/xm/Xamarin.Mac/System.html'>System.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Collections.Concurrent --> <div> 
<h2>Namespace System.Collections.Concurrent</h2>
<!-- start type ConcurrentBag`1 --> <div>
<h3>Type Changed: System.Collections.Concurrent.ConcurrentBag`1</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Clear ();</span>
</pre>
</div>

</div> <!-- end type ConcurrentBag`1 -->

</div> <!-- end namespace System.Collections.Concurrent -->
<!-- start namespace System.Collections.Generic --> <div> 
<h2>Namespace System.Collections.Generic</h2>
<!-- start type Queue`1 --> <div>
<h3>Type Changed: System.Collections.Generic.Queue`1</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool TryDequeue (T result);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool TryPeek (T result);</span>
</pre>
</div>

</div> <!-- end type Queue`1 -->
<!-- start type SortedSet`1 --> <div>
<h3>Type Changed: System.Collections.Generic.SortedSet`1</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool TryGetValue (T equalValue, T actualValue);</span>
</pre>
</div>

</div> <!-- end type SortedSet`1 -->
<!-- start type Stack`1 --> <div>
<h3>Type Changed: System.Collections.Generic.Stack`1</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool TryPeek (T result);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool TryPop (T result);</span>
</pre>
</div>

</div> <!-- end type Stack`1 -->

</div> <!-- end namespace System.Collections.Generic -->
<!-- start namespace System.IO.Compression --> <div> 
<h2>Namespace System.IO.Compression</h2>
<!-- start type DeflateStream --> <div>
<h3>Type Changed: System.IO.Compression.DeflateStream</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public override System.IAsyncResult BeginRead (byte[] <span class='removed removed-inline removed-breaking-inline'>buffer</span> <span class='added '>array</span>, int offset, int count, System.AsyncCallback <span class='removed removed-inline removed-breaking-inline'>cback</span> <span class='added '>asyncCallback</span>, object <span class='removed removed-inline removed-breaking-inline'>state</span> <span class='added '>asyncState</span>)
</div><div data-is-breaking="">	public override System.IAsyncResult BeginWrite (byte[] <span class='removed removed-inline removed-breaking-inline'>buffer</span> <span class='added '>array</span>, int offset, int count, System.AsyncCallback <span class='removed removed-inline removed-breaking-inline'>cback</span> <span class='added '>asyncCallback</span>, object <span class='removed removed-inline removed-breaking-inline'>state</span> <span class='added '>asyncState</span>)
</div><div data-is-breaking="">	public override int EndRead (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>async_result</span> <span class='added '>asyncResult</span>)
</div><div data-is-breaking="">	public override void EndWrite (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>async_result</span> <span class='added '>asyncResult</span>)
</div></pre>

</div> <!-- end type DeflateStream -->

</div> <!-- end namespace System.IO.Compression -->
<!-- start namespace System.Net --> <div> 
<h2>Namespace System.Net</h2>
<!-- start type HttpWebRequest --> <div>
<h3>Type Changed: System.Net.HttpWebRequest</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public System.IO.Stream EndGetRequestStream (System.IAsyncResult asyncResult, out TransportContext <span class='removed removed-inline removed-breaking-inline'>transportContext</span> <span class='added '>context</span>)
</div></pre>

</div> <!-- end type HttpWebRequest -->

</div> <!-- end namespace System.Net -->
<!-- start namespace System.Net.Mail --> <div> 
<h2>Namespace System.Net.Mail</h2>
<!-- start type AlternateView --> <div>
<h3>Type Changed: System.Net.Mail.AlternateView</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public AlternateView CreateAlternateViewFromString (string content, System.Text.Encoding <span class='removed removed-inline removed-breaking-inline'>encoding</span> <span class='added '>contentEncoding</span>, string mediaType)
</div></pre>

</div> <!-- end type AlternateView -->
<!-- start type MailAddress --> <div>
<h3>Type Changed: System.Net.Mail.MailAddress</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public override bool Equals (object <span class='removed removed-inline removed-breaking-inline'>obj</span> <span class='added '>value</span>)
</div></pre>

</div> <!-- end type MailAddress -->
<!-- start type SmtpClient --> <div>
<h3>Type Changed: System.Net.Mail.SmtpClient</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public void Send (string from, string <span class='removed removed-inline removed-breaking-inline'>to</span> <span class='added '>recipients</span>, string subject, string body)
</div><div data-is-breaking="">	public void SendAsync (string from, string <span class='removed removed-inline removed-breaking-inline'>to</span> <span class='added '>recipients</span>, string subject, string body, object userToken)
</div></pre>

</div> <!-- end type SmtpClient -->
<!-- start type SmtpException --> <div>
<h3>Type Changed: System.Net.Mail.SmtpException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	protected SmtpException (System.Runtime.Serialization.SerializationInfo <span class='removed removed-inline removed-breaking-inline'>info</span> <span class='added '>serializationInfo</span>, System.Runtime.Serialization.StreamingContext <span class='removed removed-inline removed-breaking-inline'>context</span> <span class='added '>streamingContext</span>)
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public override void GetObjectData (System.Runtime.Serialization.SerializationInfo <span class='removed removed-inline removed-breaking-inline'>info</span> <span class='added '>serializationInfo</span>, System.Runtime.Serialization.StreamingContext <span class='removed removed-inline removed-breaking-inline'>context</span> <span class='added '>streamingContext</span>)
</div></pre>

</div> <!-- end type SmtpException -->
<!-- start type SmtpFailedRecipientException --> <div>
<h3>Type Changed: System.Net.Mail.SmtpFailedRecipientException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	protected SmtpFailedRecipientException (System.Runtime.Serialization.SerializationInfo <span class='removed removed-inline removed-breaking-inline'>serializationInfo</span> <span class='added '>info</span>, System.Runtime.Serialization.StreamingContext <span class='removed removed-inline removed-breaking-inline'>streamingContext</span> <span class='added '>context</span>)
</div></pre>

</div> <!-- end type SmtpFailedRecipientException -->
<!-- start type SmtpFailedRecipientsException --> <div>
<h3>Type Changed: System.Net.Mail.SmtpFailedRecipientsException</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public override void GetObjectData (System.Runtime.Serialization.SerializationInfo <span class='removed removed-inline removed-breaking-inline'>info</span> <span class='added '>serializationInfo</span>, System.Runtime.Serialization.StreamingContext <span class='removed removed-inline removed-breaking-inline'>context</span> <span class='added '>streamingContext</span>)
</div></pre>

</div> <!-- end type SmtpFailedRecipientsException -->

</div> <!-- end namespace System.Net.Mail -->
<!-- start namespace System.Net.Sockets --> <div> 
<h2>Namespace System.Net.Sockets</h2>
<!-- start type Socket --> <div>
<h3>Type Changed: System.Net.Sockets.Socket</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public System.IAsyncResult BeginConnect (System.Net.EndPoint <span class='removed removed-inline removed-breaking-inline'>end_point</span> <span class='added '>remoteEP</span>, System.AsyncCallback callback, object state)
</div><div data-is-breaking="">	public System.IAsyncResult BeginConnect (System.Net.IPAddress[] addresses, int port, System.AsyncCallback <span class='removed removed-inline removed-breaking-inline'>callback</span> <span class='added '>requestCallback</span>, object state)
</div><div data-is-breaking="">	public System.IAsyncResult BeginConnect (string host, int port, System.AsyncCallback <span class='removed removed-inline removed-breaking-inline'>callback</span> <span class='added '>requestCallback</span>, object state)
</div><div data-is-breaking="">	public System.IAsyncResult BeginReceiveFrom (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline removed-breaking-inline'>socket_flags</span> <span class='added '>socketFlags</span>, ref System.Net.EndPoint <span class='removed removed-inline removed-breaking-inline'>remote_end</span> <span class='added '>remoteEP</span>, System.AsyncCallback callback, object state)
</div><div data-is-breaking="">	public System.IAsyncResult BeginSendTo (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline removed-breaking-inline'>socket_flags</span> <span class='added '>socketFlags</span>, System.Net.EndPoint <span class='removed removed-inline removed-breaking-inline'>remote_end</span> <span class='added '>remoteEP</span>, System.AsyncCallback callback, object state)
</div><div data-is-breaking="">	public Socket EndAccept (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>result</span> <span class='added '>asyncResult</span>)
</div><div data-is-breaking="">	public void EndConnect (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>result</span> <span class='added '>asyncResult</span>)
</div><div data-is-breaking="">	public int EndReceiveFrom (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>result</span> <span class='added '>asyncResult</span>, ref System.Net.EndPoint <span class='removed removed-inline removed-breaking-inline'>end_point</span> <span class='added '>endPoint</span>)
</div><div data-is-breaking="">	public int EndSendTo (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>result</span> <span class='added '>asyncResult</span>)
</div></pre>

</div> <!-- end type Socket -->

</div> <!-- end namespace System.Net.Sockets -->
<!-- start namespace System.Net.WebSockets --> <div> 
<h2>Namespace System.Net.WebSockets</h2>
<!-- start type ClientWebSocketOptions --> <div>
<h3>Type Changed: System.Net.WebSockets.ClientWebSocketOptions</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public ClientWebSocketOptions ();</span>
</pre>

</div> <!-- end type ClientWebSocketOptions -->
<!-- start type HttpListenerWebSocketContext --> <div>
<h3>Type Changed: System.Net.WebSockets.HttpListenerWebSocketContext</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public HttpListenerWebSocketContext ();</span>
</pre>

</div> <!-- end type HttpListenerWebSocketContext -->
<!-- start type WebSocketException --> <div>
<h3>Type Changed: System.Net.WebSockets.WebSocketException</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override int ErrorCode { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);</span>
</pre>
</div>

</div> <!-- end type WebSocketException -->

</div> <!-- end namespace System.Net.WebSockets -->
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
</script><h1 id='diff/xm/Xamarin.Mac/System.Core.html'>System.Core.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Collections.Generic --> <div> 
<h2>Namespace System.Collections.Generic</h2>
<!-- start type HashSet`1 --> <div>
<h3>Type Changed: System.Collections.Generic.HashSet`1</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public HashSet`1 (int capacity);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HashSet`1 (int capacity, System.Collections.Generic.IEqualityComparer&lt;T&gt; comparer);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool TryGetValue (T equalValue, T actualValue);</span>
</pre>
</div>

</div> <!-- end type HashSet`1 -->

</div> <!-- end namespace System.Collections.Generic -->
<!-- start namespace System.Linq --> <div> 
<h2>Namespace System.Linq</h2>
<!-- start type Queryable --> <div>
<h3>Type Changed: System.Linq.Queryable</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Linq.IQueryable&lt;TSource&gt; Append&lt;TSource&gt; (System.Linq.IQueryable&lt;TSource&gt; source, TSource element);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Linq.IQueryable&lt;TSource&gt; Prepend&lt;TSource&gt; (System.Linq.IQueryable&lt;TSource&gt; source, TSource element);</span>
</pre>
</div>

</div> <!-- end type Queryable -->

</div> <!-- end namespace System.Linq -->
<!-- start namespace System.Security.Cryptography.X509Certificates --> <div> 
<h2>Namespace System.Security.Cryptography.X509Certificates</h2>
<div> <!-- start type TrustStatus -->
<h3>New Type System.Security.Cryptography.X509Certificates.TrustStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TrustStatus {
	<span class='added added-field ' data-is-non-breaking="">KnownIdentity = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Trusted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownIdentity = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Untrusted = 0,</span>
}
</pre>
</div> <!-- end type TrustStatus -->

</div> <!-- end namespace System.Security.Cryptography.X509Certificates -->
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
</script><h1 id='diff/xm/Xamarin.Mac/System.Data.html'>System.Data.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Data.Common --> <div> 
<h2>Namespace System.Data.Common</h2>
<div> <!-- start type DbDataReaderExtensions -->
<h3>New Type System.Data.Common.DbDataReaderExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class DbDataReaderExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanGetColumnSchema (DbDataReader reader);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.ObjectModel.ReadOnlyCollection&lt;DbColumn&gt; GetColumnSchema (DbDataReader reader);</span>
}
</pre>
</div> <!-- end type DbDataReaderExtensions -->

</div> <!-- end namespace System.Data.Common -->
<!-- start namespace System.Data.SqlClient --> <div> 
<h2>Namespace System.Data.SqlClient</h2>
<!-- start type SqlBulkCopy --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlBulkCopy</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.DataRow[] rows);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.DataTable table);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.IDataReader reader);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.DataRow[] rows, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.DataTable table, System.Data.DataRowState rowState);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.DataTable table, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.IDataReader reader, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.DataTable table, System.Data.DataRowState rowState, System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type SqlBulkCopy -->
<!-- start type SqlConnection --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlConnection</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public SqlConnection (string connectionString, SqlCredential <span class='removed removed-inline removed-breaking-inline'>cred</span> <span class='added '>credential</span>)
</div></pre>

</div> <!-- end type SqlConnection -->
<!-- start type SqlCredential --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlCredential</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public SqlCredential (string <span class='removed removed-inline removed-breaking-inline'>user</span> <span class='added '>userId</span>, System.Security.SecureString password)
</div></pre>

</div> <!-- end type SqlCredential -->

</div> <!-- end namespace System.Data.SqlClient -->
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
</script><h1 id='diff/xm/Xamarin.Mac/System.ServiceModel.html'>System.ServiceModel.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Collections.Generic --> <div> 
<h2>Namespace System.Collections.Generic</h2>
<!-- start type KeyedByTypeCollection`1 --> <div>
<h3>Type Changed: System.Collections.Generic.KeyedByTypeCollection`1</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	protected override void InsertItem (int index, TItem <span class='removed removed-inline removed-breaking-inline'>kind</span> <span class='added '>item</span>)
</div><div data-is-breaking="">	protected override void SetItem (int index, TItem <span class='removed removed-inline removed-breaking-inline'>kind</span> <span class='added '>item</span>)
</div></pre>

</div> <!-- end type KeyedByTypeCollection`1 -->
<!-- start type SynchronizedKeyedCollection`2 --> <div>
<h3>Type Changed: System.Collections.Generic.SynchronizedKeyedCollection`2</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	protected SynchronizedKeyedCollection`2 (object syncRoot, System.Collections.Generic.IEqualityComparer&lt;K&gt; comparer, int <span class='removed removed-inline removed-breaking-inline'>capacity</span> <span class='added '>dictionaryCreationThreshold</span>)
</div></pre>

</div> <!-- end type SynchronizedKeyedCollection`2 -->
<!-- start type SynchronizedReadOnlyCollection`1 --> <div>
<h3>Type Changed: System.Collections.Generic.SynchronizedReadOnlyCollection`1</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public SynchronizedReadOnlyCollection`1 (object <span class='removed removed-inline removed-breaking-inline'>sync_root</span> <span class='added '>syncRoot</span>)
</div><div data-is-breaking="">	public SynchronizedReadOnlyCollection`1 (object <span class='removed removed-inline removed-breaking-inline'>sync_root</span> <span class='added '>syncRoot</span>, System.Collections.Generic.IEnumerable&lt;T&gt; list)
</div><div data-is-breaking="">	public SynchronizedReadOnlyCollection`1 (object <span class='removed removed-inline removed-breaking-inline'>sync_root</span> <span class='added '>syncRoot</span>, T[] list)
</div></pre>

</div> <!-- end type SynchronizedReadOnlyCollection`1 -->

</div> <!-- end namespace System.Collections.Generic -->
<!-- start namespace System.ServiceModel --> <div> 
<h2>Namespace System.ServiceModel</h2>
<!-- start type ChannelFactory --> <div>
<h3>Type Changed: System.ServiceModel.ChannelFactory</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	protected void InitializeEndpoint (string configurationName, EndpointAddress <span class='removed removed-inline removed-breaking-inline'>remoteAddress</span> <span class='added '>address</span>)
</div></pre>

</div> <!-- end type ChannelFactory -->
<!-- start type ChannelFactory`1 --> <div>
<h3>Type Changed: System.ServiceModel.ChannelFactory`1</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public TChannel CreateChannel (Channels.Binding binding, EndpointAddress <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>endpointAddress</span>)
</div><div data-is-breaking="">	public TChannel CreateChannel (Channels.Binding binding, EndpointAddress <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>endpointAddress</span>, System.Uri via)
</div></pre>

</div> <!-- end type ChannelFactory`1 -->
<!-- start type ClientBase`1 --> <div>
<h3>Type Changed: System.ServiceModel.ClientBase`1</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	protected ClientBase`1 (InstanceContext <span class='removed removed-inline removed-breaking-inline'>instance</span> <span class='added '>callbackInstance</span>)
</div><div data-is-breaking="">	protected ClientBase`1 (InstanceContext <span class='removed removed-inline removed-breaking-inline'>instance</span> <span class='added '>callbackInstance</span>, Description.ServiceEndpoint endpoint)
</div><div data-is-breaking="">	protected ClientBase`1 (InstanceContext <span class='removed removed-inline removed-breaking-inline'>instance</span> <span class='added '>callbackInstance</span>, string endpointConfigurationName)
</div><div data-is-breaking="">	protected ClientBase`1 (InstanceContext <span class='removed removed-inline removed-breaking-inline'>instance</span> <span class='added '>callbackInstance</span>, Channels.Binding binding, EndpointAddress remoteAddress)
</div><div data-is-breaking="">	protected ClientBase`1 (InstanceContext <span class='removed removed-inline removed-breaking-inline'>instance</span> <span class='added '>callbackInstance</span>, string endpointConfigurationName, EndpointAddress remoteAddress)
</div><div data-is-breaking="">	protected ClientBase`1 (InstanceContext <span class='removed removed-inline removed-breaking-inline'>instance</span> <span class='added '>callbackInstance</span>, string endpointConfigurationName, string remoteAddress)
</div></pre>

</div> <!-- end type ClientBase`1 -->
<!-- start type DuplexChannelFactory`1 --> <div>
<h3>Type Changed: System.ServiceModel.DuplexChannelFactory`1</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public DuplexChannelFactory`1 (object <span class='removed removed-inline removed-breaking-inline'>callbackInstance</span> <span class='added '>callbackObject</span>)
</div><div data-is-breaking="">	public DuplexChannelFactory`1 (object <span class='removed removed-inline removed-breaking-inline'>callbackInstance</span> <span class='added '>callbackObject</span>, Channels.Binding binding)
</div><div data-is-breaking="">	public DuplexChannelFactory`1 (object <span class='removed removed-inline removed-breaking-inline'>callbackInstance</span> <span class='added '>callbackObject</span>, Description.ServiceEndpoint endpoint)
</div><div data-is-breaking="">	public DuplexChannelFactory`1 (object <span class='removed removed-inline removed-breaking-inline'>callbackInstance</span> <span class='added '>callbackObject</span>, string endpointConfigurationName)
</div><div data-is-breaking="">	public DuplexChannelFactory`1 (object <span class='removed removed-inline removed-breaking-inline'>callbackInstance</span> <span class='added '>callbackObject</span>, Channels.Binding binding, EndpointAddress remoteAddress)
</div><div data-is-breaking="">	public DuplexChannelFactory`1 (object <span class='removed removed-inline removed-breaking-inline'>callbackInstance</span> <span class='added '>callbackObject</span>, Channels.Binding binding, string remoteAddress)
</div><div data-is-breaking="">	public DuplexChannelFactory`1 (object <span class='removed removed-inline removed-breaking-inline'>callbackInstance</span> <span class='added '>callbackObject</span>, string endpointConfigurationName, EndpointAddress remoteAddress)
</div></pre>

</div> <!-- end type DuplexChannelFactory`1 -->
<!-- start type DuplexClientBase`1 --> <div>
<h3>Type Changed: System.ServiceModel.DuplexClientBase`1</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	protected DuplexClientBase`1 (object callbackInstance, string <span class='removed removed-inline removed-breaking-inline'>bindingConfigurationName</span> <span class='added '>endpointConfigurationName</span>, EndpointAddress remoteAddress)
</div><div data-is-breaking="">	protected DuplexClientBase`1 (InstanceContext callbackInstance, string endpointConfigurationName, EndpointAddress <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>remoteAddress</span>)
</div></pre>

</div> <!-- end type DuplexClientBase`1 -->
<!-- start type EndpointAddress --> <div>
<h3>Type Changed: System.ServiceModel.EndpointAddress</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public void WriteTo (Channels.AddressingVersion addressingVersion, System.Xml.XmlDictionaryWriter writer, System.Xml.XmlDictionaryString <span class='removed removed-inline removed-breaking-inline'>localname</span> <span class='added '>localName</span>, System.Xml.XmlDictionaryString ns)
</div><div data-is-breaking="">	public void WriteTo (Channels.AddressingVersion addressingVersion, System.Xml.XmlWriter writer, string <span class='removed removed-inline removed-breaking-inline'>localname</span> <span class='added '>localName</span>, string ns)
</div></pre>

</div> <!-- end type EndpointAddress -->
<!-- start type FaultException --> <div>
<h3>Type Changed: System.ServiceModel.FaultException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public FaultException (string <span class='removed removed-inline removed-breaking-inline'>msg</span> <span class='added '>reason</span>)
</div><div data-is-breaking="">	public FaultException (string <span class='removed removed-inline removed-breaking-inline'>msg</span> <span class='added '>reason</span>, FaultCode code)
</div></pre>

</div> <!-- end type FaultException -->
<!-- start type InstanceContext --> <div>
<h3>Type Changed: System.ServiceModel.InstanceContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.ServiceModel.IExtensionCollection&lt;InstanceContext&gt; Extensions { get; }</span>
</pre>
</div>

</div> <!-- end type InstanceContext -->
<!-- start type OptionalReliableSession --> <div>
<h3>Type Changed: System.ServiceModel.OptionalReliableSession</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public OptionalReliableSession (Channels.ReliableSessionBindingElement <span class='removed removed-inline removed-breaking-inline'>binding</span> <span class='added '>reliableSessionBindingElement</span>)
</div></pre>

</div> <!-- end type OptionalReliableSession -->
<!-- start type ReliableSession --> <div>
<h3>Type Changed: System.ServiceModel.ReliableSession</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public ReliableSession (Channels.ReliableSessionBindingElement <span class='removed removed-inline removed-breaking-inline'>binding</span> <span class='added '>reliableSessionBindingElement</span>)
</div></pre>

</div> <!-- end type ReliableSession -->
<!-- start type UriSchemeKeyedCollection --> <div>
<h3>Type Changed: System.ServiceModel.UriSchemeKeyedCollection</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public UriSchemeKeyedCollection (System.Uri[] <span class='removed removed-inline removed-breaking-inline'>uris</span> <span class='added '>addresses</span>)
</div></pre>

</div> <!-- end type UriSchemeKeyedCollection -->

</div> <!-- end namespace System.ServiceModel -->
<!-- start namespace System.ServiceModel.Channels --> <div> 
<h2>Namespace System.ServiceModel.Channels</h2>
<!-- start type CustomBinding --> <div>
<h3>Type Changed: System.ServiceModel.Channels.CustomBinding</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public CustomBinding (string <span class='removed removed-inline removed-breaking-inline'>name</span> <span class='added '>configurationName</span>)
</div></pre>

</div> <!-- end type CustomBinding -->
<!-- start type Message --> <div>
<h3>Type Changed: System.ServiceModel.Channels.Message</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public Message CreateMessage (MessageVersion version, System.ServiceModel.FaultCode <span class='removed removed-inline removed-breaking-inline'>code</span> <span class='added '>faultCode</span>, string reason, string action)
</div><div data-is-breaking="">	public Message CreateMessage (MessageVersion version, System.ServiceModel.FaultCode <span class='removed removed-inline removed-breaking-inline'>code</span> <span class='added '>faultCode</span>, string reason, object detail, string action)
</div></pre>

</div> <!-- end type Message -->
<!-- start type MessageFault --> <div>
<h3>Type Changed: System.ServiceModel.Channels.MessageFault</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public MessageFault CreateFault (System.ServiceModel.FaultCode code, System.ServiceModel.FaultReason reason, object detail, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline removed-breaking-inline'>formatter</span> <span class='added '>serializer</span>)
</div><div data-is-breaking="">	public MessageFault CreateFault (System.ServiceModel.FaultCode code, System.ServiceModel.FaultReason reason, object detail, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline removed-breaking-inline'>formatter</span> <span class='added '>serializer</span>, string actor)
</div><div data-is-breaking="">	public MessageFault CreateFault (System.ServiceModel.FaultCode code, System.ServiceModel.FaultReason reason, object detail, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline removed-breaking-inline'>formatter</span> <span class='added '>serializer</span>, string actor, string node)
</div></pre>

</div> <!-- end type MessageFault -->
<!-- start type MessageHeaders --> <div>
<h3>Type Changed: System.ServiceModel.Channels.MessageHeaders</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public MessageHeaders (MessageHeaders <span class='removed removed-inline removed-breaking-inline'>headers</span> <span class='added '>collection</span>)
</div><div data-is-breaking="">	public MessageHeaders (MessageVersion version, int <span class='removed removed-inline removed-breaking-inline'>capacity</span> <span class='added '>initialSize</span>)
</div></pre>

</div> <!-- end type MessageHeaders -->
<!-- start type UnderstoodHeaders --> <div>
<h3>Type Changed: System.ServiceModel.Channels.UnderstoodHeaders</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public void Add (MessageHeaderInfo <span class='removed removed-inline removed-breaking-inline'>header</span> <span class='added '>headerInfo</span>)
</div><div data-is-breaking="">	public bool Contains (MessageHeaderInfo <span class='removed removed-inline removed-breaking-inline'>header</span> <span class='added '>headerInfo</span>)
</div><div data-is-breaking="">	public void Remove (MessageHeaderInfo <span class='removed removed-inline removed-breaking-inline'>header</span> <span class='added '>headerInfo</span>)
</div></pre>

</div> <!-- end type UnderstoodHeaders -->

</div> <!-- end namespace System.ServiceModel.Channels -->
<!-- start namespace System.ServiceModel.Description --> <div> 
<h2>Namespace System.ServiceModel.Description</h2>
<!-- start type FaultDescriptionCollection --> <div>
<h3>Type Changed: System.ServiceModel.Description.FaultDescriptionCollection</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public FaultDescription Find (string <span class='removed removed-inline removed-breaking-inline'>name</span> <span class='added '>action</span>)
</div><div data-is-breaking="">	public System.Collections.ObjectModel.Collection&lt;FaultDescription&gt; FindAll (string <span class='removed removed-inline removed-breaking-inline'>name</span> <span class='added '>action</span>)
</div></pre>

</div> <!-- end type FaultDescriptionCollection -->
<!-- start type XmlSerializerOperationBehavior --> <div>
<h3>Type Changed: System.ServiceModel.Description.XmlSerializerOperationBehavior</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public XmlSerializerOperationBehavior (OperationDescription operation, System.ServiceModel.XmlSerializerFormatAttribute <span class='removed removed-inline removed-breaking-inline'>format</span> <span class='added '>attribute</span>)
</div></pre>

</div> <!-- end type XmlSerializerOperationBehavior -->

</div> <!-- end namespace System.ServiceModel.Description -->
<!-- start namespace System.ServiceModel.Dispatcher --> <div> 
<h2>Namespace System.ServiceModel.Dispatcher</h2>
<!-- start type IDispatchMessageFormatter --> <div>
<h3>Type Changed: System.ServiceModel.Dispatcher.IDispatchMessageFormatter</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public abstract System.ServiceModel.Channels.Message SerializeReply (System.ServiceModel.Channels.MessageVersion <span class='removed removed-inline removed-breaking-inline'>version</span> <span class='added '>messageVersion</span>, object[] parameters, object result)
</div></pre>

</div> <!-- end type IDispatchMessageFormatter -->

</div> <!-- end namespace System.ServiceModel.Dispatcher -->
<!-- start namespace System.ServiceModel.Security --> <div> 
<h2>Namespace System.ServiceModel.Security</h2>
<!-- start type MessagePartSpecification --> <div>
<h3>Type Changed: System.ServiceModel.Security.MessagePartSpecification</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public void Union (MessagePartSpecification <span class='removed removed-inline removed-breaking-inline'>other</span> <span class='added '>specification</span>)
</div></pre>

</div> <!-- end type MessagePartSpecification -->
<div> <!-- start type SecurityNegotiationException -->
<h3>New Type System.ServiceModel.Security.SecurityNegotiationException</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public class SecurityNegotiationException : System.ServiceModel.CommunicationException, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SecurityNegotiationException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecurityNegotiationException (string message);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SecurityNegotiationException (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecurityNegotiationException (string message, System.Exception innerException);</span>
}
</pre>
</div> <!-- end type SecurityNegotiationException -->

</div> <!-- end namespace System.ServiceModel.Security -->
<!-- start namespace System.ServiceModel.Security.Tokens --> <div> 
<h2>Namespace System.ServiceModel.Security.Tokens</h2>
<!-- start type SecureConversationSecurityTokenParameters --> <div>
<h3>Type Changed: System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	protected SecureConversationSecurityTokenParameters (SecureConversationSecurityTokenParameters <span class='removed removed-inline removed-breaking-inline'>source</span> <span class='added '>other</span>)
</div></pre>

</div> <!-- end type SecureConversationSecurityTokenParameters -->
<!-- start type UserNameSecurityTokenParameters --> <div>
<h3>Type Changed: System.ServiceModel.Security.Tokens.UserNameSecurityTokenParameters</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	protected UserNameSecurityTokenParameters (UserNameSecurityTokenParameters <span class='removed removed-inline removed-breaking-inline'>source</span> <span class='added '>other</span>)
</div></pre>

</div> <!-- end type UserNameSecurityTokenParameters -->

</div> <!-- end namespace System.ServiceModel.Security.Tokens -->
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
</script><h1 id='diff/xm/Xamarin.Mac/System.ServiceModel.Web.html'>System.ServiceModel.Web.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type UriTemplateMatchException --> <div>
<h3>Type Changed: System.UriTemplateMatchException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public UriTemplateMatchException (string <span class='removed removed-inline removed-breaking-inline'>msg</span> <span class='added '>message</span>)
</div><div data-is-breaking="">	public UriTemplateMatchException (string <span class='removed removed-inline removed-breaking-inline'>msg</span> <span class='added '>message</span>, Exception <span class='removed removed-inline removed-breaking-inline'>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type UriTemplateMatchException -->

</div> <!-- end namespace System -->
<!-- start namespace System.ServiceModel --> <div> 
<h2>Namespace System.ServiceModel</h2>
<!-- start type WebHttpBinding --> <div>
<h3>Type Changed: System.ServiceModel.WebHttpBinding</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public WebHttpBinding (WebHttpSecurityMode <span class='removed removed-inline removed-breaking-inline'>mode</span> <span class='added '>securityMode</span>)
</div></pre>

</div> <!-- end type WebHttpBinding -->

</div> <!-- end namespace System.ServiceModel -->
<!-- start namespace System.ServiceModel.Web --> <div> 
<h2>Namespace System.ServiceModel.Web</h2>
<!-- start type WebChannelFactory`1 --> <div>
<h3>Type Changed: System.ServiceModel.Web.WebChannelFactory`1</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public WebChannelFactory`1 (string <span class='removed removed-inline removed-breaking-inline'>configurationName</span> <span class='added '>endpointConfigurationName</span>)
</div><div data-is-breaking="">	public WebChannelFactory`1 (System.Type <span class='removed removed-inline removed-breaking-inline'>serviceType</span> <span class='added '>channelType</span>)
</div></pre>

</div> <!-- end type WebChannelFactory`1 -->
<!-- start type WebOperationContext --> <div>
<h3>Type Changed: System.ServiceModel.Web.WebOperationContext</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public WebOperationContext (System.ServiceModel.OperationContext <span class='removed removed-inline removed-breaking-inline'>operation</span> <span class='added '>operationContext</span>)
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public void Attach (System.ServiceModel.OperationContext <span class='removed removed-inline removed-breaking-inline'>context</span> <span class='added '>owner</span>)
</div><div data-is-breaking="">	public void Detach (System.ServiceModel.OperationContext <span class='removed removed-inline removed-breaking-inline'>context</span> <span class='added '>owner</span>)
</div></pre>

</div> <!-- end type WebOperationContext -->

</div> <!-- end namespace System.ServiceModel.Web -->
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
</script><h1 id='diff/xm/Xamarin.Mac/System.Web.Services.html'>System.Web.Services.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Web --> <div> 
<h2>Namespace System.Web</h2>
<!-- start type HttpUtility --> <div>
<h3>Type Changed: System.Web.HttpUtility</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public string UrlDecode (string <span class='removed removed-inline removed-breaking-inline'>s</span> <span class='added '>str</span>, System.Text.Encoding e)
</div><div data-is-breaking="">	public string UrlEncode (string <span class='removed removed-inline removed-breaking-inline'>s</span> <span class='added '>str</span>, System.Text.Encoding <span class='removed removed-inline removed-breaking-inline'>Enc</span> <span class='added '>e</span>)
</div><div data-is-breaking="">	public string UrlPathEncode (string <span class='removed removed-inline removed-breaking-inline'>s</span> <span class='added '>str</span>)
</div></pre>

</div> <!-- end type HttpUtility -->

</div> <!-- end namespace System.Web -->
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
</script><h1 id='diff/xm/Xamarin.Mac/System.Transactions.html'>System.Transactions.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Transactions --> <div> 
<h2>Namespace System.Transactions</h2>
<!-- start type CommittableTransaction --> <div>
<h3>Type Changed: System.Transactions.CommittableTransaction</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public System.IAsyncResult BeginCommit (System.AsyncCallback <span class='removed removed-inline removed-breaking-inline'>callback</span> <span class='added '>asyncCallback</span>, object <span class='removed removed-inline removed-breaking-inline'>user_defined_state</span> <span class='added '>asyncState</span>)
</div><div data-is-breaking="">	public void EndCommit (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>ar</span> <span class='added '>asyncResult</span>)
</div></pre>

</div> <!-- end type CommittableTransaction -->
<!-- start type IDtcTransaction --> <div>
<h3>Type Changed: System.Transactions.IDtcTransaction</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public abstract void Abort (IntPtr <span class='removed removed-inline removed-breaking-inline'>manager</span> <span class='added '>reason</span>, int <span class='removed removed-inline removed-breaking-inline'>whatever</span> <span class='added '>retaining</span>, int <span class='removed removed-inline removed-breaking-inline'>whatever2</span> <span class='added '>async</span>)
</div><div data-is-breaking="">	public abstract void Commit (int <span class='removed removed-inline removed-breaking-inline'>whatever</span> <span class='added '>retaining</span>, int <span class='removed removed-inline removed-breaking-inline'>whatever2</span> <span class='added '>commitType</span>, int <span class='removed removed-inline removed-breaking-inline'>whatever3</span> <span class='added '>reserved</span>)
</div><div data-is-breaking="">	public abstract void GetTransactionInfo (IntPtr <span class='removed removed-inline removed-breaking-inline'>whatever</span> <span class='added '>transactionInformation</span>)
</div></pre>

</div> <!-- end type IDtcTransaction -->
<!-- start type IPromotableSinglePhaseNotification --> <div>
<h3>Type Changed: System.Transactions.IPromotableSinglePhaseNotification</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public abstract void Rollback (SinglePhaseEnlistment <span class='removed removed-inline removed-breaking-inline'>enlistment</span> <span class='added '>singlePhaseEnlistment</span>)
</div><div data-is-breaking="">	public abstract void SinglePhaseCommit (SinglePhaseEnlistment <span class='removed removed-inline removed-breaking-inline'>enlistment</span> <span class='added '>singlePhaseEnlistment</span>)
</div></pre>

</div> <!-- end type IPromotableSinglePhaseNotification -->
<!-- start type ISinglePhaseNotification --> <div>
<h3>Type Changed: System.Transactions.ISinglePhaseNotification</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public abstract void SinglePhaseCommit (SinglePhaseEnlistment <span class='removed removed-inline removed-breaking-inline'>enlistment</span> <span class='added '>singlePhaseEnlistment</span>)
</div></pre>

</div> <!-- end type ISinglePhaseNotification -->
<!-- start type PreparingEnlistment --> <div>
<h3>Type Changed: System.Transactions.PreparingEnlistment</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public void ForceRollback (System.Exception <span class='removed removed-inline removed-breaking-inline'>ex</span> <span class='added '>e</span>)
</div></pre>

</div> <!-- end type PreparingEnlistment -->
<!-- start type SubordinateTransaction --> <div>
<h3>Type Changed: System.Transactions.SubordinateTransaction</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public SubordinateTransaction (IsolationLevel <span class='removed removed-inline removed-breaking-inline'>level</span> <span class='added '>isoLevel</span>, ISimpleTransactionSuperior superior)
</div></pre>

</div> <!-- end type SubordinateTransaction -->
<!-- start type Transaction --> <div>
<h3>Type Changed: System.Transactions.Transaction</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public DependentTransaction DependentClone (DependentCloneOption <span class='removed removed-inline removed-breaking-inline'>option</span> <span class='added '>cloneOption</span>)
</div><div data-is-breaking="">	public Enlistment EnlistDurable (System.Guid <span class='removed removed-inline removed-breaking-inline'>manager</span> <span class='added '>resourceManagerIdentifier</span>, IEnlistmentNotification <span class='removed removed-inline removed-breaking-inline'>notification</span> <span class='added '>enlistmentNotification</span>, EnlistmentOptions <span class='removed removed-inline removed-breaking-inline'>options</span> <span class='added '>enlistmentOptions</span>)
</div><div data-is-breaking="">	public Enlistment EnlistDurable (System.Guid <span class='removed removed-inline removed-breaking-inline'>manager</span> <span class='added '>resourceManagerIdentifier</span>, ISinglePhaseNotification <span class='removed removed-inline removed-breaking-inline'>notification</span> <span class='added '>singlePhaseNotification</span>, EnlistmentOptions <span class='removed removed-inline removed-breaking-inline'>options</span> <span class='added '>enlistmentOptions</span>)
</div><div data-is-breaking="">	public bool EnlistPromotableSinglePhase (IPromotableSinglePhaseNotification <span class='removed removed-inline removed-breaking-inline'>notification</span> <span class='added '>promotableSinglePhaseNotification</span>)
</div><div data-is-breaking="">	public Enlistment EnlistVolatile (IEnlistmentNotification <span class='removed removed-inline removed-breaking-inline'>notification</span> <span class='added '>enlistmentNotification</span>, EnlistmentOptions <span class='removed removed-inline removed-breaking-inline'>options</span> <span class='added '>enlistmentOptions</span>)
</div><div data-is-breaking="">	public Enlistment EnlistVolatile (ISinglePhaseNotification <span class='removed removed-inline removed-breaking-inline'>notification</span> <span class='added '>singlePhaseNotification</span>, EnlistmentOptions <span class='removed removed-inline removed-breaking-inline'>options</span> <span class='added '>enlistmentOptions</span>)
</div><div data-is-breaking="">	public void Rollback (System.Exception <span class='removed removed-inline removed-breaking-inline'>ex</span> <span class='added '>e</span>)
</div></pre>

</div> <!-- end type Transaction -->
<!-- start type TransactionInterop --> <div>
<h3>Type Changed: System.Transactions.TransactionInterop</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public byte[] GetExportCookie (Transaction transaction, byte[] <span class='removed removed-inline removed-breaking-inline'>exportCookie</span> <span class='added '>whereabouts</span>)
</div><div data-is-breaking="">	public Transaction GetTransactionFromDtcTransaction (IDtcTransaction <span class='removed removed-inline removed-breaking-inline'>dtc</span> <span class='added '>transactionNative</span>)
</div><div data-is-breaking="">	public Transaction GetTransactionFromExportCookie (byte[] <span class='removed removed-inline removed-breaking-inline'>exportCookie</span> <span class='added '>cookie</span>)
</div><div data-is-breaking="">	public Transaction GetTransactionFromTransmitterPropagationToken (byte[] <span class='removed removed-inline removed-breaking-inline'>token</span> <span class='added '>propagationToken</span>)
</div></pre>

</div> <!-- end type TransactionInterop -->
<!-- start type TransactionManager --> <div>
<h3>Type Changed: System.Transactions.TransactionManager</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public void RecoveryComplete (System.Guid <span class='removed removed-inline removed-breaking-inline'>manager</span> <span class='added '>resourceManagerIdentifier</span>)
</div><div data-is-breaking="">	public Enlistment Reenlist (System.Guid <span class='removed removed-inline removed-breaking-inline'>manager</span> <span class='added '>resourceManagerIdentifier</span>, byte[] <span class='removed removed-inline removed-breaking-inline'>recoveryInfo</span> <span class='added '>recoveryInformation</span>, IEnlistmentNotification <span class='removed removed-inline removed-breaking-inline'>notification</span> <span class='added '>enlistmentNotification</span>)
</div></pre>

</div> <!-- end type TransactionManager -->
<!-- start type TransactionOptions --> <div>
<h3>Type Changed: System.Transactions.TransactionOptions</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public bool op_Equality (TransactionOptions <span class='removed removed-inline removed-breaking-inline'>o1</span> <span class='added '>x</span>, TransactionOptions <span class='removed removed-inline removed-breaking-inline'>o2</span> <span class='added '>y</span>)
</div><div data-is-breaking="">	public bool op_Inequality (TransactionOptions <span class='removed removed-inline removed-breaking-inline'>o1</span> <span class='added '>x</span>, TransactionOptions <span class='removed removed-inline removed-breaking-inline'>o2</span> <span class='added '>y</span>)
</div></pre>

</div> <!-- end type TransactionOptions -->
<!-- start type TransactionScope --> <div>
<h3>Type Changed: System.Transactions.TransactionScope</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public TransactionScope (Transaction <span class='removed removed-inline removed-breaking-inline'>transaction</span> <span class='added '>transactionToUse</span>)
</div><div data-is-breaking="">	public TransactionScope (TransactionScopeAsyncFlowOption <span class='removed removed-inline removed-breaking-inline'>asyncFlow</span> <span class='added '>asyncFlowOption</span>)
</div><div data-is-breaking="">	public TransactionScope (TransactionScopeOption <span class='removed removed-inline removed-breaking-inline'>option</span> <span class='added '>scopeOption</span>)
</div><div data-is-breaking="">	public TransactionScope (Transaction <span class='removed removed-inline removed-breaking-inline'>transaction</span> <span class='added '>transactionToUse</span>, System.TimeSpan <span class='removed removed-inline removed-breaking-inline'>timeout</span> <span class='added '>scopeTimeout</span>)
</div><div data-is-breaking="">	public TransactionScope (TransactionScopeOption <span class='removed removed-inline removed-breaking-inline'>option</span> <span class='added '>scopeOption</span>, System.TimeSpan <span class='removed removed-inline removed-breaking-inline'>timeout</span> <span class='added '>scopeTimeout</span>)
</div><div data-is-breaking="">	public TransactionScope (TransactionScopeOption scopeOption, TransactionOptions <span class='removed removed-inline removed-breaking-inline'>options</span> <span class='added '>transactionOptions</span>)
</div><div data-is-breaking="">	public TransactionScope (Transaction <span class='removed removed-inline removed-breaking-inline'>transaction</span> <span class='added '>transactionToUse</span>, System.TimeSpan <span class='removed removed-inline removed-breaking-inline'>timeout</span> <span class='added '>scopeTimeout</span>, EnterpriseServicesInteropOption <span class='removed removed-inline removed-breaking-inline'>opt</span> <span class='added '>interopOption</span>)
</div><div data-is-breaking="">	public TransactionScope (TransactionScopeOption <span class='removed removed-inline removed-breaking-inline'>option</span> <span class='added '>scopeOption</span>, System.TimeSpan <span class='removed removed-inline removed-breaking-inline'>timeout</span> <span class='added '>scopeTimeout</span>, TransactionScopeAsyncFlowOption asyncFlow)
</div><div data-is-breaking="">	public TransactionScope (TransactionScopeOption scopeOption, TransactionOptions <span class='removed removed-inline removed-breaking-inline'>options</span> <span class='added '>transactionOptions</span>, EnterpriseServicesInteropOption <span class='removed removed-inline removed-breaking-inline'>opt</span> <span class='added '>interopOption</span>)
</div></pre>

</div> <!-- end type TransactionScope -->

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
</script><h1 id='diff/xm/XamMac.html'>XamMac.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoMac --> <div> 
<h2>Namespace MonoMac</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: MonoMac.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.12"</span> <span class='added '>"10.13"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"3.4.0"</span> <span class='added '>"3.99.1"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VisionLibrary = "/System/Library/Frameworks/Vision.framework/Vision";</span>
</pre>
</div>

</div> <!-- end type Constants -->

</div> <!-- end namespace MonoMac -->
<!-- start namespace MonoMac.AVFoundation --> <div> 
<h2>Namespace MonoMac.AVFoundation</h2>
<!-- start type AVCaptureVideoPreviewLayer --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureVideoPreviewLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVCaptureVideoPreviewLayer -->
<!-- start type AVPlayerLayer --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayerLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVPlayerLayer -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVSampleBufferDisplayLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVSynchronizedLayer --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVSynchronizedLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSynchronizedLayer -->

</div> <!-- end namespace MonoMac.AVFoundation -->
<!-- start namespace MonoMac.AVKit --> <div> 
<h2>Namespace MonoMac.AVKit</h2>
<div> <!-- start type AVRoutePickerView -->
<h3>New Type MonoMac.AVKit.AVRoutePickerView</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerView : MonoMac.AppKit.NSView, MonoMac.AppKit.INSAccessibility, MonoMac.AppKit.INSAccessibilityElementProtocol, MonoMac.AppKit.INSAppearanceCustomization, MonoMac.AppKit.INSDraggingDestination, MonoMac.AppKit.INSTouchBarProvider, MonoMac.AppKit.INSUserInterfaceItemIdentification, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (System.Drawing.RectangleF frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVRoutePickerViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RoutePickerButtonBordered { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MonoMac.AppKit.NSColor GetRoutePickerButtonColor (AVRoutePickerViewButtonState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetRoutePickerButtonColor (MonoMac.AppKit.NSColor color, AVRoutePickerViewButtonState state);</span>
}
</pre>
</div> <!-- end type AVRoutePickerView -->
<div> <!-- start type AVRoutePickerViewButtonState -->
<h3>New Type MonoMac.AVKit.AVRoutePickerViewButtonState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVRoutePickerViewButtonState {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ActiveHighlighted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NormalHighlighted = 1,</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewButtonState -->
<div> <!-- start type AVRoutePickerViewDelegate -->
<h3>New Type MonoMac.AVKit.AVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerViewDelegate : MonoMac.Foundation.NSObject, IAVRoutePickerViewDelegate, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndPresentingRoutes (AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginPresentingRoutes (AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate -->
<div> <!-- start type AVRoutePickerViewDelegate_Extensions -->
<h3>New Type MonoMac.AVKit.AVRoutePickerViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVRoutePickerViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate_Extensions -->
<div> <!-- start type IAVRoutePickerViewDelegate -->
<h3>New Type MonoMac.AVKit.IAVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVRoutePickerViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IAVRoutePickerViewDelegate -->

</div> <!-- end namespace MonoMac.AVKit -->
<!-- start namespace MonoMac.AppKit --> <div> 
<h2>Namespace MonoMac.AppKit</h2>
<!-- start type NSAccessibilityAttributes --> <div>
<h3>Type Changed: MonoMac.AppKit.NSAccessibilityAttributes</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnotationTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString CustomTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString LanguageTextAttribute { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityAttributes -->
<!-- start type NSAccessibilityElement --> <div>
<h3>Type Changed: MonoMac.AppKit.NSAccessibilityElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityElement -->
<!-- start type NSAccessibilityRoles --> <div>
<h3>Type Changed: MonoMac.AppKit.NSAccessibilityRoles</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString PageRole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityRoles -->
<!-- start type NSAccessibilitySubroles --> <div>
<h3>Type Changed: MonoMac.AppKit.NSAccessibilitySubroles</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString CollectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString SectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString TabButtonSubrole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilitySubroles -->
<!-- start type NSAccessibility_Extensions --> <div>
<h3>Type Changed: MonoMac.AppKit.NSAccessibility_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityElement[] GetAccessibilityChildrenInNavigationOrder (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomAction[] GetAccessibilityCustomActions (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomRotor[] GetAccessibilityCustomRotors (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityChildrenInNavigationOrder (INSAccessibility This, NSAccessibilityElement[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomActions (INSAccessibility This, NSAccessibilityCustomAction[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomRotors (INSAccessibility This, NSAccessibilityCustomRotor[] value);</span>
</pre>
</div>

</div> <!-- end type NSAccessibility_Extensions -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: MonoMac.AppKit.NSApplication</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;NSApplicationOpenUrlsEventArgs&gt; OpenUrls;</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSApplicationDelegate --> <div>
<h3>Type Changed: MonoMac.AppKit.NSApplicationDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenUrls (NSApplication application, MonoMac.Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate -->
<!-- start type NSApplicationDelegate_Extensions --> <div>
<h3>Type Changed: MonoMac.AppKit.NSApplicationDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void OpenUrls (INSApplicationDelegate This, NSApplication application, MonoMac.Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate_Extensions -->
<!-- start type NSBezierPath --> <div>
<h3>Type Changed: MonoMac.AppKit.NSBezierPath</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (uint[], NSFont)' instead.")]
	public void AppendPathWithGlyphs (uint[] glyphs, NSFont font);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (CGPoint[])' instead.")]
	public void AppendPathWithPoints (System.Drawing.PointF[] points);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Append (NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (System.Drawing.PointF[] points);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (uint[] glyphs, NSFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AppendBezierPathWithCGGlyph (ushort glyph, NSFont font);</span>
</pre>
</div>

</div> <!-- end type NSBezierPath -->
<!-- start type NSButton --> <div>
<h3>Type Changed: MonoMac.AppKit.NSButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Drawing.SizeF GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
</pre>
</div>

</div> <!-- end type NSButton -->
<!-- start type NSCell --> <div>
<h3>Type Changed: MonoMac.AppKit.NSCell</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCell -->
<!-- start type NSCollectionView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSCollectionView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSCollectionViewPrefetching PrefetchDataSource { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCollectionView -->
<!-- start type NSCollectionViewTransitionLayout --> <div>
<h3>Type Changed: MonoMac.AppKit.NSCollectionViewTransitionLayout</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the constructor that allows you to set currentLayout and newLayout.")]
	public NSCollectionViewTransitionLayout ();</span>
</div></pre>

</div> <!-- end type NSCollectionViewTransitionLayout -->
<!-- start type NSColor --> <div>
<h3>Type Changed: MonoMac.AppKit.NSColor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBlueColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBrownColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGrayColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGreenColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemOrangeColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPinkColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPurpleColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemRedColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemYellowColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorType Type { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name, MonoMac.Foundation.NSBundle bundle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSColor GetColor (NSColorType type);</span>
</pre>
</div>

</div> <!-- end type NSColor -->
<!-- start type NSColorPickerTouchBarItem --> <div>
<h3>Type Changed: MonoMac.AppKit.NSColorPickerTouchBarItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorSpace[] AllowedColorSpaces { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSColorPickerTouchBarItem -->
<!-- start type NSDocument --> <div>
<h3>Type Changed: MonoMac.AppKit.NSDocument</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentSharing { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (MonoMac.Foundation.NSCoder coder, MonoMac.Foundation.NSOperationQueue queue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Prepare (NSSharingServicePicker sharingServicePicker);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ShareDocument (NSSharingService sharingService, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; ShareDocumentAsync (NSSharingService sharingService);</span>
</pre>
</div>

</div> <!-- end type NSDocument -->
<!-- start type NSDocumentController --> <div>
<h3>Type Changed: MonoMac.AppKit.NSDocumentController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsAutomaticShareMenu { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMenuItem StandardShareMenuItem { get; }</span>
</pre>
</div>

</div> <!-- end type NSDocumentController -->
<!-- start type NSDrawer --> <div>
<h3>Type Changed: MonoMac.AppKit.NSDrawer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDrawer -->
<!-- start type NSFont --> <div>
<h3>Type Changed: MonoMac.AppKit.NSFont</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSFont FromCTFont (MonoMac.CoreText.CTFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Drawing.SizeF GetAdvancement (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Drawing.SizeF[] GetAdvancements (ushort[] glyphs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Drawing.RectangleF GetBoundingRect (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Drawing.RectangleF[] GetBoundingRects (ushort[] glyphs);</span>
</pre>
</div>

</div> <!-- end type NSFont -->
<!-- start type NSFontDescriptor --> <div>
<h3>Type Changed: MonoMac.AppKit.NSFontDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RequiresFontAssetRequest { get; }</span>
</pre>
</div>

</div> <!-- end type NSFontDescriptor -->
<!-- start type NSFontSymbolicTraits --> <div>
<h3>Type Changed: MonoMac.AppKit.NSFontSymbolicTraits</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TraitLooseLeading = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">TraitTightLeading = 32768,</span>
</pre>
</div>

</div> <!-- end type NSFontSymbolicTraits -->
<!-- start type NSGlyphInfo --> <div>
<h3>Type Changed: MonoMac.AppKit.NSGlyphInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BaseString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ushort GlyphId { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGlyphInfo GetGlyphInfo (ushort glyph, NSFont font, string string);</span>
</pre>
</div>

</div> <!-- end type NSGlyphInfo -->
<!-- start type NSGroupTouchBarItem --> <div>
<h3>Type Changed: MonoMac.AppKit.NSGroupTouchBarItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions EffectiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceLayoutDirection GroupUserInterfaceLayoutDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float PreferredItemWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrefersEqualWidths { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions[] PrioritizedCompressionOptions { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateAlertStyleGroupItem (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateGroupItem (string identifier, NSTouchBarItem[] items, NSUserInterfaceCompressionOptions allowedCompressionOptions);</span>
</pre>
</div>

</div> <!-- end type NSGroupTouchBarItem -->
<!-- start type NSImageName --> <div>
<h3>Type Changed: MonoMac.AppKit.NSImageName</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TouchBarRemoveTemplate = 116,</span>
</pre>
</div>

</div> <!-- end type NSImageName -->
<!-- start type NSLevelIndicator --> <div>
<h3>Type Changed: MonoMac.AppKit.NSLevelIndicator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor CriticalFillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DrawsTieredCapacityLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Editable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor FillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLevelIndicatorPlaceholderVisibility PlaceholderVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingPlaceholderImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor WarningFillColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSLevelIndicator -->
<!-- start type NSMenu --> <div>
<h3>Type Changed: MonoMac.AppKit.NSMenu</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenu -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: MonoMac.AppKit.NSMenuItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsKeyEquivalentWhenHidden { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOpenGLLayer --> <div>
<h3>Type Changed: MonoMac.AppKit.NSOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSOpenGLLayer -->
<!-- start type NSPasteboard --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPasteboard</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString NSPasteboardNameDrag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString NSPasteboardNameFind { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString NSPasteboardNameFont { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString NSPasteboardNameGeneral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString NSPasteboardNameRuler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString NSPasteboardTypeFileUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString NSPasteboardTypeUrl { get; }</span>
</pre>
</div>

</div> <!-- end type NSPasteboard -->
<!-- start type NSPopUpButton --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPopUpButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>

</div> <!-- end type NSPopUpButton -->
<!-- start type NSPopover --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPopover</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSAppearanceCustomization</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'GetAppearance' and 'SetAppearance' methods instead.")]
	public virtual NSPopoverAppearance Appearance { get; set; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAppearance EffectiveAppearance { get; }</span>
</pre>
</div>

</div> <!-- end type NSPopover -->
<!-- start type NSResponder --> <div>
<h3>Type Changed: MonoMac.AppKit.NSResponder</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (MonoMac.Foundation.NSCoder coder, MonoMac.Foundation.NSOperationQueue queue);</span>
</pre>
</div>

</div> <!-- end type NSResponder -->
<!-- start type NSSegmentedControl --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSegmentedControl</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSegmentDistribution SegmentDistribution { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTextAlignment GetAlignment (int segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Drawing.SizeF GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int GetTag (int segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetToolTip (int forSegment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAlignment (NSTextAlignment alignment, int segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetShowsMenuIndicator (bool showsMenuIndicator, int segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTag (int tag, int segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetToolTip (string toolTip, int segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShowsMenuIndicator (int segment);</span>
</pre>
</div>

</div> <!-- end type NSSegmentedControl -->
<!-- start type NSSliderAccessory --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSliderAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSSliderAccessory -->
<!-- start type NSSliderTouchBarItem --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSliderTouchBarItem</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Drawing.SizeF GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
</pre>
</div>

</div> <!-- end type NSSliderTouchBarItem -->
<!-- start type NSSplitViewController --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSplitViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceValidations</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ValidateUserInterfaceItem (INSValidatedUserInterfaceItem item);</span>
</pre>
</div>

</div> <!-- end type NSSplitViewController -->
<!-- start type NSStatusBarButton --> <div>
<h3>Type Changed: MonoMac.AppKit.NSStatusBarButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>

</div> <!-- end type NSStatusBarButton -->
<!-- start type NSStoryboard --> <div>
<h3>Type Changed: MonoMac.AppKit.NSStoryboard</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSStoryboard MainStoryboard { get; }</span>
</pre>
</div>

</div> <!-- end type NSStoryboard -->
<!-- start type NSTableView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTableView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesAutomaticRowHeights { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTableView -->
<!-- start type NSTextList --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextList</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextList (NSTextListMarkerFormats format, NSTextListOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSTextList -->
<!-- start type NSTouchBar --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTouchBar</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string EscapeKeyReplacementItemIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTouchBar -->
<!-- start type NSTouchBarItemIdentifier --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTouchBarItemIdentifier</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CandidateList = 10,</span>
</pre>
</div>

</div> <!-- end type NSTouchBarItemIdentifier -->
<!-- start type NSView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSView -->
<!-- start type NSWindow --> <div>
<h3>Type Changed: MonoMac.AppKit.NSWindow</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTab Tab { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTabGroup TabGroup { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the EndSheet(NSWindow,NSModalResponse) overload.")]
	public virtual void EndSheet (NSWindow sheetWindow, int returnCode);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndSheet (NSWindow sheetWindow, NSModalResponse returnCode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToggleTabOverview (MonoMac.Foundation.NSObject sender);</span>
</pre>
</div>

</div> <!-- end type NSWindow -->
<!-- start type NSWorkspace --> <div>
<h3>Type Changed: MonoMac.AppKit.NSWorkspace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SwitchControlEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool VoiceOverEnabled { get; }</span>
</pre>
</div>

</div> <!-- end type NSWorkspace -->
<div> <!-- start type DownloadFontAssetsRequestCompletionHandler -->
<h3>New Type MonoMac.AppKit.DownloadFontAssetsRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate DownloadFontAssetsRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DownloadFontAssetsRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (MonoMac.Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type DownloadFontAssetsRequestCompletionHandler -->
<div> <!-- start type INSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type MonoMac.AppKit.INSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityCustomRotorItemSearchDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type INSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type INSAccessibilityElementLoading -->
<h3>New Type MonoMac.AppKit.INSAccessibilityElementLoading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityElementLoading : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityElement GetAccessibilityElement (MonoMac.Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type INSAccessibilityElementLoading -->
<div> <!-- start type INSCollectionViewPrefetching -->
<h3>New Type MonoMac.AppKit.INSCollectionViewPrefetching</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCollectionViewPrefetching : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrefetchItems (NSCollectionView collectionView, MonoMac.Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type INSCollectionViewPrefetching -->
<div> <!-- start type INSUserInterfaceCompression -->
<h3>New Type MonoMac.AppKit.INSUserInterfaceCompression</h3>
<pre class='added' data-is-non-breaking="">
public interface INSUserInterfaceCompression : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Drawing.SizeF GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
}
</pre>
</div> <!-- end type INSUserInterfaceCompression -->
<div> <!-- start type NSAboutPanelOption -->
<h3>New Type MonoMac.AppKit.NSAboutPanelOption</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAboutPanelOption {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationIcon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString Credits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString Version { get; }</span>
}
</pre>
</div> <!-- end type NSAboutPanelOption -->
<div> <!-- start type NSAccessibilityAnnotationAttributeKey -->
<h3>New Type MonoMac.AppKit.NSAccessibilityAnnotationAttributeKey</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityAnnotationAttributeKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnotationElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnotationLabel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnotationLocation { get; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationAttributeKey -->
<div> <!-- start type NSAccessibilityAnnotationPosition -->
<h3>New Type MonoMac.AppKit.NSAccessibilityAnnotationPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityAnnotationPosition {
	<span class='added added-field ' data-is-non-breaking="">End = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FullRange = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Start = 1,</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationPosition -->
<div> <!-- start type NSAccessibilityCustomAction -->
<h3>New Type MonoMac.AppKit.NSAccessibilityCustomAction</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomAction : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, System.Func&lt;bool&gt; handler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector selector);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;bool&gt; Handler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.ObjCRuntime.Selector Selector { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Target { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomAction -->
<div> <!-- start type NSAccessibilityCustomRotor -->
<h3>New Type MonoMac.AppKit.NSAccessibilityCustomRotor</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotor : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (NSAccessibilityCustomRotorType rotorType, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (string label, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityElementLoading ItemLoadingDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityCustomRotorItemSearchDelegate ItemSearchDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorType Type { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotor -->
<div> <!-- start type NSAccessibilityCustomRotorItemResult -->
<h3>New Type MonoMac.AppKit.NSAccessibilityCustomRotorItemResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorItemResult : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (NSAccessibilityElement targetElement);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (MonoMac.Foundation.INSSecureCoding itemLoadingToken, string customLabel);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.INSSecureCoding ItemLoadingToken { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement TargetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSRange TargetRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemResult -->
<div> <!-- start type NSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type MonoMac.AppKit.NSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSAccessibilityCustomRotorItemSearchDelegate : MonoMac.Foundation.NSObject, INSAccessibilityCustomRotorItemSearchDelegate, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemSearchDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemSearchDelegate (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemSearchDelegate (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemSearchDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type NSAccessibilityCustomRotorItemSearchDelegate_Extensions -->
<h3>New Type MonoMac.AppKit.NSAccessibilityCustomRotorItemSearchDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityCustomRotorItemSearchDelegate_Extensions {
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemSearchDelegate_Extensions -->
<div> <!-- start type NSAccessibilityCustomRotorSearchDirection -->
<h3>New Type MonoMac.AppKit.NSAccessibilityCustomRotorSearchDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorSearchDirection {
	<span class='added added-field ' data-is-non-breaking="">Next = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Previous = 0,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchDirection -->
<div> <!-- start type NSAccessibilityCustomRotorSearchParameters -->
<h3>New Type MonoMac.AppKit.NSAccessibilityCustomRotorSearchParameters</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorSearchParameters : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorSearchParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorSearchParameters (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorSearchParameters (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorSearchParameters (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult CurrentItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FilterString { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorSearchDirection SearchDirection { get; set; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchParameters -->
<div> <!-- start type NSAccessibilityCustomRotorType -->
<h3>New Type MonoMac.AppKit.NSAccessibilityCustomRotorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorType {
	<span class='added added-field ' data-is-non-breaking="">Annotation = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">BoldText = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Custom = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Heading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel1 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel2 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel3 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel4 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel5 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel6 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">ItalicText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">MisspelledWord = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Table = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">TextField = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlinedText = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">VisitedLink = 20,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorType -->
<div> <!-- start type NSAccessibilityElementLoading_Extensions -->
<h3>New Type MonoMac.AppKit.NSAccessibilityElementLoading_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityElementLoading_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MonoMac.Foundation.NSRange GetAccessibilityRangeInTargetElement (INSAccessibilityElementLoading This, MonoMac.Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type NSAccessibilityElementLoading_Extensions -->
<div> <!-- start type NSApplicationOpenUrlsEventArgs -->
<h3>New Type MonoMac.AppKit.NSApplicationOpenUrlsEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class NSApplicationOpenUrlsEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSApplicationOpenUrlsEventArgs (MonoMac.Foundation.NSUrl[] urls);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public MonoMac.Foundation.NSUrl[] Urls { get; set; }</span>
}
</pre>
</div> <!-- end type NSApplicationOpenUrlsEventArgs -->
<div> <!-- start type NSCollectionViewPrefetching_Extensions -->
<h3>New Type MonoMac.AppKit.NSCollectionViewPrefetching_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSCollectionViewPrefetching_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelPrefetching (INSCollectionViewPrefetching This, NSCollectionView collectionView, MonoMac.Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type NSCollectionViewPrefetching_Extensions -->
<div> <!-- start type NSColorType -->
<h3>New Type MonoMac.AppKit.NSColorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSColorType {
	<span class='added added-field ' data-is-non-breaking="">Catalog = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ComponentBased = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Pattern = 1,</span>
}
</pre>
</div> <!-- end type NSColorType -->
<div> <!-- start type NSFontAssetRequest -->
<h3>New Type MonoMac.AppKit.NSFontAssetRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSFontAssetRequest : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFontAssetRequest (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFontAssetRequest (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFontAssetRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFontAssetRequest (NSFontDescriptor[] fontDescriptors, NSFontAssetRequestOptions options);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFontDescriptor[] DownloadedFontDescriptors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSProgress Progress { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DownloadFontAssets (DownloadFontAssetsRequestCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type NSFontAssetRequest -->
<div> <!-- start type NSFontAssetRequestOptions -->
<h3>New Type MonoMac.AppKit.NSFontAssetRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontAssetRequestOptions {
	<span class='added added-field ' data-is-non-breaking="">UsesStandardUI = 1,</span>
}
</pre>
</div> <!-- end type NSFontAssetRequestOptions -->
<div> <!-- start type NSFontError -->
<h3>New Type MonoMac.AppKit.NSFontError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFontError {
	<span class='added added-field ' data-is-non-breaking="">AssetDownloadError = 66304,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMaximum = 66335,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMinimum = 66304,</span>
}
</pre>
</div> <!-- end type NSFontError -->
<div> <!-- start type NSFontPanelModeMask -->
<h3>New Type MonoMac.AppKit.NSFontPanelModeMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontPanelModeMask {
	<span class='added added-field ' data-is-non-breaking="">AllEffects = 1048320,</span>
	<span class='added added-field ' data-is-non-breaking="">AllModes = 4294967295,</span>
	<span class='added added-field ' data-is-non-breaking="">Collection = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">DocumentColorEffect = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">Face = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ShadowEffect = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">Size = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">StandardModes = 65535,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikethroughEffect = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">TextColorEffect = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlineEffect = 256,</span>
}
</pre>
</div> <!-- end type NSFontPanelModeMask -->
<div> <!-- start type NSLevelIndicatorPlaceholderVisibility -->
<h3>New Type MonoMac.AppKit.NSLevelIndicatorPlaceholderVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSLevelIndicatorPlaceholderVisibility {
	<span class='added added-field ' data-is-non-breaking="">Always = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WhileEditing = 2,</span>
}
</pre>
</div> <!-- end type NSLevelIndicatorPlaceholderVisibility -->
<div> <!-- start type NSObject_NSFontPanelValidationAdditions -->
<h3>New Type MonoMac.AppKit.NSObject_NSFontPanelValidationAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSObject_NSFontPanelValidationAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFontPanelModeMask GetValidModes (MonoMac.Foundation.NSObject This, NSFontPanel fontPanel);</span>
}
</pre>
</div> <!-- end type NSObject_NSFontPanelValidationAdditions -->
<div> <!-- start type NSRulerViewUnits -->
<h3>New Type MonoMac.AppKit.NSRulerViewUnits</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSRulerViewUnits {
	<span class='added added-field ' data-is-non-breaking="">Centimeters = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inches = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Picas = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Points = 2,</span>
}
</pre>
</div> <!-- end type NSRulerViewUnits -->
<div> <!-- start type NSRulerViewUnitsExtensions -->
<h3>New Type MonoMac.AppKit.NSRulerViewUnitsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSRulerViewUnitsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MonoMac.Foundation.NSString GetConstant (NSRulerViewUnits self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSRulerViewUnits GetValue (MonoMac.Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSRulerViewUnitsExtensions -->
<div> <!-- start type NSSegmentDistribution -->
<h3>New Type MonoMac.AppKit.NSSegmentDistribution</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSSegmentDistribution {
	<span class='added added-field ' data-is-non-breaking="">Fill = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FillEqually = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FillProportionally = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Fit = 0,</span>
}
</pre>
</div> <!-- end type NSSegmentDistribution -->
<div> <!-- start type NSTextListMarkerFormats -->
<h3>New Type MonoMac.AppKit.NSTextListMarkerFormats</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTextListMarkerFormats {
	<span class='added added-field ' data-is-non-breaking="">Box = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Check = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Decimal = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Disc = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Hyphen = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseAlpha = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseHexadecimal = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseLatin = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseRoman = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Octal = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseAlpha = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseHexadecimal = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseLatin = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseRoman = 15,</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormats -->
<div> <!-- start type NSTextListMarkerFormatsExtensions -->
<h3>New Type MonoMac.AppKit.NSTextListMarkerFormatsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTextListMarkerFormatsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MonoMac.Foundation.NSString GetConstant (NSTextListMarkerFormats self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextListMarkerFormats GetValue (MonoMac.Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormatsExtensions -->
<div> <!-- start type NSUserInterfaceCompressionOptions -->
<h3>New Type MonoMac.AppKit.NSUserInterfaceCompressionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class NSUserInterfaceCompressionOptions : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (MonoMac.Foundation.NSSet options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions BreakEqualWidthsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Empty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideImagesOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideTextOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions ReduceMetricsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions StandardOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByAdding (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByRemoving (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Intersects (NSUserInterfaceCompressionOptions options);</span>
}
</pre>
</div> <!-- end type NSUserInterfaceCompressionOptions -->
<div> <!-- start type NSUserInterfaceCompression_Extensions -->
<h3>New Type MonoMac.AppKit.NSUserInterfaceCompression_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSUserInterfaceCompression_Extensions {
}
</pre>
</div> <!-- end type NSUserInterfaceCompression_Extensions -->
<div> <!-- start type NSWindowTab -->
<h3>New Type MonoMac.AppKit.NSWindowTab</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTab : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTab ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTab (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTab (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTab (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView AccessoryView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSAttributedString AttributedTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ToolTip { get; set; }</span>
}
</pre>
</div> <!-- end type NSWindowTab -->
<div> <!-- start type NSWindowTabGroup -->
<h3>New Type MonoMac.AppKit.NSWindowTabGroup</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTabGroup : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTabGroup (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTabGroup (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTabGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool OverviewVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow SelectedWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TabBarVisible { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow[] Windows { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (NSWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Insert (NSWindow window, int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Remove (NSWindow window);</span>
}
</pre>
</div> <!-- end type NSWindowTabGroup -->

</div> <!-- end namespace MonoMac.AppKit -->
<!-- start namespace MonoMac.CoreAnimation --> <div> 
<h2>Namespace MonoMac.CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CAAnimationGroup --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAAnimationGroup</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimationGroup -->
<!-- start type CABasicAnimation --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CABasicAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CABasicAnimation -->
<!-- start type CAConstraint --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAConstraint</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAConstraint -->
<!-- start type CAEmitterBehavior --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAEmitterBehavior</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterBehavior -->
<!-- start type CAEmitterCell --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAEmitterCell</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterCell -->
<!-- start type CAEmitterLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAEmitterLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterLayer -->
<!-- start type CAGradientLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAGradientLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAGradientLayer -->
<!-- start type CAKeyFrameAnimation --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAKeyFrameAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAKeyFrameAnimation -->
<!-- start type CALayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CALayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CALayer -->
<!-- start type CAMediaTimingFunction --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAMediaTimingFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAMediaTimingFunction -->
<!-- start type CAOpenGLLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAOpenGLLayer -->
<!-- start type CAPropertyAnimation --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAPropertyAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAPropertyAnimation -->
<!-- start type CAReplicatorLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAReplicatorLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAReplicatorLayer -->
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAScrollLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<!-- start type CAShapeLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAShapeLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAShapeLayer -->
<!-- start type CASpringAnimation --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CASpringAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CASpringAnimation -->
<!-- start type CATextLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CATextLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATextLayer -->
<!-- start type CATiledLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CATiledLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATiledLayer -->
<!-- start type CATransformLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CATransformLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransformLayer -->
<!-- start type CATransition --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CATransition</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransition -->
<!-- start type CAValueFunction --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAValueFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAValueFunction -->

</div> <!-- end namespace MonoMac.CoreAnimation -->
<!-- start namespace MonoMac.CoreData --> <div> 
<h2>Namespace MonoMac.CoreData</h2>
<!-- start type MigrationErrorType --> <div>
<h3>Type Changed: MonoMac.CoreData.MigrationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HistoryTokenExpired = 134301,</span>
</pre>
</div>

</div> <!-- end type MigrationErrorType -->
<!-- start type NSAttributeType --> <div>
<h3>Type Changed: MonoMac.CoreData.NSAttributeType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Uri = 1200,</span>
	<span class='added added-field ' data-is-non-breaking="">Uuid = 1100,</span>
</pre>
</div>

</div> <!-- end type NSAttributeType -->
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: MonoMac.CoreData.NSEntityDescription</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSExpression CoreSpotlightDisplayNameExpression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription[] Indexes { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: MonoMac.CoreData.NSManagedObjectContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionAuthor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: MonoMac.CoreData.NSPersistentStoreCoordinator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString CoreSpotlightExporter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString HistoryTrackingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString UbiquitousContainerIdentifierKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator -->
<!-- start type NSQueryGenerationToken --> <div>
<h3>Type Changed: MonoMac.CoreData.NSQueryGenerationToken</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSQueryGenerationToken -->
<!-- start type ValidationErrorType --> <div>
<h3>Type Changed: MonoMac.CoreData.ValidationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidUri = 1690,</span>
</pre>
</div>

</div> <!-- end type ValidationErrorType -->
<div> <!-- start type NSFetchIndexDescription -->
<h3>New Type MonoMac.CoreData.NSFetchIndexDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexDescription : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (string name, NSFetchIndexElementDescription[] elements);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementDescription[] Elements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSEntityDescription Entity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSPredicate PartialIndexPredicate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSFetchIndexDescription -->
<div> <!-- start type NSFetchIndexElementDescription -->
<h3>New Type MonoMac.CoreData.NSFetchIndexElementDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexElementDescription : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (NSPropertyDescription property, NSFetchIndexElementType collationType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementType CollationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription IndexDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAscending { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPropertyDescription Property { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PropertyName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementDescription -->
<div> <!-- start type NSFetchIndexElementType -->
<h3>New Type MonoMac.CoreData.NSFetchIndexElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFetchIndexElementType {
	<span class='added added-field ' data-is-non-breaking="">Binary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RTree = 1,</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementType -->
<div> <!-- start type NSPersistentHistoryChange -->
<h3>New Type MonoMac.CoreData.NSPersistentHistoryChange</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryChange : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryChange (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryChange (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual long ChangeId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChangeType ChangeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectID ChangedObjectId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSDictionary Tombstone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryTransaction Transaction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSSet UpdatedProperties { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChange -->
<div> <!-- start type NSPersistentHistoryChangeRequest -->
<h3>New Type MonoMac.CoreData.NSPersistentHistoryChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryChangeRequest : MonoMac.CoreData.NSPersistentStoreRequest, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryChangeRequest (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryChangeRequest (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (MonoMac.Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (MonoMac.Foundation.NSDate date);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeRequest -->
<div> <!-- start type NSPersistentHistoryChangeType -->
<h3>New Type MonoMac.CoreData.NSPersistentHistoryChangeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryChangeType {
	<span class='added added-field ' data-is-non-breaking="">Delete = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Update = 1,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeType -->
<div> <!-- start type NSPersistentHistoryResult -->
<h3>New Type MonoMac.CoreData.NSPersistentHistoryResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryResult : MonoMac.CoreData.NSPersistentStoreResult, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Result { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; }</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResult -->
<div> <!-- start type NSPersistentHistoryResultType -->
<h3>New Type MonoMac.CoreData.NSPersistentHistoryResultType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryResultType {
	<span class='added added-field ' data-is-non-breaking="">ChangesOnly = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectIds = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusOnly = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsAndChanges = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsOnly = 3,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResultType -->
<div> <!-- start type NSPersistentHistoryToken -->
<h3>New Type MonoMac.CoreData.NSPersistentHistoryToken</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryToken : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryToken -->
<div> <!-- start type NSPersistentHistoryTransaction -->
<h3>New Type MonoMac.CoreData.NSPersistentHistoryTransaction</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryTransaction : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryTransaction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryTransaction (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryTransaction (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryTransaction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BundleId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChange[] Changes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContextName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSNotification ObjectIdNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProcessId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StoreId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSDate Timestamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long TransactionNumber { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryTransaction -->

</div> <!-- end namespace MonoMac.CoreData -->
<!-- start namespace MonoMac.CoreImage --> <div> 
<h2>Namespace MonoMac.CoreImage</h2>
<!-- start type CIImageAccumulator --> <div>
<h3>Type Changed: MonoMac.CoreImage.CIImageAccumulator</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CIImageAccumulator ();</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (System.Drawing.RectangleF extent, int format, MonoMac.CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (System.Drawing.RectangleF extent, int format, MonoMac.CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIImageAccumulator -->
<!-- start type CIQRCodeFeature --> <div>
<h3>Type Changed: MonoMac.CoreImage.CIQRCodeFeature</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type CIQRCodeFeature -->
<div> <!-- start type CIAreaMinMaxRed -->
<h3>New Type MonoMac.CoreImage.CIAreaMinMaxRed</h3>
<pre class='added' data-is-non-breaking="">
public class CIAreaMinMaxRed : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAreaMinMaxRed -->
<div> <!-- start type CIAttributedTextImageGenerator -->
<h3>New Type MonoMac.CoreImage.CIAttributedTextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIAttributedTextImageGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAttributedTextImageGenerator -->
<div> <!-- start type CIBarcodeGenerator -->
<h3>New Type MonoMac.CoreImage.CIBarcodeGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIBarcodeGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBarcodeGenerator -->
<div> <!-- start type CIBicubicScaleTransform -->
<h3>New Type MonoMac.CoreImage.CIBicubicScaleTransform</h3>
<pre class='added' data-is-non-breaking="">
public class CIBicubicScaleTransform : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBicubicScaleTransform -->
<div> <!-- start type CIBokehBlur -->
<h3>New Type MonoMac.CoreImage.CIBokehBlur</h3>
<pre class='added' data-is-non-breaking="">
public class CIBokehBlur : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBokehBlur -->
<div> <!-- start type CIColorCubesMixedWithMask -->
<h3>New Type MonoMac.CoreImage.CIColorCubesMixedWithMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCubesMixedWithMask : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCubesMixedWithMask -->
<div> <!-- start type CIColorCurves -->
<h3>New Type MonoMac.CoreImage.CIColorCurves</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCurves : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCurves -->
<div> <!-- start type CIDepthBlurEffect -->
<h3>New Type MonoMac.CoreImage.CIDepthBlurEffect</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthBlurEffect : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthBlurEffect -->
<div> <!-- start type CIDepthToDisparity -->
<h3>New Type MonoMac.CoreImage.CIDepthToDisparity</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthToDisparity : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthToDisparity -->
<div> <!-- start type CIDisparityToDepth -->
<h3>New Type MonoMac.CoreImage.CIDisparityToDepth</h3>
<pre class='added' data-is-non-breaking="">
public class CIDisparityToDepth : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type MonoMac.CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CILabDeltaE -->
<div> <!-- start type CIMorphologyGradient -->
<h3>New Type MonoMac.CoreImage.CIMorphologyGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyGradient : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyGradient -->
<div> <!-- start type CIMorphologyMaximum -->
<h3>New Type MonoMac.CoreImage.CIMorphologyMaximum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMaximum : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMaximum -->
<div> <!-- start type CIMorphologyMinimum -->
<h3>New Type MonoMac.CoreImage.CIMorphologyMinimum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMinimum : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMinimum -->
<div> <!-- start type CITextImageGenerator -->
<h3>New Type MonoMac.CoreImage.CITextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CITextImageGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CITextImageGenerator -->

</div> <!-- end namespace MonoMac.CoreImage -->
<!-- start namespace MonoMac.CoreLocation --> <div> 
<h2>Namespace MonoMac.CoreLocation</h2>
<!-- start type CLGeocoder --> <div>
<h3>Type Changed: MonoMac.CoreLocation.CLGeocoder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLRegion region, MonoMac.Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region, MonoMac.Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, MonoMac.Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, MonoMac.Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->

</div> <!-- end namespace MonoMac.CoreLocation -->
<!-- start namespace MonoMac.Foundation --> <div> 
<h2>Namespace MonoMac.Foundation</h2>
<!-- start type NSActivityOptions --> <div>
<h3>Type Changed: MonoMac.Foundation.NSActivityOptions</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	IdleDisplaySleepDisabled = <span class='removed removed-inline removed-breaking-inline'>256</span> <span class='added '>1099511627776</span>
</div></pre>

</div> <!-- end type NSActivityOptions -->
<!-- start type NSDimension --> <div>
<h3>Type Changed: MonoMac.Foundation.NSDimension</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">[Obsolete ("Not intended to be directly instantiated, this is an abstract class.")]
	public NSDimension ();</span>
</pre>
</div>

</div> <!-- end type NSDimension -->
<!-- start type NSFileManager --> <div>
<h3>Type Changed: MonoMac.Foundation.NSFileManager</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnmountVolume (NSUrl url, NSFileManagerUnmountOptions mask, System.Action&lt;NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UnmountVolumeAsync (NSUrl url, NSFileManagerUnmountOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSFileManager -->
<!-- start type NSUnit --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnit</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string)")]
	public NSUnit ();</span>
</div></pre>

</div> <!-- end type NSUnit -->
<!-- start type NSUnitAcceleration --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitAcceleration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAcceleration ();</span>
</div></pre>

</div> <!-- end type NSUnitAcceleration -->
<!-- start type NSUnitAngle --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitAngle</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAngle ();</span>
</div></pre>

</div> <!-- end type NSUnitAngle -->
<!-- start type NSUnitArea --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitArea</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitArea ();</span>
</div></pre>

</div> <!-- end type NSUnitArea -->
<!-- start type NSUnitConcentrationMass --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitConcentrationMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitConcentrationMass ();</span>
</div></pre>

</div> <!-- end type NSUnitConcentrationMass -->
<!-- start type NSUnitDispersion --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitDispersion</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDispersion ();</span>
</div></pre>

</div> <!-- end type NSUnitDispersion -->
<!-- start type NSUnitDuration --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitDuration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDuration ();</span>
</div></pre>

</div> <!-- end type NSUnitDuration -->
<!-- start type NSUnitElectricCharge --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitElectricCharge</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCharge ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCharge -->
<!-- start type NSUnitElectricCurrent --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitElectricCurrent</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCurrent ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCurrent -->
<!-- start type NSUnitElectricPotentialDifference --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitElectricPotentialDifference</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricPotentialDifference ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricPotentialDifference -->
<!-- start type NSUnitElectricResistance --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitElectricResistance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricResistance ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricResistance -->
<!-- start type NSUnitEnergy --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitEnergy</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitEnergy ();</span>
</div></pre>

</div> <!-- end type NSUnitEnergy -->
<!-- start type NSUnitFrequency --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitFrequency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFrequency ();</span>
</div></pre>

</div> <!-- end type NSUnitFrequency -->
<!-- start type NSUnitFuelEfficiency --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitFuelEfficiency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFuelEfficiency ();</span>
</div></pre>

</div> <!-- end type NSUnitFuelEfficiency -->
<!-- start type NSUnitIlluminance --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitIlluminance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitIlluminance ();</span>
</div></pre>

</div> <!-- end type NSUnitIlluminance -->
<!-- start type NSUnitLength --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitLength</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitLength ();</span>
</div></pre>

</div> <!-- end type NSUnitLength -->
<!-- start type NSUnitMass --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitMass ();</span>
</div></pre>

</div> <!-- end type NSUnitMass -->
<!-- start type NSUnitPower --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitPower</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPower ();</span>
</div></pre>

</div> <!-- end type NSUnitPower -->
<!-- start type NSUnitPressure --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitPressure</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPressure ();</span>
</div></pre>

</div> <!-- end type NSUnitPressure -->
<!-- start type NSUnitSpeed --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitSpeed</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitSpeed ();</span>
</div></pre>

</div> <!-- end type NSUnitSpeed -->
<!-- start type NSUnitVolume --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUnitVolume</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitVolume ();</span>
</div></pre>

</div> <!-- end type NSUnitVolume -->
<!-- start type ProtocolAttribute --> <div>
<h3>Type Changed: MonoMac.Foundation.ProtocolAttribute</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string FormalSince { get; set; }</span>
</pre>
</div>

</div> <!-- end type ProtocolAttribute -->
<div> <!-- start type INSItemProviderReading -->
<h3>New Type MonoMac.Foundation.INSItemProviderReading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSItemProviderReading : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSItemProviderReading -->
<div> <!-- start type NSFileProviderMessageInterface -->
<h3>New Type MonoMac.Foundation.NSFileProviderMessageInterface</h3>
<pre class='added' data-is-non-breaking="">
public class NSFileProviderMessageInterface : MonoMac.Foundation.NSObject, INSCoding, INSObjectProtocol, INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
}
</pre>
</div> <!-- end type NSFileProviderMessageInterface -->
<div> <!-- start type NSItemProviderReading_Extensions -->
<h3>New Type MonoMac.Foundation.NSItemProviderReading_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSItemProviderReading_Extensions {
}
</pre>
</div> <!-- end type NSItemProviderReading_Extensions -->
<div> <!-- start type NotImplementedAttribute -->
<h3>New Type MonoMac.Foundation.NotImplementedAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class NotImplementedAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NotImplementedAttribute ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NotImplementedAttribute (string message);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; set; }</span>
}
</pre>
</div> <!-- end type NotImplementedAttribute -->

</div> <!-- end namespace MonoMac.Foundation -->
<!-- start namespace MonoMac.LocalAuthentication --> <div> 
<h2>Namespace MonoMac.LocalAuthentication</h2>
<!-- start type LAStatus --> <div>
<h3>Type Changed: MonoMac.LocalAuthentication.LAStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NotInteractive = -1004,</span>
</pre>
</div>

</div> <!-- end type LAStatus -->

</div> <!-- end namespace MonoMac.LocalAuthentication -->
<!-- start namespace MonoMac.ObjCRuntime --> <div> 
<h2>Namespace MonoMac.ObjCRuntime</h2>
<!-- start type Dlfcn --> <div>
<h3>Type Changed: MonoMac.ObjCRuntime.Dlfcn</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetUInt32 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetUInt64 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt32 (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt64 (IntPtr handle, string symbol, long value);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->
<!-- start type Messaging --> <div>
<h3>Type Changed: MonoMac.ObjCRuntime.Messaging</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static uint UInt32_objc_msgSendSuper_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoMac.Foundation.NSRange arg2);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static uint UInt32_objc_msgSend_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoMac.Foundation.NSRange arg2);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static int int_objc_msgSendSuper_NSRange_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static int int_objc_msgSendSuper_NSRange_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static int int_objc_msgSend_NSRange_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static int int_objc_msgSend_NSRange_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr IntPtr_objc_msgSendSuper_UInt16_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, ushort arg1, IntPtr arg2, IntPtr arg3);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr IntPtr_objc_msgSend_UInt16_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, ushort arg1, IntPtr arg2, IntPtr arg3);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.RectangleF RectangleF_objc_msgSendSuper_UInt16 (IntPtr receiver, IntPtr selector, ushort arg1);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RectangleF_objc_msgSendSuper_stret_UInt16 (System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, ushort arg1);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.RectangleF RectangleF_objc_msgSend_UInt16 (IntPtr receiver, IntPtr selector, ushort arg1);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RectangleF_objc_msgSend_stret_UInt16 (System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, ushort arg1);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.SizeF SizeF_objc_msgSendSuper_UInt16 (IntPtr receiver, IntPtr selector, ushort arg1);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.SizeF SizeF_objc_msgSend_UInt16 (IntPtr receiver, IntPtr selector, ushort arg1);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void void_objc_msgSendSuper_UInt16_IntPtr (IntPtr receiver, IntPtr selector, ushort arg1, IntPtr arg2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void void_objc_msgSend_UInt16_IntPtr (IntPtr receiver, IntPtr selector, ushort arg1, IntPtr arg2);</span>
</pre>
</div>

</div> <!-- end type Messaging -->

</div> <!-- end namespace MonoMac.ObjCRuntime -->
<!-- start namespace MonoMac.QTKit --> <div> 
<h2>Namespace MonoMac.QTKit</h2>
<!-- start type QTCaptureLayer --> <div>
<h3>Type Changed: MonoMac.QTKit.QTCaptureLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTCaptureLayer -->
<!-- start type QTMovieLayer --> <div>
<h3>Type Changed: MonoMac.QTKit.QTMovieLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTMovieLayer -->

</div> <!-- end namespace MonoMac.QTKit -->
<!-- start namespace MonoMac.QuartzComposer --> <div> 
<h2>Namespace MonoMac.QuartzComposer</h2>
<!-- start type QCCompositionLayer --> <div>
<h3>Type Changed: MonoMac.QuartzComposer.QCCompositionLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QCCompositionLayer -->

</div> <!-- end namespace MonoMac.QuartzComposer -->
<!-- start namespace MonoMac.SceneKit --> <div> 
<h2>Namespace MonoMac.SceneKit</h2>
<!-- start type SCNLayer --> <div>
<h3>Type Changed: MonoMac.SceneKit.SCNLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">MonoMac.Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type SCNLayer -->

</div> <!-- end namespace MonoMac.SceneKit -->
<!-- start namespace MonoMac.Security --> <div> 
<h2>Namespace MonoMac.Security</h2>
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: MonoMac.Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_8_SHA256 = 4869,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_SHA256 = 4868,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_GCM_SHA256 = 4865,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_256_GCM_SHA384 = 4866,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_CHACHA20_POLY1305_SHA256 = 4867,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->

</div> <!-- end namespace MonoMac.Security -->
<!-- start namespace MonoMac.SpriteKit --> <div> 
<h2>Namespace MonoMac.SpriteKit</h2>
<div> <!-- start type SKNodeFocusBehavior -->
<h3>New Type MonoMac.SpriteKit.SKNodeFocusBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKNodeFocusBehavior {
	<span class='added added-field ' data-is-non-breaking="">Focusable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Occluding = 1,</span>
}
</pre>
</div> <!-- end type SKNodeFocusBehavior -->

</div> <!-- end namespace MonoMac.SpriteKit -->
<!-- start namespace MonoMac.WebKit --> <div> 
<h2>Namespace MonoMac.WebKit</h2>
<!-- start type WKErrorCode --> <div>
<h3>Type Changed: MonoMac.WebKit.WKErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreCompileFailed = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreLookUpFailed = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreRemoveFailed = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreVersionMismatch = 9,</span>
</pre>
</div>

</div> <!-- end type WKErrorCode -->
<!-- start type WebView --> <div>
<h3>Type Changed: MonoMac.WebKit.WebView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSelectedDomRange (DomRange range, MonoMac.AppKit.NSSelectionAffinity selectionAffinity);</span>
</pre>
</div>

</div> <!-- end type WebView -->
<div> <!-- start type IWKHttpCookieStoreObserver -->
<h3>New Type MonoMac.WebKit.IWKHttpCookieStoreObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKHttpCookieStoreObserver : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IWKHttpCookieStoreObserver -->
<div> <!-- start type IWKUrlSchemeTask -->
<h3>New Type MonoMac.WebKit.IWKUrlSchemeTask</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeTask : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSUrlRequest Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFailWithError (MonoMac.Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveData (MonoMac.Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveResponse (MonoMac.Foundation.NSUrlResponse response);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeTask -->
<div> <!-- start type WKContentRuleList -->
<h3>New Type MonoMac.WebKit.WKContentRuleList</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleList : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleList (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleList (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type WKContentRuleList -->
<div> <!-- start type WKContentRuleListStore -->
<h3>New Type MonoMac.WebKit.WKContentRuleListStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleListStore : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleListStore ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleListStore (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleListStore (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleListStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static WKContentRuleListStore DefaultStore { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CompileContentRuleList (string identifier, string encodedContentRuleList, System.Action&lt;WKContentRuleList,MonoMac.Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; CompileContentRuleListAsync (string identifier, string encodedContentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public static WKContentRuleListStore FromUrl (MonoMac.Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAvailableContentRuleListIdentifiers (System.Action&lt;System.String[]&gt; callback);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; GetAvailableContentRuleListIdentifiersAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LookUpContentRuleList (string identifier, System.Action&lt;WKContentRuleList,MonoMac.Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; LookUpContentRuleListAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (string identifier, System.Action&lt;MonoMac.Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RemoveContentRuleListAsync (string identifier);</span>
}
</pre>
</div> <!-- end type WKContentRuleListStore -->
<div> <!-- start type WKHttpCookieStore -->
<h3>New Type MonoMac.WebKit.WKHttpCookieStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKHttpCookieStore : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKHttpCookieStore (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKHttpCookieStore (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKHttpCookieStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeleteCookie (MonoMac.Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DeleteCookieAsync (MonoMac.Foundation.NSHttpCookie cookie);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAllCookies (System.Action&lt;MonoMac.Foundation.NSHttpCookie[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MonoMac.Foundation.NSHttpCookie[]&gt; GetAllCookiesAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCookie (MonoMac.Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetCookieAsync (MonoMac.Foundation.NSHttpCookie cookie);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStore -->
<div> <!-- start type WKHttpCookieStoreObserver_Extensions -->
<h3>New Type MonoMac.WebKit.WKHttpCookieStoreObserver_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class WKHttpCookieStoreObserver_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CookiesDidChangeInCookieStore (IWKHttpCookieStoreObserver This, WKHttpCookieStore cookieStore);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStoreObserver_Extensions -->
<div> <!-- start type WKSnapshotConfiguration -->
<h3>New Type MonoMac.WebKit.WKSnapshotConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class WKSnapshotConfiguration : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKSnapshotConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKSnapshotConfiguration (MonoMac.Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKSnapshotConfiguration (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WKSnapshotConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Drawing.RectangleF Rect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSNumber SnapshotWidth { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type WKSnapshotConfiguration -->
<div> <!-- start type WKUrlSchemeTask_Extensions -->
<h3>New Type MonoMac.WebKit.WKUrlSchemeTask_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class WKUrlSchemeTask_Extensions {
}
</pre>
</div> <!-- end type WKUrlSchemeTask_Extensions -->

</div> <!-- end namespace MonoMac.WebKit -->
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
</script><h1 id='diff/xm/Xamarin.Mac/Xamarin.Mac.html'>Xamarin.Mac.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVCaptureVideoPreviewLayer --> <div>
<h3>Type Changed: AVFoundation.AVCaptureVideoPreviewLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVCaptureVideoPreviewLayer -->
<!-- start type AVPlayerLayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayerLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVPlayerLayer -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVSynchronizedLayer --> <div>
<h3>Type Changed: AVFoundation.AVSynchronizedLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSynchronizedLayer -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVPlayerView --> <div>
<h3>Type Changed: AVKit.AVPlayerView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UpdatesNowPlayingInfoCenter { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerView -->
<div> <!-- start type AVRoutePickerView -->
<h3>New Type AVKit.AVRoutePickerView</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerView : AppKit.NSView, AppKit.INSAccessibility, AppKit.INSAccessibilityElementProtocol, AppKit.INSAppearanceCustomization, AppKit.INSDraggingDestination, AppKit.INSTouchBarProvider, AppKit.INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVRoutePickerViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RoutePickerButtonBordered { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSColor GetRoutePickerButtonColor (AVRoutePickerViewButtonState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetRoutePickerButtonColor (AppKit.NSColor color, AVRoutePickerViewButtonState state);</span>
}
</pre>
</div> <!-- end type AVRoutePickerView -->
<div> <!-- start type AVRoutePickerViewButtonState -->
<h3>New Type AVKit.AVRoutePickerViewButtonState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVRoutePickerViewButtonState {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ActiveHighlighted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NormalHighlighted = 1,</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewButtonState -->
<div> <!-- start type AVRoutePickerViewDelegate -->
<h3>New Type AVKit.AVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerViewDelegate : Foundation.NSObject, IAVRoutePickerViewDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndPresentingRoutes (AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginPresentingRoutes (AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate -->
<div> <!-- start type AVRoutePickerViewDelegate_Extensions -->
<h3>New Type AVKit.AVRoutePickerViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVRoutePickerViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate_Extensions -->
<div> <!-- start type IAVRoutePickerViewDelegate -->
<h3>New Type AVKit.IAVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVRoutePickerViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IAVRoutePickerViewDelegate -->

</div> <!-- end namespace AVKit -->
<!-- start namespace Accounts --> <div> 
<h2>Namespace Accounts</h2>
<!-- start type ACAccountStore --> <div>
<h3>Type Changed: Accounts.ACAccountStore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAccount (ACAccount account, ACAccountStoreRemoveCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; RemoveAccountAsync (ACAccount account);</span>
</pre>
</div>

</div> <!-- end type ACAccountStore -->
<div> <!-- start type ACAccountStoreRemoveCompletionHandler -->
<h3>New Type Accounts.ACAccountStoreRemoveCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ACAccountStoreRemoveCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ACAccountStoreRemoveCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (bool success, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (bool success, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type ACAccountStoreRemoveCompletionHandler -->

</div> <!-- end namespace Accounts -->
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSAccessibilityAttributes --> <div>
<h3>Type Changed: AppKit.NSAccessibilityAttributes</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CustomTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LanguageTextAttribute { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityAttributes -->
<!-- start type NSAccessibilityElement --> <div>
<h3>Type Changed: AppKit.NSAccessibilityElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityElement -->
<!-- start type NSAccessibilityRoles --> <div>
<h3>Type Changed: AppKit.NSAccessibilityRoles</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PageRole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityRoles -->
<!-- start type NSAccessibilitySubroles --> <div>
<h3>Type Changed: AppKit.NSAccessibilitySubroles</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CollectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TabButtonSubrole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilitySubroles -->
<!-- start type NSAccessibility_Extensions --> <div>
<h3>Type Changed: AppKit.NSAccessibility_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityElement[] GetAccessibilityChildrenInNavigationOrder (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomAction[] GetAccessibilityCustomActions (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomRotor[] GetAccessibilityCustomRotors (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityChildrenInNavigationOrder (INSAccessibility This, NSAccessibilityElement[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomActions (INSAccessibility This, NSAccessibilityCustomAction[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomRotors (INSAccessibility This, NSAccessibilityCustomRotor[] value);</span>
</pre>
</div>

</div> <!-- end type NSAccessibility_Extensions -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;NSApplicationOpenUrlsEventArgs&gt; OpenUrls;</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSApplicationDelegate --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenUrls (NSApplication application, Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate -->
<!-- start type NSApplicationDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void OpenUrls (INSApplicationDelegate This, NSApplication application, Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate_Extensions -->
<!-- start type NSBezierPath --> <div>
<h3>Type Changed: AppKit.NSBezierPath</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (uint[], NSFont)' instead.")]
	public void AppendPathWithGlyphs (uint[] glyphs, NSFont font);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (CGPoint[])' instead.")]
	public void AppendPathWithPoints (CoreGraphics.CGPoint[] points);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Append (NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (CoreGraphics.CGPoint[] points);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (uint[] glyphs, NSFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AppendBezierPathWithCGGlyph (ushort glyph, NSFont font);</span>
</pre>
</div>

</div> <!-- end type NSBezierPath -->
<!-- start type NSButton --> <div>
<h3>Type Changed: AppKit.NSButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
</pre>
</div>

</div> <!-- end type NSButton -->
<!-- start type NSCell --> <div>
<h3>Type Changed: AppKit.NSCell</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCell -->
<!-- start type NSCollectionView --> <div>
<h3>Type Changed: AppKit.NSCollectionView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSCollectionViewPrefetching PrefetchDataSource { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCollectionView -->
<!-- start type NSCollectionViewTransitionLayout --> <div>
<h3>Type Changed: AppKit.NSCollectionViewTransitionLayout</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the constructor that allows you to set currentLayout and newLayout.")]
	public NSCollectionViewTransitionLayout ();</span>
</div></pre>

</div> <!-- end type NSCollectionViewTransitionLayout -->
<!-- start type NSColor --> <div>
<h3>Type Changed: AppKit.NSColor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBlueColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBrownColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGrayColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGreenColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemOrangeColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPinkColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPurpleColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemRedColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemYellowColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorType Type { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name, Foundation.NSBundle bundle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSColor GetColor (NSColorType type);</span>
</pre>
</div>

</div> <!-- end type NSColor -->
<!-- start type NSColorPickerTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSColorPickerTouchBarItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorSpace[] AllowedColorSpaces { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSColorPickerTouchBarItem -->
<!-- start type NSDocument --> <div>
<h3>Type Changed: AppKit.NSDocument</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentSharing { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (Foundation.NSCoder coder, Foundation.NSOperationQueue queue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Prepare (NSSharingServicePicker sharingServicePicker);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ShareDocument (NSSharingService sharingService, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; ShareDocumentAsync (NSSharingService sharingService);</span>
</pre>
</div>

</div> <!-- end type NSDocument -->
<!-- start type NSDocumentController --> <div>
<h3>Type Changed: AppKit.NSDocumentController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsAutomaticShareMenu { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMenuItem StandardShareMenuItem { get; }</span>
</pre>
</div>

</div> <!-- end type NSDocumentController -->
<!-- start type NSDrawer --> <div>
<h3>Type Changed: AppKit.NSDrawer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDrawer -->
<!-- start type NSFont --> <div>
<h3>Type Changed: AppKit.NSFont</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSFont FromCTFont (CoreText.CTFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAdvancement (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreGraphics.CGSize[] GetAdvancements (ushort[] glyphs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetBoundingRect (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreGraphics.CGRect[] GetBoundingRects (ushort[] glyphs);</span>
</pre>
</div>

</div> <!-- end type NSFont -->
<!-- start type NSFontDescriptor --> <div>
<h3>Type Changed: AppKit.NSFontDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RequiresFontAssetRequest { get; }</span>
</pre>
</div>

</div> <!-- end type NSFontDescriptor -->
<!-- start type NSFontSymbolicTraits --> <div>
<h3>Type Changed: AppKit.NSFontSymbolicTraits</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TraitLooseLeading = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">TraitTightLeading = 32768,</span>
</pre>
</div>

</div> <!-- end type NSFontSymbolicTraits -->
<!-- start type NSGlyphInfo --> <div>
<h3>Type Changed: AppKit.NSGlyphInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BaseString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ushort GlyphId { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGlyphInfo GetGlyphInfo (ushort glyph, NSFont font, string string);</span>
</pre>
</div>

</div> <!-- end type NSGlyphInfo -->
<!-- start type NSGroupTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSGroupTouchBarItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions EffectiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceLayoutDirection GroupUserInterfaceLayoutDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredItemWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrefersEqualWidths { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions[] PrioritizedCompressionOptions { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateAlertStyleGroupItem (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateGroupItem (string identifier, NSTouchBarItem[] items, NSUserInterfaceCompressionOptions allowedCompressionOptions);</span>
</pre>
</div>

</div> <!-- end type NSGroupTouchBarItem -->
<!-- start type NSImageName --> <div>
<h3>Type Changed: AppKit.NSImageName</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TouchBarRemoveTemplate = 116,</span>
</pre>
</div>

</div> <!-- end type NSImageName -->
<!-- start type NSLayoutAnchor`1 --> <div>
<h3>Type Changed: AppKit.NSLayoutAnchor`1</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLayoutConstraint[] ConstraintsAffectingLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAmbiguousLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSLayoutAnchor`1 -->
<!-- start type NSLayoutXAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutXAxisAnchor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension GetAnchorWithOffset (NSLayoutXAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutXAxisAnchor -->
<!-- start type NSLayoutYAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutYAxisAnchor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension GetAnchorWithOffset (NSLayoutYAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutYAxisAnchor -->
<!-- start type NSLevelIndicator --> <div>
<h3>Type Changed: AppKit.NSLevelIndicator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor CriticalFillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DrawsTieredCapacityLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Editable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor FillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLevelIndicatorPlaceholderVisibility PlaceholderVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingPlaceholderImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor WarningFillColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSLevelIndicator -->
<!-- start type NSMenu --> <div>
<h3>Type Changed: AppKit.NSMenu</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenu -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: AppKit.NSMenuItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsKeyEquivalentWhenHidden { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOpenGLLayer --> <div>
<h3>Type Changed: AppKit.NSOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSOpenGLLayer -->
<!-- start type NSPasteboard --> <div>
<h3>Type Changed: AppKit.NSPasteboard</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameDrag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameFind { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameFont { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameGeneral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameRuler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardTypeFileUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardTypeUrl { get; }</span>
</pre>
</div>

</div> <!-- end type NSPasteboard -->
<!-- start type NSPopUpButton --> <div>
<h3>Type Changed: AppKit.NSPopUpButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>

</div> <!-- end type NSPopUpButton -->
<!-- start type NSPopover --> <div>
<h3>Type Changed: AppKit.NSPopover</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSAppearanceCustomization</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'GetAppearance' and 'SetAppearance' methods instead.")]
	public virtual NSPopoverAppearance Appearance { get; set; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAppearance EffectiveAppearance { get; }</span>
</pre>
</div>

</div> <!-- end type NSPopover -->
<!-- start type NSResponder --> <div>
<h3>Type Changed: AppKit.NSResponder</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (Foundation.NSCoder coder, Foundation.NSOperationQueue queue);</span>
</pre>
</div>

</div> <!-- end type NSResponder -->
<!-- start type NSSegmentedControl --> <div>
<h3>Type Changed: AppKit.NSSegmentedControl</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSegmentDistribution SegmentDistribution { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTextAlignment GetAlignment (nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetTag (nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetToolTip (nint forSegment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAlignment (NSTextAlignment alignment, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetShowsMenuIndicator (bool showsMenuIndicator, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTag (nint tag, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetToolTip (string toolTip, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShowsMenuIndicator (nint segment);</span>
</pre>
</div>

</div> <!-- end type NSSegmentedControl -->
<!-- start type NSSliderAccessory --> <div>
<h3>Type Changed: AppKit.NSSliderAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSSliderAccessory -->
<!-- start type NSSliderTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSSliderTouchBarItem</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
</pre>
</div>

</div> <!-- end type NSSliderTouchBarItem -->
<!-- start type NSSplitViewController --> <div>
<h3>Type Changed: AppKit.NSSplitViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceValidations</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ValidateUserInterfaceItem (INSValidatedUserInterfaceItem item);</span>
</pre>
</div>

</div> <!-- end type NSSplitViewController -->
<!-- start type NSStatusBarButton --> <div>
<h3>Type Changed: AppKit.NSStatusBarButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>

</div> <!-- end type NSStatusBarButton -->
<!-- start type NSStoryboard --> <div>
<h3>Type Changed: AppKit.NSStoryboard</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSStoryboard MainStoryboard { get; }</span>
</pre>
</div>

</div> <!-- end type NSStoryboard -->
<!-- start type NSTableView --> <div>
<h3>Type Changed: AppKit.NSTableView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesAutomaticRowHeights { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTableView -->
<!-- start type NSTextList --> <div>
<h3>Type Changed: AppKit.NSTextList</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextList (NSTextListMarkerFormats format, NSTextListOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSTextList -->
<!-- start type NSToolbar --> <div>
<h3>Type Changed: AppKit.NSToolbar</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSToolbar ();</span>
</pre>
</div>

</div> <!-- end type NSToolbar -->
<!-- start type NSTouchBar --> <div>
<h3>Type Changed: AppKit.NSTouchBar</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string EscapeKeyReplacementItemIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTouchBar -->
<!-- start type NSTouchBarItemIdentifier --> <div>
<h3>Type Changed: AppKit.NSTouchBarItemIdentifier</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CandidateList = 10,</span>
</pre>
</div>

</div> <!-- end type NSTouchBarItemIdentifier -->
<!-- start type NSView --> <div>
<h3>Type Changed: AppKit.NSView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSView -->
<!-- start type NSWindow --> <div>
<h3>Type Changed: AppKit.NSWindow</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTab Tab { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTabGroup TabGroup { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the EndSheet(NSWindow,NSModalResponse) overload.")]
	public virtual void EndSheet (NSWindow sheetWindow, nint returnCode);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndSheet (NSWindow sheetWindow, NSModalResponse returnCode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToggleTabOverview (Foundation.NSObject sender);</span>
</pre>
</div>

</div> <!-- end type NSWindow -->
<!-- start type NSWorkspace --> <div>
<h3>Type Changed: AppKit.NSWorkspace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SwitchControlEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool VoiceOverEnabled { get; }</span>
</pre>
</div>

</div> <!-- end type NSWorkspace -->
<div> <!-- start type DownloadFontAssetsRequestCompletionHandler -->
<h3>New Type AppKit.DownloadFontAssetsRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate DownloadFontAssetsRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DownloadFontAssetsRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type DownloadFontAssetsRequestCompletionHandler -->
<div> <!-- start type INSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type AppKit.INSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityCustomRotorItemSearchDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type INSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type INSAccessibilityElementLoading -->
<h3>New Type AppKit.INSAccessibilityElementLoading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityElementLoading : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityElement GetAccessibilityElement (Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type INSAccessibilityElementLoading -->
<div> <!-- start type INSCollectionViewPrefetching -->
<h3>New Type AppKit.INSCollectionViewPrefetching</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCollectionViewPrefetching : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrefetchItems (NSCollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type INSCollectionViewPrefetching -->
<div> <!-- start type INSUserInterfaceCompression -->
<h3>New Type AppKit.INSUserInterfaceCompression</h3>
<pre class='added' data-is-non-breaking="">
public interface INSUserInterfaceCompression : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
}
</pre>
</div> <!-- end type INSUserInterfaceCompression -->
<div> <!-- start type NSAboutPanelOption -->
<h3>New Type AppKit.NSAboutPanelOption</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAboutPanelOption {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationIcon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Credits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Version { get; }</span>
}
</pre>
</div> <!-- end type NSAboutPanelOption -->
<div> <!-- start type NSAccessibilityAnnotationAttributeKey -->
<h3>New Type AppKit.NSAccessibilityAnnotationAttributeKey</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityAnnotationAttributeKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationLabel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationLocation { get; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationAttributeKey -->
<div> <!-- start type NSAccessibilityAnnotationPosition -->
<h3>New Type AppKit.NSAccessibilityAnnotationPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityAnnotationPosition {
	<span class='added added-field ' data-is-non-breaking="">End = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FullRange = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Start = 1,</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationPosition -->
<div> <!-- start type NSAccessibilityCustomAction -->
<h3>New Type AppKit.NSAccessibilityCustomAction</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomAction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomAction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomAction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, System.Func&lt;bool&gt; handler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, Foundation.NSObject target, ObjCRuntime.Selector selector);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;bool&gt; Handler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Selector Selector { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Target { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomAction -->
<div> <!-- start type NSAccessibilityCustomRotor -->
<h3>New Type AppKit.NSAccessibilityCustomRotor</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (NSAccessibilityCustomRotorType rotorType, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (string label, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityElementLoading ItemLoadingDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityCustomRotorItemSearchDelegate ItemSearchDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorType Type { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotor -->
<div> <!-- start type NSAccessibilityCustomRotorItemResult -->
<h3>New Type AppKit.NSAccessibilityCustomRotorItemResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorItemResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (NSAccessibilityElement targetElement);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemResult (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (Foundation.INSSecureCoding itemLoadingToken, string customLabel);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.INSSecureCoding ItemLoadingToken { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement TargetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange TargetRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemResult -->
<div> <!-- start type NSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type AppKit.NSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSAccessibilityCustomRotorItemSearchDelegate : Foundation.NSObject, INSAccessibilityCustomRotorItemSearchDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type NSAccessibilityCustomRotorSearchDirection -->
<h3>New Type AppKit.NSAccessibilityCustomRotorSearchDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorSearchDirection {
	<span class='added added-field ' data-is-non-breaking="">Next = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Previous = 0,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchDirection -->
<div> <!-- start type NSAccessibilityCustomRotorSearchParameters -->
<h3>New Type AppKit.NSAccessibilityCustomRotorSearchParameters</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorSearchParameters : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorSearchParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorSearchParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorSearchParameters (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult CurrentItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FilterString { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorSearchDirection SearchDirection { get; set; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchParameters -->
<div> <!-- start type NSAccessibilityCustomRotorType -->
<h3>New Type AppKit.NSAccessibilityCustomRotorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorType {
	<span class='added added-field ' data-is-non-breaking="">Annotation = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">BoldText = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Custom = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Heading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel1 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel2 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel3 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel4 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel5 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel6 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">ItalicText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">MisspelledWord = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Table = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">TextField = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlinedText = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">VisitedLink = 20,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorType -->
<div> <!-- start type NSAccessibilityElementLoading_Extensions -->
<h3>New Type AppKit.NSAccessibilityElementLoading_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityElementLoading_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSRange GetAccessibilityRangeInTargetElement (INSAccessibilityElementLoading This, Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type NSAccessibilityElementLoading_Extensions -->
<div> <!-- start type NSApplicationOpenUrlsEventArgs -->
<h3>New Type AppKit.NSApplicationOpenUrlsEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class NSApplicationOpenUrlsEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSApplicationOpenUrlsEventArgs (Foundation.NSUrl[] urls);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl[] Urls { get; set; }</span>
}
</pre>
</div> <!-- end type NSApplicationOpenUrlsEventArgs -->
<div> <!-- start type NSCollectionViewPrefetching_Extensions -->
<h3>New Type AppKit.NSCollectionViewPrefetching_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSCollectionViewPrefetching_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelPrefetching (INSCollectionViewPrefetching This, NSCollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type NSCollectionViewPrefetching_Extensions -->
<div> <!-- start type NSColorType -->
<h3>New Type AppKit.NSColorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSColorType {
	<span class='added added-field ' data-is-non-breaking="">Catalog = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ComponentBased = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Pattern = 1,</span>
}
</pre>
</div> <!-- end type NSColorType -->
<div> <!-- start type NSFontAssetRequest -->
<h3>New Type AppKit.NSFontAssetRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSFontAssetRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFontAssetRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFontAssetRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFontAssetRequest (NSFontDescriptor[] fontDescriptors, NSFontAssetRequestOptions options);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFontDescriptor[] DownloadedFontDescriptors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSProgress Progress { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DownloadFontAssets (DownloadFontAssetsRequestCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type NSFontAssetRequest -->
<div> <!-- start type NSFontAssetRequestOptions -->
<h3>New Type AppKit.NSFontAssetRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontAssetRequestOptions {
	<span class='added added-field ' data-is-non-breaking="">UsesStandardUI = 1,</span>
}
</pre>
</div> <!-- end type NSFontAssetRequestOptions -->
<div> <!-- start type NSFontError -->
<h3>New Type AppKit.NSFontError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFontError {
	<span class='added added-field ' data-is-non-breaking="">AssetDownloadError = 66304,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMaximum = 66335,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMinimum = 66304,</span>
}
</pre>
</div> <!-- end type NSFontError -->
<div> <!-- start type NSFontPanelModeMask -->
<h3>New Type AppKit.NSFontPanelModeMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontPanelModeMask {
	<span class='added added-field ' data-is-non-breaking="">AllEffects = 1048320,</span>
	<span class='added added-field ' data-is-non-breaking="">AllModes = 4294967295,</span>
	<span class='added added-field ' data-is-non-breaking="">Collection = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">DocumentColorEffect = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">Face = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ShadowEffect = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">Size = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">StandardModes = 65535,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikethroughEffect = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">TextColorEffect = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlineEffect = 256,</span>
}
</pre>
</div> <!-- end type NSFontPanelModeMask -->
<div> <!-- start type NSLevelIndicatorPlaceholderVisibility -->
<h3>New Type AppKit.NSLevelIndicatorPlaceholderVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSLevelIndicatorPlaceholderVisibility {
	<span class='added added-field ' data-is-non-breaking="">Always = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WhileEditing = 2,</span>
}
</pre>
</div> <!-- end type NSLevelIndicatorPlaceholderVisibility -->
<div> <!-- start type NSObject_NSFontPanelValidationAdditions -->
<h3>New Type AppKit.NSObject_NSFontPanelValidationAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSObject_NSFontPanelValidationAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFontPanelModeMask GetValidModes (Foundation.NSObject This, NSFontPanel fontPanel);</span>
}
</pre>
</div> <!-- end type NSObject_NSFontPanelValidationAdditions -->
<div> <!-- start type NSRulerViewUnits -->
<h3>New Type AppKit.NSRulerViewUnits</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSRulerViewUnits {
	<span class='added added-field ' data-is-non-breaking="">Centimeters = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inches = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Picas = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Points = 2,</span>
}
</pre>
</div> <!-- end type NSRulerViewUnits -->
<div> <!-- start type NSRulerViewUnitsExtensions -->
<h3>New Type AppKit.NSRulerViewUnitsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSRulerViewUnitsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSRulerViewUnits self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSRulerViewUnits GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSRulerViewUnitsExtensions -->
<div> <!-- start type NSSegmentDistribution -->
<h3>New Type AppKit.NSSegmentDistribution</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSSegmentDistribution {
	<span class='added added-field ' data-is-non-breaking="">Fill = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FillEqually = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FillProportionally = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Fit = 0,</span>
}
</pre>
</div> <!-- end type NSSegmentDistribution -->
<div> <!-- start type NSTextListMarkerFormats -->
<h3>New Type AppKit.NSTextListMarkerFormats</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTextListMarkerFormats {
	<span class='added added-field ' data-is-non-breaking="">Box = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Check = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Decimal = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Disc = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Hyphen = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseAlpha = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseHexadecimal = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseLatin = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseRoman = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Octal = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseAlpha = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseHexadecimal = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseLatin = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseRoman = 15,</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormats -->
<div> <!-- start type NSTextListMarkerFormatsExtensions -->
<h3>New Type AppKit.NSTextListMarkerFormatsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTextListMarkerFormatsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSTextListMarkerFormats self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextListMarkerFormats GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormatsExtensions -->
<div> <!-- start type NSUserInterfaceCompressionOptions -->
<h3>New Type AppKit.NSUserInterfaceCompressionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class NSUserInterfaceCompressionOptions : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserInterfaceCompressionOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (Foundation.NSSet&lt;NSUserInterfaceCompressionOptions&gt; options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserInterfaceCompressionOptions (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions BreakEqualWidthsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Empty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideImagesOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideTextOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions ReduceMetricsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions StandardOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByAdding (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByRemoving (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Intersects (NSUserInterfaceCompressionOptions options);</span>
}
</pre>
</div> <!-- end type NSUserInterfaceCompressionOptions -->
<div> <!-- start type NSWindowTab -->
<h3>New Type AppKit.NSWindowTab</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTab : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTab ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTab (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTab (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView AccessoryView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ToolTip { get; set; }</span>
}
</pre>
</div> <!-- end type NSWindowTab -->
<div> <!-- start type NSWindowTabGroup -->
<h3>New Type AppKit.NSWindowTabGroup</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTabGroup : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTabGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTabGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool OverviewVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow SelectedWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TabBarVisible { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow[] Windows { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (NSWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Insert (NSWindow window, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Remove (NSWindow window);</span>
}
</pre>
</div> <!-- end type NSWindowTabGroup -->

</div> <!-- end namespace AppKit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKFetchRecordZoneChangesOptions --> <div>
<h3>Type Changed: CloudKit.CKFetchRecordZoneChangesOptions</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type CKFetchRecordZoneChangesOptions -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNErrorCode --> <div>
<h3>Type Changed: Contacts.CNErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierDoesNotExist = 601,</span>
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierInvalid = 600,</span>
</pre>
</div>

</div> <!-- end type CNErrorCode -->
<!-- start type CNLabelContactRelationKey --> <div>
<h3>Type Changed: Contacts.CNLabelContactRelationKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Daughter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Son { get; }</span>
</pre>
</div>

</div> <!-- end type CNLabelContactRelationKey -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CAAnimationGroup --> <div>
<h3>Type Changed: CoreAnimation.CAAnimationGroup</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimationGroup -->
<!-- start type CABasicAnimation --> <div>
<h3>Type Changed: CoreAnimation.CABasicAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CABasicAnimation -->
<!-- start type CAConstraint --> <div>
<h3>Type Changed: CoreAnimation.CAConstraint</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAConstraint -->
<!-- start type CAEmitterBehavior --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterBehavior</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterBehavior -->
<!-- start type CAEmitterCell --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterCell</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterCell -->
<!-- start type CAEmitterLayer --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterLayer -->
<!-- start type CAGradientLayer --> <div>
<h3>Type Changed: CoreAnimation.CAGradientLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAGradientLayer -->
<!-- start type CAKeyFrameAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAKeyFrameAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAKeyFrameAnimation -->
<!-- start type CALayer --> <div>
<h3>Type Changed: CoreAnimation.CALayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CALayer -->
<!-- start type CAMediaTimingFunction --> <div>
<h3>Type Changed: CoreAnimation.CAMediaTimingFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAMediaTimingFunction -->
<!-- start type CAMetalLayer --> <div>
<h3>Type Changed: CoreAnimation.CAMetalLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->
<!-- start type CAOpenGLLayer --> <div>
<h3>Type Changed: CoreAnimation.CAOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAOpenGLLayer -->
<!-- start type CAPropertyAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAPropertyAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAPropertyAnimation -->
<!-- start type CAReplicatorLayer --> <div>
<h3>Type Changed: CoreAnimation.CAReplicatorLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAReplicatorLayer -->
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: CoreAnimation.CAScrollLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<!-- start type CAShapeLayer --> <div>
<h3>Type Changed: CoreAnimation.CAShapeLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAShapeLayer -->
<!-- start type CASpringAnimation --> <div>
<h3>Type Changed: CoreAnimation.CASpringAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CASpringAnimation -->
<!-- start type CATextLayer --> <div>
<h3>Type Changed: CoreAnimation.CATextLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATextLayer -->
<!-- start type CATiledLayer --> <div>
<h3>Type Changed: CoreAnimation.CATiledLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATiledLayer -->
<!-- start type CATransformLayer --> <div>
<h3>Type Changed: CoreAnimation.CATransformLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransformLayer -->
<!-- start type CATransition --> <div>
<h3>Type Changed: CoreAnimation.CATransition</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransition -->
<!-- start type CAValueFunction --> <div>
<h3>Type Changed: CoreAnimation.CAValueFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAValueFunction -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreAudioKit --> <div> 
<h2>Namespace CoreAudioKit</h2>
<div> <!-- start type AUAudioUnitViewConfiguration -->
<h3>New Type CoreAudioKit.AUAudioUnitViewConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class AUAudioUnitViewConfiguration : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AUAudioUnitViewConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AUAudioUnitViewConfiguration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration (nfloat width, nfloat height, bool hostHasController);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HostHasController { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type AUAudioUnitViewConfiguration -->
<div> <!-- start type AUAudioUnitViewControllerExtensions -->
<h3>New Type CoreAudioKit.AUAudioUnitViewControllerExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AUAudioUnitViewControllerExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSIndexSet GetSupportedViewConfigurations (AudioUnit.AUAudioUnit This, AUAudioUnitViewConfiguration[] availableViewConfigurations);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SelectViewConfiguration (AudioUnit.AUAudioUnit This, AUAudioUnitViewConfiguration viewConfiguration);</span>
}
</pre>
</div> <!-- end type AUAudioUnitViewControllerExtensions -->

</div> <!-- end namespace CoreAudioKit -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type MigrationErrorType --> <div>
<h3>Type Changed: CoreData.MigrationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HistoryTokenExpired = 134301,</span>
</pre>
</div>

</div> <!-- end type MigrationErrorType -->
<!-- start type NSAttributeType --> <div>
<h3>Type Changed: CoreData.NSAttributeType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Uri = 1200,</span>
	<span class='added added-field ' data-is-non-breaking="">Uuid = 1100,</span>
</pre>
</div>

</div> <!-- end type NSAttributeType -->
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: CoreData.NSEntityDescription</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression CoreSpotlightDisplayNameExpression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription[] Indexes { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionAuthor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CoreSpotlightExporter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HistoryTrackingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UbiquitousContainerIdentifierKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator -->
<!-- start type NSQueryGenerationToken --> <div>
<h3>Type Changed: CoreData.NSQueryGenerationToken</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSQueryGenerationToken (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type NSQueryGenerationToken -->
<!-- start type ValidationErrorType --> <div>
<h3>Type Changed: CoreData.ValidationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidUri = 1690,</span>
</pre>
</div>

</div> <!-- end type ValidationErrorType -->
<div> <!-- start type NSFetchIndexDescription -->
<h3>New Type CoreData.NSFetchIndexDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (string name, NSFetchIndexElementDescription[] elements);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementDescription[] Elements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSEntityDescription Entity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate PartialIndexPredicate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexDescription -->
<div> <!-- start type NSFetchIndexElementDescription -->
<h3>New Type CoreData.NSFetchIndexElementDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexElementDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (NSPropertyDescription property, NSFetchIndexElementType collationType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementType CollationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription IndexDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAscending { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPropertyDescription Property { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PropertyName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementDescription -->
<div> <!-- start type NSFetchIndexElementType -->
<h3>New Type CoreData.NSFetchIndexElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFetchIndexElementType {
	<span class='added added-field ' data-is-non-breaking="">Binary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RTree = 1,</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementType -->
<div> <!-- start type NSPersistentHistoryChange -->
<h3>New Type CoreData.NSPersistentHistoryChange</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryChange : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual long ChangeId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChangeType ChangeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectID ChangedObjectId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary Tombstone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryTransaction Transaction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSPropertyDescription&gt; UpdatedProperties { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChange -->
<div> <!-- start type NSPersistentHistoryChangeRequest -->
<h3>New Type CoreData.NSPersistentHistoryChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryChangeRequest : CoreData.NSPersistentStoreRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (Foundation.NSDate date);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeRequest -->
<div> <!-- start type NSPersistentHistoryChangeType -->
<h3>New Type CoreData.NSPersistentHistoryChangeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryChangeType {
	<span class='added added-field ' data-is-non-breaking="">Delete = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Update = 1,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeType -->
<div> <!-- start type NSPersistentHistoryResult -->
<h3>New Type CoreData.NSPersistentHistoryResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryResult : CoreData.NSPersistentStoreResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Result { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; }</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResult -->
<div> <!-- start type NSPersistentHistoryResultType -->
<h3>New Type CoreData.NSPersistentHistoryResultType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryResultType {
	<span class='added added-field ' data-is-non-breaking="">ChangesOnly = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectIds = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusOnly = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsAndChanges = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsOnly = 3,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResultType -->
<div> <!-- start type NSPersistentHistoryToken -->
<h3>New Type CoreData.NSPersistentHistoryToken</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryToken : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryToken -->
<div> <!-- start type NSPersistentHistoryTransaction -->
<h3>New Type CoreData.NSPersistentHistoryTransaction</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryTransaction : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BundleId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChange[] Changes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContextName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNotification ObjectIdNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProcessId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StoreId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Timestamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long TransactionNumber { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryTransaction -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIImageAccumulator --> <div>
<h3>Type Changed: CoreImage.CIImageAccumulator</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CIImageAccumulator ();</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect extent, int format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect extent, int format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIImageAccumulator -->
<!-- start type CIQRCodeFeature --> <div>
<h3>Type Changed: CoreImage.CIQRCodeFeature</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeFeature (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type CIQRCodeFeature -->
<div> <!-- start type CIAreaMinMaxRed -->
<h3>New Type CoreImage.CIAreaMinMaxRed</h3>
<pre class='added' data-is-non-breaking="">
public class CIAreaMinMaxRed : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAreaMinMaxRed -->
<div> <!-- start type CIAttributedTextImageGenerator -->
<h3>New Type CoreImage.CIAttributedTextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIAttributedTextImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAttributedTextImageGenerator -->
<div> <!-- start type CIBarcodeGenerator -->
<h3>New Type CoreImage.CIBarcodeGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIBarcodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBarcodeGenerator -->
<div> <!-- start type CIBicubicScaleTransform -->
<h3>New Type CoreImage.CIBicubicScaleTransform</h3>
<pre class='added' data-is-non-breaking="">
public class CIBicubicScaleTransform : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBicubicScaleTransform -->
<div> <!-- start type CIBokehBlur -->
<h3>New Type CoreImage.CIBokehBlur</h3>
<pre class='added' data-is-non-breaking="">
public class CIBokehBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBokehBlur -->
<div> <!-- start type CIColorCubesMixedWithMask -->
<h3>New Type CoreImage.CIColorCubesMixedWithMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCubesMixedWithMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCubesMixedWithMask -->
<div> <!-- start type CIColorCurves -->
<h3>New Type CoreImage.CIColorCurves</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCurves : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCurves -->
<div> <!-- start type CIDepthBlurEffect -->
<h3>New Type CoreImage.CIDepthBlurEffect</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthBlurEffect : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthBlurEffect -->
<div> <!-- start type CIDepthToDisparity -->
<h3>New Type CoreImage.CIDepthToDisparity</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthToDisparity : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthToDisparity -->
<div> <!-- start type CIDisparityToDepth -->
<h3>New Type CoreImage.CIDisparityToDepth</h3>
<pre class='added' data-is-non-breaking="">
public class CIDisparityToDepth : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CILabDeltaE -->
<div> <!-- start type CIMorphologyGradient -->
<h3>New Type CoreImage.CIMorphologyGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyGradient : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyGradient -->
<div> <!-- start type CIMorphologyMaximum -->
<h3>New Type CoreImage.CIMorphologyMaximum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMaximum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMaximum -->
<div> <!-- start type CIMorphologyMinimum -->
<h3>New Type CoreImage.CIMorphologyMinimum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMinimum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMinimum -->
<div> <!-- start type CITextImageGenerator -->
<h3>New Type CoreImage.CITextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CITextImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CITextImageGenerator -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLGeocoder --> <div>
<h3>Type Changed: CoreLocation.CLGeocoder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLRegion region, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->
<!-- start type CLPlacemark --> <div>
<h3>Type Changed: CoreLocation.CLPlacemark</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Contacts.CNPostalAddress PostalAddress { get; }</span>
</pre>
</div>

</div> <!-- end type CLPlacemark -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
<!-- start type CMAttachmentBearer --> <div>
<h3>Type Changed: CoreMedia.CMAttachmentBearer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (ICMAttachmentBearer target, CMAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CMAttachmentBearer -->

</div> <!-- end namespace CoreMedia -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVBuffer --> <div>
<h3>Type Changed: CoreVideo.CVBuffer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (CVAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CVBuffer -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace EventKit --> <div> 
<h2>Namespace EventKit</h2>
<!-- start type EKAlarm --> <div>
<h3>Type Changed: EventKit.EKAlarm</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the static methods FromDate or FromTimeInterval to create alarms")]
	public EKAlarm ();</span>
</div></pre>

</div> <!-- end type EKAlarm -->
<!-- start type EKEventStore --> <div>
<h3>Type Changed: EventKit.EKEventStore</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public EKEventStore (EKSource[] sources);</span>
</pre>
</div>

</div> <!-- end type EKEventStore -->

</div> <!-- end namespace EventKit -->
<!-- start namespace FinderSync --> <div> 
<h2>Namespace FinderSync</h2>
<!-- start type FIFinderSync --> <div>
<h3>Type Changed: FinderSync.FIFinderSync</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetExportedObject (Foundation.NSFileProviderMessageInterface messageInterface, Foundation.NSUrl itemUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetValues (string[] attributes, Foundation.NSUrl itemUrl, GetValuesCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt;&gt; GetValuesAsync (string[] attributes, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] SupportedServiceNames (Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSync -->
<!-- start type FIFinderSyncController --> <div>
<h3>Type Changed: FinderSync.FIFinderSyncController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSDate GetLastUsedDate (Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetTagData (Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLastUsedDate (Foundation.NSDate lastUsedDate, Foundation.NSUrl itemUrl, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetLastUsedDateAsync (Foundation.NSDate lastUsedDate, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTagData (Foundation.NSData tagData, Foundation.NSUrl itemUrl, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetTagDataAsync (Foundation.NSData tagData, Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSyncController -->
<!-- start type FIFinderSyncProtocol_Extensions --> <div>
<h3>Type Changed: FinderSync.FIFinderSyncProtocol_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject GetExportedObject (IFIFinderSyncProtocol This, Foundation.NSFileProviderMessageInterface messageInterface, Foundation.NSUrl itemUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetValues (IFIFinderSyncProtocol This, string[] attributes, Foundation.NSUrl itemUrl, GetValuesCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt;&gt; GetValuesAsync (IFIFinderSyncProtocol This, string[] attributes, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] SupportedServiceNames (IFIFinderSyncProtocol This, Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSyncProtocol_Extensions -->
<div> <!-- start type GetValuesCompletionHandler -->
<h3>New Type FinderSync.GetValuesCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate GetValuesCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GetValuesCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; values, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; values, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type GetValuesCompletionHandler -->

</div> <!-- end namespace FinderSync -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSActivityOptions --> <div>
<h3>Type Changed: Foundation.NSActivityOptions</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	IdleDisplaySleepDisabled = <span class='removed removed-inline removed-breaking-inline'>256</span> <span class='added '>1099511627776</span>
</div></pre>

</div> <!-- end type NSActivityOptions -->
<!-- start type NSDimension --> <div>
<h3>Type Changed: Foundation.NSDimension</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">[Obsolete ("Not intended to be directly instantiated, this is an abstract class.")]
	public NSDimension ();</span>
</pre>
</div>

</div> <!-- end type NSDimension -->
<!-- start type NSFileManager --> <div>
<h3>Type Changed: Foundation.NSFileManager</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnmountVolume (NSUrl url, NSFileManagerUnmountOptions mask, System.Action&lt;NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UnmountVolumeAsync (NSUrl url, NSFileManagerUnmountOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSFileManager -->
<!-- start type NSUnit --> <div>
<h3>Type Changed: Foundation.NSUnit</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string)")]
	public NSUnit ();</span>
</div></pre>

</div> <!-- end type NSUnit -->
<!-- start type NSUnitAcceleration --> <div>
<h3>Type Changed: Foundation.NSUnitAcceleration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAcceleration ();</span>
</div></pre>

</div> <!-- end type NSUnitAcceleration -->
<!-- start type NSUnitAngle --> <div>
<h3>Type Changed: Foundation.NSUnitAngle</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAngle ();</span>
</div></pre>

</div> <!-- end type NSUnitAngle -->
<!-- start type NSUnitArea --> <div>
<h3>Type Changed: Foundation.NSUnitArea</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitArea ();</span>
</div></pre>

</div> <!-- end type NSUnitArea -->
<!-- start type NSUnitConcentrationMass --> <div>
<h3>Type Changed: Foundation.NSUnitConcentrationMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitConcentrationMass ();</span>
</div></pre>

</div> <!-- end type NSUnitConcentrationMass -->
<!-- start type NSUnitDispersion --> <div>
<h3>Type Changed: Foundation.NSUnitDispersion</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDispersion ();</span>
</div></pre>

</div> <!-- end type NSUnitDispersion -->
<!-- start type NSUnitDuration --> <div>
<h3>Type Changed: Foundation.NSUnitDuration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDuration ();</span>
</div></pre>

</div> <!-- end type NSUnitDuration -->
<!-- start type NSUnitElectricCharge --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCharge</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCharge ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCharge -->
<!-- start type NSUnitElectricCurrent --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCurrent</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCurrent ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCurrent -->
<!-- start type NSUnitElectricPotentialDifference --> <div>
<h3>Type Changed: Foundation.NSUnitElectricPotentialDifference</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricPotentialDifference ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricPotentialDifference -->
<!-- start type NSUnitElectricResistance --> <div>
<h3>Type Changed: Foundation.NSUnitElectricResistance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricResistance ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricResistance -->
<!-- start type NSUnitEnergy --> <div>
<h3>Type Changed: Foundation.NSUnitEnergy</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitEnergy ();</span>
</div></pre>

</div> <!-- end type NSUnitEnergy -->
<!-- start type NSUnitFrequency --> <div>
<h3>Type Changed: Foundation.NSUnitFrequency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFrequency ();</span>
</div></pre>

</div> <!-- end type NSUnitFrequency -->
<!-- start type NSUnitFuelEfficiency --> <div>
<h3>Type Changed: Foundation.NSUnitFuelEfficiency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFuelEfficiency ();</span>
</div></pre>

</div> <!-- end type NSUnitFuelEfficiency -->
<!-- start type NSUnitIlluminance --> <div>
<h3>Type Changed: Foundation.NSUnitIlluminance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitIlluminance ();</span>
</div></pre>

</div> <!-- end type NSUnitIlluminance -->
<!-- start type NSUnitLength --> <div>
<h3>Type Changed: Foundation.NSUnitLength</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitLength ();</span>
</div></pre>

</div> <!-- end type NSUnitLength -->
<!-- start type NSUnitMass --> <div>
<h3>Type Changed: Foundation.NSUnitMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitMass ();</span>
</div></pre>

</div> <!-- end type NSUnitMass -->
<!-- start type NSUnitPower --> <div>
<h3>Type Changed: Foundation.NSUnitPower</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPower ();</span>
</div></pre>

</div> <!-- end type NSUnitPower -->
<!-- start type NSUnitPressure --> <div>
<h3>Type Changed: Foundation.NSUnitPressure</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPressure ();</span>
</div></pre>

</div> <!-- end type NSUnitPressure -->
<!-- start type NSUnitSpeed --> <div>
<h3>Type Changed: Foundation.NSUnitSpeed</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitSpeed ();</span>
</div></pre>

</div> <!-- end type NSUnitSpeed -->
<!-- start type NSUnitVolume --> <div>
<h3>Type Changed: Foundation.NSUnitVolume</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitVolume ();</span>
</div></pre>

</div> <!-- end type NSUnitVolume -->
<!-- start type ProtocolAttribute --> <div>
<h3>Type Changed: Foundation.ProtocolAttribute</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string FormalSince { get; set; }</span>
</pre>
</div>

</div> <!-- end type ProtocolAttribute -->
<div> <!-- start type INSItemProviderReading -->
<h3>New Type Foundation.INSItemProviderReading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSItemProviderReading : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSItemProviderReading -->
<div> <!-- start type NSFileProviderMessageInterface -->
<h3>New Type Foundation.NSFileProviderMessageInterface</h3>
<pre class='added' data-is-non-breaking="">
public class NSFileProviderMessageInterface : Foundation.NSObject, INSCoding, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderMessageInterface (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderMessageInterface (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFileProviderMessageInterface -->
<div> <!-- start type NotImplementedAttribute -->
<h3>New Type Foundation.NotImplementedAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class NotImplementedAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NotImplementedAttribute ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NotImplementedAttribute (string message);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; set; }</span>
}
</pre>
</div> <!-- end type NotImplementedAttribute -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCMotion --> <div>
<h3>Type Changed: GameController.GCMotion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAttitudeAndRotationRate { get; }</span>
</pre>
</div>

</div> <!-- end type GCMotion -->

</div> <!-- end namespace GameController -->
<!-- start namespace LocalAuthentication --> <div> 
<h2>Namespace LocalAuthentication</h2>
<!-- start type LAContext --> <div>
<h3>Type Changed: LocalAuthentication.LAContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InteractionNotAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedReason { get; set; }</span>
</pre>
</div>

</div> <!-- end type LAContext -->
<!-- start type LAStatus --> <div>
<h3>Type Changed: LocalAuthentication.LAStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NotInteractive = -1004,</span>
</pre>
</div>

</div> <!-- end type LAStatus -->

</div> <!-- end namespace LocalAuthentication -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKAnnotationView --> <div>
<h3>Type Changed: MapKit.MKAnnotationView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationView ClusterAnnotationView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ClusteringIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationViewCollisionMode CollisionMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float DisplayPriority { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareForDisplay ();</span>
</pre>
</div>

</div> <!-- end type MKAnnotationView -->
<!-- start type MKMapItem --> <div>
<h3>Type Changed: MapKit.MKMapItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MKMapItem -->
<!-- start type MKMapType --> <div>
<h3>Type Changed: MapKit.MKMapType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MutedStandard = 5,</span>
</pre>
</div>

</div> <!-- end type MKMapType -->
<!-- start type MKMapView --> <div>
<h3>Type Changed: MapKit.MKMapView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MKCreateClusterAnnotation CreateClusterAnnotation { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKAnnotationView DequeueReusableAnnotation (string identifier, IMKAnnotation annotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Register (ObjCRuntime.Class viewClass, string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Register (System.Type viewType, string identifier);</span>
</pre>
</div>

</div> <!-- end type MKMapView -->
<!-- start type MKMapViewDelegate --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation CreateClusterAnnotation (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate -->
<!-- start type MKMapViewDelegate_Extensions --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MKClusterAnnotation CreateClusterAnnotation (IMKMapViewDelegate This, MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate_Extensions -->
<!-- start type MKPlacemark --> <div>
<h3>Type Changed: MapKit.MKPlacemark</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate, Contacts.CNPostalAddress postalAddress);</span>
</pre>
</div>

</div> <!-- end type MKPlacemark -->
<div> <!-- start type MKAnnotationViewCollisionMode -->
<h3>New Type MapKit.MKAnnotationViewCollisionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKAnnotationViewCollisionMode {
	<span class='added added-field ' data-is-non-breaking="">Circle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Rectangle = 0,</span>
}
</pre>
</div> <!-- end type MKAnnotationViewCollisionMode -->
<div> <!-- start type MKClusterAnnotation -->
<h3>New Type MapKit.MKClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public class MKClusterAnnotation : Foundation.NSObject, Foundation.INSObjectProtocol, IMKAnnotation, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKClusterAnnotation (IMKAnnotation[] memberAnnotations);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMKAnnotation[] MemberAnnotations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Subtitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCoordinate (CoreLocation.CLLocationCoordinate2D value);</span>
}
</pre>
</div> <!-- end type MKClusterAnnotation -->
<div> <!-- start type MKCreateClusterAnnotation -->
<h3>New Type MapKit.MKCreateClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MKCreateClusterAnnotation : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKCreateClusterAnnotation (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, IMKAnnotation[] memberAnnotations, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation Invoke (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
}
</pre>
</div> <!-- end type MKCreateClusterAnnotation -->
<div> <!-- start type MKFeatureDisplayPriority -->
<h3>New Type MapKit.MKFeatureDisplayPriority</h3>
<pre class='added' data-is-non-breaking="">
public static class MKFeatureDisplayPriority {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultHigh;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultLow;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float Required;</span>
}
</pre>
</div> <!-- end type MKFeatureDisplayPriority -->
<div> <!-- start type MKFeatureVisibility -->
<h3>New Type MapKit.MKFeatureVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKFeatureVisibility {
	<span class='added added-field ' data-is-non-breaking="">Adaptive = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hidden = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Visible = 2,</span>
}
</pre>
</div> <!-- end type MKFeatureVisibility -->
<div> <!-- start type MKMapViewDefault -->
<h3>New Type MapKit.MKMapViewDefault</h3>
<pre class='added' data-is-non-breaking="">
public static class MKMapViewDefault {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationViewReuseIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ClusterAnnotationViewReuseIdentifier { get; }</span>
}
</pre>
</div> <!-- end type MKMapViewDefault -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaLibrary --> <div> 
<h2>Namespace MediaLibrary</h2>
<!-- start type MediaLibraryTypeIdentifierKey --> <div>
<h3>Type Changed: MediaLibrary.MediaLibraryTypeIdentifierKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosAnimatedGroupTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosLivePhotosGroupTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosLongExposureGroupTypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MediaLibraryTypeIdentifierKey -->

</div> <!-- end namespace MediaLibrary -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.12"</span> <span class='added '>"10.13"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"3.4.0"</span> <span class='added '>"3.99.1"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VisionLibrary = "/System/Library/Frameworks/Vision.framework/Vision";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetUInt32 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetUInt64 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNFloat (IntPtr handle, string symbol, nfloat value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNInt (IntPtr handle, string symbol, nint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNUInt (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt32 (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt64 (IntPtr handle, string symbol, long value);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHContentEditingInput --> <div>
<h3>Type Changed: Photos.PHContentEditingInput</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage DisplaySizeImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
</pre>
</div>

</div> <!-- end type PHContentEditingInput -->
<!-- start type PHLivePhotoEditingContext --> <div>
<h3>Type Changed: Photos.PHLivePhotoEditingContext</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, PHLivePhotoEditingOption options, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output, PHLivePhotoEditingOption options);</span>
</pre>
</div>

</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type IPHContentEditingController -->
<h3>New Type Photos.IPHContentEditingController</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHContentEditingController : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldShowCancelConfirmation { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanHandleAdjustmentData (PHAdjustmentData adjustmentData);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelContentEditing ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishContentEditing (System.Action&lt;PHContentEditingOutput&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartContentEditing (PHContentEditingInput contentEditingInput, AppKit.NSImage placeholderImage);</span>
}
</pre>
</div> <!-- end type IPHContentEditingController -->
<div> <!-- start type IPHPhotoLibraryChangeObserver -->
<h3>New Type Photos.IPHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHPhotoLibraryChangeObserver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type IPHPhotoLibraryChangeObserver -->
<div> <!-- start type IPHProjectExtensionController -->
<h3>New Type Photos.IPHProjectExtensionController</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHProjectExtensionController : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginProject (PHProjectExtensionContext extensionContext, PHProjectInfo projectInfo, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishProject (System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ResumeProject (PHProjectExtensionContext extensionContext, System.Action&lt;Foundation.NSError&gt; completion);</span>
}
</pre>
</div> <!-- end type IPHProjectExtensionController -->
<div> <!-- start type PHAsset -->
<h3>New Type Photos.PHAsset</h3>
<pre class='added' data-is-non-breaking="">
public class PHAsset : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAsset ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string BurstIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetBurstSelectionType BurstSelectionTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Favorite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LocalIdentifierNotFound { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaSubtype MediaSubtypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaType MediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ModificationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RepresentsBurst { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType SourceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SyncFailureHidden { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHAssetEditOperation editOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetMediaType mediaType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (string burstIdentifier, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetsUsingLocalIdentifiers (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchKeyAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHAsset -->
<div> <!-- start type PHAssetCollection -->
<h3>New Type Photos.PHAssetCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetCollection : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetCollection ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation ApproximateLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionSubtype AssetCollectionSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionType AssetCollectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint EstimatedAssetCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (Foundation.NSUrl[] assetGroupUrls, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAsset asset, PHAssetCollectionType type, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAssetCollectionType type, PHAssetCollectionSubtype subtype, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHCollectionList momentList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHAsset[] assets, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHFetchResult fetchResult, string title);</span>
}
</pre>
</div> <!-- end type PHAssetCollection -->
<div> <!-- start type PHAssetImageProgressHandler -->
<h3>New Type Photos.PHAssetImageProgressHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHAssetImageProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetImageProgressHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (double progress, Foundation.NSError error, bool stop, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (double progress, Foundation.NSError error, bool stop, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHAssetImageProgressHandler -->
<div> <!-- start type PHAssetPlaybackStyle -->
<h3>New Type Photos.PHAssetPlaybackStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetPlaybackStyle {
	<span class='added added-field ' data-is-non-breaking="">Image = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageAnimated = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LivePhoto = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoLooping = 5,</span>
}
</pre>
</div> <!-- end type PHAssetPlaybackStyle -->
<div> <!-- start type PHAuthorizationStatus -->
<h3>New Type Photos.PHAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type PHAuthorizationStatus -->
<div> <!-- start type PHChange -->
<h3>New Type Photos.PHChange</h3>
<pre class='added' data-is-non-breaking="">
public class PHChange : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual PHFetchResultChangeDetails GetFetchResultChangeDetails (PHFetchResult obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PHObjectChangeDetails GetObjectChangeDetails (PHObject obj);</span>
}
</pre>
</div> <!-- end type PHChange -->
<div> <!-- start type PHChangeDetailEnumerator -->
<h3>New Type Photos.PHChangeDetailEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHChangeDetailEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChangeDetailEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (uint fromIndex, uint toIndex, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (uint fromIndex, uint toIndex);</span>
}
</pre>
</div> <!-- end type PHChangeDetailEnumerator -->
<div> <!-- start type PHCloudIdentifier -->
<h3>New Type Photos.PHCloudIdentifier</h3>
<pre class='added' data-is-non-breaking="">
public class PHCloudIdentifier : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCloudIdentifier (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCloudIdentifier (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier (string stringValue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHCloudIdentifier NotFoundIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHCloudIdentifier -->
<div> <!-- start type PHCollection -->
<h3>New Type Photos.PHCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollection : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainAssets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainCollections { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHCollectionEditOperation anOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollections (PHCollectionList collectionList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchTopLevelUserCollections (PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollection -->
<div> <!-- start type PHCollectionList -->
<h3>New Type Photos.PHCollectionList</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollectionList : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCollectionList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListSubtype CollectionListSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListType CollectionListType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHAssetCollection[] collections, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHFetchResult fetchResult, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollection collection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollectionListType type, PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHAssetCollection moment, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollectionList -->
<div> <!-- start type PHFetchOptions -->
<h3>New Type Photos.PHFetchOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FetchLimit { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeAllBurstAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType IncludeAssetSourceTypes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeHiddenAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate Predicate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSortDescriptor[] SortDescriptors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsIncrementalChangeDetails { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHFetchOptions -->
<div> <!-- start type PHFetchResult -->
<h3>New Type Photos.PHFetchResult</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResult : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject LastObject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject firstObject { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint CountOfAssetsWithMediaType (PHAssetMediaType mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSIndexSet idx, Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id, Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAt (nint index);</span>
}
</pre>
</div> <!-- end type PHFetchResult -->
<div> <!-- start type PHFetchResultChangeDetails -->
<h3>New Type Photos.PHFetchResultChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResultChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet ChangedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] ChangedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasIncrementalChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasMoves { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet InsertedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] InsertedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet RemovedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] RemovedObjects { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResultChangeDetails ChangeDetails (PHFetchResult fromResult, PHFetchResult toResult, PHObject[] changedObjects);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateMoves (PHChangeDetailEnumerator handler);</span>
}
</pre>
</div> <!-- end type PHFetchResultChangeDetails -->
<div> <!-- start type PHFetchResultEnumerator -->
<h3>New Type Photos.PHFetchResultEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHFetchResultEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSObject element, uint elementIndex, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSObject element, uint elementIndex, bool stop);</span>
}
</pre>
</div> <!-- end type PHFetchResultEnumerator -->
<div> <!-- start type PHImageDataHandler -->
<h3>New Type Photos.PHImageDataHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageDataHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData data, Foundation.NSString dataUti, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData data, Foundation.NSString dataUti, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageDataHandler -->
<div> <!-- start type PHImageKeys -->
<h3>New Type Photos.PHImageKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PHImageKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Cancelled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsDegraded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsInCloud { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultRequestID { get; }</span>
}
</pre>
</div> <!-- end type PHImageKeys -->
<div> <!-- start type PHImageManager -->
<h3>New Type Photos.PHImageManager</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHImageManager DefaultManager { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGSize MaximumSize { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelImageRequest (int requestID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageData (PHAsset asset, PHImageRequestOptions options, PHImageDataHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageForAsset (PHAsset asset, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHImageRequestOptions options, PHImageResultHandler resultHandler);</span>
}
</pre>
</div> <!-- end type PHImageManager -->
<div> <!-- start type PHImageRequestOptions -->
<h3>New Type Photos.PHImageRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageRequestOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect NormalizedCropRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsResizeMode ResizeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Synchronous { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsVersion Version { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHImageRequestOptions -->
<div> <!-- start type PHImageRequestOptionsDeliveryMode -->
<h3>New Type Photos.PHImageRequestOptionsDeliveryMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsDeliveryMode {
	<span class='added added-field ' data-is-non-breaking="">FastFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HighQualityFormat = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Opportunistic = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsDeliveryMode -->
<div> <!-- start type PHImageRequestOptionsResizeMode -->
<h3>New Type Photos.PHImageRequestOptionsResizeMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsResizeMode {
	<span class='added added-field ' data-is-non-breaking="">Exact = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsResizeMode -->
<div> <!-- start type PHImageRequestOptionsVersion -->
<h3>New Type Photos.PHImageRequestOptionsVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsVersion {
	<span class='added added-field ' data-is-non-breaking="">Current = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Original = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unadjusted = 1,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsVersion -->
<div> <!-- start type PHImageResultHandler -->
<h3>New Type Photos.PHImageResultHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageResultHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageResultHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AppKit.NSImage result, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (AppKit.NSImage result, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageResultHandler -->
<div> <!-- start type PHLivePhotoEditingOption -->
<h3>New Type Photos.PHLivePhotoEditingOption</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoEditingOption : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? ShouldRenderAtPlaybackTime { get; }</span>
}
</pre>
</div> <!-- end type PHLivePhotoEditingOption -->
<div> <!-- start type PHObject -->
<h3>New Type Photos.PHObject</h3>
<pre class='added' data-is-non-breaking="">
public class PHObject : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHObject -->
<div> <!-- start type PHObjectChangeDetails -->
<h3>New Type Photos.PHObjectChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHObjectChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHObjectChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AssetContentChanged { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ObjectWasDeleted { get; }</span>
}
</pre>
</div> <!-- end type PHObjectChangeDetails -->
<div> <!-- start type PHPhotoLibrary -->
<h3>New Type Photos.PHPhotoLibrary</h3>
<pre class='added' data-is-non-breaking="">
public class PHPhotoLibrary : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static PHAuthorizationStatus AuthorizationStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHPhotoLibrary SharedPhotoLibrary { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformChanges (System.Action changeHandler, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PerformChangesAndWait (System.Action changeHandler, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestAuthorization (System.Action&lt;PHAuthorizationStatus&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;PHAuthorizationStatus&gt; RequestAuthorizationAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnregisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary -->
<div> <!-- start type PHPhotoLibraryChangeObserver -->
<h3>New Type Photos.PHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public abstract class PHPhotoLibraryChangeObserver : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IPHPhotoLibraryChangeObserver, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type PHPhotoLibraryChangeObserver -->
<div> <!-- start type PHPhotoLibrary_CloudIdentifiers -->
<h3>New Type Photos.PHPhotoLibrary_CloudIdentifiers</h3>
<pre class='added' data-is-non-breaking="">
public static class PHPhotoLibrary_CloudIdentifiers {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCloudIdentifier[] GetCloudIdentifiers (PHPhotoLibrary This, string[] localIdentifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetLocalIdentifiers (PHPhotoLibrary This, PHCloudIdentifier[] cloudIdentifiers);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary_CloudIdentifiers -->
<div> <!-- start type PHProject -->
<h3>New Type Photos.PHProject</h3>
<pre class='added' data-is-non-breaking="">
public class PHProject : Photos.PHAssetCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProject ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ProjectExtensionData { get; }</span>
}
</pre>
</div> <!-- end type PHProject -->
<div> <!-- start type PHProjectAssetElement -->
<h3>New Type Photos.PHProjectAssetElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectAssetElement : Photos.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectAssetElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectAssetElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectAssetElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectAssetElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Annotation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCloudIdentifier CloudAssetIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect CropRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectRegionOfInterest[] RegionsOfInterest { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectAssetElement -->
<div> <!-- start type PHProjectChangeRequest -->
<h3>New Type Photos.PHProjectChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectChangeRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectChangeRequest ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectChangeRequest (PHProject project);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ProjectExtensionData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetKeyAsset (PHAsset keyAsset);</span>
}
</pre>
</div> <!-- end type PHProjectChangeRequest -->
<div> <!-- start type PHProjectCreationSource -->
<h3>New Type Photos.PHProjectCreationSource</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectCreationSource {
	<span class='added added-field ' data-is-non-breaking="">Album = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Memory = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Moment = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Project = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectBook = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectCalendar = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectCard = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectExtension = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectPrintOrder = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectSlideshow = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserSelection = 1,</span>
}
</pre>
</div> <!-- end type PHProjectCreationSource -->
<div> <!-- start type PHProjectElement -->
<h3>New Type Photos.PHProjectElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectElement : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Placement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectElement -->
<div> <!-- start type PHProjectExtensionContext -->
<h3>New Type Photos.PHProjectExtensionContext</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectExtensionContext : Foundation.NSExtensionContext, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectExtensionContext ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectExtensionContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectExtensionContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHPhotoLibrary PhotoLibrary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProject Project { get; }</span>
}
</pre>
</div> <!-- end type PHProjectExtensionContext -->
<div> <!-- start type PHProjectExtensionController_Extensions -->
<h3>New Type Photos.PHProjectExtensionController_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PHProjectExtensionController_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHProjectTypeDescription[] GetSupportedProjectTypes (IPHProjectExtensionController This);</span>
}
</pre>
</div> <!-- end type PHProjectExtensionController_Extensions -->
<div> <!-- start type PHProjectInfo -->
<h3>New Type Photos.PHProjectInfo</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectInfo : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectInfo (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectInfo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectInfo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectCreationSource CreationSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ProjectType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSection[] Sections { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectInfo -->
<div> <!-- start type PHProjectJournalEntryElement -->
<h3>New Type Photos.PHProjectJournalEntryElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectJournalEntryElement : Photos.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectJournalEntryElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectJournalEntryElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectJournalEntryElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectJournalEntryElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectAssetElement AssetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Date { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTextElement TextElement { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectJournalEntryElement -->
<div> <!-- start type PHProjectRegionOfInterest -->
<h3>New Type Photos.PHProjectRegionOfInterest</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectRegionOfInterest : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectRegionOfInterest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectRegionOfInterest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectRegionOfInterest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectRegionOfInterest -->
<div> <!-- start type PHProjectSection -->
<h3>New Type Photos.PHProjectSection</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectSection : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectSection (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSectionContent[] SectionContents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSectionType SectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectSection -->
<div> <!-- start type PHProjectSectionContent -->
<h3>New Type Photos.PHProjectSectionContent</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectSectionContent : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectSectionContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSectionContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSectionContent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double AspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCloudIdentifier[] CloudAssetIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectElement[] Elements { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfColumns { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectSectionContent -->
<div> <!-- start type PHProjectSectionType -->
<h3>New Type Photos.PHProjectSectionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectSectionType {
	<span class='added added-field ' data-is-non-breaking="">Auxiliary = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Content = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Cover = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type PHProjectSectionType -->
<div> <!-- start type PHProjectTextElement -->
<h3>New Type Photos.PHProjectTextElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectTextElement : Photos.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTextElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTextElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTextElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTextElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Text { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTextElementType TextElementType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectTextElement -->
<div> <!-- start type PHProjectTextElementType -->
<h3>New Type Photos.PHProjectTextElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectTextElementType {
	<span class='added added-field ' data-is-non-breaking="">Body = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtitle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Title = 1,</span>
}
</pre>
</div> <!-- end type PHProjectTextElementType -->
<div> <!-- start type PHProjectType -->
<h3>New Type Photos.PHProjectType</h3>
<pre class='added' data-is-non-breaking="">
public static class PHProjectType {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Undefined { get; }</span>
}
</pre>
</div> <!-- end type PHProjectType -->
<div> <!-- start type PHProjectTypeDescription -->
<h3>New Type Photos.PHProjectTypeDescription</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectTypeDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTypeDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTypeDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSString projectType, string localizedTitle, string localizedDescription, AppKit.NSImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSString projectType, string localizedTitle, string localizedDescription, AppKit.NSImage image, PHProjectTypeDescription[] subtypeDescriptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ProjectType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTypeDescription[] SubtypeDescriptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectTypeDescription -->

</div> <!-- end namespace Photos -->
<!-- start namespace QTKit --> <div> 
<h2>Namespace QTKit</h2>
<!-- start type QTCaptureLayer --> <div>
<h3>Type Changed: QTKit.QTCaptureLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTCaptureLayer -->
<!-- start type QTMovieLayer --> <div>
<h3>Type Changed: QTKit.QTMovieLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTMovieLayer -->

</div> <!-- end namespace QTKit -->
<!-- start namespace QuartzComposer --> <div> 
<h2>Namespace QuartzComposer</h2>
<!-- start type QCCompositionLayer --> <div>
<h3>Type Changed: QuartzComposer.QCCompositionLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QCCompositionLayer -->

</div> <!-- end namespace QuartzComposer -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNLayer --> <div>
<h3>Type Changed: SceneKit.SCNLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type SCNLayer -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_8_SHA256 = 4869,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_SHA256 = 4868,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_GCM_SHA256 = 4865,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_256_GCM_SHA384 = 4866,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_CHACHA20_POLY1305_SHA256 = 4867,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->

</div> <!-- end namespace Security -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKLabelNode --> <div>
<h3>Type Changed: SpriteKit.SKLabelNode</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSLineBreakMode LineBreakMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfLines { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredMaxLayoutWidth { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKLabelNode FromText (Foundation.NSAttributedString attributedText);</span>
</pre>
</div>

</div> <!-- end type SKLabelNode -->
<div> <!-- start type SKNodeFocusBehavior -->
<h3>New Type SpriteKit.SKNodeFocusBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKNodeFocusBehavior {
	<span class='added added-field ' data-is-non-breaking="">Focusable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Occluding = 1,</span>
}
</pre>
</div> <!-- end type SKNodeFocusBehavior -->
<div> <!-- start type SKRenderer -->
<h3>New Type SpriteKit.SKRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class SKRenderer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IgnoresSiblingOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKScene Scene { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldCullNonVisibleNodes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsDrawCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsFields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsNodeCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsPhysics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsQuadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKRenderer FromDevice (Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLCommandBuffer commandBuffer, Metal.MTLRenderPassDescriptor renderPassDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLRenderCommandEncoder renderCommandEncoder, Metal.MTLRenderPassDescriptor renderPassDescriptor, Metal.IMTLCommandQueue commandQueue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (double currentTime);</span>
}
</pre>
</div> <!-- end type SKRenderer -->
<div> <!-- start type SKTransformNode -->
<h3>New Type SpriteKit.SKTransformNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKTransformNode : SpriteKit.SKNode, AppKit.INSTouchBarProvider, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 EulerAngles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Quaternion Quaternion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 RotationMatrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat XRotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat YRotation { get; set; }</span>
}
</pre>
</div> <!-- end type SKTransformNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKErrorCode --> <div>
<h3>Type Changed: WebKit.WKErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreCompileFailed = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreLookUpFailed = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreRemoveFailed = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreVersionMismatch = 9,</span>
</pre>
</div>

</div> <!-- end type WKErrorCode -->
<!-- start type WKFrameInfo --> <div>
<h3>Type Changed: WebKit.WKFrameInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKWebView WebView { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type WKFrameInfo -->
<!-- start type WKUserContentController --> <div>
<h3>Type Changed: WebKit.WKUserContentController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddContentRuleList (WKContentRuleList contentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllContentRuleLists ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (WKContentRuleList contentRuleList);</span>
</pre>
</div>

</div> <!-- end type WKUserContentController -->
<!-- start type WKWebView --> <div>
<h3>Type Changed: WebKit.WKWebView</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool HandlesUrlScheme (string urlScheme);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TakeSnapshot (WKSnapshotConfiguration snapshotConfiguration, System.Action&lt;AppKit.NSImage,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AppKit.NSImage&gt; TakeSnapshotAsync (WKSnapshotConfiguration snapshotConfiguration);</span>
</pre>
</div>

</div> <!-- end type WKWebView -->
<!-- start type WKWebViewConfiguration --> <div>
<h3>Type Changed: WebKit.WKWebViewConfiguration</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWKUrlSchemeHandler GetUrlSchemeHandler (string urlScheme);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetUrlSchemeHandler (IWKUrlSchemeHandler urlSchemeHandler, string urlScheme);</span>
</pre>
</div>

</div> <!-- end type WKWebViewConfiguration -->
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKHttpCookieStore HttpCookieStore { get; }</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->
<!-- start type WebView --> <div>
<h3>Type Changed: WebKit.WebView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSelectedDomRange (DomRange range, AppKit.NSSelectionAffinity selectionAffinity);</span>
</pre>
</div>

</div> <!-- end type WebView -->
<div> <!-- start type IWKHttpCookieStoreObserver -->
<h3>New Type WebKit.IWKHttpCookieStoreObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKHttpCookieStoreObserver : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IWKHttpCookieStoreObserver -->
<div> <!-- start type IWKUrlSchemeHandler -->
<h3>New Type WebKit.IWKUrlSchemeHandler</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeHandler : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartUrlSchemeTask (WKWebView webView, IWKUrlSchemeTask urlSchemeTask);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopUrlSchemeTask (WKWebView webView, IWKUrlSchemeTask urlSchemeTask);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeHandler -->
<div> <!-- start type IWKUrlSchemeTask -->
<h3>New Type WebKit.IWKUrlSchemeTask</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeTask : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrlRequest Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFailWithError (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveData (Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveResponse (Foundation.NSUrlResponse response);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeTask -->
<div> <!-- start type WKContentRuleList -->
<h3>New Type WebKit.WKContentRuleList</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleList : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type WKContentRuleList -->
<div> <!-- start type WKContentRuleListStore -->
<h3>New Type WebKit.WKContentRuleListStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleListStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleListStore ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleListStore (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleListStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static WKContentRuleListStore DefaultStore { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CompileContentRuleList (string identifier, string encodedContentRuleList, System.Action&lt;WKContentRuleList,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; CompileContentRuleListAsync (string identifier, string encodedContentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public static WKContentRuleListStore FromUrl (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAvailableContentRuleListIdentifiers (System.Action&lt;System.String[]&gt; callback);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; GetAvailableContentRuleListIdentifiersAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LookUpContentRuleList (string identifier, System.Action&lt;WKContentRuleList,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; LookUpContentRuleListAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RemoveContentRuleListAsync (string identifier);</span>
}
</pre>
</div> <!-- end type WKContentRuleListStore -->
<div> <!-- start type WKHttpCookieStore -->
<h3>New Type WebKit.WKHttpCookieStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKHttpCookieStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected WKHttpCookieStore (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKHttpCookieStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeleteCookie (Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DeleteCookieAsync (Foundation.NSHttpCookie cookie);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAllCookies (System.Action&lt;Foundation.NSHttpCookie[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSHttpCookie[]&gt; GetAllCookiesAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCookie (Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetCookieAsync (Foundation.NSHttpCookie cookie);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStore -->
<div> <!-- start type WKHttpCookieStoreObserver_Extensions -->
<h3>New Type WebKit.WKHttpCookieStoreObserver_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class WKHttpCookieStoreObserver_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CookiesDidChangeInCookieStore (IWKHttpCookieStoreObserver This, WKHttpCookieStore cookieStore);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStoreObserver_Extensions -->
<div> <!-- start type WKSnapshotConfiguration -->
<h3>New Type WebKit.WKSnapshotConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class WKSnapshotConfiguration : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKSnapshotConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKSnapshotConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKSnapshotConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber SnapshotWidth { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type WKSnapshotConfiguration -->

</div> <!-- end namespace WebKit -->
<!-- start namespace CoreML --> <div> 
<h2>New Namespace CoreML</h2>

<div> <!-- start type IMLFeatureProvider -->
<h3>New Type CoreML.IMLFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMLFeatureProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type IMLFeatureProvider -->
<div> <!-- start type MLDictionaryFeatureProvider -->
<h3>New Type CoreML.MLDictionaryFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryFeatureProvider : Foundation.NSObject, IMLFeatureProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; dictionary, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureValue&gt; Dictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLFeatureValue Item { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type MLDictionaryFeatureProvider -->
<div> <!-- start type MLFeatureDescription -->
<h3>New Type CoreML.MLFeatureDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureDescription : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Optional { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAllowed (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureDescription -->
<div> <!-- start type MLFeatureType -->
<h3>New Type CoreML.MLFeatureType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLFeatureType {
	<span class='added added-field ' data-is-non-breaking="">Dictionary = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Double = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Int64 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiArray = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 3,</span>
}
</pre>
</div> <!-- end type MLFeatureType -->
<div> <!-- start type MLFeatureValue -->
<h3>New Type CoreML.MLFeatureValue</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureValue : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureValue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; DictionaryValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double DoubleValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer ImageBufferValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long Int64Value { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArray MultiArrayValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Undefined { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue CreateUndefined (MLFeatureType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromDictionary (Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; value, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromDouble (double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromInt64 (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromMultiArray (MLMultiArray value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromPixelBuffer (CoreVideo.CVPixelBuffer value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromString (string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqual (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureValue -->
<div> <!-- start type MLModel -->
<h3>New Type CoreML.MLModel</h3>
<pre class='added' data-is-non-breaking="">
public class MLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLModelDescription ModelDescription { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MLModel FromUrl (Foundation.NSUrl url, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MLModel -->
<div> <!-- start type MLModelDescription -->
<h3>New Type CoreML.MLModelDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelDescription : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; InputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLModelMetadata Metadata { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; OutputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedFeatureName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedProbabilitiesName { get; }</span>
}
</pre>
</div> <!-- end type MLModelDescription -->
<div> <!-- start type MLModelError -->
<h3>New Type CoreML.MLModelError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLModelError {
	<span class='added added-field ' data-is-non-breaking="">DescriptionMismatch = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FeatureType = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Generic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Io = 3,</span>
}
</pre>
</div> <!-- end type MLModelError -->
<div> <!-- start type MLModelErrorExtensions -->
<h3>New Type CoreML.MLModelErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MLModelErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (MLModelError self);</span>
}
</pre>
</div> <!-- end type MLModelErrorExtensions -->
<div> <!-- start type MLModelMetadata -->
<h3>New Type CoreML.MLModelMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelMetadata : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Description { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string License { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string VersionString { get; }</span>
}
</pre>
</div> <!-- end type MLModelMetadata -->
<div> <!-- start type MLMultiArray -->
<h3>New Type CoreML.MLMultiArray</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSError error);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (IntPtr dataPointer, Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSNumber[] strides, System.Action&lt;IntPtr&gt; deallocator, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr DataPointer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Shape { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Strides { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (nint idx);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, nint idx);</span>
}
</pre>
</div> <!-- end type MLMultiArray -->
<div> <!-- start type MLMultiArrayDataType -->
<h3>New Type CoreML.MLMultiArrayDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLMultiArrayDataType {
	<span class='added added-field ' data-is-non-breaking="">Double = 65600,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 65568,</span>
	<span class='added added-field ' data-is-non-breaking="">Int32 = 131104,</span>
}
</pre>
</div> <!-- end type MLMultiArrayDataType -->
</div> <!-- end namespace CoreML -->

<!-- start namespace Vision --> <div> 
<h2>New Namespace Vision</h2>

<div> <!-- start type IVNFaceObservationAccepting -->
<h3>New Type Vision.IVNFaceObservationAccepting</h3>
<pre class='added' data-is-non-breaking="">
public interface IVNFaceObservationAccepting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type IVNFaceObservationAccepting -->
<div> <!-- start type VNBarcodeObservation -->
<h3>New Type Vision.VNBarcodeObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNBarcodeObservation : Vision.VNRectangleObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Symbology { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNBarcodeObservation -->
<div> <!-- start type VNBarcodeSymbology -->
<h3>New Type Vision.VNBarcodeSymbology</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNBarcodeSymbology {
	<span class='added added-field ' data-is-non-breaking="">Aztec = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Code128 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39Checksum = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAscii = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAsciiChecksum = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93i = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DataMatrix = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean13 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean8 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5Checksum = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Itf14 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Pdf417 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">QR = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Upce = 16,</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbology -->
<div> <!-- start type VNBarcodeSymbologyExtensions -->
<h3>New Type Vision.VNBarcodeSymbologyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNBarcodeSymbologyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (VNBarcodeSymbology self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbologyExtensions -->
<div> <!-- start type VNClassificationObservation -->
<h3>New Type Vision.VNClassificationObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNClassificationObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNClassificationObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type VNClassificationObservation -->
<div> <!-- start type VNCoreMLFeatureValueObservation -->
<h3>New Type Vision.VNCoreMLFeatureValueObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLFeatureValueObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLFeatureValueObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreML.MLFeatureValue FeatureValue { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLFeatureValueObservation -->
<div> <!-- start type VNCoreMLModel -->
<h3>New Type Vision.VNCoreMLModel</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNCoreMLModel FromMLModel (CoreML.MLModel model, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNCoreMLModel -->
<div> <!-- start type VNCoreMLRequest -->
<h3>New Type Vision.VNCoreMLRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNImageCropAndScaleOption ImageCropAndScaleOption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNCoreMLModel Model { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLRequest -->
<div> <!-- start type VNDetectBarcodesRequest -->
<h3>New Type Vision.VNDetectBarcodesRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNDetectBarcodesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectBarcodesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string[] SupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Symbologies { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectBarcodesRequest -->
<div> <!-- start type VNDetectFaceLandmarksRequest -->
<h3>New Type Vision.VNDetectFaceLandmarksRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceLandmarksRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IVNFaceObservationAccepting {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceLandmarksRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceLandmarksRequest -->
<div> <!-- start type VNDetectFaceRectanglesRequest -->
<h3>New Type Vision.VNDetectFaceRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceRectanglesRequest -->
<div> <!-- start type VNDetectHorizonRequest -->
<h3>New Type Vision.VNDetectHorizonRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectHorizonRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectHorizonRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectHorizonRequest -->
<div> <!-- start type VNDetectRectanglesRequest -->
<h3>New Type Vision.VNDetectRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumObservations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumConfidence { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float QuadratureTolerance { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectRectanglesRequest -->
<div> <!-- start type VNDetectTextRectanglesRequest -->
<h3>New Type Vision.VNDetectTextRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectTextRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectTextRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReportCharacterBoxes { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectTextRectanglesRequest -->
<div> <!-- start type VNDetectedObjectObservation -->
<h3>New Type Vision.VNDetectedObjectObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectedObjectObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectedObjectObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect BoundingBox { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNDetectedObjectObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNDetectedObjectObservation -->
<div> <!-- start type VNErrorCode -->
<h3>New Type Vision.VNErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNErrorCode {
	<span class='added added-field ' data-is-non-breaking="">IOError = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InternalError = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidArgument = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidImage = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidModel = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOperation = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOption = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingOption = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">NotImplemented = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationFailed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfBoundsError = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfMemory = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestCancelled = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownError = 11,</span>
}
</pre>
</div> <!-- end type VNErrorCode -->
<div> <!-- start type VNErrorCodeExtensions -->
<h3>New Type Vision.VNErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (VNErrorCode self);</span>
}
</pre>
</div> <!-- end type VNErrorCodeExtensions -->
<div> <!-- start type VNFaceLandmarkRegion -->
<h3>New Type Vision.VNFaceLandmarkRegion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarkRegion : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PointCount { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion -->
<div> <!-- start type VNFaceLandmarkRegion2D -->
<h3>New Type Vision.VNFaceLandmarkRegion2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarkRegion2D : Vision.VNFaceLandmarkRegion, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.Vector2 Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector2[] Points { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2 GetPoint (uint index);</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion2D -->
<div> <!-- start type VNFaceLandmarks -->
<h3>New Type Vision.VNFaceLandmarks</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarks : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks -->
<div> <!-- start type VNFaceLandmarks2D -->
<h3>New Type Vision.VNFaceLandmarks2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarks2D : Vision.VNFaceLandmarks, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D AllPoints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D FaceContour { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D InnerLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftPupil { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D MedianLine { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D Nose { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D NoseCrest { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D OuterLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightPupil { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks2D -->
<div> <!-- start type VNFaceObservation -->
<h3>New Type Vision.VNFaceObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNFaceObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarks2D Landmarks { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNFaceObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNFaceObservation -->
<div> <!-- start type VNHomographicImageRegistrationRequest -->
<h3>New Type Vision.VNHomographicImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNHomographicImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNHomographicImageRegistrationRequest -->
<div> <!-- start type VNHorizonObservation -->
<h3>New Type Vision.VNHorizonObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNHorizonObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHorizonObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Angle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform Transform { get; }</span>
}
</pre>
</div> <!-- end type VNHorizonObservation -->
<div> <!-- start type VNImageAlignmentObservation -->
<h3>New Type Vision.VNImageAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageAlignmentObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageAlignmentObservation -->
<div> <!-- start type VNImageBasedRequest -->
<h3>New Type Vision.VNImageBasedRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageBasedRequest : Vision.VNRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageBasedRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect RegionOfInterest { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageBasedRequest -->
<div> <!-- start type VNImageCropAndScaleOption -->
<h3>New Type Vision.VNImageCropAndScaleOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNImageCropAndScaleOption {
	<span class='added added-field ' data-is-non-breaking="">CenterCrop = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFill = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFit = 1,</span>
}
</pre>
</div> <!-- end type VNImageCropAndScaleOption -->
<div> <!-- start type VNImageHomographicAlignmentObservation -->
<h3>New Type Vision.VNImageHomographicAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageHomographicAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageHomographicAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 WarpTransform { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageHomographicAlignmentObservation -->
<div> <!-- start type VNImageOptions -->
<h3>New Type Vision.VNImageOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CameraIntrinsics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary WeakProperties { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageOptions -->
<div> <!-- start type VNImageRegistrationRequest -->
<h3>New Type Vision.VNImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageRegistrationRequest : Vision.VNTargetedImageRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageRegistrationRequest -->
<div> <!-- start type VNImageRequestHandler -->
<h3>New Type Vision.VNImageRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNImageRequestHandler -->
<div> <!-- start type VNImageTranslationAlignmentObservation -->
<h3>New Type Vision.VNImageTranslationAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageTranslationAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageTranslationAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform AlignmentTransform { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageTranslationAlignmentObservation -->
<div> <!-- start type VNObservation -->
<h3>New Type Vision.VNObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNObservation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid Uuid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type VNObservation -->
<div> <!-- start type VNPixelBufferObservation -->
<h3>New Type Vision.VNPixelBufferObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNPixelBufferObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNPixelBufferObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
}
</pre>
</div> <!-- end type VNPixelBufferObservation -->
<div> <!-- start type VNRectangleObservation -->
<h3>New Type Vision.VNRectangleObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNRectangleObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRectangleObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopRight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNRectangleObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNRectangleObservation -->
<div> <!-- start type VNRequest -->
<h3>New Type Vision.VNRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNRequest : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestCompletionHandler CompletionHandler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreferBackgroundProcessing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice PreferredMetalContext { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual T[] GetResults&lt;T&gt; ();</span>
}
</pre>
</div> <!-- end type VNRequest -->
<div> <!-- start type VNRequestCompletionHandler -->
<h3>New Type Vision.VNRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate VNRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (VNRequest request, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (VNRequest request, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNRequestCompletionHandler -->
<div> <!-- start type VNRequestTrackingLevel -->
<h3>New Type Vision.VNRequestTrackingLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNRequestTrackingLevel {
	<span class='added added-field ' data-is-non-breaking="">Accurate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
}
</pre>
</div> <!-- end type VNRequestTrackingLevel -->
<div> <!-- start type VNSequenceRequestHandler -->
<h3>New Type Vision.VNSequenceRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNSequenceRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNSequenceRequestHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNSequenceRequestHandler -->
<div> <!-- start type VNTargetedImageRequest -->
<h3>New Type Vision.VNTargetedImageRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTargetedImageRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTargetedImageRequest -->
<div> <!-- start type VNTextObservation -->
<h3>New Type Vision.VNTextObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNTextObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTextObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRectangleObservation[] CharacterBoxes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNTextObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNTextObservation -->
<div> <!-- start type VNTrackObjectRequest -->
<h3>New Type Vision.VNTrackObjectRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackObjectRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackObjectRequest -->
<div> <!-- start type VNTrackRectangleRequest -->
<h3>New Type Vision.VNTrackRectangleRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackRectangleRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackRectangleRequest -->
<div> <!-- start type VNTrackingRequest -->
<h3>New Type Vision.VNTrackingRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTrackingRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackingRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNDetectedObjectObservation InputObservation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LastFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestTrackingLevel TrackingLevel { get; set; }</span>
}
</pre>
</div> <!-- end type VNTrackingRequest -->
<div> <!-- start type VNTranslationalImageRegistrationRequest -->
<h3>New Type Vision.VNTranslationalImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTranslationalImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTranslationalImageRegistrationRequest -->
<div> <!-- start type VNUtils -->
<h3>New Type Vision.VNUtils</h3>
<pre class='added' data-is-non-breaking="">
public static class VNUtils {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGRect NormalizedIdentityRect { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (CoreGraphics.CGPoint normalizedPoint, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetImageRect (CoreGraphics.CGRect normalizedRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetNormalizedFaceBoundingBoxPoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetNormalizedRect (CoreGraphics.CGRect imageRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsIdentityRect (CoreGraphics.CGRect rect);</span>
}
</pre>
</div> <!-- end type VNUtils -->
</div> <!-- end namespace Vision -->

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
</script><h1 id='diff/xm/4.5/Xamarin.Mac.html'>Xamarin.Mac.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVCaptureVideoPreviewLayer --> <div>
<h3>Type Changed: AVFoundation.AVCaptureVideoPreviewLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVCaptureVideoPreviewLayer -->
<!-- start type AVPlayerLayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayerLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVPlayerLayer -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVSynchronizedLayer --> <div>
<h3>Type Changed: AVFoundation.AVSynchronizedLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSynchronizedLayer -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVPlayerView --> <div>
<h3>Type Changed: AVKit.AVPlayerView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UpdatesNowPlayingInfoCenter { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerView -->
<div> <!-- start type AVRoutePickerView -->
<h3>New Type AVKit.AVRoutePickerView</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerView : AppKit.NSView, AppKit.INSAccessibility, AppKit.INSAccessibilityElementProtocol, AppKit.INSAppearanceCustomization, AppKit.INSDraggingDestination, AppKit.INSTouchBarProvider, AppKit.INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVRoutePickerViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RoutePickerButtonBordered { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSColor GetRoutePickerButtonColor (AVRoutePickerViewButtonState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetRoutePickerButtonColor (AppKit.NSColor color, AVRoutePickerViewButtonState state);</span>
}
</pre>
</div> <!-- end type AVRoutePickerView -->
<div> <!-- start type AVRoutePickerViewButtonState -->
<h3>New Type AVKit.AVRoutePickerViewButtonState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVRoutePickerViewButtonState {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ActiveHighlighted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NormalHighlighted = 1,</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewButtonState -->
<div> <!-- start type AVRoutePickerViewDelegate -->
<h3>New Type AVKit.AVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerViewDelegate : Foundation.NSObject, IAVRoutePickerViewDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndPresentingRoutes (AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginPresentingRoutes (AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate -->
<div> <!-- start type AVRoutePickerViewDelegate_Extensions -->
<h3>New Type AVKit.AVRoutePickerViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVRoutePickerViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate_Extensions -->
<div> <!-- start type IAVRoutePickerViewDelegate -->
<h3>New Type AVKit.IAVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVRoutePickerViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IAVRoutePickerViewDelegate -->

</div> <!-- end namespace AVKit -->
<!-- start namespace Accounts --> <div> 
<h2>Namespace Accounts</h2>
<!-- start type ACAccountStore --> <div>
<h3>Type Changed: Accounts.ACAccountStore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAccount (ACAccount account, ACAccountStoreRemoveCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; RemoveAccountAsync (ACAccount account);</span>
</pre>
</div>

</div> <!-- end type ACAccountStore -->
<div> <!-- start type ACAccountStoreRemoveCompletionHandler -->
<h3>New Type Accounts.ACAccountStoreRemoveCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ACAccountStoreRemoveCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ACAccountStoreRemoveCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (bool success, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (bool success, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type ACAccountStoreRemoveCompletionHandler -->

</div> <!-- end namespace Accounts -->
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSAccessibilityAttributes --> <div>
<h3>Type Changed: AppKit.NSAccessibilityAttributes</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CustomTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LanguageTextAttribute { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityAttributes -->
<!-- start type NSAccessibilityElement --> <div>
<h3>Type Changed: AppKit.NSAccessibilityElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityElement -->
<!-- start type NSAccessibilityRoles --> <div>
<h3>Type Changed: AppKit.NSAccessibilityRoles</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PageRole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityRoles -->
<!-- start type NSAccessibilitySubroles --> <div>
<h3>Type Changed: AppKit.NSAccessibilitySubroles</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CollectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TabButtonSubrole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilitySubroles -->
<!-- start type NSAccessibility_Extensions --> <div>
<h3>Type Changed: AppKit.NSAccessibility_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityElement[] GetAccessibilityChildrenInNavigationOrder (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomAction[] GetAccessibilityCustomActions (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomRotor[] GetAccessibilityCustomRotors (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityChildrenInNavigationOrder (INSAccessibility This, NSAccessibilityElement[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomActions (INSAccessibility This, NSAccessibilityCustomAction[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomRotors (INSAccessibility This, NSAccessibilityCustomRotor[] value);</span>
</pre>
</div>

</div> <!-- end type NSAccessibility_Extensions -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;NSApplicationOpenUrlsEventArgs&gt; OpenUrls;</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSApplicationDelegate --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenUrls (NSApplication application, Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate -->
<!-- start type NSApplicationDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void OpenUrls (INSApplicationDelegate This, NSApplication application, Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate_Extensions -->
<!-- start type NSBezierPath --> <div>
<h3>Type Changed: AppKit.NSBezierPath</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (uint[], NSFont)' instead.")]
	public void AppendPathWithGlyphs (uint[] glyphs, NSFont font);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (CGPoint[])' instead.")]
	public void AppendPathWithPoints (CoreGraphics.CGPoint[] points);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Append (NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (CoreGraphics.CGPoint[] points);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (uint[] glyphs, NSFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AppendBezierPathWithCGGlyph (ushort glyph, NSFont font);</span>
</pre>
</div>

</div> <!-- end type NSBezierPath -->
<!-- start type NSButton --> <div>
<h3>Type Changed: AppKit.NSButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
</pre>
</div>

</div> <!-- end type NSButton -->
<!-- start type NSCell --> <div>
<h3>Type Changed: AppKit.NSCell</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCell -->
<!-- start type NSCollectionView --> <div>
<h3>Type Changed: AppKit.NSCollectionView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSCollectionViewPrefetching PrefetchDataSource { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCollectionView -->
<!-- start type NSCollectionViewTransitionLayout --> <div>
<h3>Type Changed: AppKit.NSCollectionViewTransitionLayout</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the constructor that allows you to set currentLayout and newLayout.")]
	public NSCollectionViewTransitionLayout ();</span>
</div></pre>

</div> <!-- end type NSCollectionViewTransitionLayout -->
<!-- start type NSColor --> <div>
<h3>Type Changed: AppKit.NSColor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBlueColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBrownColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGrayColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGreenColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemOrangeColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPinkColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPurpleColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemRedColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemYellowColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorType Type { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name, Foundation.NSBundle bundle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSColor GetColor (NSColorType type);</span>
</pre>
</div>

</div> <!-- end type NSColor -->
<!-- start type NSColorPickerTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSColorPickerTouchBarItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorSpace[] AllowedColorSpaces { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSColorPickerTouchBarItem -->
<!-- start type NSDocument --> <div>
<h3>Type Changed: AppKit.NSDocument</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentSharing { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (Foundation.NSCoder coder, Foundation.NSOperationQueue queue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Prepare (NSSharingServicePicker sharingServicePicker);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ShareDocument (NSSharingService sharingService, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; ShareDocumentAsync (NSSharingService sharingService);</span>
</pre>
</div>

</div> <!-- end type NSDocument -->
<!-- start type NSDocumentController --> <div>
<h3>Type Changed: AppKit.NSDocumentController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsAutomaticShareMenu { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMenuItem StandardShareMenuItem { get; }</span>
</pre>
</div>

</div> <!-- end type NSDocumentController -->
<!-- start type NSDrawer --> <div>
<h3>Type Changed: AppKit.NSDrawer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDrawer -->
<!-- start type NSFont --> <div>
<h3>Type Changed: AppKit.NSFont</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSFont FromCTFont (CoreText.CTFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAdvancement (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreGraphics.CGSize[] GetAdvancements (ushort[] glyphs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetBoundingRect (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreGraphics.CGRect[] GetBoundingRects (ushort[] glyphs);</span>
</pre>
</div>

</div> <!-- end type NSFont -->
<!-- start type NSFontDescriptor --> <div>
<h3>Type Changed: AppKit.NSFontDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RequiresFontAssetRequest { get; }</span>
</pre>
</div>

</div> <!-- end type NSFontDescriptor -->
<!-- start type NSFontSymbolicTraits --> <div>
<h3>Type Changed: AppKit.NSFontSymbolicTraits</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TraitLooseLeading = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">TraitTightLeading = 32768,</span>
</pre>
</div>

</div> <!-- end type NSFontSymbolicTraits -->
<!-- start type NSGlyphInfo --> <div>
<h3>Type Changed: AppKit.NSGlyphInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BaseString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ushort GlyphId { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGlyphInfo GetGlyphInfo (ushort glyph, NSFont font, string string);</span>
</pre>
</div>

</div> <!-- end type NSGlyphInfo -->
<!-- start type NSGroupTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSGroupTouchBarItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions EffectiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceLayoutDirection GroupUserInterfaceLayoutDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredItemWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrefersEqualWidths { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions[] PrioritizedCompressionOptions { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateAlertStyleGroupItem (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateGroupItem (string identifier, NSTouchBarItem[] items, NSUserInterfaceCompressionOptions allowedCompressionOptions);</span>
</pre>
</div>

</div> <!-- end type NSGroupTouchBarItem -->
<!-- start type NSImageName --> <div>
<h3>Type Changed: AppKit.NSImageName</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TouchBarRemoveTemplate = 116,</span>
</pre>
</div>

</div> <!-- end type NSImageName -->
<!-- start type NSLayoutAnchor`1 --> <div>
<h3>Type Changed: AppKit.NSLayoutAnchor`1</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLayoutConstraint[] ConstraintsAffectingLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAmbiguousLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSLayoutAnchor`1 -->
<!-- start type NSLayoutXAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutXAxisAnchor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension GetAnchorWithOffset (NSLayoutXAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutXAxisAnchor -->
<!-- start type NSLayoutYAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutYAxisAnchor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension GetAnchorWithOffset (NSLayoutYAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutYAxisAnchor -->
<!-- start type NSLevelIndicator --> <div>
<h3>Type Changed: AppKit.NSLevelIndicator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor CriticalFillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DrawsTieredCapacityLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Editable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor FillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLevelIndicatorPlaceholderVisibility PlaceholderVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingPlaceholderImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor WarningFillColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSLevelIndicator -->
<!-- start type NSMenu --> <div>
<h3>Type Changed: AppKit.NSMenu</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenu -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: AppKit.NSMenuItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsKeyEquivalentWhenHidden { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOpenGLLayer --> <div>
<h3>Type Changed: AppKit.NSOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSOpenGLLayer -->
<!-- start type NSPasteboard --> <div>
<h3>Type Changed: AppKit.NSPasteboard</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameDrag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameFind { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameFont { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameGeneral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameRuler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardTypeFileUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardTypeUrl { get; }</span>
</pre>
</div>

</div> <!-- end type NSPasteboard -->
<!-- start type NSPopUpButton --> <div>
<h3>Type Changed: AppKit.NSPopUpButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>

</div> <!-- end type NSPopUpButton -->
<!-- start type NSPopover --> <div>
<h3>Type Changed: AppKit.NSPopover</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSAppearanceCustomization</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'GetAppearance' and 'SetAppearance' methods instead.")]
	public virtual NSPopoverAppearance Appearance { get; set; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAppearance EffectiveAppearance { get; }</span>
</pre>
</div>

</div> <!-- end type NSPopover -->
<!-- start type NSResponder --> <div>
<h3>Type Changed: AppKit.NSResponder</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (Foundation.NSCoder coder, Foundation.NSOperationQueue queue);</span>
</pre>
</div>

</div> <!-- end type NSResponder -->
<!-- start type NSSegmentedControl --> <div>
<h3>Type Changed: AppKit.NSSegmentedControl</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSegmentDistribution SegmentDistribution { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTextAlignment GetAlignment (nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetTag (nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetToolTip (nint forSegment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAlignment (NSTextAlignment alignment, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetShowsMenuIndicator (bool showsMenuIndicator, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTag (nint tag, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetToolTip (string toolTip, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShowsMenuIndicator (nint segment);</span>
</pre>
</div>

</div> <!-- end type NSSegmentedControl -->
<!-- start type NSSliderAccessory --> <div>
<h3>Type Changed: AppKit.NSSliderAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSSliderAccessory -->
<!-- start type NSSliderTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSSliderTouchBarItem</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
</pre>
</div>

</div> <!-- end type NSSliderTouchBarItem -->
<!-- start type NSSplitViewController --> <div>
<h3>Type Changed: AppKit.NSSplitViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceValidations</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ValidateUserInterfaceItem (INSValidatedUserInterfaceItem item);</span>
</pre>
</div>

</div> <!-- end type NSSplitViewController -->
<!-- start type NSStatusBarButton --> <div>
<h3>Type Changed: AppKit.NSStatusBarButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>

</div> <!-- end type NSStatusBarButton -->
<!-- start type NSStoryboard --> <div>
<h3>Type Changed: AppKit.NSStoryboard</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSStoryboard MainStoryboard { get; }</span>
</pre>
</div>

</div> <!-- end type NSStoryboard -->
<!-- start type NSTableView --> <div>
<h3>Type Changed: AppKit.NSTableView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesAutomaticRowHeights { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTableView -->
<!-- start type NSTextList --> <div>
<h3>Type Changed: AppKit.NSTextList</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextList (NSTextListMarkerFormats format, NSTextListOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSTextList -->
<!-- start type NSToolbar --> <div>
<h3>Type Changed: AppKit.NSToolbar</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSToolbar ();</span>
</pre>
</div>

</div> <!-- end type NSToolbar -->
<!-- start type NSTouchBar --> <div>
<h3>Type Changed: AppKit.NSTouchBar</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string EscapeKeyReplacementItemIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTouchBar -->
<!-- start type NSTouchBarItemIdentifier --> <div>
<h3>Type Changed: AppKit.NSTouchBarItemIdentifier</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CandidateList = 10,</span>
</pre>
</div>

</div> <!-- end type NSTouchBarItemIdentifier -->
<!-- start type NSView --> <div>
<h3>Type Changed: AppKit.NSView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSView -->
<!-- start type NSWindow --> <div>
<h3>Type Changed: AppKit.NSWindow</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTab Tab { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTabGroup TabGroup { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the EndSheet(NSWindow,NSModalResponse) overload.")]
	public virtual void EndSheet (NSWindow sheetWindow, nint returnCode);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndSheet (NSWindow sheetWindow, NSModalResponse returnCode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToggleTabOverview (Foundation.NSObject sender);</span>
</pre>
</div>

</div> <!-- end type NSWindow -->
<!-- start type NSWorkspace --> <div>
<h3>Type Changed: AppKit.NSWorkspace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SwitchControlEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool VoiceOverEnabled { get; }</span>
</pre>
</div>

</div> <!-- end type NSWorkspace -->
<div> <!-- start type DownloadFontAssetsRequestCompletionHandler -->
<h3>New Type AppKit.DownloadFontAssetsRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate DownloadFontAssetsRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DownloadFontAssetsRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type DownloadFontAssetsRequestCompletionHandler -->
<div> <!-- start type INSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type AppKit.INSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityCustomRotorItemSearchDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type INSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type INSAccessibilityElementLoading -->
<h3>New Type AppKit.INSAccessibilityElementLoading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityElementLoading : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityElement GetAccessibilityElement (Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type INSAccessibilityElementLoading -->
<div> <!-- start type INSCollectionViewPrefetching -->
<h3>New Type AppKit.INSCollectionViewPrefetching</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCollectionViewPrefetching : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrefetchItems (NSCollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type INSCollectionViewPrefetching -->
<div> <!-- start type INSUserInterfaceCompression -->
<h3>New Type AppKit.INSUserInterfaceCompression</h3>
<pre class='added' data-is-non-breaking="">
public interface INSUserInterfaceCompression : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
}
</pre>
</div> <!-- end type INSUserInterfaceCompression -->
<div> <!-- start type NSAboutPanelOption -->
<h3>New Type AppKit.NSAboutPanelOption</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAboutPanelOption {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationIcon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Credits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Version { get; }</span>
}
</pre>
</div> <!-- end type NSAboutPanelOption -->
<div> <!-- start type NSAccessibilityAnnotationAttributeKey -->
<h3>New Type AppKit.NSAccessibilityAnnotationAttributeKey</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityAnnotationAttributeKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationLabel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationLocation { get; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationAttributeKey -->
<div> <!-- start type NSAccessibilityAnnotationPosition -->
<h3>New Type AppKit.NSAccessibilityAnnotationPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityAnnotationPosition {
	<span class='added added-field ' data-is-non-breaking="">End = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FullRange = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Start = 1,</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationPosition -->
<div> <!-- start type NSAccessibilityCustomAction -->
<h3>New Type AppKit.NSAccessibilityCustomAction</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomAction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomAction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomAction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, System.Func&lt;bool&gt; handler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, Foundation.NSObject target, ObjCRuntime.Selector selector);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;bool&gt; Handler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Selector Selector { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Target { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomAction -->
<div> <!-- start type NSAccessibilityCustomRotor -->
<h3>New Type AppKit.NSAccessibilityCustomRotor</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (NSAccessibilityCustomRotorType rotorType, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (string label, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityElementLoading ItemLoadingDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityCustomRotorItemSearchDelegate ItemSearchDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorType Type { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotor -->
<div> <!-- start type NSAccessibilityCustomRotorItemResult -->
<h3>New Type AppKit.NSAccessibilityCustomRotorItemResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorItemResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (NSAccessibilityElement targetElement);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemResult (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (Foundation.INSSecureCoding itemLoadingToken, string customLabel);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.INSSecureCoding ItemLoadingToken { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement TargetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange TargetRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemResult -->
<div> <!-- start type NSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type AppKit.NSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSAccessibilityCustomRotorItemSearchDelegate : Foundation.NSObject, INSAccessibilityCustomRotorItemSearchDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type NSAccessibilityCustomRotorSearchDirection -->
<h3>New Type AppKit.NSAccessibilityCustomRotorSearchDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorSearchDirection {
	<span class='added added-field ' data-is-non-breaking="">Next = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Previous = 0,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchDirection -->
<div> <!-- start type NSAccessibilityCustomRotorSearchParameters -->
<h3>New Type AppKit.NSAccessibilityCustomRotorSearchParameters</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorSearchParameters : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorSearchParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorSearchParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorSearchParameters (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult CurrentItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FilterString { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorSearchDirection SearchDirection { get; set; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchParameters -->
<div> <!-- start type NSAccessibilityCustomRotorType -->
<h3>New Type AppKit.NSAccessibilityCustomRotorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorType {
	<span class='added added-field ' data-is-non-breaking="">Annotation = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">BoldText = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Custom = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Heading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel1 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel2 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel3 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel4 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel5 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel6 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">ItalicText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">MisspelledWord = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Table = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">TextField = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlinedText = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">VisitedLink = 20,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorType -->
<div> <!-- start type NSAccessibilityElementLoading_Extensions -->
<h3>New Type AppKit.NSAccessibilityElementLoading_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityElementLoading_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSRange GetAccessibilityRangeInTargetElement (INSAccessibilityElementLoading This, Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type NSAccessibilityElementLoading_Extensions -->
<div> <!-- start type NSApplicationOpenUrlsEventArgs -->
<h3>New Type AppKit.NSApplicationOpenUrlsEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class NSApplicationOpenUrlsEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSApplicationOpenUrlsEventArgs (Foundation.NSUrl[] urls);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl[] Urls { get; set; }</span>
}
</pre>
</div> <!-- end type NSApplicationOpenUrlsEventArgs -->
<div> <!-- start type NSCollectionViewPrefetching_Extensions -->
<h3>New Type AppKit.NSCollectionViewPrefetching_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSCollectionViewPrefetching_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelPrefetching (INSCollectionViewPrefetching This, NSCollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type NSCollectionViewPrefetching_Extensions -->
<div> <!-- start type NSColorType -->
<h3>New Type AppKit.NSColorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSColorType {
	<span class='added added-field ' data-is-non-breaking="">Catalog = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ComponentBased = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Pattern = 1,</span>
}
</pre>
</div> <!-- end type NSColorType -->
<div> <!-- start type NSFontAssetRequest -->
<h3>New Type AppKit.NSFontAssetRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSFontAssetRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFontAssetRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFontAssetRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFontAssetRequest (NSFontDescriptor[] fontDescriptors, NSFontAssetRequestOptions options);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFontDescriptor[] DownloadedFontDescriptors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSProgress Progress { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DownloadFontAssets (DownloadFontAssetsRequestCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type NSFontAssetRequest -->
<div> <!-- start type NSFontAssetRequestOptions -->
<h3>New Type AppKit.NSFontAssetRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontAssetRequestOptions {
	<span class='added added-field ' data-is-non-breaking="">UsesStandardUI = 1,</span>
}
</pre>
</div> <!-- end type NSFontAssetRequestOptions -->
<div> <!-- start type NSFontError -->
<h3>New Type AppKit.NSFontError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFontError {
	<span class='added added-field ' data-is-non-breaking="">AssetDownloadError = 66304,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMaximum = 66335,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMinimum = 66304,</span>
}
</pre>
</div> <!-- end type NSFontError -->
<div> <!-- start type NSFontPanelModeMask -->
<h3>New Type AppKit.NSFontPanelModeMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontPanelModeMask {
	<span class='added added-field ' data-is-non-breaking="">AllEffects = 1048320,</span>
	<span class='added added-field ' data-is-non-breaking="">AllModes = 4294967295,</span>
	<span class='added added-field ' data-is-non-breaking="">Collection = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">DocumentColorEffect = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">Face = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ShadowEffect = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">Size = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">StandardModes = 65535,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikethroughEffect = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">TextColorEffect = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlineEffect = 256,</span>
}
</pre>
</div> <!-- end type NSFontPanelModeMask -->
<div> <!-- start type NSLevelIndicatorPlaceholderVisibility -->
<h3>New Type AppKit.NSLevelIndicatorPlaceholderVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSLevelIndicatorPlaceholderVisibility {
	<span class='added added-field ' data-is-non-breaking="">Always = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WhileEditing = 2,</span>
}
</pre>
</div> <!-- end type NSLevelIndicatorPlaceholderVisibility -->
<div> <!-- start type NSObject_NSFontPanelValidationAdditions -->
<h3>New Type AppKit.NSObject_NSFontPanelValidationAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSObject_NSFontPanelValidationAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFontPanelModeMask GetValidModes (Foundation.NSObject This, NSFontPanel fontPanel);</span>
}
</pre>
</div> <!-- end type NSObject_NSFontPanelValidationAdditions -->
<div> <!-- start type NSRulerViewUnits -->
<h3>New Type AppKit.NSRulerViewUnits</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSRulerViewUnits {
	<span class='added added-field ' data-is-non-breaking="">Centimeters = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inches = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Picas = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Points = 2,</span>
}
</pre>
</div> <!-- end type NSRulerViewUnits -->
<div> <!-- start type NSRulerViewUnitsExtensions -->
<h3>New Type AppKit.NSRulerViewUnitsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSRulerViewUnitsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSRulerViewUnits self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSRulerViewUnits GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSRulerViewUnitsExtensions -->
<div> <!-- start type NSSegmentDistribution -->
<h3>New Type AppKit.NSSegmentDistribution</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSSegmentDistribution {
	<span class='added added-field ' data-is-non-breaking="">Fill = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FillEqually = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FillProportionally = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Fit = 0,</span>
}
</pre>
</div> <!-- end type NSSegmentDistribution -->
<div> <!-- start type NSTextListMarkerFormats -->
<h3>New Type AppKit.NSTextListMarkerFormats</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTextListMarkerFormats {
	<span class='added added-field ' data-is-non-breaking="">Box = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Check = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Decimal = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Disc = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Hyphen = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseAlpha = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseHexadecimal = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseLatin = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseRoman = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Octal = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseAlpha = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseHexadecimal = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseLatin = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseRoman = 15,</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormats -->
<div> <!-- start type NSTextListMarkerFormatsExtensions -->
<h3>New Type AppKit.NSTextListMarkerFormatsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTextListMarkerFormatsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSTextListMarkerFormats self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextListMarkerFormats GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormatsExtensions -->
<div> <!-- start type NSUserInterfaceCompressionOptions -->
<h3>New Type AppKit.NSUserInterfaceCompressionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class NSUserInterfaceCompressionOptions : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserInterfaceCompressionOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (Foundation.NSSet&lt;NSUserInterfaceCompressionOptions&gt; options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserInterfaceCompressionOptions (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions BreakEqualWidthsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Empty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideImagesOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideTextOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions ReduceMetricsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions StandardOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByAdding (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByRemoving (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Intersects (NSUserInterfaceCompressionOptions options);</span>
}
</pre>
</div> <!-- end type NSUserInterfaceCompressionOptions -->
<div> <!-- start type NSWindowTab -->
<h3>New Type AppKit.NSWindowTab</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTab : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTab ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTab (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTab (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView AccessoryView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ToolTip { get; set; }</span>
}
</pre>
</div> <!-- end type NSWindowTab -->
<div> <!-- start type NSWindowTabGroup -->
<h3>New Type AppKit.NSWindowTabGroup</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTabGroup : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTabGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTabGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool OverviewVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow SelectedWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TabBarVisible { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow[] Windows { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (NSWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Insert (NSWindow window, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Remove (NSWindow window);</span>
}
</pre>
</div> <!-- end type NSWindowTabGroup -->

</div> <!-- end namespace AppKit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKFetchRecordZoneChangesOptions --> <div>
<h3>Type Changed: CloudKit.CKFetchRecordZoneChangesOptions</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type CKFetchRecordZoneChangesOptions -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNErrorCode --> <div>
<h3>Type Changed: Contacts.CNErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierDoesNotExist = 601,</span>
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierInvalid = 600,</span>
</pre>
</div>

</div> <!-- end type CNErrorCode -->
<!-- start type CNLabelContactRelationKey --> <div>
<h3>Type Changed: Contacts.CNLabelContactRelationKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Daughter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Son { get; }</span>
</pre>
</div>

</div> <!-- end type CNLabelContactRelationKey -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CAAnimationGroup --> <div>
<h3>Type Changed: CoreAnimation.CAAnimationGroup</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimationGroup -->
<!-- start type CABasicAnimation --> <div>
<h3>Type Changed: CoreAnimation.CABasicAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CABasicAnimation -->
<!-- start type CAConstraint --> <div>
<h3>Type Changed: CoreAnimation.CAConstraint</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAConstraint -->
<!-- start type CAEmitterBehavior --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterBehavior</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterBehavior -->
<!-- start type CAEmitterCell --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterCell</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterCell -->
<!-- start type CAEmitterLayer --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterLayer -->
<!-- start type CAGradientLayer --> <div>
<h3>Type Changed: CoreAnimation.CAGradientLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAGradientLayer -->
<!-- start type CAKeyFrameAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAKeyFrameAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAKeyFrameAnimation -->
<!-- start type CALayer --> <div>
<h3>Type Changed: CoreAnimation.CALayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CALayer -->
<!-- start type CAMediaTimingFunction --> <div>
<h3>Type Changed: CoreAnimation.CAMediaTimingFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAMediaTimingFunction -->
<!-- start type CAMetalLayer --> <div>
<h3>Type Changed: CoreAnimation.CAMetalLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->
<!-- start type CAOpenGLLayer --> <div>
<h3>Type Changed: CoreAnimation.CAOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAOpenGLLayer -->
<!-- start type CAPropertyAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAPropertyAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAPropertyAnimation -->
<!-- start type CAReplicatorLayer --> <div>
<h3>Type Changed: CoreAnimation.CAReplicatorLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAReplicatorLayer -->
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: CoreAnimation.CAScrollLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<!-- start type CAShapeLayer --> <div>
<h3>Type Changed: CoreAnimation.CAShapeLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAShapeLayer -->
<!-- start type CASpringAnimation --> <div>
<h3>Type Changed: CoreAnimation.CASpringAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CASpringAnimation -->
<!-- start type CATextLayer --> <div>
<h3>Type Changed: CoreAnimation.CATextLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATextLayer -->
<!-- start type CATiledLayer --> <div>
<h3>Type Changed: CoreAnimation.CATiledLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATiledLayer -->
<!-- start type CATransformLayer --> <div>
<h3>Type Changed: CoreAnimation.CATransformLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransformLayer -->
<!-- start type CATransition --> <div>
<h3>Type Changed: CoreAnimation.CATransition</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransition -->
<!-- start type CAValueFunction --> <div>
<h3>Type Changed: CoreAnimation.CAValueFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAValueFunction -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreAudioKit --> <div> 
<h2>Namespace CoreAudioKit</h2>
<div> <!-- start type AUAudioUnitViewConfiguration -->
<h3>New Type CoreAudioKit.AUAudioUnitViewConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class AUAudioUnitViewConfiguration : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AUAudioUnitViewConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AUAudioUnitViewConfiguration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration (nfloat width, nfloat height, bool hostHasController);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HostHasController { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type AUAudioUnitViewConfiguration -->
<div> <!-- start type AUAudioUnitViewControllerExtensions -->
<h3>New Type CoreAudioKit.AUAudioUnitViewControllerExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AUAudioUnitViewControllerExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSIndexSet GetSupportedViewConfigurations (AudioUnit.AUAudioUnit This, AUAudioUnitViewConfiguration[] availableViewConfigurations);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SelectViewConfiguration (AudioUnit.AUAudioUnit This, AUAudioUnitViewConfiguration viewConfiguration);</span>
}
</pre>
</div> <!-- end type AUAudioUnitViewControllerExtensions -->

</div> <!-- end namespace CoreAudioKit -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type MigrationErrorType --> <div>
<h3>Type Changed: CoreData.MigrationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HistoryTokenExpired = 134301,</span>
</pre>
</div>

</div> <!-- end type MigrationErrorType -->
<!-- start type NSAttributeType --> <div>
<h3>Type Changed: CoreData.NSAttributeType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Uri = 1200,</span>
	<span class='added added-field ' data-is-non-breaking="">Uuid = 1100,</span>
</pre>
</div>

</div> <!-- end type NSAttributeType -->
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: CoreData.NSEntityDescription</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression CoreSpotlightDisplayNameExpression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription[] Indexes { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionAuthor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CoreSpotlightExporter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HistoryTrackingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UbiquitousContainerIdentifierKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator -->
<!-- start type NSQueryGenerationToken --> <div>
<h3>Type Changed: CoreData.NSQueryGenerationToken</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSQueryGenerationToken (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type NSQueryGenerationToken -->
<!-- start type ValidationErrorType --> <div>
<h3>Type Changed: CoreData.ValidationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidUri = 1690,</span>
</pre>
</div>

</div> <!-- end type ValidationErrorType -->
<div> <!-- start type NSFetchIndexDescription -->
<h3>New Type CoreData.NSFetchIndexDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (string name, NSFetchIndexElementDescription[] elements);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementDescription[] Elements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSEntityDescription Entity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate PartialIndexPredicate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexDescription -->
<div> <!-- start type NSFetchIndexElementDescription -->
<h3>New Type CoreData.NSFetchIndexElementDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexElementDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (NSPropertyDescription property, NSFetchIndexElementType collationType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementType CollationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription IndexDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAscending { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPropertyDescription Property { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PropertyName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementDescription -->
<div> <!-- start type NSFetchIndexElementType -->
<h3>New Type CoreData.NSFetchIndexElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFetchIndexElementType {
	<span class='added added-field ' data-is-non-breaking="">Binary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RTree = 1,</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementType -->
<div> <!-- start type NSPersistentHistoryChange -->
<h3>New Type CoreData.NSPersistentHistoryChange</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryChange : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual long ChangeId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChangeType ChangeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectID ChangedObjectId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary Tombstone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryTransaction Transaction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSPropertyDescription&gt; UpdatedProperties { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChange -->
<div> <!-- start type NSPersistentHistoryChangeRequest -->
<h3>New Type CoreData.NSPersistentHistoryChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryChangeRequest : CoreData.NSPersistentStoreRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (Foundation.NSDate date);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeRequest -->
<div> <!-- start type NSPersistentHistoryChangeType -->
<h3>New Type CoreData.NSPersistentHistoryChangeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryChangeType {
	<span class='added added-field ' data-is-non-breaking="">Delete = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Update = 1,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeType -->
<div> <!-- start type NSPersistentHistoryResult -->
<h3>New Type CoreData.NSPersistentHistoryResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryResult : CoreData.NSPersistentStoreResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Result { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; }</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResult -->
<div> <!-- start type NSPersistentHistoryResultType -->
<h3>New Type CoreData.NSPersistentHistoryResultType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryResultType {
	<span class='added added-field ' data-is-non-breaking="">ChangesOnly = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectIds = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusOnly = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsAndChanges = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsOnly = 3,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResultType -->
<div> <!-- start type NSPersistentHistoryToken -->
<h3>New Type CoreData.NSPersistentHistoryToken</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryToken : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryToken -->
<div> <!-- start type NSPersistentHistoryTransaction -->
<h3>New Type CoreData.NSPersistentHistoryTransaction</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryTransaction : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BundleId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChange[] Changes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContextName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNotification ObjectIdNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProcessId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StoreId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Timestamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long TransactionNumber { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryTransaction -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIImageAccumulator --> <div>
<h3>Type Changed: CoreImage.CIImageAccumulator</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CIImageAccumulator ();</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect extent, int format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect extent, int format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIImageAccumulator -->
<!-- start type CIQRCodeFeature --> <div>
<h3>Type Changed: CoreImage.CIQRCodeFeature</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeFeature (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type CIQRCodeFeature -->
<div> <!-- start type CIAreaMinMaxRed -->
<h3>New Type CoreImage.CIAreaMinMaxRed</h3>
<pre class='added' data-is-non-breaking="">
public class CIAreaMinMaxRed : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAreaMinMaxRed -->
<div> <!-- start type CIAttributedTextImageGenerator -->
<h3>New Type CoreImage.CIAttributedTextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIAttributedTextImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAttributedTextImageGenerator -->
<div> <!-- start type CIBarcodeGenerator -->
<h3>New Type CoreImage.CIBarcodeGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIBarcodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBarcodeGenerator -->
<div> <!-- start type CIBicubicScaleTransform -->
<h3>New Type CoreImage.CIBicubicScaleTransform</h3>
<pre class='added' data-is-non-breaking="">
public class CIBicubicScaleTransform : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBicubicScaleTransform -->
<div> <!-- start type CIBokehBlur -->
<h3>New Type CoreImage.CIBokehBlur</h3>
<pre class='added' data-is-non-breaking="">
public class CIBokehBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBokehBlur -->
<div> <!-- start type CIColorCubesMixedWithMask -->
<h3>New Type CoreImage.CIColorCubesMixedWithMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCubesMixedWithMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCubesMixedWithMask -->
<div> <!-- start type CIColorCurves -->
<h3>New Type CoreImage.CIColorCurves</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCurves : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCurves -->
<div> <!-- start type CIDepthBlurEffect -->
<h3>New Type CoreImage.CIDepthBlurEffect</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthBlurEffect : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthBlurEffect -->
<div> <!-- start type CIDepthToDisparity -->
<h3>New Type CoreImage.CIDepthToDisparity</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthToDisparity : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthToDisparity -->
<div> <!-- start type CIDisparityToDepth -->
<h3>New Type CoreImage.CIDisparityToDepth</h3>
<pre class='added' data-is-non-breaking="">
public class CIDisparityToDepth : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CILabDeltaE -->
<div> <!-- start type CIMorphologyGradient -->
<h3>New Type CoreImage.CIMorphologyGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyGradient : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyGradient -->
<div> <!-- start type CIMorphologyMaximum -->
<h3>New Type CoreImage.CIMorphologyMaximum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMaximum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMaximum -->
<div> <!-- start type CIMorphologyMinimum -->
<h3>New Type CoreImage.CIMorphologyMinimum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMinimum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMinimum -->
<div> <!-- start type CITextImageGenerator -->
<h3>New Type CoreImage.CITextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CITextImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CITextImageGenerator -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLGeocoder --> <div>
<h3>Type Changed: CoreLocation.CLGeocoder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLRegion region, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->
<!-- start type CLPlacemark --> <div>
<h3>Type Changed: CoreLocation.CLPlacemark</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Contacts.CNPostalAddress PostalAddress { get; }</span>
</pre>
</div>

</div> <!-- end type CLPlacemark -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
<!-- start type CMAttachmentBearer --> <div>
<h3>Type Changed: CoreMedia.CMAttachmentBearer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (ICMAttachmentBearer target, CMAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CMAttachmentBearer -->

</div> <!-- end namespace CoreMedia -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVBuffer --> <div>
<h3>Type Changed: CoreVideo.CVBuffer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (CVAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CVBuffer -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace EventKit --> <div> 
<h2>Namespace EventKit</h2>
<!-- start type EKAlarm --> <div>
<h3>Type Changed: EventKit.EKAlarm</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the static methods FromDate or FromTimeInterval to create alarms")]
	public EKAlarm ();</span>
</div></pre>

</div> <!-- end type EKAlarm -->
<!-- start type EKEventStore --> <div>
<h3>Type Changed: EventKit.EKEventStore</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public EKEventStore (EKSource[] sources);</span>
</pre>
</div>

</div> <!-- end type EKEventStore -->

</div> <!-- end namespace EventKit -->
<!-- start namespace FinderSync --> <div> 
<h2>Namespace FinderSync</h2>
<!-- start type FIFinderSync --> <div>
<h3>Type Changed: FinderSync.FIFinderSync</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetExportedObject (Foundation.NSFileProviderMessageInterface messageInterface, Foundation.NSUrl itemUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetValues (string[] attributes, Foundation.NSUrl itemUrl, GetValuesCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt;&gt; GetValuesAsync (string[] attributes, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] SupportedServiceNames (Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSync -->
<!-- start type FIFinderSyncController --> <div>
<h3>Type Changed: FinderSync.FIFinderSyncController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSDate GetLastUsedDate (Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetTagData (Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLastUsedDate (Foundation.NSDate lastUsedDate, Foundation.NSUrl itemUrl, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetLastUsedDateAsync (Foundation.NSDate lastUsedDate, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTagData (Foundation.NSData tagData, Foundation.NSUrl itemUrl, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetTagDataAsync (Foundation.NSData tagData, Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSyncController -->
<!-- start type FIFinderSyncProtocol_Extensions --> <div>
<h3>Type Changed: FinderSync.FIFinderSyncProtocol_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject GetExportedObject (IFIFinderSyncProtocol This, Foundation.NSFileProviderMessageInterface messageInterface, Foundation.NSUrl itemUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetValues (IFIFinderSyncProtocol This, string[] attributes, Foundation.NSUrl itemUrl, GetValuesCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt;&gt; GetValuesAsync (IFIFinderSyncProtocol This, string[] attributes, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] SupportedServiceNames (IFIFinderSyncProtocol This, Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSyncProtocol_Extensions -->
<div> <!-- start type GetValuesCompletionHandler -->
<h3>New Type FinderSync.GetValuesCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate GetValuesCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GetValuesCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; values, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; values, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type GetValuesCompletionHandler -->

</div> <!-- end namespace FinderSync -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSActivityOptions --> <div>
<h3>Type Changed: Foundation.NSActivityOptions</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	IdleDisplaySleepDisabled = <span class='removed removed-inline removed-breaking-inline'>256</span> <span class='added '>1099511627776</span>
</div></pre>

</div> <!-- end type NSActivityOptions -->
<!-- start type NSDimension --> <div>
<h3>Type Changed: Foundation.NSDimension</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">[Obsolete ("Not intended to be directly instantiated, this is an abstract class.")]
	public NSDimension ();</span>
</pre>
</div>

</div> <!-- end type NSDimension -->
<!-- start type NSFileManager --> <div>
<h3>Type Changed: Foundation.NSFileManager</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnmountVolume (NSUrl url, NSFileManagerUnmountOptions mask, System.Action&lt;NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UnmountVolumeAsync (NSUrl url, NSFileManagerUnmountOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSFileManager -->
<!-- start type NSUnit --> <div>
<h3>Type Changed: Foundation.NSUnit</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string)")]
	public NSUnit ();</span>
</div></pre>

</div> <!-- end type NSUnit -->
<!-- start type NSUnitAcceleration --> <div>
<h3>Type Changed: Foundation.NSUnitAcceleration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAcceleration ();</span>
</div></pre>

</div> <!-- end type NSUnitAcceleration -->
<!-- start type NSUnitAngle --> <div>
<h3>Type Changed: Foundation.NSUnitAngle</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAngle ();</span>
</div></pre>

</div> <!-- end type NSUnitAngle -->
<!-- start type NSUnitArea --> <div>
<h3>Type Changed: Foundation.NSUnitArea</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitArea ();</span>
</div></pre>

</div> <!-- end type NSUnitArea -->
<!-- start type NSUnitConcentrationMass --> <div>
<h3>Type Changed: Foundation.NSUnitConcentrationMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitConcentrationMass ();</span>
</div></pre>

</div> <!-- end type NSUnitConcentrationMass -->
<!-- start type NSUnitDispersion --> <div>
<h3>Type Changed: Foundation.NSUnitDispersion</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDispersion ();</span>
</div></pre>

</div> <!-- end type NSUnitDispersion -->
<!-- start type NSUnitDuration --> <div>
<h3>Type Changed: Foundation.NSUnitDuration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDuration ();</span>
</div></pre>

</div> <!-- end type NSUnitDuration -->
<!-- start type NSUnitElectricCharge --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCharge</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCharge ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCharge -->
<!-- start type NSUnitElectricCurrent --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCurrent</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCurrent ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCurrent -->
<!-- start type NSUnitElectricPotentialDifference --> <div>
<h3>Type Changed: Foundation.NSUnitElectricPotentialDifference</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricPotentialDifference ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricPotentialDifference -->
<!-- start type NSUnitElectricResistance --> <div>
<h3>Type Changed: Foundation.NSUnitElectricResistance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricResistance ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricResistance -->
<!-- start type NSUnitEnergy --> <div>
<h3>Type Changed: Foundation.NSUnitEnergy</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitEnergy ();</span>
</div></pre>

</div> <!-- end type NSUnitEnergy -->
<!-- start type NSUnitFrequency --> <div>
<h3>Type Changed: Foundation.NSUnitFrequency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFrequency ();</span>
</div></pre>

</div> <!-- end type NSUnitFrequency -->
<!-- start type NSUnitFuelEfficiency --> <div>
<h3>Type Changed: Foundation.NSUnitFuelEfficiency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFuelEfficiency ();</span>
</div></pre>

</div> <!-- end type NSUnitFuelEfficiency -->
<!-- start type NSUnitIlluminance --> <div>
<h3>Type Changed: Foundation.NSUnitIlluminance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitIlluminance ();</span>
</div></pre>

</div> <!-- end type NSUnitIlluminance -->
<!-- start type NSUnitLength --> <div>
<h3>Type Changed: Foundation.NSUnitLength</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitLength ();</span>
</div></pre>

</div> <!-- end type NSUnitLength -->
<!-- start type NSUnitMass --> <div>
<h3>Type Changed: Foundation.NSUnitMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitMass ();</span>
</div></pre>

</div> <!-- end type NSUnitMass -->
<!-- start type NSUnitPower --> <div>
<h3>Type Changed: Foundation.NSUnitPower</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPower ();</span>
</div></pre>

</div> <!-- end type NSUnitPower -->
<!-- start type NSUnitPressure --> <div>
<h3>Type Changed: Foundation.NSUnitPressure</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPressure ();</span>
</div></pre>

</div> <!-- end type NSUnitPressure -->
<!-- start type NSUnitSpeed --> <div>
<h3>Type Changed: Foundation.NSUnitSpeed</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitSpeed ();</span>
</div></pre>

</div> <!-- end type NSUnitSpeed -->
<!-- start type NSUnitVolume --> <div>
<h3>Type Changed: Foundation.NSUnitVolume</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitVolume ();</span>
</div></pre>

</div> <!-- end type NSUnitVolume -->
<!-- start type ProtocolAttribute --> <div>
<h3>Type Changed: Foundation.ProtocolAttribute</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string FormalSince { get; set; }</span>
</pre>
</div>

</div> <!-- end type ProtocolAttribute -->
<div> <!-- start type INSItemProviderReading -->
<h3>New Type Foundation.INSItemProviderReading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSItemProviderReading : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSItemProviderReading -->
<div> <!-- start type NSFileProviderMessageInterface -->
<h3>New Type Foundation.NSFileProviderMessageInterface</h3>
<pre class='added' data-is-non-breaking="">
public class NSFileProviderMessageInterface : Foundation.NSObject, INSCoding, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderMessageInterface (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderMessageInterface (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFileProviderMessageInterface -->
<div> <!-- start type NotImplementedAttribute -->
<h3>New Type Foundation.NotImplementedAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class NotImplementedAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NotImplementedAttribute ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NotImplementedAttribute (string message);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; set; }</span>
}
</pre>
</div> <!-- end type NotImplementedAttribute -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCMotion --> <div>
<h3>Type Changed: GameController.GCMotion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAttitudeAndRotationRate { get; }</span>
</pre>
</div>

</div> <!-- end type GCMotion -->

</div> <!-- end namespace GameController -->
<!-- start namespace LocalAuthentication --> <div> 
<h2>Namespace LocalAuthentication</h2>
<!-- start type LAContext --> <div>
<h3>Type Changed: LocalAuthentication.LAContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InteractionNotAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedReason { get; set; }</span>
</pre>
</div>

</div> <!-- end type LAContext -->
<!-- start type LAStatus --> <div>
<h3>Type Changed: LocalAuthentication.LAStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NotInteractive = -1004,</span>
</pre>
</div>

</div> <!-- end type LAStatus -->

</div> <!-- end namespace LocalAuthentication -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKAnnotationView --> <div>
<h3>Type Changed: MapKit.MKAnnotationView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationView ClusterAnnotationView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ClusteringIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationViewCollisionMode CollisionMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float DisplayPriority { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareForDisplay ();</span>
</pre>
</div>

</div> <!-- end type MKAnnotationView -->
<!-- start type MKMapItem --> <div>
<h3>Type Changed: MapKit.MKMapItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MKMapItem -->
<!-- start type MKMapType --> <div>
<h3>Type Changed: MapKit.MKMapType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MutedStandard = 5,</span>
</pre>
</div>

</div> <!-- end type MKMapType -->
<!-- start type MKMapView --> <div>
<h3>Type Changed: MapKit.MKMapView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MKCreateClusterAnnotation CreateClusterAnnotation { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKAnnotationView DequeueReusableAnnotation (string identifier, IMKAnnotation annotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Register (ObjCRuntime.Class viewClass, string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Register (System.Type viewType, string identifier);</span>
</pre>
</div>

</div> <!-- end type MKMapView -->
<!-- start type MKMapViewDelegate --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation CreateClusterAnnotation (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate -->
<!-- start type MKMapViewDelegate_Extensions --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MKClusterAnnotation CreateClusterAnnotation (IMKMapViewDelegate This, MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate_Extensions -->
<!-- start type MKPlacemark --> <div>
<h3>Type Changed: MapKit.MKPlacemark</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate, Contacts.CNPostalAddress postalAddress);</span>
</pre>
</div>

</div> <!-- end type MKPlacemark -->
<div> <!-- start type MKAnnotationViewCollisionMode -->
<h3>New Type MapKit.MKAnnotationViewCollisionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKAnnotationViewCollisionMode {
	<span class='added added-field ' data-is-non-breaking="">Circle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Rectangle = 0,</span>
}
</pre>
</div> <!-- end type MKAnnotationViewCollisionMode -->
<div> <!-- start type MKClusterAnnotation -->
<h3>New Type MapKit.MKClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public class MKClusterAnnotation : Foundation.NSObject, Foundation.INSObjectProtocol, IMKAnnotation, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKClusterAnnotation (IMKAnnotation[] memberAnnotations);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMKAnnotation[] MemberAnnotations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Subtitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCoordinate (CoreLocation.CLLocationCoordinate2D value);</span>
}
</pre>
</div> <!-- end type MKClusterAnnotation -->
<div> <!-- start type MKCreateClusterAnnotation -->
<h3>New Type MapKit.MKCreateClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MKCreateClusterAnnotation : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKCreateClusterAnnotation (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, IMKAnnotation[] memberAnnotations, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation Invoke (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
}
</pre>
</div> <!-- end type MKCreateClusterAnnotation -->
<div> <!-- start type MKFeatureDisplayPriority -->
<h3>New Type MapKit.MKFeatureDisplayPriority</h3>
<pre class='added' data-is-non-breaking="">
public static class MKFeatureDisplayPriority {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultHigh;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultLow;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float Required;</span>
}
</pre>
</div> <!-- end type MKFeatureDisplayPriority -->
<div> <!-- start type MKFeatureVisibility -->
<h3>New Type MapKit.MKFeatureVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKFeatureVisibility {
	<span class='added added-field ' data-is-non-breaking="">Adaptive = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hidden = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Visible = 2,</span>
}
</pre>
</div> <!-- end type MKFeatureVisibility -->
<div> <!-- start type MKMapViewDefault -->
<h3>New Type MapKit.MKMapViewDefault</h3>
<pre class='added' data-is-non-breaking="">
public static class MKMapViewDefault {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationViewReuseIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ClusterAnnotationViewReuseIdentifier { get; }</span>
}
</pre>
</div> <!-- end type MKMapViewDefault -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaLibrary --> <div> 
<h2>Namespace MediaLibrary</h2>
<!-- start type MediaLibraryTypeIdentifierKey --> <div>
<h3>Type Changed: MediaLibrary.MediaLibraryTypeIdentifierKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosAnimatedGroupTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosLivePhotosGroupTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosLongExposureGroupTypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MediaLibraryTypeIdentifierKey -->

</div> <!-- end namespace MediaLibrary -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.12"</span> <span class='added '>"10.13"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"3.4.0"</span> <span class='added '>"3.99.1"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VisionLibrary = "/System/Library/Frameworks/Vision.framework/Vision";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetUInt32 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetUInt64 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNFloat (IntPtr handle, string symbol, nfloat value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNInt (IntPtr handle, string symbol, nint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNUInt (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt32 (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt64 (IntPtr handle, string symbol, long value);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHContentEditingInput --> <div>
<h3>Type Changed: Photos.PHContentEditingInput</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage DisplaySizeImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
</pre>
</div>

</div> <!-- end type PHContentEditingInput -->
<!-- start type PHLivePhotoEditingContext --> <div>
<h3>Type Changed: Photos.PHLivePhotoEditingContext</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, PHLivePhotoEditingOption options, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output, PHLivePhotoEditingOption options);</span>
</pre>
</div>

</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type IPHContentEditingController -->
<h3>New Type Photos.IPHContentEditingController</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHContentEditingController : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldShowCancelConfirmation { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanHandleAdjustmentData (PHAdjustmentData adjustmentData);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelContentEditing ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishContentEditing (System.Action&lt;PHContentEditingOutput&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartContentEditing (PHContentEditingInput contentEditingInput, AppKit.NSImage placeholderImage);</span>
}
</pre>
</div> <!-- end type IPHContentEditingController -->
<div> <!-- start type IPHPhotoLibraryChangeObserver -->
<h3>New Type Photos.IPHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHPhotoLibraryChangeObserver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type IPHPhotoLibraryChangeObserver -->
<div> <!-- start type IPHProjectExtensionController -->
<h3>New Type Photos.IPHProjectExtensionController</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHProjectExtensionController : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginProject (PHProjectExtensionContext extensionContext, PHProjectInfo projectInfo, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishProject (System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ResumeProject (PHProjectExtensionContext extensionContext, System.Action&lt;Foundation.NSError&gt; completion);</span>
}
</pre>
</div> <!-- end type IPHProjectExtensionController -->
<div> <!-- start type PHAsset -->
<h3>New Type Photos.PHAsset</h3>
<pre class='added' data-is-non-breaking="">
public class PHAsset : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAsset ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string BurstIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetBurstSelectionType BurstSelectionTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Favorite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LocalIdentifierNotFound { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaSubtype MediaSubtypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaType MediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ModificationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RepresentsBurst { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType SourceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SyncFailureHidden { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHAssetEditOperation editOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetMediaType mediaType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (string burstIdentifier, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetsUsingLocalIdentifiers (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchKeyAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHAsset -->
<div> <!-- start type PHAssetCollection -->
<h3>New Type Photos.PHAssetCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetCollection : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetCollection ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation ApproximateLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionSubtype AssetCollectionSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionType AssetCollectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint EstimatedAssetCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (Foundation.NSUrl[] assetGroupUrls, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAsset asset, PHAssetCollectionType type, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAssetCollectionType type, PHAssetCollectionSubtype subtype, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHCollectionList momentList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHAsset[] assets, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHFetchResult fetchResult, string title);</span>
}
</pre>
</div> <!-- end type PHAssetCollection -->
<div> <!-- start type PHAssetImageProgressHandler -->
<h3>New Type Photos.PHAssetImageProgressHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHAssetImageProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetImageProgressHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (double progress, Foundation.NSError error, bool stop, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (double progress, Foundation.NSError error, bool stop, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHAssetImageProgressHandler -->
<div> <!-- start type PHAssetPlaybackStyle -->
<h3>New Type Photos.PHAssetPlaybackStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetPlaybackStyle {
	<span class='added added-field ' data-is-non-breaking="">Image = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageAnimated = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LivePhoto = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoLooping = 5,</span>
}
</pre>
</div> <!-- end type PHAssetPlaybackStyle -->
<div> <!-- start type PHAuthorizationStatus -->
<h3>New Type Photos.PHAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type PHAuthorizationStatus -->
<div> <!-- start type PHChange -->
<h3>New Type Photos.PHChange</h3>
<pre class='added' data-is-non-breaking="">
public class PHChange : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual PHFetchResultChangeDetails GetFetchResultChangeDetails (PHFetchResult obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PHObjectChangeDetails GetObjectChangeDetails (PHObject obj);</span>
}
</pre>
</div> <!-- end type PHChange -->
<div> <!-- start type PHChangeDetailEnumerator -->
<h3>New Type Photos.PHChangeDetailEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHChangeDetailEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChangeDetailEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (uint fromIndex, uint toIndex, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (uint fromIndex, uint toIndex);</span>
}
</pre>
</div> <!-- end type PHChangeDetailEnumerator -->
<div> <!-- start type PHCloudIdentifier -->
<h3>New Type Photos.PHCloudIdentifier</h3>
<pre class='added' data-is-non-breaking="">
public class PHCloudIdentifier : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCloudIdentifier (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCloudIdentifier (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier (string stringValue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHCloudIdentifier NotFoundIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHCloudIdentifier -->
<div> <!-- start type PHCollection -->
<h3>New Type Photos.PHCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollection : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainAssets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainCollections { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHCollectionEditOperation anOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollections (PHCollectionList collectionList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchTopLevelUserCollections (PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollection -->
<div> <!-- start type PHCollectionList -->
<h3>New Type Photos.PHCollectionList</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollectionList : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCollectionList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListSubtype CollectionListSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListType CollectionListType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHAssetCollection[] collections, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHFetchResult fetchResult, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollection collection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollectionListType type, PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHAssetCollection moment, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollectionList -->
<div> <!-- start type PHFetchOptions -->
<h3>New Type Photos.PHFetchOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FetchLimit { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeAllBurstAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType IncludeAssetSourceTypes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeHiddenAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate Predicate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSortDescriptor[] SortDescriptors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsIncrementalChangeDetails { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHFetchOptions -->
<div> <!-- start type PHFetchResult -->
<h3>New Type Photos.PHFetchResult</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResult : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject LastObject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject firstObject { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint CountOfAssetsWithMediaType (PHAssetMediaType mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSIndexSet idx, Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id, Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAt (nint index);</span>
}
</pre>
</div> <!-- end type PHFetchResult -->
<div> <!-- start type PHFetchResultChangeDetails -->
<h3>New Type Photos.PHFetchResultChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResultChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet ChangedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] ChangedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasIncrementalChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasMoves { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet InsertedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] InsertedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet RemovedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] RemovedObjects { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResultChangeDetails ChangeDetails (PHFetchResult fromResult, PHFetchResult toResult, PHObject[] changedObjects);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateMoves (PHChangeDetailEnumerator handler);</span>
}
</pre>
</div> <!-- end type PHFetchResultChangeDetails -->
<div> <!-- start type PHFetchResultEnumerator -->
<h3>New Type Photos.PHFetchResultEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHFetchResultEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSObject element, uint elementIndex, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSObject element, uint elementIndex, bool stop);</span>
}
</pre>
</div> <!-- end type PHFetchResultEnumerator -->
<div> <!-- start type PHImageDataHandler -->
<h3>New Type Photos.PHImageDataHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageDataHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData data, Foundation.NSString dataUti, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData data, Foundation.NSString dataUti, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageDataHandler -->
<div> <!-- start type PHImageKeys -->
<h3>New Type Photos.PHImageKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PHImageKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Cancelled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsDegraded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsInCloud { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultRequestID { get; }</span>
}
</pre>
</div> <!-- end type PHImageKeys -->
<div> <!-- start type PHImageManager -->
<h3>New Type Photos.PHImageManager</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHImageManager DefaultManager { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGSize MaximumSize { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelImageRequest (int requestID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageData (PHAsset asset, PHImageRequestOptions options, PHImageDataHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageForAsset (PHAsset asset, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHImageRequestOptions options, PHImageResultHandler resultHandler);</span>
}
</pre>
</div> <!-- end type PHImageManager -->
<div> <!-- start type PHImageRequestOptions -->
<h3>New Type Photos.PHImageRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageRequestOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect NormalizedCropRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsResizeMode ResizeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Synchronous { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsVersion Version { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHImageRequestOptions -->
<div> <!-- start type PHImageRequestOptionsDeliveryMode -->
<h3>New Type Photos.PHImageRequestOptionsDeliveryMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsDeliveryMode {
	<span class='added added-field ' data-is-non-breaking="">FastFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HighQualityFormat = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Opportunistic = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsDeliveryMode -->
<div> <!-- start type PHImageRequestOptionsResizeMode -->
<h3>New Type Photos.PHImageRequestOptionsResizeMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsResizeMode {
	<span class='added added-field ' data-is-non-breaking="">Exact = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsResizeMode -->
<div> <!-- start type PHImageRequestOptionsVersion -->
<h3>New Type Photos.PHImageRequestOptionsVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsVersion {
	<span class='added added-field ' data-is-non-breaking="">Current = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Original = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unadjusted = 1,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsVersion -->
<div> <!-- start type PHImageResultHandler -->
<h3>New Type Photos.PHImageResultHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageResultHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageResultHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AppKit.NSImage result, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (AppKit.NSImage result, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageResultHandler -->
<div> <!-- start type PHLivePhotoEditingOption -->
<h3>New Type Photos.PHLivePhotoEditingOption</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoEditingOption : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? ShouldRenderAtPlaybackTime { get; }</span>
}
</pre>
</div> <!-- end type PHLivePhotoEditingOption -->
<div> <!-- start type PHObject -->
<h3>New Type Photos.PHObject</h3>
<pre class='added' data-is-non-breaking="">
public class PHObject : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHObject -->
<div> <!-- start type PHObjectChangeDetails -->
<h3>New Type Photos.PHObjectChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHObjectChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHObjectChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AssetContentChanged { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ObjectWasDeleted { get; }</span>
}
</pre>
</div> <!-- end type PHObjectChangeDetails -->
<div> <!-- start type PHPhotoLibrary -->
<h3>New Type Photos.PHPhotoLibrary</h3>
<pre class='added' data-is-non-breaking="">
public class PHPhotoLibrary : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static PHAuthorizationStatus AuthorizationStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHPhotoLibrary SharedPhotoLibrary { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformChanges (System.Action changeHandler, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PerformChangesAndWait (System.Action changeHandler, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestAuthorization (System.Action&lt;PHAuthorizationStatus&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;PHAuthorizationStatus&gt; RequestAuthorizationAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnregisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary -->
<div> <!-- start type PHPhotoLibraryChangeObserver -->
<h3>New Type Photos.PHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public abstract class PHPhotoLibraryChangeObserver : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IPHPhotoLibraryChangeObserver, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type PHPhotoLibraryChangeObserver -->
<div> <!-- start type PHPhotoLibrary_CloudIdentifiers -->
<h3>New Type Photos.PHPhotoLibrary_CloudIdentifiers</h3>
<pre class='added' data-is-non-breaking="">
public static class PHPhotoLibrary_CloudIdentifiers {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCloudIdentifier[] GetCloudIdentifiers (PHPhotoLibrary This, string[] localIdentifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetLocalIdentifiers (PHPhotoLibrary This, PHCloudIdentifier[] cloudIdentifiers);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary_CloudIdentifiers -->
<div> <!-- start type PHProject -->
<h3>New Type Photos.PHProject</h3>
<pre class='added' data-is-non-breaking="">
public class PHProject : Photos.PHAssetCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProject ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ProjectExtensionData { get; }</span>
}
</pre>
</div> <!-- end type PHProject -->
<div> <!-- start type PHProjectAssetElement -->
<h3>New Type Photos.PHProjectAssetElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectAssetElement : Photos.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectAssetElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectAssetElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectAssetElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectAssetElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Annotation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCloudIdentifier CloudAssetIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect CropRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectRegionOfInterest[] RegionsOfInterest { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectAssetElement -->
<div> <!-- start type PHProjectChangeRequest -->
<h3>New Type Photos.PHProjectChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectChangeRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectChangeRequest ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectChangeRequest (PHProject project);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ProjectExtensionData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetKeyAsset (PHAsset keyAsset);</span>
}
</pre>
</div> <!-- end type PHProjectChangeRequest -->
<div> <!-- start type PHProjectCreationSource -->
<h3>New Type Photos.PHProjectCreationSource</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectCreationSource {
	<span class='added added-field ' data-is-non-breaking="">Album = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Memory = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Moment = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Project = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectBook = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectCalendar = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectCard = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectExtension = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectPrintOrder = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectSlideshow = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserSelection = 1,</span>
}
</pre>
</div> <!-- end type PHProjectCreationSource -->
<div> <!-- start type PHProjectElement -->
<h3>New Type Photos.PHProjectElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectElement : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Placement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectElement -->
<div> <!-- start type PHProjectExtensionContext -->
<h3>New Type Photos.PHProjectExtensionContext</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectExtensionContext : Foundation.NSExtensionContext, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectExtensionContext ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectExtensionContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectExtensionContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHPhotoLibrary PhotoLibrary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProject Project { get; }</span>
}
</pre>
</div> <!-- end type PHProjectExtensionContext -->
<div> <!-- start type PHProjectExtensionController_Extensions -->
<h3>New Type Photos.PHProjectExtensionController_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PHProjectExtensionController_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHProjectTypeDescription[] GetSupportedProjectTypes (IPHProjectExtensionController This);</span>
}
</pre>
</div> <!-- end type PHProjectExtensionController_Extensions -->
<div> <!-- start type PHProjectInfo -->
<h3>New Type Photos.PHProjectInfo</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectInfo : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectInfo (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectInfo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectInfo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectCreationSource CreationSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ProjectType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSection[] Sections { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectInfo -->
<div> <!-- start type PHProjectJournalEntryElement -->
<h3>New Type Photos.PHProjectJournalEntryElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectJournalEntryElement : Photos.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectJournalEntryElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectJournalEntryElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectJournalEntryElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectJournalEntryElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectAssetElement AssetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Date { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTextElement TextElement { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectJournalEntryElement -->
<div> <!-- start type PHProjectRegionOfInterest -->
<h3>New Type Photos.PHProjectRegionOfInterest</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectRegionOfInterest : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectRegionOfInterest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectRegionOfInterest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectRegionOfInterest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectRegionOfInterest -->
<div> <!-- start type PHProjectSection -->
<h3>New Type Photos.PHProjectSection</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectSection : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectSection (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSectionContent[] SectionContents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSectionType SectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectSection -->
<div> <!-- start type PHProjectSectionContent -->
<h3>New Type Photos.PHProjectSectionContent</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectSectionContent : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectSectionContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSectionContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSectionContent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double AspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCloudIdentifier[] CloudAssetIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectElement[] Elements { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfColumns { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectSectionContent -->
<div> <!-- start type PHProjectSectionType -->
<h3>New Type Photos.PHProjectSectionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectSectionType {
	<span class='added added-field ' data-is-non-breaking="">Auxiliary = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Content = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Cover = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type PHProjectSectionType -->
<div> <!-- start type PHProjectTextElement -->
<h3>New Type Photos.PHProjectTextElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectTextElement : Photos.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTextElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTextElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTextElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTextElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Text { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTextElementType TextElementType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectTextElement -->
<div> <!-- start type PHProjectTextElementType -->
<h3>New Type Photos.PHProjectTextElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectTextElementType {
	<span class='added added-field ' data-is-non-breaking="">Body = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtitle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Title = 1,</span>
}
</pre>
</div> <!-- end type PHProjectTextElementType -->
<div> <!-- start type PHProjectType -->
<h3>New Type Photos.PHProjectType</h3>
<pre class='added' data-is-non-breaking="">
public static class PHProjectType {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Undefined { get; }</span>
}
</pre>
</div> <!-- end type PHProjectType -->
<div> <!-- start type PHProjectTypeDescription -->
<h3>New Type Photos.PHProjectTypeDescription</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectTypeDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTypeDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTypeDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSString projectType, string localizedTitle, string localizedDescription, AppKit.NSImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSString projectType, string localizedTitle, string localizedDescription, AppKit.NSImage image, PHProjectTypeDescription[] subtypeDescriptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ProjectType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTypeDescription[] SubtypeDescriptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectTypeDescription -->

</div> <!-- end namespace Photos -->
<!-- start namespace QTKit --> <div> 
<h2>Namespace QTKit</h2>
<!-- start type QTCaptureLayer --> <div>
<h3>Type Changed: QTKit.QTCaptureLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTCaptureLayer -->
<!-- start type QTMovieLayer --> <div>
<h3>Type Changed: QTKit.QTMovieLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTMovieLayer -->

</div> <!-- end namespace QTKit -->
<!-- start namespace QuartzComposer --> <div> 
<h2>Namespace QuartzComposer</h2>
<!-- start type QCCompositionLayer --> <div>
<h3>Type Changed: QuartzComposer.QCCompositionLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QCCompositionLayer -->

</div> <!-- end namespace QuartzComposer -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNLayer --> <div>
<h3>Type Changed: SceneKit.SCNLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type SCNLayer -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_8_SHA256 = 4869,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_SHA256 = 4868,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_GCM_SHA256 = 4865,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_256_GCM_SHA384 = 4866,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_CHACHA20_POLY1305_SHA256 = 4867,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->

</div> <!-- end namespace Security -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKLabelNode --> <div>
<h3>Type Changed: SpriteKit.SKLabelNode</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSLineBreakMode LineBreakMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfLines { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredMaxLayoutWidth { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKLabelNode FromText (Foundation.NSAttributedString attributedText);</span>
</pre>
</div>

</div> <!-- end type SKLabelNode -->
<div> <!-- start type SKNodeFocusBehavior -->
<h3>New Type SpriteKit.SKNodeFocusBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKNodeFocusBehavior {
	<span class='added added-field ' data-is-non-breaking="">Focusable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Occluding = 1,</span>
}
</pre>
</div> <!-- end type SKNodeFocusBehavior -->
<div> <!-- start type SKRenderer -->
<h3>New Type SpriteKit.SKRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class SKRenderer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IgnoresSiblingOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKScene Scene { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldCullNonVisibleNodes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsDrawCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsFields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsNodeCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsPhysics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsQuadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKRenderer FromDevice (Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLCommandBuffer commandBuffer, Metal.MTLRenderPassDescriptor renderPassDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLRenderCommandEncoder renderCommandEncoder, Metal.MTLRenderPassDescriptor renderPassDescriptor, Metal.IMTLCommandQueue commandQueue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (double currentTime);</span>
}
</pre>
</div> <!-- end type SKRenderer -->
<div> <!-- start type SKTransformNode -->
<h3>New Type SpriteKit.SKTransformNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKTransformNode : SpriteKit.SKNode, AppKit.INSTouchBarProvider, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 EulerAngles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Quaternion Quaternion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 RotationMatrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat XRotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat YRotation { get; set; }</span>
}
</pre>
</div> <!-- end type SKTransformNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKErrorCode --> <div>
<h3>Type Changed: WebKit.WKErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreCompileFailed = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreLookUpFailed = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreRemoveFailed = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreVersionMismatch = 9,</span>
</pre>
</div>

</div> <!-- end type WKErrorCode -->
<!-- start type WKFrameInfo --> <div>
<h3>Type Changed: WebKit.WKFrameInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKWebView WebView { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type WKFrameInfo -->
<!-- start type WKUserContentController --> <div>
<h3>Type Changed: WebKit.WKUserContentController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddContentRuleList (WKContentRuleList contentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllContentRuleLists ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (WKContentRuleList contentRuleList);</span>
</pre>
</div>

</div> <!-- end type WKUserContentController -->
<!-- start type WKWebView --> <div>
<h3>Type Changed: WebKit.WKWebView</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool HandlesUrlScheme (string urlScheme);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TakeSnapshot (WKSnapshotConfiguration snapshotConfiguration, System.Action&lt;AppKit.NSImage,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AppKit.NSImage&gt; TakeSnapshotAsync (WKSnapshotConfiguration snapshotConfiguration);</span>
</pre>
</div>

</div> <!-- end type WKWebView -->
<!-- start type WKWebViewConfiguration --> <div>
<h3>Type Changed: WebKit.WKWebViewConfiguration</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWKUrlSchemeHandler GetUrlSchemeHandler (string urlScheme);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetUrlSchemeHandler (IWKUrlSchemeHandler urlSchemeHandler, string urlScheme);</span>
</pre>
</div>

</div> <!-- end type WKWebViewConfiguration -->
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKHttpCookieStore HttpCookieStore { get; }</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->
<!-- start type WebView --> <div>
<h3>Type Changed: WebKit.WebView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSelectedDomRange (DomRange range, AppKit.NSSelectionAffinity selectionAffinity);</span>
</pre>
</div>

</div> <!-- end type WebView -->
<div> <!-- start type IWKHttpCookieStoreObserver -->
<h3>New Type WebKit.IWKHttpCookieStoreObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKHttpCookieStoreObserver : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IWKHttpCookieStoreObserver -->
<div> <!-- start type IWKUrlSchemeHandler -->
<h3>New Type WebKit.IWKUrlSchemeHandler</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeHandler : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartUrlSchemeTask (WKWebView webView, IWKUrlSchemeTask urlSchemeTask);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopUrlSchemeTask (WKWebView webView, IWKUrlSchemeTask urlSchemeTask);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeHandler -->
<div> <!-- start type IWKUrlSchemeTask -->
<h3>New Type WebKit.IWKUrlSchemeTask</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeTask : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrlRequest Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFailWithError (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveData (Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveResponse (Foundation.NSUrlResponse response);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeTask -->
<div> <!-- start type WKContentRuleList -->
<h3>New Type WebKit.WKContentRuleList</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleList : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type WKContentRuleList -->
<div> <!-- start type WKContentRuleListStore -->
<h3>New Type WebKit.WKContentRuleListStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleListStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleListStore ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleListStore (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleListStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static WKContentRuleListStore DefaultStore { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CompileContentRuleList (string identifier, string encodedContentRuleList, System.Action&lt;WKContentRuleList,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; CompileContentRuleListAsync (string identifier, string encodedContentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public static WKContentRuleListStore FromUrl (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAvailableContentRuleListIdentifiers (System.Action&lt;System.String[]&gt; callback);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; GetAvailableContentRuleListIdentifiersAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LookUpContentRuleList (string identifier, System.Action&lt;WKContentRuleList,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; LookUpContentRuleListAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RemoveContentRuleListAsync (string identifier);</span>
}
</pre>
</div> <!-- end type WKContentRuleListStore -->
<div> <!-- start type WKHttpCookieStore -->
<h3>New Type WebKit.WKHttpCookieStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKHttpCookieStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected WKHttpCookieStore (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKHttpCookieStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeleteCookie (Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DeleteCookieAsync (Foundation.NSHttpCookie cookie);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAllCookies (System.Action&lt;Foundation.NSHttpCookie[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSHttpCookie[]&gt; GetAllCookiesAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCookie (Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetCookieAsync (Foundation.NSHttpCookie cookie);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStore -->
<div> <!-- start type WKHttpCookieStoreObserver_Extensions -->
<h3>New Type WebKit.WKHttpCookieStoreObserver_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class WKHttpCookieStoreObserver_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CookiesDidChangeInCookieStore (IWKHttpCookieStoreObserver This, WKHttpCookieStore cookieStore);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStoreObserver_Extensions -->
<div> <!-- start type WKSnapshotConfiguration -->
<h3>New Type WebKit.WKSnapshotConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class WKSnapshotConfiguration : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKSnapshotConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKSnapshotConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKSnapshotConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber SnapshotWidth { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type WKSnapshotConfiguration -->

</div> <!-- end namespace WebKit -->
<!-- start namespace CoreML --> <div> 
<h2>New Namespace CoreML</h2>

<div> <!-- start type IMLFeatureProvider -->
<h3>New Type CoreML.IMLFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMLFeatureProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type IMLFeatureProvider -->
<div> <!-- start type MLDictionaryFeatureProvider -->
<h3>New Type CoreML.MLDictionaryFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryFeatureProvider : Foundation.NSObject, IMLFeatureProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; dictionary, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureValue&gt; Dictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLFeatureValue Item { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type MLDictionaryFeatureProvider -->
<div> <!-- start type MLFeatureDescription -->
<h3>New Type CoreML.MLFeatureDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureDescription : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Optional { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAllowed (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureDescription -->
<div> <!-- start type MLFeatureType -->
<h3>New Type CoreML.MLFeatureType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLFeatureType {
	<span class='added added-field ' data-is-non-breaking="">Dictionary = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Double = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Int64 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiArray = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 3,</span>
}
</pre>
</div> <!-- end type MLFeatureType -->
<div> <!-- start type MLFeatureValue -->
<h3>New Type CoreML.MLFeatureValue</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureValue : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureValue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; DictionaryValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double DoubleValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer ImageBufferValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long Int64Value { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArray MultiArrayValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Undefined { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue CreateUndefined (MLFeatureType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromDictionary (Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; value, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromDouble (double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromInt64 (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromMultiArray (MLMultiArray value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromPixelBuffer (CoreVideo.CVPixelBuffer value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromString (string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqual (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureValue -->
<div> <!-- start type MLModel -->
<h3>New Type CoreML.MLModel</h3>
<pre class='added' data-is-non-breaking="">
public class MLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLModelDescription ModelDescription { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MLModel FromUrl (Foundation.NSUrl url, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MLModel -->
<div> <!-- start type MLModelDescription -->
<h3>New Type CoreML.MLModelDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelDescription : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; InputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLModelMetadata Metadata { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; OutputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedFeatureName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedProbabilitiesName { get; }</span>
}
</pre>
</div> <!-- end type MLModelDescription -->
<div> <!-- start type MLModelError -->
<h3>New Type CoreML.MLModelError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLModelError {
	<span class='added added-field ' data-is-non-breaking="">DescriptionMismatch = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FeatureType = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Generic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Io = 3,</span>
}
</pre>
</div> <!-- end type MLModelError -->
<div> <!-- start type MLModelErrorExtensions -->
<h3>New Type CoreML.MLModelErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MLModelErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (MLModelError self);</span>
}
</pre>
</div> <!-- end type MLModelErrorExtensions -->
<div> <!-- start type MLModelMetadata -->
<h3>New Type CoreML.MLModelMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelMetadata : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Description { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string License { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string VersionString { get; }</span>
}
</pre>
</div> <!-- end type MLModelMetadata -->
<div> <!-- start type MLMultiArray -->
<h3>New Type CoreML.MLMultiArray</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSError error);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (IntPtr dataPointer, Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSNumber[] strides, System.Action&lt;IntPtr&gt; deallocator, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr DataPointer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Shape { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Strides { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (nint idx);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, nint idx);</span>
}
</pre>
</div> <!-- end type MLMultiArray -->
<div> <!-- start type MLMultiArrayDataType -->
<h3>New Type CoreML.MLMultiArrayDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLMultiArrayDataType {
	<span class='added added-field ' data-is-non-breaking="">Double = 65600,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 65568,</span>
	<span class='added added-field ' data-is-non-breaking="">Int32 = 131104,</span>
}
</pre>
</div> <!-- end type MLMultiArrayDataType -->
</div> <!-- end namespace CoreML -->

<!-- start namespace Vision --> <div> 
<h2>New Namespace Vision</h2>

<div> <!-- start type IVNFaceObservationAccepting -->
<h3>New Type Vision.IVNFaceObservationAccepting</h3>
<pre class='added' data-is-non-breaking="">
public interface IVNFaceObservationAccepting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type IVNFaceObservationAccepting -->
<div> <!-- start type VNBarcodeObservation -->
<h3>New Type Vision.VNBarcodeObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNBarcodeObservation : Vision.VNRectangleObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Symbology { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNBarcodeObservation -->
<div> <!-- start type VNBarcodeSymbology -->
<h3>New Type Vision.VNBarcodeSymbology</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNBarcodeSymbology {
	<span class='added added-field ' data-is-non-breaking="">Aztec = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Code128 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39Checksum = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAscii = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAsciiChecksum = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93i = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DataMatrix = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean13 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean8 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5Checksum = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Itf14 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Pdf417 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">QR = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Upce = 16,</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbology -->
<div> <!-- start type VNBarcodeSymbologyExtensions -->
<h3>New Type Vision.VNBarcodeSymbologyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNBarcodeSymbologyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (VNBarcodeSymbology self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbologyExtensions -->
<div> <!-- start type VNClassificationObservation -->
<h3>New Type Vision.VNClassificationObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNClassificationObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNClassificationObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type VNClassificationObservation -->
<div> <!-- start type VNCoreMLFeatureValueObservation -->
<h3>New Type Vision.VNCoreMLFeatureValueObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLFeatureValueObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLFeatureValueObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreML.MLFeatureValue FeatureValue { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLFeatureValueObservation -->
<div> <!-- start type VNCoreMLModel -->
<h3>New Type Vision.VNCoreMLModel</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNCoreMLModel FromMLModel (CoreML.MLModel model, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNCoreMLModel -->
<div> <!-- start type VNCoreMLRequest -->
<h3>New Type Vision.VNCoreMLRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNImageCropAndScaleOption ImageCropAndScaleOption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNCoreMLModel Model { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLRequest -->
<div> <!-- start type VNDetectBarcodesRequest -->
<h3>New Type Vision.VNDetectBarcodesRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNDetectBarcodesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectBarcodesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string[] SupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Symbologies { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectBarcodesRequest -->
<div> <!-- start type VNDetectFaceLandmarksRequest -->
<h3>New Type Vision.VNDetectFaceLandmarksRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceLandmarksRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IVNFaceObservationAccepting {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceLandmarksRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceLandmarksRequest -->
<div> <!-- start type VNDetectFaceRectanglesRequest -->
<h3>New Type Vision.VNDetectFaceRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceRectanglesRequest -->
<div> <!-- start type VNDetectHorizonRequest -->
<h3>New Type Vision.VNDetectHorizonRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectHorizonRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectHorizonRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectHorizonRequest -->
<div> <!-- start type VNDetectRectanglesRequest -->
<h3>New Type Vision.VNDetectRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumObservations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumConfidence { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float QuadratureTolerance { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectRectanglesRequest -->
<div> <!-- start type VNDetectTextRectanglesRequest -->
<h3>New Type Vision.VNDetectTextRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectTextRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectTextRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReportCharacterBoxes { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectTextRectanglesRequest -->
<div> <!-- start type VNDetectedObjectObservation -->
<h3>New Type Vision.VNDetectedObjectObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectedObjectObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectedObjectObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect BoundingBox { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNDetectedObjectObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNDetectedObjectObservation -->
<div> <!-- start type VNErrorCode -->
<h3>New Type Vision.VNErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNErrorCode {
	<span class='added added-field ' data-is-non-breaking="">IOError = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InternalError = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidArgument = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidImage = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidModel = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOperation = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOption = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingOption = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">NotImplemented = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationFailed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfBoundsError = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfMemory = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestCancelled = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownError = 11,</span>
}
</pre>
</div> <!-- end type VNErrorCode -->
<div> <!-- start type VNErrorCodeExtensions -->
<h3>New Type Vision.VNErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (VNErrorCode self);</span>
}
</pre>
</div> <!-- end type VNErrorCodeExtensions -->
<div> <!-- start type VNFaceLandmarkRegion -->
<h3>New Type Vision.VNFaceLandmarkRegion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarkRegion : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PointCount { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion -->
<div> <!-- start type VNFaceLandmarkRegion2D -->
<h3>New Type Vision.VNFaceLandmarkRegion2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarkRegion2D : Vision.VNFaceLandmarkRegion, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.Vector2 Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector2[] Points { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2 GetPoint (uint index);</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion2D -->
<div> <!-- start type VNFaceLandmarks -->
<h3>New Type Vision.VNFaceLandmarks</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarks : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks -->
<div> <!-- start type VNFaceLandmarks2D -->
<h3>New Type Vision.VNFaceLandmarks2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarks2D : Vision.VNFaceLandmarks, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D AllPoints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D FaceContour { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D InnerLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftPupil { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D MedianLine { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D Nose { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D NoseCrest { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D OuterLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightPupil { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks2D -->
<div> <!-- start type VNFaceObservation -->
<h3>New Type Vision.VNFaceObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNFaceObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarks2D Landmarks { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNFaceObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNFaceObservation -->
<div> <!-- start type VNHomographicImageRegistrationRequest -->
<h3>New Type Vision.VNHomographicImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNHomographicImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNHomographicImageRegistrationRequest -->
<div> <!-- start type VNHorizonObservation -->
<h3>New Type Vision.VNHorizonObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNHorizonObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHorizonObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Angle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform Transform { get; }</span>
}
</pre>
</div> <!-- end type VNHorizonObservation -->
<div> <!-- start type VNImageAlignmentObservation -->
<h3>New Type Vision.VNImageAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageAlignmentObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageAlignmentObservation -->
<div> <!-- start type VNImageBasedRequest -->
<h3>New Type Vision.VNImageBasedRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageBasedRequest : Vision.VNRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageBasedRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect RegionOfInterest { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageBasedRequest -->
<div> <!-- start type VNImageCropAndScaleOption -->
<h3>New Type Vision.VNImageCropAndScaleOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNImageCropAndScaleOption {
	<span class='added added-field ' data-is-non-breaking="">CenterCrop = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFill = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFit = 1,</span>
}
</pre>
</div> <!-- end type VNImageCropAndScaleOption -->
<div> <!-- start type VNImageHomographicAlignmentObservation -->
<h3>New Type Vision.VNImageHomographicAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageHomographicAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageHomographicAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 WarpTransform { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageHomographicAlignmentObservation -->
<div> <!-- start type VNImageOptions -->
<h3>New Type Vision.VNImageOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CameraIntrinsics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary WeakProperties { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageOptions -->
<div> <!-- start type VNImageRegistrationRequest -->
<h3>New Type Vision.VNImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageRegistrationRequest : Vision.VNTargetedImageRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageRegistrationRequest -->
<div> <!-- start type VNImageRequestHandler -->
<h3>New Type Vision.VNImageRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNImageRequestHandler -->
<div> <!-- start type VNImageTranslationAlignmentObservation -->
<h3>New Type Vision.VNImageTranslationAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageTranslationAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageTranslationAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform AlignmentTransform { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageTranslationAlignmentObservation -->
<div> <!-- start type VNObservation -->
<h3>New Type Vision.VNObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNObservation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid Uuid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type VNObservation -->
<div> <!-- start type VNPixelBufferObservation -->
<h3>New Type Vision.VNPixelBufferObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNPixelBufferObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNPixelBufferObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
}
</pre>
</div> <!-- end type VNPixelBufferObservation -->
<div> <!-- start type VNRectangleObservation -->
<h3>New Type Vision.VNRectangleObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNRectangleObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRectangleObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopRight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNRectangleObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNRectangleObservation -->
<div> <!-- start type VNRequest -->
<h3>New Type Vision.VNRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNRequest : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestCompletionHandler CompletionHandler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreferBackgroundProcessing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice PreferredMetalContext { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual T[] GetResults&lt;T&gt; ();</span>
}
</pre>
</div> <!-- end type VNRequest -->
<div> <!-- start type VNRequestCompletionHandler -->
<h3>New Type Vision.VNRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate VNRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (VNRequest request, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (VNRequest request, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNRequestCompletionHandler -->
<div> <!-- start type VNRequestTrackingLevel -->
<h3>New Type Vision.VNRequestTrackingLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNRequestTrackingLevel {
	<span class='added added-field ' data-is-non-breaking="">Accurate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
}
</pre>
</div> <!-- end type VNRequestTrackingLevel -->
<div> <!-- start type VNSequenceRequestHandler -->
<h3>New Type Vision.VNSequenceRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNSequenceRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNSequenceRequestHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNSequenceRequestHandler -->
<div> <!-- start type VNTargetedImageRequest -->
<h3>New Type Vision.VNTargetedImageRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTargetedImageRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTargetedImageRequest -->
<div> <!-- start type VNTextObservation -->
<h3>New Type Vision.VNTextObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNTextObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTextObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRectangleObservation[] CharacterBoxes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNTextObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNTextObservation -->
<div> <!-- start type VNTrackObjectRequest -->
<h3>New Type Vision.VNTrackObjectRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackObjectRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackObjectRequest -->
<div> <!-- start type VNTrackRectangleRequest -->
<h3>New Type Vision.VNTrackRectangleRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackRectangleRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackRectangleRequest -->
<div> <!-- start type VNTrackingRequest -->
<h3>New Type Vision.VNTrackingRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTrackingRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackingRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNDetectedObjectObservation InputObservation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LastFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestTrackingLevel TrackingLevel { get; set; }</span>
}
</pre>
</div> <!-- end type VNTrackingRequest -->
<div> <!-- start type VNTranslationalImageRegistrationRequest -->
<h3>New Type Vision.VNTranslationalImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTranslationalImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTranslationalImageRegistrationRequest -->
<div> <!-- start type VNUtils -->
<h3>New Type Vision.VNUtils</h3>
<pre class='added' data-is-non-breaking="">
public static class VNUtils {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGRect NormalizedIdentityRect { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (CoreGraphics.CGPoint normalizedPoint, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetImageRect (CoreGraphics.CGRect normalizedRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetNormalizedFaceBoundingBoxPoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetNormalizedRect (CoreGraphics.CGRect imageRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsIdentityRect (CoreGraphics.CGRect rect);</span>
}
</pre>
</div> <!-- end type VNUtils -->
</div> <!-- end namespace Vision -->

</div>



   


 <hr>
