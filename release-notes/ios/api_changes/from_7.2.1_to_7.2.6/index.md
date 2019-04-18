---
id: 8FDCEFF0-37DC-40A7-879D-306B774A82D3
title: "From 7.2.1 to 7.2.6"
---

# mscorlib.dll

## Namespace System.Diagnostics

### Type Changed: System.Diagnostics.Debugger

Added method:

```
public static void NotifyOfCrossThreadDependency ();
```

## Namespace System.Diagnostics.Tracing

### Type Changed: System.Diagnostics.Tracing.EventCommandEventArgs

Added properties:

```
public System.Collections.Generic.IDictionary<System.String,System.String> Arguments { get; }
	public EventCommand Command { get; }
```

Added methods:

```
public bool DisableEvent (int eventId);
	public bool EnableEvent (int eventId);
```

### Type Changed: System.Diagnostics.Tracing.EventSource

Added methods:

```
public bool IsEnabled (EventLevel level, EventKeywords keywords);
	protected virtual void OnEventCommand (EventCommandEventArgs command);
	protected void WriteEvent (int eventId, string arg1);
	protected void WriteEvent (int eventId, string arg1, int arg2);
	protected void WriteEvent (int eventId, string arg1, int arg2, int arg3);
```

### New Type System.Diagnostics.Tracing.EventAttribute

```
public sealed class EventAttribute : System.Attribute {
	// constructors
	public EventAttribute (int eventId);
	// properties
	public int EventId { get; }
}
```

### New Type System.Diagnostics.Tracing.EventCommand

```
[Serializable]
public enum EventCommand {
	Disable = -3,
	Enable = -2,
	SendManifest = -1,
	Update = 0,
}
```

### New Type System.Diagnostics.Tracing.EventKeywords

```
[Serializable]
[Flags]
public enum EventKeywords {
	AuditFailure = 4503599627370496,
	AuditSuccess = 9007199254740992,
	CorrelationHint = 4503599627370496,
	EventLogClassic = 36028797018963968,
	None = 0,
	Sqm = 2251799813685248,
	WdiContext = 562949953421312,
	WdiDiagnostic = 1125899906842624,
}
```

### New Type System.Diagnostics.Tracing.EventLevel

```
[Serializable]
public enum EventLevel {
	Critical = 1,
	Error = 2,
	Informational = 4,
	LogAlways = 0,
	Verbose = 5,
	Warning = 3,
}
```

### New Type System.Diagnostics.Tracing.EventSourceAttribute

```
public sealed class EventSourceAttribute : System.Attribute {
	// constructors
	public EventSourceAttribute ();
	// properties
	public string Guid { get; set; }
	public string LocalizationResources { get; set; }
	public string Name { get; set; }
}
```

### New Type System.Diagnostics.Tracing.NonEventAttribute

```
public sealed class NonEventAttribute : System.Attribute {
	// constructors
	public NonEventAttribute ();
}
```

## Namespace System.Globalization

### New Type System.Globalization.SortVersion

```
[Serializable]
public sealed class SortVersion : System.IEquatable<SortVersion> {
	// constructors
	public SortVersion (int fullVersion, System.Guid sortId);
	// properties
	public int FullVersion { get; }
	public System.Guid SortId { get; }
	// methods
	public override bool Equals (object obj);
	public virtual bool Equals (SortVersion other);
	public override int GetHashCode ();
	public static bool op_Equality (SortVersion left, SortVersion right);
	public static bool op_Inequality (SortVersion left, SortVersion right);
}
```

## Namespace System.Runtime

### New Type System.Runtime.GCLargeObjectHeapCompactionMode

```
[Serializable]
public enum GCLargeObjectHeapCompactionMode {
	CompactOnce = 2,
	Default = 1,
}
```

## Namespace System.Runtime.InteropServices

### Type Changed: System.Runtime.InteropServices.ComInterfaceType

Added value:

```
InterfaceIsIInspectable = 3,
```

## Namespace System.Security.Principal

### Type Changed: System.Security.Principal.WindowsIdentity

Removed properties:

```
public virtual string AuthenticationType { get; }
	public virtual bool IsAuthenticated { get; }
	public virtual string Name { get; }
```

Added properties:

```
public override string AuthenticationType { get; }
	public override bool IsAuthenticated { get; }
	public override string Name { get; }
```

## New Namespace System.Security.Claims

### New Type System.Security.Claims.Claim

```
[Serializable]
public class Claim {
	// constructors
	public Claim (string type, string value);
	public Claim (string type, string value, string valueType);
	public Claim (string type, string value, string valueType, string issuer);
	public Claim (string type, string value, string valueType, string issuer, string originalIssuer);
	public Claim (string type, string value, string valueType, string issuer, string originalIssuer, ClaimsIdentity subject);
	// properties
	public string Issuer { get; }
	public string OriginalIssuer { get; }
	public System.Collections.Generic.IDictionary<System.String,System.String> Properties { get; }
	public ClaimsIdentity Subject { get; }
	public string Type { get; }
	public string Value { get; }
	public string ValueType { get; }
	// methods
	public virtual Claim Clone ();
	public virtual Claim Clone (ClaimsIdentity identity);
	public override string ToString ();
}
```

### New Type System.Security.Claims.ClaimsIdentity

```
[Serializable]
public class ClaimsIdentity : System.Security.Principal.IIdentity {
	// constructors
	public ClaimsIdentity ();
	protected ClaimsIdentity (System.Runtime.Serialization.SerializationInfo info);
	public ClaimsIdentity (System.Security.Principal.IIdentity identity, System.Collections.Generic.IEnumerable<Claim> claims, string authenticationType, string nameType, string roleType);
	public ClaimsIdentity (System.Security.Principal.IIdentity identity, System.Collections.Generic.IEnumerable<Claim> claims);
	public ClaimsIdentity (System.Collections.Generic.IEnumerable<Claim> claims, string authenticationType, string nameType, string roleType);
	public ClaimsIdentity (System.Security.Principal.IIdentity identity);
	public ClaimsIdentity (string authenticationType, string nameType, string roleType);
	public ClaimsIdentity (System.Collections.Generic.IEnumerable<Claim> claims, string authenticationType);
	public ClaimsIdentity (string authenticationType);
	protected ClaimsIdentity (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
	// fields
	public static const string DefaultIssuer = "LOCAL AUTHORITY";
	public static const string DefaultNameClaimType = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name";
	public static const string DefaultRoleClaimType = "http://schemas.microsoft.com/ws/2008/06/identity/claims/role";
	// properties
	public ClaimsIdentity Actor { get; set; }
	public virtual string AuthenticationType { get; }
	public object BootstrapContext { get; set; }
	public virtual System.Collections.Generic.IEnumerable<Claim> Claims { get; }
	public virtual bool IsAuthenticated { get; }
	public string Label { get; set; }
	public virtual string Name { get; }
	public string NameClaimType { get; }
	public string RoleClaimType { get; }
	// methods
	public virtual void AddClaim (Claim claim);
	public virtual void AddClaims (System.Collections.Generic.IEnumerable<Claim> claims);
	public virtual ClaimsIdentity Clone ();
	public virtual System.Collections.Generic.IEnumerable<Claim> FindAll (System.Predicate<Claim> match);
	public virtual System.Collections.Generic.IEnumerable<Claim> FindAll (string type);
	public virtual Claim FindFirst (string type);
	public virtual Claim FindFirst (System.Predicate<Claim> match);
	public virtual bool HasClaim (System.Predicate<Claim> match);
	public virtual bool HasClaim (string type, string value);
	public virtual void RemoveClaim (Claim claim);
	public virtual bool TryRemoveClaim (Claim claim);
}
```

### New Type System.Security.Claims.ClaimsPrincipal

```
[Serializable]
public class ClaimsPrincipal : System.Security.Principal.IPrincipal {
	// constructors
	public ClaimsPrincipal ();
	public ClaimsPrincipal (System.Collections.Generic.IEnumerable<ClaimsIdentity> identities);
	public ClaimsPrincipal (System.Security.Principal.IIdentity identity);
	public ClaimsPrincipal (System.Security.Principal.IPrincipal principal);
	protected ClaimsPrincipal (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
	// properties
	public virtual System.Collections.Generic.IEnumerable<Claim> Claims { get; }
	public static System.Func<ClaimsPrincipal> ClaimsPrincipalSelector { get; set; }
	public static ClaimsPrincipal Current { get; }
	public virtual System.Collections.Generic.IEnumerable<ClaimsIdentity> Identities { get; }
	public virtual System.Security.Principal.IIdentity Identity { get; }
	public static System.Func<System.Collections.Generic.IEnumerable<ClaimsIdentity>> PrimaryIdentitySelector { get; set; }
	// methods
	public virtual void AddIdentities (System.Collections.Generic.IEnumerable<ClaimsIdentity> identities);
	public virtual void AddIdentity (ClaimsIdentity identity);
	public virtual System.Collections.Generic.IEnumerable<Claim> FindAll (System.Predicate<Claim> match);
	public virtual Claim FindFirst (System.Predicate<Claim> match);
	public virtual bool HasClaim (System.Predicate<Claim> match);
	public virtual bool IsInRole (string role);
}
```

### New Type System.Security.Claims.ClaimTypes

```
public static class ClaimTypes {
	// fields
	public static const string Anonymous = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/anonymous";
	public static const string Authentication = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/authentication";
	public static const string AuthorizationDecision = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/authorizationdecision";
	public static const string Country = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country";
	public static const string DateOfBirth = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/dateofbirth";
	public static const string DenyOnlySid = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/denyonlysid";
	public static const string Dns = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/dns";
	public static const string Email = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress";
	public static const string Gender = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/gender";
	public static const string GivenName = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname";
	public static const string Hash = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/hash";
	public static const string HomePhone = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/homephone";
	public static const string Locality = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/locality";
	public static const string MobilePhone = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/mobilephone";
	public static const string Name = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name";
	public static const string NameIdentifier = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier";
	public static const string OtherPhone = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/otherphone";
	public static const string PostalCode = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/postalcode";
	public static const string PPID = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/privatepersonalidentifier";
	public static const string Rsa = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/rsa";
	public static const string Sid = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/sid";
	public static const string Spn = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn";
	public static const string StateOrProvince = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/stateorprovince";
	public static const string StreetAddress = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/streetaddress";
	public static const string Surname = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname";
	public static const string System = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/system";
	public static const string Thumbprint = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/thumbprint";
	public static const string Upn = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn";
	public static const string Uri = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/uri";
	public static const string Webpage = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/webpage";
	public static const string X500DistinguishedName = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/x500distinguishedname";
}
```

### New Type System.Security.Claims.ClaimValueTypes

```
public static class ClaimValueTypes {
	// fields
	public static const string Base64Binary = "http://www.w3.org/2001/XMLSchema#base64Binary";
	public static const string Base64Octet = "http://www.w3.org/2001/XMLSchema#base64Octet";
	public static const string Boolean = "http://www.w3.org/2001/XMLSchema#boolean";
	public static const string Date = "http://www.w3.org/2001/XMLSchema#date";
	public static const string DateTime = "http://www.w3.org/2001/XMLSchema#dateTime";
	public static const string DaytimeDuration = "http://www.w3.org/TR/2002/WD-xquery-operators-20020816#dayTimeDuration";
	public static const string DnsName = "http://schemas.xmlsoap.org/claims/dns";
	public static const string Double = "http://www.w3.org/2001/XMLSchema#double";
	public static const string DsaKeyValue = "http://www.w3.org/2000/09/xmldsig#DSAKeyValue";
	public static const string Email = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress";
	public static const string Fqbn = "http://www.w3.org/2001/XMLSchema#fqbn";
	public static const string HexBinary = "http://www.w3.org/2001/XMLSchema#hexBinary";
	public static const string Integer = "http://www.w3.org/2001/XMLSchema#integer";
	public static const string Integer32 = "http://www.w3.org/2001/XMLSchema#integer32";
	public static const string Integer64 = "http://www.w3.org/2001/XMLSchema#integer64";
	public static const string KeyInfo = "http://www.w3.org/2000/09/xmldsig#KeyInfo";
	public static const string Rfc822Name = "urn:oasis:names:tc:xacml:1.0:data-type:rfc822Name";
	public static const string Rsa = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/rsa";
	public static const string RsaKeyValue = "http://www.w3.org/2000/09/xmldsig#RSAKeyValue";
	public static const string Sid = "http://www.w3.org/2001/XMLSchema#sid";
	public static const string String = "http://www.w3.org/2001/XMLSchema#string";
	public static const string Time = "http://www.w3.org/2001/XMLSchema#time";
	public static const string UInteger32 = "http://www.w3.org/2001/XMLSchema#uinteger32";
	public static const string UInteger64 = "http://www.w3.org/2001/XMLSchema#uinteger64";
	public static const string UpnName = "http://schemas.xmlsoap.org/claims/UPN";
	public static const string X500Name = "urn:oasis:names:tc:xacml:1.0:data-type:x500Name";
	public static const string YearMonthDuration = "http://www.w3.org/TR/2002/WD-xquery-operators-20020816#yearMonthDuration";
}
```

   


 <hr>

# System.dll

## Namespace System.Net.Mail

### Type Changed: System.Net.Mail.SmtpClient

Added methods:

```
public System.Threading.Tasks.Task SendMailAsync (MailMessage message);
	public System.Threading.Tasks.Task SendMailAsync (string from, string recipients, string subject, string body);
```

## Namespace System.Runtime.InteropServices

### New Type System.Runtime.InteropServices.HandleCollector

```
public sealed class HandleCollector {
	// constructors
	public HandleCollector (string name, int initialThreshold);
	public HandleCollector (string name, int initialThreshold, int maximumThreshold);
	// properties
	public int Count { get; }
	public int InitialThreshold { get; }
	public int MaximumThreshold { get; }
	public string Name { get; }
	// methods
	public void Add ();
	public void Remove ();
}
```

   


 <hr>

# System.Core.dll

## Namespace System.IO.MemoryMappedFiles

### Type Changed: System.IO.MemoryMappedFiles.MemoryMappedFile

Removed methods:

```
public static MemoryMappedFile CreateFromFile (System.IO.FileStream fileStream, string mapName, long capacity, MemoryMappedFileAccess access, System.IO.HandleInheritability inheritability, bool leaveOpen);
	public static MemoryMappedFile CreateNew (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, System.IO.HandleInheritability handleInheritability);
	public static MemoryMappedFile CreateOrOpen (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, System.IO.HandleInheritability inheritability);
```

Added methods:

```
public static MemoryMappedFile CreateFromFile (System.IO.FileStream fileStream, string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileSecurity memoryMappedFileSecurity, System.IO.HandleInheritability inheritability, bool leaveOpen);
	public static MemoryMappedFile CreateNew (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, MemoryMappedFileSecurity memoryMappedFileSecurity, System.IO.HandleInheritability inheritability);
	public static MemoryMappedFile CreateOrOpen (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, MemoryMappedFileSecurity memoryMappedFileSecurity, System.IO.HandleInheritability inheritability);
	public MemoryMappedFileSecurity GetAccessControl ();
	public void SetAccessControl (MemoryMappedFileSecurity memoryMappedFileSecurity);
```

### Type Changed: System.IO.MemoryMappedFiles.MemoryMappedViewStream

Added property:

```
public Microsoft.Win32.SafeHandles.SafeMemoryMappedViewHandle SafeMemoryMappedViewHandle { get; }
```

### New Type System.IO.MemoryMappedFiles.MemoryMappedFileSecurity

```
public class MemoryMappedFileSecurity : System.Security.AccessControl.ObjectSecurity`1[System.IO.MemoryMappedFiles.MemoryMappedFileRights] {
	// constructors
	public MemoryMappedFileSecurity ();
}
```

## Namespace System.Security.Cryptography

### New Type System.Security.Cryptography.AesCryptoServiceProvider

```
public sealed class AesCryptoServiceProvider : System.Security.Cryptography.Aes, System.IDisposable {
	// constructors
	public AesCryptoServiceProvider ();
	// methods
	public override ICryptoTransform CreateDecryptor (byte[] rgbKey, byte[] rgbIV);
	public override ICryptoTransform CreateEncryptor (byte[] rgbKey, byte[] rgbIV);
	public override void GenerateIV ();
	public override void GenerateKey ();
}
```

   


 <hr>

# System.ComponentModel.DataAnnotations.dll

## Namespace System.ComponentModel.DataAnnotations

### New Type System.ComponentModel.DataAnnotations.UrlAttribute

```
public sealed class UrlAttribute : System.ComponentModel.DataAnnotations.DataTypeAttribute {
	// constructors
	public UrlAttribute ();
	// methods
	public override bool IsValid (object value);
}
```

   


 <hr>

# System.IO.Compression.dll

## Namespace System.IO.Compression

### Type Changed: System.IO.Compression.ZipArchiveEntry

Removed constructor:

```
public ZipArchiveEntry ();
```

   


 <hr>

# Mono.Security.dll

## Namespace Mono.Security.X509.Extensions

### Type Changed: Mono.Security.X509.Extensions.AuthorityKeyIdentifierExtension

Removed property:

```
public byte[] Identifier { get; }
```

Added property:

```
public byte[] Identifier { get; set; }
```

Added method:

```
protected override void Encode ();
```

### Type Changed: Mono.Security.X509.Extensions.SubjectKeyIdentifierExtension

Removed property:

```
public byte[] Identifier { get; }
```

Added property:

```
public byte[] Identifier { get; set; }
```

Added method:

```
protected override void Encode ();
```

   


 <hr>

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed field:

```
public static const string Version = "7.2.1";
```

Added field:

```
public static const string Version = "7.2.6";
```

## Namespace MonoTouch.Accelerate

### Type Changed: MonoTouch.Accelerate.vImage

Added methods:

```
public static vImageError ConvolveMultiKernelARGB8888 (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, short[][] kernels, uint kernel_height, uint kernel_width, int[] divisors, int[] biases, Pixel8888 backgroundColor, vImageFlags flags);
	public static vImageError ConvolveMultiKernelARGBFFFF (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, float[][] kernels, uint kernel_height, uint kernel_width, float[] biases, PixelFFFF backgroundColor, vImageFlags flags);
```

Obsoleted methods:

```
[Obsolete ("Use the overload with 'short[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGB8888 (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, short[] kernels, uint kernel_height, uint kernel_width, int[] divisors, int[] biases, Pixel8888 backgroundColor, vImageFlags flags);

	[Obsolete ("Use the overload with 'float[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGBFFFF (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, float[] kernels, uint kernel_height, uint kernel_width, float[] biases, ref PixelFFFF backgroundColor, vImageFlags flags);

	[Obsolete ("Use the overload with 'float[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGBFFFF (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, float[] kernels, uint kernel_height, uint kernel_width, float[] biases, PixelFFFF backgroundColor, vImageFlags flags);
```

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.MusicSequence

Added methods:

```
public MusicPlayerStatus BarBeatTimeToBeats (MonoTouch.CoreAnimation.CABarBeatTime barBeatTime, out double beats);
	public MusicPlayerStatus GetTrackIndex (MusicTrack track, out int index);
```

Obsoleted methods:

```
[Obsolete ("Use overload with an out 'double beats'")]
	public MusicPlayerStatus BarBeatTimeToBeats (MonoTouch.CoreAnimation.CABarBeatTime barBeatTime);

	[Obsolete ("Use GetTrackIndex(MusicTrack, out int) to distinguish between the track or an error code")]
	public int GetTrackIndex (MusicTrack track);
```

### Type Changed: MonoTouch.AudioToolbox.MusicTrack

Added interface:

```
System.IDisposable
```

Removed method:

```
public void Dispose ();
```

Added method:

```
public virtual void Dispose ();
```

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioUnit

Added method:

```
public uint GetElementCount (AudioUnitScopeType scope);
```

### Type Changed: MonoTouch.AudioUnit.AUGraph

Added methods:

```
public AudioUnitStatus AddRenderNotify (RenderDelegate callback);
	public AudioUnitStatus RemoveRenderNotify (RenderDelegate callback);
	public AUGraphError SetNodeInputCallback (int destNode, uint destInputNumber, RenderDelegate renderDelegate);
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAssetImageGenerator

Obsoleted method:

```
[Obsolete ("Use the overload that takes NSValue[] instead")]
	public virtual void GenerateCGImagesAsynchronously (MonoTouch.Foundation.NSValue cmTimesRequestedTimes, AVAssetImageGeneratorCompletionHandler handler);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate

Added method:

```
public virtual void DidCancelLoadingRequest (AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate_Extensions

Added method:

```
public static void DidCancelLoadingRequest (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoadingRequest

Added properties:

```
public virtual AVAssetResourceLoadingContentInformationRequest ContentInformationRequest { get; }
	public virtual AVAssetResourceLoadingDataRequest DataRequest { get; }
	public virtual bool IsCancelled { get; }
	public virtual MonoTouch.Foundation.NSUrlRequest Redirect { get; set; }
	public virtual MonoTouch.Foundation.NSUrlResponse Response { get; set; }
```

Added method:

```
public virtual void FinishLoading ();
```

Obsoleted method:

```
[Obsolete ("Use instead the Response, Redirect properties and the AVAssetResourceLoadingDataRequest.Responds and AVAssetResourceLoadingRequest.FinishLoading methods")]
	public virtual void FinishLoading (MonoTouch.Foundation.NSUrlResponse usingResponse, MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSUrlRequest redirect);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureSession

Added property:

```
public static MonoTouch.Foundation.NSString Preset1920x1080 { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVError

Added value:

```
ApplicationIsNotAuthorizedToUseDevice = 11852,
```

### Type Changed: MonoTouch.AVFoundation.AVPlayerActionAtItemEnd

Added value:

```
Advance = 0,
```

### New Type MonoTouch.AVFoundation.AVAssetResourceLoadingContentInformationRequest

```
public class AVAssetResourceLoadingContentInformationRequest : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceLoadingContentInformationRequest ();
	public AVAssetResourceLoadingContentInformationRequest (MonoTouch.Foundation.NSCoder coder);
	public AVAssetResourceLoadingContentInformationRequest (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetResourceLoadingContentInformationRequest (System.IntPtr handle);
	// properties
	public virtual bool ByteRangeAccessSupported { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual long ContentLength { get; set; }
	public virtual string ContentType { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAssetResourceLoadingDataRequest

```
public class AVAssetResourceLoadingDataRequest : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceLoadingDataRequest ();
	public AVAssetResourceLoadingDataRequest (MonoTouch.Foundation.NSCoder coder);
	public AVAssetResourceLoadingDataRequest (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetResourceLoadingDataRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual long CurrentOffset { get; }
	public virtual int RequestedLength { get; }
	public virtual long RequestedOffset { get; }
	// methods
	public virtual void Respond (MonoTouch.Foundation.NSData responseData);
}
```

## Namespace MonoTouch.CoreAnimation

### Type Changed: MonoTouch.CoreAnimation.CAAnimation

Added properties:

```
public static MonoTouch.Foundation.NSString AnimationCubic { get; }
	public static MonoTouch.Foundation.NSString AnimationCubicPaced { get; }
```

### Type Changed: MonoTouch.CoreAnimation.CAFillMode

Removed fields:

```
public static const string Backwards = "backwards";
	public static const string Both = "both";
	public static const string Forwards = "forwards";
	public static const string Frozen = "frozen";
	public static const string Removed = "removed";
```

Added properties:

```
public static MonoTouch.Foundation.NSString Backwards { get; }
	public static MonoTouch.Foundation.NSString Both { get; }
	public static MonoTouch.Foundation.NSString Forwards { get; }
	public static MonoTouch.Foundation.NSString Frozen { get; }
	public static MonoTouch.Foundation.NSString Removed { get; }
```

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.PeripheralConnectionOptions

Added properties:

```
public bool? NotifyOnConnection { get; set; }
	public bool? NotifyOnDisconnection { get; set; }
	public bool? NotifyOnNotification { get; set; }
```

Obsoleted properties:

```
[Obsolete ("use NotifyOnConnection property instead")]
	public bool NotifyOnConnectionKey { set; }

	[Obsolete ("Use NotifyOnDisconnection property instead")]
	public bool NotifyOnDisconnectionKey { set; }

	[Obsolete ("use NotifyOnNotification property instead")]
	public bool NotifyOnNotificationKey { set; }
```

## Namespace MonoTouch.CoreData

### Type Changed: MonoTouch.CoreData.NSAttributeType

Added value:

```
ObjectID = 2000,
```

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFAllocator

Added method:

```
public static int GetTypeID ();
```

### Type Changed: MonoTouch.CoreFoundation.CFRunLoop

Removed fields:

```
public static const string ModeCommon = "kCFRunLoopCommonModes";
	public static const string ModeDefault = "kCFRunLoopDefaultMode";
```

Added properties:

```
public static MonoTouch.Foundation.NSString ModeCommon { get; }
	public static MonoTouch.Foundation.NSString ModeDefault { get; }
```

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGAffineTransform

Added methods:

```
public static CGAffineTransform Rotate (CGAffineTransform transform, float angle);
	public static CGAffineTransform Scale (CGAffineTransform transform, float sx, float sy);
	public static CGAffineTransform Translate (CGAffineTransform transform, float tx, float ty);
```

### Type Changed: MonoTouch.CoreGraphics.CGDataConsumer

Added constructor:

```
public CGDataConsumer (MonoTouch.Foundation.NSUrl url);
```

### Type Changed: MonoTouch.CoreGraphics.CGFont

Added method:

```
public MonoTouch.CoreText.CTFont ToCTFont (float size, CGAffineTransform matrix);
```

Obsoleted method:

```
[Obsolete ("Use ToCTFont(GCFloat,CGAffineTransform)")]
	public MonoTouch.CoreText.CTFont ToCTFont (float size, ref CGAffineTransform matrix);
```

### Type Changed: MonoTouch.CoreGraphics.CGPath

Removed methods:

```
public CGPath CopyByDashingPath (CGAffineTransform transform, float[] phase);
	public CGPath CopyByDashingPath (float[] phase);
```

Added methods:

```
public void AddEllipseInRect (System.Drawing.RectangleF rect);
	public CGPath CopyByDashingPath (float[] lengths, float phase);
	public CGPath CopyByDashingPath (CGAffineTransform transform, float[] lengths);
	public CGPath CopyByDashingPath (float[] lengths);
	public CGPath CopyByDashingPath (CGAffineTransform transform, float[] lengths, float phase);
	public static CGPath EllipseFromRect (System.Drawing.RectangleF boundingRect);
```

Obsoleted method:

```
[Obsolete ("Use AddEllipseInRect instead")]
	public void AddElipseInRect (System.Drawing.RectangleF rect);
```

### Type Changed: MonoTouch.CoreGraphics.CGPDFDictionary

Added method:

```
public void Apply (System.Action<System.String,MonoTouch.CoreGraphics.CGPDFObject> callback);
```

Obsoleted method:

```
[Obsolete ("Use the Apply(Action method")]
	public void Apply (System.Action<System.String,System.Object> callback);
```

### Type Changed: MonoTouch.CoreGraphics.CGPDFStream

Obsoleted property:

```
[Obsolete ("Use GetData(out CGPDFDataFormat) instead")]
	public MonoTouch.Foundation.NSData Data { get; }
```

Added method:

```
public MonoTouch.Foundation.NSData GetData (out CGPDFDataFormat format);
```

### New Type MonoTouch.CoreGraphics.CGPDFContentStream

```
public class CGPDFContentStream : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGPDFContentStream (System.IntPtr handle);
	public CGPDFContentStream (CGPDFPage page);
	public CGPDFContentStream (CGPDFStream stream, MonoTouch.Foundation.NSDictionary streamResources, CGPDFContentStream parent);
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CGPDFContentStream ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public CGPDFObject GetResource (string category, string name);
	public CGPDFStream[] GetStreams ();
}
```

### New Type MonoTouch.CoreGraphics.CGPDFDataFormat

```
[Serializable]
public enum CGPDFDataFormat {
	JPEG2000 = 2,
	JPEGEncoded = 1,
	Raw = 0,
}
```

### New Type MonoTouch.CoreGraphics.CGPDFObject

```
public class CGPDFObject : MonoTouch.ObjCRuntime.INativeObject {
	// constructors
	public CGPDFObject (System.IntPtr handle);
	// properties
	public virtual System.IntPtr Handle { get; }
	public bool IsNull { get; }
	public CGPDFObjectType Type { get; }
	// methods
	public bool TryGetName (out string name);
	public bool TryGetValue (out CGPDFStream value);
	public bool TryGetValue (out CGPDFDictionary value);
	public bool TryGetValue (out CGPDFArray value);
	public bool TryGetValue (out bool value);
	public bool TryGetValue (out float value);
	public bool TryGetValue (out int value);
	public bool TryGetValue (out string value);
}
```

### New Type MonoTouch.CoreGraphics.CGPDFObjectType

```
[Serializable]
public enum CGPDFObjectType {
	Array = 7,
	Boolean = 2,
	Dictionary = 8,
	Integer = 3,
	Name = 5,
	Null = 1,
	Real = 4,
	Stream = 9,
	String = 6,
}
```

### New Type MonoTouch.CoreGraphics.CGPDFOperatorTable

```
public class CGPDFOperatorTable : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGPDFOperatorTable ();
	public CGPDFOperatorTable (System.IntPtr handle);
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CGPDFOperatorTable ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public static CGPDFScanner GetScannerFromInfo (System.IntPtr gchandle);
	public void SetCallback (string name, System.Action<System.IntPtr,System.IntPtr> callback);
}
```

### New Type MonoTouch.CoreGraphics.CGPDFScanner

```
public class CGPDFScanner : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGPDFScanner (CGPDFContentStream cs, CGPDFOperatorTable table, object userInfo);
	public CGPDFScanner (System.IntPtr handle);
	// properties
	public virtual System.IntPtr Handle { get; }
	public object UserInfo { get; }
	// methods
	protected override void ~CGPDFScanner ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public CGPDFContentStream GetContentStream ();
	public bool Scan ();
	public bool TryPop (out CGPDFDictionary value);
	public bool TryPop (out CGPDFArray value);
	public bool TryPop (out string value);
	public bool TryPop (out float value);
	public bool TryPop (out int value);
	public bool TryPop (out bool value);
	public bool TryPop (out CGPDFObject value);
	public bool TryPop (out CGPDFStream value);
	public bool TryPopName (out string name);
}
```

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIAffineFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIBlendFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIBloom

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorClamp

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorControls

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorCrossPolynomial

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorCube

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorInvert

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorMap

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorMatrix

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorMonochrome

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIColorPosterize

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CICompositingFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIConvolutionCore

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CICrop

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIDistortionFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIExposureAdjust

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIFalseColor

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIFilter

Added property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIGammaAdjust

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIGaussianBlur

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIGloom

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIHighlightShadowAdjust

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIHueAdjust

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CILanczosScaleTransform

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CILightTunnel

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CILinearToSRGBToneCurve

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIMaskToAlpha

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIMaximumComponent

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIMinimumComponent

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIPerspectiveTile

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIPerspectiveTransform

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffect

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIPixellate

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIScreenFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CISepiaTone

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CISharpenLuminance

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CISRGBToneCurveToLinear

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIStarShineGenerator

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIStraightenFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CITemperatureAndTint

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CITileFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIToneCurve

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CITransitionFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CITriangleKaleidoscope

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIUnsharpMask

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIVibrance

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIVignette

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIVignetteEffect

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIWhitePointAdjust

Removed property:

```
public CIImage Image { get; set; }
```

## Namespace MonoTouch.CoreMedia

### Type Changed: MonoTouch.CoreMedia.CMMediaType

Removed value:

```
Metadata = 1953326452,
```

Added value:

```
Metadata = 1835365473,
```

Obsoleted field:

```
[Obsolete ("Use Metadata instead")]
	TimedMetadata = 1953326452,
```

## Namespace MonoTouch.CoreMidi

### Type Changed: MonoTouch.CoreMidi.MidiNetworkSession

Removed properties:

```
public virtual MidiEndpoint DestinationEndpoint { get; }
	public virtual MidiEndpoint SourceEndpoint { get; }
```

Added properties:

```
public MidiEndpoint DestinationEndPoint { get; }
	public MidiEndpoint SourceEndpoint { get; }
```

### Type Changed: MonoTouch.CoreMidi.MidiObject

Added constructor:

```
public MidiObject (int handle);
```

Obsoleted constructor:

```
[Obsolete ("Use the (int) overload instead")]
	public MidiObject (System.IntPtr handle);
```

### Type Changed: MonoTouch.CoreMidi.MidiPacket

Added interface:

```
System.IDisposable
```

Added method:

```
public virtual void Dispose ();
```

### Type Changed: MonoTouch.CoreMidi.MidiPacketsEventArgs

Added interface:

```
System.IDisposable
```

Added method:

```
public virtual void Dispose ();
```

## Namespace MonoTouch.CoreServices

### Type Changed: MonoTouch.CoreServices.CFHTTPStream

Added method:

```
public void SetProxy (MonoTouch.CoreFoundation.CFProxySettings proxySettings);
```

## Namespace MonoTouch.CoreText

### Type Changed: MonoTouch.CoreText.CTParagraphStyleSettings

Added property:

```
public CTLineBoundsOptions? LineBoundsOptions { get; set; }
```

## Namespace MonoTouch.CoreVideo

### Type Changed: MonoTouch.CoreVideo.CVPixelBuffer

Added constructors:

```
public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormat);
	public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, CVPixelBufferAttributes attributes);
```

Removed method:

```
public int GetWidthtOfPlane (int planeIndex);
```

Added methods:

```
public static int GetTypeID ();
	public int GetWidthOfPlane (int planeIndex);
```

### Type Changed: MonoTouch.CoreVideo.CVPixelBufferAttributes

Added constructor:

```
public CVPixelBufferAttributes (CVPixelFormatType pixelFormatType, int width, int height);
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.DictionaryContainer

Added methods:

```
protected int? GetNIntValue (NSString key);
	protected uint? GetNUIntValue (NSString key);
```

### Type Changed: MonoTouch.Foundation.ExportAttribute

Obsoleted constructor:

```
[Obsolete ("Every exported selector must include a name")]
	public ExportAttribute ();
```

### Type Changed: MonoTouch.Foundation.NSData

Added methods:

```
public bool Save (NSUrl url, NSDataWritingOptions options, out NSError error);
	public byte[] ToArray ();
```

### Type Changed: MonoTouch.Foundation.NSDecimal

Added methods:

```
public static double op_Explicit (NSDecimal value);
	public static float op_Explicit (NSDecimal value);
	public static System.Decimal op_Explicit (NSDecimal value);
	public static NSDecimal op_Implicit (System.Decimal value);
	public static NSDecimal op_Implicit (double value);
	public static NSDecimal op_Implicit (float value);
```

### Type Changed: MonoTouch.Foundation.NSDecimalNumber

Added interface:

```
System.IEquatable<NSNumber>
```

### Type Changed: MonoTouch.Foundation.NSMutableArray

Removed constructor:

```
public NSMutableArray (int capacity);
```

Added constructor:

```
public NSMutableArray (uint capacity);
```

### Type Changed: MonoTouch.Foundation.NSNumber

Added interface:

```
System.IEquatable<NSNumber>
```

Added properties:

```
public virtual int LongValue { get; }
	public float NFloatValue { get; }
	public virtual uint UnsignedLongValue { get; }
```

Added methods:

```
public virtual bool Equals (NSNumber other);
	public override bool Equals (object other);
	public static NSNumber FromLong (int value);
	public static NSNumber FromUnsignedLong (uint value);
	public override int GetHashCode ();
```

### Type Changed: MonoTouch.Foundation.NSObject

Removed method:

```
public virtual void PerformSelector (MonoTouch.ObjCRuntime.Selector sel, NSObject obj, double delay);
```

Added method:

```
public virtual void PerformSelector (MonoTouch.ObjCRuntime.Selector selector, NSObject withObject, double delay);
```

### Type Changed: MonoTouch.Foundation.NSPredicate

Added methods:

```
public static NSPredicate FromFormat (string predicateFormat);
	public static NSPredicate FromFormat (string predicateFormat, NSObject argument);
```

### Type Changed: MonoTouch.Foundation.NSStream

Added properties:

```
public NSData DataWrittenToMemoryStream { get; }
	public NSNumber FileCurrentOffset { get; }
	public NSStreamServiceType ServiceType { get; set; }
	public NSStreamSocketSecurityLevel SocketSecurityLevel { get; set; }
	public NSStreamSocksOptions SocksOptions { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSTimeZone

Added method:

```
public virtual string GetLocalizedName (NSTimeZoneNameStyle style, NSLocale locale);
```

### Type Changed: MonoTouch.Foundation.NSUnderlineStyle

Added values:

```
Double = 9,
	Thick = 2,
```

### Type Changed: MonoTouch.Foundation.NSWritingDirection

Removed value:

```
RightToLeft = -1,
```

Added value:

```
RightToLeft = 1,
```

### New Type MonoTouch.Foundation.NSStreamServiceType

```
[Serializable]
public enum NSStreamServiceType {
	Background = 3,
	Default = 0,
	Video = 2,
	Voice = 4,
	VoIP = 1,
}
```

### New Type MonoTouch.Foundation.NSStreamSocketSecurityLevel

```
[Serializable]
public enum NSStreamSocketSecurityLevel {
	NegotiatedSsl = 4,
	None = 0,
	SslV2 = 1,
	SslV3 = 2,
	TlsV1 = 3,
	Unknown = 5,
}
```

### New Type MonoTouch.Foundation.NSStreamSocksOptions

```
public class NSStreamSocksOptions {
	// constructors
	public NSStreamSocksOptions ();
	// fields
	public string HostName;
	public int HostPort;
	public string Password;
	public string Username;
	public int Version;
}
```

### New Type MonoTouch.Foundation.NSTimeZoneNameStyle

```
[Serializable]
public enum NSTimeZoneNameStyle {
	DaylightSaving = 2,
	Generic = 4,
	ShortDaylightSaving = 3,
	ShortGeneric = 5,
	ShortStandard = 1,
	Standard = 0,
}
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate

Added method:

```
public virtual void HandleInviteFromGameCenter (MonoTouch.Foundation.NSString[] playersToInvite);
```

Obsoleted method:

```
[Obsolete ("Use HandleInviteFromGameCenter(NSString[])")]
	public virtual void HandleInviteFromGameCenter (GKPlayer[] playersToInvite);
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate_Extensions

Added method:

```
public static void HandleInviteFromGameCenter (IGKTurnBasedEventHandlerDelegate This, MonoTouch.Foundation.NSString[] playersToInvite);
```

Obsoleted method:

```
[Obsolete ("Use HandleInviteFromGameCenter(NSString[])")]
	public static void HandleInviteFromGameCenter (IGKTurnBasedEventHandlerDelegate This, GKPlayer[] playersToInvite);
```

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.GLKit.GLKViewDrawableColorFormat

Added value:

```
SRGBA8888 = 2,
```

## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADBannerView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

## Namespace MonoTouch.ImageIO

### Type Changed: MonoTouch.ImageIO.CGImageDestination

Added method:

```
public static CGImageDestination Create (MonoTouch.CoreGraphics.CGDataConsumer consumer, string typeIdentifier, int imageCount, CGImageDestinationOptions options);
```

### Type Changed: MonoTouch.ImageIO.CGImageMetadata

Removed method:

```
public MonoTouch.Foundation.NSString GetTag (CGImageMetadata parent, MonoTouch.Foundation.NSString path);
```

Added method:

```
public CGImageMetadataTag GetTag (CGImageMetadata parent, MonoTouch.Foundation.NSString path);
```

### Type Changed: MonoTouch.ImageIO.CGImageSource

Added method:

```
public void UpdateDataProvider (MonoTouch.CoreGraphics.CGDataProvider provider, bool final);
```

Obsoleted method:

```
[Obsolete ("Use UpdateDataProvider(CGDataProvider,bool)")]
	public void UpdateDataProvider (MonoTouch.CoreGraphics.CGDataProvider provider);
```

## Namespace MonoTouch.JavaScriptCore

### New Type MonoTouch.JavaScriptCore.IJSExport

```
public interface IJSExport : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.JavaScriptCore.JSExport

```
public class JSExport : MonoTouch.Foundation.NSObject, IJSExport, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public JSExport ();
	public JSExport (MonoTouch.Foundation.NSCoder coder);
	public JSExport (MonoTouch.Foundation.NSObjectFlag t);
	public JSExport (System.IntPtr handle);
}
```

### New Type MonoTouch.JavaScriptCore.JSExport_Extensions

```
public static class JSExport_Extensions {
}
```

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.MapKit.MKCircleView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.MapKit.MKMapRect

Added field:

```
public static MKMapRect Null;
```

### Type Changed: MonoTouch.MapKit.MKMapView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.MapKit.MKOverlayView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.MapKit.MKPolygonView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.MapKit.MKPolylineView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMediaPlaylistProperty

Removed fields:

```
public static const string Name = "name";
	public static const string PersistentID = "playlistPersistentID";
	public static const string PlaylistAttributes = "playlistAttributes";
	public static const string SeedItems = "seedItems";
```

Added properties:

```
public static MonoTouch.Foundation.NSString Name { get; }
	public static MonoTouch.Foundation.NSString PersistentID { get; }
	public static MonoTouch.Foundation.NSString PlaylistAttributes { get; }
	public static MonoTouch.Foundation.NSString SeedItems { get; }
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaType

Added value:

```
AudioITunesU = 8,
```

### Type Changed: MonoTouch.MediaPlayer.MPMovieControlStyle

Removed value:

```
Default = 2,
```

Added value:

```
Default = 1,
```

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.AvailabilityAttribute

Added properties:

```
public Platform DeprecatedArchitecture { get; }
	public Platform DeprecatedVersion { get; }
	public Platform IntroducedArchitecture { get; }
	public Platform IntroducedVersion { get; }
	public Platform ObsoletedArchitecture { get; }
	public Platform ObsoletedVersion { get; }
```

### Type Changed: MonoTouch.ObjCRuntime.BlockLiteral

Added property:

```
public object Target { get; }
```

Added method:

```
public T GetDelegateForBlock<T> ();
```

### Type Changed: MonoTouch.ObjCRuntime.LionAttribute

Added constructor:

```
public LionAttribute (bool onlyOn64);
```

### Type Changed: MonoTouch.ObjCRuntime.MavericksAttribute

Added constructor:

```
public MavericksAttribute (bool onlyOn64);
```

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

```
public static bool bool_objc_msgSend_bool_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, int arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_bool_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_CMTimeRange_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1, System.IntPtr arg2, MonoTouch.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_Double_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, double arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_float_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, float arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_int_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, bool arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, MonoTouch.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7, ref System.IntPtr arg8);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static bool bool_objc_msgSend_ref_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_bool_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, int arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_bool_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_CMTimeRange_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1, System.IntPtr arg2, MonoTouch.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_Double_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, double arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_float_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, float arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_int_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, bool arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, MonoTouch.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7, ref System.IntPtr arg8);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static int int_objc_msgSend_IntPtr_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, int arg4, ref System.IntPtr arg5);
	public static int int_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static int int_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, int arg4, ref System.IntPtr arg5);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static int int_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_CMTime_out_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out MonoTouch.CoreMedia.CMTime arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_int_IntPtr_ref_NSRange_ref_NSRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, ref MonoTouch.Foundation.NSRange arg3, ref MonoTouch.Foundation.NSRange arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_IntPtr_out_Boolean_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, out bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_ref_NSPropertyListFormat_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref MonoTouch.Foundation.NSPropertyListFormat arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_out_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out uint arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_RectangleF_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.RectangleF arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoTouch.Foundation.NSRange arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoTouch.Foundation.NSRange arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_CMTime_out_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out MonoTouch.CoreMedia.CMTime arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_ref_NSRange_ref_NSRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, ref MonoTouch.Foundation.NSRange arg3, ref MonoTouch.Foundation.NSRange arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_IntPtr_out_Boolean_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, out bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_ref_NSPropertyListFormat_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref MonoTouch.Foundation.NSPropertyListFormat arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_out_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out uint arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_RectangleF_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.RectangleF arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoTouch.Foundation.NSRange arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoTouch.Foundation.NSRange arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static void RectangleF_objc_msgSend_stret_IntPtr_IntPtr_ref_IntPtr (out System.Drawing.RectangleF retval, System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static void RectangleF_objc_msgSendSuper_stret_IntPtr_IntPtr_ref_IntPtr (out System.Drawing.RectangleF retval, System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static uint UInt32_objc_msgSend_IntPtr_Int64_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, long arg2, uint arg3, ref System.IntPtr arg4);
	public static uint UInt32_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static uint UInt32_objc_msgSendSuper_IntPtr_Int64_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, long arg2, uint arg3, ref System.IntPtr arg4);
	public static uint UInt32_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static void void_objc_msgSend_IntPtr_int_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, System.IntPtr arg6);
	public static void void_objc_msgSend_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, double arg3);
	public static void void_objc_msgSend_IntPtr_IntPtr_SizeF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.SizeF arg3);
	public static void void_objc_msgSend_IntPtr_ref_RectangleF_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.Drawing.RectangleF arg2, ref System.IntPtr arg3);
	public static void void_objc_msgSendSuper_IntPtr_int_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, System.IntPtr arg6);
	public static void void_objc_msgSendSuper_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, double arg3);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_SizeF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.SizeF arg3);
	public static void void_objc_msgSendSuper_IntPtr_ref_RectangleF_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.Drawing.RectangleF arg2, ref System.IntPtr arg3);
```

### Type Changed: MonoTouch.ObjCRuntime.MountainLionAttribute

Added constructor:

```
public MountainLionAttribute (bool onlyOn64);
```

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added values:

```
iOS_8_0 = 524288,
	iOS_Arch = 1095216660480,
	iOS_Arch32 = 4294967296,
	iOS_Arch64 = 8589934592,
	iOS_Version = 16777215,
	Mac_10_0 = 2814749767106560,
	Mac_10_1 = 2815849278734336,
	Mac_10_2 = 2816948790362112,
	Mac_10_3 = 2818048301989888,
	Mac_10_4 = 2819147813617664,
	Mac_10_5 = 2820247325245440,
	Mac_Arch = 18374686479671623680,
	Mac_Arch32 = 72057594037927936,
	Mac_Arch64 = 144115188075855872,
	Mac_Version = 72057589742960640,
```

Obsoleted fields:

```
[Obsolete ("Use iOS_Version")]
	iOS = 4294967295,

	[Obsolete ("Use Mac_Version")]
	Mac = 18446744069414584320,
```

### Type Changed: MonoTouch.ObjCRuntime.PlatformHelper

Added methods:

```
public static int CompareIosVersion (Platform a, Platform b);
	public static int CompareMacVersion (Platform a, Platform b);
	public static Platform ToArch (Platform platform);
	public static Platform ToIosArch (Platform platform);
	public static Platform ToIosVersion (Platform platform);
	public static Platform ToMacArch (Platform platform);
	public static Platform ToMacVersion (Platform platform);
	public static Platform ToVersion (Platform platform);
```

Obsoleted methods:

```
[Obsolete ("UseCompareIosVersion")]
	public static int CompareIos (Platform a, Platform b);

	[Obsolete ("Use CompareMacVersion")]
	public static int CompareMac (Platform a, Platform b);

	[Obsolete ("Use ToIosVersion")]
	public static Platform ToIos (Platform platform);

	[Obsolete ("Use ToMacVersion")]
	public static Platform ToMac (Platform platform);
```

### New Type MonoTouch.ObjCRuntime.BaseWrapper

```
public abstract class BaseWrapper : INativeObject, System.IDisposable {
	// constructors
	public BaseWrapper (System.IntPtr handle, bool owns);
	// properties
	protected override System.IntPtr Handle { get; set; }
	// methods
	protected override void ~BaseWrapper ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
```

## Namespace MonoTouch.OpenGLES

### Type Changed: MonoTouch.OpenGLES.EAGLRenderingAPI

Added value:

```
OpenGLES3 = 3,
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecAccessible

Added value:

```
Invalid = -1,
```

### Type Changed: MonoTouch.Security.SecAuthenticationType

Added value:

```
Invalid = -1,
```

### Type Changed: MonoTouch.Security.SecKey

Removed methods:

```
public SecStatusCode Decrypt (SecPadding padding, System.IntPtr cipherText, int cipherLen, System.IntPtr plainText, int playLen);
	public SecStatusCode Encrypt (SecPadding padding, System.IntPtr plainText, int playLen, System.IntPtr cipherText, int cipherLen);
```

Added methods:

```
[Obsolete ("Use the Decrypt overload which returns (ref) the plainTextLen value so you can adjust it if needed")]
	public SecStatusCode Decrypt (SecPadding padding, System.IntPtr cipherText, int cipherTextLen, System.IntPtr plainText, int plainTextLen);
	public SecStatusCode Decrypt (SecPadding padding, byte[] cipherText, out byte[] plainText);
	public SecStatusCode Decrypt (SecPadding padding, System.IntPtr cipherText, int cipherTextLen, System.IntPtr plainText, ref int plainTextLen);
	public SecStatusCode Encrypt (SecPadding padding, System.IntPtr plainText, int plainTextLen, System.IntPtr cipherText, ref int cipherTextLen);

	[Obsolete ("Use the Encrypt overload which returns (out) the cipherTextLen value so you can adjust it if needed")]
	public SecStatusCode Encrypt (SecPadding padding, System.IntPtr plainText, int plainTextLen, System.IntPtr cipherText, int cipherTextLen);
	public SecStatusCode RawSign (SecPadding padding, byte[] dataToSign, out byte[] result);
	public SecStatusCode RawSign (SecPadding padding, System.IntPtr dataToSign, int dataToSignLen, out byte[] result);
```

Obsoleted method:

```
[Obsolete ("Use the Decrypt overload which returns (out) the plainText array so you can adjust it if needed")]
	public SecStatusCode Decrypt (SecPadding padding, byte[] cipherText, byte[] plainText);
```

### Type Changed: MonoTouch.Security.SecKeyClass

Added value:

```
Invalid = -1,
```

### Type Changed: MonoTouch.Security.SecKeyType

Added value:

```
Invalid = -1,
```

### Type Changed: MonoTouch.Security.SecProtocol

Added value:

```
Invalid = -1,
```

### Type Changed: MonoTouch.Security.SecRecord

Added method:

```
public MonoTouch.Foundation.NSDictionary ToDictionary ();
```

### Type Changed: MonoTouch.Security.SslProtocol

Added value:

```
Ssl_3_0 = 2,
```

Obsoleted field:

```
[Obsolete ("Use Ssl_3_0")]
	Ssl3_0 = 2,
```

### New Type MonoTouch.Security.SslAuthenticate

```
[Serializable]
public enum SslAuthenticate {
	Always = 1,
	Never = 0,
	Try = 2,
}
```

### New Type MonoTouch.Security.SslCipherSuite

```
[Serializable]
public enum SslCipherSuite {
	SSL_DH_anon_EXPORT_WITH_RC4_40_MD5 = 23,
	SSL_DH_anon_WITH_3DES_EDE_CBC_SHA = 27,
	SSL_DH_anon_WITH_RC4_128_MD5 = 24,
	SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA = 22,
	SSL_NULL_WITH_NULL_NULL = 0,
	SSL_RSA_EXPORT_WITH_RC4_40_MD5 = 3,
	SSL_RSA_WITH_3DES_EDE_CBC_SHA = 10,
	SSL_RSA_WITH_NULL_MD5 = 1,
	SSL_RSA_WITH_NULL_SHA = 2,
	SSL_RSA_WITH_RC4_128_MD5 = 4,
	SSL_RSA_WITH_RC4_128_SHA = 5,
	TLS_DH_anon_WITH_3DES_EDE_CBC_SHA = 27,
	TLS_DH_anon_WITH_AES_128_CBC_SHA = 52,
	TLS_DH_anon_WITH_AES_128_CBC_SHA256 = 108,
	TLS_DH_anon_WITH_AES_128_GCM_SHA256 = 166,
	TLS_DH_anon_WITH_AES_256_CBC_SHA = 58,
	TLS_DH_anon_WITH_AES_256_CBC_SHA256 = 109,
	TLS_DH_anon_WITH_AES_256_GCM_SHA384 = 167,
	TLS_DH_anon_WITH_RC4_128_MD5 = 24,
	TLS_DHE_RSA_WITH_3DES_EDE_CBC_SHA = 22,
	TLS_DHE_RSA_WITH_AES_128_CBC_SHA = 51,
	TLS_DHE_RSA_WITH_AES_128_CBC_SHA256 = 103,
	TLS_DHE_RSA_WITH_AES_256_CBC_SHA = 57,
	TLS_DHE_RSA_WITH_AES_256_CBC_SHA256 = 107,
	TLS_ECDH_ECDSA_WITH_3DES_EDE_CBC_SHA = 49155,
	TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA = 49156,
	TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA256 = 49189,
	TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA = 49157,
	TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA384 = 49190,
	TLS_ECDH_ECDSA_WITH_NULL_SHA = 49153,
	TLS_ECDH_ECDSA_WITH_RC4_128_SHA = 49154,
	TLS_ECDH_RSA_WITH_3DES_EDE_CBC_SHA = 49165,
	TLS_ECDH_RSA_WITH_AES_128_CBC_SHA = 49166,
	TLS_ECDH_RSA_WITH_AES_128_CBC_SHA256 = 49193,
	TLS_ECDH_RSA_WITH_AES_256_CBC_SHA = 49167,
	TLS_ECDH_RSA_WITH_AES_256_CBC_SHA384 = 49194,
	TLS_ECDH_RSA_WITH_NULL_SHA = 49163,
	TLS_ECDH_RSA_WITH_RC4_128_SHA = 49164,
	TLS_ECDHE_ECDSA_WITH_3DES_EDE_CBC_SHA = 49160,
	TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA = 49161,
	TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256 = 49187,
	TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA = 49162,
	TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384 = 49188,
	TLS_ECDHE_ECDSA_WITH_NULL_SHA = 49158,
	TLS_ECDHE_ECDSA_WITH_RC4_128_SHA = 49159,
	TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA = 49170,
	TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA = 49171,
	TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 = 49191,
	TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA = 49172,
	TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 = 49192,
	TLS_ECDHE_RSA_WITH_NULL_SHA = 49168,
	TLS_ECDHE_RSA_WITH_RC4_128_SHA = 49169,
	TLS_NULL_WITH_NULL_NULL = 0,
	TLS_PSK_WITH_3DES_EDE_CBC_SHA = 139,
	TLS_PSK_WITH_AES_128_CBC_SHA = 140,
	TLS_PSK_WITH_AES_128_CBC_SHA256 = 174,
	TLS_PSK_WITH_AES_256_CBC_SHA = 141,
	TLS_PSK_WITH_AES_256_CBC_SHA384 = 175,
	TLS_PSK_WITH_NULL_SHA = 44,
	TLS_PSK_WITH_NULL_SHA256 = 176,
	TLS_PSK_WITH_NULL_SHA384 = 177,
	TLS_PSK_WITH_RC4_128_SHA = 138,
	TLS_RSA_WITH_3DES_EDE_CBC_SHA = 10,
	TLS_RSA_WITH_AES_128_CBC_SHA = 47,
	TLS_RSA_WITH_AES_128_CBC_SHA256 = 60,
	TLS_RSA_WITH_AES_256_CBC_SHA = 53,
	TLS_RSA_WITH_AES_256_CBC_SHA256 = 61,
	TLS_RSA_WITH_NULL_MD5 = 1,
	TLS_RSA_WITH_NULL_SHA = 2,
	TLS_RSA_WITH_NULL_SHA256 = 59,
	TLS_RSA_WITH_RC4_128_MD5 = 4,
	TLS_RSA_WITH_RC4_128_SHA = 5,
}
```

### New Type MonoTouch.Security.SslClientCertificateState

```
[Serializable]
public enum SslClientCertificateState {
	None = 0,
	Rejected = 3,
	Requested = 1,
	Sent = 2,
}
```

### New Type MonoTouch.Security.SslConnection

```
public abstract class SslConnection : System.IDisposable {
	// constructors
	protected SslConnection ();
	// properties
	public System.IntPtr ConnectionId { get; }
	// methods
	protected override void ~SslConnection ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public virtual SslStatus Read (System.IntPtr data, ref int dataLength);
	public virtual SslStatus Write (System.IntPtr data, ref int dataLength);
}
```

### New Type MonoTouch.Security.SslConnectionType

```
[Serializable]
public enum SslConnectionType {
	Datagram = 1,
	Stream = 0,
}
```

### New Type MonoTouch.Security.SslContext

```
public class SslContext : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SslContext (SslProtocolSide protocolSide, SslConnectionType connectionType);
	// properties
	public int BufferedReadSize { get; }
	public SslClientCertificateState ClientCertificateState { get; }
	public SslConnection Connection { get; set; }
	public int DatagramWriteSize { get; }
	public virtual System.IntPtr Handle { get; }
	public int MaxDatagramRecordSize { get; set; }
	public SslProtocol MaxProtocol { get; set; }
	public SslProtocol MinProtocol { get; set; }
	public SslCipherSuite NegotiatedCipher { get; }
	public SslProtocol NegotiatedProtocol { get; }
	public string PeerDomainName { get; set; }
	public byte[] PeerId { get; set; }
	public SecTrust PeerTrust { get; }
	public SslSessionState SessionState { get; }
	// methods
	protected override void ~SslContext ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public System.Collections.Generic.IList<SslCipherSuite> GetEnabledCiphers ();
	public SslStatus GetLastStatus ();
	public SslStatus GetSessionOption (SslSessionOption option, out bool value);
	public System.Collections.Generic.IList<SslCipherSuite> GetSupportedCiphers ();
	public static System.IntPtr GetTypeId ();
	public SslStatus Handshake ();
	public SslStatus Read (byte[] data, out int processed);
	public SslStatus SetCertificate (SecIdentity identify, System.Collections.Generic.IEnumerable<SecCertificate> certificates);
	public SslStatus SetClientSideAuthenticate (SslAuthenticate auth);
	public SslStatus SetDatagramHelloCookie (byte[] cookie);
	public SslStatus SetEnabledCiphers (System.Collections.Generic.IEnumerable<SslCipherSuite> ciphers);
	public SslStatus SetEncryptionCertificate (SecIdentity identify, System.Collections.Generic.IEnumerable<SecCertificate> certificates);
	public SslStatus SetSessionOption (SslSessionOption option, bool value);
	public SslStatus Write (byte[] data, out int processed);
}
```

### New Type MonoTouch.Security.SslProtocolSide

```
[Serializable]
public enum SslProtocolSide {
	Client = 1,
	Server = 0,
}
```

### New Type MonoTouch.Security.SslSessionOption

```
[Serializable]
public enum SslSessionOption {
	BreakOnCertRequested = 1,
	BreakOnClientAuth = 2,
	BreakOnServerAuth = 0,
	FalseStart = 3,
	SendOneByteRecord = 4,
}
```

### New Type MonoTouch.Security.SslSessionState

```
[Serializable]
public enum SslSessionState {
	Aborted = 4,
	Closed = 3,
	Connected = 2,
	Handshake = 1,
	Idle = 0,
	Invalid = -1,
}
```

### New Type MonoTouch.Security.SslStatus

```
[Serializable]
public enum SslStatus {
	BadCert = -9808,
	BadCipherSuite = -9818,
	BadConfiguration = -9848,
	BadRecordMac = -9846,
	BufferOverflow = -9817,
	CertExpired = -9814,
	CertNotYetValid = -9815,
	ClosedAbort = -9806,
	ClosedGraceful = -9805,
	ClosedNotNotified = -9816,
	ConnectionRefused = -9844,
	Crypto = -9809,
	DecryptionFail = -9845,
	FatalAlert = -9802,
	HostNameMismatch = -9843,
	IllegalParam = -9830,
	Internal = -9810,
	ModuleAttach = -9811,
	Negotiation = -9801,
	NoRootCert = -9813,
	PeerAccessDenied = -9832,
	PeerAuthCompleted = -9841,
	PeerBadCert = -9825,
	PeerBadRecordMac = -9820,
	PeerCertExpired = -9828,
	PeerCertRevoked = -9827,
	PeerCertUnknown = -9829,
	PeerClientCertRequested = -9842,
	PeerDecodeError = -9833,
	PeerDecompressFail = -9823,
	PeerDecryptError = -9834,
	PeerDecryptionFail = -9821,
	PeerExportRestriction = -9835,
	PeerHandshakeFail = -9824,
	PeerInsufficientSecurity = -9837,
	PeerInternalError = -9838,
	PeerNoRenegotiation = -9840,
	PeerProtocolVersion = -9836,
	PeerRecordOverflow = -9822,
	PeerUnexpectedMsg = -9819,
	PeerUnknownCA = -9831,
	PeerUnsupportedCert = -9826,
	PeerUserCancelled = -9839,
	Protocol = -9800,
	RecordOverflow = -9847,
	SessionNotFound = -9804,
	Success = 0,
	UnexpectedRecord = -9849,
	UnknownRootCert = -9812,
	WouldBlock = -9803,
	XCertChainInvalid = -9807,
}
```

### New Type MonoTouch.Security.SslStreamConnection

```
public class SslStreamConnection : MonoTouch.Security.SslConnection, System.IDisposable {
	// constructors
	public SslStreamConnection (System.IO.Stream stream);
	// properties
	public System.IO.Stream InnerStream { get; }
	// methods
	public override SslStatus Read (System.IntPtr data, ref int dataLength);
	public override SslStatus Write (System.IntPtr data, ref int dataLength);
}
```

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.NSLayoutManagerDelegate

Removed method:

```
public virtual void DidChangeGeometry (NSLayoutManager layoutManager, NSTextContainer textContainer, float oldSize);
```

Added method:

```
public virtual void DidChangeGeometry (NSLayoutManager layoutManager, NSTextContainer textContainer, System.Drawing.SizeF oldSize);
```

### Type Changed: MonoTouch.UIKit.NSLayoutManagerDelegate_Extensions

Removed method:

```
public static void DidChangeGeometry (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSTextContainer textContainer, float oldSize);
```

Added method:

```
public static void DidChangeGeometry (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSTextContainer textContainer, System.Drawing.SizeF oldSize);
```

### Type Changed: MonoTouch.UIKit.UIActionSheet

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIAlertView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIApplication

Added method:

```
public static void Main (string[] args, System.Type principalClass, System.Type delegateClass);
```

### Type Changed: MonoTouch.UIKit.UIButton

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UICollectionView

Added interface:

```
IUIAccessibilityIdentification
```

Removed method:

```
protected virtual void RegisterNibForSupplementaryView (UINib nib, MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSString reuseIdentifier);
```

Added methods:

```
public void RegisterClassForSupplementaryView (System.Type cellType, MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSString reuseIdentifier);
	public virtual void RegisterNibForSupplementaryView (UINib nib, MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSString reuseIdentifier);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIContentSizeCategory

Added value:

```
ExtraExtraExtraLarge = 6,
```

### Type Changed: MonoTouch.UIKit.UIControl

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIDatePicker

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIImageView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIInputView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UILabel

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UINavigationBar

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIPageControl

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIPickerView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIProgressView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIScrollView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UISearchBar

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UISlider

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIStepper

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UISwitch

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UITabBar

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UITableView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UITableViewCell

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UITextField

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UITextView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIToolbar

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIView

Added interface:

```
IUIAccessibilityIdentification
```

Added property:

```
public virtual string AccessibilityIdentifier { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIWebView

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIWindow

Added interface:

```
IUIAccessibilityIdentification
```

Obsoleted fields:

```
[Obsolete ("Use UIWindowLevel.Alert")]
	public static const float LevelAlert;

	[Obsolete ("Use UIWindowLevel.Normal")]
	public static const float LevelNormal;

	[Obsolete ("Use UIWindowLevel.StatusBar")]
	public static const float LevelStatusBar;
```

### New Type MonoTouch.UIKit.IUIAccessibilityIdentification

```
public interface IUIAccessibilityIdentification : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual string AccessibilityIdentifier { get; set; }
}
```

### New Type MonoTouch.UIKit.IUIInputViewAudioFeedback

```
public interface IUIInputViewAudioFeedback : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual bool EnableInputClicksWhenVisible { get; }
}
```

### New Type MonoTouch.UIKit.UIAccessibilityIdentification_Extensions

```
public static class UIAccessibilityIdentification_Extensions {
}
```

### New Type MonoTouch.UIKit.UIInputViewAudioFeedback_Extensions

```
public static class UIInputViewAudioFeedback_Extensions {
}
```

## Namespace OpenTK

### Type Changed: OpenTK.MathHelper

Added methods:

```
public static double DegreesToRadians (double degrees);
	public static double RadiansToDegrees (double radians);
```

### Type Changed: OpenTK.Matrix4

Added method:

```
public void Invert (ref Matrix4 result);
```

### Type Changed: OpenTK.Matrix4d

Added method:

```
public void Invert (ref Matrix4d result);
```

### Type Changed: OpenTK.Vector2

Added constructor:

```
public Vector2 (float value);
```

### Type Changed: OpenTK.Vector2d

Added constructor:

```
public Vector2d (double value);
```

### Type Changed: OpenTK.Vector2h

Added constructors:

```
public Vector2h (Half value);
	public Vector2h (float value);
```

### Type Changed: OpenTK.Vector3

Added constructor:

```
public Vector3 (float value);
```

### Type Changed: OpenTK.Vector3d

Added constructor:

```
public Vector3d (double value);
```

### Type Changed: OpenTK.Vector3h

Added constructors:

```
public Vector3h (Half value);
	public Vector3h (float value);
```

### Type Changed: OpenTK.Vector4

Added constructor:

```
public Vector4 (float value);
```

### Type Changed: OpenTK.Vector4d

Added constructor:

```
public Vector4d (double value);
```

### Type Changed: OpenTK.Vector4h

Added constructors:

```
public Vector4h (Half value);
	public Vector4h (float value);
```

   


 <hr>

# MonoTouch.Dialog-1.dll

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement.TextWithImageCellView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.Dialog.GlassButton

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.Dialog.MessageSummaryView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.Dialog.RefreshTableHeaderView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

   


 <hr>

# OpenTK.dll

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

## Removed Namespace System.ComponentModel

### Removed Type System.ComponentModel.CancelEventArgs    
 <hr>

# OpenTK-1.0.dll

## Namespace OpenTK

### Type Changed: OpenTK.Configuration

Added property:

```
public static bool RunningOnAndroid { get; }
```

## Namespace OpenTK.Audio.OpenAL

### Type Changed: OpenTK.Audio.OpenAL.AL

Added methods:

```
public static void DeleteBuffers (int n, int* buffers);
	public static void GenBuffers (int n, int* buffers);
```

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.ColorFormat

Added interface:

```
System.IComparable<ColorFormat>
```

Added field:

```
public static ColorFormat Empty;
```

Added methods:

```
public virtual int CompareTo (ColorFormat other);
	public static bool op_GreaterThan (ColorFormat left, ColorFormat right);
	public static bool op_GreaterThanOrEqual (ColorFormat left, ColorFormat right);
	public static bool op_LessThan (ColorFormat left, ColorFormat right);
	public static bool op_LessThanOrEqual (ColorFormat left, ColorFormat right);
```

### Type Changed: OpenTK.Graphics.GraphicsContext

Added property:

```
public virtual int SwapInterval { get; set; }
```

Obsoleted property:

```
[Obsolete ("Use SwapInterval property instead.")]
	public virtual bool VSync { get; set; }
```

Added methods:

```
public override bool Equals (object obj);
	public override int GetHashCode ();
	public override string ToString ();
```

### Type Changed: OpenTK.Graphics.IGraphicsContext

Added property:

```
public virtual int SwapInterval { get; set; }
```

Obsoleted property:

```
[Obsolete ("Use SwapInterval property instead.")]
	public virtual bool VSync { get; set; }
```

### New Type OpenTK.Graphics.Color4

```
[Serializable]
public struct Color4, System.IEquatable<Color4> {
	// constructors
	public Color4 (float r, float g, float b, float a);
	public Color4 (byte r, byte g, byte b, byte a);

	[Obsolete ("Use new Color4(r, g, b, a) instead.")]
	public Color4 (System.Drawing.Color color);
	// fields
	public float A;
	public float B;
	public float G;
	public float R;
	// properties
	public static Color4 AliceBlue { get; }
	public static Color4 AntiqueWhite { get; }
	public static Color4 Aqua { get; }
	public static Color4 Aquamarine { get; }
	public static Color4 Azure { get; }
	public static Color4 Beige { get; }
	public static Color4 Bisque { get; }
	public static Color4 Black { get; }
	public static Color4 BlanchedAlmond { get; }
	public static Color4 Blue { get; }
	public static Color4 BlueViolet { get; }
	public static Color4 Brown { get; }
	public static Color4 BurlyWood { get; }
	public static Color4 CadetBlue { get; }
	public static Color4 Chartreuse { get; }
	public static Color4 Chocolate { get; }
	public static Color4 Coral { get; }
	public static Color4 CornflowerBlue { get; }
	public static Color4 Cornsilk { get; }
	public static Color4 Crimson { get; }
	public static Color4 Cyan { get; }
	public static Color4 DarkBlue { get; }
	public static Color4 DarkCyan { get; }
	public static Color4 DarkGoldenrod { get; }
	public static Color4 DarkGray { get; }
	public static Color4 DarkGreen { get; }
	public static Color4 DarkKhaki { get; }
	public static Color4 DarkMagenta { get; }
	public static Color4 DarkOliveGreen { get; }
	public static Color4 DarkOrange { get; }
	public static Color4 DarkOrchid { get; }
	public static Color4 DarkRed { get; }
	public static Color4 DarkSalmon { get; }
	public static Color4 DarkSeaGreen { get; }
	public static Color4 DarkSlateBlue { get; }
	public static Color4 DarkSlateGray { get; }
	public static Color4 DarkTurquoise { get; }
	public static Color4 DarkViolet { get; }
	public static Color4 DeepPink { get; }
	public static Color4 DeepSkyBlue { get; }
	public static Color4 DimGray { get; }
	public static Color4 DodgerBlue { get; }
	public static Color4 Firebrick { get; }
	public static Color4 FloralWhite { get; }
	public static Color4 ForestGreen { get; }
	public static Color4 Fuchsia { get; }
	public static Color4 Gainsboro { get; }
	public static Color4 GhostWhite { get; }
	public static Color4 Gold { get; }
	public static Color4 Goldenrod { get; }
	public static Color4 Gray { get; }
	public static Color4 Green { get; }
	public static Color4 GreenYellow { get; }
	public static Color4 Honeydew { get; }
	public static Color4 HotPink { get; }
	public static Color4 IndianRed { get; }
	public static Color4 Indigo { get; }
	public static Color4 Ivory { get; }
	public static Color4 Khaki { get; }
	public static Color4 Lavender { get; }
	public static Color4 LavenderBlush { get; }
	public static Color4 LawnGreen { get; }
	public static Color4 LemonChiffon { get; }
	public static Color4 LightBlue { get; }
	public static Color4 LightCoral { get; }
	public static Color4 LightCyan { get; }
	public static Color4 LightGoldenrodYellow { get; }
	public static Color4 LightGray { get; }
	public static Color4 LightGreen { get; }
	public static Color4 LightPink { get; }
	public static Color4 LightSalmon { get; }
	public static Color4 LightSeaGreen { get; }
	public static Color4 LightSkyBlue { get; }
	public static Color4 LightSlateGray { get; }
	public static Color4 LightSteelBlue { get; }
	public static Color4 LightYellow { get; }
	public static Color4 Lime { get; }
	public static Color4 LimeGreen { get; }
	public static Color4 Linen { get; }
	public static Color4 Magenta { get; }
	public static Color4 Maroon { get; }
	public static Color4 MediumAquamarine { get; }
	public static Color4 MediumBlue { get; }
	public static Color4 MediumOrchid { get; }
	public static Color4 MediumPurple { get; }
	public static Color4 MediumSeaGreen { get; }
	public static Color4 MediumSlateBlue { get; }
	public static Color4 MediumSpringGreen { get; }
	public static Color4 MediumTurquoise { get; }
	public static Color4 MediumVioletRed { get; }
	public static Color4 MidnightBlue { get; }
	public static Color4 MintCream { get; }
	public static Color4 MistyRose { get; }
	public static Color4 Moccasin { get; }
	public static Color4 NavajoWhite { get; }
	public static Color4 Navy { get; }
	public static Color4 OldLace { get; }
	public static Color4 Olive { get; }
	public static Color4 OliveDrab { get; }
	public static Color4 Orange { get; }
	public static Color4 OrangeRed { get; }
	public static Color4 Orchid { get; }
	public static Color4 PaleGoldenrod { get; }
	public static Color4 PaleGreen { get; }
	public static Color4 PaleTurquoise { get; }
	public static Color4 PaleVioletRed { get; }
	public static Color4 PapayaWhip { get; }
	public static Color4 PeachPuff { get; }
	public static Color4 Peru { get; }
	public static Color4 Pink { get; }
	public static Color4 Plum { get; }
	public static Color4 PowderBlue { get; }
	public static Color4 Purple { get; }
	public static Color4 Red { get; }
	public static Color4 RosyBrown { get; }
	public static Color4 RoyalBlue { get; }
	public static Color4 SaddleBrown { get; }
	public static Color4 Salmon { get; }
	public static Color4 SandyBrown { get; }
	public static Color4 SeaGreen { get; }
	public static Color4 SeaShell { get; }
	public static Color4 Sienna { get; }
	public static Color4 Silver { get; }
	public static Color4 SkyBlue { get; }
	public static Color4 SlateBlue { get; }
	public static Color4 SlateGray { get; }
	public static Color4 Snow { get; }
	public static Color4 SpringGreen { get; }
	public static Color4 SteelBlue { get; }
	public static Color4 Tan { get; }
	public static Color4 Teal { get; }
	public static Color4 Thistle { get; }
	public static Color4 Tomato { get; }
	public static Color4 Transparent { get; }
	public static Color4 Turquoise { get; }
	public static Color4 Violet { get; }
	public static Color4 Wheat { get; }
	public static Color4 White { get; }
	public static Color4 WhiteSmoke { get; }
	public static Color4 Yellow { get; }
	public static Color4 YellowGreen { get; }
	// methods
	public virtual bool Equals (Color4 other);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (Color4 left, Color4 right);
	public static System.Drawing.Color op_Explicit (Color4 color);
	public static Color4 op_Implicit (System.Drawing.Color color);
	public static bool op_Inequality (Color4 left, Color4 right);
	public int ToArgb ();
	public override string ToString ();
}
```

## Namespace OpenTK.Graphics.ES11

### Type Changed: OpenTK.Graphics.ES11.All

Added values:

```
Alpha8Ext = 32828,
	AppleCopyTextureLevels = 1,
	Bgra8Ext = 37793,
	ExtMapBufferRange = 1,
	ExtTextureStorage = 1,
	Luminance8Alpha8Ext = 32837,
	Luminance8Ext = 32832,
	MapFlushExplicitBitExt = 16,
	MapInvalidateBufferBitExt = 8,
	MapInvalidateRangeBitExt = 4,
	MapReadBitExt = 1,
	MapUnsynchronizedBitExt = 32,
	MapWriteBitExt = 2,
	TextureImmutableFormatExt = 37167,
	UnsignedShort1555Rev = 33638,
```

### Type Changed: OpenTK.Graphics.ES11.GL

Added field:

```
public static const string Library = "libGLES.dll";
```

Added method:

```
public static void Clear (ClearBufferMask mask);
```

Obsoleted methods:

```
[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Clear (int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Clear (uint mask);
```

### Type Changed: OpenTK.Graphics.ES11.GL.Apple

Added methods:

```
public static void CopyTextureLevel (int destinationTexture, int sourceTexture, int sourceBaseLevel, int sourceLevelCount);
	public static void CopyTextureLevel (uint destinationTexture, uint sourceTexture, int sourceBaseLevel, int sourceLevelCount);
```

### Type Changed: OpenTK.Graphics.ES11.GL.Ext

Added methods:

```
public static void FlushMappedBufferRange (All target, System.IntPtr offset, System.IntPtr length);
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, int access);
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, uint access);
	public static void TexStorage2D (All target, int levels, All internalformat, int width, int height);
```

### Type Changed: OpenTK.Graphics.ES11.Unknown

Added values:

```
Alpha8Ext = 32828,
	AppleCopyTextureLevels = 1,
	Bgra8Ext = 37793,
	ExtMapBufferRange = 1,
	ExtTextureStorage = 1,
	Luminance8Alpha8Ext = 32837,
	Luminance8Ext = 32832,
	MapFlushExplicitBitExt = 16,
	MapInvalidateBufferBitExt = 8,
	MapInvalidateRangeBitExt = 4,
	MapReadBitExt = 1,
	MapUnsynchronizedBitExt = 32,
	MapWriteBitExt = 2,
	TextureImmutableFormatExt = 37167,
	UnsignedShort1555Rev = 33638,
```

### New Type OpenTK.Graphics.ES11.OesDrawTexture

```
[Serializable]
public enum OesDrawTexture {
	TextureCropRectOes = 35741,
}
```

### New Type OpenTK.Graphics.ES11.OesMatrixGet

```
[Serializable]
public enum OesMatrixGet {
	ModelviewMatrixFloatAsIntBitsOes = 35213,
	ProjectionMatrixFloatAsIntBitsOes = 35214,
	TextureMatrixFloatAsIntBitsOes = 35215,
}
```

### New Type OpenTK.Graphics.ES11.OesMatrixPalette

```
[Serializable]
public enum OesMatrixPalette {
	CurrentPaletteMatrixOes = 34883,
	MatrixIndexArrayBufferBindingOes = 35742,
	MatrixIndexArrayOes = 34884,
	MatrixIndexArrayPointerOes = 34889,
	MatrixIndexArraySizeOes = 34886,
	MatrixIndexArrayStrideOes = 34888,
	MatrixIndexArrayTypeOes = 34887,
	MatrixPaletteOes = 34880,
	MaxPaletteMatricesOes = 34882,
	MaxVertexUnitsOes = 34468,
	WeightArrayBufferBindingOes = 34974,
	WeightArrayOes = 34477,
	WeightArrayPointerOes = 34476,
	WeightArraySizeOes = 34475,
	WeightArrayStrideOes = 34474,
	WeightArrayTypeOes = 34473,
}
```

### New Type OpenTK.Graphics.ES11.OesPointSizeArray

```
[Serializable]
public enum OesPointSizeArray {
	PointSizeArrayBufferBindingOes = 35743,
	PointSizeArrayOes = 35740,
	PointSizeArrayPointerOes = 35212,
	PointSizeArrayStrideOes = 35211,
	PointSizeArrayTypeOes = 35210,
}
```

### New Type OpenTK.Graphics.ES11.OesPointSprite

```
[Serializable]
public enum OesPointSprite {
	CoordReplaceOes = 34914,
	PointSpriteOes = 34913,
}
```

### New Type OpenTK.Graphics.ES11.OpenGlEsCoreVersions

```
[Serializable]
public enum OpenGlEsCoreVersions {
	VersionEsCl10 = 1,
	VersionEsCl11 = 1,
	VersionEsCm10 = 1,
	VersionEsCm11 = 1,
}
```

## Namespace OpenTK.Graphics.ES20

### Type Changed: OpenTK.Graphics.ES20.All

Added values:

```
Alpha16fExt = 34844,
	Alpha32fExt = 34838,
	Alpha8Ext = 32828,
	AlreadySignaledApple = 37146,
	AppleCopyTextureLevels = 1,
	AppleSync = 1,
	Bgra8Ext = 37793,
	CompressedSrgbAlphaPvrtc2Bppv1Ext = 35414,
	CompressedSrgbAlphaPvrtc4Bppv1Ext = 35415,
	CompressedSrgbPvrtc2Bppv1Ext = 35412,
	CompressedSrgbPvrtc4Bppv1Ext = 35413,
	ConditionSatisfiedApple = 37148,
	DepthComponent32Oes = 33191,
	ExtDrawInstanced = 1,
	ExtInstancedArrays = 1,
	ExtMapBufferRange = 1,
	ExtPvrtcSrgb = 1,
	ExtShaderFramebufferFetch = 1,
	ExtSrgb = 1,
	ExtTextureStorage = 1,
	FragmentShaderDiscardsSamplesExt = 35410,
	FramebufferAttachmentColorEncodingExt = 33296,
	Luminance16fExt = 34846,
	Luminance32fExt = 34840,
	Luminance8Alpha8Ext = 32837,
	Luminance8Ext = 32832,
	LuminanceAlpha16fExt = 34847,
	LuminanceAlpha32fExt = 34841,
	MapFlushExplicitBitExt = 16,
	MapInvalidateBufferBitExt = 8,
	MapInvalidateRangeBitExt = 4,
	MapReadBitExt = 1,
	MapUnsynchronizedBitExt = 32,
	MapWriteBitExt = 2,
	MaxServerWaitTimeoutApple = 37137,
	ObjectTypeApple = 37138,
	OesTextureHalfFloatLinear = 1,
	R32fExt = 33326,
	Rg32fExt = 33328,
	Rgb32fExt = 34837,
	Rgba32fExt = 34836,
	RgbRaw422Apple = 35409,
	Sampler2DShadowExt = 35682,
	SignaledApple = 37145,
	Srgb8Alpha8Ext = 35907,
	SrgbAlphaExt = 35906,
	SrgbExt = 35904,
	SyncConditionApple = 37139,
	SyncFenceApple = 37142,
	SyncFlagsApple = 37141,
	SyncFlushCommandsBitApple = 1,
	SyncGpuCommandsCompleteApple = 37143,
	SyncObjectApple = 35411,
	SyncStatusApple = 37140,
	TextureImmutableFormatExt = 37167,
	TimeoutExpiredApple = 37147,
	TimeoutIgnoredApple = -1,
	UnsignaledApple = 37144,
	UnsignedShort1555Rev = 33638,
	VertexAttribArrayDivisorExt = 35070,
	WaitFailedApple = 37149,
```

### Type Changed: OpenTK.Graphics.ES20.GL

Added field:

```
public static const string Library = "libGLESv2.dll";
```

Added methods:

```
public static void BlendColor (OpenTK.Graphics.Color4 color);
	public static void ClearColor (OpenTK.Graphics.Color4 color);
	public static ErrorCode GetErrorCode ();
	public static void Uniform4 (int location, OpenTK.Graphics.Color4 color);
```

Obsoleted method:

```
[Obsolete ("Use the GetErrorCode method, for compatability with Xamarin Android's OpenTK-1.0")]
	public static ErrorCode GetError ();
```

### Type Changed: OpenTK.Graphics.ES20.GL.Apple

Added methods:

```
public static All ClientWaitSync (System.IntPtr sync, int flags, long timeout);
	public static All ClientWaitSync (System.IntPtr sync, uint flags, ulong timeout);
	public static void CopyTextureLevel (int destinationTexture, int sourceTexture, int sourceBaseLevel, int sourceLevelCount);
	public static void CopyTextureLevel (uint destinationTexture, uint sourceTexture, int sourceBaseLevel, int sourceLevelCount);
	public static void DeleteSync (System.IntPtr sync);
	public static System.IntPtr FenceSync (All condition, int flags);
	public static System.IntPtr FenceSync (All condition, uint flags);
	public static void GetInteger64 (All pname, long* params);
	public static void GetInteger64 (All pname, out long params);
	public static void GetInteger64 (All pname, long[] params);
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, int* length, int* values);
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, out int length, out int values);
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, int[] length, int[] values);
	public static bool IsSync (System.IntPtr sync);
	public static void WaitSync (System.IntPtr sync, int flags, long timeout);
	public static void WaitSync (System.IntPtr sync, uint flags, ulong timeout);
```

### Type Changed: OpenTK.Graphics.ES20.GL.Ext

Added methods:

```
public static void DrawArraysInstanced (All mode, int first, int count, int instanceCount);
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, out T3 indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[0...,0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[] indices, int instanceCount);
	public static void DrawElementsInstanced (All mode, int count, All type, System.IntPtr indices, int instanceCount);
	public static void FlushMappedBufferRange (All target, System.IntPtr offset, System.IntPtr length);
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, uint access);
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, int access);
	public static void TexStorage2D (All target, int levels, All internalformat, int width, int height);
	public static void VertexAttribDivisor (int index, int divisor);
	public static void VertexAttribDivisor (uint index, uint divisor);
```

Obsoleted methods:

```
[Obsolete ("This method was removed from iOS API 6.0 and higher")]
	public static void GetQueryObject (uint id, All pname, int[] params);

	[Obsolete ("This method was removed from iOS API 6.0 and higher")]
	public static void GetQueryObject (uint id, All pname, out int params);

	[Obsolete ("This method was removed from iOS API 6.0 and higher")]
	public static void GetQueryObject (uint id, All pname, int* params);
```

### Type Changed: OpenTK.Graphics.ES20.Unknown

Added values:

```
Alpha16fExt = 34844,
	Alpha32fExt = 34838,
	Alpha8Ext = 32828,
	AlreadySignaledApple = 37146,
	AppleCopyTextureLevels = 1,
	AppleSync = 1,
	Bgra8Ext = 37793,
	CompressedSrgbAlphaPvrtc2Bppv1Ext = 35414,
	CompressedSrgbAlphaPvrtc4Bppv1Ext = 35415,
	CompressedSrgbPvrtc2Bppv1Ext = 35412,
	CompressedSrgbPvrtc4Bppv1Ext = 35413,
	ConditionSatisfiedApple = 37148,
	DepthComponent32Oes = 33191,
	ExtDrawInstanced = 1,
	ExtInstancedArrays = 1,
	ExtMapBufferRange = 1,
	ExtPvrtcSrgb = 1,
	ExtShaderFramebufferFetch = 1,
	ExtSrgb = 1,
	ExtTextureStorage = 1,
	FragmentShaderDiscardsSamplesExt = 35410,
	FramebufferAttachmentColorEncodingExt = 33296,
	Luminance16fExt = 34846,
	Luminance32fExt = 34840,
	Luminance8Alpha8Ext = 32837,
	Luminance8Ext = 32832,
	LuminanceAlpha16fExt = 34847,
	LuminanceAlpha32fExt = 34841,
	MapFlushExplicitBitExt = 16,
	MapInvalidateBufferBitExt = 8,
	MapInvalidateRangeBitExt = 4,
	MapReadBitExt = 1,
	MapUnsynchronizedBitExt = 32,
	MapWriteBitExt = 2,
	MaxServerWaitTimeoutApple = 37137,
	ObjectTypeApple = 37138,
	OesTextureHalfFloatLinear = 1,
	R32fExt = 33326,
	Rg32fExt = 33328,
	Rgb32fExt = 34837,
	Rgba32fExt = 34836,
	RgbRaw422Apple = 35409,
	Sampler2DShadowExt = 35682,
	SignaledApple = 37145,
	Srgb8Alpha8Ext = 35907,
	SrgbAlphaExt = 35906,
	SrgbExt = 35904,
	SyncConditionApple = 37139,
	SyncFenceApple = 37142,
	SyncFlagsApple = 37141,
	SyncFlushCommandsBitApple = 1,
	SyncGpuCommandsCompleteApple = 37143,
	SyncObjectApple = 35411,
	SyncStatusApple = 37140,
	TextureImmutableFormatExt = 37167,
	TimeoutExpiredApple = 37147,
	TimeoutIgnoredApple = -1,
	UnsignaledApple = 37144,
	UnsignedShort1555Rev = 33638,
	VertexAttribArrayDivisorExt = 35070,
	WaitFailedApple = 37149,
```

### New Type OpenTK.Graphics.ES20.OpenGlEsCoreVersions

```
[Serializable]
public enum OpenGlEsCoreVersions {
	EsVersion20 = 1,
}
```

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

## Removed Namespace System.ComponentModel

### Removed Type System.ComponentModel.CancelEventArgs 

## New Namespace OpenTK.Graphics.ES30

### New Type OpenTK.Graphics.ES30.ActiveAttribType

```
[Serializable]
public enum ActiveAttribType {
	Float = 5126,
	FloatMat2 = 35674,
	FloatMat2x3 = 35685,
	FloatMat2x4 = 35686,
	FloatMat3 = 35675,
	FloatMat3x2 = 35687,
	FloatMat3x4 = 35688,
	FloatMat4 = 35676,
	FloatMat4x2 = 35689,
	FloatMat4x3 = 35690,
	FloatVec2 = 35664,
	FloatVec3 = 35665,
	FloatVec4 = 35666,
	Int = 5124,
	IntVec2 = 35667,
	IntVec3 = 35668,
	IntVec4 = 35669,
	UnsignedInt = 5125,
	UnsignedIntVec2 = 36294,
	UnsignedIntVec3 = 36295,
	UnsignedIntVec4 = 36296,
}
```

### New Type OpenTK.Graphics.ES30.ActiveUniformBlockParameter

```
[Serializable]
public enum ActiveUniformBlockParameter {
	UniformBlockActiveUniformIndices = 35395,
	UniformBlockActiveUniforms = 35394,
	UniformBlockBinding = 35391,
	UniformBlockDataSize = 35392,
	UniformBlockNameLength = 35393,
	UniformBlockReferencedByFragmentShader = 35398,
	UniformBlockReferencedByVertexShader = 35396,
}
```

### New Type OpenTK.Graphics.ES30.ActiveUniformParameter

```
[Serializable]
public enum ActiveUniformParameter {
	UniformArrayStride = 35388,
	UniformBlockIndex = 35386,
	UniformIsRowMajor = 35390,
	UniformMatrixStride = 35389,
	UniformNameLength = 35385,
	UniformOffset = 35387,
	UniformSize = 35384,
	UniformType = 35383,
}
```

### New Type OpenTK.Graphics.ES30.ActiveUniformType

```
[Serializable]
public enum ActiveUniformType {
	Bool = 35670,
	BoolVec2 = 35671,
	BoolVec3 = 35672,
	BoolVec4 = 35673,
	Float = 5126,
	FloatMat2 = 35674,
	FloatMat2x3 = 35685,
	FloatMat2x4 = 35686,
	FloatMat3 = 35675,
	FloatMat3x2 = 35687,
	FloatMat3x4 = 35688,
	FloatMat4 = 35676,
	FloatMat4x2 = 35689,
	FloatMat4x3 = 35690,
	FloatVec2 = 35664,
	FloatVec3 = 35665,
	FloatVec4 = 35666,
	Int = 5124,
	IntSampler2D = 36298,
	IntSampler2DArray = 36303,
	IntSampler3D = 36299,
	IntSamplerCube = 36300,
	IntVec2 = 35667,
	IntVec3 = 35668,
	IntVec4 = 35669,
	Sampler2D = 35678,
	Sampler2DArray = 36289,
	Sampler2DArrayShadow = 36292,
	Sampler2DShadow = 35682,
	Sampler3D = 35679,
	SamplerBinding = 35097,
	SamplerCube = 35680,
	SamplerCubeShadow = 36293,
	UnsignedInt = 5125,
	UnsignedIntSampler2D = 36306,
	UnsignedIntSampler2DArray = 36311,
	UnsignedIntSampler3D = 36307,
	UnsignedIntSamplerCube = 36308,
	UnsignedIntVec2 = 36294,
	UnsignedIntVec3 = 36295,
	UnsignedIntVec4 = 36296,
}
```

### New Type OpenTK.Graphics.ES30.All

```
[Serializable]
public enum All {
	ActiveAttributeMaxLength = 35722,
	ActiveAttributes = 35721,
	ActiveProgramExt = 33369,
	ActiveTexture = 34016,
	ActiveUniformBlockMaxNameLength = 35381,
	ActiveUniformBlocks = 35382,
	ActiveUniformMaxLength = 35719,
	ActiveUniforms = 35718,
	AliasedLineWidthRange = 33902,
	AliasedPointSizeRange = 33901,
	AllShaderBitsExt = -1,
	Alpha = 6406,
	AlphaBits = 3413,
	AlreadySignaled = 37146,
	Always = 519,
	AnySamplesPassed = 35887,
	AnySamplesPassedConservative = 36202,
	AppleCopyTextureLevels = 1,
	AppleRgb422 = 1,
	AppleTextureFormatBgra8888 = 1,
	ArrayBuffer = 34962,
	ArrayBufferBinding = 34964,
	AttachedShaders = 35717,
	Back = 1029,
	Bgra = 32993,
	Bgra8Ext = 37793,
	BgraExt = 32993,
	BgraImg = 32993,
	Blend = 3042,
	BlendColor = 32773,
	BlendDstAlpha = 32970,
	BlendDstRgb = 32968,
	BlendEquation = 32777,
	BlendEquationAlpha = 34877,
	BlendEquationRgb = 32777,
	BlendSrcAlpha = 32971,
	BlendSrcRgb = 32969,
	Blue = 6405,
	BlueBits = 3412,
	Bool = 35670,
	BoolVec2 = 35671,
	BoolVec3 = 35672,
	BoolVec4 = 35673,
	BufferAccessFlags = 37151,
	BufferMapLength = 37152,
	BufferMapOffset = 37153,
	BufferMapped = 35004,
	BufferMapPointer = 35005,
	BufferObjectExt = 37201,
	BufferSize = 34660,
	BufferUsage = 34661,
	Byte = 5120,
	Ccw = 2305,
	ClampToEdge = 33071,
	Color = 6144,
	ColorAttachment0 = 36064,
	ColorAttachment1 = 36065,
	ColorAttachment10 = 36074,
	ColorAttachment11 = 36075,
	ColorAttachment12 = 36076,
	ColorAttachment13 = 36077,
	ColorAttachment14 = 36078,
	ColorAttachment15 = 36079,
	ColorAttachment2 = 36066,
	ColorAttachment3 = 36067,
	ColorAttachment4 = 36068,
	ColorAttachment5 = 36069,
	ColorAttachment6 = 36070,
	ColorAttachment7 = 36071,
	ColorAttachment8 = 36072,
	ColorAttachment9 = 36073,
	ColorBufferBit = 16384,
	ColorClearValue = 3106,
	ColorWritemask = 3107,
	CompareRefToTexture = 34894,
	CompareRefToTextureExt = 34894,
	CompileStatus = 35713,
	CompressedR11Eac = 37488,
	CompressedRg11Eac = 37490,
	CompressedRgb8Etc2 = 37492,
	CompressedRgb8PunchthroughAlpha1Etc2 = 37494,
	CompressedRgba8Etc2Eac = 37496,
	CompressedRgbaPvrtc2Bppv1Img = 35843,
	CompressedRgbaPvrtc4Bppv1Img = 35842,
	CompressedRgbPvrtc2Bppv1Img = 35841,
	CompressedRgbPvrtc4Bppv1Img = 35840,
	CompressedSignedR11Eac = 37489,
	CompressedSignedRg11Eac = 37491,
	CompressedSrgb8Alpha8Etc2Eac = 37497,
	CompressedSrgb8Etc2 = 37493,
	CompressedSrgb8PunchthroughAlpha1Etc2 = 37495,
	CompressedSrgbAlphaPvrtc2Bppv1Ext = 35414,
	CompressedSrgbAlphaPvrtc4Bppv1Ext = 35415,
	CompressedSrgbPvrtc2Bppv1Ext = 35412,
	CompressedSrgbPvrtc4Bppv1Ext = 35413,
	CompressedTextureFormats = 34467,
	ConditionSatisfied = 37148,
	ConstantAlpha = 32771,
	ConstantColor = 32769,
	CopyReadBuffer = 36662,
	CopyReadBufferBinding = 36662,
	CopyWriteBuffer = 36663,
	CopyWriteBufferBinding = 36663,
	CullFace = 2884,
	CullFaceMode = 2885,
	CurrentProgram = 35725,
	CurrentQuery = 34917,
	CurrentVertexAttrib = 34342,
	Cw = 2304,
	Decr = 7683,
	DecrWrap = 34056,
	DeleteStatus = 35712,
	Depth = 6145,
	Depth24Stencil8 = 35056,
	Depth32fStencil8 = 36013,
	Depth32FStencil8 = 36013,
	DepthAttachment = 36096,
	DepthBits = 3414,
	DepthBufferBit = 256,
	DepthClearValue = 2931,
	DepthComponent = 6402,
	DepthComponent16 = 33189,
	DepthComponent24 = 33190,
	DepthComponent32f = 36012,
	DepthComponent32F = 36012,
	DepthFunc = 2932,
	DepthRange = 2928,
	DepthStencil = 34041,
	DepthStencilAttachment = 33306,
	DepthTest = 2929,
	DepthWritemask = 2930,
	Dither = 3024,
	DontCare = 4352,
	DrawBuffer0 = 34853,
	DrawBuffer1 = 34854,
	DrawBuffer10 = 34863,
	DrawBuffer11 = 34864,
	DrawBuffer12 = 34865,
	DrawBuffer13 = 34866,
	DrawBuffer14 = 34867,
	DrawBuffer15 = 34868,
	DrawBuffer2 = 34855,
	DrawBuffer3 = 34856,
	DrawBuffer4 = 34857,
	DrawBuffer5 = 34858,
	DrawBuffer6 = 34859,
	DrawBuffer7 = 34860,
	DrawBuffer8 = 34861,
	DrawBuffer9 = 34862,
	DrawFramebuffer = 36009,
	DrawFramebufferBinding = 36006,
	DstAlpha = 772,
	DstColor = 774,
	DynamicCopy = 35050,
	DynamicDraw = 35048,
	DynamicRead = 35049,
	ElementArrayBuffer = 34963,
	ElementArrayBufferBinding = 34965,
	Equal = 514,
	EsVersion20 = 1,
	EsVersion30 = 1,
	ExtColorBufferHalfFloat = 1,
	ExtDebugLabel = 1,
	ExtDebugMarker = 1,
	Extensions = 7939,
	ExtPvrtcSrgb = 1,
	ExtReadFormatBgra = 1,
	ExtSeparateShaderObjects = 1,
	ExtShaderFramebufferFetch = 1,
	ExtShaderTextureLod = 1,
	ExtShadowSamplers = 1,
	ExtTextureFilterAnisotropic = 1,
	False = 0,
	Fastest = 4353,
	Fixed = 5132,
	Float = 5126,
	Float32UnsignedInt248Rev = 36269,
	FloatMat2 = 35674,
	FloatMat2x3 = 35685,
	FloatMat2x4 = 35686,
	FloatMat3 = 35675,
	FloatMat3x2 = 35687,
	FloatMat3x4 = 35688,
	FloatMat4 = 35676,
	FloatMat4x2 = 35689,
	FloatMat4x3 = 35690,
	FloatVec2 = 35664,
	FloatVec3 = 35665,
	FloatVec4 = 35666,
	FragmentShader = 35632,
	FragmentShaderBitExt = 2,
	FragmentShaderDerivativeHint = 35723,
	FragmentShaderDerivativeHintOes = 35723,
	FragmentShaderDiscardsSamplesExt = 35410,
	Framebuffer = 36160,
	FramebufferAttachmentAlphaSize = 33301,
	FramebufferAttachmentBlueSize = 33300,
	FramebufferAttachmentColorEncoding = 33296,
	FramebufferAttachmentComponentType = 33297,
	FramebufferAttachmentComponentTypeExt = 33297,
	FramebufferAttachmentDepthSize = 33302,
	FramebufferAttachmentGreenSize = 33299,
	FramebufferAttachmentObjectName = 36049,
	FramebufferAttachmentObjectType = 36048,
	FramebufferAttachmentRedSize = 33298,
	FramebufferAttachmentStencilSize = 33303,
	FramebufferAttachmentTextureCubeMapFace = 36051,
	FramebufferAttachmentTextureLayer = 36052,
	FramebufferAttachmentTextureLevel = 36050,
	FramebufferBinding = 36006,
	FramebufferComplete = 36053,
	FramebufferDefault = 33304,
	FramebufferIncompleteAttachment = 36054,
	FramebufferIncompleteDimensions = 36057,
	FramebufferIncompleteMissingAttachment = 36055,
	FramebufferIncompleteMultisample = 36182,
	FramebufferUndefined = 33305,
	FramebufferUnsupported = 36061,
	Front = 1028,
	FrontAndBack = 1032,
	FrontFace = 2886,
	FuncAdd = 32774,
	FuncReverseSubtract = 32779,
	FuncSubtract = 32778,
	GenerateMipmapHint = 33170,
	Gequal = 518,
	Greater = 516,
	Green = 6404,
	GreenBits = 3411,
	HalfFloat = 5131,
	HighFloat = 36338,
	HighInt = 36341,
	ImgReadFormat = 1,
	ImgTextureCompressionPvrtc = 1,
	ImgTextureFormatBgra8888 = 1,
	ImplementationColorReadFormat = 35739,
	ImplementationColorReadType = 35738,
	Incr = 7682,
	IncrWrap = 34055,
	InfoLogLength = 35716,
	Int = 5124,
	Int2101010Rev = 36255,
	InterleavedAttribs = 35980,
	IntSampler2D = 36298,
	IntSampler2DArray = 36303,
	IntSampler3D = 36299,
	IntSamplerCube = 36300,
	IntVec2 = 35667,
	IntVec3 = 35668,
	IntVec4 = 35669,
	InvalidEnum = 1280,
	InvalidFramebufferOperation = 1286,
	InvalidIndex = -1,
	InvalidOperation = 1282,
	InvalidValue = 1281,
	Invert = 5386,
	Keep = 7680,
	Lequal = 515,
	Less = 513,
	Linear = 9729,
	LinearMipmapLinear = 9987,
	LinearMipmapNearest = 9985,
	LineLoop = 2,
	Lines = 1,
	LineStrip = 3,
	LineWidth = 2849,
	LinkStatus = 35714,
	LowFloat = 36336,
	LowInt = 36339,
	Luminance = 6409,
	LuminanceAlpha = 6410,
	MajorVersion = 33307,
	MapFlushExplicitBit = 16,
	MapInvalidateBufferBit = 8,
	MapInvalidateRangeBit = 4,
	MapReadBit = 1,
	MapUnsynchronizedBit = 32,
	MapWriteBit = 2,
	Max = 32776,
	Max3DTextureSize = 32883,
	MaxArrayTextureLayers = 35071,
	MaxColorAttachments = 36063,
	MaxCombinedFragmentUniformComponents = 35379,
	MaxCombinedTextureImageUnits = 35661,
	MaxCombinedUniformBlocks = 35374,
	MaxCombinedVertexUniformComponents = 35377,
	MaxCubeMapTextureSize = 34076,
	MaxDrawBuffers = 34852,
	MaxElementIndex = 36203,
	MaxElementsIndices = 33001,
	MaxElementsVertices = 33000,
	MaxFragmentInputComponents = 37157,
	MaxFragmentUniformBlocks = 35373,
	MaxFragmentUniformComponents = 35657,
	MaxFragmentUniformVectors = 36349,
	MaxProgramTexelOffset = 35077,
	MaxRenderbufferSize = 34024,
	MaxSamples = 36183,
	MaxServerWaitTimeout = 37137,
	MaxTextureImageUnits = 34930,
	MaxTextureLodBias = 34045,
	MaxTextureMaxAnisotropyExt = 34047,
	MaxTextureSize = 3379,
	MaxTransformFeedbackInterleavedComponents = 35978,
	MaxTransformFeedbackSeparateAttribs = 35979,
	MaxTransformFeedbackSeparateComponents = 35968,
	MaxUniformBlockSize = 35376,
	MaxUniformBufferBindings = 35375,
	MaxVaryingComponents = 35659,
	MaxVaryingVectors = 36348,
	MaxVertexAttribs = 34921,
	MaxVertexOutputComponents = 37154,
	MaxVertexTextureImageUnits = 35660,
	MaxVertexUniformBlocks = 35371,
	MaxVertexUniformComponents = 35658,
	MaxVertexUniformVectors = 36347,
	MaxViewportDims = 3386,
	MediumFloat = 36337,
	MediumInt = 36340,
	Min = 32775,
	MinorVersion = 33308,
	MinProgramTexelOffset = 35076,
	MirroredRepeat = 33648,
	Nearest = 9728,
	NearestMipmapLinear = 9986,
	NearestMipmapNearest = 9984,
	Never = 512,
	Nicest = 4354,
	NoError = 0,
	None = 0,
	Notequal = 517,
	NumCompressedTextureFormats = 34466,
	NumExtensions = 33309,
	NumProgramBinaryFormats = 34814,
	NumSampleCounts = 37760,
	NumShaderBinaryFormats = 36345,
	ObjectType = 37138,
	OesStandardDerivatives = 1,
	One = 1,
	OneMinusConstantAlpha = 32772,
	OneMinusConstantColor = 32770,
	OneMinusDstAlpha = 773,
	OneMinusDstColor = 775,
	OneMinusSrcAlpha = 771,
	OneMinusSrcColor = 769,
	OutOfMemory = 1285,
	PackAlignment = 3333,
	PackRowLength = 3330,
	PackSkipPixels = 3332,
	PackSkipRows = 3331,
	PixelPackBuffer = 35051,
	PixelPackBufferBinding = 35053,
	PixelUnpackBuffer = 35052,
	PixelUnpackBufferBinding = 35055,
	Points = 0,
	PolygonOffsetFactor = 32824,
	PolygonOffsetFill = 32823,
	PolygonOffsetUnits = 10752,
	PrimitiveRestartFixedIndex = 36201,
	ProgramBinaryFormats = 34815,
	ProgramBinaryLength = 34625,
	ProgramBinaryRetrievableHint = 33367,
	ProgramObjectExt = 35648,
	ProgramPipelineBindingExt = 33370,
	ProgramPipelineObjectExt = 35407,
	ProgramSeparableExt = 33368,
	QueryObjectExt = 37203,
	QueryResult = 34918,
	QueryResultAvailable = 34919,
	R11fG11fB10f = 35898,
	R16f = 33325,
	R16fExt = 33325,
	R16i = 33331,
	R16ui = 33332,
	R32f = 33326,
	R32i = 33333,
	R32ui = 33334,
	R8 = 33321,
	R8i = 33329,
	R8Snorm = 36756,
	R8ui = 33330,
	RasterizerDiscard = 35977,
	ReadBuffer = 3074,
	ReadFramebuffer = 36008,
	ReadFramebufferBinding = 36010,
	Red = 6403,
	RedBits = 3410,
	RedInteger = 36244,
	Renderbuffer = 36161,
	RenderbufferAlphaSize = 36179,
	RenderbufferBinding = 36007,
	RenderbufferBlueSize = 36178,
	RenderbufferDepthSize = 36180,
	RenderbufferGreenSize = 36177,
	RenderbufferHeight = 36163,
	RenderbufferInternalFormat = 36164,
	RenderbufferRedSize = 36176,
	RenderbufferSamples = 36011,
	RenderbufferStencilSize = 36181,
	RenderbufferWidth = 36162,
	Renderer = 7937,
	Repeat = 10497,
	Replace = 7681,
	Rg = 33319,
	Rg16f = 33327,
	Rg16fExt = 33327,
	Rg16i = 33337,
	Rg16ui = 33338,
	Rg32f = 33328,
	Rg32i = 33339,
	Rg32ui = 33340,
	Rg8 = 33323,
	Rg8i = 33335,
	Rg8Snorm = 36757,
	Rg8ui = 33336,
	Rgb = 6407,
	Rgb10A2 = 32857,
	Rgb10A2ui = 36975,
	Rgb16f = 34843,
	Rgb16fExt = 34843,
	Rgb16i = 36233,
	Rgb16ui = 36215,
	Rgb32f = 34837,
	Rgb32i = 36227,
	Rgb32ui = 36209,
	Rgb422Apple = 35359,
	Rgb565 = 36194,
	Rgb5A1 = 32855,
	Rgb8 = 32849,
	Rgb8i = 36239,
	Rgb8Snorm = 36758,
	Rgb8ui = 36221,
	Rgb9E5 = 35901,
	Rgba = 6408,
	Rgba16f = 34842,
	Rgba16fExt = 34842,
	Rgba16i = 36232,
	Rgba16ui = 36214,
	Rgba32f = 34836,
	Rgba32i = 36226,
	Rgba32ui = 36208,
	Rgba4 = 32854,
	Rgba8 = 32856,
	Rgba8i = 36238,
	Rgba8Snorm = 36759,
	Rgba8ui = 36220,
	RgbaInteger = 36249,
	RgbInteger = 36248,
	RgbRaw422Apple = 35409,
	RgInteger = 33320,
	SampleAlphaToCoverage = 32926,
	SampleBuffers = 32936,
	SampleCoverage = 32928,
	SampleCoverageInvert = 32939,
	SampleCoverageValue = 32938,
	Sampler = 33510,
	Sampler2D = 35678,
	Sampler2DArray = 36289,
	Sampler2DArrayShadow = 36292,
	Sampler2DShadow = 35682,
	Sampler2DShadowExt = 35682,
	Sampler3D = 35679,
	SamplerBinding = 35097,
	SamplerCube = 35680,
	SamplerCubeShadow = 36293,
	Samples = 32937,
	ScissorBox = 3088,
	ScissorTest = 3089,
	SeparateAttribs = 35981,
	ShaderBinaryFormats = 36344,
	ShaderCompiler = 36346,
	ShaderObjectExt = 35656,
	ShaderSourceLength = 35720,
	ShaderType = 35663,
	ShadingLanguageVersion = 35724,
	Short = 5122,
	Signaled = 37145,
	SignedNormalized = 36764,
	SrcAlpha = 770,
	SrcAlphaSaturate = 776,
	SrcColor = 768,
	Srgb = 35904,
	Srgb8 = 35905,
	Srgb8Alpha8 = 35907,
	StaticCopy = 35046,
	StaticDraw = 35044,
	StaticRead = 35045,
	Stencil = 6146,
	StencilAttachment = 36128,
	StencilBackFail = 34817,
	StencilBackFunc = 34816,
	StencilBackPassDepthFail = 34818,
	StencilBackPassDepthPass = 34819,
	StencilBackRef = 36003,
	StencilBackValueMask = 36004,
	StencilBackWritemask = 36005,
	StencilBits = 3415,
	StencilBufferBit = 1024,
	StencilClearValue = 2961,
	StencilFail = 2964,
	StencilFunc = 2962,
	StencilIndex = 6401,
	StencilIndex8 = 36168,
	StencilPassDepthFail = 2965,
	StencilPassDepthPass = 2966,
	StencilRef = 2967,
	StencilTest = 2960,
	StencilValueMask = 2963,
	StencilWritemask = 2968,
	StreamCopy = 35042,
	StreamDraw = 35040,
	StreamRead = 35041,
	SubpixelBits = 3408,
	SyncCondition = 37139,
	SyncFence = 37142,
	SyncFlags = 37141,
	SyncFlushCommandsBit = 1,
	SyncGpuCommandsComplete = 37143,
	SyncObjectApple = 35411,
	SyncStatus = 37140,
	Texture = 5890,
	Texture0 = 33984,
	Texture1 = 33985,
	Texture10 = 33994,
	Texture11 = 33995,
	Texture12 = 33996,
	Texture13 = 33997,
	Texture14 = 33998,
	Texture15 = 33999,
	Texture16 = 34000,
	Texture17 = 34001,
	Texture18 = 34002,
	Texture19 = 34003,
	Texture2 = 33986,
	Texture20 = 34004,
	Texture21 = 34005,
	Texture22 = 34006,
	Texture23 = 34007,
	Texture24 = 34008,
	Texture25 = 34009,
	Texture26 = 34010,
	Texture27 = 34011,
	Texture28 = 34012,
	Texture29 = 34013,
	Texture2D = 3553,
	Texture2DArray = 35866,
	Texture3 = 33987,
	Texture30 = 34014,
	Texture31 = 34015,
	Texture3D = 32879,
	Texture4 = 33988,
	Texture5 = 33989,
	Texture6 = 33990,
	Texture7 = 33991,
	Texture8 = 33992,
	Texture9 = 33993,
	TextureBaseLevel = 33084,
	TextureBinding2D = 32873,
	TextureBinding2DArray = 35869,
	TextureBinding3D = 32874,
	TextureBindingCubeMap = 34068,
	TextureCompareFunc = 34893,
	TextureCompareFuncExt = 34893,
	TextureCompareMode = 34892,
	TextureCompareModeExt = 34892,
	TextureCubeMap = 34067,
	TextureCubeMapNegativeX = 34070,
	TextureCubeMapNegativeY = 34072,
	TextureCubeMapNegativeZ = 34074,
	TextureCubeMapPositiveX = 34069,
	TextureCubeMapPositiveY = 34071,
	TextureCubeMapPositiveZ = 34073,
	TextureImmutableFormat = 37167,
	TextureImmutableLevels = 33503,
	TextureMagFilter = 10240,
	TextureMaxAnisotropyExt = 34046,
	TextureMaxLevel = 33085,
	TextureMaxLod = 33083,
	TextureMinFilter = 10241,
	TextureMinLod = 33082,
	TextureSwizzleA = 36421,
	TextureSwizzleB = 36420,
	TextureSwizzleG = 36419,
	TextureSwizzleR = 36418,
	TextureWrapR = 32882,
	TextureWrapS = 10242,
	TextureWrapT = 10243,
	TimeoutExpired = 37147,
	TimeoutIgnored = -1,
	TransformFeedback = 36386,
	TransformFeedbackActive = 36388,
	TransformFeedbackBinding = 36389,
	TransformFeedbackBuffer = 35982,
	TransformFeedbackBufferBinding = 35983,
	TransformFeedbackBufferMode = 35967,
	TransformFeedbackBufferSize = 35973,
	TransformFeedbackBufferStart = 35972,
	TransformFeedbackPaused = 36387,
	TransformFeedbackPrimitivesWritten = 35976,
	TransformFeedbackVaryingMaxLength = 35958,
	TransformFeedbackVaryings = 35971,
	TriangleFan = 6,
	Triangles = 4,
	TriangleStrip = 5,
	True = 1,
	UniformArrayStride = 35388,
	UniformBlockActiveUniformIndices = 35395,
	UniformBlockActiveUniforms = 35394,
	UniformBlockBinding = 35391,
	UniformBlockDataSize = 35392,
	UniformBlockIndex = 35386,
	UniformBlockNameLength = 35393,
	UniformBlockReferencedByFragmentShader = 35398,
	UniformBlockReferencedByVertexShader = 35396,
	UniformBuffer = 35345,
	UniformBufferBinding = 35368,
	UniformBufferOffsetAlignment = 35380,
	UniformBufferSize = 35370,
	UniformBufferStart = 35369,
	UniformIsRowMajor = 35390,
	UniformMatrixStride = 35389,
	UniformNameLength = 35385,
	UniformOffset = 35387,
	UniformSize = 35384,
	UniformType = 35383,
	UnpackAlignment = 3317,
	UnpackImageHeight = 32878,
	UnpackRowLength = 3314,
	UnpackSkipImages = 32877,
	UnpackSkipPixels = 3316,
	UnpackSkipRows = 3315,
	Unsignaled = 37144,
	UnsignedByte = 5121,
	UnsignedInt = 5125,
	UnsignedInt10F11F11FRev = 35899,
	UnsignedInt2101010Rev = 33640,
	UnsignedInt248 = 34042,
	UnsignedInt5999Rev = 35902,
	UnsignedIntSampler2D = 36306,
	UnsignedIntSampler2DArray = 36311,
	UnsignedIntSampler3D = 36307,
	UnsignedIntSamplerCube = 36308,
	UnsignedIntVec2 = 36294,
	UnsignedIntVec3 = 36295,
	UnsignedIntVec4 = 36296,
	UnsignedNormalized = 35863,
	UnsignedNormalizedExt = 35863,
	UnsignedShort = 5123,
	UnsignedShort1555Rev = 33638,
	UnsignedShort1555RevExt = 33638,
	UnsignedShort4444 = 32819,
	UnsignedShort4444Rev = 33637,
	UnsignedShort4444RevExt = 33637,
	UnsignedShort4444RevImg = 33637,
	UnsignedShort5551 = 32820,
	UnsignedShort565 = 33635,
	UnsignedShort88Apple = 34234,
	UnsignedShort88RevApple = 34235,
	ValidateStatus = 35715,
	Vendor = 7936,
	Version = 7938,
	VertexArrayBinding = 34229,
	VertexArrayObjectExt = 37204,
	VertexAttribArrayBufferBinding = 34975,
	VertexAttribArrayDivisor = 35070,
	VertexAttribArrayEnabled = 34338,
	VertexAttribArrayInteger = 35069,
	VertexAttribArrayNormalized = 34922,
	VertexAttribArrayPointer = 34373,
	VertexAttribArraySize = 34339,
	VertexAttribArrayStride = 34340,
	VertexAttribArrayType = 34341,
	VertexShader = 35633,
	VertexShaderBitExt = 1,
	Viewport = 2978,
	WaitFailed = 37149,
	Zero = 0,
}
```

### New Type OpenTK.Graphics.ES30.BeginMode

```
[Serializable]
public enum BeginMode {
	LineLoop = 2,
	Lines = 1,
	LineStrip = 3,
	Points = 0,
	TriangleFan = 6,
	Triangles = 4,
	TriangleStrip = 5,
}
```

### New Type OpenTK.Graphics.ES30.BlendEquationMode

```
[Serializable]
public enum BlendEquationMode {
	FuncAdd = 32774,
	FuncReverseSubtract = 32779,
	FuncSubtract = 32778,
	Max = 32776,
	Min = 32775,
}
```

### New Type OpenTK.Graphics.ES30.BlendEquationSeparate

```
[Serializable]
public enum BlendEquationSeparate {
	BlendEquation = 32777,
	BlendEquationAlpha = 34877,
	FuncAdd = 32774,
}
```

### New Type OpenTK.Graphics.ES30.BlendingFactorDest

```
[Serializable]
public enum BlendingFactorDest {
	ConstantAlpha = 32771,
	ConstantColor = 32769,
	DstAlpha = 772,
	DstColor = 774,
	One = 1,
	OneMinusConstantAlpha = 32772,
	OneMinusConstantColor = 32770,
	OneMinusDstAlpha = 773,
	OneMinusDstColor = 775,
	OneMinusSrcAlpha = 771,
	OneMinusSrcColor = 769,
	SrcAlpha = 770,
	SrcAlphaSaturate = 776,
	SrcColor = 768,
	Zero = 0,
}
```

### New Type OpenTK.Graphics.ES30.BlendingFactorSrc

```
[Serializable]
public enum BlendingFactorSrc {
	ConstantAlpha = 32771,
	ConstantColor = 32769,
	DstAlpha = 772,
	DstColor = 774,
	One = 1,
	OneMinusConstantAlpha = 32772,
	OneMinusConstantColor = 32770,
	OneMinusDstAlpha = 773,
	OneMinusDstColor = 775,
	OneMinusSrcAlpha = 771,
	OneMinusSrcColor = 769,
	SrcAlpha = 770,
	SrcAlphaSaturate = 776,
	SrcColor = 768,
	Zero = 0,
}
```

### New Type OpenTK.Graphics.ES30.BlendSubtract

```
[Serializable]
public enum BlendSubtract {
	FuncReverseSubtract = 32779,
	FuncSubtract = 32778,
}
```

### New Type OpenTK.Graphics.ES30.BlitFramebufferFilter

```
[Serializable]
public enum BlitFramebufferFilter {
	Linear = 9729,
	Nearest = 9728,
}
```

### New Type OpenTK.Graphics.ES30.Boolean

```
[Serializable]
public enum Boolean {
	False = 0,
	True = 1,
}
```

### New Type OpenTK.Graphics.ES30.BufferAccessMask

```
[Serializable]
[Flags]
public enum BufferAccessMask {
	MapFlushExplicitBit = 16,
	MapInvalidateBufferBit = 8,
	MapInvalidateRangeBit = 4,
	MapReadBit = 1,
	MapUnsynchronizedBit = 32,
	MapWriteBit = 2,
}
```

### New Type OpenTK.Graphics.ES30.BufferObjects

```
[Serializable]
public enum BufferObjects {
	ArrayBuffer = 34962,
	ArrayBufferBinding = 34964,
	BufferSize = 34660,
	BufferUsage = 34661,
	CurrentVertexAttrib = 34342,
	DynamicDraw = 35048,
	ElementArrayBuffer = 34963,
	ElementArrayBufferBinding = 34965,
	StaticDraw = 35044,
	StreamDraw = 35040,
}
```

### New Type OpenTK.Graphics.ES30.BufferParameterName

```
[Serializable]
public enum BufferParameterName {
	BufferAccessFlags = 37151,
	BufferMapLength = 37152,
	BufferMapOffset = 37153,
	BufferMapped = 35004,
	BufferMapPointer = 35005,
	BufferSize = 34660,
	BufferUsage = 34661,
}
```

### New Type OpenTK.Graphics.ES30.BufferPointer

```
[Serializable]
public enum BufferPointer {
	BufferMapPointer = 35005,
}
```

### New Type OpenTK.Graphics.ES30.BufferRangeTarget

```
[Serializable]
public enum BufferRangeTarget {
	TransformFeedbackBuffer = 35982,
	UniformBuffer = 35345,
}
```

### New Type OpenTK.Graphics.ES30.BufferTarget

```
[Serializable]
public enum BufferTarget {
	ArrayBuffer = 34962,
	CopyReadBuffer = 36662,
	CopyWriteBuffer = 36663,
	ElementArrayBuffer = 34963,
	PixelPackBuffer = 35051,
	PixelUnpackBuffer = 35052,
	TransformFeedbackBuffer = 35982,
	UniformBuffer = 35345,
}
```

### New Type OpenTK.Graphics.ES30.BufferUsage

```
[Serializable]
public enum BufferUsage {
	DynamicDraw = 35048,
	StaticDraw = 35044,
	StreamDraw = 35040,
}
```

### New Type OpenTK.Graphics.ES30.ClearBuffer

```
[Serializable]
public enum ClearBuffer {
	Back = 1029,
	Color = 6144,
	Depth = 6145,
	Front = 1028,
	FrontAndBack = 1032,
	Stencil = 6146,
}
```

### New Type OpenTK.Graphics.ES30.ClearBufferCombined

```
[Serializable]
public enum ClearBufferCombined {
	DepthStencil = 34041,
}
```

### New Type OpenTK.Graphics.ES30.ClearBufferMask

```
[Serializable]
[Flags]
public enum ClearBufferMask {
	ColorBufferBit = 16384,
	DepthBufferBit = 256,
	StencilBufferBit = 1024,
}
```

### New Type OpenTK.Graphics.ES30.CompressedInternalFormat

```
[Serializable]
public enum CompressedInternalFormat {
	CompressedR11Eac = 37488,
	CompressedRg11Eac = 37490,
	CompressedRgb8Etc2 = 37492,
	CompressedRgb8PunchthroughAlpha1Etc2 = 37494,
	CompressedRgba8Etc2Eac = 37496,
	CompressedSignedR11Eac = 37489,
	CompressedSignedRg11Eac = 37491,
	CompressedSrgb8Alpha8Etc2Eac = 37497,
	CompressedSrgb8Etc2 = 37493,
	CompressedSrgb8PunchthroughAlpha1Etc2 = 37495,
}
```

### New Type OpenTK.Graphics.ES30.CullFaceMode

```
[Serializable]
public enum CullFaceMode {
	Back = 1029,
	Front = 1028,
	FrontAndBack = 1032,
}
```

### New Type OpenTK.Graphics.ES30.DataType

```
[Serializable]
public enum DataType {
	Byte = 5120,
	Fixed = 5132,
	Float = 5126,
	Int = 5124,
	Short = 5122,
	UnsignedByte = 5121,
	UnsignedInt = 5125,
	UnsignedShort = 5123,
}
```

### New Type OpenTK.Graphics.ES30.DepthFunction

```
[Serializable]
public enum DepthFunction {
	Always = 519,
	Equal = 514,
	Gequal = 518,
	Greater = 516,
	Lequal = 515,
	Less = 513,
	Never = 512,
	Notequal = 517,
}
```

### New Type OpenTK.Graphics.ES30.DrawBufferMode

```
[Serializable]
public enum DrawBufferMode {
	Back = 1029,
	ColorAttachment0 = 36064,
	ColorAttachment1 = 36065,
	ColorAttachment10 = 36074,
	ColorAttachment11 = 36075,
	ColorAttachment12 = 36076,
	ColorAttachment13 = 36077,
	ColorAttachment14 = 36078,
	ColorAttachment15 = 36079,
	ColorAttachment2 = 36066,
	ColorAttachment3 = 36067,
	ColorAttachment4 = 36068,
	ColorAttachment5 = 36069,
	ColorAttachment6 = 36070,
	ColorAttachment7 = 36071,
	ColorAttachment8 = 36072,
	ColorAttachment9 = 36073,
	None = 0,
}
```

### New Type OpenTK.Graphics.ES30.DrawElementsType

```
[Serializable]
public enum DrawElementsType {
	UnsignedByte = 5121,
	UnsignedInt = 5125,
	UnsignedShort = 5123,
}
```

### New Type OpenTK.Graphics.ES30.EnableCap

```
[Serializable]
public enum EnableCap {
	Blend = 3042,
	CullFace = 2884,
	DepthTest = 2929,
	Dither = 3024,
	PolygonOffsetFill = 32823,
	PrimitiveRestartFixedIndex = 36201,
	RasterizerDiscard = 35977,
	SampleAlphaToCoverage = 32926,
	SampleCoverage = 32928,
	ScissorTest = 3089,
	StencilTest = 2960,
	Texture2D = 3553,
}
```

### New Type OpenTK.Graphics.ES30.ErrorCode

```
[Serializable]
public enum ErrorCode {
	InvalidEnum = 1280,
	InvalidFramebufferOperation = 1286,
	InvalidOperation = 1282,
	InvalidValue = 1281,
	NoError = 0,
	OutOfMemory = 1285,
}
```

### New Type OpenTK.Graphics.ES30.FramebufferAttachment

```
[Serializable]
public enum FramebufferAttachment {
	ColorAttachment0 = 36064,
	ColorAttachment1 = 36065,
	ColorAttachment10 = 36074,
	ColorAttachment11 = 36075,
	ColorAttachment12 = 36076,
	ColorAttachment13 = 36077,
	ColorAttachment14 = 36078,
	ColorAttachment15 = 36079,
	ColorAttachment2 = 36066,
	ColorAttachment3 = 36067,
	ColorAttachment4 = 36068,
	ColorAttachment5 = 36069,
	ColorAttachment6 = 36070,
	ColorAttachment7 = 36071,
	ColorAttachment8 = 36072,
	ColorAttachment9 = 36073,
	DepthAttachment = 36096,
	DepthStencilAttachment = 33306,
	StencilAttachment = 36128,
}
```

### New Type OpenTK.Graphics.ES30.FramebufferErrorCode

```
[Serializable]
public enum FramebufferErrorCode {
	FramebufferComplete = 36053,
	FramebufferIncompleteAttachment = 36054,
	FramebufferIncompleteDimensions = 36057,
	FramebufferIncompleteMissingAttachment = 36055,
	FramebufferUnsupported = 36061,
}
```

### New Type OpenTK.Graphics.ES30.FramebufferObject

```
[Serializable]
public enum FramebufferObject {
	ColorAttachment0 = 36064,
	DepthAttachment = 36096,
	DepthComponent16 = 33189,
	Framebuffer = 36160,
	FramebufferAttachmentObjectName = 36049,
	FramebufferAttachmentObjectType = 36048,
	FramebufferAttachmentTextureCubeMapFace = 36051,
	FramebufferAttachmentTextureLevel = 36050,
	FramebufferBinding = 36006,
	FramebufferComplete = 36053,
	FramebufferIncompleteAttachment = 36054,
	FramebufferIncompleteDimensions = 36057,
	FramebufferIncompleteMissingAttachment = 36055,
	FramebufferUnsupported = 36061,
	InvalidFramebufferOperation = 1286,
	MaxRenderbufferSize = 34024,
	None = 0,
	Renderbuffer = 36161,
	RenderbufferAlphaSize = 36179,
	RenderbufferBinding = 36007,
	RenderbufferBlueSize = 36178,
	RenderbufferDepthSize = 36180,
	RenderbufferGreenSize = 36177,
	RenderbufferHeight = 36163,
	RenderbufferInternalFormat = 36164,
	RenderbufferRedSize = 36176,
	RenderbufferStencilSize = 36181,
	RenderbufferWidth = 36162,
	Rgb565 = 36194,
	Rgb5A1 = 32855,
	Rgba4 = 32854,
	StencilAttachment = 36128,
	StencilIndex = 6401,
	StencilIndex8 = 36168,
}
```

### New Type OpenTK.Graphics.ES30.FramebufferParameterName

```
[Serializable]
public enum FramebufferParameterName {
	FramebufferAttachmentAlphaSize = 33301,
	FramebufferAttachmentBlueSize = 33300,
	FramebufferAttachmentColorEncoding = 33296,
	FramebufferAttachmentComponentType = 33297,
	FramebufferAttachmentDepthSize = 33302,
	FramebufferAttachmentGreenSize = 33299,
	FramebufferAttachmentObjectName = 36049,
	FramebufferAttachmentObjectType = 36048,
	FramebufferAttachmentRedSize = 33298,
	FramebufferAttachmentStencilSize = 33303,
	FramebufferAttachmentTextureCubeMapFace = 36051,
	FramebufferAttachmentTextureLayer = 36052,
	FramebufferAttachmentTextureLevel = 36050,
}
```

### New Type OpenTK.Graphics.ES30.FramebufferSlot

```
[Serializable]
public enum FramebufferSlot {
	ColorAttachment0 = 36064,
	ColorAttachment1 = 36065,
	ColorAttachment10 = 36074,
	ColorAttachment11 = 36075,
	ColorAttachment12 = 36076,
	ColorAttachment13 = 36077,
	ColorAttachment14 = 36078,
	ColorAttachment15 = 36079,
	ColorAttachment2 = 36066,
	ColorAttachment3 = 36067,
	ColorAttachment4 = 36068,
	ColorAttachment5 = 36069,
	ColorAttachment6 = 36070,
	ColorAttachment7 = 36071,
	ColorAttachment8 = 36072,
	ColorAttachment9 = 36073,
	DepthAttachment = 36096,
	DepthStencilAttachment = 33306,
	StencilAttachment = 36128,
}
```

### New Type OpenTK.Graphics.ES30.FramebufferTarget

```
[Serializable]
public enum FramebufferTarget {
	DrawFramebuffer = 36009,
	Framebuffer = 36160,
	ReadFramebuffer = 36008,
}
```

### New Type OpenTK.Graphics.ES30.FrontFaceDirection

```
[Serializable]
public enum FrontFaceDirection {
	Ccw = 2305,
	Cw = 2304,
}
```

### New Type OpenTK.Graphics.ES30.GetIndexedPName

```
[Serializable]
public enum GetIndexedPName {
	TransformFeedbackBufferBinding = 35983,
	TransformFeedbackBufferSize = 35973,
	TransformFeedbackBufferStart = 35972,
	UniformBufferBinding = 35368,
	UniformBufferSize = 35370,
	UniformBufferStart = 35369,
}
```

### New Type OpenTK.Graphics.ES30.GetPName

```
[Serializable]
public enum GetPName {
	ActiveTexture = 34016,
	AliasedLineWidthRange = 33902,
	AliasedPointSizeRange = 33901,
	AlphaBits = 3413,
	ArrayBufferBinding = 34964,
	Blend = 3042,
	BlendColor = 32773,
	BlendDstAlpha = 32970,
	BlendDstRgb = 32968,
	BlendEquation = 32777,
	BlendEquationAlpha = 34877,
	BlendEquationRgb = 32777,
	BlendSrcAlpha = 32971,
	BlendSrcRgb = 32969,
	BlueBits = 3412,
	ColorClearValue = 3106,
	ColorWritemask = 3107,
	CompressedTextureFormats = 34467,
	CullFace = 2884,
	CullFaceMode = 2885,
	CurrentProgram = 35725,
	DepthBits = 3414,
	DepthClearValue = 2931,
	DepthFunc = 2932,
	DepthRange = 2928,
	DepthTest = 2929,
	DepthWritemask = 2930,
	Dither = 3024,
	DrawBuffer0 = 34853,
	DrawBuffer1 = 34854,
	DrawBuffer10 = 34863,
	DrawBuffer11 = 34864,
	DrawBuffer12 = 34865,
	DrawBuffer13 = 34866,
	DrawBuffer14 = 34867,
	DrawBuffer15 = 34868,
	DrawBuffer2 = 34855,
	DrawBuffer3 = 34856,
	DrawBuffer4 = 34857,
	DrawBuffer5 = 34858,
	DrawBuffer6 = 34859,
	DrawBuffer7 = 34860,
	DrawBuffer8 = 34861,
	DrawBuffer9 = 34862,
	DrawFramebufferBinding = 36006,
	ElementArrayBufferBinding = 34965,
	FragmentShaderDerivativeHint = 35723,
	FramebufferBinding = 36006,
	FrontFace = 2886,
	GenerateMipmapHint = 33170,
	GreenBits = 3411,
	ImplementationColorReadFormat = 35739,
	ImplementationColorReadType = 35738,
	LineWidth = 2849,
	MajorVersion = 33307,
	Max3DTextureSize = 32883,
	MaxArrayTextureLayers = 35071,
	MaxColorAttachments = 36063,
	MaxCombinedFragmentUniformComponents = 35379,
	MaxCombinedTextureImageUnits = 35661,
	MaxCombinedUniformBlocks = 35374,
	MaxCombinedVertexUniformComponents = 35377,
	MaxCubeMapTextureSize = 34076,
	MaxDrawBuffers = 34852,
	MaxElementIndex = 36203,
	MaxElementsIndices = 33001,
	MaxElementsVertices = 33000,
	MaxFragmentInputComponents = 37157,
	MaxFragmentUniformBlocks = 35373,
	MaxFragmentUniformComponents = 35657,
	MaxFragmentUniformVectors = 36349,
	MaxProgramTexelOffset = 35077,
	MaxRenderbufferSize = 34024,
	MaxSamples = 36183,
	MaxServerWaitTimeout = 37137,
	MaxTextureImageUnits = 34930,
	MaxTextureLodBias = 34045,
	MaxTextureSize = 3379,
	MaxTransformFeedbackInterleavedComponents = 35978,
	MaxTransformFeedbackSeparateAttribs = 35979,
	MaxTransformFeedbackSeparateComponents = 35968,
	MaxUniformBlockSize = 35376,
	MaxUniformBufferBindings = 35375,
	MaxVaryingComponents = 35659,
	MaxVaryingVectors = 36348,
	MaxVertexAttribs = 34921,
	MaxVertexOutputComponents = 37154,
	MaxVertexTextureImageUnits = 35660,
	MaxVertexUniformBlocks = 35371,
	MaxVertexUniformComponents = 35658,
	MaxVertexUniformVectors = 36347,
	MaxViewportDims = 3386,
	MinorVersion = 33308,
	MinProgramTexelOffset = 35076,
	NumCompressedTextureFormats = 34466,
	NumExtensions = 33309,
	NumProgramBinaryFormats = 34814,
	NumShaderBinaryFormats = 36345,
	PackAlignment = 3333,
	PackRowLength = 3330,
	PackSkipPixels = 3332,
	PackSkipRows = 3331,
	PixelPackBufferBinding = 35053,
	PixelUnpackBufferBinding = 35055,
	PolygonOffsetFactor = 32824,
	PolygonOffsetFill = 32823,
	PolygonOffsetUnits = 10752,
	PrimitiveRestartFixedIndex = 36201,
	ProgramBinaryFormats = 34815,
	ReadBuffer = 3074,
	ReadFramebufferBinding = 36010,
	RedBits = 3410,
	RenderbufferBinding = 36007,
	SampleAlphaToCoverage = 32926,
	SampleBuffers = 32936,
	SampleCoverage = 32928,
	SampleCoverageInvert = 32939,
	SampleCoverageValue = 32938,
	Samples = 32937,
	ScissorBox = 3088,
	ScissorTest = 3089,
	ShaderBinaryFormats = 36344,
	ShaderCompiler = 36346,
	StencilBackFail = 34817,
	StencilBackFunc = 34816,
	StencilBackPassDepthFail = 34818,
	StencilBackPassDepthPass = 34819,
	StencilBackRef = 36003,
	StencilBackValueMask = 36004,
	StencilBackWritemask = 36005,
	StencilBits = 3415,
	StencilClearValue = 2961,
	StencilFail = 2964,
	StencilFunc = 2962,
	StencilPassDepthFail = 2965,
	StencilPassDepthPass = 2966,
	StencilRef = 2967,
	StencilTest = 2960,
	StencilValueMask = 2963,
	StencilWritemask = 2968,
	SubpixelBits = 3408,
	Texture2D = 3553,
	Texture3D = 32879,
	TextureBinding2D = 32873,
	TextureBinding2DArray = 35869,
	TextureBinding3D = 32874,
	TextureBindingCubeMap = 34068,
	TransformFeedbackActive = 36388,
	TransformFeedbackBinding = 36389,
	TransformFeedbackBufferBinding = 35983,
	TransformFeedbackBufferSize = 35973,
	TransformFeedbackBufferStart = 35972,
	TransformFeedbackPaused = 36387,
	UniformBufferBinding = 35368,
	UniformBufferOffsetAlignment = 35380,
	UniformBufferSize = 35370,
	UniformBufferStart = 35369,
	UnpackAlignment = 3317,
	UnpackImageHeight = 32878,
	UnpackRowLength = 3314,
	UnpackSkipImages = 32877,
	UnpackSkipPixels = 3316,
	UnpackSkipRows = 3315,
	VertexArrayBinding = 34229,
	Viewport = 2978,
}
```

### New Type OpenTK.Graphics.ES30.GetQueryObjectParam

```
[Serializable]
public enum GetQueryObjectParam {
	QueryResult = 34918,
	QueryResultAvailable = 34919,
}
```

### New Type OpenTK.Graphics.ES30.GetQueryParam

```
[Serializable]
public enum GetQueryParam {
	CurrentQuery = 34917,
}
```

### New Type OpenTK.Graphics.ES30.GetTextureParameter

```
[Serializable]
public enum GetTextureParameter {
	CompressedTextureFormats = 34467,
	NumCompressedTextureFormats = 34466,
	TextureBaseLevel = 33084,
	TextureCompareFunc = 34893,
	TextureCompareMode = 34892,
	TextureImmutableFormat = 37167,
	TextureMagFilter = 10240,
	TextureMaxLevel = 33085,
	TextureMaxLod = 33083,
	TextureMinFilter = 10241,
	TextureMinLod = 33082,
	TextureSwizzleA = 36421,
	TextureSwizzleB = 36420,
	TextureSwizzleG = 36419,
	TextureSwizzleR = 36418,
	TextureWrapR = 32882,
	TextureWrapS = 10242,
	TextureWrapT = 10243,
}
```

### New Type OpenTK.Graphics.ES30.GL

```
public sealed class GL : OpenTK.Graphics.GraphicsBindingsBase {
	// constructors
	public GL ();
	// fields
	public static const string Library = "libGLESv2.dll";
	// properties
	protected override object SyncRoot { get; }
	// methods
	public static void ActiveTexture (TextureUnit texture);
	public static void AttachShader (uint program, uint shader);
	public static void AttachShader (int program, int shader);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BeginQuery (All target, int id);
	public static void BeginQuery (QueryTarget target, uint id);
	public static void BeginQuery (QueryTarget target, int id);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BeginQuery (All target, uint id);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BeginTransformFeedback (All primitiveMode);
	public static void BeginTransformFeedback (TransformFeedbackPrimitiveType primitiveMode);
	public static void BindAttribLocation (int program, int index, string name);
	public static void BindAttribLocation (uint program, uint index, string name);
	public static void BindBuffer (BufferTarget target, uint buffer);
	public static void BindBuffer (BufferTarget target, int buffer);
	public static void BindBufferBase (BufferRangeTarget target, int index, int buffer);
	public static void BindBufferBase (BufferRangeTarget target, uint index, uint buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBufferBase (All target, uint index, uint buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBufferBase (All target, int index, int buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBufferRange (All target, int index, int buffer, System.IntPtr offset, System.IntPtr size);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBufferRange (All target, uint index, uint buffer, System.IntPtr offset, System.IntPtr size);
	public static void BindBufferRange (BufferRangeTarget target, int index, int buffer, System.IntPtr offset, System.IntPtr size);
	public static void BindBufferRange (BufferRangeTarget target, uint index, uint buffer, System.IntPtr offset, System.IntPtr size);
	public static void BindFramebuffer (FramebufferTarget target, uint framebuffer);
	public static void BindFramebuffer (FramebufferTarget target, int framebuffer);
	public static void BindRenderbuffer (RenderbufferTarget target, int renderbuffer);
	public static void BindRenderbuffer (RenderbufferTarget target, uint renderbuffer);
	public static void BindSampler (uint unit, uint sampler);
	public static void BindSampler (int unit, int sampler);
	public static void BindTexture (TextureTarget target, uint texture);
	public static void BindTexture (TextureTarget target, int texture);
	public static void BindTransformFeedback (TransformFeedbackTarget target, int id);
	public static void BindTransformFeedback (TransformFeedbackTarget target, uint id);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTransformFeedback (All target, int id);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTransformFeedback (All target, uint id);
	public static void BindVertexArray (int array);
	public static void BindVertexArray (uint array);
	public static void BlendColor (OpenTK.Graphics.Color4 color);
	public static void BlendColor (System.Drawing.Color color);
	public static void BlendColor (float red, float green, float blue, float alpha);
	public static void BlendEquation (BlendEquationMode mode);
	public static void BlendEquationSeparate (BlendEquationMode modeRGB, BlendEquationMode modeAlpha);
	public static void BlendFunc (BlendingFactorSrc sfactor, BlendingFactorDest dfactor);
	public static void BlendFuncSeparate (BlendingFactorSrc srcRGB, BlendingFactorDest dstRGB, BlendingFactorSrc srcAlpha, BlendingFactorDest dstAlpha);
	public static void BlitFramebuffer (int srcX0, int srcY0, int srcX1, int srcY1, int dstX0, int dstY0, int dstX1, int dstY1, ClearBufferMask mask, BlitFramebufferFilter filter);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlitFramebuffer (int srcX0, int srcY0, int srcX1, int srcY1, int dstX0, int dstY0, int dstX1, int dstY1, int mask, All filter);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlitFramebuffer (int srcX0, int srcY0, int srcX1, int srcY1, int dstX0, int dstY0, int dstX1, int dstY1, uint mask, All filter);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, out T2 data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[0...,0...,0...] data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[0...,0...] data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[] data, BufferUsage usage);
	public static void BufferData (BufferTarget target, System.IntPtr size, System.IntPtr data, BufferUsage usage);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[] data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, out T3 data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[0...,0...,0...] data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[0...,0...] data);
	public static void BufferSubData (BufferTarget target, System.IntPtr offset, System.IntPtr size, System.IntPtr data);
	public static FramebufferErrorCode CheckFramebufferStatus (FramebufferTarget target);
	public static void Clear (ClearBufferMask mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, float depth, int stencil);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, float[] value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, ref float value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, float* value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, uint* value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, ref uint value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, uint[] value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, int* value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, ref int value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, uint* value);
	public static void ClearBuffer (ClearBufferCombined buffer, int drawbuffer, float depth, int stencil);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, float[] value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, ref float value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, float* value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, int[] value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, ref int value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, int* value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, uint[] value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, ref uint value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, int[] value);
	public static void ClearColor (System.Drawing.Color color);
	public static void ClearColor (OpenTK.Graphics.Color4 color);
	public static void ClearColor (float red, float green, float blue, float alpha);
	public static void ClearDepth (float depth);
	public static void ClearStencil (int s);
	public static All ClientWaitSync (System.IntPtr sync, int flags, long timeout);
	public static All ClientWaitSync (System.IntPtr sync, uint flags, ulong timeout);
	public static void ColorMask (bool red, bool green, bool blue, bool alpha);
	public static void CompileShader (int shader);
	public static void CompileShader (uint shader);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[0...,0...,0...] data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[0...,0...] data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, out T7 data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[] data);
	public static void CompressedTexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, System.IntPtr data);
	public static void CompressedTexImage3D<T8> (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, out T8 data);
	public static void CompressedTexImage3D (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, System.IntPtr data);
	public static void CompressedTexImage3D<T8> (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, T8[] data);
	public static void CompressedTexImage3D<T8> (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...] data);
	public static void CompressedTexImage3D<T8> (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, out T8 data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[0...,0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, out T8 data);
	public static void CompressedTexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[0...,0...] data);
	public static void CompressedTexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, out T10 data);
	public static void CompressedTexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, T10[0...,0...,0...] data);
	public static void CompressedTexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, T10[0...,0...] data);
	public static void CompressedTexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, T10[] data);
	public static void CompressedTexSubImage3D (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, out T10 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyBufferSubData (All readTarget, All writeTarget, System.IntPtr readOffset, System.IntPtr writeOffset, System.IntPtr size);
	public static void CopyBufferSubData (BufferTarget readTarget, BufferTarget writeTarget, System.IntPtr readOffset, System.IntPtr writeOffset, System.IntPtr size);
	public static void CopyTexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int x, int y, int width, int height, int border);
	public static void CopyTexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyTexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int x, int y, int width, int height);
	public static void CopyTexSubImage3D (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int x, int y, int width, int height);
	public static int CreateProgram ();
	public static int CreateShader (ShaderType type);
	public static void CullFace (CullFaceMode mode);
	public static void DeleteBuffers (int n, uint* buffers);
	public static void DeleteBuffers (int n, ref uint buffers);
	public static void DeleteBuffers (int n, uint[] buffers);
	public static void DeleteBuffers (int n, int* buffers);
	public static void DeleteBuffers (int n, ref int buffers);
	public static void DeleteBuffers (int n, int[] buffers);
	public static void DeleteFramebuffers (int n, uint* framebuffers);
	public static void DeleteFramebuffers (int n, ref uint framebuffers);
	public static void DeleteFramebuffers (int n, uint[] framebuffers);
	public static void DeleteFramebuffers (int n, int* framebuffers);
	public static void DeleteFramebuffers (int n, ref int framebuffers);
	public static void DeleteFramebuffers (int n, int[] framebuffers);
	public static void DeleteProgram (uint program);
	public static void DeleteProgram (int program);
	public static void DeleteQueries (int n, uint* ids);
	public static void DeleteQueries (int n, ref uint ids);
	public static void DeleteQueries (int n, uint[] ids);
	public static void DeleteQueries (int n, int* ids);
	public static void DeleteQueries (int n, ref int ids);
	public static void DeleteQueries (int n, int[] ids);
	public static void DeleteRenderbuffers (int n, uint* renderbuffers);
	public static void DeleteRenderbuffers (int n, ref uint renderbuffers);
	public static void DeleteRenderbuffers (int n, uint[] renderbuffers);
	public static void DeleteRenderbuffers (int n, int* renderbuffers);
	public static void DeleteRenderbuffers (int n, ref int renderbuffers);
	public static void DeleteRenderbuffers (int n, int[] renderbuffers);
	public static void DeleteSamplers (int count, uint* samplers);
	public static void DeleteSamplers (int count, ref uint samplers);
	public static void DeleteSamplers (int count, uint[] samplers);
	public static void DeleteSamplers (int count, int* samplers);
	public static void DeleteSamplers (int count, ref int samplers);
	public static void DeleteSamplers (int count, int[] samplers);
	public static void DeleteShader (uint shader);
	public static void DeleteShader (int shader);
	public static void DeleteSync (System.IntPtr sync);
	public static void DeleteTexture (uint id);
	public static void DeleteTexture (int id);
	public static void DeleteTextures (int n, ref int textures);
	public static void DeleteTextures (int n, int* textures);
	public static void DeleteTextures (int n, uint[] textures);
	public static void DeleteTextures (int n, ref uint textures);
	public static void DeleteTextures (int n, uint* textures);
	public static void DeleteTextures (int n, int[] textures);
	public static void DeleteTransformFeedback (int n, uint* ids);
	public static void DeleteTransformFeedback (int n, uint[] ids);
	public static void DeleteTransformFeedback (int n, ref uint ids);
	public static void DeleteTransformFeedback (int n, int* ids);
	public static void DeleteTransformFeedback (int n, ref int ids);
	public static void DeleteTransformFeedback (int n, int[] ids);
	public static void DeleteVertexArrays (int n, uint* arrays);
	public static void DeleteVertexArrays (int n, ref uint arrays);
	public static void DeleteVertexArrays (int n, uint[] arrays);
	public static void DeleteVertexArrays (int n, int* arrays);
	public static void DeleteVertexArrays (int n, int[] arrays);
	public static void DeleteVertexArrays (int n, ref int arrays);
	public static void DepthFunc (DepthFunction func);
	public static void DepthMask (bool flag);
	public static void DepthRange (float zNear, float zFar);
	public static void DetachShader (int program, int shader);
	public static void DetachShader (uint program, uint shader);
	public static void Disable (EnableCap cap);
	public static void DisableVertexAttribArray (int index);
	public static void DisableVertexAttribArray (uint index);
	public static void DrawArrays (BeginMode mode, int first, int count);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawArraysInstanced (All mode, int first, int count, int instanceCount);
	public static void DrawArraysInstanced (PrimitiveType mode, int first, int count, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawBuffers (int n, All[] bufs);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawBuffers (int n, ref All bufs);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawBuffers (int n, All* bufs);
	public static void DrawBuffers (int n, DrawBufferMode* bufs);
	public static void DrawBuffers (int n, ref DrawBufferMode bufs);
	public static void DrawBuffers (int n, DrawBufferMode[] bufs);
	public static void DrawElements (BeginMode mode, int count, DrawElementsType type, int offset);
	public static void DrawElements (BeginMode mode, int count, DrawElementsType type, System.IntPtr indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[0...,0...] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[0...,0...,0...] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, out T3 indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, out T3 indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[0...,0...] indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[] indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced (All mode, int count, All type, System.IntPtr indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[0...,0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (PrimitiveType mode, int count, DrawElementsType type, out T3 indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (PrimitiveType mode, int count, DrawElementsType type, T3[0...,0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (PrimitiveType mode, int count, DrawElementsType type, T3[0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (PrimitiveType mode, int count, DrawElementsType type, T3[] indices, int instanceCount);
	public static void DrawElementsInstanced (PrimitiveType mode, int count, DrawElementsType type, System.IntPtr indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, out T5 indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements (All mode, uint start, uint end, int count, All type, System.IntPtr indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, uint start, uint end, int count, All type, T5[] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, uint start, uint end, int count, All type, T5[0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, uint start, uint end, int count, All type, T5[0...,0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, uint start, uint end, int count, All type, out T5 indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5[0...,0...,0...] indices);
	public static void DrawRangeElements (PrimitiveType mode, int start, int end, int count, DrawElementsType type, System.IntPtr indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, int start, int end, int count, DrawElementsType type, T5[] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, int start, int end, int count, DrawElementsType type, T5[0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements (All mode, int start, int end, int count, All type, System.IntPtr indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5[] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5[0...,0...] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, T5[0...,0...] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, out T5 indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, T5[0...,0...,0...] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, int start, int end, int count, DrawElementsType type, T5[0...,0...,0...] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, T5[] indices);
	public static void DrawRangeElements (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, System.IntPtr indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, int start, int end, int count, DrawElementsType type, out T5 indices);
	public static void Enable (EnableCap cap);
	public static void EnableVertexAttribArray (int index);
	public static void EnableVertexAttribArray (uint index);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void EndQuery (All target);
	public static void EndQuery (QueryTarget target);
	public static void EndTransformFeedback ();
	public static System.IntPtr FenceSync (SyncCondition condition, WaitSyncFlags flags);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static System.IntPtr FenceSync (All condition, uint flags);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static System.IntPtr FenceSync (All condition, int flags);
	public static void Finish ();
	public static void Flush ();

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FlushMappedBufferRange (All target, System.IntPtr offset, System.IntPtr length);
	public static void FlushMappedBufferRange (BufferTarget target, System.IntPtr offset, System.IntPtr length);
	public static void FramebufferRenderbuffer (FramebufferTarget target, FramebufferSlot attachment, RenderbufferTarget renderbuffertarget, int renderbuffer);
	public static void FramebufferRenderbuffer (FramebufferTarget target, FramebufferSlot attachment, RenderbufferTarget renderbuffertarget, uint renderbuffer);
	public static void FramebufferTexture2D (FramebufferTarget target, FramebufferSlot attachment, TextureTarget textarget, uint texture, int level);
	public static void FramebufferTexture2D (FramebufferTarget target, FramebufferSlot attachment, TextureTarget textarget, int texture, int level);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTextureLayer (All target, All attachment, uint texture, int level, int layer);
	public static void FramebufferTextureLayer (FramebufferTarget target, FramebufferAttachment attachment, uint texture, int level, int layer);
	public static void FramebufferTextureLayer (FramebufferTarget target, FramebufferAttachment attachment, int texture, int level, int layer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTextureLayer (All target, All attachment, int texture, int level, int layer);
	public static void FrontFace (FrontFaceDirection mode);
	public static void GenBuffers (int n, out int buffers);
	public static void GenBuffers (int n, int* buffers);
	public static void GenBuffers (int n, uint[] buffers);
	public static void GenBuffers (int n, int[] buffers);
	public static void GenBuffers (int n, uint* buffers);
	public static void GenBuffers (int n, out uint buffers);
	public static void GenerateMipmap (TextureTarget target);
	public static void GenFramebuffers (int n, uint* framebuffers);
	public static void GenFramebuffers (int n, out uint framebuffers);
	public static void GenFramebuffers (int n, uint[] framebuffers);
	public static void GenFramebuffers (int n, int* framebuffers);
	public static void GenFramebuffers (int n, out int framebuffers);
	public static void GenFramebuffers (int n, int[] framebuffers);
	public static void GenQueries (int n, uint* ids);
	public static void GenQueries (int n, out uint ids);
	public static void GenQueries (int n, uint[] ids);
	public static void GenQueries (int n, int* ids);
	public static void GenQueries (int n, out int ids);
	public static void GenQueries (int n, int[] ids);
	public static void GenRenderbuffers (int n, int[] renderbuffers);
	public static void GenRenderbuffers (int n, out int renderbuffers);
	public static void GenRenderbuffers (int n, int* renderbuffers);
	public static void GenRenderbuffers (int n, uint* renderbuffers);
	public static void GenRenderbuffers (int n, out uint renderbuffers);
	public static void GenRenderbuffers (int n, uint[] renderbuffers);
	public static void GenSamplers (int count, uint* samplers);
	public static void GenSamplers (int count, out uint samplers);
	public static void GenSamplers (int count, uint[] samplers);
	public static void GenSamplers (int count, int* samplers);
	public static void GenSamplers (int count, out int samplers);
	public static void GenSamplers (int count, int[] samplers);
	public static int GenTexture ();
	public static void GenTextures (int n, out uint textures);
	public static void GenTextures (int n, uint[] textures);
	public static void GenTextures (int n, int* textures);
	public static void GenTextures (int n, out int textures);
	public static void GenTextures (int n, int[] textures);
	public static void GenTextures (int n, uint* textures);
	public static void GenTransformFeedback (int n, int[] ids);
	public static void GenTransformFeedback (int n, out int ids);
	public static void GenTransformFeedback (int n, int* ids);
	public static void GenTransformFeedback (int n, uint[] ids);
	public static void GenTransformFeedback (int n, out uint ids);
	public static void GenTransformFeedback (int n, uint* ids);
	public static void GenVertexArrays (int n, uint* arrays);
	public static void GenVertexArrays (int n, out uint arrays);
	public static void GenVertexArrays (int n, uint[] arrays);
	public static void GenVertexArrays (int n, int* arrays);
	public static void GenVertexArrays (int n, out int arrays);
	public static void GenVertexArrays (int n, int[] arrays);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int* length, int* size, ActiveAttribType* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, int[] length, int[] size, ActiveAttribType[] type, System.Text.StringBuilder name);
	public static string GetActiveAttrib (int program, int index, out int size, out ActiveAttribType type);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, out int length, out int size, out ActiveAttribType type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int[] length, int[] size, ActiveAttribType[] type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, int* length, int* size, ActiveAttribType* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, out int length, out int size, out ActiveAttribType type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, out int length, out int size, out ActiveUniformType type, System.Text.StringBuilder name);
	public static string GetActiveUniform (int program, int uniformIndex, out int size, out ActiveUniformType type);
	public static void GetActiveUniform (uint program, uint index, int bufsize, int* length, int* size, ActiveUniformType* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, int[] length, int[] size, ActiveUniformType[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, int* length, int* size, ActiveUniformType* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, out int length, out int size, out ActiveUniformType type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, int[] length, int[] size, ActiveUniformType[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, int[] params);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, ActiveUniformBlockParameter pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, int* params);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, ActiveUniformBlockParameter pname, out int params);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, ActiveUniformBlockParameter pname, int[] params);
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, ActiveUniformBlockParameter pname, int* params);
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, ActiveUniformBlockParameter pname, out int params);
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, ActiveUniformBlockParameter pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, int* params);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, int* length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, out int length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, int[] length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, int* length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, out int length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, int[] length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniforms (int program, int uniformCount, out int uniformIndices, ActiveUniformParameter pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (int program, int uniformCount, int[] uniformIndices, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (int program, int uniformCount, out int uniformIndices, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (int program, int uniformCount, int* uniformIndices, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (uint program, int uniformCount, uint[] uniformIndices, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (uint program, int uniformCount, out uint uniformIndices, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (uint program, int uniformCount, uint* uniformIndices, All pname, int* params);
	public static void GetActiveUniforms (uint program, int uniformCount, uint[] uniformIndices, ActiveUniformParameter pname, int[] params);
	public static void GetActiveUniforms (int program, int uniformCount, int* uniformIndices, ActiveUniformParameter pname, int* params);
	public static void GetActiveUniforms (int program, int uniformCount, int[] uniformIndices, ActiveUniformParameter pname, int[] params);
	public static void GetActiveUniforms (uint program, int uniformCount, out uint uniformIndices, ActiveUniformParameter pname, out int params);
	public static void GetActiveUniforms (uint program, int uniformCount, uint* uniformIndices, ActiveUniformParameter pname, int* params);
	public static void GetAttachedShaders (int program, int maxcount, int[] count, int[] shaders);
	public static void GetAttachedShaders (int program, int maxcount, int* count, int* shaders);
	public static void GetAttachedShaders (uint program, int maxcount, int[] count, uint[] shaders);
	public static void GetAttachedShaders (uint program, int maxcount, out int count, out uint shaders);
	public static void GetAttachedShaders (uint program, int maxcount, int* count, uint* shaders);
	public static void GetAttachedShaders (int program, int maxcount, out int count, out int shaders);
	public static int GetAttribLocation (uint program, string name);
	public static int GetAttribLocation (int program, string name);
	public static void GetBoolean (GetPName pname, out bool params);
	public static void GetBoolean (GetPName pname, bool* params);
	public static void GetBoolean (GetPName pname, bool[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, long[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, out long params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, out long params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, long* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, long[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, int* params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, out int params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, long* params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer (All target, All pname, System.IntPtr params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer<T2> (All target, All pname, T2[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer<T2> (All target, All pname, T2[0...,0...] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer<T2> (All target, All pname, T2[0...,0...,0...] params);
	public static void GetBufferPointer (BufferTarget target, BufferPointer pname, System.IntPtr params);
	public static void GetBufferPointer<T2> (BufferTarget target, BufferPointer pname, T2[] params);
	public static void GetBufferPointer<T2> (BufferTarget target, BufferPointer pname, T2[0...,0...] params);
	public static void GetBufferPointer<T2> (BufferTarget target, BufferPointer pname, T2[0...,0...,0...] params);
	public static void GetBufferPointer<T2> (BufferTarget target, BufferPointer pname, out T2 params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer<T2> (All target, All pname, out T2 params);

	[Obsolete ("Use the GetErrorCode method, for compatability with Xamarin Android's OpenTK-1.0")]
	public static All GetError ();
	public static ErrorCode GetErrorCode ();
	public static void GetFloat (GetPName pname, float* params);
	public static void GetFloat (GetPName pname, out float params);
	public static void GetFloat (GetPName pname, float[] params);
	public static void GetFloat (GetPName pname, out OpenTK.Vector2 vector);
	public static void GetFloat (GetPName pname, out OpenTK.Matrix4 matrix);
	public static void GetFloat (GetPName pname, out OpenTK.Vector4 vector);
	public static void GetFloat (GetPName pname, out OpenTK.Vector3 vector);
	public static int GetFragDataLocation (uint program, System.Text.StringBuilder name);
	public static int GetFragDataLocation (int program, System.Text.StringBuilder name);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, int* params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, out int params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, int* data);
	public static void GetInteger (GetIndexedPName target, uint index, out long data);
	public static void GetInteger (GetIndexedPName target, uint index, long[] data);
	public static void GetInteger (GetIndexedPName target, int index, long* data);
	public static void GetInteger (GetIndexedPName target, int index, out long data);
	public static void GetInteger (GetIndexedPName target, int index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, int* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, int[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, out int data);
	public static void GetInteger (GetIndexedPName target, uint index, long* data);
	public static void GetInteger (GetPName pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, int[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, long* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, out long data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, long* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, out long data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, long[] data);
	public static void GetInteger (GetPName pname, int* params);
	public static void GetInteger (GetIndexedPName target, int index, int[] data);
	public static void GetInteger (GetIndexedPName target, int index, out int data);
	public static void GetInteger (GetIndexedPName target, int index, int* data);
	public static void GetInteger (GetIndexedPName target, uint index, int[] data);
	public static void GetInteger (GetIndexedPName target, uint index, out int data);
	public static void GetInteger (GetIndexedPName target, uint index, int* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, out int data);
	public static void GetInteger (GetPName pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All pname, long[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All pname, out long params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All pname, long* params);
	public static void GetInteger64 (GetPName pname, long* params);
	public static void GetInteger64 (GetPName pname, out long params);
	public static void GetInteger64 (GetPName pname, long[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, int* params);
	public static void GetInternalformat (ImageTarget target, SizedInternalFormat internalformat, InternalFormatParameter pname, int bufSize, int* params);
	public static void GetInternalformat (ImageTarget target, SizedInternalFormat internalformat, InternalFormatParameter pname, int bufSize, int[] params);
	public static void GetInternalformat (ImageTarget target, SizedInternalFormat internalformat, InternalFormatParameter pname, int bufSize, out int params);
	public static void GetProgram (int program, ProgramParameter pname, int[] params);
	public static void GetProgram (int program, ProgramParameter pname, out int params);
	public static void GetProgram (uint program, ProgramParameter pname, int* params);
	public static void GetProgram (uint program, ProgramParameter pname, out int params);
	public static void GetProgram (uint program, ProgramParameter pname, int[] params);
	public static void GetProgram (int program, ProgramParameter pname, int* params);
	public static void GetProgramBinary<T4> (int program, int bufSize, out int length, out All binaryFormat, out T4 binary);
	public static void GetProgramBinary (int program, int bufSize, int* length, All* binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int* length, All* binaryFormat, T4[] binary);
	public static void GetProgramBinary (uint program, int bufSize, int[] length, All[] binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int* length, All* binaryFormat, out T4 binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int* length, All* binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int* length, All* binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, out int length, out All binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary (int program, int bufSize, int[] length, All[] binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int[] length, All[] binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int[] length, All[] binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int[] length, All[] binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int[] length, All[] binaryFormat, out T4 binary);
	public static void GetProgramBinary (int program, int bufSize, out int length, out All binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, out int length, out All binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, out int length, out All binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int[] length, All[] binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, out int length, out All binaryFormat, out T4 binary);
	public static void GetProgramBinary (uint program, int bufSize, int* length, All* binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int* length, All* binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int* length, All* binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int* length, All* binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int* length, All* binaryFormat, out T4 binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, out int length, out All binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int[] length, All[] binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int[] length, All[] binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int[] length, All[] binaryFormat, out T4 binary);
	public static void GetProgramBinary (uint program, int bufSize, out int length, out All binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, out int length, out All binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, out int length, out All binaryFormat, T4[0...,0...] binary);
	public static string GetProgramInfoLog (int program);
	public static void GetProgramInfoLog (uint program, int bufsize, int[] length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (uint program, int bufsize, out int length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (uint program, int bufsize, int* length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (int program, out string info);
	public static void GetProgramInfoLog (int program, int bufsize, int* length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (int program, int bufsize, out int length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (int program, int bufsize, int[] length, System.Text.StringBuilder infolog);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQuery (All target, All pname, int* params);
	public static void GetQuery (QueryTarget target, GetQueryParam pname, int* params);
	public static void GetQuery (QueryTarget target, GetQueryParam pname, out int params);
	public static void GetQuery (QueryTarget target, GetQueryParam pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQuery (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQuery (All target, All pname, out int params);
	public static void GetQueryObject (uint id, GetQueryObjectParam pname, uint* params);
	public static void GetQueryObject (uint id, GetQueryObjectParam pname, out uint params);
	public static void GetQueryObject (int id, GetQueryObjectParam pname, int* params);
	public static void GetQueryObject (int id, GetQueryObjectParam pname, out int params);
	public static void GetQueryObject (int id, GetQueryObjectParam pname, int[] params);
	public static void GetQueryObject (uint id, GetQueryObjectParam pname, uint[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (int id, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (uint id, All pname, uint* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (uint id, All pname, out uint params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (uint id, All pname, uint[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (int id, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (int id, All pname, int[] params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, int* params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, out int params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, float[] params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, float[] params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, out float params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, int* params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, out int params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, int[] params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, int* params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, out int params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, float* params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, float[] params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, out float params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, float* params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, int[] params);
	public static void GetShader (int shader, ShaderParameter pname, int[] params);
	public static void GetShader (int shader, ShaderParameter pname, int* params);
	public static void GetShader (uint shader, ShaderParameter pname, int[] params);
	public static void GetShader (uint shader, ShaderParameter pname, out int params);
	public static void GetShader (uint shader, ShaderParameter pname, int* params);
	public static void GetShader (int shader, ShaderParameter pname, out int params);
	public static void GetShaderInfoLog (uint shader, int bufsize, out int length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (uint shader, int bufsize, int* length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (uint shader, int bufsize, int[] length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (int shader, int bufsize, int* length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (int shader, int bufsize, out int length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (int shader, int bufsize, int[] length, System.Text.StringBuilder infolog);
	public static string GetShaderInfoLog (int shader);
	public static void GetShaderInfoLog (int shader, out string info);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, int[] range, int[] precision);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, out int range, out int precision);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, int* range, int* precision);
	public static void GetShaderSource (uint shader, int bufsize, int* length, System.Text.StringBuilder source);
	public static void GetShaderSource (uint shader, int bufsize, out int length, System.Text.StringBuilder source);
	public static void GetShaderSource (uint shader, int bufsize, int[] length, System.Text.StringBuilder source);
	public static void GetShaderSource (int shader, int bufsize, int* length, System.Text.StringBuilder source);
	public static void GetShaderSource (int shader, int bufsize, int[] length, System.Text.StringBuilder source);
	public static void GetShaderSource (int shader, int bufsize, out int length, System.Text.StringBuilder source);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (StringName name, int index);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (StringName name, uint index);
	public static byte GetString (StringNameIndexed name, int index);
	public static byte GetString (StringNameIndexed name, uint index);
	public static string GetString (StringName name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, out int length, out int values);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, int* length, int* values);
	public static void GetSync (System.IntPtr sync, SyncParameterName pname, int bufSize, out int length, out int values);
	public static void GetSync (System.IntPtr sync, SyncParameterName pname, int bufSize, int[] length, int[] values);
	public static void GetSync (System.IntPtr sync, SyncParameterName pname, int bufSize, int* length, int* values);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, int[] length, int[] values);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, int* params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, out int params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, int[] params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, float* params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, out float params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, float[] params);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, out int length, out int size, out TransformFeedbackType type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, out int length, out int size, out All type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, int[] length, int[] size, TransformFeedbackType[] type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, int* length, int* size, TransformFeedbackType* type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, out int length, out int size, out TransformFeedbackType type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, int* length, int* size, TransformFeedbackType* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, out int length, out int size, out All type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, int[] length, int[] size, TransformFeedbackType[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);
	public static void GetUniform (uint program, int location, uint[] params);
	public static void GetUniform (uint program, int location, int* params);
	public static void GetUniform (uint program, int location, out int params);
	public static void GetUniform (uint program, int location, float[] params);
	public static void GetUniform (uint program, int location, out float params);
	public static void GetUniform (int program, int location, out float params);
	public static void GetUniform (int program, int location, float[] params);
	public static void GetUniform (uint program, int location, float* params);
	public static void GetUniform (int program, int location, int[] params);
	public static void GetUniform (int program, int location, float* params);
	public static void GetUniform (int program, int location, int* params);
	public static void GetUniform (uint program, int location, int[] params);
	public static void GetUniform (int program, int location, out int params);
	public static void GetUniform (uint program, int location, out uint params);
	public static void GetUniform (uint program, int location, uint* params);
	public static int GetUniformBlockIndex (uint program, System.Text.StringBuilder uniformBlockName);
	public static int GetUniformBlockIndex (int program, System.Text.StringBuilder uniformBlockName);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, int[] uniformIndices);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, out int uniformIndices);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, int* uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, uint[] uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, out uint uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, uint* uniformIndices);
	public static int GetUniformLocation (uint program, string name);
	public static int GetUniformLocation (int program, string name);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, float[] params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, out float params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, float* params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, float[] params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, out float params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, float* params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, int* params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, uint[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (int index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (int index, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (int index, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, out int params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, out uint params);
	public static void GetVertexAttribI (int index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, uint* params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, out uint params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, uint[] params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttribI (int index, VertexAttribParameter pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, uint* params);
	public static void GetVertexAttribI (int index, VertexAttribParameter pname, int* params);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[] pointer);
	public static void GetVertexAttribPointer (uint index, VertexAttribPointerParameter pname, System.IntPtr pointer);
	public static void GetVertexAttribPointer (int index, VertexAttribPointerParameter pname, System.IntPtr pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[] pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, out T2 pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, out T2 pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[0...,0...,0...] pointer);
	public static void Hint (HintTarget target, HintMode mode);
	public static void InvalidateFramebuffer (FramebufferTarget target, int numAttachments, FramebufferAttachment* attachments);
	public static void InvalidateFramebuffer (FramebufferTarget target, int numAttachments, ref FramebufferAttachment attachments);
	public static void InvalidateFramebuffer (FramebufferTarget target, int numAttachments, FramebufferAttachment[] attachments);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateFramebuffer (All target, int numAttachments, All[] attachments);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateFramebuffer (All target, int numAttachments, ref All attachments);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateFramebuffer (All target, int numAttachments, All* attachments);
	public static void InvalidateSubFramebuffer (FramebufferTarget target, int numAttachments, FramebufferAttachment[] attachments, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateSubFramebuffer (All target, int numAttachments, All* attachments, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateSubFramebuffer (All target, int numAttachments, ref All attachments, int x, int y, int width, int height);
	public static void InvalidateSubFramebuffer (FramebufferTarget target, int numAttachments, FramebufferAttachment* attachments, int x, int y, int width, int height);
	public static void InvalidateSubFramebuffer (FramebufferTarget target, int numAttachments, ref FramebufferAttachment attachments, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateSubFramebuffer (All target, int numAttachments, All[] attachments, int x, int y, int width, int height);
	public static bool IsBuffer (int buffer);
	public static bool IsBuffer (uint buffer);
	public static bool IsEnabled (EnableCap cap);
	public static bool IsFramebuffer (int framebuffer);
	public static bool IsFramebuffer (uint framebuffer);
	public static bool IsProgram (uint program);
	public static bool IsProgram (int program);
	public static bool IsQuery (int id);
	public static bool IsQuery (uint id);
	public static bool IsRenderbuffer (int renderbuffer);
	public static bool IsRenderbuffer (uint renderbuffer);
	public static bool IsSampler (int sampler);
	public static bool IsSampler (uint sampler);
	public static bool IsShader (int shader);
	public static bool IsShader (uint shader);
	public static bool IsSync (System.IntPtr sync);
	public static bool IsTexture (uint texture);
	public static bool IsTexture (int texture);
	public static bool IsTransformFeedback (int id);
	public static bool IsTransformFeedback (uint id);
	public static bool IsVertexArray (int array);
	public static bool IsVertexArray (uint array);
	public static void LineWidth (float width);
	public static void LinkProgram (uint program);
	public static void LinkProgram (int program);
	public static System.IntPtr MapBufferRange (BufferTarget target, System.IntPtr offset, System.IntPtr length, BufferAccessMask access);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, int access);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, uint access);
	public static void PauseTransformFeedback ();
	public static void PixelStore (PixelStoreParameter pname, int param);
	public static void PolygonOffset (float factor, float units);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[0...,0...] binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[] binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, out T2 binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[0...,0...,0...] binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[0...,0...] binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[] binary, int length);
	public static void ProgramBinary (uint program, All binaryFormat, System.IntPtr binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, out T2 binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[0...,0...,0...] binary, int length);
	public static void ProgramBinary (int program, All binaryFormat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ProgramParameter (int program, All pname, int value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ProgramParameter (uint program, All pname, int value);
	public static void ProgramParameter (uint program, ProgramParameterName pname, int value);
	public static void ProgramParameter (int program, ProgramParameterName pname, int value);
	public static void ReadBuffer (ReadBufferMode mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadBuffer (All mode);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[0...,0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, out T6 pixels);
	public static void ReadPixels (int x, int y, int width, int height, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[0...,0...] pixels);
	public static void ReleaseShaderCompiler ();
	public static void RenderbufferStorage (RenderbufferTarget target, RenderbufferInternalFormat internalformat, int width, int height);
	public static void RenderbufferStorageMultisample (RenderbufferTarget target, int samples, RenderbufferInternalFormat internalformat, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void RenderbufferStorageMultisample (All target, int samples, All internalformat, int width, int height);
	public static void ResumeTransformFeedback ();
	public static void SampleCoverage (float value, bool invert);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, int[] param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, int* param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, int[] param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, int* param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, int param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, float* param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, float[] param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, int param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, float param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, float[] param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, float* param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, int* param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, int[] param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, int* param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, float[] param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, float* param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, int[] param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, float* param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, float[] param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, float param);
	public static void Scissor (int x, int y, int width, int height);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, uint[] shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary (int n, uint* shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, ref uint shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, int[] shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, int* shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary (int n, ref int shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderSource (uint shader, int count, string[] string, int* length);
	public static void ShaderSource (uint shader, int count, string[] string, int[] length);
	public static void ShaderSource (int shader, int count, string[] string, int* length);
	public static void ShaderSource (int shader, int count, string[] string, ref int length);
	public static void ShaderSource (int shader, int count, string[] string, int[] length);
	public static void ShaderSource (uint shader, int count, string[] string, ref int length);
	public static void ShaderSource (int shader, string string);
	public static void StencilFunc (StencilFunction func, int ref, uint mask);
	public static void StencilFunc (StencilFunction func, int ref, int mask);
	public static void StencilFuncSeparate (CullFaceMode face, StencilFunction func, int ref, uint mask);
	public static void StencilFuncSeparate (CullFaceMode face, StencilFunction func, int ref, int mask);
	public static void StencilMask (uint mask);
	public static void StencilMask (int mask);
	public static void StencilMaskSeparate (CullFaceMode face, uint mask);
	public static void StencilMaskSeparate (CullFaceMode face, int mask);
	public static void StencilOp (StencilOp fail, StencilOp zfail, StencilOp zpass);
	public static void StencilOpSeparate (CullFaceMode face, StencilOp fail, StencilOp zfail, StencilOp zpass);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, out T8 pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[0...,0...,0...] pixels);
	public static void TexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[] pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[0...,0...] pixels);
	public static void TexImage3D<T9> (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, out T9 pixels);
	public static void TexImage3D<T9> (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, T9[0...,0...,0...] pixels);
	public static void TexImage3D<T9> (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, T9[0...,0...] pixels);
	public static void TexImage3D<T9> (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, T9[] pixels);
	public static void TexImage3D (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, out T9 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, System.IntPtr pixels);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int* params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int[] params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int param);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float* params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float[] params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexStorage2D (All target, int levels, All internalformat, int width, int height);
	public static void TexStorage2D (TextureTarget2D target, int levels, SizedInternalFormat internalformat, int width, int height);
	public static void TexStorage3D (TextureTarget3D target, int levels, SizedInternalFormat internalformat, int width, int height, int depth);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexStorage3D (All target, int levels, All internalformat, int width, int height, int depth);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, out T8 pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[0...,0...,0...] pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[0...,0...] pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[] pixels);
	public static void TexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, out T10 pixels);
	public static void TexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, T10[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, out T10 pixels);
	public static void TexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, T10[0...,0...] pixels);
	public static void TexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, T10[] pixels);
	public static void TexSubImage3D (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TransformFeedbackVaryings (int program, int count, string varyings, All bufferMode);
	public static void TransformFeedbackVaryings (uint program, int count, string varyings, All bufferMode);
	public static void TransformFeedbackVaryings (int program, int count, string varyings, TransformFeedbackMode bufferMode);
	public static void TransformFeedbackVaryings (uint program, int count, string varyings, TransformFeedbackMode bufferMode);
	public static void Uniform1 (int location, int count, int* v);
	public static void Uniform1 (int location, float x);
	public static void Uniform1 (int location, int count, float[] v);
	public static void Uniform1 (int location, int count, ref float v);
	public static void Uniform1 (int location, int count, float* v);
	public static void Uniform1 (int location, uint v0);
	public static void Uniform1 (int location, int count, ref int v);
	public static void Uniform1 (int location, int count, ref uint value);
	public static void Uniform1 (int location, int count, uint* value);
	public static void Uniform1 (int location, int count, uint[] value);
	public static void Uniform1 (int location, int count, int[] v);
	public static void Uniform1 (int location, int x);
	public static void Uniform2 (int location, ref OpenTK.Vector2 vector);
	public static void Uniform2 (int location, OpenTK.Vector2 vector);
	public static void Uniform2 (int location, float x, float y);
	public static void Uniform2 (int location, int count, float[] v);
	public static void Uniform2 (int location, int count, ref float v);
	public static void Uniform2 (int location, int count, float* v);
	public static void Uniform2 (int location, int x, int y);
	public static void Uniform2 (int location, int count, int[] v);
	public static void Uniform2 (int location, int count, uint* value);
	public static void Uniform2 (int location, int count, ref uint value);
	public static void Uniform2 (int location, int count, uint[] value);
	public static void Uniform2 (int location, uint v0, uint v1);
	public static void Uniform2 (int location, int count, int* v);
	public static void Uniform3 (int location, ref OpenTK.Vector3 vector);
	public static void Uniform3 (int location, OpenTK.Vector3 vector);
	public static void Uniform3 (int location, uint v0, uint v1, uint v2);
	public static void Uniform3 (int location, int count, int[] v);
	public static void Uniform3 (int location, int count, ref int v);
	public static void Uniform3 (int location, int count, int* v);
	public static void Uniform3 (int location, int count, uint[] value);
	public static void Uniform3 (int location, int count, ref uint value);
	public static void Uniform3 (int location, int count, uint* value);
	public static void Uniform3 (int location, int count, float* v);
	public static void Uniform3 (int location, int x, int y, int z);
	public static void Uniform3 (int location, float x, float y, float z);
	public static void Uniform3 (int location, int count, float[] v);
	public static void Uniform3 (int location, int count, ref float v);
	public static void Uniform4 (int location, int count, float[] v);
	public static void Uniform4 (int location, float x, float y, float z, float w);
	public static void Uniform4 (int location, OpenTK.Graphics.Color4 color);
	public static void Uniform4 (int location, ref OpenTK.Vector4 vector);
	public static void Uniform4 (int location, OpenTK.Quaternion quaternion);
	public static void Uniform4 (int location, OpenTK.Vector4 vector);
	public static void Uniform4 (int location, uint v0, uint v1, uint v2, uint v3);
	public static void Uniform4 (int location, int count, int* v);
	public static void Uniform4 (int location, int count, int[] v);
	public static void Uniform4 (int location, int count, uint[] value);
	public static void Uniform4 (int location, int count, ref uint value);
	public static void Uniform4 (int location, int count, uint* value);
	public static void Uniform4 (int location, int count, ref int v);
	public static void Uniform4 (int location, int x, int y, int z, int w);
	public static void Uniform4 (int location, int count, float* v);
	public static void Uniform4 (int location, int count, ref float v);
	public static void UniformBlockBinding (uint program, uint uniformBlockIndex, uint uniformBlockBinding);
	public static void UniformBlockBinding (int program, int uniformBlockIndex, int uniformBlockBinding);
	public static void UniformMatrix2 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix2 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix2 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix3 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix3 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix3 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix4 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix4 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix4 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix4 (int location, bool transpose, ref OpenTK.Matrix4 matrix);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, float[] value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static bool UnmapBuffer (All target);
	public static bool UnmapBuffer (BufferTarget target);
	public static void UseProgram (uint program);
	public static void UseProgram (int program);
	public static void ValidateProgram (int program);
	public static void ValidateProgram (uint program);
	public static void VertexAttrib1 (uint indx, float[] values);
	public static void VertexAttrib1 (int indx, float* values);
	public static void VertexAttrib1 (int indx, float[] values);
	public static void VertexAttrib1 (uint indx, float x);
	public static void VertexAttrib1 (int indx, float x);
	public static void VertexAttrib1 (uint indx, float* values);
	public static void VertexAttrib2 (int index, OpenTK.Vector2 v);
	public static void VertexAttrib2 (int index, ref OpenTK.Vector2 v);
	public static void VertexAttrib2 (uint indx, float* values);
	public static void VertexAttrib2 (uint indx, ref float values);
	public static void VertexAttrib2 (uint indx, float[] values);
	public static void VertexAttrib2 (int indx, float* values);
	public static void VertexAttrib2 (int indx, ref float values);
	public static void VertexAttrib2 (int indx, float[] values);
	public static void VertexAttrib2 (uint indx, float x, float y);
	public static void VertexAttrib2 (int indx, float x, float y);
	public static void VertexAttrib3 (int index, ref OpenTK.Vector3 v);
	public static void VertexAttrib3 (uint indx, float* values);
	public static void VertexAttrib3 (uint indx, ref float values);
	public static void VertexAttrib3 (uint indx, float[] values);
	public static void VertexAttrib3 (int indx, float* values);
	public static void VertexAttrib3 (int indx, ref float values);
	public static void VertexAttrib3 (int indx, float[] values);
	public static void VertexAttrib3 (uint indx, float x, float y, float z);
	public static void VertexAttrib3 (int index, OpenTK.Vector3 v);
	public static void VertexAttrib3 (int indx, float x, float y, float z);
	public static void VertexAttrib4 (int indx, float x, float y, float z, float w);
	public static void VertexAttrib4 (int index, ref OpenTK.Vector4 v);
	public static void VertexAttrib4 (int index, OpenTK.Vector4 v);
	public static void VertexAttrib4 (uint indx, float* values);
	public static void VertexAttrib4 (uint indx, ref float values);
	public static void VertexAttrib4 (uint indx, float[] values);
	public static void VertexAttrib4 (int indx, float* values);
	public static void VertexAttrib4 (int indx, ref float values);
	public static void VertexAttrib4 (int indx, float[] values);
	public static void VertexAttrib4 (uint indx, float x, float y, float z, float w);
	public static void VertexAttribDivisor (uint index, uint divisor);
	public static void VertexAttribDivisor (int index, int divisor);
	public static void VertexAttribI4 (uint index, int* v);
	public static void VertexAttribI4 (int index, int[] v);
	public static void VertexAttribI4 (int index, ref int v);
	public static void VertexAttribI4 (int index, int* v);
	public static void VertexAttribI4 (uint index, int[] v);
	public static void VertexAttribI4 (uint index, ref int v);
	public static void VertexAttribI4 (uint index, uint x, uint y, uint z, uint w);
	public static void VertexAttribI4 (uint index, uint[] v);
	public static void VertexAttribI4 (uint index, ref uint v);
	public static void VertexAttribI4 (uint index, int x, int y, int z, int w);
	public static void VertexAttribI4 (uint index, uint* v);
	public static void VertexAttribI4 (int index, int x, int y, int z, int w);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, out T4 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer (int index, int size, All type, int stride, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer (uint index, int size, All type, int stride, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, out T4 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, VertexAttribIntegerType type, int stride, out T4 pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, VertexAttribIntegerType type, int stride, T4[0...,0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, VertexAttribIntegerType type, int stride, T4[0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, VertexAttribIntegerType type, int stride, T4[] pointer);
	public static void VertexAttribIPointer (uint index, int size, VertexAttribIntegerType type, int stride, System.IntPtr pointer);
	public static void VertexAttribIPointer (int index, int size, VertexAttribIntegerType type, int stride, System.IntPtr pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, VertexAttribIntegerType type, int stride, T4[] pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, VertexAttribIntegerType type, int stride, T4[0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, VertexAttribIntegerType type, int stride, T4[0...,0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, VertexAttribIntegerType type, int stride, out T4 pointer);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, out T5 ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer (int index, int size, VertexAttribPointerType type, bool normalized, int stride, int offset);
	public static void VertexAttribPointer (uint index, int size, VertexAttribPointerType type, bool normalized, int stride, int offset);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, out T5 ptr);
	public static void Viewport (System.Drawing.Rectangle rectangle);
	public static void Viewport (System.Drawing.Point location, System.Drawing.Size size);
	public static void Viewport (System.Drawing.Size size);
	public static void Viewport (int x, int y, int width, int height);
	public static void WaitSync (System.IntPtr sync, uint flags, ulong timeout);
	public static void WaitSync (System.IntPtr sync, int flags, long timeout);

	// inner types
	public static class Apple {
		// methods
		public static void CopyTextureLevel (int destinationTexture, int sourceTexture, int sourceBaseLevel, int sourceLevelCount);
		public static void CopyTextureLevel (uint destinationTexture, uint sourceTexture, int sourceBaseLevel, int sourceLevelCount);
	}
	public static class Ext {
		// methods
		public static void ActiveShaderProgram (int pipeline, int program);
		public static void ActiveShaderProgram (uint pipeline, uint program);
		public static void BindProgramPipeline (uint pipeline);
		public static void BindProgramPipeline (int pipeline);
		public static int CreateShaderProgram (All type, int count, string strings);
		public static void DeleteProgramPipelines (int n, uint* pipelines);
		public static void DeleteProgramPipelines (int n, ref uint pipelines);
		public static void DeleteProgramPipelines (int n, uint[] pipelines);
		public static void DeleteProgramPipelines (int n, int* pipelines);
		public static void DeleteProgramPipelines (int n, ref int pipelines);
		public static void DeleteProgramPipelines (int n, int[] pipelines);
		public static void GenProgramPipelines (int n, uint* pipelines);
		public static void GenProgramPipelines (int n, out uint pipelines);
		public static void GenProgramPipelines (int n, uint[] pipelines);
		public static void GenProgramPipelines (int n, int* pipelines);
		public static void GenProgramPipelines (int n, out int pipelines);
		public static void GenProgramPipelines (int n, int[] pipelines);
		public static void GetObjectLabel (All type, uint object, int bufSize, int* length, System.Text.StringBuilder label);
		public static void GetObjectLabel (All type, uint object, int bufSize, out int length, System.Text.StringBuilder label);
		public static void GetObjectLabel (All type, uint object, int bufSize, int[] length, System.Text.StringBuilder label);
		public static void GetObjectLabel (All type, int object, int bufSize, int* length, System.Text.StringBuilder label);
		public static void GetObjectLabel (All type, int object, int bufSize, out int length, System.Text.StringBuilder label);
		public static void GetObjectLabel (All type, int object, int bufSize, int[] length, System.Text.StringBuilder label);
		public static void GetProgramPipeline (int pipeline, All pname, out int params);
		public static void GetProgramPipeline (int pipeline, All pname, int* params);
		public static void GetProgramPipeline (uint pipeline, All pname, int[] params);
		public static void GetProgramPipeline (uint pipeline, All pname, out int params);
		public static void GetProgramPipeline (uint pipeline, All pname, int* params);
		public static void GetProgramPipeline (int pipeline, All pname, int[] params);
		public static void GetProgramPipelineInfoLog (int pipeline, int bufSize, int[] length, System.Text.StringBuilder infoLog);
		public static void GetProgramPipelineInfoLog (int pipeline, int bufSize, out int length, System.Text.StringBuilder infoLog);
		public static void GetProgramPipelineInfoLog (int pipeline, int bufSize, int* length, System.Text.StringBuilder infoLog);
		public static void GetProgramPipelineInfoLog (uint pipeline, int bufSize, int[] length, System.Text.StringBuilder infoLog);
		public static void GetProgramPipelineInfoLog (uint pipeline, int bufSize, out int length, System.Text.StringBuilder infoLog);
		public static void GetProgramPipelineInfoLog (uint pipeline, int bufSize, int* length, System.Text.StringBuilder infoLog);
		public static void InsertEventMarker (int length, string marker);
		public static bool IsProgramPipeline (int pipeline);
		public static bool IsProgramPipeline (uint pipeline);
		public static void LabelObject (All type, int object, int length, string label);
		public static void LabelObject (All type, uint object, int length, string label);
		public static void PopGroupMarker ();
		public static void ProgramParameter (int program, All pname, int value);
		public static void ProgramParameter (uint program, All pname, int value);
		public static void ProgramUniform1 (uint program, int location, int count, ref int value);
		public static void ProgramUniform1 (uint program, int location, int count, int[] value);
		public static void ProgramUniform1 (int program, int location, int count, int* value);
		public static void ProgramUniform1 (int program, int location, int count, ref int value);
		public static void ProgramUniform1 (uint program, int location, int count, int* value);
		public static void ProgramUniform1 (uint program, int location, uint x);
		public static void ProgramUniform1 (uint program, int location, int count, uint[] value);
		public static void ProgramUniform1 (uint program, int location, int count, ref uint value);
		public static void ProgramUniform1 (uint program, int location, int count, uint* value);
		public static void ProgramUniform1 (int program, int location, int count, int[] value);
		public static void ProgramUniform1 (int program, int location, float x);
		public static void ProgramUniform1 (uint program, int location, float x);
		public static void ProgramUniform1 (int program, int location, int count, float[] value);
		public static void ProgramUniform1 (int program, int location, int count, ref float value);
		public static void ProgramUniform1 (int program, int location, int count, float* value);
		public static void ProgramUniform1 (uint program, int location, int x);
		public static void ProgramUniform1 (int program, int location, int x);
		public static void ProgramUniform1 (uint program, int location, int count, float* value);
		public static void ProgramUniform1 (uint program, int location, int count, ref float value);
		public static void ProgramUniform1 (uint program, int location, int count, float[] value);
		public static void ProgramUniform2 (int program, int location, int count, int[] value);
		public static void ProgramUniform2 (int program, int location, int count, int* value);
		public static void ProgramUniform2 (uint program, int location, int count, int[] value);
		public static void ProgramUniform2 (uint program, int location, int count, int* value);
		public static void ProgramUniform2 (uint program, int location, uint x, uint y);
		public static void ProgramUniform2 (uint program, int location, int count, uint[] value);
		public static void ProgramUniform2 (uint program, int location, int count, ref uint value);
		public static void ProgramUniform2 (uint program, int location, int count, uint* value);
		public static void ProgramUniform2 (uint program, int location, int x, int y);
		public static void ProgramUniform2 (int program, int location, float x, float y);
		public static void ProgramUniform2 (uint program, int location, float x, float y);
		public static void ProgramUniform2 (int program, int location, int count, float[] value);
		public static void ProgramUniform2 (int program, int location, int count, ref float value);
		public static void ProgramUniform2 (int program, int location, int count, float* value);
		public static void ProgramUniform2 (int program, int location, int x, int y);
		public static void ProgramUniform2 (uint program, int location, int count, float* value);
		public static void ProgramUniform2 (uint program, int location, int count, ref float value);
		public static void ProgramUniform2 (uint program, int location, int count, float[] value);
		public static void ProgramUniform3 (uint program, int location, int count, ref int value);
		public static void ProgramUniform3 (uint program, int location, int count, int[] value);
		public static void ProgramUniform3 (int program, int location, int count, int* value);
		public static void ProgramUniform3 (int program, int location, int count, ref int value);
		public static void ProgramUniform3 (uint program, int location, int count, int* value);
		public static void ProgramUniform3 (uint program, int location, uint x, uint y, uint z);
		public static void ProgramUniform3 (uint program, int location, int count, uint[] value);
		public static void ProgramUniform3 (uint program, int location, int count, ref uint value);
		public static void ProgramUniform3 (uint program, int location, int count, uint* value);
		public static void ProgramUniform3 (int program, int location, int count, int[] value);
		public static void ProgramUniform3 (int program, int location, float x, float y, float z);
		public static void ProgramUniform3 (uint program, int location, float x, float y, float z);
		public static void ProgramUniform3 (int program, int location, int count, float[] value);
		public static void ProgramUniform3 (int program, int location, int count, ref float value);
		public static void ProgramUniform3 (int program, int location, int count, float* value);
		public static void ProgramUniform3 (uint program, int location, int x, int y, int z);
		public static void ProgramUniform3 (int program, int location, int x, int y, int z);
		public static void ProgramUniform3 (uint program, int location, int count, float* value);
		public static void ProgramUniform3 (uint program, int location, int count, ref float value);
		public static void ProgramUniform3 (uint program, int location, int count, float[] value);
		public static void ProgramUniform4 (uint program, int location, int count, ref int value);
		public static void ProgramUniform4 (uint program, int location, int count, int[] value);
		public static void ProgramUniform4 (int program, int location, int count, int* value);
		public static void ProgramUniform4 (int program, int location, int count, ref int value);
		public static void ProgramUniform4 (uint program, int location, int count, int* value);
		public static void ProgramUniform4 (uint program, int location, uint x, uint y, uint z, uint w);
		public static void ProgramUniform4 (uint program, int location, int count, uint[] value);
		public static void ProgramUniform4 (uint program, int location, int count, ref uint value);
		public static void ProgramUniform4 (uint program, int location, int count, uint* value);
		public static void ProgramUniform4 (int program, int location, int count, int[] value);
		public static void ProgramUniform4 (int program, int location, float x, float y, float z, float w);
		public static void ProgramUniform4 (uint program, int location, float x, float y, float z, float w);
		public static void ProgramUniform4 (int program, int location, int count, float[] value);
		public static void ProgramUniform4 (int program, int location, int count, ref float value);
		public static void ProgramUniform4 (int program, int location, int count, float* value);
		public static void ProgramUniform4 (uint program, int location, int x, int y, int z, int w);
		public static void ProgramUniform4 (int program, int location, int x, int y, int z, int w);
		public static void ProgramUniform4 (uint program, int location, int count, float* value);
		public static void ProgramUniform4 (uint program, int location, int count, ref float value);
		public static void ProgramUniform4 (uint program, int location, int count, float[] value);
		public static void ProgramUniformMatrix2 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix2 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix2 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix2 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix2 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix2 (int program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix2x3 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix2x3 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix2x3 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix2x3 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix2x3 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix2x3 (int program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix2x4 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix2x4 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix2x4 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix2x4 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix2x4 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix2x4 (int program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix3 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix3 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix3 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix3 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix3 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix3 (int program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix3x2 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix3x2 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix3x2 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix3x2 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix3x2 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix3x2 (int program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix3x4 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix3x4 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix3x4 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix3x4 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix3x4 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix3x4 (int program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix4 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix4 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix4 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix4 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix4 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix4 (int program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix4x2 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix4x2 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix4x2 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix4x2 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix4x2 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix4x2 (int program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix4x3 (uint program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix4x3 (uint program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix4x3 (uint program, int location, int count, bool transpose, float[] value);
		public static void ProgramUniformMatrix4x3 (int program, int location, int count, bool transpose, float* value);
		public static void ProgramUniformMatrix4x3 (int program, int location, int count, bool transpose, ref float value);
		public static void ProgramUniformMatrix4x3 (int program, int location, int count, bool transpose, float[] value);
		public static void PushGroupMarker (int length, string marker);
		public static void UseProgramStages (int pipeline, int stages, int program);
		public static void UseProgramStages (uint pipeline, uint stages, uint program);
		public static void ValidateProgramPipeline (int pipeline);
		public static void ValidateProgramPipeline (uint pipeline);
	}
}
```

### New Type OpenTK.Graphics.ES30.HintMode

```
[Serializable]
public enum HintMode {
	DontCare = 4352,
	Fastest = 4353,
	Nicest = 4354,
}
```

### New Type OpenTK.Graphics.ES30.HintTarget

```
[Serializable]
public enum HintTarget {
	FragmentShaderDerivativeHint = 35723,
	GenerateMipmapHint = 33170,
}
```

### New Type OpenTK.Graphics.ES30.ImageTarget

```
[Serializable]
public enum ImageTarget {
	Renderbuffer = 36161,
}
```

### New Type OpenTK.Graphics.ES30.InternalFormatParameter

```
[Serializable]
public enum InternalFormatParameter {
	NumSampleCounts = 37760,
	Samples = 32937,
}
```

### New Type OpenTK.Graphics.ES30.OpenGlEsCoreVersions

```
[Serializable]
public enum OpenGlEsCoreVersions {
	EsVersion20 = 1,
	EsVersion30 = 1,
}
```

### New Type OpenTK.Graphics.ES30.PixelFormat

```
[Serializable]
public enum PixelFormat {
	Alpha = 6406,
	DepthComponent = 6402,
	DepthStencil = 34041,
	Luminance = 6409,
	LuminanceAlpha = 6410,
	Red = 6403,
	RedInteger = 36244,
	Rg = 33319,
	Rgb = 6407,
	Rgba = 6408,
	RgbaInteger = 36249,
	RgbInteger = 36248,
	RgInteger = 33320,
}
```

### New Type OpenTK.Graphics.ES30.PixelInternalFormat

```
[Serializable]
public enum PixelInternalFormat {
	Alpha = 6406,
	Luminance = 6409,
	LuminanceAlpha = 6410,
	Rgb = 6407,
	Rgba = 6408,
}
```

### New Type OpenTK.Graphics.ES30.PixelStoreParameter

```
[Serializable]
public enum PixelStoreParameter {
	PackAlignment = 3333,
	PackRowLength = 3330,
	PackSkipPixels = 3332,
	PackSkipRows = 3331,
	UnpackAlignment = 3317,
	UnpackImageHeight = 32878,
	UnpackRowLength = 3314,
	UnpackSkipImages = 32877,
	UnpackSkipPixels = 3316,
	UnpackSkipRows = 3315,
}
```

### New Type OpenTK.Graphics.ES30.PixelType

```
[Serializable]
public enum PixelType {
	Byte = 5120,
	Float = 5126,
	Float32UnsignedInt248Rev = 36269,
	HalfFloat = 5131,
	Int = 5124,
	Short = 5122,
	UnsignedByte = 5121,
	UnsignedInt = 5125,
	UnsignedInt10F11F11FRev = 35899,
	UnsignedInt2101010Rev = 33640,
	UnsignedInt248 = 34042,
	UnsignedInt5999Rev = 35902,
	UnsignedShort = 5123,
	UnsignedShort4444 = 32819,
	UnsignedShort5551 = 32820,
	UnsignedShort565 = 33635,
}
```

### New Type OpenTK.Graphics.ES30.PrimitiveType

```
[Serializable]
public enum PrimitiveType {
	LineLoop = 2,
	Lines = 1,
	LineStrip = 3,
	Points = 0,
	TriangleFan = 6,
	Triangles = 4,
	TriangleStrip = 5,
}
```

### New Type OpenTK.Graphics.ES30.ProgramParameter

```
[Serializable]
public enum ProgramParameter {
	ActiveAttributeMaxLength = 35722,
	ActiveAttributes = 35721,
	ActiveUniformMaxLength = 35719,
	ActiveUniforms = 35718,
	AttachedShaders = 35717,
	DeleteStatus = 35712,
	InfoLogLength = 35716,
	LinkStatus = 35714,
	ProgramBinaryRetrievableHint = 33367,
	ValidateStatus = 35715,
}
```

### New Type OpenTK.Graphics.ES30.ProgramParameterName

```
[Serializable]
public enum ProgramParameterName {
	ProgramBinaryRetrievableHint = 33367,
}
```

### New Type OpenTK.Graphics.ES30.QueryTarget

```
[Serializable]
public enum QueryTarget {
	AnySamplesPassed = 35887,
	AnySamplesPassedConservative = 36202,
	TransformFeedbackPrimitivesWritten = 35976,
}
```

### New Type OpenTK.Graphics.ES30.ReadBufferMode

```
[Serializable]
public enum ReadBufferMode {
	Back = 1029,
	ColorAttachment0 = 36064,
	ColorAttachment1 = 36065,
	ColorAttachment10 = 36074,
	ColorAttachment11 = 36075,
	ColorAttachment12 = 36076,
	ColorAttachment13 = 36077,
	ColorAttachment14 = 36078,
	ColorAttachment15 = 36079,
	ColorAttachment2 = 36066,
	ColorAttachment3 = 36067,
	ColorAttachment4 = 36068,
	ColorAttachment5 = 36069,
	ColorAttachment6 = 36070,
	ColorAttachment7 = 36071,
	ColorAttachment8 = 36072,
	ColorAttachment9 = 36073,
	None = 0,
}
```

### New Type OpenTK.Graphics.ES30.ReadFormat

```
[Serializable]
public enum ReadFormat {
	ImplementationColorReadFormat = 35739,
	ImplementationColorReadType = 35738,
}
```

### New Type OpenTK.Graphics.ES30.RenderbufferInternalFormat

```
[Serializable]
public enum RenderbufferInternalFormat {
	Depth24Stencil8 = 35056,
	Depth32FStencil8 = 36013,
	DepthComponent16 = 33189,
	DepthComponent24 = 33190,
	DepthComponent32F = 36012,
	R16i = 33331,
	R16ui = 33332,
	R32i = 33333,
	R32ui = 33334,
	R8 = 33321,
	R8i = 33329,
	R8ui = 33330,
	Rg16i = 33337,
	Rg16ui = 33338,
	Rg32i = 33339,
	Rg32ui = 33340,
	Rg8 = 33323,
	Rg8i = 33335,
	Rg8ui = 33336,
	Rgb10A2 = 32857,
	Rgb10A2ui = 36975,
	Rgb565 = 36194,
	Rgb5A1 = 32855,
	Rgb8 = 32849,
	Rgba16i = 36232,
	Rgba16ui = 36214,
	Rgba32i = 36226,
	Rgba32ui = 36208,
	Rgba4 = 32854,
	Rgba8 = 32856,
	Rgba8i = 36238,
	Rgba8ui = 36220,
	Srgb8Alpha8 = 35907,
	StencilIndex8 = 36168,
}
```

### New Type OpenTK.Graphics.ES30.RenderbufferParameterName

```
[Serializable]
public enum RenderbufferParameterName {
	RenderbufferAlphaSize = 36179,
	RenderbufferBlueSize = 36178,
	RenderbufferDepthSize = 36180,
	RenderbufferGreenSize = 36177,
	RenderbufferHeight = 36163,
	RenderbufferInternalFormat = 36164,
	RenderbufferRedSize = 36176,
	RenderbufferSamples = 36011,
	RenderbufferStencilSize = 36181,
	RenderbufferWidth = 36162,
}
```

### New Type OpenTK.Graphics.ES30.RenderbufferTarget

```
[Serializable]
public enum RenderbufferTarget {
	Renderbuffer = 36161,
}
```

### New Type OpenTK.Graphics.ES30.SamplerParameterName

```
[Serializable]
public enum SamplerParameterName {
	TextureCompareFunc = 34893,
	TextureCompareMode = 34892,
	TextureMagFilter = 10240,
	TextureMaxLod = 33083,
	TextureMinFilter = 10241,
	TextureMinLod = 33082,
	TextureWrapR = 32882,
	TextureWrapS = 10242,
	TextureWrapT = 10243,
}
```

### New Type OpenTK.Graphics.ES30.SeparateBlendFunctions

```
[Serializable]
public enum SeparateBlendFunctions {
	BlendColor = 32773,
	BlendDstAlpha = 32970,
	BlendDstRgb = 32968,
	BlendSrcAlpha = 32971,
	BlendSrcRgb = 32969,
	ConstantAlpha = 32771,
	ConstantColor = 32769,
	OneMinusConstantAlpha = 32772,
	OneMinusConstantColor = 32770,
}
```

### New Type OpenTK.Graphics.ES30.ShaderBinary

```
[Serializable]
public enum ShaderBinary {
	NumShaderBinaryFormats = 36345,
	ShaderBinaryFormats = 36344,
}
```

### New Type OpenTK.Graphics.ES30.ShaderBinaryFormat

```
[Serializable]
public enum ShaderBinaryFormat {
}
```

### New Type OpenTK.Graphics.ES30.ShaderParameter

```
[Serializable]
public enum ShaderParameter {
	CompileStatus = 35713,
	DeleteStatus = 35712,
	InfoLogLength = 35716,
	ShaderSourceLength = 35720,
	ShaderType = 35663,
}
```

### New Type OpenTK.Graphics.ES30.ShaderPrecision

```
[Serializable]
public enum ShaderPrecision {
	HighFloat = 36338,
	HighInt = 36341,
	LowFloat = 36336,
	LowInt = 36339,
	MediumFloat = 36337,
	MediumInt = 36340,
}
```

### New Type OpenTK.Graphics.ES30.ShaderPrecisionSpecifiedTypes

```
[Serializable]
public enum ShaderPrecisionSpecifiedTypes {
	HighFloat = 36338,
	HighInt = 36341,
	LowFloat = 36336,
	LowInt = 36339,
	MediumFloat = 36337,
	MediumInt = 36340,
}
```

### New Type OpenTK.Graphics.ES30.Shaders

```
[Serializable]
public enum Shaders {
	ActiveAttributeMaxLength = 35722,
	ActiveAttributes = 35721,
	ActiveUniformMaxLength = 35719,
	ActiveUniforms = 35718,
	AttachedShaders = 35717,
	CurrentProgram = 35725,
	DeleteStatus = 35712,
	FragmentShader = 35632,
	LinkStatus = 35714,
	MaxCombinedTextureImageUnits = 35661,
	MaxFragmentUniformVectors = 36349,
	MaxTextureImageUnits = 34930,
	MaxVaryingVectors = 36348,
	MaxVertexAttribs = 34921,
	MaxVertexTextureImageUnits = 35660,
	MaxVertexUniformVectors = 36347,
	ShaderType = 35663,
	ShadingLanguageVersion = 35724,
	ValidateStatus = 35715,
	VertexShader = 35633,
}
```

### New Type OpenTK.Graphics.ES30.ShaderSource

```
[Serializable]
public enum ShaderSource {
	CompileStatus = 35713,
	InfoLogLength = 35716,
	ShaderCompiler = 36346,
	ShaderSourceLength = 35720,
}
```

### New Type OpenTK.Graphics.ES30.ShaderType

```
[Serializable]
public enum ShaderType {
	FragmentShader = 35632,
	VertexShader = 35633,
}
```

### New Type OpenTK.Graphics.ES30.SizedInternalFormat

```
[Serializable]
public enum SizedInternalFormat {
	Depth24Stencil8 = 35056,
	Depth32fStencil8 = 36013,
	DepthComponent16 = 33189,
	DepthComponent24 = 33190,
	DepthComponent32f = 36012,
	R11fG11fB10f = 35898,
	R16f = 33325,
	R16i = 33331,
	R16ui = 33332,
	R32f = 33326,
	R32i = 33333,
	R32ui = 33334,
	R8 = 33321,
	R8i = 33329,
	R8Snorm = 36756,
	R8ui = 33330,
	Rg16f = 33327,
	Rg16i = 33337,
	Rg16ui = 33338,
	Rg32f = 33328,
	Rg32i = 33339,
	Rg32ui = 33340,
	Rg8 = 33323,
	Rg8i = 33335,
	Rg8Snorm = 36757,
	Rg8ui = 33336,
	Rgb10A2 = 32857,
	Rgb10A2ui = 36975,
	Rgb16f = 34843,
	Rgb16i = 36233,
	Rgb16ui = 36215,
	Rgb32f = 34837,
	Rgb32i = 36227,
	Rgb32ui = 36209,
	Rgb565 = 36194,
	Rgb5A1 = 32855,
	Rgb8 = 32849,
	Rgb8i = 36239,
	Rgb8Snorm = 36758,
	Rgb8ui = 36221,
	Rgb9E5 = 35901,
	Rgba16f = 34842,
	Rgba16i = 36232,
	Rgba16ui = 36214,
	Rgba32f = 34836,
	Rgba32i = 36226,
	Rgba32ui = 36208,
	Rgba4 = 32854,
	Rgba8 = 32856,
	Rgba8i = 36238,
	Rgba8Snorm = 36759,
	Rgba8ui = 36220,
	Srgb8 = 35905,
	Srgb8Alpha8 = 35907,
}
```

### New Type OpenTK.Graphics.ES30.StencilFunction

```
[Serializable]
public enum StencilFunction {
	Always = 519,
	Equal = 514,
	Gequal = 518,
	Greater = 516,
	Lequal = 515,
	Less = 513,
	Never = 512,
	Notequal = 517,
}
```

### New Type OpenTK.Graphics.ES30.StencilOp

```
[Serializable]
public enum StencilOp {
	Decr = 7683,
	DecrWrap = 34056,
	Incr = 7682,
	IncrWrap = 34055,
	Invert = 5386,
	Keep = 7680,
	Replace = 7681,
	Zero = 0,
}
```

### New Type OpenTK.Graphics.ES30.StringName

```
[Serializable]
public enum StringName {
	Extensions = 7939,
	Renderer = 7937,
	ShadingLanguageVersion = 35724,
	Vendor = 7936,
	Version = 7938,
}
```

### New Type OpenTK.Graphics.ES30.StringNameIndexed

```
[Serializable]
public enum StringNameIndexed {
	Extensions = 7939,
}
```

### New Type OpenTK.Graphics.ES30.SyncCondition

```
[Serializable]
public enum SyncCondition {
	SyncGpuCommandsComplete = 37143,
}
```

### New Type OpenTK.Graphics.ES30.SyncParameterName

```
[Serializable]
public enum SyncParameterName {
	ObjectType = 37138,
	SyncCondition = 37139,
	SyncFlags = 37141,
	SyncStatus = 37140,
}
```

### New Type OpenTK.Graphics.ES30.TextureComponentCount

```
[Serializable]
public enum TextureComponentCount {
	Alpha = 6406,
	Depth24Stencil8 = 35056,
	Depth32fStencil8 = 36013,
	DepthComponent16 = 33189,
	DepthComponent24 = 33190,
	DepthComponent32f = 36012,
	Luminance = 6409,
	LuminanceAlpha = 6410,
	R11fG11fB10f = 35898,
	R16f = 33325,
	R16i = 33331,
	R16ui = 33332,
	R32f = 33326,
	R32i = 33333,
	R32ui = 33334,
	R8 = 33321,
	R8i = 33329,
	R8Snorm = 36756,
	R8ui = 33330,
	Rg16f = 33327,
	Rg16i = 33337,
	Rg16ui = 33338,
	Rg32f = 33328,
	Rg32i = 33339,
	Rg32ui = 33340,
	Rg8 = 33323,
	Rg8i = 33335,
	Rg8Snorm = 36757,
	Rg8ui = 33336,
	Rgb = 6407,
	Rgb10A2 = 32857,
	Rgb10A2ui = 36975,
	Rgb16f = 34843,
	Rgb16i = 36233,
	Rgb16ui = 36215,
	Rgb32f = 34837,
	Rgb32i = 36227,
	Rgb32ui = 36209,
	Rgb565 = 36194,
	Rgb5A1 = 32855,
	Rgb8 = 32849,
	Rgb8i = 36239,
	Rgb8Snorm = 36758,
	Rgb8ui = 36221,
	Rgb9E5 = 35901,
	Rgba = 6408,
	Rgba16f = 34842,
	Rgba16i = 36232,
	Rgba16ui = 36214,
	Rgba32f = 34836,
	Rgba32i = 36226,
	Rgba32ui = 36208,
	Rgba4 = 32854,
	Rgba8 = 32856,
	Rgba8i = 36238,
	Rgba8Snorm = 36759,
	Rgba8ui = 36220,
	Srgb8 = 35905,
	Srgb8Alpha8 = 35907,
}
```

### New Type OpenTK.Graphics.ES30.TextureMagFilter

```
[Serializable]
public enum TextureMagFilter {
	Linear = 9729,
	Nearest = 9728,
}
```

### New Type OpenTK.Graphics.ES30.TextureMinFilter

```
[Serializable]
public enum TextureMinFilter {
	Linear = 9729,
	LinearMipmapLinear = 9987,
	LinearMipmapNearest = 9985,
	Nearest = 9728,
	NearestMipmapLinear = 9986,
	NearestMipmapNearest = 9984,
}
```

### New Type OpenTK.Graphics.ES30.TextureParameterName

```
[Serializable]
public enum TextureParameterName {
	TextureBaseLevel = 33084,
	TextureCompareFunc = 34893,
	TextureCompareMode = 34892,
	TextureMagFilter = 10240,
	TextureMaxLevel = 33085,
	TextureMaxLod = 33083,
	TextureMinFilter = 10241,
	TextureMinLod = 33082,
	TextureSwizzleA = 36421,
	TextureSwizzleB = 36420,
	TextureSwizzleG = 36419,
	TextureSwizzleR = 36418,
	TextureWrapR = 32882,
	TextureWrapS = 10242,
	TextureWrapT = 10243,
}
```

### New Type OpenTK.Graphics.ES30.TextureTarget

```
[Serializable]
public enum TextureTarget {
	MaxCubeMapTextureSize = 34076,
	Texture = 5890,
	Texture2D = 3553,
	Texture2DArray = 35866,
	Texture3D = 32879,
	TextureBindingCubeMap = 34068,
	TextureCubeMap = 34067,
	TextureCubeMapNegativeX = 34070,
	TextureCubeMapNegativeY = 34072,
	TextureCubeMapNegativeZ = 34074,
	TextureCubeMapPositiveX = 34069,
	TextureCubeMapPositiveY = 34071,
	TextureCubeMapPositiveZ = 34073,
}
```

### New Type OpenTK.Graphics.ES30.TextureTarget2D

```
[Serializable]
public enum TextureTarget2D {
	Texture2D = 3553,
	TextureCubeMap = 34067,
}
```

### New Type OpenTK.Graphics.ES30.TextureTarget3D

```
[Serializable]
public enum TextureTarget3D {
	Texture2DArray = 35866,
	Texture3D = 32879,
}
```

### New Type OpenTK.Graphics.ES30.TextureUnit

```
[Serializable]
public enum TextureUnit {
	ActiveTexture = 34016,
	Texture0 = 33984,
	Texture1 = 33985,
	Texture10 = 33994,
	Texture11 = 33995,
	Texture12 = 33996,
	Texture13 = 33997,
	Texture14 = 33998,
	Texture15 = 33999,
	Texture16 = 34000,
	Texture17 = 34001,
	Texture18 = 34002,
	Texture19 = 34003,
	Texture2 = 33986,
	Texture20 = 34004,
	Texture21 = 34005,
	Texture22 = 34006,
	Texture23 = 34007,
	Texture24 = 34008,
	Texture25 = 34009,
	Texture26 = 34010,
	Texture27 = 34011,
	Texture28 = 34012,
	Texture29 = 34013,
	Texture3 = 33987,
	Texture30 = 34014,
	Texture31 = 34015,
	Texture4 = 33988,
	Texture5 = 33989,
	Texture6 = 33990,
	Texture7 = 33991,
	Texture8 = 33992,
	Texture9 = 33993,
}
```

### New Type OpenTK.Graphics.ES30.TextureWrapMode

```
[Serializable]
public enum TextureWrapMode {
	ClampToEdge = 33071,
	MirroredRepeat = 33648,
	Repeat = 10497,
}
```

### New Type OpenTK.Graphics.ES30.Token

```
[Serializable]
public enum Token {
	ActiveUniformBlockMaxNameLength = 35381,
	ActiveUniformBlocks = 35382,
	AlreadySignaled = 37146,
	AnySamplesPassed = 35887,
	AnySamplesPassedConservative = 36202,
	Blue = 6405,
	BufferAccessFlags = 37151,
	BufferMapLength = 37152,
	BufferMapOffset = 37153,
	BufferMapped = 35004,
	BufferMapPointer = 35005,
	Color = 6144,
	ColorAttachment1 = 36065,
	ColorAttachment10 = 36074,
	ColorAttachment11 = 36075,
	ColorAttachment12 = 36076,
	ColorAttachment13 = 36077,
	ColorAttachment14 = 36078,
	ColorAttachment15 = 36079,
	ColorAttachment2 = 36066,
	ColorAttachment3 = 36067,
	ColorAttachment4 = 36068,
	ColorAttachment5 = 36069,
	ColorAttachment6 = 36070,
	ColorAttachment7 = 36071,
	ColorAttachment8 = 36072,
	ColorAttachment9 = 36073,
	CompareRefToTexture = 34894,
	CompressedR11Eac = 37488,
	CompressedRg11Eac = 37490,
	CompressedRgb8Etc2 = 37492,
	CompressedRgb8PunchthroughAlpha1Etc2 = 37494,
	CompressedRgba8Etc2Eac = 37496,
	CompressedSignedR11Eac = 37489,
	CompressedSignedRg11Eac = 37491,
	CompressedSrgb8Alpha8Etc2Eac = 37497,
	CompressedSrgb8Etc2 = 37493,
	CompressedSrgb8PunchthroughAlpha1Etc2 = 37495,
	ConditionSatisfied = 37148,
	CopyReadBuffer = 36662,
	CopyReadBufferBinding = 36662,
	CopyWriteBuffer = 36663,
	CopyWriteBufferBinding = 36663,
	CurrentQuery = 34917,
	Depth = 6145,
	Depth24Stencil8 = 35056,
	Depth32fStencil8 = 36013,
	DepthComponent24 = 33190,
	DepthComponent32f = 36012,
	DepthStencil = 34041,
	DepthStencilAttachment = 33306,
	DrawBuffer0 = 34853,
	DrawBuffer1 = 34854,
	DrawBuffer10 = 34863,
	DrawBuffer11 = 34864,
	DrawBuffer12 = 34865,
	DrawBuffer13 = 34866,
	DrawBuffer14 = 34867,
	DrawBuffer15 = 34868,
	DrawBuffer2 = 34855,
	DrawBuffer3 = 34856,
	DrawBuffer4 = 34857,
	DrawBuffer5 = 34858,
	DrawBuffer6 = 34859,
	DrawBuffer7 = 34860,
	DrawBuffer8 = 34861,
	DrawBuffer9 = 34862,
	DrawFramebuffer = 36009,
	DrawFramebufferBinding = 36006,
	DynamicCopy = 35050,
	DynamicRead = 35049,
	Float32UnsignedInt248Rev = 36269,
	FloatMat2x3 = 35685,
	FloatMat2x4 = 35686,
	FloatMat3x2 = 35687,
	FloatMat3x4 = 35688,
	FloatMat4x2 = 35689,
	FloatMat4x3 = 35690,
	FragmentShaderDerivativeHint = 35723,
	FramebufferAttachmentAlphaSize = 33301,
	FramebufferAttachmentBlueSize = 33300,
	FramebufferAttachmentColorEncoding = 33296,
	FramebufferAttachmentComponentType = 33297,
	FramebufferAttachmentDepthSize = 33302,
	FramebufferAttachmentGreenSize = 33299,
	FramebufferAttachmentRedSize = 33298,
	FramebufferAttachmentStencilSize = 33303,
	FramebufferAttachmentTextureLayer = 36052,
	FramebufferBinding = 36006,
	FramebufferDefault = 33304,
	FramebufferIncompleteMultisample = 36182,
	FramebufferUndefined = 33305,
	Green = 6404,
	HalfFloat = 5131,
	Int2101010Rev = 36255,
	InterleavedAttribs = 35980,
	IntSampler2D = 36298,
	IntSampler2DArray = 36303,
	IntSampler3D = 36299,
	IntSamplerCube = 36300,
	InvalidIndex = -1,
	MajorVersion = 33307,
	MapFlushExplicitBit = 16,
	MapInvalidateBufferBit = 8,
	MapInvalidateRangeBit = 4,
	MapReadBit = 1,
	MapUnsynchronizedBit = 32,
	MapWriteBit = 2,
	Max = 32776,
	Max3DTextureSize = 32883,
	MaxArrayTextureLayers = 35071,
	MaxColorAttachments = 36063,
	MaxCombinedFragmentUniformComponents = 35379,
	MaxCombinedUniformBlocks = 35374,
	MaxCombinedVertexUniformComponents = 35377,
	MaxDrawBuffers = 34852,
	MaxElementIndex = 36203,
	MaxElementsIndices = 33001,
	MaxElementsVertices = 33000,
	MaxFragmentInputComponents = 37157,
	MaxFragmentUniformBlocks = 35373,
	MaxFragmentUniformComponents = 35657,
	MaxProgramTexelOffset = 35077,
	MaxSamples = 36183,
	MaxServerWaitTimeout = 37137,
	MaxTextureLodBias = 34045,
	MaxTransformFeedbackInterleavedComponents = 35978,
	MaxTransformFeedbackSeparateAttribs = 35979,
	MaxTransformFeedbackSeparateComponents = 35968,
	MaxUniformBlockSize = 35376,
	MaxUniformBufferBindings = 35375,
	MaxVaryingComponents = 35659,
	MaxVertexOutputComponents = 37154,
	MaxVertexUniformBlocks = 35371,
	MaxVertexUniformComponents = 35658,
	Min = 32775,
	MinorVersion = 33308,
	MinProgramTexelOffset = 35076,
	NumExtensions = 33309,
	NumProgramBinaryFormats = 34814,
	NumSampleCounts = 37760,
	ObjectType = 37138,
	PackRowLength = 3330,
	PackSkipPixels = 3332,
	PackSkipRows = 3331,
	PixelPackBuffer = 35051,
	PixelPackBufferBinding = 35053,
	PixelUnpackBuffer = 35052,
	PixelUnpackBufferBinding = 35055,
	PrimitiveRestartFixedIndex = 36201,
	ProgramBinaryFormats = 34815,
	ProgramBinaryLength = 34625,
	ProgramBinaryRetrievableHint = 33367,
	QueryResult = 34918,
	QueryResultAvailable = 34919,
	R11fG11fB10f = 35898,
	R16f = 33325,
	R16i = 33331,
	R16ui = 33332,
	R32f = 33326,
	R32i = 33333,
	R32ui = 33334,
	R8 = 33321,
	R8i = 33329,
	R8Snorm = 36756,
	R8ui = 33330,
	RasterizerDiscard = 35977,
	ReadBuffer = 3074,
	ReadFramebuffer = 36008,
	ReadFramebufferBinding = 36010,
	Red = 6403,
	RedInteger = 36244,
	RenderbufferSamples = 36011,
	Rg = 33319,
	Rg16f = 33327,
	Rg16i = 33337,
	Rg16ui = 33338,
	Rg32f = 33328,
	Rg32i = 33339,
	Rg32ui = 33340,
	Rg8 = 33323,
	Rg8i = 33335,
	Rg8Snorm = 36757,
	Rg8ui = 33336,
	Rgb10A2 = 32857,
	Rgb10A2ui = 36975,
	Rgb16f = 34843,
	Rgb16i = 36233,
	Rgb16ui = 36215,
	Rgb32f = 34837,
	Rgb32i = 36227,
	Rgb32ui = 36209,
	Rgb8 = 32849,
	Rgb8i = 36239,
	Rgb8Snorm = 36758,
	Rgb8ui = 36221,
	Rgb9E5 = 35901,
	Rgba16f = 34842,
	Rgba16i = 36232,
	Rgba16ui = 36214,
	Rgba32f = 34836,
	Rgba32i = 36226,
	Rgba32ui = 36208,
	Rgba8 = 32856,
	Rgba8i = 36238,
	Rgba8Snorm = 36759,
	Rgba8ui = 36220,
	RgbaInteger = 36249,
	RgbInteger = 36248,
	RgInteger = 33320,
	Sampler2DArray = 36289,
	Sampler2DArrayShadow = 36292,
	Sampler2DShadow = 35682,
	Sampler3D = 35679,
	SamplerBinding = 35097,
	SamplerCubeShadow = 36293,
	SeparateAttribs = 35981,
	Signaled = 37145,
	SignedNormalized = 36764,
	Srgb = 35904,
	Srgb8 = 35905,
	Srgb8Alpha8 = 35907,
	StaticCopy = 35046,
	StaticRead = 35045,
	Stencil = 6146,
	StreamCopy = 35042,
	StreamRead = 35041,
	SyncCondition = 37139,
	SyncFence = 37142,
	SyncFlags = 37141,
	SyncFlushCommandsBit = 1,
	SyncGpuCommandsComplete = 37143,
	SyncStatus = 37140,
	Texture2DArray = 35866,
	Texture3D = 32879,
	TextureBaseLevel = 33084,
	TextureBinding2DArray = 35869,
	TextureBinding3D = 32874,
	TextureCompareFunc = 34893,
	TextureCompareMode = 34892,
	TextureImmutableFormat = 37167,
	TextureImmutableLevels = 33503,
	TextureMaxLevel = 33085,
	TextureMaxLod = 33083,
	TextureMinLod = 33082,
	TextureSwizzleA = 36421,
	TextureSwizzleB = 36420,
	TextureSwizzleG = 36419,
	TextureSwizzleR = 36418,
	TextureWrapR = 32882,
	TimeoutExpired = 37147,
	TimeoutIgnored = -1,
	TransformFeedback = 36386,
	TransformFeedbackActive = 36388,
	TransformFeedbackBinding = 36389,
	TransformFeedbackBuffer = 35982,
	TransformFeedbackBufferBinding = 35983,
	TransformFeedbackBufferMode = 35967,
	TransformFeedbackBufferSize = 35973,
	TransformFeedbackBufferStart = 35972,
	TransformFeedbackPaused = 36387,
	TransformFeedbackPrimitivesWritten = 35976,
	TransformFeedbackVaryingMaxLength = 35958,
	TransformFeedbackVaryings = 35971,
	UniformArrayStride = 35388,
	UniformBlockActiveUniformIndices = 35395,
	UniformBlockActiveUniforms = 35394,
	UniformBlockBinding = 35391,
	UniformBlockDataSize = 35392,
	UniformBlockIndex = 35386,
	UniformBlockNameLength = 35393,
	UniformBlockReferencedByFragmentShader = 35398,
	UniformBlockReferencedByVertexShader = 35396,
	UniformBuffer = 35345,
	UniformBufferBinding = 35368,
	UniformBufferOffsetAlignment = 35380,
	UniformBufferSize = 35370,
	UniformBufferStart = 35369,
	UniformIsRowMajor = 35390,
	UniformMatrixStride = 35389,
	UniformNameLength = 35385,
	UniformOffset = 35387,
	UniformSize = 35384,
	UniformType = 35383,
	UnpackImageHeight = 32878,
	UnpackRowLength = 3314,
	UnpackSkipImages = 32877,
	UnpackSkipPixels = 3316,
	UnpackSkipRows = 3315,
	Unsignaled = 37144,
	UnsignedInt10F11F11FRev = 35899,
	UnsignedInt2101010Rev = 33640,
	UnsignedInt248 = 34042,
	UnsignedInt5999Rev = 35902,
	UnsignedIntSampler2D = 36306,
	UnsignedIntSampler2DArray = 36311,
	UnsignedIntSampler3D = 36307,
	UnsignedIntSamplerCube = 36308,
	UnsignedIntVec2 = 36294,
	UnsignedIntVec3 = 36295,
	UnsignedIntVec4 = 36296,
	UnsignedNormalized = 35863,
	VertexArrayBinding = 34229,
	VertexAttribArrayDivisor = 35070,
	VertexAttribArrayInteger = 35069,
	WaitFailed = 37149,
}
```

### New Type OpenTK.Graphics.ES30.TransformFeedbackMode

```
[Serializable]
public enum TransformFeedbackMode {
	InterleavedAttribs = 35980,
	SeparateAttribs = 35981,
}
```

### New Type OpenTK.Graphics.ES30.TransformFeedbackPrimitiveType

```
[Serializable]
public enum TransformFeedbackPrimitiveType {
	Lines = 1,
	Points = 0,
	Triangles = 4,
}
```

### New Type OpenTK.Graphics.ES30.TransformFeedbackTarget

```
[Serializable]
public enum TransformFeedbackTarget {
	TransformFeedback = 36386,
}
```

### New Type OpenTK.Graphics.ES30.TransformFeedbackType

```
[Serializable]
public enum TransformFeedbackType {
	Float = 5126,
	FloatMat2 = 35674,
	FloatMat2x3 = 35685,
	FloatMat2x4 = 35686,
	FloatMat3 = 35675,
	FloatMat3x2 = 35687,
	FloatMat3x4 = 35688,
	FloatMat4 = 35676,
	FloatMat4x2 = 35689,
	FloatMat4x3 = 35690,
	FloatVec2 = 35664,
	FloatVec3 = 35665,
	FloatVec4 = 35666,
	Int = 5124,
	IntVec2 = 35667,
	IntVec3 = 35668,
	IntVec4 = 35669,
	UnsignedInt = 5125,
	UnsignedIntVec2 = 36294,
	UnsignedIntVec3 = 36295,
	UnsignedIntVec4 = 36296,
}
```

### New Type OpenTK.Graphics.ES30.UniformTypes

```
[Serializable]
public enum UniformTypes {
	Bool = 35670,
	BoolVec2 = 35671,
	BoolVec3 = 35672,
	BoolVec4 = 35673,
	FloatMat2 = 35674,
	FloatMat3 = 35675,
	FloatMat4 = 35676,
	FloatVec2 = 35664,
	FloatVec3 = 35665,
	FloatVec4 = 35666,
	IntVec2 = 35667,
	IntVec3 = 35668,
	IntVec4 = 35669,
	Sampler2D = 35678,
	SamplerCube = 35680,
}
```

### New Type OpenTK.Graphics.ES30.Unknown

```
[Serializable]
public enum Unknown {
	ActiveProgramExt = 33369,
	AllShaderBitsExt = -1,
	AppleCopyTextureLevels = 1,
	AppleRgb422 = 1,
	AppleTextureFormatBgra8888 = 1,
	Bgra = 32993,
	Bgra8Ext = 37793,
	BgraExt = 32993,
	BgraImg = 32993,
	BufferObjectExt = 37201,
	CompareRefToTextureExt = 34894,
	CompressedRgbaPvrtc2Bppv1Img = 35843,
	CompressedRgbaPvrtc4Bppv1Img = 35842,
	CompressedRgbPvrtc2Bppv1Img = 35841,
	CompressedRgbPvrtc4Bppv1Img = 35840,
	CompressedSrgbAlphaPvrtc2Bppv1Ext = 35414,
	CompressedSrgbAlphaPvrtc4Bppv1Ext = 35415,
	CompressedSrgbPvrtc2Bppv1Ext = 35412,
	CompressedSrgbPvrtc4Bppv1Ext = 35413,
	ExtColorBufferHalfFloat = 1,
	ExtDebugLabel = 1,
	ExtDebugMarker = 1,
	ExtPvrtcSrgb = 1,
	ExtReadFormatBgra = 1,
	ExtSeparateShaderObjects = 1,
	ExtShaderFramebufferFetch = 1,
	ExtShaderTextureLod = 1,
	ExtShadowSamplers = 1,
	ExtTextureFilterAnisotropic = 1,
	FragmentShaderBitExt = 2,
	FragmentShaderDerivativeHintOes = 35723,
	FragmentShaderDiscardsSamplesExt = 35410,
	FramebufferAttachmentComponentTypeExt = 33297,
	ImgReadFormat = 1,
	ImgTextureCompressionPvrtc = 1,
	ImgTextureFormatBgra8888 = 1,
	MaxTextureMaxAnisotropyExt = 34047,
	OesStandardDerivatives = 1,
	ProgramObjectExt = 35648,
	ProgramPipelineBindingExt = 33370,
	ProgramPipelineObjectExt = 35407,
	ProgramSeparableExt = 33368,
	QueryObjectExt = 37203,
	R16fExt = 33325,
	Rg16fExt = 33327,
	Rgb16fExt = 34843,
	Rgb422Apple = 35359,
	Rgba16fExt = 34842,
	RgbRaw422Apple = 35409,
	Sampler = 33510,
	Sampler2DShadowExt = 35682,
	ShaderObjectExt = 35656,
	SyncObjectApple = 35411,
	TextureCompareFuncExt = 34893,
	TextureCompareModeExt = 34892,
	TextureMaxAnisotropyExt = 34046,
	UnsignedNormalizedExt = 35863,
	UnsignedShort1555Rev = 33638,
	UnsignedShort1555RevExt = 33638,
	UnsignedShort4444Rev = 33637,
	UnsignedShort4444RevExt = 33637,
	UnsignedShort4444RevImg = 33637,
	UnsignedShort88Apple = 34234,
	UnsignedShort88RevApple = 34235,
	VertexArrayObjectExt = 37204,
	VertexShaderBitExt = 1,
}
```

### New Type OpenTK.Graphics.ES30.VertexArrays

```
[Serializable]
public enum VertexArrays {
	VertexAttribArrayBufferBinding = 34975,
	VertexAttribArrayEnabled = 34338,
	VertexAttribArrayNormalized = 34922,
	VertexAttribArrayPointer = 34373,
	VertexAttribArraySize = 34339,
	VertexAttribArrayStride = 34340,
	VertexAttribArrayType = 34341,
}
```

### New Type OpenTK.Graphics.ES30.VertexAttribIntegerType

```
[Serializable]
public enum VertexAttribIntegerType {
	Byte = 5120,
	Int = 5124,
	Short = 5122,
	UnsignedByte = 5121,
	UnsignedInt = 5125,
	UnsignedShort = 5123,
}
```

### New Type OpenTK.Graphics.ES30.VertexAttribParameter

```
[Serializable]
public enum VertexAttribParameter {
	CurrentVertexAttrib = 34342,
	VertexAttribArrayBufferBinding = 34975,
	VertexAttribArrayDivisor = 35070,
	VertexAttribArrayEnabled = 34338,
	VertexAttribArrayInteger = 35069,
	VertexAttribArrayNormalized = 34922,
	VertexAttribArraySize = 34339,
	VertexAttribArrayStride = 34340,
	VertexAttribArrayType = 34341,
}
```

### New Type OpenTK.Graphics.ES30.VertexAttribPointerParameter

```
[Serializable]
public enum VertexAttribPointerParameter {
	VertexAttribArrayPointer = 34373,
}
```

### New Type OpenTK.Graphics.ES30.VertexAttribPointerType

```
[Serializable]
public enum VertexAttribPointerType {
	Byte = 5120,
	Fixed = 5132,
	Float = 5126,
	HalfFloat = 5131,
	Int = 5124,
	Int2101010Rev = 36255,
	Short = 5122,
	UnsignedByte = 5121,
	UnsignedInt = 5125,
	UnsignedInt2101010Rev = 33640,
	UnsignedShort = 5123,
}
```

### New Type OpenTK.Graphics.ES30.WaitSyncFlags

```
[Serializable]
public enum WaitSyncFlags {
	None = 0,
}
```

### New Type OpenTK.Graphics.ES30.WaitSyncStatus

```
[Serializable]
public enum WaitSyncStatus {
	AlreadySignaled = 37146,
	ConditionSatisfied = 37148,
	TimeoutExpired = 37147,
	WaitFailed = 37149,
}
```

   


 <hr>
