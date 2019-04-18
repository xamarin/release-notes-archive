---
id: A7301E79-E9E0-4F53-ADF5-01698E01DF0B
title: "From 8.10.0 to 8.99.0"
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

### New Type System.Runtime.InteropServices.DefaultDllImportSearchPathsAttribute

<pre style='color: green'>
public sealed class DefaultDllImportSearchPathsAttribute : System.Attribute {
	// constructors
	public DefaultDllImportSearchPathsAttribute (DllImportSearchPath paths);
	// properties
	public DllImportSearchPath Paths { get; }
}
</pre>

### New Type System.Runtime.InteropServices.DllImportSearchPath

<pre style='color: green'>
[Serializable]
[Flags]
public enum DllImportSearchPath {
	ApplicationDirectory = 512,
	AssemblyDirectory = 2,
	LegacyBehavior = 0,
	SafeDirectories = 4096,
	System32 = 2048,
	UseDllDirectoryForDependencies = 256,
	UserDirectories = 1024,
}
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
public const string Version = "8.10.0" "8.99.0";
```

Added fields:

<pre style='color: green'>
	public static const string ContactsLibrary = "/System/Library/Frameworks/Contacts.framework/Contacts";
	public static const string ContactsUILibrary = "/System/Library/Frameworks/ContactsUI.framework/ContactsUI";
	public static const string CoreSpotlightLibrary = "/System/Library/Frameworks/CoreSpotlight.framework/CoreSpotlight";
	public static const string libcLibrary = "/usr/lib/libc.dylib";
	public static const string libSystemLibrary = "/usr/lib/libSystem.dylib";
	public static const string ReplayKitLibrary = "/System/Library/Frameworks/ReplayKit.framework/ReplayKit";
	public static const string SdkVersion = "9.0";
	public static const string WatchConnectivityLibrary = "/System/Library/Frameworks/WatchConnectivity.framework/WatchConnectivity";
	public static const string WebKitLibrary = "/System/Library/Frameworks/WebKit.framework/WebKit";
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

### Type Changed: MonoTouch.AudioToolbox.AudioFormatType

Added value:

<pre style='color: green'>
	EnhancedAES3 = 1700998451,
</pre>

### Type Changed: MonoTouch.AudioToolbox.AudioQueue

Added method:

<pre style='color: green'>
	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, AudioStreamPacketDescription[] desc);
</pre>

### Type Changed: MonoTouch.AudioToolbox.AudioTimeStamp

### Type Changed: MonoTouch.AudioToolbox.AudioTimeStamp.AtsFlags

Added field:

<pre style='color: green'>
	public static const AudioTimeStamp.AtsFlags NothingValid;
</pre>

### Type Changed: MonoTouch.AudioToolbox.SmpteTime

Added properties:

<pre style='color: green'>
	public SmpteTimeFlags FlagsStrong { get; set; }
	public SmpteTimeType TypeStrong { get; set; }
</pre>

### New Type MonoTouch.AudioToolbox.MPEG4ObjectID

<pre style='color: green'>
[Serializable]
public enum MPEG4ObjectID {
	AacLc = 2,
	AacMain = 1,
}
</pre>

### New Type MonoTouch.AudioToolbox.SmpteTimeFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum SmpteTimeFlags {
	TimeRunning = 2,
	TimeValid = 1,
	Unknown = 0,
}
</pre>

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioTypeConverter

Added value:

<pre style='color: green'>
	MultiSplitter = 1836281964,
</pre>

### Type Changed: MonoTouch.AudioUnit.AudioUnit

Obsoleted methods:

```
[Obsolete ("Use SetFormat instead as it has the ability of returning a status code"]
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

### New Type MonoTouch.AudioUnit.AUAudioUnit

<pre style='color: green'>
public class AUAudioUnit : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public AUAudioUnit (MonoTouch.Foundation.NSCoder coder);
	public AUAudioUnit (MonoTouch.Foundation.NSObjectFlag t);
	public AUAudioUnit (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void RequestViewController (System.Action&lt;MonoTouch.CoreAudioKit.AUViewController&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;MonoTouch.CoreAudioKit.AUViewController&gt; RequestViewControllerAsync ();
}
</pre>

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAsset

Added property:

<pre style='color: green'>
	public virtual int UnusedTrackId { get; }
</pre>

Removed method:

<pre style='color: red'>
	public virtual AVMetadataItem[] ChapterMetadataGroups (MonoTouch.Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
</pre>

Added method:

<pre style='color: green'>
	public virtual AVTimedMetadataGroup[] ChapterMetadataGroups (MonoTouch.Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
</pre>

### Type Changed: MonoTouch.AVFoundation.AVAssetTrack

Removed method:

<pre style='color: red'>
	public virtual MonoTouch.Foundation.NSString GetAssociatedTracksOfType (MonoTouch.Foundation.NSString avAssetTrackTrackAssociationType);
</pre>

Added method:

<pre style='color: green'>
	public virtual AVAssetTrack[] GetAssociatedTracksOfType (MonoTouch.Foundation.NSString avAssetTrackTrackAssociationType);
</pre>

### Type Changed: MonoTouch.AVFoundation.AVAudioChannelLayout

Added interfaces:

<pre style='color: green'>
	MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.AVFoundation.AVAudioFormat

Added interfaces:

<pre style='color: green'>
	MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.AVFoundation.AVCompositionTrackSegment

Added property:

<pre style='color: green'>
	public virtual bool Empty { get; }
</pre>

### Type Changed: MonoTouch.AVFoundation.AVTextStyleRule

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public AVTextStyleRule ();
```

## Namespace MonoTouch.AVKit

### Type Changed: MonoTouch.AVKit.AVPlayerViewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

Added properties:

<pre style='color: green'>
	public virtual bool AllowsPictureInPicturePlayback { get; set; }
	public AVPlayerViewControllerDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
</pre>

### New Type MonoTouch.AVKit.AVPictureInPictureController

<pre style='color: green'>
public class AVPictureInPictureController : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public AVPictureInPictureController (MonoTouch.Foundation.NSCoder coder);
	public AVPictureInPictureController (MonoTouch.Foundation.NSObjectFlag t);
	public AVPictureInPictureController (IntPtr handle);
	public AVPictureInPictureController (MonoTouch.AVFoundation.AVPlayerLayer playerLayer);
	// properties
	public override IntPtr ClassHandle { get; }
	public AVPictureInPictureControllerDelegate Delegate { get; set; }
	public static bool IsPictureInPictureSupported { get; }
	public virtual bool PictureInPictureActive { get; }
	public virtual bool PictureInPicturePossible { get; }
	public virtual bool PictureInPictureSuspended { get; }
	public virtual MonoTouch.AVFoundation.AVPlayerLayer PlayerLayer { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void StartPictureInPicture ();
	public virtual void StopPictureInPicture ();
}
</pre>

### New Type MonoTouch.AVKit.AVPictureInPictureControllerDelegate

<pre style='color: green'>
public class AVPictureInPictureControllerDelegate : MonoTouch.Foundation.NSObject, IAVPictureInPictureControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public AVPictureInPictureControllerDelegate ();
	public AVPictureInPictureControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVPictureInPictureControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVPictureInPictureControllerDelegate (IntPtr handle);
	// methods
	public virtual void DidStartPictureInPicture (AVPictureInPictureController pictureInPictureController);
	public virtual void DidStopPictureInPicture (AVPictureInPictureController pictureInPictureController);
	public virtual void FailedToStartPictureInPicture (AVPictureInPictureController pictureInPictureController, MonoTouch.Foundation.NSError error);
	public virtual void RestoreUserInterfaceForPictureInPicture (AVPictureInPictureController pictureInPictureController, System.Action&lt;bool&gt; completionHandler);
	public virtual void WillStartPictureInPicture (AVPictureInPictureController pictureInPictureController);
	public virtual void WillStopPictureInPicture (AVPictureInPictureController pictureInPictureController);
}
</pre>

### New Type MonoTouch.AVKit.AVPictureInPictureControllerDelegate_Extensions

<pre style='color: green'>
public static class AVPictureInPictureControllerDelegate_Extensions {
	// methods
	public static void DidStartPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController);
	public static void DidStopPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController);
	public static void FailedToStartPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController, MonoTouch.Foundation.NSError error);
	public static void RestoreUserInterfaceForPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController, System.Action&lt;bool&gt; completionHandler);
	public static void WillStartPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController);
	public static void WillStopPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController);
}
</pre>

### New Type MonoTouch.AVKit.AVPlayerViewControllerDelegate

<pre style='color: green'>
public class AVPlayerViewControllerDelegate : MonoTouch.Foundation.NSObject, IAVPlayerViewControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public AVPlayerViewControllerDelegate ();
	public AVPlayerViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerViewControllerDelegate (IntPtr handle);
	// methods
	public virtual void DidStartPictureInPicture (AVPlayerViewController playerViewController);
	public virtual void DidStopPictureInPicture (AVPlayerViewController playerViewController);
	public virtual void FailedToStartPictureInPicture (AVPlayerViewController playerViewController, MonoTouch.Foundation.NSError error);
	public virtual void RestoreUserInterfaceForPictureInPicture (AVPlayerViewController playerViewController, System.Action&lt;bool&gt; completionHandler);
	public virtual bool ShouldAutomaticallyDismissAtPictureInPictureStart (AVPlayerViewController playerViewController);
	public virtual void WillStartPictureInPicture (AVPlayerViewController playerViewController);
	public virtual void WillStopPictureInPicture (AVPlayerViewController playerViewController);
}
</pre>

### New Type MonoTouch.AVKit.AVPlayerViewControllerDelegate_Extensions

<pre style='color: green'>
public static class AVPlayerViewControllerDelegate_Extensions {
	// methods
	public static void DidStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
	public static void DidStopPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
	public static void FailedToStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, MonoTouch.Foundation.NSError error);
	public static void RestoreUserInterfaceForPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, System.Action&lt;bool&gt; completionHandler);
	public static bool ShouldAutomaticallyDismissAtPictureInPictureStart (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
	public static void WillStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
	public static void WillStopPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
}
</pre>

### New Type MonoTouch.AVKit.IAVPictureInPictureControllerDelegate

<pre style='color: green'>
public interface IAVPictureInPictureControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.AVKit.IAVPlayerViewControllerDelegate

<pre style='color: green'>
public interface IAVPlayerViewControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

## Namespace MonoTouch.CloudKit

### Type Changed: MonoTouch.CloudKit.CKRecordID

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public CKRecordID ();
```

### Type Changed: MonoTouch.CloudKit.CKRecordZoneID

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public CKRecordZoneID ();
```

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

### New Type MonoTouch.CoreAnimation.CASpringAnimation

<pre style='color: green'>
public class CASpringAnimation : MonoTouch.CoreAnimation.CABasicAnimation, ICAAction, ICAMediaTiming, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CASpringAnimation ();
	public CASpringAnimation (MonoTouch.Foundation.NSCoder coder);
	public CASpringAnimation (MonoTouch.Foundation.NSObjectFlag t);
	public CASpringAnimation (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual float Damping { get; set; }
	public virtual float InitialVelocity { get; set; }
	public virtual float Mass { get; set; }
	public virtual double SettlingDuration { get; }
	public virtual float Stiffness { get; set; }
	// methods
	public static CABasicAnimation FromKeyPath (string path);
}
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

### New Type MonoTouch.CoreAudioKit.AUViewController

<pre style='color: green'>
public class AUViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAppearanceContainer, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public AUViewController ();
	public AUViewController (MonoTouch.Foundation.NSCoder coder);
	public AUViewController (MonoTouch.Foundation.NSObjectFlag t);
	public AUViewController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBPeer

Obsoleted constructors:

```
[Obsolete ("This type is not meant to be created by user code."]
	public CBPeer ();
```

## Namespace MonoTouch.CoreData

### Type Changed: MonoTouch.CoreData.NSManagedObjectContext

Added method:

<pre style='color: green'>
	public virtual NSManagedObject GetExistingObject (NSManagedObjectID objectID, out MonoTouch.Foundation.NSError error);
</pre>

## Namespace MonoTouch.CoreFoundation

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
[Obsolete ("Use a real `null` value instead of this managed wrapper over a null native instance"]
	public static CGColorSpace Null;
```

Added methods:

<pre style='color: green'>
	public static CGColorSpace CreateAdobeRGB1988 ();
	public static CGColorSpace CreateGenericCMYK ();
	public static CGColorSpace CreateGenericGray ();
	public static CGColorSpace CreateGenericGrayGamma2_2 ();
	public static CGColorSpace CreateGenericRGB ();
	public static CGColorSpace CreateGenericRGBLinear ();
	public static CGColorSpace CreateSRGB ();
</pre>

### New Type MonoTouch.CoreGraphics.CGColorSpaceNames

<pre style='color: green'>
public static class CGColorSpaceNames {
	// properties
	public static MonoTouch.Foundation.NSString AdobeRGB1998 { get; }
	public static MonoTouch.Foundation.NSString GenericCMYK { get; }
	public static MonoTouch.Foundation.NSString GenericGray { get; }
	public static MonoTouch.Foundation.NSString GenericGrayGamma2_2 { get; }
	public static MonoTouch.Foundation.NSString GenericRGB { get; }
	public static MonoTouch.Foundation.NSString GenericRGBLinear { get; }
	public static MonoTouch.Foundation.NSString SRGB { get; }
}
</pre>

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIAccordionFoldTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIAdditionCompositing

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIAffineClamp

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIAffineFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIAffineTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIAffineTransform

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIAreaHistogram

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIAztecCodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoTouch.CoreImage.CIFilter</span></span>

 <span style='color:green'>MonoTouch.CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public MonoTouch.Foundation.NSData Message { get; set; }
</pre>

### Type Changed: MonoTouch.CoreImage.CIBarsSwipeTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIBlendFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIBlendWithAlphaMask

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIBlendWithMask

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIBloom

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIBumpDistortion

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIBumpDistortionLinear

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CICheckerboardGenerator

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CICircleSplashDistortion

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CICircularScreen

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CICode128BarcodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoTouch.CoreImage.CIFilter</span></span>

 <span style='color:green'>MonoTouch.CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public MonoTouch.Foundation.NSData Message { get; set; }
</pre>

### Type Changed: MonoTouch.CoreImage.CIColor

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorBurnBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorClamp

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorControls

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorCrossPolynomial

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorCube

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorCubeWithColorSpace

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorDodgeBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorInvert

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorMap

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorMatrix

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorMonochrome

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorPolynomial

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIColorPosterize

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CICompositingFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIConstantColorGenerator

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIConvolution3X3

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIConvolution5X5

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIConvolution9Horizontal

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIConvolution9Vertical

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIConvolutionCore

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CICopyMachineTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CICrop

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIDarkenBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIDifferenceBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIDisintegrateWithMaskTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIDissolveTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIDistortionFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIDivideBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIDotScreen

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIEightfoldReflectedTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIExclusionBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIExposureAdjust

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIFaceBalance

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIFalseColor

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIFilterAttributes

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString TypeColor { get; }
</pre>

### Type Changed: MonoTouch.CoreImage.CIFlashTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIFourfoldReflectedTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIFourfoldRotatedTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIFourfoldTranslatedTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIGammaAdjust

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIGaussianBlur

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIGaussianGradient

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIGlassDistortion

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIGlideReflectedTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIGloom

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIHardLightBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIHatchedScreen

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIHighlightShadowAdjust

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIHistogramDisplayFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIHoleDistortion

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIHueAdjust

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIHueBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIImage

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILanczosScaleTransform

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILightenBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILightTunnel

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILinearBurnBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILinearDodgeBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILinearGradient

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILinearToSRGBToneCurve

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILineScreen

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CILuminosityBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIMaskToAlpha

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIMaximumComponent

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIMaximumCompositing

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIMinimumComponent

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIMinimumCompositing

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIModTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIMotionBlur

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIMultiplyBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIMultiplyCompositing

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIOverlayBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPerspectiveCorrection

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPerspectiveTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPerspectiveTransform

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPerspectiveTransformWithExtent

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffect

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectChrome

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectFade

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectInstant

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectMono

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectNoir

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectProcess

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectTonal

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectTransfer

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPinchDistortion

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPinLightBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIPixellate

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIQRCodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoTouch.CoreImage.CIFilter</span></span>

 <span style='color:green'>MonoTouch.CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public MonoTouch.Foundation.NSData Message { get; set; }
</pre>

### Type Changed: MonoTouch.CoreImage.CIRadialGradient

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIRandomGenerator

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISaturationBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIScreenBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIScreenFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISepiaTone

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISharpenLuminance

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISixfoldReflectedTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISixfoldRotatedTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISmoothLinearGradient

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISoftLightBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISourceAtopCompositing

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISourceInCompositing

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISourceOutCompositing

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISourceOverCompositing

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISRGBToneCurveToLinear

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIStarShineGenerator

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIStraightenFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIStripesGenerator

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISubtractBlendMode

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CISwipeTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CITemperatureAndTint

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CITileFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIToneCurve

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CITransitionFilter

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CITriangleKaleidoscope

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CITwelvefoldReflectedTile

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CITwirlDistortion

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIUnsharpMask

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIVector

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIVibrance

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIVignette

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIVignetteEffect

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIVortexDistortion

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIWhitePointAdjust

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.CoreImage.CIZoomBlur

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### New Type MonoTouch.CoreImage.CIAreaAverage

<pre style='color: green'>
public class CIAreaAverage : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaAverage ();
	public CIAreaAverage (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIAreaMaximum

<pre style='color: green'>
public class CIAreaMaximum : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMaximum ();
	public CIAreaMaximum (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIAreaMaximumAlpha

<pre style='color: green'>
public class CIAreaMaximumAlpha : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMaximumAlpha ();
	public CIAreaMaximumAlpha (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIAreaMinimum

<pre style='color: green'>
public class CIAreaMinimum : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMinimum ();
	public CIAreaMinimum (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIAreaMinimumAlpha

<pre style='color: green'>
public class CIAreaMinimumAlpha : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMinimumAlpha ();
	public CIAreaMinimumAlpha (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIBoxBlur

<pre style='color: green'>
public class CIBoxBlur : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIBoxBlur ();
	public CIBoxBlur (IntPtr handle);
}
</pre>

### New Type MonoTouch.CoreImage.CICircularWrap

<pre style='color: green'>
public class CICircularWrap : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CICircularWrap ();
	public CICircularWrap (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CICMYKHalftone

<pre style='color: green'>
public class CICMYKHalftone : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CICMYKHalftone ();
	public CICMYKHalftone (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float GrayComponentReplacement { get; set; }
	public float InputSharpness { get; set; }
	public float UnderColorRemoval { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CICodeGenerator

<pre style='color: green'>
public abstract class CICodeGenerator : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CICodeGenerator (string name);
	public CICodeGenerator (IntPtr handle);
	// properties
	public MonoTouch.Foundation.NSData Message { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIColumnAverage

<pre style='color: green'>
public class CIColumnAverage : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIColumnAverage ();
	public CIColumnAverage (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIComicEffect

<pre style='color: green'>
public class CIComicEffect : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIComicEffect ();
	public CIComicEffect (IntPtr handle);
}
</pre>

### New Type MonoTouch.CoreImage.CIConvolution7X7

<pre style='color: green'>
public class CIConvolution7X7 : MonoTouch.CoreImage.CIConvolutionCore, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIConvolution7X7 ();
	public CIConvolution7X7 (IntPtr handle);
}
</pre>

### New Type MonoTouch.CoreImage.CICrystallize

<pre style='color: green'>
public class CICrystallize : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CICrystallize ();
	public CICrystallize (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIDepthOfField

<pre style='color: green'>
public class CIDepthOfField : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIDepthOfField ();
	public CIDepthOfField (IntPtr handle);
	// properties
	public CIVector Point1 { get; set; }
	public CIVector Point2 { get; set; }
	public float Radius { get; set; }
	public float Saturation { get; set; }
	public float UnsharpMaskIntensity { get; set; }
	public float UnsharpMaskRadius { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIDiscBlur

<pre style='color: green'>
public class CIDiscBlur : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIDiscBlur ();
	public CIDiscBlur (IntPtr handle);
}
</pre>

### New Type MonoTouch.CoreImage.CIDisplacementDistortion

<pre style='color: green'>
public class CIDisplacementDistortion : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIDisplacementDistortion ();
	public CIDisplacementDistortion (IntPtr handle);
	// properties
	public float Scale { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIDroste

<pre style='color: green'>
public class CIDroste : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIDroste ();
	public CIDroste (IntPtr handle);
	// properties
	public CIVector InsetPoint0 { get; set; }
	public CIVector InsetPoint1 { get; set; }
	public float Periodicity { get; set; }
	public float Rotation { get; set; }
	public float Strands { get; set; }
	public float Zoom { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIEdges

<pre style='color: green'>
public class CIEdges : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIEdges ();
	public CIEdges (IntPtr handle);
}
</pre>

### New Type MonoTouch.CoreImage.CIEdgeWork

<pre style='color: green'>
public class CIEdgeWork : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIEdgeWork ();
	public CIEdgeWork (IntPtr handle);
}
</pre>

### New Type MonoTouch.CoreImage.CIGlassLozenge

<pre style='color: green'>
public class CIGlassLozenge : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIGlassLozenge ();
	public CIGlassLozenge (IntPtr handle);
	// properties
	public CIVector Point0 { get; set; }
	public CIVector Point1 { get; set; }
	public float Radius { get; set; }
	public float Refraction { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIHeightFieldFromMask

<pre style='color: green'>
public class CIHeightFieldFromMask : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIHeightFieldFromMask ();
	public CIHeightFieldFromMask (IntPtr handle);
}
</pre>

### New Type MonoTouch.CoreImage.CIHexagonalPixellate

<pre style='color: green'>
public class CIHexagonalPixellate : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIHexagonalPixellate ();
	public CIHexagonalPixellate (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Scale { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIKaleidoscope

<pre style='color: green'>
public class CIKaleidoscope : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIKaleidoscope ();
	public CIKaleidoscope (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Count { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CILenticularHaloGenerator

<pre style='color: green'>
public class CILenticularHaloGenerator : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CILenticularHaloGenerator ();
	public CILenticularHaloGenerator (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIColor Color { get; set; }
	public float HaloOverlap { get; set; }
	public float HaloRadius { get; set; }
	public float HaloWidth { get; set; }
	public float StriationContrast { get; set; }
	public float StriationStrength { get; set; }
	public float Time { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CILineOverlay

<pre style='color: green'>
public class CILineOverlay : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CILineOverlay ();
	public CILineOverlay (IntPtr handle);
	// properties
	public float Contrast { get; set; }
	public float EdgeIntensity { get; set; }
	public float NRNoiseLevel { get; set; }
	public float NRSharpness { get; set; }
	public float Threshold { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIMedianFilter

<pre style='color: green'>
public class CIMedianFilter : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIMedianFilter ();
	public CIMedianFilter (IntPtr handle);
}
</pre>

### New Type MonoTouch.CoreImage.CINoiseReduction

<pre style='color: green'>
public class CINoiseReduction : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CINoiseReduction ();
	public CINoiseReduction (IntPtr handle);
	// properties
	public float NoiseLevel { get; set; }
	public float Sharpness { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIOpTile

<pre style='color: green'>
public class CIOpTile : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIOpTile ();
	public CIOpTile (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Scale { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIPageCurlTransition

<pre style='color: green'>
public class CIPageCurlTransition : MonoTouch.CoreImage.CITransitionFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIPageCurlTransition ();
	public CIPageCurlTransition (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIImage BacksideImage { get; set; }
	public CIVector Extent { get; set; }
	public float Radius { get; set; }
	public CIImage ShadingImage { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIPageCurlWithShadowTransition

<pre style='color: green'>
public class CIPageCurlWithShadowTransition : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIPageCurlWithShadowTransition ();
	public CIPageCurlWithShadowTransition (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIImage BacksideImage { get; set; }
	public CIVector Extent { get; set; }
	public float InputTime { get; set; }
	public float Radius { get; set; }
	public float ShadowAmount { get; set; }
	public CIVector ShadowExtent { get; set; }
	public float ShadowSize { get; set; }
	public CIImage TargetImage { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIParallelogramTile

<pre style='color: green'>
public class CIParallelogramTile : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIParallelogramTile ();
	public CIParallelogramTile (IntPtr handle);
	// properties
	public float AcuteAngle { get; set; }
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIPDF417BarcodeGenerator

<pre style='color: green'>
public class CIPDF417BarcodeGenerator : MonoTouch.CoreImage.CICodeGenerator, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIPDF417BarcodeGenerator ();
	public CIPDF417BarcodeGenerator (IntPtr handle);
	// properties
	public int CompactionMode { get; set; }
	public bool CompactStyle { get; set; }
	public int CorrectionLevel { get; set; }
	public int DataColumns { get; set; }
	public float MaxHeight { get; set; }
	public float MaxWidth { get; set; }
	public float MinWidth { get; set; }
	public float PreferredAspectRatio { get; set; }
	public int Rows { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIPointillize

<pre style='color: green'>
public class CIPointillize : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIPointillize ();
	public CIPointillize (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIRippleTransition

<pre style='color: green'>
public class CIRippleTransition : MonoTouch.CoreImage.CITransitionFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIRippleTransition ();
	public CIRippleTransition (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIVector Extent { get; set; }
	public float Scale { get; set; }
	public CIImage ShadingImage { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIRowAverage

<pre style='color: green'>
public class CIRowAverage : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIRowAverage ();
	public CIRowAverage (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIShadedMaterial

<pre style='color: green'>
public class CIShadedMaterial : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIShadedMaterial ();
	public CIShadedMaterial (IntPtr handle);
	// properties
	public float Scale { get; set; }
	public CIImage ShadingImage { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CISpotColor

<pre style='color: green'>
public class CISpotColor : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CISpotColor ();
	public CISpotColor (IntPtr handle);
	// properties
	public CIColor CenterColor1 { get; set; }
	public CIColor CenterColor2 { get; set; }
	public CIColor CenterColor3 { get; set; }
	public float Closeness1 { get; set; }
	public float Closeness2 { get; set; }
	public float Closeness3 { get; set; }
	public float Contrast1 { get; set; }
	public float Contrast2 { get; set; }
	public float Contrast3 { get; set; }
	public CIColor ReplacementColor1 { get; set; }
	public CIColor ReplacementColor2 { get; set; }
	public CIColor ReplacementColor3 { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CISpotLight

<pre style='color: green'>
public class CISpotLight : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CISpotLight ();
	public CISpotLight (IntPtr handle);
	// properties
	public float Brightness { get; set; }
	public CIColor Color { get; set; }
	public float Concentration { get; set; }
	public CIVector LightPointsAt { get; set; }
	public CIVector LightPosition { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CIStretchCrop

<pre style='color: green'>
public class CIStretchCrop : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CIStretchCrop ();
	public CIStretchCrop (IntPtr handle);
	// properties
	public float CenterStretchAmount { get; set; }
	public float CropAmount { get; set; }
	public CIVector Size { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CISunbeamsGenerator

<pre style='color: green'>
public class CISunbeamsGenerator : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CISunbeamsGenerator ();
	public CISunbeamsGenerator (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIColor Color { get; set; }
	public float CropAmount { get; set; }
	public float MaxStriationRadius { get; set; }
	public float StriationContrast { get; set; }
	public float StriationStrength { get; set; }
	public float SunRadius { get; set; }
	public float Time { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CITorusLensDistortion

<pre style='color: green'>
public class CITorusLensDistortion : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CITorusLensDistortion ();
	public CITorusLensDistortion (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
	public float Refraction { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type MonoTouch.CoreImage.CITriangleTile

<pre style='color: green'>
public class CITriangleTile : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CITriangleTile ();
	public CITriangleTile (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Width { get; set; }
}
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

### Type Changed: MonoTouch.CoreMotion.CMPedometer

Added property:

<pre style='color: green'>
	public static bool IsPaceAvailable { get; }
</pre>

### Type Changed: MonoTouch.CoreMotion.CMPedometerData

Added property:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSNumber CurrentPace { get; }
</pre>

### New Type MonoTouch.CoreMotion.CMSensorDataList

<pre style='color: green'>
public class CMSensorDataList : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CMSensorDataList ();
	public CMSensorDataList (MonoTouch.Foundation.NSCoder coder);
	public CMSensorDataList (MonoTouch.Foundation.NSObjectFlag t);
	public CMSensorDataList (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type MonoTouch.CoreMotion.CMSensorRecorder

<pre style='color: green'>
public class CMSensorRecorder : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CMSensorRecorder ();
	public CMSensorRecorder (MonoTouch.Foundation.NSCoder coder);
	public CMSensorRecorder (MonoTouch.Foundation.NSObjectFlag t);
	public CMSensorRecorder (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static bool IsAccelerometerRecordingAvailable { get; }
	// methods
	public virtual CMSensorDataList GetAccelerometerData (MonoTouch.Foundation.NSDate fromDate, MonoTouch.Foundation.NSDate toDate);
	public virtual CMSensorDataList GetAccelerometerDataSince (ulong identifier);
	public virtual void RecordAccelerometerFor (double duration);
}
</pre>

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

### Type Changed: MonoTouch.Foundation.NSFormatter

Obsoleted methods:

```
[Obsolete ("Use GetEditingString instead"]
	public virtual string EditingStringFor (NSObject value);
	[Obsolete ("Use GetString instead"]
	public virtual string StringFor (NSObject value);
```

Added methods:

<pre style='color: green'>
	public NSAttributedString GetAttributedString (NSObject obj, MonoTouch.UIKit.UIStringAttributes attrs);
	public virtual NSAttributedString GetAttributedString (NSObject obj, NSDictionary attrs);
	public virtual string GetEditingString (NSObject value);
	public virtual bool GetObjectValue (out NSObject obj, string str, out NSString error);
	public virtual string GetString (NSObject value);
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

### Type Changed: MonoTouch.Foundation.NSObject

Added method:

<pre style='color: green'>
	public virtual void PrepareForInterfaceBuilder ();
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

### Type Changed: MonoTouch.Foundation.NSUrlSessionUploadTask


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoTouch.Foundation.NSUrlSessionTask</span></span>

 <span style='color:green'>MonoTouch.Foundation.NSUrlSessionDataTask</span>

### Type Changed: MonoTouch.Foundation.NSUserActivity

Added property:

<pre style='color: green'>
	public virtual MonoTouch.CoreSpotlight.CSSearchableItemAttributeSet ContentAttributeSet { get; set; }
</pre>

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

### Type Changed: MonoTouch.GameKit.GKLocalPlayerListener

Added method:

<pre style='color: green'>
	public virtual void WantsToQuitMatch (GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: MonoTouch.GameKit.GKMatch

Added event:

<pre style='color: green'>
	public event System.EventHandler&lt;GKDataReceivedForRecipientEventArgs&gt; DataReceivedForRecipient;
</pre>

### Type Changed: MonoTouch.GameKit.GKMatchDelegate

Added method:

<pre style='color: green'>
	public virtual void DataReceivedForRecipient (GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer recipient, GKPlayer player);
</pre>

### Type Changed: MonoTouch.GameKit.GKMatchDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DataReceivedForRecipient (IGKMatchDelegate This, GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer recipient, GKPlayer player);
</pre>

### Type Changed: MonoTouch.GameKit.GKMatchmakerViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoTouch.UIKit.UIViewController</span></span>

 <span style='color:green'>MonoTouch.UIKit.UINavigationController</span>

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.GameKit.GKPlayer

Added property:

<pre style='color: green'>
	public virtual string GuestIdentifier { get; }
</pre>

Added method:

<pre style='color: green'>
	public static GKPlayer GetAnonymousGuestPlayer (string guestIdentifier);
</pre>

### Type Changed: MonoTouch.GameKit.GKTurnBasedEventListener

Added method:

<pre style='color: green'>
	public virtual void WantsToQuitMatch (GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: MonoTouch.GameKit.GKTurnBasedEventListener_Extensions

Added method:

<pre style='color: green'>
	public static void WantsToQuitMatch (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match);
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

### New Type MonoTouch.GameKit.GKDataReceivedForRecipientEventArgs

<pre style='color: green'>
public class GKDataReceivedForRecipientEventArgs : System.EventArgs {
	// constructors
	public GKDataReceivedForRecipientEventArgs (MonoTouch.Foundation.NSData data, GKPlayer recipient, GKPlayer player);
	// properties
	public MonoTouch.Foundation.NSData Data { get; set; }
	public GKPlayer Player { get; set; }
	public GKPlayer Recipient { get; set; }
}
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

### New Type MonoTouch.GLKit.GLKMesh

<pre style='color: green'>
public class GLKMesh : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public GLKMesh ();
	public GLKMesh (MonoTouch.Foundation.NSCoder coder);
	public GLKMesh (MonoTouch.Foundation.NSObjectFlag t);
	public GLKMesh (IntPtr handle);
	public GLKMesh (MonoTouch.ModelIO.MDLMesh mesh);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Matrix4 Matrix { get; }
	public virtual string Name { get; }
	public virtual GLKSubmesh[] Submeshes { get; }
	public virtual GLKMeshBuffer[] VertexBuffers { get; }
	public virtual uint VertexCount { get; }
	public virtual MonoTouch.ModelIO.MDLVertexDescriptor VertexDescriptor { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static GLKMesh[] MeshesFromAsset (MonoTouch.ModelIO.MDLAsset asset);
}
</pre>

### New Type MonoTouch.GLKit.GLKMeshBuffer

<pre style='color: green'>
public class GLKMeshBuffer : MonoTouch.Foundation.NSObject, MonoTouch.ModelIO.IMDLMeshBuffer, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public GLKMeshBuffer ();
	public GLKMeshBuffer (MonoTouch.Foundation.NSCoder coder);
	public GLKMeshBuffer (MonoTouch.Foundation.NSObjectFlag t);
	public GLKMeshBuffer (IntPtr handle);
	// properties
	public virtual MonoTouch.ModelIO.IMDLMeshBufferAllocator Allocator { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint GlBufferName { get; }
	public virtual uint Length { get; }
	public virtual MonoTouch.Foundation.NSData Map { get; }
	public virtual MonoTouch.ModelIO.MDLMeshBufferType Type { get; }
	public virtual MonoTouch.ModelIO.IMDLMeshBufferZone Zone { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Offset (MonoTouch.Foundation.NSData data, uint offset);
}
</pre>

### New Type MonoTouch.GLKit.GLKMeshBufferAllocator

<pre style='color: green'>
public class GLKMeshBufferAllocator : MonoTouch.Foundation.NSObject, MonoTouch.ModelIO.IMDLMeshBufferAllocator, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public GLKMeshBufferAllocator (MonoTouch.Foundation.NSCoder coder);
	public GLKMeshBufferAllocator (MonoTouch.Foundation.NSObjectFlag t);
	public GLKMeshBufferAllocator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.ModelIO.IMDLMeshBuffer NewBuffer (uint length, MonoTouch.ModelIO.MDLMeshBufferType type);
	public virtual MonoTouch.ModelIO.IMDLMeshBuffer NewBufferFromZone (MonoTouch.ModelIO.IMDLMeshBufferZone zone, uint length, MonoTouch.ModelIO.MDLMeshBufferType type);
	public virtual MonoTouch.ModelIO.IMDLMeshBuffer NewBufferFromZone (MonoTouch.ModelIO.IMDLMeshBufferZone zone, MonoTouch.Foundation.NSData data, MonoTouch.ModelIO.MDLMeshBufferType type);
	public virtual MonoTouch.ModelIO.IMDLMeshBuffer NewBufferWithData (MonoTouch.Foundation.NSData data, MonoTouch.ModelIO.MDLMeshBufferType type);
	public virtual MonoTouch.ModelIO.IMDLMeshBufferZone NewZone (uint capacity);
}
</pre>

### New Type MonoTouch.GLKit.GLKSubmesh

<pre style='color: green'>
public class GLKSubmesh : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public GLKSubmesh ();
	public GLKSubmesh (MonoTouch.Foundation.NSCoder coder);
	public GLKSubmesh (MonoTouch.Foundation.NSObjectFlag t);
	public GLKSubmesh (IntPtr handle);
	public GLKSubmesh (GLKMesh mesh, MonoTouch.ModelIO.MDLSubmesh submesh);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GLKMeshBuffer ElementBuffer { get; }
	public virtual int ElementCount { get; }
	public virtual MonoTouch.ModelIO.MDLMaterial Material { get; set; }
	public virtual GLKMesh Mesh { get; }
	public virtual uint Mode { get; }
	public virtual string Name { get; }
	public virtual uint Type { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.GLKit.GLKVertexAttributeParameters

<pre style='color: green'>
public struct GLKVertexAttributeParameters {
	// fields
	public uint GlSize;
	public uint GlType;
	public bool Normalized;
	// methods
	public static GLKVertexAttributeParameters FromVertexFormat (MonoTouch.ModelIO.MDLVertexFormat vertexFormat);
}
</pre>

## Namespace MonoTouch.HealthKit

### Type Changed: MonoTouch.HealthKit.HKBiologicalSexObject

Added interfaces:

<pre style='color: green'>
	MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSSecureCoding
</pre>

Added method:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
</pre>

### Type Changed: MonoTouch.HealthKit.HKBloodTypeObject

Added interfaces:

<pre style='color: green'>
	MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSSecureCoding
</pre>

Added method:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
</pre>

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

## Namespace MonoTouch.JavaScriptCore

### Type Changed: MonoTouch.JavaScriptCore.JSValue

Added properties:

<pre style='color: green'>
	public virtual bool IsArray { get; }
	public virtual bool IsDate { get; }
</pre>

## Namespace MonoTouch.LocalAuthentication

### Type Changed: MonoTouch.LocalAuthentication.LAContext

Added properties:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSData EvaluatedPolicyDomainState { get; set; }
	public static double LATouchIdAuthenticationMaximumAllowableReuseDuration { get; }
	public virtual double TouchIdAuthenticationAllowableReuseDuration { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void EvaluateAccessControl (MonoTouch.Security.SecAccessControl accessControl, LAAccessControlOperation operation, string localizedReason, System.Action&lt;System.Boolean,MonoTouch.Foundation.NSError&gt; reply);
	public virtual void Invalidate ();
	public virtual bool IsCredentialSet (LACredentialType type);
	public virtual bool SetCredentialType (MonoTouch.Foundation.NSData credential, LACredentialType type);
</pre>

### Type Changed: MonoTouch.LocalAuthentication.LAPolicy

Added value:

<pre style='color: green'>
	DeviceOwnerAuthentication = 2,
</pre>

### Type Changed: MonoTouch.LocalAuthentication.LAStatus

Added values:

<pre style='color: green'>
	AppCancel = -9,
	InvalidContext = -10,
	TouchIDLockout = -8,
</pre>

### New Type MonoTouch.LocalAuthentication.LAAccessControlOperation

<pre style='color: green'>
[Serializable]
public enum LAAccessControlOperation {
	CreateItem = 0,
	CreateKey = 2,
	UseItem = 1,
	UseKeySign = 3,
}
</pre>

### New Type MonoTouch.LocalAuthentication.LACredentialType

<pre style='color: green'>
[Serializable]
public enum LACredentialType {
	ApplicationPassword = 0,
}
</pre>

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

Added property:

<pre style='color: green'>
	public virtual MonoTouch.UIKit.UIView DetailCalloutAccessoryView { get; set; }
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

### Type Changed: MonoTouch.MapKit.MKDirections

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public MKDirections ();
```

### Type Changed: MonoTouch.MapKit.MKDirectionsMode

Added value:

<pre style='color: green'>
	Transit = 2,
</pre>

### Type Changed: MonoTouch.MapKit.MKDirectionsTransportType

Added value:

<pre style='color: green'>
	Transit = 4,
</pre>

### Type Changed: MonoTouch.MapKit.MKETAResponse

Added properties:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSDate ExpectedArrivalDate { get; }
	public virtual MonoTouch.Foundation.NSDate ExpectedDepartureDate { get; }
	public virtual MKDirectionsTransportType TransportType { get; }
</pre>

### Type Changed: MonoTouch.MapKit.MKMapCamera

Added method:

<pre style='color: green'>
	public static MKMapCamera CameraLookingAtCenterCoordinate (MonoTouch.CoreLocation.CLLocationCoordinate2D centerCoordinate, double locationDistance, float pitch, double locationDirectionHeading);
</pre>

### Type Changed: MonoTouch.MapKit.MKMapItem

Added property:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSTimeZone TimeZone { get; set; }
</pre>

### Type Changed: MonoTouch.MapKit.MKMapType

Added values:

<pre style='color: green'>
	HybridFlyover = 4,
	SatelliteFlyover = 3,
</pre>

### Type Changed: MonoTouch.MapKit.MKMapView

Added interfaces:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearance
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

Added properties:

<pre style='color: green'>
	public virtual bool ShowsCompass { get; set; }
	public virtual bool ShowsScale { get; set; }
	public virtual bool ShowsTraffic { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void _HandleSelectionAtPoint (System.Drawing.PointF locationInView);
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

Added properties:

<pre style='color: green'>
	public static MonoTouch.UIKit.UIColor GreenPinColor { get; }
	public virtual MonoTouch.UIKit.UIColor PinTintColor { get; set; }
	public static MonoTouch.UIKit.UIColor PurplePinColor { get; }
	public static MonoTouch.UIKit.UIColor RedPinColor { get; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView.MKPinAnnotationViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKPinAnnotationView (IntPtr handle);
</pre>

Added property:

<pre style='color: green'>
	public virtual MonoTouch.UIKit.UIColor PinTintColor { get; set; }
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

### Type Changed: MonoTouch.MediaPlayer.MPMediaItem

Added method:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSObject GetObject (MonoTouch.Foundation.NSObject key);
</pre>

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

### Type Changed: MonoTouch.MediaPlayer.MPPlayableContentDelegate

Obsoleted methods:

```
[Obsolete ("Use InitiatePlaybackOfContentItem instead"]
	public virtual void PlayableContentManager (MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

<pre style='color: green'>
	public virtual void ContextUpdated (MPPlayableContentManager contentManager, MPPlayableContentManagerContext context);
	public virtual void InitiatePlaybackOfContentItem (MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPPlayableContentDelegate_Extensions

Obsoleted methods:

```
[Obsolete ("Use InitiatePlaybackOfContentItem instead"]
	public static void PlayableContentManager (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

<pre style='color: green'>
	public static void ContextUpdated (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MPPlayableContentManagerContext context);
	public static void InitiatePlaybackOfContentItem (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPPlayableContentManager

Added property:

<pre style='color: green'>
	public virtual MPPlayableContentManagerContext Context { get; }
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

### New Type MonoTouch.MediaPlayer.MPPlayableContentManagerContext

<pre style='color: green'>
public class MPPlayableContentManagerContext : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MPPlayableContentManagerContext ();
	public MPPlayableContentManagerContext (MonoTouch.Foundation.NSCoder coder);
	public MPPlayableContentManagerContext (MonoTouch.Foundation.NSObjectFlag t);
	public MPPlayableContentManagerContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool ContentLimitsEnforced { get; }
	public virtual bool EndpointAvailable { get; }
	public virtual int EnforcedContentItemsCount { get; }
	public virtual int EnforcedContentTreeDepth { get; }
}
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

## Namespace MonoTouch.MobileCoreServices

### Type Changed: MonoTouch.MobileCoreServices.UTType

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString SwiftSource { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSDictionary GetDeclaration (string uti);
	public static MonoTouch.Foundation.NSUrl GetDeclaringBundleURL (string uti);
	public static string GetPreferredTag (string uti, string tagClass);
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
	public static bool bool_objc_msgSend_float_float_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, float arg1, float arg2, IntPtr arg3, IntPtr arg4);
	public static bool bool_objc_msgSend_float_float_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, float arg1, float arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
	public static bool bool_objc_msgSend_float_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, float arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
	public static bool bool_objc_msgSend_int_float_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, float arg2, IntPtr arg3, IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_ref_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref IntPtr arg2, IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_ref_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref IntPtr arg2, ref IntPtr arg3);
	public static bool bool_objc_msgSend_ref_IntPtr_out_NSRange_IntPtr_NSRange_ref_IntPtr (IntPtr receiver, IntPtr selector, ref IntPtr arg1, out MonoTouch.Foundation.NSRange arg2, IntPtr arg3, MonoTouch.Foundation.NSRange arg4, ref IntPtr arg5);
	public static bool bool_objc_msgSend_Vector2i_int_float_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector2i arg1, int arg2, float arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6);
	public static bool bool_objc_msgSend_Vector2i_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector2i arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
	public static bool bool_objc_msgSendSuper_float_float_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, float arg1, float arg2, IntPtr arg3, IntPtr arg4);
	public static bool bool_objc_msgSendSuper_float_float_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, float arg1, float arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
	public static bool bool_objc_msgSendSuper_float_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, float arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
	public static bool bool_objc_msgSendSuper_int_float_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, float arg2, IntPtr arg3, IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_ref_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref IntPtr arg2, IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_ref_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref IntPtr arg2, ref IntPtr arg3);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_out_NSRange_IntPtr_NSRange_ref_IntPtr (IntPtr receiver, IntPtr selector, ref IntPtr arg1, out MonoTouch.Foundation.NSRange arg2, IntPtr arg3, MonoTouch.Foundation.NSRange arg4, ref IntPtr arg5);
	public static bool bool_objc_msgSendSuper_Vector2i_int_float_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector2i arg1, int arg2, float arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6);
	public static bool bool_objc_msgSendSuper_Vector2i_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector2i arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
	public static IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_Double_float_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2, float arg3, double arg4);
	public static IntPtr IntPtr_objc_msgSend_float_bool_IntPtr (IntPtr receiver, IntPtr selector, float arg1, bool arg2, IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_float_Vector2_UInt32_UInt32_int_bool_IntPtr (IntPtr receiver, IntPtr selector, float arg1, OpenTK.Vector2 arg2, uint arg3, uint arg4, int arg5, bool arg6, IntPtr arg7);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, bool arg4, bool arg5);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_IntPtr_Vector2i_int_UInt32_int_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, OpenTK.Vector2i arg4, int arg5, uint arg6, int arg7, bool arg8);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_float_float (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, float arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_UInt32_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3, uint arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_UInt32_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, uint arg3, int arg4, int arg5, IntPtr arg6);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_Vector2i (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, OpenTK.Vector2i arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_Vector2i_float (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, OpenTK.Vector2i arg3, float arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_float (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, float arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, int arg3, int arg4, IntPtr arg5);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_Matrix4 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, OpenTK.Matrix4 arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_Vector2 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, OpenTK.Vector2 arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_Vector3 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, OpenTK.Vector3 arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_Vector4 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, OpenTK.Vector4 arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_Matrix4 (IntPtr receiver, IntPtr selector, OpenTK.Matrix4 arg1);
	public static IntPtr IntPtr_objc_msgSend_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1);
	public static IntPtr IntPtr_objc_msgSend_UInt32_out_NSRange_bool (IntPtr receiver, IntPtr selector, uint arg1, out MonoTouch.Foundation.NSRange arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSend_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static IntPtr IntPtr_objc_msgSend_Vector2_Vector2i_int_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector2 arg1, OpenTK.Vector2i arg2, int arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSend_Vector3 (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1);
	public static IntPtr IntPtr_objc_msgSend_Vector3_UInt32_UInt32_int_bool_bool_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1, uint arg2, uint arg3, int arg4, bool arg5, bool arg6, IntPtr arg7);
	public static IntPtr IntPtr_objc_msgSend_Vector3_Vector3i_bool_int_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1, OpenTK.Vector3i arg2, bool arg3, int arg4, IntPtr arg5);
	public static IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_Double_float_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2, float arg3, double arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_float_bool_IntPtr (IntPtr receiver, IntPtr selector, float arg1, bool arg2, IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_float_Vector2_UInt32_UInt32_int_bool_IntPtr (IntPtr receiver, IntPtr selector, float arg1, OpenTK.Vector2 arg2, uint arg3, uint arg4, int arg5, bool arg6, IntPtr arg7);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, bool arg4, bool arg5);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_IntPtr_Vector2i_int_UInt32_int_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, OpenTK.Vector2i arg4, int arg5, uint arg6, int arg7, bool arg8);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_float (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, float arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_UInt32_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3, uint arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_UInt32_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, uint arg3, int arg4, int arg5, IntPtr arg6);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_Vector2i (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, OpenTK.Vector2i arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_Vector2i_float (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, OpenTK.Vector2i arg3, float arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_float (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, float arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, int arg3, int arg4, IntPtr arg5);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_Matrix4 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, OpenTK.Matrix4 arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_Vector2 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, OpenTK.Vector2 arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_Vector3 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, OpenTK.Vector3 arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_Vector4 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, OpenTK.Vector4 arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_Matrix4 (IntPtr receiver, IntPtr selector, OpenTK.Matrix4 arg1);
	public static IntPtr IntPtr_objc_msgSendSuper_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1);
	public static IntPtr IntPtr_objc_msgSendSuper_UInt32_out_NSRange_bool (IntPtr receiver, IntPtr selector, uint arg1, out MonoTouch.Foundation.NSRange arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static IntPtr IntPtr_objc_msgSendSuper_Vector2_Vector2i_int_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector2 arg1, OpenTK.Vector2i arg2, int arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_Vector3 (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1);
	public static IntPtr IntPtr_objc_msgSendSuper_Vector3_UInt32_UInt32_int_bool_bool_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1, uint arg2, uint arg3, int arg4, bool arg5, bool arg6, IntPtr arg7);
	public static IntPtr IntPtr_objc_msgSendSuper_Vector3_Vector3i_bool_int_IntPtr (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1, OpenTK.Vector3i arg2, bool arg3, int arg4, IntPtr arg5);
	public static void Matrix4_objc_msgSend_stret_Double (out OpenTK.Matrix4 retval, IntPtr receiver, IntPtr selector, double arg1);
	public static void Matrix4_objc_msgSend_stret_IntPtr_Double (out OpenTK.Matrix4 retval, IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2);
	public static void Matrix4_objc_msgSendSuper_stret_Double (out OpenTK.Matrix4 retval, IntPtr receiver, IntPtr selector, double arg1);
	public static void Matrix4_objc_msgSendSuper_stret_IntPtr_Double (out OpenTK.Matrix4 retval, IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2);
	public static void MDLAxisAlignedBoundingBox_objc_msgSend_stret (out MonoTouch.ModelIO.MDLAxisAlignedBoundingBox retval, IntPtr receiver, IntPtr selector);
	public static void MDLAxisAlignedBoundingBox_objc_msgSend_stret_Double (out MonoTouch.ModelIO.MDLAxisAlignedBoundingBox retval, IntPtr receiver, IntPtr selector, double arg1);
	public static void MDLAxisAlignedBoundingBox_objc_msgSendSuper_stret (out MonoTouch.ModelIO.MDLAxisAlignedBoundingBox retval, IntPtr receiver, IntPtr selector);
	public static void MDLAxisAlignedBoundingBox_objc_msgSendSuper_stret_Double (out MonoTouch.ModelIO.MDLAxisAlignedBoundingBox retval, IntPtr receiver, IntPtr selector, double arg1);
	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static void NSRange_objc_msgSend_stret_IntPtr_UInt64_NSRange (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static void NSRange_objc_msgSendSuper_stret_IntPtr_UInt64_NSRange (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static void RectangleF_objc_msgSend_stret_UInt32_out_NSRange_bool (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, uint arg1, out MonoTouch.Foundation.NSRange arg2, bool arg3);
	public static void RectangleF_objc_msgSendSuper_stret_UInt32_out_NSRange_bool (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, uint arg1, out MonoTouch.Foundation.NSRange arg2, bool arg3);
	public static uint UInt32_objc_msgSend_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
	public static uint UInt32_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static uint UInt32_objc_msgSendSuper_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
	public static uint UInt32_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static OpenTK.Vector2i Vector2i_objc_msgSend (IntPtr receiver, IntPtr selector);
	public static void Vector2i_objc_msgSend_stret (out OpenTK.Vector2i retval, IntPtr receiver, IntPtr selector);
	public static OpenTK.Vector2i Vector2i_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
	public static void Vector2i_objc_msgSendSuper_stret (out OpenTK.Vector2i retval, IntPtr receiver, IntPtr selector);
	public static void Vector3_objc_msgSend_stret_Double (out OpenTK.Vector3 retval, IntPtr receiver, IntPtr selector, double arg1);
	public static void Vector3_objc_msgSendSuper_stret_Double (out OpenTK.Vector3 retval, IntPtr receiver, IntPtr selector, double arg1);
	public static void void_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSend_Matrix4_Double (IntPtr receiver, IntPtr selector, OpenTK.Matrix4 arg1, double arg2);
	public static void void_objc_msgSend_Vector3_Double (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1, double arg2);
	public static void void_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoTouch.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSendSuper_Matrix4_Double (IntPtr receiver, IntPtr selector, OpenTK.Matrix4 arg1, double arg2);
	public static void void_objc_msgSendSuper_Vector3_Double (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1, double arg2);
	public static void xamarin_vector_float3__Vector3_objc_msgSend_stret_Vector3 (out OpenTK.Vector3 retval, IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1);
	public static void xamarin_vector_float3__Vector3_objc_msgSendSuper_stret_Vector3 (out OpenTK.Vector3 retval, IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1);
	public static void xamarin_vector_float3__Vector4_objc_msgSend_stret (out OpenTK.Vector4 retval, IntPtr receiver, IntPtr selector);
	public static void xamarin_vector_float3__Vector4_objc_msgSendSuper_stret (out OpenTK.Vector4 retval, IntPtr receiver, IntPtr selector);
	public static void xamarin_vector_float3__void_objc_msgSend_Vector4 (IntPtr receiver, IntPtr selector, OpenTK.Vector4 arg1);
	public static void xamarin_vector_float3__void_objc_msgSendSuper_Vector4 (IntPtr receiver, IntPtr selector, OpenTK.Vector4 arg1);
</pre>

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added values:

<pre style='color: green'>
	iOS_8_4 = 525312,
	iOS_9_0 = 589824,
	Mac_10_10_3 = 2825757768286208,
	Mac_10_11 = 2826844395012096,
</pre>

## Namespace MonoTouch.OpenGLES

### Type Changed: MonoTouch.OpenGLES.EAGLContext

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public EAGLContext ();
```

Added method:

<pre style='color: green'>
	public static void EAGLGetVersion (out uint major, out uint minor);
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

## Namespace MonoTouch.Photos

### Type Changed: MonoTouch.Photos.PHAssetChangeRequest

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public PHAssetChangeRequest ();
```

## Namespace MonoTouch.QuickLook

### Type Changed: MonoTouch.QuickLook.QLPreviewController

Added interface:

<pre style='color: green'>
	MonoTouch.UIKit.IUIAppearanceContainer
</pre>

## Namespace MonoTouch.SafariServices

### New Type MonoTouch.SafariServices.ISFSafariViewControllerDelegate

<pre style='color: green'>
public interface ISFSafariViewControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.SafariServices.SFContentBlockerErrorCode

<pre style='color: green'>
[Serializable]
public enum SFContentBlockerErrorCode {
	LoadingInterrupted = 3,
	NoAttachmentFound = 2,
	NoExtensionFound = 1,
	Ok = 0,
}
</pre>

### New Type MonoTouch.SafariServices.SFContentBlockerManager

<pre style='color: green'>
public class SFContentBlockerManager : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public SFContentBlockerManager ();
	public SFContentBlockerManager (MonoTouch.Foundation.NSCoder coder);
	public SFContentBlockerManager (MonoTouch.Foundation.NSObjectFlag t);
	public SFContentBlockerManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public static void ReloadContentBlocker (string identifier, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
}
</pre>

### New Type MonoTouch.SafariServices.SFSafariViewController

<pre style='color: green'>
public class SFSafariViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAppearanceContainer, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public SFSafariViewController (MonoTouch.Foundation.NSCoder coder);
	public SFSafariViewController (MonoTouch.Foundation.NSObjectFlag t);
	public SFSafariViewController (IntPtr handle);
	public SFSafariViewController (MonoTouch.Foundation.NSUrl url, bool entersReaderIfAvailable);
	public SFSafariViewController (MonoTouch.Foundation.NSUrl url);
	// properties
	public override IntPtr ClassHandle { get; }
	public SFSafariViewControllerDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.SafariServices.SFSafariViewControllerDelegate

<pre style='color: green'>
public class SFSafariViewControllerDelegate : MonoTouch.Foundation.NSObject, ISFSafariViewControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public SFSafariViewControllerDelegate ();
	public SFSafariViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public SFSafariViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SFSafariViewControllerDelegate (IntPtr handle);
	// methods
	public virtual void DidFinish (SFSafariViewController controller);
	public virtual MonoTouch.UIKit.UIActivity[] GetActivityItemsForUrl (SFSafariViewController controller, MonoTouch.Foundation.NSUrl url, string title);
}
</pre>

### New Type MonoTouch.SafariServices.SFSafariViewControllerDelegate_Extensions

<pre style='color: green'>
public static class SFSafariViewControllerDelegate_Extensions {
	// methods
	public static void DidFinish (ISFSafariViewControllerDelegate This, SFSafariViewController controller);
	public static MonoTouch.UIKit.UIActivity[] GetActivityItemsForUrl (ISFSafariViewControllerDelegate This, SFSafariViewController controller, MonoTouch.Foundation.NSUrl url, string title);
}
</pre>

## Namespace MonoTouch.SceneKit

### Type Changed: MonoTouch.SceneKit.SCNAction

Added methods:

<pre style='color: green'>
	public static SCNAction Hide ();
	public static SCNAction Unhide ();
</pre>

### Type Changed: MonoTouch.SceneKit.SCNLight

Obsoleted methods:

```
[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
	public virtual MonoTouch.Foundation.NSObject GetAttribute (MonoTouch.Foundation.NSString lightAttribute);
	[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
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

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecAccessControl

Added interfaces:

<pre style='color: green'>
	MonoTouch.ObjCRuntime.INativeObject
	System.IDisposable
</pre>

Added property:

<pre style='color: green'>
	public virtual IntPtr Handle { get; }
</pre>

Added methods:

<pre style='color: green'>
	protected override void ~SecAccessControl ();
	public virtual void Dispose ();
	public virtual void Dispose (bool disposing);
</pre>

### Type Changed: MonoTouch.Security.SecAccessControlCreateFlags

Added values:

<pre style='color: green'>
	And = 32768,
	ApplicationPassword = -2147483648,
	DevicePasscode = 16,
	Or = 16384,
	PrivateKeyUsage = 1073741824,
	TouchIDAny = 2,
	TouchIDCurrentSet = 8,
</pre>

### Type Changed: MonoTouch.Security.SslCipherSuite

Added values:

<pre style='color: green'>
	TLS_DHE_RSA_WITH_AES_128_GCM_SHA256 = 158,
	TLS_DHE_RSA_WITH_AES_256_GCM_SHA384 = 159,
	TLS_ECDH_ECDSA_WITH_AES_128_GCM_SHA256 = 49197,
	TLS_ECDH_ECDSA_WITH_AES_256_GCM_SHA384 = 49198,
	TLS_ECDH_RSA_WITH_AES_128_GCM_SHA256 = 49201,
	TLS_ECDH_RSA_WITH_AES_256_GCM_SHA384 = 49202,
	TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256 = 49195,
	TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384 = 49196,
	TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 = 49199,
	TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 = 49200,
	TLS_RSA_WITH_AES_128_GCM_SHA256 = 156,
	TLS_RSA_WITH_AES_256_GCM_SHA384 = 157,
</pre>

### Type Changed: MonoTouch.Security.SslContext

Added method:

<pre style='color: green'>
	public SslStatus SetSessionStrengthPolicy (SslSessionStrengthPolicy policyStrength);
</pre>

### Type Changed: MonoTouch.Security.SslSessionOption

Added values:

<pre style='color: green'>
	AllowServerIdentityChange = 5,
	BreakOnClientHello = 7,
</pre>

### Type Changed: MonoTouch.Security.SslStatus

Added values:

<pre style='color: green'>
	SSLClientHelloReceived = -9851,
	SSLWeakPeerEphemeralDHKey = -9850,
</pre>

### New Type MonoTouch.Security.SslSessionStrengthPolicy

<pre style='color: green'>
[Serializable]
public enum SslSessionStrengthPolicy {
	ATSv1 = 1,
	Default = 0,
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
[Obsolete ("Use the method CreateVortexField instead"]
	public static SKFieldNode CraeteVortexField ();
```

Added method:

<pre style='color: green'>
	public static SKFieldNode CreateVortexField ();
</pre>

### Type Changed: MonoTouch.SpriteKit.SKTransition

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSCopying
</pre>

Added method:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
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

### Type Changed: MonoTouch.UIKit.NSLayoutManager

Added methods:

<pre style='color: green'>
	public virtual ushort CGGlyphAtIndex (uint glyphIndex, ref bool isValidIndex);
	public virtual ushort CGGlyphAtIndex (uint glyphIndex);
	public virtual System.Drawing.RectangleF LineFragmentRectForGlyphAtIndex (uint glyphIndex, out MonoTouch.Foundation.NSRange effectiveGlyphRange, bool withoutAdditionalLayout);
	public virtual System.Drawing.RectangleF LineFragmentUsedRectForGlyphAtIndex (uint glyphIndex, out MonoTouch.Foundation.NSRange effectiveGlyphRange, bool withoutAdditionalLayout);
	public virtual NSTextContainer TextContainerForGlyphAtIndex (uint glyphIndex, out MonoTouch.Foundation.NSRange effectiveGlyphRange, bool withoutAdditionalLayout);
</pre>

### Type Changed: MonoTouch.UIKit.NSTextContainer

Added property:

<pre style='color: green'>
	public virtual bool SimpleRectangularTextContainer { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void ReplaceLayoutManager (NSLayoutManager newLayoutManager);
</pre>

### Type Changed: MonoTouch.UIKit.UIAccessibilityCustomAction

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIAccessibilityCustomAction ();
```

### Type Changed: MonoTouch.UIKit.UIActionSheet

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

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIActivityItemProvider ();
```

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

### Type Changed: MonoTouch.UIKit.UIActivityType

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString OpenInIBooks { get; }
</pre>

### Type Changed: MonoTouch.UIKit.UIActivityViewController

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIActivityViewController ();
```

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
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

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Added methods:

<pre style='color: green'>
	public virtual void ApplicationShouldRequestHealthAuthorization (UIApplication application);
	public virtual void HandleAction (UIApplication application, string actionIdentifier, MonoTouch.Foundation.NSDictionary remoteNotificationInfo, MonoTouch.Foundation.NSDictionary responseInfo, System.Action completionHandler);
	public virtual void HandleAction (UIApplication application, string actionIdentifier, UILocalNotification localNotification, MonoTouch.Foundation.NSDictionary responseInfo, System.Action completionHandler);
	public virtual bool OpenUrl (UIApplication app, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
	public bool OpenUrl (UIApplication app, MonoTouch.Foundation.NSUrl url, UIApplicationOpenUrlOptions options);
</pre>

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static void ApplicationShouldRequestHealthAuthorization (IUIApplicationDelegate This, UIApplication application);
	public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, UILocalNotification localNotification, MonoTouch.Foundation.NSDictionary responseInfo, System.Action completionHandler);
	public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, MonoTouch.Foundation.NSDictionary remoteNotificationInfo, MonoTouch.Foundation.NSDictionary responseInfo, System.Action completionHandler);
	public static bool OpenUrl (IUIApplicationDelegate This, UIApplication app, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
	public static bool OpenUrl (IUIApplicationDelegate This, UIApplication app, MonoTouch.Foundation.NSUrl url, UIApplicationOpenUrlOptions options);
</pre>

### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Added interface:

<pre style='color: green'>
	IUIAppearance
</pre>

Added property:

<pre style='color: green'>
	public virtual UIBarButtonItemGroup ButtonGroup { get; }
</pre>

### Type Changed: MonoTouch.UIKit.UIBarButtonItem.UIBarButtonItemAppearance

Added constructor:

<pre style='color: green'>
	protected UIBarButtonItem (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIBarItem

Added interfaces:

<pre style='color: green'>
	MonoTouch.Foundation.INSCoding
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

### Type Changed: MonoTouch.UIKit.UICollectionViewTransitionLayout

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UICollectionViewTransitionLayout ();
```

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

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIDocumentMenuViewController ();
```

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

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIDocumentPickerViewController ();
```

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: MonoTouch.UIKit.UIFontDescriptor

Added interface:

<pre style='color: green'>
	MonoTouch.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoTouch.UIKit.UIImage

Added property:

<pre style='color: green'>
	public virtual bool FlipsForRightToLeftLayoutDirection { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual UIImage ImageFlippedForRightToLeftLayoutDirection ();
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

### Type Changed: MonoTouch.UIKit.UIKeyCommand

Added property:

<pre style='color: green'>
	public virtual string DiscoverabilityTitle { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public static UIKeyCommand Create (MonoTouch.Foundation.NSString keyCommandInput, UIKeyModifierFlags modifierFlags, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSString discoverabilityTitle);
</pre>

### Type Changed: MonoTouch.UIKit.UILabel

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added property:

<pre style='color: green'>
	public virtual bool AllowsDefaultTighteningForTruncation { get; set; }
</pre>

### Type Changed: MonoTouch.UIKit.UILabel.UILabelAppearance

Added constructor:

<pre style='color: green'>
	protected UILabel (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UIMutableUserNotificationAction

Added properties:

<pre style='color: green'>
	public virtual UIUserNotificationActionBehavior Behavior { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary Parameters { get; set; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
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

### Type Changed: MonoTouch.UIKit.UIProgressView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added property:

<pre style='color: green'>
	public virtual MonoTouch.Foundation.NSProgress ObservedProgress { get; set; }
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

### Type Changed: MonoTouch.UIKit.UIReturnKeyType

Added value:

<pre style='color: green'>
	Continue = 11,
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

### Type Changed: MonoTouch.UIKit.UIStoryboardPopoverSegue

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIStoryboardPopoverSegue ();
```

### Type Changed: MonoTouch.UIKit.UIStoryboardSegue

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIStoryboardSegue ();
```

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

Added interfaces:

<pre style='color: green'>
	MonoTouch.Foundation.INSCoding
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

Added property:

<pre style='color: green'>
	public virtual bool CellLayoutMarginsFollowReadableWidth { get; set; }
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

Added methods:

<pre style='color: green'>
	public virtual void BeginFloatingCursorAtPoint (System.Drawing.PointF point);
	public virtual void EndFloatingCursor ();
	public virtual UITextInputAssistantItem InputAssistantItem ();
	public virtual void UpdateFloatingCursorAtPoint (System.Drawing.PointF point);
</pre>

### Type Changed: MonoTouch.UIKit.UITextField.UITextFieldAppearance

Added constructor:

<pre style='color: green'>
	protected UITextField (IntPtr handle);
</pre>

### Type Changed: MonoTouch.UIKit.UITextInput_Extensions

Added methods:

<pre style='color: green'>
	public static void BeginFloatingCursorAtPoint (IUITextInput This, System.Drawing.PointF point);
	public static void EndFloatingCursor (IUITextInput This);
	public static UITextInputAssistantItem InputAssistantItem (IUITextInput This);
	public static void UpdateFloatingCursorAtPoint (IUITextInput This, System.Drawing.PointF point);
</pre>

### Type Changed: MonoTouch.UIKit.UITextView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void BeginFloatingCursorAtPoint (System.Drawing.PointF point);
	public virtual void EndFloatingCursor ();
	public virtual UITextInputAssistantItem InputAssistantItem ();
	public virtual void UpdateFloatingCursorAtPoint (System.Drawing.PointF point);
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

### Type Changed: MonoTouch.UIKit.UIUserNotificationAction

Added properties:

<pre style='color: green'>
	public virtual UIUserNotificationActionBehavior Behavior { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary Parameters { get; set; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
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

Added properties:

<pre style='color: green'>
	public virtual NSLayoutYAxisAnchor BottomAnchor { get; }
	public virtual NSLayoutXAxisAnchor CenterXAnchor { get; }
	public virtual NSLayoutYAxisAnchor CenterYAnchor { get; }
	public virtual NSLayoutYAxisAnchor FirstBaselineAnchor { get; }
	public virtual NSLayoutDimension HeightAnchor { get; }
	public static double InheritedAnimationDuration { get; }
	public virtual NSLayoutYAxisAnchor LastBaselineAnchor { get; }
	public virtual UILayoutGuide[] LayoutGuides { get; }
	public virtual UILayoutGuide LayoutMarginsGuide { get; }
	public virtual NSLayoutXAxisAnchor LeadingAnchor { get; }
	public virtual NSLayoutXAxisAnchor LeftAnchor { get; }
	public virtual UILayoutGuide ReadableContentGuide { get; }
	public virtual NSLayoutXAxisAnchor RightAnchor { get; }
	public virtual UISemanticContentAttribute SemanticContentAttribute { get; set; }
	public virtual NSLayoutYAxisAnchor TopAnchor { get; }
	public virtual NSLayoutXAxisAnchor TrailingAnchor { get; }
	public virtual UIView ViewForFirstBaselineLayout { get; }
	public virtual UIView ViewForLastBaselineLayout { get; }
	public virtual NSLayoutDimension WidthAnchor { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddLayoutGuide (UILayoutGuide guide);
	public static UIUserInterfaceLayoutDirection GetUserInterfaceLayoutDirection (UISemanticContentAttribute attribute);
	public virtual void RemoveLayoutGuide (UILayoutGuide guide);
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

### New Type MonoTouch.UIKit.NSDataAsset

<pre style='color: green'>
public class NSDataAsset : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public NSDataAsset (MonoTouch.Foundation.NSCoder coder);
	public NSDataAsset (MonoTouch.Foundation.NSObjectFlag t);
	public NSDataAsset (IntPtr handle);
	public NSDataAsset (string name);
	public NSDataAsset (string name, MonoTouch.Foundation.NSBundle bundle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSData Data { get; }
	public virtual string Name { get; }
	public virtual MonoTouch.Foundation.NSString TypeIdentifier { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.UIKit.NSLayoutAnchor

<pre style='color: green'>
public class NSLayoutAnchor : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public NSLayoutAnchor (MonoTouch.Foundation.NSCoder coder);
	public NSLayoutAnchor (MonoTouch.Foundation.NSObjectFlag t);
	public NSLayoutAnchor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutAnchor anchor);
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutAnchor anchor, float constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutAnchor anchor);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutAnchor anchor, float constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutAnchor anchor);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutAnchor anchor, float constant);
}
</pre>

### New Type MonoTouch.UIKit.NSLayoutDimension

<pre style='color: green'>
public class NSLayoutDimension : MonoTouch.UIKit.NSLayoutAnchor, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public NSLayoutDimension (MonoTouch.Foundation.NSCoder coder);
	public NSLayoutDimension (MonoTouch.Foundation.NSObjectFlag t);
	public NSLayoutDimension (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutDimension anchor, float multiplier);
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutDimension anchor, float multiplier, float constant);
	public virtual NSLayoutConstraint ConstraintEqualToConstant (float constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutDimension anchor, float multiplier, float constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutDimension anchor, float multiplier);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToConstant (float constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutDimension anchor, float multiplier);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutDimension anchor, float multiplier, float constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToConstant (float constant);
}
</pre>

### New Type MonoTouch.UIKit.NSLayoutXAxisAnchor

<pre style='color: green'>
public class NSLayoutXAxisAnchor : MonoTouch.UIKit.NSLayoutAnchor, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public NSLayoutXAxisAnchor (MonoTouch.Foundation.NSCoder coder);
	public NSLayoutXAxisAnchor (MonoTouch.Foundation.NSObjectFlag t);
	public NSLayoutXAxisAnchor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type MonoTouch.UIKit.NSLayoutYAxisAnchor

<pre style='color: green'>
public class NSLayoutYAxisAnchor : MonoTouch.UIKit.NSLayoutAnchor, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public NSLayoutYAxisAnchor (MonoTouch.Foundation.NSCoder coder);
	public NSLayoutYAxisAnchor (MonoTouch.Foundation.NSObjectFlag t);
	public NSLayoutYAxisAnchor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type MonoTouch.UIKit.NSWritingDirectionFormatType

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSWritingDirectionFormatType {
	Embedding = 1,
	Override = 2,
}
</pre>

### New Type MonoTouch.UIKit.UIApplicationOpenUrlOptionKeys

<pre style='color: green'>
public static class UIApplicationOpenUrlOptionKeys {
	// properties
	public static MonoTouch.Foundation.NSString AnnotationKey { get; }
	public static MonoTouch.Foundation.NSString OpenInPlaceKey { get; }
	public static MonoTouch.Foundation.NSString SourceApplicationKey { get; }
}
</pre>

### New Type MonoTouch.UIKit.UIApplicationOpenUrlOptions

<pre style='color: green'>
public class UIApplicationOpenUrlOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public UIApplicationOpenUrlOptions ();
	public UIApplicationOpenUrlOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public MonoTouch.Foundation.NSObject Annotation { get; set; }
	public bool? OpenInPlace { get; set; }
	public string SourceApplication { get; set; }
}
</pre>

### New Type MonoTouch.UIKit.UIBarButtonItemGroup

<pre style='color: green'>
public class UIBarButtonItemGroup : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIBarButtonItemGroup ();
	public UIBarButtonItemGroup (MonoTouch.Foundation.NSCoder coder);
	public UIBarButtonItemGroup (MonoTouch.Foundation.NSObjectFlag t);
	public UIBarButtonItemGroup (IntPtr handle);
	public UIBarButtonItemGroup (UIBarButtonItem[] barButtonItems, UIBarButtonItem representativeItem);
	// properties
	public virtual UIBarButtonItem[] BarButtonItems { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual bool DisplayingRepresentativeItem { get; }
	public virtual UIBarButtonItem RepresentativeItem { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.UIKit.UIInterfaceOrientationExtensions

<pre style='color: green'>
public static class UIInterfaceOrientationExtensions {
	// methods
	public static bool IsLandscape (UIInterfaceOrientation orientation);
	public static bool IsPortrait (UIInterfaceOrientation orientation);
}
</pre>

### New Type MonoTouch.UIKit.UILayoutGuide

<pre style='color: green'>
public class UILayoutGuide : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UILayoutGuide ();
	public UILayoutGuide (MonoTouch.Foundation.NSCoder coder);
	public UILayoutGuide (MonoTouch.Foundation.NSObjectFlag t);
	public UILayoutGuide (IntPtr handle);
	// properties
	public virtual NSLayoutYAxisAnchor BottomAnchor { get; }
	public virtual NSLayoutXAxisAnchor CenterXAnchor { get; }
	public virtual NSLayoutYAxisAnchor CenterYAnchor { get; }
	public override IntPtr ClassHandle { get; }
	public virtual NSLayoutDimension HeightAnchor { get; }
	public virtual string Identifier { get; set; }
	public virtual System.Drawing.RectangleF LayoutFrame { get; }
	public virtual NSLayoutXAxisAnchor LeadingAnchor { get; }
	public virtual NSLayoutXAxisAnchor LeftAnchor { get; }
	public virtual UIView OwningView { get; set; }
	public virtual NSLayoutXAxisAnchor RightAnchor { get; }
	public virtual NSLayoutYAxisAnchor TopAnchor { get; }
	public virtual NSLayoutXAxisAnchor TrailingAnchor { get; }
	public virtual NSLayoutDimension WidthAnchor { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.UIKit.UIPrinterCutterBehavior

<pre style='color: green'>
[Serializable]
public enum UIPrinterCutterBehavior {
	CutAfterEachCopy = 3,
	CutAfterEachJob = 4,
	CutAfterEachPage = 2,
	NoCut = 0,
	PrinterDefault = 1,
}
</pre>

### New Type MonoTouch.UIKit.UIRegion

<pre style='color: green'>
public class UIRegion : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIRegion ();
	public UIRegion (MonoTouch.Foundation.NSCoder coder);
	public UIRegion (MonoTouch.Foundation.NSObjectFlag t);
	public UIRegion (IntPtr handle);
	public UIRegion (float radius);
	public UIRegion (System.Drawing.SizeF size);
	// properties
	public override IntPtr ClassHandle { get; }
	public static UIRegion InfiniteRegion { get; }
	// methods
	public virtual bool ContainsPoint (System.Drawing.PointF point);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual UIRegion InverseRegion ();
	public virtual UIRegion RegionByDifferenceFromRegion (UIRegion region);
	public virtual MonoTouch.Foundation.NSObject RegionByIntersectionWithRegion (UIRegion region);
	public virtual UIRegion RegionByUnionWithRegion (UIRegion region);
}
</pre>

### New Type MonoTouch.UIKit.UISemanticContentAttribute

<pre style='color: green'>
[Serializable]
public enum UISemanticContentAttribute {
	ForceLeftToRight = 3,
	ForceRightToLeft = 4,
	Playback = 1,
	Spatial = 2,
	Unspecified = 0,
}
</pre>

### New Type MonoTouch.UIKit.UIStackView

<pre style='color: green'>
public class UIStackView : MonoTouch.UIKit.UIView, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, IUIAccessibilityIdentification, IUIAppearance, IUIAppearanceContainer, IUICoordinateSpace, IUIDynamicItem, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIStackView ();
	public UIStackView (MonoTouch.Foundation.NSCoder coder);
	public UIStackView (MonoTouch.Foundation.NSObjectFlag t);
	public UIStackView (IntPtr handle);
	public UIStackView (UIView[] views);
	// properties
	public virtual UIStackViewAlignment Alignment { get; set; }
	public static UIStackView.UIStackViewAppearance Appearance { get; }
	public virtual UIView ArrangedSubviews { get; }
	public virtual UILayoutConstraintAxis Axis { get; set; }
	public virtual bool BaselineRelativeArrangement { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual UIStackViewDistribution Distribution { get; set; }
	public virtual bool LayoutMarginsRelativeArrangement { get; set; }
	public virtual float Spacing { get; set; }
	// methods
	public virtual void AddArrangedSubview (UIView view);
	public static UIStackView.UIStackViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static UIStackView.UIStackViewAppearance GetAppearance&lt;T&gt; (UITraitCollection traits);
	public static UIStackView.UIStackViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIStackView.UIStackViewAppearance GetAppearance (UITraitCollection traits);
	public static UIStackView.UIStackViewAppearance GetAppearance&lt;T&gt; ();
	public static UIStackView.UIStackViewAppearance GetAppearance&lt;T&gt; (UITraitCollection traits, System.Type[] containers);
	public virtual void InsertArrangedSubview (UIView view, uint stackIndex);
	public virtual void RemoveArrangedSubview (UIView view);

	// inner types
	public class UIStackViewAppearance : MonoTouch.UIKit.UIView+UIViewAppearance, IUIAppearance, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
		// constructors
		protected UIStackView (IntPtr handle);
	}
}
</pre>

### New Type MonoTouch.UIKit.UIStackViewAlignment

<pre style='color: green'>
[Serializable]
public enum UIStackViewAlignment {
	Bottom = 4,
	Center = 3,
	Fill = 0,
	FirstBaseline = 2,
	LastBaseline = 5,
	Leading = 1,
	Top = 1,
	Trailing = 4,
}
</pre>

### New Type MonoTouch.UIKit.UIStackViewDistribution

<pre style='color: green'>
[Serializable]
public enum UIStackViewDistribution {
	EqualCentering = 4,
	EqualSpacing = 3,
	Fill = 0,
	FillEqually = 1,
	FillProportionally = 2,
}
</pre>

### New Type MonoTouch.UIKit.UIStoryboardUnwindSegueSource

<pre style='color: green'>
public class UIStoryboardUnwindSegueSource : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIStoryboardUnwindSegueSource (MonoTouch.Foundation.NSCoder coder);
	public UIStoryboardUnwindSegueSource (MonoTouch.Foundation.NSObjectFlag t);
	public UIStoryboardUnwindSegueSource (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSObject Sender { get; }
	public virtual UIViewController SourceViewController { get; }
	public virtual MonoTouch.ObjCRuntime.Selector UnwindAction { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.UIKit.UITextInputAssistantItem

<pre style='color: green'>
public class UITextInputAssistantItem : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UITextInputAssistantItem ();
	public UITextInputAssistantItem (MonoTouch.Foundation.NSCoder coder);
	public UITextInputAssistantItem (MonoTouch.Foundation.NSObjectFlag t);
	public UITextInputAssistantItem (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual UIBarButtonItemGroup[] LeadingBarButtonGroups { get; set; }
	public virtual UIBarButtonItemGroup[] TrailingBarButtonGroups { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.UIKit.UIUserNotificationActionBehavior

<pre style='color: green'>
[Serializable]
public enum UIUserNotificationActionBehavior {
	Default = 0,
	TextInput = 1,
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

Added property:

<pre style='color: green'>
	public virtual string CustomUserAgent { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual WKNavigation LoadData (MonoTouch.Foundation.NSData data, string MIMEType, string characterEncodingName, MonoTouch.Foundation.NSUrl baseUrl);
	public virtual WKNavigation LoadFileUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSUrl readAccessUrl);
</pre>

### Type Changed: MonoTouch.WebKit.WKWebView.WKWebViewAppearance

Added constructor:

<pre style='color: green'>
	protected WKWebView (IntPtr handle);
</pre>

### Type Changed: MonoTouch.WebKit.WKWebViewConfiguration

Added properties:

<pre style='color: green'>
	public virtual string ApplicationNameForUserAgent { get; set; }
	public virtual WKWebsiteDataStore WebsiteDataStore { get; set; }
</pre>

### New Type MonoTouch.WebKit.WKWebsiteDataRecord

<pre style='color: green'>
public class WKWebsiteDataRecord : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKWebsiteDataRecord ();
	public WKWebsiteDataRecord (MonoTouch.Foundation.NSCoder coder);
	public WKWebsiteDataRecord (MonoTouch.Foundation.NSObjectFlag t);
	public WKWebsiteDataRecord (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSSet DataTypes { get; }
	public virtual string DisplayName { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.WebKit.WKWebsiteDataStore

<pre style='color: green'>
public class WKWebsiteDataStore : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKWebsiteDataStore ();
	public WKWebsiteDataStore (MonoTouch.Foundation.NSCoder coder);
	public WKWebsiteDataStore (MonoTouch.Foundation.NSObjectFlag t);
	public WKWebsiteDataStore (IntPtr handle);
	// properties
	public static MonoTouch.Foundation.NSSet AllWebsiteDataTypes { get; }
	public override IntPtr ClassHandle { get; }
	public static WKWebsiteDataStore DefaultDataStore { get; }
	public static WKWebsiteDataStore NonPersistentDataStore { get; }
	public virtual bool Persistent { get; }
	// methods
	public virtual void FetchDataRecordsOfTypes (MonoTouch.Foundation.NSSet dataTypes, System.Action&lt;MonoTouch.Foundation.NSArray&gt; completionHandler);
	public virtual void RemoveDataOfTypes (MonoTouch.Foundation.NSSet dataTypes, WKWebsiteDataRecord[] dataRecords, System.Action completionHandler);
	public virtual void RemoveDataOfTypes (MonoTouch.Foundation.NSSet websiteDataTypes, MonoTouch.Foundation.NSDate date, System.Action completionHandler);
}
</pre>

### New Type MonoTouch.WebKit.WKWebsiteDataType

<pre style='color: green'>
public static class WKWebsiteDataType {
	// properties
	public static MonoTouch.Foundation.NSString Cookies { get; }
	public static MonoTouch.Foundation.NSString DiskCache { get; }
	public static MonoTouch.Foundation.NSString IndexedDBDatabases { get; }
	public static MonoTouch.Foundation.NSString LocalStorage { get; }
	public static MonoTouch.Foundation.NSString MemoryCache { get; }
	public static MonoTouch.Foundation.NSString OfflineWebApplicationCache { get; }
	public static MonoTouch.Foundation.NSString WebSQLDatabases { get; }
}
</pre>

## Namespace OpenTK

### New Type OpenTK.Vector2i

<pre style='color: green'>
[Serializable]
public struct Vector2i, System.IEquatable&lt;Vector2i&gt; {
	// constructors
	public Vector2i (int x, int y);
	// fields
	public static Vector2i One;
	public static int SizeInBytes;
	public static Vector2i UnitX;
	public static Vector2i UnitY;
	public int X;
	public int Y;
	public static Vector2i Zero;
	// methods
	public static Vector2i Add (Vector2i a, Vector2i b);
	public static void Add (ref Vector2i a, ref Vector2i b, out Vector2i result);
	public static Vector2i Clamp (Vector2i vec, Vector2i min, Vector2i max);
	public static void Clamp (ref Vector2i vec, ref Vector2i min, ref Vector2i max, out Vector2i result);
	public override bool Equals (object obj);
	public virtual bool Equals (Vector2i other);
	public override int GetHashCode ();
	public static Vector2i op_Addition (Vector2i left, Vector2i right);
	public static bool op_Equality (Vector2i left, Vector2i right);
	public static bool op_Inequality (Vector2i left, Vector2i right);
	public static Vector2i op_Subtraction (Vector2i left, Vector2i right);
	public static Vector2i op_UnaryNegation (Vector2i vec);
	public static void Subtract (ref Vector2i a, ref Vector2i b, out Vector2i result);
	public static Vector2i Subtract (Vector2i a, Vector2i b);
	public override string ToString ();
}
</pre>

### New Type OpenTK.Vector3i

<pre style='color: green'>
[Serializable]
public struct Vector3i, System.IEquatable&lt;Vector3i&gt; {
	// constructors
	public Vector3i (int x, int y, int z);
	public Vector3i (Vector2i v);
	public Vector3i (Vector3i v);
	// fields
	public static Vector3i One;
	public static int SizeInBytes;
	public static Vector3i UnitX;
	public static Vector3i UnitY;
	public static Vector3i UnitZ;
	public int X;
	public int Y;
	public int Z;
	public static Vector3i Zero;
	// properties
	public Vector2i Xy { get; set; }
	// methods
	public static Vector3i Add (Vector3i a, Vector3i b);
	public static void Add (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public static void Clamp (ref Vector3i vec, ref Vector3i min, ref Vector3i max, out Vector3i result);
	public static Vector3i Clamp (Vector3i vec, Vector3i min, Vector3i max);
	public static Vector3i ComponentMax (Vector3i a, Vector3i b);
	public static void ComponentMax (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public static Vector3i ComponentMin (Vector3i a, Vector3i b);
	public static void ComponentMin (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public override bool Equals (object obj);
	public virtual bool Equals (Vector3i other);
	public override int GetHashCode ();
	public static Vector3i op_Addition (Vector3i left, Vector3i right);
	public static bool op_Equality (Vector3i left, Vector3i right);
	public static bool op_Inequality (Vector3i left, Vector3i right);
	public static Vector3i op_Subtraction (Vector3i left, Vector3i right);
	public static Vector3i op_UnaryNegation (Vector3i vec);
	public static Vector3i Subtract (Vector3i a, Vector3i b);
	public static void Subtract (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public override string ToString ();
}
</pre>

## New Namespace MonoTouch.Contacts

### New Type MonoTouch.Contacts.CNAuthorizationStatus

<pre style='color: green'>
[Serializable]
public enum CNAuthorizationStatus {
	Authorized = 3,
	Denied = 2,
	NotDetermined = 0,
	Restricted = 1,
}
</pre>

### New Type MonoTouch.Contacts.CNContact

<pre style='color: green'>
public class CNContact : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContact ();
	public CNContact (MonoTouch.Foundation.NSCoder coder);
	public CNContact (MonoTouch.Foundation.NSObjectFlag t);
	public CNContact (IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSDateComponents Birthday { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSObject[] ContactRelations { get; }
	public virtual CNContactType ContactType { get; }
	public virtual MonoTouch.Foundation.NSObject[] Dates { get; }
	public virtual string DepartmentName { get; }
	public virtual MonoTouch.Foundation.NSObject[] EmailAddresses { get; }
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	public virtual string FamilyName { get; }
	public virtual string GivenName { get; }
	public virtual string Identifier { get; }
	public virtual MonoTouch.Foundation.NSData ImageData { get; }
	public virtual bool ImageDataAvailable { get; }
	public virtual MonoTouch.Foundation.NSObject[] InstantMessageAddresses { get; }
	public virtual string JobTitle { get; }
	public virtual string MiddleName { get; }
	public virtual string NamePrefix { get; }
	public virtual string NameSuffix { get; }
	public virtual string Nickname { get; }
	public virtual MonoTouch.Foundation.NSDateComponents NonGregorianBirthday { get; }
	public virtual string Note { get; }
	public virtual string OrganizationName { get; }
	public virtual MonoTouch.Foundation.NSObject[] PhoneNumbers { get; }
	public virtual string PhoneticFamilyName { get; }
	public virtual string PhoneticGivenName { get; }
	public virtual string PhoneticMiddleName { get; }
	public virtual MonoTouch.Foundation.NSObject[] PostalAddresses { get; }
	public virtual string PreviousFamilyName { get; }
	public static MonoTouch.Foundation.NSString PropertyNotFetchedExceptionName { get; }
	public virtual MonoTouch.Foundation.NSObject[] SocialProfiles { get; }
	public virtual MonoTouch.Foundation.NSData ThumbnailImageData { get; }
	public virtual MonoTouch.Foundation.NSObject[] UrlAddresses { get; }
	// methods
	public virtual bool AreKeysAvailable (ICNKeyDescriptor[] keyDescriptors);
	public static System.Func&lt;MonoTouch.Foundation.NSObject,MonoTouch.Foundation.NSObject,MonoTouch.Foundation.NSComparisonResult&gt; ComparatorForName (CNContactSortOrder sortOrder);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static ICNKeyDescriptor DescriptorForAllComparatorKeys ();
	protected override void Dispose (bool disposing);
	public virtual bool IsKeyAvailable (MonoTouch.Foundation.NSString contactKey);
	public virtual bool IsKeyAvailable (CNContactOption contactOption);
	public static string LocalizeProperty (CNContactOption contactOption);
	public static string LocalizeProperty (MonoTouch.Foundation.NSString contactKey);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
}
</pre>

### New Type MonoTouch.Contacts.CNContact_PredicatesExtension

<pre style='color: green'>
public static class CNContact_PredicatesExtension {
	// methods
	public static MonoTouch.Foundation.NSPredicate GetPredicateForContacts (CNContact This, string matchingName);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForContacts (CNContact This, string[] identifiers);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForContactsInContainer (CNContact This, string containerIdentifier);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForContactsInGroup (CNContact This, string groupIdentifier);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForContactsLinked (CNContact This, CNContact contact);
}
</pre>

### New Type MonoTouch.Contacts.CNContactDisplayNameOrder

<pre style='color: green'>
[Serializable]
public enum CNContactDisplayNameOrder {
	FamilyNameFirst = 2,
	GivenNameFirst = 1,
	UserDefault = 0,
}
</pre>

### New Type MonoTouch.Contacts.CNContactFetchRequest

<pre style='color: green'>
public class CNContactFetchRequest : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactFetchRequest (MonoTouch.Foundation.NSCoder coder);
	public CNContactFetchRequest (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactFetchRequest (IntPtr handle);
	public CNContactFetchRequest (ICNKeyDescriptor[] keysToFetch);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual ICNKeyDescriptor[] KeysToFetch { get; set; }
	public virtual bool MutableObjects { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate Predicate { get; set; }
	public virtual CNContactSortOrder SortOrder { get; set; }
	public virtual bool UnifyResults { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.Contacts.CNContactFormatter

<pre style='color: green'>
public class CNContactFormatter : MonoTouch.Foundation.NSFormatter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactFormatter ();
	public CNContactFormatter (MonoTouch.Foundation.NSCoder coder);
	public CNContactFormatter (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactFormatter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString ContactPropertyAttribute { get; }
	public virtual CNContactFormatterStyle Style { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSAttributedString GetAttributedString (CNContact contact, MonoTouch.Foundation.NSDictionary attributes);
	public static MonoTouch.Foundation.NSAttributedString GetAttributedStringFrom (CNContact contact, CNContactFormatterStyle style, MonoTouch.Foundation.NSDictionary attributes);
	public static string GetDelimiterFor (CNContact contact);
	public static ICNKeyDescriptor GetDescriptorForRequiredKeys (CNContactFormatterStyle style);
	public static CNContactDisplayNameOrder GetNameOrderFor (CNContact contact);
	public virtual string GetString (CNContact contact);
	public static string GetStringFrom (CNContact contact, CNContactFormatterStyle style);
}
</pre>

### New Type MonoTouch.Contacts.CNContactFormatterStyle

<pre style='color: green'>
[Serializable]
public enum CNContactFormatterStyle {
	FullName = 0,
	PhoneticFullName = 1,
}
</pre>

### New Type MonoTouch.Contacts.CNContactKey

<pre style='color: green'>
public static class CNContactKey {
	// properties
	public static MonoTouch.Foundation.NSString Birthday { get; }
	public static MonoTouch.Foundation.NSString Dates { get; }
	public static MonoTouch.Foundation.NSString DepartmentName { get; }
	public static MonoTouch.Foundation.NSString EmailAddresses { get; }
	public static MonoTouch.Foundation.NSString FamilyName { get; }
	public static MonoTouch.Foundation.NSString GivenName { get; }
	public static MonoTouch.Foundation.NSString Identifier { get; }
	public static MonoTouch.Foundation.NSString ImageData { get; }
	public static MonoTouch.Foundation.NSString ImageDataAvailable { get; }
	public static MonoTouch.Foundation.NSString InstantMessageAddresses { get; }
	public static MonoTouch.Foundation.NSString JobTitle { get; }
	public static MonoTouch.Foundation.NSString MiddleName { get; }
	public static MonoTouch.Foundation.NSString NamePrefix { get; }
	public static MonoTouch.Foundation.NSString NameSuffix { get; }
	public static MonoTouch.Foundation.NSString Nickname { get; }
	public static MonoTouch.Foundation.NSString NonGregorianBirthday { get; }
	public static MonoTouch.Foundation.NSString Note { get; }
	public static MonoTouch.Foundation.NSString OrganizationName { get; }
	public static MonoTouch.Foundation.NSString PhoneNumbers { get; }
	public static MonoTouch.Foundation.NSString PhoneticFamilyName { get; }
	public static MonoTouch.Foundation.NSString PhoneticGivenName { get; }
	public static MonoTouch.Foundation.NSString PhoneticMiddleName { get; }
	public static MonoTouch.Foundation.NSString PostalAddresses { get; }
	public static MonoTouch.Foundation.NSString PreviousFamilyName { get; }
	public static MonoTouch.Foundation.NSString Relations { get; }
	public static MonoTouch.Foundation.NSString SocialProfiles { get; }
	public static MonoTouch.Foundation.NSString ThumbnailImageData { get; }
	public static MonoTouch.Foundation.NSString Type { get; }
	public static MonoTouch.Foundation.NSString UrlAddresses { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNContactOption

<pre style='color: green'>
[Serializable]
public enum CNContactOption {
	Birthday = 7,
	Dates = 17,
	DepartmentName = 5,
	EmailAddresses = 15,
	ImageData = 10,
	ImageDataAvailable = 12,
	InstantMessageAddresses = 21,
	JobTitle = 6,
	Nickname = 0,
	NonGregorianBirthday = 8,
	Note = 9,
	OrganizationName = 4,
	PhoneNumbers = 14,
	PhoneticFamilyName = 3,
	PhoneticGivenName = 1,
	PhoneticMiddleName = 2,
	PostalAddresses = 16,
	Relations = 19,
	SocialProfiles = 20,
	ThumbnailImageData = 11,
	Type = 13,
	UrlAddresses = 18,
}
</pre>

### New Type MonoTouch.Contacts.CNContactProperty

<pre style='color: green'>
public class CNContactProperty : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactProperty ();
	public CNContactProperty (MonoTouch.Foundation.NSCoder coder);
	public CNContactProperty (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactProperty (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CNContact Contact { get; }
	public virtual string Identifier { get; }
	public virtual string Key { get; }
	public virtual string Label { get; }
	public virtual MonoTouch.Foundation.NSObject Value { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.Contacts.CNContactRelation

<pre style='color: green'>
public class CNContactRelation : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactRelation ();
	public CNContactRelation (MonoTouch.Foundation.NSCoder coder);
	public CNContactRelation (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactRelation (IntPtr handle);
	public CNContactRelation (string name);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static CNContactRelation FromName (string name);
}
</pre>

### New Type MonoTouch.Contacts.CNContactSortOrder

<pre style='color: green'>
[Serializable]
public enum CNContactSortOrder {
	FamilyName = 3,
	GivenName = 2,
	None = 0,
	UserDefault = 1,
}
</pre>

### New Type MonoTouch.Contacts.CNContactStore

<pre style='color: green'>
public class CNContactStore : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactStore ();
	public CNContactStore (MonoTouch.Foundation.NSCoder coder);
	public CNContactStore (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactStore (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string DefaultContainerIdentifier { get; }
	public static MonoTouch.Foundation.NSString NotificationDidChange { get; }
	// methods
	public virtual bool EnumerateContacts (CNContactFetchRequest fetchRequest, out MonoTouch.Foundation.NSError error, CNContactStoreEnumerateContactsHandler handler);
	public virtual bool ExecuteSaveRequest (CNSaveRequest saveRequest, out MonoTouch.Foundation.NSError error);
	public static CNAuthorizationStatus GetAuthorizationStatus (CNEntityType entityType);
	public virtual CNContainer[] GetContainers (MonoTouch.Foundation.NSPredicate predicate, out MonoTouch.Foundation.NSError error);
	public virtual CNGroup[] GetGroups (MonoTouch.Foundation.NSPredicate predicate, out MonoTouch.Foundation.NSError error);
	public virtual CNContact GetUnifiedContact (string identifier, ICNKeyDescriptor[] keys, out MonoTouch.Foundation.NSError error);
	public virtual CNContact[] GetUnifiedContacts (MonoTouch.Foundation.NSPredicate predicate, ICNKeyDescriptor[] keys, out MonoTouch.Foundation.NSError error);
	public virtual MonoTouch.Foundation.NSObject GetUnifiedMeContact (ICNKeyDescriptor[] keys, out MonoTouch.Foundation.NSError error);
	public virtual void RequestAccess (CNEntityType entityType, CNContactStoreRequestAccessHandler completionHandler);
	public virtual System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (CNEntityType entityType);

	// inner types
	public static class Notifications {
		// methods
		public static MonoTouch.Foundation.NSObject ObserveNotificationDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type MonoTouch.Contacts.CNContactStoreEnumerateContactsHandler

<pre style='color: green'>
public sealed delegate CNContactStoreEnumerateContactsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CNContactStoreEnumerateContactsHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CNContact contact, bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CNContact contact, bool stop);
}
</pre>

### New Type MonoTouch.Contacts.CNContactStoreRequestAccessHandler

<pre style='color: green'>
public sealed delegate CNContactStoreRequestAccessHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CNContactStoreRequestAccessHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool granted, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool granted, MonoTouch.Foundation.NSError error);
}
</pre>

### New Type MonoTouch.Contacts.CNContactsUserDefaults

<pre style='color: green'>
public class CNContactsUserDefaults : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactsUserDefaults ();
	public CNContactsUserDefaults (MonoTouch.Foundation.NSCoder coder);
	public CNContactsUserDefaults (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactsUserDefaults (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string CountryCode { get; }
	public virtual CNContactSortOrder SortOrder { get; }
	// methods
	public static CNContactsUserDefaults GetSharedDefaults ();
}
</pre>

### New Type MonoTouch.Contacts.CNContactType

<pre style='color: green'>
[Serializable]
public enum CNContactType {
	Organization = 1,
	Person = 0,
}
</pre>

### New Type MonoTouch.Contacts.CNContactVCardSerialization

<pre style='color: green'>
public class CNContactVCardSerialization : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactVCardSerialization ();
	public CNContactVCardSerialization (MonoTouch.Foundation.NSCoder coder);
	public CNContactVCardSerialization (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactVCardSerialization (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public static ICNKeyDescriptor DescriptorFromRequiredKeys ();
	public static CNContact[] GetContactsFromData (MonoTouch.Foundation.NSData data, out MonoTouch.Foundation.NSError error);
	public static MonoTouch.Foundation.NSData GetDataFromContacts (CNContact[] contacts, out MonoTouch.Foundation.NSError error);
}
</pre>

### New Type MonoTouch.Contacts.CNContainer

<pre style='color: green'>
public class CNContainer : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContainer ();
	public CNContainer (MonoTouch.Foundation.NSCoder coder);
	public CNContainer (MonoTouch.Foundation.NSObjectFlag t);
	public CNContainer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual string Name { get; }
	public virtual CNContainerType Type { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
</pre>

### New Type MonoTouch.Contacts.CNContainer_PredicatesExtension

<pre style='color: green'>
public static class CNContainer_PredicatesExtension {
	// methods
	public static MonoTouch.Foundation.NSPredicate GetPredicateForContainerOfContact (CNContainer This, string contactIdentifier);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForContainerOfGroup (CNContainer This, string groupIdentifier);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForContainers (CNContainer This, string[] identifiers);
}
</pre>

### New Type MonoTouch.Contacts.CNContainerKey

<pre style='color: green'>
public static class CNContainerKey {
	// properties
	public static MonoTouch.Foundation.NSString Identifier { get; }
	public static MonoTouch.Foundation.NSString Name { get; }
	public static MonoTouch.Foundation.NSString Type { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNContainerType

<pre style='color: green'>
[Serializable]
public enum CNContainerType {
	CardDav = 3,
	Exchange = 2,
	Local = 1,
	Unassigned = 0,
}
</pre>

### New Type MonoTouch.Contacts.CNEntityType

<pre style='color: green'>
[Serializable]
public enum CNEntityType {
	Contacts = 0,
}
</pre>

### New Type MonoTouch.Contacts.CNErrorCode

<pre style='color: green'>
[Serializable]
public enum CNErrorCode {
	AuthorizationDenied = 100,
	CommunicationError = 1,
	ContainmentCycle = 202,
	ContainmentScope = 203,
	DataAccessError = 2,
	InsertedRecordAlreadyExists = 201,
	ParentRecordDoesNotExist = 204,
	PolicyViolation = 500,
	PredicateInvalid = 400,
	RecordDoesNotExist = 200,
	ValidationConfigurationError = 302,
	ValidationMultipleErrors = 300,
	ValidationTypeMismatch = 301,
}
</pre>

### New Type MonoTouch.Contacts.CNErrorUserInfoKey

<pre style='color: green'>
public static class CNErrorUserInfoKey {
	// properties
	public static MonoTouch.Foundation.NSString AffectedRecordIdentifiers { get; }
	public static MonoTouch.Foundation.NSString AffectedRecords { get; }
	public static MonoTouch.Foundation.NSString KeyPaths { get; }
	public static MonoTouch.Foundation.NSString ValidationErrors { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNGroup

<pre style='color: green'>
public class CNGroup : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNGroup ();
	public CNGroup (MonoTouch.Foundation.NSCoder coder);
	public CNGroup (MonoTouch.Foundation.NSObjectFlag t);
	public CNGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual string Name { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
}
</pre>

### New Type MonoTouch.Contacts.CNGroup_PredicatesExtension

<pre style='color: green'>
public static class CNGroup_PredicatesExtension {
	// methods
	public static MonoTouch.Foundation.NSPredicate GetPredicateForGroups (CNGroup This, string[] identifiers);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForGroupsInContainer (CNGroup This, string containerIdentifier);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForSubgroupsInGroup (CNGroup This, string parentGroupIdentifier);
}
</pre>

### New Type MonoTouch.Contacts.CNGroupKey

<pre style='color: green'>
public static class CNGroupKey {
	// properties
	public static MonoTouch.Foundation.NSString Identifier { get; }
	public static MonoTouch.Foundation.NSString Name { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNInstantMessageAddress

<pre style='color: green'>
public class CNInstantMessageAddress : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNInstantMessageAddress ();
	public CNInstantMessageAddress (MonoTouch.Foundation.NSCoder coder);
	public CNInstantMessageAddress (MonoTouch.Foundation.NSObjectFlag t);
	public CNInstantMessageAddress (IntPtr handle);
	public CNInstantMessageAddress (string username, string service);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Service { get; }
	public virtual string Username { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static string LocalizeProperty (CNInstantMessageAddressOption property);
	public static string LocalizeProperty (MonoTouch.Foundation.NSString propertyKey);
	public static string LocalizeService (CNInstantMessageServiceOption serviceOption);
	public static string LocalizeService (MonoTouch.Foundation.NSString service);
}
</pre>

### New Type MonoTouch.Contacts.CNInstantMessageAddressKey

<pre style='color: green'>
public static class CNInstantMessageAddressKey {
	// properties
	public static MonoTouch.Foundation.NSString Service { get; }
	public static MonoTouch.Foundation.NSString Username { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNInstantMessageAddressOption

<pre style='color: green'>
[Serializable]
public enum CNInstantMessageAddressOption {
	Service = 1,
	Username = 0,
}
</pre>

### New Type MonoTouch.Contacts.CNInstantMessageServiceKey

<pre style='color: green'>
public static class CNInstantMessageServiceKey {
	// properties
	public static MonoTouch.Foundation.NSString Aim { get; }
	public static MonoTouch.Foundation.NSString Facebook { get; }
	public static MonoTouch.Foundation.NSString GaduGadu { get; }
	public static MonoTouch.Foundation.NSString GoogleTalk { get; }
	public static MonoTouch.Foundation.NSString Icq { get; }
	public static MonoTouch.Foundation.NSString Jabber { get; }
	public static MonoTouch.Foundation.NSString Msn { get; }
	public static MonoTouch.Foundation.NSString QQ { get; }
	public static MonoTouch.Foundation.NSString Skype { get; }
	public static MonoTouch.Foundation.NSString Yahoo { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNInstantMessageServiceOption

<pre style='color: green'>
[Serializable]
public enum CNInstantMessageServiceOption {
	Aim = 0,
	Facebook = 1,
	GaduGadu = 2,
	GoogleTalk = 3,
	Icq = 4,
	Jabber = 5,
	Msn = 6,
	QQ = 7,
	Skype = 8,
	Yahoo = 9,
}
</pre>

### New Type MonoTouch.Contacts.CNKeyDescriptor

<pre style='color: green'>
public class CNKeyDescriptor : MonoTouch.Foundation.NSObject, ICNKeyDescriptor, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNKeyDescriptor ();
	public CNKeyDescriptor (MonoTouch.Foundation.NSCoder coder);
	public CNKeyDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public CNKeyDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
</pre>

### New Type MonoTouch.Contacts.CNKeyDescriptor_Extensions

<pre style='color: green'>
public static class CNKeyDescriptor_Extensions {
}
</pre>

### New Type MonoTouch.Contacts.CNLabelContactRelationKey

<pre style='color: green'>
public static class CNLabelContactRelationKey {
	// properties
	public static MonoTouch.Foundation.NSString Assistant { get; }
	public static MonoTouch.Foundation.NSString Brother { get; }
	public static MonoTouch.Foundation.NSString Child { get; }
	public static MonoTouch.Foundation.NSString Father { get; }
	public static MonoTouch.Foundation.NSString Friend { get; }
	public static MonoTouch.Foundation.NSString Manager { get; }
	public static MonoTouch.Foundation.NSString Mother { get; }
	public static MonoTouch.Foundation.NSString Parent { get; }
	public static MonoTouch.Foundation.NSString Partner { get; }
	public static MonoTouch.Foundation.NSString Sister { get; }
	public static MonoTouch.Foundation.NSString Spouse { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNLabeledValue

<pre style='color: green'>
public class CNLabeledValue : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNLabeledValue ();
	public CNLabeledValue (MonoTouch.Foundation.NSCoder coder);
	public CNLabeledValue (MonoTouch.Foundation.NSObjectFlag t);
	public CNLabeledValue (IntPtr handle);
	public CNLabeledValue (string label, MonoTouch.Foundation.NSObject value);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual string Label { get; }
	public virtual MonoTouch.Foundation.NSObject Value { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public static CNLabeledValue FromLabel (string label, MonoTouch.Foundation.NSObject value);
	public virtual CNLabeledValue GetLabeledValue (string label);
	public virtual CNLabeledValue GetLabeledValue (MonoTouch.Foundation.NSObject value);
	public virtual CNLabeledValue GetLabeledValue (string label, MonoTouch.Foundation.NSObject value);
	public static string LocalizeLabel (MonoTouch.Foundation.NSString labelKey);
}
</pre>

### New Type MonoTouch.Contacts.CNLabelKey

<pre style='color: green'>
public static class CNLabelKey {
	// properties
	public static MonoTouch.Foundation.NSString DateAnniversary { get; }
	public static MonoTouch.Foundation.NSString EmailiCloud { get; }
	public static MonoTouch.Foundation.NSString Home { get; }
	public static MonoTouch.Foundation.NSString Other { get; }
	public static MonoTouch.Foundation.NSString UrlAddressHomePage { get; }
	public static MonoTouch.Foundation.NSString Work { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNLabelPhoneNumberKey

<pre style='color: green'>
public static class CNLabelPhoneNumberKey {
	// properties
	public static MonoTouch.Foundation.NSString HomeFax { get; }
	public static MonoTouch.Foundation.NSString iPhone { get; }
	public static MonoTouch.Foundation.NSString Main { get; }
	public static MonoTouch.Foundation.NSString Mobile { get; }
	public static MonoTouch.Foundation.NSString OtherFax { get; }
	public static MonoTouch.Foundation.NSString Pager { get; }
	public static MonoTouch.Foundation.NSString WorkFax { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNMutableContact

<pre style='color: green'>
public class CNMutableContact : MonoTouch.Contacts.CNContact, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNMutableContact ();
	public CNMutableContact (MonoTouch.Foundation.NSCoder coder);
	public CNMutableContact (MonoTouch.Foundation.NSObjectFlag t);
	public CNMutableContact (IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSDateComponents Birthday { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSObject[] ContactRelations { get; set; }
	public virtual CNContactType ContactType { get; set; }
	public virtual MonoTouch.Foundation.NSObject[] Dates { get; set; }
	public virtual string DepartmentName { get; set; }
	public virtual MonoTouch.Foundation.NSObject[] EmailAddresses { get; set; }
	public virtual string FamilyName { get; set; }
	public virtual string GivenName { get; set; }
	public virtual MonoTouch.Foundation.NSData ImageData { get; set; }
	public virtual MonoTouch.Foundation.NSObject[] InstantMessageAddresses { get; set; }
	public virtual string JobTitle { get; set; }
	public virtual string MiddleName { get; set; }
	public virtual string NamePrefix { get; set; }
	public virtual string NameSuffix { get; set; }
	public virtual string Nickname { get; set; }
	public virtual MonoTouch.Foundation.NSDateComponents NonGregorianBirthday { get; set; }
	public virtual string Note { get; set; }
	public virtual string OrganizationName { get; set; }
	public virtual MonoTouch.Foundation.NSObject[] PhoneNumbers { get; set; }
	public virtual string PhoneticFamilyName { get; set; }
	public virtual string PhoneticGivenName { get; set; }
	public virtual string PhoneticMiddleName { get; set; }
	public virtual MonoTouch.Foundation.NSObject[] PostalAddresses { get; set; }
	public virtual string PreviousFamilyName { get; set; }
	public virtual MonoTouch.Foundation.NSObject[] SocialProfiles { get; set; }
	public virtual MonoTouch.Foundation.NSObject[] UrlAddresses { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.Contacts.CNMutableGroup

<pre style='color: green'>
public class CNMutableGroup : MonoTouch.Contacts.CNGroup, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNMutableGroup ();
	public CNMutableGroup (MonoTouch.Foundation.NSCoder coder);
	public CNMutableGroup (MonoTouch.Foundation.NSObjectFlag t);
	public CNMutableGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
}
</pre>

### New Type MonoTouch.Contacts.CNMutablePostalAddress

<pre style='color: green'>
public class CNMutablePostalAddress : MonoTouch.Contacts.CNPostalAddress, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNMutablePostalAddress ();
	public CNMutablePostalAddress (MonoTouch.Foundation.NSCoder coder);
	public CNMutablePostalAddress (MonoTouch.Foundation.NSObjectFlag t);
	public CNMutablePostalAddress (IntPtr handle);
	// properties
	public virtual string City { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string Country { get; set; }
	public virtual string IsoCountryCode { get; set; }
	public virtual string PostalCode { get; set; }
	public virtual string State { get; set; }
	public virtual string Street { get; set; }
}
</pre>

### New Type MonoTouch.Contacts.CNPhoneNumber

<pre style='color: green'>
public class CNPhoneNumber : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNPhoneNumber (MonoTouch.Foundation.NSCoder coder);
	public CNPhoneNumber (MonoTouch.Foundation.NSObjectFlag t);
	public CNPhoneNumber (IntPtr handle);
	public CNPhoneNumber (string stringValue);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string StringValue { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static CNPhoneNumber PhoneNumberWithStringValue (string stringValue);
}
</pre>

### New Type MonoTouch.Contacts.CNPostalAddress

<pre style='color: green'>
public class CNPostalAddress : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNPostalAddress ();
	public CNPostalAddress (MonoTouch.Foundation.NSCoder coder);
	public CNPostalAddress (MonoTouch.Foundation.NSObjectFlag t);
	public CNPostalAddress (IntPtr handle);
	// properties
	public virtual string City { get; }
	public override IntPtr ClassHandle { get; }
	public virtual string Country { get; }
	public virtual string IsoCountryCode { get; }
	public virtual string PostalCode { get; }
	public virtual string State { get; }
	public virtual string Street { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static string LocalizeProperty (CNPostalAddressKeyOption option);
	public static string LocalizeProperty (MonoTouch.Foundation.NSString property);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
}
</pre>

### New Type MonoTouch.Contacts.CNPostalAddressFormatter

<pre style='color: green'>
public class CNPostalAddressFormatter : MonoTouch.Foundation.NSFormatter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNPostalAddressFormatter ();
	public CNPostalAddressFormatter (MonoTouch.Foundation.NSCoder coder);
	public CNPostalAddressFormatter (MonoTouch.Foundation.NSObjectFlag t);
	public CNPostalAddressFormatter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString LocalizedPropertyNameAttribute { get; }
	public static MonoTouch.Foundation.NSString PropertyAttribute { get; }
	// methods
	public static MonoTouch.Foundation.NSAttributedString GetAttributedStringFrom (CNPostalAddress postalAddress, MonoTouch.Foundation.NSDictionary attributes);
	public virtual MonoTouch.Foundation.NSAttributedString GetAttributedStringFromPostalAddress (CNPostalAddress postalAddress, MonoTouch.Foundation.NSDictionary attributes);
	public static string GetStringFrom (CNPostalAddress postalAddress);
	public virtual string GetStringFromPostalAddress (CNPostalAddress postalAddress);
}
</pre>

### New Type MonoTouch.Contacts.CNPostalAddressKey

<pre style='color: green'>
public static class CNPostalAddressKey {
	// properties
	public static MonoTouch.Foundation.NSString City { get; }
	public static MonoTouch.Foundation.NSString Country { get; }
	public static MonoTouch.Foundation.NSString IsoCountryCode { get; }
	public static MonoTouch.Foundation.NSString PostalCode { get; }
	public static MonoTouch.Foundation.NSString State { get; }
	public static MonoTouch.Foundation.NSString Street { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNPostalAddressKeyOption

<pre style='color: green'>
[Serializable]
public enum CNPostalAddressKeyOption {
	City = 1,
	Country = 4,
	IsoCountryCode = 5,
	PostalCode = 3,
	State = 2,
	Street = 0,
}
</pre>

### New Type MonoTouch.Contacts.CNSaveRequest

<pre style='color: green'>
public class CNSaveRequest : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNSaveRequest ();
	public CNSaveRequest (MonoTouch.Foundation.NSCoder coder);
	public CNSaveRequest (MonoTouch.Foundation.NSObjectFlag t);
	public CNSaveRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void AddContact (CNMutableContact contact, string identifier);
	public virtual void AddGroup (CNMutableGroup group, string identifier);
	public virtual void AddMember (CNContact contact, CNGroup group);
	public virtual void AddSubgroup (CNGroup subgroup, CNGroup group);
	public virtual void DeleteContact (CNMutableContact contact);
	public virtual void DeleteGroup (CNMutableGroup group);
	public virtual void RemoveMember (CNContact contact, CNGroup group);
	public virtual void RemoveSubgroup (CNGroup subgroup, CNGroup group);
	public virtual void UpdateContact (CNMutableContact contact);
	public virtual void UpdateGroup (CNMutableGroup group);
}
</pre>

### New Type MonoTouch.Contacts.CNSocialProfile

<pre style='color: green'>
public class CNSocialProfile : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNSocialProfile ();
	public CNSocialProfile (MonoTouch.Foundation.NSCoder coder);
	public CNSocialProfile (MonoTouch.Foundation.NSObjectFlag t);
	public CNSocialProfile (IntPtr handle);
	public CNSocialProfile (string url, string username, string userIdentifier, string service);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Service { get; }
	public virtual string UrlString { get; }
	public virtual string UserIdentifier { get; }
	public virtual string Username { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static string LocalizeProperty (CNSocialProfileOption option);
	public static string LocalizeProperty (MonoTouch.Foundation.NSString key);
	public static string LocalizeService (CNSocialProfileServiceOption serviceOption);
	public static string LocalizeService (MonoTouch.Foundation.NSString service);
}
</pre>

### New Type MonoTouch.Contacts.CNSocialProfileKey

<pre style='color: green'>
public static class CNSocialProfileKey {
	// properties
	public static MonoTouch.Foundation.NSString Service { get; }
	public static MonoTouch.Foundation.NSString UrlString { get; }
	public static MonoTouch.Foundation.NSString UserIdentifier { get; }
	public static MonoTouch.Foundation.NSString Username { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNSocialProfileOption

<pre style='color: green'>
[Serializable]
public enum CNSocialProfileOption {
	Service = 3,
	UrlString = 0,
	UserIdentifier = 2,
	Username = 1,
}
</pre>

### New Type MonoTouch.Contacts.CNSocialProfileServiceKey

<pre style='color: green'>
public static class CNSocialProfileServiceKey {
	// properties
	public static MonoTouch.Foundation.NSString Facebook { get; }
	public static MonoTouch.Foundation.NSString Flickr { get; }
	public static MonoTouch.Foundation.NSString GameCenter { get; }
	public static MonoTouch.Foundation.NSString LinkedIn { get; }
	public static MonoTouch.Foundation.NSString MySpace { get; }
	public static MonoTouch.Foundation.NSString SinaWeibo { get; }
	public static MonoTouch.Foundation.NSString TencentWeibo { get; }
	public static MonoTouch.Foundation.NSString Twitter { get; }
	public static MonoTouch.Foundation.NSString Yelp { get; }
}
</pre>

### New Type MonoTouch.Contacts.CNSocialProfileServiceOption

<pre style='color: green'>
[Serializable]
public enum CNSocialProfileServiceOption {
	Facebook = 0,
	Flickr = 1,
	GameCenter = 8,
	LinkedIn = 2,
	MySpace = 3,
	SinaWeibo = 4,
	TencentWeibo = 5,
	Twitter = 6,
	Yelp = 7,
}
</pre>

### New Type MonoTouch.Contacts.ICNKeyDescriptor

<pre style='color: green'>
public interface ICNKeyDescriptor : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding {
}
</pre>

## New Namespace MonoTouch.ContactsUI

### New Type MonoTouch.ContactsUI.CNContactPickerDelegate

<pre style='color: green'>
public class CNContactPickerDelegate : MonoTouch.Foundation.NSObject, ICNContactPickerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactPickerDelegate ();
	public CNContactPickerDelegate (MonoTouch.Foundation.NSCoder coder);
	public CNContactPickerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactPickerDelegate (IntPtr handle);
	// methods
	public virtual void ContactPickerDidCancel (CNContactPickerViewController picker);
	public virtual void DidSelectContact (CNContactPickerViewController picker, MonoTouch.Contacts.CNContact contact);
	public virtual void DidSelectContactProperties (CNContactPickerViewController picker, MonoTouch.Contacts.CNContactProperty[] contactProperties);
	public virtual void DidSelectContactProperty (CNContactPickerViewController picker, MonoTouch.Contacts.CNContactProperty contactProperty);
	public virtual void DidSelectContacts (CNContactPickerViewController picker, MonoTouch.Contacts.CNContact[] contacts);
}
</pre>

### New Type MonoTouch.ContactsUI.CNContactPickerDelegate_Extensions

<pre style='color: green'>
public static class CNContactPickerDelegate_Extensions {
	// methods
	public static void ContactPickerDidCancel (ICNContactPickerDelegate This, CNContactPickerViewController picker);
	public static void DidSelectContact (ICNContactPickerDelegate This, CNContactPickerViewController picker, MonoTouch.Contacts.CNContact contact);
	public static void DidSelectContactProperties (ICNContactPickerDelegate This, CNContactPickerViewController picker, MonoTouch.Contacts.CNContactProperty[] contactProperties);
	public static void DidSelectContactProperty (ICNContactPickerDelegate This, CNContactPickerViewController picker, MonoTouch.Contacts.CNContactProperty contactProperty);
	public static void DidSelectContacts (ICNContactPickerDelegate This, CNContactPickerViewController picker, MonoTouch.Contacts.CNContact[] contacts);
}
</pre>

### New Type MonoTouch.ContactsUI.CNContactPickerViewController

<pre style='color: green'>
public class CNContactPickerViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAppearanceContainer, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactPickerViewController ();
	public CNContactPickerViewController (MonoTouch.Foundation.NSCoder coder);
	public CNContactPickerViewController (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactPickerViewController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual ICNContactPickerDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSString[] DisplayedPropertyKeys { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate PredicateForEnablingContact { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate PredicateForSelectionOfContact { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate PredicateForSelectionOfProperty { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ContactsUI.CNContactViewController

<pre style='color: green'>
public class CNContactViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAppearanceContainer, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactViewController ();
	public CNContactViewController (MonoTouch.Foundation.NSCoder coder);
	public CNContactViewController (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactViewController (IntPtr handle);
	// properties
	public virtual bool AllowsActions { get; set; }
	public virtual bool AllowsEditing { get; set; }
	public virtual string AlternateName { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Contacts.CNContact Contact { get; }
	public virtual MonoTouch.Contacts.CNContactStore ContactStore { get; set; }
	public virtual ICNContactViewControllerDelegate Delegate { get; set; }
	public static MonoTouch.Contacts.ICNKeyDescriptor DescriptorForRequiredKeys { get; }
	public virtual MonoTouch.Foundation.NSString[] DisplayedPropertyKeys { get; set; }
	public virtual string Message { get; set; }
	public virtual MonoTouch.Contacts.CNGroup ParentGroup { get; set; }
	public virtual bool ShouldShowLinkedContacts { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static CNContactViewController FromContact (MonoTouch.Contacts.CNContact contact);
	public static CNContactViewController FromNewContact (MonoTouch.Contacts.CNContact contact);
	public static CNContactViewController FromUnknownContact (MonoTouch.Contacts.CNContact contact);
	public virtual void HighlightProperty (MonoTouch.Foundation.NSString key, string identifier);
}
</pre>

### New Type MonoTouch.ContactsUI.CNContactViewControllerDelegate

<pre style='color: green'>
public class CNContactViewControllerDelegate : MonoTouch.Foundation.NSObject, ICNContactViewControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CNContactViewControllerDelegate ();
	public CNContactViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public CNContactViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public CNContactViewControllerDelegate (IntPtr handle);
	// methods
	public virtual void DidSelectContact (CNContactPickerViewController picker, MonoTouch.Contacts.CNContact contact);
	public virtual bool ShouldPerformDefaultAction (CNContactViewController viewController, MonoTouch.Contacts.CNContactProperty property);
}
</pre>

### New Type MonoTouch.ContactsUI.CNContactViewControllerDelegate_Extensions

<pre style='color: green'>
public static class CNContactViewControllerDelegate_Extensions {
	// methods
	public static void DidSelectContact (ICNContactViewControllerDelegate This, CNContactPickerViewController picker, MonoTouch.Contacts.CNContact contact);
	public static bool ShouldPerformDefaultAction (ICNContactViewControllerDelegate This, CNContactViewController viewController, MonoTouch.Contacts.CNContactProperty property);
}
</pre>

### New Type MonoTouch.ContactsUI.ICNContactPickerDelegate

<pre style='color: green'>
public interface ICNContactPickerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.ContactsUI.ICNContactViewControllerDelegate

<pre style='color: green'>
public interface ICNContactViewControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

## New Namespace MonoTouch.CoreSpotlight

### New Type MonoTouch.CoreSpotlight.CSCustomAttributeKey

<pre style='color: green'>
public class CSCustomAttributeKey : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CSCustomAttributeKey ();
	public CSCustomAttributeKey (MonoTouch.Foundation.NSCoder coder);
	public CSCustomAttributeKey (MonoTouch.Foundation.NSObjectFlag t);
	public CSCustomAttributeKey (IntPtr handle);
	public CSCustomAttributeKey (string keyName);
	public CSCustomAttributeKey (string keyName, bool searchable, bool searchableByDefault, bool unique, bool multiValued);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string KeyName { get; }
	public virtual bool MultiValued { get; }
	public virtual bool Searchable { get; }
	public virtual bool SearchableByDefault { get; }
	public virtual bool Unique { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSExposureProgramKey

<pre style='color: green'>
public static class CSExposureProgramKey {
	// properties
	public static MonoTouch.Foundation.NSString Aperture { get; }
	public static MonoTouch.Foundation.NSString Manual { get; }
	public static MonoTouch.Foundation.NSString Normal { get; }
	public static MonoTouch.Foundation.NSString Priority { get; }
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSFileProtection

<pre style='color: green'>
[Serializable]
public enum CSFileProtection {
	Complete = 1,
	CompleteUnlessOpen = 2,
	CompleteUntilFirstUserAuthentication = 3,
	None = 0,
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSIndexErrorCode

<pre style='color: green'>
[Serializable]
public enum CSIndexErrorCode {
	IndexUnavailableError = -1000,
	InvalidClientStateError = -1002,
	InvalidItemError = -1001,
	QuotaExceeded = -1004,
	RemoteConnectionError = -1003,
	UnknownError = -1,
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSIndexExtensionRequestHandler

<pre style='color: green'>
public class CSIndexExtensionRequestHandler : MonoTouch.Foundation.NSObject, ICSSearchableIndexDelegate, MonoTouch.Foundation.INSExtensionRequestHandling, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CSIndexExtensionRequestHandler ();
	public CSIndexExtensionRequestHandler (MonoTouch.Foundation.NSCoder coder);
	public CSIndexExtensionRequestHandler (MonoTouch.Foundation.NSObjectFlag t);
	public CSIndexExtensionRequestHandler (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void BeginRequestWithExtensionContext (MonoTouch.Foundation.NSExtensionContext context);
	public virtual void ReindexAllSearchableItems (CSSearchableIndex searchableIndex, System.Action acknowledgementHandler);
	public virtual void ReindexSearchableItems (CSSearchableIndex searchableIndex, string[] identifiers, System.Action acknowledgementHandler);
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSLocalizedString

<pre style='color: green'>
public class CSLocalizedString : MonoTouch.Foundation.NSString, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CSLocalizedString ();
	public CSLocalizedString (MonoTouch.Foundation.NSCoder coder);
	public CSLocalizedString (MonoTouch.Foundation.NSObjectFlag t);
	public CSLocalizedString (IntPtr handle);
	public CSLocalizedString (MonoTouch.Foundation.NSDictionary localizedStrings);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual string GetLocalizedString ();
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSMailboxKey

<pre style='color: green'>
public static class CSMailboxKey {
	// properties
	public static MonoTouch.Foundation.NSString Archive { get; }
	public static MonoTouch.Foundation.NSString Drafts { get; }
	public static MonoTouch.Foundation.NSString Inbox { get; }
	public static MonoTouch.Foundation.NSString Junk { get; }
	public static MonoTouch.Foundation.NSString Sent { get; }
	public static MonoTouch.Foundation.NSString Trash { get; }
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSMeteringModeKey

<pre style='color: green'>
public static class CSMeteringModeKey {
	// properties
	public static MonoTouch.Foundation.NSString Average { get; }
	public static MonoTouch.Foundation.NSString CenterWeightedAverage { get; }
	public static MonoTouch.Foundation.NSString MultiSpot { get; }
	public static MonoTouch.Foundation.NSString Partial { get; }
	public static MonoTouch.Foundation.NSString Pattern { get; }
	public static MonoTouch.Foundation.NSString Spot { get; }
	public static MonoTouch.Foundation.NSString Unknown { get; }
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSPerson

<pre style='color: green'>
public class CSPerson : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CSPerson ();
	public CSPerson (MonoTouch.Foundation.NSCoder coder);
	public CSPerson (MonoTouch.Foundation.NSObjectFlag t);
	public CSPerson (IntPtr handle);
	public CSPerson (string displayName, string[] handles, MonoTouch.Foundation.NSString handleIdentifier);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string ContactIdentifier { get; set; }
	public virtual string DisplayName { get; }
	public virtual MonoTouch.Foundation.NSString HandleIdentifier { get; }
	public virtual string[] Handles { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSSearchableIndex

<pre style='color: green'>
public class CSSearchableIndex : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CSSearchableIndex ();
	public CSSearchableIndex (MonoTouch.Foundation.NSCoder coder);
	public CSSearchableIndex (MonoTouch.Foundation.NSObjectFlag t);
	public CSSearchableIndex (IntPtr handle);
	public CSSearchableIndex (string name);
	public CSSearchableIndex (string name, MonoTouch.Foundation.NSString protectionClass);
	// properties
	public override IntPtr ClassHandle { get; }
	public static CSSearchableIndex DefaultSearchableIndex { get; }
	public virtual ICSSearchableIndexDelegate IndexDelegate { get; set; }
	// methods
	public virtual void Delete (string[] identifiers, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual void DeleteAll (System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual void DeleteWithDomain (string[] domainIdentifiers, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
	protected override void Dispose (bool disposing);
	public static CSSearchableIndex FromName (string name, CSFileProtection? protectionOption);
	public virtual void Index (CSSearchableItem[] items, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSSearchableIndex_CSOptionalBatchingExtension

<pre style='color: green'>
public static class CSSearchableIndex_CSOptionalBatchingExtension {
	// methods
	public static void BeginIndexBatch (CSSearchableIndex This);
	public static void EndIndexBatch (CSSearchableIndex This, MonoTouch.Foundation.NSData clientState, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
	public static void FetchLastClientState (CSSearchableIndex This, CSSearchableIndexFetchHandler completionHandler);
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSSearchableIndexDelegate

<pre style='color: green'>
public abstract class CSSearchableIndexDelegate : MonoTouch.Foundation.NSObject, ICSSearchableIndexDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CSSearchableIndexDelegate ();
	public CSSearchableIndexDelegate (MonoTouch.Foundation.NSCoder coder);
	public CSSearchableIndexDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public CSSearchableIndexDelegate (IntPtr handle);
	// methods
	public virtual void ReindexAllSearchableItems (CSSearchableIndex searchableIndex, System.Action acknowledgementHandler);
	public virtual void ReindexSearchableItems (CSSearchableIndex searchableIndex, string[] identifiers, System.Action acknowledgementHandler);
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSSearchableIndexDelegate_Extensions

<pre style='color: green'>
public static class CSSearchableIndexDelegate_Extensions {
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSSearchableIndexFetchHandler

<pre style='color: green'>
public sealed delegate CSSearchableIndexFetchHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CSSearchableIndexFetchHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSData clientState, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSData clientState, MonoTouch.Foundation.NSError error);
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSSearchableItem

<pre style='color: green'>
public class CSSearchableItem : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CSSearchableItem ();
	public CSSearchableItem (MonoTouch.Foundation.NSCoder coder);
	public CSSearchableItem (MonoTouch.Foundation.NSObjectFlag t);
	public CSSearchableItem (IntPtr handle);
	public CSSearchableItem (string uniqueIdentifier, string domainIdentifier, CSSearchableItemAttributeSet attributeSet);
	// properties
	public static MonoTouch.Foundation.NSString ActionType { get; }
	public static MonoTouch.Foundation.NSString ActivityIdentifier { get; }
	public virtual CSSearchableItemAttributeSet AttributeSet { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string DomainIdentifier { get; set; }
	public virtual MonoTouch.Foundation.NSDate ExpirationDate { get; set; }
	public virtual string UniqueIdentifier { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.CoreSpotlight.CSSearchableItemAttributeSet

<pre style='color: green'>
public class CSSearchableItemAttributeSet : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public CSSearchableItemAttributeSet ();
	public CSSearchableItemAttributeSet (MonoTouch.Foundation.NSCoder coder);
	public CSSearchableItemAttributeSet (MonoTouch.Foundation.NSObjectFlag t);
	public CSSearchableItemAttributeSet (IntPtr handle);
	public CSSearchableItemAttributeSet (string itemContentType);
	// properties
	public virtual string[] AccountHandles { get; set; }
	public virtual string AccountIdentifier { get; set; }
	public virtual string AcquisitionMake { get; set; }
	public virtual string AcquisitionModel { get; set; }
	public virtual MonoTouch.Foundation.NSDate AddedDate { get; set; }
	public virtual CSPerson[] AdditionalRecipients { get; set; }
	public virtual string Album { get; set; }
	public virtual string[] AlternateNames { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Altitude { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Aperture { get; set; }
	public virtual string Artist { get; set; }
	public virtual string[] Audiences { get; set; }
	public virtual MonoTouch.Foundation.NSNumber AudioBitRate { get; set; }
	public virtual MonoTouch.Foundation.NSNumber AudioChannelCount { get; set; }
	public virtual string AudioEncodingApplication { get; set; }
	public virtual MonoTouch.Foundation.NSNumber AudioSampleRate { get; set; }
	public virtual MonoTouch.Foundation.NSNumber AudioTrackNumber { get; set; }
	public virtual string[] AuthorAddresses { get; set; }
	public virtual string[] AuthorEmailAddresses { get; set; }
	public virtual string[] AuthorNames { get; set; }
	public virtual CSPerson[] Authors { get; set; }
	public virtual MonoTouch.Foundation.NSNumber BitsPerSample { get; set; }
	public virtual string CameraOwner { get; set; }
	public virtual string City { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string[] Codecs { get; set; }
	public virtual string ColorSpace { get; set; }
	public virtual string Comment { get; set; }
	public virtual MonoTouch.Foundation.NSDate CompletionDate { get; set; }
	public virtual string Composer { get; set; }
	public virtual string[] ContactKeywords { get; set; }
	public virtual MonoTouch.Foundation.NSDate ContentCreationDate { get; set; }
	public virtual string ContentDescription { get; set; }
	public virtual MonoTouch.Foundation.NSDate ContentModificationDate { get; set; }
	public virtual MonoTouch.Foundation.NSNumber ContentRating { get; set; }
	public virtual string[] ContentSources { get; set; }
	public virtual string ContentType { get; set; }
	public virtual string[] ContentTypeTree { get; set; }
	public virtual MonoTouch.Foundation.NSUrl ContentUrl { get; set; }
	public virtual string[] Contributors { get; set; }
	public virtual string Copyright { get; set; }
	public virtual string Country { get; set; }
	public virtual string[] Coverage { get; set; }
	public virtual string Creator { get; set; }
	public virtual MonoTouch.Foundation.NSNumber DeliveryType { get; set; }
	public virtual string Director { get; set; }
	public virtual string DisplayName { get; set; }
	public virtual MonoTouch.Foundation.NSDate DownloadedDate { get; set; }
	public virtual MonoTouch.Foundation.NSDate DueDate { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Duration { get; set; }
	public virtual string[] Editors { get; set; }
	public virtual string[] EmailAddresses { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary EmailHeaders { get; set; }
	public virtual string[] EncodingApplications { get; set; }
	public virtual MonoTouch.Foundation.NSDate EndDate { get; set; }
	public virtual string ExifGpsVersion { get; set; }
	public virtual string ExifVersion { get; set; }
	public virtual MonoTouch.Foundation.NSNumber ExposureMode { get; set; }
	public virtual string ExposureProgram { get; set; }
	public virtual MonoTouch.Foundation.NSNumber ExposureTime { get; set; }
	public virtual string ExposureTimeString { get; set; }
	public virtual MonoTouch.Foundation.NSNumber FlashOn { get; set; }
	public virtual MonoTouch.Foundation.NSNumber FNumber { get; set; }
	public virtual MonoTouch.Foundation.NSNumber FocalLength { get; set; }
	public virtual MonoTouch.Foundation.NSNumber FocalLength35mm { get; set; }
	public virtual string[] FontNames { get; set; }
	public virtual MonoTouch.Foundation.NSNumber GeneralMidiSequence { get; set; }
	public virtual string Genre { get; set; }
	public virtual string GpsAreaInformation { get; set; }
	public virtual MonoTouch.Foundation.NSDate GpsDateStamp { get; set; }
	public virtual MonoTouch.Foundation.NSNumber GpsDestBearing { get; set; }
	public virtual MonoTouch.Foundation.NSNumber GpsDestDistance { get; set; }
	public virtual MonoTouch.Foundation.NSNumber GpsDestLatitude { get; set; }
	public virtual MonoTouch.Foundation.NSNumber GpsDestLongitude { get; set; }
	public virtual MonoTouch.Foundation.NSNumber GpsDifferental { get; set; }
	public virtual MonoTouch.Foundation.NSNumber GpsDop { get; set; }
	public virtual string GpsMapDatum { get; set; }
	public virtual string GpsMeasureMode { get; set; }
	public virtual string GpsProcessingMethod { get; set; }
	public virtual string GpsStatus { get; set; }
	public virtual MonoTouch.Foundation.NSNumber GpsTrack { get; set; }
	public virtual MonoTouch.Foundation.NSNumber HasAlphaChannel { get; set; }
	public virtual string Headline { get; set; }
	public virtual CSPerson[] HiddenAdditionalRecipients { get; set; }
	public virtual MonoTouch.Foundation.NSData HtmlContentData { get; set; }
	public virtual string Identifier { get; set; }
	public virtual MonoTouch.Foundation.NSNumber ImageDirection { get; set; }
	public virtual MonoTouch.Foundation.NSDate[] ImportantDates { get; set; }
	public virtual string Information { get; set; }
	public virtual string[] InstantMessageAddresses { get; set; }
	public virtual string Instructions { get; set; }
	public virtual MonoTouch.Foundation.NSNumber IsoSpeed { get; set; }
	public virtual string KeySignature { get; set; }
	public virtual string[] Keywords { get; set; }
	public virtual string Kind { get; set; }
	public virtual string[] Languages { get; set; }
	public virtual MonoTouch.Foundation.NSDate LastUsedDate { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Latitude { get; set; }
	public virtual string[] LayerNames { get; set; }
	public virtual string LensModel { get; set; }
	public virtual MonoTouch.Foundation.NSNumber LikelyJunk { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Local { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Longitude { get; set; }
	public virtual string Lyricist { get; set; }
	public virtual string[] MailboxIdentifiers { get; set; }
	public virtual MonoTouch.Foundation.NSNumber MaxAperture { get; set; }
	public virtual string[] MediaTypes { get; set; }
	public virtual MonoTouch.Foundation.NSDate MetadataModificationDate { get; set; }
	public virtual string MeteringMode { get; set; }
	public virtual string MusicalGenre { get; set; }
	public virtual string MusicalInstrumentCategory { get; set; }
	public virtual string MusicalInstrumentName { get; set; }
	public virtual string NamedLocation { get; set; }
	public virtual string[] Organizations { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Orientation { get; set; }
	public virtual string OriginalFormat { get; set; }
	public virtual string OriginalSource { get; set; }
	public virtual MonoTouch.Foundation.NSNumber PageCount { get; set; }
	public virtual MonoTouch.Foundation.NSNumber PageHeight { get; set; }
	public virtual MonoTouch.Foundation.NSNumber PageWidth { get; set; }
	public virtual string[] Participants { get; set; }
	public virtual string Path { get; set; }
	public virtual string[] Performers { get; set; }
	public virtual string[] PhoneNumbers { get; set; }
	public virtual MonoTouch.Foundation.NSNumber PixelCount { get; set; }
	public virtual MonoTouch.Foundation.NSNumber PixelHeight { get; set; }
	public virtual MonoTouch.Foundation.NSNumber PixelWidth { get; set; }
	public virtual MonoTouch.Foundation.NSNumber PlayCount { get; set; }
	public virtual CSPerson[] PrimaryRecipients { get; set; }
	public virtual string Producer { get; set; }
	public virtual string ProfileName { get; set; }
	public virtual string[] Projects { get; set; }
	public virtual string[] Publishers { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Rating { get; set; }
	public virtual string[] RecipientAddresses { get; set; }
	public virtual string[] RecipientEmailAddresses { get; set; }
	public virtual string[] RecipientNames { get; set; }
	public virtual MonoTouch.Foundation.NSDate RecordingDate { get; set; }
	public virtual MonoTouch.Foundation.NSNumber RedEyeOn { get; set; }
	public virtual string RelatedUniqueIdentifier { get; set; }
	public virtual MonoTouch.Foundation.NSNumber ResolutionHeightDPI { get; set; }
	public virtual MonoTouch.Foundation.NSNumber ResolutionWidthDpi { get; set; }
	public virtual string Rights { get; set; }
	public virtual string Role { get; set; }
	public virtual string SecurityMethod { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Speed { get; set; }
	public virtual MonoTouch.Foundation.NSDate StartDate { get; set; }
	public virtual string StateOrProvince { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Streamable { get; set; }
	public virtual string Subject { get; set; }
	public virtual MonoTouch.Foundation.NSNumber Tempo { get; set; }
	public virtual string TextContent { get; set; }
	public virtual string Theme { get; set; }
	public virtual MonoTouch.Foundation.NSData ThumbnailData { get; set; }
	public virtual MonoTouch.Foundation.NSUrl ThumbnailUrl { get; set; }
	public virtual string TimeSignature { get; set; }
	public virtual MonoTouch.Foundation.NSDate Timestamp { get; set; }
	public virtual string Title { get; set; }
	public virtual MonoTouch.Foundation.NSNumber TotalBitRate { get; set; }
	public virtual MonoTouch.Foundation.NSUrl Url { get; set; }
	public virtual string Version { get; set; }
	public virtual MonoTouch.Foundation.NSNumber VideoBitRate { get; set; }
	public virtual MonoTouch.Foundation.NSNumber WhiteBalance { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.CoreSpotlight.ICSSearchableIndexDelegate

<pre style='color: green'>
public interface ICSSearchableIndexDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void ReindexAllSearchableItems (CSSearchableIndex searchableIndex, System.Action acknowledgementHandler);
	public virtual void ReindexSearchableItems (CSSearchableIndex searchableIndex, string[] identifiers, System.Action acknowledgementHandler);
}
</pre>

## New Namespace MonoTouch.ModelIO

### New Type MonoTouch.ModelIO.IMDLComponent

<pre style='color: green'>
public interface IMDLComponent : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.ModelIO.IMDLMeshBuffer

<pre style='color: green'>
public interface IMDLMeshBuffer : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSCopying {
	// properties
	public virtual MonoTouch.Foundation.NSData Map { get; }
	// methods
	public virtual void Offset (MonoTouch.Foundation.NSData data, uint offset);
}
</pre>

### New Type MonoTouch.ModelIO.IMDLMeshBufferAllocator

<pre style='color: green'>
public interface IMDLMeshBufferAllocator : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual IMDLMeshBuffer NewBuffer (uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferFromZone (IMDLMeshBufferZone zone, uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferFromZone (IMDLMeshBufferZone zone, MonoTouch.Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferWithData (MonoTouch.Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBufferZone NewZone (uint capacity);
}
</pre>

### New Type MonoTouch.ModelIO.IMDLMeshBufferZone

<pre style='color: green'>
public interface IMDLMeshBufferZone : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.ModelIO.IMDLNamed

<pre style='color: green'>
public interface IMDLNamed : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.ModelIO.IMDLObjectContainerComponent

<pre style='color: green'>
public interface IMDLObjectContainerComponent : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMDLComponent {
	// properties
	public virtual MDLObject[] Objects { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type MonoTouch.ModelIO.IMDLTransformComponent

<pre style='color: green'>
public interface IMDLTransformComponent : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMDLComponent {
	// properties
	public virtual OpenTK.Matrix4 Matrix { get; set; }
	public virtual double MaximumTime { get; }
	public virtual double MinimumTime { get; }
}
</pre>

### New Type MonoTouch.ModelIO.MDLAreaLight

<pre style='color: green'>
public class MDLAreaLight : MonoTouch.ModelIO.MDLPhysicallyPlausibleLight, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLAreaLight (MonoTouch.Foundation.NSCoder coder);
	public MDLAreaLight (MonoTouch.Foundation.NSObjectFlag t);
	public MDLAreaLight (IntPtr handle);
	// properties
	public virtual float AreaRadius { get; set; }
	public virtual float Aspect { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2 SuperEllipticPower { get; set; }
}
</pre>

### New Type MonoTouch.ModelIO.MDLAsset

<pre style='color: green'>
public class MDLAsset : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLAsset ();
	public MDLAsset (MonoTouch.Foundation.NSCoder coder);
	public MDLAsset (MonoTouch.Foundation.NSObjectFlag t);
	public MDLAsset (IntPtr handle);
	public MDLAsset (MonoTouch.Foundation.NSUrl URL);
	public MDLAsset (MonoTouch.Foundation.NSUrl URL, MDLVertexDescriptor vertexDescriptor, IMDLMeshBufferAllocator bufferAllocator);
	// properties
	public virtual MDLAxisAlignedBoundingBox BoundingBox { get; }
	public virtual IMDLMeshBufferAllocator BufferAllocator { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual double EndTime { get; set; }
	public virtual double FrameInterval { get; set; }
	public MDLObject Item { get; }
	public virtual double StartTime { get; set; }
	public virtual MonoTouch.Foundation.NSUrl URL { get; }
	public virtual MDLVertexDescriptor VertexDescriptor { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	public virtual MDLAxisAlignedBoundingBox BoundingBoxAtTime (double time);
	public static bool CanExportFileExtension (string extension);
	public static bool CanImportFileExtension (string extension);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual bool ExportAssetToURL (MonoTouch.Foundation.NSUrl URL);
	public virtual MDLObject GetObjectAtIndex (uint index);
	public virtual MDLObject GetObjectAtIndexedSubscript (uint index);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type MonoTouch.ModelIO.MDLAxisAlignedBoundingBox

<pre style='color: green'>
public struct MDLAxisAlignedBoundingBox {
	// fields
	public OpenTK.Vector3 MaxBounds;
	public OpenTK.Vector3 MinBounds;
}
</pre>

### New Type MonoTouch.ModelIO.MDLComponent

<pre style='color: green'>
public class MDLComponent : MonoTouch.Foundation.NSObject, IMDLComponent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLComponent ();
	public MDLComponent (MonoTouch.Foundation.NSCoder coder);
	public MDLComponent (MonoTouch.Foundation.NSObjectFlag t);
	public MDLComponent (IntPtr handle);
}
</pre>

### New Type MonoTouch.ModelIO.MDLComponent_Extensions

<pre style='color: green'>
public static class MDLComponent_Extensions {
}
</pre>

### New Type MonoTouch.ModelIO.MDLGeometryKind

<pre style='color: green'>
[Serializable]
public enum MDLGeometryKind {
	Lines = 1,
	Points = 0,
	Quads = 4,
	Triangles = 2,
	TriangleStrips = 3,
}
</pre>

### New Type MonoTouch.ModelIO.MDLIndexBitDepth

<pre style='color: green'>
[Serializable]
public enum MDLIndexBitDepth {
	Invalid = 0,
	UInt16 = 16,
	UInt32 = 32,
	UInt8 = 8,
}
</pre>

### New Type MonoTouch.ModelIO.MDLLight

<pre style='color: green'>
public class MDLLight : MonoTouch.ModelIO.MDLObject, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLLight ();
	public MDLLight (MonoTouch.Foundation.NSCoder coder);
	public MDLLight (MonoTouch.Foundation.NSObjectFlag t);
	public MDLLight (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLLightType LightType { get; }
	// methods
	public virtual MonoTouch.CoreGraphics.CGColor EvaluatedColorFromVector (OpenTK.Vector3 vector);
}
</pre>

### New Type MonoTouch.ModelIO.MDLLightProbe

<pre style='color: green'>
public class MDLLightProbe : MonoTouch.ModelIO.MDLLight, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLLightProbe ();
	public MDLLightProbe (MonoTouch.Foundation.NSCoder coder);
	public MDLLightProbe (MonoTouch.Foundation.NSObjectFlag t);
	public MDLLightProbe (IntPtr handle);
	public MDLLightProbe (MDLTexture reflectiveTexture, MDLTexture irradianceTexture);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLTexture IrradianceTexture { get; }
	public virtual MDLTexture ReflectiveTexture { get; }
	public virtual MonoTouch.Foundation.NSData SphericalHarmonicsCoefficients { get; }
	public virtual uint SphericalHarmonicsLevel { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void GenerateSphericalHarmonicsFromIrradiance (uint sphericalHarmonicsLevel);
}
</pre>

### New Type MonoTouch.ModelIO.MDLLightType

<pre style='color: green'>
[Serializable]
public enum MDLLightType {
	Ambient = 1,
	Directional = 2,
	DiscArea = 6,
	Environment = 11,
	Linear = 5,
	Photometric = 9,
	Point = 4,
	Probe = 10,
	RectangularArea = 7,
	Spot = 3,
	SuperElliptical = 8,
	Unknown = 0,
}
</pre>

### New Type MonoTouch.ModelIO.MDLMaterial

<pre style='color: green'>
public class MDLMaterial : MonoTouch.Foundation.NSObject, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLMaterial ();
	public MDLMaterial (MonoTouch.Foundation.NSCoder coder);
	public MDLMaterial (MonoTouch.Foundation.NSObjectFlag t);
	public MDLMaterial (IntPtr handle);
	public MDLMaterial (string name, MDLScatteringFunction scatteringFunction);
	// properties
	public virtual MDLMaterial BaseMaterial { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual string Name { get; set; }
	public virtual MDLScatteringFunction ScatteringFunction { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual MDLMaterialProperty GetProperty (string name);
	public virtual MDLMaterialProperty GetProperty (MDLMaterialSemantic semantic);
	public virtual void RemoveAllProperties ();
	public virtual void RemoveProperty (MDLMaterialProperty property);
	public virtual void SetProperty (MDLMaterialProperty property);
}
</pre>

### New Type MonoTouch.ModelIO.MDLMaterialMipMapFilterMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialMipMapFilterMode {
	Linear = 1,
	Nearest = 0,
}
</pre>

### New Type MonoTouch.ModelIO.MDLMaterialProperty

<pre style='color: green'>
public class MDLMaterialProperty : MonoTouch.Foundation.NSObject, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLMaterialProperty (MonoTouch.Foundation.NSCoder coder);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, MDLTextureSampler textureSampler);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, string stringValue);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, MonoTouch.Foundation.NSUrl URL);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Matrix4 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector4 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector3 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector2 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, float value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic);
	public MDLMaterialProperty (IntPtr handle);
	public MDLMaterialProperty (MonoTouch.Foundation.NSObjectFlag t);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, MonoTouch.CoreGraphics.CGColor color);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.CoreGraphics.CGColor Color { get; set; }
	public virtual OpenTK.Vector2 Float2Value { get; set; }
	public virtual OpenTK.Vector3 Float3Value { get; set; }
	public virtual OpenTK.Vector4 Float4Value { get; set; }
	public virtual float FloatValue { get; set; }
	public virtual OpenTK.Matrix4 Matrix4x4 { get; set; }
	public virtual string Name { get; set; }
	public virtual MDLMaterialSemantic Semantic { get; set; }
	public virtual string StringValue { get; set; }
	public virtual MDLTextureSampler TextureSamplerValue { get; set; }
	public virtual MDLMaterialPropertyType Type { get; }
	public virtual MonoTouch.Foundation.NSUrl UrlValue { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetProperties (MDLMaterialProperty property);
}
</pre>

### New Type MonoTouch.ModelIO.MDLMaterialPropertyType

<pre style='color: green'>
[Serializable]
public enum MDLMaterialPropertyType {
	Color = 4,
	Float = 5,
	Float2 = 6,
	Float3 = 7,
	Float4 = 8,
	Matrix44 = 9,
	None = 0,
	String = 1,
	Texture = 3,
	Url = 2,
}
</pre>

### New Type MonoTouch.ModelIO.MDLMaterialSemantic

<pre style='color: green'>
[Serializable]
public enum MDLMaterialSemantic {
	AmbientOcclusion = 20,
	AmbientOcclusionScale = 21,
	Anisotropic = 6,
	BaseColor = 0,
	Bump = 12,
	Clearcoat = 9,
	ClearcoatGloss = 10,
	Displacement = 18,
	DisplacementScale = 19,
	Emission = 11,
	InterfaceIndexOfRefraction = 14,
	MaterialIndexOfRefraction = 15,
	Metallic = 2,
	None = 32768,
	ObjectSpaceNormal = 16,
	Opacity = 13,
	Roughness = 5,
	Sheen = 7,
	SheenTint = 8,
	Specular = 3,
	SpecularTint = 4,
	Subsurface = 1,
	TangentSpaceNormal = 17,
	UserDefined = 32769,
}
</pre>

### New Type MonoTouch.ModelIO.MDLMaterialTextureFilterMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialTextureFilterMode {
	Linear = 1,
	Nearest = 0,
}
</pre>

### New Type MonoTouch.ModelIO.MDLMaterialTextureWrapMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialTextureWrapMode {
	Clamp = 0,
	Mirror = 2,
	Repeat = 1,
}
</pre>

### New Type MonoTouch.ModelIO.MDLMesh

<pre style='color: green'>
public class MDLMesh : MonoTouch.ModelIO.MDLObject, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLMesh ();
	public MDLMesh (MonoTouch.Foundation.NSCoder coder);
	public MDLMesh (MonoTouch.Foundation.NSObjectFlag t);
	public MDLMesh (IntPtr handle);
	public MDLMesh (IMDLMeshBuffer vertexBuffer, uint vertexCount, MDLVertexDescriptor descriptor, MDLSubmesh[] submeshes);
	public MDLMesh (IMDLMeshBuffer[] vertexBuffers, uint vertexCount, MDLVertexDescriptor descriptor, MDLSubmesh[] submeshes);
	// properties
	public virtual MDLAxisAlignedBoundingBox BoundingBox { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSMutableArray Submeshes { get; }
	public virtual MonoTouch.Foundation.NSMutableArray VertexBuffers { get; }
	public virtual uint VertexCount { get; }
	public virtual MDLVertexDescriptor VertexDescriptor { get; set; }
	// methods
	public virtual void AddAttribute (string name, MDLVertexFormat format);
	public virtual void AddNormals (string name, float creaseThreshold);
	public virtual void AddTangentBasis (string textureCoordinateAttributeName, string tangentAttributeName, string bitangentAttributeName);
	public virtual void AddTangentBasisWithNormals (string textureCoordinateAttributeName, string normalAttributeName, string tangentAttributeName);
	public static MDLMesh CreateBox (OpenTK.Vector3 dimensions, OpenTK.Vector3i segments, bool inwardNormals, MDLGeometryKind geometryType, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateCylindroid (float height, OpenTK.Vector2 radii, uint radialSegments, uint verticalSegments, MDLGeometryKind geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateEllipsoid (OpenTK.Vector3 radii, uint radialSegments, uint verticalSegments, MDLGeometryKind geometryType, bool inwardNormals, bool hemisphere, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateEllipticalCone (float height, OpenTK.Vector2 radii, uint radialSegments, uint verticalSegments, MDLGeometryKind geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateIcosahedron (float radius, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MonoTouch.Foundation.NSObject CreatePlane (OpenTK.Vector2 dimensions, OpenTK.Vector2i segments, MDLGeometryKind geometryType, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateSubdividedMesh (MDLMesh mesh, uint submeshIndex, uint subdivisionLevels);
	protected override void Dispose (bool disposing);
	public virtual bool GenerateAmbientOcclusionTexture (float bakeQuality, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateAmbientOcclusionTexture (OpenTK.Vector2i textureSize, int raysPerSample, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateAmbientOcclusionVertexColors (int raysPerSample, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual bool GenerateAmbientOcclusionVertexColors (float bakeQuality, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual bool GenerateLightMapTexture (float bakeQuality, MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateLightMapTexture (OpenTK.Vector2i textureSize, MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateLightMapVertexColors (MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual MDLVertexAttributeData GetVertexAttributeDataForAttribute (string attributeName);
	public virtual void MakeVerticesUnique ();
}
</pre>

### New Type MonoTouch.ModelIO.MDLMeshBuffer

<pre style='color: green'>
public abstract class MDLMeshBuffer : MonoTouch.Foundation.NSObject, IMDLMeshBuffer, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLMeshBuffer ();
	public MDLMeshBuffer (MonoTouch.Foundation.NSCoder coder);
	public MDLMeshBuffer (MonoTouch.Foundation.NSObjectFlag t);
	public MDLMeshBuffer (IntPtr handle);
	// properties
	public virtual IMDLMeshBufferAllocator Allocator { get; }
	public virtual uint Length { get; }
	public virtual MonoTouch.Foundation.NSData Map { get; }
	public virtual MDLMeshBufferType Type { get; }
	public virtual IMDLMeshBufferZone Zone { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual void Offset (MonoTouch.Foundation.NSData data, uint offset);
}
</pre>

### New Type MonoTouch.ModelIO.MDLMeshBuffer_Extensions

<pre style='color: green'>
public static class MDLMeshBuffer_Extensions {
	// methods
	public static IMDLMeshBufferAllocator GetAllocator (IMDLMeshBuffer This);
	public static uint GetLength (IMDLMeshBuffer This);
	public static MDLMeshBufferType GetType (IMDLMeshBuffer This);
	public static IMDLMeshBufferZone GetZone (IMDLMeshBuffer This);
}
</pre>

### New Type MonoTouch.ModelIO.MDLMeshBufferAllocator

<pre style='color: green'>
public abstract class MDLMeshBufferAllocator : MonoTouch.Foundation.NSObject, IMDLMeshBufferAllocator, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLMeshBufferAllocator ();
	public MDLMeshBufferAllocator (MonoTouch.Foundation.NSCoder coder);
	public MDLMeshBufferAllocator (MonoTouch.Foundation.NSObjectFlag t);
	public MDLMeshBufferAllocator (IntPtr handle);
	// methods
	public virtual IMDLMeshBuffer NewBuffer (uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferFromZone (IMDLMeshBufferZone zone, uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferFromZone (IMDLMeshBufferZone zone, MonoTouch.Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferWithData (MonoTouch.Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBufferZone NewZone (uint capacity);
}
</pre>

### New Type MonoTouch.ModelIO.MDLMeshBufferAllocator_Extensions

<pre style='color: green'>
public static class MDLMeshBufferAllocator_Extensions {
}
</pre>

### New Type MonoTouch.ModelIO.MDLMeshBufferType

<pre style='color: green'>
[Serializable]
public enum MDLMeshBufferType {
	Index = 2,
	Vertex = 1,
}
</pre>

### New Type MonoTouch.ModelIO.MDLMeshBufferZone

<pre style='color: green'>
public class MDLMeshBufferZone : MonoTouch.Foundation.NSObject, IMDLMeshBufferZone, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLMeshBufferZone ();
	public MDLMeshBufferZone (MonoTouch.Foundation.NSCoder coder);
	public MDLMeshBufferZone (MonoTouch.Foundation.NSObjectFlag t);
	public MDLMeshBufferZone (IntPtr handle);
	// properties
	public virtual IMDLMeshBufferAllocator Allocator { get; }
	public virtual uint Capacity { get; }
}
</pre>

### New Type MonoTouch.ModelIO.MDLMeshBufferZone_Extensions

<pre style='color: green'>
public static class MDLMeshBufferZone_Extensions {
	// methods
	public static IMDLMeshBufferAllocator GetAllocator (IMDLMeshBufferZone This);
	public static uint GetCapacity (IMDLMeshBufferZone This);
}
</pre>

### New Type MonoTouch.ModelIO.MDLNamed_Extensions

<pre style='color: green'>
public static class MDLNamed_Extensions {
	// methods
	public static string GetName (IMDLNamed This);
	public static void SetName (IMDLNamed This, string value);
}
</pre>

### New Type MonoTouch.ModelIO.MDLObject

<pre style='color: green'>
public class MDLObject : MonoTouch.Foundation.NSObject, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLObject ();
	public MDLObject (MonoTouch.Foundation.NSCoder coder);
	public MDLObject (MonoTouch.Foundation.NSObjectFlag t);
	public MDLObject (IntPtr handle);
	// properties
	public virtual IMDLObjectContainerComponent Children { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	public virtual MDLObject Parent { get; set; }
	public virtual IMDLTransformComponent Transform { get; set; }
	// methods
	public virtual void AddChild (MDLObject child);
	public virtual MDLAxisAlignedBoundingBox BoundingBoxAtTime (double time);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ModelIO.MDLObjectContainerComponent

<pre style='color: green'>
public abstract class MDLObjectContainerComponent : MonoTouch.Foundation.NSObject, IMDLObjectContainerComponent, IMDLComponent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLObjectContainerComponent ();
	public MDLObjectContainerComponent (MonoTouch.Foundation.NSCoder coder);
	public MDLObjectContainerComponent (MonoTouch.Foundation.NSObjectFlag t);
	public MDLObjectContainerComponent (IntPtr handle);
	// properties
	public virtual MDLObject[] Objects { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type MonoTouch.ModelIO.MDLObjectContainerComponent_Extensions

<pre style='color: green'>
public static class MDLObjectContainerComponent_Extensions {
}
</pre>

### New Type MonoTouch.ModelIO.MDLPhotometricLight

<pre style='color: green'>
public class MDLPhotometricLight : MonoTouch.ModelIO.MDLLight, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLPhotometricLight ();
	public MDLPhotometricLight (MonoTouch.Foundation.NSCoder coder);
	public MDLPhotometricLight (MonoTouch.Foundation.NSObjectFlag t);
	public MDLPhotometricLight (IntPtr handle);
	public MDLPhotometricLight (MonoTouch.Foundation.NSUrl url);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint ConeSpans { get; }
	public virtual float HorizontalAngle { get; }
	public virtual uint HorizontalSpans { get; }
	public virtual float IESConeAngle { get; }
	public virtual MonoTouch.Foundation.NSData LightWeb { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ModelIO.MDLPhysicallyPlausibleLight

<pre style='color: green'>
public class MDLPhysicallyPlausibleLight : MonoTouch.ModelIO.MDLLight, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLPhysicallyPlausibleLight ();
	public MDLPhysicallyPlausibleLight (MonoTouch.Foundation.NSCoder coder);
	public MDLPhysicallyPlausibleLight (MonoTouch.Foundation.NSObjectFlag t);
	public MDLPhysicallyPlausibleLight (IntPtr handle);
	// properties
	public virtual float AttenuationEndDistance { get; set; }
	public virtual float AttenuationFalloffExponent { get; set; }
	public virtual float AttenuationStartDistance { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.CoreGraphics.CGColor Color { get; set; }
	public virtual float InnerConeAngle { get; set; }
	public virtual float Lumens { get; set; }
	public virtual float OuterConeAngle { get; set; }
	// methods
	public virtual void SetColorByTemperature (float temperature);
}
</pre>

### New Type MonoTouch.ModelIO.MDLPhysicallyPlausibleScatteringFunction

<pre style='color: green'>
public class MDLPhysicallyPlausibleScatteringFunction : MonoTouch.ModelIO.MDLScatteringFunction, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLPhysicallyPlausibleScatteringFunction ();
	public MDLPhysicallyPlausibleScatteringFunction (MonoTouch.Foundation.NSCoder coder);
	public MDLPhysicallyPlausibleScatteringFunction (MonoTouch.Foundation.NSObjectFlag t);
	public MDLPhysicallyPlausibleScatteringFunction (IntPtr handle);
	// properties
	public virtual MDLMaterialProperty Anisotropic { get; }
	public virtual MDLMaterialProperty AnisotropicRotation { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialProperty Clearcoat { get; }
	public virtual MDLMaterialProperty ClearcoatGloss { get; }
	public virtual MDLMaterialProperty Metallic { get; }
	public virtual MDLMaterialProperty Roughness { get; }
	public virtual MDLMaterialProperty Sheen { get; }
	public virtual MDLMaterialProperty SheenTint { get; }
	public virtual MDLMaterialProperty SpecularAmount { get; }
	public virtual MDLMaterialProperty SpecularTint { get; }
	public virtual MDLMaterialProperty Subsurface { get; }
	public virtual int Version { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ModelIO.MDLScatteringFunction

<pre style='color: green'>
public class MDLScatteringFunction : MonoTouch.Foundation.NSObject, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLScatteringFunction ();
	public MDLScatteringFunction (MonoTouch.Foundation.NSCoder coder);
	public MDLScatteringFunction (MonoTouch.Foundation.NSObjectFlag t);
	public MDLScatteringFunction (IntPtr handle);
	// properties
	public virtual MDLMaterialProperty AmbientOcclusion { get; }
	public virtual MDLMaterialProperty AmbientOcclusionScale { get; }
	public virtual MDLMaterialProperty BaseColor { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialProperty Emission { get; }
	public virtual MDLMaterialProperty InterfaceIndexOfRefraction { get; }
	public virtual MDLMaterialProperty MaterialIndexOfRefraction { get; }
	public virtual string Name { get; set; }
	public virtual MDLMaterialProperty Normal { get; }
	public virtual MDLMaterialProperty Specular { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ModelIO.MDLSubmesh

<pre style='color: green'>
public class MDLSubmesh : MonoTouch.Foundation.NSObject, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLSubmesh ();
	public MDLSubmesh (MonoTouch.Foundation.NSCoder coder);
	public MDLSubmesh (MonoTouch.Foundation.NSObjectFlag t);
	public MDLSubmesh (IntPtr handle);
	public MDLSubmesh (string name, IMDLMeshBuffer indexBuffer, uint indexCount, MDLIndexBitDepth indexType, MDLGeometryKind geometryType, MDLMaterial material);
	public MDLSubmesh (IMDLMeshBuffer indexBuffer, uint indexCount, MDLIndexBitDepth indexType, MDLGeometryKind geometryType, MDLMaterial material);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLGeometryKind GeometryType { get; }
	public virtual IMDLMeshBuffer IndexBuffer { get; }
	public virtual uint IndexCount { get; }
	public virtual MDLIndexBitDepth IndexType { get; }
	public virtual MDLMaterial Material { get; set; }
	public virtual string Name { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ModelIO.MDLTexture

<pre style='color: green'>
public class MDLTexture : MonoTouch.Foundation.NSObject, IMDLNamed, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLTexture ();
	public MDLTexture (MonoTouch.Foundation.NSCoder coder);
	public MDLTexture (MonoTouch.Foundation.NSObjectFlag t);
	public MDLTexture (IntPtr handle);
	public MDLTexture (MonoTouch.Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, int rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public virtual uint ChannelCount { get; }
	public virtual MDLTextureChannelEncoding ChannelEncoding { get; }
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2i Dimensions { get; }
	public virtual bool IsCube { get; }
	public virtual uint MipLevelCount { get; }
	public virtual string Name { get; set; }
	public virtual int RowStride { get; }
	// methods
	public static MDLTexture CreateIrradianceTextureCube (MDLTexture texture, string name, OpenTK.Vector2i dimensions);
	public static MDLTexture CreateIrradianceTextureCubeWithConvolution (MDLTexture reflectiveTexture, string name, OpenTK.Vector2i dimensions, float roughness);
	public static MDLTexture CreateTextureCube (string[] imageNames);
	public static MDLTexture CreateTextureCube (string[] imageNames, MonoTouch.Foundation.NSBundle bundleOrNil);
	public static MDLTexture FromBundle (string name, MonoTouch.Foundation.NSBundle bundleOrNil);
	public static MDLTexture FromBundle (string name);
	public virtual MonoTouch.Foundation.NSData GetTexelDataWithBottomLeftOrigin ();
	public virtual MonoTouch.Foundation.NSData GetTexelDataWithBottomLeftOriginAtMipLevel (int mipLevel, bool create);
	public virtual MonoTouch.Foundation.NSData GetTexelDataWithTopLeftOrigin ();
	public virtual MonoTouch.Foundation.NSData GetTexelDataWithTopLeftOriginAtMipLevel (int mipLevel, bool create);
	public virtual bool WriteToFile (string path, bool atomically);
	public virtual bool WriteToUrl (MonoTouch.Foundation.NSUrl url, bool atomically);
}
</pre>

### New Type MonoTouch.ModelIO.MDLTextureChannelEncoding

<pre style='color: green'>
[Serializable]
public enum MDLTextureChannelEncoding {
	Float16 = 258,
	Float32 = 260,
	UInt16 = 2,
	UInt24 = 3,
	UInt32 = 4,
	UInt8 = 1,
}
</pre>

### New Type MonoTouch.ModelIO.MDLTextureFilter

<pre style='color: green'>
public class MDLTextureFilter : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLTextureFilter ();
	public MDLTextureFilter (MonoTouch.Foundation.NSCoder coder);
	public MDLTextureFilter (MonoTouch.Foundation.NSObjectFlag t);
	public MDLTextureFilter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialTextureFilterMode MagFilter { get; set; }
	public virtual MDLMaterialTextureFilterMode MinFilter { get; set; }
	public virtual MDLMaterialMipMapFilterMode MipFilter { get; set; }
	public virtual MDLMaterialTextureWrapMode RWrapMode { get; set; }
	public virtual MDLMaterialTextureWrapMode SWrapMode { get; set; }
	public virtual MDLMaterialTextureWrapMode TWrapMode { get; set; }
}
</pre>

### New Type MonoTouch.ModelIO.MDLTextureSampler

<pre style='color: green'>
public class MDLTextureSampler : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLTextureSampler ();
	public MDLTextureSampler (MonoTouch.Foundation.NSCoder coder);
	public MDLTextureSampler (MonoTouch.Foundation.NSObjectFlag t);
	public MDLTextureSampler (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLTextureFilter HardwareFilter { get; set; }
	public virtual MDLTexture Texture { get; set; }
	public virtual MDLTransform Transform { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ModelIO.MDLTransform

<pre style='color: green'>
public class MDLTransform : MonoTouch.Foundation.NSObject, IMDLComponent, IMDLTransformComponent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLTransform ();
	public MDLTransform (MonoTouch.Foundation.NSCoder coder);
	public MDLTransform (MonoTouch.Foundation.NSObjectFlag t);
	public MDLTransform (IntPtr handle);
	public MDLTransform (IMDLTransformComponent component);
	public MDLTransform (OpenTK.Matrix4 matrix);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Matrix4 Matrix { get; set; }
	public virtual double MaximumTime { get; }
	public virtual double MinimumTime { get; }
	public virtual OpenTK.Vector3 Rotation { get; set; }
	public virtual OpenTK.Vector3 Scale { get; set; }
	public virtual OpenTK.Vector3 Translation { get; set; }
	// methods
	public static OpenTK.Matrix4 GlobalTransformWithObject (MDLObject obj, double time);
	public virtual OpenTK.Matrix4 LocalTransformAtTime (double time);
	public virtual OpenTK.Vector3 RotationAtTime (double time);
	public virtual OpenTK.Vector3 ScaleAtTime (double time);
	public virtual void SetIdentity ();
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform);
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform, double time);
	public virtual void SetRotation (OpenTK.Vector3 rotation, double time);
	public virtual void SetScale (OpenTK.Vector3 scale, double time);
	public virtual void SetTranslation (OpenTK.Vector3 translation, double time);
	public virtual OpenTK.Vector3 TranslationAtTime (double time);
}
</pre>

### New Type MonoTouch.ModelIO.MDLTransformComponent

<pre style='color: green'>
public abstract class MDLTransformComponent : MonoTouch.Foundation.NSObject, IMDLTransformComponent, IMDLComponent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLTransformComponent ();
	public MDLTransformComponent (MonoTouch.Foundation.NSCoder coder);
	public MDLTransformComponent (MonoTouch.Foundation.NSObjectFlag t);
	public MDLTransformComponent (IntPtr handle);
	// properties
	public virtual OpenTK.Matrix4 Matrix { get; set; }
	public virtual double MaximumTime { get; }
	public virtual double MinimumTime { get; }
	// methods
	public static OpenTK.Matrix4 GlobalTransformWithObject (MDLObject obj, double time);
	public virtual OpenTK.Matrix4 LocalTransformAtTime (double time);
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform, double time);
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform);
}
</pre>

### New Type MonoTouch.ModelIO.MDLTransformComponent_Extensions

<pre style='color: green'>
public static class MDLTransformComponent_Extensions {
	// methods
	public static OpenTK.Matrix4 LocalTransformAtTime (IMDLTransformComponent This, double time);
	public static void SetLocalTransform (IMDLTransformComponent This, OpenTK.Matrix4 transform, double time);
	public static void SetLocalTransform (IMDLTransformComponent This, OpenTK.Matrix4 transform);
}
</pre>

### New Type MonoTouch.ModelIO.MDLVertexAttribute

<pre style='color: green'>
public class MDLVertexAttribute : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLVertexAttribute ();
	public MDLVertexAttribute (MonoTouch.Foundation.NSCoder coder);
	public MDLVertexAttribute (MonoTouch.Foundation.NSObjectFlag t);
	public MDLVertexAttribute (IntPtr handle);
	public MDLVertexAttribute (string name, MDLVertexFormat format, uint offset, uint bufferIndex);
	// properties
	public virtual uint BufferIndex { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLVertexFormat Format { get; set; }
	public virtual OpenTK.Vector4 InitializationValue { get; set; }
	public virtual string Name { get; set; }
	public virtual uint Offset { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
</pre>

### New Type MonoTouch.ModelIO.MDLVertexAttributeData

<pre style='color: green'>
public class MDLVertexAttributeData : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLVertexAttributeData (MonoTouch.Foundation.NSCoder coder);
	public MDLVertexAttributeData (MonoTouch.Foundation.NSObjectFlag t);
	public MDLVertexAttributeData (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IntPtr DataStart { get; set; }
	public virtual MDLVertexFormat Format { get; set; }
	public virtual MonoTouch.Foundation.NSData MappedData { get; set; }
	public virtual uint Stride { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ModelIO.MDLVertexDescriptor

<pre style='color: green'>
public class MDLVertexDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MDLVertexDescriptor ();
	public MDLVertexDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MDLVertexDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MDLVertexDescriptor (IntPtr handle);
	public MDLVertexDescriptor (MDLVertexDescriptor vertexDescriptor);
	// properties
	public virtual MonoTouch.Foundation.NSMutableArray Attributes { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSMutableArray Layouts { get; set; }
	// methods
	public virtual void AddOrReplaceAttribute (MDLVertexAttribute attribute);
	public virtual MDLVertexAttribute AttributeNamed (string name);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
	public virtual void SetPackedOffsets ();
	public virtual void SetPackedStrides ();
}
</pre>

### New Type MonoTouch.ModelIO.MDLVertexFormat

<pre style='color: green'>
[Serializable]
public enum MDLVertexFormat {
	Char = 131073,
	Char2 = 131074,
	Char2Normalized = 262146,
	Char3 = 131075,
	Char3Normalized = 262147,
	Char4 = 131076,
	Char4Normalized = 262148,
	CharNormalized = 262145,
	Float = 786433,
	Float2 = 786434,
	Float3 = 786435,
	Float4 = 786436,
	Half = 720897,
	Half2 = 720898,
	Half3 = 720899,
	Half4 = 720900,
	Int = 655361,
	Int1010102Normalized = 4100,
	Int2 = 655362,
	Int3 = 655363,
	Int4 = 655364,
	Invalid = 0,
	Short = 393217,
	Short2 = 393218,
	Short2Normalized = 524290,
	Short3 = 393219,
	Short3Normalized = 524291,
	Short4 = 393220,
	Short4Normalized = 524292,
	ShortNormalized = 524289,
	UChar = 65537,
	UChar2 = 65538,
	UChar2Normalized = 196610,
	UChar3 = 65539,
	UChar3Normalized = 196611,
	UChar4 = 65540,
	UChar4Normalized = 196612,
	UCharNormalized = 196609,
	UInt = 589825,
	UInt1010102Normalized = 8196,
	UInt2 = 589826,
	UInt3 = 589827,
	UInt4 = 589828,
	UShort = 327681,
	UShort2 = 327682,
	UShort2Normalized = 458754,
	UShort3 = 327683,
	UShort3Normalized = 458755,
	UShort4 = 327684,
	UShort4Normalized = 458756,
	UShortNormalized = 458753,
}
</pre>

## New Namespace MonoTouch.ReplayKit

### New Type MonoTouch.ReplayKit.IRPPreviewViewControllerDelegate

<pre style='color: green'>
public interface IRPPreviewViewControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.ReplayKit.IRPScreenRecorderDelegate

<pre style='color: green'>
public interface IRPScreenRecorderDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.ReplayKit.RPPreviewViewController

<pre style='color: green'>
public class RPPreviewViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAppearanceContainer, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public RPPreviewViewController ();
	public RPPreviewViewController (MonoTouch.Foundation.NSCoder coder);
	public RPPreviewViewController (MonoTouch.Foundation.NSObjectFlag t);
	public RPPreviewViewController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IRPPreviewViewControllerDelegate PreviewControllerDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.ReplayKit.RPPreviewViewControllerDelegate

<pre style='color: green'>
public class RPPreviewViewControllerDelegate : MonoTouch.Foundation.NSObject, IRPPreviewViewControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public RPPreviewViewControllerDelegate ();
	public RPPreviewViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public RPPreviewViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public RPPreviewViewControllerDelegate (IntPtr handle);
	// methods
	public virtual void PreviewControllerDidFinish (RPPreviewViewController previewController);
}
</pre>

### New Type MonoTouch.ReplayKit.RPPreviewViewControllerDelegate_Extensions

<pre style='color: green'>
public static class RPPreviewViewControllerDelegate_Extensions {
	// methods
	public static void PreviewControllerDidFinish (IRPPreviewViewControllerDelegate This, RPPreviewViewController previewController);
}
</pre>

### New Type MonoTouch.ReplayKit.RPScreenRecorder

<pre style='color: green'>
public class RPScreenRecorder : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public RPScreenRecorder (MonoTouch.Foundation.NSCoder coder);
	public RPScreenRecorder (MonoTouch.Foundation.NSObjectFlag t);
	public RPScreenRecorder (IntPtr handle);
	// properties
	public virtual bool Available { get; }
	public override IntPtr ClassHandle { get; }
	public virtual IRPScreenRecorderDelegate Delegate { get; set; }
	public virtual bool MicrophoneEnabled { get; }
	public virtual bool Recording { get; }
	public static RPScreenRecorder SharedRecorder { get; }
	// methods
	public virtual void DiscardRecording (System.Action handler);
	public virtual System.Threading.Tasks.Task DiscardRecordingAsync ();
	protected override void Dispose (bool disposing);
	public virtual void StartRecording (bool microphoneEnabled, System.Action&lt;MonoTouch.Foundation.NSError&gt; handler);
	public virtual System.Threading.Tasks.Task StartRecordingAsync (bool microphoneEnabled);
	public virtual void StopRecording (System.Action&lt;MonoTouch.Foundation.NSError&gt; handler);
	public virtual System.Threading.Tasks.Task StopRecordingAsync ();
}
</pre>

### New Type MonoTouch.ReplayKit.RPScreenRecorderDelegate

<pre style='color: green'>
public class RPScreenRecorderDelegate : MonoTouch.Foundation.NSObject, IRPScreenRecorderDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public RPScreenRecorderDelegate ();
	public RPScreenRecorderDelegate (MonoTouch.Foundation.NSCoder coder);
	public RPScreenRecorderDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public RPScreenRecorderDelegate (IntPtr handle);
	// methods
	public virtual void DidChangeAvailability (RPScreenRecorder screenRecorder);
	public virtual void DidStopRecording (RPScreenRecorder screenRecorder, MonoTouch.Foundation.NSError error, RPPreviewViewController previewViewController);
}
</pre>

### New Type MonoTouch.ReplayKit.RPScreenRecorderDelegate_Extensions

<pre style='color: green'>
public static class RPScreenRecorderDelegate_Extensions {
	// methods
	public static void DidChangeAvailability (IRPScreenRecorderDelegate This, RPScreenRecorder screenRecorder);
	public static void DidStopRecording (IRPScreenRecorderDelegate This, RPScreenRecorder screenRecorder, MonoTouch.Foundation.NSError error, RPPreviewViewController previewViewController);
}
</pre>

## New Namespace MonoTouch.WatchConnectivity

### New Type MonoTouch.WatchConnectivity.IWCSessionDelegate

<pre style='color: green'>
public interface IWCSessionDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCErrorCode

<pre style='color: green'>
[Serializable]
public enum WCErrorCode {
	DeviceNotPaired = 7005,
	FileAccessDenied = 7013,
	GenericError = 7001,
	InvalidParameter = 7008,
	MessageReplyFailed = 7011,
	MessageReplyTimedOut = 7012,
	NotReachable = 7007,
	PayloadTooLarge = 7009,
	PayloadUnsupportedTypes = 7010,
	SessionMissingDelegate = 7003,
	SessionNotActivated = 7004,
	SessionNotSupported = 7002,
	WatchAppNotInstalled = 7006,
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCSession

<pre style='color: green'>
public class WCSession : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WCSession (MonoTouch.Foundation.NSCoder coder);
	public WCSession (MonoTouch.Foundation.NSObjectFlag t);
	public WCSession (IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSDictionary ApplicationContext { get; }
	public override IntPtr ClassHandle { get; }
	public virtual bool ComplicationEnabled { get; }
	public static WCSession DefaultSession { get; }
	public virtual IWCSessionDelegate Delegate { get; set; }
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	public static bool IsSupported { get; }
	public virtual WCSessionFileTransfer[] OutstandingFileTransfers { get; }
	public virtual WCSessionUserInfoTransfer[] OutstandingUserInfoTransfers { get; }
	public virtual bool Paired { get; }
	public virtual bool Reachable { get; }
	public virtual MonoTouch.Foundation.NSDictionary ReceivedApplicationContext { get; }
	public virtual bool WatchAppInstalled { get; }
	public virtual MonoTouch.Foundation.NSUrl WatchDirectoryUrl { get; }
	// methods
	public virtual void ActivateSession ();
	protected override void Dispose (bool disposing);
	public virtual void SendMessage (MonoTouch.Foundation.NSData data, WCSessionReplyDataHandler replyHandler, System.Action&lt;MonoTouch.Foundation.NSError&gt; errorHandler);
	public virtual void SendMessage (MonoTouch.Foundation.NSDictionary message, WCSessionReplyHandler replyHandler, System.Action&lt;MonoTouch.Foundation.NSError&gt; errorHandler);
	public virtual WCSessionUserInfoTransfer TransferCurrentComplicationUserInfo (MonoTouch.Foundation.NSDictionary userInfo);
	public virtual WCSessionFileTransfer TransferFile (MonoTouch.Foundation.NSUrl file, MonoTouch.Foundation.NSDictionary metadata);
	public virtual WCSessionUserInfoTransfer TransferUserInfo (MonoTouch.Foundation.NSDictionary userInfo);
	public virtual bool UpdateApplicationContext (MonoTouch.Foundation.NSDictionary applicationContext, out MonoTouch.Foundation.NSError error);
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCSessionDelegate

<pre style='color: green'>
public class WCSessionDelegate : MonoTouch.Foundation.NSObject, IWCSessionDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WCSessionDelegate ();
	public WCSessionDelegate (MonoTouch.Foundation.NSCoder coder);
	public WCSessionDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public WCSessionDelegate (IntPtr handle);
	// methods
	public virtual void DidFinishFileTransfer (WCSession session, WCSessionFileTransfer fileTransfer, MonoTouch.Foundation.NSError error);
	public virtual void DidFinishUserInfoTransfer (WCSession session, WCSessionUserInfoTransfer userInfoTransfer, MonoTouch.Foundation.NSError error);
	public virtual void DidReceiveApplicationContext (WCSession session, MonoTouch.Foundation.NSDictionary applicationContext);
	public virtual void DidReceiveFile (WCSession session, WCSessionFile file);
	public virtual void DidReceiveMessage (WCSession session, MonoTouch.Foundation.NSDictionary message, WCSessionReplyHandler replyHandler);
	public virtual void DidReceiveMessage (WCSession session, MonoTouch.Foundation.NSDictionary message);
	public virtual void DidReceiveMessageData (WCSession session, MonoTouch.Foundation.NSData messageData);
	public virtual void DidReceiveMessageData (WCSession session, MonoTouch.Foundation.NSData messageData, WCSessionReplyDataHandler replyHandler);
	public virtual void DidReceiveUserInfo (WCSession session, MonoTouch.Foundation.NSDictionary userInfo);
	public virtual void SessionReachabilityDidChange (WCSession session);
	public virtual void SessionWatchStateDidChange (WCSession session);
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCSessionDelegate_Extensions

<pre style='color: green'>
public static class WCSessionDelegate_Extensions {
	// methods
	public static void DidFinishFileTransfer (IWCSessionDelegate This, WCSession session, WCSessionFileTransfer fileTransfer, MonoTouch.Foundation.NSError error);
	public static void DidFinishUserInfoTransfer (IWCSessionDelegate This, WCSession session, WCSessionUserInfoTransfer userInfoTransfer, MonoTouch.Foundation.NSError error);
	public static void DidReceiveApplicationContext (IWCSessionDelegate This, WCSession session, MonoTouch.Foundation.NSDictionary applicationContext);
	public static void DidReceiveFile (IWCSessionDelegate This, WCSession session, WCSessionFile file);
	public static void DidReceiveMessage (IWCSessionDelegate This, WCSession session, MonoTouch.Foundation.NSDictionary message);
	public static void DidReceiveMessage (IWCSessionDelegate This, WCSession session, MonoTouch.Foundation.NSDictionary message, WCSessionReplyHandler replyHandler);
	public static void DidReceiveMessageData (IWCSessionDelegate This, WCSession session, MonoTouch.Foundation.NSData messageData, WCSessionReplyDataHandler replyHandler);
	public static void DidReceiveMessageData (IWCSessionDelegate This, WCSession session, MonoTouch.Foundation.NSData messageData);
	public static void DidReceiveUserInfo (IWCSessionDelegate This, WCSession session, MonoTouch.Foundation.NSDictionary userInfo);
	public static void SessionReachabilityDidChange (IWCSessionDelegate This, WCSession session);
	public static void SessionWatchStateDidChange (IWCSessionDelegate This, WCSession session);
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCSessionFile

<pre style='color: green'>
public class WCSessionFile : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WCSessionFile (MonoTouch.Foundation.NSCoder coder);
	public WCSessionFile (MonoTouch.Foundation.NSObjectFlag t);
	public WCSessionFile (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSUrl FileUrl { get; }
	public virtual MonoTouch.Foundation.NSDictionary Metadata { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCSessionFileTransfer

<pre style='color: green'>
public class WCSessionFileTransfer : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WCSessionFileTransfer (MonoTouch.Foundation.NSCoder coder);
	public WCSessionFileTransfer (MonoTouch.Foundation.NSObjectFlag t);
	public WCSessionFileTransfer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual WCSessionFile File { get; }
	public virtual bool Transferring { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCSessionReplyDataHandler

<pre style='color: green'>
public sealed delegate WCSessionReplyDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public WCSessionReplyDataHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSData replyMessage, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSData replyMessage);
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCSessionReplyHandler

<pre style='color: green'>
public sealed delegate WCSessionReplyHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public WCSessionReplyHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSDictionary replyMessage, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSDictionary replyMessage);
}
</pre>

### New Type MonoTouch.WatchConnectivity.WCSessionUserInfoTransfer

<pre style='color: green'>
public class WCSessionUserInfoTransfer : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WCSessionUserInfoTransfer (MonoTouch.Foundation.NSCoder coder);
	public WCSessionUserInfoTransfer (MonoTouch.Foundation.NSObjectFlag t);
	public WCSessionUserInfoTransfer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool CurrentComplicationInfo { get; }
	public virtual bool Transferring { get; }
	public virtual MonoTouch.Foundation.NSDictionary UserInfo { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
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

### Type Changed: AudioToolbox.AudioFormatType

Added value:

<pre style='color: green'>
	EnhancedAES3 = 1700998451,
</pre>

### Type Changed: AudioToolbox.AudioQueue

Added method:

<pre style='color: green'>
	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, AudioStreamPacketDescription[] desc);
</pre>

### Type Changed: AudioToolbox.AudioTimeStamp

### Type Changed: AudioToolbox.AudioTimeStamp.AtsFlags

Added field:

<pre style='color: green'>
	public static const AudioTimeStamp.AtsFlags NothingValid;
</pre>

### Type Changed: AudioToolbox.SmpteTime

Added properties:

<pre style='color: green'>
	public SmpteTimeFlags FlagsStrong { get; set; }
	public SmpteTimeType TypeStrong { get; set; }
</pre>

### New Type AudioToolbox.MPEG4ObjectID

<pre style='color: green'>
[Serializable]
public enum MPEG4ObjectID {
	AacLc = 2,
	AacMain = 1,
}
</pre>

### New Type AudioToolbox.SmpteTimeFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum SmpteTimeFlags {
	TimeRunning = 2,
	TimeValid = 1,
	Unknown = 0,
}
</pre>

## Namespace AudioUnit

### Type Changed: AudioUnit.AudioTypeConverter

Added value:

<pre style='color: green'>
	MultiSplitter = 1836281964,
</pre>

### Type Changed: AudioUnit.AudioUnit

Obsoleted methods:

```
[Obsolete ("Use SetFormat instead as it has the ability of returning a status code"]
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

### New Type AudioUnit.AUAudioUnit

<pre style='color: green'>
public class AUAudioUnit : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected AUAudioUnit (Foundation.NSObjectFlag t);
	protected AUAudioUnit (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void RequestViewController (System.Action&lt;CoreAudioKit.AUViewController&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;CoreAudioKit.AUViewController&gt; RequestViewControllerAsync ();
}
</pre>

## Namespace AVFoundation

### Type Changed: AVFoundation.AVAsset

Added property:

<pre style='color: green'>
	public virtual int UnusedTrackId { get; }
</pre>

Removed method:

<pre style='color: red'>
	public virtual AVMetadataItem[] ChapterMetadataGroups (Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
</pre>

Added method:

<pre style='color: green'>
	public virtual AVTimedMetadataGroup[] ChapterMetadataGroups (Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
</pre>

### Type Changed: AVFoundation.AVAssetTrack

Removed method:

<pre style='color: red'>
	public virtual Foundation.NSString GetAssociatedTracksOfType (Foundation.NSString avAssetTrackTrackAssociationType);
</pre>

Added method:

<pre style='color: green'>
	public virtual AVAssetTrack[] GetAssociatedTracksOfType (Foundation.NSString avAssetTrackTrackAssociationType);
</pre>

### Type Changed: AVFoundation.AVAudioChannelLayout

Added constructor:

<pre style='color: green'>
	public AVAudioChannelLayout (Foundation.NSCoder coder);
</pre>

Added interfaces:

<pre style='color: green'>
	Foundation.INSCoding
	Foundation.INSSecureCoding
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

### Type Changed: AVFoundation.AVAudioFormat

Added constructor:

<pre style='color: green'>
	public AVAudioFormat (Foundation.NSCoder coder);
</pre>

Added interfaces:

<pre style='color: green'>
	Foundation.INSCoding
	Foundation.INSSecureCoding
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

### Type Changed: AVFoundation.AVCompositionTrackSegment

Added property:

<pre style='color: green'>
	public virtual bool Empty { get; }
</pre>

### Type Changed: AVFoundation.AVTextStyleRule

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public AVTextStyleRule ();
```

## Namespace AVKit

### Type Changed: AVKit.AVPlayerViewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

Added properties:

<pre style='color: green'>
	public virtual bool AllowsPictureInPicturePlayback { get; set; }
	public IAVPlayerViewControllerDelegate Delegate { get; set; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
</pre>

### New Type AVKit.AVPictureInPictureController

<pre style='color: green'>
public class AVPictureInPictureController : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected AVPictureInPictureController (Foundation.NSObjectFlag t);
	protected AVPictureInPictureController (IntPtr handle);
	public AVPictureInPictureController (AVFoundation.AVPlayerLayer playerLayer);
	// properties
	public override IntPtr ClassHandle { get; }
	public IAVPictureInPictureControllerDelegate Delegate { get; set; }
	public static bool IsPictureInPictureSupported { get; }
	public virtual bool PictureInPictureActive { get; }
	public virtual bool PictureInPicturePossible { get; }
	public virtual bool PictureInPictureSuspended { get; }
	public virtual AVFoundation.AVPlayerLayer PlayerLayer { get; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void StartPictureInPicture ();
	public virtual void StopPictureInPicture ();
}
</pre>

### New Type AVKit.AVPictureInPictureControllerDelegate

<pre style='color: green'>
public class AVPictureInPictureControllerDelegate : Foundation.NSObject, IAVPictureInPictureControllerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public AVPictureInPictureControllerDelegate ();
	protected AVPictureInPictureControllerDelegate (Foundation.NSObjectFlag t);
	protected AVPictureInPictureControllerDelegate (IntPtr handle);
	// methods
	public virtual void DidStartPictureInPicture (AVPictureInPictureController pictureInPictureController);
	public virtual void DidStopPictureInPicture (AVPictureInPictureController pictureInPictureController);
	public virtual void FailedToStartPictureInPicture (AVPictureInPictureController pictureInPictureController, Foundation.NSError error);
	public virtual void RestoreUserInterfaceForPictureInPicture (AVPictureInPictureController pictureInPictureController, System.Action&lt;bool&gt; completionHandler);
	public virtual void WillStartPictureInPicture (AVPictureInPictureController pictureInPictureController);
	public virtual void WillStopPictureInPicture (AVPictureInPictureController pictureInPictureController);
}
</pre>

### New Type AVKit.AVPictureInPictureControllerDelegate_Extensions

<pre style='color: green'>
public static class AVPictureInPictureControllerDelegate_Extensions {
	// methods
	public static void DidStartPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController);
	public static void DidStopPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController);
	public static void FailedToStartPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController, Foundation.NSError error);
	public static void RestoreUserInterfaceForPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController, System.Action&lt;bool&gt; completionHandler);
	public static void WillStartPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController);
	public static void WillStopPictureInPicture (IAVPictureInPictureControllerDelegate This, AVPictureInPictureController pictureInPictureController);
}
</pre>

### New Type AVKit.AVPlayerViewControllerDelegate

<pre style='color: green'>
public class AVPlayerViewControllerDelegate : Foundation.NSObject, IAVPlayerViewControllerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public AVPlayerViewControllerDelegate ();
	protected AVPlayerViewControllerDelegate (Foundation.NSObjectFlag t);
	protected AVPlayerViewControllerDelegate (IntPtr handle);
	// methods
	public virtual void DidStartPictureInPicture (AVPlayerViewController playerViewController);
	public virtual void DidStopPictureInPicture (AVPlayerViewController playerViewController);
	public virtual void FailedToStartPictureInPicture (AVPlayerViewController playerViewController, Foundation.NSError error);
	public virtual void RestoreUserInterfaceForPictureInPicture (AVPlayerViewController playerViewController, System.Action&lt;bool&gt; completionHandler);
	public virtual bool ShouldAutomaticallyDismissAtPictureInPictureStart (AVPlayerViewController playerViewController);
	public virtual void WillStartPictureInPicture (AVPlayerViewController playerViewController);
	public virtual void WillStopPictureInPicture (AVPlayerViewController playerViewController);
}
</pre>

### New Type AVKit.AVPlayerViewControllerDelegate_Extensions

<pre style='color: green'>
public static class AVPlayerViewControllerDelegate_Extensions {
	// methods
	public static void DidStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
	public static void DidStopPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
	public static void FailedToStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, Foundation.NSError error);
	public static void RestoreUserInterfaceForPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, System.Action&lt;bool&gt; completionHandler);
	public static bool ShouldAutomaticallyDismissAtPictureInPictureStart (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
	public static void WillStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
	public static void WillStopPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);
}
</pre>

### New Type AVKit.IAVPictureInPictureControllerDelegate

<pre style='color: green'>
public interface IAVPictureInPictureControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type AVKit.IAVPlayerViewControllerDelegate

<pre style='color: green'>
public interface IAVPlayerViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

## Namespace CloudKit

### Type Changed: CloudKit.CKRecordID

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public CKRecordID ();
```

### Type Changed: CloudKit.CKRecordZoneID

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public CKRecordZoneID ();
```

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

### New Type CoreAnimation.CASpringAnimation

<pre style='color: green'>
public class CASpringAnimation : CoreAnimation.CABasicAnimation, ICAAction, ICAMediaTiming, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CASpringAnimation ();
	public CASpringAnimation (Foundation.NSCoder coder);
	protected CASpringAnimation (Foundation.NSObjectFlag t);
	protected CASpringAnimation (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nfloat Damping { get; set; }
	public virtual nfloat InitialVelocity { get; set; }
	public virtual nfloat Mass { get; set; }
	public virtual double SettlingDuration { get; }
	public virtual nfloat Stiffness { get; set; }
	// methods
	public static CABasicAnimation FromKeyPath (string path);
}
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

### New Type CoreAudioKit.AUViewController

<pre style='color: green'>
public class AUViewController : UIKit.UIViewController, System.Collections.IEnumerable, Foundation.INSCoding, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public AUViewController ();
	public AUViewController (Foundation.NSCoder coder);
	protected AUViewController (Foundation.NSObjectFlag t);
	protected AUViewController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

## Namespace CoreBluetooth

### Type Changed: CoreBluetooth.CBPeer

Removed constructor:

<pre style='color: red'>
	public CBPeer ();
</pre>

## Namespace CoreData

### Type Changed: CoreData.NSManagedObjectContext

Added method:

<pre style='color: green'>
	public virtual NSManagedObject GetExistingObject (NSManagedObjectID objectID, out Foundation.NSError error);
</pre>

## Namespace CoreFoundation

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
[Obsolete ("Use a real `null` value instead of this managed wrapper over a null native instance"]
	public static CGColorSpace Null;
```

Added methods:

<pre style='color: green'>
	public static CGColorSpace CreateAdobeRGB1988 ();
	public static CGColorSpace CreateGenericCMYK ();
	public static CGColorSpace CreateGenericGray ();
	public static CGColorSpace CreateGenericGrayGamma2_2 ();
	public static CGColorSpace CreateGenericRGB ();
	public static CGColorSpace CreateGenericRGBLinear ();
	public static CGColorSpace CreateSRGB ();
</pre>

### New Type CoreGraphics.CGColorSpaceNames

<pre style='color: green'>
public static class CGColorSpaceNames {
	// properties
	public static Foundation.NSString AdobeRGB1998 { get; }
	public static Foundation.NSString GenericCMYK { get; }
	public static Foundation.NSString GenericGray { get; }
	public static Foundation.NSString GenericGrayGamma2_2 { get; }
	public static Foundation.NSString GenericRGB { get; }
	public static Foundation.NSString GenericRGBLinear { get; }
	public static Foundation.NSString SRGB { get; }
}
</pre>

## Namespace CoreImage

### Type Changed: CoreImage.CIAccordionFoldTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAdditionCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAffineClamp

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAffineFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAffineTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAffineTransform

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAreaHistogram

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAztecCodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>CoreImage.CIFilter</span></span>

 <span style='color:green'>CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public Foundation.NSData Message { get; set; }
</pre>

### Type Changed: CoreImage.CIBarsSwipeTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBlendFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBlendWithAlphaMask

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBlendWithMask

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBloom

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBumpDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBumpDistortionLinear

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICheckerboardGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICircleSplashDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICircularScreen

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICode128BarcodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>CoreImage.CIFilter</span></span>

 <span style='color:green'>CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public Foundation.NSData Message { get; set; }
</pre>

### Type Changed: CoreImage.CIColor

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorBurnBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorClamp

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorControls

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorCrossPolynomial

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorCube

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorCubeWithColorSpace

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorDodgeBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorInvert

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorMap

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorMatrix

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorMonochrome

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorPolynomial

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorPosterize

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICompositingFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConstantColorGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolution3X3

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolution5X5

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolution9Horizontal

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolution9Vertical

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolutionCore

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICopyMachineTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICrop

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDarkenBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDifferenceBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDisintegrateWithMaskTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDissolveTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDistortionFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDivideBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDotScreen

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIEightfoldReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIExclusionBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIExposureAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFaceBalance

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFalseColor

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFilterAttributes

Added property:

<pre style='color: green'>
	public static Foundation.NSString TypeColor { get; }
</pre>

### Type Changed: CoreImage.CIFlashTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFourfoldReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFourfoldRotatedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFourfoldTranslatedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGammaAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGaussianBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGaussianGradient

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGlassDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGlideReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGloom

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHardLightBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHatchedScreen

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHighlightShadowAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHistogramDisplayFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHoleDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHueAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHueBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIImage

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILanczosScaleTransform

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILightenBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILightTunnel

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILinearBurnBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILinearDodgeBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILinearGradient

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILinearToSRGBToneCurve

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILineScreen

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILuminosityBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMaskToAlpha

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMaximumComponent

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMaximumCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMinimumComponent

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMinimumCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIModTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMotionBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMultiplyBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMultiplyCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIOverlayBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPerspectiveCorrection

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPerspectiveTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPerspectiveTransform

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPerspectiveTransformWithExtent

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffect

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectChrome

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectFade

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectInstant

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectMono

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectNoir

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectProcess

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectTonal

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectTransfer

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPinchDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPinLightBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPixellate

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIQRCodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>CoreImage.CIFilter</span></span>

 <span style='color:green'>CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public Foundation.NSData Message { get; set; }
</pre>

### Type Changed: CoreImage.CIRadialGradient

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIRandomGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISaturationBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIScreenBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIScreenFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISepiaTone

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISharpenLuminance

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISixfoldReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISixfoldRotatedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISmoothLinearGradient

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISoftLightBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISourceAtopCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISourceInCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISourceOutCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISourceOverCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISRGBToneCurveToLinear

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIStarShineGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIStraightenFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIStripesGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISubtractBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISwipeTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITemperatureAndTint

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITileFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIToneCurve

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITransitionFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITriangleKaleidoscope

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITwelvefoldReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITwirlDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIUnsharpMask

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVector

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVibrance

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVignette

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVignetteEffect

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVortexDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIWhitePointAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIZoomBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### New Type CoreImage.CIAreaAverage

<pre style='color: green'>
public class CIAreaAverage : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIAreaAverage ();
	public CIAreaAverage (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type CoreImage.CIAreaMaximum

<pre style='color: green'>
public class CIAreaMaximum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMaximum ();
	public CIAreaMaximum (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type CoreImage.CIAreaMaximumAlpha

<pre style='color: green'>
public class CIAreaMaximumAlpha : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMaximumAlpha ();
	public CIAreaMaximumAlpha (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type CoreImage.CIAreaMinimum

<pre style='color: green'>
public class CIAreaMinimum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMinimum ();
	public CIAreaMinimum (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type CoreImage.CIAreaMinimumAlpha

<pre style='color: green'>
public class CIAreaMinimumAlpha : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMinimumAlpha ();
	public CIAreaMinimumAlpha (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type CoreImage.CIBoxBlur

<pre style='color: green'>
public class CIBoxBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIBoxBlur ();
	public CIBoxBlur (IntPtr handle);
}
</pre>

### New Type CoreImage.CICircularWrap

<pre style='color: green'>
public class CICircularWrap : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CICircularWrap ();
	public CICircularWrap (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
</pre>

### New Type CoreImage.CICMYKHalftone

<pre style='color: green'>
public class CICMYKHalftone : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CICMYKHalftone ();
	public CICMYKHalftone (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float GrayComponentReplacement { get; set; }
	public float InputSharpness { get; set; }
	public float UnderColorRemoval { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type CoreImage.CICodeGenerator

<pre style='color: green'>
public abstract class CICodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CICodeGenerator (string name);
	public CICodeGenerator (IntPtr handle);
	// properties
	public Foundation.NSData Message { get; set; }
}
</pre>

### New Type CoreImage.CIColumnAverage

<pre style='color: green'>
public class CIColumnAverage : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIColumnAverage ();
	public CIColumnAverage (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type CoreImage.CIComicEffect

<pre style='color: green'>
public class CIComicEffect : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIComicEffect ();
	public CIComicEffect (IntPtr handle);
}
</pre>

### New Type CoreImage.CIConvolution7X7

<pre style='color: green'>
public class CIConvolution7X7 : CoreImage.CIConvolutionCore, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIConvolution7X7 ();
	public CIConvolution7X7 (IntPtr handle);
}
</pre>

### New Type CoreImage.CICrystallize

<pre style='color: green'>
public class CICrystallize : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CICrystallize ();
	public CICrystallize (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
</pre>

### New Type CoreImage.CIDepthOfField

<pre style='color: green'>
public class CIDepthOfField : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIDepthOfField ();
	public CIDepthOfField (IntPtr handle);
	// properties
	public CIVector Point1 { get; set; }
	public CIVector Point2 { get; set; }
	public float Radius { get; set; }
	public float Saturation { get; set; }
	public float UnsharpMaskIntensity { get; set; }
	public float UnsharpMaskRadius { get; set; }
}
</pre>

### New Type CoreImage.CIDiscBlur

<pre style='color: green'>
public class CIDiscBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIDiscBlur ();
	public CIDiscBlur (IntPtr handle);
}
</pre>

### New Type CoreImage.CIDisplacementDistortion

<pre style='color: green'>
public class CIDisplacementDistortion : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIDisplacementDistortion ();
	public CIDisplacementDistortion (IntPtr handle);
	// properties
	public float Scale { get; set; }
}
</pre>

### New Type CoreImage.CIDroste

<pre style='color: green'>
public class CIDroste : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIDroste ();
	public CIDroste (IntPtr handle);
	// properties
	public CIVector InsetPoint0 { get; set; }
	public CIVector InsetPoint1 { get; set; }
	public float Periodicity { get; set; }
	public float Rotation { get; set; }
	public float Strands { get; set; }
	public float Zoom { get; set; }
}
</pre>

### New Type CoreImage.CIEdges

<pre style='color: green'>
public class CIEdges : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIEdges ();
	public CIEdges (IntPtr handle);
}
</pre>

### New Type CoreImage.CIEdgeWork

<pre style='color: green'>
public class CIEdgeWork : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIEdgeWork ();
	public CIEdgeWork (IntPtr handle);
}
</pre>

### New Type CoreImage.CIGlassLozenge

<pre style='color: green'>
public class CIGlassLozenge : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIGlassLozenge ();
	public CIGlassLozenge (IntPtr handle);
	// properties
	public CIVector Point0 { get; set; }
	public CIVector Point1 { get; set; }
	public float Radius { get; set; }
	public float Refraction { get; set; }
}
</pre>

### New Type CoreImage.CIHeightFieldFromMask

<pre style='color: green'>
public class CIHeightFieldFromMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIHeightFieldFromMask ();
	public CIHeightFieldFromMask (IntPtr handle);
}
</pre>

### New Type CoreImage.CIHexagonalPixellate

<pre style='color: green'>
public class CIHexagonalPixellate : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIHexagonalPixellate ();
	public CIHexagonalPixellate (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Scale { get; set; }
}
</pre>

### New Type CoreImage.CIKaleidoscope

<pre style='color: green'>
public class CIKaleidoscope : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIKaleidoscope ();
	public CIKaleidoscope (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Count { get; set; }
}
</pre>

### New Type CoreImage.CILenticularHaloGenerator

<pre style='color: green'>
public class CILenticularHaloGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CILenticularHaloGenerator ();
	public CILenticularHaloGenerator (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIColor Color { get; set; }
	public float HaloOverlap { get; set; }
	public float HaloRadius { get; set; }
	public float HaloWidth { get; set; }
	public float StriationContrast { get; set; }
	public float StriationStrength { get; set; }
	public float Time { get; set; }
}
</pre>

### New Type CoreImage.CILineOverlay

<pre style='color: green'>
public class CILineOverlay : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CILineOverlay ();
	public CILineOverlay (IntPtr handle);
	// properties
	public float Contrast { get; set; }
	public float EdgeIntensity { get; set; }
	public float NRNoiseLevel { get; set; }
	public float NRSharpness { get; set; }
	public float Threshold { get; set; }
}
</pre>

### New Type CoreImage.CIMedianFilter

<pre style='color: green'>
public class CIMedianFilter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIMedianFilter ();
	public CIMedianFilter (IntPtr handle);
}
</pre>

### New Type CoreImage.CINoiseReduction

<pre style='color: green'>
public class CINoiseReduction : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CINoiseReduction ();
	public CINoiseReduction (IntPtr handle);
	// properties
	public float NoiseLevel { get; set; }
	public float Sharpness { get; set; }
}
</pre>

### New Type CoreImage.CIOpTile

<pre style='color: green'>
public class CIOpTile : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIOpTile ();
	public CIOpTile (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Scale { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type CoreImage.CIPageCurlTransition

<pre style='color: green'>
public class CIPageCurlTransition : CoreImage.CITransitionFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIPageCurlTransition ();
	public CIPageCurlTransition (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIImage BacksideImage { get; set; }
	public CIVector Extent { get; set; }
	public float Radius { get; set; }
	public CIImage ShadingImage { get; set; }
}
</pre>

### New Type CoreImage.CIPageCurlWithShadowTransition

<pre style='color: green'>
public class CIPageCurlWithShadowTransition : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIPageCurlWithShadowTransition ();
	public CIPageCurlWithShadowTransition (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIImage BacksideImage { get; set; }
	public CIVector Extent { get; set; }
	public float InputTime { get; set; }
	public float Radius { get; set; }
	public float ShadowAmount { get; set; }
	public CIVector ShadowExtent { get; set; }
	public float ShadowSize { get; set; }
	public CIImage TargetImage { get; set; }
}
</pre>

### New Type CoreImage.CIParallelogramTile

<pre style='color: green'>
public class CIParallelogramTile : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIParallelogramTile ();
	public CIParallelogramTile (IntPtr handle);
	// properties
	public float AcuteAngle { get; set; }
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type CoreImage.CIPDF417BarcodeGenerator

<pre style='color: green'>
public class CIPDF417BarcodeGenerator : CoreImage.CICodeGenerator, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIPDF417BarcodeGenerator ();
	public CIPDF417BarcodeGenerator (IntPtr handle);
	// properties
	public int CompactionMode { get; set; }
	public bool CompactStyle { get; set; }
	public int CorrectionLevel { get; set; }
	public int DataColumns { get; set; }
	public float MaxHeight { get; set; }
	public float MaxWidth { get; set; }
	public float MinWidth { get; set; }
	public float PreferredAspectRatio { get; set; }
	public int Rows { get; set; }
}
</pre>

### New Type CoreImage.CIPointillize

<pre style='color: green'>
public class CIPointillize : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIPointillize ();
	public CIPointillize (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
</pre>

### New Type CoreImage.CIRippleTransition

<pre style='color: green'>
public class CIRippleTransition : CoreImage.CITransitionFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIRippleTransition ();
	public CIRippleTransition (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIVector Extent { get; set; }
	public float Scale { get; set; }
	public CIImage ShadingImage { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type CoreImage.CIRowAverage

<pre style='color: green'>
public class CIRowAverage : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIRowAverage ();
	public CIRowAverage (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type CoreImage.CIShadedMaterial

<pre style='color: green'>
public class CIShadedMaterial : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIShadedMaterial ();
	public CIShadedMaterial (IntPtr handle);
	// properties
	public float Scale { get; set; }
	public CIImage ShadingImage { get; set; }
}
</pre>

### New Type CoreImage.CISpotColor

<pre style='color: green'>
public class CISpotColor : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CISpotColor ();
	public CISpotColor (IntPtr handle);
	// properties
	public CIColor CenterColor1 { get; set; }
	public CIColor CenterColor2 { get; set; }
	public CIColor CenterColor3 { get; set; }
	public float Closeness1 { get; set; }
	public float Closeness2 { get; set; }
	public float Closeness3 { get; set; }
	public float Contrast1 { get; set; }
	public float Contrast2 { get; set; }
	public float Contrast3 { get; set; }
	public CIColor ReplacementColor1 { get; set; }
	public CIColor ReplacementColor2 { get; set; }
	public CIColor ReplacementColor3 { get; set; }
}
</pre>

### New Type CoreImage.CISpotLight

<pre style='color: green'>
public class CISpotLight : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CISpotLight ();
	public CISpotLight (IntPtr handle);
	// properties
	public float Brightness { get; set; }
	public CIColor Color { get; set; }
	public float Concentration { get; set; }
	public CIVector LightPointsAt { get; set; }
	public CIVector LightPosition { get; set; }
}
</pre>

### New Type CoreImage.CIStretchCrop

<pre style='color: green'>
public class CIStretchCrop : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CIStretchCrop ();
	public CIStretchCrop (IntPtr handle);
	// properties
	public float CenterStretchAmount { get; set; }
	public float CropAmount { get; set; }
	public CIVector Size { get; set; }
}
</pre>

### New Type CoreImage.CISunbeamsGenerator

<pre style='color: green'>
public class CISunbeamsGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CISunbeamsGenerator ();
	public CISunbeamsGenerator (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIColor Color { get; set; }
	public float CropAmount { get; set; }
	public float MaxStriationRadius { get; set; }
	public float StriationContrast { get; set; }
	public float StriationStrength { get; set; }
	public float SunRadius { get; set; }
	public float Time { get; set; }
}
</pre>

### New Type CoreImage.CITorusLensDistortion

<pre style='color: green'>
public class CITorusLensDistortion : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CITorusLensDistortion ();
	public CITorusLensDistortion (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
	public float Refraction { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type CoreImage.CITriangleTile

<pre style='color: green'>
public class CITriangleTile : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CITriangleTile ();
	public CITriangleTile (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Width { get; set; }
}
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

### Type Changed: CoreMotion.CMPedometer

Added property:

<pre style='color: green'>
	public static bool IsPaceAvailable { get; }
</pre>

### Type Changed: CoreMotion.CMPedometerData

Added property:

<pre style='color: green'>
	public virtual Foundation.NSNumber CurrentPace { get; }
</pre>

### New Type CoreMotion.CMSensorDataList

<pre style='color: green'>
public class CMSensorDataList : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public CMSensorDataList ();
	protected CMSensorDataList (Foundation.NSObjectFlag t);
	protected CMSensorDataList (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type CoreMotion.CMSensorRecorder

<pre style='color: green'>
public class CMSensorRecorder : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public CMSensorRecorder ();
	protected CMSensorRecorder (Foundation.NSObjectFlag t);
	protected CMSensorRecorder (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static bool IsAccelerometerRecordingAvailable { get; }
	// methods
	public virtual CMSensorDataList GetAccelerometerData (Foundation.NSDate fromDate, Foundation.NSDate toDate);
	public virtual CMSensorDataList GetAccelerometerDataSince (ulong identifier);
	public virtual void RecordAccelerometerFor (double duration);
}
</pre>

## Namespace CoreVideo

### Type Changed: CoreVideo.CVImageBuffer

Added properties:

<pre style='color: green'>
	public static Foundation.NSString TransferFunction_ITU_R_2020 { get; }
	public static Foundation.NSString YCbCrMatrix_DCI_P3 { get; }
	public static Foundation.NSString YCbCrMatrix_ITU_R_2020 { get; }
	public static Foundation.NSString YCbCrMatrix_P3_D65 { get; }
</pre>

### Type Changed: CoreVideo.CVPixelBufferPool

Added properties:

<pre style='color: green'>
	public static Foundation.NSString TransferFunction_ITU_R_2020 { get; }
	public static Foundation.NSString YCbCrMatrix_DCI_P3 { get; }
	public static Foundation.NSString YCbCrMatrix_ITU_R_2020 { get; }
	public static Foundation.NSString YCbCrMatrix_P3_D65 { get; }
</pre>

### New Type CoreVideo.CVOpenGLESTextureCache

<pre style='color: green'>
public class CVOpenGLESTextureCache {
	// constructors
	public CVOpenGLESTextureCache ();
}
</pre>

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

### Type Changed: Foundation.NSFormatter

Obsoleted methods:

```
[Obsolete ("Use GetEditingString instead"]
	public virtual string EditingStringFor (NSObject value);
	[Obsolete ("Use GetString instead"]
	public virtual string StringFor (NSObject value);
```

Added methods:

<pre style='color: green'>
	public NSAttributedString GetAttributedString (NSObject obj, UIKit.UIStringAttributes attrs);
	public virtual NSAttributedString GetAttributedString (NSObject obj, NSDictionary attrs);
	public virtual string GetEditingString (NSObject value);
	public virtual bool GetObjectValue (out NSObject obj, string str, out NSString error);
	public virtual string GetString (NSObject value);
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

### Type Changed: Foundation.NSObject

Added method:

<pre style='color: green'>
	public virtual void PrepareForInterfaceBuilder ();
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

### Type Changed: Foundation.NSUrlSessionUploadTask


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Foundation.NSUrlSessionTask</span></span>

 <span style='color:green'>Foundation.NSUrlSessionDataTask</span>

### Type Changed: Foundation.NSUserActivity

Added property:

<pre style='color: green'>
	public virtual CoreSpotlight.CSSearchableItemAttributeSet ContentAttributeSet { get; set; }
</pre>

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

### Type Changed: GameKit.GKLocalPlayerListener

Added method:

<pre style='color: green'>
	public virtual void WantsToQuitMatch (GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: GameKit.GKMatch

Added event:

<pre style='color: green'>
	public event System.EventHandler&lt;GKDataReceivedForRecipientEventArgs&gt; DataReceivedForRecipient;
</pre>

### Type Changed: GameKit.GKMatchDelegate

Added method:

<pre style='color: green'>
	public virtual void DataReceivedForRecipient (GKMatch match, Foundation.NSData data, GKPlayer recipient, GKPlayer player);
</pre>

### Type Changed: GameKit.GKMatchDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DataReceivedForRecipient (IGKMatchDelegate This, GKMatch match, Foundation.NSData data, GKPlayer recipient, GKPlayer player);
</pre>

### Type Changed: GameKit.GKMatchmakerViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>UIKit.UIViewController</span></span>

 <span style='color:green'>UIKit.UINavigationController</span>

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

### Type Changed: GameKit.GKPlayer

Added property:

<pre style='color: green'>
	public virtual string GuestIdentifier { get; }
</pre>

Added method:

<pre style='color: green'>
	public static GKPlayer GetAnonymousGuestPlayer (string guestIdentifier);
</pre>

### Type Changed: GameKit.GKTurnBasedEventListener

Added method:

<pre style='color: green'>
	public virtual void WantsToQuitMatch (GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: GameKit.GKTurnBasedEventListener_Extensions

Added method:

<pre style='color: green'>
	public static void WantsToQuitMatch (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match);
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

### New Type GameKit.GKDataReceivedForRecipientEventArgs

<pre style='color: green'>
public class GKDataReceivedForRecipientEventArgs : System.EventArgs {
	// constructors
	public GKDataReceivedForRecipientEventArgs (Foundation.NSData data, GKPlayer recipient, GKPlayer player);
	// properties
	public Foundation.NSData Data { get; set; }
	public GKPlayer Player { get; set; }
	public GKPlayer Recipient { get; set; }
}
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

### New Type GLKit.GLKMesh

<pre style='color: green'>
public class GLKMesh : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public GLKMesh ();
	protected GLKMesh (Foundation.NSObjectFlag t);
	protected GLKMesh (IntPtr handle);
	public GLKMesh (ModelIO.MDLMesh mesh);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Matrix4 Matrix { get; }
	public virtual string Name { get; }
	public virtual GLKSubmesh[] Submeshes { get; }
	public virtual GLKMeshBuffer[] VertexBuffers { get; }
	public virtual uint VertexCount { get; }
	public virtual ModelIO.MDLVertexDescriptor VertexDescriptor { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static GLKMesh[] MeshesFromAsset (ModelIO.MDLAsset asset);
}
</pre>

### New Type GLKit.GLKMeshBuffer

<pre style='color: green'>
public class GLKMeshBuffer : Foundation.NSObject, ModelIO.IMDLMeshBuffer, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public GLKMeshBuffer ();
	protected GLKMeshBuffer (Foundation.NSObjectFlag t);
	protected GLKMeshBuffer (IntPtr handle);
	// properties
	public virtual ModelIO.IMDLMeshBufferAllocator Allocator { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint GlBufferName { get; }
	public virtual uint Length { get; }
	public virtual Foundation.NSData Map { get; }
	public virtual ModelIO.MDLMeshBufferType Type { get; }
	public virtual ModelIO.IMDLMeshBufferZone Zone { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Offset (Foundation.NSData data, uint offset);
}
</pre>

### New Type GLKit.GLKMeshBufferAllocator

<pre style='color: green'>
public class GLKMeshBufferAllocator : Foundation.NSObject, ModelIO.IMDLMeshBufferAllocator, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected GLKMeshBufferAllocator (Foundation.NSObjectFlag t);
	protected GLKMeshBufferAllocator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual ModelIO.IMDLMeshBuffer NewBuffer (uint length, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer NewBufferFromZone (ModelIO.IMDLMeshBufferZone zone, uint length, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer NewBufferFromZone (ModelIO.IMDLMeshBufferZone zone, Foundation.NSData data, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer NewBufferWithData (Foundation.NSData data, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBufferZone NewZone (uint capacity);
}
</pre>

### New Type GLKit.GLKSubmesh

<pre style='color: green'>
public class GLKSubmesh : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public GLKSubmesh ();
	protected GLKSubmesh (Foundation.NSObjectFlag t);
	protected GLKSubmesh (IntPtr handle);
	public GLKSubmesh (GLKMesh mesh, ModelIO.MDLSubmesh submesh);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GLKMeshBuffer ElementBuffer { get; }
	public virtual int ElementCount { get; }
	public virtual ModelIO.MDLMaterial Material { get; set; }
	public virtual GLKMesh Mesh { get; }
	public virtual uint Mode { get; }
	public virtual string Name { get; }
	public virtual uint Type { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type GLKit.GLKVertexAttributeParameters

<pre style='color: green'>
public struct GLKVertexAttributeParameters {
	// fields
	public uint GlSize;
	public uint GlType;
	public bool Normalized;
	// methods
	public static GLKVertexAttributeParameters FromVertexFormat (ModelIO.MDLVertexFormat vertexFormat);
}
</pre>

## Namespace HealthKit

### Type Changed: HealthKit.HKBiologicalSexObject

Added constructor:

<pre style='color: green'>
	public HKBiologicalSexObject (Foundation.NSCoder coder);
</pre>

Added interfaces:

<pre style='color: green'>
	Foundation.INSCoding
	Foundation.INSCopying
	Foundation.INSSecureCoding
</pre>

Added methods:

<pre style='color: green'>
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

### Type Changed: HealthKit.HKBloodTypeObject

Added constructor:

<pre style='color: green'>
	public HKBloodTypeObject (Foundation.NSCoder coder);
</pre>

Added interfaces:

<pre style='color: green'>
	Foundation.INSCoding
	Foundation.INSCopying
	Foundation.INSSecureCoding
</pre>

Added methods:

<pre style='color: green'>
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

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

## Namespace JavaScriptCore

### Type Changed: JavaScriptCore.JSValue

Added properties:

<pre style='color: green'>
	public virtual bool IsArray { get; }
	public virtual bool IsDate { get; }
</pre>

## Namespace LocalAuthentication

### Type Changed: LocalAuthentication.LAContext

Added properties:

<pre style='color: green'>
	public virtual Foundation.NSData EvaluatedPolicyDomainState { get; set; }
	public static double LATouchIdAuthenticationMaximumAllowableReuseDuration { get; }
	public virtual double TouchIdAuthenticationAllowableReuseDuration { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void EvaluateAccessControl (Security.SecAccessControl accessControl, LAAccessControlOperation operation, string localizedReason, System.Action&lt;System.Boolean,Foundation.NSError&gt; reply);
	public virtual void Invalidate ();
	public virtual bool IsCredentialSet (LACredentialType type);
	public virtual bool SetCredentialType (Foundation.NSData credential, LACredentialType type);
</pre>

### Type Changed: LocalAuthentication.LAPolicy

Added value:

<pre style='color: green'>
	DeviceOwnerAuthentication = 2,
</pre>

### Type Changed: LocalAuthentication.LAStatus

Added values:

<pre style='color: green'>
	AppCancel = -9,
	InvalidContext = -10,
	TouchIDLockout = -8,
</pre>

### New Type LocalAuthentication.LAAccessControlOperation

<pre style='color: green'>
[Serializable]
public enum LAAccessControlOperation {
	CreateItem = 0,
	CreateKey = 2,
	UseItem = 1,
	UseKeySign = 3,
}
</pre>

### New Type LocalAuthentication.LACredentialType

<pre style='color: green'>
[Serializable]
public enum LACredentialType {
	ApplicationPassword = 0,
}
</pre>

## Namespace MapKit

### Type Changed: MapKit.MKAnnotationView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

Added property:

<pre style='color: green'>
	public virtual UIKit.UIView DetailCalloutAccessoryView { get; set; }
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

### Type Changed: MapKit.MKDirections

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public MKDirections ();
```

### Type Changed: MapKit.MKDirectionsMode

Added value:

<pre style='color: green'>
	Transit = 2,
</pre>

### Type Changed: MapKit.MKDirectionsTransportType

Added value:

<pre style='color: green'>
	Transit = 4,
</pre>

### Type Changed: MapKit.MKETAResponse

Added properties:

<pre style='color: green'>
	public virtual Foundation.NSDate ExpectedArrivalDate { get; }
	public virtual Foundation.NSDate ExpectedDepartureDate { get; }
	public virtual MKDirectionsTransportType TransportType { get; }
</pre>

### Type Changed: MapKit.MKMapCamera

Added method:

<pre style='color: green'>
	public static MKMapCamera CameraLookingAtCenterCoordinate (CoreLocation.CLLocationCoordinate2D centerCoordinate, double locationDistance, nfloat pitch, double locationDirectionHeading);
</pre>

### Type Changed: MapKit.MKMapItem

Added property:

<pre style='color: green'>
	public virtual Foundation.NSTimeZone TimeZone { get; set; }
</pre>

### Type Changed: MapKit.MKMapType

Added values:

<pre style='color: green'>
	HybridFlyover = 4,
	SatelliteFlyover = 3,
</pre>

### Type Changed: MapKit.MKMapView

Added interfaces:

<pre style='color: green'>
	UIKit.IUIAppearance
	UIKit.IUIAppearanceContainer
</pre>

Added properties:

<pre style='color: green'>
	public virtual bool ShowsCompass { get; set; }
	public virtual bool ShowsScale { get; set; }
	public virtual bool ShowsTraffic { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void _HandleSelectionAtPoint (CoreGraphics.CGPoint locationInView);
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

Added properties:

<pre style='color: green'>
	public static UIKit.UIColor GreenPinColor { get; }
	public virtual UIKit.UIColor PinTintColor { get; set; }
	public static UIKit.UIColor PurplePinColor { get; }
	public static UIKit.UIColor RedPinColor { get; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

### Type Changed: MapKit.MKPinAnnotationView.MKPinAnnotationViewAppearance

Added constructor:

<pre style='color: green'>
	protected MKPinAnnotationView (IntPtr handle);
</pre>

Added property:

<pre style='color: green'>
	public virtual UIKit.UIColor PinTintColor { get; set; }
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

### Type Changed: MediaPlayer.MPMediaEntity

Added method:

<pre style='color: green'>
	public virtual Foundation.NSObject GetObject (Foundation.NSObject key);
</pre>

### Type Changed: MediaPlayer.MPMediaItemCollection


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Foundation.NSObject</span></span>

 <span style='color:green'>MediaPlayer.MPMediaEntity</span>

Added method:

<pre style='color: green'>
	public virtual Foundation.NSObject GetObject (Foundation.NSObject key);
</pre>

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

### Type Changed: MediaPlayer.MPPlayableContentDelegate

Obsoleted methods:

```
[Obsolete ("Use InitiatePlaybackOfContentItem instead"]
	public virtual void PlayableContentManager (MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action<Foundation.NSError> completionHandler);
```

Added methods:

<pre style='color: green'>
	public virtual void ContextUpdated (MPPlayableContentManager contentManager, MPPlayableContentManagerContext context);
	public virtual void InitiatePlaybackOfContentItem (MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action&lt;Foundation.NSError&gt; completionHandler);
</pre>

### Type Changed: MediaPlayer.MPPlayableContentDelegate_Extensions

Obsoleted methods:

```
[Obsolete ("Use InitiatePlaybackOfContentItem instead"]
	public static void PlayableContentManager (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action<Foundation.NSError> completionHandler);
```

Added methods:

<pre style='color: green'>
	public static void ContextUpdated (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MPPlayableContentManagerContext context);
	public static void InitiatePlaybackOfContentItem (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action&lt;Foundation.NSError&gt; completionHandler);
</pre>

### Type Changed: MediaPlayer.MPPlayableContentManager

Added property:

<pre style='color: green'>
	public virtual MPPlayableContentManagerContext Context { get; }
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

### New Type MediaPlayer.MPPlayableContentManagerContext

<pre style='color: green'>
public class MPPlayableContentManagerContext : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public MPPlayableContentManagerContext ();
	protected MPPlayableContentManagerContext (Foundation.NSObjectFlag t);
	protected MPPlayableContentManagerContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool ContentLimitsEnforced { get; }
	public virtual bool EndpointAvailable { get; }
	public virtual nint EnforcedContentItemsCount { get; }
	public virtual nint EnforcedContentTreeDepth { get; }
}
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

## Namespace MobileCoreServices

### Type Changed: MobileCoreServices.UTType

Added property:

<pre style='color: green'>
	public static Foundation.NSString SwiftSource { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static Foundation.NSDictionary GetDeclaration (string uti);
	public static Foundation.NSUrl GetDeclaringBundleURL (string uti);
	public static string GetPreferredTag (string uti, string tagClass);
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
public const string Version = "8.10.0" "8.99.0";
```

Added fields:

<pre style='color: green'>
	public static const string ContactsLibrary = "/System/Library/Frameworks/Contacts.framework/Contacts";
	public static const string ContactsUILibrary = "/System/Library/Frameworks/ContactsUI.framework/ContactsUI";
	public static const string CoreSpotlightLibrary = "/System/Library/Frameworks/CoreSpotlight.framework/CoreSpotlight";
	public static const string libcLibrary = "/usr/lib/libc.dylib";
	public static const string libSystemLibrary = "/usr/lib/libSystem.dylib";
	public static const string ReplayKitLibrary = "/System/Library/Frameworks/ReplayKit.framework/ReplayKit";
	public static const string SdkVersion = "9.0";
	public static const string WatchConnectivityLibrary = "/System/Library/Frameworks/WatchConnectivity.framework/WatchConnectivity";
	public static const string WebKitLibrary = "/System/Library/Frameworks/WebKit.framework/WebKit";
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

Added values:

<pre style='color: green'>
	iOS_8_4 = 525312,
	iOS_9_0 = 589824,
	Mac_10_10_3 = 2825757768286208,
	Mac_10_11 = 2826844395012096,
</pre>

## Namespace OpenGLES

### Type Changed: OpenGLES.EAGLContext

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public EAGLContext ();
```

Added method:

<pre style='color: green'>
	public static void EAGLGetVersion (out uint major, out uint minor);
</pre>

## Namespace OpenTK

### New Type OpenTK.Vector2i

<pre style='color: green'>
[Serializable]
public struct Vector2i, System.IEquatable&lt;Vector2i&gt; {
	// constructors
	public Vector2i (int x, int y);
	// fields
	public static Vector2i One;
	public static int SizeInBytes;
	public static Vector2i UnitX;
	public static Vector2i UnitY;
	public int X;
	public int Y;
	public static Vector2i Zero;
	// methods
	public static Vector2i Add (Vector2i a, Vector2i b);
	public static void Add (ref Vector2i a, ref Vector2i b, out Vector2i result);
	public static Vector2i Clamp (Vector2i vec, Vector2i min, Vector2i max);
	public static void Clamp (ref Vector2i vec, ref Vector2i min, ref Vector2i max, out Vector2i result);
	public override bool Equals (object obj);
	public virtual bool Equals (Vector2i other);
	public override int GetHashCode ();
	public static Vector2i op_Addition (Vector2i left, Vector2i right);
	public static bool op_Equality (Vector2i left, Vector2i right);
	public static bool op_Inequality (Vector2i left, Vector2i right);
	public static Vector2i op_Subtraction (Vector2i left, Vector2i right);
	public static Vector2i op_UnaryNegation (Vector2i vec);
	public static void Subtract (ref Vector2i a, ref Vector2i b, out Vector2i result);
	public static Vector2i Subtract (Vector2i a, Vector2i b);
	public override string ToString ();
}
</pre>

### New Type OpenTK.Vector3i

<pre style='color: green'>
[Serializable]
public struct Vector3i, System.IEquatable&lt;Vector3i&gt; {
	// constructors
	public Vector3i (int x, int y, int z);
	public Vector3i (Vector2i v);
	public Vector3i (Vector3i v);
	// fields
	public static Vector3i One;
	public static int SizeInBytes;
	public static Vector3i UnitX;
	public static Vector3i UnitY;
	public static Vector3i UnitZ;
	public int X;
	public int Y;
	public int Z;
	public static Vector3i Zero;
	// properties
	public Vector2i Xy { get; set; }
	// methods
	public static Vector3i Add (Vector3i a, Vector3i b);
	public static void Add (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public static void Clamp (ref Vector3i vec, ref Vector3i min, ref Vector3i max, out Vector3i result);
	public static Vector3i Clamp (Vector3i vec, Vector3i min, Vector3i max);
	public static Vector3i ComponentMax (Vector3i a, Vector3i b);
	public static void ComponentMax (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public static Vector3i ComponentMin (Vector3i a, Vector3i b);
	public static void ComponentMin (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public override bool Equals (object obj);
	public virtual bool Equals (Vector3i other);
	public override int GetHashCode ();
	public static Vector3i op_Addition (Vector3i left, Vector3i right);
	public static bool op_Equality (Vector3i left, Vector3i right);
	public static bool op_Inequality (Vector3i left, Vector3i right);
	public static Vector3i op_Subtraction (Vector3i left, Vector3i right);
	public static Vector3i op_UnaryNegation (Vector3i vec);
	public static Vector3i Subtract (Vector3i a, Vector3i b);
	public static void Subtract (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public override string ToString ();
}
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

## Namespace Photos

### Type Changed: Photos.PHAssetChangeRequest

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public PHAssetChangeRequest ();
```

## Namespace QuickLook

### Type Changed: QuickLook.QLPreviewController

Added interface:

<pre style='color: green'>
	UIKit.IUIAppearanceContainer
</pre>

## Namespace SafariServices

### New Type SafariServices.ISFSafariViewControllerDelegate

<pre style='color: green'>
public interface ISFSafariViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type SafariServices.SFContentBlockerErrorCode

<pre style='color: green'>
[Serializable]
public enum SFContentBlockerErrorCode {
	LoadingInterrupted = 3,
	NoAttachmentFound = 2,
	NoExtensionFound = 1,
	Ok = 0,
}
</pre>

### New Type SafariServices.SFContentBlockerManager

<pre style='color: green'>
public class SFContentBlockerManager : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public SFContentBlockerManager ();
	protected SFContentBlockerManager (Foundation.NSObjectFlag t);
	protected SFContentBlockerManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public static void ReloadContentBlocker (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);
}
</pre>

### New Type SafariServices.SFSafariViewController

<pre style='color: green'>
public class SFSafariViewController : UIKit.UIViewController, System.Collections.IEnumerable, Foundation.INSCoding, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public SFSafariViewController (Foundation.NSCoder coder);
	protected SFSafariViewController (Foundation.NSObjectFlag t);
	protected SFSafariViewController (IntPtr handle);
	public SFSafariViewController (Foundation.NSUrl url, bool entersReaderIfAvailable);
	public SFSafariViewController (Foundation.NSUrl url);
	// properties
	public override IntPtr ClassHandle { get; }
	public ISFSafariViewControllerDelegate Delegate { get; set; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type SafariServices.SFSafariViewControllerDelegate

<pre style='color: green'>
public class SFSafariViewControllerDelegate : Foundation.NSObject, ISFSafariViewControllerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public SFSafariViewControllerDelegate ();
	protected SFSafariViewControllerDelegate (Foundation.NSObjectFlag t);
	protected SFSafariViewControllerDelegate (IntPtr handle);
	// methods
	public virtual void DidFinish (SFSafariViewController controller);
	public virtual UIKit.UIActivity[] GetActivityItemsForUrl (SFSafariViewController controller, Foundation.NSUrl url, string title);
}
</pre>

### New Type SafariServices.SFSafariViewControllerDelegate_Extensions

<pre style='color: green'>
public static class SFSafariViewControllerDelegate_Extensions {
	// methods
	public static void DidFinish (ISFSafariViewControllerDelegate This, SFSafariViewController controller);
	public static UIKit.UIActivity[] GetActivityItemsForUrl (ISFSafariViewControllerDelegate This, SFSafariViewController controller, Foundation.NSUrl url, string title);
}
</pre>

## Namespace SceneKit

### Type Changed: SceneKit.SCNAction

Added methods:

<pre style='color: green'>
	public static SCNAction Hide ();
	public static SCNAction Unhide ();
</pre>

### Type Changed: SceneKit.SCNLight

Obsoleted methods:

```
[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
	public virtual Foundation.NSObject GetAttribute (Foundation.NSString lightAttribute);
	[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
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

## Namespace Security

### Type Changed: Security.SecAccessControl

Added interfaces:

<pre style='color: green'>
	ObjCRuntime.INativeObject
	System.IDisposable
</pre>

Added property:

<pre style='color: green'>
	public virtual IntPtr Handle { get; }
</pre>

Added methods:

<pre style='color: green'>
	protected override void ~SecAccessControl ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
</pre>

### Type Changed: Security.SecAccessControlCreateFlags

Added values:

<pre style='color: green'>
	And = 32768,
	ApplicationPassword = -2147483648,
	DevicePasscode = 16,
	Or = 16384,
	PrivateKeyUsage = 1073741824,
	TouchIDAny = 2,
	TouchIDCurrentSet = 8,
</pre>

### Type Changed: Security.SslCipherSuite

Added values:

<pre style='color: green'>
	TLS_DHE_RSA_WITH_AES_128_GCM_SHA256 = 158,
	TLS_DHE_RSA_WITH_AES_256_GCM_SHA384 = 159,
	TLS_ECDH_ECDSA_WITH_AES_128_GCM_SHA256 = 49197,
	TLS_ECDH_ECDSA_WITH_AES_256_GCM_SHA384 = 49198,
	TLS_ECDH_RSA_WITH_AES_128_GCM_SHA256 = 49201,
	TLS_ECDH_RSA_WITH_AES_256_GCM_SHA384 = 49202,
	TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256 = 49195,
	TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384 = 49196,
	TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 = 49199,
	TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 = 49200,
	TLS_RSA_WITH_AES_128_GCM_SHA256 = 156,
	TLS_RSA_WITH_AES_256_GCM_SHA384 = 157,
</pre>

### Type Changed: Security.SslContext

Added method:

<pre style='color: green'>
	public SslStatus SetSessionStrengthPolicy (SslSessionStrengthPolicy policyStrength);
</pre>

### Type Changed: Security.SslSessionOption

Added values:

<pre style='color: green'>
	AllowServerIdentityChange = 5,
	BreakOnClientHello = 7,
</pre>

### Type Changed: Security.SslStatus

Added values:

<pre style='color: green'>
	SSLClientHelloReceived = -9851,
	SSLWeakPeerEphemeralDHKey = -9850,
</pre>

### New Type Security.SslSessionStrengthPolicy

<pre style='color: green'>
[Serializable]
public enum SslSessionStrengthPolicy {
	ATSv1 = 1,
	Default = 0,
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
[Obsolete ("Use the method CreateVortexField instead"]
	public static SKFieldNode CraeteVortexField ();
```

Added method:

<pre style='color: green'>
	public static SKFieldNode CreateVortexField ();
</pre>

### Type Changed: SpriteKit.SKTransition

Added interface:

<pre style='color: green'>
	Foundation.INSCopying
</pre>

Added method:

<pre style='color: green'>
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
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

### Type Changed: UIKit.NSLayoutManager

Added methods:

<pre style='color: green'>
	public virtual ushort CGGlyphAtIndex (uint glyphIndex, ref bool isValidIndex);
	public virtual ushort CGGlyphAtIndex (uint glyphIndex);
	public virtual CoreGraphics.CGRect LineFragmentRectForGlyphAtIndex (uint glyphIndex, out Foundation.NSRange effectiveGlyphRange, bool withoutAdditionalLayout);
	public virtual CoreGraphics.CGRect LineFragmentUsedRectForGlyphAtIndex (uint glyphIndex, out Foundation.NSRange effectiveGlyphRange, bool withoutAdditionalLayout);
	public virtual NSTextContainer TextContainerForGlyphAtIndex (uint glyphIndex, out Foundation.NSRange effectiveGlyphRange, bool withoutAdditionalLayout);
</pre>

### Type Changed: UIKit.NSTextContainer

Added property:

<pre style='color: green'>
	public virtual bool SimpleRectangularTextContainer { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void ReplaceLayoutManager (NSLayoutManager newLayoutManager);
</pre>

### Type Changed: UIKit.UIAccessibilityCustomAction

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIAccessibilityCustomAction ();
```

### Type Changed: UIKit.UIActionSheet

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

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

### Type Changed: UIKit.UIActivityIndicatorView.UIActivityIndicatorViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIActivityIndicatorView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIActivityItemProvider

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIActivityItemProvider ();
```

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

### Type Changed: UIKit.UIActivityType

Added property:

<pre style='color: green'>
	public static Foundation.NSString OpenInIBooks { get; }
</pre>

### Type Changed: UIKit.UIActivityViewController

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIActivityViewController ();
```

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
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

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

### Type Changed: UIKit.UIAlertView.UIAlertViewAppearance

Added constructor:

<pre style='color: green'>
	protected UIAlertView (IntPtr handle);
</pre>

### Type Changed: UIKit.UIApplicationDelegate

Added methods:

<pre style='color: green'>
	public virtual void ApplicationShouldRequestHealthAuthorization (UIApplication application);
	public virtual void HandleAction (UIApplication application, string actionIdentifier, Foundation.NSDictionary remoteNotificationInfo, Foundation.NSDictionary responseInfo, System.Action completionHandler);
	public virtual void HandleAction (UIApplication application, string actionIdentifier, UILocalNotification localNotification, Foundation.NSDictionary responseInfo, System.Action completionHandler);
	public bool OpenUrl (UIApplication app, Foundation.NSUrl url, UIApplicationOpenUrlOptions options);
	public virtual bool OpenUrl (UIApplication app, Foundation.NSUrl url, Foundation.NSDictionary options);
</pre>

### Type Changed: UIKit.UIApplicationDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static void ApplicationShouldRequestHealthAuthorization (IUIApplicationDelegate This, UIApplication application);
	public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, UILocalNotification localNotification, Foundation.NSDictionary responseInfo, System.Action completionHandler);
	public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, Foundation.NSDictionary remoteNotificationInfo, Foundation.NSDictionary responseInfo, System.Action completionHandler);
	public static bool OpenUrl (IUIApplicationDelegate This, UIApplication app, Foundation.NSUrl url, Foundation.NSDictionary options);
	public static bool OpenUrl (IUIApplicationDelegate This, UIApplication app, Foundation.NSUrl url, UIApplicationOpenUrlOptions options);
</pre>

### Type Changed: UIKit.UIBarButtonItem

Added interface:

<pre style='color: green'>
	IUIAppearance
</pre>

Added property:

<pre style='color: green'>
	public virtual UIBarButtonItemGroup ButtonGroup { get; }
</pre>

### Type Changed: UIKit.UIBarButtonItem.UIBarButtonItemAppearance

Added constructor:

<pre style='color: green'>
	protected UIBarButtonItem (IntPtr handle);
</pre>

### Type Changed: UIKit.UIBarItem

Added constructor:

<pre style='color: green'>
	protected UIBarItem (Foundation.NSCoder coder);
</pre>

Added interfaces:

<pre style='color: green'>
	Foundation.INSCoding
	IUIAppearance
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

### Type Changed: UIKit.UICollectionViewTransitionLayout

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UICollectionViewTransitionLayout ();
```

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

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIDocumentMenuViewController ();
```

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

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIDocumentPickerViewController ();
```

Added interface:

<pre style='color: green'>
	IUIAppearanceContainer
</pre>

### Type Changed: UIKit.UIFontDescriptor

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: UIKit.UIImage

Added property:

<pre style='color: green'>
	public virtual bool FlipsForRightToLeftLayoutDirection { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual UIImage ImageFlippedForRightToLeftLayoutDirection ();
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

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

### Type Changed: UIKit.UIInterpolatingMotionEffect

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

### Type Changed: UIKit.UIKeyCommand

Added property:

<pre style='color: green'>
	public virtual string DiscoverabilityTitle { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public static UIKeyCommand Create (Foundation.NSString keyCommandInput, UIKeyModifierFlags modifierFlags, ObjCRuntime.Selector action, Foundation.NSString discoverabilityTitle);
</pre>

### Type Changed: UIKit.UILabel

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added property:

<pre style='color: green'>
	public virtual bool AllowsDefaultTighteningForTruncation { get; set; }
</pre>

### Type Changed: UIKit.UILabel.UILabelAppearance

Added constructor:

<pre style='color: green'>
	protected UILabel (IntPtr handle);
</pre>

### Type Changed: UIKit.UIMutableUserNotificationAction

Added properties:

<pre style='color: green'>
	public virtual UIUserNotificationActionBehavior Behavior { get; set; }
	public virtual Foundation.NSDictionary Parameters { get; set; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

### Type Changed: UIKit.UINavigationBar

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

### Type Changed: UIKit.UIProgressView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added property:

<pre style='color: green'>
	public virtual Foundation.NSProgress ObservedProgress { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

### Type Changed: UIKit.UIReturnKeyType

Added value:

<pre style='color: green'>
	Continue = 11,
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

### Type Changed: UIKit.UIStoryboardPopoverSegue

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIStoryboardPopoverSegue ();
```

### Type Changed: UIKit.UIStoryboardSegue

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance"]
	public UIStoryboardSegue ();
```

### Type Changed: UIKit.UISwitch

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

Added constructor:

<pre style='color: green'>
	public UITabBarItem (Foundation.NSCoder coder);
</pre>

Added interfaces:

<pre style='color: green'>
	Foundation.INSCoding
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

Added property:

<pre style='color: green'>
	public virtual bool CellLayoutMarginsFollowReadableWidth { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
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

Added methods:

<pre style='color: green'>
	public virtual void BeginFloatingCursorAtPoint (CoreGraphics.CGPoint point);
	public virtual void EndFloatingCursor ();
	public virtual UITextInputAssistantItem InputAssistantItem ();
	public virtual void UpdateFloatingCursorAtPoint (CoreGraphics.CGPoint point);
</pre>

### Type Changed: UIKit.UITextField.UITextFieldAppearance

Added constructor:

<pre style='color: green'>
	protected UITextField (IntPtr handle);
</pre>

### Type Changed: UIKit.UITextInput_Extensions

Added methods:

<pre style='color: green'>
	public static void BeginFloatingCursorAtPoint (IUITextInput This, CoreGraphics.CGPoint point);
	public static void EndFloatingCursor (IUITextInput This);
	public static UITextInputAssistantItem InputAssistantItem (IUITextInput This);
	public static void UpdateFloatingCursorAtPoint (IUITextInput This, CoreGraphics.CGPoint point);
</pre>

### Type Changed: UIKit.UITextView

Added interfaces:

<pre style='color: green'>
	IUIAppearance
	IUIAppearanceContainer
</pre>

Added methods:

<pre style='color: green'>
	public virtual void BeginFloatingCursorAtPoint (CoreGraphics.CGPoint point);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void EndFloatingCursor ();
	public virtual UITextInputAssistantItem InputAssistantItem ();
	public virtual void UpdateFloatingCursorAtPoint (CoreGraphics.CGPoint point);
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

### Type Changed: UIKit.UIUserNotificationAction

Added properties:

<pre style='color: green'>
	public virtual UIUserNotificationActionBehavior Behavior { get; set; }
	public virtual Foundation.NSDictionary Parameters { get; set; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
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

Added properties:

<pre style='color: green'>
	public virtual NSLayoutYAxisAnchor BottomAnchor { get; }
	public virtual NSLayoutXAxisAnchor CenterXAnchor { get; }
	public virtual NSLayoutYAxisAnchor CenterYAnchor { get; }
	public virtual NSLayoutYAxisAnchor FirstBaselineAnchor { get; }
	public virtual NSLayoutDimension HeightAnchor { get; }
	public static double InheritedAnimationDuration { get; }
	public virtual NSLayoutYAxisAnchor LastBaselineAnchor { get; }
	public virtual UILayoutGuide[] LayoutGuides { get; }
	public virtual UILayoutGuide LayoutMarginsGuide { get; }
	public virtual NSLayoutXAxisAnchor LeadingAnchor { get; }
	public virtual NSLayoutXAxisAnchor LeftAnchor { get; }
	public virtual UILayoutGuide ReadableContentGuide { get; }
	public virtual NSLayoutXAxisAnchor RightAnchor { get; }
	public virtual UISemanticContentAttribute SemanticContentAttribute { get; set; }
	public virtual NSLayoutYAxisAnchor TopAnchor { get; }
	public virtual NSLayoutXAxisAnchor TrailingAnchor { get; }
	public virtual UIView ViewForFirstBaselineLayout { get; }
	public virtual UIView ViewForLastBaselineLayout { get; }
	public virtual NSLayoutDimension WidthAnchor { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddLayoutGuide (UILayoutGuide guide);
	public static UIUserInterfaceLayoutDirection GetUserInterfaceLayoutDirection (UISemanticContentAttribute attribute);
	public virtual void RemoveLayoutGuide (UILayoutGuide guide);
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

### New Type UIKit.NSDataAsset

<pre style='color: green'>
public class NSDataAsset : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected NSDataAsset (Foundation.NSObjectFlag t);
	protected NSDataAsset (IntPtr handle);
	public NSDataAsset (string name);
	public NSDataAsset (string name, Foundation.NSBundle bundle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSData Data { get; }
	public virtual string Name { get; }
	public virtual Foundation.NSString TypeIdentifier { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type UIKit.NSLayoutAnchor

<pre style='color: green'>
public class NSLayoutAnchor : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected NSLayoutAnchor (Foundation.NSObjectFlag t);
	protected NSLayoutAnchor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutAnchor anchor);
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutAnchor anchor, nfloat constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutAnchor anchor);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutAnchor anchor, nfloat constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutAnchor anchor);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutAnchor anchor, nfloat constant);
}
</pre>

### New Type UIKit.NSLayoutDimension

<pre style='color: green'>
public class NSLayoutDimension : UIKit.NSLayoutAnchor, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected NSLayoutDimension (Foundation.NSObjectFlag t);
	protected NSLayoutDimension (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier);
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier, nfloat constant);
	public virtual NSLayoutConstraint ConstraintEqualToConstant (nfloat constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier, nfloat constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToConstant (nfloat constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier, nfloat constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToConstant (nfloat constant);
}
</pre>

### New Type UIKit.NSLayoutXAxisAnchor

<pre style='color: green'>
public class NSLayoutXAxisAnchor : UIKit.NSLayoutAnchor, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected NSLayoutXAxisAnchor (Foundation.NSObjectFlag t);
	protected NSLayoutXAxisAnchor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type UIKit.NSLayoutYAxisAnchor

<pre style='color: green'>
public class NSLayoutYAxisAnchor : UIKit.NSLayoutAnchor, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected NSLayoutYAxisAnchor (Foundation.NSObjectFlag t);
	protected NSLayoutYAxisAnchor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type UIKit.NSWritingDirectionFormatType

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSWritingDirectionFormatType {
	Embedding = 1,
	Override = 2,
}
</pre>

### New Type UIKit.UIApplicationOpenUrlOptionKeys

<pre style='color: green'>
public static class UIApplicationOpenUrlOptionKeys {
	// properties
	public static Foundation.NSString AnnotationKey { get; }
	public static Foundation.NSString OpenInPlaceKey { get; }
	public static Foundation.NSString SourceApplicationKey { get; }
}
</pre>

### New Type UIKit.UIApplicationOpenUrlOptions

<pre style='color: green'>
public class UIApplicationOpenUrlOptions : Foundation.DictionaryContainer {
	// constructors
	public UIApplicationOpenUrlOptions ();
	public UIApplicationOpenUrlOptions (Foundation.NSDictionary dictionary);
	// properties
	public Foundation.NSObject Annotation { get; set; }
	public bool? OpenInPlace { get; set; }
	public string SourceApplication { get; set; }
}
</pre>

### New Type UIKit.UIBarButtonItemGroup

<pre style='color: green'>
public class UIBarButtonItemGroup : Foundation.NSObject, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public UIBarButtonItemGroup ();
	public UIBarButtonItemGroup (Foundation.NSCoder coder);
	protected UIBarButtonItemGroup (Foundation.NSObjectFlag t);
	protected UIBarButtonItemGroup (IntPtr handle);
	public UIBarButtonItemGroup (UIBarButtonItem[] barButtonItems, UIBarButtonItem representativeItem);
	// properties
	public virtual UIBarButtonItem[] BarButtonItems { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual bool DisplayingRepresentativeItem { get; }
	public virtual UIBarButtonItem RepresentativeItem { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type UIKit.UIInterfaceOrientationExtensions

<pre style='color: green'>
public static class UIInterfaceOrientationExtensions {
	// methods
	public static bool IsLandscape (UIInterfaceOrientation orientation);
	public static bool IsPortrait (UIInterfaceOrientation orientation);
}
</pre>

### New Type UIKit.UILayoutGuide

<pre style='color: green'>
public class UILayoutGuide : Foundation.NSObject, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public UILayoutGuide ();
	public UILayoutGuide (Foundation.NSCoder coder);
	protected UILayoutGuide (Foundation.NSObjectFlag t);
	protected UILayoutGuide (IntPtr handle);
	// properties
	public virtual NSLayoutYAxisAnchor BottomAnchor { get; }
	public virtual NSLayoutXAxisAnchor CenterXAnchor { get; }
	public virtual NSLayoutYAxisAnchor CenterYAnchor { get; }
	public override IntPtr ClassHandle { get; }
	public virtual NSLayoutDimension HeightAnchor { get; }
	public virtual string Identifier { get; set; }
	public virtual CoreGraphics.CGRect LayoutFrame { get; }
	public virtual NSLayoutXAxisAnchor LeadingAnchor { get; }
	public virtual NSLayoutXAxisAnchor LeftAnchor { get; }
	public virtual UIView OwningView { get; set; }
	public virtual NSLayoutXAxisAnchor RightAnchor { get; }
	public virtual NSLayoutYAxisAnchor TopAnchor { get; }
	public virtual NSLayoutXAxisAnchor TrailingAnchor { get; }
	public virtual NSLayoutDimension WidthAnchor { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type UIKit.UIPrinterCutterBehavior

<pre style='color: green'>
[Serializable]
public enum UIPrinterCutterBehavior {
	CutAfterEachCopy = 3,
	CutAfterEachJob = 4,
	CutAfterEachPage = 2,
	NoCut = 0,
	PrinterDefault = 1,
}
</pre>

### New Type UIKit.UIRegion

<pre style='color: green'>
public class UIRegion : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public UIRegion ();
	public UIRegion (Foundation.NSCoder coder);
	protected UIRegion (Foundation.NSObjectFlag t);
	protected UIRegion (IntPtr handle);
	public UIRegion (nfloat radius);
	public UIRegion (CoreGraphics.CGSize size);
	// properties
	public override IntPtr ClassHandle { get; }
	public static UIRegion InfiniteRegion { get; }
	// methods
	public virtual bool ContainsPoint (CoreGraphics.CGPoint point);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual UIRegion InverseRegion ();
	public virtual UIRegion RegionByDifferenceFromRegion (UIRegion region);
	public virtual Foundation.NSObject RegionByIntersectionWithRegion (UIRegion region);
	public virtual UIRegion RegionByUnionWithRegion (UIRegion region);
}
</pre>

### New Type UIKit.UISemanticContentAttribute

<pre style='color: green'>
[Serializable]
public enum UISemanticContentAttribute {
	ForceLeftToRight = 3,
	ForceRightToLeft = 4,
	Playback = 1,
	Spatial = 2,
	Unspecified = 0,
}
</pre>

### New Type UIKit.UIStackView

<pre style='color: green'>
public class UIStackView : UIKit.UIView, System.Collections.IEnumerable, Foundation.INSCoding, IUIAccessibilityIdentification, IUIAppearance, IUIAppearanceContainer, IUICoordinateSpace, IUIDynamicItem, IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public UIStackView ();
	public UIStackView (Foundation.NSCoder coder);
	protected UIStackView (Foundation.NSObjectFlag t);
	protected UIStackView (IntPtr handle);
	public UIStackView (UIView[] views);
	// properties
	public virtual UIStackViewAlignment Alignment { get; set; }
	public static UIStackView.UIStackViewAppearance Appearance { get; }
	public virtual UIView ArrangedSubviews { get; }
	public virtual UILayoutConstraintAxis Axis { get; set; }
	public virtual bool BaselineRelativeArrangement { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual UIStackViewDistribution Distribution { get; set; }
	public virtual bool LayoutMarginsRelativeArrangement { get; set; }
	public virtual nfloat Spacing { get; set; }
	// methods
	public virtual void AddArrangedSubview (UIView view);
	public static UIStackView.UIStackViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static UIStackView.UIStackViewAppearance GetAppearance&lt;T&gt; (UITraitCollection traits);
	public static UIStackView.UIStackViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIStackView.UIStackViewAppearance GetAppearance (UITraitCollection traits);
	public static UIStackView.UIStackViewAppearance GetAppearance&lt;T&gt; ();
	public static UIStackView.UIStackViewAppearance GetAppearance&lt;T&gt; (UITraitCollection traits, System.Type[] containers);
	public virtual void InsertArrangedSubview (UIView view, uint stackIndex);
	public virtual void RemoveArrangedSubview (UIView view);

	// inner types
	public class UIStackViewAppearance : UIKit.UIView+UIViewAppearance, IUIAppearance, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
		// constructors
		protected UIStackView (IntPtr handle);
	}
}
</pre>

### New Type UIKit.UIStackViewAlignment

<pre style='color: green'>
[Serializable]
public enum UIStackViewAlignment {
	Bottom = 4,
	Center = 3,
	Fill = 0,
	FirstBaseline = 2,
	LastBaseline = 5,
	Leading = 1,
	Top = 1,
	Trailing = 4,
}
</pre>

### New Type UIKit.UIStackViewDistribution

<pre style='color: green'>
[Serializable]
public enum UIStackViewDistribution {
	EqualCentering = 4,
	EqualSpacing = 3,
	Fill = 0,
	FillEqually = 1,
	FillProportionally = 2,
}
</pre>

### New Type UIKit.UIStoryboardUnwindSegueSource

<pre style='color: green'>
public class UIStoryboardUnwindSegueSource : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected UIStoryboardUnwindSegueSource (Foundation.NSObjectFlag t);
	protected UIStoryboardUnwindSegueSource (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSObject Sender { get; }
	public virtual UIViewController SourceViewController { get; }
	public virtual ObjCRuntime.Selector UnwindAction { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type UIKit.UITextInputAssistantItem

<pre style='color: green'>
public class UITextInputAssistantItem : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public UITextInputAssistantItem ();
	protected UITextInputAssistantItem (Foundation.NSObjectFlag t);
	protected UITextInputAssistantItem (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual UIBarButtonItemGroup[] LeadingBarButtonGroups { get; set; }
	public virtual UIBarButtonItemGroup[] TrailingBarButtonGroups { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type UIKit.UIUserNotificationActionBehavior

<pre style='color: green'>
[Serializable]
public enum UIUserNotificationActionBehavior {
	Default = 0,
	TextInput = 1,
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

Added property:

<pre style='color: green'>
	public virtual string CustomUserAgent { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual WKNavigation LoadData (Foundation.NSData data, string MIMEType, string characterEncodingName, Foundation.NSUrl baseUrl);
	public virtual WKNavigation LoadFileUrl (Foundation.NSUrl url, Foundation.NSUrl readAccessUrl);
</pre>

### Type Changed: WebKit.WKWebView.WKWebViewAppearance

Added constructor:

<pre style='color: green'>
	protected WKWebView (IntPtr handle);
</pre>

### Type Changed: WebKit.WKWebViewConfiguration

Added properties:

<pre style='color: green'>
	public virtual string ApplicationNameForUserAgent { get; set; }
	public virtual WKWebsiteDataStore WebsiteDataStore { get; set; }
</pre>

### New Type WebKit.WKWebsiteDataRecord

<pre style='color: green'>
public class WKWebsiteDataRecord : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public WKWebsiteDataRecord ();
	protected WKWebsiteDataRecord (Foundation.NSObjectFlag t);
	protected WKWebsiteDataRecord (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSSet DataTypes { get; }
	public virtual string DisplayName { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type WebKit.WKWebsiteDataStore

<pre style='color: green'>
public class WKWebsiteDataStore : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public WKWebsiteDataStore ();
	protected WKWebsiteDataStore (Foundation.NSObjectFlag t);
	protected WKWebsiteDataStore (IntPtr handle);
	// properties
	public static Foundation.NSSet AllWebsiteDataTypes { get; }
	public override IntPtr ClassHandle { get; }
	public static WKWebsiteDataStore DefaultDataStore { get; }
	public static WKWebsiteDataStore NonPersistentDataStore { get; }
	public virtual bool Persistent { get; }
	// methods
	public virtual void FetchDataRecordsOfTypes (Foundation.NSSet dataTypes, System.Action&lt;Foundation.NSArray&gt; completionHandler);
	public virtual void RemoveDataOfTypes (Foundation.NSSet dataTypes, WKWebsiteDataRecord[] dataRecords, System.Action completionHandler);
	public virtual void RemoveDataOfTypes (Foundation.NSSet websiteDataTypes, Foundation.NSDate date, System.Action completionHandler);
}
</pre>

### New Type WebKit.WKWebsiteDataType

<pre style='color: green'>
public static class WKWebsiteDataType {
	// properties
	public static Foundation.NSString Cookies { get; }
	public static Foundation.NSString DiskCache { get; }
	public static Foundation.NSString IndexedDBDatabases { get; }
	public static Foundation.NSString LocalStorage { get; }
	public static Foundation.NSString MemoryCache { get; }
	public static Foundation.NSString OfflineWebApplicationCache { get; }
	public static Foundation.NSString WebSQLDatabases { get; }
}
</pre>

## New Namespace Contacts

### New Type Contacts.CNAuthorizationStatus

<pre style='color: green'>
[Serializable]
public enum CNAuthorizationStatus {
	Authorized = 3,
	Denied = 2,
	NotDetermined = 0,
	Restricted = 1,
}
</pre>

### New Type Contacts.CNContact

<pre style='color: green'>
public class CNContact : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContact ();
	public CNContact (Foundation.NSCoder coder);
	protected CNContact (Foundation.NSObjectFlag t);
	protected CNContact (IntPtr handle);
	// properties
	public virtual Foundation.NSDateComponents Birthday { get; }
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSObject[] ContactRelations { get; }
	public virtual CNContactType ContactType { get; }
	public virtual Foundation.NSObject[] Dates { get; }
	public virtual string DepartmentName { get; }
	public virtual Foundation.NSObject[] EmailAddresses { get; }
	public static Foundation.NSString ErrorDomain { get; }
	public virtual string FamilyName { get; }
	public virtual string GivenName { get; }
	public virtual string Identifier { get; }
	public virtual Foundation.NSData ImageData { get; }
	public virtual bool ImageDataAvailable { get; }
	public virtual Foundation.NSObject[] InstantMessageAddresses { get; }
	public virtual string JobTitle { get; }
	public virtual string MiddleName { get; }
	public virtual string NamePrefix { get; }
	public virtual string NameSuffix { get; }
	public virtual string Nickname { get; }
	public virtual Foundation.NSDateComponents NonGregorianBirthday { get; }
	public virtual string Note { get; }
	public virtual string OrganizationName { get; }
	public virtual Foundation.NSObject[] PhoneNumbers { get; }
	public virtual string PhoneticFamilyName { get; }
	public virtual string PhoneticGivenName { get; }
	public virtual string PhoneticMiddleName { get; }
	public virtual Foundation.NSObject[] PostalAddresses { get; }
	public virtual string PreviousFamilyName { get; }
	public static Foundation.NSString PropertyNotFetchedExceptionName { get; }
	public virtual Foundation.NSObject[] SocialProfiles { get; }
	public virtual Foundation.NSData ThumbnailImageData { get; }
	public virtual Foundation.NSObject[] UrlAddresses { get; }
	// methods
	public virtual bool AreKeysAvailable (ICNKeyDescriptor[] keyDescriptors);
	public static System.Func&lt;Foundation.NSObject,Foundation.NSObject,Foundation.NSComparisonResult&gt; ComparatorForName (CNContactSortOrder sortOrder);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static ICNKeyDescriptor DescriptorForAllComparatorKeys ();
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual bool IsKeyAvailable (Foundation.NSString contactKey);
	public virtual bool IsKeyAvailable (CNContactOption contactOption);
	public static string LocalizeProperty (CNContactOption contactOption);
	public static string LocalizeProperty (Foundation.NSString contactKey);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
</pre>

### New Type Contacts.CNContact_PredicatesExtension

<pre style='color: green'>
public static class CNContact_PredicatesExtension {
	// methods
	public static Foundation.NSPredicate GetPredicateForContacts (CNContact This, string matchingName);
	public static Foundation.NSPredicate GetPredicateForContacts (CNContact This, string[] identifiers);
	public static Foundation.NSPredicate GetPredicateForContactsInContainer (CNContact This, string containerIdentifier);
	public static Foundation.NSPredicate GetPredicateForContactsInGroup (CNContact This, string groupIdentifier);
	public static Foundation.NSPredicate GetPredicateForContactsLinked (CNContact This, CNContact contact);
}
</pre>

### New Type Contacts.CNContactDisplayNameOrder

<pre style='color: green'>
[Serializable]
public enum CNContactDisplayNameOrder {
	FamilyNameFirst = 2,
	GivenNameFirst = 1,
	UserDefault = 0,
}
</pre>

### New Type Contacts.CNContactFetchRequest

<pre style='color: green'>
public class CNContactFetchRequest : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected CNContactFetchRequest (Foundation.NSObjectFlag t);
	protected CNContactFetchRequest (IntPtr handle);
	public CNContactFetchRequest (ICNKeyDescriptor[] keysToFetch);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual ICNKeyDescriptor[] KeysToFetch { get; set; }
	public virtual bool MutableObjects { get; set; }
	public virtual Foundation.NSPredicate Predicate { get; set; }
	public virtual CNContactSortOrder SortOrder { get; set; }
	public virtual bool UnifyResults { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Contacts.CNContactFormatter

<pre style='color: green'>
public class CNContactFormatter : Foundation.NSFormatter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContactFormatter ();
	public CNContactFormatter (Foundation.NSCoder coder);
	protected CNContactFormatter (Foundation.NSObjectFlag t);
	protected CNContactFormatter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString ContactPropertyAttribute { get; }
	public virtual CNContactFormatterStyle Style { get; set; }
	// methods
	public virtual Foundation.NSAttributedString GetAttributedString (CNContact contact, Foundation.NSDictionary attributes);
	public static Foundation.NSAttributedString GetAttributedStringFrom (CNContact contact, CNContactFormatterStyle style, Foundation.NSDictionary attributes);
	public static string GetDelimiterFor (CNContact contact);
	public static ICNKeyDescriptor GetDescriptorForRequiredKeys (CNContactFormatterStyle style);
	public static CNContactDisplayNameOrder GetNameOrderFor (CNContact contact);
	public virtual string GetString (CNContact contact);
	public static string GetStringFrom (CNContact contact, CNContactFormatterStyle style);
}
</pre>

### New Type Contacts.CNContactFormatterStyle

<pre style='color: green'>
[Serializable]
public enum CNContactFormatterStyle {
	FullName = 0,
	PhoneticFullName = 1,
}
</pre>

### New Type Contacts.CNContactKey

<pre style='color: green'>
public static class CNContactKey {
	// properties
	public static Foundation.NSString Birthday { get; }
	public static Foundation.NSString Dates { get; }
	public static Foundation.NSString DepartmentName { get; }
	public static Foundation.NSString EmailAddresses { get; }
	public static Foundation.NSString FamilyName { get; }
	public static Foundation.NSString GivenName { get; }
	public static Foundation.NSString Identifier { get; }
	public static Foundation.NSString ImageData { get; }
	public static Foundation.NSString ImageDataAvailable { get; }
	public static Foundation.NSString InstantMessageAddresses { get; }
	public static Foundation.NSString JobTitle { get; }
	public static Foundation.NSString MiddleName { get; }
	public static Foundation.NSString NamePrefix { get; }
	public static Foundation.NSString NameSuffix { get; }
	public static Foundation.NSString Nickname { get; }
	public static Foundation.NSString NonGregorianBirthday { get; }
	public static Foundation.NSString Note { get; }
	public static Foundation.NSString OrganizationName { get; }
	public static Foundation.NSString PhoneNumbers { get; }
	public static Foundation.NSString PhoneticFamilyName { get; }
	public static Foundation.NSString PhoneticGivenName { get; }
	public static Foundation.NSString PhoneticMiddleName { get; }
	public static Foundation.NSString PostalAddresses { get; }
	public static Foundation.NSString PreviousFamilyName { get; }
	public static Foundation.NSString Relations { get; }
	public static Foundation.NSString SocialProfiles { get; }
	public static Foundation.NSString ThumbnailImageData { get; }
	public static Foundation.NSString Type { get; }
	public static Foundation.NSString UrlAddresses { get; }
}
</pre>

### New Type Contacts.CNContactOption

<pre style='color: green'>
[Serializable]
public enum CNContactOption {
	Birthday = 7,
	Dates = 17,
	DepartmentName = 5,
	EmailAddresses = 15,
	ImageData = 10,
	ImageDataAvailable = 12,
	InstantMessageAddresses = 21,
	JobTitle = 6,
	Nickname = 0,
	NonGregorianBirthday = 8,
	Note = 9,
	OrganizationName = 4,
	PhoneNumbers = 14,
	PhoneticFamilyName = 3,
	PhoneticGivenName = 1,
	PhoneticMiddleName = 2,
	PostalAddresses = 16,
	Relations = 19,
	SocialProfiles = 20,
	ThumbnailImageData = 11,
	Type = 13,
	UrlAddresses = 18,
}
</pre>

### New Type Contacts.CNContactProperty

<pre style='color: green'>
public class CNContactProperty : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContactProperty ();
	public CNContactProperty (Foundation.NSCoder coder);
	protected CNContactProperty (Foundation.NSObjectFlag t);
	protected CNContactProperty (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CNContact Contact { get; }
	public virtual string Identifier { get; }
	public virtual string Key { get; }
	public virtual string Label { get; }
	public virtual Foundation.NSObject Value { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type Contacts.CNContactRelation

<pre style='color: green'>
public class CNContactRelation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContactRelation ();
	public CNContactRelation (Foundation.NSCoder coder);
	protected CNContactRelation (Foundation.NSObjectFlag t);
	protected CNContactRelation (IntPtr handle);
	public CNContactRelation (string name);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static CNContactRelation FromName (string name);
}
</pre>

### New Type Contacts.CNContactSortOrder

<pre style='color: green'>
[Serializable]
public enum CNContactSortOrder {
	FamilyName = 3,
	GivenName = 2,
	None = 0,
	UserDefault = 1,
}
</pre>

### New Type Contacts.CNContactStore

<pre style='color: green'>
public class CNContactStore : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public CNContactStore ();
	protected CNContactStore (Foundation.NSObjectFlag t);
	protected CNContactStore (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string DefaultContainerIdentifier { get; }
	public static Foundation.NSString NotificationDidChange { get; }
	// methods
	public virtual bool EnumerateContacts (CNContactFetchRequest fetchRequest, out Foundation.NSError error, CNContactStoreEnumerateContactsHandler handler);
	public virtual bool ExecuteSaveRequest (CNSaveRequest saveRequest, out Foundation.NSError error);
	public static CNAuthorizationStatus GetAuthorizationStatus (CNEntityType entityType);
	public virtual CNContainer[] GetContainers (Foundation.NSPredicate predicate, out Foundation.NSError error);
	public virtual CNGroup[] GetGroups (Foundation.NSPredicate predicate, out Foundation.NSError error);
	public virtual CNContact GetUnifiedContact (string identifier, ICNKeyDescriptor[] keys, out Foundation.NSError error);
	public virtual CNContact[] GetUnifiedContacts (Foundation.NSPredicate predicate, ICNKeyDescriptor[] keys, out Foundation.NSError error);
	public virtual Foundation.NSObject GetUnifiedMeContact (ICNKeyDescriptor[] keys, out Foundation.NSError error);
	public virtual void RequestAccess (CNEntityType entityType, CNContactStoreRequestAccessHandler completionHandler);
	public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; RequestAccessAsync (CNEntityType entityType);

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveNotificationDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type Contacts.CNContactStoreEnumerateContactsHandler

<pre style='color: green'>
public sealed delegate CNContactStoreEnumerateContactsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CNContactStoreEnumerateContactsHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CNContact contact, bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CNContact contact, bool stop);
}
</pre>

### New Type Contacts.CNContactStoreRequestAccessHandler

<pre style='color: green'>
public sealed delegate CNContactStoreRequestAccessHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CNContactStoreRequestAccessHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool granted, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool granted, Foundation.NSError error);
}
</pre>

### New Type Contacts.CNContactsUserDefaults

<pre style='color: green'>
public class CNContactsUserDefaults : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public CNContactsUserDefaults ();
	protected CNContactsUserDefaults (Foundation.NSObjectFlag t);
	protected CNContactsUserDefaults (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string CountryCode { get; }
	public virtual CNContactSortOrder SortOrder { get; }
	// methods
	public static CNContactsUserDefaults GetSharedDefaults ();
}
</pre>

### New Type Contacts.CNContactType

<pre style='color: green'>
[Serializable]
public enum CNContactType {
	Organization = 1,
	Person = 0,
}
</pre>

### New Type Contacts.CNContactVCardSerialization

<pre style='color: green'>
public class CNContactVCardSerialization : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public CNContactVCardSerialization ();
	protected CNContactVCardSerialization (Foundation.NSObjectFlag t);
	protected CNContactVCardSerialization (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public static ICNKeyDescriptor DescriptorFromRequiredKeys ();
	public static CNContact[] GetContactsFromData (Foundation.NSData data, out Foundation.NSError error);
	public static Foundation.NSData GetDataFromContacts (CNContact[] contacts, out Foundation.NSError error);
}
</pre>

### New Type Contacts.CNContainer

<pre style='color: green'>
public class CNContainer : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContainer ();
	public CNContainer (Foundation.NSCoder coder);
	protected CNContainer (Foundation.NSObjectFlag t);
	protected CNContainer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual string Name { get; }
	public virtual CNContainerType Type { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type Contacts.CNContainer_PredicatesExtension

<pre style='color: green'>
public static class CNContainer_PredicatesExtension {
	// methods
	public static Foundation.NSPredicate GetPredicateForContainerOfContact (CNContainer This, string contactIdentifier);
	public static Foundation.NSPredicate GetPredicateForContainerOfGroup (CNContainer This, string groupIdentifier);
	public static Foundation.NSPredicate GetPredicateForContainers (CNContainer This, string[] identifiers);
}
</pre>

### New Type Contacts.CNContainerKey

<pre style='color: green'>
public static class CNContainerKey {
	// properties
	public static Foundation.NSString Identifier { get; }
	public static Foundation.NSString Name { get; }
	public static Foundation.NSString Type { get; }
}
</pre>

### New Type Contacts.CNContainerType

<pre style='color: green'>
[Serializable]
public enum CNContainerType {
	CardDav = 3,
	Exchange = 2,
	Local = 1,
	Unassigned = 0,
}
</pre>

### New Type Contacts.CNEntityType

<pre style='color: green'>
[Serializable]
public enum CNEntityType {
	Contacts = 0,
}
</pre>

### New Type Contacts.CNErrorCode

<pre style='color: green'>
[Serializable]
public enum CNErrorCode {
	AuthorizationDenied = 100,
	CommunicationError = 1,
	ContainmentCycle = 202,
	ContainmentScope = 203,
	DataAccessError = 2,
	InsertedRecordAlreadyExists = 201,
	ParentRecordDoesNotExist = 204,
	PolicyViolation = 500,
	PredicateInvalid = 400,
	RecordDoesNotExist = 200,
	ValidationConfigurationError = 302,
	ValidationMultipleErrors = 300,
	ValidationTypeMismatch = 301,
}
</pre>

### New Type Contacts.CNErrorUserInfoKey

<pre style='color: green'>
public static class CNErrorUserInfoKey {
	// properties
	public static Foundation.NSString AffectedRecordIdentifiers { get; }
	public static Foundation.NSString AffectedRecords { get; }
	public static Foundation.NSString KeyPaths { get; }
	public static Foundation.NSString ValidationErrors { get; }
}
</pre>

### New Type Contacts.CNGroup

<pre style='color: green'>
public class CNGroup : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNGroup ();
	public CNGroup (Foundation.NSCoder coder);
	protected CNGroup (Foundation.NSObjectFlag t);
	protected CNGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual string Name { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
</pre>

### New Type Contacts.CNGroup_PredicatesExtension

<pre style='color: green'>
public static class CNGroup_PredicatesExtension {
	// methods
	public static Foundation.NSPredicate GetPredicateForGroups (CNGroup This, string[] identifiers);
	public static Foundation.NSPredicate GetPredicateForGroupsInContainer (CNGroup This, string containerIdentifier);
	public static Foundation.NSPredicate GetPredicateForSubgroupsInGroup (CNGroup This, string parentGroupIdentifier);
}
</pre>

### New Type Contacts.CNGroupKey

<pre style='color: green'>
public static class CNGroupKey {
	// properties
	public static Foundation.NSString Identifier { get; }
	public static Foundation.NSString Name { get; }
}
</pre>

### New Type Contacts.CNInstantMessageAddress

<pre style='color: green'>
public class CNInstantMessageAddress : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNInstantMessageAddress ();
	public CNInstantMessageAddress (Foundation.NSCoder coder);
	protected CNInstantMessageAddress (Foundation.NSObjectFlag t);
	protected CNInstantMessageAddress (IntPtr handle);
	public CNInstantMessageAddress (string username, string service);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Service { get; }
	public virtual string Username { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static string LocalizeProperty (CNInstantMessageAddressOption property);
	public static string LocalizeProperty (Foundation.NSString propertyKey);
	public static string LocalizeService (CNInstantMessageServiceOption serviceOption);
	public static string LocalizeService (Foundation.NSString service);
}
</pre>

### New Type Contacts.CNInstantMessageAddressKey

<pre style='color: green'>
public static class CNInstantMessageAddressKey {
	// properties
	public static Foundation.NSString Service { get; }
	public static Foundation.NSString Username { get; }
}
</pre>

### New Type Contacts.CNInstantMessageAddressOption

<pre style='color: green'>
[Serializable]
public enum CNInstantMessageAddressOption {
	Service = 1,
	Username = 0,
}
</pre>

### New Type Contacts.CNInstantMessageServiceKey

<pre style='color: green'>
public static class CNInstantMessageServiceKey {
	// properties
	public static Foundation.NSString Aim { get; }
	public static Foundation.NSString Facebook { get; }
	public static Foundation.NSString GaduGadu { get; }
	public static Foundation.NSString GoogleTalk { get; }
	public static Foundation.NSString Icq { get; }
	public static Foundation.NSString Jabber { get; }
	public static Foundation.NSString Msn { get; }
	public static Foundation.NSString QQ { get; }
	public static Foundation.NSString Skype { get; }
	public static Foundation.NSString Yahoo { get; }
}
</pre>

### New Type Contacts.CNInstantMessageServiceOption

<pre style='color: green'>
[Serializable]
public enum CNInstantMessageServiceOption {
	Aim = 0,
	Facebook = 1,
	GaduGadu = 2,
	GoogleTalk = 3,
	Icq = 4,
	Jabber = 5,
	Msn = 6,
	QQ = 7,
	Skype = 8,
	Yahoo = 9,
}
</pre>

### New Type Contacts.CNKeyDescriptor

<pre style='color: green'>
public class CNKeyDescriptor : Foundation.NSObject, ICNKeyDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNKeyDescriptor ();
	public CNKeyDescriptor (Foundation.NSCoder coder);
	protected CNKeyDescriptor (Foundation.NSObjectFlag t);
	protected CNKeyDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type Contacts.CNLabelContactRelationKey

<pre style='color: green'>
public static class CNLabelContactRelationKey {
	// properties
	public static Foundation.NSString Assistant { get; }
	public static Foundation.NSString Brother { get; }
	public static Foundation.NSString Child { get; }
	public static Foundation.NSString Father { get; }
	public static Foundation.NSString Friend { get; }
	public static Foundation.NSString Manager { get; }
	public static Foundation.NSString Mother { get; }
	public static Foundation.NSString Parent { get; }
	public static Foundation.NSString Partner { get; }
	public static Foundation.NSString Sister { get; }
	public static Foundation.NSString Spouse { get; }
}
</pre>

### New Type Contacts.CNLabeledValue

<pre style='color: green'>
public class CNLabeledValue : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNLabeledValue ();
	public CNLabeledValue (Foundation.NSCoder coder);
	protected CNLabeledValue (Foundation.NSObjectFlag t);
	protected CNLabeledValue (IntPtr handle);
	public CNLabeledValue (string label, Foundation.NSObject value);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual string Label { get; }
	public virtual Foundation.NSObject Value { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static CNLabeledValue FromLabel (string label, Foundation.NSObject value);
	public virtual CNLabeledValue GetLabeledValue (Foundation.NSObject value);
	public virtual CNLabeledValue GetLabeledValue (string label, Foundation.NSObject value);
	public virtual CNLabeledValue GetLabeledValue (string label);
	public static string LocalizeLabel (Foundation.NSString labelKey);
}
</pre>

### New Type Contacts.CNLabelKey

<pre style='color: green'>
public static class CNLabelKey {
	// properties
	public static Foundation.NSString DateAnniversary { get; }
	public static Foundation.NSString EmailiCloud { get; }
	public static Foundation.NSString Home { get; }
	public static Foundation.NSString Other { get; }
	public static Foundation.NSString UrlAddressHomePage { get; }
	public static Foundation.NSString Work { get; }
}
</pre>

### New Type Contacts.CNLabelPhoneNumberKey

<pre style='color: green'>
public static class CNLabelPhoneNumberKey {
	// properties
	public static Foundation.NSString HomeFax { get; }
	public static Foundation.NSString iPhone { get; }
	public static Foundation.NSString Main { get; }
	public static Foundation.NSString Mobile { get; }
	public static Foundation.NSString OtherFax { get; }
	public static Foundation.NSString Pager { get; }
	public static Foundation.NSString WorkFax { get; }
}
</pre>

### New Type Contacts.CNMutableContact

<pre style='color: green'>
public class CNMutableContact : Contacts.CNContact, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNMutableContact ();
	public CNMutableContact (Foundation.NSCoder coder);
	protected CNMutableContact (Foundation.NSObjectFlag t);
	protected CNMutableContact (IntPtr handle);
	// properties
	public virtual Foundation.NSDateComponents Birthday { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSObject[] ContactRelations { get; set; }
	public virtual CNContactType ContactType { get; set; }
	public virtual Foundation.NSObject[] Dates { get; set; }
	public virtual string DepartmentName { get; set; }
	public virtual Foundation.NSObject[] EmailAddresses { get; set; }
	public virtual string FamilyName { get; set; }
	public virtual string GivenName { get; set; }
	public virtual Foundation.NSData ImageData { get; set; }
	public virtual Foundation.NSObject[] InstantMessageAddresses { get; set; }
	public virtual string JobTitle { get; set; }
	public virtual string MiddleName { get; set; }
	public virtual string NamePrefix { get; set; }
	public virtual string NameSuffix { get; set; }
	public virtual string Nickname { get; set; }
	public virtual Foundation.NSDateComponents NonGregorianBirthday { get; set; }
	public virtual string Note { get; set; }
	public virtual string OrganizationName { get; set; }
	public virtual Foundation.NSObject[] PhoneNumbers { get; set; }
	public virtual string PhoneticFamilyName { get; set; }
	public virtual string PhoneticGivenName { get; set; }
	public virtual string PhoneticMiddleName { get; set; }
	public virtual Foundation.NSObject[] PostalAddresses { get; set; }
	public virtual string PreviousFamilyName { get; set; }
	public virtual Foundation.NSObject[] SocialProfiles { get; set; }
	public virtual Foundation.NSObject[] UrlAddresses { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Contacts.CNMutableGroup

<pre style='color: green'>
public class CNMutableGroup : Contacts.CNGroup, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNMutableGroup ();
	public CNMutableGroup (Foundation.NSCoder coder);
	protected CNMutableGroup (Foundation.NSObjectFlag t);
	protected CNMutableGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
}
</pre>

### New Type Contacts.CNMutablePostalAddress

<pre style='color: green'>
public class CNMutablePostalAddress : Contacts.CNPostalAddress, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNMutablePostalAddress ();
	public CNMutablePostalAddress (Foundation.NSCoder coder);
	protected CNMutablePostalAddress (Foundation.NSObjectFlag t);
	protected CNMutablePostalAddress (IntPtr handle);
	// properties
	public virtual string City { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string Country { get; set; }
	public virtual string IsoCountryCode { get; set; }
	public virtual string PostalCode { get; set; }
	public virtual string State { get; set; }
	public virtual string Street { get; set; }
}
</pre>

### New Type Contacts.CNPhoneNumber

<pre style='color: green'>
public class CNPhoneNumber : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNPhoneNumber (Foundation.NSCoder coder);
	protected CNPhoneNumber (Foundation.NSObjectFlag t);
	protected CNPhoneNumber (IntPtr handle);
	public CNPhoneNumber (string stringValue);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string StringValue { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static CNPhoneNumber PhoneNumberWithStringValue (string stringValue);
}
</pre>

### New Type Contacts.CNPostalAddress

<pre style='color: green'>
public class CNPostalAddress : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNPostalAddress ();
	public CNPostalAddress (Foundation.NSCoder coder);
	protected CNPostalAddress (Foundation.NSObjectFlag t);
	protected CNPostalAddress (IntPtr handle);
	// properties
	public virtual string City { get; }
	public override IntPtr ClassHandle { get; }
	public virtual string Country { get; }
	public virtual string IsoCountryCode { get; }
	public virtual string PostalCode { get; }
	public virtual string State { get; }
	public virtual string Street { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static string LocalizeProperty (CNPostalAddressKeyOption option);
	public static string LocalizeProperty (Foundation.NSString property);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
</pre>

### New Type Contacts.CNPostalAddressFormatter

<pre style='color: green'>
public class CNPostalAddressFormatter : Foundation.NSFormatter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNPostalAddressFormatter ();
	public CNPostalAddressFormatter (Foundation.NSCoder coder);
	protected CNPostalAddressFormatter (Foundation.NSObjectFlag t);
	protected CNPostalAddressFormatter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString LocalizedPropertyNameAttribute { get; }
	public static Foundation.NSString PropertyAttribute { get; }
	// methods
	public static Foundation.NSAttributedString GetAttributedStringFrom (CNPostalAddress postalAddress, Foundation.NSDictionary attributes);
	public virtual Foundation.NSAttributedString GetAttributedStringFromPostalAddress (CNPostalAddress postalAddress, Foundation.NSDictionary attributes);
	public static string GetStringFrom (CNPostalAddress postalAddress);
	public virtual string GetStringFromPostalAddress (CNPostalAddress postalAddress);
}
</pre>

### New Type Contacts.CNPostalAddressKey

<pre style='color: green'>
public static class CNPostalAddressKey {
	// properties
	public static Foundation.NSString City { get; }
	public static Foundation.NSString Country { get; }
	public static Foundation.NSString IsoCountryCode { get; }
	public static Foundation.NSString PostalCode { get; }
	public static Foundation.NSString State { get; }
	public static Foundation.NSString Street { get; }
}
</pre>

### New Type Contacts.CNPostalAddressKeyOption

<pre style='color: green'>
[Serializable]
public enum CNPostalAddressKeyOption {
	City = 1,
	Country = 4,
	IsoCountryCode = 5,
	PostalCode = 3,
	State = 2,
	Street = 0,
}
</pre>

### New Type Contacts.CNSaveRequest

<pre style='color: green'>
public class CNSaveRequest : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public CNSaveRequest ();
	protected CNSaveRequest (Foundation.NSObjectFlag t);
	protected CNSaveRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void AddContact (CNMutableContact contact, string identifier);
	public virtual void AddGroup (CNMutableGroup group, string identifier);
	public virtual void AddMember (CNContact contact, CNGroup group);
	public virtual void AddSubgroup (CNGroup subgroup, CNGroup group);
	public virtual void DeleteContact (CNMutableContact contact);
	public virtual void DeleteGroup (CNMutableGroup group);
	public virtual void RemoveMember (CNContact contact, CNGroup group);
	public virtual void RemoveSubgroup (CNGroup subgroup, CNGroup group);
	public virtual void UpdateContact (CNMutableContact contact);
	public virtual void UpdateGroup (CNMutableGroup group);
}
</pre>

### New Type Contacts.CNSocialProfile

<pre style='color: green'>
public class CNSocialProfile : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNSocialProfile ();
	public CNSocialProfile (Foundation.NSCoder coder);
	protected CNSocialProfile (Foundation.NSObjectFlag t);
	protected CNSocialProfile (IntPtr handle);
	public CNSocialProfile (string url, string username, string userIdentifier, string service);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Service { get; }
	public virtual string UrlString { get; }
	public virtual string UserIdentifier { get; }
	public virtual string Username { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static string LocalizeProperty (CNSocialProfileOption option);
	public static string LocalizeProperty (Foundation.NSString key);
	public static string LocalizeService (CNSocialProfileServiceOption serviceOption);
	public static string LocalizeService (Foundation.NSString service);
}
</pre>

### New Type Contacts.CNSocialProfileKey

<pre style='color: green'>
public static class CNSocialProfileKey {
	// properties
	public static Foundation.NSString Service { get; }
	public static Foundation.NSString UrlString { get; }
	public static Foundation.NSString UserIdentifier { get; }
	public static Foundation.NSString Username { get; }
}
</pre>

### New Type Contacts.CNSocialProfileOption

<pre style='color: green'>
[Serializable]
public enum CNSocialProfileOption {
	Service = 3,
	UrlString = 0,
	UserIdentifier = 2,
	Username = 1,
}
</pre>

### New Type Contacts.CNSocialProfileServiceKey

<pre style='color: green'>
public static class CNSocialProfileServiceKey {
	// properties
	public static Foundation.NSString Facebook { get; }
	public static Foundation.NSString Flickr { get; }
	public static Foundation.NSString GameCenter { get; }
	public static Foundation.NSString LinkedIn { get; }
	public static Foundation.NSString MySpace { get; }
	public static Foundation.NSString SinaWeibo { get; }
	public static Foundation.NSString TencentWeibo { get; }
	public static Foundation.NSString Twitter { get; }
	public static Foundation.NSString Yelp { get; }
}
</pre>

### New Type Contacts.CNSocialProfileServiceOption

<pre style='color: green'>
[Serializable]
public enum CNSocialProfileServiceOption {
	Facebook = 0,
	Flickr = 1,
	GameCenter = 8,
	LinkedIn = 2,
	MySpace = 3,
	SinaWeibo = 4,
	TencentWeibo = 5,
	Twitter = 6,
	Yelp = 7,
}
</pre>

### New Type Contacts.ICNKeyDescriptor

<pre style='color: green'>
public interface ICNKeyDescriptor : ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding {
}
</pre>

## New Namespace ContactsUI

### New Type ContactsUI.CNContactPickerDelegate

<pre style='color: green'>
public class CNContactPickerDelegate : Foundation.NSObject, ICNContactPickerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContactPickerDelegate ();
	protected CNContactPickerDelegate (Foundation.NSObjectFlag t);
	protected CNContactPickerDelegate (IntPtr handle);
	// methods
	public virtual void ContactPickerDidCancel (CNContactPickerViewController picker);
	public virtual void DidSelectContact (CNContactPickerViewController picker, Contacts.CNContact contact);
	public virtual void DidSelectContactProperties (CNContactPickerViewController picker, Contacts.CNContactProperty[] contactProperties);
	public virtual void DidSelectContactProperty (CNContactPickerViewController picker, Contacts.CNContactProperty contactProperty);
	public virtual void DidSelectContacts (CNContactPickerViewController picker, Contacts.CNContact[] contacts);
}
</pre>

### New Type ContactsUI.CNContactPickerDelegate_Extensions

<pre style='color: green'>
public static class CNContactPickerDelegate_Extensions {
	// methods
	public static void ContactPickerDidCancel (ICNContactPickerDelegate This, CNContactPickerViewController picker);
	public static void DidSelectContact (ICNContactPickerDelegate This, CNContactPickerViewController picker, Contacts.CNContact contact);
	public static void DidSelectContactProperties (ICNContactPickerDelegate This, CNContactPickerViewController picker, Contacts.CNContactProperty[] contactProperties);
	public static void DidSelectContactProperty (ICNContactPickerDelegate This, CNContactPickerViewController picker, Contacts.CNContactProperty contactProperty);
	public static void DidSelectContacts (ICNContactPickerDelegate This, CNContactPickerViewController picker, Contacts.CNContact[] contacts);
}
</pre>

### New Type ContactsUI.CNContactPickerViewController

<pre style='color: green'>
public class CNContactPickerViewController : UIKit.UIViewController, System.Collections.IEnumerable, Foundation.INSCoding, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContactPickerViewController ();
	public CNContactPickerViewController (Foundation.NSCoder coder);
	protected CNContactPickerViewController (Foundation.NSObjectFlag t);
	protected CNContactPickerViewController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual ICNContactPickerDelegate Delegate { get; set; }
	public virtual Foundation.NSString[] DisplayedPropertyKeys { get; set; }
	public virtual Foundation.NSPredicate PredicateForEnablingContact { get; set; }
	public virtual Foundation.NSPredicate PredicateForSelectionOfContact { get; set; }
	public virtual Foundation.NSPredicate PredicateForSelectionOfProperty { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ContactsUI.CNContactViewController

<pre style='color: green'>
public class CNContactViewController : UIKit.UIViewController, System.Collections.IEnumerable, Foundation.INSCoding, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContactViewController ();
	public CNContactViewController (Foundation.NSCoder coder);
	protected CNContactViewController (Foundation.NSObjectFlag t);
	protected CNContactViewController (IntPtr handle);
	// properties
	public virtual bool AllowsActions { get; set; }
	public virtual bool AllowsEditing { get; set; }
	public virtual string AlternateName { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual Contacts.CNContact Contact { get; }
	public virtual Contacts.CNContactStore ContactStore { get; set; }
	public virtual ICNContactViewControllerDelegate Delegate { get; set; }
	public static Contacts.ICNKeyDescriptor DescriptorForRequiredKeys { get; }
	public virtual Foundation.NSString[] DisplayedPropertyKeys { get; set; }
	public virtual string Message { get; set; }
	public virtual Contacts.CNGroup ParentGroup { get; set; }
	public virtual bool ShouldShowLinkedContacts { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static CNContactViewController FromContact (Contacts.CNContact contact);
	public static CNContactViewController FromNewContact (Contacts.CNContact contact);
	public static CNContactViewController FromUnknownContact (Contacts.CNContact contact);
	public virtual void HighlightProperty (Foundation.NSString key, string identifier);
}
</pre>

### New Type ContactsUI.CNContactViewControllerDelegate

<pre style='color: green'>
public class CNContactViewControllerDelegate : Foundation.NSObject, ICNContactViewControllerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CNContactViewControllerDelegate ();
	protected CNContactViewControllerDelegate (Foundation.NSObjectFlag t);
	protected CNContactViewControllerDelegate (IntPtr handle);
	// methods
	public virtual void DidSelectContact (CNContactPickerViewController picker, Contacts.CNContact contact);
	public virtual bool ShouldPerformDefaultAction (CNContactViewController viewController, Contacts.CNContactProperty property);
}
</pre>

### New Type ContactsUI.CNContactViewControllerDelegate_Extensions

<pre style='color: green'>
public static class CNContactViewControllerDelegate_Extensions {
	// methods
	public static void DidSelectContact (ICNContactViewControllerDelegate This, CNContactPickerViewController picker, Contacts.CNContact contact);
	public static bool ShouldPerformDefaultAction (ICNContactViewControllerDelegate This, CNContactViewController viewController, Contacts.CNContactProperty property);
}
</pre>

### New Type ContactsUI.ICNContactPickerDelegate

<pre style='color: green'>
public interface ICNContactPickerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type ContactsUI.ICNContactViewControllerDelegate

<pre style='color: green'>
public interface ICNContactViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

## New Namespace CoreSpotlight

### New Type CoreSpotlight.CSCustomAttributeKey

<pre style='color: green'>
public class CSCustomAttributeKey : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CSCustomAttributeKey ();
	public CSCustomAttributeKey (Foundation.NSCoder coder);
	protected CSCustomAttributeKey (Foundation.NSObjectFlag t);
	protected CSCustomAttributeKey (IntPtr handle);
	public CSCustomAttributeKey (string keyName);
	public CSCustomAttributeKey (string keyName, bool searchable, bool searchableByDefault, bool unique, bool multiValued);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string KeyName { get; }
	public virtual bool MultiValued { get; }
	public virtual bool Searchable { get; }
	public virtual bool SearchableByDefault { get; }
	public virtual bool Unique { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type CoreSpotlight.CSExposureProgramKey

<pre style='color: green'>
public static class CSExposureProgramKey {
	// properties
	public static Foundation.NSString Aperture { get; }
	public static Foundation.NSString Manual { get; }
	public static Foundation.NSString Normal { get; }
	public static Foundation.NSString Priority { get; }
}
</pre>

### New Type CoreSpotlight.CSFileProtection

<pre style='color: green'>
[Serializable]
public enum CSFileProtection {
	Complete = 1,
	CompleteUnlessOpen = 2,
	CompleteUntilFirstUserAuthentication = 3,
	None = 0,
}
</pre>

### New Type CoreSpotlight.CSIndexErrorCode

<pre style='color: green'>
[Serializable]
public enum CSIndexErrorCode {
	IndexUnavailableError = -1000,
	InvalidClientStateError = -1002,
	InvalidItemError = -1001,
	QuotaExceeded = -1004,
	RemoteConnectionError = -1003,
	UnknownError = -1,
}
</pre>

### New Type CoreSpotlight.CSIndexExtensionRequestHandler

<pre style='color: green'>
public class CSIndexExtensionRequestHandler : Foundation.NSObject, ICSSearchableIndexDelegate, Foundation.INSExtensionRequestHandling, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CSIndexExtensionRequestHandler ();
	protected CSIndexExtensionRequestHandler (Foundation.NSObjectFlag t);
	protected CSIndexExtensionRequestHandler (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void BeginRequestWithExtensionContext (Foundation.NSExtensionContext context);
	public virtual void ReindexAllSearchableItems (CSSearchableIndex searchableIndex, System.Action acknowledgementHandler);
	public virtual void ReindexSearchableItems (CSSearchableIndex searchableIndex, string[] identifiers, System.Action acknowledgementHandler);
}
</pre>

### New Type CoreSpotlight.CSLocalizedString

<pre style='color: green'>
public class CSLocalizedString : Foundation.NSString, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CSLocalizedString ();
	protected CSLocalizedString (Foundation.NSObjectFlag t);
	protected CSLocalizedString (IntPtr handle);
	public CSLocalizedString (Foundation.NSDictionary localizedStrings);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual string GetLocalizedString ();
}
</pre>

### New Type CoreSpotlight.CSMailboxKey

<pre style='color: green'>
public static class CSMailboxKey {
	// properties
	public static Foundation.NSString Archive { get; }
	public static Foundation.NSString Drafts { get; }
	public static Foundation.NSString Inbox { get; }
	public static Foundation.NSString Junk { get; }
	public static Foundation.NSString Sent { get; }
	public static Foundation.NSString Trash { get; }
}
</pre>

### New Type CoreSpotlight.CSMeteringModeKey

<pre style='color: green'>
public static class CSMeteringModeKey {
	// properties
	public static Foundation.NSString Average { get; }
	public static Foundation.NSString CenterWeightedAverage { get; }
	public static Foundation.NSString MultiSpot { get; }
	public static Foundation.NSString Partial { get; }
	public static Foundation.NSString Pattern { get; }
	public static Foundation.NSString Spot { get; }
	public static Foundation.NSString Unknown { get; }
}
</pre>

### New Type CoreSpotlight.CSPerson

<pre style='color: green'>
public class CSPerson : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CSPerson ();
	public CSPerson (Foundation.NSCoder coder);
	protected CSPerson (Foundation.NSObjectFlag t);
	protected CSPerson (IntPtr handle);
	public CSPerson (string displayName, string[] handles, Foundation.NSString handleIdentifier);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string ContactIdentifier { get; set; }
	public virtual string DisplayName { get; }
	public virtual Foundation.NSString HandleIdentifier { get; }
	public virtual string[] Handles { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type CoreSpotlight.CSSearchableIndex

<pre style='color: green'>
public class CSSearchableIndex : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public CSSearchableIndex ();
	protected CSSearchableIndex (Foundation.NSObjectFlag t);
	protected CSSearchableIndex (IntPtr handle);
	public CSSearchableIndex (string name);
	public CSSearchableIndex (string name, Foundation.NSString protectionClass);
	// properties
	public override IntPtr ClassHandle { get; }
	public static CSSearchableIndex DefaultSearchableIndex { get; }
	public virtual ICSSearchableIndexDelegate IndexDelegate { get; set; }
	// methods
	public virtual void Delete (string[] identifiers, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual void DeleteAll (System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual void DeleteWithDomain (string[] domainIdentifiers, System.Action&lt;Foundation.NSError&gt; completionHandler);
	protected override void Dispose (bool disposing);
	public static CSSearchableIndex FromName (string name, CSFileProtection? protectionOption);
	public virtual void Index (CSSearchableItem[] items, System.Action&lt;Foundation.NSError&gt; completionHandler);
}
</pre>

### New Type CoreSpotlight.CSSearchableIndex_CSOptionalBatchingExtension

<pre style='color: green'>
public static class CSSearchableIndex_CSOptionalBatchingExtension {
	// methods
	public static void BeginIndexBatch (CSSearchableIndex This);
	public static void EndIndexBatch (CSSearchableIndex This, Foundation.NSData clientState, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public static void FetchLastClientState (CSSearchableIndex This, CSSearchableIndexFetchHandler completionHandler);
}
</pre>

### New Type CoreSpotlight.CSSearchableIndexDelegate

<pre style='color: green'>
public abstract class CSSearchableIndexDelegate : Foundation.NSObject, ICSSearchableIndexDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected CSSearchableIndexDelegate ();
	protected CSSearchableIndexDelegate (Foundation.NSObjectFlag t);
	protected CSSearchableIndexDelegate (IntPtr handle);
	// methods
	public virtual void ReindexAllSearchableItems (CSSearchableIndex searchableIndex, System.Action acknowledgementHandler);
	public virtual void ReindexSearchableItems (CSSearchableIndex searchableIndex, string[] identifiers, System.Action acknowledgementHandler);
}
</pre>

### New Type CoreSpotlight.CSSearchableIndexFetchHandler

<pre style='color: green'>
public sealed delegate CSSearchableIndexFetchHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CSSearchableIndexFetchHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSData clientState, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSData clientState, Foundation.NSError error);
}
</pre>

### New Type CoreSpotlight.CSSearchableItem

<pre style='color: green'>
public class CSSearchableItem : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CSSearchableItem ();
	public CSSearchableItem (Foundation.NSCoder coder);
	protected CSSearchableItem (Foundation.NSObjectFlag t);
	protected CSSearchableItem (IntPtr handle);
	public CSSearchableItem (string uniqueIdentifier, string domainIdentifier, CSSearchableItemAttributeSet attributeSet);
	// properties
	public static Foundation.NSString ActionType { get; }
	public static Foundation.NSString ActivityIdentifier { get; }
	public virtual CSSearchableItemAttributeSet AttributeSet { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string DomainIdentifier { get; set; }
	public virtual Foundation.NSDate ExpirationDate { get; set; }
	public virtual string UniqueIdentifier { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type CoreSpotlight.CSSearchableItemAttributeSet

<pre style='color: green'>
public class CSSearchableItemAttributeSet : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public CSSearchableItemAttributeSet ();
	public CSSearchableItemAttributeSet (Foundation.NSCoder coder);
	protected CSSearchableItemAttributeSet (Foundation.NSObjectFlag t);
	protected CSSearchableItemAttributeSet (IntPtr handle);
	public CSSearchableItemAttributeSet (string itemContentType);
	// properties
	public virtual string[] AccountHandles { get; set; }
	public virtual string AccountIdentifier { get; set; }
	public virtual string AcquisitionMake { get; set; }
	public virtual string AcquisitionModel { get; set; }
	public virtual Foundation.NSDate AddedDate { get; set; }
	public virtual CSPerson[] AdditionalRecipients { get; set; }
	public virtual string Album { get; set; }
	public virtual string[] AlternateNames { get; set; }
	public virtual Foundation.NSNumber Altitude { get; set; }
	public virtual Foundation.NSNumber Aperture { get; set; }
	public virtual string Artist { get; set; }
	public virtual string[] Audiences { get; set; }
	public virtual Foundation.NSNumber AudioBitRate { get; set; }
	public virtual Foundation.NSNumber AudioChannelCount { get; set; }
	public virtual string AudioEncodingApplication { get; set; }
	public virtual Foundation.NSNumber AudioSampleRate { get; set; }
	public virtual Foundation.NSNumber AudioTrackNumber { get; set; }
	public virtual string[] AuthorAddresses { get; set; }
	public virtual string[] AuthorEmailAddresses { get; set; }
	public virtual string[] AuthorNames { get; set; }
	public virtual CSPerson[] Authors { get; set; }
	public virtual Foundation.NSNumber BitsPerSample { get; set; }
	public virtual string CameraOwner { get; set; }
	public virtual string City { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string[] Codecs { get; set; }
	public virtual string ColorSpace { get; set; }
	public virtual string Comment { get; set; }
	public virtual Foundation.NSDate CompletionDate { get; set; }
	public virtual string Composer { get; set; }
	public virtual string[] ContactKeywords { get; set; }
	public virtual Foundation.NSDate ContentCreationDate { get; set; }
	public virtual string ContentDescription { get; set; }
	public virtual Foundation.NSDate ContentModificationDate { get; set; }
	public virtual Foundation.NSNumber ContentRating { get; set; }
	public virtual string[] ContentSources { get; set; }
	public virtual string ContentType { get; set; }
	public virtual string[] ContentTypeTree { get; set; }
	public virtual Foundation.NSUrl ContentUrl { get; set; }
	public virtual string[] Contributors { get; set; }
	public virtual string Copyright { get; set; }
	public virtual string Country { get; set; }
	public virtual string[] Coverage { get; set; }
	public virtual string Creator { get; set; }
	public virtual Foundation.NSNumber DeliveryType { get; set; }
	public virtual string Director { get; set; }
	public virtual string DisplayName { get; set; }
	public virtual Foundation.NSDate DownloadedDate { get; set; }
	public virtual Foundation.NSDate DueDate { get; set; }
	public virtual Foundation.NSNumber Duration { get; set; }
	public virtual string[] Editors { get; set; }
	public virtual string[] EmailAddresses { get; set; }
	public virtual Foundation.NSDictionary EmailHeaders { get; set; }
	public virtual string[] EncodingApplications { get; set; }
	public virtual Foundation.NSDate EndDate { get; set; }
	public virtual string ExifGpsVersion { get; set; }
	public virtual string ExifVersion { get; set; }
	public virtual Foundation.NSNumber ExposureMode { get; set; }
	public virtual string ExposureProgram { get; set; }
	public virtual Foundation.NSNumber ExposureTime { get; set; }
	public virtual string ExposureTimeString { get; set; }
	public virtual Foundation.NSNumber FlashOn { get; set; }
	public virtual Foundation.NSNumber FNumber { get; set; }
	public virtual Foundation.NSNumber FocalLength { get; set; }
	public virtual Foundation.NSNumber FocalLength35mm { get; set; }
	public virtual string[] FontNames { get; set; }
	public virtual Foundation.NSNumber GeneralMidiSequence { get; set; }
	public virtual string Genre { get; set; }
	public virtual string GpsAreaInformation { get; set; }
	public virtual Foundation.NSDate GpsDateStamp { get; set; }
	public virtual Foundation.NSNumber GpsDestBearing { get; set; }
	public virtual Foundation.NSNumber GpsDestDistance { get; set; }
	public virtual Foundation.NSNumber GpsDestLatitude { get; set; }
	public virtual Foundation.NSNumber GpsDestLongitude { get; set; }
	public virtual Foundation.NSNumber GpsDifferental { get; set; }
	public virtual Foundation.NSNumber GpsDop { get; set; }
	public virtual string GpsMapDatum { get; set; }
	public virtual string GpsMeasureMode { get; set; }
	public virtual string GpsProcessingMethod { get; set; }
	public virtual string GpsStatus { get; set; }
	public virtual Foundation.NSNumber GpsTrack { get; set; }
	public virtual Foundation.NSNumber HasAlphaChannel { get; set; }
	public virtual string Headline { get; set; }
	public virtual CSPerson[] HiddenAdditionalRecipients { get; set; }
	public virtual Foundation.NSData HtmlContentData { get; set; }
	public virtual string Identifier { get; set; }
	public virtual Foundation.NSNumber ImageDirection { get; set; }
	public virtual Foundation.NSDate[] ImportantDates { get; set; }
	public virtual string Information { get; set; }
	public virtual string[] InstantMessageAddresses { get; set; }
	public virtual string Instructions { get; set; }
	public virtual Foundation.NSNumber IsoSpeed { get; set; }
	public virtual string KeySignature { get; set; }
	public virtual string[] Keywords { get; set; }
	public virtual string Kind { get; set; }
	public virtual string[] Languages { get; set; }
	public virtual Foundation.NSDate LastUsedDate { get; set; }
	public virtual Foundation.NSNumber Latitude { get; set; }
	public virtual string[] LayerNames { get; set; }
	public virtual string LensModel { get; set; }
	public virtual Foundation.NSNumber LikelyJunk { get; set; }
	public virtual Foundation.NSNumber Local { get; set; }
	public virtual Foundation.NSNumber Longitude { get; set; }
	public virtual string Lyricist { get; set; }
	public virtual string[] MailboxIdentifiers { get; set; }
	public virtual Foundation.NSNumber MaxAperture { get; set; }
	public virtual string[] MediaTypes { get; set; }
	public virtual Foundation.NSDate MetadataModificationDate { get; set; }
	public virtual string MeteringMode { get; set; }
	public virtual string MusicalGenre { get; set; }
	public virtual string MusicalInstrumentCategory { get; set; }
	public virtual string MusicalInstrumentName { get; set; }
	public virtual string NamedLocation { get; set; }
	public virtual string[] Organizations { get; set; }
	public virtual Foundation.NSNumber Orientation { get; set; }
	public virtual string OriginalFormat { get; set; }
	public virtual string OriginalSource { get; set; }
	public virtual Foundation.NSNumber PageCount { get; set; }
	public virtual Foundation.NSNumber PageHeight { get; set; }
	public virtual Foundation.NSNumber PageWidth { get; set; }
	public virtual string[] Participants { get; set; }
	public virtual string Path { get; set; }
	public virtual string[] Performers { get; set; }
	public virtual string[] PhoneNumbers { get; set; }
	public virtual Foundation.NSNumber PixelCount { get; set; }
	public virtual Foundation.NSNumber PixelHeight { get; set; }
	public virtual Foundation.NSNumber PixelWidth { get; set; }
	public virtual Foundation.NSNumber PlayCount { get; set; }
	public virtual CSPerson[] PrimaryRecipients { get; set; }
	public virtual string Producer { get; set; }
	public virtual string ProfileName { get; set; }
	public virtual string[] Projects { get; set; }
	public virtual string[] Publishers { get; set; }
	public virtual Foundation.NSNumber Rating { get; set; }
	public virtual string[] RecipientAddresses { get; set; }
	public virtual string[] RecipientEmailAddresses { get; set; }
	public virtual string[] RecipientNames { get; set; }
	public virtual Foundation.NSDate RecordingDate { get; set; }
	public virtual Foundation.NSNumber RedEyeOn { get; set; }
	public virtual string RelatedUniqueIdentifier { get; set; }
	public virtual Foundation.NSNumber ResolutionHeightDPI { get; set; }
	public virtual Foundation.NSNumber ResolutionWidthDpi { get; set; }
	public virtual string Rights { get; set; }
	public virtual string Role { get; set; }
	public virtual string SecurityMethod { get; set; }
	public virtual Foundation.NSNumber Speed { get; set; }
	public virtual Foundation.NSDate StartDate { get; set; }
	public virtual string StateOrProvince { get; set; }
	public virtual Foundation.NSNumber Streamable { get; set; }
	public virtual string Subject { get; set; }
	public virtual Foundation.NSNumber Tempo { get; set; }
	public virtual string TextContent { get; set; }
	public virtual string Theme { get; set; }
	public virtual Foundation.NSData ThumbnailData { get; set; }
	public virtual Foundation.NSUrl ThumbnailUrl { get; set; }
	public virtual string TimeSignature { get; set; }
	public virtual Foundation.NSDate Timestamp { get; set; }
	public virtual string Title { get; set; }
	public virtual Foundation.NSNumber TotalBitRate { get; set; }
	public virtual Foundation.NSUrl Url { get; set; }
	public virtual string Version { get; set; }
	public virtual Foundation.NSNumber VideoBitRate { get; set; }
	public virtual Foundation.NSNumber WhiteBalance { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type CoreSpotlight.ICSSearchableIndexDelegate

<pre style='color: green'>
public interface ICSSearchableIndexDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void ReindexAllSearchableItems (CSSearchableIndex searchableIndex, System.Action acknowledgementHandler);
	public virtual void ReindexSearchableItems (CSSearchableIndex searchableIndex, string[] identifiers, System.Action acknowledgementHandler);
}
</pre>

## New Namespace ModelIO

### New Type ModelIO.IMDLComponent

<pre style='color: green'>
public interface IMDLComponent : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type ModelIO.IMDLMeshBuffer

<pre style='color: green'>
public interface IMDLMeshBuffer : ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSCopying {
	// properties
	public virtual Foundation.NSData Map { get; }
	// methods
	public virtual void Offset (Foundation.NSData data, uint offset);
}
</pre>

### New Type ModelIO.IMDLMeshBufferAllocator

<pre style='color: green'>
public interface IMDLMeshBufferAllocator : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual IMDLMeshBuffer NewBuffer (uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferFromZone (IMDLMeshBufferZone zone, uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferFromZone (IMDLMeshBufferZone zone, Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferWithData (Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBufferZone NewZone (uint capacity);
}
</pre>

### New Type ModelIO.IMDLMeshBufferZone

<pre style='color: green'>
public interface IMDLMeshBufferZone : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type ModelIO.IMDLNamed

<pre style='color: green'>
public interface IMDLNamed : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type ModelIO.IMDLObjectContainerComponent

<pre style='color: green'>
public interface IMDLObjectContainerComponent : ObjCRuntime.INativeObject, System.IDisposable, IMDLComponent {
	// properties
	public virtual MDLObject[] Objects { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type ModelIO.IMDLTransformComponent

<pre style='color: green'>
public interface IMDLTransformComponent : ObjCRuntime.INativeObject, System.IDisposable, IMDLComponent {
	// properties
	public virtual OpenTK.Matrix4 Matrix { get; set; }
	public virtual double MaximumTime { get; }
	public virtual double MinimumTime { get; }
}
</pre>

### New Type ModelIO.MDLAreaLight

<pre style='color: green'>
public class MDLAreaLight : ModelIO.MDLPhysicallyPlausibleLight, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected MDLAreaLight (Foundation.NSObjectFlag t);
	protected MDLAreaLight (IntPtr handle);
	// properties
	public virtual float AreaRadius { get; set; }
	public virtual float Aspect { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2 SuperEllipticPower { get; set; }
}
</pre>

### New Type ModelIO.MDLAsset

<pre style='color: green'>
public class MDLAsset : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLAsset ();
	protected MDLAsset (Foundation.NSObjectFlag t);
	protected MDLAsset (IntPtr handle);
	public MDLAsset (Foundation.NSUrl URL);
	public MDLAsset (Foundation.NSUrl URL, MDLVertexDescriptor vertexDescriptor, IMDLMeshBufferAllocator bufferAllocator);
	// properties
	public virtual MDLAxisAlignedBoundingBox BoundingBox { get; }
	public virtual IMDLMeshBufferAllocator BufferAllocator { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual double EndTime { get; set; }
	public virtual double FrameInterval { get; set; }
	public MDLObject Item { get; }
	public virtual double StartTime { get; set; }
	public virtual Foundation.NSUrl URL { get; }
	public virtual MDLVertexDescriptor VertexDescriptor { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	public virtual MDLAxisAlignedBoundingBox BoundingBoxAtTime (double time);
	public static bool CanExportFileExtension (string extension);
	public static bool CanImportFileExtension (string extension);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual bool ExportAssetToURL (Foundation.NSUrl URL);
	public virtual MDLObject GetObjectAtIndex (uint index);
	public virtual MDLObject GetObjectAtIndexedSubscript (uint index);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type ModelIO.MDLAxisAlignedBoundingBox

<pre style='color: green'>
public struct MDLAxisAlignedBoundingBox {
	// fields
	public OpenTK.Vector3 MaxBounds;
	public OpenTK.Vector3 MinBounds;
}
</pre>

### New Type ModelIO.MDLComponent

<pre style='color: green'>
public class MDLComponent : Foundation.NSObject, IMDLComponent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLComponent ();
	protected MDLComponent (Foundation.NSObjectFlag t);
	protected MDLComponent (IntPtr handle);
}
</pre>

### New Type ModelIO.MDLGeometryKind

<pre style='color: green'>
[Serializable]
public enum MDLGeometryKind {
	Lines = 1,
	Points = 0,
	Quads = 4,
	Triangles = 2,
	TriangleStrips = 3,
}
</pre>

### New Type ModelIO.MDLIndexBitDepth

<pre style='color: green'>
[Serializable]
public enum MDLIndexBitDepth {
	Invalid = 0,
	UInt16 = 16,
	UInt32 = 32,
	UInt8 = 8,
}
</pre>

### New Type ModelIO.MDLLight

<pre style='color: green'>
public class MDLLight : ModelIO.MDLObject, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLLight ();
	protected MDLLight (Foundation.NSObjectFlag t);
	protected MDLLight (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLLightType LightType { get; }
	// methods
	public virtual CoreGraphics.CGColor EvaluatedColorFromVector (OpenTK.Vector3 vector);
}
</pre>

### New Type ModelIO.MDLLightProbe

<pre style='color: green'>
public class MDLLightProbe : ModelIO.MDLLight, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLLightProbe ();
	protected MDLLightProbe (Foundation.NSObjectFlag t);
	protected MDLLightProbe (IntPtr handle);
	public MDLLightProbe (MDLTexture reflectiveTexture, MDLTexture irradianceTexture);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLTexture IrradianceTexture { get; }
	public virtual MDLTexture ReflectiveTexture { get; }
	public virtual Foundation.NSData SphericalHarmonicsCoefficients { get; }
	public virtual uint SphericalHarmonicsLevel { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void GenerateSphericalHarmonicsFromIrradiance (uint sphericalHarmonicsLevel);
}
</pre>

### New Type ModelIO.MDLLightType

<pre style='color: green'>
[Serializable]
public enum MDLLightType {
	Ambient = 1,
	Directional = 2,
	DiscArea = 6,
	Environment = 11,
	Linear = 5,
	Photometric = 9,
	Point = 4,
	Probe = 10,
	RectangularArea = 7,
	Spot = 3,
	SuperElliptical = 8,
	Unknown = 0,
}
</pre>

### New Type ModelIO.MDLMaterial

<pre style='color: green'>
public class MDLMaterial : Foundation.NSObject, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLMaterial ();
	protected MDLMaterial (Foundation.NSObjectFlag t);
	protected MDLMaterial (IntPtr handle);
	public MDLMaterial (string name, MDLScatteringFunction scatteringFunction);
	// properties
	public virtual MDLMaterial BaseMaterial { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual string Name { get; set; }
	public virtual MDLScatteringFunction ScatteringFunction { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual MDLMaterialProperty GetProperty (string name);
	public virtual MDLMaterialProperty GetProperty (MDLMaterialSemantic semantic);
	public virtual void RemoveAllProperties ();
	public virtual void RemoveProperty (MDLMaterialProperty property);
	public virtual void SetProperty (MDLMaterialProperty property);
}
</pre>

### New Type ModelIO.MDLMaterialMipMapFilterMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialMipMapFilterMode {
	Linear = 1,
	Nearest = 0,
}
</pre>

### New Type ModelIO.MDLMaterialProperty

<pre style='color: green'>
public class MDLMaterialProperty : Foundation.NSObject, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected MDLMaterialProperty (Foundation.NSObjectFlag t);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, MDLTextureSampler textureSampler);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, string stringValue);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, Foundation.NSUrl URL);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Matrix4 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector4 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector3 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector2 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, float value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic);
	protected MDLMaterialProperty (IntPtr handle);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, CoreGraphics.CGColor color);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGColor Color { get; set; }
	public virtual OpenTK.Vector2 Float2Value { get; set; }
	public virtual OpenTK.Vector3 Float3Value { get; set; }
	public virtual OpenTK.Vector4 Float4Value { get; set; }
	public virtual float FloatValue { get; set; }
	public virtual OpenTK.Matrix4 Matrix4x4 { get; set; }
	public virtual string Name { get; set; }
	public virtual MDLMaterialSemantic Semantic { get; set; }
	public virtual string StringValue { get; set; }
	public virtual MDLTextureSampler TextureSamplerValue { get; set; }
	public virtual MDLMaterialPropertyType Type { get; }
	public virtual Foundation.NSUrl UrlValue { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetProperties (MDLMaterialProperty property);
}
</pre>

### New Type ModelIO.MDLMaterialPropertyType

<pre style='color: green'>
[Serializable]
public enum MDLMaterialPropertyType {
	Color = 4,
	Float = 5,
	Float2 = 6,
	Float3 = 7,
	Float4 = 8,
	Matrix44 = 9,
	None = 0,
	String = 1,
	Texture = 3,
	Url = 2,
}
</pre>

### New Type ModelIO.MDLMaterialSemantic

<pre style='color: green'>
[Serializable]
public enum MDLMaterialSemantic {
	AmbientOcclusion = 20,
	AmbientOcclusionScale = 21,
	Anisotropic = 6,
	BaseColor = 0,
	Bump = 12,
	Clearcoat = 9,
	ClearcoatGloss = 10,
	Displacement = 18,
	DisplacementScale = 19,
	Emission = 11,
	InterfaceIndexOfRefraction = 14,
	MaterialIndexOfRefraction = 15,
	Metallic = 2,
	None = 32768,
	ObjectSpaceNormal = 16,
	Opacity = 13,
	Roughness = 5,
	Sheen = 7,
	SheenTint = 8,
	Specular = 3,
	SpecularTint = 4,
	Subsurface = 1,
	TangentSpaceNormal = 17,
	UserDefined = 32769,
}
</pre>

### New Type ModelIO.MDLMaterialTextureFilterMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialTextureFilterMode {
	Linear = 1,
	Nearest = 0,
}
</pre>

### New Type ModelIO.MDLMaterialTextureWrapMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialTextureWrapMode {
	Clamp = 0,
	Mirror = 2,
	Repeat = 1,
}
</pre>

### New Type ModelIO.MDLMesh

<pre style='color: green'>
public class MDLMesh : ModelIO.MDLObject, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLMesh ();
	protected MDLMesh (Foundation.NSObjectFlag t);
	protected MDLMesh (IntPtr handle);
	public MDLMesh (IMDLMeshBuffer vertexBuffer, uint vertexCount, MDLVertexDescriptor descriptor, MDLSubmesh[] submeshes);
	public MDLMesh (IMDLMeshBuffer[] vertexBuffers, uint vertexCount, MDLVertexDescriptor descriptor, MDLSubmesh[] submeshes);
	// properties
	public virtual MDLAxisAlignedBoundingBox BoundingBox { get; }
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSMutableArray Submeshes { get; }
	public virtual Foundation.NSMutableArray VertexBuffers { get; }
	public virtual uint VertexCount { get; }
	public virtual MDLVertexDescriptor VertexDescriptor { get; set; }
	// methods
	public virtual void AddAttribute (string name, MDLVertexFormat format);
	public virtual void AddNormals (string name, float creaseThreshold);
	public virtual void AddTangentBasis (string textureCoordinateAttributeName, string tangentAttributeName, string bitangentAttributeName);
	public virtual void AddTangentBasisWithNormals (string textureCoordinateAttributeName, string normalAttributeName, string tangentAttributeName);
	public static MDLMesh CreateBox (OpenTK.Vector3 dimensions, OpenTK.Vector3i segments, bool inwardNormals, MDLGeometryKind geometryType, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateCylindroid (float height, OpenTK.Vector2 radii, uint radialSegments, uint verticalSegments, MDLGeometryKind geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateEllipsoid (OpenTK.Vector3 radii, uint radialSegments, uint verticalSegments, MDLGeometryKind geometryType, bool inwardNormals, bool hemisphere, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateEllipticalCone (float height, OpenTK.Vector2 radii, uint radialSegments, uint verticalSegments, MDLGeometryKind geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateIcosahedron (float radius, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static Foundation.NSObject CreatePlane (OpenTK.Vector2 dimensions, OpenTK.Vector2i segments, MDLGeometryKind geometryType, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateSubdividedMesh (MDLMesh mesh, uint submeshIndex, uint subdivisionLevels);
	protected override void Dispose (bool disposing);
	public virtual bool GenerateAmbientOcclusionTexture (float bakeQuality, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateAmbientOcclusionTexture (OpenTK.Vector2i textureSize, nint raysPerSample, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateAmbientOcclusionVertexColors (nint raysPerSample, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual bool GenerateAmbientOcclusionVertexColors (float bakeQuality, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual bool GenerateLightMapTexture (float bakeQuality, MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateLightMapTexture (OpenTK.Vector2i textureSize, MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateLightMapVertexColors (MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual MDLVertexAttributeData GetVertexAttributeDataForAttribute (string attributeName);
	public virtual void MakeVerticesUnique ();
}
</pre>

### New Type ModelIO.MDLMeshBuffer

<pre style='color: green'>
public abstract class MDLMeshBuffer : Foundation.NSObject, IMDLMeshBuffer, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected MDLMeshBuffer ();
	protected MDLMeshBuffer (Foundation.NSObjectFlag t);
	protected MDLMeshBuffer (IntPtr handle);
	// properties
	public virtual IMDLMeshBufferAllocator Allocator { get; }
	public virtual uint Length { get; }
	public virtual Foundation.NSData Map { get; }
	public virtual MDLMeshBufferType Type { get; }
	public virtual IMDLMeshBufferZone Zone { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void Offset (Foundation.NSData data, uint offset);
}
</pre>

### New Type ModelIO.MDLMeshBuffer_Extensions

<pre style='color: green'>
public static class MDLMeshBuffer_Extensions {
	// methods
	public static IMDLMeshBufferAllocator GetAllocator (IMDLMeshBuffer This);
	public static uint GetLength (IMDLMeshBuffer This);
	public static MDLMeshBufferType GetType (IMDLMeshBuffer This);
	public static IMDLMeshBufferZone GetZone (IMDLMeshBuffer This);
}
</pre>

### New Type ModelIO.MDLMeshBufferAllocator

<pre style='color: green'>
public abstract class MDLMeshBufferAllocator : Foundation.NSObject, IMDLMeshBufferAllocator, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected MDLMeshBufferAllocator ();
	protected MDLMeshBufferAllocator (Foundation.NSObjectFlag t);
	protected MDLMeshBufferAllocator (IntPtr handle);
	// methods
	public virtual IMDLMeshBuffer NewBuffer (uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferFromZone (IMDLMeshBufferZone zone, uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferFromZone (IMDLMeshBufferZone zone, Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer NewBufferWithData (Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBufferZone NewZone (uint capacity);
}
</pre>

### New Type ModelIO.MDLMeshBufferType

<pre style='color: green'>
[Serializable]
public enum MDLMeshBufferType {
	Index = 2,
	Vertex = 1,
}
</pre>

### New Type ModelIO.MDLMeshBufferZone

<pre style='color: green'>
public class MDLMeshBufferZone : Foundation.NSObject, IMDLMeshBufferZone, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLMeshBufferZone ();
	protected MDLMeshBufferZone (Foundation.NSObjectFlag t);
	protected MDLMeshBufferZone (IntPtr handle);
	// properties
	public virtual IMDLMeshBufferAllocator Allocator { get; }
	public virtual uint Capacity { get; }
}
</pre>

### New Type ModelIO.MDLMeshBufferZone_Extensions

<pre style='color: green'>
public static class MDLMeshBufferZone_Extensions {
	// methods
	public static IMDLMeshBufferAllocator GetAllocator (IMDLMeshBufferZone This);
	public static uint GetCapacity (IMDLMeshBufferZone This);
}
</pre>

### New Type ModelIO.MDLNamed_Extensions

<pre style='color: green'>
public static class MDLNamed_Extensions {
	// methods
	public static string GetName (IMDLNamed This);
	public static void SetName (IMDLNamed This, string value);
}
</pre>

### New Type ModelIO.MDLObject

<pre style='color: green'>
public class MDLObject : Foundation.NSObject, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLObject ();
	protected MDLObject (Foundation.NSObjectFlag t);
	protected MDLObject (IntPtr handle);
	// properties
	public virtual IMDLObjectContainerComponent Children { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	public virtual MDLObject Parent { get; set; }
	public virtual IMDLTransformComponent Transform { get; set; }
	// methods
	public virtual void AddChild (MDLObject child);
	public virtual MDLAxisAlignedBoundingBox BoundingBoxAtTime (double time);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLObjectContainerComponent

<pre style='color: green'>
public abstract class MDLObjectContainerComponent : Foundation.NSObject, IMDLObjectContainerComponent, IMDLComponent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected MDLObjectContainerComponent ();
	protected MDLObjectContainerComponent (Foundation.NSObjectFlag t);
	protected MDLObjectContainerComponent (IntPtr handle);
	// properties
	public virtual MDLObject[] Objects { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type ModelIO.MDLPhotometricLight

<pre style='color: green'>
public class MDLPhotometricLight : ModelIO.MDLLight, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLPhotometricLight ();
	protected MDLPhotometricLight (Foundation.NSObjectFlag t);
	protected MDLPhotometricLight (IntPtr handle);
	public MDLPhotometricLight (Foundation.NSUrl url);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint ConeSpans { get; }
	public virtual float HorizontalAngle { get; }
	public virtual uint HorizontalSpans { get; }
	public virtual float IESConeAngle { get; }
	public virtual Foundation.NSData LightWeb { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLPhysicallyPlausibleLight

<pre style='color: green'>
public class MDLPhysicallyPlausibleLight : ModelIO.MDLLight, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLPhysicallyPlausibleLight ();
	protected MDLPhysicallyPlausibleLight (Foundation.NSObjectFlag t);
	protected MDLPhysicallyPlausibleLight (IntPtr handle);
	// properties
	public virtual float AttenuationEndDistance { get; set; }
	public virtual float AttenuationFalloffExponent { get; set; }
	public virtual float AttenuationStartDistance { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGColor Color { get; set; }
	public virtual float InnerConeAngle { get; set; }
	public virtual float Lumens { get; set; }
	public virtual float OuterConeAngle { get; set; }
	// methods
	public virtual void SetColorByTemperature (float temperature);
}
</pre>

### New Type ModelIO.MDLPhysicallyPlausibleScatteringFunction

<pre style='color: green'>
public class MDLPhysicallyPlausibleScatteringFunction : ModelIO.MDLScatteringFunction, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLPhysicallyPlausibleScatteringFunction ();
	protected MDLPhysicallyPlausibleScatteringFunction (Foundation.NSObjectFlag t);
	protected MDLPhysicallyPlausibleScatteringFunction (IntPtr handle);
	// properties
	public virtual MDLMaterialProperty Anisotropic { get; }
	public virtual MDLMaterialProperty AnisotropicRotation { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialProperty Clearcoat { get; }
	public virtual MDLMaterialProperty ClearcoatGloss { get; }
	public virtual MDLMaterialProperty Metallic { get; }
	public virtual MDLMaterialProperty Roughness { get; }
	public virtual MDLMaterialProperty Sheen { get; }
	public virtual MDLMaterialProperty SheenTint { get; }
	public virtual MDLMaterialProperty SpecularAmount { get; }
	public virtual MDLMaterialProperty SpecularTint { get; }
	public virtual MDLMaterialProperty Subsurface { get; }
	public virtual nint Version { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLScatteringFunction

<pre style='color: green'>
public class MDLScatteringFunction : Foundation.NSObject, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLScatteringFunction ();
	protected MDLScatteringFunction (Foundation.NSObjectFlag t);
	protected MDLScatteringFunction (IntPtr handle);
	// properties
	public virtual MDLMaterialProperty AmbientOcclusion { get; }
	public virtual MDLMaterialProperty AmbientOcclusionScale { get; }
	public virtual MDLMaterialProperty BaseColor { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialProperty Emission { get; }
	public virtual MDLMaterialProperty InterfaceIndexOfRefraction { get; }
	public virtual MDLMaterialProperty MaterialIndexOfRefraction { get; }
	public virtual string Name { get; set; }
	public virtual MDLMaterialProperty Normal { get; }
	public virtual MDLMaterialProperty Specular { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLSubmesh

<pre style='color: green'>
public class MDLSubmesh : Foundation.NSObject, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLSubmesh ();
	protected MDLSubmesh (Foundation.NSObjectFlag t);
	protected MDLSubmesh (IntPtr handle);
	public MDLSubmesh (string name, IMDLMeshBuffer indexBuffer, uint indexCount, MDLIndexBitDepth indexType, MDLGeometryKind geometryType, MDLMaterial material);
	public MDLSubmesh (IMDLMeshBuffer indexBuffer, uint indexCount, MDLIndexBitDepth indexType, MDLGeometryKind geometryType, MDLMaterial material);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLGeometryKind GeometryType { get; }
	public virtual IMDLMeshBuffer IndexBuffer { get; }
	public virtual uint IndexCount { get; }
	public virtual MDLIndexBitDepth IndexType { get; }
	public virtual MDLMaterial Material { get; set; }
	public virtual string Name { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLTexture

<pre style='color: green'>
public class MDLTexture : Foundation.NSObject, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLTexture ();
	protected MDLTexture (Foundation.NSObjectFlag t);
	protected MDLTexture (IntPtr handle);
	public MDLTexture (Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, nint rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public virtual uint ChannelCount { get; }
	public virtual MDLTextureChannelEncoding ChannelEncoding { get; }
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2i Dimensions { get; }
	public virtual bool IsCube { get; }
	public virtual uint MipLevelCount { get; }
	public virtual string Name { get; set; }
	public virtual nint RowStride { get; }
	// methods
	public static MDLTexture CreateIrradianceTextureCube (MDLTexture texture, string name, OpenTK.Vector2i dimensions);
	public static MDLTexture CreateIrradianceTextureCubeWithConvolution (MDLTexture reflectiveTexture, string name, OpenTK.Vector2i dimensions, float roughness);
	public static MDLTexture CreateTextureCube (string[] imageNames);
	public static MDLTexture CreateTextureCube (string[] imageNames, Foundation.NSBundle bundleOrNil);
	public static MDLTexture FromBundle (string name, Foundation.NSBundle bundleOrNil);
	public static MDLTexture FromBundle (string name);
	public virtual Foundation.NSData GetTexelDataWithBottomLeftOrigin ();
	public virtual Foundation.NSData GetTexelDataWithBottomLeftOriginAtMipLevel (nint mipLevel, bool create);
	public virtual Foundation.NSData GetTexelDataWithTopLeftOrigin ();
	public virtual Foundation.NSData GetTexelDataWithTopLeftOriginAtMipLevel (nint mipLevel, bool create);
	public virtual bool WriteToFile (string path, bool atomically);
	public virtual bool WriteToUrl (Foundation.NSUrl url, bool atomically);
}
</pre>

### New Type ModelIO.MDLTextureChannelEncoding

<pre style='color: green'>
[Serializable]
public enum MDLTextureChannelEncoding {
	Float16 = 258,
	Float32 = 260,
	UInt16 = 2,
	UInt24 = 3,
	UInt32 = 4,
	UInt8 = 1,
}
</pre>

### New Type ModelIO.MDLTextureFilter

<pre style='color: green'>
public class MDLTextureFilter : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public MDLTextureFilter ();
	protected MDLTextureFilter (Foundation.NSObjectFlag t);
	protected MDLTextureFilter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialTextureFilterMode MagFilter { get; set; }
	public virtual MDLMaterialTextureFilterMode MinFilter { get; set; }
	public virtual MDLMaterialMipMapFilterMode MipFilter { get; set; }
	public virtual MDLMaterialTextureWrapMode RWrapMode { get; set; }
	public virtual MDLMaterialTextureWrapMode SWrapMode { get; set; }
	public virtual MDLMaterialTextureWrapMode TWrapMode { get; set; }
}
</pre>

### New Type ModelIO.MDLTextureSampler

<pre style='color: green'>
public class MDLTextureSampler : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public MDLTextureSampler ();
	protected MDLTextureSampler (Foundation.NSObjectFlag t);
	protected MDLTextureSampler (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLTextureFilter HardwareFilter { get; set; }
	public virtual MDLTexture Texture { get; set; }
	public virtual MDLTransform Transform { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLTransform

<pre style='color: green'>
public class MDLTransform : Foundation.NSObject, IMDLComponent, IMDLTransformComponent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLTransform ();
	protected MDLTransform (Foundation.NSObjectFlag t);
	protected MDLTransform (IntPtr handle);
	public MDLTransform (IMDLTransformComponent component);
	public MDLTransform (OpenTK.Matrix4 matrix);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Matrix4 Matrix { get; set; }
	public virtual double MaximumTime { get; }
	public virtual double MinimumTime { get; }
	public virtual OpenTK.Vector3 Rotation { get; set; }
	public virtual OpenTK.Vector3 Scale { get; set; }
	public virtual OpenTK.Vector3 Translation { get; set; }
	// methods
	public static OpenTK.Matrix4 GlobalTransformWithObject (MDLObject obj, double time);
	public virtual OpenTK.Matrix4 LocalTransformAtTime (double time);
	public virtual OpenTK.Vector3 RotationAtTime (double time);
	public virtual OpenTK.Vector3 ScaleAtTime (double time);
	public virtual void SetIdentity ();
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform);
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform, double time);
	public virtual void SetRotation (OpenTK.Vector3 rotation, double time);
	public virtual void SetScale (OpenTK.Vector3 scale, double time);
	public virtual void SetTranslation (OpenTK.Vector3 translation, double time);
	public virtual OpenTK.Vector3 TranslationAtTime (double time);
}
</pre>

### New Type ModelIO.MDLTransformComponent

<pre style='color: green'>
public abstract class MDLTransformComponent : Foundation.NSObject, IMDLTransformComponent, IMDLComponent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	protected MDLTransformComponent ();
	protected MDLTransformComponent (Foundation.NSObjectFlag t);
	protected MDLTransformComponent (IntPtr handle);
	// properties
	public virtual OpenTK.Matrix4 Matrix { get; set; }
	public virtual double MaximumTime { get; }
	public virtual double MinimumTime { get; }
	// methods
	public static OpenTK.Matrix4 GlobalTransformWithObject (MDLObject obj, double time);
	public virtual OpenTK.Matrix4 LocalTransformAtTime (double time);
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform, double time);
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform);
}
</pre>

### New Type ModelIO.MDLTransformComponent_Extensions

<pre style='color: green'>
public static class MDLTransformComponent_Extensions {
	// methods
	public static OpenTK.Matrix4 LocalTransformAtTime (IMDLTransformComponent This, double time);
	public static void SetLocalTransform (IMDLTransformComponent This, OpenTK.Matrix4 transform, double time);
	public static void SetLocalTransform (IMDLTransformComponent This, OpenTK.Matrix4 transform);
}
</pre>

### New Type ModelIO.MDLVertexAttribute

<pre style='color: green'>
public class MDLVertexAttribute : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLVertexAttribute ();
	protected MDLVertexAttribute (Foundation.NSObjectFlag t);
	protected MDLVertexAttribute (IntPtr handle);
	public MDLVertexAttribute (string name, MDLVertexFormat format, uint offset, uint bufferIndex);
	// properties
	public virtual uint BufferIndex { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLVertexFormat Format { get; set; }
	public virtual OpenTK.Vector4 InitializationValue { get; set; }
	public virtual string Name { get; set; }
	public virtual uint Offset { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
</pre>

### New Type ModelIO.MDLVertexAttributeData

<pre style='color: green'>
public class MDLVertexAttributeData : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected MDLVertexAttributeData (Foundation.NSObjectFlag t);
	protected MDLVertexAttributeData (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IntPtr DataStart { get; set; }
	public virtual MDLVertexFormat Format { get; set; }
	public virtual Foundation.NSData MappedData { get; set; }
	public virtual uint Stride { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLVertexDescriptor

<pre style='color: green'>
public class MDLVertexDescriptor : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public MDLVertexDescriptor ();
	protected MDLVertexDescriptor (Foundation.NSObjectFlag t);
	protected MDLVertexDescriptor (IntPtr handle);
	public MDLVertexDescriptor (MDLVertexDescriptor vertexDescriptor);
	// properties
	public virtual Foundation.NSMutableArray Attributes { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSMutableArray Layouts { get; set; }
	// methods
	public virtual void AddOrReplaceAttribute (MDLVertexAttribute attribute);
	public virtual MDLVertexAttribute AttributeNamed (string name);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
	public virtual void SetPackedOffsets ();
	public virtual void SetPackedStrides ();
}
</pre>

### New Type ModelIO.MDLVertexFormat

<pre style='color: green'>
[Serializable]
public enum MDLVertexFormat {
	Char = 131073,
	Char2 = 131074,
	Char2Normalized = 262146,
	Char3 = 131075,
	Char3Normalized = 262147,
	Char4 = 131076,
	Char4Normalized = 262148,
	CharNormalized = 262145,
	Float = 786433,
	Float2 = 786434,
	Float3 = 786435,
	Float4 = 786436,
	Half = 720897,
	Half2 = 720898,
	Half3 = 720899,
	Half4 = 720900,
	Int = 655361,
	Int1010102Normalized = 4100,
	Int2 = 655362,
	Int3 = 655363,
	Int4 = 655364,
	Invalid = 0,
	Short = 393217,
	Short2 = 393218,
	Short2Normalized = 524290,
	Short3 = 393219,
	Short3Normalized = 524291,
	Short4 = 393220,
	Short4Normalized = 524292,
	ShortNormalized = 524289,
	UChar = 65537,
	UChar2 = 65538,
	UChar2Normalized = 196610,
	UChar3 = 65539,
	UChar3Normalized = 196611,
	UChar4 = 65540,
	UChar4Normalized = 196612,
	UCharNormalized = 196609,
	UInt = 589825,
	UInt1010102Normalized = 8196,
	UInt2 = 589826,
	UInt3 = 589827,
	UInt4 = 589828,
	UShort = 327681,
	UShort2 = 327682,
	UShort2Normalized = 458754,
	UShort3 = 327683,
	UShort3Normalized = 458755,
	UShort4 = 327684,
	UShort4Normalized = 458756,
	UShortNormalized = 458753,
}
</pre>

## New Namespace ReplayKit

### New Type ReplayKit.IRPPreviewViewControllerDelegate

<pre style='color: green'>
public interface IRPPreviewViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type ReplayKit.IRPScreenRecorderDelegate

<pre style='color: green'>
public interface IRPScreenRecorderDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type ReplayKit.RPPreviewViewController

<pre style='color: green'>
public class RPPreviewViewController : UIKit.UIViewController, System.Collections.IEnumerable, Foundation.INSCoding, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUITraitEnvironment, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public RPPreviewViewController ();
	public RPPreviewViewController (Foundation.NSCoder coder);
	protected RPPreviewViewController (Foundation.NSObjectFlag t);
	protected RPPreviewViewController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IRPPreviewViewControllerDelegate PreviewControllerDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ReplayKit.RPPreviewViewControllerDelegate

<pre style='color: green'>
public class RPPreviewViewControllerDelegate : Foundation.NSObject, IRPPreviewViewControllerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public RPPreviewViewControllerDelegate ();
	protected RPPreviewViewControllerDelegate (Foundation.NSObjectFlag t);
	protected RPPreviewViewControllerDelegate (IntPtr handle);
	// methods
	public virtual void PreviewControllerDidFinish (RPPreviewViewController previewController);
}
</pre>

### New Type ReplayKit.RPPreviewViewControllerDelegate_Extensions

<pre style='color: green'>
public static class RPPreviewViewControllerDelegate_Extensions {
	// methods
	public static void PreviewControllerDidFinish (IRPPreviewViewControllerDelegate This, RPPreviewViewController previewController);
}
</pre>

### New Type ReplayKit.RPScreenRecorder

<pre style='color: green'>
public class RPScreenRecorder : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected RPScreenRecorder (Foundation.NSObjectFlag t);
	protected RPScreenRecorder (IntPtr handle);
	// properties
	public virtual bool Available { get; }
	public override IntPtr ClassHandle { get; }
	public virtual IRPScreenRecorderDelegate Delegate { get; set; }
	public virtual bool MicrophoneEnabled { get; }
	public virtual bool Recording { get; }
	public static RPScreenRecorder SharedRecorder { get; }
	// methods
	public virtual void DiscardRecording (System.Action handler);
	public virtual System.Threading.Tasks.Task DiscardRecordingAsync ();
	protected override void Dispose (bool disposing);
	public virtual void StartRecording (bool microphoneEnabled, System.Action&lt;Foundation.NSError&gt; handler);
	public virtual System.Threading.Tasks.Task StartRecordingAsync (bool microphoneEnabled);
	public virtual void StopRecording (System.Action&lt;Foundation.NSError&gt; handler);
	public virtual System.Threading.Tasks.Task StopRecordingAsync ();
}
</pre>

### New Type ReplayKit.RPScreenRecorderDelegate

<pre style='color: green'>
public class RPScreenRecorderDelegate : Foundation.NSObject, IRPScreenRecorderDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public RPScreenRecorderDelegate ();
	protected RPScreenRecorderDelegate (Foundation.NSObjectFlag t);
	protected RPScreenRecorderDelegate (IntPtr handle);
	// methods
	public virtual void DidChangeAvailability (RPScreenRecorder screenRecorder);
	public virtual void DidStopRecording (RPScreenRecorder screenRecorder, Foundation.NSError error, RPPreviewViewController previewViewController);
}
</pre>

### New Type ReplayKit.RPScreenRecorderDelegate_Extensions

<pre style='color: green'>
public static class RPScreenRecorderDelegate_Extensions {
	// methods
	public static void DidChangeAvailability (IRPScreenRecorderDelegate This, RPScreenRecorder screenRecorder);
	public static void DidStopRecording (IRPScreenRecorderDelegate This, RPScreenRecorder screenRecorder, Foundation.NSError error, RPPreviewViewController previewViewController);
}
</pre>

## New Namespace WatchConnectivity

### New Type WatchConnectivity.IWCSessionDelegate

<pre style='color: green'>
public interface IWCSessionDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type WatchConnectivity.WCErrorCode

<pre style='color: green'>
[Serializable]
public enum WCErrorCode {
	DeviceNotPaired = 7005,
	FileAccessDenied = 7013,
	GenericError = 7001,
	InvalidParameter = 7008,
	MessageReplyFailed = 7011,
	MessageReplyTimedOut = 7012,
	NotReachable = 7007,
	PayloadTooLarge = 7009,
	PayloadUnsupportedTypes = 7010,
	SessionMissingDelegate = 7003,
	SessionNotActivated = 7004,
	SessionNotSupported = 7002,
	WatchAppNotInstalled = 7006,
}
</pre>

### New Type WatchConnectivity.WCSession

<pre style='color: green'>
public class WCSession : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WCSession (Foundation.NSObjectFlag t);
	protected WCSession (IntPtr handle);
	// properties
	public virtual Foundation.NSDictionary ApplicationContext { get; }
	public override IntPtr ClassHandle { get; }
	public virtual bool ComplicationEnabled { get; }
	public static WCSession DefaultSession { get; }
	public virtual IWCSessionDelegate Delegate { get; set; }
	public static Foundation.NSString ErrorDomain { get; }
	public static bool IsSupported { get; }
	public virtual WCSessionFileTransfer[] OutstandingFileTransfers { get; }
	public virtual WCSessionUserInfoTransfer[] OutstandingUserInfoTransfers { get; }
	public virtual bool Paired { get; }
	public virtual bool Reachable { get; }
	public virtual Foundation.NSDictionary ReceivedApplicationContext { get; }
	public virtual bool WatchAppInstalled { get; }
	public virtual Foundation.NSUrl WatchDirectoryUrl { get; }
	// methods
	public virtual void ActivateSession ();
	protected override void Dispose (bool disposing);
	public virtual void SendMessage (Foundation.NSData data, WCSessionReplyDataHandler replyHandler, System.Action&lt;Foundation.NSError&gt; errorHandler);
	public virtual void SendMessage (Foundation.NSDictionary message, WCSessionReplyHandler replyHandler, System.Action&lt;Foundation.NSError&gt; errorHandler);
	public virtual WCSessionUserInfoTransfer TransferCurrentComplicationUserInfo (Foundation.NSDictionary userInfo);
	public virtual WCSessionFileTransfer TransferFile (Foundation.NSUrl file, Foundation.NSDictionary metadata);
	public virtual WCSessionUserInfoTransfer TransferUserInfo (Foundation.NSDictionary userInfo);
	public virtual bool UpdateApplicationContext (Foundation.NSDictionary applicationContext, out Foundation.NSError error);
}
</pre>

### New Type WatchConnectivity.WCSessionDelegate

<pre style='color: green'>
public class WCSessionDelegate : Foundation.NSObject, IWCSessionDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public WCSessionDelegate ();
	protected WCSessionDelegate (Foundation.NSObjectFlag t);
	protected WCSessionDelegate (IntPtr handle);
	// methods
	public virtual void DidFinishFileTransfer (WCSession session, WCSessionFileTransfer fileTransfer, Foundation.NSError error);
	public virtual void DidFinishUserInfoTransfer (WCSession session, WCSessionUserInfoTransfer userInfoTransfer, Foundation.NSError error);
	public virtual void DidReceiveApplicationContext (WCSession session, Foundation.NSDictionary applicationContext);
	public virtual void DidReceiveFile (WCSession session, WCSessionFile file);
	public virtual void DidReceiveMessage (WCSession session, Foundation.NSDictionary message, WCSessionReplyHandler replyHandler);
	public virtual void DidReceiveMessage (WCSession session, Foundation.NSDictionary message);
	public virtual void DidReceiveMessageData (WCSession session, Foundation.NSData messageData);
	public virtual void DidReceiveMessageData (WCSession session, Foundation.NSData messageData, WCSessionReplyDataHandler replyHandler);
	public virtual void DidReceiveUserInfo (WCSession session, Foundation.NSDictionary userInfo);
	public virtual void SessionReachabilityDidChange (WCSession session);
	public virtual void SessionWatchStateDidChange (WCSession session);
}
</pre>

### New Type WatchConnectivity.WCSessionDelegate_Extensions

<pre style='color: green'>
public static class WCSessionDelegate_Extensions {
	// methods
	public static void DidFinishFileTransfer (IWCSessionDelegate This, WCSession session, WCSessionFileTransfer fileTransfer, Foundation.NSError error);
	public static void DidFinishUserInfoTransfer (IWCSessionDelegate This, WCSession session, WCSessionUserInfoTransfer userInfoTransfer, Foundation.NSError error);
	public static void DidReceiveApplicationContext (IWCSessionDelegate This, WCSession session, Foundation.NSDictionary applicationContext);
	public static void DidReceiveFile (IWCSessionDelegate This, WCSession session, WCSessionFile file);
	public static void DidReceiveMessage (IWCSessionDelegate This, WCSession session, Foundation.NSDictionary message);
	public static void DidReceiveMessage (IWCSessionDelegate This, WCSession session, Foundation.NSDictionary message, WCSessionReplyHandler replyHandler);
	public static void DidReceiveMessageData (IWCSessionDelegate This, WCSession session, Foundation.NSData messageData, WCSessionReplyDataHandler replyHandler);
	public static void DidReceiveMessageData (IWCSessionDelegate This, WCSession session, Foundation.NSData messageData);
	public static void DidReceiveUserInfo (IWCSessionDelegate This, WCSession session, Foundation.NSDictionary userInfo);
	public static void SessionReachabilityDidChange (IWCSessionDelegate This, WCSession session);
	public static void SessionWatchStateDidChange (IWCSessionDelegate This, WCSession session);
}
</pre>

### New Type WatchConnectivity.WCSessionFile

<pre style='color: green'>
public class WCSessionFile : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WCSessionFile (Foundation.NSObjectFlag t);
	protected WCSessionFile (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSUrl FileUrl { get; }
	public virtual Foundation.NSDictionary Metadata { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type WatchConnectivity.WCSessionFileTransfer

<pre style='color: green'>
public class WCSessionFileTransfer : Foundation.NSObject, System.IEquatable&lt;Foundation.NSObject&gt;, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WCSessionFileTransfer (Foundation.NSObjectFlag t);
	protected WCSessionFileTransfer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual WCSessionFile File { get; }
	public virtual bool Transferring { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
</pre>

### New Type WatchConnectivity.WCSessionReplyDataHandler

<pre style='color: green'>
public sealed delegate WCSessionReplyDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public WCSessionReplyDataHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSData replyMessage, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSData replyMessage);
}
</pre>

### New Type WatchConnectivity.WCSessionReplyHandler

<pre style='color: green'>
public sealed delegate WCSessionReplyHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public WCSessionReplyHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary replyMessage, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSDictionary replyMessage);
}
</pre>

### New Type WatchConnectivity.WCSessionUserInfoTransfer

<pre style='color: green'>
public class WCSessionUserInfoTransfer : Foundation.NSObject, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, Foundation.INSObjectProtocol {
	// constructors
	public WCSessionUserInfoTransfer (Foundation.NSCoder coder);
	protected WCSessionUserInfoTransfer (Foundation.NSObjectFlag t);
	protected WCSessionUserInfoTransfer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool CurrentComplicationInfo { get; }
	public virtual bool Transferring { get; }
	public virtual Foundation.NSDictionary UserInfo { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

   


 <hr>
