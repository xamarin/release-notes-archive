---
id: 85BA894A-B7AA-4568-A027-4F4DFE4D624D
title: "iOS 10.2.1 to 10.4.0"
---

# API diff

 [mscorlib.dll](#diff/xi/Xamarin.iOS/mscorlib.html)

   


 [System.dll](#diff/xi/Xamarin.iOS/System.html)

   


 [System.Core.dll](#diff/xi/Xamarin.iOS/System.Core.html)

   


 [System.Data.dll](#diff/xi/Xamarin.iOS/System.Data.html)

   


 [System.Runtime.Serialization.dll](#diff/xi/Xamarin.iOS/System.Runtime.Serialization.html)

   


 [System.Xml.dll](#diff/xi/Xamarin.iOS/System.Xml.html)

   


 [Mono.Security.dll](#diff/xi/Xamarin.iOS/Mono.Security.html)

   


 [MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.iOS/MonoTouch.NUnitLite.html)

   


 [System.Net.Http.dll](#diff/xi/Xamarin.iOS/System.Net.Http.html)

   


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
<!-- start namespace Mono --> <div> 
<h2>Namespace Mono</h2>
<!-- start type Runtime --> <div>
<h3>Type Changed: Mono.Runtime</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void InstallSignalHandlers ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveSignalHandlers ();</span>
</pre>
</div>

</div> <!-- end type Runtime -->

</div> <!-- end namespace Mono -->
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type AppDomain --> <div>
<h3>Type Changed: System.AppDomain</h3>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event ResolveEventHandler ReflectionOnlyAssemblyResolve;</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use AppDomainSetup.DynamicBase")]
	public void SetDynamicBase (string path);</span>
</pre>
</div>

</div> <!-- end type AppDomain -->
<!-- start type ContextBoundObject --> <div>
<h3>Type Changed: System.ContextBoundObject</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>System.MarshalByRefObject</span>

</div> <!-- end type ContextBoundObject -->
<!-- start type Environment --> <div>
<h3>Type Changed: System.Environment</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string SystemDirectory { get; }</span>
</pre>
</div>

</div> <!-- end type Environment -->
<!-- start type GC --> <div>
<h3>Type Changed: System.GC</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void Collect (int generation, GCCollectionMode mode, bool blocking, bool compacting);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void EndNoGCRegion ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryStartNoGCRegion (long totalSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryStartNoGCRegion (long totalSize, bool disallowFullBlockingGC);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryStartNoGCRegion (long totalSize, long lohSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryStartNoGCRegion (long totalSize, long lohSize, bool disallowFullBlockingGC);</span>
</pre>
</div>

</div> <!-- end type GC -->

</div> <!-- end namespace System -->
<!-- start namespace System.Diagnostics.Tracing --> <div> 
<h2>Namespace System.Diagnostics.Tracing</h2>
<!-- start type EventSourceException --> <div>
<h3>Type Changed: System.Diagnostics.Tracing.EventSourceException</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected EventSourceException (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);</span>
</pre>
</div>

</div> <!-- end type EventSourceException -->
<div> <!-- start type EventCounter -->
<h3>New Type System.Diagnostics.Tracing.EventCounter</h3>
<pre class='added' data-is-non-breaking="">
public class EventCounter {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EventCounter (string name, EventSource eventSource);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void WriteMetric (float value);</span>
}
</pre>
</div> <!-- end type EventCounter -->

</div> <!-- end namespace System.Diagnostics.Tracing -->
<!-- start namespace System.Globalization --> <div> 
<h2>Namespace System.Globalization</h2>
<!-- start type CompareInfo --> <div>
<h3>Type Changed: System.Globalization.CompareInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public SortVersion Version { get; }</span>
</pre>
</div>

</div> <!-- end type CompareInfo -->
<!-- start type CultureInfo --> <div>
<h3>Type Changed: System.Globalization.CultureInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CultureTypes CultureTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string IetfLanguageTag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int KeyboardLayoutId { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CultureInfo GetConsoleFallbackUICulture ();</span>
</pre>
</div>

</div> <!-- end type CultureInfo -->

</div> <!-- end namespace System.Globalization -->
<!-- start namespace System.IO --> <div> 
<h2>Namespace System.IO</h2>
<!-- start type File --> <div>
<h3>Type Changed: System.IO.File</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static FileStream Create (string path, int bufferSize, FileOptions options, System.Security.AccessControl.FileSecurity fileSecurity);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Security.AccessControl.FileSecurity GetAccessControl (string path);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Security.AccessControl.FileSecurity GetAccessControl (string path, System.Security.AccessControl.AccessControlSections includeSections);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessControl (string path, System.Security.AccessControl.FileSecurity fileSecurity);</span>
</pre>
</div>

</div> <!-- end type File -->
<!-- start type FileInfo --> <div>
<h3>Type Changed: System.IO.FileInfo</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Security.AccessControl.FileSecurity GetAccessControl ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Security.AccessControl.FileSecurity GetAccessControl (System.Security.AccessControl.AccessControlSections includeSections);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAccessControl (System.Security.AccessControl.FileSecurity fileSecurity);</span>
</pre>
</div>

</div> <!-- end type FileInfo -->
<!-- start type FileStream --> <div>
<h3>Type Changed: System.IO.FileStream</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public FileStream (string path, FileMode mode, System.Security.AccessControl.FileSystemRights rights, FileShare share, int bufferSize, FileOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public FileStream (string path, FileMode mode, System.Security.AccessControl.FileSystemRights rights, FileShare share, int bufferSize, FileOptions options, System.Security.AccessControl.FileSecurity fileSecurity);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Security.AccessControl.FileSecurity GetAccessControl ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAccessControl (System.Security.AccessControl.FileSecurity fileSecurity);</span>
</pre>
</div>

</div> <!-- end type FileStream -->
<!-- start type FileSystemInfo --> <div>
<h3>Type Changed: System.IO.FileSystemInfo</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>System.MarshalByRefObject</span>

</div> <!-- end type FileSystemInfo -->
<!-- start type Stream --> <div>
<h3>Type Changed: System.IO.Stream</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>System.MarshalByRefObject</span>

</div> <!-- end type Stream -->
<!-- start type TextReader --> <div>
<h3>Type Changed: System.IO.TextReader</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>System.MarshalByRefObject</span>

</div> <!-- end type TextReader -->
<!-- start type TextWriter --> <div>
<h3>Type Changed: System.IO.TextWriter</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>System.MarshalByRefObject</span>

</div> <!-- end type TextWriter -->

</div> <!-- end namespace System.IO -->
<!-- start namespace System.Reflection --> <div> 
<h2>Namespace System.Reflection</h2>
<!-- start type Assembly --> <div>
<h3>Type Changed: System.Reflection.Assembly</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.Runtime.Serialization.ISerializable</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.SecurityRuleSet SecurityRuleSet { get; }</span>
</pre>
</div>

</div> <!-- end type Assembly -->
<!-- start type TargetException --> <div>
<h3>Type Changed: System.Reflection.TargetException</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Exception</span> <span class='added '>System.ApplicationException</span>

</div> <!-- end type TargetException -->
<!-- start type TargetInvocationException --> <div>
<h3>Type Changed: System.Reflection.TargetInvocationException</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Exception</span> <span class='added '>System.ApplicationException</span>

</div> <!-- end type TargetInvocationException -->
<!-- start type TargetParameterCountException --> <div>
<h3>Type Changed: System.Reflection.TargetParameterCountException</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Exception</span> <span class='added '>System.ApplicationException</span>

</div> <!-- end type TargetParameterCountException -->

</div> <!-- end namespace System.Reflection -->
<!-- start namespace System.Reflection.Emit --> <div> 
<h2>Namespace System.Reflection.Emit</h2>
<div> <!-- start type AssemblyBuilder -->
<h3>New Type System.Reflection.Emit.AssemblyBuilder</h3>
<pre class='added' data-is-non-breaking="">
public class AssemblyBuilder : System.Reflection.Assembly, System.Reflection.ICustomAttributeProvider, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AssemblyBuilder ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AssemblyBuilder DefineDynamicAssembly (System.Reflection.AssemblyName name, AssemblyBuilderAccess access);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AssemblyBuilder DefineDynamicAssembly (System.Reflection.AssemblyName name, AssemblyBuilderAccess access, System.Collections.Generic.IEnumerable&lt;CustomAttributeBuilder&gt; assemblyAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public ModuleBuilder DefineDynamicModule (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public ModuleBuilder GetDynamicModule (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
}
</pre>
</div> <!-- end type AssemblyBuilder -->
<div> <!-- start type AssemblyBuilderAccess -->
<h3>New Type System.Reflection.Emit.AssemblyBuilderAccess</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum AssemblyBuilderAccess {
	<span class='added added-field ' data-is-non-breaking="">ReflectionOnly = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Run = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RunAndCollect = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">RunAndSave = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Save = 2,</span>
}
</pre>
</div> <!-- end type AssemblyBuilderAccess -->
<div> <!-- start type ConstructorBuilder -->
<h3>New Type System.Reflection.Emit.ConstructorBuilder</h3>
<pre class='added' data-is-non-breaking="">
public abstract class ConstructorBuilder : System.Reflection.ConstructorInfo, System.Reflection.ICustomAttributeProvider, System.Runtime.InteropServices._MemberInfo, System.Runtime.InteropServices._MethodBase {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ConstructorBuilder ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.MethodAttributes Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type DeclaringType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool InitLocals { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public ParameterBuilder DefineParameter (int iSequence, System.Reflection.ParameterAttributes attributes, string strParamName);</span>
	<span class='added added-method ' data-is-non-breaking="">public ILGenerator GetILGenerator ();</span>
	<span class='added added-method ' data-is-non-breaking="">public ILGenerator GetILGenerator (int streamSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Reflection.ParameterInfo[] GetParameters ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetImplementationFlags (System.Reflection.MethodImplAttributes attributes);</span>
}
</pre>
</div> <!-- end type ConstructorBuilder -->
<div> <!-- start type CustomAttributeBuilder -->
<h3>New Type System.Reflection.Emit.CustomAttributeBuilder</h3>
<pre class='added' data-is-non-breaking="">
public class CustomAttributeBuilder {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CustomAttributeBuilder (System.Reflection.ConstructorInfo con, object[] constructorArgs);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CustomAttributeBuilder (System.Reflection.ConstructorInfo con, object[] constructorArgs, System.Reflection.FieldInfo[] namedFields, object[] fieldValues);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CustomAttributeBuilder (System.Reflection.ConstructorInfo con, object[] constructorArgs, System.Reflection.PropertyInfo[] namedProperties, object[] propertyValues);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CustomAttributeBuilder (System.Reflection.ConstructorInfo con, object[] constructorArgs, System.Reflection.PropertyInfo[] namedProperties, object[] propertyValues, System.Reflection.FieldInfo[] namedFields, object[] fieldValues);</span>
}
</pre>
</div> <!-- end type CustomAttributeBuilder -->
<div> <!-- start type EnumBuilder -->
<h3>New Type System.Reflection.Emit.EnumBuilder</h3>
<pre class='added' data-is-non-breaking="">
public abstract class EnumBuilder : System.Reflection.TypeInfo, System.Reflection.ICustomAttributeProvider, System.Reflection.IReflect, System.Reflection.IReflectableType, System.Runtime.InteropServices._MemberInfo, System.Runtime.InteropServices._Type {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected EnumBuilder ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.Assembly Assembly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string AssemblyQualifiedName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type BaseType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string FullName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Guid GUID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.Module Module { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Namespace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public FieldBuilder UnderlyingField { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public System.Reflection.TypeInfo CreateTypeInfo ();</span>
	<span class='added added-method ' data-is-non-breaking="">public FieldBuilder DefineLiteral (string literalName, object literalValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Type GetElementType ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
}
</pre>
</div> <!-- end type EnumBuilder -->
<div> <!-- start type EventBuilder -->
<h3>New Type System.Reflection.Emit.EventBuilder</h3>
<pre class='added' data-is-non-breaking="">
public class EventBuilder {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EventBuilder ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AddOtherMethod (MethodBuilder mdBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAddOnMethod (MethodBuilder mdBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetRaiseMethod (MethodBuilder mdBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetRemoveOnMethod (MethodBuilder mdBuilder);</span>
}
</pre>
</div> <!-- end type EventBuilder -->
<div> <!-- start type FieldBuilder -->
<h3>New Type System.Reflection.Emit.FieldBuilder</h3>
<pre class='added' data-is-non-breaking="">
public abstract class FieldBuilder : System.Reflection.FieldInfo, System.Reflection.ICustomAttributeProvider, System.Runtime.InteropServices._MemberInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected FieldBuilder ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.FieldAttributes Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type DeclaringType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type FieldType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override object GetValue (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetConstant (object defaultValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetOffset (int iOffset);</span>
}
</pre>
</div> <!-- end type FieldBuilder -->
<div> <!-- start type GenericTypeParameterBuilder -->
<h3>New Type System.Reflection.Emit.GenericTypeParameterBuilder</h3>
<pre class='added' data-is-non-breaking="">
public abstract class GenericTypeParameterBuilder : System.Reflection.TypeInfo, System.Reflection.ICustomAttributeProvider, System.Reflection.IReflect, System.Reflection.IReflectableType, System.Runtime.InteropServices._MemberInfo, System.Runtime.InteropServices._Type {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GenericTypeParameterBuilder ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.Assembly Assembly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string AssemblyQualifiedName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type BaseType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string FullName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Guid GUID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.Module Module { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Namespace { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override System.Type GetElementType ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetBaseTypeConstraint (System.Type baseTypeConstraint);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetGenericParameterAttributes (System.Reflection.GenericParameterAttributes genericParameterAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetInterfaceConstraints (System.Type[] interfaceConstraints);</span>
}
</pre>
</div> <!-- end type GenericTypeParameterBuilder -->
<div> <!-- start type ILGenerator -->
<h3>New Type System.Reflection.Emit.ILGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class ILGenerator {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int ILOffset { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginCatchBlock (System.Type exceptionType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginExceptFilterBlock ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Label BeginExceptionBlock ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginFaultBlock ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginFinallyBlock ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginScope ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual LocalBuilder DeclareLocal (System.Type localType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual LocalBuilder DeclareLocal (System.Type localType, bool pinned);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Label DefineLabel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, byte arg);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, double arg);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, short arg);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, int arg);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, long arg);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, System.Reflection.ConstructorInfo con);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, Label label);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, Label[] labels);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, LocalBuilder local);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, SignatureHelper signature);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, System.Reflection.FieldInfo field);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, System.Reflection.MethodInfo meth);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Emit (OpCode opcode, sbyte arg);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, float arg);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, string str);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Emit (OpCode opcode, System.Type cls);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EmitCall (OpCode opcode, System.Reflection.MethodInfo methodInfo, System.Type[] optionalParameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EmitCalli (OpCode opcode, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] parameterTypes, System.Type[] optionalParameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EmitWriteLine (LocalBuilder localBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EmitWriteLine (System.Reflection.FieldInfo fld);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EmitWriteLine (string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndExceptionBlock ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndScope ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MarkLabel (Label loc);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ThrowException (System.Type excType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UsingNamespace (string usingNamespace);</span>
}
</pre>
</div> <!-- end type ILGenerator -->
<div> <!-- start type Label -->
<h3>New Type System.Reflection.Emit.Label</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public struct Label {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (Label obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Label a, Label b);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Label a, Label b);</span>
}
</pre>
</div> <!-- end type Label -->
<div> <!-- start type LocalBuilder -->
<h3>New Type System.Reflection.Emit.LocalBuilder</h3>
<pre class='added' data-is-non-breaking="">
public sealed class LocalBuilder : System.Reflection.LocalVariableInfo {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override bool IsPinned { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override int LocalIndex { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type LocalType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void SetLocalSymInfo (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetLocalSymInfo (string name, int startOffset, int endOffset);</span>
}
</pre>
</div> <!-- end type LocalBuilder -->
<div> <!-- start type MethodBuilder -->
<h3>New Type System.Reflection.Emit.MethodBuilder</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MethodBuilder : System.Reflection.MethodInfo, System.Reflection.ICustomAttributeProvider, System.Runtime.InteropServices._MemberInfo, System.Runtime.InteropServices._MethodBase {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MethodBuilder ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.MethodAttributes Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type DeclaringType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool InitLocals { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public GenericTypeParameterBuilder[] DefineGenericParameters (string[] names);</span>
	<span class='added added-method ' data-is-non-breaking="">public ParameterBuilder DefineParameter (int position, System.Reflection.ParameterAttributes attributes, string strParamName);</span>
	<span class='added added-method ' data-is-non-breaking="">public ILGenerator GetILGenerator ();</span>
	<span class='added added-method ' data-is-non-breaking="">public ILGenerator GetILGenerator (int size);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Reflection.ParameterInfo[] GetParameters ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetImplementationFlags (System.Reflection.MethodImplAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetParameters (System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetReturnType (System.Type returnType);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetSignature (System.Type returnType, System.Type[] returnTypeRequiredCustomModifiers, System.Type[] returnTypeOptionalCustomModifiers, System.Type[] parameterTypes, System.Type[][] parameterTypeRequiredCustomModifiers, System.Type[][] parameterTypeOptionalCustomModifiers);</span>
}
</pre>
</div> <!-- end type MethodBuilder -->
<div> <!-- start type ModuleBuilder -->
<h3>New Type System.Reflection.Emit.ModuleBuilder</h3>
<pre class='added' data-is-non-breaking="">
public abstract class ModuleBuilder : System.Reflection.Module, System.Reflection.ICustomAttributeProvider, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ModuleBuilder ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void CreateGlobalFunctions ();</span>
	<span class='added added-method ' data-is-non-breaking="">public EnumBuilder DefineEnum (string name, System.Reflection.TypeAttributes visibility, System.Type underlyingType);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodBuilder DefineGlobalMethod (string name, System.Reflection.MethodAttributes attributes, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodBuilder DefineGlobalMethod (string name, System.Reflection.MethodAttributes attributes, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodBuilder DefineGlobalMethod (string name, System.Reflection.MethodAttributes attributes, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] requiredReturnTypeCustomModifiers, System.Type[] optionalReturnTypeCustomModifiers, System.Type[] parameterTypes, System.Type[][] requiredParameterTypeCustomModifiers, System.Type[][] optionalParameterTypeCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public FieldBuilder DefineInitializedData (string name, byte[] data, System.Reflection.FieldAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineType (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineType (string name, System.Reflection.TypeAttributes attr);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineType (string name, System.Reflection.TypeAttributes attr, System.Type parent);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineType (string name, System.Reflection.TypeAttributes attr, System.Type parent, int typesize);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineType (string name, System.Reflection.TypeAttributes attr, System.Type parent, PackingSize packsize);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineType (string name, System.Reflection.TypeAttributes attr, System.Type parent, System.Type[] interfaces);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineType (string name, System.Reflection.TypeAttributes attr, System.Type parent, PackingSize packingSize, int typesize);</span>
	<span class='added added-method ' data-is-non-breaking="">public FieldBuilder DefineUninitializedData (string name, int size, System.Reflection.FieldAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Reflection.MethodInfo GetArrayMethod (System.Type arrayClass, string methodName, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
}
</pre>
</div> <!-- end type ModuleBuilder -->
<div> <!-- start type ParameterBuilder -->
<h3>New Type System.Reflection.Emit.ParameterBuilder</h3>
<pre class='added' data-is-non-breaking="">
public class ParameterBuilder {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsIn { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsOptional { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsOut { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Position { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetConstant (object defaultValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
}
</pre>
</div> <!-- end type ParameterBuilder -->
<div> <!-- start type PropertyBuilder -->
<h3>New Type System.Reflection.Emit.PropertyBuilder</h3>
<pre class='added' data-is-non-breaking="">
public abstract class PropertyBuilder : System.Reflection.PropertyInfo, System.Reflection.ICustomAttributeProvider, System.Runtime.InteropServices._MemberInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PropertyBuilder ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.PropertyAttributes Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override bool CanRead { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override bool CanWrite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type DeclaringType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type PropertyType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AddOtherMethod (MethodBuilder mdBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Reflection.ParameterInfo[] GetIndexParameters ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetConstant (object defaultValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetGetMethod (MethodBuilder mdBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetSetMethod (MethodBuilder mdBuilder);</span>
}
</pre>
</div> <!-- end type PropertyBuilder -->
<div> <!-- start type SignatureHelper -->
<h3>New Type System.Reflection.Emit.SignatureHelper</h3>
<pre class='added' data-is-non-breaking="">
public class SignatureHelper {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AddArgument (System.Type clsArgument);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddArgument (System.Type argument, bool pinned);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddArgument (System.Type argument, System.Type[] requiredCustomModifiers, System.Type[] optionalCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddArguments (System.Type[] arguments, System.Type[][] requiredCustomModifiers, System.Type[][] optionalCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddSentinel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetFieldSigHelper (System.Reflection.Module mod);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetLocalVarSigHelper ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetLocalVarSigHelper (System.Reflection.Module mod);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetMethodSigHelper (System.Reflection.CallingConventions callingConvention, System.Type returnType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetMethodSigHelper (System.Reflection.Module mod, System.Reflection.CallingConventions callingConvention, System.Type returnType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetMethodSigHelper (System.Reflection.Module mod, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetPropertySigHelper (System.Reflection.Module mod, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetPropertySigHelper (System.Reflection.Module mod, System.Type returnType, System.Type[] requiredReturnTypeCustomModifiers, System.Type[] optionalReturnTypeCustomModifiers, System.Type[] parameterTypes, System.Type[][] requiredParameterTypeCustomModifiers, System.Type[][] optionalParameterTypeCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SignatureHelper GetPropertySigHelper (System.Reflection.Module mod, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] requiredReturnTypeCustomModifiers, System.Type[] optionalReturnTypeCustomModifiers, System.Type[] parameterTypes, System.Type[][] requiredParameterTypeCustomModifiers, System.Type[][] optionalParameterTypeCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] GetSignature ();</span>
}
</pre>
</div> <!-- end type SignatureHelper -->
<div> <!-- start type TypeBuilder -->
<h3>New Type System.Reflection.Emit.TypeBuilder</h3>
<pre class='added' data-is-non-breaking="">
public abstract class TypeBuilder : System.Reflection.TypeInfo, System.Reflection.ICustomAttributeProvider, System.Reflection.IReflect, System.Reflection.IReflectableType, System.Runtime.InteropServices._MemberInfo, System.Runtime.InteropServices._Type {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected TypeBuilder ();</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int UnspecifiedTypeSize;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.Assembly Assembly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string AssemblyQualifiedName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Type BaseType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string FullName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Guid GUID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override System.Reflection.Module Module { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override string Namespace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PackingSize PackingSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Size { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AddInterfaceImplementation (System.Type interfaceType);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Reflection.TypeInfo CreateTypeInfo ();</span>
	<span class='added added-method ' data-is-non-breaking="">public ConstructorBuilder DefineConstructor (System.Reflection.MethodAttributes attributes, System.Reflection.CallingConventions callingConvention, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public ConstructorBuilder DefineConstructor (System.Reflection.MethodAttributes attributes, System.Reflection.CallingConventions callingConvention, System.Type[] parameterTypes, System.Type[][] requiredCustomModifiers, System.Type[][] optionalCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public ConstructorBuilder DefineDefaultConstructor (System.Reflection.MethodAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public EventBuilder DefineEvent (string name, System.Reflection.EventAttributes attributes, System.Type eventtype);</span>
	<span class='added added-method ' data-is-non-breaking="">public FieldBuilder DefineField (string fieldName, System.Type type, System.Reflection.FieldAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public FieldBuilder DefineField (string fieldName, System.Type type, System.Type[] requiredCustomModifiers, System.Type[] optionalCustomModifiers, System.Reflection.FieldAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public GenericTypeParameterBuilder[] DefineGenericParameters (string[] names);</span>
	<span class='added added-method ' data-is-non-breaking="">public FieldBuilder DefineInitializedData (string name, byte[] data, System.Reflection.FieldAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodBuilder DefineMethod (string name, System.Reflection.MethodAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodBuilder DefineMethod (string name, System.Reflection.MethodAttributes attributes, System.Reflection.CallingConventions callingConvention);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodBuilder DefineMethod (string name, System.Reflection.MethodAttributes attributes, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodBuilder DefineMethod (string name, System.Reflection.MethodAttributes attributes, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public MethodBuilder DefineMethod (string name, System.Reflection.MethodAttributes attributes, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] returnTypeRequiredCustomModifiers, System.Type[] returnTypeOptionalCustomModifiers, System.Type[] parameterTypes, System.Type[][] parameterTypeRequiredCustomModifiers, System.Type[][] parameterTypeOptionalCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DefineMethodOverride (System.Reflection.MethodInfo methodInfoBody, System.Reflection.MethodInfo methodInfoDeclaration);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineNestedType (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineNestedType (string name, System.Reflection.TypeAttributes attr);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineNestedType (string name, System.Reflection.TypeAttributes attr, System.Type parent);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineNestedType (string name, System.Reflection.TypeAttributes attr, System.Type parent, int typeSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineNestedType (string name, System.Reflection.TypeAttributes attr, System.Type parent, PackingSize packSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineNestedType (string name, System.Reflection.TypeAttributes attr, System.Type parent, System.Type[] interfaces);</span>
	<span class='added added-method ' data-is-non-breaking="">public TypeBuilder DefineNestedType (string name, System.Reflection.TypeAttributes attr, System.Type parent, PackingSize packSize, int typeSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public PropertyBuilder DefineProperty (string name, System.Reflection.PropertyAttributes attributes, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public PropertyBuilder DefineProperty (string name, System.Reflection.PropertyAttributes attributes, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] parameterTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public PropertyBuilder DefineProperty (string name, System.Reflection.PropertyAttributes attributes, System.Type returnType, System.Type[] returnTypeRequiredCustomModifiers, System.Type[] returnTypeOptionalCustomModifiers, System.Type[] parameterTypes, System.Type[][] parameterTypeRequiredCustomModifiers, System.Type[][] parameterTypeOptionalCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public PropertyBuilder DefineProperty (string name, System.Reflection.PropertyAttributes attributes, System.Reflection.CallingConventions callingConvention, System.Type returnType, System.Type[] returnTypeRequiredCustomModifiers, System.Type[] returnTypeOptionalCustomModifiers, System.Type[] parameterTypes, System.Type[][] parameterTypeRequiredCustomModifiers, System.Type[][] parameterTypeOptionalCustomModifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public ConstructorBuilder DefineTypeInitializer ();</span>
	<span class='added added-method ' data-is-non-breaking="">public FieldBuilder DefineUninitializedData (string name, int size, System.Reflection.FieldAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Reflection.ConstructorInfo GetConstructor (System.Type type, System.Reflection.ConstructorInfo constructor);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Type GetElementType ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Reflection.FieldInfo GetField (System.Type type, System.Reflection.FieldInfo field);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Reflection.MethodInfo GetMethod (System.Type type, System.Reflection.MethodInfo method);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool IsCreated ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (CustomAttributeBuilder customBuilder);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCustomAttribute (System.Reflection.ConstructorInfo con, byte[] binaryAttribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetParent (System.Type parent);</span>
}
</pre>
</div> <!-- end type TypeBuilder -->

</div> <!-- end namespace System.Reflection.Emit -->
<!-- start namespace System.Runtime --> <div> 
<h2>Namespace System.Runtime</h2>
<!-- start type GCLatencyMode --> <div>
<h3>Type Changed: System.Runtime.GCLatencyMode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NoGCRegion = 4,</span>
</pre>
</div>

</div> <!-- end type GCLatencyMode -->

</div> <!-- end namespace System.Runtime -->
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<div> <!-- start type IDispatchConstantAttribute -->
<h3>New Type System.Runtime.CompilerServices.IDispatchConstantAttribute</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class IDispatchConstantAttribute : System.Runtime.CompilerServices.CustomConstantAttribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public IDispatchConstantAttribute ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override object Value { get; }</span>
}
</pre>
</div> <!-- end type IDispatchConstantAttribute -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
<!-- start namespace System.Runtime.InteropServices --> <div> 
<h2>Namespace System.Runtime.InteropServices</h2>
<!-- start type Marshal --> <div>
<h3>Type Changed: System.Runtime.InteropServices.Marshal</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr BufferToBSTR (System.Array ptr, int slen);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void CleanupUnusedObjectsInCurrentContext ();</span>
</pre>
</div>

</div> <!-- end type Marshal -->
<!-- start type RuntimeEnvironment --> <div>
<h3>Type Changed: System.Runtime.InteropServices.RuntimeEnvironment</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetRuntimeInterfaceAsIntPtr (System.Guid clsid, System.Guid riid);</span>
	<span class='added added-method ' data-is-non-breaking="">public static object GetRuntimeInterfaceAsObject (System.Guid clsid, System.Guid riid);</span>
</pre>
</div>

</div> <!-- end type RuntimeEnvironment -->
<h3>Removed Type <span class='breaking' data-is-breaking="">System.Runtime.InteropServices.ComAwareEventInfo</span></h3>
</div> <!-- end namespace System.Runtime.InteropServices -->
<!-- start namespace System.Runtime.Serialization.Formatters.Binary --> <div> 
<h2>Namespace System.Runtime.Serialization.Formatters.Binary</h2>
<!-- start type BinaryFormatter --> <div>
<h3>Type Changed: System.Runtime.Serialization.Formatters.Binary.BinaryFormatter</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.Runtime.Remoting.Messaging.IRemotingFormatter</span>
</pre>
</div>

</div> <!-- end type BinaryFormatter -->

</div> <!-- end namespace System.Runtime.Serialization.Formatters.Binary -->
<!-- start namespace System.Security --> <div> 
<h2>Namespace System.Security</h2>
<!-- start type SecurityCriticalAttribute --> <div>
<h3>Type Changed: System.Security.SecurityCriticalAttribute</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SecurityCriticalAttribute (SecurityCriticalScope scope);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">[Obsolete ("SecurityCriticalScope is only used for .NET 2.0 transparency compatibility.")]
	public SecurityCriticalScope Scope { get; }</span>
</pre>
</div>

</div> <!-- end type SecurityCriticalAttribute -->

</div> <!-- end namespace System.Security -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type CryptoConfig --> <div>
<h3>Type Changed: System.Security.Cryptography.CryptoConfig</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void AddAlgorithm (System.Type algorithm, string[] names);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void AddOID (string oid, string[] names);</span>
</pre>
</div>

</div> <!-- end type CryptoConfig -->
<!-- start type DSA --> <div>
<h3>Type Changed: System.Security.Cryptography.DSA</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected virtual byte[] HashData (System.IO.Stream data, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual byte[] HashData (byte[] data, int offset, int count, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] SignData (byte[] data, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual byte[] SignData (System.IO.Stream data, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual byte[] SignData (byte[] data, int offset, int count, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool VerifyData (byte[] data, byte[] signature, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool VerifyData (System.IO.Stream data, byte[] signature, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool VerifyData (byte[] data, int offset, int count, byte[] signature, HashAlgorithmName hashAlgorithm);</span>
</pre>
</div>

</div> <!-- end type DSA -->
<!-- start type RC2CryptoServiceProvider --> <div>
<h3>Type Changed: System.Security.Cryptography.RC2CryptoServiceProvider</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool UseSalt { get; set; }</span>
</pre>
</div>

</div> <!-- end type RC2CryptoServiceProvider -->
<!-- start type RNGCryptoServiceProvider --> <div>
<h3>Type Changed: System.Security.Cryptography.RNGCryptoServiceProvider</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public RNGCryptoServiceProvider (byte[] rgb);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RNGCryptoServiceProvider (CspParameters cspParams);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RNGCryptoServiceProvider (string str);</span>
</pre>
</div>

</div> <!-- end type RNGCryptoServiceProvider -->
<!-- start type RSACryptoServiceProvider --> <div>
<h3>Type Changed: System.Security.Cryptography.RSACryptoServiceProvider</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override byte[] Decrypt (byte[] data, RSAEncryptionPadding padding);</span>
	<span class='added added-method ' data-is-non-breaking="">public override byte[] Encrypt (byte[] data, RSAEncryptionPadding padding);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override byte[] HashData (System.IO.Stream data, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override byte[] HashData (byte[] data, int offset, int count, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public override byte[] SignHash (byte[] hash, HashAlgorithmName hashAlgorithm, RSASignaturePadding padding);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool VerifyHash (byte[] hash, byte[] signature, HashAlgorithmName hashAlgorithm, RSASignaturePadding padding);</span>
</pre>
</div>

</div> <!-- end type RSACryptoServiceProvider -->
<!-- start type Rfc2898DeriveBytes --> <div>
<h3>Type Changed: System.Security.Cryptography.Rfc2898DeriveBytes</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public byte[] CryptDeriveKey (string algname, string alghashname, int keySize, byte[] rgbIV);</span>
</pre>
</div>

</div> <!-- end type Rfc2898DeriveBytes -->
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
<!-- start namespace System.Threading --> <div> 
<h2>Namespace System.Threading</h2>
<!-- start type EventWaitHandle --> <div>
<h3>Type Changed: System.Threading.EventWaitHandle</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">protected override void Dispose (bool explicitDisposing);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Security.AccessControl.EventWaitHandleSecurity GetAccessControl ();</span>
</pre>
</div>

</div> <!-- end type EventWaitHandle -->
<!-- start type Thread --> <div>
<h3>Type Changed: System.Threading.Thread</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void DisableComObjectEagerCleanup ();</span>
</pre>
</div>

</div> <!-- end type Thread -->
<!-- start type ThreadAbortException --> <div>
<h3>Type Changed: System.Threading.ThreadAbortException</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public object ExceptionState { get; }</span>
</pre>
</div>

</div> <!-- end type ThreadAbortException -->

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
</script><h1 id='diff/xi/Xamarin.iOS/System.html'>System.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Microsoft.Win32.SafeHandles --> <div> 
<h2>Namespace Microsoft.Win32.SafeHandles</h2>
<!-- start type SafeX509ChainHandle --> <div>
<h3>Type Changed: Microsoft.Win32.SafeHandles.SafeX509ChainHandle</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Runtime.InteropServices.SafeHandle</span> <span class='added '>Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid</span>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public override bool IsInvalid { get; }</span>
</pre>

</div> <!-- end type SafeX509ChainHandle -->

</div> <!-- end namespace Microsoft.Win32.SafeHandles -->
<!-- start namespace Mono.Security.Interface --> <div> 
<h2>Namespace Mono.Security.Interface</h2>
<!-- start type CertificateValidationHelper --> <div>
<h3>Type Changed: Mono.Security.Interface.CertificateValidationHelper</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static ICertificateValidator GetValidator (MonoTlsSettings settings, MonoTlsProvider provider);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static ICertificateValidator GetValidator (MonoTlsSettings settings);</span>
</pre>
</div>

</div> <!-- end type CertificateValidationHelper -->
<!-- start type MonoTlsConnectionInfo --> <div>
<h3>Type Changed: Mono.Security.Interface.MonoTlsConnectionInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string PeerDomainName { get; set; }</span>
</pre>
</div>

</div> <!-- end type MonoTlsConnectionInfo -->
<!-- start type MonoTlsProviderFactory --> <div>
<h3>Type Changed: Mono.Security.Interface.MonoTlsProviderFactory</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static bool HasProvider { get; }</span>
</pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsInitialized { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ()]
	public static MonoTlsProvider GetDefaultProvider ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ()]
	public static void SetDefaultProvider (string name);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public MonoTlsProvider GetProvider (string <span class='removed removed-inline removed-breaking-inline'>name</span> <span class='added '>provider</span>)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void Initialize ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Initialize (string provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsProviderSupported (string provider);</span>
</pre>
</div>

</div> <!-- end type MonoTlsProviderFactory -->

</div> <!-- end namespace Mono.Security.Interface -->
<!-- start namespace System.Diagnostics --> <div> 
<h2>Namespace System.Diagnostics</h2>
<!-- start type ProcessModuleCollection --> <div>
<h3>Type Changed: System.Diagnostics.ProcessModuleCollection</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Diagnostics.ProcessModuleCollectionBase</span> <span class='added '>System.Collections.ReadOnlyCollectionBase</span>
<p>Removed interfaces:</p>

<pre>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.ICollection&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.IEnumerable&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.IList&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.IReadOnlyCollection&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.IReadOnlyList&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.IList</span>
</pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int Capacity { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Add (ProcessModule item);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void AddRange (System.Collections.Generic.IEnumerable&lt;ProcessModule&gt; collection);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public System.Collections.ObjectModel.ReadOnlyCollection&lt;ProcessModule&gt; AsReadOnly ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int BinarySearch (ProcessModule item);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int BinarySearch (ProcessModule item, System.Collections.Generic.IComparer&lt;ProcessModule&gt; comparer);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int BinarySearch (int index, int count, ProcessModule item, System.Collections.Generic.IComparer&lt;ProcessModule&gt; comparer);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Clear ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public System.Collections.Generic.List&lt;TOutput&gt; ConvertAll&lt;TOutput&gt; (System.Converter&lt;ProcessModule,TOutput&gt; converter);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void CopyTo (ProcessModule[] array);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void CopyTo (int index, ProcessModule[] array, int arrayIndex, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public bool Exists (System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public ProcessModule Find (System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public System.Collections.Generic.List&lt;ProcessModule&gt; FindAll (System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindIndex (System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindIndex (int startIndex, System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindIndex (int startIndex, int count, System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public ProcessModule FindLast (System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindLastIndex (System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindLastIndex (int startIndex, System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindLastIndex (int startIndex, int count, System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void ForEach (System.Action&lt;ProcessModule&gt; action);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public System.Collections.Generic.List&lt;ProcessModule&gt; GetRange (int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int IndexOf (ProcessModule item, int index);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int IndexOf (ProcessModule item, int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Insert (int index, ProcessModule item);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void InsertRange (int index, System.Collections.Generic.IEnumerable&lt;ProcessModule&gt; collection);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int LastIndexOf (ProcessModule item);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int LastIndexOf (ProcessModule item, int index);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int LastIndexOf (ProcessModule item, int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public bool Remove (ProcessModule item);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int RemoveAll (System.Predicate&lt;ProcessModule&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void RemoveAt (int index);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void RemoveRange (int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Reverse ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Reverse (int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Sort ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Sort (System.Collections.Generic.IComparer&lt;ProcessModule&gt; comparer);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Sort (System.Comparison&lt;ProcessModule&gt; comparison);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Sort (int index, int count, System.Collections.Generic.IComparer&lt;ProcessModule&gt; comparer);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public ProcessModule[] ToArray ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void TrimExcess ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public bool TrueForAll (System.Predicate&lt;ProcessModule&gt; match);</span>
</pre>
</div>

</div> <!-- end type ProcessModuleCollection -->
<!-- start type ProcessThreadCollection --> <div>
<h3>Type Changed: System.Diagnostics.ProcessThreadCollection</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Diagnostics.ProcessThreadCollectionBase</span> <span class='added '>System.Collections.ReadOnlyCollectionBase</span>
<p>Removed interfaces:</p>

<pre>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.ICollection&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.IEnumerable&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.IList&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.IReadOnlyCollection&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.Generic.IReadOnlyList&lt;T&gt;</span>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Collections.IList</span>
</pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int Capacity { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void AddRange (System.Collections.Generic.IEnumerable&lt;ProcessThread&gt; collection);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public System.Collections.ObjectModel.ReadOnlyCollection&lt;ProcessThread&gt; AsReadOnly ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int BinarySearch (ProcessThread item);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int BinarySearch (ProcessThread item, System.Collections.Generic.IComparer&lt;ProcessThread&gt; comparer);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int BinarySearch (int index, int count, ProcessThread item, System.Collections.Generic.IComparer&lt;ProcessThread&gt; comparer);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Clear ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public System.Collections.Generic.List&lt;TOutput&gt; ConvertAll&lt;TOutput&gt; (System.Converter&lt;ProcessThread,TOutput&gt; converter);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void CopyTo (ProcessThread[] array);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void CopyTo (int index, ProcessThread[] array, int arrayIndex, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public bool Exists (System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public ProcessThread Find (System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public System.Collections.Generic.List&lt;ProcessThread&gt; FindAll (System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindIndex (System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindIndex (int startIndex, System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindIndex (int startIndex, int count, System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public ProcessThread FindLast (System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindLastIndex (System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindLastIndex (int startIndex, System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int FindLastIndex (int startIndex, int count, System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void ForEach (System.Action&lt;ProcessThread&gt; action);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public System.Collections.Generic.List&lt;ProcessThread&gt; GetRange (int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int IndexOf (ProcessThread item, int index);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int IndexOf (ProcessThread item, int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void InsertRange (int index, System.Collections.Generic.IEnumerable&lt;ProcessThread&gt; collection);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int LastIndexOf (ProcessThread item);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int LastIndexOf (ProcessThread item, int index);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int LastIndexOf (ProcessThread item, int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public int RemoveAll (System.Predicate&lt;ProcessThread&gt; match);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void RemoveAt (int index);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void RemoveRange (int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Reverse ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Reverse (int index, int count);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Sort ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Sort (System.Collections.Generic.IComparer&lt;ProcessThread&gt; comparer);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Sort (System.Comparison&lt;ProcessThread&gt; comparison);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void Sort (int index, int count, System.Collections.Generic.IComparer&lt;ProcessThread&gt; comparer);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public ProcessThread[] ToArray ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public void TrimExcess ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API is no longer available")]
	public bool TrueForAll (System.Predicate&lt;ProcessThread&gt; match);</span>
</pre>
</div>

</div> <!-- end type ProcessThreadCollection -->
<h3>Removed Type <span class='breaking' data-is-breaking="">System.Diagnostics.ProcessModuleCollectionBase</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">System.Diagnostics.ProcessThreadCollectionBase</span></h3>
</div> <!-- end namespace System.Diagnostics -->
<!-- start namespace System.IO --> <div> 
<h2>Namespace System.IO</h2>
<!-- start type FileSystemWatcher --> <div>
<h3>Type Changed: System.IO.FileSystemWatcher</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>System.ComponentModel.Component</span>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.ComponentModel.IComponent</span>
	<span class='added added-interface ' data-is-non-breaking="">System.ComponentModel.ISupportInitialize</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override System.ComponentModel.ISite Site { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ComponentModel.ISynchronizeInvoke SynchronizingObject { get; set; }</span>
</pre>
</div>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	protected <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> void Dispose (bool disposing)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginInit ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInit ();</span>
</pre>
</div>

</div> <!-- end type FileSystemWatcher -->
<div> <!-- start type IODescriptionAttribute -->
<h3>New Type System.IO.IODescriptionAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class IODescriptionAttribute : System.ComponentModel.DescriptionAttribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public IODescriptionAttribute (string description);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override string Description { get; }</span>
}
</pre>
</div> <!-- end type IODescriptionAttribute -->

</div> <!-- end namespace System.IO -->
<!-- start namespace System.Net --> <div> 
<h2>Namespace System.Net</h2>
<!-- start type HttpListener --> <div>
<h3>Type Changed: System.Net.HttpListener</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.ExtendedProtection.ServiceNameCollection DefaultServiceNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy ExtendedProtectionPolicy { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HttpListener.ExtendedProtectionSelector ExtendedProtectionSelectorDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HttpListenerTimeoutManager TimeoutManager { get; }</span>
</pre>
</div>

</div> <!-- end type HttpListener -->
<!-- start type HttpListenerContext --> <div>
<h3>Type Changed: System.Net.HttpListenerContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;WebSockets.HttpListenerWebSocketContext&gt; AcceptWebSocketAsync (string subProtocol, System.TimeSpan keepAliveInterval);</span>
</pre>
</div>

</div> <!-- end type HttpListenerContext -->
<!-- start type HttpListenerTimeoutManager --> <div>
<h3>Type Changed: System.Net.HttpListenerTimeoutManager</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan DrainEntityBody { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan EntityBody { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan HeaderWait { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan IdleConnection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public long MinSendBytesPerSecond { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.TimeSpan RequestQueue { get; set; }</span>
</pre>
</div>

</div> <!-- end type HttpListenerTimeoutManager -->
<!-- start type HttpWebRequest --> <div>
<h3>Type Changed: System.Net.HttpWebRequest</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>virtual</span> bool AllowAutoRedirect { get; set; }
</div><div data-is-non-breaking="">	public <span class='added '>virtual</span> bool AllowWriteStreamBuffering { get; set; }
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.IO.Stream GetRequestStream (TransportContext context);</span>
</pre>
</div>

</div> <!-- end type HttpWebRequest -->
<!-- start type ServicePointManager --> <div>
<h3>Type Changed: System.Net.ServicePointManager</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Security.EncryptionPolicy EncryptionPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool ReusePort { get; set; }</span>
</pre>
</div>

</div> <!-- end type ServicePointManager -->
<!-- start type WebProxy --> <div>
<h3>Type Changed: System.Net.WebProxy</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public WebProxy (string <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>Address</span>)
</div><div data-is-breaking="">	public WebProxy (System.Uri <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>Address</span>)
</div><div data-is-breaking="">	public WebProxy (string <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>Address</span>, bool <span class='removed removed-inline removed-breaking-inline'>bypassOnLocal</span> <span class='added '>BypassOnLocal</span>)
</div><div data-is-breaking="">	public WebProxy (string <span class='removed removed-inline removed-breaking-inline'>host</span> <span class='added '>Host</span>, int <span class='removed removed-inline removed-breaking-inline'>port</span> <span class='added '>Port</span>)
</div><div data-is-breaking="">	public WebProxy (System.Uri <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>Address</span>, bool <span class='removed removed-inline removed-breaking-inline'>bypassOnLocal</span> <span class='added '>BypassOnLocal</span>)
</div><div data-is-breaking="">	public WebProxy (string <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>Address</span>, bool <span class='removed removed-inline removed-breaking-inline'>bypassOnLocal</span> <span class='added '>BypassOnLocal</span>, string[] <span class='removed removed-inline removed-breaking-inline'>bypassList</span> <span class='added '>BypassList</span>)
</div><div data-is-breaking="">	public WebProxy (System.Uri <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>Address</span>, bool <span class='removed removed-inline removed-breaking-inline'>bypassOnLocal</span> <span class='added '>BypassOnLocal</span>, string[] <span class='removed removed-inline removed-breaking-inline'>bypassList</span> <span class='added '>BypassList</span>)
</div><div data-is-breaking="">	public WebProxy (string <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>Address</span>, bool <span class='removed removed-inline removed-breaking-inline'>bypassOnLocal</span> <span class='added '>BypassOnLocal</span>, string[] <span class='removed removed-inline removed-breaking-inline'>bypassList</span> <span class='added '>BypassList</span>, ICredentials <span class='removed removed-inline removed-breaking-inline'>credentials</span> <span class='added '>Credentials</span>)
</div><div data-is-breaking="">	public WebProxy (System.Uri <span class='removed removed-inline removed-breaking-inline'>address</span> <span class='added '>Address</span>, bool <span class='removed removed-inline removed-breaking-inline'>bypassOnLocal</span> <span class='added '>BypassOnLocal</span>, string[] <span class='removed removed-inline removed-breaking-inline'>bypassList</span> <span class='added '>BypassList</span>, ICredentials <span class='removed removed-inline removed-breaking-inline'>credentials</span> <span class='added '>Credentials</span>)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IWebProxy CreateDefaultProxy ();</span>
</pre>
</div>

</div> <!-- end type WebProxy -->
<!-- start type WebRequest --> <div>
<h3>Type Changed: System.Net.WebRequest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public virtual IWebRequestCreate CreatorInstance { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public static void RegisterPortableWebRequestCreator (IWebRequestCreate creator);</span>
</pre>
</div>

</div> <!-- end type WebRequest -->

</div> <!-- end namespace System.Net -->
<!-- start namespace System.Net.Mail --> <div> 
<h2>Namespace System.Net.Mail</h2>
<!-- start type MailMessage --> <div>
<h3>Type Changed: System.Net.Mail.MailMessage</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Net.Mime.TransferEncoding BodyTransferEncoding { get; set; }</span>
</pre>
</div>

</div> <!-- end type MailMessage -->
<!-- start type SmtpClient --> <div>
<h3>Type Changed: System.Net.Mail.SmtpClient</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public SmtpDeliveryFormat DeliveryFormat { get; set; }</span>
</pre>
</div>

</div> <!-- end type SmtpClient -->

</div> <!-- end namespace System.Net.Mail -->
<!-- start namespace System.Net.Security --> <div> 
<h2>Namespace System.Net.Security</h2>
<!-- start type NegotiateStream --> <div>
<h3>Type Changed: System.Net.Security.NegotiateStream</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AuthenticateAsClient (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ChannelBinding binding, string targetName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AuthenticateAsClient (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ChannelBinding binding, string targetName, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel allowedImpersonationLevel);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AuthenticateAsServer (System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy policy);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AuthenticateAsServer (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy policy, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel requiredImpersonationLevel);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginAuthenticateAsClient (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ChannelBinding binding, string targetName, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginAuthenticateAsClient (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ChannelBinding binding, string targetName, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel allowedImpersonationLevel, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginAuthenticateAsServer (System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy policy, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginAuthenticateAsServer (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy policy, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel requiredImpersonationLevel, System.AsyncCallback asyncCallback, object asyncState);</span>
</pre>
</div>

</div> <!-- end type NegotiateStream -->

</div> <!-- end namespace System.Net.Security -->
<!-- start namespace System.Net.Sockets --> <div> 
<h2>Namespace System.Net.Sockets</h2>
<!-- start type Socket --> <div>
<h3>Type Changed: System.Net.Sockets.Socket</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public Socket (SocketInformation socketInformation);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public SocketInformation DuplicateAndClose (int targetProcessId);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetIPProtectionLevel (IPProtectionLevel level);</span>
</pre>
</div>

</div> <!-- end type Socket -->
<!-- start type SocketAsyncEventArgs --> <div>
<h3>Type Changed: System.Net.Sockets.SocketAsyncEventArgs</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public TransmitFileOptions SendPacketsFlags { get; set; }</span>
</pre>
</div>

</div> <!-- end type SocketAsyncEventArgs -->
<!-- start type TcpListener --> <div>
<h3>Type Changed: System.Net.Sockets.TcpListener</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AllowNatTraversal (bool allowed);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TcpListener Create (int port);</span>
</pre>
</div>

</div> <!-- end type TcpListener -->
<!-- start type UdpClient --> <div>
<h3>Type Changed: System.Net.Sockets.UdpClient</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AllowNatTraversal (bool allowed);</span>
</pre>
</div>

</div> <!-- end type UdpClient -->
<div> <!-- start type SocketReceiveFromResult -->
<h3>New Type System.Net.Sockets.SocketReceiveFromResult</h3>
<pre class='added' data-is-non-breaking="">
public struct SocketReceiveFromResult {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public int ReceivedBytes;</span>
	<span class='added added-field ' data-is-non-breaking="">public System.Net.EndPoint RemoteEndPoint;</span>
}
</pre>
</div> <!-- end type SocketReceiveFromResult -->
<div> <!-- start type SocketReceiveMessageFromResult -->
<h3>New Type System.Net.Sockets.SocketReceiveMessageFromResult</h3>
<pre class='added' data-is-non-breaking="">
public struct SocketReceiveMessageFromResult {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public IPPacketInformation PacketInformation;</span>
	<span class='added added-field ' data-is-non-breaking="">public int ReceivedBytes;</span>
	<span class='added added-field ' data-is-non-breaking="">public System.Net.EndPoint RemoteEndPoint;</span>
	<span class='added added-field ' data-is-non-breaking="">public SocketFlags SocketFlags;</span>
}
</pre>
</div> <!-- end type SocketReceiveMessageFromResult -->
<div> <!-- start type SocketTaskExtensions -->
<h3>New Type System.Net.Sockets.SocketTaskExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SocketTaskExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;Socket&gt; AcceptAsync (Socket socket);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;Socket&gt; AcceptAsync (Socket socket, Socket acceptSocket);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task ConnectAsync (Socket socket, System.Net.EndPoint remoteEP);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task ConnectAsync (Socket socket, System.Net.IPAddress address, int port);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task ConnectAsync (Socket socket, System.Net.IPAddress[] addresses, int port);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task ConnectAsync (Socket socket, string host, int port);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;int&gt; ReceiveAsync (Socket socket, System.ArraySegment&lt;byte&gt; buffer, SocketFlags socketFlags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;int&gt; ReceiveAsync (Socket socket, System.Collections.Generic.IList&lt;System.ArraySegment&lt;byte&gt;&gt; buffers, SocketFlags socketFlags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;SocketReceiveFromResult&gt; ReceiveFromAsync (Socket socket, System.ArraySegment&lt;byte&gt; buffer, SocketFlags socketFlags, System.Net.EndPoint remoteEndPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;SocketReceiveMessageFromResult&gt; ReceiveMessageFromAsync (Socket socket, System.ArraySegment&lt;byte&gt; buffer, SocketFlags socketFlags, System.Net.EndPoint remoteEndPoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;int&gt; SendAsync (Socket socket, System.ArraySegment&lt;byte&gt; buffer, SocketFlags socketFlags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;int&gt; SendAsync (Socket socket, System.Collections.Generic.IList&lt;System.ArraySegment&lt;byte&gt;&gt; buffers, SocketFlags socketFlags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;int&gt; SendToAsync (Socket socket, System.ArraySegment&lt;byte&gt; buffer, SocketFlags socketFlags, System.Net.EndPoint remoteEP);</span>
}
</pre>
</div> <!-- end type SocketTaskExtensions -->

</div> <!-- end namespace System.Net.Sockets -->
<!-- start namespace System.Security.Cryptography.X509Certificates --> <div> 
<h2>Namespace System.Security.Cryptography.X509Certificates</h2>
<!-- start type X509Certificate2 --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509Certificate2</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected X509Certificate2 (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);</span>
</pre>
</div>

</div> <!-- end type X509Certificate2 -->

</div> <!-- end namespace System.Security.Cryptography.X509Certificates -->
<!-- start namespace System.Text.RegularExpressions --> <div> 
<h2>Namespace System.Text.RegularExpressions</h2>
<!-- start type Regex --> <div>
<h3>Type Changed: System.Text.RegularExpressions.Regex</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected bool UseOptionC ();</span>
</pre>
</div>

</div> <!-- end type Regex -->

</div> <!-- end namespace System.Text.RegularExpressions -->
<!-- start namespace System.Diagnostics.CodeAnalysis --> <div> 
<h2>New Namespace System.Diagnostics.CodeAnalysis</h2>

<div> <!-- start type ExcludeFromCodeCoverageAttribute -->
<h3>New Type System.Diagnostics.CodeAnalysis.ExcludeFromCodeCoverageAttribute</h3>
<pre class='added' data-is-non-breaking="">
public sealed class ExcludeFromCodeCoverageAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ExcludeFromCodeCoverageAttribute ();</span>
}
</pre>
</div> <!-- end type ExcludeFromCodeCoverageAttribute -->
</div> <!-- end namespace System.Diagnostics.CodeAnalysis -->

<!-- start namespace System.Windows.Markup --> <div> 
<h2>New Namespace System.Windows.Markup</h2>

<div> <!-- start type ValueSerializerAttribute -->
<h3>New Type System.Windows.Markup.ValueSerializerAttribute</h3>
<pre class='added' data-is-non-breaking="">
public sealed class ValueSerializerAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueSerializerAttribute (string valueSerializerTypeName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ValueSerializerAttribute (System.Type valueSerializerType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Type ValueSerializerType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ValueSerializerTypeName { get; }</span>
}
</pre>
</div> <!-- end type ValueSerializerAttribute -->
</div> <!-- end namespace System.Windows.Markup -->

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
<!-- start namespace Microsoft.Win32.SafeHandles --> <div> 
<h2>Namespace Microsoft.Win32.SafeHandles</h2>
<!-- start type SafeNCryptHandle --> <div>
<h3>Type Changed: Microsoft.Win32.SafeHandles.SafeNCryptHandle</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Runtime.InteropServices.SafeHandle</span> <span class='added '>Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid</span>

</div> <!-- end type SafeNCryptHandle -->

</div> <!-- end namespace Microsoft.Win32.SafeHandles -->
<!-- start namespace System.IO.Pipes --> <div> 
<h2>Namespace System.IO.Pipes</h2>
<!-- start type AnonymousPipeServerStream --> <div>
<h3>Type Changed: System.IO.Pipes.AnonymousPipeServerStream</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AnonymousPipeServerStream (PipeDirection direction, System.IO.HandleInheritability inheritability, int bufferSize, PipeSecurity pipeSecurity);</span>
</pre>
</div>

</div> <!-- end type AnonymousPipeServerStream -->
<!-- start type NamedPipeClientStream --> <div>
<h3>Type Changed: System.IO.Pipes.NamedPipeClientStream</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeClientStream (string serverName, string pipeName, PipeAccessRights desiredAccessRights, PipeOptions options, System.Security.Principal.TokenImpersonationLevel impersonationLevel, System.IO.HandleInheritability inheritability);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void CheckPipePropertyOperations ();</span>
</pre>
</div>

</div> <!-- end type NamedPipeClientStream -->
<!-- start type NamedPipeServerStream --> <div>
<h3>Type Changed: System.IO.Pipes.NamedPipeServerStream</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName, PipeDirection direction, int maxNumberOfServerInstances, PipeTransmissionMode transmissionMode, PipeOptions options, int inBufferSize, int outBufferSize, PipeSecurity pipeSecurity);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName, PipeDirection direction, int maxNumberOfServerInstances, PipeTransmissionMode transmissionMode, PipeOptions options, int inBufferSize, int outBufferSize, PipeSecurity pipeSecurity, System.IO.HandleInheritability inheritability);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NamedPipeServerStream (string pipeName, PipeDirection direction, int maxNumberOfServerInstances, PipeTransmissionMode transmissionMode, PipeOptions options, int inBufferSize, int outBufferSize, PipeSecurity pipeSecurity, System.IO.HandleInheritability inheritability, PipeAccessRights additionalAccessRights);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.IAsyncResult BeginWaitForConnection (System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">public void EndWaitForConnection (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RunAsClient (PipeStreamImpersonationWorker impersonationWorker);</span>
</pre>
</div>

</div> <!-- end type NamedPipeServerStream -->
<!-- start type PipeStream --> <div>
<h3>Type Changed: System.IO.Pipes.PipeStream</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">protected bool IsHandleExposed { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override System.IAsyncResult BeginRead (byte[] buffer, int offset, int count, System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.IAsyncResult BeginWrite (byte[] buffer, int offset, int count, System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void CheckPipePropertyOperations ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected void CheckReadOperations ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected void CheckWriteOperations ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override int EndRead (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public override void EndWrite (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public PipeSecurity GetAccessControl ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected void InitializeHandle (Microsoft.Win32.SafeHandles.SafePipeHandle handle, bool isExposed, bool isAsync);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAccessControl (PipeSecurity pipeSecurity);</span>
</pre>
</div>

</div> <!-- end type PipeStream -->

</div> <!-- end namespace System.IO.Pipes -->
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<!-- start type DebugInfoGenerator --> <div>
<h3>Type Changed: System.Runtime.CompilerServices.DebugInfoGenerator</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static DebugInfoGenerator CreatePdbGenerator ();</span>
</pre>
</div>

</div> <!-- end type DebugInfoGenerator -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type ECDiffieHellmanPublicKey --> <div>
<h3>Type Changed: System.Security.Cryptography.ECDiffieHellmanPublicKey</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> string ToXmlString ()
</div></pre>

</div> <!-- end type ECDiffieHellmanPublicKey -->
<h3>Removed Type <span class='breaking' data-is-breaking="">System.Security.Cryptography.IncrementalHash</span></h3>
</div> <!-- end namespace System.Security.Cryptography -->
<!-- start namespace System.Runtime.InteropServices --> <div> 
<h2>New Namespace System.Runtime.InteropServices</h2>

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
</div> <!-- end namespace System.Runtime.InteropServices -->

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
<!-- start namespace System.Data.SqlClient --> <div> 
<h2>Namespace System.Data.SqlClient</h2>
<!-- start type SqlConnectionStringBuilder --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlConnectionStringBuilder</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public PoolBlockingPeriod PoolBlockingPeriod { get; set; }</span>
</pre>
</div>

</div> <!-- end type SqlConnectionStringBuilder -->
<div> <!-- start type PoolBlockingPeriod -->
<h3>New Type System.Data.SqlClient.PoolBlockingPeriod</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PoolBlockingPeriod {
	<span class='added added-field ' data-is-non-breaking="">AlwaysBlock = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Auto = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NeverBlock = 2,</span>
}
</pre>
</div> <!-- end type PoolBlockingPeriod -->

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
</script><h1 id='diff/xi/Xamarin.iOS/System.Runtime.Serialization.html'>System.Runtime.Serialization.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Runtime.Serialization --> <div> 
<h2>Namespace System.Runtime.Serialization</h2>
<!-- start type XmlSerializableServices --> <div>
<h3>Type Changed: System.Runtime.Serialization.XmlSerializableServices</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void AddDefaultSchema (System.Xml.Schema.XmlSchemaSet schemas, System.Xml.XmlQualifiedName typeQName);</span>
</pre>
</div>

</div> <!-- end type XmlSerializableServices -->
<div> <!-- start type XsdDataContractExporter -->
<h3>New Type System.Runtime.Serialization.XsdDataContractExporter</h3>
<pre class='added' data-is-non-breaking="">
public class XsdDataContractExporter {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public XsdDataContractExporter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public XsdDataContractExporter (System.Xml.Schema.XmlSchemaSet schemas);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public ExportOptions Options { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Xml.Schema.XmlSchemaSet Schemas { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public bool CanExport (System.Collections.Generic.ICollection&lt;System.Reflection.Assembly&gt; assemblies);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool CanExport (System.Collections.Generic.ICollection&lt;System.Type&gt; types);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool CanExport (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Export (System.Collections.Generic.ICollection&lt;System.Reflection.Assembly&gt; assemblies);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Export (System.Collections.Generic.ICollection&lt;System.Type&gt; types);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Export (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Xml.XmlQualifiedName GetRootElementName (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Xml.Schema.XmlSchemaType GetSchemaType (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Xml.XmlQualifiedName GetSchemaTypeName (System.Type type);</span>
}
</pre>
</div> <!-- end type XsdDataContractExporter -->

</div> <!-- end namespace System.Runtime.Serialization -->
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
</script><h1 id='diff/xi/Xamarin.iOS/System.Xml.html'>System.Xml.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Xml.Serialization --> <div> 
<h2>Namespace System.Xml.Serialization</h2>
<!-- start type XmlSerializationReader --> <div>
<h3>Type Changed: System.Xml.Serialization.XmlSerializationReader</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected IXmlSerializable ReadSerializable (IXmlSerializable serializable, bool wrappedAny);</span>
</pre>
</div>

</div> <!-- end type XmlSerializationReader -->
<!-- start type XmlSerializer --> <div>
<h3>Type Changed: System.Xml.Serialization.XmlSerializer</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public XmlSerializer (System.Type type, XmlAttributeOverrides overrides, System.Type[] extraTypes, XmlRootAttribute root, string defaultNamespace, string location);</span>
</pre>
</div>

</div> <!-- end type XmlSerializer -->
<!-- start type XmlSerializerFactory --> <div>
<h3>Type Changed: System.Xml.Serialization.XmlSerializerFactory</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public XmlSerializer CreateSerializer (System.Type type, XmlAttributeOverrides overrides, System.Type[] extraTypes, XmlRootAttribute root, string defaultNamespace, string location);</span>
</pre>
</div>

</div> <!-- end type XmlSerializerFactory -->

</div> <!-- end namespace System.Xml.Serialization -->
<!-- start namespace System.Xml.Xsl --> <div> 
<h2>Namespace System.Xml.Xsl</h2>
<!-- start type XslCompiledTransform --> <div>
<h3>Type Changed: System.Xml.Xsl.XslCompiledTransform</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Load (System.Type compiledStylesheet);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Load (System.Reflection.MethodInfo executeMethod, byte[] queryData, System.Type[] earlyBoundTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Transform (System.Xml.XPath.IXPathNavigable input, XsltArgumentList arguments, System.Xml.XmlWriter results, System.Xml.XmlResolver documentResolver);</span>
</pre>
</div>

</div> <!-- end type XslCompiledTransform -->

</div> <!-- end namespace System.Xml.Xsl -->
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
</script><h1 id='diff/xi/Xamarin.iOS/Mono.Security.html'>Mono.Security.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Mono.Security.X509 --> <div> 
<h2>Namespace Mono.Security.X509</h2>
<!-- start type X509StoreManager --> <div>
<h3>Type Changed: Mono.Security.X509.X509StoreManager</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static X509Stores NewCurrentUser { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static X509Stores NewLocalMachine { get; }</span>
</pre>
</div>

</div> <!-- end type X509StoreManager -->

</div> <!-- end namespace Mono.Security.X509 -->
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
<!-- start namespace NUnitLite.Runner --> <div> 
<h2>Namespace NUnitLite.Runner</h2>
<!-- start type TextUI --> <div>
<h3>Type Changed: NUnitLite.Runner.TextUI</h3>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public bool Failure;</span>
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
<!-- start type NSUrlSessionHandler --> <div>
<h3>Type Changed: System.Net.Http.NSUrlSessionHandler</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionHandler -->

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
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAssetDownloadOptions --> <div>
<h3>Type Changed: AVFoundation.AVAssetDownloadOptions</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public AVMediaSelection MediaSelection { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public Foundation.NSNumber MinimumRequiredMediaBitrate { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type AVAssetDownloadOptions -->
<!-- start type AVAssetExportSession --> <div>
<h3>Type Changed: AVFoundation.AVAssetExportSession</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAssetExportSession (AVAsset asset, AVAssetExportSessionPreset preset);</span>
</pre>
</div>

</div> <!-- end type AVAssetExportSession -->
<!-- start type AVCaptureDevice --> <div>
<h3>Type Changed: AVFoundation.AVCaptureDevice</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use GetDefaultDevice(AVMediaTypes)")]
	public static AVCaptureDevice DefaultDeviceWithMediaType (string mediaType);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVCaptureDevice GetDefaultDevice (AVMediaTypes mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVCaptureDevice GetDefaultDevice (Foundation.NSString mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool HasMediaType (AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVCaptureDevice -->
<div> <!-- start type AVAssetExportSessionPreset -->
<h3>New Type AVFoundation.AVAssetExportSessionPreset</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAssetExportSessionPreset {
	<span class='added added-field ' data-is-non-breaking="">AppleM4A = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HighestQuality = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LowQuality = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumQuality = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Passthrough = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset1280x720 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset1920x1080 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset3840x2160 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset640x480 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset960x540 = 4,</span>
}
</pre>
</div> <!-- end type AVAssetExportSessionPreset -->
<div> <!-- start type AVAssetExportSessionPresetExtensions -->
<h3>New Type AVFoundation.AVAssetExportSessionPresetExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVAssetExportSessionPresetExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVAssetExportSessionPreset self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVAssetExportSessionPreset GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVAssetExportSessionPresetExtensions -->
<div> <!-- start type AVMediaTypes -->
<h3>New Type AVFoundation.AVMediaTypes</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVMediaTypes {
	<span class='added added-field ' data-is-non-breaking="">Audio = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ClosedCaption = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Metadata = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">MetadataObject = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Muxed = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtitle = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Timecode = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TimedMetadata = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 0,</span>
}
</pre>
</div> <!-- end type AVMediaTypes -->
<div> <!-- start type AVMediaTypesExtensions -->
<h3>New Type AVFoundation.AVMediaTypesExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVMediaTypesExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVMediaTypes self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVMediaTypes GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVMediaTypesExtensions -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnimationDiscrete { get; }</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CADisplayLink --> <div>
<h3>Type Changed: CoreAnimation.CADisplayLink</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveFromRunLoop (Foundation.NSRunLoop runloop, Foundation.NSRunLoopMode mode);</span>
</pre>
</div>

</div> <!-- end type CADisplayLink -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIImage --> <div>
<h3>Type Changed: CoreImage.CIImage</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGColorSpace ColorSpace { get; }</span>
</pre>
</div>

</div> <!-- end type CIImage -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<div> <!-- start type CVPlanarPixelBufferInfo_YCbCrBiPlanar -->
<h3>New Type CoreVideo.CVPlanarPixelBufferInfo_YCbCrBiPlanar</h3>
<pre class='added' data-is-non-breaking="">
public struct CVPlanarPixelBufferInfo_YCbCrBiPlanar {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public CVPlanarComponentInfo ComponentInfoCbCr;</span>
	<span class='added added-field ' data-is-non-breaking="">public CVPlanarComponentInfo ComponentInfoY;</span>
}
</pre>
</div> <!-- end type CVPlanarPixelBufferInfo_YCbCrBiPlanar -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSFileHandle --> <div>
<h3>Type Changed: Foundation.NSFileHandle</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AcceptConnectionInBackground (NSRunLoopMode[] notifyRunLoopModes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ReadInBackground (NSRunLoopMode[] notifyRunLoopModes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ReadToEndOfFileInBackground (NSRunLoopMode[] notifyRunLoopModes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void WaitForDataInBackground (NSRunLoopMode[] notifyRunLoopModes);</span>
</pre>
</div>

</div> <!-- end type NSFileHandle -->
<!-- start type NSMetadataItem --> <div>
<h3>Type Changed: Foundation.NSMetadataItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public NSString ContentType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSString[] ContentTypeTree { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSString UbiquitousItemContainerDisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool UbiquitousItemDownloadRequested { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool UbiquitousItemIsExternalDocument { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSUrl UbiquitousItemUrlInLocalContainer { get; }</span>
</pre>
</div>

</div> <!-- end type NSMetadataItem -->
<!-- start type NSNetService --> <div>
<h3>Type Changed: Foundation.NSNetService</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Schedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unschedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
</pre>
</div>

</div> <!-- end type NSNetService -->
<!-- start type NSNetServiceBrowser --> <div>
<h3>Type Changed: Foundation.NSNetServiceBrowser</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Schedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unschedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
</pre>
</div>

</div> <!-- end type NSNetServiceBrowser -->
<!-- start type NSPort --> <div>
<h3>Type Changed: Foundation.NSPort</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveFromRunLoop (NSRunLoop runLoop, NSRunLoopMode runLoopMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ScheduleInRunLoop (NSRunLoop runLoop, NSRunLoopMode runLoopMode);</span>
</pre>
</div>

</div> <!-- end type NSPort -->
<!-- start type NSRunLoop --> <div>
<h3>Type Changed: Foundation.NSRunLoop</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public bool RunUntil (NSRunLoopMode <span class='removed removed-inline removed-breaking-inline'>mode</span> <span class='added '>runLoopMode</span>, NSDate limitDate)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Perform (NSRunLoopMode[] modes, System.Action block);</span>
</pre>
</div>

</div> <!-- end type NSRunLoop -->
<!-- start type NSStream --> <div>
<h3>Type Changed: Foundation.NSStream</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Schedule (NSRunLoop aRunLoop, NSRunLoopMode mode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unschedule (NSRunLoop aRunLoop, NSRunLoopMode mode);</span>
</pre>
</div>

</div> <!-- end type NSStream -->
<!-- start type NSUrlConnection --> <div>
<h3>Type Changed: Foundation.NSUrlConnection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Schedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unschedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
</pre>
</div>

</div> <!-- end type NSUrlConnection -->
<div> <!-- start type NSItemDownloadingStatusExtensions -->
<h3>New Type Foundation.NSItemDownloadingStatusExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSItemDownloadingStatusExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSString GetConstant (NSItemDownloadingStatus self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSItemDownloadingStatus GetValue (NSString constant);</span>
}
</pre>
</div> <!-- end type NSItemDownloadingStatusExtensions -->
<div> <!-- start type NSRunLoopModeExtensions -->
<h3>New Type Foundation.NSRunLoopModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSRunLoopModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSString GetConstant (NSRunLoopMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSString[] GetConstants (NSRunLoopMode[] self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSRunLoopMode GetValue (NSString constant);</span>
}
</pre>
</div> <!-- end type NSRunLoopModeExtensions -->

</div> <!-- end namespace Foundation -->
<!-- start namespace MultipeerConnectivity --> <div> 
<h2>Namespace MultipeerConnectivity</h2>
<!-- start type MCSession --> <div>
<h3>Type Changed: MultipeerConnectivity.MCSession</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; NearbyConnectionDataForPeerAsync (MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendResourceAsync (Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendResourceAsync (Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID, Foundation.NSProgress result);</span>
</pre>
</div>

</div> <!-- end type MCSession -->

</div> <!-- end namespace MultipeerConnectivity -->
<!-- start namespace NetworkExtension --> <div> 
<h2>Namespace NetworkExtension</h2>
<!-- start type NETunnelProviderManager --> <div>
<h3>Type Changed: NetworkExtension.NETunnelProviderManager</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NETunnelProviderManager ();</span>
</pre>
</div>

</div> <!-- end type NETunnelProviderManager -->

</div> <!-- end namespace NetworkExtension -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.2.1"</span> <span class='added '>"10.4.0"</span>;
</div></pre>

</div> <!-- end type Constants -->
<!-- start type LinkWithAttribute --> <div>
<h3>Type Changed: ObjCRuntime.LinkWithAttribute</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public LinkWithAttribute ();</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public DlsymOption Dlsym { get; set; }</span>
</pre>
</div>

</div> <!-- end type LinkWithAttribute -->
<div> <!-- start type DlsymOption -->
<h3>New Type ObjCRuntime.DlsymOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum DlsymOption {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disabled = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Required = 1,</span>
}
</pre>
</div> <!-- end type DlsymOption -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, SCNHitTestOptions options);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SCNRenderer FromContext (OpenGLES.EAGLContext context, Foundation.NSDictionary options);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SecRecord --> <div>
<h3>Type Changed: Security.SecRecord</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SecRecord (SecCertificate certificate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecRecord (SecIdentity identity);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecRecord (SecKey key);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public LocalAuthentication.LAContext AuthenticationContext { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public SecCertificate GetCertificate ();</span>
	<span class='added added-method ' data-is-non-breaking="">public SecIdentity GetIdentity ();</span>
	<span class='added added-method ' data-is-non-breaking="">public SecKey GetKey ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCertificate (SecCertificate cert);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetIdentity (SecIdentity identity);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetKey (SecKey key);</span>
</pre>
</div>

</div> <!-- end type SecRecord -->

</div> <!-- end namespace Security -->
<!-- start namespace Social --> <div> 
<h2>Namespace Social</h2>
<!-- start type SLComposeServiceViewController --> <div>
<h3>Type Changed: Social.SLComposeServiceViewController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInteractWithTextAttachment (UIKit.UITextView textView, UIKit.NSTextAttachment textAttachment, Foundation.NSRange characterRange, UIKit.UITextItemInteraction interaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInteractWithUrl (UIKit.UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UIKit.UITextItemInteraction interaction);</span>
</pre>
</div>

</div> <!-- end type SLComposeServiceViewController -->

</div> <!-- end namespace Social -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type UIFont --> <div>
<h3>Type Changed: UIKit.UIFont</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIFont GetPreferredFontForTextStyle (UIFontTextStyle uiFontTextStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIFont GetPreferredFontForTextStyle (UIFontTextStyle uiFontTextStyle, UITraitCollection traitCollection);</span>
</pre>
</div>

</div> <!-- end type UIFont -->
<!-- start type UIFontDescriptor --> <div>
<h3>Type Changed: UIKit.UIFontDescriptor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIFontDescriptor GetPreferredDescriptorForTextStyle (UIFontTextStyle uiFontTextStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIFontDescriptor GetPreferredDescriptorForTextStyle (UIFontTextStyle uiFontTextStyle, UITraitCollection traitCollection);</span>
</pre>
</div>

</div> <!-- end type UIFontDescriptor -->
<!-- start type UITextField --> <div>
<h3>Type Changed: UIKit.UITextField</h3>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;UITextFieldEditingEndedEventArgs&gt; EndedWithReason;</span>
</pre>
</div>

</div> <!-- end type UITextField -->
<!-- start type UITextFieldDelegate --> <div>
<h3>Type Changed: UIKit.UITextFieldDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EditingEnded (UITextField textField, UITextFieldDidEndEditingReason reason);</span>
</pre>
</div>

</div> <!-- end type UITextFieldDelegate -->
<!-- start type UITextFieldDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UITextFieldDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void EditingEnded (IUITextFieldDelegate This, UITextField textField, UITextFieldDidEndEditingReason reason);</span>
</pre>
</div>

</div> <!-- end type UITextFieldDelegate_Extensions -->
<!-- start type UITextView --> <div>
<h3>Type Changed: UIKit.UITextView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public UITextViewDelegateShouldInteractTextDelegate AllowTextAttachmentInteraction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public UITextViewDelegateShouldInteractUrlDelegate AllowUrlInteraction { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextView -->
<!-- start type UITextViewDelegate --> <div>
<h3>Type Changed: UIKit.UITextViewDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInteractWithTextAttachment (UITextView textView, NSTextAttachment textAttachment, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInteractWithUrl (UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
</pre>
</div>

</div> <!-- end type UITextViewDelegate -->
<!-- start type UITextViewDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UITextViewDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldInteractWithTextAttachment (IUITextViewDelegate This, UITextView textView, NSTextAttachment textAttachment, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldInteractWithUrl (IUITextViewDelegate This, UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
</pre>
</div>

</div> <!-- end type UITextViewDelegate_Extensions -->
<div> <!-- start type UIFontTextStyle -->
<h3>New Type UIKit.UIFontTextStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIFontTextStyle {
	<span class='added added-field ' data-is-non-breaking="">Body = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Callout = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Caption1 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Caption2 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Footnote = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Headline = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Subheadline = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Title1 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Title2 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Title3 = 8,</span>
}
</pre>
</div> <!-- end type UIFontTextStyle -->
<div> <!-- start type UIFontTextStyleExtensions -->
<h3>New Type UIKit.UIFontTextStyleExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIFontTextStyleExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (UIFontTextStyle self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIFontTextStyle GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type UIFontTextStyleExtensions -->
<div> <!-- start type UITextFieldEditingEndedEventArgs -->
<h3>New Type UIKit.UITextFieldEditingEndedEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class UITextFieldEditingEndedEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextFieldEditingEndedEventArgs (UITextFieldDidEndEditingReason reason);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public UITextFieldDidEndEditingReason Reason { get; set; }</span>
}
</pre>
</div> <!-- end type UITextFieldEditingEndedEventArgs -->
<div> <!-- start type UITextViewDelegateShouldInteractTextDelegate -->
<h3>New Type UIKit.UITextViewDelegateShouldInteractTextDelegate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UITextViewDelegateShouldInteractTextDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextViewDelegateShouldInteractTextDelegate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UITextView textView, NSTextAttachment textAttachment, Foundation.NSRange characterRange, UITextItemInteraction interaction, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (UITextView textView, NSTextAttachment textAttachment, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
}
</pre>
</div> <!-- end type UITextViewDelegateShouldInteractTextDelegate -->
<div> <!-- start type UITextViewDelegateShouldInteractUrlDelegate -->
<h3>New Type UIKit.UITextViewDelegateShouldInteractUrlDelegate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UITextViewDelegateShouldInteractUrlDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextViewDelegateShouldInteractUrlDelegate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UITextItemInteraction interaction, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
}
</pre>
</div> <!-- end type UITextViewDelegateShouldInteractUrlDelegate -->

</div> <!-- end namespace UIKit -->
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKInterfaceDevice --> <div>
<h3>Type Changed: WatchKit.WKInterfaceDevice</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use PreferredContentSizeCategoryString instead.")]
	public UIKit.UIContentSizeCategory PreferredContentSizeCategory { get; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string PreferredContentSizeCategoryString { get; }</span>
</pre>
</div>

</div> <!-- end type WKInterfaceDevice -->

</div> <!-- end namespace WatchKit -->
</div>



   


 <hr>
