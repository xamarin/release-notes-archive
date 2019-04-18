---
id: 3209BE1D-3BF1-4746-AB1D-2CF5A85FF018
title: "From 8.10.3 to 8.13.0"
---

# API diff

 [mscorlib.dll](#mscorlib)

   


 [System.dll](#System)

   


 [System.Core.dll](#System.Core)

   


 [System.ComponentModel.DataAnnotations.dll](#System.ComponentModel.DataAnnotations)

   


 [System.ComponentModel.Composition.dll](#System.ComponentModel.Composition)

   


 [System.Data.dll](#System.Data)

   


 [System.Data.Services.Client.dll](#System.Data.Services.Client)

   


 [System.Runtime.Serialization.dll](#System.Runtime.Serialization)

   


 [System.ServiceModel.dll](#System.ServiceModel)

   


 [System.ServiceModel.Web.dll](#System.ServiceModel.Web)

   


 [System.Web.Services.dll](#System.Web.Services)

   


 [System.Xml.dll](#System.Xml)

   


 [Mono.Data.Sqlite.dll](#Mono.Data.Sqlite)

   


 [Mono.Data.Tds.dll](#Mono.Data.Tds)

   


 [System.Net.Http.dll](#System.Net.Http)

   


 [(Classic) monotouch.dll](#compat/monotouch)

   


 [(Classic) MonoTouch.Dialog-1.dll](#compat/MonoTouch.Dialog-1)

   


 [(Classic) MonoTouch.NUnitLite.dll](#compat/MonoTouch.NUnitLite)

   


 [(Classic) OpenTK.dll](#compat/OpenTK)

   


 [(Classic) OpenTK-1.0.dll](#compat/OpenTK-1.0)

   


 [(Unified) MonoTouch.Dialog-1.dll](#reference/MonoTouch.Dialog-1)

   


 [(Unified) MonoTouch.NUnitLite.dll](#reference/MonoTouch.NUnitLite)

   


 [(Unified) OpenTK-1.0.dll](#reference/OpenTK-1.0)

   


 [(Unified) Xamarin.iOS.dll](#reference/Xamarin.iOS)

   


   


 <hr>

<h1 id='mscorlib'>mscorlib.dll</h1>

## Namespace System

### Type Changed: System._AppDomain

Added methods:

<pre style='color: green'>
	public virtual void GetIDsOfNames (ref Guid riid, IntPtr rgszNames, uint cNames, uint lcid, IntPtr rgDispId);
	public virtual void GetTypeInfo (uint iTInfo, uint lcid, IntPtr ppTInfo);
	public virtual void GetTypeInfoCount (out uint pcTInfo);
	public virtual void Invoke (uint dispIdMember, ref Guid riid, uint lcid, short wFlags, IntPtr pDispParams, IntPtr pVarResult, IntPtr pExcepInfo, IntPtr puArgErr);
</pre>

### Type Changed: System.ContextBoundObject


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>System.MarshalByRefObject</span></span>

 <span style='color:green'>System.Object</span>

### Type Changed: System.Type

Added interfaces:

<pre style='color: green'>
	Runtime.InteropServices._Type
	Runtime.InteropServices._MemberInfo
</pre>

## Namespace System.Globalization

### Type Changed: System.Globalization.NumberFormatInfo

Added properties:

<pre style='color: green'>
	public DigitShapes DigitSubstitution { get; set; }
	public string[] NativeDigits { get; set; }
</pre>

## Namespace System.IO

### Type Changed: System.IO.BinaryReader

Modified methods:

```
protected protected int Read7BitEncodedInt ()
```

## Namespace System.Reflection

### Type Changed: System.Reflection.Binder

Added method:

<pre style='color: green'>
	public virtual bool CanChangeType (object value, System.Type type, System.Globalization.CultureInfo culture);
</pre>

### Type Changed: System.Reflection.ConstructorInfo

Added interfaces:

<pre style='color: green'>
	System.Runtime.InteropServices._MethodBase
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.EventInfo

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.FieldInfo

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.MemberInfo

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.MethodBase

Added interfaces:

<pre style='color: green'>
	System.Runtime.InteropServices._MethodBase
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.MethodInfo

Added interfaces:

<pre style='color: green'>
	System.Runtime.InteropServices._MethodBase
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.PropertyInfo

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.TypeDelegator

Added interfaces:

<pre style='color: green'>
	System.Runtime.InteropServices._Type
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.TypeInfo

Added interfaces:

<pre style='color: green'>
	System.Runtime.InteropServices._Type
	System.Runtime.InteropServices._MemberInfo
</pre>

## Namespace System.Runtime.InteropServices

### Type Changed: System.Runtime.InteropServices.ComInterfaceType

Removed value:

<pre style='color: red'>
	InterfaceIsIInspectable = 3,
</pre>

### Type Changed: System.Runtime.InteropServices.VarEnum

Removed value:

<pre style='color: red'>
	VT_DISPATCH = 9,
</pre>

### New Type System.Runtime.InteropServices.ImportedFromTypeLibAttribute

<pre style='color: green'>
public sealed class ImportedFromTypeLibAttribute : System.Attribute {
	// constructors
	public ImportedFromTypeLibAttribute (string tlbFile);
	// properties
	public string Value { get; }
}
</pre>

### New Type System.Runtime.InteropServices.TypeLibImportClassAttribute

<pre style='color: green'>
public sealed class TypeLibImportClassAttribute : System.Attribute {
	// constructors
	public TypeLibImportClassAttribute (System.Type importClass);
	// properties
	public string Value { get; }
}
</pre>

## Namespace System.Runtime.InteropServices.ComTypes

### New Type System.Runtime.InteropServices.ComTypes.EXCEPINFO

<pre style='color: green'>
public struct EXCEPINFO {
	// fields
	public string bstrDescription;
	public string bstrHelpFile;
	public string bstrSource;
	public int dwHelpContext;
	public IntPtr pfnDeferredFillIn;
	public IntPtr pvReserved;
	public int scode;
	public short wCode;
	public short wReserved;
}
</pre>

## Namespace System.Runtime.Serialization

### Type Changed: System.Runtime.Serialization.SerializationInfo

Added constructor:

<pre style='color: green'>
	public SerializationInfo (System.Type type, IFormatterConverter converter, bool requireSameTokenInPartialTrust);
</pre>

## Namespace System.Security

### Type Changed: System.Security.AllowPartiallyTrustedCallersAttribute

Added property:

<pre style='color: green'>
	public PartialTrustVisibilityLevel PartialTrustVisibilityLevel { get; set; }
</pre>

### New Type System.Security.PartialTrustVisibilityLevel

<pre style='color: green'>
[Serializable]
public enum PartialTrustVisibilityLevel {
	NotVisibleByDefault = 1,
	VisibleToAllHosts = 0,
}
</pre>

## Namespace System.Security.Claims

### Type Changed: System.Security.Claims.ClaimsIdentity

Added method:

<pre style='color: green'>
	protected virtual void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
</pre>

## Namespace System.Security.Cryptography

### Type Changed: System.Security.Cryptography.CryptoConfig

Added property:

<pre style='color: green'>
	public static bool AllowOnlyFipsAlgorithms { get; }
</pre>

### Type Changed: System.Security.Cryptography.CryptographicException

Removed interface:

<pre style='color: red'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: System.Security.Cryptography.CryptographicUnexpectedOperationException

Removed interface:

<pre style='color: red'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace System.Security.Policy

### Type Changed: System.Security.Policy.Evidence

Added method:

<pre style='color: green'>
	public Evidence Clone ();
</pre>

## Namespace System.Security.Principal

### Type Changed: System.Security.Principal.GenericIdentity

Added method:

<pre style='color: green'>
	public override System.Security.Claims.ClaimsIdentity Clone ();
</pre>

   


 <hr>

<h1 id='System'>System.dll</h1>

## Namespace System.CodeDom.Compiler

### Type Changed: System.CodeDom.Compiler.IndentedTextWriter

Modified methods:

```
public override void Write (string format, object[] args arg)
	public override void Write (string format, object arg arg0)
	public override void Write (string value s)
	public override void Write (char[] value buffer)
	public override void WriteLine (string value s)
	public override void WriteLine (string format, object arg arg0)
	public override void WriteLine (string format, object[] args arg)
	public override void WriteLine (char[] value buffer)
	public void WriteLineNoTabs (string value s)
```

## Namespace System.Diagnostics

### Type Changed: System.Diagnostics.SourceSwitch

Modified constructors:

```
public SourceSwitch (string displayName name)
```

### Type Changed: System.Diagnostics.Trace

Modified methods:

```
public void TraceError (string message format, object[] args)
	public void TraceInformation (string message format, object[] args)
	public void TraceWarning (string message format, object[] args)
```

### Type Changed: System.Diagnostics.TraceListener

Added property:

<pre style='color: green'>
	public TraceFilter Filter { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void TraceData (TraceEventCache eventCache, string source, TraceEventType eventType, int id, object[] data);
	public virtual void TraceData (TraceEventCache eventCache, string source, TraceEventType eventType, int id, object data);
	public virtual void TraceEvent (TraceEventCache eventCache, string source, TraceEventType eventType, int id, string format, object[] args);
	public virtual void TraceEvent (TraceEventCache eventCache, string source, TraceEventType eventType, int id, string message);
	public virtual void TraceEvent (TraceEventCache eventCache, string source, TraceEventType eventType, int id);
	public virtual void TraceTransfer (TraceEventCache eventCache, string source, int id, string message, System.Guid relatedActivityId);
</pre>

### Type Changed: System.Diagnostics.TraceListenerCollection

Modified properties:

```
public TraceListener this [int index i] { get; set; }
```

### New Type System.Diagnostics.TraceEventCache

<pre style='color: green'>
public class TraceEventCache {
	// constructors
	public TraceEventCache ();
	// properties
	public string Callstack { get; }
	public System.DateTime DateTime { get; }
	public System.Collections.Stack LogicalOperationStack { get; }
	public int ProcessId { get; }
	public string ThreadId { get; }
	public long Timestamp { get; }
}
</pre>

### New Type System.Diagnostics.TraceFilter

<pre style='color: green'>
public abstract class TraceFilter {
	// constructors
	protected TraceFilter ();
	// methods
	public virtual bool ShouldTrace (TraceEventCache cache, string source, TraceEventType eventType, int id, string formatOrMessage, object[] args, object data1, object[] data);
}
</pre>

### New Type System.Diagnostics.TraceSource

<pre style='color: green'>
public class TraceSource {
	// constructors
	public TraceSource (string name);
	public TraceSource (string name, SourceLevels defaultLevel);
	// properties
	public System.Collections.Specialized.StringDictionary Attributes { get; }
	public TraceListenerCollection Listeners { get; }
	public string Name { get; }
	public SourceSwitch Switch { get; set; }
	// methods
	public void Close ();
	public void Flush ();
	protected virtual string[] GetSupportedAttributes ();
	public void TraceData (TraceEventType eventType, int id, object[] data);
	public void TraceData (TraceEventType eventType, int id, object data);
	public void TraceEvent (TraceEventType eventType, int id, string format, object[] args);
	public void TraceEvent (TraceEventType eventType, int id, string message);
	public void TraceEvent (TraceEventType eventType, int id);
	public void TraceInformation (string message);
	public void TraceInformation (string format, object[] args);
	public void TraceTransfer (int id, string message, System.Guid relatedActivityId);
}
</pre>

## Namespace System.Net.NetworkInformation

### Type Changed: System.Net.NetworkInformation.NetworkInterface

Added method:

<pre style='color: green'>
	public static System.Net.IPAddress GetNetMask (System.Net.IPAddress address);
</pre>

### Type Changed: System.Net.NetworkInformation.UnicastIPAddressInformation

Added property:

<pre style='color: green'>
	public virtual int PrefixLength { get; }
</pre>

### New Type System.Net.NetworkInformation.IPInterfaceStatistics

<pre style='color: green'>
public abstract class IPInterfaceStatistics {
	// constructors
	protected IPInterfaceStatistics ();
	// properties
	public virtual long BytesReceived { get; }
	public virtual long BytesSent { get; }
	public virtual long IncomingPacketsDiscarded { get; }
	public virtual long IncomingPacketsWithErrors { get; }
	public virtual long IncomingUnknownProtocolPackets { get; }
	public virtual long NonUnicastPacketsReceived { get; }
	public virtual long NonUnicastPacketsSent { get; }
	public virtual long OutgoingPacketsDiscarded { get; }
	public virtual long OutgoingPacketsWithErrors { get; }
	public virtual long OutputQueueLength { get; }
	public virtual long UnicastPacketsReceived { get; }
	public virtual long UnicastPacketsSent { get; }
}
</pre>

### New Type System.Net.NetworkInformation.ScopeLevel

<pre style='color: green'>
[Serializable]
public enum ScopeLevel {
	Admin = 4,
	Global = 14,
	Interface = 1,
	Link = 2,
	None = 0,
	Organization = 8,
	Site = 5,
	Subnet = 3,
}
</pre>

## Namespace System.Net.Sockets

### Type Changed: System.Net.Sockets.Socket

Obsoleted properties:

```
[Obsolete ("Use OSSupportsIPv4 instead"]
	public static bool SupportsIPv4 { get; }
```

Added property:

<pre style='color: green'>
	public bool DualMode { get; set; }
</pre>

Modified methods:

```
public int Send (byte[] buf buffer, int offset, int size, SocketFlags flags)
	public int Send (byte[] buf buffer, int size, SocketFlags flags)
	public int Send (byte[] buf buffer, SocketFlags flags)
	public int Send (byte[] buf buffer)
	public int Send (byte[] buf buffer, int offset, int size, SocketFlags flags, out SocketError error)
```

### Type Changed: System.Net.Sockets.SocketOptionName

Added values:

<pre style='color: green'>
	IPProtectionLevel = 23,
	IPv6Only = 27,
</pre>

   


 <hr>

<h1 id='System.Core'>System.Core.dll</h1>

## Namespace System.IO.MemoryMappedFiles

### Type Changed: System.IO.MemoryMappedFiles.MemoryMappedViewAccessor

Added property:

<pre style='color: green'>
	public long PointerOffset { get; }
</pre>

### Type Changed: System.IO.MemoryMappedFiles.MemoryMappedViewStream

Added property:

<pre style='color: green'>
	public long PointerOffset { get; }
</pre>

Added method:

<pre style='color: green'>
	public override void SetLength (long value);
</pre>

## Namespace System.Linq.Expressions

### Type Changed: System.Linq.Expressions.DynamicExpression

Added methods:

<pre style='color: green'>
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1, Expression arg2, Expression arg3);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1, Expression arg2);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, System.Collections.Generic.IEnumerable&lt;Expression&gt; arguments);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression[] arguments);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1, Expression arg2);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression[] arguments);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, System.Collections.Generic.IEnumerable&lt;Expression&gt; arguments);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1, Expression arg2, Expression arg3);
</pre>

### Type Changed: System.Linq.Expressions.DynamicExpressionVisitor

Added method:

<pre style='color: green'>
	protected override Expression VisitDynamic (DynamicExpression node);
</pre>

   


 <hr>

<h1 id='System.ComponentModel.DataAnnotations'>System.ComponentModel.DataAnnotations.dll</h1>

## Namespace System.ComponentModel.DataAnnotations

### Type Changed: System.ComponentModel.DataAnnotations.AssociationAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.BindableTypeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.CompareAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.ConcurrencyCheckAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.CreditCardAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.CustomValidationAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.DataTypeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.DisplayAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.DisplayColumnAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.DisplayFormatAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.EditableAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.EmailAddressAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.EnumDataTypeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.FileExtensionsAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.FilterUIHintAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.KeyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.MaxLengthAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.MetadataTypeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.MinLengthAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.PhoneAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.RangeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.RegularExpressionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.RequiredAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.ScaffoldColumnAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.ScaffoldTableAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.StringLengthAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.TimestampAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.UIHintAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.UrlAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.ValidationAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace System.ComponentModel.DataAnnotations.Schema

### Type Changed: System.ComponentModel.DataAnnotations.Schema.ColumnAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.Schema.ComplexTypeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.Schema.DatabaseGeneratedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.Schema.ForeignKeyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.Schema.InversePropertyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.Schema.NotMappedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.DataAnnotations.Schema.TableAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='System.ComponentModel.Composition'>System.ComponentModel.Composition.dll</h1>

## Namespace System.ComponentModel.Composition

### Type Changed: System.ComponentModel.Composition.CatalogReflectionContextAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.ExportAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.ExportMetadataAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.ImportAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.ImportingConstructorAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.ImportManyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.InheritedExportAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.MetadataAttributeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.MetadataViewImplementationAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.PartCreationPolicyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.PartMetadataAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ComponentModel.Composition.PartNotDiscoverableAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='System.Data'>System.Data.dll</h1>

## Namespace Microsoft.SqlServer.Server

### Type Changed: Microsoft.SqlServer.Server.SqlFunctionAttribute

Added properties:

<pre style='color: green'>
	public string FillRowMethodName { get; set; }
	public string Name { get; set; }
	public string TableDefinition { get; set; }
</pre>

### Type Changed: Microsoft.SqlServer.Server.SqlMethodAttribute

Added property:

<pre style='color: green'>
	public bool InvokeIfReceiverIsNull { get; set; }
</pre>

### Type Changed: Microsoft.SqlServer.Server.SqlUserDefinedAggregateAttribute

Added property:

<pre style='color: green'>
	public string Name { get; set; }
</pre>

### Type Changed: Microsoft.SqlServer.Server.SqlUserDefinedTypeAttribute

Added properties:

<pre style='color: green'>
	public string Name { get; set; }
	public string ValidationMethodName { get; set; }
</pre>

### Type Changed: Microsoft.SqlServer.Server.TriggerAction

Added value:

<pre style='color: green'>
	DenyStatement = 168,
</pre>

## Namespace System.Data

### Type Changed: System.Data.Constraint

Modified properties:

```
protected protected virtual DataSet _DataSet { get; }
```

### Type Changed: System.Data.DataColumn

Modified methods:

```
protected protected virtual void OnPropertyChanging (System.ComponentModel.PropertyChangedEventArgs pcevent)
```

### Type Changed: System.Data.DataRowView

Added methods:

<pre style='color: green'>
	public DataView CreateChildView (string relationName, bool followParent);
	public DataView CreateChildView (DataRelation relation, bool followParent);
</pre>

### Type Changed: System.Data.DataSet

Modified methods:

```
protected protected virtual void OnPropertyChanging (System.ComponentModel.PropertyChangedEventArgs pcevent)
	protected protected virtual void OnRemoveTable (DataTable table)
```

Added methods:

<pre style='color: green'>
	public void WriteXmlSchema (System.IO.Stream stream, System.Converter&lt;System.Type,System.String&gt; multipleTargetConverter);
	public void WriteXmlSchema (System.Xml.XmlWriter writer, System.Converter&lt;System.Type,System.String&gt; multipleTargetConverter);
	public void WriteXmlSchema (string fileName, System.Converter&lt;System.Type,System.String&gt; multipleTargetConverter);
	public void WriteXmlSchema (System.IO.TextWriter writer, System.Converter&lt;System.Type,System.String&gt; multipleTargetConverter);
</pre>

### Type Changed: System.Data.DataTable

Removed method:

<pre style='color: red'>
	public XmlReadMode ReadXml_internal (System.Xml.XmlReader reader, bool serializable);
</pre>

Modified methods:

```
protected protected virtual void OnColumnChanged (DataColumnChangeEventArgs e)
	protected protected virtual void OnColumnChanging (DataColumnChangeEventArgs e)
	protected protected virtual void OnPropertyChanging (System.ComponentModel.PropertyChangedEventArgs pcevent)
	protected protected virtual void OnRemoveColumn (DataColumn column)
```

### Type Changed: System.Data.PropertyCollection

Added method:

<pre style='color: green'>
	public override object Clone ();
</pre>

## Namespace System.Data.Common

### Type Changed: System.Data.Common.DbConnection

Modified properties:

```
protected protected virtual DbProviderFactory DbProviderFactory { get; }
```

### Type Changed: System.Data.Common.DbDataReader

Modified methods:

```
public abstract virtual void Close ()
	public virtual T GetFieldValue<T> (int i ordinal)
	public abstract virtual System.Data.DataTable GetSchemaTable ()
	public virtual System.IO.Stream GetStream (int i ordinal)
	public virtual System.IO.TextReader GetTextReader (int i ordinal)
```

### Type Changed: System.Data.Common.DbParameter

Modified properties:

```
public abstract virtual System.Data.DataRowVersion SourceVersion { get; set; }
```

Added properties:

<pre style='color: green'>
	public virtual byte Precision { get; set; }
	public virtual byte Scale { get; set; }
</pre>

### Type Changed: System.Data.Common.DbParameterCollection

Modified properties:

```
public abstract virtual bool IsFixedSize { get; }
	public abstract virtual bool IsReadOnly { get; }
	public abstract virtual bool IsSynchronized { get; }
```

## Namespace System.Data.SqlClient

### Type Changed: System.Data.SqlClient.SqlConnection

Modified properties:

```
protected protected override System.Data.Common.DbProviderFactory DbProviderFactory { get; }
```

### Type Changed: System.Data.SqlClient.SqlConnectionStringBuilder

Obsoleted properties:

```
[Obsolete ("ConnectionReset has been deprecated.  SqlConnection will ignore the 'connection reset' keyword and always reset the connection"]
	public bool ConnectionReset { get; set; }
```

Added properties:

<pre style='color: green'>
	public ApplicationIntent ApplicationIntent { get; set; }
	public int ConnectRetryCount { get; set; }
	public int ConnectRetryInterval { get; set; }
	public bool MultiSubnetFailover { get; set; }
	public string TransactionBinding { get; set; }
</pre>

Added method:

<pre style='color: green'>
	protected override void GetProperties (System.Collections.Hashtable propertyDescriptors);
</pre>

## Namespace System.Xml

### Type Changed: System.Xml.XmlDataDocument

Added method:

<pre style='color: green'>
	public override XmlNodeList GetElementsByTagName (string name);
</pre>

## New Namespace System.Data.OleDb

### New Type System.Data.OleDb.OleDbType

<pre style='color: green'>
[Serializable]
public enum OleDbType {
	BigInt = 20,
	Binary = 128,
	Boolean = 11,
	BSTR = 8,
	Char = 129,
	Currency = 6,
	Date = 7,
	DBDate = 133,
	DBTime = 134,
	DBTimeStamp = 135,
	Decimal = 14,
	Double = 5,
	Empty = 0,
	Error = 10,
	Filetime = 64,
	Guid = 72,
	IDispatch = 9,
	Integer = 3,
	IUnknown = 13,
	LongVarBinary = 205,
	LongVarChar = 201,
	LongVarWChar = 203,
	Numeric = 131,
	PropVariant = 138,
	Single = 4,
	SmallInt = 2,
	TinyInt = 16,
	UnsignedBigInt = 21,
	UnsignedInt = 19,
	UnsignedSmallInt = 18,
	UnsignedTinyInt = 17,
	VarBinary = 204,
	VarChar = 200,
	Variant = 12,
	VarNumeric = 139,
	VarWChar = 202,
	WChar = 130,
}
</pre>

   


 <hr>

<h1 id='System.Data.Services.Client'>System.Data.Services.Client.dll</h1>

## Namespace System.Data.Services.Client

### Type Changed: System.Data.Services.Client.MediaEntryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Data.Services.Client.MimeTypePropertyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace System.Data.Services.Common

### Type Changed: System.Data.Services.Common.DataServiceEntityAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Data.Services.Common.DataServiceKeyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Data.Services.Common.EntityPropertyMappingAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Data.Services.Common.EntitySetAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Data.Services.Common.HasStreamAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='System.Runtime.Serialization'>System.Runtime.Serialization.dll</h1>

## Namespace System.Runtime.Serialization

### Type Changed: System.Runtime.Serialization.DataContractSerializer

Modified constructors:

```
public DataContractSerializer (System.Type type, System.Xml.XmlDictionaryString rootName, System.Xml.XmlDictionaryString rootNamespace, System.Collections.Generic.IEnumerable<System.Type> knownTypes, int maxObjectsInGraph maxItemsInObjectGraph, bool ignoreExtensionDataObject, bool preserveObjectReferences, IDataContractSurrogate dataContractSurrogate, DataContractResolver dataContractResolver)
	public DataContractSerializer (System.Type type, string rootName, string rootNamespace, System.Collections.Generic.IEnumerable<System.Type> knownTypes, int maxObjectsInGraph maxItemsInObjectGraph, bool ignoreExtensionDataObject, bool preserveObjectReferences, IDataContractSurrogate dataContractSurrogate, DataContractResolver dataContractResolver)
	public DataContractSerializer (System.Type type, System.Collections.Generic.IEnumerable<System.Type> knownTypes, int maxObjectsInGraph maxItemsInObjectGraph, bool ignoreExtensionDataObject, bool preserveObjectReferences, IDataContractSurrogate dataContractSurrogate, DataContractResolver dataContractResolver)
	public DataContractSerializer (System.Type type, System.Xml.XmlDictionaryString rootName, System.Xml.XmlDictionaryString rootNamespace, System.Collections.Generic.IEnumerable<System.Type> knownTypes, int maxObjectsInGraph maxItemsInObjectGraph, bool ignoreExtensionDataObject, bool preserveObjectReferences, IDataContractSurrogate dataContractSurrogate)
	public DataContractSerializer (System.Type type, string rootName, string rootNamespace, System.Collections.Generic.IEnumerable<System.Type> knownTypes, int maxObjectsInGraph maxItemsInObjectGraph, bool ignoreExtensionDataObject, bool preserveObjectReferences, IDataContractSurrogate dataContractSurrogate)
	public DataContractSerializer (System.Type type, System.Collections.Generic.IEnumerable<System.Type> knownTypes, int maxObjectsInGraph maxItemsInObjectGraph, bool ignoreExtensionDataObject, bool preserveObjectReferences, IDataContractSurrogate dataContractSurrogate)
```

Modified methods:

```
public object ReadObject (System.Xml.XmlDictionaryReader reader, bool verifyObjectName, DataContractResolver resolver dataContractResolver)
	public void WriteObject (System.Xml.XmlDictionaryWriter writer, object graph, DataContractResolver resolver dataContractResolver)
```

### Type Changed: System.Runtime.Serialization.IDataContractSurrogate

Added method:

<pre style='color: green'>
	public virtual System.Type GetReferencedTypeOnImport (string typeName, string typeNamespace, object customData);
</pre>

### Type Changed: System.Runtime.Serialization.NetDataContractSerializer

Modified constructors:

```
public NetDataContractSerializer (StreamingContext context, int maxItemsInObjectGraph, bool ignoreExtensibleDataObject ignoreExtensionDataObject, Formatters.FormatterAssemblyStyle assemblyFormat, ISurrogateSelector surrogateSelector)
	public NetDataContractSerializer (string rootName, string rootNamespace, StreamingContext context, int maxItemsInObjectGraph, bool ignoreExtensibleDataObject ignoreExtensionDataObject, Formatters.FormatterAssemblyStyle assemblyFormat, ISurrogateSelector surrogateSelector)
	public NetDataContractSerializer (System.Xml.XmlDictionaryString rootName, System.Xml.XmlDictionaryString rootNamespace, StreamingContext context, int maxItemsInObjectGraph, bool ignoreExtensibleDataObject ignoreExtensionDataObject, Formatters.FormatterAssemblyStyle assemblyFormat, ISurrogateSelector surrogateSelector)
```

Modified methods:

```
public override object ReadObject (System.Xml.XmlDictionaryReader reader, bool readContentOnly verifyObjectName)
```

Added methods:

<pre style='color: green'>
	public override bool IsStartObject (System.Xml.XmlReader reader);
	public override object ReadObject (System.Xml.XmlReader reader, bool verifyObjectName);
	public override object ReadObject (System.Xml.XmlReader reader);
	public override void WriteEndObject (System.Xml.XmlWriter writer);
	public override void WriteObject (System.Xml.XmlWriter writer, object graph);
	public override void WriteObjectContent (System.Xml.XmlWriter writer, object graph);
	public override void WriteStartObject (System.Xml.XmlWriter writer, object graph);
</pre>

### Type Changed: System.Runtime.Serialization.XmlObjectSerializer

Modified methods:

```
public abstract object ReadObject (System.Xml.XmlDictionaryReader reader, bool readContentOnly verifyObjectName)
	public virtual object ReadObject (System.Xml.XmlReader reader, bool readContentOnly verifyObjectName)
```

### New Type System.Runtime.Serialization.XmlSerializableServices

<pre style='color: green'>
public static class XmlSerializableServices {
	// methods
	public static System.Xml.XmlNode[] ReadNodes (System.Xml.XmlReader xmlReader);
	public static void WriteNodes (System.Xml.XmlWriter xmlWriter, System.Xml.XmlNode[] nodes);
}
</pre>

### New Type System.Runtime.Serialization.XPathQueryGenerator

<pre style='color: green'>
public static class XPathQueryGenerator {
	// methods
	public static string CreateFromDataContractSerializer (System.Type type, System.Reflection.MemberInfo[] pathToMember, out System.Xml.XmlNamespaceManager namespaces);
	public static string CreateFromDataContractSerializer (System.Type type, System.Reflection.MemberInfo[] pathToMember, System.Text.StringBuilder rootElementXpath, out System.Xml.XmlNamespaceManager namespaces);
}
</pre>

## Namespace System.Runtime.Serialization.Json

### Type Changed: System.Runtime.Serialization.Json.JsonReaderWriterFactory

Added methods:

<pre style='color: green'>
	public static System.Xml.XmlDictionaryWriter CreateJsonWriter (System.IO.Stream stream, System.Text.Encoding encoding, bool ownsStream, bool indent);
	public static System.Xml.XmlDictionaryWriter CreateJsonWriter (System.IO.Stream stream, System.Text.Encoding encoding, bool ownsStream, bool indent, string indentChars);
</pre>

## Namespace System.Xml

### Type Changed: System.Xml.IXmlBinaryReaderInitializer

Modified methods:

```
public abstract void SetInput (System.IO.Stream stream, IXmlDictionary dictionary, XmlDictionaryReaderQuotas quota quotas, XmlBinaryReaderSession session, OnXmlDictionaryReaderClose onClose)
	public abstract void SetInput (byte[] buffer, int offset, int count, IXmlDictionary dictionary, XmlDictionaryReaderQuotas quota quotas, XmlBinaryReaderSession session, OnXmlDictionaryReaderClose onClose)
```

### Type Changed: System.Xml.IXmlTextReaderInitializer

Modified methods:

```
public abstract void SetInput (byte[] buffer, int offset, int count, System.Text.Encoding encoding, XmlDictionaryReaderQuotas quota quotas, OnXmlDictionaryReaderClose onClose)
	public abstract void SetInput (System.IO.Stream stream, System.Text.Encoding encoding, XmlDictionaryReaderQuotas quota quotas, OnXmlDictionaryReaderClose onClose)
```

### Type Changed: System.Xml.UniqueId

Modified constructors:

```
public UniqueId (byte[] id guid)
	public UniqueId (System.Guid id guid)
	public UniqueId (byte[] id guid, int offset)
	public UniqueId (char[] id chars, int offset, int count)
```

Modified methods:

```
public int ToCharArray (char[] array chars, int offset)
```

### Type Changed: System.Xml.XmlDictionaryReader

Removed method:

<pre style='color: red'>
	public virtual bool IsArray (out System.Type type);
</pre>

Modified methods:

```
public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, long[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, int[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, short[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, short[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, int[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, bool[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, bool[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, System.DateTime[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, System.Guid[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, System.Decimal[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, System.Decimal[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, double[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, double[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, System.DateTime[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, long[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, System.Guid[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, System.TimeSpan[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, System.TimeSpan[] array, int offset, int length count)
	public virtual int ReadArray (string localName, string namespaceUri, float[] array, int offset, int length count)
	public virtual int ReadArray (XmlDictionaryString localName, XmlDictionaryString namespaceUri, float[] array, int offset, int length count)
	public override object ReadContentAs (System.Type type, IXmlNamespaceResolver nsResolver namespaceResolver)
	public virtual int ReadValueAsBase64 (byte[] bytes buffer, int start offset, int length count)
	public virtual bool TryGetBase64ContentLength (out int count length)
```

Added methods:

<pre style='color: green'>
	public static XmlDictionaryReader CreateMtomReader (System.IO.Stream stream, System.Text.Encoding[] encodings, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (System.IO.Stream stream, System.Text.Encoding encoding, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (System.IO.Stream stream, System.Text.Encoding[] encodings, string contentType, XmlDictionaryReaderQuotas quotas, int maxBufferSize, OnXmlDictionaryReaderClose onClose);
	public static XmlDictionaryReader CreateMtomReader (byte[] buffer, int offset, int count, System.Text.Encoding encoding, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (byte[] buffer, int offset, int count, System.Text.Encoding[] encodings, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (byte[] buffer, int offset, int count, System.Text.Encoding[] encodings, string contentType, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (byte[] buffer, int offset, int count, System.Text.Encoding[] encodings, string contentType, XmlDictionaryReaderQuotas quotas, int maxBufferSize, OnXmlDictionaryReaderClose onClose);
	public static XmlDictionaryReader CreateMtomReader (System.IO.Stream stream, System.Text.Encoding[] encodings, string contentType, XmlDictionaryReaderQuotas quotas);
	public virtual void GetNonAtomizedNames (out string localName, out string namespaceUri);
</pre>

### Type Changed: System.Xml.XmlDictionaryReaderQuotas

Added property:

<pre style='color: green'>
	public XmlDictionaryReaderQuotaTypes ModifiedQuotas { get; }
</pre>

Modified methods:

```
public void CopyTo (XmlDictionaryReaderQuotas quota quotas)
```

### Type Changed: System.Xml.XmlDictionaryWriter

Modified methods:

```
public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, System.Guid[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, double[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, double[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, System.Decimal[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, System.Decimal[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, System.DateTime[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, System.DateTime[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, bool[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, bool[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, System.Guid[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, System.TimeSpan[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, float[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, float[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, long[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, long[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, int[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, int[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, short[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, XmlDictionaryString localName, XmlDictionaryString namespaceUri, short[] array, int offset, int length count)
	public virtual void WriteArray (string prefix, string localName, string namespaceUri, System.TimeSpan[] array, int offset, int length count)
	public virtual void WriteValue (UniqueId id value)
	public virtual void WriteValue (System.Guid guid value)
	public virtual void WriteValue (System.TimeSpan duration value)
```

Added methods:

<pre style='color: green'>
	public static XmlDictionaryWriter CreateMtomWriter (System.IO.Stream stream, System.Text.Encoding encoding, int maxSizeInBytes, string startInfo, string boundary, string startUri, bool writeMessageHeaders, bool ownsStream);
	public static XmlDictionaryWriter CreateMtomWriter (System.IO.Stream stream, System.Text.Encoding encoding, int maxSizeInBytes, string startInfo);
	public override System.Threading.Tasks.Task WriteBase64Async (byte[] buffer, int index, int count);
	public virtual System.Threading.Tasks.Task WriteValueAsync (IStreamProvider value);
</pre>

### New Type System.Xml.IFragmentCapableXmlDictionaryWriter

<pre style='color: green'>
public interface IFragmentCapableXmlDictionaryWriter {
	// properties
	public virtual bool CanFragment { get; }
	// methods
	public virtual void EndFragment ();
	public virtual void StartFragment (System.IO.Stream stream, bool generateSelfContainedTextFragment);
	public virtual void WriteFragment (byte[] buffer, int offset, int count);
}
</pre>

### New Type System.Xml.XmlDictionaryReaderQuotaTypes

<pre style='color: green'>
[Serializable]
[Flags]
public enum XmlDictionaryReaderQuotaTypes {
	MaxArrayLength = 4,
	MaxBytesPerRead = 8,
	MaxDepth = 1,
	MaxNameTableCharCount = 16,
	MaxStringContentLength = 2,
}
</pre>

   


 <hr>

<h1 id='System.ServiceModel'>System.ServiceModel.dll</h1>

## Namespace System.ServiceModel

### Type Changed: System.ServiceModel.DataContractFormatAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.FaultContractAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.MessageBodyMemberAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.MessageContractAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.MessageContractMemberAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.MessageHeaderArrayAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.MessageHeaderAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.MessageParameterAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.MessagePropertyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.OperationContractAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.ServiceContractAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.ServiceKnownTypeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.XmlSerializerFormatAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='System.ServiceModel.Web'>System.ServiceModel.Web.dll</h1>

## Namespace System.ServiceModel.Web

### Type Changed: System.ServiceModel.Web.WebGetAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.ServiceModel.Web.WebInvokeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='System.Web.Services'>System.Web.Services.dll</h1>

## Namespace System.Web.Services

### Type Changed: System.Web.Services.WebMethodAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.WebServiceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.WebServiceBindingAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace System.Web.Services.Configuration

### Type Changed: System.Web.Services.Configuration.XmlFormatExtensionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.Configuration.XmlFormatExtensionPointAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.Configuration.XmlFormatExtensionPrefixAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace System.Web.Services.Protocols

### Type Changed: System.Web.Services.Protocols.HttpMethodAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.Protocols.SoapDocumentMethodAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.Protocols.SoapDocumentServiceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.Protocols.SoapExtensionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.Protocols.SoapHeaderAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.Protocols.SoapRpcMethodAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: System.Web.Services.Protocols.SoapRpcServiceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='System.Xml'>System.Xml.dll</h1>

## Namespace System.Xml

### Type Changed: System.Xml.XmlNodeList

Added interface:

<pre style='color: green'>
	System.IDisposable
</pre>

Added method:

<pre style='color: green'>
	protected virtual void PrivateDisposeNodeList ();
</pre>

### Type Changed: System.Xml.XmlReaderSettings

Added constructor:

<pre style='color: green'>
	[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public XmlReaderSettings (XmlResolver resolver);
</pre>

### Type Changed: System.Xml.XmlTextReader

Obsoleted properties:

```
[Obsolete ("Use DtdProcessing property instead."]
	public bool ProhibitDtd { get; set; }
```

### Type Changed: System.Xml.XmlValidatingReader

Removed property:

<pre style='color: red'>
	public override XmlReaderSettings Settings { get; }
</pre>

### Type Changed: System.Xml.XmlWriterSettings

Added property:

<pre style='color: green'>
	public bool DoNotEscapeUriAttributes { get; set; }
</pre>

### New Type System.Xml.IApplicationResourceStreamResolver

<pre style='color: green'>
public interface IApplicationResourceStreamResolver {
	// methods

	[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public virtual System.IO.Stream GetApplicationResourceStream (System.Uri relativeUri);
}
</pre>

### New Type System.Xml.XmlSecureResolver

<pre style='color: green'>
public class XmlSecureResolver : System.Xml.XmlResolver {
	// constructors
	public XmlSecureResolver (XmlResolver resolver, string securityUrl);
	public XmlSecureResolver (XmlResolver resolver, System.Security.Policy.Evidence evidence);
	public XmlSecureResolver (XmlResolver resolver, System.Security.PermissionSet permissionSet);
	// properties
	public override System.Net.ICredentials Credentials { set; }
	// methods
	public static System.Security.Policy.Evidence CreateEvidenceForUrl (string securityUrl);
	public override object GetEntity (System.Uri absoluteUri, string role, System.Type ofObjectToReturn);
	public override System.Threading.Tasks.Task&lt;object&gt; GetEntityAsync (System.Uri absoluteUri, string role, System.Type ofObjectToReturn);
	public override System.Uri ResolveUri (System.Uri baseUri, string relativeUri);
}
</pre>

### New Type System.Xml.XmlXapResolver

<pre style='color: green'>
public class XmlXapResolver : System.Xml.XmlResolver {
	// constructors

	[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public XmlXapResolver ();
	// methods
	public override object GetEntity (System.Uri absoluteUri, string role, System.Type ofObjectToReturn);

	[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public static void RegisterApplicationResourceStreamResolver (IApplicationResourceStreamResolver appStreamResolver);
}
</pre>

## Namespace System.Xml.Schema

### Type Changed: System.Xml.Schema.XmlAtomicValue

Removed property:

<pre style='color: red'>
	public System.Decimal ValueAsDecimal { get; }
</pre>

### Type Changed: System.Xml.Schema.XmlSchemaFacet

### Removed Type  <span style='color: red'>System.Xml.Schema.XmlSchemaFacet.Facet</span>

## Namespace System.Xml.Serialization

### Type Changed: System.Xml.Serialization.XmlSerializationReader

### Type Changed: System.Xml.Serialization.XmlSerializationReader.CollectionFixup

Removed constructor:

<pre style='color: red'>
	public XmlSerializationReader (object collection, XmlSerializationCollectionFixupCallback callback, string id);
</pre>

Added constructor:

<pre style='color: green'>
	public XmlSerializationReader (object collection, XmlSerializationCollectionFixupCallback callback, object collectionItems);
</pre>

Removed property:

<pre style='color: red'>
	public object Id { get; }
</pre>

Added property:

<pre style='color: green'>
	public object CollectionItems { get; }
</pre>

### Removed Type  <span style='color: red'>System.Xml.Serialization.XmlSerializationReader.CollectionItemFixup</span>

## Namespace System.Xml.XPath

### Type Changed: System.Xml.XPath.XPathResultType

Modified fields:

```
Navigator = 4 1
```

## New Namespace System.Xml.Resolvers

### New Type System.Xml.Resolvers.XmlKnownDtds

<pre style='color: green'>
[Serializable]
[Flags]
public enum XmlKnownDtds {
	All = 65535,
	None = 0,
	Rss091 = 2,
	Xhtml10 = 1,
}
</pre>

### New Type System.Xml.Resolvers.XmlPreloadedResolver

<pre style='color: green'>
public class XmlPreloadedResolver : System.Xml.XmlResolver {
	// constructors
	public XmlPreloadedResolver ();
	public XmlPreloadedResolver (XmlKnownDtds preloadedDtds);
	public XmlPreloadedResolver (System.Xml.XmlResolver fallbackResolver);
	public XmlPreloadedResolver (System.Xml.XmlResolver fallbackResolver, XmlKnownDtds preloadedDtds);
	public XmlPreloadedResolver (System.Xml.XmlResolver fallbackResolver, XmlKnownDtds preloadedDtds, System.Collections.Generic.IEqualityComparer&lt;System.Uri&gt; uriComparer);
	// properties
	public override System.Net.ICredentials Credentials { set; }
	public System.Collections.Generic.IEnumerable&lt;System.Uri&gt; PreloadedUris { get; }
	// methods
	public void Add (System.Uri uri, byte[] value, int offset, int count);
	public void Add (System.Uri uri, string value);
	public void Add (System.Uri uri, byte[] value);
	public void Add (System.Uri uri, System.IO.Stream value);
	public override object GetEntity (System.Uri absoluteUri, string role, System.Type ofObjectToReturn);
	public override System.Threading.Tasks.Task&lt;object&gt; GetEntityAsync (System.Uri absoluteUri, string role, System.Type ofObjectToReturn);
	public void Remove (System.Uri uri);
	public override System.Uri ResolveUri (System.Uri baseUri, string relativeUri);
	public override bool SupportsType (System.Uri absoluteUri, System.Type type);
}
</pre>

## New Namespace System.Xml.XmlConfiguration

### New Type System.Xml.XmlConfiguration.XmlReaderSection

<pre style='color: green'>
public sealed class XmlReaderSection {
	// constructors
	public XmlReaderSection ();
}
</pre>

### New Type System.Xml.XmlConfiguration.XsltConfigSection

<pre style='color: green'>
public sealed class XsltConfigSection {
	// constructors
	public XsltConfigSection ();
}
</pre>

## New Namespace System.Xml.Xsl.Runtime

### New Type System.Xml.Xsl.Runtime.StringConcat

<pre style='color: green'>
public struct StringConcat {
	// properties
	public string Delimiter { get; set; }
	// methods
	public void Clear ();
	public void Concat (string value);
	public string GetResult ();
}
</pre>

   


 <hr>

<h1 id='Mono.Data.Sqlite'>Mono.Data.Sqlite.dll</h1>

## Namespace Mono.Data.Sqlite

### Type Changed: Mono.Data.Sqlite.SqliteFunctionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='Mono.Data.Tds'>Mono.Data.Tds.dll</h1>

## Namespace Mono.Data.Tds.Protocol

### Type Changed: Mono.Data.Tds.Protocol.TdsColumnType

Added values:

<pre style='color: green'>
	DateTime2 = 42,
	DateTimeOffset = 43,
</pre>

   


 <hr>

<h1 id='System.Net.Http'>System.Net.Http.dll</h1>

## Namespace System.Net.Http

### Removed Type  <span style='color: red'>System.Net.Http.CFNetworkHandler</span>

   


 <hr>

<h1 id='compat/monotouch'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.10.3" "8.13.0";
```

Added field:

<pre style='color: green'>
	public static const string SdkVersion = "8.4";
</pre>

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABNewPersonViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance

Added constructor:

<pre style='color: green'>
	protected ABPeoplePickerNavigationController (IntPtr handle);
</pre>

### Type Changed: MonoTouch.AddressBookUI.ABPersonViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIViewControllerRestoration
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

Added property:

<pre style='color: green'>
	public virtual bool ShouldShowLinkedPeople { get; set; }
</pre>

### Type Changed: MonoTouch.AddressBookUI.ABUnknownPersonViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.AudioQueue

Added method:

<pre style='color: green'>
	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, AudioStreamPacketDescription[] desc);
</pre>

### Type Changed: MonoTouch.AudioToolbox.SystemSound

Added constructor:

<pre style='color: green'>
	public SystemSound (uint soundId);
</pre>

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioUnit

Obsoleted methods:

```
[Obsolete (]
	public void SetAudioFormat (MonoTouch.AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
```

Added method:

<pre style='color: green'>
	public AudioUnitStatus SetFormat (MonoTouch.AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
</pre>

### Type Changed: MonoTouch.AudioUnit.ExtAudioFile

Modified properties:

```
public MonoTouch.AudioToolbox.AudioStreamBasicDescription ClientDataFormat { get; set; }
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAsset

Added property:

<pre style='color: green'>
	public virtual int UnusedTrackId { get; }
</pre>

### Type Changed: MonoTouch.AVFoundation.AVAudioSession

Obsoleted events:

```
[Obsolete (]
	public event System.EventHandler BeginInterruption;
	[Obsolete (]
	public event System.EventHandler<AVCategoryEventArgs> CategoryChanged;
	[Obsolete (]
	public event System.EventHandler EndInterruption;
	[Obsolete (]
	public event System.EventHandler<AVStatusEventArgs> InputAvailabilityChanged;
	[Obsolete (]
	public event System.EventHandler<AVChannelsEventArgs> InputChannelsChanged;
	[Obsolete (]
	public event System.EventHandler<AVChannelsEventArgs> OutputChannelsChanged;
	[Obsolete (]
	public event System.EventHandler<AVSampleRateEventArgs> SampleRateChanged;
```

### Type Changed: MonoTouch.AVFoundation.AVAudioSessionPortDescription

Obsoleted properties:

```
[Obsolete (]
	public AVAudioSessionChannelDescription[] DataSources { get; }
```

Modified properties:

```
public virtual AVAudioSessionChannelDescription[] DataSources { get; }
```

Added property:

<pre style='color: green'>
	public virtual AVAudioSessionDataSourceDescription[] DataSourceDescriptions { get; }
</pre>

### Type Changed: MonoTouch.AVFoundation.AVCaptureVideoStabilizationMode

Modified fields:

```
Auto = 3 -1
```

### Type Changed: MonoTouch.AVFoundation.AVCompositionTrackSegment

Added property:

<pre style='color: green'>
	public virtual bool Empty { get; }
</pre>

### Type Changed: MonoTouch.AVFoundation.AVUrlAsset

Added constructor:

<pre style='color: green'>
	public AVUrlAsset (MonoTouch.Foundation.NSUrl url);
</pre>

Added method:

<pre style='color: green'>
	public static AVUrlAsset Create (MonoTouch.Foundation.NSUrl url);
</pre>

### New Type MonoTouch.AVFoundation.AVErrorKeys

<pre style='color: green'>
public static class AVErrorKeys {
	// properties
	public static MonoTouch.Foundation.NSString Device { get; }
	public static MonoTouch.Foundation.NSString DiscontinuityFlags { get; }
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	public static MonoTouch.Foundation.NSString FileSize { get; }
	public static MonoTouch.Foundation.NSString FileType { get; }
	public static MonoTouch.Foundation.NSString MediaSubType { get; }
	public static MonoTouch.Foundation.NSString MediaType { get; }
	public static MonoTouch.Foundation.NSString PersistentTrackID { get; }
	public static MonoTouch.Foundation.NSString Pid { get; }
	public static MonoTouch.Foundation.NSString PresentationTimeStamp { get; }
	public static MonoTouch.Foundation.NSString RecordingSuccessfullyFinished { get; }
	public static MonoTouch.Foundation.NSString Time { get; }
}
</pre>

## Namespace MonoTouch.AVKit

### Type Changed: MonoTouch.AVKit.AVPlayerViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

## Namespace MonoTouch.CoreAnimation

### Type Changed: MonoTouch.CoreAnimation.CAAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

Added method:

<pre style='color: green'>
	public virtual void RunAction (string eventKey, MonoTouch.Foundation.NSObject obj, MonoTouch.Foundation.NSDictionary arguments);
</pre>

### Type Changed: MonoTouch.CoreAnimation.CAAnimationGroup

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: MonoTouch.CoreAnimation.CABasicAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: MonoTouch.CoreAnimation.CAPropertyAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: MonoTouch.CoreAnimation.CATransition

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

## Namespace MonoTouch.CoreAudioKit

### Type Changed: MonoTouch.CoreAudioKit.CABTMidiCentralViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUITableViewDataSource
	MonoTouch.UIKit.IUITableViewDelegate
	MonoTouch.UIKit.IUIScrollViewDelegate
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CABTMidiLocalPeripheralViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioSwitcherView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance

Added constructor:

<pre style='color: green'>
	protected CAInterAppAudioSwitcherView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioTransportView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance

Added constructor:

<pre style='color: green'>
	protected CAInterAppAudioTransportView (IntPtr handle);
</pre>

## Namespace MonoTouch.CoreData

### Type Changed: MonoTouch.CoreData.NSManagedObjectContext

Added method:

<pre style='color: green'>
	public virtual NSManagedObject GetExistingObject (NSManagedObjectID objectID, out MonoTouch.Foundation.NSError error);
</pre>

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFNetwork

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
</pre>

### Type Changed: MonoTouch.CoreFoundation.DispatchSource

Added method:

<pre style='color: green'>
	public void Suspend ();
</pre>

### Type Changed: MonoTouch.CoreFoundation.DispatchSource.Timer

Added constructor:

<pre style='color: green'>
	public DispatchSource (bool strict, DispatchQueue queue);
</pre>

### Type Changed: MonoTouch.CoreFoundation.DispatchTime

Modified constructors:

```
public DispatchTime (DispatchTime when, long delta deltaNanoseconds)
```

Added constructor:

<pre style='color: green'>
	public DispatchTime (DispatchTime when, System.TimeSpan delta);
</pre>

### New Type MonoTouch.CoreFoundation.CFMachPort

<pre style='color: green'>
public class CFMachPort : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CFMachPort (IntPtr handle);
	public CFMachPort (IntPtr handle, bool ownsHandle);
	// properties
	public virtual IntPtr Handle { get; }
	public bool IsValid { get; }
	public IntPtr MachPort { get; }
	// methods
	protected override void ~CFMachPort ();
	public CFRunLoopSource CreateRunLoopSource ();
	public virtual void Dispose ();
	public virtual void Dispose (bool disposing);
	public void Invalidate ();
}
</pre>

### New Type MonoTouch.CoreFoundation.CFMessagePort

<pre style='color: green'>
public class CFMessagePort : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public CFMessagePortContext Context { get; }
	public virtual IntPtr Handle { get; }
	public System.Action InvalidationCallback { get; set; }
	public bool IsRemote { get; }
	public bool IsValid { get; }
	public string Name { get; set; }
	// methods
	protected override void ~CFMessagePort ();
	protected void Check ();
	public static CFMessagePort CreateLocalPort (CFAllocator allocator, string name, CFMessagePort.CFMessagePortCallBack callback, CFMessagePortContext context);
	public static CFMessagePort CreateRemotePort (CFAllocator allocator, string name);
	public CFRunLoopSource CreateRunLoopSource ();
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	public void Invalidate ();
	public CFMessagePortSendRequestStatus SendRequest (int msgid, MonoTouch.Foundation.NSData data, double sendTimeout, double rcvTimeout, MonoTouch.Foundation.NSString replyMode, out MonoTouch.Foundation.NSData returnData);
	public void SetDispatchQueue (DispatchQueue queue);

	// inner types
	public sealed delegate CFMessagePortCallBack : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public CFMessagePort (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (int type, MonoTouch.Foundation.NSData data, System.AsyncCallback callback, object object);
		public virtual MonoTouch.Foundation.NSData EndInvoke (System.IAsyncResult result);
		public virtual MonoTouch.Foundation.NSData Invoke (int type, MonoTouch.Foundation.NSData data);
	}
}
</pre>

### New Type MonoTouch.CoreFoundation.CFMessagePortContext

<pre style='color: green'>
public class CFMessagePortContext {
	// constructors
	public CFMessagePortContext ();
	// properties
	public System.Func&lt;MonoTouch.Foundation.NSString&gt; CopyDescription { get; set; }
	public System.Action Release { get; set; }
	public System.Func&lt;MonoTouch.ObjCRuntime.INativeObject&gt; Retain { get; set; }
}
</pre>

### New Type MonoTouch.CoreFoundation.CFMessagePortSendRequestStatus

<pre style='color: green'>
[Serializable]
public enum CFMessagePortSendRequestStatus {
	BecameInvalidError = -5,
	IsInvalid = -3,
	ReceiveTimeout = -2,
	SendTimeout = -1,
	Success = 0,
	TransportError = -4,
}
</pre>

### New Type MonoTouch.CoreFoundation.CFNetworkErrors

<pre style='color: green'>
[Serializable]
public enum CFNetworkErrors {
	BackgroundSessionInUseByAnotherProcess = -996,
	BackgroundSessionWasDisconnected = -997,
	BadServerResponse = -1011,
	BadURL = -1000,
	CallIsActive = -1019,
	Cancelled = -999,
	CannotCloseFile = -3002,
	CannotConnectToHost = -1004,
	CannotCreateFile = -3000,
	CannotDecodeContentData = -1016,
	CannotDecodeRawData = -1015,
	CannotFindHost = -1003,
	CannotLoadFromNetwork = -2000,
	CannotMoveFile = -3005,
	CannotOpenFile = -3001,
	CannotParseCookieFile = -4000,
	CannotParseResponse = -1017,
	CannotRemoveFile = -3004,
	CannotWriteToFile = -3003,
	ClientCertificateRejected = -1205,
	ClientCertificateRequired = -1206,
	DataLengthExceedsMaximum = -1103,
	DataNotAllowed = -1020,
	DNSLookupFailed = -1006,
	DownloadDecodingFailedMidStream = -3006,
	DownloadDecodingFailedToComplete = -3007,
	FileDoesNotExist = -1100,
	FileIsDirectory = -1101,
	FtpUnexpectedStatusCode = 200,
	HostNotFound = 1,
	HostUnknown = 2,
	HttpAuthenticationTypeUnsupported = 300,
	HttpBadCredentials = 301,
	HttpBadProxyCredentials = 307,
	HttpBadURL = 305,
	HttpConnectionLost = 302,
	HttpParseFailure = 303,
	HttpProxyConnectionFailure = 306,
	HttpRedirectionLoopDetected = 304,
	HttpsProxyConnectionFailure = 310,
	HttpsProxyFailureUnexpectedResponseToConnectMethod = 311,
	HTTPTooManyRedirects = -1007,
	InternationalRoamingOff = -1018,
	NetServiceBadArgument = -72004,
	NetServiceCancel = -72005,
	NetServiceCollision = -72001,
	NetServiceDnsServiceFailure = -73000,
	NetServiceInProgress = -72003,
	NetServiceInvalid = -72006,
	NetServiceNotFound = -72002,
	NetServiceTimeout = -72007,
	NetServiceUnknown = -72000,
	NetworkConnectionLost = -1005,
	NoPermissionsToReadFile = -1102,
	NotConnectedToInternet = -1009,
	PacFileAuth = 309,
	PacFileError = 308,
	RedirectToNonExistentLocation = -1010,
	RequestBodyStreamExhausted = -1021,
	ResourceUnavailable = -1008,
	SecureConnectionFailed = -1200,
	ServerCertificateHasBadDate = -1201,
	ServerCertificateHasUnknownRoot = -1203,
	ServerCertificateNotYetValid = -1204,
	ServerCertificateUntrusted = -1202,
	Socks4IdConflict = 112,
	Socks4IdentdFailed = 111,
	Socks4RequestFailed = 110,
	Socks4UnknownStatusCode = 113,
	Socks5BadCredentials = 122,
	Socks5BadResponseAddr = 121,
	Socks5BadState = 120,
	Socks5NoAcceptableMethod = 124,
	Socks5UnsupportedNegotiationMethod = 123,
	SocksUnknownClientVersion = 100,
	SocksUnsupportedServerVersion = 101,
	TimedOut = -1001,
	Unknown = -998,
	UnsupportedURL = -1002,
	UserAuthenticationRequired = -1013,
	UserCancelledAuthentication = -1012,
	ZeroByteResource = -1014,
}
</pre>

### New Type MonoTouch.CoreFoundation.CFPreferences

<pre style='color: green'>
public static class CFPreferences {
	// fields
	public static MonoTouch.Foundation.NSString CurrentApplication;
	// methods
	public static void AddSuitePreferencesToApp (MonoTouch.Foundation.NSString applicationId, string suiteId);
	public static void AddSuitePreferencesToApp (string suiteId);
	public static void AddSuitePreferencesToApp (string applicationId, string suiteId);
	public static bool AppSynchronize (MonoTouch.Foundation.NSString applicationId);
	public static bool AppSynchronize (string applicationId);
	public static bool AppSynchronize ();
	public static bool AppValueIsForced (string key, MonoTouch.Foundation.NSString applicationId);
	public static bool AppValueIsForced (string key);
	public static bool AppValueIsForced (string key, string applicationId);
	public static bool GetAppBooleanValue (string key, MonoTouch.Foundation.NSString applicationId);
	public static bool GetAppBooleanValue (string key, string applicationId);
	public static bool GetAppBooleanValue (string key);
	public static int GetAppIntegerValue (string key, MonoTouch.Foundation.NSString applicationId);
	public static int GetAppIntegerValue (string key, string applicationId);
	public static int GetAppIntegerValue (string key);
	public static object GetAppValue (string key, string applicationId);
	public static object GetAppValue (string key, MonoTouch.Foundation.NSString applicationId);
	public static object GetAppValue (string key);
	public static void RemoveAppValue (string key);
	public static void RemoveAppValue (string key, MonoTouch.Foundation.NSString applicationId);
	public static void RemoveAppValue (string key, string applicationId);
	public static void RemoveSuitePreferencesFromApp (string suiteId);
	public static void RemoveSuitePreferencesFromApp (string applicationId, string suiteId);
	public static void RemoveSuitePreferencesFromApp (MonoTouch.Foundation.NSString applicationId, string suiteId);
	public static void SetAppValue (string key, object value);
	public static void SetAppValue (string key, object value, MonoTouch.Foundation.NSString applicationId);
	public static void SetAppValue (string key, object value, string applicationId);
}
</pre>

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGColorSpace

Obsoleted fields:

```
[Obsolete (]
	public static CGColorSpace Null;
```

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIFilterAttributes

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString TypeColor { get; }
</pre>

## Namespace MonoTouch.CoreMedia

### Type Changed: MonoTouch.CoreMedia.CMBlockBuffer

Added property:

<pre style='color: green'>
	public bool IsEmpty { get; }
</pre>

Added methods:

<pre style='color: green'>
	public CMBlockBufferError AccessDataBytes (uint offset, uint length, IntPtr temporaryBlock, ref IntPtr returnedPointer);
	public CMBlockBufferError AppendBuffer (CMBlockBuffer targetBuffer, uint offsetToData, uint dataLength, CMBlockBufferFlags flags);
	public CMBlockBufferError AppendMemoryBlock (IntPtr memoryBlock, uint blockLength, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags);
	public CMBlockBufferError AssureBlockMemory ();
	public static CMBlockBuffer CreateContiguous (CMBlockBuffer sourceBuffer, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public static CMBlockBuffer CreateFromBuffer (CMBlockBuffer targetBuffer, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public static CMBlockBuffer CreateFromMemoryBlock (IntPtr memoryBlock, uint blockLength, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public CMBlockBufferError FillDataBytes (byte fillByte, uint offsetIntoDestination, uint dataLength);
	public CMBlockBufferError GetDataPointer (uint offset, out uint lengthAtOffset, out uint totalLength, ref IntPtr dataPointer);
	public bool IsRangeContiguous (uint offset, uint length);
	public CMBlockBufferError ReplaceDataBytes (IntPtr sourceBytes, uint offsetIntoDestination, uint dataLength);
</pre>

### Type Changed: MonoTouch.CoreMedia.CMBlockBufferError

Added value:

<pre style='color: green'>
	InsufficientSpace = -12708,
</pre>

### Type Changed: MonoTouch.CoreMedia.CMVideoFormatDescription

Added methods:

<pre style='color: green'>
	public static CMVideoFormatDescription FromH264ParameterSets (System.Collections.Generic.List&lt;System.Byte[]&gt; parameterSets, int nalUnitHeaderLength, out CMFormatDescriptionError error);
	public byte[] GetH264ParameterSet (uint index, out uint parameterSetCount, out int nalUnitHeaderLength, out CMFormatDescriptionError error);
</pre>

### New Type MonoTouch.CoreMedia.CMCustomBlockAllocator

<pre style='color: green'>
public class CMCustomBlockAllocator : System.IDisposable {
	// constructors
	public CMCustomBlockAllocator ();
	// methods
	protected override void ~CMCustomBlockAllocator ();
	public virtual IntPtr Allocate (uint sizeInBytes);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public virtual void Free (IntPtr doomedMemoryBlock, uint sizeInBytes);
}
</pre>

## Namespace MonoTouch.CoreMotion

### Type Changed: MonoTouch.CoreMotion.CMMotionActivity


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoTouch.Foundation.NSObject</span></span>

 <span style='color:green'>MonoTouch.CoreMotion.CMLogItem</span>

## Namespace MonoTouch.EventKit

### Type Changed: MonoTouch.EventKit.EKParticipant

Added method:

<pre style='color: green'>
	public virtual MonoTouch.AddressBook.ABRecord GetRecord (MonoTouch.AddressBook.ABAddressBook addressBook);
</pre>

## Namespace MonoTouch.EventKitUI

### Type Changed: MonoTouch.EventKitUI.EKCalendarChooser

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.EventKitUI.EKEventEditViewController.EKEventEditViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected EKEventEditViewController (IntPtr handle);
</pre>

### Type Changed: MonoTouch.EventKitUI.EKEventViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

## Namespace MonoTouch.ExternalAccessory

### New Type MonoTouch.ExternalAccessory.EABluetoothAccessoryPickerError

<pre style='color: green'>
[Serializable]
public enum EABluetoothAccessoryPickerError {
	AlreadyConnected = 0,
	Cancelled = 2,
	Failed = 3,
	NotFound = 1,
}
</pre>

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSArray

Added methods:

<pre style='color: green'>
	public virtual bool Contains (NSObject anObject);
	public virtual uint IndexOf (NSObject anObject);
</pre>

### Type Changed: MonoTouch.Foundation.NSCoder

Added methods:

<pre style='color: green'>
	public virtual IntPtr DecodeBytes (out uint length);
	public virtual IntPtr DecodeBytes (string key, out uint length);
	public byte[] DecodeBytes ();
	public bool TryDecodeBool (string key, out bool result);
	public bool TryDecodeBytes (string key, out byte[] result);
	public bool TryDecodeDouble (string key, out double result);
	public bool TryDecodeFloat (string key, out float result);
	public bool TryDecodeInt (string key, out int result);
	public bool TryDecodeLong (string key, out long result);
	public bool TryDecodeObject (string key, out NSObject result);
</pre>

### Type Changed: MonoTouch.Foundation.NSData

Added methods:

<pre style='color: green'>
	public virtual void GetBytes (IntPtr buffer, uint length);
	public virtual void GetBytes (IntPtr buffer, NSRange range);
	public virtual NSData Subdata (NSRange range);
</pre>

### Type Changed: MonoTouch.Foundation.NSDate

Added methods:

<pre style='color: green'>
	public virtual NSComparisonResult Compare (NSDate other);
	public virtual NSDate EarlierDate (NSDate anotherDate);
	public virtual bool IsEqualToDate (NSDate other);
	public virtual NSDate LaterDate (NSDate anotherDate);
</pre>

### Type Changed: MonoTouch.Foundation.NSDateFormatter

Added property:

<pre style='color: green'>
	public virtual bool DoesRelativeDateFormatting { get; set; }
</pre>

### Type Changed: MonoTouch.Foundation.NSError

Added property:

<pre style='color: green'>
	public static NSString CFNetworkErrorDomain { get; }
</pre>

### Type Changed: MonoTouch.Foundation.NSFormatter

Added methods:

<pre style='color: green'>
	public NSAttributedString GetAttributedString (NSObject obj, MonoTouch.UIKit.UIStringAttributes attrs);
	public virtual NSAttributedString GetAttributedString (NSObject obj, NSDictionary attrs);
	public virtual bool GetObjectValue (out NSObject obj, string str, out NSString error);
	public virtual bool IsPartialStringValid (string partialString, out string newString, out NSString error);
	public virtual bool IsPartialStringValid (out string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out NSString error);
</pre>

### Type Changed: MonoTouch.Foundation.NSMetadataQuery

Added properties:

<pre style='color: green'>
	public static NSString QueryUpdateAddedItemsKey { get; }
	public static NSString QueryUpdateChangedItemsKey { get; }
	public static NSString QueryUpdateRemovedItemsKey { get; }
</pre>

### Type Changed: MonoTouch.Foundation.NSMutableData

Added methods:

<pre style='color: green'>
	public virtual void ReplaceBytes (NSRange range, IntPtr buffer);
	public virtual void ReplaceBytes (NSRange range, IntPtr buffer, uint length);
	public virtual void ResetBytes (NSRange range);
</pre>

### Type Changed: MonoTouch.Foundation.NSObject

Added method:

<pre style='color: green'>
	public virtual void PrepareForInterfaceBuilder ();
</pre>

### Type Changed: MonoTouch.Foundation.NSOperation

Added property:

<pre style='color: green'>
	public virtual System.Action CompletionBlock { get; set; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void WaitUntilFinishedNS ();
```

Added method:

<pre style='color: green'>
	public virtual void WaitUntilFinished ();
</pre>

### Type Changed: MonoTouch.Foundation.NSPurgeableData

Added interface:

<pre style='color: green'>
	INSDiscardableContent
</pre>

Added property:

<pre style='color: green'>
	public virtual bool IsContentDiscarded { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool BeginContentAccess ();
	public virtual void DiscardContentIfPossible ();
	public virtual void EndContentAccess ();
</pre>

### Type Changed: MonoTouch.Foundation.NSSortDescriptor

Added constructor:

<pre style='color: green'>
	public NSSortDescriptor (string key, bool ascending, NSComparator comparator);
</pre>

### Type Changed: MonoTouch.Foundation.NSTimeZone

Added method:

<pre style='color: green'>
	public static NSTimeZone FromGMT (int seconds);
</pre>

### Type Changed: MonoTouch.Foundation.NSUndoManager

Added method:

<pre style='color: green'>
	public virtual void SetActionName (string actionName);
</pre>

### Type Changed: MonoTouch.Foundation.NSUrl

Added properties:

<pre style='color: green'>
	public virtual NSUrl FilePathUrl { get; }
	public virtual NSUrl FileReferenceUrl { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSUrl FromBookmarkData (NSData data, NSUrlBookmarkResolutionOptions options, NSUrl relativeToUrl, out bool isStale, out NSError error);
	public static NSData GetBookmarkData (NSUrl bookmarkFileUrl, out NSError error);
	public static bool WriteBookmarkData (NSData data, NSUrl bookmarkFileUrl, NSUrlBookmarkCreationOptions options, out NSError error);
</pre>

### Type Changed: MonoTouch.Foundation.NSUrlError

Added values:

<pre style='color: green'>
	CallIsActive = -1019,
	ClientCertificateRequired = -1206,
	DataNotAllowed = -1020,
	InternationalRoamingOff = -1018,
	RequestBodyStreamExhausted = -1021,
</pre>

### Type Changed: MonoTouch.Foundation.NSUrlSessionUploadTask


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoTouch.Foundation.NSUrlSessionTask</span></span>

 <span style='color:green'>MonoTouch.Foundation.NSUrlSessionDataTask</span>

### New Type MonoTouch.Foundation.INSDiscardableContent

<pre style='color: green'>
public interface INSDiscardableContent : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual bool IsContentDiscarded { get; }
	// methods
	public virtual bool BeginContentAccess ();
	public virtual void DiscardContentIfPossible ();
	public virtual void EndContentAccess ();
}
</pre>

### New Type MonoTouch.Foundation.NSCondition

<pre style='color: green'>
public class NSCondition : MonoTouch.Foundation.NSObject, INSLocking, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSCondition ();
	public NSCondition (NSCoder coder);
	public NSCondition (NSObjectFlag t);
	public NSCondition (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Broadcast ();
	public virtual void Lock ();
	public virtual void Signal ();
	public virtual void Unlock ();
	public virtual void Wait ();
	public virtual bool WaitUntilDate (NSDate limit);
}
</pre>

### New Type MonoTouch.Foundation.NSConditionLock

<pre style='color: green'>
public class NSConditionLock : MonoTouch.Foundation.NSObject, INSLocking, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSConditionLock ();
	public NSConditionLock (NSCoder coder);
	public NSConditionLock (NSObjectFlag t);
	public NSConditionLock (IntPtr handle);
	public NSConditionLock (int condition);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual int Condition { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool LockWhenCondition (int condition, NSDate limit);
	public virtual void LockWhenCondition (int condition);
	public virtual bool TryLock ();
	public virtual bool TryLockWhenCondition (int condition);
	public virtual void Unlock ();
	public virtual void UnlockWithCondition (int condition);
}
</pre>

### New Type MonoTouch.Foundation.NSDataDetector

<pre style='color: green'>
public class NSDataDetector : MonoTouch.Foundation.NSRegularExpression, INSCoding, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSDataDetector ();
	public NSDataDetector (NSCoder coder);
	public NSDataDetector (NSObjectFlag t);
	public NSDataDetector (IntPtr handle);
	// properties
	public virtual NSTextCheckingTypes CheckingTypes { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	public static NSDataDetector Create (NSTextCheckingTypes checkingTypes, out NSError error);
}
</pre>

### New Type MonoTouch.Foundation.NSDiscardableContent_Extensions

<pre style='color: green'>
public static class NSDiscardableContent_Extensions {
}
</pre>

### New Type MonoTouch.Foundation.NSLock

<pre style='color: green'>
public class NSLock : MonoTouch.Foundation.NSObject, INSLocking, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSLock ();
	public NSLock (NSCoder coder);
	public NSLock (NSObjectFlag t);
	public NSLock (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool TryLock ();
	public virtual void Unlock ();
}
</pre>

### New Type MonoTouch.Foundation.NSMatchEnumerator

<pre style='color: green'>
public sealed delegate NSMatchEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSMatchEnumerator (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSTextCheckingResult result, NSMatchingFlags flags, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (NSTextCheckingResult result, NSMatchingFlags flags, ref bool stop);
}
</pre>

### New Type MonoTouch.Foundation.NSMatchingFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSMatchingFlags {
	Completed = 2,
	HitEnd = 4,
	InternalError = 16,
	Progress = 1,
	RequiredEnd = 8,
}
</pre>

### New Type MonoTouch.Foundation.NSMatchingOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSMatchingOptions {
	Anchored = 4,
	ReportCompletion = 2,
	ReportProgress = 1,
	WithoutAnchoringBounds = 16,
	WithTransparentBounds = 8,
}
</pre>

### New Type MonoTouch.Foundation.NSPredicateSupport_NSArray

<pre style='color: green'>
public static class NSPredicateSupport_NSArray {
	// methods
	public static NSArray FilterUsingPredicate (NSArray This, NSArray array);
}
</pre>

### New Type MonoTouch.Foundation.NSPredicateSupport_NSMutableArray

<pre style='color: green'>
public static class NSPredicateSupport_NSMutableArray {
	// methods
	public static void FilterUsingPredicate (NSMutableArray This, NSPredicate predicate);
}
</pre>

### New Type MonoTouch.Foundation.NSPredicateSupport_NSMutableSet

<pre style='color: green'>
public static class NSPredicateSupport_NSMutableSet {
	// methods
	public static void FilterUsingPredicate (NSMutableSet This, NSPredicate predicate);
}
</pre>

### New Type MonoTouch.Foundation.NSPredicateSupport_NSSet

<pre style='color: green'>
public static class NSPredicateSupport_NSSet {
	// methods
	public static NSSet FilterUsingPredicate (NSSet This, NSPredicate predicate);
}
</pre>

### New Type MonoTouch.Foundation.NSRecursiveLock

<pre style='color: green'>
public class NSRecursiveLock : MonoTouch.Foundation.NSObject, INSLocking, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSRecursiveLock ();
	public NSRecursiveLock (NSCoder coder);
	public NSRecursiveLock (NSObjectFlag t);
	public NSRecursiveLock (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool TryLock ();
	public virtual void Unlock ();
}
</pre>

### New Type MonoTouch.Foundation.NSRegularExpression

<pre style='color: green'>
public class NSRegularExpression : MonoTouch.Foundation.NSObject, INSCoding, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSRegularExpression ();
	public NSRegularExpression (NSCoder coder);
	public NSRegularExpression (NSObjectFlag t);
	public NSRegularExpression (IntPtr handle);
	public NSRegularExpression (NSString pattern, NSRegularExpressionOptions options, out NSError error);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint NumberOfCaptureGroups { get; }
	public virtual NSRegularExpressionOptions Options { get; }
	public virtual NSString Pattern { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EnumerateMatches (NSString str, NSMatchingOptions options, NSRange range, NSMatchEnumerator enumerator);
	public virtual NSTextCheckingResult FindFirstMatch (string str, NSMatchingOptions options, NSRange range);
	public static NSString GetEscapedPattern (NSString str);
	public static NSString GetEscapedTemplate (NSString str);
	public virtual NSString[] GetMatches (NSString str, NSMatchingOptions options, NSRange range);
	public virtual uint GetNumberOfMatches (NSString str, NSMatchingOptions options, NSRange range);
	public virtual NSRange GetRangeOfFirstMatch (string str, NSMatchingOptions options, NSRange range);
	public virtual NSString GetReplacementString (NSTextCheckingResult result, NSString str, int offset, NSString template);
	public virtual string ReplaceMatches (string sourceString, NSMatchingOptions options, NSRange range, string template);
	public virtual uint ReplaceMatches (NSMutableString mutableString, NSMatchingOptions options, NSRange range, NSString template);
}
</pre>

### New Type MonoTouch.Foundation.NSRegularExpressionOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSRegularExpressionOptions {
	AllowCommentsAndWhitespace = 2,
	AnchorsMatchLines = 16,
	CaseInsensitive = 1,
	DotMatchesLineSeparators = 8,
	IgnoreMetacharacters = 4,
	UseUnicodeWordBoundaries = 64,
}
</pre>

### New Type MonoTouch.Foundation.NSValueTransformer

<pre style='color: green'>
public abstract class NSValueTransformer : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSValueTransformer ();
	public NSValueTransformer (NSCoder coder);
	public NSValueTransformer (NSObjectFlag t);
	public NSValueTransformer (IntPtr handle);
	// properties
	public static bool AllowsReverseTransformation { get; }
	public static NSString BooleanTransformerName { get; }
	public override IntPtr ClassHandle { get; }
	public static NSString IsNilTransformerName { get; }
	public static NSString NSIsNotNilTransformerName { get; }
	public static NSString NSKeyedUnarchiveFromDataTransformerName { get; }
	public static MonoTouch.ObjCRuntime.Class TransformedValueClass { get; }
	public static NSString UnarchiveFromDataTransformerName { get; }
	public static string[] ValueTransformerNames { get; }
	// methods
	public static NSValueTransformer GetValueTransformer (string name);
	public virtual NSObject ReverseTransformedValue (NSObject value);
	public static void SetValueTransformer (NSValueTransformer transformer, string name);
	public virtual NSObject TransformedValue (NSObject value);
}
</pre>

### New Type MonoTouch.Foundation.ProtocolMemberAttribute

<pre style='color: green'>
public sealed class ProtocolMemberAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public ProtocolMemberAttribute ();
	// properties
	public MonoTouch.ObjCRuntime.ArgumentSemantic ArgumentSemantic { get; set; }
	public string GetterSelector { get; set; }
	public bool IsProperty { get; set; }
	public bool IsRequired { get; set; }
	public bool IsStatic { get; set; }
	public bool IsVariadic { get; set; }
	public string Name { get; set; }
	public bool[] ParameterByRef { get; set; }
	public System.Type[] ParameterType { get; set; }
	public System.Type PropertyType { get; set; }
	public System.Type ReturnType { get; set; }
	public string Selector { get; set; }
	public string SetterSelector { get; set; }
}
</pre>

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKAchievementViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.GameKit.GKAchievementViewController.GKAchievementViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected GKAchievementViewController (IntPtr handle);
</pre>

### Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected GKFriendRequestComposeViewController (IntPtr handle);
</pre>

### Type Changed: MonoTouch.GameKit.GKGameCenterViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.GameKit.GKLeaderboardViewController.GKLeaderboardViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected GKLeaderboardViewController (IntPtr handle);
</pre>

### Type Changed: MonoTouch.GameKit.GKMatchmakerViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoTouch.UIKit.UIViewController</span></span>

 <span style='color:green'>MonoTouch.UIKit.UINavigationController</span>

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected GKTurnBasedMatchmakerViewController (IntPtr handle);
</pre>

### Type Changed: MonoTouch.GameKit.GKVoiceChat

Obsoleted methods:

```
[Obsolete (]
	public virtual void SetMute (bool isMuted, GKPlayer player);
```

Added method:

<pre style='color: green'>
	public virtual void SetMute (bool isMuted, string playerID);
</pre>

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKBaseEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

### Type Changed: MonoTouch.GLKit.GLKReflectionMapEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

### Type Changed: MonoTouch.GLKit.GLKSkyboxEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

### Type Changed: MonoTouch.GLKit.GLKView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.GLKit.GLKView.GLKViewAppearance

Added constructor:

<pre style='color: green'>
	protected GLKView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.GLKit.GLKViewController

Added interfaces:

<pre style='color: green'>
	IGLKViewDelegate
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

Added method:

<pre style='color: green'>
	public virtual void DrawInRect (GLKView view, System.Drawing.RectangleF rect);
</pre>

## Namespace MonoTouch.HealthKit

### Type Changed: MonoTouch.HealthKit.HKQuantityTypeIdentifierKey

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString ElectrodermalActivity { get; }
</pre>

## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADBannerView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.iAd.ADBannerView.ADBannerViewAppearance

Added constructor:

<pre style='color: green'>
	protected ADBannerView (IntPtr handle);
</pre>

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MapKit.MKAnnotationView.MKAnnotationViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKAnnotationView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MapKit.MKCircle

Modified properties:

```
public override virtual string Subtitle { get; }
	public override virtual string Title { get; }
```

### Type Changed: MonoTouch.MapKit.MKCircleView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MapKit.MKCircleView.MKCircleViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKCircleView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MapKit.MKMapView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MapKit.MKMapView.MKMapViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKMapView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MapKit.MKOverlayPathView.MKOverlayPathViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKOverlayPathView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MapKit.MKOverlayView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MapKit.MKOverlayView.MKOverlayViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKOverlayView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView.MKPinAnnotationViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKPinAnnotationView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MapKit.MKPolygon

Modified properties:

```
public override virtual string Subtitle { get; }
	public override virtual string Title { get; }
```

### Type Changed: MonoTouch.MapKit.MKPolygonView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MapKit.MKPolygonView.MKPolygonViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKPolygonView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MapKit.MKPolyline

Modified properties:

```
public override virtual string Subtitle { get; }
	public override virtual string Title { get; }
```

### Type Changed: MonoTouch.MapKit.MKPolylineView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MapKit.MKPolylineView.MKPolylineViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKPolylineView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MapKit.MKUserTrackingBarButtonItem

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
</pre>

### Type Changed: MonoTouch.MapKit.MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance

Added constructor:

<pre style='color: green'>
	protected MKUserTrackingBarButtonItem (IntPtr handle);
</pre>

## Namespace MonoTouch.MediaAccessibility

### New Type MonoTouch.MediaAccessibility.MAAudibleMedia

<pre style='color: green'>
public static class MAAudibleMedia {
	// properties
	public static MonoTouch.Foundation.NSString SettingsChangedNotification { get; }
	// methods
	public static string[] GetPreferredCharacteristics ();

	// inner types
	public static class Notifications {
		// methods
		public static MonoTouch.Foundation.NSObject ObserveSettingsChanged (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type MonoTouch.MediaAccessibility.MAMediaCharacteristic

<pre style='color: green'>
public static class MAMediaCharacteristic {
	// properties
	public static MonoTouch.Foundation.NSString DescribesMusicAndSoundForAccessibility { get; }
	public static MonoTouch.Foundation.NSString DescribesVideoForAccessibility { get; }
	public static MonoTouch.Foundation.NSString TranscribesSpokenDialogForAccessibility { get; }
}
</pre>

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMediaPickerController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView.MPVolumeViewAppearance

Added constructor:

<pre style='color: green'>
	protected MPVolumeView (IntPtr handle);
</pre>

## Namespace MonoTouch.MessageUI

### Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MessageUI.MFMailComposeViewController.MFMailComposeViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected MFMailComposeViewController (IntPtr handle);
</pre>

### Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController.MFMessageComposeViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected MFMessageComposeViewController (IntPtr handle);
</pre>

## Namespace MonoTouch.Metal

### Type Changed: MonoTouch.Metal.MTLRegion

Added methods:

<pre style='color: green'>
	public static MTLRegion Create1D (int x, int width);
	public static MTLRegion Create2D (int x, int y, int width, int height);
	public static MTLRegion Create3D (int x, int y, int z, int width, int height, int depth);
</pre>

### Type Changed: MonoTouch.Metal.MTLVertexAttribute

Added property:

<pre style='color: green'>
	public virtual string Name { get; }
</pre>

## Namespace MonoTouch.MultipeerConnectivity

### Type Changed: MonoTouch.MultipeerConnectivity.MCBrowserViewController

Added interfaces:

<pre style='color: green'>
	IMCNearbyServiceBrowserDelegate
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidNotStartBrowsingForPeers (MCNearbyServiceBrowser browser, MonoTouch.Foundation.NSError error);
	public virtual void FoundPeer (MCNearbyServiceBrowser browser, MCPeerID peerID, MonoTouch.Foundation.NSDictionary info);
	public virtual void LostPeer (MCNearbyServiceBrowser browser, MCPeerID peerID);
</pre>

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.BlockDescriptor

Added field:

<pre style='color: green'>
	public IntPtr signature;
</pre>

### Type Changed: MonoTouch.ObjCRuntime.BlockFlags

Added value:

<pre style='color: green'>
	BLOCK_HAS_SIGNATURE = 1073741824,
</pre>

### Type Changed: MonoTouch.ObjCRuntime.BlockLiteral

Added method:

<pre style='color: green'>
	public static bool IsManagedBlock (IntPtr block);
</pre>

### Type Changed: MonoTouch.ObjCRuntime.iOSAttribute

Added constructor:

<pre style='color: green'>
	public iOSAttribute (byte major, byte minor, byte subminor);
</pre>

### Type Changed: MonoTouch.ObjCRuntime.MacAttribute

Added constructors:

<pre style='color: green'>
	public MacAttribute (byte major, byte minor);
	public MacAttribute (byte major, byte minor, byte subminor);
	public MacAttribute (byte major, byte minor, byte subminor, bool onlyOn64);
</pre>

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

<pre style='color: green'>
	public static bool bool_objc_msgSend_IntPtr_ref_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref IntPtr arg2, ref IntPtr arg3);
	public static bool bool_objc_msgSend_ref_IntPtr_out_NSRange_IntPtr_NSRange_ref_IntPtr (IntPtr receiver, IntPtr selector, ref IntPtr arg1, out MonoTouch.Foundation.NSRange arg2, IntPtr arg3, MonoTouch.Foundation.NSRange arg4, ref IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_ref_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref IntPtr arg2, ref IntPtr arg3);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_out_NSRange_IntPtr_NSRange_ref_IntPtr (IntPtr receiver, IntPtr selector, ref IntPtr arg1, out MonoTouch.Foundation.NSRange arg2, IntPtr arg3, MonoTouch.Foundation.NSRange arg4, ref IntPtr arg5);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1);
	public static IntPtr IntPtr_objc_msgSend_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1);
	public static IntPtr IntPtr_objc_msgSendSuper_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static void NSRange_objc_msgSend_stret_IntPtr_UInt64_NSRange (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static void NSRange_objc_msgSendSuper_stret_IntPtr_UInt64_NSRange (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSend_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
	public static uint UInt32_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static uint UInt32_objc_msgSendSuper_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
	public static uint UInt32_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSend_NSRange_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, uint arg3);
	public static void void_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSendSuper_NSRange_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, uint arg3);
</pre>

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added value:

<pre style='color: green'>
	Mac_10_10_3 = 2825757768286208,
</pre>

## Namespace MonoTouch.PassKit

### Type Changed: MonoTouch.PassKit.PKAddPassesViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.PassKit.PKPaymentAuthorizationViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.PassKit.PKPaymentButton

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.PassKit.PKPaymentButton.PKPaymentButtonAppearance

Added constructor:

<pre style='color: green'>
	protected PKPaymentButton (IntPtr handle);
</pre>

## Namespace MonoTouch.QuickLook

### Type Changed: MonoTouch.QuickLook.QLPreviewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

## Namespace MonoTouch.SceneKit

### Type Changed: MonoTouch.SceneKit.SCNLight

Obsoleted methods:

```
[Obsolete (]
	public virtual MonoTouch.Foundation.NSObject GetAttribute (MonoTouch.Foundation.NSString lightAttribute);
	[Obsolete (]
	public virtual void SetAttribute (MonoTouch.Foundation.NSObject value, MonoTouch.Foundation.NSString attribuetKey);
```

### Type Changed: MonoTouch.SceneKit.SCNParticleSystem

Added properties:

<pre style='color: green'>
	public SCNPropertyControllers PropertyControllers { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary WeakPropertyControllers { get; set; }
</pre>

Modified methods:

```
public virtual void HandleEvent (SCNParticleEvent evnt, MonoTouch.Foundation.NSString[] properties particleProperties, SCNParticleEventHandler handler)
```

### Type Changed: MonoTouch.SceneKit.SCNView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.SceneKit.SCNView.SCNViewAppearance

Added constructor:

<pre style='color: green'>
	protected SCNView (IntPtr handle);
</pre>

### New Type MonoTouch.SceneKit.SCNParticleProperty

<pre style='color: green'>
public static class SCNParticleProperty {
	// properties
	public static MonoTouch.Foundation.NSString Angle { get; }
	public static MonoTouch.Foundation.NSString AngularVelocity { get; }
	public static MonoTouch.Foundation.NSString Bounce { get; }
	public static MonoTouch.Foundation.NSString Charge { get; }
	public static MonoTouch.Foundation.NSString Color { get; }
	public static MonoTouch.Foundation.NSString Frame { get; }
	public static MonoTouch.Foundation.NSString FrameRate { get; }
	public static MonoTouch.Foundation.NSString Friction { get; }
	public static MonoTouch.Foundation.NSString Life { get; }
	public static MonoTouch.Foundation.NSString Opacity { get; }
	public static MonoTouch.Foundation.NSString Position { get; }
	public static MonoTouch.Foundation.NSString RotationAxis { get; }
	public static MonoTouch.Foundation.NSString Size { get; }
	public static MonoTouch.Foundation.NSString Velocity { get; }
}
</pre>

### New Type MonoTouch.SceneKit.SCNPhysicsCollisionCategory

<pre style='color: green'>
[Serializable]
public enum SCNPhysicsCollisionCategory {
	All = 4294967295,
	Default = 1,
	None = 0,
	Static = 2,
}
</pre>

### New Type MonoTouch.SceneKit.SCNPropertyControllers

<pre style='color: green'>
public class SCNPropertyControllers {
	// constructors
	public SCNPropertyControllers ();
	// properties
	public SCNParticlePropertyController Angle { get; set; }
	public SCNParticlePropertyController AngularVelocity { get; set; }
	public SCNParticlePropertyController Bounce { get; set; }
	public SCNParticlePropertyController Charge { get; set; }
	public SCNParticlePropertyController Color { get; set; }
	public SCNParticlePropertyController Frame { get; set; }
	public SCNParticlePropertyController FrameRate { get; set; }
	public SCNParticlePropertyController Friction { get; set; }
	public SCNParticlePropertyController Life { get; set; }
	public SCNParticlePropertyController Opacity { get; set; }
	public SCNParticlePropertyController Position { get; set; }
	public SCNParticlePropertyController RotationAxis { get; set; }
	public SCNParticlePropertyController Size { get; set; }
	public SCNParticlePropertyController Velocity { get; set; }
}
</pre>

## Namespace MonoTouch.Social

### Type Changed: MonoTouch.Social.SLComposeServiceViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Social.SLComposeViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKFieldNode

Obsoleted methods:

```
[Obsolete (]
	public static SKFieldNode CraeteVortexField ();
```

Added method:

<pre style='color: green'>
	public static SKFieldNode CreateVortexField ();
</pre>

### Type Changed: MonoTouch.SpriteKit.SKView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.SpriteKit.SKView.SKViewAppearance

Added constructor:

<pre style='color: green'>
	protected SKView (IntPtr handle);
</pre>

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.SKStoreProductViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

## Namespace MonoTouch.Twitter

### Type Changed: MonoTouch.Twitter.TWTweetComposeViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.NSIdentifier

Obsoleted methods:

```
[Obsolete (]
	public static string Identifier (NSLayoutConstraint This);
```

Added methods:

<pre style='color: green'>
	public static string GetIdentifier (NSLayoutConstraint This);
	public static void SetIdentifier (NSLayoutConstraint This, string id);
</pre>

### Type Changed: MonoTouch.UIKit.UIActionSheet

Added constructors:

<pre style='color: green'>
	public UIActionSheet (string title, IUIActionSheetDelegate del);
	public UIActionSheet (string title, IUIActionSheetDelegate del, string cancelTitle, string destroy, string[] other);
</pre>

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIActionSheet.UIActionSheetAppearance

Added constructor:

<pre style='color: green'>
	protected UIActionSheet (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView.UIActivityIndicatorViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIActivityIndicatorView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIActivityItemProvider

Added interface:

<pre style='color: green'>
	IUIActivityItemSource
</pre>

Added methods:

<pre style='color: green'>
	public virtual string GetDataTypeIdentifierForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
	public virtual MonoTouch.Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
	public virtual MonoTouch.Foundation.NSObject GetPlaceholderData (UIActivityViewController activityViewController);
	public virtual string GetSubjectForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
	public virtual UIImage GetThumbnailImageForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType, System.Drawing.SizeF suggestedSize);
</pre>

### Type Changed: MonoTouch.UIKit.UIActivityViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIAdaptivePresentationControllerDelegate

Obsoleted methods:

```
[Obsolete (]
	public virtual UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style);
```

Added method:

<pre style='color: green'>
	public virtual UIModalPresentationStyle GetAdaptivePresentationStyle (UIPresentationController controller, UITraitCollection traitCollection);
</pre>

### Type Changed: MonoTouch.UIKit.UIAdaptivePresentationControllerDelegate_Extensions

Obsoleted methods:

```
[Obsolete (]
	public static UIViewController GetAdaptivePresentationStyle (IUIAdaptivePresentationControllerDelegate This, UIPresentationController controller, UIModalPresentationStyle style);
```

Added method:

<pre style='color: green'>
	public static UIModalPresentationStyle GetAdaptivePresentationStyle (IUIAdaptivePresentationControllerDelegate This, UIPresentationController controller, UITraitCollection traitCollection);
</pre>

### Type Changed: MonoTouch.UIKit.UIAlertController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIAlertView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIAlertView.UIAlertViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIAlertView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Added interface:

<pre style='color: green'>
	IUIAppearance
</pre>

### Type Changed: MonoTouch.UIKit.UIBarButtonItem.UIBarButtonItemAppearance

Added constructor:

<pre style='color: green'>
	protected UIBarButtonItem (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIBarItem

Added interface:

<pre style='color: green'>
	IUIAppearance
</pre>

### Type Changed: MonoTouch.UIKit.UIBarItem.UIBarItemAppearance

Added constructor:

<pre style='color: green'>
	protected UIBarItem (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIButton

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIButton.UIButtonAppearance

Added constructor:

<pre style='color: green'>
	protected UIButton (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionReusableView.UICollectionReusableViewAppearance

Added constructor:

<pre style='color: green'>
	protected UICollectionReusableView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionView.UICollectionViewAppearance

Added constructor:

<pre style='color: green'>
	protected UICollectionView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewCell.UICollectionViewCellAppearance

Added constructor:

<pre style='color: green'>
	protected UICollectionViewCell (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UICollectionViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIControl

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIControl.UIControlAppearance

Added constructor:

<pre style='color: green'>
	protected UIControl (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIDatePicker

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIDatePicker.UIDatePickerAppearance

Added constructor:

<pre style='color: green'>
	protected UIDatePicker (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIDocumentMenuViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIDocumentPickerExtensionViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIDocumentPickerViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIImagePickerController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIImageView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIImageView.UIImageViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIImageView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIInputView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIInputView.UIInputViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIInputView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIInputViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UILabel

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UILabel.UILabelAppearance

Added constructor:

<pre style='color: green'>
	protected UILabel (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UINavigationBar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UINavigationBar.UINavigationBarAppearance

Added constructor:

<pre style='color: green'>
	protected UINavigationBar (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UINavigationController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIPageControl

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIPageControl.UIPageControlAppearance

Added constructor:

<pre style='color: green'>
	protected UIPageControl (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIPageViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIPickerView

Added interfaces:

<pre style='color: green'>
	IUITableViewDataSource
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual UITableViewCell GetCell (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual int RowsInSection (UITableView tableview, int section);
</pre>

### Type Changed: MonoTouch.UIKit.UIPickerView.UIPickerViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIPickerView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIPopoverBackgroundView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIPopoverController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIPopoverPresentationControllerDelegate

Obsoleted methods:

```
[Obsolete (]
	public virtual UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style);
```

Modified methods:

```
public override virtual UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style)
```

Added method:

<pre style='color: green'>
	public override UIModalPresentationStyle GetAdaptivePresentationStyle (UIPresentationController controller, UITraitCollection traitCollection);
</pre>

### Type Changed: MonoTouch.UIKit.UIProgressView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIProgressView.UIProgressViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIProgressView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIReferenceLibraryViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIRefreshControl.UIRefreshControlAppearance

Added constructor:

<pre style='color: green'>
	protected UIRefreshControl (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIScrollView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIScrollView.UIScrollViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIScrollView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UISearchBar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UISearchBar.UISearchBarAppearance

Added constructor:

<pre style='color: green'>
	protected UISearchBar (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UISearchController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UISegmentedControl.UISegmentedControlAppearance

Added constructor:

<pre style='color: green'>
	protected UISegmentedControl (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UISlider

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UISlider.UISliderAppearance

Added constructor:

<pre style='color: green'>
	protected UISlider (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UISplitViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIStepper

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIStepper.UIStepperAppearance

Added constructor:

<pre style='color: green'>
	protected UIStepper (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UISwitch

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UISwitch.UISwitchAppearance

Added constructor:

<pre style='color: green'>
	protected UISwitch (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UITabBar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UITabBar.UITabBarAppearance

Added constructor:

<pre style='color: green'>
	protected UITabBar (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UITabBarController

Added interfaces:

<pre style='color: green'>
	IUITabBarDelegate
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidBeginCustomizingItems (UITabBar tabbar, UITabBarItem[] items);
	public virtual void DidEndCustomizingItems (UITabBar tabbar, UITabBarItem[] items, bool changed);
	public virtual void ItemSelected (UITabBar tabbar, UITabBarItem item);
	public virtual void WillBeginCustomizingItems (UITabBar tabbar, UITabBarItem[] items);
	public virtual void WillEndCustomizingItems (UITabBar tabbar, UITabBarItem[] items, bool changed);
</pre>

### Type Changed: MonoTouch.UIKit.UITabBarItem

Added interface:

<pre style='color: green'>
	IUIAppearance
</pre>

### Type Changed: MonoTouch.UIKit.UITabBarItem.UITabBarItemAppearance

Added constructor:

<pre style='color: green'>
	protected UITabBarItem (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UITableView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UITableView.UITableViewAppearance

Added constructor:

<pre style='color: green'>
	protected UITableView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewCell

Added interfaces:

<pre style='color: green'>
	IUIGestureRecognizerDelegate
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool ShouldBegin (UIGestureRecognizer recognizer);
	public virtual bool ShouldBeRequiredToFailBy (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
	public virtual bool ShouldReceiveTouch (UIGestureRecognizer recognizer, UITouch touch);
	public virtual bool ShouldRecognizeSimultaneously (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
	public virtual bool ShouldRequireFailureOf (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewCell.UITableViewCellAppearance

Added constructor:

<pre style='color: green'>
	protected UITableViewCell (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewController

Added interfaces:

<pre style='color: green'>
	IUITableViewDataSource
	IUITableViewDelegate
	IUIScrollViewDelegate
	IUIAppearanceContainer
</pre>

Modified methods:

```
public virtual int RowsInSection (UITableView tableview tableView, int section)
```

Added methods:

<pre style='color: green'>
	public virtual void DecelerationEnded (UIScrollView scrollView);
	public virtual void DecelerationStarted (UIScrollView scrollView);
	public virtual void DidZoom (UIScrollView scrollView);
	public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
	public virtual void DraggingStarted (UIScrollView scrollView);
	public virtual void ScrollAnimationEnded (UIScrollView scrollView);
	public virtual void Scrolled (UIScrollView scrollView);
	public virtual void ScrolledToTop (UIScrollView scrollView);
	public virtual bool ShouldScrollToTop (UIScrollView scrollView);
	public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);
	public virtual void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
	public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
	public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance

Added constructor:

<pre style='color: green'>
	protected UITableViewHeaderFooterView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UITextField

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UITextField.UITextFieldAppearance

Added constructor:

<pre style='color: green'>
	protected UITextField (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UITextView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UITextView.UITextViewAppearance

Added constructor:

<pre style='color: green'>
	protected UITextView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIToolbar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIToolbar.UIToolbarAppearance

Added constructor:

<pre style='color: green'>
	protected UIToolbar (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIVideoEditorController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIView.UIViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIVisualEffectView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIVisualEffectView.UIVisualEffectViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIVisualEffectView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIWebView

Added interfaces:

<pre style='color: green'>
	IUIScrollViewDelegate
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DecelerationEnded (UIScrollView scrollView);
	public virtual void DecelerationStarted (UIScrollView scrollView);
	public virtual void DidZoom (UIScrollView scrollView);
	public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
	public virtual void DraggingStarted (UIScrollView scrollView);
	public virtual void ScrollAnimationEnded (UIScrollView scrollView);
	public virtual void Scrolled (UIScrollView scrollView);
	public virtual void ScrolledToTop (UIScrollView scrollView);
	public virtual bool ShouldScrollToTop (UIScrollView scrollView);
	public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);
	public virtual void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
	public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
	public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);
</pre>

### Type Changed: MonoTouch.UIKit.UIWebView.UIWebViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIWebView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIWindow

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIWindow.UIWindowAppearance

Added constructor:

<pre style='color: green'>
	protected UIWindow (IntPtr handle);
</pre>

### New Type MonoTouch.UIKit.UIInterfaceOrientationExtensions

<pre style='color: green'>
public static class UIInterfaceOrientationExtensions {
	// methods
	public static bool IsLandscape (UIInterfaceOrientation orientation);
	public static bool IsPortrait (UIInterfaceOrientation orientation);
}
</pre>

## Namespace MonoTouch.WatchKit

### Type Changed: MonoTouch.WatchKit.WKInterfaceController

Added method:

<pre style='color: green'>
	public void PushController (string name, string context);
</pre>

## Namespace MonoTouch.WebKit

### Type Changed: MonoTouch.WebKit.WKWebView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.WebKit.WKWebView.WKWebViewAppearance

Added constructor:

<pre style='color: green'>
	protected WKWebView (IntPtr handle);
</pre>

   


 <hr>

<h1 id='compat/MonoTouch.Dialog-1'>MonoTouch.Dialog-1.dll</h1>

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement.TextWithImageCellView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIGestureRecognizerDelegate
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Dialog.DialogViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUITableViewDataSource
	MonoTouch.UIKit.IUITableViewDelegate
	MonoTouch.UIKit.IUIScrollViewDelegate
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Dialog.GlassButton

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Dialog.MessageSummaryView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Dialog.RefreshTableHeaderView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

   


 <hr>

<h1 id='compat/MonoTouch.NUnitLite'>MonoTouch.NUnitLite.dll</h1>

## Namespace MonoTouch.NUnit.UI

### Type Changed: MonoTouch.NUnit.UI.TouchViewController

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUITableViewDataSource
	MonoTouch.UIKit.IUITableViewDelegate
	MonoTouch.UIKit.IUIScrollViewDelegate
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

   


 <hr>

<h1 id='compat/OpenTK'>OpenTK.dll</h1>

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

   


 <hr>

<h1 id='compat/OpenTK-1.0'>OpenTK-1.0.dll</h1>

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

   


 <hr>

<h1 id='reference/MonoTouch.Dialog-1'>MonoTouch.Dialog-1.dll</h1>

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement.TextWithImageCellView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIGestureRecognizerDelegate
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Dialog.DialogViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUITableViewDataSource
	UIKit.IUITableViewDelegate
	UIKit.IUIScrollViewDelegate
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Dialog.GlassButton

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Dialog.MessageSummaryView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.Dialog.RefreshTableHeaderView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

   


 <hr>

<h1 id='reference/MonoTouch.NUnitLite'>MonoTouch.NUnitLite.dll</h1>

## Namespace MonoTouch.NUnit.UI

### Type Changed: MonoTouch.NUnit.UI.TouchViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUITableViewDataSource
	UIKit.IUITableViewDelegate
	UIKit.IUIScrollViewDelegate
	UIKit.IUIAppearanceContainer
</pre>

   


 <hr>

<h1 id='reference/OpenTK-1.0'>OpenTK-1.0.dll</h1>

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace AddressBookUI

### Type Changed: AddressBookUI.ABNewPersonViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: AddressBookUI.ABPeoplePickerNavigationController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: AddressBookUI.ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance

Added constructor:

<pre style='color: green'>
	protected ABPeoplePickerNavigationController (IntPtr handle);
</pre>

### Type Changed: AddressBookUI.ABPersonViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIViewControllerRestoration
	UIKit.IUIAppearanceContainer
</pre>

Added property:

<pre style='color: green'>
	public virtual bool ShouldShowLinkedPeople { get; set; }
</pre>

### Type Changed: AddressBookUI.ABUnknownPersonViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

## Namespace AudioToolbox

### Type Changed: AudioToolbox.AudioQueue

Added method:

<pre style='color: green'>
	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, AudioStreamPacketDescription[] desc);
</pre>

### Type Changed: AudioToolbox.SystemSound

Added constructor:

<pre style='color: green'>
	public SystemSound (uint soundId);
</pre>

## Namespace AudioUnit

### Type Changed: AudioUnit.AudioUnit

Obsoleted methods:

```
[Obsolete (]
	public void SetAudioFormat (AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
```

Added method:

<pre style='color: green'>
	public AudioUnitStatus SetFormat (AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
</pre>

### Type Changed: AudioUnit.ExtAudioFile

Modified properties:

```
public AudioToolbox.AudioStreamBasicDescription ClientDataFormat { get; set; }
```

## Namespace AVFoundation

### Type Changed: AVFoundation.AVAsset

Added property:

<pre style='color: green'>
	public virtual int UnusedTrackId { get; }
</pre>

### Type Changed: AVFoundation.AVAudioSession

Obsoleted events:

```
[Obsolete (]
	public event System.EventHandler BeginInterruption;
	[Obsolete (]
	public event System.EventHandler<AVCategoryEventArgs> CategoryChanged;
	[Obsolete (]
	public event System.EventHandler EndInterruption;
	[Obsolete (]
	public event System.EventHandler<AVStatusEventArgs> InputAvailabilityChanged;
	[Obsolete (]
	public event System.EventHandler<AVChannelsEventArgs> InputChannelsChanged;
	[Obsolete (]
	public event System.EventHandler<AVChannelsEventArgs> OutputChannelsChanged;
	[Obsolete (]
	public event System.EventHandler<AVSampleRateEventArgs> SampleRateChanged;
```

### Type Changed: AVFoundation.AVAudioSessionPortDescription

Obsoleted properties:

```
[Obsolete (]
	public AVAudioSessionChannelDescription[] DataSources { get; }
```

Modified properties:

```
public virtual AVAudioSessionChannelDescription[] DataSources { get; }
```

Added property:

<pre style='color: green'>
	public virtual AVAudioSessionDataSourceDescription[] DataSourceDescriptions { get; }
</pre>

### Type Changed: AVFoundation.AVCaptureVideoStabilizationMode

Modified fields:

```
Auto = 3 -1
```

### Type Changed: AVFoundation.AVCompositionTrackSegment

Added property:

<pre style='color: green'>
	public virtual bool Empty { get; }
</pre>

### Type Changed: AVFoundation.AVUrlAsset

Added constructor:

<pre style='color: green'>
	public AVUrlAsset (Foundation.NSUrl url);
</pre>

Added method:

<pre style='color: green'>
	public static AVUrlAsset Create (Foundation.NSUrl url);
</pre>

### New Type AVFoundation.AVErrorKeys

<pre style='color: green'>
public static class AVErrorKeys {
	// properties
	public static Foundation.NSString Device { get; }
	public static Foundation.NSString DiscontinuityFlags { get; }
	public static Foundation.NSString ErrorDomain { get; }
	public static Foundation.NSString FileSize { get; }
	public static Foundation.NSString FileType { get; }
	public static Foundation.NSString MediaSubType { get; }
	public static Foundation.NSString MediaType { get; }
	public static Foundation.NSString PersistentTrackID { get; }
	public static Foundation.NSString Pid { get; }
	public static Foundation.NSString PresentationTimeStamp { get; }
	public static Foundation.NSString RecordingSuccessfullyFinished { get; }
	public static Foundation.NSString Time { get; }
}
</pre>

## Namespace AVKit

### Type Changed: AVKit.AVPlayerViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

## Namespace CoreAnimation

### Type Changed: CoreAnimation.CAAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

Added method:

<pre style='color: green'>
	public virtual void RunAction (string eventKey, Foundation.NSObject obj, Foundation.NSDictionary arguments);
</pre>

### Type Changed: CoreAnimation.CAAnimationGroup

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: CoreAnimation.CABasicAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: CoreAnimation.CAKeyFrameAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: CoreAnimation.CAPropertyAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: CoreAnimation.CATransition

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

## Namespace CoreAudioKit

### Type Changed: CoreAudioKit.CABTMidiCentralViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUITableViewDataSource
	UIKit.IUITableViewDelegate
	UIKit.IUIScrollViewDelegate
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: CoreAudioKit.CABTMidiLocalPeripheralViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: CoreAudioKit.CAInterAppAudioSwitcherView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: CoreAudioKit.CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance

Added constructor:

<pre style='color: green'>
	protected CAInterAppAudioSwitcherView (IntPtr handle);
</pre>

### Type Changed: CoreAudioKit.CAInterAppAudioTransportView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: CoreAudioKit.CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance

Added constructor:

<pre style='color: green'>
	protected CAInterAppAudioTransportView (IntPtr handle);
</pre>

## Namespace CoreData

### Type Changed: CoreData.NSManagedObjectContext

Added method:

<pre style='color: green'>
	public virtual NSManagedObject GetExistingObject (NSManagedObjectID objectID, out Foundation.NSError error);
</pre>

## Namespace CoreFoundation

### Type Changed: CoreFoundation.CFNetwork

Added property:

<pre style='color: green'>
	public static Foundation.NSString ErrorDomain { get; }
</pre>

### Type Changed: CoreFoundation.DispatchSource

Added method:

<pre style='color: green'>
	public void Suspend ();
</pre>

### Type Changed: CoreFoundation.DispatchSource.Timer

Added constructor:

<pre style='color: green'>
	public DispatchSource (bool strict, DispatchQueue queue);
</pre>

### Type Changed: CoreFoundation.DispatchTime

Modified constructors:

```
public DispatchTime (DispatchTime when, long delta deltaNanoseconds)
```

Added constructor:

<pre style='color: green'>
	public DispatchTime (DispatchTime when, System.TimeSpan delta);
</pre>

### New Type CoreFoundation.CFMachPort

<pre style='color: green'>
public class CFMachPort : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CFMachPort (IntPtr handle);
	public CFMachPort (IntPtr handle, bool ownsHandle);
	// properties
	public virtual IntPtr Handle { get; }
	public bool IsValid { get; }
	public IntPtr MachPort { get; }
	// methods
	protected override void ~CFMachPort ();
	public CFRunLoopSource CreateRunLoopSource ();
	public virtual void Dispose ();
	public virtual void Dispose (bool disposing);
	public void Invalidate ();
}
</pre>

### New Type CoreFoundation.CFMessagePort

<pre style='color: green'>
public class CFMessagePort : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public CFMessagePortContext Context { get; }
	public virtual IntPtr Handle { get; }
	public System.Action InvalidationCallback { get; set; }
	public bool IsRemote { get; }
	public bool IsValid { get; }
	public string Name { get; set; }
	// methods
	protected override void ~CFMessagePort ();
	protected void Check ();
	public static CFMessagePort CreateLocalPort (CFAllocator allocator, string name, CFMessagePort.CFMessagePortCallBack callback, CFMessagePortContext context);
	public static CFMessagePort CreateRemotePort (CFAllocator allocator, string name);
	public CFRunLoopSource CreateRunLoopSource ();
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	public void Invalidate ();
	public CFMessagePortSendRequestStatus SendRequest (int msgid, Foundation.NSData data, double sendTimeout, double rcvTimeout, Foundation.NSString replyMode, out Foundation.NSData returnData);
	public void SetDispatchQueue (DispatchQueue queue);

	// inner types
	public sealed delegate CFMessagePortCallBack : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public CFMessagePort (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (int type, Foundation.NSData data, System.AsyncCallback callback, object object);
		public virtual Foundation.NSData EndInvoke (System.IAsyncResult result);
		public virtual Foundation.NSData Invoke (int type, Foundation.NSData data);
	}
}
</pre>

### New Type CoreFoundation.CFMessagePortContext

<pre style='color: green'>
public class CFMessagePortContext {
	// constructors
	public CFMessagePortContext ();
	// properties
	public System.Func&lt;Foundation.NSString&gt; CopyDescription { get; set; }
	public System.Action Release { get; set; }
	public System.Func&lt;ObjCRuntime.INativeObject&gt; Retain { get; set; }
}
</pre>

### New Type CoreFoundation.CFMessagePortSendRequestStatus

<pre style='color: green'>
[Serializable]
public enum CFMessagePortSendRequestStatus {
	BecameInvalidError = -5,
	IsInvalid = -3,
	ReceiveTimeout = -2,
	SendTimeout = -1,
	Success = 0,
	TransportError = -4,
}
</pre>

### New Type CoreFoundation.CFNetworkErrors

<pre style='color: green'>
[Serializable]
public enum CFNetworkErrors {
	BackgroundSessionInUseByAnotherProcess = -996,
	BackgroundSessionWasDisconnected = -997,
	BadServerResponse = -1011,
	BadURL = -1000,
	CallIsActive = -1019,
	Cancelled = -999,
	CannotCloseFile = -3002,
	CannotConnectToHost = -1004,
	CannotCreateFile = -3000,
	CannotDecodeContentData = -1016,
	CannotDecodeRawData = -1015,
	CannotFindHost = -1003,
	CannotLoadFromNetwork = -2000,
	CannotMoveFile = -3005,
	CannotOpenFile = -3001,
	CannotParseCookieFile = -4000,
	CannotParseResponse = -1017,
	CannotRemoveFile = -3004,
	CannotWriteToFile = -3003,
	ClientCertificateRejected = -1205,
	ClientCertificateRequired = -1206,
	DataLengthExceedsMaximum = -1103,
	DataNotAllowed = -1020,
	DNSLookupFailed = -1006,
	DownloadDecodingFailedMidStream = -3006,
	DownloadDecodingFailedToComplete = -3007,
	FileDoesNotExist = -1100,
	FileIsDirectory = -1101,
	FtpUnexpectedStatusCode = 200,
	HostNotFound = 1,
	HostUnknown = 2,
	HttpAuthenticationTypeUnsupported = 300,
	HttpBadCredentials = 301,
	HttpBadProxyCredentials = 307,
	HttpBadURL = 305,
	HttpConnectionLost = 302,
	HttpParseFailure = 303,
	HttpProxyConnectionFailure = 306,
	HttpRedirectionLoopDetected = 304,
	HttpsProxyConnectionFailure = 310,
	HttpsProxyFailureUnexpectedResponseToConnectMethod = 311,
	HTTPTooManyRedirects = -1007,
	InternationalRoamingOff = -1018,
	NetServiceBadArgument = -72004,
	NetServiceCancel = -72005,
	NetServiceCollision = -72001,
	NetServiceDnsServiceFailure = -73000,
	NetServiceInProgress = -72003,
	NetServiceInvalid = -72006,
	NetServiceNotFound = -72002,
	NetServiceTimeout = -72007,
	NetServiceUnknown = -72000,
	NetworkConnectionLost = -1005,
	NoPermissionsToReadFile = -1102,
	NotConnectedToInternet = -1009,
	PacFileAuth = 309,
	PacFileError = 308,
	RedirectToNonExistentLocation = -1010,
	RequestBodyStreamExhausted = -1021,
	ResourceUnavailable = -1008,
	SecureConnectionFailed = -1200,
	ServerCertificateHasBadDate = -1201,
	ServerCertificateHasUnknownRoot = -1203,
	ServerCertificateNotYetValid = -1204,
	ServerCertificateUntrusted = -1202,
	Socks4IdConflict = 112,
	Socks4IdentdFailed = 111,
	Socks4RequestFailed = 110,
	Socks4UnknownStatusCode = 113,
	Socks5BadCredentials = 122,
	Socks5BadResponseAddr = 121,
	Socks5BadState = 120,
	Socks5NoAcceptableMethod = 124,
	Socks5UnsupportedNegotiationMethod = 123,
	SocksUnknownClientVersion = 100,
	SocksUnsupportedServerVersion = 101,
	TimedOut = -1001,
	Unknown = -998,
	UnsupportedURL = -1002,
	UserAuthenticationRequired = -1013,
	UserCancelledAuthentication = -1012,
	ZeroByteResource = -1014,
}
</pre>

### New Type CoreFoundation.CFPreferences

<pre style='color: green'>
public static class CFPreferences {
	// fields
	public static Foundation.NSString CurrentApplication;
	// methods
	public static void AddSuitePreferencesToApp (Foundation.NSString applicationId, string suiteId);
	public static void AddSuitePreferencesToApp (string suiteId);
	public static void AddSuitePreferencesToApp (string applicationId, string suiteId);
	public static bool AppSynchronize (Foundation.NSString applicationId);
	public static bool AppSynchronize (string applicationId);
	public static bool AppSynchronize ();
	public static bool AppValueIsForced (string key, Foundation.NSString applicationId);
	public static bool AppValueIsForced (string key);
	public static bool AppValueIsForced (string key, string applicationId);
	public static bool GetAppBooleanValue (string key, Foundation.NSString applicationId);
	public static bool GetAppBooleanValue (string key, string applicationId);
	public static bool GetAppBooleanValue (string key);
	public static nint GetAppIntegerValue (string key, Foundation.NSString applicationId);
	public static nint GetAppIntegerValue (string key, string applicationId);
	public static nint GetAppIntegerValue (string key);
	public static object GetAppValue (string key, string applicationId);
	public static object GetAppValue (string key, Foundation.NSString applicationId);
	public static object GetAppValue (string key);
	public static void RemoveAppValue (string key);
	public static void RemoveAppValue (string key, Foundation.NSString applicationId);
	public static void RemoveAppValue (string key, string applicationId);
	public static void RemoveSuitePreferencesFromApp (string suiteId);
	public static void RemoveSuitePreferencesFromApp (string applicationId, string suiteId);
	public static void RemoveSuitePreferencesFromApp (Foundation.NSString applicationId, string suiteId);
	public static void SetAppValue (string key, object value);
	public static void SetAppValue (string key, object value, Foundation.NSString applicationId);
	public static void SetAppValue (string key, object value, string applicationId);
}
</pre>

## Namespace CoreGraphics

### Type Changed: CoreGraphics.CGColorSpace

Obsoleted fields:

```
[Obsolete (]
	public static CGColorSpace Null;
```

## Namespace CoreImage

### Type Changed: CoreImage.CIFilterAttributes

Added property:

<pre style='color: green'>
	public static Foundation.NSString TypeColor { get; }
</pre>

## Namespace CoreMedia

### Type Changed: CoreMedia.CMBlockBuffer

Added property:

<pre style='color: green'>
	public bool IsEmpty { get; }
</pre>

Added methods:

<pre style='color: green'>
	public CMBlockBufferError AccessDataBytes (uint offset, uint length, IntPtr temporaryBlock, ref IntPtr returnedPointer);
	public CMBlockBufferError AppendBuffer (CMBlockBuffer targetBuffer, uint offsetToData, uint dataLength, CMBlockBufferFlags flags);
	public CMBlockBufferError AppendMemoryBlock (IntPtr memoryBlock, uint blockLength, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags);
	public CMBlockBufferError AssureBlockMemory ();
	public static CMBlockBuffer CreateContiguous (CMBlockBuffer sourceBuffer, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public static CMBlockBuffer CreateFromBuffer (CMBlockBuffer targetBuffer, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public static CMBlockBuffer CreateFromMemoryBlock (IntPtr memoryBlock, uint blockLength, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public CMBlockBufferError FillDataBytes (byte fillByte, uint offsetIntoDestination, uint dataLength);
	public CMBlockBufferError GetDataPointer (uint offset, out uint lengthAtOffset, out uint totalLength, ref IntPtr dataPointer);
	public bool IsRangeContiguous (uint offset, uint length);
	public CMBlockBufferError ReplaceDataBytes (IntPtr sourceBytes, uint offsetIntoDestination, uint dataLength);
</pre>

### Type Changed: CoreMedia.CMBlockBufferError

Added value:

<pre style='color: green'>
	InsufficientSpace = -12708,
</pre>

### Type Changed: CoreMedia.CMVideoFormatDescription

Added methods:

<pre style='color: green'>
	public static CMVideoFormatDescription FromH264ParameterSets (System.Collections.Generic.List&lt;System.Byte[]&gt; parameterSets, int nalUnitHeaderLength, out CMFormatDescriptionError error);
	public byte[] GetH264ParameterSet (uint index, out uint parameterSetCount, out int nalUnitHeaderLength, out CMFormatDescriptionError error);
</pre>

### New Type CoreMedia.CMCustomBlockAllocator

<pre style='color: green'>
public class CMCustomBlockAllocator : System.IDisposable {
	// constructors
	public CMCustomBlockAllocator ();
	// methods
	protected override void ~CMCustomBlockAllocator ();
	public virtual IntPtr Allocate (uint sizeInBytes);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public virtual void Free (IntPtr doomedMemoryBlock, uint sizeInBytes);
}
</pre>

## Namespace CoreMotion

### Type Changed: CoreMotion.CMMotionActivity


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Foundation.NSObject</span></span>

 <span style='color:green'>CoreMotion.CMLogItem</span>

## Namespace EventKit

### Type Changed: EventKit.EKParticipant

Added method:

<pre style='color: green'>
	public virtual AddressBook.ABRecord GetRecord (AddressBook.ABAddressBook addressBook);
</pre>

## Namespace EventKitUI

### Type Changed: EventKitUI.EKCalendarChooser

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: EventKitUI.EKEventEditViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: EventKitUI.EKEventEditViewController.EKEventEditViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected EKEventEditViewController (IntPtr handle);
</pre>

### Type Changed: EventKitUI.EKEventViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

## Namespace ExternalAccessory

### New Type ExternalAccessory.EABluetoothAccessoryPickerError

<pre style='color: green'>
[Serializable]
public enum EABluetoothAccessoryPickerError {
	AlreadyConnected = 0,
	Cancelled = 2,
	Failed = 3,
	NotFound = 1,
}
</pre>

## Namespace Foundation

### Type Changed: Foundation.NSArray

Added methods:

<pre style='color: green'>
	public virtual bool Contains (NSObject anObject);
	public virtual uint IndexOf (NSObject anObject);
</pre>

### Type Changed: Foundation.NSCoder

Added methods:

<pre style='color: green'>
	public virtual IntPtr DecodeBytes (out uint length);
	public virtual IntPtr DecodeBytes (string key, out uint length);
	public byte[] DecodeBytes ();
	public bool TryDecodeBool (string key, out bool result);
	public bool TryDecodeBytes (string key, out byte[] result);
	public bool TryDecodeDouble (string key, out double result);
	public bool TryDecodeFloat (string key, out float result);
	public bool TryDecodeInt (string key, out int result);
	public bool TryDecodeLong (string key, out long result);
	public bool TryDecodeNInt (string key, out nint result);
	public bool TryDecodeObject (string key, out NSObject result);
</pre>

### Type Changed: Foundation.NSData

Added methods:

<pre style='color: green'>
	public virtual void GetBytes (IntPtr buffer, uint length);
	public virtual void GetBytes (IntPtr buffer, NSRange range);
	public virtual NSData Subdata (NSRange range);
</pre>

### Type Changed: Foundation.NSDate

Added methods:

<pre style='color: green'>
	public virtual NSComparisonResult Compare (NSDate other);
	public virtual NSDate EarlierDate (NSDate anotherDate);
	public virtual bool IsEqualToDate (NSDate other);
	public virtual NSDate LaterDate (NSDate anotherDate);
</pre>

### Type Changed: Foundation.NSDateFormatter

Added property:

<pre style='color: green'>
	public virtual bool DoesRelativeDateFormatting { get; set; }
</pre>

### Type Changed: Foundation.NSError

Added property:

<pre style='color: green'>
	public static NSString CFNetworkErrorDomain { get; }
</pre>

### Type Changed: Foundation.NSFormatter

Added methods:

<pre style='color: green'>
	public NSAttributedString GetAttributedString (NSObject obj, UIKit.UIStringAttributes attrs);
	public virtual NSAttributedString GetAttributedString (NSObject obj, NSDictionary attrs);
	public virtual bool GetObjectValue (out NSObject obj, string str, out NSString error);
	public virtual bool IsPartialStringValid (string partialString, out string newString, out NSString error);
	public virtual bool IsPartialStringValid (out string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out NSString error);
</pre>

### Type Changed: Foundation.NSMetadataQuery

Added properties:

<pre style='color: green'>
	public static NSString QueryUpdateAddedItemsKey { get; }
	public static NSString QueryUpdateChangedItemsKey { get; }
	public static NSString QueryUpdateRemovedItemsKey { get; }
</pre>

### Type Changed: Foundation.NSMutableData

Added methods:

<pre style='color: green'>
	public virtual void ReplaceBytes (NSRange range, IntPtr buffer);
	public virtual void ReplaceBytes (NSRange range, IntPtr buffer, uint length);
	public virtual void ResetBytes (NSRange range);
</pre>

### Type Changed: Foundation.NSObject

Added method:

<pre style='color: green'>
	public virtual void PrepareForInterfaceBuilder ();
</pre>

### Type Changed: Foundation.NSOperation

Added property:

<pre style='color: green'>
	public virtual System.Action CompletionBlock { get; set; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void WaitUntilFinishedNS ();
```

Added method:

<pre style='color: green'>
	public virtual void WaitUntilFinished ();
</pre>

### Type Changed: Foundation.NSPurgeableData

Added interface:

<pre style='color: green'>
	INSDiscardableContent
</pre>

Added property:

<pre style='color: green'>
	public virtual bool IsContentDiscarded { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool BeginContentAccess ();
	public virtual void DiscardContentIfPossible ();
	public virtual void EndContentAccess ();
</pre>

### Type Changed: Foundation.NSSortDescriptor

Added constructor:

<pre style='color: green'>
	public NSSortDescriptor (string key, bool ascending, NSComparator comparator);
</pre>

### Type Changed: Foundation.NSTimeZone

Added method:

<pre style='color: green'>
	public static NSTimeZone FromGMT (nint seconds);
</pre>

### Type Changed: Foundation.NSUndoManager

Added method:

<pre style='color: green'>
	public virtual void SetActionName (string actionName);
</pre>

### Type Changed: Foundation.NSUrl

Added properties:

<pre style='color: green'>
	public virtual NSUrl FilePathUrl { get; }
	public virtual NSUrl FileReferenceUrl { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSUrl FromBookmarkData (NSData data, NSUrlBookmarkResolutionOptions options, NSUrl relativeToUrl, out bool isStale, out NSError error);
	public static NSData GetBookmarkData (NSUrl bookmarkFileUrl, out NSError error);
	public static bool WriteBookmarkData (NSData data, NSUrl bookmarkFileUrl, NSUrlBookmarkCreationOptions options, out NSError error);
</pre>

### Type Changed: Foundation.NSUrlError

Added values:

<pre style='color: green'>
	CallIsActive = -1019,
	ClientCertificateRequired = -1206,
	DataNotAllowed = -1020,
	InternationalRoamingOff = -1018,
	RequestBodyStreamExhausted = -1021,
</pre>

### Type Changed: Foundation.NSUrlSessionUploadTask


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Foundation.NSUrlSessionTask</span></span>

 <span style='color:green'>Foundation.NSUrlSessionDataTask</span>

### New Type Foundation.INSDiscardableContent

<pre style='color: green'>
public interface INSDiscardableContent : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual bool IsContentDiscarded { get; }
	// methods
	public virtual bool BeginContentAccess ();
	public virtual void DiscardContentIfPossible ();
	public virtual void EndContentAccess ();
}
</pre>

### New Type Foundation.NSCondition

<pre style='color: green'>
public class NSCondition : Foundation.NSObject, INSLocking, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt;, INSObjectProtocol {
	// constructors
	public NSCondition ();
	protected NSCondition (NSObjectFlag t);
	protected NSCondition (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Broadcast ();
	public virtual void Lock ();
	public virtual void Signal ();
	public virtual void Unlock ();
	public virtual void Wait ();
	public virtual bool WaitUntilDate (NSDate limit);
}
</pre>

### New Type Foundation.NSConditionLock

<pre style='color: green'>
public class NSConditionLock : Foundation.NSObject, INSLocking, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt;, INSObjectProtocol {
	// constructors
	public NSConditionLock ();
	protected NSConditionLock (NSObjectFlag t);
	protected NSConditionLock (IntPtr handle);
	public NSConditionLock (nint condition);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nint Condition { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool LockWhenCondition (nint condition, NSDate limit);
	public virtual void LockWhenCondition (nint condition);
	public virtual bool TryLock ();
	public virtual bool TryLockWhenCondition (nint condition);
	public virtual void Unlock ();
	public virtual void UnlockWithCondition (nint condition);
}
</pre>

### New Type Foundation.NSDataDetector

<pre style='color: green'>
public class NSDataDetector : Foundation.NSRegularExpression, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt;, INSObjectProtocol {
	// constructors
	public NSDataDetector ();
	public NSDataDetector (NSCoder coder);
	protected NSDataDetector (NSObjectFlag t);
	protected NSDataDetector (IntPtr handle);
	// properties
	public virtual NSTextCheckingTypes CheckingTypes { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	public static NSDataDetector Create (NSTextCheckingTypes checkingTypes, out NSError error);
	public virtual void EncodeTo (NSCoder encoder);
}
</pre>

### New Type Foundation.NSExtension

<pre style='color: green'>
public static class NSExtension {
	// properties
	public static NSString JavaScriptFinalizeArgumentKey { get; }
	public static NSString JavaScriptPreprocessingResultsKey { get; }
}
</pre>

### New Type Foundation.NSLock

<pre style='color: green'>
public class NSLock : Foundation.NSObject, INSLocking, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt;, INSObjectProtocol {
	// constructors
	public NSLock ();
	protected NSLock (NSObjectFlag t);
	protected NSLock (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool TryLock ();
	public virtual void Unlock ();
}
</pre>

### New Type Foundation.NSMatchEnumerator

<pre style='color: green'>
public sealed delegate NSMatchEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSMatchEnumerator (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSTextCheckingResult result, NSMatchingFlags flags, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (NSTextCheckingResult result, NSMatchingFlags flags, ref bool stop);
}
</pre>

### New Type Foundation.NSMatchingFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSMatchingFlags {
	Completed = 2,
	HitEnd = 4,
	InternalError = 16,
	Progress = 1,
	RequiredEnd = 8,
}
</pre>

### New Type Foundation.NSMatchingOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSMatchingOptions {
	Anchored = 4,
	ReportCompletion = 2,
	ReportProgress = 1,
	WithoutAnchoringBounds = 16,
	WithTransparentBounds = 8,
}
</pre>

### New Type Foundation.NSPredicateSupport_NSArray

<pre style='color: green'>
public static class NSPredicateSupport_NSArray {
	// methods
	public static NSArray FilterUsingPredicate (NSArray This, NSArray array);
}
</pre>

### New Type Foundation.NSPredicateSupport_NSMutableArray

<pre style='color: green'>
public static class NSPredicateSupport_NSMutableArray {
	// methods
	public static void FilterUsingPredicate (NSMutableArray This, NSPredicate predicate);
}
</pre>

### New Type Foundation.NSPredicateSupport_NSMutableSet

<pre style='color: green'>
public static class NSPredicateSupport_NSMutableSet {
	// methods
	public static void FilterUsingPredicate (NSMutableSet This, NSPredicate predicate);
}
</pre>

### New Type Foundation.NSPredicateSupport_NSSet

<pre style='color: green'>
public static class NSPredicateSupport_NSSet {
	// methods
	public static NSSet FilterUsingPredicate (NSSet This, NSPredicate predicate);
}
</pre>

### New Type Foundation.NSRecursiveLock

<pre style='color: green'>
public class NSRecursiveLock : Foundation.NSObject, INSLocking, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt;, INSObjectProtocol {
	// constructors
	public NSRecursiveLock ();
	protected NSRecursiveLock (NSObjectFlag t);
	protected NSRecursiveLock (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool TryLock ();
	public virtual void Unlock ();
}
</pre>

### New Type Foundation.NSRegularExpression

<pre style='color: green'>
public class NSRegularExpression : Foundation.NSObject, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt;, INSObjectProtocol {
	// constructors
	public NSRegularExpression ();
	public NSRegularExpression (NSCoder coder);
	protected NSRegularExpression (NSObjectFlag t);
	protected NSRegularExpression (IntPtr handle);
	public NSRegularExpression (NSString pattern, NSRegularExpressionOptions options, out NSError error);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint NumberOfCaptureGroups { get; }
	public virtual NSRegularExpressionOptions Options { get; }
	public virtual NSString Pattern { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (NSCoder encoder);
	public virtual void EnumerateMatches (NSString str, NSMatchingOptions options, NSRange range, NSMatchEnumerator enumerator);
	public virtual NSTextCheckingResult FindFirstMatch (string str, NSMatchingOptions options, NSRange range);
	public static NSString GetEscapedPattern (NSString str);
	public static NSString GetEscapedTemplate (NSString str);
	public virtual NSString[] GetMatches (NSString str, NSMatchingOptions options, NSRange range);
	public virtual uint GetNumberOfMatches (NSString str, NSMatchingOptions options, NSRange range);
	public virtual NSRange GetRangeOfFirstMatch (string str, NSMatchingOptions options, NSRange range);
	public virtual NSString GetReplacementString (NSTextCheckingResult result, NSString str, nint offset, NSString template);
	public virtual string ReplaceMatches (string sourceString, NSMatchingOptions options, NSRange range, string template);
	public virtual uint ReplaceMatches (NSMutableString mutableString, NSMatchingOptions options, NSRange range, NSString template);
}
</pre>

### New Type Foundation.NSRegularExpressionOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSRegularExpressionOptions {
	AllowCommentsAndWhitespace = 2,
	AnchorsMatchLines = 16,
	CaseInsensitive = 1,
	DotMatchesLineSeparators = 8,
	IgnoreMetacharacters = 4,
	UseUnicodeWordBoundaries = 64,
}
</pre>

### New Type Foundation.NSValueTransformer

<pre style='color: green'>
public abstract class NSValueTransformer : Foundation.NSObject, System.IEquatable&lt;NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	protected NSValueTransformer ();
	protected NSValueTransformer (NSObjectFlag t);
	protected NSValueTransformer (IntPtr handle);
	// properties
	public static bool AllowsReverseTransformation { get; }
	public static NSString BooleanTransformerName { get; }
	public override IntPtr ClassHandle { get; }
	public static NSString IsNilTransformerName { get; }
	public static NSString NSIsNotNilTransformerName { get; }
	public static NSString NSKeyedUnarchiveFromDataTransformerName { get; }
	public static ObjCRuntime.Class TransformedValueClass { get; }
	public static NSString UnarchiveFromDataTransformerName { get; }
	public static string[] ValueTransformerNames { get; }
	// methods
	public static NSValueTransformer GetValueTransformer (string name);
	public virtual NSObject ReverseTransformedValue (NSObject value);
	public static void SetValueTransformer (NSValueTransformer transformer, string name);
	public virtual NSObject TransformedValue (NSObject value);
}
</pre>

### New Type Foundation.ProtocolMemberAttribute

<pre style='color: green'>
public sealed class ProtocolMemberAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public ProtocolMemberAttribute ();
	// properties
	public ObjCRuntime.ArgumentSemantic ArgumentSemantic { get; set; }
	public string GetterSelector { get; set; }
	public bool IsProperty { get; set; }
	public bool IsRequired { get; set; }
	public bool IsStatic { get; set; }
	public bool IsVariadic { get; set; }
	public string Name { get; set; }
	public bool[] ParameterByRef { get; set; }
	public System.Type[] ParameterType { get; set; }
	public System.Type PropertyType { get; set; }
	public System.Type ReturnType { get; set; }
	public string Selector { get; set; }
	public string SetterSelector { get; set; }
}
</pre>

## Namespace GameKit

### Type Changed: GameKit.GKAchievementViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: GameKit.GKAchievementViewController.GKAchievementViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected GKAchievementViewController (IntPtr handle);
</pre>

### Type Changed: GameKit.GKFriendRequestComposeViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: GameKit.GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected GKFriendRequestComposeViewController (IntPtr handle);
</pre>

### Type Changed: GameKit.GKGameCenterViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: GameKit.GKLeaderboardViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: GameKit.GKLeaderboardViewController.GKLeaderboardViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected GKLeaderboardViewController (IntPtr handle);
</pre>

### Type Changed: GameKit.GKMatchmakerViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>UIKit.UIViewController</span></span>

 <span style='color:green'>UIKit.UINavigationController</span>

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: GameKit.GKTurnBasedMatchmakerViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: GameKit.GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected GKTurnBasedMatchmakerViewController (IntPtr handle);
</pre>

### Type Changed: GameKit.GKVoiceChat

Obsoleted methods:

```
[Obsolete (]
	public virtual void SetMute (bool isMuted, GKPlayer player);
```

Added method:

<pre style='color: green'>
	public virtual void SetMute (bool isMuted, string playerID);
</pre>

## Namespace GLKit

### Type Changed: GLKit.GLKBaseEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

### Type Changed: GLKit.GLKReflectionMapEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

### Type Changed: GLKit.GLKSkyboxEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

### Type Changed: GLKit.GLKView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: GLKit.GLKView.GLKViewAppearance

Added constructor:

<pre style='color: green'>
	protected GLKView (IntPtr handle);
</pre>

### Type Changed: GLKit.GLKViewController

Added interfaces:

<pre style='color: green'>
	IGLKViewDelegate
	UIKit.IUIAppearanceContainer
</pre>

Added method:

<pre style='color: green'>
	public virtual void DrawInRect (GLKView view, CoreGraphics.CGRect rect);
</pre>

## Namespace HealthKit

### Type Changed: HealthKit.HKQuantityTypeIdentifierKey

Added property:

<pre style='color: green'>
	public static Foundation.NSString ElectrodermalActivity { get; }
</pre>

## Namespace iAd

### Type Changed: iAd.ADBannerView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: iAd.ADBannerView.ADBannerViewAppearance

Added constructor:

<pre style='color: green'>
	protected ADBannerView (IntPtr handle);
</pre>

## Namespace MapKit

### Type Changed: MapKit.MKAnnotationView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MapKit.MKAnnotationView.MKAnnotationViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKAnnotationView (IntPtr handle);
</pre>

### Type Changed: MapKit.MKCircleView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MapKit.MKCircleView.MKCircleViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKCircleView (IntPtr handle);
</pre>

### Type Changed: MapKit.MKMapView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MapKit.MKMapView.MKMapViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKMapView (IntPtr handle);
</pre>

### Type Changed: MapKit.MKOverlayPathView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MapKit.MKOverlayPathView.MKOverlayPathViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKOverlayPathView (IntPtr handle);
</pre>

### Type Changed: MapKit.MKOverlayView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MapKit.MKOverlayView.MKOverlayViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKOverlayView (IntPtr handle);
</pre>

### Type Changed: MapKit.MKPinAnnotationView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MapKit.MKPinAnnotationView.MKPinAnnotationViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKPinAnnotationView (IntPtr handle);
</pre>

### Type Changed: MapKit.MKPolygonView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MapKit.MKPolygonView.MKPolygonViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKPolygonView (IntPtr handle);
</pre>

### Type Changed: MapKit.MKPolylineView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MapKit.MKPolylineView.MKPolylineViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKPolylineView (IntPtr handle);
</pre>

### Type Changed: MapKit.MKUserTrackingBarButtonItem

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearance
</pre>

### Type Changed: MapKit.MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance

Added constructor:

<pre style='color: green'>
	protected MKUserTrackingBarButtonItem (IntPtr handle);
</pre>

## Namespace MediaAccessibility

### New Type MediaAccessibility.MAAudibleMedia

<pre style='color: green'>
public static class MAAudibleMedia {
	// properties
	public static Foundation.NSString SettingsChangedNotification { get; }
	// methods
	public static string[] GetPreferredCharacteristics ();

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveSettingsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type MediaAccessibility.MAMediaCharacteristic

<pre style='color: green'>
public static class MAMediaCharacteristic {
	// properties
	public static Foundation.NSString DescribesMusicAndSoundForAccessibility { get; }
	public static Foundation.NSString DescribesVideoForAccessibility { get; }
	public static Foundation.NSString TranscribesSpokenDialogForAccessibility { get; }
}
</pre>

## Namespace MediaPlayer

### Type Changed: MediaPlayer.MPMediaItemCollection


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Foundation.NSObject</span></span>

 <span style='color:green'>MediaPlayer.MPMediaEntity</span>

### Type Changed: MediaPlayer.MPMediaPickerController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MediaPlayer.MPMoviePlayerViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MediaPlayer.MPVolumeView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MediaPlayer.MPVolumeView.MPVolumeViewAppearance

Added constructor:

<pre style='color: green'>
	protected MPVolumeView (IntPtr handle);
</pre>

## Namespace MessageUI

### Type Changed: MessageUI.MFMailComposeViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MessageUI.MFMailComposeViewController.MFMailComposeViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected MFMailComposeViewController (IntPtr handle);
</pre>

### Type Changed: MessageUI.MFMessageComposeViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MessageUI.MFMessageComposeViewController.MFMessageComposeViewControllerAppearance

Added constructor:

<pre style='color: green'>
	protected MFMessageComposeViewController (IntPtr handle);
</pre>

## Namespace Metal

### Type Changed: Metal.MTLRegion

Added methods:

<pre style='color: green'>
	public static MTLRegion Create1D (nint x, nint width);
	public static MTLRegion Create2D (nint x, nint y, nint width, nint height);
	public static MTLRegion Create3D (nint x, nint y, nint z, nint width, nint height, nint depth);
</pre>

### Type Changed: Metal.MTLVertexAttribute

Added property:

<pre style='color: green'>
	public virtual string Name { get; }
</pre>

## Namespace MultipeerConnectivity

### Type Changed: MultipeerConnectivity.MCBrowserViewController

Added interfaces:

<pre style='color: green'>
	IMCNearbyServiceBrowserDelegate
	UIKit.IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidNotStartBrowsingForPeers (MCNearbyServiceBrowser browser, Foundation.NSError error);
	public virtual void FoundPeer (MCNearbyServiceBrowser browser, MCPeerID peerID, Foundation.NSDictionary info);
	public virtual void LostPeer (MCNearbyServiceBrowser browser, MCPeerID peerID);
</pre>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.BlockFlags

Added value:

<pre style='color: green'>
	BLOCK_HAS_SIGNATURE = 1073741824,
</pre>

### Type Changed: ObjCRuntime.BlockLiteral

Added method:

<pre style='color: green'>
	public static bool IsManagedBlock (IntPtr block);
</pre>

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.10.3" "8.13.0";
```

Added field:

<pre style='color: green'>
	public static const string SdkVersion = "8.4";
</pre>

### Type Changed: ObjCRuntime.iOSAttribute

Added constructor:

<pre style='color: green'>
	public iOSAttribute (byte major, byte minor, byte subminor);
</pre>

### Type Changed: ObjCRuntime.MacAttribute

Added constructors:

<pre style='color: green'>
	public MacAttribute (byte major, byte minor);
	public MacAttribute (byte major, byte minor, byte subminor);
	public MacAttribute (byte major, byte minor, byte subminor, bool onlyOn64);
</pre>

### Type Changed: ObjCRuntime.Platform

Added value:

<pre style='color: green'>
	Mac_10_10_3 = 2825757768286208,
</pre>

## Namespace PassKit

### Type Changed: PassKit.PKAddPassesViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: PassKit.PKPaymentAuthorizationViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: PassKit.PKPaymentButton

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: PassKit.PKPaymentButton.PKPaymentButtonAppearance

Added constructor:

<pre style='color: green'>
	protected PKPaymentButton (IntPtr handle);
</pre>

## Namespace QuickLook

### Type Changed: QuickLook.QLPreviewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

## Namespace SceneKit

### Type Changed: SceneKit.SCNLight

Obsoleted methods:

```
[Obsolete (]
	public virtual Foundation.NSObject GetAttribute (Foundation.NSString lightAttribute);
	[Obsolete (]
	public virtual void SetAttribute (Foundation.NSObject value, Foundation.NSString attribuetKey);
```

### Type Changed: SceneKit.SCNParticleSystem

Added properties:

<pre style='color: green'>
	public SCNPropertyControllers PropertyControllers { get; set; }
	public virtual Foundation.NSDictionary WeakPropertyControllers { get; set; }
</pre>

Modified methods:

```
public virtual void HandleEvent (SCNParticleEvent evnt, Foundation.NSString[] properties particleProperties, SCNParticleEventHandler handler)
```

### Type Changed: SceneKit.SCNView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: SceneKit.SCNView.SCNViewAppearance

Added constructor:

<pre style='color: green'>
	protected SCNView (IntPtr handle);
</pre>

### New Type SceneKit.SCNParticleProperty

<pre style='color: green'>
public static class SCNParticleProperty {
	// properties
	public static Foundation.NSString Angle { get; }
	public static Foundation.NSString AngularVelocity { get; }
	public static Foundation.NSString Bounce { get; }
	public static Foundation.NSString Charge { get; }
	public static Foundation.NSString Color { get; }
	public static Foundation.NSString Frame { get; }
	public static Foundation.NSString FrameRate { get; }
	public static Foundation.NSString Friction { get; }
	public static Foundation.NSString Life { get; }
	public static Foundation.NSString Opacity { get; }
	public static Foundation.NSString Position { get; }
	public static Foundation.NSString RotationAxis { get; }
	public static Foundation.NSString Size { get; }
	public static Foundation.NSString Velocity { get; }
}
</pre>

### New Type SceneKit.SCNPhysicsCollisionCategory

<pre style='color: green'>
[Serializable]
public enum SCNPhysicsCollisionCategory {
	All = 18446744073709551615,
	Default = 1,
	None = 0,
	Static = 2,
}
</pre>

### New Type SceneKit.SCNPropertyControllers

<pre style='color: green'>
public class SCNPropertyControllers {
	// constructors
	public SCNPropertyControllers ();
	// properties
	public SCNParticlePropertyController Angle { get; set; }
	public SCNParticlePropertyController AngularVelocity { get; set; }
	public SCNParticlePropertyController Bounce { get; set; }
	public SCNParticlePropertyController Charge { get; set; }
	public SCNParticlePropertyController Color { get; set; }
	public SCNParticlePropertyController Frame { get; set; }
	public SCNParticlePropertyController FrameRate { get; set; }
	public SCNParticlePropertyController Friction { get; set; }
	public SCNParticlePropertyController Life { get; set; }
	public SCNParticlePropertyController Opacity { get; set; }
	public SCNParticlePropertyController Position { get; set; }
	public SCNParticlePropertyController RotationAxis { get; set; }
	public SCNParticlePropertyController Size { get; set; }
	public SCNParticlePropertyController Velocity { get; set; }
}
</pre>

## Namespace Social

### Type Changed: Social.SLComposeServiceViewController

Added interfaces:

<pre style='color: green'>
	UIKit.IUITextViewDelegate
	UIKit.IUIScrollViewDelegate
	UIKit.IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void Changed (UIKit.UITextView textView);
	public virtual void EditingEnded (UIKit.UITextView textView);
	public virtual void EditingStarted (UIKit.UITextView textView);
	public virtual void SelectionChanged (UIKit.UITextView textView);
	public virtual bool ShouldBeginEditing (UIKit.UITextView textView);
	public virtual bool ShouldChangeText (UIKit.UITextView textView, Foundation.NSRange range, string text);
	public virtual bool ShouldEndEditing (UIKit.UITextView textView);
	public virtual bool ShouldInteractWithTextAttachment (UIKit.UITextView textView, UIKit.NSTextAttachment textAttachment, Foundation.NSRange characterRange);
	public virtual bool ShouldInteractWithUrl (UIKit.UITextView textView, Foundation.NSUrl URL, Foundation.NSRange characterRange);
</pre>

### Type Changed: Social.SLComposeViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

## Namespace SpriteKit

### Type Changed: SpriteKit.SKFieldNode

Obsoleted methods:

```
[Obsolete (]
	public static SKFieldNode CraeteVortexField ();
```

Added method:

<pre style='color: green'>
	public static SKFieldNode CreateVortexField ();
</pre>

### Type Changed: SpriteKit.SKView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: SpriteKit.SKView.SKViewAppearance

Added constructor:

<pre style='color: green'>
	protected SKView (IntPtr handle);
</pre>

## Namespace StoreKit

### Type Changed: StoreKit.SKStoreProductViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

## Namespace Twitter

### Type Changed: Twitter.TWTweetComposeViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

## Namespace UIKit

### Type Changed: UIKit.NSIdentifier

Obsoleted methods:

```
[Obsolete (]
	public static string Identifier (NSLayoutConstraint This);
```

Added methods:

<pre style='color: green'>
	public static string GetIdentifier (NSLayoutConstraint This);
	public static void SetIdentifier (NSLayoutConstraint This, string id);
</pre>

### Type Changed: UIKit.UIActionSheet

Added constructors:

<pre style='color: green'>
	public UIActionSheet (string title, IUIActionSheetDelegate del);
	public UIActionSheet (string title, IUIActionSheetDelegate del, string cancelTitle, string destroy, string[] other);
</pre>

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIActionSheet.UIActionSheetAppearance

Added constructor:

<pre style='color: green'>
	protected UIActionSheet (IntPtr handle);
</pre>

### Type Changed: UIKit.UIActivityIndicatorView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIActivityIndicatorView.UIActivityIndicatorViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIActivityIndicatorView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIActivityItemProvider

Added interface:

<pre style='color: green'>
	IUIActivityItemSource
</pre>

Added methods:

<pre style='color: green'>
	public virtual string GetDataTypeIdentifierForActivity (UIActivityViewController activityViewController, Foundation.NSString activityType);
	public virtual Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, Foundation.NSString activityType);
	public virtual Foundation.NSObject GetPlaceholderData (UIActivityViewController activityViewController);
	public virtual string GetSubjectForActivity (UIActivityViewController activityViewController, Foundation.NSString activityType);
	public virtual UIImage GetThumbnailImageForActivity (UIActivityViewController activityViewController, Foundation.NSString activityType, CoreGraphics.CGSize suggestedSize);
</pre>

### Type Changed: UIKit.UIActivityViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIAdaptivePresentationControllerDelegate

Obsoleted methods:

```
[Obsolete (]
	public virtual UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style);
```

Added method:

<pre style='color: green'>
	public virtual UIModalPresentationStyle GetAdaptivePresentationStyle (UIPresentationController controller, UITraitCollection traitCollection);
</pre>

### Type Changed: UIKit.UIAdaptivePresentationControllerDelegate_Extensions

Obsoleted methods:

```
[Obsolete (]
	public static UIViewController GetAdaptivePresentationStyle (IUIAdaptivePresentationControllerDelegate This, UIPresentationController controller, UIModalPresentationStyle style);
```

Added method:

<pre style='color: green'>
	public static UIModalPresentationStyle GetAdaptivePresentationStyle (IUIAdaptivePresentationControllerDelegate This, UIPresentationController controller, UITraitCollection traitCollection);
</pre>

### Type Changed: UIKit.UIAlertController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIAlertView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIAlertView.UIAlertViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIAlertView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIBarButtonItem

Added interface:

<pre style='color: green'>
	IUIAppearance
</pre>

### Type Changed: UIKit.UIBarButtonItem.UIBarButtonItemAppearance

Added constructor:

<pre style='color: green'>
	protected UIBarButtonItem (IntPtr handle);
</pre>

### Type Changed: UIKit.UIBarItem

Added interface:

<pre style='color: green'>
	IUIAppearance
</pre>

### Type Changed: UIKit.UIBarItem.UIBarItemAppearance

Added constructor:

<pre style='color: green'>
	protected UIBarItem (IntPtr handle);
</pre>

### Type Changed: UIKit.UIButton

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIButton.UIButtonAppearance

Added constructor:

<pre style='color: green'>
	protected UIButton (IntPtr handle);
</pre>

### Type Changed: UIKit.UICollectionReusableView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UICollectionReusableView.UICollectionReusableViewAppearance

Added constructor:

<pre style='color: green'>
	protected UICollectionReusableView (IntPtr handle);
</pre>

### Type Changed: UIKit.UICollectionView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UICollectionView.UICollectionViewAppearance

Added constructor:

<pre style='color: green'>
	protected UICollectionView (IntPtr handle);
</pre>

### Type Changed: UIKit.UICollectionViewCell

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UICollectionViewCell.UICollectionViewCellAppearance

Added constructor:

<pre style='color: green'>
	protected UICollectionViewCell (IntPtr handle);
</pre>

### Type Changed: UIKit.UICollectionViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIControl

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIControl.UIControlAppearance

Added constructor:

<pre style='color: green'>
	protected UIControl (IntPtr handle);
</pre>

### Type Changed: UIKit.UIDatePicker

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIDatePicker.UIDatePickerAppearance

Added constructor:

<pre style='color: green'>
	protected UIDatePicker (IntPtr handle);
</pre>

### Type Changed: UIKit.UIDocumentMenuViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIDocumentPickerExtensionViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIDocumentPickerViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIImagePickerController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIImageView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIImageView.UIImageViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIImageView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIInputView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIInputView.UIInputViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIInputView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIInputViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UILabel

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UILabel.UILabelAppearance

Added constructor:

<pre style='color: green'>
	protected UILabel (IntPtr handle);
</pre>

### Type Changed: UIKit.UINavigationBar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UINavigationBar.UINavigationBarAppearance

Added constructor:

<pre style='color: green'>
	protected UINavigationBar (IntPtr handle);
</pre>

### Type Changed: UIKit.UINavigationController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIPageControl

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIPageControl.UIPageControlAppearance

Added constructor:

<pre style='color: green'>
	protected UIPageControl (IntPtr handle);
</pre>

### Type Changed: UIKit.UIPageViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIPickerView

Added interfaces:

<pre style='color: green'>
	IUITableViewDataSource
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual UITableViewCell GetCell (UITableView tableView, Foundation.NSIndexPath indexPath);
	public virtual nint RowsInSection (UITableView tableview, nint section);
</pre>

### Type Changed: UIKit.UIPickerView.UIPickerViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIPickerView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIPopoverBackgroundView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIPopoverBackgroundView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIPopoverController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIPopoverPresentationControllerDelegate

Added method:

<pre style='color: green'>
	[Obsolete]
	public virtual UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style);
</pre>

### Type Changed: UIKit.UIProgressView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIProgressView.UIProgressViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIProgressView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIReferenceLibraryViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIRefreshControl

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIRefreshControl.UIRefreshControlAppearance

Added constructor:

<pre style='color: green'>
	protected UIRefreshControl (IntPtr handle);
</pre>

### Type Changed: UIKit.UIScrollView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIScrollView.UIScrollViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIScrollView (IntPtr handle);
</pre>

### Type Changed: UIKit.UISearchBar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UISearchBar.UISearchBarAppearance

Added constructor:

<pre style='color: green'>
	protected UISearchBar (IntPtr handle);
</pre>

### Type Changed: UIKit.UISearchController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UISegmentedControl

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UISegmentedControl.UISegmentedControlAppearance

Added constructor:

<pre style='color: green'>
	protected UISegmentedControl (IntPtr handle);
</pre>

### Type Changed: UIKit.UISlider

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UISlider.UISliderAppearance

Added constructor:

<pre style='color: green'>
	protected UISlider (IntPtr handle);
</pre>

### Type Changed: UIKit.UISplitViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIStepper

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIStepper.UIStepperAppearance

Added constructor:

<pre style='color: green'>
	protected UIStepper (IntPtr handle);
</pre>

### Type Changed: UIKit.UISwitch

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UISwitch.UISwitchAppearance

Added constructor:

<pre style='color: green'>
	protected UISwitch (IntPtr handle);
</pre>

### Type Changed: UIKit.UITabBar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UITabBar.UITabBarAppearance

Added constructor:

<pre style='color: green'>
	protected UITabBar (IntPtr handle);
</pre>

### Type Changed: UIKit.UITabBarController

Added interfaces:

<pre style='color: green'>
	IUITabBarDelegate
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DidBeginCustomizingItems (UITabBar tabbar, UITabBarItem[] items);
	public virtual void DidEndCustomizingItems (UITabBar tabbar, UITabBarItem[] items, bool changed);
	public virtual void ItemSelected (UITabBar tabbar, UITabBarItem item);
	public virtual void WillBeginCustomizingItems (UITabBar tabbar, UITabBarItem[] items);
	public virtual void WillEndCustomizingItems (UITabBar tabbar, UITabBarItem[] items, bool changed);
</pre>

### Type Changed: UIKit.UITabBarItem

Added interface:

<pre style='color: green'>
	IUIAppearance
</pre>

### Type Changed: UIKit.UITabBarItem.UITabBarItemAppearance

Added constructor:

<pre style='color: green'>
	protected UITabBarItem (IntPtr handle);
</pre>

### Type Changed: UIKit.UITableView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UITableView.UITableViewAppearance

Added constructor:

<pre style='color: green'>
	protected UITableView (IntPtr handle);
</pre>

### Type Changed: UIKit.UITableViewCell

Added interfaces:

<pre style='color: green'>
	IUIGestureRecognizerDelegate
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool ShouldBegin (UIGestureRecognizer recognizer);
	public virtual bool ShouldBeRequiredToFailBy (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
	public virtual bool ShouldReceiveTouch (UIGestureRecognizer recognizer, UITouch touch);
	public virtual bool ShouldRecognizeSimultaneously (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
	public virtual bool ShouldRequireFailureOf (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
</pre>

### Type Changed: UIKit.UITableViewCell.UITableViewCellAppearance

Added constructor:

<pre style='color: green'>
	protected UITableViewCell (IntPtr handle);
</pre>

### Type Changed: UIKit.UITableViewController

Added interfaces:

<pre style='color: green'>
	IUITableViewDataSource
	IUITableViewDelegate
	IUIScrollViewDelegate
	IUIAppearanceContainer
</pre>

Modified methods:

```
public virtual nint RowsInSection (UITableView tableview tableView, nint section)
```

### Type Changed: UIKit.UITableViewHeaderFooterView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance

Added constructor:

<pre style='color: green'>
	protected UITableViewHeaderFooterView (IntPtr handle);
</pre>

### Type Changed: UIKit.UITextField

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UITextField.UITextFieldAppearance

Added constructor:

<pre style='color: green'>
	protected UITextField (IntPtr handle);
</pre>

### Type Changed: UIKit.UITextView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UITextView.UITextViewAppearance

Added constructor:

<pre style='color: green'>
	protected UITextView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIToolbar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIToolbar.UIToolbarAppearance

Added constructor:

<pre style='color: green'>
	protected UIToolbar (IntPtr handle);
</pre>

### Type Changed: UIKit.UIVideoEditorController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIView.UIViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIViewController

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIVisualEffectView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIVisualEffectView.UIVisualEffectViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIVisualEffectView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIWebView

Added interfaces:

<pre style='color: green'>
	IUIScrollViewDelegate
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DecelerationEnded (UIScrollView scrollView);
	public virtual void DecelerationStarted (UIScrollView scrollView);
	public virtual void DidZoom (UIScrollView scrollView);
	public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
	public virtual void DraggingStarted (UIScrollView scrollView);
	public virtual void ScrollAnimationEnded (UIScrollView scrollView);
	public virtual void Scrolled (UIScrollView scrollView);
	public virtual void ScrolledToTop (UIScrollView scrollView);
	public virtual bool ShouldScrollToTop (UIScrollView scrollView);
	public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);
	public virtual void WillEndDragging (UIScrollView scrollView, CoreGraphics.CGPoint velocity, ref CoreGraphics.CGPoint targetContentOffset);
	public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, nfloat atScale);
	public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);
</pre>

### Type Changed: UIKit.UIWebView.UIWebViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIWebView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIWindow

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIWindow.UIWindowAppearance

Added constructor:

<pre style='color: green'>
	protected UIWindow (IntPtr handle);
</pre>

### New Type UIKit.UIInterfaceOrientationExtensions

<pre style='color: green'>
public static class UIInterfaceOrientationExtensions {
	// methods
	public static bool IsLandscape (UIInterfaceOrientation orientation);
	public static bool IsPortrait (UIInterfaceOrientation orientation);
}
</pre>

## Namespace WatchKit

### Type Changed: WatchKit.WKInterfaceController

Added method:

<pre style='color: green'>
	public void PushController (string name, string context);
</pre>

## Namespace WebKit

### Type Changed: WebKit.WKWebView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: WebKit.WKWebView.WKWebViewAppearance

Added constructor:

<pre style='color: green'>
	protected WKWebView (IntPtr handle);
</pre>

   


 <hr>
