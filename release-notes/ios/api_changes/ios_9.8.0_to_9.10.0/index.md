---
id: 11C69C88-74FF-4F88-8325-A049E3C721A5
title: "iOS 9.8.0 to 9.10.0"
---

# API diff

 [(Classic) mscorlib.dll](#diff/xi/2.1/mscorlib.html)

   


 [(Classic) System.dll](#diff/xi/2.1/System.html)

   


 [(Classic) System.Core.dll](#diff/xi/2.1/System.Core.html)

   


 [(Classic) System.Data.dll](#diff/xi/2.1/System.Data.html)

   


 [(Classic) System.ServiceModel.dll](#diff/xi/2.1/System.ServiceModel.html)

   


 [(Classic) System.Transactions.dll](#diff/xi/2.1/System.Transactions.html)

   


 [(Classic) monotouch.dll](#diff/xi/2.1/monotouch.html)

   


 [(Classic) MonoTouch.NUnitLite.dll](#diff/xi/2.1/MonoTouch.NUnitLite.html)

   


 [(Classic) System.Net.Http.dll](#diff/xi/2.1/System.Net.Http.html)

   


 [(Unified) MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.iOS/MonoTouch.NUnitLite.html)

   


 [(Unified) System.Net.Http.dll](#diff/xi/Xamarin.iOS/System.Net.Http.html)

   


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
<!-- start namespace Microsoft.Win32 --> <div> 
<h2>Namespace Microsoft.Win32</h2>
<!-- start type RegistryKey --> <div>
<h3>Type Changed: Microsoft.Win32.RegistryKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public SafeHandles.SafeRegistryHandle Handle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int SubKeyCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int ValueCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public RegistryView View { get; }</span>
</pre>
</div>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static object GetValue (string keyName, string valueName, object defaultValue);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey, bool writable);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey, bool writable, RegistryOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteSubKey (string subkey);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteSubKey (string subkey, bool throwOnMissingSubKey);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteSubKeyTree (string subkey);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteSubKeyTree (string subkey, bool throwOnMissingSubKey);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteValue (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteValue (string name, bool throwOnMissingValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Flush ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static RegistryKey FromHandle (SafeHandles.SafeRegistryHandle handle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static RegistryKey FromHandle (SafeHandles.SafeRegistryHandle handle, RegistryView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public string[] GetSubKeyNames ();</span>
	<span class='added added-method ' data-is-non-breaking="">public object GetValue (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public object GetValue (string name, object defaultValue, RegistryValueOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryValueKind GetValueKind (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public string[] GetValueNames ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static RegistryKey OpenBaseKey (RegistryHive hKey, RegistryView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey OpenSubKey (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey OpenSubKey (string name, System.Security.AccessControl.RegistryRights rights);</span>
</pre>
</div>

</div> <!-- end type RegistryKey -->

</div> <!-- end namespace Microsoft.Win32 -->
<!-- start namespace Microsoft.Win32.SafeHandles --> <div> 
<h2>Namespace Microsoft.Win32.SafeHandles</h2>
<!-- start type SafeAccessTokenHandle --> <div>
<h3>Type Changed: Microsoft.Win32.SafeHandles.SafeAccessTokenHandle</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SafeAccessTokenHandle ();</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SafeAccessTokenHandle (IntPtr handle);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static SafeAccessTokenHandle InvalidHandle { get; }</span>
</pre>
</div>

</div> <!-- end type SafeAccessTokenHandle -->

</div> <!-- end namespace Microsoft.Win32.SafeHandles -->
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type AppContext --> <div>
<h3>Type Changed: System.AppContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string BaseDirectory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string TargetFrameworkName { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static object GetData (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSwitch (string switchName, bool isEnabled);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryGetSwitch (string switchName, out bool isEnabled);</span>
</pre>
</div>

</div> <!-- end type AppContext -->
<!-- start type Console --> <div>
<h3>Type Changed: System.Console</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static ConsoleColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int BufferHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int BufferWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool CapsLock { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int CursorLeft { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int CursorSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int CursorTop { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool CursorVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ConsoleColor ForegroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsErrorRedirected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsInputRedirected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsOutputRedirected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool KeyAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int LargestWindowHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int LargestWindowWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool NumberLock { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool TreatControlCAsInput { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int WindowHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int WindowLeft { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int WindowTop { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int WindowWidth { get; set; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event ConsoleCancelEventHandler CancelKeyPress;</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void Beep ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Beep (int frequency, int duration);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Clear ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void MoveBufferArea (int sourceLeft, int sourceTop, int sourceWidth, int sourceHeight, int targetLeft, int targetTop);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void MoveBufferArea (int sourceLeft, int sourceTop, int sourceWidth, int sourceHeight, int targetLeft, int targetTop, char sourceChar, ConsoleColor sourceForeColor, ConsoleColor sourceBackColor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ConsoleKeyInfo ReadKey ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static ConsoleKeyInfo ReadKey (bool intercept);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResetColor ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetBufferSize (int width, int height);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetCursorPosition (int left, int top);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetWindowPosition (int left, int top);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetWindowSize (int width, int height);</span>
</pre>
</div>

</div> <!-- end type Console -->
<!-- start type Environment --> <div>
<h3>Type Changed: System.Environment</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static string GetEnvironmentVariable (string variable, EnvironmentVariableTarget target);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Collections.IDictionary GetEnvironmentVariables (EnvironmentVariableTarget target);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetEnvironmentVariable (string variable, string value, EnvironmentVariableTarget target);</span>
</pre>
</div>

</div> <!-- end type Environment -->

</div> <!-- end namespace System -->
<!-- start namespace System.Diagnostics.Tracing --> <div> 
<h2>Namespace System.Diagnostics.Tracing</h2>
<!-- start type EventAttribute --> <div>
<h3>Type Changed: System.Diagnostics.Tracing.EventAttribute</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public EventActivityOptions ActivityOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventChannel Channel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventOpcode Opcode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventTags Tags { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventTask Task { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte Version { get; set; }</span>
</pre>
</div>

</div> <!-- end type EventAttribute -->
<!-- start type EventSource --> <div>
<h3>Type Changed: System.Diagnostics.Tracing.EventSource</h3>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;EventCommandEventArgs&gt; EventCommandExecuted;</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static string GenerateManifest (System.Type eventSourceType, string assemblyPathToIncludeInManifest);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GenerateManifest (System.Type eventSourceType, string assemblyPathToIncludeInManifest, EventManifestOptions flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Guid GetGuid (System.Type eventSourceType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetName (System.Type eventSourceType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IEnumerable&lt;EventSource&gt; GetSources ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SendCommand (EventSource eventSource, EventCommand command, System.Collections.Generic.IDictionary&lt;System.String,System.String&gt; commandArguments);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetCurrentThreadActivityId (System.Guid activityId);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetCurrentThreadActivityId (System.Guid activityId, out System.Guid oldActivityThatWillContinue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Write (string eventName, EventSourceOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void WriteEventCore (int eventId, int eventDataCount, EventSource.EventData* data);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void WriteEventWithRelatedActivityId (int eventId, System.Guid relatedActivityId, object[] args);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void WriteEventWithRelatedActivityIdCore (int eventId, System.Guid* relatedActivityId, int eventDataCount, EventSource.EventData* data);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~EventSource ();</span>
</pre>
</div>

</div> <!-- end type EventSource -->

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
<!-- start type File --> <div>
<h3>Type Changed: System.IO.File</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static FileStream Create (string path, int bufferSize, FileOptions options);</span>
</pre>
</div>

</div> <!-- end type File -->
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
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<!-- start type ConditionalWeakTable`2 --> <div>
<h3>Type Changed: System.Runtime.CompilerServices.ConditionalWeakTable`2</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~ConditionalWeakTable ();</span>
</pre>
</div>

</div> <!-- end type ConditionalWeakTable`2 -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
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
<!-- start type Marshal --> <div>
<h3>Type Changed: System.Runtime.InteropServices.Marshal</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool AreComObjectsAvailableForCleanup ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static TWrapper CreateWrapperOfType&lt;T, TWrapper&gt; (T o);</span>
	<span class='added added-method ' data-is-non-breaking="">public static object CreateWrapperOfType (object o, System.Type t);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int FinalReleaseComObject (object o);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetComInterfaceForObject&lt;T, TInterface&gt; (T o);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetComInterfaceForObject (object o, System.Type T);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetComInterfaceForObject (object o, System.Type T, CustomQueryInterfaceMode mode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetExceptionCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetHRForException (System.Exception e);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetHRForLastWin32Error ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetIUnknownForObject (object o);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetNativeVariantForObject (object obj, IntPtr pDstNativeVariant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetNativeVariantForObject&lt;T&gt; (T obj, IntPtr pDstNativeVariant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static object GetObjectForIUnknown (IntPtr pUnk);</span>
	<span class='added added-method ' data-is-non-breaking="">public static T GetObjectForNativeVariant&lt;T&gt; (IntPtr pSrcNativeVariant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static object GetObjectForNativeVariant (IntPtr pSrcNativeVariant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static T[] GetObjectsForNativeVariants&lt;T&gt; (IntPtr aSrcNativeVariant, int cVars);</span>
	<span class='added added-method ' data-is-non-breaking="">public static object[] GetObjectsForNativeVariants (IntPtr aSrcNativeVariant, int cVars);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetStartComSlot (System.Type t);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Type GetTypeFromCLSID (System.Guid clsid);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetTypeInfoName (ComTypes.ITypeInfo typeInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public static object GetUniqueObjectForIUnknown (IntPtr unknown);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsComObject (object o);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int ReleaseComObject (object o);</span>
</pre>
</div>

</div> <!-- end type Marshal -->
<div> <!-- start type ComImportAttribute -->
<h3>New Type System.Runtime.InteropServices.ComImportAttribute</h3>
<pre class='added' data-is-non-breaking="">
public sealed class ComImportAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ComImportAttribute ();</span>
}
</pre>
</div> <!-- end type ComImportAttribute -->
<div> <!-- start type DispatchWrapper -->
<h3>New Type System.Runtime.InteropServices.DispatchWrapper</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class DispatchWrapper {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DispatchWrapper (object obj);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public object WrappedObject { get; }</span>
}
</pre>
</div> <!-- end type DispatchWrapper -->
<div> <!-- start type ErrorWrapper -->
<h3>New Type System.Runtime.InteropServices.ErrorWrapper</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class ErrorWrapper {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ErrorWrapper (System.Exception e);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ErrorWrapper (int errorCode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ErrorWrapper (object errorCode);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int ErrorCode { get; }</span>
}
</pre>
</div> <!-- end type ErrorWrapper -->

</div> <!-- end namespace System.Runtime.InteropServices -->
<!-- start namespace System.Security --> <div> 
<h2>Namespace System.Security</h2>
<!-- start type CodeAccessPermission --> <div>
<h3>Type Changed: System.Security.CodeAccessPermission</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void Assert ()
</div><div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void Demand ()
</div><div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void Deny ()
</div><div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void PermitOnly ()
</div></pre>

</div> <!-- end type CodeAccessPermission -->

</div> <!-- end namespace System.Security -->
<!-- start namespace System.Security.AccessControl --> <div> 
<h2>Namespace System.Security.AccessControl</h2>
<!-- start type AuthorizationRuleCollection --> <div>
<h3>Type Changed: System.Security.AccessControl.AuthorizationRuleCollection</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AuthorizationRuleCollection ();</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddRule (AuthorizationRule rule);</span>
</pre>
</div>

</div> <!-- end type AuthorizationRuleCollection -->
<!-- start type CommonSecurityDescriptor --> <div>
<h3>Type Changed: System.Security.AccessControl.CommonSecurityDescriptor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddDiscretionaryAcl (byte revision, int trusted);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddSystemAcl (byte revision, int trusted);</span>
</pre>
</div>

</div> <!-- end type CommonSecurityDescriptor -->
<!-- start type DiscretionaryAcl --> <div>
<h3>Type Changed: System.Security.AccessControl.DiscretionaryAcl</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddAccess (AccessControlType accessType, System.Security.Principal.SecurityIdentifier sid, ObjectAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool RemoveAccess (AccessControlType accessType, System.Security.Principal.SecurityIdentifier sid, ObjectAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAccessSpecific (AccessControlType accessType, System.Security.Principal.SecurityIdentifier sid, ObjectAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAccess (AccessControlType accessType, System.Security.Principal.SecurityIdentifier sid, ObjectAccessRule rule);</span>
</pre>
</div>

</div> <!-- end type DiscretionaryAcl -->
<!-- start type ObjectSecurity --> <div>
<h3>Type Changed: System.Security.AccessControl.ObjectSecurity</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected ObjectSecurity ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ObjectSecurity (CommonSecurityDescriptor securityDescriptor);</span>
</pre>
</div>

</div> <!-- end type ObjectSecurity -->
<!-- start type SystemAcl --> <div>
<h3>Type Changed: System.Security.AccessControl.SystemAcl</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddAudit (System.Security.Principal.SecurityIdentifier sid, ObjectAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool RemoveAudit (System.Security.Principal.SecurityIdentifier sid, ObjectAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAuditSpecific (System.Security.Principal.SecurityIdentifier sid, ObjectAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAudit (System.Security.Principal.SecurityIdentifier sid, ObjectAuditRule rule);</span>
</pre>
</div>

</div> <!-- end type SystemAcl -->

</div> <!-- end namespace System.Security.AccessControl -->
<!-- start namespace System.Security.Principal --> <div> 
<h2>Namespace System.Security.Principal</h2>
<!-- start type WindowsIdentity --> <div>
<h3>Type Changed: System.Security.Principal.WindowsIdentity</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void RunImpersonated (Microsoft.Win32.SafeHandles.SafeAccessTokenHandle safeAccessTokenHandle, System.Action action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static T RunImpersonated&lt;T&gt; (Microsoft.Win32.SafeHandles.SafeAccessTokenHandle safeAccessTokenHandle, System.Func&lt;T&gt; func);</span>
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
<!-- start namespace Mono.Security.Interface --> <div> 
<h2>Namespace Mono.Security.Interface</h2>
<!-- start type MonoTlsProviderFactory --> <div>
<h3>Type Changed: Mono.Security.Interface.MonoTlsProviderFactory</h3>
<p>Removed field:</p>

<pre>
	<span class='removed removed-field breaking' data-is-breaking="">public static MonoTlsProviderFactoryDelegate _PrivateFactoryDelegate;</span>
</pre>

</div> <!-- end type MonoTlsProviderFactory -->
<h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoTlsProviderFactoryDelegate</span></h3>
</div> <!-- end namespace Mono.Security.Interface -->
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
<!-- start type ProcessModuleCollection --> <div>
<h3>Type Changed: System.Diagnostics.ProcessModuleCollection</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public ProcessModule Item { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (ProcessModule module);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (ProcessModule[] array, int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public int IndexOf (ProcessModule module);</span>
</pre>
</div>

</div> <!-- end type ProcessModuleCollection -->
<!-- start type ProcessModuleCollectionBase --> <div>
<h3>Type Changed: System.Diagnostics.ProcessModuleCollectionBase</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.IEnumerator GetEnumerator ();</span>
</pre>
</div>

</div> <!-- end type ProcessModuleCollectionBase -->
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
<!-- start type ProcessThreadCollection --> <div>
<h3>Type Changed: System.Diagnostics.ProcessThreadCollection</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public ProcessThread Item { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public int Add (ProcessThread thread);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (ProcessThread thread);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (ProcessThread[] array, int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public int IndexOf (ProcessThread thread);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Insert (int index, ProcessThread thread);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Remove (ProcessThread thread);</span>
</pre>
</div>

</div> <!-- end type ProcessThreadCollection -->
<!-- start type ProcessThreadCollectionBase --> <div>
<h3>Type Changed: System.Diagnostics.ProcessThreadCollectionBase</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.IEnumerator GetEnumerator ();</span>
</pre>
</div>

</div> <!-- end type ProcessThreadCollectionBase -->

</div> <!-- end namespace System.Diagnostics -->
<!-- start namespace System.IO --> <div> 
<h2>Namespace System.IO</h2>
<!-- start type FileSystemWatcher --> <div>
<h3>Type Changed: System.IO.FileSystemWatcher</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.IDisposable</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type FileSystemWatcher -->

</div> <!-- end namespace System.IO -->
<!-- start namespace System.IO.Compression --> <div> 
<h2>Namespace System.IO.Compression</h2>
<!-- start type DeflateStream --> <div>
<h3>Type Changed: System.IO.Compression.DeflateStream</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public DeflateStream (System.IO.Stream <span class='removed removed-inline '>compressedStream</span> <span class='added '>stream</span>, CompressionMode mode)
</div><div data-is-non-breaking="">	public DeflateStream (System.IO.Stream <span class='removed removed-inline '>compressedStream</span> <span class='added '>stream</span>, CompressionMode mode, bool leaveOpen)
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public override int Read (byte[] <span class='removed removed-inline '>dest</span> <span class='added '>array</span>, int <span class='removed removed-inline '>dest_offset</span> <span class='added '>offset</span>, int count)
</div><div data-is-non-breaking="">	public override void Write (byte[] <span class='removed removed-inline '>src</span> <span class='added '>array</span>, int <span class='removed removed-inline '>src_offset</span> <span class='added '>offset</span>, int count)
</div></pre>

</div> <!-- end type DeflateStream -->
<!-- start type GZipStream --> <div>
<h3>Type Changed: System.IO.Compression.GZipStream</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public override int Read (byte[] <span class='removed removed-inline '>dest</span> <span class='added '>array</span>, int <span class='removed removed-inline '>dest_offset</span> <span class='added '>offset</span>, int count)
</div><div data-is-non-breaking="">	public override void Write (byte[] <span class='removed removed-inline '>src</span> <span class='added '>array</span>, int <span class='removed removed-inline '>src_offset</span> <span class='added '>offset</span>, int count)
</div></pre>

</div> <!-- end type GZipStream -->

</div> <!-- end namespace System.IO.Compression -->
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
<!-- start type SslStream --> <div>
<h3>Type Changed: System.Net.Security.SslStream</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SslStream (System.IO.Stream innerStream, bool leaveInnerStreamOpen, RemoteCertificateValidationCallback userCertificateValidationCallback, LocalCertificateSelectionCallback userCertificateSelectionCallback, EncryptionPolicy encryptionPolicy);</span>
</pre>
</div>

</div> <!-- end type SslStream -->

</div> <!-- end namespace System.Net.Security -->
<!-- start namespace System.Net.Sockets --> <div> 
<h2>Namespace System.Net.Sockets</h2>
<!-- start type Socket --> <div>
<h3>Type Changed: System.Net.Sockets.Socket</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public void Bind (System.Net.EndPoint <span class='removed removed-inline '>local_end</span> <span class='added '>localEP</span>)
</div><div data-is-non-breaking="">	public byte[] GetSocketOption (SocketOptionLevel optionLevel, SocketOptionName optionName, int <span class='removed removed-inline '>length</span> <span class='added '>optionLength</span>)
</div><div data-is-non-breaking="">	public int IOControl (int <span class='removed removed-inline '>ioctl_code</span> <span class='added '>ioControlCode</span>, byte[] <span class='removed removed-inline '>in_value</span> <span class='added '>optionInValue</span>, byte[] <span class='removed removed-inline '>out_value</span> <span class='added '>optionOutValue</span>)
</div><div data-is-non-breaking="">	public bool Poll (int <span class='removed removed-inline '>time_us</span> <span class='added '>microSeconds</span>, SelectMode mode)
</div><div data-is-non-breaking="">	public int Receive (byte[] buffer, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>)
</div><div data-is-non-breaking="">	public int Receive (byte[] buffer, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>)
</div><div data-is-non-breaking="">	public int Receive (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>)
</div><div data-is-non-breaking="">	public int Receive (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>, out SocketError <span class='removed removed-inline '>error</span> <span class='added '>errorCode</span>)
</div><div data-is-non-breaking="">	public int ReceiveFrom (byte[] buffer, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>, ref System.Net.EndPoint remoteEP)
</div><div data-is-non-breaking="">	public int ReceiveFrom (byte[] buffer, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>, ref System.Net.EndPoint remoteEP)
</div><div data-is-non-breaking="">	public int ReceiveFrom (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>, ref System.Net.EndPoint remoteEP)
</div><div data-is-non-breaking="">	public int Send (byte[] buffer, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>)
</div><div data-is-non-breaking="">	public int Send (byte[] buffer, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>)
</div><div data-is-non-breaking="">	public int Send (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>)
</div><div data-is-non-breaking="">	public int Send (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>, out SocketError <span class='removed removed-inline '>error</span> <span class='added '>errorCode</span>)
</div><div data-is-non-breaking="">	public int SendTo (byte[] buffer, System.Net.EndPoint <span class='removed removed-inline '>remote_end</span> <span class='added '>remoteEP</span>)
</div><div data-is-non-breaking="">	public int SendTo (byte[] buffer, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>, System.Net.EndPoint <span class='removed removed-inline '>remote_end</span> <span class='added '>remoteEP</span>)
</div><div data-is-non-breaking="">	public int SendTo (byte[] buffer, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>, System.Net.EndPoint <span class='removed removed-inline '>remote_end</span> <span class='added '>remoteEP</span>)
</div><div data-is-non-breaking="">	public int SendTo (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline '>flags</span> <span class='added '>socketFlags</span>, System.Net.EndPoint <span class='removed removed-inline '>remote_end</span> <span class='added '>remoteEP</span>)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void CancelConnectAsync (SocketAsyncEventArgs e);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ConnectAsync (SocketType socketType, ProtocolType protocolType, SocketAsyncEventArgs e);</span>
</pre>
</div>

</div> <!-- end type Socket -->
<!-- start type SocketAsyncEventArgs --> <div>
<h3>Type Changed: System.Net.Sockets.SocketAsyncEventArgs</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public IPPacketInformation ReceiveMessageFromPacketInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SendPacketsElement[] SendPacketsElements { get; set; }</span>
</pre>
</div>

</div> <!-- end type SocketAsyncEventArgs -->
<!-- start type TcpClient --> <div>
<h3>Type Changed: System.Net.Sockets.TcpClient</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
</pre>
</div>

</div> <!-- end type TcpClient -->
<!-- start type UdpClient --> <div>
<h3>Type Changed: System.Net.Sockets.UdpClient</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
</pre>
</div>

</div> <!-- end type UdpClient -->

</div> <!-- end namespace System.Net.Sockets -->
<!-- start namespace System.Security.AccessControl --> <div> 
<h2>Namespace System.Security.AccessControl</h2>
<!-- start type SemaphoreAccessRule --> <div>
<h3>Type Changed: System.Security.AccessControl.SemaphoreAccessRule</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public SemaphoreAccessRule (System.Security.Principal.IdentityReference identity, SemaphoreRights <span class='removed removed-inline '>semaphoreRights</span> <span class='added '>eventRights</span>, AccessControlType type)
</div><div data-is-non-breaking="">	public SemaphoreAccessRule (string identity, SemaphoreRights <span class='removed removed-inline '>semaphoreRights</span> <span class='added '>eventRights</span>, AccessControlType type)
</div></pre>

</div> <!-- end type SemaphoreAccessRule -->
<!-- start type SemaphoreAuditRule --> <div>
<h3>Type Changed: System.Security.AccessControl.SemaphoreAuditRule</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public SemaphoreAuditRule (System.Security.Principal.IdentityReference identity, SemaphoreRights <span class='removed removed-inline '>semaphoreRights</span> <span class='added '>eventRights</span>, AuditFlags flags)
</div></pre>

</div> <!-- end type SemaphoreAuditRule -->

</div> <!-- end namespace System.Security.AccessControl -->
<!-- start namespace System.Security.Authentication.ExtendedProtection --> <div> 
<h2>Namespace System.Security.Authentication.ExtendedProtection</h2>
<!-- start type ServiceNameCollection --> <div>
<h3>Type Changed: System.Security.Authentication.ExtendedProtection.ServiceNameCollection</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (string searchServiceName);</span>
</pre>
</div>

</div> <!-- end type ServiceNameCollection -->
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
<!-- start namespace System.Security.Cryptography.X509Certificates --> <div> 
<h2>Namespace System.Security.Cryptography.X509Certificates</h2>
<!-- start type X509Chain --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509Chain</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeX509ChainHandle SafeHandle { get; }</span>
</pre>
</div>

</div> <!-- end type X509Chain -->
<!-- start type X509ChainStatusFlags --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509ChainStatusFlags</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ExplicitDistrust = 67108864,</span>
	<span class='added added-field ' data-is-non-breaking="">HasNotSupportedCriticalExtension = 134217728,</span>
	<span class='added added-field ' data-is-non-breaking="">HasWeakSignature = 1048576,</span>
</pre>
</div>

</div> <!-- end type X509ChainStatusFlags -->
<!-- start type X509KeyUsageExtension --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509KeyUsageExtension</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public override void CopyFrom (System.Security.Cryptography.AsnEncodedData <span class='removed removed-inline '>encodedData</span> <span class='added '>asnEncodedData</span>)
</div></pre>

</div> <!-- end type X509KeyUsageExtension -->
<!-- start type X509Store --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509Store</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.IDisposable</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
</pre>
</div>

</div> <!-- end type X509Store -->
<!-- start type X509SubjectKeyIdentifierExtension --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509SubjectKeyIdentifierExtension</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public override void CopyFrom (System.Security.Cryptography.AsnEncodedData <span class='removed removed-inline '>encodedData</span> <span class='added '>asnEncodedData</span>)
</div></pre>

</div> <!-- end type X509SubjectKeyIdentifierExtension -->

</div> <!-- end namespace System.Security.Cryptography.X509Certificates -->
<!-- start namespace System.Text.RegularExpressions --> <div> 
<h2>Namespace System.Text.RegularExpressions</h2>
<!-- start type Regex --> <div>
<h3>Type Changed: System.Text.RegularExpressions.Regex</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">protected System.Collections.IDictionary CapNames { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected System.Collections.IDictionary Caps { get; set; }</span>
</pre>
</div>

</div> <!-- end type Regex -->

</div> <!-- end namespace System.Text.RegularExpressions -->
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
<!-- start namespace System.IO.MemoryMappedFiles --> <div> 
<h2>Namespace System.IO.MemoryMappedFiles</h2>
<!-- start type MemoryMappedFile --> <div>
<h3>Type Changed: System.IO.MemoryMappedFiles.MemoryMappedFile</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MemoryMappedFile CreateFromFile (System.IO.FileStream fileStream, string mapName, long capacity, MemoryMappedFileAccess access, System.IO.HandleInheritability inheritability, bool leaveOpen);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MemoryMappedFile CreateNew (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, System.IO.HandleInheritability inheritability);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MemoryMappedFile CreateOrOpen (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, System.IO.HandleInheritability inheritability);</span>
</pre>
</div>

</div> <!-- end type MemoryMappedFile -->

</div> <!-- end namespace System.IO.MemoryMappedFiles -->
<!-- start namespace System.IO.Pipes --> <div> 
<h2>Namespace System.IO.Pipes</h2>
<!-- start type NamedPipeClientStream --> <div>
<h3>Type Changed: System.IO.Pipes.NamedPipeClientStream</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task ConnectAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task ConnectAsync (int timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task ConnectAsync (System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task ConnectAsync (int timeout, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~NamedPipeClientStream ();</span>
</pre>
</div>

</div> <!-- end type NamedPipeClientStream -->
<!-- start type NamedPipeServerStream --> <div>
<h3>Type Changed: System.IO.Pipes.NamedPipeServerStream</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WaitForConnectionAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WaitForConnectionAsync (System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type NamedPipeServerStream -->
<!-- start type PipeStream --> <div>
<h3>Type Changed: System.IO.Pipes.PipeStream</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void WaitForPipeDrain ();</span>
</pre>
</div>

</div> <!-- end type PipeStream -->
<div> <!-- start type PipeAccessRights -->
<h3>New Type System.IO.Pipes.PipeAccessRights</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PipeAccessRights {
	<span class='added added-field ' data-is-non-breaking="">AccessSystemSecurity = 16777216,</span>
	<span class='added added-field ' data-is-non-breaking="">ChangePermissions = 262144,</span>
	<span class='added added-field ' data-is-non-breaking="">CreateNewInstance = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Delete = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">FullControl = 2032031,</span>
	<span class='added added-field ' data-is-non-breaking="">Read = 131209,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadAttributes = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadData = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadExtendedAttributes = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadPermissions = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadWrite = 131483,</span>
	<span class='added added-field ' data-is-non-breaking="">Synchronize = 1048576,</span>
	<span class='added added-field ' data-is-non-breaking="">TakeOwnership = 524288,</span>
	<span class='added added-field ' data-is-non-breaking="">Write = 274,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteAttributes = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteData = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteExtendedAttributes = 16,</span>
}
</pre>
</div> <!-- end type PipeAccessRights -->
<div> <!-- start type PipeAccessRule -->
<h3>New Type System.IO.Pipes.PipeAccessRule</h3>
<pre class='added' data-is-non-breaking="">
public sealed class PipeAccessRule : System.Security.AccessControl.AccessRule {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PipeAccessRule (System.Security.Principal.IdentityReference identity, PipeAccessRights rights, System.Security.AccessControl.AccessControlType type);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PipeAccessRule (string identity, PipeAccessRights rights, System.Security.AccessControl.AccessControlType type);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public PipeAccessRights PipeAccessRights { get; }</span>
}
</pre>
</div> <!-- end type PipeAccessRule -->
<div> <!-- start type PipeAuditRule -->
<h3>New Type System.IO.Pipes.PipeAuditRule</h3>
<pre class='added' data-is-non-breaking="">
public sealed class PipeAuditRule : System.Security.AccessControl.AuditRule {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PipeAuditRule (System.Security.Principal.IdentityReference identity, PipeAccessRights rights, System.Security.AccessControl.AuditFlags flags);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PipeAuditRule (string identity, PipeAccessRights rights, System.Security.AccessControl.AuditFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public PipeAccessRights PipeAccessRights { get; }</span>
}
</pre>
</div> <!-- end type PipeAuditRule -->
<div> <!-- start type PipeSecurity -->
<h3>New Type System.IO.Pipes.PipeSecurity</h3>
<pre class='added' data-is-non-breaking="">
public class PipeSecurity : System.Security.AccessControl.NativeObjectSecurity {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PipeSecurity ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Type AccessRightType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type AccessRuleType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type AuditRuleType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.AccessControl.AccessRule AccessRuleFactory (System.Security.Principal.IdentityReference identityReference, int accessMask, bool isInherited, System.Security.AccessControl.InheritanceFlags inheritanceFlags, System.Security.AccessControl.PropagationFlags propagationFlags, System.Security.AccessControl.AccessControlType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddAccessRule (PipeAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddAuditRule (PipeAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.AccessControl.AuditRule AuditRuleFactory (System.Security.Principal.IdentityReference identityReference, int accessMask, bool isInherited, System.Security.AccessControl.InheritanceFlags inheritanceFlags, System.Security.AccessControl.PropagationFlags propagationFlags, System.Security.AccessControl.AuditFlags flags);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void Persist (System.Runtime.InteropServices.SafeHandle handle);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void Persist (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool RemoveAccessRule (PipeAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAccessRuleSpecific (PipeAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool RemoveAuditRule (PipeAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAuditRuleAll (PipeAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAuditRuleSpecific (PipeAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ResetAccessRule (PipeAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAccessRule (PipeAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAuditRule (PipeAuditRule rule);</span>
}
</pre>
</div> <!-- end type PipeSecurity -->
<div> <!-- start type PipeStreamImpersonationWorker -->
<h3>New Type System.IO.Pipes.PipeStreamImpersonationWorker</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PipeStreamImpersonationWorker : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PipeStreamImpersonationWorker (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke ();</span>
}
</pre>
</div> <!-- end type PipeStreamImpersonationWorker -->

</div> <!-- end namespace System.IO.Pipes -->
<!-- start namespace System.Linq --> <div> 
<h2>Namespace System.Linq</h2>
<!-- start type Enumerable --> <div>
<h3>Type Changed: System.Linq.Enumerable</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IEnumerable&lt;TSource&gt; Append&lt;TSource&gt; (System.Collections.Generic.IEnumerable&lt;TSource&gt; source, TSource element);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IEnumerable&lt;TSource&gt; Prepend&lt;TSource&gt; (System.Collections.Generic.IEnumerable&lt;TSource&gt; source, TSource element);</span>
</pre>
</div>

</div> <!-- end type Enumerable -->

</div> <!-- end namespace System.Linq -->
<!-- start namespace System.Linq.Expressions --> <div> 
<h2>Namespace System.Linq.Expressions</h2>
<!-- start type Expression`1 --> <div>
<h3>Type Changed: System.Linq.Expressions.Expression`1</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public TDelegate Compile (bool preferInterpretation);</span>
</pre>
</div>

</div> <!-- end type Expression`1 -->
<!-- start type LambdaExpression --> <div>
<h3>Type Changed: System.Linq.Expressions.LambdaExpression</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Delegate Compile (bool preferInterpretation);</span>
</pre>
</div>

</div> <!-- end type LambdaExpression -->

</div> <!-- end namespace System.Linq.Expressions -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type CngAlgorithm --> <div>
<h3>Type Changed: System.Security.Cryptography.CngAlgorithm</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDiffieHellman { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDsa { get; }</span>
</pre>
</div>

</div> <!-- end type CngAlgorithm -->
<!-- start type CngKey --> <div>
<h3>Type Changed: System.Security.Cryptography.CngKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CngAlgorithm Algorithm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngAlgorithmGroup AlgorithmGroup { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngExportPolicies ExportPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeNCryptKeyHandle Handle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsEphemeral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsMachineKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string KeyName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int KeySize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngKeyUsages KeyUsage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IntPtr ParentWindowHandle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngProvider Provider { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeNCryptProviderHandle ProviderHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngUIPolicy UIPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string UniqueName { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Create (CngAlgorithm algorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Create (CngAlgorithm algorithm, string keyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Create (CngAlgorithm algorithm, string keyName, CngKeyCreationParameters creationParameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Delete ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Exists (string keyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Exists (string keyName, CngProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Exists (string keyName, CngProvider provider, CngKeyOpenOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] Export (CngKeyBlobFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public CngProperty GetProperty (string name, CngPropertyOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool HasProperty (string name, CngPropertyOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Import (byte[] keyBlob, CngKeyBlobFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Import (byte[] keyBlob, CngKeyBlobFormat format, CngProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Open (string keyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Open (Microsoft.Win32.SafeHandles.SafeNCryptKeyHandle keyHandle, CngKeyHandleOpenOptions keyHandleOpenOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Open (string keyName, CngProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Open (string keyName, CngProvider provider, CngKeyOpenOptions openOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetProperty (CngProperty property);</span>
</pre>
</div>

</div> <!-- end type CngKey -->
<!-- start type CngKeyBlobFormat --> <div>
<h3>Type Changed: System.Security.Cryptography.CngKeyBlobFormat</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat EccFullPrivateBlob { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat EccFullPublicBlob { get; }</span>
</pre>
</div>

</div> <!-- end type CngKeyBlobFormat -->
<!-- start type ECDsa --> <div>
<h3>Type Changed: System.Security.Cryptography.ECDsa</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static ECDsa Create (ECCurve curve);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ECDsa Create (ECParameters parameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ECParameters ExportExplicitParameters (bool includePrivateParameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ECParameters ExportParameters (bool includePrivateParameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GenerateKey (ECCurve curve);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ImportParameters (ECParameters parameters);</span>
</pre>
</div>

</div> <!-- end type ECDsa -->
<!-- start type ECDsaCng --> <div>
<h3>Type Changed: System.Security.Cryptography.ECDsaCng</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public ECDsaCng (int keySize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ECDsaCng (CngKey key);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ECDsaCng (ECCurve curve);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CngKey Key { get; }</span>
</pre>
</div>

</div> <!-- end type ECDsaCng -->
<!-- start type RSACng --> <div>
<h3>Type Changed: System.Security.Cryptography.RSACng</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public RSACng (int keySize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RSACng (CngKey key);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CngKey Key { get; }</span>
</pre>
</div>

</div> <!-- end type RSACng -->
<div> <!-- start type ECCurve -->
<h3>New Type System.Security.Cryptography.ECCurve</h3>
<pre class='added' data-is-non-breaking="">
public struct ECCurve {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public byte[] A;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] B;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Cofactor;</span>
	<span class='added added-field ' data-is-non-breaking="">public ECCurve.ECCurveType CurveType;</span>
	<span class='added added-field ' data-is-non-breaking="">public ECPoint G;</span>
	<span class='added added-field ' data-is-non-breaking="">public HashAlgorithmName? Hash;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Order;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Polynomial;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Prime;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Seed;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsCharacteristic2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsExplicit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsNamed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsPrime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Oid Oid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static ECCurve CreateFromFriendlyName (string oidFriendlyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ECCurve CreateFromOid (Oid curveOid);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ECCurve CreateFromValue (string oidValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Validate ();</span>

	// inner types
	[Serializable]
	public enum ECCurveType {
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType Characteristic2;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType Implicit;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType Named;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType PrimeMontgomery;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType PrimeShortWeierstrass;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType PrimeTwistedEdwards;</span>
	}
	public static class NamedCurves {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP160r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP160t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP192r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP192t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP224r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP224t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP256r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP256t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP320r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP320t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP384r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP384t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP512r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP512t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve nistP256 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve nistP384 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve nistP521 { get; }</span>
	}
}
</pre>
</div> <!-- end type ECCurve -->
<div> <!-- start type ECParameters -->
<h3>New Type System.Security.Cryptography.ECParameters</h3>
<pre class='added' data-is-non-breaking="">
public struct ECParameters {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ECCurve Curve;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] D;</span>
	<span class='added added-field ' data-is-non-breaking="">public ECPoint Q;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Validate ();</span>
}
</pre>
</div> <!-- end type ECParameters -->
<div> <!-- start type ECPoint -->
<h3>New Type System.Security.Cryptography.ECPoint</h3>
<pre class='added' data-is-non-breaking="">
public struct ECPoint {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public byte[] X;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Y;</span>
}
</pre>
</div> <!-- end type ECPoint -->
<div> <!-- start type IncrementalHash -->
<h3>New Type System.Security.Cryptography.IncrementalHash</h3>
<pre class='added' data-is-non-breaking="">
public sealed class IncrementalHash : System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HashAlgorithmName AlgorithmName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AppendData (byte[] data);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AppendData (byte[] data, int offset, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IncrementalHash CreateHMAC (HashAlgorithmName hashAlgorithm, byte[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IncrementalHash CreateHash (HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] GetHashAndReset ();</span>
}
</pre>
</div> <!-- end type IncrementalHash -->

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
</script><h1 id='diff/xi/2.1/System.Data.html'>System.Data.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Microsoft.SqlServer.Server --> <div> 
<h2>Namespace Microsoft.SqlServer.Server</h2>
<!-- start type SqlDataRecord --> <div>
<h3>Type Changed: Microsoft.SqlServer.Server.SqlDataRecord</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SqlDataRecord ();</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlDataRecord (SqlMetaData[] metaData);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> int FieldCount { get; }
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> object this [int ordinal] { get; }
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> object this [string name] { get; }
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> bool GetBoolean (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> byte GetByte (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> long GetBytes (int ordinal, long fieldOffset, byte[] buffer, int bufferOffset, int length)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> char GetChar (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> long GetChars (int ordinal, long fieldOffset, char[] buffer, int bufferOffset, int length)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.Data.IDataReader GetData (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> string GetDataTypeName (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.DateTime GetDateTime (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.Decimal GetDecimal (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> double GetDouble (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.Type GetFieldType (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> float GetFloat (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.Guid GetGuid (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> short GetInt16 (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> int GetInt32 (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> long GetInt64 (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> string GetName (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> int GetOrdinal (string name)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> string GetString (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> object GetValue (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> int GetValues (object[] values)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> bool IsDBNull (int ordinal)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.DateTimeOffset GetDateTimeOffset (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlBinary GetSqlBinary (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlBoolean GetSqlBoolean (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlByte GetSqlByte (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlBytes GetSqlBytes (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlChars GetSqlChars (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlDateTime GetSqlDateTime (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlDecimal GetSqlDecimal (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlDouble GetSqlDouble (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Type GetSqlFieldType (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlGuid GetSqlGuid (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlInt16 GetSqlInt16 (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlInt32 GetSqlInt32 (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlInt64 GetSqlInt64 (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SqlMetaData GetSqlMetaData (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlMoney GetSqlMoney (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlSingle GetSqlSingle (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlString GetSqlString (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual object GetSqlValue (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int GetSqlValues (object[] values);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlXml GetSqlXml (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.TimeSpan GetTimeSpan (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetBoolean (int ordinal, bool value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetByte (int ordinal, byte value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetBytes (int ordinal, long fieldOffset, byte[] buffer, int bufferOffset, int length);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetChar (int ordinal, char value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetChars (int ordinal, long fieldOffset, char[] buffer, int bufferOffset, int length);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDBNull (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDateTime (int ordinal, System.DateTime value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDateTimeOffset (int ordinal, System.DateTimeOffset value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDecimal (int ordinal, System.Decimal value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDouble (int ordinal, double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetFloat (int ordinal, float value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetGuid (int ordinal, System.Guid value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetInt16 (int ordinal, short value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetInt32 (int ordinal, int value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetInt64 (int ordinal, long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlBinary (int ordinal, System.Data.SqlTypes.SqlBinary value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlBoolean (int ordinal, System.Data.SqlTypes.SqlBoolean value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlByte (int ordinal, System.Data.SqlTypes.SqlByte value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlBytes (int ordinal, System.Data.SqlTypes.SqlBytes value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlChars (int ordinal, System.Data.SqlTypes.SqlChars value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlDateTime (int ordinal, System.Data.SqlTypes.SqlDateTime value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlDecimal (int ordinal, System.Data.SqlTypes.SqlDecimal value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlDouble (int ordinal, System.Data.SqlTypes.SqlDouble value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlGuid (int ordinal, System.Data.SqlTypes.SqlGuid value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlInt16 (int ordinal, System.Data.SqlTypes.SqlInt16 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlInt32 (int ordinal, System.Data.SqlTypes.SqlInt32 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlInt64 (int ordinal, System.Data.SqlTypes.SqlInt64 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlMoney (int ordinal, System.Data.SqlTypes.SqlMoney value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlSingle (int ordinal, System.Data.SqlTypes.SqlSingle value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlString (int ordinal, System.Data.SqlTypes.SqlString value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlXml (int ordinal, System.Data.SqlTypes.SqlXml value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetString (int ordinal, string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTimeSpan (int ordinal, System.TimeSpan value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (int ordinal, object value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int SetValues (object[] values);</span>
</pre>
</div>

</div> <!-- end type SqlDataRecord -->
<!-- start type SqlMetaData --> <div>
<h3>Type Changed: Microsoft.SqlServer.Server.SqlMetaData</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, long maxLength, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, byte precision, byte scale, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, long maxLength, long locale, System.Data.SqlTypes.SqlCompareOptions compareOptions, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, string database, string owningSchema, string objectName, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, long maxLength, byte precision, byte scale, long localeId, System.Data.SqlTypes.SqlCompareOptions compareOptions, System.Type userDefinedType, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool IsUniqueKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Data.SqlClient.SortOrder SortOrder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int SortOrdinal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool UseServerDefault { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Data.SqlTypes.SqlXml Adjust (System.Data.SqlTypes.SqlXml value);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.DateTimeOffset Adjust (System.DateTimeOffset value);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.TimeSpan Adjust (System.TimeSpan value);</span>
</pre>
</div>

</div> <!-- end type SqlMetaData -->

</div> <!-- end namespace Microsoft.SqlServer.Server -->
<!-- start namespace System.Data.SqlClient --> <div> 
<h2>Namespace System.Data.SqlClient</h2>
<!-- start type SqlBulkCopy --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlBulkCopy</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool EnableStreaming { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void WriteToServer (System.Data.Common.DbDataReader reader);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.Common.DbDataReader reader);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.Common.DbDataReader reader, System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type SqlBulkCopy -->
<!-- start type SqlCommand --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlCommand</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;SqlDataReader&gt; ExecuteReaderAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;SqlDataReader&gt; ExecuteReaderAsync (System.Data.CommandBehavior behavior);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;SqlDataReader&gt; ExecuteReaderAsync (System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;SqlDataReader&gt; ExecuteReaderAsync (System.Data.CommandBehavior behavior, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Xml.XmlReader&gt; ExecuteXmlReaderAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Xml.XmlReader&gt; ExecuteXmlReaderAsync (System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type SqlCommand -->
<!-- start type SqlConnection --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlConnection</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Guid ClientConnectionId { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void ResetStatistics ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.IDictionary RetrieveStatistics ();</span>
</pre>
</div>

</div> <!-- end type SqlConnection -->
<!-- start type SqlDataReader --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlDataReader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override System.Threading.Tasks.Task&lt;T&gt; GetFieldValueAsync&lt;T&gt; (int i, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.IO.Stream GetStream (int i);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.IO.TextReader GetTextReader (int i);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Threading.Tasks.Task&lt;bool&gt; IsDBNullAsync (int i, System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type SqlDataReader -->
<!-- start type SqlException --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlException</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Guid ClientConnectionId { get; }</span>
</pre>
</div>

</div> <!-- end type SqlException -->
<!-- start type SqlParameter --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlParameter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string TypeName { get; set; }</span>
</pre>
</div>

</div> <!-- end type SqlParameter -->

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
</script><h1 id='diff/xi/2.1/System.ServiceModel.html'>System.ServiceModel.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.ServiceModel --> <div> 
<h2>Namespace System.ServiceModel</h2>
<!-- start type ActionNotSupportedException --> <div>
<h3>Type Changed: System.ServiceModel.ActionNotSupportedException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public ActionNotSupportedException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public ActionNotSupportedException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type ActionNotSupportedException -->
<!-- start type ChannelFactory --> <div>
<h3>Type Changed: System.ServiceModel.ChannelFactory</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	protected virtual void ApplyConfiguration (string <span class='removed removed-inline '>endpointConfig</span> <span class='added '>configurationName</span>)
</div><div data-is-non-breaking="">	protected void InitializeEndpoint (Channels.Binding binding, EndpointAddress <span class='removed removed-inline '>remoteAddress</span> <span class='added '>address</span>)
</div><div data-is-non-breaking="">	protected void InitializeEndpoint (string <span class='removed removed-inline '>endpointConfigurationName</span> <span class='added '>configurationName</span>, EndpointAddress remoteAddress)
</div></pre>

</div> <!-- end type ChannelFactory -->
<!-- start type ChannelFactory`1 --> <div>
<h3>Type Changed: System.ServiceModel.ChannelFactory`1</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected ChannelFactory`1 (System.Type <span class='removed removed-inline '>type</span> <span class='added '>channelType</span>)
</div></pre>

</div> <!-- end type ChannelFactory`1 -->
<!-- start type CommunicationException --> <div>
<h3>Type Changed: System.ServiceModel.CommunicationException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public CommunicationException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public CommunicationException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type CommunicationException -->
<!-- start type CommunicationObjectAbortedException --> <div>
<h3>Type Changed: System.ServiceModel.CommunicationObjectAbortedException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public CommunicationObjectAbortedException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public CommunicationObjectAbortedException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type CommunicationObjectAbortedException -->
<!-- start type CommunicationObjectFaultedException --> <div>
<h3>Type Changed: System.ServiceModel.CommunicationObjectFaultedException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public CommunicationObjectFaultedException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public CommunicationObjectFaultedException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type CommunicationObjectFaultedException -->
<!-- start type DnsEndpointIdentity --> <div>
<h3>Type Changed: System.ServiceModel.DnsEndpointIdentity</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public DnsEndpointIdentity (string <span class='removed removed-inline '>dns</span> <span class='added '>dnsName</span>)
</div></pre>

</div> <!-- end type DnsEndpointIdentity -->
<!-- start type DuplexClientBase`1 --> <div>
<h3>Type Changed: System.ServiceModel.DuplexClientBase`1</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected DuplexClientBase`1 (object <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (InstanceContext <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (object <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, Description.ServiceEndpoint endpoint)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (object <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, string <span class='removed removed-inline '>configurationName</span> <span class='added '>endpointConfigurationName</span>)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (InstanceContext <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, Description.ServiceEndpoint endpoint)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (InstanceContext <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, string <span class='removed removed-inline '>configurationName</span> <span class='added '>endpointConfigurationName</span>)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (object <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, Channels.Binding binding, EndpointAddress <span class='removed removed-inline '>address</span> <span class='added '>remoteAddress</span>)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (object <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, string bindingConfigurationName, EndpointAddress <span class='removed removed-inline '>address</span> <span class='added '>remoteAddress</span>)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (object <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, string endpointConfigurationName, string remoteAddress)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (InstanceContext <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, Channels.Binding binding, EndpointAddress <span class='removed removed-inline '>address</span> <span class='added '>remoteAddress</span>)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (InstanceContext <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, string <span class='removed removed-inline '>configurationName</span> <span class='added '>endpointConfigurationName</span>, EndpointAddress address)
</div><div data-is-non-breaking="">	protected DuplexClientBase`1 (InstanceContext <span class='removed removed-inline '>instance</span> <span class='added '>callbackInstance</span>, string endpointConfigurationName, string remoteAddress)
</div></pre>

</div> <!-- end type DuplexClientBase`1 -->
<!-- start type EndpointAddress --> <div>
<h3>Type Changed: System.ServiceModel.EndpointAddress</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public EndpointAddress (System.Uri uri, Channels.AddressHeader[] <span class='removed removed-inline '>headers</span> <span class='added '>addressHeaders</span>)
</div><div data-is-non-breaking="">	public EndpointAddress (System.Uri uri, EndpointIdentity identity, Channels.AddressHeader[] <span class='removed removed-inline '>headers</span> <span class='added '>addressHeaders</span>)
</div></pre>

</div> <!-- end type EndpointAddress -->
<!-- start type EndpointAddressBuilder --> <div>
<h3>Type Changed: System.ServiceModel.EndpointAddressBuilder</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public EndpointIdentity Identity { get; set; }</span>
</pre>
</div>

</div> <!-- end type EndpointAddressBuilder -->
<!-- start type EndpointNotFoundException --> <div>
<h3>Type Changed: System.ServiceModel.EndpointNotFoundException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public EndpointNotFoundException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public EndpointNotFoundException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type EndpointNotFoundException -->
<!-- start type FaultCode --> <div>
<h3>Type Changed: System.ServiceModel.FaultCode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public FaultCode (string name, FaultCode <span class='removed removed-inline '>subcode</span> <span class='added '>subCode</span>)
</div><div data-is-non-breaking="">	public FaultCode (string name, string ns, FaultCode <span class='removed removed-inline '>subcode</span> <span class='added '>subCode</span>)
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public FaultCode CreateReceiverFaultCode (FaultCode <span class='removed removed-inline '>subcode</span> <span class='added '>subCode</span>)
</div><div data-is-non-breaking="">	public FaultCode CreateSenderFaultCode (FaultCode <span class='removed removed-inline '>subcode</span> <span class='added '>subCode</span>)
</div></pre>

</div> <!-- end type FaultCode -->
<!-- start type FaultException --> <div>
<h3>Type Changed: System.ServiceModel.FaultException</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public FaultException CreateFault (Channels.MessageFault <span class='removed removed-inline '>fault</span> <span class='added '>messageFault</span>, System.Type[] <span class='removed removed-inline '>details</span> <span class='added '>faultDetailTypes</span>)
</div></pre>

</div> <!-- end type FaultException -->
<!-- start type InstanceContext --> <div>
<h3>Type Changed: System.ServiceModel.InstanceContext</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>System.ServiceModel.Channels.CommunicationObject</span>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public InstanceContext (object <span class='removed removed-inline '>dummy</span> <span class='added '>implementation</span>)
</div></pre>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICommunicationObject</span>
	<span class='added added-interface ' data-is-non-breaking="">System.ServiceModel.IExtensibleObject&lt;InstanceContext&gt;</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">protected override System.TimeSpan DefaultCloseTimeout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.TimeSpan DefaultOpenTimeout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Threading.SynchronizationContext SynchronizationContext { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public object GetServiceInstance (Channels.Message message);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnAbort ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override System.IAsyncResult OnBeginClose (System.TimeSpan timeout, System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override System.IAsyncResult OnBeginOpen (System.TimeSpan timeout, System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnClose (System.TimeSpan timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnClosed ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnEndClose (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnEndOpen (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnFaulted ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnOpen (System.TimeSpan timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnOpened ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnOpening ();</span>
</pre>
</div>

</div> <!-- end type InstanceContext -->
<!-- start type InvalidMessageContractException --> <div>
<h3>Type Changed: System.ServiceModel.InvalidMessageContractException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public InvalidMessageContractException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public InvalidMessageContractException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type InvalidMessageContractException -->
<!-- start type MessageHeaderException --> <div>
<h3>Type Changed: System.ServiceModel.MessageHeaderException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public MessageHeaderException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public MessageHeaderException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type MessageHeaderException -->
<!-- start type MessageHeader`1 --> <div>
<h3>Type Changed: System.ServiceModel.MessageHeader`1</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public MessageHeader`1 (T content, bool <span class='removed removed-inline '>must_understand</span> <span class='added '>mustUnderstand</span>, string actor, bool relay)
</div></pre>

</div> <!-- end type MessageHeader`1 -->
<!-- start type MessageSecurityOverTcp --> <div>
<h3>Type Changed: System.ServiceModel.MessageSecurityOverTcp</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MessageSecurityOverTcp ();</span>
</pre>
</div>

</div> <!-- end type MessageSecurityOverTcp -->
<!-- start type ProtocolException --> <div>
<h3>Type Changed: System.ServiceModel.ProtocolException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public ProtocolException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public ProtocolException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type ProtocolException -->
<!-- start type QuotaExceededException --> <div>
<h3>Type Changed: System.ServiceModel.QuotaExceededException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public QuotaExceededException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public QuotaExceededException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type QuotaExceededException -->
<!-- start type ServerTooBusyException --> <div>
<h3>Type Changed: System.ServiceModel.ServerTooBusyException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public ServerTooBusyException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public ServerTooBusyException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type ServerTooBusyException -->
<!-- start type ServiceActivationException --> <div>
<h3>Type Changed: System.ServiceModel.ServiceActivationException</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public ServiceActivationException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public ServiceActivationException (string <span class='removed removed-inline '>msg</span> <span class='added '>message</span>, System.Exception <span class='removed removed-inline '>inner</span> <span class='added '>innerException</span>)
</div></pre>

</div> <!-- end type ServiceActivationException -->
<!-- start type SpnEndpointIdentity --> <div>
<h3>Type Changed: System.ServiceModel.SpnEndpointIdentity</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public SpnEndpointIdentity (string <span class='removed removed-inline '>spn</span> <span class='added '>spnName</span>)
</div></pre>

</div> <!-- end type SpnEndpointIdentity -->
<!-- start type TcpTransportSecurity --> <div>
<h3>Type Changed: System.ServiceModel.TcpTransportSecurity</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.SslProtocols SslProtocols { get; set; }</span>
</pre>
</div>

</div> <!-- end type TcpTransportSecurity -->
<!-- start type UpnEndpointIdentity --> <div>
<h3>Type Changed: System.ServiceModel.UpnEndpointIdentity</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public UpnEndpointIdentity (string <span class='removed removed-inline '>upn</span> <span class='added '>upnName</span>)
</div></pre>

</div> <!-- end type UpnEndpointIdentity -->

</div> <!-- end namespace System.ServiceModel -->
<!-- start namespace System.ServiceModel.Channels --> <div> 
<h2>Namespace System.ServiceModel.Channels</h2>
<!-- start type AddressHeader --> <div>
<h3>Type Changed: System.ServiceModel.Channels.AddressHeader</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public AddressHeader CreateAddressHeader (object value, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>formatter</span> <span class='added '>serializer</span>)
</div><div data-is-non-breaking="">	public AddressHeader CreateAddressHeader (string name, string ns, object value, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>formatter</span> <span class='added '>serializer</span>)
</div><div data-is-non-breaking="">	public T GetValue&lt;T&gt; (System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>formatter</span> <span class='added '>serializer</span>)
</div></pre>

</div> <!-- end type AddressHeader -->
<!-- start type AddressHeaderCollection --> <div>
<h3>Type Changed: System.ServiceModel.Channels.AddressHeaderCollection</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public AddressHeaderCollection (System.Collections.Generic.IEnumerable&lt;AddressHeader&gt; <span class='removed removed-inline '>headers</span> <span class='added '>addressHeaders</span>)
</div></pre>

</div> <!-- end type AddressHeaderCollection -->
<!-- start type BindingContext --> <div>
<h3>Type Changed: System.ServiceModel.Channels.BindingContext</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public BindingContext (CustomBinding binding, BindingParameterCollection <span class='removed removed-inline '>parms</span> <span class='added '>parameters</span>)
</div></pre>

</div> <!-- end type BindingContext -->
<!-- start type BindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.BindingElement</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected BindingElement (BindingElement <span class='removed removed-inline '>other</span> <span class='added '>elementToBeCloned</span>)
</div></pre>

</div> <!-- end type BindingElement -->
<!-- start type BindingElementCollection --> <div>
<h3>Type Changed: System.ServiceModel.Channels.BindingElementCollection</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public BindingElementCollection (System.Collections.Generic.IEnumerable&lt;BindingElement&gt; <span class='removed removed-inline '>bindings</span> <span class='added '>elements</span>)
</div><div data-is-non-breaking="">	public BindingElementCollection (BindingElement[] <span class='removed removed-inline '>bindings</span> <span class='added '>elements</span>)
</div></pre>

</div> <!-- end type BindingElementCollection -->
<!-- start type ChannelBase --> <div>
<h3>Type Changed: System.ServiceModel.Channels.ChannelBase</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected ChannelBase (ChannelManagerBase <span class='removed removed-inline '>manager</span> <span class='added '>channelManager</span>)
</div></pre>

</div> <!-- end type ChannelBase -->
<!-- start type ChannelFactoryBase`1 --> <div>
<h3>Type Changed: System.ServiceModel.Channels.ChannelFactoryBase`1</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual final TChannel CreateChannel (System.ServiceModel.EndpointAddress <span class='removed removed-inline '>remoteAddress</span> <span class='added '>address</span>)
</div><div data-is-non-breaking="">	public virtual final TChannel CreateChannel (System.ServiceModel.EndpointAddress <span class='removed removed-inline '>remoteAddress</span> <span class='added '>address</span>, System.Uri via)
</div><div data-is-non-breaking="">	protected abstract TChannel OnCreateChannel (System.ServiceModel.EndpointAddress <span class='removed removed-inline '>remoteAddress</span> <span class='added '>address</span>, System.Uri via)
</div></pre>

</div> <!-- end type ChannelFactoryBase`1 -->
<!-- start type CustomBinding --> <div>
<h3>Type Changed: System.ServiceModel.Channels.CustomBinding</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public CustomBinding (System.Collections.Generic.IEnumerable&lt;BindingElement&gt; <span class='removed removed-inline '>bindingElements</span> <span class='added '>bindingElementsInTopDownChannelStackOrder</span>)
</div><div data-is-non-breaking="">	public CustomBinding (BindingElement[] <span class='removed removed-inline '>binding</span> <span class='added '>bindingElementsInTopDownChannelStackOrder</span>)
</div><div data-is-non-breaking="">	public CustomBinding (string name, string ns, BindingElement[] <span class='removed removed-inline '>binding</span> <span class='added '>bindingElementsInTopDownChannelStackOrder</span>)
</div></pre>

</div> <!-- end type CustomBinding -->
<!-- start type FaultConverter --> <div>
<h3>Type Changed: System.ServiceModel.Channels.FaultConverter</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	protected abstract bool OnTryCreateException (Message message, MessageFault fault, out System.Exception <span class='removed removed-inline '>error</span> <span class='added '>exception</span>)
</div><div data-is-non-breaking="">	protected abstract bool OnTryCreateFaultMessage (System.Exception <span class='removed removed-inline '>error</span> <span class='added '>exception</span>, out Message message)
</div><div data-is-non-breaking="">	public bool TryCreateException (Message message, MessageFault fault, out System.Exception <span class='removed removed-inline '>error</span> <span class='added '>exception</span>)
</div><div data-is-non-breaking="">	public bool TryCreateFaultMessage (System.Exception <span class='removed removed-inline '>error</span> <span class='added '>exception</span>, out Message message)
</div></pre>

</div> <!-- end type FaultConverter -->
<!-- start type HttpTransportBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.HttpTransportBindingElement</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected HttpTransportBindingElement (HttpTransportBindingElement <span class='removed removed-inline '>other</span> <span class='added '>elementToBeCloned</span>)
</div></pre>

</div> <!-- end type HttpTransportBindingElement -->
<!-- start type HttpsTransportBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.HttpsTransportBindingElement</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected HttpsTransportBindingElement (HttpsTransportBindingElement <span class='removed removed-inline '>other</span> <span class='added '>elementToBeCloned</span>)
</div></pre>

</div> <!-- end type HttpsTransportBindingElement -->
<!-- start type Message --> <div>
<h3>Type Changed: System.ServiceModel.Channels.Message</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public Message CreateMessage (MessageVersion version, string action, object body, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>xmlFormatter</span> <span class='added '>serializer</span>)
</div><div data-is-non-breaking="">	public T GetBody&lt;T&gt; (System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>xmlFormatter</span> <span class='added '>serializer</span>)
</div></pre>

</div> <!-- end type Message -->
<!-- start type MessageEncodingBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.MessageEncodingBindingElement</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public MessageEncodingBindingElement (MessageEncodingBindingElement <span class='removed removed-inline '>source</span> <span class='added '>elementToBeCloned</span>)
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public override T GetProperty&lt;T&gt; (BindingContext <span class='removed removed-inline '>ctx</span> <span class='added '>context</span>)
</div></pre>

</div> <!-- end type MessageEncodingBindingElement -->
<!-- start type MessageFault --> <div>
<h3>Type Changed: System.ServiceModel.Channels.MessageFault</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public T GetDetail&lt;T&gt; (System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>formatter</span> <span class='added '>serializer</span>)
</div></pre>

</div> <!-- end type MessageFault -->
<!-- start type MessageHeader --> <div>
<h3>Type Changed: System.ServiceModel.Channels.MessageHeader</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public MessageHeader CreateHeader (string name, string ns, object value, bool <span class='removed removed-inline '>must_understand</span> <span class='added '>mustUnderstand</span>)
</div><div data-is-non-breaking="">	public MessageHeader CreateHeader (string name, string ns, object value, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>formatter</span> <span class='added '>serializer</span>)
</div><div data-is-non-breaking="">	public MessageHeader CreateHeader (string name, string ns, object value, bool <span class='removed removed-inline '>must_understand</span> <span class='added '>mustUnderstand</span>, string actor)
</div><div data-is-non-breaking="">	public MessageHeader CreateHeader (string name, string ns, object value, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>formatter</span> <span class='added '>serializer</span>, bool <span class='removed removed-inline '>must_understand</span> <span class='added '>mustUnderstand</span>)
</div><div data-is-non-breaking="">	public MessageHeader CreateHeader (string name, string ns, object value, bool <span class='removed removed-inline '>must_understand</span> <span class='added '>mustUnderstand</span>, string actor, bool relay)
</div><div data-is-non-breaking="">	public MessageHeader CreateHeader (string name, string ns, object value, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>formatter</span> <span class='added '>serializer</span>, bool <span class='removed removed-inline '>must_understand</span> <span class='added '>mustUnderstand</span>, string actor)
</div><div data-is-non-breaking="">	public MessageHeader CreateHeader (string name, string ns, object value, System.Runtime.Serialization.XmlObjectSerializer <span class='removed removed-inline '>formatter</span> <span class='added '>serializer</span>, bool <span class='removed removed-inline '>must_understand</span> <span class='added '>mustUnderstand</span>, string actor, bool relay)
</div><div data-is-non-breaking="">	public virtual bool IsMessageVersionSupported (MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>)
</div><div data-is-non-breaking="">	protected abstract void OnWriteHeaderContents (System.Xml.XmlDictionaryWriter writer, MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>)
</div><div data-is-non-breaking="">	protected virtual void OnWriteStartHeader (System.Xml.XmlDictionaryWriter writer, MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>)
</div><div data-is-non-breaking="">	public void WriteHeader (System.Xml.XmlDictionaryWriter writer, MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>)
</div><div data-is-non-breaking="">	public void WriteHeader (System.Xml.XmlWriter writer, MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>)
</div><div data-is-non-breaking="">	protected void WriteHeaderAttributes (System.Xml.XmlDictionaryWriter writer, MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>)
</div><div data-is-non-breaking="">	public void WriteHeaderContents (System.Xml.XmlDictionaryWriter writer, MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>)
</div><div data-is-non-breaking="">	public void WriteStartHeader (System.Xml.XmlDictionaryWriter writer, MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>)
</div></pre>

</div> <!-- end type MessageHeader -->
<!-- start type MessageHeaders --> <div>
<h3>Type Changed: System.ServiceModel.Channels.MessageHeaders</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public void CopyHeaderFrom (Message <span class='removed removed-inline '>m</span> <span class='added '>message</span>, int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>)
</div><div data-is-non-breaking="">	public void CopyHeaderFrom (MessageHeaders <span class='removed removed-inline '>headers</span> <span class='added '>collection</span>, int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>)
</div><div data-is-non-breaking="">	public void CopyHeadersFrom (Message <span class='removed removed-inline '>m</span> <span class='added '>message</span>)
</div><div data-is-non-breaking="">	public void CopyHeadersFrom (MessageHeaders <span class='removed removed-inline '>headers</span> <span class='added '>collection</span>)
</div><div data-is-non-breaking="">	public void CopyTo (MessageHeaderInfo[] <span class='removed removed-inline '>dst</span> <span class='added '>array</span>, int index)
</div><div data-is-non-breaking="">	public System.Xml.XmlDictionaryReader GetReaderAtHeader (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>)
</div><div data-is-non-breaking="">	public void Insert (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>, MessageHeader header)
</div><div data-is-non-breaking="">	public void RemoveAt (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>)
</div><div data-is-non-breaking="">	public void WriteHeader (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>, System.Xml.XmlDictionaryWriter writer)
</div><div data-is-non-breaking="">	public void WriteHeader (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>, System.Xml.XmlWriter writer)
</div><div data-is-non-breaking="">	public void WriteHeaderContents (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>, System.Xml.XmlDictionaryWriter writer)
</div><div data-is-non-breaking="">	public void WriteHeaderContents (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>, System.Xml.XmlWriter writer)
</div><div data-is-non-breaking="">	public void WriteStartHeader (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>, System.Xml.XmlDictionaryWriter writer)
</div><div data-is-non-breaking="">	public void WriteStartHeader (int <span class='removed removed-inline '>index</span> <span class='added '>headerIndex</span>, System.Xml.XmlWriter writer)
</div></pre>

</div> <!-- end type MessageHeaders -->
<!-- start type MessageVersion --> <div>
<h3>Type Changed: System.ServiceModel.Channels.MessageVersion</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public MessageVersion CreateVersion (System.ServiceModel.EnvelopeVersion <span class='removed removed-inline '>envelope_version</span> <span class='added '>envelopeVersion</span>)
</div><div data-is-non-breaking="">	public MessageVersion CreateVersion (System.ServiceModel.EnvelopeVersion <span class='removed removed-inline '>envelope_version</span> <span class='added '>envelopeVersion</span>, AddressingVersion <span class='removed removed-inline '>addressing_version</span> <span class='added '>addressingVersion</span>)
</div><div data-is-non-breaking="">	public override bool Equals (object <span class='removed removed-inline '>value</span> <span class='added '>obj</span>)
</div></pre>

</div> <!-- end type MessageVersion -->
<!-- start type SecurityBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.SecurityBindingElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.Tokens.SupportingTokenParameters EndpointSupportingTokenParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.MessageSecurityVersion MessageSecurityVersion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SecurityHeaderLayout SecurityHeaderLayout { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SecurityBindingElement CreateSecureConversationBindingElement (SecurityBindingElement bootstrapSecurity);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecurityBindingElement CreateSecureConversationBindingElement (SecurityBindingElement bootstrapSecurity, bool requireCancellation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecurityBindingElement CreateSecureConversationBindingElement (SecurityBindingElement bootstrapSecurity, bool requireCancellation, System.ServiceModel.Security.ChannelProtectionRequirements bootstrapProtectionRequirements);</span>
</pre>
</div>

</div> <!-- end type SecurityBindingElement -->
<!-- start type SslStreamSecurityBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.SslStreamSecurityBindingElement</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.SslProtocols SslProtocols { get; set; }</span>
</pre>
</div>

</div> <!-- end type SslStreamSecurityBindingElement -->
<!-- start type TcpTransportBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.TcpTransportBindingElement</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected TcpTransportBindingElement (TcpTransportBindingElement <span class='removed removed-inline '>other</span> <span class='added '>elementToBeCloned</span>)
</div></pre>

</div> <!-- end type TcpTransportBindingElement -->
<!-- start type TransportBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.TransportBindingElement</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected TransportBindingElement (TransportBindingElement <span class='removed removed-inline '>other</span> <span class='added '>elementToBeCloned</span>)
</div></pre>

</div> <!-- end type TransportBindingElement -->

</div> <!-- end namespace System.ServiceModel.Channels -->
<!-- start namespace System.ServiceModel.Description --> <div> 
<h2>Namespace System.ServiceModel.Description</h2>
<!-- start type ClientCredentials --> <div>
<h3>Type Changed: System.ServiceModel.Description.ClientCredentials</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	protected ClientCredentials (ClientCredentials <span class='removed removed-inline '>source</span> <span class='added '>other</span>)
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.X509CertificateInitiatorClientCredential ClientCertificate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.HttpDigestClientCredential HttpDigest { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.X509CertificateRecipientClientCredential ServiceCertificate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.WindowsClientCredential Windows { get; }</span>
</pre>
</div>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual void ApplyClientBehavior (ServiceEndpoint <span class='removed removed-inline '>endpoint</span> <span class='added '>serviceEndpoint</span>, System.ServiceModel.Dispatcher.ClientRuntime behavior)
</div></pre>

</div> <!-- end type ClientCredentials -->
<!-- start type IContractBehavior --> <div>
<h3>Type Changed: System.ServiceModel.Description.IContractBehavior</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public abstract void AddBindingParameters (ContractDescription <span class='removed removed-inline '>description</span> <span class='added '>contractDescription</span>, ServiceEndpoint endpoint, System.ServiceModel.Channels.BindingParameterCollection <span class='removed removed-inline '>parameters</span> <span class='added '>bindingParameters</span>)
</div><div data-is-non-breaking="">	public abstract void ApplyClientBehavior (ContractDescription <span class='removed removed-inline '>description</span> <span class='added '>contractDescription</span>, ServiceEndpoint endpoint, System.ServiceModel.Dispatcher.ClientRuntime <span class='removed removed-inline '>proxy</span> <span class='added '>clientRuntime</span>)
</div><div data-is-non-breaking="">	public abstract void ApplyDispatchBehavior (ContractDescription <span class='removed removed-inline '>description</span> <span class='added '>contractDescription</span>, ServiceEndpoint endpoint, System.ServiceModel.Dispatcher.DispatchRuntime <span class='removed removed-inline '>dispatch</span> <span class='added '>dispatchRuntime</span>)
</div><div data-is-non-breaking="">	public abstract void Validate (ContractDescription <span class='removed removed-inline '>description</span> <span class='added '>contractDescription</span>, ServiceEndpoint endpoint)
</div></pre>

</div> <!-- end type IContractBehavior -->
<!-- start type IEndpointBehavior --> <div>
<h3>Type Changed: System.ServiceModel.Description.IEndpointBehavior</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public abstract void AddBindingParameters (ServiceEndpoint endpoint, System.ServiceModel.Channels.BindingParameterCollection <span class='removed removed-inline '>parameters</span> <span class='added '>bindingParameters</span>)
</div><div data-is-non-breaking="">	public abstract void ApplyClientBehavior (ServiceEndpoint <span class='removed removed-inline '>serviceEndpoint</span> <span class='added '>endpoint</span>, System.ServiceModel.Dispatcher.ClientRuntime <span class='removed removed-inline '>behavior</span> <span class='added '>clientRuntime</span>)
</div><div data-is-non-breaking="">	public abstract void ApplyDispatchBehavior (ServiceEndpoint <span class='removed removed-inline '>serviceEndpoint</span> <span class='added '>endpoint</span>, System.ServiceModel.Dispatcher.EndpointDispatcher <span class='removed removed-inline '>dispatcher</span> <span class='added '>endpointDispatcher</span>)
</div><div data-is-non-breaking="">	public abstract void Validate (ServiceEndpoint <span class='removed removed-inline '>serviceEndpoint</span> <span class='added '>endpoint</span>)
</div></pre>

</div> <!-- end type IEndpointBehavior -->
<!-- start type IOperationBehavior --> <div>
<h3>Type Changed: System.ServiceModel.Description.IOperationBehavior</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public abstract void AddBindingParameters (OperationDescription <span class='removed removed-inline '>description</span> <span class='added '>operationDescription</span>, System.ServiceModel.Channels.BindingParameterCollection <span class='removed removed-inline '>parameters</span> <span class='added '>bindingParameters</span>)
</div><div data-is-non-breaking="">	public abstract void ApplyClientBehavior (OperationDescription <span class='removed removed-inline '>description</span> <span class='added '>operationDescription</span>, System.ServiceModel.Dispatcher.ClientOperation <span class='removed removed-inline '>proxy</span> <span class='added '>clientOperation</span>)
</div><div data-is-non-breaking="">	public abstract void ApplyDispatchBehavior (OperationDescription <span class='removed removed-inline '>description</span> <span class='added '>operationDescription</span>, System.ServiceModel.Dispatcher.DispatchOperation <span class='removed removed-inline '>dispatch</span> <span class='added '>dispatchOperation</span>)
</div><div data-is-non-breaking="">	public abstract void Validate (OperationDescription <span class='removed removed-inline '>description</span> <span class='added '>operationDescription</span>)
</div></pre>

</div> <!-- end type IOperationBehavior -->

</div> <!-- end namespace System.ServiceModel.Description -->
<!-- start namespace System.ServiceModel.Dispatcher --> <div> 
<h2>Namespace System.ServiceModel.Dispatcher</h2>
<!-- start type IClientMessageFormatter --> <div>
<h3>Type Changed: System.ServiceModel.Dispatcher.IClientMessageFormatter</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public abstract object DeserializeReply (System.ServiceModel.Channels.Message message, object[] <span class='removed removed-inline '>paremeters</span> <span class='added '>parameters</span>)
</div><div data-is-non-breaking="">	public abstract System.ServiceModel.Channels.Message SerializeRequest (System.ServiceModel.Channels.MessageVersion <span class='removed removed-inline '>version</span> <span class='added '>messageVersion</span>, object[] <span class='removed removed-inline '>inputs</span> <span class='added '>parameters</span>)
</div></pre>

</div> <!-- end type IClientMessageFormatter -->
<!-- start type IClientMessageInspector --> <div>
<h3>Type Changed: System.ServiceModel.Dispatcher.IClientMessageInspector</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public abstract void AfterReceiveReply (ref System.ServiceModel.Channels.Message <span class='removed removed-inline '>message</span> <span class='added '>reply</span>, object correlationState)
</div><div data-is-non-breaking="">	public abstract object BeforeSendRequest (ref System.ServiceModel.Channels.Message <span class='removed removed-inline '>message</span> <span class='added '>request</span>, System.ServiceModel.IClientChannel channel)
</div></pre>

</div> <!-- end type IClientMessageInspector -->

</div> <!-- end namespace System.ServiceModel.Dispatcher -->
<!-- start namespace System.ServiceModel.Security --> <div> 
<h2>Namespace System.ServiceModel.Security</h2>
<div> <!-- start type ChannelProtectionRequirements -->
<h3>New Type System.ServiceModel.Security.ChannelProtectionRequirements</h3>
<pre class='added' data-is-non-breaking="">
public class ChannelProtectionRequirements {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ChannelProtectionRequirements ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ChannelProtectionRequirements (ChannelProtectionRequirements other);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public ScopedMessagePartSpecification IncomingEncryptionParts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ScopedMessagePartSpecification IncomingSignatureParts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ScopedMessagePartSpecification OutgoingEncryptionParts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ScopedMessagePartSpecification OutgoingSignatureParts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Add (ChannelProtectionRequirements protectionRequirements);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Add (ChannelProtectionRequirements protectionRequirements, bool channelScopeOnly);</span>
	<span class='added added-method ' data-is-non-breaking="">public ChannelProtectionRequirements CreateInverse ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void MakeReadOnly ();</span>
}
</pre>
</div> <!-- end type ChannelProtectionRequirements -->
<div> <!-- start type MessagePartSpecification -->
<h3>New Type System.ServiceModel.Security.MessagePartSpecification</h3>
<pre class='added' data-is-non-breaking="">
public class MessagePartSpecification {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MessagePartSpecification ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MessagePartSpecification (bool isBodyIncluded);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MessagePartSpecification (System.Xml.XmlQualifiedName[] headerTypes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MessagePartSpecification (bool isBodyIncluded, System.Xml.XmlQualifiedName[] headerTypes);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.ICollection&lt;System.Xml.XmlQualifiedName&gt; HeaderTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsBodyIncluded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessagePartSpecification NoParts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Clear ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void MakeReadOnly ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Union (MessagePartSpecification other);</span>
}
</pre>
</div> <!-- end type MessagePartSpecification -->
<div> <!-- start type ScopedMessagePartSpecification -->
<h3>New Type System.ServiceModel.Security.ScopedMessagePartSpecification</h3>
<pre class='added' data-is-non-breaking="">
public class ScopedMessagePartSpecification {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ScopedMessagePartSpecification ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ScopedMessagePartSpecification (ScopedMessagePartSpecification other);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.ICollection&lt;string&gt; Actions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MessagePartSpecification ChannelParts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsReadOnly { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AddParts (MessagePartSpecification parts);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddParts (MessagePartSpecification parts, string action);</span>
	<span class='added added-method ' data-is-non-breaking="">public void MakeReadOnly ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool TryGetParts (string action, out MessagePartSpecification parts);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool TryGetParts (string action, bool excludeChannelScope, out MessagePartSpecification parts);</span>
}
</pre>
</div> <!-- end type ScopedMessagePartSpecification -->
<div> <!-- start type X509CertificateInitiatorClientCredential -->
<h3>New Type System.ServiceModel.Security.X509CertificateInitiatorClientCredential</h3>
<pre class='added' data-is-non-breaking="">
public sealed class X509CertificateInitiatorClientCredential {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509Certificate2 Certificate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void SetCertificate (string subjectName, System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCertificate (System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName, System.Security.Cryptography.X509Certificates.X509FindType findType, object findValue);</span>
}
</pre>
</div> <!-- end type X509CertificateInitiatorClientCredential -->
<div> <!-- start type X509CertificateRecipientClientCredential -->
<h3>New Type System.ServiceModel.Security.X509CertificateRecipientClientCredential</h3>
<pre class='added' data-is-non-breaking="">
public sealed class X509CertificateRecipientClientCredential {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public X509ServiceCertificateAuthentication Authentication { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509Certificate2 DefaultCertificate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.Dictionary&lt;System.Uri,System.Security.Cryptography.X509Certificates.X509Certificate2&gt; ScopedCertificates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public X509ServiceCertificateAuthentication SslCertificateAuthentication { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void SetDefaultCertificate (string subjectName, System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetDefaultCertificate (System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName, System.Security.Cryptography.X509Certificates.X509FindType findType, object findValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetScopedCertificate (string subjectName, System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName, System.Uri targetService);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetScopedCertificate (System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName, System.Security.Cryptography.X509Certificates.X509FindType findType, object findValue, System.Uri targetService);</span>
}
</pre>
</div> <!-- end type X509CertificateRecipientClientCredential -->
<div> <!-- start type X509ServiceCertificateAuthentication -->
<h3>New Type System.ServiceModel.Security.X509ServiceCertificateAuthentication</h3>
<pre class='added' data-is-non-breaking="">
public class X509ServiceCertificateAuthentication {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public X509ServiceCertificateAuthentication ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public X509CertificateValidationMode CertificateValidationMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.IdentityModel.Selectors.X509CertificateValidator CustomCertificateValidator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509RevocationMode RevocationMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.StoreLocation TrustedStoreLocation { get; set; }</span>
}
</pre>
</div> <!-- end type X509ServiceCertificateAuthentication -->

</div> <!-- end namespace System.ServiceModel.Security -->
<!-- start namespace System.ServiceModel.Security.Tokens --> <div> 
<h2>Namespace System.ServiceModel.Security.Tokens</h2>
<!-- start type SecureConversationSecurityTokenParameters --> <div>
<h3>Type Changed: System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public SecureConversationSecurityTokenParameters (System.ServiceModel.Channels.SecurityBindingElement <span class='removed removed-inline '>element</span> <span class='added '>bootstrapSecurityBindingElement</span>)
</div><div data-is-non-breaking="">	public SecureConversationSecurityTokenParameters (System.ServiceModel.Channels.SecurityBindingElement <span class='removed removed-inline '>element</span> <span class='added '>bootstrapSecurityBindingElement</span>, bool requireCancellation)
</div></pre>

</div> <!-- end type SecureConversationSecurityTokenParameters -->

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
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"9.8.0"</span> <span class='added '>"9.10.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace MonoTouch -->
<!-- start namespace MonoTouch.AudioToolbox --> <div> 
<h2>Namespace MonoTouch.AudioToolbox</h2>
<!-- start type MusicSequence --> <div>
<h3>Type Changed: MonoTouch.AudioToolbox.MusicSequence</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public MusicTrack GetTempoTrack ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetUserCallback (MusicSequenceUserCallback callback);</span>
</pre>
</div>

</div> <!-- end type MusicSequence -->
<div> <!-- start type MusicSequenceUserCallback -->
<h3>New Type MonoTouch.AudioToolbox.MusicSequenceUserCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MusicSequenceUserCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MusicSequenceUserCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MusicTrack track, double inEventTime, MusicEventUserData inEventData, double inStartSliceBeat, double inEndSliceBeat, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (MusicTrack track, double inEventTime, MusicEventUserData inEventData, double inStartSliceBeat, double inEndSliceBeat);</span>
}
</pre>
</div> <!-- end type MusicSequenceUserCallback -->

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
<!-- start type AUParameter --> <div>
<h3>Type Changed: MonoTouch.AudioUnit.AUParameter</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void SetValue (float value, IntPtr originator);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void SetValue (float value, IntPtr originator, ulong hostTime);</span>
</div></pre>
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
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void RemoveParameterObserver (IntPtr token);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the CreateTokenByAddingParameterObserver instead")]
	public virtual IntPtr TokenByAddingParameterObserver (AUParameterObserver observer);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterObserver (AUParameterObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterRecordingObserver (AUParameterRecordingObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveParameterObserver (AUParameterObserverToken token);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use the CreateTokenByAddingParameterRecordingObserver instead")]
	public virtual IntPtr TokenByAddingParameterRecordingObserver (AUParameterRecordingObserver observer);</span>
</pre>
</div>

</div> <!-- end type AUParameterNode -->
<div> <!-- start type AUHostTransportStateBlock -->
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
<!-- start namespace MonoTouch.CoreBluetooth --> <div> 
<h2>Namespace MonoTouch.CoreBluetooth</h2>
<div> <!-- start type AdvertisementData -->
<h3>New Type MonoTouch.CoreBluetooth.AdvertisementData</h3>
<pre class='added' data-is-non-breaking="">
public class AdvertisementData : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisementData ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisementData (MonoTouch.Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? IsConnectable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string LocalName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MonoTouch.Foundation.NSData ManufacturerData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] OverflowServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MonoTouch.Foundation.NSDictionary ServiceData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] ServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] SolicitedServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MonoTouch.Foundation.NSNumber TxPowerLevel { get; set; }</span>
}
</pre>
</div> <!-- end type AdvertisementData -->
<div> <!-- start type RestoredState -->
<h3>New Type MonoTouch.CoreBluetooth.RestoredState</h3>
<pre class='added' data-is-non-breaking="">
public class RestoredState : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RestoredState ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RestoredState (MonoTouch.Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral[] Peripherals { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PeripheralScanningOptions ScanOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral[] ScanServices { get; set; }</span>
}
</pre>
</div> <!-- end type RestoredState -->

</div> <!-- end namespace MonoTouch.CoreBluetooth -->
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
	public virtual NSExpression ExpressionValueWithObject (NSObject obj, NSMutableDictionary context);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFormat (string, NSExpression[]) is deprecated, please use FromFormat (string, NSObject[]) instead.")]
	public static NSExpression FromFormat (string format, NSExpression[] parameters);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFunction (NSExpressionHandler, NSExpression[]) is deprecated, please use FromFunction (NSExpressionCallbackHandler, NSExpression[]) instead.")]
	public static NSExpression FromFunction (NSExpressionHandler target, NSExpression[] parameters);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual NSExpression ExpressionValueWithObject (NSObject <span class='removed removed-inline '>object1</span> <span class='added '>obj</span>, NSMutableDictionary context)
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
<!-- start type NSMutableAttributedString --> <div>
<h3>Type Changed: MonoTouch.Foundation.NSMutableAttributedString</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMutableString MutableString { get; }</span>
</pre>
</div>

</div> <!-- end type NSMutableAttributedString -->
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
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public int Port { get; }</span>
</pre>
</div>
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
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use DidRequestMatch(GKPlayer player, GKPlayer[] recipientPlayers) instead")]
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);</span>
</div></pre>

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
<!-- start type UIView --> <div>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIImage Capture (bool afterScreenUpdates);</span>
</pre>
</div>

</div> <!-- end type UIView -->
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
</script><h1 id='diff/xi/2.1/System.Net.Http.html'>System.Net.Http.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Net.Http --> <div> 
<h2>Namespace System.Net.Http</h2>
<!-- start type HttpClientHandler --> <div>
<h3>Type Changed: System.Net.Http.HttpClientHandler</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool CheckCertificateRevocationList { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509CertificateCollection ClientCertificates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Net.ICredentials DefaultProxyCredentials { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxConnectionsPerServer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxResponseHeadersLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IDictionary&lt;System.String,System.Object&gt; Properties { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Func&lt;HttpRequestMessage,System.Security.Cryptography.X509Certificates.X509Certificate2,System.Security.Cryptography.X509Certificates.X509Chain,System.Net.Security.SslPolicyErrors,System.Boolean&gt; ServerCertificateCustomValidationCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.SslProtocols SslProtocols { get; set; }</span>
</pre>
</div>

</div> <!-- end type HttpClientHandler -->

</div> <!-- end namespace System.Net.Http -->
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
</script><h1 id='diff/xi/Xamarin.iOS/System.Net.Http.html'>System.Net.Http.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Net.Http --> <div> 
<h2>Namespace System.Net.Http</h2>
<!-- start type HttpClientHandler --> <div>
<h3>Type Changed: System.Net.Http.HttpClientHandler</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool CheckCertificateRevocationList { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509CertificateCollection ClientCertificates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Net.ICredentials DefaultProxyCredentials { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxConnectionsPerServer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxResponseHeadersLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IDictionary&lt;System.String,System.Object&gt; Properties { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Func&lt;HttpRequestMessage,System.Security.Cryptography.X509Certificates.X509Certificate2,System.Security.Cryptography.X509Certificates.X509Chain,System.Net.Security.SslPolicyErrors,System.Boolean&gt; ServerCertificateCustomValidationCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.SslProtocols SslProtocols { get; set; }</span>
</pre>
</div>

</div> <!-- end type HttpClientHandler -->

</div> <!-- end namespace System.Net.Http -->
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
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public MusicTrack GetTempoTrack ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetUserCallback (MusicSequenceUserCallback callback);</span>
</pre>
</div>

</div> <!-- end type MusicSequence -->
<div> <!-- start type MusicSequenceUserCallback -->
<h3>New Type AudioToolbox.MusicSequenceUserCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MusicSequenceUserCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MusicSequenceUserCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MusicTrack track, double inEventTime, MusicEventUserData inEventData, double inStartSliceBeat, double inEndSliceBeat, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (MusicTrack track, double inEventTime, MusicEventUserData inEventData, double inStartSliceBeat, double inEndSliceBeat);</span>
}
</pre>
</div> <!-- end type MusicSequenceUserCallback -->

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
<!-- start type AUParameter --> <div>
<h3>Type Changed: AudioUnit.AUParameter</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void SetValue (float value, IntPtr originator);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void SetValue (float value, IntPtr originator, ulong hostTime);</span>
</div></pre>
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
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void RemoveParameterObserver (IntPtr token);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the CreateTokenByAddingParameterObserver instead")]
	public virtual IntPtr TokenByAddingParameterObserver (AUParameterObserver observer);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterObserver (AUParameterObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterRecordingObserver (AUParameterRecordingObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveParameterObserver (AUParameterObserverToken token);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use the CreateTokenByAddingParameterRecordingObserver instead")]
	public virtual IntPtr TokenByAddingParameterRecordingObserver (AUParameterRecordingObserver observer);</span>
</pre>
</div>

</div> <!-- end type AUParameterNode -->
<div> <!-- start type AUHostTransportStateBlock -->
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
<!-- start namespace CoreBluetooth --> <div> 
<h2>Namespace CoreBluetooth</h2>
<div> <!-- start type AdvertisementData -->
<h3>New Type CoreBluetooth.AdvertisementData</h3>
<pre class='added' data-is-non-breaking="">
public class AdvertisementData : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisementData ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisementData (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? IsConnectable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string LocalName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData ManufacturerData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] OverflowServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary&lt;CBUUID,Foundation.NSData&gt; ServiceData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] ServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] SolicitedServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber TxPowerLevel { get; set; }</span>
}
</pre>
</div> <!-- end type AdvertisementData -->
<div> <!-- start type RestoredState -->
<h3>New Type CoreBluetooth.RestoredState</h3>
<pre class='added' data-is-non-breaking="">
public class RestoredState : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RestoredState ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RestoredState (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral[] Peripherals { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PeripheralScanningOptions ScanOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral[] ScanServices { get; set; }</span>
}
</pre>
</div> <!-- end type RestoredState -->

</div> <!-- end namespace CoreBluetooth -->
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
<!-- start type DictionaryContainer --> <div>
<h3>Type Changed: Foundation.DictionaryContainer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected Foundation.NSDictionary&lt;TKey,TValue&gt; GetNSDictionary&lt;TKey, TValue&gt; (NSString key);</span>
</pre>
</div>

</div> <!-- end type DictionaryContainer -->
<!-- start type NSDictionary`2 --> <div>
<h3>Type Changed: Foundation.NSDictionary`2</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("TKey and TValue are inversed and won't work unless both types are identical. Use the generic overload that takes a count parameter instead")]
	public static Foundation.NSDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TKey[] objects, TValue[] keys);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TValue[] objects, TKey[] keys, nint count);</span>
</pre>
</div>

</div> <!-- end type NSDictionary`2 -->
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
	public virtual NSExpression ExpressionValueWithObject (NSObject obj, NSMutableDictionary context);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFormat (string, NSExpression[]) is deprecated, please use FromFormat (string, NSObject[]) instead.")]
	public static NSExpression FromFormat (string format, NSExpression[] parameters);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFunction (NSExpressionHandler, NSExpression[]) is deprecated, please use FromFunction (NSExpressionCallbackHandler, NSExpression[]) instead.")]
	public static NSExpression FromFunction (NSExpressionHandler target, NSExpression[] parameters);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual NSExpression ExpressionValueWithObject (NSObject <span class='removed removed-inline '>object1</span> <span class='added '>obj</span>, NSMutableDictionary context)
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
<!-- start type NSMutableAttributedString --> <div>
<h3>Type Changed: Foundation.NSMutableAttributedString</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMutableString MutableString { get; }</span>
</pre>
</div>

</div> <!-- end type NSMutableAttributedString -->
<!-- start type NSMutableDictionary`2 --> <div>
<h3>Type Changed: Foundation.NSMutableDictionary`2</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("TKey and TValue are inversed and won't work unless both types are identical. Use the generic overload that takes a count parameter instead")]
	public static Foundation.NSMutableDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TKey[] objects, TValue[] keys);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSMutableDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TValue[] objects, TKey[] keys, nint count);</span>
</pre>
</div>

</div> <!-- end type NSMutableDictionary`2 -->
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
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public int Port { get; }</span>
</pre>
</div>
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
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"9.8.0"</span> <span class='added '>"9.10.0"</span>;
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
<!-- start type UIView --> <div>
<h3>Type Changed: UIKit.UIView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIImage Capture (bool afterScreenUpdates);</span>
</pre>
</div>

</div> <!-- end type UIView -->
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
