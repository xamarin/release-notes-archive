---
id: 069244F6-F427-429A-AF81-32611DE6E0FD
title: "iOS 10.12.0 to 10.99.4"
---

# API diff

 [mscorlib.dll](#diff/xi/Xamarin.iOS/mscorlib.html)

   


 [System.dll](#diff/xi/Xamarin.iOS/System.html)

   


 [System.Core.dll](#diff/xi/Xamarin.iOS/System.Core.html)

   


 [System.Data.dll](#diff/xi/Xamarin.iOS/System.Data.html)

   


 [System.ServiceModel.dll](#diff/xi/Xamarin.iOS/System.ServiceModel.html)

   


 [System.ServiceModel.Web.dll](#diff/xi/Xamarin.iOS/System.ServiceModel.Web.html)

   


 [System.Web.Services.dll](#diff/xi/Xamarin.iOS/System.Web.Services.html)

   


 [System.Transactions.dll](#diff/xi/Xamarin.iOS/System.Transactions.html)

   


 [MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.iOS/MonoTouch.NUnitLite.html)

   


 [Xamarin.iOS.dll](#diff/xi/Xamarin.iOS/Xamarin.iOS.html)

   


   


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
</script><h1 id='diff/xi/Xamarin.iOS/mscorlib.html'>mscorlib.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.html'>System.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.Core.html'>System.Core.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.Data.html'>System.Data.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.ServiceModel.html'>System.ServiceModel.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.ServiceModel.Web.html'>System.ServiceModel.Web.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.Web.Services.html'>System.Web.Services.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.Transactions.html'>System.Transactions.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

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
<!-- start type AVPlayerViewController --> <div>
<h3>Type Changed: AVKit.AVPlayerViewController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool EntersFullScreenWhenPlaybackBegins { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExitsFullScreenWhenPlaybackEnds { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewController -->
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
<!-- start namespace AudioToolbox --> <div> 
<h2>Namespace AudioToolbox</h2>
<!-- start type AudioChannelLabel --> <div>
<h3>Type Changed: AudioToolbox.AudioChannelLabel</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HoaAcn = 500,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn0 = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn1 = 131073,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn10 = 131082,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn11 = 131083,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn12 = 131084,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn13 = 131085,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn14 = 131086,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn15 = 131087,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn2 = 131074,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn3 = 131075,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn4 = 131076,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn5 = 131077,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn6 = 131078,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn65024 = 196096,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn7 = 131079,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn8 = 131080,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn9 = 131081,</span>
</pre>
</div>

</div> <!-- end type AudioChannelLabel -->
<!-- start type AudioChannelLayoutTag --> <div>
<h3>Type Changed: AudioToolbox.AudioChannelLayoutTag</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HOA_ACN_N3D = 12517376,</span>
	<span class='added added-field ' data-is-non-breaking="">HOA_ACN_SN3D = 12451840,</span>
</pre>
</div>

</div> <!-- end type AudioChannelLayoutTag -->
<!-- start type AudioFormatType --> <div>
<h3>Type Changed: AudioToolbox.AudioFormatType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Flac = 1718378851,</span>
	<span class='added added-field ' data-is-non-breaking="">Opus = 1869641075,</span>
</pre>
</div>

</div> <!-- end type AudioFormatType -->

</div> <!-- end namespace AudioToolbox -->
<!-- start namespace CallKit --> <div> 
<h2>Namespace CallKit</h2>
<!-- start type CXCallController --> <div>
<h3>Type Changed: CallKit.CXCallController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestTransaction (CXAction action, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestTransaction (CXAction[] actions, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RequestTransactionAsync (CXAction action);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RequestTransactionAsync (CXAction[] actions);</span>
</pre>
</div>

</div> <!-- end type CXCallController -->
<!-- start type CXCallDirectoryExtensionContext --> <div>
<h3>Type Changed: CallKit.CXCallDirectoryExtensionContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Incremental { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllBlockingEntries ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllIdentificationEntries ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveBlockingEntry (long phoneNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveIdentificationEntry (long phoneNumber);</span>
</pre>
</div>

</div> <!-- end type CXCallDirectoryExtensionContext -->
<!-- start type CXErrorCodeCallDirectoryManagerError --> <div>
<h3>Type Changed: CallKit.CXErrorCodeCallDirectoryManagerError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UnexpectedIncrementalRemoval = 8,</span>
</pre>
</div>

</div> <!-- end type CXErrorCodeCallDirectoryManagerError -->
<!-- start type CXProviderConfiguration --> <div>
<h3>Type Changed: CallKit.CXProviderConfiguration</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludesCallsInRecents { get; set; }</span>
</pre>
</div>

</div> <!-- end type CXProviderConfiguration -->
<!-- start type CXSetGroupCallAction --> <div>
<h3>Type Changed: CallKit.CXSetGroupCallAction</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>

</div> <!-- end type CXSetGroupCallAction -->

</div> <!-- end namespace CallKit -->
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
<!-- start type CNContact --> <div>
<h3>Type Changed: Contacts.CNContact</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderReading</span>
</pre>
</div>

</div> <!-- end type CNContact -->
<!-- start type CNErrorCode --> <div>
<h3>Type Changed: Contacts.CNErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierDoesNotExist = 601,</span>
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierInvalid = 600,</span>
	<span class='added added-field ' data-is-non-breaking="">VCardMalformed = 700,</span>
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
<!-- start type CNMutableContact --> <div>
<h3>Type Changed: Contacts.CNMutableContact</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderReading</span>
</pre>
</div>

</div> <!-- end type CNMutableContact -->

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
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CACornerMask MaskedCorners { get; set; }</span>
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
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsNextDrawableTimeout { get; set; }</span>
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
<div> <!-- start type CACornerMask -->
<h3>New Type CoreAnimation.CACornerMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CACornerMask {
	<span class='added added-field ' data-is-non-breaking="">MaxXMaxYCorner = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">MaxXMinYCorner = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MinXMaxYCorner = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">MinXMinYCorner = 1,</span>
}
</pre>
</div> <!-- end type CACornerMask -->

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
<!-- start type NSPersistentStore --> <div>
<h3>Type Changed: CoreData.NSPersistentStore</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSCoreDataCoreSpotlightDelegate CoreSpotlightExporter { get; }</span>
</pre>
</div>

</div> <!-- end type NSPersistentStore -->
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
<div> <!-- start type NSCoreDataCoreSpotlightDelegate -->
<h3>New Type CoreData.NSCoreDataCoreSpotlightDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class NSCoreDataCoreSpotlightDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSCoreDataCoreSpotlightDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCoreDataCoreSpotlightDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCoreDataCoreSpotlightDelegate (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSCoreDataCoreSpotlightDelegate (NSPersistentStoreDescription description, NSManagedObjectModel model);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DomainIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string IndexName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreSpotlight.CSSearchableItemAttributeSet GetAttributeSet (NSManagedObject object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReindexAllSearchableItems (CoreSpotlight.CSSearchableIndex searchableIndex, System.Action acknowledgementHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReindexSearchableItems (CoreSpotlight.CSSearchableIndex searchableIndex, string[] identifiers, System.Action acknowledgementHandler);</span>
}
</pre>
</div> <!-- end type NSCoreDataCoreSpotlightDelegate -->
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
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("The default initializer does not work in recent iOS version (11b4).")]
	public CIImageAccumulator ();</span>
</div></pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect rectangle, CIFormat format);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect rect, CIFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
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
<div> <!-- start type CIBarcodeDescriptor -->
<h3>New Type CoreImage.CIBarcodeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIBarcodeDescriptor : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CIBarcodeDescriptor -->
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
<div> <!-- start type CIBlendWithBlueMask -->
<h3>New Type CoreImage.CIBlendWithBlueMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithBlueMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithBlueMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBlendWithBlueMask -->
<div> <!-- start type CIBlendWithRedMask -->
<h3>New Type CoreImage.CIBlendWithRedMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithRedMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithRedMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBlendWithRedMask -->
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
<div> <!-- start type CIEdgePreserveUpsampleFilter -->
<h3>New Type CoreImage.CIEdgePreserveUpsampleFilter</h3>
<pre class='added' data-is-non-breaking="">
public class CIEdgePreserveUpsampleFilter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (IntPtr handle);</span>
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
<!-- start type CLLocationManager --> <div>
<h3>Type Changed: CoreLocation.CLLocationManager</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsBackgroundLocationIndicator { get; set; }</span>
</pre>
</div>

</div> <!-- end type CLLocationManager -->
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
<!-- start namespace CoreMotion --> <div> 
<h2>Namespace CoreMotion</h2>
<!-- start type CMAltimeter --> <div>
<h3>Type Changed: CoreMotion.CMAltimeter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CMAuthorizationStatus AuthorizationStatus { get; }</span>
</pre>
</div>

</div> <!-- end type CMAltimeter -->
<!-- start type CMDeviceMotion --> <div>
<h3>Type Changed: CoreMotion.CMDeviceMotion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Heading { get; }</span>
</pre>
</div>

</div> <!-- end type CMDeviceMotion -->
<!-- start type CMMotionActivityManager --> <div>
<h3>Type Changed: CoreMotion.CMMotionActivityManager</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CMAuthorizationStatus AuthorizationStatus { get; }</span>
</pre>
</div>

</div> <!-- end type CMMotionActivityManager -->
<!-- start type CMPedometer --> <div>
<h3>Type Changed: CoreMotion.CMPedometer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CMAuthorizationStatus AuthorizationStatus { get; }</span>
</pre>
</div>

</div> <!-- end type CMPedometer -->
<!-- start type CMSensorRecorder --> <div>
<h3>Type Changed: CoreMotion.CMSensorRecorder</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CMAuthorizationStatus AuthorizationStatus { get; }</span>
</pre>
</div>

</div> <!-- end type CMSensorRecorder -->
<div> <!-- start type CMAuthorizationStatus -->
<h3>New Type CoreMotion.CMAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CMAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type CMAuthorizationStatus -->

</div> <!-- end namespace CoreMotion -->
<!-- start namespace CoreSpotlight --> <div> 
<h2>Namespace CoreSpotlight</h2>
<!-- start type CSIndexExtensionRequestHandler --> <div>
<h3>Type Changed: CoreSpotlight.CSIndexExtensionRequestHandler</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetData (CSSearchableIndex searchableIndex, string itemIdentifier, string typeIdentifier, Foundation.NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl GetFileUrl (CSSearchableIndex searchableIndex, string itemIdentifier, string typeIdentifier, bool inPlace, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type CSIndexExtensionRequestHandler -->
<!-- start type CSSearchableIndexDelegate --> <div>
<h3>Type Changed: CoreSpotlight.CSSearchableIndexDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetData (CSSearchableIndex searchableIndex, string itemIdentifier, string typeIdentifier, Foundation.NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl GetFileUrl (CSSearchableIndex searchableIndex, string itemIdentifier, string typeIdentifier, bool inPlace, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type CSSearchableIndexDelegate -->
<!-- start type CSSearchableIndexDelegate_Extensions --> <div>
<h3>Type Changed: CoreSpotlight.CSSearchableIndexDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetData (ICSSearchableIndexDelegate This, CSSearchableIndex searchableIndex, string itemIdentifier, string typeIdentifier, Foundation.NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrl GetFileUrl (ICSSearchableIndexDelegate This, CSSearchableIndex searchableIndex, string itemIdentifier, string typeIdentifier, bool inPlace, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type CSSearchableIndexDelegate_Extensions -->
<!-- start type CSSearchableItemAttributeSet --> <div>
<h3>Type Changed: CoreSpotlight.CSSearchableItemAttributeSet</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? IsUserCreated { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IsUserCurated { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IsUserOwned { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] ProviderDataTypeIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] ProviderFileTypeIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] ProviderInPlaceFileTypeIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber RankingHint { get; set; }</span>
</pre>
</div>

</div> <!-- end type CSSearchableItemAttributeSet -->

</div> <!-- end namespace CoreSpotlight -->
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

</div> <!-- end namespace EventKit -->
<!-- start namespace EventKitUI --> <div> 
<h2>Namespace EventKitUI</h2>
<div> <!-- start type EKUIBundle -->
<h3>New Type EventKitUI.EKUIBundle</h3>
<pre class='added' data-is-non-breaking="">
public static class EKUIBundle {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSBundle UIBundle { get; }</span>
}
</pre>
</div> <!-- end type EKUIBundle -->

</div> <!-- end namespace EventKitUI -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSActivityOptions --> <div>
<h3>Type Changed: Foundation.NSActivityOptions</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	IdleDisplaySleepDisabled = <span class='removed removed-inline removed-breaking-inline'>256</span> <span class='added '>1099511627776</span>
</div></pre>

</div> <!-- end type NSActivityOptions -->
<!-- start type NSAttributedString --> <div>
<h3>Type Changed: Foundation.NSAttributedString</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAttributedString (NSData providerData, string typeIdentifier, NSError outError);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableTypeIdentifiersForItemProvider { get; }</span>
</pre>
</div>

</div> <!-- end type NSAttributedString -->
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
<!-- start type NSError --> <div>
<h3>Type Changed: Foundation.NSError</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSError GetFileProviderError (FileProvider.INSFileProviderItem existingItem);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSError GetFileProviderError (string nonExistentItemIdentifier);</span>
</pre>
</div>

</div> <!-- end type NSError -->
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
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public HMEventTrigger (string name, HMEvent[] events, HMEvent[] endEvents, Foundation.NSDateComponents[] recurrences, Foundation.NSPredicate predicate);</span>
</pre>
</div>
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
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateEndEvents (HMEvent[] endEvents, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateEndEventsAsync (HMEvent[] endEvents);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateEvents (HMEvent[] events, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateEventsAsync (HMEvent[] events);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateExecuteOnce (bool executeOnce, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateExecuteOnceAsync (bool executeOnce);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateRecurrences (Foundation.NSDateComponents[] recurrences, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateRecurrencesAsync (Foundation.NSDateComponents[] recurrences);</span>
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
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageDestination --> <div>
<h3>Type Changed: ImageIO.CGImageDestination</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddAuxiliaryDataInfo (CGImageDestination dest, CGImageAuxiliaryDataType auxiliaryImageDataType, CGImageAuxiliaryDataInfo auxiliaryDataInfo);</span>
</pre>
</div>

</div> <!-- end type CGImageDestination -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AuxiliaryData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AuxiliaryDataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FileContentsDictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ImageCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Images { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NamedColorSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ThumbnailImages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Width { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->
<!-- start type CGImageSource --> <div>
<h3>Type Changed: ImageIO.CGImageSource</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo CopyAuxiliaryDataInfo (CGImageSource imageSource, uint index, CGImageAuxiliaryDataType auxiliaryImageDataType);</span>
</pre>
</div>

</div> <!-- end type CGImageSource -->
<div> <!-- start type CGImageAuxiliaryDataInfo -->
<h3>New Type ImageIO.CGImageAuxiliaryDataInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CGImageAuxiliaryDataInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData DepthData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary DepthDataDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CGImageMetadata Metadata { get; set; }</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataInfo -->
<div> <!-- start type CGImageAuxiliaryDataType -->
<h3>New Type ImageIO.CGImageAuxiliaryDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CGImageAuxiliaryDataType {
	<span class='added added-field ' data-is-non-breaking="">Depth = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disparity = 1,</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataType -->
<div> <!-- start type CGImageAuxiliaryDataTypeExtensions -->
<h3>New Type ImageIO.CGImageAuxiliaryDataTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CGImageAuxiliaryDataTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CGImageAuxiliaryDataType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGImageAuxiliaryDataType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataTypeExtensions -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INRestaurantGuest --> <div>
<h3>Type Changed: Intents.INRestaurantGuest</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This constructor does not create a valid instance of the type")]
	public INRestaurantGuest ();</span>
</div></pre>

</div> <!-- end type INRestaurantGuest -->

</div> <!-- end namespace Intents -->
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
<div> <!-- start type MKCompassButton -->
<h3>New Type MapKit.MKCompassButton</h3>
<pre class='added' data-is-non-breaking="">
public class MKCompassButton : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKCompassButton (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKCompassButton (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKCompassButton (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MKCompassButton.MKCompassButtonAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility CompassVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKMapView MapView { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKCompassButton.MKCompassButtonAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKCompassButton FromMapView (MKMapView mapView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKCompassButton.MKCompassButtonAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKCompassButton.MKCompassButtonAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKCompassButton.MKCompassButtonAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKCompassButton.MKCompassButtonAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKCompassButton.MKCompassButtonAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class MKCompassButtonAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MKCompassButton (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type MKCompassButton -->
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
<div> <!-- start type MKUserTrackingButton -->
<h3>New Type MapKit.MKUserTrackingButton</h3>
<pre class='added' data-is-non-breaking="">
public class MKUserTrackingButton : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKUserTrackingButton (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKUserTrackingButton (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKUserTrackingButton (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MKUserTrackingButton.MKUserTrackingButtonAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKMapView MapView { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKUserTrackingButton.MKUserTrackingButtonAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKUserTrackingButton FromMapView (MKMapView mapView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKUserTrackingButton.MKUserTrackingButtonAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKUserTrackingButton.MKUserTrackingButtonAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKUserTrackingButton.MKUserTrackingButtonAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKUserTrackingButton.MKUserTrackingButtonAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKUserTrackingButton.MKUserTrackingButtonAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class MKUserTrackingButtonAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MKUserTrackingButton (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type MKUserTrackingButton -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyServiceIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->
<!-- start type MPRemoteCommandHandlerStatus --> <div>
<h3>Type Changed: MediaPlayer.MPRemoteCommandHandlerStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">DeviceNotFound = 120,</span>
</pre>
</div>

</div> <!-- end type MPRemoteCommandHandlerStatus -->
<div> <!-- start type IMPSystemMusicPlayerController -->
<h3>New Type MediaPlayer.IMPSystemMusicPlayerController</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSystemMusicPlayerController : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenToPlay (MPMusicPlayerQueueDescriptor queueDescriptor);</span>
}
</pre>
</div> <!-- end type IMPSystemMusicPlayerController -->
<div> <!-- start type MPMusicPlayerPlayParameters -->
<h3>New Type MediaPlayer.MPMusicPlayerPlayParameters</h3>
<pre class='added' data-is-non-breaking="">
public class MPMusicPlayerPlayParameters : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerPlayParameters (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerPlayParameters (Foundation.NSDictionary dictionary);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerPlayParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerPlayParameters (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary Dictionary { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type MPMusicPlayerPlayParameters -->
<div> <!-- start type MPMusicPlayerPlayParametersQueueDescriptor -->
<h3>New Type MediaPlayer.MPMusicPlayerPlayParametersQueueDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPMusicPlayerPlayParametersQueueDescriptor : MediaPlayer.MPMusicPlayerQueueDescriptor, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerPlayParametersQueueDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerPlayParametersQueueDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerPlayParametersQueueDescriptor (MPMusicPlayerPlayParameters[] playParametersQueue);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerPlayParametersQueueDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPMusicPlayerPlayParameters[] PlayParametersQueue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPMusicPlayerPlayParameters StartItemPlayParameters { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetEndTime (double endTime, MPMusicPlayerPlayParameters playParameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetStartTime (double startTime, MPMusicPlayerPlayParameters playParameters);</span>
}
</pre>
</div> <!-- end type MPMusicPlayerPlayParametersQueueDescriptor -->
<div> <!-- start type NSUserActivity_MediaPlayerAdditions -->
<h3>New Type MediaPlayer.NSUserActivity_MediaPlayerAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSUserActivity_MediaPlayerAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetExternalMediaContentIdentifier (Foundation.NSUserActivity This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetExternalMediaContentIdentifier (Foundation.NSUserActivity This, Foundation.NSString identifier);</span>
}
</pre>
</div> <!-- end type NSUserActivity_MediaPlayerAdditions -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace MessageUI --> <div> 
<h2>Namespace MessageUI</h2>
<!-- start type MFMailComposeViewController --> <div>
<h3>Type Changed: MessageUI.MFMailComposeViewController</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetPreferredSendingEmailAddress (string emailAddress);</span>
</pre>
</div>

</div> <!-- end type MFMailComposeViewController -->

</div> <!-- end namespace MessageUI -->
<!-- start namespace Messages --> <div> 
<h2>Namespace Messages</h2>
<!-- start type MSConversation --> <div>
<h3>Type Changed: Messages.MSConversation</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendAttachment (Foundation.NSUrl url, string filename, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendAttachmentAsync (Foundation.NSUrl url, string filename);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendMessage (MSMessage message, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendMessageAsync (MSMessage message);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendSticker (MSSticker sticker, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendStickerAsync (MSSticker sticker);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendText (string text, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendTextAsync (string text);</span>
</pre>
</div>

</div> <!-- end type MSConversation -->
<!-- start type MSMessage --> <div>
<h3>Type Changed: Messages.MSMessage</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Pending { get; }</span>
</pre>
</div>

</div> <!-- end type MSMessage -->
<!-- start type MSMessageErrorCode --> <div>
<h3>Type Changed: Messages.MSMessageErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SendWhileNotVisible = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">SendWithoutRecentInteraction = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = -1,</span>
</pre>
</div>

</div> <!-- end type MSMessageErrorCode -->
<!-- start type MSMessagesAppPresentationStyle --> <div>
<h3>Type Changed: Messages.MSMessagesAppPresentationStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Transcript = 2,</span>
</pre>
</div>

</div> <!-- end type MSMessagesAppPresentationStyle -->
<!-- start type MSMessagesAppViewController --> <div>
<h3>Type Changed: Messages.MSMessagesAppViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IMSMessagesAppTranscriptPresentation</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetContentSizeThatFits (CoreGraphics.CGSize size);</span>
</pre>
</div>

</div> <!-- end type MSMessagesAppViewController -->
<div> <!-- start type IMSMessagesAppTranscriptPresentation -->
<h3>New Type Messages.IMSMessagesAppTranscriptPresentation</h3>
<pre class='added' data-is-non-breaking="">
public interface IMSMessagesAppTranscriptPresentation : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetContentSizeThatFits (CoreGraphics.CGSize size);</span>
}
</pre>
</div> <!-- end type IMSMessagesAppTranscriptPresentation -->
<div> <!-- start type MSMessageLiveLayout -->
<h3>New Type Messages.MSMessageLiveLayout</h3>
<pre class='added' data-is-non-breaking="">
public class MSMessageLiveLayout : Messages.MSMessageLayout, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MSMessageLiveLayout (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MSMessageLiveLayout (MSMessageTemplateLayout alternateLayout);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MSMessageLiveLayout (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MSMessageTemplateLayout AlternateLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MSMessageLiveLayout -->

</div> <!-- end namespace Messages -->
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
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.3"</span> <span class='added '>"11.0"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.10.0"</span> <span class='added '>"10.99.3"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string ARKitLibrary = "/System/Library/Frameworks/ARKit.framework/ARKit";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreNFCLibrary = "/System/Library/Frameworks/CoreNFC.framework/CoreNFC";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string DeviceCheckLibrary = "/System/Library/Frameworks/DeviceCheck.framework/DeviceCheck";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string EventKitUILibrary = "/System/Library/Frameworks/EventKitUI.framework/EventKitUI";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string FileProviderLibrary = "/System/Library/Frameworks/FileProvider.framework/FileProvider";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string FileProviderUILibrary = "/System/Library/Frameworks/FileProviderUI.framework/FileProviderUI";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string IdentityLookupLibrary = "/System/Library/Frameworks/IdentityLookup.framework/IdentityLookup";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string PdfKitLibrary = "/System/Library/Frameworks/PDFKit.framework/PDFKit";</span>
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
<!-- start type PHAssetCollectionSubtype --> <div>
<h3>Type Changed: Photos.PHAssetCollectionSubtype</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumAnimated = 214,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumLongExposures = 215,</span>
</pre>
</div>

</div> <!-- end type PHAssetCollectionSubtype -->
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
<!-- start namespace PushKit --> <div> 
<h2>Namespace PushKit</h2>
<!-- start type PKPushRegistryDelegate --> <div>
<h3>Type Changed: PushKit.PKPushRegistryDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveIncomingPush (PKPushRegistry registry, PKPushPayload payload, string type, System.Action completion);</span>
</pre>
</div>

</div> <!-- end type PKPushRegistryDelegate -->
<!-- start type PKPushRegistryDelegate_Extensions --> <div>
<h3>Type Changed: PushKit.PKPushRegistryDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidReceiveIncomingPush (IPKPushRegistryDelegate This, PKPushRegistry registry, PKPushPayload payload, string type, System.Action completion);</span>
</pre>
</div>

</div> <!-- end type PKPushRegistryDelegate_Extensions -->
<!-- start type PKPushType --> <div>
<h3>Type Changed: PushKit.PKPushType</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FileProvider { get; }</span>
</pre>
</div>

</div> <!-- end type PKPushType -->

</div> <!-- end namespace PushKit -->
<!-- start namespace QuickLook --> <div> 
<h2>Namespace QuickLook</h2>
<div> <!-- start type IQLPreviewingController -->
<h3>New Type QuickLook.IQLPreviewingController</h3>
<pre class='added' data-is-non-breaking="">
public interface IQLPreviewingController : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IQLPreviewingController -->
<div> <!-- start type QLFileThumbnailRequest -->
<h3>New Type QuickLook.QLFileThumbnailRequest</h3>
<pre class='added' data-is-non-breaking="">
public class QLFileThumbnailRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public QLFileThumbnailRequest ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected QLFileThumbnailRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected QLFileThumbnailRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl FileUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize MaximumSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize MinimumSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Scale { get; }</span>
}
</pre>
</div> <!-- end type QLFileThumbnailRequest -->
<div> <!-- start type QLPreviewingController_Extensions -->
<h3>New Type QuickLook.QLPreviewingController_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class QLPreviewingController_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void PreparePreviewOfFile (IQLPreviewingController This, Foundation.NSUrl url, System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PreparePreviewOfSearchableItem (IQLPreviewingController This, string identifier, string queryString, System.Action&lt;Foundation.NSError&gt; handler);</span>
}
</pre>
</div> <!-- end type QLPreviewingController_Extensions -->
<div> <!-- start type QLThumbnailProvider -->
<h3>New Type QuickLook.QLThumbnailProvider</h3>
<pre class='added' data-is-non-breaking="">
public class QLThumbnailProvider : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public QLThumbnailProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected QLThumbnailProvider (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected QLThumbnailProvider (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void ProvideThumbnail (QLFileThumbnailRequest request, System.Action&lt;QLThumbnailReply,Foundation.NSError&gt; handler);</span>
}
</pre>
</div> <!-- end type QLThumbnailProvider -->
<div> <!-- start type QLThumbnailReply -->
<h3>New Type QuickLook.QLThumbnailReply</h3>
<pre class='added' data-is-non-breaking="">
public class QLThumbnailReply : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected QLThumbnailReply (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected QLThumbnailReply (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static QLThumbnailReply CreateReply (Foundation.NSUrl fileUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static QLThumbnailReply CreateReply (CoreGraphics.CGSize contextSize, System.Func&lt;bool&gt; drawingBlock);</span>
	<span class='added added-method ' data-is-non-breaking="">public static QLThumbnailReply CreateReply (CoreGraphics.CGSize contextSize, System.Func&lt;CoreGraphics.CGContext,System.Boolean&gt; drawingBlock);</span>
}
</pre>
</div> <!-- end type QLThumbnailReply -->

</div> <!-- end namespace QuickLook -->
<!-- start namespace SafariServices --> <div> 
<h2>Namespace SafariServices</h2>
<!-- start type SFSafariViewController --> <div>
<h3>Type Changed: SafariServices.SFSafariViewController</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SFSafariViewController (Foundation.NSUrl url, SFSafariViewControllerConfiguration configuration);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SFSafariViewControllerConfiguration Configuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SFSafariViewControllerDismissButtonStyle DismissButtonStyle { get; set; }</span>
</pre>
</div>

</div> <!-- end type SFSafariViewController -->
<!-- start type SFSafariViewControllerDelegate --> <div>
<h3>Type Changed: SafariServices.SFSafariViewControllerDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetExcludedActivityTypes (SFSafariViewController controller, Foundation.NSUrl url, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InitialLoadDidRedirectToUrl (SFSafariViewController controller, Foundation.NSUrl url);</span>
</pre>
</div>

</div> <!-- end type SFSafariViewControllerDelegate -->
<!-- start type SFSafariViewControllerDelegate_Extensions --> <div>
<h3>Type Changed: SafariServices.SFSafariViewControllerDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetExcludedActivityTypes (ISFSafariViewControllerDelegate This, SFSafariViewController controller, Foundation.NSUrl url, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void InitialLoadDidRedirectToUrl (ISFSafariViewControllerDelegate This, SFSafariViewController controller, Foundation.NSUrl url);</span>
</pre>
</div>

</div> <!-- end type SFSafariViewControllerDelegate_Extensions -->
<div> <!-- start type SFAuthenticationCompletionHandler -->
<h3>New Type SafariServices.SFAuthenticationCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate SFAuthenticationCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFAuthenticationCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSUrl callbackUrl, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSUrl callbackUrl, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type SFAuthenticationCompletionHandler -->
<div> <!-- start type SFAuthenticationError -->
<h3>New Type SafariServices.SFAuthenticationError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SFAuthenticationError {
	<span class='added added-field ' data-is-non-breaking="">CanceledLogin = 1,</span>
}
</pre>
</div> <!-- end type SFAuthenticationError -->
<div> <!-- start type SFAuthenticationErrorExtensions -->
<h3>New Type SafariServices.SFAuthenticationErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SFAuthenticationErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (SFAuthenticationError self);</span>
}
</pre>
</div> <!-- end type SFAuthenticationErrorExtensions -->
<div> <!-- start type SFAuthenticationSession -->
<h3>New Type SafariServices.SFAuthenticationSession</h3>
<pre class='added' data-is-non-breaking="">
public class SFAuthenticationSession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SFAuthenticationSession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFAuthenticationSession (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SFAuthenticationSession (Foundation.NSUrl url, string callbackUrlScheme, SFAuthenticationCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Cancel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Start ();</span>
}
</pre>
</div> <!-- end type SFAuthenticationSession -->
<div> <!-- start type SFSafariViewControllerConfiguration -->
<h3>New Type SafariServices.SFSafariViewControllerConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariViewControllerConfiguration : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFSafariViewControllerConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariViewControllerConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariViewControllerConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool BarCollapsingEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool EntersReaderIfAvailable { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type SFSafariViewControllerConfiguration -->
<div> <!-- start type SFSafariViewControllerDismissButtonStyle -->
<h3>New Type SafariServices.SFSafariViewControllerDismissButtonStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SFSafariViewControllerDismissButtonStyle {
	<span class='added added-field ' data-is-non-breaking="">Cancel = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Close = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Done = 0,</span>
}
</pre>
</div> <!-- end type SFSafariViewControllerDismissButtonStyle -->
<div> <!-- start type SSReadingListErrorExtensions -->
<h3>New Type SafariServices.SSReadingListErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SSReadingListErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (SSReadingListError self);</span>
}
</pre>
</div> <!-- end type SSReadingListErrorExtensions -->

</div> <!-- end namespace SafariServices -->
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
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKCloudServiceController --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString StorefrontCountryCodeDidChangeNotification { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestStorefrontCountryCode (System.Action&lt;Foundation.NSString,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSString&gt; RequestStorefrontCountryCodeAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestUserToken (string developerToken, System.Action&lt;Foundation.NSString,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSString&gt; RequestUserTokenAsync (string developerToken);</span>
</pre>
</div>
<!-- start type SKCloudServiceController.Notifications --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStorefrontCountryCodeDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStorefrontCountryCodeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type SKCloudServiceController.Notifications -->

</div> <!-- end type SKCloudServiceController -->
<!-- start type SKCloudServiceSetupOptions --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceSetupOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string MessageIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type SKCloudServiceSetupOptions -->
<!-- start type SKPaymentTransactionObserver --> <div>
<h3>Type Changed: StoreKit.SKPaymentTransactionObserver</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAddStorePayment (SKPaymentQueue queue, SKPayment payment, SKProduct product);</span>
</pre>
</div>

</div> <!-- end type SKPaymentTransactionObserver -->
<!-- start type SKPaymentTransactionObserver_Extensions --> <div>
<h3>Type Changed: StoreKit.SKPaymentTransactionObserver_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldAddStorePayment (ISKPaymentTransactionObserver This, SKPaymentQueue queue, SKPayment payment, SKProduct product);</span>
</pre>
</div>

</div> <!-- end type SKPaymentTransactionObserver_Extensions -->
<!-- start type SKStoreProductParameterKey --> <div>
<h3>Type Changed: StoreKit.SKStoreProductParameterKey</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ProductIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type SKStoreProductParameterKey -->
<div> <!-- start type SKCloudServiceSetupMessageIdentifier -->
<h3>New Type StoreKit.SKCloudServiceSetupMessageIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKCloudServiceSetupMessageIdentifier {
	<span class='added added-field ' data-is-non-breaking="">AddMusic = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Connect = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Join = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PlayMusic = 3,</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupMessageIdentifier -->
<div> <!-- start type SKCloudServiceSetupMessageIdentifierExtensions -->
<h3>New Type StoreKit.SKCloudServiceSetupMessageIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SKCloudServiceSetupMessageIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (SKCloudServiceSetupMessageIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKCloudServiceSetupMessageIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupMessageIdentifierExtensions -->
<div> <!-- start type SKProductStorePromotionController -->
<h3>New Type StoreKit.SKProductStorePromotionController</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductStorePromotionController : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductStorePromotionController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductStorePromotionController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SKProductStorePromotionController Default { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchStorePromotionOrder (System.Action&lt;SKProduct[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SKProduct[]&gt; FetchStorePromotionOrderAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchStorePromotionVisibility (SKProduct product, System.Action&lt;SKProductStorePromotionVisibility,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SKProductStorePromotionVisibility&gt; FetchStorePromotionVisibilityAsync (SKProduct product);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SKProduct[] storePromotionOrder, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SKProductStorePromotionVisibility promotionVisibility, SKProduct product, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateAsync (SKProduct[] storePromotionOrder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateAsync (SKProductStorePromotionVisibility promotionVisibility, SKProduct product);</span>
}
</pre>
</div> <!-- end type SKProductStorePromotionController -->
<div> <!-- start type SKProductStorePromotionVisibility -->
<h3>New Type StoreKit.SKProductStorePromotionVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductStorePromotionVisibility {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hide = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Show = 1,</span>
}
</pre>
</div> <!-- end type SKProductStorePromotionVisibility -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type NSFileProviderExtension --> <div>
<h3>Type Changed: UIKit.NSFileProviderExtension</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CreateDirectory (string directoryName, string parentItemIdentifier, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; CreateDirectoryAsync (string directoryName, string parentItemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeleteItem (string itemIdentifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DeleteItemAsync (string itemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSProgress FetchThumbnails (FileProvider.NSFileProviderItemIdentifier[] itemIdentifiers, CoreGraphics.CGSize size, NSFileProviderExtensionFetchThumbnailsHandler perThumbnailCompletionHandler, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSProgress FetchThumbnails (Foundation.NSString[] itemIdentifiers, CoreGraphics.CGSize size, NSFileProviderExtensionFetchThumbnailsHandler perThumbnailCompletionHandler, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task FetchThumbnailsAsync (FileProvider.NSFileProviderItemIdentifier[] itemIdentifiers, CoreGraphics.CGSize size, NSFileProviderExtensionFetchThumbnailsHandler perThumbnailCompletionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task FetchThumbnailsAsync (Foundation.NSString[] itemIdentifiers, CoreGraphics.CGSize size, NSFileProviderExtensionFetchThumbnailsHandler perThumbnailCompletionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task FetchThumbnailsAsync (FileProvider.NSFileProviderItemIdentifier[] itemIdentifiers, CoreGraphics.CGSize size, NSFileProviderExtensionFetchThumbnailsHandler perThumbnailCompletionHandler, Foundation.NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task FetchThumbnailsAsync (Foundation.NSString[] itemIdentifiers, CoreGraphics.CGSize size, NSFileProviderExtensionFetchThumbnailsHandler perThumbnailCompletionHandler, Foundation.NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual FileProvider.INSFileProviderEnumerator GetEnumerator (string containerItemIdentifier, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public FileProvider.INSFileProviderItem GetItem (FileProvider.NSFileProviderItemIdentifier identifier, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual FileProvider.INSFileProviderItem GetItem (Foundation.NSString identifier, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ImportDocument (Foundation.NSUrl fileUrl, string parentItemIdentifier, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; ImportDocumentAsync (Foundation.NSUrl fileUrl, string parentItemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RenameItem (string itemIdentifier, string itemName, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; RenameItemAsync (string itemIdentifier, string itemName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReparentItem (string itemIdentifier, string parentItemIdentifier, string newName, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; ReparentItemAsync (string itemIdentifier, string parentItemIdentifier, string newName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetFavoriteRank (Foundation.NSNumber favoriteRank, string itemIdentifier, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; SetFavoriteRankAsync (Foundation.NSNumber favoriteRank, string itemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLastUsedDate (Foundation.NSDate lastUsedDate, string itemIdentifier, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; SetLastUsedDateAsync (Foundation.NSDate lastUsedDate, string itemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTagData (Foundation.NSData tagData, string itemIdentifier, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; SetTagDataAsync (Foundation.NSData tagData, string itemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TrashItem (string itemIdentifier, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; TrashItemAsync (string itemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UntrashItem (string itemIdentifier, string parentItemIdentifier, System.Action&lt;FileProvider.INSFileProviderItem,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;FileProvider.INSFileProviderItem&gt; UntrashItemAsync (string itemIdentifier, string parentItemIdentifier);</span>
</pre>
</div>

</div> <!-- end type NSFileProviderExtension -->
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
<!-- start type UICollectionView --> <div>
<h3>Type Changed: UIKit.UICollectionView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIDataSourceTranslating</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUICollectionViewDragDelegate DragDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DragInteractionEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUICollectionViewDropDelegate DropDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasActiveDrag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasActiveDrop { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasUncommittedUpdates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UICollectionViewReorderingCadence ReorderingCadence { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
</pre>
</div>

</div> <!-- end type UICollectionView -->
<!-- start type UICollectionViewCell --> <div>
<h3>Type Changed: UIKit.UICollectionViewCell</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DragStateDidChange (UICollectionViewCellDragState dragState);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewCell -->
<!-- start type UICollectionViewController --> <div>
<h3>Type Changed: UIKit.UICollectionViewController</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSpringLoadItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath, IUISpringLoadedInteractionContext context);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewController -->
<!-- start type UICollectionViewDelegate --> <div>
<h3>Type Changed: UIKit.UICollectionViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSpringLoadItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath, IUISpringLoadedInteractionContext context);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewDelegate -->
<!-- start type UICollectionViewDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UICollectionViewDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldSpringLoadItem (IUICollectionViewDelegate This, UICollectionView collectionView, Foundation.NSIndexPath indexPath, IUISpringLoadedInteractionContext context);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewDelegate_Extensions -->
<!-- start type UICollectionViewFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UICollectionViewFocusUpdateContext</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This cannot be directly created.")]
	public UICollectionViewFocusUpdateContext ();</span>
</div></pre>

</div> <!-- end type UICollectionViewFocusUpdateContext -->
<!-- start type UICollectionViewSource --> <div>
<h3>Type Changed: UIKit.UICollectionViewSource</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSpringLoadItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath, IUISpringLoadedInteractionContext context);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewSource -->
<!-- start type UIColor --> <div>
<h3>Type Changed: UIKit.UIColor</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public UIColor (Foundation.NSData providerData, string typeIdentifier, Foundation.NSError outError);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableTypeIdentifiersForItemProvider { get; }</span>
</pre>
</div>
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
<!-- start type UIFocusAnimationCoordinator --> <div>
<h3>Type Changed: UIKit.UIFocusAnimationCoordinator</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedFocusingAnimations (System.Action&lt;IUIFocusAnimationContext&gt; animations, System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AddCoordinatedFocusingAnimationsAsync (System.Action&lt;IUIFocusAnimationContext&gt; animations);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedUnfocusingAnimations (System.Action&lt;IUIFocusAnimationContext&gt; animations, System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AddCoordinatedUnfocusingAnimationsAsync (System.Action&lt;IUIFocusAnimationContext&gt; animations);</span>
</pre>
</div>

</div> <!-- end type UIFocusAnimationCoordinator -->
<!-- start type UIFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UIFocusUpdateContext</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This cannot be directly created.")]
	public UIFocusUpdateContext ();</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnimationCoordinatorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidUpdateNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Key { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovementDidFailNotification { get; }</span>
</pre>
</div>

</div> <!-- end type UIFocusUpdateContext -->
<!-- start type UIImage --> <div>
<h3>Type Changed: UIKit.UIImage</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public UIImage (Foundation.NSData providerData, string typeIdentifier, Foundation.NSError outError);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableTypeIdentifiersForItemProvider { get; }</span>
</pre>
</div>

</div> <!-- end type UIImage -->
<!-- start type UIModalPresentationStyle --> <div>
<h3>Type Changed: UIKit.UIModalPresentationStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BlurOverFullScreen = 8,</span>
</pre>
</div>

</div> <!-- end type UIModalPresentationStyle -->
<!-- start type UISearchBar --> <div>
<h3>Type Changed: UIKit.UISearchBar</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UISearchBar -->
<!-- start type UISplitViewController --> <div>
<h3>Type Changed: UIKit.UISplitViewController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UISplitViewControllerPrimaryEdge PrimaryEdge { get; set; }</span>
</pre>
</div>

</div> <!-- end type UISplitViewController -->
<!-- start type UIStackView --> <div>
<h3>Type Changed: UIKit.UIStackView</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual nfloat GetCustomSpacing (UIView arrangedSubview);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCustomSpacing (nfloat spacing, UIView arrangedSubview);</span>
</pre>
</div>

</div> <!-- end type UIStackView -->
<!-- start type UITableView --> <div>
<h3>Type Changed: UIKit.UITableView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIDataSourceTranslating</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUITableViewDragDelegate DragDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DragInteractionEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUITableViewDropDelegate DropDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasActiveDrag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasActiveDrop { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasUncommittedUpdates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InsetsContentViewsToSafeArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITableViewSeparatorInsetReference SeparatorInsetReference { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformBatchUpdates (System.Action updates, System.Action&lt;bool&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PerformBatchUpdatesAsync (System.Action updates);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
</pre>
</div>

</div> <!-- end type UITableView -->
<!-- start type UITableViewCell --> <div>
<h3>Type Changed: UIKit.UITableViewCell</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UserInteractionEnabledWhileDragging { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DragStateDidChange (UITableViewCellDragState dragState);</span>
</pre>
</div>

</div> <!-- end type UITableViewCell -->
<!-- start type UITableViewController --> <div>
<h3>Type Changed: UIKit.UITableViewController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual UISwipeActionsConfiguration GetLeadingSwipeActionsConfiguration (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UISwipeActionsConfiguration GetTrailingSwipeActionsConfiguration (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSpringLoadRow (UITableView tableView, Foundation.NSIndexPath indexPath, IUISpringLoadedInteractionContext context);</span>
</pre>
</div>

</div> <!-- end type UITableViewController -->
<!-- start type UITableViewDelegate --> <div>
<h3>Type Changed: UIKit.UITableViewDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual UISwipeActionsConfiguration GetLeadingSwipeActionsConfiguration (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UISwipeActionsConfiguration GetTrailingSwipeActionsConfiguration (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSpringLoadRow (UITableView tableView, Foundation.NSIndexPath indexPath, IUISpringLoadedInteractionContext context);</span>
</pre>
</div>

</div> <!-- end type UITableViewDelegate -->
<!-- start type UITableViewDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UITableViewDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UISwipeActionsConfiguration GetLeadingSwipeActionsConfiguration (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UISwipeActionsConfiguration GetTrailingSwipeActionsConfiguration (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldSpringLoadRow (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath, IUISpringLoadedInteractionContext context);</span>
</pre>
</div>

</div> <!-- end type UITableViewDelegate_Extensions -->
<!-- start type UITableViewSource --> <div>
<h3>Type Changed: UIKit.UITableViewSource</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual UISwipeActionsConfiguration GetLeadingSwipeActionsConfiguration (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UISwipeActionsConfiguration GetTrailingSwipeActionsConfiguration (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSpringLoadRow (UITableView tableView, Foundation.NSIndexPath indexPath, IUISpringLoadedInteractionContext context);</span>
</pre>
</div>

</div> <!-- end type UITableViewSource -->
<!-- start type UITextContentType --> <div>
<h3>Type Changed: UIKit.UITextContentType</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Password { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Username { get; }</span>
</pre>
</div>

</div> <!-- end type UITextContentType -->
<!-- start type UITextDocumentProxy --> <div>
<h3>Type Changed: UIKit.UITextDocumentProxy</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid DocumentIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SelectedText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextDocumentProxy -->
<!-- start type UITextDocumentProxy_Extensions --> <div>
<h3>Type Changed: UIKit.UITextDocumentProxy_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUuid GetDocumentIdentifier (IUITextDocumentProxy This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetSelectedText (IUITextDocumentProxy This);</span>
</pre>
</div>

</div> <!-- end type UITextDocumentProxy_Extensions -->
<!-- start type UITextField --> <div>
<h3>Type Changed: UIKit.UITextField</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextField -->
<!-- start type UITextInputTraits_Extensions --> <div>
<h3>Type Changed: UIKit.UITextInputTraits_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartDashesType GetSmartDashesType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartInsertDeleteType GetSmartInsertDeleteType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartQuotesType GetSmartQuotesType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartDashesType (IUITextInputTraits This, UITextSmartDashesType value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartInsertDeleteType (IUITextInputTraits This, UITextSmartInsertDeleteType value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartQuotesType (IUITextInputTraits This, UITextSmartQuotesType value);</span>
</pre>
</div>

</div> <!-- end type UITextInputTraits_Extensions -->
<!-- start type UITextView --> <div>
<h3>Type Changed: UIKit.UITextView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextView -->
<!-- start type UIView --> <div>
<h3>Type Changed: UIKit.UIView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIInteraction[] Interactions { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddInteraction (IUIInteraction interaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveInteraction (IUIInteraction interaction);</span>
</pre>
</div>

</div> <!-- end type UIView -->
<div> <!-- start type IUICollectionViewDragDelegate -->
<h3>New Type UIKit.IUICollectionViewDragDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUICollectionViewDragDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForBeginningDragSession (UICollectionView collectionView, IUIDragSession session, Foundation.NSIndexPath indexPath);</span>
}
</pre>
</div> <!-- end type IUICollectionViewDragDelegate -->
<div> <!-- start type IUICollectionViewDropCoordinator -->
<h3>New Type UIKit.IUICollectionViewDropCoordinator</h3>
<pre class='added' data-is-non-breaking="">
public interface IUICollectionViewDropCoordinator : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexPath DestinationIndexPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUICollectionViewDropItem[] Items { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UICollectionViewDropProposal Proposal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIDropSession Session { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIDragAnimating DropItemIntoItem (UIDragItem dragItem, Foundation.NSIndexPath itemIndexPath, CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIDragAnimating DropItemToItem (UIDragItem dragItem, Foundation.NSIndexPath itemIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUICollectionViewDropPlaceholderContext DropItemToPlaceholder (UIDragItem dragItem, UICollectionViewDropPlaceholder placeholder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIDragAnimating DropItemToTarget (UIDragItem dragItem, UIDragPreviewTarget target);</span>
}
</pre>
</div> <!-- end type IUICollectionViewDropCoordinator -->
<div> <!-- start type IUICollectionViewDropDelegate -->
<h3>New Type UIKit.IUICollectionViewDropDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUICollectionViewDropDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformDrop (UICollectionView collectionView, IUICollectionViewDropCoordinator coordinator);</span>
}
</pre>
</div> <!-- end type IUICollectionViewDropDelegate -->
<div> <!-- start type IUICollectionViewDropItem -->
<h3>New Type UIKit.IUICollectionViewDropItem</h3>
<pre class='added' data-is-non-breaking="">
public interface IUICollectionViewDropItem : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragItem DragItem { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize PreviewSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexPath SourceIndexPath { get; }</span>
}
</pre>
</div> <!-- end type IUICollectionViewDropItem -->
<div> <!-- start type IUICollectionViewDropPlaceholderContext -->
<h3>New Type UIKit.IUICollectionViewDropPlaceholderContext</h3>
<pre class='added' data-is-non-breaking="">
public interface IUICollectionViewDropPlaceholderContext : ObjCRuntime.INativeObject, System.IDisposable, IUIDragAnimating {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragItem DragItem { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CommitInsertion (System.Action&lt;Foundation.NSIndexPath&gt; dataSourceUpdates);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DeletePlaceholder ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeedsCellUpdate ();</span>
}
</pre>
</div> <!-- end type IUICollectionViewDropPlaceholderContext -->
<div> <!-- start type IUIDataSourceTranslating -->
<h3>New Type UIKit.IUIDataSourceTranslating</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDataSourceTranslating : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
}
</pre>
</div> <!-- end type IUIDataSourceTranslating -->
<div> <!-- start type IUIDragAnimating -->
<h3>New Type UIKit.IUIDragAnimating</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDragAnimating : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimations (System.Action animations);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCompletion (System.Action&lt;UIViewAnimatingPosition&gt; completion);</span>
}
</pre>
</div> <!-- end type IUIDragAnimating -->
<div> <!-- start type IUIDragDropSession -->
<h3>New Type UIKit.IUIDragDropSession</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDragDropSession : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsMoveOperation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragItem[] Items { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RestrictedToDraggingApplication { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanLoadObjects (ObjCRuntime.Class itemProviderReadingClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool HasConformingItems (string[] typeIdentifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint LocationInView (UIView view);</span>
}
</pre>
</div> <!-- end type IUIDragDropSession -->
<div> <!-- start type IUIDragInteractionDelegate -->
<h3>New Type UIKit.IUIDragInteractionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDragInteractionDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForBeginningSession (UIDragInteraction interaction, IUIDragSession session);</span>
}
</pre>
</div> <!-- end type IUIDragInteractionDelegate -->
<div> <!-- start type IUIDragSession -->
<h3>New Type UIKit.IUIDragSession</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDragSession : ObjCRuntime.INativeObject, System.IDisposable, IUIDragDropSession {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject LocalContext { get; set; }</span>
}
</pre>
</div> <!-- end type IUIDragSession -->
<div> <!-- start type IUIDropInteractionDelegate -->
<h3>New Type UIKit.IUIDropInteractionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDropInteractionDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IUIDropInteractionDelegate -->
<div> <!-- start type IUIDropSession -->
<h3>New Type UIKit.IUIDropSession</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDropSession : Foundation.INSProgressReporting, ObjCRuntime.INativeObject, System.IDisposable, IUIDragDropSession {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIDragSession LocalDragSession { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDropSessionProgressIndicatorStyle ProgressIndicatorStyle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSProgress LoadObjects (ObjCRuntime.Class itemProviderReadingClass, System.Action&lt;Foundation.INSItemProviderReading[]&gt; completion);</span>
}
</pre>
</div> <!-- end type IUIDropSession -->
<div> <!-- start type IUIFocusAnimationContext -->
<h3>New Type UIKit.IUIFocusAnimationContext</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIFocusAnimationContext : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
}
</pre>
</div> <!-- end type IUIFocusAnimationContext -->
<div> <!-- start type IUIFocusDebuggerOutput -->
<h3>New Type UIKit.IUIFocusDebuggerOutput</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIFocusDebuggerOutput : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IUIFocusDebuggerOutput -->
<div> <!-- start type IUIInteraction -->
<h3>New Type UIKit.IUIInteraction</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIInteraction : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView View { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidMoveToView (UIView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillMoveToView (UIView view);</span>
}
</pre>
</div> <!-- end type IUIInteraction -->
<div> <!-- start type IUIPasteConfigurationSupporting -->
<h3>New Type UIKit.IUIPasteConfigurationSupporting</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIPasteConfigurationSupporting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIPasteConfiguration PasteConfiguration { get; set; }</span>
}
</pre>
</div> <!-- end type IUIPasteConfigurationSupporting -->
<div> <!-- start type IUISpringLoadedInteractionBehavior -->
<h3>New Type UIKit.IUISpringLoadedInteractionBehavior</h3>
<pre class='added' data-is-non-breaking="">
public interface IUISpringLoadedInteractionBehavior : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAllowInteraction (UISpringLoadedInteraction interaction, IUISpringLoadedInteractionContext context);</span>
}
</pre>
</div> <!-- end type IUISpringLoadedInteractionBehavior -->
<div> <!-- start type IUISpringLoadedInteractionContext -->
<h3>New Type UIKit.IUISpringLoadedInteractionContext</h3>
<pre class='added' data-is-non-breaking="">
public interface IUISpringLoadedInteractionContext : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UISpringLoadedInteractionEffectState State { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject TargetItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView TargetView { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint LocationInView (UIView view);</span>
}
</pre>
</div> <!-- end type IUISpringLoadedInteractionContext -->
<div> <!-- start type IUISpringLoadedInteractionEffect -->
<h3>New Type UIKit.IUISpringLoadedInteractionEffect</h3>
<pre class='added' data-is-non-breaking="">
public interface IUISpringLoadedInteractionEffect : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChange (UISpringLoadedInteraction interaction, IUISpringLoadedInteractionContext context);</span>
}
</pre>
</div> <!-- end type IUISpringLoadedInteractionEffect -->
<div> <!-- start type IUISpringLoadedInteractionSupporting -->
<h3>New Type UIKit.IUISpringLoadedInteractionSupporting</h3>
<pre class='added' data-is-non-breaking="">
public interface IUISpringLoadedInteractionSupporting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SpringLoaded { get; set; }</span>
}
</pre>
</div> <!-- end type IUISpringLoadedInteractionSupporting -->
<div> <!-- start type IUITableViewDragDelegate -->
<h3>New Type UIKit.IUITableViewDragDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITableViewDragDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForBeginningDragSession (UITableView tableView, IUIDragSession session, Foundation.NSIndexPath indexPath);</span>
}
</pre>
</div> <!-- end type IUITableViewDragDelegate -->
<div> <!-- start type IUITableViewDropCoordinator -->
<h3>New Type UIKit.IUITableViewDropCoordinator</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITableViewDropCoordinator : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexPath DestinationIndexPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUITableViewDropItem[] Items { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITableViewDropProposal Proposal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIDropSession Session { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIDragAnimating DropItemIntoRow (UIDragItem dragItem, Foundation.NSIndexPath indexPath, CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUITableViewDropPlaceholderContext DropItemToPlaceholder (UIDragItem dragItem, UITableViewDropPlaceholder placeholder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIDragAnimating DropItemToRow (UIDragItem dragItem, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIDragAnimating DropItemToTarget (UIDragItem dragItem, UIDragPreviewTarget target);</span>
}
</pre>
</div> <!-- end type IUITableViewDropCoordinator -->
<div> <!-- start type IUITableViewDropDelegate -->
<h3>New Type UIKit.IUITableViewDropDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITableViewDropDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformDrop (UITableView tableView, IUITableViewDropCoordinator coordinator);</span>
}
</pre>
</div> <!-- end type IUITableViewDropDelegate -->
<div> <!-- start type IUITableViewDropItem -->
<h3>New Type UIKit.IUITableViewDropItem</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITableViewDropItem : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragItem DragItem { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize PreviewSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexPath SourceIndexPath { get; }</span>
}
</pre>
</div> <!-- end type IUITableViewDropItem -->
<div> <!-- start type IUITableViewDropPlaceholderContext -->
<h3>New Type UIKit.IUITableViewDropPlaceholderContext</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITableViewDropPlaceholderContext : ObjCRuntime.INativeObject, System.IDisposable, IUIDragAnimating {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragItem DragItem { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CommitInsertion (System.Action&lt;Foundation.NSIndexPath&gt; dataSourceUpdates);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DeletePlaceholder ();</span>
}
</pre>
</div> <!-- end type IUITableViewDropPlaceholderContext -->
<div> <!-- start type IUITextDragDelegate -->
<h3>New Type UIKit.IUITextDragDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextDragDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IUITextDragDelegate -->
<div> <!-- start type IUITextDragRequest -->
<h3>New Type UIKit.IUITextDragRequest</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextDragRequest : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextRange DragRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIDragSession DragSession { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragItem[] ExistingItems { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Selected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragItem[] SuggestedItems { get; }</span>
}
</pre>
</div> <!-- end type IUITextDragRequest -->
<div> <!-- start type IUITextDraggable -->
<h3>New Type UIKit.IUITextDraggable</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextDraggable : ObjCRuntime.INativeObject, System.IDisposable, IUIKeyInput, IUITextInput, IUITextInputTraits {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TextDragActive { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUITextDragDelegate TextDragDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragInteraction TextDragInteraction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextDragOptions TextDragOptions { get; set; }</span>
}
</pre>
</div> <!-- end type IUITextDraggable -->
<div> <!-- start type IUITextDropDelegate -->
<h3>New Type UIKit.IUITextDropDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextDropDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IUITextDropDelegate -->
<div> <!-- start type IUITextDropRequest -->
<h3>New Type UIKit.IUITextDropRequest</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextDropRequest : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextPosition DropPosition { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIDropSession DropSession { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SameView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextDropProposal SuggestedProposal { get; }</span>
}
</pre>
</div> <!-- end type IUITextDropRequest -->
<div> <!-- start type IUITextDroppable -->
<h3>New Type UIKit.IUITextDroppable</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextDroppable : ObjCRuntime.INativeObject, System.IDisposable, IUIKeyInput, IUIPasteConfigurationSupporting, IUITextInput, IUITextInputTraits, IUITextPasteConfigurationSupporting {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TextDropActive { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUITextDropDelegate TextDropDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDropInteraction TextDropInteraction { get; }</span>
}
</pre>
</div> <!-- end type IUITextDroppable -->
<div> <!-- start type IUITextPasteConfigurationSupporting -->
<h3>New Type UIKit.IUITextPasteConfigurationSupporting</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextPasteConfigurationSupporting : ObjCRuntime.INativeObject, System.IDisposable, IUIPasteConfigurationSupporting {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IUITextPasteDelegate PasteDelegate { get; set; }</span>
}
</pre>
</div> <!-- end type IUITextPasteConfigurationSupporting -->
<div> <!-- start type IUITextPasteDelegate -->
<h3>New Type UIKit.IUITextPasteDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextPasteDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IUITextPasteDelegate -->
<div> <!-- start type IUITextPasteItem -->
<h3>New Type UIKit.IUITextPasteItem</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITextPasteItem : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; DefaultAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSItemProvider ItemProvider { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject LocalObject { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAttachmentResult (NSTextAttachment textAttachment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAttributedStringResult (Foundation.NSAttributedString string);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDefaultResult ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNoResult ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetStringResult (string string);</span>
}
</pre>
</div> <!-- end type IUITextPasteItem -->
<div> <!-- start type NSFileProviderExtensionFetchThumbnailsHandler -->
<h3>New Type UIKit.NSFileProviderExtensionFetchThumbnailsHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSFileProviderExtensionFetchThumbnailsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderExtensionFetchThumbnailsHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSString identifier, Foundation.NSData imageData, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSString identifier, Foundation.NSData imageData, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type NSFileProviderExtensionFetchThumbnailsHandler -->
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
<div> <!-- start type UICollectionViewCellDragState -->
<h3>New Type UIKit.UICollectionViewCellDragState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UICollectionViewCellDragState {
	<span class='added added-field ' data-is-non-breaking="">Dragging = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Lifting = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UICollectionViewCellDragState -->
<div> <!-- start type UICollectionViewDragDelegate -->
<h3>New Type UIKit.UICollectionViewDragDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class UICollectionViewDragDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUICollectionViewDragDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDragDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDragDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDragDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DragSessionAllowsMoveOperation (UICollectionView collectionView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DragSessionDidEnd (UICollectionView collectionView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DragSessionIsRestrictedToDraggingApplication (UICollectionView collectionView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DragSessionWillBegin (UICollectionView collectionView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragPreviewParameters GetDragPreviewParameters (UICollectionView collectionView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForAddingToDragSession (UICollectionView collectionView, IUIDragSession session, Foundation.NSIndexPath indexPath, CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForBeginningDragSession (UICollectionView collectionView, IUIDragSession session, Foundation.NSIndexPath indexPath);</span>
}
</pre>
</div> <!-- end type UICollectionViewDragDelegate -->
<div> <!-- start type UICollectionViewDragDelegate_Extensions -->
<h3>New Type UIKit.UICollectionViewDragDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UICollectionViewDragDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool DragSessionAllowsMoveOperation (IUICollectionViewDragDelegate This, UICollectionView collectionView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DragSessionDidEnd (IUICollectionViewDragDelegate This, UICollectionView collectionView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool DragSessionIsRestrictedToDraggingApplication (IUICollectionViewDragDelegate This, UICollectionView collectionView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DragSessionWillBegin (IUICollectionViewDragDelegate This, UICollectionView collectionView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragPreviewParameters GetDragPreviewParameters (IUICollectionViewDragDelegate This, UICollectionView collectionView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragItem[] GetItemsForAddingToDragSession (IUICollectionViewDragDelegate This, UICollectionView collectionView, IUIDragSession session, Foundation.NSIndexPath indexPath, CoreGraphics.CGPoint point);</span>
}
</pre>
</div> <!-- end type UICollectionViewDragDelegate_Extensions -->
<div> <!-- start type UICollectionViewDropDelegate -->
<h3>New Type UIKit.UICollectionViewDropDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class UICollectionViewDropDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUICollectionViewDropDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDropDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDropDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDropDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanHandleDropSession (UICollectionView collectionView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidEnd (UICollectionView collectionView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidEnter (UICollectionView collectionView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidExit (UICollectionView collectionView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UICollectionViewDropProposal DropSessionDidUpdate (UICollectionView collectionView, IUIDropSession session, Foundation.NSIndexPath destinationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragPreviewParameters GetDropPreviewParameters (UICollectionView collectionView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformDrop (UICollectionView collectionView, IUICollectionViewDropCoordinator coordinator);</span>
}
</pre>
</div> <!-- end type UICollectionViewDropDelegate -->
<div> <!-- start type UICollectionViewDropDelegate_Extensions -->
<h3>New Type UIKit.UICollectionViewDropDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UICollectionViewDropDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanHandleDropSession (IUICollectionViewDropDelegate This, UICollectionView collectionView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidEnd (IUICollectionViewDropDelegate This, UICollectionView collectionView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidEnter (IUICollectionViewDropDelegate This, UICollectionView collectionView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidExit (IUICollectionViewDropDelegate This, UICollectionView collectionView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UICollectionViewDropProposal DropSessionDidUpdate (IUICollectionViewDropDelegate This, UICollectionView collectionView, IUIDropSession session, Foundation.NSIndexPath destinationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragPreviewParameters GetDropPreviewParameters (IUICollectionViewDropDelegate This, UICollectionView collectionView, Foundation.NSIndexPath indexPath);</span>
}
</pre>
</div> <!-- end type UICollectionViewDropDelegate_Extensions -->
<div> <!-- start type UICollectionViewDropIntent -->
<h3>New Type UIKit.UICollectionViewDropIntent</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UICollectionViewDropIntent {
	<span class='added added-field ' data-is-non-breaking="">InsertAtDestinationIndexPath = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InsertIntoDestinationIndexPath = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type UICollectionViewDropIntent -->
<div> <!-- start type UICollectionViewDropPlaceholder -->
<h3>New Type UIKit.UICollectionViewDropPlaceholder</h3>
<pre class='added' data-is-non-breaking="">
public class UICollectionViewDropPlaceholder : UIKit.UICollectionViewPlaceholder, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UICollectionViewDropPlaceholder ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDropPlaceholder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDropPlaceholder (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UICollectionViewDropPlaceholder (Foundation.NSIndexPath insertionIndexPath, string reuseIdentifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;UICollectionViewCell,UIKit.UIDragPreviewParameters&gt; PreviewParametersProvider { get; set; }</span>
}
</pre>
</div> <!-- end type UICollectionViewDropPlaceholder -->
<div> <!-- start type UICollectionViewDropProposal -->
<h3>New Type UIKit.UICollectionViewDropProposal</h3>
<pre class='added' data-is-non-breaking="">
public class UICollectionViewDropProposal : UIKit.UIDropProposal, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDropProposal (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewDropProposal (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UICollectionViewDropProposal (UIDropOperation operation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UICollectionViewDropProposal (UIDropOperation operation, UICollectionViewDropIntent intent);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UICollectionViewDropIntent Intent { get; }</span>
}
</pre>
</div> <!-- end type UICollectionViewDropProposal -->
<div> <!-- start type UICollectionViewPlaceholder -->
<h3>New Type UIKit.UICollectionViewPlaceholder</h3>
<pre class='added' data-is-non-breaking="">
public class UICollectionViewPlaceholder : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewPlaceholder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICollectionViewPlaceholder (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UICollectionViewPlaceholder (Foundation.NSIndexPath insertionIndexPath, string reuseIdentifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;UICollectionViewCell&gt; CellUpdateHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type UICollectionViewPlaceholder -->
<div> <!-- start type UICollectionViewReorderingCadence -->
<h3>New Type UIKit.UICollectionViewReorderingCadence</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UICollectionViewReorderingCadence {
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Immediate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Slow = 2,</span>
}
</pre>
</div> <!-- end type UICollectionViewReorderingCadence -->
<div> <!-- start type UIContextualAction -->
<h3>New Type UIKit.UIContextualAction</h3>
<pre class='added' data-is-non-breaking="">
public class UIContextualAction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIContextualAction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIContextualAction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIContextualActionHandler Handler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIImage Image { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIContextualActionStyle Style { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UIContextualAction FromContextualActionStyle (UIContextualActionStyle style, string title, UIContextualActionHandler handler);</span>
}
</pre>
</div> <!-- end type UIContextualAction -->
<div> <!-- start type UIContextualActionCompletionHandler -->
<h3>New Type UIKit.UIContextualActionCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UIContextualActionCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIContextualActionCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (bool finished, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (bool finished);</span>
}
</pre>
</div> <!-- end type UIContextualActionCompletionHandler -->
<div> <!-- start type UIContextualActionHandler -->
<h3>New Type UIKit.UIContextualActionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UIContextualActionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIContextualActionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UIContextualAction action, UIView sourceView, UIContextualActionCompletionHandler completionHandler, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (UIContextualAction action, UIView sourceView, UIContextualActionCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type UIContextualActionHandler -->
<div> <!-- start type UIContextualActionStyle -->
<h3>New Type UIKit.UIContextualActionStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIContextualActionStyle {
	<span class='added added-field ' data-is-non-breaking="">Destructive = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 0,</span>
}
</pre>
</div> <!-- end type UIContextualActionStyle -->
<div> <!-- start type UIDataSourceTranslating -->
<h3>New Type UIKit.UIDataSourceTranslating</h3>
<pre class='added' data-is-non-breaking="">
public abstract class UIDataSourceTranslating : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIDataSourceTranslating {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDataSourceTranslating ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDataSourceTranslating (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDataSourceTranslating (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
}
</pre>
</div> <!-- end type UIDataSourceTranslating -->
<div> <!-- start type UIDocumentBrowserActionAvailability -->
<h3>New Type UIKit.UIDocumentBrowserActionAvailability</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum UIDocumentBrowserActionAvailability {
	<span class='added added-field ' data-is-non-breaking="">Menu = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NavigationBar = 2,</span>
}
</pre>
</div> <!-- end type UIDocumentBrowserActionAvailability -->
<div> <!-- start type UIDocumentBrowserImportMode -->
<h3>New Type UIKit.UIDocumentBrowserImportMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIDocumentBrowserImportMode {
	<span class='added added-field ' data-is-non-breaking="">Copy = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Move = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UIDocumentBrowserImportMode -->
<div> <!-- start type UIDocumentBrowserUserInterfaceStyle -->
<h3>New Type UIKit.UIDocumentBrowserUserInterfaceStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIDocumentBrowserUserInterfaceStyle {
	<span class='added added-field ' data-is-non-breaking="">Dark = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Light = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">White = 0,</span>
}
</pre>
</div> <!-- end type UIDocumentBrowserUserInterfaceStyle -->
<div> <!-- start type UIDragDropSessionExtensions -->
<h3>New Type UIKit.UIDragDropSessionExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIDragDropSessionExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanLoadObjects (IUIDragDropSession session, System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSProgress LoadObjects (IUIDropSession session, System.Type type, System.Action&lt;Foundation.INSItemProviderReading[]&gt; completion);</span>
}
</pre>
</div> <!-- end type UIDragDropSessionExtensions -->
<div> <!-- start type UIDragInteraction -->
<h3>New Type UIKit.UIDragInteraction</h3>
<pre class='added' data-is-non-breaking="">
public class UIDragInteraction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIInteraction {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragInteraction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragInteraction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIDragInteraction (IUIDragInteractionDelegate delegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsSimultaneousRecognitionDuringLift { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIDragInteractionDelegate Delegate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool EnabledByDefault { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView View { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidMoveToView (UIView view);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillMoveToView (UIView view);</span>
}
</pre>
</div> <!-- end type UIDragInteraction -->
<div> <!-- start type UIDragInteractionDelegate -->
<h3>New Type UIKit.UIDragInteractionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class UIDragInteractionDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIDragInteractionDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragInteractionDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragInteractionDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragInteractionDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForAddingToSession (UIDragInteraction interaction, IUIDragSession session, CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForBeginningSession (UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITargetedDragPreview GetPreviewForCancellingItem (UIDragInteraction interaction, UIDragItem item, UITargetedDragPreview defaultPreview);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITargetedDragPreview GetPreviewForLiftingItem (UIDragInteraction interaction, UIDragItem item, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIDragSession GetSessionForAddingItems (UIDragInteraction interaction, IUIDragSession[] sessions, CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PrefersFullSizePreviews (UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SessionAllowsMoveOperation (UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionDidEnd (UIDragInteraction interaction, IUIDragSession session, UIDropOperation operation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionDidMove (UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionDidTransferItems (UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SessionIsRestrictedToDraggingApplication (UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionWillBegin (UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionWillEnd (UIDragInteraction interaction, IUIDragSession session, UIDropOperation operation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillAddItems (UIDragInteraction interaction, IUIDragSession session, UIDragItem[] items, UIDragInteraction addingInteraction);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillAnimateCancel (UIDragInteraction interaction, UIDragItem item, IUIDragAnimating animator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillAnimateLift (UIDragInteraction interaction, IUIDragAnimating animator, IUIDragSession session);</span>
}
</pre>
</div> <!-- end type UIDragInteractionDelegate -->
<div> <!-- start type UIDragInteractionDelegate_Extensions -->
<h3>New Type UIKit.UIDragInteractionDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIDragInteractionDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UIDragItem[] GetItemsForAddingToSession (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session, CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITargetedDragPreview GetPreviewForCancellingItem (IUIDragInteractionDelegate This, UIDragInteraction interaction, UIDragItem item, UITargetedDragPreview defaultPreview);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITargetedDragPreview GetPreviewForLiftingItem (IUIDragInteractionDelegate This, UIDragInteraction interaction, UIDragItem item, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IUIDragSession GetSessionForAddingItems (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession[] sessions, CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool PrefersFullSizePreviews (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool SessionAllowsMoveOperation (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionDidEnd (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session, UIDropOperation operation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionDidMove (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionDidTransferItems (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool SessionIsRestrictedToDraggingApplication (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionWillBegin (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionWillEnd (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session, UIDropOperation operation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillAddItems (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragSession session, UIDragItem[] items, UIDragInteraction addingInteraction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillAnimateCancel (IUIDragInteractionDelegate This, UIDragInteraction interaction, UIDragItem item, IUIDragAnimating animator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillAnimateLift (IUIDragInteractionDelegate This, UIDragInteraction interaction, IUIDragAnimating animator, IUIDragSession session);</span>
}
</pre>
</div> <!-- end type UIDragInteractionDelegate_Extensions -->
<div> <!-- start type UIDragItem -->
<h3>New Type UIKit.UIDragItem</h3>
<pre class='added' data-is-non-breaking="">
public class UIDragItem : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIDragItem (Foundation.NSItemProvider itemProvider);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragItem (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSItemProvider ItemProvider { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject LocalObject { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;UIDragPreview&gt; PreviewProvider { get; set; }</span>
}
</pre>
</div> <!-- end type UIDragItem -->
<div> <!-- start type UIDragPreview -->
<h3>New Type UIKit.UIDragPreview</h3>
<pre class='added' data-is-non-breaking="">
public class UIDragPreview : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragPreview (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragPreview (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIDragPreview (UIView view);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIDragPreview (UIView view, UIDragPreviewParameters parameters);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragPreviewParameters Parameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView View { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragPreview GetPreview (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragPreview GetPreview (Foundation.NSUrl url, string title);</span>
}
</pre>
</div> <!-- end type UIDragPreview -->
<div> <!-- start type UIDragPreviewParameters -->
<h3>New Type UIKit.UIDragPreviewParameters</h3>
<pre class='added' data-is-non-breaking="">
public class UIDragPreviewParameters : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIDragPreviewParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragPreviewParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIDragPreviewParameters (Foundation.NSValue[] textLineRects);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragPreviewParameters (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIBezierPath VisiblePath { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type UIDragPreviewParameters -->
<div> <!-- start type UIDragPreviewTarget -->
<h3>New Type UIKit.UIDragPreviewTarget</h3>
<pre class='added' data-is-non-breaking="">
public class UIDragPreviewTarget : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragPreviewTarget (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDragPreviewTarget (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIDragPreviewTarget (UIView container, CoreGraphics.CGPoint center);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIDragPreviewTarget (UIView container, CoreGraphics.CGPoint center, CoreGraphics.CGAffineTransform transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint Center { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView Container { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform Transform { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type UIDragPreviewTarget -->
<div> <!-- start type UIDropInteraction -->
<h3>New Type UIKit.UIDropInteraction</h3>
<pre class='added' data-is-non-breaking="">
public class UIDropInteraction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIInteraction {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDropInteraction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDropInteraction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIDropInteraction (IUIDropInteractionDelegate delegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsSimultaneousDropSessions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIDropInteractionDelegate Delegate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView View { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidMoveToView (UIView view);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillMoveToView (UIView view);</span>
}
</pre>
</div> <!-- end type UIDropInteraction -->
<div> <!-- start type UIDropInteractionDelegate -->
<h3>New Type UIKit.UIDropInteractionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class UIDropInteractionDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIDropInteractionDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIDropInteractionDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDropInteractionDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDropInteractionDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanHandleSession (UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ConcludeDrop (UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITargetedDragPreview GetPreviewForDroppingItem (UIDropInteraction interaction, UIDragItem item, UITargetedDragPreview defaultPreview);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformDrop (UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionDidEnd (UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionDidEnter (UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionDidExit (UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDropProposal SessionDidUpdate (UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillAnimateDrop (UIDropInteraction interaction, UIDragItem item, IUIDragAnimating animator);</span>
}
</pre>
</div> <!-- end type UIDropInteractionDelegate -->
<div> <!-- start type UIDropInteractionDelegate_Extensions -->
<h3>New Type UIKit.UIDropInteractionDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIDropInteractionDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanHandleSession (IUIDropInteractionDelegate This, UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ConcludeDrop (IUIDropInteractionDelegate This, UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITargetedDragPreview GetPreviewForDroppingItem (IUIDropInteractionDelegate This, UIDropInteraction interaction, UIDragItem item, UITargetedDragPreview defaultPreview);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PerformDrop (IUIDropInteractionDelegate This, UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionDidEnd (IUIDropInteractionDelegate This, UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionDidEnter (IUIDropInteractionDelegate This, UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionDidExit (IUIDropInteractionDelegate This, UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDropProposal SessionDidUpdate (IUIDropInteractionDelegate This, UIDropInteraction interaction, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillAnimateDrop (IUIDropInteractionDelegate This, UIDropInteraction interaction, UIDragItem item, IUIDragAnimating animator);</span>
}
</pre>
</div> <!-- end type UIDropInteractionDelegate_Extensions -->
<div> <!-- start type UIDropOperation -->
<h3>New Type UIKit.UIDropOperation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIDropOperation {
	<span class='added added-field ' data-is-non-breaking="">Cancel = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Copy = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Forbidden = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Move = 3,</span>
}
</pre>
</div> <!-- end type UIDropOperation -->
<div> <!-- start type UIDropProposal -->
<h3>New Type UIKit.UIDropProposal</h3>
<pre class='added' data-is-non-breaking="">
public class UIDropProposal : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDropProposal (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDropProposal (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIDropProposal (UIDropOperation operation);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDropOperation Operation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Precise { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrefersFullSizePreview { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type UIDropProposal -->
<div> <!-- start type UIDropSessionProgressIndicatorStyle -->
<h3>New Type UIKit.UIDropSessionProgressIndicatorStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIDropSessionProgressIndicatorStyle {
	<span class='added added-field ' data-is-non-breaking="">Default = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UIDropSessionProgressIndicatorStyle -->
<div> <!-- start type UIFocusDebugger -->
<h3>New Type UIKit.UIFocusDebugger</h3>
<pre class='added' data-is-non-breaking="">
public class UIFocusDebugger : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIFocusDebugger ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusDebugger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusDebugger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IUIFocusDebuggerOutput Help { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IUIFocusDebuggerOutput Status { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IUIFocusDebuggerOutput CheckFocusability (IUIFocusItem item);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IUIFocusDebuggerOutput SimulateFocusUpdateRequest (IUIFocusEnvironment environment);</span>
}
</pre>
</div> <!-- end type UIFocusDebugger -->
<div> <!-- start type UIFocusSystem -->
<h3>New Type UIKit.UIFocusSystem</h3>
<pre class='added' data-is-non-breaking="">
public class UIFocusSystem : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusSystem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusSystem (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool Contains (IUIFocusEnvironment environment, IUIFocusEnvironment otherEnvironment);</span>
}
</pre>
</div> <!-- end type UIFocusSystem -->
<div> <!-- start type UIImagePickerControllerImageUrlExportPreset -->
<h3>New Type UIKit.UIImagePickerControllerImageUrlExportPreset</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIImagePickerControllerImageUrlExportPreset {
	<span class='added added-field ' data-is-non-breaking="">Compatible = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Current = 1,</span>
}
</pre>
</div> <!-- end type UIImagePickerControllerImageUrlExportPreset -->
<div> <!-- start type UIPasteConfiguration -->
<h3>New Type UIKit.UIPasteConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class UIPasteConfiguration : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIPasteConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIPasteConfiguration (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIPasteConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIPasteConfiguration (ObjCRuntime.Class itemProviderReadingClass);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIPasteConfiguration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIPasteConfiguration (string[] acceptableTypeIdentifiers);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIPasteConfiguration (System.Type itemProviderReadingType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] AcceptableTypeIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAcceptableTypeIdentifiers (string[] acceptableTypeIdentifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddTypeIdentifiers (ObjCRuntime.Class itemProviderReadingClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddTypeIdentifiers (System.Type itemProviderReadingType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type UIPasteConfiguration -->
<div> <!-- start type UIPasteConfigurationSupporting_Extensions -->
<h3>New Type UIKit.UIPasteConfigurationSupporting_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIPasteConfigurationSupporting_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanPasteItemProviders (IUIPasteConfigurationSupporting This, Foundation.NSItemProvider[] itemProviders);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PasteItemProviders (IUIPasteConfigurationSupporting This, Foundation.NSItemProvider[] itemProviders);</span>
}
</pre>
</div> <!-- end type UIPasteConfigurationSupporting_Extensions -->
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
<div> <!-- start type UISpringLoadedInteraction -->
<h3>New Type UIKit.UISpringLoadedInteraction</h3>
<pre class='added' data-is-non-breaking="">
public class UISpringLoadedInteraction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIInteraction {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UISpringLoadedInteraction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISpringLoadedInteraction (System.Action&lt;UISpringLoadedInteraction,UIKit.IUISpringLoadedInteractionContext&gt; handler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UISpringLoadedInteraction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISpringLoadedInteraction (IUISpringLoadedInteractionBehavior interactionBehavior, IUISpringLoadedInteractionEffect interactionEffect, System.Action&lt;UISpringLoadedInteraction,UIKit.IUISpringLoadedInteractionContext&gt; handler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUISpringLoadedInteractionBehavior InteractionBehavior { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUISpringLoadedInteractionEffect InteractionEffect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView View { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidMoveToView (UIView view);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillMoveToView (UIView view);</span>
}
</pre>
</div> <!-- end type UISpringLoadedInteraction -->
<div> <!-- start type UISpringLoadedInteractionBehavior_Extensions -->
<h3>New Type UIKit.UISpringLoadedInteractionBehavior_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UISpringLoadedInteractionBehavior_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void InteractionDidFinish (IUISpringLoadedInteractionBehavior This, UISpringLoadedInteraction interaction);</span>
}
</pre>
</div> <!-- end type UISpringLoadedInteractionBehavior_Extensions -->
<div> <!-- start type UISpringLoadedInteractionEffectState -->
<h3>New Type UIKit.UISpringLoadedInteractionEffectState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UISpringLoadedInteractionEffectState {
	<span class='added added-field ' data-is-non-breaking="">Activated = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Activating = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Inactive = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Possible = 1,</span>
}
</pre>
</div> <!-- end type UISpringLoadedInteractionEffectState -->
<div> <!-- start type UISwipeActionsConfiguration -->
<h3>New Type UIKit.UISwipeActionsConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class UISwipeActionsConfiguration : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UISwipeActionsConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UISwipeActionsConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIContextualAction[] Actions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PerformsFirstActionWithFullSwipe { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UISwipeActionsConfiguration FromActions (UIContextualAction[] actions);</span>
}
</pre>
</div> <!-- end type UISwipeActionsConfiguration -->
<div> <!-- start type UITableViewCellDragState -->
<h3>New Type UIKit.UITableViewCellDragState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITableViewCellDragState {
	<span class='added added-field ' data-is-non-breaking="">Dragging = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Lifting = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UITableViewCellDragState -->
<div> <!-- start type UITableViewDragDelegate -->
<h3>New Type UIKit.UITableViewDragDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class UITableViewDragDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUITableViewDragDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDragDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDragDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDragDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DragSessionAllowsMoveOperation (UITableView tableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DragSessionDidEnd (UITableView tableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DragSessionIsRestrictedToDraggingApplication (UITableView tableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DragSessionWillBegin (UITableView tableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragPreviewParameters GetDragPreviewParameters (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForAddingToDragSession (UITableView tableView, IUIDragSession session, Foundation.NSIndexPath indexPath, CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForBeginningDragSession (UITableView tableView, IUIDragSession session, Foundation.NSIndexPath indexPath);</span>
}
</pre>
</div> <!-- end type UITableViewDragDelegate -->
<div> <!-- start type UITableViewDragDelegate_Extensions -->
<h3>New Type UIKit.UITableViewDragDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UITableViewDragDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool DragSessionAllowsMoveOperation (IUITableViewDragDelegate This, UITableView tableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DragSessionDidEnd (IUITableViewDragDelegate This, UITableView tableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool DragSessionIsRestrictedToDraggingApplication (IUITableViewDragDelegate This, UITableView tableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DragSessionWillBegin (IUITableViewDragDelegate This, UITableView tableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragPreviewParameters GetDragPreviewParameters (IUITableViewDragDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragItem[] GetItemsForAddingToDragSession (IUITableViewDragDelegate This, UITableView tableView, IUIDragSession session, Foundation.NSIndexPath indexPath, CoreGraphics.CGPoint point);</span>
}
</pre>
</div> <!-- end type UITableViewDragDelegate_Extensions -->
<div> <!-- start type UITableViewDropDelegate -->
<h3>New Type UIKit.UITableViewDropDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class UITableViewDropDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUITableViewDropDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDropDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDropDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDropDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanHandleDropSession (UITableView tableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidEnd (UITableView tableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidEnter (UITableView tableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidExit (UITableView tableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITableViewDropProposal DropSessionDidUpdate (UITableView tableView, IUIDropSession session, Foundation.NSIndexPath destinationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragPreviewParameters GetDropPreviewParameters (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformDrop (UITableView tableView, IUITableViewDropCoordinator coordinator);</span>
}
</pre>
</div> <!-- end type UITableViewDropDelegate -->
<div> <!-- start type UITableViewDropDelegate_Extensions -->
<h3>New Type UIKit.UITableViewDropDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UITableViewDropDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanHandleDropSession (IUITableViewDropDelegate This, UITableView tableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidEnd (IUITableViewDropDelegate This, UITableView tableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidEnter (IUITableViewDropDelegate This, UITableView tableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidExit (IUITableViewDropDelegate This, UITableView tableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITableViewDropProposal DropSessionDidUpdate (IUITableViewDropDelegate This, UITableView tableView, IUIDropSession session, Foundation.NSIndexPath destinationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragPreviewParameters GetDropPreviewParameters (IUITableViewDropDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
}
</pre>
</div> <!-- end type UITableViewDropDelegate_Extensions -->
<div> <!-- start type UITableViewDropIntent -->
<h3>New Type UIKit.UITableViewDropIntent</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITableViewDropIntent {
	<span class='added added-field ' data-is-non-breaking="">Automatic = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">InsertAtDestinationIndexPath = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InsertIntoDestinationIndexPath = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type UITableViewDropIntent -->
<div> <!-- start type UITableViewDropPlaceholder -->
<h3>New Type UIKit.UITableViewDropPlaceholder</h3>
<pre class='added' data-is-non-breaking="">
public class UITableViewDropPlaceholder : UIKit.UITableViewPlaceholder, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITableViewDropPlaceholder ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDropPlaceholder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDropPlaceholder (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITableViewDropPlaceholder (Foundation.NSIndexPath insertionIndexPath, string reuseIdentifier, nfloat rowHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;UITableViewCell,UIKit.UIDragPreviewParameters&gt; PreviewParametersProvider { get; set; }</span>
}
</pre>
</div> <!-- end type UITableViewDropPlaceholder -->
<div> <!-- start type UITableViewDropProposal -->
<h3>New Type UIKit.UITableViewDropProposal</h3>
<pre class='added' data-is-non-breaking="">
public class UITableViewDropProposal : UIKit.UIDropProposal, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDropProposal (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewDropProposal (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITableViewDropProposal (UIDropOperation operation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITableViewDropProposal (UIDropOperation operation, UITableViewDropIntent intent);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITableViewDropIntent Intent { get; }</span>
}
</pre>
</div> <!-- end type UITableViewDropProposal -->
<div> <!-- start type UITableViewPlaceholder -->
<h3>New Type UIKit.UITableViewPlaceholder</h3>
<pre class='added' data-is-non-breaking="">
public class UITableViewPlaceholder : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewPlaceholder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITableViewPlaceholder (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITableViewPlaceholder (Foundation.NSIndexPath insertionIndexPath, string reuseIdentifier, nfloat rowHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;UITableViewCell&gt; CellUpdateHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type UITableViewPlaceholder -->
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
<div> <!-- start type UITargetedDragPreview -->
<h3>New Type UIKit.UITargetedDragPreview</h3>
<pre class='added' data-is-non-breaking="">
public class UITargetedDragPreview : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UITargetedDragPreview (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITargetedDragPreview (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITargetedDragPreview (UIView view);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITargetedDragPreview (UIView view, UIDragPreviewParameters parameters);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITargetedDragPreview (UIView view, UIDragPreviewParameters parameters, UIDragPreviewTarget target);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragPreviewParameters Parameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize Size { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDragPreviewTarget Target { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView View { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITargetedDragPreview GetPreview (Foundation.NSUrl url, UIDragPreviewTarget target);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITargetedDragPreview GetPreview (Foundation.NSUrl url, string title, UIDragPreviewTarget target);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITargetedDragPreview GetRetargetedPreview (UIDragPreviewTarget newTarget);</span>
}
</pre>
</div> <!-- end type UITargetedDragPreview -->
<div> <!-- start type UITextDragDelegate -->
<h3>New Type UIKit.UITextDragDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class UITextDragDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUITextDragDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextDragDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextDragDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextDragDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DragSessionDidEnd (IUITextDraggable textDraggableView, IUIDragSession session, UIDropOperation operation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DragSessionWillBegin (IUITextDraggable textDraggableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIDragItem[] GetItemsForDrag (IUITextDraggable textDraggableView, IUITextDragRequest dragRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITargetedDragPreview GetPreviewForLiftingItem (IUITextDraggable textDraggableView, UIDragItem item, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillAnimateLift (IUITextDraggable textDraggableView, IUIDragAnimating animator, IUIDragSession session);</span>
}
</pre>
</div> <!-- end type UITextDragDelegate -->
<div> <!-- start type UITextDragDelegate_Extensions -->
<h3>New Type UIKit.UITextDragDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UITextDragDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DragSessionDidEnd (IUITextDragDelegate This, IUITextDraggable textDraggableView, IUIDragSession session, UIDropOperation operation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DragSessionWillBegin (IUITextDragDelegate This, IUITextDraggable textDraggableView, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIDragItem[] GetItemsForDrag (IUITextDragDelegate This, IUITextDraggable textDraggableView, IUITextDragRequest dragRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITargetedDragPreview GetPreviewForLiftingItem (IUITextDragDelegate This, IUITextDraggable textDraggableView, UIDragItem item, IUIDragSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillAnimateLift (IUITextDragDelegate This, IUITextDraggable textDraggableView, IUIDragAnimating animator, IUIDragSession session);</span>
}
</pre>
</div> <!-- end type UITextDragDelegate_Extensions -->
<div> <!-- start type UITextDragOptions -->
<h3>New Type UIKit.UITextDragOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum UITextDragOptions {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">StripTextColorFromPreviews = 1,</span>
}
</pre>
</div> <!-- end type UITextDragOptions -->
<div> <!-- start type UITextDragPreviewRenderer -->
<h3>New Type UIKit.UITextDragPreviewRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class UITextDragPreviewRenderer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextDragPreviewRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextDragPreviewRenderer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITextDragPreviewRenderer (NSLayoutManager layoutManager, Foundation.NSRange range);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITextDragPreviewRenderer (NSLayoutManager layoutManager, Foundation.NSRange range, bool unifyRects);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect BodyRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect FirstLineRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect LastLineRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLayoutManager LayoutManager { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Adjust (CoreGraphics.CGRect firstLineRect, CoreGraphics.CGRect bodyRect, CoreGraphics.CGRect lastLineRect, CoreGraphics.CGPoint origin);</span>
}
</pre>
</div> <!-- end type UITextDragPreviewRenderer -->
<div> <!-- start type UITextDropAction -->
<h3>New Type UIKit.UITextDropAction</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextDropAction {
	<span class='added added-field ' data-is-non-breaking="">Insert = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ReplaceAll = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ReplaceSelection = 1,</span>
}
</pre>
</div> <!-- end type UITextDropAction -->
<div> <!-- start type UITextDropDelegate -->
<h3>New Type UIKit.UITextDropDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class UITextDropDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUITextDropDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextDropDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextDropDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextDropDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidEnd (IUITextDroppable textDroppableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidEnter (IUITextDroppable textDroppableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidExit (IUITextDroppable textDroppableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DropSessionDidUpdate (IUITextDroppable textDroppableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITargetedDragPreview GetPreviewForDroppingAllItems (IUITextDroppable textDroppableView, UITargetedDragPreview defaultPreview);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITextDropProposal GetProposalForDrop (IUITextDroppable textDroppableView, IUITextDropRequest drop);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITextDropEditability WillBecomeEditable (IUITextDroppable textDroppableView, IUITextDropRequest drop);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillPerformDrop (IUITextDroppable textDroppableView, IUITextDropRequest drop);</span>
}
</pre>
</div> <!-- end type UITextDropDelegate -->
<div> <!-- start type UITextDropDelegate_Extensions -->
<h3>New Type UIKit.UITextDropDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UITextDropDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidEnd (IUITextDropDelegate This, IUITextDroppable textDroppableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidEnter (IUITextDropDelegate This, IUITextDroppable textDroppableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidExit (IUITextDropDelegate This, IUITextDroppable textDroppableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DropSessionDidUpdate (IUITextDropDelegate This, IUITextDroppable textDroppableView, IUIDropSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITargetedDragPreview GetPreviewForDroppingAllItems (IUITextDropDelegate This, IUITextDroppable textDroppableView, UITargetedDragPreview defaultPreview);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextDropProposal GetProposalForDrop (IUITextDropDelegate This, IUITextDroppable textDroppableView, IUITextDropRequest drop);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextDropEditability WillBecomeEditable (IUITextDropDelegate This, IUITextDroppable textDroppableView, IUITextDropRequest drop);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillPerformDrop (IUITextDropDelegate This, IUITextDroppable textDroppableView, IUITextDropRequest drop);</span>
}
</pre>
</div> <!-- end type UITextDropDelegate_Extensions -->
<div> <!-- start type UITextDropEditability -->
<h3>New Type UIKit.UITextDropEditability</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextDropEditability {
	<span class='added added-field ' data-is-non-breaking="">No = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Temporary = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextDropEditability -->
<div> <!-- start type UITextDropPerformer -->
<h3>New Type UIKit.UITextDropPerformer</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextDropPerformer {
	<span class='added added-field ' data-is-non-breaking="">Delegate = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">View = 0,</span>
}
</pre>
</div> <!-- end type UITextDropPerformer -->
<div> <!-- start type UITextDropProgressMode -->
<h3>New Type UIKit.UITextDropProgressMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextDropProgressMode {
	<span class='added added-field ' data-is-non-breaking="">Custom = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">System = 0,</span>
}
</pre>
</div> <!-- end type UITextDropProgressMode -->
<div> <!-- start type UITextDropProposal -->
<h3>New Type UIKit.UITextDropProposal</h3>
<pre class='added' data-is-non-breaking="">
public class UITextDropProposal : UIKit.UIDropProposal, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextDropProposal (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextDropProposal (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UITextDropProposal (UIDropOperation operation);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextDropAction DropAction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextDropPerformer DropPerformer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextDropProgressMode DropProgressMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UseFastSameViewOperations { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type UITextDropProposal -->
<div> <!-- start type UITextPasteDelegate -->
<h3>New Type UIKit.UITextPasteDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class UITextPasteDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUITextPasteDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextPasteDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextPasteDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UITextPasteDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString CombineItemAttributedStrings (IUITextPasteConfigurationSupporting textPasteConfigurationSupporting, Foundation.NSAttributedString[] itemStrings, UITextRange textRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UITextRange PerformPaste (IUITextPasteConfigurationSupporting textPasteConfigurationSupporting, Foundation.NSAttributedString attributedString, UITextRange textRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAnimatePaste (IUITextPasteConfigurationSupporting textPasteConfigurationSupporting, Foundation.NSAttributedString attributedString, UITextRange textRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TransformPasteItem (IUITextPasteConfigurationSupporting textPasteConfigurationSupporting, IUITextPasteItem item);</span>
}
</pre>
</div> <!-- end type UITextPasteDelegate -->
<div> <!-- start type UITextPasteDelegate_Extensions -->
<h3>New Type UIKit.UITextPasteDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UITextPasteDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSAttributedString CombineItemAttributedStrings (IUITextPasteDelegate This, IUITextPasteConfigurationSupporting textPasteConfigurationSupporting, Foundation.NSAttributedString[] itemStrings, UITextRange textRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextRange PerformPaste (IUITextPasteDelegate This, IUITextPasteConfigurationSupporting textPasteConfigurationSupporting, Foundation.NSAttributedString attributedString, UITextRange textRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldAnimatePaste (IUITextPasteDelegate This, IUITextPasteConfigurationSupporting textPasteConfigurationSupporting, Foundation.NSAttributedString attributedString, UITextRange textRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void TransformPasteItem (IUITextPasteDelegate This, IUITextPasteConfigurationSupporting textPasteConfigurationSupporting, IUITextPasteItem item);</span>
}
</pre>
</div> <!-- end type UITextPasteDelegate_Extensions -->
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
<!-- start namespace UserNotifications --> <div> 
<h2>Namespace UserNotifications</h2>
<!-- start type UNNotificationCategory --> <div>
<h3>Type Changed: UserNotifications.UNNotificationCategory</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string HiddenPreviewsBodyPlaceholder { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UNNotificationCategory FromIdentifier (string identifier, UNNotificationAction[] actions, string[] intentIdentifiers, string hiddenPreviewsBodyPlaceholder, UNNotificationCategoryOptions options);</span>
</pre>
</div>

</div> <!-- end type UNNotificationCategory -->
<!-- start type UNNotificationCategoryOptions --> <div>
<h3>Type Changed: UserNotifications.UNNotificationCategoryOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HiddenPreviewsShowSubtitle = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HiddenPreviewsShowTitle = 4,</span>
</pre>
</div>

</div> <!-- end type UNNotificationCategoryOptions -->
<!-- start type UNNotificationSettings --> <div>
<h3>Type Changed: UserNotifications.UNNotificationSettings</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UNShowPreviewsSetting ShowPreviewsSetting { get; }</span>
</pre>
</div>

</div> <!-- end type UNNotificationSettings -->
<div> <!-- start type UNShowPreviewsSetting -->
<h3>New Type UserNotifications.UNShowPreviewsSetting</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UNShowPreviewsSetting {
	<span class='added added-field ' data-is-non-breaking="">Always = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Never = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WhenAuthenticated = 1,</span>
}
</pre>
</div> <!-- end type UNShowPreviewsSetting -->

</div> <!-- end namespace UserNotifications -->
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
	<span class='added added-method ' data-is-non-breaking="">public virtual void TakeSnapshot (WKSnapshotConfiguration snapshotConfiguration, System.Action&lt;UIKit.UIImage,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;UIKit.UIImage&gt; TakeSnapshotAsync (WKSnapshotConfiguration snapshotConfiguration);</span>
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
<!-- start namespace ARKit --> <div> 
<h2>New Namespace ARKit</h2>

<div> <!-- start type ARAnchor -->
<h3>New Type ARKit.ARAnchor</h3>
<pre class='added' data-is-non-breaking="">
public class ARAnchor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARAnchor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ARAnchor (OpenTK.Matrix4 transform);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARAnchor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix4 Transform { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type ARAnchor -->
<div> <!-- start type ARCamera -->
<h3>New Type ARKit.ARCamera</h3>
<pre class='added' data-is-non-breaking="">
public class ARCamera : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARCamera (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARCamera (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 EulerAngles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize ImageResolution { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 Intrinsics { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix4 ProjectionMatrix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARTrackingState TrackingState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARTrackingStateReason TrackingStateReason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix4 Transform { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetProjectPoint (OpenTK.Vector3 point, UIKit.UIInterfaceOrientation orientation, CoreGraphics.CGSize viewportSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Matrix4 GetProjectionMatrix (UIKit.UIInterfaceOrientation orientation, CoreGraphics.CGSize viewportSize, nfloat zNear, nfloat zFar);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Matrix4 GetViewMatrix (UIKit.UIInterfaceOrientation orientation);</span>
}
</pre>
</div> <!-- end type ARCamera -->
<div> <!-- start type ARConfiguration -->
<h3>New Type ARKit.ARConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class ARConfiguration : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsSupported { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LightEstimationEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ProvidesAudioData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARWorldAlignment WorldAlignment { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type ARConfiguration -->
<div> <!-- start type ARErrorCode -->
<h3>New Type ARKit.ARErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ARErrorCode {
	<span class='added added-field ' data-is-non-breaking="">CameraUnauthorized = 103,</span>
	<span class='added added-field ' data-is-non-breaking="">SensorFailed = 102,</span>
	<span class='added added-field ' data-is-non-breaking="">SensorUnavailable = 101,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedConfiguration = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">WorldTrackingFailed = 200,</span>
}
</pre>
</div> <!-- end type ARErrorCode -->
<div> <!-- start type ARErrorCodeExtensions -->
<h3>New Type ARKit.ARErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class ARErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (ARErrorCode self);</span>
}
</pre>
</div> <!-- end type ARErrorCodeExtensions -->
<div> <!-- start type ARFrame -->
<h3>New Type ARKit.ARFrame</h3>
<pre class='added' data-is-non-breaking="">
public class ARFrame : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARFrame (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARFrame (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual ARAnchor[] Anchors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARCamera Camera { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer CapturedImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARLightEstimate LightEstimate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARPointCloud RawFeaturePoints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Timestamp { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform DisplayTransform (UIKit.UIInterfaceOrientation orientation, CoreGraphics.CGSize viewportSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ARHitTestResult[] HitTest (CoreGraphics.CGPoint point, ARHitTestResultType types);</span>
}
</pre>
</div> <!-- end type ARFrame -->
<div> <!-- start type ARHitTestResult -->
<h3>New Type ARKit.ARHitTestResult</h3>
<pre class='added' data-is-non-breaking="">
public class ARHitTestResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARHitTestResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARHitTestResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual ARAnchor Anchor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Distance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix4 LocalTransform { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARHitTestResultType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix4 WorldTransform { get; }</span>
}
</pre>
</div> <!-- end type ARHitTestResult -->
<div> <!-- start type ARHitTestResultType -->
<h3>New Type ARKit.ARHitTestResultType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum ARHitTestResultType {
	<span class='added added-field ' data-is-non-breaking="">EstimatedHorizontalPlane = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ExistingPlane = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ExistingPlaneUsingExtent = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">FeaturePoint = 1,</span>
}
</pre>
</div> <!-- end type ARHitTestResultType -->
<div> <!-- start type ARLightEstimate -->
<h3>New Type ARKit.ARLightEstimate</h3>
<pre class='added' data-is-non-breaking="">
public class ARLightEstimate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARLightEstimate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARLightEstimate (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat AmbientColorTemperature { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat AmbientIntensity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type ARLightEstimate -->
<div> <!-- start type AROrientationTrackingConfiguration -->
<h3>New Type ARKit.AROrientationTrackingConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class AROrientationTrackingConfiguration : ARKit.ARConfiguration, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AROrientationTrackingConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AROrientationTrackingConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AROrientationTrackingConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type AROrientationTrackingConfiguration -->
<div> <!-- start type ARPlaneAnchor -->
<h3>New Type ARKit.ARPlaneAnchor</h3>
<pre class='added' data-is-non-breaking="">
public class ARPlaneAnchor : ARKit.ARAnchor, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARPlaneAnchor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARPlaneAnchor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual ARPlaneAnchorAlignment Alignment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 Center { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 Extent { get; }</span>
}
</pre>
</div> <!-- end type ARPlaneAnchor -->
<div> <!-- start type ARPlaneAnchorAlignment -->
<h3>New Type ARKit.ARPlaneAnchorAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ARPlaneAnchorAlignment {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 0,</span>
}
</pre>
</div> <!-- end type ARPlaneAnchorAlignment -->
<div> <!-- start type ARPlaneDetection -->
<h3>New Type ARKit.ARPlaneDetection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum ARPlaneDetection {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type ARPlaneDetection -->
<div> <!-- start type ARPointCloud -->
<h3>New Type ARKit.ARPointCloud</h3>
<pre class='added' data-is-non-breaking="">
public class ARPointCloud : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARPointCloud (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARPointCloud (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.Vector3[] Points { get; }</span>
}
</pre>
</div> <!-- end type ARPointCloud -->
<div> <!-- start type ARSCNDebugOptions -->
<h3>New Type ARKit.ARSCNDebugOptions</h3>
<pre class='added' data-is-non-breaking="">
public static class ARSCNDebugOptions {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static SceneKit.SCNDebugOptions ShowFeaturePoints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SceneKit.SCNDebugOptions ShowWorldOrigin { get; }</span>
}
</pre>
</div> <!-- end type ARSCNDebugOptions -->
<div> <!-- start type ARSCNView -->
<h3>New Type ARKit.ARSCNView</h3>
<pre class='added' data-is-non-breaking="">
public class ARSCNView : SceneKit.SCNView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, SceneKit.ISCNSceneRenderer, SceneKit.ISCNTechniqueSupport, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARSCNView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ARSCNView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSCNView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSCNView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static ARSCNView.ARSCNViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticallyUpdatesLighting { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IARSCNViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SceneKit.SCNScene Scene { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARSession Session { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNView.ARSCNViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ARAnchor GetAnchor (SceneKit.SCNNode node);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNView.ARSCNViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNView.ARSCNViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNView.ARSCNViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNView.ARSCNViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNView.ARSCNViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SceneKit.SCNNode GetNode (ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ARHitTestResult[] HitTest (CoreGraphics.CGPoint point, ARHitTestResultType types);</span>

	// inner types
	public class ARSCNViewAppearance : SceneKit.SCNView+SCNViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected ARSCNView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type ARSCNView -->
<div> <!-- start type ARSCNViewDelegate -->
<h3>New Type ARKit.ARSCNViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class ARSCNViewDelegate : Foundation.NSObject, IARSCNViewDelegate, IARSessionObserver, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, SceneKit.ISCNSceneRendererDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARSCNViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSCNViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSCNViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CameraDidChangeTrackingState (ARSession session, ARCamera camera);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddNode (SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidApplyAnimations (SceneKit.ISCNSceneRenderer renderer, double timeInSeconds);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFail (ARSession session, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOutputAudioSampleBuffer (ARSession session, CoreMedia.CMSampleBuffer audioSampleBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveNode (SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRenderScene (SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNScene scene, double timeInSeconds);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidSimulatePhysics (SceneKit.ISCNSceneRenderer renderer, double timeInSeconds);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNode (SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SceneKit.SCNNode GetNode (SceneKit.ISCNSceneRenderer renderer, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionInterruptionEnded (ARSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionWasInterrupted (ARSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SceneKit.ISCNSceneRenderer renderer, double timeInSeconds);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillRenderScene (SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNScene scene, double timeInSeconds);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillUpdateNode (SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNNode node, ARAnchor anchor);</span>
}
</pre>
</div> <!-- end type ARSCNViewDelegate -->
<div> <!-- start type ARSCNViewDelegate_Extensions -->
<h3>New Type ARKit.ARSCNViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class ARSCNViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddNode (IARSCNViewDelegate This, SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveNode (IARSCNViewDelegate This, SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNode (IARSCNViewDelegate This, SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SceneKit.SCNNode GetNode (IARSCNViewDelegate This, SceneKit.ISCNSceneRenderer renderer, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillUpdateNode (IARSCNViewDelegate This, SceneKit.ISCNSceneRenderer renderer, SceneKit.SCNNode node, ARAnchor anchor);</span>
}
</pre>
</div> <!-- end type ARSCNViewDelegate_Extensions -->
<div> <!-- start type ARSKView -->
<h3>New Type ARKit.ARSKView</h3>
<pre class='added' data-is-non-breaking="">
public class ARSKView : SpriteKit.SKView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARSKView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ARSKView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSKView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSKView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static ARSKView.ARSKViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IARSKViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARSession Session { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static ARSKView.ARSKViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ARAnchor GetAnchor (SpriteKit.SKNode node);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSKView.ARSKViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSKView.ARSKViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSKView.ARSKViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSKView.ARSKViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSKView.ARSKViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SpriteKit.SKNode GetNode (ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ARHitTestResult[] HitTest (CoreGraphics.CGPoint point, ARHitTestResultType types);</span>

	// inner types
	public class ARSKViewAppearance : SpriteKit.SKView+SKViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected ARSKView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type ARSKView -->
<div> <!-- start type ARSKViewDelegate -->
<h3>New Type ARKit.ARSKViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class ARSKViewDelegate : Foundation.NSObject, IARSKViewDelegate, IARSessionObserver, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, SpriteKit.ISKViewDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARSKViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSKViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSKViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CameraDidChangeTrackingState (ARSession session, ARCamera camera);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddNode (ARSKView view, SpriteKit.SKNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFail (ARSession session, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOutputAudioSampleBuffer (ARSession session, CoreMedia.CMSampleBuffer audioSampleBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveNode (ARSKView view, SpriteKit.SKNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNode (ARSKView view, SpriteKit.SKNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SpriteKit.SKNode GetNode (ARSKView view, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionInterruptionEnded (ARSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionWasInterrupted (ARSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldRender (SpriteKit.SKView view, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillUpdateNode (ARSKView view, SpriteKit.SKNode node, ARAnchor anchor);</span>
}
</pre>
</div> <!-- end type ARSKViewDelegate -->
<div> <!-- start type ARSKViewDelegate_Extensions -->
<h3>New Type ARKit.ARSKViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class ARSKViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddNode (IARSKViewDelegate This, ARSKView view, SpriteKit.SKNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveNode (IARSKViewDelegate This, ARSKView view, SpriteKit.SKNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNode (IARSKViewDelegate This, ARSKView view, SpriteKit.SKNode node, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SpriteKit.SKNode GetNode (IARSKViewDelegate This, ARSKView view, ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillUpdateNode (IARSKViewDelegate This, ARSKView view, SpriteKit.SKNode node, ARAnchor anchor);</span>
}
</pre>
</div> <!-- end type ARSKViewDelegate_Extensions -->
<div> <!-- start type ARSession -->
<h3>New Type ARKit.ARSession</h3>
<pre class='added' data-is-non-breaking="">
public class ARSession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARSession ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSession (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARConfiguration Configuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARFrame CurrentFrame { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IARSessionDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreFoundation.DispatchQueue DelegateQueue { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnchor (ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Pause ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnchor (ARAnchor anchor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Run (ARConfiguration configuration, ARSessionRunOptions options);</span>
}
</pre>
</div> <!-- end type ARSession -->
<div> <!-- start type ARSessionDelegate -->
<h3>New Type ARKit.ARSessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class ARSessionDelegate : Foundation.NSObject, IARSessionDelegate, IARSessionObserver, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARSessionDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSessionDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSessionDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CameraDidChangeTrackingState (ARSession session, ARCamera camera);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddAnchors (ARSession session, ARAnchor[] anchors);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFail (ARSession session, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOutputAudioSampleBuffer (ARSession session, CoreMedia.CMSampleBuffer audioSampleBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveAnchors (ARSession session, ARAnchor[] anchors);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateAnchors (ARSession session, ARAnchor[] anchors);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateFrame (ARSession session, ARFrame frame);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionInterruptionEnded (ARSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SessionWasInterrupted (ARSession session);</span>
}
</pre>
</div> <!-- end type ARSessionDelegate -->
<div> <!-- start type ARSessionDelegate_Extensions -->
<h3>New Type ARKit.ARSessionDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class ARSessionDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddAnchors (IARSessionDelegate This, ARSession session, ARAnchor[] anchors);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveAnchors (IARSessionDelegate This, ARSession session, ARAnchor[] anchors);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateAnchors (IARSessionDelegate This, ARSession session, ARAnchor[] anchors);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateFrame (IARSessionDelegate This, ARSession session, ARFrame frame);</span>
}
</pre>
</div> <!-- end type ARSessionDelegate_Extensions -->
<div> <!-- start type ARSessionObserver_Extensions -->
<h3>New Type ARKit.ARSessionObserver_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class ARSessionObserver_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CameraDidChangeTrackingState (IARSessionObserver This, ARSession session, ARCamera camera);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidFail (IARSessionObserver This, ARSession session, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidOutputAudioSampleBuffer (IARSessionObserver This, ARSession session, CoreMedia.CMSampleBuffer audioSampleBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionInterruptionEnded (IARSessionObserver This, ARSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SessionWasInterrupted (IARSessionObserver This, ARSession session);</span>
}
</pre>
</div> <!-- end type ARSessionObserver_Extensions -->
<div> <!-- start type ARSessionRunOptions -->
<h3>New Type ARKit.ARSessionRunOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum ARSessionRunOptions {
	<span class='added added-field ' data-is-non-breaking="">RemoveExistingAnchors = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ResetTracking = 1,</span>
}
</pre>
</div> <!-- end type ARSessionRunOptions -->
<div> <!-- start type ARTrackingState -->
<h3>New Type ARKit.ARTrackingState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ARTrackingState {
	<span class='added added-field ' data-is-non-breaking="">Limited = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAvailable = 0,</span>
}
</pre>
</div> <!-- end type ARTrackingState -->
<div> <!-- start type ARTrackingStateReason -->
<h3>New Type ARKit.ARTrackingStateReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ARTrackingStateReason {
	<span class='added added-field ' data-is-non-breaking="">ExcessiveMotion = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Initializing = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientFeatures = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type ARTrackingStateReason -->
<div> <!-- start type ARWorldAlignment -->
<h3>New Type ARKit.ARWorldAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ARWorldAlignment {
	<span class='added added-field ' data-is-non-breaking="">Camera = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Gravity = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">GravityAndHeading = 1,</span>
}
</pre>
</div> <!-- end type ARWorldAlignment -->
<div> <!-- start type ARWorldTrackingConfiguration -->
<h3>New Type ARKit.ARWorldTrackingConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class ARWorldTrackingConfiguration : ARKit.ARConfiguration, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARWorldTrackingConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARWorldTrackingConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARWorldTrackingConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARPlaneDetection PlaneDetection { get; set; }</span>
}
</pre>
</div> <!-- end type ARWorldTrackingConfiguration -->
<div> <!-- start type IARSCNViewDelegate -->
<h3>New Type ARKit.IARSCNViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IARSCNViewDelegate : IARSessionObserver, ObjCRuntime.INativeObject, SceneKit.ISCNSceneRendererDelegate, System.IDisposable {
}
</pre>
</div> <!-- end type IARSCNViewDelegate -->
<div> <!-- start type IARSKViewDelegate -->
<h3>New Type ARKit.IARSKViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IARSKViewDelegate : IARSessionObserver, ObjCRuntime.INativeObject, SpriteKit.ISKViewDelegate, System.IDisposable {
}
</pre>
</div> <!-- end type IARSKViewDelegate -->
<div> <!-- start type IARSessionDelegate -->
<h3>New Type ARKit.IARSessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IARSessionDelegate : IARSessionObserver, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IARSessionDelegate -->
<div> <!-- start type IARSessionObserver -->
<h3>New Type ARKit.IARSessionObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IARSessionObserver : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IARSessionObserver -->
</div> <!-- end namespace ARKit -->

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
<div> <!-- start type MLDictionaryConstraint -->
<h3>New Type CoreML.MLDictionaryConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType KeyType { get; }</span>
}
</pre>
</div> <!-- end type MLDictionaryConstraint -->
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
	<span class='added added-property ' data-is-non-breaking="">public virtual MLDictionaryConstraint DictionaryConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLImageConstraint ImageConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayConstraint MultiArrayConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Optional { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
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
<div> <!-- start type MLImageConstraint -->
<h3>New Type CoreML.MLImageConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLImageConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLImageConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLImageConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelFormatType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsHigh { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsWide { get; }</span>
}
</pre>
</div> <!-- end type MLImageConstraint -->
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
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrl CompileModel (Foundation.NSUrl modelUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLModel FromUrl (Foundation.NSUrl url, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, MLPredictionOptions options, Foundation.NSError error);</span>
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
	<span class='added added-field ' data-is-non-breaking="">FeatureType = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Generic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">IO = 3,</span>
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
	<span class='added added-property ' data-is-non-breaking="">public string CreatorDefined { get; }</span>
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
<div> <!-- start type MLMultiArrayConstraint -->
<h3>New Type CoreML.MLMultiArrayConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArrayConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArrayConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArrayConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Shape { get; }</span>
}
</pre>
</div> <!-- end type MLMultiArrayConstraint -->
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
<div> <!-- start type MLPredictionOptions -->
<h3>New Type CoreML.MLPredictionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class MLPredictionOptions : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLPredictionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLPredictionOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLPredictionOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesCpuOnly { get; set; }</span>
}
</pre>
</div> <!-- end type MLPredictionOptions -->
</div> <!-- end namespace CoreML -->

<!-- start namespace CoreNFC --> <div> 
<h2>New Namespace CoreNFC</h2>

<div> <!-- start type INFCIso15693Tag -->
<h3>New Type CoreNFC.INFCIso15693Tag</h3>
<pre class='added' data-is-non-breaking="">
public interface INFCIso15693Tag : INFCTag, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint IcManufacturerCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData IcSerialNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Identifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadMultipleBlocks (NFCIso15693ReadMultipleBlocksConfiguration readConfiguration, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendCustomCommand (NFCIso15693CustomCommandConfiguration commandConfiguration, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);</span>
}
</pre>
</div> <!-- end type INFCIso15693Tag -->
<div> <!-- start type INFCNdefReaderSessionDelegate -->
<h3>New Type CoreNFC.INFCNdefReaderSessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INFCNdefReaderSessionDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidDetect (NFCNdefReaderSession session, NFCNdefMessage[] messages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidInvalidate (NFCNdefReaderSession session, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type INFCNdefReaderSessionDelegate -->
<div> <!-- start type INFCReaderSessionContract -->
<h3>New Type CoreNFC.INFCReaderSessionContract</h3>
<pre class='added' data-is-non-breaking="">
public interface INFCReaderSessionContract : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AlertMessage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Ready { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginSession ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InvalidateSession ();</span>
}
</pre>
</div> <!-- end type INFCReaderSessionContract -->
<div> <!-- start type INFCReaderSessionDelegate -->
<h3>New Type CoreNFC.INFCReaderSessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INFCReaderSessionDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidBecomeActive (NFCReaderSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidDetectTags (NFCReaderSession session, INFCTag[] tags);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidInvalidate (NFCReaderSession session, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type INFCReaderSessionDelegate -->
<div> <!-- start type INFCTag -->
<h3>New Type CoreNFC.INFCTag</h3>
<pre class='added' data-is-non-breaking="">
public interface INFCTag : Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Available { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NFCReaderSession Session { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NFCTagType Type { get; }</span>
}
</pre>
</div> <!-- end type INFCTag -->
<div> <!-- start type NFCIso15693CustomCommandConfiguration -->
<h3>New Type CoreNFC.NFCIso15693CustomCommandConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class NFCIso15693CustomCommandConfiguration : CoreNFC.NFCTagCommandConfiguration, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NFCIso15693CustomCommandConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCIso15693CustomCommandConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCIso15693CustomCommandConfiguration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NFCIso15693CustomCommandConfiguration (uint manufacturerCode, uint customCommandCode, Foundation.NSData requestParameters);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NFCIso15693CustomCommandConfiguration (uint manufacturerCode, uint customCommandCode, Foundation.NSData requestParameters, uint maximumRetries, double retryInterval);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint CustomCommandCode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ManufacturerCode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData RequestParameters { get; set; }</span>
}
</pre>
</div> <!-- end type NFCIso15693CustomCommandConfiguration -->
<div> <!-- start type NFCIso15693ReadMultipleBlocksConfiguration -->
<h3>New Type CoreNFC.NFCIso15693ReadMultipleBlocksConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class NFCIso15693ReadMultipleBlocksConfiguration : CoreNFC.NFCTagCommandConfiguration, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NFCIso15693ReadMultipleBlocksConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCIso15693ReadMultipleBlocksConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCIso15693ReadMultipleBlocksConfiguration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NFCIso15693ReadMultipleBlocksConfiguration (Foundation.NSRange range, uint chunkSize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NFCIso15693ReadMultipleBlocksConfiguration (Foundation.NSRange range, uint chunkSize, uint maximumRetries, double retryInterval);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ChunkSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange Range { get; set; }</span>
}
</pre>
</div> <!-- end type NFCIso15693ReadMultipleBlocksConfiguration -->
<div> <!-- start type NFCIso15693ReaderSession -->
<h3>New Type CoreNFC.NFCIso15693ReaderSession</h3>
<pre class='added' data-is-non-breaking="">
public class NFCIso15693ReaderSession : CoreNFC.NFCReaderSession, INFCReaderSessionContract, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCIso15693ReaderSession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCIso15693ReaderSession (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NFCIso15693ReaderSession (INFCReaderSessionDelegate delegate, CoreFoundation.DispatchQueue queue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool ReadingAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TagResponseErrorKey { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void RestartPolling ();</span>
}
</pre>
</div> <!-- end type NFCIso15693ReaderSession -->
<div> <!-- start type NFCNdefMessage -->
<h3>New Type CoreNFC.NFCNdefMessage</h3>
<pre class='added' data-is-non-breaking="">
public class NFCNdefMessage : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NFCNdefMessage (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefMessage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefMessage (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NFCNdefPayload[] Records { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NFCNdefMessage -->
<div> <!-- start type NFCNdefPayload -->
<h3>New Type CoreNFC.NFCNdefPayload</h3>
<pre class='added' data-is-non-breaking="">
public class NFCNdefPayload : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NFCNdefPayload (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefPayload (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefPayload (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Identifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Payload { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Type { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NFCTypeNameFormat TypeNameFormat { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NFCNdefPayload -->
<div> <!-- start type NFCNdefReaderSession -->
<h3>New Type CoreNFC.NFCNdefReaderSession</h3>
<pre class='added' data-is-non-breaking="">
public class NFCNdefReaderSession : CoreNFC.NFCReaderSession, INFCReaderSessionContract, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefReaderSession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefReaderSession (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NFCNdefReaderSession (INFCNdefReaderSessionDelegate delegate, CoreFoundation.DispatchQueue queue, bool invalidateAfterFirstRead);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool ReadingAvailable { get; }</span>
}
</pre>
</div> <!-- end type NFCNdefReaderSession -->
<div> <!-- start type NFCNdefReaderSessionDelegate -->
<h3>New Type CoreNFC.NFCNdefReaderSessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NFCNdefReaderSessionDelegate : Foundation.NSObject, INFCNdefReaderSessionDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefReaderSessionDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefReaderSessionDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCNdefReaderSessionDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidDetect (NFCNdefReaderSession session, NFCNdefMessage[] messages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidInvalidate (NFCNdefReaderSession session, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type NFCNdefReaderSessionDelegate -->
<div> <!-- start type NFCReaderError -->
<h3>New Type CoreNFC.NFCReaderError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NFCReaderError {
	<span class='added added-field ' data-is-non-breaking="">ReaderSessionInvalidationErrorFirstNDEFTagRead = 204,</span>
	<span class='added added-field ' data-is-non-breaking="">ReaderSessionInvalidationErrorSessionTerminatedUnexpectedly = 202,</span>
	<span class='added added-field ' data-is-non-breaking="">ReaderSessionInvalidationErrorSessionTimeout = 201,</span>
	<span class='added added-field ' data-is-non-breaking="">ReaderSessionInvalidationErrorSystemIsBusy = 203,</span>
	<span class='added added-field ' data-is-non-breaking="">ReaderSessionInvalidationErrorUserCanceled = 200,</span>
	<span class='added added-field ' data-is-non-breaking="">ReaderTransceiveErrorRetryExceeded = 101,</span>
	<span class='added added-field ' data-is-non-breaking="">ReaderTransceiveErrorTagConnectionLost = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">ReaderTransceiveErrorTagResponseError = 102,</span>
	<span class='added added-field ' data-is-non-breaking="">SecurityViolation = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TagCommandConfigurationErrorInvalidParameters = 300,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedFeature = 1,</span>
}
</pre>
</div> <!-- end type NFCReaderError -->
<div> <!-- start type NFCReaderErrorExtensions -->
<h3>New Type CoreNFC.NFCReaderErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NFCReaderErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (NFCReaderError self);</span>
}
</pre>
</div> <!-- end type NFCReaderErrorExtensions -->
<div> <!-- start type NFCReaderSession -->
<h3>New Type CoreNFC.NFCReaderSession</h3>
<pre class='added' data-is-non-breaking="">
public class NFCReaderSession : Foundation.NSObject, INFCReaderSessionContract, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCReaderSession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCReaderSession (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AlertMessage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INFCReaderSessionDelegate Delegate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Ready { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreFoundation.DispatchQueue SessionQueue { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginSession ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InvalidateSession ();</span>
}
</pre>
</div> <!-- end type NFCReaderSession -->
<div> <!-- start type NFCReaderSessionDelegate -->
<h3>New Type CoreNFC.NFCReaderSessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NFCReaderSessionDelegate : Foundation.NSObject, INFCReaderSessionDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCReaderSessionDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCReaderSessionDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCReaderSessionDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidBecomeActive (NFCReaderSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidDetectTags (NFCReaderSession session, INFCTag[] tags);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidInvalidate (NFCReaderSession session, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type NFCReaderSessionDelegate -->
<div> <!-- start type NFCTagCommandConfiguration -->
<h3>New Type CoreNFC.NFCTagCommandConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class NFCTagCommandConfiguration : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NFCTagCommandConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCTagCommandConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NFCTagCommandConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumRetries { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double RetryInterval { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NFCTagCommandConfiguration -->
<div> <!-- start type NFCTagType -->
<h3>New Type CoreNFC.NFCTagType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NFCTagType {
	<span class='added added-field ' data-is-non-breaking="">Iso15693 = 1,</span>
}
</pre>
</div> <!-- end type NFCTagType -->
<div> <!-- start type NFCTypeNameFormat -->
<h3>New Type CoreNFC.NFCTypeNameFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NFCTypeNameFormat {
	<span class='added added-field ' data-is-non-breaking="">AbsoluteUri = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Empty = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Media = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NFCExternal = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">NFCWellKnown = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unchanged = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 5,</span>
}
</pre>
</div> <!-- end type NFCTypeNameFormat -->
</div> <!-- end namespace CoreNFC -->

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

<!-- start namespace FileProvider --> <div> 
<h2>New Namespace FileProvider</h2>

<div> <!-- start type INSFileProviderChangeObserver -->
<h3>New Type FileProvider.INSFileProviderChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface INSFileProviderChangeObserver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidDeleteItems (string[] deletedItemIdentifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateItems (INSFileProviderItem[] updatedItems);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishEnumerating (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishEnumeratingChanges (Foundation.NSData anchor, bool moreComing);</span>
}
</pre>
</div> <!-- end type INSFileProviderChangeObserver -->
<div> <!-- start type INSFileProviderEnumerationObserver -->
<h3>New Type FileProvider.INSFileProviderEnumerationObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface INSFileProviderEnumerationObserver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEnumerateItems (INSFileProviderItem[] updatedItems);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishEnumerating (Foundation.NSData upToPage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishEnumerating (Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type INSFileProviderEnumerationObserver -->
<div> <!-- start type INSFileProviderEnumerator -->
<h3>New Type FileProvider.INSFileProviderEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public interface INSFileProviderEnumerator : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateItems (INSFileProviderEnumerationObserver observer, Foundation.NSData startPage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invalidate ();</span>
}
</pre>
</div> <!-- end type INSFileProviderEnumerator -->
<div> <!-- start type INSFileProviderItem -->
<h3>New Type FileProvider.INSFileProviderItem</h3>
<pre class='added' data-is-non-breaking="">
public interface INSFileProviderItem : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Filename { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ParentIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TypeIdentifier { get; }</span>
}
</pre>
</div> <!-- end type INSFileProviderItem -->
<div> <!-- start type NSFileProviderDomain -->
<h3>New Type FileProvider.NSFileProviderDomain</h3>
<pre class='added' data-is-non-breaking="">
public class NSFileProviderDomain : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderDomain (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderDomain (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderDomain (string identifier, string displayName, string pathRelativeToDocumentStorage);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PathRelativeToDocumentStorage { get; }</span>
}
</pre>
</div> <!-- end type NSFileProviderDomain -->
<div> <!-- start type NSFileProviderEnumerator_Extensions -->
<h3>New Type FileProvider.NSFileProviderEnumerator_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSFileProviderEnumerator_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CurrentSyncAnchor (INSFileProviderEnumerator This, System.Action&lt;Foundation.NSData&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void EnumerateChanges (INSFileProviderEnumerator This, INSFileProviderChangeObserver observer, Foundation.NSData syncAnchor);</span>
}
</pre>
</div> <!-- end type NSFileProviderEnumerator_Extensions -->
<div> <!-- start type NSFileProviderError -->
<h3>New Type FileProvider.NSFileProviderError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFileProviderError {
	<span class='added added-field ' data-is-non-breaking="">FilenameCollision = -1001,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientQuota = -1003,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSuchItem = -1005,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAuthenticated = -1000,</span>
	<span class='added added-field ' data-is-non-breaking="">PageExpired = -1002,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerUnreachable = -1004,</span>
	<span class='added added-field ' data-is-non-breaking="">SyncAnchorExpired = -1002,</span>
}
</pre>
</div> <!-- end type NSFileProviderError -->
<div> <!-- start type NSFileProviderErrorExtensions -->
<h3>New Type FileProvider.NSFileProviderErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSFileProviderErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (NSFileProviderError self);</span>
}
</pre>
</div> <!-- end type NSFileProviderErrorExtensions -->
<div> <!-- start type NSFileProviderItemCapabilities -->
<h3>New Type FileProvider.NSFileProviderItemCapabilities</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFileProviderItemCapabilities {
	<span class='added added-field ' data-is-non-breaking="">AddingSubItems = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">All = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentEnumerating = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Deleting = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Reading = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Renaming = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Reparenting = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Trashing = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Writing = 2,</span>
}
</pre>
</div> <!-- end type NSFileProviderItemCapabilities -->
<div> <!-- start type NSFileProviderItemIdentifier -->
<h3>New Type FileProvider.NSFileProviderItemIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFileProviderItemIdentifier {
	<span class='added added-field ' data-is-non-breaking="">RootContainer = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WorkingSetContainer = 1,</span>
}
</pre>
</div> <!-- end type NSFileProviderItemIdentifier -->
<div> <!-- start type NSFileProviderItemIdentifierExtensions -->
<h3>New Type FileProvider.NSFileProviderItemIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSFileProviderItemIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSFileProviderItemIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString[] GetConstants (NSFileProviderItemIdentifier[] self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSFileProviderItemIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSFileProviderItemIdentifierExtensions -->
<div> <!-- start type NSFileProviderItem_Extensions -->
<h3>New Type FileProvider.NSFileProviderItem_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSFileProviderItem_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFileProviderItemCapabilities GetCapabilities (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSNumber GetChildItemCount (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDate GetContentModificationDate (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDate GetCreationDate (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSNumber GetDocumentSize (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError GetDownloadingError (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSNumber GetFavoriteRank (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDate GetLastUsedDate (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPersonNameComponents GetMostRecentEditorNameComponents (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPersonNameComponents GetOwnerNameComponents (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetTagData (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError GetUploadingError (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary GetUserInfo (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetVersionIdentifier (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsDownloaded (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsDownloading (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsMostRecentVersionDownloaded (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsShared (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsSharedByCurrentUser (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsTrashed (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsUploaded (INSFileProviderItem This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsUploading (INSFileProviderItem This);</span>
}
</pre>
</div> <!-- end type NSFileProviderItem_Extensions -->
<div> <!-- start type NSFileProviderManager -->
<h3>New Type FileProvider.NSFileProviderManager</h3>
<pre class='added' data-is-non-breaking="">
public class NSFileProviderManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSFileProviderManager DefaultManager { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl DocumentStorageUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProviderIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AddDomain (NSFileProviderDomain domain, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task AddDomainAsync (NSFileProviderDomain domain);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSFileProviderManager FromDomain (NSFileProviderDomain domain);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetDomains (System.Action&lt;NSFileProviderDomain[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;NSFileProviderDomain[]&gt; GetDomainsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrl GetPlaceholderUrl (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Register (Foundation.NSUrlSessionTask task, NSFileProviderItemIdentifier identifier, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Register (Foundation.NSUrlSessionTask task, Foundation.NSString identifier, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAllDomains (System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task RemoveAllDomainsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveDomain (NSFileProviderDomain domain, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task RemoveDomainAsync (NSFileProviderDomain domain);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SignalEnumerator (NSFileProviderItemIdentifier containerItemIdentifier, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void SignalEnumerator (Foundation.NSString containerItemIdentifier, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool WritePlaceholder (Foundation.NSUrl placeholderUrl, INSFileProviderItem metadata, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type NSFileProviderManager -->
</div> <!-- end namespace FileProvider -->

<!-- start namespace FileProviderUI --> <div> 
<h2>New Namespace FileProviderUI</h2>

<div> <!-- start type FPUIActionExtensionContext -->
<h3>New Type FileProviderUI.FPUIActionExtensionContext</h3>
<pre class='added' data-is-non-breaking="">
public class FPUIActionExtensionContext : Foundation.NSExtensionContext, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected FPUIActionExtensionContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FPUIActionExtensionContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DomainIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelRequest (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CompleteRequest ();</span>
}
</pre>
</div> <!-- end type FPUIActionExtensionContext -->
<div> <!-- start type FPUIActionExtensionViewController -->
<h3>New Type FileProviderUI.FPUIActionExtensionViewController</h3>
<pre class='added' data-is-non-breaking="">
public class FPUIActionExtensionViewController : UIKit.UIViewController, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FPUIActionExtensionViewController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FPUIActionExtensionViewController (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FPUIActionExtensionViewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected FPUIActionExtensionViewController (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FPUIActionExtensionViewController (string nibName, Foundation.NSBundle bundle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual FPUIActionExtensionContext ExtensionContext { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Prepare (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Prepare (string actionIdentifier, FileProvider.NSFileProviderItemIdentifier[] itemIdentifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Prepare (string actionIdentifier, Foundation.NSString[] itemIdentifiers);</span>
}
</pre>
</div> <!-- end type FPUIActionExtensionViewController -->
<div> <!-- start type FPUIExtensionErrorCode -->
<h3>New Type FileProviderUI.FPUIExtensionErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum FPUIExtensionErrorCode {
	<span class='added added-field ' data-is-non-breaking="">Failed = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UserCancelled = 0,</span>
}
</pre>
</div> <!-- end type FPUIExtensionErrorCode -->
<div> <!-- start type FPUIExtensionErrorCodeExtensions -->
<h3>New Type FileProviderUI.FPUIExtensionErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class FPUIExtensionErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (FPUIExtensionErrorCode self);</span>
}
</pre>
</div> <!-- end type FPUIExtensionErrorCodeExtensions -->
</div> <!-- end namespace FileProviderUI -->

<!-- start namespace IdentityLookup --> <div> 
<h2>New Namespace IdentityLookup</h2>

<div> <!-- start type IILMessageFilterQueryHandling -->
<h3>New Type IdentityLookup.IILMessageFilterQueryHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IILMessageFilterQueryHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleQueryRequest (ILMessageFilterQueryRequest queryRequest, ILMessageFilterExtensionContext context, System.Action&lt;ILMessageFilterQueryResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IILMessageFilterQueryHandling -->
<div> <!-- start type ILMessageFilterAction -->
<h3>New Type IdentityLookup.ILMessageFilterAction</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ILMessageFilterAction {
	<span class='added added-field ' data-is-non-breaking="">Allow = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Filter = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type ILMessageFilterAction -->
<div> <!-- start type ILMessageFilterError -->
<h3>New Type IdentityLookup.ILMessageFilterError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ILMessageFilterError {
	<span class='added added-field ' data-is-non-breaking="">InvalidNetworkUrl = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NetworkRequestFailed = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">NetworkUrlUnauthorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">RedundantNetworkDeferral = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">System = 1,</span>
}
</pre>
</div> <!-- end type ILMessageFilterError -->
<div> <!-- start type ILMessageFilterErrorExtensions -->
<h3>New Type IdentityLookup.ILMessageFilterErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class ILMessageFilterErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (ILMessageFilterError self);</span>
}
</pre>
</div> <!-- end type ILMessageFilterErrorExtensions -->
<div> <!-- start type ILMessageFilterExtension -->
<h3>New Type IdentityLookup.ILMessageFilterExtension</h3>
<pre class='added' data-is-non-breaking="">
public class ILMessageFilterExtension : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ILMessageFilterExtension (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ILMessageFilterExtension (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type ILMessageFilterExtension -->
<div> <!-- start type ILMessageFilterExtensionContext -->
<h3>New Type IdentityLookup.ILMessageFilterExtensionContext</h3>
<pre class='added' data-is-non-breaking="">
public class ILMessageFilterExtensionContext : Foundation.NSExtensionContext, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ILMessageFilterExtensionContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ILMessageFilterExtensionContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeferQueryRequestToNetwork (System.Action&lt;ILNetworkResponse,Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;ILNetworkResponse&gt; DeferQueryRequestToNetworkAsync ();</span>
}
</pre>
</div> <!-- end type ILMessageFilterExtensionContext -->
<div> <!-- start type ILMessageFilterQueryRequest -->
<h3>New Type IdentityLookup.ILMessageFilterQueryRequest</h3>
<pre class='added' data-is-non-breaking="">
public class ILMessageFilterQueryRequest : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ILMessageFilterQueryRequest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ILMessageFilterQueryRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ILMessageFilterQueryRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string MessageBody { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Sender { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type ILMessageFilterQueryRequest -->
<div> <!-- start type ILMessageFilterQueryResponse -->
<h3>New Type IdentityLookup.ILMessageFilterQueryResponse</h3>
<pre class='added' data-is-non-breaking="">
public class ILMessageFilterQueryResponse : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ILMessageFilterQueryResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ILMessageFilterQueryResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ILMessageFilterQueryResponse (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual ILMessageFilterAction Action { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type ILMessageFilterQueryResponse -->
<div> <!-- start type ILNetworkResponse -->
<h3>New Type IdentityLookup.ILNetworkResponse</h3>
<pre class='added' data-is-non-breaking="">
public class ILNetworkResponse : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ILNetworkResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ILNetworkResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ILNetworkResponse (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSHttpUrlResponse UrlResponse { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type ILNetworkResponse -->
</div> <!-- end namespace IdentityLookup -->

<!-- start namespace PdfKit --> <div> 
<h2>New Namespace PdfKit</h2>

<div> <!-- start type ClassForAnnotationTypeDelegate -->
<h3>New Type PdfKit.ClassForAnnotationTypeDelegate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ClassForAnnotationTypeDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ClassForAnnotationTypeDelegate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string annotationType, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class Invoke (string annotationType);</span>
}
</pre>
</div> <!-- end type ClassForAnnotationTypeDelegate -->
<div> <!-- start type IPdfDocumentDelegate -->
<h3>New Type PdfKit.IPdfDocumentDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IPdfDocumentDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IPdfDocumentDelegate -->
<div> <!-- start type IPdfViewDelegate -->
<h3>New Type PdfKit.IPdfViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IPdfViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IPdfViewDelegate -->
<div> <!-- start type PdfAction -->
<h3>New Type PdfKit.PdfAction</h3>
<pre class='added' data-is-non-breaking="">
public abstract class PdfAction : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PdfAction -->
<div> <!-- start type PdfActionGoTo -->
<h3>New Type PdfKit.PdfActionGoTo</h3>
<pre class='added' data-is-non-breaking="">
public class PdfActionGoTo : PdfKit.PdfAction, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionGoTo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionGoTo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionGoTo (PdfDestination destination);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionGoTo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDestination Destination { get; set; }</span>
}
</pre>
</div> <!-- end type PdfActionGoTo -->
<div> <!-- start type PdfActionNamed -->
<h3>New Type PdfKit.PdfActionNamed</h3>
<pre class='added' data-is-non-breaking="">
public class PdfActionNamed : PdfKit.PdfAction, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionNamed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionNamed (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionNamed (PdfActionNamedName name);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionNamed (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfActionNamedName Name { get; set; }</span>
}
</pre>
</div> <!-- end type PdfActionNamed -->
<div> <!-- start type PdfActionNamedName -->
<h3>New Type PdfKit.PdfActionNamedName</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfActionNamedName {
	<span class='added added-field ' data-is-non-breaking="">Find = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">FirstPage = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">GoBack = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">GoForward = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">GoToPage = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LastPage = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">NextPage = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PreviousPage = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Print = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">ZoomIn = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">ZoomOut = 11,</span>
}
</pre>
</div> <!-- end type PdfActionNamedName -->
<div> <!-- start type PdfActionRemoteGoTo -->
<h3>New Type PdfKit.PdfActionRemoteGoTo</h3>
<pre class='added' data-is-non-breaking="">
public class PdfActionRemoteGoTo : PdfKit.PdfAction, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionRemoteGoTo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionRemoteGoTo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionRemoteGoTo (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionRemoteGoTo (nint pageIndex, CoreGraphics.CGPoint point, Foundation.NSUrl fileUrl);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PageIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint Point { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; set; }</span>
}
</pre>
</div> <!-- end type PdfActionRemoteGoTo -->
<div> <!-- start type PdfActionResetForm -->
<h3>New Type PdfKit.PdfActionResetForm</h3>
<pre class='added' data-is-non-breaking="">
public class PdfActionResetForm : PdfKit.PdfAction, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionResetForm ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionResetForm (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionResetForm (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Fields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FieldsIncludedAreCleared { get; set; }</span>
}
</pre>
</div> <!-- end type PdfActionResetForm -->
<div> <!-- start type PdfActionUrl -->
<h3>New Type PdfKit.PdfActionUrl</h3>
<pre class='added' data-is-non-breaking="">
public class PdfActionUrl : PdfKit.PdfAction, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionUrl ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionUrl (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfActionUrl (Foundation.NSUrl url);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfActionUrl (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; set; }</span>
}
</pre>
</div> <!-- end type PdfActionUrl -->
<div> <!-- start type PdfAnnotation -->
<h3>New Type PdfKit.PdfAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public class PdfAnnotation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation (CoreGraphics.CGRect bounds);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAnnotation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAnnotation (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation (CoreGraphics.CGRect bounds, Foundation.NSString annotationType, Foundation.NSDictionary properties);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation (CoreGraphics.CGRect bounds, PdfAnnotationKey annotationType, Foundation.NSDictionary properties);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfAction Action { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UITextAlignment Alignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsToggleToOff { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary AnnotationKeyValues { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PdfAnnotationKey AnnotationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfBorder Border { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Bounds { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetCellState ButtonWidgetState { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ButtonWidgetStateString { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Caption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Choices { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor Color { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Comb { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Contents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDestination Destination { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfLineStyle EndLineStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint EndPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FieldName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIFont Font { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor FontColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAppearanceStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Highlighted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfTextAnnotationIconType IconType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsPasswordField { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ListChoice { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfMarkupType MarkupType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MaximumLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ModificationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfAction MouseUpAction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Multiline { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Open { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfPage Page { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIBezierPath[] Paths { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSValue[] QuadrilateralPoints { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RadiosInUnison { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReadOnly { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldDisplay { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldPrint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfLineStyle StartLineStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint StartPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ToolTip { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Type { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string UserName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Values { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetControlType WidgetControlType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetDefaultStringValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetFieldType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetStringValue { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddBezierPath (UIKit.UIBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (PdfDisplayBox box, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfLineStyle GetLineStyle (string fromName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetName (PdfLineStyle style);</span>
	<span class='added added-method ' data-is-non-breaking="">public T GetValue&lt;T&gt; (PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllAppearanceStreams ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveBezierPath (UIKit.UIBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void RemoveValue (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveValue (PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual bool SetValue (CoreGraphics.CGRect rect, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (CoreGraphics.CGRect rect, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual bool SetValue (bool boolean, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (bool boolean, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (string str, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue&lt;T&gt; (T value, PdfAnnotationKey key);</span>
}
</pre>
</div> <!-- end type PdfAnnotation -->
<div> <!-- start type PdfAnnotationHighlightingMode -->
<h3>New Type PdfKit.PdfAnnotationHighlightingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationHighlightingMode {
	<span class='added added-field ' data-is-non-breaking="">Invert = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Outline = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Push = 3,</span>
}
</pre>
</div> <!-- end type PdfAnnotationHighlightingMode -->
<div> <!-- start type PdfAnnotationHighlightingModeExtensions -->
<h3>New Type PdfKit.PdfAnnotationHighlightingModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationHighlightingModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationHighlightingMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationHighlightingMode GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationHighlightingModeExtensions -->
<div> <!-- start type PdfAnnotationKey -->
<h3>New Type PdfKit.PdfAnnotationKey</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationKey {
	<span class='added added-field ' data-is-non-breaking="">Action = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">AdditionalActions = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">AppearanceDictionary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AppearanceState = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Border = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">BorderStyle = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Color = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Contents = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Date = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DefaultAppearance = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Destination = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Flags = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HighlightingMode = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">IconName = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">Inklist = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">InteriorColor = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">LineEndingStyles = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">LinePoints = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Name = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Open = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">Page = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Parent = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">Popup = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">QuadPoints = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">Quadding = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Rect = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtype = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">TextLabel = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetAppearanceDictionary = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetBackgroundColor = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetBorderColor = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetCaption = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetDefaultValue = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetDownCaption = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetFieldFlags = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetFieldType = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetMaxLen = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetOptions = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetRolloverCaption = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetRotation = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetTextLabelUI = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetValue = 41,</span>
}
</pre>
</div> <!-- end type PdfAnnotationKey -->
<div> <!-- start type PdfAnnotationKeyExtensions -->
<h3>New Type PdfKit.PdfAnnotationKeyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationKeyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationKey self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationKey GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationKeyExtensions -->
<div> <!-- start type PdfAnnotationLineEndingStyle -->
<h3>New Type PdfKit.PdfAnnotationLineEndingStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationLineEndingStyle {
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ClosedArrow = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OpenArrow = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 1,</span>
}
</pre>
</div> <!-- end type PdfAnnotationLineEndingStyle -->
<div> <!-- start type PdfAnnotationLineEndingStyleExtensions -->
<h3>New Type PdfKit.PdfAnnotationLineEndingStyleExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationLineEndingStyleExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationLineEndingStyle self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationLineEndingStyle GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationLineEndingStyleExtensions -->
<div> <!-- start type PdfAnnotationSubtype -->
<h3>New Type PdfKit.PdfAnnotationSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationSubtype {
	<span class='added added-field ' data-is-non-breaking="">Circle = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FreeText = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Highlight = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Ink = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Line = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Popup = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Stamp = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikeOut = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Underline = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Widget = 12,</span>
}
</pre>
</div> <!-- end type PdfAnnotationSubtype -->
<div> <!-- start type PdfAnnotationSubtypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationSubtypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationSubtypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationSubtype self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationSubtype GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationSubtypeExtensions -->
<div> <!-- start type PdfAnnotationTextIconType -->
<h3>New Type PdfKit.PdfAnnotationTextIconType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationTextIconType {
	<span class='added added-field ' data-is-non-breaking="">Comment = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Help = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Key = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NewParagraph = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Note = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Paragraph = 5,</span>
}
</pre>
</div> <!-- end type PdfAnnotationTextIconType -->
<div> <!-- start type PdfAnnotationTextIconTypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationTextIconTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationTextIconTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationTextIconType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationTextIconType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationTextIconTypeExtensions -->
<div> <!-- start type PdfAnnotationWidgetSubtype -->
<h3>New Type PdfKit.PdfAnnotationWidgetSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationWidgetSubtype {
	<span class='added added-field ' data-is-non-breaking="">Button = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Choice = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Signature = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 3,</span>
}
</pre>
</div> <!-- end type PdfAnnotationWidgetSubtype -->
<div> <!-- start type PdfAnnotationWidgetSubtypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationWidgetSubtypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationWidgetSubtypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationWidgetSubtype self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationWidgetSubtype GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationWidgetSubtypeExtensions -->
<div> <!-- start type PdfAppearanceCharacteristics -->
<h3>New Type PdfKit.PdfAppearanceCharacteristics</h3>
<pre class='added' data-is-non-breaking="">
public class PdfAppearanceCharacteristics : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAppearanceCharacteristics ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAppearanceCharacteristics (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAppearanceCharacteristics (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor BorderColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Caption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetControlType ControlType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DownCaption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RolloverCaption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Rotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakAppearanceCharacteristicsKeyValues { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PdfAppearanceCharacteristics -->
<div> <!-- start type PdfAppearanceCharacteristicsKeys -->
<h3>New Type PdfKit.PdfAppearanceCharacteristicsKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAppearanceCharacteristicsKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BackgroundColorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BorderColorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DownCaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RolloverCaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RotationKey { get; }</span>
}
</pre>
</div> <!-- end type PdfAppearanceCharacteristicsKeys -->
<div> <!-- start type PdfAreaOfInterest -->
<h3>New Type PdfKit.PdfAreaOfInterest</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PdfAreaOfInterest {
	<span class='added added-field ' data-is-non-breaking="">AnnotationArea = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ControlArea = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">IconArea = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageArea = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">LinkArea = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">NoArea = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PageArea = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PopupArea = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">TextArea = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TextFieldArea = 32,</span>
}
</pre>
</div> <!-- end type PdfAreaOfInterest -->
<div> <!-- start type PdfBorder -->
<h3>New Type PdfKit.PdfBorder</h3>
<pre class='added' data-is-non-breaking="">
public class PdfBorder : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfBorder ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfBorder (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfBorder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfBorder (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat HorizontalCornerRadius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat LineWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfBorderStyle Style { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat VerticalCornerRadius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakBorderKeyValues { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSArray WeakDashPattern { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PdfBorder -->
<div> <!-- start type PdfBorderKeys -->
<h3>New Type PdfKit.PdfBorderKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfBorderKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DashPatternKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LineWidthKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString StyleKey { get; }</span>
}
</pre>
</div> <!-- end type PdfBorderKeys -->
<div> <!-- start type PdfBorderStyle -->
<h3>New Type PdfKit.PdfBorderStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfBorderStyle {
	<span class='added added-field ' data-is-non-breaking="">Beveled = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Dashed = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inset = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Solid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Underline = 4,</span>
}
</pre>
</div> <!-- end type PdfBorderStyle -->
<div> <!-- start type PdfDestination -->
<h3>New Type PdfKit.PdfDestination</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDestination : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDestination ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfDestination (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfDestination (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDestination (PdfPage page, CoreGraphics.CGPoint point);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfPage Page { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint Point { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Zoom { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSComparisonResult Compare (PdfDestination destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PdfDestination -->
<div> <!-- start type PdfDisplayBox -->
<h3>New Type PdfKit.PdfDisplayBox</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfDisplayBox {
	<span class='added added-field ' data-is-non-breaking="">Art = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Bleed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Crop = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Media = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Trim = 3,</span>
}
</pre>
</div> <!-- end type PdfDisplayBox -->
<div> <!-- start type PdfDisplayDirection -->
<h3>New Type PdfKit.PdfDisplayDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfDisplayDirection {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertical = 0,</span>
}
</pre>
</div> <!-- end type PdfDisplayDirection -->
<div> <!-- start type PdfDisplayMode -->
<h3>New Type PdfKit.PdfDisplayMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfDisplayMode {
	<span class='added added-field ' data-is-non-breaking="">SinglePage = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SinglePageContinuous = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TwoUp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TwoUpContinuous = 3,</span>
}
</pre>
</div> <!-- end type PdfDisplayMode -->
<div> <!-- start type PdfDocument -->
<h3>New Type PdfKit.PdfDocument</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDocument : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocument ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocument (Foundation.NSData data);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfDocument (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocument (Foundation.NSUrl url);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfDocument (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsCommenting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsContentAccessibility { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsCopying { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentAssembly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsFormFieldEntry { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsPrinting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IPdfDocumentDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginPageFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginPageWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndPageFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndPageWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidFindMatchNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidUnlockNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPDFDocument Document { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary DocumentAttributes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl DocumentUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ClassForAnnotationTypeDelegate GetClassForAnnotationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsEncrypted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsFinding { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsLocked { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MajorVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MinorVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfOutline OutlineRoot { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Class PageClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PageCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Type PageType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDocumentPermissions PermissionsStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Text { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidBeginDocumentFind;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidMatchString;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUnlock;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler FindFinished;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler MatchFound;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler PageFindFinished;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler PageFindStarted;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelFind ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ExchangePages (nint indexA, nint indexB);</span>
	<span class='added added-method ' data-is-non-breaking="">public PdfSelection[] Find (string text, Foundation.NSStringCompareOptions compareOptions);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'Find (string, NSStringCompareOptions)' instead.")]
	public virtual PdfSelection[] Find (string text, nint options);</span>
	<span class='added added-method ' data-is-non-breaking="">public PdfSelection Find (string text, PdfSelection selection, Foundation.NSStringCompareOptions compareOptions);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'Find (string, PdfSelection, NSStringCompareOptions)' instead.")]
	public virtual PdfSelection Find (string text, PdfSelection selection, nint options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FindAsync (string text, Foundation.NSStringCompareOptions compareOptions);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'FindAsync (string, NSStringCompareOptions)' instead.")]
	public virtual void FindAsync (string text, nint options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FindAsync (string[] text, Foundation.NSStringCompareOptions compareOptions);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'FindAsync (string [], NSStringCompareOptions)' instead.")]
	public virtual void FindAsync (string[] text, nint options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetDataRepresentation ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetDataRepresentation (Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public PdfDocumentAttributes GetDocumentAttributes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfPage GetPage (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPageIndex (PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection GetSelection (PdfPage startPage, CoreGraphics.CGPoint startPoint, PdfPage endPage, CoreGraphics.CGPoint endPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection GetSelection (PdfPage startPage, nint startCharIndex, PdfPage endPage, nint endCharIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InsertPage (PdfPage page, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfOutline OutlineItem (PdfSelection selection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemovePage (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection SelectEntireDocument ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetDocumentAttributes (PdfDocumentAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Unlock (string password);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Write (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Write (string path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Write (Foundation.NSUrl url, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Write (Foundation.NSUrl url, PdfDocumentWriteOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Write (string path, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Write (string path, PdfDocumentWriteOptions options);</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginFind (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginFind (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginPageFind (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginPageFind (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginPageWrite (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginPageWrite (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginWrite (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginWrite (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndFind (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndFind (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndPageFind (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndPageFind (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndPageWrite (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndPageWrite (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndWrite (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndWrite (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidFindMatch (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidFindMatch (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidUnlock (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidUnlock (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	}
}
</pre>
</div> <!-- end type PdfDocument -->
<div> <!-- start type PdfDocumentAttributes -->
<h3>New Type PdfKit.PdfDocumentAttributes</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDocumentAttributes : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentAttributes ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentAttributes (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Author { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDate CreationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Creator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Keywords { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDate ModificationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Producer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Subject { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Title { get; set; }</span>
}
</pre>
</div> <!-- end type PdfDocumentAttributes -->
<div> <!-- start type PdfDocumentDelegate -->
<h3>New Type PdfKit.PdfDocumentDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDocumentDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IPdfDocumentDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfDocumentDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfDocumentDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidBeginDocumentFind (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidMatchString (PdfSelection sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUnlock (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FindFinished (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForAnnotationType (string annotationType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForPage ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MatchFound (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PageFindFinished (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PageFindStarted (Foundation.NSNotification notification);</span>
}
</pre>
</div> <!-- end type PdfDocumentDelegate -->
<div> <!-- start type PdfDocumentDelegate_Extensions -->
<h3>New Type PdfKit.PdfDocumentDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfDocumentDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidBeginDocumentFind (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidMatchString (IPdfDocumentDelegate This, PdfSelection sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUnlock (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void FindFinished (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ObjCRuntime.Class GetClassForAnnotationType (IPdfDocumentDelegate This, string annotationType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ObjCRuntime.Class GetClassForPage (IPdfDocumentDelegate This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void MatchFound (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PageFindFinished (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PageFindStarted (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
}
</pre>
</div> <!-- end type PdfDocumentDelegate_Extensions -->
<div> <!-- start type PdfDocumentPermissions -->
<h3>New Type PdfKit.PdfDocumentPermissions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfDocumentPermissions {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Owner = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">User = 1,</span>
}
</pre>
</div> <!-- end type PdfDocumentPermissions -->
<div> <!-- start type PdfDocumentWriteOptions -->
<h3>New Type PdfKit.PdfDocumentWriteOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDocumentWriteOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentWriteOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentWriteOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string OwnerPassword { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string UserPassword { get; set; }</span>
}
</pre>
</div> <!-- end type PdfDocumentWriteOptions -->
<div> <!-- start type PdfInterpolationQuality -->
<h3>New Type PdfKit.PdfInterpolationQuality</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfInterpolationQuality {
	<span class='added added-field ' data-is-non-breaking="">High = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Low = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type PdfInterpolationQuality -->
<div> <!-- start type PdfLineStyle -->
<h3>New Type PdfKit.PdfLineStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfLineStyle {
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ClosedArrow = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OpenArrow = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 1,</span>
}
</pre>
</div> <!-- end type PdfLineStyle -->
<div> <!-- start type PdfMarkupType -->
<h3>New Type PdfKit.PdfMarkupType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfMarkupType {
	<span class='added added-field ' data-is-non-breaking="">Highlight = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikeOut = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Underline = 2,</span>
}
</pre>
</div> <!-- end type PdfMarkupType -->
<div> <!-- start type PdfOutline -->
<h3>New Type PdfKit.PdfOutline</h3>
<pre class='added' data-is-non-breaking="">
public class PdfOutline : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfOutline ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfOutline (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfOutline (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfAction Action { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint ChildrenCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDestination Destination { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDocument Document { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Index { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOpen { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfOutline Parent { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfOutline Child (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InsertChild (PdfOutline child, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveFromParent ();</span>
}
</pre>
</div> <!-- end type PdfOutline -->
<div> <!-- start type PdfPage -->
<h3>New Type PdfKit.PdfPage</h3>
<pre class='added' data-is-non-breaking="">
public class PdfPage : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfPage ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfPage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfPage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfPage (UIKit.UIImage image);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfAnnotation[] Annotations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint CharacterCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData DataRepresentation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplaysAnnotations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDocument Document { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPDFPage Page { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Rotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Text { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnnotation (PdfAnnotation annotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (PdfDisplayBox box, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfAnnotation GetAnnotation (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetBoundsForBox (PdfDisplayBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetCharacterBounds (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetCharacterIndex (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection GetSelection (CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection GetSelection (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection GetSelection (CoreGraphics.CGPoint startPoint, CoreGraphics.CGPoint endPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIKit.UIImage GetThumbnail (CoreGraphics.CGSize size, PdfDisplayBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform GetTransform (PdfDisplayBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnnotation (PdfAnnotation annotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection SelectLine (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection SelectWord (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetBoundsForBox (CoreGraphics.CGRect bounds, PdfDisplayBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TransformContext (CoreGraphics.CGContext context, PdfDisplayBox box);</span>
}
</pre>
</div> <!-- end type PdfPage -->
<div> <!-- start type PdfPrintScalingMode -->
<h3>New Type PdfKit.PdfPrintScalingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfPrintScalingMode {
	<span class='added added-field ' data-is-non-breaking="">DownToFit = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ToFit = 1,</span>
}
</pre>
</div> <!-- end type PdfPrintScalingMode -->
<div> <!-- start type PdfSelection -->
<h3>New Type PdfKit.PdfSelection</h3>
<pre class='added' data-is-non-breaking="">
public class PdfSelection : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfSelection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfSelection (PdfDocument document);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfSelection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor Color { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfPage[] Pages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Text { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddSelection (PdfSelection selection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddSelections (PdfSelection[] selections);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (PdfPage page, bool active);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (PdfPage page, PdfDisplayBox box, bool active);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ExtendSelectionAtEnd (nint succeed);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ExtendSelectionAtStart (nint precede);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ExtendSelectionForLineBoundaries ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetBoundsForPage (PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetNumberOfTextRanges (PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetRange (uint index, PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection[] SelectionsByLine ();</span>
}
</pre>
</div> <!-- end type PdfSelection -->
<div> <!-- start type PdfTextAnnotationIconType -->
<h3>New Type PdfKit.PdfTextAnnotationIconType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfTextAnnotationIconType {
	<span class='added added-field ' data-is-non-breaking="">Comment = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Help = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Key = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NewParagraph = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Note = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Paragraph = 5,</span>
}
</pre>
</div> <!-- end type PdfTextAnnotationIconType -->
<div> <!-- start type PdfThumbnailLayoutMode -->
<h3>New Type PdfKit.PdfThumbnailLayoutMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfThumbnailLayoutMode {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertical = 0,</span>
}
</pre>
</div> <!-- end type PdfThumbnailLayoutMode -->
<div> <!-- start type PdfThumbnailView -->
<h3>New Type PdfKit.PdfThumbnailView</h3>
<pre class='added' data-is-non-breaking="">
public class PdfThumbnailView : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfThumbnailView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfThumbnailView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfThumbnailView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfThumbnailView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfThumbnailView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static PdfThumbnailView.PdfThumbnailViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIEdgeInsets ContentInset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DocumentEditedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfThumbnailLayoutMode LayoutMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfView PdfView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfPage[] SelectedPages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize ThumbnailSize { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PdfThumbnailView.PdfThumbnailViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfThumbnailView.PdfThumbnailViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfThumbnailView.PdfThumbnailViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfThumbnailView.PdfThumbnailViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfThumbnailView.PdfThumbnailViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfThumbnailView.PdfThumbnailViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDocumentEdited (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDocumentEdited (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	}
	public class PdfThumbnailViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected PdfThumbnailView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type PdfThumbnailView -->
<div> <!-- start type PdfView -->
<h3>New Type PdfKit.PdfView</h3>
<pre class='added' data-is-non-breaking="">
public class PdfView : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUIGestureRecognizerDelegate, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationHitNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationWillHitNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PdfView.PdfViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutoScales { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanGoBack { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanGoForward { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanGoToFirstPage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanGoToLastPage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanGoToNextPage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanGoToPreviousPage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanZoomIn { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanZoomOut { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChangedHistoryNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CopyPermissionNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDestination CurrentDestination { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfPage CurrentPage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfSelection CurrentSelection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IPdfViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDisplayBox DisplayBox { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisplayBoxChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDisplayDirection DisplayDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDisplayMode DisplayMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisplayModeChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplaysAsBook { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplaysPageBreaks { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplaysRtl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDocument Document { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DocumentChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIView DocumentView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool EnableDataDetectors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat GreekingThreshold { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfSelection[] HighlightedSelections { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfInterpolationQuality InterpolationQuality { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsUsingPageViewController { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaxScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIEdgeInsets PageBreakMargins { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PageChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PrintPermissionNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ScaleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScaleFactorForSizeToFit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectionChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldAntiAlias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfPage[] VisiblePages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VisiblePagesChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;PdfViewActionEventArgs&gt; OpenPdf;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler PerformFind;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler PerformGoToPage;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;PdfViewUrlEventArgs&gt; WillClickOnLink;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnnotationsChanged (PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfView.PdfViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ClearSelection ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint ConvertPointFromPage (CoreGraphics.CGPoint point, PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint ConvertPointToPage (CoreGraphics.CGPoint point, PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect ConvertRectangleFromPage (CoreGraphics.CGRect rect, PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect ConvertRectangleToPage (CoreGraphics.CGRect rect, PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Copy (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DrawPage (PdfPage page, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DrawPagePost (PdfPage page, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfView.PdfViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfView.PdfViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfView.PdfViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfView.PdfViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfView.PdfViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfAreaOfInterest GetAreaOfInterest (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfAreaOfInterest GetAreaOfInterest (UIKit.UIEvent mouseEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfPage GetPage (CoreGraphics.CGPoint point, bool nearest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoBack (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoForward (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoToDestination (PdfDestination destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoToFirstPage (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoToLastPage (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoToNextPage (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoToPage (PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoToPreviousPage (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoToRectangle (CoreGraphics.CGRect rect, PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GoToSelection (PdfSelection selection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LayoutDocumentView ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformAction (PdfAction action);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize RowSize (PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScrollSelectionToVisible (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SelectAll (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCurrentSelection (PdfSelection selection, bool animate);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldBeRequiredToFailBy (UIKit.UIGestureRecognizer gestureRecognizer, UIKit.UIGestureRecognizer otherGestureRecognizer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldBegin (UIKit.UIGestureRecognizer recognizer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldReceivePress (UIKit.UIGestureRecognizer gestureRecognizer, UIKit.UIPress press);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldReceiveTouch (UIKit.UIGestureRecognizer recognizer, UIKit.UITouch touch);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldRecognizeSimultaneously (UIKit.UIGestureRecognizer gestureRecognizer, UIKit.UIGestureRecognizer otherGestureRecognizer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldRequireFailureOf (UIKit.UIGestureRecognizer gestureRecognizer, UIKit.UIGestureRecognizer otherGestureRecognizer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TakeBackgroundColor (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TakePasswordFrom (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UsePageViewController (bool enable, Foundation.NSDictionary viewOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ZoomIn (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ZoomOut (Foundation.NSObject sender);</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnotationHit (System.EventHandler&lt;PdfViewAnnotationHitEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnotationHit (Foundation.NSObject objectToObserve, System.EventHandler&lt;PdfViewAnnotationHitEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnotationWillHit (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnotationWillHit (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChangedHistory (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChangedHistory (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCopyPermission (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCopyPermission (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDisplayBoxChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDisplayBoxChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDisplayModeChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDisplayModeChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDocumentChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDocumentChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePageChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePageChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePrintPermission (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePrintPermission (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveScaleChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveScaleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVisiblePagesChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVisiblePagesChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	}
	public class PdfViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected PdfView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type PdfView -->
<div> <!-- start type PdfViewActionEventArgs -->
<h3>New Type PdfKit.PdfViewActionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class PdfViewActionEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfViewActionEventArgs (PdfActionRemoteGoTo action);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public PdfActionRemoteGoTo Action { get; set; }</span>
}
</pre>
</div> <!-- end type PdfViewActionEventArgs -->
<div> <!-- start type PdfViewAnnotationHitEventArgs -->
<h3>New Type PdfKit.PdfViewAnnotationHitEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class PdfViewAnnotationHitEventArgs : Foundation.NSNotificationEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfViewAnnotationHitEventArgs (Foundation.NSNotification notification);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public PdfAnnotation AnnotationHit { get; }</span>
}
</pre>
</div> <!-- end type PdfViewAnnotationHitEventArgs -->
<div> <!-- start type PdfViewDelegate -->
<h3>New Type PdfKit.PdfViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class PdfViewDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IPdfViewDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenPdf (PdfView sender, PdfActionRemoteGoTo action);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformFind (PdfView sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformGoToPage (PdfView sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillClickOnLink (PdfView sender, Foundation.NSUrl url);</span>
}
</pre>
</div> <!-- end type PdfViewDelegate -->
<div> <!-- start type PdfViewDelegate_Extensions -->
<h3>New Type PdfKit.PdfViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void OpenPdf (IPdfViewDelegate This, PdfView sender, PdfActionRemoteGoTo action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PerformFind (IPdfViewDelegate This, PdfView sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PerformGoToPage (IPdfViewDelegate This, PdfView sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillClickOnLink (IPdfViewDelegate This, PdfView sender, Foundation.NSUrl url);</span>
}
</pre>
</div> <!-- end type PdfViewDelegate_Extensions -->
<div> <!-- start type PdfViewUrlEventArgs -->
<h3>New Type PdfKit.PdfViewUrlEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class PdfViewUrlEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfViewUrlEventArgs (Foundation.NSUrl url);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl Url { get; set; }</span>
}
</pre>
</div> <!-- end type PdfViewUrlEventArgs -->
<div> <!-- start type PdfWidgetCellState -->
<h3>New Type PdfKit.PdfWidgetCellState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfWidgetCellState {
	<span class='added added-field ' data-is-non-breaking="">Mixed = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">On = 1,</span>
}
</pre>
</div> <!-- end type PdfWidgetCellState -->
<div> <!-- start type PdfWidgetControlType -->
<h3>New Type PdfKit.PdfWidgetControlType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfWidgetControlType {
	<span class='added added-field ' data-is-non-breaking="">CheckBox = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">PushButton = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RadioButton = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = -1,</span>
}
</pre>
</div> <!-- end type PdfWidgetControlType -->
</div> <!-- end namespace PdfKit -->

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
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIBarcodeDescriptor BarcodeDescriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PayloadStringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VNBarcodeSymbology Symbology { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakSymbology { get; }</span>
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
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString[] GetConstants (VNBarcodeSymbology[] self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology GetValue (Foundation.NSString constant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology[] GetValues (Foundation.NSString[] constants);</span>
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
	<span class='added added-property ' data-is-non-breaking="">public static VNBarcodeSymbology[] SupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VNBarcodeSymbology[] Symbologies { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected static Foundation.NSString[] WeakSupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString[] WeakSymbologies { get; set; }</span>
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
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint[] NormalizedPoints { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint[] GetPointsInImage (CoreGraphics.CGSize imageSize);</span>
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
	<span class='added added-property ' data-is-non-breaking="">public CoreImage.CIContext CIContext { get; set; }</span>
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
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesCpuOnly { get; set; }</span>
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
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
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
