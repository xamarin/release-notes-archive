---
id: 29EE2C1E-6F57-4C88-902F-46EB339B108B
title: "tvOS 10.10.0 to 10.99.1"
---

# API diff

 [mscorlib.dll](#diff/xi/Xamarin.TVOS/mscorlib.html)

   


 [System.dll](#diff/xi/Xamarin.TVOS/System.html)

   


 [System.Core.dll](#diff/xi/Xamarin.TVOS/System.Core.html)

   


 [System.Data.dll](#diff/xi/Xamarin.TVOS/System.Data.html)

   


 [System.ServiceModel.dll](#diff/xi/Xamarin.TVOS/System.ServiceModel.html)

   


 [System.ServiceModel.Web.dll](#diff/xi/Xamarin.TVOS/System.ServiceModel.Web.html)

   


 [System.Web.Services.dll](#diff/xi/Xamarin.TVOS/System.Web.Services.html)

   


 [System.Transactions.dll](#diff/xi/Xamarin.TVOS/System.Transactions.html)

   


 [Xamarin.TVOS.dll](#diff/xi/Xamarin.TVOS/Xamarin.TVOS.html)

   


 [MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.TVOS/MonoTouch.NUnitLite.html)

   


   


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
</script><h1 id='diff/xi/Xamarin.TVOS/mscorlib.html'>mscorlib.dll</h1>

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
<!-- start namespace System.Reflection.Emit --> <div> 
<h2>Namespace System.Reflection.Emit</h2>
<div> <!-- start type PEFileKinds -->
<h3>New Type System.Reflection.Emit.PEFileKinds</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PEFileKinds {
	<span class='added added-field ' data-is-non-breaking="">ConsoleApplication = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Dll = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">WindowApplication = 3,</span>
}
</pre>
</div> <!-- end type PEFileKinds -->

</div> <!-- end namespace System.Reflection.Emit -->
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
</script><h1 id='diff/xi/Xamarin.TVOS/System.html'>System.dll</h1>

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
<!-- start namespace System.Diagnostics --> <div> 
<h2>Namespace System.Diagnostics</h2>
<!-- start type Process --> <div>
<h3>Type Changed: System.Diagnostics.Process</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public Process Start (string fileName, string <span class='removed removed-inline removed-breaking-inline'>username</span> <span class='added '>userName</span>, System.Security.SecureString password, string domain)
</div><div data-is-breaking="">	public Process Start (string fileName, string arguments, string <span class='removed removed-inline removed-breaking-inline'>username</span> <span class='added '>userName</span>, System.Security.SecureString password, string domain)
</div></pre>

</div> <!-- end type Process -->

</div> <!-- end namespace System.Diagnostics -->
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
</script><h1 id='diff/xi/Xamarin.TVOS/System.Core.html'>System.Core.dll</h1>

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
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<!-- start type RuntimeOps --> <div>
<h3>Type Changed: System.Runtime.CompilerServices.RuntimeOps</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("do not use this method")]
	public static IRuntimeVariables MergeRuntimeVariables (IRuntimeVariables first, IRuntimeVariables second, int[] indexes);</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("do not use this method")]
	public static System.Linq.Expressions.Expression Quote (System.Linq.Expressions.Expression expression, object hoistedLocals, object[] locals);</span>
</pre>

</div> <!-- end type RuntimeOps -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
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
</script><h1 id='diff/xi/Xamarin.TVOS/System.Data.html'>System.Data.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.TVOS/System.ServiceModel.html'>System.ServiceModel.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.TVOS/System.ServiceModel.Web.html'>System.ServiceModel.Web.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.TVOS/System.Web.Services.html'>System.Web.Services.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.TVOS/System.Transactions.html'>System.Transactions.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.TVOS/Xamarin.TVOS.html'>Xamarin.TVOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
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
<!-- start type AVKitMetadataIdentifier --> <div>
<h3>Type Changed: AVKit.AVKitMetadataIdentifier</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApproximateEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApproximateStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExactEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExactStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ServiceIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type AVKitMetadataIdentifier -->
<!-- start type AVPlayerViewController --> <div>
<h3>Type Changed: AVKit.AVPlayerViewController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIViewController CustomInfoViewController { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PlaybackControlsIncludeInfoViews { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PlaybackControlsIncludeTransportBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UILayoutGuide UnobscuredContentGuide { get; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewController -->
<!-- start type AVPlayerViewControllerDelegate --> <div>
<h3>Type Changed: AVKit.AVPlayerViewControllerDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndDismissalTransition (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldDismiss (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginDismissalTransition (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillTransitionToVisibilityOfTransportBar (AVPlayerViewController playerViewController, bool visible, IAVPlayerViewControllerAnimationCoordinator coordinator);</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewControllerDelegate -->
<!-- start type AVPlayerViewControllerDelegate_Extensions --> <div>
<h3>Type Changed: AVKit.AVPlayerViewControllerDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndDismissalTransition (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldDismiss (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginDismissalTransition (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillTransitionToVisibilityOfTransportBar (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, bool visible, IAVPlayerViewControllerAnimationCoordinator coordinator);</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewControllerDelegate_Extensions -->
<div> <!-- start type AVRoutePickerView -->
<h3>New Type AVKit.AVRoutePickerView</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerView : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor ActiveTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVRoutePickerViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVRoutePickerViewButtonStyle RoutePickerButtonStyle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class AVRoutePickerViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type AVRoutePickerView -->
<div> <!-- start type AVRoutePickerViewButtonStyle -->
<h3>New Type AVKit.AVRoutePickerViewButtonStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVRoutePickerViewButtonStyle {
	<span class='added added-field ' data-is-non-breaking="">Custom = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Plain = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">System = 0,</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewButtonStyle -->
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
<div> <!-- start type IAVPlayerViewControllerAnimationCoordinator -->
<h3>New Type AVKit.IAVPlayerViewControllerAnimationCoordinator</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVPlayerViewControllerAnimationCoordinator : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedAnimations (System.Action animations, System.Action&lt;bool&gt; completion);</span>
}
</pre>
</div> <!-- end type IAVPlayerViewControllerAnimationCoordinator -->
<div> <!-- start type IAVRoutePickerViewDelegate -->
<h3>New Type AVKit.IAVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVRoutePickerViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IAVRoutePickerViewDelegate -->

</div> <!-- end namespace AVKit -->
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
<!-- start type CAEAGLLayer --> <div>
<h3>Type Changed: CoreAnimation.CAEAGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEAGLLayer -->
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
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HistoryTrackingKey { get; }</span>
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
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect rectangle, int ciImageFormat);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect extent, int format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect rect, int ciImageFormat);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CIEdgePreserveUpsampleFilter -->
<h3>New Type CoreImage.CIEdgePreserveUpsampleFilter</h3>
<pre class='added' data-is-non-breaking="">
public class CIEdgePreserveUpsampleFilter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIEdgePreserveUpsampleFilter -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (IntPtr handle);</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (IntPtr handle);</span>
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
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->

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
<!-- start namespace HomeKit --> <div> 
<h2>Namespace HomeKit</h2>
<!-- start type HMAccessory --> <div>
<h3>Type Changed: HomeKit.HMAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FirmwareVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Manufacturer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Model { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMAccessoryProfile[] Profiles { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryProfileEventArgs&gt; DidAddProfile;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryProfileEventArgs&gt; DidRemoveProfile;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryFirmwareVersionEventArgs&gt; DidUpdateFirmwareVersion;</span>
</pre>
</div>

</div> <!-- end type HMAccessory -->
<!-- start type HMAccessoryDelegate --> <div>
<h3>Type Changed: HomeKit.HMAccessoryDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddProfile (HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveProfile (HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateFirmwareVersion (HMAccessory accessory, string firmwareVersion);</span>
</pre>
</div>

</div> <!-- end type HMAccessoryDelegate -->
<!-- start type HMAccessoryDelegate_Extensions --> <div>
<h3>Type Changed: HomeKit.HMAccessoryDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddProfile (IHMAccessoryDelegate This, HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveProfile (IHMAccessoryDelegate This, HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateFirmwareVersion (IHMAccessoryDelegate This, HMAccessory accessory, string firmwareVersion);</span>
</pre>
</div>

</div> <!-- end type HMAccessoryDelegate_Extensions -->
<!-- start type HMCharacteristicEvent --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicEvent</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual HMCharacteristic Characteristic { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public virtual Foundation.INSCopying TriggerValue { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type HMCharacteristicEvent -->
<!-- start type HMCharacteristicType --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ColorTemperature = 115,</span>
</pre>
</div>

</div> <!-- end type HMCharacteristicType -->
<!-- start type HMError --> <div>
<h3>Type Changed: HomeKit.HMError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">IncompatibleHomeHub = 92,</span>
	<span class='added added-field ' data-is-non-breaking="">NoHomeHub = 91,</span>
</pre>
</div>

</div> <!-- end type HMError -->
<!-- start type HMEvent --> <div>
<h3>Type Changed: HomeKit.HMEvent</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsSupported (HMHome home);</span>
</pre>
</div>

</div> <!-- end type HMEvent -->
<!-- start type HMEventTrigger --> <div>
<h3>Type Changed: HomeKit.HMEventTrigger</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMEvent[] EndEvents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExecuteOnce { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents[] Recurrences { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMEventTriggerActivationState TriggerActivationState { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTrigger (HMPresenceEvent presenceEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringAfterSignificantEvent (HMSignificantTimeEvent significantEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBeforeSignificantEvent (HMSignificantTimeEvent significantEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBetweenDates (Foundation.NSDateComponents firstDateComponents, Foundation.NSDateComponents secondDateComponents);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBetweenSignificantEvent (HMSignificantTimeEvent firstSignificantEvent, HMSignificantTimeEvent secondSignificantEvent);</span>
</pre>
</div>

</div> <!-- end type HMEventTrigger -->
<!-- start type HMHome --> <div>
<h3>Type Changed: HomeKit.HMHome</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMHomeHubState HomeHubState { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdateAccessControlForCurrentUser;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeHubStateEventArgs&gt; DidUpdateHomeHubState;</span>
</pre>
</div>

</div> <!-- end type HMHome -->
<!-- start type HMHomeDelegate --> <div>
<h3>Type Changed: HomeKit.HMHomeDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateAccessControlForCurrentUser (HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateHomeHubState (HMHome home, HMHomeHubState homeHubState);</span>
</pre>
</div>

</div> <!-- end type HMHomeDelegate -->
<!-- start type HMHomeDelegate_Extensions --> <div>
<h3>Type Changed: HomeKit.HMHomeDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateAccessControlForCurrentUser (IHMHomeDelegate This, HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateHomeHubState (IHMHomeDelegate This, HMHome home, HMHomeHubState homeHubState);</span>
</pre>
</div>

</div> <!-- end type HMHomeDelegate_Extensions -->
<!-- start type HMLocationEvent --> <div>
<h3>Type Changed: HomeKit.HMLocationEvent</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSMutableCopying</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual CoreLocation.CLRegion Region { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type HMLocationEvent -->
<div> <!-- start type HMAccessoryFirmwareVersionEventArgs -->
<h3>New Type HomeKit.HMAccessoryFirmwareVersionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryFirmwareVersionEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryFirmwareVersionEventArgs (string firmwareVersion);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string FirmwareVersion { get; set; }</span>
}
</pre>
</div> <!-- end type HMAccessoryFirmwareVersionEventArgs -->
<div> <!-- start type HMAccessoryProfileEventArgs -->
<h3>New Type HomeKit.HMAccessoryProfileEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryProfileEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryProfileEventArgs (HMAccessoryProfile profile);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMAccessoryProfile Profile { get; set; }</span>
}
</pre>
</div> <!-- end type HMAccessoryProfileEventArgs -->
<div> <!-- start type HMCalendarEvent -->
<h3>New Type HomeKit.HMCalendarEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMCalendarEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCalendarEvent (Foundation.NSDateComponents fireDateComponents);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCalendarEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCalendarEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents FireDateComponents { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMCalendarEvent -->
<div> <!-- start type HMCharacteristicThresholdRangeEvent -->
<h3>New Type HomeKit.HMCharacteristicThresholdRangeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMCharacteristicThresholdRangeEvent : HomeKit.HMEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicThresholdRangeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicThresholdRangeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMCharacteristicThresholdRangeEvent (HMCharacteristic characteristic, HMNumberRange thresholdRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMNumberRange ThresholdRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMCharacteristicThresholdRangeEvent -->
<div> <!-- start type HMDurationEvent -->
<h3>New Type HomeKit.HMDurationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMDurationEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMDurationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMDurationEvent (double duration);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMDurationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMDurationEvent -->
<div> <!-- start type HMEventTriggerActivationState -->
<h3>New Type HomeKit.HMEventTriggerActivationState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMEventTriggerActivationState {
	<span class='added added-field ' data-is-non-breaking="">Disabled = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoCompatibleHomeHub = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoHomeHub = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoLocationServicesAuthorization = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Enabled = 4,</span>
}
</pre>
</div> <!-- end type HMEventTriggerActivationState -->
<div> <!-- start type HMHomeHubState -->
<h3>New Type HomeKit.HMHomeHubState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMHomeHubState {
	<span class='added added-field ' data-is-non-breaking="">Connected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Disconnected = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAvailable = 0,</span>
}
</pre>
</div> <!-- end type HMHomeHubState -->
<div> <!-- start type HMHomeHubStateEventArgs -->
<h3>New Type HomeKit.HMHomeHubStateEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeHubStateEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeHubStateEventArgs (HMHomeHubState homeHubState);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMHomeHubState HomeHubState { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeHubStateEventArgs -->
<div> <!-- start type HMMutableCalendarEvent -->
<h3>New Type HomeKit.HMMutableCalendarEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCalendarEvent : HomeKit.HMCalendarEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCalendarEvent (Foundation.NSDateComponents fireDateComponents);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCalendarEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCalendarEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.NSDateComponents FireDateComponents { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableCalendarEvent -->
<div> <!-- start type HMMutableCharacteristicEvent -->
<h3>New Type HomeKit.HMMutableCharacteristicEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCharacteristicEvent : HomeKit.HMCharacteristicEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCharacteristicEvent (HMCharacteristic characteristic, Foundation.INSCopying triggerValue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.INSCopying TriggerValue { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMMutableCharacteristicEvent -->
<div> <!-- start type HMMutableCharacteristicThresholdRangeEvent -->
<h3>New Type HomeKit.HMMutableCharacteristicThresholdRangeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCharacteristicThresholdRangeEvent : HomeKit.HMCharacteristicThresholdRangeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicThresholdRangeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicThresholdRangeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCharacteristicThresholdRangeEvent (HMCharacteristic characteristic, HMNumberRange thresholdRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override HMNumberRange ThresholdRange { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableCharacteristicThresholdRangeEvent -->
<div> <!-- start type HMMutableDurationEvent -->
<h3>New Type HomeKit.HMMutableDurationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableDurationEvent : HomeKit.HMDurationEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableDurationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableDurationEvent (double duration);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableDurationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override double Duration { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableDurationEvent -->
<div> <!-- start type HMMutableLocationEvent -->
<h3>New Type HomeKit.HMMutableLocationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableLocationEvent : HomeKit.HMLocationEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableLocationEvent (CoreLocation.CLRegion region);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableLocationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableLocationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override CoreLocation.CLRegion Region { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableLocationEvent -->
<div> <!-- start type HMMutablePresenceEvent -->
<h3>New Type HomeKit.HMMutablePresenceEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutablePresenceEvent : HomeKit.HMPresenceEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutablePresenceEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutablePresenceEvent (HMPresenceType presenceType);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutablePresenceEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceType PresenceType { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutablePresenceEvent -->
<div> <!-- start type HMMutableSignificantTimeEvent -->
<h3>New Type HomeKit.HMMutableSignificantTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableSignificantTimeEvent : HomeKit.HMSignificantTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableSignificantTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableSignificantTimeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent (Foundation.NSString significantEvent, Foundation.NSDateComponents offset);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent (HMSignificantEvent significantEvent, Foundation.NSDateComponents offset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.NSDateComponents Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMSignificantEvent SignificantEvent { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableSignificantTimeEvent -->
<div> <!-- start type HMNumberRange -->
<h3>New Type HomeKit.HMNumberRange</h3>
<pre class='added' data-is-non-breaking="">
public class HMNumberRange : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMNumberRange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMNumberRange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Max { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Min { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromMax (Foundation.NSNumber maxValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromMin (Foundation.NSNumber minValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromRange (Foundation.NSNumber minValue, Foundation.NSNumber maxValue);</span>
}
</pre>
</div> <!-- end type HMNumberRange -->
<div> <!-- start type HMPresenceEvent -->
<h3>New Type HomeKit.HMPresenceEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMPresenceEvent : HomeKit.HMEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMPresenceEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMPresenceEvent (HMPresenceType presenceType);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMPresenceEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeyPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceType PresenceType { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMPresenceEvent -->
<div> <!-- start type HMPresenceType -->
<h3>New Type HomeKit.HMPresenceType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMPresenceType {
	<span class='added added-field ' data-is-non-breaking="">AnyUserAtHome = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentUserAtHome = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentUserNotAtHome = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NoUserAtHome = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">UsersAtHome = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">UsersNotAtHome = 5,</span>
}
</pre>
</div> <!-- end type HMPresenceType -->
<div> <!-- start type HMPresenceTypeExtensions -->
<h3>New Type HomeKit.HMPresenceTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMPresenceTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (HMPresenceType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMPresenceType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type HMPresenceTypeExtensions -->
<div> <!-- start type HMSignificantEventExtensions -->
<h3>New Type HomeKit.HMSignificantEventExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMSignificantEventExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (HMSignificantEvent self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMSignificantEvent GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type HMSignificantEventExtensions -->
<div> <!-- start type HMSignificantTimeEvent -->
<h3>New Type HomeKit.HMSignificantTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMSignificantTimeEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMSignificantTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMSignificantTimeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMSignificantTimeEvent (Foundation.NSString significantEvent, Foundation.NSDateComponents offset);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMSignificantTimeEvent (HMSignificantEvent significantEvent, Foundation.NSDateComponents offset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMSignificantEvent SignificantEvent { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMSignificantTimeEvent -->
<div> <!-- start type HMTimeEvent -->
<h3>New Type HomeKit.HMTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMTimeEvent : HomeKit.HMEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMTimeEvent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTimeEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMTimeEvent -->

</div> <!-- end namespace HomeKit -->
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
<div> <!-- start type MKMarkerAnnotationView -->
<h3>New Type MapKit.MKMarkerAnnotationView</h3>
<pre class='added' data-is-non-breaking="">
public class MKMarkerAnnotationView : MapKit.MKAnnotationView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView (IMKAnnotation annotation, string reuseIdentifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AnimatesWhenAdded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage GlyphImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string GlyphText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor GlyphTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor MarkerTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage SelectedGlyphImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility SubtitleVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility TitleVisibility { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class MKMarkerAnnotationViewAppearance : MapKit.MKAnnotationView+MKAnnotationViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (IntPtr handle);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage GlyphImage { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual string GlyphText { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor GlyphTintColor { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor MarkerTintColor { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage SelectedGlyphImage { get; set; }</span>
	}
}
</pre>
</div> <!-- end type MKMarkerAnnotationView -->
<div> <!-- start type MKScaleView -->
<h3>New Type MapKit.MKScaleView</h3>
<pre class='added' data-is-non-breaking="">
public class MKScaleView : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKScaleView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKScaleViewAlignment LegendAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKMapView MapView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility ScaleVisibility { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView FromMapView (MKMapView mapView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class MKScaleViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type MKScaleView -->
<div> <!-- start type MKScaleViewAlignment -->
<h3>New Type MapKit.MKScaleViewAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKScaleViewAlignment {
	<span class='added added-field ' data-is-non-breaking="">Leading = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 1,</span>
}
</pre>
</div> <!-- end type MKScaleViewAlignment -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MetalPerformanceShaders --> <div> 
<h2>Namespace MetalPerformanceShaders</h2>
<!-- start type MPSBinaryImageKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSBinaryImageKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSBinaryImageKernel -->
<!-- start type MPSCnnConvolution --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnConvolution</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnConvolution -->
<!-- start type MPSCnnConvolutionDescriptor --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnConvolutionDescriptor</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionDescriptor (Foundation.NSCoder coder);</span>
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

</div> <!-- end type MPSCnnConvolutionDescriptor -->
<!-- start type MPSCnnCrossChannelNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnCrossChannelNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnCrossChannelNormalization -->
<!-- start type MPSCnnFullyConnected --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnFullyConnected</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnFullyConnected -->
<!-- start type MPSCnnKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnKernel -->
<!-- start type MPSCnnLocalContrastNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnLocalContrastNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnLocalContrastNormalization -->
<!-- start type MPSCnnLogSoftMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnLogSoftMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnLogSoftMax -->
<!-- start type MPSCnnNeuron --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuron</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuron -->
<!-- start type MPSCnnNeuronAbsolute --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronAbsolute</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsolute (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronAbsolute -->
<!-- start type MPSCnnNeuronLinear --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronLinear</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinear (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronLinear -->
<!-- start type MPSCnnNeuronReLU --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronReLU</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLU (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronReLU -->
<!-- start type MPSCnnNeuronSigmoid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronSigmoid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronSigmoid -->
<!-- start type MPSCnnNeuronTanH --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronTanH</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanH (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronTanH -->
<!-- start type MPSCnnPooling --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPooling</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPooling -->
<!-- start type MPSCnnPoolingAverage --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPoolingAverage</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPoolingAverage -->
<!-- start type MPSCnnPoolingMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPoolingMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPoolingMax -->
<!-- start type MPSCnnSoftMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnSoftMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnSoftMax -->
<!-- start type MPSCnnSpatialNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnSpatialNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnSpatialNormalization -->
<!-- start type MPSImageAreaMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageAreaMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageAreaMax -->
<!-- start type MPSImageAreaMin --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageAreaMin</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMin (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageAreaMin -->
<!-- start type MPSImageBox --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageBox</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageBox -->
<!-- start type MPSImageConversion --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageConversion</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageConversion -->
<!-- start type MPSImageConvolution --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageConvolution</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageConvolution -->
<!-- start type MPSImageDilate --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageDilate</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageDilate -->
<!-- start type MPSImageErode --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageErode</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageErode -->
<!-- start type MPSImageGaussianBlur --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageGaussianBlur</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageGaussianBlur -->
<!-- start type MPSImageGaussianPyramid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageGaussianPyramid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageGaussianPyramid -->
<!-- start type MPSImageHistogram --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogram</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogram -->
<!-- start type MPSImageHistogramEqualization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogramEqualization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogramEqualization -->
<!-- start type MPSImageHistogramSpecification --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogramSpecification</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogramSpecification -->
<!-- start type MPSImageIntegral --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageIntegral</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageIntegral -->
<!-- start type MPSImageIntegralOfSquares --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageIntegralOfSquares</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageIntegralOfSquares -->
<!-- start type MPSImageLanczosScale --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLanczosScale</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageLanczosScale -->
<!-- start type MPSImageLaplacian --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLaplacian</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageLaplacian -->
<!-- start type MPSImageMedian --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageMedian</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageMedian -->
<!-- start type MPSImagePyramid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImagePyramid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImagePyramid -->
<!-- start type MPSImageSobel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageSobel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageSobel -->
<!-- start type MPSImageTent --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageTent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTent (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageTent -->
<!-- start type MPSImageThresholdBinary --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdBinary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdBinary -->
<!-- start type MPSImageThresholdBinaryInverse --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdBinaryInverse</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdBinaryInverse -->
<!-- start type MPSImageThresholdToZero --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdToZero</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdToZero -->
<!-- start type MPSImageThresholdToZeroInverse --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdToZeroInverse</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdToZeroInverse -->
<!-- start type MPSImageThresholdTruncate --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdTruncate</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdTruncate -->
<!-- start type MPSImageTranspose --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageTranspose</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageTranspose -->
<!-- start type MPSKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Foundation.NSCoder coder);</span>
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

</div> <!-- end type MPSKernel -->
<!-- start type MPSMatrixMultiplication --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSMatrixMultiplication</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSMatrixMultiplication -->
<!-- start type MPSUnaryImageKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSUnaryImageKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSUnaryImageKernel -->

</div> <!-- end namespace MetalPerformanceShaders -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.2"</span> <span class='added '>"11.0"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.10.0"</span> <span class='added '>"10.99.1"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string DeviceCheckLibrary = "/System/Library/Frameworks/DeviceCheck.framework/DeviceCheck";</span>
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
<!-- start type PHAsset --> <div>
<h3>Type Changed: Photos.PHAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
</pre>
</div>

</div> <!-- end type PHAsset -->
<!-- start type PHContentEditingInput --> <div>
<h3>Type Changed: Photos.PHContentEditingInput</h3>
<div>
<p>Added property:</p>
<pre>
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

</div> <!-- end namespace Photos -->
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
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UILineBreakMode LineBreakMode { get; set; }</span>
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
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKNodeFocusBehavior FocusBehavior { get; set; }</span>
</pre>
</div>

</div> <!-- end type SKNode -->
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
public class SKTransformNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem {
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
<!-- start namespace TVMLKit --> <div> 
<h2>Namespace TVMLKit</h2>
<!-- start type TVElementAlignment --> <div>
<h3>Type Changed: TVMLKit.TVElementAlignment</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Leading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 5,</span>
</pre>
</div>

</div> <!-- end type TVElementAlignment -->
<!-- start type TVElementPosition --> <div>
<h3>Type Changed: TVMLKit.TVElementPosition</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BottomLeading = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">BottomTrailing = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Leading = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">TopLeading = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">TopTrailing = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 13,</span>
</pre>
</div>

</div> <!-- end type TVElementPosition -->

</div> <!-- end namespace TVMLKit -->
<!-- start namespace TVServices --> <div> 
<h2>Namespace TVServices</h2>
<!-- start type TVContentItem --> <div>
<h3>Type Changed: TVServices.TVContentItem</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl GetImageUrl (TVContentItemImageTrait traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetImageUrl (Foundation.NSUrl aUrl, TVContentItemImageTrait traits);</span>
</pre>
</div>

</div> <!-- end type TVContentItem -->
<div> <!-- start type TVContentItemImageTrait -->
<h3>New Type TVServices.TVContentItemImageTrait</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum TVContentItemImageTrait {
	<span class='added added-field ' data-is-non-breaking="">UserInterfaceStyleDark = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">UserInterfaceStyleLight = 256,</span>
}
</pre>
</div> <!-- end type TVContentItemImageTrait -->

</div> <!-- end namespace TVServices -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type NSLayoutFormatOptions --> <div>
<h3>Type Changed: UIKit.NSLayoutFormatOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SpacingBaselineToBaseline = 524288,</span>
	<span class='added added-field ' data-is-non-breaking="">SpacingEdgeToEdge = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SpacingMask = 524288,</span>
</pre>
</div>

</div> <!-- end type NSLayoutFormatOptions -->
<!-- start type UIBezierPath --> <div>
<h3>Type Changed: UIKit.UIBezierPath</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type UIBezierPath -->
<!-- start type UIButtonType --> <div>
<h3>Type Changed: UIKit.UIButtonType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Plain = 6,</span>
</pre>
</div>

</div> <!-- end type UIButtonType -->
<!-- start type UICollectionViewFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UICollectionViewFocusUpdateContext</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This cannot be directly created.")]
	public UICollectionViewFocusUpdateContext ();</span>
</div></pre>

</div> <!-- end type UICollectionViewFocusUpdateContext -->
<!-- start type UIColor --> <div>
<h3>Type Changed: UIKit.UIColor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIColor FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIColor FromName (string name, Foundation.NSBundle inBundle, UITraitCollection compatibleWithTraitCollection);</span>
</pre>
</div>

</div> <!-- end type UIColor -->
<!-- start type UIControlContentHorizontalAlignment --> <div>
<h3>Type Changed: UIKit.UIControlContentHorizontalAlignment</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Leading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 5,</span>
</pre>
</div>

</div> <!-- end type UIControlContentHorizontalAlignment -->
<!-- start type UIFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UIFocusUpdateContext</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This cannot be directly created.")]
	public UIFocusUpdateContext ();</span>
</div></pre>

</div> <!-- end type UIFocusUpdateContext -->
<!-- start type UIImageView --> <div>
<h3>Type Changed: UIKit.UIImageView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView OverlayContentView { get; }</span>
</pre>
</div>

</div> <!-- end type UIImageView -->
<!-- start type UIModalPresentationStyle --> <div>
<h3>Type Changed: UIKit.UIModalPresentationStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BlurOverFullScreen = 8,</span>
</pre>
</div>

</div> <!-- end type UIModalPresentationStyle -->
<div> <!-- start type UIAccessibilityContainerType -->
<h3>New Type UIKit.UIAccessibilityContainerType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIAccessibilityContainerType {
	<span class='added added-field ' data-is-non-breaking="">DataTable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UIAccessibilityContainerType -->
<div> <!-- start type UIAccessibilityCustomSystemRotorType -->
<h3>New Type UIKit.UIAccessibilityCustomSystemRotorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIAccessibilityCustomSystemRotorType {
	<span class='added added-field ' data-is-non-breaking="">BoldText = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Heading = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel1 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel2 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel3 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel4 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel5 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel6 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">ItalicText = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">MisspelledWord = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Table = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">TextField = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlineText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">VisitedLink = 2,</span>
}
</pre>
</div> <!-- end type UIAccessibilityCustomSystemRotorType -->
<div> <!-- start type UIScrollViewContentInsetAdjustmentBehavior -->
<h3>New Type UIKit.UIScrollViewContentInsetAdjustmentBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIScrollViewContentInsetAdjustmentBehavior {
	<span class='added added-field ' data-is-non-breaking="">Always = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Never = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ScrollableAxes = 1,</span>
}
</pre>
</div> <!-- end type UIScrollViewContentInsetAdjustmentBehavior -->
<div> <!-- start type UISplitViewControllerPrimaryEdge -->
<h3>New Type UIKit.UISplitViewControllerPrimaryEdge</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UISplitViewControllerPrimaryEdge {
	<span class='added added-field ' data-is-non-breaking="">Leading = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 1,</span>
}
</pre>
</div> <!-- end type UISplitViewControllerPrimaryEdge -->
<div> <!-- start type UITableViewSeparatorInsetReference -->
<h3>New Type UIKit.UITableViewSeparatorInsetReference</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITableViewSeparatorInsetReference {
	<span class='added added-field ' data-is-non-breaking="">AutomaticInsets = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">CellEdges = 0,</span>
}
</pre>
</div> <!-- end type UITableViewSeparatorInsetReference -->
<div> <!-- start type UITextSmartDashesType -->
<h3>New Type UIKit.UITextSmartDashesType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartDashesType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartDashesType -->
<div> <!-- start type UITextSmartInsertDeleteType -->
<h3>New Type UIKit.UITextSmartInsertDeleteType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartInsertDeleteType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartInsertDeleteType -->
<div> <!-- start type UITextSmartQuotesType -->
<h3>New Type UIKit.UITextSmartQuotesType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartQuotesType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartQuotesType -->

</div> <!-- end namespace UIKit -->
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

<!-- start namespace DeviceCheck --> <div> 
<h2>New Namespace DeviceCheck</h2>

<div> <!-- start type DCDevice -->
<h3>New Type DeviceCheck.DCDevice</h3>
<pre class='added' data-is-non-breaking="">
public class DCDevice : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DCDevice ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DCDevice (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DCDevice (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DCDevice CurrentDevice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Supported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void GenerateToken (DCDeviceGenerateTokenCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; GenerateTokenAsync ();</span>
}
</pre>
</div> <!-- end type DCDevice -->
<div> <!-- start type DCDeviceGenerateTokenCompletionHandler -->
<h3>New Type DeviceCheck.DCDeviceGenerateTokenCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate DCDeviceGenerateTokenCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DCDeviceGenerateTokenCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData token, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData token, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type DCDeviceGenerateTokenCompletionHandler -->
<div> <!-- start type DCError -->
<h3>New Type DeviceCheck.DCError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum DCError {
	<span class='added added-field ' data-is-non-breaking="">FeatureUnsupported = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownSystemFailure = 0,</span>
}
</pre>
</div> <!-- end type DCError -->
<div> <!-- start type DCErrorExtensions -->
<h3>New Type DeviceCheck.DCErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class DCErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (DCError self);</span>
}
</pre>
</div> <!-- end type DCErrorExtensions -->
</div> <!-- end namespace DeviceCheck -->

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
</script><h1 id='diff/xi/Xamarin.TVOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoTouch.NUnit --> <div> 
<h2>Namespace MonoTouch.NUnit</h2>
<!-- start type NUnitOutputTextWriter --> <div>
<h3>Type Changed: MonoTouch.NUnit.NUnitOutputTextWriter</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public NUnitOutputTextWriter (UI.BaseTouchRunner runner, System.IO.TextWriter baseWriter, NUnitLite.Runner.OutputWriter xmlWriter);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NUnitOutputTextWriter (UI.BaseTouchRunner runner, System.IO.TextWriter baseWriter, NUnitLite.Runner.OutputWriter xmlWriter, UI.XmlMode xmlMode);</span>
</pre>
</div>

</div> <!-- end type NUnitOutputTextWriter -->

</div> <!-- end namespace MonoTouch.NUnit -->
<!-- start namespace MonoTouch.NUnit.UI --> <div> 
<h2>Namespace MonoTouch.NUnit.UI</h2>
<!-- start type TouchOptions --> <div>
<h3>Type Changed: MonoTouch.NUnit.UI.TouchOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string LogFile { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public XmlMode XmlMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type TouchOptions -->
<div> <!-- start type XmlMode -->
<h3>New Type MonoTouch.NUnit.UI.XmlMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum XmlMode {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Wrapped = 1,</span>
}
</pre>
</div> <!-- end type XmlMode -->

</div> <!-- end namespace MonoTouch.NUnit.UI -->
</div>



   


 <hr>
