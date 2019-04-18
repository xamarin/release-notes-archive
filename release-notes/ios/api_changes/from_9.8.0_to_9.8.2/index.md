---
id: B5835256-0EAF-4C8F-96C3-DFA5492E9127
title: "From 9.8.0 to 9.8.2"
---

# API diff

 [(Classic) mscorlib.dll](#diff/xi/2.1/mscorlib.html)

   


 [(Classic) System.dll](#diff/xi/2.1/System.html)

   


 [(Classic) System.Core.dll](#diff/xi/2.1/System.Core.html)

   


 [(Classic) System.Numerics.dll](#diff/xi/2.1/System.Numerics.html)

   


 [(Classic) System.Data.dll](#diff/xi/2.1/System.Data.html)

   


 [(Classic) System.ServiceModel.dll](#diff/xi/2.1/System.ServiceModel.html)

   


 [(Classic) System.IO.Compression.dll](#diff/xi/2.1/System.IO.Compression.html)

   


 [(Classic) monotouch.dll](#diff/xi/2.1/monotouch.html)

   


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
<div> <!-- start type Registry -->
<h3>New Type Microsoft.Win32.Registry</h3>
<pre class='added' data-is-non-breaking="">
public static class Registry {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static RegistryKey ClassesRoot;</span>
	<span class='added added-field ' data-is-non-breaking="">public static RegistryKey CurrentConfig;</span>
	<span class='added added-field ' data-is-non-breaking="">public static RegistryKey CurrentUser;</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("Use PerformanceData instead")]
	public static RegistryKey DynData;</span>
	<span class='added added-field ' data-is-non-breaking="">public static RegistryKey LocalMachine;</span>
	<span class='added added-field ' data-is-non-breaking="">public static RegistryKey PerformanceData;</span>
	<span class='added added-field ' data-is-non-breaking="">public static RegistryKey Users;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static object GetValue (string keyName, string valueName, object defaultValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetValue (string keyName, string valueName, object value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetValue (string keyName, string valueName, object value, RegistryValueKind valueKind);</span>
}
</pre>
</div> <!-- end type Registry -->
<div> <!-- start type RegistryHive -->
<h3>New Type Microsoft.Win32.RegistryHive</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RegistryHive {
	<span class='added added-field ' data-is-non-breaking="">ClassesRoot = -2147483648,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentConfig = -2147483643,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentUser = -2147483647,</span>
	<span class='added added-field ' data-is-non-breaking="">DynData = -2147483642,</span>
	<span class='added added-field ' data-is-non-breaking="">LocalMachine = -2147483646,</span>
	<span class='added added-field ' data-is-non-breaking="">PerformanceData = -2147483644,</span>
	<span class='added added-field ' data-is-non-breaking="">Users = -2147483645,</span>
}
</pre>
</div> <!-- end type RegistryHive -->
<div> <!-- start type RegistryKey -->
<h3>New Type Microsoft.Win32.RegistryKey</h3>
<pre class='added' data-is-non-breaking="">
public sealed class RegistryKey : System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public object GetValue (string name, object defaultValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static object GetValue (string keyName, string valueName, object defaultValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey OpenSubKey (string name, bool writable);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (string name, object value);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (string name, object value, RegistryValueKind valueKind);</span>
}
</pre>
</div> <!-- end type RegistryKey -->
<div> <!-- start type RegistryValueKind -->
<h3>New Type Microsoft.Win32.RegistryValueKind</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RegistryValueKind {
	<span class='added added-field ' data-is-non-breaking="">Binary = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">DWord = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ExpandString = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiString = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">None = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">QWord = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type RegistryValueKind -->
<div> <!-- start type RegistryValueOptions -->
<h3>New Type Microsoft.Win32.RegistryValueOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum RegistryValueOptions {
	<span class='added added-field ' data-is-non-breaking="">DoNotExpandEnvironmentNames = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type RegistryValueOptions -->

</div> <!-- end namespace Microsoft.Win32 -->
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
<!-- start namespace System.Diagnostics.Tracing --> <div> 
<h2>Namespace System.Diagnostics.Tracing</h2>
<div> <!-- start type EventDataAttribute -->
<h3>New Type System.Diagnostics.Tracing.EventDataAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class EventDataAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EventDataAttribute ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; set; }</span>
}
</pre>
</div> <!-- end type EventDataAttribute -->
<div> <!-- start type EventFieldAttribute -->
<h3>New Type System.Diagnostics.Tracing.EventFieldAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class EventFieldAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EventFieldAttribute ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public EventFieldFormat Format { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventFieldTags Tags { get; set; }</span>
}
</pre>
</div> <!-- end type EventFieldAttribute -->
<div> <!-- start type EventFieldFormat -->
<h3>New Type System.Diagnostics.Tracing.EventFieldFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum EventFieldFormat {
	<span class='added added-field ' data-is-non-breaking="">Boolean = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">HResult = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Hexadecimal = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Json = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Xml = 11,</span>
}
</pre>
</div> <!-- end type EventFieldFormat -->
<div> <!-- start type EventFieldTags -->
<h3>New Type System.Diagnostics.Tracing.EventFieldTags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum EventFieldTags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type EventFieldTags -->
<div> <!-- start type EventIgnoreAttribute -->
<h3>New Type System.Diagnostics.Tracing.EventIgnoreAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class EventIgnoreAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EventIgnoreAttribute ();</span>
}
</pre>
</div> <!-- end type EventIgnoreAttribute -->
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
<div> <!-- start type EventManifestOptions -->
<h3>New Type System.Diagnostics.Tracing.EventManifestOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum EventManifestOptions {
	<span class='added added-field ' data-is-non-breaking="">AllCultures = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowEventSourceOverride = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OnlyIfNeededForRegistration = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Strict = 1,</span>
}
</pre>
</div> <!-- end type EventManifestOptions -->
<div> <!-- start type EventSourceException -->
<h3>New Type System.Diagnostics.Tracing.EventSourceException</h3>
<pre class='added' data-is-non-breaking="">
public class EventSourceException : System.Exception, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EventSourceException ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EventSourceException (string message);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EventSourceException (string message, System.Exception innerException);</span>
}
</pre>
</div> <!-- end type EventSourceException -->
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
<!-- start namespace System.Globalization --> <div> 
<h2>Namespace System.Globalization</h2>
<!-- start type CultureInfo --> <div>
<h3>Type Changed: System.Globalization.CultureInfo</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public CultureInfo CurrentCulture { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public CultureInfo CurrentUICulture { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type CultureInfo -->

</div> <!-- end namespace System.Globalization -->
<!-- start namespace System.Reflection --> <div> 
<h2>Namespace System.Reflection</h2>
<!-- start type AssemblyName --> <div>
<h3>Type Changed: System.Reflection.AssemblyName</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public string CultureName { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type AssemblyName -->

</div> <!-- end namespace System.Reflection -->
<!-- start namespace System.Reflection.Emit --> <div> 
<h2>Namespace System.Reflection.Emit</h2>
<div> <!-- start type FlowControl -->
<h3>New Type System.Reflection.Emit.FlowControl</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum FlowControl {
	<span class='added added-field ' data-is-non-breaking="">Branch = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Break = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Call = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Cond_Branch = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Meta = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Next = 5,</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This API has been deprecated.")]
	Phi = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Return = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Throw = 8,</span>
}
</pre>
</div> <!-- end type FlowControl -->
<div> <!-- start type OpCode -->
<h3>New Type System.Reflection.Emit.OpCode</h3>
<pre class='added' data-is-non-breaking="">
public struct OpCode {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public FlowControl FlowControl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OpCodeType OpCodeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OperandType OperandType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Size { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public StackBehaviour StackBehaviourPop { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public StackBehaviour StackBehaviourPush { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public short Value { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (OpCode obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (OpCode a, OpCode b);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (OpCode a, OpCode b);</span>
}
</pre>
</div> <!-- end type OpCode -->
<div> <!-- start type OpCodeType -->
<h3>New Type System.Reflection.Emit.OpCodeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum OpCodeType {

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This API has been deprecated.")]
	Annotation = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Macro = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Nternal = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Objmodel = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Prefix = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Primitive = 5,</span>
}
</pre>
</div> <!-- end type OpCodeType -->
<div> <!-- start type OpCodes -->
<h3>New Type System.Reflection.Emit.OpCodes</h3>
<pre class='added' data-is-non-breaking="">
public class OpCodes {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Add;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Add_Ovf;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Add_Ovf_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode And;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Arglist;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Beq;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Beq_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bge;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bge_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bge_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bge_Un_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bgt;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bgt_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bgt_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bgt_Un_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ble;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ble_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ble_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ble_Un_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Blt;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Blt_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Blt_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Blt_Un_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bne_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Bne_Un_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Box;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Br;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Br_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Break;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Brfalse;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Brfalse_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Brtrue;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Brtrue_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Call;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Calli;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Callvirt;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Castclass;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ceq;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Cgt;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Cgt_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ckfinite;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Clt;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Clt_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Constrained;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_I;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_I1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_I2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_I4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_I8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I1_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I2_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I4_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I8_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_I_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U1_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U2_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U4_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U8_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_Ovf_U_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_R4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_R8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_R_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_U;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_U1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_U2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_U4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Conv_U8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Cpblk;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Cpobj;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Div;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Div_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Dup;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Endfilter;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Endfinally;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Initblk;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Initobj;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Isinst;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Jmp;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldarg;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldarg_0;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldarg_1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldarg_2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldarg_3;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldarg_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldarga;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldarga_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_0;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_3;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_5;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_6;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_7;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_M1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I4_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_I8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_R4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldc_R8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_I;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_I1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_I2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_I4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_I8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_R4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_R8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_Ref;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_U1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_U2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelem_U4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldelema;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldfld;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldflda;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldftn;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_I;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_I1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_I2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_I4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_I8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_R4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_R8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_Ref;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_U1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_U2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldind_U4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldlen;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldloc;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldloc_0;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldloc_1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldloc_2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldloc_3;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldloc_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldloca;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldloca_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldnull;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldobj;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldsfld;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldsflda;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldstr;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldtoken;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ldvirtftn;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Leave;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Leave_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Localloc;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Mkrefany;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Mul;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Mul_Ovf;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Mul_Ovf_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Neg;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Newarr;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Newobj;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Nop;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Not;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Or;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Pop;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Prefix1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Prefix2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Prefix3;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Prefix4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Prefix5;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Prefix6;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Prefix7;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Prefixref;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Readonly;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Refanytype;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Refanyval;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Rem;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Rem_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Ret;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Rethrow;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Shl;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Shr;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Shr_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Sizeof;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Starg;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Starg_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem_I;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem_I1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem_I2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem_I4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem_I8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem_R4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem_R8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stelem_Ref;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stfld;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stind_I;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stind_I1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stind_I2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stind_I4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stind_I8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stind_R4;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stind_R8;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stind_Ref;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stloc;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stloc_0;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stloc_1;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stloc_2;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stloc_3;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stloc_S;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stobj;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Stsfld;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Sub;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Sub_Ovf;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Sub_Ovf_Un;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Switch;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Tailcall;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Throw;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Unaligned;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Unbox;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Unbox_Any;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Volatile;</span>
	<span class='added added-field ' data-is-non-breaking="">public static OpCode Xor;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool TakesSingleByteArgument (OpCode inst);</span>
}
</pre>
</div> <!-- end type OpCodes -->
<div> <!-- start type OperandType -->
<h3>New Type System.Reflection.Emit.OperandType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum OperandType {
	<span class='added added-field ' data-is-non-breaking="">InlineBrTarget = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineField = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineI = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineI8 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineMethod = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineNone = 5,</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("This API has been deprecated.")]
	InlinePhi = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineR = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineSig = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineString = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineSwitch = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineTok = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineType = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineVar = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">ShortInlineBrTarget = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">ShortInlineI = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">ShortInlineR = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">ShortInlineVar = 18,</span>
}
</pre>
</div> <!-- end type OperandType -->
<div> <!-- start type PackingSize -->
<h3>New Type System.Reflection.Emit.PackingSize</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PackingSize {
	<span class='added added-field ' data-is-non-breaking="">Size1 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Size128 = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">Size16 = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Size2 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Size32 = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Size4 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Size64 = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">Size8 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type PackingSize -->
<div> <!-- start type StackBehaviour -->
<h3>New Type System.Reflection.Emit.StackBehaviour</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum StackBehaviour {
	<span class='added added-field ' data-is-non-breaking="">Pop0 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Pop1 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Pop1_pop1 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Popi = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Popi_pop1 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Popi_popi = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Popi_popi8 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Popi_popi_popi = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Popi_popr4 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Popi_popr8 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref_pop1 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref_popi = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref_popi_pop1 = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref_popi_popi = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref_popi_popi8 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref_popi_popr4 = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref_popi_popr8 = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Popref_popi_popref = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Push0 = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">Push1 = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Push1_push1 = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">Pushi = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">Pushi8 = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">Pushr4 = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">Pushr8 = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">Pushref = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Varpop = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">Varpush = 27,</span>
}
</pre>
</div> <!-- end type StackBehaviour -->

</div> <!-- end namespace System.Reflection.Emit -->
<!-- start namespace System.Runtime.InteropServices --> <div> 
<h2>Namespace System.Runtime.InteropServices</h2>
<div> <!-- start type ComAwareEventInfo -->
<h3>New Type System.Runtime.InteropServices.ComAwareEventInfo</h3>
<pre class='added' data-is-non-breaking="">
public class ComAwareEventInfo : System.Reflection.EventInfo, System.Reflection.ICustomAttributeProvider, _MemberInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ComAwareEventInfo (System.Type type, string eventName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.EventAttributes Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type DeclaringType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type ReflectedType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override void AddEventHandler (object target, System.Delegate handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Reflection.MethodInfo GetAddMethod (bool nonPublic);</span>
	<span class='added added-method ' data-is-non-breaking="">public override object[] GetCustomAttributes (bool inherit);</span>
	<span class='added added-method ' data-is-non-breaking="">public override object[] GetCustomAttributes (System.Type attributeType, bool inherit);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Reflection.MethodInfo GetRaiseMethod (bool nonPublic);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Reflection.MethodInfo GetRemoveMethod (bool nonPublic);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool IsDefined (System.Type attributeType, bool inherit);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void RemoveEventHandler (object target, System.Delegate handler);</span>
}
</pre>
</div> <!-- end type ComAwareEventInfo -->
<div> <!-- start type ComEventsHelper -->
<h3>New Type System.Runtime.InteropServices.ComEventsHelper</h3>
<pre class='added' data-is-non-breaking="">
public static class ComEventsHelper {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Combine (object rcw, System.Guid iid, int dispid, System.Delegate d);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Delegate Remove (object rcw, System.Guid iid, int dispid, System.Delegate d);</span>
}
</pre>
</div> <!-- end type ComEventsHelper -->
<div> <!-- start type CustomQueryInterfaceMode -->
<h3>New Type System.Runtime.InteropServices.CustomQueryInterfaceMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CustomQueryInterfaceMode {
	<span class='added added-field ' data-is-non-breaking="">Allow = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Ignore = 0,</span>
}
</pre>
</div> <!-- end type CustomQueryInterfaceMode -->
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
<!-- start namespace System.Reflection.Metadata --> <div> 
<h2>New Namespace System.Reflection.Metadata</h2>

<div> <!-- start type AssemblyExtensions -->
<h3>New Type System.Reflection.Metadata.AssemblyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AssemblyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool TryGetRawMetadata (System.Reflection.Assembly assembly, out byte* blob, out int length);</span>
}
</pre>
</div> <!-- end type AssemblyExtensions -->
</div> <!-- end namespace System.Reflection.Metadata -->

<!-- start namespace System.Runtime.Loader --> <div> 
<h2>New Namespace System.Runtime.Loader</h2>

<div> <!-- start type AssemblyLoadContext -->
<h3>New Type System.Runtime.Loader.AssemblyLoadContext</h3>
<pre class='added' data-is-non-breaking="">
public abstract class AssemblyLoadContext {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AssemblyLoadContext ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static AssemblyLoadContext Default { get; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.Func&lt;AssemblyLoadContext,System.Reflection.AssemblyName,System.Reflection.Assembly&gt; Resolving;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.Action&lt;AssemblyLoadContext&gt; Unloading;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static System.Reflection.AssemblyName GetAssemblyName (string assemblyPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AssemblyLoadContext GetLoadContext (System.Reflection.Assembly assembly);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual System.Reflection.Assembly Load (System.Reflection.AssemblyName assemblyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Reflection.Assembly LoadFromAssemblyName (System.Reflection.AssemblyName assemblyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Reflection.Assembly LoadFromAssemblyPath (string assemblyPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Reflection.Assembly LoadFromNativeImagePath (string nativeImagePath, string assemblyPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Reflection.Assembly LoadFromStream (System.IO.Stream assembly);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Reflection.Assembly LoadFromStream (System.IO.Stream assembly, System.IO.Stream assemblySymbols);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual IntPtr LoadUnmanagedDll (string unmanagedDllName);</span>
	<span class='added added-method ' data-is-non-breaking="">protected IntPtr LoadUnmanagedDllFromPath (string unmanagedDllPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetProfileOptimizationRoot (string directoryPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public void StartProfileOptimization (string profile);</span>
}
</pre>
</div> <!-- end type AssemblyLoadContext -->
</div> <!-- end namespace System.Runtime.Loader -->

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
<!-- start namespace System.IO --> <div> 
<h2>Namespace System.IO</h2>
<div> <!-- start type ErrorEventArgs -->
<h3>New Type System.IO.ErrorEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class ErrorEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ErrorEventArgs (System.Exception exception);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Exception GetException ();</span>
}
</pre>
</div> <!-- end type ErrorEventArgs -->
<div> <!-- start type ErrorEventHandler -->
<h3>New Type System.IO.ErrorEventHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ErrorEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ErrorEventHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, ErrorEventArgs e, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, ErrorEventArgs e);</span>
}
</pre>
</div> <!-- end type ErrorEventHandler -->
<div> <!-- start type FileSystemEventArgs -->
<h3>New Type System.IO.FileSystemEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class FileSystemEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemEventArgs (WatcherChangeTypes changeType, string directory, string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public WatcherChangeTypes ChangeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string FullPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
}
</pre>
</div> <!-- end type FileSystemEventArgs -->
<div> <!-- start type FileSystemEventHandler -->
<h3>New Type System.IO.FileSystemEventHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate FileSystemEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemEventHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, FileSystemEventArgs e, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, FileSystemEventArgs e);</span>
}
</pre>
</div> <!-- end type FileSystemEventHandler -->
<div> <!-- start type FileSystemWatcher -->
<h3>New Type System.IO.FileSystemWatcher</h3>
<pre class='added' data-is-non-breaking="">
public class FileSystemWatcher {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemWatcher ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemWatcher (string path);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FileSystemWatcher (string path, string filter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool EnableRaisingEvents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Filter { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IncludeSubdirectories { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int InternalBufferSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NotifyFilters NotifyFilter { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Path { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event FileSystemEventHandler Changed;</span>
	<span class='added added-event ' data-is-non-breaking="">public event FileSystemEventHandler Created;</span>
	<span class='added added-event ' data-is-non-breaking="">public event FileSystemEventHandler Deleted;</span>
	<span class='added added-event ' data-is-non-breaking="">public event ErrorEventHandler Error;</span>
	<span class='added added-event ' data-is-non-breaking="">public event RenamedEventHandler Renamed;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected void OnChanged (FileSystemEventArgs e);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void OnCreated (FileSystemEventArgs e);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void OnDeleted (FileSystemEventArgs e);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void OnError (ErrorEventArgs e);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void OnRenamed (RenamedEventArgs e);</span>
	<span class='added added-method ' data-is-non-breaking="">public WaitForChangedResult WaitForChanged (WatcherChangeTypes changeType);</span>
	<span class='added added-method ' data-is-non-breaking="">public WaitForChangedResult WaitForChanged (WatcherChangeTypes changeType, int timeout);</span>
}
</pre>
</div> <!-- end type FileSystemWatcher -->
<div> <!-- start type NotifyFilters -->
<h3>New Type System.IO.NotifyFilters</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NotifyFilters {
	<span class='added added-field ' data-is-non-breaking="">Attributes = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">CreationTime = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">DirectoryName = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FileName = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">LastAccess = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">LastWrite = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Security = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">Size = 8,</span>
}
</pre>
</div> <!-- end type NotifyFilters -->
<div> <!-- start type RenamedEventArgs -->
<h3>New Type System.IO.RenamedEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class RenamedEventArgs : System.IO.FileSystemEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RenamedEventArgs (WatcherChangeTypes changeType, string directory, string name, string oldName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string OldFullPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string OldName { get; }</span>
}
</pre>
</div> <!-- end type RenamedEventArgs -->
<div> <!-- start type RenamedEventHandler -->
<h3>New Type System.IO.RenamedEventHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RenamedEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RenamedEventHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, RenamedEventArgs e, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, RenamedEventArgs e);</span>
}
</pre>
</div> <!-- end type RenamedEventHandler -->
<div> <!-- start type WaitForChangedResult -->
<h3>New Type System.IO.WaitForChangedResult</h3>
<pre class='added' data-is-non-breaking="">
public struct WaitForChangedResult {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public WatcherChangeTypes ChangeType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string OldName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool TimedOut { get; set; }</span>
}
</pre>
</div> <!-- end type WaitForChangedResult -->
<div> <!-- start type WatcherChangeTypes -->
<h3>New Type System.IO.WatcherChangeTypes</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum WatcherChangeTypes {
	<span class='added added-field ' data-is-non-breaking="">All = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Changed = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Created = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Deleted = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Renamed = 8,</span>
}
</pre>
</div> <!-- end type WatcherChangeTypes -->

</div> <!-- end namespace System.IO -->
<!-- start namespace System.Net.WebSockets --> <div> 
<h2>Namespace System.Net.WebSockets</h2>
<!-- start type WebSocketCloseStatus --> <div>
<h3>Type Changed: System.Net.WebSockets.WebSocketCloseStatus</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	Empty = <span class='removed removed-inline removed-breaking-inline'>1004</span> <span class='added '>1005</span>
</div><div data-is-breaking="">	MessageTooBig = <span class='removed removed-inline removed-breaking-inline'>1004</span> <span class='added '>1009</span>
</div></pre>

</div> <!-- end type WebSocketCloseStatus -->

</div> <!-- end namespace System.Net.WebSockets -->
<!-- start namespace System.Security.Authentication.ExtendedProtection --> <div> 
<h2>Namespace System.Security.Authentication.ExtendedProtection</h2>
<!-- start type ChannelBindingKind --> <div>
<h3>Type Changed: System.Security.Authentication.ExtendedProtection.ChannelBindingKind</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	Endpoint = <span class='removed removed-inline removed-breaking-inline'>2</span> <span class='added '>26</span>
</div><div data-is-breaking="">	Unique = <span class='removed removed-inline removed-breaking-inline'>1</span> <span class='added '>25</span>
</div></pre>

</div> <!-- end type ChannelBindingKind -->

</div> <!-- end namespace System.Security.Authentication.ExtendedProtection -->
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
<div> <!-- start type SafeX509ChainHandle -->
<h3>New Type Microsoft.Win32.SafeHandles.SafeX509ChainHandle</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SafeX509ChainHandle : System.Runtime.InteropServices.SafeHandle, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override bool IsInvalid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override bool ReleaseHandle ();</span>
}
</pre>
</div> <!-- end type SafeX509ChainHandle -->
</div> <!-- end namespace Microsoft.Win32.SafeHandles -->

<!-- start namespace System.Runtime.InteropServices.ComTypes --> <div> 
<h2>New Namespace System.Runtime.InteropServices.ComTypes</h2>

<div> <!-- start type ADVF -->
<h3>New Type System.Runtime.InteropServices.ComTypes.ADVF</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum ADVF {
	<span class='added added-field ' data-is-non-breaking="">ADVFCACHE_FORCEBUILTIN = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">ADVFCACHE_NOHANDLER = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ADVFCACHE_ONSAVE = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">ADVF_DATAONSTOP = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">ADVF_NODATA = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ADVF_ONLYONCE = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ADVF_PRIMEFIRST = 2,</span>
}
</pre>
</div> <!-- end type ADVF -->
<div> <!-- start type DATADIR -->
<h3>New Type System.Runtime.InteropServices.ComTypes.DATADIR</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum DATADIR {
	<span class='added added-field ' data-is-non-breaking="">DATADIR_GET = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">DATADIR_SET = 2,</span>
}
</pre>
</div> <!-- end type DATADIR -->
<div> <!-- start type DVASPECT -->
<h3>New Type System.Runtime.InteropServices.ComTypes.DVASPECT</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum DVASPECT {
	<span class='added added-field ' data-is-non-breaking="">DVASPECT_CONTENT = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">DVASPECT_DOCPRINT = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">DVASPECT_ICON = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">DVASPECT_THUMBNAIL = 2,</span>
}
</pre>
</div> <!-- end type DVASPECT -->
<div> <!-- start type FORMATETC -->
<h3>New Type System.Runtime.InteropServices.ComTypes.FORMATETC</h3>
<pre class='added' data-is-non-breaking="">
public struct FORMATETC {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public short cfFormat;</span>
	<span class='added added-field ' data-is-non-breaking="">public DVASPECT dwAspect;</span>
	<span class='added added-field ' data-is-non-breaking="">public int lindex;</span>
	<span class='added added-field ' data-is-non-breaking="">public IntPtr ptd;</span>
	<span class='added added-field ' data-is-non-breaking="">public TYMED tymed;</span>
}
</pre>
</div> <!-- end type FORMATETC -->
<div> <!-- start type IAdviseSink -->
<h3>New Type System.Runtime.InteropServices.ComTypes.IAdviseSink</h3>
<pre class='added' data-is-non-breaking="">
public interface IAdviseSink {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnClose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnDataChange (ref FORMATETC format, ref STGMEDIUM stgmedium);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnRename (IMoniker moniker);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnSave ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OnViewChange (int aspect, int index);</span>
}
</pre>
</div> <!-- end type IAdviseSink -->
<div> <!-- start type IDataObject -->
<h3>New Type System.Runtime.InteropServices.ComTypes.IDataObject</h3>
<pre class='added' data-is-non-breaking="">
public interface IDataObject {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int DAdvise (ref FORMATETC pFormatetc, ADVF advf, IAdviseSink adviseSink, out int connection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DUnadvise (int connection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int EnumDAdvise (out IEnumSTATDATA enumAdvise);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IEnumFORMATETC EnumFormatEtc (DATADIR direction);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int GetCanonicalFormatEtc (ref FORMATETC formatIn, out FORMATETC formatOut);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetData (ref FORMATETC format, out STGMEDIUM medium);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetDataHere (ref FORMATETC format, ref STGMEDIUM medium);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int QueryGetData (ref FORMATETC format);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetData (ref FORMATETC formatIn, ref STGMEDIUM medium, bool release);</span>
}
</pre>
</div> <!-- end type IDataObject -->
<div> <!-- start type IEnumFORMATETC -->
<h3>New Type System.Runtime.InteropServices.ComTypes.IEnumFORMATETC</h3>
<pre class='added' data-is-non-breaking="">
public interface IEnumFORMATETC {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Clone (out IEnumFORMATETC newEnum);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Next (int celt, FORMATETC[] rgelt, int[] pceltFetched);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Reset ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Skip (int celt);</span>
}
</pre>
</div> <!-- end type IEnumFORMATETC -->
<div> <!-- start type IEnumSTATDATA -->
<h3>New Type System.Runtime.InteropServices.ComTypes.IEnumSTATDATA</h3>
<pre class='added' data-is-non-breaking="">
public interface IEnumSTATDATA {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Clone (out IEnumSTATDATA newEnum);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Next (int celt, STATDATA[] rgelt, int[] pceltFetched);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Reset ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Skip (int celt);</span>
}
</pre>
</div> <!-- end type IEnumSTATDATA -->
<div> <!-- start type STATDATA -->
<h3>New Type System.Runtime.InteropServices.ComTypes.STATDATA</h3>
<pre class='added' data-is-non-breaking="">
public struct STATDATA {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public IAdviseSink advSink;</span>
	<span class='added added-field ' data-is-non-breaking="">public ADVF advf;</span>
	<span class='added added-field ' data-is-non-breaking="">public int connection;</span>
	<span class='added added-field ' data-is-non-breaking="">public FORMATETC formatetc;</span>
}
</pre>
</div> <!-- end type STATDATA -->
<div> <!-- start type STGMEDIUM -->
<h3>New Type System.Runtime.InteropServices.ComTypes.STGMEDIUM</h3>
<pre class='added' data-is-non-breaking="">
public struct STGMEDIUM {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public object pUnkForRelease;</span>
	<span class='added added-field ' data-is-non-breaking="">public TYMED tymed;</span>
	<span class='added added-field ' data-is-non-breaking="">public IntPtr unionmember;</span>
}
</pre>
</div> <!-- end type STGMEDIUM -->
<div> <!-- start type TYMED -->
<h3>New Type System.Runtime.InteropServices.ComTypes.TYMED</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum TYMED {
	<span class='added added-field ' data-is-non-breaking="">TYMED_ENHMF = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">TYMED_FILE = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TYMED_GDI = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">TYMED_HGLOBAL = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TYMED_ISTORAGE = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">TYMED_ISTREAM = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">TYMED_MFPICT = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">TYMED_NULL = 0,</span>
}
</pre>
</div> <!-- end type TYMED -->
</div> <!-- end namespace System.Runtime.InteropServices.ComTypes -->

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
<!-- start namespace Microsoft.Win32.SafeHandles --> <div> 
<h2>Namespace Microsoft.Win32.SafeHandles</h2>
<div> <!-- start type SafeNCryptHandle -->
<h3>New Type Microsoft.Win32.SafeHandles.SafeNCryptHandle</h3>
<pre class='added' data-is-non-breaking="">
public abstract class SafeNCryptHandle : System.Runtime.InteropServices.SafeHandle, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SafeNCryptHandle ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override bool IsInvalid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override bool ReleaseHandle ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual bool ReleaseNativeHandle ();</span>
}
</pre>
</div> <!-- end type SafeNCryptHandle -->
<div> <!-- start type SafeNCryptKeyHandle -->
<h3>New Type Microsoft.Win32.SafeHandles.SafeNCryptKeyHandle</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SafeNCryptKeyHandle : Microsoft.Win32.SafeHandles.SafeNCryptHandle, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SafeNCryptKeyHandle ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override bool ReleaseNativeHandle ();</span>
}
</pre>
</div> <!-- end type SafeNCryptKeyHandle -->
<div> <!-- start type SafeNCryptProviderHandle -->
<h3>New Type Microsoft.Win32.SafeHandles.SafeNCryptProviderHandle</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SafeNCryptProviderHandle : Microsoft.Win32.SafeHandles.SafeNCryptHandle, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SafeNCryptProviderHandle ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override bool ReleaseNativeHandle ();</span>
}
</pre>
</div> <!-- end type SafeNCryptProviderHandle -->
<div> <!-- start type SafeNCryptSecretHandle -->
<h3>New Type Microsoft.Win32.SafeHandles.SafeNCryptSecretHandle</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SafeNCryptSecretHandle : Microsoft.Win32.SafeHandles.SafeNCryptHandle, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SafeNCryptSecretHandle ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override bool ReleaseNativeHandle ();</span>
}
</pre>
</div> <!-- end type SafeNCryptSecretHandle -->
<div> <!-- start type SafePipeHandle -->
<h3>New Type Microsoft.Win32.SafeHandles.SafePipeHandle</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SafePipeHandle : Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SafePipeHandle (IntPtr preexistingHandle, bool ownsHandle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override bool ReleaseHandle ();</span>
}
</pre>
</div> <!-- end type SafePipeHandle -->

</div> <!-- end namespace Microsoft.Win32.SafeHandles -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<div> <!-- start type AesCng -->
<h3>New Type System.Security.Cryptography.AesCng</h3>
<pre class='added' data-is-non-breaking="">
public sealed class AesCng : System.Security.Cryptography.Aes, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AesCng ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AesCng (string keyName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AesCng (string keyName, CngProvider provider);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AesCng (string keyName, CngProvider provider, CngKeyOpenOptions openOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override byte[] Key { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override int KeySize { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override ICryptoTransform CreateDecryptor ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override ICryptoTransform CreateDecryptor (byte[] rgbKey, byte[] rgbIV);</span>
	<span class='added added-method ' data-is-non-breaking="">public override ICryptoTransform CreateEncryptor ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override ICryptoTransform CreateEncryptor (byte[] rgbKey, byte[] rgbIV);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void GenerateIV ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override void GenerateKey ();</span>
}
</pre>
</div> <!-- end type AesCng -->
<div> <!-- start type CngAlgorithm -->
<h3>New Type System.Security.Cryptography.CngAlgorithm</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class CngAlgorithm : System.IEquatable&lt;CngAlgorithm&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngAlgorithm (string algorithm);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Algorithm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDiffieHellmanP256 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDiffieHellmanP384 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDiffieHellmanP521 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDsaP256 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDsaP384 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDsaP521 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm MD5 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm Rsa { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm Sha1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm Sha256 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm Sha384 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm Sha512 { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (CngAlgorithm other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (CngAlgorithm left, CngAlgorithm right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (CngAlgorithm left, CngAlgorithm right);</span>
}
</pre>
</div> <!-- end type CngAlgorithm -->
<div> <!-- start type CngAlgorithmGroup -->
<h3>New Type System.Security.Cryptography.CngAlgorithmGroup</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class CngAlgorithmGroup : System.IEquatable&lt;CngAlgorithmGroup&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngAlgorithmGroup (string algorithmGroup);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string AlgorithmGroup { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithmGroup DiffieHellman { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithmGroup Dsa { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithmGroup ECDiffieHellman { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithmGroup ECDsa { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithmGroup Rsa { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (CngAlgorithmGroup other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (CngAlgorithmGroup left, CngAlgorithmGroup right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (CngAlgorithmGroup left, CngAlgorithmGroup right);</span>
}
</pre>
</div> <!-- end type CngAlgorithmGroup -->
<div> <!-- start type CngExportPolicies -->
<h3>New Type System.Security.Cryptography.CngExportPolicies</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CngExportPolicies {
	<span class='added added-field ' data-is-non-breaking="">AllowArchiving = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowExport = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowPlaintextArchiving = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowPlaintextExport = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type CngExportPolicies -->
<div> <!-- start type CngKey -->
<h3>New Type System.Security.Cryptography.CngKey</h3>
<pre class='added' data-is-non-breaking="">
public sealed class CngKey : System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngKey ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
}
</pre>
</div> <!-- end type CngKey -->
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
<div> <!-- start type CngKeyCreationOptions -->
<h3>New Type System.Security.Cryptography.CngKeyCreationOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CngKeyCreationOptions {
	<span class='added added-field ' data-is-non-breaking="">MachineKey = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OverwriteExistingKey = 128,</span>
}
</pre>
</div> <!-- end type CngKeyCreationOptions -->
<div> <!-- start type CngKeyCreationParameters -->
<h3>New Type System.Security.Cryptography.CngKeyCreationParameters</h3>
<pre class='added' data-is-non-breaking="">
public sealed class CngKeyCreationParameters {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngKeyCreationParameters ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CngExportPolicies? ExportPolicy { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngKeyCreationOptions KeyCreationOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngKeyUsages? KeyUsage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngPropertyCollection Parameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IntPtr ParentWindowHandle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngProvider Provider { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngUIPolicy UIPolicy { get; set; }</span>
}
</pre>
</div> <!-- end type CngKeyCreationParameters -->
<div> <!-- start type CngKeyHandleOpenOptions -->
<h3>New Type System.Security.Cryptography.CngKeyHandleOpenOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CngKeyHandleOpenOptions {
	<span class='added added-field ' data-is-non-breaking="">EphemeralKey = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type CngKeyHandleOpenOptions -->
<div> <!-- start type CngKeyOpenOptions -->
<h3>New Type System.Security.Cryptography.CngKeyOpenOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CngKeyOpenOptions {
	<span class='added added-field ' data-is-non-breaking="">MachineKey = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Silent = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">UserKey = 0,</span>
}
</pre>
</div> <!-- end type CngKeyOpenOptions -->
<div> <!-- start type CngKeyUsages -->
<h3>New Type System.Security.Cryptography.CngKeyUsages</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CngKeyUsages {
	<span class='added added-field ' data-is-non-breaking="">AllUsages = 16777215,</span>
	<span class='added added-field ' data-is-non-breaking="">Decryption = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyAgreement = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Signing = 2,</span>
}
</pre>
</div> <!-- end type CngKeyUsages -->
<div> <!-- start type CngProperty -->
<h3>New Type System.Security.Cryptography.CngProperty</h3>
<pre class='added' data-is-non-breaking="">
public struct CngProperty, System.IEquatable&lt;CngProperty&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngProperty (string name, byte[] value, CngPropertyOptions options);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngPropertyOptions Options { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (CngProperty other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] GetValue ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (CngProperty left, CngProperty right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (CngProperty left, CngProperty right);</span>
}
</pre>
</div> <!-- end type CngProperty -->
<div> <!-- start type CngPropertyCollection -->
<h3>New Type System.Security.Cryptography.CngPropertyCollection</h3>
<pre class='added' data-is-non-breaking="">
public sealed class CngPropertyCollection : System.Collections.ObjectModel.Collection`1[System.Security.Cryptography.CngProperty], System.Collections.Generic.ICollection&lt;T&gt;, System.Collections.Generic.IEnumerable&lt;T&gt;, System.Collections.Generic.IList&lt;T&gt;, System.Collections.Generic.IReadOnlyCollection&lt;T&gt;, System.Collections.Generic.IReadOnlyList&lt;T&gt;, System.Collections.ICollection, System.Collections.IEnumerable, System.Collections.IList {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngPropertyCollection ();</span>
}
</pre>
</div> <!-- end type CngPropertyCollection -->
<div> <!-- start type CngPropertyOptions -->
<h3>New Type System.Security.Cryptography.CngPropertyOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CngPropertyOptions {
	<span class='added added-field ' data-is-non-breaking="">CustomProperty = 1073741824,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Persist = -2147483648,</span>
}
</pre>
</div> <!-- end type CngPropertyOptions -->
<div> <!-- start type CngProvider -->
<h3>New Type System.Security.Cryptography.CngProvider</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class CngProvider : System.IEquatable&lt;CngProvider&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngProvider (string provider);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static CngProvider MicrosoftSmartCardKeyStorageProvider { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngProvider MicrosoftSoftwareKeyStorageProvider { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Provider { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (CngProvider other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (CngProvider left, CngProvider right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (CngProvider left, CngProvider right);</span>
}
</pre>
</div> <!-- end type CngProvider -->
<div> <!-- start type CngUIPolicy -->
<h3>New Type System.Security.Cryptography.CngUIPolicy</h3>
<pre class='added' data-is-non-breaking="">
public sealed class CngUIPolicy {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CngUIPolicy (CngUIProtectionLevels protectionLevel);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CngUIPolicy (CngUIProtectionLevels protectionLevel, string friendlyName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CngUIPolicy (CngUIProtectionLevels protectionLevel, string friendlyName, string description);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CngUIPolicy (CngUIProtectionLevels protectionLevel, string friendlyName, string description, string useContext);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CngUIPolicy (CngUIProtectionLevels protectionLevel, string friendlyName, string description, string useContext, string creationTitle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string CreationTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Description { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string FriendlyName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngUIProtectionLevels ProtectionLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string UseContext { get; }</span>
}
</pre>
</div> <!-- end type CngUIPolicy -->
<div> <!-- start type CngUIProtectionLevels -->
<h3>New Type System.Security.Cryptography.CngUIProtectionLevels</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CngUIProtectionLevels {
	<span class='added added-field ' data-is-non-breaking="">ForceHighProtection = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ProtectKey = 1,</span>
}
</pre>
</div> <!-- end type CngUIProtectionLevels -->
<div> <!-- start type ECDsaCng -->
<h3>New Type System.Security.Cryptography.ECDsaCng</h3>
<pre class='added' data-is-non-breaking="">
public sealed class ECDsaCng : System.Security.Cryptography.ECDsa, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ECDsaCng ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override byte[] SignHash (byte[] hash);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool VerifyHash (byte[] hash, byte[] signature);</span>
}
</pre>
</div> <!-- end type ECDsaCng -->
<div> <!-- start type RSACng -->
<h3>New Type System.Security.Cryptography.RSACng</h3>
<pre class='added' data-is-non-breaking="">
public sealed class RSACng : System.Security.Cryptography.RSA, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RSACng ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override RSAParameters ExportParameters (bool includePrivateParameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void ImportParameters (RSAParameters parameters);</span>
}
</pre>
</div> <!-- end type RSACng -->
<div> <!-- start type TripleDESCng -->
<h3>New Type System.Security.Cryptography.TripleDESCng</h3>
<pre class='added' data-is-non-breaking="">
public sealed class TripleDESCng : System.Security.Cryptography.TripleDES, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TripleDESCng ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TripleDESCng (string keyName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TripleDESCng (string keyName, CngProvider provider);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TripleDESCng (string keyName, CngProvider provider, CngKeyOpenOptions openOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override byte[] Key { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override int KeySize { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override ICryptoTransform CreateDecryptor ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override ICryptoTransform CreateDecryptor (byte[] rgbKey, byte[] rgbIV);</span>
	<span class='added added-method ' data-is-non-breaking="">public override ICryptoTransform CreateEncryptor ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override ICryptoTransform CreateEncryptor (byte[] rgbKey, byte[] rgbIV);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void GenerateIV ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override void GenerateKey ();</span>
}
</pre>
</div> <!-- end type TripleDESCng -->

</div> <!-- end namespace System.Security.Cryptography -->
<!-- start namespace System.IO.Pipes --> <div> 
<h2>New Namespace System.IO.Pipes</h2>

<div> <!-- start type AnonymousPipeClientStream -->
<h3>New Type System.IO.Pipes.AnonymousPipeClientStream</h3>
<pre class='added' data-is-non-breaking="">
public sealed class AnonymousPipeClientStream : System.IO.Pipes.PipeStream, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeClientStream (string pipeHandleAsString);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeClientStream (PipeDirection direction, Microsoft.Win32.SafeHandles.SafePipeHandle safePipeHandle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeClientStream (PipeDirection direction, string pipeHandleAsString);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override PipeTransmissionMode ReadMode { set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override PipeTransmissionMode TransmissionMode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void ~AnonymousPipeClientStream ();</span>
}
</pre>
</div> <!-- end type AnonymousPipeClientStream -->
<div> <!-- start type AnonymousPipeServerStream -->
<h3>New Type System.IO.Pipes.AnonymousPipeServerStream</h3>
<pre class='added' data-is-non-breaking="">
public sealed class AnonymousPipeServerStream : System.IO.Pipes.PipeStream, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeServerStream ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeServerStream (PipeDirection direction);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeServerStream (PipeDirection direction, System.IO.HandleInheritability inheritability);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeServerStream (PipeDirection direction, Microsoft.Win32.SafeHandles.SafePipeHandle serverSafePipeHandle, Microsoft.Win32.SafeHandles.SafePipeHandle clientSafePipeHandle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeServerStream (PipeDirection direction, System.IO.HandleInheritability inheritability, int bufferSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafePipeHandle ClientSafePipeHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override PipeTransmissionMode ReadMode { set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override PipeTransmissionMode TransmissionMode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void DisposeLocalCopyOfClientHandle ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string GetClientHandleAsString ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~AnonymousPipeServerStream ();</span>
}
</pre>
</div> <!-- end type AnonymousPipeServerStream -->
<div> <!-- start type NamedPipeClientStream -->
<h3>New Type System.IO.Pipes.NamedPipeClientStream</h3>
<pre class='added' data-is-non-breaking="">
public sealed class NamedPipeClientStream : System.IO.Pipes.PipeStream, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeClientStream (string pipeName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeClientStream (string serverName, string pipeName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeClientStream (string serverName, string pipeName, PipeDirection direction);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeClientStream (PipeDirection direction, bool isAsync, bool isConnected, Microsoft.Win32.SafeHandles.SafePipeHandle safePipeHandle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeClientStream (string serverName, string pipeName, PipeDirection direction, PipeOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeClientStream (string serverName, string pipeName, PipeDirection direction, PipeOptions options, System.Security.Principal.TokenImpersonationLevel impersonationLevel);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeClientStream (string serverName, string pipeName, PipeDirection direction, PipeOptions options, System.Security.Principal.TokenImpersonationLevel impersonationLevel, System.IO.HandleInheritability inheritability);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int NumberOfServerInstances { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Connect ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Connect (int timeout);</span>
}
</pre>
</div> <!-- end type NamedPipeClientStream -->
<div> <!-- start type NamedPipeServerStream -->
<h3>New Type System.IO.Pipes.NamedPipeServerStream</h3>
<pre class='added' data-is-non-breaking="">
public sealed class NamedPipeServerStream : System.IO.Pipes.PipeStream, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName, PipeDirection direction);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName, PipeDirection direction, int maxNumberOfServerInstances);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (PipeDirection direction, bool isAsync, bool isConnected, Microsoft.Win32.SafeHandles.SafePipeHandle safePipeHandle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName, PipeDirection direction, int maxNumberOfServerInstances, PipeTransmissionMode transmissionMode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName, PipeDirection direction, int maxNumberOfServerInstances, PipeTransmissionMode transmissionMode, PipeOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName, PipeDirection direction, int maxNumberOfServerInstances, PipeTransmissionMode transmissionMode, PipeOptions options, int inBufferSize, int outBufferSize);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int MaxAllowedServerInstances;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Disconnect ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string GetImpersonationUserName ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void WaitForConnection ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~NamedPipeServerStream ();</span>
}
</pre>
</div> <!-- end type NamedPipeServerStream -->
<div> <!-- start type PipeDirection -->
<h3>New Type System.IO.Pipes.PipeDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PipeDirection {
	<span class='added added-field ' data-is-non-breaking="">In = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InOut = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Out = 2,</span>
}
</pre>
</div> <!-- end type PipeDirection -->
<div> <!-- start type PipeOptions -->
<h3>New Type System.IO.Pipes.PipeOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PipeOptions {
	<span class='added added-field ' data-is-non-breaking="">Asynchronous = 1073741824,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteThrough = -2147483648,</span>
}
</pre>
</div> <!-- end type PipeOptions -->
<div> <!-- start type PipeStream -->
<h3>New Type System.IO.Pipes.PipeStream</h3>
<pre class='added' data-is-non-breaking="">
public abstract class PipeStream : System.IO.Stream, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PipeStream (PipeDirection direction, int bufferSize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PipeStream (PipeDirection direction, PipeTransmissionMode transmissionMode, int outBufferSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override bool CanRead { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override bool CanSeek { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override bool CanWrite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int InBufferSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsAsync { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool IsConnected { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsMessageComplete { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override long Length { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int OutBufferSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override long Position { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PipeTransmissionMode ReadMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafePipeHandle SafePipeHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PipeTransmissionMode TransmissionMode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void Flush ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override int Read (byte[] buffer, int offset, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int ReadByte ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override long Seek (long offset, System.IO.SeekOrigin origin);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void SetLength (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void Write (byte[] buffer, int offset, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void WriteByte (byte value);</span>
}
</pre>
</div> <!-- end type PipeStream -->
<div> <!-- start type PipeTransmissionMode -->
<h3>New Type System.IO.Pipes.PipeTransmissionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PipeTransmissionMode {
	<span class='added added-field ' data-is-non-breaking="">Byte = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Message = 1,</span>
}
</pre>
</div> <!-- end type PipeTransmissionMode -->
</div> <!-- end namespace System.IO.Pipes -->

<!-- start namespace System.Security.Cryptography.X509Certificates --> <div> 
<h2>New Namespace System.Security.Cryptography.X509Certificates</h2>

<div> <!-- start type ECDsaCertificateExtensions -->
<h3>New Type System.Security.Cryptography.X509Certificates.ECDsaCertificateExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class ECDsaCertificateExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static System.Security.Cryptography.ECDsa GetECDsaPrivateKey (X509Certificate2 certificate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Security.Cryptography.ECDsa GetECDsaPublicKey (X509Certificate2 certificate);</span>
}
</pre>
</div> <!-- end type ECDsaCertificateExtensions -->
<div> <!-- start type RSACertificateExtensions -->
<h3>New Type System.Security.Cryptography.X509Certificates.RSACertificateExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class RSACertificateExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static System.Security.Cryptography.RSA GetRSAPrivateKey (X509Certificate2 certificate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Security.Cryptography.RSA GetRSAPublicKey (X509Certificate2 certificate);</span>
}
</pre>
</div> <!-- end type RSACertificateExtensions -->
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
</script><h1 id='diff/xi/2.1/System.Numerics.html'>System.Numerics.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Numerics --> <div> 
<h2>Namespace System.Numerics</h2>
<div> <!-- start type Matrix3x2 -->
<h3>New Type System.Numerics.Matrix3x2</h3>
<pre class='added' data-is-non-breaking="">
public struct Matrix3x2, System.IEquatable&lt;Matrix3x2&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Matrix3x2 (float m11, float m12, float m21, float m22, float m31, float m32);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float M11;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M12;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M21;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M22;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M31;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M32;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Matrix3x2 Identity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsIdentity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector2 Translation { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 Add (Matrix3x2 value1, Matrix3x2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateRotation (float radians);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateRotation (float radians, Vector2 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateScale (Vector2 scales);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateScale (float scale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateScale (Vector2 scales, Vector2 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateScale (float scale, Vector2 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateScale (float xScale, float yScale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateScale (float xScale, float yScale, Vector2 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateSkew (float radiansX, float radiansY);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateSkew (float radiansX, float radiansY, Vector2 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateTranslation (Vector2 position);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 CreateTranslation (float xPosition, float yPosition);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (Matrix3x2 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public float GetDeterminant ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Invert (Matrix3x2 matrix, out Matrix3x2 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 Lerp (Matrix3x2 matrix1, Matrix3x2 matrix2, float amount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 Multiply (Matrix3x2 value1, Matrix3x2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 Multiply (Matrix3x2 value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 Negate (Matrix3x2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 Subtract (Matrix3x2 value1, Matrix3x2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 op_Addition (Matrix3x2 value1, Matrix3x2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Matrix3x2 value1, Matrix3x2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Matrix3x2 value1, Matrix3x2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 op_Multiply (Matrix3x2 value1, Matrix3x2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 op_Multiply (Matrix3x2 value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 op_Subtraction (Matrix3x2 value1, Matrix3x2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3x2 op_UnaryNegation (Matrix3x2 value);</span>
}
</pre>
</div> <!-- end type Matrix3x2 -->
<div> <!-- start type Matrix4x4 -->
<h3>New Type System.Numerics.Matrix4x4</h3>
<pre class='added' data-is-non-breaking="">
public struct Matrix4x4, System.IEquatable&lt;Matrix4x4&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Matrix4x4 (Matrix3x2 value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Matrix4x4 (float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float M11;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M12;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M13;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M14;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M21;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M22;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M23;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M24;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M31;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M32;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M33;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M34;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M41;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M42;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M43;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M44;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Matrix4x4 Identity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsIdentity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector3 Translation { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 Add (Matrix4x4 value1, Matrix4x4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateBillboard (Vector3 objectPosition, Vector3 cameraPosition, Vector3 cameraUpVector, Vector3 cameraForwardVector);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateConstrainedBillboard (Vector3 objectPosition, Vector3 cameraPosition, Vector3 rotateAxis, Vector3 cameraForwardVector, Vector3 objectForwardVector);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateFromAxisAngle (Vector3 axis, float angle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateFromQuaternion (Quaternion quaternion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateFromYawPitchRoll (float yaw, float pitch, float roll);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateLookAt (Vector3 cameraPosition, Vector3 cameraTarget, Vector3 cameraUpVector);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateOrthographic (float width, float height, float zNearPlane, float zFarPlane);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateOrthographicOffCenter (float left, float right, float bottom, float top, float zNearPlane, float zFarPlane);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreatePerspective (float width, float height, float nearPlaneDistance, float farPlaneDistance);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreatePerspectiveFieldOfView (float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreatePerspectiveOffCenter (float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateReflection (Plane value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateRotationX (float radians);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateRotationX (float radians, Vector3 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateRotationY (float radians);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateRotationY (float radians, Vector3 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateRotationZ (float radians);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateRotationZ (float radians, Vector3 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateScale (Vector3 scales);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateScale (float scale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateScale (Vector3 scales, Vector3 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateScale (float scale, Vector3 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateScale (float xScale, float yScale, float zScale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateScale (float xScale, float yScale, float zScale, Vector3 centerPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateShadow (Vector3 lightDirection, Plane plane);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateTranslation (Vector3 position);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateTranslation (float xPosition, float yPosition, float zPosition);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 CreateWorld (Vector3 position, Vector3 forward, Vector3 up);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Decompose (Matrix4x4 matrix, out Vector3 scale, out Quaternion rotation, out Vector3 translation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (Matrix4x4 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public float GetDeterminant ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Invert (Matrix4x4 matrix, out Matrix4x4 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 Lerp (Matrix4x4 matrix1, Matrix4x4 matrix2, float amount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 Multiply (Matrix4x4 value1, Matrix4x4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 Multiply (Matrix4x4 value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 Negate (Matrix4x4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 Subtract (Matrix4x4 value1, Matrix4x4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 Transform (Matrix4x4 value, Quaternion rotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 Transpose (Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 op_Addition (Matrix4x4 value1, Matrix4x4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Matrix4x4 value1, Matrix4x4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Matrix4x4 value1, Matrix4x4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 op_Multiply (Matrix4x4 value1, Matrix4x4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 op_Multiply (Matrix4x4 value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 op_Subtraction (Matrix4x4 value1, Matrix4x4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4x4 op_UnaryNegation (Matrix4x4 value);</span>
}
</pre>
</div> <!-- end type Matrix4x4 -->
<div> <!-- start type Plane -->
<h3>New Type System.Numerics.Plane</h3>
<pre class='added' data-is-non-breaking="">
public struct Plane, System.IEquatable&lt;Plane&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Plane (Vector4 value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Plane (Vector3 normal, float d);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Plane (float x, float y, float z, float d);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float D;</span>
	<span class='added added-field ' data-is-non-breaking="">public Vector3 Normal;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Plane CreateFromVertices (Vector3 point1, Vector3 point2, Vector3 point3);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float Dot (Plane plane, Vector4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float DotCoordinate (Plane plane, Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float DotNormal (Plane plane, Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (Plane other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Plane Normalize (Plane value);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Plane Transform (Plane plane, Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Plane Transform (Plane plane, Quaternion rotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Plane value1, Plane value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Plane value1, Plane value2);</span>
}
</pre>
</div> <!-- end type Plane -->
<div> <!-- start type Quaternion -->
<h3>New Type System.Numerics.Quaternion</h3>
<pre class='added' data-is-non-breaking="">
public struct Quaternion, System.IEquatable&lt;Quaternion&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Quaternion (Vector3 vectorPart, float scalarPart);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Quaternion (float x, float y, float z, float w);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float W;</span>
	<span class='added added-field ' data-is-non-breaking="">public float X;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Z;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Quaternion Identity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsIdentity { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Add (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Concatenate (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Conjugate (Quaternion value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion CreateFromAxisAngle (Vector3 axis, float angle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion CreateFromRotationMatrix (Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion CreateFromYawPitchRoll (float yaw, float pitch, float roll);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Divide (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float Dot (Quaternion quaternion1, Quaternion quaternion2);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (Quaternion other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Inverse (Quaternion value);</span>
	<span class='added added-method ' data-is-non-breaking="">public float Length ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float LengthSquared ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Lerp (Quaternion quaternion1, Quaternion quaternion2, float amount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Multiply (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Multiply (Quaternion value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Negate (Quaternion value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Normalize (Quaternion value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Slerp (Quaternion quaternion1, Quaternion quaternion2, float amount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion Subtract (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion op_Addition (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion op_Division (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion op_Multiply (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion op_Multiply (Quaternion value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion op_Subtraction (Quaternion value1, Quaternion value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Quaternion op_UnaryNegation (Quaternion value);</span>
}
</pre>
</div> <!-- end type Quaternion -->
<div> <!-- start type Vector2 -->
<h3>New Type System.Numerics.Vector2</h3>
<pre class='added' data-is-non-breaking="">
public struct Vector2, System.IEquatable&lt;Vector2&gt;, System.IFormattable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Vector2 (float value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Vector2 (float x, float y);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float X;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Y;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Vector2 One { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector2 UnitX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector2 UnitY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector2 Zero { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Abs (Vector2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Add (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Clamp (Vector2 value1, Vector2 min, Vector2 max);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (float[] array);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (float[] array, int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float Distance (Vector2 value1, Vector2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float DistanceSquared (Vector2 value1, Vector2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Divide (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Divide (Vector2 left, float divisor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float Dot (Vector2 value1, Vector2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (Vector2 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float Length ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float LengthSquared ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Lerp (Vector2 value1, Vector2 value2, float amount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Max (Vector2 value1, Vector2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Min (Vector2 value1, Vector2 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Multiply (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Multiply (Vector2 left, float right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Multiply (float left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Negate (Vector2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Normalize (Vector2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Reflect (Vector2 vector, Vector2 normal);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 SquareRoot (Vector2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Subtract (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string ToString (string format);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (string format, System.IFormatProvider formatProvider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Transform (Vector2 position, Matrix3x2 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Transform (Vector2 position, Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 Transform (Vector2 value, Quaternion rotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 TransformNormal (Vector2 normal, Matrix3x2 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 TransformNormal (Vector2 normal, Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 op_Addition (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 op_Division (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 op_Division (Vector2 value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 op_Multiply (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 op_Multiply (Vector2 left, float right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 op_Multiply (float left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 op_Subtraction (Vector2 left, Vector2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector2 op_UnaryNegation (Vector2 value);</span>
}
</pre>
</div> <!-- end type Vector2 -->
<div> <!-- start type Vector3 -->
<h3>New Type System.Numerics.Vector3</h3>
<pre class='added' data-is-non-breaking="">
public struct Vector3, System.IEquatable&lt;Vector3&gt;, System.IFormattable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Vector3 (float value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Vector3 (Vector2 value, float z);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Vector3 (float x, float y, float z);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float X;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Z;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Vector3 One { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector3 UnitX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector3 UnitY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector3 UnitZ { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector3 Zero { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Abs (Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Add (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Clamp (Vector3 value1, Vector3 min, Vector3 max);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (float[] array);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (float[] array, int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Cross (Vector3 vector1, Vector3 vector2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float Distance (Vector3 value1, Vector3 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float DistanceSquared (Vector3 value1, Vector3 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Divide (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Divide (Vector3 left, float divisor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float Dot (Vector3 vector1, Vector3 vector2);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (Vector3 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float Length ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float LengthSquared ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Lerp (Vector3 value1, Vector3 value2, float amount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Max (Vector3 value1, Vector3 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Min (Vector3 value1, Vector3 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Multiply (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Multiply (Vector3 left, float right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Multiply (float left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Negate (Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Normalize (Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Reflect (Vector3 vector, Vector3 normal);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 SquareRoot (Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Subtract (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string ToString (string format);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (string format, System.IFormatProvider formatProvider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Transform (Vector3 position, Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 Transform (Vector3 value, Quaternion rotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 TransformNormal (Vector3 normal, Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_Addition (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_Division (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_Division (Vector3 value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_Multiply (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_Multiply (Vector3 left, float right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_Multiply (float left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_Subtraction (Vector3 left, Vector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_UnaryNegation (Vector3 value);</span>
}
</pre>
</div> <!-- end type Vector3 -->
<div> <!-- start type Vector4 -->
<h3>New Type System.Numerics.Vector4</h3>
<pre class='added' data-is-non-breaking="">
public struct Vector4, System.IEquatable&lt;Vector4&gt;, System.IFormattable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Vector4 (float value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Vector4 (Vector3 value, float w);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Vector4 (Vector2 value, float z, float w);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Vector4 (float x, float y, float z, float w);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float W;</span>
	<span class='added added-field ' data-is-non-breaking="">public float X;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Z;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Vector4 One { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector4 UnitW { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector4 UnitX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector4 UnitY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector4 UnitZ { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Vector4 Zero { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Abs (Vector4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Add (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Clamp (Vector4 value1, Vector4 min, Vector4 max);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (float[] array);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (float[] array, int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float Distance (Vector4 value1, Vector4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float DistanceSquared (Vector4 value1, Vector4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Divide (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Divide (Vector4 left, float divisor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static float Dot (Vector4 vector1, Vector4 vector2);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (Vector4 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float Length ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float LengthSquared ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Lerp (Vector4 value1, Vector4 value2, float amount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Max (Vector4 value1, Vector4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Min (Vector4 value1, Vector4 value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Multiply (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Multiply (Vector4 left, float right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Multiply (float left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Negate (Vector4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Normalize (Vector4 vector);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 SquareRoot (Vector4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Subtract (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string ToString (string format);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (string format, System.IFormatProvider formatProvider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Transform (Vector2 position, Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Transform (Vector2 value, Quaternion rotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Transform (Vector3 position, Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Transform (Vector3 value, Quaternion rotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Transform (Vector4 vector, Matrix4x4 matrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 Transform (Vector4 value, Quaternion rotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 op_Addition (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 op_Division (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 op_Division (Vector4 value1, float value2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 op_Multiply (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 op_Multiply (Vector4 left, float right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 op_Multiply (float left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 op_Subtraction (Vector4 left, Vector4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector4 op_UnaryNegation (Vector4 value);</span>
}
</pre>
</div> <!-- end type Vector4 -->

</div> <!-- end namespace System.Numerics -->
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
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public virtual final object this [int <span class='removed removed-inline removed-breaking-inline'>index</span> <span class='added '>ordinal</span>] { get; }
</div><div data-is-breaking="">	public virtual final object this [string <span class='removed removed-inline removed-breaking-inline'>index</span> <span class='added '>name</span>] { get; }
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual final bool GetBoolean (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final byte GetByte (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final long GetBytes (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>, long fieldOffset, byte[] buffer, int <span class='removed removed-inline '>bufferoffset</span> <span class='added '>bufferOffset</span>, int length)
</div><div data-is-non-breaking="">	public virtual final char GetChar (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final long GetChars (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>, long <span class='removed removed-inline '>fieldoffset</span> <span class='added '>fieldOffset</span>, char[] buffer, int <span class='removed removed-inline '>bufferoffset</span> <span class='added '>bufferOffset</span>, int length)
</div><div data-is-non-breaking="">	public virtual final System.Data.IDataReader GetData (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final string GetDataTypeName (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final System.DateTime GetDateTime (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final System.Decimal GetDecimal (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final double GetDouble (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final System.Type GetFieldType (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final float GetFloat (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final System.Guid GetGuid (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final short GetInt16 (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final int GetInt32 (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final long GetInt64 (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final string GetName (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final string GetString (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final object GetValue (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div><div data-is-non-breaking="">	public virtual final bool IsDBNull (int <span class='removed removed-inline '>i</span> <span class='added '>ordinal</span>)
</div></pre>

</div> <!-- end type SqlDataRecord -->

</div> <!-- end namespace Microsoft.SqlServer.Server -->
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
<!-- start type BasicHttpsBinding --> <div>
<h3>Type Changed: System.ServiceModel.BasicHttpsBinding</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public BasicHttpsSecurity Security { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type BasicHttpsBinding -->
<!-- start type BasicHttpsSecurity --> <div>
<h3>Type Changed: System.ServiceModel.BasicHttpsSecurity</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public HttpTransportSecurity Transport { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type BasicHttpsSecurity -->
<!-- start type HttpBindingBase --> <div>
<h3>Type Changed: System.ServiceModel.HttpBindingBase</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>override</span> string Scheme { get; }
</div></pre>

</div> <!-- end type HttpBindingBase -->
<div> <!-- start type CallbackBehaviorAttribute -->
<h3>New Type System.ServiceModel.CallbackBehaviorAttribute</h3>
<pre class='added' data-is-non-breaking="">
public sealed class CallbackBehaviorAttribute : System.Attribute, Description.IEndpointBehavior {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CallbackBehaviorAttribute ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool AutomaticSessionShutdown { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ConcurrencyMode ConcurrencyMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IgnoreExtensionDataObject { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IncludeExceptionDetailInFaults { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxItemsInObjectGraph { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string TransactionTimeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool UseSynchronizationContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool ValidateMustUnderstand { get; set; }</span>
}
</pre>
</div> <!-- end type CallbackBehaviorAttribute -->
<div> <!-- start type DnsEndpointIdentity -->
<h3>New Type System.ServiceModel.DnsEndpointIdentity</h3>
<pre class='added' data-is-non-breaking="">
public class DnsEndpointIdentity : System.ServiceModel.EndpointIdentity {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DnsEndpointIdentity (string dns);</span>
}
</pre>
</div> <!-- end type DnsEndpointIdentity -->
<div> <!-- start type DuplexChannelFactory`1 -->
<h3>New Type System.ServiceModel.DuplexChannelFactory`1</h3>
<pre class='added' data-is-non-breaking="">
public class DuplexChannelFactory`1 : System.ServiceModel.ChannelFactory`1[TChannel], System.IDisposable, Channels.IChannelFactory, System.ServiceModel.Channels.IChannelFactory&lt;TChannel&gt;, ICommunicationObject {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (object callbackInstance);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (InstanceContext callbackInstance);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (System.Type callbackInstanceType);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (object callbackInstance, Channels.Binding binding);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (object callbackInstance, Description.ServiceEndpoint endpoint);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (object callbackInstance, string endpointConfigurationName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (InstanceContext callbackInstance, Channels.Binding binding);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (InstanceContext callbackInstance, Description.ServiceEndpoint endpoint);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (InstanceContext callbackInstance, string endpointConfigurationName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (System.Type callbackInstanceType, Channels.Binding binding);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (System.Type callbackInstanceType, Description.ServiceEndpoint endpoint);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (System.Type callbackInstanceType, string endpointConfigurationName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (object callbackInstance, Channels.Binding binding, EndpointAddress remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (object callbackInstance, Channels.Binding binding, string remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (object callbackInstance, string endpointConfigurationName, EndpointAddress remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (InstanceContext callbackInstance, Channels.Binding binding, EndpointAddress remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (InstanceContext callbackInstance, Channels.Binding binding, string remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (InstanceContext callbackInstance, string endpointConfigurationName, EndpointAddress remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (System.Type callbackInstanceType, Channels.Binding binding, EndpointAddress remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (System.Type callbackInstanceType, Channels.Binding binding, string remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public DuplexChannelFactory`1 (System.Type callbackInstanceType, string endpointConfigurationName, EndpointAddress remoteAddress);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public TChannel CreateChannel (InstanceContext callbackInstance);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TChannel CreateChannel (object callbackObject, string endpointConfigurationName);</span>
	<span class='added added-method ' data-is-non-breaking="">public override TChannel CreateChannel (EndpointAddress address, System.Uri via);</span>
	<span class='added added-method ' data-is-non-breaking="">public TChannel CreateChannel (InstanceContext callbackInstance, EndpointAddress address);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TChannel CreateChannel (InstanceContext callbackInstance, string endpointConfigurationName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TChannel CreateChannel (object callbackObject, Channels.Binding binding, EndpointAddress endpointAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TChannel CreateChannel (InstanceContext callbackInstance, Channels.Binding binding, EndpointAddress endpointAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual TChannel CreateChannel (InstanceContext callbackInstance, EndpointAddress address, System.Uri via);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TChannel CreateChannel (object callbackObject, Channels.Binding binding, EndpointAddress endpointAddress, System.Uri via);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TChannel CreateChannel (InstanceContext callbackInstance, Channels.Binding binding, EndpointAddress endpointAddress, System.Uri via);</span>
}
</pre>
</div> <!-- end type DuplexChannelFactory`1 -->
<div> <!-- start type DuplexClientBase`1 -->
<h3>New Type System.ServiceModel.DuplexClientBase`1</h3>
<pre class='added' data-is-non-breaking="">
public class DuplexClientBase`1 : System.ServiceModel.ClientBase`1[TChannel], System.IDisposable, ICommunicationObject {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (object instance);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (InstanceContext instance);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (object instance, Description.ServiceEndpoint endpoint);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (object instance, string configurationName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (InstanceContext instance, Description.ServiceEndpoint endpoint);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (InstanceContext instance, string configurationName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (object instance, Channels.Binding binding, EndpointAddress address);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (object instance, string bindingConfigurationName, EndpointAddress address);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (object instance, string endpointConfigurationName, string remoteAddress);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (InstanceContext instance, Channels.Binding binding, EndpointAddress address);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (InstanceContext instance, string configurationName, EndpointAddress address);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DuplexClientBase`1 (InstanceContext instance, string endpointConfigurationName, string remoteAddress);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public IDuplexContextChannel InnerDuplexChannel { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override TChannel CreateChannel ();</span>
}
</pre>
</div> <!-- end type DuplexClientBase`1 -->
<div> <!-- start type IDuplexContextChannel -->
<h3>New Type System.ServiceModel.IDuplexContextChannel</h3>
<pre class='added' data-is-non-breaking="">
public interface IDuplexContextChannel : Channels.IChannel, ICommunicationObject, IContextChannel, System.ServiceModel.IExtensibleObject&lt;IContextChannel&gt; {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticInputSessionShutdown { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual InstanceContext CallbackInstance { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginCloseOutputSession (System.TimeSpan timeout, System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CloseOutputSession (System.TimeSpan timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndCloseOutputSession (System.IAsyncResult result);</span>
}
</pre>
</div> <!-- end type IDuplexContextChannel -->
<div> <!-- start type MessageSecurityOverTcp -->
<h3>New Type System.ServiceModel.MessageSecurityOverTcp</h3>
<pre class='added' data-is-non-breaking="">
public sealed class MessageSecurityOverTcp {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public MessageCredentialType ClientCredentialType { get; set; }</span>
}
</pre>
</div> <!-- end type MessageSecurityOverTcp -->
<div> <!-- start type MessageSecurityVersion -->
<h3>New Type System.ServiceModel.MessageSecurityVersion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MessageSecurityVersion {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Security.BasicSecurityProfileVersion BasicSecurityProfileVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessageSecurityVersion Default { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Security.SecureConversationVersion SecureConversationVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Security.SecurityPolicyVersion SecurityPolicyVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Security.SecurityVersion SecurityVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Security.TrustVersion TrustVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessageSecurityVersion WSSecurity10WSTrust13WSSecureConversation13WSSecurityPolicy12BasicSecurityProfile10 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessageSecurityVersion WSSecurity10WSTrustFebruary2005WSSecureConversationFebruary2005WSSecurityPolicy11BasicSecurityProfile10 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessageSecurityVersion WSSecurity11WSTrust13WSSecureConversation13WSSecurityPolicy12 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessageSecurityVersion WSSecurity11WSTrust13WSSecureConversation13WSSecurityPolicy12BasicSecurityProfile10 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessageSecurityVersion WSSecurity11WSTrustFebruary2005WSSecureConversationFebruary2005WSSecurityPolicy11 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessageSecurityVersion WSSecurity11WSTrustFebruary2005WSSecureConversationFebruary2005WSSecurityPolicy11BasicSecurityProfile10 { get; }</span>
}
</pre>
</div> <!-- end type MessageSecurityVersion -->
<div> <!-- start type NetHttpsBinding -->
<h3>New Type System.ServiceModel.NetHttpsBinding</h3>
<pre class='added' data-is-non-breaking="">
public class NetHttpsBinding : System.ServiceModel.HttpBindingBase, Channels.IBindingRuntimePreferences, IDefaultCommunicationTimeouts {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NetHttpsBinding ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NetHttpsBinding (BasicHttpsSecurityMode securityMode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NetHttpsBinding (string configurationName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NetHttpsBinding (BasicHttpsSecurityMode securityMode, bool reliableSessionEnabled);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NetHttpMessageEncoding MessageEncoding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OptionalReliableSession ReliableSession { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Scheme { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public BasicHttpsSecurity Security { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Channels.WebSocketTransportSettings WebSocketSettings { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override Channels.BindingElementCollection CreateBindingElements ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool ShouldSerializeReliableSession ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool ShouldSerializeSecurity ();</span>
}
</pre>
</div> <!-- end type NetHttpsBinding -->
<div> <!-- start type NetTcpBinding -->
<h3>New Type System.ServiceModel.NetTcpBinding</h3>
<pre class='added' data-is-non-breaking="">
public class NetTcpBinding : System.ServiceModel.Channels.Binding, Channels.IBindingRuntimePreferences, IDefaultCommunicationTimeouts {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NetTcpBinding ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NetTcpBinding (SecurityMode securityMode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NetTcpBinding (string configurationName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NetTcpBinding (SecurityMode securityMode, bool reliableSessionEnabled);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public EnvelopeVersion EnvelopeVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HostNameComparisonMode HostNameComparisonMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int ListenBacklog { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long MaxBufferPoolSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxBufferSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxConnections { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long MaxReceivedMessageSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool PortSharingEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Xml.XmlDictionaryReaderQuotas ReaderQuotas { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OptionalReliableSession ReliableSession { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Scheme { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NetTcpSecurity Security { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool TransactionFlow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public TransferMode TransferMode { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override Channels.BindingElementCollection CreateBindingElements ();</span>
}
</pre>
</div> <!-- end type NetTcpBinding -->
<div> <!-- start type NetTcpSecurity -->
<h3>New Type System.ServiceModel.NetTcpSecurity</h3>
<pre class='added' data-is-non-breaking="">
public sealed class NetTcpSecurity {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NetTcpSecurity ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public MessageSecurityOverTcp Message { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SecurityMode Mode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public TcpTransportSecurity Transport { get; set; }</span>
}
</pre>
</div> <!-- end type NetTcpSecurity -->
<div> <!-- start type SpnEndpointIdentity -->
<h3>New Type System.ServiceModel.SpnEndpointIdentity</h3>
<pre class='added' data-is-non-breaking="">
public class SpnEndpointIdentity : System.ServiceModel.EndpointIdentity {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SpnEndpointIdentity (string spn);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static System.TimeSpan SpnLookupTime { get; set; }</span>
}
</pre>
</div> <!-- end type SpnEndpointIdentity -->
<div> <!-- start type TcpTransportSecurity -->
<h3>New Type System.ServiceModel.TcpTransportSecurity</h3>
<pre class='added' data-is-non-breaking="">
public sealed class TcpTransportSecurity {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TcpTransportSecurity ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public TcpClientCredentialType ClientCredentialType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Net.Security.ProtectionLevel ProtectionLevel { get; set; }</span>
}
</pre>
</div> <!-- end type TcpTransportSecurity -->
<div> <!-- start type UpnEndpointIdentity -->
<h3>New Type System.ServiceModel.UpnEndpointIdentity</h3>
<pre class='added' data-is-non-breaking="">
public class UpnEndpointIdentity : System.ServiceModel.EndpointIdentity {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UpnEndpointIdentity (string upn);</span>
}
</pre>
</div> <!-- end type UpnEndpointIdentity -->

</div> <!-- end namespace System.ServiceModel -->
<!-- start namespace System.ServiceModel.Channels --> <div> 
<h2>Namespace System.ServiceModel.Channels</h2>
<!-- start type TransportBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.TransportBindingElement</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>virtual</span> bool ManualAddressing { get; set; }
</div></pre>

</div> <!-- end type TransportBindingElement -->
<div> <!-- start type ConnectionOrientedTransportBindingElement -->
<h3>New Type System.ServiceModel.Channels.ConnectionOrientedTransportBindingElement</h3>
<pre class='added' data-is-non-breaking="">
public abstract class ConnectionOrientedTransportBindingElement : System.ServiceModel.Channels.TransportBindingElement, System.ServiceModel.Description.IPolicyExportExtension, System.ServiceModel.Description.IWsdlExportExtension {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan ChannelInitializationTimeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int ConnectionBufferSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.HostNameComparisonMode HostNameComparisonMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxBufferSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan MaxOutputDelay { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxPendingAccepts { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxPendingConnections { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.TransferMode TransferMode { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool CanBuildChannelFactory&lt;TChannel&gt; (BindingContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public override T GetProperty&lt;T&gt; (BindingContext context);</span>
}
</pre>
</div> <!-- end type ConnectionOrientedTransportBindingElement -->
<div> <!-- start type SslStreamSecurityBindingElement -->
<h3>New Type System.ServiceModel.Channels.SslStreamSecurityBindingElement</h3>
<pre class='added' data-is-non-breaking="">
public class SslStreamSecurityBindingElement : System.ServiceModel.Channels.BindingElement, ITransportTokenAssertionProvider, System.ServiceModel.Description.IPolicyExportExtension {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SslStreamSecurityBindingElement ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool RequireClientCertificate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override System.ServiceModel.Channels.IChannelFactory&lt;TChannel&gt; BuildChannelFactory&lt;TChannel&gt; (BindingContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool CanBuildChannelFactory&lt;TChannel&gt; (BindingContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public override BindingElement Clone ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override T GetProperty&lt;T&gt; (BindingContext context);</span>
}
</pre>
</div> <!-- end type SslStreamSecurityBindingElement -->
<div> <!-- start type TcpConnectionPoolSettings -->
<h3>New Type System.ServiceModel.Channels.TcpConnectionPoolSettings</h3>
<pre class='added' data-is-non-breaking="">
public sealed class TcpConnectionPoolSettings {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string GroupName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan IdleTimeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan LeaseTimeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxOutboundConnectionsPerEndpoint { get; set; }</span>
}
</pre>
</div> <!-- end type TcpConnectionPoolSettings -->
<div> <!-- start type TcpTransportBindingElement -->
<h3>New Type System.ServiceModel.Channels.TcpTransportBindingElement</h3>
<pre class='added' data-is-non-breaking="">
public class TcpTransportBindingElement : System.ServiceModel.Channels.ConnectionOrientedTransportBindingElement, System.ServiceModel.Description.IPolicyExportExtension, System.ServiceModel.Description.IWsdlExportExtension {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TcpTransportBindingElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TcpTransportBindingElement (TcpTransportBindingElement other);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public TcpConnectionPoolSettings ConnectionPoolSettings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int ListenBacklog { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool PortSharingEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Scheme { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool TeredoEnabled { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override System.ServiceModel.Channels.IChannelFactory&lt;TChannel&gt; BuildChannelFactory&lt;TChannel&gt; (BindingContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public override BindingElement Clone ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override T GetProperty&lt;T&gt; (BindingContext context);</span>
}
</pre>
</div> <!-- end type TcpTransportBindingElement -->
<div> <!-- start type WindowsStreamSecurityBindingElement -->
<h3>New Type System.ServiceModel.Channels.WindowsStreamSecurityBindingElement</h3>
<pre class='added' data-is-non-breaking="">
public class WindowsStreamSecurityBindingElement : System.ServiceModel.Channels.BindingElement, ISecurityCapabilities, ITransportTokenAssertionProvider, System.ServiceModel.Description.IPolicyExportExtension {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WindowsStreamSecurityBindingElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public WindowsStreamSecurityBindingElement (WindowsStreamSecurityBindingElement other);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Net.Security.ProtectionLevel ProtectionLevel { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override System.ServiceModel.Channels.IChannelFactory&lt;TChannel&gt; BuildChannelFactory&lt;TChannel&gt; (BindingContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool CanBuildChannelFactory&lt;TChannel&gt; (BindingContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public override BindingElement Clone ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override T GetProperty&lt;T&gt; (BindingContext context);</span>
}
</pre>
</div> <!-- end type WindowsStreamSecurityBindingElement -->

</div> <!-- end namespace System.ServiceModel.Channels -->
<!-- start namespace System.ServiceModel.Security --> <div> 
<h2>Namespace System.ServiceModel.Security</h2>
<div> <!-- start type BasicSecurityProfileVersion -->
<h3>New Type System.ServiceModel.Security.BasicSecurityProfileVersion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class BasicSecurityProfileVersion {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static BasicSecurityProfileVersion BasicSecurityProfile10 { get; }</span>
}
</pre>
</div> <!-- end type BasicSecurityProfileVersion -->
<div> <!-- start type SecureConversationVersion -->
<h3>New Type System.ServiceModel.Security.SecureConversationVersion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class SecureConversationVersion {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SecureConversationVersion ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static SecureConversationVersion Default { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Xml.XmlDictionaryString Namespace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Xml.XmlDictionaryString Prefix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SecureConversationVersion WSSecureConversation13 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SecureConversationVersion WSSecureConversationFeb2005 { get; }</span>
}
</pre>
</div> <!-- end type SecureConversationVersion -->
<div> <!-- start type SecurityPolicyVersion -->
<h3>New Type System.ServiceModel.Security.SecurityPolicyVersion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class SecurityPolicyVersion {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SecurityPolicyVersion ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Namespace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Prefix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SecurityPolicyVersion WSSecurityPolicy11 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SecurityPolicyVersion WSSecurityPolicy12 { get; }</span>
}
</pre>
</div> <!-- end type SecurityPolicyVersion -->
<div> <!-- start type SecurityVersion -->
<h3>New Type System.ServiceModel.Security.SecurityVersion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class SecurityVersion {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SecurityVersion ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static SecurityVersion WSSecurity10 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SecurityVersion WSSecurity11 { get; }</span>
}
</pre>
</div> <!-- end type SecurityVersion -->
<div> <!-- start type TrustVersion -->
<h3>New Type System.ServiceModel.Security.TrustVersion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class TrustVersion {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected TrustVersion ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static TrustVersion Default { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Xml.XmlDictionaryString Namespace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Xml.XmlDictionaryString Prefix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static TrustVersion WSTrust13 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static TrustVersion WSTrustFeb2005 { get; }</span>
}
</pre>
</div> <!-- end type TrustVersion -->

</div> <!-- end namespace System.ServiceModel.Security -->
<!-- start namespace System.ServiceModel.Security.Tokens --> <div> 
<h2>Namespace System.ServiceModel.Security.Tokens</h2>
<div> <!-- start type SecureConversationSecurityTokenParameters -->
<h3>New Type System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters</h3>
<pre class='added' data-is-non-breaking="">
public class SecureConversationSecurityTokenParameters : System.ServiceModel.Security.Tokens.SecurityTokenParameters {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SecureConversationSecurityTokenParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecureConversationSecurityTokenParameters (System.ServiceModel.Channels.SecurityBindingElement element);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SecureConversationSecurityTokenParameters (SecureConversationSecurityTokenParameters source);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecureConversationSecurityTokenParameters (System.ServiceModel.Channels.SecurityBindingElement element, bool requireCancellation);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Channels.SecurityBindingElement BootstrapSecurityBindingElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override bool HasAsymmetricKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool RequireCancellation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override bool SupportsClientAuthentication { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override bool SupportsClientWindowsIdentity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override bool SupportsServerAuthentication { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override SecurityTokenParameters CloneCore ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type SecureConversationSecurityTokenParameters -->
<div> <!-- start type SecurityTokenParameters -->
<h3>New Type System.ServiceModel.Security.Tokens.SecurityTokenParameters</h3>
<pre class='added' data-is-non-breaking="">
public abstract class SecurityTokenParameters {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SecurityTokenParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SecurityTokenParameters (SecurityTokenParameters other);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">protected virtual bool HasAsymmetricKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SecurityTokenInclusionMode InclusionMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SecurityTokenReferenceStyle ReferenceStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool RequireDerivedKeys { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual bool SupportsClientAuthentication { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual bool SupportsClientWindowsIdentity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual bool SupportsServerAuthentication { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public SecurityTokenParameters Clone ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual SecurityTokenParameters CloneCore ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type SecurityTokenParameters -->
<div> <!-- start type SecurityTokenReferenceStyle -->
<h3>New Type System.ServiceModel.Security.Tokens.SecurityTokenReferenceStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SecurityTokenReferenceStyle {
	<span class='added added-field ' data-is-non-breaking="">External = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Internal = 0,</span>
}
</pre>
</div> <!-- end type SecurityTokenReferenceStyle -->
<div> <!-- start type SupportingTokenParameters -->
<h3>New Type System.ServiceModel.Security.Tokens.SupportingTokenParameters</h3>
<pre class='added' data-is-non-breaking="">
public class SupportingTokenParameters {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SupportingTokenParameters ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.ObjectModel.Collection&lt;SecurityTokenParameters&gt; Endorsing { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.ObjectModel.Collection&lt;SecurityTokenParameters&gt; Signed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.ObjectModel.Collection&lt;SecurityTokenParameters&gt; SignedEncrypted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.ObjectModel.Collection&lt;SecurityTokenParameters&gt; SignedEndorsing { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public SupportingTokenParameters Clone ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetKeyDerivation (bool requireDerivedKeys);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type SupportingTokenParameters -->
<div> <!-- start type UserNameSecurityTokenParameters -->
<h3>New Type System.ServiceModel.Security.Tokens.UserNameSecurityTokenParameters</h3>
<pre class='added' data-is-non-breaking="">
public class UserNameSecurityTokenParameters : System.ServiceModel.Security.Tokens.SecurityTokenParameters {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UserNameSecurityTokenParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UserNameSecurityTokenParameters (UserNameSecurityTokenParameters source);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">protected override bool HasAsymmetricKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override bool SupportsClientAuthentication { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override bool SupportsClientWindowsIdentity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override bool SupportsServerAuthentication { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override SecurityTokenParameters CloneCore ();</span>
}
</pre>
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
</script><h1 id='diff/xi/2.1/System.IO.Compression.html'>System.IO.Compression.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.IO.Compression --> <div> 
<h2>Namespace System.IO.Compression</h2>
<!-- start type ZipArchiveEntry --> <div>
<h3>Type Changed: System.IO.Compression.ZipArchiveEntry</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type ZipArchiveEntry -->

</div> <!-- end namespace System.IO.Compression -->
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
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"9.8.0"</span> <span class='added '>"9.8.2"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace MonoTouch -->
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
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"9.8.0"</span> <span class='added '>"9.8.2"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
</div>



   


 <hr>
