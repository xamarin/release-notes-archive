---
id: EB3B6304-F22E-4B87-9526-1D008FF928B5
title: "From 9.1.0 to 9.2.1"
---

# API diff

 [mscorlib.dll](#mscorlib)

   


 [System.dll](#System)

   


 [System.Core.dll](#System.Core)

   


 [System.Data.dll](#System.Data)

   


 [System.Runtime.Serialization.dll](#System.Runtime.Serialization)

   


 [System.Xml.dll](#System.Xml)

   


 [Mono.Data.Tds.dll](#Mono.Data.Tds)

   


 [(Classic) monotouch.dll](#compat/monotouch)

   


 [(Classic) MonoTouch.Dialog-1.dll](#compat/MonoTouch.Dialog-1)

   


 [(Classic) MonoTouch.NUnitLite.dll](#compat/MonoTouch.NUnitLite)

   


 [(Classic) OpenTK.dll](#compat/OpenTK)

   


 [(Classic) OpenTK-1.0.dll](#compat/OpenTK-1.0)

   


 [(Classic) System.Net.Http.dll](#compat/System.Net.Http)

   


 [(Unified) MonoTouch.Dialog-1.dll](#reference/MonoTouch.Dialog-1)

   


 [(Unified) MonoTouch.NUnitLite.dll](#reference/MonoTouch.NUnitLite)

   


 [(Unified) OpenTK-1.0.dll](#reference/OpenTK-1.0)

   


 [(Unified) System.Net.Http.dll](#reference/System.Net.Http)

   


 [(Unified) Xamarin.iOS.dll](#reference/Xamarin.iOS)

   


   


 <hr>

<h1 id='mscorlib'>mscorlib.dll</h1>

## Namespace System

### Type Changed: System._AppDomain

Added methods:

<pre style='color: red'>
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
	Runtime.InteropServices._MemberInfo
	Runtime.InteropServices._Type
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
	System.Runtime.InteropServices._MemberInfo
	System.Runtime.InteropServices._MethodBase
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
	System.Runtime.InteropServices._MemberInfo
	System.Runtime.InteropServices._MethodBase
</pre>

### Type Changed: System.Reflection.MethodInfo

Added interfaces:

<pre style='color: green'>
	System.Runtime.InteropServices._MemberInfo
	System.Runtime.InteropServices._MethodBase
</pre>

### Type Changed: System.Reflection.PropertyInfo

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._MemberInfo
</pre>

### Type Changed: System.Reflection.TypeDelegator

Added interfaces:

<pre style='color: green'>
	System.Runtime.InteropServices._MemberInfo
	System.Runtime.InteropServices._Type
</pre>

### Type Changed: System.Reflection.TypeInfo

Added interfaces:

<pre style='color: green'>
	System.Runtime.InteropServices._MemberInfo
	System.Runtime.InteropServices._Type
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
	public virtual void TraceData (TraceEventCache eventCache, string source, TraceEventType eventType, int id, object data);
	public virtual void TraceData (TraceEventCache eventCache, string source, TraceEventType eventType, int id, object[] data);
	public virtual void TraceEvent (TraceEventCache eventCache, string source, TraceEventType eventType, int id);
	public virtual void TraceEvent (TraceEventCache eventCache, string source, TraceEventType eventType, int id, string message);
	public virtual void TraceEvent (TraceEventCache eventCache, string source, TraceEventType eventType, int id, string format, object[] args);
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
	public void TraceData (TraceEventType eventType, int id, object data);
	public void TraceData (TraceEventType eventType, int id, object[] data);
	public void TraceEvent (TraceEventType eventType, int id);
	public void TraceEvent (TraceEventType eventType, int id, string message);
	public void TraceEvent (TraceEventType eventType, int id, string format, object[] args);
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
[Obsolete ("Use OSSupportsIPv4 instead")]
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
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, System.Collections.Generic.IEnumerable&lt;Expression&gt; arguments);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression[] arguments);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1, Expression arg2);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1, Expression arg2, Expression arg3);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, System.Collections.Generic.IEnumerable&lt;Expression&gt; arguments);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression[] arguments);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1, Expression arg2);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1, Expression arg2, Expression arg3);
</pre>

### Type Changed: System.Linq.Expressions.DynamicExpressionVisitor

Added method:

<pre style='color: green'>
	protected override Expression VisitDynamic (DynamicExpression node);
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
	public DataView CreateChildView (DataRelation relation, bool followParent);
	public DataView CreateChildView (string relationName, bool followParent);
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
	public void WriteXmlSchema (System.IO.TextWriter writer, System.Converter&lt;System.Type,System.String&gt; multipleTargetConverter);
	public void WriteXmlSchema (string fileName, System.Converter&lt;System.Type,System.String&gt; multipleTargetConverter);
	public void WriteXmlSchema (System.Xml.XmlWriter writer, System.Converter&lt;System.Type,System.String&gt; multipleTargetConverter);
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
[Obsolete ("ConnectionReset has been deprecated.  SqlConnection will ignore the 'connection reset' keyword and always reset the connection")]
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

### New Type System.Data.SqlClient.SortOrder

<pre style='color: green'>
[Serializable]
public enum SortOrder {
	Ascending = 0,
	Descending = 1,
	Unspecified = -1,
}
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

<pre style='color: red'>
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
	public override object ReadObject (System.Xml.XmlReader reader);
	public override object ReadObject (System.Xml.XmlReader reader, bool verifyObjectName);
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
	public static XmlDictionaryReader CreateMtomReader (System.IO.Stream stream, System.Text.Encoding encoding, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (System.IO.Stream stream, System.Text.Encoding[] encodings, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (System.IO.Stream stream, System.Text.Encoding[] encodings, string contentType, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (byte[] buffer, int offset, int count, System.Text.Encoding encoding, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (byte[] buffer, int offset, int count, System.Text.Encoding[] encodings, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (byte[] buffer, int offset, int count, System.Text.Encoding[] encodings, string contentType, XmlDictionaryReaderQuotas quotas);
	public static XmlDictionaryReader CreateMtomReader (System.IO.Stream stream, System.Text.Encoding[] encodings, string contentType, XmlDictionaryReaderQuotas quotas, int maxBufferSize, OnXmlDictionaryReaderClose onClose);
	public static XmlDictionaryReader CreateMtomReader (byte[] buffer, int offset, int count, System.Text.Encoding[] encodings, string contentType, XmlDictionaryReaderQuotas quotas, int maxBufferSize, OnXmlDictionaryReaderClose onClose);
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
	public static XmlDictionaryWriter CreateMtomWriter (System.IO.Stream stream, System.Text.Encoding encoding, int maxSizeInBytes, string startInfo);
	public static XmlDictionaryWriter CreateMtomWriter (System.IO.Stream stream, System.Text.Encoding encoding, int maxSizeInBytes, string startInfo, string boundary, string startUri, bool writeMessageHeaders, bool ownsStream);
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
[Obsolete ("Use DtdProcessing property instead.")]
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
	public XmlSecureResolver (XmlResolver resolver, System.Security.PermissionSet permissionSet);
	public XmlSecureResolver (XmlResolver resolver, System.Security.Policy.Evidence evidence);
	public XmlSecureResolver (XmlResolver resolver, string securityUrl);
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
	public void Add (System.Uri uri, byte[] value);
	public void Add (System.Uri uri, System.IO.Stream value);
	public void Add (System.Uri uri, string value);
	public void Add (System.Uri uri, byte[] value, int offset, int count);
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

<h1 id='Mono.Data.Tds'>Mono.Data.Tds.dll</h1>

## Namespace Mono.Data.Tds.Protocol

### Type Changed: Mono.Data.Tds.Protocol.TdsColumnType

Added values:

<pre style='color: green'>
	DateTime2 = 42,
	DateTimeOffset = 43,
</pre>

   


 <hr>

<h1 id='compat/monotouch'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "9.1.0" "9.2.1";
```

### Type Changed: MonoTouch.MonoNativeFunctionWrapperAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.MonoPInvokeCallbackAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.RuntimeException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.AudioQueueException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: MonoTouch.AudioToolbox.AudioSessionException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AUAudioUnit

Added properties:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString AudioComponentInstanceInvalidationNotification { get; }
	public static MonoTouch.Foundation.NSString AudioComponentRegistrationsChangedNotification { get; }
</pre>

### Type Changed: MonoTouch.AudioUnit.AudioUnitException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: MonoTouch.CoreFoundation.CFSocketException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace MonoTouch.CoreMidi

### Type Changed: MonoTouch.CoreMidi.MidiException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.ActionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.AdviceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.ConnectAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.ExportAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.FieldAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.LinkerSafeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.ModelAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.ModelNotImplementedException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: MonoTouch.Foundation.MonoTouchException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: MonoTouch.Foundation.NSErrorException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: MonoTouch.Foundation.OutletAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.PreserveAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.ProtocolAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.ProtocolMemberAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.RegisterAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Foundation.You_Should_Not_Call_base_In_This_Method

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace MonoTouch.HomeKit

### Type Changed: MonoTouch.HomeKit.HMService

Obsoleted methods:

```
[Obsolete ()]
	public System.Threading.Tasks.Task UpdateNameAsync (HMServiceType serviceType);
```

Added method:

<pre style='color: green'>
	public System.Threading.Tasks.Task UpdateAssociatedServiceTypeAsync (HMServiceType serviceType);
</pre>

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.AdoptsAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.AlphaAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.AvailabilityAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.AvailabilityBaseAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.BlockProxyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.CategoryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.DeprecatedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.DesignatedInitializerAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.IntroducedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.iOSAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.LinkWithAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.LionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.MacAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.MavericksAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Removed methods:

<pre style='color: red'>
	public static void MDLAxisAlignedBoundingBox_objc_msgSend_stret_Double (out MonoTouch.ModelIO.MDLAxisAlignedBoundingBox retval, IntPtr receiver, IntPtr selector, double arg1);
	public static void MDLAxisAlignedBoundingBox_objc_msgSendSuper_stret_Double (out MonoTouch.ModelIO.MDLAxisAlignedBoundingBox retval, IntPtr receiver, IntPtr selector, double arg1);
</pre>

Added methods:

<pre style='color: green'>
	public static void xamarin_simd__MDLAxisAlignedBoundingBox_objc_msgSend_stret_Double (out MonoTouch.ModelIO.MDLAxisAlignedBoundingBox retval, IntPtr receiver, IntPtr selector, double arg1);
	public static void xamarin_simd__MDLAxisAlignedBoundingBox_objc_msgSendSuper_stret_Double (out MonoTouch.ModelIO.MDLAxisAlignedBoundingBox retval, IntPtr receiver, IntPtr selector, double arg1);
</pre>

### Type Changed: MonoTouch.ObjCRuntime.MountainLionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.NativeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.ObsoletedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.ReleaseAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.SinceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.ThreadSafeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.TransientAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.ObjCRuntime.UnavailableAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecurityException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace MonoTouch.SystemConfiguration

### Type Changed: MonoTouch.SystemConfiguration.SystemConfigurationException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIKitThreadAccessException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: MonoTouch.UIKit.UIMutableApplicationShortcutItem

Modified properties:

```
public override MonoTouch.Foundation.NSDictionary UserInfo { get; set; }
```

   


 <hr>

<h1 id='compat/MonoTouch.Dialog-1'>MonoTouch.Dialog-1.dll</h1>

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.AlignmentAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.CaptionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.CheckboxAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.DateAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.EntryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.HtmlAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.MultilineAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.OnTapAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.PasswordAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.RadioSelectionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.RangeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.SectionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.SkipAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.TimeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='compat/MonoTouch.NUnitLite'>MonoTouch.NUnitLite.dll</h1>

## Namespace Mono.Options

### Type Changed: Mono.Options.OptionException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace NUnit

### Type Changed: NUnit.ObjectList

Removed interfaces:

<pre style='color: red'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

## Namespace NUnit.Framework

### Type Changed: NUnit.Framework.AssertionException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.CategoryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.CombinatorialAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.CultureAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DataAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DatapointAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DatapointsAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DatapointSourceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DescriptionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.ExpectedExceptionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.ExplicitAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.IgnoreAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.IgnoreException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.IncludeExcludeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.InconclusiveException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.MaxTimeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.NUnitAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PairwiseAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PlatformAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PostTestAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PreTestAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PropertyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.RandomAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.RangeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SequentialAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SetCultureAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SetUICultureAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SetUpAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SuccessException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.TearDownAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestCaseAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestCaseSourceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestFixtureAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestFixtureSetUpAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestFixtureTearDownAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TheoryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TimeoutAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.ValuesAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.ValueSourceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace NUnit.Framework.Api

### Type Changed: NUnit.Framework.Api.AttributeDictionary

Removed interfaces:

<pre style='color: red'>
	System.Collections.Generic.IReadOnlyDictionary&lt;TKey,TValue&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt;
</pre>

### Type Changed: NUnit.Framework.Api.NodeList

Removed interfaces:

<pre style='color: red'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

## Namespace NUnit.Framework.Internal

### Type Changed: NUnit.Framework.Internal.InvalidTestFixtureException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.Internal.NUnitException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace NUnit.Framework.Internal.Commands

### Type Changed: NUnit.Framework.Internal.Commands.CommandDecoratorList

Removed interfaces:

<pre style='color: red'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

   


 <hr>

<h1 id='compat/OpenTK'>OpenTK.dll</h1>

## Namespace OpenTK

### Type Changed: OpenTK.AutoGeneratedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace OpenTK.Audio

### Type Changed: OpenTK.Audio.AudioContextException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioDeviceException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioValueException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.GraphicsContextException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Graphics.GraphicsContextMissingException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Graphics.GraphicsModeException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

   


 <hr>

<h1 id='compat/OpenTK-1.0'>OpenTK-1.0.dll</h1>

## Namespace OpenTK

### Type Changed: OpenTK.AutoGeneratedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace OpenTK.Audio

### Type Changed: OpenTK.Audio.AudioContextException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioDeviceException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioValueException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.GraphicsContextException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Graphics.GraphicsContextMissingException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Graphics.GraphicsModeException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

   


 <hr>

<h1 id='compat/System.Net.Http'>System.Net.Http.dll</h1>

## Namespace System.Net.Http

### Type Changed: System.Net.Http.HttpRequestException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

   


 <hr>

<h1 id='reference/MonoTouch.Dialog-1'>MonoTouch.Dialog-1.dll</h1>

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.AlignmentAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.CaptionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.CheckboxAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.DateAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.EntryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.HtmlAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.MultilineAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.OnTapAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.PasswordAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.RadioSelectionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.RangeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.SectionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.SkipAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: MonoTouch.Dialog.TimeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

   


 <hr>

<h1 id='reference/MonoTouch.NUnitLite'>MonoTouch.NUnitLite.dll</h1>

## Namespace Mono.Options

### Type Changed: Mono.Options.OptionException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace NUnit

### Type Changed: NUnit.ObjectList

Removed interfaces:

<pre style='color: red'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

## Namespace NUnit.Framework

### Type Changed: NUnit.Framework.AssertionException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.CategoryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.CombinatorialAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.CultureAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DataAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DatapointAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DatapointsAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DatapointSourceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.DescriptionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.ExpectedExceptionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.ExplicitAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.IgnoreAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.IgnoreException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.IncludeExcludeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.InconclusiveException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.MaxTimeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.NUnitAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PairwiseAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PlatformAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PostTestAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PreTestAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.PropertyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.RandomAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.RangeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SequentialAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SetCultureAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SetUICultureAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SetUpAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.SuccessException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.TearDownAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestCaseAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestCaseSourceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestFixtureAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestFixtureSetUpAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TestFixtureTearDownAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TheoryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.TimeoutAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.ValuesAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: NUnit.Framework.ValueSourceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace NUnit.Framework.Api

### Type Changed: NUnit.Framework.Api.AttributeDictionary

Removed interfaces:

<pre style='color: red'>
	System.Collections.Generic.IReadOnlyDictionary&lt;TKey,TValue&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt;
</pre>

### Type Changed: NUnit.Framework.Api.NodeList

Removed interfaces:

<pre style='color: red'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

## Namespace NUnit.Framework.Internal

### Type Changed: NUnit.Framework.Internal.InvalidTestFixtureException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: NUnit.Framework.Internal.NUnitException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace NUnit.Framework.Internal.Commands

### Type Changed: NUnit.Framework.Internal.Commands.CommandDecoratorList

Removed interfaces:

<pre style='color: red'>
	System.Collections.Generic.IReadOnlyList&lt;T&gt;
	System.Collections.Generic.IReadOnlyCollection&lt;T&gt;
</pre>

   


 <hr>

<h1 id='reference/OpenTK-1.0'>OpenTK-1.0.dll</h1>

## Namespace OpenTK

### Type Changed: OpenTK.AutoGeneratedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace OpenTK.Audio

### Type Changed: OpenTK.Audio.AudioContextException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioDeviceException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Audio.AudioValueException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.GraphicsContextException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Graphics.GraphicsContextMissingException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: OpenTK.Graphics.GraphicsModeException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

   


 <hr>

<h1 id='reference/System.Net.Http'>System.Net.Http.dll</h1>

## Namespace System.Net.Http

### Type Changed: System.Net.Http.HttpRequestException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace AudioToolbox

### Type Changed: AudioToolbox.AudioQueueException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: AudioToolbox.AudioSessionException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace AudioUnit

### Type Changed: AudioUnit.AUAudioUnit

Added properties:

<pre style='color: green'>
	public static Foundation.NSString AudioComponentInstanceInvalidationNotification { get; }
	public static Foundation.NSString AudioComponentRegistrationsChangedNotification { get; }
</pre>

### Type Changed: AudioUnit.AudioUnitException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace AVFoundation

### Type Changed: AVFoundation.AVAudioUnit

Added property:

<pre style='color: green'>
	public virtual AudioUnit.AUAudioUnit AUAudioUnit { get; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

## Namespace CoreFoundation

### Type Changed: CoreFoundation.CFException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: CoreFoundation.CFSocketException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace CoreMidi

### Type Changed: CoreMidi.MidiException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace CoreVideo

### Type Changed: CoreVideo.CVImageBuffer

Added properties:

<pre style='color: green'>
	public static Foundation.NSString ColorPrimaries_DCI_P3 { get; }
	public static Foundation.NSString ColorPrimaries_ITU_R_2020 { get; }
	public static Foundation.NSString ColorPrimaries_P3_D65 { get; }
</pre>

### Type Changed: CoreVideo.CVPixelBufferPool

Added properties:

<pre style='color: green'>
	public static Foundation.NSString ColorPrimaries_DCI_P3 { get; }
	public static Foundation.NSString ColorPrimaries_ITU_R_2020 { get; }
	public static Foundation.NSString ColorPrimaries_P3_D65 { get; }
</pre>

## Namespace Foundation

### Type Changed: Foundation.ActionAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.AdviceAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.ConnectAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.ExportAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.FieldAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.LinkerSafeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.ModelAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.ModelNotImplementedException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: Foundation.MonoTouchException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: Foundation.NSErrorException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: Foundation.OutletAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.PreserveAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.ProtocolAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.ProtocolMemberAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.RegisterAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: Foundation.You_Should_Not_Call_base_In_This_Method

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace HomeKit

### Type Changed: HomeKit.HMService

Obsoleted methods:

```
[Obsolete ()]
	public System.Threading.Tasks.Task UpdateNameAsync (HMServiceType serviceType);
```

Added method:

<pre style='color: green'>
	public System.Threading.Tasks.Task UpdateAssociatedServiceTypeAsync (HMServiceType serviceType);
</pre>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.AdoptsAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.AvailabilityAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.AvailabilityBaseAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.BlockProxyAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.CategoryAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "9.1.0" "9.2.1";
```

### Type Changed: ObjCRuntime.DeprecatedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.DesignatedInitializerAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.IntroducedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.iOSAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.LinkWithAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.MacAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.MonoNativeFunctionWrapperAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.MonoPInvokeCallbackAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.NativeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.ObsoletedAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.ReleaseAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.RuntimeException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: ObjCRuntime.ThreadSafeAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.TransientAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

### Type Changed: ObjCRuntime.UnavailableAttribute

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Attribute
</pre>

## Namespace Security

### Type Changed: Security.SecurityException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace SystemConfiguration

### Type Changed: SystemConfiguration.SystemConfigurationException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

## Namespace UIKit

### Type Changed: UIKit.UIKitThreadAccessException

Added interface:

<pre style='color: green'>
	System.Runtime.InteropServices._Exception
</pre>

### Type Changed: UIKit.UIMutableApplicationShortcutItem

Added property:

<pre style='color: green'>
	public override Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; UserInfo { get; set; }
</pre>

   


 <hr>
