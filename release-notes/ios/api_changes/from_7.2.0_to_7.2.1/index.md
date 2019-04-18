---
id: 40E2656C-34B1-4007-8A02-DF6BD6EF15DF
title: "From 7.2.0 to 7.2.1"
---

# mscorlib.dll

## Namespace System.Globalization

### Type Changed: System.Globalization.Calendar

Added properties:

```
protected virtual int DaysInYearBeforeMinSupportedYear { get; }
```

### Type Changed: System.Globalization.ChineseLunisolarCalendar

Added properties:

```
protected override int DaysInYearBeforeMinSupportedYear { get; }
```

### Type Changed: System.Globalization.GregorianCalendar

Removed methods:

```
public override int GetWeekOfYear (System.DateTime time, CalendarWeekRule rule, System.DayOfWeek firstDayOfWeek);
```

### Type Changed: System.Globalization.HijriCalendar

Added properties:

```
protected override int DaysInYearBeforeMinSupportedYear { get; }
```

### Type Changed: System.Globalization.JapaneseLunisolarCalendar

Added properties:

```
protected override int DaysInYearBeforeMinSupportedYear { get; }
```

### Type Changed: System.Globalization.KoreanLunisolarCalendar

Added properties:

```
protected override int DaysInYearBeforeMinSupportedYear { get; }
```

### Type Changed: System.Globalization.TaiwanLunisolarCalendar

Added properties:

```
protected override int DaysInYearBeforeMinSupportedYear { get; }
```

### Type Changed: System.Globalization.UmAlQuraCalendar

Added properties:

```
protected override int DaysInYearBeforeMinSupportedYear { get; }
```

## Namespace System.Runtime.InteropServices

### Type Changed: System.Runtime.InteropServices.Marshal

Removed methods:

```
public static System.Delegate GetDelegateForFunctionPointer<T> (System.IntPtr ptr);
	public static object PtrToStructure<T> (System.IntPtr ptr);
```

Added methods:

```
public static TDelegate GetDelegateForFunctionPointer<TDelegate> (System.IntPtr ptr);
	public static T PtrToStructure<T> (System.IntPtr ptr);
```

## New Namespace System.Diagnostics.Tracing

### New Type System.Diagnostics.Tracing.EventCommandEventArgs

```
public class EventCommandEventArgs : System.EventArgs {
}
```

### New Type System.Diagnostics.Tracing.EventSource

```
public class EventSource : System.IDisposable {
	// constructors
	protected EventSource ();
	protected EventSource (bool throwOnEventWriteErrors);
	// methods
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public bool IsEnabled ();
	protected void WriteEvent (int eventId, int arg1, int arg2, int arg3);
}
```

   


 <hr>

# System.dll

## Namespace System.CodeDom.Compiler

### New Type System.CodeDom.Compiler.IndentedTextWriter

```
public class IndentedTextWriter : System.IO.TextWriter, System.IDisposable {
	// constructors
	public IndentedTextWriter (System.IO.TextWriter writer);
	public IndentedTextWriter (System.IO.TextWriter writer, string tabString);
	// fields
	public static const string DefaultTabString = "    ";
	// properties
	public override System.Text.Encoding Encoding { get; }
	public int Indent { get; set; }
	public System.IO.TextWriter InnerWriter { get; }
	public override string NewLine { get; set; }
	// methods
	public override void Close ();
	public override void Flush ();
	protected virtual void OutputTabs ();
	public override void Write (char value);
	public override void Write (bool value);
	public override void Write (string format, object arg0, object arg1);
	public override void Write (System.Char[] buffer, int index, int count);
	public override void Write (string format, System.Object[] args);
	public override void Write (string format, object arg);
	public override void Write (string value);
	public override void Write (System.Char[] value);
	public override void Write (double value);
	public override void Write (int value);
	public override void Write (long value);
	public override void Write (object value);
	public override void Write (float value);
	public override void WriteLine (string value);
	public override void WriteLine (uint value);
	public override void WriteLine (string format, object arg);
	public override void WriteLine (string format, System.Object[] args);
	public override void WriteLine (System.Char[] buffer, int index, int count);
	public override void WriteLine (string format, object arg0, object arg1);
	public override void WriteLine (float value);
	public override void WriteLine (bool value);
	public override void WriteLine (char value);
	public override void WriteLine (System.Char[] value);
	public override void WriteLine (double value);
	public override void WriteLine (int value);
	public override void WriteLine (long value);
	public override void WriteLine (object value);
	public override void WriteLine ();
	public void WriteLineNoTabs (string value);
}
```

## Namespace System.Net

### Type Changed: System.Net.HttpWebRequest

Added methods:

```
public System.IO.Stream EndGetRequestStream (System.IAsyncResult asyncResult, TransportContext& transportContext);
```

### Type Changed: System.Net.IPAddress

Added properties:

```
public bool IsIPv6Teredo { get; }
```

### Type Changed: System.Net.NetworkCredential

Added constructors:

```
public NetworkCredential (string userName, System.Security.SecureString password);
	public NetworkCredential (string userName, System.Security.SecureString password, string domain);
```

### Type Changed: System.Net.ServicePointManager

Added properties:

```
public static CipherSuitesCallback ClientCipherSuitesCallback { get; set; }
	public static CipherSuitesCallback ServerCipherSuitesCallback { get; set; }
```

### New Type System.Net.CipherSuitesCallback

```
public sealed delegate CipherSuitesCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CipherSuitesCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SecurityProtocolType protocol, System.Collections.Generic.IEnumerable<string> allCiphers, System.AsyncCallback callback, object object);
	public virtual System.Collections.Generic.IEnumerable<string> EndInvoke (System.IAsyncResult result);
	public virtual System.Collections.Generic.IEnumerable<string> Invoke (SecurityProtocolType protocol, System.Collections.Generic.IEnumerable<string> allCiphers);
}
```

## Namespace System.Net.Sockets

### Type Changed: System.Net.Sockets.NetworkStream

Removed constructors:

```
public NetworkStream (Socket socket, bool owns_socket);
	public NetworkStream (Socket socket, System.IO.FileAccess access, bool owns_socket);
```

Added constructors:

```
public NetworkStream (Socket socket, bool ownsSocket);
	public NetworkStream (Socket socket, System.IO.FileAccess access, bool ownsSocket);
```

## Namespace System.Security.Authentication

### Type Changed: System.Security.Authentication.SslProtocols

Added values:

```
Tls11 = 768,
	Tls12 = 3072,
```

## New Namespace System.Net.WebSockets

### New Type System.Net.WebSockets.ClientWebSocket

```
public class ClientWebSocket : System.Net.WebSockets.WebSocket, System.IDisposable {
	// constructors
	public ClientWebSocket ();
	// properties
	public override System.Net.WebSockets.WebSocketCloseStatus? CloseStatus { get; }
	public override string CloseStatusDescription { get; }
	public ClientWebSocketOptions Options { get; }
	public override WebSocketState State { get; }
	public override string SubProtocol { get; }
	// methods
	public override void Abort ();
	public override System.Threading.Tasks.Task CloseAsync (WebSocketCloseStatus closeStatus, string statusDescription, System.Threading.CancellationToken cancellationToken);
	public override System.Threading.Tasks.Task CloseOutputAsync (WebSocketCloseStatus closeStatus, string statusDescription, System.Threading.CancellationToken cancellationToken);
	public System.Threading.Tasks.Task ConnectAsync (System.Uri uri, System.Threading.CancellationToken cancellationToken);
	public override void Dispose ();
	public override System.Threading.Tasks.Task<WebSocketReceiveResult> ReceiveAsync (System.ArraySegment<byte> buffer, System.Threading.CancellationToken cancellationToken);
	public override System.Threading.Tasks.Task SendAsync (System.ArraySegment<byte> buffer, WebSocketMessageType messageType, bool endOfMessage, System.Threading.CancellationToken cancellationToken);
}
```

### New Type System.Net.WebSockets.ClientWebSocketOptions

```
public sealed class ClientWebSocketOptions {
	// constructors
	public ClientWebSocketOptions ();
	// properties
	public System.Security.Cryptography.X509Certificates.X509CertificateCollection ClientCertificates { get; set; }
	public System.Net.CookieContainer Cookies { get; set; }
	public System.Net.ICredentials Credentials { get; set; }
	public System.TimeSpan KeepAliveInterval { get; set; }
	public System.Net.IWebProxy Proxy { get; set; }
	public bool UseDefaultCredentials { get; set; }
	// methods
	public void AddSubProtocol (string subProtocol);
	public void SetBuffer (int receiveBufferSize, int sendBufferSize);
	public void SetBuffer (int receiveBufferSize, int sendBufferSize, System.ArraySegment<byte> buffer);
	public void SetRequestHeader (string headerName, string headerValue);
}
```

### New Type System.Net.WebSockets.HttpListenerWebSocketContext

```
public class HttpListenerWebSocketContext : System.Net.WebSockets.WebSocketContext {
	// constructors
	public HttpListenerWebSocketContext ();
	// properties
	public override System.Net.CookieCollection CookieCollection { get; }
	public override System.Collections.Specialized.NameValueCollection Headers { get; }
	public override bool IsAuthenticated { get; }
	public override bool IsLocal { get; }
	public override bool IsSecureConnection { get; }
	public override string Origin { get; }
	public override System.Uri RequestUri { get; }
	public override string SecWebSocketKey { get; }
	public override System.Collections.Generic.IEnumerable<string> SecWebSocketProtocols { get; }
	public override string SecWebSocketVersion { get; }
	public override System.Security.Principal.IPrincipal User { get; }
	public override WebSocket WebSocket { get; }
}
```

### New Type System.Net.WebSockets.WebSocket

```
public abstract class WebSocket : System.IDisposable {
	// constructors
	protected WebSocket ();
	// properties
	public virtual System.Net.WebSockets.WebSocketCloseStatus? CloseStatus { get; }
	public virtual string CloseStatusDescription { get; }
	public static System.TimeSpan DefaultKeepAliveInterval { get; }
	public virtual WebSocketState State { get; }
	public virtual string SubProtocol { get; }
	// methods
	public virtual void Abort ();
	public virtual System.Threading.Tasks.Task CloseAsync (WebSocketCloseStatus closeStatus, string statusDescription, System.Threading.CancellationToken cancellationToken);
	public virtual System.Threading.Tasks.Task CloseOutputAsync (WebSocketCloseStatus closeStatus, string statusDescription, System.Threading.CancellationToken cancellationToken);
	public static System.ArraySegment<byte> CreateClientBuffer (int receiveBufferSize, int sendBufferSize);
	public static WebSocket CreateClientWebSocket (System.IO.Stream innerStream, string subProtocol, int receiveBufferSize, int sendBufferSize, System.TimeSpan keepAliveInterval, bool useZeroMaskingKey, System.ArraySegment<byte> internalBuffer);
	public static System.ArraySegment<byte> CreateServerBuffer (int receiveBufferSize);
	public virtual void Dispose ();
	[Obsolete ("")]
	public static bool IsApplicationTargeting45 ();

	protected static bool IsStateTerminal (WebSocketState state);
	public virtual System.Threading.Tasks.Task<WebSocketReceiveResult> ReceiveAsync (System.ArraySegment<byte> buffer, System.Threading.CancellationToken cancellationToken);
	public static void RegisterPrefixes ();
	public virtual System.Threading.Tasks.Task SendAsync (System.ArraySegment<byte> buffer, WebSocketMessageType messageType, bool endOfMessage, System.Threading.CancellationToken cancellationToken);
	protected static void ThrowOnInvalidState (WebSocketState state, WebSocketState[] validStates);
}
```

### New Type System.Net.WebSockets.WebSocketCloseStatus

```
[Serializable]
public enum WebSocketCloseStatus {
	Empty = 1004,
	EndpointUnavailable = 1001,
	InternalServerError = 1011,
	InvalidMessageType = 1003,
	InvalidPayloadData = 1007,
	MandatoryExtension = 1010,
	MessageTooBig = 1004,
	NormalClosure = 1000,
	PolicyViolation = 1008,
	ProtocolError = 1002,
}
```

### New Type System.Net.WebSockets.WebSocketContext

```
public abstract class WebSocketContext {
	// constructors
	protected WebSocketContext ();
	// properties
	public virtual System.Net.CookieCollection CookieCollection { get; }
	public virtual System.Collections.Specialized.NameValueCollection Headers { get; }
	public virtual bool IsAuthenticated { get; }
	public virtual bool IsLocal { get; }
	public virtual bool IsSecureConnection { get; }
	public virtual string Origin { get; }
	public virtual System.Uri RequestUri { get; }
	public virtual string SecWebSocketKey { get; }
	public virtual System.Collections.Generic.IEnumerable<string> SecWebSocketProtocols { get; }
	public virtual string SecWebSocketVersion { get; }
	public virtual System.Security.Principal.IPrincipal User { get; }
	public virtual WebSocket WebSocket { get; }
}
```

### New Type System.Net.WebSockets.WebSocketError

```
[Serializable]
public enum WebSocketError {
	ConnectionClosedPrematurely = 8,
	Faulted = 2,
	HeaderError = 7,
	InvalidMessageType = 1,
	InvalidState = 9,
	NativeError = 3,
	NotAWebSocket = 4,
	Success = 0,
	UnsupportedProtocol = 6,
	UnsupportedVersion = 5,
}
```

### New Type System.Net.WebSockets.WebSocketException

```
public sealed class WebSocketException : System.ComponentModel.Win32Exception, System.Runtime.Serialization.ISerializable {
	// constructors
	public WebSocketException ();
	public WebSocketException (WebSocketError error, string message, System.Exception innerException);
	public WebSocketException (WebSocketError error, int nativeError, string message);
	public WebSocketException (WebSocketError error, int nativeError, System.Exception innerException);
	public WebSocketException (WebSocketError error, string message);
	public WebSocketException (WebSocketError error, int nativeError);
	public WebSocketException (WebSocketError error, System.Exception innerException);
	public WebSocketException (int nativeError);
	public WebSocketException (string message);
	public WebSocketException (WebSocketError error);
	public WebSocketException (int nativeError, System.Exception innerException);
	public WebSocketException (int nativeError, string message);
	public WebSocketException (string message, System.Exception innerException);
	public WebSocketException (WebSocketError error, int nativeError, string message, System.Exception innerException);
	// properties
	public WebSocketError WebSocketErrorCode { get; }
}
```

### New Type System.Net.WebSockets.WebSocketMessageType

```
[Serializable]
public enum WebSocketMessageType {
	Binary = 2,
	Close = 8,
	Text = 1,
}
```

### New Type System.Net.WebSockets.WebSocketReceiveResult

```
public class WebSocketReceiveResult {
	// constructors
	public WebSocketReceiveResult (int count, WebSocketMessageType messageType, bool endOfMessage);
	public WebSocketReceiveResult (int count, WebSocketMessageType messageType, bool endOfMessage, System.Net.WebSockets.WebSocketCloseStatus? closeStatus, string closeStatusDescription);
	// properties
	public System.Net.WebSockets.WebSocketCloseStatus? CloseStatus { get; }
	public string CloseStatusDescription { get; }
	public int Count { get; }
	public bool EndOfMessage { get; }
	public WebSocketMessageType MessageType { get; }
}
```

### New Type System.Net.WebSockets.WebSocketState

```
[Serializable]
public enum WebSocketState {
	Aborted = 6,
	Closed = 5,
	CloseReceived = 4,
	CloseSent = 3,
	Connecting = 1,
	None = 0,
	Open = 2,
}
```

   


 <hr>

# System.Core.dll

## Namespace System.Linq.Expressions

### Type Changed: System.Linq.Expressions.BinaryExpression

Added properties:

```
public override bool CanReduce { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public override Expression Reduce ();
	public BinaryExpression Update (Expression left, LambdaExpression conversion, Expression right);
```

### Type Changed: System.Linq.Expressions.ConditionalExpression

Added properties:

```
public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public ConditionalExpression Update (Expression test, Expression ifTrue, Expression ifFalse);
```

### Type Changed: System.Linq.Expressions.ConstantExpression

Added properties:

```
public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
```

### Type Changed: System.Linq.Expressions.ElementInit

Added methods:

```
public ElementInit Update (System.Collections.Generic.IEnumerable<Expression> arguments);
```

### Type Changed: System.Linq.Expressions.Expression

Removed constructors:

```
protected Expression (ExpressionType node_type, System.Type type);
```

Added constructors:

```
[Obsolete ("use a different constructor that does not take ExpressionType. Then override NodeType and Type properties to provide the values that would be specified to this constructor.")]
	protected Expression (ExpressionType nodeType, System.Type type);

	protected Expression ();
```

Added properties:

```
public virtual bool CanReduce { get; }
```

Added methods:

```
protected virtual Expression Accept (ExpressionVisitor visitor);
	public static BinaryExpression AddAssign (Expression left, Expression right);
	public static BinaryExpression AddAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression AddAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression AddAssignChecked (Expression left, Expression right);
	public static BinaryExpression AddAssignChecked (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression AddAssignChecked (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression AndAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression AndAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression AndAssign (Expression left, Expression right);
	public static IndexExpression ArrayAccess (Expression array, System.Collections.Generic.IEnumerable<Expression> indexes);
	public static IndexExpression ArrayAccess (Expression array, Expression[] indexes);
	public static BinaryExpression Assign (Expression left, Expression right);
	public static BlockExpression Block (System.Type type, System.Collections.Generic.IEnumerable<Expression> expressions);
	public static BlockExpression Block (System.Collections.Generic.IEnumerable<ParameterExpression> variables, Expression[] expressions);
	public static BlockExpression Block (System.Type type, System.Collections.Generic.IEnumerable<ParameterExpression> variables, Expression[] expressions);
	public static BlockExpression Block (System.Collections.Generic.IEnumerable<ParameterExpression> variables, System.Collections.Generic.IEnumerable<Expression> expressions);
	public static BlockExpression Block (System.Type type, System.Collections.Generic.IEnumerable<ParameterExpression> variables, System.Collections.Generic.IEnumerable<Expression> expressions);
	public static BlockExpression Block (System.Type type, Expression[] expressions);
	public static BlockExpression Block (Expression arg0, Expression arg1);
	public static BlockExpression Block (Expression arg0, Expression arg1, Expression arg2);
	public static BlockExpression Block (Expression arg0, Expression arg1, Expression arg2, Expression arg3);
	public static BlockExpression Block (Expression arg0, Expression arg1, Expression arg2, Expression arg3, Expression arg4);
	public static BlockExpression Block (Expression[] expressions);
	public static BlockExpression Block (System.Collections.Generic.IEnumerable<Expression> expressions);
	public static GotoExpression Break (LabelTarget target, Expression value);
	public static GotoExpression Break (LabelTarget target);
	public static GotoExpression Break (LabelTarget target, System.Type type);
	public static GotoExpression Break (LabelTarget target, Expression value, System.Type type);
	public static MethodCallExpression Call (System.Reflection.MethodInfo method, System.Collections.Generic.IEnumerable<Expression> arguments);
	public static MethodCallExpression Call (System.Reflection.MethodInfo method, Expression arg0, Expression arg1, Expression arg2, Expression arg3, Expression arg4);
	public static MethodCallExpression Call (System.Reflection.MethodInfo method, Expression arg0, Expression arg1, Expression arg2, Expression arg3);
	public static MethodCallExpression Call (System.Reflection.MethodInfo method, Expression arg0, Expression arg1, Expression arg2);
	public static MethodCallExpression Call (System.Reflection.MethodInfo method, Expression arg0, Expression arg1);
	public static MethodCallExpression Call (System.Reflection.MethodInfo method, Expression arg0);
	public static MethodCallExpression Call (Expression instance, System.Reflection.MethodInfo method, Expression arg0, Expression arg1, Expression arg2);
	public static MethodCallExpression Call (Expression instance, System.Reflection.MethodInfo method, Expression arg0, Expression arg1);
	public static CatchBlock Catch (System.Type type, Expression body);
	public static CatchBlock Catch (System.Type type, Expression body, Expression filter);
	public static CatchBlock Catch (ParameterExpression variable, Expression body, Expression filter);
	public static CatchBlock Catch (ParameterExpression variable, Expression body);
	public static DebugInfoExpression ClearDebugInfo (SymbolDocumentInfo document);
	public static ConditionalExpression Condition (Expression test, Expression ifTrue, Expression ifFalse, System.Type type);
	public static GotoExpression Continue (LabelTarget target);
	public static GotoExpression Continue (LabelTarget target, System.Type type);
	public static DebugInfoExpression DebugInfo (SymbolDocumentInfo document, int startLine, int startColumn, int endLine, int endColumn);
	public static UnaryExpression Decrement (Expression expression);
	public static UnaryExpression Decrement (Expression expression, System.Reflection.MethodInfo method);
	public static DefaultExpression Default (System.Type type);
	public static BinaryExpression DivideAssign (Expression left, Expression right);
	public static BinaryExpression DivideAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression DivideAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, System.Collections.Generic.IEnumerable<Expression> arguments);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1, Expression arg2, Expression arg3);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1, Expression arg2);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0, Expression arg1);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression arg0);
	public static DynamicExpression Dynamic (System.Runtime.CompilerServices.CallSiteBinder binder, System.Type returnType, Expression[] arguments);
	public static DefaultExpression Empty ();
	public static BinaryExpression ExclusiveOrAssign (Expression left, Expression right);
	public static BinaryExpression ExclusiveOrAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression ExclusiveOrAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static MemberExpression Field (Expression expression, System.Type type, string fieldName);
	public static System.Type GetDelegateType (System.Type[] typeArgs);
	public static GotoExpression Goto (LabelTarget target, Expression value);
	public static GotoExpression Goto (LabelTarget target, System.Type type);
	public static GotoExpression Goto (LabelTarget target, Expression value, System.Type type);
	public static GotoExpression Goto (LabelTarget target);
	public static ConditionalExpression IfThen (Expression test, Expression ifTrue);
	public static ConditionalExpression IfThenElse (Expression test, Expression ifTrue, Expression ifFalse);
	public static UnaryExpression Increment (Expression expression, System.Reflection.MethodInfo method);
	public static UnaryExpression Increment (Expression expression);
	public static UnaryExpression IsFalse (Expression expression);
	public static UnaryExpression IsFalse (Expression expression, System.Reflection.MethodInfo method);
	public static UnaryExpression IsTrue (Expression expression);
	public static UnaryExpression IsTrue (Expression expression, System.Reflection.MethodInfo method);
	public static LabelExpression Label (LabelTarget target);
	public static LabelTarget Label ();
	public static LabelTarget Label (string name);
	public static LabelTarget Label (System.Type type, string name);
	public static LabelExpression Label (LabelTarget target, Expression defaultValue);
	public static LabelTarget Label (System.Type type);
	public static LambdaExpression Lambda (Expression body, bool tailCall, ParameterExpression[] parameters);
	public static System.Linq.Expressions.Expression<TDelegate> Lambda<TDelegate> (Expression body, string name, bool tailCall, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static System.Linq.Expressions.Expression<TDelegate> Lambda<TDelegate> (Expression body, bool tailCall, ParameterExpression[] parameters);
	public static LambdaExpression Lambda (System.Type delegateType, Expression body, bool tailCall, ParameterExpression[] parameters);
	public static LambdaExpression Lambda (Expression body, bool tailCall, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static System.Linq.Expressions.Expression<TDelegate> Lambda<TDelegate> (Expression body, bool tailCall, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static LambdaExpression Lambda (System.Type delegateType, Expression body, bool tailCall, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static LambdaExpression Lambda (Expression body, string name, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static LambdaExpression Lambda (Expression body, string name, bool tailCall, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static LambdaExpression Lambda (System.Type delegateType, Expression body, string name, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static System.Linq.Expressions.Expression<TDelegate> Lambda<TDelegate> (Expression body, string name, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static LambdaExpression Lambda (System.Type delegateType, Expression body, string name, bool tailCall, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static LambdaExpression Lambda (Expression body, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
	public static BinaryExpression LeftShiftAssign (Expression left, Expression right);
	public static BinaryExpression LeftShiftAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression LeftShiftAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static LoopExpression Loop (Expression body, LabelTarget break);
	public static LoopExpression Loop (Expression body);
	public static LoopExpression Loop (Expression body, LabelTarget break, LabelTarget continue);
	public static CatchBlock MakeCatchBlock (System.Type type, ParameterExpression variable, Expression body, Expression filter);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1, Expression arg2, Expression arg3);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1, Expression arg2);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0, Expression arg1);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression arg0);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, System.Collections.Generic.IEnumerable<Expression> arguments);
	public static DynamicExpression MakeDynamic (System.Type delegateType, System.Runtime.CompilerServices.CallSiteBinder binder, Expression[] arguments);
	public static GotoExpression MakeGoto (GotoExpressionKind kind, LabelTarget target, Expression value, System.Type type);
	public static IndexExpression MakeIndex (Expression instance, System.Reflection.PropertyInfo indexer, System.Collections.Generic.IEnumerable<Expression> arguments);
	public static TryExpression MakeTry (System.Type type, Expression body, Expression finally, Expression fault, System.Collections.Generic.IEnumerable<CatchBlock> handlers);
	public static BinaryExpression ModuloAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression ModuloAssign (Expression left, Expression right);
	public static BinaryExpression ModuloAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression MultiplyAssign (Expression left, Expression right);
	public static BinaryExpression MultiplyAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression MultiplyAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression MultiplyAssignChecked (Expression left, Expression right);
	public static BinaryExpression MultiplyAssignChecked (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression MultiplyAssignChecked (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static UnaryExpression OnesComplement (Expression expression, System.Reflection.MethodInfo method);
	public static UnaryExpression OnesComplement (Expression expression);
	public static BinaryExpression OrAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression OrAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression OrAssign (Expression left, Expression right);
	public static ParameterExpression Parameter (System.Type type);
	public static UnaryExpression PostDecrementAssign (Expression expression, System.Reflection.MethodInfo method);
	public static UnaryExpression PostDecrementAssign (Expression expression);
	public static UnaryExpression PostIncrementAssign (Expression expression, System.Reflection.MethodInfo method);
	public static UnaryExpression PostIncrementAssign (Expression expression);
	public static BinaryExpression PowerAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression PowerAssign (Expression left, Expression right);
	public static BinaryExpression PowerAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static UnaryExpression PreDecrementAssign (Expression expression, System.Reflection.MethodInfo method);
	public static UnaryExpression PreDecrementAssign (Expression expression);
	public static UnaryExpression PreIncrementAssign (Expression expression);
	public static UnaryExpression PreIncrementAssign (Expression expression, System.Reflection.MethodInfo method);
	public static IndexExpression Property (Expression instance, System.Reflection.PropertyInfo indexer, System.Collections.Generic.IEnumerable<Expression> arguments);
	public static IndexExpression Property (Expression instance, System.Reflection.PropertyInfo indexer, Expression[] arguments);
	public static IndexExpression Property (Expression instance, string propertyName, Expression[] arguments);
	public static MemberExpression Property (Expression expression, System.Type type, string propertyName);
	public virtual Expression Reduce ();
	public Expression ReduceAndCheck ();
	public Expression ReduceExtensions ();
	public static BinaryExpression ReferenceEqual (Expression left, Expression right);
	public static BinaryExpression ReferenceNotEqual (Expression left, Expression right);
	public static UnaryExpression Rethrow (System.Type type);
	public static UnaryExpression Rethrow ();
	public static GotoExpression Return (LabelTarget target, Expression value, System.Type type);
	public static GotoExpression Return (LabelTarget target, Expression value);
	public static GotoExpression Return (LabelTarget target, System.Type type);
	public static GotoExpression Return (LabelTarget target);
	public static BinaryExpression RightShiftAssign (Expression left, Expression right);
	public static BinaryExpression RightShiftAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression RightShiftAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static RuntimeVariablesExpression RuntimeVariables (ParameterExpression[] variables);
	public static RuntimeVariablesExpression RuntimeVariables (System.Collections.Generic.IEnumerable<ParameterExpression> variables);
	public static BinaryExpression SubtractAssign (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static BinaryExpression SubtractAssign (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression SubtractAssign (Expression left, Expression right);
	public static BinaryExpression SubtractAssignChecked (Expression left, Expression right);
	public static BinaryExpression SubtractAssignChecked (Expression left, Expression right, System.Reflection.MethodInfo method);
	public static BinaryExpression SubtractAssignChecked (Expression left, Expression right, System.Reflection.MethodInfo method, LambdaExpression conversion);
	public static SwitchExpression Switch (System.Type type, Expression switchValue, Expression defaultBody, System.Reflection.MethodInfo comparison, SwitchCase[] cases);
	public static SwitchExpression Switch (Expression switchValue, SwitchCase[] cases);
	public static SwitchExpression Switch (System.Type type, Expression switchValue, Expression defaultBody, System.Reflection.MethodInfo comparison, System.Collections.Generic.IEnumerable<SwitchCase> cases);
	public static SwitchExpression Switch (Expression switchValue, Expression defaultBody, System.Reflection.MethodInfo comparison, SwitchCase[] cases);
	public static SwitchExpression Switch (Expression switchValue, Expression defaultBody, System.Reflection.MethodInfo comparison, System.Collections.Generic.IEnumerable<SwitchCase> cases);
	public static SwitchExpression Switch (Expression switchValue, Expression defaultBody, SwitchCase[] cases);
	public static SwitchCase SwitchCase (Expression body, System.Collections.Generic.IEnumerable<Expression> testValues);
	public static SwitchCase SwitchCase (Expression body, Expression[] testValues);
	public static SymbolDocumentInfo SymbolDocument (string fileName, System.Guid language, System.Guid languageVendor, System.Guid documentType);
	public static SymbolDocumentInfo SymbolDocument (string fileName, System.Guid language, System.Guid languageVendor);
	public static SymbolDocumentInfo SymbolDocument (string fileName);
	public static SymbolDocumentInfo SymbolDocument (string fileName, System.Guid language);
	public static UnaryExpression Throw (Expression value, System.Type type);
	public static UnaryExpression Throw (Expression value);
	public static TryExpression TryCatch (Expression body, CatchBlock[] handlers);
	public static TryExpression TryCatchFinally (Expression body, Expression finally, CatchBlock[] handlers);
	public static TryExpression TryFault (Expression body, Expression fault);
	public static TryExpression TryFinally (Expression body, Expression finally);
	public static bool TryGetActionType (System.Type[] typeArgs, System.Type& actionType);
	public static bool TryGetFuncType (System.Type[] typeArgs, System.Type& funcType);
	public static TypeBinaryExpression TypeEqual (Expression expression, System.Type type);
	public static UnaryExpression Unbox (Expression expression, System.Type type);
	public static ParameterExpression Variable (System.Type type, string name);
	public static ParameterExpression Variable (System.Type type);
	protected virtual Expression VisitChildren (ExpressionVisitor visitor);
```

### Type Changed: System.Linq.Expressions.Expression`1

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public TDelegate Compile (System.Runtime.CompilerServices.DebugInfoGenerator debugInfoGenerator);
	public System.Linq.Expressions.Expression<TDelegate> Update (Expression body, System.Collections.Generic.IEnumerable<ParameterExpression> parameters);
```

### Type Changed: System.Linq.Expressions.ExpressionType

Added values:

```
AddAssign = 63,
	AddAssignChecked = 74,
	AndAssign = 64,
	Assign = 46,
	Block = 47,
	DebugInfo = 48,
	Decrement = 49,
	Default = 51,
	DivideAssign = 65,
	Dynamic = 50,
	ExclusiveOrAssign = 66,
	Extension = 52,
	Goto = 53,
	Increment = 54,
	Index = 55,
	IsFalse = 84,
	IsTrue = 83,
	Label = 56,
	LeftShiftAssign = 67,
	Loop = 58,
	ModuloAssign = 68,
	MultiplyAssign = 69,
	MultiplyAssignChecked = 75,
	OnesComplement = 82,
	OrAssign = 70,
	PostDecrementAssign = 80,
	PostIncrementAssign = 79,
	PowerAssign = 71,
	PreDecrementAssign = 78,
	PreIncrementAssign = 77,
	RightShiftAssign = 72,
	RuntimeVariables = 57,
	SubtractAssign = 73,
	SubtractAssignChecked = 76,
	Switch = 59,
	Throw = 60,
	Try = 61,
	TypeEqual = 81,
	Unbox = 62,
```

### Type Changed: System.Linq.Expressions.ExpressionVisitor

Removed methods:

```
protected virtual void Visit (Expression expression);
	protected virtual void VisitBinary (BinaryExpression binary);
	protected virtual void VisitBinding (MemberBinding binding);
	protected virtual void VisitBindingList (System.Collections.ObjectModel.ReadOnlyCollection<MemberBinding> list);
	protected virtual void VisitConditional (ConditionalExpression conditional);
	protected virtual void VisitConstant (ConstantExpression constant);
	protected virtual void VisitElementInitializer (ElementInit initializer);
	protected virtual void VisitElementInitializerList (System.Collections.ObjectModel.ReadOnlyCollection<ElementInit> list);
	protected virtual void VisitExpressionList (System.Collections.ObjectModel.ReadOnlyCollection<Expression> list);
	protected virtual void VisitInvocation (InvocationExpression invocation);
	protected virtual void VisitLambda (LambdaExpression lambda);
	protected virtual void VisitList<T> (System.Collections.ObjectModel.ReadOnlyCollection<T> list, System.Action<T> visitor);
	protected virtual void VisitListInit (ListInitExpression init);
	protected virtual void VisitMemberAccess (MemberExpression member);
	protected virtual void VisitMemberAssignment (MemberAssignment assignment);
	protected virtual void VisitMemberInit (MemberInitExpression init);
	protected virtual void VisitMemberListBinding (MemberListBinding binding);
	protected virtual void VisitMemberMemberBinding (MemberMemberBinding binding);
	protected virtual void VisitMethodCall (MethodCallExpression methodCall);
	protected virtual void VisitNew (NewExpression nex);
	protected virtual void VisitNewArray (NewArrayExpression newArray);
	protected virtual void VisitParameter (ParameterExpression parameter);
	protected virtual void VisitTypeIs (TypeBinaryExpression type);
	protected virtual void VisitUnary (UnaryExpression unary);
```

Added methods:

```
public virtual Expression Visit (Expression node);
	public System.Collections.ObjectModel.ReadOnlyCollection<Expression> Visit (System.Collections.ObjectModel.ReadOnlyCollection<Expression> nodes);
	public static System.Collections.ObjectModel.ReadOnlyCollection<T> Visit<T> (System.Collections.ObjectModel.ReadOnlyCollection<T> nodes, System.Func<T,T> elementVisitor);
	public T VisitAndConvert<T> (T node, string callerName);
	public System.Collections.ObjectModel.ReadOnlyCollection<T> VisitAndConvert<T> (System.Collections.ObjectModel.ReadOnlyCollection<T> nodes, string callerName);
	protected virtual Expression VisitBinary (BinaryExpression node);
	protected virtual Expression VisitBlock (BlockExpression node);
	protected virtual CatchBlock VisitCatchBlock (CatchBlock node);
	protected virtual Expression VisitConditional (ConditionalExpression node);
	protected virtual Expression VisitConstant (ConstantExpression node);
	protected virtual Expression VisitDebugInfo (DebugInfoExpression node);
	protected virtual Expression VisitDefault (DefaultExpression node);
	protected virtual Expression VisitDynamic (DynamicExpression node);
	protected virtual ElementInit VisitElementInit (ElementInit node);
	protected virtual Expression VisitExtension (Expression node);
	protected virtual Expression VisitGoto (GotoExpression node);
	protected virtual Expression VisitIndex (IndexExpression node);
	protected virtual Expression VisitInvocation (InvocationExpression node);
	protected virtual Expression VisitLabel (LabelExpression node);
	protected virtual LabelTarget VisitLabelTarget (LabelTarget node);
	protected virtual Expression VisitLambda<T> (System.Linq.Expressions.Expression<T> node);
	protected virtual Expression VisitListInit (ListInitExpression node);
	protected virtual Expression VisitLoop (LoopExpression node);
	protected virtual Expression VisitMember (MemberExpression node);
	protected virtual MemberAssignment VisitMemberAssignment (MemberAssignment node);
	protected virtual MemberBinding VisitMemberBinding (MemberBinding node);
	protected virtual Expression VisitMemberInit (MemberInitExpression node);
	protected virtual MemberListBinding VisitMemberListBinding (MemberListBinding node);
	protected virtual MemberMemberBinding VisitMemberMemberBinding (MemberMemberBinding node);
	protected virtual Expression VisitMethodCall (MethodCallExpression node);
	protected virtual Expression VisitNew (NewExpression node);
	protected virtual Expression VisitNewArray (NewArrayExpression node);
	protected virtual Expression VisitParameter (ParameterExpression node);
	protected virtual Expression VisitRuntimeVariables (RuntimeVariablesExpression node);
	protected virtual Expression VisitSwitch (SwitchExpression node);
	protected virtual SwitchCase VisitSwitchCase (SwitchCase node);
	protected virtual Expression VisitTry (TryExpression node);
	protected virtual Expression VisitTypeBinary (TypeBinaryExpression node);
	protected virtual Expression VisitUnary (UnaryExpression node);
```

### Type Changed: System.Linq.Expressions.InvocationExpression

Added properties:

```
public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public InvocationExpression Update (Expression expression, System.Collections.Generic.IEnumerable<Expression> arguments);
```

### Type Changed: System.Linq.Expressions.LambdaExpression

Added properties:

```
public string Name { get; }
	public override ExpressionType NodeType { get; }
	public System.Type ReturnType { get; }
	public bool TailCall { get; }
	public override System.Type Type { get; }
```

Added methods:

```
public System.Delegate Compile (System.Runtime.CompilerServices.DebugInfoGenerator debugInfoGenerator);
```

### Type Changed: System.Linq.Expressions.ListInitExpression

Added properties:

```
public override bool CanReduce { get; }
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public override Expression Reduce ();
	public ListInitExpression Update (NewExpression newExpression, System.Collections.Generic.IEnumerable<ElementInit> initializers);
```

### Type Changed: System.Linq.Expressions.MemberAssignment

Added methods:

```
public MemberAssignment Update (Expression expression);
```

### Type Changed: System.Linq.Expressions.MemberBinding

Removed constructors:

```
protected MemberBinding (MemberBindingType binding_type, System.Reflection.MemberInfo member);
```

Added constructors:

```
[Obsolete ("Do not use this constructor. It will be removed in future releases.")]
	protected MemberBinding (MemberBindingType type, System.Reflection.MemberInfo member);
```

### Type Changed: System.Linq.Expressions.MemberExpression

Added properties:

```
public override ExpressionType NodeType { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public MemberExpression Update (Expression expression);
```

### Type Changed: System.Linq.Expressions.MemberInitExpression

Added properties:

```
public override bool CanReduce { get; }
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public override Expression Reduce ();
	public MemberInitExpression Update (NewExpression newExpression, System.Collections.Generic.IEnumerable<MemberBinding> bindings);
```

### Type Changed: System.Linq.Expressions.MemberListBinding

Added methods:

```
public MemberListBinding Update (System.Collections.Generic.IEnumerable<ElementInit> initializers);
```

### Type Changed: System.Linq.Expressions.MemberMemberBinding

Added methods:

```
public MemberMemberBinding Update (System.Collections.Generic.IEnumerable<MemberBinding> bindings);
```

### Type Changed: System.Linq.Expressions.MethodCallExpression

Added properties:

```
public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public MethodCallExpression Update (Expression object, System.Collections.Generic.IEnumerable<Expression> arguments);
```

### Type Changed: System.Linq.Expressions.NewArrayExpression

Added properties:

```
public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public NewArrayExpression Update (System.Collections.Generic.IEnumerable<Expression> expressions);
```

### Type Changed: System.Linq.Expressions.NewExpression

Added properties:

```
public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public NewExpression Update (System.Collections.Generic.IEnumerable<Expression> arguments);
```

### Type Changed: System.Linq.Expressions.ParameterExpression

Added properties:

```
public bool IsByRef { get; }
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
```

### Type Changed: System.Linq.Expressions.TypeBinaryExpression

Added properties:

```
public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public TypeBinaryExpression Update (Expression expression);
```

### Type Changed: System.Linq.Expressions.UnaryExpression

Added properties:

```
public override bool CanReduce { get; }
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
```

Added methods:

```
protected override Expression Accept (ExpressionVisitor visitor);
	public override Expression Reduce ();
	public UnaryExpression Update (Expression operand);
```

### New Type System.Linq.Expressions.BlockExpression

```
public class BlockExpression : System.Linq.Expressions.Expression {
	// properties
	public System.Collections.ObjectModel.ReadOnlyCollection<Expression> Expressions { get; }
	public override ExpressionType NodeType { get; }
	public Expression Result { get; }
	public override System.Type Type { get; }
	public System.Collections.ObjectModel.ReadOnlyCollection<ParameterExpression> Variables { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public BlockExpression Update (System.Collections.Generic.IEnumerable<ParameterExpression> variables, System.Collections.Generic.IEnumerable<Expression> expressions);
}
```

### New Type System.Linq.Expressions.CatchBlock

```
public sealed class CatchBlock {
	// properties
	public Expression Body { get; }
	public Expression Filter { get; }
	public System.Type Test { get; }
	public ParameterExpression Variable { get; }
	// methods
	public override string ToString ();
	public CatchBlock Update (ParameterExpression variable, Expression filter, Expression body);
}
```

### New Type System.Linq.Expressions.DebugInfoExpression

```
public class DebugInfoExpression : System.Linq.Expressions.Expression {
	// properties
	public SymbolDocumentInfo Document { get; }
	public virtual int EndColumn { get; }
	public virtual int EndLine { get; }
	public virtual bool IsClear { get; }
	public override ExpressionType NodeType { get; }
	public virtual int StartColumn { get; }
	public virtual int StartLine { get; }
	public override System.Type Type { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
}
```

### New Type System.Linq.Expressions.DefaultExpression

```
public sealed class DefaultExpression : System.Linq.Expressions.Expression {
	// properties
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
}
```

### New Type System.Linq.Expressions.DynamicExpression

```
public class DynamicExpression : System.Linq.Expressions.Expression {
	// properties
	public System.Collections.ObjectModel.ReadOnlyCollection<Expression> Arguments { get; }
	public System.Runtime.CompilerServices.CallSiteBinder Binder { get; }
	public System.Type DelegateType { get; }
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public DynamicExpression Update (System.Collections.Generic.IEnumerable<Expression> arguments);
}
```

### New Type System.Linq.Expressions.DynamicExpressionVisitor

```
public abstract class DynamicExpressionVisitor : System.Linq.Expressions.ExpressionVisitor {
	// constructors
	protected DynamicExpressionVisitor ();
}
```

### New Type System.Linq.Expressions.GotoExpression

```
public sealed class GotoExpression : System.Linq.Expressions.Expression {
	// properties
	public GotoExpressionKind Kind { get; }
	public override ExpressionType NodeType { get; }
	public LabelTarget Target { get; }
	public override System.Type Type { get; }
	public Expression Value { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public GotoExpression Update (LabelTarget target, Expression value);
}
```

### New Type System.Linq.Expressions.GotoExpressionKind

```
[Serializable]
public enum GotoExpressionKind {
	Break = 2,
	Continue = 3,
	Goto = 0,
	Return = 1,
}
```

### New Type System.Linq.Expressions.IndexExpression

```
public sealed class IndexExpression : System.Linq.Expressions.Expression {
	// properties
	public System.Collections.ObjectModel.ReadOnlyCollection<Expression> Arguments { get; }
	public System.Reflection.PropertyInfo Indexer { get; }
	public override ExpressionType NodeType { get; }
	public Expression Object { get; }
	public override System.Type Type { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public IndexExpression Update (Expression object, System.Collections.Generic.IEnumerable<Expression> arguments);
}
```

### New Type System.Linq.Expressions.LabelExpression

```
public sealed class LabelExpression : System.Linq.Expressions.Expression {
	// properties
	public Expression DefaultValue { get; }
	public override ExpressionType NodeType { get; }
	public LabelTarget Target { get; }
	public override System.Type Type { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public LabelExpression Update (LabelTarget target, Expression defaultValue);
}
```

### New Type System.Linq.Expressions.LabelTarget

```
public sealed class LabelTarget {
	// properties
	public string Name { get; }
	public System.Type Type { get; }
	// methods
	public override string ToString ();
}
```

### New Type System.Linq.Expressions.LoopExpression

```
public sealed class LoopExpression : System.Linq.Expressions.Expression {
	// properties
	public Expression Body { get; }
	public LabelTarget BreakLabel { get; }
	public LabelTarget ContinueLabel { get; }
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public LoopExpression Update (LabelTarget breakLabel, LabelTarget continueLabel, Expression body);
}
```

### New Type System.Linq.Expressions.RuntimeVariablesExpression

```
public sealed class RuntimeVariablesExpression : System.Linq.Expressions.Expression {
	// properties
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
	public System.Collections.ObjectModel.ReadOnlyCollection<ParameterExpression> Variables { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public RuntimeVariablesExpression Update (System.Collections.Generic.IEnumerable<ParameterExpression> variables);
}
```

### New Type System.Linq.Expressions.SwitchCase

```
public sealed class SwitchCase {
	// properties
	public Expression Body { get; }
	public System.Collections.ObjectModel.ReadOnlyCollection<Expression> TestValues { get; }
	// methods
	public override string ToString ();
	public SwitchCase Update (System.Collections.Generic.IEnumerable<Expression> testValues, Expression body);
}
```

### New Type System.Linq.Expressions.SwitchExpression

```
public sealed class SwitchExpression : System.Linq.Expressions.Expression {
	// properties
	public System.Collections.ObjectModel.ReadOnlyCollection<SwitchCase> Cases { get; }
	public System.Reflection.MethodInfo Comparison { get; }
	public Expression DefaultBody { get; }
	public override ExpressionType NodeType { get; }
	public Expression SwitchValue { get; }
	public override System.Type Type { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public SwitchExpression Update (Expression switchValue, System.Collections.Generic.IEnumerable<SwitchCase> cases, Expression defaultBody);
}
```

### New Type System.Linq.Expressions.SymbolDocumentInfo

```
public class SymbolDocumentInfo {
	// properties
	public virtual System.Guid DocumentType { get; }
	public string FileName { get; }
	public virtual System.Guid Language { get; }
	public virtual System.Guid LanguageVendor { get; }
}
```

### New Type System.Linq.Expressions.TryExpression

```
public sealed class TryExpression : System.Linq.Expressions.Expression {
	// properties
	public Expression Body { get; }
	public Expression Fault { get; }
	public Expression Finally { get; }
	public System.Collections.ObjectModel.ReadOnlyCollection<CatchBlock> Handlers { get; }
	public override ExpressionType NodeType { get; }
	public override System.Type Type { get; }
	// methods
	protected override Expression Accept (ExpressionVisitor visitor);
	public TryExpression Update (Expression body, System.Collections.Generic.IEnumerable<CatchBlock> handlers, Expression finally, Expression fault);
}
```

## Namespace System.Runtime.CompilerServices

### New Type System.Runtime.CompilerServices.CallSite

```
public class CallSite {
	// properties
	public CallSiteBinder Binder { get; }
	// methods
	public static CallSite Create (System.Type delegateType, CallSiteBinder binder);
}
```

### New Type System.Runtime.CompilerServices.CallSite`1

```
public class CallSite`1 : System.Runtime.CompilerServices.CallSite {
	// fields
	public T Target;
	// properties
	public T Update { get; }
	// methods
	public static System.Runtime.CompilerServices.CallSite<T> Create (CallSiteBinder binder);
}
```

### New Type System.Runtime.CompilerServices.CallSiteBinder

```
public abstract class CallSiteBinder {
	// constructors
	protected CallSiteBinder ();
	// properties
	public static System.Linq.Expressions.LabelTarget UpdateLabel { get; }
	// methods
	public virtual System.Linq.Expressions.Expression Bind (System.Object[] args, System.Collections.ObjectModel.ReadOnlyCollection<System.Linq.Expressions.ParameterExpression> parameters, System.Linq.Expressions.LabelTarget returnLabel);
	public virtual T BindDelegate<T> (System.Runtime.CompilerServices.CallSite<T> site, System.Object[] args);
	protected void CacheTarget<T> (T target);
}
```

### New Type System.Runtime.CompilerServices.CallSiteHelpers

```
public static class CallSiteHelpers {
	// methods
	public static bool IsInternalFrame (System.Reflection.MethodBase mb);
}
```

### New Type System.Runtime.CompilerServices.CallSiteOps

```
public static class CallSiteOps {
	// methods
	[Obsolete ("do not use this method")]
	public static void AddRule<T> (System.Runtime.CompilerServices.CallSite<T> site, T rule);

	[Obsolete ("do not use this method")]
	public static T Bind<T> (CallSiteBinder binder, System.Runtime.CompilerServices.CallSite<T> site, System.Object[] args);

	[Obsolete ("do not use this method")]
	public static void ClearMatch (CallSite site);

	[Obsolete ("do not use this method")]
	public static System.Runtime.CompilerServices.CallSite<T> CreateMatchmaker<T> (System.Runtime.CompilerServices.CallSite<T> site);

	[Obsolete ("do not use this method")]
	public static T[] GetCachedRules<T> (System.Runtime.CompilerServices.RuleCache<T> cache);

	[Obsolete ("do not use this method")]
	public static bool GetMatch (CallSite site);

	[Obsolete ("do not use this method")]
	public static System.Runtime.CompilerServices.RuleCache<T> GetRuleCache<T> (System.Runtime.CompilerServices.CallSite<T> site);

	[Obsolete ("do not use this method")]
	public static T[] GetRules<T> (System.Runtime.CompilerServices.CallSite<T> site);

	[Obsolete ("do not use this method")]
	public static void MoveRule<T> (System.Runtime.CompilerServices.RuleCache<T> cache, T rule, int i);

	[Obsolete ("do not use this method")]
	public static bool SetNotMatched (CallSite site);

	[Obsolete ("do not use this method")]
	public static void UpdateRules<T> (System.Runtime.CompilerServices.CallSite<T> this, int matched);

}
```

### New Type System.Runtime.CompilerServices.Closure

```
public sealed class Closure {
	// constructors
	public Closure (System.Object[] constants, System.Object[] locals);
	// fields
	public System.Object[] Constants;
	public System.Object[] Locals;
}
```

### New Type System.Runtime.CompilerServices.DebugInfoGenerator

```
public abstract class DebugInfoGenerator {
	// constructors
	protected DebugInfoGenerator ();
	// methods
	public virtual void MarkSequencePoint (System.Linq.Expressions.LambdaExpression method, int ilOffset, System.Linq.Expressions.DebugInfoExpression sequencePoint);
}
```

### New Type System.Runtime.CompilerServices.DynamicAttribute

```
public sealed class DynamicAttribute : System.Attribute {
	// constructors
	public DynamicAttribute ();
	public DynamicAttribute (System.Boolean[] transformFlags);
	// properties
	public System.Collections.Generic.IList<bool> TransformFlags { get; }
}
```

### New Type System.Runtime.CompilerServices.IRuntimeVariables

```
public interface IRuntimeVariables {
	// properties
	public virtual int Count { get; }
	public virtual object Item { get; set; }
}
```

### New Type System.Runtime.CompilerServices.ReadOnlyCollectionBuilder`1

```
[Serializable]
public sealed class ReadOnlyCollectionBuilder`1 : System.Collections.Generic.IList<T>, System.Collections.IList, System.Collections.Generic.ICollection<T>, System.Collections.Generic.IEnumerable<T>, System.Collections.IEnumerable, System.Collections.ICollection {
	// constructors
	public ReadOnlyCollectionBuilder`1 ();
	public ReadOnlyCollectionBuilder`1 (int capacity);
	public ReadOnlyCollectionBuilder`1 (System.Collections.Generic.IEnumerable<T> collection);
	// properties
	public int Capacity { get; set; }
	public virtual int Count { get; }
	public virtual T Item { get; set; }
	// methods
	public virtual void Add (T item);
	public virtual void Clear ();
	public virtual bool Contains (T item);
	public virtual void CopyTo (T[] array, int arrayIndex);
	public virtual System.Collections.Generic.IEnumerator<T> GetEnumerator ();
	public virtual int IndexOf (T item);
	public virtual void Insert (int index, T item);
	public virtual bool Remove (T item);
	public virtual void RemoveAt (int index);
	public void Reverse ();
	public void Reverse (int index, int count);
	public T[] ToArray ();
	public System.Collections.ObjectModel.ReadOnlyCollection<T> ToReadOnlyCollection ();
}
```

### New Type System.Runtime.CompilerServices.RuleCache`1

```
public class RuleCache`1 {
}
```

### New Type System.Runtime.CompilerServices.RuntimeOps

```
public static class RuntimeOps {
	// methods
	[Obsolete ("do not use this method")]
	public static bool ExpandoCheckVersion (System.Dynamic.ExpandoObject expando, object version);

	[Obsolete ("do not use this method")]
	public static void ExpandoPromoteClass (System.Dynamic.ExpandoObject expando, object oldClass, object newClass);

	[Obsolete ("do not use this method")]
	public static bool ExpandoTryDeleteValue (System.Dynamic.ExpandoObject expando, object indexClass, int index, string name, bool ignoreCase);

	[Obsolete ("do not use this method")]
	public static bool ExpandoTryGetValue (System.Dynamic.ExpandoObject expando, object indexClass, int index, string name, bool ignoreCase, System.Object& value);

	[Obsolete ("do not use this method")]
	public static object ExpandoTrySetValue (System.Dynamic.ExpandoObject expando, object indexClass, int index, object value, string name, bool ignoreCase);

}
```

## New Namespace System.Dynamic

### New Type System.Dynamic.BinaryOperationBinder

```
public abstract class BinaryOperationBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected BinaryOperationBinder (System.Linq.Expressions.ExpressionType operation);
	// properties
	public System.Linq.Expressions.ExpressionType Operation { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackBinaryOperation (DynamicMetaObject target, DynamicMetaObject arg);
	public virtual DynamicMetaObject FallbackBinaryOperation (DynamicMetaObject target, DynamicMetaObject arg, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.BindingRestrictions

```
public abstract class BindingRestrictions {
	// fields
	public static BindingRestrictions Empty;
	// methods
	public static BindingRestrictions Combine (System.Collections.Generic.IList<DynamicMetaObject> contributingObjects);
	public static BindingRestrictions GetExpressionRestriction (System.Linq.Expressions.Expression expression);
	public static BindingRestrictions GetInstanceRestriction (System.Linq.Expressions.Expression expression, object instance);
	public static BindingRestrictions GetTypeRestriction (System.Linq.Expressions.Expression expression, System.Type type);
	public BindingRestrictions Merge (BindingRestrictions restrictions);
	public System.Linq.Expressions.Expression ToExpression ();
}
```

### New Type System.Dynamic.CallInfo

```
public sealed class CallInfo {
	// constructors
	public CallInfo (int argCount, System.String[] argNames);
	public CallInfo (int argCount, System.Collections.Generic.IEnumerable<string> argNames);
	// properties
	public int ArgumentCount { get; }
	public System.Collections.ObjectModel.ReadOnlyCollection<string> ArgumentNames { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.Dynamic.ConvertBinder

```
public abstract class ConvertBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected ConvertBinder (System.Type type, bool explicit);
	// properties
	public bool Explicit { get; }
	public override System.Type ReturnType { get; }
	public System.Type Type { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackConvert (DynamicMetaObject target);
	public virtual DynamicMetaObject FallbackConvert (DynamicMetaObject target, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.CreateInstanceBinder

```
public abstract class CreateInstanceBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected CreateInstanceBinder (CallInfo callInfo);
	// properties
	public CallInfo CallInfo { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackCreateInstance (DynamicMetaObject target, DynamicMetaObject[] args);
	public virtual DynamicMetaObject FallbackCreateInstance (DynamicMetaObject target, DynamicMetaObject[] args, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.DeleteIndexBinder

```
public abstract class DeleteIndexBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected DeleteIndexBinder (CallInfo callInfo);
	// properties
	public CallInfo CallInfo { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackDeleteIndex (DynamicMetaObject target, DynamicMetaObject[] indexes);
	public virtual DynamicMetaObject FallbackDeleteIndex (DynamicMetaObject target, DynamicMetaObject[] indexes, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.DeleteMemberBinder

```
public abstract class DeleteMemberBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected DeleteMemberBinder (string name, bool ignoreCase);
	// properties
	public bool IgnoreCase { get; }
	public string Name { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackDeleteMember (DynamicMetaObject target);
	public virtual DynamicMetaObject FallbackDeleteMember (DynamicMetaObject target, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.DynamicMetaObject

```
public class DynamicMetaObject {
	// constructors
	public DynamicMetaObject (System.Linq.Expressions.Expression expression, BindingRestrictions restrictions);
	public DynamicMetaObject (System.Linq.Expressions.Expression expression, BindingRestrictions restrictions, object value);
	// fields
	public static DynamicMetaObject[] EmptyMetaObjects;
	// properties
	public System.Linq.Expressions.Expression Expression { get; }
	public bool HasValue { get; }
	public System.Type LimitType { get; }
	public BindingRestrictions Restrictions { get; }
	public System.Type RuntimeType { get; }
	public object Value { get; }
	// methods
	public virtual DynamicMetaObject BindBinaryOperation (BinaryOperationBinder binder, DynamicMetaObject arg);
	public virtual DynamicMetaObject BindConvert (ConvertBinder binder);
	public virtual DynamicMetaObject BindCreateInstance (CreateInstanceBinder binder, DynamicMetaObject[] args);
	public virtual DynamicMetaObject BindDeleteIndex (DeleteIndexBinder binder, DynamicMetaObject[] indexes);
	public virtual DynamicMetaObject BindDeleteMember (DeleteMemberBinder binder);
	public virtual DynamicMetaObject BindGetIndex (GetIndexBinder binder, DynamicMetaObject[] indexes);
	public virtual DynamicMetaObject BindGetMember (GetMemberBinder binder);
	public virtual DynamicMetaObject BindInvoke (InvokeBinder binder, DynamicMetaObject[] args);
	public virtual DynamicMetaObject BindInvokeMember (InvokeMemberBinder binder, DynamicMetaObject[] args);
	public virtual DynamicMetaObject BindSetIndex (SetIndexBinder binder, DynamicMetaObject[] indexes, DynamicMetaObject value);
	public virtual DynamicMetaObject BindSetMember (SetMemberBinder binder, DynamicMetaObject value);
	public virtual DynamicMetaObject BindUnaryOperation (UnaryOperationBinder binder);
	public static DynamicMetaObject Create (object value, System.Linq.Expressions.Expression expression);
	public virtual System.Collections.Generic.IEnumerable<string> GetDynamicMemberNames ();
}
```

### New Type System.Dynamic.DynamicMetaObjectBinder

```
public abstract class DynamicMetaObjectBinder : System.Runtime.CompilerServices.CallSiteBinder {
	// constructors
	protected DynamicMetaObjectBinder ();
	// properties
	public virtual System.Type ReturnType { get; }
	// methods
	public override System.Linq.Expressions.Expression Bind (System.Object[] args, System.Collections.ObjectModel.ReadOnlyCollection<System.Linq.Expressions.ParameterExpression> parameters, System.Linq.Expressions.LabelTarget returnLabel);
	public virtual DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject Defer (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject Defer (DynamicMetaObject[] args);
	public System.Linq.Expressions.Expression GetUpdateExpression (System.Type type);
}
```

### New Type System.Dynamic.DynamicObject

```
[Serializable]
public class DynamicObject : IDynamicMetaObjectProvider {
	// constructors
	protected DynamicObject ();
	// methods
	public virtual System.Collections.Generic.IEnumerable<string> GetDynamicMemberNames ();
	public virtual DynamicMetaObject GetMetaObject (System.Linq.Expressions.Expression parameter);
	public virtual bool TryBinaryOperation (BinaryOperationBinder binder, object arg, System.Object& result);
	public virtual bool TryConvert (ConvertBinder binder, System.Object& result);
	public virtual bool TryCreateInstance (CreateInstanceBinder binder, System.Object[] args, System.Object& result);
	public virtual bool TryDeleteIndex (DeleteIndexBinder binder, System.Object[] indexes);
	public virtual bool TryDeleteMember (DeleteMemberBinder binder);
	public virtual bool TryGetIndex (GetIndexBinder binder, System.Object[] indexes, System.Object& result);
	public virtual bool TryGetMember (GetMemberBinder binder, System.Object& result);
	public virtual bool TryInvoke (InvokeBinder binder, System.Object[] args, System.Object& result);
	public virtual bool TryInvokeMember (InvokeMemberBinder binder, System.Object[] args, System.Object& result);
	public virtual bool TrySetIndex (SetIndexBinder binder, System.Object[] indexes, object value);
	public virtual bool TrySetMember (SetMemberBinder binder, object value);
	public virtual bool TryUnaryOperation (UnaryOperationBinder binder, System.Object& result);
}
```

### New Type System.Dynamic.ExpandoObject

```
public sealed class ExpandoObject : IDynamicMetaObjectProvider, System.Collections.Generic.IDictionary<System.String,System.Object>, System.ComponentModel.INotifyPropertyChanged, System.Collections.Generic.ICollection<System.Collections.Generic.KeyValuePair<System.String,System.Object>>, System.Collections.Generic.IEnumerable<System.Collections.Generic.KeyValuePair<System.String,System.Object>>, System.Collections.IEnumerable {
	// constructors
	public ExpandoObject ();
}
```

### New Type System.Dynamic.GetIndexBinder

```
public abstract class GetIndexBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected GetIndexBinder (CallInfo callInfo);
	// properties
	public CallInfo CallInfo { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackGetIndex (DynamicMetaObject target, DynamicMetaObject[] indexes);
	public virtual DynamicMetaObject FallbackGetIndex (DynamicMetaObject target, DynamicMetaObject[] indexes, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.GetMemberBinder

```
public abstract class GetMemberBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected GetMemberBinder (string name, bool ignoreCase);
	// properties
	public bool IgnoreCase { get; }
	public string Name { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackGetMember (DynamicMetaObject target);
	public virtual DynamicMetaObject FallbackGetMember (DynamicMetaObject target, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.IDynamicMetaObjectProvider

```
public interface IDynamicMetaObjectProvider {
	// methods
	public virtual DynamicMetaObject GetMetaObject (System.Linq.Expressions.Expression parameter);
}
```

### New Type System.Dynamic.IInvokeOnGetBinder

```
public interface IInvokeOnGetBinder {
	// properties
	public virtual bool InvokeOnGet { get; }
}
```

### New Type System.Dynamic.InvokeBinder

```
public abstract class InvokeBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected InvokeBinder (CallInfo callInfo);
	// properties
	public CallInfo CallInfo { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackInvoke (DynamicMetaObject target, DynamicMetaObject[] args);
	public virtual DynamicMetaObject FallbackInvoke (DynamicMetaObject target, DynamicMetaObject[] args, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.InvokeMemberBinder

```
public abstract class InvokeMemberBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected InvokeMemberBinder (string name, bool ignoreCase, CallInfo callInfo);
	// properties
	public CallInfo CallInfo { get; }
	public bool IgnoreCase { get; }
	public string Name { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public virtual DynamicMetaObject FallbackInvoke (DynamicMetaObject target, DynamicMetaObject[] args, DynamicMetaObject errorSuggestion);
	public DynamicMetaObject FallbackInvokeMember (DynamicMetaObject target, DynamicMetaObject[] args);
	public virtual DynamicMetaObject FallbackInvokeMember (DynamicMetaObject target, DynamicMetaObject[] args, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.SetIndexBinder

```
public abstract class SetIndexBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected SetIndexBinder (CallInfo callInfo);
	// properties
	public CallInfo CallInfo { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackSetIndex (DynamicMetaObject target, DynamicMetaObject[] indexes, DynamicMetaObject value);
	public virtual DynamicMetaObject FallbackSetIndex (DynamicMetaObject target, DynamicMetaObject[] indexes, DynamicMetaObject value, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.SetMemberBinder

```
public abstract class SetMemberBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected SetMemberBinder (string name, bool ignoreCase);
	// properties
	public bool IgnoreCase { get; }
	public string Name { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackSetMember (DynamicMetaObject target, DynamicMetaObject value);
	public virtual DynamicMetaObject FallbackSetMember (DynamicMetaObject target, DynamicMetaObject value, DynamicMetaObject errorSuggestion);
}
```

### New Type System.Dynamic.UnaryOperationBinder

```
public abstract class UnaryOperationBinder : System.Dynamic.DynamicMetaObjectBinder {
	// constructors
	protected UnaryOperationBinder (System.Linq.Expressions.ExpressionType operation);
	// properties
	public System.Linq.Expressions.ExpressionType Operation { get; }
	public override System.Type ReturnType { get; }
	// methods
	public override DynamicMetaObject Bind (DynamicMetaObject target, DynamicMetaObject[] args);
	public DynamicMetaObject FallbackUnaryOperation (DynamicMetaObject target);
	public virtual DynamicMetaObject FallbackUnaryOperation (DynamicMetaObject target, DynamicMetaObject errorSuggestion);
}
```

   


 <hr>

# System.ServiceModel.Web.dll

## Namespace System

### Type Changed: System.UriTemplate

Removed methods:

```
public Uri BindByName (Uri baseAddress, object parameters);
	public Uri BindByName (Uri baseAddress, object parameters, bool omitDefaults);
```

Added methods:

```
public Uri BindByName (Uri baseAddress, Collections.Specialized.NameValueCollection parameters);
	public Uri BindByName (Uri baseAddress, Collections.Specialized.NameValueCollection parameters, bool omitDefaults);
```

### Type Changed: System.UriTemplateMatch

Removed properties:

```
public System.Collections.Generic.Dictionary<String,System.String> BoundVariables { get; }
	public System.Collections.Generic.Dictionary<String,System.String> QueryParameters { get; }
```

Added properties:

```
public Collections.Specialized.NameValueCollection BoundVariables { get; }
	public Collections.Specialized.NameValueCollection QueryParameters { get; }
```

## Namespace System.ServiceModel

### Type Changed: System.ServiceModel.WebHttpBinding

Added interfaces:

```
Channels.IBindingRuntimePreferences
```

   


 <hr>

# Mono.Data.Tds.dll

## Namespace Mono.Data.Tds

### Type Changed: Mono.Data.Tds.TdsMetaParameter

Added fields:

```
public static const int maxNVarCharCharacters;
	public static const int maxVarCharCharacters;
```

Added properties:

```
public bool IsAnyVarCharMax { get; }
	public bool IsDateTimeType { get; }
	public bool IsDecimalType { get; }
	public bool IsMoneyType { get; }
	public bool IsNonUnicodeText { get; }
	public bool IsTextType { get; }
	public bool IsVarCharMax { get; }
	public bool IsVarNVarCharMax { get; }
```

Added methods:

```
public void CalculateIsVariableType ();
```

## Namespace Mono.Data.Tds.Protocol

### Type Changed: Mono.Data.Tds.Protocol.TdsBulkCopy

Removed methods:

```
public bool BulkCopyData (object o, int size, bool isNewRow);
```

Added methods:

```
public bool BulkCopyData (object o, bool isNewRow, int size, Mono.Data.Tds.TdsMetaParameter parameter);
```

   


 <hr>

# Mono.Security.dll

## Namespace Mono.Security.Protocol.Ntlm

### Type Changed: Mono.Security.Protocol.Ntlm.Type3Message

Removed properties:

```
public static NtlmAuthLevel DefaultAuthLevel { get; set; }
```

Added properties:

```
[Obsolete ("Use NtlmSettings.DefaultAuthLevel")]
	public static NtlmAuthLevel DefaultAuthLevel { get; set; }
```

### New Type Mono.Security.Protocol.Ntlm.NtlmSettings

```
public static class NtlmSettings {
	// properties
	public static NtlmAuthLevel DefaultAuthLevel { get; set; }
}
```

## Namespace Mono.Security.Protocol.Tls

### Type Changed: Mono.Security.Protocol.Tls.SecurityProtocolType

Added values:

```
Tls11 = 768,
	Tls12 = 3072,
```

   


 <hr>

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string Version = "7.2.0";
```

Added fields:

```
public static const string Version = "7.2.1";
```

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.MusicTrack

Added properties:

```
public double TrackLength { get; set; }
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAudioSession

Added methods:

```
public MonoTouch.Foundation.NSError SetActive (bool beActive);
	public MonoTouch.Foundation.NSError SetActive (bool active, AVAudioSessionSetActiveOptions options);
	public MonoTouch.Foundation.NSError SetCategory (MonoTouch.Foundation.NSString theCategory);
	public MonoTouch.Foundation.NSError SetCategory (AVAudioSessionCategory category);
	public MonoTouch.Foundation.NSError SetCategory (AVAudioSessionCategory category, AVAudioSessionCategoryOptions options);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureAudioDataOutput

Added methods:

```
public void SetSampleBufferDelegateQueue (IAVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, MonoTouch.CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutput

Added methods:

```
public void SetSampleBufferDelegateQueue (IAVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, MonoTouch.CoreFoundation.DispatchQueue sampleBufferCallbackQueue);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate

Added methods:

```
public virtual void DidDropSampleBuffer (AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate_Extensions

Added methods:

```
public static void DidDropSampleBuffer (IAVCaptureVideoDataOutputSampleBufferDelegate This, AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
```

### New Type MonoTouch.AVFoundation.AVAudioSessionCategory

```
[Serializable]
public enum AVAudioSessionCategory {
	Ambient = 0,
	AudioProcessing = 5,
	MultiRoute = 6,
	PlayAndRecord = 4,
	Playback = 2,
	Record = 3,
	SoloAmbient = 1,
}
```

## Namespace MonoTouch.CoreData

### Type Changed: MonoTouch.CoreData.NSFetchedResultsControllerDelegate

Removed methods:

```
public virtual void DidChangeSection (NSFetchedResultsController controller, NSFetchedResultsSectionInfo sectionInfo, uint sectionIndex, NSFetchedResultsChangeType type);
```

Added methods:

```
public virtual void DidChangeSection (NSFetchedResultsController controller, INSFetchedResultsSectionInfo sectionInfo, uint sectionIndex, NSFetchedResultsChangeType type);
```

### Type Changed: MonoTouch.CoreData.NSFetchedResultsControllerDelegate_Extensions

Removed methods:

```
public static void DidChangeSection (INSFetchedResultsControllerDelegate This, NSFetchedResultsController controller, NSFetchedResultsSectionInfo sectionInfo, uint sectionIndex, NSFetchedResultsChangeType type);
```

Added methods:

```
public static void DidChangeSection (INSFetchedResultsControllerDelegate This, NSFetchedResultsController controller, INSFetchedResultsSectionInfo sectionInfo, uint sectionIndex, NSFetchedResultsChangeType type);
```

### Type Changed: MonoTouch.CoreData.NSManagedObject

Removed methods:

```
public virtual bool ValidateValue (MonoTouch.Foundation.NSObject value, string key, MonoTouch.Foundation.NSError& error);
```

Added methods:

```
public virtual void PrepareForDeletion ();
	public virtual bool ValidateValue (MonoTouch.Foundation.NSObject& value, string key, MonoTouch.Foundation.NSError& error);
```

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFRunLoopSource

Added constructors:

```
public CFRunLoopSource (System.IntPtr handle);
	public CFRunLoopSource (System.IntPtr handle, bool ownsHandle);
```

### Type Changed: MonoTouch.CoreFoundation.CFType

Added methods:

```
public static bool Equal (System.IntPtr cf1, System.IntPtr cf2);
```

### Type Changed: MonoTouch.CoreFoundation.DispatchGroup

Added methods:

```
public void Notify (DispatchQueue queue, MonoTouch.Foundation.NSAction action);
```

### Type Changed: MonoTouch.CoreFoundation.DispatchQueuePriority

Added values:

```
Background = -32768,
```

## Namespace MonoTouch.CoreMidi

### Type Changed: MonoTouch.CoreMidi.MidiClient

Added methods:

```
public MidiEndpoint CreateVirtualDestination (string name, MidiError& status);
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.MonoTouchException

Added methods:

```
public override string ToString ();
```

### Type Changed: MonoTouch.Foundation.NSAttributedString

Added methods:

```
public static NSAttributedString CreateFrom (MonoTouch.UIKit.NSTextAttachment attachment);
```

### Type Changed: MonoTouch.Foundation.NSNetService

Removed properties:

```
[Obsolete ("Deprecated in iOS 6.1 and OSX 10.8")]
	public virtual NSData[] Addresses { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OSX 10.8")]
	public virtual string Domain { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OSX 10.8")]
	public virtual string HostName { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OSX 10.8")]
	public virtual string Name { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OSX 10.8")]
	public virtual int Port { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OSX 10.8")]
	public virtual string Type { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OSX 10.8")]
	public virtual NSObject WeakDelegate { get; set; }
```

Added properties:

```
public virtual NSData[] Addresses { get; }
	public virtual string Domain { get; }
	public virtual string HostName { get; }
	public virtual string Name { get; }
	public virtual int Port { get; }
	public virtual string Type { get; }
	public virtual NSObject WeakDelegate { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSObject

Removed methods:

```
public NSObject Autorelease ();
	protected static bool IsNewRefcountEnabled ();
	public void Release ();
	public NSObject Retain ();
```

Added methods:

```
[Obsolete ("Low-level API warning: Use at your own risk: this calls the Retain method on the underlying object; Use DangerousAutorelease to avoid this warning")]
	public NSObject Autorelease ();

	public NSObject DangerousAutorelease ();
	public void DangerousRelease ();
	public NSObject DangerousRetain ();
	public static bool IsNewRefcountEnabled ();
	[Obsolete ("Low-level API warning: Use at your own risk: this calls the Release method on the underlying object;  Use DangerousRelease to avoid this warning")]
	public void Release ();

	[Obsolete ("Low-level API warning: Use at your own risk: this calls the Retain method on the underlying object; Use DangerousRetain to avoid this warning")]
	public NSObject Retain ();
```

### Type Changed: MonoTouch.Foundation.NSPortMessage

Removed properties:

```
public virtual uint MsgId { get; set; }
	public virtual NSPort ReceivePort { get; }
	public virtual NSPort SendPort { get; }
```

Added properties:

```
[Obsolete ("Only available on OSX")]
	public virtual uint MsgId { get; set; }

	[Obsolete ("Only available on OSX")]
	public virtual NSPort ReceivePort { get; }

	[Obsolete ("Only available on OSX")]
	public virtual NSPort SendPort { get; }
```

Removed methods:

```
public virtual bool SendBefore (NSDate date);
```

Added methods:

```
[Obsolete ("Only available on OSX")]
	public virtual bool SendBefore (NSDate date);
```

### New Type MonoTouch.Foundation.NSSortDescriptorSorting_NSMutableArray

```
public static class NSSortDescriptorSorting_NSMutableArray {
	// methods
	public static void SortUsingDescriptors (NSMutableArray This, NSSortDescriptor[] sortDescriptors);
}
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKChallenge

Added methods:

```
public override string ToString ();
```

### Type Changed: MonoTouch.GameKit.GKMatch

Removed events:

```
[Obsolete ("No longer on iOS")]
	public event System.EventHandler<GKPlayerErrorEventArgs> ConnectionFailed;
```

Added events:

```
[Obsolete ("No longer an iOS API - it will never be called")]
	public event System.EventHandler<GKPlayerErrorEventArgs> ConnectionFailed;
```

### Type Changed: MonoTouch.GameKit.GKMatchDelegate

Removed methods:

```
[Obsolete ("No longer on iOS")]
	public virtual void ConnectionFailed (GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
```

Added methods:

```
[Obsolete ("No longer an iOS API - it will never be called")]
	public virtual void ConnectionFailed (GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.GameKit.GKMatchDelegate_Extensions

Removed methods:

```
[Obsolete ("No longer on iOS")]
	public static void ConnectionFailed (IGKMatchDelegate This, GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
```

Added methods:

```
[Obsolete ("No longer an iOS API - it will never be called")]
	public static void ConnectionFailed (IGKMatchDelegate This, GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.ArgumentSemantic

Added values:

```
Strong = 2,
	UnsafeUnretained = 0,
	Weak = 3,
```

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

```
public static void void_objc_msgSend_IntPtr_int_float (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, float arg3);
	public static void void_objc_msgSendSuper_IntPtr_int_float (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, float arg3);
```

### New Type MonoTouch.ObjCRuntime.ReleaseAttribute

```
public class ReleaseAttribute : System.Attribute {
	// constructors
	public ReleaseAttribute ();
}
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIBezierPath

Added methods:

```
public void SetLineDash (System.Single[] values, float phase);
	public void SetLineDash (System.Single[] values, int offset, int count, float phase);
```

### Type Changed: MonoTouch.UIKit.UIPercentDrivenInteractiveTransition

Removed interfaces:

```
IUIPercentDrivenInteractiveTransition
```

Added interfaces:

```
IUIViewControllerInteractiveTransitioning
```

### Type Changed: MonoTouch.UIKit.UITableView

### Type Changed: MonoTouch.UIKit.UITableView.UITableViewAppearance

Added properties:

```
public virtual UIColor SectionIndexBackgroundColor { get; set; }
	public virtual UIEdgeInsets SeparatorInset { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIViewController

Added methods:

```
public static void PrepareForInterstitialAds ();
```

### Removed Type MonoTouch.UIKit.IUIPercentDrivenInteractiveTransition ### Removed Type MonoTouch.UIKit.UIPercentDrivenInteractiveTransition_Extensions    
 <hr>
