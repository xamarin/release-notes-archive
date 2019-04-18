---
id: E13AAC98-A11A-427F-951D-06CB1EE9DB1B
title: "From 8.9.1 to 8.10.0"
---

# API diff

 [mscorlib.dll](#mscorlib)

   


 [System.dll](#System)

   


 [System.Core.dll](#System.Core)

   


 [System.ComponentModel.DataAnnotations.dll](#System.ComponentModel.DataAnnotations)

   


 [System.Data.dll](#System.Data)

   


 [System.Runtime.Serialization.dll](#System.Runtime.Serialization)

   


 [(Classic) monotouch.dll](#compat/monotouch)

   


 [(Classic) MonoTouch.Dialog-1.dll](#compat/MonoTouch.Dialog-1)

   


 [(Classic) MonoTouch.NUnitLite.dll](#compat/MonoTouch.NUnitLite)

   


 [(Classic) OpenTK-1.0.dll](#compat/OpenTK-1.0)

   


 [(Unified) MonoTouch.Dialog-1.dll](#reference/MonoTouch.Dialog-1)

   


 [(Unified) MonoTouch.NUnitLite.dll](#reference/MonoTouch.NUnitLite)

   


 [(Unified) OpenTK-1.0.dll](#reference/OpenTK-1.0)

   


 [(Unified) Xamarin.iOS.dll](#reference/Xamarin.iOS)

   


   


 <hr>

<h1 id='mscorlib'>mscorlib.dll</h1>

## Namespace System

### Type Changed: System.AppDomainSetup

Added property:

```
public string TargetFrameworkName { get; set; }
```

## Namespace System.Globalization

### Type Changed: System.Globalization.GregorianCalendar

Added property:

```
public override CalendarAlgorithmType AlgorithmType { get; }
```

### Type Changed: System.Globalization.HebrewCalendar

Added property:

```
public override CalendarAlgorithmType AlgorithmType { get; }
```

### Type Changed: System.Globalization.HijriCalendar

Added property:

```
public override CalendarAlgorithmType AlgorithmType { get; }
```

### Type Changed: System.Globalization.JapaneseCalendar

Added property:

```
public override CalendarAlgorithmType AlgorithmType { get; }
```

### Type Changed: System.Globalization.KoreanCalendar

Added property:

```
public override CalendarAlgorithmType AlgorithmType { get; }
```

### Type Changed: System.Globalization.TaiwanCalendar

Added property:

```
public override CalendarAlgorithmType AlgorithmType { get; }
```

### Type Changed: System.Globalization.ThaiBuddhistCalendar

Added property:

```
public override CalendarAlgorithmType AlgorithmType { get; }
```

### Type Changed: System.Globalization.UmAlQuraCalendar

Added property:

```
public override CalendarAlgorithmType AlgorithmType { get; }
```

## Namespace System.IO

### Type Changed: System.IO.BufferedStream

Added methods:

```
public override System.IAsyncResult BeginRead (byte[] buffer, int offset, int count, System.AsyncCallback callback, object state);
	public override System.IAsyncResult BeginWrite (byte[] buffer, int offset, int count, System.AsyncCallback callback, object state);
	public override int EndRead (System.IAsyncResult asyncResult);
	public override void EndWrite (System.IAsyncResult asyncResult);
	public override System.Threading.Tasks.Task FlushAsync (System.Threading.CancellationToken cancellationToken);
	public override System.Threading.Tasks.Task<int> ReadAsync (byte[] buffer, int offset, int count, System.Threading.CancellationToken cancellationToken);
	public override System.Threading.Tasks.Task WriteAsync (byte[] buffer, int offset, int count, System.Threading.CancellationToken cancellationToken);
```

## Namespace System.Runtime.CompilerServices

### Type Changed: System.Runtime.CompilerServices.RuntimeHelpers

Added method:

```
public static void PrepareContractedDelegate (System.Delegate d);
```

### Removed Type System.Runtime.CompilerServices.IDispatchConstantAttribute 

## Namespace System.Security.Claims

### Type Changed: System.Security.Claims.ClaimsPrincipal

Added method:

```
protected virtual void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
```

## Namespace System.Threading

### Type Changed: System.Threading.HostExecutionContext

Added interface:

```
System.IDisposable
```

Added methods:

```
public virtual void Dispose ();
	public virtual void Dispose (bool disposing);
```

### Type Changed: System.Threading.ThreadPool

Added method:

```
public static void GetAvailableThreads (out int workerThreads, out int completionPortThreads);
```

## Namespace System.Threading.Tasks

### Type Changed: System.Threading.Tasks.TaskScheduler

Modified methods:

```
protected protected bool TryExecuteTask (Task task)
```

   


 <hr>

<h1 id='System'>System.dll</h1>

## Namespace System.Collections.Generic

### Type Changed: System.Collections.Generic.LinkedList`1

### Type Changed: System.Collections.Generic.LinkedList`1.Enumerator

Added interfaces:

```
System.Runtime.Serialization.ISerializable
	System.Runtime.Serialization.IDeserializationCallback
```

### Type Changed: System.Collections.Generic.SortedDictionary`2

Removed constructor:

```
protected SortedDictionary`2 (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
```

Removed interface:

```
System.Runtime.Serialization.ISerializable
```

Removed method:

```
public virtual void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
```

### Type Changed: System.Collections.Generic.SortedSet`1

### Type Changed: System.Collections.Generic.SortedSet`1.Enumerator

Added interfaces:

```
System.Runtime.Serialization.ISerializable
	System.Runtime.Serialization.IDeserializationCallback
```

## Namespace System.Collections.Specialized

### New Type System.Collections.Specialized.CollectionsUtil

```
public class CollectionsUtil {
	// constructors
	public CollectionsUtil ();
	// methods
	public static System.Collections.Hashtable CreateCaseInsensitiveHashtable ();
	public static System.Collections.Hashtable CreateCaseInsensitiveHashtable (int capacity);
	public static System.Collections.Hashtable CreateCaseInsensitiveHashtable (System.Collections.IDictionary d);
	public static System.Collections.SortedList CreateCaseInsensitiveSortedList ();
}
```

## Namespace System.ComponentModel

### Type Changed: System.ComponentModel.AsyncCompletedEventArgs

Added constructor:

```
[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public AsyncCompletedEventArgs ();
```

### Type Changed: System.ComponentModel.AttributeCollection

Modified methods:

```
public bool Contains (System.Attribute attr attribute)
	public bool Matches (System.Attribute attr attribute)
```

### Type Changed: System.ComponentModel.BackgroundWorker

Added interfaces:

```
IComponent
	System.IDisposable
```

### Type Changed: System.ComponentModel.Component

Modified methods:

```
protected virtual void Dispose (bool release_all disposing)
```

### Type Changed: System.ComponentModel.DesignerSerializationVisibilityAttribute

Modified constructors:

```
public DesignerSerializationVisibilityAttribute (DesignerSerializationVisibility vis visibility)
```

### Type Changed: System.ComponentModel.DesignOnlyAttribute

Modified constructors:

```
public DesignOnlyAttribute (bool design_only isDesignOnly)
```

### Type Changed: System.ComponentModel.DoWorkEventArgs

Removed property:

```
public bool Cancel { get; set; }
```

### Type Changed: System.ComponentModel.EventDescriptor

Modified constructors:

```
protected EventDescriptor (MemberDescriptor desc descr)
	protected EventDescriptor (MemberDescriptor desc descr, System.Attribute[] attrs)
	protected EventDescriptor (string str name, System.Attribute[] attrs)
```

### Type Changed: System.ComponentModel.EventDescriptorCollection

Modified methods:

```
protected void InternalSort (System.Collections.IComparer comparer sorter)
	protected void InternalSort (string[] order names)
	public virtual EventDescriptorCollection Sort (string[] order names)
	public virtual EventDescriptorCollection Sort (string[] order names, System.Collections.IComparer comparer)
```

### Type Changed: System.ComponentModel.ExpandableObjectConverter

Added methods:

```
public override PropertyDescriptorCollection GetProperties (ITypeDescriptorContext context, object value, System.Attribute[] attributes);
	public override bool GetPropertiesSupported (ITypeDescriptorContext context);
```

### Type Changed: System.ComponentModel.ICustomTypeDescriptor

Modified methods:

```
public abstract EventDescriptorCollection GetEvents (System.Attribute[] arr attributes)
	public abstract PropertyDescriptorCollection GetProperties (System.Attribute[] arr attributes)
```

### Type Changed: System.ComponentModel.InheritanceAttribute

Modified methods:

```
public override bool Equals (object obj value)
```

### Type Changed: System.ComponentModel.InstanceCreationEditor

Modified methods:

```
public abstract object CreateInstance (ITypeDescriptorContext context, System.Type type instanceType)
```

### Type Changed: System.ComponentModel.ListSortDescription

Modified constructors:

```
public ListSortDescription (PropertyDescriptor propertyDescriptor property, ListSortDirection sortDirection direction)
```

### Type Changed: System.ComponentModel.LocalizableAttribute

Modified constructors:

```
public LocalizableAttribute (bool localizable isLocalizable)
```

### Type Changed: System.ComponentModel.MemberDescriptor

Modified constructors:

```
protected MemberDescriptor (string name, System.Attribute[] attrs attributes)
	protected MemberDescriptor (MemberDescriptor reference oldMemberDescriptor, System.Attribute[] attrs newAttributes)
	protected MemberDescriptor (MemberDescriptor reference descr)
```

### Type Changed: System.ComponentModel.NullableConverter

Modified constructors:

```
public NullableConverter (System.Type nullableType type)
```

### Type Changed: System.ComponentModel.PropertyChangedEventArgs

Modified properties:

```
public virtual string PropertyName { get; }
```

### Type Changed: System.ComponentModel.PropertyDescriptor

Modified constructors:

```
protected PropertyDescriptor (MemberDescriptor reference descr)
	protected PropertyDescriptor (MemberDescriptor reference descr, System.Attribute[] attrs)
```

### Type Changed: System.ComponentModel.PropertyDescriptorCollection

Modified methods:

```
protected void InternalSort (System.Collections.IComparer ic sorter)
	protected void InternalSort (string[] order names)
	public virtual PropertyDescriptorCollection Sort (string[] order names)
	public virtual PropertyDescriptorCollection Sort (string[] order names, System.Collections.IComparer comparer)
```

### Type Changed: System.ComponentModel.ReadOnlyAttribute

Modified methods:

```
public override bool Equals (object obj value)
```

### Type Changed: System.ComponentModel.RefreshPropertiesAttribute

Modified methods:

```
public override bool Equals (object obj value)
```

### Type Changed: System.ComponentModel.ToolboxItemAttribute

Modified constructors:

```
public ToolboxItemAttribute (string toolboxItemName toolboxItemTypeName)
```

Modified methods:

```
public override bool Equals (object o obj)
```

### Type Changed: System.ComponentModel.TypeConverter

Modified methods:

```
public object ConvertFrom (object o value)
```

### Type Changed: System.ComponentModel.TypeDescriptor

Modified methods:

```
public object GetEditor (System.Type componentType type, System.Type editorBaseType)
```

Added method:

```
public static void AddEditorTable (System.Type editorBaseType, System.Collections.Hashtable table);
```

### New Type System.ComponentModel.License

```
public abstract class License : System.IDisposable {
	// constructors
	protected License ();
	// properties
	public virtual string LicenseKey { get; }
	// methods
	public virtual void Dispose ();
}
```

### New Type System.ComponentModel.LicenseContext

```
public class LicenseContext : System.IServiceProvider {
	// constructors
	public LicenseContext ();
	// properties
	public virtual LicenseUsageMode UsageMode { get; }
	// methods
	public virtual string GetSavedLicenseKey (System.Type type, System.Reflection.Assembly resourceAssembly);
	public virtual object GetService (System.Type type);
	public virtual void SetSavedLicenseKey (System.Type type, string key);
}
```

### New Type System.ComponentModel.LicenseException

```
[Serializable]
public class LicenseException : System.SystemException, System.Runtime.Serialization.ISerializable {
	// constructors
	public LicenseException (System.Type type);
	public LicenseException (System.Type type, object instance);
	public LicenseException (System.Type type, object instance, string message);
	public LicenseException (System.Type type, object instance, string message, System.Exception innerException);
	protected LicenseException (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
	// properties
	public System.Type LicensedType { get; }
	// methods
	public override void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
}
```

### New Type System.ComponentModel.LicenseManager

```
public sealed class LicenseManager {
	// properties
	public static LicenseContext CurrentContext { get; set; }
	public static LicenseUsageMode UsageMode { get; }
	// methods
	public static object CreateWithContext (System.Type type, LicenseContext creationContext);
	public static object CreateWithContext (System.Type type, LicenseContext creationContext, object[] args);
	public static bool IsLicensed (System.Type type);
	public static bool IsValid (System.Type type, object instance, out License license);
	public static bool IsValid (System.Type type);
	public static void LockContext (object contextUser);
	public static void UnlockContext (object contextUser);
	public static void Validate (System.Type type);
	public static License Validate (System.Type type, object instance);
}
```

### New Type System.ComponentModel.LicenseProvider

```
public abstract class LicenseProvider {
	// constructors
	protected LicenseProvider ();
	// methods
	public virtual License GetLicense (LicenseContext context, System.Type type, object instance, bool allowExceptions);
}
```

### New Type System.ComponentModel.LicenseProviderAttribute

```
public sealed class LicenseProviderAttribute : System.Attribute {
	// constructors
	public LicenseProviderAttribute ();
	public LicenseProviderAttribute (string typeName);
	public LicenseProviderAttribute (System.Type type);
	// fields
	public static LicenseProviderAttribute Default;
	// properties
	public System.Type LicenseProvider { get; }
	public override object TypeId { get; }
	// methods
	public override bool Equals (object value);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.LicenseUsageMode

```
[Serializable]
public enum LicenseUsageMode {
	Designtime = 1,
	Runtime = 0,
}
```

### New Type System.ComponentModel.LicFileLicenseProvider

```
public class LicFileLicenseProvider : System.ComponentModel.LicenseProvider {
	// constructors
	public LicFileLicenseProvider ();
	// methods
	protected virtual string GetKey (System.Type type);
	public override License GetLicense (LicenseContext context, System.Type type, object instance, bool allowExceptions);
	protected virtual bool IsKeyValid (string key, System.Type type);
}
```

## Namespace System.ComponentModel.Design

### Type Changed: System.ComponentModel.Design.DesignerOptionService

Modified constructors:

```
protected protected DesignerOptionService ()
```

### Type Changed: System.ComponentModel.Design.DesignerOptionService.DesignerOptionCollection

Modified methods:

```
public int IndexOf (DesignerOptionService.DesignerOptionCollection item value)
```

### Removed Type System.ComponentModel.Design.DesignerOptionService.WrappedPropertyDescriptor ### Type Changed: System.ComponentModel.Design.HelpKeywordAttribute

Modified methods:

```
public override bool Equals (object other obj)
```

### New Type System.ComponentModel.Design.DesigntimeLicenseContext

```
public class DesigntimeLicenseContext : System.ComponentModel.LicenseContext, System.IServiceProvider {
	// constructors
	public DesigntimeLicenseContext ();
	// properties
	public override System.ComponentModel.LicenseUsageMode UsageMode { get; }
	// methods
	public override string GetSavedLicenseKey (System.Type type, System.Reflection.Assembly resourceAssembly);
	public override void SetSavedLicenseKey (System.Type type, string key);
}
```

### New Type System.ComponentModel.Design.DesigntimeLicenseContextSerializer

```
public class DesigntimeLicenseContextSerializer {
	// methods
	public static void Serialize (System.IO.Stream o, string cryptoKey, DesigntimeLicenseContext context);
}
```



## Namespace System.ComponentModel.Design.Serialization

### Type Changed: System.ComponentModel.Design.Serialization.MemberRelationship

Modified methods:

```
public override bool Equals (object o obj)
```

## Namespace System.IO.Compression

### Type Changed: System.IO.Compression.GZipStream

Modified constructors:

```
public GZipStream (System.IO.Stream compressedStream stream, CompressionMode mode)
	public GZipStream (System.IO.Stream compressedStream stream, CompressionMode mode, bool leaveOpen)
```

## Namespace System.Net

### Type Changed: System.Net.WebClient

Added properties:

```
[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public bool AllowReadStreamBuffering { get; set; }

	[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public bool AllowWriteStreamBuffering { get; set; }
```

Added event:

```
[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public event WriteStreamClosedEventHandler WriteStreamClosed;
```

Added method:

```
[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	protected virtual void OnWriteStreamClosed (WriteStreamClosedEventArgs e);
```

### New Type System.Net.EndpointPermission

```
[Serializable]
public class EndpointPermission {
	// properties
	public string Hostname { get; }
	public int Port { get; }
	public TransportType Transport { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public override string ToString ();
}
```

### New Type System.Net.SocketPermission

```
[Serializable]
public sealed class SocketPermission : System.Security.CodeAccessPermission, System.Security.Permissions.IUnrestrictedPermission, System.Security.IPermission, System.Security.ISecurityEncodable, System.Security.IStackWalk {
	// constructors
	public SocketPermission (System.Security.Permissions.PermissionState state);
	public SocketPermission (NetworkAccess access, TransportType transport, string hostName, int portNumber);
	// fields
	public static const int AllPorts;
	// properties
	public System.Collections.IEnumerator AcceptList { get; }
	public System.Collections.IEnumerator ConnectList { get; }
	// methods
	public void AddPermission (NetworkAccess access, TransportType transport, string hostName, int portNumber);
	public override System.Security.IPermission Copy ();
	public override void FromXml (System.Security.SecurityElement securityElement);
	public override System.Security.IPermission Intersect (System.Security.IPermission target);
	public override bool IsSubsetOf (System.Security.IPermission target);
	public virtual bool IsUnrestricted ();
	public override System.Security.SecurityElement ToXml ();
	public override System.Security.IPermission Union (System.Security.IPermission target);
}
```

### New Type System.Net.SocketPermissionAttribute

```
[Serializable]
public sealed class SocketPermissionAttribute : System.Security.Permissions.CodeAccessSecurityAttribute {
	// constructors
	public SocketPermissionAttribute (System.Security.Permissions.SecurityAction action);
	// properties
	public string Access { get; set; }
	public string Host { get; set; }
	public string Port { get; set; }
	public string Transport { get; set; }
	// methods
	public override System.Security.IPermission CreatePermission ();
}
```

### New Type System.Net.WriteStreamClosedEventArgs

```
public class WriteStreamClosedEventArgs : System.EventArgs {
	// constructors

	[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public WriteStreamClosedEventArgs ();
	// properties

	[Obsolete ("This API supports the .NET Framework infrastructure and is not intended to be used directly from your code.")]
	public System.Exception Error { get; }
}
```

### New Type System.Net.WriteStreamClosedEventHandler

```
public sealed delegate WriteStreamClosedEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public WriteStreamClosedEventHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (object sender, WriteStreamClosedEventArgs e, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (object sender, WriteStreamClosedEventArgs e);
}
```

## Namespace System.Text.RegularExpressions

### Type Changed: System.Text.RegularExpressions.Regex

Added fields:

```
protected System.Collections.Hashtable capnames;
	protected System.Collections.Hashtable caps;
	protected RegexRunnerFactory factory;
	protected System.TimeSpan internalMatchTimeout;
```

Added method:

```
protected static void ValidateMatchTimeout (System.TimeSpan matchTimeout);
```

### Type Changed: System.Text.RegularExpressions.RegexCompilationInfo

Added constructor:

```
public RegexCompilationInfo (string pattern, RegexOptions options, string name, string fullnamespace, bool ispublic, System.TimeSpan matchTimeout);
```

Added property:

```
public System.TimeSpan MatchTimeout { get; set; }
```

### New Type System.Text.RegularExpressions.RegexRunner

```
public abstract class RegexRunner {
	// constructors
	protected RegexRunner ();
	// fields
	protected int[] runcrawl;
	protected int runcrawlpos;
	protected Match runmatch;
	protected Regex runregex;
	protected int[] runstack;
	protected int runstackpos;
	protected string runtext;
	protected int runtextbeg;
	protected int runtextend;
	protected int runtextpos;
	protected int runtextstart;
	protected int[] runtrack;
	protected int runtrackcount;
	protected int runtrackpos;
	// methods
	protected void Capture (int capnum, int start, int end);
	protected static bool CharInClass (char ch, string charClass);
	protected static bool CharInSet (char ch, string set, string category);
	protected void CheckTimeout ();
	protected void Crawl (int i);
	protected int Crawlpos ();
	protected void DoubleCrawl ();
	protected void DoubleStack ();
	protected void DoubleTrack ();
	protected void EnsureStorage ();
	protected virtual bool FindFirstChar ();
	protected virtual void Go ();
	protected virtual void InitTrackCount ();
	protected bool IsBoundary (int index, int startpos, int endpos);
	protected bool IsECMABoundary (int index, int startpos, int endpos);
	protected bool IsMatched (int cap);
	protected int MatchIndex (int cap);
	protected int MatchLength (int cap);
	protected int Popcrawl ();
	protected Match Scan (Regex regex, string text, int textbeg, int textend, int textstart, int prevlen, bool quick, System.TimeSpan timeout);
	protected Match Scan (Regex regex, string text, int textbeg, int textend, int textstart, int prevlen, bool quick);
	protected void TransferCapture (int capnum, int uncapnum, int start, int end);
	protected void Uncapture ();
}
```

### New Type System.Text.RegularExpressions.RegexRunnerFactory

```
public abstract class RegexRunnerFactory {
	// constructors
	protected RegexRunnerFactory ();
	// methods
	protected virtual RegexRunner CreateInstance ();
}
```

## New Namespace System.Security.Permissions

### New Type System.Security.Permissions.TypeDescriptorPermission

```
[Serializable]
public sealed class TypeDescriptorPermission : System.Security.CodeAccessPermission, IUnrestrictedPermission, System.Security.IPermission, System.Security.ISecurityEncodable, System.Security.IStackWalk {
	// constructors
	public TypeDescriptorPermission (PermissionState state);
	public TypeDescriptorPermission (TypeDescriptorPermissionFlags flag);
	// properties
	public TypeDescriptorPermissionFlags Flags { get; set; }
	// methods
	public override System.Security.IPermission Copy ();
	public override void FromXml (System.Security.SecurityElement securityElement);
	public override System.Security.IPermission Intersect (System.Security.IPermission target);
	public override bool IsSubsetOf (System.Security.IPermission target);
	public virtual bool IsUnrestricted ();
	public override System.Security.SecurityElement ToXml ();
	public override System.Security.IPermission Union (System.Security.IPermission target);
}
```

### New Type System.Security.Permissions.TypeDescriptorPermissionFlags

```
[Serializable]
[Flags]
public enum TypeDescriptorPermissionFlags {
	NoFlags = 0,
	RestrictedRegistrationAccess = 1,
}
```

   


 <hr>

<h1 id='System.Core'>System.Core.dll</h1>

## Namespace System.Runtime.CompilerServices

### Removed Type System.Runtime.CompilerServices.Closure ### New Type System.Runtime.CompilerServices.ExecutionScope

```
public class ExecutionScope {
	// fields
	public object[] Globals;
	public object[] Locals;
	public ExecutionScope Parent;
	// methods
	public System.Delegate CreateDelegate (int indexLambda, object[] locals);
	public object[] CreateHoistedLocals ();
	public System.Linq.Expressions.Expression IsolateExpression (System.Linq.Expressions.Expression expression, object[] locals);
}
```

   
 <hr>

<h1 id='System.ComponentModel.DataAnnotations'>System.ComponentModel.DataAnnotations.dll</h1>

## Namespace System.ComponentModel.DataAnnotations

### Type Changed: System.ComponentModel.DataAnnotations.CompareAttribute

Modified methods:

```
protected override ValidationResult IsValid (object value, ValidationContext context validationContext)
```

### Type Changed: System.ComponentModel.DataAnnotations.MinLengthAttribute

Removed constructor:

```
public MinLengthAttribute ();
```

### New Type System.ComponentModel.DataAnnotations.AssociatedMetadataTypeTypeDescriptionProvider

```
public class AssociatedMetadataTypeTypeDescriptionProvider : System.ComponentModel.TypeDescriptionProvider {
	// constructors
	public AssociatedMetadataTypeTypeDescriptionProvider (System.Type type);
	public AssociatedMetadataTypeTypeDescriptionProvider (System.Type type, System.Type associatedMetadataType);
	// methods
	public override System.ComponentModel.ICustomTypeDescriptor GetTypeDescriptor (System.Type objectType, object instance);
}
```

### New Type System.ComponentModel.DataAnnotations.BindableTypeAttribute

```
public sealed class BindableTypeAttribute : System.Attribute {
	// constructors
	public BindableTypeAttribute ();
	// properties
	public bool IsBindable { get; set; }
}
```

   


 <hr>

<h1 id='System.Data'>System.Data.dll</h1>

## Namespace System.Data.SqlClient

### New Type System.Data.SqlClient.ApplicationIntent

```
[Serializable]
public enum ApplicationIntent {
	ReadOnly = 1,
	ReadWrite = 0,
}
```

### New Type System.Data.SqlClient.SortOrder

```
[Serializable]
public enum SortOrder {
	Ascending = 0,
	Descending = 1,
	Unspecified = -1,
}
```

## Namespace System.Data.SqlTypes

### Type Changed: System.Data.SqlTypes.SqlCompareOptions

Added value:

```
BinarySort2 = 16384,
```

### Type Changed: System.Data.SqlTypes.SqlString

Added field:

```
public static int BinarySort2;
```

   


 <hr>

<h1 id='System.Runtime.Serialization'>System.Runtime.Serialization.dll</h1>

## Namespace System.Runtime.Serialization

### Type Changed: System.Runtime.Serialization.ContractNamespaceAttribute

Modified constructors:

```
public ContractNamespaceAttribute (string ns contractNamespace)
```

   


 <hr>

<h1 id='compat/monotouch'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.9.1" "8.10.0";
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController

Modified methods:

```
public ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T T : ABPeoplePickerNavigationController> (MonoTouch.UIKit.UITraitCollection traits)
	public ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T T : ABPeoplePickerNavigationController> ()
	public ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T T : ABPeoplePickerNavigationController> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.AudioConverterError

Added value:

```
AudioFormatUnsupported = 560226676,
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVCaptureConnection

Obsoleted properties:

```
[Obsolete ("Use AvailableAudioChannels property instead."]
	public virtual AVCaptureAudioChannel AudioChannels { get; }
```

Added property:

```
public virtual AVCaptureAudioChannel[] AvailableAudioChannels { get; }
```

## Namespace MonoTouch.CoreAnimation

### Type Changed: MonoTouch.CoreAnimation.CABasicAnimation

Added methods:

```
public T GetByAs<T> ();
	public T GetFromAs<T> ();
	public T GetToAs<T> ();
	public void SetBy (MonoTouch.ObjCRuntime.INativeObject value);
	public void SetFrom (MonoTouch.ObjCRuntime.INativeObject value);
	public void SetTo (MonoTouch.ObjCRuntime.INativeObject value);
```

### Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation

Added methods:

```
public T[] GetValuesAs<T> ();
	public void SetValues (MonoTouch.ObjCRuntime.INativeObject[] value);
```

### Type Changed: MonoTouch.CoreAnimation.CALayer

Added methods:

```
public T GetContentsAs<T> ();
	public void SetContents (MonoTouch.Foundation.NSObject value);
```

## Namespace MonoTouch.CoreAudioKit

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioSwitcherView

Modified methods:

```
public CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T T : CAInterAppAudioSwitcherView> ()
	public CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T T : CAInterAppAudioSwitcherView> (MonoTouch.UIKit.UITraitCollection traits)
	public CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T T : CAInterAppAudioSwitcherView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioTransportView

Modified methods:

```
public CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T T : CAInterAppAudioTransportView> (MonoTouch.UIKit.UITraitCollection traits)
	public CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T T : CAInterAppAudioTransportView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
	public CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T T : CAInterAppAudioTransportView> ()
```

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFStream

Added method:

```
public static MonoTouch.CoreServices.CFHTTPStream CreateForStreamedHTTPRequest (MonoTouch.CoreServices.CFHTTPMessage request, MonoTouch.Foundation.NSInputStream body);
```

### Type Changed: MonoTouch.CoreFoundation.DispatchQueue

Added constructor:

```
public DispatchQueue (string label, bool concurrent);
```

Added methods:

```
public void DispatchBarrierAsync (MonoTouch.Foundation.NSAction action);
	public void Submit (System.Action<int> action, long times);
```

### New Type MonoTouch.CoreFoundation.DispatchSource

```
public class DispatchSource : MonoTouch.CoreFoundation.DispatchObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public bool IsCanceled { get; }
	// methods
	public void Cancel ();
	protected override void Dispose (bool disposing);
	public void Resume ();
	public void SetCancelHandler (System.Action handler);
	public void SetEventHandler (System.Action handler);
	public void SetRegistrationHandler (System.Action handler);

	// inner types
	public class Data : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// properties
		public IntPtr PendingData { get; }
		// methods
		public void MergeData (IntPtr value);
	}
	public class DataAdd : MonoTouch.CoreFoundation.DispatchSource+Data, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
	}
	public class DataOr : MonoTouch.CoreFoundation.DispatchSource+Data, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
	}
	public class Mach : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// properties
		public int MachPort { get; }
	}
	public class MachSend : MonoTouch.CoreFoundation.DispatchSource+Mach, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int machPort, bool sendDead, DispatchQueue queue);
		// properties
		public bool SendRightsDestroyed { get; }
	}
	public class MachReceive : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int machPort, DispatchQueue queue);
	}
	public class MemoryPressure : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (MemoryPressureFlags monitorFlags, DispatchQueue queue);
		// properties
		public MemoryPressureFlags PressureFlags { get; }
	}
	public class ProcessMonitor : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int processId, ProcessMonitorFlags monitorKind, DispatchQueue queue);
		// properties
		public ProcessMonitorFlags MonitorFlags { get; }
		public int ProcessId { get; }
	}
	public class ReadMonitor : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, DispatchQueue queue);
		// properties
		public int BytesAvailable { get; }
		public int FileDescriptor { get; }
	}
	public class SignalMonitor : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int signalNumber, DispatchQueue queue);
		// properties
		public int SignalNumber { get; }
		public int SignalsDelivered { get; }
	}
	public class Timer : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
		// properties
		public int TimerFiredCount { get; }
		// methods
		public void SetTimer (DispatchTime time, long nanosecondInterval, long nanosecondLeeway);
	}
	public class VnodeMonitor : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, VnodeMonitorKind vnodeKind, DispatchQueue queue);
		public DispatchSource (string path, VnodeMonitorKind vnodeKind, DispatchQueue queue);
		// properties
		public int FileDescriptor { get; }
		public VnodeMonitorKind ObservedEvents { get; }
		// methods
		protected override void Dispose (bool disposing);
	}
	public class WriteMonitor : MonoTouch.CoreFoundation.DispatchSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, DispatchQueue queue);
		// properties
		public int BufferSpaceAvailable { get; }
		public int FileDescriptor { get; }
	}
}
```

### New Type MonoTouch.CoreFoundation.MemoryPressureFlags

```
[Serializable]
[Flags]
public enum MemoryPressureFlags {
	Critical = 4,
	Normal = 1,
	Warn = 2,
}
```

### New Type MonoTouch.CoreFoundation.ProcessMonitorFlags

```
[Serializable]
[Flags]
public enum ProcessMonitorFlags {
	Exec = 536870912,
	Exit = 2147483648,
	Fork = 1073741824,
	Signal = 134217728,
}
```

### New Type MonoTouch.CoreFoundation.VnodeMonitorKind

```
[Serializable]
[Flags]
public enum VnodeMonitorKind {
	Attrib = 8,
	Delete = 1,
	Extend = 4,
	Link = 16,
	Rename = 32,
	Revoke = 64,
	Write = 2,
}
```

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGBitmapContext

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.CoreGraphics.CGGradientDrawingOptions

Added value:

```
None = 0,
```

## Namespace MonoTouch.CoreMedia

### Type Changed: MonoTouch.CoreMedia.CMTimeRange

Added fields:

```
public static CMTimeRange Invalid;
	public static CMTimeRange Zero;
```

### New Type MonoTouch.CoreMedia.CMPixelFormat

```
[Serializable]
public enum CMPixelFormat {
	AlphaRedGreenBlue32bits = 32,
	BigEndian555_16bits = 16,
	BigEndian565_16bits = 1110783541,
	BlueGreenRedAlpha32bits = 1111970369,
	IndexedGrayWhiteIsZero_8bits = 40,
	LittleEndian555_16bits = 1278555445,
	LittleEndian5551_16bits = 892679473,
	LittleEndian565_16bits = 1278555701,
	RedGreenBlue24bits = 24,
	YpCbCr422_10bits = 1983000880,
	YpCbCr422_16bits = 1983000886,
	YpCbCr422_8bits = 846624121,
	YpCbCr422yuvs_8bits = 2037741171,
	YpCbCr444_10bits = 1983131952,
	YpCbCr444_8bits = 1983066168,
	YpCbCrA4444_8bits = 1983131704,
}
```

## Namespace MonoTouch.CoreText

### Type Changed: MonoTouch.CoreText.CTFontManager

Obsoleted methods:

```
[Obsolete ("API not available on iOS, it will always return false"]
	public static bool IsFontSupported (MonoTouch.Foundation.NSUrl url);
```

## Namespace MonoTouch.EventKitUI

### Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Modified methods:

```
public EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T T : EKEventEditViewController> ()
	public EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T T : EKEventEditViewController> (MonoTouch.UIKit.UITraitCollection traits)
	public EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T T : EKEventEditViewController> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSArray

Added method:

```
public static T[] FromArrayNative<T> (NSArray weakArray);
```

### Type Changed: MonoTouch.Foundation.NSDirectoryEnumerator

Added interfaces:

```
System.Collections.Generic.IEnumerator<NSString>
	System.Collections.Generic.IEnumerator<string>
	System.Collections.IEnumerator
```

### Type Changed: MonoTouch.Foundation.NSDistributedNotificationCenter

Obsoleted methods:

```
[Obsolete ("This is not available in iOS"]
	public void AddObserver (NSObject observer, MonoTouch.ObjCRuntime.Selector aSelector, string aName, string anObject);
	[Obsolete ("This is not available in iOS"]
	public void RemoveObserver (NSObject observer, string aName, string anObject);
```

### Type Changed: MonoTouch.Foundation.NSFileManager

Added method:

```
public NSUrl[] GetMountedVolumes (NSString[] properties, NSVolumeEnumerationOptions options);
```

### Type Changed: MonoTouch.Foundation.NSStream

Added methods:

```
public static void CreateBoundPair (out NSInputStream readStream, out NSOutputStream writeStream, int bufferSize);
	public static void CreatePairWithPeerSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, out NSInputStream readStream, out NSOutputStream writeStream);
	public static void CreatePairWithSocket (MonoTouch.CoreFoundation.CFSocket socket, out NSInputStream readStream, out NSOutputStream writeStream);
	public static void CreatePairWithSocketToHost (System.Net.IPEndPoint endpoint, out NSInputStream readStream, out NSOutputStream writeStream);
```

### Type Changed: MonoTouch.Foundation.NSUrl

Added property:

```
public virtual string PathExtension { get; }
```

### Type Changed: MonoTouch.Foundation.PreserveAttribute

Added constructor:

```
public PreserveAttribute (System.Type type);
```

### Type Changed: MonoTouch.Foundation.ProtocolAttribute

Added property:

```
public bool IsInformal { get; set; }
```

### New Type MonoTouch.Foundation.NSTextChecking

```
public static class NSTextChecking {
	// properties
	public static NSString AirlineKey { get; }
	public static NSString CityKey { get; }
	public static NSString CountryKey { get; }
	public static NSString FlightKey { get; }
	public static NSString JobTitleKey { get; }
	public static NSString NameKey { get; }
	public static NSString OrganizationKey { get; }
	public static NSString PhoneKey { get; }
	public static NSString StateKey { get; }
	public static NSString StreetKey { get; }
	public static NSString ZipKey { get; }
}
```

### New Type MonoTouch.Foundation.NSTextCheckingAddressComponents

```
public class NSTextCheckingAddressComponents : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public NSTextCheckingAddressComponents ();
	public NSTextCheckingAddressComponents (NSDictionary dictionary);
	// properties
	public string City { get; }
	public string Country { get; }
	public string JobTitle { get; }
	public string Name { get; }
	public string Organization { get; }
	public string Phone { get; }
	public string State { get; }
	public string Street { get; }
	public string ZIP { get; }
}
```

### New Type MonoTouch.Foundation.NSTextCheckingResult

```
public class NSTextCheckingResult : MonoTouch.Foundation.NSObject, INSCoding, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSTextCheckingResult (NSCoder coder);
	public NSTextCheckingResult (NSObjectFlag t);
	public NSTextCheckingResult (IntPtr handle);
	// properties
	public NSTextCheckingAddressComponents AddressComponents { get; }
	public virtual string[] AlternativeStrings { get; }
	public override IntPtr ClassHandle { get; }
	public NSTextCheckingTransitComponents Components { get; }
	public virtual NSDate Date { get; }
	public virtual string[] GrammarDetails { get; }
	public virtual uint NumberOfRanges { get; }
	public virtual NSOrthography Orthography { get; }
	public virtual string PhoneNumber { get; }
	public virtual NSRange Range { get; }
	public virtual string ReplacementString { get; }
	public virtual NSTextCheckingType ResultType { get; }
	public virtual double TimeInterval { get; }
	public virtual NSTimeZone TimeZone { get; }
	public virtual NSUrl Url { get; }
	public virtual NSDictionary WeakAddressComponents { get; }
	public virtual NSDictionary WeakComponents { get; }
	// methods
	public static NSTextCheckingResult AddressCheckingResult (NSRange range, NSDictionary components);
	public static NSTextCheckingResult AddressCheckingResult (NSRange range, NSTextCheckingAddressComponents components);
	public virtual NSObject Copy (NSZone zone);
	public static NSTextCheckingResult CorrectionCheckingResult (NSRange range, string replacementString, string[] alternativeStrings);
	public static NSTextCheckingResult CorrectionCheckingResult (NSRange range, string replacementString);
	public static NSTextCheckingResult DashCheckingResult (NSRange range, string replacementString);
	public static NSTextCheckingResult DateCheckingResult (NSRange range, NSDate date);
	public static NSTextCheckingResult DateCheckingResult (NSRange range, NSDate date, NSTimeZone timezone, double duration);
	protected override void Dispose (bool disposing);
	public static NSTextCheckingResult GrammarCheckingResult (NSRange range, string[] details);
	public static NSTextCheckingResult LinkCheckingResult (NSRange range, NSUrl url);
	public static NSTextCheckingResult OrthographyCheckingResult (NSRange range, NSOrthography ortography);
	public static NSTextCheckingResult PhoneNumberCheckingResult (NSRange range, string phoneNumber);
	public static NSTextCheckingResult QuoteCheckingResult (NSRange range, NSString replacementString);
	public virtual NSRange RangeAtIndex (uint idx);
	public static NSTextCheckingResult ReplacementCheckingResult (NSRange range, string replacementString);
	public virtual NSTextCheckingResult ResultByAdjustingRanges (int offset);
	public static NSTextCheckingResult SpellCheckingResult (NSRange range);
	public static NSTextCheckingResult TransitInformationCheckingResult (NSRange range, NSDictionary components);
	public static NSTextCheckingResult TransitInformationCheckingResult (NSRange range, NSTextCheckingTransitComponents components);
}
```

### New Type MonoTouch.Foundation.NSTextCheckingTransitComponents

```
public class NSTextCheckingTransitComponents : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public NSTextCheckingTransitComponents ();
	public NSTextCheckingTransitComponents (NSDictionary dictionary);
	// properties
	public string Airline { get; }
	public string Flight { get; }
}
```

### New Type MonoTouch.Foundation.NSTextCheckingType

```
[Serializable]
public enum NSTextCheckingType {
	Address = 16,
	Correction = 512,
	Dash = 128,
	Date = 8,
	Grammar = 4,
	Link = 32,
	Orthography = 1,
	PhoneNumber = 2048,
	Quote = 64,
	RegularExpression = 1024,
	Replacement = 256,
	Spelling = 2,
	TransitInformation = 4096,
}
```

### New Type MonoTouch.Foundation.NSTextCheckingTypes

```
[Serializable]
public enum NSTextCheckingTypes {
	AllCustomTypes = 18446744069414584320,
	AllSystemTypes = 4294967295,
	AllTypes = 18446744073709551615,
}
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKAchievementViewController

Modified methods:

```
public GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T T : GKAchievementViewController> ()
	public GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T T : GKAchievementViewController> (MonoTouch.UIKit.UITraitCollection traits)
	public GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T T : GKAchievementViewController> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Modified methods:

```
public GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T T : GKFriendRequestComposeViewController> (MonoTouch.UIKit.UITraitCollection traits)
	public GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T T : GKFriendRequestComposeViewController> ()
	public GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T T : GKFriendRequestComposeViewController> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Modified methods:

```
public GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T T : GKLeaderboardViewController> ()
	public GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T T : GKLeaderboardViewController> (MonoTouch.UIKit.UITraitCollection traits)
	public GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T T : GKLeaderboardViewController> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Modified methods:

```
public GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T T : GKTurnBasedMatchmakerViewController> ()
	public GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T T : GKTurnBasedMatchmakerViewController> (MonoTouch.UIKit.UITraitCollection traits)
	public GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T T : GKTurnBasedMatchmakerViewController> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKView

Modified methods:

```
public GLKView.GLKViewAppearance GetAppearance<T T : GLKView> (MonoTouch.UIKit.UITraitCollection traits)
	public GLKView.GLKViewAppearance GetAppearance<T T : GLKView> ()
	public GLKView.GLKViewAppearance GetAppearance<T T : GLKView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MonoTouch.HealthKit

### Type Changed: MonoTouch.HealthKit.HKAnchoredObjectQuery

Added constructor:

```
public HKAnchoredObjectQuery (HKSampleType type, MonoTouch.Foundation.NSPredicate predicate, uint anchor, uint limit, HKAnchoredObjectResultHandler2 completion);
```

### Type Changed: MonoTouch.HealthKit.HKQuantitySample

Added method:

```
public static HKQuantitySample FromType (HKQuantityType quantityType, HKQuantity quantity, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate);
```

### New Type MonoTouch.HealthKit.HKAnchoredObjectResultHandler2

```
public sealed delegate HKAnchoredObjectResultHandler2 : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKAnchoredObjectResultHandler2 (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKAnchoredObjectQuery query, HKSample[] results, uint newAnchor, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKAnchoredObjectQuery query, HKSample[] results, uint newAnchor, MonoTouch.Foundation.NSError error);
}
```

## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADBannerView

Modified methods:

```
public ADBannerView.ADBannerViewAppearance GetAppearance<T T : ADBannerView> ()
	public ADBannerView.ADBannerViewAppearance GetAppearance<T T : ADBannerView> (MonoTouch.UIKit.UITraitCollection traits)
	public ADBannerView.ADBannerViewAppearance GetAppearance<T T : ADBannerView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Modified methods:

```
public MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T T : MKAnnotationView> ()
	public MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T T : MKAnnotationView> (MonoTouch.UIKit.UITraitCollection traits)
	public MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T T : MKAnnotationView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.MapKit.MKCircleView

Modified methods:

```
public MKCircleView.MKCircleViewAppearance GetAppearance<T T : MKCircleView> ()
	public MKCircleView.MKCircleViewAppearance GetAppearance<T T : MKCircleView> (MonoTouch.UIKit.UITraitCollection traits)
	public MKCircleView.MKCircleViewAppearance GetAppearance<T T : MKCircleView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.MapKit.MKMapView

Modified methods:

```
public MKMapView.MKMapViewAppearance GetAppearance<T T : MKMapView> (MonoTouch.UIKit.UITraitCollection traits)
	public MKMapView.MKMapViewAppearance GetAppearance<T T : MKMapView> ()
	public MKMapView.MKMapViewAppearance GetAppearance<T T : MKMapView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Modified methods:

```
public MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T T : MKOverlayPathView> (MonoTouch.UIKit.UITraitCollection traits)
	public MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T T : MKOverlayPathView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
	public MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T T : MKOverlayPathView> ()
```

### Type Changed: MonoTouch.MapKit.MKOverlayView

Modified methods:

```
public MKOverlayView.MKOverlayViewAppearance GetAppearance<T T : MKOverlayView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
	public MKOverlayView.MKOverlayViewAppearance GetAppearance<T T : MKOverlayView> (MonoTouch.UIKit.UITraitCollection traits)
	public MKOverlayView.MKOverlayViewAppearance GetAppearance<T T : MKOverlayView> ()
```

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Modified methods:

```
public MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T T : MKPinAnnotationView> ()
	public MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T T : MKPinAnnotationView> (MonoTouch.UIKit.UITraitCollection traits)
	public MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T T : MKPinAnnotationView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.MapKit.MKPointAnnotation

Added property:

```
public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate { get; set; }
```

### Type Changed: MonoTouch.MapKit.MKPolygonView

Modified methods:

```
public MKPolygonView.MKPolygonViewAppearance GetAppearance<T T : MKPolygonView> ()
	public MKPolygonView.MKPolygonViewAppearance GetAppearance<T T : MKPolygonView> (MonoTouch.UIKit.UITraitCollection traits)
	public MKPolygonView.MKPolygonViewAppearance GetAppearance<T T : MKPolygonView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.MapKit.MKPolylineView

Modified methods:

```
public MKPolylineView.MKPolylineViewAppearance GetAppearance<T T : MKPolylineView> ()
	public MKPolylineView.MKPolylineViewAppearance GetAppearance<T T : MKPolylineView> (MonoTouch.UIKit.UITraitCollection traits)
	public MKPolylineView.MKPolylineViewAppearance GetAppearance<T T : MKPolylineView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.MapKit.MKUserTrackingBarButtonItem

Modified methods:

```
public MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T T : MKUserTrackingBarButtonItem> ()
	public MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T T : MKUserTrackingBarButtonItem> (MonoTouch.UIKit.UITraitCollection traits)
	public MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T T : MKUserTrackingBarButtonItem> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Modified methods:

```
public MPVolumeView.MPVolumeViewAppearance GetAppearance<T T : MPVolumeView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
	public MPVolumeView.MPVolumeViewAppearance GetAppearance<T T : MPVolumeView> ()
	public MPVolumeView.MPVolumeViewAppearance GetAppearance<T T : MPVolumeView> (MonoTouch.UIKit.UITraitCollection traits)
```

## Namespace MonoTouch.MessageUI

### Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Modified methods:

```
public MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T T : MFMailComposeViewController> ()
	public MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T T : MFMailComposeViewController> (MonoTouch.UIKit.UITraitCollection traits)
	public MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T T : MFMailComposeViewController> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Modified methods:

```
public MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T T : MFMessageComposeViewController> (MonoTouch.UIKit.UITraitCollection traits)
	public MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T T : MFMessageComposeViewController> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
	public MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T T : MFMessageComposeViewController> ()
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Dlfcn

Added method:

```
public static IntPtr dlsym (Dlfcn.RTLD lookupType, string symbol);
```

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

```
public static IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_IntPtr_Double (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, double arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_IntPtr_Double (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, double arg4);
```

### Type Changed: MonoTouch.ObjCRuntime.Runtime

Added method:

```
public static MonoTouch.Foundation.NSObject TryGetNSObject (IntPtr ptr);
```

### New Type MonoTouch.ObjCRuntime.CategoryAttribute

```
public class CategoryAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public CategoryAttribute (System.Type type);
	// properties
	public string Name { get; set; }
	public System.Type Type { get; set; }
}
```

### New Type MonoTouch.ObjCRuntime.Protocol

```
public class Protocol : INativeObject {
	// constructors
	public Protocol (string name);
	public Protocol (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	public string Name { get; }
	// methods
	public static IntPtr GetHandle (string name);
}
```

## Namespace MonoTouch.PassKit

### Type Changed: MonoTouch.PassKit.PKPaymentButton

Modified methods:

```
public PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T T : PKPaymentButton> ()
	public PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T T : PKPaymentButton> (MonoTouch.UIKit.UITraitCollection traits)
	public PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T T : PKPaymentButton> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MonoTouch.SceneKit

### Type Changed: MonoTouch.SceneKit.SCNGeometry

Obsoleted methods:

```
[Obsolete ("Use the Create(SCNGeometrySource[], SCNGeometryElement[]) method instead, as it has a strongly typed return"]
	public static MonoTouch.Foundation.NSObject FromSources (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
```

Added method:

```
public static SCNGeometry Create (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
```

### Type Changed: MonoTouch.SceneKit.SCNView

Modified methods:

```
public SCNView.SCNViewAppearance GetAppearance<T T : SCNView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
	public SCNView.SCNViewAppearance GetAppearance<T T : SCNView> ()
	public SCNView.SCNViewAppearance GetAppearance<T T : SCNView> (MonoTouch.UIKit.UITraitCollection traits)
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecRecord

Added constructor:

```
public SecRecord ();
```

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKView

Modified methods:

```
public SKView.SKViewAppearance GetAppearance<T T : SKView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
	public SKView.SKViewAppearance GetAppearance<T T : SKView> (MonoTouch.UIKit.UITraitCollection traits)
	public SKView.SKViewAppearance GetAppearance<T T : SKView> ()
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIActionSheet

Modified methods:

```
public UIActionSheet.UIActionSheetAppearance GetAppearance<T T : UIActionSheet> (UITraitCollection traits)
	public UIActionSheet.UIActionSheetAppearance GetAppearance<T T : UIActionSheet> ()
	public UIActionSheet.UIActionSheetAppearance GetAppearance<T T : UIActionSheet> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Modified methods:

```
public UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T T : UIActivityIndicatorView> (UITraitCollection traits)
	public UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T T : UIActivityIndicatorView> (UITraitCollection traits, System.Type[] containers)
	public UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T T : UIActivityIndicatorView> ()
```

### Type Changed: MonoTouch.UIKit.UIAlertView

Modified methods:

```
public UIAlertView.UIAlertViewAppearance GetAppearance<T T : UIAlertView> (UITraitCollection traits)
	public UIAlertView.UIAlertViewAppearance GetAppearance<T T : UIAlertView> (UITraitCollection traits, System.Type[] containers)
	public UIAlertView.UIAlertViewAppearance GetAppearance<T T : UIAlertView> ()
```

### Type Changed: MonoTouch.UIKit.UIApplication

Added field:

```
public static bool CheckForEventAndDelegateMismatches;
```

### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Modified methods:

```
public UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T T : UIBarButtonItem> ()
	public UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T T : UIBarButtonItem> (UITraitCollection traits, System.Type[] containers)
	public UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T T : UIBarButtonItem> (UITraitCollection traits)
```

### Type Changed: MonoTouch.UIKit.UIBarItem

Modified methods:

```
public UIBarItem.UIBarItemAppearance GetAppearance<T T : UIBarItem> ()
	public UIBarItem.UIBarItemAppearance GetAppearance<T T : UIBarItem> (UITraitCollection traits)
	public UIBarItem.UIBarItemAppearance GetAppearance<T T : UIBarItem> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIButton

Modified methods:

```
public UIButton.UIButtonAppearance GetAppearance<T T : UIButton> ()
	public UIButton.UIButtonAppearance GetAppearance<T T : UIButton> (UITraitCollection traits)
	public UIButton.UIButtonAppearance GetAppearance<T T : UIButton> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Modified methods:

```
public UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T T : UICollectionReusableView> (UITraitCollection traits, System.Type[] containers)
	public UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T T : UICollectionReusableView> (UITraitCollection traits)
	public UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T T : UICollectionReusableView> ()
```

### Type Changed: MonoTouch.UIKit.UICollectionView

Modified methods:

```
public UICollectionView.UICollectionViewAppearance GetAppearance<T T : UICollectionView> (UITraitCollection traits)
	public UICollectionView.UICollectionViewAppearance GetAppearance<T T : UICollectionView> ()
	public UICollectionView.UICollectionViewAppearance GetAppearance<T T : UICollectionView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Modified methods:

```
public UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T T : UICollectionViewCell> ()
	public UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T T : UICollectionViewCell> (UITraitCollection traits)
	public UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T T : UICollectionViewCell> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIControl

Modified methods:

```
public UIControl.UIControlAppearance GetAppearance<T T : UIControl> (UITraitCollection traits)
	public UIControl.UIControlAppearance GetAppearance<T T : UIControl> ()
	public UIControl.UIControlAppearance GetAppearance<T T : UIControl> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIDatePicker

Modified methods:

```
public UIDatePicker.UIDatePickerAppearance GetAppearance<T T : UIDatePicker> (UITraitCollection traits)
	public UIDatePicker.UIDatePickerAppearance GetAppearance<T T : UIDatePicker> (UITraitCollection traits, System.Type[] containers)
	public UIDatePicker.UIDatePickerAppearance GetAppearance<T T : UIDatePicker> ()
```

### Type Changed: MonoTouch.UIKit.UIDocument

Added property:

```
public static MonoTouch.Foundation.NSString UserActivityDocumentUrlKey { get; }
```

### Type Changed: MonoTouch.UIKit.UIFont

Added methods:

```
public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (UIFont f1, UIFont f2);
	public static bool op_Inequality (UIFont f1, UIFont f2);
```

### Type Changed: MonoTouch.UIKit.UIImageView

Modified methods:

```
public UIImageView.UIImageViewAppearance GetAppearance<T T : UIImageView> (UITraitCollection traits)
	public UIImageView.UIImageViewAppearance GetAppearance<T T : UIImageView> (UITraitCollection traits, System.Type[] containers)
	public UIImageView.UIImageViewAppearance GetAppearance<T T : UIImageView> ()
```

### Type Changed: MonoTouch.UIKit.UIInputView

Modified methods:

```
public UIInputView.UIInputViewAppearance GetAppearance<T T : UIInputView> ()
	public UIInputView.UIInputViewAppearance GetAppearance<T T : UIInputView> (UITraitCollection traits)
	public UIInputView.UIInputViewAppearance GetAppearance<T T : UIInputView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UILabel

Modified methods:

```
public UILabel.UILabelAppearance GetAppearance<T T : UILabel> ()
	public UILabel.UILabelAppearance GetAppearance<T T : UILabel> (UITraitCollection traits)
	public UILabel.UILabelAppearance GetAppearance<T T : UILabel> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UINavigationBar

Modified methods:

```
public UINavigationBar.UINavigationBarAppearance GetAppearance<T T : UINavigationBar> (UITraitCollection traits, System.Type[] containers)
	public UINavigationBar.UINavigationBarAppearance GetAppearance<T T : UINavigationBar> ()
	public UINavigationBar.UINavigationBarAppearance GetAppearance<T T : UINavigationBar> (UITraitCollection traits)
```

### Type Changed: MonoTouch.UIKit.UIPageControl

Modified methods:

```
public UIPageControl.UIPageControlAppearance GetAppearance<T T : UIPageControl> (UITraitCollection traits)
	public UIPageControl.UIPageControlAppearance GetAppearance<T T : UIPageControl> (UITraitCollection traits, System.Type[] containers)
	public UIPageControl.UIPageControlAppearance GetAppearance<T T : UIPageControl> ()
```

### Type Changed: MonoTouch.UIKit.UIPickerView

Modified methods:

```
public UIPickerView.UIPickerViewAppearance GetAppearance<T T : UIPickerView> (UITraitCollection traits, System.Type[] containers)
	public UIPickerView.UIPickerViewAppearance GetAppearance<T T : UIPickerView> (UITraitCollection traits)
	public UIPickerView.UIPickerViewAppearance GetAppearance<T T : UIPickerView> ()
```

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Modified methods:

```
public UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T T : UIPopoverBackgroundView> (UITraitCollection traits)
	public UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T T : UIPopoverBackgroundView> (UITraitCollection traits, System.Type[] containers)
	public UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T T : UIPopoverBackgroundView> ()
```

### Type Changed: MonoTouch.UIKit.UIProgressView

Modified methods:

```
public UIProgressView.UIProgressViewAppearance GetAppearance<T T : UIProgressView> (UITraitCollection traits)
	public UIProgressView.UIProgressViewAppearance GetAppearance<T T : UIProgressView> (UITraitCollection traits, System.Type[] containers)
	public UIProgressView.UIProgressViewAppearance GetAppearance<T T : UIProgressView> ()
```

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Modified methods:

```
public UIRefreshControl.UIRefreshControlAppearance GetAppearance<T T : UIRefreshControl> ()
	public UIRefreshControl.UIRefreshControlAppearance GetAppearance<T T : UIRefreshControl> (UITraitCollection traits)
	public UIRefreshControl.UIRefreshControlAppearance GetAppearance<T T : UIRefreshControl> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIScrollView

Modified methods:

```
public UIScrollView.UIScrollViewAppearance GetAppearance<T T : UIScrollView> (UITraitCollection traits)
	public UIScrollView.UIScrollViewAppearance GetAppearance<T T : UIScrollView> ()
	public UIScrollView.UIScrollViewAppearance GetAppearance<T T : UIScrollView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UISearchBar

Modified methods:

```
public UISearchBar.UISearchBarAppearance GetAppearance<T T : UISearchBar> ()
	public UISearchBar.UISearchBarAppearance GetAppearance<T T : UISearchBar> (UITraitCollection traits)
	public UISearchBar.UISearchBarAppearance GetAppearance<T T : UISearchBar> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Modified methods:

```
public UISegmentedControl.UISegmentedControlAppearance GetAppearance<T T : UISegmentedControl> ()
	public UISegmentedControl.UISegmentedControlAppearance GetAppearance<T T : UISegmentedControl> (UITraitCollection traits, System.Type[] containers)
	public UISegmentedControl.UISegmentedControlAppearance GetAppearance<T T : UISegmentedControl> (UITraitCollection traits)
```

### Type Changed: MonoTouch.UIKit.UISlider

Modified methods:

```
public UISlider.UISliderAppearance GetAppearance<T T : UISlider> (UITraitCollection traits, System.Type[] containers)
	public UISlider.UISliderAppearance GetAppearance<T T : UISlider> ()
	public UISlider.UISliderAppearance GetAppearance<T T : UISlider> (UITraitCollection traits)
```

### Type Changed: MonoTouch.UIKit.UIStepper

Modified methods:

```
public UIStepper.UIStepperAppearance GetAppearance<T T : UIStepper> (UITraitCollection traits)
	public UIStepper.UIStepperAppearance GetAppearance<T T : UIStepper> ()
	public UIStepper.UIStepperAppearance GetAppearance<T T : UIStepper> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UISwitch

Modified methods:

```
public UISwitch.UISwitchAppearance GetAppearance<T T : UISwitch> (UITraitCollection traits)
	public UISwitch.UISwitchAppearance GetAppearance<T T : UISwitch> (UITraitCollection traits, System.Type[] containers)
	public UISwitch.UISwitchAppearance GetAppearance<T T : UISwitch> ()
```

### Type Changed: MonoTouch.UIKit.UITabBar

Modified methods:

```
public UITabBar.UITabBarAppearance GetAppearance<T T : UITabBar> (UITraitCollection traits)
	public UITabBar.UITabBarAppearance GetAppearance<T T : UITabBar> ()
	public UITabBar.UITabBarAppearance GetAppearance<T T : UITabBar> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UITabBarItem

Modified methods:

```
public UITabBarItem.UITabBarItemAppearance GetAppearance<T T : UITabBarItem> (UITraitCollection traits)
	public UITabBarItem.UITabBarItemAppearance GetAppearance<T T : UITabBarItem> (UITraitCollection traits, System.Type[] containers)
	public UITabBarItem.UITabBarItemAppearance GetAppearance<T T : UITabBarItem> ()
```

### Type Changed: MonoTouch.UIKit.UITableView

Modified methods:

```
public UITableView.UITableViewAppearance GetAppearance<T T : UITableView> (UITraitCollection traits)
	public UITableView.UITableViewAppearance GetAppearance<T T : UITableView> ()
	public UITableView.UITableViewAppearance GetAppearance<T T : UITableView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UITableViewCell

Modified methods:

```
public UITableViewCell.UITableViewCellAppearance GetAppearance<T T : UITableViewCell> ()
	public UITableViewCell.UITableViewCellAppearance GetAppearance<T T : UITableViewCell> (UITraitCollection traits)
	public UITableViewCell.UITableViewCellAppearance GetAppearance<T T : UITableViewCell> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Modified methods:

```
public UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T T : UITableViewHeaderFooterView> (UITraitCollection traits)
	public UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T T : UITableViewHeaderFooterView> (UITraitCollection traits, System.Type[] containers)
	public UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T T : UITableViewHeaderFooterView> ()
```

### Type Changed: MonoTouch.UIKit.UITextField

Modified methods:

```
public UITextField.UITextFieldAppearance GetAppearance<T T : UITextField> (UITraitCollection traits)
	public UITextField.UITextFieldAppearance GetAppearance<T T : UITextField> ()
	public UITextField.UITextFieldAppearance GetAppearance<T T : UITextField> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UITextView

Modified methods:

```
public UITextView.UITextViewAppearance GetAppearance<T T : UITextView> (UITraitCollection traits, System.Type[] containers)
	public UITextView.UITextViewAppearance GetAppearance<T T : UITextView> ()
	public UITextView.UITextViewAppearance GetAppearance<T T : UITextView> (UITraitCollection traits)
```

### Type Changed: MonoTouch.UIKit.UIToolbar

Modified methods:

```
public UIToolbar.UIToolbarAppearance GetAppearance<T T : UIToolbar> (UITraitCollection traits)
	public UIToolbar.UIToolbarAppearance GetAppearance<T T : UIToolbar> ()
	public UIToolbar.UIToolbarAppearance GetAppearance<T T : UIToolbar> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIView

Modified methods:

```
public UIView.UIViewAppearance GetAppearance<T T : UIView> (UITraitCollection traits)
	public UIView.UIViewAppearance GetAppearance<T T : UIView> ()
	public UIView.UIViewAppearance GetAppearance<T T : UIView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIVisualEffectView

Modified methods:

```
public UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T T : UIVisualEffectView> ()
	public UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T T : UIVisualEffectView> (UITraitCollection traits)
	public UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T T : UIVisualEffectView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIWebView

Modified methods:

```
public UIWebView.UIWebViewAppearance GetAppearance<T T : UIWebView> ()
	public UIWebView.UIWebViewAppearance GetAppearance<T T : UIWebView> (UITraitCollection traits)
	public UIWebView.UIWebViewAppearance GetAppearance<T T : UIWebView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MonoTouch.UIKit.UIWindow

Modified methods:

```
public UIWindow.UIWindowAppearance GetAppearance<T T : UIWindow> (UITraitCollection traits)
	public UIWindow.UIWindowAppearance GetAppearance<T T : UIWindow> ()
	public UIWindow.UIWindowAppearance GetAppearance<T T : UIWindow> (UITraitCollection traits, System.Type[] containers)
```

### New Type MonoTouch.UIKit.IUIViewControllerRestoration

```
public interface IUIViewControllerRestoration : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.UIViewControllerRestoration_Extensions

```
public static class UIViewControllerRestoration_Extensions {
}
```

## Namespace MonoTouch.WebKit

### Type Changed: MonoTouch.WebKit.WKWebView

Modified methods:

```
public WKWebView.WKWebViewAppearance GetAppearance<T T : WKWebView> ()
	public WKWebView.WKWebViewAppearance GetAppearance<T T : WKWebView> (MonoTouch.UIKit.UITraitCollection traits)
	public WKWebView.WKWebViewAppearance GetAppearance<T T : WKWebView> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace OpenTK

### Type Changed: OpenTK.Matrix3

Added constructor:

```
public Matrix3 (Matrix4 matrix);
```

## New Namespace MonoTouch.VideoToolbox

### New Type MonoTouch.VideoToolbox.VTColorPrimaries

```
[Serializable]
public enum VTColorPrimaries {
	Ebu3213 = 2,
	ItuR7092 = 1,
	P22 = 4,
	SmpteC = 3,
	Unset = 0,
}
```

### New Type MonoTouch.VideoToolbox.VTCompressionProperties

```
public class VTCompressionProperties : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public VTCompressionProperties ();
	public VTCompressionProperties (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public bool? AllowFrameReordering { get; set; }
	public bool? AllowTemporalCompression { get; set; }
	public bool? AspectRatio16x9 { get; set; }
	public int? AverageBitRate { get; set; }
	public MonoTouch.Foundation.NSDictionary CleanAperture { get; set; }
	public System.Collections.Generic.List<VTDataRateLimit> DataRateLimits { get; set; }
	public MonoTouch.CoreMedia.CMPixelFormat? Depth { get; set; }
	public double? ExpectedDuration { get; set; }
	public double? ExpectedFrameRate { get; set; }
	public VTFieldCount? FieldCount { get; set; }
	public VTFieldDetail FieldDetail { get; set; }
	public VTH264EntropyMode H264EntropyMode { get; set; }
	public MonoTouch.Foundation.NSData ICCProfile { get; set; }
	public int? MaxFrameDelayCount { get; set; }
	public int? MaxH264SliceBytes { get; set; }
	public int? MaxKeyFrameInterval { get; set; }
	public double? MaxKeyFrameIntervalDuration { get; set; }
	public bool? MoreFramesAfterEnd { get; set; }
	public bool? MoreFramesBeforeStart { get; set; }
	public VTMultiPassStorage MultiPassStorage { get; set; }
	public int? NumberOfPendingFrames { get; }
	public MonoTouch.Foundation.NSDictionary PixelAspectRatio { get; set; }
	public bool? PixelBufferPoolIsShared { get; }
	public MonoTouch.Foundation.NSDictionary PixelTransferProperties { get; set; }
	public VTProfileLevel ProfileLevel { get; set; }
	public bool? ProgressiveScan { get; set; }
	public float? Quality { get; set; }
	public bool? RealTime { get; set; }
	public uint? SourceFrameCount { get; set; }
	public VTTransferFunction TransferFunction { get; set; }
	public bool? UsingHardwareAcceleratedVideoEncoder { get; }
	public MonoTouch.Foundation.NSDictionary VideoEncoderPixelBufferAttributes { get; }
	public VTYCbCrMatrix YCbCrMatrix { get; set; }
}
```

### New Type MonoTouch.VideoToolbox.VTCompressionPropertyKey

```
public static class VTCompressionPropertyKey {
	// properties
	public static MonoTouch.Foundation.NSString AllowFrameReordering { get; }
	public static MonoTouch.Foundation.NSString AllowTemporalCompression { get; }
	public static MonoTouch.Foundation.NSString AspectRatio16x9 { get; }
	public static MonoTouch.Foundation.NSString AverageBitRate { get; }
	public static MonoTouch.Foundation.NSString CleanAperture { get; }
	public static MonoTouch.Foundation.NSString ColorPrimaries { get; }
	public static MonoTouch.Foundation.NSString DataRateLimits { get; }
	public static MonoTouch.Foundation.NSString Depth { get; }
	public static MonoTouch.Foundation.NSString ExpectedDuration { get; }
	public static MonoTouch.Foundation.NSString ExpectedFrameRate { get; }
	public static MonoTouch.Foundation.NSString FieldCount { get; }
	public static MonoTouch.Foundation.NSString FieldDetail { get; }
	public static MonoTouch.Foundation.NSString H264EntropyMode { get; }
	public static MonoTouch.Foundation.NSString ICCProfile { get; }
	public static MonoTouch.Foundation.NSString MaxFrameDelayCount { get; }
	public static MonoTouch.Foundation.NSString MaxH264SliceBytes { get; }
	public static MonoTouch.Foundation.NSString MaxKeyFrameInterval { get; }
	public static MonoTouch.Foundation.NSString MaxKeyFrameIntervalDuration { get; }
	public static MonoTouch.Foundation.NSString MoreFramesAfterEnd { get; }
	public static MonoTouch.Foundation.NSString MoreFramesBeforeStart { get; }
	public static MonoTouch.Foundation.NSString MultiPassStorage { get; }
	public static MonoTouch.Foundation.NSString NumberOfPendingFrames { get; }
	public static MonoTouch.Foundation.NSString PixelAspectRatio { get; }
	public static MonoTouch.Foundation.NSString PixelBufferPoolIsShared { get; }
	public static MonoTouch.Foundation.NSString PixelTransferProperties { get; }
	public static MonoTouch.Foundation.NSString ProfileLevel { get; }
	public static MonoTouch.Foundation.NSString ProgressiveScan { get; }
	public static MonoTouch.Foundation.NSString Quality { get; }
	public static MonoTouch.Foundation.NSString RealTime { get; }
	public static MonoTouch.Foundation.NSString SourceFrameCount { get; }
	public static MonoTouch.Foundation.NSString TransferFunction { get; }
	public static MonoTouch.Foundation.NSString UsingHardwareAcceleratedVideoEncoder { get; }
	public static MonoTouch.Foundation.NSString VideoEncoderPixelBufferAttributes { get; }
	public static MonoTouch.Foundation.NSString YCbCrMatrix { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTCompressionSession

```
public class VTCompressionSession : MonoTouch.VideoToolbox.VTSession, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTCompressionSession (IntPtr handle);
	// methods
	protected override void ~VTCompressionSession ();
	public VTStatus BeginPass (VTCompressionSessionOptionFlags flags);
	public VTStatus CompleteFrames (MonoTouch.CoreMedia.CMTime completeUntilPresentationTimeStamp);
	public static VTCompressionSession Create (int width, int height, MonoTouch.CoreMedia.CMVideoCodecType codecType, VTCompressionSession.VTCompressionOutputCallback compressionOutputCallback, VTVideoEncoderSpecification encoderSpecification, MonoTouch.Foundation.NSDictionary sourceImageBufferAttributes);
	public void Dispose ();
	protected override void Dispose (bool disposing);
	public VTStatus EncodeFrame (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, MonoTouch.CoreMedia.CMTime presentationTimestampe, MonoTouch.CoreMedia.CMTime duration, MonoTouch.Foundation.NSDictionary frameProperties, IntPtr sourceFrame, out VTEncodeInfoFlags infoFlags);
	public VTStatus EndPass (out bool furtherPassesRequested);
	public VTStatus EndPassAsFinal ();
	public MonoTouch.CoreVideo.CVPixelBufferPool GetPixelBufferPool ();
	public VTStatus GetTimeRangesForNextPass (out MonoTouch.CoreMedia.CMTimeRange[] timeRanges);
	public VTStatus PrepareToEncodeFrames ();
	public VTStatus SetCompressionProperties (VTCompressionProperties options);

	// inner types
	public sealed delegate VTCompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public VTCompressionSession (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, MonoTouch.CoreMedia.CMSampleBuffer buffer, System.AsyncCallback callback, object object);
		public virtual void EndInvoke (System.IAsyncResult result);
		public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, MonoTouch.CoreMedia.CMSampleBuffer buffer);
	}
}
```

### New Type MonoTouch.VideoToolbox.VTCompressionSessionOptionFlags

```
[Serializable]
[Flags]
public enum VTCompressionSessionOptionFlags {
	BeginFinalPass = 1,
}
```

### New Type MonoTouch.VideoToolbox.VTDataRateLimit

```
public struct VTDataRateLimit {
	// constructors
	public VTDataRateLimit (uint numberOfBytes, double seconds);
	// properties
	public uint NumberOfBytes { get; set; }
	public double Seconds { get; set; }
}
```

### New Type MonoTouch.VideoToolbox.VTDecodeFrameFlags

```
[Serializable]
[Flags]
public enum VTDecodeFrameFlags {
	DoNotOutputFrame = 2,
	EnableAsynchronousDecompression = 1,
	EnableTemporalProcessing = 8,
	OneTimeRealTimePlayback = 4,
}
```

### New Type MonoTouch.VideoToolbox.VTDecodeInfoFlags

```
[Serializable]
[Flags]
public enum VTDecodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
	ImageBufferModifiable = 4,
}
```

### New Type MonoTouch.VideoToolbox.VTDecompressionProperties

```
public class VTDecompressionProperties : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public VTDecompressionProperties ();
	public VTDecompressionProperties (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public bool? ContentHasInterframeDependencies { get; }
	public VTDeinterlaceMode DeinterlaceMode { get; set; }
	public VTFieldMode FieldMode { get; set; }
	public MonoTouch.Foundation.NSDictionary MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public MonoTouch.Foundation.NSDictionary MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public uint? NumberOfFramesBeingDecoded { get; }
	public VTOnlyTheseFrames OnlyTheseFrames { get; set; }
	public uint? OutputPoolRequestedMinimumBufferCount { get; set; }
	public MonoTouch.CoreVideo.CVPixelBufferPool PixelBufferPool { get; }
	public bool? PixelBufferPoolIsShared { get; }
	public MonoTouch.CoreMedia.CMPixelFormat[] PixelFormatsWithReducedResolutionSupport { get; }
	public MonoTouch.Foundation.NSDictionary PixelTransferProperties { get; set; }
	public bool? RealTime { get; set; }
	public uint? ReducedCoefficientDecode { get; set; }
	public float? ReducedFrameDelivery { get; set; }
	public VTDecompressionResolutionOptions ReducedResolutionDecode { get; set; }
	public MonoTouch.Foundation.NSDictionary[] SuggestedQualityOfServiceTiers { get; }
	public MonoTouch.CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByPerformance { get; }
	public MonoTouch.CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByQuality { get; }
	public uint? ThreadCount { get; set; }
	public bool? UsingHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTDecompressionPropertyKey

```
public static class VTDecompressionPropertyKey {
	// properties
	public static MonoTouch.Foundation.NSString ContentHasInterframeDependencies { get; }
	public static MonoTouch.Foundation.NSString DeinterlaceMode { get; }
	public static MonoTouch.Foundation.NSString DeinterlaceMode_Temporal { get; }
	public static MonoTouch.Foundation.NSString DeinterlaceMode_VerticalFilter { get; }
	public static MonoTouch.Foundation.NSString FieldMode { get; }
	public static MonoTouch.Foundation.NSString FieldMode_BothFields { get; }
	public static MonoTouch.Foundation.NSString FieldMode_BottomFieldOnly { get; }
	public static MonoTouch.Foundation.NSString FieldMode_DeinterlaceFields { get; }
	public static MonoTouch.Foundation.NSString FieldMode_SingleField { get; }
	public static MonoTouch.Foundation.NSString FieldMode_TopFieldOnly { get; }
	public static MonoTouch.Foundation.NSString MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static MonoTouch.Foundation.NSString MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static MonoTouch.Foundation.NSString NumberOfFramesBeingDecoded { get; }
	public static MonoTouch.Foundation.NSString OnlyTheseFrames { get; }
	public static MonoTouch.Foundation.NSString OnlyTheseFrames_AllFrames { get; }
	public static MonoTouch.Foundation.NSString OnlyTheseFrames_IFrames { get; }
	public static MonoTouch.Foundation.NSString OnlyTheseFrames_KeyFrames { get; }
	public static MonoTouch.Foundation.NSString OnlyTheseFrames_NonDroppableFrames { get; }
	public static MonoTouch.Foundation.NSString OutputPoolRequestedMinimumBufferCount { get; }
	public static MonoTouch.Foundation.NSString PixelBufferPool { get; }
	public static MonoTouch.Foundation.NSString PixelBufferPoolIsShared { get; }
	public static MonoTouch.Foundation.NSString PixelFormatsWithReducedResolutionSupport { get; }
	public static MonoTouch.Foundation.NSString PixelTransferProperties { get; }
	public static MonoTouch.Foundation.NSString RealTime { get; }
	public static MonoTouch.Foundation.NSString ReducedCoefficientDecode { get; }
	public static MonoTouch.Foundation.NSString ReducedFrameDelivery { get; }
	public static MonoTouch.Foundation.NSString ReducedResolutionDecode { get; }
	public static MonoTouch.Foundation.NSString SuggestedQualityOfServiceTiers { get; }
	public static MonoTouch.Foundation.NSString SupportedPixelFormatsOrderedByPerformance { get; }
	public static MonoTouch.Foundation.NSString SupportedPixelFormatsOrderedByQuality { get; }
	public static MonoTouch.Foundation.NSString ThreadCount { get; }
	public static MonoTouch.Foundation.NSString UsingHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTDecompressionResolutionKeys

```
public static class VTDecompressionResolutionKeys {
	// properties
	public static MonoTouch.Foundation.NSString Height { get; }
	public static MonoTouch.Foundation.NSString Width { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTDecompressionResolutionOptions

```
public class VTDecompressionResolutionOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public VTDecompressionResolutionOptions ();
	public VTDecompressionResolutionOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public float? Height { get; set; }
	public float? Width { get; set; }
}
```

### New Type MonoTouch.VideoToolbox.VTDecompressionSession

```
public class VTDecompressionSession : MonoTouch.VideoToolbox.VTSession, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTDecompressionSession (IntPtr handle);
	// methods
	protected override void ~VTDecompressionSession ();
	public VTStatus CanAcceptFormatDescriptor (MonoTouch.CoreMedia.CMFormatDescription newDescriptor);
	public VTStatus CopyBlackPixelBuffer (out MonoTouch.CoreVideo.CVPixelBuffer pixelBuffer);
	public static VTDecompressionSession Create (VTDecompressionSession.VTDecompressionOutputCallback outputCallback, MonoTouch.CoreMedia.CMVideoFormatDescription formatDescription, VTVideoDecoderSpecification decoderSpecification, MonoTouch.Foundation.NSDictionary destinationImageBufferAttributes);
	public VTStatus DecodeFrame (MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, VTDecodeFrameFlags decodeFlags, IntPtr sourceFrame, out VTDecodeInfoFlags infoFlags);
	protected override void Dispose (bool disposing);
	public void Dispose ();
	public VTStatus FinishDelayedFrames ();
	public VTStatus SetDecompressionProperties (VTDecompressionProperties options);
	public VTStatus WaitForAsynchronousFrames ();

	// inner types
	public sealed delegate VTDecompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public VTDecompressionSession (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, MonoTouch.CoreVideo.CVImageBuffer buffer, MonoTouch.CoreMedia.CMTime presentationTimeStamp, MonoTouch.CoreMedia.CMTime presentationDuration, System.AsyncCallback callback, object object);
		public virtual void EndInvoke (System.IAsyncResult result);
		public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, MonoTouch.CoreVideo.CVImageBuffer buffer, MonoTouch.CoreMedia.CMTime presentationTimeStamp, MonoTouch.CoreMedia.CMTime presentationDuration);
	}
}
```

### New Type MonoTouch.VideoToolbox.VTDeinterlaceMode

```
[Serializable]
public enum VTDeinterlaceMode {
	Temporal = 2,
	Unset = 0,
	VerticalFilter = 1,
}
```

### New Type MonoTouch.VideoToolbox.VTEncodeFrameOptionKey

```
public static class VTEncodeFrameOptionKey {
	// properties
	public static MonoTouch.Foundation.NSString ForceKeyFrame { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTEncodeFrameOptions

```
public class VTEncodeFrameOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public VTEncodeFrameOptions ();
	public VTEncodeFrameOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public bool? ForceKeyFrame { get; set; }
}
```

### New Type MonoTouch.VideoToolbox.VTEncodeInfoFlags

```
[Serializable]
[Flags]
public enum VTEncodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
}
```

### New Type MonoTouch.VideoToolbox.VTFieldCount

```
[Serializable]
public enum VTFieldCount {
	Interlaced = 2,
	Progressive = 1,
}
```

### New Type MonoTouch.VideoToolbox.VTFieldDetail

```
[Serializable]
public enum VTFieldDetail {
	SpatialFirstLineEarly = 3,
	SpatialFirstLineLate = 4,
	TemporalBottomFirst = 2,
	TemporalTopFirst = 1,
	Unset = 0,
}
```

### New Type MonoTouch.VideoToolbox.VTFieldMode

```
[Serializable]
public enum VTFieldMode {
	BothFields = 1,
	BottomFieldOnly = 3,
	DeinterlaceFields = 5,
	SingleField = 4,
	TopFieldOnly = 2,
	Unset = 0,
}
```

### New Type MonoTouch.VideoToolbox.VTFrameSilo

```
public class VTFrameSilo : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTFrameSilo (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTFrameSilo ();
	public VTStatus AddSampleBuffer (MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer);
	public static VTFrameSilo Create (MonoTouch.Foundation.NSUrl fileUrl, MonoTouch.CoreMedia.CMTimeRange? timeRange);
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	public VTStatus ForEach (System.Func<MonoTouch.CoreMedia.CMSampleBuffer,MonoTouch.VideoToolbox.VTStatus> callback, MonoTouch.CoreMedia.CMTimeRange? range);
	public VTStatus GetProgressOfCurrentPass (out float progress);
	public VTStatus SetTimeRangesForNextPass (MonoTouch.CoreMedia.CMTimeRange[] ranges);
}
```

### New Type MonoTouch.VideoToolbox.VTH264EntropyMode

```
[Serializable]
public enum VTH264EntropyMode {
	Cabac = 2,
	Cavlc = 1,
	Unset = 0,
}
```

### New Type MonoTouch.VideoToolbox.VTH264EntropyModeKeys

```
public static class VTH264EntropyModeKeys {
	// properties
	public static MonoTouch.Foundation.NSString CABAC { get; }
	public static MonoTouch.Foundation.NSString CAVLC { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTMultiPassStorage

```
public class VTMultiPassStorage : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTMultiPassStorage (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTMultiPassStorage ();
	public VTStatus Close ();
	public static VTMultiPassStorage Create (VTMultiPassStorageCreationOptions options, MonoTouch.Foundation.NSUrl fileUrl, MonoTouch.CoreMedia.CMTimeRange? timeRange);
	public static VTMultiPassStorage Create (MonoTouch.Foundation.NSUrl fileUrl, MonoTouch.CoreMedia.CMTimeRange? timeRange, MonoTouch.Foundation.NSDictionary options);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
```

### New Type MonoTouch.VideoToolbox.VTMultiPassStorageCreationOptionKeys

```
public static class VTMultiPassStorageCreationOptionKeys {
	// properties
	public static MonoTouch.Foundation.NSString DoNotDelete { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTMultiPassStorageCreationOptions

```
public class VTMultiPassStorageCreationOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public VTMultiPassStorageCreationOptions ();
	public VTMultiPassStorageCreationOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public bool? DoNotDelete { get; set; }
}
```

### New Type MonoTouch.VideoToolbox.VTOnlyTheseFrames

```
[Serializable]
public enum VTOnlyTheseFrames {
	AllFrames = 1,
	IFrames = 3,
	KeyFrames = 4,
	NonDroppableFrames = 2,
	Unset = 0,
}
```

### New Type MonoTouch.VideoToolbox.VTProfileLevel

```
[Serializable]
public enum VTProfileLevel {
	H263Profile0Level10 = 46,
	H263Profile0Level45 = 47,
	H263Profile3Level45 = 48,
	H264Baseline13 = 1,
	H264Baseline30 = 2,
	H264Baseline31 = 3,
	H264Baseline32 = 4,
	H264Baseline40 = 5,
	H264Baseline41 = 6,
	H264Baseline42 = 7,
	H264Baseline50 = 8,
	H264Baseline51 = 9,
	H264Baseline52 = 10,
	H264BaselineAutoLevel = 11,
	H264Extended50 = 22,
	H264ExtendedAutoLevel = 23,
	H264High30 = 24,
	H264High31 = 25,
	H264High32 = 26,
	H264High40 = 27,
	H264High41 = 28,
	H264High42 = 29,
	H264High50 = 30,
	H264High51 = 31,
	H264High52 = 32,
	H264HighAutoLevel = 33,
	H264Main30 = 12,
	H264Main31 = 13,
	H264Main32 = 14,
	H264Main40 = 15,
	H264Main41 = 16,
	H264Main42 = 17,
	H264Main50 = 18,
	H264Main51 = 19,
	H264Main52 = 20,
	H264MainAutoLevel = 21,
	MP4VAdvancedSimpleL0 = 41,
	MP4VAdvancedSimpleL1 = 42,
	MP4VAdvancedSimpleL2 = 43,
	MP4VAdvancedSimpleL3 = 44,
	MP4VAdvancedSimpleL4 = 45,
	MP4VMainL2 = 38,
	MP4VMainL3 = 39,
	MP4VMainL4 = 40,
	MP4VSimpleL0 = 34,
	MP4VSimpleL1 = 35,
	MP4VSimpleL2 = 36,
	MP4VSimpleL3 = 37,
	Unset = 0,
}
```

### New Type MonoTouch.VideoToolbox.VTProfileLevelKeys

```
public static class VTProfileLevelKeys {
	// properties
	public static MonoTouch.Foundation.NSString H263_Profile0_Level10 { get; }
	public static MonoTouch.Foundation.NSString H263_Profile0_Level45 { get; }
	public static MonoTouch.Foundation.NSString H263_Profile3_Level45 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_1_3 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_3_0 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_3_1 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_3_2 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_4_0 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_4_1 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_4_2 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_5_0 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_5_1 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_5_2 { get; }
	public static MonoTouch.Foundation.NSString H264_Baseline_AutoLevel { get; }
	public static MonoTouch.Foundation.NSString H264_Extended_5_0 { get; }
	public static MonoTouch.Foundation.NSString H264_Extended_AutoLevel { get; }
	public static MonoTouch.Foundation.NSString H264_High_3_0 { get; }
	public static MonoTouch.Foundation.NSString H264_High_3_1 { get; }
	public static MonoTouch.Foundation.NSString H264_High_3_2 { get; }
	public static MonoTouch.Foundation.NSString H264_High_4_0 { get; }
	public static MonoTouch.Foundation.NSString H264_High_4_1 { get; }
	public static MonoTouch.Foundation.NSString H264_High_4_2 { get; }
	public static MonoTouch.Foundation.NSString H264_High_5_0 { get; }
	public static MonoTouch.Foundation.NSString H264_High_5_1 { get; }
	public static MonoTouch.Foundation.NSString H264_High_5_2 { get; }
	public static MonoTouch.Foundation.NSString H264_High_AutoLevel { get; }
	public static MonoTouch.Foundation.NSString H264_Main_3_0 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_3_1 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_3_2 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_4_0 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_4_1 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_4_2 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_5_0 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_5_1 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_5_2 { get; }
	public static MonoTouch.Foundation.NSString H264_Main_AutoLevel { get; }
	public static MonoTouch.Foundation.NSString MP4V_AdvancedSimple_L0 { get; }
	public static MonoTouch.Foundation.NSString MP4V_AdvancedSimple_L1 { get; }
	public static MonoTouch.Foundation.NSString MP4V_AdvancedSimple_L2 { get; }
	public static MonoTouch.Foundation.NSString MP4V_AdvancedSimple_L3 { get; }
	public static MonoTouch.Foundation.NSString MP4V_AdvancedSimple_L4 { get; }
	public static MonoTouch.Foundation.NSString MP4V_Main_L2 { get; }
	public static MonoTouch.Foundation.NSString MP4V_Main_L3 { get; }
	public static MonoTouch.Foundation.NSString MP4V_Main_L4 { get; }
	public static MonoTouch.Foundation.NSString MP4V_Simple_L0 { get; }
	public static MonoTouch.Foundation.NSString MP4V_Simple_L1 { get; }
	public static MonoTouch.Foundation.NSString MP4V_Simple_L2 { get; }
	public static MonoTouch.Foundation.NSString MP4V_Simple_L3 { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTPropertyKeys

```
public static class VTPropertyKeys {
	// properties
	public static MonoTouch.Foundation.NSString DocumentationKey { get; }
	public static MonoTouch.Foundation.NSString ReadWriteStatus { get; }
	public static MonoTouch.Foundation.NSString ShouldBeSerialized { get; }
	public static MonoTouch.Foundation.NSString SupportedValueListKey { get; }
	public static MonoTouch.Foundation.NSString SupportedValueMaximumKey { get; }
	public static MonoTouch.Foundation.NSString SupportedValueMinimumKey { get; }
	public static MonoTouch.Foundation.NSString Type { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTPropertyOptions

```
public class VTPropertyOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public VTPropertyOptions ();
	public VTPropertyOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public MonoTouch.Foundation.NSString Documentation { get; set; }
	public VTReadWriteStatus ReadWriteStatus { get; set; }
	public bool? ShouldBeSerialized { get; set; }
	public MonoTouch.Foundation.NSNumber[] SupportedValueList { get; set; }
	public MonoTouch.Foundation.NSNumber SupportedValueMaximum { get; set; }
	public MonoTouch.Foundation.NSNumber SupportedValueMinimum { get; set; }
	public VTPropertyType Type { get; set; }
}
```

### New Type MonoTouch.VideoToolbox.VTPropertyReadWriteStatusKeys

```
public static class VTPropertyReadWriteStatusKeys {
	// properties
	public static MonoTouch.Foundation.NSString ReadOnly { get; }
	public static MonoTouch.Foundation.NSString ReadWrite { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTPropertyType

```
[Serializable]
public enum VTPropertyType {
	Boolean = 2,
	Enumeration = 1,
	Number = 3,
	Unset = 0,
}
```

### New Type MonoTouch.VideoToolbox.VTPropertyTypeKeys

```
public static class VTPropertyTypeKeys {
	// properties
	public static MonoTouch.Foundation.NSString Boolean { get; }
	public static MonoTouch.Foundation.NSString Enumeration { get; }
	public static MonoTouch.Foundation.NSString Number { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTReadWriteStatus

```
[Serializable]
public enum VTReadWriteStatus {
	ReadOnly = 1,
	ReadWrite = 2,
	Unset = 0,
}
```

### New Type MonoTouch.VideoToolbox.VTSession

```
public class VTSession : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTSession (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTSession ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public VTPropertyOptions GetProperties ();
	public MonoTouch.Foundation.NSObject GetProperty (MonoTouch.Foundation.NSString propertyKey);
	public MonoTouch.Foundation.NSDictionary GetSerializableProperties ();
	public MonoTouch.Foundation.NSDictionary GetSupportedProperties ();
	public VTStatus SetProperties (VTPropertyOptions options);
	public VTStatus SetProperty (MonoTouch.Foundation.NSString propertyKey, MonoTouch.Foundation.NSObject value);
}
```

### New Type MonoTouch.VideoToolbox.VTStatus

```
[Serializable]
public enum VTStatus {
	AllocationFailed = -12904,
	ColorCorrectionPixelTransferFailed = -12212,
	ColorSyncTransformConvertFailed = -12919,
	CouldNotCreateColorCorrectionData = -12918,
	CouldNotCreateInstance = -12907,
	CouldNotFindTemporalFilter = -12217,
	CouldNotFindVideoDecoder = -12906,
	CouldNotFindVideoEncoder = -12908,
	FormatDescriptionChangeNotSupported = -12916,
	FrameSiloInvalidTimeRange = -12216,
	FrameSiloInvalidTimeStamp = -12215,
	ImageRotationNotSupported = -12914,
	InsufficientSourceColorData = -12917,
	InvalidSession = -12903,
	MultiPassStorageIdentifierMismatch = -12913,
	MultiPassStorageInvalid = -12214,
	Ok = 0,
	Parameter = -12902,
	PixelTransferNotPermitted = -12218,
	PixelTransferNotSupported = -12905,
	PropertyNotSupported = -12900,
	PropertyReadOnly = -12901,
	VideoDecoderAuthorization = -12210,
	VideoDecoderBadData = -12909,
	VideoDecoderMalfunction = -12911,
	VideoDecoderNotAvailableNow = -12913,
	VideoDecoderUnsupportedDataFormat = -12910,
	VideoEncoderAuthorization = -12211,
	VideoEncoderMalfunction = -12912,
	VideoEncoderNotAvailableNow = -12915,
}
```

### New Type MonoTouch.VideoToolbox.VTTransferFunction

```
[Serializable]
public enum VTTransferFunction {
	ItuR7092 = 1,
	Smpte240M1955 = 2,
	Unset = 0,
	UseGamma = 3,
}
```

### New Type MonoTouch.VideoToolbox.VTVideoDecoderSpecification

```
public class VTVideoDecoderSpecification : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public VTVideoDecoderSpecification ();
	public VTVideoDecoderSpecification (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public bool? EnableHardwareAcceleratedVideoDecoder { get; set; }
	public bool? RequireHardwareAcceleratedVideoDecoder { get; set; }
}
```

### New Type MonoTouch.VideoToolbox.VTVideoDecoderSpecificationKeys

```
public static class VTVideoDecoderSpecificationKeys {
	// properties
	public static MonoTouch.Foundation.NSString EnableHardwareAcceleratedVideoDecoder { get; }
	public static MonoTouch.Foundation.NSString RequireHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTVideoEncoder

```
public class VTVideoEncoder {
	// properties
	public string CodecName { get; }
	public int CodecType { get; }
	public string DisplayName { get; }
	public string EncoderId { get; }
	public string EncoderName { get; }
	// methods
	public static VTVideoEncoder[] GetEncoderList ();
}
```

### New Type MonoTouch.VideoToolbox.VTVideoEncoderSpecification

```
public class VTVideoEncoderSpecification : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public VTVideoEncoderSpecification ();
	public VTVideoEncoderSpecification (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public string EncoderID { get; set; }
}
```

### New Type MonoTouch.VideoToolbox.VTVideoEncoderSpecificationKeys

```
public static class VTVideoEncoderSpecificationKeys {
	// properties
	public static MonoTouch.Foundation.NSString EncoderID { get; }
}
```

### New Type MonoTouch.VideoToolbox.VTYCbCrMatrix

```
[Serializable]
public enum VTYCbCrMatrix {
	ItuR6014 = 2,
	ItuR7092 = 1,
	Smpte240M1955 = 3,
	Unset = 0,
}
```

   


 <hr>

<h1 id='compat/MonoTouch.Dialog-1'>MonoTouch.Dialog-1.dll</h1>

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.ActivityElement

Removed interface:

```
IElementSizing
```

Added property:

```
protected override MonoTouch.Foundation.NSString CellKey { get; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public override MonoTouch.UIKit.UITableViewCell GetCell (MonoTouch.UIKit.UITableView tv);
```

### Type Changed: MonoTouch.Dialog.DateTimeElement

Added field:

```
public int MinuteInterval;
```

### Type Changed: MonoTouch.Dialog.DialogViewController

Added event:

```
public event System.EventHandler ViewAppearing;
```

### Type Changed: MonoTouch.Dialog.EntryElement

Added properties:

```
public bool AlignEntryWithAllSections { get; set; }
	public bool EnablesReturnKeyAutomatically { get; set; }
	public bool NotifyChangedOnKeyStroke { get; set; }
```

### Type Changed: MonoTouch.Dialog.FloatElement

Added constructor:

```
public FloatElement (float value);
```

### Type Changed: MonoTouch.Dialog.MessageElement

Added method:

```
public override bool Matches (string text);
```

### Type Changed: MonoTouch.Dialog.UIViewElement

Added constructor:

```
public UIViewElement (string caption, MonoTouch.UIKit.UIView view, bool transparent, MonoTouch.UIKit.UIEdgeInsets insets);
```

Added field:

```
public MonoTouch.UIKit.UIView ContainerView;
```

Added property:

```
public MonoTouch.UIKit.UIEdgeInsets Insets { get; set; }
```

   


 <hr>

<h1 id='compat/MonoTouch.NUnitLite'>MonoTouch.NUnitLite.dll</h1>

## Namespace MonoTouch.NUnit.UI

### Type Changed: MonoTouch.NUnit.UI.TouchRunner

Added method:

```
public void Add (System.Reflection.Assembly assembly, System.Collections.Generic.IList<string> fixtures);
```

   


 <hr>

<h1 id='compat/OpenTK-1.0'>OpenTK-1.0.dll</h1>

## Namespace OpenTK.Graphics.ES20

### Type Changed: OpenTK.Graphics.ES20.GL

Added methods:

```
public static void UniformMatrix2 (int location, bool transpose, ref OpenTK.Matrix2 matrix);
	public static void UniformMatrix3 (int location, bool transpose, ref OpenTK.Matrix3 matrix);
```

## Namespace OpenTK.Graphics.ES30

### Type Changed: OpenTK.Graphics.ES30.GL

Added methods:

```
public static void UniformMatrix2 (int location, bool transpose, ref OpenTK.Matrix2 matrix);
	public static void UniformMatrix3 (int location, bool transpose, ref OpenTK.Matrix3 matrix);
```

   


 <hr>

<h1 id='reference/MonoTouch.Dialog-1'>MonoTouch.Dialog-1.dll</h1>

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.ActivityElement

Removed interface:

```
IElementSizing
```

Added property:

```
protected override Foundation.NSString CellKey { get; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public override UIKit.UITableViewCell GetCell (UIKit.UITableView tv);
```

### Type Changed: MonoTouch.Dialog.DateTimeElement

Added field:

```
public int MinuteInterval;
```

### Type Changed: MonoTouch.Dialog.DialogViewController

Added event:

```
public event System.EventHandler ViewAppearing;
```

### Type Changed: MonoTouch.Dialog.EntryElement

Added properties:

```
public bool AlignEntryWithAllSections { get; set; }
	public bool EnablesReturnKeyAutomatically { get; set; }
	public bool NotifyChangedOnKeyStroke { get; set; }
```

### Type Changed: MonoTouch.Dialog.FloatElement

Added constructor:

```
public FloatElement (float value);
```

### Type Changed: MonoTouch.Dialog.MessageElement

Added method:

```
public override bool Matches (string text);
```

### Type Changed: MonoTouch.Dialog.UIViewElement

Added constructor:

```
public UIViewElement (string caption, UIKit.UIView view, bool transparent, UIKit.UIEdgeInsets insets);
```

Added field:

```
public UIKit.UIView ContainerView;
```

Added property:

```
public UIKit.UIEdgeInsets Insets { get; set; }
```

   


 <hr>

<h1 id='reference/MonoTouch.NUnitLite'>MonoTouch.NUnitLite.dll</h1>

## Namespace MonoTouch.NUnit.UI

### Type Changed: MonoTouch.NUnit.UI.TouchRunner

Added method:

```
public void Add (System.Reflection.Assembly assembly, System.Collections.Generic.IList<string> fixtures);
```

   


 <hr>

<h1 id='reference/OpenTK-1.0'>OpenTK-1.0.dll</h1>

## Namespace OpenTK.Graphics.ES20

### Type Changed: OpenTK.Graphics.ES20.GL

Added methods:

```
public static void UniformMatrix2 (int location, bool transpose, ref OpenTK.Matrix2 matrix);
	public static void UniformMatrix3 (int location, bool transpose, ref OpenTK.Matrix3 matrix);
```

## Namespace OpenTK.Graphics.ES30

### Type Changed: OpenTK.Graphics.ES30.GL

Added methods:

```
public static void UniformMatrix2 (int location, bool transpose, ref OpenTK.Matrix2 matrix);
	public static void UniformMatrix3 (int location, bool transpose, ref OpenTK.Matrix3 matrix);
```

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace AddressBookUI

### Type Changed: AddressBookUI.ABPeoplePickerNavigationController

Modified methods:

```
public ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T T : ABPeoplePickerNavigationController> (UIKit.UITraitCollection traits)
	public ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T T : ABPeoplePickerNavigationController> ()
	public ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T T : ABPeoplePickerNavigationController> (UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace AudioToolbox

### Type Changed: AudioToolbox.AudioConverterError

Added value:

```
AudioFormatUnsupported = 560226676,
```

## Namespace AVFoundation

### Type Changed: AVFoundation.AVCaptureConnection

Obsoleted properties:

```
[Obsolete ("Use AvailableAudioChannels property instead."]
	public virtual AVCaptureAudioChannel AudioChannels { get; }
```

Added property:

```
public virtual AVCaptureAudioChannel[] AvailableAudioChannels { get; }
```

## Namespace CoreAnimation

### Type Changed: CoreAnimation.CABasicAnimation

Added methods:

```
public T GetByAs<T> ();
	public T GetFromAs<T> ();
	public T GetToAs<T> ();
	public void SetBy (ObjCRuntime.INativeObject value);
	public void SetFrom (ObjCRuntime.INativeObject value);
	public void SetTo (ObjCRuntime.INativeObject value);
```

### Type Changed: CoreAnimation.CAKeyFrameAnimation

Added methods:

```
public T[] GetValuesAs<T> ();
	public void SetValues (ObjCRuntime.INativeObject[] value);
```

### Type Changed: CoreAnimation.CALayer

Added methods:

```
public T GetContentsAs<T> ();
	public void SetContents (Foundation.NSObject value);
```

## Namespace CoreAudioKit

### Type Changed: CoreAudioKit.CAInterAppAudioSwitcherView

Modified methods:

```
public CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T T : CAInterAppAudioSwitcherView> ()
	public CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T T : CAInterAppAudioSwitcherView> (UIKit.UITraitCollection traits)
	public CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T T : CAInterAppAudioSwitcherView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: CoreAudioKit.CAInterAppAudioTransportView

Modified methods:

```
public CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T T : CAInterAppAudioTransportView> (UIKit.UITraitCollection traits)
	public CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T T : CAInterAppAudioTransportView> (UIKit.UITraitCollection traits, System.Type[] containers)
	public CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T T : CAInterAppAudioTransportView> ()
```

## Namespace CoreBluetooth

### Type Changed: CoreBluetooth.CBPeer

Added property:

```
public virtual CBUUID UUID { get; }
```

### Type Changed: CoreBluetooth.CBUUID

Added methods:

```
public override bool Equals (object obj);
	public override int GetHashCode ();
```

## Namespace CoreFoundation

### Type Changed: CoreFoundation.CFStream

Added method:

```
public static CoreServices.CFHTTPStream CreateForStreamedHTTPRequest (CoreServices.CFHTTPMessage request, Foundation.NSInputStream body);
```

### Type Changed: CoreFoundation.DispatchQueue

Added constructor:

```
public DispatchQueue (string label, bool concurrent);
```

Added methods:

```
public void DispatchBarrierAsync (System.Action action);
	public void Submit (System.Action<int> action, long times);
```

### New Type CoreFoundation.DispatchSource

```
public class DispatchSource : CoreFoundation.DispatchObject, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public bool IsCanceled { get; }
	// methods
	public void Cancel ();
	protected override void Dispose (bool disposing);
	public void Resume ();
	public void SetCancelHandler (System.Action handler);
	public void SetEventHandler (System.Action handler);
	public void SetRegistrationHandler (System.Action handler);

	// inner types
	public class Data : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// properties
		public IntPtr PendingData { get; }
		// methods
		public void MergeData (IntPtr value);
	}
	public class DataAdd : CoreFoundation.DispatchSource+Data, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
	}
	public class DataOr : CoreFoundation.DispatchSource+Data, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
	}
	public class Mach : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// properties
		public int MachPort { get; }
	}
	public class MachSend : CoreFoundation.DispatchSource+Mach, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int machPort, bool sendDead, DispatchQueue queue);
		// properties
		public bool SendRightsDestroyed { get; }
	}
	public class MachReceive : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int machPort, DispatchQueue queue);
	}
	public class MemoryPressure : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (MemoryPressureFlags monitorFlags, DispatchQueue queue);
		// properties
		public MemoryPressureFlags PressureFlags { get; }
	}
	public class ProcessMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int processId, ProcessMonitorFlags monitorKind, DispatchQueue queue);
		// properties
		public ProcessMonitorFlags MonitorFlags { get; }
		public int ProcessId { get; }
	}
	public class ReadMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, DispatchQueue queue);
		// properties
		public int BytesAvailable { get; }
		public int FileDescriptor { get; }
	}
	public class SignalMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int signalNumber, DispatchQueue queue);
		// properties
		public int SignalNumber { get; }
		public int SignalsDelivered { get; }
	}
	public class Timer : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
		// properties
		public int TimerFiredCount { get; }
		// methods
		public void SetTimer (DispatchTime time, long nanosecondInterval, long nanosecondLeeway);
	}
	public class VnodeMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, VnodeMonitorKind vnodeKind, DispatchQueue queue);
		public DispatchSource (string path, VnodeMonitorKind vnodeKind, DispatchQueue queue);
		// properties
		public int FileDescriptor { get; }
		public VnodeMonitorKind ObservedEvents { get; }
		// methods
		protected override void Dispose (bool disposing);
	}
	public class WriteMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, DispatchQueue queue);
		// properties
		public int BufferSpaceAvailable { get; }
		public int FileDescriptor { get; }
	}
}
```

### New Type CoreFoundation.MemoryPressureFlags

```
[Serializable]
[Flags]
public enum MemoryPressureFlags {
	Critical = 4,
	Normal = 1,
	Warn = 2,
}
```

### New Type CoreFoundation.ProcessMonitorFlags

```
[Serializable]
[Flags]
public enum ProcessMonitorFlags {
	Exec = 536870912,
	Exit = 2147483648,
	Fork = 1073741824,
	Signal = 134217728,
}
```

### New Type CoreFoundation.VnodeMonitorKind

```
[Serializable]
[Flags]
public enum VnodeMonitorKind {
	Attrib = 8,
	Delete = 1,
	Extend = 4,
	Link = 16,
	Rename = 32,
	Revoke = 64,
	Write = 2,
}
```

## Namespace CoreGraphics

### Type Changed: CoreGraphics.CGBitmapContext

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: CoreGraphics.CGGradientDrawingOptions

Added value:

```
None = 0,
```

### Type Changed: CoreGraphics.CGPoint

Added constructor:

```
public CGPoint (double x, double y);
```

### Type Changed: CoreGraphics.CGRect

Added constructor:

```
public CGRect (double x, double y, double width, double height);
```

### Type Changed: CoreGraphics.CGSize

Added constructor:

```
public CGSize (double width, double height);
```

## Namespace CoreMedia

### Type Changed: CoreMedia.CMTimeRange

Added fields:

```
public static CMTimeRange Invalid;
	public static CMTimeRange Zero;
```

### New Type CoreMedia.CMPixelFormat

```
[Serializable]
public enum CMPixelFormat {
	AlphaRedGreenBlue32bits = 32,
	BigEndian555_16bits = 16,
	BigEndian565_16bits = 1110783541,
	BlueGreenRedAlpha32bits = 1111970369,
	IndexedGrayWhiteIsZero_8bits = 40,
	LittleEndian555_16bits = 1278555445,
	LittleEndian5551_16bits = 892679473,
	LittleEndian565_16bits = 1278555701,
	RedGreenBlue24bits = 24,
	YpCbCr422_10bits = 1983000880,
	YpCbCr422_16bits = 1983000886,
	YpCbCr422_8bits = 846624121,
	YpCbCr422yuvs_8bits = 2037741171,
	YpCbCr444_10bits = 1983131952,
	YpCbCr444_8bits = 1983066168,
	YpCbCrA4444_8bits = 1983131704,
}
```

## Namespace CoreText

### Type Changed: CoreText.CTFontManager

Obsoleted methods:

```
[Obsolete ("API not available on iOS, it will always return false"]
	public static bool IsFontSupported (Foundation.NSUrl url);
```

## Namespace CoreVideo

### Type Changed: CoreVideo.CVImageBuffer

Added properties:

```
public static Foundation.NSString ColorPrimaries_EBU_3213 { get; }
	public static Foundation.NSString ColorPrimaries_ITU_R_709_2 { get; }
	public static Foundation.NSString ColorPrimaries_P22 { get; }
	public static Foundation.NSString ColorPrimaries_SMPTE_C { get; }
	public static Foundation.NSString ColorPrimariesKey { get; }
```

### Type Changed: CoreVideo.CVPixelBufferPool

Added properties:

```
public static Foundation.NSString ColorPrimaries_EBU_3213 { get; }
	public static Foundation.NSString ColorPrimaries_ITU_R_709_2 { get; }
	public static Foundation.NSString ColorPrimaries_P22 { get; }
	public static Foundation.NSString ColorPrimaries_SMPTE_C { get; }
	public static Foundation.NSString ColorPrimariesKey { get; }
```

## Namespace EventKitUI

### Type Changed: EventKitUI.EKEventEditViewController

Modified methods:

```
public EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T T : EKEventEditViewController> ()
	public EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T T : EKEventEditViewController> (UIKit.UITraitCollection traits)
	public EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T T : EKEventEditViewController> (UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace Foundation

### Type Changed: Foundation.NSArray

Added method:

```
public static T[] FromArrayNative<T> (NSArray weakArray);
```

### Type Changed: Foundation.NSDirectoryEnumerator

Added interfaces:

```
System.Collections.Generic.IEnumerator<NSString>
	System.Collections.Generic.IEnumerator<string>
	System.Collections.IEnumerator
```

### Type Changed: Foundation.NSDistributedNotificationCenter

Obsoleted methods:

```
[Obsolete ("This is not available in iOS"]
	public void AddObserver (NSObject observer, ObjCRuntime.Selector aSelector, string aName, string anObject);
	[Obsolete ("This is not available in iOS"]
	public void RemoveObserver (NSObject observer, string aName, string anObject);
```

### Type Changed: Foundation.NSFileManager

Added method:

```
public NSUrl[] GetMountedVolumes (NSString[] properties, NSVolumeEnumerationOptions options);
```

### Type Changed: Foundation.NSStream

Added methods:

```
public static void CreateBoundPair (out NSInputStream readStream, out NSOutputStream writeStream, nint bufferSize);
	public static void CreatePairWithPeerSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, out NSInputStream readStream, out NSOutputStream writeStream);
	public static void CreatePairWithSocket (CoreFoundation.CFSocket socket, out NSInputStream readStream, out NSOutputStream writeStream);
	public static void CreatePairWithSocketToHost (System.Net.IPEndPoint endpoint, out NSInputStream readStream, out NSOutputStream writeStream);
```

### Type Changed: Foundation.NSUrl

Added property:

```
public virtual string PathExtension { get; }
```

### Type Changed: Foundation.PreserveAttribute

Added constructor:

```
public PreserveAttribute (System.Type type);
```

### Type Changed: Foundation.ProtocolAttribute

Added property:

```
public bool IsInformal { get; set; }
```

### New Type Foundation.NSTextChecking

```
public static class NSTextChecking {
	// properties
	public static NSString AirlineKey { get; }
	public static NSString CityKey { get; }
	public static NSString CountryKey { get; }
	public static NSString FlightKey { get; }
	public static NSString JobTitleKey { get; }
	public static NSString NameKey { get; }
	public static NSString OrganizationKey { get; }
	public static NSString PhoneKey { get; }
	public static NSString StateKey { get; }
	public static NSString StreetKey { get; }
	public static NSString ZipKey { get; }
}
```

### New Type Foundation.NSTextCheckingAddressComponents

```
public class NSTextCheckingAddressComponents : Foundation.DictionaryContainer {
	// constructors
	public NSTextCheckingAddressComponents ();
	public NSTextCheckingAddressComponents (NSDictionary dictionary);
	// properties
	public string City { get; }
	public string Country { get; }
	public string JobTitle { get; }
	public string Name { get; }
	public string Organization { get; }
	public string Phone { get; }
	public string State { get; }
	public string Street { get; }
	public string ZIP { get; }
}
```

### New Type Foundation.NSTextCheckingResult

```
public class NSTextCheckingResult : Foundation.NSObject, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<NSObject>, INSObjectProtocol {
	// constructors
	public NSTextCheckingResult (NSCoder coder);
	protected NSTextCheckingResult (NSObjectFlag t);
	protected NSTextCheckingResult (IntPtr handle);
	// properties
	public NSTextCheckingAddressComponents AddressComponents { get; }
	public virtual string[] AlternativeStrings { get; }
	public override IntPtr ClassHandle { get; }
	public NSTextCheckingTransitComponents Components { get; }
	public virtual NSDate Date { get; }
	public virtual string[] GrammarDetails { get; }
	public virtual uint NumberOfRanges { get; }
	public virtual NSOrthography Orthography { get; }
	public virtual string PhoneNumber { get; }
	public virtual NSRange Range { get; }
	public virtual string ReplacementString { get; }
	public virtual NSTextCheckingType ResultType { get; }
	public virtual double TimeInterval { get; }
	public virtual NSTimeZone TimeZone { get; }
	public virtual NSUrl Url { get; }
	public virtual NSDictionary WeakAddressComponents { get; }
	public virtual NSDictionary WeakComponents { get; }
	// methods
	public static NSTextCheckingResult AddressCheckingResult (NSRange range, NSDictionary components);
	public static NSTextCheckingResult AddressCheckingResult (NSRange range, NSTextCheckingAddressComponents components);
	public virtual NSObject Copy (NSZone zone);
	public static NSTextCheckingResult CorrectionCheckingResult (NSRange range, string replacementString, string[] alternativeStrings);
	public static NSTextCheckingResult CorrectionCheckingResult (NSRange range, string replacementString);
	public static NSTextCheckingResult DashCheckingResult (NSRange range, string replacementString);
	public static NSTextCheckingResult DateCheckingResult (NSRange range, NSDate date);
	public static NSTextCheckingResult DateCheckingResult (NSRange range, NSDate date, NSTimeZone timezone, double duration);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (NSCoder encoder);
	public static NSTextCheckingResult GrammarCheckingResult (NSRange range, string[] details);
	public static NSTextCheckingResult LinkCheckingResult (NSRange range, NSUrl url);
	public static NSTextCheckingResult OrthographyCheckingResult (NSRange range, NSOrthography ortography);
	public static NSTextCheckingResult PhoneNumberCheckingResult (NSRange range, string phoneNumber);
	public static NSTextCheckingResult QuoteCheckingResult (NSRange range, NSString replacementString);
	public virtual NSRange RangeAtIndex (uint idx);
	public static NSTextCheckingResult ReplacementCheckingResult (NSRange range, string replacementString);
	public virtual NSTextCheckingResult ResultByAdjustingRanges (nint offset);
	public static NSTextCheckingResult SpellCheckingResult (NSRange range);
	public static NSTextCheckingResult TransitInformationCheckingResult (NSRange range, NSDictionary components);
	public static NSTextCheckingResult TransitInformationCheckingResult (NSRange range, NSTextCheckingTransitComponents components);
}
```

### New Type Foundation.NSTextCheckingTransitComponents

```
public class NSTextCheckingTransitComponents : Foundation.DictionaryContainer {
	// constructors
	public NSTextCheckingTransitComponents ();
	public NSTextCheckingTransitComponents (NSDictionary dictionary);
	// properties
	public string Airline { get; }
	public string Flight { get; }
}
```

### New Type Foundation.NSTextCheckingType

```
[Serializable]
public enum NSTextCheckingType {
	Address = 16,
	Correction = 512,
	Dash = 128,
	Date = 8,
	Grammar = 4,
	Link = 32,
	Orthography = 1,
	PhoneNumber = 2048,
	Quote = 64,
	RegularExpression = 1024,
	Replacement = 256,
	Spelling = 2,
	TransitInformation = 4096,
}
```

### New Type Foundation.NSTextCheckingTypes

```
[Serializable]
public enum NSTextCheckingTypes {
	AllCustomTypes = 18446744069414584320,
	AllSystemTypes = 4294967295,
	AllTypes = 18446744073709551615,
}
```

## Namespace GameKit

### Type Changed: GameKit.GKAchievementViewController

Modified methods:

```
public GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T T : GKAchievementViewController> ()
	public GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T T : GKAchievementViewController> (UIKit.UITraitCollection traits)
	public GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T T : GKAchievementViewController> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: GameKit.GKFriendRequestComposeViewController

Modified methods:

```
public GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T T : GKFriendRequestComposeViewController> (UIKit.UITraitCollection traits)
	public GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T T : GKFriendRequestComposeViewController> ()
	public GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T T : GKFriendRequestComposeViewController> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: GameKit.GKLeaderboardViewController

Modified methods:

```
public GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T T : GKLeaderboardViewController> ()
	public GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T T : GKLeaderboardViewController> (UIKit.UITraitCollection traits)
	public GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T T : GKLeaderboardViewController> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: GameKit.GKTurnBasedMatchmakerViewController

Modified methods:

```
public GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T T : GKTurnBasedMatchmakerViewController> ()
	public GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T T : GKTurnBasedMatchmakerViewController> (UIKit.UITraitCollection traits)
	public GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T T : GKTurnBasedMatchmakerViewController> (UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace GLKit

### Type Changed: GLKit.GLKView

Modified methods:

```
public GLKView.GLKViewAppearance GetAppearance<T T : GLKView> (UIKit.UITraitCollection traits)
	public GLKView.GLKViewAppearance GetAppearance<T T : GLKView> ()
	public GLKView.GLKViewAppearance GetAppearance<T T : GLKView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace HealthKit

### Type Changed: HealthKit.HKAnchoredObjectQuery

Obsoleted constructors:

```
[Obsolete ("Use the overload that takes HKAnchoredObjectResultHandler2 instead"]
	public HKAnchoredObjectQuery (HKSampleType type, Foundation.NSPredicate predicate, uint anchor, uint limit, HKAnchoredObjectResultHandler completion);
```

Added constructor:

```
public HKAnchoredObjectQuery (HKSampleType type, Foundation.NSPredicate predicate, uint anchor, uint limit, HKAnchoredObjectResultHandler2 completion);
```

### Type Changed: HealthKit.HKQuantitySample

Added method:

```
public static HKQuantitySample FromType (HKQuantityType quantityType, HKQuantity quantity, Foundation.NSDate startDate, Foundation.NSDate endDate);
```

### New Type HealthKit.HKAnchoredObjectResultHandler2

```
public sealed delegate HKAnchoredObjectResultHandler2 : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKAnchoredObjectResultHandler2 (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKAnchoredObjectQuery query, HKSample[] results, uint newAnchor, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKAnchoredObjectQuery query, HKSample[] results, uint newAnchor, Foundation.NSError error);
}
```

## Namespace iAd

### Type Changed: iAd.ADBannerView

Modified methods:

```
public ADBannerView.ADBannerViewAppearance GetAppearance<T T : ADBannerView> ()
	public ADBannerView.ADBannerViewAppearance GetAppearance<T T : ADBannerView> (UIKit.UITraitCollection traits)
	public ADBannerView.ADBannerViewAppearance GetAppearance<T T : ADBannerView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MapKit

### Type Changed: MapKit.MKAnnotationView

Modified methods:

```
public MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T T : MKAnnotationView> ()
	public MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T T : MKAnnotationView> (UIKit.UITraitCollection traits)
	public MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T T : MKAnnotationView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MapKit.MKCircleView

Modified methods:

```
public MKCircleView.MKCircleViewAppearance GetAppearance<T T : MKCircleView> ()
	public MKCircleView.MKCircleViewAppearance GetAppearance<T T : MKCircleView> (UIKit.UITraitCollection traits)
	public MKCircleView.MKCircleViewAppearance GetAppearance<T T : MKCircleView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MapKit.MKMapView

Modified methods:

```
public MKMapView.MKMapViewAppearance GetAppearance<T T : MKMapView> ()
	public MKMapView.MKMapViewAppearance GetAppearance<T T : MKMapView> (UIKit.UITraitCollection traits)
	public MKMapView.MKMapViewAppearance GetAppearance<T T : MKMapView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MapKit.MKOverlayPathView

Modified methods:

```
public MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T T : MKOverlayPathView> (UIKit.UITraitCollection traits)
	public MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T T : MKOverlayPathView> (UIKit.UITraitCollection traits, System.Type[] containers)
	public MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T T : MKOverlayPathView> ()
```

### Type Changed: MapKit.MKOverlayView

Modified methods:

```
public MKOverlayView.MKOverlayViewAppearance GetAppearance<T T : MKOverlayView> (UIKit.UITraitCollection traits, System.Type[] containers)
	public MKOverlayView.MKOverlayViewAppearance GetAppearance<T T : MKOverlayView> (UIKit.UITraitCollection traits)
	public MKOverlayView.MKOverlayViewAppearance GetAppearance<T T : MKOverlayView> ()
```

### Type Changed: MapKit.MKPinAnnotationView

Modified methods:

```
public MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T T : MKPinAnnotationView> ()
	public MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T T : MKPinAnnotationView> (UIKit.UITraitCollection traits)
	public MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T T : MKPinAnnotationView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MapKit.MKPointAnnotation

Added property:

```
public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; set; }
```

### Type Changed: MapKit.MKPolygonView

Modified methods:

```
public MKPolygonView.MKPolygonViewAppearance GetAppearance<T T : MKPolygonView> ()
	public MKPolygonView.MKPolygonViewAppearance GetAppearance<T T : MKPolygonView> (UIKit.UITraitCollection traits)
	public MKPolygonView.MKPolygonViewAppearance GetAppearance<T T : MKPolygonView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MapKit.MKPolylineView

Modified methods:

```
public MKPolylineView.MKPolylineViewAppearance GetAppearance<T T : MKPolylineView> ()
	public MKPolylineView.MKPolylineViewAppearance GetAppearance<T T : MKPolylineView> (UIKit.UITraitCollection traits)
	public MKPolylineView.MKPolylineViewAppearance GetAppearance<T T : MKPolylineView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MapKit.MKUserTrackingBarButtonItem

Modified methods:

```
public MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T T : MKUserTrackingBarButtonItem> ()
	public MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T T : MKUserTrackingBarButtonItem> (UIKit.UITraitCollection traits)
	public MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T T : MKUserTrackingBarButtonItem> (UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace MediaPlayer

### Type Changed: MediaPlayer.MPVolumeView

Modified methods:

```
public MPVolumeView.MPVolumeViewAppearance GetAppearance<T T : MPVolumeView> (UIKit.UITraitCollection traits, System.Type[] containers)
	public MPVolumeView.MPVolumeViewAppearance GetAppearance<T T : MPVolumeView> ()
	public MPVolumeView.MPVolumeViewAppearance GetAppearance<T T : MPVolumeView> (UIKit.UITraitCollection traits)
```

## Namespace MessageUI

### Type Changed: MessageUI.MFMailComposeViewController

Modified methods:

```
public MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T T : MFMailComposeViewController> ()
	public MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T T : MFMailComposeViewController> (UIKit.UITraitCollection traits)
	public MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T T : MFMailComposeViewController> (UIKit.UITraitCollection traits, System.Type[] containers)
```

### Type Changed: MessageUI.MFMessageComposeViewController

Modified methods:

```
public MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T T : MFMessageComposeViewController> (UIKit.UITraitCollection traits)
	public MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T T : MFMessageComposeViewController> (UIKit.UITraitCollection traits, System.Type[] containers)
	public MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T T : MFMessageComposeViewController> ()
```

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.9.1" "8.10.0";
```

### Type Changed: ObjCRuntime.Dlfcn

Added method:

```
public static IntPtr dlsym (Dlfcn.RTLD lookupType, string symbol);
```

### Type Changed: ObjCRuntime.Runtime

Added method:

```
public static Foundation.NSObject TryGetNSObject (IntPtr ptr);
```

### New Type ObjCRuntime.CategoryAttribute

```
public class CategoryAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public CategoryAttribute (System.Type type);
	// properties
	public string Name { get; set; }
	public System.Type Type { get; set; }
}
```

### New Type ObjCRuntime.Protocol

```
public class Protocol : INativeObject {
	// constructors
	public Protocol (string name);
	public Protocol (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	public string Name { get; }
	// methods
	public static IntPtr GetHandle (string name);
}
```

## Namespace OpenTK

### Type Changed: OpenTK.Matrix3

Added constructor:

```
public Matrix3 (Matrix4 matrix);
```

## Namespace PassKit

### Type Changed: PassKit.PKPaymentButton

Modified methods:

```
public PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T T : PKPaymentButton> ()
	public PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T T : PKPaymentButton> (UIKit.UITraitCollection traits)
	public PKPaymentButton.PKPaymentButtonAppearance GetAppearance<T T : PKPaymentButton> (UIKit.UITraitCollection traits, System.Type[] containers)
```

## Namespace SceneKit

### Type Changed: SceneKit.SCNGeometry

Obsoleted methods:

```
[Obsolete ("Use the Create(SCNGeometrySource[], SCNGeometryElement[]) method instead, as it has a strongly typed return"]
	public static Foundation.NSObject FromSources (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
```

Added method:

```
public static SCNGeometry Create (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
```

### Type Changed: SceneKit.SCNView

Modified methods:

```
public SCNView.SCNViewAppearance GetAppearance<T T : SCNView> (UIKit.UITraitCollection traits, System.Type[] containers)
	public SCNView.SCNViewAppearance GetAppearance<T T : SCNView> ()
	public SCNView.SCNViewAppearance GetAppearance<T T : SCNView> (UIKit.UITraitCollection traits)
```

## Namespace Security

### Type Changed: Security.SecRecord

Added constructor:

```
public SecRecord ();
```

## Namespace SpriteKit

### Type Changed: SpriteKit.SKView

Modified methods:

```
public SKView.SKViewAppearance GetAppearance<T T : SKView> (UIKit.UITraitCollection traits, System.Type[] containers)
	public SKView.SKViewAppearance GetAppearance<T T : SKView> (UIKit.UITraitCollection traits)
	public SKView.SKViewAppearance GetAppearance<T T : SKView> ()
```

## Namespace UIKit

### Type Changed: UIKit.UIActionSheet

Modified methods:

```
public UIActionSheet.UIActionSheetAppearance GetAppearance<T T : UIActionSheet> (UITraitCollection traits)
	public UIActionSheet.UIActionSheetAppearance GetAppearance<T T : UIActionSheet> ()
	public UIActionSheet.UIActionSheetAppearance GetAppearance<T T : UIActionSheet> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIActivityIndicatorView

Modified methods:

```
public UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T T : UIActivityIndicatorView> (UITraitCollection traits)
	public UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T T : UIActivityIndicatorView> (UITraitCollection traits, System.Type[] containers)
	public UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T T : UIActivityIndicatorView> ()
```

### Type Changed: UIKit.UIAlertView

Modified methods:

```
public UIAlertView.UIAlertViewAppearance GetAppearance<T T : UIAlertView> (UITraitCollection traits)
	public UIAlertView.UIAlertViewAppearance GetAppearance<T T : UIAlertView> (UITraitCollection traits, System.Type[] containers)
	public UIAlertView.UIAlertViewAppearance GetAppearance<T T : UIAlertView> ()
```

### Type Changed: UIKit.UIApplication

Added field:

```
public static bool CheckForEventAndDelegateMismatches;
```

### Type Changed: UIKit.UIBarButtonItem

Modified methods:

```
public UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T T : UIBarButtonItem> ()
	public UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T T : UIBarButtonItem> (UITraitCollection traits)
	public UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T T : UIBarButtonItem> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIBarItem

Modified methods:

```
public UIBarItem.UIBarItemAppearance GetAppearance<T T : UIBarItem> ()
	public UIBarItem.UIBarItemAppearance GetAppearance<T T : UIBarItem> (UITraitCollection traits)
	public UIBarItem.UIBarItemAppearance GetAppearance<T T : UIBarItem> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIButton

Modified methods:

```
public UIButton.UIButtonAppearance GetAppearance<T T : UIButton> ()
	public UIButton.UIButtonAppearance GetAppearance<T T : UIButton> (UITraitCollection traits)
	public UIButton.UIButtonAppearance GetAppearance<T T : UIButton> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UICollectionReusableView

Modified methods:

```
public UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T T : UICollectionReusableView> (UITraitCollection traits, System.Type[] containers)
	public UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T T : UICollectionReusableView> (UITraitCollection traits)
	public UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T T : UICollectionReusableView> ()
```

### Type Changed: UIKit.UICollectionView

Modified methods:

```
public UICollectionView.UICollectionViewAppearance GetAppearance<T T : UICollectionView> (UITraitCollection traits)
	public UICollectionView.UICollectionViewAppearance GetAppearance<T T : UICollectionView> ()
	public UICollectionView.UICollectionViewAppearance GetAppearance<T T : UICollectionView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UICollectionViewCell

Modified methods:

```
public UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T T : UICollectionViewCell> ()
	public UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T T : UICollectionViewCell> (UITraitCollection traits)
	public UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T T : UICollectionViewCell> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIControl

Modified methods:

```
public UIControl.UIControlAppearance GetAppearance<T T : UIControl> (UITraitCollection traits)
	public UIControl.UIControlAppearance GetAppearance<T T : UIControl> ()
	public UIControl.UIControlAppearance GetAppearance<T T : UIControl> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIDatePicker

Modified methods:

```
public UIDatePicker.UIDatePickerAppearance GetAppearance<T T : UIDatePicker> (UITraitCollection traits)
	public UIDatePicker.UIDatePickerAppearance GetAppearance<T T : UIDatePicker> (UITraitCollection traits, System.Type[] containers)
	public UIDatePicker.UIDatePickerAppearance GetAppearance<T T : UIDatePicker> ()
```

### Type Changed: UIKit.UIDocument

Added property:

```
public static Foundation.NSString UserActivityDocumentUrlKey { get; }
```

### Type Changed: UIKit.UIFont

Added methods:

```
public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (UIFont f1, UIFont f2);
	public static bool op_Inequality (UIFont f1, UIFont f2);
```

### Type Changed: UIKit.UIImageView

Modified methods:

```
public UIImageView.UIImageViewAppearance GetAppearance<T T : UIImageView> (UITraitCollection traits)
	public UIImageView.UIImageViewAppearance GetAppearance<T T : UIImageView> (UITraitCollection traits, System.Type[] containers)
	public UIImageView.UIImageViewAppearance GetAppearance<T T : UIImageView> ()
```

### Type Changed: UIKit.UIInputView

Modified methods:

```
public UIInputView.UIInputViewAppearance GetAppearance<T T : UIInputView> ()
	public UIInputView.UIInputViewAppearance GetAppearance<T T : UIInputView> (UITraitCollection traits)
	public UIInputView.UIInputViewAppearance GetAppearance<T T : UIInputView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UILabel

Modified methods:

```
public UILabel.UILabelAppearance GetAppearance<T T : UILabel> ()
	public UILabel.UILabelAppearance GetAppearance<T T : UILabel> (UITraitCollection traits)
	public UILabel.UILabelAppearance GetAppearance<T T : UILabel> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UINavigationBar

Modified methods:

```
public UINavigationBar.UINavigationBarAppearance GetAppearance<T T : UINavigationBar> (UITraitCollection traits, System.Type[] containers)
	public UINavigationBar.UINavigationBarAppearance GetAppearance<T T : UINavigationBar> ()
	public UINavigationBar.UINavigationBarAppearance GetAppearance<T T : UINavigationBar> (UITraitCollection traits)
```

### Type Changed: UIKit.UIPageControl

Modified methods:

```
public UIPageControl.UIPageControlAppearance GetAppearance<T T : UIPageControl> (UITraitCollection traits)
	public UIPageControl.UIPageControlAppearance GetAppearance<T T : UIPageControl> (UITraitCollection traits, System.Type[] containers)
	public UIPageControl.UIPageControlAppearance GetAppearance<T T : UIPageControl> ()
```

### Type Changed: UIKit.UIPickerView

Modified methods:

```
public UIPickerView.UIPickerViewAppearance GetAppearance<T T : UIPickerView> (UITraitCollection traits, System.Type[] containers)
	public UIPickerView.UIPickerViewAppearance GetAppearance<T T : UIPickerView> (UITraitCollection traits)
	public UIPickerView.UIPickerViewAppearance GetAppearance<T T : UIPickerView> ()
```

### Type Changed: UIKit.UIPopoverBackgroundView

Modified methods:

```
public UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T T : UIPopoverBackgroundView> (UITraitCollection traits)
	public UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T T : UIPopoverBackgroundView> (UITraitCollection traits, System.Type[] containers)
	public UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T T : UIPopoverBackgroundView> ()
```

### Type Changed: UIKit.UIProgressView

Modified methods:

```
public UIProgressView.UIProgressViewAppearance GetAppearance<T T : UIProgressView> (UITraitCollection traits)
	public UIProgressView.UIProgressViewAppearance GetAppearance<T T : UIProgressView> (UITraitCollection traits, System.Type[] containers)
	public UIProgressView.UIProgressViewAppearance GetAppearance<T T : UIProgressView> ()
```

### Type Changed: UIKit.UIRefreshControl

Modified methods:

```
public UIRefreshControl.UIRefreshControlAppearance GetAppearance<T T : UIRefreshControl> ()
	public UIRefreshControl.UIRefreshControlAppearance GetAppearance<T T : UIRefreshControl> (UITraitCollection traits)
	public UIRefreshControl.UIRefreshControlAppearance GetAppearance<T T : UIRefreshControl> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIScrollView

Modified methods:

```
public UIScrollView.UIScrollViewAppearance GetAppearance<T T : UIScrollView> (UITraitCollection traits)
	public UIScrollView.UIScrollViewAppearance GetAppearance<T T : UIScrollView> ()
	public UIScrollView.UIScrollViewAppearance GetAppearance<T T : UIScrollView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UISearchBar

Modified methods:

```
public UISearchBar.UISearchBarAppearance GetAppearance<T T : UISearchBar> ()
	public UISearchBar.UISearchBarAppearance GetAppearance<T T : UISearchBar> (UITraitCollection traits)
	public UISearchBar.UISearchBarAppearance GetAppearance<T T : UISearchBar> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UISegmentedControl

Modified methods:

```
public UISegmentedControl.UISegmentedControlAppearance GetAppearance<T T : UISegmentedControl> ()
	public UISegmentedControl.UISegmentedControlAppearance GetAppearance<T T : UISegmentedControl> (UITraitCollection traits, System.Type[] containers)
	public UISegmentedControl.UISegmentedControlAppearance GetAppearance<T T : UISegmentedControl> (UITraitCollection traits)
```

### Type Changed: UIKit.UISlider

Modified methods:

```
public UISlider.UISliderAppearance GetAppearance<T T : UISlider> (UITraitCollection traits, System.Type[] containers)
	public UISlider.UISliderAppearance GetAppearance<T T : UISlider> ()
	public UISlider.UISliderAppearance GetAppearance<T T : UISlider> (UITraitCollection traits)
```

### Type Changed: UIKit.UIStepper

Modified methods:

```
public UIStepper.UIStepperAppearance GetAppearance<T T : UIStepper> (UITraitCollection traits)
	public UIStepper.UIStepperAppearance GetAppearance<T T : UIStepper> ()
	public UIStepper.UIStepperAppearance GetAppearance<T T : UIStepper> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UISwitch

Modified methods:

```
public UISwitch.UISwitchAppearance GetAppearance<T T : UISwitch> (UITraitCollection traits)
	public UISwitch.UISwitchAppearance GetAppearance<T T : UISwitch> (UITraitCollection traits, System.Type[] containers)
	public UISwitch.UISwitchAppearance GetAppearance<T T : UISwitch> ()
```

### Type Changed: UIKit.UITabBar

Modified methods:

```
public UITabBar.UITabBarAppearance GetAppearance<T T : UITabBar> (UITraitCollection traits)
	public UITabBar.UITabBarAppearance GetAppearance<T T : UITabBar> ()
	public UITabBar.UITabBarAppearance GetAppearance<T T : UITabBar> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UITabBarItem

Modified methods:

```
public UITabBarItem.UITabBarItemAppearance GetAppearance<T T : UITabBarItem> (UITraitCollection traits)
	public UITabBarItem.UITabBarItemAppearance GetAppearance<T T : UITabBarItem> (UITraitCollection traits, System.Type[] containers)
	public UITabBarItem.UITabBarItemAppearance GetAppearance<T T : UITabBarItem> ()
```

### Type Changed: UIKit.UITableView

Modified methods:

```
public UITableView.UITableViewAppearance GetAppearance<T T : UITableView> (UITraitCollection traits)
	public UITableView.UITableViewAppearance GetAppearance<T T : UITableView> ()
	public UITableView.UITableViewAppearance GetAppearance<T T : UITableView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UITableViewCell

Modified methods:

```
public UITableViewCell.UITableViewCellAppearance GetAppearance<T T : UITableViewCell> ()
	public UITableViewCell.UITableViewCellAppearance GetAppearance<T T : UITableViewCell> (UITraitCollection traits)
	public UITableViewCell.UITableViewCellAppearance GetAppearance<T T : UITableViewCell> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UITableViewHeaderFooterView

Modified methods:

```
public UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T T : UITableViewHeaderFooterView> (UITraitCollection traits)
	public UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T T : UITableViewHeaderFooterView> (UITraitCollection traits, System.Type[] containers)
	public UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T T : UITableViewHeaderFooterView> ()
```

### Type Changed: UIKit.UITextField

Modified methods:

```
public UITextField.UITextFieldAppearance GetAppearance<T T : UITextField> (UITraitCollection traits)
	public UITextField.UITextFieldAppearance GetAppearance<T T : UITextField> ()
	public UITextField.UITextFieldAppearance GetAppearance<T T : UITextField> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UITextView

Modified methods:

```
public UITextView.UITextViewAppearance GetAppearance<T T : UITextView> (UITraitCollection traits, System.Type[] containers)
	public UITextView.UITextViewAppearance GetAppearance<T T : UITextView> ()
	public UITextView.UITextViewAppearance GetAppearance<T T : UITextView> (UITraitCollection traits)
```

### Type Changed: UIKit.UIToolbar

Modified methods:

```
public UIToolbar.UIToolbarAppearance GetAppearance<T T : UIToolbar> (UITraitCollection traits)
	public UIToolbar.UIToolbarAppearance GetAppearance<T T : UIToolbar> ()
	public UIToolbar.UIToolbarAppearance GetAppearance<T T : UIToolbar> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIView

Modified methods:

```
public UIView.UIViewAppearance GetAppearance<T T : UIView> (UITraitCollection traits)
	public UIView.UIViewAppearance GetAppearance<T T : UIView> ()
	public UIView.UIViewAppearance GetAppearance<T T : UIView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIVisualEffectView

Modified methods:

```
public UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T T : UIVisualEffectView> ()
	public UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T T : UIVisualEffectView> (UITraitCollection traits)
	public UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T T : UIVisualEffectView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIWebView

Modified methods:

```
public UIWebView.UIWebViewAppearance GetAppearance<T T : UIWebView> ()
	public UIWebView.UIWebViewAppearance GetAppearance<T T : UIWebView> (UITraitCollection traits)
	public UIWebView.UIWebViewAppearance GetAppearance<T T : UIWebView> (UITraitCollection traits, System.Type[] containers)
```

### Type Changed: UIKit.UIWindow

Modified methods:

```
public UIWindow.UIWindowAppearance GetAppearance<T T : UIWindow> (UITraitCollection traits)
	public UIWindow.UIWindowAppearance GetAppearance<T T : UIWindow> ()
	public UIWindow.UIWindowAppearance GetAppearance<T T : UIWindow> (UITraitCollection traits, System.Type[] containers)
```

### New Type UIKit.IUIViewControllerRestoration

```
public interface IUIViewControllerRestoration : ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace WebKit

### Type Changed: WebKit.WKWebView

Modified methods:

```
public WKWebView.WKWebViewAppearance GetAppearance<T T : WKWebView> ()
	public WKWebView.WKWebViewAppearance GetAppearance<T T : WKWebView> (UIKit.UITraitCollection traits)
	public WKWebView.WKWebViewAppearance GetAppearance<T T : WKWebView> (UIKit.UITraitCollection traits, System.Type[] containers)
```

## New Namespace VideoToolbox

### New Type VideoToolbox.VTColorPrimaries

```
[Serializable]
public enum VTColorPrimaries {
	Ebu3213 = 2,
	ItuR7092 = 1,
	P22 = 4,
	SmpteC = 3,
	Unset = 0,
}
```

### New Type VideoToolbox.VTCompressionProperties

```
public class VTCompressionProperties : Foundation.DictionaryContainer {
	// constructors
	public VTCompressionProperties ();
	public VTCompressionProperties (Foundation.NSDictionary dictionary);
	// properties
	public bool? AllowFrameReordering { get; set; }
	public bool? AllowTemporalCompression { get; set; }
	public bool? AspectRatio16x9 { get; set; }
	public int? AverageBitRate { get; set; }
	public Foundation.NSDictionary CleanAperture { get; set; }
	public VTColorPrimaries ColorPrimaries { get; set; }
	public System.Collections.Generic.List<VTDataRateLimit> DataRateLimits { get; set; }
	public CoreMedia.CMPixelFormat? Depth { get; set; }
	public double? ExpectedDuration { get; set; }
	public double? ExpectedFrameRate { get; set; }
	public VTFieldCount? FieldCount { get; set; }
	public VTFieldDetail FieldDetail { get; set; }
	public VTH264EntropyMode H264EntropyMode { get; set; }
	public Foundation.NSData ICCProfile { get; set; }
	public int? MaxFrameDelayCount { get; set; }
	public int? MaxH264SliceBytes { get; set; }
	public int? MaxKeyFrameInterval { get; set; }
	public double? MaxKeyFrameIntervalDuration { get; set; }
	public bool? MoreFramesAfterEnd { get; set; }
	public bool? MoreFramesBeforeStart { get; set; }
	public VTMultiPassStorage MultiPassStorage { get; set; }
	public int? NumberOfPendingFrames { get; }
	public Foundation.NSDictionary PixelAspectRatio { get; set; }
	public bool? PixelBufferPoolIsShared { get; }
	public Foundation.NSDictionary PixelTransferProperties { get; set; }
	public VTProfileLevel ProfileLevel { get; set; }
	public bool? ProgressiveScan { get; set; }
	public float? Quality { get; set; }
	public bool? RealTime { get; set; }
	public uint? SourceFrameCount { get; set; }
	public VTTransferFunction TransferFunction { get; set; }
	public bool? UsingHardwareAcceleratedVideoEncoder { get; }
	public Foundation.NSDictionary VideoEncoderPixelBufferAttributes { get; }
	public VTYCbCrMatrix YCbCrMatrix { get; set; }
}
```

### New Type VideoToolbox.VTCompressionPropertyKey

```
public static class VTCompressionPropertyKey {
	// properties
	public static Foundation.NSString AllowFrameReordering { get; }
	public static Foundation.NSString AllowTemporalCompression { get; }
	public static Foundation.NSString AspectRatio16x9 { get; }
	public static Foundation.NSString AverageBitRate { get; }
	public static Foundation.NSString CleanAperture { get; }
	public static Foundation.NSString ColorPrimaries { get; }
	public static Foundation.NSString DataRateLimits { get; }
	public static Foundation.NSString Depth { get; }
	public static Foundation.NSString ExpectedDuration { get; }
	public static Foundation.NSString ExpectedFrameRate { get; }
	public static Foundation.NSString FieldCount { get; }
	public static Foundation.NSString FieldDetail { get; }
	public static Foundation.NSString H264EntropyMode { get; }
	public static Foundation.NSString ICCProfile { get; }
	public static Foundation.NSString MaxFrameDelayCount { get; }
	public static Foundation.NSString MaxH264SliceBytes { get; }
	public static Foundation.NSString MaxKeyFrameInterval { get; }
	public static Foundation.NSString MaxKeyFrameIntervalDuration { get; }
	public static Foundation.NSString MoreFramesAfterEnd { get; }
	public static Foundation.NSString MoreFramesBeforeStart { get; }
	public static Foundation.NSString MultiPassStorage { get; }
	public static Foundation.NSString NumberOfPendingFrames { get; }
	public static Foundation.NSString PixelAspectRatio { get; }
	public static Foundation.NSString PixelBufferPoolIsShared { get; }
	public static Foundation.NSString PixelTransferProperties { get; }
	public static Foundation.NSString ProfileLevel { get; }
	public static Foundation.NSString ProgressiveScan { get; }
	public static Foundation.NSString Quality { get; }
	public static Foundation.NSString RealTime { get; }
	public static Foundation.NSString SourceFrameCount { get; }
	public static Foundation.NSString TransferFunction { get; }
	public static Foundation.NSString UsingHardwareAcceleratedVideoEncoder { get; }
	public static Foundation.NSString VideoEncoderPixelBufferAttributes { get; }
	public static Foundation.NSString YCbCrMatrix { get; }
}
```

### New Type VideoToolbox.VTCompressionSession

```
public class VTCompressionSession : VideoToolbox.VTSession, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTCompressionSession (IntPtr handle);
	// methods
	protected override void ~VTCompressionSession ();
	public VTStatus BeginPass (VTCompressionSessionOptionFlags flags);
	public VTStatus CompleteFrames (CoreMedia.CMTime completeUntilPresentationTimeStamp);
	public static VTCompressionSession Create (int width, int height, CoreMedia.CMVideoCodecType codecType, VTCompressionSession.VTCompressionOutputCallback compressionOutputCallback, VTVideoEncoderSpecification encoderSpecification, Foundation.NSDictionary sourceImageBufferAttributes);
	public void Dispose ();
	protected override void Dispose (bool disposing);
	public VTStatus EncodeFrame (CoreVideo.CVImageBuffer imageBuffer, CoreMedia.CMTime presentationTimestampe, CoreMedia.CMTime duration, Foundation.NSDictionary frameProperties, IntPtr sourceFrame, out VTEncodeInfoFlags infoFlags);
	public VTStatus EndPass (out bool furtherPassesRequested);
	public VTStatus EndPassAsFinal ();
	public CoreVideo.CVPixelBufferPool GetPixelBufferPool ();
	public VTStatus GetTimeRangesForNextPass (out CoreMedia.CMTimeRange[] timeRanges);
	public VTStatus PrepareToEncodeFrames ();
	public VTStatus SetCompressionProperties (VTCompressionProperties options);

	// inner types
	public sealed delegate VTCompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public VTCompressionSession (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, CoreMedia.CMSampleBuffer buffer, System.AsyncCallback callback, object object);
		public virtual void EndInvoke (System.IAsyncResult result);
		public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, CoreMedia.CMSampleBuffer buffer);
	}
}
```

### New Type VideoToolbox.VTCompressionSessionOptionFlags

```
[Serializable]
[Flags]
public enum VTCompressionSessionOptionFlags {
	BeginFinalPass = 1,
}
```

### New Type VideoToolbox.VTDataRateLimit

```
public struct VTDataRateLimit {
	// constructors
	public VTDataRateLimit (uint numberOfBytes, double seconds);
	// properties
	public uint NumberOfBytes { get; set; }
	public double Seconds { get; set; }
}
```

### New Type VideoToolbox.VTDecodeFrameFlags

```
[Serializable]
[Flags]
public enum VTDecodeFrameFlags {
	DoNotOutputFrame = 2,
	EnableAsynchronousDecompression = 1,
	EnableTemporalProcessing = 8,
	OneTimeRealTimePlayback = 4,
}
```

### New Type VideoToolbox.VTDecodeInfoFlags

```
[Serializable]
[Flags]
public enum VTDecodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
	ImageBufferModifiable = 4,
}
```

### New Type VideoToolbox.VTDecompressionProperties

```
public class VTDecompressionProperties : Foundation.DictionaryContainer {
	// constructors
	public VTDecompressionProperties ();
	public VTDecompressionProperties (Foundation.NSDictionary dictionary);
	// properties
	public bool? ContentHasInterframeDependencies { get; }
	public VTDeinterlaceMode DeinterlaceMode { get; set; }
	public VTFieldMode FieldMode { get; set; }
	public Foundation.NSDictionary MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public Foundation.NSDictionary MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public uint? NumberOfFramesBeingDecoded { get; }
	public VTOnlyTheseFrames OnlyTheseFrames { get; set; }
	public uint? OutputPoolRequestedMinimumBufferCount { get; set; }
	public CoreVideo.CVPixelBufferPool PixelBufferPool { get; }
	public bool? PixelBufferPoolIsShared { get; }
	public CoreMedia.CMPixelFormat[] PixelFormatsWithReducedResolutionSupport { get; }
	public Foundation.NSDictionary PixelTransferProperties { get; set; }
	public bool? RealTime { get; set; }
	public uint? ReducedCoefficientDecode { get; set; }
	public float? ReducedFrameDelivery { get; set; }
	public VTDecompressionResolutionOptions ReducedResolutionDecode { get; set; }
	public Foundation.NSDictionary[] SuggestedQualityOfServiceTiers { get; }
	public CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByPerformance { get; }
	public CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByQuality { get; }
	public uint? ThreadCount { get; set; }
	public bool? UsingHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type VideoToolbox.VTDecompressionPropertyKey

```
public static class VTDecompressionPropertyKey {
	// properties
	public static Foundation.NSString ContentHasInterframeDependencies { get; }
	public static Foundation.NSString DeinterlaceMode { get; }
	public static Foundation.NSString DeinterlaceMode_Temporal { get; }
	public static Foundation.NSString DeinterlaceMode_VerticalFilter { get; }
	public static Foundation.NSString FieldMode { get; }
	public static Foundation.NSString FieldMode_BothFields { get; }
	public static Foundation.NSString FieldMode_BottomFieldOnly { get; }
	public static Foundation.NSString FieldMode_DeinterlaceFields { get; }
	public static Foundation.NSString FieldMode_SingleField { get; }
	public static Foundation.NSString FieldMode_TopFieldOnly { get; }
	public static Foundation.NSString MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static Foundation.NSString MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static Foundation.NSString NumberOfFramesBeingDecoded { get; }
	public static Foundation.NSString OnlyTheseFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_AllFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_IFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_KeyFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_NonDroppableFrames { get; }
	public static Foundation.NSString OutputPoolRequestedMinimumBufferCount { get; }
	public static Foundation.NSString PixelBufferPool { get; }
	public static Foundation.NSString PixelBufferPoolIsShared { get; }
	public static Foundation.NSString PixelFormatsWithReducedResolutionSupport { get; }
	public static Foundation.NSString PixelTransferProperties { get; }
	public static Foundation.NSString RealTime { get; }
	public static Foundation.NSString ReducedCoefficientDecode { get; }
	public static Foundation.NSString ReducedFrameDelivery { get; }
	public static Foundation.NSString ReducedResolutionDecode { get; }
	public static Foundation.NSString SuggestedQualityOfServiceTiers { get; }
	public static Foundation.NSString SupportedPixelFormatsOrderedByPerformance { get; }
	public static Foundation.NSString SupportedPixelFormatsOrderedByQuality { get; }
	public static Foundation.NSString ThreadCount { get; }
	public static Foundation.NSString UsingHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type VideoToolbox.VTDecompressionResolutionKeys

```
public static class VTDecompressionResolutionKeys {
	// properties
	public static Foundation.NSString Height { get; }
	public static Foundation.NSString Width { get; }
}
```

### New Type VideoToolbox.VTDecompressionResolutionOptions

```
public class VTDecompressionResolutionOptions : Foundation.DictionaryContainer {
	// constructors
	public VTDecompressionResolutionOptions ();
	public VTDecompressionResolutionOptions (Foundation.NSDictionary dictionary);
	// properties
	public float? Height { get; set; }
	public float? Width { get; set; }
}
```

### New Type VideoToolbox.VTDecompressionSession

```
public class VTDecompressionSession : VideoToolbox.VTSession, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTDecompressionSession (IntPtr handle);
	// methods
	protected override void ~VTDecompressionSession ();
	public VTStatus CanAcceptFormatDescriptor (CoreMedia.CMFormatDescription newDescriptor);
	public VTStatus CopyBlackPixelBuffer (out CoreVideo.CVPixelBuffer pixelBuffer);
	public static VTDecompressionSession Create (VTDecompressionSession.VTDecompressionOutputCallback outputCallback, CoreMedia.CMVideoFormatDescription formatDescription, VTVideoDecoderSpecification decoderSpecification, Foundation.NSDictionary destinationImageBufferAttributes);
	public VTStatus DecodeFrame (CoreMedia.CMSampleBuffer sampleBuffer, VTDecodeFrameFlags decodeFlags, IntPtr sourceFrame, out VTDecodeInfoFlags infoFlags);
	protected override void Dispose (bool disposing);
	public void Dispose ();
	public VTStatus FinishDelayedFrames ();
	public VTStatus SetDecompressionProperties (VTDecompressionProperties options);
	public VTStatus WaitForAsynchronousFrames ();

	// inner types
	public sealed delegate VTDecompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public VTDecompressionSession (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, CoreVideo.CVImageBuffer buffer, CoreMedia.CMTime presentationTimeStamp, CoreMedia.CMTime presentationDuration, System.AsyncCallback callback, object object);
		public virtual void EndInvoke (System.IAsyncResult result);
		public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, CoreVideo.CVImageBuffer buffer, CoreMedia.CMTime presentationTimeStamp, CoreMedia.CMTime presentationDuration);
	}
}
```

### New Type VideoToolbox.VTDeinterlaceMode

```
[Serializable]
public enum VTDeinterlaceMode {
	Temporal = 2,
	Unset = 0,
	VerticalFilter = 1,
}
```

### New Type VideoToolbox.VTEncodeFrameOptionKey

```
public static class VTEncodeFrameOptionKey {
	// properties
	public static Foundation.NSString ForceKeyFrame { get; }
}
```

### New Type VideoToolbox.VTEncodeFrameOptions

```
public class VTEncodeFrameOptions : Foundation.DictionaryContainer {
	// constructors
	public VTEncodeFrameOptions ();
	public VTEncodeFrameOptions (Foundation.NSDictionary dictionary);
	// properties
	public bool? ForceKeyFrame { get; set; }
}
```

### New Type VideoToolbox.VTEncodeInfoFlags

```
[Serializable]
[Flags]
public enum VTEncodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
}
```

### New Type VideoToolbox.VTFieldCount

```
[Serializable]
public enum VTFieldCount {
	Interlaced = 2,
	Progressive = 1,
}
```

### New Type VideoToolbox.VTFieldDetail

```
[Serializable]
public enum VTFieldDetail {
	SpatialFirstLineEarly = 3,
	SpatialFirstLineLate = 4,
	TemporalBottomFirst = 2,
	TemporalTopFirst = 1,
	Unset = 0,
}
```

### New Type VideoToolbox.VTFieldMode

```
[Serializable]
public enum VTFieldMode {
	BothFields = 1,
	BottomFieldOnly = 3,
	DeinterlaceFields = 5,
	SingleField = 4,
	TopFieldOnly = 2,
	Unset = 0,
}
```

### New Type VideoToolbox.VTFrameSilo

```
public class VTFrameSilo : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTFrameSilo (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTFrameSilo ();
	public VTStatus AddSampleBuffer (CoreMedia.CMSampleBuffer sampleBuffer);
	public static VTFrameSilo Create (Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange);
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	public VTStatus ForEach (System.Func<CoreMedia.CMSampleBuffer,VideoToolbox.VTStatus> callback, CoreMedia.CMTimeRange? range);
	public VTStatus GetProgressOfCurrentPass (out float progress);
	public VTStatus SetTimeRangesForNextPass (CoreMedia.CMTimeRange[] ranges);
}
```

### New Type VideoToolbox.VTH264EntropyMode

```
[Serializable]
public enum VTH264EntropyMode {
	Cabac = 2,
	Cavlc = 1,
	Unset = 0,
}
```

### New Type VideoToolbox.VTH264EntropyModeKeys

```
public static class VTH264EntropyModeKeys {
	// properties
	public static Foundation.NSString CABAC { get; }
	public static Foundation.NSString CAVLC { get; }
}
```

### New Type VideoToolbox.VTMultiPassStorage

```
public class VTMultiPassStorage : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTMultiPassStorage (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTMultiPassStorage ();
	public VTStatus Close ();
	public static VTMultiPassStorage Create (VTMultiPassStorageCreationOptions options, Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange);
	public static VTMultiPassStorage Create (Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange, Foundation.NSDictionary options);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
```

### New Type VideoToolbox.VTMultiPassStorageCreationOptionKeys

```
public static class VTMultiPassStorageCreationOptionKeys {
	// properties
	public static Foundation.NSString DoNotDelete { get; }
}
```

### New Type VideoToolbox.VTMultiPassStorageCreationOptions

```
public class VTMultiPassStorageCreationOptions : Foundation.DictionaryContainer {
	// constructors
	public VTMultiPassStorageCreationOptions ();
	public VTMultiPassStorageCreationOptions (Foundation.NSDictionary dictionary);
	// properties
	public bool? DoNotDelete { get; set; }
}
```

### New Type VideoToolbox.VTOnlyTheseFrames

```
[Serializable]
public enum VTOnlyTheseFrames {
	AllFrames = 1,
	IFrames = 3,
	KeyFrames = 4,
	NonDroppableFrames = 2,
	Unset = 0,
}
```

### New Type VideoToolbox.VTProfileLevel

```
[Serializable]
public enum VTProfileLevel {
	H263Profile0Level10 = 46,
	H263Profile0Level45 = 47,
	H263Profile3Level45 = 48,
	H264Baseline13 = 1,
	H264Baseline30 = 2,
	H264Baseline31 = 3,
	H264Baseline32 = 4,
	H264Baseline40 = 5,
	H264Baseline41 = 6,
	H264Baseline42 = 7,
	H264Baseline50 = 8,
	H264Baseline51 = 9,
	H264Baseline52 = 10,
	H264BaselineAutoLevel = 11,
	H264Extended50 = 22,
	H264ExtendedAutoLevel = 23,
	H264High30 = 24,
	H264High31 = 25,
	H264High32 = 26,
	H264High40 = 27,
	H264High41 = 28,
	H264High42 = 29,
	H264High50 = 30,
	H264High51 = 31,
	H264High52 = 32,
	H264HighAutoLevel = 33,
	H264Main30 = 12,
	H264Main31 = 13,
	H264Main32 = 14,
	H264Main40 = 15,
	H264Main41 = 16,
	H264Main42 = 17,
	H264Main50 = 18,
	H264Main51 = 19,
	H264Main52 = 20,
	H264MainAutoLevel = 21,
	MP4VAdvancedSimpleL0 = 41,
	MP4VAdvancedSimpleL1 = 42,
	MP4VAdvancedSimpleL2 = 43,
	MP4VAdvancedSimpleL3 = 44,
	MP4VAdvancedSimpleL4 = 45,
	MP4VMainL2 = 38,
	MP4VMainL3 = 39,
	MP4VMainL4 = 40,
	MP4VSimpleL0 = 34,
	MP4VSimpleL1 = 35,
	MP4VSimpleL2 = 36,
	MP4VSimpleL3 = 37,
	Unset = 0,
}
```

### New Type VideoToolbox.VTProfileLevelKeys

```
public static class VTProfileLevelKeys {
	// properties
	public static Foundation.NSString H263_Profile0_Level10 { get; }
	public static Foundation.NSString H263_Profile0_Level45 { get; }
	public static Foundation.NSString H263_Profile3_Level45 { get; }
	public static Foundation.NSString H264_Baseline_1_3 { get; }
	public static Foundation.NSString H264_Baseline_3_0 { get; }
	public static Foundation.NSString H264_Baseline_3_1 { get; }
	public static Foundation.NSString H264_Baseline_3_2 { get; }
	public static Foundation.NSString H264_Baseline_4_0 { get; }
	public static Foundation.NSString H264_Baseline_4_1 { get; }
	public static Foundation.NSString H264_Baseline_4_2 { get; }
	public static Foundation.NSString H264_Baseline_5_0 { get; }
	public static Foundation.NSString H264_Baseline_5_1 { get; }
	public static Foundation.NSString H264_Baseline_5_2 { get; }
	public static Foundation.NSString H264_Baseline_AutoLevel { get; }
	public static Foundation.NSString H264_Extended_5_0 { get; }
	public static Foundation.NSString H264_Extended_AutoLevel { get; }
	public static Foundation.NSString H264_High_3_0 { get; }
	public static Foundation.NSString H264_High_3_1 { get; }
	public static Foundation.NSString H264_High_3_2 { get; }
	public static Foundation.NSString H264_High_4_0 { get; }
	public static Foundation.NSString H264_High_4_1 { get; }
	public static Foundation.NSString H264_High_4_2 { get; }
	public static Foundation.NSString H264_High_5_0 { get; }
	public static Foundation.NSString H264_High_5_1 { get; }
	public static Foundation.NSString H264_High_5_2 { get; }
	public static Foundation.NSString H264_High_AutoLevel { get; }
	public static Foundation.NSString H264_Main_3_0 { get; }
	public static Foundation.NSString H264_Main_3_1 { get; }
	public static Foundation.NSString H264_Main_3_2 { get; }
	public static Foundation.NSString H264_Main_4_0 { get; }
	public static Foundation.NSString H264_Main_4_1 { get; }
	public static Foundation.NSString H264_Main_4_2 { get; }
	public static Foundation.NSString H264_Main_5_0 { get; }
	public static Foundation.NSString H264_Main_5_1 { get; }
	public static Foundation.NSString H264_Main_5_2 { get; }
	public static Foundation.NSString H264_Main_AutoLevel { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L0 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L1 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L2 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L3 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L4 { get; }
	public static Foundation.NSString MP4V_Main_L2 { get; }
	public static Foundation.NSString MP4V_Main_L3 { get; }
	public static Foundation.NSString MP4V_Main_L4 { get; }
	public static Foundation.NSString MP4V_Simple_L0 { get; }
	public static Foundation.NSString MP4V_Simple_L1 { get; }
	public static Foundation.NSString MP4V_Simple_L2 { get; }
	public static Foundation.NSString MP4V_Simple_L3 { get; }
}
```

### New Type VideoToolbox.VTPropertyKeys

```
public static class VTPropertyKeys {
	// properties
	public static Foundation.NSString DocumentationKey { get; }
	public static Foundation.NSString ReadWriteStatus { get; }
	public static Foundation.NSString ShouldBeSerialized { get; }
	public static Foundation.NSString SupportedValueListKey { get; }
	public static Foundation.NSString SupportedValueMaximumKey { get; }
	public static Foundation.NSString SupportedValueMinimumKey { get; }
	public static Foundation.NSString Type { get; }
}
```

### New Type VideoToolbox.VTPropertyOptions

```
public class VTPropertyOptions : Foundation.DictionaryContainer {
	// constructors
	public VTPropertyOptions ();
	public VTPropertyOptions (Foundation.NSDictionary dictionary);
	// properties
	public Foundation.NSString Documentation { get; set; }
	public VTReadWriteStatus ReadWriteStatus { get; set; }
	public bool? ShouldBeSerialized { get; set; }
	public Foundation.NSNumber[] SupportedValueList { get; set; }
	public Foundation.NSNumber SupportedValueMaximum { get; set; }
	public Foundation.NSNumber SupportedValueMinimum { get; set; }
	public VTPropertyType Type { get; set; }
}
```

### New Type VideoToolbox.VTPropertyReadWriteStatusKeys

```
public static class VTPropertyReadWriteStatusKeys {
	// properties
	public static Foundation.NSString ReadOnly { get; }
	public static Foundation.NSString ReadWrite { get; }
}
```

### New Type VideoToolbox.VTPropertyType

```
[Serializable]
public enum VTPropertyType {
	Boolean = 2,
	Enumeration = 1,
	Number = 3,
	Unset = 0,
}
```

### New Type VideoToolbox.VTPropertyTypeKeys

```
public static class VTPropertyTypeKeys {
	// properties
	public static Foundation.NSString Boolean { get; }
	public static Foundation.NSString Enumeration { get; }
	public static Foundation.NSString Number { get; }
}
```

### New Type VideoToolbox.VTReadWriteStatus

```
[Serializable]
public enum VTReadWriteStatus {
	ReadOnly = 1,
	ReadWrite = 2,
	Unset = 0,
}
```

### New Type VideoToolbox.VTSession

```
public class VTSession : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTSession (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTSession ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public VTPropertyOptions GetProperties ();
	public Foundation.NSObject GetProperty (Foundation.NSString propertyKey);
	public Foundation.NSDictionary GetSerializableProperties ();
	public Foundation.NSDictionary GetSupportedProperties ();
	public VTStatus SetProperties (VTPropertyOptions options);
	public VTStatus SetProperty (Foundation.NSString propertyKey, Foundation.NSObject value);
}
```

### New Type VideoToolbox.VTStatus

```
[Serializable]
public enum VTStatus {
	AllocationFailed = -12904,
	ColorCorrectionPixelTransferFailed = -12212,
	ColorSyncTransformConvertFailed = -12919,
	CouldNotCreateColorCorrectionData = -12918,
	CouldNotCreateInstance = -12907,
	CouldNotFindTemporalFilter = -12217,
	CouldNotFindVideoDecoder = -12906,
	CouldNotFindVideoEncoder = -12908,
	FormatDescriptionChangeNotSupported = -12916,
	FrameSiloInvalidTimeRange = -12216,
	FrameSiloInvalidTimeStamp = -12215,
	ImageRotationNotSupported = -12914,
	InsufficientSourceColorData = -12917,
	InvalidSession = -12903,
	MultiPassStorageIdentifierMismatch = -12913,
	MultiPassStorageInvalid = -12214,
	Ok = 0,
	Parameter = -12902,
	PixelTransferNotPermitted = -12218,
	PixelTransferNotSupported = -12905,
	PropertyNotSupported = -12900,
	PropertyReadOnly = -12901,
	VideoDecoderAuthorization = -12210,
	VideoDecoderBadData = -12909,
	VideoDecoderMalfunction = -12911,
	VideoDecoderNotAvailableNow = -12913,
	VideoDecoderUnsupportedDataFormat = -12910,
	VideoEncoderAuthorization = -12211,
	VideoEncoderMalfunction = -12912,
	VideoEncoderNotAvailableNow = -12915,
}
```

### New Type VideoToolbox.VTTransferFunction

```
[Serializable]
public enum VTTransferFunction {
	ItuR7092 = 1,
	Smpte240M1955 = 2,
	Unset = 0,
	UseGamma = 3,
}
```

### New Type VideoToolbox.VTVideoDecoderSpecification

```
public class VTVideoDecoderSpecification : Foundation.DictionaryContainer {
	// constructors
	public VTVideoDecoderSpecification ();
	public VTVideoDecoderSpecification (Foundation.NSDictionary dictionary);
	// properties
	public bool? EnableHardwareAcceleratedVideoDecoder { get; set; }
	public bool? RequireHardwareAcceleratedVideoDecoder { get; set; }
}
```

### New Type VideoToolbox.VTVideoDecoderSpecificationKeys

```
public static class VTVideoDecoderSpecificationKeys {
	// properties
	public static Foundation.NSString EnableHardwareAcceleratedVideoDecoder { get; }
	public static Foundation.NSString RequireHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type VideoToolbox.VTVideoEncoder

```
public class VTVideoEncoder {
	// properties
	public string CodecName { get; }
	public int CodecType { get; }
	public string DisplayName { get; }
	public string EncoderId { get; }
	public string EncoderName { get; }
	// methods
	public static VTVideoEncoder[] GetEncoderList ();
}
```

### New Type VideoToolbox.VTVideoEncoderSpecification

```
public class VTVideoEncoderSpecification : Foundation.DictionaryContainer {
	// constructors
	public VTVideoEncoderSpecification ();
	public VTVideoEncoderSpecification (Foundation.NSDictionary dictionary);
	// properties
	public string EncoderID { get; set; }
}
```

### New Type VideoToolbox.VTVideoEncoderSpecificationKeys

```
public static class VTVideoEncoderSpecificationKeys {
	// properties
	public static Foundation.NSString EncoderID { get; }
}
```

### New Type VideoToolbox.VTYCbCrMatrix

```
[Serializable]
public enum VTYCbCrMatrix {
	ItuR6014 = 2,
	ItuR7092 = 1,
	Smpte240M1955 = 3,
	Unset = 0,
}
```

   


 <hr>
